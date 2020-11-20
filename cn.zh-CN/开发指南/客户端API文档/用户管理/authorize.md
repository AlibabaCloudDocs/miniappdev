# authorize

获取用户授权。

## 方法定义

该方法的定义如下：

```
authorize(options: AuthorizeOptions): Promise<{success: boolean;}>
```

## 请求参数

|字段名|类型|必填|说明|
|---|--|--|--|
|options|Object|否|-   authProvider\{String\} ：客户端类型。取值：
    -   alipay\_openapi（默认值）
    -   wechat\_openapi
-   authType\{String\}：授权方式。取值：
    -   空字符串（默认值）。
    -   anonymous：匿名方式 |

**说明：**

-   如果同时指定了authProvider和authType，authType配置优先。
-   如果将authType设置为anonymous，则不需要设置authProvider。
-   如果没有设置authType，则必须设置authProvider。

## 返回参数

|字段名|类型|说明|
|---|--|--|
|success|Boolean|操作是否成功。|

## 示例

-   非匿名授权：

    ```
    const res = await mpserverless.user.authorize({
      authProvider: 'alipay_openapi'
    });
    if (res.success) {
      console.log('授权成功');
    }
    ```

-   匿名授权：

    ```
    const res = await mpserverless.user.authorize({
      authType:'anonymous'
    });
    if (res.success) {
      console.log('授权成功');
    }
    ```

    **说明：** 匿名授权获取的用户身份是一个临时身份，每次匿名授权得到的用户标识是随机不固定的，若需要获取固定用户标识，则需要通过三方授权获取。


