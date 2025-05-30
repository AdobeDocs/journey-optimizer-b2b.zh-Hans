---
title: 面向AI助手的问题指南
description: 了解如何在Journey Optimizer B2B edition中为AI助手编写有效的问题。
feature: AI Assistant
role: User
level: Beginner
exl-id: 65541246-7f4f-442f-8293-df036ea1c4ac
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 1%

---

# Journey Optimizer B2B edition中的AI助手问题指南

查看以下一组在Journey Optimizer B2B edition中查询AI助手时的示例问题。 此信息还包含有关如何对您的问题进行短语以从AI助手获得最佳响应的提示。

## 基于目标的问题

以下示例问题根据使用AI助手时可以完成的目标进行分组：

| 目标 | 描述 | 示例 |
| --- | --- | --- |
| 学习概念和持续工作流 | 作为新手，您可以使用AI Assistant学习Real-Time CDP和Adobe Journey Optimizer B2B edition概念，并熟悉不熟悉的产品和功能。 <br>作为经验丰富的用户，您可以使用AI Assistant解决可能阻止您工作流的边缘案例。 | <li>告诉我Real-Time CDP的一些用例。 <li>向我解释购买组的概念。 |
| 故障排除 | 使用AI Assistant了解如何调试工作流中可能遇到的基本错误。 | <li>此错误&lt;ERROR_MESSAGE>表示什么？ <li>为何无法删除名为“……”的受众？ |
| 沙盒卫生 | 使用AI Assistant识别任何重复或未使用的对象，以便您能够有效地维护沙盒。 | <li>能否向我显示类似的帐户受众？ <li>是否有任何没有关联数据集的架构？ |
| 价值分析 | 使用AI Assistant识别您最常用的数据对象，评估任何绩效指标或找到最有价值的数据对象。 | <li>我们的“……”区段定义中有多少帐户？ <li>何时将受众激活到Experience Cloud受众目标？ |
| 搜索 | 使用AI Assistant查找受支持的Experience Platform和Adobe Journey Optimizer B2B edition对象，如帐户受众、数据集、目标、架构、源、帐户历程、购买组模板和解决方案兴趣 | <li>在帐户历程中使用的名称中列出包含“Luma”的受众。 <li>“Luma：自定义操作”XDM架构中有哪些属性？ |
| 影响分析 | 使用AI Assistant识别某些工作流中使用的数据对象，以便您能够评估任何更改的影响。 | <li>哪些帐户受众在“B2B人员”架构中使用`workEmail.address`？ <li>`jobTitle`存储在哪些数据集中？ |

## 用短语表述您的问题

您必须清晰明了地向AI Assistant表达您的问题，并且提供相应的上下文，才能获得尽可能准确的响应。 请参阅以下提示列表，以获取有关如何根据上下文提出明确问题的指导：

* 以简洁的方式陈述您的任务和/或问题。
* 避免使用模糊的语言或过于复杂的语法以促进理解。
* 提供关于您的任务和/或问题的相关上下文，因为上下文可以帮助AI助手生成更相关的响应。

下表提供了在使用AI助手时可以遵循的一些最佳实践：

| Do | 示例 |
| --- | --- |
| <li>指定要检索或分析的对象或信息。 <li>尝试将数据对象名称放在引号中。 <li>如果您只知道对象名称的一部分，则还可以在问题中指定该部分。 | <li>哪些数据集使用“B2B帐户”架构？ <li>显示名称中包含“帐户”的激活受众。 按成员数对其进行排名。 |
| <li>避免歧义，使用清晰的语言。 <li>使用准确的术语以确保查询更清晰。 <li>在就Adobe Experience Platform和Adobe Journey Optimizer B2B edition提出疑问时，请尝试使用特定于Experience Platform或Adobe Journey Optimizer B2B edition的术语，以提高响应的相关性。 | <li>“我的帐户受众”中有多少成员？ <li>有多少帐户历程使用帐户受众“我的帐户受众”？ |
| <li>提供上下文或指定条件以筛选结果。 <li>在问题中使用过滤条件限制响应中的数据量。 | <li>向我显示尚未激活且创建日期超过6个月且从未修改的帐户受众。 <li>显示过去7天内发布的帐户历程，并使用拥有1000多个成员的帐户受众 |

| 不要 | 示例 |
| --- | --- |
| 使用模糊或模糊的语言。 | <li>给我有关数据集的信息。 <li>历程x有什么作用？ <li>“ACME受众”中有多少用户？ <li>显示区段。 <li>列表属性。 |
| 发出不完整的请求。 | <li>“Luma — 忠诚度数据集” |
| 接受没有上下文的知识。 | <li>过去6个月中的受众。 <li>为我构建查询。 <li>为我创建历程 |
| 制定过于复杂的查询。 | <li>提供跨所有对象及其依赖关系的数据谱系的综合分析。 |
| 省略标准或参数。 | <li>向我显示数据集。 |

## 不支持的问题的示例

以下列表包括Journey Optimizer B2B edition中的AI助手当前不支持的问题示例：

* 哪些帐户受众在条件中使用……字段组的workEmail.address字段？ 
* 在分发可视化图表中显示使用规模超过10,000、5000-10,000、1000-5000以及低于1000的帐户受众的活动历程数
* 谁对帐户历程x进行了最后一次更新？
* 有多少活动历程会为解决方案兴趣x添加购买组成员？
* 对于解决方案兴趣x，哪些活动历程会增加购买小组成员？
* 购买组模板时最常见的决策者标题是什么？
* 谁是购买组模板x的决策者？

## 后续步骤

有关如何在工作流中使用AI助手功能的信息，请参阅[在Journey Optimizer B2B edition中使用AI助手](./use-ai-assistant.md)。
