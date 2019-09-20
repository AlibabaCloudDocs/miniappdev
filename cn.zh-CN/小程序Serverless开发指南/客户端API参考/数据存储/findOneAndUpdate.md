# findOneAndUpdate {#concept_645208 .concept}

查询并更新记录。

## 方法定义 {#section_9ur_mbc_5xs .section}

该方法的定义如下：

``` {#codeblock_3x9_6ef_9rs}
findOneAndUpdate(filter: object, update: object, options?: object): Promise<MongoResult>
```

## 请求参数 {#section_9dt_1s5_1az .section}

该方法接收 7个参数，其定义如下：

|字段|类型|必填|说明|
|--|--|--|--|
|filter|Object|是|数据库操作时的过滤条件。|
|update|Object|是|数据库操作时的更新对象。|
|options|String|否|控制项。|
|options.maxTimeMS|Number|否|超时时间。|
|options.sort|Object|否|排序规则。|
|options.upsert|Boolean|否|如果查找不到对应文档，是否插入。默认值：false。|
|options.projection|Object|否|查询后过滤的字段。|

## 示例 {#section_hze_d1s_fgv .section}

``` {#codeblock_s36_gy0_8pd}
mpserverless.db.collection('users')
    .findOneAndUpdate({
        username: "zhangsan"
    },
    {
    $set: {
        age: 18
        }
    })
    .then(res => {})
    .catch(console.error)
```

