---
title: 设置电子邮件跟踪和投放
description: 配置电子邮件传递协议——设置 DNS、SPF、DKIM、DMARC 和 IP 允许列表，以便在 Journey Optimizer B2B Edition 中实现最佳跟踪和供应能力。
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: 944d2616fa21e7f8d2f8c439eaa2f5e529dacb84
workflow-type: tm+mt
source-wordcount: '2396'
ht-degree: 99%

---

# 设置电子邮件跟踪和投放

Adobe Journey Optimizer B2B edition利用附加的Marketo Engage实例中的电子邮件渠道功能和事件跟踪。 为了确保使用限制性防火墙或代理服务器设置的组织的电子邮件传递能够按预期进行，系统管理员必须将某些域和 IP 地址范围添加到允许列表中。

>[!NOTE]
>
>如果贵组织已使用连接的Marketo Engage实例运行营销操作，则这些协议和配置应已准备就绪。

确保将以下域（包括星号）添加到允许列表中，以启用所有 Marketo Engage 资源和 WebSockets：

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

按照以下步骤操作，以确保追踪和电子邮件传递正常：

1. [为登陆页面和电子邮件创建DNS记录](#create-dns-records-for-landing-pages-and-email)
1. [设置 SPF 和 DKIM](#set-up-spf-and-dkim)
1. [设置 DMARC](#set-up-dmarc)
1. [为您的域设置 MX 记录](#set-up-mx-records-for-your-domain)
1. [将出站 IP 地址添加到允许列表](#outbound-ip-addresses)

>[!NOTE]
>
>电子邮件可投放性服务和咨询是独立于Adobe的付费产品。 如果您需要或希望可交付性团队为Journey Optimizer B2B edition实例提供支持，则必须购买该实例的其中一个电子邮件可交付性服务包（Essentials、Enhanced或Plus）。 这与预先存在的Marketo Engage实例上的任何可投放性包无关。 可投放性服务是按实例附加的，而不是按组织附加的。 两个实例上的可投放性支持都需要两个单独的Deliverability Services包。 每当为Journey Optimizer B2B edition配置新IP时，都需要一个新的可交付性服务包来进行IP预热和持续的可交付性支持。

## 为登陆页面和电子邮件创建DNS记录

连接 CNAME 记录可以让营销人员托管电子邮件、登陆页面和博客的网页版本，保持一致的品牌形象，从而提升流量和转化率。 强烈建议您将 CNAME 添加到您的根域主机，以便 Marketo Engage 托管您的以营销为中心的网络资产。 作为管理员，您应该与您的营销团队合作，为通过 Marketo Engage 发送的电子邮件中包含的跟踪链接规划和实施 CNAME 记录。

作为管理员，您应该与营销团队合作，计划和实施两个CNAME记录。 第一个是针对登陆页面URL的，这样登陆页面就会显示在反映您域的URL中，而不是显示在Adobe Marketo Engage（实际的主机）中。 第二个用于跟踪通过Marketo Engage发送的电子邮件中包含的链接。

### 为登陆页面添加CNAME

将登陆页面CNAME添加到您的DNS记录，以便`[YourLandingPageCNAME]`指向分配给您的登陆页面的唯一帐户字符串。 登录到域注册器的网站，然后输入登陆页面CNAME和帐户字符串。 此条目通常涉及三个字段：

* 别名：输入`[YourLandingPageCNAME]`
* 类型：CNAME
* 指向：输入`[MunchkinID].mktoweb.com`

### 为电子邮件跟踪链接添加 CNAME

添加电子邮件 CNAME，使 `[YourEmailCNAME]` 指向 `[MktoTrackingLink]`，这是 Marketo Engage 分配的默认跟踪链接，其格式为：

`[YourEmailCNAME].[YourDomain].com` IN CNAME `[MktoTrackingLink]`

例如：

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>`[MktoTrackingLink]` 值必须是默认[品牌域](../admin/configure-channels-emails.md#branding-domains)。

### 提供 SSL 证书

联系 [Adobe 支持部门](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support){target="_blank"}，以开始 SSL 证书设置过程。

此过程可能最多需要三个工作日。

## 设置 SPF 和 DKIM

您的营销团队应提供要添加到 DNS 资源记录中的 DKIM (Domain Keys Identified Mail) 信息。 按照以下步骤配置 DKIM 和 SPF（发件人策略框架），然后在更新时通知您的营销团队。

您可以将相同的DKIM配置用于生产Marketo Engage实例和附加的Journey Optimizer B2B edition实例。 在附加的实例中，创建与在Marketo Engage实例中完全相同的域。 选择器和加密值不需要匹配。 将域添加到Journey Optimizer B2B edition实例后，打开Adobe支持票证以请求将您的DKIM配置从Marketo Engage实例共享到新实例。 提供您的Marketo Engage前缀(Munchkin ID)和新的Journey Optimizer B2B edition前缀(Munchkin ID)。

1. 要设置 SPF，请将以下行添加到 DNS 条目中：

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   如果您的 DNS 条目中已经有 SPF 记录，只需向其中添加以下内容：

   ```
   include: mktomail.com
   ```

   将 `CompanyDomain` 替换为您网站的主域（例如 `company.com/`），并将 `CorpIP` 替换为您公司电子邮件服务器的 IP 地址（例如 `255.255.255.255`）。 如果您计划通过 Marketo Engage 从多个域发送电子邮件，请为每个域添加此行（单独一行）。

1. 对于 DKIM，为每个域创建 DNS 资源记录。

   为每个域添加主机记录和 TXT 值：

   `[DKIMDomain1]`：主机记录是 `[HostRecord1]`，TXT 值为 `[TXTValue1]`。

   `[DKIMDomain2]`：主机记录是 `[HostRecord2]`，TXT 值为 `[TXTValue2]`。

   按照 Marketo Engage 文档中的[说明](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}操作后，复制每个 DKIM 域的 `HostRecord` 和 `TXTValue`。 您可以在 Journey Optimizer B2B Edition 中验证这些域（请参阅 [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)）。

## 设置 DMARC

DMARC（基于域的消息认证、报告和一致性）是一种认证协议，用于帮助确保组织的域不在未经授权的情况下被使用。 它扩展了现有的身份验证协议（例如 SPF 和 DKIM），以告知收件人服务器在其域上发生身份验证失败时应采取的行动。 DMARC 是可选的，但强烈建议使用，因为它有助于保护您的品牌和声誉。 Google 和 Yahoo 等主要服务提供商从 2024 年 2 月开始要求批量发件人使用 DMARC。

为了使 DMARC 正常运行，您必须至少拥有以下 DNS TXT 记录之一：

* 有效的 SPF
* 您的FROM：域的有效DKIM记录（建议用于[!DNL Marketo Engage]和[!UICONTROL Journey Optimizer B2B edition]）

您的 `FROM:` 域还必须拥有 DMARC 特定的 DNS TXT 记录。 您也可以选择定义一个电子邮件地址，由此指定 DMARC 报告在您组织内应发送到该地址，以便进行报告监控。

### DMARC 工作流程示例

>[!TIP]
>
>最佳实践是将 DMARC 实施为&#x200B;_缓慢转出_。 随着对潜在影响的深入了解，逐步将您的 DMARC 策略从 `p=none` 提升至 `p=quarantine`，然后再提升至 `p=reject`，并将 DMARC 策略设置为对 SPF 和 DKIM 宽松对齐。

如果您收到 DMARC 报告，应该执行以下操作：

1. 使用 `p=none` 并分析您收到的反馈和报告。 报告会指示接收者对未通过身份验证的消息不采取任何行动，并向发件人发送电子邮件报告。

   * 如果合法消息未通过身份验证，请检查并解决 SPF/DKIM 方面的问题。

   * 确定 SPF 或 DKIM 是否已对齐，并确保所有合法电子邮件均通过身份验证。

   * 审查报告，确保结果符合您根据 SPF/DKIM 策略所预期的结果。

1. 将策略调整为 `p=quarantine`，指示接收电子邮件的服务器隔离那些身份验证失败的邮件（通常会将这些邮件放入垃圾邮件文件夹）。

   审查报告，确保结果符合预期。

1. 如果您对 `p=quarantine` 级别的消息行为感到满意，则可以将策略调整为 (`p=reject`)。

   拒绝策略会指示接收者拒绝（退回）任何未通过身份验证的域的电子邮件。 启用此策略后，只有经过域的 100% 验证的电子邮件才有机会被放入收件箱。

   >[!CAUTION]
   >
   >请谨慎使用此策略，并确定其是否适合您的组织。

### DMARC 报告

DMARC 提供的功能可以接收关于 SPF/DKIM 验证失败电子邮件的报告。 作为身份验证过程的一部分，ISP 服务商会生成两份不同的报告。 发件人可以通过其 DMARC 策略中的 RUA/RUF 标记接收这些报告。

* **汇总报告 (RUA)**：不包含任何可能属于《通用数据保护条例》（GDPR）敏感范畴的个人身份信息（PII）。

* **取证报告 (RUF)**  - 包含属于 GDPR 敏感范畴的电子邮件地址。 在实施此报告之前，请核实您的组织对于需符合 GDPR 规定的信息的处理政策。

这些报告的主要用途是获得那些试图进行欺骗的电子邮件的概述情况。 它们是技术性很强的报告，因此最好通过第三方工具来消化。

### DMARC 记录示例

* 最低限度记录：`v=DMARC1; p=none`

* 这类记录指向用于接收报告的电子邮件地址：`v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### DMARC 标记

DMARC 记录有多个名为 _DMARC 标记_&#x200B;的组件。 每个标记都有一个值，用于指定 DMARC 的某个方面。

| 标记名称 | 使用 | 函数 | 示例 | 默认值 |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | 必需 | 指定版本。 只有一个版本，因此它的固定值为 `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | 必需 | 指定 DMARC 策略，该策略指示接收者应报告、隔离或拒绝未通过身份验证检查的电子邮件。 | `p=none`、`p=quarantine` 或 `p=reject` | - |
| `fo` | 可选 | 允许域所有者指定报告选项。 | `0`：如果 SPF 和 DKIM 均失败，则生成报告  <br> `1` - 如果 SPF 或 DKIM 失败，则生成报告 <br> `d` - 如果 DKIM 失败，则生成报告 <br> `s` - 如果 SPF 失败，则生成报告 | `1`（建议用于 DMARC 报告） |
| `pct` | 可选 | 指定需要筛选的消息的百分比。 | `pct=20` | `100` |
| `rua` | 可选（推荐） | 指定将汇总报告发送到哪里。 | `rua=mailto:aggrep@example.com` | - |
| `ruf` | 可选（推荐） | 指定将取证报告发送到哪里。 | `ruf=mailto:authfail@example.com` | - |
| `sp` | 可选 | 指定某个父域的若干子域的 DMARC 策略。 | `sp=reject` | - |
| `adkim` | 可选 | 指定严格 (`s`) 或宽松 (`r`) 对齐。 宽松对齐意味着该域用于 DKIM 签名，并且可以是 `From:` 地址的子域。 严格对齐意味着在 DKIM 签名中使用的域必须与 `From:` 地址中使用的域完全匹配。 | `adkim=r` | `r` |
| `aspf` | 可选 | 可以是严格的 (`s`)，也可以是宽松的 (`r`)。 宽松模式意味着返回路径域可以是 `From:` 地址的子域。 严格模式意味着返回路径域必须与 `From:` 地址完全匹配。 | `aspf=r` | `r` |

有关 DMARC 及其所有选项的详细信息，请参阅 [https://dmarc.org/](https://dmarc.org/){target="_blank"}。

### 为 Marketo Engage 实施 DMARC

DMARC 有两种对齐方式：

* **DKIM** (Domain Keys Identified Mail) 对齐：电子邮件 `From:` 标头中指定的域与 DKIM 签名匹配。 DKIM 签名包含一个 `d=` 值，其中指定了与 `From:` 标头域进行匹配的域。

  DKIM 对齐会验证发件人是否有权从该域发送邮件，并验证电子邮件传输过程中内容是否未发生更改。 要实施 DKIM 对齐的 DMARC：

   * 为您的邮件的 MAIL FROM 域设置 DKIM。 使用 Marketo Engage 文档中的[说明](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}。

   * 为 DKIM MAIL FROM 域配置 DMARC。

  >[!NOTE]
  >
  >建议为 Marketo Engage 使用 DKIM 对齐。

* **SPF** （发件人策略框架）对齐：`From:` 标头中的域必须与返回路径标头中的域匹配。 如果两个 DNS 域相同，则 SPF 会匹配（对齐）并给出验证通过的结果。 要实施 SPF 对齐的 DMARC：

   * 设置品牌化返回路径域。

      * 配置适当的 SPF 记录。
      * 将 MX 记录更改为指回到发送邮件的数据中心的默认 MX

   * 为品牌化返回路径域配置 DMARC。

  >[!NOTE]
  >
  >不支持或不推荐为 Marketo Engage 使用严格的 SPF 对齐。

### 专用 IP 和共享池

如果您通过 Marketo Engage 使用专用 IP 发送邮件，且未实施（或不确定是否已实施）品牌化返回路径，请向 [Adobe 支持部门](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support){target="_blank"}提交工单。

>[!BEGINSHADEBOX]

**将专用IP迁移到Journey Optimizer B2B Edition**

如果您有专用IP，则必须在与现有Journey Optimizer实例相同的区域创建新的Marketo Engage B2B edition实例。 如果新实例位于不同的区域，则无法共享现有IP。 如果区域匹配，请打开具有[Adobe支持](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support){target="_blank"}的票证，以请求将现有IP和绑定组与新实例共享。 提供您的Marketo Engage前缀(Munchkin ID)和新的Journey Optimizer B2B edition前缀(Munchkin ID)。

通过此请求，Adobe会复制与现有Marketo Engage实例相同的IP、绑定组和配置的返回路径域。 在Marketo Engage实例和Journey Optimizer B2B edition之间共享IP时，两者会同时使用它们（从Marketo Engage发送和Journey Optimizer B2B edition发送使用相同的IP）。

>[!ENDSHADEBOX]

可信 IP 池是为每月发送量低于 75k 且不符合专用 IP 条件的低流量用户预留的共享 IP 池。 这些用户还必须满足最佳实践要求。

* 如果您通过 Marketo Engage 使用 IP 共享池发送邮件，那么您可以通过[申请可信 IP 发送范围计划](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}来检查您是否有资格获得可信 IP。 从 Marketo Engage 可信 IP 发送时包含品牌化返回路径。 如果获准参与此计划，请联系 Adobe 支持部门以设置品牌化返回路径。

* 如果您每月发送的消息量超过 10 万条，并希望通过 Marketo Engage 使用共享 IP 发送电子邮件，请联系 Adobe 帐户团队（即您的帐户经理）以购买专用 IP。

共享IP池中的客户不需要任何其他配置。 您可以继续使用与之前相同的IP池和默认返回路径域。



## 为您的域设置 MX 记录

MX 记录允许您接收发送电子邮件所使用域名的来信，以处理回复和自动回复。 如果您从公司域发出邮件，这可能已经配置好了。 如果没有，您通常可以将其设置为映射到您的公司域 MX 记录。

## 出站 IP 地址

出站连接是 Marketo Engage 代表您与互联网上的服务器建立的连接。 您的 IT 组织和一些合作伙伴/供应商可能会使用允许列表来限制对服务器的访问。 如果是这样，您必须向他们提供 Marketo Engage 出站 IP 地址块，以添加到他们的允许列表中。

<!--
 ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. 
-->

## 出站 IP 地址块

以下列表涵盖了所有发出出站呼叫的 Marketo Engage 服务器。 请参阅这些列表，以配置 IP 允许列表、服务器、防火墙、访问控制列表、安全组或第三方服务，以接收 Marketo Engage 建立的出站连接。

| IP 块（CIDR 表示法） | 个人 IP 地址 |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
