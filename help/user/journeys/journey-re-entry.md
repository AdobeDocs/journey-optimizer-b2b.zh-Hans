---
title: 历程重新进入
description: 控制帐户重新进入同一帐户历程的时间和频率。
feature: Account Journeys
role: User
level: Intermediate
exl-id: e5153125-6d5b-4835-bd19-c9b7ce67e46a
source-git-commit: 5adf65f3c48c17f73e4897fb9ce027631bf196a7
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 1%

---

# 历程重新进入

_仅限帐户历程_

为帐户历程启用重新进入后，您可以控制帐户何时以及多久重新进入一次同一历程。 使用重新进入设置来设置标准、限制和等待时间，以便帐户需要以可控方式完成历程。

当以下项为true时，帐户可以重新符合历程的资格：

* 帐户在历程允许的重新进入次数之内。
* 帐户已达到等待时间阈值（重新认证前等待的最短时间）。
* 帐户当前不在历程中。

## 为帐户历程启用重新登录

当历程处于&#x200B;_草稿_&#x200B;状态时，您可以启用重新进入并更改重新进入设置。

1. 打开草稿帐户历程。

1. 单击右上方的&#x200B;**[!UICONTROL 更多……]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 重新进入]**。

   ![单击右上角的“更多”](./assets/account-journey-draft-more-menu.png){width="450"}

1. 在&#x200B;_[!UICONTROL 历程重新进入]_&#x200B;对话框中，切换&#x200B;**[!UICONTROL 启用重新进入]**&#x200B;选项。

   启用该功能后，将显示计时、延迟和限制选项。

   ![已启用功能的历程重新进入对话框](./assets/journey-re-entry-dialog-enabled.png){width="450"}

1. 对于&#x200B;**[!UICONTROL 重新进入计时]**，请选择等待的计算方式：

   * **[!UICONTROL 从历程结束时等待]** — 等待期从帐户退出或完成历程时开始。 例如，“在帐户完成历程30天后，他们可以重新进入。”

   * **[!UICONTROL 从历程开始等待]** — 等待时间基于帐户首次进入历程的时间。 例如，“在帐户开始旅程后30天，他们可以重新进入。”

1. 设置&#x200B;**[!UICONTROL 重新进入延迟]**，即等待持续时间（小时或天）。

   该设置确定帐户在退出或开始历程后必须等待多久才能重新进入。

1. 设置&#x200B;**[!UICONTROL 进入限制]**&#x200B;以定义允许帐户进入历程的最大次数。

   当帐户达到限制时，在重置限制或使用新限制重新发布历程之前，该帐户不再具有进入资格。

   此限制适用于该历程的每个帐户。

1. 单击&#x200B;**[!UICONTROL 保存]**。

## 帐户进展和活动

对于已发布的帐户历程，历程图显示历程节点的[帐户进度](./journeys-overview.md#review-account-progression)。 映射中的每个节点会显示到达该节点的帐户数，对于实时历程，会显示当前在该节点的帐户数。 每次帐户重新进入历程时，它都计为一个不同的条目。
<!-- You can see how many times accounts have entered the journey. ?? -->

当您深入到[帐户详细信息](../accounts/account-details.md)时，帐户活动会在每次帐户进入历程时显示。 它包括显式活动和重复计数，以便您可以清楚地看到重复条目。
