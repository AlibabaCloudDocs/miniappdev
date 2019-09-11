# deleteFile {#concept_645208 .concept}

删除之前上传的文件。

## 方法定义 {#section_9ur_mbc_5xs .section}

该方法的定义如下：

``` {#codeblock_3x9_6ef_9rs}
mpserverless.file.deleteFile(url: string): Promise<Result>
```

## 请求参数 {#section_9dt_1s5_1az .section}

该方法接收 1 个参数，其定义如下：

|字段名|类型|必填|说明|
|---|--|--|--|
|url|String|是|线上完整路径|

## 示例 {#section_hze_d1s_fgv .section}

``` {#codeblock_s36_gy0_8pd}
mpserverless.file.deleteFile('https://resource.bspapp.com/xxx-xx/4b82ded0-0118-4de4-9f50-ab13110a1ffb.jpg').then(res => {
  console.log(res);
}).catch(err => {
  console.error(err);
});
```

