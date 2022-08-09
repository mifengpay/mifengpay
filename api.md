## /all
```text
暂无描述
```
#### 公共Header参数
参数名 | 示例值 | 参数描述
--- | --- | ---
暂无参数
#### 公共Query参数
参数名 | 示例值 | 参数描述
--- | --- | ---
暂无参数
#### 公共Body参数
参数名 | 示例值 | 参数描述
--- | --- | ---
暂无参数
#### 预执行脚本
```javascript
暂无预执行脚本
```
#### 后执行脚本
```javascript
暂无后执行脚本
```
## /all/api
```text
暂无描述
```
#### 公共Header参数
参数名 | 示例值 | 参数描述
--- | --- | ---
暂无参数
#### 公共Query参数
参数名 | 示例值 | 参数描述
--- | --- | ---
暂无参数
#### 公共Body参数
参数名 | 示例值 | 参数描述
--- | --- | ---
暂无参数
#### 预执行脚本
```javascript
暂无预执行脚本
```
#### 后执行脚本
```javascript
暂无后执行脚本
```
## /all/api/统一下单
```text
暂无描述
```
#### 接口状态
> 开发中

#### 接口URL
> https://open.mifengpay.com:27102/v1/api/pay/unifiedorder

#### 请求方式
> POST

#### Content-Type
> json

#### 请求Body参数
```javascript
{
	"token": "1",
    "channel_no":1,
	"subject": "标题",
	"out_order_no": "20213557897313123",
	"money": "1000.12",
	"client_ip": "0.0.0.0",
	"notify_url": "https://baidu.com",
	"return_url": "https://jump.com",
	"param": "Iloveyou",
	"timestamp": 1626863144831
}
```
#### 预执行脚本
```javascript
暂无预执行脚本
```
#### 后执行脚本
```javascript
暂无后执行脚本
```
#### 成功响应示例
```javascript
{
	"code": 0,
	"msg": "",
	"data": {
		"mch_id": 1000011,
		"order_no": "20220802202158972560",
		"out_order_no": "20213557897313123",
		"money": "1000.12",
		"pay_url": "",
		"expired_time": "2022-08-02 20:21:58",
		"expired_timestamp": 1659442918762
	},
	"request_id": ""
}
```
参数名 | 示例值 | 参数类型 | 参数描述
--- | --- | --- | ---
code | - | Number | 错误码
msg | - | Object | 错误字符串
data | - | Object | 返回值
data.mch_id | 1000011 | Number | 商户号,唯一的商户编号 
data.order_no | 20220802202158972560 | String | 订单号
data.out_order_no | 20213557897313123 | String | 商户订单号
data.money | 1000.12 | String | 金钱,小数字符串
data.pay_url | - | Object | 支付链接
data.expired_time | 2022-08-02 20:21:58 | String | 过期时间
data.expired_timestamp | 1659442918762 | Number | 过期时间时间戳毫秒
request_id | - | Object | 
#### 错误响应示例
```javascript
{
	"code": 12,
	"msg": "Money参数有误",
	"data": {
		"mch_id": 0,
		"order_no": "",
		"out_order_no": "",
		"money": "",
		"pay_url": "",
		"expired_time": "",
		"expired_timestamp": 0
	},
	"request_id": ""
}
```
参数名 | 示例值 | 参数类型 | 参数描述
--- | --- | --- | ---
code | 12 | Number | 错误码
msg | Money参数有误 | String | 错误字符串
data | - | Object | 返回值
data.mch_id | - | Number | 商户号,唯一的商户编号 
data.order_no | - | Object | 订单号
data.out_order_no | - | Object | 商户订单号
data.money | - | Object | 金额，单位为元，精确到小数点后两位
data.pay_url | - | Object | 支付链接
data.expired_time | - | Object | 过期时间
data.expired_timestamp | - | Number | 过期时间时间戳毫秒
request_id | - | Object | 
## /all/api/订单查询
```text
暂无描述
```
#### 接口状态
> 开发中

#### 接口URL
> 未填写

#### 请求方式
> POST

#### Content-Type
> form-data

#### 预执行脚本
```javascript
暂无预执行脚本
```
#### 后执行脚本
```javascript
暂无后执行脚本
```
## /all/api/余额查询
```text
暂无描述
```
#### 接口状态
> 开发中

#### 接口URL
> https://open.mifengpay.com:27102/v1/api/pay/balance

#### 请求方式
> POST

#### Content-Type
> json

#### 请求Body参数
```javascript
{
    "token":"1"
}
```
#### 预执行脚本
```javascript
暂无预执行脚本
```
#### 后执行脚本
```javascript
暂无后执行脚本
```
#### 成功响应示例
```javascript
{
	"code": 0,
	"msg": "",
	"data": {
		"balance": "1000.00"
	},
	"request_id": ""
}
```
## /all/api/获取TOKEN + JSON
```text
暂无描述
```
#### 接口状态
> 开发中

#### 接口URL
> https://open.mifengpay.com:27102/v1/api/pay/accesstoken

#### 请求方式
> POST

#### Content-Type
> json

#### 请求Body参数
```javascript
{
	"mch_id": 100045,
	"secret": "3ZWQBPN5SFP7MW6EQHXSCGLMAZVJZT3I",
	"request_id": "4BEFBD36AB2C45DFA24232B52BFC7311"
}
```
参数名 | 示例值 | 参数类型 | 是否必填 | 参数描述
--- | --- | --- | --- | ---
mch_id | 100045 | String | 是 | 商户号,唯一的商户编号 
secret | 3ZWQBPN5SFP7MW6EQHXSCGLMAZVJZT3I | String | 是 | 密钥
request_id | 4BEFBD36AB2C45DFA24232B52BFC7311 | String | 是 | -
#### 预执行脚本
```javascript
暂无预执行脚本
```
#### 后执行脚本
```javascript
暂无后执行脚本
```
## /all/api/获取TOKEN  + Query 
```text
暂无描述
```
#### 接口状态
> 开发中

#### 接口URL
> https://open.mifengpay.com:27102/v1/api/pay/accesstoken?mch_id=100045&secret=3ZWQBPN5SFP7MW6EQHXSCGLMAZVJZT3I&request_id=4BEFBD36AB2C45DFA24232B52BFC7311

#### 请求方式
> GET

#### Content-Type
> form-data

#### 请求Query参数
参数名 | 示例值 | 参数类型 | 是否必填 | 参数描述
--- | --- | --- | --- | ---
mch_id | 100045 | Text | 是 | -
secret | 3ZWQBPN5SFP7MW6EQHXSCGLMAZVJZT3I | Text | 是 | -
request_id | 4BEFBD36AB2C45DFA24232B52BFC7311 | Text | 是 | -
#### 预执行脚本
```javascript
暂无预执行脚本
```
#### 后执行脚本
```javascript
暂无后执行脚本
```
## /all/api/获取TOKEN + FormData
```text
暂无描述
```
#### 接口状态
> 开发中

#### 接口URL
> https://open.mifengpay.com:27102/v1/api/pay/accesstoken

#### 请求方式
> GET

#### Content-Type
> form-data

#### 请求Body参数
参数名 | 示例值 | 参数类型 | 是否必填 | 参数描述
--- | --- | --- | --- | ---
mch_id | 100045 | Text | 是 | 商户号,唯一的商户编号 
secret | 3ZWQBPN5SFP7MW6EQHXSCGLMAZVJZT3I | Text | 是 | 密钥
request_id | 4BEFBD36AB2C45DFA24232B52BFC7311 | Text | 否 | -
#### 预执行脚本
```javascript
暂无预执行脚本
```
#### 后执行脚本
```javascript
暂无后执行脚本
```
