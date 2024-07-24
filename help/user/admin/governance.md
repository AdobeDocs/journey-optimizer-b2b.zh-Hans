---
title: 治理功能
description: 了解Journey Optimizer B2B版本中当前可用的治理功能。
source-git-commit: 1353defe804947617a4d7489592d380bf372c7df
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# 治理功能

作为集成的Adobe Experience Platform应用程序，Journey Optimizer B2B Edition采用多种服务和工具，使您能够放心地控制收集的体验数据，以符合您的业务实践、法律义务和开发流程。 以下各节概述了每种治理功能。

## 隐私 — GDPR

Journey Optimizer B2B版本使用Privacy Service和Marketo隐私代理服务提供的现有Marketo EngageGDPR治理功能。

## 基于角色的访问控制(RBAC)

通过使用Journey Optimizer B2B版本和对Adobe Admin Console的访问权限，管理员可以授予用户对实体类型（查看区段、管理区段、管理历程等）的权限。 此功能是Unified Permissions Framework (UPF)的一部分，允许所有Adobe Experience Platform客户定义和管理其组织的角色和权限。

## 数据加密

**_静态数据加密_** — 从Adobe Experience Platform传输到Journey Optimizer B2B版本的所有帐户和人员配置文件数据都将进行加密，以保持Experience Platform中的现有合规性。 源自Journey Optimizer B2B版本的所有实体（例如历程和购买群组）也都进行了加密。

**_传输中数据的加密_**（通过公共网络） — 使用TLS 1.2对所有Journey Optimizer B2B Edition API和实体进行传输中加密。

## 同意选择启用/选择禁用

同意选择加入/选择退出是一种治理形式，其中用户档案可以从通信渠道（如电子邮件或短信）中选择退出，然后用户档案应该从此类通信渠道中排除。

通过Journey Optimizer B2B Edition，您可以构建和管理电子邮件和短信投放用例的订阅/取消订阅用例。 这些同意首选项存储在XDM配置文件同意字段组中，并作为Data Sync Framework的一部分同步到Journey Optimizer B2B版本中或从中同步。 这些首选项在投放时用于从投放中排除已选择退出的用户档案。

## 尚不可用

以下治理功能尚不可用，但包含在产品路线图中：

* 数据使用标签实施(DULE) /使用策略
* 数据卫生
* 沙盒重置
* 同意政策
* 字段级访问控制(FLAC)
* 对象级访问控制(OLAC)
* 静态数据的CMK加密
* 平台审计服务