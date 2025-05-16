---
title: 电子邮件渠道配置
description: 了解如何访问和查看Marketo Engage中配置的电子邮件设置。
feature: Setup, Channels
role: Admin
exl-id: fb16b5e5-f1a5-4e59-b8c6-56985f03225a
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 0%

---

# 电子邮件渠道配置

Adobe Journey Optimizer B2B edition可利用Marketo Engage中的渠道功能和事件跟踪。 管理员应确保已设置投放和跟踪配置，以便为营销人员启用渠道投放。 有关通过Marketo Engage进行电子邮件投放和跟踪所需协议的信息，请参阅[跟踪和电子邮件投放协议](../start/email-protocols.md)。

## 投放设置

营销人员在帐户历程中创建电子邮件时，将使用默认电子邮件设置。 若要查看电子邮件投放设置，请转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**。 在导航面板中的&#x200B;_[!UICONTROL 电子邮件]_&#x200B;下，选择&#x200B;**[!UICONTROL 投放设置]**。

![访问电子邮件投放设置](./assets/config-email-delivery-email-header.png){width="800" zoomable="yes"}

Journey Optimizer B2B edition中的设置是只读的。 单击右上角的&#x200B;**[!UICONTROL 编辑设置]**&#x200B;可访问连接的Marketo Engage实例中的配置选项。

>[!NOTE]
>
>要在Adobe Marketo Engage中访问和编辑这些设置，您必须具有产品管理员权限。

选择以下每个选项卡以查看当前设置。

### [!UICONTROL 电子邮件标头参数] {#email-header}

电子邮件标头参数定义了以下项的默认值：

* **[!UICONTROL 发件人电子邮件]** — 电子邮件标头的&#x200B;_发件人_&#x200B;字段中列出的电子邮件地址。

* **[!UICONTROL 发件人标签]** — 显示的电子邮件发件人地址名称。

* **[!UICONTROL 取消订阅HTML]** — 显示在非运营电子邮件中的HTML（适用于受支持的电子邮件客户端），用于向收件人说明取消订阅操作。 此文本和链接将附加到底部。

* **[!UICONTROL 取消订阅文本]** — 在非运行电子邮件中显示的纯文本，用于向收件人解释取消订阅操作。 此文本和链接将附加到底部。

* **[!UICONTROL 以网页形式查看HTML]** — 用于&#x200B;_以网页形式查看_&#x200B;的HTML（适用于受支持的电子邮件客户端），该网页提供了一个链接，可在浏览器中显示电子邮件。

* **[!UICONTROL 以网页文本查看]** — 纯文本用于&#x200B;_以网页形式查看_，它提供了一个链接，可在浏览器中显示电子邮件。

### [!UICONTROL 品牌化域] {#branding-domains}

要检查品牌推广域，请单击&#x200B;**[!UICONTROL 品牌推广域]**&#x200B;选项卡。

![访问品牌策略域设置](./assets/config-email-delivery-branding-domains.png){width="700" zoomable="yes"}

此设置为一个或多个Marketo Engage工作区定义主域。 新电子邮件使用此域作为默认域，但营销人员可以根据每封电子邮件覆盖此域。 有关详细信息，请参阅[Marketo Engage文档](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/edit-your-default-branding-domain){target="_blank"}。

>[!NOTE]
>
>如果您在Journey Optimizer B2B edition和连接的Marketo Engage实例中推广多个品牌，并希望每个品牌都有自己的品牌跟踪链接，则可以添加额外的品牌推广域。 有关详细信息，请参阅[Marketo Engage文档](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/add-an-additional-branding-domain){target="_blank"}。

### [!UICONTROL 自定义标头选项] {#custom-header-options}

要查看自定义标题选项，请单击&#x200B;**[!UICONTROL 自定义标题选项]**&#x200B;选项卡。

![访问自定义标头选项](./assets/config-email-delivery-custom-header.png){width="700" zoomable="yes"}

启用&#x200B;_[!UICONTROL 严格传输安全]_&#x200B;后，它将保证通过HTTPS提供跟踪链接（仅适用于具有受SSL保护的跟踪链接的订阅）。

## 通信限制

通信限制控制贵组织发送的电子邮件数量。 最佳做法是设置限制，这样您就不会让收件人对来自贵组织的过多电子邮件感到不知所措。

若要查看当前设置，请转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**。 在导航面板中的&#x200B;_[!UICONTROL 电子邮件]_&#x200B;下，选择&#x200B;**[!UICONTROL 通信限制]**。

![访问通信限制设置](./assets/config-email-communication-limits.png){width="700" zoomable="yes"}

Journey Optimizer B2B edition中的设置是只读的。 单击右上角的&#x200B;**[!UICONTROL 编辑设置]**&#x200B;可访问连接的Marketo Engage实例中的配置选项。

>[!NOTE]
>
>要在Adobe Marketo Engage中访问和编辑这些设置，您必须具有产品管理员权限。

有关配置通信限制的更多信息，请参阅[Marketo Engage文档](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/email-setup/enable-communication-limits){target="_blank"}。

## SPF/DKIM

通过将SPF (Sender Policy Framework)和DKIM (Domain Keys Identified Mail)整合到DNS设置中，提高电子邮件投放率。 这些技术可确保收件人不会收到垃圾邮件。 为帮助防止收件人的垃圾邮件过滤器拒绝电子邮件，请确保为您的域设置了SPF和DKIM。

若要查看当前设置，请转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**。 在导航面板中的&#x200B;_[!UICONTROL 电子邮件]_&#x200B;下，选择&#x200B;**[!UICONTROL SPF/DKIM]**。

![访问SPF/DKIM配置](./assets/config-email-spf-dkim.png){width="700" zoomable="yes"}

Journey Optimizer B2B edition中的设置是只读的。 单击右上角的&#x200B;**[!UICONTROL 编辑设置]**&#x200B;可访问连接的Marketo Engage实例中的配置选项。

>[!NOTE]
>
>要在Adobe Marketo Engage中访问和编辑这些设置，您必须具有产品管理员权限。

### SPF设置

网络管理员应将以下行添加到您的DNS条目中：

`[domain] IN TXT v=spf1 mx ip4:[corpIP] include:mktomail.com ~all`

在此条目中，将`[domain]`替换为网站的主域（如`company.com`），将`[corpIP]`替换为公司电子邮件服务器的IP地址（如`255.255.255.255`）。 如果您通过Marketo Engage从多个域发送电子邮件，请在一行中为每个域添加此条目。

如果您的DNS条目中已有SPF记录，请添加以下内容：

`include:mktomail.com`

### DKIM设置

DKIM是一种身份验证协议，电子邮件接收者使用它来验证电子邮件的发件人。 它通常会提高向收件箱发送电子邮件的可投放性，因为接收者可以确信该消息不是伪造。

在DNS记录中激活公钥并在连接的Marketo Engage实例中激活发送域后，自定义DKIM签名将用于发送消息。 自定义DKIM签名包含加密的数字签名，其中包含在发送的每封电子邮件中。 然后，接收方可通过在发送域的DNS中查找&#x200B;_公钥_&#x200B;来解密数字签名。 如果电子邮件中的密钥与DNS记录中的密钥相对应，则接收邮件服务器更有可能接受通过Marketo Engage发送的电子邮件。

有关为电子邮件投放配置自定义DKIM签名的更多信息，请参阅[Marketo Engage文档](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}。

## 机器人活动

电子邮件机器人活动可能会错误地夸大您的电子邮件打开次数和点击数据。

Marketo Engage使用两种方法确认机器人活动：

* **与交互式Advertising局(IAB)列表匹配** — 与IAB UA/IP（用户代理/IP地址）列表上的任何内容匹配的活动将被标记为机器人。

* **与邻近模式匹配** — 当同时发生两个或多个活动时（在一秒内），它们将被识别为机器人。 此方法会考虑以下属性进行比较：

   * 商机ID（应相同）
   * 电子邮件资源（应相同）
   * 链接点击或电子邮件打开
   * 时间差（应小于1秒）

对于电子邮件链接点击和电子邮件打开活动，新属性将填充以下值：

* 识别为机器人的活动将&#x200B;_机器人活动_&#x200B;作为`True`，将&#x200B;_机器人活动模式_&#x200B;作为识别的模式/方法。
* 被识别为不是机器人的活动将&#x200B;_机器人活动_&#x200B;作为`False`，将&#x200B;_机器人活动模式_&#x200B;作为`N/A`。
* 在引入属性之前发生的活动将&#x200B;_机器人活动_&#x200B;设置为空(null)，将&#x200B;_机器人活动模式_&#x200B;设置为空(null)

若要查看当前设置，请转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**。 在导航面板中的&#x200B;_[!UICONTROL 电子邮件]_&#x200B;下，选择&#x200B;**[!UICONTROL 机器人活动]**。

![访问电子邮件投放的机器人活动配置](./assets/config-email-bot-activity.png){width="700" zoomable="yes"}

Journey Optimizer B2B edition中的设置是只读的。 单击右上角的&#x200B;**[!UICONTROL 编辑设置]**&#x200B;可访问连接的Marketo Engage实例中的配置选项。

>[!NOTE]
>
>要在Adobe Marketo Engage中访问和编辑这些设置，您必须具有产品管理员权限。

有关配置机器人活动选项的更多信息，请参阅[Marketo Engage文档](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/email-setup/filtering-email-bot-activity#select-filter-type){target="_blank"}。
