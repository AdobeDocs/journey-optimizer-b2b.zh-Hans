---
title: AI助理技能
description: 查看Journey Optimizer B2B Prime中的AI助手技能 — 项目、历程、受众、评分、内容和发送时间优化的打包工作流程。
badgeBeta: label="Beta 版" type="informative" tooltip="此功能当前为有限测试版"
autotag-review: '2026-06-24T23:55:36.649Z'
TQID: 'https://experienceleague.adobe.com/iIi07OBWKxxa-oW-A6VrlkoTS02kmCx8kfMaCe-C-4o'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ff10f619-348f-47e3-99bf-3ce4c817cf2cid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 9433a1e86767e4504cb238ba8f3fae6e5c098a86
workflow-type: tm+mt
source-wordcount: 565
ht-degree: 6%

---

# AI助理技能

_技能_&#x200B;是代理程序知道如何运行的打包工作流 — `/`菜单和自然语言请求背后的构建块。 每个技能都捆绑了分步说明和一个工作所需的特定工具（例如，“发布历程”、“比较两个人列表”、“构建评分模型”）。

>[!NOTE]
>
>每个技能都根据技能是否改变[!DNL Journey Optimizer B2B Prime]或[!DNL Marketo Engage]状态（**写入**）、是否只查询/分析/生成（**读取**）或是否具有同等的查询+变异函数（**读取+写入**）进行分类。

## 方案和规划 {#programs-planning}

| 技能 | 作用 | 访问 | 产品表面 | 影响/数据流 |
|---|---|---|---|---|
| `falco-program-creation` | 端到端[!DNL Journey Optimizer B2B Prime]项目创建 — 项目、子文件夹、令牌、列表、历程。 | 写入 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `adapt-program` | 从[!DNL Marketo Engage]项目生成迁移故事以进行[!DNL Journey Optimizer B2B Prime]适应。 | 读取 | [!DNL Journey Optimizer B2B Prime] | 读取[!DNL Marketo Engage]，写入[!DNL Journey Optimizer B2B Prime] |
| `folder-creation` | 在资产树中创建组织文件夹。 | 写入 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `program-creation` *（生成程序）* | 从营销活动简报创建Marketo项目。 | 写入 | [!DNL Marketo Engage] | 读取+写入[!DNL Marketo Engage] |
| `program-planning` *（计划营销活动）* | 将简报转换为设置/实施文档。 | 读取 | [!DNL Marketo Engage] | 读取[!DNL Marketo Engage] |
| `program-qa` *（验证程序）* | 验证/审核程序（仅限规则、测试计划或简要）。 | 读取 | [!DNL Marketo Engage] | 读取[!DNL Marketo Engage] |

## 历程 {#journeys}

| 技能 | 作用 | 访问 | 产品 | 后端（数据流） |
|---|---|---|---|---|
| `journey-creation` | 从自然语言创建和编辑人员历程。 | 写入 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `journey-edit-dates` | 在不发布的情况下更改历程的开始/结束日期。 | 写入 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `journey-publish` | 发布/启动/计划人员历程。 | 写入 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `journey-stop` | 中止、关闭、停止、停止或终止历程。 | 写入 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `journey-reentry` | 配置重新进入：允许/不允许、关闭、最大条目数。 | 写入 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `journey-trafficcontrol` | 运行显示配置文件路由的流量控制模拟。 | 读取 | [!DNL Journey Optimizer B2B Prime] | 读取[!DNL Journey Optimizer B2B Prime]（模拟） |
| `journey-observability` | 调试/监控进度 — 路径、计时、拆分、停顿、停顿。 | 读取 | [!DNL Journey Optimizer B2B Prime] | 读取[!DNL Journey Optimizer B2B Prime] + [!DNL Marketo Engage]（静态列表检查） |

## 受众和人员 {#audiences-people}

| 技能 | 作用 | 访问 | 产品 | 后端（数据流） |
|---|---|---|---|---|
| `audience-creation` | 调整[!DNL Marketo Engage]智能列表、创建人员列表或添加/更新规则。 | 写入 | [!DNL Journey Optimizer B2B Prime] | 读取[!DNL Marketo Engage] +读取/写入[!DNL Journey Optimizer B2B Prime] |
| `people-list-comparison` | 比较两个人员列表并显示重叠的成员。 | 读取 | [!DNL Journey Optimizer B2B Prime] | 读取[!DNL Journey Optimizer B2B Prime] |
| `import-leads` | 检查CSV数据质量并将导入提交到[!DNL Marketo Engage]。 | 读+写 | 两者 | 读取+写入[!DNL Marketo Engage] |
| `lead-investigation` *（调查潜在客户）* | 调查商机的活动、评分、资格鉴定和生命周期。 | 读取 | [!DNL Marketo Engage] | 读取[!DNL Marketo Engage] |

## 内容和渠道 {#content-channels}

| 技能 | 作用 | 访问 | 产品 | 后端（数据流） |
|---|---|---|---|---|
| `content-personalization` | 浏览/预览模板和编辑内容/生成变体。 | 读+写 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `asset-tokens` | 程序/文件夹/历程中的完整令牌CRUD。 | 读+写 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `fcs-channels` | 渠道查找和CRUD +发布/停止/删除。 | 读+写 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |

## 评分和信号 {#scoring-signals}

| 技能 | 作用 | 访问 | 产品 | 后端（数据流） |
|---|---|---|---|---|
| `scoring-studio` | 列出/获取评分模型并构建/发布它们。 | 读+写 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] （评分服务）；读取[!DNL Marketo Engage]潜在客户字段/活动类型 |
| `engagementconfiguration` | 显示参与配置和编辑/更新权重。 | 读+写 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `intentconfiguration` | 显示意图配置和设置/更新权重。 | 读+写 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `intent-query` | 按人员/区段/列表查询和解释意图分数。 | 读取 | [!DNL Journey Optimizer B2B Prime] | 读取[!DNL Journey Optimizer B2B Prime] |

## 发送时间优化 {#sto}

| 技能 | 作用 | 访问 | 产品 | 后端（数据流） |
|---|---|---|---|---|
| `send-time-optimization` | 检查STO状态并在电子邮件节点上启用/禁用。 | 读+写 | [!DNL Journey Optimizer B2B Prime] | 读取+写入[!DNL Journey Optimizer B2B Prime] |
| `send-time-report` | 获取/显示STO性能报告。 | 读取 | [!DNL Journey Optimizer B2B Prime] | 读取[!DNL Journey Optimizer B2B Prime] |

## 知识 {#knowledge}

| 技能 | 作用 | 访问 | 产品 | 后端（数据流） |
|---|---|---|---|---|
| `product-knowledge` | 回答有关Experience League的[!DNL Journey Optimizer B2B Prime]文档中的操作方法/概念问题。 | 读取 | 两者 | 读取外部文档 — 无产品数据 |

## 跨后端 {#cross-backend}

这些技能跨越多个后端：

- **`adapt-program`** — `gather_program_assets`读取[!DNL Marketo Engage] (`get_program`， `get_smart_campaign`， `list_emails`)，然后通过`falcomcp_create_journey`写入 — 经典跨后端。
- **`audience-creation`** — 读取[!DNL Marketo Engage]个智能列表(`get_smart_list` / `get_smart_campaign`)，然后写入[!DNL Journey Optimizer B2B Prime]个人列表。
- **`journey-observability`** — [!DNL Journey Optimizer B2B Prime]读取加上`check_lead_in_marketo_static_list` [!DNL Marketo Engage]读取。
- **`scoring-studio`** — 与[!DNL Journey Optimizer B2B Prime]评分服务一起读取[!DNL Marketo Engage]潜在客户字段/活动类型。

所有`falco-mcp_*`和journey/token/scoring/STO/FCS工具点击[!DNL Journey Optimizer B2B Prime]服务；CSV/program/lead工具点击[!DNL Marketo Engage]。
