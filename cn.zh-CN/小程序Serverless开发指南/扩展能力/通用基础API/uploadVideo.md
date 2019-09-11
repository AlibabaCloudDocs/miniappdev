# uploadVideo {#concept_2151445 .concept}

上传门店视频，目前仅支持mp4格式。

## 方法定义 {#section_8vf_jph_x46 .section}

该方法的定义如下：

``` {#codeblock_nbv_dzs_fr9}
uploadVideo(params: Media): Promise<FunctionResponse<MediaResponse | Response>>;
```

## 请求参数 {#section_veu_sds_eua .section}

该方法接收以下请求参数。

|字段名|类型|必填|说明|
|---|--|--|--|
|fileName|string|是|视频名，例如：video.mp4|
|filePath|string|是|视频路径，例如：\>https://video.com/video.mp4|

## 返回参数 {#section_4vh_hyr_1fu .section}

 

|字段名|类型|是否必有|说明|
|---|--|----|--|
|fileId|string|是|文件的ID。|
|fileUrl|string|是|文件上传生成的URL。|

## 示例 {#section_o9y_rdm_dqh .section}

``` {#codeblock_iau_mw4_rzc}
async uploadVideo() {
  try {
    const res = await cloud.base.uploadVideo({
      fileName: 'video.mp4',
      filePath: 'https://video.com/video.mp4'
    });
  } catch (e) {
    // 这里处理异常
  }
}
```

