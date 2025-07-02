---
title: 管理员和营销人员入门指南
description: 作为 Journey Optimizer B2B Edition 的新管理员或用户，请了解入门流程中的关键环节。
role: Admin, User
level: Beginner
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: d0bd2d5153b972df92ff42c6f1eebb25448b222f
workflow-type: ht
source-wordcount: '685'
ht-degree: 100%

---

# 入门指南

您在 Adobe Journey Optimizer B2B Edition 中需要使用的功能和工具，取决于您在团队中的角色。根据组织架构，管理员可定义多种用户类型，并根据其权限授予相应功能的访问权限。

>[!TIP]
>
>此外，请检查您的许可证权利和相应的[产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}，了解性能护栏和静态限制。

>[!BEGINTABS]

>[!TAB 管理员]

在您的团队开始使用 Adobe Journey Optimizer B2B Edition 功能之前，需要通过几个步骤来准备您的环境。请执行这些步骤，以便数据工程师和营销人员可以开始使用 Adobe Journey Optimizer B2B Edition。

作为系统管理员，您需要了解产品轮廓，以及分配沙盒管理和渠道配置的权限。您还需要设置沙盒，并为可用的产品轮廓管理这些沙盒。然后，您可以将团队成员分配给产品轮廓。具备 Adobe Admin Console 访问权限的产品管理员可对这些功能进行管理。[进一步了解 Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/using/admin-console.html)。

在以下页面中了解访问管理：

1. **创建沙盒**&#x200B;以将实例分割为单独的独立虚拟环境。[了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sandbox/home#understanding-sandboxes){target="_blank"}

1. **与您的数据工程师协作**，共同规划并实施 B2B 受众与轮廓的激活策略。查看已发布的蓝图，并根据您的需求遵循相关指南。[了解详情](https://experienceleague.adobe.com/zh-hans/docs/blueprints-learn/architecture/b2b-activation/overview){target="_blank"}

1. **设置产品轮廓**。产品轮廓是 Adobe Experience Platform 中的一组单一权利，这些权利允许用户访问界面中的某些功能或对象。[了解详情](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. 为包括沙盒在内的产品轮廓&#x200B;**设置用户权限**，将团队成员分配给不同的产品轮廓，由此授予他们访问权限。在 Admin Console 中可完成此任务。[了解详情](../admin/user-management.md#create-a-user-group)

1. 在 Marketo Engage 中&#x200B;**配置电子邮件传递**，以便您的团队可以从帐户历程中发送电子邮件内容。[了解详情](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability){target="_blank"}

1. **配置 SMS 服务**。设置其中一个受支持的第三方 SMS 提供商，该提供商独立提供文本消息服务，并在 Adobe Journey Optimizer B2B Edition 中配置帐户凭据。[了解详情](../admin/configure-channels-sms.md)

1. 为使用 Assets as a Cloud Service 进行集中数字资产管理的团队&#x200B;**配置并启用 Adobe Experience Manager Assets**。[了解详情](../admin/configure-aem-repositories.md)

1. 为负责创建帐户历程并监听 AEP 体验事件的团队&#x200B;**设置 Adobe Experience Platform (AEP) 体验事件定义**。[了解详情](../admin/configure-aep-events.md)

>[!TAB 营销人员]

作为营销人员或&#x200B;_帐户历程实践者_，您负责设计历程和制作内容。系统管理员和数据工程师准备好您的环境并授予您访问权限后，您就可以开始使用 Adobe Journey Optimizer B2B Edition。

请参阅以下部分，以设置第一个历程、添加资产并发送内容：

1. **添加帐户受众**。Journey Optimizer B2B Edition 允许您通过区段定义直接从应用程序创建帐户受众，并将其用于帐户历程。[了解详情](../audiences/account-audience-overview.md)

1. **创建购买群组**。定义满足您的业务目标和目的的关键组件，并创建购买群组来确定目标帐户列表的成员。[了解详情](../buying-groups/buying-groups-overview.md)

1. **创建和管理资产**。Adobe Experience Manager Assets 提供了一个集中式资产存储库，您可以使用它来填充您的消息。[了解详情](../content/assets-overview.md)

1. **添加个性化的动态电子邮件模板**。利用 Journey Optimizer B2B Edition 个性化的动态内容功能，根据受众调整消息。[了解详情](../content/email-templates.md)

1. **设计帐户历程，以提供个性化的上下文体验**。Journey Optimizer B2B Edition 允许您利用事件或数据源中存储的上下文数据来构建实时编排用例。设计由以下功能提供支持的多步骤高级场景：

   * 使用 Adobe Experience Platform 受众在接收到事件时触发发送实时单一投放，或进行批量处理。

   * 利用来自事件的上下文数据、来自 Adobe Experience Platform 的信息或来自第三方 API 服务的数据。

   * 使用内置渠道操作（电子邮件和 SMS）发送在 Journey Optimizer B2B Edition 中设计的消息。

   * 在历程地图中构建多步骤用例、添加条件、发送个性化消息。

[了解详情](../journeys/journey-overview.md)

>[!ENDTABS]
