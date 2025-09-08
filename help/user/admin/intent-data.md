---
title: 目的数据
description: 在Journey Optimizer B2B edition中，通过关键词映射配置意图数据以预测客户兴趣和用于基于账户的营销的购买信号。
feature: Setup, Intent, Account Insights
roles: Admin
exl-id: c7f9f6fe-2275-42a4-af80-b5c3d1a82837
source-git-commit: 9ed2d2a36dbdaf39c107a18632d951003c86197b
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 意图数据

在Journey Optimizer B2B edition中，意图检测模型根据商机活动预测具有足够高置信度的感兴趣解决方案/产品。 它还利用了其他帐户共同成员的活动，以及标记的内容。 个人的意图可以解释为对产品感兴趣的可能性。

* 意图级别 — 在已知潜在客户、客户和购买组级别上可用。
* 意图信号类型 — 关键字、产品和解决方案

意图数据用于&#x200B;[_智能仪表板_](../dashboards/intelligent-dashboard.md)、[_帐户详细信息_&#x200B;页](../accounts/account-details.md)、[_购买群组详细信息_&#x200B;页](../buying-groups/buying-group-details.md)和&#x200B;[_个人详细信息_&#x200B;页](../accounts/person-details.md)。

![意图数据可视化图表](../data/assets/intent-data-visualization.png){width="700" zoomable="yes"}

## 准备意图映射数据

要激活此功能，请使用选项卡创建电子表格(如Microsoft Excel文件)以定义意图分类。 整个电子表格作为一个类别上传，该类别可以有多个产品，每个产品可以有多个关键字。 对于要定义的每个类别，请使用以下意图映射电子表格定义：

* 电子表格名称= _类别名称_
* 每个选项卡=您的产品名称
* 每个选项卡包含一列=产品关键字（最多150个）

您可以下载一个Excel文件，用作准备映射数据的模板。 要下载模板，请执行以下操作：

1. 在左侧导航中，选择&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 配置]**。

1. 单击中间面板中的&#x200B;**[!UICONTROL 意图映射]**。

1. 单击&#x200B;**[!UICONTROL 创建类别]**。

1. 在对话框中，单击&#x200B;**[!UICONTROL 下载文件模板]**&#x200B;链接。

   ![意图数据下载模板文件](./assets/intent-data-upload-files.png){width="500"}

1. 单击&#x200B;**[!UICONTROL 取消]**。

   完成后，您可以返回上载准备的文件。

1. 使用模板定义意图映射数据：

   * 重命名文件以反映您的类别名称，例如&#x200B;_Personalization的比例_。
   * 根据您的产品名称重命名每个选项卡，如&#x200B;_Journey Optimizer B2B_、_Marketo Engage_&#x200B;和&#x200B;_Experience Manager_。
   * 为每个选项卡添加产品关键字，如&#x200B;_B2B营销_、_品牌认可_&#x200B;和&#x200B;_潜在客户参与度_。

   ![类别电子表格](./assets/intent-category-spreadsheet.png){width="600" zoomable="yes"}

## 上传类别文件

电子表格准备就绪后，返回到&#x200B;_[!UICONTROL 意图映射]_&#x200B;配置页面并上传文件。

1. 单击&#x200B;**[!UICONTROL 创建类别]**。

1. 将文件拖放到&#x200B;_[!UICONTROL 上载文件]_&#x200B;对话框中，或单击&#x200B;**[!UICONTROL 选择文件]**&#x200B;以在系统上查找并选择该文件。

1. 单击&#x200B;**[!UICONTROL 下一步]**。

   预处理运行对相似关键词进行聚类，提高了意图检测能力，避免了关键词稀释。 一旦完成此预处理，就会显示脉冲通知（根据数据，最长为15分钟）。

   ![脉冲通知](./assets/intent-data-upload-files-pre-process.png){width="500"}

   结果显示在&#x200B;_意图映射_&#x200B;页面中。

   ![上传的意向类别以供审批](./assets/intent-data-category-approve.png){width="600" zoomable="yes"}

## 批准或拒绝类别

查看类别列表并单击&#x200B;**[!UICONTROL 批准]**&#x200B;以激活关键字，以便在智能仪表板、帐户详细信息页面、购买群组详细信息页面和人员详细信息页面中使用。 单击&#x200B;**[!UICONTROL 查看全部]**&#x200B;以显示每个产品的完整列表，或单击&#x200B;**[!UICONTROL 下载]**&#x200B;以Excel文件形式查看完整列表。

如果您不满意该列表，可以单击&#x200B;**[!UICONTROL 删除]**&#x200B;以删除该类别。 然后，您可以调整电子表格文件，然后重新开始上传流程以定义该类别。

>[!IMPORTANT]
>
>在添加其他类别或编辑类别之前，必须批准或拒绝（删除）新类别。

如果添加另一个类别，并且其分类会影响现有类别，则会出现警告。 在决定批准或拒绝类别时，请考虑此影响。 如果产品在多个类别中使用，则所有类别中的产品到关键字映射应该是相同的。

![现有类别影响的警报](./assets/intent-data-category-overlap.png){width="600" zoomable="yes"}
