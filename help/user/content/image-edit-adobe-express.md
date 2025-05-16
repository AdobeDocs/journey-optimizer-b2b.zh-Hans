---
title: 使用Adobe Express编辑图像
description: 了解如何使用Adobe Express在Journey Optimizer B2B edition工作区中编辑图像。
feature: Assets, Content, Integrations
role: User
exl-id: 16909f8f-77db-40f8-acd6-e18ac50c0af9
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 3%

---

# 使用 Adobe Express 编辑图像 {#edit-images-adobe-express}

>[!CONTEXTUALHELP]
>id="ajo-b2b_assets_edit_adobe_express"
>title="在 Adobe Express 中编辑图像"
>abstract="可直接在 Adobe Journey Optimizer B2B Edition 中使用简单而直观的受 Adobe Express 支持的图像编辑工具，以提高内容速度。"

Adobe Journey Optimizer B2B edition与Adobe Express原生集成，允许您访问一组Adobe Express图像编辑工具。 您可以使用这些工具修改存储在Journey Optimizer B2B edition工作区中的图像以访问连接的Marketo Engage资源存储库。 该集成具有以下主要优势：

* 通过在Journey Optimizer B2B edition中编辑和保存新图像资源来提高内容重复使用率。

* 减少了更新图像资源或创建现有图像资源的新版本的时间和精力。

>[!NOTE]
>
>所有Adobe ExpressB2B edition订阅都包含Journey Optimizer编辑功能的权限。

Adobe Express函数支持PNG和JPEG图像文件格式。

_要修改图像：_

1. 转到左侧导航并单击&#x200B;**[!UICONTROL 内容管理]** > **[!UICONTROL Assets]**。

此操作会打开一个列表页面，其中列出了所有资产。 默认情况下已选择&#x200B;_[!UICONTROL Journey Optimizer B2B edition]_&#x200B;工作区。

1. 找到要修改的图像，或将其用作创建新资源的原始图像。

   * 要按工作区和文件夹查看资源，请单击左上角的&#x200B;_显示文件夹_&#x200B;图标以打开结构。

   * 要按任意列对表进行排序，请单击列标题。 标题行中的箭头指示当前排序列和顺序。

   * 要在选定的工作区或文件夹中搜索图像资源，请在搜索栏中输入文本字符串。

   ![浏览Journey Optimizer B2B edition工作区中的资源](./assets/assets-native-workspace-filtered.png){width="800" zoomable="yes"}

1. 单击图像资源的名称以将其打开并查看其详细信息。

   >[!TIP]
   >
   >在继续编辑图像文件之前，最佳做法是选择图像详细信息中的[由&#x200B;]_使用的_[[!UICONTROL &#x200B;选项卡]](./marketo-engage-design-studio.md#view-asset-used-by-references)并查看当前使用该图像的内容。

1. 在右侧的图像&#x200B;_[!UICONTROL 详细信息]_&#x200B;中，单击&#x200B;**[!UICONTROL 使用Adobe Express编辑]**。

   ![在Adobe Express编辑器中打开图像](./assets/assets-edit-adobe-express.png){width="600" zoomable="yes"}

   如果该图像正在使用中，则会出现一个警报对话框，通知您所做的任何更改都将影响该内容。 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以进入Adobe Express编辑器。

   ![警报提供有关映像使用情况的信息](./assets/assets-edit-adobe-express-usage-alert.png){width="300"}

## Adobe Express企业许可证

如果您拥有Adobe Express的企业版许可证，则可以访问和使用Express编辑器。 这些编辑功能包括用于图像调整的操作，例如颜色、亮度、锐化、对比和裁切。 它们还包含&#x200B;_AI魔术_&#x200B;操作，如删除背景、插入和删除对象以及擦除图像的部分。

>[!NOTE]
>
>必须在同一IMS组织下购买您的Adobe Express Enterprise许可证，才能从Journey Optimizer B2B edition访问这些完整的编辑器功能。 作为IMS组织的个人成员，您需要在Adobe Express实例中分配许可证。 否则，您的Adobe Express访问权限将被限制为Journey Optimizer B2B edition中针对Adobe Express[&#128279;](#quick-actions-in-adobe-express)的快速操作。

![在Adobe Express Enterprise编辑器中打开图像](./assets/assets-edit-adobe-express-enterprise-editor.png){width="600" zoomable="yes"}

[Adobe Express用户指南](https://helpx.adobe.com/cn/express/user-guide.html){target="_blank"}提供了有关可用编辑功能的详细信息。

## Adobe Express中的快速操作

如果您没有Adobe Express企业许可证，则可以访问Adobe Express快速操作编辑器。

1. 在Adobe Express快速操作编辑器中，选择任意图像修改函数以更改图像。

   * [**[!UICONTROL 调整图像大小]**](#resize-image)
   * [**[!UICONTROL 删除背景]**](#remove-background)
   * [**[!UICONTROL 裁切图像]**](#crop-image)
   * [**[!UICONTROL 转换为PNG]**](#convert-file-format)(加载JPEG图像时)
   * [**[!UICONTROL 转换为JPEG]**](#convert-file-format)（加载PNG图像时）

   ![选择编辑类型以修改图像](./assets/assets-edit-adobe-express-left-menu.png){width="600" zoomable="yes"}

1. 返回主Adobe Express快速操作编辑器时，单击&#x200B;**[!UICONTROL 保存]**&#x200B;以使用相同的文件名将修改后的图像文件保存到Journey Optimizer B2B edition资源工作区中。

## 调整图像大小

1. 使用调整大小设置来缩小或展开图像：

   * 选择&#x200B;**[!UICONTROL 宽高比]**&#x200B;选项。 使用数字内容的标准大小，或者选择&#x200B;**[!UICONTROL 自定义]**（如果要输入&#x200B;**[!UICONTROL 宽度]**&#x200B;和&#x200B;**[!UICONTROL 高度]**&#x200B;的值），以满足您的需要。

   * 显示的&#x200B;_[!UICONTROL 原始大小]_&#x200B;和&#x200B;_[!UICONTROL 压缩大小]_&#x200B;显示的是应用更改后导致的大小更改。 使用&#x200B;**[!UICONTROL 缩放和裁切]**&#x200B;工具，您可以更密切地检查所显示图像的各个部分。

   * 如果要将图像恢复到其原始状态，请单击&#x200B;**[!UICONTROL 重置]**。

   ![使用Adobe Express编辑 — 调整图像大小](./assets/assets-edit-adobe-express-resize-image.png){width="600" zoomable="yes"}

1. 如果对结果满意，请单击&#x200B;**[!UICONTROL 应用]**。

## 删除背景

![使用Adobe Express编辑 — 删除背景](./assets/assets-edit-adobe-express-remove-background.png){width="600" zoomable="yes"}

Adobe Express执行自动背景移除以隔离图像中的主要对象。 如果对结果满意，请单击&#x200B;**[!UICONTROL 应用]**。

## 裁切图像

1. 拖动图像边角的手柄，以移除不想包含在图像资源中的外部区域。

   ![使用Adobe Express编辑 — 裁切图像](./assets/assets-edit-adobe-express-crop-image.png){width="600" zoomable="yes"}

1. 如果对结果满意，请单击&#x200B;**[!UICONTROL 应用]**。

## 转换文件格式

* **[!UICONTROL 转换为JPEG]** — 对于PNG图像，您可以将该图像转换为JPEG图像文件，并将其另存为工作区中的新资源。
* **[!UICONTROL 转换为PNG]** — 对于JPEG图像，您可以将该图像转换为PNG图像文件，并将其另存为工作区中的新资源。

![使用Adobe Express编辑 — 转换为PNG](./assets/assets-edit-adobe-express-convert-to-png.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 应用]**。
