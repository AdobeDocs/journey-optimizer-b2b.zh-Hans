---
title: '[!DNL Adobe Target]外部受众'
description: 通过帐户历程将外部受众激活到 [!DNL Adobe Target] 。 个性化B2B Web体验并保持跨平台一致性。
feature: Integrations, Audiences, Account Journeys
role: User, Admin
source-git-commit: 598546c62cb2d567f19b26f7f760aa43e4dd0bc9
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 1%

---

# [!DNL Adobe Target]外部受众

您可以通过帐户历程在[!DNL Adobe Target]中激活和个性化外部受众体验。 使用此集成实现高级和量身定制的个性化以提高参与度，并维护[!DNL Target]和[!DNL Journey Optimizer B2B Edition]之间的跨平台一致性。 此一致性确保团队在整个B2B购买者历程中为购买群体调整Web渠道并使其个性化。

通过Adobe Target激活外部受众分为两步工作流：

1. 从历程[添加到外部客户受众](#add-to-customer-external-audience-from-a-journey)。
2. [在Experience Platform中将外部受众](#activate-the-external-audience-to-target-as-a-destination)激活到[!DNL Target]作为目标。

## 从历程添加到客户外部受众

在您的历程中，[添加&#x200B;_执行操作_&#x200B;节点](../journeys/action-nodes.md)以执行&#x200B;_[!UICONTROL 添加到外部客户受众]_&#x200B;操作。 操作通常是您希望因某种类型的触发器（例如事件或上一个操作）而发生的操作。 当具有人员配置文件的合格帐户到达节点时，历程会执行操作。

>[!NOTE]
>
>当具有人员配置文件的合格帐户到达已发布历程中的&#x200B;_添加到外部客户受众_&#x200B;节点时，这些配置文件可能需要48小时才能填充到外部受众中。

1. 在历程画布中选择了&#x200B;_执行操作_&#x200B;节点，选择&#x200B;_[!UICONTROL 对]_ **[!UICONTROL 人员]**&#x200B;执行操作选项。

1. 对于&#x200B;_[!UICONTROL 对人员的操作]_，请选择&#x200B;**[!UICONTROL 添加到外部客户受众]**。

   ![历程节点 — 对人员执行操作 — 添加到外部客户受众](./assets/node-add-external-audience.png){width="550" zoomable="yes"}

1. 从右侧的节点属性中，设置外部受众。

   * 如果已创建一个或多个外部受众，则可以选择&#x200B;**[!UICONTROL 选择现有]**&#x200B;和[选择要使用的受众](#choose-an-external-audience)。

   * 如果要[创建受众](#create-an-external-audience)以用于节点，请选择&#x200B;**[!UICONTROL 新建]**。

### 创建外部受众

1. 在节点属性中选择&#x200B;**[!UICONTROL 新建]**&#x200B;选项后，单击&#x200B;**[!UICONTROL 创建外部客户受众]**。

   ![对人员执行操作 — 添加到外部客户受众 — 创建新选项](./assets/node-add-external-audience-create-new-option.png){width="400"}

1. 在对话框中，为新受众输入&#x200B;**[!UICONTROL Name]**（必需）和&#x200B;**[!UICONTROL Description]**（可选）。

   ![创建外部客户受众对话框](./assets/create-external-customer-audience-dialog.png){width="400"}

1. 单击&#x200B;**[!UICONTROL 创建]**。

   系统会创建新受众并显示确认消息。 然后，您可以继续将其用作节点操作的现有受众。

### 选择外部受众

1. 在节点属性中选择&#x200B;**[!UICONTROL 选择现有]**&#x200B;选项后，单击&#x200B;**[!UICONTROL 选择外部客户受众]**。

   ![对人员执行操作 — 添加到外部客户受众 — 选择现有选项](./assets/node-add-external-audience-select-existing-option.png){width="300"}

1. 在&#x200B;_[!UICONTROL 添加受众]_&#x200B;对话框中，选择要使用的受众。

   您可以在&#x200B;_搜索_&#x200B;字段中输入文本，以筛选显示的项目以匹配受众名称。

   ![对人员执行操作 — 添加到外部客户受众 — 添加受众对话框](./assets/add-audience-dialog.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 添加受众]**。

## 将外部受众激活到Target作为目标

要将外部受众激活到Adobe Target，您需要在[!DNL Adobe Target]中将[!DNL Real-time Customer Data Platform (RTCDP)]配置为目标。 有关此配置的其他信息，请参阅[RTCDP文档](https://experienceleague.adobe.com/zh-hans/docs/platform-learn/tutorials/destinations/target/configure-the-target-destination){target="_blank"}。

>[!IMPORTANT]
>
>通过旅程使用激活功能时，要求您实施的RTCDP使用电子邮件地址作为身份。

激活过程要求您将[!DNL Adobe Target]添加为外部受众或外部目标。 首先，在受众生成器中构建[!DNL Target]受众。 您还可以创建占位符受众并添加外部受众功能。

>[!BEGINSHADEBOX]

![AEP权限图标](../../assets/do-not-localize/icon_permissions-outline.svg)这些步骤需要您分配的用户角色的以下权限：

* **[!UICONTROL Experience Platform]** — 对于&#x200B;_[!UICONTROL 目标]_&#x200B;资源： `Activate Destinations`、`Manage and Activate Dataset Destination`和`View Destination`
* **[!DNL Target]** — `Approver`

>[!ENDSHADEBOX]

1. 在Experience Platform中，在左侧导航中转到&#x200B;**[!UICONTROL 连接]** > **[!UICONTROL 目标]**。

1. 选择&#x200B;**[!UICONTROL 浏览]**&#x200B;选项卡。

1. 找到要用于激活区段的目标连接，单击该名称旁边的&#x200B;_更多菜单_ ( **...**)图标，然后选择&#x200B;**[!UICONTROL 激活受众]**。

   在&#x200B;_[!UICONTROL 搜索]_&#x200B;字段中输入文本以按名称筛选显示的匹配目标。

   ![Experience Platform — 目标 — 浏览Target目标 — 更多菜单](./assets/aep-destinations-activate-target-audience.png){width="800" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 可用受众]_&#x200B;列表中，选择您的外部受众，然后单击&#x200B;**[!UICONTROL 下一步]**。

   ![Experience Platform — 目标 — 浏览Target目标 — 更多菜单](./assets/aep-destinations-activate-target-audience-available-audiences.png){width="700" zoomable="yes"}

1. 执行到目标的任何其他字段映射（可选），然后单击&#x200B;**[!UICONTROL 下一步]**。

1. 查看新的受众参数并单击&#x200B;**[!UICONTROL 完成]**。

   ![Experience Platform — 目标 — 激活目标 — 审核](./assets/aep-destinations-activate-target-audience-review.png){width="700" zoomable="yes"}

激活后，您可以在[Adobe Target受众](https://experienceleague.adobe.com/zh-hans/docs/target/using/audiences/create-audiences/audiences#use-list){target="_blank"}中看到该受众，并在Adobe Target活动中使用它们。

