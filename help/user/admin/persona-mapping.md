---
title: 角色映射
description: 了解如何为B2B营销设置角色映射。 在Journey Optimizer B2B edition中映射人员属性以创建角色模板并优化购买群组定位。
feature: Setup, Buying Groups
role: Admin
source-git-commit: 278add74cc8d1aedd7809fd4675627f26501b0df
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# 人物角色映射

角色是基于帐户的营销(ABM)方法中的关键方面，因为它们帮助营销人员根据目标帐户中个人的特定需求、偏好和棘手问题调整其策略。 营销人员可以为每个角色创建详细的配置文件，包括其背景、职责、棘手问题和首选通信渠道。 借助这些定义，管理员可以根据Journey Optimizer B2B edition中的人员属性配置角色，以便角色模板可以使用简化且一致的角色条件来捕获这些角色。

<!-- Currently there is no insight into what persona goes into what role. With buying group agent, when asked questions about, what should be the size of the buying group, what persona should be in that buying group, what role do they play, etc, then agent will analyze all the data, (opportunity data, engagement data, sales conversation, etc) and informs the user that the buying group needs 7 persona, e.g.CMO, VP of marketing, marketing leader, Marketing ops, etc. 

Then based on what agent informed, users can create a template with those personas. -->
角色定义和使用限制：

* 您最多可以在&#x200B;_[!UICONTROL 角色映射]_&#x200B;列表中定义20个角色。
* 每个角色在其定义中最多可以包含五个属性。
* 在所有定义的角色中，您最多可以使用10个不同的人员属性。

>[!BEGINSHADEBOX]

**用例：职务变体**

许多营销和销售团队使用职称作为识别帐户中不同角色的一种方式。 但联系人的标题可能会不一致，并且会为类似角色使用大量变体。 在构建购买组角色模板时，可能会要求您为给定角色定义每个可能的相关职务。 您可以简化这些定义，并将具有类似职称的人员归入一个推断的角色下，然后您可以跨不同的角色模板利用这一角色来购买组。

例如，您可以配置名为&#x200B;_产品管理_&#x200B;的角色，并使用&#x200B;_产品经理_、_Sr的值的工作标题属性来定义它。产品经理_，_高级产品经理_，_下午_，_高级。PM_、_主体PM_&#x200B;和&#x200B;_主要产品经理_。 然后，在&#x200B;_角色为产品管理_&#x200B;的条件匹配的“角色”模板中使用此角色。 使用配置的角色简化了创建每个角色模板的过程，并且不需要与每个可能的工作标题匹配的复杂条件。

>[!ENDSHADEBOX]

## 访问配置的角色

1. 在左侧导航中，选择&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 配置]**。

1. 单击中间面板上的&#x200B;**[!UICONTROL 角色映射]**&#x200B;以显示角色列表。

   ![访问配置的角色](./assets/configuration-persona-mapping.png){width="800" zoomable="yes"}

   在此页面中，您可以[创建](#create-a-persona)、[编辑](#edit-a-persona)或[删除](#delete-a-persona)角色。

   角色映射列表以表格形式组织，并在顶部显示最近更新的角色（按&#x200B;_[!UICONTROL 上次更新]_&#x200B;排序）。 您可以通过单击右上角的&#x200B;_列设置_ （ ![列设置](../assets/do-not-localize/icon-column-settings.svg) ）图标并选中或清除列复选框来自定义显示的表。

要在角色映射列表中显示的![列](./assets/configuration-persona-mapping-list-columns.png){width="300"}

1. 要访问角色的详细信息，请单击名称。

### 默认角色

_角色映射_&#x200B;列表包含根据作业标题属性定义的五个默认角色。 您可以根据组织的需求编辑以下任何默认角色：

| 用户画像 | 职称 |
| ------- | ---------- |
| CXO / EVP - CXO /执行副总裁 | 首席执行官、首席信息官、首席技术官、首席运营官、首席财务官、战略执行副总裁 |
| SVP/VP — 高级副总裁/副总裁 | 营销部副总裁、销售部副总裁、运营部副总裁、产品部副总裁、 IT部副总裁 |
| 高级董事/董事 — 高级董事/董事 | 工程总监、高级产品总监、财务总监、客户成功总监 |
| 高级经理/经理 — 高级经理/经理 | 高级营销经理、IT经理、运营经理、销售经理、人力资源经理 |
| 个人贡献者 — 个人贡献者 | 客户主管、软件工程师、营销专家、客户成功代表 |
| 分析师 — 分析师 | 业务分析师、数据分析师、市场研究分析师、财务分析师、运营分析师 |
| 开发人员 — 开发人员 | 前端开发人员、后端开发人员、全栈开发人员、移动应用程序开发人员、开发运营工程师 |
| 专业人员 — 专业人员 | 人力资源专家、法律顾问、合规干事、项目经理、采购专家 |
| 顾问 — 顾问 | 管理顾问、IT顾问、业务流程顾问、营销顾问 |
| 其他 — 其他 | 行业专家、独立顾问、自由顾问、主题专家 |

### 列表筛选

要查找所需的角色，请在搜索栏中输入文本字符串，以按名称匹配角色，

![筛选显示的角色映射](./assets/configuration-persona-mapping-search.png){width="700" zoomable="yes"}

## 创建角色

1. 在左侧导航中，选择&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 配置]**。

1. 单击中间面板中的&#x200B;**[!UICONTROL 角色映射]**。

1. 单击&#x200B;**[!UICONTROL 创建角色]**。

1. 输入角色的唯一的&#x200B;**[!UICONTROL Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**（可选）。

   ![创建角色映射](./assets/configuration-persona-mapping-new.png){width="700" zoomable="yes"}

1. 选择用于匹配角色的属性。

   * 单击&#x200B;**[!UICONTROL 选择人员属性]**。

   * 在对话框中，选中要映射的每个属性的复选框（最多五个）。

     您可以通过单击右上角的&#x200B;_列设置_ （ ![列设置](../assets/do-not-localize/icon-column-settings.svg) ）图标来自定义显示的表。

     要按名称筛选属性列表，请在搜索栏中输入文本字符串。 您还可以单击左上角的&#x200B;_筛选器_（![筛选器图标](../assets/do-not-localize/icon-filter.svg)）图标，以按类型&#x200B;_标准_&#x200B;或&#x200B;_自定义_&#x200B;筛选显示的列表。

     ![选择角色属性对话框](./assets/configuration-persona-mapping-select-attributes.png){width="700" zoomable="yes"}

   * 单击&#x200B;**[!UICONTROL 保存]**。

     选定的属性填充在&#x200B;_[!UICONTROL 角色属性]_&#x200B;部分。

1. 对于每个属性，输入要与属性匹配的逗号分隔值。

   您还可以添加用于标识匹配项的提示，以代替值。 例如，您可以输入

1. 单击&#x200B;**[!UICONTROL 提交]**。

## 编辑角色

单击角色名称以访问和编辑角色的详细信息，

您可以更改名称或说明、添加属性或更新属性值。 完成更改后，单击&#x200B;**[!UICONTROL 提交]**。

## 删除角色

删除角色会将其从&#x200B;_角色映射_&#x200B;列表中删除，并且角色模板中不再有该角色可用。

1. 在&#x200B;_[!UICONTROL 角色映射]_&#x200B;页面上，找到要删除的角色。

1. 在名称旁边，单击的省略号(**...**)图标，然后选择&#x200B;**[!UICONTROL 删除]**。

1. 在确认对话框中单击&#x200B;**[!UICONTROL 删除]**。
