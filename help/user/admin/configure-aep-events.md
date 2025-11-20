---
title: 选择体验事件和字段
description: 选择Experience Platform事件和字段以根据客户行为在历程中触发实时决策。
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta 版" type="informative" tooltip="此功能当前为测试版"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 046d3648c5e482a69719d0095c297a766dd852ea
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# 选择体验事件和字段

管理员可以在Experience Event合并架构中选择特定的[AEP Experience Events](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"}及其关联字段。 选择后，用户可以配置决策规则以侦听这些Experience事件，以基于近乎实时的事件数据启用动态和针对性的营销活动操作。

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
在历程中使用AEP体验事件包括两个步骤：

1. 管理员[在AEP B2B edition配置中添加了Journey Optimizer体验事件和字段](#add-an-event)。

2. 在历程中，营销人员添加了&#x200B;_侦听事件_&#x200B;节点和[选择体验事件](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event)。

   * 选择要在节点中使用的事件。
   * 选择要用作约束的字段。

>[!BEGINSHADEBOX]

## 准则和限制

在选择符合组织目标的事件时，请牢记以下几点：

* 您最多可以选择50个事件，每个事件最多可以选择100个字段。

* 历程可以收听使用Experience Platform流功能(如Web SDK或HTTP API)引入的Experience事件。

* 您可以使用体验事件在历程中进行决策，但不会保留这些事件。 因此，您无法利用Journey Optimizer B2B edition中体验事件的历史记录。

* 当您使用体验事件并发布历程时，您可以添加更多字段，但无法删除之前已选择的字段。

* 您可以在多个历程中引用体验事件，或在同一历程中多次使用体验事件。

>[!ENDSHADEBOX]

## 管理体验事件

1. 在左侧导航中，选择&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 配置]**。

1. 单击中间面板上的&#x200B;**[!UICONTROL XDM类]**，然后单击&#x200B;**[!UICONTROL 事件]**&#x200B;选项卡以显示可用事件的列表。

   ![访问选定的体验事件](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   该表按&#x200B;_[!UICONTROL 上次更新]_&#x200B;列排序，最近更新的事件默认位于顶部。

   在此页面中，您可以[选择](#add-an-event)和[编辑](#edit-an-event)事件以在历程中使用。

   要访问选定事件的详细信息，请单击事件名称。

### 筛选事件列表

在&#x200B;_[!UICONTROL 搜索]_&#x200B;字段中输入文本以筛选显示的事件以匹配事件名称。

![按名称筛选选定事件的列表](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### 添加事件

要使体验事件可用于历程中的&#x200B;_侦听事件_&#x200B;节点，请选择该事件和支持的字段。

>[!NOTE]
>
>在测试版中，您无法从列表中删除事件。 确保您添加的每个事件均可供您的组织使用。

1. 单击右上方的&#x200B;**[!UICONTROL 选择体验事件]**。

   此时将显示事件详细信息页面。 在此页中，您可以选择事件类型和字段。

   新事件的![事件详细信息](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. 选择事件类型。

   * 单击&#x200B;**[!UICONTROL 选择事件类型]**。

   * 在对话框中，选择事件类型。

     使用&#x200B;_[!UICONTROL 搜索]_&#x200B;字段按名称筛选显示的列表。 使用&#x200B;**[!UICONTROL 仅显示选定字段]**&#x200B;滑块查看当前选择。

     ![选择事件类型对话框](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * 单击&#x200B;**[!UICONTROL 选择]**。

1. 为事件类型选择一个或多个字段。

   * 单击&#x200B;**[!UICONTROL 选择字段]**。

   * 在该对话框中，选择要用作匹配事件的约束条件的字段。

     使用&#x200B;_[!UICONTROL 搜索]_&#x200B;字段按名称筛选显示的列表。 使用&#x200B;**[!UICONTROL 仅显示选定字段]**&#x200B;滑块查看当前选择。

     ![选择字段对话框](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * 单击&#x200B;**[!UICONTROL 选择]**。

1. 在事件详细信息页面中，单击&#x200B;**[!UICONTROL 保存]**。

保存的事件显示在&#x200B;_[!UICONTROL 事件]_&#x200B;选项卡的列表中。

### 编辑事件

编辑事件详细信息以更改字段。

1. 单击事件名称，或单击&#x200B;_更多菜单_ (**...** )图标并选择&#x200B;**[!UICONTROL 编辑]**。

   ![单击“更多”菜单图标](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 编辑字段]**&#x200B;在&#x200B;_[!UICONTROL 选择字段]_&#x200B;对话框中添加更多字段或删除现有选择。

1. 单击&#x200B;**[!UICONTROL 选择]**&#x200B;以保存您的选择。

### 删除事件

>[!NOTE]
>
>对于此功能的Beta版本，您无法从选定事件的列表中删除事件。 计划在GA版本中删除事件。

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->