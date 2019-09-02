# getInfo {#concept_645208 .concept}

获取用户信息。

## 方法定义 {#section_9ur_mbc_5xs .section}

该方法的定义如下：

``` {#codeblock_3x9_6ef_9rs}
mpserverless.user.getInfo(options: string): Promise<Result>
```

## 请求参数 {#section_9dt_1s5_1az .section}

该方法不需要传递请求参数。

|字段名|类型|必填|说明|
|---|--|--|--|
|options|String|否|\{String\}\[authProvider\] 指定客户端类型，取值： -   alipay\_openapi（默认值）
-   wechat\_openapi

 |

## 返回参数 {#section_het_92i_9f4 .section}

|字段名|类型|说明|
|---|--|--|
|success|Boolean|操作是否成功。|
|result|Object|用户信息： -   spaceId\{String\}：服务空间ID。
-   userId\{String\}：用户ID。
-   AuthUserId\{String\}：客户端类型。只有指定了authProvider时才会返回该参数。

 |

## 示例 {#section_hze_d1s_fgv .section}

``` {#codeblock_s36_gy0_8pd}
mpserverless.user.getInfo().then(user => {
  this.setData(userInfo: user);
}).catch(console.error);
```

