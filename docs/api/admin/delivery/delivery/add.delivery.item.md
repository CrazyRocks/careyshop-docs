# 添加一个配送方式

#### 接口描述：
- 添加一个配送方式。

#### 请求 URL：
- `http|https://host/api/v1/delivery/method/add.delivery.item/`

#### 请求方式：
- GET
- POST

#### 是否授权：
- 需要授权

#### 业务参数：
|参数名|类型|是否必须|范围值|默认值|示例值|描述|
|:----|:---|:---:|:-----|:-----|:-----|-----|
|delivery_item_id |integer |是 |gt:0 | |7 |快递公司编号 |
|content |string |否 |max:150 | |EMS |配送方式描述 |
|first_weight |number |是 |egt:0 | |1.00 |首重 |
|first_weight_price |number |是 |egt:0 | |8.00 |续重费运 |
|second_weight |number |是 |egt:0 | |1.00 |续重 |
|second_weight_price |number |是 |egt:0 | |5.00 |续重运费 |
|first_item |integer |是 |between:0,255 | |1 |首件 |
|first_item_price |number |是 |egt:0 | |8.00 |首件运费 |
|second_item |integer |是 |between:0,255 | |1 |续件 |
|second_item_price |number |是 |egt:0 | |5.00 |续件运费 |
|first_volume |number |是 |egt:0 | |2 |首体积量 |
|first_volume_price |number |是 |egt:0 | |10.00 |首体积运费 |
|second_volume |number |是 |egt:0 | |1.00 |续体积量 |
|second_volume_price |number |是 |egt:0 | |5.00 |续体积运费 |
|sort |integer |否 |between:0,255 |50 |50 |配送方式排序值 |
|status |integer |否 |in:0,1 |1 |1 |配送方式状态 0=禁用 1=启用|

#### 响应参数：
|参数名|类型|是否返回|示例值|描述|
|:-----|:-----|:---:|:-----|-----|
|status |integer |是 |200 |状态码 |
|message |string |是 |success |消息信息 |
|data |object |是 |[] |返回对象 |

|data|类型|是否返回|示例值|描述|
|:-----|:-----|:---:|:-----|-----|
|delivery_item_id |integer |是 |7 |快递公司编号 |
|content |string |否 |EMS |配送方式描述 |
|first_weight |number |是 |1 |首重 |
|first_weight_price |number |是 |8 |续重费运 |
|second_weight |number |是 |1 |续重 |
|second_weight_price |number |是 |5 |续重运费 |
|first_item |integer |是 |1 |首件 |
|first_item_price |number |是 |8 |首件运费 |
|second_item |integer |是 |1 |续件 |
|second_item_price |number |是 |5 |续件运费 |
|first_volume |number |是 |2 |首体积量 |
|first_volume_price |number |是 |10 |首体积运费 |
|second_volume |number |是 |1 |续体积量 |
|second_volume_price |number |是 |5 |续体积运费 |
|sort |integer |否 |50 |配送方式排序值 |
|status |integer |否 |1 |配送方式状态 0=禁用 1=启用|
|delivery_id |integer |是 |9 |配送方式编号 |

#### 响应示例：
```json
{
  "status": 200,
  "message": "success",
  "data": {
    "delivery_item_id": 7,
    "content": "EMS",
    "first_weight": 1,
    "first_weight_price": 8,
    "second_weight": 1,
    "second_weight_price": 5,
    "first_item": 1,
    "first_item_price": 8,
    "second_item": 1,
    "second_item_price": 5,
    "first_volume": 2,
    "first_volume_price": 10,
    "second_volume": 1,
    "second_volume_price": 5,
    "sort": 50,
    "status": 1,
    "delivery_id": 9
  }
}
```

#### 备注:
无