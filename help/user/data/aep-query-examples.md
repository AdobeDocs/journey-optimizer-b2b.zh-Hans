---
title: 数据集查询
description: 了解如何在查询服务中使用SQL查询示例来分析Adobe Journey Optimizer B2B Edition导出的帐户、购买组、人员和旅程数据。
feature: Reporting, Data Management
role: Admin, Developer
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: 6db81a0b993f450a3ff448dcb4c417e3e81ec70a
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 1%
---

# 数据集查询

查找现成的SQL查询示例，以分析[!DNL Adobe Journey Optimizer B2B Edition]导出到[!DNL Adobe Experience Platform]的帐户、人员、购买组和历程数据。 要报告帐户、购买组、电子邮件参与和历程活动，请在[!DNL Query Service]中运行查询。

有关这些查询中使用的数据集和字段的说明，请参阅[导出的数据集](./aep-exported-datasets.md)。

## 先决条件 {#prerequisites}

在此页面上运行任何查询之前，请确保您满足以下条件：

* **访问[!DNL Query Service]：**&#x200B;您必须有权访问[!DNL Experience Platform]沙盒中的[查询服务](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/query/home){target="_blank"}。
* **可用数据集：**&#x200B;查询针对导出的[!DNL Journey Optimizer B2B Edition]数据集。 在沙盒中，转到&#x200B;**[!UICONTROL 数据集]**&#x200B;并验证该数据集存在且包含数据。
* **架构字段值：**&#x200B;确保查询中的字段在相应架构中具有值。 空字段不返回任何结果，也不会产生错误。

>[!NOTE]
>
>这些示例使用短表名称，如`account_table`和`person_activity_table`。 将每个表名称替换为沙盒中相应数据集的名称。 如果数据集名称包含连字符，请用双引号将其括起来。 将占位符值（如`Example Company`和`PASTE_COMPLETE_JOURNEY_ID_HERE`）替换为环境中的值。

## 运行查询 {#run}

要在此页面上运行任何示例，请执行以下操作：

1. 在[!DNL Experience Platform]中，选择&#x200B;**[!UICONTROL 查询服务]** > **[!UICONTROL 查询]**。
1. 将示例粘贴到查询编辑器中，然后替换表名和占位符值。
1. 选择&#x200B;**[!UICONTROL 运行]**。

按日期过滤的示例使用过去30天。 要更改时间范围，请编辑`INTERVAL '30' DAY`值。

## 选择查询

使用下表为您的报告任务选择查询。

| 我想 | 转到 |
|---|---|
| 审核帐户名称、行业和位置 | [查看帐户详细信息](#account-details) |
| 按参与度比较购买组 | [比较购买团体参与情况](#buying-group-engagement) |
| 查找与帐户关联的人员 | [查找帐户中的人员](#account-people) |
| 跟踪购买组状态的更改 | [查看购买组状态更改](#buying-group-status-changes) |
| 查找单击了电子邮件的用户 | [查找点击了电子邮件的用户](#email-clicks) |
| 按类型比较近期活动 | [比较近期人员活动](#person-activity) |
| 按大小比较帐户历程 | [按历程比较帐户计数](#account-journey-counts) |
| 列出历程中的帐户 | [在历程中列出帐户](#journey-accounts) |
| 跟踪每日帐户历程活动 | [跟踪每日帐户活动](#account-daily-activity) |
| 调查历程中帐户的历史记录 | [查看帐户历程时间线](#account-timeline) |
| 按大小和状态比较人员历程 | [按历程比较人员计数](#person-journey-counts) |
| 列出历程中的人员 | [列出历程中的人员](#journey-people) |
| 查看人员在历程中的位置 | [按步骤](#person-step-counts)比较人员计数 |
| 跟踪最近的人员历程活动 | [跟踪最近的历程活动](#person-journey-activity) |
| 调查历程中人员的历史记录 | [查看人员历程时间表](#person-timeline) |

## 帐户和购买团体查询

使用这些查询可查看帐户、购买组和可用于报表的人员。

### 查看帐户详细信息 {#account-details}

查看帐户名称、行业、位置和公司规模，以了解可用于报告的帐户。

```sql
SELECT
a._id AS accountID,
a.accountName,
a.industry,
a.country,
a.numberOfEmployees
FROM account_table a
WHERE a.isDeleted = FALSE
ORDER BY a.accountName
LIMIT 100;
```

### 比较购买团体参与度 {#buying-group-engagement}

通过记录的参与度分数、完整性和解决方案兴趣来比较购买群体。

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
bg.engagementScore,
bg.completenessScore,
bg.solutionInterest,
bg.buyingGroupStatus
FROM buying_group_table bg
WHERE bg.isDeleted = FALSE
ORDER BY bg.engagementScore DESC NULLS LAST, bg.buyingGroupName
LIMIT 100;
```

### 在帐户中查找人员 {#account-people}

查找与帐户关联的人员和职称，以了解其联系人。 将`Example Company`替换为沙盒中的帐户名。

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
p._id AS personID,
p.firstName,
p.lastName,
p.email,
p.jobTitle
FROM account_member_table m
JOIN account_table a ON m.accountID = a._id
JOIN person_table p ON m.personID = p._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND p.isDeleted = FALSE
AND a.accountName = 'Example Company'
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### 查看购买组状态更改 {#buying-group-status-changes}

查看过去30天中购买群组的状态变化，以了解群组如何随时间的变化。

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
e.timestamp AS changedAt,
e.newStatus
FROM buying_group_event_table e
JOIN buying_group_table bg ON e.buyingGroupID = bg._id
WHERE bg.isDeleted = FALSE
AND e.eventType = 'buyingGroup.changeStatus'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## 人员参与查询

使用这些查询可查看电子邮件参与和其他记录的人员活动。

### 查找单击了电子邮件的用户 {#email-clicks}

要查看最近的电子邮件参与情况，请识别过去30天内有记录电子邮件点击的人员。

```sql
SELECT DISTINCT
p._id AS personID,
p.firstName,
p.lastName,
p.email
FROM person_activity_table e
JOIN person_table p ON e.personID = p._id
WHERE e.isDeleted = FALSE
AND p.isDeleted = FALSE
AND e.eventType = 'directMarketing.emailClicked'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### 比较最近的人员活动 {#person-activity}

比较记录的活动类型和参与的人员数量以了解最近的参与情况。

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC
LIMIT 100;
```

## 帐户历程查询

使用这些查询分析帐户历程。 将`PASTE_COMPLETE_JOURNEY_ID_HERE`替换为帐户历程的`_id`值，将`PASTE_COMPLETE_ACCOUNT_ID_HERE`替换为帐户的`_id`值。

### 按历程比较帐户计数 {#account-journey-counts}

按状态和记录的成员资格计数比较帐户历程，以查看哪些历程的帐户人口最多。

```sql
SELECT
j._id AS journeyID,
j.accountJourneyName,
j.accountJourneyStatus,
COUNT(DISTINCT m.accountID) AS accountsWithRecordedMembership
FROM account_journey_table j
LEFT JOIN account_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.accountID <> ''
WHERE j.isDeleted = FALSE
GROUP BY j._id, j.accountJourneyName, j.accountJourneyStatus
ORDER BY accountsWithRecordedMembership DESC, j.accountJourneyName
LIMIT 100;
```

### 在历程中列出帐户 {#journey-accounts}

查看与特定历程关联的帐户，包括其行业和国家/地区。

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
a.industry,
a.country
FROM account_journey_member_table m
JOIN account_table a ON m.accountID = a._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY a.accountName, accountID
LIMIT 100;
```

### 跟踪每日帐户活动 {#account-daily-activity}

跟踪每日帐户添加、移除和步骤变化，以了解过去30天历程中的活动。

```sql
SELECT
CAST(e.timestamp AS DATE) AS activityDate,
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.accountID) AS distinctAccounts
FROM account_activity_table e
WHERE e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.accountID IS NOT NULL
AND e.accountID <> ''
AND e.eventType IN (
'account.addAccountToJourney',
'account.removeAccountFromJourney',
'account.changeAccountJourneyNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY CAST(e.timestamp AS DATE), e.eventType
ORDER BY activityDate DESC, e.eventType
LIMIT 100;
```

### 查看帐户历程时间线 {#account-timeline}

通过查看帐户记录的事件和历程步骤来调查帐户的近期历程历史记录。

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
n.nodeType,
e.previousJourneyNodeID,
e.buyingGroupID
FROM account_activity_table e
LEFT JOIN account_journey_node_table n
ON e.journeyNodeID = n._id
AND e.journeyID = n.accountJourneyID
AND n.isDeleted = FALSE
WHERE e.accountID = 'PASTE_COMPLETE_ACCOUNT_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## 人员历程查询

使用这些查询分析人员历程。 将`PASTE_COMPLETE_JOURNEY_ID_HERE`替换为人员历程的`_id`值，将`PASTE_COMPLETE_PERSON_ID_HERE`替换为人员的`_id`值。

### 按历程比较人员计数 {#person-journey-counts}

按记录的会员资格计数、状态和日期比较人员历程，以了解其规模和生命周期。

```sql
SELECT
j._id AS journeyID,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate,
COUNT(DISTINCT m.personID) AS peopleWithRecordedMembership
FROM person_journey_table j
LEFT JOIN person_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.personID <> ''
WHERE j.isDeleted = FALSE
GROUP BY
j._id,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate
ORDER BY peopleWithRecordedMembership DESC, j.personJourneyName
LIMIT 100;
```

### 列出历程中的人员 {#journey-people}

查看与旅程关联的用户、上次输入时间以及输入频率。

```sql
SELECT DISTINCT
m.personID,
p.firstName,
p.lastName,
p.email,
m.membershipDate,
m.lastEntryDate,
m.entryCount,
m.reentryOpensAt,
m.journeyNodeID
FROM person_journey_member_table m
LEFT JOIN person_table p
ON m.personID = p._id
AND p.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY m.lastEntryDate DESC NULLS LAST, m.personID
LIMIT 100;
```

### 按步骤比较人员计数 {#person-step-counts}

了解如何在历程成员资格中记录的各个步骤之间分配人员。

```sql
SELECT
m.journeyNodeID,
n.nodeType,
COUNT(DISTINCT m.personID) AS peopleWithRecordedStep
FROM person_journey_member_table m
LEFT JOIN person_journey_node_table n
ON m.journeyNodeID = n._id
AND m.journeyID = n.personJourneyID
AND n.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
GROUP BY m.journeyNodeID, n.nodeType
ORDER BY peopleWithRecordedStep DESC, m.journeyNodeID
LIMIT 100;
```

### 跟踪最近的历程活动 {#person-journey-activity}

比较记录的历程开始、结束和过渡，以了解过去30天历程中的人员活动。

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.eventType IN (
'person.journeyAdd',
'person.journeyRemove',
'person.journeyStart',
'person.journeyEnd',
'person.journeyNodeTransition',
'person.journeySplitNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC, e.eventType
LIMIT 100;
```

### 查看人员历程时间线 {#person-timeline}

调查人员最近的历程历史记录，包括步骤过渡、拆分选择和历程归因用户档案更新。

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
e.previousJourneyNodeID,
e.newJourneyNodeID,
e.journeyChoiceNumber,
e.journeyEntryCount,
e.attributeName,
e.attributeOldValue,
e.attributeNewValue
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID = 'PASTE_COMPLETE_PERSON_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```
