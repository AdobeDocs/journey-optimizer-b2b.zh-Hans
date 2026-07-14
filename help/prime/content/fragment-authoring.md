---
title: 片段创作
description: 在Journey Optimizer B2B Prime中，通过可视化设计工具创作可重用内容片段 — 为电子邮件和模板添加结构、资源、个性化、条件内容以及链接的URL跟踪。
badgeBeta: label="Beta 版" type="informative" tooltip="此功能属于有限测试版。"
autotag-review: '2026-07-13T16:38:09.506Z'
TQID: 'https://experienceleague.adobe.com/Zn5L6Bc3x8SuGyjOPDdTWI-oxrrhk06a2f8ZvX2SN4s'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: e1663313-7961-4100-bea9-fa9f4edf8493
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 5206ed7bc0ce24e65700da28b023d76c68cb6419
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 4%

---

# 片段创作

在您[创建片段](./fragments.md#create-fragments)后，请使用可视化设计空间在片段中创作结构和内容组件。

## 添加结构和内容 {#design-fragment}

{{$include /help/_includes/content-design-components-prime.md}}

## 添加资源 {#add-assets}

在可视设计空间中，选择左侧导航栏中的&#x200B;_Assets_ （![Assets图标](../../assets/do-not-localize/icon-assets-me.svg) ）图标以浏览和选择[!DNL Journey Optimizer B2B Prime]资源库中的图像资源。

有关选择、替换或上传图像资产的步骤，请参阅[使用资产进行内容创作](./digital-asset-management.md#assets-authoring)。

## 导航图层、设置和样式 {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

## 个性化内容 {#personalize-content}

[!DNL Journey Optimizer B2B Prime]使用Handlebars语法进行个性化。 在发送时，令牌会被替换为来自每个收件人的配置文件数据的值。

添加个性化&#x200B;:_(_T)

1. 选择文本组件，然后单击工具栏中的&#x200B;_添加个性化_ （ ![个性化图标](../../user/assets/do-not-localize/icon-personalize.svg) ）图标。
1. 在个性化对话框中，浏览左侧的架构树并选择配置文件属性。 编辑器插入相应的Handlebars表达式 — 例如，`{{profile.firstName}}`。
1. 如果需要，添加回退值以处理缺少的数据，例如`{{profile.firstName | default: "there"}}`。
1. 单击&#x200B;**[!UICONTROL 确认]**&#x200B;或&#x200B;**[!UICONTROL 插入]**。 表达式在字段中内联显示。

有关表达式编辑器工具和语法的详细信息，请参阅[Personalization编辑器](./personalization-expressions.md)。

## 编辑链接的URL跟踪 {#edit-linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}
