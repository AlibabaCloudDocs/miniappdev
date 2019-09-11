# queryFaceCertifyId {#concept_2151441 .concept}

小程序中的人脸认证功能。

## 方法定义 {#section_g0k_dq8_hsw .section}

该方法的定义如下：

``` {#codeblock_xq9_h1e_eoi}
queryFaceCertifyId(params: QueryFaceCertifyIdRequest): Promise<FunctionResponse<QueryFaceCertifyIdResponse>>
```

## 请求参数 {#section_7pz_vzg_a7u .section}

|字段名|类型|必填|说明|
|---|--|--|--|
|bizId|string|是|业务单据号，随机生成的一个唯一字符串，例如：`+new Date()` 生成的字符串，可用于排查问题。|
|zimId|string|是|刷脸认证标识，能通过 my.ap.faceVerifyAPI 进行获取。|
|faceType|string|是|人脸认证的类型，取值： -   0：匿名注册
-   1：匿名认证
-   2：实名认证

 |
|needImg|boolean|是|是否需要返回人脸图片。|

## 返回参数 {#section_vsn_7lk_xu1 .section}

|字段名|类型|说明|
|---|--|--|
|bizId|string|请求的bizID。|
|zimCode|string|人脸服务端返回码。|
|zimMsg|string|人脸服务端返回信息。|
|imgSrc|string|Base64的人脸图片。|
|faceAttrInfo|`Object, { rect: string`\}|人脸属性信息，目前只返回矩阵信息，例如 `0.0.0.0`。|

## 示例 {#section_gbq_hco_o5x .section}

``` {#codeblock_sej_y1n_mze}
queryFaceCertifyId() {
  const bizId = +new Date();
  my.ap.faceVerify({
    bizId,
    bizType: '2', // 人脸认证传入 2，参见 JSAPI 文档
    success: async faceRes => {
      const { zimId } = faceRes;
      try {
        const res = await cloud.mini.queryFaceCertifyId({
          bizId,
          zimId,
          faceType: 3,
          needImg: true
        });
        // 进行业务处理
      } catch (e) {
        // 进行异常处理
      }
    },
  });
}
```

