---
title: 登陆页面
description: 在Journey Optimizer B2B Prime中创建、设计和发布人员历程的登陆页面 — 从头开始构建、导入HTML、添加表单、个性化内容以及通过电子邮件进行链接。
autotag-review: '2026-06-12T22:53:39.337Z'
TQID: 'https://experienceleague.adobe.com/BvtB0i5CzlVutPA6HAzZy-Gfymw7ppZwthyBauyciLc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: a96755d6-1f54-4f3f-a971-d31f83705ab7id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 1461
ht-degree: 6%

---

# 登陆页面

登陆页面是一个独立的网页，您可以在联系人和客户单击电子邮件、短信消息或任何数字位置中的链接项目后指引他们。 您可以将这些页面合并到您的帐户历程中，以使您的潜在客户和客户在Web上查看您的消息，并在您的帐户历程中前进。 您可以在登陆页面可视设计空间中创建、个性化和预览登陆页面。

登陆页面的常见用例：

* 提供选择加入或选择退出营销通信或特定服务。 在电子邮件或其他通信中使用指向目标列表的链接。
* 在发送通信之前收集同意，并在选择加入或选择退出时发送确认电子邮件。
* 使用登陆页面上的表单捕获或更新用户档案数据（渐进式用户档案、偏好设置、注册和类似方案）。
* 将人员引导至为您的历程编排设计的特定于促销活动的信息。
* 将用户重定向到专用的Web表单，而无需在Journey Optimizer B2B Prime之外构建外部页面。

<!-- 
## Landing page workflow

To direct members of a journey audience to a defined web page when they click a specific link, create a landing page in Journey Optimizer B2B Edition: 


1. [Create the page](./landing-pages-create-publish.md) - Select a preset, set up the primary page, and add any required subpages.
1. [Design the landing page content](./landing-page-design.md) - Build the page content using drag-and-drop visual design components.
1. [Test and publish the landing page](./landing-pages-create-publish.md) - Preview the page, test form behavior, and then publish to make it live.
1. [Link to the page from your journey](#link-to-a-landing-page) - Add the landing page URL to an email, SMS, or journey action so that recipients can reach it.


For example, you can create and design landing pages to direct your users to online information. The page could include a form where they can opt in or opt out from receiving your communications. Or it could be an opportunity to subscribe to a recurring communications, such as a newsletter. 

You can create, personalize, and preview landing pages in the visual design space.
-->
## 访问和管理登陆页面

要在Journey Optimizer B2B Prime中访问登陆页面，请转到左侧导航并单击&#x200B;**[!UICONTROL 内容管理]** > **[!UICONTROL 登陆页面]**。 此操作显示实例中创建的所有登陆页面的列表。

该列表按&#x200B;_[!UICONTROL 修改时间]_&#x200B;列排序，最近更新的项目位于顶部。 单击列标题可在升序和降序之间更改。

### 筛选登陆页面列表

要按名称搜索登陆页面，请在搜索栏中输入匹配项的文本字符串。 单击&#x200B;_筛选器_&#x200B;图标<!-- ( ![Show or hide filters icon](../assets/do-not-localize/icon-filter.svg) ) -->以显示可用的筛选器选项，并更改设置以根据指定的条件筛选显示的项。

![筛选显示的登陆页面](./assets/landing-pages-list-filtered.png){width="800" zoomable="yes"}

<!-- 
This is going away? ### Customize the column display

Customize the columns that you want to display in the table by clicking the _Customize table_ icon ( ![Customize table icon](../assets/do-not-localize/icon-column-settings.svg) ) at the top right. 

In the dialog, select the columns to display and click **[!UICONTROL Apply]**.

![Select the columns that you want to display](./assets/landing-pages-customize-table-dialog.png){width="300"} 
-->

### 登陆页面状态和生命周期

登陆页面状态决定了在电子邮件和短信内容中进行链接的可用性，以及您可以对登陆页面进行的更改。

| 状态 | 描述 |
| -------------------- | ----------- |
| 草稿 | 创建登陆页面时，该页面处于草稿状态。 在您定义或编辑可视内容时，它保持此状态，直到您将其发布为托管页面。 可用操作： <br/><ul><li>编辑名称或描述<li>编辑链接URL<li>在可视设计空间中编辑<li>发布<li>重复<li>删除 |
| 发布日期 | 发布登陆页面时，该页面托管在Journey Optimizer B2B Prime实例上，可供在电子邮件或短信消息内容中进行链接。 可用操作： <br/><ul><li>编辑名称或描述<li>编辑链接URL<li>在电子邮件或短信消息内容中添加链接<li>创建草稿版本<li>重复<li>删除 |
| 以草稿发布 | 从已发布的登陆页面创建草稿时，已发布的版本会保留，并且草稿内容可以在可视设计空间中修改。 如果您发布草稿版本，则该草稿版本会替换当前已发布的版本，并且托管页面中的内容会更新。 可用操作： <br/><ul><li>编辑名称或描述<li>编辑链接URL<li>在电子邮件或短信消息内容中添加链接<li>在可视设计空间中编辑草稿版本<li>发布草稿版本<li>重复<li>删除（删除两个版本）<li>放弃草稿（返回到已发布状态） |

<!-- ![Landing page status lifecycle](./assets/status-lifecycle-diagram.png){zoomable="yes"} -->

## 创建登陆页面 {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_create"
>title="定义和配置您的登陆页面"
>abstract="要创建登陆页面，您需要选择一个预设，然后配置主要页面和子页面，最后在发布之前测试您的页面。"

待定

## 配置主要页面 {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_primary_page"
>title="定义主要页面设置"
>abstract="定义主页面，当收件人单击登陆页面链接（如来自电子邮件或网站的链接）时，将立即显示该主页面。"

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_access_settings"
>title="定义登陆页面 URL"
>abstract="在此部分中，定义一个唯一的登陆页面 URL。 URL的第一部分要求您之前将登陆页面子域设置为您选择的预设的一部分。"

待定

## 测试登陆页面 {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_preview_lp_profiles"
>title="预览和测试登陆页面"
>abstract="定义登陆页面设置和内容后，请使用测试配置文件预览页面。"

待定

## 编辑登陆页面

对登陆页面的编辑取决于其当前状态：

* 当登陆页面处于&#x200B;**_草稿_**&#x200B;状态时，您可以编辑其任何详细信息、URL和可视内容。
* 当登陆页面处于&#x200B;**_已发布_**&#x200B;状态时，您可以编辑描述，但不能编辑名称。 要更改可视内容，您必须创建页面的草稿版本。
* 当登陆页面处于&#x200B;**_已发布，状态为_**&#x200B;草稿时，编辑详细信息仅限于描述。 您还可以编辑草稿版本的可视内容。

>[!BEGINTABS]

>[!TAB 草稿]

1. 从&#x200B;_[!UICONTROL 登陆页面]_&#x200B;列表页面中，单击登陆页面名称以将其打开。

   此时将显示可视化内容的预览，其中登陆页面的详细信息位于右侧。

1. 修改任何详细信息，如名称和描述。

   <!-- ![Details for landing page with Draft status](./assets/landing-page-draft-details.png){width="700" zoomable="yes"} -->

1. 若要更改可视化设计空间中的内容，请单击&#x200B;**[!UICONTROL 编辑登陆页面]**。

   <!-- 
   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)
   -->

1. 单击&#x200B;**[!UICONTROL 保存]**，或单击&#x200B;**[!UICONTROL 保存并关闭]**&#x200B;以返回登陆页面的详细信息。

1. 当页面符合您的条件并且您想要显示时，请单击&#x200B;**[!UICONTROL 发布]**。

>[!TAB 已发布]

1. 从&#x200B;_[!UICONTROL 登陆页面]_&#x200B;列表页面，单击页面名称以将其打开。

   此时将显示可视化内容的预览，其中登陆页面的详细信息位于右侧。

1. 如果需要，请修改说明。

   对于已发布的登陆页面，无法更改所有其他详细信息。

1. 如果要更新内容，请单击右侧的&#x200B;**[!UICONTROL 编辑登陆页面]**。

   在对话框中单击&#x200B;**[!UICONTROL 创建草稿版本]**&#x200B;以在可视设计空间中打开草稿版本。

   <!-- 
   ![Create draft version dialog](./assets/landing-page-create-draft-version.png){width="300"} 

   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)
   -->

1. 单击&#x200B;**[!UICONTROL 保存]**，或单击&#x200B;**[!UICONTROL 保存并关闭]**&#x200B;以返回登陆页面的详细信息。

1. 当草稿登陆页面符合您的条件并且您希望在已发布的页面上提供更改时，单击&#x200B;**[!UICONTROL 发布]**。

   发布草稿版本时，草稿版本会替换当前已发布的版本，并且页面URL的内容会更新。

>[!TAB 已发布草稿]

打开登陆页面时，将显示草稿版本。 预览空间顶部的选项卡允许您在已发布版本和草稿版本之间切换显示。 草稿操作和详细信息将显示在右侧。

<!-- ![Preview and details for the landing page draft version](./assets/landing-page-published-draft-details.png){width="700" zoomable="yes"} -->

要更新内容，请执行以下操作：

1. 单击右上方的&#x200B;**[!UICONTROL 编辑登陆页面]**。

   <!--

   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)

   -->

1. 单击&#x200B;**[!UICONTROL 保存]**，或单击&#x200B;**[!UICONTROL 保存并关闭]**&#x200B;以返回登陆页面的详细信息。

1. 当草稿页面符合您的条件并且您想要使更改可用时，单击&#x200B;**[!UICONTROL 发布]**。

   发布草稿版本时，草稿版本会替换当前已发布的版本，并且托管页面中的内容会更新。

>[!ENDTABS]

## 复制登陆页面

您可以使用以下任一方法复制登陆页面：

* 从&#x200B;_[!UICONTROL 登陆页面]_&#x200B;列表页面，单击&#x200B;_更多_&#x200B;图标(**...**) 在登陆页面名称旁边，然后选择&#x200B;**[!UICONTROL 复制]**。
* 在登陆页面详细信息页面的右上角，单击&#x200B;**[!UICONTROL ...更多]**&#x200B;并选择&#x200B;**[!UICONTROL 复制]**。

<!-- ![Duplicate the landing page](./assets/landing-page-details-duplicate-delete.png){width="600" zoomable="yes"} -->

在对话框中，输入有用的名称（唯一）和描述（可选）。 单击&#x200B;**[!UICONTROL 复制]**&#x200B;以完成操作。

<!-- ![Enter a name and description for the duplicated landing page](./assets/landing-page-duplicate-dialog.png){width="350"} -->

然后，重复的（新）页面出现在&#x200B;_登陆页面_&#x200B;列表中。

## 删除登陆页面

您可以使用以下任一方法删除登陆页面：

* 从&#x200B;_[!UICONTROL 登陆页面]_&#x200B;列表页面，单击&#x200B;_更多_&#x200B;图标(**...**) 在登陆页面名称旁边，然后选择&#x200B;**[!UICONTROL 删除]**。
* 在登陆页面详细信息页面的右上角，单击&#x200B;**[!UICONTROL ...更多]**&#x200B;并选择&#x200B;**[!UICONTROL 删除]**。

此操作将打开确认对话框。 您可以通过单击&#x200B;**[!UICONTROL 取消]**&#x200B;或单击&#x200B;**[!UICONTROL 删除]**&#x200B;确认删除来中止该进程。

<!-- ![Delete landing page dialog](./assets/landing-page-delete-dialog.png){width="400"} -->

## 链接到登陆页面

作为生成电子邮件、片段和页面内容的营销人员或创意人员，您可以嵌入指向在Journey Optimizer B2B Prime实例中创建的已发布（实时）登陆页面的链接。

1. 当您在片段、电子邮件、登陆页面或模板的可视设计空间中工作时，为链接选择文本摘录、按钮组件或图像组件。

   **[!UICONTROL 链接]**&#x200B;选项显示在右侧面板中。

1. 对于&#x200B;**[!UICONTROL Type]**&#x200B;选项，请选择&#x200B;**[!UICONTROL 登陆页面]**。

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-settings.png){width="700" zoomable="yes"} -->

1. 对于&#x200B;**[!UICONTROL 登陆页面]**&#x200B;选项，单击&#x200B;_选择页面_&#x200B;图标<!-- ( ![Show links icon](/help/assets/do-not-localize/icon-landing-page-select.svg) ) -->。

1. 在“选择登陆页面”对话框中，将&#x200B;**[!UICONTROL 登陆页面源]**&#x200B;设置为&#x200B;**[!UICONTROL Journey Optimizer B2B edition]**，从已发布的页面列表中选中该登陆页面的复选框，然后单击&#x200B;**[!UICONTROL 选择]**。

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-landing-page-select.png){width="600" zoomable="yes"} -->

1. 对于&#x200B;**[!UICONTROL Target]**&#x200B;选项，请选择链接目标行为：

   * **[!UICONTROL 无]** — 使用浏览器默认行为打开链接。
   * **[!UICONTROL 空白]** — 在新窗口或选项卡中打开链接。
   * **[!UICONTROL Self]** — 在同一帧中打开链接。
   * **[!UICONTROL 父项]** — 在父框架中打开链接。
   * **[!UICONTROL Top]** — 在窗口的整个正文中打开链接。

1. （仅限文本链接）如果要为链接的文本加下划线，请选中&#x200B;**[!UICONTROL 加下划线链接]**&#x200B;复选框。

   通过选择右侧面板中的&#x200B;**[!UICONTROL 样式]**&#x200B;选项卡，可以为链接文本设置其他样式，包括链接颜色。
