---
title: B2B命名空间和架构
description: 使用Experience Platform自动生成实用程序为Journey Optimizer B2B edition配置Postman B2B命名空间和架构。
feature: Setup, Data Management
role: Admin
exl-id: 40d01027-7cf2-4189-8a49-7a0783c00721
source-git-commit: 0f34a98753b71b388c822ef4a26dbae6b4c8fb1b
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 96%

---

# B2B命名空间和架构

Journey Optimizer B2B Edition设置包括配置用于B2B源的Experience Platform命名空间和架构。 生成B2B命名空间和架构需要Postman自动化实用程序。

>[!AVAILABILITY]
>
>- 您必须有权访问[Adobe Real-Time Customer Data Platform B2B edition](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdpb2b-intro/b2b-overview){target="_blank"}，您的B2B架构才能在[实时客户档案](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/home){target="_blank"}中获得资格。
>
>- 您的Experience Platform B2B实体必须使用[B2B命名空间和架构指南](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/schemas/b2b){target="_blank"}中所述的标准关系。

查看以下有关要与B2B源一起使用的命名空间和架构的基础设置的信息。 它还提供了有关设置Postman自动化实用程序的详细信息，该实用程序是生成B2B命名空间和架构所必需的。

## 设置自动生成实用程序

请参阅以下资源，了解先决条件和有关如何设置[!DNL Postman]环境以支持B2B命名空间和架构自动生成实用程序的详细信息。

- 从[GitHub存储库](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility){target="_blank"}下载命名空间和架构自动生成实用程序集合和环境。
- 有关使用Experience Platform API的信息，包括有关收集所需标头的值和读取示例API调用的详细信息，请参阅&#x200B;[_Adobe Experience Platform API快速入门_](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/landing/platform-apis/api-guide){target="_blank"}。
- 有关为Experience Platform API生成凭据的信息，请参阅&#x200B;[_身份验证和访问Experience Platform API_](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication){target="_blank"}。
- 有关为Experience Platform API设置[!DNL Postman]的信息，请参阅Adobe Experience Platform中的[_[!DNL Postman]_](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman){target="_blank"}。

### 环境值

设置Experience Platform开发人员控制台和[!DNL Postman]后，您可以将相应的环境值应用于您的[!DNL Postman]环境。 下表提供了有关填充[!DNL Postman]环境的示例值和其他信息：

| Variable | 描述 | 示例 |
| --- | --- | --- |
| `CLIENT_SECRET` | 用于生成`{ACCESS_TOKEN}`的唯一标识符。 | `{CLIENT_SECRET}` |
| `API_KEY` | 用于对调用Experience Platform API进行身份验证的唯一标识符。 | `c8d9a2f5c1e03789bd22e8efdd1bdc1b` |
| `ACCESS_TOKEN` | 完成对Experience Platform API的调用所需的授权令牌。 | `Bearer {ACCESS_TOKEN}` |
| `META_SCOPE` | 对于[!DNL Journey Optimizer B2B]和[!DNL Marketo Engage]，此值是固定的，并且始终设置为： `ent_dataservices_sdk`。 | `ent_dataservices_sdk` |
| `CONTAINER_ID` | `global`容器包含所有标准Adobe和Experience Platform合作伙伴提供的类、架构字段组、数据类型和架构。 对于[!DNL Marketo]，此值是固定的，并且始终设置为`global`。 | `global` |
| `TECHNICAL_ACCOUNT_ID` | 用于集成到Adobe I/O的凭据。 | `D42AEVJZTTJC6LZADUBVPA15@techacct.adobe.com` |
| `IMS` | Identity Management System (IMS)提供了对Adobe服务进行身份验证的框架。 对于[!DNL Journey Optimizer B2B]和[!DNL Marketo Engage]，此值是固定的，并且始终设置为： `ims-na1.adobelogin.com`。 | `ims-na1.adobelogin.com` |
| `IMS_ORG` | 公司实体，可以拥有产品或服务，也可以为其授予产品和服务许可证，并允许其成员访问。 | `ABCEH0D9KX6A7WA7ATQE0TE@adobeOrg` |
| `SANDBOX_NAME` | 您正在使用的虚拟沙盒分区的名称。 | `prod` |
| `TENANT_ID` | 一个ID，用于确保您创建的资源被正确命名并包含在您的组织内。 | `b2bcdpproductiontest` |
| `PLATFORM_URL` | 您对其进行API调用的URL端点。 此值是固定的，并且始终设置为： `http://platform.adobe.io/`。 | `http://platform.adobe.io/` |

{style="table-layout:auto"}

### 运行脚本

在环境值就绪后，使用[!DNL Postman]界面运行脚本以创建命名空间和架构。 选择自动生成器实用工具的根文件夹，然后从顶部标题中选择&#x200B;**[!DNL Run]**。

Postman UI中命名空间和架构生成器的![根文件夹](./assets/namespaces-schemas-postman-root-folder.png){width="500" zoomable="yes"}

出现[!DNL Runner]接口。 在此处，确保选中所有复选框，然后选择&#x200B;**[!DNL Run Namespaces and Schemas Autogeneration Utility]**。

![Postman UI，其中已选择命名空间和架构集合中的多个请求。](./assets/namespaces-schemas-postman-run-generator.png){width="800" zoomable="yes"}

成功的请求会创建所需的B2B命名空间和架构。

## B2B命名空间

身份命名空间是Experience Platform [[!DNL Identity Service]](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home){target="_blank"}的组件，用于区分身份的上下文。 完全限定的身份包括身份值和命名空间。 有关详细信息，请参阅[命名空间概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces){target="_blank"}。

B2B命名空间在实体的主标识中使用。

| 显示名称 | 身份标识符号 | 身份类型 |
| --- | --- | --- |
| B2B人员 | `b2b_person` | `CROSS_DEVICE` |
| B2B 帐户 | `b2b_account` | `B2B_ACCOUNT` |
| B2B 机会 | `b2b_opportunity` | `B2B_OPPORTUNITY` |
| B2B机会人员关系 | `b2b_opportunity_person_relation` | `B2B_OPPORTUNITY_PERSON` |
| B2B 营销活动 | `b2b_campaign` | `B2B_CAMPAIGN` |
| B2B 营销活动成员 | `b2b_campaign_member` | `B2B_CAMPAIGN_MEMBER` |
| B2B 营销列表 | `b2b_marketing_list` | `B2B_MARKETING_LIST` |
| B2B 营销列表成员 | `b2b_marketing_list_member` | `B2B_MARKETING_LIST_MEMBER` |
| B2B帐户人员关系 | `b2b_account_person_relation` | `B2B_ACCOUNT_PERSON` |

{style="table-layout:auto"}

## B2B架构

Experience Platform使用架构，以一致且可重用的方式描述数据结构。 通过在系统中以一致的方式定义数据，更容易保留含义并因此从数据中获取价值。

在Experience Platform可以摄取数据之前，必须有一个架构来描述数据的结构并对每个字段中可以包含的数据类型提供限制。 架构由一个基类以及零个或多个架构字段组组成。

有关架构组合模型的详细信息，包括设计原则和最佳实践，请参阅&#x200B;[_架构组合基础_](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}。

+++ B2B 帐户

<table>
    <tr>
        <td style="width: 30%;">基类</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account" target="_blank">XDM业务帐户</a></td>
    </tr>
    <tr>
        <td>字段组</td>
        <td>XDM业务帐户详细信息</td>
    </tr>
    <tr>
        <td>[!DNL Profile] 在架构中</td>
        <td>已启用</td>
    </tr>
    <tr>
        <td>主要身份标识</td>
        <td><code>accountKey.sourceKey</code> 在基类中</td>
    </tr>
    <tr>
        <td>主要身份标识命名空间</td>
        <td>B2B 帐户</td>
    </tr>
    <tr>
        <td>辅助标识</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> 在基类中</td>
    </tr>
    <tr>
        <td>辅助身份命名空间</td>
        <td>B2B 帐户</td>
    </tr>
    <tr>
        <td>关系</td>
        <td><ul><li><code>accountParentKey.sourceKey</code> 在“XDM业务帐户详细信息”字段组中</li><li>目标属性： <code>/accountKey/sourceKey</code></li><li>类型：一对一</li><li>引用架构：B2B帐户</li><li>命名空间： B2B帐户</li></ul> </td>
    </tr>
</table>

+++

+++ B2B人员

<table>
    <tr>
        <td style="width: 30%;">基类</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/individual-profile">XDM个人配置文件</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>字段组</td>
        <td><ul><li>XDM业务人员详细信息</li><li>XDM业务人员组件</li><li>Identitymap</li><li>同意和偏好设置详细信息</li></ul> </td>
    </tr>
    <tr>
        <td>[!DNL Profile] 在架构中</td>
        <td>已启用</td>
    </tr>
    <tr>
        <td>主要身份标识</td>
        <td><code>b2b.personKey.sourceKey</code> 在“XDM业务人员详细信息”字段组中</td>
    </tr>
    <tr>
        <td>主要身份标识命名空间</td>
        <td>B2B人员</td>
    </tr>
    <tr>
        <td>辅助标识</td>
        <td><ol><li><code>extSourceSystemAudit.externalKey.sourceKey</code> XDM业务人员详细信息字段组的</li><li><code>workEmail.address</code> XDM业务人员详细信息字段组的</li></ol></td>
    </tr>
    <tr>
        <td>辅助身份命名空间</td>
        <td><ol><li>B2B人员</li><li>电子邮件</li></ol></td>
    </tr>
    <tr>
        <td>关系</td>
        <td><ul><li><code>personComponents.sourceAccountKey.sourceKey</code> XDM业务人员组件字段组的</li><li>类型：多对一</li><li>引用架构：B2B帐户</li><li>命名空间： B2B帐户</li><li>目标属性： accountKey.sourceKey</li><li>来自当前架构的关系名称：帐户</li><li>引用架构中的关系名称：人员</li></ul> </td>
    </tr>
</table>

+++

<!--

+++B2B Opportunity

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity">XDM Business Opportunity</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Opportunity Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> in the base class</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td><ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: Opportunities</li></ul></td>
    </tr>
</table>

+++

+++B2B Opportunity Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity-person-relation">XDM Business Opportunity Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td> **First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Opportunities</li></ul>**Second relationship**<ul><li><code>opportunityKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Opportunity </li><li>Namespace: B2B Opportunity </li><li>Destination property: <code>opportunityKey.sourceKey</code></li><li>Relationship name from current schema: Opportunity</li><li>Relationship name from reference schema: People</li></ul> </td>
    </tr>
</table>


+++

+++B2B Campaign

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign">XDM Business Campaign</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

+++

+++B2B Campaign Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign-members">XDM Business Campaign Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Member Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Campaigns</li></ul>**Second relationship**<ul><li><code>campaignKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Campaign</li><li>Namespace: B2B Campaign</li><li>Destination property: <code>campaignKey.sourceKey</code></li><li>Relationship name from current schema: Campaign</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++B2B Marketing List

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list">XDM Business Marketing List</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

>[!NOTE]
>
>Static List in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Marketing List Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list-members">XDM Business Marketing List Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Marketing Lists</li></ul>**Second relationship**<ul><li><code>marketingListKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Marketing List</li><li>Namespace: B2B Marketing List</li><li>Destination property: <code>marketingListKey.sourceKey</code></li><li>Relationship name from current schema: Marketing List</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

>[!NOTE]
>
>Static List member in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Account Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account-person-relation">XDM Business Account Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>Identity Map</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>accountPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Account Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: People</li><li>Relationship name from reference schema: Account</li></ul>**Second relationship**<ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++
-->
