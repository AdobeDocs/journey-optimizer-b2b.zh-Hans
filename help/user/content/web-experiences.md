---
title: Web体验
description: 创建、设计和发布帐户历程的个性化Web体验 — 在Journey Optimizer B2B edition中为网站访客提供有针对性的内容修改。
feature: Content, Channels
role: User
badgeBeta: label="Beta 版" type="informative" tooltip="此功能当前为有限测试版"
source-git-commit: 6eae855a1e20b3a4350353940cb3ea82fd84933b
workflow-type: tm+mt
source-wordcount: '1497'
ht-degree: 1%

---

# Web体验

Adobe Journey Optimizer B2B edition中的Web渠道使您能够在您的网站上直接创建个性化体验，帮助您以有意义的方式与客户联系。 此功能提供了一个灵活的工具包，您可以使用它来增强与定制内容的互动，并将其与其他渠道（如电子邮件和短信）无缝集成。

通过Web体验，您可以：

* 向目标网站访客投放个性化的内容修改
* 根据帐户属性自定义网站元素，如横幅、文本、图像和按钮
* 使用URL匹配规则定位特定页面或在多个页面中应用更改
* 跟踪参与并监控Web个性化工作的影响

>[!BEGINSHADEBOX]

## 先决条件

在创建Web体验之前，请确保满足以下要求：

* 产品管理员已配置一个或多个Web渠道来定义要用于Web体验的URL（页面）。 有关详细信息，请参阅[Web渠道配置](../admin/configure-channels-web.md)。

* 您的网站已实施[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`)，用于访客识别和内容交付。 确保Adobe Experience Platform Web SDK的版本为2.16或更高版本。

* 您拥有在历程中创建和管理Web体验所需的[权限](../admin/user-management.md#b2b-product-permissions)：
   * _[!UICONTROL 营销活动]_ > _[!UICONTROL 管理营销活动]_ — 添加或更新Web个性化操作节点是必需的。
   * _[!UICONTROL 营销活动]_ > _[!UICONTROL 查看营销活动]_ — 需要查看Web个性化操作节点的详细信息。
   * _[!UICONTROL 营销活动]_ > _[!UICONTROL 批准和发布营销活动]_ — 发布具有一个或多个Web个性化操作节点的历程是必需的。

* 您已经为Web浏览器安装了Adobe Experience Cloud [可视化编辑帮助程序浏览器扩展](#install-the-visual-editing-helper-extension)。 要在Journey Optimizer B2B edition内容设计空间中可靠地打开、创作和预览网页，需要使用此扩展。

  >[!NOTE]
  >
  >Google Chrome和Microsoft Edge目前是唯一支持在Journey Optimizer B2B edition中创作网页的浏览器。

>[!ENDSHADEBOX]

## 安装可视化编辑帮助程序扩展

1. 在浏览器（[!DNL Google Chrome]或[!DNL Microsoft Edge]）中打开新选项卡。

1. 转到[Google Chrome网上商店](https://chromewebstore.google.com/category/extensions)。

   如果您使用的是[!DNL Microsoft Edge]，请选择顶部横幅上其他商店中的&#x200B;_允许扩展_。 启用此选项可让您将扩展从[!DNL Chrome Web Store]添加到[!DNL Microsoft Edge]。

1. 搜索并导航到&#x200B;_[!DNL Adobe Experience Cloud Visual Editing Helper]_浏览器扩展。

   ![适用于Adobe Experience Cloud Chrome的Google可视化编辑帮助程序扩展](./assets/web-experience-google-chrome-adobe-visual-editing-extension.png){width="800" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 添加到Chrome]**，然后在确认对话框中单击&#x200B;**[!UICONTROL 添加扩展]**。

   如果您使用的是[!DNL Microsoft Edge]，此操作会将扩展添加到[!DNL Edge]。

1. 确保在浏览器工具栏中正确启用[!DNL Visual Editing Helper]浏览器扩展。

   Google Chrome工具栏中的![Adobe Experience Cloud可视化编辑帮助程序扩展图标](./assets/web-experience-google-chrome-adobe-visual-editing-extension-icon.png){width="450"}

现在，在Journey Optimizer B2B edition可视化编辑器中为Web体验打开网站时，[!DNL Adobe Experience Cloud Visual Editing Helper]会自动启用。 该扩展没有任何条件设置，并且会自动处理所有设置，包括SameSite Cookie设置。

>[!NOTE]
>
>由于以下原因之一，某些网站可能无法在Journey Optimizer B2B edition Web编辑器中可靠地打开：
>
>* 网站具有严格的安全策略。
>* 网站位于iframe中。
>* 客户QA或暂存站点在外部不可用（该站点为内部站点）。

## 创建Web体验

当您[添加&#x200B;_[!UICONTROL 执行操作]_&#x200B;节点](../journeys/action-nodes.md)并执行以下操作时，可以在历程中设置Web体验：

1. 对于&#x200B;_[!UICONTROL 目标上的]_&#x200B;操作，请选择&#x200B;**[!UICONTROL 人员]**。

1. 若要对人员执行&#x200B;_[!UICONTROL 操作]_，请选择&#x200B;**[!UICONTROL 个性化Web体验]**。

   ![执行操作 — 个性化Web体验](./assets/web-experience-add-journey-node.png){width="500"}

1. 单击&#x200B;**[!UICONTROL 创建Web体验]**。

1. 在&#x200B;_[!UICONTROL 创建Web体验]_&#x200B;对话框中，输入有用的&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**（可选）。

   * 名称 — 最多100个字符，必须唯一，不区分大小写

   * 描述 — 最多300个字符

   >[!NOTE]
   >
   >名称和描述字段支持字母、数字和特殊字符。 保留字符(`\ / : * ? " < > |`)为&#x200B;**_不允许_**。

   ![创建Web体验对话框](./assets/web-experience-create-dialog.png){width="400"}

<!-- What is this for? 1. Properties? -->

1. 在&#x200B;**[!UICONTROL 属性]**&#x200B;选项卡中，输入Web体验的说明。

1. 单击&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡，然后选择要用于Web体验的&#x200B;**[!UICONTROL Web渠道]**。

   Web渠道配置根据配置的页面匹配规则确定应用内容修改的位置。 有关详细信息，请参阅[Web渠道配置](../admin/configure-channels-web.md)。

   ![选定的Web渠道配置](./assets/web-experience-journey-node-actions-tab.png){width="700" zoomable="yes"}

1. 要定义Web修改，请单击&#x200B;**[!UICONTROL 编辑内容]**。

   编辑器将在&#x200B;_[!UICONTROL 内容]_&#x200B;选项卡中打开，您可以在其中定义Web体验的修改。 有关使用设计工具添加Web体验内容修改的详细信息，请参阅[Web体验设计](./web-experience-design.md)。

1. 在右侧面板中，根据要定义和管理体验的方式设置Web体验属性。

   * **[!UICONTROL 可视编辑器]** — 在[可视和非可视编辑器](./web-experience-design.md#web-design-tools)之间切换，以便进行Web体验修改设计。
   * **[!UICONTROL 访客重定向]** — 启用此选项可[将访客重定向到另一个现有URL](#redirect-to-url)，而不是在内容选项卡中创作新的变量。

   ![切换可视编辑器的属性和重定向URL](./assets/web-experience-journey-node-content-properties.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 编辑网页]**&#x200B;以[设计网页修改](./web-experience-design.md)。

1. 修改完成后，单击编辑器上方的左箭头以返回内容选项卡并个性化Web体验节点属性。

   您可以单击最上方的左箭头以返回历程画布。

## 编辑Web体验

1. 打开历程并选择&#x200B;**[!UICONTROL 个性化Web体验]**&#x200B;操作节点。

1. 要更改Web渠道配置或内容，请单击&#x200B;**[!UICONTROL 编辑Web体验]**。

1. 选择&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡，并根据需要更改Web配置。

1. 选择&#x200B;**[!UICONTROL Content]**&#x200B;选项卡，并根据需要使用可视化设计工具。

   * _可视编辑器_ — 单击&#x200B;**[!UICONTROL 编辑内容]**。
   * _非可视编辑器_ — 单击&#x200B;**[!UICONTROL 添加修改]**。

   有关详细信息，请参阅[Web体验设计](./web-experience-design.md)。

1. 修改定义完成后，单击编辑器上方的左箭头以返回内容选项卡和Web体验属性。

   您可以单击最上方的左箭头以返回历程画布。

## 重新定向到 URL

在创建Web体验时，您可以将访客重定向到另一个现有URL，而不是在内容编辑器中创作新的变体。 当您要运行比较两个不同体验的内容试验，而不是只更改页面中的几个元素时，此选项非常有用。

例如，创建具有两种处理方式的Web营销活动：

在处理A中，使用内容编辑器为一半目标群体创作Web体验。

在处理B中，为另一半目标群体选择&#x200B;_[!UICONTROL 重定向到URL]_&#x200B;选项。 输入具有您在Journey Optimizer B2B edition之外创作的替代设计的页面的URL。

![设置访客重定向以将访客重定向到特定URL](./assets/web-experience-journey-node-content-visitor-redirection.png){width="500" zoomable="yes"}

>[!NOTE]
>
>选中此选项后，不会显示网站预览，并禁用&#x200B;_[!UICONTROL 可视编辑器]_&#x200B;切换开关。

当您的Web营销活动处于实时状态时，您可以跟踪您在Journey Optimizer B2B edition中定义的Web体验如何针对使用重定向到替代页面的Web体验执行。

## 测试 Web 体验

在Web体验的内容设计完成后，您可以使用&#x200B;_模拟内容_&#x200B;功能来预览网页修改。 如果插入个性化内容，则可以使用测试配置文件数据检查内容的呈现方式。 模拟工具可从Web体验的&#x200B;_[!UICONTROL Content]_&#x200B;选项卡或内容可视设计编辑器中获得。

1. 单击右上方的&#x200B;**[!UICONTROL 模拟内容]**。

1. 选择测试用户档案。

1. 添加测试配置文件以使用测试配置文件数据检查网页。

<!-- This works differently than emails (rely on Marketo data), currently. Will expand when we figure it out -->

## 激活您的Web体验

当您[发布历程](../journeys/create-publish-journey.md#publish-an-account-journey)时，您的Web体验已激活并对受众可见。 在通过历程激活Web体验之前，请考虑以下事项：

* 如果您发布一个历程，其中的Web体验与另一个已上线的历程影响相同的页面，则所有更改都将应用于网页。

* 如果多个历程更新网站的相同元素，则最近应用的更改优先。

### 投放要求

要启用Web体验交付，必须定义以下设置：

* 在Adobe Experience Platform数据收集中，确保在Adobe Experience Platform服务下启用Adobe Journey Optimizer B2B edition选项的情况下定义数据流。

  此配置可确保Adobe Experience Platform Edge能够正确处理入站事件。 [了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)

* 在Adobe Experience Platform中，确保您有一个启用了&#x200B;_[!UICONTROL Active-On-Edge合并策略]_&#x200B;选项的合并策略。

  在Customer > Profiles > Merge Policies Experience Platform菜单下选择策略。 [了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/ui-guide#configure)

  Journey Optimizer B2B edition入站渠道使用此合并策略，以便在边缘上正确激活和发布入站Web体验。 [了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/ui-guide)

### 故障排除

您可以使用Adobe Experience Platform Assurance中的Edge Delivery视图对Journey Optimizer B2B edition Web体验的交付进行故障诊断。 通过此插件，您可以详细检查请求调用、验证预期的边缘调用以及检查配置文件数据。 此配置文件数据包括身份映射、区段成员资格和同意设置。 您还可以查看该请求的符合条件和不符合条件的活动。

有关Assurance中Edge Delivery视图的更多信息，请参阅[Experience Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/assurance/view/edge-delivery)。
