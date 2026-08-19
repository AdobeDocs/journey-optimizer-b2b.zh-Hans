---
title: C2PA元数据
description: 了解Adobe Journey Optimizer B2B edition如何将C2PA元数据自动应用于使用创作AI工具生成或编辑的图像，以及这对于您的内容意味着什么。
feature: Assets, Content
hide: true
role: User
autotag-review: '2026-07-31T22:15:54.535Z'
TQID: 'https://experienceleague.adobe.com/9XCqPWz62uDDLFAyxARfD2jErYx2aOiOB5fAOGLLTbo'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0b
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c1e8e03ccd6f2d132ca1bc1a27c0d9ea18dcdcac
workflow-type: tm+mt
source-wordcount: 913
ht-degree: 0%

---

# C2PA元数据

营销机构比以往任何时候都更关注内容透明度、人工智能披露，以及防止资产被篡改。 Adobe的Content Authenticity Initiative (CAI)构建符合[内容来源和授权联盟](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA)技术标准的工具。 _C2PA元数据_&#x200B;是加密的、显示篡改的信息，可帮助查看者了解内容的历程并确保品牌资产的完整性。 此信息包括：

* 发行者或签名者 — 关于发行数字签名以证明或签署资产的实体或公司的信息。
* 问题日期 — 将C2PA元数据应用于资源的日期。
* 信用和使用 — 有关资产制作者的信息，包括名称、社交媒体句柄或其他身份相关信息。
* 流程 — 对资产进行任何编辑或修改的记录。
* 设备详细信息 — 有关用于创建或编辑资产的应用程序或设备的信息。
* 使用的AI工具 — 如果使用创作AI编辑或创建资产，则可能包含所使用的模型的名称。
* 其他相关信息 — 可能还包括其他数据，以帮助提供有关资产历史的更多上下文。

有关资产历史记录的全面信息，您可以使用Adobe Content Authenticity [检查工具](https://contentauthenticity.adobe.com/inspect)。

C2PA元数据会随图像文件一起保留。 使用创作AI生成或编辑的图像上传到[!DNL Adobe Journey Optimizer B2B Edition]或从导出时，其C2PA元数据将保留。

>[!NOTE]
>
>某些将图像导入内容的方法(例如从PDF或从嵌入的(base64)源中提取图像)可能不会保留原始C2PA元数据。 在这些情况下，无法从源中读取C2PA元数据，并且不会为结果创建任何元数据。

>[!BEGINSHADEBOX]

## 通过渠道的C2PA元数据持久性 {#channels}

当您将图像包含在电子邮件或WhatsApp消息中时，也会保留已投放图像的C2PA元数据：

* **电子邮件** — 当您使用&#x200B;_发送电子邮件_&#x200B;历程操作时，请将该图像从&#x200B;_Assets_&#x200B;库添加到您的电子邮件内容。 在发送电子邮件时，收件人可以从邮件中下载图像，并且C2PA元数据保持不变。
* **WhatsApp** — 将图像添加到您的Meta商业帐户的WhatsApp消息模板中。 您可以直接从自己的系统添加该文件，或从&#x200B;_Assets_&#x200B;库下载图像文件。 使用此模板进行&#x200B;_发送WhatsApp_&#x200B;历程操作。 在传递WhatsApp消息时，收件人可以从消息中下载图像，并且C2PA元数据是完整的。

>[!ENDSHADEBOX]

## 影响C2PA元数据的操作 {#cc-workflows}

>[!INFO]
>
>围绕创新型人工智能透明度的新法律正在出现，Adobe正在努力满足跨司法辖区的适用要求。 C2PA元数据是Adobe用于满足这些法规要求的源工具。

在[!DNL Journey Optimizer B2B Edition]中使用创作AI工具生成或编辑图像时，C2PA元数据会自动附加到该图像，您无需执行任何操作。

### 生成图像 {#generate}

**_Example:_**&#x200B;通过描述所需视觉效果的文本提示为电子邮件生成横幅图像。 C2PA元数据附加到生成的图像。

在从文本提示、引用图像创建新图像或生成类似图像时，始终附加C2PA元数据。

### 裁切图像 {#crop}

**_示例:_**

* 裁切生成的横幅图像以适合网页。 C2PA元数据通过裁切进行保留。
* 使用上传的照片库作为电子邮件背景，并裁切它以适合屏幕。 如果照片中没有产生式的AI信息，则不会创建C2PA元数据。

对图像文件进行调整时（例如将其裁剪为请求的尺寸），仅当源图像已具有其C2PA元数据时，才会保留该元数据。 裁剪会重新创建图像像素，这通常会删除该C2PA元数据，因此AI Assistant在裁剪之前会从源图像读取该元数据，然后重新创建并将其重新附加到裁剪的结果。 裁剪本身不会添加新的创新型人工智能操作；而是保留现有操作。

### 添加文本叠加

**_Example:_**&#x200B;在登陆页面生成的背景图像上生成促销标题作为文本叠加。 来自背景图像的C2PA元数据将被保留。

在背景图像上渲染生成的文本时，仅当背景图像已具有C2PA元数据时，C2PA元数据才会附加到生成的图像中。 渲染叠加会生成一个新图像，因此图像编辑工具从背景中读取C2PA元数据并将其重新附加到结果中。 叠加步骤不会添加新的创作AI操作。

### 叠加图像

**_示例:_**

* 通过将生成的产品图像与生成的背景相结合，创建电子邮件标题。 结果携带反映两个创作AI源的C2PA元数据。
* 将两张上传的品牌照片合并到一个拼贴图像中。 由于源图像都不会执行生成性人工智能操作，因此不会创建C2PA元数据。

当您将两个或更多图像组合在一起，并且任何源图像具有C2PA元数据时，组合的图像会保留它，并合并到单个C2PA元数据元素中。 合成会从源中生成一个新图像，该图像通常会删除该C2PA元数据。 但是，图像编辑工具在合成之前读取源元数据，然后构建单个组合C2PA元数据元素，该元素列出每个有助于创作AI操作的源。

<!--

In [!DNL Adobe Journey Optimizer B2B Edition], you can see C2PA metadata directly within the _Assets_ library. When you open the asset details, any image with C2PA metadata (such as those created with GenAI services) shows the manifest details in a dedicated panel. If the asset is downloaded, published, or shared, the C2PA metadata remains intact with the asset.

_To access C2PA metadata:_

1. In the left navigation, expand **[!UICONTROL Content Management]** and select **[!UICONTROL Assets]**.

   This action opens a listing page with all the assets listed.

1. Navigate to a folder, and select the desired asset.

1. In the right panel, ??? where is it.

-->
