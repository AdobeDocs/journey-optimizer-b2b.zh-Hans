---
title: 同意渠道消息传递
description: 了解Journey Optimizer B2B edition如何读取AEP XDM配置文件同意首选项，以及如何在电子邮件、短信和WhatsApp渠道的消息投放时强制选择启用和选择禁用。
feature: Setup, Channels
role: Admin, User
autotag-review: '2026-05-19T16:18:37.228Z'
TQID: 'https://experienceleague.adobe.com/-c0dJnpfiIcj0B5gViyEQ7E1Ws0BwP864OLF003rOjw'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6id: a22f05f6-0fcf-40c0-a70e-e13a3db185f7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 2c6aafd07cf033df8801621f7e5275dbeeb2768e
workflow-type: tm+mt
source-wordcount: 415
ht-degree: 1%

---

# 同意渠道消息传递

Adobe Journey Optimizer B2B edition读取存储在Adobe Experience Platform XDM配置文件中的个人同意偏好设置，并在消息投放时强制执行这些偏好设置，作为应用程序的[治理控制](../admin/governance.md)的一部分。 在从渠道或下游消息提供商发送内容之前，会从投放中排除选择退出渠道的人员。

以下部分介绍Journey Optimizer B2B edition如何在消息发送时评估每个受支持渠道的同意情况。

## 电子邮件 {#email}

在[电子邮件渠道](../admin/configure-channels-emails.md)上发送消息时，Journey Optimizer B2B edition会评估以下XDM属性以获得电子邮件同意：

| XDM属性 | `y` | `n` | 无值 |
| --- | --- | --- | --- |
| `consents.marketing.email.val` | 已选择加入 | 已选择退出 | 已选择加入 |

为征得电子邮件同意，请考虑以下事项：

* 全局选择退出电子邮件的用户可以接收标记为可操作的电子邮件。
* 不支持订阅级别的首选项。

若要查看已发送电子邮件的取消订阅活动，请参阅[电子邮件性能报表](../dashboards/email-performance-dashboard.md)。

## 短信 {#sms}

通过[SMS渠道](../admin/configure-channels-sms.md)发送消息时，Journey Optimizer B2B edition会评估以下XDM属性以获得SMS同意：

| XDM属性 | `y` | `n` | 无值 |
| --- | --- | --- | --- |
| `consents.marketing.sms.val` | 已选择加入 | 已选择退出 | 已选择退出 |
| `consents.marketing.subscriptions.<senderID>` | 已选择加入 | 已选择退出 | 已选择退出 |
| `consents.marketing.sms.subscriptions.<senderId>.subscribers.<phoneNumber>` | 已选择加入 | 已选择退出 | 已选择退出 |

同意短信时请考虑以下事项：

* 当潜在客户（人员）记录退出短信时，该记录将被完全排除，并且不会传递给下游短信提供商。
* 如果可用，将评估订阅级别的同意。 当订阅级别的同意不可用时，全局选择退出将用作回退。
* 选择退出短信的用户仍可接收标记为可操作的消息。
* 如果多个潜在客户记录共享相同的电话号码，则他们共享相同的选择加入或选择退出状态。

## WhatsApp {#whatsapp}

通过配置的[WhatsApp渠道](../admin/configure-channels-whatsapp.md)发送消息时，Journey Optimizer B2B edition会根据WhatsApp同意评估以下XDM属性：

| XDM属性 | `y` | `n` | 无值 |
| --- | --- | --- | --- |
| `consents.marketing.whatsApp.val` | 已选择加入 | 已选择退出 | 已选择退出 |
| `consents.idSpecific.Phone.<number>.marketing.whatsApp.val` | 已选择加入 | 已选择退出 | 已选择退出 |

为了WhatsApp同意，请考虑以下事项：

* 如果全局WhatsApp属性值(`consents.marketing.whatsApp.val`)存在，则将其用于同意评估。
* 如果全局属性值不存在，但存在特定于发件人的条目，则将使用特定于发件人的条目进行同意评估。
* 如果任一属性均不存在值，则将人员视为选择退出。

## 不受支持 {#not-supported}

Journey Optimizer B2B edition当前不支持以下与同意相关的功能：

* AEP同意政策
* 营销首选属性(`consents.marketing.preferred`)
