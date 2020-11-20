# deleteOne

删除集合中的一条记录。如果没有查询条件，则默认删除第一行。

## 方法定义

该方法的定义如下：

```
deleteOne(filter: object): Promise<MongoResult>
```

## 请求参数

该方法接收一个参数，其定义如下：

|字段名|类型|必填|说明|
|---|--|--|--|
|filter|Object|否|数据库操作时的过滤条件|

## 示例

```
mpserverless.db.collection('users').deleteOne({age: {$lt: 18}}).then((res) => {
  const hasDeleted = res.affectedDocs > 0;
}).catch(console.error);
```

