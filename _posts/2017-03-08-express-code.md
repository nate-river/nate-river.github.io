---
layout: post
title:  "express web开发常用代码"
tags:
categories:
---

## 处理普通post请求


```javascript
const bodyParser = require('body-parser');

// parse application/x-www-form-urlencoded
app.use(bodyParser.urlencoded({extended: false}));

// parse application/json
app.use(bodyParser.json());

app.post('/',(req,res)=>{
  console.log(req.body);
})
```

## 处理session

```javascript
const session = require('express-session');

app.use(session({
  secret: 'keyboard cat',
  resave: false,
  saveUninitialized: true
}));

app.get('/logincheck',(req,res)=>{
  req.session.login = true;
})

// 中间件
app.use('/admin',(req,res,next)=>{
  if(req.seesion.login){
    next();
  }else{
    res.redirct('/login');
  }
})
```

## 上传文件

```javascript


const os = require('os');
const fs = require('fs');
const multer = require('multer');    // multipart/form-data
const upload = multer({dest: os.tmpdir()});

app.post('/upload', upload.single('f'), function (req, res) {
   console.log( req.body )
   let f = req.file;
    fs.rename(
      f.path,
      './public/upload/' + f.filename + path.extname(f.originalname),
      ()=> {
        res.end('ok');
      }
    );
});
```

## 创建md5

```javascript
const crypto = require('crypto');
const hash = crypto.createHash('md5');
hash.update('123456');
console.log(hash.digest('hex'));
```


## 防止意外退出

```javascript
process.on('uncaughtException', (ex)=> {
  console.log('error');
});
```

## 使用fetch

```javascript
// npm install whatwg-fetch --save

// fetch上传文件
var input = document.querySelector('input[type="file"]')

var data = new FormData()
data.append('file', input.files[0])
data.append('user', 'hubot')

fetch('/avatars', {
  credentials: "same-origin",
  method: 'POST',
  body: data
})

// fetch提交表单
var form = document.querySelector('form')

fetch('/users', {
  credentials: "same-origin",
  method: 'POST',
  body: new FormData(form)
})

// fetch 收取cookie
fetch('/users', {
  credentials: "same-origin",
})
```

## react富文本编辑器组件

```html
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <link rel="stylesheet" href="/css/wangEditor.min.css">
</head>
<body>
<div id="page"></div>
<script src="js/jquery-2.2.1.js"></script>
<script src="js/wangEditor.js"></script>
<script src="/js/admin.js"></script>
</body>
</html>
```

```javascript
const React = require('react');
const ReactDOM = require('react-dom');
class Editor extends React.Component {
  constructor(props) {
    super(props);
    this.getContents = this.getContents.bind(this);
  }

  componentDidMount() {
    this.editor = new window.wangEditor(this.el);
    this.editor.config.uploadImgUrl = '/upload';
    this.editor.create();
    // 初始化内容
    this.editor.$txt.html('<div>this is a a</div>');
  }

  getContents() {
    console.log(this.editor.$txt.html());
  }

  render() {
    return (
      <div>
        <div contentEditable="true" style={{height:300}} ref={(el)=>{this.el = el}}></div>
        <div onClick={this.getContents}>获取内容</div>
      </div>
    );
  }
}
ReactDOM.render(<Editor/>, document.querySelector('#page'));
```
