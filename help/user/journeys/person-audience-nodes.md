---
title: 人员受众节点
description: 使用区段或基于事件的受众配置人员受众节点，以在Journey Optimizer B2B edition中为目标编排定义人员历程入口点。
feature: Audiences
role: User
badgeBeta: label="Beta 版" type="informative" tooltip="此功能当前为有限测试版"
source-git-commit: f5170767a6df14874fab5de203264a5a5e3e245a
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# 人员受众历程节点

_人员受众_&#x200B;节点指定哪些人员配置文件进入历程。 当您[创建人员历程](./create-publish-journey.md#create-a-journey)时，该历程始终以定义其输入的人员受众节点开始。 人员受众节点可以具有以下两种受众输入类型之一：CDP区段或基于事件的成员资格。 无法组合区段定义和基于事件的受众定义。

为人员受众历程节点使用以下输入选项之一：

* **个人资料受众** — 使用CDP中定义的区段受众。 所有符合受众资格的用户档案都将作为成员添加到历程。 在每天[用户档案摄取](#profile-ingestion)任务期间，区段的新资格用户档案会添加到历程中。 如果配置文件不再符合该区段的条件，则它&#x200B;**_不_**&#x200B;从历程中删除。

* **事件受众** — 使用符合条件的事件来定义受众。 这些事件是在节点配置中定义的，必须使用在管理设置[中配置的](../admin/configure-aep-events.md)XDM事件。 基于事件的受众成员资格支持最多10个事件。 用户档案在其用户档案接受的第一个匹配事件之后，立即符合历程的条件。

  >[!NOTE]
  >
  >事件不能与配置文件属性结合使用，以缩小受众定义的范围。 计划在未来版本中针对此限制进行改进。

## 轮廓摄取

在Journey Optimizer B2B edition中，夜间受众摄取任务可使配置文件与Experience Platform保持同步。 虽然基于事件的人员历程可以确定不属于由Journey Optimizer B2B edition摄取/使用的配置文件或帐户受众的用户档案，但这会导致摄取的配置文件保持陈旧，除非它们属于由人员历程、帐户历程或购买团体使用的受众。 如果摄取某个配置文件后将其添加到受众，则会执行配置文件拼接，并且该配置文件会与Experience Platform保持同步。 计划在未来版本中改进此配置文件数据同步。

基于事件的人员历程摄取的新创建的用户档案在摄取时可能没有更新的用户档案信息。 例如，如果配置文件通过表单填写事件创建，并且人员历程从符合条件的表单填写事件中摄取它们，则表单中提交的数据可能尚未在历程摄取时同步到配置文件。 结果可能是用于个性化的数据不完整（如电子邮件内容中的数据）。 计划在未来版本中改进此配置文件事件数据同步。

基于事件的人员历程可使仍为匿名/没有电子邮件地址且仅包含ECID的用户档案符合条件。 当具有网页活动的资格逻辑时，最常发生这种情况。 如果符合条件的配置文件过多，则过于宽泛的基于事件的受众逻辑可能会导致实例达到4,000万个配置文件上限。 限制受众的可能范围以防止出现这种情况。

>[!IMPORTANT]
>
>在当前的测试版计划中，人员历程的理想用途是仅限定您还在帐户历程和购买组定义中定位的用户档案。 此用法可确保完整的配置文件与Experience Platform保持同步。

## 设置人员受众节点的受众

1. 单击&#x200B;**[!UICONTROL 人员受众]**&#x200B;节点。

   此操作在右侧显示节点属性。

   ![人员受众历程节点](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"}

1. 选择进入历程的人员输入类型：

   * **[!UICONTROL 个人资料受众]**

     选择&#x200B;_[!UICONTROL 个人资料受众]_&#x200B;选项。 然后，单击&#x200B;**[!UICONTROL 添加配置文件受众]**。

     在&#x200B;_[!UICONTROL 添加受众]_&#x200B;对话框中，选择之前创建的受众区段。 然后，单击&#x200B;**[!UICONTROL 添加受众]**。

     ![选择节点的配置文件受众](./assets/node-person-audience-add-audience-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL 活动受众]**

     选择&#x200B;_[!UICONTROL 事件受众]_&#x200B;选项。 然后，单击&#x200B;**[!UICONTROL 添加事件条件]**。

     在&#x200B;_[!UICONTROL 编辑事件标准]_&#x200B;对话框中，添加一个或多个要用于受众成员资格的事件。 对于您添加的每个事件，单击&#x200B;**[!UICONTROL 添加约束]**&#x200B;以选择匹配的事件属性。 设置要用于匹配的评估。 您可以添加多个约束以匹配事件。

     ![添加事件并匹配条件以确定人员配置文件](./assets/node-person-audience-edit-event-criteria-dialog.png){width="700" zoomable="yes"}

     定义事件条件后，单击&#x200B;**[!UICONTROL 保存]**。

     有关历程支持事件的配置的详细信息，请参阅[管理体验事件](../admin/configure-aep-events.md#manage-experience-events)。
