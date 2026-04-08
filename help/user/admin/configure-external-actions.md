---
title: 外部操作配置
description: 了解开发人员、管理员和营销人员如何协作来实施、配置和使用外部操作，以便将Journey Optimizer B2B edition与帐户历程中的外部服务相关联。
feature: Setup, Integrations
role: Admin, Developer
source-git-commit: 6d3967babc1bc868fde0c76ac9068e63156070cd
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# 外部操作配置

外部操作允许Journey Optimizer B2B edition中的帐户旅程直接从旅程画布与外部系统连接。 当帐户受众访问外部操作节点时，系统会向配置的外部服务进行异步出站调用，传递帐户、人员或两者的受众属性数据。 外部服务处理数据并使用回调进行响应，返回可用于指导历程执行的受众数据和元数据。

此功能支持两种历程节点类型：

* **外部操作** — 调用外部服务并沿单个传出路径继续。 适用于&#x200B;_触发并忘记_&#x200B;集成，例如更新CRM记录或触发下游通知。
* **外部拆分路径** — 调用外部服务并评估响应以沿几个定义的路径之一路由帐户。

>[!NOTE]
>
>仅帐户历程支持外部操作服务。 这些节点类型不适用于人员历程。

## 实施概述

设置外部操作需要依次在三个角色之间进行协调：

| | 角色 | 任务 |
| ---- | ---- | ---- |
| 1 | Developer | [实施并发布外部服务](#implement-service) |
| 2 | 管理员 | [在Journey Optimizer B2B edition中配置操作](#configure-action) |
| 3 | 营销人员 | [向帐户历程添加外部节点](#add-journey-node) |

## 实施外部服务 {#implement-service}

开发人员必须创建并发布符合[Adobe Journey Optimizer B2B edition外部操作服务提供程序接口](https://developer.adobe.com/journey-optimizer-b2b-apis/)的面向公众的Web服务。

>[!NOTE]
>
>回调函数需要持有者令牌。 通过在Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)中为您的IMS组织设置[OAuth服务器到服务器凭据来检索此项。

服务启动后，将指向OpenAPI规范的URL和身份验证凭据提供给负责配置该操作的产品管理员。

## 配置操作 {#configure-action}

必须先配置和激活操作，营销人员才能在历程中使用它。 操作以&#x200B;_草稿_&#x200B;状态创建，并且您的更改会自动保存。 在激活它之前，它将保持为草稿。

>[!PREREQUISITES]
>
>在添加配置之前，请从开发人员处获取指向OpenAPI规范的URL和身份验证凭据。
>
>要定义和激活外部操作，您必须具有&#x200B;_[!UICONTROL 管理B2B管理员配置]_ [产品权限](./user-management.md#b2b-product-permissions)。

1. 转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 配置]**。

1. 单击中间面板上的&#x200B;**[!UICONTROL 外部操作]**。

   ![访问外部操作配置空间](./assets/configuration-external-actions-list.png){width="800" zoomable="yes"}

1. 单击右上方的&#x200B;**[!UICONTROL 创建操作]**。

1. 输入外部服务的OpenAPI规范的URL，然后单击&#x200B;**[!UICONTROL 创建]**。

   ![输入服务URL](./assets/configuration-external-actions-create-url.png){width="500"}

   >[!NOTE]
   >
   >您的外部服务必须处于实时状态并且可访问，才能成功完成此步骤。

1. 成功解析URL后，查看&#x200B;**[!UICONTROL 服务详细信息]**。

   创建操作后，将直接从OpenAPI规范中读取服务详细信息。 创建后，无法在配置中更改这些属性。

   | 属性 | 描述 | OpenAPI规范属性 |
   | -------- | ----------- | --------------------- |
   | [!UICONTROL 名称] | 操作的名称 | `info.title` |
   | [!UICONTROL 描述] | 操作的描述 | `info.description` |
   | [!UICONTROL URL] | 定义外部服务的OpenAPI规范的URL | `servers.url` |

1. 输入外部服务(`components.securitySchemes`)的&#x200B;**[!UICONTROL 身份验证]**&#x200B;凭据。

   >[!NOTE]
   >
   >显示的凭据字段取决于外部服务中定义的身份验证机制。 支持的类型包括API密钥、OAuth2和HTTP基本身份验证。

   ![添加身份验证凭据](./assets/configuration-external-actions-auth-credentials.png){width="600" zoomable="yes"}

   当配置的操作处于&#x200B;_草稿_&#x200B;或&#x200B;_活动_&#x200B;状态时，您可以根据需要更改凭据。

1. 单击&#x200B;**[!UICONTROL 下一步]**。

1. 设置&#x200B;**[!UICONTROL 配置]**&#x200B;属性以定义操作与外部服务交换数据的方式。

   >[!NOTE]
   >
   >标记为&#x200B;_静态_&#x200B;的属性在配置时不可更新，且基于服务定义。

   * **[!UICONTROL 操作类型]** （_静态_） — 支持的历程节点类型：

      * [!UICONTROL 外部操作] (`enableSplitPath` = false)
      * [!UICONTROL 外部操作拆分路径] (`enableSplitPath` = true)

     创建操作配置后，无法更改操作类型。

   * **[!UICONTROL 访问器]** （_静态_） — （仅限外部操作拆分路径）外部服务返回的变量可用作外部拆分路径节点中的路径条件。 (`invocationPayloadDef.accessorsMetadata`)

   * **[!UICONTROL 历程上下文]** （_静态_） — 在请求中发送的受众数据的范围(`supportedEntityType`)：

      * [!UICONTROL 帐户] — 仅发送帐户

      * [!UICONTROL 人员] — 仅发送人员

      * [!UICONTROL 帐户中的人员] — 发送帐户和与帐户相关的人员

   * **[!UICONTROL 传出字段]** — 将表中的每个字段映射到[XDM字段](../admin/xdm-field-management.md)。 这些字段在请求正文中发送到外部服务。 服务定义属性： `invocationPayloadDef.accountFields`，`invocationPayloadDef.fields`。

   ![映射外部操作传出字段](./assets/configuration-external-actions-fields.png){width="600" zoomable="yes"}

   * **[!UICONTROL 传入字段]** — 将表中的每个字段映射到[可更新的XDM字段](../admin/xdm-field-management.md#updatable-fields)。 这些字段从外部服务响应中填充。 服务定义属性： `callbackPayloadDef.accountFields`，`callbackPayloadDef.fields`。 创建后可更新。

   * **[!UICONTROL 标头参数]** — 为请求中要作为HTTP标头传递的每一行输入一个值。 服务定义属性： `invocationPayloadDef.headers`。

   * **[!UICONTROL 超时]** — 输入在请求被视为失败之前等待外部服务调用回调的分钟数。 服务定义属性： `timeout`。

   * **[!UICONTROL 全局属性]** — 为每一行输入一个值，以作为静态字段包含在请求正文中。 服务定义属性： `invocationPayloadDef.globalAttributes`。

   ![外部操作标头参数、超时和全局属性](./assets/configuration-external-actions-header-timeout-global.png){width="600" zoomable="yes"}

1. 单击&#x200B;_上退箭头_&#x200B;返回列表并将操作保持在&#x200B;_草稿_&#x200B;状态。

   或者，单击&#x200B;**[!UICONTROL 激活]**&#x200B;以将操作配置更改为&#x200B;_活动_&#x200B;状态。 配置的外部操作必须处于活动状态才能在帐户历程中使用。

## 向历程添加外部节点 {#add-journey-node}

在激活操作后，营销人员可以将&#x200B;_[!UICONTROL 外部操作]_&#x200B;或&#x200B;_[!UICONTROL 外部拆分路径]_&#x200B;节点添加到任何帐户历程。 有关如何在帐户历程画布中添加和使用这些节点的信息，请参阅[外部节点](../journeys/external-nodes.md)。
