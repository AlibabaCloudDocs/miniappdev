# findOneAndReplace {#concept_645208 .concept}

查询并整体替换一条记录。

## 方法定义 {#section_9ur_mbc_5xs .section}

该方法的定义如下：

``` {#codeblock_3x9_6ef_9rs}
findOneAndReplace(query?: object, options?: object): Promise<MongoResult>
```

## 请求参数 {#section_9dt_1s5_1az .section}

该方法接收 6 个参数，其定义如下：

|字段|类型|必填|描述|
|--|--|--|--|
|query|Object|否|数据库操作时的查询条件。|
|options|String|否|控制项。|
|options.maxTimeMS|Number|否|超时时间。|
|options.sort|Object|否|排序规则|
|options.upsert|Boolean|否|如果查找不到对应文档，是否插入。默认值：false。|
|options.projection|Object|否|查询后过滤的字段。|

## 示例 {#section_hze_d1s_fgv .section}

``` {#codeblock_s36_gy0_8pd}
mpserverless.db.collection('users')
.findOneAndReplace({
    age: 18
})
.then(res => {})
.catch(console.error)
```

