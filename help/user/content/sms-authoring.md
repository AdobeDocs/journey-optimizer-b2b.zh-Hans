---
title: 短信创作
description: 了解如何在其移动设备上向客户发送短信(SMS)，以及通过短信编辑器以文本格式个性化和预览消息。
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: e0d9359560f31b3e66f593426c66e64d31044d54
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%

---

# 短信创作

使用Adobe Journey Optimizer B2B Edition向客户在其移动设备上发送短信(SMS)。 您可以通过短信编辑器以文本格式创建、个性化和预览消息。

## SMS配置

Adobe Journey Optimizer B2B版本通过SMS服务提供商（或SMS网关提供商）发送文本消息。 在创建短信消息之前，请从“管理员”设置配置服务提供商。

### SMS网关服务提供商

Adobe Journey Optimizer B2B版本目前与独立提供文本消息服务的第三方提供商集成。 受支持的短信提供商有Sinch、Twilio和Infobip。

在Adobe Journey Optimizer B2B版本中配置短信渠道之前，必须向这些提供商之一创建帐户，以获取API令牌和服务ID。 配置Adobe Journey Optimizer B2B Edition与适用提供商之间的连接时需要这些凭据。

>[!IMPORTANT]
>
>您对短信服务的使用受适用提供商提供的其他条款与条件的约束。 作为第三方解决方案，Adobe Journey Optimizer B2B Edition用户可通过集成使用Sinch、Twilio和Infobip。 Adobe不控制，也不对第三方产品负责。 有关短信服务(SMS)的任何问题或协助请求，请与提供商联系。

### 验证现有SMS API配置

>[!NOTE]
>
>仅具有短信管理员权限的用户可访问描述的设置。

在左侧导航栏中，展开&#x200B;**[!UICONTROL 管理员]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 配置]**。

![访问AMA API凭据的配置](./assets/config-sms-api.png){width="800" zoomable="yes"}

页面列出了实例的可用API配置。 您可以通过SMS服务提供商或创建者筛选显示的API凭据。

![单击筛选器图标以筛选API凭据列表](./assets/config-sms-api-filter.png){width="500"}

### 为SMS服务提供商创建新的API凭据

>[!BEGINTABS]

>[!TAB Sinch]

_要将Sinch配置为您的SMS提供商，请添加Adobe Journey Optimizer B2B版本：_

1. 在左侧导航栏中，展开&#x200B;**[!UICONTROL 管理员]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 配置]**。

1. 单击&#x200B;_[!UICONTROL API凭据]_&#x200B;列表右上角的&#x200B;**[!UICONTROL 创建新API凭据]**。

1. 配置您的SMS API凭据：

   ![配置Sinch SMS API凭据](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL SMS供应商]** — 选择`Sinch`作为SMS提供商。

   * **[!UICONTROL 名称]** — 输入API凭据的名称。

   * **[!UICONTROL 服务ID]**&#x200B;和&#x200B;**[!UICONTROL API令牌]** — 从你的Sinch帐户访问API页面（你可以在“短信”选项卡下找到你的凭据）。

   有关查找你的Sinch帐户的此信息的详细信息，请参阅[Sinch开发人员文档](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)

1. 完成API凭据的配置详细信息后，单击&#x200B;**[!UICONTROL 提交]**。

>[!TAB Twilio]

_要将Twilio配置为您的SMS提供商，请添加Adobe Journey Optimizer B2B版本：_

1. 在左侧导航栏中，展开&#x200B;**[!UICONTROL 管理员]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 配置]**。

1. 单击&#x200B;_[!UICONTROL API凭据]_&#x200B;列表右上角的&#x200B;**[!UICONTROL 创建新API凭据]**。

1. 配置您的SMS API凭据：

   ![配置Twilio SMS API凭据](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL SMS供应商]** — 选择`Twilio`作为SMS提供商。

   * **[!UICONTROL 名称]** — 输入API凭据定义的名称。

   * **[!UICONTROL 帐户SID]**&#x200B;和&#x200B;**[!UICONTROL 身份验证令牌]** — 访问Twilio控制台仪表板页面的&#x200B;_帐户信息_&#x200B;窗格以查找你的凭据。

   有关为您的Twilio帐户查找此信息的详细信息，请参阅[Twilio帮助中心](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-)。

1. 完成API凭据的配置详细信息后，单击页面右上角的&#x200B;**[!UICONTROL 提交]**。

>[!TAB Infobip]

_要通过Adobe Journey Optimizer B2B版本将Infobip配置为您的SMS提供程序：_

1. 在左侧导航栏中，展开&#x200B;**[!UICONTROL 管理员]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL 配置]**。

1. 单击&#x200B;_[!UICONTROL API凭据]_&#x200B;列表右上角的&#x200B;**[!UICONTROL 创建新API凭据]**。

1. 配置您的SMS API凭据：

   ![配置Infobip SMS API凭据](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL SMS供应商]** — 选择`Infobip`作为SMS提供商。

   * **[!UICONTROL 名称]** — 输入API凭据定义的名称。

   * **[!UICONTROL API基本URL]**&#x200B;和&#x200B;**[!UICONTROL API密钥]** — 访问您的Web界面主页或Infobip帐户的API密钥管理页面以查找您的凭据。

   有关为您的Infobip帐户查找此信息的详细信息，请参阅[Infobip文档](https://www.infobip.com/docs/api/_blank)。

1. 完成API凭据的配置详细信息后，单击页面右上角的&#x200B;**[!UICONTROL 提交]**。

>[!ENDTABS]

单击&#x200B;_[!UICONTROL 提交]_&#x200B;后，将立即验证并保存凭据，并将您重定向到&#x200B;_[!UICONTROL API凭据]_&#x200B;列表页面。 如果提交的凭据无效，系统会在列表页面上显示错误消息。 在这种情况下，您可以选择取消配置，或更新配置并重新提交。

## 在帐户历程中添加短信操作

在添加&#x200B;_[!UICONTROL Take an action]_&#x200B;历程并执行以下操作时，可以在Account节点中设置短信投放：

1. 对于&#x200B;]_目标上的_[!UICONTROL &#x200B;操作，请选择&#x200B;**[!UICONTROL 人员]**。

1. 若要对人员&#x200B;]_执行_[!UICONTROL &#x200B;操作，请选择&#x200B;**[!UICONTROL 发送短信]**。

   ![执行操作 — 发送短信](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 执行操作]_&#x200B;面板的底部，单击&#x200B;**[!UICONTROL 创建短信]**。

1. 在对话框中，为电子邮件输入唯一的&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 主题行]**。

   ![新建短信对话框](assets/create-new-sms.png){width="500"}

## 创建短信消息

>[!IMPORTANT]
>
>**短信同意管理**<br/>
><br/>
>根据行业标准和法规，所有短信营销消息都必须包含一种让接收者轻松取消订阅的方式。 要实现此目的，短信收件人可以使用选择启用和选择禁用关键词进行回复。 支持并遵循所有标准的选择加入和选择退出关键词。 此外，还支持并遵循为短信服务提供商帐户配置的任何自定义关键字。

1. 在&#x200B;**[!UICONTROL 消息]**&#x200B;字段中输入要发送的文本。

   您可以创建最多1600个字符的消息，每160个字符即被视为一条短信消息。

1. **个性化设置短信**。

   在创作文本消息时，随时单击文本消息框右侧的&#x200B;_个性化_&#x200B;图标。

   ![单击“个性化”图标向邮件添加令牌](./assets/sms-message-personalize-icon.png){width="800" zoomable="yes"}

   显示的页面提供了对Adobe Marketo Engage潜在客户和系统令牌的访问权限。 包括标准令牌和自定义令牌。 您可以使用搜索栏找到所需的令牌，或浏览文件夹树以查找并选择任何潜在客户/系统令牌。

   将光标放在要添加令牌的消息中的位置。 通过单击令牌旁边的加号( **+**)符号添加令牌。 如果要添加带有回退的令牌（如果该字段对于潜在客户不可用，将显示默认值），请单击省略号( **...** )，然后选择&#x200B;**[!UICONTROL 插入带有回退文本]**。

   ![单击省略号以使用令牌的回退](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

   在&#x200B;_[!UICONTROL 输入回退值]_&#x200B;对话框中，输入显示为回退的文本，然后单击&#x200B;**[!UICONTROL 添加]**。

   ![输入令牌的回退文本](./assets/sms-message-personalize-fallback-text.png){width="400"}

   放置个性化令牌后，单击&#x200B;**[!UICONTROL 保存]**&#x200B;以保存更改并返回主短信创作工作区。 您可以根据需要继续编辑包含令牌的消息。

<!-- 1. **Add URLs to text message**.

   After defining your content, you can add URLs to your message by clicking the _Link_ icon.
   
   You can add two types of URLs: 

   External URLs - This is ANY external URL that can be directly typed into/ pasted into the input text box
   Adobe Marketo Engage Design Studio Landing Pages - Selecting this option, you will see a 'Landing Page picker' from which you can select any of the listed approved Landing Pages from Marketo Engage

   You can choose to 'shorten' either of these URLs by selecting the checkbox
   Note that the URL shortening function, uses the Marketo subdomain for shortening
   The shortened URL appears as a read-only field within the modal
   You can optionally track clicks on the URL
   You can also choose to include 'mkt_tok' for tracking activity against a user
   Click on Add to save changes & add the chosen URL to the SMS message
-->

## 设置短信属性

1. 在&#x200B;_[!UICONTROL SMS属性]_&#x200B;部分中，为您的消息输入&#x200B;**[!UICONTROL Name]**（必需，最多100个cha\racter）和&#x200B;**[!UICONTROL Description]**（可选，最多300个字符）。

   这些字段允许Alpha、数字和特殊字符。 以下保留字符是&#x200B;**不允许的**： `\`、`/`、`:`、`*`、`?`、`"`、`<`、`>`和`|`。

1. 选择&#x200B;**[!UICONTROL 短信类型]**：

   * 将`Marketing`用于需要用户同意的促销短信。
   * 将`Transactional`用于非商业邮件，如订单确认、密码重置通知或投放信息。

1. 对于&#x200B;**[!UICONTROL SMS配置]**，请选择预定义的API配置之一。

   此设置确定用于传递消息的SMS网关服务提供商和帐户。

1. 输入要&#x200B;用于通信的&#x200B;**[!UICONTROL 发件人号码]**。

   ![执行操作 — 发送短信](./assets/sms-properties.png){width="700" zoomable="yes"}

   收件人号码始终映射到Marketo Engage中的`Lead.MainPhone`字段。

<!-- ## Preview the text message content

When your message content is defined, you can use test profiles to preview its content. If you inserted personalized content, you can check how this content is displayed in the message, using test profile data.

1. Click **[!UICONTROL Simulate Content]** at the top of the SMS authoring workspace.

1. From the _[!UICONTROL Simulate Content]_ page, click **[!UICONTROL Add People]**.

1. Use the # page to manage the leads used for your test profile.

   In the displayed list, you can search for and add any of the leads (up to 10 leads at a time) from the Marketo Engage lead database.

   To search, enter the whole email address and click enter. The corresponding lead profile shows up for selection.

   The preview updated to the personalization fields for the selected profile.

   All the added leads appear on the left rail of the 'Simulate Content' page

   You can manage this list by adding more people and deleting individual leads from the profile listing (it does not remove them from the database).

1. Simulate content for a lead.

   Select any of the leads listed on the left rail of the Simulate Content page and the SMS preview on the page updates for the corresponding lead.

   You can also select a lead from the 'drop-down' box above the preview space and the SMS preview on the page updates for the corresponding lead

1. To exit the _[!UICONTROL Simulate Content]_ page and return back to the SMS authoring workspace, click Close. -->
