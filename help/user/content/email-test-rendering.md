---
title: 测试电子邮件渲染
description: 使用Litmus集成跨桌面、移动设备和Web客户端测试电子邮件渲染，以确保Journey Optimizer B2B edition中的收件箱兼容性。
feature: Email Authoring, Integrations
level: Intermediate
role: User
exl-id: 26d87a56-6bd1-4d4a-8090-71f5b0a7e9f8
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: cad51180-f8ce-4cb7-aefc-437847b5d6d6
autotag-review: 2026-03-30T22:28:13.343Z
TQID: https://experienceleague.adobe.com/G9c2TdbEje4HgE82tKURAn-UYz5wB-9iLsT9805m1JI
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 2%

---

# 使用 Litmus 测试电子邮件渲染效果

要测试电子邮件，您可以利用Journey Optimizer B2B edition中的[Litmus](https://www.litmus.com/email-testing){target="_blank"}企业帐户。 利用此集成，您可以预览电子邮件在常用电子邮件客户端中的渲染方式。 此工具可帮助您确保您的电子邮件内容在各种收件箱中都具有美观的显示效果并正常工作。

>[!AVAILABILITY]
>
>此集成仅适用于具有Litmus Enterprise帐户的Journey Optimizer B2B edition用户。 有关详细信息，请参阅Litmus网站[&#128279;](https://www.litmus.com/solutions/esp/adobe-journey-optimizer){target="_blank"}上的解决方案页面。

1. 当您的电子邮件设计完成并准备好进行测试时，请在电子邮件设计空间单击&#x200B;**[!UICONTROL 模拟内容]**。

1. 单击右上方的&#x200B;**[!UICONTROL 渲染电子邮件]**。

   ![呈现电子邮件按钮](./assets/email-simulate-render-button.png){width="700" zoomable="yes"}

   如果您尚未从Journey Optimizer B2B edition连接到Litmus帐户，则显示的页面将提供一个选项，可用于启动试用帐户或连接到您的现有帐户。

1. 单击右上方的&#x200B;**[!UICONTROL 连接您的Litmus帐户]**，或者使用页面内的链接。

   ![连接您的Litmus帐户](./assets/email-simulate-render-litmus-connect.png){width="700" zoomable="yes"}

1. 输入您的Litmus帐户凭据，然后单击&#x200B;**[!UICONTROL 登录]**。

1. 单击&#x200B;**[!UICONTROL 连接]**&#x200B;以确认Litmus与Journey Optimizer B2B edition之间的连接并发送用于渲染的电子邮件内容。

   >[!IMPORTANT]
   >
   >将Litmus帐户与Journey Optimizer B2B edition连接后，您同意将测试消息发送至Litmus。 然后，此内容将在Litmus中进行管理，而不是在Adobe中进行管理。 因此， Litmus数据保留电子邮件策略适用于这些电子邮件，包括可能包含在测试消息中的个性化数据。

1. 单击右上方的&#x200B;**[!UICONTROL 运行测试]**&#x200B;以生成电子邮件预览。

   ![运行Litmus渲染测试](./assets/email-simulate-render-litmus-run-test.png){width="700" zoomable="yes"}

1. 在常用的桌面、移动和基于Web的客户端中查看您的电子邮件内容。

   单击显示的缩略图可查看任何渲染的客户端测试的详细信息。

   ![Litmus电子邮件预览](./assets/email-simulate-render-litmus-previews.png){width="700" zoomable="yes"}

1. 完成审阅后，单击左上角的向后箭头（![显示或隐藏过滤器图标](../../assets/do-not-localize/icon_back-arrow.svg) ）以返回到“模拟内容”页面。

   您可以选择另一个配置文件并执行另一个渲染测试，或返回电子邮件设计空间根据您的审核做出任何所需的调整。
