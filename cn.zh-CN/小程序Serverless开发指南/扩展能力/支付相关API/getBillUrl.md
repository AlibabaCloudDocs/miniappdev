# getBillUrl {#concept_2151215 .concept}

查询对账单地址。

## 方法定义 {#section_kxj_zdj_15i .section}

该方法的定义如下：

``` {#codeblock_mqi_mfi_uy7}
getBillUrl(params: GetBillUrlRequest): Promise<FunctionResponse<GetBillUrlResponse>>
```

## 请求参数 {#section_5mg_h0z_n1h .section}

|字段名|类型|必填|说明|
|---|--|--|--|
|billType|string|是|账单类型： -   trade：指商户基于支付宝交易收单的业务账单。
-   signcustomer：指基于商户支付宝余额收入及支出等资金变动的帐务账单。

 |
|billDate|string|是|账单时间：日账单格式为yyyy-MM-dd，月账单格式为yyyy-MM。例如：2019-11-11|

## 返回参数 {#section_dc9_kl8_2ku .section}

|字段名|类型|说明|
|---|--|--|
|billDownloadUrl|string|账单下载地址链接，获取连接后30秒后未下载，链接地址失效。|

## 示例 {#section_90v_x5c_j2x .section}

``` {#codeblock_vu1_fj9_22t}
async getBillUrl() {
  try {
    const params = {
      billType: 'trade',
      billDate: '2019-11-11',
    };
    const res = await cloud.payment.getBillUrl(params);
    // 进行业务处理
  } catch (e) {
    // 进行错误处理
  }
}
```

