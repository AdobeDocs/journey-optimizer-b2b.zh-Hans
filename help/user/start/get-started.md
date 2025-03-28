---
title: Journey Optimizer B2B edition快速入门
description: 作为 Journey Optimizer B2B Edition 的新用户，了解入门的关键领域。
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: b403ff764c002796953956379e33fec6eb8c0611
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 10%

---

# Journey Optimizer B2B edition入门

您希望在Adobe Journey Optimizer B2B edition中处理的功能和工具取决于您在团队中的角色。

根据您的组织，管理员可以定义几种类型的用户，并根据用户的权限授予他们对特定功能的访问权限。

>[!TIP]
>
>此外，还要检查您的许可证授权和相应的[产品描述](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}，了解性能护栏和静态限制。

>[!BEGINTABS]

>[!TAB 管理员快速入门]

需要执行多个步骤来准备环境，然后您的团队才能开始使用Adobe Journey Optimizer B2B edition功能。 执行这些步骤，以便数据工程师和营销人员可以开始使用Adobe Journey Optimizer B2B edition。

作为系统管理员，您需要了解产品配置文件并为沙盒管理和渠道配置分配权限。 您还需要设置沙盒并对可用的产品配置文件管理沙盒。 然后，您可以将团队成员分配给产品配置文件。 这些功能可以由有权访问Adobe Admin Console的产品管理员管理。 [进一步了解 Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/using/admin-console.html)。

在以下页面中了解访问管理：

1. **创建沙盒**&#x200B;以将实例分割为单独的独立虚拟环境。[了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home#understanding-sandboxes)

1. **设置产品配置文件**。 产品配置文件是Adobe Experience Platform中的一组统一权限，允许用户访问界面中的特定功能或对象。 [了解详情](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **为产品配置文件（包括沙箱）设置用户权限**，并通过将团队成员分配给不同的产品配置文件来授予他们访问权限。 此任务在Admin Console中执行。 [了解详情](../admin/user-management.md#create-a-user-group)

1. **在Marketo Engage中配置电子邮件投放**，使您的团队能够通过帐户历程发送电子邮件内容。 [了解详情](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability)

1. **配置短信服务**。 在Adobe Journey Optimizer B2B edition中设置一个受支持的第三方短信提供商，这些提供商独立提供短信服务，并配置帐户凭据。 [了解详情](../admin/configure-channels-sms.md)

1. **为使用Adobe Experience Manager Assetsas a Cloud Service进行集中数字资源管理的团队配置并启用使用Assets**。 [了解详情](../admin/configure-aem-repositories.md)

1. **为负责创建监听AEP体验事件的帐户历程的团队设置Adobe Experience Platform (AEP) Experience Event定义**。 [了解详情](../admin/configure-aep-events.md)

>[!TAB 营销人员快速入门]

作为营销人员或&#x200B;_帐户历程从业者_，您负责设计历程和制作内容。 系统管理员和数据工程师准备好您的环境并授予您访问权限后，您即可开始使用Adobe Journey Optimizer B2B edition。

请参阅以下部分以设置您的第一个历程、添加资源和发送内容：

1. **添加帐户受众**。 Journey Optimizer B2B edition允许您直接从应用程序通过区段定义创建帐户受众，并将它们用于您的帐户历程。 [了解详情](../audiences/account-audience-overview.md)

1. **创建购买组**。 定义满足您的业务目标和目的的关键组件，并创建购买组以标识目标帐户列表的成员。 [了解详情](../buying-groups/buying-groups-overview.md)

1. **创建和管理资源**。Adobe Experience Manager Assets提供了单一集中式资源存储库，您可以使用它填充消息。 [了解详情](../content/assets-overview.md)

1. **添加个性化和动态电子邮件模板**。 利用Journey Optimizer B2B edition个性化和动态内容功能，根据受众调整消息。 [了解详情](../content/email-templates.md)

1. **设计帐户历程以提供个性化的情境式体验**。 Journey Optimizer B2B edition允许您利用存储在事件或数据源中的情境数据构建实时编排用例。 设计由以下功能提供支持的多步高级方案：

   * 实时发送由事件接收触发的单一投放，或使用Adobe Experience Platform受众批量发送。

   * 使用来自事件的上下文数据、来自Adobe Experience Platform的信息或来自第三方API服务的数据。

   * 使用内置渠道操作（电子邮件和短信）发送在Journey Optimizer B2B edition中设计的消息。

   * 在历程设计器中，构建分步式用例，添加条件并发送个性化消息。

[了解详情](../journeys/journey-overview.md)

>[!ENDTABS]
