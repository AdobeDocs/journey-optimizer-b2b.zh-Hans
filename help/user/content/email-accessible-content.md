---
title: 设计可访问的内容
description: 了解如何在Journey Optimizer B2B edition中为您的电子邮件和登陆页面设计无障碍内容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 电子邮件、设计、辅助功能
source-git-commit: 09391f6d7c3360d0624edd7dae6c25a8616046d9
workflow-type: tm+mt
source-wordcount: '1645'
ht-degree: 0%

---

# 设计可访问的内容 {#accessible-content}

[欧洲无障碍法](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32019L0882){target="_blank"}是一项指令，旨在通过消除因成员国之间国家规则不同而造成的障碍，增强无障碍产品和服务的内部市场。

此法规规定，所有数字通信（包括电子邮件、新闻稿、PDF和可下载内容）都应可供访问。 因此，在为收件人创建内容时，您需要遵循特定准则，例如使用无障碍字体、可读格式并为图像提供替换文本。

通过[!DNL Journey Optimizer B2B Edition]设计工具，营销人员可以为&#x200B;**电子邮件**&#x200B;和&#x200B;**登陆页面**&#x200B;生成内容。 根据Web内容无障碍准则(WCAG) 2.1 （级别AA），使用这些工具遵守此指令。

以下部分概述了使用[!DNL Journey Optimizer B2B Edition]设计辅助功能内容的最佳实践。 此信息侧重于设计可供所有收件人访问的内容，以便残障人士能够阅读、理解您的电子邮件和登陆页面并与之交互。
 
## 确保文本可读性 {#text-readability}

利用&#x200B;**[!UICONTROL 文本]**&#x200B;组件的&#x200B;**[!UICONTROL 样式]**&#x200B;选项卡确保文本可读，例如使用适当的颜色对比度和简单字体。 有关文本组件样式设置的详细信息，请参阅[内容组件](content-components.md#text)

![文本组件“样式”选项卡显示字体、大小和颜色选项](assets/accessible-text-styles.png){width="700" zoomable="yes"}

对于字体和文本，请确保遵循以下准则：

### 字体选择

* 使用无衬线字体，如Arial、Verdana、Tahoma、Helvetica或Open Sans。
* 避免在正文内容中使用衬线、草稿或装饰性字体。
* 为了一致性和回退，请粘贴到有限的字体集（例如： `font-family: Arial, Helvetica, sans-serif;`）。

### 字体大小

* 确保正文的最小字体大小为16px。
* 为标题使用正确的层次结构。

### 颜色对比度

* 保持文本与背景之间的对比度至少为4.5:1。
* 对于大文本(≥24px或粗体18px)，请确保对比度至少为3:1。
* 避免在白色背景上使用浅灰色或淡色文本。
* 不要只依靠颜色来传达含义，而是要使用下划线、图标等。

### 文本辅助功能

* 避免在图像中使用文本。
* 请勿在正文中使用所有大写字母。
* 确保文本可以缩放到200%而不破坏布局。

## 确保可视辅助功能 {#visual-accessibility}

要确保您的内容能够以可视方式访问，请遵循以下最佳实践：

* 避免使用仅用于颜色指示器的重要信息。
* 请使用文本标签或图标以确保清晰明了。
* 针对移动和响应式布局优化您的设计，确保按钮较大且间距适当。
* 定期跨设备和屏幕大小测试以保持可访问性。

在[!DNL Journey Optimizer B2B Edition]中，可以使用Email Designer **[!UICONTROL 样式]**&#x200B;窗格中的样式参数和属性进一步细化内容中不同元素的大小和间距。

例如，您可以更新背景或更改边距、填充和对齐方式，以改善内容的可视访问性。

![样式窗格，带有背景、边距、填充和对齐设置](assets/accessible-styles.png){width="700" zoomable="yes"}

此外，[!DNL Journey Optimizer B2B Edition]电子邮件Designer允许您预览和优化不同设备和屏幕大小的设计。 您可以随时&#x200B;**[!UICONTROL 切换到实时视图]**，以查看内容在各种设备大小上的呈现方式。

![显示桌面、平板电脑和移动设备预览选项的实时视图切换](assets/accessible-live-view.png){width="700" zoomable="yes"}

>[!CAUTION]
>
>实时视图是一个通用预览，用于比较呈现在各种设备大小中的外观。 最终渲染可能会因收件人的电子邮件客户端而异。

## 对图像使用替换文本 {#alt-text}

使用&#x200B;**[!UICONTROL 图像]**&#x200B;组件为图像提供替换文本。 有关图像组件设置的详细信息，请参阅[内容组件](content-components.md#image)

![突出显示替换文本字段的图像组件设置面板](assets/accessible-alt-text.png){width="700" zoomable="yes"}

要在数字产品中使用有效的替换文本，请遵循以下准则：

* 简洁而符合情境地描述图像的用途。
* 避免使用“图像……”等多余短语，并使用空替换文本作为装饰性图像。
* 对于具有意义的图标，提供有意义的标签；对于复杂的图像，使用简短的替换文本以及在其他位置使用更长的描述。

## 使用可读格式 {#readable-format}

使用Email Designer相关结构和[内容组件](content-components.md)，以及&#x200B;**[!UICONTROL 样式]**&#x200B;窗格中的选项，以清晰、逻辑和简洁的方式整理您的内容，使所有人都可以访问。

![向Designer发送电子邮件，显示有条理布局的结构和内容组件](assets/accessible-components.png){width="800" zoomable="yes"}

* 使用结构化、语义化的HTML，并带有适当的标题、段落、列表和表。
* 确保内容遵循从左至右、从上至下的逻辑流程。
* 使用简洁明了的语言。
* 为PDF和信息图形提供替代格式。
* 允许调整文本大小和重排，并确保在所有格式下均可使用足够的颜色对比度读取排版规则。

## 确保内容可读性 {#readability}

要阅读，您的内容必须清晰、结构合理，并且可供所有人使用，包括患有视觉、认知或阅读障碍的人以及使用辅助技术的人。 创建无障碍内容时要考虑的一些要点包括：

* 保持句子不超过20个词。
* 将副本编辑为直接指向点。
* 使用主动语态使句子结构更简单。
* 避免使用某些人可能不熟悉的俚语、行话或地区性用语。

要评估您的电子邮件可读性，请使用Microsoft Word中常用的[Flesch阅读简易测试](https://support.microsoft.com/en-us/office/get-your-document-s-readability-and-level-statistics-85b4969e-e80a-4777-8dd3-f7fc3c8b3fd2){target="_blank"}。 它按0-100的数值计算内容的读取难易程度。

## 测试您的内容 {#test}

要验证内容的辅助功能，您可以使用[!DNL Journey Optimizer B2B Edition]提供的测试功能。 它们并非专门用于检查您的内容是否完全可访问，但它们可以提供第一级别的验证。

* 使用测试配置文件预览内容。

* 使用[电子邮件渲染](email-test-rendering.md)选项，该选项可利用Litmus在主要电子邮件客户端(Apple Mail、Gmail、Outlook)间模拟您的设计，并查看文本、颜色和图像是否可以访问您的内容。<!--Litmus includes accessibility testing-->

* 在将内容发送到实际受众之前，请发送校样以测试内容的渲染。

![具有测试配置文件预览选项的内容模拟界面](assets/accessible-simulate.png){width="800" zoomable="yes"}

如果内容可可靠访问，要以更一致的方式签入，请访问特定的外部工具，例如：

* [WebAim对比度检查器](https://webaim.org/resources/contrastchecker/){target="_blank"}和[WAVE Web辅助功能评估工具](https://wave.webaim.org/){target="_blank"}用于评估对比度和符合性；

* 屏幕阅读器等辅助技术(例如：[NVDA](https://www.nvaccess.org/download/){target="_blank"}或iPhone上的[VoiceOver](https://support.apple.com/en-ie/guide/iphone/iph3e2e415f/ios){target="_blank"})可从视障用户的角度体验电子邮件。

## 使用深色模式 {#dark-mode}


深色模式增强了对光线敏感或视觉障碍的用户的可视访问性，从而改善了观看体验。

![比较浅色模式和深色模式渲染的电子邮件预览](assets/accessible-dark-mode.png){width="800" zoomable="yes"}

针对深色模式进行设计时，请使用透明的PNG或SVG图像，并设置相应的元标记和CSS。 如果不支持深色模式，请提供可访问的回退样式。 最后，在浅色和深色模式下测试所有电子邮件内容和UI元素。

## 使用特定属性进行辅助功能 {#attributes}

### 语言属性 {#language}

创建设计时，请在内容正文中包含`lang`（语言）和`dir`（文本方向）属性。 这些属性可帮助辅助技术（如屏幕阅读器）以适当的方式解释和展示您的内容。

* `lang`属性指示发送给辅助技术的电子邮件的语言，确保单词的发音正确。

  +++示例

  英语示例：

  ```
  <body lang="en">
  ```

  法语示例：

  ```
  <body lang="fr">
  ```

  +++

* `dir`属性指定文本方向。 大多数语言，包括英语和法语，从左至右(ltr)阅读，而阿拉伯语和希伯来语等语言从右至左(rtl)阅读。

  +++示例

  英语示例（从左至右）：

  ```html
  <body lang="en" dir="ltr">
  ```

  阿拉伯语示例（从右至左）：

  ```html
  <body lang="ar" dir="rtl">
  ```

  +++

屏幕阅读器依赖`lang`属性来应用正确的发音规则。 文本方向可确保内容自然地以从左至右或从右至左的语言流动。 如果没有这些属性，用户可能会遇到阅读顺序混乱或发音错误的情况。 因此，请始终使用适当的`lang`和`dir`属性来封装电子邮件正文。

>[!TIP]
>
>如果电子邮件包含多种语言，请将相应的语言属性分配给特定部分（如`<table>`或`<td>`块），以确保每个部分均可正确读取。

### 表格 {#tables}

在HTML内容中，表格通常用于布局。 默认情况下，屏幕阅读器将每`<table>`视为数据表，声明行、列和结构。 如果表仅用于格式化，则此结构可能会混淆。

将`role="presentation"`（或`role="none"`）添加到布局表，以确保辅助型技术跳过其结构并仅关注实际内容。

+++示例 — 布局表（带`role="presentation"`）

```html
<table role="presentation" border="0" cellpadding="0" cellspacing="0" width="100%"> 
  <tr> 
    <td align="center"> 
      <h1>Hello World</h1> 
      <p>Welcome to our newsletter</p> 
    </td> 
  </tr> 
</table>
```

屏幕阅读器显示：
“你好，世界。 欢迎收看此新闻稿。” *（未提及行、列或表）*

+++

+++示例 — 数据表（不带`role="presentation"`）

```html
<table border="1" cellpadding="5" cellspacing="0"> 
  <tr> 
    <th scope="col">Name</th> 
    <th scope="col">Score</th> 
  </tr> 
  <tr> 
    <td>Alice</td> 
    <td>95</td> 
  </tr> 
  <tr> 
    <td>Bob</td> 
    <td>88</td> 
  </tr> 
</table> 
```

屏幕阅读器显示：
“带2列3行的表。”

“姓名，爱丽丝。 分数，95。”

“姓名，鲍勃。 分数，88。”

+++

>[!TIP]
>
>仅将`role="presentation"`用于布局表。 对于数据表，请保留语义`<table>`结构，以便屏幕阅读器可以正确声明标题和关系。

### 链接文本 {#links}

屏幕阅读器使用文本阅读链接。 如果链接仅标记为&#x200B;_单击此处_&#x200B;或&#x200B;_了解更多_，则使用辅助技术的用户不知道目标。 为确保辅助功能，他们需要清晰地指示目标或操作的描述性文本。

使用电子邮件Designer添加指向内容的链接并编辑标签，使其可见（可见）且具有描述性（清除用途）。 避免&#x200B;_此处_&#x200B;或&#x200B;_更多_&#x200B;之类的模糊标签。

![显示URL字段和描述性标签选项的链接设置面板](assets/accessible-link.png){width="600" zoomable="yes"}

+++示例 — 良好链接（描述性）： 

```
<p>Learn more in the  
<a href="https://adobe.com/release-notes">August release notes</a>. 
</p>
```

屏幕阅读器显示：
“Link， 8月发行说明。”

+++

+++示例 — 错误链接（非描述性）

```
<p>Learn more about our new features.  
  <a href="https://adobe.com/release-notes">Click here</a>. 
</p>
```

屏幕阅读器显示：
“链接，单击此处。” *（未提供顺序不正确的上下文）*

+++

## 提供键盘导航和焦点支持 {#keyboard}

<!--for landing pages-->

提供键盘导航和焦点支持使无法使用鼠标访问内容并与内容交互的用户能够访问。 它还通过为所有用户提供清晰、一致的信息浏览方式，提高了总体可用性。

* 通过键盘聚焦
   * 确保所有交互式元素（如按钮、复选框、链接）均具有`tabindex="0"`，以便它们按自然选项卡顺序包含。
   * 允许使用Tab键和箭头键(↑ ↓ ← →)进行导航，此时应会突出显示重点显示的元素。
* 自定义焦点样式
   * 应用清晰且可区分的样式来关注可操作元素：
     +++示例(CSS)

     ```
     [tabindex="0"] : focus { 
     outline: 2px solid #00AEEF;  /* Cyan border */ 
     background-color: #20CEFF;   /* Optional background */ 
     }
     ```

     +++

   * 确保焦点指标符合WCAG 2.2的焦点外观标准，包括：
      * 最小区域：2 CSS像素粗轮廓。
      * 聚焦状态和非聚焦状态之间的对比度：≥ 3:1。

* 键盘激活支持
   * 确保复选框和按钮与Enter和Space键相对应。
   * 仅使用键盘验证交互：
      * Enter或Space应该切换复选框。
      * Enter或Space应触发按钮。
