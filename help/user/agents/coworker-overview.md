---
title: Adobe Journey Optimizer B2B Edition中的同事
description: 了解如何使用CX Enterprise Coworker查找、创建和配置帐户和人员历程，查看草稿预览并批准历程创建。
feature: Account Journeys, Person Journeys, Agentic AI
role: User
level: Beginner
autotag-review: '2026-11-24T23:47:29.469Z'
TQID: 'https://experienceleague.adobe.com/gkizS-MB6qEMoG1pMqD3tSCBtcEuv-m-GMD5H6Z4JsY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: 9b63d357-750f-5558-9208-62fc8a356785
    internal-label: Approval
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: c2f21a5c-bae4-56c6-97e3-2fc9a0e6c120
    internal-label: Use Cases
subfeature_v2:
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 81b4844bc7b333baaa2218639a542fefd512102f
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 1%
---

# [!DNL Adobe Journey Optimizer B2B Edition]中的[!DNL CX Enterprise Coworker] {#coworker-overview}

使用[!DNL Adobe CX Enterprise Coworker]聊天完成[!DNL Adobe Journey Optimizer B2B Edition]中的任务。 用简单的语言描述目标。 [!DNL Coworker]计划工作，执行工作，验证结果，并提交工作供您审批。

查找现有帐户和人员历程，创建新草稿历程或更新已保存的草稿。 [!DNL Coworker]将您的简报转换为经过验证的历程图，并在创建草稿之前对其进行预览。 在[!DNL Coworker]创建历程之前，您必须明确批准预览。

[!DNL Coworker]尊重您组织的现有[产品权限](../admin/user-management.md#b2b-product-permissions)。 您只能执行已经允许您执行的操作。 管理员控制您何时具有写入权限。 有关访问要求，请参阅[启用AI访问](../ai-coworker/enable-ai-access.md)。

[!DNL Coworker]在Adobe生态系统中工作，而不仅仅是在[!DNL Journey Optimizer B2B Edition]中。 有关其更广泛的功能，请参阅[Adobe CX Enterprise Coworker聊天概述](https://experienceleague.adobe.com/zh-hans/docs/coworker/content/chat/overview){target="_blank"}。 有关打开应用和开始对话的说明，请使用[同事界面指南](https://experienceleague.adobe.com/zh-hans/docs/coworker/content/chat/ui-guide){target="_blank"}。

## 历程技能 {#skills}

使用这三种技能检查历程、构建历程图和配置节点。 技能标识符是准确的技术名称。

| 技能 | 它有助于您完成哪些工作 | 超出技能范围 |
| --- | --- | --- |
| `journey-lookup-ajob2b` | 列出、计数、查找和解释帐户和人员历程。 检查节点、重新进入设置以及历程使用的活动、属性或事件受众。 这项技能不会改变历程。 | 创建或更改历程、配置规则、创作消息副本、管理购买群组模板、发布或删除。 |
| `journey-creation-ajob2b` | 将简介转换为历程。 Select历程类型，将受众解析为其[!DNL Adobe Experience Platform]受众ID，验证并预览该图形。 在获得明确批准后创建草稿。 编辑已保存草稿的图形和再次进入设置。 | 查找现有历程、配置规则、创作消息副本、管理购买群组模板、发现受众、发布或删除。 |
| `journey-rules-ajob2b` | 在已保存历程的未配置节点上配置拆分条件、操作、事件和动态列表受众。 | 更改图表、查找历程、创作电子邮件或短信副本、发现受众或发布。 |

有关其他提示指导，请参阅[B2B的历程技能](./journey-skills.md)。 若要使用帐户和人员受众，请参阅[B2B帐户和人员的受众技能](./audience-skills-b2b.md)。

## 示例用例 {#use-cases}

使用单独的请求来构建草稿、配置其节点并检查现有历程。

### 构建帐户历程 {#build-account-journey}

从简介创建客户培养历程，然后配置其节点。

示例提示： _为企业目标帐户受众创建帐户历程，该历程会发送欢迎电子邮件，等待三天，然后发送案例研究电子邮件。_

1. 在[!DNL Coworker]聊天中描述受众和历程流。
1. 查看经过验证的历程图和预览。 [!DNL Coworker]将指定受众解析为其[!DNL Experience Platform]受众ID。
1. 明确批准预览。 [!DNL Coworker]创建草稿并返回其链接。
1. 要求[!DNL Coworker]配置草稿的未配置节点。
1. 在[!DNL Journey Optimizer B2B Edition]中打开草稿以添加邮件副本并查看历程。

结果是一个草稿历程，而不是发布的历程。 在应用程序中完成[历程审阅和发布步骤](../journeys/create-publish-journey.md)。

### 检查和更新历程 {#inspect-update-journeys}

审查历程清单，然后优化已保存草稿的拆分条件和重新进入设置。

示例查找提示：_有多少帐户历程是实时的？ 显示journey 14251帐户正在等待的位置。_

1. 询问[!DNL Coworker]按州的历程计数，或按名称或ID查找历程。
1. 查看每个节点的历程详细信息和帐户计数。
1. 标识要更新的已保存草稿。
1. 要求[!DNL Coworker]配置其拆分条件。 例如： _对于草稿历程14252，请让高意图分支需要访问定价页面。_
1. 请求重新进入更改。 例如： _对于草稿历程14252，在30天内阻止帐户重新进入。_

更改将应用于保存的草稿。 发布是一个单独的步骤。 有关配置详细信息，请参阅[拆分和合并路径](../journeys/split-merge-paths-nodes.md)和[历程重新进入](../journeys/journey-re-entry.md)。

## MCP工具 {#mcp-tools}

[!DNL Coworker]对历程任务使用以下模型上下文协议(MCP)工具。 读取工具检查现有信息，检查工具验证图形，写入工具更改历程设置或草稿。

| 工具 | 支持的操作 | 类型 |
| --- | --- | --- |
| `list_account_journeys` | 返回按页划分的帐户历程列表。 | 读取 |
| `list_person_journeys` | 返回人员历程的分页列表。 | 读取 |
| `count_account_journeys` | 按州计数帐户历程。 | 读取 |
| `count_person_journeys` | 按州计算人员旅程。 | 读取 |
| `get_journey` | 读取历程节点和再次进入设置。 | 读取 |
| `get_journey_rules` | 读取历程未配置节点的配置目标。 | 读取 |
| `get_journey_node_catalog` | 返回`ruleset_types`，这是规则数据的有效输入。 | 读取 |
| `validate_journey_graph` | 验证已编写的草稿图形。 | Check |
| `create_journey` | 使用`confirm=false`预览历程。 获得明确批准后，创建草稿并返回其链接。 | 写入 |
| `update_journey` | 更改已保存草稿历程的图形。 | 写入 |
| `set_journey_reentry` | 更改重新进入设置。 | 写入 |
| `set_journey_split_conditions` | 设置拆分分支条件。 | 写入 |
| `apply_journey_rules` | 将`rule_data`用于条件、操作、事件和动态列表受众应用到历程。 | 写入 |
