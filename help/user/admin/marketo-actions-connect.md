---
title: 激活Marketo Engage以支持历程操作
description: 激活Marketo Engage连接以支持历程操作，以便营销人员能够在Marketo Engage和Journey Optimizer B2B edition之间协调营销活动。
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: 9b77570ddb9b416251f38db51a57507a935a526a
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---


# 激活Marketo Engage实例以支持操作

Marketo Engage操作是&#x200B;_基于人员的_&#x200B;操作，通过此类操作，可在Journey Optimizer B2B edition和Marketo Engage中基于&#x200B;_潜在客户_&#x200B;的营销工作之间，协调您的&#x200B;_基于帐户的_&#x200B;营销编排。 使用这些操作可编排静态列表成员资格并将人员放入营销策划。

要使用Marketo Engage历程操作，管理员首先在Marketo Engage中创建[自定义服务](https://experienceleague.adobe.com/zh-hans/docs/marketo-developer/marketo/rest/custom-services){target="_blank"}，该服务提供身份验证所需的凭据。 然后，Journey Optimizer B2B edition的产品管理员使用这些凭据创建与Marketo Engage的连接。 然后，Journey Optimizer B2B edition用户可引用连接以在<!-- person and -->帐户历程中配置Marketo Engage操作，例如从Marketo Engage列表中添加或删除人员，或将他们添加到请求营销活动。

## 配置Marketo Engage连接 {#external-marketo-configure}

>[!CONTEXTUALHELP]
>id="ajo-b2b_marketo-configure-connections"
>title="外部Marketo Engage连接"
>abstract="产品管理员可以配置与外部Marketo Engage实例的连接，以便执行历程操作。"

完成以下任务以配置外部Marketo Engage实例用于历程操作。

### 创建Marketo Engage自定义服务

1. 以管理员身份登录Marketo Engage并[创建自定义服务](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}。
1. 复制以下值以用于Journey Optimizer B2B edition连接：

   * Munchkin ID
   * 客户端 ID
   * 客户端密码

资产（如列表和营销活动）的Marketo Engage工作区可见性受自定义服务中分配的[角色权限](https://experienceleague.adobe.com/zh-hans/docs/marketo-developer/marketo/rest/custom-services#permission-list){target="_blank"}控制。 营销人员可以在一个历程中多次使用同一连接，并在同一历程中使用不同的Marketo Engage连接。

### 添加集成

![添加集成详细信息](assets/integration-connection-details.png){width="800" zoomable="yes"}

1. 在Journey Optimizer B2B edition中，导航到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 配置]**。
1. 选择到&#x200B;**[!UICONTROL 集成]**&#x200B;选项卡。
1. 单击&#x200B;**[!UICONTROL 创建连接]**。
1. 输入&#x200B;**[!UICONTROL Name]**（必需）和&#x200B;**[!UICONTROL Description]**（可选）。
1. 选择用于将操作应用于匹配人员记录的更新策略。

   为连接的Marketo Engage实例运行操作时，选定的&#x200B;_更新策略_&#x200B;确定Marketo Engage中的人员记录以选择统一人员配置文件中是否存在多个标识符。

   * **[!UICONTROL 更新所有匹配的记录]**
   * **[!UICONTROL 仅更新最旧的匹配记录]**
   * **[!UICONTROL 仅更新最新的匹配记录]**

   >[!NOTE]
   >
   >除了发生错误外，无论是否匹配，人员都会继续历程。

1. 输入在外部Munchkin实例中创建的服务的Marketo Engage ID、客户端ID和客户端密钥。
1. 单击&#x200B;**[!UICONTROL 连接到Marketo]**。
1. 单击&#x200B;**[!UICONTROL 创建]**。

## 在历程操作中使用连接

当营销人员在旅程中使用Marketo Engage操作时，他们可以使用连接名称配置节点。

完成集成后，可从节点属性中的&#x200B;**对**&#x200B;执行的操作中执行Marketo Engage操作。

![Marketo操作列表](assets/marketo-actions-list.png){width="800" zoomable="yes"}