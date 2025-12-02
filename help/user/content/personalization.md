---
title: 内容个性化
description: 在Journey Optimizer B2B edition中使用帐户、人员和系统令牌个性化B2B电子邮件。 了解如何使用个性化编辑器和语法。
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: 表达式、编辑器、开始、个性化
source-git-commit: 5063f9a924aef0a54b05e9bf223fc2d4898bc5a5
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# 内容个性化 {#add-personalization}

>[!CONTEXTUALHELP]
>id="aj-b2b_personalization"
>title="个性化内容体验"
>abstract="使用&#x200B;**Adobe Journey Optimizer B2B edition**，利用您拥有的关于每个特定收件人的数据和信息调整您的邮件。 它可以是他们的名字、行业、头衔等。"

[!DNL Adobe Journey Optimizer B2B Edition]个性化功能允许您利用有关每个特定收件人的数据和信息，根据他们调整电子邮件。 它可以是他们的名字、行业、头衔等。

使用&#x200B;_个性化编辑器_，您可以选择、排列、自定义和验证所有数据，以便为您的内容创建自定义个性化。 使用各种工具（如辅助函数）定制消息。 编辑器使用基于&#x200B;_Handlebars_&#x200B;的内联个性化语法，其中表达式由双大括号`{{}}`括起来的内容构建。

在处理消息时，Journey Optimizer B2B edition会使用Adobe Experience Platform数据集中包含的数据和本地系统值替换表达式。 例如，`Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`动态变为`Hello John Doe`。

使用此语法，您可以跨多个字段个性化消息，包括电子邮件主题行、消息正文和发件人信息。

## Personalization令牌

在[!DNL Journey Optimizer B2B Edition]中，您可以使用个性化令牌构建动态电子邮件内容：

* **帐户令牌** — 这些令牌基于帐户属性，如&#x200B;_帐户名称_、_行业_&#x200B;和&#x200B;_员工人数_。 使用这些令牌填充由&#x200B;**_XDM业务帐户详细信息_**&#x200B;架构(在Adobe Experience Platform中定义)管理的属性数据。

* **人员令牌** — 这些令牌基于业务人员属性，如&#x200B;_名字_、_职务_&#x200B;和&#x200B;_公司名称_。 使用这些令牌填充由&#x200B;**_XDM业务人员详细信息_**&#x200B;架构管理的属性数据，该架构在Adobe Experience Platform中定义。

* **系统令牌** — 这些令牌基于系统字段值，如&#x200B;_date_、_time_&#x200B;和&#x200B;_取消订阅链接_。

* **我的令牌**（为历程定义时） — 为电子邮件所在的历程[定义的](./personalization-my-tokens.md)自定义令牌。

>[!NOTE]
>
>在[Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home){target="_blank"}中了解有关XDM架构的更多信息。

## Personalization编辑器

个性化编辑器适用于您需要在电子邮件内容中定义个性化的每个上下文。 在编辑器中，您可以选择、排列、自定义和验证所有数据，以创建内容的自定义个性化设置。

通过单击&#x200B;_添加个性化_ （ ![添加个性化图标](../../assets/do-not-localize/icon-personalization-field.svg) ）图标，在任何字段或内容组件中添加个性化。

![Personalization编辑器](./assets/personalization-editor.png){width="800" zoomable="yes"}

>[!NOTE]
>
>以下有关个性化编辑器的信息反映了在[!DNL Journey Optimizer B2B Edition]简化架构[上配置的](../simplified-architecture.md)环境可用的更改。

### 令牌和辅助函数

若要使用个性化令牌或辅助函数，请在左侧导航窗格中找到它，然后单击&#x200B;**+**&#x200B;以将其添加到表达式中。

单击&#x200B;_更多菜单_ (**...** )图标(_添加_ (**+** )图标旁边)以查看每个属性的更多详细信息，并将最常用的属性添加到&#x200B;_收藏夹_。 添加到收藏夹的属性可从编辑器左侧导航栏的&#x200B;**[!UICONTROL 收藏夹]**&#x200B;菜单访问。

![Personalization编辑器 — “令牌更多”菜单](./assets/personalization-editor-token-more-menu.png){width="800" zoomable="yes"}

<!-- >>[!NOTE]
>
>By default, the attributes list shows only populated attributes. To display all attributes, click the _Settings_ icon above the search field and toggle off the **[!UICONTROL Show only populated attributes]** option.
-->
您还可以定义在字符串类型的配置文件属性为空时显示的默认回退文本字符串。 单击属性的&#x200B;_更多菜单_ ( **...** )图标，然后选择&#x200B;**[!UICONTROL 插入后备文本]**。 输入配置文件属性值为空时应显示的文本，然后单击&#x200B;**[!UICONTROL 添加]**。

最佳做法是在将表达式插入内容之前对其进行验证。 单击编辑器底部的&#x200B;**[!UICONTROL 验证]**&#x200B;以检查您的语法并确保没有错误。

![Personalization编辑器已验证代码](./assets/personalization-editor-validated.png){width="500"}

当表达式完成且没有错误时，单击&#x200B;**[!UICONTROL 保存]**。

### 自定义数据集

可以使用关系架构（基于模型的类）进行电子邮件个性化。 自定义对象是在&#x200B;_关系架构_&#x200B;中定义的，产品管理员可以在[中](../admin/xdm-field-management.md#relational-schemas)配置关系架构字段[!DNL Journey Optimizer B2B Edition]。 可在个性化编辑器中访问这些字段。 只有与帐户:M具有一对多(1<!-- (M1.5 Beta) or Person (M1.5 GA) -->)关系的自定义对象才可用。

>[!IMPORTANT]
>
>在将自定义对象用于脚本式个性化之前，请确保查看并了解[Handlebar模板语言](https://handlebarsjs.com/guide/)、[个性化语法](./personalization-syntax.md)和内置[帮助程序函数](./personalization-helper-functions.md)。

使用自定义对象定义个性化时，您可以跨&#x200B;**[!UICONTROL Personalization令牌]**（人员/潜在客户、帐户、系统和我的令牌）以及&#x200B;**[!UICONTROL 基于模型的类]**（关系架构）访问可脚本访问对象中的所有变量。 选择基于模型的类后，可通过单击自定义对象文件夹来查看字段。 对于要将其添加到表达式的每个字段，单击&#x200B;**+**。

![Personalization编辑器 — 基于模型的类 — 添加自定义对象字段](./assets/personalization-editor-custom-object-fields.png){width="800" zoomable="yes"}

<!-- ## Personalization experimentation {#playground}

**[!DNL Adobe Journey Optimizer]** includes an interactive tool designed to help you learn and experiment with personalization capabilities.

This playground provides a simulated environment to write and test personalization code using sample data without requiring live datasets. You can leverage predefined code samples, edit dummy profile payloads, and preview the output of your personalization code in real-time. 

![personalization playground](assets/playground.png)

➡️ [Access the personalization playground](https://experienceleague.adobe.com/en/apps/journey-optimizer/ajo-personalization){target="_blank"} 

## How-to videos{#video-perso}

Learn how to use contextual event information from a journey to personalize a message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Learn how to add profile-based personalization to a message and how to use audience membership as a pre-condition to a personalization block.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Learn how to leverage the personalization editor playground to write and test personalization code using sample data.

>[!VIDEO](https://video.tv.adobe.com/v/3457868?quality=12) -->