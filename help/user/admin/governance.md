---
title: 治理和隐私功能
description: 了解Journey Optimizer B2B edition中当前可用的治理功能。
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: 2026-03-27T23:18:44.352Z
TQID: https://experienceleague.adobe.com/PwH34suDPc84nB9eiAWtrkVzsOw82RRGw4hrRogf9zE
source-git-commit: 61481d57fb8eca805d9a9bc545124aed568b5416
workflow-type: tm+mt
source-wordcount: 697
ht-degree: 0%

---

# 治理和隐私功能

[!DNL Journey Optimizer B2B Edition]是一个集成的Adobe Experience Platform应用程序。 它采用多种工具和服务，根据您的业务做法、法律义务和开发流程控制您收集的体验数据。 以下各节概述了每种治理功能。

## 隐私

有多种法规适用于为居住在上述地区或国家（欧盟、加利福尼亚、泰国、巴西、新西兰）的持有数据主体数据的[!DNL Journey Optimizer B2B Edition]客户。 本页上的这些信息不是法律建议，也不保证您遵守适用法律。

### GDPR

《通用数据保护条例》(GDPR)是一项欧盟(EU)隐私法律，旨在协调欧盟国家或地区的[数据保护要求](https://commission.europa.eu/law/law-topic/data-protection/data-protection-explained_en){target="_blank"}并使之现代化。

[!DNL Journey Optimizer B2B Edition]使用Privacy Service和Marketo Engage隐私代理服务提供的现有Marketo GDPR治理功能。

### CNIL

2026年4月14日，国家信息和自由委员会[发布了关于在电子邮件中使用跟踪像素的建议](https://cnil.fr/sites/default/files/2026-05/recommandation_tracking_pixels_emails.pdf)。 该指南阐明何时需要获得同意，并强调针对电子邮件像素跟踪的适当同意实践的重要性。 此策略会影响向位于法国的订阅者发送电子邮件的任何实体。

CNIL提供了自建议之日起三个月的时间，要求公司通知电子邮件收件人存在跟踪像素、跟踪像素的目的以及收件人选择退出的权利。 在此过渡期间，Marketo Engage用户应通知其收件人有关像素跟踪的信息，并在必要时提供选择退出选项。 预计CNIL将在2026年7月14日之后开始执行活动。

随着CNIL和其他监管机构澄清有关跟踪像素和相关问题的指导，Adobe将继续监控最新信息，并告知您技术能力正在发生变化。

[!DNL Journey Optimizer B2B Edition]提供可帮助您在电子邮件级别管理打开跟踪的控制。 用户负责根据适用的CNIL指导和其他法律确定自己的合规义务。 有关使用这些功能管理电子邮件打开跟踪的信息，请参阅&#x200B;[_管理电子邮件跟踪_](../content/email-tracking-manage.md)。

## 基于角色的访问控制(RBAC)

通过Journey Optimizer B2B edition并访问Adobe Admin Console，管理员可以授予用户对实体类型（查看区段、管理区段、管理历程等）的权限。 此功能是Unified Permissions Framework (UPF)的一部分，允许所有Adobe Experience Platform客户定义和管理其组织的角色和权限。

## 数据加密

**_静态数据加密_** — 所有从Adobe Experience Platform传输到Journey Optimizer B2B edition的帐户和人员配置文件数据均已加密，以保持Experience Platform的现有合规性。 源自Journey Optimizer B2B edition的所有实体（例如历程和购买群组）也都进行了加密。

**_传输中数据的加密_**（通过公共网络） — 使用TLS 1.2对所有Journey Optimizer B2B edition API和实体进行传输中加密。

## 同意选择启用/选择禁用

Journey Optimizer B2B edition会读取存储在Adobe Experience Platform XDM用户档案中的个人同意首选项，并在发送电子邮件、短信和WhatsApp渠道的消息时强制执行这些首选项。 在从渠道或下游消息提供商发送内容之前，会先从投放中排除选择退出渠道的人员。

在投放时，使用用户档案同意字段组中的XDM字段评估同意。 默认同意行为因渠道而异 — 在没有设置首选项时，电子邮件默认为选择启用，而短信和WhatsApp默认为选择禁用。

有关为每个渠道评估的XDM属性及其默认行为的详细信息，请参阅[同意首选项](../content/channels-consent-preferences.md)。

## 沙盒重置

当前不支持&#x200B;**沙盒重置**&#x200B;用于Adobe Journey Optimizer B2B edition。 重置或删除映射到Journey Optimizer B2B edition的沙盒可能会导致永久数据丢失，并需要配置新实例。

## 尚不可用

以下治理功能尚不可用：

* 数据使用标签实施(DULE) /使用策略
* 数据卫生
* 同意政策
* 字段级访问控制(FLAC)
* 对象级访问控制(OLAC)
* 静态数据的CMK加密
* 平台审计服务
