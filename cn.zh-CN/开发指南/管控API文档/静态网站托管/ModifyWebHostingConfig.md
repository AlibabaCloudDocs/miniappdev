# ModifyWebHostingConfig

调用ModifyWebHostingConfig更新静态网站配置。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=ModifyWebHostingConfig&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyWebHostingConfig|系统规定参数。取值：ModifyWebHostingConfig。 |
|IndexPath|String|是|index.html|首页路径。 |
|SpaceId|String|是|0e16bb12-14af-4635-b24c-5ac1a9a\*\*\*\*\*|服务空间ID。 |
|ErrorPath|String|否|error.html|404错误路径。 |
|AllowedIps|String|否|42.120.72.0/24|静态网站托管测试域名允许访问IP的白名单，不在白名单中的访问可能会被限制，仅支持配置ipv4，可以配置ip或者ip网段，掩码位数取值范围24-31，最多可同时配置三个，多个之间用逗号隔开。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Data|Boolean|true|操作执行结果。

 -   true：成功。
-   false：失败。 |
|RequestId|String|074C8CF9-E7F8-436D-A546-4E5876D0F800|唯一请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyWebHostingConfig
&SpaceId=0e16bb12-14af-4635-b24c-5ac1a9a*****
&IndexPath=index.html
&ErrorPath=error.html
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ModifyWebHostingConfigResponse>
      <RequestId>CEF9831B-A6D2-4485-9CAD-1B8FBC8BC6F7</RequestId>
      <HttpStatusCode>200</HttpStatusCode>
      <Data>true</Data>
      <Code>success</Code>
      <Success>true</Success>
</ModifyWebHostingConfigResponse>
```

`JSON`格式

```
{
    "RequestId": "CEF9831B-A6D2-4485-9CAD-1B8FBC8BC6F7",
    "HttpStatusCode": 200,
    "Data": true,
    "Code": "success",
    "Success": true
}
```

