# ListFunctionDeployment

调用ListFunctionDeployment查询云函数部署单列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=ListFunctionDeployment&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListFunctionDeployment|系统规定参数。取值：ListFunctionDeployment。 |
|Name|String|是|demoFunction|部署单名称。 |
|SpaceId|String|是|dece4ea0-d432-4cfa-\*\*\*\*-8a88d205e2b8|服务空间ID。 |
|PageNum|Integer|否|1|列表的页码。起始值：1 默认值：1。 |
|PageSize|Integer|否|10|每页行数。最大值：100 默认值：10。 |
|Status|String|否|DEPLOY\_SUCCESS|部署单元状态，取值：

 -   DEPLOY\_SUCCESS：查询部署成功的部署单。
-   DEPLOY\_FAILED：查询部署失败的部署单。

 **说明：** 如果不指定状态，则查询全部部署单。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|DataList|Array of DataList| |函数数据列表。 |
|CreatedAt|String|2019-06-21T02:22:53.309Z|创建时间。 |
|DeploymentId|String|dep-5e49fd471c9d4451c33bdd06|部署ID。 |
|DownloadSignedUrl|String|http://function-apiserver-test.oss-cn-shanghai.aliyuncs.com/5d0afc0e1c9d44\*\*\*\*\*32c30a-v5.zip?OSSAccessKeyId=LTA\*\*\*\*\*\*\*\*\*\*\*\*&Expires=1561425220&Signature=SAgUkZFK54eAbU6TLT9zMZ7S8eg%3D|下载地址。 |
|ModifiedAt|String|2019-06-21T02:22:55.996Z|修改时间。 |
|Status|Struct| |状态。 |
|Label|String|部署成功|状态描述。 |
|Status|String|DEPLOY\_SUCCESS|状态。 |
|VersionNo|String|2019061110511930090|版本号。 |
|Paginator|Struct| |分页信息。 |
|PageCount|Integer|1|当前页面总数。 |
|PageNum|Integer|1|页码。 |
|PageSize|Integer|10|每页行数。 |
|Total|Integer|1|总数。 |
|RequestId|String|C293BB03-B6AD-46C2-80D1-19C8FB573916|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ListFunctionDeployment
&Name=demoFunction
&PageNum=1
&SpaceId=dece4ea0-d432-4cfa-8514-8a88d205e2b8
&Status=DEPLOY_SUCCESS
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<HttpStatusCode>200</HttpStatusCode>
<RequestId>71F897B5-7078-487E-8029-EE2FD071D203</RequestId>
<Paginator>
    <PageCount>1</PageCount>
    <PageSize>10</PageSize>
    <PageNum>1</PageNum>
    <Total>2</Total>
</Paginator>
<DataList>
    <Status>
        <Status>DEPLOY_SUCCESS</Status>
        <Label>部署成功</Label>
    </Status>
    <DeploymentId>dep-5e0ab12b1c9d44709fa2c***</DeploymentId>
    <DownloadSignedUrl>http://mps-zjk-faas-prod.oss-cn-zhangjiakou.aliyuncs.com/upload/xxxx</DownloadSignedUrl>
    <ModifiedAt>2019-12-31T02:23:41.799Z</ModifiedAt>
    <VersionNo>2019123110233936929</VersionNo>
    <CreatedAt>2019-12-31T02:23:39.371Z</CreatedAt>
</DataList>
<DataList>
    <Status>
        <Status>DEPLOY_SUCCESS</Status>
        <Label>部署成功</Label>
    </Status>
    <DeploymentId>dep-5e0aa9d21c9d446d94af0***</DeploymentId>
    <DownloadSignedUrl>http://mps-zjk-faas-prod.oss-cn-zhangjiakou.aliyuncs.com/upload/xxxx</DownloadSignedUrl>
    <ModifiedAt>2019-12-31T01:52:20.966Z</ModifiedAt>
    <VersionNo>2019123109521824866</VersionNo>
    <CreatedAt>2019-12-31T01:52:18.251Z</CreatedAt>
</DataList>
<Success>true</Success>
<Code>OK</Code>
```

`JSON`格式

```
{
    "HttpStatusCode": "200",
    "RequestId": "71F897B5-7078-487E-8029-EE2FD071D203",
    "Paginator": {
        "PageCount": 1,
        "PageSize": 10,
        "PageNum": 1,
        "Total": 2
    },
    "DataList": [
        {
            "Status": {
                "Status": "DEPLOY_SUCCESS",
                "Label": "部署成功"
            },
            "DeploymentId": "dep-5e0ab12b1c9d44709fa2c***",
            "DownloadSignedUrl": "http://mps-zjk-faas-prod.oss-cn-zhangjiakou.aliyuncs.com/upload/xxxx",
            "ModifiedAt": "2019-12-31T02:23:41.799Z",
            "VersionNo": "2019123110233936929",
            "CreatedAt": "2019-12-31T02:23:39.371Z"
        },
        {
            "Status": {
                "Status": "DEPLOY_SUCCESS",
                "Label": "部署成功"
            },
            "DeploymentId": "dep-5e0aa9d21c9d446d94af0***",
            "DownloadSignedUrl": "http://mps-zjk-faas-prod.oss-cn-zhangjiakou.aliyuncs.com/upload/xxxx",
            "ModifiedAt": "2019-12-31T01:52:20.966Z",
            "VersionNo": "2019123109521824866",
            "CreatedAt": "2019-12-31T01:52:18.251Z"
        }

    ],
    "Success": true,
    "Code": "OK"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/MPServerless)查看更多错误码。

访问[错误中心](https://error-center.alibabacloud.com/status/product/MPServerless)查看更多错误码。

