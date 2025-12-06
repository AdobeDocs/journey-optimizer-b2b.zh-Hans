---
title: Adobe Journey Optimizer B2B Edition 文档
description: Journey Optimizer B2B Edition 的完整文档——浏览可用于加入、创建购买群组、生成帐户历程和管理内容的资源。
exl-id: 3d7b6c82-95c3-4d89-b3dc-7fd5b0aef615
source-git-commit: 792ce46885010b41f21e501b4484fadd323d5785
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 49%

---

# Adobe Journey Optimizer B2B Edition 文档

[!DNL Adobe Journey Optimizer B2B Edition]是首创的应用程序，它允许营销和销售团队在整个客户生命周期中编排基于帐户的体验，并使购买组有资格购买特定产品。 它利用AI吸引和授权目标客户中的购买群体，帮助您的团队形成更高质量的管道，设计更好的收购、扩展和保留策略。 它还支持在销售和营销团队之间共享见解。

本文档提供了有关如何掌握应用程序的信息。 它专为营销人员、业务开发代表、数据分析师和运营管理员而设计。

## 新增功能

查看[!DNL Journey Optimizer B2B Edition]应用程序和文档中的最新添加和增强功能的此抽样。

>[!BEGINTABS]

>[!TAB AI代理]

借助[Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/home#agent-orchestrator){target="_blank"}，AI Assistant界面可自动调用专业代理以获取正确的答案和见解。 Agent Orchestrator 会记住您的对话历史，使您能够自然地延续以前的问题，无需重复上下文，它还会结合来自多个代理的洞察，为您提供清晰、统一的回答。在[!DNL Journey Optimizer B2B Edition]上下文中，有三个针对特定B2B任务和域的专门构建代理：

* [Audience Agent B2B](./agents/audience-agent-b2b.md)
* [历程生成代理B2B](./agents/journey-agent.md)
* [Account Qualification 代理](./agents/sales-qualifier.md#account-qualification-agent)

>[!TAB 品牌主题]

通过主题，非技术设计人员能够创建符合特定品牌和样式的可重用电子邮件内容设计准则。 主题使营销人员能够更快地利用具有视觉吸引力、品牌一致的电子邮件，而且所需的工作量更少，并提供高级自定义选项以满足独特的设计需求。

[!BADGE 了解详情]{type=Informative url="/help/user/content/brand-themes.md" tooltip="了解品牌主题"}

>[!TAB 角色映射]

营销人员可以定义详细的用户档案，包括背景、职责、棘手问题和首选通信渠道。 使用这些定义，管理员可以根据[!DNL Journey Optimizer B2B Edition]中的人员属性配置角色，以便角色模板可以使用简化且一致的角色条件来捕获这些角色。

[!BADGE 了解详情]{type=Informative url="/help/user/admin/persona-mapping.md" tooltip="了解角色映射"}

>[!TAB In-CRM销售分析]

销售团队成员现在可在 Salesforce 或 Dynamics 集成中查看正在成熟的购买群体及相关洞察，从而发现新的销售机会。系统会显示购买群体的阶段、评分及相关成员等详细信息。

[!BADGE 了解详情]{type=Informative url="/help/user/buying-groups/incrm-insights.md" tooltip="了解In-CRM销售分析"}

>[!TAB 电子邮件内容协作]

电子邮件设计空间包括用于提供反馈和解决问题的协作工具，以便营销团队可以直接在[!DNL Journey Optimizer B2B Edition]内无缝审查、讨论和最终确定电子邮件资产。 用户无需通过外部工具（如聊天、电子邮件会话或电子表格）共享草稿，即可在邮件设计空间内直接进行评论、提出修改建议并处理反馈。您可以标记您的团队成员，这样他们就会收到包含评论详细信息的电子邮件或推送通知。

[!BADGE 了解详情]{type=Informative url="/help/user/content/email-collaboration-tools.md" tooltip="了解电子邮件内容协作工具"}

>[!TAB 深色模式电子邮件设计]

电子邮件设计空间现在包含&#x200B;_深色模式_&#x200B;预览和设置。深色模式允许支持该功能的电子邮件客户端或应用程序以深色背景显示邮件，同时采用浅色文字、按钮及其他视觉元素。预览渲染、自定义设置、确保无障碍访问，并在不同电子邮件客户端中进行测试。

[!BADGE 了解详情]{type=Informative url="/help/user/content/email-dark-mode.md" tooltip="了解深色模式电子邮件设计"}

>[!TAB 人员参与度评分]

B2B 营销人员现在可以使用个人级别的参与度评分作为某个历程的拆分路径的过滤器，或作为角色模板中的过滤器，来创建购买群组。通过评分和筛选可以精确定位购买群组成员，使持续参与更加个性化。

[!BADGE 了解详情]{type=Informative url="/help/user/buying-groups/engagement-scores.md" tooltip="了解人员参与度评分和筛选"}

>[!ENDTABS]

有关新功能和改进的完整列表，请参阅[发行说明](../user/release-notes/release-notes.md)。

## 开始浏览 {#section-explore}

:::: landing-cards-container

:::
![列表图标](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

最新发行说明

了解Adobe Journey Optimizer B2B edition中的最新发行说明、新增功能和改进。

[查看发行说明](./release-notes/release-notes.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

快速入门

查看Journey Optimizer B2B edition管理员和营销人员入门指南。

[快速入门](./start/get-started.md)
:::

:::
![配置图标](https://cdn.experienceleague.adobe.com/icons/gear.svg)

配置XDM字段

实施系统配置以激活要在Adobe Journey Optimizer B2B edition中使用的XDM架构和字段。

[查看XDM字段管理](./admin/xdm-field-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

通信渠道

配置和管理电子邮件、短信和其他渠道，以提供个性化的客户互动。

[配置电子邮件渠道](./admin/configure-channels-emails.md)
[配置短信渠道](./admin/configure-channels-sms.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

创建帐户历程

设计、编排、管理和优化个性化的帐户历程。

[探索历程](./journeys/journey-overview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/users.svg)

了解购买组

有关创建、管理和优化购买群体以实现有效定位的详细指导。

[了解购买群组](./buying-groups/buying-groups-overview.md)
:::

::::

<!-- 
:::
![icon](https://cdn.experienceleague.adobe.com/icons/image.svg)

Design Content

Learn how to author and manage content for personalized customer experiences orchestarted through journeys.

[Explore Content Components](./content/content-components.md)
::: 
-->

## 概述演示

探索购买群组的组成部分，了解构建帐户历程的基础知识。

>[!VIDEO](https://video.tv.adobe.com/v/3432054?quality=12)

## 深入了解文档

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px" alt="快速入门"><br/>
      <strong>快速入门</strong><br/><a href="home-page.md">登录和主页</a><br/><a href="./start/get-started.md">加入指南</a> <br/><a href="./ai-assistant/ai-assistant-overview.md">AI 助手</a>
    </td>
    <!--
    <td>
      <img src="../assets/do-not-localize/icon-configure.svg" width="35px"><br/>
      <strong>Configuration<br/>administration</strong><br/><a href="using/configuration/channel-surfaces.md">Channel surfaces</a> - <a href="using/configuration/about-data-sources-events-actions.md">Configure journeys</a>  - <a href="using/administration/permissions-overview.md">Access control</a> - <a href="using/administration/sandboxes.md">Sandboxes management</a>
    </td> -->
    <td>
      <img src="../assets/do-not-localize/icon_audience.svg" width="35px" alt="购买群组"><br/>
      <strong>购买群组</strong><br/><a href="./buying-groups/buying-groups-overview.md">购买群组概述</a><br/><a href="./buying-groups/buying-groups-role-templates.md">角色模板</a><br/><a href="./buying-groups/solution-interests.md">解决方案兴趣</a><br/><a href="./buying-groups/buying-groups-create.md">创建购买群组</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-paths.svg" width="35px" alt="帐户历程"><br/>
      <strong>帐户历程</strong><br/><a href="./journeys/journey-overview.md">历程概述</a><br/><a href="./journeys/journey-overview.md#create-an-account-journey">创建帐户历程</a><br/><a href="./journeys/journey-nodes.md">历程节点</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-campaign.svg" width="35px" alt="历程内容"><br/>
      <strong>历程内容</strong><br/><a href="./content/add-email.md">电子邮件渠道</a><br/><a href="./content/ai-assistant-emails.md">电子邮件 AI 助手</a><br/><a href="./content/genstudio-email-workflow.md">GenStudio 电子邮件体验</a><br/><a href="./content/sales-alert-email.md">销售警报电子邮件</a><br/><a href="./content/sms-authoring.md">SMS 渠道</a>
    </td>
        <td>
      <img src="../assets/do-not-localize/icon_assets.svg" width="35px" alt="内容管理"><br/>
      <strong>内容管理</strong><br/><a href="./content/assets-overview.md">Assets概述</a><br/><a href="./content/email-templates.md">电子邮件模板</a><br/><a href="./content/fragments.md">视觉片段</a><br/><a href="./content/conditional-content.md">条件内容</a><br/><a href="./content/brand-themes.md">品牌主题</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-offer.svg" width="35px" alt="洞察和仪表板"><br/>
      <strong>Insights</strong><br/><a href="./dashboards/intelligent-dashboard.md">智能仪表板</a><br/><a href="./dashboards/engagement-dashboard.md">参与仪表板</a><br/><a href="./dashboards/buying-groups-dashboard.md">购买团体仪表板</a><br/><a href="./dashboards/journeys-dashboard.md">历程仪表板</a><br/><a href="./buying-groups/incrm-insights.md">In-CRM Insights</a>
    </td>

</tr>
</table>

## 其他资源

<table style="table-layout:fixed"><tr style="border: 0;">
<tr><td><strong>Adobe Journey Optimizer B2B Edition</strong><br/>
<a href="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-b2b-learn/tutorials/overview" target="_blank">视频和教程</a>——<a href="https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer-b2b.html" target="_blank">产品描述</a> <!-- - <a href="https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf" target="_blank">Security overview (PDF)</a> - <a href="https://developer.adobe.com/journey-optimizer-apis/" target="_blank">APIs reference</a> - <a href="https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html" target="_blank">Journey Optimizer Schema Dictionary</a> -->
</td>
<td><strong>Adobe Experience Platform</strong><br/>
<a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/landing/home" target="_blank">文档</a>——<a href="https://business.adobe.com/products/experience-platform/documentation-and-developer-resources.html" target="_blank">开发人员资源</a>
</td></tr>
<tr><td><strong>Adobe Real-Time Customer Data Platform</strong><br/>
<a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/rtcdp/home" target="_blank">文档</a>——<a href="https://experienceleague.adobe.com/zh-hans/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/overview" target="_blank">开发人员教程</a>
</td><td><strong>Adobe Marketo Engage</strong><br/>
<a href="https://experienceleague.adobe.com/zh-hans/docs/marketo/using/home" target="_blank">用户文档</a>——<a href="https://experienceleague.adobe.com/zh-hans/docs/marketo-developer/marketo/home" target="_blank">开发人员文档</a>
</td>
</tr></table>

