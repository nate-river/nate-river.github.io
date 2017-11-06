---
layout: post
title:  css3例子
tags:
categories: git
---




<dl id="content">
</dl>

<script>
var data = {
            "边框和背景":{
              "半透明边框": "012289cc14106a1bd7a5",
              "多重边框": "525eb8e9cdade71723c1",
              "背景定位1": "0f226e63595d1bef88cb",
              "背景定位2": "0f19ac5d28d0aa7b6c60",
              "背景定位3": "b5fcb42d055427ab6c1a",
              "边框内圆角": "170fe436f290083cc24c",
              "水平条纹": "119dbf7f0c76dba7b7ee",
              "垂直条纹": "1b4983062fd2b4d7e60e",
              "对角条纹": "abeab80934fc26e6538e",
              "对角条纹60度": "5646121210b0c99c94a7",
              "复杂条纹": "aa50d296a8ec07cf7334",
              "蓝网格图": "43bde2086e9d549fb844",
              "圆点图": "cd33da5d1a48046746cd",
              "棋盘图": "4f7ca0749582b1bd7527",
              "棋盘图-svg": "5d3cacead6f134da842e",
              "旋转动画": "ea53f3bee9a7f1439aa7",
              "随机条纹": "4b4ad05f4c1b5259066f",
              "边框图片": "c73fd4ea4b592a05c004",
              "连续的边框图片": "55b5f131c45702a55684",
              "古老的信封背景实现": "e3cfcb094e65d85df847",
              "古老的信封边框实现": "0f6900d370f55ec9c975",
              "行进的蚂蚁": "f26dddc71730c3847153",
              "页脚": "9483cc7012049f2c808e",
            },


            "形状":{
              "椭圆": "aada0b96b21ae3e45c1b",
              "半椭圆": "e98d11da331bd9482bb0",
              "4分之一椭圆": "2b75df0e72c9804e8abe",
              "平行四边形": "e1f72639c34a5578dda3",
              "利用伪元素的平行四边形": "f2d98791ab1f0b238aa9",
              "钻石图片": "7563400",
              "钻石图片效果": "c62456fed36a524b8273",
              "四角直切图片": "2937c990d6bfad274740",
              "四角圆切图片": "24484257bc6cf7076a8e",
              "使用边框的切角": "365c867441f3ee298212",
              "平行四边形选项卡": "1345dc9399dc8e794502",
              "圆饼动画": "722909b9808c14eb7300",
              "静止饼图": "66e1e52ac2a44ad87aa4",
              "五彩流动": "e324a92d31b7f67da5c0",
              "svg饼动画": "4696e4c6700fe9f346d8",
           	},

           	"视觉效果":{
              "一侧阴影": "cc055dadf493c15723cf",
              "双侧阴影": "d29d19ab66177b18bd64",
              "反向阴影": "a23e445fca36293d12f6",
              "投影滤镜": "d8a2376c79906d68f3d1",
              "图片滤镜": "b338c9940a31b727b7a9",
              "变色的老虎": "0dced2852818c0f555e9",
              "透明背景文字": "d9f243ddd7dbffa341a4",
              "卷脚": "83b4d6bc907aa5ab576a",
              "卷脚2": "bc32dc20adea2261c731",
           	},

           	"字体处理":{
              "文本均分": "e370ba333ae95116e212",
              "断行": "7eb242f4e8f078cadbca",
              "隔行色": "cf30f5d442533b32600d",
              "代码tab数量": "88c1523dfd1284950b4d",
              "个性下划线": "58f3d67d5bb0f8338776",
              "更个性的下划线": "c9184f634e9e9efde6e8",
              "文本阴影": "80eafefae35d26979972",
              "空心文字": "7a665ce85190f9cb201e",
              "发光文字": "4af6d5c3b22395543cb8",
              "3d文字": "ba8161d038b9c13b99ac",
              "圆环文字": "bda1bf6b0c4adbcea63d",
            },

            "用户体验":{
              "禁止的按钮": "41c8da81742e1ab1d07f",
              "扩大点击区域": "df5686d4047307991f73",
              "扩大点击区域": "d76ac0acc80923d47106",
              "复选框": "e269f10328615254e29e",
              "点击切换样式的按钮": "fa5c622180b232043891",
              "方便的遮罩": "91538b2131d3545035ca",
              "模糊遮罩": "1326eb460b0dff91d638",
              "滑动到底部顶部的提示": "20205b5fcdd834461e80",
              "可拖动的图片遮罩": "b7e7fef7dcf9a7161a51",
            },

             "动画效果":{
              "弹球": "1b37089310d0a5a2d8e6",
              "android风": "6cf33228089efef8a5ac",
              "android动画": "73294faf1e2bc5ff0078",
              "帧动画": "bcc082518391f45b41dc",
              "闪烁": "46fe09e5f2b97d6f282d",
              "打字效果": "b04ab9f41084b0a66960",
              "静态播放动画": "b7b53efcc2f933ca6d54",
              "转动动画": "87d80a51a5294ec07aea",
              "转动动画2": "6c647a5599dc11145f2c"
             },

            "弹性布局":{
              "intrinsic-sizing": "82eb1575806f6eff9c37",
              "styling-sibling-count": "70c434a6e802b062f494",
              "fluid-fixed": "763229b68fa27c5c1bfa",
              "vertical-centering-text": "00b5cd0de91a439616e8",
              "vertical-centering": "8aa9aa04ee57f479c513",
              "vertical-centering-vh": "bf12b39d8f5da2b6e5b6",
              "vertical-centering-abs": "cd12fac0e18bb27fb62d",
              "sticky-footer-fixed": "b10c3eb3b7078711a588",
              "sticky-footer": "410e43c60863a8dba193",
             },
           };
var content = document.querySelector('#content');
var htmlStr = '';
for(var cate in data){
  htmlStr += '<h2>'+cate+'</h2>';
  for( var name in data[cate] ){
    htmlStr += '<dd><a href="http://dabblet.com/gist/'+data[cate][name]+'">'+name+'</a></dd>';
  }
}
content.innerHTML = htmlStr;
</script>
