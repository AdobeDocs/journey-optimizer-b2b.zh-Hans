---
title: Adobe Journey Optimizer B2B Edition 文档
description: Journey Optimizer B2B Edition 的完整文档——浏览可用于加入、创建购买群组、生成帐户历程和管理内容的资源。
exl-id: 3d7b6c82-95c3-4d89-b3dc-7fd5b0aef615
source-git-commit: 0e79785bd8baf3914127cc650b8e503a8d461a3d
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 29%

---

# Adobe Journey Optimizer B2B Edition 文档

[!DNL Adobe Journey Optimizer B2B Edition]是首创的应用程序，它允许营销和销售团队在整个客户生命周期中编排基于帐户的体验，并使购买组有资格购买特定产品。 它利用AI吸引和授权目标客户中的购买群体，帮助您的团队形成更高质量的管道，设计更好的收购、扩展和保留策略。 它还支持在销售和营销团队之间共享见解。

本文档提供了有关如何掌握应用程序的信息。 它专为营销人员、业务开发代表、数据分析师和运营管理员而设计。

## 新增功能

查看[!DNL Journey Optimizer B2B Edition]应用程序和文档中的最新添加和增强功能的此抽样。

>[!BEGINTABS]

>[!TAB AI代理]

借助[Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/home#agent-orchestrator){target="_blank"}，AI Assistant界面可自动调用专业代理以获取正确的答案和见解。 Agent Orchestrator 会记住您的对话历史，使您能够自然地延续以前的问题，无需重复上下文，它还会结合来自多个代理的洞察，为您提供清晰、统一的回答。 在[!DNL Journey Optimizer B2B Edition]上下文中，有三个针对特定B2B任务和域的专门构建代理：

* [Audience Agent B2B](./agents/audience-agent-b2b.md)
* [Journey Agent B2B](./agents/journey-agent.md)
* [Account Qualification 代理](./agents/sales-qualifier.md#account-qualification-agent)

>[!TAB WhatsApp渠道]

当开发人员和产品管理员配置与Meta Business Manager帐户的集成时，营销人员可以使用Meta Cloud API将WhatsApp消息作为内容渠道包含在帐户历程中。 WhatsApp将电子邮件和短信作为直接将历程内容交付给帐户成员的可用渠道。

[!BADGE 了解详情]{type=Informative url="/help/user/admin/configure-channels-whatsapp.md" tooltip="了解WhatsApp渠道"}

>[!TAB 生成AI模型]

在为电子邮件内容生成图像时，电子邮件设计人员现在可以从标准[!DNL Firefly]模型、基于品牌特定资产培训的自定义[!DNL Firefly]模型和批准的第三方图像模型中进行选择。 从一般内容需求到品牌或专业用例，此选择使团队能够控制哪些模型适合其特定设计情景。

[!BADGE 了解详情]{type=Informative url="/help/user/content/generative-ai-models.md" tooltip="了解创作AI模型选择"}

>[!TAB 发送时间优化]

对于个人历程中的&#x200B;_发送电子邮件_&#x200B;操作节点，您现在可以使用发送时间优化来个性化电子邮件投放时间。 该系统预测每个人何时最有可能参与并相应地计划投放，而不是同时发送给所有收件人。

[!BADGE 了解详情]{type=Informative url="/help/user/content/email-send-time-optimization.md" tooltip="了解发送时间优化"}

>[!TAB 历程重新进入]

您现在可以通过帐户历程工作流多次发送帐户/人员。 重返工作涉及多种情形，例如重新评估资格标准和可重复使用的培养工作流程。 使用重新进入设置来设置标准、限制和等待时间，以便帐户需要以可控方式完成历程。

[!BADGE 了解详情]{type=Informative url="/help/user/journeys/journey-re-entry.md" tooltip="了解历程重新进入"}

>[!TAB 品牌主题]

通过主题，非技术设计人员能够创建符合特定品牌和样式的可重用电子邮件内容设计准则。 主题使营销人员能够更快地利用具有视觉吸引力、品牌一致的电子邮件，而且所需的工作量更少，并提供高级自定义选项以满足独特的设计需求。

[!BADGE 了解详情]{type=Informative url="/help/user/content/brand-themes.md" tooltip="了解品牌主题"}

>[!TAB 角色映射]

营销人员可以定义详细的用户档案，包括背景、职责、棘手问题和首选通信渠道。 使用这些定义，管理员可以根据[!DNL Journey Optimizer B2B Edition]中的人员属性配置角色，以便角色模板可以使用简化且一致的角色条件来捕获这些角色。

[!BADGE 了解详情]{type=Informative url="/help/user/admin/persona-mapping.md" tooltip="了解角色映射"}

>[!ENDTABS]

## 开始浏览 {#section-explore}

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hans)

最新发行说明

了解Adobe Journey Optimizer B2B edition中的最新发行说明、新增功能和改进。

[查看发行说明](./release-notes/release-notes.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hans)

快速入门

查看Journey Optimizer B2B edition管理员和营销人员入门指南。

[快速入门](./start/get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hans)

配置XDM字段

实施系统配置以激活要在Adobe Journey Optimizer B2B edition中使用的XDM架构和字段。

[查看XDM字段管理](./admin/xdm-field-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hans)

通信渠道

配置和管理电子邮件、短信、WhatsApp和其他渠道，以提供个性化的客户互动。

[配置电子邮件渠道](./admin/configure-channels-emails.md)
[配置短信渠道](./admin/configure-channels-sms.md)
[配置WhatsApp渠道](./admin/configure-channels-whatsapp.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hans)

创建帐户历程

设计、编排、管理和优化个性化的帐户历程。

[探索历程](./journeys/journeys-overview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/users.svg?lang=zh-Hans)

了解购买组

有关创建、管理和优化购买群体以实现有效定位的详细指导。

[了解购买群组](./buying-groups/buying-groups-overview.md)
:::

::::

<!-- 
:::
![icon](https://cdn.experienceleague.adobe.com/icons/image.svg?lang=zh-Hans)

Design Content

Learn how to author and manage content for personalized customer experiences orchestrated through journeys.

[Explore Content Components](./content/content-components.md)
::: 
-->

## 概述演示

探索购买群组的组成部分，了解构建帐户历程的基础知识。

>[!VIDEO](https://video.tv.adobe.com/v/3432054?quality=12)

## 浏览文档

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
      <strong>帐户历程</strong><br/><a href="./journeys/journeys-overview.md">历程概述</a><br/><a href="./journeys/create-publish-journey.md#create-a-journey">创建帐户历程</a><br/><a href="./journeys/journey-nodes.md">历程节点</a>
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

<table style="table-layout:fixed">
<tr><td><strong>Adobe Journey Optimizer B2B edition</strong><br/>
<a href="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-b2b-learn/tutorials/overview" target="_blank">视频和教程</a> - <a href="https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer-b2b.html" target="_blank">产品说明</a> <!-- - <a href="https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf" target="_blank">Security overview (PDF)</a> - <a href="https://developer.adobe.com/journey-optimizer-apis/" target="_blank">APIs reference</a> - <a href="https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=zh-Hans" target="_blank">Journey Optimizer Schema Dictionary</a> -->
</td>
<td><strong>Adobe Experience Platform</strong><br/>
<a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/landing/home" target="_blank">文档</a> - <a href="https://business.adobe.com/cn/products/experience-platform/documentation-and-developer-resources.html" target="_blank">开发人员资源</a>
</td></tr>
<tr><td><strong>Adobe Real-Time Customer Data Platform</strong><br/>
<a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/rtcdp/home" target="_blank">文档</a> - <a href="https://experienceleague.adobe.com/zh-hans/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/overview" target="_blank">开发人员教程</a>
</td><td><strong>Adobe Marketo Engage</strong><br/>
<a href="https://experienceleague.adobe.com/zh-hans/docs/marketo/using/home" target="_blank">用户文档</a> - <a href="https://experienceleague.adobe.com/zh-hans/docs/marketo-developer/marketo/home" target="_blank">开发人员文档</a>
</td>
</tr></table>

