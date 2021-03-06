getInfo 
============================

获取用户信息。

方法定义 
-------------------------

    mpserverless.user.getInfo(options: object): Promise<Result>



请求参数 
-------------------------



|   字段名   |   类型   | 必填 |                                                                                                                        说明                                                                                                                        |
|---------|--------|----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| options | Object | 否  | `authProvider{String}`指定客户端类型，取值： * alipay_openapi：支付宝（默认值）   * wechat_openapi：微信   * dingtalk_openapi：钉钉    |



返回参数 
-------------------------



|   字段名   |   类型    |                                                                                                                   说明                                                                                                                    |
|---------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| success | Boolean | 操作是否成功。                                                                                                                                                                                                                                 |
| result  | Object  | 用户信息： * `spaceId{String}`：服务空间ID。   * `userId{String}`：用户ID。   * `oAuthUserId{String}`：三方授权用户标识。    |



示例 
-----------------------

在调用 getInfo 接口之前，请先完成 SDK 的初始化。

    await mpserverless.init(); // 初始化
    
    const {result} = await mpserverless.user.getInfo();
    console.log(result) // { spaceId: xxx, userId: xxx, oAuthUserId: xxxx}


