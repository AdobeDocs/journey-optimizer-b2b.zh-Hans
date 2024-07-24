---
title: 用户管理
description: 了解如何将团队成员分配给Journey Optimizer B2B版本产品配置文件。
feature: Setup
roles: Admin
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 1%

---

# 用户管理

完成配置并绑定沙盒后，请完成以下步骤以向团队和用户提供对Adobe Journey Optimizer B2B版本的访问权限。

1. [在Admin Console中创建Marketo Engage产品配置文件](#marketo-engage-profile)(仅新Marketo Engage实例)。
1. 在Admin Console中[创建用户组](#create-user-group)。
1. 在AEP权限中[创建角色](#create-role)。
1. 在Admin Console中[添加用户](#add-users)。

作为管理员，您可以在Adobe Admin Console中完成这些任务，该网站是管理Adobe产品许可证和用户的中心位置。 在Admin Console中，您可以在单个位置而不是在各种单独的解决方案中创建和管理用户。 请参阅[Admin Console概述](https://helpx.adobe.com/cn/enterprise/using/admin-console.html)页面，了解有关其功能和功能的更多信息。

## 访问Admin Console

在使用Admin Console管理团队中的用户之前，您需要确保可以访问该Admin Console并具有适当的权限。

1. 作为系统管理员，您应在载入流程中从Adobe收到多封电子邮件。

   查找欢迎电子邮件，其中提供了有关您被授予访问权限的组织名称的信息。

1. 单击欢迎电子邮件中的&#x200B;**[!UICONTROL 开始使用]**&#x200B;链接以导航到该Admin Console。

   如果找不到电子邮件，请直接打开浏览器，打开[https://adminconsole.adobe.com](https://adminconsole.adobe.com)上的Admin Console。

1. 使用您的Adobe ID登录。

   成功登录后，您将看到Adobe Admin Console的概述页面。

1. 如果您有权访问多个组织，请确保您已登录到正确的组织。

   要更改您的组织，请单击右上角的组织名称，然后选择您需要访问的组织。

1. 在用户信息卡中选择管理员，验证您是否为系统管理员。

1. 通过输入您的Adobe ID电子邮件、用户名、名字或姓氏进行搜索。

   * 如果您的访问权限配置正确，搜索将返回您的记录。

   * 如果&#x200B;**[!UICONTROL 管理员角色]**&#x200B;列中的值显示`System`，则表示您自己（或显示的用户）是系统管理员。

## 创建Marketo Engage产品配置文件 {#marketo-engage-profile}

授予用户访问Adobe解决方案的权限时，您不一定要授予他们完全访问权限。 产品配置文件使每个解决方案都有自己的用户权限集。 使用Admin Console分配产品配置文件。

>[!NOTE]
>
>这些步骤只能由Admin Console系统管理员或Marketo Engage产品管理员执行。

1. 登录到[https://adminconsole.adobe.com](https://adminconsole.adobe.com)。

1. 选择“产品”>“Marketo Engage”。

1. 单击“新建配置文件”并输入产品配置文件名称，如&#x200B;_标准用户_。

1. 单击下一步>保存

## 创建用户组 {#create-user-group}

用户组是指一组被授予共享权限的用户。 您可以在用户组中添加或删除用户。 当组内的用户发生更改时，组权限保持不变。

>[!NOTE]
>
>这些步骤只能由Admin Console系统管理员执行。

1. 登录到[https://adminconsole.adobe.com](https://adminconsole.adobe.com)。

1. 选择&#x200B;**[!UICONTROL 用户]** > **[!UICONTROL 用户组]** > **[!UICONTROL 新建用户组]**。

1. 输入用户组的名称，如&#x200B;_标准用户_，然后单击&#x200B;**[!UICONTROL 保存]**。

1. 单击刚刚创建的用户组。

1. 单击&#x200B;**[!UICONTROL 已分配的产品配置文件]** > **[!UICONTROL 分配配置文件]**。

1. 选择以下产品：
   * [!UICONTROL Marketo Engage — 标准用户]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Adobe Experience Platform数据收集 — 默认]
   * [!UICONTROL 数据收集所有访问权限]

1. 单击&#x200B;**[!UICONTROL 保存]**。

## 在AEP权限中创建角色 {#create-role}

权限是单一的权利，可用于定义分配给产品配置文件的授权。 每个权限都是通过某种功能（如历程或购买群组）收集的，该功能代表Journey Optimizer B2B版本中的不同功能或对象。

_权限_&#x200B;是Adobe Experience Platform的区域，管理员可以在其中定义用户角色和访问策略，以管理产品应用程序内功能和对象的访问权限。 在此应用程序中，您可以创建和管理角色，并为这些角色分配所需的资源权限。 权限还允许您管理与特定角色关联的标签、沙盒和用户。

>[!NOTE]
>
>要完成以下步骤，您必须是Adobe Experience Platform的产品管理员。

1. 转到[experience.adobe.com](https://experience.adobe.com/)。

1. 选择&#x200B;**[!UICONTROL 权限]**。

   >[!NOTE]
   >
   >如果您没有看到“权限”，则可能需要单击“查看全部”并从可用应用程序中选择它。

1. 在左侧导航中选择&#x200B;**[!UICONTROL 角色]**，然后选择&#x200B;**[!UICONTROL 创建角色]**。

1. 在&#x200B;_[!UICONTROL 创建新角色]_&#x200B;对话框中，输入角色的名称（如&#x200B;_标准用户_）和描述（可选）。

1. 单击&#x200B;**[!UICONTROL 确认]**。

1. 选择您的沙箱。

1. 添加配置文件权限：

   * 在左侧的&#x200B;_[!UICONTROL 资源]_&#x200B;列表中，找到&#x200B;**[!UICONTROL 配置文件管理]**&#x200B;项目，然后单击加号(**+**)图标以添加该属性。

   * 对于属性，添加以下权限：
      * [!UICONTROL 查看区段]
      * [!UICONTROL 管理区段]
      * [!UICONTROL 查看配置文件]
      * [!UICONTROL 管理配置文件]
      * [!UICONTROL 查看B2B配置文件]
      * [!UICONTROL 管理B2B配置文件]

1. 单击右上方的&#x200B;**[!UICONTROL 保存]**。

1. 选择&#x200B;**[!UICONTROL 用户组]** > **[!UICONTROL 添加组]**。

1. 选中您之前在Admin Console中创建的用户组旁边的复选框。

1. 单击&#x200B;**[!UICONTROL 保存]**。

## 在Admin Console中添加用户

>[!NOTE]
>
>这些步骤只能由Admin Console系统管理员或产品管理员执行。

1. 转到[https://adminconsole.adobe.com](https://adminconsole.adobe.com)。

1. 单击&#x200B;**[!UICONTROL 添加用户]**。

1. 添加每个用户：

   * 输入用户的电子邮件地址、名字和姓氏。
   * 单击[!UICONTROL 用户组]。
   * 选择您之前创建的用户组。

1. 单击&#x200B;**[!UICONTROL 应用]**。

1. 单击&#x200B;**[!UICONTROL 保存]**。