---
title: 短信创作
description: 了解如何在其移动设备上向客户发送短信(SMS)，以及通过短信编辑器以文本格式个性化和预览消息。
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: eea4afcf352eeefbd5a67c4bfff6a4c2ec559319
workflow-type: tm+mt
source-wordcount: '1908'
ht-degree: 2%

---

# 短信创作

使用Adobe Journey Optimizer B2B Edition向客户在其移动设备上发送短信(SMS)。 您可以从短信编辑器中创建、个性化和预览文本格式的消息。

## SMS配置

Adobe Journey Optimizer B2B版本通过SMS服务提供商（或SMS网关提供商）发送文本消息。 在创建短信消息之前，请从&#x200B;_管理员_&#x200B;设置中配置服务提供商。

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

1. **向文本消息添加URL**。

   定义内容后，您可以通过单击&#x200B;_链接_&#x200B;图标，向消息添加URL。

   此操作将打开一个对话框，您可以在其中选择要链接的两种URL类型之一：

   * **[!UICONTROL 外部URL]** — 此类型是您在文本框中输入的任何外部URL。
   * **[!UICONTROL 登陆页面]** — 选择此选项可从您的Marketo Engage实例中选择任何已批准的Adobe Marketo Engage Design Studio登陆页面。

   该对话框还包括URL链接的选项：

   * **[!UICONTROL 缩短URL]** — 选中此复选框可&#x200B;_缩短_ URL，这是跟踪所必需的。 对于登陆页面，它会使用缩短URL的Marketo Engage子域。 此时将显示缩短的URL格式的示例。 实际URL是在将短信发送给收件人时创建的。

   * **[!UICONTROL 包含mkt_tok]** — 选中此复选框可跟踪针对用户的活动。

   链接选项完成后，单击&#x200B;**[!UICONTROL 添加]**&#x200B;以保存更改并将URL链接添加到短信消息。

## 设置短信属性

1. 在&#x200B;_[!UICONTROL 短信属性]_&#x200B;部分中，为您的消息输入&#x200B;**[!UICONTROL Name]**（必需，最多100个字符）和&#x200B;**[!UICONTROL Description]**（可选，最多300个字符）。

   这些字段允许Alpha、数字和特殊字符。 以下保留字符是&#x200B;**不允许的**： `\`、`/`、`:`、`*`、`?`、`"`、`<`、`>`和`|`。

1. 选择&#x200B;**[!UICONTROL 短信类型]**：

   * 将`Marketing`用于需要用户同意的促销短信。
   * 将`Transactional`用于非商业邮件，如订单确认、密码重置通知或投放信息。

1. 对于&#x200B;**[!UICONTROL SMS配置]**，请选择预定义的API配置之一。

   此设置确定用于传递消息的SMS网关服务提供商和帐户。

1. 输入要&#x200B;用于通信的&#x200B;**[!UICONTROL 发件人号码]**。

   ![执行操作 — 发送短信](./assets/sms-properties.png){width="700" zoomable="yes"}

   收件人号码始终映射到Marketo Engage中的`Lead.mobilePhone`字段。

## 模拟短信内容 {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_sms_preview_simulate"
>title="检查您的内容的渲染方式"
>abstract="定义内容后可预览它，并根据所使用的渠道检查渲染是否正确。"

定义消息内容后，您可以使用测试用户档案来模拟（预览）其内容。 如果插入个性化内容，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

>[!IMPORTANT]
>
>请确保先保存短信消息，然后再继续模拟短信。

1. 单击短信创作工作区顶部的&#x200B;**[!UICONTROL 模拟内容]**。

1. 在&#x200B;_[!UICONTROL 模拟内容]_&#x200B;页面中，单击&#x200B;**[!UICONTROL 添加联系人]**。

1. 使用&#x200B;_模拟内容_&#x200B;页面管理用于测试配置文件的潜在客户。

   在显示的列表中，您可以从Marketo Engage潜在客户数据库中搜索并添加任何潜在客户（一次最多10个潜在客户）。

   要搜索，请输入整个电子邮件地址，然后按&#x200B;_Enter_。 将显示相应的潜在客户配置文件以供选择。

   所选配置文件的个性化字段的预览更新。

   所有添加的潜在客户都显示在左侧。

   您可以通过添加更多人员并从配置文件列表中删除各个潜在客户来管理此列表（它不会从数据库中删除这些潜在客户）。

1. 模拟选定商机的内容。

   选择左侧列出的任何潜在客户，页面上的短信预览将更新相应潜在客户。

   您还可以从预览空间上方的选择器中选择潜在客户，以更新相应潜在客户的页面上的SMS预览。

1. 要退出&#x200B;_[!UICONTROL 模拟内容]_&#x200B;页面并返回短信创作工作区，请单击右上方的&#x200B;**[!UICONTROL 关闭]**。

## 短信同意管理

向收件人提供取消订阅以停止从品牌接收通信的功能，并遵守此选择是一项法律要求。 未能遵守这些法规会为您的品牌带来法律风险。 此功能还可帮助您避免向收件人发送未经请求的通信，这种通信可能会导致他们将您的邮件标记为垃圾邮件并损害您的声誉。

提供此选项后，短信收件人可以使用选择启用和选择禁用关键词进行回复。 支持并接受所有标准的选择加入和选择退出关键词，以及短信服务提供商配置的任何自定义关键词。 取消订阅后，用户档案将自动从未来营销消息的受众中删除。

Journey Optimizer B2B版本提供了使用以下逻辑管理短信消息中的选择退出的功能：

* 默认情况下，如果商机选择不接收您的通信，则相应的用户档案将从后续短信投放中排除

* 来自不同来源（例如AEP或SMS服务提供商）的潜在客户同意将同步到Journey Optimizer B2B版本。 目前，在实例级别，它仅支持每个商机的单个同意状态（商机“John Doe”订阅或取消订阅实例中的所有促销短信）。 它当前不支持在品牌级别/单个订阅列表级别同意双重选择加入。
