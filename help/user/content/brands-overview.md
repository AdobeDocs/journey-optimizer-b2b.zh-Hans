---
title: 使用品牌来生成内容并保持一致性
description: 了解您可以在Journey Optimizer B2B edition中定义的品牌准则，以根据您的品牌风格和声音生成和优化内容。
badge: label="Beta 版" type="Informative"
feature: Content, Brand Identity
hide: true
hidefromtoc: true
role: User
level: Beginner, Intermediate
exl-id: 83d210bc-a204-4b7e-8b7e-07b0ec5413b9
source-git-commit: c95323936f48a595a74c469c201b19daf1ee95e5
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 9%

---

# 使用品牌进行内容生成并确保一致性 {#brands}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_overview"
>title="开始使用品牌"
>abstract="创建并定制您自己的品牌，以塑造您独特的视觉风格与语言特征，同时更轻松地创作出符合您品牌风格和声音的内容。"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_ai_menu"
>title="选择您的品牌"
>abstract="选择您的品牌，以确保所有 AI 生成的内容都符合您的品牌规范和指南。"

品牌可帮助定义您的&#x200B;_品牌标识_，并在确保一致而有效的内容创建方面发挥关键作用，以准确表示您的品牌标识、价值和消息。 通过坚持定义清晰的品牌风格，组织可以跨渠道和接触点保持一致和可识别的品牌影响力，并在目标受众中增强其品牌认知度、信任度和忠诚度。

+++使用品牌的优势

您的组织可以通过在创建和评估内容时使用品牌来实现重大价值，例如：

* **一致的品牌标识** — 品牌指南作为其视觉和语言标识的基础Blueprint。 它们定义了品牌可识别的核心元素，例如徽标、调色板、排版规则、图像样式和语调。 通过遵循这些准则，内容创建者可以确保所有营销材料（从Web文案到社交媒体帖子再到电子邮件营销活动）始终反映独特的品牌个性和视觉识别。 这种一致性有助于加强品牌认知度并在目标市场内建立信任。

* **一致的讯息和定位** — 品牌指南通常包括概述品牌价值主张、关键讯息支柱和定位声明的讯息指南。 通过遵守这些准则，内容创作者可以确保其内容中的宣传讯息与整体品牌定位和价值主张保持一致。 这一一致的消息传递有助于强化其独特的卖点和独特优势，使客户更容易理解和联系品牌产品。

* **正宗的品牌语调和语调** — 品牌指南通常包括有关首选语调、沟通方式和语言使用的详细指导。 这些指导原则可帮助内容创作者抓住品牌个性并打造正确的语调，无论是友好和平易近人、专业和权威，还是娱乐和诙谐。 在所有内容中保持一致的品牌声音，有助于为客户营造更真实、更有吸引力的品牌体验。

* **视觉凝聚力和品牌知名度** — 品牌指南为视觉元素（如徽标、调色板、排版规则、图像样式和布局模板）提供了清晰的规则和规范。 遵守这些准则确保所有视觉内容保持一致和可识别的品牌美感。 这种视觉一致性有助于加强品牌认知度并与客户建立信任，因为他们可以轻松识别内容并将其与品牌关联。

* **品牌权益和声誉维护** — 始终遵守品牌准则有助于维护和保护品牌的权益和声誉。 当所有内容和营销材料都准确地反映品牌标识、价值和消息时，就会增强品牌信誉并巩固其在市场中的地位。 这种公平性和声誉可以提高客户忠诚度和倡导度，最终为品牌的长期成功做出贡献。

+++

>[!AVAILABILITY]
>
>此功能目前作为专用测试版提供，计划在未来版本中逐步提供给所有客户。
>
>在Adobe Journey Optimizer B2B edition中使用AI支持的功能之前，需要[用户协议](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}。 有关更多信息，请与您的 Adobe 代表联系。

定义的品牌为您的创意团队在创作任何视觉或书面内容时提供了&#x200B;_真实来源_。 在编译这些指南并共享品牌资产后，任何团队成员或协作者都可以为您的产品创建品牌上内容。 要在Journey Optimizer B2B edition中启用品牌内内容创建，请完成以下任务：

1. 准备品牌定义。

   * 高级品牌特征
   * 写作风格
   * 可视化元素

1. 在一个或多个PDF文件中组合此信息。

1. 使用PDF文件在Journey Optimizer B2B edition中[创建品牌](./brands-manage-create.md#create-and-define-a-brand)。

1. 当它可以使用时，[发布品牌](./brands-manage-create.md#publish-the-brand)。

1. 使用品牌进行[电子邮件内容对齐](./brand-alignment.md)。
<!-- 
1. Use the brand to generate content. -->

>[!BEGINSHADEBOX]

## 品牌相关权限

产品管理员可以通过在Adobe Experience Cloud中分配&#x200B;**[!UICONTROL 管理品牌套件]**&#x200B;或&#x200B;**[!UICONTROL 启用AI助手]**&#x200B;资源权限（通过&#x200B;_权限_&#x200B;应用程序），启用对品牌管理和品牌协调功能的访问。

1. 在权限应用程序中，转到&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡，然后选择所需的[角色](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/abac/permissions-ui/roles){target="_blank"}。

1. 单击&#x200B;**[!UICONTROL 编辑]**，修改权限。

1. 添加&#x200B;**[!UICONTROL AI助手]**&#x200B;资源，然后选择&#x200B;**[!UICONTROL 管理品牌套件]**&#x200B;或&#x200B;**[!UICONTROL 启用Ai助手]**

   >[!NOTE]
   >
   >**[!UICONTROL 启用Ai助手]**&#x200B;权限提供对&#x200B;**[!UICONTROL Brands]**&#x200B;库的只读访问权限。

   ![为品牌访问权限添加AI助理权限](./assets/brands-aep-permissions.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以应用更改。

   已分配给该角色的任何用户的权限都会自动更新。

1. 要将此角色分配给新用户，请选择“**[!UICONTROL 角色]**”仪表板中的“_[!UICONTROL 用户]_”选项卡，然后单击“**[!UICONTROL 添加用户]**”。

   * 输入用户名和电子邮件地址，或从列表中选择现有用户。

     如果尚未创建用户，请参阅[Experience Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/abac/permissions-ui/users){target="_blank"}。

   * 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以应用更改。

>[!ENDSHADEBOX]
