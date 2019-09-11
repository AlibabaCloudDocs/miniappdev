# queryFaceVerified {#concept_2151468 .concept}

小程序中进行人脸采集。

## 方法定义 {#section_gfb_s9x_vi0 .section}

该方法的定义如下：

``` {#codeblock_esd_1jh_m9t}
queryFaceVerified(params: QueryFaceVerifiedRequest): Promise<FunctionResponse<QueryFaceVerifiedResponse>>
```

## 请求参数 {#section_ee3_lth_3ga .section}

|字段名|类型|必填|说明|
|---|--|--|--|
|bizId|string|是|业务单据号，随机生成的一个唯一字符串，如：`+new Date()` 生成的字符串，可用于排查问题|
|zimId|string|是|刷脸认证标识，能通过 my.ap.faceVerify JSAPI 进行获取|
|externParam|object|否|扩展参数|

## 返回参数 {#section_21x_l3v_78f .section}

|字段名|类型|说明|
|---|--|--|
|externInfo|string|扩展结果|

## 示例 {#section_h4a_pp9_91i .section}

``` {#codeblock_310_7m3_q7f}
queryFaceVerified() {
  const bizId = +new Date();
  my.ap.faceVerify({
    bizId,
    bizType: '1',
    success: async faceRes => {
      const { zimId } = faceRes;
      try {
        const res = await cloud.mini.queryFaceVerified({
          bizId,
          zimId,
          externParam: {} // 扩展参数，选填
        });  
        // 进行业务处理
      } catch (e) {
        // 进行异常处理
      }
    }
  });
}
```

