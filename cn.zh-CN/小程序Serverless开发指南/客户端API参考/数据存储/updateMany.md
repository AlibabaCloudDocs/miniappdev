# updateMany {#concept_645208 .concept}

更新集合中的一批记录。

## 方法定义 {#section_9ur_mbc_5xs .section}

该方法的定义如下：

``` {#codeblock_3x9_6ef_9rs}
updateMany(filter: object, update: object, options?: object): Promise<MongoResult>
```

## 请求参数 {#section_9dt_1s5_1az .section}

该方法接收 4 个参数，其定义如下：

|字段名|类型|必填|说明|
|---|--|--|--|
|filter|Object|是|过滤条件。|
|update|Object|是|更新的文档|
|options|Object|否|控制项|
|options.upsert|Boolean|否|不匹配时是否直接插入文档。默认值：false。|

## 示例 {#section_hze_d1s_fgv .section}

``` {#codeblock_s36_gy0_8pd}
mpserverless.db.collection('users').updateMany({
    name: 'jerry'
}, {
    $set: {
        age: 10
    }
})
.then(res => {})
.catch(console.error)
```

