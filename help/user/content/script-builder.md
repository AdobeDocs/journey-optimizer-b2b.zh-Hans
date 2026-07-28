---
title: 脚本生成器
description: 使用Script Builder（电子邮件设计空间中支持AI的助手）生成Handlebars个性化脚本并转换Journey Optimizer B2B edition中的Marketo Engage Velocity脚本。
feature: AI Assistant, Generative AI, Personalization, Email Authoring
role: User, Developer
badgeBeta: label="Beta 版" type="informative" tooltip="此功能当前为有限测试版"
autotag-review: '2026-07-27T16:18:02.498Z'
TQID: 'https://experienceleague.adobe.com/JWnXAAbCuZVLv4ZhWubpNsZ61xbYU7xtdOXkG9uoWis'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: bd3c685c-6c92-4a4a-becb-535cc25215de
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0004f8fba0c3d4ae89063418e4d3ef8fea22b0c3
workflow-type: tm+mt
source-wordcount: 1074
ht-degree: 2%

---

# 脚本生成器

_脚本生成器_&#x200B;是[!DNL Adobe Journey Optimizer B2B Edition]电子邮件设计空间中可用的AI支持的助手。 它有助于营销人员和电子邮件开发人员更快地创建个性化脚本，并通过将现有个性化逻辑转换为[!DNL Journey Optimizer B2B Edition]来帮助从[!DNL Marketo Engage]迁移，而无需手动重写代码。

>[!AVAILABILITY]
>
>当前，脚本生成器仅在&#x200B;**_帐户历程_**&#x200B;中作为受限测试版提供给选择客户。 计划在将来的版本中支持人员历程。 要获取访问权限，请联系您的Adobe代表。

构建条件电子邮件个性化需要创作&#x200B;_Handlebars_&#x200B;表达式，例如按区域设置切换语言块、按区域或角色交换内容，或者插入动态配置文件或自定义对象值。 如果从[!DNL Marketo Engage]迁移，您会面临一个附加的挑战：逐行重写&#x200B;_Velocity_&#x200B;脚本。 Script Builder从单个对话界面中解决了这两个障碍：

* 从纯语言描述生成新的Handlebars个性化脚本。
* 粘贴[!DNL Marketo Engage] Velocity脚本并将其转换为具有自动令牌映射的等效Handlebars脚本。
* 预览、编辑、验证输出并将其直接保存到电子邮件中，而无需在工具之间复制和粘贴。

## 准则和限制

>[!IMPORTANT]
>
>用户对Script Builder的访问通过[!DNL Journey Optimizer B2B Edition]中其他生成AI功能使用的相同权限进行控制。 有关授予功能权限的信息，请参阅[启用AI助手访问](../ai-assistant/enable-ai-assistant-access.md)。

在使用脚本生成器之前，请查看适用于[!DNL Journey Optimizer B2B Edition]中的创作AI功能的[准则和限制](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations)。 [在使用AI功能之前，还需要用户同意](https://www.adobe.com/cn/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}。

熟悉[!DNL Journey Optimizer B2B Edition]支持的[Handlebars模板语言](https://handlebarsjs.com/guide/){target="_blank"}、[个性化语法](./personalization-syntax.md)和[辅助函数](./personalization-helper-functions.md)。 脚本生成器会为您生成有效的Handlebars，但了解语法可帮助您满怀信心地查看和编辑输出。

## 打开脚本生成器 {#open-script-builder}

当您[为帐户历程](./email-authoring.md)创作电子邮件内容[时，可通过个性化编辑器](./personalization.md)使用脚本生成器。

1. 在电子邮件设计空间中，选择要添加或替换个性化脚本的组件。

1. 要打开个性化编辑器，请单击&#x200B;_添加个性化_ （ ![添加个性化图标](../../assets/do-not-localize/icon-personalization-field.svg) ）图标。

1. 在编辑器中，选择&#x200B;**[!UICONTROL 脚本生成器]**。

   ![Personalization编辑器 — 选择脚本生成器](./assets/personalization-script-builder-select.png){width="700" zoomable="yes"}

   >[!BEGINSHADEBOX]

   首次访问脚本生成器时，请查看[_[!UICONTROL 创作AI使用条款&#x200B;]_](https://www.adobe.com/cn/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}并确认您的协议。

   ![脚本生成器中的创作AI使用条款协议对话框](./assets/personalization-script-builder-gen-ai-terms.png){width="400"}

   >[!ENDSHADEBOX]

   将打开Script Builder面板，其中包含对话式聊天界面。

   ![Personalization编辑器 — Script Builder面板](./assets/personalization-script-builder-welcome.png){width="700" zoomable="yes"}

1. 根据您想要执行的操作开始聊天：

   * [生成新脚本](#generate-personalization-script)
   * [转换现有的Velocity脚本](#convert-marketo-velocity-script)

## 生成个性化脚本 {#generate-personalization-script}

使用脚本生成器从纯语言描述创建新的Handlebars个性化脚本，而无需自己编写表达式。

脚本生成器包含一个映射库，该映射库根据为您的组织定义的[XDM字段映射](../admin/xdm-field-management.md)，将[!DNL Marketo Engage]潜在客户和帐户字段解析为等效的[!DNL Journey Optimizer B2B Edition]个XDM配置文件属性。

1. 在Script Builder聊天界面中，描述所需的个性化逻辑。

   例如，描述用于确定要显示的内容变体的属性、自定义对象或条件。

1. 在预览窗格中查看生成的Handlebars脚本。

1. 如果要优化逻辑或措辞，请直接在预览窗格中编辑脚本。

1. 单击&#x200B;**[!UICONTROL 验证]**&#x200B;以根据[!DNL Journey Optimizer B2B Edition]架构检查脚本。

   在保存脚本之前，验证会捕捉到语法错误和未解析的令牌引用，以便损坏的个性化不会发布到实时电子邮件。

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;将脚本直接插入到电子邮件中的选定位置。

## 转换Marketo Engage Velocity脚本 {#convert-marketo-velocity-script}

使用脚本生成器将现有[!DNL Marketo Engage] Velocity脚本迁移到[!DNL Journey Optimizer B2B Edition]的对等Handlebars脚本中。

1. 在脚本生成器聊天中，输入`Convert this`并粘贴要转换的Velocity脚本。

   脚本生成器解析Velocity构造，将令牌引用与XDM配置文件属性匹配，并生成等效的Handlebars脚本。

1. 查看[转化报表](#review-conversion-report)和[解析需要手动映射](#resolve-tokens-without-mapping)的所有令牌。

1. [预览并验证](#preview-validate-script)生成的脚本，然后将其直接保存到电子邮件中。

### 支持的Velocity结构 {#supported-velocity-constructs}

脚本生成器将以下[!DNL Marketo Engage]个Velocity控制流构造转换为等效的Handlebars或条件内容表达式：

| 速度结构 | Handlebars或条件内容等效项 |
| ------------------- | --------------------------------------------- |
| `#if` / `#elseif` / `#else` | Handlebars `{{#if}}`、`{{else if}}`和`{{else}}`块帮助程序或[!DNL Journey Optimizer B2B Edition] [条件内容](./conditional-content.md)规则 |
| `#set` | 生成的脚本中的Handlebars变量分配 |

它将基于区段的条件逻辑转换为[条件内容](./conditional-content.md)规则，以复制分支行为，包括具有多个语言变体块的电子邮件。

如果Velocity构造没有直接的Handlebars或等效的条件内容，则脚本生成器将在[转化报表](#review-conversion-report)中标记该构造，而不是生成不完整或不正确的表达式。

### 查看转化报表 {#review-conversion-report}

每次转换后，Script Builder都会显示一个结构化报表，其中列出：

* 已成功映射的令牌。
* 需要手动解析的令牌。
* Velocity构造没有等效的Handlebars。

使用报告确认转换已完成，然后再解析任何剩余的令牌并保存脚本。

### 解析没有映射的令牌 {#resolve-tokens-without-mapping}

对于映射库中没有的令牌（如自定义潜在客户属性或自定义[!DNL Marketo Engage]对象），脚本生成器会尝试按以下顺序解析映射：

1. 它基于可用的XDM字段和为自定义对象配置的基于模型的[类](./personalization.md#custom-datasets)建议可能的映射，当存在可靠匹配时。

1. 如果不能提供可信的匹配项，则会在聊天中询问您正确的映射。

当您确认库中没有的令牌的映射时，脚本生成器会询问您是否要记住该决策。 如果您同意，将记住源[!DNL Marketo Engage]实例的映射，该映射由其Munchkin ID标识，这样当您下次从该实例转换脚本时，将自动解析同一令牌。

### 预览和验证脚本 {#preview-validate-script}

在提交转换之前，Script Builder会并排显示原始Velocity脚本和生成的Handlebars输出的预览，其中具有内联编辑支持。 使用预览可比较两个版本，并直接在生成的脚本中进行任何调整。

单击&#x200B;**[!UICONTROL 验证]**&#x200B;以根据[!DNL Journey Optimizer B2B Edition]架构检查生成的Handlebars。 保存后会再次运行验证，这样损坏的个性化就不会发布到实时电子邮件。

如果对结果满意，请单击&#x200B;**[!UICONTROL 保存]**&#x200B;将脚本直接插入到电子邮件中的所选位置。

<!--
### Save reusable conversion profiles {#save-reusable-conversion-profiles}

Save your field mappings and segment mappings as a reusable conversion profile so that your token schema does not need to be re-entered for each script or migration batch. Select a saved profile at the start of a conversion to apply its mappings automatically.

### Audit logs {#conversion-audit-logs}

Script Builder records an audit log for every conversion event, including which scripts were processed, which tokens were remapped, which tokens required manual intervention, and who approved the final output. Use the audit log to review migration activity across your organization.

-->
