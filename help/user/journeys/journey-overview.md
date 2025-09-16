---
title: 帐户历程
description: 通过帐户历程简化需求开发——在 Journey Optimizer B2B Edition 中创建、发布、管理购买群组参与度，覆盖电子邮件、短信及线下活动。
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: a8c2e8e96c5a70032ceba3f0630d1f6c5ae01726
workflow-type: ht
source-wordcount: '1032'
ht-degree: 100%

---


# 帐户历程

通过帐户历程，您可以简化需求生成和购买群组鉴定，并为您获取客户、追加销售/交叉销售和保留计划带来更多合格的需求。通过电子邮件、短信、活动等自动参与方式，为每个购买群组和购买群组成员定制历程。

定义销售驱动型参与（包括电子邮件、短信和更多内部帐户历程），协调每个购买群组成员的入站营销和出站销售活动。

![视频](../../assets/do-not-localize/icon-video.svg){width="30"} [观看概述视频](#overview-video)

## 开始使用历程

如要开始使用帐户历程：

1. [创建历程](./create-publish-journey.md#create-an-account-journey)。
1. 在历程图中[添加节点](./create-publish-journey.md#add-a-node)，然后[定义历程流程图](./create-publish-journey.md#add-and-delete-a-path)。
1. [发布历程](./create-publish-journey.md#publish-an-account-journey)。

## 访问并浏览帐户历程

在左侧导航栏中展开&#x200B;**[!UICONTROL 帐户管理]**，然后单击&#x200B;**[!UICONTROL 帐户历程]**。

在列表顶部的&#x200B;_搜索_&#x200B;工具中输入文本，按名称筛选所显示的列表。

![筛选帐户历程列表](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

_[!UICONTROL 帐户历程]_&#x200B;列表页面包括以下几列：

* [!UICONTROL 名称]（单击名称可打开历程进行编辑）
* [!UICONTROL 状态]
* [!UICONTROL 描述]
* [!UICONTROL 创建者]
* [!UICONTROL 上次更新时间]
* [!UICONTROL 上次更新者]
* [!UICONTROL 发布日期]
* [!UICONTROL 发布者]

您可以通过单击列标题按&#x200B;_[!UICONTROL 状态]_&#x200B;对列表进行排序。

您可以通过单击右上角的&#x200B;_自定义表格_（![自定义表格](../assets/do-not-localize/icon-column-settings.svg)）图标来自定义表格中显示的列。选择或清除对话框中的复选框，然后单击&#x200B;**[!UICONTROL 应用]**。

![选择要在帐户历程列表中显示的列](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## 帐户历程剖析

单击&#x200B;_[!UICONTROL 帐户历程]_&#x200B;列表中的名称（显示为链接），查看详细信息、进行更改并执行操作。

![帐户历程工作区](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

每个帐户历程图的标头包括：

* 历程名称
* 历程名称（![编辑图标](../assets/do-not-localize/icon-edit.svg) _编辑_&#x200B;图标）的编辑工具
* 历程的状态

历程的状态会根据您应用的操作而改变。根据历程的状态，标头右侧的某些操作可用/不可用。

| 状态 | 描述 | 可用操作 |
| ------ | ----------- | ----------------- |
| _**草稿**_ | 可编辑的未发布历程。 | <li>[发布](./create-publish-journey.md#publish-an-account-journey)<li>[重复](#duplicate-journey) <li>[删除](#delete-journey) |
| _**实时**_ | 历程发布后，历程状态就从草稿变为实时。在这种状态下，历程无法再编辑。 | <li>[重复](#duplicate-journey)<li>[对新条目关闭](#close-to-new-entries) <li>[中止](#abort-journey) |
| _**对新条目关闭**_ | 单击顶部导航中的[!UICONTROL 对新条目关闭]，历程状态从&#x200B;_实时_&#x200B;变为&#x200B;_对新条目关闭_。 | <li>[重复](#duplicate-journey) <li>[中止](#abort-journey) |
| _**已中止**_ | 历程中止后，历程状态从&#x200B;_实时_&#x200B;或&#x200B;_对新条目关闭_&#x200B;改变。已中止历程无法重新开始。 | <li>[重复](#duplicate-journey) <li>[删除](#delete-journey) |
| _**已完成**_ | 历程中的所有帐户都完成该历程后，状态将从&#x200B;_实时_&#x200B;或&#x200B;_对新条目关闭_&#x200B;变为&#x200B;_已完成_。 | <li>[重复](#duplicate-journey) <li>[删除](#delete-journey) |

## 管理历程

_帐户历程_&#x200B;列表中包含您的 Journey Optimizer B2B Edition 实例中的所有历程。

### 中止历程

如果中止（停止）一个正在进行或已计划的历程，该历程中的帐户会立即停止进度，该历程无法再被进入。已中止历程无法重新开始。

>[!IMPORTANT]
>
>如果这个帐户历程被用在从具有&#x200B;_将帐户添加到（其他）历程_&#x200B;操作的&#x200B;_执行操作_&#x200B;节点开始的另一个历程中，中止这个历程就会阻止那个历程中的此操作。

1. 单击历程名称将其打开。

1. 单击右上角的&#x200B;**[!UICONTROL 更多...]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 中止]**。

   ![单击右上角的“更多”](./assets/account-journey-live-more-menu.png){width="450"}

1. 在确认对话框中单击&#x200B;**[!UICONTROL 中止]**。

### 对新条目关闭

如果关闭一个实时历程，当前在该历程中的帐户将继续其在历程中的路径，该历程无法再被进入。已关闭历程无法重新开始。您可以重复一个已关闭的历程。

>[!IMPORTANT]
>
>如果这个帐户历程被用在从具有&#x200B;_将帐户添加到（其他）历程_&#x200B;操作的&#x200B;_执行操作_&#x200B;节点开始的另一个历程中，对新条目关闭会阻止那个历程中的此操作。

1. 单击历程名称将其打开。

1. 单击右上角的&#x200B;**[!UICONTROL 更多...]**&#x200B;菜单，然后选择 **[!UICONTROL 对新条目关闭]**。

1. 在确认对话框中单击&#x200B;**[!UICONTROL 对新条目关闭]**。

### 复制历程

复制操作类似于克隆功能，但复制的历程不包含任何已创建的历程内容资产。您可以复制帐户历程的详细信息，或者仅复制流程和路径结构的简单&#x200B;_框架_。

1. 单击历程名称旁边的&#x200B;_更多_&#x200B;图标 (**...**)，然后选择&#x200B;**[!UICONTROL 复制]**。

   ![单击 ... 图标，然后选择“复制”](./assets/account-journeys-list-more-menu.png){width="450"}

   根据帐户历程的状态，您还可以从历程详细信息或历程图访问复制操作：

   * 对于草稿历程，请单击右上角的&#x200B;**[!UICONTROL 更多...]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 复制]**。

   * 对于所有其他历程状态，请单击右上角的&#x200B;**[!UICONTROL 复制]**。

     ![单击右上角的“复制”](./assets/account-journey-duplicate-button.png){width="450"}

1. 在&#x200B;_复制历程_&#x200B;对话框中，设置新历程的&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

   在默认情况下，该对话框会使用所复制历程的名称加上 __copy_。根据需要为历程输入另一个唯一名称。

   ![复制历程对话框](./assets/account-journey-duplicate-dialog.png){width="400"}

1. 选择复制&#x200B;**[!UICONTROL 类型]**：

   * **[!UICONTROL 部分内容复制]** - 使用此类型来复制历程中的所有内容，但不包括任何已创建的电子邮件或 SMS 消息。引用 Marketo Engage 电子邮件或 SMS 消息的节点会被完整保留。

   * **[!UICONTROL 复制但不包含详细信息]** - 使用此类型仅复制节点结构和路径。所有节点设置和路径条件均未定义（默认），以便您可以重复使用具有不同受众、操作和路径分段设置的基本流程。所有&#x200B;_等待_&#x200B;节点默认设置为五天。

1. 单击&#x200B;**[!UICONTROL 复制]**。

   复制的帐户历程会在历程图中打开，您可以在其中设置详细信息并根据需要创建历程内容。

### 删除历程

使用删除操作来永久删除历程。您不能删除正在进行或已计划的历程。

1. 单击历程名称旁边的&#x200B;_更多_&#x200B;图标 (**...**)，然后选择&#x200B;**[!UICONTROL 删除]**。

   根据帐户历程的状态，您还可以从历程详细信息或历程图访问删除操作：

   * 对于草稿历程，请单击右上角的&#x200B;**[!UICONTROL 更多...]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 删除]**。

   * 对于其他历程状态，例如&#x200B;_已完成_&#x200B;或&#x200B;_已中止_，请单击右上角的&#x200B;**[!UICONTROL 删除]**。

1. 在确认对话框中单击&#x200B;**[!UICONTROL 删除]**。

## 概述视频

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
