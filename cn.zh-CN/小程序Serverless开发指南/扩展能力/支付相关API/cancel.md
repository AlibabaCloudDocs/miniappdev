# cancel {#concept_2151212 .concept}

取消交易单，取消后该笔交易会进行回滚。

## 方法定义 {#section_lzm_5hm_hiq .section}

该方法的定义如下：

``` {#codeblock_u8o_ykz_h2t}
cancel(params: CancelRequest): Promise<FunctionResponse<CancelResponse>>
```

## 请求参数 {#section_9ed_b8a_lkc .section}

|字段名|类型|必填|说明|
|---|--|--|--|
|outTradeNo|string|是|商家订单号，用于商家唯一确定一笔交易，如：`+new Date()`，64个字符以内，只能包含字母、数字、下划线。|

## 返回参数 {#section_dfi_uox_gkf .section}

|字段名|类型|说明|
|---|--|--|
|outTradeNo|string|商家订单号。|
|tradeNo|string|支付宝交易号。|
|retryFlag|string|是否需要重试。|
|action|string|本次取消触发的交易动作。 -   close：交易未支付，触发关闭交易动作，无退款。
-   refund：交易已支付，触发交易退款动作。
-   如果没有返回值，则未查询到交易，或接口调用失败。

 |

## 示例 {#section_1lz_1l0_y27 .section}

``` {#codeblock_1d5_y8z_wc8}
async cancel() {
  try {
    const res = await cloud.payment.cancel({
      outTradeNo: '', // 商家订单号
    });
  } catch (e) {
    // 进行错误处理
  }
}
```

