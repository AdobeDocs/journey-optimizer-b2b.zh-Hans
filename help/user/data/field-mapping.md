---
title: XDM字段
description: 查看在Adobe Experience Platform和Journey Optimizer B2B edition之间同步的默认属性字段。
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 6578fdf35ec565ba315c00eeb3d2466c925cf816
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 13%

---

# XDM字段

帐户受众数据同时作为属性存储在XDM业务帐户和XDM业务人员类中。 数据定期在Adobe Experience Platform和Journey Optimizer B2B edition之间同步。 以下部分列出了缺省属性集。

## XDM业务人员属性

>[!IMPORTANT]
>
>`workEmail.Address`属性是必需的。 如果帐户受众成员的该值为空，则不会摄取该人员，并会将其从引用该受众的帐户历程和购买组中忽略。

| [属性](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | 显示名称 | Journey Optimizer B2B显示名称 | 数据类型 | 描述 |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.companyName` | 公司名称 | 公司名称 | 字符串 | 与业务人员关联的公司的名称。 |
| `b2b.companyWebsite` | 公司网站 | 网站 | 字符串 | 与业务人员关联的公司的网站。 |
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
| `accountName` | 名称 | 名称 | **必填字段** <br/>字符串 | 公司名称。 此字段最多可包含255个字符。 |
| `accountOrganization.annualRevenue.amount` | 年收入 | 年收入 | 数值 | 估计的组织年收入金额。 |
| `accountOrganization.industry` | 行业 | 行业 | 字符串 | 业界归功于该组织。 它是一个自由格式字段，建议在查询中使用结构化值或使用`xdm:classifier`属性。 |
| `accountOrganization.logoUrl` | 徽标URL | 徽标URL | 字符串 | 要与Salesforce实例的URL（例如`https://yourInstance.salesforce.com/`）组合的路径，用于生成URL以请求与帐户关联的社交网络个人资料图像。 生成的URL会返回指向帐户的社交网络个人资料图像的HTTP重定向（代码302）。 |
| `accountOrganization.numberOfEmployees` | 员工数 | 员工数 | 整数 | 组织的员工数。 |
| `accountOrganization.SICCode` | SIC 代码 | SIC 代码 | 字符串 | 标准行业分类(SIC)代码，它是一个四位数的代码，根据公司的业务活动对公司所属的行业进行分类。 |
| `accountOrganization.website` | 网站URL | 域名 | 字符串 | 组织网站的URL。 |
| `accountPhone.number` | 不适用 | 帐户电话号码 | 字符串 | 与帐户关联的电话号码。 |
| `accountSourceType` | 不适用 | 源类型 | 字符串 | 帐户的Source类型。 |
