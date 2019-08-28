# invoke {#concept_645208 .concept}

调用云服务。

## 方法定义 {#section_9ur_mbc_5xs .section}

该方法的定义如下：

``` {#codeblock_3x9_6ef_9rs}
mpserverless.function.invoke(target: string, arg: {
  method: string,
  path?: string,
  header?: object,
  params?: object,
  query?: object,
  body?: object,
}): Promise<Result>
```

## 请求参数 {#section_9dt_1s5_1az .section}

该方法接收 6 个参数，其定义如下：

|字段名|类型|必填|说明|
|---|--|--|--|
|target|String|是|目标 AppService 名称。|
|arg|Object|是| -   \{String\}method 目标路由 HTTP 方法。
-   \{String\}\[path\] 目标路由。
-   \{String\}\[header\] 发送给目标路由的 HTTP Header。
-   \{Object\}\[params\] 若目标路由 SDK 组装好，Params 就不需要填写。
-   \{Object\}\[query\] 发送给目标路由的 HTTP Query。
-   \{Object\}\[body\] 发送给目标路由的 HTTP Body。

 |

## 返回参数 {#section_hze_d1s_fgv .section}

|字段名|类型|说明|
|---|--|--|
|success|Boolean|执行状态。|
|requestId|String|请求ID。|
|result|Any|接口返回内容，由开发者代码和请求参数 header 的 content-type 决定，默认 content-type 为 application/json。|

## 示例 {#section_bi5_kb6_iwb .section}

``` {#codeblock_shh_qv2_pqj}
mpserverless.function.invoke('appservice2', {
  method: 'GET',
  path: '/requestId',
  header: {
      'content-type': 'application/json',
  },
  params: {},
  query: {},
  body: {},
}).then(res => {
  console.log(res.result.requestId);
}).catch(err => {
  console.error(err);
});
```

