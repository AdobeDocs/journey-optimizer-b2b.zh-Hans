---
title: 片段
description: 了解如何在Adobe Journey Optimizer B2B edition中创建可视化内容片段，并将其用作电子邮件和电子邮件模板的可重用组件。
feature: Fragments, Content
role: User
exl-id: 3c1d2ca0-d009-4a2a-9d81-1a838845b7fa
source-git-commit: f700f84c55d37ded9980a08286da05011345800c
workflow-type: tm+mt
source-wordcount: '2738'
ht-degree: 2%

---

# 片段

片段是可重复使用的组件，可以在Adobe Journey Optimizer B2B edition中的一个或多个电子邮件和电子邮件模板中引用。 它通常是可以预先创建并快速插入到电子邮件或电子邮件模板中的内容块（文本、图像或两者）。 借助此功能，您可以预构建多个自定义内容块，以供营销团队成员用于汇编电子邮件内容，从而改进设计过程。 常见用例包括电子邮件的页眉/页脚内容块、事件邀请横幅和季节性问候。

>[!BEGINSHADEBOX]

**可视片段**

可视化片段是使用可视化设计工具构建的预定义可视化块，您可以在多个电子邮件或电子邮件模板中重用这些可视化块。 Journey Optimizer B2B edition和本文档的当前范围仅为可视化片段。

>[!NOTE]
>
>[!DNL Journey Optimizer B2B Edition]中尚不支持基于表达式的片段。

>[!ENDSHADEBOX]

要在工作流中充分利用片段，请执行以下操作：

* _创建您自己的片段_ — 从头开始创建可视化片段，或从可视化内容编辑器中将内容另存为片段。
* _重用片段_ — 根据需要多次在内容中使用它们。

## 访问和管理片段

要在Adobe Journey Optimizer B2B edition中访问可视化片段，请转到左侧导航并单击&#x200B;**[!UICONTROL 内容管理]** > **[!UICONTROL 片段]**。 此操作将打开一个列表页面，其中包含实例中创建的所有片段在表中列出。

![访问片段库](./assets/fragments-list.png){width="700" zoomable="yes"}

该表按&#x200B;_[!UICONTROL Modified]_&#x200B;列排序，最近更新的片段默认位于顶部。 单击列标题可在升序和降序之间更改。

### 片段状态和生命周期

片段状态决定其是否可用于电子邮件或电子邮件模板，以及您可以对其进行的更改。

| 状态 | 描述 |
| -------------------- | ----------- |
| 草稿 | 创建片段时，它处于草稿状态。 在您定义或编辑可视化设计空间时，它保持此状态，直到您发布它以用于电子邮件或电子邮件模板为止。 可用操作： <br/><ul><li>编辑所有详细信息<li>在可视设计空间中编辑<li>发布<li>重复<li>删除 |
| 发布日期 | 发布片段后，该片段将可用于电子邮件或电子邮件模板。 无法在可视设计空间中修改已发布的片段内容。 可用操作： <br/><ul><li>编辑描述<li>添加到电子邮件或模板<li>创建草稿版本<li>重复<li>删除（如果未使用） |
| 以草稿发布 | 从已发布的片段创建草稿时，已发布的版本仍可用于电子邮件或电子邮件模板，并且草稿内容可在可视设计空间中修改。 如果您发布草稿版本，它会替换当前已发布的版本，并且内容会在使用草稿的电子邮件和电子邮件模板中进行更新。 可用操作： <br/><ul><li>编辑描述<li>添加到电子邮件或模板<li>在可视设计空间中编辑草稿版本<li>发布草稿版本<li>重复<li>删除（如果未使用） |

![片段状态生命周期](./assets/status-lifecycle-diagram.png){zoomable="yes"}

>[!IMPORTANT]
>
>Journey Optimizer B2B edition 8月版本中引入了片段状态。 在此版本之前创建的所有片段均具有&#x200B;_草稿_&#x200B;状态，即使它们在电子邮件或模板中使用也是如此。 如果您对这些片段进行了任何更改，则必须发布片段以传播更改。

### 筛选片段列表

要按名称搜索片段，请在搜索栏中输入文本字符串以查找匹配项。 单击&#x200B;_筛选器_&#x200B;图标（![显示或隐藏筛选器图标](../assets/do-not-localize/icon-filter.svg)）以显示可用的筛选器选项并更改设置以根据指定的条件筛选显示的项。

![筛选显示的片段](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

### 自定义列显示

通过单击右上角的&#x200B;_自定义表_&#x200B;图标（![自定义表图标](../assets/do-not-localize/icon-column-settings.svg)）自定义要在表中显示的列。

在对话框中，选择要显示的列，然后单击&#x200B;**[!UICONTROL 应用]**。

![选择要显示的列](./assets/fragments-customize-table-dialog.png){width="300"}

## 创建片段

您可以通过单击右上角的&#x200B;**[!UICONTROL 创建片段]**，在Journey Optimizer B2B edition中创建新可视片段。

1. 在&#x200B;_[!UICONTROL 创建片段]_&#x200B;对话框中，输入有用的&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**（可选）。

   片段要求：

   * 名称 — 最多100个字符，必须唯一，不区分大小写

   * 描述 — 最多300个字符

   * 允许使用Alpha、数字和特殊字符

   * 保留字符为&#x200B;**_不允许_**： `\ / : * ? " < > |`

   ![创建片段对话框](./assets/assets-fragments-create-dialog.png){width="400"}

1. 单击&#x200B;**[!UICONTROL 创建]**。

   此时将打开可视化设计空间，并显示一个空画布。

1. 使用内容设计工具创建可视化片段内容：

   * [添加结构和内容](./fragment-authoring.md#add-structure-and-content)
   * [添加Assets](./fragment-authoring.md#add-assets)
   * [导航图层、设置和样式](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [个性化内容](./fragment-authoring.md#personalize-content)
   * [启用自定义字段](./fragment-authoring.md#enable-fragment-customization)
   * [编辑链接的URL跟踪](./fragment-authoring.md#edit-linked-url-tracking)

1. （可选）将[品牌主题](./brand-themes.md)应用于片段内容以简化片段创作过程并确保设计符合定义的标准。

   >[!NOTE]
   >
   >应用主题时，片段兼容性仅限于在&#x200B;_主题模式_&#x200B;中创建的电子邮件和电子邮件模板。

   单击右侧的&#x200B;_主题_ （ ![主题图标](../assets/do-not-localize/icon-design-themes.svg) ）图标。

   ![片段设计空间 — 已选择“主题”图标](./assets/fragment-design-themes-icon-selected.png){width="600" zoomable="yes"}

   选择&#x200B;**[!UICONTROL 我的主题]**&#x200B;选项卡中列出的自定义主题之一，或者您可以选择&#x200B;**[!UICONTROL Adobe主题]**&#x200B;以使用内置主题。 单击列表外部时，选定的主题将应用画布中所有组件的样式。 您可以根据需要切换颜色变体。

1. 随时单击&#x200B;**[!UICONTROL 保存]**&#x200B;以保存草稿片段。

1. 准备好在电子邮件或电子邮件模板中使用片段时，单击&#x200B;**[!UICONTROL 发布]**。

## 查看片段详细信息

单击列表页面中任何片段的名称以打开片段详细信息页面。 您可以选择编辑片段、重命名片段或更新片段描述。 进行更新，然后单击名称或描述字段外部以自动保存更改。

>[!NOTE]
>
>如果电子邮件或电子邮件模板正在使用已发布的片段，则无法更改名称或编辑内容。 如果要对片段进行更改，可以创建草稿版本。

![查看已发布片段的详细信息](./assets/fragment-details-published.png){width="600" zoomable="yes"}

单击&#x200B;**[!UICONTROL 编辑片段]**&#x200B;以在可视内容编辑器中打开该片段。

单击左上角的&#x200B;_返回_&#x200B;箭头可随时退出视图，该箭头将返回到&#x200B;_片段_&#x200B;列表页面。

## 引用使用的视图片段

在片段详细信息页面中，单击&#x200B;**[!UICONTROL 使用者]**&#x200B;选项卡以查看片段当前在Journey Optimizer B2B edition中的使用位置、电子邮件、电子邮件模板和片段的详细信息。

>[!IMPORTANT]
>
>无法删除任何电子邮件或电子邮件模板当前正在使用的任何片段。

根据类别显示引用： _电子邮件_&#x200B;或&#x200B;_电子邮件模板_。 Journey Optimizer B2B edition中的电子邮件在帐户历程中嵌入和创作，因此使用片段的电子邮件的父历程显示在引用中。

![由对片段的引用使用](./assets/fragment-used-by-published.png){width="600" zoomable="yes"}

单击链接以打开相应的电子邮件或电子邮件模板，其中使用该片段。

## 删除片段

无法删除任何电子邮件或电子邮件模板当前使用的任何片段，因此请确保在启动片段移除之前检查&#x200B;_used-by_&#x200B;引用。 此外，删除操作无法撤消，因此在启动删除操作之前请检查。

您可以使用以下任一方法删除片段：

* 从右侧的片段详细信息中，单击&#x200B;**[!UICONTROL 删除]**。
* 从&#x200B;_[!UICONTROL 片段]_&#x200B;列表页面，单击片段旁边的省略号并选择&#x200B;**[!UICONTROL 删除]**。

此操作将打开确认对话框。 您可以通过单击&#x200B;**[!UICONTROL 取消]**&#x200B;或单击&#x200B;**[!UICONTROL 删除]**&#x200B;确认删除来中止该进程。

![删除片段对话框](./assets/fragment-delete-dialog.png){width="400"}

如果片段当前正在使用中，则该操作会打开一个信息对话框，警告您无法删除该片段。 单击&#x200B;**[!UICONTROL 确定]**，这将中止删除操作。

![删除片段对话框 — 无法删除正在使用的片段](./assets/fragment-delete-dialog-in-use.png){width="400"}

## 编辑片段

对片段的编辑取决于其当前状态：

* 当片段处于&#x200B;_草稿_&#x200B;状态时，您可以编辑其任何详细信息和可视内容。
* 当片段处于&#x200B;_已发布_&#x200B;状态时，您可以编辑片段描述，但不能编辑名称。 无法编辑可视内容。
* 当片段处于&#x200B;_已发布，状态为_&#x200B;草稿时，编辑详细信息仅限于描述。 您还可以编辑草稿版本的可视内容。

>[!BEGINTABS]

>[!TAB 草稿]

1. 从&#x200B;_[!UICONTROL 片段]_&#x200B;列表页面，单击片段名称以将其打开。

   随后将显示可视内容的预览，其中片段详细信息位于右侧。

1. 修改任何详细信息，如名称和描述。

   ![具有草稿状态的片段的详细信息](./assets/fragment-draft-details.png){width="600" zoomable="yes"}

1. 若要更改可视化设计空间中的内容，请单击&#x200B;**[!UICONTROL 编辑片段]**。

   根据需要使用可视化设计工具：

   * [添加结构和内容](./fragment-authoring.md#add-structure-and-content)
   * [添加Assets](./fragment-authoring.md#add-assets)
   * [导航图层、设置和样式](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [个性化内容](./fragment-authoring.md#personalize-content)
   * [启用自定义字段](./fragment-authoring.md#enable-fragment-customization)
   * [编辑链接的URL跟踪](./fragment-authoring.md#edit-linked-url-tracking)

   单击&#x200B;**[!UICONTROL 保存]**，或单击&#x200B;**[!UICONTROL 保存并关闭]**&#x200B;以返回片段详细信息。

1. 如果片段符合您的条件并且您想在电子邮件或电子邮件模板中使用它，请单击&#x200B;**[!UICONTROL 发布]**。

>[!TAB 已发布]

1. 从&#x200B;_[!UICONTROL 片段]_&#x200B;列表页面，单击片段名称以将其打开。

   随后将显示可视内容的预览，其中片段详细信息位于右侧。

1. 如果需要，请修改说明。

   对于已发布的片段，无法更改所有其他详细信息。

1. 如果要更新内容，请单击右上方的&#x200B;**[!UICONTROL 创建草稿版本]**。

   在对话框中单击&#x200B;**[!UICONTROL 确定]**&#x200B;以在可视设计空间中打开草稿版本。

   ![创建草稿版本对话框](./assets/fragments-create-draft-version.png){width="300"}

   根据需要使用可视化设计工具：

   * [添加结构和内容](./fragment-authoring.md#add-structure-and-content)
   * [添加Assets](./fragment-authoring.md#add-assets)
   * [导航图层、设置和样式](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [个性化内容](./fragment-authoring.md#personalize-content)
   * [启用自定义字段](./fragment-authoring.md#enable-fragment-customization)
   * [编辑链接的URL跟踪](./fragment-authoring.md#edit-linked-url-tracking)

   单击&#x200B;**[!UICONTROL 保存]**，或单击&#x200B;**[!UICONTROL 保存并关闭]**&#x200B;以返回片段详细信息。

1. 当草稿片段符合您的条件并且您想要使更改可用于电子邮件或电子邮件模板时，请单击&#x200B;**[!UICONTROL 发布]**。

   发布草稿版本时，草稿版本会替换当前已发布的版本，并且内容会在电子邮件和电子邮件模板中更新（该模板已在使用中）。

>[!TAB 已发布草稿]

有两种方法可以打开草稿版本以从&#x200B;_[!UICONTROL 片段]_&#x200B;列表页面进行编辑：

* 单击片段名称旁边的&#x200B;_更多_&#x200B;图标(**...**)，然后选择&#x200B;**[!UICONTROL 打开草稿版本]**。

  ![打开草稿版本](./assets/fragments-create-draft-version.png){width="300"}

* 单击片段名称以将其打开。 然后，单击右上方的&#x200B;**[!UICONTROL 打开草稿版本]**。

  将显示草稿版本的可视内容预览，其中片段详细信息位于右侧。

要更新内容，请执行以下操作：

1. 单击右上方的&#x200B;**[!UICONTROL 编辑片段]**。 根据需要使用可视化设计工具：

   * [添加结构和内容](./fragment-authoring.md#add-structure-and-content)
   * [添加Assets](./fragment-authoring.md#add-assets)
   * [导航图层、设置和样式](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [个性化内容](./fragment-authoring.md#personalize-content)
   * [启用自定义字段](./fragment-authoring.md#enable-fragment-customization)
   * [编辑链接的URL跟踪](./fragment-authoring.md#edit-linked-url-tracking)

   单击&#x200B;**[!UICONTROL 保存]**，或单击&#x200B;**[!UICONTROL 保存并关闭]**&#x200B;以返回片段详细信息。

1. 当草稿片段符合您的条件并且您想要使更改可用于电子邮件或电子邮件模板时，请单击&#x200B;**[!UICONTROL 发布]**。

   发布草稿版本时，草稿版本会替换当前已发布的版本，并且内容会在电子邮件和电子邮件模板中更新（该模板已在使用中）。

>[!ENDTABS]

## 重复片段

您可以使用以下任一方法复制片段：

* 从&#x200B;_[!UICONTROL 片段]_&#x200B;列表页面，单击片段名称旁边的&#x200B;_更多_&#x200B;图标(**...**)，然后选择&#x200B;**[!UICONTROL 复制]**。
* 在片段详细信息页面的右上方，单击&#x200B;**[!UICONTROL ...更多]**&#x200B;并选择&#x200B;**[!UICONTROL 复制]**。

![复制片段](./assets/fragment-details-duplicate.png){width="600" zoomable="yes"}

在对话框中，输入有用的名称（唯一）和描述。 单击&#x200B;**[!UICONTROL 复制]**&#x200B;以完成操作。

![输入复制的片段的名称和描述](./assets/fragment-duplicate-dialog.png){width="400"}

然后，重复的（新）片段出现在&#x200B;_片段_&#x200B;列表中。

## 从电子邮件或模板内容保存新片段

在可视内容编辑器中创建/编辑电子邮件或电子邮件模板时，您可以选择将内容的所有或部分另存为片段，以便重用。

1. 当某些内容要另存为片段时，请单击“**[!UICONTROL 更多]**”，然后选择“**[!UICONTROL 另存为片段]**”。

1. 选择要包含在片段中的不同元素。

   按住Shift或Control按钮选择多个结构。

   您只能选择彼此相邻的结构，并且接口不允许您选择非相邻元素。

1. 选择内容后，单击右上方的&#x200B;**[!UICONTROL 创建]**。

1. 在对话框中，为片段输入有用的名称和描述。 然后单击&#x200B;**[!UICONTROL 创建]**。

   然后，新片段将显示在&#x200B;_片段_&#x200B;列表页面中，并可用于电子邮件和电子邮件模板。

## 将可视化片段添加到您的电子邮件或模板内容

片段设计为可重复使用，并且可以插入以用于电子邮件和电子邮件模板的创作。 您最多可以在电子邮件或模板中添加30个片段。 片段最多只能嵌套一个级别。

>[!BEGINTABS]

>[!TAB 向电子邮件添加片段]

1. 导航到&#x200B;**[!UICONTROL 帐户历程]**&#x200B;并打开现有历程或创建新历程。

1. 创建[_[!UICONTROL 发送电子邮件&#x200B;]_节点](./add-email.md#add-an-email-action-node-in-a-journey)。

1. 创建或编辑节点[的](./email-authoring.md)电子邮件内容。

1. 从&#x200B;**[!UICONTROL 组件]**&#x200B;菜单拖放项以提供片段的&#x200B;_结构_。

1. 要打开已发布片段的列表，请单击&#x200B;_片段_&#x200B;图标。

   您可以：
   * 对列表进行排序。
   * 浏览、搜索和筛选列表。
   * 在卡片（缩略图）和列表视图之间切换。
   * 刷新列表以反映任何最近创建的片段。

   ![在可视设计器中搜索片段](./assets/fragments-list-designer-search.png){width="600"}

1. 将任意片段拖放到结构组件占位符中。

   编辑器在电子邮件结构的部分/元素中呈现片段。

片段的内容在结构中动态更新，以呈现内容在电子邮件中如何显示的可视化。

>[!TIP]
>
>如果希望片段占据电子邮件中的整个水平布局，请添加[!UICONTROL 1:1列]结构，然后将片段拖放到其中。

保存电子邮件后，选择&#x200B;_[!UICONTROL 使用者]_&#x200B;选项卡时，该电子邮件会显示在片段详细信息页面中。 添加到电子邮件的片段在电子邮件或模板中不可编辑 — 已发布的源片段定义了内容。

>[!TAB 将片段添加到电子邮件模板]

1. 从左侧导航中，单击&#x200B;**[!UICONTROL 内容管理]** > **[!UICONTROL 模板]**。

1. 创建新模板，或打开现有电子邮件模板，然后单击&#x200B;**[!UICONTROL 编辑电子邮件模板]**。

1. 从&#x200B;**[!UICONTROL 组件]**&#x200B;菜单拖放项以提供片段的&#x200B;_结构_。

1. 要打开片段列表，请单击&#x200B;_片段_&#x200B;图标。

   您可以：
   * 对列表进行排序。
   * 浏览、搜索和筛选列表。
   * 在卡片（缩略图）和列表视图之间切换。
   * 刷新列表以反映任何最近创建的片段。

   ![在可视设计器中搜索片段](./assets/fragments-list-designer-search.png){width="600"}

1. 将任意片段拖放到结构组件占位符中。

   编辑器在电子邮件模板结构的部分/元素中呈现片段。

1. 将任意片段拖放到结构组件占位符中。

   编辑器在电子邮件模板结构的部分/元素中呈现片段。

>[!TIP]
>
>如果希望片段占据电子邮件模板内的整个水平布局，请添加&#x200B;_[!UICONTROL 1:1列]_&#x200B;结构，然后将片段拖放到其中。

保存电子邮件模板后，在选择&#x200B;_[!UICONTROL 使用者]_&#x200B;选项卡时，该模板会显示在片段详细信息页面中。 添加到电子邮件模板的片段在模板中不可编辑 — 已发布的源片段定义了内容。

>[!ENDTABS]

## 电子邮件和模板创作期间的片段操作

将片段添加到电子邮件或电子邮件模板时，无法在电子邮件或模板中编辑片段内容。 但是，您可以应用以下操作：

* **[!UICONTROL 删除]** — 此操作从当前电子邮件或电子邮件模板内容中删除片段（片段源不受影响）。
* **[!UICONTROL 刷新]** — 此操作刷新当前电子邮件或电子邮件模板中片段的内容。 当您想要反映在添加到电子邮件或电子邮件模板之后对片段进行的任何最近编辑时，刷新很有用。
* **[!UICONTROL 复制]** — 此操作在编辑器中复制同一电子邮件或电子邮件模板中的片段，这些片段具有相同的维度，并紧跟其下添加。
* **[!UICONTROL 打开片段]** — 此操作将打开一个新的浏览器选项卡，其中包含片段编辑器页面和详细信息。
* **[!UICONTROL 中断继承]** — 此操作中断来自源的片段（及其更改）继承。 使用此操作可以在电子邮件或电子邮件模板中作为独立的可编辑内容使用片段内容。 此操作还会从原始片段的&#x200B;_Used By_&#x200B;引用中删除电子邮件或电子邮件模板。

在编辑器页面上选择片段时，可以从右侧的上下文工具栏和属性面板中执行这些操作。

![将操作应用于所选片段](./assets/fragment-actions-email-authoring.png){width="600" zoomable="yes"}
