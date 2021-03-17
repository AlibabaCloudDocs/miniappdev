# CreateFunction

调用CreateFunction创建云函数。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=CreateFunction&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateFunction|系统规定参数。取值：**CreateFunction**。 |
|Name|String|是|demoFunction|函数名称。

 函数名称长度在1-30个字符间，只能包含字母、数字、下划线和中划线，不能以数字、中划线开头。

 **说明：** 云函数的名称必须和要上传的Node.js代码包名称一致。 |
|SpaceId|String|是|dece4ea0-d432-4cfa-8514-xxxxx|云函数所属的服务空间ID。 |
|Desc|String|否|测试函数|云函数的描述信息。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CreatedAt|String|2019-06-20T09:33:57.445Z|创建时间。 |
|Desc|String|测试函数|函数描述。 |
|ModifiedAt|String|2019-06-20T09:33:57.445Z|修改时间。 |
|Name|String|demoFunction|函数名称。 |
|RequestId|String|C1111725-1CD4-4787-A815-879B8F5268F6|请求ID。 |
|Spec|Struct| |云函数运行参数。 |
|InstanceConcurrency|String|1|单实例允许的最大并发度 |
|Memory|String|128 MB|内存大小。 |
|Runtime|String|Node.js 8|运行环境。 |
|Timeout|String|5s|超时时间。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateFunction
&Name=demoFunction
&SpaceId=dece4ea0-d432-4cfa-8514-8a88d205e2b8
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ModifiedAt>2019-06-20T03:22:54.854Z</ModifiedAt>
<Desc>xxx</Desc>
<RequestId>319DADF8-0BE9-4AAB-B3C1-4EA07ACE35CE</RequestId>
<CreatedAt>2019-06-20T03:22:54.854Z</CreatedAt>
<Spec>
    <InstanceConcurrency>1</InstanceConcurrency>
    <Runtime>Node.js 8</Runtime>
    <Timeout>5s</Timeout>
    <Memory>128 MB</Memory>
</Spec>
<Name>sayHello</Name>
```

`JSON`格式

```
{
  "ModifiedAt": "2019-06-20T03:22:54.854Z",
  "Desc": "xxx",
  "RequestId": "319DADF8-0BE9-4AAB-B3C1-4EA07ACE35CE",
  "CreatedAt": "2019-06-20T03:22:54.854Z",
  "Spec": {
    "InstanceConcurrency" : 1,
    "Runtime": "Node.js 8",
    "Timeout": "5s",
    "Memory": "128 MB"
  },
  "Name": "sayHello"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/MPServerless)查看更多错误码。

访问[错误中心](https://error-center.alibabacloud.com/status/product/MPServerless)查看更多错误码。

