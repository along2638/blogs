# datafusion服务


**简介**:datafusion服务


**HOST**:192.168.2.100:10021


**联系人**:


**Version**:1.0


**接口路径**:/v2/api-docs


[TOC]






# OpenLevelAPI


## 条件查询关卡


**接口地址**:`/v1/level/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "projectId": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|openLevelQueryReq|openLevelQueryReq|body|true|关卡对象0|关卡对象0|
|&emsp;&emsp;projectId|项目id||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«关卡对象»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|关卡对象|
|&emsp;&emsp;id||string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;remark|备注|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"id": "",
			"name": "",
			"remark": ""
		}
	]
}
```


# OpenLifeAPI


## 生命体操作


**接口地址**:`/v1/life/data/command`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "functionMethod": "",
  "functionParam": [],
  "ids": [],
  "isExclude": true,
  "module": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|openLifeDictDataCommandReq|生命体命令请求体|body|true|OpenLifeDictDataCommandReq|OpenLifeDictDataCommandReq|
|&emsp;&emsp;functionMethod|||false|string||
|&emsp;&emsp;functionParam|||false|array|object|
|&emsp;&emsp;ids|||false|array|string|
|&emsp;&emsp;isExclude|||false|boolean||
|&emsp;&emsp;module|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 条件查询生命体


**接口地址**:`/v1/life/data/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "name": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|openLifeDictDataQueryReq|生命体查询|body|true|OpenLifeDictDataQueryReq|OpenLifeDictDataQueryReq|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;name|生命体名称||false|string||
|&emsp;&emsp;type|生命体类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«OpenLifeDictDataQueryRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||OpenLifeDictDataQueryRes|OpenLifeDictDataQueryRes|
|&emsp;&emsp;id||string||
|&emsp;&emsp;levelId||string||
|&emsp;&emsp;name||string||
|&emsp;&emsp;transform||TransformDTO|TransformDTO|
|&emsp;&emsp;&emsp;&emsp;location||string||
|&emsp;&emsp;&emsp;&emsp;rotation||string||
|&emsp;&emsp;&emsp;&emsp;scale||string||
|&emsp;&emsp;type||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"id": "",
		"levelId": "",
		"name": "",
		"transform": {
			"location": "",
			"rotation": "",
			"scale": ""
		},
		"type": ""
	}
}
```


# OpenProjectAPI


## 条件查询项目


**接口地址**:`/v1/project/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": "",
  "remark": "",
  "sceneBindId": "",
  "thumbnailUrl": "",
  "toolBindId": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|openProjectQueryReq|openProjectQueryReq|body|true|项目对象0|项目对象0|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;sceneBindId|绑定场景id||false|string||
|&emsp;&emsp;thumbnailUrl|项目缩略图url||false|string||
|&emsp;&emsp;toolBindId|绑定工具id||false|string||
|&emsp;&emsp;type|类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«项目对象»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|项目对象|
|&emsp;&emsp;id||string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sceneBindId|绑定场景id|string||
|&emsp;&emsp;thumbnailUrl|项目缩略图url|string||
|&emsp;&emsp;toolBindId|绑定工具id|string||
|&emsp;&emsp;type|类型|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"id": "",
			"name": "",
			"remark": "",
			"sceneBindId": "",
			"thumbnailUrl": "",
			"toolBindId": "",
			"type": ""
		}
	]
}
```


# api环境变量管理


## 新增环境变量


**接口地址**:`/api-env-var`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "envId": "",
  "id": "",
  "varName": "",
  "varValue": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvVarReq|api环境值表|body|true|api环境值表0|api环境值表0|
|&emsp;&emsp;envId|环境id||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;varName|变量key||false|string||
|&emsp;&emsp;varValue|变量value||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 修改环境变量


**接口地址**:`/api-env-var`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "envId": "",
  "id": "",
  "varName": "",
  "varValue": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvVarReq|api环境值表|body|true|api环境值表0|api环境值表0|
|&emsp;&emsp;envId|环境id||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;varName|变量key||false|string||
|&emsp;&emsp;varValue|变量value||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id删除环境变量


**接口地址**:`/api-env-var`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据条件查询环境变量


**接口地址**:`/api-env-var/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "envId": "",
  "id": "",
  "varName": "",
  "varValue": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvVarReq|api环境值表|body|true|api环境值表0|api环境值表0|
|&emsp;&emsp;envId|环境id||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;varName|变量key||false|string||
|&emsp;&emsp;varValue|变量value||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«api环境值表»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|api环境值表|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;envId|环境id|string||
|&emsp;&emsp;id|id|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;varName|变量key|string||
|&emsp;&emsp;varValue|变量value|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"createBy": "",
			"createTime": "",
			"envId": "",
			"id": "",
			"updateBy": "",
			"updateTime": "",
			"varName": "",
			"varValue": ""
		}
	]
}
```


# api详情表管理


## 新增api接口


**接口地址**:`/api-detail`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "appId": "",
  "contentType": "",
  "descr": "",
  "id": "",
  "method": "",
  "name": "",
  "page": 0,
  "reqJsonValue": "",
  "size": 0,
  "suffixUrl": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiDetailReq|api详情表|body|true|api详情表|api详情表|
|&emsp;&emsp;appId|app id||false|string||
|&emsp;&emsp;contentType|null,application/x-www-form-urlencoded,application/json||false|string||
|&emsp;&emsp;descr|api描述||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;method|GET,POST,DELETE,CREATE||false|string||
|&emsp;&emsp;name|api名称||false|string||
|&emsp;&emsp;page|page||false|integer(int32)||
|&emsp;&emsp;reqJsonValue|请求体json值||false|string||
|&emsp;&emsp;size|size||false|integer(int32)||
|&emsp;&emsp;suffixUrl|后置路径||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«ApiDetailBO»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||ApiDetailBO|ApiDetailBO|
|&emsp;&emsp;appId||string||
|&emsp;&emsp;bodyList||array|ApiReqFormFieldBO|
|&emsp;&emsp;&emsp;&emsp;apiId||string||
|&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;descr||string||
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;reqType||string||
|&emsp;&emsp;&emsp;&emsp;type||string||
|&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;&emsp;&emsp;value||string||
|&emsp;&emsp;contentType||string||
|&emsp;&emsp;createBy||string||
|&emsp;&emsp;createTime||string(date-time)||
|&emsp;&emsp;descr||string||
|&emsp;&emsp;headerList||array|ApiReqFormFieldBO|
|&emsp;&emsp;&emsp;&emsp;apiId||string||
|&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;descr||string||
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;reqType||string||
|&emsp;&emsp;&emsp;&emsp;type||string||
|&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;&emsp;&emsp;value||string||
|&emsp;&emsp;id||string||
|&emsp;&emsp;method||string||
|&emsp;&emsp;name||string||
|&emsp;&emsp;pathList||array|ApiReqFormFieldBO|
|&emsp;&emsp;&emsp;&emsp;apiId||string||
|&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;descr||string||
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;reqType||string||
|&emsp;&emsp;&emsp;&emsp;type||string||
|&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;&emsp;&emsp;value||string||
|&emsp;&emsp;queryList||array|ApiReqFormFieldBO|
|&emsp;&emsp;&emsp;&emsp;apiId||string||
|&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;descr||string||
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;reqType||string||
|&emsp;&emsp;&emsp;&emsp;type||string||
|&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;&emsp;&emsp;value||string||
|&emsp;&emsp;reqJsonValue||string||
|&emsp;&emsp;suffixUrl||string||
|&emsp;&emsp;updateBy||string||
|&emsp;&emsp;updateTime||string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"appId": "",
		"bodyList": [
			{
				"apiId": "",
				"createBy": "",
				"createTime": "",
				"descr": "",
				"id": "",
				"name": "",
				"reqType": "",
				"type": "",
				"updateBy": "",
				"updateTime": "",
				"value": ""
			}
		],
		"contentType": "",
		"createBy": "",
		"createTime": "",
		"descr": "",
		"headerList": [
			{
				"apiId": "",
				"createBy": "",
				"createTime": "",
				"descr": "",
				"id": "",
				"name": "",
				"reqType": "",
				"type": "",
				"updateBy": "",
				"updateTime": "",
				"value": ""
			}
		],
		"id": "",
		"method": "",
		"name": "",
		"pathList": [
			{
				"apiId": "",
				"createBy": "",
				"createTime": "",
				"descr": "",
				"id": "",
				"name": "",
				"reqType": "",
				"type": "",
				"updateBy": "",
				"updateTime": "",
				"value": ""
			}
		],
		"queryList": [
			{
				"apiId": "",
				"createBy": "",
				"createTime": "",
				"descr": "",
				"id": "",
				"name": "",
				"reqType": "",
				"type": "",
				"updateBy": "",
				"updateTime": "",
				"value": ""
			}
		],
		"reqJsonValue": "",
		"suffixUrl": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 修改api接口


**接口地址**:`/api-detail`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "appId": "",
  "contentType": "",
  "descr": "",
  "id": "",
  "method": "",
  "name": "",
  "page": 0,
  "reqJsonValue": "",
  "size": 0,
  "suffixUrl": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiDetailReq|api详情表|body|true|api详情表|api详情表|
|&emsp;&emsp;appId|app id||false|string||
|&emsp;&emsp;contentType|null,application/x-www-form-urlencoded,application/json||false|string||
|&emsp;&emsp;descr|api描述||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;method|GET,POST,DELETE,CREATE||false|string||
|&emsp;&emsp;name|api名称||false|string||
|&emsp;&emsp;page|page||false|integer(int32)||
|&emsp;&emsp;reqJsonValue|请求体json值||false|string||
|&emsp;&emsp;size|size||false|integer(int32)||
|&emsp;&emsp;suffixUrl|后置路径||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id删除api接口


**接口地址**:`/api-detail`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 调试api接口


**接口地址**:`/api-detail/debug`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "apiId": "",
  "envId": "",
  "globalVarIds": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiDebugQueryReq|api接口调试入参|body|true|ApiDebugReq|ApiDebugReq|
|&emsp;&emsp;apiId|api接口id||false|string||
|&emsp;&emsp;envId|环境id||false|string||
|&emsp;&emsp;globalVarIds|勾选全局变量ids，多个以逗号分隔||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 根据条件分页查询api接口


**接口地址**:`/api-detail/queryByPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "appId": "",
  "contentType": "",
  "descr": "",
  "id": "",
  "method": "",
  "name": "",
  "page": 0,
  "reqJsonValue": "",
  "size": 0,
  "suffixUrl": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiDetailReq|api详情表|body|true|api详情表|api详情表|
|&emsp;&emsp;appId|app id||false|string||
|&emsp;&emsp;contentType|null,application/x-www-form-urlencoded,application/json||false|string||
|&emsp;&emsp;descr|api描述||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;method|GET,POST,DELETE,CREATE||false|string||
|&emsp;&emsp;name|api名称||false|string||
|&emsp;&emsp;page|page||false|integer(int32)||
|&emsp;&emsp;reqJsonValue|请求体json值||false|string||
|&emsp;&emsp;size|size||false|integer(int32)||
|&emsp;&emsp;suffixUrl|后置路径||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«ApiDetailBO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«ApiDetailBO»|IPage«ApiDetailBO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|ApiDetailBO|
|&emsp;&emsp;&emsp;&emsp;appId||string||
|&emsp;&emsp;&emsp;&emsp;bodyList||array|ApiReqFormFieldBO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;apiId||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;descr||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;reqType||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;type||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;value||string||
|&emsp;&emsp;&emsp;&emsp;contentType||string||
|&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;descr||string||
|&emsp;&emsp;&emsp;&emsp;headerList||array|ApiReqFormFieldBO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;apiId||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;descr||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;reqType||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;type||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;value||string||
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;method||string||
|&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;pathList||array|ApiReqFormFieldBO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;apiId||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;descr||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;reqType||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;type||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;value||string||
|&emsp;&emsp;&emsp;&emsp;queryList||array|ApiReqFormFieldBO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;apiId||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;descr||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;reqType||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;type||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;value||string||
|&emsp;&emsp;&emsp;&emsp;reqJsonValue||string||
|&emsp;&emsp;&emsp;&emsp;suffixUrl||string||
|&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"appId": "",
				"bodyList": [
					{
						"apiId": "",
						"createBy": "",
						"createTime": "",
						"descr": "",
						"id": "",
						"name": "",
						"reqType": "",
						"type": "",
						"updateBy": "",
						"updateTime": "",
						"value": ""
					}
				],
				"contentType": "",
				"createBy": "",
				"createTime": "",
				"descr": "",
				"headerList": [
					{
						"apiId": "",
						"createBy": "",
						"createTime": "",
						"descr": "",
						"id": "",
						"name": "",
						"reqType": "",
						"type": "",
						"updateBy": "",
						"updateTime": "",
						"value": ""
					}
				],
				"id": "",
				"method": "",
				"name": "",
				"pathList": [
					{
						"apiId": "",
						"createBy": "",
						"createTime": "",
						"descr": "",
						"id": "",
						"name": "",
						"reqType": "",
						"type": "",
						"updateBy": "",
						"updateTime": "",
						"value": ""
					}
				],
				"queryList": [
					{
						"apiId": "",
						"createBy": "",
						"createTime": "",
						"descr": "",
						"id": "",
						"name": "",
						"reqType": "",
						"type": "",
						"updateBy": "",
						"updateTime": "",
						"value": ""
					}
				],
				"reqJsonValue": "",
				"suffixUrl": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


# api请求表单字段表管理


## 新增api接口请求参数


**接口地址**:`/api-req-form-field`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "apiId": "",
  "descr": "",
  "id": "",
  "name": "",
  "reqType": "",
  "type": "",
  "value": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiReqFormFieldReq|api请求表单字段表|body|true|api请求表单字段表|api请求表单字段表|
|&emsp;&emsp;apiId|api id||false|string||
|&emsp;&emsp;descr|参数说明||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|参数名称||false|string||
|&emsp;&emsp;reqType|请求类型（0 header、1 param、2 param的query参数、3 body中的application/x-www-form-urlencoded）||false|string||
|&emsp;&emsp;type|参数类型（string/integer/array/number）||false|string||
|&emsp;&emsp;value|参数值||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 修改api接口请求参数


**接口地址**:`/api-req-form-field`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "apiId": "",
  "descr": "",
  "id": "",
  "name": "",
  "reqType": "",
  "type": "",
  "value": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiReqFormFieldReq|api请求表单字段表|body|true|api请求表单字段表|api请求表单字段表|
|&emsp;&emsp;apiId|api id||false|string||
|&emsp;&emsp;descr|参数说明||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|参数名称||false|string||
|&emsp;&emsp;reqType|请求类型（0 header、1 param、2 param的query参数、3 body中的application/x-www-form-urlencoded）||false|string||
|&emsp;&emsp;type|参数类型（string/integer/array/number）||false|string||
|&emsp;&emsp;value|参数值||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id删除api接口请求参数


**接口地址**:`/api-req-form-field`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 根据条件查询api接口请求参数


**接口地址**:`/api-req-form-field/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "apiId": "",
  "descr": "",
  "id": "",
  "name": "",
  "reqType": "",
  "type": "",
  "value": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiReqFormFieldReq|api请求表单字段表|body|true|api请求表单字段表|api请求表单字段表|
|&emsp;&emsp;apiId|api id||false|string||
|&emsp;&emsp;descr|参数说明||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|参数名称||false|string||
|&emsp;&emsp;reqType|请求类型（0 header、1 param、2 param的query参数、3 body中的application/x-www-form-urlencoded）||false|string||
|&emsp;&emsp;type|参数类型（string/integer/array/number）||false|string||
|&emsp;&emsp;value|参数值||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«api请求表单字段表»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|api请求表单字段表0|
|&emsp;&emsp;apiId|api id|string||
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;descr|参数说明|string||
|&emsp;&emsp;id|id|string||
|&emsp;&emsp;name|参数名称|string||
|&emsp;&emsp;reqType|请求类型（0 header、1 param、2 param的query参数、3 body中的application/x-www-form-urlencoded）|string||
|&emsp;&emsp;type|参数类型（string/integer/array/number）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;value|参数值|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"apiId": "",
			"createBy": "",
			"createTime": "",
			"descr": "",
			"id": "",
			"name": "",
			"reqType": "",
			"type": "",
			"updateBy": "",
			"updateTime": "",
			"value": ""
		}
	]
}
```


# app详情表管理


## 新增数据源


**接口地址**:`/app-detail`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "countId": "",
  "current": 0,
  "descr": "",
  "id": "",
  "maxLimit": 0,
  "name": "",
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "records": [],
  "searchCount": true,
  "size": 0,
  "total": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|appDetailReq|app详情表|body|true|app详情表|app详情表|
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;descr|api描述||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;name|api名称||false|string||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 修改数据源


**接口地址**:`/app-detail`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "countId": "",
  "current": 0,
  "descr": "",
  "id": "",
  "maxLimit": 0,
  "name": "",
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "records": [],
  "searchCount": true,
  "size": 0,
  "total": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|appDetailReq|app详情表|body|true|app详情表|app详情表|
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;descr|api描述||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;name|api名称||false|string||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id删除数据源


**接口地址**:`/app-detail`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据条件分页查询api数据源


**接口地址**:`/app-detail/queryByPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "countId": "",
  "current": 0,
  "descr": "",
  "id": "",
  "maxLimit": 0,
  "name": "",
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "records": [],
  "searchCount": true,
  "size": 0,
  "total": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|appDetailReq|app详情表|body|true|app详情表|app详情表|
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;descr|api描述||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;name|api名称||false|string||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«AppDetailBO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«AppDetailBO»|IPage«AppDetailBO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|AppDetailBO|
|&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;descr||string||
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"createBy": "",
				"createTime": "",
				"descr": "",
				"id": "",
				"name": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


# biz_data_life_job表管理


## 新增非变量任务


**接口地址**:`/api-biz-data-life-job`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "apiBizDataLifeValueMap": {},
  "apiId": "",
  "appId": "",
  "cron": "",
  "envId": "",
  "globalVarIds": "",
  "id": "",
  "lifeDataMapList": [
    {
      "conditionValue": "",
      "lifeDataId": ""
    }
  ],
  "lifeTemplateId": "",
  "name": "",
  "projectId": "",
  "remarkFieldJsonPath": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|bizDataLifeJobReq|biz_data_life_job表|body|true|biz_data_life_job表|biz_data_life_job表|
|&emsp;&emsp;apiBizDataLifeValueMap|业务数据key与生命体value字段内部的key映射（jsonpath）||false|object||
|&emsp;&emsp;apiId|api id||false|string||
|&emsp;&emsp;appId|app id||false|string||
|&emsp;&emsp;cron|cron表达式||false|string||
|&emsp;&emsp;envId|env id||false|string||
|&emsp;&emsp;globalVarIds|全局变量id，多个逗号分隔||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;lifeDataMapList|生命体数据实例映射||false|array|LifeDataMap|
|&emsp;&emsp;&emsp;&emsp;conditionValue|||false|string||
|&emsp;&emsp;&emsp;&emsp;lifeDataId|||false|string||
|&emsp;&emsp;lifeTemplateId|生命体模板id||false|string||
|&emsp;&emsp;name|任务名称||false|string||
|&emsp;&emsp;projectId|project id||false|string||
|&emsp;&emsp;remarkFieldJsonPath|备注字段jsonpath||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 修改非变量任务


**接口地址**:`/api-biz-data-life-job`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "apiBizDataLifeValueMap": {},
  "apiId": "",
  "appId": "",
  "cron": "",
  "envId": "",
  "globalVarIds": "",
  "id": "",
  "lifeDataMapList": [
    {
      "conditionValue": "",
      "lifeDataId": ""
    }
  ],
  "lifeTemplateId": "",
  "name": "",
  "projectId": "",
  "remarkFieldJsonPath": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|bizDataLifeJobReq|biz_data_life_job表|body|true|biz_data_life_job表|biz_data_life_job表|
|&emsp;&emsp;apiBizDataLifeValueMap|业务数据key与生命体value字段内部的key映射（jsonpath）||false|object||
|&emsp;&emsp;apiId|api id||false|string||
|&emsp;&emsp;appId|app id||false|string||
|&emsp;&emsp;cron|cron表达式||false|string||
|&emsp;&emsp;envId|env id||false|string||
|&emsp;&emsp;globalVarIds|全局变量id，多个逗号分隔||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;lifeDataMapList|生命体数据实例映射||false|array|LifeDataMap|
|&emsp;&emsp;&emsp;&emsp;conditionValue|||false|string||
|&emsp;&emsp;&emsp;&emsp;lifeDataId|||false|string||
|&emsp;&emsp;lifeTemplateId|生命体模板id||false|string||
|&emsp;&emsp;name|任务名称||false|string||
|&emsp;&emsp;projectId|project id||false|string||
|&emsp;&emsp;remarkFieldJsonPath|备注字段jsonpath||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id删除非变量任务


**接口地址**:`/api-biz-data-life-job`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id查询生命体映射定时任务


**接口地址**:`/api-biz-data-life-job/queryById`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 分页查询定时任务


**接口地址**:`/api-biz-data-life-job/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "appId": "",
  "envId": "",
  "jobName": "",
  "jobStatus": "",
  "jobType": "",
  "pageIndex": 0,
  "pageSize": 10
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|jobQueryReq|jobQueryReq|body|true|JobQueryReq|JobQueryReq|
|&emsp;&emsp;appId|数据源id||false|string||
|&emsp;&emsp;envId|环境id||false|string||
|&emsp;&emsp;jobName|任务名称||false|string||
|&emsp;&emsp;jobStatus|任务状态||false|string||
|&emsp;&emsp;jobType|任务类型||false|string||
|&emsp;&emsp;pageIndex|页码||false|integer(int32)||
|&emsp;&emsp;pageSize|每页条数||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«JobVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«JobVO»|IPage«JobVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|JobVO|
|&emsp;&emsp;&emsp;&emsp;api||string||
|&emsp;&emsp;&emsp;&emsp;cron||string||
|&emsp;&emsp;&emsp;&emsp;frequency||string||
|&emsp;&emsp;&emsp;&emsp;jobId||string||
|&emsp;&emsp;&emsp;&emsp;jobName||string||
|&emsp;&emsp;&emsp;&emsp;jobStatus||string||
|&emsp;&emsp;&emsp;&emsp;jobType||string||
|&emsp;&emsp;&emsp;&emsp;lastRunTime||string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"api": "",
				"cron": "",
				"frequency": "",
				"jobId": "",
				"jobName": "",
				"jobStatus": "",
				"jobType": "",
				"lastRunTime": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


# job-controller


## 删除job


**接口地址**:`/quartz/job/delete`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|jobGroup|jobGroup|query|true|string||
|jobId|jobId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 暂停job


**接口地址**:`/quartz/job/pause`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|jobGroup|jobGroup|query|true|string||
|jobId|jobId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 恢复job


**接口地址**:`/quartz/job/resume`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|jobGroup|jobGroup|query|true|string||
|jobId|jobId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 同步job


**接口地址**:`/quartz/job/sync`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|jobGroup|jobGroup|query|true|string||
|jobId|jobId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 更新job


**接口地址**:`/quartz/job/update`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|cronExpression|cronExpression|query|true|string||
|jobGroup|jobGroup|query|true|string||
|jobId|jobId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


# websocket-服务端


## 查询在线用户列表


**接口地址**:`/websocket/server/queryListOnlineUser`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«string»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": []
}
```


## 广播


**接口地址**:`/websocket/server/sendAll`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|message|消息|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 单播


**接口地址**:`/websocket/server/sendOne`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|message|消息|query|true|string||
|userId|用户id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


# 全局环境参数表管理


## 新增api环境全局参数


**接口地址**:`/api-env-global-param-field`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "apiEnvId": "",
  "globalType": "",
  "id": "",
  "paramDesc": "",
  "paramName": "",
  "paramType": "",
  "paramValue": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvGlobalParamFieldReq|全局环境参数表|body|true|全局环境参数表0|全局环境参数表0|
|&emsp;&emsp;apiEnvId|env id||false|string||
|&emsp;&emsp;globalType|全局类型（0请求头、1请求体）||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;paramDesc|参数注释||false|string||
|&emsp;&emsp;paramName|参数名称||false|string||
|&emsp;&emsp;paramType|参数类型（0常量、1变量）||false|string||
|&emsp;&emsp;paramValue|参数值||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 修改api环境全局参数


**接口地址**:`/api-env-global-param-field`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "apiEnvId": "",
  "globalType": "",
  "id": "",
  "paramDesc": "",
  "paramName": "",
  "paramType": "",
  "paramValue": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvGlobalParamFieldReq|全局环境参数表|body|true|全局环境参数表0|全局环境参数表0|
|&emsp;&emsp;apiEnvId|env id||false|string||
|&emsp;&emsp;globalType|全局类型（0请求头、1请求体）||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;paramDesc|参数注释||false|string||
|&emsp;&emsp;paramName|参数名称||false|string||
|&emsp;&emsp;paramType|参数类型（0常量、1变量）||false|string||
|&emsp;&emsp;paramValue|参数值||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id删除api环境全局参数


**接口地址**:`/api-env-global-param-field`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据条件查询api环境全局参数


**接口地址**:`/api-env-global-param-field/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "apiEnvId": "",
  "globalType": "",
  "id": "",
  "paramDesc": "",
  "paramName": "",
  "paramType": "",
  "paramValue": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvGlobalParamFieldReq|全局环境参数表|body|true|全局环境参数表0|全局环境参数表0|
|&emsp;&emsp;apiEnvId|env id||false|string||
|&emsp;&emsp;globalType|全局类型（0请求头、1请求体）||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;paramDesc|参数注释||false|string||
|&emsp;&emsp;paramName|参数名称||false|string||
|&emsp;&emsp;paramType|参数类型（0常量、1变量）||false|string||
|&emsp;&emsp;paramValue|参数值||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«全局环境参数表»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|全局环境参数表|
|&emsp;&emsp;apiEnvId|env id|string||
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;globalType|全局类型（0请求头、1请求体）|string||
|&emsp;&emsp;id|id|string||
|&emsp;&emsp;paramDesc|参数注释|string||
|&emsp;&emsp;paramName|参数名称|string||
|&emsp;&emsp;paramType|参数类型（0常量、1常量）|string||
|&emsp;&emsp;paramValue|参数值|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"apiEnvId": "",
			"createBy": "",
			"createTime": "",
			"globalType": "",
			"id": "",
			"paramDesc": "",
			"paramName": "",
			"paramType": "",
			"paramValue": "",
			"updateBy": "",
			"updateTime": ""
		}
	]
}
```


# 公共目录树V1.0 


## 2:新增目录


**接口地址**:`/systree/v1/add`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "directParentId": "",
  "id": "",
  "lockStatus": "",
  "model": 0,
  "name": "",
  "projectId": "",
  "sameLevelLastId": "",
  "showStatus": "",
  "status": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysTreeReq|sysTreeReq|body|true|SysTreeReq|SysTreeReq|
|&emsp;&emsp;businessId|业务id，没有的话传项目id||true|string||
|&emsp;&emsp;directParentId|直接上级ID,无上级可为空||false|string||
|&emsp;&emsp;id|||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;model|所属模块：1-关卡空间树  2-关卡通用树(关卡id隔离)||false|integer(int32)||
|&emsp;&emsp;name|匹配目录名，模糊搜索用||false|string||
|&emsp;&emsp;projectId|项目ID||false|string||
|&emsp;&emsp;sameLevelLastId|同级目录上一个ID,如果默认放到最后，可为空||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;status|保留字段，状态（0正常 1停用 ）||false|string||
|&emsp;&emsp;type|类型：0-系统初始化 1-自定义||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysTreeRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysTreeRes|SysTreeRes|
|&emsp;&emsp;ancestorChainPathIds|祖链路径IDS|string||
|&emsp;&emsp;ancestorChainPathNames|祖链路径NAMES|string||
|&emsp;&emsp;children|仅 getType=search 时，才会有叶子数据 |IPage«SysTreeDrillVO»|IPage«SysTreeDrillVO»|
|&emsp;&emsp;&emsp;&emsp;current||integer||
|&emsp;&emsp;&emsp;&emsp;pages||integer||
|&emsp;&emsp;&emsp;&emsp;records||array|SysTreeDrillVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirId|节点ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirPath|祖籍路径|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lifeCount|集合下生命体数量|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lockStatus|是否上锁|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;model|所属模块：   2-关卡树(关卡id隔离)|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name|业务名称|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;sortIndex|排序索引|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;value|value|object||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workId|业务ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workType|业务节点分类|string||
|&emsp;&emsp;&emsp;&emsp;size||integer||
|&emsp;&emsp;&emsp;&emsp;total||integer||
|&emsp;&emsp;childrenDir|目录节点|array|SysTreeRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;directParentId|直接父级目录ID|string||
|&emsp;&emsp;directParentName|直接父级目录名称|string||
|&emsp;&emsp;directSubDirCount|直接子目录个数|integer(int64)||
|&emsp;&emsp;directSubDirIds|直接子目录ID|string||
|&emsp;&emsp;directSubDirNames|直接子目录名|string||
|&emsp;&emsp;getType|search or drill  默认drill|string||
|&emsp;&emsp;id||string||
|&emsp;&emsp;leafAllCount||integer(int64)||
|&emsp;&emsp;leafCount|直接叶子节点个数 [具体业务-任务]|integer(int64)||
|&emsp;&emsp;level|层级|integer(int32)||
|&emsp;&emsp;lft|左值|integer(int64)||
|&emsp;&emsp;lockStatus|锁定状态(0不锁定 1锁定)|string||
|&emsp;&emsp;model|所属模块：  2-关卡树(关卡id隔离)|integer(int32)||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;rgt|右值|integer(int64)||
|&emsp;&emsp;searchLeafAllCount|检索出的下属集合所有叶子节点个数|integer(int64)||
|&emsp;&emsp;searchLeafCount|检索出的直接叶子节点个数|integer(int64)||
|&emsp;&emsp;seq|顺序|integer(int32)||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏）|string||
|&emsp;&emsp;status|状态（0正常 1停用）|string||
|&emsp;&emsp;subDirBool|是否是叶子目录 0-否 1-是|integer(int32)||
|&emsp;&emsp;subDirCount|全部子目录个数|integer(int64)||
|&emsp;&emsp;target|目录搜索|boolean||
|&emsp;&emsp;type|类型：0-系统初始化 1-自定义|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"ancestorChainPathIds": "",
		"ancestorChainPathNames": "",
		"children": {
			"current": 0,
			"pages": 0,
			"records": [
				{
					"dirId": "",
					"dirPath": "",
					"lifeCount": 0,
					"lockStatus": "",
					"model": 0,
					"name": "",
					"projectId": "",
					"remark": "",
					"showStatus": "",
					"sortIndex": 0,
					"value": {},
					"workId": "",
					"workType": ""
				}
			],
			"size": 0,
			"total": 0
		},
		"childrenDir": [
			{}
		],
		"createBy": "",
		"createTime": "",
		"directParentId": "",
		"directParentName": "",
		"directSubDirCount": 0,
		"directSubDirIds": "",
		"directSubDirNames": "",
		"getType": "",
		"id": "",
		"leafAllCount": 0,
		"leafCount": 0,
		"level": 0,
		"lft": 0,
		"lockStatus": "",
		"model": 0,
		"name": "",
		"projectId": "",
		"remark": "",
		"rgt": 0,
		"searchLeafAllCount": 0,
		"searchLeafCount": 0,
		"seq": 0,
		"showStatus": "",
		"status": "",
		"subDirBool": 0,
		"subDirCount": 0,
		"target": true,
		"type": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 6:下移


**接口地址**:`/systree/v1/down`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 7:下钻业务，统一查询入口


**接口地址**:`/systree/v1/drill`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "businessPageId": "",
  "countId": "",
  "current": 0,
  "directParentId": "",
  "labelsModel": "",
  "maxLimit": 0,
  "model": 0,
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "passId": "",
  "projectId": "",
  "records": [],
  "searchCount": true,
  "size": 0,
  "total": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysTreeDrillReq|sysTreeDrillReq|body|true|SysTreeDrillReq|SysTreeDrillReq|
|&emsp;&emsp;businessId|租户空间ID||false|string||
|&emsp;&emsp;businessPageId|业务页面ID||false|string||
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;directParentId|直接上级ID||false|string||
|&emsp;&emsp;labelsModel|资产标签分模块 (1/标签管理-我的管理 2/数据资产-标签资产 3/我的标签-我申请的 4/我的标签-我收藏的) 5/标签管理-实体对象||false|string||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;model|所属模块：   2-关卡树(关卡id隔离)||false|integer(int32)||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;passId|关卡ID||false|string||
|&emsp;&emsp;projectId|项目ID||false|string||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«SysTreeDrillVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«SysTreeDrillVO»|IPage«SysTreeDrillVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SysTreeDrillVO|
|&emsp;&emsp;&emsp;&emsp;dirId|节点ID|string||
|&emsp;&emsp;&emsp;&emsp;dirPath|祖籍路径|string||
|&emsp;&emsp;&emsp;&emsp;lifeCount|集合下生命体数量|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|是否上锁|string||
|&emsp;&emsp;&emsp;&emsp;model|所属模块：   2-关卡树(关卡id隔离)|integer||
|&emsp;&emsp;&emsp;&emsp;name|业务名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;sortIndex|排序索引|integer||
|&emsp;&emsp;&emsp;&emsp;value|value|object||
|&emsp;&emsp;&emsp;&emsp;workId|业务ID|string||
|&emsp;&emsp;&emsp;&emsp;workType|业务节点分类|string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"dirId": "",
				"dirPath": "",
				"lifeCount": 0,
				"lockStatus": "",
				"model": 0,
				"name": "",
				"projectId": "",
				"remark": "",
				"showStatus": "",
				"sortIndex": 0,
				"value": {},
				"workId": "",
				"workType": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 11:下钻业务，统一查询入口,节点名称模糊查询


**接口地址**:`/systree/v1/drill/plus`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "businessPageId": "",
  "countId": "",
  "current": 0,
  "directParentId": "",
  "labelsModel": "",
  "maxLimit": 0,
  "model": 0,
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "passId": "",
  "projectId": "",
  "records": [],
  "searchCount": true,
  "size": 0,
  "total": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysTreeDrillReq|sysTreeDrillReq|body|true|SysTreeDrillReq|SysTreeDrillReq|
|&emsp;&emsp;businessId|租户空间ID||false|string||
|&emsp;&emsp;businessPageId|业务页面ID||false|string||
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;directParentId|直接上级ID||false|string||
|&emsp;&emsp;labelsModel|资产标签分模块 (1/标签管理-我的管理 2/数据资产-标签资产 3/我的标签-我申请的 4/我的标签-我收藏的) 5/标签管理-实体对象||false|string||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;model|所属模块：   2-关卡树(关卡id隔离)||false|integer(int32)||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;passId|关卡ID||false|string||
|&emsp;&emsp;projectId|项目ID||false|string||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||
|nodeName|nodeName|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«SysTreeDrillVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«SysTreeDrillVO»|IPage«SysTreeDrillVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SysTreeDrillVO|
|&emsp;&emsp;&emsp;&emsp;dirId|节点ID|string||
|&emsp;&emsp;&emsp;&emsp;dirPath|祖籍路径|string||
|&emsp;&emsp;&emsp;&emsp;lifeCount|集合下生命体数量|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|是否上锁|string||
|&emsp;&emsp;&emsp;&emsp;model|所属模块：   2-关卡树(关卡id隔离)|integer||
|&emsp;&emsp;&emsp;&emsp;name|业务名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;sortIndex|排序索引|integer||
|&emsp;&emsp;&emsp;&emsp;value|value|object||
|&emsp;&emsp;&emsp;&emsp;workId|业务ID|string||
|&emsp;&emsp;&emsp;&emsp;workType|业务节点分类|string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"dirId": "",
				"dirPath": "",
				"lifeCount": 0,
				"lockStatus": "",
				"model": 0,
				"name": "",
				"projectId": "",
				"remark": "",
				"showStatus": "",
				"sortIndex": 0,
				"value": {},
				"workId": "",
				"workType": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 8:移动叶子


**接口地址**:`/systree/v1/move`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "afterDirId": "",
  "afterDirPath": "",
  "afterSortIndex": 0,
  "afterWorkId": "",
  "model": 0,
  "preDirId": "",
  "preDirectParentId": "",
  "preSortIndex": 0,
  "preWorkId": "",
  "projectId": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysTreeMoveReq|sysTreeMoveReq|body|true|SysTreeMoveReq|SysTreeMoveReq|
|&emsp;&emsp;afterDirId|移动后节点ID||false|string||
|&emsp;&emsp;afterDirPath|移动后祖籍路径||false|string||
|&emsp;&emsp;afterSortIndex|移动后业务下标||false|integer(int32)||
|&emsp;&emsp;afterWorkId|移动后业务ID||false|string||
|&emsp;&emsp;model|||true|integer(int32)||
|&emsp;&emsp;preDirId|移动前节点ID||false|string||
|&emsp;&emsp;preDirectParentId|移动前直接上级目录ID||false|string||
|&emsp;&emsp;preSortIndex|移动前业务下标||false|integer(int32)||
|&emsp;&emsp;preWorkId|移动前业务ID||false|string||
|&emsp;&emsp;projectId|||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 目录节点移动


**接口地址**:`/systree/v1/moveDirNode`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "dirTargetId": "",
  "id": "",
  "model": 0,
  "moveStep": 0,
  "moveType": 0,
  "projectId": "",
  "targetDirSeq": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sameLevelMoveReq|同级移动目录树入参|body|true|SameLevelMoveReq|SameLevelMoveReq|
|&emsp;&emsp;businessId|业务关联id||false|string||
|&emsp;&emsp;dirTargetId|移动目标的父节点id||false|string||
|&emsp;&emsp;id|目录树id||false|string||
|&emsp;&emsp;model|所属模块： 1-文件夹类(项目id隔离) 2-关卡树(关卡id隔离)||false|integer(int32)||
|&emsp;&emsp;moveStep|移动步数||false|integer(int32)||
|&emsp;&emsp;moveType|移动类型 0:向上移动 1:向下移动过 2:跨级移动||false|integer(int32)||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;targetDirSeq|移动目标的父节点下的位次seq||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«string»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": ""
}
```


## 1:获取目录树plus


**接口地址**:`/systree/v1/newbieTree`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "directParentId": "",
  "id": "",
  "lockStatus": "",
  "model": 0,
  "name": "",
  "projectId": "",
  "sameLevelLastId": "",
  "showStatus": "",
  "status": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysTreeReq|sysTreeReq|body|true|SysTreeReq|SysTreeReq|
|&emsp;&emsp;businessId|业务id，没有的话传项目id||true|string||
|&emsp;&emsp;directParentId|直接上级ID,无上级可为空||false|string||
|&emsp;&emsp;id|||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;model|所属模块：1-关卡空间树  2-关卡通用树(关卡id隔离)||false|integer(int32)||
|&emsp;&emsp;name|匹配目录名，模糊搜索用||false|string||
|&emsp;&emsp;projectId|项目ID||false|string||
|&emsp;&emsp;sameLevelLastId|同级目录上一个ID,如果默认放到最后，可为空||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;status|保留字段，状态（0正常 1停用 ）||false|string||
|&emsp;&emsp;type|类型：0-系统初始化 1-自定义||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«SysTreeRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|SysTreeRes|
|&emsp;&emsp;ancestorChainPathIds|祖链路径IDS|string||
|&emsp;&emsp;ancestorChainPathNames|祖链路径NAMES|string||
|&emsp;&emsp;children|仅 getType=search 时，才会有叶子数据 |IPage«SysTreeDrillVO»|IPage«SysTreeDrillVO»|
|&emsp;&emsp;&emsp;&emsp;current||integer||
|&emsp;&emsp;&emsp;&emsp;pages||integer||
|&emsp;&emsp;&emsp;&emsp;records||array|SysTreeDrillVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirId|节点ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirPath|祖籍路径|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lifeCount|集合下生命体数量|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lockStatus|是否上锁|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;model|所属模块：   2-关卡树(关卡id隔离)|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name|业务名称|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;sortIndex|排序索引|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;value|value|object||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workId|业务ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workType|业务节点分类|string||
|&emsp;&emsp;&emsp;&emsp;size||integer||
|&emsp;&emsp;&emsp;&emsp;total||integer||
|&emsp;&emsp;childrenDir|目录节点|array|SysTreeRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;directParentId|直接父级目录ID|string||
|&emsp;&emsp;directParentName|直接父级目录名称|string||
|&emsp;&emsp;directSubDirCount|直接子目录个数|integer(int64)||
|&emsp;&emsp;directSubDirIds|直接子目录ID|string||
|&emsp;&emsp;directSubDirNames|直接子目录名|string||
|&emsp;&emsp;getType|search or drill  默认drill|string||
|&emsp;&emsp;id||string||
|&emsp;&emsp;leafAllCount||integer(int64)||
|&emsp;&emsp;leafCount|直接叶子节点个数 [具体业务-任务]|integer(int64)||
|&emsp;&emsp;level|层级|integer(int32)||
|&emsp;&emsp;lft|左值|integer(int64)||
|&emsp;&emsp;lockStatus|锁定状态(0不锁定 1锁定)|string||
|&emsp;&emsp;model|所属模块：  2-关卡树(关卡id隔离)|integer(int32)||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;rgt|右值|integer(int64)||
|&emsp;&emsp;searchLeafAllCount|检索出的下属集合所有叶子节点个数|integer(int64)||
|&emsp;&emsp;searchLeafCount|检索出的直接叶子节点个数|integer(int64)||
|&emsp;&emsp;seq|顺序|integer(int32)||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏）|string||
|&emsp;&emsp;status|状态（0正常 1停用）|string||
|&emsp;&emsp;subDirBool|是否是叶子目录 0-否 1-是|integer(int32)||
|&emsp;&emsp;subDirCount|全部子目录个数|integer(int64)||
|&emsp;&emsp;target|目录搜索|boolean||
|&emsp;&emsp;type|类型：0-系统初始化 1-自定义|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"ancestorChainPathIds": "",
			"ancestorChainPathNames": "",
			"children": {
				"current": 0,
				"pages": 0,
				"records": [
					{
						"dirId": "",
						"dirPath": "",
						"lifeCount": 0,
						"lockStatus": "",
						"model": 0,
						"name": "",
						"projectId": "",
						"remark": "",
						"showStatus": "",
						"sortIndex": 0,
						"value": {},
						"workId": "",
						"workType": ""
					}
				],
				"size": 0,
				"total": 0
			},
			"childrenDir": [
				{}
			],
			"createBy": "",
			"createTime": "",
			"directParentId": "",
			"directParentName": "",
			"directSubDirCount": 0,
			"directSubDirIds": "",
			"directSubDirNames": "",
			"getType": "",
			"id": "",
			"leafAllCount": 0,
			"leafCount": 0,
			"level": 0,
			"lft": 0,
			"lockStatus": "",
			"model": 0,
			"name": "",
			"projectId": "",
			"remark": "",
			"rgt": 0,
			"searchLeafAllCount": 0,
			"searchLeafCount": 0,
			"seq": 0,
			"showStatus": "",
			"status": "",
			"subDirBool": 0,
			"subDirCount": 0,
			"target": true,
			"type": "",
			"updateBy": "",
			"updateTime": ""
		}
	]
}
```


## 4:删除目录


**接口地址**:`/systree/v1/remove`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 9:检索


**接口地址**:`/systree/v1/search`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "keywords": "",
  "limit": 0,
  "model": 0,
  "projectId": "",
  "searchType": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|queryTreeLeafReq|queryTreeLeafReq|body|true|QueryTreeLeafReq|QueryTreeLeafReq|
|&emsp;&emsp;businessId|业务ID||false|string||
|&emsp;&emsp;keywords|检索关键字||false|string||
|&emsp;&emsp;limit|限制个数，默认不限||false|integer(int32)||
|&emsp;&emsp;model|||true|integer(int32)||
|&emsp;&emsp;projectId|项目ID||false|string||
|&emsp;&emsp;searchType|检索类型  1-目录节点 2-目录节点+业务节点 ||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«SysTreeRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|SysTreeRes|
|&emsp;&emsp;ancestorChainPathIds|祖链路径IDS|string||
|&emsp;&emsp;ancestorChainPathNames|祖链路径NAMES|string||
|&emsp;&emsp;children|仅 getType=search 时，才会有叶子数据 |IPage«SysTreeDrillVO»|IPage«SysTreeDrillVO»|
|&emsp;&emsp;&emsp;&emsp;current||integer||
|&emsp;&emsp;&emsp;&emsp;pages||integer||
|&emsp;&emsp;&emsp;&emsp;records||array|SysTreeDrillVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirId|节点ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirPath|祖籍路径|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lifeCount|集合下生命体数量|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lockStatus|是否上锁|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;model|所属模块：   2-关卡树(关卡id隔离)|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name|业务名称|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;sortIndex|排序索引|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;value|value|object||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workId|业务ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workType|业务节点分类|string||
|&emsp;&emsp;&emsp;&emsp;size||integer||
|&emsp;&emsp;&emsp;&emsp;total||integer||
|&emsp;&emsp;childrenDir|目录节点|array|SysTreeRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;directParentId|直接父级目录ID|string||
|&emsp;&emsp;directParentName|直接父级目录名称|string||
|&emsp;&emsp;directSubDirCount|直接子目录个数|integer(int64)||
|&emsp;&emsp;directSubDirIds|直接子目录ID|string||
|&emsp;&emsp;directSubDirNames|直接子目录名|string||
|&emsp;&emsp;getType|search or drill  默认drill|string||
|&emsp;&emsp;id||string||
|&emsp;&emsp;leafAllCount||integer(int64)||
|&emsp;&emsp;leafCount|直接叶子节点个数 [具体业务-任务]|integer(int64)||
|&emsp;&emsp;level|层级|integer(int32)||
|&emsp;&emsp;lft|左值|integer(int64)||
|&emsp;&emsp;lockStatus|锁定状态(0不锁定 1锁定)|string||
|&emsp;&emsp;model|所属模块：  2-关卡树(关卡id隔离)|integer(int32)||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;rgt|右值|integer(int64)||
|&emsp;&emsp;searchLeafAllCount|检索出的下属集合所有叶子节点个数|integer(int64)||
|&emsp;&emsp;searchLeafCount|检索出的直接叶子节点个数|integer(int64)||
|&emsp;&emsp;seq|顺序|integer(int32)||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏）|string||
|&emsp;&emsp;status|状态（0正常 1停用）|string||
|&emsp;&emsp;subDirBool|是否是叶子目录 0-否 1-是|integer(int32)||
|&emsp;&emsp;subDirCount|全部子目录个数|integer(int64)||
|&emsp;&emsp;target|目录搜索|boolean||
|&emsp;&emsp;type|类型：0-系统初始化 1-自定义|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"ancestorChainPathIds": "",
			"ancestorChainPathNames": "",
			"children": {
				"current": 0,
				"pages": 0,
				"records": [
					{
						"dirId": "",
						"dirPath": "",
						"lifeCount": 0,
						"lockStatus": "",
						"model": 0,
						"name": "",
						"projectId": "",
						"remark": "",
						"showStatus": "",
						"sortIndex": 0,
						"value": {},
						"workId": "",
						"workType": ""
					}
				],
				"size": 0,
				"total": 0
			},
			"childrenDir": [
				{}
			],
			"createBy": "",
			"createTime": "",
			"directParentId": "",
			"directParentName": "",
			"directSubDirCount": 0,
			"directSubDirIds": "",
			"directSubDirNames": "",
			"getType": "",
			"id": "",
			"leafAllCount": 0,
			"leafCount": 0,
			"level": 0,
			"lft": 0,
			"lockStatus": "",
			"model": 0,
			"name": "",
			"projectId": "",
			"remark": "",
			"rgt": 0,
			"searchLeafAllCount": 0,
			"searchLeafCount": 0,
			"seq": 0,
			"showStatus": "",
			"status": "",
			"subDirBool": 0,
			"subDirCount": 0,
			"target": true,
			"type": "",
			"updateBy": "",
			"updateTime": ""
		}
	]
}
```


## 10:检索叶子


**接口地址**:`/systree/v1/searchLeaf`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "keywords": "",
  "limit": 0,
  "model": 0,
  "projectId": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|searchLeafReq|searchLeafReq|body|true|检索叶子|检索叶子|
|&emsp;&emsp;businessId|业务ID||false|string||
|&emsp;&emsp;keywords|检索关键字||false|string||
|&emsp;&emsp;limit|限制个数，默认不限||false|integer(int32)||
|&emsp;&emsp;model|||true|integer(int32)||
|&emsp;&emsp;projectId|项目ID||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«SysTreeRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|SysTreeRes|
|&emsp;&emsp;ancestorChainPathIds|祖链路径IDS|string||
|&emsp;&emsp;ancestorChainPathNames|祖链路径NAMES|string||
|&emsp;&emsp;children|仅 getType=search 时，才会有叶子数据 |IPage«SysTreeDrillVO»|IPage«SysTreeDrillVO»|
|&emsp;&emsp;&emsp;&emsp;current||integer||
|&emsp;&emsp;&emsp;&emsp;pages||integer||
|&emsp;&emsp;&emsp;&emsp;records||array|SysTreeDrillVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirId|节点ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirPath|祖籍路径|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lifeCount|集合下生命体数量|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lockStatus|是否上锁|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;model|所属模块：   2-关卡树(关卡id隔离)|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name|业务名称|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;sortIndex|排序索引|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;value|value|object||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workId|业务ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workType|业务节点分类|string||
|&emsp;&emsp;&emsp;&emsp;size||integer||
|&emsp;&emsp;&emsp;&emsp;total||integer||
|&emsp;&emsp;childrenDir|目录节点|array|SysTreeRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;directParentId|直接父级目录ID|string||
|&emsp;&emsp;directParentName|直接父级目录名称|string||
|&emsp;&emsp;directSubDirCount|直接子目录个数|integer(int64)||
|&emsp;&emsp;directSubDirIds|直接子目录ID|string||
|&emsp;&emsp;directSubDirNames|直接子目录名|string||
|&emsp;&emsp;getType|search or drill  默认drill|string||
|&emsp;&emsp;id||string||
|&emsp;&emsp;leafAllCount||integer(int64)||
|&emsp;&emsp;leafCount|直接叶子节点个数 [具体业务-任务]|integer(int64)||
|&emsp;&emsp;level|层级|integer(int32)||
|&emsp;&emsp;lft|左值|integer(int64)||
|&emsp;&emsp;lockStatus|锁定状态(0不锁定 1锁定)|string||
|&emsp;&emsp;model|所属模块：  2-关卡树(关卡id隔离)|integer(int32)||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;rgt|右值|integer(int64)||
|&emsp;&emsp;searchLeafAllCount|检索出的下属集合所有叶子节点个数|integer(int64)||
|&emsp;&emsp;searchLeafCount|检索出的直接叶子节点个数|integer(int64)||
|&emsp;&emsp;seq|顺序|integer(int32)||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏）|string||
|&emsp;&emsp;status|状态（0正常 1停用）|string||
|&emsp;&emsp;subDirBool|是否是叶子目录 0-否 1-是|integer(int32)||
|&emsp;&emsp;subDirCount|全部子目录个数|integer(int64)||
|&emsp;&emsp;target|目录搜索|boolean||
|&emsp;&emsp;type|类型：0-系统初始化 1-自定义|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"ancestorChainPathIds": "",
			"ancestorChainPathNames": "",
			"children": {
				"current": 0,
				"pages": 0,
				"records": [
					{
						"dirId": "",
						"dirPath": "",
						"lifeCount": 0,
						"lockStatus": "",
						"model": 0,
						"name": "",
						"projectId": "",
						"remark": "",
						"showStatus": "",
						"sortIndex": 0,
						"value": {},
						"workId": "",
						"workType": ""
					}
				],
				"size": 0,
				"total": 0
			},
			"childrenDir": [
				{}
			],
			"createBy": "",
			"createTime": "",
			"directParentId": "",
			"directParentName": "",
			"directSubDirCount": 0,
			"directSubDirIds": "",
			"directSubDirNames": "",
			"getType": "",
			"id": "",
			"leafAllCount": 0,
			"leafCount": 0,
			"level": 0,
			"lft": 0,
			"lockStatus": "",
			"model": 0,
			"name": "",
			"projectId": "",
			"remark": "",
			"rgt": 0,
			"searchLeafAllCount": 0,
			"searchLeafCount": 0,
			"seq": 0,
			"showStatus": "",
			"status": "",
			"subDirBool": 0,
			"subDirCount": 0,
			"target": true,
			"type": "",
			"updateBy": "",
			"updateTime": ""
		}
	]
}
```


## 1:获取目录树


**接口地址**:`/systree/v1/tree`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "directParentId": "",
  "id": "",
  "lockStatus": "",
  "model": 0,
  "name": "",
  "projectId": "",
  "sameLevelLastId": "",
  "showStatus": "",
  "status": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysTreeReq|sysTreeReq|body|true|SysTreeReq|SysTreeReq|
|&emsp;&emsp;businessId|业务id，没有的话传项目id||true|string||
|&emsp;&emsp;directParentId|直接上级ID,无上级可为空||false|string||
|&emsp;&emsp;id|||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;model|所属模块：1-关卡空间树  2-关卡通用树(关卡id隔离)||false|integer(int32)||
|&emsp;&emsp;name|匹配目录名，模糊搜索用||false|string||
|&emsp;&emsp;projectId|项目ID||false|string||
|&emsp;&emsp;sameLevelLastId|同级目录上一个ID,如果默认放到最后，可为空||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;status|保留字段，状态（0正常 1停用 ）||false|string||
|&emsp;&emsp;type|类型：0-系统初始化 1-自定义||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«SysTreeRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|SysTreeRes|
|&emsp;&emsp;ancestorChainPathIds|祖链路径IDS|string||
|&emsp;&emsp;ancestorChainPathNames|祖链路径NAMES|string||
|&emsp;&emsp;children|仅 getType=search 时，才会有叶子数据 |IPage«SysTreeDrillVO»|IPage«SysTreeDrillVO»|
|&emsp;&emsp;&emsp;&emsp;current||integer||
|&emsp;&emsp;&emsp;&emsp;pages||integer||
|&emsp;&emsp;&emsp;&emsp;records||array|SysTreeDrillVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirId|节点ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirPath|祖籍路径|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lifeCount|集合下生命体数量|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lockStatus|是否上锁|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;model|所属模块：   2-关卡树(关卡id隔离)|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name|业务名称|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;sortIndex|排序索引|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;value|value|object||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workId|业务ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workType|业务节点分类|string||
|&emsp;&emsp;&emsp;&emsp;size||integer||
|&emsp;&emsp;&emsp;&emsp;total||integer||
|&emsp;&emsp;childrenDir|目录节点|array|SysTreeRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;directParentId|直接父级目录ID|string||
|&emsp;&emsp;directParentName|直接父级目录名称|string||
|&emsp;&emsp;directSubDirCount|直接子目录个数|integer(int64)||
|&emsp;&emsp;directSubDirIds|直接子目录ID|string||
|&emsp;&emsp;directSubDirNames|直接子目录名|string||
|&emsp;&emsp;getType|search or drill  默认drill|string||
|&emsp;&emsp;id||string||
|&emsp;&emsp;leafAllCount||integer(int64)||
|&emsp;&emsp;leafCount|直接叶子节点个数 [具体业务-任务]|integer(int64)||
|&emsp;&emsp;level|层级|integer(int32)||
|&emsp;&emsp;lft|左值|integer(int64)||
|&emsp;&emsp;lockStatus|锁定状态(0不锁定 1锁定)|string||
|&emsp;&emsp;model|所属模块：  2-关卡树(关卡id隔离)|integer(int32)||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;remark|描述|string||
|&emsp;&emsp;rgt|右值|integer(int64)||
|&emsp;&emsp;searchLeafAllCount|检索出的下属集合所有叶子节点个数|integer(int64)||
|&emsp;&emsp;searchLeafCount|检索出的直接叶子节点个数|integer(int64)||
|&emsp;&emsp;seq|顺序|integer(int32)||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏）|string||
|&emsp;&emsp;status|状态（0正常 1停用）|string||
|&emsp;&emsp;subDirBool|是否是叶子目录 0-否 1-是|integer(int32)||
|&emsp;&emsp;subDirCount|全部子目录个数|integer(int64)||
|&emsp;&emsp;target|目录搜索|boolean||
|&emsp;&emsp;type|类型：0-系统初始化 1-自定义|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"ancestorChainPathIds": "",
			"ancestorChainPathNames": "",
			"children": {
				"current": 0,
				"pages": 0,
				"records": [
					{
						"dirId": "",
						"dirPath": "",
						"lifeCount": 0,
						"lockStatus": "",
						"model": 0,
						"name": "",
						"projectId": "",
						"remark": "",
						"showStatus": "",
						"sortIndex": 0,
						"value": {},
						"workId": "",
						"workType": ""
					}
				],
				"size": 0,
				"total": 0
			},
			"childrenDir": [
				{}
			],
			"createBy": "",
			"createTime": "",
			"directParentId": "",
			"directParentName": "",
			"directSubDirCount": 0,
			"directSubDirIds": "",
			"directSubDirNames": "",
			"getType": "",
			"id": "",
			"leafAllCount": 0,
			"leafCount": 0,
			"level": 0,
			"lft": 0,
			"lockStatus": "",
			"model": 0,
			"name": "",
			"projectId": "",
			"remark": "",
			"rgt": 0,
			"searchLeafAllCount": 0,
			"searchLeafCount": 0,
			"seq": 0,
			"showStatus": "",
			"status": "",
			"subDirBool": 0,
			"subDirCount": 0,
			"target": true,
			"type": "",
			"updateBy": "",
			"updateTime": ""
		}
	]
}
```


## 5:上移


**接口地址**:`/systree/v1/up`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 3:修改目录名称,状态


**接口地址**:`/systree/v1/update`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "directParentId": "",
  "id": "",
  "lockStatus": "",
  "model": 0,
  "name": "",
  "projectId": "",
  "sameLevelLastId": "",
  "showStatus": "",
  "status": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysTreeReq|sysTreeReq|body|true|SysTreeReq|SysTreeReq|
|&emsp;&emsp;businessId|业务id，没有的话传项目id||true|string||
|&emsp;&emsp;directParentId|直接上级ID,无上级可为空||false|string||
|&emsp;&emsp;id|||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;model|所属模块：1-关卡空间树  2-关卡通用树(关卡id隔离)||false|integer(int32)||
|&emsp;&emsp;name|匹配目录名，模糊搜索用||false|string||
|&emsp;&emsp;projectId|项目ID||false|string||
|&emsp;&emsp;sameLevelLastId|同级目录上一个ID,如果默认放到最后，可为空||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;status|保留字段，状态（0正常 1停用 ）||false|string||
|&emsp;&emsp;type|类型：0-系统初始化 1-自定义||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


# 关卡


## 新增单条数据,内部新增默认关卡树


**接口地址**:`/level`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": "",
  "projectId": "",
  "remark": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|levelQuery|关卡请求体|body|true|LevelReq|LevelReq|
|&emsp;&emsp;id|||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;remark|标记||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 通过主键id修改单条数据


**接口地址**:`/level`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": "",
  "projectId": "",
  "remark": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|levelQuery|关卡请求体|body|true|LevelReq|LevelReq|
|&emsp;&emsp;id|||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;remark|标记||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 分页查询数据


**接口地址**:`/level/page/{pageNum}/{pageSize}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pageNum|当前页|path|true|integer(int32)||
|pageSize|每页条数|path|true|integer(int32)||
|createBy|创建者|query|false|string||
|createTime|创建时间|query|false|string(date-time)||
|delFlag|删除标志 （0代表存在 1代表删除）|query|false|string||
|id||query|false|string||
|name|名称|query|false|string||
|projectId|项目id|query|false|string||
|remark|标记|query|false|string||
|updateBy|更新者|query|false|string||
|updateTime|更新时间|query|false|string(date-time)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«LevelVO»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«LevelVO»|IPage«LevelVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|LevelVO|
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;remark|标记|string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"id": "",
				"name": "",
				"projectId": "",
				"remark": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 通过id主键查询单条数据


**接口地址**:`/level/{id}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id主键|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«LevelVO»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||LevelVO|LevelVO|
|&emsp;&emsp;id||string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;remark|标记|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"id": "",
		"name": "",
		"projectId": "",
		"remark": ""
	}
}
```


## 通过id主键删除单条数据


**接口地址**:`/level/{id}`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id主键|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


# 字典管理-数据


## 5:修改字典数据


**接口地址**:`/dict/data`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "delFlag": "",
  "id": 0,
  "label": "",
  "parentId": 0,
  "remark": "",
  "sort": 0,
  "type": "",
  "value": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDictDataReq|sysDictDataReq|body|true|SysDictDataReq|SysDictDataReq|
|&emsp;&emsp;delFlag|||false|string||
|&emsp;&emsp;id|||false|integer(int64)||
|&emsp;&emsp;label|||false|string||
|&emsp;&emsp;parentId|||false|integer(int64)||
|&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;sort|||false|integer(int32)||
|&emsp;&emsp;type|||false|string||
|&emsp;&emsp;value|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 6:删除字典数据(批量删除，IDs逗号分割)


**接口地址**:`/dict/data`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|ids|ids|body|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 10：字典批量提交


**接口地址**:`/dict/data/batchSubmit`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "dataType": "",
  "parentId": 0,
  "sysDictDataList": [
    {
      "createBy": "",
      "createTime": "",
      "dataType": "",
      "delFlag": "",
      "id": 0,
      "label": "",
      "parentId": 0,
      "remark": "",
      "sort": 0,
      "type": "",
      "updateBy": "",
      "updateTime": "",
      "value": ""
    }
  ],
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDictDataSubmitReq|字典批量提交req|body|true|SysDictDataSubmitReq|SysDictDataSubmitReq|
|&emsp;&emsp;dataType|数据类型 0:列表 1:树形||false|string||
|&emsp;&emsp;parentId|父节点id||false|integer(int64)||
|&emsp;&emsp;sysDictDataList|字典列表数据||false|array|SysDictDataBO|
|&emsp;&emsp;&emsp;&emsp;createBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;createTime|||false|string||
|&emsp;&emsp;&emsp;&emsp;dataType|||false|string||
|&emsp;&emsp;&emsp;&emsp;delFlag|||false|string||
|&emsp;&emsp;&emsp;&emsp;id|||false|integer||
|&emsp;&emsp;&emsp;&emsp;label|||false|string||
|&emsp;&emsp;&emsp;&emsp;parentId|||false|integer||
|&emsp;&emsp;&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;&emsp;&emsp;sort|||false|integer||
|&emsp;&emsp;&emsp;&emsp;type|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|||false|string||
|&emsp;&emsp;&emsp;&emsp;value|||false|string||
|&emsp;&emsp;type|字典类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 1：新增字典数据


**接口地址**:`/dict/data/insert`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "delFlag": "",
  "id": 0,
  "label": "",
  "parentId": 0,
  "remark": "",
  "sort": 0,
  "type": "",
  "value": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDictDataReq|系统-字典数据表|body|true|SysDictDataSaveReq|SysDictDataSaveReq|
|&emsp;&emsp;delFlag|状态（0正常 1停用）||false|string||
|&emsp;&emsp;id|字典编码||false|integer(int64)||
|&emsp;&emsp;label|字典标签||false|string||
|&emsp;&emsp;parentId|父级id||false|integer(int64)||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;sort|字典排序||false|integer(int32)||
|&emsp;&emsp;type|字典类型||false|string||
|&emsp;&emsp;value|字典键值||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 2：根据条件批量查询字典数据(条件：Code、Type、Status、Label)


**接口地址**:`/dict/data/list`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "createBy": "",
  "createTime": "",
  "dataType": "",
  "delFlag": "",
  "id": 0,
  "label": "",
  "parentId": 0,
  "remark": "",
  "sort": 0,
  "type": "",
  "updateBy": "",
  "updateTime": "",
  "value": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDictDataBO|sysDictDataBO|body|true|SysDictDataBO|SysDictDataBO|
|&emsp;&emsp;createBy|||false|string||
|&emsp;&emsp;createTime|||false|string(date-time)||
|&emsp;&emsp;dataType|||false|string||
|&emsp;&emsp;delFlag|||false|string||
|&emsp;&emsp;id|||false|integer(int64)||
|&emsp;&emsp;label|||false|string||
|&emsp;&emsp;parentId|||false|integer(int64)||
|&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;sort|||false|integer(int32)||
|&emsp;&emsp;type|||false|string||
|&emsp;&emsp;updateBy|||false|string||
|&emsp;&emsp;updateTime|||false|string(date-time)||
|&emsp;&emsp;value|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«SysDictDataBO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|SysDictDataBO|
|&emsp;&emsp;createBy||string||
|&emsp;&emsp;createTime||string(date-time)||
|&emsp;&emsp;dataType||string||
|&emsp;&emsp;delFlag||string||
|&emsp;&emsp;id||integer(int64)||
|&emsp;&emsp;label||string||
|&emsp;&emsp;parentId||integer(int64)||
|&emsp;&emsp;remark||string||
|&emsp;&emsp;sort||integer(int32)||
|&emsp;&emsp;type||string||
|&emsp;&emsp;updateBy||string||
|&emsp;&emsp;updateTime||string(date-time)||
|&emsp;&emsp;value||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"createBy": "",
			"createTime": "",
			"dataType": "",
			"delFlag": "",
			"id": 0,
			"label": "",
			"parentId": 0,
			"remark": "",
			"sort": 0,
			"type": "",
			"updateBy": "",
			"updateTime": "",
			"value": ""
		}
	]
}
```


## 3：根据条件批量查询字典数据Plus(返回值为json)


**接口地址**:`/dict/data/list/plus`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "createBy": "",
  "createTime": "",
  "dataType": "",
  "delFlag": "",
  "id": 0,
  "label": "",
  "parentId": 0,
  "remark": "",
  "sort": 0,
  "type": "",
  "updateBy": "",
  "updateTime": "",
  "value": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDictDataBO|sysDictDataBO|body|true|SysDictDataBO|SysDictDataBO|
|&emsp;&emsp;createBy|||false|string||
|&emsp;&emsp;createTime|||false|string(date-time)||
|&emsp;&emsp;dataType|||false|string||
|&emsp;&emsp;delFlag|||false|string||
|&emsp;&emsp;id|||false|integer(int64)||
|&emsp;&emsp;label|||false|string||
|&emsp;&emsp;parentId|||false|integer(int64)||
|&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;sort|||false|integer(int32)||
|&emsp;&emsp;type|||false|string||
|&emsp;&emsp;updateBy|||false|string||
|&emsp;&emsp;updateTime|||false|string(date-time)||
|&emsp;&emsp;value|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«SysDictDataPlusBO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|SysDictDataPlusBO|
|&emsp;&emsp;dataType||string||
|&emsp;&emsp;delFlag||string||
|&emsp;&emsp;id||integer(int64)||
|&emsp;&emsp;label||string||
|&emsp;&emsp;parentId||integer(int64)||
|&emsp;&emsp;remark||object||
|&emsp;&emsp;sort||integer(int32)||
|&emsp;&emsp;type||string||
|&emsp;&emsp;value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"dataType": "",
			"delFlag": "",
			"id": 0,
			"label": "",
			"parentId": 0,
			"remark": {},
			"sort": 0,
			"type": "",
			"value": {}
		}
	]
}
```


## 7：字典数据分页查询(current、size)


**接口地址**:`/dict/data/page`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|countId||query|false|string||
|current||query|false|integer(int64)||
|maxLimit||query|false|integer(int64)||
|optimizeCountSql||query|false|boolean||
|orders[0].asc||query|false|boolean||
|orders[0].column||query|false|string||
|page|页面参数|query|false|||
|pages||query|false|integer(int64)||
|records||query|false|array|object|
|searchCount||query|false|boolean||
|size||query|false|integer(int64)||
|total||query|false|integer(int64)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«SysDictDataVO»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«SysDictDataVO»|Page«SysDictDataVO»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SysDictDataVO|
|&emsp;&emsp;&emsp;&emsp;code|字典编码|integer||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|更新时间|string||
|&emsp;&emsp;&emsp;&emsp;cssClass|样式属性（其他样式扩展）|string||
|&emsp;&emsp;&emsp;&emsp;dictType|字典类型|string||
|&emsp;&emsp;&emsp;&emsp;isDefault|是否默认（Y是 N否）|string||
|&emsp;&emsp;&emsp;&emsp;label|字典标签|string||
|&emsp;&emsp;&emsp;&emsp;listClass|表格回显样式|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;sort|字典排序|integer||
|&emsp;&emsp;&emsp;&emsp;status|状态（0正常 1停用）|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;&emsp;&emsp;value|字典键值|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"code": 0,
				"createBy": "",
				"createTime": "",
				"cssClass": "",
				"dictType": "",
				"isDefault": "",
				"label": "",
				"listClass": "",
				"remark": "",
				"sort": 0,
				"status": "",
				"updateBy": "",
				"updateTime": "",
				"value": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


## 9：通过id删除数据字典单个节点(如果是树节点则删除对应的子节点)


**接口地址**:`/dict/data/removeById`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|integer(int64)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 4：根据字典类型和字典键值查询字典数据


**接口地址**:`/dict/data/selectLabel`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|type|字典类型|query|true|string||
|value|字典键值|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 5:修改字典数据Plus


**接口地址**:`/dict/data/updatePlus`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": 0,
  "label": "",
  "parentId": 0,
  "remark": "",
  "sort": 0,
  "type": "",
  "value": {}
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDictDataUpdatePlusReq|sysDictDataUpdatePlusReq|body|true|SysDictDataUpdatePlusReq|SysDictDataUpdatePlusReq|
|&emsp;&emsp;id|||true|integer(int64)||
|&emsp;&emsp;label|||false|string||
|&emsp;&emsp;parentId|||false|integer(int64)||
|&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;sort|||false|integer(int32)||
|&emsp;&emsp;type|||false|string||
|&emsp;&emsp;value|||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 8：根据ID获取字典数据信息


**接口地址**:`/dict/data/{id}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|path|true|integer(int64)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysDictDataPlusBO»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysDictDataPlusBO|SysDictDataPlusBO|
|&emsp;&emsp;dataType||string||
|&emsp;&emsp;delFlag||string||
|&emsp;&emsp;id||integer(int64)||
|&emsp;&emsp;label||string||
|&emsp;&emsp;parentId||integer(int64)||
|&emsp;&emsp;remark||object||
|&emsp;&emsp;sort||integer(int32)||
|&emsp;&emsp;type||string||
|&emsp;&emsp;value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"dataType": "",
		"delFlag": "",
		"id": 0,
		"label": "",
		"parentId": 0,
		"remark": {},
		"sort": 0,
		"type": "",
		"value": {}
	}
}
```


# 字典管理-类型


## 6：删除字典类型


**接口地址**:`/dict/type/delete`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|integer(int64)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 4：字典类型分页查询(current、size)


**接口地址**:`/dict/type/page`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|countId||query|false|string||
|current||query|false|integer(int64)||
|maxLimit||query|false|integer(int64)||
|name|name|query|false|string||
|optimizeCountSql||query|false|boolean||
|orders[0].asc||query|false|boolean||
|orders[0].column||query|false|string||
|page|分页参数|query|false|||
|pages||query|false|integer(int64)||
|records||query|false|array|object|
|searchCount||query|false|boolean||
|size||query|false|integer(int64)||
|total||query|false|integer(int64)||
|type|type|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«SysDictTypeVO»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«SysDictTypeVO»|Page«SysDictTypeVO»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SysDictTypeVO|
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;dataType|数据类型 0:列表 1:树形|string||
|&emsp;&emsp;&emsp;&emsp;delFlag|字典类型|string||
|&emsp;&emsp;&emsp;&emsp;id|字典主键|integer||
|&emsp;&emsp;&emsp;&emsp;name|字典名称|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;status|状态（0正常 1停用）|string||
|&emsp;&emsp;&emsp;&emsp;type|字典编码|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"createBy": "",
				"createTime": "",
				"dataType": "",
				"delFlag": "",
				"id": 0,
				"name": "",
				"remark": "",
				"status": "",
				"type": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


## 1：新增字典类型


**接口地址**:`/dict/type/save`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "dataType": "",
  "delFlag": "",
  "id": 0,
  "name": "",
  "remark": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDictTypeReq|系统-字典类型表|body|true|SysDictTypeReq|SysDictTypeReq|
|&emsp;&emsp;dataType|数据类型,0:列表 1:树||false|string||
|&emsp;&emsp;delFlag|状态（0正常 1停用）||false|string||
|&emsp;&emsp;id|字典主键||false|integer(int64)||
|&emsp;&emsp;name|字典名称||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;type|字典类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 3：根据字典类型查询批量查询字典数据


**接口地址**:`/dict/type/select`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|dataType|dataType|query|true|string||
|type|type|query|true|string||
|delFlag|delFlag|query|false|string||
|label|label|query|false|string||
|value|value|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«object»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": []
}
```


## 7：根据多个字典类型查询批量查询字典数据


**接口地址**:`/dict/type/selectByTypes`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|delFlag|delFlag|query|false|string||
|types|types|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Map«string,List«SysDictDataBO»»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysDictDataBO|SysDictDataBO|
|&emsp;&emsp;createBy||string||
|&emsp;&emsp;createTime||string(date-time)||
|&emsp;&emsp;dataType||string||
|&emsp;&emsp;delFlag||string||
|&emsp;&emsp;id||integer(int64)||
|&emsp;&emsp;label||string||
|&emsp;&emsp;parentId||integer(int64)||
|&emsp;&emsp;remark||string||
|&emsp;&emsp;sort||integer(int32)||
|&emsp;&emsp;type||string||
|&emsp;&emsp;updateBy||string||
|&emsp;&emsp;updateTime||string(date-time)||
|&emsp;&emsp;value||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"additionalProperties1": {
			"createBy": "",
			"createTime": "",
			"dataType": "",
			"delFlag": "",
			"id": 0,
			"label": "",
			"parentId": 0,
			"remark": "",
			"sort": 0,
			"type": "",
			"updateBy": "",
			"updateTime": "",
			"value": ""
		}
	}
}
```


## 3：根据字典类型查询批量查询字典数据(PLUS)


**接口地址**:`/dict/type/selectPlus`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|dataType|dataType|query|false|string||
|delFlag|delFlag|query|false|string||
|type|type|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«object»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": []
}
```


## 5：更新字典类型


**接口地址**:`/dict/type/update`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "dataType": "",
  "delFlag": "",
  "id": 0,
  "name": "",
  "remark": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDictTypeReq|系统-字典类型表|body|true|SysDictTypeReq|SysDictTypeReq|
|&emsp;&emsp;dataType|数据类型,0:列表 1:树||false|string||
|&emsp;&emsp;delFlag|状态（0正常 1停用）||false|string||
|&emsp;&emsp;id|字典主键||false|integer(int64)||
|&emsp;&emsp;name|字典名称||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;type|字典类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 2：根据ID获取字典类型信息


**接口地址**:`/dict/type/{id}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysDictTypeRes»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysDictTypeRes|SysDictTypeRes|
|&emsp;&emsp;createBy||string||
|&emsp;&emsp;createTime||string(date-time)||
|&emsp;&emsp;dataType||string||
|&emsp;&emsp;delFlag||string||
|&emsp;&emsp;id||integer(int64)||
|&emsp;&emsp;name||string||
|&emsp;&emsp;remark||string||
|&emsp;&emsp;type||string||
|&emsp;&emsp;updateBy||string||
|&emsp;&emsp;updateTime||string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"dataType": "",
		"delFlag": "",
		"id": 0,
		"name": "",
		"remark": "",
		"type": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


# 接收命令


## 分页通过接收命令反查生命体列表


**接口地址**:`/acmValue/getLifeListByAcmValue`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "acmValue": "",
  "countId": "",
  "current": 0,
  "levelId": "",
  "maxLimit": 0,
  "name": "",
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "records": [],
  "searchCount": true,
  "size": 0,
  "total": 0,
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDataPageQueryReq|分页通过接收命令反查生命体列表Req|body|true|LifeListPageByAcmValueReq|LifeListPageByAcmValueReq|
|&emsp;&emsp;acmValue|接收命令||false|string||
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;levelId|关卡Id||false|string||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;name|生命体名称||false|string||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||
|&emsp;&emsp;type|类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«LifeDataVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«LifeDataVO»|IPage«LifeDataVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|LifeDataVO|
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡ID|string||
|&emsp;&emsp;&emsp;&emsp;lifeTemplateId|生命体模板ID|string||
|&emsp;&emsp;&emsp;&emsp;lockStatus|锁定状态|string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;type|类型|string||
|&emsp;&emsp;&emsp;&emsp;value|键值|object||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"id": "",
				"levelId": "",
				"lifeTemplateId": "",
				"lockStatus": "",
				"name": "",
				"projectId": "",
				"remark": "",
				"showStatus": "",
				"type": "",
				"value": {}
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 通过关卡id跟函数名称名称 模糊搜索获取生命体接收命令列表


**接口地址**:`/acmValue/queryLifeAcmValueListByLevelId`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "acmValueName": "",
  "levelId": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeAcmValueListQueryReq|生命体接受命令Req|body|true|LifeAcmValueListQueryReq|LifeAcmValueListQueryReq|
|&emsp;&emsp;acmValueName|函数名称||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«string»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": []
}
```


# 操作日志管理


## 分页查询


**接口地址**:`/operateLog/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "className": "",
  "costTime": 0,
  "countId": "",
  "current": 0,
  "id": "",
  "maxLimit": 0,
  "methodName": "",
  "methodParam": "",
  "methodReturn": "",
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "records": [],
  "requestUrl": "",
  "searchCount": true,
  "size": 0,
  "total": 0,
  "userName": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|operateLogPageQueryReq|操作日志分页查询Req|body|true|OperateLogPageQueryReq|OperateLogPageQueryReq|
|&emsp;&emsp;className|类名||false|string||
|&emsp;&emsp;costTime|消耗时间||false|integer(int64)||
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;methodName|方法名||false|string||
|&emsp;&emsp;methodParam|入参||false|string||
|&emsp;&emsp;methodReturn|出参||false|string||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;requestUrl|请求路径||false|string||
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||
|&emsp;&emsp;userName|用户名||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«OperateLogVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«OperateLogVO»|IPage«OperateLogVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|OperateLogVO|
|&emsp;&emsp;&emsp;&emsp;className|类名|string||
|&emsp;&emsp;&emsp;&emsp;costTime|消耗时间|integer||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;methodName|方法名|string||
|&emsp;&emsp;&emsp;&emsp;methodParam|入参|string||
|&emsp;&emsp;&emsp;&emsp;methodReturn|出参|string||
|&emsp;&emsp;&emsp;&emsp;requestUrl|请求路径|string||
|&emsp;&emsp;&emsp;&emsp;userName|用户名|string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"className": "",
				"costTime": 0,
				"createTime": "",
				"id": "",
				"methodName": "",
				"methodParam": "",
				"methodReturn": "",
				"requestUrl": "",
				"userName": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


# 数据转换-生命体


## update


**接口地址**:`/data-converter-life-dic-data`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "coordinate": "{\"type\":\"Point\",\"coordinates\":[30,10]}",
  "id": "",
  "levelId": 1808439439534354433,
  "modelType": "设备-摄像头",
  "name": "生命体名称",
  "projectId": 1808439439337222145,
  "property": "{\"type\":\"camera\"}",
  "spatialLevel": "建筑-楼层-区域-房间",
  "templateId": "d0a586024105bc42678dcd8cff4c06da",
  "type": "mesh"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|dataConverterLifeDicDataReq|数据转化成生命体|body|true|DataConverterLifeDicDataReq|DataConverterLifeDicDataReq|
|&emsp;&emsp;coordinate|坐标||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;levelId|等级id||false|string||
|&emsp;&emsp;modelType|对象属性||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;property|属性||false|string||
|&emsp;&emsp;spatialLevel|空间层次||false|string||
|&emsp;&emsp;templateId|模板id||false|string||
|&emsp;&emsp;type|生命体类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## create


**接口地址**:`/data-converter-life-dic-data/add`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "coordinate": "{\"type\":\"Point\",\"coordinates\":[30,10]}",
  "id": "",
  "levelId": 1808439439534354433,
  "modelType": "设备-摄像头",
  "name": "生命体名称",
  "projectId": 1808439439337222145,
  "property": "{\"type\":\"camera\"}",
  "spatialLevel": "建筑-楼层-区域-房间",
  "templateId": "d0a586024105bc42678dcd8cff4c06da",
  "type": "mesh"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|dataConverterLifeDicDataReq|数据转化成生命体|body|true|DataConverterLifeDicDataReq|DataConverterLifeDicDataReq|
|&emsp;&emsp;coordinate|坐标||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;levelId|等级id||false|string||
|&emsp;&emsp;modelType|对象属性||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;property|属性||false|string||
|&emsp;&emsp;spatialLevel|空间层次||false|string||
|&emsp;&emsp;templateId|模板id||false|string||
|&emsp;&emsp;type|生命体类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 单对象-转换数据


**接口地址**:`/data-converter-life-dic-data/converter`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>通过传入单个对象，来转换数据</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|coordinate|空间信息|query|false|string||
|levelId|层级id|query|false|string||
|lifeId|生成的生命体id|query|false|string||
|modelType|业务层次|query|false|string||
|name|生命体名称|query|false|string||
|number|生命体批次|query|false|string||
|projectId|项目id|query|false|string||
|property|属性|query|false|string||
|spatialLevel|空间层次|query|false|string||
|templateId|模板id|query|false|string||
|type|生命体类型|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 【历史数据清洗】从三维到二维


**接口地址**:`/data-converter-life-dic-data/converter3Dto2D`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>历史数据清洗从三维到二维</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 导入记录


**接口地址**:`/data-converter-life-dic-data/importRecord`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 生命体分类新增并引入


**接口地址**:`/data-converter-life-dic-data/lifeSortAddIntroduce`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "lifeSortId": "",
  "lifeTemplateId": "",
  "lockStatus": "",
  "name": "",
  "projectId": "",
  "remark": "",
  "showStatus": "",
  "type": "",
  "value": {}
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSortDataImportReq|生命体分类新增引入|body|true|LifeSortDateImportReq|LifeSortDateImportReq|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeSortId|生命体分类id||false|string||
|&emsp;&emsp;lifeTemplateId|生命体模板ID||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;name|生命体名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;type|生命体类型||false|string||
|&emsp;&emsp;value|键值||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 获取最大id数据


**接口地址**:`/data-converter-life-dic-data/max_id`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«int»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||integer(int32)|integer(int32)|


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": 0
}
```


## queryPageList


**接口地址**:`/data-converter-life-dic-data/queryPageList`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "coordinate": "{\"type\":\"Point\",\"coordinates\":[30,10]}",
  "id": "",
  "levelId": 1808439439534354433,
  "modelType": "设备-摄像头",
  "name": "生命体名称",
  "projectId": 1808439439337222145,
  "property": "{\"type\":\"camera\"}",
  "spatialLevel": "建筑-楼层-区域-房间",
  "templateId": "d0a586024105bc42678dcd8cff4c06da",
  "type": "mesh"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|dataConverterLifeDicData|数据转化成生命体|body|true|DataConverterLifeDicDataReq|DataConverterLifeDicDataReq|
|&emsp;&emsp;coordinate|坐标||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;levelId|等级id||false|string||
|&emsp;&emsp;modelType|对象属性||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;property|属性||false|string||
|&emsp;&emsp;spatialLevel|空间层次||false|string||
|&emsp;&emsp;templateId|模板id||false|string||
|&emsp;&emsp;type|生命体类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«DataConverterLifeDicDataRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«DataConverterLifeDicDataRes»|IPage«DataConverterLifeDicDataRes»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|DataConverterLifeDicDataRes|
|&emsp;&emsp;&emsp;&emsp;coordinate|坐标|string||
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|等级id|string||
|&emsp;&emsp;&emsp;&emsp;modelType|对象属性|string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;property|属性|string||
|&emsp;&emsp;&emsp;&emsp;spatialLevel|空间层次|string||
|&emsp;&emsp;&emsp;&emsp;templateId|模板id|string||
|&emsp;&emsp;&emsp;&emsp;type|生命体类型|string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"coordinate": "{\"type\":\"Point\",\"coordinates\":[30,10]}",
				"id": "",
				"levelId": 1808439439534354433,
				"modelType": "设备-摄像头",
				"name": "生命体名称",
				"projectId": 1808439439337222145,
				"property": "{\"type\":\"camera\"}",
				"spatialLevel": "建筑-楼层-区域-房间",
				"templateId": "d0a586024105bc42678dcd8cff4c06da",
				"type": "mesh"
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## Excel导入-批量转换数据


**接口地址**:`/data-converter-life-dic-data/upload`


**请求方式**:`POST`


**请求数据类型**:`multipart/form-data`


**响应数据类型**:`*/*`


**接口描述**:<p>通过传入项目id和关卡id，来批量转换数据</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|levelId|levelId|query|true|string||
|number|number|query|true|string||
|projectId|projectId|query|true|string||
|file||formData|false|file||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Map«string,object»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## delete


**接口地址**:`/data-converter-life-dic-data/{id}`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


# 权限菜单关联表对象功能接口


## 根据id查询数据


**接口地址**:`/sysRoleMenu`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysRoleMenuRes»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysRoleMenuRes|SysRoleMenuRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;menuId|菜单id|string||
|&emsp;&emsp;roleId|角色id|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"id": "",
		"menuId": "",
		"roleId": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 添加数据


**接口地址**:`/sysRoleMenu`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "menuId": "",
  "roleId": "",
  "size": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysRoleMenuReq|权限菜单关联表|body|true|SysRoleMenuReq|SysRoleMenuReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;menuId|菜单id||false|string||
|&emsp;&emsp;roleId|角色id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysRoleMenuRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysRoleMenuRes|SysRoleMenuRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;menuId|菜单id|string||
|&emsp;&emsp;roleId|角色id|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"id": "",
		"menuId": "",
		"roleId": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 根据id更新数据


**接口地址**:`/sysRoleMenu`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "menuId": "",
  "roleId": "",
  "size": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysRoleMenuReq|权限菜单关联表|body|true|SysRoleMenuReq|SysRoleMenuReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;menuId|菜单id||false|string||
|&emsp;&emsp;roleId|角色id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysRoleMenuRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysRoleMenuRes|SysRoleMenuRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;menuId|菜单id|string||
|&emsp;&emsp;roleId|角色id|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"id": "",
		"menuId": "",
		"roleId": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 根据ids删除数据


**接口地址**:`/sysRoleMenu`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|ids|ids列表|body|true|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«int»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||integer(int32)|integer(int32)|


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": 0
}
```


## 分页条件查询数据


**接口地址**:`/sysRoleMenu/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "menuId": "",
  "roleId": "",
  "size": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysRoleMenuReq|权限菜单关联表|body|true|SysRoleMenuReq|SysRoleMenuReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;menuId|菜单id||false|string||
|&emsp;&emsp;roleId|角色id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«SysRoleMenuRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«SysRoleMenuRes»|Page«SysRoleMenuRes»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SysRoleMenuRes|
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;menuId|菜单id|string||
|&emsp;&emsp;&emsp;&emsp;roleId|角色id|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"createBy": "",
				"createTime": "",
				"id": "",
				"menuId": "",
				"roleId": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


# 权限表对象功能接口


## 根据id查询数据


**接口地址**:`/sysRole`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysRoleRes»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysRoleRes|SysRoleRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;key|角色权限|string||
|&emsp;&emsp;menuCheckStrictly|父子联动|boolean||
|&emsp;&emsp;name|角色名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|角色状态（0正常、1不正常）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"id": "",
		"key": "",
		"menuCheckStrictly": true,
		"name": "",
		"remark": "",
		"sort": 0,
		"status": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 添加数据


**接口地址**:`/sysRole`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "beginTime": "",
  "current": 0,
  "endTime": "",
  "id": "",
  "key": "",
  "menuCheckStrictly": true,
  "menuIds": [],
  "name": "",
  "remark": "",
  "size": 0,
  "sort": 0,
  "status": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysRoleReq|权限表|body|true|SysRoleReq|SysRoleReq|
|&emsp;&emsp;beginTime|开始时间||false|string(date-time)||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;endTime|结束时间||false|string(date-time)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;key|角色权限||false|string||
|&emsp;&emsp;menuCheckStrictly|父子联动||false|boolean||
|&emsp;&emsp;menuIds|菜单ids||false|array|string|
|&emsp;&emsp;name|角色名称||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序||false|integer(int32)||
|&emsp;&emsp;status|角色状态（0正常、1不正常）||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysRoleRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysRoleRes|SysRoleRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;key|角色权限|string||
|&emsp;&emsp;menuCheckStrictly|父子联动|boolean||
|&emsp;&emsp;name|角色名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|角色状态（0正常、1不正常）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"id": "",
		"key": "",
		"menuCheckStrictly": true,
		"name": "",
		"remark": "",
		"sort": 0,
		"status": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 根据id更新数据


**接口地址**:`/sysRole`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "beginTime": "",
  "current": 0,
  "endTime": "",
  "id": "",
  "key": "",
  "menuCheckStrictly": true,
  "menuIds": [],
  "name": "",
  "remark": "",
  "size": 0,
  "sort": 0,
  "status": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysRoleReq|权限表|body|true|SysRoleReq|SysRoleReq|
|&emsp;&emsp;beginTime|开始时间||false|string(date-time)||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;endTime|结束时间||false|string(date-time)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;key|角色权限||false|string||
|&emsp;&emsp;menuCheckStrictly|父子联动||false|boolean||
|&emsp;&emsp;menuIds|菜单ids||false|array|string|
|&emsp;&emsp;name|角色名称||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序||false|integer(int32)||
|&emsp;&emsp;status|角色状态（0正常、1不正常）||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysRoleRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysRoleRes|SysRoleRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;key|角色权限|string||
|&emsp;&emsp;menuCheckStrictly|父子联动|boolean||
|&emsp;&emsp;name|角色名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|角色状态（0正常、1不正常）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"id": "",
		"key": "",
		"menuCheckStrictly": true,
		"name": "",
		"remark": "",
		"sort": 0,
		"status": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 根据ids删除数据


**接口地址**:`/sysRole`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|ids|ids列表|body|true|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«int»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||integer(int32)|integer(int32)|


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": 0
}
```


## 根据权限获取绑定的用户


**接口地址**:`/sysRole/allocatedList`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "allocated": true,
  "avatar": "",
  "beginTime": "",
  "createTime": "",
  "current": 0,
  "email": "",
  "endTime": "",
  "gender": "",
  "id": 0,
  "loginDate": "",
  "nickname": "",
  "password": "",
  "phoneNumber": "",
  "remark": "",
  "roleId": [],
  "size": 0,
  "status": "",
  "username": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|userDto|userDto|body|true|UserDTO|UserDTO|
|&emsp;&emsp;allocated|绑定（true绑定、false未绑定）||false|boolean||
|&emsp;&emsp;avatar|用户头像||false|string||
|&emsp;&emsp;beginTime|开始时间||false|string(date-time)||
|&emsp;&emsp;createTime|创建时间||false|string(date-time)||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;email|用户邮箱||false|string||
|&emsp;&emsp;endTime|结束时间||false|string(date-time)||
|&emsp;&emsp;gender|用户性别||false|string||
|&emsp;&emsp;id|唯一id||false|integer(int64)||
|&emsp;&emsp;loginDate|最近登录时间||false|string(date-time)||
|&emsp;&emsp;nickname|用户昵称||false|string||
|&emsp;&emsp;password|用户密码||false|string||
|&emsp;&emsp;phoneNumber|手机号码||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;roleId|角色id||false|array|string|
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;status|用户状态（0停用、1正常）||false|string||
|&emsp;&emsp;username|用户账号||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«UserDTO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«UserDTO»|Page«UserDTO»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|UserDTO|
|&emsp;&emsp;&emsp;&emsp;allocated|绑定（true绑定、false未绑定）|boolean||
|&emsp;&emsp;&emsp;&emsp;avatar|用户头像|string||
|&emsp;&emsp;&emsp;&emsp;beginTime|开始时间|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;current|起始页|integer||
|&emsp;&emsp;&emsp;&emsp;email|用户邮箱|string||
|&emsp;&emsp;&emsp;&emsp;endTime|结束时间|string||
|&emsp;&emsp;&emsp;&emsp;gender|用户性别|string||
|&emsp;&emsp;&emsp;&emsp;id|唯一id|integer||
|&emsp;&emsp;&emsp;&emsp;loginDate|最近登录时间|string||
|&emsp;&emsp;&emsp;&emsp;nickname|用户昵称|string||
|&emsp;&emsp;&emsp;&emsp;password|用户密码|string||
|&emsp;&emsp;&emsp;&emsp;phoneNumber|手机号码|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;roleId|角色id|array|string|
|&emsp;&emsp;&emsp;&emsp;size|每页条数|integer||
|&emsp;&emsp;&emsp;&emsp;status|用户状态（0停用、1正常）|string||
|&emsp;&emsp;&emsp;&emsp;username|用户账号|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"allocated": true,
				"avatar": "",
				"beginTime": "",
				"createTime": "",
				"current": 0,
				"email": "",
				"endTime": "",
				"gender": "",
				"id": 0,
				"loginDate": "",
				"nickname": "",
				"password": "",
				"phoneNumber": "",
				"remark": "",
				"roleId": [],
				"size": 0,
				"status": "",
				"username": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


## 分页条件查询数据


**接口地址**:`/sysRole/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "beginTime": "",
  "current": 0,
  "endTime": "",
  "id": "",
  "key": "",
  "menuCheckStrictly": true,
  "menuIds": [],
  "name": "",
  "remark": "",
  "size": 0,
  "sort": 0,
  "status": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysRoleReq|权限表|body|true|SysRoleReq|SysRoleReq|
|&emsp;&emsp;beginTime|开始时间||false|string(date-time)||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;endTime|结束时间||false|string(date-time)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;key|角色权限||false|string||
|&emsp;&emsp;menuCheckStrictly|父子联动||false|boolean||
|&emsp;&emsp;menuIds|菜单ids||false|array|string|
|&emsp;&emsp;name|角色名称||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序||false|integer(int32)||
|&emsp;&emsp;status|角色状态（0正常、1不正常）||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«SysRoleRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«SysRoleRes»|Page«SysRoleRes»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SysRoleRes|
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;key|角色权限|string||
|&emsp;&emsp;&emsp;&emsp;menuCheckStrictly|父子联动|boolean||
|&emsp;&emsp;&emsp;&emsp;name|角色名称|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序|integer||
|&emsp;&emsp;&emsp;&emsp;status|角色状态（0正常、1不正常）|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"createBy": "",
				"createTime": "",
				"id": "",
				"key": "",
				"menuCheckStrictly": true,
				"name": "",
				"remark": "",
				"sort": 0,
				"status": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


## 根据当前登录用户查询角色列表


**接口地址**:`/sysRole/queryRolesByCurrentUser`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«SysRoleRes»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|SysRoleRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;key|角色权限|string||
|&emsp;&emsp;menuCheckStrictly|父子联动|boolean||
|&emsp;&emsp;name|角色名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|角色状态（0正常、1不正常）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"createBy": "",
			"createTime": "",
			"id": "",
			"key": "",
			"menuCheckStrictly": true,
			"name": "",
			"remark": "",
			"sort": 0,
			"status": "",
			"updateBy": "",
			"updateTime": ""
		}
	]
}
```


# 树跟生命体之间关联关系


## 批量双删树下叶子节点跟关联关系


**接口地址**:`/sysTreeWorkIndex/batchDeleteLeafAndIndex`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "model": 0,
  "projectId": "",
  "sysTreeWorkIndexDTOList": [
    {
      "dirId": "",
      "dirPath": "",
      "lifeCount": 0,
      "lockStatus": "",
      "name": "",
      "showStatus": "",
      "sortIndex": 0,
      "value": {},
      "workId": "",
      "workType": ""
    }
  ]
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|batchCreateSysTreeWorkIndexReq|批量插入树跟业务节点关联关系请求体|body|true|BatchCreateSysTreeWorkIndexReq|BatchCreateSysTreeWorkIndexReq|
|&emsp;&emsp;businessId|业务ID||false|string||
|&emsp;&emsp;model|树跟业务节点关联关系类型:1-目录树||false|integer(int32)||
|&emsp;&emsp;projectId|项目ID||false|string||
|&emsp;&emsp;sysTreeWorkIndexDTOList|||false|array|SysTreeWorkIndexDTO|
|&emsp;&emsp;&emsp;&emsp;dirId|||false|string||
|&emsp;&emsp;&emsp;&emsp;dirPath|||false|string||
|&emsp;&emsp;&emsp;&emsp;lifeCount|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;name|||false|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;sortIndex|||false|integer||
|&emsp;&emsp;&emsp;&emsp;value|||false|object||
|&emsp;&emsp;&emsp;&emsp;workId|||false|string||
|&emsp;&emsp;&emsp;&emsp;workType|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 批量删除树跟叶子节点之间关联关系


**接口地址**:`/sysTreeWorkIndex/batchDeleteSysTreeWorkIndex`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "model": 0,
  "projectId": "",
  "sysTreeWorkIndexDTOList": [
    {
      "dirId": "",
      "dirPath": "",
      "lifeCount": 0,
      "lockStatus": "",
      "name": "",
      "showStatus": "",
      "sortIndex": 0,
      "value": {},
      "workId": "",
      "workType": ""
    }
  ]
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|batchCreateSysTreeWorkIndexReq|批量插入树跟业务节点关联关系请求体|body|true|BatchCreateSysTreeWorkIndexReq|BatchCreateSysTreeWorkIndexReq|
|&emsp;&emsp;businessId|业务ID||false|string||
|&emsp;&emsp;model|树跟业务节点关联关系类型:1-目录树||false|integer(int32)||
|&emsp;&emsp;projectId|项目ID||false|string||
|&emsp;&emsp;sysTreeWorkIndexDTOList|||false|array|SysTreeWorkIndexDTO|
|&emsp;&emsp;&emsp;&emsp;dirId|||false|string||
|&emsp;&emsp;&emsp;&emsp;dirPath|||false|string||
|&emsp;&emsp;&emsp;&emsp;lifeCount|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;name|||false|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;sortIndex|||false|integer||
|&emsp;&emsp;&emsp;&emsp;value|||false|object||
|&emsp;&emsp;&emsp;&emsp;workId|||false|string||
|&emsp;&emsp;&emsp;&emsp;workType|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 批量插入树跟叶子节点之间关联关系


**接口地址**:`/sysTreeWorkIndex/batchInsertSysTreeWorkIndex`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "businessId": "",
  "model": 0,
  "projectId": "",
  "sysTreeWorkIndexDTOList": [
    {
      "dirId": "",
      "dirPath": "",
      "lifeCount": 0,
      "lockStatus": "",
      "name": "",
      "showStatus": "",
      "sortIndex": 0,
      "value": {},
      "workId": "",
      "workType": ""
    }
  ]
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|batchCreateSysTreeWorkIndexReq|批量插入树跟业务节点关联关系请求体|body|true|BatchCreateSysTreeWorkIndexReq|BatchCreateSysTreeWorkIndexReq|
|&emsp;&emsp;businessId|业务ID||false|string||
|&emsp;&emsp;model|树跟业务节点关联关系类型:1-目录树||false|integer(int32)||
|&emsp;&emsp;projectId|项目ID||false|string||
|&emsp;&emsp;sysTreeWorkIndexDTOList|||false|array|SysTreeWorkIndexDTO|
|&emsp;&emsp;&emsp;&emsp;dirId|||false|string||
|&emsp;&emsp;&emsp;&emsp;dirPath|||false|string||
|&emsp;&emsp;&emsp;&emsp;lifeCount|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;name|||false|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;sortIndex|||false|integer||
|&emsp;&emsp;&emsp;&emsp;value|||false|object||
|&emsp;&emsp;&emsp;&emsp;workId|||false|string||
|&emsp;&emsp;&emsp;&emsp;workType|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


# 环境任务表管理


## 新增变量任务


**接口地址**:`/api-env-job`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "activeStatus": "",
  "apiId": "",
  "apiResEnvVarMap": {},
  "appId": "",
  "cron": "",
  "envId": "",
  "id": "",
  "name": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvJobReq|环境任务表|body|true|环境任务表|环境任务表|
|&emsp;&emsp;activeStatus|开启标识（0关闭状态、1开启状态）||false|string||
|&emsp;&emsp;apiId|api id||false|string||
|&emsp;&emsp;apiResEnvVarMap|api出参与环境变量key映射 jsonpath||false|object||
|&emsp;&emsp;appId|app id||false|string||
|&emsp;&emsp;cron|定时任务表达式||false|string||
|&emsp;&emsp;envId|env id||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|任务名称||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 修改变量任务


**接口地址**:`/api-env-job`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "activeStatus": "",
  "apiId": "",
  "apiResEnvVarMap": {},
  "appId": "",
  "cron": "",
  "envId": "",
  "id": "",
  "name": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvJobReq|环境任务表|body|true|环境任务表|环境任务表|
|&emsp;&emsp;activeStatus|开启标识（0关闭状态、1开启状态）||false|string||
|&emsp;&emsp;apiId|api id||false|string||
|&emsp;&emsp;apiResEnvVarMap|api出参与环境变量key映射 jsonpath||false|object||
|&emsp;&emsp;appId|app id||false|string||
|&emsp;&emsp;cron|定时任务表达式||false|string||
|&emsp;&emsp;envId|env id||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|任务名称||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id删除变量任务


**接口地址**:`/api-env-job`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id查询环境变量任务


**接口地址**:`/api-env-job/queryById`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


# 环境表管理


## 根据ids查询环境信息


**接口地址**:`/api-env`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|ids|id列表|query|true|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«环境表»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|环境表0|
|&emsp;&emsp;apiEnvGlobalParamFieldResList|环境全局配置|array|全局环境参数表|
|&emsp;&emsp;&emsp;&emsp;apiEnvId|env id|string||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;globalType|全局类型（0请求头、1请求体）|string||
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;paramDesc|参数注释|string||
|&emsp;&emsp;&emsp;&emsp;paramName|参数名称|string||
|&emsp;&emsp;&emsp;&emsp;paramType|参数类型（0常量、1常量）|string||
|&emsp;&emsp;&emsp;&emsp;paramValue|参数值|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;appId|app id|string||
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;envName|环境名称|string||
|&emsp;&emsp;envPrefixUrl|前置路径|string||
|&emsp;&emsp;id|id|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"apiEnvGlobalParamFieldResList": [
				{
					"apiEnvId": "",
					"createBy": "",
					"createTime": "",
					"globalType": "",
					"id": "",
					"paramDesc": "",
					"paramName": "",
					"paramType": "",
					"paramValue": "",
					"updateBy": "",
					"updateTime": ""
				}
			],
			"appId": "",
			"createBy": "",
			"createTime": "",
			"envName": "",
			"envPrefixUrl": "",
			"id": "",
			"updateBy": "",
			"updateTime": ""
		}
	]
}
```


## 新增api环境


**接口地址**:`/api-env`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "appId": "",
  "envName": "",
  "envPrefixUrl": "",
  "id": "",
  "page": 0,
  "size": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvReq|环境表|body|true|环境表|环境表|
|&emsp;&emsp;appId|app id||false|string||
|&emsp;&emsp;envName|环境名称||false|string||
|&emsp;&emsp;envPrefixUrl|前置路径||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;page|page||false|integer(int32)||
|&emsp;&emsp;size|size||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«string»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": ""
}
```


## 修改api环境


**接口地址**:`/api-env`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "appId": "",
  "envName": "",
  "envPrefixUrl": "",
  "id": "",
  "page": 0,
  "size": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvReq|环境表|body|true|环境表|环境表|
|&emsp;&emsp;appId|app id||false|string||
|&emsp;&emsp;envName|环境名称||false|string||
|&emsp;&emsp;envPrefixUrl|前置路径||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;page|page||false|integer(int32)||
|&emsp;&emsp;size|size||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id删除api环境


**接口地址**:`/api-env`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据条件分页查询api环境


**接口地址**:`/api-env/queryByPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "appId": "",
  "envName": "",
  "envPrefixUrl": "",
  "id": "",
  "page": 0,
  "size": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|apiEnvReq|环境表|body|true|环境表|环境表|
|&emsp;&emsp;appId|app id||false|string||
|&emsp;&emsp;envName|环境名称||false|string||
|&emsp;&emsp;envPrefixUrl|前置路径||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;page|page||false|integer(int32)||
|&emsp;&emsp;size|size||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«ApiEnvBO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«ApiEnvBO»|IPage«ApiEnvBO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|ApiEnvBO|
|&emsp;&emsp;&emsp;&emsp;apiEnvGlobalParamFieldBoList||array|ApiEnvGlobalParamFieldBO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;apiEnvId||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;apiEnvVarBoList||array|ApiEnvVarBO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;envId||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;varName||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;varValue||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;globalType||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;paramDesc||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;paramName||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;paramType||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;paramValue||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;&emsp;&emsp;appId||string||
|&emsp;&emsp;&emsp;&emsp;createBy||string||
|&emsp;&emsp;&emsp;&emsp;createTime||string||
|&emsp;&emsp;&emsp;&emsp;envName||string||
|&emsp;&emsp;&emsp;&emsp;envPrefixUrl||string||
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;updateBy||string||
|&emsp;&emsp;&emsp;&emsp;updateTime||string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"apiEnvGlobalParamFieldBoList": [
					{
						"apiEnvId": "",
						"apiEnvVarBoList": [
							{
								"createBy": "",
								"createTime": "",
								"envId": "",
								"id": "",
								"updateBy": "",
								"updateTime": "",
								"varName": "",
								"varValue": ""
							}
						],
						"createBy": "",
						"createTime": "",
						"globalType": "",
						"id": "",
						"paramDesc": "",
						"paramName": "",
						"paramType": "",
						"paramValue": "",
						"updateBy": "",
						"updateTime": ""
					}
				],
				"appId": "",
				"createBy": "",
				"createTime": "",
				"envName": "",
				"envPrefixUrl": "",
				"id": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


# 生命体二级分类通用集合


## 新增生命体二级分类通用集合


**接口地址**:`/life/subtype/common/add`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "lifeIds": "",
  "model": 0,
  "name": "",
  "oldParentId": "",
  "projectId": "",
  "sqlContent": "",
  "sysTreeDTO": {
    "ancestralChain": "",
    "businessId": "",
    "businessPageId": "",
    "createBy": "",
    "createTime": "",
    "delFlag": "",
    "directParentId": "",
    "id": "",
    "labelsModel": "",
    "level": 0,
    "lft": 0,
    "lockStatus": "",
    "model": 0,
    "name": "",
    "oldId": "",
    "passId": "",
    "projectId": "",
    "remark": "",
    "rgt": 0,
    "sameLevelLastId": "",
    "seq": 0,
    "showStatus": "",
    "status": "",
    "tenantWorkId": "",
    "type": "",
    "updateBy": "",
    "updateTime": ""
  }
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSubtypeCommonCollectionSaveReq|新增生命体二级分类通用集合|body|true|lifeSubtypeCommonCollectionSaveReq|lifeSubtypeCommonCollectionSaveReq|
|&emsp;&emsp;id|生命体二级分类集合id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeIds|生命体ids，以逗号隔开||false|string||
|&emsp;&emsp;model|1：动态（执行SQL挂载）2：静态（手动添加生命体）||false|integer(int32)||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;oldParentId|旧父节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;sqlContent|SQL查询语句||false|string||
|&emsp;&emsp;sysTreeDTO|当前树根节点||false|SysTreeDTO|SysTreeDTO|
|&emsp;&emsp;&emsp;&emsp;ancestralChain|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessId|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessPageId|||false|string||
|&emsp;&emsp;&emsp;&emsp;createBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;createTime|||false|string||
|&emsp;&emsp;&emsp;&emsp;delFlag|||false|string||
|&emsp;&emsp;&emsp;&emsp;directParentId|||false|string||
|&emsp;&emsp;&emsp;&emsp;id|||false|string||
|&emsp;&emsp;&emsp;&emsp;labelsModel|||false|string||
|&emsp;&emsp;&emsp;&emsp;level|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lft|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;model|||false|integer||
|&emsp;&emsp;&emsp;&emsp;name|||false|string||
|&emsp;&emsp;&emsp;&emsp;oldId|||false|string||
|&emsp;&emsp;&emsp;&emsp;passId|||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|||false|string||
|&emsp;&emsp;&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;&emsp;&emsp;rgt|||false|integer||
|&emsp;&emsp;&emsp;&emsp;sameLevelLastId|||false|string||
|&emsp;&emsp;&emsp;&emsp;seq|||false|integer||
|&emsp;&emsp;&emsp;&emsp;showStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;status|||false|string||
|&emsp;&emsp;&emsp;&emsp;tenantWorkId|||false|string||
|&emsp;&emsp;&emsp;&emsp;type|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysWorkIndexVO»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysWorkIndexVO|SysWorkIndexVO|
|&emsp;&emsp;dirId||string||
|&emsp;&emsp;dirPath||string||
|&emsp;&emsp;lifeCount||integer(int32)||
|&emsp;&emsp;lockStatus||string||
|&emsp;&emsp;name||string||
|&emsp;&emsp;showStatus||string||
|&emsp;&emsp;sortIndex||integer(int32)||
|&emsp;&emsp;value||object||
|&emsp;&emsp;workId||string||
|&emsp;&emsp;workType||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"dirId": "",
		"dirPath": "",
		"lifeCount": 0,
		"lockStatus": "",
		"name": "",
		"showStatus": "",
		"sortIndex": 0,
		"value": {},
		"workId": "",
		"workType": ""
	}
}
```


## 根据id删除生命体二级分类通用集合


**接口地址**:`/life/subtype/common/delete`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 条件查询生命体二级分类通用集合


**接口地址**:`/life/subtype/common/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "lifeIds": "",
  "model": 0,
  "name": "",
  "oldParentId": "",
  "projectId": "",
  "sqlContent": "",
  "sysTreeDTO": {
    "ancestralChain": "",
    "businessId": "",
    "businessPageId": "",
    "createBy": "",
    "createTime": "",
    "delFlag": "",
    "directParentId": "",
    "id": "",
    "labelsModel": "",
    "level": 0,
    "lft": 0,
    "lockStatus": "",
    "model": 0,
    "name": "",
    "oldId": "",
    "passId": "",
    "projectId": "",
    "remark": "",
    "rgt": 0,
    "sameLevelLastId": "",
    "seq": 0,
    "showStatus": "",
    "status": "",
    "tenantWorkId": "",
    "type": "",
    "updateBy": "",
    "updateTime": ""
  }
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSubtypeCommonCollectionSaveReq|新增生命体二级分类通用集合|body|true|lifeSubtypeCommonCollectionSaveReq|lifeSubtypeCommonCollectionSaveReq|
|&emsp;&emsp;id|生命体二级分类集合id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeIds|生命体ids，以逗号隔开||false|string||
|&emsp;&emsp;model|1：动态（执行SQL挂载）2：静态（手动添加生命体）||false|integer(int32)||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;oldParentId|旧父节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;sqlContent|SQL查询语句||false|string||
|&emsp;&emsp;sysTreeDTO|当前树根节点||false|SysTreeDTO|SysTreeDTO|
|&emsp;&emsp;&emsp;&emsp;ancestralChain|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessId|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessPageId|||false|string||
|&emsp;&emsp;&emsp;&emsp;createBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;createTime|||false|string||
|&emsp;&emsp;&emsp;&emsp;delFlag|||false|string||
|&emsp;&emsp;&emsp;&emsp;directParentId|||false|string||
|&emsp;&emsp;&emsp;&emsp;id|||false|string||
|&emsp;&emsp;&emsp;&emsp;labelsModel|||false|string||
|&emsp;&emsp;&emsp;&emsp;level|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lft|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;model|||false|integer||
|&emsp;&emsp;&emsp;&emsp;name|||false|string||
|&emsp;&emsp;&emsp;&emsp;oldId|||false|string||
|&emsp;&emsp;&emsp;&emsp;passId|||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|||false|string||
|&emsp;&emsp;&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;&emsp;&emsp;rgt|||false|integer||
|&emsp;&emsp;&emsp;&emsp;sameLevelLastId|||false|string||
|&emsp;&emsp;&emsp;&emsp;seq|||false|integer||
|&emsp;&emsp;&emsp;&emsp;showStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;status|||false|string||
|&emsp;&emsp;&emsp;&emsp;tenantWorkId|||false|string||
|&emsp;&emsp;&emsp;&emsp;type|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«lifeSubtypeCollectionRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||lifeSubtypeCollectionRes|lifeSubtypeCollectionRes|
|&emsp;&emsp;lifeSubtypeCommonCollectionVOList||array|LifeSubtypeCommonCollectionVO|
|&emsp;&emsp;&emsp;&emsp;id|生命体二级分类集合id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;lifeIds|所选生命体ids|string||
|&emsp;&emsp;&emsp;&emsp;model|1：动态（执行SQL挂载）2：静态（手动添加生命体）|integer||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;sqlContent|SQL查询语句|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"lifeSubtypeCommonCollectionVOList": [
			{
				"id": "",
				"levelId": "",
				"lifeIds": "",
				"model": 0,
				"name": "",
				"projectId": "",
				"sqlContent": ""
			}
		]
	}
}
```


## 分页根据集合id所属查询生命体


**接口地址**:`/life/subtype/common/queryLifeBySubtypeId`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "collectionId": "",
  "countId": "",
  "current": 0,
  "maxLimit": 0,
  "name": "",
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "records": [],
  "searchCount": true,
  "size": 0,
  "total": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeByCollectionQueryReq|通过集合id生命体分页查询|body|true|LifeByCollectionQueryReq|LifeByCollectionQueryReq|
|&emsp;&emsp;collectionId|||false|string||
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;name|||false|string||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«LifeDataQueryPageVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«LifeDataQueryPageVO»|IPage«LifeDataQueryPageVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|LifeDataQueryPageVO|
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡ID|string||
|&emsp;&emsp;&emsp;&emsp;lifeTemplateId|生命体模板ID|string||
|&emsp;&emsp;&emsp;&emsp;lifeTemplateName|生命体模板名称|string||
|&emsp;&emsp;&emsp;&emsp;lifeTemplateThumbnail|生命体模板缩略图|string||
|&emsp;&emsp;&emsp;&emsp;lockStatus|锁定状态|string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;type|类型|string||
|&emsp;&emsp;&emsp;&emsp;value|键值|object||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"id": "",
				"levelId": "",
				"lifeTemplateId": "",
				"lifeTemplateName": "",
				"lifeTemplateThumbnail": "",
				"lockStatus": "",
				"name": "",
				"projectId": "",
				"remark": "",
				"showStatus": "",
				"type": "",
				"value": {}
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 根据id修改生命体二级分类通用集合


**接口地址**:`/life/subtype/common/update`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "lifeIds": "",
  "model": 0,
  "name": "",
  "oldParentId": "",
  "projectId": "",
  "sqlContent": "",
  "sysTreeDTO": {
    "ancestralChain": "",
    "businessId": "",
    "businessPageId": "",
    "createBy": "",
    "createTime": "",
    "delFlag": "",
    "directParentId": "",
    "id": "",
    "labelsModel": "",
    "level": 0,
    "lft": 0,
    "lockStatus": "",
    "model": 0,
    "name": "",
    "oldId": "",
    "passId": "",
    "projectId": "",
    "remark": "",
    "rgt": 0,
    "sameLevelLastId": "",
    "seq": 0,
    "showStatus": "",
    "status": "",
    "tenantWorkId": "",
    "type": "",
    "updateBy": "",
    "updateTime": ""
  }
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSubtypeCommonCollectionSaveReq|新增生命体二级分类通用集合|body|true|lifeSubtypeCommonCollectionSaveReq|lifeSubtypeCommonCollectionSaveReq|
|&emsp;&emsp;id|生命体二级分类集合id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeIds|生命体ids，以逗号隔开||false|string||
|&emsp;&emsp;model|1：动态（执行SQL挂载）2：静态（手动添加生命体）||false|integer(int32)||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;oldParentId|旧父节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;sqlContent|SQL查询语句||false|string||
|&emsp;&emsp;sysTreeDTO|当前树根节点||false|SysTreeDTO|SysTreeDTO|
|&emsp;&emsp;&emsp;&emsp;ancestralChain|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessId|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessPageId|||false|string||
|&emsp;&emsp;&emsp;&emsp;createBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;createTime|||false|string||
|&emsp;&emsp;&emsp;&emsp;delFlag|||false|string||
|&emsp;&emsp;&emsp;&emsp;directParentId|||false|string||
|&emsp;&emsp;&emsp;&emsp;id|||false|string||
|&emsp;&emsp;&emsp;&emsp;labelsModel|||false|string||
|&emsp;&emsp;&emsp;&emsp;level|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lft|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;model|||false|integer||
|&emsp;&emsp;&emsp;&emsp;name|||false|string||
|&emsp;&emsp;&emsp;&emsp;oldId|||false|string||
|&emsp;&emsp;&emsp;&emsp;passId|||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|||false|string||
|&emsp;&emsp;&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;&emsp;&emsp;rgt|||false|integer||
|&emsp;&emsp;&emsp;&emsp;sameLevelLastId|||false|string||
|&emsp;&emsp;&emsp;&emsp;seq|||false|integer||
|&emsp;&emsp;&emsp;&emsp;showStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;status|||false|string||
|&emsp;&emsp;&emsp;&emsp;tenantWorkId|||false|string||
|&emsp;&emsp;&emsp;&emsp;type|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysWorkIndexVO»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysWorkIndexVO|SysWorkIndexVO|
|&emsp;&emsp;dirId||string||
|&emsp;&emsp;dirPath||string||
|&emsp;&emsp;lifeCount||integer(int32)||
|&emsp;&emsp;lockStatus||string||
|&emsp;&emsp;name||string||
|&emsp;&emsp;showStatus||string||
|&emsp;&emsp;sortIndex||integer(int32)||
|&emsp;&emsp;value||object||
|&emsp;&emsp;workId||string||
|&emsp;&emsp;workType||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"dirId": "",
		"dirPath": "",
		"lifeCount": 0,
		"lockStatus": "",
		"name": "",
		"showStatus": "",
		"sortIndex": 0,
		"value": {},
		"workId": "",
		"workType": ""
	}
}
```


# 生命体分类动态表管理


## 绑定id


**接口地址**:`/life-sort-dynamic/bindingId`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[
  {
    "businessId": "",
    "instanceId": "",
    "lifeSortId": ""
  }
]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDictDataList|lifeDictDataList|body|true|array|LifeSortBindReq|
|&emsp;&emsp;businessId|业务主键ID||false|string||
|&emsp;&emsp;instanceId|实例id||false|string||
|&emsp;&emsp;lifeSortId|生命体分类ID||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 引入生命体数据


**接口地址**:`/life-sort-dynamic/bringIn/{lifeSortId}`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDictDataList|lifeDictDataList|body|true|array|string|
|lifeSortId|lifeSortId|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 根据ids动态删除数据


**接口地址**:`/life-sort-dynamic/deleteDynamic`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|array|string|
|lifeSortId|lifeSortId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 根据id更新表结构


**接口地址**:`/life-sort-dynamic/doUpdateWork`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSortId|lifeSortId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 创建表结构


**接口地址**:`/life-sort-dynamic/doWork`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSortId|lifeSortId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 分页条件查询动态表


**接口地址**:`/life-sort-dynamic/queryDynamicPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSortId|lifeSortId|query|true|string||
|params|params|query|true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«object»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«object»|Page«object»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|object|
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


## 分页条件查询生命体分类动态表


**接口地址**:`/life-sort-dynamic/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|fieldName|字段名称|query|true|string||
|fieldType|字段类型|query|true|string||
|levelId|关卡id|query|true|string||
|lifeSortId|生命体分类ID|query|true|string||
|projectId|项目id|query|true|string||
|annotation|字段注释|query|false|string||
|current|起始页|query|false|integer(int64)||
|decimalPlace|小数点位数|query|false|integer(int32)||
|defaultValue|默认值|query|false|string||
|id|业务唯一id|query|false|string||
|name|表名称|query|false|string||
|parentId|父级id|query|false|string||
|parentNode|父节点|query|false|string||
|primaryKey|业务主建|query|false|string||
|required|是否必填|query|false|string||
|searchFlag|是否支持检索 0不支持、1支持|query|false|string||
|show|列表是否展示(0不展示、1展示)|query|false|string||
|size|每页条数|query|false|integer(int32)||
|sort|排序字段|query|false|string||
|update|是否更新|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«LifeSortDynamicTableRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«LifeSortDynamicTableRes»|Page«LifeSortDynamicTableRes»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|LifeSortDynamicTableRes|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释|string||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称|string||
|&emsp;&emsp;&emsp;&emsp;fieldNamePinYin|字段名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;lifeSortId|生命体分类ID|string||
|&emsp;&emsp;&emsp;&emsp;name|表名称|string||
|&emsp;&emsp;&emsp;&emsp;namePinYin|表名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;parentNode|父节点|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"annotation": "",
				"createBy": "",
				"createTime": "",
				"decimalPlace": 0,
				"defaultValue": "",
				"fieldName": "",
				"fieldNamePinYin": "",
				"fieldType": "",
				"id": "",
				"levelId": "",
				"lifeSortId": "",
				"name": "",
				"namePinYin": "",
				"parentNode": "",
				"primaryKey": "",
				"projectId": "",
				"required": "",
				"searchFlag": "",
				"show": "",
				"sort": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


## 根据ids动态更新数据【可级联更新生命体】


**接口地址**:`/life-sort-dynamic/updateDynamic`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "lifeSortId": "",
  "lifeTemplateId": "",
  "lockStatus": "",
  "name": "",
  "params": {},
  "remark": "",
  "showStatus": "",
  "type": "",
  "value": {}
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSortDynamicTableUpdateReq|生命体分类动态更新表|body|true|LifeSortDynamicTableUpdateReq|LifeSortDynamicTableUpdateReq|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;lifeSortId|生命体分类id||false|string||
|&emsp;&emsp;lifeTemplateId|生命体模板ID||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;name|生命体名称||false|string||
|&emsp;&emsp;params|动态表字段||false|object||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;type|生命体类型||false|string||
|&emsp;&emsp;value|键值||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


# 生命体分类管理


## 根据id返回生命体分类数据


**接口地址**:`/life-sort`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«LifeSortReq»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||LifeSortReq|LifeSortReq|
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;lifeSortDynamicList|数据结构|array|LifeSortDynamicTableRes|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释|string||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称|string||
|&emsp;&emsp;&emsp;&emsp;fieldNamePinYin|字段名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;lifeSortId|生命体分类ID|string||
|&emsp;&emsp;&emsp;&emsp;name|表名称|string||
|&emsp;&emsp;&emsp;&emsp;namePinYin|表名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;parentNode|父节点|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;parentId|父级节点id|string||
|&emsp;&emsp;projectId|项目id|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createTime": "",
		"id": "",
		"levelId": "",
		"lifeSortDynamicList": [
			{
				"annotation": "",
				"createBy": "",
				"createTime": "",
				"decimalPlace": 0,
				"defaultValue": "",
				"fieldName": "",
				"fieldNamePinYin": "",
				"fieldType": "",
				"id": "",
				"levelId": "",
				"lifeSortId": "",
				"name": "",
				"namePinYin": "",
				"parentNode": "",
				"primaryKey": "",
				"projectId": "",
				"required": "",
				"searchFlag": "",
				"show": "",
				"sort": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"name": "",
		"parentId": "",
		"projectId": ""
	}
}
```


## 添加生命体分类


**接口地址**:`/life-sort`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "levelId": "",
  "lifeSortDynamicList": [
    {
      "annotation": "",
      "current": 0,
      "decimalPlace": 0,
      "defaultValue": "",
      "fieldName": "",
      "fieldType": "",
      "id": "",
      "levelId": "",
      "lifeSortId": "",
      "name": "",
      "parentId": "",
      "parentNode": "",
      "primaryKey": "",
      "projectId": "",
      "required": "",
      "searchFlag": "",
      "show": "",
      "size": 0,
      "sort": "",
      "update": ""
    }
  ],
  "name": "",
  "parentId": "",
  "projectId": "",
  "size": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSortReq|生命体分类|body|true|LifeSortReq0|LifeSortReq0|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeSortDynamicList|数据结构||false|array|LifeSortDynamicTableReq|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释||false|string||
|&emsp;&emsp;&emsp;&emsp;current|起始页||false|integer||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数||false|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值||false|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称||false|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型||false|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;&emsp;&emsp;lifeSortId|生命体分类ID||false|string||
|&emsp;&emsp;&emsp;&emsp;name|表名称||false|string||
|&emsp;&emsp;&emsp;&emsp;parentId|父级id||false|string||
|&emsp;&emsp;&emsp;&emsp;parentNode|父节点||false|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填||false|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持||false|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)||false|string||
|&emsp;&emsp;&emsp;&emsp;size|每页条数||false|integer||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段||false|string||
|&emsp;&emsp;&emsp;&emsp;update|是否更新||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;parentId|父级节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«LifeSortReq»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||LifeSortReq|LifeSortReq|
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;lifeSortDynamicList|数据结构|array|LifeSortDynamicTableRes|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释|string||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称|string||
|&emsp;&emsp;&emsp;&emsp;fieldNamePinYin|字段名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;lifeSortId|生命体分类ID|string||
|&emsp;&emsp;&emsp;&emsp;name|表名称|string||
|&emsp;&emsp;&emsp;&emsp;namePinYin|表名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;parentNode|父节点|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;parentId|父级节点id|string||
|&emsp;&emsp;projectId|项目id|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createTime": "",
		"id": "",
		"levelId": "",
		"lifeSortDynamicList": [
			{
				"annotation": "",
				"createBy": "",
				"createTime": "",
				"decimalPlace": 0,
				"defaultValue": "",
				"fieldName": "",
				"fieldNamePinYin": "",
				"fieldType": "",
				"id": "",
				"levelId": "",
				"lifeSortId": "",
				"name": "",
				"namePinYin": "",
				"parentNode": "",
				"primaryKey": "",
				"projectId": "",
				"required": "",
				"searchFlag": "",
				"show": "",
				"sort": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"name": "",
		"parentId": "",
		"projectId": ""
	}
}
```


## 根据id更新生命体分类


**接口地址**:`/life-sort`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "levelId": "",
  "lifeSortDynamicList": [
    {
      "annotation": "",
      "current": 0,
      "decimalPlace": 0,
      "defaultValue": "",
      "fieldName": "",
      "fieldType": "",
      "id": "",
      "levelId": "",
      "lifeSortId": "",
      "name": "",
      "parentId": "",
      "parentNode": "",
      "primaryKey": "",
      "projectId": "",
      "required": "",
      "searchFlag": "",
      "show": "",
      "size": 0,
      "sort": "",
      "update": ""
    }
  ],
  "name": "",
  "parentId": "",
  "projectId": "",
  "size": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSortReq|生命体分类|body|true|LifeSortReq0|LifeSortReq0|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeSortDynamicList|数据结构||false|array|LifeSortDynamicTableReq|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释||false|string||
|&emsp;&emsp;&emsp;&emsp;current|起始页||false|integer||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数||false|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值||false|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称||false|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型||false|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;&emsp;&emsp;lifeSortId|生命体分类ID||false|string||
|&emsp;&emsp;&emsp;&emsp;name|表名称||false|string||
|&emsp;&emsp;&emsp;&emsp;parentId|父级id||false|string||
|&emsp;&emsp;&emsp;&emsp;parentNode|父节点||false|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填||false|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持||false|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)||false|string||
|&emsp;&emsp;&emsp;&emsp;size|每页条数||false|integer||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段||false|string||
|&emsp;&emsp;&emsp;&emsp;update|是否更新||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;parentId|父级节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«LifeSortReq»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||LifeSortReq|LifeSortReq|
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;lifeSortDynamicList|数据结构|array|LifeSortDynamicTableRes|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释|string||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称|string||
|&emsp;&emsp;&emsp;&emsp;fieldNamePinYin|字段名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;lifeSortId|生命体分类ID|string||
|&emsp;&emsp;&emsp;&emsp;name|表名称|string||
|&emsp;&emsp;&emsp;&emsp;namePinYin|表名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;parentNode|父节点|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;parentId|父级节点id|string||
|&emsp;&emsp;projectId|项目id|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createTime": "",
		"id": "",
		"levelId": "",
		"lifeSortDynamicList": [
			{
				"annotation": "",
				"createBy": "",
				"createTime": "",
				"decimalPlace": 0,
				"defaultValue": "",
				"fieldName": "",
				"fieldNamePinYin": "",
				"fieldType": "",
				"id": "",
				"levelId": "",
				"lifeSortId": "",
				"name": "",
				"namePinYin": "",
				"parentNode": "",
				"primaryKey": "",
				"projectId": "",
				"required": "",
				"searchFlag": "",
				"show": "",
				"sort": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"name": "",
		"parentId": "",
		"projectId": ""
	}
}
```


## 根据ids删除生命体分类


**接口地址**:`/life-sort`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|ids|ids列表|body|true|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«int»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||integer(int32)|integer(int32)|


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": 0
}
```


## 分页条件查询生命体分类


**接口地址**:`/life-sort/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|levelId|关卡id|query|true|string||
|lifeSortDynamicList[0].fieldName|字段名称|query|true|string||
|lifeSortDynamicList[0].fieldType|字段类型|query|true|string||
|lifeSortDynamicList[0].levelId|关卡id|query|true|string||
|lifeSortDynamicList[0].lifeSortId|生命体分类ID|query|true|string||
|lifeSortDynamicList[0].projectId|项目id|query|true|string||
|name|名称|query|true|string||
|parentId|父级节点id|query|true|string||
|projectId|项目id|query|true|string||
|current|起始页|query|false|integer(int64)||
|id|业务唯一id|query|false|string||
|lifeSortDynamicList[0].annotation|字段注释|query|false|string||
|lifeSortDynamicList[0].current|起始页|query|false|integer(int64)||
|lifeSortDynamicList[0].decimalPlace|小数点位数|query|false|integer(int32)||
|lifeSortDynamicList[0].defaultValue|默认值|query|false|string||
|lifeSortDynamicList[0].id|业务唯一id|query|false|string||
|lifeSortDynamicList[0].name|表名称|query|false|string||
|lifeSortDynamicList[0].parentId|父级id|query|false|string||
|lifeSortDynamicList[0].parentNode|父节点|query|false|string||
|lifeSortDynamicList[0].primaryKey|业务主建|query|false|string||
|lifeSortDynamicList[0].required|是否必填|query|false|string||
|lifeSortDynamicList[0].searchFlag|是否支持检索 0不支持、1支持|query|false|string||
|lifeSortDynamicList[0].show|列表是否展示(0不展示、1展示)|query|false|string||
|lifeSortDynamicList[0].size|每页条数|query|false|integer(int32)||
|lifeSortDynamicList[0].sort|排序字段|query|false|string||
|lifeSortDynamicList[0].update|是否更新|query|false|string||
|size|每页条数|query|false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«LifeSortReq»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«LifeSortReq»|Page«LifeSortReq»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|LifeSortReq|
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;lifeSortDynamicList|数据结构|array|LifeSortDynamicTableRes|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;annotation|字段注释|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;defaultValue|默认值|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;fieldName|字段名称|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;fieldNamePinYin|字段名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;fieldType|字段类型|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lifeSortId|生命体分类ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name|表名称|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;namePinYin|表名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;parentNode|父节点|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;required|是否必填|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;sort|排序字段|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;parentId|父级节点id|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"createTime": "",
				"id": "",
				"levelId": "",
				"lifeSortDynamicList": [
					{
						"annotation": "",
						"createBy": "",
						"createTime": "",
						"decimalPlace": 0,
						"defaultValue": "",
						"fieldName": "",
						"fieldNamePinYin": "",
						"fieldType": "",
						"id": "",
						"levelId": "",
						"lifeSortId": "",
						"name": "",
						"namePinYin": "",
						"parentNode": "",
						"primaryKey": "",
						"projectId": "",
						"required": "",
						"searchFlag": "",
						"show": "",
						"sort": "",
						"updateBy": "",
						"updateTime": ""
					}
				],
				"name": "",
				"parentId": "",
				"projectId": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


# 生命体数据


## 初始化,UE批量新增生命体


**接口地址**:`/life/data/batchSave`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "features": [
    {
      "list": [
        {
          "advancedlist": [],
          "base": {
            "category": "",
            "id": "",
            "name": ""
          },
          "command": {
            "acm_name": "",
            "acm_value": "",
            "advancedpage": "",
            "tag": ""
          },
          "transform": {
            "location": "",
            "rotation": "",
            "scale": ""
          }
        }
      ],
      "module": ""
    }
  ],
  "levelId": "",
  "projectId": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|listDictDataSaveReq|listDictDataSaveReq|body|true|ListDictDataSaveReq|ListDictDataSaveReq|
|&emsp;&emsp;features|||false|array|FeaturesVO|
|&emsp;&emsp;&emsp;&emsp;list|特性数据列表||false|array|FeaturesDataVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;advancedlist|||false|array|object|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;base|||false|BaseVO|BaseVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;category|类别||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name|名字||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;command|||false|CommandVO|CommandVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;acm_name|acm名称||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;acm_value|acm值||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;advancedpage|导前页||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;tag|标签||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;transform|||false|TransformVO|TransformVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;location|位置||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;rotation|旋转||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;scale|规模||false|string||
|&emsp;&emsp;&emsp;&emsp;module|模块||false|string||
|&emsp;&emsp;levelId|||true|string||
|&emsp;&emsp;projectId|||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 通过关卡id获取生命体各个分类的数量


**接口地址**:`/life/data/getLifeTypeCountListByLevelId`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|levelId|关卡id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«LifeTypeCountVO»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|LifeTypeCountVO|
|&emsp;&emsp;count|数量|integer(int32)||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;param|参数|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"count": 0,
			"name": "",
			"param": ""
		}
	]
}
```


## 根据id查询单个生命体基础信息


**接口地址**:`/life/data/getOneById`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|生命体id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«LifeDataVO»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||LifeDataVO|LifeDataVO|
|&emsp;&emsp;id|id|string||
|&emsp;&emsp;levelId|关卡ID|string||
|&emsp;&emsp;lifeTemplateId|生命体模板ID|string||
|&emsp;&emsp;lockStatus|锁定状态|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;type|类型|string||
|&emsp;&emsp;value|键值|object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"id": "",
		"levelId": "",
		"lifeTemplateId": "",
		"lockStatus": "",
		"name": "",
		"projectId": "",
		"remark": "",
		"showStatus": "",
		"type": "",
		"value": {}
	}
}
```


## 条件查询生命体


**接口地址**:`/life/data/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "lifeTemplateId": "",
  "name": "",
  "projectId": "",
  "remark": "",
  "type": "",
  "value": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDataQueryReq|生命体查询|body|true|LifeDataQueryReq|LifeDataQueryReq|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeTemplateId|生命体模板ID||false|string||
|&emsp;&emsp;name|生命体名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;type|生命体类型||false|string||
|&emsp;&emsp;value|键值||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«LifeDataQueryRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||LifeDataQueryRes|LifeDataQueryRes|
|&emsp;&emsp;lifeDataList||array|LifeDataVO|
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡ID|string||
|&emsp;&emsp;&emsp;&emsp;lifeTemplateId|生命体模板ID|string||
|&emsp;&emsp;&emsp;&emsp;lockStatus|锁定状态|string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;type|类型|string||
|&emsp;&emsp;&emsp;&emsp;value|键值|object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"lifeDataList": [
			{
				"id": "",
				"levelId": "",
				"lifeTemplateId": "",
				"lockStatus": "",
				"name": "",
				"projectId": "",
				"remark": "",
				"showStatus": "",
				"type": "",
				"value": {}
			}
		]
	}
}
```


## 通过sql语句查询生命体


**接口地址**:`/life/data/queryListBySqlStr`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "sqlStr": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeListQueryBySqlStrReq|通过sql语句查询生命体列表Req|body|true|LifeListQueryBySqlStrReq|LifeListQueryBySqlStrReq|
|&emsp;&emsp;sqlStr|sql字符串||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«LifeDataVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|LifeDataVO|
|&emsp;&emsp;id|id|string||
|&emsp;&emsp;levelId|关卡ID|string||
|&emsp;&emsp;lifeTemplateId|生命体模板ID|string||
|&emsp;&emsp;lockStatus|锁定状态|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;type|类型|string||
|&emsp;&emsp;value|键值|object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"id": "",
			"levelId": "",
			"lifeTemplateId": "",
			"lockStatus": "",
			"name": "",
			"projectId": "",
			"remark": "",
			"showStatus": "",
			"type": "",
			"value": {}
		}
	]
}
```


## 分页查询生命体


**接口地址**:`/life/data/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "countId": "",
  "current": 0,
  "id": "",
  "levelId": "",
  "lifeTemplateId": "",
  "lifeTemplateName": "",
  "maxLimit": 0,
  "name": "",
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "projectId": "",
  "records": [],
  "remark": "",
  "searchCount": true,
  "size": 0,
  "total": 0,
  "type": "",
  "value": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDataPageQueryReq|生命体分页查询|body|true|LifeDataPageQueryReq|LifeDataPageQueryReq|
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeTemplateId|生命体模板ID||false|string||
|&emsp;&emsp;lifeTemplateName|生命体模板名称||false|string||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;name|生命体名称||false|string||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||
|&emsp;&emsp;type|生命体类型||false|string||
|&emsp;&emsp;value|键值||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«LifeDataQueryPageVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«LifeDataQueryPageVO»|IPage«LifeDataQueryPageVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|LifeDataQueryPageVO|
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡ID|string||
|&emsp;&emsp;&emsp;&emsp;lifeTemplateId|生命体模板ID|string||
|&emsp;&emsp;&emsp;&emsp;lifeTemplateName|生命体模板名称|string||
|&emsp;&emsp;&emsp;&emsp;lifeTemplateThumbnail|生命体模板缩略图|string||
|&emsp;&emsp;&emsp;&emsp;lockStatus|锁定状态|string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;type|类型|string||
|&emsp;&emsp;&emsp;&emsp;value|键值|object||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"id": "",
				"levelId": "",
				"lifeTemplateId": "",
				"lifeTemplateName": "",
				"lifeTemplateThumbnail": "",
				"lockStatus": "",
				"name": "",
				"projectId": "",
				"remark": "",
				"showStatus": "",
				"type": "",
				"value": {}
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 根据id删除生命体


**接口地址**:`/life/data/removeById`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|生命体id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 新增生命体数据


**接口地址**:`/life/data/save`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "lifeTemplateId": "",
  "lockStatus": "",
  "name": "",
  "projectId": "",
  "remark": "",
  "showStatus": "",
  "type": "",
  "value": {}
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDataSaveReq|新增生命体|body|true|LifeDataSaveReq|LifeDataSaveReq|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeTemplateId|生命体模板ID||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;name|生命体名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;type|生命体类型||false|string||
|&emsp;&emsp;value|键值||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 初始化后,云端导出项目相关json


**接口地址**:`/life/data/serverExportJson`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|levelId|关卡ID|query|true|string||
|projectId|项目Id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«ProjectFeatureBO»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||ProjectFeatureBO|ProjectFeatureBO|
|&emsp;&emsp;features||array|FeaturesVO|
|&emsp;&emsp;&emsp;&emsp;list|特性数据列表|array|FeaturesDataVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;advancedlist||array|object|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;base||BaseVO|BaseVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;category|类别|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name|名字|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;command||CommandVO|CommandVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;acm_name|acm名称|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;acm_value|acm值|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;advancedpage|导前页|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;tag|标签|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;transform||TransformVO|TransformVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;location|位置|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;rotation|旋转|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;scale|规模|string||
|&emsp;&emsp;&emsp;&emsp;module|模块|string||
|&emsp;&emsp;levelid||string||
|&emsp;&emsp;projectid||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"features": [
			{
				"list": [
					{
						"advancedlist": [],
						"base": {
							"category": "",
							"id": "",
							"name": ""
						},
						"command": {
							"acm_name": "",
							"acm_value": "",
							"advancedpage": "",
							"tag": ""
						},
						"transform": {
							"location": "",
							"rotation": "",
							"scale": ""
						}
					}
				],
				"module": ""
			}
		],
		"levelid": "",
		"projectid": ""
	}
}
```


## 根据id更新生命体


**接口地址**:`/life/data/updateById`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "lifeTemplateId": "",
  "lockStatus": "",
  "name": "",
  "projectId": "",
  "remark": "",
  "showStatus": "",
  "type": "",
  "value": {}
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDataUpdateReq|更新生命体|body|true|LifeDataUpdateReq|LifeDataUpdateReq|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeTemplateId|生命体模板ID||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0正常 1锁定 ）||false|string||
|&emsp;&emsp;name|生命体名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;type|生命体类型||false|string||
|&emsp;&emsp;value|键值||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


# 生命体数据模板


## 批量导入生命体模板


**接口地址**:`/life/template/batchImport`


**请求方式**:`POST`


**请求数据类型**:`multipart/form-data`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|file|缩略图文件|query|true|file||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 批量解析txt文件的json体入库


**接口地址**:`/life/template/batchReadFileListSinkDb`


**请求方式**:`POST`


**请求数据类型**:`application/json,multipart/form-data`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|bizType|bizType|query|true|string||
|textureFileList||formData|false|array|file|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 初始化批量替换生命体模板


**接口地址**:`/life/template/initBatchReplace`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[
  {
    "subtype": "",
    "texture": "",
    "title": "",
    "type": "",
    "value": {
      "content": "",
      "module": "",
      "value": {
        "advancedlist": [],
        "base": {
          "category": "",
          "id": "",
          "name": ""
        },
        "command": {
          "acm_name": "",
          "acm_value": "",
          "advancedpage": "",
          "tag": ""
        },
        "transform": {
          "location": "",
          "rotation": "",
          "scale": ""
        }
      }
    }
  }
]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeTemReqList|批量替换生命体请求体|body|true|array|LifeTemReq|
|&emsp;&emsp;subtype|||false|string||
|&emsp;&emsp;texture|||false|string||
|&emsp;&emsp;title|||false|string||
|&emsp;&emsp;type|||false|string||
|&emsp;&emsp;value|||false|LifeTemOutValueVO|LifeTemOutValueVO|
|&emsp;&emsp;&emsp;&emsp;content|||false|string||
|&emsp;&emsp;&emsp;&emsp;module|||false|string||
|&emsp;&emsp;&emsp;&emsp;value|||false|LifeTemValueVO|LifeTemValueVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;advancedlist|||false|array|object|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;base|||false|LifeTemBaseVO|LifeTemBaseVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;category|种类||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id|生命体id||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;command|||false|LifeTemCommandVO|LifeTemCommandVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;acm_name|模块名称||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;acm_value|命令||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;advancedpage|属性页||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;tag|标签||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;transform|||false|LifeTemTransformVO|LifeTemTransformVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;location|位置||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;rotation|旋转||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;scale|缩放||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 初始化新增预制


**接口地址**:`/life/template/insertPre`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "bizType": "",
  "industrySecondTypeIndex": "",
  "industryTypeIndex": "",
  "json": {
    "content": "",
    "module": "",
    "value": {
      "advancedlist": [],
      "base": {
        "category": "",
        "id": "",
        "name": ""
      },
      "command": {
        "acm_name": "",
        "acm_value": "",
        "advancedpage": "",
        "tag": ""
      },
      "transform": {
        "location": "",
        "rotation": "",
        "scale": ""
      }
    }
  },
  "materialTypeIndex": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|listDictDataSaveReq|listDictDataSaveReq|body|true|LifeDictDataTemplatePreSaveReq|LifeDictDataTemplatePreSaveReq|
|&emsp;&emsp;bizType|0：商城库 1：族库||false|string||
|&emsp;&emsp;industrySecondTypeIndex|行业二级类型索引||false|string||
|&emsp;&emsp;industryTypeIndex|行业一级类型索引||false|string||
|&emsp;&emsp;json|json体||false|LifeDictDataTemplateJsonPreSaveReq|LifeDictDataTemplateJsonPreSaveReq|
|&emsp;&emsp;&emsp;&emsp;content|||false|string||
|&emsp;&emsp;&emsp;&emsp;module|||true|string||
|&emsp;&emsp;&emsp;&emsp;value|||false|TemplateFeaturesDataVO|TemplateFeaturesDataVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;advancedlist|||false|array|object|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;base|||false|BaseVO|BaseVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;category|类别||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name|名字||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;command|||false|CommandVO|CommandVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;acm_name|acm名称||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;acm_value|acm值||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;advancedpage|导前页||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;tag|标签||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;transform|||false|TransformVO|TransformVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;location|位置||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;rotation|旋转||false|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;scale|规模||false|string||
|&emsp;&emsp;materialTypeIndex|素材类型索引||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 条件查询预制的生命体模板


**接口地址**:`/life/template/queryList`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "bizType": "",
  "id": "",
  "industrySecondTypeIndex": "",
  "industryTypeIndex": "",
  "isAsc": "",
  "lockStatus": "",
  "materialTypeIndex": "",
  "name": "",
  "orderByColumn": "",
  "pageNum": 0,
  "pageSize": 0,
  "remark": "",
  "showStatus": "",
  "thumbnail": "",
  "type": "",
  "ueThumbnailPath": "",
  "value": {}
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDictDataTemplateSaveReq|新增生命体模板|body|true|LifeDictDataTemplateSaveReq|LifeDictDataTemplateSaveReq|
|&emsp;&emsp;bizType|0：商城库 1：族库||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;industrySecondTypeIndex|行业二级类型索引||false|string||
|&emsp;&emsp;industryTypeIndex|行业一级类型索引||false|string||
|&emsp;&emsp;isAsc|||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;materialTypeIndex|素材类型索引||false|string||
|&emsp;&emsp;name|生名称||false|string||
|&emsp;&emsp;orderByColumn|||false|string||
|&emsp;&emsp;pageNum|||false|integer(int32)||
|&emsp;&emsp;pageSize|||false|integer(int32)||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;thumbnail|缩略图||false|string||
|&emsp;&emsp;type|一级类型||false|string||
|&emsp;&emsp;ueThumbnailPath|UE缩略图路径||false|string||
|&emsp;&emsp;value|键值||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«LifeDictDataTemplateVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|LifeDictDataTemplateVO|
|&emsp;&emsp;bizType|0：商城库 1：族库|string||
|&emsp;&emsp;id|id|string||
|&emsp;&emsp;industrySecondTypeIndex|行业二级类型索引|string||
|&emsp;&emsp;industryTypeIndex|行业一级类型索引|string||
|&emsp;&emsp;lastUpdateStructureTime|value结构最新更新时间|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）|string||
|&emsp;&emsp;materialTypeIndex|素材类型索引下标|string||
|&emsp;&emsp;name|生命体名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）|string||
|&emsp;&emsp;thumbnail|缩略图|string||
|&emsp;&emsp;thumbnailName|缩略图名称|string||
|&emsp;&emsp;type|生命体类型|string||
|&emsp;&emsp;ueThumbnailPath|UE缩略图路径|string||
|&emsp;&emsp;value|键值|object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"bizType": "",
			"id": "",
			"industrySecondTypeIndex": "",
			"industryTypeIndex": "",
			"lastUpdateStructureTime": "",
			"lockStatus": "",
			"materialTypeIndex": "",
			"name": "",
			"remark": "",
			"showStatus": "",
			"thumbnail": "",
			"thumbnailName": "",
			"type": "",
			"ueThumbnailPath": "",
			"value": {}
		}
	]
}
```


## 根据id查询单个生命体


**接口地址**:`/life/template/queryOneById`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|生命体模板id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«LifeDictDataTemplateVO»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||LifeDictDataTemplateVO|LifeDictDataTemplateVO|
|&emsp;&emsp;bizType|0：商城库 1：族库|string||
|&emsp;&emsp;id|id|string||
|&emsp;&emsp;industrySecondTypeIndex|行业二级类型索引|string||
|&emsp;&emsp;industryTypeIndex|行业一级类型索引|string||
|&emsp;&emsp;lastUpdateStructureTime|value结构最新更新时间|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）|string||
|&emsp;&emsp;materialTypeIndex|素材类型索引下标|string||
|&emsp;&emsp;name|生命体名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）|string||
|&emsp;&emsp;thumbnail|缩略图|string||
|&emsp;&emsp;thumbnailName|缩略图名称|string||
|&emsp;&emsp;type|生命体类型|string||
|&emsp;&emsp;ueThumbnailPath|UE缩略图路径|string||
|&emsp;&emsp;value|键值|object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"bizType": "",
		"id": "",
		"industrySecondTypeIndex": "",
		"industryTypeIndex": "",
		"lastUpdateStructureTime": "",
		"lockStatus": "",
		"materialTypeIndex": "",
		"name": "",
		"remark": "",
		"showStatus": "",
		"thumbnail": "",
		"thumbnailName": "",
		"type": "",
		"ueThumbnailPath": "",
		"value": {}
	}
}
```


## 分页查询预制的生命体模板


**接口地址**:`/life/template/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "bizType": "",
  "id": "",
  "industrySecondTypeIndex": "",
  "industryTypeIndex": "",
  "isAsc": "",
  "lockStatus": "",
  "materialTypeIndex": "",
  "name": "",
  "orderByColumn": "",
  "pageNum": 0,
  "pageSize": 0,
  "remark": "",
  "showStatus": "",
  "thumbnail": "",
  "type": "",
  "ueThumbnailPath": "",
  "value": {}
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDictDataTemplateSaveReq|新增生命体模板|body|true|LifeDictDataTemplateSaveReq|LifeDictDataTemplateSaveReq|
|&emsp;&emsp;bizType|0：商城库 1：族库||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;industrySecondTypeIndex|行业二级类型索引||false|string||
|&emsp;&emsp;industryTypeIndex|行业一级类型索引||false|string||
|&emsp;&emsp;isAsc|||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;materialTypeIndex|素材类型索引||false|string||
|&emsp;&emsp;name|生名称||false|string||
|&emsp;&emsp;orderByColumn|||false|string||
|&emsp;&emsp;pageNum|||false|integer(int32)||
|&emsp;&emsp;pageSize|||false|integer(int32)||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;thumbnail|缩略图||false|string||
|&emsp;&emsp;type|一级类型||false|string||
|&emsp;&emsp;ueThumbnailPath|UE缩略图路径||false|string||
|&emsp;&emsp;value|键值||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«LifeDictDataTemplateVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«LifeDictDataTemplateVO»|IPage«LifeDictDataTemplateVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|LifeDictDataTemplateVO|
|&emsp;&emsp;&emsp;&emsp;bizType|0：商城库 1：族库|string||
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;industrySecondTypeIndex|行业二级类型索引|string||
|&emsp;&emsp;&emsp;&emsp;industryTypeIndex|行业一级类型索引|string||
|&emsp;&emsp;&emsp;&emsp;lastUpdateStructureTime|value结构最新更新时间|string||
|&emsp;&emsp;&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）|string||
|&emsp;&emsp;&emsp;&emsp;materialTypeIndex|素材类型索引下标|string||
|&emsp;&emsp;&emsp;&emsp;name|生命体名称|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）|string||
|&emsp;&emsp;&emsp;&emsp;thumbnail|缩略图|string||
|&emsp;&emsp;&emsp;&emsp;thumbnailName|缩略图名称|string||
|&emsp;&emsp;&emsp;&emsp;type|生命体类型|string||
|&emsp;&emsp;&emsp;&emsp;ueThumbnailPath|UE缩略图路径|string||
|&emsp;&emsp;&emsp;&emsp;value|键值|object||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"bizType": "",
				"id": "",
				"industrySecondTypeIndex": "",
				"industryTypeIndex": "",
				"lastUpdateStructureTime": "",
				"lockStatus": "",
				"materialTypeIndex": "",
				"name": "",
				"remark": "",
				"showStatus": "",
				"thumbnail": "",
				"thumbnailName": "",
				"type": "",
				"ueThumbnailPath": "",
				"value": {}
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 根据id删除预制的生命体模板


**接口地址**:`/life/template/removeById`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|生命体模板id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 新增生命体数据模板


**接口地址**:`/life/template/save`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "bizType": "",
  "id": "",
  "industrySecondTypeIndex": "",
  "industryTypeIndex": "",
  "isAsc": "",
  "lockStatus": "",
  "materialTypeIndex": "",
  "name": "",
  "orderByColumn": "",
  "pageNum": 0,
  "pageSize": 0,
  "remark": "",
  "showStatus": "",
  "thumbnail": "",
  "type": "",
  "ueThumbnailPath": "",
  "value": {}
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDictDataTemplateSaveReq|新增生命体模板|body|true|LifeDictDataTemplateSaveReq|LifeDictDataTemplateSaveReq|
|&emsp;&emsp;bizType|0：商城库 1：族库||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;industrySecondTypeIndex|行业二级类型索引||false|string||
|&emsp;&emsp;industryTypeIndex|行业一级类型索引||false|string||
|&emsp;&emsp;isAsc|||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;materialTypeIndex|素材类型索引||false|string||
|&emsp;&emsp;name|生名称||false|string||
|&emsp;&emsp;orderByColumn|||false|string||
|&emsp;&emsp;pageNum|||false|integer(int32)||
|&emsp;&emsp;pageSize|||false|integer(int32)||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;thumbnail|缩略图||false|string||
|&emsp;&emsp;type|一级类型||false|string||
|&emsp;&emsp;ueThumbnailPath|UE缩略图路径||false|string||
|&emsp;&emsp;value|键值||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id更新预制的生命体模板,并同步数据结构给生命体实例


**接口地址**:`/life/template/updateAndSynchronizeJsonStructureById`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "bizType": "",
  "id": "",
  "industrySecondTypeIndex": "",
  "industryTypeIndex": "",
  "isAsc": "",
  "lockStatus": "",
  "materialTypeIndex": "",
  "name": "",
  "orderByColumn": "",
  "pageNum": 0,
  "pageSize": 0,
  "remark": "",
  "showStatus": "",
  "thumbnail": "",
  "type": "",
  "ueThumbnailPath": "",
  "value": {}
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDictDataTemplateSaveReq|新增生命体模板|body|true|LifeDictDataTemplateSaveReq|LifeDictDataTemplateSaveReq|
|&emsp;&emsp;bizType|0：商城库 1：族库||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;industrySecondTypeIndex|行业二级类型索引||false|string||
|&emsp;&emsp;industryTypeIndex|行业一级类型索引||false|string||
|&emsp;&emsp;isAsc|||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;materialTypeIndex|素材类型索引||false|string||
|&emsp;&emsp;name|生名称||false|string||
|&emsp;&emsp;orderByColumn|||false|string||
|&emsp;&emsp;pageNum|||false|integer(int32)||
|&emsp;&emsp;pageSize|||false|integer(int32)||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;thumbnail|缩略图||false|string||
|&emsp;&emsp;type|一级类型||false|string||
|&emsp;&emsp;ueThumbnailPath|UE缩略图路径||false|string||
|&emsp;&emsp;value|键值||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 根据id更新预制的生命体模板


**接口地址**:`/life/template/updateById`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "bizType": "",
  "id": "",
  "industrySecondTypeIndex": "",
  "industryTypeIndex": "",
  "isAsc": "",
  "lockStatus": "",
  "materialTypeIndex": "",
  "name": "",
  "orderByColumn": "",
  "pageNum": 0,
  "pageSize": 0,
  "remark": "",
  "showStatus": "",
  "thumbnail": "",
  "type": "",
  "ueThumbnailPath": "",
  "value": {}
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDictDataTemplateSaveReq|新增生命体模板|body|true|LifeDictDataTemplateSaveReq|LifeDictDataTemplateSaveReq|
|&emsp;&emsp;bizType|0：商城库 1：族库||false|string||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;industrySecondTypeIndex|行业二级类型索引||false|string||
|&emsp;&emsp;industryTypeIndex|行业一级类型索引||false|string||
|&emsp;&emsp;isAsc|||false|string||
|&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）||false|string||
|&emsp;&emsp;materialTypeIndex|素材类型索引||false|string||
|&emsp;&emsp;name|生名称||false|string||
|&emsp;&emsp;orderByColumn|||false|string||
|&emsp;&emsp;pageNum|||false|integer(int32)||
|&emsp;&emsp;pageSize|||false|integer(int32)||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）||false|string||
|&emsp;&emsp;thumbnail|缩略图||false|string||
|&emsp;&emsp;type|一级类型||false|string||
|&emsp;&emsp;ueThumbnailPath|UE缩略图路径||false|string||
|&emsp;&emsp;value|键值||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 上传生命体模板缩略图


**接口地址**:`/life/template/uploadThumbnail`


**请求方式**:`POST`


**请求数据类型**:`multipart/form-data`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|file|缩略图文件|query|true|file||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«string»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": ""
}
```


# 生命体数据模板结构修改记录


## 分页查询


**接口地址**:`/life/templateStructureChangeRecord/page`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "countId": "",
  "current": 0,
  "maxLimit": 0,
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "records": [],
  "searchCount": true,
  "size": 0,
  "total": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeDictDataTemplateStructureChangeRecordPageReq|生命体模板结构修改记录分页请求体|body|true|LifeDictDataTemplateStructureChangeRecordPageReq|LifeDictDataTemplateStructureChangeRecordPageReq|
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«LifeDictDataTemplateStructureChangeRecordVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«LifeDictDataTemplateStructureChangeRecordVO»|IPage«LifeDictDataTemplateStructureChangeRecordVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|LifeDictDataTemplateStructureChangeRecordVO|
|&emsp;&emsp;&emsp;&emsp;afterValue|修改后结构|object||
|&emsp;&emsp;&emsp;&emsp;befValue|修改前结构|object||
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;lifeTemplateId|生命体模板id|string||
|&emsp;&emsp;&emsp;&emsp;lockStatus|锁定状态（0不锁定 1锁定）|string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|显隐状态（0显示 1隐藏 ）|string||
|&emsp;&emsp;&emsp;&emsp;thumbnail|缩略图|string||
|&emsp;&emsp;&emsp;&emsp;thumbnailName|缩略图名称|string||
|&emsp;&emsp;&emsp;&emsp;type|类型|string||
|&emsp;&emsp;&emsp;&emsp;ueThumbnailPath|UE缩略图路径|string||
|&emsp;&emsp;&emsp;&emsp;updateStructureTime|结构更新时间|string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"afterValue": {},
				"befValue": {},
				"id": "",
				"lifeTemplateId": "",
				"lockStatus": "",
				"name": "",
				"remark": "",
				"showStatus": "",
				"thumbnail": "",
				"thumbnailName": "",
				"type": "",
				"ueThumbnailPath": "",
				"updateStructureTime": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


# 生命体材质字典数据


## 删除孪生体材质类型字典


**接口地址**:`/life/materialTypeDictData/delete`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeMaterialTypeDictDataDeleteReq|孪生体素材类型字典删除Req|body|true|LifeMaterialTypeDictDataDeleteReq|LifeMaterialTypeDictDataDeleteReq|
|&emsp;&emsp;id|id||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 条件查询孪生体材质类型字典


**接口地址**:`/life/materialTypeDictData/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeMaterialTypeDictDataQueryReq|孪生体素材类型字典查询|body|true|LifeMaterialTypeDictDataQueryReq|LifeMaterialTypeDictDataQueryReq|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|行业名称||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«LifeMaterialTypeDictDataListQueryRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||LifeMaterialTypeDictDataListQueryRes|LifeMaterialTypeDictDataListQueryRes|
|&emsp;&emsp;lifeMaterialTypeDictDataList||array|LifeMaterialTypeDictDataVO|
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;name|材质类型名字|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"lifeMaterialTypeDictDataList": [
			{
				"id": "",
				"name": ""
			}
		]
	}
}
```


## 新增孪生体材质类型字典


**接口地址**:`/life/materialTypeDictData/save`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeMaterialTypeDictDataReq|孪生体素材类型字典查询|body|true|LifeMaterialTypeDictDataQueryReq|LifeMaterialTypeDictDataQueryReq|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|行业名称||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 通过id更新孪生体材质类型字典


**接口地址**:`/life/materialTypeDictData/updateById`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeMaterialTypeDictDataUpdateReq|孪生体素材类型字典更新Req|body|true|LifeMaterialTypeDictDataUpdateReq|LifeMaterialTypeDictDataUpdateReq|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|行业名称||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


# 用户权限关联表对象功能接口


## 根据id查询数据


**接口地址**:`/sysUserRole`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysUserRoleRes»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysUserRoleRes|SysUserRoleRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;roleId|角色id|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;userId|用户id|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"id": "",
		"roleId": "",
		"updateBy": "",
		"updateTime": "",
		"userId": ""
	}
}
```


## 添加数据


**接口地址**:`/sysUserRole`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "roleId": "",
  "size": 0,
  "userId": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysUserRoleReq|用户权限关联表|body|true|SysUserRoleReq|SysUserRoleReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;roleId|角色id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;userId|用户id||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysUserRoleRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysUserRoleRes|SysUserRoleRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;roleId|角色id|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;userId|用户id|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"id": "",
		"roleId": "",
		"updateBy": "",
		"updateTime": "",
		"userId": ""
	}
}
```


## 根据id更新数据


**接口地址**:`/sysUserRole`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "roleId": "",
  "size": 0,
  "userId": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysUserRoleReq|用户权限关联表|body|true|SysUserRoleReq|SysUserRoleReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;roleId|角色id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;userId|用户id||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysUserRoleRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysUserRoleRes|SysUserRoleRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;roleId|角色id|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;userId|用户id|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"id": "",
		"roleId": "",
		"updateBy": "",
		"updateTime": "",
		"userId": ""
	}
}
```


## 根据ids删除数据


**接口地址**:`/sysUserRole`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|ids|ids列表|body|true|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«int»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||integer(int32)|integer(int32)|


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": 0
}
```


## 取消授权


**接口地址**:`/sysUserRole/cancelAuth`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "roleId": "",
  "userIds": []
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|cancelAuthReq|取消授权|body|true|CancelAuthReq|CancelAuthReq|
|&emsp;&emsp;roleId|角色id||false|string||
|&emsp;&emsp;userIds|用户ids||false|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 分页条件查询数据


**接口地址**:`/sysUserRole/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "roleId": "",
  "size": 0,
  "userId": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysUserRoleReq|用户权限关联表|body|true|SysUserRoleReq|SysUserRoleReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;roleId|角色id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;userId|用户id||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«SysUserRoleRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«SysUserRoleRes»|Page«SysUserRoleRes»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SysUserRoleRes|
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;roleId|角色id|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;&emsp;&emsp;userId|用户id|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"createBy": "",
				"createTime": "",
				"id": "",
				"roleId": "",
				"updateBy": "",
				"updateTime": "",
				"userId": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


## 批量添加数据


**接口地址**:`/sysUserRole/saveBatch`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "roleId": "",
  "userIds": []
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|cancelAuthReq|取消授权|body|true|CancelAuthReq|CancelAuthReq|
|&emsp;&emsp;roleId|角色id||false|string||
|&emsp;&emsp;userIds|用户ids||false|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


# 用户管理


## 根据id查询用户


**接口地址**:`/sysUser`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|userId|用户id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«UserDTO»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||UserDTO|UserDTO|
|&emsp;&emsp;allocated|绑定（true绑定、false未绑定）|boolean||
|&emsp;&emsp;avatar|用户头像|string||
|&emsp;&emsp;beginTime|开始时间|string(date-time)||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;current|起始页|integer(int64)||
|&emsp;&emsp;email|用户邮箱|string||
|&emsp;&emsp;endTime|结束时间|string(date-time)||
|&emsp;&emsp;gender|用户性别|string||
|&emsp;&emsp;id|唯一id|integer(int64)||
|&emsp;&emsp;loginDate|最近登录时间|string(date-time)||
|&emsp;&emsp;nickname|用户昵称|string||
|&emsp;&emsp;password|用户密码|string||
|&emsp;&emsp;phoneNumber|手机号码|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;roleId|角色id|array|string|
|&emsp;&emsp;size|每页条数|integer(int32)||
|&emsp;&emsp;status|用户状态（0停用、1正常）|string||
|&emsp;&emsp;username|用户账号|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"allocated": true,
		"avatar": "",
		"beginTime": "",
		"createTime": "",
		"current": 0,
		"email": "",
		"endTime": "",
		"gender": "",
		"id": 0,
		"loginDate": "",
		"nickname": "",
		"password": "",
		"phoneNumber": "",
		"remark": "",
		"roleId": [],
		"size": 0,
		"status": "",
		"username": ""
	}
}
```


## 添加用户


**接口地址**:`/sysUser`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "allocated": true,
  "avatar": "",
  "beginTime": "",
  "createTime": "",
  "current": 0,
  "email": "",
  "endTime": "",
  "gender": "",
  "id": 0,
  "loginDate": "",
  "nickname": "",
  "password": "",
  "phoneNumber": "",
  "remark": "",
  "roleId": [],
  "size": 0,
  "status": "",
  "username": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|userDto|userDto|body|true|UserDTO|UserDTO|
|&emsp;&emsp;allocated|绑定（true绑定、false未绑定）||false|boolean||
|&emsp;&emsp;avatar|用户头像||false|string||
|&emsp;&emsp;beginTime|开始时间||false|string(date-time)||
|&emsp;&emsp;createTime|创建时间||false|string(date-time)||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;email|用户邮箱||false|string||
|&emsp;&emsp;endTime|结束时间||false|string(date-time)||
|&emsp;&emsp;gender|用户性别||false|string||
|&emsp;&emsp;id|唯一id||false|integer(int64)||
|&emsp;&emsp;loginDate|最近登录时间||false|string(date-time)||
|&emsp;&emsp;nickname|用户昵称||false|string||
|&emsp;&emsp;password|用户密码||false|string||
|&emsp;&emsp;phoneNumber|手机号码||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;roleId|角色id||false|array|string|
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;status|用户状态（0停用、1正常）||false|string||
|&emsp;&emsp;username|用户账号||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 根据id更新用户


**接口地址**:`/sysUser`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "allocated": true,
  "avatar": "",
  "beginTime": "",
  "createTime": "",
  "current": 0,
  "email": "",
  "endTime": "",
  "gender": "",
  "id": 0,
  "loginDate": "",
  "nickname": "",
  "password": "",
  "phoneNumber": "",
  "remark": "",
  "roleId": [],
  "size": 0,
  "status": "",
  "username": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|userDto|userDto|body|true|UserDTO|UserDTO|
|&emsp;&emsp;allocated|绑定（true绑定、false未绑定）||false|boolean||
|&emsp;&emsp;avatar|用户头像||false|string||
|&emsp;&emsp;beginTime|开始时间||false|string(date-time)||
|&emsp;&emsp;createTime|创建时间||false|string(date-time)||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;email|用户邮箱||false|string||
|&emsp;&emsp;endTime|结束时间||false|string(date-time)||
|&emsp;&emsp;gender|用户性别||false|string||
|&emsp;&emsp;id|唯一id||false|integer(int64)||
|&emsp;&emsp;loginDate|最近登录时间||false|string(date-time)||
|&emsp;&emsp;nickname|用户昵称||false|string||
|&emsp;&emsp;password|用户密码||false|string||
|&emsp;&emsp;phoneNumber|手机号码||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;roleId|角色id||false|array|string|
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;status|用户状态（0停用、1正常）||false|string||
|&emsp;&emsp;username|用户账号||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 根据id删除用户


**接口地址**:`/sysUser`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|ids|ids|body|true|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 根据当前登入人获取用户信息


**接口地址**:`/sysUser/queryCurrentUserInfo`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 分页条件查询数据


**接口地址**:`/sysUser/queryUser`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "allocated": true,
  "avatar": "",
  "beginTime": "",
  "createTime": "",
  "current": 0,
  "email": "",
  "endTime": "",
  "gender": "",
  "id": 0,
  "loginDate": "",
  "nickname": "",
  "password": "",
  "phoneNumber": "",
  "remark": "",
  "roleId": [],
  "size": 0,
  "status": "",
  "username": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|userDto|userDto|body|true|UserDTO|UserDTO|
|&emsp;&emsp;allocated|绑定（true绑定、false未绑定）||false|boolean||
|&emsp;&emsp;avatar|用户头像||false|string||
|&emsp;&emsp;beginTime|开始时间||false|string(date-time)||
|&emsp;&emsp;createTime|创建时间||false|string(date-time)||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;email|用户邮箱||false|string||
|&emsp;&emsp;endTime|结束时间||false|string(date-time)||
|&emsp;&emsp;gender|用户性别||false|string||
|&emsp;&emsp;id|唯一id||false|integer(int64)||
|&emsp;&emsp;loginDate|最近登录时间||false|string(date-time)||
|&emsp;&emsp;nickname|用户昵称||false|string||
|&emsp;&emsp;password|用户密码||false|string||
|&emsp;&emsp;phoneNumber|手机号码||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;roleId|角色id||false|array|string|
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;status|用户状态（0停用、1正常）||false|string||
|&emsp;&emsp;username|用户账号||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«UserDTO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«UserDTO»|Page«UserDTO»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|UserDTO|
|&emsp;&emsp;&emsp;&emsp;allocated|绑定（true绑定、false未绑定）|boolean||
|&emsp;&emsp;&emsp;&emsp;avatar|用户头像|string||
|&emsp;&emsp;&emsp;&emsp;beginTime|开始时间|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;current|起始页|integer||
|&emsp;&emsp;&emsp;&emsp;email|用户邮箱|string||
|&emsp;&emsp;&emsp;&emsp;endTime|结束时间|string||
|&emsp;&emsp;&emsp;&emsp;gender|用户性别|string||
|&emsp;&emsp;&emsp;&emsp;id|唯一id|integer||
|&emsp;&emsp;&emsp;&emsp;loginDate|最近登录时间|string||
|&emsp;&emsp;&emsp;&emsp;nickname|用户昵称|string||
|&emsp;&emsp;&emsp;&emsp;password|用户密码|string||
|&emsp;&emsp;&emsp;&emsp;phoneNumber|手机号码|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;roleId|角色id|array|string|
|&emsp;&emsp;&emsp;&emsp;size|每页条数|integer||
|&emsp;&emsp;&emsp;&emsp;status|用户状态（0停用、1正常）|string||
|&emsp;&emsp;&emsp;&emsp;username|用户账号|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"allocated": true,
				"avatar": "",
				"beginTime": "",
				"createTime": "",
				"current": 0,
				"email": "",
				"endTime": "",
				"gender": "",
				"id": 0,
				"loginDate": "",
				"nickname": "",
				"password": "",
				"phoneNumber": "",
				"remark": "",
				"roleId": [],
				"size": 0,
				"status": "",
				"username": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


# 登录管理


## 账户密码登录


**接口地址**:`/login/password`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|password|用户密码|query|true|string||
|username|用户名称|query|true|string||
|captchaFlag|验证码是否开启|query|false|boolean||
|code|验证码|query|false|string||
|uuid|唯一标识|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«string»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": ""
}
```


# 空间分类动态表管理


## 删除数据根据id


**接口地址**:`/space-sort-dynamic/deleteDynamic`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|params|params|body|true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«object»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 根据id更新表结构


**接口地址**:`/space-sort-dynamic/doUpdateWork`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|spaceSortId|spaceSortId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 创建表结构


**接口地址**:`/space-sort-dynamic/doWork`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|spaceSortId|spaceSortId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 分页条件查询动态表


**接口地址**:`/space-sort-dynamic/queryDynamicPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|params|params|body|true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«object»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«object»|Page«object»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|object|
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


## 根据层级获取父级数据列表


**接口地址**:`/space-sort-dynamic/queryLevelList`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "level": "",
  "levelId": "",
  "name": "",
  "projectId": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|spaceSortLevelReq|空间分类父级查询|body|true|SpaceSortLevelReq|SpaceSortLevelReq|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;level|层级||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;type|类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«SpaceSortTreeRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|SpaceSortTreeRes|
|&emsp;&emsp;children|子节点|array|SpaceSortTreeRes|
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;levelName|层级名称|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;parent|父级id|string||
|&emsp;&emsp;type|类型|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"children": [
				{
					"children": [
						{}
					],
					"id": "",
					"levelName": "",
					"name": "",
					"parent": "",
					"type": ""
				}
			],
			"id": "",
			"levelName": "",
			"name": "",
			"parent": "",
			"type": ""
		}
	]
}
```


## 分页条件查询空间体分类动态表


**接口地址**:`/space-sort-dynamic/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "annotation": "",
  "current": 0,
  "decimalPlace": 0,
  "defaultValue": "",
  "fieldName": "",
  "fieldType": "",
  "id": "",
  "levelId": "",
  "primaryKey": "",
  "projectId": "",
  "required": "",
  "searchFlag": "",
  "show": "",
  "size": 0,
  "sort": "",
  "spaceSortId": "",
  "update": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|spaceSortDynamicTableReq|空间分类动态表|body|true|SpaceSortDynamicTableReq|SpaceSortDynamicTableReq|
|&emsp;&emsp;annotation|字段注释||false|string||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;decimalPlace|小数点位数||false|integer(int32)||
|&emsp;&emsp;defaultValue|默认值||false|string||
|&emsp;&emsp;fieldName|字段名称||false|string||
|&emsp;&emsp;fieldType|字段类型||false|string||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;primaryKey|业务主建||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;required|是否必填||false|string||
|&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持||false|string||
|&emsp;&emsp;show|列表是否展示(0不展示、1展示)||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序字段||false|string||
|&emsp;&emsp;spaceSortId|空间分类ID||false|string||
|&emsp;&emsp;update|是否更新||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«SpaceSortDynamicTableRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«SpaceSortDynamicTableRes»|Page«SpaceSortDynamicTableRes»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SpaceSortDynamicTableRes|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释|string||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称|string||
|&emsp;&emsp;&emsp;&emsp;fieldNamePinYin|字段名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段|string||
|&emsp;&emsp;&emsp;&emsp;spaceSortId|空间分类ID|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"annotation": "",
				"createBy": "",
				"createTime": "",
				"decimalPlace": 0,
				"defaultValue": "",
				"fieldName": "",
				"fieldNamePinYin": "",
				"fieldType": "",
				"id": "",
				"levelId": "",
				"primaryKey": "",
				"projectId": "",
				"required": "",
				"searchFlag": "",
				"show": "",
				"sort": "",
				"spaceSortId": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


## 查询树型结构


**接口地址**:`/space-sort-dynamic/queryTree`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|levelId|关卡id|query|true|string||
|projectId|项目id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«SpaceSortTreeRes»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|SpaceSortTreeRes|
|&emsp;&emsp;children|子节点|array|SpaceSortTreeRes|
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;levelName|层级名称|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;parent|父级id|string||
|&emsp;&emsp;type|类型|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"children": [
				{
					"children": [
						{}
					],
					"id": "",
					"levelName": "",
					"name": "",
					"parent": "",
					"type": ""
				}
			],
			"id": "",
			"levelName": "",
			"name": "",
			"parent": "",
			"type": ""
		}
	]
}
```


## 添加数据


**接口地址**:`/space-sort-dynamic/saveDynamic`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|params|params|body|true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Void»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true
}
```


## 更新数据


**接口地址**:`/space-sort-dynamic/updateDynamic`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|params|params|body|true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


# 空间分类管理


## 根据id查询空间分类数据


**接口地址**:`/space-sort`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SpaceSortRes»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SpaceSortRes|SpaceSortRes|
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;level|层级|integer(int32)||
|&emsp;&emsp;levelId|关卡|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;parentId|父级树id|string||
|&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;spaceSortDynamicList|数据结构|array|SpaceSortDynamicTableRes|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释|string||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称|string||
|&emsp;&emsp;&emsp;&emsp;fieldNamePinYin|字段名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段|string||
|&emsp;&emsp;&emsp;&emsp;spaceSortId|空间分类ID|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;sysTreeWorkIndex|树结构对象|SysTreeWorkIndexDTO|SysTreeWorkIndexDTO|
|&emsp;&emsp;&emsp;&emsp;dirId||string||
|&emsp;&emsp;&emsp;&emsp;dirPath||string||
|&emsp;&emsp;&emsp;&emsp;lifeCount||integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus||string||
|&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;showStatus||string||
|&emsp;&emsp;&emsp;&emsp;sortIndex||integer||
|&emsp;&emsp;&emsp;&emsp;value||object||
|&emsp;&emsp;&emsp;&emsp;workId||string||
|&emsp;&emsp;&emsp;&emsp;workType||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"id": "",
		"level": 0,
		"levelId": "",
		"name": "",
		"parentId": "",
		"projectId": "",
		"spaceSortDynamicList": [
			{
				"annotation": "",
				"createBy": "",
				"createTime": "",
				"decimalPlace": 0,
				"defaultValue": "",
				"fieldName": "",
				"fieldNamePinYin": "",
				"fieldType": "",
				"id": "",
				"levelId": "",
				"primaryKey": "",
				"projectId": "",
				"required": "",
				"searchFlag": "",
				"show": "",
				"sort": "",
				"spaceSortId": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"sysTreeWorkIndex": {
			"dirId": "",
			"dirPath": "",
			"lifeCount": 0,
			"lockStatus": "",
			"name": "",
			"showStatus": "",
			"sortIndex": 0,
			"value": {},
			"workId": "",
			"workType": ""
		}
	}
}
```


## 添加空间分类


**接口地址**:`/space-sort`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "level": 0,
  "levelId": "",
  "name": "",
  "parentId": "",
  "projectId": "",
  "size": 0,
  "spaceSortDynamicList": [
    {
      "annotation": "",
      "current": 0,
      "decimalPlace": 0,
      "defaultValue": "",
      "fieldName": "",
      "fieldType": "",
      "id": "",
      "levelId": "",
      "primaryKey": "",
      "projectId": "",
      "required": "",
      "searchFlag": "",
      "show": "",
      "size": 0,
      "sort": "",
      "spaceSortId": "",
      "update": ""
    }
  ]
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|spaceSortReq|空间分类|body|true|SpaceSortReq|SpaceSortReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;level|层级||false|integer(int32)||
|&emsp;&emsp;levelId|关卡||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;parentId|父级节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;spaceSortDynamicList|数据结构||false|array|SpaceSortDynamicTableReq|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释||false|string||
|&emsp;&emsp;&emsp;&emsp;current|起始页||false|integer||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数||false|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值||false|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称||false|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型||false|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填||false|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持||false|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)||false|string||
|&emsp;&emsp;&emsp;&emsp;size|每页条数||false|integer||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段||false|string||
|&emsp;&emsp;&emsp;&emsp;spaceSortId|空间分类ID||false|string||
|&emsp;&emsp;&emsp;&emsp;update|是否更新||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SpaceSortRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SpaceSortRes|SpaceSortRes|
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;level|层级|integer(int32)||
|&emsp;&emsp;levelId|关卡|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;parentId|父级树id|string||
|&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;spaceSortDynamicList|数据结构|array|SpaceSortDynamicTableRes|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释|string||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称|string||
|&emsp;&emsp;&emsp;&emsp;fieldNamePinYin|字段名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段|string||
|&emsp;&emsp;&emsp;&emsp;spaceSortId|空间分类ID|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;sysTreeWorkIndex|树结构对象|SysTreeWorkIndexDTO|SysTreeWorkIndexDTO|
|&emsp;&emsp;&emsp;&emsp;dirId||string||
|&emsp;&emsp;&emsp;&emsp;dirPath||string||
|&emsp;&emsp;&emsp;&emsp;lifeCount||integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus||string||
|&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;showStatus||string||
|&emsp;&emsp;&emsp;&emsp;sortIndex||integer||
|&emsp;&emsp;&emsp;&emsp;value||object||
|&emsp;&emsp;&emsp;&emsp;workId||string||
|&emsp;&emsp;&emsp;&emsp;workType||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"id": "",
		"level": 0,
		"levelId": "",
		"name": "",
		"parentId": "",
		"projectId": "",
		"spaceSortDynamicList": [
			{
				"annotation": "",
				"createBy": "",
				"createTime": "",
				"decimalPlace": 0,
				"defaultValue": "",
				"fieldName": "",
				"fieldNamePinYin": "",
				"fieldType": "",
				"id": "",
				"levelId": "",
				"primaryKey": "",
				"projectId": "",
				"required": "",
				"searchFlag": "",
				"show": "",
				"sort": "",
				"spaceSortId": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"sysTreeWorkIndex": {
			"dirId": "",
			"dirPath": "",
			"lifeCount": 0,
			"lockStatus": "",
			"name": "",
			"showStatus": "",
			"sortIndex": 0,
			"value": {},
			"workId": "",
			"workType": ""
		}
	}
}
```


## 根据id更新空间分类


**接口地址**:`/space-sort`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "level": 0,
  "levelId": "",
  "name": "",
  "parentId": "",
  "projectId": "",
  "size": 0,
  "spaceSortDynamicList": [
    {
      "annotation": "",
      "current": 0,
      "decimalPlace": 0,
      "defaultValue": "",
      "fieldName": "",
      "fieldType": "",
      "id": "",
      "levelId": "",
      "primaryKey": "",
      "projectId": "",
      "required": "",
      "searchFlag": "",
      "show": "",
      "size": 0,
      "sort": "",
      "spaceSortId": "",
      "update": ""
    }
  ]
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|spaceSortReq|空间分类|body|true|SpaceSortReq|SpaceSortReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;level|层级||false|integer(int32)||
|&emsp;&emsp;levelId|关卡||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;parentId|父级节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;spaceSortDynamicList|数据结构||false|array|SpaceSortDynamicTableReq|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释||false|string||
|&emsp;&emsp;&emsp;&emsp;current|起始页||false|integer||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数||false|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值||false|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称||false|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型||false|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填||false|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持||false|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)||false|string||
|&emsp;&emsp;&emsp;&emsp;size|每页条数||false|integer||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段||false|string||
|&emsp;&emsp;&emsp;&emsp;spaceSortId|空间分类ID||false|string||
|&emsp;&emsp;&emsp;&emsp;update|是否更新||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SpaceSortRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SpaceSortRes|SpaceSortRes|
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;level|层级|integer(int32)||
|&emsp;&emsp;levelId|关卡|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;parentId|父级树id|string||
|&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;spaceSortDynamicList|数据结构|array|SpaceSortDynamicTableRes|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释|string||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称|string||
|&emsp;&emsp;&emsp;&emsp;fieldNamePinYin|字段名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段|string||
|&emsp;&emsp;&emsp;&emsp;spaceSortId|空间分类ID|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;sysTreeWorkIndex|树结构对象|SysTreeWorkIndexDTO|SysTreeWorkIndexDTO|
|&emsp;&emsp;&emsp;&emsp;dirId||string||
|&emsp;&emsp;&emsp;&emsp;dirPath||string||
|&emsp;&emsp;&emsp;&emsp;lifeCount||integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus||string||
|&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;showStatus||string||
|&emsp;&emsp;&emsp;&emsp;sortIndex||integer||
|&emsp;&emsp;&emsp;&emsp;value||object||
|&emsp;&emsp;&emsp;&emsp;workId||string||
|&emsp;&emsp;&emsp;&emsp;workType||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"id": "",
		"level": 0,
		"levelId": "",
		"name": "",
		"parentId": "",
		"projectId": "",
		"spaceSortDynamicList": [
			{
				"annotation": "",
				"createBy": "",
				"createTime": "",
				"decimalPlace": 0,
				"defaultValue": "",
				"fieldName": "",
				"fieldNamePinYin": "",
				"fieldType": "",
				"id": "",
				"levelId": "",
				"primaryKey": "",
				"projectId": "",
				"required": "",
				"searchFlag": "",
				"show": "",
				"sort": "",
				"spaceSortId": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"sysTreeWorkIndex": {
			"dirId": "",
			"dirPath": "",
			"lifeCount": 0,
			"lockStatus": "",
			"name": "",
			"showStatus": "",
			"sortIndex": 0,
			"value": {},
			"workId": "",
			"workType": ""
		}
	}
}
```


## 根据ids删除空间分类


**接口地址**:`/space-sort`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|ids|ids列表|body|true|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«int»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||integer(int32)|integer(int32)|


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": 0
}
```


## 分页条件查询空间分类


**接口地址**:`/space-sort/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "id": "",
  "level": 0,
  "levelId": "",
  "name": "",
  "parentId": "",
  "projectId": "",
  "size": 0,
  "spaceSortDynamicList": [
    {
      "annotation": "",
      "current": 0,
      "decimalPlace": 0,
      "defaultValue": "",
      "fieldName": "",
      "fieldType": "",
      "id": "",
      "levelId": "",
      "primaryKey": "",
      "projectId": "",
      "required": "",
      "searchFlag": "",
      "show": "",
      "size": 0,
      "sort": "",
      "spaceSortId": "",
      "update": ""
    }
  ]
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|spaceSortReq|空间分类|body|true|SpaceSortReq|SpaceSortReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;level|层级||false|integer(int32)||
|&emsp;&emsp;levelId|关卡||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;parentId|父级节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;spaceSortDynamicList|数据结构||false|array|SpaceSortDynamicTableReq|
|&emsp;&emsp;&emsp;&emsp;annotation|字段注释||false|string||
|&emsp;&emsp;&emsp;&emsp;current|起始页||false|integer||
|&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数||false|integer||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认值||false|string||
|&emsp;&emsp;&emsp;&emsp;fieldName|字段名称||false|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|字段类型||false|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填||false|string||
|&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持||false|string||
|&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)||false|string||
|&emsp;&emsp;&emsp;&emsp;size|每页条数||false|integer||
|&emsp;&emsp;&emsp;&emsp;sort|排序字段||false|string||
|&emsp;&emsp;&emsp;&emsp;spaceSortId|空间分类ID||false|string||
|&emsp;&emsp;&emsp;&emsp;update|是否更新||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«SpaceSortRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«SpaceSortRes»|Page«SpaceSortRes»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SpaceSortRes|
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;level|层级|integer||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡|string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;parentId|父级树id|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;spaceSortDynamicList|数据结构|array|SpaceSortDynamicTableRes|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;annotation|字段注释|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;decimalPlace|小数点位数|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;defaultValue|默认值|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;fieldName|字段名称|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;fieldNamePinYin|字段名称拼音|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;fieldType|字段类型|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;primaryKey|业务主建|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;required|是否必填|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;searchFlag|是否支持检索 0不支持、1支持|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;show|列表是否展示(0不展示、1展示)|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;sort|排序字段|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;spaceSortId|空间分类ID|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;&emsp;&emsp;sysTreeWorkIndex|树结构对象|SysTreeWorkIndexDTO|SysTreeWorkIndexDTO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirId||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;dirPath||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lifeCount||integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;lockStatus||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;showStatus||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;sortIndex||integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;value||object||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workId||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;workType||string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"id": "",
				"level": 0,
				"levelId": "",
				"name": "",
				"parentId": "",
				"projectId": "",
				"spaceSortDynamicList": [
					{
						"annotation": "",
						"createBy": "",
						"createTime": "",
						"decimalPlace": 0,
						"defaultValue": "",
						"fieldName": "",
						"fieldNamePinYin": "",
						"fieldType": "",
						"id": "",
						"levelId": "",
						"primaryKey": "",
						"projectId": "",
						"required": "",
						"searchFlag": "",
						"show": "",
						"sort": "",
						"spaceSortId": "",
						"updateBy": "",
						"updateTime": ""
					}
				],
				"sysTreeWorkIndex": {
					"dirId": "",
					"dirPath": "",
					"lifeCount": 0,
					"lockStatus": "",
					"name": "",
					"showStatus": "",
					"sortIndex": 0,
					"value": {},
					"workId": "",
					"workType": ""
				}
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


# 菜单表对象功能接口


## 根据id查询数据


**接口地址**:`/sysMenu`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysMenuRes»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysMenuRes|SysMenuRes|
|&emsp;&emsp;children|子节点|array|SysMenuRes|
|&emsp;&emsp;component|组件地址|string||
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;hidden|显示状态（0显示、1 隐藏）|boolean||
|&emsp;&emsp;icon|菜单图标|string||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;isCache|是否缓存（0缓存、1不缓存）|string||
|&emsp;&emsp;isFrame|是否外链|string||
|&emsp;&emsp;meta|meta|MetaRes|MetaRes|
|&emsp;&emsp;&emsp;&emsp;icon|设置该路由的图标，对应路径src/assets/icons/svg|string||
|&emsp;&emsp;&emsp;&emsp;link|内链地址（http(s)://开头）|string||
|&emsp;&emsp;&emsp;&emsp;noCache|设置为true，则不会被 <keep-alive>缓存|boolean||
|&emsp;&emsp;&emsp;&emsp;title|设置该路由在侧边栏和面包屑中展示的名字|string||
|&emsp;&emsp;name|菜单名称|string||
|&emsp;&emsp;parentId|父菜单id|string||
|&emsp;&emsp;path|路由地址|string||
|&emsp;&emsp;perms|权限字符串|string||
|&emsp;&emsp;queryParam|路由参数|string||
|&emsp;&emsp;redirect|redirect|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|菜单状态（0正常、1停用）|string||
|&emsp;&emsp;type|类型（M目录 C菜单 F按钮）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;visible|显示状态（0显示、1 隐藏）|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"children": [
			{
				"children": [
					{}
				],
				"component": "",
				"createBy": "",
				"createTime": "",
				"hidden": true,
				"icon": "",
				"id": "",
				"isCache": "",
				"isFrame": "",
				"meta": {
					"icon": "",
					"link": "",
					"noCache": true,
					"title": ""
				},
				"name": "",
				"parentId": "",
				"path": "",
				"perms": "",
				"queryParam": "",
				"redirect": "",
				"remark": "",
				"sort": 0,
				"status": "",
				"type": "",
				"updateBy": "",
				"updateTime": "",
				"visible": ""
			}
		],
		"component": "",
		"createBy": "",
		"createTime": "",
		"hidden": true,
		"icon": "",
		"id": "",
		"isCache": "",
		"isFrame": "",
		"meta": {
			"icon": "",
			"link": "",
			"noCache": true,
			"title": ""
		},
		"name": "",
		"parentId": "",
		"path": "",
		"perms": "",
		"queryParam": "",
		"redirect": "",
		"remark": "",
		"sort": 0,
		"status": "",
		"type": "",
		"updateBy": "",
		"updateTime": "",
		"visible": ""
	}
}
```


## 添加数据


**接口地址**:`/sysMenu`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "component": "",
  "current": 0,
  "icon": "",
  "id": "",
  "isCache": "",
  "isFrame": "",
  "name": "",
  "parentId": "",
  "path": "",
  "perms": "",
  "queryParam": "",
  "remark": "",
  "size": 0,
  "sort": 0,
  "status": "",
  "type": "",
  "visible": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysMenuReq|菜单表|body|true|SysMenuReq|SysMenuReq|
|&emsp;&emsp;component|组件地址||false|string||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;icon|菜单图标||false|string||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;isCache|是否缓存（0缓存、1不缓存）||false|string||
|&emsp;&emsp;isFrame|是否外链||false|string||
|&emsp;&emsp;name|菜单名称||false|string||
|&emsp;&emsp;parentId|父菜单id||false|string||
|&emsp;&emsp;path|路由地址||false|string||
|&emsp;&emsp;perms|权限字符串||false|string||
|&emsp;&emsp;queryParam|路由参数||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序||false|integer(int32)||
|&emsp;&emsp;status|菜单状态（0正常、1停用）||false|string||
|&emsp;&emsp;type|类型（M目录 C菜单 F按钮）||false|string||
|&emsp;&emsp;visible|显示状态（0显示、1 隐藏）||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysMenuRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysMenuRes|SysMenuRes|
|&emsp;&emsp;children|子节点|array|SysMenuRes|
|&emsp;&emsp;component|组件地址|string||
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;hidden|显示状态（0显示、1 隐藏）|boolean||
|&emsp;&emsp;icon|菜单图标|string||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;isCache|是否缓存（0缓存、1不缓存）|string||
|&emsp;&emsp;isFrame|是否外链|string||
|&emsp;&emsp;meta|meta|MetaRes|MetaRes|
|&emsp;&emsp;&emsp;&emsp;icon|设置该路由的图标，对应路径src/assets/icons/svg|string||
|&emsp;&emsp;&emsp;&emsp;link|内链地址（http(s)://开头）|string||
|&emsp;&emsp;&emsp;&emsp;noCache|设置为true，则不会被 <keep-alive>缓存|boolean||
|&emsp;&emsp;&emsp;&emsp;title|设置该路由在侧边栏和面包屑中展示的名字|string||
|&emsp;&emsp;name|菜单名称|string||
|&emsp;&emsp;parentId|父菜单id|string||
|&emsp;&emsp;path|路由地址|string||
|&emsp;&emsp;perms|权限字符串|string||
|&emsp;&emsp;queryParam|路由参数|string||
|&emsp;&emsp;redirect|redirect|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|菜单状态（0正常、1停用）|string||
|&emsp;&emsp;type|类型（M目录 C菜单 F按钮）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;visible|显示状态（0显示、1 隐藏）|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"children": [
			{
				"children": [
					{}
				],
				"component": "",
				"createBy": "",
				"createTime": "",
				"hidden": true,
				"icon": "",
				"id": "",
				"isCache": "",
				"isFrame": "",
				"meta": {
					"icon": "",
					"link": "",
					"noCache": true,
					"title": ""
				},
				"name": "",
				"parentId": "",
				"path": "",
				"perms": "",
				"queryParam": "",
				"redirect": "",
				"remark": "",
				"sort": 0,
				"status": "",
				"type": "",
				"updateBy": "",
				"updateTime": "",
				"visible": ""
			}
		],
		"component": "",
		"createBy": "",
		"createTime": "",
		"hidden": true,
		"icon": "",
		"id": "",
		"isCache": "",
		"isFrame": "",
		"meta": {
			"icon": "",
			"link": "",
			"noCache": true,
			"title": ""
		},
		"name": "",
		"parentId": "",
		"path": "",
		"perms": "",
		"queryParam": "",
		"redirect": "",
		"remark": "",
		"sort": 0,
		"status": "",
		"type": "",
		"updateBy": "",
		"updateTime": "",
		"visible": ""
	}
}
```


## 根据id更新数据


**接口地址**:`/sysMenu`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "component": "",
  "current": 0,
  "icon": "",
  "id": "",
  "isCache": "",
  "isFrame": "",
  "name": "",
  "parentId": "",
  "path": "",
  "perms": "",
  "queryParam": "",
  "remark": "",
  "size": 0,
  "sort": 0,
  "status": "",
  "type": "",
  "visible": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysMenuReq|菜单表|body|true|SysMenuReq|SysMenuReq|
|&emsp;&emsp;component|组件地址||false|string||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;icon|菜单图标||false|string||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;isCache|是否缓存（0缓存、1不缓存）||false|string||
|&emsp;&emsp;isFrame|是否外链||false|string||
|&emsp;&emsp;name|菜单名称||false|string||
|&emsp;&emsp;parentId|父菜单id||false|string||
|&emsp;&emsp;path|路由地址||false|string||
|&emsp;&emsp;perms|权限字符串||false|string||
|&emsp;&emsp;queryParam|路由参数||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序||false|integer(int32)||
|&emsp;&emsp;status|菜单状态（0正常、1停用）||false|string||
|&emsp;&emsp;type|类型（M目录 C菜单 F按钮）||false|string||
|&emsp;&emsp;visible|显示状态（0显示、1 隐藏）||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysMenuRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysMenuRes|SysMenuRes|
|&emsp;&emsp;children|子节点|array|SysMenuRes|
|&emsp;&emsp;component|组件地址|string||
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;hidden|显示状态（0显示、1 隐藏）|boolean||
|&emsp;&emsp;icon|菜单图标|string||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;isCache|是否缓存（0缓存、1不缓存）|string||
|&emsp;&emsp;isFrame|是否外链|string||
|&emsp;&emsp;meta|meta|MetaRes|MetaRes|
|&emsp;&emsp;&emsp;&emsp;icon|设置该路由的图标，对应路径src/assets/icons/svg|string||
|&emsp;&emsp;&emsp;&emsp;link|内链地址（http(s)://开头）|string||
|&emsp;&emsp;&emsp;&emsp;noCache|设置为true，则不会被 <keep-alive>缓存|boolean||
|&emsp;&emsp;&emsp;&emsp;title|设置该路由在侧边栏和面包屑中展示的名字|string||
|&emsp;&emsp;name|菜单名称|string||
|&emsp;&emsp;parentId|父菜单id|string||
|&emsp;&emsp;path|路由地址|string||
|&emsp;&emsp;perms|权限字符串|string||
|&emsp;&emsp;queryParam|路由参数|string||
|&emsp;&emsp;redirect|redirect|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|菜单状态（0正常、1停用）|string||
|&emsp;&emsp;type|类型（M目录 C菜单 F按钮）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;visible|显示状态（0显示、1 隐藏）|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"children": [
			{
				"children": [
					{}
				],
				"component": "",
				"createBy": "",
				"createTime": "",
				"hidden": true,
				"icon": "",
				"id": "",
				"isCache": "",
				"isFrame": "",
				"meta": {
					"icon": "",
					"link": "",
					"noCache": true,
					"title": ""
				},
				"name": "",
				"parentId": "",
				"path": "",
				"perms": "",
				"queryParam": "",
				"redirect": "",
				"remark": "",
				"sort": 0,
				"status": "",
				"type": "",
				"updateBy": "",
				"updateTime": "",
				"visible": ""
			}
		],
		"component": "",
		"createBy": "",
		"createTime": "",
		"hidden": true,
		"icon": "",
		"id": "",
		"isCache": "",
		"isFrame": "",
		"meta": {
			"icon": "",
			"link": "",
			"noCache": true,
			"title": ""
		},
		"name": "",
		"parentId": "",
		"path": "",
		"perms": "",
		"queryParam": "",
		"redirect": "",
		"remark": "",
		"sort": 0,
		"status": "",
		"type": "",
		"updateBy": "",
		"updateTime": "",
		"visible": ""
	}
}
```


## 根据ids删除数据


**接口地址**:`/sysMenu`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|ids|ids列表|body|true|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«int»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||integer(int32)|integer(int32)|


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": 0
}
```


## 根据当前登录人获取对应的菜单


**接口地址**:`/sysMenu/getRouters`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«RouterVo»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|RouterVo|
|&emsp;&emsp;alwaysShow||boolean||
|&emsp;&emsp;children||array|RouterVo|
|&emsp;&emsp;component||string||
|&emsp;&emsp;hidden||boolean||
|&emsp;&emsp;meta||MetaRes0|MetaRes0|
|&emsp;&emsp;&emsp;&emsp;icon|设置该路由的图标，对应路径src/assets/icons/svg|string||
|&emsp;&emsp;&emsp;&emsp;link|内链地址（http(s)://开头）|string||
|&emsp;&emsp;&emsp;&emsp;noCache|设置为true，则不会被 <keep-alive>缓存|boolean||
|&emsp;&emsp;&emsp;&emsp;title|设置该路由在侧边栏和面包屑中展示的名字|string||
|&emsp;&emsp;name||string||
|&emsp;&emsp;path||string||
|&emsp;&emsp;query||string||
|&emsp;&emsp;redirect||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"alwaysShow": true,
			"children": [
				{
					"alwaysShow": true,
					"children": [
						{}
					],
					"component": "",
					"hidden": true,
					"meta": {
						"icon": "",
						"link": "",
						"noCache": true,
						"title": ""
					},
					"name": "",
					"path": "",
					"query": "",
					"redirect": ""
				}
			],
			"component": "",
			"hidden": true,
			"meta": {
				"icon": "",
				"link": "",
				"noCache": true,
				"title": ""
			},
			"name": "",
			"path": "",
			"query": "",
			"redirect": ""
		}
	]
}
```


## 查询菜单


**接口地址**:`/sysMenu/queryMenu`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "component": "",
  "current": 0,
  "icon": "",
  "id": "",
  "isCache": "",
  "isFrame": "",
  "name": "",
  "parentId": "",
  "path": "",
  "perms": "",
  "queryParam": "",
  "remark": "",
  "size": 0,
  "sort": 0,
  "status": "",
  "type": "",
  "visible": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysMenuReq|菜单表|body|true|SysMenuReq|SysMenuReq|
|&emsp;&emsp;component|组件地址||false|string||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;icon|菜单图标||false|string||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;isCache|是否缓存（0缓存、1不缓存）||false|string||
|&emsp;&emsp;isFrame|是否外链||false|string||
|&emsp;&emsp;name|菜单名称||false|string||
|&emsp;&emsp;parentId|父菜单id||false|string||
|&emsp;&emsp;path|路由地址||false|string||
|&emsp;&emsp;perms|权限字符串||false|string||
|&emsp;&emsp;queryParam|路由参数||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序||false|integer(int32)||
|&emsp;&emsp;status|菜单状态（0正常、1停用）||false|string||
|&emsp;&emsp;type|类型（M目录 C菜单 F按钮）||false|string||
|&emsp;&emsp;visible|显示状态（0显示、1 隐藏）||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«SysMenuRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|SysMenuRes|
|&emsp;&emsp;children|子节点|array|SysMenuRes|
|&emsp;&emsp;component|组件地址|string||
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;hidden|显示状态（0显示、1 隐藏）|boolean||
|&emsp;&emsp;icon|菜单图标|string||
|&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;isCache|是否缓存（0缓存、1不缓存）|string||
|&emsp;&emsp;isFrame|是否外链|string||
|&emsp;&emsp;meta|meta|MetaRes|MetaRes|
|&emsp;&emsp;&emsp;&emsp;icon|设置该路由的图标，对应路径src/assets/icons/svg|string||
|&emsp;&emsp;&emsp;&emsp;link|内链地址（http(s)://开头）|string||
|&emsp;&emsp;&emsp;&emsp;noCache|设置为true，则不会被 <keep-alive>缓存|boolean||
|&emsp;&emsp;&emsp;&emsp;title|设置该路由在侧边栏和面包屑中展示的名字|string||
|&emsp;&emsp;name|菜单名称|string||
|&emsp;&emsp;parentId|父菜单id|string||
|&emsp;&emsp;path|路由地址|string||
|&emsp;&emsp;perms|权限字符串|string||
|&emsp;&emsp;queryParam|路由参数|string||
|&emsp;&emsp;redirect|redirect|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|菜单状态（0正常、1停用）|string||
|&emsp;&emsp;type|类型（M目录 C菜单 F按钮）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;visible|显示状态（0显示、1 隐藏）|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"children": [
				{
					"children": [
						{}
					],
					"component": "",
					"createBy": "",
					"createTime": "",
					"hidden": true,
					"icon": "",
					"id": "",
					"isCache": "",
					"isFrame": "",
					"meta": {
						"icon": "",
						"link": "",
						"noCache": true,
						"title": ""
					},
					"name": "",
					"parentId": "",
					"path": "",
					"perms": "",
					"queryParam": "",
					"redirect": "",
					"remark": "",
					"sort": 0,
					"status": "",
					"type": "",
					"updateBy": "",
					"updateTime": "",
					"visible": ""
				}
			],
			"component": "",
			"createBy": "",
			"createTime": "",
			"hidden": true,
			"icon": "",
			"id": "",
			"isCache": "",
			"isFrame": "",
			"meta": {
				"icon": "",
				"link": "",
				"noCache": true,
				"title": ""
			},
			"name": "",
			"parentId": "",
			"path": "",
			"perms": "",
			"queryParam": "",
			"redirect": "",
			"remark": "",
			"sort": 0,
			"status": "",
			"type": "",
			"updateBy": "",
			"updateTime": "",
			"visible": ""
		}
	]
}
```


## 根据权限查询菜单选择项


**接口地址**:`/sysMenu/queryMenuSelect`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|roleId|roleId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«string»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": []
}
```


## 分页条件查询数据


**接口地址**:`/sysMenu/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "component": "",
  "current": 0,
  "icon": "",
  "id": "",
  "isCache": "",
  "isFrame": "",
  "name": "",
  "parentId": "",
  "path": "",
  "perms": "",
  "queryParam": "",
  "remark": "",
  "size": 0,
  "sort": 0,
  "status": "",
  "type": "",
  "visible": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysMenuReq|菜单表|body|true|SysMenuReq|SysMenuReq|
|&emsp;&emsp;component|组件地址||false|string||
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;icon|菜单图标||false|string||
|&emsp;&emsp;id|业务唯一id||false|string||
|&emsp;&emsp;isCache|是否缓存（0缓存、1不缓存）||false|string||
|&emsp;&emsp;isFrame|是否外链||false|string||
|&emsp;&emsp;name|菜单名称||false|string||
|&emsp;&emsp;parentId|父菜单id||false|string||
|&emsp;&emsp;path|路由地址||false|string||
|&emsp;&emsp;perms|权限字符串||false|string||
|&emsp;&emsp;queryParam|路由参数||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序||false|integer(int32)||
|&emsp;&emsp;status|菜单状态（0正常、1停用）||false|string||
|&emsp;&emsp;type|类型（M目录 C菜单 F按钮）||false|string||
|&emsp;&emsp;visible|显示状态（0显示、1 隐藏）||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«SysMenuRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«SysMenuRes»|Page«SysMenuRes»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SysMenuRes|
|&emsp;&emsp;&emsp;&emsp;children|子节点|array|SysMenuRes|
|&emsp;&emsp;&emsp;&emsp;component|组件地址|string||
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;hidden|显示状态（0显示、1 隐藏）|boolean||
|&emsp;&emsp;&emsp;&emsp;icon|菜单图标|string||
|&emsp;&emsp;&emsp;&emsp;id|业务唯一id|string||
|&emsp;&emsp;&emsp;&emsp;isCache|是否缓存（0缓存、1不缓存）|string||
|&emsp;&emsp;&emsp;&emsp;isFrame|是否外链|string||
|&emsp;&emsp;&emsp;&emsp;meta|meta|MetaRes|MetaRes|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;icon|设置该路由的图标，对应路径src/assets/icons/svg|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;link|内链地址（http(s)://开头）|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;noCache|设置为true，则不会被 <keep-alive>缓存|boolean||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;title|设置该路由在侧边栏和面包屑中展示的名字|string||
|&emsp;&emsp;&emsp;&emsp;name|菜单名称|string||
|&emsp;&emsp;&emsp;&emsp;parentId|父菜单id|string||
|&emsp;&emsp;&emsp;&emsp;path|路由地址|string||
|&emsp;&emsp;&emsp;&emsp;perms|权限字符串|string||
|&emsp;&emsp;&emsp;&emsp;queryParam|路由参数|string||
|&emsp;&emsp;&emsp;&emsp;redirect|redirect|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序|integer||
|&emsp;&emsp;&emsp;&emsp;status|菜单状态（0正常、1停用）|string||
|&emsp;&emsp;&emsp;&emsp;type|类型（M目录 C菜单 F按钮）|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;&emsp;&emsp;visible|显示状态（0显示、1 隐藏）|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"children": [
					{
						"children": [
							{}
						],
						"component": "",
						"createBy": "",
						"createTime": "",
						"hidden": true,
						"icon": "",
						"id": "",
						"isCache": "",
						"isFrame": "",
						"meta": {
							"icon": "",
							"link": "",
							"noCache": true,
							"title": ""
						},
						"name": "",
						"parentId": "",
						"path": "",
						"perms": "",
						"queryParam": "",
						"redirect": "",
						"remark": "",
						"sort": 0,
						"status": "",
						"type": "",
						"updateBy": "",
						"updateTime": "",
						"visible": ""
					}
				],
				"component": "",
				"createBy": "",
				"createTime": "",
				"hidden": true,
				"icon": "",
				"id": "",
				"isCache": "",
				"isFrame": "",
				"meta": {
					"icon": "",
					"link": "",
					"noCache": true,
					"title": ""
				},
				"name": "",
				"parentId": "",
				"path": "",
				"perms": "",
				"queryParam": "",
				"redirect": "",
				"remark": "",
				"sort": 0,
				"status": "",
				"type": "",
				"updateBy": "",
				"updateTime": "",
				"visible": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


# 资源管理


## add


**接口地址**:`/resourcedata/add`


**请求方式**:`POST`


**请求数据类型**:`multipart/form-data`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|thumbnail||formData|false|file||
|file||formData|false|file||
|id|id|query|false|string||
|name|名称|query|false|string||
|projectId|项目id|query|false|string||
|property|属性|query|false|string||
|subType|二级分类|query|false|string||
|type|类型 mesh|material|texture|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## queryPageList


**接口地址**:`/resourcedata/queryPageList`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "countId": "",
  "current": 0,
  "id": "",
  "maxLimit": 0,
  "name": "",
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "projectId": "",
  "records": [],
  "searchCount": true,
  "size": 0,
  "total": 0,
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|resourceDataQueryReq|资源管理|body|true|ResourceDataReq|ResourceDataReq|
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;total|||false|integer(int64)||
|&emsp;&emsp;type|类型 mesh|material|texture||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«资源管理»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«资源管理»|IPage«资源管理»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|资源管理|
|&emsp;&emsp;&emsp;&emsp;fileName|文件名称|string||
|&emsp;&emsp;&emsp;&emsp;fileSize|文件大小|string||
|&emsp;&emsp;&emsp;&emsp;fileUrl|文件地址|string||
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;property|属性|string||
|&emsp;&emsp;&emsp;&emsp;subType|二级分类|string||
|&emsp;&emsp;&emsp;&emsp;thumbnailName|缩略图名称|string||
|&emsp;&emsp;&emsp;&emsp;thumbnailUrl|缩略图地址|string||
|&emsp;&emsp;&emsp;&emsp;type|类型|string||
|&emsp;&emsp;&emsp;&emsp;version|版本号|number||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"fileName": "",
				"fileSize": "",
				"fileUrl": "",
				"id": "",
				"name": "",
				"projectId": "",
				"property": "",
				"subType": "",
				"thumbnailName": "",
				"thumbnailUrl": "",
				"type": "",
				"version": 0
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## update


**接口地址**:`/resourcedata/update`


**请求方式**:`POST`


**请求数据类型**:`multipart/form-data`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|thumbnail||formData|false|file||
|file||formData|false|file||
|id|id|query|false|string||
|name|名称|query|false|string||
|projectId|项目id|query|false|string||
|property|属性|query|false|string||
|subType|二级分类|query|false|string||
|type|类型 mesh|material|texture|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## get


**接口地址**:`/resourcedata/{id}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«资源管理»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||资源管理|资源管理|
|&emsp;&emsp;fileName|文件名称|string||
|&emsp;&emsp;fileSize|文件大小|string||
|&emsp;&emsp;fileUrl|文件地址|string||
|&emsp;&emsp;id|id|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;property|属性|string||
|&emsp;&emsp;subType|二级分类|string||
|&emsp;&emsp;thumbnailName|缩略图名称|string||
|&emsp;&emsp;thumbnailUrl|缩略图地址|string||
|&emsp;&emsp;type|类型|string||
|&emsp;&emsp;version|版本号|number(double)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"fileName": "",
		"fileSize": "",
		"fileUrl": "",
		"id": "",
		"name": "",
		"projectId": "",
		"property": "",
		"subType": "",
		"thumbnailName": "",
		"thumbnailUrl": "",
		"type": "",
		"version": 0
	}
}
```


## delete


**接口地址**:`/resourcedata/{id}`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


# 资源管理-项目-生命体二级分类空间集合


## 新增生命体二级分类空间集合


**接口地址**:`/life/subtype/space/add`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "lifeIds": "",
  "model": 0,
  "name": "",
  "oldParentId": "",
  "projectId": "",
  "sqlContent": "",
  "sysTreeDTO": {
    "ancestralChain": "",
    "businessId": "",
    "businessPageId": "",
    "createBy": "",
    "createTime": "",
    "delFlag": "",
    "directParentId": "",
    "id": "",
    "labelsModel": "",
    "level": 0,
    "lft": 0,
    "lockStatus": "",
    "model": 0,
    "name": "",
    "oldId": "",
    "passId": "",
    "projectId": "",
    "remark": "",
    "rgt": 0,
    "sameLevelLastId": "",
    "seq": 0,
    "showStatus": "",
    "status": "",
    "tenantWorkId": "",
    "type": "",
    "updateBy": "",
    "updateTime": ""
  }
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSubtypeSpaceCollectionSaveReq|新增生命体二级分类集合|body|true|LifeSubtypeSpaceCollectionSaveReq|LifeSubtypeSpaceCollectionSaveReq|
|&emsp;&emsp;id|生命体二级分类集合id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeIds|生命体ids，以逗号隔开||false|string||
|&emsp;&emsp;model|1：动态（执行SQL挂载）2：静态（手动添加生命体）||false|integer(int32)||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;oldParentId|旧父节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;sqlContent|SQL查询语句||false|string||
|&emsp;&emsp;sysTreeDTO|当前树根节点||false|SysTreeDTO|SysTreeDTO|
|&emsp;&emsp;&emsp;&emsp;ancestralChain|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessId|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessPageId|||false|string||
|&emsp;&emsp;&emsp;&emsp;createBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;createTime|||false|string||
|&emsp;&emsp;&emsp;&emsp;delFlag|||false|string||
|&emsp;&emsp;&emsp;&emsp;directParentId|||false|string||
|&emsp;&emsp;&emsp;&emsp;id|||false|string||
|&emsp;&emsp;&emsp;&emsp;labelsModel|||false|string||
|&emsp;&emsp;&emsp;&emsp;level|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lft|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;model|||false|integer||
|&emsp;&emsp;&emsp;&emsp;name|||false|string||
|&emsp;&emsp;&emsp;&emsp;oldId|||false|string||
|&emsp;&emsp;&emsp;&emsp;passId|||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|||false|string||
|&emsp;&emsp;&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;&emsp;&emsp;rgt|||false|integer||
|&emsp;&emsp;&emsp;&emsp;sameLevelLastId|||false|string||
|&emsp;&emsp;&emsp;&emsp;seq|||false|integer||
|&emsp;&emsp;&emsp;&emsp;showStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;status|||false|string||
|&emsp;&emsp;&emsp;&emsp;tenantWorkId|||false|string||
|&emsp;&emsp;&emsp;&emsp;type|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysWorkIndexVO»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysWorkIndexVO|SysWorkIndexVO|
|&emsp;&emsp;dirId||string||
|&emsp;&emsp;dirPath||string||
|&emsp;&emsp;lifeCount||integer(int32)||
|&emsp;&emsp;lockStatus||string||
|&emsp;&emsp;name||string||
|&emsp;&emsp;showStatus||string||
|&emsp;&emsp;sortIndex||integer(int32)||
|&emsp;&emsp;value||object||
|&emsp;&emsp;workId||string||
|&emsp;&emsp;workType||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"dirId": "",
		"dirPath": "",
		"lifeCount": 0,
		"lockStatus": "",
		"name": "",
		"showStatus": "",
		"sortIndex": 0,
		"value": {},
		"workId": "",
		"workType": ""
	}
}
```


## 根据id删除生命体二级分类空间集合


**接口地址**:`/life/subtype/space/delete`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 条件查询生命体二级分类空间集合


**接口地址**:`/life/subtype/space/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "lifeIds": "",
  "model": 0,
  "name": "",
  "oldParentId": "",
  "projectId": "",
  "sqlContent": "",
  "sysTreeDTO": {
    "ancestralChain": "",
    "businessId": "",
    "businessPageId": "",
    "createBy": "",
    "createTime": "",
    "delFlag": "",
    "directParentId": "",
    "id": "",
    "labelsModel": "",
    "level": 0,
    "lft": 0,
    "lockStatus": "",
    "model": 0,
    "name": "",
    "oldId": "",
    "passId": "",
    "projectId": "",
    "remark": "",
    "rgt": 0,
    "sameLevelLastId": "",
    "seq": 0,
    "showStatus": "",
    "status": "",
    "tenantWorkId": "",
    "type": "",
    "updateBy": "",
    "updateTime": ""
  }
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSubtypeSpaceCollectionSaveReq|新增生命体二级分类集合|body|true|LifeSubtypeSpaceCollectionSaveReq|LifeSubtypeSpaceCollectionSaveReq|
|&emsp;&emsp;id|生命体二级分类集合id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeIds|生命体ids，以逗号隔开||false|string||
|&emsp;&emsp;model|1：动态（执行SQL挂载）2：静态（手动添加生命体）||false|integer(int32)||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;oldParentId|旧父节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;sqlContent|SQL查询语句||false|string||
|&emsp;&emsp;sysTreeDTO|当前树根节点||false|SysTreeDTO|SysTreeDTO|
|&emsp;&emsp;&emsp;&emsp;ancestralChain|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessId|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessPageId|||false|string||
|&emsp;&emsp;&emsp;&emsp;createBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;createTime|||false|string||
|&emsp;&emsp;&emsp;&emsp;delFlag|||false|string||
|&emsp;&emsp;&emsp;&emsp;directParentId|||false|string||
|&emsp;&emsp;&emsp;&emsp;id|||false|string||
|&emsp;&emsp;&emsp;&emsp;labelsModel|||false|string||
|&emsp;&emsp;&emsp;&emsp;level|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lft|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;model|||false|integer||
|&emsp;&emsp;&emsp;&emsp;name|||false|string||
|&emsp;&emsp;&emsp;&emsp;oldId|||false|string||
|&emsp;&emsp;&emsp;&emsp;passId|||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|||false|string||
|&emsp;&emsp;&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;&emsp;&emsp;rgt|||false|integer||
|&emsp;&emsp;&emsp;&emsp;sameLevelLastId|||false|string||
|&emsp;&emsp;&emsp;&emsp;seq|||false|integer||
|&emsp;&emsp;&emsp;&emsp;showStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;status|||false|string||
|&emsp;&emsp;&emsp;&emsp;tenantWorkId|||false|string||
|&emsp;&emsp;&emsp;&emsp;type|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«lifeSubtypeSpaceCollectionRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||lifeSubtypeSpaceCollectionRes|lifeSubtypeSpaceCollectionRes|
|&emsp;&emsp;lifeSubtypeSpaceCollectionVOList||array|LifeSubtypeSpaceCollectionVO|
|&emsp;&emsp;&emsp;&emsp;id|生命体二级分类集合id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡id|string||
|&emsp;&emsp;&emsp;&emsp;lifeIds|所选生命体ids|string||
|&emsp;&emsp;&emsp;&emsp;model|1：动态（执行SQL挂载）2：静态（手动添加生命体）|integer||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;sqlContent|SQL查询语句|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"lifeSubtypeSpaceCollectionVOList": [
			{
				"id": "",
				"levelId": "",
				"lifeIds": "",
				"model": 0,
				"name": "",
				"projectId": "",
				"sqlContent": ""
			}
		]
	}
}
```


## 根据树节点id查询对应生命体列表


**接口地址**:`/life/subtype/space/queryLifeDataByTreeId`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|collectionId|collectionId|query|true|string||
|current|current|query|true|integer(int32)||
|size|size|query|true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«LifeDataVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«LifeDataVO»|IPage«LifeDataVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|LifeDataVO|
|&emsp;&emsp;&emsp;&emsp;id|id|string||
|&emsp;&emsp;&emsp;&emsp;levelId|关卡ID|string||
|&emsp;&emsp;&emsp;&emsp;lifeTemplateId|生命体模板ID|string||
|&emsp;&emsp;&emsp;&emsp;lockStatus|锁定状态|string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目ID|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;showStatus|显示隐藏|string||
|&emsp;&emsp;&emsp;&emsp;type|类型|string||
|&emsp;&emsp;&emsp;&emsp;value|键值|object||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"id": "",
				"levelId": "",
				"lifeTemplateId": "",
				"lockStatus": "",
				"name": "",
				"projectId": "",
				"remark": "",
				"showStatus": "",
				"type": "",
				"value": {}
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 根据id修改生命体二级分类空间集合


**接口地址**:`/life/subtype/space/update`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "levelId": "",
  "lifeIds": "",
  "model": 0,
  "name": "",
  "oldParentId": "",
  "projectId": "",
  "sqlContent": "",
  "sysTreeDTO": {
    "ancestralChain": "",
    "businessId": "",
    "businessPageId": "",
    "createBy": "",
    "createTime": "",
    "delFlag": "",
    "directParentId": "",
    "id": "",
    "labelsModel": "",
    "level": 0,
    "lft": 0,
    "lockStatus": "",
    "model": 0,
    "name": "",
    "oldId": "",
    "passId": "",
    "projectId": "",
    "remark": "",
    "rgt": 0,
    "sameLevelLastId": "",
    "seq": 0,
    "showStatus": "",
    "status": "",
    "tenantWorkId": "",
    "type": "",
    "updateBy": "",
    "updateTime": ""
  }
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|lifeSubtypeSpaceCollectionSaveReq|新增生命体二级分类集合|body|true|LifeSubtypeSpaceCollectionSaveReq|LifeSubtypeSpaceCollectionSaveReq|
|&emsp;&emsp;id|生命体二级分类集合id||false|string||
|&emsp;&emsp;levelId|关卡id||false|string||
|&emsp;&emsp;lifeIds|生命体ids，以逗号隔开||false|string||
|&emsp;&emsp;model|1：动态（执行SQL挂载）2：静态（手动添加生命体）||false|integer(int32)||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;oldParentId|旧父节点id||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;sqlContent|SQL查询语句||false|string||
|&emsp;&emsp;sysTreeDTO|当前树根节点||false|SysTreeDTO|SysTreeDTO|
|&emsp;&emsp;&emsp;&emsp;ancestralChain|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessId|||false|string||
|&emsp;&emsp;&emsp;&emsp;businessPageId|||false|string||
|&emsp;&emsp;&emsp;&emsp;createBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;createTime|||false|string||
|&emsp;&emsp;&emsp;&emsp;delFlag|||false|string||
|&emsp;&emsp;&emsp;&emsp;directParentId|||false|string||
|&emsp;&emsp;&emsp;&emsp;id|||false|string||
|&emsp;&emsp;&emsp;&emsp;labelsModel|||false|string||
|&emsp;&emsp;&emsp;&emsp;level|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lft|||false|integer||
|&emsp;&emsp;&emsp;&emsp;lockStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;model|||false|integer||
|&emsp;&emsp;&emsp;&emsp;name|||false|string||
|&emsp;&emsp;&emsp;&emsp;oldId|||false|string||
|&emsp;&emsp;&emsp;&emsp;passId|||false|string||
|&emsp;&emsp;&emsp;&emsp;projectId|||false|string||
|&emsp;&emsp;&emsp;&emsp;remark|||false|string||
|&emsp;&emsp;&emsp;&emsp;rgt|||false|integer||
|&emsp;&emsp;&emsp;&emsp;sameLevelLastId|||false|string||
|&emsp;&emsp;&emsp;&emsp;seq|||false|integer||
|&emsp;&emsp;&emsp;&emsp;showStatus|||false|string||
|&emsp;&emsp;&emsp;&emsp;status|||false|string||
|&emsp;&emsp;&emsp;&emsp;tenantWorkId|||false|string||
|&emsp;&emsp;&emsp;&emsp;type|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|||false|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysWorkIndexVO»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysWorkIndexVO|SysWorkIndexVO|
|&emsp;&emsp;dirId||string||
|&emsp;&emsp;dirPath||string||
|&emsp;&emsp;lifeCount||integer(int32)||
|&emsp;&emsp;lockStatus||string||
|&emsp;&emsp;name||string||
|&emsp;&emsp;showStatus||string||
|&emsp;&emsp;sortIndex||integer(int32)||
|&emsp;&emsp;value||object||
|&emsp;&emsp;workId||string||
|&emsp;&emsp;workType||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"dirId": "",
		"dirPath": "",
		"lifeCount": 0,
		"lockStatus": "",
		"name": "",
		"showStatus": "",
		"sortIndex": 0,
		"value": {},
		"workId": "",
		"workType": ""
	}
}
```


# 部门表对象功能接口


## 根据id查询数据


**接口地址**:`/sys-dept`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysDeptRes»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysDeptRes|SysDeptRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;email|邮箱|string||
|&emsp;&emsp;id|唯一id|string||
|&emsp;&emsp;leader|负责人|string||
|&emsp;&emsp;name|部门名称|string||
|&emsp;&emsp;parentId|父部门id|string||
|&emsp;&emsp;phone|电话|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|部门状态（0正常、1停用）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"email": "",
		"id": "",
		"leader": "",
		"name": "",
		"parentId": "",
		"phone": "",
		"sort": 0,
		"status": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 添加数据


**接口地址**:`/sys-dept`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "email": "",
  "id": "",
  "leader": "",
  "name": "",
  "parentId": "",
  "phone": "",
  "size": 0,
  "sort": 0,
  "status": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDeptReq|部门查询|body|true|SysDeptReq|SysDeptReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;email|邮箱||false|string||
|&emsp;&emsp;id|唯一id||false|string||
|&emsp;&emsp;leader|负责人||false|string||
|&emsp;&emsp;name|部门名称||false|string||
|&emsp;&emsp;parentId|父部门id||false|string||
|&emsp;&emsp;phone|电话||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序||false|integer(int32)||
|&emsp;&emsp;status|部门状态（0正常、1停用）||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysDeptRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysDeptRes|SysDeptRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;email|邮箱|string||
|&emsp;&emsp;id|唯一id|string||
|&emsp;&emsp;leader|负责人|string||
|&emsp;&emsp;name|部门名称|string||
|&emsp;&emsp;parentId|父部门id|string||
|&emsp;&emsp;phone|电话|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|部门状态（0正常、1停用）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"email": "",
		"id": "",
		"leader": "",
		"name": "",
		"parentId": "",
		"phone": "",
		"sort": 0,
		"status": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 根据id更新数据


**接口地址**:`/sys-dept`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "email": "",
  "id": "",
  "leader": "",
  "name": "",
  "parentId": "",
  "phone": "",
  "size": 0,
  "sort": 0,
  "status": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDeptReq|部门查询|body|true|SysDeptReq|SysDeptReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;email|邮箱||false|string||
|&emsp;&emsp;id|唯一id||false|string||
|&emsp;&emsp;leader|负责人||false|string||
|&emsp;&emsp;name|部门名称||false|string||
|&emsp;&emsp;parentId|父部门id||false|string||
|&emsp;&emsp;phone|电话||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序||false|integer(int32)||
|&emsp;&emsp;status|部门状态（0正常、1停用）||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«SysDeptRes»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||SysDeptRes|SysDeptRes|
|&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;email|邮箱|string||
|&emsp;&emsp;id|唯一id|string||
|&emsp;&emsp;leader|负责人|string||
|&emsp;&emsp;name|部门名称|string||
|&emsp;&emsp;parentId|父部门id|string||
|&emsp;&emsp;phone|电话|string||
|&emsp;&emsp;sort|排序|integer(int32)||
|&emsp;&emsp;status|部门状态（0正常、1停用）|string||
|&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"createBy": "",
		"createTime": "",
		"email": "",
		"id": "",
		"leader": "",
		"name": "",
		"parentId": "",
		"phone": "",
		"sort": 0,
		"status": "",
		"updateBy": "",
		"updateTime": ""
	}
}
```


## 根据ids删除数据


**接口地址**:`/sys-dept`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
[]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|ids|ids列表|body|true|array|string|


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«int»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||integer(int32)|integer(int32)|


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": 0
}
```


## 分页条件查询数据


**接口地址**:`/sys-dept/queryPage`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "current": 0,
  "email": "",
  "id": "",
  "leader": "",
  "name": "",
  "parentId": "",
  "phone": "",
  "size": 0,
  "sort": 0,
  "status": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|sysDeptReq|部门查询|body|true|SysDeptReq|SysDeptReq|
|&emsp;&emsp;current|起始页||false|integer(int64)||
|&emsp;&emsp;email|邮箱||false|string||
|&emsp;&emsp;id|唯一id||false|string||
|&emsp;&emsp;leader|负责人||false|string||
|&emsp;&emsp;name|部门名称||false|string||
|&emsp;&emsp;parentId|父部门id||false|string||
|&emsp;&emsp;phone|电话||false|string||
|&emsp;&emsp;size|每页条数||false|integer(int32)||
|&emsp;&emsp;sort|排序||false|integer(int32)||
|&emsp;&emsp;status|部门状态（0正常、1停用）||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«Page«SysDeptRes»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||Page«SysDeptRes»|Page«SysDeptRes»|
|&emsp;&emsp;countId||string||
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;maxLimit||integer(int64)||
|&emsp;&emsp;optimizeCountSql||boolean||
|&emsp;&emsp;orders||array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc||boolean||
|&emsp;&emsp;&emsp;&emsp;column||string||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|SysDeptRes|
|&emsp;&emsp;&emsp;&emsp;createBy|创建者|string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;email|邮箱|string||
|&emsp;&emsp;&emsp;&emsp;id|唯一id|string||
|&emsp;&emsp;&emsp;&emsp;leader|负责人|string||
|&emsp;&emsp;&emsp;&emsp;name|部门名称|string||
|&emsp;&emsp;&emsp;&emsp;parentId|父部门id|string||
|&emsp;&emsp;&emsp;&emsp;phone|电话|string||
|&emsp;&emsp;&emsp;&emsp;sort|排序|integer||
|&emsp;&emsp;&emsp;&emsp;status|部门状态（0正常、1停用）|string||
|&emsp;&emsp;&emsp;&emsp;updateBy|更新者|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;searchCount||boolean||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"countId": "",
		"current": 0,
		"maxLimit": 0,
		"optimizeCountSql": true,
		"orders": [
			{
				"asc": true,
				"column": ""
			}
		],
		"pages": 0,
		"records": [
			{
				"createBy": "",
				"createTime": "",
				"email": "",
				"id": "",
				"leader": "",
				"name": "",
				"parentId": "",
				"phone": "",
				"sort": 0,
				"status": "",
				"updateBy": "",
				"updateTime": ""
			}
		],
		"searchCount": true,
		"size": 0,
		"total": 0
	}
}
```


# 项目场景


## 新增单条数据


**接口地址**:`/projectScene`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": "",
  "projectId": "",
  "remark": "",
  "sceneFileUrl": "",
  "sceneVersion": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectSceneReq|项目场景请求体|body|true|ProjectSceneReq|ProjectSceneReq|
|&emsp;&emsp;id|||false|string||
|&emsp;&emsp;name|场景名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;sceneFileUrl|场景文件url||false|string||
|&emsp;&emsp;sceneVersion|场景版本||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 通过主键id修改单条数据


**接口地址**:`/projectScene`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": "",
  "projectId": "",
  "remark": "",
  "sceneFileUrl": "",
  "sceneVersion": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectSceneReq|项目场景请求体|body|true|ProjectSceneReq|ProjectSceneReq|
|&emsp;&emsp;id|||false|string||
|&emsp;&emsp;name|场景名称||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;sceneFileUrl|场景文件url||false|string||
|&emsp;&emsp;sceneVersion|场景版本||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 分页查询数据


**接口地址**:`/projectScene/page/{pageNum}/{pageSize}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pageNum|当前页|path|true|integer(int32)||
|pageSize|每页条数|path|true|integer(int32)||
|id||query|false|string||
|name |场景名称|query|false|string||
|projectId|项目id|query|false|string||
|remark|备注|query|false|string||
|sceneFileUrl|场景文件url|query|false|string||
|sceneVersion|场景版本|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«ProjectSceneVO»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«ProjectSceneVO»|IPage«ProjectSceneVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|ProjectSceneVO|
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;name|场景名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;sceneFileUrl|场景文件url|string||
|&emsp;&emsp;&emsp;&emsp;sceneVersion|场景版本|string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"id": "",
				"name": "",
				"projectId": "",
				"remark": "",
				"sceneFileUrl": "",
				"sceneVersion": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 上传项目场景文件


**接口地址**:`/projectScene/uploadSceneFile`


**请求方式**:`POST`


**请求数据类型**:`multipart/form-data`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|file|项目场景文件|query|true|file||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«string»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": ""
}
```


## 通过id主键查询单条数据


**接口地址**:`/projectScene/{id}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id主键|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«ProjectSceneVO»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||ProjectSceneVO|ProjectSceneVO|
|&emsp;&emsp;id||string||
|&emsp;&emsp;name|场景名称|string||
|&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sceneFileUrl|场景文件url|string||
|&emsp;&emsp;sceneVersion|场景版本|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"id": "",
		"name": "",
		"projectId": "",
		"remark": "",
		"sceneFileUrl": "",
		"sceneVersion": ""
	}
}
```


## 通过id主键删除单条数据


**接口地址**:`/projectScene/{id}`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id主键|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


# 项目工具


## 新增单条数据


**接口地址**:`/projectTool`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "projectId": "",
  "remark": "",
  "toolFileUrl": "",
  "toolVersion": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectToolReq|项目工具Req|body|true|ProjectToolReq|ProjectToolReq|
|&emsp;&emsp;id|||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;toolFileUrl|工具文件url||false|string||
|&emsp;&emsp;toolVersion|工具版本||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 通过主键id修改单条数据


**接口地址**:`/projectTool`


**请求方式**:`PUT`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "projectId": "",
  "remark": "",
  "toolFileUrl": "",
  "toolVersion": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectToolReq|项目工具Req|body|true|ProjectToolReq|ProjectToolReq|
|&emsp;&emsp;id|||false|string||
|&emsp;&emsp;projectId|项目id||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;toolFileUrl|工具文件url||false|string||
|&emsp;&emsp;toolVersion|工具版本||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


## 分页查询数据


**接口地址**:`/projectTool/page/{pageNum}/{pageSize}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pageNum|当前页|path|true|integer(int32)||
|pageSize|每页条数|path|true|integer(int32)||
|projectId|项目id|query|true|string||
|id||query|false|string||
|remark|备注|query|false|string||
|toolFileUrl|工具文件url|query|false|string||
|toolVersion|工具版本|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«ProjectToolVO»»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«ProjectToolVO»|IPage«ProjectToolVO»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|ProjectToolVO|
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;toolFileUrl|工具文件url|string||
|&emsp;&emsp;&emsp;&emsp;toolVersion|工具版本|string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"id": "",
				"projectId": "",
				"remark": "",
				"toolFileUrl": "",
				"toolVersion": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 上传项目工具文件


**接口地址**:`/projectTool/uploadToolFile`


**请求方式**:`POST`


**请求数据类型**:`multipart/form-data`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|file|项目工具文件|query|true|file||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«string»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": ""
}
```


## 通过id主键查询单条数据


**接口地址**:`/projectTool/{id}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id主键|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«ProjectToolVO»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||ProjectToolVO|ProjectToolVO|
|&emsp;&emsp;id||string||
|&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;toolFileUrl|工具文件url|string||
|&emsp;&emsp;toolVersion|工具版本|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"id": "",
		"projectId": "",
		"remark": "",
		"toolFileUrl": "",
		"toolVersion": ""
	}
}
```


## 通过id主键删除单条数据


**接口地址**:`/projectTool/{id}`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id主键|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«boolean»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||boolean||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": true
}
```


# 项目管理


## 删除项目


**接口地址**:`/project/delete`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 条件查询项目


**接口地址**:`/project/query`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": "",
  "remark": "",
  "sceneBindId": "",
  "thumbnailUrl": "",
  "toolBindId": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectReq|projectReq|body|true|项目对象0|项目对象0|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;sceneBindId|绑定场景id||false|string||
|&emsp;&emsp;thumbnailUrl|项目缩略图url||false|string||
|&emsp;&emsp;toolBindId|绑定工具id||false|string||
|&emsp;&emsp;type|类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«项目对象»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|项目对象|
|&emsp;&emsp;id||string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sceneBindId|绑定场景id|string||
|&emsp;&emsp;thumbnailUrl|项目缩略图url|string||
|&emsp;&emsp;toolBindId|绑定工具id|string||
|&emsp;&emsp;type|类型|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"id": "",
			"name": "",
			"remark": "",
			"sceneBindId": "",
			"thumbnailUrl": "",
			"toolBindId": "",
			"type": ""
		}
	]
}
```


## 条件查询项目以及对应的关卡


**接口地址**:`/project/queryListWithLevel`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": "",
  "remark": "",
  "sceneBindId": "",
  "thumbnailUrl": "",
  "toolBindId": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectReq|projectReq|body|true|项目对象0|项目对象0|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;sceneBindId|绑定场景id||false|string||
|&emsp;&emsp;thumbnailUrl|项目缩略图url||false|string||
|&emsp;&emsp;toolBindId|绑定工具id||false|string||
|&emsp;&emsp;type|类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«List«ProjectLevelQueryVO»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||array|ProjectLevelQueryVO|
|&emsp;&emsp;id|id|string||
|&emsp;&emsp;levelList|关卡列表|array|LevelVO|
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;remark|标记|string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sceneBindId|绑定场景id|string||
|&emsp;&emsp;thumbnailUrl|项目缩略图url|string||
|&emsp;&emsp;toolBindId|绑定工具id|string||
|&emsp;&emsp;type|类型|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": [
		{
			"id": "",
			"levelList": [
				{
					"id": "",
					"name": "",
					"projectId": "",
					"remark": ""
				}
			],
			"name": "",
			"remark": "",
			"sceneBindId": "",
			"thumbnailUrl": "",
			"toolBindId": "",
			"type": ""
		}
	]
}
```


## 分页查询项目


**接口地址**:`/project/queryPageList`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "countId": "",
  "current": 0,
  "id": "",
  "maxLimit": 0,
  "name": "",
  "optimizeCountSql": true,
  "optimizeJoinOfCountSql": true,
  "orders": [
    {
      "asc": true,
      "column": ""
    }
  ],
  "pages": 0,
  "records": [],
  "remark": "",
  "sceneBindId": "",
  "searchCount": true,
  "size": 0,
  "thumbnailUrl": "",
  "toolBindId": "",
  "total": 0,
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectPageListQueryReq|项目分页查询请求体|body|true|ProjectPageListQueryReq|ProjectPageListQueryReq|
|&emsp;&emsp;countId|||false|string||
|&emsp;&emsp;current|||false|integer(int64)||
|&emsp;&emsp;id|项目id||false|string||
|&emsp;&emsp;maxLimit|||false|integer(int64)||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;optimizeCountSql|||false|boolean||
|&emsp;&emsp;optimizeJoinOfCountSql|||false|boolean||
|&emsp;&emsp;orders|||false|array|OrderItem|
|&emsp;&emsp;&emsp;&emsp;asc|||false|boolean||
|&emsp;&emsp;&emsp;&emsp;column|||false|string||
|&emsp;&emsp;pages|||false|integer(int64)||
|&emsp;&emsp;records|||false|array|object|
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;sceneBindId|绑定场景id||false|string||
|&emsp;&emsp;searchCount|||false|boolean||
|&emsp;&emsp;size|||false|integer(int64)||
|&emsp;&emsp;thumbnailUrl|项目缩略图url||false|string||
|&emsp;&emsp;toolBindId|绑定工具id||false|string||
|&emsp;&emsp;total|||false|integer(int64)||
|&emsp;&emsp;type|类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«IPage«ProjectPO对象»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||IPage«ProjectPO对象»|IPage«ProjectPO对象»|
|&emsp;&emsp;current||integer(int64)||
|&emsp;&emsp;pages||integer(int64)||
|&emsp;&emsp;records||array|ProjectPO对象|
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;&emsp;&emsp;sceneBindId|绑定场景id|string||
|&emsp;&emsp;&emsp;&emsp;thumbnailUrl|项目缩略图url|string||
|&emsp;&emsp;&emsp;&emsp;toolBindId|绑定工具id|string||
|&emsp;&emsp;&emsp;&emsp;type|类型|string||
|&emsp;&emsp;size||integer(int64)||
|&emsp;&emsp;total||integer(int64)||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"current": 0,
		"pages": 0,
		"records": [
			{
				"id": "",
				"name": "",
				"remark": "",
				"sceneBindId": "",
				"thumbnailUrl": "",
				"toolBindId": "",
				"type": ""
			}
		],
		"size": 0,
		"total": 0
	}
}
```


## 新增项目


**接口地址**:`/project/save`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": "",
  "remark": "",
  "sceneBindId": "",
  "thumbnailUrl": "",
  "toolBindId": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectSaveReq|projectSaveReq|body|true|项目对象0|项目对象0|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;sceneBindId|绑定场景id||false|string||
|&emsp;&emsp;thumbnailUrl|项目缩略图url||false|string||
|&emsp;&emsp;toolBindId|绑定工具id||false|string||
|&emsp;&emsp;type|类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«ProjectInsertVO»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||ProjectInsertVO|ProjectInsertVO|
|&emsp;&emsp;id||string||
|&emsp;&emsp;level|默认关卡信息|LevelAndTreeVO|LevelAndTreeVO|
|&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;name|名称|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;&emsp;&emsp;remark|标记|string||
|&emsp;&emsp;&emsp;&emsp;tree|树信息|LevelTreeVO|LevelTreeVO|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;businessId||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;id||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;model||integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;name||string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;projectId||string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sceneBindId|绑定场景id|string||
|&emsp;&emsp;thumbnailUrl|项目缩略图url|string||
|&emsp;&emsp;toolBindId|绑定工具id|string||
|&emsp;&emsp;type|类型|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"id": "",
		"level": {
			"id": "",
			"name": "",
			"projectId": "",
			"remark": "",
			"tree": {
				"businessId": "",
				"id": "",
				"model": 0,
				"name": "",
				"projectId": ""
			}
		},
		"name": "",
		"remark": "",
		"sceneBindId": "",
		"thumbnailUrl": "",
		"toolBindId": "",
		"type": ""
	}
}
```


## 更新项目


**接口地址**:`/project/update`


**请求方式**:`POST`


**请求数据类型**:`application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "id": "",
  "name": "",
  "remark": "",
  "sceneBindId": "",
  "thumbnailUrl": "",
  "toolBindId": "",
  "type": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectReq|projectReq|body|true|项目对象0|项目对象0|
|&emsp;&emsp;id|id||false|string||
|&emsp;&emsp;name|名称||false|string||
|&emsp;&emsp;remark|备注||false|string||
|&emsp;&emsp;sceneBindId|绑定场景id||false|string||
|&emsp;&emsp;thumbnailUrl|项目缩略图url||false|string||
|&emsp;&emsp;toolBindId|绑定工具id||false|string||
|&emsp;&emsp;type|类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||object||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {}
}
```


## 上传项目缩略图


**接口地址**:`/project/uploadThumbnail`


**请求方式**:`POST`


**请求数据类型**:`multipart/form-data`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|file|缩略图文件|query|true|file||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«string»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": ""
}
```


## 根据ID获取项目信息


**接口地址**:`/project/{id}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|id|id|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ResResult«项目对象»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|exception||string||
|msg||string||
|success||boolean||
|value||项目对象|项目对象|
|&emsp;&emsp;id||string||
|&emsp;&emsp;name|名称|string||
|&emsp;&emsp;remark|备注|string||
|&emsp;&emsp;sceneBindId|绑定场景id|string||
|&emsp;&emsp;thumbnailUrl|项目缩略图url|string||
|&emsp;&emsp;toolBindId|绑定工具id|string||
|&emsp;&emsp;type|类型|string||


**响应示例**:
```javascript
{
	"code": 0,
	"exception": "",
	"msg": "",
	"success": true,
	"value": {
		"id": "",
		"name": "",
		"remark": "",
		"sceneBindId": "",
		"thumbnailUrl": "",
		"toolBindId": "",
		"type": ""
	}
}
```