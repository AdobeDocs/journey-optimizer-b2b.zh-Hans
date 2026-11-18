---
title: 目标
description: 了解支持的Experience Platform目标以及如何连接目标以在Journey Optimizer B2B Edition中激活静态人员列表。
feature: Audiences, Integrations
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: 734966636b6d2addf014905431fa755f6fe92ee6
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 4%
---

# 目标

目标是预建的集成，可让您将[静态人员列表](./people-lists-static.md)成员和帐户历程受众发送到社交平台。 将静态列表激活到目标可使成员资格保持同步。 向列表添加人员或从列表中删除人员时，会向目标受众相应地添加人员，或从目标受众中相应地删除人员，此外，他们会相应地从受众馈送的任何营销活动中添加人员。

可通过三种方式将人员激活到连接的目标：

* **从静态列表** — 直接从&#x200B;**_[!UICONTROL 人员列表]_**&#x200B;选项卡激活现有的静态列表。 请参阅&#x200B;[_激活到目标_](./people-lists-static.md#static-list-activate)。
* **从帐户历程** — 将&#x200B;**_[!UICONTROL 激活到目标]_**&#x200B;操作节点添加到历程路径，以便符合条件的帐户在到达该节点时激活到目标。 请参阅&#x200B;[_激活目标_](../journeys/action-nodes.md#activate-deactivate-destination)&#x200B;或从中取消激活。
* **来自购买组** — 若要填充购买组中的空角色，您可以激活LinkedIn匹配受众，以定位与购买组参数匹配的潜在客户。 查看与audience_s[&#128279;](../data/linkedin-account-matched-audiences.md#activate-buying-group)匹配的_LinkedIn帐户。

>[!BEGINSHADEBOX]

## 所需的权限 {#required-permissions}

完整目标功能需要以下[!DNL Adobe Experience Platform]权限。

| 类别 | 权限 |
|--- |--- |--- |
| 沙盒 | 沙盒访问 |
| 仪表板 | 查看标准仪表板 |
| 仪表板 | 管理标准仪表板 |
| 目标 | 查看目标 |
| 目标 | 管理目标 |
| 目标 | 激活目标 |
| 目标 | 激活没有映射的区段 |
| 目标 | 管理和激活数据集目标 |
| 目标 | 目标创作 |
| 数据监管 | 查看数据使用策略 |
| 数据监管 | 管理数据使用策略 |
| 数据引入 | 查看源 |
| 数据引入 | 管理源 |
| 轮廓管理 | 查看配置文件设置 |
| 轮廓管理 | 管理配置文件设置 |

>[!ENDSHADEBOX]

## 支持的目标 {#supported-destinations}

在激活静态列表之前，目标必须存在于目标目录中。 在左侧导航中，展开&#x200B;**[!UICONTROL 连接]**&#x200B;并选择&#x200B;**[!UICONTROL 目标]**。 [!DNL Journey Optimizer B2B Edition]当前支持&#x200B;**[!UICONTROL LinkedIn匹配受众]** (Social)目标。 查看&#x200B;[_与受众匹配的LinkedIn帐户_](../data/linkedin-account-matched-audiences.md)

<!-- 
the following destinations:

* **[!UICONTROL Google Customer Match]** (Advertising)
* **[!UICONTROL Facebook Custom Audience]** (Social)
* **[!UICONTROL LinkedIn Matched Audience]** (Social)

![Access the available connector types](./assets/destinations-catalog.png){width="800" zoomable="yes"}

-->

>[!NOTE]
>
>显示的目录不是完整的[!DNL Adobe Experience Platform]目标目录。 如果您直接从[!DNL Experience Platform]访问目标，则会看到更大的目录，但目前在[!DNL Journey Optimizer B2B Edition]中只能激活这些目标。 计划在未来版本中使用其他目标。

## 设置目标 {#set-up-destination}

每个受支持的目标卡都显示&#x200B;**[!UICONTROL 配置新目标]**。 配置目标是激活的先决条件。

1. 在连接器卡中，单击&#x200B;**[!UICONTROL 配置新目标]**。

   ![配置新目标](./assets/destinations-configure-new.png){width="500"}

1. 选择&#x200B;**[!UICONTROL 现有帐户]**&#x200B;或&#x200B;**[!UICONTROL 新帐户]**&#x200B;并输入帐户详细信息，如帐户名称和描述。

1. 单击&#x200B;**[!UICONTROL 连接到目标]**。

   OAuth流允许您登录到相应的帐户：LinkedIn、Google或Facebook。

   >[!IMPORTANT]
   >
   >此时，请勿输入&#x200B;_[!UICONTROL 目标详细信息]_。 只需要连接。

1. 完成人员属性和目标所需的字段之间的任何必填字段映射。

1. 查看数据治理和营销操作设置，然后单击&#x200B;**[!UICONTROL 保存]**。

有关完整设置步骤，请参阅[!DNL Experience Platform]文档中的[新建目标连接](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/destinations/ui/connect-destination){target="_blank"}。

配置后，目标可用于在[!DNL Journey Optimizer B2B Edition]中选择目标的任意位置进行激活。

## 激活和同步 {#activation-sync}

激活由静态列表成员资格驱动，列表和目标受众之间双向同步：

* 将人员添加到静态列表会在24小时内将它们激活到目标，并将它们添加到目标受众，随后添加到受众馈送的任何营销活动。
* 从静态列表中删除人员会从目标中停用他们。 它们会从目标受众和任何连接的营销活动中删除。
* 可以将同一列表同时激活到多个目标。 成员资格会同步到所有成员。

>[!TIP]
>
>要针对区段运行LinkedIn营销活动，请激活这些人员的静态列表以将其添加到LinkedIn匹配的受众目标。 列表中的所有人都会添加到LinkedIn中的匹配受众，营销活动可以在其中定位他们，并且受众会在列表发生更改时自动保持最新状态。
