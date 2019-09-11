# refund {#concept_2151203 .concept}

支付退款。

## 方法定义 {#section_sfs_9ln_tdr .section}

该方法的定义如下：

``` {#codeblock_kza_3h2_vd2}
refund(params: RefundRequest): Promise<FunctionResponse<RefundResponse>>
```

## 请求参数 {#section_0qb_o7v_xgb .section}

|字段名|类型|必填|描述|
|---|--|--|--|
|outTradeNo|string|是|商家订单号，用于商家唯一确定一笔交易，如：`+new Date()`，64个字符以内，只能包含字母、数字、下划线。|
|refundAmount|string|是|退款金额。|

## 返回参数 {#section_ux3_a81_zvn .section}

可参考SDK中类型定义文件dist/esm/model/OpenApiModel.d.ts。

## 示例 {#section_z1x_yie_3zp .section}

``` {#codeblock_005_6j6_4nl}
async refund() {
  try {
    const res = await cloud.payment.refund({
      outTradeNo: '', // .pay 接口支付的商家订单号
      refundAmount: '0.1' // 推荐金额
    });
    // 进行业务处理
  } catch (e) {
    // 进行错误处理
  }
}
```

