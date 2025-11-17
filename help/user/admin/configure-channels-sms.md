---
title: 短信配置
description: 将Sinch、Twilio和Infobip等SMS提供商连接到API凭据，以在Journey Optimizer B2B edition历程中启用文本消息。
feature: Setup, Channels
role: Admin
exl-id: bd41a5ec-929f-489f-a757-0720c1b44ed2
source-git-commit: 325ae8e8c1f3bbf25e0d96907ede6cb9f2e76e3d
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# 短信配置

Adobe Journey Optimizer B2B edition通过短信服务提供商（或短信网关提供商）发送文本消息。 在创建短信消息之前，请从&#x200B;_管理员_&#x200B;设置中配置服务提供商。

## SMS网关服务提供商

Adobe Journey Optimizer B2B edition目前与独立提供短信服务的第三方提供商集成。 受支持的短信提供商有Sinch、Twilio和Infobip。

在Adobe Journey Optimizer B2B edition中配置短信渠道之前，必须向这些提供商之一创建帐户，以获取API令牌和服务ID。 配置Adobe Journey Optimizer B2B edition与适用提供商之间的连接时需要这些凭据。

>[!IMPORTANT]
>
>您对短信服务的使用受适用提供商提供的其他条款与条件的约束。 作为第三方解决方案，Adobe Journey Optimizer B2B edition用户可通过集成使用Sinch、Twilio和Infobip。 Adobe不控制，也不负责第三方产品。 有关短信服务(SMS)的任何问题或协助请求，请与提供商联系。

## 验证现有SMS API配置

>[!NOTE]
>
>仅具有短信管理员权限的用户可访问描述的设置。

1. 在左侧导航栏中，展开&#x200B;**[!UICONTROL 管理员]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 渠道]**。

   ![访问SMS API凭据的配置](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. 在导航面板中，选择&#x200B;**[!UICONTROL API凭据]**。

   页面列出了实例的可用API配置。

1. 如果需要，请单击&#x200B;_筛选器_&#x200B;图标（![显示或隐藏筛选器图标](../assets/do-not-localize/icon-filter.svg)），然后选择相应选项以显示SMS服务提供商或创建者配置的API凭据列表。

   ![单击“筛选器”图标以优化API凭据列表](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

## 为SMS服务提供商创建新的API凭据

>[!BEGINTABS]

>[!TAB Sinch]

使用Adobe Journey Optimizer B2B edition将Sinch配置为短信提供商(_T):_

1. 在左侧导航栏中，展开&#x200B;**[!UICONTROL 管理员]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 配置]**。

1. 单击&#x200B;**[!UICONTROL API凭据]**&#x200B;列表右上角的&#x200B;_[!UICONTROL 创建新API凭据]_。

1. 配置您的SMS API凭据：

   ![配置Sinch SMS API凭据](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL SMS供应商]** — 选择`Sinch`作为SMS提供商。

   * **[!UICONTROL 名称]** — 输入API凭据的名称。

   * **[!UICONTROL 服务ID]**&#x200B;和&#x200B;**[!UICONTROL API令牌]** — 从你的Sinch帐户访问API页面（你可以在“短信”选项卡下找到你的凭据）。

   有关查找你的Sinch帐户的此信息的详细信息，请参阅[Sinch开发人员文档](https://developers.sinch.com/docs/sms/getting-started)

1. 完成API凭据的配置详细信息后，单击&#x200B;**[!UICONTROL 提交]**。

>[!TAB Twilio]

要将Twilio配置为使用Adobe Journey Optimizer B2B edition的短信提供商(_T):_

1. 在左侧导航栏中，展开&#x200B;**[!UICONTROL 管理员]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 配置]**。

1. 单击&#x200B;**[!UICONTROL API凭据]**&#x200B;列表右上角的&#x200B;_[!UICONTROL 创建新API凭据]_。

1. 配置您的SMS API凭据：

   ![配置Twilio SMS API凭据](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL SMS供应商]** — 选择`Twilio`作为SMS提供商。

   * **[!UICONTROL 名称]** — 输入API凭据定义的名称。

   * **[!UICONTROL 帐户SID]**&#x200B;和&#x200B;**[!UICONTROL 身份验证令牌]** — 访问Twilio控制台仪表板页面的&#x200B;_帐户信息_&#x200B;窗格以查找你的凭据。

   有关为您的Twilio帐户查找此信息的详细信息，请参阅[Twilio帮助中心](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-)。

1. 完成API凭据的配置详细信息后，单击页面右上角的&#x200B;**[!UICONTROL 提交]**。

>[!TAB Infobip]

使用Adobe Journey Optimizer B2B edition将Infobip配置为短信提供商(_T):_

1. 在左侧导航栏中，展开&#x200B;**[!UICONTROL 管理员]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 配置]**。

1. 单击&#x200B;**[!UICONTROL API凭据]**&#x200B;列表右上角的&#x200B;_[!UICONTROL 创建新API凭据]_。

1. 配置您的SMS API凭据：

   ![配置Infobip SMS API凭据](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL SMS供应商]** — 选择`Infobip`作为SMS提供商。

   * **[!UICONTROL 名称]** — 输入API凭据定义的名称。

   * **[!UICONTROL API基本URL]**&#x200B;和&#x200B;**[!UICONTROL API密钥]** — 访问您的Web界面主页或Infobip帐户的API密钥管理页面以查找您的凭据。

   有关为您的Infobip帐户查找此信息的详细信息，请参阅[Infobip文档](https://www.infobip.com/docs/api/_blank)。

1. 完成API凭据的配置详细信息后，单击页面右上角的&#x200B;**[!UICONTROL 提交]**。

>[!ENDTABS]

单击&#x200B;_[!UICONTROL 提交]_&#x200B;后，将立即验证并保存凭据，并将您重定向到&#x200B;_[!UICONTROL API凭据]_&#x200B;列表页面。 如果提交的凭据无效，系统会在列表页面上显示错误消息。 在这种情况下，您可以选择取消配置，或更新配置并重新提交。
