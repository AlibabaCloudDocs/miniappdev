# createQrcode {#concept_2151532 .concept}

生成小程序推广二维码。

## 方法定义 {#section_oj9_bs1_fv6 .section}

该方法的定义如下：

``` {#codeblock_0vy_8dp_wor}
createQrcode(params: QrcodeCreateRequest): Promise<FunctionResponse<QrcodeCreateResponse>>
```

## 请求参数 {#section_mj7_whb_m5t .section}

|字段名|类型|必填|说明|
|---|--|--|--|
|urlParam|string|是|小程序页面，例如：pages/index/index。|
|queryParam|object|是|自定义参数，JSON类型。|
|describe|string|是|推广二维码描述。|

## 返回参数 {#section_i40_6lx_vx6 .section}

|字段名|类型|说明|
|---|--|--|
|qrCodeUrl|string|推广二维码URL地址。|

## 示例 {#section_t4x_0cw_rv6 .section}

``` {#codeblock_gvx_n18_gje}
async createQrcode() {
  try {
    const res = await cloud.mini.createQrcode({
      urlParam: 'pages/index/index',
      queryParam: {
        data: 'data'
      },
      describe: '我是描述'
    });
    const { result } = res;
    const { qrCodeUrl } = result;
    // 进行业务处理
  } catch (e) {
    // 进行异常处理
  }
}
```

