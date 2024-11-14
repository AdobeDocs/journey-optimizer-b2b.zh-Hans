---
title: 跟踪和电子邮件投放协议
description: 了解如何在Marketo Engage中配置协议以供Journey Optimizer B2B edition用于跟踪和电子邮件渠道功能。
feature: Setup
role: Admin
source-git-commit: a8ca8b99ddf33b4a64b42b751f7be798274d0084
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 0%

---

# 跟踪和电子邮件投放协议

Adobe Journey Optimizer B2B edition利用Marketo Engage中的电子邮件渠道功能和事件跟踪。 列入允许列表对于使用限制性防火墙或代理服务器设置的组织，为确保电子邮件传递按预期工作，系统管理员必须将某些域和IP地址范围添加到。

>[!NOTE]
>
>如果贵组织已使用连接的Marketo Engage实例运行其营销操作，则这些协议和配置应已准备就绪。

确保将以下域（包括星号）添加到允许列表以启用所有Marketo Engage资源和Web套接字：

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

请完成以下步骤以确保跟踪和电子邮件投放：

1. [创建DNS记录 ](#create-dns-records-for-landing-pages-and-email)
1. [设置SPF和DKIM](#set-up-spf-and-dkim)
1. [设置DMARC](#set-up-dmarc)
1. [为您的域设置MX记录](#set-up-mx-records-for-your-domain)
1. [列入允许列表将出站IP地址添加到](#outbound-ip-addresses)

## 为<!-- landing pages and -->电子邮件创建DNS记录

连接CNAME记录可让营销人员托管具有一致品牌推广的电子邮件、登陆页面和博客的Web版本，从而提高流量和转化率。 强烈建议您将CNAME添加到根域主机，以便Marketo Engage托管以营销为中心的Web资产。 作为管理员，您应该与营销团队合作，为通过Marketo Engage发送的电子邮件中包含的跟踪链接计划和实施CNAME记录。
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### 为电子邮件跟踪链接添加CNAME

添加电子邮件CNAME，以便`[YourEmailCNAME]`指向`[MktoTrackingLink]`(Marketo Engage分配的默认跟踪链接)，格式为：

CNAME `[MktoTrackingLink]`中的`[YourEmailCNAME].[YourDomain].com`

例如：

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>`[MktoTrackingLink]`值必须是默认品牌策略域。

### 配置SSL证书

联系[Adobe支持](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"}以开始预配SSL证书的流程。

完成此过程最多可能需要三个工作日。

## 设置SPF和DKIM

您的营销团队应提供要添加到DNS资源记录的DKIM（域密钥识别邮件）信息。 按照以下步骤配置DKIM和SPF（发件人策略框架），然后在更新时通知您的营销团队。

1. 要设置SPF，请将以下行添加到DNS条目中：

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   如果在DNS条目中已有SPF记录，只需将以下内容添加到该记录中即可：

   ```
   include: mktomail.com
   ```

   将`CompanyDomain`替换为网站的主域（如`company.com/`），将`CorpIP`替换为公司电子邮件服务器的IP地址（如`255.255.255.255`）。 如果您计划通过Marketo Engage从多个域发送电子邮件，请为每个域添加此行（在一行中）。

1. 对于DKIM，请为每个域创建DNS资源记录。

   为每个域添加主机记录和TXT值：

   `[DKIMDomain1]`：主机记录为`[HostRecord1]`，TXT值为`[TXTValue1]`。

   `[DKIMDomain2]`：主机记录为`[HostRecord2]`，TXT值为`[TXTValue2]`。

   按照Marketo Engage文档中的[说明](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}复制每个DKIM域的`HostRecord`和`TXTValue`。 您可以在Journey Optimizer B2B edition中验证域（请参阅[SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)）。

## 设置DMARC

DMARC（基于域的消息身份验证、报告和符合性）是一种身份验证协议，用于帮助组织保护其域免遭未经授权的使用。 它扩展了现有的身份验证协议，如SPF和DKIM，以通知接收方服务器在其域上发生身份验证失败时应采取的操作。 DMARC是可选的，但强烈建议使用，因为这样有助于保护您的品牌和声誉。 从2024年2月开始，Google和雅虎等主要提供商开始要求批量发件人使用DMARC。

要使DMARC正常运行，您必须至少具有以下DNS TXT记录之一：

* 有效的SPF
* 您的FROM：域的有效DKIM记录(建议用于Marketo Engage和Journey Optimizer B2B edition)

您还必须拥有`FROM:`域的特定于DMARC的DNS TXT记录。 或者，您可以定义一个电子邮件地址，用于指定DMARC报告在组织内用于报告监视的位置。

### DMARC工作流示例

>[!TIP]
>
>最佳实践是将DMARC实施为&#x200B;_缓慢转出_。 将DMARC策略从`p=none`提升到`p=quarantine`，然后再提升到`p=reject`，因为您可以了解潜在的影响，并将DMARC策略设置为放松对SPF和DKIM的协调。

如果您收到DMARC报表，则应当执行以下操作：

1. 使用`p=none`分析您收到的反馈和报告。 报告告知接收者不对验证失败的邮件执行任何操作，并向发件人发送电子邮件报告。

   * 如果合法消息未通过身份验证，请检查并修复SPF/DKIM的问题。

   * 确定SPF或DKIM是否一致，并通过所有合法电子邮件的身份验证。

   * 查看报告，确保结果符合您的SPF/DKIM政策的预期。

1. 将策略调整为`p=quarantine`，以告知接收电子邮件服务器隔离身份验证失败的电子邮件（通常将这些邮件放入垃圾邮件文件夹）。

   审查报告以确保结果符合预期。

1. 如果您对`p=quarantine`级别上的消息行为感到满意，则可以调整策略以使用(`p=reject`)。

   拒绝策略会告知接收者拒绝（退回）未通过身份验证的域的任何电子邮件。 启用此策略后，只有经域验证为100%经过身份验证的电子邮件才有机会放置收件箱。

   >[!CAUTION]
   >
   >请谨慎使用此策略，并确定它是否适合您的组织。

### DMARC报表

DMARC提供接收有关SPF/DKIM失败的电子邮件的报表的功能。 在身份验证过程中，ISP服务生成了两个不同的报告。 发件人可通过其DMARC策略中的RUA/RUF标记接收这些报告。

* **汇总报表(RUA)**：不包含任何可能对GDPR（通用数据保护条例）敏感的PII（个人身份信息）。

* **取证报告(RUF)** — 包含对GDPR敏感的电子邮件地址。 在实施此报表之前，请验证您的组织政策，以处理需要符合GDPR的信息。

这些报告的主要用途是接收尝试欺骗的电子邮件概述。 这些是技术含量很高的报告，最好通过第三方工具消化。

### DMARC记录示例

* 最小裸记录： `v=DMARC1; p=none`

* 指向接收报告的电子邮件地址的记录： `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### DMARC标记

DMARC记录具有多个名为&#x200B;_DMARC标记_&#x200B;的组件。 每个标记都有一个值，该值指定DMARC的某些方面。

| 标记名称 | 使用 | 函数 | 示例 | 默认值 |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | 必需 | 指定版本。 只有一个版本，因此其固定值为`v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | 必需 | 指定DMARC策略，该策略指示收件人报告、隔离或拒绝未通过身份验证检查的电子邮件。 | `p=none`、`p=quarantine`或`p=reject` | - |
| `fo` | 可选 | 允许域所有者指定报告选项。 | `0`：如果SPF和DKIM都失败，则生成报告<br> `1` — 如果SPF或DKIM失败，则生成报告<br> `d` — 如果DKIM失败，则生成报告<br> `s` — 如果SPF失败，则生成报告 | `1` (建议用于DMARC报表) |
| `pct` | 可选 | 指定受过滤的邮件的百分比。 | `pct=20` | `100` |
| `rua` | 可选（推荐） | 指定汇总报表的交付位置。 | `rua=mailto:aggrep@example.com` | - |
| `ruf` | 可选（推荐） | 指定传送鉴证报告的位置。 | `ruf=mailto:authfail@example.com` | - |
| `sp` | 可选 | 为父域的子域指定DMARC策略。 | `sp=reject` | - |
| `adkim` | 可选 | 指定严格(`s`)或宽松(`r`)对齐。 松弛对齐意味着该域用在DKIM签名中，可以是`From:`地址的子域。 严格对齐意味着该域用在DKIM签名中，并且必须与`From:`地址中使用的域完全匹配。 | `adkim=r` | `r` |
| `aspf` | 可选 | 可以是严格(`s`)或宽松(`r`)。 松弛模式意味着Return-Path域可以是`From:`地址的子域。 Strict模式意味着Return-Path域必须与`From:`地址完全匹配。 | `aspf=r` | `r` |

有关DMARC及其所有选项的详细信息，请参阅[https://dmarc.org/](https://dmarc.org/){target="_blank"}。

### 适用于Marketo Engage的DMARC实施

DMARC有两种类型的对齐方式：

* **DKIM** （域名识别邮件）对齐：电子邮件的`From:`标头中指定的域与DKIM-Signature匹配。 DKIM签名包含`d=`值，其中指定域与`From:`标头域匹配。

  DKIM对齐验证发件人是否被授权从域发送邮件，并验证在电子邮件传输期间是否未更改任何内容。 要实施与DKIM关联的DMARC，请执行以下操作：

   * 为消息的MAIL FROM域设置DKIM。 在Marketo Engage文档中使用[说明](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}。

   * 为DKIM MAIL FROM域配置DMARC。

  >[!NOTE]
  >
  >建议使用DKIM对齐进行Marketo Engage。

* **SPF** （发件人策略框架）对齐： `From:`标头中的域必须与Return-Path：标头中的域匹配。 如果两个DNS域相同，则SPF匹配（对齐）并给出传递结果。 要实施与SPF对齐的DMARC，请执行以下操作：

   * 设置标记的Return-Path域。

      * 配置相应的SPF记录。
      * 更改MX记录以指向发送邮件的数据中心的默认MX

   * 为标记的Return-Path域配置DMARC。

  >[!NOTE]
  >
  >Marketo Engage不支持或建议使用严格的SPF对齐方式。

### 专用IP和共享池

如果您通过专用IP通过Marketo Engage发送邮件，并且尚未实现标记返回路径（或者不确定您是否具有），请打开具有[Adobe支持](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"}的票证。

受信任的IP是IP的共享池，为每月发送少于75,000次并且不符合专用IP条件的低容量用户保留。 这些用户还必须满足最佳实践要求。

* 如果您使用共享IP池通过Marketo Engage发送邮件，则可以通过[申请受信任IP发送范围程序](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}来检查您是否符合受信任IP的条件。 从Marketo Engage受信任的IP发送时，将包含标记的return-path。 如果批准此计划，请联系Adobe支持部门以设置标记的return-path。

* 如果您每月发送的邮件超过100,000条，并且希望使用共享IP通过Marketo Engage发送电子邮件，请联系Adobe客户团队（您的客户经理）以购买专用IP。

## 为您的域设置MX记录

利用MX记录，可接收发往所发电子邮件之域的邮件，以处理回复和自动回复者。 如果您从公司域发送，则它可能已配置。 如果没有，则通常可以将其设置为映射到公司域MX记录。

## 出站IP地址

出站连接是指Marketo Engage代表您与Internet上的服务器建立的连接。 您的IT部门和某些合作伙伴/供应商可能会使用允许列表来限制对服务器的访问。 如果是，则必须向他们提供Marketo Engage列入允许列表出站IP地址块，以将其添加到其。

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## 出站IP地址块

下表列出了进行出站调用的所有Marketo Engage服务器。 请参阅这些列表以配置IP允许列表、服务器、防火墙、访问控制列表、安全组或第三方服务来接收来自Marketo Engage的传出连接。

| IP块（CIDR表示法） | 单个IP地址 |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
