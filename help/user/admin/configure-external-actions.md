---
title: 外部操作配置
description: 了解开发人员、管理员和营销人员如何协作来实施、配置和使用外部操作，以便将Journey Optimizer B2B edition与帐户历程中的外部服务相关联。
feature: Setup, Integrations
role: Admin, Developer
exl-id: 226fbf23-7df2-4fd7-b5a4-2057a417a261
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: effa8e2a45ecc5afbaa5a3f75437735bef89a400
workflow-type: tm+mt
source-wordcount: 1306
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
>回调函数需要持有者令牌。 通过在Adobe Developer Console[&#128279;](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)中为您的IMS组织设置OAuth服务器到服务器凭据来检索此项。

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

   外部服务必须处于活动状态并且可访问，才能成功完成此步骤。 如果存在验证错误，对话框将显示一条描述错误的消息以及解决该错误的建议。 有关详细信息，请参阅&#x200B;[_疑难解答_](#troubleshooting)。

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

### 故障排除 {#troubleshooting}

当您输入外部服务的OpenAPI规范的URL并单击&#x200B;**[!UICONTROL 创建]**&#x200B;时，系统会执行服务验证。 当遇到错误时，对话框会显示消息以描述错误。

![外部操作URL服务验证错误消息](./assets/configuration-external-actions-create-url-error.png){width="600" zoomable="yes"}

>[!NOTE]
>
>以下许多错误都需要与创建和发布面向公众的Web服务的开发人员合作才能解决。

#### 验证错误详细信息

| 显示的错误 | 为什么会这样 | 要做什么 |
|---|---|---|
| `This URL is already used by another external action` | 此规范URL已注册到贵组织中的其他操作。 | 使用其他规范URL，或删除已使用该规范URL的现有操作。 |
| `An action with this name already exists` | 规范中的`info.title`与已存在的操作匹配 | 将规范`info.title`字段中的标题更改为其他唯一内容。 |
| `Duplicate operation ID found in the specification` | 规范中的两个或多个操作共享相同的`operationId`。 | 为每个操作指定一个唯一的`operationId`。 |
| `Field in the specification exceeds the maximum allowed length` | 规范中的文本字段（如标题或描述）太长。 | 缩短标记的字段。 |
| `The entity type value is invalid` | 实体类型的特定于Adobe的`x-`扩展具有无法识别的值 | 将实体类型更正为支持的值。 有关有效选项，请参阅[开发人员文档](https://developer.adobe.com/journey-optimizer-b2b-apis/)。 |
| `The provided document is not a valid OpenAPI specification` | 规范无法进行结构解析。 | 根据OpenAPI 3.0架构验证您的规范并修复任何问题。 |
| `Required OpenAPI field is missing` | 缺少标准OpenAPI必填字段（如`info`或`paths`）。 | 添加缺少的字段。 |
| `Required endpoint is missing from the specification` | 您的规范中未定义Adobe Journey Optimizer B2B edition所需的端点。 | 添加所需的端点。 请参阅需要端点的[开发人员文档](https://developer.adobe.com/journey-optimizer-b2b-apis/)。 |
| `Required extension field is missing` | 您的规范中不存在必需的Adobe `x-`扩展字段。 | 按照文档中的说明，添加缺少的扩展字段。 |
| `Security schemes are missing from the specification` | 您的规范没有在`components`下定义`securitySchemes`。 | 定义至少一个安全方案。 |
| `Multiple authentication types are not supported` | 您的规范定义了多个身份验证方案。 | 更新您的规范以使用单一身份验证类型。 |
| `The authentication type is not supported` | 不支持您使用的安全方案类型（如`oauth2`或`openIdConnect`）。 | 切换到支持的身份验证类型。 有关支持的选项，请参阅开发人员文档。 |
| `The OpenAPI version is not supported` | 规格级别的版本不匹配 | 更新您的规格以使用OpenAPI 3.0.x。 |
| `An unexpected error occurred` | 在您的规范中发现未分类的问题。 | 检查您的规格中是否有任何不寻常的情况，然后重试。 如果错误仍然存在，请联系支持人员。 |

<!--
## Errors you'll see if something goes wrong with the request itself

This error appears below the URL field (not in the alert banner) and means there was a network problem or an unexpected server response — not a problem with your URL or spec.

| What you'll see | Why it happened | What to do |
|---|---|---|
| `Failed to create external action. Please try again.` | A network error occurred or the server returned an unexpected response | Check your connection and try again. If it keeps happening, contact support |
-->

## 向历程添加外部节点 {#add-journey-node}

在激活操作后，营销人员可以将&#x200B;_[!UICONTROL 外部操作]_&#x200B;或&#x200B;_[!UICONTROL 外部拆分路径]_&#x200B;节点添加到任何帐户历程。 有关如何在帐户历程画布中添加和使用这些节点的信息，请参阅[外部节点](../journeys/external-nodes.md)。
