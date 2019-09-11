# pay {#concept_2151200 .concept}

进行条形码支付，配合扫码枪可使用。

## 方法定义 {#section_0s2_uql_gnv .section}

该方法的定义如下：

``` {#codeblock_b7d_and_rzz}
pay(params: PayRequest): Promise<FunctionResponse<PayResponse>>
```

## 请求参数 {#section_bay_yzk_9rw .section}

|字段名|类型|必填|说明|
|---|--|--|--|
|outTradeNo|string|是|商家订单号，用于商家唯一确定一笔交易，如：`+new Date()`，64个字符以内，只能包含字母、数字、下划线。|
|authCode|string|是|条形码。。|
|subject|string|是|商品名称|
|totalAmount|string|是|商品价格。|

## 返回参数 {#section_a3p_7ng_ytw .section}

可参考SDK中类型定义文件dist/esm/model/OpenApiModel.d.ts。

## 示例 {#section_i37_hg8_jx7 .section}

``` {#codeblock_6k1_2xh_bex}
async pay() {
  try {
    const outTradeNo = +new Date();
    const subject = '商品名';
    const totalAmount = '0.1';

    const payRes = await cloud.payment.pay({
      outTradeNo,
      // 条码数目，有效期是1分钟
      authCode: '条形码', // 可通过扫码枪获取
      subject,
      totalAmount
    });
    // 进行业务处理
  } catch (e) {
    // 进行错误处理 
  }
}
```

