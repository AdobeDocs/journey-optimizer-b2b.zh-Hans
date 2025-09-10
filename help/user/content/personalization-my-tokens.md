---
title: 电子邮件Personalization的自定义令牌
description: 创建和管理用于动态电子邮件个性化的自定义我的令牌 — 在Journey Optimizer B2B edition中为帐户历程定义文本和数字变量。
feature: Personalization, Content, Email Authoring
role: User
exl-id: 05d4f446-6348-4555-9c46-316c2857f01d
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 2%

---

# 电子邮件个性化的自定义令牌

内容个性化使用令牌作为生成内容工件时填充的占位符或变量。 标准个性化令牌可用于电子邮件、登陆页面、片段和模板。 您还可以使用特定于帐户历程的值定义一组自定义令牌。 这组自定义令牌称为&#x200B;_我的令牌_，其中的任何自定义令牌均适用于[创作历程电子邮件](./email-authoring.md#content-authoring---personalization)时的个性化。

除了特定于帐户历程的&#x200B;_我的令牌_&#x200B;之外，您还可以使用任何用于电子邮件个性化的标准（内置）令牌。

## 管理我的令牌 {#my-tokens}

_我的令牌_&#x200B;是您为处于草稿状态的帐户历程创建或修改的自定义变量。 此自定义令牌集当前支持文本和数字令牌定义。

向电子邮件添加自定义令牌时，会显示为`{{my.TokenName}}`。 例如，您可能创建了`{{my.EventDate}}`或`{{my.WebinarSpeaker}}`个令牌以管理与即将召开的网络研讨会相关的电子邮件内容。

要访问帐户历程&#x200B;:_的自定义令牌(_T)

1. 打开草稿帐户历程。

1. 单击右上方的&#x200B;**[!UICONTROL 更多……]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 我的令牌]**。

   ![单击右上角的“更多”](../journeys/assets/account-journey-draft-more-menu.png){width="450"}

   _我的令牌_&#x200B;页面列出了为历程定义的所有自定义令牌。

   ![我的令牌](./assets/my-tokens-list-page.png){width="700" zoomable="yes"}

### 创建令牌

1. 在&#x200B;_[!UICONTROL 我的令牌]_&#x200B;页面中，单击&#x200B;**[!UICONTROL 创建]**，然后选择要定义的令牌类型：

   * **[!UICONTROL 文本]** — 使用此类型定义具有基本文本字符串值的令牌。

   * **[!UICONTROL 数字]** — 使用此类型定义具有数字值的令牌。

1. 在对话框中，输入令牌的&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 值]**。

   ![输入文本令牌的名称和值](./assets/my-tokens-create-text-token-dialog.png){width="400"}

   令牌名称中不能使用空格或特殊字符。 您可以使用&#x200B;_驼峰式大小写_（如`EventType`）来使用易于识别的多词名称。

   如果要定义&#x200B;_数字_&#x200B;令牌，该值只能包含数字字符。 您可以使用十进制值。

   ![输入数字令牌的名称和值](./assets/my-tokens-create-number-token-dialog.png){width="400"}

1. 单击&#x200B;**[!UICONTROL 添加]**。

### 编辑令牌

虽然帐户历程仍处于草稿状态，但您可以编辑任何定义的“我的令牌”。

1. 在&#x200B;_[!UICONTROL 我的令牌]_&#x200B;页面中，单击令牌名称旁边的&#x200B;_更多操作_&#x200B;图标(**...**)，然后选择&#x200B;**[!UICONTROL 编辑]**。

   ![令牌更多操作菜单](./assets/my-tokens-more-actions.png){width="430"}

1. 在对话框中，根据需要更改历程的&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 值]**。

   ![更改令牌的名称和值](./assets/my-tokens-edit-text-token-dialog.png){width="400"}

1. 单击&#x200B;**[!UICONTROL 编辑]**。

### 删除令牌

您可以从&#x200B;_我的令牌_&#x200B;列表中删除自定义令牌，但您应确保历程电子邮件内容当前未使用该令牌。

1. 在&#x200B;_[!UICONTROL 我的令牌]_&#x200B;页面中，单击令牌名称旁边的&#x200B;_更多操作_&#x200B;图标(**...**)，然后选择&#x200B;**[!UICONTROL 删除]**。

1. 在确认对话框中单击&#x200B;**[!UICONTROL 删除]**。

## 在内容中使用自定义令牌

在为帐户历程创作电子邮件内容时，您可以在可视化设计空间中使用个性化工具时，使用&#x200B;_我的令牌_&#x200B;列表中的任意令牌。

1. 选择文本组件，然后单击工具栏中的&#x200B;_添加个性化_ （ ![添加个性化图标](../../assets/do-not-localize/icon-personalization-field.svg) ）图标。

   ![单击“添加个性化”图标](./assets/email-personalize-text.png){width="600"}

   此操作打开&#x200B;_编辑Personalization_&#x200B;对话框。 如果为帐户历程定义了自定义令牌，则该对话框在&#x200B;_[!UICONTROL Personalization令牌]_&#x200B;库中包含一个&#x200B;_[!UICONTROL 我的令牌]_&#x200B;文件夹。

1. 展开&#x200B;**[!UICONTROL 我的令牌]**&#x200B;文件夹，然后单击&#x200B;**+**&#x200B;或&#x200B;**...**&#x200B;以向空格中添加一个自定义令牌。

   您可以根据需要添加任何其他静态文本。

   ![使用“我的令牌”构造个性化文本](./assets/personalization-edit-dialog-my-tokens.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 保存]**。
