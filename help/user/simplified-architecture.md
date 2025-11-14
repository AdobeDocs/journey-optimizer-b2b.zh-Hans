---
title: 简化的架构设置
description: 在简化的架构上设置Journey Optimizer B2B edition 。 配置XDM架构、电子邮件/短信渠道、Marketo Engage历程操作和用户。
feature: Setup, Administration
role: Admin, Data Engineer
hide: true
hidefromtoc: true
source-git-commit: bbb9ff0deeb55c4cb132c6c97ec04f53a97339c6
workflow-type: tm+mt
source-wordcount: '1385'
ht-degree: 6%

---

# 简化的架构设置

Adobe Journey Optimizer B2B Edition 现已采用简化架构。通过此更新，Journey Optimizer B2B Edition 与 Marketo Engage 不再共享同一系统或数据存储库。Journey Optimizer B2B Edition 仅从 Adobe Experience Platform 接收数据。但仍依赖 Marketo Engage 的使用权限及部分配置功能来完成系统的部署与设置。

简化的架构是解锁Adobe Journey Optimizer B2B edition中新功能的基础：

* **轻松统一和扩展您的数据：**&#x200B;新平台支持复杂的数据模型，包括自定义对象、购买群组和帐户事件。 

* **连接多个Adobe Marketo Engage实例：**&#x200B;在一个位置管理和统一多个Adobe Marketo Engage环境中的数据。

* **保护您的数据安全：**&#x200B;高级隐私和安全功能有助于保护您的客户信息。 （_即将推出_）

* **面向未来构建：**&#x200B;此升级为您准备好持续的改进和创新。 

对于为此架构配置的环境，请使用以下配置准则。

## 命名空间和架构

有关概述，请参阅Experience Platform文档中的[B2B命名空间和架构](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo-namespaces)。

### 环境设置

设置Postman环境以支持B2B命名空间和模式自动生成实用程序。

* 您可以从[GitHub存储库](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility)下载命名空间和架构自动生成实用程序集合和环境。

* 有关如何使用Experience Platform API的信息，包括有关如何收集所需标头的值和读取示例API调用的详细信息，请参阅[Experience Platform API快速入门](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/landing/platform-apis/api-guide)指南。

* 有关如何生成Experience Platform API凭据的信息，请参阅有关[身份验证和访问Experience Platform API](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication)的教程。

* 有关为Experience Platform API设置Postman的信息，请参阅Adobe Experience Platform中[Postman](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman)的详细步骤。

通过设置Experience Platform开发人员控制台和Postman，您现在可以开始将相应的环境值应用于您的Postman环境。

### 运行脚本

通过Postman收藏集和环境设置，您可以通过Postman界面运行脚本。

在Postman界面中，选择自动生成器实用工具的根文件夹，然后从顶部标题中选择&#x200B;**运行**。

显示Runner界面时，请确保选中了所有复选框，然后选择&#x200B;**运行命名空间和架构自动生成实用程序**。

成功的请求将创建B2B所需的命名空间和架构。

## XDM字段选择

您可以在Journey Optimizer B2B edition UI中管理整个应用程序中可用的XDM字段。 这些字段通过仅公开与生成&#x200B;**_历程_**、**_购买群_**&#x200B;或&#x200B;**_电子邮件个性化_**&#x200B;相关的字段来帮助简化实例。

### XDM类

#### 标准类

使用以下步骤可定义标准XDM类的字段：

1. 导航到&#x200B;**[!UICONTROL 管理] > [!UICONTROL 配置]**。

1. 在导航面板中，选择&#x200B;**[!UICONTROL XDM类]**。

1. 选择&#x200B;**[!UICONTROL 标准]**&#x200B;选项卡以查看可用的XDM类：

   * XDM 个人轮廓

   * XDM业务帐户

#### 受管字段

定义在整个应用程序中可用的字段。

1. 单击&#x200B;_更多菜单_ (**...**)图标并选择&#x200B;**[!UICONTROL 编辑托管字段]**。

1. 查看可用字段的列表（单击字段元数据的&#x200B;_信息_&#x200B;图标）。

1. 选择要包含的字段，并清除不需要的字段选择。

1. 使用&#x200B;**[!UICONTROL 仅显示选定的字段]**&#x200B;滑块来查看您的选择。

1. 单击&#x200B;**[!UICONTROL 保存]**。

#### 可更新字段

选择可以通过&#x200B;**[!UICONTROL 更新帐户配置文件]**&#x200B;或&#x200B;**[!UICONTROL 更新人员配置文件]**&#x200B;历程操作修改的字段。

1. 单击&#x200B;_更多菜单_ (**...**)图标并选择&#x200B;**[!UICONTROL 编辑可更新字段]**。

1. 选择&#x200B;**[!UICONTROL 架构]**，然后选择&#x200B;**[!UICONTROL 数据集]**。

   这些架构和数据集由您的组织提供。

1. 查看可更新字段的列表（单击元数据的&#x200B;_信息_&#x200B;图标）。

   只能编辑托管字段。

1. 选择要使其可从历程更新的字段。

1. 单击&#x200B;**保存**

### 关系架构

选择[关系架构](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational)以在&#x200B;**_历程决策_**&#x200B;和&#x200B;**_个性化_**&#x200B;中使用。 目前，这些架构适用于自定义对象用例。 将来，关系架构也可用于其他对象用例。

1. 选择&#x200B;**[!UICONTROL 关系]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 选择关系XDM类]**。

   目前，仅支持帐户多对一自定义对象。

1. 查看架构字段列表（单击&#x200B;_信息_&#x200B;图标以查看元数据）。

1. 选择要包含的字段。

1. 使用&#x200B;**[!UICONTROL 仅显示选定的字段]**&#x200B;滑块来查看您的选择。

1. 单击&#x200B;**[!UICONTROL 保存]**。

>[!NOTE]
>
>请注意，关系架构必须具有以下配置：
>
><li>行为：记录
&gt; <li>分段：已启用
&gt; <li>关系类型：多对一
&gt; <li>引用架构：[B2B帐户 — XDM业务帐户架构](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/schemas/create-schemas-for-b2b-data)
&gt; <li>必填字段：主键、外键和版本描述符
&gt; <li>关联的数据集：已定义并映射到架构

### 事件

选择要在&#x200B;**_journey decisioning_**&#x200B;中使用的体验事件。

1. 选择&#x200B;**[!UICONTROL 事件]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 选择体验事件]**。

1. 单击&#x200B;**[!UICONTROL 选择事件类型]**，选择事件类型，单击&#x200B;**[!UICONTROL 选择]**。

1. 单击&#x200B;**[!UICONTROL 选择字段]**，选择所需的字段，单击&#x200B;**[!UICONTROL 选择]**。

1. 单击&#x200B;**[!UICONTROL 保存]**。

## 电子邮件配置

应将以下内容配置为从Journey Optimizer B2B edition发送电子邮件。  

[https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols)

### 跟踪和电子邮件传递协议

1. [为电子邮件创建DNS记录](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#create-dns-records-for-landing-pages-and-email)

1. [设置SPF和DKIM](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-spf-and-dkim)

1. [设置DMARC](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-dmarc)

1. [为您的域设置MX记录](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-mx-records-for-your-domain)

1. 列入允许列表 [将出站IP地址添加到](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#outbound-ip-addresses)

1. 如果您需要共享专用IP池，请联系可投放性团队以了解可行性和辅助设置。

### 电子邮件渠道配置

在简化的架构中，可从Marketo Engage UI配置电子邮件设置。 完成与电子邮件相关的设置步骤：[https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps)

[https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails)

### 通信限制

1. 在左侧导航中，选择&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**。

1. 在导航面板中，选择&#x200B;**[!UICONTROL 通信限制]**。

1. 创建全局通信限制规则集(默认情况下，此规则集在每个Journey Optimizer B2B edition实例中创建)。

   如果未创建全局规则集，则没有通信限制。

<!-- In the future, you can also add local communication limit rule sets (AJO B2C doc can be found here [https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets). We may need a small update for our B2B version.) -->

### 共享通信限制

在新架构中，Journey Optimizer B2B edition和Marketo Engage默认具有独立的通信限制。

如果您希望Marketo Engage实例共享Journey Optimizer B2B edition实例中设置的通信限制，请联系Adobe支持部门获取配置帮助或打开支持服务单。 根据请求，工程团队可以在Journey Optimizer B2B edition和一个或多个Marketo Engage实例之间共享通信限制。

目前，必须通过API调用设置Marketo Engage实例中的共享通信限制。

例如，当：

* Journey Optimizer B2B edition实例的munchkinId为`JKL-567-MNO`。
* Marketo Engage实例的munchkinId为`ABC-123-DEF`，它位于SJ数据中心中

API请求应当类似于以下内容：

```
curl --location --request POST 'http://sjrest2a.marketo.org/rest/v1/fm.json?_munchkinId=ABC-123-DEF&featureName=Mktmail%20Config&paramName=ajoB2bMappingMunchkinId&dataType=string&value=JKL-567-MNO'
```

## 短信渠道配置

有关详细信息，请参阅&#x200B;[_短信配置_](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-sms)。

## 历程中的Marketo Engage操作

您可以配置一个或多个远程&#x200B;**_Marketo Engage_**&#x200B;实例，以便与以下历程操作一起使用：

* 添加到Marketo列表
* 从Marketo列表中删除
* 添加到Marketo请求营销活动

完成以下步骤以配置这些连接：

1. 导航到&#x200B;**[!UICONTROL 管理] > [!UICONTROL 配置]**。

1. 在导航面板中，选择&#x200B;**[!UICONTROL XDM类]**。

1. 选择&#x200B;**[!UICONTROL 集成]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 创建连接]**。

1. 输入&#x200B;**[!UICONTROL Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**。

1. 为匹配的人员记录选择&#x200B;**[!UICONTROL 更新策略]**。

1. 输入&#x200B;**[!UICONTROL Munchkin ID]**、**[!UICONTROL 客户端ID]**、**[!UICONTROL 客户端密钥]**，然后单击&#x200B;**[!UICONTROL 连接到Marketo]**。

1. 单击&#x200B;**[!UICONTROL 创建]**。

## 用户载入

有关概述，请参阅[用户管理](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management)页面。

### 现有用户组

如果所有现有Journey Optimizer B2B edition用户都需要访问新架构，请使用现有Journey Optimizer B2B edition用户组。 系统管理员或产品管理员可以执行以下步骤。

1. 在专用的Marketo Engage中创建产品配置文件。

1. 将现有用户组添加到创建的产品配置文件。

配置文件会授予已分配给该用户组的所有角色和权限，这些角色和权限应已配置为用户能够访问Journey Optimizer B2B edition。 如果只有部分用户应访问新架构，请完成下面列出的步骤。 [当前文档](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management)中提供了更多详细信息。

### 创建新用户组

1. 在专用的Marketo Engage实例中创建产品配置文件。
1. 为新用户创建用户组。
1. 选择所需的产品配置文件并将其分配给用户组：

   * 您创建的Marketo Engage配置文件
   * Adobe Experience Platform配置文件
      * AEP-Default-All-Users
      * Adobe Experience Platform 数据收集
      * 数据收集所有访问

1. 将用户添加到用户组。
1. 在Experience Platform中向Journey Optimizer B2B edition角色添加新用户组。
