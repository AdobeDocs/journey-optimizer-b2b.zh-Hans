---
title: 购买组角色模板
description: 了解如何定义用作购买组组件的角色模板。
feature: Buying Groups
exl-id: 9206356e-e9cf-486c-8982-c7d893222413
source-git-commit: 099b515ac91e37c90421cf92f7a724257b07f42e
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---

# 购买组角色模板

在B2B市场中，购买决策通常由多人做出。 这些个人根据其在组织内的作用参与决策过程。 根据每种产品和服务类型或帐户用例，创建包含这些角色定义的购买组角色模板。

## 访问和浏览角色模板

1. 在Adobe Experience Platform主页中，单击Adobe Journey Optimizer B2B Edition 。

1. 在左侧导航栏中，单击&#x200B;**[!UICONTROL 购买群组]**。

1. 在&#x200B;_[!UICONTROL 购买组]_&#x200B;页面中，选择&#x200B;**[!UICONTROL 角色模板]**&#x200B;选项卡。

   ![“角色模板”选项卡](assets/roles-templates-tab.png){width="700" zoomable="yes"}

   该选项卡提供了所有现有角色模板的清单列表，这些模板具有以下列：

   * [!UICONTROL 名称]
   * [!UICONTROL 状态]
   * [!UICONTROL 创建日期]
   * [!UICONTROL 创建者]
   * [!UICONTROL 上次更新]
   * [!UICONTROL 上次更新者]
   * [!UICONTROL 发布于]
   * [!UICONTROL 发布者]

   默认情况下，该列表按&#x200B;_[!UICONTROL 上次更新]_&#x200B;列排序。

   _实时_（已发布）角色模板的数量显示在页面的右上方。 所有角色模板的状态均为`Draft`或`Live`。

1. 要按名称筛选列表，请使用列表顶部的搜索字段。

   输入名称的前几个字符可将显示的列表缩小到匹配项。

   ![按搜索字符串筛选角色模板](assets/roles-templates-search.png){width="700" zoomable="yes"}

## 创建角色模板

1. 在&#x200B;_[!UICONTROL 角色模板]_&#x200B;选项卡中，单击右上角的&#x200B;**[!UICONTROL 创建模板]**。

1. 在对话框中，为模板输入唯一的&#x200B;**[!UICONTROL Name]**（必需）和&#x200B;**[!UICONTROL Description]**（可选）。

   ![创建角色模板对话框](assets/roles-template-create-dialog.png){width="400"}

1. 为要为模板定义的每个角色添加一个规则。

* 从列表中选择&#x200B;**[!UICONTROL 购买团体角色]**。

  对于当前版本，有六个角色：`Decision Maker`、`Influencer`、`Practitioner`、`Executive Steering Committee`、`Champion`和`Other`。

![购买团体角色列表](./assets/roles-template-create-roles-list.png){width="700" zoomable="yes"}

* 为用于计算参与度分数的角色设置&#x200B;**[!UICONTROL 权重]**。

  每个选项的值已转换为得分计算的百分比： [!UICONTROL 普通] = 20，[!UICONTROL 次要] = 40，[!UICONTROL 普通] = 60，[!UICONTROL 重要] = 80，以及[!UICONTROL 重要] = 100。

  例如，角色使用Vital、Important和Normal的角色模板随后将转换为100/240、80/240、60/240。

* **[!UICONTROL 为自动分配添加条件]** — 选中此复选框可将自动分配成员的条件添加到符合条件的购买组。 如果未选中该复选框，则不需要添加条件。

* **[!UICONTROL 完整性得分必需]** — 如果您希望该角色成为计算完整性得分的要求，请选中此复选框。—>

* 单击&#x200B;**[!UICONTROL 添加条件]**。

   * 在条件对话框中，展开&#x200B;**[!UICONTROL 人员属性]**&#x200B;的列表，并找到要用于匹配角色的属性。 将其拖动到右侧，然后将其放到过滤器空间中。

     ![角色模板添加条件拖动属性](assets/roles-template-role-attribute.png){width="700" zoomable="yes"}

   * 使用属性可使用一个或多个值创建匹配过滤器。

     在以下示例中，职称属性用于标识决策者的匹配项。 任何以`Director`或`Sr Director`开头的标题值都会将该条件的评估为true。

     使用工作标题的![角色模板条件示例](assets/roles-template-condition-example-job-title.png){width="700" zoomable="yes"}

   * 如果需要，可添加其他属性和条件，以进一步优化与角色的匹配条件。

   * 单击&#x200B;**[!UICONTROL 完成]**。

对于要为模板包括的每个其他角色，单击&#x200B;**[!UICONTROL 添加其他角色]**&#x200B;并定义一个或多个条件以与该角色匹配。

![定义了多个角色的角色模板](assets/roles-template-multiple-roles.png){width="700" zoomable="yes"}

1. 如果模板已准备就绪，请单击右上方的&#x200B;**[!UICONTROL Publish]**。

   发布模板会将其设置为&#x200B;_实时_&#x200B;状态，并使其可以与解决方案兴趣关联。 必须至少定义一个角色才能发布角色模板。

   您的更改将自动保存为&#x200B;_草稿_&#x200B;状态。 如果您还未准备好发布角色模板，请单击页面顶部的左（后）箭头，并返回到“角色模板”列表。

## 编辑草稿角色模板

当角色模板处于&#x200B;_草稿_&#x200B;状态时，您可以继续编辑定义的角色。 您所做的任何更改都会自动保存。

更改角色卡标题中的任何设置，包括购买组角色、权重、自动分配和完整性评分要求。

![更改购买团体角色属性](./assets/roles-template-role-properties.png){width="600"}

### 修改角色的过滤器

要更改任何角色的筛选逻辑，请单击角色卡片右上角的&#x200B;_编辑_（铅笔）图标。 此操作打开&#x200B;_[!UICONTROL 条件]_&#x200B;工作区，您可以在其中修改现有筛选器、添加另一个筛选器、删除筛选器或更改筛选器逻辑。

### 删除角色信息卡

如果要从模板中删除角色，请单击角色信息卡中的&#x200B;_删除_（垃圾桶）图标。

### 设置角色的优先级

您可以对模板中的角色重新排序，这决定了将潜在客户分配给角色的优先级。 每个角色卡的右侧显示有&#x200B;**[!UICONTROL 优先级]**&#x200B;控制器。 单击右侧的&#x200B;_向上_&#x200B;或&#x200B;_向下_&#x200B;箭头可按优先级向上或向下移动角色卡。

![更改角色优先级](./assets/roles-template-role-priority.png){width="700"}

## 删除角色模板

如果角色模板处于&#x200B;_草稿_&#x200B;状态，则可以将其删除。

1. 从列表中选择角色模板以将其打开。

1. 单击右上方的&#x200B;**[!UICONTROL 删除]**。

   ![更改角色优先级](./assets/roles-template-delete.png){width="700"}

1. 在对话框中，单击&#x200B;**[!UICONTROL 删除]**&#x200B;以进行确认。
