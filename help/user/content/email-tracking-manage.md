---
title: 管理电子邮件打开跟踪
description: 为单个电子邮件禁用电子邮件打开跟踪，或捕获人员的跟踪偏好设置，并使用拆分路径发送跟踪和非跟踪电子邮件变体。
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
autotag-review: '2026-07-08T00:02:50.497Z'
TQID: 'https://experienceleague.adobe.com/LIutoajlpVQTeJP2y4i0Wv7H-WqGj-c-LVsOGfin384'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 61481d57fb8eca805d9a9bc545124aed568b5416
workflow-type: tm+mt
source-wordcount: 860
ht-degree: 0%

---

# 管理电子邮件打开跟踪

您可以禁用单个电子邮件的打开跟踪，或在Adobe Experience Platform中捕获每个人的跟踪偏好设置，并使用拆分路径将人们路由到跟踪和非跟踪电子邮件变体。

>[!BEGINSHADEBOX “关于电子邮件跟踪像素的CNIL指南”]

2026年4月14日，全国信息和自由委员会&#x200B;*(CNIL)发布了关于在电子邮件中使用跟踪像素的[建议](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf)。*&#x200B;该指南阐明何时需要获得同意，并强调针对电子邮件像素跟踪的适当同意实践的重要性。 此策略可能会影响向位于法国的订阅者发送电子邮件的任何实体的发送实践。

电子邮件跟踪像素是嵌入到电子邮件HTML中的1x1透明图像。 收件人的电子邮件客户端加载该图像时，像素会向服务器发出ping信号，该信号记录时间戳、设备类型、电子邮件客户端等数据，有时还会记录IP地址以大致了解位置。 然后，该日志将绑定到收件人的记录，从而让营销人员知道电子邮件是否已打开。

此处描述的[!UICONTROL Journey Optimizer B2B edition]产品功能是构建块，经过适当配置和操作后，这些构建块可能支持合规的实施。 每位客户均须负责决定及履行其于适用法律下之责任。

>[!ENDSHADEBOX]

## 禁用对单个电子邮件的跟踪 {#disable-tracking-single-email}

当您希望特定电子邮件从不报告打开的活动时，无论谁接收该活动，都使用此选项。

1. 从右侧的历程节点属性中，打开电子邮件。

1. 在电子邮件属性中，选中&#x200B;**[!UICONTROL 禁用打开跟踪]**&#x200B;复选框。

   ![禁用电子邮件打开跟踪](./assets/email-tracking-disable-all.png){width="500" zoomable="yes"}

   有关电子邮件属性的完整列表，请参阅[定义电子邮件设置](./add-email.md#define-the-email-settings)。

## 按跟踪偏好设置划分人员 {#segment-people-tracking-preference}

如果您希望让每个人都选择是否跟踪其电子邮件打开次数，请在Adobe Experience Platform (AEP)中将该偏好设置捕获为人员属性。 您可以在[登陆页面表单](./forms.md)中使用此字段，以便您的联系人有机会选择退出电子邮件打开跟踪。 然后，您可以在历程中使用&#x200B;_拆分路径_&#x200B;节点将跟踪人员和非跟踪人员路由到不同的电子邮件变体。 这样，您就可以在不禁用每个人的打开跟踪的情况下，执行单个选择退出。

该工作流包括三个部分：

1. [在AEP中为跟踪首选项](#add-custom-field-tracking-preference)添加自定义字段，并通过表单链接发送选择退出通信。
1. [在历程中添加用于跟踪选择退出的拆分路径](#add-split-path-tracking)。
1. [为每个路径配置跟踪和非跟踪电子邮件变体](#configure-tracking-and-non-tracking-email-variants)。

### 添加用于跟踪首选项的自定义字段 {#add-custom-field-tracking-preference}

>[!NOTE]
>
>添加和映射自定义XDM字段是Adobe Experience Platform管理任务。 请与AEP管理员或数据工程团队合作来完成此步骤。

1. 在AEP中，打开用于B2B人员配置文件的架构（例如，_B2B人员_）。

1. 在租户ID下，为您的组织的同意管理字段（例如，`consents`）找到或创建一个字段组。

1. 向字段组添加一个字段，如名为`emailTracking`的布尔字段，以表示人员是否已同意打开跟踪。

1. 输入字段名称和显示名称，设置类型，将其分配给字段组，然后单击&#x200B;**[!UICONTROL 应用]**。

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以保存架构更改。

   ![将emailTracking字段添加到AEP架构同意字段组](./assets/email-tracking-xdm-field-aep-schema.png){width="800" zoomable="yes"}

1. 通过在[XDM字段管理](../admin/xdm-field-management.md#managed-fields)中选择[!UICONTROL XDM个人资料]类的&#x200B;_托管字段_，使该字段在[!DNL Journey Optimizer B2B Edition]中可用。

   ![在XDM字段管理中选择emailTracking作为托管字段](./assets/email-tracking-xdm-field-select.png){width="450"}

   这使得该字段可用作拆分路径节点中的条件。

### 添加用于跟踪选择退出的拆分路径 {#add-split-path-tracking}

向历程添加&#x200B;[_按人员拆分路径_&#x200B;节点](../journeys/split-merge-paths-nodes.md#split-paths-by-people)，并为每个跟踪首选项值定义路径。

1. 添加&#x200B;**[!UICONTROL 拆分路径]**&#x200B;节点并选择&#x200B;**[!UICONTROL 人员]**&#x200B;进行拆分。

1. 对于第一个路径，使用自定义跟踪首选项字段应用条件（例如，`emailTracking`为`true`）以识别允许打开跟踪的人员。

   ![拆分路径条件 — 将电子邮件跟踪字段添加为true](./assets/email-tracking-condition-true.png){width="700" zoomable="yes"}

1. 添加第二个路径并应用反向条件（`emailTracking`为`false`）以标识选择退出跟踪的人员。

   有关添加路径、应用条件和重新排序路径的一般步骤，请参阅[按人员添加拆分路径](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node)。

   ![按人员拆分路径 — 电子邮件跟踪打开和关闭条件](./assets/email-tracking-split-paths.png){width="500" zoomable="yes"}

### 配置跟踪和非跟踪电子邮件变体 {#configure-tracking-and-non-tracking-email-variants}

向每个路径添加一个[_[!UICONTROL 发送电子邮件&#x200B;]_&#x200B;操作节点](./add-email.md)，以便每个人接收与其跟踪首选项匹配的电子邮件变体。

1. 在启用跟踪的路径上，添加&#x200B;**[!UICONTROL 发送电子邮件]**&#x200B;操作，然后照常选择或创建电子邮件，在电子邮件属性中清除&#x200B;**[!UICONTROL 禁用打开跟踪]**。

1. 在选择的退出路径上，使用相同或重复的电子邮件添加&#x200B;**[!UICONTROL 发送电子邮件]**&#x200B;操作，然后选择右侧电子邮件属性中的&#x200B;**[!UICONTROL 禁用打开跟踪]**&#x200B;复选框。

   ![用于跟踪路径外的电子邮件 — 禁用打开跟踪](./assets/email-tracking-disable.png){width="600" zoomable="yes"}

1. [发布历程](../journeys/create-publish-journey.md#publish-a-journey)。

   系统会自动将用户路由到与其跟踪偏好设置字段值匹配的电子邮件变体，并且用户对其偏好设置所做的任何更新会在下次进入历程时反映出来。
