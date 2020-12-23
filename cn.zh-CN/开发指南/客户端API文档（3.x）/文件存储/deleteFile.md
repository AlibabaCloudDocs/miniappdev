deleteFile 
===============================

删除已上传的文件。

方法定义 
-------------------------

    mpserverless.file.deleteFile(url: string): Promise<Result>



请求参数 
-------------------------



| 字段名 |   类型   | 必填 |    说明    |
|-----|--------|----|----------|
| url | String | 是  | 文件存储完整路径 |



返回参数 
-------------------------



|   字段名   |   类型    |  说明   |
|---------|---------|-------|
| success | Boolean | 执行状态。 |
| result  | any     |       |



示例 
-----------------------

假设已知一个上传文件后获得的文件链接地址 `fileURL` ，根据文件地址从服务空间中删除该文件。

    const fileURL = 'https://resource.bspapp.com/xxx-xx/4b82ded0-0118-4de4-9f50-ab13110a1ffb.jpg';
    
    mpserverless.file.deleteFile(fileURL).then(res => {
      console.log(res);
    }).catch(err => {
      console.error(err);
    });


