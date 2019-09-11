# findOneAndDelete {#concept_645208 .concept}

查询并删除一条记录。

## 方法定义 {#section_9ur_mbc_5xs .section}

该方法的定义如下：

``` {#codeblock_3x9_6ef_9rs}
findOneAndDelete(query?: object, options?: object): Promise<MongoResult>
```

## 请求参数 {#section_9dt_1s5_1az .section}

该方法接收 8 个参数，其定义如下：

|字段名|类型|必填|说明|
|---|--|--|--|
|query|Object|否|数据库操作时的查询条件。|
|options|String|否|控制项。|
|options.limit|Number|否|查询的文档数量限制。|
|options.skip|Number|否|跳过的文档数量。|
|options.maxTimeMS|Number|否|超时时间。|
|options.sort|Object|否|排序规则。|
|options.projection|Object|否|查询后过滤的字段|
|options.hint|Object|否|指定查询时使用的索引|

## 示例 {#section_hze_d1s_fgv .section}

``` {#codeblock_s36_gy0_8pd}
mpserverless.db.collection('users')
.findOne({
    age: {$gt: 18}
}, {
    projection: {name: 1},
    limit: 10,
    skip: 10,
})
.then(res => {})
.error(console.error)
```

