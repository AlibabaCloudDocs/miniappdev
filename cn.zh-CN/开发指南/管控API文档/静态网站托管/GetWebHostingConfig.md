# GetWebHostingConfig

调用GetWebHostingConfig查询静态网站配置。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=GetWebHostingConfig&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetWebHostingConfig|系统规定参数。取值：GetWebHostingConfig。 |
|SpaceId|String|是|0e16bb12-14af-4635-b24c-5ac1a9a\*\*\*\*\*|服务空间ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Data|Struct| |返回数据。 |
|AllowedIps|String|42.120.72.0/24|静态网站托管测试域名允许访问IP的白名单，不在白名单中的访问可能会被限制。 |
|DefaultDomain|String|static-0e16bb12-14af-4635-b24c-5ac1a9a\*\*\*\*\*.bspapp.com|默认域名，仅供测试使用，请求速度会收到限制。如果您需要对外正式提供网站服务，请绑定您已备案的自定义域名。 |
|ErrorPath|String|error.html|404错误路径 |
|IndexPath|String|index.html|首页路径。 |
|SpaceId|String|0e16bb12-14af-4635-b24c-5ac1a9a\*\*\*\*\*|服务空间ID。 |
|RequestId|String|828A8808-3FC9-418C-893A-5A708CFABB8E|唯一请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=GetWebHostingConfig
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<RequestId>828A8808-3FC9-418C-893A-5A708CFABB8E</RequestId>
<HttpStatusCode>200</HttpStatusCode>
<Data>
    <SpaceId>0e16bb12-14af-4635-b24c-5ac1a9a*****</SpaceId>
    <IndexPath>index.html</IndexPath>
    <ErrorPath>error.html</ErrorPath>
    <AllowedIps>42.120.72.0/24</AllowedIps>
    <DefaultDomain>static-0e16bb12-14af-4635-b24c-5ac1a9a*****.bspapp.com</DefaultDomain>
</Data>
<Code>success</Code>
<Success>true</Success>
```

`JSON`格式

```
{
    "RequestId": "828A8808-3FC9-418C-893A-5A708CFABB8E",
    "HttpStatusCode": 200,
    "Data": {
        "SpaceId": "0e16bb12-14af-4635-b24c-5ac1a9a*****",
        "IndexPath": "index.html",
        "ErrorPath": "error.html",
        "AllowedIps": "42.120.72.0/24",
        "DefaultDomain": "static-0e16bb12-14af-4635-b24c-5ac1a9a*****.bspapp.com"
    },
    "Code": "success",
    "Success": true
}
```

