# API概览

小程序云Serverless提供以下相关API接口。

## 服务空间

|API|描述|
|---|--|
|[CreateSpace](/cn.zh-CN/开发指南/管控API文档/服务空间/CreateSpace.md)

|调用CreateSpace创建一个服务空间。|
|[ListSpace](/cn.zh-CN/开发指南/管控API文档/服务空间/ListSpace.md)

|调用ListSpace查询服务空间列表。|
|[DeleteSpace](/cn.zh-CN/开发指南/管控API文档/服务空间/DeleteSpace.md)

|调用DeleteSpace删除一个服务空间。|

## 云函数

|API|描述|
|---|--|
|[CreateFunction](/cn.zh-CN/开发指南/管控API文档/云函数/CreateFunction.md)

|调用CreateFunction创建云函数。|
|[DeleteFunction](/cn.zh-CN/开发指南/管控API文档/云函数/DeleteFunction.md)

|调用DeleteFunction删除函数。|
|[ListFunction](/cn.zh-CN/开发指南/管控API文档/云函数/ListFunction.md)

|调用ListFunction查询函数列表。|
|[UpdateFunction](/cn.zh-CN/开发指南/管控API文档/云函数/UpdateFunction.md)

|调用UpdateFunction更新函数。|
|[DescribeFunction](/cn.zh-CN/开发指南/管控API文档/云函数/DescribeFunction.md)

|调用DescribeFunction获取一个函数的详细信息。|
|[DeployFunction](/cn.zh-CN/开发指南/管控API文档/云函数/DeployFunction.md)

|调用DeployFunction部署函数。|
|[ListFunctionDeployment](/cn.zh-CN/开发指南/管控API文档/云函数/ListFunctionDeployment.md)

|调用ListFunctionDeployment查询函数部署记录。|
|[CreateFunctionDeployment](/cn.zh-CN/开发指南/管控API文档/云函数/CreateFunctionDeployment.md)

|调用CreateFunctionDeployment上传函数包。|
|[RunFunction](/cn.zh-CN/开发指南/管控API文档/云函数/RunFunction.md)

|调用RunFunction执行函数。|
|[ListFunctionLog](/cn.zh-CN/开发指南/管控API文档/云函数/ListFunctionLog.md)

|调用ListFunctionLog查询函数执行日志。|

## 数据存储

|API|描述|
|---|--|
|[RunDBCommand](/cn.zh-CN/开发指南/管控API文档/数据存储/RunDBCommand.md)

|调用RunFunction执行数据库命令。|
|[DeleteDBCollection](/cn.zh-CN/开发指南/管控API文档/数据存储/DeleteDBCollection.md)

|调用DeleteDBCollection删除数据集。|
|[CreateDBExportTask](/cn.zh-CN/开发指南/管控API文档/数据存储/CreateDBExportTask.md)

|调用CreateDBExportTask创建数据库导出任务。|
|[QueryDBExportTaskStatus](/cn.zh-CN/开发指南/管控API文档/数据存储/QueryDBExportTaskStatus.md)

|调用QueryDBExportTaskStatus查询数据库导出任务状态。|
|[CreateDBImportTask](/cn.zh-CN/开发指南/管控API文档/数据存储/CreateDBImportTask.md)

|调用CreateDBImportTask创建数据库导入任务。|
|[QueryDBImportTaskStatus](/cn.zh-CN/开发指南/管控API文档/数据存储/QueryDBImportTaskStatus.md)

|调用QueryDBImportTaskStatus查询数据库导入状态。|

## 文件存储

|API|描述|
|---|--|
|[ListFile](/cn.zh-CN/开发指南/管控API文档/文件存储/ListFile.md)

|调用ListFile查询文件列表。|
|[DescribeFileUploadSignedUrl](/cn.zh-CN/开发指南/管控API文档/文件存储/DescribeFileUploadSignedUrl.md)

|调用DescribeFileUploadSignedUrl获取上传文件需要的签名。|
|[RegisterFile](/cn.zh-CN/开发指南/管控API文档/文件存储/RegisterFile.md)

|调用RegisterFile注册文件。|
|[DeleteFile](/cn.zh-CN/开发指南/管控API文档/文件存储/DeleteFile.md)

|调用DeleteFile删除文件。|

## 权限设置

|API|描述|
|---|--|
|[UpdateServicePolicy](/cn.zh-CN/开发指南/管控API文档/权限设置/UpdateServicePolicy.md)

|调用UpdateServicePolicy更新权限。|
|[DescribeServicePolicy](/cn.zh-CN/开发指南/管控API文档/权限设置/DescribeServicePolicy.md)

|调用DescribeServicePolicy查询权限规则。|

## 开放平台设置

|API|描述|
|---|--|
|[ListOpenPlatformConfig](/cn.zh-CN/开发指南/管控API文档/开放平台设置/ListOpenPlatformConfig.md)

|调用ListOpenPlatformConfig查询支付宝、微信开放平台配置。|
|[SaveAntOpenPlatformConfig](/cn.zh-CN/开发指南/管控API文档/开放平台设置/SaveAntOpenPlatformConfig.md)

|调用SaveAntOpenPlatformConfig保存支付宝开放平台配置。|
|[DeleteAntOpenPlatformConfig](/cn.zh-CN/开发指南/管控API文档/开放平台设置/DeleteAntOpenPlatformConfig.md)

|调用DeleteAntOpenPlatformConfig删除支付宝开放平台配置。|
|[SaveWechatOpenPlatformConfig](/cn.zh-CN/开发指南/管控API文档/开放平台设置/SaveWechatOpenPlatformConfig.md)

|调用SaveWechatOpenPlatformConfig保存微信开放平台配置。|
|[DeleteWechatOpenPlatformConfig](/cn.zh-CN/开发指南/管控API文档/开放平台设置/DeleteWechatOpenPlatformConfig.md)

|调用DeleteWechatOpenPlatformConfig删除微信开放平台配置。|
|[ListDingtalkOpenPlatformConfigs](/cn.zh-CN/开发指南/管控API文档/开放平台设置/ListDingtalkOpenPlatformConfigs.md)

|调用ListDingtalkOpenPlatformConfigs查询钉钉开放平台配置。|
|[AddDingtalkOpenPlatformConfig](/cn.zh-CN/开发指南/管控API文档/开放平台设置/AddDingtalkOpenPlatformConfig.md)

|调用AddDingtalkOpenPlatformConfig添加钉钉开放平台配置。|
|[UpdateDingtalkOpenPlatformConfig](/cn.zh-CN/开发指南/管控API文档/开放平台设置/UpdateDingtalkOpenPlatformConfig.md)

|调用UpdateDingtalkOpenPlatformConfig更新钉钉开放平台配置。|
|[DeleteDingtalkOpenPlatformConfig](/cn.zh-CN/开发指南/管控API文档/开放平台设置/DeleteDingtalkOpenPlatformConfig.md)

|调用DeleteDingtalkOpenPlatformConfig删除钉钉开放平台配置。|

## 扩展能力

|API|描述|
|---|--|
|[ListExtensions](/cn.zh-CN/开发指南/管控API文档/扩展能力/ListExtensions.md)

|调用ListExtensions查询扩展能力。|
|[EnableExtension](/cn.zh-CN/开发指南/管控API文档/扩展能力/EnableExtension.md)

|调用EnableExtension开通扩展能力。|

## HTTP触发配置

|API|描述|
|---|--|
|[UpdateHttpTriggerConfig](/cn.zh-CN/开发指南/管控API文档/HTTP触发配置/UpdateHttpTriggerConfig.md)|调用UpdateHttpTriggerConfig更新云函数的HTTP触发配置。|
|[DescribeHttpTriggerConfig](/cn.zh-CN/开发指南/管控API文档/HTTP触发配置/DescribeHttpTriggerConfig.md)|调用DescribeHttpTriggerConfig查询云函数的HTTP触发配置。|

## 静态网站托管

|API|描述|
|---|--|
|[OpenWebHostingService](/cn.zh-CN/开发指南/管控API文档/静态网站托管/OpenWebHostingService.md)|调用OpenWebHostingService开通静态网站托管功能。|
|[GetWebHostingStatus](/cn.zh-CN/开发指南/管控API文档/静态网站托管/GetWebHostingStatus.md)|调用GetWebHostingStatus查询静态网站托管功能开通状态。|
|[GetWebHostingConfig](/cn.zh-CN/开发指南/管控API文档/静态网站托管/GetWebHostingConfig.md)|调用GetWebHostingConfig查询静态网站配置。|
|[ModifyWebHostingConfig](/cn.zh-CN/开发指南/管控API文档/静态网站托管/ModifyWebHostingConfig.md)|调用ModifyWebHostingConfig更新静态网站配置。|
|[ListWebHostingFiles](/cn.zh-CN/开发指南/管控API文档/静态网站托管/ListWebHostingFiles.md)|调用ListWebHostingFiles分页获取网站静态文件。|
|[GetWebHostingUploadCredential](/cn.zh-CN/开发指南/管控API文档/静态网站托管/GetWebHostingUploadCredential.md)|调用GetWebHostingUploadCredential获取静态网站托管的上传文件凭证。|
|[DeleteWebHostingFile](/cn.zh-CN/开发指南/管控API文档/静态网站托管/DeleteWebHostingFile.md)|调用DeleteWebHostingFile删除静态网站托管下的文件。|
|[ListWebHostingCustomDomains](/cn.zh-CN/开发指南/管控API文档/静态网站托管/ListWebHostingCustomDomains.md)|调用ListWebHostingCustomDomains查询当前静态网站绑定的自定义域名。|
|[SaveWebHostingCustomDomainConfig](/cn.zh-CN/开发指南/管控API文档/静态网站托管/SaveWebHostingCustomDomainConfig.md)|调用SaveWebHostingCustomDomainConfig保存域名配置。|
|[BindWebHostingCustomDomain](/cn.zh-CN/开发指南/管控API文档/静态网站托管/BindWebHostingCustomDomain.md)|调用BindWebHostingCustomDomain添加自定义域名。|
|[UnbindWebHostingCustomDomain](/cn.zh-CN/开发指南/管控API文档/静态网站托管/UnbindWebHostingCustomDomain.md)|调用UnbindWebHostingCustomDomain删除一个自定义域名。|
|[GetWebHostingCertificateDetail](/cn.zh-CN/开发指南/管控API文档/静态网站托管/GetWebHostingCertificateDetail.md)|调用GetWebHostingCertificateDetail查询自定义域名关联的证书详情。|
|[AttachWebHostingCertificate](/cn.zh-CN/开发指南/管控API文档/静态网站托管/AttachWebHostingCertificate.md)|调用AttachWebHostingCertificate为自定义域名绑定证书。|
|[DeleteWebHostingCertificate](/cn.zh-CN/开发指南/管控API文档/静态网站托管/DeleteWebHostingCertificate.md)|调用DeleteWebHostingCertificate解绑证书，关闭HTTPS访问。|
|[DescribeWebHostingFile](/cn.zh-CN/开发指南/管控API文档/静态网站托管/DescribeWebHostingFile.md)|调用DescribeWebHostingFile查询静态网站托管下的一个文件详情。|
|[BatchDeleteWebHostingFiles](/cn.zh-CN/开发指南/管控API文档/静态网站托管/BatchDeleteWebHostingFiles.md)|调用BatchDeleteWebHostingFiles批量删除静态网站托管下的文件。|
|[MoveWebHostingFile](/cn.zh-CN/开发指南/管控API文档/静态网站托管/MoveWebHostingFile.md)|调用MoveWebHostingFile移动静态网站托管下的文件位置。|

