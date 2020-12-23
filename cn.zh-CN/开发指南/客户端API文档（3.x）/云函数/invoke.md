invoke 
===========================

调用云函数。

方法定义 
-------------------------

    mpserverless.function.invoke(functionName: string, functionArgs?: object): Promise<Result>



请求参数 
-------------------------



|     字段名      |   类型   | 必填 |    说明     |
|--------------|--------|----|-----------|
| functionName | String | 是  | 所调用的云函数名。 |
| functionArgs | Object | 否  | 目标云函数的参数。 |



返回参数 
-------------------------



|    字段名    |   类型    |                                       说明                                        |
|-----------|---------|---------------------------------------------------------------------------------|
| success   | Boolean | 执行状态。                                                                           |
| requestId | String  | 请求ID。                                                                           |
| result    | Any     | 接口返回内容，由开发者代码和请求参数 header 的 content-type 决定，默认 content-type 为 application/json。 |



示例 
-----------------------

假设已经有了一个云函数sum，云函数的定义如下。

    'use strict';
    
    module.exports = async (ctx) => {
      const {a, b} = ctx.args;
      return a + b;
    }



小程序端发起对云函数 `sum` 的调用示例如下。

    const { result } = await mpserverless.function.invoke('sum', { a: 1, b: 1 });
    console.log('1 + 1 = ', result);  // 1 + 1 = 2 



在云函数端任意云函数发起对云函数`sum`的调用示例如下。

    'use strict';
    
    module.exports = async (ctx) => {
      const { result } = ctx.mpserverless.function.invoke('sum', { a: 1, b: 1 });
      return result;
    }



