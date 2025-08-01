---
title: 购买群组
description: 了解 Journey Optimizer B2B Edition 中的购买群组如何通过为您的帐户列表识别和定向成员来提高营销效果。
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: ada98f505aad848f958cf8325ed90d66692a6cac
workflow-type: ht
source-wordcount: '2151'
ht-degree: 100%

---


# 购买群组

对于 B2B 销售和营销活动，帐户是任何策略的关键。每个帐户都有一组与之相关联的人员，这些人员可能是该帐户的员工，也可能是与该帐户合作的承包商。帐户具有层级结构，不同的产品可能在不同的层级销售。如，Adobe Experience Platform 可能以公司级别出售给某个顶级帐户。Adobe Photoshop 可能出售给代表组织内某个部门的帐户，例如某个较大公司的设计部门。

![帐户角色图表](assets/account-roles-diagram.png){width="800"}

在帐户中，其中的一部分人员可能会组成&#x200B;_购买群组_。这些人员最终做出购买决策，因此需要营销人员给予特别关注，并向他们提供与该帐户其他相关人员不同的信息。购买群组可能由负责不同产品线或产品的不同人员组成。例如，网络安全产品通常需要首席信息官或首席安全官以及法律部门的代表批准购买。错误跟踪产品通常可能需要购买群组的成员中有一位工程副总裁和一位 IT 总监。

![视频](../../assets/do-not-localize/icon-video.svg){width="30"} [观看视频概述](#overview-video)

## 关键组件

您可以在 Journey Optimizer B2B Edition 中建立购买群组，根据您的销售团队负责销售的解决方案来确定目标帐户列表中有哪些成员，从而提高营销效果。在您和您的营销团队开始创建购买群组之前，请先确保您已定义了关键组件。这些组件对于实现您的业务目标和目的至关重要。

| 组件 | 用途 |
| --------- | ------- |
| 解决方案兴趣 | 该组件回答以下问题： <ul><li>作为营销组织，您销售什么？</li><li>您定位销售哪种产品或产品系列？</li></ul>  **_示例:_** 向现有客户交叉销售新产品 X |
| 帐户受众 | 该组件回答以下问题： <ul><li>您要向谁销售？</li><li>您将哪个帐户列表选为目标市场？</li></ul> **_示例:_** 通过产品 Y 收入超过 100 万的帐户所定义的帐户区段 |
| 购买群组角色模板 | 该组件回答以下问题： <ul><li>您将哪些角色选为目标？</li><li>使用哪套规则来确定谁被分配购买群组角色？</li></ul>  **_示例:_** 给某个 CMO 职位的人员分配决策者角色 |
| 购买群组阶段 | （可选）该组件回答以下问题：购买群组跟踪是成功还是失败？ |

## 成员分配

有三种方式可以将成员分配到购买群组或从购买群组中删除。下表按优先顺序列出了这些添加和删除方法。排在最前面的方法具有最高优先级，后面的方法不能覆盖它。

1. **_手动操作_** - 一名销售用户为购买群组执行的手动添加成员或移除成员的操作
2. **_旅程行动_**  - [购买群组成员资格的旅程行动节点](../journeys/action-nodes.md#add-a-people-based-action)（_分配到购买群组_&#x200B;或&#x200B;_从购买群组中移除_）
3. **_系统工作_**  - 购买群组[创建](../buying-groups/buying-groups-create.md#buying-group-creation-jobs)和维护工作。

为了确保购买群组中的成员分配不被错误覆盖，此列表按照系统中的优先顺序排列，以确保准确分配成员。例如，当一名销售用户手动将成员添加到购买群组时，他们不希望因维护工作而改变这一添加操作。使用优先顺序时强制执行以下场景：

* 如果用户手动将某个成员分配到某个购买群组，而购买群组维护工作随后又会将该成员从此群组中移除，那么此维护工作&#x200B;**不会移除**&#x200B;该成员，也无法覆盖手动分配操作。
* 如果用户手动将成员分配给购买群组，而随后触发的旅程节点会将此成员从购买群组中移除，那么此节点行动&#x200B;**不会移除**&#x200B;该成员，并且无法覆盖手动分配操作。
* 如果触发的旅程行动节点将某个成员添加到购买群组，而随后进行的购买群组维护工作会从此群组中移除该成员，那么此维护工作&#x200B;**不会删除**&#x200B;该成员，也无法覆盖旅程行动分配操作。

## 购买群组工作流

1. 创建购买群组。

   * 定义[解决方案兴趣](./solution-interests.md)和[角色模板](./buying-groups-role-templates.md)
   * [创建购买群组](./buying-groups-create.md#create-buying-groups)并分配[购买群组阶段](./buying-group-stages.md)。

1. 通过完整性来识别缺失人员。

   使用过滤器分析购买群组。

   **_示例:_** 决策者角色缺失，完整性评分 &lt; 50

1. 完成购买群组定义。
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. 将购买群组行动添加到您的帐户旅程中。

## 查看购买群组和组件

在左侧导航栏中展开&#x200B;**[!UICONTROL 帐户]**，然后单击&#x200B;**[!UICONTROL 购买群组]**。

_[!UICONTROL 购买群组]_&#x200B;页面分成若干选项卡：

| 选项卡 | 描述 |
| --- | ----------- |
| [!UICONTROL 概述] | 这是默认选项卡，显示[购买群组仪表板](../dashboards/buying-groups-dashboard.md)。 |
| [!UICONTROL 浏览] | 此选项卡支持以下活动： <ul><li>查看现有购买群组列表。 </li><li>按购买群组名称搜索。 </li><li>按解决方案兴趣筛选。 </li><li>深入了解购买群组详细信息。 </li><li>创建购买群组。 </li></ul> |
| [!UICONTROL 解决方案兴趣] | 此选项卡支持以下活动： <ul><li>查看现有购买群组列表。 </li><li>按购买群组名称搜索。 </li><li>访问并编辑解决方案兴趣属性。 </li><li>创建解决方案兴趣。 </li><li>删除解决方案兴趣。 </li><li>查看并删除购买群组任务。 </li></ul> |
| [!UICONTROL 角色模板] | 此选项卡支持以下活动： <ul><li>查看现有角色模板的列表。 </li><li>按角色模板名称搜索。 </li><li>访问并编辑角色模板属性和条件。 </li><li>创建角色模板。 </li><li>删除角色模板。 </li></ul> |
| [!UICONTROL 阶段] | 此选项卡支持以下活动： <ul><li>查看现有的购买群组阶段模型。 </li><li>访问并编辑购买群组阶段模型草稿。 </li><li>创建购买群组阶段模型。 </li></ul> |

## 购买群组搜索和过滤

使用&#x200B;_[!UICONTROL 浏览]_&#x200B;选项卡可查看购买群组列表。您可以按名称搜索，并按解决方案兴趣筛选列表。

![购买群组浏览页面](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## 购买群组详细信息

要访问购买群组的详细信息，请在&#x200B;_[!UICONTROL 浏览]_&#x200B;选项卡中单击购买群组名称。[了解详情](./buying-group-details.md)

![购买群组详细信息](assets/buying-group-details.png){width="600" zoomable="yes"}

### 购买群组完整性评分

完整性评分用于确定购买群组是否完整，这意味着它已为正确的成员分配了角色，并准备好用于帐户历程。该评分是根据购买群组内的角色数量以及至少分配了一个潜在客户的角色的数量得出的百分比。

例如，如果购买群组内有四个角色，其中三个角色分配了至少一个潜在客户，那么购买群组就完成了 75%。

每次创建或更新购买群组时都会重新计算购买群组完整性评分。

### 购买群组参与度评分

购买群组参与度评分用于根据购买群组成员所执行的活动来确定购买群组成员参与度。

* 购买群组生成后，就开始计算参与度评分。
* 购买群组成员在过去 30 天内执行的任何入站活动都用于计算该评分。
* 随着 30 天期限以及活动的到期，评分可能会下降。
* 每项活动的每日频率上限为 20 次。如果购买群组的成员每天执行相同活动超过 20 次，则该活动计数上限为 20，而不会更高。
* 评分四舍五入后显示。例如，评分 75.89999 显示为 76。

+++ 用于评分的活动

| 活动名称 | 描述 | 参与类型 | 每日最大频率计数 | 活动权重 |
| --- | --- | --- | --- | --- |
| [!UICONTROL 访问网页] | 成员访问某个网页 | Web | 20 | 40 |
| [!UICONTROL 填写表单] | 成员在某个网页上填写并提交一份表单 | Web | 20 | 40 |
| [!UICONTROL 单击链接] | 成员点击网页上的某个链接 | Web | 20 | 40 |
| [!UICONTROL 打开电子邮件] | 成员打开一个电子邮件 | 电子邮件 | 20 | 30 |
| [!UICONTROL 点击电子邮件] | 成员点击电子邮件中的链接 | 电子邮件 | 20 | 30 |
| [!UICONTROL 打开销售电子邮件] | 成员打开销售电子邮件 | 电子邮件 | 20 | 30 |
| [!UICONTROL 点击销售电子邮件] | 成员点击销售电子邮件中的链接 | 电子邮件 | 20 | 30 |
| [!UICONTROL 有趣的时刻] | 成员有一个有趣的时刻 | 策划的 | 20 | 60 |
| [!UICONTROL 点击推送通知] | 成员收到一个推送通知 | 移动设备 | 20 | 30 |
| [!UICONTROL 移动设备应用程序活动] | 成员在移动设备应用程序上执行某个活动 | 移动设备 | 20 | 30 |
| [!UICONTROL 移动设备应用程序会话] | 成员在某个移动设备应用程序会话中处于活跃状态 | 移动设备 | 20 | 30 |
| [!UICONTROL 填写 Facebook 潜在客户广告表单] | 成员在 Facebook 页面上填写并提交潜在客户广告表单 | 社交 | 20 | 30 |
| [!UICONTROL 点击 RTP 行动号召] | 成员点击某个个性化行动号召 | Web | 20 | 60 |
| [!UICONTROL 查看应用程序内消息] | 成员查看一个应用程序内消息 | 移动设备 | 20 | 30 |
| [!UICONTROL 点击应用程序内消息] | 成员点击一个应用程序内消息 | 移动设备 | 20 | 30 |
| [!UICONTROL 订阅短信] | 成员订阅短信通信 | 短信 | 20 | 90 |
| [!UICONTROL 回复销售电子邮件] | 成员回复销售电子邮件 | 电子邮件 | 20 | 30 |
| [!UICONTROL 参与了对话] | 成员参与 Dynamic Chat 对话 | 聊天 | 20 | 90 |
| [!UICONTROL 在对话中与文档交互] | 成员在 Dynamic Chat 对话中与文档进行交互 | 聊天 | 20 | 90 |
| [!UICONTROL 在对话中安排了会议] | 成员在 Dynamic Chat 对话中预约了会议 | 聊天 | 20 | 90 |
| [!UICONTROL 达成了对话目标] | 成员在 Dynamic Chat 对话中达成某个目标 |  | 20 | 90 |
| [!UICONTROL 回复了网络研讨会中的轮询] | 成员回复网络研讨会活动中的轮询 | 聊天 | 20 | 90 |
| [!UICONTROL 点击了网络研讨会中的行动号召] | 成员点击网络研讨会活动中的行动号召链接 | 号召 | 20 | 30 |
| [!UICONTROL 网络研讨会中资产下载] | 成员在网络研讨会活动中下载文件/资产 | 活动 | 20 | 60 |
| [!UICONTROL 在网络研讨会中提问] | 成员在网络研讨会活动中提问 | 活动 | 20 | 60 |
| [!UICONTROL 参与了活动] | 成员参加了某个活动 | 活动 | 20 | 60 |
| [!UICONTROL 在对话中与代理进行了互动] | 成员在 Dynamic Chat 对话中与代理进行互动 | 聊天 | 20 | 90 |
| [!UICONTROL 点击了对话聊天中的链接] | 成员点击 Dynamic Chat 对话中的链接 | 聊天 | 20 | 90 |
| [!UICONTROL 参与了会话流] | 成员参与 Dynamic Chat 会话流 | 聊天 | 20 | 90 |
| [!UICONTROL 已在会话流中计划会议] | 成员在 Dynamic Chat 会话流中预约了会议 | 聊天 | 20 | 90 |
| [!UICONTROL 达到了会话流目标] | 成员在 Dynamic Chat 会话流中达到目标 | 聊天 | 20 | 90 |
| [!UICONTROL 在会话流中与文档交互] | 成员在 Dynamic Chat 会话流中与文档进行交互 | 聊天 | 20 | 90 |
| [!UICONTROL 在会话流中与代理进行了互动] | 成员在 Dynamic Chat 会话流中与代理进行互动 | 聊天 | 20 | 90 |
| [!UICONTROL 点击了会话流聊天中的链接] | 成员点击 Dynamic Chat 会话流中的链接 | 聊天 | 20 | 90 |
| [!UICONTROL 点击短信 V2 中的链接] | 成员点击短信中的链接 | 短信 | 20 | 90 |

>[!NOTE]
>
>参与度评分活动记录在[个人的 Marketo Engage 活动日志](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"}中。

+++

#### 权重

用户可以为角色模板中的每个角色分配&#x200B;_权重_，通过为角色分配不同的权重来计算参与度评分。

![设置角色模板中每个角色的权重](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

每个权重级别都转换为一个值，用于计算参与度评分：

* [!UICONTROL 不重要] = 20
* [!UICONTROL 轻微] = 40
* [!UICONTROL 普通] = 60
* [!UICONTROL 重要] = 80
* [!UICONTROL 必不可少] = 100

角色模板中的三个角色权重分别为&#x200B;_[!UICONTROL 必不可少]_、_[!UICONTROL 重要]_&#x200B;和&#x200B;_[!UICONTROL 普通]_，转化为以下权重百分比：

| 角色 | 权重 | 系统值 | 值计算 | 百分比 |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| 决策者 | 必不可少 | 100 | 100/240 | 41.67% |
| 影响者 | 重要 | 80 | 80/240 | 33.33% |
| 业务员 | 普通 | 60 | 60/240 | 25% |
|               | 总计 | 240 |                   |           |

#### 计算示例

下面的示例说明了参与度评分的计算方法，其中使用了上面概述的角色权重百分比、购买群组中每个成员的入站活动计数，以及每个活动每日 20 次的计数上限（如果该活动发生多次）。

| 角色 | 成员 | 活动类型 | 昨日计数 | 今日计数 | 计算 | 总评分 |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| 决策者 | Adam | 访问了网站 | 37 | 15 | 20 + 15 | 35 |
|               |          | 点击了电子邮件 | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | 标记 | 访问了网站 | 5 | 3 | 5 + 3 | 8 |
|               |          | 点击了电子邮件 | 1 | 1 | 1 + 1 | 2 |
|               |          | 下载了发布 | 3 | 2 | 3 + 2 | 5 |
| **决策者总评分** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| 影响者 | John | 访问了网站 | 19 | 9 | 19 + 9 | 28 |
| **影响者总评分** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| 业务员 | Bob | 点击了电子邮件 | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | 点击了电子邮件 | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | 点击了电子邮件 | 1 | 1 | 1 + 1 | 2 |
|               |          | 访问了网站 | 1 | 7 | 1 + 7 | 8 |
|               |          | 下载了发布 | 1 | 2 | 1 + 2 | 3 |
| **业务员总评分** |         |             |                 |             |      | **17** |

最终参与度评分是通过应用每个角色评分的权重计算得出的：

| 角色 | 角色总评分 | 角色权重 % | 评分 X 权重 % |
|-------------- |---------------- |------------- |---------------- |
| 决策者 | 52 | 41.67% | 21.67 |
| 影响者 | 28 | 33.33% | 9.33 |
| 业务员 | 17 | 25% | 4.25 |
| **最终参与度评分** |                |             | **35.25** |

## 概述视频

>[!VIDEO](https://video.tv.adobe.com/v/3452950/?learn=on&captions=chi_hans)
