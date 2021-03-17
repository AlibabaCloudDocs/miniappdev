# ListFunction

调用ListFunction查询已创建的云函数列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=ListFunction&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListFunction|系统规定参数。取值：ListFunction。 |
|SpaceId|String|是|dece4ea0-d432-4cfa-\*\*\*\*-8a88d205e2b8|云函数所属的服务空间ID。 |
|PageNum|Integer|否|1|页码。从第1页开始。 |
|PageSize|Integer|否|10|每页显示的行数。默认为10。 |
|FilterBy|String|否|demo|查询条件。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|DataList|Array of DataList| |云函数详情。 |
|CreatedAt|String|2019-06-21T02:22:55.996Z|云函数创建时间。 |
|Desc|String|test|云函数描述。 |
|HttpTriggerPath|String|/http/hello|HTTP触发的路径。 |
|ModifiedAt|String|2019-06-21T02:22:55.996Z|云函数修改时间。 |
|Name|String|demoFunction|云函数名称。 |
|Spec|Struct| |云函数运行参数。 |
|InstanceConcurrency|Integer|1|单实例允许的最大并发度 |
|Memory|String|128 MB|内存大小。 |
|Runtime|String|Node.js 8|运行环境。 |
|Timeout|String|5s|超时时间。 |
|TimingTriggerConfig|String|cron:0 0 \* \* \* \*|定时触发配置。 |
|Paginator|Struct| |分页信息。 |
|PageCount|Integer|1|查询的页数。 |
|PageNum|Integer|1|列表的页码。 |
|PageSize|Integer|10|分页查询时设置的每页行数。 |
|Total|Integer|1|查询的云函数总数。 |
|RequestId|String|D388FE2B-61D5-4A76-A8F0-xxxx|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ListFunction
&FilterBy=demo
&PageNum=1
&SpaceId=dece4ea0-d432-4cfa-****-8a88d205e2b8
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<RequestId>319DADF8-0BE9-4AAB-B3C1-4EA07ACE35CE</RequestId>
<Paginator>
    <Total>1</Total>
    <PageNum>1</PageNum>
    <PageSize>10</PageSize>
    <PageCount>1</PageCount>
</Paginator>
<DataList>
    <Name>testFunction</Name>
    <Desc/>
    <HttpTriggerPath>/http/hello</HttpTriggerPath>
    <CreatedAt>2019-06-10T02:33:16.674Z</CreatedAt>
    <ModifiedAt>2019-06-10T02:33:16.674Z</ModifiedAt>
    <TimingTriggerConfig>cron:0 0 * * * *</TimingTriggerConfig>
    <Spec>
        <InstanceConcurrency>1</InstanceConcurrency>
        <Memory>128 MB</Memory>
        <Timeout>5s</Timeout>
        <Runtime>Node.js 8</Runtime>
    </Spec>
</DataList>
```

`JSON`格式

```
{
    "RequestId": "319DADF8-0BE9-4AAB-B3C1-4EA07ACE35CE",
    "Paginator": {
        "Total": 1,
        "PageNum": 1,
        "PageSize": 10,
        "PageCount": 1
    },
    "DataList": [
        {
            "Name": "testFunction",
            "Desc": "",
            "HttpTriggerPath": "/http/hello",
            "CreatedAt": "2019-06-10T02:33:16.674Z",
            "ModifiedAt": "2019-06-10T02:33:16.674Z",
            "TimingTriggerConfig": "cron:0 0 * * * *",
            "Spec": {
                "InstanceConcurrency": 1,
                "Memory": "128 MB",
                "Timeout": "5s",
                "Runtime": "Node.js 8"
            }
        }
    ]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/MPServerless)查看更多错误码。

访问[错误中心](https://error-center.alibabacloud.com/status/product/MPServerless)查看更多错误码。

