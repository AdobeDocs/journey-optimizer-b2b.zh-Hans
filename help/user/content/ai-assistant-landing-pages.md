---
title: 用于登陆页面内容的AI助手
description: 使用AI助手生成登陆页面内容 — 在Journey Optimizer B2B edition中使用参考资源和购买团体角色定位创建页面文本和图像。
feature: Generative AI, Landing Pages, Content
badgeBeta: label="Beta 版" type="informative" tooltip="此功能当前为有限测试版"
topic: Artificial Intelligence
role: User
level: Beginner
exl-id: d1e818fb-7450-4c13-bc6c-24da5fb71285
source-git-commit: 859656dc4e355be0d9efe9414ad93404970d6e73
workflow-type: tm+mt
source-wordcount: '2700'
ht-degree: 1%

---

# 用于登陆页面内容的AI助手 {#generative-full-content}

用于[!DNL Adobe Journey Optimizer B2B Edition]中登陆页面内容的AI助手使用Adobe的AI支持的内容生成功能，彻底改变了营销人员创建专业且品牌一致的登陆页面内容的方式。 借助先进的创作AI模型和对品牌准则的深入了解，AI Assistant可自动生成个性化、吸引人和有效的内容。 它利用您的营销目标并优化品牌概述样式、布局、色调等内容。 AI Assistant使营销活动和项目的创建和执行更加直观、简单和轻松。 将此功能添加到工作流可以节省时间、提高效率并取得更好的结果。

您可以为登陆页面生成完整的内容体验，包括文本和图像。 这项强大的功能可帮助您创建引人注目的品牌内内容，这些内容会与您的受众连接。

>[!NOTE]
>
>此功能在其Beta版本中提供，如有更改，恕不另行通知。

>[!IMPORTANT]
>
>若要在[!DNL Journey Optimizer B2B Edition]中访问这些功能，您必须具有&#x200B;_[!UICONTROL AI助手]_ > _[!UICONTROL 生成内容]_&#x200B;权限。 有关产品管理员如何授予功能权限的详细信息，请参阅[编辑产品权限的角色](../admin/user-management.md#edit-roles-for-product-permissions)。

## 准则和限制

在开始使用此功能之前，请查看[准则和限制](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations)。 在[!DNL Journey Optimizer B2B Edition]中使用AI功能之前，还需要用户同意[&#128279;](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}。 有关更多信息，请与您的 Adobe 代表联系。

Adobe承诺在媒体创建中使用创作AI工具时提高透明度，有鉴于此，Adobe在下载或导出包含Firefly生成的资源的任何内容或项目时应用[内容凭据](https://helpx.adobe.com/cn/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"}。

以下限制和准则适用于在[!DNL Journey Optimizer B2B Edition]中生成登陆页面内容所使用的AI助手功能：

* 英语是唯一受支持的语言。
* 生成的内容可能不准确 — 请分享您的反馈，以便Adobe工程师可以优化模型。
* 您可以上传多个内容引用资源，但只能为特定层代利用一个。
* 使用特定于品牌或自定义的模板为完整登陆页面生成内容。 建议使用最多包含8至10个图像的登陆页面模板。
* 选择生成的变体时，请确保使用向上缩略图、向下缩略图或标记图标报告任何有问题的输出。

## 用于内容生成的输入和设置

您可以为登陆页面或页面中选定的组件生成完整内容。 使用AI助手工具生成所需的内容时，需要提供输入（包括提示和引用内容）以及文本和图像的设置。

### 提示

为创作AI模型使用定义良好的提示来准确地解释。 您提供的营销目标/提示会极大地影响所生成内容的质量。

![提示字段](./assets/gen-ai-prompt.png){width="320"}

有关创建有效提示的详细信息，请参阅&#x200B;_[提示最佳实践](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_。

>[!BEGINSHADEBOX]

**提示库**

有效的提示对于生成最佳内容至关重要。 如果您希望在构建提示方面获得帮助，请单击&#x200B;_提示库_ ![提示库图标](../assets/do-not-localize/icon-library.svg)图标以访问根据目标整理的提示想法库。 在搜索字段中输入文本以根据关键词字符串查找提示。

![AI助手 — 访问提示库](./assets/gen-ai-prompt-library.png){width="600" zoomable="no"}

选择最能反映您预期目标的提示，然后单击&#x200B;**[!UICONTROL 尝试此提示]**。 在&#x200B;_[!UICONTROL 提示]_&#x200B;字段中，将任意占位符（如`[Key Feature/Information]`）替换为指定您的品牌、产品、营销活动和用例所需的值。

>[!ENDSHADEBOX]

### 文本设置

展开右侧面板中的&#x200B;**[!UICONTROL 文本设置]**，并设置生成文本的选项。

* **[!UICONTROL 购买群]** — 选择[购买群角色](../buying-groups/buying-groups-role-templates.md)，以用于定位您的消息传送。
* **[!UICONTROL 营销历程阶段]** — 选择[购买团体阶段](../buying-groups/buying-group-stages.md)，以用于消息传递的定位。
* **[!UICONTROL 通信策略]** — 为生成的文本选择最合适的通信样式。
* **[!UICONTROL 语言]** — 选择所生成内容的语言。
* **[!UICONTROL 音调]** — 该音调应该与您的受众产生共鸣。 例如，您可以将消息调整为提供声音信息、富有趣味或有说服力。

![文本设置面板，显示购买群组、营销历程阶段、沟通策略、语言和音调选项](./assets/gen-ai-text-settings.png){width="350" zoomable="yes"}

单击左箭头返回主&#x200B;_[!UICONTROL 设置]_。

### 图像设置

要在生成的内容中包含图像，请展开右侧面板中的&#x200B;**[!UICONTROL 图像设置]**&#x200B;并设置选项。

默认情况下，**[!UICONTROL 使用AI生成图像]**&#x200B;选项处于禁用状态。 启用此功能并设置以下选项以在建议的内容变体中包含生成的图像：

* **[!UICONTROL 创成模型]**：从现成的Adobe提供的模型、用于专门功能的合作伙伴模型或根据您的品牌资源训练的配置自定义模型中选择。 有关创成模型的详细信息，请参阅&#x200B;_[用于品牌对齐的创成AI模型](generative-ai-models.md)_。
* **[!UICONTROL 宽高比]**：选择图像组件时，此设置将确定资源的宽度和高度。 您可以选择通用比率，如16:9、4:3、3:2或1:1，也可以输入自定义大小。
* **[!UICONTROL 内容类型]**：该类型对可视元素的性质进行分类，区分不同的可视表示形式，如照片、图形或艺术品。
* **[!UICONTROL 视觉强度]**：通过调整图像的强度来控制其影响。 较低的设置（如2）可创建更柔和、更受限的外观，而较高的设置（如10）则使图像更生动、视觉更强大。
* **[!UICONTROL 颜色和色调]**：图像内颜色的总体外观及其传达的情绪或气氛。
* **[!UICONTROL 照明]**：用于图像的照明样式，它塑造了图像的大气并突出显示特定的元素。
* **[!UICONTROL 合成]**：图像框架中元素的排列。

![显示生成模型、内容类型、视觉强度、颜色和色调、光照和合成选项的图像设置面板](./assets/gen-ai-image-settings.png){width="350" zoomable="yes"}

单击左箭头返回主&#x200B;_[!UICONTROL 设置]_。

### 参考内容

上传参考内容资产以生成准确的品牌内内容。 否则，生成的内容将基于公开可用的信息。 引用内容用作内容生成和图像推荐的源。 有关准则和最佳实践，请参阅&#x200B;_[优化的参考内容](../ai-assistant/generative-ai-content.md#reference-content)_。

从&#x200B;**[!UICONTROL 引用内容]**&#x200B;设置中，单击&#x200B;**[!UICONTROL 上载文件]**&#x200B;以添加包含要用于其他上下文的内容的任何资源。

![上载要用于引用内容的文件](./assets/gen-ai-reference-content-upload.png){width="350" zoomable="yes"}

要上传的文件可以具有以下格式：PDF、JPEG、PNG或ZIP文件（包含支持的文件格式）。 上传的品牌资产的最大大小为50MB。 较大的文件或大量的图像可以工作，但这会增加处理时间。

如果要选择以前上载的文件，请展开&#x200B;**[!UICONTROL 上载的引用内容]**&#x200B;列表，然后启用要用于内容生成的资源。

![启用现有引用内容以使用](./assets/gen-ai-reference-content-select.png){width="350" zoomable="yes"}

## 使用创作AI工具 {#gen-ai-tools}

要开始生成内容，请打开登陆页面的内容编辑器，并访问右侧面板外边栏上的创作AI工具。 选择&#x200B;_AI助手_ （![用于内容的AI助手](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ）以显示可用于当前内容选择的内容生成工具。

根据要使用的登陆页面内容生成类型，请执行以下步骤：

>[!BEGINTABS]

>[!TAB 整页]

请按照以下步骤操作，使用AI助手通过优化现有登陆页面模板来生成完整的登陆页面：

1. 在[创建登陆页面](./landing-pages.md#create-a-landing-page)后，单击&#x200B;**[!UICONTROL 编辑登陆页面]**。

1. 选择模板。

   完整内容生成需要模板。 它可以是Adobe提供的标准模板，也可以是保存的模板。 您还可以使用&#x200B;_[!UICONTROL 导入HTML]_&#x200B;选项导入模板。

   有关使用登陆页面模板的详细信息，请参阅&#x200B;_[选择已保存或示例模板](./landing-pages.md#select-a-saved-or-sample-template)_。

1. 在右侧面板的外边栏上，选择&#x200B;_AI助手_ （![用于内容切换的AI助手](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ）图标。

   登陆页面设计空间中的![AI助手切换](./assets/gen-ai-full-landing-page-ai-panel.png){width="600" zoomable="yes"}

   右侧的AI助手设置反映完整登陆页面的生成设置。

1. (Beta)选择您的&#x200B;**[!UICONTROL Brand]**&#x200B;以确保AI生成的内容与您的品牌规范一致。

   如果没有已发布的品牌，请单击&#x200B;**[!UICONTROL 创建品牌]**&#x200B;以定义您的[可重复使用的品牌指南](./brands-overview.md)。

1. 在&#x200B;**[!UICONTROL 提示]**&#x200B;字段中，输入要生成的内容的描述。

   如果您需要有关创建有效提示的帮助，请使用[提示库](#prompt-library)。

   ![AI助手 — 用于生成登陆页面内容的提示库](./assets/email-designer-ai-assistant-full.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >如果您不熟悉如何提示生成内容，请查看&#x200B;_[提示最佳实践](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_。

1. 完成内容指导设置以定制生成的内容：

   * [**[!UICONTROL 文本设置]**](#text-settings) — 为生成的文本内容提供指导。
   * [**[!UICONTROL 图像设置]**](#image-settings) — 如果要在生成的内容中包含图像，请启用图像生成并提供指导。
   * [**[!UICONTROL 引用内容]**](#reference-content) — 提供用作内容生成源的内容资源。

1. 提示和设置就绪后，单击&#x200B;**[!UICONTROL 生成]**。

1. 在AI助手面板中向下滚动，浏览生成的变体以确定哪个变体最适合。

   * 单击&#x200B;_全屏_ （![全屏图标](../assets/do-not-localize/icon-full-screen.svg) ）图标以打开&#x200B;_[!UICONTROL 生成登陆页面]_&#x200B;对话框

   * 如果需要，请使用[细化操作](#refine-a-variation)来微调变体，以确保它们符合您的确切要求。

   * 通过单击&#x200B;_向上缩略图_、_向下缩略图_&#x200B;或&#x200B;_标记_&#x200B;图标，为生成的变体[提交反馈](#submit-variation-feedback)，并选择最能总结您的反馈的原因。

1. 单击&#x200B;**[!UICONTROL 选择]**&#x200B;以将模板内容替换为选定的变体并返回登陆页面设计空间。

   您可以使用画布上的编辑和格式化工具来更改生成的内容，以及右侧的&#x200B;_[!UICONTROL 设置]_&#x200B;和&#x200B;_[!UICONTROL 样式]_&#x200B;选项。

>[!TAB 仅限文本]

按照以下步骤使用AI助手优化或增强现有登陆页面的文本内容：

1. 在登陆页面设计空间中，选择&#x200B;_文本_&#x200B;组件以定位特定内容。

1. 在右侧面板的外边栏上，选择&#x200B;_AI助手_ （![用于内容切换的AI助手](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ）图标。

   登陆页面设计空间中的![AI助手切换](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   右侧的设置反映了文本组件的内容生成设置。

1. (Beta)选择您的&#x200B;**[!UICONTROL Brand]**&#x200B;以确保AI生成的内容与您的品牌规范一致。

   如果没有已发布的品牌，请单击&#x200B;**[!UICONTROL 创建品牌]**&#x200B;以[定义可重复使用的品牌指南](./brands-overview.md)。

1. 在&#x200B;**[!UICONTROL 提示]**&#x200B;字段中，输入要生成的内容的描述。

   ![AI助手 — 文本设置](./assets/email-designer-ai-assistant-text.png){width="600" zoomable="yes"}

   如果您需要有关创建有效提示的帮助，请使用[提示库](#prompt-library)。

1. 完成内容指导设置以定制生成的内容：

   * [**[!UICONTROL 文本设置]**](#text-settings) — 为生成的文本内容提供指导。

   * [**[!UICONTROL 引用内容]**](#reference-content) — 提供用作内容生成源的内容资源。

1. 提示和设置就绪后，单击&#x200B;**[!UICONTROL 生成]**。

1. 在AI助手面板中向下滚动，浏览生成的变体以确定哪个变体最适合。

   * 单击&#x200B;_全屏_ （![全屏图标](../assets/do-not-localize/icon-full-screen.svg) ）图标以打开&#x200B;_[!UICONTROL 生成文本]_&#x200B;对话框

   * 如果需要，请使用[细化操作](#refine-a-variation)来微调变体，以确保它们符合您的确切要求。

   * 通过单击&#x200B;_向上缩略图_、_向下缩略图_&#x200B;或&#x200B;_标记_&#x200B;图标，为生成的变体[提交反馈](#submit-variation-feedback)，并选择最能总结您的反馈的原因。

1. 获得所需的内容后，单击&#x200B;**[!UICONTROL 选择]**&#x200B;以使用选定的变体替换文本并返回登陆页面设计空间。

   您可以使用画布上的编辑和格式化工具来更改文本，以及右侧的&#x200B;_[!UICONTROL 设置]_&#x200B;和&#x200B;_[!UICONTROL 样式]_&#x200B;选项。

>[!TAB 仅图像]

按照以下步骤使用AI助手优化或增强现有登陆页面的图像内容：

1. 在登陆页面设计空间中，选择&#x200B;_Image_&#x200B;组件以定位特定内容。

1. 在右侧面板的外边栏上，选择&#x200B;_AI助手_ （![用于内容切换的AI助手](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ）图标。

   登陆页面设计空间中的![AI助手切换](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   右侧的AI助手设置反映了图像组件的生成设置。

1. (Beta)选择您的&#x200B;**[!UICONTROL Brand]**&#x200B;以确保AI生成的内容与您的品牌规范一致。

   如果没有已发布的品牌，请单击&#x200B;**[!UICONTROL 创建品牌]**&#x200B;以[定义可重复使用的品牌指南](./brands-overview.md)。

1. 在&#x200B;**[!UICONTROL 提示]**&#x200B;字段中输入所需内容的说明。

   ![AI助手 — 文本设置](./assets/email-designer-ai-assistant-image.png){width="600" zoomable="yes"}

   如果您需要有关创建有效提示的帮助，请使用[提示库](#prompt-library)。

1. 完成内容指导设置以定制生成的内容：

   * [**[!UICONTROL 图像设置]**](#image-settings) — 如果要在生成的内容中包含图像，请启用图像生成并提供指导。

   * [**[!UICONTROL 引用内容]**](#reference-content) — 提供用作内容生成源的内容资源。

1. 如果对提示和设置感到满意，请单击&#x200B;**[!UICONTROL 生成]**。

   AI Assistant处理请求并根据提示和其他输入生成最合适的图像。

   >[!IMPORTANT]
   >
   >如果参考内容中没有图像，或者没有与输入提示相关的图像，则输出为空。

1. 浏览生成的变体或单击&#x200B;_全屏_ （ ![全屏图标](../assets/do-not-localize/icon-full-screen.svg) ）图标以打开&#x200B;_[!UICONTROL 生成图像]_&#x200B;对话框。

   该对话框提供了额外的空间来比较变体、调整图像和引用内容设置（如果需要）以及重新生成变体。

   您可以选择变体并单击&#x200B;**[!UICONTROL 生成类似]**&#x200B;以生成与所选变体类似的其他图像。 或者，单击&#x200B;**[!UICONTROL 在Adobe Express中编辑]**&#x200B;以自己对图像进行更改。 有关使用Adobe Express优化图像的更多信息，请参阅[Adobe Express中的快速操作](./image-edit-adobe-express.md#quick-actions-in-adobe-express)。

   ![文本变体和细化选项的AI Assistant预览](./assets/email-designer-ai-assistant-image-refine.png){width="700" zoomable="yes"}

   您还可以[提交生成的变体的反馈](#submit-variation-feedback)。

1. 突出显示所需的图像，然后单击&#x200B;**[!UICONTROL 选择]**&#x200B;将图像或占位符替换为选定项，并返回到登陆页设计空间。

   您可以使用画布上的编辑和格式化工具来更改图像，以及右侧的&#x200B;_[!UICONTROL 设置]_&#x200B;和&#x200B;_[!UICONTROL 样式]_&#x200B;选项。

>[!ENDTABS]

## 预览和内容细化 {#refine-finalize}

生成内容变体后，您可以优化结果以确保它们满足您的确切要求。 审查品牌定位，调整语调和语言，并为可审核的草稿准备内容。 您还可以提交变体的反馈，以帮助培训AI Assistant并改进未来输出。

### 打开全屏视图

1. 在初始内容生成后，浏览&#x200B;**[!UICONTROL 变体]**。

1. 识别与您的目标最匹配的变量，然后单击&#x200B;_全屏_ （ ![全屏图标](../assets/do-not-localize/icon-full-screen.svg) ）图标以打开对话框。

   ![访问“生成”对话框](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

1. 如果对所选变量满意，请单击&#x200B;**[!UICONTROL 选择]**&#x200B;以将其应用于画布。

### 优化变体

单击&#x200B;**[!UICONTROL Refine]**&#x200B;选项可访问登陆页面和文本变体的其他自定义功能：

* **[!UICONTROL 精心设计]** - AI助手可以帮助您展开特定主题，提供其他详细信息以便更好地了解和参与。

* **[!UICONTROL 摘要]** — 过长的信息可能会使页面查看者过载。 使用AI Assistant将关键点浓缩为清晰、简洁的摘要，以吸引注意并鼓励他们进一步阅读。

* **[!UICONTROL 重写]** — 重写邮件并保留其含义。 此选项可帮助您在不更改核心消息的情况下生成替代措辞、改善流量或调整词语。

* **[!UICONTROL 使用更简单的语言]** — 简化语言，确保更广受众的清晰度和可访问性。

* **[!UICONTROL 翻译]** — 将文本翻译成其他语言。 （目前，英语是唯一受支持的语言。）

* **[!UICONTROL 更改音调]** — 调整消息音调以符合您的沟通风格，例如，使消息更友好、更专业、更紧急或更具启发性。

* **[!UICONTROL 更改沟通策略]** — 根据您的目标修改消息传送方式，如创建紧迫感或强调令人兴奋的吸引力。

<!-- * **[!UICONTROL Use as reference content]** - Select this option to use the variant as the reference content for generating other results. -->

![细化显示内容细化选项的菜单](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

### 提交变量反馈

通过单击&#x200B;_拇指向上_、_拇指向下_&#x200B;或&#x200B;_标记_&#x200B;图标，为生成的变体提供反馈，并选择最能总结您的反馈的原因。

![AI助手 — 预览生成的变体](./assets/gen-ai-preview-feedback-thumbs-up.png){width="700" zoomable="yes"}

### 检查您的品牌一致性(Beta)

<!-- Are we surfacing scoring here in the future, or will it be a separate post-creation task? 1. Click the percentage icon to view your **[!UICONTROL Brand Alignment Score]** and identify any misalignments with your brand. -->

品牌一致性评估和评分可帮助您确保活动之间的语气、消息传递和视觉身份的一致性，同时在内容上线之前充当质量检查。 完成登陆页面内容后，单击右侧的&#x200B;_品牌对齐方式_ （![品牌对齐方式图标](../assets/do-not-localize/icon-brand-compliance.svg) ）图标，以在登陆页面设计空间中打开&#x200B;_品牌对齐方式_&#x200B;右侧面板。

![访问品牌协调工具](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

有关详细信息，请参阅[验证您的品牌一致性](./brand-alignment.md#validate-your-brand-alignment)
