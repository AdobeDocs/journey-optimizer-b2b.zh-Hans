---
title: 激活Marketo Engage以支持历程操作
description: 激活Marketo Engage连接以支持历程操作，以便营销人员能够在Marketo Engage和Journey Optimizer B2B edition之间协调营销活动。
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---


# 激活Marketo Engage实例以支持操作

Marketo Engage操作是&#x200B;_基于人员的_&#x200B;操作，通过此类操作，可在Journey Optimizer B2B edition和Marketo Engage中基于&#x200B;_潜在客户_&#x200B;的营销工作之间，协调您的&#x200B;_基于帐户的_&#x200B;营销编排。 使用这些操作可编排静态列表成员资格并将人员放入营销策划。

要使用Marketo Engage操作，管理员首先在Marketo Engage中创建[自定义服务](https://experienceleague.adobe.com/zh-hans/docs/marketo-developer/marketo/rest/custom-services#)，该服务提供身份验证所需的凭据。
然后，Journey Optimizer B2B edition的产品管理员通过输入凭据创建与Marketo Engage的连接。
然后，Journey Optimizer B2B edition用户可引用连接以在<!-- Person and -->帐户历程中配置Marketo Engage操作，例如从Marketo Engage列表中添加或删除人员，或将他们添加到请求营销活动。

Marketo Engage工作区对资产（如列表和营销活动）的可见性受在自定义服务中分配的角色权限控制。

同一连接可在历程中多次使用，不同的Marketo Engage连接可在单个历程中并存。

当操作运行时，它使用选择策略来确定Marketo Engage中的哪些人员记录来选择统一人员配置文件中是否存在多个标识符。 选项包括选择最旧、最新或所有匹配的Marketo Engage记录。 除了发生错误外，无论是否匹配，人员都会继续历程。

## 配置Marketo Engage连接

配置远程Marketo Engage实例以用于Marketo Engage历程操作。

### 创建Marketo Engage自定义服务

1. 以管理员身份登录Marketo Engage并创建自定义服务。
1. 记录用于连接的以下值：

   * Munchkin ID
   * 客户端 ID
   * 客户端密码

### 添加集成

![添加集成详细信息](assets/integration-connection-details.png)

1. 在Journey Optimizer B2B edition中，导航到&#x200B;**管理** > **配置**。
1. 选择到&#x200B;**集成**&#x200B;选项卡。
1. 单击&#x200B;**[!UICONTROL 创建连接]**。
1. 输入名称（必需）和说明（可选）。
1. 为匹配的人员记录选择&#x200B;**选择策略**。
1. 输入您的Munchkin ID、客户端ID和客户端密钥。
1. 单击&#x200B;**[!UICONTROL 连接到Marketo]**。
1. 单击&#x200B;**[!UICONTROL 创建]**。

当营销人员在旅程中使用Marketo Engage操作时，他们可以使用连接名称配置节点。

完成集成后，可从节点属性中的&#x200B;**对**&#x200B;执行的操作中执行Marketo Engage操作。

![Marketo操作列表](assets/marketo-actions-list.png)