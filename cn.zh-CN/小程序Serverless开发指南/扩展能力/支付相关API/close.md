# close {#concept_2151211 .concept}

关闭交易单，修改交易的状态，不做交易回滚。

## 方法定义 {#section_po6_zxr_p87 .section}

该方法的定义如下：

``` {#codeblock_wou_6m1_r3c}
close(params: CloseRequest): Promise<FunctionResponse<CloseResponse>>
```

## 请求参数 {#section_pcf_rm0_jdo .section}

|字段名|类型|必填|说明|
|---|--|--|--|
|outTradeNo|string|是|商家订单号，用于商家唯一确定一笔交易，如：`+new Date()`，64个字符以内，只能包含字母、数字、下划线。|

## 返回参数 {#section_8vn_8gv_83s .section}

|字段名|类型|说明|
|---|--|--|
|outTradeNo|string|商家订单号。|
|tradeNo|string|支付宝交易号。|

## 示例 {#section_zva_73x_xa6 .section}

``` {#codeblock_uxm_9tz_6xb}
async close() {
  try {
    const res = await cloud.payment.close({
      outTradeNo: '', // 商家订单号
    });
  } catch (e) {
    // 进行错误处理
  }
}
```

