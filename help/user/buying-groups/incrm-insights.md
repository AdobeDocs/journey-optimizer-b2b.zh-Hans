---
title: In-CRM Insights
description: 直接在CRM中访问Journey Optimizer B2B edition购买群组。 销售团队成员可以使用In-CRM Insights查看参与数据并识别销售机会。
feature: Sales Insights, Buying Groups
role: User
exl-id: c55a1fce-2ddc-481b-9f60-5e67a4bf9633
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: afadf741-c5fe-42cd-8013-23bb6ff2d1bcid: fc1ff3b2-6614-41ad-a113-de48597598fdid: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2: id: fe583b80-65a2-48c2-b4e1-9ea8fbac0a8a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: '2026-03-30T21:40:22.011Z'
source-git-commit: ff337a5f215daee1ea6dbe8d6b643087ac3324e2
workflow-type: tm+mt
source-wordcount: 483
ht-degree: 1%

---

# In-CRM Insights

[!DNL In-CRM Insights]是一个集成到Salesforce和Microsoft Dynamics 365中的基于Web的应用程序，它允许您直接在CRM中访问[!DNL Journey Optimizer B2B Edition]购买团体。 它汇集了销售数据源，使得更容易发现提高参与度和销售潜力的机会。

## 安装

安装过程包括：

* 设置用户权限和组
* 安装软件包
* 通过您的CRM登录

### 设置权限

安装软件的用户必须有权安装Salesforce软件包。

要访问该应用程序，用户必须具有角色中的成员资格，该角色具有&#x200B;**Sales Insights:View Sales Insights**&#x200B;权限。

如果要将用户限制为仅[!DNL In-CRM Insights]：

1. 创建一个[自定义角色](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/buying-groups/default-custom-roles#create-a-custom-role)并为其分配&#x200B;**销售分析：查看销售分析**&#x200B;权限。
1. 创建新的[用户组](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management#create-user-group)。
1. 将Experience Platform产品配置文件添加到组。

### 安装包

要安装In-CRM Insights包，请按照Salesforce或Microsoft Dynamics中的步骤操作。

#### Salesforce

1. 下载[In-CRM Insights安装程序包](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce)。
1. 登录后，您将被重定向到软件包安装页面。
1. 选择&#x200B;**[!UICONTROL 为所有用户安装]**&#x200B;选项，然后单击&#x200B;**[!UICONTROL 安装]**。

   ![安装In-CRM Insights包](assets/incrm-install-sf.png){width=500}

1. 在对话框中批准第三方访问，然后单击&#x200B;**[!UICONTROL 继续]**。
1. 安装完成后，单击&#x200B;**[!UICONTROL 完成]**。

   它现在列在&#x200B;**已安装的包**&#x200B;页面上，并且&#x200B;**Journey Optimizer B2B edition**&#x200B;列在应用程序启动程序中。

   在Salesforce中设置的![In-CRM Insights](assets/in-crm-install-sf-done.png){width=800 zoomable="yes"}

#### MS Dynamics

1. 下载[In-CRM Insights安装程序包](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics)。
1. 转到[Power Apps门户](https://make.powerapps.com/){target=_blank}。
1. 登录后，选择包的环境，然后从左侧菜单中导航到&#x200B;**[!UICONTROL 解决方案]**。
1. 单击&#x200B;**[!UICONTROL 导入解决方案]**。
1. 浏览并上传安装程序包，然后单击&#x200B;**[!UICONTROL 下一步]**。
1. 验证包详细信息，然后单击&#x200B;**[!UICONTROL 下一步]**。
1. 在&#x200B;_环境变量_&#x200B;下，验证该值是否设置为`prod`（不更改该值），然后单击&#x200B;**[!UICONTROL 导入]**。
1. 安装完成后，左侧导航栏上会显示&#x200B;**[!UICONTROL Journey Optimizer B2B edition]** > **[!UICONTROL 购买群组]**。

   Microsoft Dynamics中提供的![In-CRM Insights](assets/incrm-ms-install-done.png){width=800 zoomable="yes"}

## 查看您的购买组

按照提示登录Adobe帐户。 您的购买组已加载并可供查看。

选择购买组后，您可以浏览[组详细信息](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#)。 这与Journey Optimizer B2B edition中显示的数据和分析相同，但数据通过[!DNL In-CRM Insights]是只读的。
