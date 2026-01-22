---
title: 帐户详细信息
description: 在Journey Optimizer B2B edition中通过AI摘要、意图检测、联系人覆盖范围分析和电子邮件通信查看帐户洞察。
feature: Account Insights
role: User
exl-id: 12be33de-0a43-43d9-90b8-fe4411a50599
source-git-commit: 2a676f3cbeb43616a75fa3fa6eb9106230b9fb40
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 5%

---

# 帐户详细信息

当您在Journey Optimizer B2B edition的任何位置单击帐户名称时，都会显示&#x200B;_帐户详细信息_&#x200B;页面。 本页提供有关帐户的有用信息，包括创作AI摘要。 还有可为与该帐户关联的联系人执行的[操作](#account-actions)。

![访问帐户详细信息](./assets/account-details.png){width="700" zoomable="yes"}

使用&#x200B;**[!UICONTROL 概述]**&#x200B;选项卡查看有关帐户的信息，使用&#x200B;**[!UICONTROL 联系人]**&#x200B;选项卡访问帐户联系人的列表。

## [!UICONTROL 概述]选项卡

帐户详细信息页面包含三个主要部分：

### 帐户概述

![帐户概述](./assets/details-page-account-overview.png){zoomable="yes"}

帐户概述部分包含以下帐户信息：

* 帐户名称
* 帐户中的人数
* 行业
* 打开机会
* 帐户当前正在使用中的最近三次帐户历程（单击历程名称以打开[历程概述](../journeys/journeys-overview.md)）
* 帐户的创作AI摘要，其中包括有关最热门的购买群体的信息。

### 意图数据

在Journey Optimizer B2B edition中，意图检测模型根据帐户联系活动预测具有足够高置信度的感兴趣解决方案/产品。 帐户联系人的意图可以解释为对产品感兴趣的可能性。

{{intent-data-note}}

![意图数据 — 帐户详细信息](./assets/intent-data-panel.png){width="700" zoomable="yes"}

* 意图级别
* 意图信号类型 — 关键字、产品和解决方案


### 联系覆盖范围

![帐户联系人覆盖范围](./assets/details-page-contact-coverage.png){width="800" zoomable="yes"}

_[!UICONTROL 联系人覆盖范围]_&#x200B;部分显示帐户中具有与解决方案兴趣关联的特定角色的联系人的数量。 角色和解决方案兴趣的分配基于购买组角色模板。 单击单元格可显示以下详细信息：

* 描述，采用以下格式： _x个人对z解决方案兴趣具有y角色_
* 列
* 名称
* 帐户
* 作业名称
* 购买群组
* 人员参与度分数
* 上一个活动
* 详细信息

单击左上角的&#x200B;_筛选器_ （![筛选器图标](../assets/do-not-localize/icon-filter.svg)）图标，以使用以下任一属性筛选数据显示：

* 解决方案兴趣
* 时段

### 联系重叠

![帐户联系人重叠](./assets/details-page-contact-overlap.png){width="800" zoomable="yes"}

_[!UICONTROL 联系人重叠]_&#x200B;部分显示来自帐户的联系人，这些联系人由于与多个解决方案兴趣关联而属于多个购买组。 此信息以表格的形式提供，其中包含以下列：

* 名称
* 作业名称
* 帐户
* 解决方案兴趣

单击联系人名称旁边的&#x200B;_信息_ （![信息图标](../assets/do-not-localize/icon-info.svg)）以显示包含以下详细信息的表：

* 购买群组（单击名称以打开[购买群组详细信息](../buying-groups/buying-group-details.md)）
* 角色
* 解决方案兴趣
* 产品意图（如果[已配置](../admin/intent-data.md)）
* 产品

单击左上角的&#x200B;_筛选器_ （![筛选器图标](../assets/do-not-localize/icon-filter.svg)）图标，以使用以下任一属性筛选数据显示：

* 解决方案兴趣
* 角色

## [!UICONTROL 联系人]选项卡

选择&#x200B;**[!UICONTROL 联系人]**&#x200B;选项卡可查看与该帐户相关联的所有人员的列表，该帐户已同步到Experience Platform。 列出的每个联系人包括姓名、电子邮件地址和参与度分数。

![帐户详细信息 — 联系人选项卡](./assets/account-details-contacts-tab.png){width="700" zoomable="yes"}

## 发送电子邮件

您可以将营销人员批准的电子邮件发送给一个或多个选定的联系人（一次最多50个），或发送给该帐户的所有联系人。 可用电子邮件的列表仅限于来自连接的Marketo Engage实例的已批准电子邮件。

>[!BEGINTABS]

>[!TAB 所有帐户联系人]

1. 在&#x200B;_[!UICONTROL 概述]_&#x200B;选项卡中，单击右上方的&#x200B;**[!UICONTROL 发送电子邮件]**。

   ![帐户详细信息 — 选择电子邮件](../accounts/assets/account-details-send-email.png){width="700" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 发送电子邮件]_&#x200B;对话框中，选择Marketo Engage工作区，然后选中要发送的电子邮件的复选框。

   ![选择要发送给购买群成员的电子邮件](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 发送]**。

>[!TAB 选定的联系人]

1. 在&#x200B;_[!UICONTROL 联系人]_&#x200B;选项卡中，选中要接收电子邮件的联系人的复选框。

1. 单击右上角或底部选择栏中的&#x200B;**[!UICONTROL 发送电子邮件]**。

   ![成员选项卡 — 发送电子邮件](../accounts/assets/account-details-send-email-selections.png){width="700" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 发送电子邮件]_&#x200B;对话框中，选择Marketo Engage工作区，然后选中要发送的电子邮件的复选框。

   ![选择要发送给购买群成员的电子邮件](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 发送]**。

>[!ENDTABS]
