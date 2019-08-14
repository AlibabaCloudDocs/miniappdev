# 安装客户端SDK 1.0版本 {#task_744606 .task}

通过小程序云SDK，您可以在小程序中直接访问小程序云Serverless服务。

1.  在小程序项目的根目录执行以下命令安装SDK。 

    ``` {#codeblock_ca8_4wv_n4m}
    npm install @alicloud/mpserverless-sdk@1.0.3 --save
    ```

2.  执行以下代码完成初始化。 

    ``` {#codeblock_zkb_jzg_edv}
    import MPServerless from '@alicloud/mpserverless-sdk';
    const serverless = new MPServerless({
      uploadFile: my.uploadFile,
      request: my.request, 
      getAuthCode: my.getAuthCode || function (options) {
        // 通过授权页面拿到授权 code
        const code = getAuthCodeByAuthorizePage(options);
        options.complete({ authCode: code });
      },
    }, {
      appId: '1234456789', // 小程序应用标识
      spaceId: 'db4dd657-7041-470a-90xxxxx', // 服务空间标识
      clientSecret: '6c3c86xxxx6', // 服务空间 secret key
      endpoint: 'https://endpoint'， // 服务空间地址，从小程序Serverless控制台处获得
    });
    ```

    其中：

    -   appId是小程序的ID。您可以在支付宝小程序控制台获得。
    -   spaceIdclientSecret和endpoint在小程序Serverless控制台创建服务空间后可以获得。详情参见[创建服务空间](cn.zh-CN/小程序Serverless开发指南/服务空间管理/创建服务空间.md#)。

