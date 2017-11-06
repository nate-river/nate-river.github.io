---
  layout: post
  title: 搭建前端自动化开发环境
  tags:
  categories:
---


>  随着`node.js`的迅猛发展,前端开发已经脱离了刀耕火种,进入蒸汽机时代。

>  这里介绍一些基于`node.js`的前端自动化开发工具:

## node.js  &&  npm

> Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient. Node.js' package ecosystem, npm, is the largest ecosystem of open source libraries in the world.

最简单的理解：

`node.js`又提供了一个javascript的运行环境,以前,javascript代码可以在浏览器中运行,现在,它可以在node.js所搭建的运行环境中运行了.

浏览器并不是一个理想的代码运行环境,浏览器在给javascript扩展API的时候,基于安全的考虑,很多功能都不能做.比如操作文件,随意的处理网络请求.所以,在以前,javascript相对于python,ruby 是一门`不完善的语言`.

在node.js这个运行环境中,并没有这样那样的限制,在这里,javascript成功变成了python,ruby,变成了一门`真正的语言`.

windows下 node.js 的安装很简单,访问[`node.js官网`](https://nodejs.org),下载安装包,默认安装就好.

打开控制台测试是否安装成功
```sh
node -v
```

`npm` 是node.js的包管理工具, node.js以模块的方式组织代码,允许任何人提交一个模块,来扩展javascript, npm用来管理这些模块

```sh
npm -v
npm install -g bower
```

如果有的包安装不上 复制以下代码替换 `x` 为安装不上的包 (会带来一定的问题,建议翻墙)

```sh
 npm install x --registry=http://registry.npm.taobao.org
```


## bower

`npm install -g bower`

包管理工具,把项目中所依赖的文件保存在bower.json中，只需分享给别人bower.json即可

`bower install`   

寻找bower.json文件 把依赖项全部安装

`bower install  在bower官网注册的库  --save`

安装一个库，把库作为依赖项写入bower.json  

`bower install  网址 --save`

`bower install  github短语  --save`

>  bower 依赖git
> 把git命令添加到环境变量的方法:
> 在c盘中搜索 git.exe  找到它所处的位置,添加到环境变量

## grunt && gulp

`npm install -g gulp`

[一个典型的gulp配置文件](https://github.com/yeoman/generator-webapp/blob/master/app/templates/gulpfile.js);

## yeomon

`npm install -g yo`

`npm install -g generator-webapp`

`yo webapp`

脚手架，一键自动生成一个配置好的项目，包括目录结构，项目依赖，开发依赖

一般和bower gulp 结合

自定义一个yeoman 包

详细步骤见: [创建一个脚手架](http://yeoman.io/authoring/)

大致如下


```sh
npm install -g generator-generator
yo generator
```

会生成一个目录结构

```
--generators/
----app/
------temlates/   此目录中放静态文件,以供拷贝
------index.js    默认会运行的文件

其他省略
```

编写index.js

```javascript
'use strict';
var path = require('path');
var yeoman = require('yeoman-generator');
var chalk = require('chalk');
var yosay = require('yosay');
var wiredep = require('wiredep');

var mkdirp = require('mkdirp');
var _s = require('underscore.string');

module.exports = yeoman.Base.extend({
  prompting: function () {
    // Have Yeoman greet the user.
    this.log(yosay(
      'Welcome to the remarkable ' + chalk.red('generator-mobile-app-myl') + ' generator!'
    ));

    var prompts = [
      {
        type: 'confirm',
        name: 'includeBootStrap',
        message: 'Would you like to use bootStrap?',
        default: true
      },
      {
        type: 'confirm',
        name: 'includeJquery',
        message: 'Would you like to use jQuery?',
        default: true
      },
      {
        type: 'confirm',
        name: 'includeTouch',
        message: 'Would you like to use Baidu Touch.js?',
        default: true
      },
      {
        type: 'confirm',
        name: 'includeSwiper',
        message: 'Would you like to use Swiper.js?',
        default: true
      },
      {
        type: 'input',
        name:'name',
        message :'you app name?',
        default:'mobile'
      }
    ];

    return this.prompt(prompts).then(function (props) {
      this.props = props;
    }.bind(this));
  },

  default: function(){
    if (path.basename(this.destinationPath()) !== this.props.name) {
      this.log(
        'Your generator must be inside a folder named ' + this.props.name + '\n' +
        'I\'ll automatically create this folder.'
      );
      mkdirp(this.props.name);
      this.destinationRoot(this.destinationPath(this.props.name));
    }
  },

  writing: function () {
    var packageJson = {
      "private": true,
      "devDependencies": {
        "gulp": "^3.9.0",
      }
    };
    this.fs.writeJSON('package.json',packageJson);

    var bowerJson = {
      name: this.appname,
      private: true,
      main: 'index.html',
      dependencies: {}
    };
    if(this.props.includeJquery){
      bowerJson.dependencies['jquery'] = '~2.1.1';
    }
    if(this.props.includeBootStrap){
      bowerJson.dependencies['bootstrap'] = '^3.3.6';
    }
    if(this.props.includeTouch){
      bowerJson.dependencies['touch.code.baidu.com'] = 'Clouda-team/touch.code.baidu.com';
    }
    if(this.props.includeSwiper){
      bowerJson.dependencies['Swiper'] = 'swiper#^3.3.1';
    }

    this.fs.writeJSON('bower.json',bowerJson);

    this.fs.copy(
      this.templatePath('main.js'),
      this.destinationPath('scripts/main.js')
    );

    this.fs.copy(
      this.templatePath('gitignore'),
      this.destinationPath('.gitignore')
    );

    this.fs.copy(
      this.templatePath('main.scss'),
      this.destinationPath('styles/main.scss')
    );
    this.fs.copy(
      this.templatePath('index.html'),
      this.destinationPath('index.html')
    );
    this.fs.copy(
      this.templatePath('touch/'),
      this.destinationPath('images/touch/')
    );
  },

  install: function(){
    this.installDependencies({ });
  },
  end:function(){
    wiredep({ src: 'index.html' });
  }
});
```

然后

```sh
npm link
```

随后就可以  `yo name` 了
