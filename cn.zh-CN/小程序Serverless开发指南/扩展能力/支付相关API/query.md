# query {#concept_2151201 .concept}

查询交易信息。

## 方法定义 {#section_yy8_mks_3qf .section}

该方法的定义如下：

``` {#codeblock_n72_zch_r0g}
query(params: QueryRequest): Promise<FunctionResponse<QueryResponse>>
```

## 请求参数 {#section_el6_9o1_ooa .section}

|字段名|类型|必填|说明|
|---|--|--|--|
|outTradeNo|string|是|商家订单号，用于商家唯一确定一笔交易，如：`+new Date()`，64个字符以内，只能包含字母、数字、下划线。|

## 返回参数 {#section_ysf_lt7_p8m .section}

可参考SDK中类型定义文件dist/esm/model/OpenApiModel.d.ts。

## 示例 {#section_x11_dae_72l .section}

``` {#codeblock_l97_23t_gjj}
async query() {
  try {
    const res = await cloud.payment.query({
      outTradeNo: '', // 商家订单号
    });
  } catch (e) {
    // 进行错误处理
  }
}
```

