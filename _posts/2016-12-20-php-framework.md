---
layout: post
title:  "php框架"
tags:
categories:
---

##  从零开始搭建php框架

.htaccess文件 '/.htaccess'

```
<IfModule mod_rewrite.c>
    RewriteEngine on
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteRule ^(.*)$ index.php/$1 [QSA,PT,L]
</IfModule>
```


入口文件 `/index.php`

```php
<?php
// 整个框架所在的根目录
define ('UEK', realpath('./'));

// 核心类所有在目录
define ('CORE', UEK.'/core');

// APP开发目录
define ('APP', UEK.'/app');

// 是否开启调试模式
define ('DEBUG', true);

if( DEBUG ){
  ini_set('display_errors', 'On');
}else{
  ini_set('display_errors', 'Off');
}

// 引入公共函数库
include CORE . '/common/function.php';

// 引入框架核心类
include CORE . '/uek.php';

// 如果new一个不存在的类，则调用\core\uek类中的load方法
spl_autoload_register('\core\uek::load');

// 调用uek类中的run方法启动整个框架
\core\uek::run();
```

公共函数库 `/core/common/function.php`

```php
<?php
function p($var)
{
  if( is_bool($var) ){
    var_dump($var);
  }else if( is_null ($var) ){
    var_dump($var);
  }else{
    echo '<pre>' . print_r($var, true) . '</pre>';
  }
}
```

框架核心类 `/core/uek.php`

```php
<?php
namespace core;
class uek
{
  // 缓存已经加载过的类
  public static $class_map = array();

  // 保存要输出到视图中的变量
  public $assign;

  // 框架启动方法 调用路由类管理路由
  static public function run()
  {
    // 当前并没有include route类文件 会触发spl_autoload_register() 函数中指定的方法
    // 也就是本类中的 load() 方法
    // spl_autoload_register函数会把 \core\lib\route 作为字符串传递给load()

    $route = new \core\lib\route();

    $controller_class = $route->controller;
    $action = $route->action;

    // 根据路由规则找到app下对应的类文件， 根据路由规则运行其中的方法
    $controller_file = APP . '/controller/' . $controller_class . 'Controller.php';
    if( is_file($controller_file) ){
      include $controller_file;
      $class_name =  '\\app\\controller\\'.$controller_class.'Controller';
      $controller = new $class_name();
      $controller->$action();
    }else{
      throw new \Exception("can't find module");
    }

  }

  // 自动加载一个类文件
  public static function load($class)
  {
    // 存在于缓存中
    if( isset($class_map[$class])){
      return true;
    }else{
      // 根据命名空间规则找到对应的类文件
      $file  = UEK . '/' . str_replace('\\', '/', $class) . '.php';

      if( is_file($file) ){
        include $file;
        // 如果已经include过,利用类名做一次缓存
        self::$class_map[$class] = $class;
      }else{
        return false;
      }
    }
  }

  public function assign($name, $value)
  {
    $this->assign[$name] = $value;
  }

  public function display($file)
  {
    $view_path = APP . '/' . $file;
    if(is_file($view_path)){
      extract($this->assign);
      include($view_path);
    }
  }
}
```

框架路由类 `/core/lib/route.php`

```php
<?php
namespace core\lib;
class route
{
  public $controller;
  public $action;

  // new 本类时会自动运行的方法
  public function __constructor()
  {
    // 根据用户访问的路径确定调用APP下哪个php文件中的哪个方法
    // 这里返回的只是$controller的名字和对应方法的名字
    // 这里还要处理用户的get传参
    if( isset( $_SERVER['REQUEST_URI'] ) &&  $_SERVER['REQUEST_URI'] !== '/' ){
      $path = $_SERVER['REQUEST_URI'];
      $params = explode('/', trim($path, '/'));

      if(isset($params[0])){
        $this->controller  = $params[0];
        unset($params[0]);
      }
      if(isset($params[1])){
        $this->action = $params[1];
        unset($params[1]);
      }else{
        $this->action = 'index';
      }

      // 将多余的参数收入$_GET
      // index/index/id/1/str/2/test/3
      for ($i = 2; $i < count($params) + 2; $i += 2) {
        if (isset($params[$i + 1])) {
          $_GET[$params[$i]] = $params[$i + 1];
        }
      }

    }else{
      // 用户访问 / 时候默认调用app下的 indexController.php 下的 index() 方法

      $this->controller = 'index';
      $this->action = 'index';
    }
  }
}
```

框架model类 利用pdo实现连接数据库 `/core/lib/model.php`

```php
<?php
namespace core\lib;
class model extends \PDO
{
  public function __construct()
  {
    $database_info = 'mysql:host=localhost;dbname=yarn';
    $username = 'root';
    $password = 'root';

    try{
      parent::__construct($database_info, $username, $password);
    } catch (\PDOException $e){
      p($e->getMessage());
    }
  }
}
```

用户首页类 `/app/controller/indexController.php`

```php
<?php
namespace app\controller;
// 继承框架核心文件
// 利用核心文件中的 assign 和 display 方法来管理视图

class indexController extends \core\uek
{
  public function index()
  {
    $model = new \core\lib\model();
    $sql = 'select * from todos';
    $result = $model->query($sql);
    p($result->fetchAll());
    p($_GET);

    $this->assign('data','hello world');
    $this->assign('title','facebook');
    $this->display('view/index.html');
  }
}
```

用户视图文件 '/app/view/index.html'

```html
<html>
<head>
  <meta charset='utf-8'>
  <title><?php echo $title ?></title>
</head>
<body>
  <div><?php echo $data ?></div>
</body>
</html>
```

db文件

```sql
SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET time_zone = "+00:00";

--
-- Database: `yarn`
--
CREATE DATABASE IF NOT EXISTS `yarn` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
USE `yarn`;

-- --------------------------------------------------------

--
-- 表的结构 `todos`
--

DROP TABLE IF EXISTS `todos`;
CREATE TABLE IF NOT EXISTS `todos` (
  `id` int(12) NOT NULL,
  `title` varchar(255) NOT NULL,
  `is_done` tinyint(1) NOT NULL,
  `is_del` tinyint(1) NOT NULL
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8;

--
-- 转存表中的数据 `todos`
--

INSERT INTO `todos` (`id`, `title`, `is_done`, `is_del`) VALUES
(1, 'buy a car', 0, 0),
(2, 'buy a mao', 0, 0);

--
-- Indexes for dumped tables
--

--
-- Indexes for table `todos`
--
ALTER TABLE `todos`
  ADD PRIMARY KEY (`id`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `todos`
--
ALTER TABLE `todos`
  MODIFY `id` int(12) NOT NULL AUTO_INCREMENT,AUTO_INCREMENT=3;
```

访问 `http://localhost/index/index`
