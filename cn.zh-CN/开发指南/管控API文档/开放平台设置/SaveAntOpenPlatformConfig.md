# SaveAntOpenPlatformConfig

调用SaveAntOpenPlatformConfig保存支付宝开放平台配置。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=MPServerless&api=SaveAntOpenPlatformConfig&type=RPC&version=2019-06-15)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveAntOpenPlatformConfig|系统规定参数。取值：SaveAntOpenPlatformConfig。 |
|AppId|String|是|201909116717\*\*\*\*|小程序ID。 |
|PrivateKey|String|是|MIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSk|私钥。 |
|SignMode|String|是|CERT|加签方式，可选值如下：

 -   PUBLIC\_KEY：公钥。
-   CERT：公钥证书。 |
|SpaceId|String|是|0e16bb12-14af-\*\*\*\*-b24c-5ac1a9a7bb9f|服务空间ID。 |
|PublicKey|String|否|MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCA|公钥。 |
|AppCert|String|否|-----BEGIN CERTIFICATE----- MIIEwTCCA6mgAwIBAgIQICAJGbUNoqdPr25qpPU7+ -----END CERTIFICATE-----|应用公钥证书。 |
|PublicCert|String|否|-----BEGIN CERTIFICATE----- MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQ -----END CERTIFICATE-----|支付宝公钥证书。 |
|RootCert|String|否|-----BEGIN CERTIFICATE----- MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQ -----END CERTIFICATE-----|支付宝根证书。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|2540E86F-2CD4-44AC-A7AB-59CAF40C225D|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=SaveAntOpenPlatformConfig
&SpaceId=0e16bb12-14af-****-b24c-5ac1a9a7bb9f
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>2540E86F-2CD4-44AC-A7AB-59CAF40C225D</RequestId>
```

`JSON` 格式

```
{
    "RequestId": "2540E86F-2CD4-44AC-A7AB-59CAF40C225D"
}
```

