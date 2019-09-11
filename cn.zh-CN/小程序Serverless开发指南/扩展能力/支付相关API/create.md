# create {#concept_2151197 .concept}

创建支付交易，能配合小程序收银台使用。

## 方法定义 {#section_xdl_2xs_mpp .section}

该方法的定义如下：

``` {#codeblock_sm7_e5m_9ek}
create(params: CreateRequest): Promise<FunctionResponse<CreateResponse>>
```

## 请求参数 {#section_wy1_i3x_7f9 .section}

该方法接收以下请求参数。

|字段名|类型|必填|说明|
|---|--|--|--|
|outTradeNo|string|是|商家订单号，用于商家唯一确定一笔交易，如：`+new Date()`，64个字符以内，只能包含字母、数字、下划线。|
|subject|string|是|购买的商品名。|
|totalAmount|string|是|支付金额。|
|buyerId|string|是|买家的user ID。|

## 返回参数 {#section_ycv_5v0_aiu .section}

|字段名|类型|说明|
|---|--|--|
|outTradeNo|string|商家订单号。|
|tradeNo|string|支付宝交易号。|

## 示例 {#section_izp_8k1_iac .section}

``` {#codeblock_ady_3j2_r10}
create() {
  const outTradeNo = +new Date();
  my.getAuthCode({
    scopes: 'auth_user',
    success: async authRes => {
      const { authCode } = authRes;
      const tokenRes = await cloud.base.oauth.getToken({
        grantType: 'authorization_code',
        code: authCode,
      });
      const res = await cloud.payment.create({
        outTradeNo,
        subject: '商品名',
        totalAmount: '0.1',
        buyerId: tokenRes.result.userId
      });

      // 唤起小程序收银台进行用户支付
      my.tradePay({
        tradeNO: res.result.tradeNo,
        success: res => {
          // 进行业务操作
        },
        fail: res => {
          // 进行业务操作
        }
      });
    }
  });
}
```

