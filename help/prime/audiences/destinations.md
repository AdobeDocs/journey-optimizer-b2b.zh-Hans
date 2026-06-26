---
title: 目标
description: 了解如何在Journey Optimizer B2B Prime中连接目标和激活静态人员列表，以将受众数据导出到广告、电子邮件和其他营销平台。
autotag-review: '2026-06-17T18:30:02.442Z'
TQID: 'https://experienceleague.adobe.com/xO1p-VvIfv1KB77g0l2-fFRHQ0w2hy97vnG1QHpMw8c'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: aed878b8-11d0-487c-828b-d23b2051ec37id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: af10a912422f1736fdc86e0609aee76f5d4daa46
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 2%

---

# 目标

目标是预建的集成，可让您将人员列表数据从[!DNL Adobe Journey Optimizer B2B Prime]导出到外部营销平台，如广告网络、电子邮件服务提供商和CRM系统。 在[!DNL Journey Optimizer B2B Prime]中，您将[静态人员列表](./people-lists.md#static-list)（由Marketo Engage人员记录组成）激活到目标，以便这些受众可用于在下游渠道中进行定位和参与。

<!-- 
Does not align w/AEP info for Beta

Activating a static list to a destination follows a three-step process:

1. **Connect** — Authenticate and configure a connection to a destination platform.
1. **Map** — Select the static list and map its people attributes to the fields required by the destination.
1. **Schedule** — Define when and how often the list data is exported to the destination.

Destination activations reflect the membership state of the static list at the time of each synch.

## Destination types {#destination-types}

[!DNL Journey Optimizer B2B Prime] supports the following destination types for activating static people lists:

| Type | Description |
|--- |--- |
| Streaming | Real-time API-based connections that push audience membership updates to the destination as they occur. |
| File-based (batch) | Scheduled exports that deliver audience data as structured files to cloud storage or SFTP locations, which the destination platform then ingests. |

-->

## 连接目标 {#connect-destination}

1. 在左侧导航中，展开&#x200B;**[!UICONTROL 连接]**&#x200B;并选择&#x200B;**[!UICONTROL 目标]**。

1. 在&#x200B;_[!UICONTROL 目录]_&#x200B;选项卡中，找到外部目标类型连接器。

   >[!TIP]
   >
   >通过在搜索框中输入名称（如`LinkedIn`）可以快速找到连接器。

   ![访问可用的连接器类型](./assets/destinations-catalog.png){width="800" zoomable="yes"}

1. 在连接器卡中，单击&#x200B;**[!UICONTROL 配置新目标]**。

1. 选择&#x200B;**[!UICONTROL 新帐户]**&#x200B;并输入帐户凭据。

   ![连接新的目标帐户](./assets/destinations-configure-new.png){width="500"}

1. 单击&#x200B;**[!UICONTROL 连接到目标]**。

   >[!IMPORTANT]
   >
   >此时，**不**&#x200B;输入&#x200B;_[!UICONTROL 目标详细信息]_。 只需要连接。

1. 查看数据治理和营销操作设置，然后单击&#x200B;**[!UICONTROL 保存]**。

连接的目标显示在&#x200B;_[!UICONTROL 浏览]_&#x200B;选项卡的列表中，可用于静态列表激活。

## 将静态列表激活到目标 {#activate}

>[!NOTE]
>
>只能将[静态人员列表](./people-lists.md#static-list)激活到[!DNL Journey Optimizer B2B Prime]中的目标。 [动态列表](./people-lists.md#dynamic-lists)不符合目标激活的条件。

1. 在左侧导航栏中，展开&#x200B;**[!UICONTROL 营销管理]**。

1. 在&#x200B;**[!UICONTROL 营销]**&#x200B;资源列表的右侧，选择&#x200B;**[!UICONTROL 人员列表]**。

   ![访问联系人列表以管理您的受众](./assets/people-lists.png){width="800" zoomable="yes"}

1. 选择&#x200B;**[!UICONTROL 静态列表]**&#x200B;选项卡。

1. 找到要激活到目标的静态列表。

1. 单击静态列表名称旁边的&#x200B;_激活_ （![激活图标](../../assets/do-not-localize/icon-falco-activate-dest.svg) ）图标。

1. 选中已配置的目标连接的复选框。

   ![配置的目标可用于激活](./assets/static-list-activate-destination-select.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 保存]**。

<!--

This method not working for Beta

1. On the _[!UICONTROL Browse]_ tab, locate the destination you want to use for the activation and click the name to open it.

1. Select the **[!UICONTROL Activation data]** tab.

1. Click **[!UICONTROL Activate people lists]**.

1. Select the static people list you want to export and click **[!UICONTROL Next]**.

1. Map the people list attributes to the required fields of the destination schema and click **[!UICONTROL Next]**.

1. Set the export schedule:

   * **[!UICONTROL Frequency]** — Choose how often the list is exported (for example, daily or weekly).
   * **[!UICONTROL Start date]** — Set when the first export should run.

1. Review the activation summary and click **[!UICONTROL Finish]**.

The activation is created and the static list data is exported to the destination according to the defined schedule.

-->
