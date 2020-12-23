安装客户端SDK3.0版本 
==================================

通过小程序云SDK，您可以在小程序中直接访问小程序云Serverless服务。

前提条件 
-------------------------

* 在首次使用小程序云服务前，您需要开通小程序云服务。详情信息，请参见[开通小程序云服务](/cn.zh-CN/开通小程序云服务/开通小程序云服务.md)。

  

* 在使用小程序云SDK前请确保已经正确安装了Node.js开发环境。详情信息，请参见[nodejs官方安装教程](http://nodejs.cn/learn/how-to-install-nodejs)。

  




在支付宝小程序中使用SDK 
----------------------------------

完成以下操作，在支付宝小程序中使用SDK：

1. 在支付宝小程序项目的根目录执行以下命令安装SDK。

       npm install --save @alicloud/mpserverless-sdk@3.0.0

   

2. 在小程序项目中的app.js中添加以下代码，构造小程序云SDK的实例对象。

       // app.js
       import MPServerless from '@alicloud/mpserverless-sdk'
       
       const mpserverless = new MPServerless(my, {
           appId: '1234456789', // 小程序应用标识
           spaceId: 'db4dd657-7041-470a-90xxxxx', // 服务空间标识
           clientSecret: '6c3c86xxxx6', // 服务空间 secret key
           endpoint: 'https://endpoint', // 服务空间地址，从小程序Serverless控制台处获得
       });

   

   其中：
   * my是支付宝小程序开发者工具中的全局基础库，可以在开发环境中直接获取。

     
   
   * appId是小程序的ID。您可以在支付宝小程序开发者工具中直接获取小程序的App ID。

     ![xsacv](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1540358061/p203199.png)
     
   
   * spaceId、clientSecret和endpoint在小程序Serverless控制台创建服务空间后可以获得。详情参见[创建服务空间](/cn.zh-CN/基础操作/服务空间管理/创建服务空间.md)。

     ![对方曾让你](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1540358061/p203202.png)
     
   

   

3. 在app.js的onLaunch生命周期中调用init接口完成初始化 **。** 

   **说明**

   在小程序端开始使用 serverless 服务前，需先调用mpserverless.init方法完成服务的初始化。在小程序中，我们建议您在onLaunch生命周期中进行初始化操作，并将小程序云SDK的实例对象挂载到小程序的全局APP对象之上，以便后续在其他文件中调用。

       // app.js
       App({
         mpserverless: mpserverless,
         onLaunch() {
           mpserverless.init(); // 您可以通过 result 来判断初始化完成情况
         },
       });

   

4. 在其他文件中使用SDK。

   **说明**

   在其他文件中可以通过getApp的方式从全局对象APP中获取SDK的实例对象。

       // 其他文件中使用 sdk
       const { mpserverless } = getApp();
       
       mpserverless.db.collection('test').find();
       mpserverless.function.invoke('test');

   




在微信小程序中使用SDK 
---------------------------------

完成以下操作，在微信小程序中使用小程序云SDK：

1. 在微信小程序项目的根目录执行以下命令安装SDK。

       npm install --save @alicloud/mpserverless-sdk@3.0.0

   

2. 在微信小程序IDE中单击 **工具\>构建npm** 。

   ![aDWFEVG](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1540358061/p203307.png)
   

3. 在小程序项目中的app.js中添加以下代码，构造小程序云SDK的实例对象。

       // app.js
       import MPServerless from '@alicloud/mpserverless-sdk'
       
       const mpserverless = new MPServerless(wx, {
           appId: '1234456789', // 小程序应用标识
           spaceId: 'db4dd657-7041-470a-90xxxxx', // 服务空间标识
           clientSecret: '6c3c86xxxx6', // 服务空间 secret key
           endpoint: 'https://endpoint', // 服务空间地址，从小程序Serverless控制台处获得
       });

   

   其中：
   * wx是微信小程序IDE中的全局基础库，可以在开发环境中直接获取。

     
   
   * appId是小程序的ID。您可以在微信开发者工具中直接获取小程序的App ID。

     ![AXCSVD](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1540358061/p203214.png)
     
   
   * spaceId、clientSecret和endpoint在小程序Serverless控制台创建服务空间后可以获得。详情参见[创建服务空间](/cn.zh-CN/基础操作/服务空间管理/创建服务空间.md)。

     ![dwqfev](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1540358061/p203216.png)
     
   

   

4. 在app.js的onLaunch生命周期中调用init接口完成初始化 **。** 

   **说明**

   在小程序端开始使用serverless服务前，需先调用mpserverless.init方法完成服务的初始化。在小程序中，我们建议您在onLaunch生命周期中进行初始化操作，并将小程序云SDK的实例对象挂载到小程序的全局APP对象之上，以便后续在其他文件中调用。

       App({
         mpserverless: mpserverless,
         onLaunch(options) {
           mpserverless.init(); // 您可以通过 result 来判断初始化完成情况
         },
       });

   

5. 在其他文件中使用SDK。

   **说明**

   在其他文件中可以通过getApp的方式从全局对象APP中获取SDK的实例对象。

       // 其他文件中使用 sdk
       const { mpserverless } = getApp();
       
       mpserverless.db.collection('test').find();
       mpserverless.function.invoke('test');

   




在钉钉小程序中使用SDK 
---------------------------------

完成以下操作，在第三方个人应用的钉钉小程序中使用小程序云SDK：

1. 在钉钉小程序项目的根目录执行以下命令安装SDK **。** 

       npm install --save @alicloud/mpserverless-sdk@3.0.0

   

2. 在小程序项目中的app.js中添加以下代码，构造小程序云SDK的实例对象。

       // app.js
       import MPServerless from '@alicloud/mpserverless-sdk'
       
       const mpserverless = new MPServerless(dd, {
           appId: '1234456789', // 小程序应用标识
           spaceId: 'db4dd657-7041-470a-90xxxxx', // 服务空间标识
           clientSecret: '6c3c86xxxx6', // 服务空间 secret key
           endpoint: 'https://endpoint', // 服务空间地址，从小程序Serverless控制台处获得
       });

   

   其中：
   * dd 是钉钉小程序开发者工具的全局基础库，可以在开发环境中直接获取。

     
   
   * appId是小程序的ID。可以在[钉钉开放平台](https://open-dev.dingtalk.com/)获取。

     ![saxacv](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1540358061/p203224.png)
     
   
   * spaceId、clientSecret和endpoint在小程序Serverless控制台创建服务空间后可以获得。详情参见[创建服务空间](/cn.zh-CN/基础操作/服务空间管理/创建服务空间.md)。

     ![dxswfev](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1540358061/p203220.png)
     
   

   

3. 在app.js的onLaunch生命周期中调用init接口完成初始化 **。** 

   **说明**

   在小程序端开始使用serverless服务前，需先调用mpserverless.init方法完成服务的初始化。在小程序中，我们建议您在onLaunch生命周期中进行初始化操作，并将小程序云SDK的实例对象挂载到小程序的全局APP对象之上，以便后续在其他文件中调用。

       App({
         mpserverless: mpserverless,
         onLaunch(options) {
           await mpserverless.init(); // 您可以通过 result 来判断初始化完成情况
         },
       });

   

4. 在其他文件中使用SDK。

   **说明**

   在其他文件中可以通过getApp的方式从全局对象APP中获取SDK的实例对象。

       // 其他文件中使用 sdk
       const { mpserverless } = getApp();
       
       mpserverless.db.collection('test').find();
       mpserverless.function.invoke('test');

   



