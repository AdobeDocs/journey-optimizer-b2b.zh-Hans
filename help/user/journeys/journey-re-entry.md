---
title: 历程重新进入
description: 控制帐户或人员重新进入同一帐户或人员历程的时间和频率。
feature: Account Journeys
role: User
level: Intermediate
exl-id: e5153125-6d5b-4835-bd19-c9b7ce67e46a
autotag-review: '2026-08-14T19:11:15.391Z'
TQID: 'https://experienceleague.adobe.com/BabVdaLaAwER8tEQLOAjChwyy4WI2Cle19-Uu-varIc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: 07717d3ba2d67a61e3dcfa4693e2ee2e151e78da
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 1%
---
# 历程重新进入

为历程启用重新进入后，您可以控制帐户或人员重新进入同一历程的时间和频率。 使用重新进入设置来设置标准、限制和等待时间，以便帐户或人员需要以可控方式获得历程的资格。

当以下项为true时，帐户或人员需要符合历程的资格：

* 帐户或人员处于历程允许的重新进入次数之内。
* 帐户或人员已达到等待时间阈值（重新获得资格前等待的最短时间）。
* 帐户或人员当前不在历程中。

## 为历程启用重新进入

当历程处于&#x200B;_草稿_&#x200B;状态时，您可以启用重新进入并更改重新进入设置。

>[!BEGINTABS]

>[!TAB 帐户历程]

1. 打开草稿帐户历程。

1. 单击右上方的&#x200B;**[!UICONTROL 更多……]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 重新进入]**。

   ![单击帐户历程右上角的“更多”](./assets/account-journey-draft-more-menu.png){width="450"}

1. 在&#x200B;_[!UICONTROL 历程重新进入]_&#x200B;对话框中，切换&#x200B;**[!UICONTROL 启用重新进入]**&#x200B;选项。

   启用该功能后，将显示计时、延迟和限制选项。

   ![已启用功能的帐户历程的历程重新进入对话框](./assets/journey-re-entry-dialog-enabled.png){width="450"}

1. 对于&#x200B;**[!UICONTROL 重新进入计时]**，请选择等待的计算方式：

   * **[!UICONTROL 从历程结束时等待]** — 等待期从帐户退出或完成历程时开始。 例如，“在帐户完成历程30天后，可以重新进入。”

   * **[!UICONTROL 从历程开始等待]** — 等待时间基于帐户首次进入历程的时间。 例如，“在帐户开始历程后30天，它可以重新进入。”

1. 设置&#x200B;**[!UICONTROL 重新进入延迟]**，即等待持续时间（小时或天）。

   此设置确定帐户在退出或启动历程后必须等待多长时间，才能重新进入。

1. 要定义允许帐户进入历程的最大次数，请设置&#x200B;**[!UICONTROL 进入限制]**。

   当帐户达到限制时，在重置限制或使用新限制重新发布历程之前，该帐户不再具有进入资格。

   此限制适用于该历程的每个帐户。

1. 单击&#x200B;**[!UICONTROL 保存]**。

>[!TAB 人员历程]

1. 打开草稿人员历程。

1. 单击右上方的&#x200B;**[!UICONTROL 更多……]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 重新进入设置]**。

   ![单击人员历程右上角的“更多”](./assets/person-journey-draft-more-menu.png){width="450"}

1. 在&#x200B;_[!UICONTROL 历程重新进入]_&#x200B;对话框中，切换&#x200B;**[!UICONTROL 启用重新进入]**&#x200B;选项。

   启用该功能后，将显示计时、延迟和限制选项。

   ![已启用功能的人员旅程的历程重新进入对话框](./assets/person-journey-re-entry-dialog.png){width="450"}

1. 对于&#x200B;**[!UICONTROL 重新进入计时]**，请选择等待的计算方式：

   * **[!UICONTROL 从历程结束时等待]** — 等待期从人员退出或完成历程时开始。 例如，“在人员完成历程30天后，他们可以重新进入。”

   * **[!UICONTROL 从历程开始等待]** — 等待时间基于人员首次进入历程的时间。 例如，“在人员开始旅程后30天，他们可以重新进入。”

1. 设置&#x200B;**[!UICONTROL 重新进入延迟]**，即等待持续时间（小时或天）。

   该设置确定人员退出或开始历程后必须等待多久才能重新进入。

1. 要定义允许人员进入历程的最大次数，请设置&#x200B;**[!UICONTROL 进入限制]**。

   当人员达到限制时，在重置限制或使用新限制重新发布历程之前，他们不再具有进入资格。

   此限制适用于该历程的每个人。

1. 单击&#x200B;**[!UICONTROL 保存]**。

>[!ENDTABS]

## 进展和活动

对于已发布的帐户或人员历程，历程画布显示历程节点的[进度](./journeys-overview.md#review-account-progression)。 每个节点会显示到达该节点的帐户或人员数量，对于实时历程，会显示当前在该节点处的数量。 每次帐户或人员重新进入历程时，它都计为一个不同的条目。

<!-- 
You can see how many times accounts have entered the journey. ?? 

When you drill in to [account details](../accounts/account-details.md), the account activity shows each time the account entered the journey. It includes explicit activity and a recurrence count so that you can see re-entries clearly.
-->
