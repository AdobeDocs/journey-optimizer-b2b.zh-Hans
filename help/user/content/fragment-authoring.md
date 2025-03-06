---
title: 片段创作
description: 了解如何创作可重复用于您的电子邮件的内容片段和模板设计以提高效率并维护设计和品牌标准。
feature: Content
source-git-commit: 1f551b636ef347fd65aa39a809dedba8372c3ac4
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 14%

---

# 片段创作

在[创建片段](./fragments.md#create-fragments)之后，使用可视编辑器在片段中创作结构和内容组件。

## 添加结构和内容 {#design-fragment}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="添加结构组件"
>abstract="结构组件定义片段的版面。拖放&#x200B;**结构**&#x200B;组件到画布中，开始设计您的片段内容。"

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="关于内容组件"
>abstract="内容组件是空的内容占位符，您可用它来创建片段的版面。"

{{$include /help/_includes/content-design-components.md}}

## 添加资源

{{$include /help/_includes/content-design-assets.md}}

## 导航图层、设置和样式

{{$include /help/_includes/content-design-navigation.md}}

## 使内容个性化

{{$include /help/_includes/content-design-personalization.md}}

## 启用自定义字段

当电子邮件或电子邮件模板作者添加片段时，片段内容默认处于锁定状态。 对已发布片段所做的任何更改都会自动传播到使用该片段的所有内容资产。 当您将片段中组件的参数指定为可编辑时，电子邮件或模板作者可以指定特定于其需求的自定义字段值。 此自定义标记仅限用于图像、文本和按钮可视组件。

例如，如果您设计的可重用横幅包括可单击按钮，则可以将该按钮的URL参数指定为可编辑。 然后，电子邮件作者可以使用更特定于其电子邮件促销活动的URL。 借助这些可自定义的字段，营销人员可以管理和个性化内容，而无需创建全新的内容块或中断从原始片段继承的更新。

1. 在可视内容编辑器中，选择要启用自定义的图像、文本或按钮元素。

1. 在右侧的组件详细信息中，选择&#x200B;**[!UICONTROL 可编辑字段]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 启用版本]**&#x200B;选项切换并设置可编辑的字段。

   ![为片段图像组件启用可编辑字段](./assets/fragment-editable-fields-image.png){width="700" zoomable="yes"}

   您可以为显示的字段启用自定义设置，具体取决于组件类型和片段中定义的参数。

   对于要允许自定义的每个字段，将切换开关更改为启用状态。

1. 单击&#x200B;**[!UICONTROL 概述]**&#x200B;查看所有可编辑的字段及其默认值。

   ![查看可编辑的字段及其默认值](./assets/fragment-editable-fields-image-overview.png){width="700" zoomable="yes"}

1. 保存更改。

## 编辑链接的URL跟踪

{{$include /help/_includes/content-design-links.md}}
