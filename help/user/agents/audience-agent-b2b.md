---
title: Audience Agent B2B
description: Journey Optimizer B2B edition中的Audience Agent B2B使用意图分析和角色映射来创建购买组并加快B2B营销工作流程。
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
autotag-review: '2026-06-05T16:43:42.459Z'
TQID: 'https://experienceleague.adobe.com/d7KMYbH0NpoYGnBdTCmCpzLgpGIYfNP-YIFCQUjZpIg'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: afadf741-c5fe-42cd-8013-23bb6ff2d1bcid: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
subfeature_v2: id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
source-git-commit: b43117c1e47f698d62b29f56b4713ac776c497a0
workflow-type: tm+mt
source-wordcount: 2500
ht-degree: 1%

---

# Audience Agent B2B

Audience Agent B2B由[Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator)提供支持，在Journey Optimizer B2B edition中可用。 使用此代理提高了探索和扩展受众的效率和有效性，加快了购买组的创建速度，并且优化了历程激活的工作流程：

* **_按意图排列目标受众的优先级_**：根据各种受众的产品意图推断角色并简化活动规划，减少花费在受众验证上的时间。

* **_利用AI检测和创建购买组_**：使用AI、结构化、非结构化数据和统一的第一方数据来简化购买组的发现和创建。

处于全页模式的![Audience Agent B2B](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>要使用Audience Agent B2B，需要数据定义和映射：<br/>
>
>* [意图数据分类/映射](../admin/intent-data.md)
>* [XDM字段分类/映射](#xdm-data-prerequisites)

## Audience Agent B2B功能

| 面积 | 作用 | 商业价值 |
| ---- | ------------ | -------------- |
| 目的分析 | <li> 测量特定产品的帐户意图强度（例如低、中和高）。 <li>比较一段时间的产品兴趣趋势（例如过去&#x200B;_n_&#x200B;天排名最前的产品）。 <li>识别积极显示对特定产品感兴趣的客户。 <li>将帐户活动与角色覆盖相结合的表面参与模式。 | <li>帮助团队在适当的时间将精力集中在适当的客户上。 <li>通过优先处理具有真实购买信号的帐户，提高管道质量。 <li>在竞争对手采取行动之前实现主动参与。 |
| 人物角色映射 | <li>按产品意图检测和排名最前的角色。 <li>识别购买一个或多个产品所涉及的角色。 <li>将角色映射到功能角色（例如&#x200B;_冠军_、_决策者_&#x200B;和&#x200B;_影响者_），并提供理由。 <li>验证给定人员被视为冠军的原因。 | <li>确保销售团队与真正的决策者和影响者进行互动。 <li>减少在影响较小的联系人上浪费精力。 <li>通过使推广与买方力量动态保持一致，提高赢率。 |
| 购买团体评估 | <li>评估购买群组的大小（例如，成员超过&#x200B;_n_&#x200B;个的群组）。 <li>跨帐户度量角色覆盖率（例如，低于&#x200B;_x_%）。 <li>跟踪购买小组内的角色分配和覆盖缺口。 <li>突出显示在最近交易中表现出色客户的客户。 | <li>揭示可能会阻碍交易的覆盖缺口。 <li>通过确保完全角色表示来加强多线程策略。 <li>通过组级别的参与洞察来改进交易运行状况跟踪。 |
| 购买组创建和操作性 | <li>根据观察到的角色和角色模式，建议角色到角色的映射。 <li>为指定产品生成购买组角色模板。 <li>通过包含或排除特定角色和角色，支持模板自定义。 <li>在创建购买组之前验证是否定义了所需的角色。 | <li>减少手动操作和不完全购买组模板的风险。 <li>确保在创建角色之前验证角色覆盖范围，从而降低覆盖范围差距的风险。 <li>将分析见解转化为立即、可操作的后续步骤。 |

## 限制

Audience Agent B2B取决于配置的意图分类、XDM字段映射和体验事件数据。 当机会数据不完整、意图分类缺失或过期，或所需的配置文件和帐户标识符未映射时，分析的可信度会降低。 对于意图计算，代理仅处理这些体验事件： `directMarketing.emailClicked`、`directMarketing.emailOpened`、`directMarketing.emailUnsubscribed`和`web.webpagedetails.pageViews`。

## 提示示例

这些提示示例演示了可以使用代理的一些方法：

* 显示趋势窗口：每个产品帐户产品意向的最早和最新更新。
* 对于`<product>`，列出具有产品意向和得分的购买组。
* 对于`<product>`，列出角色及其机会量度（获胜率、会员资格率、计数）。
* 对于`<industry>`中的帐户，`<product>`的平均帐户角色覆盖率是多少？
* 哪些客户对任何产品的意图都不高，但仍存在开放机会（值得培养）？
* 哪些帐户本周为`<account_name>`添加了新意图信号？
* 显示与`<product>`关联的角色。
* 为我显示`<product>`的角色到角色映射推荐。
* 为`<product>`创建购买组模板。
* 为不带`<persona>`角色的`<product>`创建购买组模板并删除`<role>`角色。

## 概念

| 概念 | 解释 |
| ------- | ----------- |
| 受众检测 | 在幕后，经纪人根据两件事来审视第一方意图信号：人们与您的品牌之间的互动程度，以及他们代表的角色类型。 该分析回顾过去18个月的活动，以检测客户中每个人的产品意图，尤其是在商机结束前的这段时间。 此分析有助于代理突出显示最有可能影响交易的角色。<br/><br/>有时，客户并非所有业务机会数据都处于完美状态，这没什么问题，代理仍然可以完全根据参与模式检测产品意图。 |
| 用户画像 | 角色表示帐户中互动的人员类型。 代理通过查看职称、职能和资历级别来构建这些信息，然后将该信息标准化，以便在不同帐户之间保持一致。 这样一来，您就可以快速了解自己是否接触到了决策者、影响者或支持角色，而不是迷失在混乱的标题中。 角色可帮助您了解谁感兴趣，而不仅仅是感兴趣程度有多高。 |
| 映射购买组角色 | 将角色映射到角色后，您可以将角色合并到购买组中，即客户内部最有可能影响购买或决定购买的完整团队。 每个角色（如&#x200B;_决策者_、_影响者_&#x200B;或&#x200B;_冠军_）都添加了一张图片，以便您清楚地了解推动交易的委员会。<br/><br/>代理将根据职务、职能、资历和您配置的其他属性，将每个已识别的角色映射到他们最有可能为特定产品扮演的角色。 它还显示了每个角色的覆盖范围，以便您了解哪些角色在参与策略中得到了充分代表，以及在哪些方面仍然存在差距。 |
| 使用机会数据检测角色 | 为了让您最准确地了解参与人员及其兴趣所在，代理将根据以下各项来处理角色排名和产品意图： <ul><li>最佳案例情景：如果您可以提供诸如&#x200B;_机会阶段_、_机会关闭日期_&#x200B;等数据以及清晰的&#x200B;_机会到产品映射_，则代理可以放心地为每个产品排名角色。<li>此排名可让您精确了解整个客户的参与度和兴趣。 </ul>但代理知道数据并不总是完整的，这没有关系。 它包括智能的后备功能，以保持移动办公：<ul><li>该代理分析活动的量，使用时间衰减为最近的活动提供更多权重。<li>此权重允许代理区分角色并对其进行排名，即使没有完整的机会数据也是如此。 </ul>在将机会与产品关联时，代理将按照以下方式处理这些机会：<ul><li>_理想_：您提供或帮助代理创建映射表。<li>_如果不可用_：代理使用模糊匹配连接点。<li>_没有任何关联_：代理根据关闭日期之前的最近活动推断产品意图。</ul>这种分层方法可确保代理仍然能够提供有意义的洞察，即使数据并不完美也是如此。 |
| 机会分析 | 代理查看历史机会数据以了解哪些因素最能强烈地预测成功，它使用三个核心维度来执行此操作：<ol><li>成功率：显示涉及某些角色时成功完成交易的频率。 如果具有特定角色模式的客户（如技术评估人员或VP级别决策者）倾向于更频繁地转化，则模型会给予该模式更高的权重。 此信息是总业务机会的百分比，例如已关闭或成功的业务机会。<li>会员资格比率：测量角色类型在给定产品的各种机会中显示的频率。 如果某些角色始终出现在成功的交易中，则表明他们在购买过程中扮演着关键角色。<li>角色影响：量化给定角色对结果的贡献度，不仅是角色是否存在，还包括其参与度或活动级别与胜选的相关度。</ol>总之，这些信号有助于推断哪些角色对购买结果的影响最大，即使商机数据不完整也是如此。 随着时间的推移，它允许系统呈现对交易成功具有最可预测性的高影响力角色和模式，然后通知客户意图、角色映射和购买团体推荐。 |
| 意图 | 当有人访问网页或单击与产品相关的电子邮件链接时，这是他们感兴趣的信号，称为&#x200B;_意图_。<br/><br/>代理从分类法开始，分类法基本上是客户的产品和描述这些产品的关键字的列表。 此信息可帮助代理了解每个内容或交互的内容。<br/><br/>接下来，代理使用该分类来标记访客活动，例如其操作与哪些关键字或产品相关。<br/><br/>然后，代理会查看某个人参与的深度，例如他们访问的页面数或他们交互的频率。 它使用此信息计算特定关键字、产品或产品类别的单个意图分数。 它将每个意图分数存储为&#x200B;_高_、_Medium_&#x200B;或&#x200B;_低_&#x200B;意图以指示兴趣强度。 （低意图： `<=0.2`，Medium意图： `0.2 < score <= 0.6`，高意图： `0.6 < score <= 1`）<br/><br/>最后，代理将来自同一公司（帐户）的所有人员的意图分数合并起来以查看整个帐户级别的意图，从而显示公司似乎最感兴趣的产品或主题。 |
| 影响购买群组的角色 | 每个购买组由对购买决策做出不同贡献的角色组成，如&#x200B;_决策者_、_影响者_、_冠军_&#x200B;和&#x200B;_最终用户_。 每个角色都有不同程度的影响。<br/><br/>决策者最具影响力，通常控制预算批准。 影响者塑造评估和推荐。 支持人员帮助建立内部共识，而最终用户则验证产品的适用性。<br/><br/>通过向您展示这些角色，代理可帮助您了解谁是购买决策的决定者、您的参与度最高以及覆盖范围可能存在差距的位置。 通过此信息，您可以专注于对于此产品最重要的角色。 |
| 角色或角色覆盖范围 | 对于任何给定产品，通常都有一组已知会影响购买的关键角色和角色（_N_&#x200B;个角色或角色）。<br/><br/>对于每个帐户，代理通过检查这些&#x200B;_N_&#x200B;角色中有多少由该帐户中的至少一个人员表示，来计算覆盖范围。<br/><br/>如果所有&#x200B;_N_&#x200B;角色都存在，则帐户具有完全覆盖范围。 如果仅呈现某些角色，则覆盖范围是部分的。<br/><br/>简单地说，角色和角色涵盖范围根据是否包含所有重要的决策者、影响者和拥护者来衡量您的购买群体对产品的完成程度。 |

## XDM数据先决条件

Audience Agent提供对显示产品第一方意图的帐户的洞察，并根据定义的数据计算角色和角色。 确保将以下先决条件数据配置为使用Audience Agent功能：

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
      <td>人员的名字，Audience Agent在满足任何条件时用于在UI中显示姓名</td>
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
      <td>人员的全名，Audience Agent在满足任何条件时用于在UI中显示姓名</td>
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
      <td>人员的姓氏，Audience Agent在满足任何条件时用于在UI中显示姓名</td>
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
      <td>Audience Agent在满足用户查询中提出的任何条件时用于在UI中显示的帐户名称</td>
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
      <td>Audience Agent用于在UI中根据用户查询对帐户应用筛选的帐户/公司的描述 </td>
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
      <td>Audience Agent用于在UI中根据用户查询对帐户应用筛选的帐户/公司行业 </td>
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
      <td>Audience Agent用于在UI中根据用户查询对帐户应用筛选的帐户/公司的帐单地址 </td>
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
      <td>Audience Agent使用的Opportunity的名称 </td>
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
      <td>Audience Agent使用的Opportunity的说明 </td>
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

Audience Agent利用Journey Optimizer B2B edition中检测到的第一方意图：

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
      <td>获取事件类型，因为代理仅处理四个事件(<span>directMarketing.emailClicked， directMarketing.emailOpen， directMarketing.emailUnsubscribed， web.webpagedetails.pageViews)</span>
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
      <td>用于从Marketo Engage数据中心获取电子邮件内容；它由(SourceID@SourceInstanceID.SourceType)组成</td>
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
