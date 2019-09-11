# detectRiskContent {#concept_2151479 .concept}

小程序内容风险检测服务。

## 方法定义 {#section_bj3_a12_41c .section}

该方法的定义如下：

``` {#codeblock_cgy_0eu_o3s}
detectRiskContent(params: DetectContentRequest): Promise<FunctionResponse<DetectContentResponse>>;
```

## 请求参数 {#section_0dt_uj1_hcm .section}

该方法接收以下请求参数。

|字段名|类型|必填|说明|
|---|--|--|--|
|content|string|是|需要识别的文本内容。|

## 返回参数 {#section_cci_cqe_d6j .section}

|字段名|类型|说明|
|---|--|--|
|action|string|处理结果： -   PASSED：通过
-   REJECT：拦截

 |
|keywords|string\[\]|命中的关键词列表。|
|uniqueId|string|业务唯一的ID。|

## 示例 {#section_hwo_b9c_mrd .section}

``` {#codeblock_798_wy9_9gg}
async detectRiskContent() {
  try {
    const res = await cloud.mini.detectRiskContent({
      content: '文本'
    });
    // 进行业务处理
  } catch (e) {
    // 进行异常处理
  }
}
```

