---
title: 内容创作 — 个性化
description: 重用有关使用个性化进行内容创作的部分
source-git-commit: d67f44419e09693ec93fd4db7982ec59c672b633
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 1%

---

# 内容创作 — 个性化

Journey Optimizer B2B edition使用内联简单语法，允许您创建包含用大括号`{}`括起来的个性化内容的表达式。 您可以在同一内容或字段中添加多个表达式，而不受限制。

示例：

* `Hello {{lead.firstName}} {{lead.lastName}}`
* `Hello {%= lead.mktoName ?: "Marketer" %}`

>[!NOTE]
>
>Journey Optimizer B2B edition现在在电子邮件中遵循个性化令牌的&#x200B;_驼峰式大小写_&#x200B;语法，以匹配其他Adobe Experience Platform应用程序以获得一致的体验。 此令牌格式与[Handlebars模板语言](https://handlebarsjs.com/guide/#what-is-handlebars){target="_blank"}完全兼容。 在此更改之前添加的任何令牌都会自动更新。

处理内容时，Journey Optimizer B2B edition会将表达式替换为Experience Platform数据库中包含的数据。 因此，第一个示例变为&#x200B;_Hello John Doe_。

以下示例概述了使用商机/帐户属性和系统令牌对内容进行个性化的步骤。

1. 选择文本组件并单击工具栏中的&#x200B;_添加个性化_&#x200B;图标。

   ![单击“个性化”图标](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   此操作打开&#x200B;_编辑Personalization_&#x200B;对话框。

1. 通过单击令牌旁边的加号( **+**)符号添加令牌。

   如果要添加带有回退的令牌（当该字段不可用于潜在客户时显示的默认文本），请单击&#x200B;_更多_&#x200B;图标( **...**)，然后选择&#x200B;**[!UICONTROL 插入带有回退文本]**。

   ![使用令牌构造个性化文本](../assets/content-design-shared/visual-designer-personalize-dialog-handlebar.png){width="700" zoomable="yes"}

1. 添加任何其他要包含的令牌或其他静态文本。

1. 单击&#x200B;**[!UICONTROL 保存]**。

   个性化脚本显示在可视设计空间中。 您可以选择它以在需要时进行更改。

   ![选择个性化脚本](../assets/content-design-shared/visual-designer-select-personalization-script.png){width="600"}
