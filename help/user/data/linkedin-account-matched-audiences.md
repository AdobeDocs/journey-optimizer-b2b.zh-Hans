---
title: linkedIn帐户匹配的受众
description: 了解如何连接LinkedIn帐户并激活用于购买群组的数据流。
hidefromtoc: true
hide: true
source-git-commit: 63bf202e179895d72cd8b3f40e1bf5333bcd4c48
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%

---

# linkedIn帐户匹配的受众

Journey Optimizer B2B版本提供了通过“帐户匹配受众”生成LinkedIn广告受众的功能，旨在帮助您在购买群组中填充空角色。 通过定义一组购买群组过滤器，您可以维护一个LinkedIn匹配受众，以定位与您的购买群组参数相匹配的潜在客户。 此功能利用Experience Platform目标来管理集成的某些方面。 数据流上限为10个。

在从Journey Optimizer B2B版本启动数据流之前，必须至少有一个[（公司）LinkedIn匹配的Audience目标连接器](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/social/linkedin#connect)的实例具有在Experience Platform应用程序中配置的LinkedIn Campaign Manager帐户。

## 配置新的LinkedIn帐户连接 {#linkedin-destination-setup}

>[!CONTEXTUALHELP]
>id="ajo-b2b_linkedin_destination_setup"
>title="需要LinkedIn目标设置"
>abstract="将按购买团体过滤的帐户发送到Linkedin目标，以与潜在的购买团体成员进行接触。 您最多可以为10个不同的已过滤帐户组创建10个数据流。 要开始使用此功能，请先添加一个Linkedin目标。"

1. 在Experience Platform中，转到左侧导航栏中的&#x200B;**[!UICONTROL 连接]** > **[!UICONTROL 目标]**，然后选择&#x200B;**[!UICONTROL 目录]**&#x200B;选项卡。

1. 在目录中，找到&#x200B;**[!UICONTROL （公司） LinkedIn匹配的受众]**&#x200B;连接器，然后单击&#x200B;**[!UICONTROL 设置]**。

   ![访问（公司） LinkedIn匹配的受众连接器](./assets/aep-destinations-catalog-linkedin.png){width="800" zoomable="yes"}

1. 选择&#x200B;**[!UICONTROL 新帐户]** > **[!UICONTROL 连接到LinkedIn]**。

1. 提供您的LinkedIn凭据并登录。

   已将LinkedIn帐户作为目标连接。

## 更新帐户详细信息

在Journey Optimizer B2B版本中，购买组可以看到LinkedIn帐户的名称和描述。 最佳实践是更新此信息，以便与购买群组一起工作的营销人员能够轻松识别此信息。 您可以在Experience Platform或Journey Optimizer B2B版本UI中更改帐户详细信息。

1. 在左侧导航中转到&#x200B;**[!UICONTROL 连接]** > **[!UICONTROL 目标]**，然后选择&#x200B;**[!UICONTROL 帐户]**&#x200B;选项卡。

1. 对于您创建的新帐户，请单击&#x200B;_更多_ (**...**)菜单，然后选择&#x200B;**[!UICONTROL 编辑详细信息]**。

   ![编辑帐户详细信息](./assets/aep-destinations-accounts-edit-details.png){width="800" zoomable="yes"}

1. 在对话框中，更新名称和描述。

   ![编辑名称和描述](./assets/destinations-linkedin-account-edit-details-dialog.png){width="500"}

1. 单击&#x200B;**[!UICONTROL 保存]**。

## 激活购买群组的帐户

>[!NOTE]
>
>如果您已有10个数据流，则无法创建另一个数据流。 如果达到最大数量，请先删除Experience Platform中的一个，然后再在Journey Optimizer B2B版本中创建一个新版本。

1. 在Journey Optimizer B2B版本中，在左侧导航中转到&#x200B;**[!UICONTROL 帐户]** > **[!UICONTROL 购买群组]**。

1. 选择&#x200B;**[!UICONTROL 浏览]**&#x200B;选项卡。

1. 单击右上方的&#x200B;**[!UICONTROL 激活到LinkedIn目标]**。

   ![编辑帐户详细信息](./assets/activate-linkedin-destination.png){width="800" zoomable="yes"}

1. 为数据流提供描述性名称和描述（可选）。

   保存后，为数据流指定的名称将带有&#x200B;_AJOB2B_&#x200B;前缀，以便帮助识别Experience Platform中的数据流。

1. 输入LinkedIn Campaign Manager帐户](https://www.linkedin.com/help/lms/answer/a424270)的[帐户ID。

   您可以在Campaign Manager UI中按帐户名称查找帐户ID。

   ![添加数据流详细信息](./assets/destinations-linkedin-activate-details.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 选择购买群体过滤器]**&#x200B;并定义帐户受众的参数。

   >[!IMPORTANT]
   >
   >目前，在激活数据流后无法编辑过滤器。 在激活数据流之前，请仔细检查您的工作。

   ![根据购买群体指定帐户受众筛选](./assets/destinations-linkedin-activate-buying-group-filters.png){width="400"}

   对于&#x200B;**[!UICONTROL 参与度分数]**，运算符`Between`是包含的，百分比范围也是。 例如，5.1和5都是介于&#x200B;_5和6之间的_。

   空条件将被视为`Is Any`。

   单击&#x200B;**[!UICONTROL 保存]**&#x200B;以添加指定的筛选器。

1. 单击&#x200B;**[!UICONTROL 选择LinkedIn目标]**，然后选择要使用的已配置LinkedIn目标。

   激活时，此设置使用目标配置和相应的虚拟区段创建数据流。

1. 双击设置，然后单击右上方的&#x200B;**[!UICONTROL 激活]**。

   在确认对话框中再次单击&#x200B;**[!UICONTROL 激活]**。

   此时会显示一个横幅，其中包含指向Experience Platform中的数据流菜单的链接，以便您查看数据流记录。