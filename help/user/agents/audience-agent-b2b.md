---
title: B2B帐户和人员的受众技能
description: 了解B2B帐户和人员的受众技能。 探索产品意图、识别角色、评估角色覆盖范围并创建购买组模板。
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
autotag-review: '2026-06-05T16:43:42.459Z'
TQID: 'https://experienceleague.adobe.com/d7KMYbH0NpoYGnBdTCmCpzLgpGIYfNP-YIFCQUjZpIg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
    internal-label: AI Assistant
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
    internal-label: Agentic AI
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
    internal-label: Taxonomy
source-git-commit: ce5504e7a539c38b489fddc103358029edf1cfba
workflow-type: tm+mt
source-wordcount: '1692'
ht-degree: 1%
---
# B2B帐户和人员的受众技能

在[!DNL CX Coworker]界面中为B2B使用受众技能。 探索客户和人员之间的产品意图。 识别相关角色，评估购买团体覆盖范围，并创建购买团体角色模板。

* 评估客户对特定产品的兴趣并比较意图趋势。
* 确定与产品兴趣相关的人员和角色。
* 审查购买团体角色并确定覆盖范围差距。
* 生成并优化购买团体角色模板。

>[!PREREQUISITES]
>
>在为B2B帐户和人员使用受众技能之前，请配置以下数据定义和映射：
>
>* [意图数据分类和映射](../admin/intent-data.md)
>* [XDM字段映射](#xdm-data-prerequisites)

单击应用程序顶部的&#x200B;_询问[!DNL Coworker]_ （![询问[!DNL Coworker]](../assets/do-not-localize/icon-ask-coworker.svg) ）图标以打开[!DNL Coworker]应用程序。 在聊天界面中输入您的自然语言提示。

![ [!DNL CX Coworker]](./assets/audience-skills-prompt.png){width="800" zoomable="yes"}中的受众提示

## 受众技能关注领域

使用以受众技能为中心的领域来探索客户意图、了解人员和角色并准备购买组模板。

| Focus | 任务 |
| ----- | ----- |
| 帐户意图 | 使用低、中、高意图级别评估特定产品的客户意图。 比较一段时间内产品兴趣的趋势，并确定对特定产品感兴趣的客户。 与角色覆盖范围一起查看参与模式。 |
| 人员和角色 | 按产品意图识别一个或多个产品中的角色并进行排名。 查看机会量度，包括获胜率、会员资格率和计数。 将角色映射到&#x200B;_冠军_、_决策者_&#x200B;和&#x200B;_影响者_&#x200B;等角色，并查看角色分配的说明。 |
| 购买团体保险 | 评估跨帐户的购买组大小和角色覆盖率。 查看角色分配并识别缺少的一个或多个角色。 查找在最近交易中被确认有拥护者的客户。 |
| 购买组模板 | 为特定产品生成购买组角色模板，并查看建议的角色映射。 通过包含或排除角色和角色来优化模板。 在创建购买组之前验证所需的角色。 |

## 限制

受众分析取决于配置的意图分类、XDM字段映射和体验事件数据。 机会数据不完整、分类缺失或过时，或者配置文件和帐户标识符缺失可能会降低insight的可靠性。

意图计算仅使用以下体验事件： `directMarketing.emailClicked`、`directMarketing.emailOpened`、`directMarketing.emailUnsubscribed`和`web.webpagedetails.pageViews`。

## 提示示例

在[!DNL CX Coworker]界面中输入以下提示以探索客户意图、了解人员和角色并准备购买组模板。

### 帐户意图

探索客户对产品的兴趣并审查意图的变化。

* 显示趋势窗口：每个产品帐户产品意向的最早和最新更新。
* 哪些客户对任何产品的意图都不高，但仍存在开放机会（值得培养）？
* 本周为`<account_name>`记录了哪些新的意图信号？

### 人员和角色

识别与产品兴趣相关的角色，并查看推荐的购买团体角色。

* 显示与`<product>`关联的角色。
* 为我显示`<product>`的角色到角色映射推荐。
* 对于`<product>`，列出角色及其机会量度（获胜率、会员资格率、计数）。

### 购买组和模板

审查购买群组意图和覆盖范围，然后生成或优化模板。

* 对于`<product>`，列出具有产品意向和得分的购买组。
* 对于`<industry>`中的帐户，`<product>`的平均帐户角色覆盖率是多少？
* 为`<product>`创建购买组模板。
* 为不带`<persona>`角色的`<product>`创建购买组模板并删除`<role>`角色。

## 概念

使用这些概念来解释帐户意图、角色排名和购买团体推荐。

| 概念 | 解释 |
| ------- | ----------- |
| 受众检测 | 分析客户中跨人员的第一方参与信号，以确定产品兴趣和相关角色。 该分析会考虑过去18个月的活动，包括商机结束前的活动。 当Opportunity数据不完整时，参与模式可指示产品意图，但缺少数据可能会降低insight的可靠性。 |
| 用户画像 | 角色按标准化的职务、职能和资历对人员分组。 使用角色了解客户中的参与者，包括决策者、影响者和支持角色。 |
| 映射购买组角色 | 根据职务、职能、资历和配置的属性，将角色映射到产品特定的购买群组角色。 这些角色表示客户中影响购买或做出购买决定的人员。 查看范围以确定缺少的角色。 |
| 角色排名的机会数据 | Opportunity阶段、结束日期以及opportunity-to-product映射支持每个产品的角色排名。 当机会数据不完整时，排名会使用活动量和时间衰减为最近活动赋予更大的权重。<br/><br/>产品链接使用提供的或生成的机会到产品映射表（如果可用）。 否则，模糊匹配会将机会链接到产品。 如果没有可用的链接，则从商机结束日期之前的最近活动推断产品意图。 这些回退方法无法消除不完整数据的可靠性限制。 |
| 机会分析 | 历史机会分析使用三个维度来确定与购买结果关联的角色模式：<ul><li>获胜率：测量在涉及特定角色时赢得机会的频率。 与较高获胜率关联的角色模式将获得更多权重。</li><li>会员资格率：衡量角色在给定产品的商机中出现的频率。</li><li>角色影响：衡量角色参与或活动与获胜次数的关联方式，但前提是角色是否存在。</li></ul>这些信号告知客户意图、角色映射和购买团体推荐。 |
| 意图 | 意图通过参与指示产品兴趣，例如网页访问或电子邮件链接点击。 产品分类将参与活动与关键字、产品和产品类别相关联。 参与深度和频率决定了每个关键词、产品或产品类别的单个意图分数。<br/><br/>分数表示兴趣强度：低意图： `<=0.2`，Medium意图： `0.2 < score <= 0.6`，高意图： `0.6 < score <= 1`。<br/><br/>个人意图分数通过汇总同一帐户中的人员来确定帐户意图。 |
| 影响购买群组的角色 | 购买团体角色对购买决策有不同的贡献。 _决策者_&#x200B;通常控制预算审批。 _影响者_&#x200B;形状评估和建议。 _拥护者_&#x200B;建立内部共识。 _最终用户_&#x200B;验证产品是否适合。<br/><br/>审查角色分配和覆盖范围，以了解哪些人会影响决策以及在哪些情况下仍然存在参与度差距。 |
| 角色或角色覆盖范围 | 覆盖范围衡量一个帐户中至少有一个代表的预期角色或角色的数量。 对于具有&#x200B;_N_&#x200B;个预期角色或角色的产品，完全覆盖意味着所有&#x200B;_N_&#x200B;都表示出来。 部分覆盖意味着部分内容缺失。 使用覆盖范围来评估购买群组的完整性和找出差距。 |

## XDM数据先决条件

配置以下XDM字段映射以支持帐户意图分析、角色标识和购买组角色映射。

### XDM字段映射

<table>
  <tbody>
    <tr>
      <th>XDM字段</th>
      <th>实体</th>
      <th>业务定义</th>
      <th>其他详细信息</th>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>轮廓</span>
        </p>
      </td>
      <td>帐户标识符，用于连接机会、事件和意图数据</td>
      <td rowspan="2">机会分析<br/>帐户探索<br/>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.personKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>轮廓</span>
        </p>
      </td>
      <td>人员标识符，在涉及事件数据和个人资料数据的连接中使用</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extendedWorkDetails.departments</span>
        </p>
      </td>
      <td>
        <p>
          <span>配置文件</span>
        </p>
      </td>
      <td>用户档案/人员的工作部门</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>角色映射</p>
      </td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>extendedWorkDetails.jobTitle</span>
        </p>
      </td>
      <td>
        <p>
          <span>配置文件</span>
        </p>
      </td>
      <td>角色计算中使用的配置文件/人员的工作标题</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>person.name.firstName</span>
        </p>
      </td>
      <td>
        <p>
          <span >轮廓</span>
        </p>
      </td>
      <td>在匹配查询的结果中显示人员的名字。</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.fullName</span>
        </p>
      </td>
      <td>
        <p>
          <span>配置文件</span>
        </p>
      </td>
      <td>在匹配查询的结果中显示人员的全名。</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.lastName</span>
        </p>
      </td>
      <td>
        <p>
          <span>配置文件</span>
        </p>
      </td>
      <td>在匹配查询的结果中显示人员的姓氏。</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>帐户</span>
        </p>
      </td>
      <td>帐户标识符，用于连接机会、事件和意图数据</td>
      <td>机会分析<br/>帐户探索</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>帐户名称</span>
        </p>
      </td>
      <td>
        <p>
          <span>帐户</span>
        </p>
      </td>
      <td>在匹配查询的结果中显示帐户名称。</td>
      <td rowspan="4">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>帐户探索</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>帐户</span>
        </p>
      </td>
      <td>支持根据您的查询按帐户描述进行帐户筛选。</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountOrganization.industry</span>
        </p>
      </td>
      <td>
        <p>
          <span>帐户</span>
        </p>
      </td>
      <td>支持根据您的查询按行业筛选帐户。</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountBillingAddress.region</span>
        </p>
      </td>
      <td>
        <p>
          <span>帐户</span>
        </p>
      </td>
      <td>支持根据您的查询按帐单地址区域进行帐户过滤。</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>机会</span>
        </p>
      </td>
      <td>帐户标识符，用于连接机会、事件和意图数据</td>
      <td rowspan="2">
        <p>机会分析<br/>帐户探索</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>机会</span>
        </p>
      </td>
      <td>机会标识符，用于帐户数据的联接</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityName</span>
        </p>
      </td>
      <td>
        <p>
          <span>个机会</span>
        </p>
      </td>
      <td>机会分析中使用的机会名称。</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>机会分析</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>isWon</span>
        </p>
      </td>
      <td>
        <p>
          <span>机会</span>
        </p>
      </td>
      <td>是否赢得了机会（二进制）</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>机会</span>
        </p>
      </td>
      <td>机会分析中使用的机会描述。</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityAmount</span>
        </p>
      </td>
      <td>
        <p>
          <span>机会</span>
        </p>
      </td>
      <td>机会涉及的金额$</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>opportunityType</span>
        </p>
      </td>
      <td>
        <p>
          <span>机会</span>
        </p>
      </td>
      <td>机会类型</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityStage</span>
        </p>
      </td>
      <td>
        <p>
          <span>个机会</span>
        </p>
      </td>
      <td>Opportunity阶段（已结束的赢家或输家，或任何中间阶段） </td>
      <td rowspan="4">
        <p>机会分析<br/>帐户探索</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>actualCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>机会</span>
        </p>
      </td>
      <td>机会的实际结束日期</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>expectedCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>个机会</span>
        </p>
      </td>
      <td>商机的预期关闭日期</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extSourceSystemAudit.createdDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>机会</span>
        </p>
      </td>
      <td>此机会的创建日期</td>
    </tr>
  </tbody>
</table>

### 分类数据

受众技能使用来自[!DNL Adobe Journey Optimizer B2B Edition]的第一方意图数据。 意图计算将产品分类与参与活动联系起来，并汇总帐户级别的各个得分。

1. 意图计算需要来自客户>分类的分类数据（客户产品和相应的关键词）
1. 分类数据用于标记事件数据（资产标记）。 此数据根据其事件数据>资产标签提供访客感兴趣的关键字和产品的见解 
1. 标记资产（事件数据）与访客行为（已访问页面数）相结合，以便在意图计算中确定关键字、产品和产品类别级别→访客意图
1. 访客配置文件级别的意图分数在帐户级别进行汇总，以确定给定关键字、产品和产品类别>意图帐户聚合中的帐户意图

除了[配置意图分类](../admin/intent-data.md)外，还需要以下字段：

<table>
  <tbody>
    <tr>
      <th>XDM字段</th>
      <th>实体</th>
      <th>业务定义</th>
    </tr>
    <tr>
      <th>
        <br/>
      </th>
      <th>
        <br/>
      </th>
      <td>人员配置文件</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.namespace.code<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>轮廓</span>
        </p>
      </td>
      <td>帮助识别人员（电子邮件或b2b_person）标识符</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.id
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>轮廓</span>
        </p>
      </td>
      <td>namespace_id</td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>keyword_id</li>
          <li>keyword_name</li>
          <li>product_id</li>
          <li>product_name</li>
          <li>product_category_id</li>
          <li>product_category_name</li>
        </ul>
      </td>
      <td>
        <p>
          <br/>
        </p>
      </td>
      <td>用作标记资产（体验事件，例如点击的电子邮件、访问的网页）的分类</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>时间戳</span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>用于获取回填和增量运行的时间</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>eventType</span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>标识事件类型。 意图计算仅使用<code>directMarketing.emailClicked</code>、<code>directMarketing.emailOpened</code>、<code>directMarketing.emailUnsubscribed</code>和<code>web.webpagedetails.pageViews</code>。
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingName</span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>仅供参考/记帐；有关营销活动名称的信息</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceID</span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>仅供参考/记帐；有关电子邮件所针对的源ID的信息</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>仅供参考/记帐；电子邮件所针对的源实例的信息</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>用于从[!DNL Adobe Marketo Engage]数据中心获取电子邮件内容。 它包括(SourceID@SourceInstanceID.SourceType)。</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceType<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>仅供参考/记帐；有关源的类型或源来自何处的信息 </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>有关网页访问源源的信息</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.name<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>用于获取内容的实际url</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.queryParameters</span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>用于获取目标内容的URL的其他查询参数 </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.isPersonalizedURL</span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>仅供参考/记账</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>仅供参考/记帐；有关电子邮件所针对的源ID的信息</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>体验活动</span>
        </p>
      </td>
      <td>仅供参考/记帐；有关电子邮件所针对的源实例的信息</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <span>体验活动</span>
      </td>
      <td>仅供参考/记帐；它由(SourceID@SourceInstanceID.SourceType)组成</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceType</span>
        </p>
      </td>
      <td>
        <span>体验活动</span>
      </td>
      <td>仅供参考/记帐；有关源类型或源来自何处的信息</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.URL</span>
        </p>
      </td>
      <td>
        <span>体验活动</span>
      </td>
      <td>用于在web.webPageDetails.name没有实际URL时获取该URL。</td>
    </tr>
  </tbody>
</table>
