---
title: Web渠道配置
description: 了解如何在Journey Optimizer B2B edition中配置Web渠道设置以定义Web属性和页面匹配规则以进行内容交付。
feature: Setup, Channels
role: Admin
badgeBeta: label="Beta 版" type="informative" tooltip="此功能当前为有限测试版"
source-git-commit: 2f9b007df233cf8a233c3646bf691b7cff139f86
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Web渠道配置

Web配置是由交付内容的URL标识的Web属性。 它可以匹配单个页面URL或多个页面，以便Web体验可以跨一个或多个网页进行修改。 营销人员需要这些配置来[在历程中添加Web个性化操作节点](../content/web-experiences.md#create-a-web-experience)和[为营销活动设计体验修改](../content/web-experience-design.md)。

>[!BEGINSHADEBOX]

**先决条件**

要使用Web渠道，您的网站必须实施[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/collection/js/js-overview) (`alloy.js`)，以便进行访客识别和内容交付。 确保Adobe Experience Platform Web SDK的版本为2.16或更高版本。

Journey Optimizer B2B edition中的Web渠道配置需要以下[权限](../admin/user-management.md#b2b-product-permissions)：

* _[!UICONTROL 渠道配置]_ > _[!UICONTROL 管理消息预设]_ — 创建、更新和删除Web渠道配置所必需的。
* _[!UICONTROL 渠道配置]_ > _[!UICONTROL 查看消息预设]_ — 查看Web渠道配置所需。

>[!ENDSHADEBOX]

## 创建Web渠道配置

1. 在左侧导航中，转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**。

1. 在导航面板中的&#x200B;_[!UICONTROL Web]_&#x200B;下，选择&#x200B;**[!UICONTROL 渠道配置]**。

   ![访问Web渠道配置](./assets/config-web-channels.png){width="800" zoomable="yes"}

1. 单击右上方的&#x200B;**[!UICONTROL 创建渠道配置]**。

1. 输入配置的&#x200B;**[!UICONTROL Name]**（必需）和&#x200B;**[!UICONTROL Description]**（可选）。

   >[!NOTE]
   >
   >名称必须以字母(A-Z)开头，并且只能包含字母数字字符。 您还可以使用下划线`_`、点`.`和连字符`-`字符。

1. 在&#x200B;**[!UICONTROL Web设置]**&#x200B;部分中，选择以下选项之一：

   * **[!UICONTROL 单页]** — 如果要将更改仅应用于单个页面，请输入或选择&#x200B;**[!UICONTROL 页面URL]**。

     ![为单页Web渠道配置选择页面URL](./assets/config-web-channel-create-single-page.png){width="600" zoomable="yes"}

   * **[!UICONTROL 页面匹配规则]** — 若要定位多个匹配同一规则的URL，请构建一个匹配规则[的](#build-a-pages-matching-rule)页面，并输入&#x200B;**[!UICONTROL 默认创作和预览URL]**。

1. 单击&#x200B;**[!UICONTROL 提交]**&#x200B;以保存更改。

保存配置后，该配置处于&#x200B;_草稿_&#x200B;状态，可供营销人员在历程中使用Web渠道时使用。 只要配置仍处于草稿状态，您就可以继续编辑配置。 您还可以通过单击名称旁边的&#x200B;_更多_&#x200B;图标(**...**)并选择&#x200B;**[!UICONTROL 删除]**&#x200B;来删除草稿Web渠道配置。

在历程中使用Web渠道后，它立即变为&#x200B;_活动_&#x200B;状态。 在此状态下，可以编辑配置的名称和说明。 您无法更改Web设置或删除配置。

## 页面匹配规则 {#pages-matching-rule}

创建Web配置时，您可以生成与规则&#x200B;_[!UICONTROL 匹配的]_&#x200B;页面，以定位多个与同一规则匹配的URL。 这些规则允许您在多个页面中应用相同的内容更改。

例如，您可能希望将更改应用于整个网站的主页横幅，或添加在所有产品页面上显示的顶部图像。

### 构建规则

1. 当您[创建Web渠道配置](#create-a-web-channel-configuration)时，请选择&#x200B;**[!UICONTROL 页面匹配规则]**。

1. 使用每个部分中的不同运算符定义&#x200B;**[!UICONTROL 域]**&#x200B;和&#x200B;**[!UICONTROL 页面]**&#x200B;字段的条件以生成规则。

   +++域运算符

   根据您输入的字符串值，使用以下运算符匹配域：

   | 操作员 | 描述 | 示例 |
   | --- | --- | --- |
   | [!UICONTROL 等于] | 域的完全匹配。 | |
   | [!UICONTROL 开始于] | 匹配以输入字符串开头的所有域（包括子域）。 | `Starts with: dev`匹配所有以`dev`开头的域和子域，如`dev.example.com`、`dev.products.example.com`和`developer.example.com` |
   | [!UICONTROL 结束于] | 匹配以输入字符串结尾的所有域（包括子域）。 | `Ends with: example.com`匹配所有以`example.com`结尾的域和子域，如`stage.example.com`、`prod.example.com`和`myexample.com` |
   | [!UICONTROL 通配符匹配] | 允许您在字符串中间定义通配符匹配，如`dev.*.example.com`。 当运算符为&#x200B;_通配符匹配_&#x200B;时，验证规则要求值仅包含一个通配符（星号）。 | `Wildcard matching: dev.*.example.com`与域（如`dev.products.example.com`、`dev.mytest.products.example.com`和`dev.blog.example.com`）匹配 |
   | [!UICONTROL 任何] | 匹配所有域。 在跨域测试特定路径时，此插件非常有用。 | |

   +++

   +++路径运算符

   根据您输入的字符串值，使用以下运算符匹配路径：

   | 操作员 | 描述 | 示例 |
   | --- | --- | --- |
   | [!UICONTROL 等于] | 路径完全匹配。 | |
   | [!UICONTROL 开始于] | 匹配以字符串开头的所有路径（包括子路径）。 | |
   | [!UICONTROL 结束于] | 匹配以字符串结尾的所有路径（包括子路径）。 | |
   | [!UICONTROL 任何] | 匹配所有路径。 当定位一个或多个域下的所有路径时，此插件非常有用。 | |
   | [!UICONTROL 通配符匹配] | 允许您在路径中定义内部通配符，如`/products/*/detail`。 路径组件中的通配符`*`与前`/`个字符之前的任意字符序列匹配。  和`/*/`匹配任意字符序列（包括子路径）。 | `Wildcard matching: /products/*/detail`匹配路径，如`example.com/products/yoga/detail`、`example.com/products/surf/detail`、`example.com/products/tennis/detail`和`example.com/products/yoga/pants/detail` |
   | [!UICONTROL 包含] | 该值将转换为通配符，如`*mystring*`，并匹配包含字符序列的所有路径。 | `Contains: product`匹配包含字符串`product`的所有路径，如`example.com/products`、`example.com/yoga/perfproduct`、`example.com/surf/productdescription`和`example.com/home/product/page` |

   +++

   例如，要支持&#x200B;_Bodea_&#x200B;网站的所有&#x200B;_LumaSecure_&#x200B;解决方案页面上的内容更改，请选择&#x200B;**[!UICONTROL 域]** > **[!UICONTROL 开头为]** > `bodea`和&#x200B;**[!UICONTROL 页面]** > **[!UICONTROL 包含]** > `lumasecure`。

   ![定义与Web渠道配置匹配的页面规则](./assets/config-web-channel-pages-matching-rules.png){width="600" zoomable="yes"}

1. 如果您的用例需要多个规则，请单击“添加其他页面规则”**&#x200B;**&#x200B;并重复上一步。

   * 您最多可以定义10个规则。

   * 在不同的规则之间使用&#x200B;**[!UICONTROL Or]**&#x200B;或&#x200B;**[!UICONTROL Exclude]**&#x200B;运算符。

     _[!UICONTROL Or]_&#x200B;是用于定义多个规则的默认运算符，可用于添加多个可匹配的条件定义。

     当与定义的规则匹配的某个页面不应被定位时，_[!UICONTROL 排除]_&#x200B;非常有用。 例如，您可以定位包含`bodea.com`但不包括博客页面（如`lumasecure`）的所有`bodea.com/blogs/lumasecure/latest-release`页面。

   ![页面匹配带有排除项的规则](./assets/config-web-channel-pages-matching-rules-exclude.png){width="600" zoomable="yes"}

1. 输入&#x200B;**[!UICONTROL 默认创作和预览URL]**。

   此步骤可确保规则生成或匹配的页面具有指定的URL，以便用于Web体验内容设计和预览。

## 复制Web渠道

您可以复制现有Web渠道配置并进行更改，以基于现有Web渠道创建新的Web渠道。 无法修改保存到库中的活动Web渠道配置。

1. 单击变体的&#x200B;_更多菜单_&#x200B;图标(**...**)，然后选择&#x200B;**[!UICONTROL 复制]**。

   ![单击更多nenu图标以复制现有Web渠道配置](./assets/config-web-channels-more-menu.png){width="450"}

   此操作创建一个名称后附加`_Copy_nnn`的重复Web渠道。

1. 单击重复的Web渠道的名称以编辑参数。

   * 更改名称和描述以匹配规则中的目的或项目。
   * 如果需要，请更改单页面URL。
   * 如果需要，请根据您的要求更改页面匹配规则。

1. 配置完成后，单击&#x200B;**[!UICONTROL 提交]**。
