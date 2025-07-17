---
title: 购买组角色模板
description: 了解如何定义用作购买组组件的角色模板。
feature: Buying Groups
role: User
exl-id: 9206356e-e9cf-486c-8982-c7d893222413
source-git-commit: 64e6b19894be749b154720ea542c8b18b9153a07
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 3%

---

# 购买群组角色模板

在B2B市场中，购买决策通常由多人做出。 这些个人根据其在组织内的作用参与决策过程。 根据每种产品和服务类型或帐户用例，创建包含这些角色定义的购买组角色模板。

![视频](../../assets/do-not-localize/icon-video.svg){width="30"} [观看概述视频](#overview-video)

## 访问和浏览角色模板

1. 在左侧导航栏中，单击&#x200B;**[!UICONTROL 购买群组]**。

1. 在&#x200B;_[!UICONTROL 购买组]_&#x200B;页面中，选择&#x200B;**[!UICONTROL 角色模板]**&#x200B;选项卡。

   ![“角色模板”选项卡](assets/roles-templates-tab.png){width="700" zoomable="yes"}

   该选项卡提供所有现有角色模板的清单列表，并以列格式显示以下信息：

   * [!UICONTROL 名称]
   * [!UICONTROL 状态]
   * [!UICONTROL 创建日期]
   * [!UICONTROL 创建者]
   * [!UICONTROL 上次更新]
   * [!UICONTROL 上次更新者]
   * [!UICONTROL 发布日期]
   * [!UICONTROL 发布者]

   默认情况下，该列表按&#x200B;_[!UICONTROL 上次更新]_&#x200B;排序。 所有角色模板的状态均为`Draft`或`Live`。

1. 要按名称筛选列表，请使用列表顶部的搜索字段。

   输入名称的前几个字符可将显示的列表缩小到匹配项。

   ![按搜索字符串筛选角色模板](assets/roles-templates-search.png){width="700" zoomable="yes"}

## 创建角色模板

1. 在&#x200B;_[!UICONTROL 角色模板]_&#x200B;选项卡中，单击右上角的&#x200B;**[!UICONTROL 创建模板]**。

1. 在对话框中，为模板输入唯一的&#x200B;**[!UICONTROL Name]**（必需）和&#x200B;**[!UICONTROL Description]**（可选）。

   ![创建角色模板对话框](assets/roles-template-create-dialog.png){width="400"}

1. 单击&#x200B;**[!UICONTROL 创建]**。

### 添加模板角色

创建模板后，该模板将在工作区中打开，并提示您定义角色。 默认情况下，将显示第一个角色卡。

您为模板定义的每个角色都使用一组筛选器（即&#x200B;_条件_）来确定分配给该角色的成员。 使用以下过滤器类型定义角色的条件：

| 类型 | 条件 |
| ---- | --------- |
| 人员属性 | <li>电子邮件地址 <li>电子邮件无效 <li>电子邮件已暂停 <li>传真号 <li>名字 <li>推断的状态区域 <li>作业名称 <li>姓氏 <li>中间名 <li>手机号码 <li>电话号码 <li>邮政编码 <li>State <li>退订 <li>取消订阅的原因 |
| 特殊过滤器 | <li>列表成员 <li>计划成员 |
| 意图数据 | 类别意图 <li>产品意图 <li>关键字意图<br/>[了解意图数据](../admin/intent-data.md)。 |

1. 对于第一个角色信息卡，定义角色属性。

   * 从列表中选择&#x200B;**[!UICONTROL 购买团体角色]**。

     对于当前版本，有六个角色：`Decision Maker`、`Influencer`、`Practitioner`、`Executive Steering Committee`、`Champion`和`Other`。

     ![购买团体角色列表](./assets/roles-template-create-roles-list.png){width="700" zoomable="yes"}

   * 为用于计算参与度分数的角色设置&#x200B;**[!UICONTROL 权重]**。

     每个选项的值已转换为得分计算的百分比： [!UICONTROL 普通] = 20，[!UICONTROL 次要] = 40，[!UICONTROL 普通] = 60，[!UICONTROL 重要] = 80，以及[!UICONTROL 重要] = 100。

     例如，角色使用Vital、Important和Normal的角色模板随后将转换为100/240、80/240、60/240。

   * **[!UICONTROL 为自动分配添加条件]** — 选中此复选框可将自动分配成员的条件添加到符合条件的购买组。 如果未选中该复选框，则不需要添加条件。

   * **[!UICONTROL 完整性得分必需]** — 如果您希望该角色成为计算完整性得分的要求，请选中此复选框。

1. 单击&#x200B;**[!UICONTROL 添加条件]**&#x200B;并为角色定义条件规则。

   * 在&#x200B;_[!UICONTROL 条件]_&#x200B;对话框中，展开&#x200B;**[!UICONTROL 人员属性]**&#x200B;的列表，然后找到要用于匹配角色的属性。 将其拖动到右侧，然后将其放到过滤器空间中。

     ![角色模板添加条件拖动属性](assets/roles-template-role-attribute.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >如果您在Experience Platform的帐户受众架构中定义了自定义人员字段，则这些字段也可用作条件中的人员属性。

   * 使用属性可使用一个或多个值创建匹配过滤器。

     在以下示例中，职称属性用于标识决策者的匹配项。 任何以`Director`或`Sr Director`开头的标题值都会将该条件的评估为true。

     使用工作标题的![角色模板条件示例](assets/roles-template-condition-example-job-title.png){width="700" zoomable="yes"}

   * 如果需要，可添加其他属性和条件，以进一步优化与角色的匹配条件。

   * 单击&#x200B;**[!UICONTROL 完成]**。

1. 对于要为模板包括的每个其他角色，单击&#x200B;**[!UICONTROL 添加其他角色]**&#x200B;并重复步骤1和2以定义该角色。

   ![定义了多个角色的角色模板](assets/roles-template-multiple-roles.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX “Marketo Engage列表成员资格”]

在Marketo Engage中，_Smart Campaigns_&#x200B;检查项目成员资格，以确保潜在客户不会收到重复的电子邮件，并且不会同时成为多个电子邮件流的成员。 在Journey Optimizer B2B中，您可以检查Marketo Engage列表成员资格，将其作为您角色模板的条件，以帮助消除购买组成员资格和旅程活动中的重复。

要将列表成员资格用作角色条件，请展开&#x200B;**[!UICONTROL 特殊筛选器]**，并将&#x200B;**[!UICONTROL 列表成员]**&#x200B;条件拖入筛选器空间。 然后完成筛选器定义以评估一个或多个Marketo Engage列表中的成员资格。

Marketo Engage列表成员资格的![角色模板条件](assets/roles-template-conditions-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

您的更改将自动保存为&#x200B;_草稿_&#x200B;状态。 如果您还未准备好发布角色模板，请单击页面顶部的左（后）箭头，并返回到&#x200B;_[!UICONTROL 角色模板]_&#x200B;列表。

### 发布角色模板

如果模板已准备就绪，请单击右上方的&#x200B;**[!UICONTROL 发布]**。

发布模板会将状态设置为&#x200B;_Live_&#x200B;状态，并使其可用于与解决方案兴趣关联。 必须至少定义一个角色才能发布角色模板。

## 编辑草稿角色模板

当角色模板处于&#x200B;_草稿_&#x200B;状态时，您可以继续编辑定义的角色。 您所做的任何更改都会自动保存。

更改角色卡标题中的任何设置，包括购买组角色、权重、自动分配和完整性评分要求。

![更改购买团体角色属性](./assets/roles-template-role-properties.png){width="600"}

### 修改角色的条件

要更改任何角色的条件/筛选逻辑，请单击角色卡片右上角的&#x200B;_编辑_ （ ![编辑图标](../assets/do-not-localize/icon-edit.svg) ）图标。 此操作打开&#x200B;_[!UICONTROL 条件]_&#x200B;工作区，您可以在其中修改现有筛选器、添加或删除筛选器或更改筛选器逻辑。

### 删除角色信息卡

如果要从模板中删除角色，请单击角色信息卡中的&#x200B;_删除_ （![删除图标](../assets/do-not-localize/icon-delete.svg) ）图标。

### 设置角色的优先级

您可以对模板中的角色重新排序，这决定了将潜在客户分配给角色的优先级。 每个角色卡的右侧显示有&#x200B;**[!UICONTROL 优先级]**&#x200B;控制器。 单击右侧的&#x200B;_向上_&#x200B;或&#x200B;_向下_&#x200B;箭头可按优先级向上或向下移动角色卡。

![更改角色优先级](./assets/roles-template-role-priority.png){width="700"}

## 删除角色模板

如果角色模板处于&#x200B;_草稿_&#x200B;状态，则可以将其删除。

1. 从列表中选择角色模板以将其打开。

1. 单击右上方的&#x200B;**[!UICONTROL 删除]**。

   ![更改角色优先级](./assets/roles-template-delete.png){width="700"}

1. 在对话框中，单击&#x200B;**[!UICONTROL 删除]**&#x200B;以进行确认。

## 概述视频

>[!VIDEO](https://video.tv.adobe.com/v/3433079/?learn=on)
