# 获取一个友情链接

#### 接口描述：
- 获取一个友情链接。

#### 请求 URL：
- `http|https://host/api/v1/friend_link/method/get.friendlink.item/`

#### 请求方式：
- GET
- POST

#### 是否授权：
- 需要授权

#### 业务参数：
|参数名|类型|是否必须|范围值|默认值|示例值|描述|
|:----|:---|:---:|:-----|:-----|:-----|-----|
|friend_link_id |integer |是 |gt:0 | |1 |友情链接编号 |

#### 响应参数：
|参数名|类型|是否返回|示例值|描述|
|:-----|:-----|:---:|:-----|-----|
|status |integer |是 |200 |状态码 |
|message |string |是 |success |消息信息 |
|data |object |否 |[] |返回对象 |

|data|类型|是否返回|示例值|描述|
|:-----|:-----|:---:|:-----|-----|
|friend_link_id |integer |是 |1 |友情链接编号 |
|name |string |是 |CareyShop |友情链接名称 |
|url |string |是 |http://carey.shop |友情链接Url |
|logo |string |是 |//logo.png |友情链接Logo |
|target |string |是 |_blank |打开方式 |
|sort |integer |是 |0 |友情链接排序值 |
|status |integer |是 |1 |友情链接状态 0=禁用 1=启用 |

#### 响应示例：
```json
{
  "status": 200,
  "message": "success",
  "data": {
    "friend_link_id": 1,
    "name": "CareyShop",
    "url": "http://carey.shop",
    "logo": "//logo.png",
    "target": "_blank",
    "sort": 0,
    "status": 1
  }
}
```

#### 备注:
无