---
layout: post
title:  "fecshop API"
tags: "ui"
categories: "ask"
---

# 1. /cms/home/index
`获取首页信息`
#### 请求方法
`GET`
#### 请求参数
```json
null
```
#### 返回数据格式
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "productList": [
      {
        "one": {
          "name": "对时尚按钮点缀空心网状针织靴子妇女的袖口",
          "sku": "sk2001-blue-zo",
          "_id": "",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160722142719_52348.jpg",
          "price": {
            "symbol": "€",
            "value": "248.59",
            "code": "EUR"
          },
          "special_price": {
            "symbol": "€",
            "value": "133.52",
            "code": "EUR"
          },
          "url": "/catalog/product/57c3aaa9f656f24f353bf56e",
          "product_id": "57c3aaa9f656f24f353bf56e"
        },
        "two": {
          "name": "时髦的镶边criss十字形的妇女的礼服",
          "sku": "sk0008",
          "_id": "",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160810112221_81491.jpg",
          "price": {
            "symbol": "€",
            "value": "30.69",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57c7da1ef656f20c713bf56e",
          "product_id": "57c7da1ef656f20c713bf56e"
        }
      },
      {
        "one": {
          "name": "时尚之字形条纹和火焰无袖连衣裙的妇女",
          "sku": "sk0004",
          "_id": "",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160707145718_97803.jpg",
          "price": {
            "symbol": "€",
            "value": "20.46",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57c7da4af656f273013bf56e",
          "product_id": "57c7da4af656f273013bf56e"
        },
        "two": {
          "name": "甜点圆点妇女的夏天礼服",
          "sku": "sk0003",
          "_id": "",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160804090311_12690.jpg",
          "price": {
            "symbol": "€",
            "value": "30.69",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57c7da9af656f2577a3bf56e",
          "product_id": "57c7da9af656f2577a3bf56e"
        }
      },
      {
        "one": {
          "name": "意大利面条打印背面Bodycon衣服",
          "sku": "sk0002",
          "_id": "",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160606112453_71094147323202778861.JPG",
          "price": {
            "symbol": "€",
            "value": "30.69",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57c7daecf656f273013bf570",
          "product_id": "57c7daecf656f273013bf570"
        },
        "two": {
          "name": "袖子信件印刷船员颈部运动衫kahaki xl",
          "sku": "p10001-kahaki-xl",
          "_id": "",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160905101021_28071.jpg",
          "price": {
            "symbol": "€",
            "value": "5.58",
            "code": "EUR"
          },
          "special_price": {
            "symbol": "€",
            "value": "4.66",
            "code": "EUR"
          },
          "url": "/catalog/product/580835d0f656f240742f0b7c",
          "product_id": "580835d0f656f240742f0b7c"
        }
      },
      {
        "one": {
          "name": "圆领女士花卉印花无袖连衣裙",
          "sku": "432432",
          "_id": "",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/1/7/17147202419675158.jpg",
          "price": {
            "symbol": "€",
            "value": "20.46",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57bac5c6f656f2940a3bf570",
          "product_id": "57bac5c6f656f2940a3bf570"
        },
        "two": {
          "name": "贝尔袖脱下肩带花边拼接女衬衫",
          "sku": "32332",
          "_id": "",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/1/14/11471858072718.jpg",
          "price": {
            "symbol": "€",
            "value": "20.46",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57bac59ef656f24f123bf56e",
          "product_id": "57bac59ef656f24f123bf56e"
        }
      }
    ],
    "advertiseImg": {
      "bigImgList": [
        {
          "imgUrl": "//img.apphtml5.fancyecommerce.com/custom/home_img_1.jpg"
        },
        {
          "imgUrl": "//img.apphtml5.fancyecommerce.com/custom/home_img_2.jpg"
        },
        {
          "imgUrl": "//img.apphtml5.fancyecommerce.com/custom/home_img_3.jpg"
        }
      ],
      "smallImgList": [
        {
          "imgUrl": "//img.apphtml5.fancyecommerce.com/custom/home_small_1.jpg"
        },
        {
          "imgUrl": "//img.apphtml5.fancyecommerce.com/custom/home_small_2.jpg"
        }
      ]
    },
    "language": {
      "langList": [
        {
          "code": "fr",
          "language": "fr_FR",
          "languageName": "Français"
        },
        {
          "code": "en",
          "language": "en_US",
          "languageName": "English"
        },
        {
          "code": "es",
          "language": "es_ES",
          "languageName": "Español"
        },
        {
          "code": "zh",
          "language": "zh_CN",
          "languageName": "中文"
        }
      ],
      "currentLang": "zh"
    },
    "currency": {
      "currencyList": {
        "EUR": {
          "code": "EUR",
          "rate": 0.93,
          "symbol": "€"
        },
        "USD": {
          "code": "USD",
          "rate": 1,
          "symbol": "$"
        },
        "GBP": {
          "code": "GBP",
          "rate": 0.8,
          "symbol": "£"
        },
        "CNY": {
          "code": "CNY",
          "rate": 6.3,
          "symbol": "￥"
        }
      },
      "currentCurrency": "EUR"
    }
  }
}
```
# 2. /general/base/menu
`获取所有产品分类`
#### 请求方法
`GET`
#### 请求参数
```json
null
```
#### 返回数据格式
```json
{
  "home": {
    "_id": "home",
    "level": 1,
    "name": "首页",
    "url": "/"
  },
  "57b6abfff656f246653bf570": {
    "_id": "57b6abfff656f246653bf570",
    "level": 1,
    "name": "婚礼",
    "url": "/catalog/category/57b6abfff656f246653bf570",
    "child": {
      "57bea0d3f656f2ec1f3bf56e": {
        "_id": "57bea0d3f656f2ec1f3bf56e",
        "level": 2,
        "name": "婚礼礼服",
        "url": "/catalog/category/57bea0d3f656f2ec1f3bf56e",
        "child": {
          "57bea0e3f656f275313bf56e": {
            "_id": "57bea0e3f656f275313bf56e",
            "level": 3,
            "name": "婚礼礼服2016",
            "url": "/catalog/category/57bea0e3f656f275313bf56e"
          },
          "57bea101f656f2ec1f3bf570": {
            "_id": "57bea101f656f2ec1f3bf570",
            "level": 3,
            "name": "婚礼礼服",
            "url": "/catalog/category/57bea101f656f2ec1f3bf570"
          },
          "57bea10af656f275313bf570": {
            "_id": "57bea10af656f275313bf570",
            "level": 3,
            "name": "产妇婚礼礼服",
            "url": "/catalog/category/57bea10af656f275313bf570"
          },
          "57bea113f656f24e623bf56e": {
            "_id": "57bea113f656f24e623bf56e",
            "level": 3,
            "name": "穆斯林婚礼礼服",
            "url": "/catalog/category/57bea113f656f24e623bf56e"
          },
          "57bea11bf656f2ec1f3bf572": {
            "_id": "57bea11bf656f2ec1f3bf572",
            "level": 3,
            "name": "A线婚纱",
            "url": "/catalog/category/57bea11bf656f2ec1f3bf572"
          },
          "57bea125f656f275313bf572": {
            "_id": "57bea125f656f275313bf572",
            "level": 3,
            "name": "球礼服婚礼礼服",
            "url": "/catalog/category/57bea125f656f275313bf572"
          },
          "57bea157f656f275313bf576": {
            "_id": "57bea157f656f275313bf576",
            "level": 3,
            "name": "小姐伴娘礼服",
            "url": "/catalog/category/57bea157f656f275313bf576"
          }
        }
      },
      "57bea132f656f24e623bf570": {
        "_id": "57bea132f656f24e623bf570",
        "level": 2,
        "name": "伴娘礼服",
        "url": "/catalog/category/57bea132f656f24e623bf570",
        "child": {
          "57bea13bf656f2ec1f3bf574": {
            "_id": "57bea13bf656f2ec1f3bf574",
            "level": 3,
            "name": "伴娘礼服2016",
            "url": "/catalog/category/57bea13bf656f2ec1f3bf574"
          },
          "57bea145f656f275313bf574": {
            "_id": "57bea145f656f275313bf574",
            "level": 3,
            "name": "伴娘礼服2015",
            "url": "/catalog/category/57bea145f656f275313bf574"
          },
          "57bea14ef656f2ec1f3bf576": {
            "_id": "57bea14ef656f2ec1f3bf576",
            "level": 3,
            "name": "伴娘礼服2014",
            "url": "/catalog/category/57bea14ef656f2ec1f3bf576"
          },
          "57bea160f656f24e623bf572": {
            "_id": "57bea160f656f24e623bf572",
            "level": 3,
            "name": "优雅伴娘礼服",
            "url": "/catalog/category/57bea160f656f24e623bf572"
          },
          "57bea170f656f2ec1f3bf578": {
            "_id": "57bea170f656f2ec1f3bf578",
            "level": 3,
            "name": "廉价伴娘礼服",
            "url": "/catalog/category/57bea170f656f2ec1f3bf578"
          }
        }
      },
      "57bea18ef656f2ec1f3bf57a": {
        "_id": "57bea18ef656f2ec1f3bf57a",
        "level": 2,
        "name": "花女孩礼服",
        "url": "/catalog/category/57bea18ef656f2ec1f3bf57a",
        "child": {
          "57bea196f656f24e623bf574": {
            "_id": "57bea196f656f24e623bf574",
            "level": 3,
            "name": "女孩聚会礼服",
            "url": "/catalog/category/57bea196f656f24e623bf574"
          },
          "57bea1a0f656f275313bf578": {
            "_id": "57bea1a0f656f275313bf578",
            "level": 3,
            "name": "首次圣餐礼服",
            "url": "/catalog/category/57bea1a0f656f275313bf578"
          }
        }
      }
    }
  },
  "57b6ac19f656f246653bf572": {
    "_id": "57b6ac19f656f246653bf572",
    "level": 1,
    "name": "特殊场合",
    "url": "/catalog/category/57b6ac19f656f246653bf572",
    "child": {
      "57b6afc6f656f22b783bf579": {
        "_id": "57b6afc6f656f22b783bf579",
        "level": 2,
        "name": "家庭礼服",
        "url": "/catalog/category/57b6afc6f656f22b783bf579"
      },
      "57b6afd1f656f25a523bf577": {
        "_id": "57b6afd1f656f25a523bf577",
        "level": 2,
        "name": "球形礼服",
        "url": "/catalog/category/57b6afd1f656f25a523bf577"
      },
      "57b6afe0f656f25a523bf579": {
        "_id": "57b6afe0f656f25a523bf579",
        "level": 2,
        "name": "正式礼服",
        "url": "/catalog/category/57b6afe0f656f25a523bf579"
      },
      "57b6afecf656f25a523bf57b": {
        "_id": "57b6afecf656f25a523bf57b",
        "level": 2,
        "name": "设计师礼服",
        "url": "/catalog/category/57b6afecf656f25a523bf57b"
      },
      "57b6affff656f25a523bf57d": {
        "_id": "57b6affff656f25a523bf57d",
        "level": 2,
        "name": "快速交货的礼服",
        "url": "/catalog/category/57b6affff656f25a523bf57d"
      }
    }
  },
  "57b6ac42f656f246653bf576": {
    "_id": "57b6ac42f656f246653bf576",
    "level": 1,
    "name": "男人",
    "url": "/catalog/category/57b6ac42f656f246653bf576",
    "child": {
      "57beb692f656f24e623bf578": {
        "_id": "57beb692f656f24e623bf578",
        "level": 2,
        "name": "衬衫",
        "url": "/catalog/category/57beb692f656f24e623bf578"
      },
      "57beb6a0f656f275313bf580": {
        "_id": "57beb6a0f656f275313bf580",
        "level": 2,
        "name": "短裤",
        "url": "/catalog/category/57beb6a0f656f275313bf580"
      }
    }
  },
  "57b6ac5bf656f246653bf57a": {
    "_id": "57b6ac5bf656f246653bf57a",
    "level": 1,
    "name": "箱包配件",
    "url": "/catalog/category/57b6ac5bf656f246653bf57a"
  },
  "57b6ac69f656f246653bf57c": {
    "_id": "57b6ac69f656f246653bf57c",
    "level": 1,
    "name": "珠宝和手表",
    "url": "/catalog/category/57b6ac69f656f246653bf57c"
  },
  "57beb586f656f275313bf57a": {
    "_id": "57beb586f656f275313bf57a",
    "level": 1,
    "name": "电脑",
    "url": "/catalog/category/57beb586f656f275313bf57a"
  },
  "5a1b673ebfb7ae44c26734f2": {
    "_id": "5a1b673ebfb7ae44c26734f2",
    "level": 1,
    "name": "测试类",
    "url": "/catalog/category/5a1b673ebfb7ae44c26734f2"
  }
}
```
# 3. /catalog/category/index
`获取某个分类下的符合条件的所有产品`
#### 请求方法
`GET`
#### 请求参数
```json
{
"categoryId": "",// 分类id
"sortColumn": "",// 排序规则
"filterAttrs": {},// 筛选条件
"filterPrice": ""// 价格区间
}
```
#### 返回数据格式
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "name": "婚礼礼服2016",
    "name_default_lang": "Wedding Dresses 2016",
    "title": null,
    "image": "//img.fancyecommerce.com/media/catalog/category/X/lP/XlP032_BACKPACK_2016-08-11_955x200_2857.jpg",
    "products": [
      {
        "one": {
          "name": "肩带长袖高低日礼服",
          "sku": "kilw0001",
          "_id": "57bab0d5f656f2940a3bf56e",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/1/22/12229472_1.jpg",
          "price": {
            "symbol": "€",
            "value": "332.94",
            "code": "EUR"
          },
          "special_price": {
            "symbol": "€",
            "value": "115.32",
            "code": "EUR"
          },
          "url": "/catalog/product/57bab0d5f656f2940a3bf56e",
          "product_id": "kilw"
        },
        "two": {
          "name": "迷你长袖开衩",
          "sku": "sk1000-khak",
          "_id": "57cfc212f656f28b5adf9deb",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160715121751_13739.jpg",
          "price": {
            "symbol": "€",
            "value": "41.45",
            "code": "EUR"
          },
          "special_price": {
            "symbol": "€",
            "value": "37.73",
            "code": "EUR"
          },
          "url": "/catalog/product/57cfc212f656f28b5adf9deb",
          "product_id": "sk1000"
        }
      },
      {
        "one": {
          "name": "正式的晚礼服护套",
          "sku": "po0001",
          "_id": "57e8d9a7f656f2e16b6234e5",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/r/nu/rnunew1467608090223.jpg",
          "price": {
            "symbol": "€",
            "value": "113.46",
            "code": "EUR"
          },
          "special_price": {
            "symbol": "€",
            "value": "112.53",
            "code": "EUR"
          },
          "url": "/catalog/product/57e8d9a7f656f2e16b6234e5",
          "product_id": "po0001"
        },
        "two": {
          "name": "圆领女士花卉印花无袖连衣裙",
          "sku": "432432",
          "_id": "57bac5c6f656f2940a3bf570",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/1/7/17147202419675158.jpg",
          "price": {
            "symbol": "€",
            "value": "20.46",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57bac5c6f656f2940a3bf570",
          "product_id": "432432"
        }
      },
      {
        "one": {
          "name": "驯鹿样式闪烁圣诞节礼服",
          "sku": "22221",
          "_id": "581ae91ff656f20f052f0b77",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20161101155240_26690.jpg",
          "price": {
            "symbol": "€",
            "value": "21.10",
            "code": "EUR"
          },
          "special_price": {
            "symbol": "€",
            "value": "20.17",
            "code": "EUR"
          },
          "url": "/catalog/product/581ae91ff656f20f052f0b77",
          "product_id": "22221"
        },
        "two": {
          "name": "优雅圆领无袖印花提花连衣裙",
          "sku": "sk10004-001",
          "_id": "57d61233f656f2b57ddf9ded",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160418182628_30828.jpg",
          "price": {
            "symbol": "€",
            "value": "40.92",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57d61233f656f2b57ddf9ded",
          "product_id": "sk10004"
        }
      }
    ],
    "query_item": {
      "frontNumPerPage": [],
      "frontSort": [
        {
          "label": "销量",
          "value": "hot",
          "selected": false
        },
        {
          "label": "评论",
          "value": "review_count",
          "selected": false
        },
        {
          "label": "收藏",
          "value": "favorite_count",
          "selected": false
        },
        {
          "label": "上架时间",
          "value": "new",
          "selected": false
        },
        {
          "label": "Stock",
          "value": "stock",
          "selected": false
        },
        {
          "label": "￥ 价格由低到高",
          "value": "low-to-high",
          "selected": false
        },
        {
          "label": "￥ 价格由高到低",
          "value": "high-to-low",
          "selected": false
        }
      ]
    },
    "refine_by_info": [],
    "filter_info": {
      "color": {
        "label": "颜色",
        "items": [
          {
            "_id": "blue",
            "count": 1,
            "selected": false,
            "label": "蓝色"
          },
          {
            "_id": "khaki",
            "count": 1,
            "selected": false,
            "label": "黄褐色"
          },
          {
            "_id": "red",
            "count": 2,
            "selected": false,
            "label": "红色"
          },
          {
            "_id": "black",
            "count": 1,
            "selected": false,
            "label": "黑色"
          },
          {
            "_id": "ivory",
            "count": 1,
            "selected": false,
            "label": "象牙色"
          },
          {
            "_id": "multicolor",
            "count": 2,
            "selected": false,
            "label": "彩色"
          },
          {
            "_id": "green",
            "count": 1,
            "selected": false,
            "label": "绿色"
          },
          {
            "_id": "white & black",
            "count": 2,
            "selected": false,
            "label": "白 & 黑"
          },
          {
            "_id": "",
            "count": 3,
            "selected": false,
            "label": ""
          },
          {
            "_id": "white",
            "count": 3,
            "selected": false,
            "label": "白色"
          }
        ]
      },
      "size": {
        "label": "尺码",
        "items": [
          {
            "_id": "XL",
            "count": 1,
            "selected": false,
            "label": "XL"
          },
          {
            "_id": "L",
            "count": 4,
            "selected": false,
            "label": "L"
          },
          {
            "_id": "",
            "count": 7,
            "selected": false,
            "label": ""
          },
          {
            "_id": "S",
            "count": 1,
            "selected": false,
            "label": "S"
          },
          {
            "_id": "M",
            "count": 4,
            "selected": false,
            "label": "M"
          }
        ]
      },
      "style": {
        "label": "风格",
        "items": [
          {
            "_id": "Vintage ",
            "count": 4,
            "selected": false,
            "label": "Vintage "
          },
          {
            "_id": "Bohemian",
            "count": 1,
            "selected": false,
            "label": "Bohemian"
          },
          {
            "_id": "Cute",
            "count": 8,
            "selected": false,
            "label": "Cute"
          },
          {
            "_id": "Sexy & Club",
            "count": 3,
            "selected": false,
            "label": "性感＆俱乐部"
          },
          {
            "_id": "Work",
            "count": 1,
            "selected": false,
            "label": "Work"
          }
        ]
      },
      "dresses-length": {
        "label": "dresses Length",
        "items": [
          {
            "_id": "Floor-Length ",
            "count": 3,
            "selected": false,
            "label": "Floor-Length "
          },
          {
            "_id": "Knee-Length",
            "count": 9,
            "selected": false,
            "label": "Knee-Length"
          },
          {
            "_id": "Mini",
            "count": 2,
            "selected": false,
            "label": "Mini"
          },
          {
            "_id": "Mid-Calf",
            "count": 3,
            "selected": false,
            "label": "Mid-Calf"
          }
        ]
      },
      "pattern-type": {
        "label": "pattern Type",
        "items": [
          {
            "_id": "Animal",
            "count": 2,
            "selected": false,
            "label": "Animal"
          },
          {
            "_id": "Floral",
            "count": 1,
            "selected": false,
            "label": "Floral"
          },
          {
            "_id": "Leopard ",
            "count": 3,
            "selected": false,
            "label": "Leopard "
          },
          {
            "_id": "Patchwork",
            "count": 2,
            "selected": false,
            "label": "Patchwork"
          },
          {
            "_id": "Character",
            "count": 3,
            "selected": false,
            "label": "Character"
          },
          {
            "_id": "Geometric ",
            "count": 5,
            "selected": false,
            "label": "Geometric "
          },
          {
            "_id": "Paisley",
            "count": 1,
            "selected": false,
            "label": "Paisley"
          }
        ]
      },
      "sleeve-length": {
        "label": "sleeve Length",
        "items": [
          {
            "_id": "Short-Sleeves",
            "count": 4,
            "selected": false,
            "label": "Short-Sleeves"
          },
          {
            "_id": "Sleeveless",
            "count": 13,
            "selected": false,
            "label": "Sleeveless"
          }
        ]
      },
      "collar": {
        "label": "collar",
        "items": [
          {
            "_id": "V-Neck",
            "count": 3,
            "selected": false,
            "label": "V-Neck"
          },
          {
            "_id": "",
            "count": 2,
            "selected": false,
            "label": ""
          },
          {
            "_id": "Hooded",
            "count": 2,
            "selected": false,
            "label": "Hooded"
          },
          {
            "_id": "Round Neck",
            "count": 10,
            "selected": false,
            "label": "Round Neck"
          }
        ]
      }
    },
    "filter_price": {
      "price": [
        {
          "selected": false,
          "label": "---€10",
          "val": "0-10"
        },
        {
          "selected": false,
          "label": "€10---€20",
          "val": "10-20"
        },
        {
          "selected": false,
          "label": "€20---€30",
          "val": "20-30"
        },
        {
          "selected": false,
          "label": "€30---€50",
          "val": "30-50"
        },
        {
          "selected": false,
          "label": "€50---€100",
          "val": "50-100"
        },
        {
          "selected": false,
          "label": "€100---€150",
          "val": "100-150"
        },
        {
          "selected": false,
          "label": "€150---€300",
          "val": "150-300"
        },
        {
          "selected": false,
          "label": "€300---€500",
          "val": "300-500"
        },
        {
          "selected": false,
          "label": "€500---€1000",
          "val": "500-1000"
        },
        {
          "selected": false,
          "label": "€1000---",
          "val": "1000-"
        }
      ]
    },
    "filter_category": {
      "57bea0d3f656f2ec1f3bf56e": {
        "name": "婚礼礼服",
        "url_key": "/wedding-dresses",
        "parent_id": "57b6abfff656f246653bf570",
        "child": {
          "57bea0e3f656f275313bf56e": {
            "name": "婚礼礼服2016",
            "url_key": "/wedding-dresses-2016",
            "parent_id": "57bea0d3f656f2ec1f3bf56e",
            "current": true,
            "url": "catalog/category/57bea0e3f656f275313bf56e"
          },
          "57bea10af656f275313bf570": {
            "name": "产妇婚礼礼服",
            "url_key": "/maternity-wedding-dresses",
            "parent_id": "57bea0d3f656f2ec1f3bf56e",
            "current": false,
            "url": "catalog/category/57bea10af656f275313bf570"
          },
          "57bea113f656f24e623bf56e": {
            "name": "穆斯林婚礼礼服",
            "url_key": "/muslim-wedding-dresses",
            "parent_id": "57bea0d3f656f2ec1f3bf56e",
            "current": false,
            "url": "catalog/category/57bea113f656f24e623bf56e"
          },
          "57bea11bf656f2ec1f3bf572": {
            "name": "A线婚纱",
            "url_key": "/a-line-wedding-dresses",
            "parent_id": "57bea0d3f656f2ec1f3bf56e",
            "current": false,
            "url": "catalog/category/57bea11bf656f2ec1f3bf572"
          },
          "57bea125f656f275313bf572": {
            "name": "球礼服婚礼礼服",
            "url_key": "/ball-gown-wedding-dresses",
            "parent_id": "57bea0d3f656f2ec1f3bf56e",
            "current": false,
            "url": "catalog/category/57bea125f656f275313bf572"
          },
          "57bea157f656f275313bf576": {
            "name": "小姐伴娘礼服",
            "url_key": "/junior-bridesmaid-dresses",
            "parent_id": "57bea0d3f656f2ec1f3bf56e",
            "current": false,
            "url": "catalog/category/57bea157f656f275313bf576"
          }
        },
        "current": false,
        "url": "catalog/category/57bea0d3f656f2ec1f3bf56e"
      },
      "57bea132f656f24e623bf570": {
        "name": "伴娘礼服",
        "url_key": "/-bridesmaid-dresses",
        "parent_id": "57b6abfff656f246653bf570",
        "current": false,
        "url": "catalog/category/57bea132f656f24e623bf570"
      },
      "57bea18ef656f2ec1f3bf57a": {
        "name": "花女孩礼服",
        "url_key": "/-flower-girl-dresses",
        "parent_id": "57b6abfff656f246653bf570",
        "current": false,
        "url": "catalog/category/57bea18ef656f2ec1f3bf57a"
      }
    },
    "page_count": 3
  }
}
```
# 4. /catalog/category/product
`获取某个分类下的符合条件的某一页的产品（分页）`
#### 请求方法
`GET`
#### 请求参数
```json
{
"categoryId": "",// 分类id
"p":"", // 第几页
"sortColumn": "",// 排序规则
"filterAttrs": {},// 筛选条件
"filterPrice": ""// 价格区间
}
```
#### 返回数据格式
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "products": [
      {
        "one": {
          "name": "花卉样式被隐瞒的拉链高腰礼服",
          "sku": "sk10003-001",
          "_id": "57d611b4f656f20070df9deb",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160617104826_51885.jpg",
          "price": {
            "symbol": "€",
            "value": "19.53",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57d611b4f656f20070df9deb",
          "product_id": "sk10003"
        },
        "two": {
          "name": "甜点圆点妇女的夏天礼服",
          "sku": "sk0003",
          "_id": "57c7da9af656f2577a3bf56e",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160804090311_12690.jpg",
          "price": {
            "symbol": "€",
            "value": "30.69",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57c7da9af656f2577a3bf56e",
          "product_id": "sk0003"
        }
      },
      {
        "one": {
          "name": "驯鹿样式闪烁圣诞节礼服",
          "sku": "222212",
          "_id": "581c6833f656f2042f2f0b77",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20161024170457_10036.jpg",
          "price": {
            "symbol": "€",
            "value": "21.39",
            "code": "EUR"
          },
          "special_price": {
            "symbol": "€",
            "value": "17.67",
            "code": "EUR"
          },
          "url": "/catalog/product/581c6833f656f2042f2f0b77",
          "product_id": "222212"
        },
        "two": {
          "name": "叶子样式腰部被拉练的礼服",
          "sku": "sk10002",
          "_id": "57d60c6cf656f2b57ddf9deb",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160723113745_77121.jpg",
          "price": {
            "symbol": "€",
            "value": "30.69",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57d60c6cf656f2b57ddf9deb",
          "product_id": "sk10002"
        }
      },
      {
        "one": {
          "name": "对时尚按钮点缀空心网状针织靴子妇女的袖口",
          "sku": "sk2001-blue-zo",
          "_id": "57c3aaa9f656f24f353bf56e",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160722142719_52348.jpg",
          "price": {
            "symbol": "€",
            "value": "248.59",
            "code": "EUR"
          },
          "special_price": {
            "symbol": "€",
            "value": "133.52",
            "code": "EUR"
          },
          "url": "/catalog/product/57c3aaa9f656f24f353bf56e",
          "product_id": "sk2001"
        },
        "two": {
          "name": "时髦的镶边criss十字形的妇女的礼服",
          "sku": "sk0008",
          "_id": "57c7da1ef656f20c713bf56e",
          "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160810112221_81491.jpg",
          "price": {
            "symbol": "€",
            "value": "30.69",
            "code": "EUR"
          },
          "special_price": "",
          "url": "/catalog/product/57c7da1ef656f20c713bf56e",
          "product_id": "sk0008"
        }
      }
    ]
  }
}
```
# 5. /catalog/product/index
`某个产品的详情数据`
#### 请求方法
`GET`
#### 请求参数
```json
{
"product_id": "57cfc212f656f28b5adf9deb"//产品id
}
```
#### 返回数据格式
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "product": {
      "groupAttrArr": {
        "重量": "0.2 Kg",
        "风格": "Bohemian",
        "dresses length": "Floor-Length ",
        "pattern type": "Geometric ",
        "sleeve length": "Sleeveless",
        "collar": "Round Neck",
        "颜色": "黄褐色"
      },
      "name": "迷你长袖开衩",
      "sku": "sk1000-khak",
      "package_number": null,
      "spu": "sk1000",
      "thumbnail_img": [
        "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/400/0/2/01/20160715121751_13739.jpg",
        "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/400/0/2/01/20160715121751_31875.jpg",
        "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/400/0/2/01/20160715121751_38104.jpg"
      ],
      "productReview": {
        "_id": {
          "$oid": "57cfc212f656f28b5adf9deb"
        },
        "spu": "sk1000",
        "review_count": 2,
        "coll": [
          {
            "_id": {
              "$oid": "593bba32bfb7ae621c36cc13"
            },
            "product_spu": "sk1000",
            "product_id": "57cfc212f656f28b5adf9deb",
            "rate_star": "1",
            "name": "w w",
            "user_id": 164,
            "ip": "124.126.180.90",
            "summary": "3213123",
            "review_content": "123133131231313",
            "review_date": 1497086514,
            "store": "fecshop.appfront.fancyecommerce.com/cn",
            "lang_code": "zh",
            "status": 1,
            "audit_user": 2,
            "audit_date": 1519295459
          },
          {
            "_id": {
              "$oid": "58132ad7f656f214272f0b7d"
            },
            "product_spu": "sk1000",
            "product_id": "57cfc212f656f28b5adf9deb",
            "rate_star": "5",
            "name": "terr fdf",
            "user_id": 17,
            "ip": "119.123.79.254",
            "summary": "fdasfds",
            "review_content": "dfasfsdfadsfa",
            "review_date": 1477651159,
            "store": "fecshop.appfront.fancyecommerce.com/cn",
            "lang_code": "zh",
            "status": 1,
            "audit_user": 2,
            "audit_date": 1519295463
          }
        ],
        "noActiveStatus": 10
      },
      "custom_option_showImg_attr": "my_color",
      "image_detail": [
        "//img.fancyecommerce.com/media/catalog/product/2/01/20160715121751_31875.jpg",
        "//img.fancyecommerce.com/media/catalog/product/2/01/20160715121751_38104.jpg",
        "//img.fancyecommerce.com/media/catalog/product/2/01/20160715121751_13739.jpg"
      ],
      "attr_group": "clothes_group",
      "review_count": 2,
      "reviw_rate_star_average": 3,
      "reviw_rate_star_info": {
        "star_0": 0,
        "star_1": 50,
        "star_2": 0,
        "star_3": 0,
        "star_4": 0,
        "star_5": 50
      },
      "price_info": {
        "price": {
          "symbol": "€",
          "value": 41.45,
          "code": "EUR"
        },
        "special_price": {
          "symbol": "€",
          "value": 37.73,
          "code": "EUR"
        }
      },
      "tier_price": [
        [
          "个数:",
          "2-3",
          "4-5",
          ">=6"
        ],
        [
          "价格:",
          "€36.8",
          "€35.87",
          "€34.94"
        ]
      ],
      "options": null,
      "custom_option": [],
      "description": "<span id=\"result_box\" lang=\"zh-CN\"><span>颜色：黑色，蓝色，灰色，红色，白色</span><br /><span>尺寸：M，L，XL，2XL</span><br /><span>类别：女装&gt;上衣&gt; T恤＆T恤</span><br /><br /><span>材质：人造丝，氨纶</span><br /><span>服装长度：定期</span><br /><span>袖长：短</span><br /><span>衣领：歪斜领</span><br /><span>风格：休闲</span><br /><span>季节：夏季</span><br /><span>图案类型：花卉</span><br /><span>重量：0.3400kg</span><br /><span>包装内容：1 x T恤</span></span>",
      "_id": "57cfc212f656f28b5adf9deb",
      "buy_also_buy": [
        {
          "one": {
            "name": "对时尚按钮点缀空心网状针织靴子妇女的袖口",
            "sku": "sk2001-blue-zo",
            "_id": "",
            "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160722142719_52348.jpg",
            "price": {
              "symbol": "€",
              "value": 248.59,
              "code": "EUR"
            },
            "special_price": {
              "symbol": "€",
              "value": 133.52,
              "code": "EUR"
            },
            "url": "/catalog/product/57c3aaa9f656f24f353bf56e",
            "product_id": "57c3aaa9f656f24f353bf56e"
          },
          "two": {
            "name": "叶子样式腰部被拉练的礼服",
            "sku": "sk10002-002",
            "_id": "",
            "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160723113749_21685.jpg",
            "price": {
              "symbol": "€",
              "value": 20.46,
              "code": "EUR"
            },
            "special_price": "",
            "url": "/catalog/product/57d610e8f656f29808df9deb",
            "product_id": "57d610e8f656f29808df9deb"
          }
        },
        {
          "one": {
            "name": "时髦的镶边criss十字形的妇女的礼服",
            "sku": "sk0008",
            "_id": "",
            "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160810112221_81491.jpg",
            "price": {
              "symbol": "€",
              "value": 30.69,
              "code": "EUR"
            },
            "special_price": "",
            "url": "/catalog/product/57c7da1ef656f20c713bf56e",
            "product_id": "57c7da1ef656f20c713bf56e"
          },
          "two": {
            "name": "意大利面条打印背面Bodycon衣服",
            "sku": "sk0002",
            "_id": "",
            "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160606112453_71094147323202778861.JPG",
            "price": {
              "symbol": "€",
              "value": 30.69,
              "code": "EUR"
            },
            "special_price": "",
            "url": "/catalog/product/57c7daecf656f273013bf570",
            "product_id": "57c7daecf656f273013bf570"
          }
        },
        {
          "one": {
            "name": "新鲜条纹花卉印花长袖衣袖T恤",
            "sku": "op0002",
            "_id": "",
            "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160805120339_64824.jpg",
            "price": {
              "symbol": "€",
              "value": 30.69,
              "code": "EUR"
            },
            "special_price": {
              "symbol": "€",
              "value": 22.32,
              "code": "EUR"
            },
            "url": "/catalog/product/57e8dd52f656f2a5746234e6",
            "product_id": "57e8dd52f656f2a5746234e6"
          },
          "two": {
            "name": "圆领印花短袖男士T恤",
            "sku": "men0001",
            "_id": "",
            "image": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160624120255_80096.jpg",
            "price": {
              "symbol": "€",
              "value": 30.69,
              "code": "EUR"
            },
            "special_price": "",
            "url": "/catalog/product/57d61555f656f29808df9ded",
            "product_id": "57d61555f656f29808df9ded"
          }
        }
      ]
    }
  }
}
```

# 6. /catalog/product/favorite
`为某个用户收藏某个商品`
#### 请求方法
`GET`
#### 请求参数
```json
{
"product_id": "57cfc212f656f28b5adf9deb" //产品id
}
```
#### 请求头信息
```json
{
"access-token": "aWknazLp87elknsWv6IMKGOJtPU5txEm"
}
```
#### 返回数据格式
##### 未登陆的返回数据
```json
{
  "code": 1100003,
  "message": "account not login or token timeout",
  "data": []
}
```
##### 登陆后的返回数据
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "content": "success"
  }
}
```
# 7. /customer/login/account
`登陆接口`
#### 请求方法
`POST`
#### 请求参数
```json
{
"email": "" ,//账号
"password":"" // 密码
}
```
#### 返回数据格式
###### 登陆失败
```json
{
  "code": 1100002,
  "message": "account login email or password is not correct",
  "data": []
}
```
###### 登陆成功
`返回数据`
```json
{
  "code": 200,
  "message": "process success",
  "data": []
}
```
`返回的头信息`
```json
{
  "Access-Token":"",
  "Fecshop-Uuid":""
}
```
# 8. /customer/register/account
`注册接口`
#### 请求方法
`POST`
#### 请求参数
```json
{
"email": "2@qq.com",
"password": "123456",
"firstname": "abc",
"lastname": "123",
"is_subscribed": "false",
"captcha": "9598"
}
```
#### 返回数据格式
###### 注册失败
```json
{
  "code": 1100007,
  "message": "account register fail",
  "data": {
    "error": "该邮箱地址已经被注册"
  }
}
```
###### 注册成功
`返回数据`
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "content": "register success"
  }
}
```
`返回的头信息`
```json
{
  "Access-Token":"",
  "Fecshop-Uuid":""
}
```
# 9. /customer/account/logout
`退出登录接口`
#### 请求方法
`GET`
#### 请求参数
```json
null
```
#### 请求头信息
```json
{
  "access-token":""
}
```
#### 返回数据格式
```json
{
  "code": 200,
  "message": "process success",
  "data": []
}
```
# 10. /customer/forgot/password
`忘记密码页面`
#### 请求方法
`GET`
#### 返回数据
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "forgotCaptchaActive": true
  }
}
```
# 11. /customer/site/captcha
`获取验证码`
#### 请求方法
`GET`
#### 返回数据
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "image": "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"
  }
}
```
# 12. /customer/forgot/sendcode
`向用户邮箱发送一封忘记密码的邮件`
#### 请求方法
`POST`
#### 请求参数
```json
{
"domain": "http://demo.fancyecommerce.com",
"email": "380037343@qq.com",
"captcha": "5322"
}
```
#### 返回数据
```json
{
"code":200,
"message":"process success",
"data":[]
}
```
# 13. /checkout/cart/add
`将商品加入购物车`
#### 请求方法
`POST`
#### 请求参数
```json
{
"custom_option": "",
"product_id":"",
"qty": "1"
}
```
#### 请求头信息
```json
{
  "access-token":""
}
```
#### 返回数据
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "items_count": 4
  }
}
```
# 14. /checkout/cart/updateinfo
`修改购物车中单个商品的数量 和 删除购物车中的单个条目`
#### 请求方法
`POST`
#### 请求参数
```json
{
"up_type": "add_one|remove|less_one",
"item_id": "2958"
}
```
#### 请求头信息
```json
{
  "access-token":""
}
```
#### 返回数据
```json
{
"code":200,
"message":"process success",
"data":[]
}
```
# 15. /checkout/cart/index
`某用户购物车中的所有条目`
#### 请求方法
`GET`
#### 请求头信息
```json
{
  "access-token":""
}
```
#### 返回数据
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "cart_info": {
      "cart_id": "2320",
      "store": "fecshop.appfront.fancyecommerce.com/cn",
      "items_count": "3",
      "coupon_code": null,
      "shipping_method": "",
      "payment_method": null,
      "grand_total": "61.38",
      "shipping_cost": "0.00",
      "coupon_cost": "0.00",
      "product_total": "61.38",
      "base_grand_total": "66.00",
      "base_shipping_cost": "0.00",
      "base_coupon_cost": "0.00",
      "base_product_total": "66.00",
      "products": [
        {
          "item_id": "2968",
          "active": 0,
          "product_id": "57c3aaa9f656f24f353bf56e",
          "sku": "sk2001-blue-zo",
          "name": "对时尚按钮点缀空心网状针织靴子妇女的袖口",
          "qty": "1",
          "custom_option_sku": "",
          "product_price": 133.52,
          "product_row_price": 133.52,
          "base_product_price": 143.56,
          "base_product_row_price": 143.56,
          "product_weight": 0,
          "product_row_weight": 0,
          "product_volume_weight": null,
          "product_row_volume_weight": 0,
          "product_volume": "0.00",
          "product_row_volume": 0,
          "product_url": "/pair-of-stylish-button-embellished-hollow-out-mesh-shape-knitted-boot-cuffs-for-women",
          "custom_option": [],
          "spu_options": {
            "color": "white",
            "size": "M"
          },
          "img_url": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/150/150/2/01/20160722142719_52348.jpg",
          "url": "/catalog/product/57c3aaa9f656f24f353bf56e",
          "custom_option_info": {
            "color": "white",
            "size": "M"
          }
        },
        {
          "item_id": "3464",
          "active": 1,
          "product_id": "57c7da1ef656f20c713bf56e",
          "sku": "sk0008",
          "name": "时髦的镶边criss十字形的妇女的礼服",
          "qty": "2",
          "custom_option_sku": "",
          "product_price": 30.69,
          "product_row_price": 61.38,
          "base_product_price": 33,
          "base_product_row_price": 66,
          "product_weight": 0,
          "product_row_weight": 0,
          "product_volume_weight": null,
          "product_row_volume_weight": 0,
          "product_volume": "0.00",
          "product_row_volume": 0,
          "product_url": "/stylish-striped-criss-cross-womens-dress",
          "custom_option": [],
          "spu_options": {
            "color": "white & black",
            "size": "M"
          },
          "img_url": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/150/150/2/01/20160810112221_81491.jpg",
          "url": "/catalog/product/57c7da1ef656f20c713bf56e",
          "custom_option_info": {
            "color": "white & black",
            "size": "M"
          }
        }
      ],
      "product_weight": "0.00",
      "product_volume_weight": "0.00",
      "product_volume": "0.00"
    },
    "currency": {
      "code": "EUR",
      "rate": 0.93,
      "symbol": "€"
    }
  }
}
```

# 16. /checkout/cart/selectall
`全选和反选购物车中的产品`
#### 请求方法
`GET`
#### 请求参数
```json
{
  "checked":0
}
```
#### 请求头信息
```json
{
  "access-token":""
}
```
#### 返回数据
```json
{
  "code": 200,
  "message": "process success",
  "data": []
}
```
# 17. /customer/productfavorite/index
`收藏列表`
#### 请求方法
`GET`
#### 请求头信息
```json
{
  "access-token":""
}
```
#### 返回数据
```json
{
  "code": 200,
  "message": "process success",
  "data": {
    "productList": [
      {
        "_id": {
          "$oid": "57cfc212f656f28b5adf9deb"
        },
        "name": "迷你长袖开衩",
        "url_key": "/alluring-long-sleeve-open-back-draped-maxi-dress-55525232",
        "price": 44.56,
        "special_price": 40.56,
        "special_from": 0,
        "special_to": 0,
        "image": {
          "gallery": [
            {
              "image": "/2/01/20160715121751_31875.jpg",
              "label": "",
              "sort_order": "",
              "is_thumbnails": "1",
              "is_detail": "1"
            },
            {
              "image": "/2/01/20160715121751_38104.jpg",
              "label": "",
              "sort_order": "",
              "is_thumbnails": "1",
              "is_detail": "1"
            }
          ],
          "main": {
            "image": "/2/01/20160715121751_13739.jpg",
            "label": "",
            "sort_order": "",
            "is_thumbnails": "1",
            "is_detail": "1"
          }
        },
        "updated_at": "2018-06-19 10:48:13",
        "favorite_id": "5b286eedbfb7ae30fc096b52",
        "imgUrl": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/2/01/20160715121751_13739.jpg",
        "price_info": {
          "price": {
            "symbol": "€",
            "value": 41.45,
            "code": "EUR"
          },
          "special_price": {
            "symbol": "€",
            "value": 37.73,
            "code": "EUR"
          }
        },
        "product_id": "57cfc212f656f28b5adf9deb"
      },
      {
        "_id": {
          "$oid": "5819941ef656f28a2a2f0b77"
        },
        "name": "测试计算机",
        "url_key": "/test-computer",
        "price": 33,
        "special_price": 0,
        "special_from": 0,
        "special_to": 0,
        "image": {
          "main": {
            "image": "/1/11/111.jpg",
            "label": "",
            "sort_order": "",
            "is_thumbnails": "1",
            "is_detail": "1"
          }
        },
        "updated_at": "2018-05-17 09:23:26",
        "favorite_id": "5afcd98ebfb7ae3eb66e664c",
        "imgUrl": "//img.fancyecommerce.com/media/catalog/product/cache/bd935443df1c50537d4edaab4af5d446/296/0/1/11/111.jpg",
        "price_info": {
          "price": {
            "symbol": "€",
            "value": 30.69,
            "code": "EUR"
          }
        },
        "product_id": "5819941ef656f28a2a2f0b77"
      }
    ],
    "count": 2,
    "numPerPage": null
  }
}
```
# 18. /customer/productfavorite/remove
`删除收藏中的产品`
#### 请求方法
`POST`
#### 请求参数
```json
{
    "favorite_id":"543"
}
```
#### 请求头信息
```json
{
  "access-token":""
}
```
#### 返回数据
```json
{
    "code": 200,
    "message": "process success",
    "data": []
}
```

