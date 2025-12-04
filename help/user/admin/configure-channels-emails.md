---
title: 电子邮件渠道配置
description: 配置电子邮件投放设置、通信限制和身份验证协议，以优化Journey Optimizer B2B edition中的投放能力。
feature: Setup, Channels
role: Admin
exl-id: fb16b5e5-f1a5-4e59-b8c6-56985f03225a
source-git-commit: cbd9117daffc3820196c1d8436af2a568e1140b7
workflow-type: tm+mt
source-wordcount: '1675'
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

此设置为连接的Marketo Engage实例中的一个或多个工作区定义主域。 新电子邮件使用此域作为默认域，但营销人员可以[基于每封电子邮件](../content/add-email.md#define-the-email-settings)覆盖此域。 有关定义默认品牌策略域的更多信息，请参阅[Marketo Engage文档](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/edit-your-default-branding-domain){target="_blank"}。

>[!NOTE]
>
>如果您要营销多个品牌，并且希望每个品牌都有自己的品牌跟踪链接，则可以添加额外的品牌推广域。 有关添加多个品牌化域的更多信息，请参阅[Marketo Engage文档](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/add-an-additional-branding-domain){target="_blank"}。

### [!UICONTROL 自定义标头选项] {#custom-header-options}

要查看自定义标题选项，请单击&#x200B;**[!UICONTROL 自定义标题选项]**&#x200B;选项卡。

![访问自定义标头选项](./assets/config-email-delivery-custom-header.png){width="700" zoomable="yes"}

启用&#x200B;_[!UICONTROL 严格传输安全]_&#x200B;后，它将保证通过HTTPS提供跟踪链接（仅适用于具有受SSL保护的跟踪链接的订阅）。

## 通信限制

通信限制控制联系人从您的组织收到的电子邮件数量。 您设置的限制在Journey Optimizer B2B edition和连接的Marketo Engage实例之间共享。 设置这些限制可确保某个潜在客户在给定时间段内收到的电子邮件数量不会超过最大数量。

>[!AVAILABILITY]
>
>通信限制适用于在[简化架构](../simplified-architecture.md)上配置的Journey Optimizer B2B edition环境。 请联系Adobe支持或打开支持工单以在Journey Optimizer B2B edition与一个或多个Marketo Engage实例之间共享通信限制。

例如，系统规定每天只能收到五封电子邮件，通过禁止第六封电子邮件，可确保某位联系人在一天内不会收到第六封电子邮件。 利用Journey Optimizer B2B edition和Marketo Engage之间的共享通信限制，可以在一个位置定义通信限制规则。 无论来自Journey Optimizer B2B edition或Marketo Engage的发送操作如何，都会禁止发送第六封电子邮件。

所有Marketo Engage生产实例默认定义了通信限制(有关详细信息，请参阅[Marketo Engage文档](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/enable-communication-limits){target="_blank"})。 要使用共享通信限制，请在Journey Optimizer B2B edition中定义规则，并将这些限制的共享扩展到Marketo Munchkin代码。

>[!IMPORTANT]
>
>要将通信规则集扩展到Marketo Munchkin代码，请联系您的Adobe客户管理团队。 此配置通常是载入流程的一部分。

若要查看或设置通信限制规则，请转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**。 在导航面板中的&#x200B;_[!UICONTROL 电子邮件]_&#x200B;下，选择&#x200B;**[!UICONTROL 通信限制]**。

![访问通信限制配置](./assets/config-email-communication-limits.png){width="700" zoomable="yes"}

默认情况下，有一个全局规则集，您可以在其中根据自己的要求定义、激活和停用多个规则。 单击规则集名称以显示规则列表。

### 创建规则

1. 单击右上方的&#x200B;**[!UICONTROL 创建规则]**。

   ![访问通信限制配置](./assets/config-email-communication-limits-create-rule-select.png){width="600" zoomable="yes"}

1. 输入&#x200B;**[!UICONTROL 规则名称]**。

1. 设置&#x200B;**[!UICONTROL 上限金额]**。

   输入值，或单击右侧的&#x200B;_向上_&#x200B;或&#x200B;_向下_&#x200B;箭头增加或减少值。

1. 根据您想要为限制定义时间周期的方式，选择&#x200B;**[!UICONTROL 重置上限频率]**&#x200B;值。

   您可以选择每小时&#x200B;_[!UICONTROL 、]_&#x200B;每日&#x200B;_[!UICONTROL 、]_&#x200B;每周&#x200B;_[!UICONTROL 或]_&#x200B;每月&#x200B;_[!UICONTROL 。]_

   ![访问通信限制配置](./assets/config-email-communication-limits-create-rule-settings.png){width="600" zoomable="yes"}

1. 根据周期中要包含的频率单位数设置&#x200B;**[!UICONTROL Every]**&#x200B;值。

   例如，如果您使用&#x200B;_每日_&#x200B;作为频率，并将此值设置为`3`，则周期定义为三天。

1. 单击右上方的&#x200B;**[!UICONTROL 创建规则]**。

新规则处于&#x200B;_草稿_&#x200B;状态，除非您选择激活它，否则不会应用于通信限制。

### 管理规则

只要规则处于&#x200B;_草稿_&#x200B;状态，您就可以编辑定义或删除规则。 当您希望应用规则时，可以激活它。 单击列表中草稿规则名称旁边的&#x200B;_更多菜单_ (***...***)图标，然后选择&#x200B;**[!UICONTROL 激活]**。

![单击草稿通信限制规则的“更多”菜单](./assets/config-email-communication-limits-draft-more-menu.png){width="400" zoomable="yes"}

然后，在确认对话框中单击&#x200B;**[!UICONTROL 激活]**。

无法编辑或删除活动规则，只能将其停用。 对于要从应用的通信限制中移除的活动规则，请单击活动规则名称旁边的&#x200B;_停用_ （![停用图标](../assets/do-not-localize/icon-deactivate.svg) ）图标。

![单击有效通信限制规则的“停用”图标](./assets/config-email-communication-limits-active-deactivate.png){width="400" zoomable="yes"}

然后，在确认对话框中单击&#x200B;**[!UICONTROL 停用]**。

该规则显示为&#x200B;_不活动_&#x200B;状态。 它类似于草稿规则，您可以根据需要编辑、删除或激活它。

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

当您的DNS记录中具有公钥，并且在连接的Marketo Engage实例中激活了发送域时，自定义DKIM签名将用于发送消息。 自定义DKIM签名包含加密的数字签名，其中包含在发送的每封电子邮件中。 然后，接收方可通过在发送域的DNS中查找&#x200B;_公钥_&#x200B;来解密数字签名。 如果电子邮件中的密钥与DNS记录中的密钥相对应，则接收邮件服务器更有可能接受通过Marketo Engage发送的电子邮件。

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

有关配置机器人活动选项的更多信息，请参阅[Marketo Engage文档](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/filtering-email-bot-activity#select-filter-type){target="_blank"}。
