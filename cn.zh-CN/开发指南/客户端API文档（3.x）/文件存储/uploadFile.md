uploadFile 
===============================

上传文件。

方法定义 
-------------------------

    mpserverless.file.uploadFile(options: object): Promise<Result>



请求参数 
-------------------------



|-------------------|--------|----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 字段名               | 类型     | 必填 | 说明                                                                                                                                                                                                                                                                                              |
| options.filePath  | String | 是  | 本地文件路径，通常可以从图片文件描述中获取文件路径。可上传文件大小限制在 100 MB 以内。                                                                                                                                                                                                                                                 |
| options.fileSize  | Number | 否  | 上传的文件大小。                                                                                                                                                                                                                                                                                        |
| options.extension | String | 否  | 上传的文件的扩展名。目前支持上传以下格式的文件： * .jpg   * .jpeg   * .png   * .gif   * .image                    |
| options.env       | String | 否  | 文件的获取方式。 唯一可选值 public： 可公开访问的文件。                                                                                                                                                                                                                                                |
| options.timeout   | Number | 否  | 超时时间，以毫秒为单位。默认值：60000。                                                                                                                                                                                                                                                                          |
| options.headers   | Object | 否  | 文件响应头键值对，可定义如下内容： * cacheControl： 缓存策略。   * contentDisposition： 文件形式。   * contentEncoding： 文件内容编码。   * expires： 缓存有效时长。    |
| options.meta      | Object | 否  | 自定义文件响应头键值对。例如，自定义 userId: halo 获得响应头 x-meta-user-id: halo 。                                                                                                                                                                                                                                    |



返回参数 
-------------------------



|   字段名    |   类型   |       说明        |
|----------|--------|-----------------|
| filePath | String | 本地文件路径。         |
| fileUrl  | String | 上传文件后获得的文件链接地址。 |



示例 
-----------------------

* 支付宝小程序上传文件示例。

      my.chooseImage({
        chooseImage: 1,
        success: res => {
          const path = res.apFilePaths[0];
          const options = {
            filePath: path,
          };
      
          mpserverless.file.uploadFile(options)
          .then(res => { // do somthing  })
          .catch(err => { // deal error  });
        },
      });

  

* 微信小程序上传文件示例。

      wx.chooseImage({
        count: 1,
        sizeType: ['original', 'compressed'],
        sourceType: ['album', 'camera'],
        success: res => {
          const path = res.tempFilePaths[0];
          const options = {
            filePath: path,
          };
      
          mpserverless.file.uploadFile(options)
          .then(res => { // do somthing  })
          .catch(err => { // deal error  });
        },
      });

  

* 钉钉小程序上传文件示例。

      dd.chooseImage({
        chooseImage: 1,
        success: res => {
          const path = res.apFilePaths[0];
          const options = {
            filePath: path,
          };
      
          mpserverless.file.uploadFile(options)
          .then(res => { // do somthing  })
          .catch(err => { // deal error  });
        },
      });

  



