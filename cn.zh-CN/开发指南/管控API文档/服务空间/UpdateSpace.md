# UpdateSpace

调用UpdateSpace接口来更新服务空间。

您可以更新服务空间的描述信息，您还可以更新服务空间的服务状态。当服务状态设置为PAUSED（服务暂停）时，服务面（包含小程序端访问服务空间和静态网站托管服务）不再提供服务，管控面（使用OpenAPI或者控制台）提供正常服务。

**说明：** 更新服务空间状态成功到状态完全生效有一定的延迟，最高不超过10分钟。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=UpdateSpace&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|UpdateSpace|系统规定参数。取值：UpdateSpace。 |
|SpaceId|String|是|826061c4-5095-4550-8b74-3bcd9af\*\*\*\*\*|服务空间ID。 |
|Desc|String|否|我的第一个服务空间。|服务空间描述信息。 |
|Status|String|否|IN\_SERVICE|服务状态，可选值为：

 -   IN\_SERVICE：服务中。
-   PAUSED：服务暂停。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|EA770971-A4A0-4555-9E00-C94A2194E150|唯一请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=UpdateSpace
&SpaceId=826061c4-5095-4550-8b74-3bcd9af*****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<UpdateSpaceResponse>
        <RequestId>9D653EC3-8F53-4307-9B1C-52F5922384A6</RequestId>
</UpdateSpaceResponse>
```

`JSON` 格式

```
{
    "RequestId": "C293BB03-B6AD-46C2-80D1-19C8FB573916"
}
```

