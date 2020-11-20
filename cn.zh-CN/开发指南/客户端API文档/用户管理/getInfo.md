# getInfo

获取用户信息。

## 方法定义

该方法的定义如下：

```
mpserverless.user.getInfo(options: object): Promise<Result>
```

## 请求参数

该方法接收以下请求参数。

|字段名|类型|必填|说明|
|---|--|--|--|
|options|Object|否|authProvider\{String\}指定客户端类型，取值： -   alipay\_openapi：支付宝（默认值）
-   wechat\_openapi：微信
-   dingtalk\_openapi：钉钉 |

## 返回参数

|字段名|类型|说明|
|---|--|--|
|success|Boolean|操作是否成功。|
|result|Object|用户信息： -   spaceId\{String\}：服务空间ID。
-   userId\{String\}：用户ID。
-   oAuthUserId\{String\}：三方授权用户标识。只有指定了authProvider时才会返回该参数。 |

## 示例

-   匿名授权方式获取用户信息。

    ```
    const res = await mpserverless.user.authorize({
      authType:'anonymous'
    });
    if (res.success) {
      console.log('授权成功');
    }
    mpserverless.user.getInfo().then(user => {
      this.setData(userInfo: user);
    }).catch(console.error);
    ```

-   非匿名授权方式获取用户信息。
    -   支付宝授权：

        ```
        const res = await mpserverless.user.authorize({
          authProvider: 'alipay_openapi'
        });
        if (res.success) {
          console.log('授权成功');
        }
        mpserverless.user.getInfo().then(user => {
          this.setData(userInfo: user);
        }).catch(console.error);
        ```

    -   微信授权：

        ```
        const res = await mpserverless.user.authorize({
          authProvider: 'wechat_openapi'
        });
        if (res.success) {
          console.log('授权成功');
        }
        mpserverless.user.getInfo().then(user => {
          this.setData(userInfo: user);
        }).catch(console.error);
        ```

    -   钉钉授权：

        ```
        const res = await mpserverless.user.authorize({
          authProvider: 'dingtalk_openapi'
        });
        if (res.success) {
          console.log('授权成功');
        }
        mpserverless.user.getInfo().then(user => {
          this.setData(userInfo: user);
        }).catch(console.error);
        ```


**说明：**

-   应用获取授权后方能获取用户信息，获取授权接口信息参见[authorize](/cn.zh-CN/开发指南/客户端API文档/用户管理/authorize.md)。
-   微信小程序中的授权和获取用户信息操作只能进行一次，建议开发者在app.js中授权并获取用户信息后，将用户信息保存到全局变量中，以便页面使用。

