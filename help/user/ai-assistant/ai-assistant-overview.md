---
title: Journey Optimizer B2B edition中的AI助手
description: 占位符
feature: AI Assistant
level: Beginner
exl-id: 52ff66d2-1969-4e2c-985a-c75e613368de
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '1241'
ht-degree: 4%

---

# Journey Optimizer B2B edition中的AI助手

Journey Optimizer B2B edition中的AI助手是基于Adobe Experience Platform[&#128279;](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home){target="_blank"}中的AI助手所基于的相同技术创建的。 它是一种对话式体验，可用于加快Adobe Journey Optimizer B2B edition中的工作流程。 您可以使用AI Assistant进一步了解产品功能、排除问题或搜索信息并查找Journey Optimizer B2B edition的操作见解。

>[!IMPORTANT]
>
>在Journey Optimizer B2B edition中使用AI助手之前，需要与[用户准则](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)达成协议。 本协议还包含公共测试版协议，以便您能够在以测试版容量推出其他AI Assistant功能时使用它们。

+++查看用户协议界面

![用户协议的第一页。](./assets/user-agreement-1.png)

![用户协议的最后一页。](./assets/user-agreement-2.png)

+++

## Journey Optimizer B2B edition中的AI助手功能

为了制定对您提交问题的响应，AI Assistant查询数据库并将数据库中的数据转换为人类可读的答案。 此响应是基础数据的内部表示形式，也称为&#x200B;_&#x200B;**_知识图_**&#x200B;_ — 给定答案的概念、数据和元数据的综合网络。 知识图由每次提交查询时引用的子图组成：

* Experience League文档。
* 操作构件，例如架构、字段、受众和历程。

考虑在提交AI Assistant查询之前需要哪种类型的查询：

### 产品知识

产品知识是指以Adobe Experience League上的Journey Optimizer B2B edition文档为基础的概念和主题。 产品知识问题可进一步细分为以下子组：

| 产品知识 | 示例 |
| --- | --- |
| 点式学习 | <li>什么是购买团体？ <li> 是否向我显示购买组角色模板的示例？ |
| 打开发现 | <li>创建购买组的步骤是什么？ <li>如何在购买组角色模板中使用自定义字段？ |
| 故障排除 | <li>为什么没有为创建的历程购买组？ <li>为什么在历程中找不到要侦听的体验事件？ |

### 运营见解

_操作分析_&#x200B;是指AI助手生成的有关元数据对象（属性、帐户受众、数据流、数据集、目标、帐户历程、架构、源、购买群组模板和解决方案兴趣）的答案。 这些见解包括计数、查找和谱系影响。 他们不会查看沙盒中的任何数据。

* 哪个帐户受众拥有最大的受众规模，该规模是多少？
* 有多少客户受众从未在任何历程中使用过？
* 哪些活动历程使用解决方案关注&#x200B;_x_？

您可以在以下域中向AI Assistant询问有关您的操作见解的问题：

| 域 | 支持的元数据 | 不支持的元数据 |
| --- | --- | --- |
| 属性/字段 | <li>属性名称搜索 <li>属性 — 架构关系 <li>属性 — 数据集关系 <li>属性 — 受众关系 <li>属性 — 目标关系 | <li>属性类 <li>审核 <li>弃用状态 <li>标记 <li>存储在属性中的值 |
| 帐户受众&#x200B;<br><br>**_注意：_**&#x200B;AJO B2B AI助手只能回答帐户受众的受众问题，而Experience Platform AI助手只能回答人员受众的问题 | <li>受众人数 <li>受众类型（流式传输或批处理） <li>创建/修改日期 <li>激活状态 <li>成员计数 <li>复制受众 <li>名称和ID搜索 | <li>受众重叠 <li>Audience Activation <li>审核 <li>创建/修改 <li>标记 <li>成员资格趋势 |
| 数据流 | <li>数据流计数 <li>数据流状态 <li>数据流 — 数据集关系 <li>数据流 — 源关系 | <li>创建/修改 <li>数据流 — 批次关系 <li>摄取配置文件计数 |
| 数据集 | <li>数据集计数 <li>配置文件启用状态 <li>创建/修改日期 <li>数据集 — 架构关系 <li>数据集 — 受众关系 <li>数据集 — 属性关系 <li>数据集 — 数据流关系 <li>名称搜索 <li>名称和ID搜索 | <li>审核 <li>创建者 <li>数据集 — 批次关系 <li>数据集创建/修改 <li>数据集大小 <li>配置文件数 <li>行数 <li>值搜索 |
| 目标 | <li>已配置的目标计数 <li>目标 — 受众关系 <li>目标属性关系 | <li>帐户设置 <li>帐户凭据信息 <li>独特配置文件已激活 |
| 历程(帐户历程) | <li>计数 <li>名称和ID搜索 <li>历程状态 <li>创建/修改日期 | <li>属性 — 历程关系审核 <li>创建/修改 <li>创建者 |
| 架构 | <li>架构计数 <li>创建/修改日期 <li>架构 — 属性关系 <li>架构 — 数据集关系 <li>架构 — 受众关系 <li>配置文件启用状态 <li>名称搜索 <li>名称和ID搜索 | <li>审核 <li>创建/修改 <li>创建者 <li>字段组 <li>身份标识 <li>身份标识命名空间 <li>标记 <li>配置文件数 |
| 源 | <li>帐户计数 <li>帐户状态 <li>每个帐户的活动/不活动数据流 <li>Source连接器 — 数据流关系 <li>Source帐户 — 数据流关系 | <li>帐户凭据信息 <li>帐户设置数据摄取量度 <li>配置文件数来源 — 批次关系 |
| 购买组模板 | <li>计数 <li>状态 <li>角色 <li>名称和ID搜索 | <li>角色规则 |
| 解决方案兴趣 | <li>计数 <li>状态 <li>解决方案兴趣 — 购买组模板关系 <li>名称和ID搜索 | <li>解决方案兴趣 — 购买团体关系 |

{style="table-layout:fixed"}

对于操作分析问题，答案可能不会反映UI的当前状态。 支持这些问题的数据每24小时更新一次。 例如，用户白天在Real-Time CDP中所做的更改会在晚上与数据存储同步，然后早上就可供用户提问了。 登录到沙盒以查询与对象相关的特定数据。

### 功能范围

目前，人工智能助理的范围如下：

* **产品知识**： AI助手可以回答Real-Time Customer Data Platform和Adobe Journey Optimizer B2B edition的产品知识问题。

* **操作分析**：您可以向AI Assistant询问有关以下数据对象的操作分析的问题：属性、帐户受众、数据流、数据集、目标、帐户历程、架构、源、购买组模板和解决方案兴趣。

### 隐私、安全和治理

Journey Optimizer B2B edition中的AI助手以隐私、安全和治理为原则。 查看以下信息，了解您可以期望从AI Assistant获得的以客户信任为中心的功能：

* 目前，AI助手不使用任何个人数据，即使用于培训目的也是如此。

* AI Assistant不知道客户数据，例如人员、帐户、机会和购买群体。

* 您必须具有显式权限才能与AI助手交互。

   * 管理员可以使用[权限UI](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"}和[Admin Console](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/ui/browse){target="_blank"}设置权限。

   * 权限是细粒度的，您的沙盒管理员可以配置哪些用户能够提出不同类别的问题（使用AI助手基于产品知识的问题或有关操作见解的问题）。

* 您可以查看之前与AI助手进行的交互的日志，保留策略为30天。

* AI助手在响应用户提示时基于特定于沙盒的数据和公共Adobe文档。 数据不会在沙盒之间共享。

* 您提供给AI助理的提示不会共享给其他客户。

### 常见问题解答

以下是有关Journey Optimizer B2B edition中AI助理的常见问题解答列表。

**是否实时提供AI助手的信息？**

AI Assistant响应中显示的数据每天都会更新。 此周期意味着，响应中包含的数据可能比响应时用户界面中显示的数据晚24小时。

**AI助手有哪些功能？**

AI Assistant可以处理Adobe产品知识查询，并可解答与运营工件的运营见解相关的问题。

**AI助手能否提供有关客户数据的信息？**

不会。AI Assistant无法访问客户数据，因此，AI Assistant不会查看或使用这些数据。

**我的个人信息是否用于AI助理的培训数据？**

AI助手不使用个人信息进行培训。 请勿向AI助手提供您本人或其他任何参与方的个人信息（包括您的姓名或联系信息）。

## 后续步骤

大致了解AI助手后，继续在工作流中启用和使用AI助手。 有关更多信息，请参阅以下文档：

* [启用 AI 助手访问](./enable-ai-assistant-access.md)
* [问题指导](./question-guidance.md)
* [使用 AI 助手](./use-ai-assistant.md)
