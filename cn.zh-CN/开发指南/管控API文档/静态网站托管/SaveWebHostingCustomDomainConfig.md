# SaveWebHostingCustomDomainConfig

调用SaveWebHostingCustomDomainConfig保存域名配置。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=SaveWebHostingCustomDomainConfig&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveWebHostingCustomDomainConfig|系统规定参数。取值：SaveWebHostingCustomDomainConfig。 |
|DomainName|String|是|www.example.com|域名。 |
|ForceRedirectType|String|是|HTTPS\_FORCE|强制跳转选项。

 -   HTTPS\_FORCE：强制跳转。
-   OFF：不跳转（默认）。 |
|SpaceId|String|是|0e16bb12-14af-4635-b24c-5ac1a9a\*\*\*\*\*|服务空间ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|828A8808-3FC9-418C-893A-5A708CFABB8E|唯一请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=SaveWebHostingCustomDomainConfig
&DomainName=www.example.com
&ForceRedirectType=HTTPS_FORCE
&SpaceId=0e16bb12-14af-4635-b24c-5ac1a9a*****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SaveWebHostingCustomDomainConfigResponse>
        <RequestId>0e16bb12-14af-4635-b24c-5ac1a9a*****</RequestId>
</SaveWebHostingCustomDomainConfigResponse>
```

`JSON` 格式

```
{
    "RequestId":"0e16bb12-14af-4635-b24c-5ac1a9a*****"
}
```

