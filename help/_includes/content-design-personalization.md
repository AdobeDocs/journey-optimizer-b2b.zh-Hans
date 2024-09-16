---
title: 内容创作 — 个性化
description: 重用有关使用个性化进行内容创作的部分
source-git-commit: 0a9c05ac2ddd95e1fa5321f44f5cbe8cfa595007
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# 内容创作 — 个性化

Journey Optimizer B2B Edition使用内联简单语法，允许您创建包含用双大括号`{}`括起来的个性化内容的表达式。 您可以在同一内容或字段中添加多个表达式，而不受限制。

示例：

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

在处理消息（电子邮件和短信）时，Journey Optimizer B2B Edition会使用Experience Platform数据库中包含的数据替换表达式。 因此，第一个示例变为&#x200B;_Hello John Doe_。

以下示例概述了使用商机/帐户属性和系统令牌对内容进行个性化的步骤。

1. 选择文本组件并单击工具栏中的&#x200B;_添加个性化_&#x200B;图标。

   ![单击“个性化”图标](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   此操作打开&#x200B;_编辑Personalization_&#x200B;对话框。

1. 单击&#x200B;**+**&#x200B;或&#x200B;**...**&#x200B;将令牌添加到空白空间。

   ![使用令牌构造个性化文本](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 保存]**。
