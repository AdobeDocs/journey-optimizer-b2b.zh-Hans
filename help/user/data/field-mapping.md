---
title: XDM字段映射
description: 查看AEP XDM架构、Marketo Engage和Journey Optimizer B2B版本之间的字段映射。
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 7103e4f6666482a72511661dfaed1392d4eb16b1
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 19%

---

# XDM字段映射

中的数据传输服务(DTS)负责将数据从Adobe Experience Platform同步到Journey Optimizer B2B版本。 DTS依赖于Experience PlatformXDM架构字段及其Marketo Engage中的等效字段之间的映射。

## XDM业务人员默认字段映射

| XDM业务人员 | Marketo Engage人员显示名称 | AJO B2B人员显示名称 | XDM类型 | Marketo类型 | XDM描述 |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `workAddress.street1` | 地址 | 不适用 | 字符串 | 文本 | 主要街道级别信息、公寓号、街道号和街道名称。 |
| `workAddress.city ` | 城市 | 城市 | 字符串 | 字符串 | 城市的名称。 |
| `b2b.companyName` | 公司名称 | 公司 | 字符串 | 字符串 | 与业务人员关联的公司的名称。 |
| `workAddress.country` | 国家/地区 | 国家/地区 | 字符串 | 字符串 | 政府管辖地区的名称。 除`xdm:countryCode`之外，这是一个自由形式的字段，可以包含任何语言的国家/地区名称。 |
| `person.birthDate` | 出生日期 | 出生日期 | 字符串 | 日期 | 人员的完整出生日期。  YYYY-MM-DD |
| `workEmail.address` | 电子邮件地址 | 电子邮件地址 | 字符串 | 电子邮件 | 技术地址，例如RFC2822和后续标准中通常定义的“<name@domain.com>”。 |
| `workEmail.status` | 电子邮件已暂停 | 电子邮件已暂停 | 字符串 | 布尔 | 关于使用电子邮件地址的能力的指示。 |
| `faxPhone.number` | 传真号码 | 不适用 | 字符串 | 电话 | 传真电话号码。 |
| `person.name.firstName` | 名字 | 名字 | 字符串 | 字符串 | 在姓名的语言中最常被接受的书写顺序排列的姓名第一部分。 在许多文化中，这是首选的个人或名字。 引入firstName和lastName属性是为了与现有系统保持兼容性，现有系统以简化、非语义和非国际化的方式建模名称。 使用xdm：fullName始终是首选。 |
| `extendedWorkDetails.jobTitle` | 职务 | 职务 | 字符串 | 字符串 | 人员的工作职位。 |
| `person.name.lastName` | 姓氏 | 姓氏 | 字符串 | 字符串 | 在姓名的语言中最常被接受的书写顺序中的姓名的末尾部分。 在许多文化中，这是继承的姓氏、父名或母名。 引入firstName和lastName属性是为了与现有系统保持兼容性，现有系统以简化、非语义和非国际化的方式建模名称。 使用xdm：fullName始终是首选。 |
| `b2b.personStatus` | 潜在客户状态 | 不适用 | 字符串 | 字符串 | 记录人员当前营销/销售状态的字段。 |
| `b2b.isMarketingSuspended` | 营销暂停 | 不适用 | 布尔 | 布尔 | 指示人员营销是否暂停。 |
| `b2b.marketingSuspendedCause` | 营销暂停原因 | 不适用 | 字符串 | 字符串 | 如果暂停了人员的营销，则此属性提供了原因。 |
| `person.name.middleName` | 中间名称 | 不适用 | 字符串 | 电话 | 在名字和姓氏之间提供的中间名、备用名或附加名。 |
| `mobilePhone.number` | 手机号码 | 手机号码 | 字符串 | 电话 | 手机号码。 |
| `workPhone.number` | 电话号码 | 电话号码 | 字符串 | 电话 | 工作电话号码。 |
| `workAddress.postalCode` | 邮政编码 | 邮政编码 | 字符串 | 字符串 | 位置的邮政编码。 并非所有国家/地区都提供邮政编码。 在一些国家/地区，这将仅包含邮政编码的一部分。 |
| `person.name.courtesyTitle` | 称谓 | 不适用 | 字符串 | 字符串 | 通常是人员的职务、尊称或称呼的缩写。 在开场白中，courtesyTitle用于全名或姓氏之前。 例如，先生、小姐或博士。 |
| `workAddress.state` | State | State | 字符串 | 字符串 | 国家的名称。 这是自由格式字段。 |
| `consents.marketing.email.val` | 退订 | 退订 | 字符串 | 布尔 | 如果取消订阅为true（例如，值= 1），则将`consents.marketing.email.val`设置为(n)。 如果取消订阅为false（例如，值= 0），则将consents.marketing.email.val设置为null。 |
| `consents.marketing.email.reason` | 退订原因 | 退订原因 | 字符串 | 字符串 |  |
| `b2b.companyWebsite` | 网站 | 不适用 | 字符串 | url | 与业务人员关联的公司的网站。 |
