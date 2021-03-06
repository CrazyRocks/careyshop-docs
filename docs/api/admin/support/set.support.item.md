# 编辑一名客服

#### 接口描述：
- 编辑一名客服。

#### 请求 URL：
- `http|https://host/api/v1/support/method/set.support.item/`

#### 请求方式：
- GET
- POST

#### 是否授权：
- 需要授权

#### 业务参数：
|参数名|类型|是否必须|范围值|默认值|示例值|描述|
|:----|:---|:---:|:-----|:-----|:-----|-----|
|support_id |integer |是 |gt:0 | |1 |客服编号 |
|type_name |string |否 |max:50 | |售前客服 |客服组名称 |
|nick_name |string |否 |max:50 | |张三 |客服昵称 |
|code |string |否 |max:150 | |javascript:; |联系方式(自定义特征码) |
|sort |integer |否 |between:0,255 | |50 |客服排序值 |
|status |integer |否 |in:0,1 | |1 |客服状态 0=禁用 1=启用 |

#### 响应参数：
|参数名|类型|是否返回|示例值|描述|
|:-----|:-----|:---:|:-----|-----|
|status |integer |是 |200 |状态码 |
|message |string |是 |success |消息信息 |
|data |object |是 |[] |返回对象 |

|data|类型|是否返回|示例值|描述|
|:-----|:-----|:---:|:-----|-----|
|support_id |integer |是 |1 |客服编号 |
|type_name |string |否 |售前客服 |客服组名称 |
|nick_name |string |否 |张三 |客服昵称 |
|code |string |否 |javascript:; |联系方式(自定义特征码) |
|sort |integer |否 |50 |客服排序值 |
|status |integer |否 |1 |客服状态 0=禁用 1=启用 |

#### 响应示例：
```json
{
  "status": 200,
  "message": "success",
  "data": {
    "support_id": 1,
    "type_name": "售前客服",
    "nick_name": "张三",
    "code": "javascript:;",
    "sort": 50,
    "status": 1
  }
}
```

#### 备注:
1. 业务参数`是否必须`一栏中被标注为`否`时，可不填写此参数，表示该接口可单独修改某个字段。