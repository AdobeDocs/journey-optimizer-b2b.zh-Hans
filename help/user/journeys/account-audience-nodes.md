---
title: 帐户受众节点
description: 了解可用于在Journey Optimizer B2B edition中定义帐户历程输入的帐户受众节点类型。
feature: Account Journeys, Audiences, Account Lists
role: User
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 5%

---

# 帐户受众历程节点

帐户受众节点定义历程的输入帐户。 当您[创建帐户历程](./journey-overview.md#create-an-account-journey)时，它始终以定义历程输入的&#x200B;_帐户受众_&#x200B;节点开头。

有两种类型的输入可用于此节点：

* **[帐户受众](../audiences/account-audience-overview.md)** — 这是从Experience Platform分段服务同步的基本受众。
* **[帐户列表](../accounts/account-lists.md)** — 这是命名帐户的集合，可用于目标历程编排。 帐户根据定义的条件（如行业、位置或公司规模）列出指定帐户的目标。

_设置节点的受众：_

1. 单击&#x200B;**[!UICONTROL 帐户受众]**&#x200B;节点可在右侧显示节点属性。

   ![帐户受众节点](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. 选择要输入历程的帐户的输入类型：

   * **[!UICONTROL 帐户受众]**

     选择此类型，然后单击&#x200B;**[!UICONTROL 添加帐户受众]**。

     在&#x200B;_[!UICONTROL 添加受众]_&#x200B;对话框中，选择之前创建的受众区段，然后单击&#x200B;**[!UICONTROL 添加受众]**。

     ![为节点选择一个受众区段](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL 帐户列表]**

     选择此类型，然后单击&#x200B;**[!UICONTROL 添加帐户列表]**。

     在&#x200B;_[!UICONTROL 选择实时帐户列表]_&#x200B;对话框中，选择之前发布的帐户列表，然后单击&#x200B;**[!UICONTROL 保存]**。

     ![为节点选择实时帐户列表](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     请转到[帐户列表](../accounts/account-lists.md)，了解有关创建和发布帐户列表的详细信息。

_创建受众区段：_

1. 在左侧导航栏中，选择&#x200B;**[!UICONTROL 帐户]** > **[!UICONTROL 受众]**。

1. 单击右上角的&#x200B;**[!UICONTROL 创建受众]**。

   ![创建受众区段](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. 按照[分段服务指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"}中所述的步骤操作。
