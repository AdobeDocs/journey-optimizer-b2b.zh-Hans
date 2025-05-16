---
title: 治理功能
description: 了解Journey Optimizer B2B edition中当前可用的治理功能。
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# 治理功能

Journey Optimizer B2B edition是一个集成的Adobe Experience Platform应用程序。 它采用多种工具和服务，根据您的业务做法、法律义务和开发流程控制您收集的体验数据。 以下各节概述了每种治理功能。

## 隐私 — GDPR

Journey Optimizer B2B edition使用Privacy Service和Marketo Engage Privacy Broker服务提供的现有Marketo GDPR治理功能。

## 基于角色的访问控制(RBAC)

通过Journey Optimizer B2B edition并访问Adobe Admin Console，管理员可以授予用户对实体类型（查看区段、管理区段、管理历程等）的权限。 此功能是Unified Permissions Framework (UPF)的一部分，允许所有Adobe Experience Platform客户定义和管理其组织的角色和权限。

## 数据加密

**_静态数据加密_** — 所有从Adobe Experience Platform传输到Journey Optimizer B2B edition的帐户和人员配置文件数据都经过加密，以保持来自Experience Platform的现有合规性。 源自Journey Optimizer B2B edition的所有实体（例如历程和购买群组）也都进行了加密。

**_传输中数据的加密_**（通过公共网络） — 使用TLS 1.2对所有Journey Optimizer B2B edition API和实体进行传输中加密。

## 同意选择启用/选择禁用

同意选择加入/选择退出是一种治理形式，其中用户档案可以从通信渠道（如电子邮件或短信）中选择退出，然后用户档案会从通信渠道中排除。

借助Journey Optimizer B2B edition，您可以为电子邮件和短信投放用例构建和管理订阅/取消订阅用例。 这些同意首选项存储在XDM配置文件同意字段组中，并作为数据同步框架的一部分同步到Journey Optimizer B2B edition中或从中导出。 这些首选项在投放时用于从投放中排除已选择退出的用户档案。

## 沙盒重置

当前不支持&#x200B;**沙盒重置**&#x200B;用于Adobe Journey Optimizer B2B edition。 重置或删除映射到Journey Optimizer B2B edition的沙盒可能会导致Journey Optimizer B2B edition中的数据永久丢失，并且可能需要配置新的Journey Optimizer B2B edition实例。

## 尚不可用

以下治理功能尚不可用：

* 数据使用标签实施(DULE) /使用策略
* 数据卫生
* 同意政策
* 字段级访问控制(FLAC)
* 对象级访问控制(OLAC)
* 静态数据的CMK加密
* 平台审计服务
