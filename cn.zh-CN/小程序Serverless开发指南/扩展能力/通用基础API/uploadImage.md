# uploadImage {#concept_2151427 .concept}

上传门店图片。

## 方法定义 {#section_vgu_sgv_32y .section}

该方法的定义如下：

``` {#codeblock_eza_zf0_jui}
uploadImage(params: Media): Promise<FunctionResponse<MediaResponse | Response>>;
```

## 请求参数 {#section_rqj_oew_fle .section}

该方法接收以下请求参数。

|字段名|类型|必填|说明|
|---|--|--|--|
|fileName|string|是|图片名，例如：image.jpg|
|filePath|string|是|图片路径，例如：https://image.com/image.jpg|
|fileType|string|否|图片类型，推荐使用默认值 jpg，目前支持：jpg、jpeg、png、gif|

## 返回参数 {#section_noq_uly_3o2 .section}

|字段名|类型|是否必有|说明|
|---|--|----|--|
|fileId|string|是|文件的ID。|
|fileUrl|string|是|文件上传生成的URL。|

## 示例 {#section_b2a_v87_sic .section}

``` {#codeblock_bvp_fxn_061}
async uploadImage() {
  try {
    const res = await cloud.base.uploadImage({
      fileName: 'test.jpg',
      filePath: 'https://image.com/test.jpg'
    });
  } catch (e) {
    // 这里处理异常
  }
}
```

