---
title: 跟踪和电子邮件传递协议
description: 了解如何在 Marketo Engage 中配置协议，以便 Journey Optimizer B2B Edition 使用跟踪和电子邮件渠道功能。
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: 4bbe641305065888a59b3e77357e9b39fa6d402e
workflow-type: ht
source-wordcount: '1798'
ht-degree: 100%

---

# 跟踪和电子邮件传递协议

Adobe Journey Optimizer B2B Edition 使用 Marketo Engage 中的电子邮件渠道功能和事件跟踪功能。为了确保使用限制性防火墙或代理服务器设置的组织的电子邮件传递能够按预期进行，系统管理员必须将某些域和 IP 地址范围添加到允许列表中。

>[!NOTE]
>
>如果您的组织已经在使用连接的 Marketo Engage 实例来进行其营销运营，这说明已经完成了这些协议和配置。

确保将以下域（包括星号）添加到允许列表中，以启用所有 Marketo Engage 资源和 WebSockets：

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

按照以下步骤操作，以确保追踪和电子邮件传递正常：

1. [为以下内容创建 DNS 记录 ](#create-dns-records-for-landing-pages-and-email)
1. [设置 SPF 和 DKIM](#set-up-spf-and-dkim)
1. [设置 DMARC](#set-up-dmarc)
1. [为您的域设置 MX 记录](#set-up-mx-records-for-your-domain)
1. [将出站 IP 地址添加到允许列表](#outbound-ip-addresses)

## 为<!-- landing pages and -->电子邮件创建 DNS 记录

连接 CNAME 记录可以让营销人员托管电子邮件、登陆页面和博客的网页版本，保持一致的品牌形象，从而提升流量和转化率。强烈建议您将 CNAME 添加到您的根域主机，以便 Marketo Engage 托管您的以营销为中心的网络资产。作为管理员，您应该与您的营销团队合作，为通过 Marketo Engage 发送的电子邮件中包含的跟踪链接规划和实施 CNAME 记录。
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

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

您的营销团队应提供要添加到 DNS 资源记录中的 DKIM (Domain Keys Identified Mail) 信息。按照以下步骤配置 DKIM 和 SPF（发件人策略框架），然后在更新时通知您的营销团队。

1. 要设置 SPF，请将以下行添加到 DNS 条目中：

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   如果您的 DNS 条目中已经有 SPF 记录，只需向其中添加以下内容：

   ```
   include: mktomail.com
   ```

   将 `CompanyDomain` 替换为您网站的主域（例如 `company.com/`），并将 `CorpIP` 替换为您公司电子邮件服务器的 IP 地址（例如 `255.255.255.255`）。如果您计划通过 Marketo Engage 从多个域发送电子邮件，请为每个域添加此行（单独一行）。

1. 对于 DKIM，为每个域创建 DNS 资源记录。

   为每个域添加主机记录和 TXT 值：

   `[DKIMDomain1]`：主机记录是 `[HostRecord1]`，TXT 值为 `[TXTValue1]`。

   `[DKIMDomain2]`：主机记录是 `[HostRecord2]`，TXT 值为 `[TXTValue2]`。

   按照 Marketo Engage 文档中的[说明](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}操作后，复制每个 DKIM 域的 `HostRecord` 和 `TXTValue`。您可以在 Journey Optimizer B2B Edition 中验证这些域（请参阅 [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)）。

## 设置 DMARC

DMARC（基于域的消息认证、报告和一致性）是一种认证协议，用于帮助确保组织的域不在未经授权的情况下被使用。它扩展了现有的身份验证协议（例如 SPF 和 DKIM），以告知收件人服务器在其域上发生身份验证失败时应采取的行动。DMARC 是可选的，但强烈建议使用，因为它有助于保护您的品牌和声誉。Google 和 Yahoo 等主要服务提供商从 2024 年 2 月开始要求批量发件人使用 DMARC。

为了使 DMARC 正常运行，您必须至少拥有以下 DNS TXT 记录之一：

* 有效的 SPF
* 您的 FROM: 域的有效 DKIM 记录（推荐用于 Marketo Engage 和 Journey Optimizer B2B Edition）

您的 `FROM:` 域还必须拥有 DMARC 特定的 DNS TXT 记录。您也可以选择定义一个电子邮件地址，由此指定 DMARC 报告在您组织内应发送到该地址，以便进行报告监控。

### DMARC 工作流程示例

>[!TIP]
>
>最佳实践是将 DMARC 实施为&#x200B;_缓慢转出_。随着对潜在影响的深入了解，逐步将您的 DMARC 策略从 `p=none` 提升至 `p=quarantine`，然后再提升至 `p=reject`，并将 DMARC 策略设置为对 SPF 和 DKIM 宽松对齐。

如果您收到 DMARC 报告，应该执行以下操作：

1. 使用 `p=none` 并分析您收到的反馈和报告。报告会指示接收者对未通过身份验证的消息不采取任何行动，并向发件人发送电子邮件报告。

   * 如果合法消息未通过身份验证，请检查并解决 SPF/DKIM 方面的问题。

   * 确定 SPF 或 DKIM 是否已对齐，并确保所有合法电子邮件均通过身份验证。

   * 审查报告，确保结果符合您根据 SPF/DKIM 策略所预期的结果。

1. 将策略调整为 `p=quarantine`，指示接收电子邮件的服务器隔离那些身份验证失败的邮件（通常会将这些邮件放入垃圾邮件文件夹）。

   审查报告，确保结果符合预期。

1. 如果您对 `p=quarantine` 级别的消息行为感到满意，则可以将策略调整为 (`p=reject`)。

   拒绝策略会指示接收者拒绝（退回）任何未通过身份验证的域的电子邮件。启用此策略后，只有经过域的 100% 验证的电子邮件才有机会被放入收件箱。

   >[!CAUTION]
   >
   >请谨慎使用此策略，并确定其是否适合您的组织。

### DMARC 报告

DMARC 提供的功能可以接收关于 SPF/DKIM 验证失败电子邮件的报告。作为身份验证过程的一部分，ISP 服务商会生成两份不同的报告。发件人可以通过其 DMARC 策略中的 RUA/RUF 标记接收这些报告。

* **汇总报告 (RUA)**：不包含任何可能属于《通用数据保护条例》（GDPR）敏感范畴的个人身份信息（PII）。

* **取证报告 (RUF)**  - 包含属于 GDPR 敏感范畴的电子邮件地址。在实施此报告之前，请核实您的组织对于需符合 GDPR 规定的信息的处理政策。

这些报告的主要用途是获得那些试图欺骗的电子邮件的概述情况。它们是技术性很强的报告，因此最好通过第三方工具来消化。

### DMARC 记录示例

* 最低限度记录：`v=DMARC1; p=none`

* 这类记录指向用于接收报告的电子邮件地址：`v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### DMARC 标记

DMARC 记录有多个名为 _DMARC 标记_&#x200B;的组件。每个标记都有一个值，用于指定 DMARC 的某个方面。

| 标记名称 | 使用 | 函数 | 示例 | 默认值 |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | 必需 | 指定版本。只有一个版本，因此它的固定值为 `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | 必需 | 指定 DMARC 策略，该策略指示接收者应报告、隔离或拒绝未通过身份验证检查的电子邮件。 | `p=none`、`p=quarantine` 或 `p=reject` | - |
| `fo` | 可选 | 允许域所有者指定报告选项。 | `0`：如果 SPF 和 DKIM 均失败，则生成报告  <br> `1` - 如果 SPF 或 DKIM 失败，则生成报告 <br> `d` - 如果 DKIM 失败，则生成报告 <br> `s` - 如果 SPF 失败，则生成报告 | `1`（建议用于 DMARC 报告） |
| `pct` | 可选 | 指定需要筛选的消息的百分比。 | `pct=20` | `100` |
| `rua` | 可选（推荐） | 指定将汇总报告发送到哪里。 | `rua=mailto:aggrep@example.com` | - |
| `ruf` | 可选（推荐） | 指定将取证报告发送到哪里。 | `ruf=mailto:authfail@example.com` | - |
| `sp` | 可选 | 指定某个父域的若干子域的 DMARC 策略。 | `sp=reject` | - |
| `adkim` | 可选 | 指定严格 (`s`) 或宽松 (`r`) 对齐。宽松对齐意味着该域用于 DKIM 签名，并且可以是 `From:` 地址的子域。严格对齐意味着在 DKIM 签名中使用的域必须与 `From:` 地址中使用的域完全匹配。 | `adkim=r` | `r` |
| `aspf` | 可选 | 可以是严格的 (`s`)，也可以是宽松的 (`r`)。宽松模式意味着返回路径域可以是 `From:` 地址的子域。严格模式意味着返回路径域必须与 `From:` 地址完全匹配。 | `aspf=r` | `r` |

有关 DMARC 及其所有选项的详细信息，请参阅 [https://dmarc.org/](https://dmarc.org/){target="_blank"}。

### 为 Marketo Engage 实施 DMARC

DMARC 有两种对齐方式：

* **DKIM** (Domain Keys Identified Mail) 对齐：电子邮件 `From:` 标头中指定的域与 DKIM 签名匹配。DKIM 签名包含一个 `d=` 值，其中指定了与 `From:` 标头域进行匹配的域。

  DKIM 对齐会验证发件人是否有权从该域发送邮件，并验证电子邮件传输过程中内容是否未发生更改。要实施 DKIM 对齐的 DMARC：

   * 为您的邮件的 MAIL FROM 域设置 DKIM。使用 Marketo Engage 文档中的[说明](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}。

   * 为 DKIM MAIL FROM 域配置 DMARC。

  >[!NOTE]
  >
  >建议为 Marketo Engage 使用 DKIM 对齐。

* **SPF** （发件人策略框架）对齐：`From:` 标头中的域必须与返回路径标头中的域匹配。如果两个 DNS 域相同，则 SPF 会匹配（对齐）并给出验证通过的结果。要实施 SPF 对齐的 DMARC：

   * 设置品牌化返回路径域。

      * 配置适当的 SPF 记录。
      * 将 MX 记录更改为指回到发送邮件的数据中心的默认 MX

   * 为品牌化返回路径域配置 DMARC。

  >[!NOTE]
  >
  >不支持或不推荐为 Marketo Engage 使用严格的 SPF 对齐。

### 专用 IP 和共享池

如果您通过 Marketo Engage 使用专用 IP 发送邮件，且未实施（或不确定是否已实施）品牌化返回路径，请向 [Adobe 支持部门](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support){target="_blank"}提交工单。

可信 IP 池是为每月发送量低于 75k 且不符合专用 IP 条件的低流量用户预留的共享 IP 池。这些用户还必须满足最佳实践要求。

* 如果您通过 Marketo Engage 使用 IP 共享池发送邮件，那么您可以通过[申请可信 IP 发送范围计划](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}来检查您是否有资格获得可信 IP。从 Marketo Engage 可信 IP 发送时包含品牌化返回路径。如果获准参与此计划，请联系 Adobe 支持部门以设置品牌化返回路径。

* 如果您每月发送的消息量超过 10 万条，并希望通过 Marketo Engage 使用共享 IP 发送电子邮件，请联系 Adobe 帐户团队（即您的帐户经理）以购买专用 IP。

## 为您的域设置 MX 记录

MX 记录允许您接收那些发送到您用于发出邮件的域的邮件，以处理回复和自动回复。如果您从公司域发出邮件，这可能已经配置好了。如果没有，您通常可以将其设置为映射到您的公司域 MX 记录。

## 出站 IP 地址

出站连接是 Marketo Engage 代表您与互联网上的服务器建立的连接。您的 IT 组织和一些合作伙伴/供应商可能会使用允许列表来限制对服务器的访问。如果是这样，您必须向他们提供 Marketo Engage 出站 IP 地址块，以添加到他们的允许列表中。

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## 出站 IP 地址块

以下列表涵盖了所有发出出站呼叫的 Marketo Engage 服务器。请参阅这些列表，以配置 IP 允许列表、服务器、防火墙、访问控制列表、安全组或第三方服务，以接收 Marketo Engage 建立的出站连接。

| IP 块（CIDR 表示法） | 个人 IP 地址 |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
