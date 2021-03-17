# DescribeFunction

调用DescribeFunction查询已创建的云函数详情。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=DescribeFunction&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeFunction|要执行的操作。取值：**DescribeFunction**。 |
|Name|String|是|demoFunction|云函数名称。 |
|SpaceId|String|是|dece4ea0-d432-4cfa-8514-xxxx|云函数所属的服务空间ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Deployment|Struct| |部署单详情。 |
|CreatedAt|String|2019-06-11T10:51:19.069Z|创建时间。 |
|DeploymentId|String|5cff17271c9d4401e92081c8|部署单ID。 |
|DownloadSignedUrl|String|http://bucket.oss-cn-shanghai.aliyuncs.com/xxxx-v2.zip?OSSAccessKeyId=LTAIKC\*\*\*\*\*1DkK6&Expires=1561425220&Signature=xEuiAgUMShQ4v8fYIl3FM8Jp3MA%3D|下载URL。 |
|ModifiedAt|String|2019-06-11T10:51:19.069Z|修改时间。 |
|VersionNo|String|2019061110511905080|版本号。版本号是部署单上传的时间。 |
|Function|Struct| |云函数信息。 |
|CreatedAt|String|2019-06-21T02:22:53.309Z|云函数创建时间。 |
|Desc|String|test|云函数描述信息。 |
|HttpTriggerPath|String|/http/hello|HTTP触发的路径。 |
|ModifiedAt|String|2019-06-21T02:22:53.309Z|修改时间。 |
|Name|String|demoFunction|云函数名称。 |
|Spec|Struct| |云函数运行参数。 |
|InstanceConcurrency|Integer|1|单实例允许的最大并发度 |
|Memory|String|128 MB|内存大小。 |
|Runtime|String|Node.js 8|运行环境。 |
|Timeout|String|5s|超时时间。 |
|TimingTriggerConfig|String|cron:0 0 \* \* \* \*|定时触发配置。 |
|RequestId|String|D388FE2B-61D5-4A76-A8F0-E7927F69CE65|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeFunction
&Name=demoFunction
&SpaceId=dece4ea0-d432-4cfa-8514-xxxx
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<RequestId>D388FE2B-61D5-4A76-A8F0-E7927F69CE65</RequestId>
<Function>
    <Name>TestFunction</Name>
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
</Function>
<Deployment>
    <DeploymentId>fun-5cebf6a81c9d44e6b85d33ae-xxxx</DeploymentId>
    <VersionNo>5</VersionNo>
    <CreatedAt>2019-06-10T02:33:16.674Z</CreatedAt>
    <ModifiedAt>2019-06-10T02:33:16.674Z</ModifiedAt>
    <DownloadSignedUrl>http://function-apiserver-test.oss-cn-shanghai.aliyuncs.com/fc-source/fun-xxxxx-v1.tgz?OSSAccessKeyId=LTAIKCq5xHz1DkK6&amp;Expires=1559805752&amp;Signature=BXyrc9Nrsvw7j53HxtkLoGkDhDI%3D</DownloadSignedUrl>
</Deployment>
```

`JSON`格式

```
{
    "RequestId": "D388FE2B-61D5-4A76-A8F0-E7927F69CE65",
    "Function": {
        "Name": "TestFunction",
        "Desc": "",
        "HttpTriggerPath": "/http/hello",
        "CreatedAt": "2019-06-10T02:33:16.674Z",
        "ModifiedAt": "2019-06-10T02:33:16.674Z",
        "TimingTriggerConfig": "cron:0 0 * * * *",
        "Spec": {
            "InstanceConcurrency" : 1,
            "Memory": "128 MB",
            "Timeout": "5s",
            "Runtime": "Node.js 8"
        }
    },
    "Deployment": {
        "DeploymentId": "fun-5cebf6a81c9d44e6b85d33ae-xxxx",
        "VersionNo": "5",
        "CreatedAt": "2019-06-10T02:33:16.674Z",
        "ModifiedAt": "2019-06-10T02:33:16.674Z",
        "DownloadSignedUrl": "http://function-apiserver-test.oss-cn-shanghai.aliyuncs.com/fc-source/fun-xxxxx-v1.tgz?OSSAccessKeyId=LTAIKCq5xHz1DkK6&Expires=1559805752&Signature=BXyrc9Nrsvw7j53HxtkLoGkDhDI%3D"
    }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/MPServerless)查看更多错误码。

访问[错误中心](https://error-center.alibabacloud.com/status/product/MPServerless)查看更多错误码。

