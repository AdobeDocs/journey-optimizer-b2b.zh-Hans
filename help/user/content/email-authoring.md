---
title: 电子邮件创作
description: 了解如何在Adobe Journey Optimizer B2B中创建电子邮件内容。 使用模板、HTML导入和AI支持的工具来个性化和优化电子邮件通信。
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 47b032788d182da7306f3d855d87162cd43afd34
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 14%

---

# 电子邮件创作

在您[将新的<!-- or duplicated -->电子邮件资产添加到历程操作节点](./add-email.md)后，您可以定义电子邮件的内容。

在右侧面板的&#x200B;**[!UICONTROL 详细信息]**&#x200B;选项卡中单击&#x200B;_[!UICONTROL 编辑电子邮件内容]_。

![单击“编辑电子邮件内容”](./assets/add-email-content.png){width="700" zoomable="yes"}

此操作将启动电子邮件设计工具，您可以在其中从以下选项中选择所需的电子邮件设计方式：

* [使用Designer电子邮件界面从头开始设计电子邮件](#design-your-email-from-scratch)。

* [从文件或.zip文件夹导入现有HTML内容](#import-existing-html-content)。

* [从内置或自定义电子邮件模板列表中选择现有模板](#select-a-template)。

创建并个性化电子邮件内容后，可导出内容以供验证或稍后使用。 单击&#x200B;**[!UICONTROL 导出HTML]**，将内容保存为.zip文件，其中包括您的HTML和资源。

>[!TIP]
>
>使用由generative AI提供支持的Adobe Journey Optimizer B2B edition中的AI助手，将您的内容提升到新的级别。 AI Assistant可以帮助您优化投放的影响，方法是生成整个电子邮件、提供有针对性的文本内容，并为可与受众产生共鸣的图像获取AI Assistant推荐。 [了解详情](./ai-assistant-emails.md)

## 从头开始设计您的电子邮件 {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="添加结构组件"
>abstract="结构组件定义登陆页面的版面。拖放&#x200B;**结构**&#x200B;组件到画布中，开始设计您的登陆页面内容。"

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="关于内容组件"
>abstract="内容组件是空的内容占位符，您可用它来创建登陆页面的版面。"

使用可视内容设计空间来定义电子邮件的结构和内容。 通过简单的拖放操作添加和移动结构组件，您可以在几秒钟内设计可重用电子邮件内容的形状。

1. 从&#x200B;_[!UICONTROL 设计您的模板]_&#x200B;主页中，选择&#x200B;**[!UICONTROL 从头开始设计]**&#x200B;选项。
1. [向电子邮件添加结构和内容](#add-structure-and-content)。
1. [将图像资源](#add-assets)添加到电子邮件中。
1. [个性化电子邮件内容](#personalize-content)。
1. [审阅并更新链接](#preview-and-edit-linked-urls)。
1. [测试电子邮件](#check-and-test-the-email)。

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

如果对内容满意，请单击&#x200B;**[!UICONTROL 保存]**。

## 导入现有HTML内容

{{$include /help/_includes/content-design-import.md}}

![在zip文件中导入html内容](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>在HTML文件中使用`<table>`标记作为第一层可能会导致样式丢失，包括顶层标记中的背景和宽度设置。

您可以根据需要使用可视电子邮件编辑器工具个性化导入的内容。

## 选择模板

{{$include /help/_includes/content-design-select-template.md}}

>[!NOTE]
>
> 保存的模板可能已将管理（内容锁定）设置应用于一个或多个组件。 当您[从受控制的模板](./email-authoring-governance.md)创作电子邮件时，可视设计器提供了有关锁定的组件的准则。

## 添加结构和内容 {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="添加结构组件"
>abstract="结构组件定义电子邮件的版面。将&#x200B;**结构**&#x200B;组件拖放到画布中，开始设计您的电子邮件内容。"

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="关于内容组件"
>abstract="内容组件是空的内容占位符，您可用它来创建电子邮件的版面。"

{{$include /help/_includes/content-design-components.md}}

### 添加自定义 CSS

您可以直接在电子邮件设计空间中添加自己的自定义CSS。 使用自定义CSS可应用高级和特定的样式，以便更加灵活地控制内容的外观。 最好在包含图像、按钮和文本等组件之前添加此最高级别的样式。

如果画布中至少有一个内容组件，请选择左侧导航树中的&#x200B;**[!UICONTROL Body]**&#x200B;组件以访问自定义CSS编辑器。

>[!NOTE]
>
>如果您的电子邮件是使用包含锁定内容[的](./template-content-governance.md)模板设计的，则无法向内容添加自定义CSS。 按钮标签更改为&#x200B;**[!UICONTROL 查看自定义CSS]**，内容中已存在的任何自定义CSS均为只读。

![访问正文样式](./assets/email-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### 添加片段

{{$include /help/_includes/content-design-use-fragments.md}}

保存电子邮件后，当您在摘要中选择&#x200B;_[!UICONTROL 使用者]_&#x200B;选项卡时，该电子邮件会显示在片段详细信息页面中。

### 添加资源

{{$include /help/_includes/content-design-assets.md}}

### 导航图层、设置和样式

{{$include /help/_includes/content-design-navigation.md}}

### 个性化内容

{{$include /help/_includes/content-design-personalization-email.md}}

>[!NOTE]
>
>如果为帐户历程定义了&#x200B;_[!UICONTROL 我的令牌]_，则还可以将这些特定于历程的令牌用于电子邮件内容。 有关详细信息，请参阅电子邮件个性化的[自定义令牌](./personalization-my-tokens.md)。

### 编辑链接的URL跟踪

{{$include /help/_includes/content-design-links.md}}

### 查看选项

利用可视电子邮件编辑器中提供的视图和内容验证选项。

* 通过预设缩放选项放大/缩小内容。

* 切换在桌面、移动设备或纯文本/纯文本中查看内容。
   * 单击&#x200B;_查看_&#x200B;图标可跨设备预览内容。
   * 选择一个现成的设备或输入自定义维度以预览内容。

## 更多选项

从电子邮件设计空间顶部的&#x200B;_[!UICONTROL 更多……]_&#x200B;菜单中，可以执行以下操作：

![单击“更多”以访问模板操作](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL 重置电子邮件]** — 单击此选项可将可视电子邮件设计器画布清除为空白并重新启动内容生成。
* **[!UICONTROL 另存为片段]** — 将电子邮件的全部或部分另存为片段，以便在多个电子邮件或电子邮件模板中重复使用。 您可以提供片段的名称和描述，并将其保存到可用片段列表中。
* **[!UICONTROL 更改您的设计]** — 返回&#x200B;_设计您的电子邮件_&#x200B;页面。 从那里，您可以选择另一个模板以重新启动设计过程，或者选择在黑色画布中从头开始设计内容。\
* **[!UICONTROL 另存为内容模板]** — 将电子邮件正文另存为电子邮件模板，以便在多个电子邮件或电子邮件模板中重复使用。 您可以提供模板的名称和描述，并将其保存到已保存电子邮件模板的列表中。
* **[!UICONTROL 导出HTML]** — 将可视画布中的内容以HTML格式下载到您的本地系统，并打包为zip文件。

## 检查并测试电子邮件 {#email-testing}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="检查您的内容的渲染方式"
>abstract="定义内容后可预览它，并根据所使用的渠道检查渲染是否正确。"

定义消息内容后，您可以使用测试用户档案进行预览、发送校样以及查看其在桌面和移动设备宽高比中的呈现方式。 如果插入个性化内容，则可以使用测试用户档案数据预览此内容在消息中的显示方式。

要[预览电子邮件内容](./email-simulate-content.md)，请单击&#x200B;**[!UICONTROL 模拟内容]**，然后选择一个测试个人资料以使用人员个人资料数据检查您的邮件。

![模拟电子邮件内容以检查您的设计](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}

您可以访问其他工具来验证和查看电子邮件内容：

* [发送验证](./email-simulate-content.md#send-proofs)
* [测试电子邮件客户端中的渲染](./email-test-rendering.md)
<!-- * Generate a spam report -->
