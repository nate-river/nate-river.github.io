---
  layout: post
  title:  Angularjs
  tags:
  categories:
---

## 1.安装引用

在 http://www.bootcdn.cn/ 中搜索 `angular` 下载

```html
<script src="pathto/angular.js"></script>
```


## 2.简单使用

```html
<!DOCTYPE html>
<!-- 这里使用 ng-app 指令  -->
<html  ng-app="reminder">
  <head>
    <meta charset="utf-8">
    <title></title>
    <script src="angualr.js" charset="utf-8"></script>
  </head>
  <!-- 这里使用 ng-controller -->
  <body ng-controller="mainControler">
    <!-- ng-model指令 会在作用域中的 $scope 上 放置一个 info 的属性  值为input的值 -->
    <input type="text" name="name" value="" ng-model="info">
    <!-- 双花括号中可以写 angular 表达式  下面写法为取出 $scope上的 info 属性的值-->
    <p>{{info}}</p>
  </body>
  <!-- controller的作用域范围在这里结束-->
</html>
```

## 3.以模块化的方式来开发自己的应用 和 依赖注入

```html
<!DOCTYPE html>
<html  ng-app="reminder">
  <head>
    <meta charset="utf-8">
    <title></title>
    <script src="angular.js"></script>
    <script src="index.js"></script>
  </head>
  <body ng-controller="mainControler">
    <table>
      <thead>
          <th>
              <td>姓名</td>
              <td>学号</td>
              <td>性别</td>
          </th>
      </thead>
      <tbody>
          <!-- ng-repeat 指令能从作用的$scopes身上取到数据，帮我们完成渲染-->
          <!-- 他会在每次数据变动的时候帮我们重新渲染 -->
          <tr ng-repeat="v in students">
              <td>{{v.name}} </td>
              <td>{{v.id}} </td>
              <td>{{v.sex}} </td>
          </tr>
          <tr>
              <td ng-click="addStudent()">+</td>
          </tr>
      </tbody>
    </table>
  </body>
</html>
```

```javascript
  // 把我们的应用作用单独的一个模块 和系统中的其他模块解耦
  var reminder = angular.module('reminder',[]);

  // 在我们的模块上创建一个控制器  来控制本模块中某个局部的可见数据
  reminder.controller('mainControler',['$scope',function($scope){
    $socpe.students = [
      {id:1001,name:'A',sex:'nan'},
      {id:1002,name:'B',sex:'nv'},
      {id:1003,name:'C',sex:'nan'},
    ]
    $scope.addStudent = function(){
      this.stuents.push({id:Math.random(),name:'new man', sex:'nan'});
    }
  }]);
```

##  4.常用的装饰型指令

装饰性指令用来在 view 和 controler 之间协调运作

[angularjs 概念介绍](http://docs.ngnice.com/guide)

[angularjs API](http://docs.ngnice.com/api)


*  ng-app
*  ng-controller

*  ng-repeat  // track by $index  可以避免同id属性报错
*  ng-model
*  ng-init

*  ng-class
*  ng-show
*  ng-hide
*  ng-if
*  ng-switch

*  ng-[event]
*  ng-href
*  ng-src

##  5.组件型指令

`组件型指令` 用来拆分复杂的html页面

实现`组件化开发` 和一定程度的 `复用`

login.html

```html
<div id="login">
  <div class="usernam"></div>
  <div class="password"></div>
  <button class="submit">Login</button>
</div>
```

index.html

```html
<!DOCTYPE html>
<html ng-app="reminder">
  <head>
    <meta charset="utf-8">
    <title></title>
    <script src="angular.js" charset="utf-8"></script>
    <script src="index.js" charset="utf-8"></script>
  </head>
  <body ng-controller = "mainControler">
    <login></login>
  </body>
</html>
```
index.js

```javascript
var reminder = angular.module('reminder',[]);
// 在整个模块的各个控制器作用域内  login指令都可用
reminder.directive('login',[function(){
  // Runs during compile
  return {
    restrict: 'AE', // E = Element, A = Attribute, C = Class, M = Comment
    templateUrl: 'login.html',
    // name: '',
    // priority: 1,
    // terminal: true,
    // scope: {}, // {} = isolate, true = child, false/undefined = no change
    // controller: function($scope, $element, $attrs, $transclude) {},
    // require: 'ngModel', // Array = multiple requires, ? = optional, ^ = check parent elements
    // template: '<h3>Hello Angular</h3>',
    // replace: true,
    // transclude: true,
    // compile: function(tElement, tAttrs, function transclude(function(scope, cloneLinkingFn){ return function linking(scope, elm, attrs){}})),
    // link: function($scope, iElm, iAttrs, controller) {
    // }
  };
}]);
```

## 6.在组件型指令中的link函数中使用jQuery或jqLite

一般推荐在自定义指令的link函数中使用jquery去操作dom元素.

在link函数中操作$scope身上的数据时一定要注意

调用`$scope.$apply()`方法让angular启动脏检查机制来自动刷新页面

调用`$scope.$apply()`方法让angular启动脏检查机制来自动刷新页面

调用`$scope.$apply()`方法让angular启动脏检查机制来自动刷新页面

另外操作文档或者使用定时函数时，需要注入 `$document`, `$timeout` 等服务



angular 内部提供 `angular.elements` 方法,类似于jQuery方法,得到jqLite对象

jqLite对象中的方法:

```json
[
 "ready()",
 "toString()",
 "eq()",
 "length()",
 "push()",
 "sort()",
 "splice()",
 "data()",
 "inheritedData()",
 "scope()",
 "isolateScope()",
 "controller()",
 "injector()",
 "removeAttr()",
 "hasClass()",
 "css()",
 "attr()",
 "prop()",
 "text()",
 "val()",
 "html()",
 "empty()",
 "removeData()",
 "bind()",
 "unbind()",
 "on()",
 "off()",
 "one()",
 "replaceWith()",
 "children()",
 "contents()",
 "append()",
 "prepend()",
 "wrap()",
 "remove()",
 "detach()",
 "after()",
 "addClass()",
 "removeClass()",
 "toggleClass()",
 "parent()",
 "next()",
 "find()",
 "clone()",
 "triggerHandler()"
]
```
如果项目中不使用jQuery插件，jqLite是很好的操作DOM，绑定事件的选择。


在普通的controller中 也可以这样使用：

```html
<button type="button" name="button" ng-click="submit($event)"></button>
```
```javascript
$scope.toggletododetail = function($event){
  console.log($event);
  var el = angular.elements() // 得到一个JqLite对象
  console.dir(el);  //查看其中的方法，比jquery少很多
}
```

如果想使用jquery,先引入jquery 后引入angular.js,jQuery 会自动覆盖jqLite,随后不用任何配置就可以在代码中使用 $.


## 7. ng-view 指令

angular 多页面切换的方式

使用ng-view指令搭配 $routeProvider配置整个应用的 `状态`

```html
<script src="angular-route.js"></script>
<div class="">
   <title-bar></title-bar>  

   <!-- 当应用处于'#/view'这种状态时，ng-view会被替换成对应的配置好的html页面-->
   <!-- 通过ajax请求的方式 或者 从缓存中 或者从页面中获取-->
   <div ng-view></div>

   <tab-bar>
     <ul>
       <li><a href="#/view"></a></li>
       <li><a href="#/"></a></li>
     </ul>
   </tab-bar>
</div>
```

```javascript
var myapp = angular.module('myapp',[]);

myapp.controller('mainctrl',['$scope',function($scope){
  //main.html 的控制器
}]);
myapp.controller('infoctrl',['$scope','$routeParams',function($scope,$routeParams){
  //info.html 的控制器
  console.log($routeParams.id);
}]);

myapp.config(['$routeProvider',function($routeProvider) {
  $routeProvider.when('/',{
    controller:'main',
    templateUrl:'main.html'
  }).when('/view/:id',{
    controller:'infoctrl',
    templateUrl:'info.html',
    publicAccess:true
  }).otherwise({
    redirectTo:'/'
  });
}])
```

通过内置的router了解了其工作原理之后，请在工程中使用 `angular-ui-router`;

切换状态可以使用a链接，也可以在js中切换

使用内置的$location 服务

```javascript
myapp.controller('listCtrl',[
  '$scope',
  '$location',
  function($scope,$location){
    $socpe.whenClick = function(url){
      $location.path(url); //可读可写，参考文档
    }
  }
])
```

## 8. 服务

为什么需要服务?

>  多页面切换的过程中  有些数据被锁死在对应的controller内。
>  需要把这些公共的数据以服务的形式组织起来，随需随取

服务在整个页面的生命周期中可用,我们一般把和后台做数据交互这样的任务，交给service去做，
而不是在controller内。

常用一个service代表后台中一张表，及对表的操作

```javascript

var myapp = angular.module('myapp',[]);

// 可以在中括号中定义其他需要的服务
myapp.factory('$student',[ function(){
  return {
      students:[
        {...},
        {...},
        {...},
      ]
      getStudentsById:function(){
        ...
      },
      removeStudentsById:function(){

      },
      updateStudentsById:function(){

      },
      addStudent:function(id){

      }
  }
}]);

myapp.service('$copyRight',  function(){
  this.name = 'unique';
  this.date  = '2015';
  this.generatorCode = function () {
    return '<span>'+this.name+'</span><img src="erweima">';
  }
});

myapp.constant('$isLogin', {islogin:false});

myapp.value('$PI', Math.PI);

```

## 9.在服务中或其他地方使用$http服务

来看一个典型的服务及其使用

所有在服务中同数据库的交互都采用这种方式

```javascript
myapp.factory('User',[
  '$http',
  '$location',
  '$q',
  function($http,$location,$q){
    var User = {
      getAllUser:function(){
        //这里涉及到异步  所以使用$q延后执行
        var deferred = $q.defer();
        $http.get('/allUser')
        .success(function(data, status, headers, config){
          deferred.resolve(data);
        }).error(function(data, status, headers, config){
          deferred.reject(data);
        })
        return deferred.promise;
      }
    }
    return User;
  }
])
myapp.controller('userCtrl',[
  '$scope',
  'User',
  function($scope,User){
    //因为期间涉及到异步，所以需要使用promise的编程思路来解决拿不到数据的问题
    User.getAllUser().then(function(data){
        $scope.users = data;
    },function(){
        $scope.users = []; //处理错误
    });
  }
])
```


## 10.过滤器

有的时候一些展现在页面上的数据需要格式化,有的时候一些展现在页面上列表需要排序，过滤。

我们使用过滤器,内置过滤器参考api文档,自定义过滤器的方式

过滤器的本质是一个函数

```html
<!--prefix 是一个函数  第一个参数为 name 变量  第二个参数为:后面提供的值-->
<span>{{name|prefix:'@联盟'}}</span>
```

所以自定义过滤器就相当于写一个公用的在整个模块中可用的函数

```javascript
myapp.filter('young',function(){
  return function(e,type){
    var r =  [];
    var _sex = type?'nan':'nv';
    for (var i = 0; i < e.length; i++) {
      if(e[i].age>=12 && e[i].age<=17 && e[i].sex == _sex){
        r.push(e[i]);
      }
    };
    return r;
  }
})
```
```html
  <li ng-repeat="stu in students| young:1" ></li>
```

过滤器可以以类似服务的方式注入到各个 控制器，服务，指令，过滤器。

```javascript
myapp.controller('indexCtrl',[
  '$scope',
  '$routeParams',
  'User',   // User为自定义的一个服务
  '$filter',// 注入$filter prefix为自定义的一个过滤器
  function($scope,$routeParams,User,$filter){
    $filter('prefix')();//这样像使用正常函数一样使用它
  }
])
```

## 11.使用动画

```html
<script src="angular-animate.js"></script>
```
```javascript
var myapp = angular.module('myapp',['ngRoute','ngAnimate']);
```

查阅文档 观察class的变化 写css样式来操控动画

```html
<style>
span.ng-enter{
  /**/
}
span.ng-enter-active{
  /**/
}

#view.ng-enter{

}
#view.ng-enter-active{

}

<style>
<span ng-if="show"> </span>   
<ng-view id="view"></ng-view>
```


## 12.自定义指令中的配置项

* 指令之name属性

  指令的名字，默认和directive第一个参数相同

* 指令之priority属性

  指令的执行优先级，当一个元素身上有两个指令的时候，优先级高的先执行，
  内置指令中，ng-repeat拥有最高优先级

* 指令之terminal属性

  编译器是否在该指令之后继续编译其他指令

* 指令之template属性

  ```html
  <!--注意这里 type 为  text/ng-template 的script标签-->
  <script  type="text/ng-template" id="tab-bar">
  <ul>
    <li></li>
    <li></li>
    <li></li>
  </ul>
  </script>
  var myapp = angular.module('myapp',[]);
  myapp.directive('tab-bar',[
    function(){
      return {
        restrict:"AE",
        template:tab-bar,  //上面那个script标签的id
      }
    }
  ])
  ```
  指定一个字符串或者一个<script type="template/javascript" id="tem"></script>的id
  或者templateCache中的某个名字来作为指令的模板

* 指令之templateUrl属性

  指定一个url地址作为指令的模板

* 指令之scope属性

  声明独立的作用域

  例子.一个轮播图指令,拥有自己独立的作用域,但是需要从父作用域中获取需要轮播的图片地址

  ```html
  <body ng-controller="mainCtrl">
    <lunbo pics="pics" a="{{a}}">
      <h1>this is a lunbo</h1>
    </lunbo>
  </body>
  ```

  ```javascript
  var di = angular.module('di',[]);
  di.controller('mainCtrl',[
  '$scope',
  function($scope){
    $scope.a = 12;
    $scope.b = 13;
    $scope.pics = [
    {title:1},
    {title:2},
    {title:3}
    ]
    $scope.addPic = function(){
      $scope.pics.push({title:4});
    }
  }
  ])

  di.directive('lunbo', [
  function(){
    return {
      restrict:'AE',
      replace:true,
      transclude:true,
      template:'<div> {{b}} <div ng-transclude></div> <ul> <li ng-repeat="v in pics  track by $index"> {{v.title}} </li> </ul> </div>',
      scope:{
        a:'@',
        pics:'=',
        addPic:'&'
        },
        controller:function($scope){
          console.log($scope);
        }
      }
    }
  ]);
  ```

* 指令之controller属性

  生命独立的controller

* 指令之require属性

  设置要注入当前指令链接函数中的其他指令的控制器

* 指令之restrict 属性

  指令在页面中的使用方式

* 指令之replace属性

  指令以元素的方式书写的时候是否替换标签

* 指令之transclude属性

  指令中能不能嵌套包含其他Html元素

* 指令之compile属性

  定义编译函数，编译函数会操作原始DOM，而且会在没有提供link设置的情况下创建链接函数

* 指令之link属性

  在指令编译的最后阶段会调用一次，通常在这里注册事件，操作dom

  如果指令了compile，则link不生效

## 13.利用templateCache来缓存页面

```javascript
//会在app启动的时候运行一次
myapp.run(function($templateCache){
  $templateCache.put('cache','<h3>内容来源于缓存!</h3>');
})
myapp.directive('tsTplcache', [function(){
  // Runs during compile
  return {
    restrict:'EAC',
    templateUrl:'cache',
    replace:true
  };
}]);
```

## 14.其他

*  ng-bind 解决网络不好的情下刷新页面会看到`{{}}`的问题

*  一次绑定问题 `{{:v.name}}`

* $apply  $watch 解决一些监测问题

  $socpe.$wacth()尽量少用

  $scope.$apply()用在link函数中去启动angular脏检查机制，保障数据的同步

  $scope.$apply()用在link函数中去启动angular脏检查机制，保障数据的同步

  $scope.$apply()用在link函数中去启动angular脏检查机制，保障数据的同步

* 其他问题

  使用了过滤器之后  ng-repeat 中的 $index 形同虚设

  需要在数据中使用id来标识一条唯一的数据

## 15.背后的原理

* angular中的mvvm模式

  M(model) V(view) C(controller)

  `Model`代表数据最原始的样子和逻辑以及对数据的操作

  > 在web页面中,大部分model都是来自Ajax服务器返回的数据或者全局配置对象. angular中的Service正是封装和处理这些与Model相关的业务逻辑的最佳方式。

  `View` 是数据最终会呈现的样子

  > 在angular中 普通的html结构 和 组件型指令就是 view

  `Controller`负责model对象的初始化.

  > 在angular中 controller 将调用一个或多个Service来获取模型数据。 并把他放在$scope上,controller也负责提供那些写在view上的装饰性指令所你调用的函数等。

  在angular中因为`Controller`和 `View` 之间通过 $scope 的数据双向绑定关系。一般angular团队不把自己称为一个`MVC`框架，而是 MVVM (model-view-view-model)

* 作用域就像javascript的函数作用域，是层层嵌套的

* $scope.$apply 可以启动脏检查机制，会在内部调用$digest去查看哪些变量发生了变化，以决定是更新$scope能还是更新页面显示。大部分情况下我们不需要手动调用它是因为在angular的各个服务，控制器中都自动对他进行了调用。如果用原生的方式写个setTimeOut去改变$scope身上的某个变量，就会看到view并不会更新，这时候就需要手动调用$apply.在link函数中也是如此。
