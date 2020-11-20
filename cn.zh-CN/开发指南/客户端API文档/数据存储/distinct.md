# distinct

获取某个属性去重后的所有记录。

## 方法定义

该方法的定义如下：

```
distinct(key: string, query: object, options?: object): Promise<MongoResult>
```

## 请求参数

该方法接收 3 个参数，其定义如下：

|字段名|类型|必填|说明|
|---|--|--|--|
|key|String|是|待获取的属性名。|
|query|Object|是|数据库操作时的查询条件。|
|options|Object|否|控制项。|

## 示例

```
mpserverless.db.collection('users').distinct('name', {age: {$gt: 18}})
.then((res) => {})
.catch(console.error);
```

