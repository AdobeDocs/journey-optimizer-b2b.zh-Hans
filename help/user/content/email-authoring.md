---
title: 电子邮件创作
description: 了解如何创建在帐户历程中使用的个性化电子邮件内容。
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 797d049cc5aefe710a39a980107f63e75cae12d2
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 11%

---

# 电子邮件创作

使用Adobe Journey Optimizer B2B edition向客户发送电子邮件。 您可以在可视设计器中创建、个性化和预览消息。

## 在帐户历程中添加电子邮件操作

在添加&#x200B;_[!UICONTROL Take an action]_&#x200B;历程并执行以下操作时，可以在Account节点中设置电子邮件投放：

1. 对于&#x200B;_目标上的_&#x200B;操作，请选择&#x200B;**[!UICONTROL 人员]**。
1. 若要对人员&#x200B;_执行_&#x200B;操作，请选择&#x200B;**[!UICONTROL 发送电子邮件]**。
1. 对于&#x200B;_[!UICONTROL 电子邮件源]_，请选择&#x200B;**[!UICONTROL 新建电子邮件]**。

   或者，您还可以选择&#x200B;_[!UICONTROL 从Adobe Marketo Engage中选择电子邮件]_&#x200B;选项，以使用Marketo Engage中预先编写的电子邮件之一，并将其作为帐户历程的一部分发送。

   >[!NOTE]
   >
   >如果您是首次创建电子邮件，请确保已在Adobe Marketo Engage中配置电子邮件渠道。 要了解更多信息，请参阅Marketo Engage文档中的[确保电子邮件可投放性](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability)。

   ![执行操作 — 发送电子邮件](assets/journey-node-send-email.png){width="700" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 执行操作]_&#x200B;面板的底部，单击&#x200B;**[!UICONTROL 创建电子邮件]**。

1. 在对话框中，为电子邮件输入唯一的&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 主题行]**。

   ![新建电子邮件对话框](assets/create-new-email.png){width="400"}

1. 单击&#x200B;**[!UICONTROL 创建]**。

   在电子邮件内容页面的&#x200B;_[!UICONTROL 电子邮件属性]_&#x200B;部分中，_[!UICONTROL 发件人电子邮件]_&#x200B;和&#x200B;_[!UICONTROL 回复地址]_&#x200B;字段已配置。 您可以为&#x200B;_[!UICONTROL From name]_&#x200B;和&#x200B;_[!UICONTROL Description]_（可选）字段输入值。

## 创建电子邮件内容

单击&#x200B;_[!UICONTROL 电子邮件]_&#x200B;预览面板顶部的&#x200B;**[!UICONTROL 添加电子邮件内容]**。

![单击“添加电子邮件内容”](./assets/add-email-content.png){width="700" zoomable="yes"}

此操作将启动电子邮件Designer，您可以在其中从以下选项中选择所需的电子邮件设计方式：

* [使用Designer电子邮件界面从头开始设计电子邮件](#design-your-email-from-scratch)。

* [从文件或.zip文件夹导入现有HTML内容](#import-existing-html-content)。

* [从内置或自定义电子邮件模板列表中选择现有模板](#select-a-template)。

要使用表达式编辑器配置和个性化主题行，请单击&#x200B;_Personalization_&#x200B;图标并添加任何Marketo Engage令牌。

创建并个性化电子邮件内容后，可导出内容以供验证或稍后使用。 单击&#x200B;**[!UICONTROL 导出HTML]**，将内容保存为.zip文件，其中包括您的HTML和资源。

>[!TIP]
>
>使用由generative AI提供支持的Adobe Journey Optimizer B2B edition中的AI助手，将您的内容提升到新的级别。 AI Assistant可以帮助您优化投放的影响，方法是生成整个电子邮件、提供有针对性的文本内容，并为可与受众产生共鸣的图像获取AI Assistant推荐。 [了解详情](./ai-assistant-emails.md)

### 从头开始设计您的电子邮件 {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="添加结构组件"
>abstract="结构组件定义登陆页面的版面。拖放&#x200B;**结构**&#x200B;组件到画布中，开始设计您的登陆页面内容。"

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="关于内容组件"
>abstract="内容组件是空的内容占位符，您可用它来创建登陆页面的版面。"

使用可视内容编辑器定义电子邮件内容的结构。 通过简单的拖放操作添加和移动结构组件，您可以在几秒钟内设计可重用电子邮件内容的形状。

1. 从&#x200B;_[!UICONTROL 设计您的模板]_&#x200B;主页中，选择&#x200B;**[!UICONTROL 从头开始设计]**&#x200B;选项。

1. [向电子邮件添加结构和内容](#add-structure-and-content)。
1. [将图像资源](#add-assets)添加到电子邮件中。
1. [个性化电子邮件内容](#personalize-content)。
1. [审阅并更新链接](#preview-and-edit-linked-urls)。

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

内容完成后，单击顶部的&#x200B;**[!UICONTROL 模拟内容]**&#x200B;以检查渲染。 您可以选择桌面视图或移动设备视图。

如果对内容满意，请单击&#x200B;**[!UICONTROL 保存]**。

### 导入现有HTML内容

{{$include /help/_includes/content-design-import.md}}

![在zip文件中导入html内容](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>在HTML文件中使用`<table>`标记作为第一层可能会导致样式丢失，包括顶层标记中的背景和宽度设置。

您可以根据需要使用可视电子邮件编辑器工具个性化导入的内容。

### 选择模板

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

### 添加片段

{{$include /help/_includes/content-design-use-fragments.md}}

保存电子邮件后，当您在摘要中选择&#x200B;_[!UICONTROL 使用者]_&#x200B;选项卡时，该电子邮件会显示在片段详细信息页面中。

### 添加资源

{{$include /help/_includes/content-design-assets.md}}

### 导航图层、设置和样式

{{$include /help/_includes/content-design-navigation.md}}

### 使内容个性化

{{$include /help/_includes/content-design-personalization.md}}

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

### 更多选项

从电子邮件设计器顶部的&#x200B;_[!UICONTROL 更多……]_&#x200B;菜单中，可以执行以下操作：

![单击“更多”以访问模板操作](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL 重置电子邮件]** — 单击此选项可将可视电子邮件设计器画布清除为空白并重新启动内容生成。
* **[!UICONTROL 另存为片段]** — 将电子邮件的全部或部分另存为片段，以便在多个电子邮件或电子邮件模板中重复使用。 您可以提供片段的名称和描述，并将其保存到可用片段列表中。
* **[!UICONTROL 更改您的设计]** — 返回&#x200B;_设计您的电子邮件_&#x200B;页面。 从那里，您可以选择另一个模板以重新启动设计过程，或者选择在黑色画布中从头开始设计内容。\
* **[!UICONTROL 另存为内容模板]** — 将电子邮件正文另存为电子邮件模板，以便在多个电子邮件或电子邮件模板中重复使用。 您可以提供模板的名称和描述，并将其保存到已保存电子邮件模板的列表中。
* **[!UICONTROL 导出HTML]** — 将可视画布中的内容以HTML格式下载到您的本地系统，并打包为zip文件。

## 检查警报

在设计电子邮件内容时，如果缺少关键设置，则会在界面（页面右上方）中显示警报。

如果未看到此按钮，则表示没有检测到问题。

可以检测到两种类型的警报：

* 引用推荐和最佳实践的&#x200B;**_警告_**，例如：

   * `The opt-out link is not present in the email body`：最佳做法是在电子邮件正文中添加退订链接。

     >[!NOTE]
     >
     >营销风格的电子邮件必须包含选择退出链接，这对于事务型消息不是必需的。

   * `Text version of HTML is empty`：别忘了定义电子邮件正文的文本版本，此文本版本在HTML内容无法显示时使用。

   * `Empty link is present in email body`：检查电子邮件中的所有链接是否正确。

   * `Email size has exceeded the limit of 100KB`：要获得最佳投放，请确保电子邮件大小不超过100KB。

* **_错误_**，阻止您测试或激活历程/营销活动，只要未解决这些错误，例如：

   * `The subject line is missing`：电子邮件主题行是必填的。

   * `The email version of the message is empty`：尚未配置电子邮件内容时显示此错误。

## 检查并测试电子邮件 {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="检查您的内容的渲染方式"
>abstract="定义内容后可预览它，并根据所使用的渠道检查渲染是否正确。"

定义消息内容后，您可以使用测试用户档案来预览、发送校样，并控制它在常用桌面、移动和基于Web的客户端中的呈现。 如果插入个性化内容，则可以使用测试用户档案数据预览此内容在消息中的显示方式。

若要预览电子邮件内容，请单击“模拟内容”**&#x200B;**，然后添加测试用户档案，以使用测试用户档案数据检查邮件。

![模拟电子邮件内容以检查您的设计](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
