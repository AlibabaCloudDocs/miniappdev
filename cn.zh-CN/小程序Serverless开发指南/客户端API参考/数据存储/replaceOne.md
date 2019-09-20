# replaceOne {#concept_645208 .concept}

查询并整体替换这条记录。

## 方法定义 {#section_9ur_mbc_5xs .section}

该方法的定义如下：

``` {#codeblock_3x9_6ef_9rs}
replaceOne(doc: object, filter: object, options?: object): Promise<MongoResult>
```

## 请求参数 {#section_9dt_1s5_1az .section}

该方法接收 4 个参数，其定义如下：

|字段名|类型|必填|说明|
|---|--|--|--|
|filter|Object|是|数据库操作时的过滤条件。|
|doc|Object|是|替换的目标文档。|
|options|Object|否|控制项。|
|options.upsert|Boolean|否|如果匹配不到，是否插入。默认值：false。|

## 示例 {#section_hze_d1s_fgv .section}

``` {#codeblock_s36_gy0_8pd}
mpserverless.db.collection('users')
.replaceOne({
    name: 'tom'
    age: 18
},{
    name: 'jerry'
})
.then(res => {})
.catch(console.error);
```

