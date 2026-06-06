---
title: 电子邮件重复数据删除
description: 了解如何在帐户历程中使用电子邮件重复数据删除，以防止将同一电子邮件多次发送到同一电子邮件地址。
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 电子邮件、重复数据删除、历程、复制
exl-id: 93107acd-1cb2-4316-acfc-e32ab1e065ae
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: 2026-03-30T22:08:16.582Z
TQID: https://experienceleague.adobe.com/aWKXaC6x4Izeh81A6Fpy-Nrf18fHgnq6jUc-82ohErs
source-git-commit: 2c6aafd07cf033df8801621f7e5275dbeeb2768e
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 1%

---

# 电子邮件重复数据删除

要确保同一电子邮件不会在历程中多次发送到同一电子邮件地址，请在帐户历程中使用电子邮件重复数据删除。 启用此功能时，将阻止重复的电子邮件地址，直到使用该电子邮件地址的第一条记录完成历程。 帐户完成历程后，作为进入历程的新帐户的一部分，人员有资格再次接收电子邮件。

## 何时使用电子邮件重复数据删除

在启用电子邮件重复数据删除时，需要考虑以下几种主要情况：

* **电子邮件未在Real-Time CDP中用作身份** — 同一电子邮件地址可能会出现在多个人员配置文件中。 如果这些重复的用户档案符合同一历程的条件，并且您想要阻止多次发送电子邮件，请启用此功能。

* **与多个帐户关联的单个人员** — 如果您的[!DNL Real-Time CDP]数据模型将单个人员与多个帐户关联，请启用此功能以避免当具有相同电子邮件地址的多个用户档案符合同一历程的资格时，发送同一电子邮件两次。

>[!NOTE]
>
>电子邮件去重适用于历程级别。 如果具有相同电子邮件地址的人员符合不同历程的资格，则他们仍可以接收来自每个历程的电子邮件。

## 为历程启用电子邮件重复数据删除

要为帐户历程启用电子邮件重复数据删除，请执行以下操作：

1. 打开帐户历程。

1. 单击&#x200B;**[!UICONTROL 更多]** (**...**) 位于历程工作区的右上角。

   ![扩展了“更多”菜单的历程工作区，其中显示了“电子邮件重复数据删除”选项](./assets/email-deduplication-more-menu.png){width="450"}

1. 选择&#x200B;**[!UICONTROL 电子邮件重复数据删除]**。

1. 在对话框中，选中&#x200B;**[!UICONTROL 电子邮件重复数据删除]**&#x200B;复选框。

   ![启用了切换的电子邮件去重对话框](./assets/email-deduplication-dialog.png){width="400"}

1. 单击&#x200B;**[!UICONTROL 保存]**。

启用电子邮件去重后，历程会在发送电子邮件之前检查每个电子邮件地址。 如果具有相同电子邮件地址的记录已进入该历程节点，则新条目将被阻止，直到第一个记录完成历程。
