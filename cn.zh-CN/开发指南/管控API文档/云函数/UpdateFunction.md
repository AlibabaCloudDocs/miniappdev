# UpdateFunction

调用UpdateFunction更新函数信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=UpdateFunction&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|UpdateFunction|系统规定参数。取值：UpdateFunction。 |
|Name|String|是|demoFunction|云函数名称。 |
|SpaceId|String|是|dece4ea0-d432-4cfa-8514-8a88d205e2b8|服务空间ID。 |
|Desc|String|否|description|云函数描述。 |
|Memory|Integer|否|256|函数内存规格，取值为64的倍数，至少128，至多3072。 |
|Timeout|Integer|否|5|函数超时时间，单位为秒，默认值为5，取值范围1-10。 |
|HttpTriggerPath|String|否|/http/hello|HTTP触发的路径，设置为空字符串表示取消该功能。必须以`/http`开头，不能以`/`结尾，同一个Space下不允许重复，只支持（/）、（-）、（\_）、（.）、字母和数字组合，最长不超过128个字符。 |
|TimingTriggerConfig|String|否|cron:0 0 \* \* \* \*|定时触发配置，设置为空字符串表示取消该功能，配置规则请参见[使用云函数定时触发功能](https://help.aliyun.com/document_detail/160666.htm)。 |
|InstanceConcurrency|Integer|否|1|单实例允许的最大并发度，默认值为1，取值范围1-100。设置单实例多并发可以降低冷启动的频率，适用于函数中有较多时间在等待下游服务响应的场景，不适用于函数中有共享状态且不能并发访问的场景，也不适用于单个请求的执行要消耗大量CPU及内存资源的场景。 |
|Runtime|String|否|nodejs8|云函数执行环境，可选值nodejs8,nodejs12。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CreatedAt|String|2019-06-20T03:22:54.854Z|云函数的创建时间。 |
|Desc|String|description|云函数的描述信息。 |
|HttpTriggerPath|String|/http/hello|HTTP触发的路径。 |
|ModifiedAt|String|2019-06-20T03:22:54.854Z|云函数的修改时间。 |
|Name|String|demoFunction|云函数的名称。 |
|RequestId|String|C293BB03-B6AD-46C2-80D1-19C8FB573916|请求ID。 |
|Spec|Struct| |云函数运行参数。 |
|InstanceConcurrency|Integer|1|单实例允许的最大并发度 |
|Memory|String|128 MB|内存大小。 |
|Runtime|String|Node.js 8|运行环境。 |
|Timeout|String|5s|超时时间。 |
|TimingTriggerConfig|String|cron:0 0 \* \* \* \*|定时触发配置。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=UpdateFunction
&Name=demoFunction
&SpaceId=dece4ea0-d432-4cfa-8514-8a88d205e2b8
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ModifiedAt>2019-06-20T03:22:54.854Z</ModifiedAt>
<Desc>xxx</Desc>
<HttpTriggerPath>/http/hello</HttpTriggerPath>
<RequestId>319DADF8-0BE9-4AAB-B3C1-4EA07ACE35CE</RequestId>
<CreatedAt>2019-06-20T03:22:54.854Z</CreatedAt>
<TimingTriggerConfig>cron:0 0 * * * *</TimingTriggerConfig>
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
    "HttpTriggerPath": "/http/hello",
    "RequestId": "319DADF8-0BE9-4AAB-B3C1-4EA07ACE35CE",
    "CreatedAt": "2019-06-20T03:22:54.854Z",
    "TimingTriggerConfig": "cron:0 0 * * * *",
    "Spec": {
        "InstanceConcurrency": 1,
        "Runtime": "Node.js 8",
        "Timeout": "5s",
        "Memory": "128 MB"
    },
    "Name": "sayHello"
}
```

