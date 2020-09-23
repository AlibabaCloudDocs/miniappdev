# ListOpenPlatformConfig

调用ListOpenPlatformConfig查询支付宝、微信开放平台配置。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=ListOpenPlatformConfig&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListOpenPlatformConfig|系统规定参数。取值：ListOpenPlatformConfig。 |
|SpaceId|String|是|0e16bb12-14af-\*\*\*\*-b24c-5ac1a9a7bb9f|服务空间ID。 |
|Platform|String|否|Alipay|平台。可选值：

 -   Alipay
-   Wechat |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|2540E86F-2CD4-44AC-A7AB-59CAF40C225D|请求ID。 |
|SecretList|Array of Secret| |密钥列表。 |
|AppCert|String|-----BEGIN CERTIFICATE----- MIIEwTCCA6mgAwIBAgIQICAJGbUNoqdPr25qpPU7+ -----END CERTIFICATE-----|应用公钥证书。 |
|AppId|String|201909116717\*\*\*\*|小程序ID。 |
|AppSecret|String|1r0ElNPFqLI6qgY08\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*9TIK3RN\_5fk9SEMO|应用密钥。 |
|Platform|String|Alipay|平台。 |
|PrivateKey|String|MIIEvgIBADANBgkqhkiG9w0BAQEFAAS|私钥。 |
|PublicCert|String|-----BEGIN CERTIFICATE----- MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQ -----END CERTIFICATE-----|支付宝公钥证书。 |
|PublicKey|String|MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ|公钥。 |
|RootCert|String|-----BEGIN CERTIFICATE----- MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQ -----END CERTIFICATE-----|支付宝根证书。 |
|SignMode|String|CERT|加签方式，可选值如下：

 -   PUBLIC\_KEY：公钥。
-   CERT：公钥证书。 |
|SpaceId|String|0e16bb12-14af-\*\*\*\*-b24c-5ac1a9a7bb9f|服务空间ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ListOpenPlatformConfig
&SpaceId=0e16bb12-14af-****-b24c-5ac1a9a7bb9f
&Platform=Alipay
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<ListOpenPlatformConfigResponse>
      <HttpStatusCode>200</HttpStatusCode>
      <RequestId>2540E86F-2CD4-44AC-A7AB-59CAF40C225D</RequestId>
      <Success>true</Success>
      <SecretList>
            <SignMode>PUBLIC_KEY</SignMode>
            <PublicKey>MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ</PublicKey>
            <AppId>201909116717****</AppId>
            <PrivateKey>MIIEvgIBADANBgkqhkiG9w0BAQEFAAS</PrivateKey>
            <Platform>Alipay</Platform>
            <SpaceId>0e16bb12-14af-****-b24c-5ac1a9a7bb9f</SpaceId>
      </SecretList>
      <Code>OK</Code>
</ListOpenPlatformConfigResponse>
```

`JSON` 格式

```
{
    "HttpStatusCode": 200,
    "RequestId": "2540E86F-2CD4-44AC-A7AB-59CAF40C225D",
    "Success": true,
    "SecretList": {
		"SignMode": "PUBLIC_KEY",
        "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ",
        "AppId": "201909116717****",
        "PrivateKey": "MIIEvgIBADANBgkqhkiG9w0BAQEFAAS",
        "Platform": "Alipay",
        "SpaceId": "0e16bb12-14af-****-b24c-5ac1a9a7bb9f"
    },
    "Code": "OK"
}
```

