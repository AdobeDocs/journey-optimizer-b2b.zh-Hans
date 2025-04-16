---
title: 帐户列表
description: 了解帐户列表以及营销人员如何使用它们通过帐户历程定位帐户。
exl-id: 7d7f5612-f0fe-4bb8-ae16-29aa3552f0f9
source-git-commit: 08c8684d138005d4560941c7d89d6771472bcd60
workflow-type: tm+mt
source-wordcount: '1621'
ht-degree: 1%

---

# 帐户列表

帐户列表是营销人员可用于进行目标历程编排的指定帐户集合。 帐户列表可以根据您定义的条件（如行业、位置或公司规模）来定位指定帐户。 帐户列表有两种类型：

* **静态** — 使用静态帐户列表时，该列表仅在您添加帐户时更改。 您可以通过应用过滤器集以根据当前帐户数据填充列表来手动添加帐户，或通过帐户历程添加和删除帐户。
* **动态** — 使用动态帐户列表，您可以定义用于自动策划列表的过滤器集。 系统使用此筛选器集根据帐户信息的更改添加和删除帐户。 此列表管理类似于Real-time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/segmentation/b2b)中的[受众分段。

当帐户列表处于&#x200B;_实时_（已发布）状态时，它可用于帐户历程。

## 访问和浏览帐户列表

在左侧导航栏中，展开&#x200B;**[!UICONTROL 帐户]**，然后单击&#x200B;**[!UICONTROL 帐户列表]**。

![访问帐户历程](./assets/account-lists-browse.png){width="800" zoomable="yes"}

显示的&#x200B;_[!UICONTROL 帐户列表]_&#x200B;页包括以下列：

* [!UICONTROL 名称] （单击帐户列表名称以查看详细信息）
* [!UICONTROL 状态]
* [!UICONTROL 类型]
* [!UICONTROL 上次更新时间：]
* [!UICONTROL 上次更新者]
* [!UICONTROL 创建日期]
* [!UICONTROL 创建者]

此表包括按名称搜索的功能。 排序功能当前不可用。

您可以通过单击右上角的&#x200B;_列设置_ （ ![列设置](../assets/do-not-localize/icon-column-settings.svg) ）图标并选择或清除复选框来自定义显示的表。

![选择要在帐户历程列表中显示的列](./assets/account-lists-list-columns.png){width="300"}

要查看帐户列表的描述，请单击名称旁边的&#x200B;_信息_ （ ![信息图标](../assets/do-not-localize/icon-info.svg) ）图标。

## 创建帐户列表

在创建帐户列表时，您可以定义一组筛选条件来生成该列表。 例如，您可以使用它生成行业为医疗保健且收入超过1亿美元的客户列表。

1. 在&#x200B;_[!UICONTROL 帐户列表]_&#x200B;页面中，单击该页面右上角的&#x200B;**[!UICONTROL 创建帐户列表]**。

   ![单击“创建帐户列表”](./assets/account-lists-create.png){width="700" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 创建帐户列表]_&#x200B;对话框中，输入唯一的&#x200B;**[!UICONTROL 名称]**（必需）和&#x200B;**[!UICONTROL 描述]**（可选）。

1. 为帐户列表&#x200B;**[!UICONTROL 静态]**&#x200B;或&#x200B;**[!UICONTROL 动态]**&#x200B;选择&#x200B;_[!UICONTROL 类型]_。

   ![为帐户列表选择“静态”或“动态”](./assets/account-list-create-dialog.png){width="380"}

1. 单击&#x200B;**[!UICONTROL 创建]**。

   此时将打开一个新的静态帐户列表，其中包含一个空的帐户列表。 此时将打开新的动态帐户列表，该列表中包含&#x200B;_[!UICONTROL 按筛选器添加帐户]_&#x200B;面板。

## 将帐户添加到帐户列表

对于静态列表，您可以继续发布空帐户列表并通过帐户历程添加帐户。 您还可以在发布之前通过应用筛选器集手动添加帐户。

对于动态帐户列表，在发布列表之前，必须添加要用于自动管理列表的过滤器集。

>[!BEGINTABS]

>[!TAB 静态帐户列表]

创建静态帐户列表后，可以通过应用过滤器集来填充该列表。 您还可以应用筛选器集在静态帐户列表发布后(_Live_)将帐户添加到静态帐户列表。

>[!NOTE]
>
>如果您希望帐户列表以空形式开始，请不要选择任何过滤器，而只需发布帐户列表。 当您计划通过帐户历程操作添加成员时，最好从空列表开始（请参阅[执行操作节点 — 添加到帐户](#take-an-action-node---add-to-account)）。

1. 单击&#x200B;**[!UICONTROL 添加帐户]**。

   ![添加帐户筛选器以填充列表](./assets/account-lists-static-new-add-accounts.png){width="700" zoomable="yes"}

   您可以在空列表页面或右上角访问此函数。

1. 在&#x200B;_[!UICONTROL 按筛选器添加帐户]_&#x200B;对话框中，使用&#x200B;**[!UICONTROL 帐户筛选器]**&#x200B;菜单添加要用于构造筛选器集的属性和活动：

   过滤器将嵌套到类别文件夹中。 您可以展开每个文件夹并滚动浏览可用过滤器列表。 或者，使用顶部的&#x200B;_搜索_&#x200B;工具来查找所需的过滤器。

   * 将筛选器从左侧菜单拖放到筛选器定义空间。
   * 完成匹配评估定义。
   * 对要包含的每个过滤器重复这些操作。

     ![添加筛选器以填充帐户列表](./assets/account-lists-static-add-accounts-by-filters.png){width="700" zoomable="yes"}

   * 可以通过在顶部应用&#x200B;**[!UICONTROL 筛选器逻辑]**&#x200B;来优化条件。 您可以选择匹配所有属性条件或任何条件。

     ![帐户列表筛选器逻辑](./assets/account-lists-filter-logic.png){width="450"}

1. 筛选器集和逻辑完成后，单击&#x200B;**[!UICONTROL 填充帐户]**。

   填充过程可能需要一些时间，具体取决于要评估和填充的帐户数量（数据库的大小和您选择的筛选条件）。 帐户填充到您的列表中最多可能需要两个小时。

您可以继续发布列表，以使其可用于帐户历程中的添加和删除操作。

>[!TAB 动态帐户列表]

创建动态帐户列表后，定义用于在列表&#x200B;_处于活动状态_（已发布）时管理该列表（添加/删除帐户）的筛选器集。 您不能通过帐户历程添加/删除帐户，但它是一个已发布的动态帐户列表，可用于起始帐户受众节点。

1. 单击&#x200B;**[!UICONTROL 选择筛选器]**。

   ![选择用于动态填充列表的筛选器](./assets/account-lists-dynamic-new-select-filters.png){width="700" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 按筛选器添加帐户]_&#x200B;对话框中，使用&#x200B;**[!UICONTROL 帐户筛选器]**&#x200B;菜单添加要用于构造筛选器集的属性和特殊筛选器：

   过滤器将嵌套到类别文件夹中。 您可以展开每个文件夹并滚动浏览可用过滤器列表。 或者，使用顶部的&#x200B;_搜索_&#x200B;工具来查找所需的过滤器。

   * 将筛选器从左侧菜单拖放到筛选器定义空间。
   * 完成匹配评估定义。
   * 对要包含的每个过滤器重复这些操作。

     ![添加筛选器以填充帐户列表](./assets/account-lists-dynamic-add-accounts-by-filters.png){width="700" zoomable="yes"}

   * 可以通过在顶部应用&#x200B;**[!UICONTROL 筛选器逻辑]**&#x200B;来优化条件。 您可以选择匹配所有属性条件或任何条件。

     ![帐户列表筛选器逻辑](./assets/account-lists-filter-logic.png){width="450"}

1. 筛选器集和逻辑完成后，单击&#x200B;**[!UICONTROL 完成]**。

   如果您对筛选器集感到满意，可以继续[发布列表](#publish-an-account-list)，使其可用于帐户历程中的起始[帐户受众节点](#account-audience-node)。

   >[!NOTE]
   >
   >在发布动态帐户列表后，您无法更新该列表的筛选器。

   填充过程可能需要一些时间，具体取决于要评估和填充的帐户数量（数据库的大小和您选择的筛选条件）。 帐户填充到您的列表中最多可能需要两个小时。

>[!ENDTABS]

## 发布帐户列表

筛选器集完成后，您可以继续发布帐户列表。

>[!BEGINTABS]

>[!TAB 静态帐户列表]

1. 单击右上方的&#x200B;**[!UICONTROL 发布]**。

   ![单击右上角的“发布”](./assets/account-lists-static-publish.png){width="700" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 发布静态帐户列表]_&#x200B;对话框中，单击&#x200B;**[!UICONTROL 发布]**&#x200B;以进行确认。

   ![确认发布静态帐户列表](./assets/account-lists-static-publish-confirm.png){width="400"}

静态帐户列表的状态更改为&#x200B;_[!UICONTROL Live]_，它可用于[在帐户历程](#account-list-usage-in-account-journeys)中使用。

>[!TAB 动态帐户列表]

筛选器集完成后，您可以继续发布动态帐户列表。 在帐户列表处于“实时”状态后，便可在帐户受众历程节点中选择。

1. 单击右上方的&#x200B;**[!UICONTROL 发布]**。

   ![单击右上角的“发布”](./assets/account-lists-dynamic-publish.png){width="700" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL 发布动态帐户列表]_&#x200B;对话框中，单击&#x200B;**[!UICONTROL 发布]**&#x200B;以进行确认。

   ![确认发布动态帐户列表](./assets/account-lists-dynamic-publish-confirm.png){width="400"}

动态帐户列表的状态更改为&#x200B;_[!UICONTROL 实时]_，并且可在帐户历程](#account-list-usage-in-account-journeys)中[使用。

>[!ENDTABS]

## 帐户历程中的帐户列表使用情况

有三种方式可以将实时（已发布）帐户列表合并到帐户历程中：

### 帐户受众节点

1. 为起始&#x200B;_帐户受众_&#x200B;节点选择&#x200B;**[!UICONTROL 帐户列表]**。

   ![为帐户受众节点选择帐户列表选项](../journeys/assets/node-audience-account-list.png){width="500"}

1. 单击&#x200B;**[!UICONTROL 添加帐户列表]**。

1. 选中帐户列表的复选框，然后单击&#x200B;**[!UICONTROL 保存]**。

   ![为帐户受众节点选择帐户列表选项](../journeys/assets/node-audience-account-list-select-dialog.png){width="600" zoomable="yes"}

当历程处于活动状态（已发布）时，列表中的帐户将在历程中移动。

### 执行操作节点 — 添加到帐户

**_仅限静态帐户列表_**

使用[a _执行操作_&#x200B;节点](../journeys/action-nodes.md)将帐户添加到静态帐户列表。

例如，您可能有一个发送电子邮件的历程路径，一些帐户会将各种操作作为响应操作。 您将此活动视为历程中的资格点，并希望将它们添加到帐户列表，该帐户列表用于作为另一个历程的受众，该历程具有不同的合格帐户流程。

>[!NOTE]
>
>如果执行节点时帐户已位于列表中，则将忽略该操作。

1. 选择&#x200B;]_**[!UICONTROL 帐户]**上的_[!UICONTROL &#x200B;操作选项。

1. 若要对帐户&#x200B;]_执行_[!UICONTROL &#x200B;操作，请选择&#x200B;**[!UICONTROL 添加到帐户列表]**。

   ![选择“添加到帐户列表”](../journeys/assets/node-action-account-add-to-account-list.png){width="500"}

1. 对于&#x200B;**[!UICONTROL 选择实时静态帐户列表]**，选择要添加帐户的帐户列表。

   ![选择“添加到帐户列表”](../journeys/assets/node-action-account-add-to-account-list-select.png){width="500"}

### 执行操作节点 — 从帐户中删除

**_仅限静态帐户列表_**

使用[a _执行操作_&#x200B;节点](../journeys/action-nodes.md)从静态帐户列表中删除帐户。

例如，您可能有一个发送电子邮件的历程路径，一些帐户会将各种操作作为响应操作。 您将此活动视为历程中的资格认证点，并想要将其从帐户列表中删除，该帐户列表用于作为另一历程的受众，该历程会发送其他电子邮件，以便您不会复制资格认证通信。

>[!NOTE]
>
>如果某个帐户不在计划删除的列表中，则该操作将被忽略。

1. 选择&#x200B;]_**[!UICONTROL 帐户]**上的_[!UICONTROL &#x200B;操作选项。

1. 若要对帐户&#x200B;]_执行_[!UICONTROL &#x200B;操作，请选择&#x200B;**[!UICONTROL 从帐户列表中删除]**。

   ![选择“添加到帐户列表”](../journeys/assets/node-action-account-remove-from-account-list.png){width="500"}

1. 对于&#x200B;**[!UICONTROL 选择实时静态帐户列表]**，选择要从中删除帐户的帐户列表。

   ![选择“添加到帐户列表”](../journeys/assets/node-action-account-remove-from-account-list-select.png){width="500"}
