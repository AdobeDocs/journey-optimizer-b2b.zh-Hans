---
title: XDM字段管理
description: 使用XDM字段管理可控制Journey Optimizer B2B edition可用的数据。
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta 版" type="informative" tooltip="此功能目前在简化架构上的有限测试版中发布"
source-git-commit: afac024e5eeb6b9d230c4292a6f37e92e16d29f6
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 1%

---


# XDM字段管理

体验数据模型(XDM)字段是向[!DNL Journey Optimizer B2B Edition]应用程序提供数据的架构元素。 将XDM字段用作历程节点、购买群组中的过滤器和限制条件，并用于内容功能，如电子邮件个性化和条件内容。

架构根据标准XDM类定义字段。 标准XDM类包括“个人资料”、“业务帐户”和“体验事件”。 关系架构还定义了一些字段，这些字段允许您以类似于传统关系数据库的方式对结构化数据进行建模。

Adobe Experience Platform (AEP)架构通常包含复杂层次结构中的许多字段。 遍历XDM架构树需要时间。 XDM字段管理通过仅显示与每个历程相关的字段而简化字段选择。 管理员控制向历程创建者显示的字段。 管理员还会将字段设置为只读或可编辑。 这些操作可在旅程设计期间提高效率。

了解XDM并与数据工程师或B2B客户数据平台(CDP)数据建模利益相关者进行协作的管理员应使用以下步骤为[!DNL Journey Optimizer B2B Edition]配置XDM类。

>[!NOTE]
>
>XDM字段管理适用于在[简化架构](../simplified-architecture.md)上配置的Journey Optimizer B2B edition环境。

## 访问XDM类

1. 在左侧导航中，选择&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 配置]**。

1. 单击中间面板上的&#x200B;**[!UICONTROL XDM类]**。

   * 使用&#x200B;**[!UICONTROL Standard]**&#x200B;和&#x200B;**[!UICONTROL Relational]**&#x200B;选项卡添加新字段并在Journey Optimizer B2B edition中提供。

   * 使用&#x200B;**事件**&#x200B;选项卡可[选择特定的AEP Experience Events及其关联字段](./configure-aep-events.md)以用于历程事件节点。

## 字段选择

>[!IMPORTANT]
>
>您可以通过选择新字段或取消选择不再需要的字段来随时更新字段选择。 使用此架构发布历程时，会锁定架构结构。 不支持删除或重命名架构、添加新字段或更改字段类型，这可能会导致历程失败。

使用以下指南进行字段选择：

* 仅当历程中主动使用架构后，您才可以添加新字段。
* 删除、重命名或更改字段类型可能会导致历程功能问题。 处理架构时要小心。
* 请勿重命名或删除架构，或修改关系架构中的键。

### 标准类

在&#x200B;_[!UICONTROL 标准]_&#x200B;选项卡中，您可以编辑标准类的&#x200B;_托管字段_&#x200B;和&#x200B;_可更新字段_：

* 受管字段显示在历程、购买群组和个性化功能中。
* 可更新字段用作&#x200B;_更新帐户配置文件_&#x200B;和&#x200B;_更新人员配置文件_&#x200B;历程节点的约束。

![显示XDM类配置的标准类选项卡](assets/xdm-standard.png){width="600" zoomable="yes"}

该列表包括两个类：

* **[!UICONTROL XDM 轮廓]**
* **[!UICONTROL XDM业务帐户]**

显示的类信息包括：

* 托管字段数
* 可更新字段数
* 上次更新时间

若要从标准XDM类的合并架构中选择字段，请单击类名以打开&#x200B;_托管字段_&#x200B;选择对话框，或单击&#x200B;_更多菜单_ (**...**)图标以在&#x200B;_[!UICONTROL 托管字段]_&#x200B;和&#x200B;_[!UICONTROL 可更新字段]_&#x200B;之间进行选择。

![单击“更多”菜单图标以在托管字段和可更新字段之间进行选择](./assets/xdm-classes-standard-more-menu.png){width="550" zoomable="yes"}

>[!NOTE]
>
>字段必须首先是&#x200B;_托管_，然后才能是&#x200B;_可更新_。 您选择的&#x200B;_可更新字段_&#x200B;必须存在于用户提供的架构中。 您的架构可能不包括必填字段，系统定义的字段除外。

#### 受管字段

选择&#x200B;**[!UICONTROL 托管字段]**&#x200B;时，_选择字段_&#x200B;对话框将列出所有可配置的字段。

1. 为每个XDM类最多选择100个字段。

   使用&#x200B;_[!UICONTROL 搜索]_&#x200B;字段按名称筛选显示的列表。 使用&#x200B;**[!UICONTROL 仅显示选定字段]**&#x200B;滑块查看当前选择。

   ![显示可配置字段选项的标准XDM类的托管字段选择对话框](assets/xdm-standard-managed-fields.png){width="450" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以确认您的选择。

#### 可更新字段

在配置可更新字段之前，它们必须驻留在自定义数据集中。 有关自定义数据集工作流的演练，请参阅[创建数据集并摄取数据](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data#){target="_blank"}，并使用&#x200B;**[!UICONTROL 从架构创建数据集]**&#x200B;选项。 此数据集用于隔离可更新字段。 所有可更新字段都必须在此数据集中。

>[!IMPORTANT]
>
>可更新字段的护栏：
>
>* 架构 — 在XDM Individual Profile类中，架构中的任何必填字段都必须由系统定义，如`identityMap`或`personID`。
>* 数据集 — 请勿将已使用的数据集用于其他目的。 作为最佳实践，请专门创建用于存储可更新字段的专用数据集。 为每个XDM类使用单独的数据集。

为个人资料创建数据集，并为企业帐户创建另一个数据集。 在配置过程中选择每个新数据集：

1. 对于&#x200B;**[!UICONTROL 数据集]**，请选择您创建的新数据源。

1. 从所选数据集中选择字段。

   ![用于从XDM架构配置中的数据集选择可更新字段的对话框](./assets/xdm-select-updateable.png){width="450" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以应用更改。

### 关系架构

关系架构允许您创建自定义数据类。 通过访问多个数据集，您可以创建专门针对您的数据需求定制的类。 在历程决策和电子邮件个性化中将关系架构用于业务实体，例如购买、许可和事件注册。 您最多可以选择50个架构，每个架构最多可以选择100个字段。

有关如何将所选字段用于高级电子邮件个性化的信息，请参阅[内容个性化](../content/personalization.md#custom-datasets)。 有关如何将所选字段用于历程决策（按帐户拆分路径）的信息，请参阅[自定义数据筛选](../journeys/split-merge-paths-nodes.md#custom-data-filtering)。<!-- add link to split path by people in M 1.5 GA release -->

>[!NOTE]
>
>[关系架构](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/schema/relational#)可作为[!DNL Journey Optimizer B2B Edition]的有限可用性版本使用。 Data Mirror和关系架构可供[!DNL Journey Optimizer Orchestrated Campaigns]许可证持有人使用。 关系架构也以受限版本形式提供给[!DNL Customer Journey Analytics]用户，具体取决于您的许可证和功能启用。 请联系您的Adobe代表以获取访问权限。

>[!NOTE]
>
>此功能当前支持与帐户相关的自定义对象用例，并计划在未来支持更多现成的对象用例。

您可以使用架构编辑器创建关系架构（在左侧导航中转到&#x200B;**[!UICONTROL 数据管理]** > **[!UICONTROL 架构]**）。

在创建用于[!DNL Journey Optimizer B2B Edition]的架构时，需要以下配置值：

* 行为：记录
* 分段：已启用
* 关系类型：多对一
* 引用架构：B2B帐户
* 必填字段：主键、外键和版本描述符
* 关联的数据集：已定义并映射到架构

要选择在[!DNL Journey Optimizer B2B Edition]中使用的关系架构字段，请执行以下操作：

1. 选择&#x200B;**[!UICONTROL 关系]**&#x200B;选项卡以查看您的架构。

   架构编辑器中的![关系架构选项卡显示Adobe Journey Optimizer B2B edition的业务实体字段](assets/xdm-relational.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 选择关系XDM架构]**。

   >[!NOTE]
   >
   >在此测试版功能中，仅支持&#x200B;_帐户多对一自定义对象_。

1. 选择关系架构并单击&#x200B;**[!UICONTROL 下一步]**。

   >[!NOTE]
   >
   >在此Beta版功能中，选择某个架构后，便无法从列表中删除该架构。

   ![在对话框中选择关系架构](./assets/xdm-classes-relational-select-schema-dialog.png){width="500" zoomable="yes"}

1. 输入命名空间或使用默认命名空间。 单击&#x200B;**[!UICONTROL 下一步]**。

   只能设置命名空间一次，并且无法撤消此操作。

   ![创建命名空间对话框中的默认命名空间](./assets/xdm-classes-relational-create-namespace.png){width="400" zoomable="yes"}

1. 查看关系架构字段。

   单击&#x200B;_信息_ ![信息图标](../assets/do-not-localize/icon-info-light.svg)图标以查看字段元数据。

1. 选择要为历程和个性化启用的字段。

   平台会自动选择以下必填字段：

   * 外键
   * 主键
   * 版本描述符

   使用&#x200B;_[!UICONTROL 搜索]_&#x200B;字段按名称筛选显示的列表。 使用&#x200B;**[!UICONTROL 仅显示选定字段]**&#x200B;滑块查看当前选择。

   ![在对话框中选择关系架构的字段](./assets/xdm-classes-relational-select-schema-fields.png){width="500" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 保存]**。
