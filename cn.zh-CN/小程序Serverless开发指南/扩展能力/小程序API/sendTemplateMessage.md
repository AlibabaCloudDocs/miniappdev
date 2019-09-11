# sendTemplateMessage {#concept_2151561 .concept}

发送小程序模板消息，依赖于表单组件获取Form ID。

## 方法定义 {#section_5sn_r5h_1v6 .section}

该方法的定义如下：

``` {#codeblock_7nt_25h_zqu}
sendTemplateMessage(params: TemplateMessageSendRequest): Promise<FunctionResponse<TemplateMessageSendResponse>>
```

## 请求参数 {#section_6xy_5i1_ivv .section}

|字段名|类型|必填|说明|
|---|--|--|--|
|toUserId|string|是|接受者的User ID。|
|formId|string|是|用户触发的表单 ID，通过表单组件可获取。|
|userTemplateId|string|是|模板ID，通过后台创建模板的时候获取。|
|page|string|是|点击模板默认打开的小程序页面，例如：pages/index/index。|
|data|object|是|模板绑定的关键字，`{ keyword1: { value: ‘Alipay' } }`|

## 返回参数 {#section_inp_0qs_ewb .section}

|字段名|数据类型|说明|
|---|----|--|
|requestId|String|请求ID。|
|success|Boolean|请求是否成功。|
|result|Any|请求响应数据，结构与具体 API 有关。|

## 示例 {#section_fx5_wyw_bfg .section}

``` {#codeblock_wzp_1ve_c6i}
sendTemplateMessage() {
  my.getAuthCode({
    scopes: ['auth_user'],
    success: async authRes => {
      const { authCode } = authRes;
      try {
        // 可配合 getToken API 获取 userId 进行发送
        const tokenRes = await cloud.base.oauth.getToken({
          grantType: 'authorization_code',
          code: authCode,
        });
        const userId = tokenRes.result.userId;
        const res = await cloud.mini.sendTemplateMessage({
          toUserId: userId,
          userTemplateId: '', // 后台模板ID
          formId: '', // 用户触发表单提交的时候存储的 formId
          page: 'pages/index/index',
          data: {
            keyword1: {
              value: +new Date()
            }
          }
        });
        // 进行业务处理
      } catch (e) {
        // 进行异常处理
      }
    },
  });
}
```

