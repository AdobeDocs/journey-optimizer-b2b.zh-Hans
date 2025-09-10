---
title: 使用 Experience Manager Assets
description: 在内容创作中访问和使用AEM Assets图像 — 在Journey Optimizer B2B edition中自动拖放、搜索、筛选和同步更改。
feature: Assets, Content, Integrations
role: User
exl-id: c6864981-209c-4123-8d3f-24deb07026a0
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 2%

---

# 使用Experience Manager资源

当[!DNL Adobe Experience Manager Assets as a Cloud Service]与[!DNL Adobe Journey Optimizer B2B Edition]集成时，您可以轻松地发现和访问数字资产，以便在营销内容中使用。 在创作内容时，可从左侧导航栏中的&#x200B;_[!UICONTROL Experience Manager Assets]_&#x200B;项访问资源，以及在创作帐户历程的电子邮件内容时也可访问资源。

{{aem-assets-licensing-note}}

当您使用这些数字资产时，[!DNL Assets as a Cloud Service]中的最新更改会自动通过链接的引用传播到实时电子邮件营销活动。 如果在[!DNL Adobe Experience Manager Assets as a Cloud Service]中删除了图像，则这些图像在电子邮件中显示时带有损坏的引用。 当帐户历程中当前使用的资产被修改或删除时，历程作者会收到有关图像更改和使用图像的历程列表的通知。 对资源的所有更改必须在[!DNL Adobe Experience Manager Assets]中央存储库中完成。

当您的环境有一个或多个[Assets存储库连接](../admin/configure-aem-repositories.md)时，内容作者在创建电子邮件、电子邮件模板或可视化片段时可以使用[!DNL Experience Manager Assets]作为资源的来源。

>[!IMPORTANT]
>
>管理员必须将需要访问Assets的用户添加到Assets Consumer Users或/和Assets Users产品配置文件。 [了解详情](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console){target="_blank"}

## 访问AEM Assets图像

在内容设计空间中，单击左侧边栏中的&#x200B;_[!UICONTROL Experience Manager Assets]_ (![Experience Manager Assets图标](../../assets/do-not-localize/icon-assets-aem.svg) )图标。 这会将“工具”面板更改为选定存储库中可用资源的列表。

![单击Assets选择器图标可访问图像资源](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

>[!NOTE]
>
>当前，[!DNL Adobe Experience Manager Assets]仅支持[!DNL Adobe Journey Optimizer B2B Edition]中的图像资源。 必须在[!DNL Adobe Experience Manager Assets]中央存储库中更改资源。 [了解详情](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets){target="_blank"}

### 更改显示的存储库

如果您有多个连接的AEM存储库，请单击&#x200B;**[!UICONTROL 存储库]**&#x200B;的菜单箭头以选择要在左侧面板中显示的存储库。

![选择AEM Assets存储库以访问图像资源](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

有多种方法可以将图像资产添加到可视画布。

### 拖放一个图像

1. 浏览左侧面板中显示的图像缩略图。

1. 将图像缩略图拖放到画布中，您可以在此处添加新的图像组件。

   ![拖放图像资产](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

## 查找并选择图像

1. 将图像组件添加到画布并单击&#x200B;**[!UICONTROL Experience Manager Assets]**&#x200B;以打开&#x200B;_[!UICONTROL 选择Assets]_&#x200B;对话框。

   ![为图像组件选择资源](./assets/content-image-component-empty.png){width="600" zoomable="yes"}

1. 在对话框中，使用可用工具选择一个图像，以查找所需的资源：

   * 更改右上角的&#x200B;**[!UICONTROL 存储库]**。

   * 单击右上角的&#x200B;**[!UICONTROL 管理资源]**&#x200B;可在其他浏览器选项卡中打开Assets存储库并使用AEM Assets管理工具。

   * 单击右上角的&#x200B;_视图类型_&#x200B;选择器以将显示更改为&#x200B;**[!UICONTROL 列表视图]**、**[!UICONTROL 网格视图]**、**[!UICONTROL 图库视图]**&#x200B;或&#x200B;**[!UICONTROL 瀑布视图]**。

   * 单击&#x200B;_排序顺序_&#x200B;图标可在升序和降序之间更改排序顺序。

     ![使用“选择Assets”对话框中的工具查找并选择图像资源](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * 单击&#x200B;**[!UICONTROL 排序方式]**&#x200B;菜单箭头以将排序条件更改为&#x200B;**[!UICONTROL 名称]**、**[!UICONTROL 大小]**&#x200B;或&#x200B;**[!UICONTROL 修改时间]**。

   * 单击左上角的&#x200B;_筛选器_&#x200B;图标以根据您的条件筛选显示的项目。

   * 在搜索字段中输入文本，以筛选显示的项目以匹配资源名称。

   ![使用筛选器和搜索字段查找资源](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 选择]**。
<!-- 

## Upload assets

To import files to Assets as a Cloud Service, you first need to browse or create the folder to be used for storage. You can then import an asset and add it to your email content. After assets are uploaded, you can [use the image assets as you author content](./assets-overview.md#add-assets-to-your-content).

1. While authoring your content in the email designer, drag an image element into the canvas. 

   The properties on the right reflect the image element selection. 

1. Click **[!UICONTROL Import media]** to open the _[!UICONTROL Upload image]_ dialog.

1. If your file system is open to your image file, drag and drop the file on the box in the dialog.

   ![Upload image file to Assets repository](./assets/email-designer-image-upload.png){width="700" zoomable="yes"}

   You can also click the **[!UICONTROL Select a file from your computer]** link and use your file system to locate and select the image file. Click Open and the image file is displayed in the box.

1. Click **[!UICONTROL Import]**.
-->
