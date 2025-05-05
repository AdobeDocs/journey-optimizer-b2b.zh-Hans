---
title: XDM字段
description: 查看在Adobe Experience Platform和Journey Optimizer B2B edition之间同步的默认属性字段。
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 34ef9681b75ef1cd43d34e3f2836a60affb95b33
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 12%

---

# XDM 字段

帐户受众数据同时作为属性存储在XDM业务帐户和XDM业务人员类中。 数据定期在Adobe Experience Platform和Journey Optimizer B2B edition之间同步。 以下部分列出了缺省属性集。

>[!TIP]
>
>您可以使用XDM业务帐户人员关系类在多对多关系中对XDM业务人员和XDM业务帐户类建模，如[Experience Platform XDM文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/tutorials/relationship-b2b)中所述。

## XDM业务帐户人员关系属性

| [属性](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | 显示名称 | Journey Optimizer B2B显示名称 | 数据类型 | 描述 |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | 人员角色 | 角色 | 字符串数组 | 与帐户中的人员关联的角色数组，如`owner, accountant, designer`。 |

## XDM业务人员属性

>[!IMPORTANT]
>
>`workEmail.Address`属性是必需的。 如果帐户受众成员的该值为空，则不会摄取该人员，并会将其从引用该受众的帐户历程和购买组中忽略。

| [属性](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | 显示名称 | Journey Optimizer B2B显示名称 | 数据类型 | 描述 |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.isMarketingSuspended` | 营销暂停指标 | 营销暂停 | 布尔值 | 该值指示人员营销是否暂停。 |
| `b2b.marketingSuspendedCause` | 营销暂停原因 | 营销暂停原因 | 字符串 | 如果暂停了人员的营销，则此属性提供了原因。 |
| `b2b.personStatus` | 人员状态 | 潜在客户状态 | 字符串 | 记录人员当前营销/销售状态的字段。 |
| `consents.marketing.email.reason` | 选择禁用原因 | 退订原因 | 字符串 | 与电子邮件选择退出关联的原因。 |
| `consents.marketing.email.val` | 退订 | 退订 | 字符串 | 如果取消订阅为true（例如，值= 1），则将`consents.marketing.email.val`设置为(n)。 如果取消订阅为false（例如，值= 0），则将`consents.marketing.email.val`设置为null。 |
| `extendedWorkDetails.jobTitle` | 职务 | 职务 | 字符串 | 人员的工作职位。 |
| `faxPhone.number` | 数值 | 传真号码 | 字符串 | 传真电话号码。 |
| `mobilePhone.number` | 数值 | 手机号码 | 字符串 | 与人员关联的手机号码。 |
| `person.birthDate` | 出生日期（年 — 月 — 日） | 出生日期 | 字符串 | 人员的完整出生日期。 YYYY-MM-DD |
| `person.name.courtesyTitle` | 尊称 | 称谓 | 字符串 | 通常是人员的职务、尊称或称呼的缩写。 在开场白中，courtesyTitle用于全名或姓氏之前。 例如，先生、女士或博士。 |
| `person.name.firstName` | 名字 | 名字 | 字符串 | 在姓名的语言中最常被接受的书写顺序排列的姓名第一部分。 在许多文化中，它是首选的个人或名字。 引入firstName和lastName属性是为了与现有系统保持兼容性，现有系统以简化、非语义和非国际化的方式建模名称。 使用`xdm:fullName`总是可取的。 |
| `person.name.lastName` | 姓氏 | 姓氏 | 字符串 | 在姓名的语言中最常被接受的书写顺序的最后一个姓名区段。 在许多文化中，这是继承的姓氏、父名或母名。 引入firstName和lastName属性是为了与现有系统保持兼容性，现有系统以简化、非语义和非国际化的方式建模名称。 使用`xdm:fullName`总是可取的。 |
| `person.name.middleName` | 中间名称 | 中间名称 | 字符串 | 在名字和姓氏之间提供的中间名、备用名或附加名。 |
| `workAddress.city ` | 城市 | 城市 | 字符串 | 城市的名称。 |
| `workAddress.country` | 国家/地区 | 国家/地区 | 字符串 | 政府管辖地区的名称。 除`xdm:countryCode`外，它是一个自由形式的字段，可以包含任何语言的国家/地区名称。 |
| `workAddress.postalCode` | 邮政编码 | 邮政编码 | 字符串 | 位置的邮政编码。 并非所有国家/地区都提供邮政编码。 在某些国家/地区，它仅包含邮政编码的一部分。 |
| `workAddress.state` | State | State | 字符串 | 地址所在州的名称。 它是一个自由格式的字段。 |
| `workAddress.street1` | 街道1 | 地址 | 字符串 | 主要街道级别信息、公寓号、街道号和街道名称。 |
| `workEmail.address` | 地址 | 电子邮件地址 | 字符串 | **必填字段** <br/>技术地址，例如RFC2822和后续标准中通常定义的`<name@domain.com>`。 |
| `workEmail.status` | 状态 | 电子邮件已暂停 | 字符串 | 关于使用电子邮件地址的能力的指示。 |
| `workPhone.number` | 数值 | 电话号码 | 字符串 | 工作电话号码。 |

## XDM业务帐户属性

>[!IMPORTANT]
>
>`accountName`属性是必需的。 如果帐户受众中某个帐户的日期为空，则不会摄取该帐户，并会在引用受众的帐户历程和购买组中忽略该帐户。

| [属性](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | 显示名称 | Journey Optimizer B2B显示名称 | 数据类型 | 描述 |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | 城市 | 城市 | 字符串 | 帐单地址中使用的城市名称。 |
| `accountBillingAddress.country` | 国家/地区 | 国家/地区 | 字符串 | 帐单地址中使用的政府管理地区的名称。 除`xdm:countryCode`外，它是一个自由形式的字段，可以包含任何语言的国家/地区名称。 |
| `accountBillingAddress.postalCode` | 邮政编码 | 地址邮政编码 | 字符串 | 帐单地址所在位置的邮政编码。 并非所有国家/地区都提供邮政编码。 在某些国家/地区，它仅包含邮政编码的一部分。 |
| `accountBillingAddress.region` | 区域 | 地址区域 | 字符串 | 帐单地址的地区、国家或地区部分。 |
| `accountBillingAddress.state` | State | State | 字符串 | 帐单地址的省/市/自治区名称。 它是一个自由格式的字段。 |
| `accountBillingAddress.street1` | 街道1 | 街道1 | 字符串 | 帐单地址的主要街道级别信息，通常包括公寓号、街道号和街道名称。 |
| `accountName` | 名称 | 名称 | 字符串 | **必填字段** <br/>公司名称。 此字段最多可包含255个字符。 |
| `accountOrganization.annualRevenue.amount` | 年收入 | 年收入 | 数值 | 估计的组织年收入金额。 |
| `accountOrganization.industry` | 行业 | 行业 | 字符串 | 业界归功于该组织。 它是一个自由格式字段，建议在查询中使用结构化值或使用`xdm:classifier`属性。 |
| `accountOrganization.logoUrl` | 徽标URL | 徽标URL | 字符串 | 要与Salesforce实例的URL（例如`https://yourInstance.salesforce.com/`）组合的路径，用于生成URL以请求与帐户关联的社交网络个人资料图像。 生成的URL会返回指向帐户的社交网络个人资料图像的HTTP重定向（代码302）。 |
| `accountOrganization.numberOfEmployees` | 员工数 | 员工数 | 整数 | 组织的员工数。 |
| `accountOrganization.SICCode` | SIC 代码 | SIC 代码 | 字符串 | 标准行业分类(SIC)代码是一个四位数的代码，根据公司的业务活动对公司所属的行业进行分类。 |
| `accountOrganization.website` | 网站URL | 域名 | 字符串 | 组织网站的URL。 |
| `accountPhone.number` | 不适用 | 帐户电话号码 | 字符串 | 与帐户关联的电话号码。 |
| `accountSourceType` | 不适用 | 源类型 | 字符串 | 帐户的Source类型。 |

## XDM业务机会属性

此外，商机数据作为属性存储在XDM业务机会类中，这些属性可以通过多对一关系与XDM业务帐户类关联，如[此处](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field)所述。

| [属性](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md) | 显示名称 | Journey Optimizer B2B显示名称 | 数据类型 | 描述 |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `expectedCloseDate` | 预计关闭日期 | 预计机会关闭日期 | 字符串 | 商机的预期结束日期。 |
| `expectedRevenue.amount` | 预期收入 | 总机会预期收入 | 字符串 | 根据金额和概率计算的收入。 |
| `fiscalQuarter` | 财政季度 | 机会会计季度 | 字符串 | 机会的目标财政季度。 |
| `fiscalYear` | 会计年度 | 机会会计年度 | 字符串 | 机会的目标财政年度。 |
| `forecastCategory` | 预测类别 | 机会预测类别 | 字符串 | 由商机阶段值确定的预测类别。 |
| `forecastCategoryName` | 预测类别名称 | 机会预测类别名称 | 字符串 | 特定预测类别的报表中显示的预测类别名称。 |
| `isClosed` | 已关闭标志 | 机会已关闭 | 字符串 | 指示商机是否已关闭的标记。 |
| `isWon` | 赢单标志 | 赢得的机会 | 字符串 | 指示是否赢得了机会的标志。 |
| `lastActivityDate` | 上次活动日期 | 上次活动日期 | 字符串 | 机会的上次活动日期。 |
| `leadSource` | 潜在客户来源 | 商机来源 | 字符串 | 机会的Source，如广告、合作伙伴或网络。 |
| `nextStep` | 下一步 | 机会下一步 | 字符串 | 关闭商机的下一个任务的描述。 |
| `opportunityAmount.amount` | 机会金额 | 机会总金额 | 字符串 | 商机的估计总销售额。 |
| `opportunityDescription` | 机会描述 | 机会描述 | 字符串 | 描述机会的附加信息，如可能销售的产品或客户过去的购买。 |
| `opportunityName` | 机会名称 | 机会名称 | 字符串 | 机会的主题或描述性名称，如预期订单或公司名称。 |
| `opportunityQuantity` | 机会数量 | 机会数量 | 字符串 | 商机的相关“产品”列表中所有产品的所有数量字段值的总和。 |
| `opportunityStage` | 机会阶段 | 机会阶段 | 字符串 | 机会的销售阶段，以帮助销售团队赢得销售机会。 |
| `opportunityType` | 机会类型 | 机会类型 | 字符串 | 分配给机会的类型，如&#x200B;_现有业务_&#x200B;或&#x200B;_新业务_ |
| `probabilityPercentage` | 概率百分比 | 机会概率百分比 | 字符串 | 关闭机会的可能性，以百分比表示。 |
