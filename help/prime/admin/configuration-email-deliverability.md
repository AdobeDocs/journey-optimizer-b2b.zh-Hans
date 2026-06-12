---
title: 电子邮件投放能力和渠道配置
description: 为Journey Optimizer B2B Prime配置子域委派、DMARC、SPF、DKIM、IP池和电子邮件渠道配置。
autotag-review: '2026-06-12T22:43:42.799Z'
TQID: 'https://experienceleague.adobe.com/RKZSQkjSRvHixOm2faRT5D-yB00IykXfPO06vvIUQ6k'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 3414
ht-degree: 0%

---

# 电子邮件投放能力和渠道配置

[!DNL Adobe Journey Optimizer B2B Edition] Prime为B2B营销人员提供了现代的企业级电子邮件创作和投放体验。 此发行版本引入了重新设计的电子邮件设计工具和一组完整的电子邮件可投放性控制。

以下信息适用于配置发送基础架构以支持营销人员和电子邮件作者的管理员。 它描述了可投放性功能、角色和权限，以及如何配置子域、身份验证、IP池和渠道配置。

有关在电子邮件设计空间中创建电子邮件和创作电子邮件内容的详细信息，请参阅[电子邮件创作](../content/email-authoring.md)。

## 电子邮件渠道概述 {#overview}

* **可视化拖放电子邮件设计工具** — 使用结构、内容组件、主题、深色模式支持和可重用可视片段设计电子邮件内容。
* **电子邮件渠道配置** — 管理发件人身份、回复行为、营销与事务性消息类型以及跟踪。
* **电子邮件可投放性控制** — 设置您的电子邮件可投放性渠道，包括子域委派（完全委派和CNAME方法）、DMARC、SPF/DKIM自动配置和共享IP池支持。
* **发送电子邮件操作** — 在历程中，添加发送电子邮件操作，包括使用用户档案属性（Handlebars语法）进行个性化。
* **Marketo Design Studio资源** — 直接从电子邮件画布中的Marketo Engage资源库的一次性副本中选择图像和资源。
* **可重用的模板和片段** — 保存通用的页眉、页脚、CTA和完整的电子邮件布局，并在历程中重复使用。
* **基于角色的访问控制(RBAC)** — 应用粒度权限以创建、编辑、批准和发送电子邮件。

## 重要概念 {#key-concepts}

在配置电子邮件之前，请查看适用于整个产品中的电子邮件渠道功能的这些概念。

| 概念 | 在[!DNL Journey Optimizer B2B Edition] Prime中的含义 |
| ------- | ---------------------- |
| **_渠道配置_** | 可重用的一组电子邮件发送设置(包括发件人身份、回复地址、子域、IP池、电子邮件类型（营销或事务性）和跟踪)，可附加到历程中的电子邮件操作。 您可以为不同的品牌、业务部门或发送类型使用多个命名渠道配置。 |
| **_子域_** | 发送域的委派部分（例如，`mail.contoso.com`），用于通过Prime发送电子邮件。 子域可将您的B2B营销声誉与公司邮件或事务性邮件隔离。 |
| **_IP池_** | 与一个或多个子域关联的一组IP地址。 在此版本中，Prime支持由Adobe管理的共享IP池；专用IP池列在GA路线图中。 |
| **_电子邮件设计空间_** | 用于撰写电子邮件内容的可视化画布和设计工具。 它包括拖放布局组件、模板、片段、主题和个性化编辑器。 |
| **_模板_** | 可用于创建新电子邮件的可重用电子邮件布局。 模板可以是Adobe提供的内置示例模板，也可以是您的团队创建的自定义模板。 |
| **_可视片段_** | 可插入到多个电子邮件中的可重用内容块（例如页眉、页脚、CTA、法律免责声明）。 更新片段会将更改传播到使用它的每封电子邮件。 |
| **_主题_** | 可在电子邮件中应用的可重用样式预设（颜色、排版规则、间距、按钮样式）。 |
| **_Personalization令牌_** | 发送时，使用每个收件人的配置文件数据解析的Handlebars表达式（例如`{{profile.firstName}}`）。 |
| **_发送电子邮件操作_** | 历程操作节点，它使用渠道配置和电子邮件内容来投放电子邮件。 |

## 角色和权限 {#roles-permissions}

[!DNL Journey Optimizer B2B Edition] Prime对电子邮件功能使用基于角色的访问控制(RBAC)。 权限在Adobe Admin Console (IMS)中进行管理并在登录时同步。 产品管理员可为产品配置文件分配粒度权限，然后将这些产品配置文件附加到用户。

对[!DNL Journey Optimizer B2B Edition] Prime中电子邮件功能的访问权限由两层控制：

1. **功能标志(LD)。** LaunchDarkly标记可控制是否为贵组织打开了整个功能。 电子邮件创作和可投放性由`dx_ajo_btob_channel_foundation`控制。 如果没有此标记，则无论权限如何，都会隐藏该功能。
2. **功能权限。** 用户级别的权限，可控制特定用户是否可以在功能中读取或写入。

大多数电子邮件功能遵循`view-*` （读取）和`manage-*` （写入）模式。 用户需要具有读取权限才能在导航中查看功能，并且需要具有写入权限才能在其中创建、编辑或删除。

### 电子邮件创作权限 {#email-authoring-permissions}

| 功能 | 权限 | 它允许 |
| ---------- | ---------- | -------------- |
| **查看电子邮件** | `view-b2b-emails` | 查看电子邮件列表、打开电子邮件、查看内容（只读）。 |
| **创建/编辑/删除电子邮件** | `manage-b2b-emails` | 所有读取权限以及创建、编辑、复制和删除电子邮件。 需要在历程中创作电子邮件内容。 |
| **查看模板** | `view-b2b-templates` | 在“模板”库中浏览和预览模板（只读）。 |
| **创建/编辑/删除模板** | `manage-b2b-templates` | 全部读取权限以及创建、编辑和删除已保存的模板。 |
| **查看片段** | `view-b2b-fragments` | 浏览和预览可视化片段（只读）。 |
| **创建/编辑片段** | `manage-b2b-fragments` | 具有全部读取权限以及创建和编辑可视化片段。 |
| **发布片段** | `publish-b2b-fragments` | 发布片段，以使其可供整个组织的电子邮件作者使用。 |
| **管理共享资源和库项目** | `manage-b2b-library-items` | 管理模板、片段和电子邮件使用的底层共享库。 通常与模板/片段管理权限一起授予。 |
| **管理使用标签** | `manage-b2b-delete-usage-labels` | 管理附加到库项目的数据使用标签(DULE)以进行管理。 |
| **管理包** | `manage-b2b-packages` | 在沙盒之间捆绑并移动模板、片段和电子邮件。 |
| **查看资源（Prime中的Marketo Design Studio资源）** | `view-b2b-assets` | 浏览资产选取器并预览图像。 只读。 |
| **管理资产** | `manage-b2b-assets` | 所有读取权限以及未来的资源管理操作（Beta范围）。 |
| **导出邮件数据** | `manage-b2b-message-export` | 导出电子邮件级别的消息数据和报表。 |

在历程中，**发送电子邮件**&#x200B;操作需要`manage-b2b-person-journeys`（添加操作和激活历程）。 仅具有电子邮件权限的用户可以创作内容，但无法将电子邮件添加到历程。

### 电子邮件投放权限 {#email-deliverability-permissions}

可投放性功能（子域、DMARC、IP池、禁止列表、允许列表、IP预热计划和种子列表）是管理员级别的配置。 它们受两个权限管辖，这些权限涵盖整个&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件设置]**&#x200B;区域：

| 功能 | 权限 | 它允许 |
| ---------- | ---------- | -------------- |
| **查看电子邮件设置** | `view-b2b-email-settings` | 查看子域、PTR记录、IP池、禁止列表、允许列表、IP预热计划和种子列表（只读）。 |
| **管理电子邮件设置** | `manage-b2b-email-settings` | 所有读取权限以及委派子域、配置DMARC、管理禁止显示和允许列表、管理IP预热计划和种子列表。 |

电子邮件设置中的某些子功能由其他LaunchDarkly标志(禁止列表(`enable-suppression`)、允许列表(`enable-allow-list`)、种子列表(`enable-seedlist-ui`)来控制。 如果子功能在您的组织中不可见，请联系您的Adobe代表来启用标记。

### 渠道配置权限 {#channel-configuration-permissions}

渠道配置位于&#x200B;**[!UICONTROL 渠道]** → **[!UICONTROL 常规设置]**&#x200B;下。 它们将可投放性基元（子域、IP池、发件人身份）绑定到历程作者引用的可重用对象。 它们受单一权限管理：

| 功能 | 权限 | 它允许 |
| ---------- | ---------- | -------------- |
| **管理渠道配置** | `manage-b2b-channels-configurations` | 查看、创建、编辑和删除电子邮件渠道配置。 |

## 电子邮件可投放性概述 {#deliverability-overview}

[!DNL Journey Optimizer B2B Edition] Prime中的电子邮件可投放性是一组基础架构和身份验证配置，可帮助电子邮件到达收件人的收件箱，而不是垃圾邮件文件夹，并且不会被ISP（Internet服务提供商）阻止。

它使用以下构建基块，这些构建基块由管理员配置，通常按以下顺序配置：

1. 将一个或多个子域委派到Adobe。
1. 在每个子域上配置DMARC、SPF和DKIM记录。
1. 确认将为子域发送电子邮件的IP池。
1. 创建一个或多个绑定子域、IP池和发件人身份的电子邮件渠道配置。
1. 在历程电子邮件操作中使用这些渠道配置。

>[!TIP]
>
>将可投放性设置视为每个业务部门或品牌的一次性管理员活动。 配置后，营销人员和电子邮件作者无需重新访问它。

## 子域委派 {#subdomain-delegation}

子域委派会告知Internet已授权Adobe代表域的特定子域（例如，`mail.contoso.com`）发送电子邮件。 委派专用子域（而不是根域）可保护您的公司邮件，从而实现

* **信誉隔离。** 营销发送与公司邮件分开。 如果营销信誉下降，您的交易邮件和公司邮件不会受到影响。
* **更快的IP预热速度。** 专用子域有助于在ISP中更快地建立积极的发件人信誉。
* **新式身份验证。** SPF、DKIM和DMARC可以按子域进行干净设置，而不会影响其他邮件流。
* **合规性。** 帮助满足Gmail、Yahoo和其他主要ISP的批量发件人要求。

>[!NOTE]
>
>Prime中的每个子域只能由一个Adobe产品使用。 您不能在Prime和其他产品（如Adobe Marketo Engage或Adobe Campaign）之间共享相同的发送子域，您必须使用不同的子域。

### 支持的方法

Prime支持Alpha中的三种子域委派方法中的两种。 第三种方法（自定义委派）正在制定中。

| 方法 | 使用时间 | 它包含的内容 |
| ------ | ----------- | ---------------- |
| **已完全委派** | 推荐 | 将子域的完整DNS特权委派给Adobe。 Adobe创建并维护MX、SPF、DKIM、DMARC、A和CNAME记录。 操作开销最低。 Adobe会为您处理DNS更改。 |
| **CNAME** | 对于受限策略 | 保留DNS权限，并创建指向Adobe管理的记录的CNAME记录。 当贵组织的DNS策略不允许完全委派时，使用此选项。 您负责维护DNS记录。 |
| **自定义委派** | 路线图(GA) | 维护DNS和SSL证书的完全所有权。 提供最大程度的控制，包括使用您自己的证书的能力。 这是针对GA版本进行的。 |

### 委派子域（完全委派方法） {#delegate-fully-delegated}

>[!PREREQUISITES]
>
>* 决定子域命名约定（例如，`mail.contoso.com`表示营销，`alerts.contoso.com`表示事务型）。
>* 与您的IT/DNS团队确认，他们可以将子域（NS记录）委派给Adobe。
>* 在DNS提供商中创建新的子域，然后等待24-48小时以进行DNS传播，然后再委派给Adobe。
>* 确认您在Prime中具有“管理员”角色。

1. [!DNL Adobe Journey Optimizer B2B Edition] Prime，导航到&#x200B;**[!UICONTROL 管理]** → **[!UICONTROL 渠道]** → **[!UICONTROL 电子邮件设置]** → **[!UICONTROL 子域]**。
1. 单击&#x200B;**[!UICONTROL 设置子域]**。
1. 输入完整的子域名（例如，`mail.contoso.com`）。
1. 选择&#x200B;**[!UICONTROL 完全委派]**&#x200B;作为委派方法。
1. 为子域配置DMARC（请参阅[DMARC、SPF和DKIM](#dmarc-spf-dkim)）。

   至少应使用开始策略`none`设置DMARC记录，以便您可以在不影响投放的情况下监视报告。

1. 查看要由Adobe管理的DNS记录列表。

   这些记录通常包括MX、SPF、DKIM、DMARC、A和CNAME记录（用于跟踪和镜像页面URL）。

1. 使用&#x200B;**[!UICONTROL 下载记录]**&#x200B;按钮将DNS记录下载为CSV文件。 与您的DNS团队共享此文件。

1. 您的DNS团队会添加域托管解决方案中的NS记录，该解决方案可将子域委派给Adobe。

1. 在您的DNS团队确认记录已到位后，返回到[!DNL Journey Optimizer B2B Edition] Prime并选中确认您已在托管网站上创建所需记录的框。

1. 单击&#x200B;**[!UICONTROL 提交]**&#x200B;以启动一系列验证检查（预验证、MX、SPF、DKIM、DMARC、FBL注册）。

1. 等待子域状态更改为&#x200B;**[!UICONTROL 成功]**。

   DNS传播完成后，这通常需要几分钟的时间。

>[!NOTE]
>
>如果验证失败，则状态将更改为&#x200B;**[!UICONTROL 失败]**，[!DNL Journey Optimizer B2B Edition]Prime将显示原因（例如，未找到NS记录、MX记录缺失或DMARC配置错误）。 请修复基本DNS问题，然后重试提交。

### 委派子域（CNAME方法） {#delegate-cname}

仅当贵组织的DNS策略禁止完全委派时，才使用此方法。 使用CNAME，您可以保留DNS记录。

1. 在[!DNL Adobe Journey Optimizer B2B Edition] Prime中，导航到&#x200B;**[!UICONTROL 管理]** → **[!UICONTROL 渠道]** → **[!UICONTROL 电子邮件设置]** → **[!UICONTROL 子域]**。
1. 单击&#x200B;**[!UICONTROL 设置子域]**。
1. 输入完整的子域名。
1. 选择&#x200B;**[!UICONTROL CNAME]**&#x200B;作为委派方法。
1. 为子域（[DMARC、SPF和DKIM](#dmarc-spf-dkim)）配置DMARC。
1. 查看Prime生成的CNAME记录列表 — 这些记录将您子域的组件指向Adobe管理的记录。
1. 以CSV格式下载记录并与您的DNS团队共享。
1. 您的DNS团队将每个CNAME记录添加到您的DNS托管解决方案。
1. 记录到位并传播后，请返回Prime并进行确认。 单击&#x200B;**[!UICONTROL 提交]**。
1. 等待状态达到&#x200B;**[!UICONTROL 成功]**。

>[!IMPORTANT]
>
>使用CNAME，Adobe无法帮助您更改、维护子域的DNS或对其进行故障排除。 任何未来的更改（例如，为功能更新添加新的CNAME）都必须由您的DNS团队进行。

### 子域护栏 {#subdomain-guardrails}

* **默认限制：**&#x200B;每个组织10个子域。 如果您需要更多（最多100个，具体取决于合同），请联系您的Adobe代表。
* **DNS传播：**&#x200B;允许24-48小时让更改在全球传播。 验证可能会失败，原因只是DNS尚未传播。
* **子域重用：**&#x200B;其他Adobe产品(Marketo Engage、Adobe Campaign)已使用的子域不能在Prime中重用。

## DMARC、SPF和DKIM {#dmarc-spf-dkim}

DMARC、SPF和DKIM是电子邮件身份验证标准。 它们共同向接收邮件服务器证明您的邮件确实代表您的域发送，并且未被欺骗。 现代ISP(Gmail、Yahoo、Microsoft)要求批量发件人遵守这些标准。

| 记录 | 表示 | 用途 |
| ------ | ---------- | ------- |
| **SPF** | 发件人策略框架 | 列出允许从域发送邮件的邮件服务器IP。 接收服务器拒绝来自此列表以外的IP的邮件。 当您委派子域（完全委派）时，Adobe会自动创建并维护SPF记录。 |
| **DKIM** | 域密钥标识的邮件 | 向每个出站电子邮件中添加了加密签名。 接收服务器根据DNS中发布的公钥验证签名。 Adobe在子域委派期间自动生成DKIM密钥和DNS记录。 |
| **DMARC** | 基于域的消息验证、报告和符合性 | 告知接收服务器如果SPF或DKIM失败该怎么做，并提供有关身份验证结果的报告。 DMARC具有三种策略模式：无、隔离和拒绝。 |

### DMARC策略模式

| 策略 | 操作 | 使用时间 |
| ------ | ------ | ----------- |
| `none` | 监测 | 如果DMARC失败，接收服务器不执行任何操作，但仍会发送报表。 在首次委派子域以确认身份验证工作正常且不会丢失消息时，请使用此选项。 |
| `quarantine` | 隔离 | 接收服务器将失败邮件放入垃圾邮件/垃圾邮件文件夹中。 |
| `reject` | 拒绝 | 接收服务器拒绝（退回）身份验证失败的消息。 最严格的模式。 一旦您对身份验证设置充满信心，则建议使用。 |

### 配置DMARC {#configure-dmarc}

DMARC在委派子域时进行配置，但您也可以为已委派的子域添加或更新DMARC 。

1. 导航到&#x200B;**[!UICONTROL 管理]** → **[!UICONTROL 渠道]** → **[!UICONTROL 电子邮件设置]** → **[!UICONTROL 子域]**。

1. 在子域列表中，找到您的子域，并检查DMARC记录列。

   如果缺少记录，则会显示警报。

1. 打开子域并滚动到DMARC记录部分。

   * 如果父域上已存在DMARC记录，[!DNL Journey Optimizer B2B Edition] Prime将自动获取值。 您可以保留或覆盖。
   * 如果不存在记录，请选择&#x200B;**[!UICONTROL 使用Adobe管理]**，Adobe将创建并托管DMARC记录。

1. 设置策略： `none`、`quarantine`或`reject`。 除非您的父域上已有成熟的DMARC状态，否则请以`none`开始。

1. （可选）配置其他DMARC标记（子域策略为`sp`，百分比为`pct`，报表地址为`rua`和`ruf`）。

1. 如果使用完全委派，请单击&#x200B;**[!UICONTROL 保存]**。

   Adobe会自动应用记录。 如果使用CNAME，请复制DNS记录并让您的DNS团队添加它，然后在[!DNL Journey Optimizer B2B Edition] Prime中确认。

1. 允许DNS传播长达48小时，然后验证子域页面上的DMARC状态指示器是否绿色/正常。

>[!TIP]
>
>从`policy=none`开始监视身份验证报告，然后进展到`quarantine`，最后在报告显示健康的SPF和DKIM对齐时再进展到`reject`。 直接移至`reject`而不进行监视可能会导致合法邮件被拒绝。

## IP池 {#ip-pools}

IP池是用于发送电子邮件的已命名IP地址组。 IP池对发件人的信誉至关重要：每个池在ISP中都有自己的信誉，因此一个池的问题（例如，触发垃圾邮件投诉的营销突发）不会污染另一个池（例如，事务确认）。

### 池类型

| 池类型 | 可用性 | 描述 |
| --------- | ------------ | ----------- |
| **共享IP池** | 可在Alpha上获取 | 由Adobe管理并在多个客户之间共享的IP地址池。 Adobe在整个池中维护声誉。 最适合中低级电子邮件数量和不想管理IP预热的客户。 |
| **专用IP池** | 路线图(GA) | 专门分配给贵组织的一个或多个IP地址。 名声归你所有。 建议大容量发件人使用。 包括IP预热计划和PTR记录管理。 |

### 查看和分配IP池 {#review-ip-pool}

在此版本中，为您的组织预配置了IP池。 在创建电子邮件渠道配置时分配IP池。

1. 导航到&#x200B;**[!UICONTROL 管理]** → **[!UICONTROL 渠道]** → **[!UICONTROL 电子邮件设置]** → **[!UICONTROL IP池]**。
1. 确认您的组织可以使用状态为&#x200B;**[!UICONTROL 活动]**&#x200B;的IP池。
1. 将鼠标悬停在池上以查看IP地址及其PTR记录（反向DNS）。
1. 如果您的组织有多个业务部门或品牌，请在创建渠道配置之前规划如何使用IP池（例如，营销池与网络研讨会池）。

>[!IMPORTANT]
>
>即使共享池可用，也不要在同一IP池上混合使用营销和事务性流量。 渠道配置中的电子邮件类型设置（营销型与事务型）可控制禁止行为，但您的渠道配置仍应尽可能使用不同的池。

## 电子邮件渠道配置 {#email-channel-configurations}

渠道配置是将发件人身份、子域、IP池和跟踪设置绑定在一起的中心对象。 历程中的电子邮件操作引用渠道配置以了解如何发送消息：

* **渠道：**&#x200B;电子邮件。
* **电子邮件类型：**&#x200B;营销或事务性。 此设置确定是否应用禁止显示规则（营销应用这些规则；默认情况下，事务型消息绕过合法事务型消息的垃圾邮件投诉禁止显示）。
* **标头参数：**&#x200B;来自姓名、电子邮件、回复姓名、回复电子邮件、错误电子邮件。
* **子域：**&#x200B;用于发送的已委派子域。 发件人电子邮件必须使用此子域。
* **IP池：**&#x200B;用于传递消息的IP池。
* **URL跟踪：**&#x200B;启用或禁用点击并打开跟踪；配置跟踪域。
* **标记：**&#x200B;组织和搜索标记。

### 创建电子邮件渠道配置 {#create-email-channel-configuration}

>[!PREREQUISITES]
>
>* 必须至少委派一个子域且处于活动状态。
>* 必须为您的组织至少分配一个IP池。
>* 您需要管理员角色。

1. 导航到&#x200B;**[!UICONTROL 渠道]** → **[!UICONTROL 常规设置]** → **[!UICONTROL 渠道配置]**。
1. 单击&#x200B;**[!UICONTROL 创建渠道配置]**。
1. 输入名称（例如“Contoso B2B Marketing — North America”）和可选的描述。
1. 选择&#x200B;**[!UICONTROL 电子邮件]**&#x200B;渠道。
1. （可选）选择标记以对配置进行分类。
1. 在&#x200B;**[!UICONTROL 电子邮件类型]**&#x200B;部分中，选择“营销”或“事务性”。
1. 在&#x200B;**[!UICONTROL 子域]**&#x200B;部分中，选择之前委派的子域。
1. 在&#x200B;**[!UICONTROL IP池]**&#x200B;部分中，选择一个活动的IP池。 您可以将鼠标悬停在IP上以查看PTR记录。
1. 配置&#x200B;**[!UICONTROL 标头参数]**：
   * 源名称（例如“Contoso Marketing”）。
   * 发件人电子邮件 — 必须使用选定的子域（例如，`marketing@mail.contoso.com`）。
   * 回复姓名和回复电子邮件 — 如果为空，则默认为从。
   * 错误电子邮件 — 接收未送达通知的地址。
1. 启用&#x200B;**[!UICONTROL URL跟踪]**&#x200B;并选择跟踪域。
1. 单击&#x200B;**[!UICONTROL 提交]**。
1. Prime运行验证：子域状态、MX记录、SPF/DKIM/DMARC校准、IP池准备情况、FBL注册。 配置将通过“草稿”→“处理”→“活动”。

>[!NOTE]
>
>如果验证失败，配置将移至&#x200B;**[!UICONTROL 失败]**&#x200B;状态。 打开配置以查看失败原因 — 常见原因是MX记录验证失败、池中的IP与配置不匹配或DMARC未对齐。 解决并重新提交。

### 编辑或删除渠道配置 {#edit-channel-configuration}

您可以在创建渠道配置后进行编辑，但具有一个重要限制：

* 无法更改&#x200B;**渠道。** 配置已绑定到其通道。

编辑正在使用的配置时：

* **对于已发布的历程：**，此更改将在下次循环或下次执行时应用。 在执行中，执行将继续使用以前的设置。
* **对于事务性或实时消息：**&#x200B;更改会在大约五分钟内传播。

要删除配置，请先删除或更新引用该配置的每个电子邮件操作。[!DNL Journey Optimizer B2B Edition] Prime不会删除活动历程当前使用的配置。

### 多渠道配置 {#multiple-channel-configurations}

大多数B2B组织都使用多个渠道配置来分隔品牌、区域或发送类型。 常见模式：

* 每个业务部门的独立营销配置（例如，*BU-A营销*、*BU-B营销*）。
* 用于产品或合同通知的专用事务型配置，其电子邮件类型为“事务型”。
* 使用特定于区域的子域（例如，`mail.eu.contoso.com`、`mail.us.contoso.com`）的区域特定配置与区域ISP和合规性保持一致。

>[!TIP]
>
>使用清晰的结构化约定命名您的配置 — 例如： *[品牌] - [地区] - [类型]*。 一旦您拥有十几个或更多配置，这一点就变得至关重要。

### 已知限制 {#known-limitations}

* 子域委派的&#x200B;**自定义委派方法**&#x200B;尚不可用 — 请使用“完全委派”或CNAME。 自定义委派面向GA。
* 在Alpha中，**专用IP池**&#x200B;不可用。 共享IP池是唯一选项。 在GA提供专用IP ，包括IP预热计划和PTR记录管理。
* 通过.html或.zip上传的&#x200B;**HTML导入**&#x200B;在Alpha上受到限制。 完整的HTML导入（包括代码编辑器+可视画布双视图、验证和内联CSS自动转换）位于Beta。
* Prime中的&#x200B;**本机图像上传和DAM**（上传、组织、编辑）位于Beta路线图中。 在此版本中使用Marketo Design Studio资源。 Marketo中的重新上传操作不反映在Prime中。
* **测试用户档案、模拟内容和发送校样**&#x200B;在此版本中不可用。 Litmus渲染和基于SpamAssassin的垃圾邮件报告都在Beta路线图上。
* **此版本中没有帐户级别的个性化和自定义对象数据**。 使用配置文件属性。
* 正式发行时&#x200B;**Velocity到Handlebars自动迁移**&#x200B;现有的Marketo模板。
* 在快速跟进版本中发送电子邮件&#x200B;**（内联评论、@mentions件、请求审阅工作流）上的**&#x200B;评论和协作。
* **AEM Assets、AEM Content Fragments和Adobe Express**&#x200B;集成位于“快速跟进”路线图上。

<!--

### Frequently asked questions {#faq}

| Question | Answer |
| -------- | ------ |
| **Can I reuse the subdomain I already use in Marketo Engage?** | No. A subdomain can only be associated with one Adobe product at a time. Create a new subdomain (for example, mail2.contoso.com) for Prime. |
| **Why does my channel configuration show Failed?** | The most common reasons are: MX record validation failed (your subdomain DNS isn't fully configured); DMARC misalignment; or an IP pool that is in Processing and has never been associated with the selected subdomain. Open the configuration to see the specific reason. |
| **What happens if a personalization token has no value at send time?** | If you defined a fallback with the Handlebars `default` helper, the fallback is used. If not, the token resolves to an empty string. Prime warns you when a token has no fallback and the underlying attribute is not guaranteed by the audience definition. |
| **Can I personalize using account-level attributes?** | Not in this release. Personalization in Prime today supports profile attributes only. |
| **What's the maximum email size?** | 100 KB is the recommended best-practice cap for inbox rendering. Prime warns you in the editor if you exceed it. |
| **Can I migrate existing Marketo email templates into Prime?** | A guided self-serve migration tool — including Velocity-to-Handlebars conversion — is delivered at GA. In this release, you can manually rebuild templates or paste raw HTML. |
| **Will my updates to Marketo assets show up in Prime?** | No. Asset availability in Prime is based on a one-time copy from Marketo Design Studio. Re-uploaded or modified Marketo assets are not reflected in Prime today. Native asset upload and management within Prime is on the Beta roadmap. |

## Glossary {#glossary}

| Term | Definition |
| ---- | ---------- |
| **DKIM** | DomainKeys Identified Mail — cryptographic email signature. |
| **DMARC** | Domain-based Message Authentication, Reporting & Conformance. |
| **FBL** | Feedback Loop — a service ISPs offer to receive spam-complaint reports back to senders. |
| **Handlebars** | JavaScript templating language used in Prime for personalization expressions. |
| **IP pool** | Group of IP addresses used to send email. |
| **MX record** | Mail Exchange DNS record — directs incoming mail to the correct mail servers. |
| **NS record** | Name Server DNS record — used to delegate a subdomain. |
| **PTR record** | Pointer record — reverse DNS that maps an IP address back to a hostname. |
| **RBAC** | Role-Based Access Control. |
| **SPF** | Sender Policy Framework — DNS record listing authorized sending IPs. |
| **Subdomain delegation** | Granting Adobe authority over a portion of your domain (a subdomain) for sending email. |

-->
