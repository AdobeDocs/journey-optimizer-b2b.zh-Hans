---
title: 治理功能
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
source-git-commit: 94a8ed9584459cf85a72448cd698740ef450ddb2
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 0%

---

# 治理功能

Journey Optimizer B2B edition是一个集成的Adobe Experience Platform应用程序。 它采用多种工具和服务，根据您的业务做法、法律义务和开发流程控制您收集的体验数据。 以下各节概述了每种治理功能。

## 隐私 — GDPR

Journey Optimizer B2B edition使用Privacy Service和Marketo Engage隐私代理服务提供的现有Marketo GDPR治理功能。

## 基于角色的访问控制(RBAC)

通过Journey Optimizer B2B edition并访问Adobe Admin Console，管理员可以授予用户对实体类型（查看区段、管理区段、管理历程等）的权限。 此功能是Unified Permissions Framework (UPF)的一部分，允许所有Adobe Experience Platform客户定义和管理其组织的角色和权限。

## 数据加密

**_静态数据加密_** — 所有从Adobe Experience Platform传输到Journey Optimizer B2B edition的帐户和人员配置文件数据均已加密，以保持Experience Platform的现有合规性。 源自Journey Optimizer B2B edition的所有实体（例如历程和购买群组）也都进行了加密。

**_传输中数据的加密_**（通过公共网络） — 使用TLS 1.2对所有Journey Optimizer B2B edition API和实体进行传输中加密。

## 同意选择启用/选择禁用

Journey Optimizer B2B edition会读取存储在Adobe Experience Platform XDM用户档案中的个人同意首选项，并在发送电子邮件、短信和WhatsApp渠道的消息时强制执行这些首选项。 在从渠道或下游消息提供商发送内容之前，会从投放中排除选择退出渠道的人员。

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
