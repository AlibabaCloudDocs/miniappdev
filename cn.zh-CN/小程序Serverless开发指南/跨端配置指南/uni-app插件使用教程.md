# uni-app插件使用教程 {#task_1732525 .task}

uni-app跨端小程序插件支持在阿里云小程序开发者工具中将uni-app工程编译为微信小程序，并同时打开微信开发者工具。

确保您安装的是最新版本小程序开发者工具。

## 步骤一 安装uni-app插件 {#section_7na_fln_6p6 .section}

完成以下操作，安装uni-app插件：

1.  打开小程序开发者工具，选择**小程序云** \> **uni-app**。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1372230/156595321455998_zh-CN.png)

2.  在左侧工具栏，单击插件市场图标，单击uni-app插件的**安装**按钮。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1372230/156595321455991_zh-CN.png)

3.  安装完成后，单击**启用**。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1372230/156595321455996_zh-CN.png)


## 步骤二 配置插件 {#section_psv_w3v_2oo .section}

启用插件后，完成以下步骤配置uni-app插件：

1.  在IDE上部菜单栏，单击**扩展** \> **uni-app小程序插件** \> **打开**。 

    **说明：** 确保您打开的是小程序uni-app项目工程，否则无法打开uni-app插件配置页面。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1372230/156595321456016_zh-CN.png)

2.  在**微信开发者工具路径**文本框中输入微信开发者工具的安装路径，然后单击**保存**。 微信开发者工具的默认安装路径如下，请根据实际情况输入。

    -   MacOS：/Applications/wechatwebdevtools.app
    -   Windows：C:/Program Files\(x86\)/Tecent/微信web开发者工具
    **说明：** 

    -   只有首次使用时需要配置IDE安装路径。
    -   微信开发者工具必须打开服务端口，否则无法唤醒IDE。详细信息，请参见[微信 IDE - 安全设置](https://developers.weixin.qq.com/miniprogram/dev/devtools/settings.html#%E5%AE%89%E5%85%A8%E8%AE%BE%E7%BD%AE)。
    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1372230/156595321556003_zh-CN.png)

    如果路径配置正确，在单击**保存**后，系统会提示**更新成功**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1372230/156595321556009_zh-CN.png)


## 步骤三 执行编译 {#section_3jj_lv8_n39 .section}

完成以下操作，执行uni-app工程编译：

1.  在uni-app小程序插件页面，单击**开始编译**。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1372230/156595321556011_zh-CN.png)

2.  编译成功后，会自动打开微信小程序开发者工具并加载编译后的微信小程序文件。 您可以在./dist/dev/mp-weixin文件目录下查看微信小程序的相关文件。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1372230/156595321556014_zh-CN.png)


