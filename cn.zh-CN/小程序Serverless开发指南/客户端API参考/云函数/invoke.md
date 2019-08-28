# invoke {#concept_645208 .concept}

调用云服务。

## 方法定义 {#section_9ur_mbc_5xs .section}

该方法的定义如下：

``` {#codeblock_3x9_6ef_9rs}
mpserverless.function.invoke(functionName: string, options?: object): Promise<Result>
```

## 返回参数 {#section_hze_d1s_fgv .section}

|字段名|类型|说明|
|---|--|--|
|success|Boolean|执行状态。|
|requestId|String|请求ID。|
|result|Any|接口返回内容，由开发者代码和请求参数 header 的 content-type 决定，默认 content-type 为 application/json。|

## 示例 {#section_bi5_kb6_iwb .section}

``` {#codeblock_shh_qv2_pqj}
mpserverless.function.invoke('dataAnalytics', {
    range: 30,
}).then((res) => {
  console.log(res);
}).catch(console.error);
```

