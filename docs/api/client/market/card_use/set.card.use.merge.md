# 相同购物卡进行余额合并

#### 接口描述：
- 相同购物卡进行余额合并。

#### 请求 URL：
- `http|https://host/api/v1/card_use/method/set.card.use.merge/`

#### 请求方式：
- GET
- POST

#### 是否授权：
- 需要授权

#### 业务参数：
|参数名|类型|是否必须|范围值|默认值|示例值|描述|
|:----|:---|:---:|:-----|:-----|:-----|-----|
|number |string |是 |length:16 | |9514677739431425 |卡号 |
|src_number |string |是 |length:16 | |1818337623626955 |被合并卡卡号 |
|money |number |否 |egt:0 |0 |100 |合并金额 |

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
1. 当参数`money` `不提交`或值为`0`时将合并`被合并卡`的全部可用余额。