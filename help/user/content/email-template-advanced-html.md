---
title: 用于电子邮件模板设计的高级HTML模式
description: 使用高级HTML模式直接在Journey Optimizer B2B edition的电子邮件设计空间中查看和编辑电子邮件模板内容的原始HTML源。
feature: Email Authoring, Templates, Content Design Tools
level: Experienced
role: User
source-git-commit: 95dba963e08125370f998cf3960d51ede94c2fb9
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# 用于电子邮件模板设计的高级HTML模式

_高级HTML模式_&#x200B;提供了一个视图，通过该视图，经验丰富的用户可以直接查看和编辑电子邮件模板内容的原始源代码。 当您想要将复杂的表达式（如条件逻辑）直接插入源时，此模式非常理想。 对于进行超出可视设计工具所展示范围的结构调整而言，它也很有用。

<!-- We don't have the code editor at this point 
>[!NOTE]
>
>_Advanced HTML mode_ is different from the code editor option that is available when you start a new design. The code editor does not allow you to change to the visual design space. With _advanced HTML mode_, you can toggle back and forth between the HTML source view and the visual design view at any time. -->

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;_有限可用性_&#x200B;中，并非对所有用户都可用。

## 重要限制

在对[电子邮件模板创作](./email-template-authoring.md)使用高级HTML模式之前，请确保您了解以下限制：

* **无验证** — HTML编辑器不执行语法检查或布局验证。 在保存之前，请仔细查看您的代码。

* **内容更新** — 未来的系统更改可能会影响或覆盖在高级HTML模式下对默认标记所做的修改。 在产品更新后检查您的内容，以确保它按预期呈现。

* **有限支持** — Adobe无法对在高级HTML模式下进行自定义代码修改导致的呈现问题或内容错误进行故障诊断。

* **预览限制** — 内容模拟（使用配置文件预览）仅在桌面视图中可用，不能直接从HTML源视图中可用。

### 访问高级HTML模式

在画布中加载电子邮件模板后，可以从可视化设计空间顶部的工具栏访问高级HTML模式。

1. 打开或[创建电子邮件模板](./email-templates.md#create-an-email-template)并打开设计空间以编辑内容。

1. 在设计空间中，单击工具栏中的&#x200B;_[!UICONTROL HTML]_ （ ![HTML图标](../assets/do-not-localize/icon-code.svg) ）图标。

   ![单击电子邮件模板设计空间工具栏中的HTML图标](./assets/email-template-advanced-html-mode-toolbar.png){width="750" zoomable="yes"}

   如果这是您首次打开高级HTML模式（或者已经过去了一个月或更长时间），则会显示警告消息。 查看信息并单击&#x200B;**[!UICONTROL 确定]**&#x200B;以继续。

   ![查看高级HTML模式警告，然后单击“确定”继续](./assets/email-template-html-mode-warning.png){width="500"}

   设计画布将切换到原始HTML源视图。

1. 查看代码并将所需的更改添加到电子邮件内容中。

   在&#x200B;_高级HTML模式_&#x200B;中，您可以直接访问电子邮件模板内容的完整HTML源：

   * 查看和修改原始HTML标记的任何部分。
   * 将高级[个性化表达式](./personalization.md)直接插入源。
   * 使用表达式语法添加[条件内容](./conditional-content.md)逻辑。
   * 添加自定义的HTML属性、跟踪标记或其他通过可视编辑器控件不可用的标记。

   ![具有电子邮件内容原始HTML源的高级HTML模式](./assets/email-template-advanced-html-mode.png){width="800" zoomable="yes"}

   >[!IMPORTANT]
   >
   >确保输入正确的HTML和CSS代码；Adobe不提供语法验证或自定义代码支持。

   出于兼容性原因，内容模拟和保存在高级HTML模式下不可用。 您可以切换回桌面视图以预览内容并保存模板。 在HTML源视图和可视设计视图之间切换时，所做的任何编辑都会保留。

   当您处于高级HTML模式时，如果单击右上方的&#x200B;**[!UICONTROL 保存]**&#x200B;或&#x200B;**[!UICONTROL 保存并关闭]**，将显示一个警告对话框，通知您必须在保存模板并退出设计空间之前退出高级HTML模式。

   ![在高级HTML模式下已禁用保存的警报对话框](./assets/email-template-advanced-html-save-disabled-alert.png){width="500"}

1. 单击工具栏中的&#x200B;_[!UICONTROL 桌面]_ （![桌面图标](../assets/do-not-localize/icon-desktop-spectrum-1.svg) ）图标，从高级HTML模式（HTML源视图）切换到可视化设计画布。

   切换视图时，将保留所做的编辑。
