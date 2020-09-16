# 买家上报换货、维修后的快递单号

#### 接口描述：
- 买家上报换货、维修后的快递单号,并填写商家寄回时需要的信息。

#### 请求 URL：
- `http|https://host/api/v1/order_service/method/set.order.service.buyer/`

#### 请求方式：
- GET
- POST

#### 是否授权：
- 需要授权

#### 业务参数：
|参数名|类型|是否必须|范围值|默认值|示例值|描述|
|:----|:---|:---:|:-----|:-----|:-----|-----|
|service_no |string |是 |max:50 | |SH_I6264796358679190001 |售后单号 |
|address |string |是 |max:255 | |浙江省 宁波市 江北区 |返件地址 |
|consignee |string |是 |max:30 | |张三 |委托人 |
|zipcode |string |否 |max:20 | |315000 |邮编 |
|mobile |string |是 |length:7,15 | |87487585 |电话 |
|logistic_code |string |是 |max:50 | |0123456 |快递单号 |
|delivery_item_id |integer |是 |gt:0 | |1 |快递公司编号 |

#### 响应参数：
|参数名|类型|是否返回|示例值|描述|
|:-----|:-----|:---:|:-----|-----|
|status |integer |是 |200 |状态码 |
|message |string |是 |success |消息信息 |
|data |boolean |是 |true |返回 true 表示执行成功 |

#### 响应示例：
```json
{
  "status": 200,
  "message": "success",
  "data": true
}
```

#### 备注:
无