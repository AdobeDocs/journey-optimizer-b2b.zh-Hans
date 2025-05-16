---
title: 向历程添加电子邮件
description: 了解如何在Adobe Journey Optimizer B2B中添加、定义和优化电子邮件操作。 通过有针对性的电子邮件通信增强您的帐户历程。
feature: Email Authoring, Account Journeys
role: User
exl-id: 21a6ce0f-b59d-4be2-abc3-fda5c6a6334f
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 0%

---

# 向历程添加电子邮件

使用Adobe Journey Optimizer B2B edition通过帐户历程向客户发送电子邮件。 您可以选择在电子邮件设计空间创建、个性化和预览消息。 或者，您也可以选择发送已在连接的Marketo Engage实例中定义的电子邮件。

>[!NOTE]
>
>如果您是首次发送电子邮件，请确保已在Adobe Marketo Engage中配置电子邮件渠道。 若要了解详细信息，请参阅[跟踪和电子邮件传递的协议](../start/email-protocols.md)。

## 在历程中添加电子邮件操作节点

当您[添加&#x200B;_[!UICONTROL 执行操作]_&#x200B;节点](../journeys/action-nodes.md)并执行以下操作时，可以在历程中设置电子邮件投放：

1. 对于&#x200B;]_目标上的_[!UICONTROL &#x200B;操作，请选择&#x200B;**[!UICONTROL 人员]**。

1. 若要对人员&#x200B;]_执行_[!UICONTROL &#x200B;操作，请选择&#x200B;**[!UICONTROL 发送电子邮件]**。

1. 对于&#x200B;_[!UICONTROL 电子邮件源]_，选择您希望如何发送电子邮件。

   ![执行操作 — 发送电子邮件](assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * 选择&#x200B;**[!UICONTROL 创建新电子邮件]**&#x200B;以在Journey Optimizer B2B edition中以本机方式创作电子邮件。

     此选项允许您在Journey Optimizer B2B edition中以本机方式管理电子邮件内容。 单击&#x200B;**[!UICONTROL 创建电子邮件]**&#x200B;以打开&#x200B;_新建电子邮件_&#x200B;对话框。 您可以创建新的电子邮件内容资产<!-- or duplicate an existing email content asset-->。

     在对话框中，输入电子邮件的唯一&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 主题行]**，然后单击&#x200B;**[!UICONTROL 创建]**。

     ![新建电子邮件对话框 — 新建电子邮件](assets/create-new-email-no-duplicate.png){width="400"}

     在电子邮件内容页面的&#x200B;_[!UICONTROL 电子邮件属性]_&#x200B;部分中，_[!UICONTROL 发件人电子邮件]_&#x200B;和&#x200B;_[!UICONTROL 回复地址]_&#x200B;字段已配置。 您可以为&#x200B;_[!UICONTROL From name]_&#x200B;和&#x200B;_[!UICONTROL Description]_（可选）字段输入值。

     定义电子邮件[设置](#define-the-email-settings)并单击&#x200B;**[!UICONTROL 编辑电子邮件内容]**&#x200B;以[设计内容](./email-authoring.md)。

     <!-- +++New email {#new-email}
     When you want to create an email using an empty canvas or an email template, use the _[!UICONTROL New email]_ option. 

     1. In the dialog, choose **[!UICONTROL New email]**.

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - new email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

       In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. Click **[!UICONTROL Edit email]** to define the email [settings](#define-the-email-settings) and design the [content](./email-authoring.md).

     +++

     +++Duplicate existing email {#duplicate-email}
     When you want to create an email using an existing email from the current journey or from another journey, use the Duplicate existing journey option. You can make changes to the duplicated email according to your objective for the journey node.

     1. In the dialog, choose **[!UICONTROL Duplicate existing email]**.

     1. For **[!UICONTROL Existing email to duplicate]**, click the _Select email_ icon and select the email you want to duplicate and use for the journey node.

      You can filter the list of emails by entering a text string in the search field to match the email name.

      ![Select email](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

      Select the checkbox for the email that you want to duplicate and click **[!UICONTROL Select]**. 

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - duplciate existing email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

        In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. If needed, click **[!UICONTROL Edit email]** to modify the email [settings](#define-the-email-settings) and [content](./email-authoring.md).

     +++
   —>
   * 选择&#x200B;**[!UICONTROL 从Adobe Marketo Engage中选择电子邮件]**&#x200B;以使用Marketo Engage中预先编写的电子邮件之一，并将其作为历程的一部分发送。

     ![选择Marketo Engage电子邮件](./assets/email-select-marketo.png){width="500" zoomable="yes"}

     利用此选项，将设置节点，并且无需在历程中进一步定义电子邮件内容。

## 定义电子邮件设置

在右侧的&#x200B;_摘要_&#x200B;面板中选择&#x200B;**[!UICONTROL 详细信息]**&#x200B;选项卡后，滚动到底部以查看并设置电子邮件选项。

![电子邮件设置](./assets/email-summary-details-settings.png){width="600" zoomable="yes"}

| 选项 | 描述 |
| ------ | ----------- |
| [!UICONTROL 发件人姓名] | 电子邮件标头中使用的发件人名称。 输入您希望向收件人显示的发件人名称。 单击&#x200B;_个性化_&#x200B;图标（![个性化图标](../assets/do-not-localize/icon-personalize.svg)）以在字段中使用个性化令牌。 |
| [!UICONTROL 来自电子邮件] | 电子邮件标头中使用的发件人地址。 默认值是从[电子邮件渠道投放设置](../admin/configure-channels-emails.md#delivery-settings)中填充的。 单击&#x200B;_个性化_&#x200B;图标（![个性化图标](../assets/do-not-localize/icon-personalize.svg)）以在字段中使用个性化令牌。 |
| [!UICONTROL 回复地址] | 电子邮件标头中使用的发件人地址。 默认值是从[电子邮件渠道投放设置](../admin/configure-channels-emails.md#delivery-settings) （[!UICONTROL 来自标签]）中填充的。 输入当收件人使用回复功能时要填充的电子邮件地址（它可能与发件人地址不同或相同）。 单击&#x200B;_个性化_&#x200B;图标（![个性化图标](../assets/do-not-localize/icon-personalize.svg)）以在字段中使用个性化令牌。 |
| [!UICONTROL 主题行] | 电子邮件主题字段中显示的文本。 默认值由您在&#x200B;_[!UICONTROL 新建电子邮件]_&#x200B;对话框中输入的文本填充。 您可以根据需要更改文本。 单击&#x200B;_个性化_&#x200B;图标（![个性化图标](../assets/do-not-localize/icon-personalize.svg)）以在字段中使用个性化令牌。<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL 操作电子邮件] | 如果要将电子邮件指定为可操作的，请选中此复选框。 操作电子邮件从选择退出/取消订阅列表和通信限制中排除。 仅当收件人不能将电子邮件视为未经请求的商业邮件(SPAM)时，才选择此选项。 |
| [!UICONTROL 包括网页形式的视图] | 选中此复选框可包含指向从电子邮件内容生成的网页的链接。 与网页相比，电子邮件的功能更为有限，因此它对于JavaScript、扩展CSS和表单非常有用。 用于生成链接的文本已在[电子邮件渠道投放设置](../admin/configure-channels-emails.md#delivery-settings)中配置([!UICONTROL 以网页HTML查看]和[!UICONTROL 以网页文本查看])。 |
| [!UICONTROL 禁用打开跟踪] | 如果不想跟踪电子邮件打开活动，请选中复选框。 禁用此功能后，仅当具有独特身份的用户打开电子邮件时，电子邮件打开活动计数才会递增。 设计电子邮件正文内容时，您可以[管理电子邮件内容链接的跟踪](./email-authoring.md#content-authoring---link-tracking)。 |
| [!UICONTROL 预编译标头] | 选中此复选框可包含预编译标头。 邮件引文是简短摘要文本，在某些电子邮件客户端中，显示在主题行之后。 它通常提供电子邮件的简短摘要，通常是单句子。 在字段<!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content -->中输入摘要文本。 |
| [!UICONTROL 用作抄送地址的字段] | 如果可用，请选择最多25个在Marketo Engage中使用`Email`类型设置的潜在客户或公司字段。 |

## 检查警报

在设计电子邮件内容时，如果缺少关键设置，则会在界面（页面右上方）中显示警报。 如果未看到此按钮，则表示没有检测到问题。

![电子邮件通知](./assets/email-alerts.png){width="600" zoomable="yes"}

可以检测到两种类型的警报：

* 引用推荐和最佳实践的&#x200B;**_警告_**，例如：

   * `The opt-out link is not present in the email body`：最佳做法是在电子邮件正文中添加退订链接。

     >[!NOTE]
     >
     >营销风格的电子邮件必须包含选择退出链接，这对于事务型消息不是必需的。

   * `Text version of HTML is empty`：别忘了定义电子邮件正文的文本版本，此文本版本在HTML内容无法显示时使用。

   * `Empty link is present in email body`：检查电子邮件中的所有链接是否正确。

   * `Email size has exceeded the limit of 100KB`：要获得最佳投放，请确保电子邮件大小不超过100KB。

* **_错误_**，阻止您测试或激活历程/营销活动，只要未解决这些错误，例如：

   * `The subject line is missing`：电子邮件主题行是必填的。

   * `The email version of the message is empty`：尚未配置电子邮件内容时显示此错误。
