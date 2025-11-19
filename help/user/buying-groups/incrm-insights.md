---
title: In-CRM Insights
description: 直接在Salesforce中访问Journey Optimizer B2B edition购买团体。 销售团队成员可以使用In-CRM Insights查看参与数据并识别销售机会。
feature: Sales Insights, Buying Groups
role: User
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# In-CRM Insights

In-CRM Insights是一个集成到Salesforce中的基于Web的应用程序，它允许您直接在Salesforce中访问Journey Optimizer B2B edition购买团体。 它使您能够发现提高参与度和销售潜力的机会。

In-CRM Insights应用程序在[Marketo Sales Insights包](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/marketo-sales-insight/msi-for-salesforce/installation/install-marketo-sales-insight-package-in-salesforce-appexchange)中可用。

## 权限

要访问该应用程序，用户必须具有角色中的成员资格，该角色具有&#x200B;**Sales Insights:View Sales Insights**&#x200B;权限。

如果要将用户组限制为InCRM-Insights，请使用以下准则专门为InCRM-Insights创建自定义角色：

* 创建仅具有&#x200B;**Sales Insights:View Sales Insights**&#x200B;权限集的自定义角色。
* 创建新的用户组，而不添加任何产品配置文件。
* 创建另一个用户组并添加AEP产品配置文件，或将现有AEP配置文件添加到您刚刚创建的用户组。
* 将新用户组分配给新角色，并将新用户添加到新用户组。

## 使用In-CRM Insights

In-CRM Insights应用程序可通过应用程序启动程序在Salesforce中使用。

1. 单击Salesforce中的应用程序启动器。
1. 选择或搜索`Journey Optimizer B2B Edition`。
1. 在显示的选项卡中，使用您的Adobe凭据登录。
1. 选择一个托管您的帐户历程的沙盒。

您的购买组已加载并可用。 数据通过In-CRM Insights为只读。

>[!NOTE]
>
>需要具有[B2B销售用户](../admin/user-management.md#b2b-built-in-roles)产品角色的成员资格才能访问In-CRM Insights。

选择购买群组后，您可以浏览[群组详细信息](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#)，就像在Journey Optimizer B2B edition中一样。
