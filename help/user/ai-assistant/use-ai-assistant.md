---
title: 使用 AI 助手
description: 了解AI Assistant如何帮助您充分利用Journey Optimizer B2B edition功能。
feature: AI Assistant
level: Beginner
exl-id: 2d642c34-6f6d-4a0f-98c5-4b9ea1cdaa29
source-git-commit: d19ed2bbe850a14cb0563f6e3563cd8f1c8d3226
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# 在Journey Optimizer B2B edition中使用AI助手

在Journey Optimizer B2B edition中，AI Assistant是一项用户界面功能，可用于了解产品概念、快速导航和了解Journey Optimizer B2B edition功能，以及获取您特定环境的操作见解。 Adobe Experience Cloud的多个产品中也提供了此功能。

>[!IMPORTANT]
>
>在使用AI助手之前，需要先签署Adobe Experience Cloud创作AI用户指南协议。 有关此协议和使用准则的更多信息，请参阅[Adobe Experience Cloud Generative AI用户准则](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)。

要访问AI助手，请单击标题中的图标。 AI助手将在右侧的面板中打开。

![单击图标以访问AI助手](./assets/ai-assistant-icon-displayed.png){width="420" zoomable="yes"}

此时将显示AI Assistant界面，它立即为您提供开始使用的信息。 您可以使用&#x200B;_构思下提供的选项开始_&#x200B;并回答问题和命令，例如：

* 发布了我的哪些帐户历程？
* 产生了哪些解决方案兴趣？
* 告诉我Journey Optimizer B2B edition的主要优势。

在Adobe Journey Optimizer B2B edition中，AI Assistant支持以下用例：

## 产品知识

产品知识问题与Journey Optimizer B2B edition概念有关，与Adobe Journey Optimizer的各个方面有关。 产品知识问题的一些示例包括：

* 如何设置短信提供商帐户？
* 如何在帐户历程中发送电子邮件？
* 如何个性化我的电子邮件内容？

要询问产品问题，请在面板底部的字段中输入该问题并按Enter键。

![在文本框中输入问题](./assets/ai-assistant-ask-question.png){width="420" zoomable="yes"}

您可以通过查看每个产品知识答案中可用的引文来验证AI Assistant返回的响应。

要查看引文并验证AI助理的响应，请选择&#x200B;**[!UICONTROL 显示源]**。

![来自AI Assistant查询的结果](./assets/ai-assistant-answer.png){width="420" zoomable="yes"}

AI Assistant会更新界面，并为您提供可证实初始响应的文档的链接。 此外，启用引用后，AI Assistant将更新响应以包含脚注，用于指示引用所提供文档的答案的特定部分。

使用向上或向下拇指对答案的质量进行评级。

## 运营见解

insight操作问题与组织沙盒中的旅程对象有关。 insight操作问题或提示的一些示例包括：

* Adobe Journey Optimizer B2B edition中有多少实时历程？
* 给我所有计划历程的列表
* 过去7天内创建了多少历程？

您必须处于AI助手的活动沙盒中，才能对关于您的操作见解的问题提供充分响应。

>[!NOTE]
>
>AI Assistant操作分析问题支持的唯一Adobe Journey Optimizer B2B edition对象在[操作分析域表](./ai-assistant-overview.md#operational-insights)中列出。 它只能访问您当前所在沙盒的数据。

<!-- Select to view an example of an operational insights question.

In the following example, AI Assistant receives the following query: _Show me dataflows that were created using the Amazon S3 source._

screen

AI Assistant responds with a table list of your dataflows and their corresponding IDs. Click the _Download_ icon ( Download icon ) to download the table as a CSV file. To view the entire table, click the _Expand_ icon ( Expand icon ).

screen

An expanded view of the table appears, providing you with a more comprehensive list of dataflows based on the parameters of your query.

screen

When prompted with an operational insights question, AI Assistant provides an explanation of how it computed the answer. In the following example, AI Assistant outlines the steps it took in order to identify the dataflows that were created using the Amazon S3 source.

screen

You can also provide filters and modifications to your questions, and you can instruct AI Assistant to render its findings based on the filters that you include. For example, you can ask AI Assistant to show you a trend of the count of segment definitions in the order of their created date, remove segment definitions with zero total profiles, and use month names instead of integers when displaying the data.

### Verify operational insights responses

You can verify each response related to operational insights questions using an SQL query that AI Assistant provides.

Select to view example of verifying operational insights responses

After receiving an answer for an operational insights question, click **[!UICONTROL Show sources]** and then select **[!UICONTROL View source query]**.

screen

When queried with an operational insights question, AI Assistant provides an SQL query that you can use to verify the process that it took to compute its answer. This source query is for verification purposes only and is not supported on Query Service.

screen  

 -->
