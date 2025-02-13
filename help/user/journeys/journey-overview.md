---
title: 帐户历程
description: 了解帐户历程以及如何创建和管理它们。
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---


# 帐户历程

使用电子邮件、短信、活动等自动参与功能，构建和执行为每个购买组和购买组成员量身定制的历程。 WIth客户历程您可以简化需求生成和购买团体资格鉴定，并推动对您的收购、追加销售/交叉销售和保留计划的更多合格需求。

定义包括电子邮件、短信和更多内部帐户历程的销售驱动型参与，以协调入站营销与每个购买组成员的出站销售活动。

![视频](../../assets/do-not-localize/icon-video.svg){width="30"} [观看概述视频](#overview-video)

## 访问和浏览帐户历程

1. 在Adobe Experience Platform主页中，单击Adobe Journey Optimizer B2B edition。

1. 在左侧导航中，单击&#x200B;**[!UICONTROL 帐户历程]**。

   ![访问帐户历程](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   显示的历程页面包含以下列：

   * [!UICONTROL 名称] （单击该名称可打开帐户历程进行编辑）
   * [!UICONTROL 状态]
   * [!UICONTROL 描述]
   * [!UICONTROL 创建者]
   * [!UICONTROL 上次更新于]
   * [!UICONTROL 上次更新者]
   * [!UICONTROL 发布于]
   * [!UICONTROL 发布者]

此表包括按名称和创建者进行搜索的功能。 排序当前不可用。

您可以通过单击右上角的&#x200B;_列_&#x200B;图标并选择或清除复选框来自定义显示的表。

![选择要显示在帐户历程列表中的列](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## 帐户历程剖析

单击&#x200B;_[!UICONTROL 帐户历程]_&#x200B;列表中的名称（显示为链接）以查看详细信息、进行更改并采取操作。

![帐户历程工作区](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

每个帐户历程的编辑器标题包括：

* 历程名称
* 能够编辑名称（_编辑_&#x200B;图标）
* 历程的状态

标头中提供了以下操作：

* **发布** — 如果没有阻止程序错误，则可以发布历程。 发布后，历程状态将更改为&#x200B;_实时_。 如果历程出现错误，按钮将灰显，并包含内容信息： `Resolve errors before publishing`。
* **复制** — 此操作类似于克隆函数，但复制的历程不包含任何资源。
* **关闭新条目** — 如果您关闭历程，则当前在历程中的帐户将继续其在历程中的路径，并且不会发生进一步的历程进入。 无法重新启动已关闭的历程。 您可以复制已关闭的历程。
* **中止** — 如果停止历程，则历程中的帐户将立即停止进度，并且不会发生进一步的历程进入。 无法重新启动停止的历程。 如果您阻止新进入而不阻止人们的进步，请考虑改为关闭历程。
* **删除** — 此操作将永久删除历程。

历程的状态会根据您应用的操作而更改。 根据历程的状态，某些操作在标题中不可用。

| 状态 | 描述 | 可用操作 |
| ------ | ----------- | ----------------- |
| _**草稿**_ | 可编辑的未发布历程。 | <ul><li>发布</li><li>复制 </li><li>Delete </li></ul> |
| _**实时**_ | 历程发布后，历程状态从草稿更改为实时。 在此状态下，它不再可编辑。 | <ul><li>复制 </li><li>关闭新条目 </li><li>中止 </li></ul> |
| _**对新条目关闭**_ | 在顶部导航中单击[!UICONTROL 关闭新条目]时，历程状态将从&#x200B;_实时_&#x200B;更改为&#x200B;_已关闭新条目_。 | <ul><li>复制 </li><li>中止 </li></ul> |
| _**已中止**_ | 当您中止历程时，历程状态从&#x200B;_实时_&#x200B;或&#x200B;_已关闭更改为新条目_。 无法重新启动已中止的历程。 | <ul><li>复制 </li><li>Delete </li></ul> |
| _**已完成**_ | 当历程中的所有帐户完成历程时，状态将从实时或已关闭更改为新条目，更改为已完成。 | <ul><li>复制 </li><li>Delete </li></ul> |

## 历程入门

要开始使用帐户历程，请执行以下操作：

1. [创建历程](./create-publish-journey.md#create-an-account-journey)。
1. [添加节点](./create-publish-journey.md#add-a-node)和[在历程图中定义历程流](./create-publish-journey.md#add-and-delete-a-path)。
1. [发布历程](./create-publish-journey.md#publish-an-account-journey)。

## 概述视频

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
