---
title: 辅助函数
description: Journey Optimizer B2B edition中个性化辅助函数的参考指南。 其中包括字符串、日期、数学等的语法和示例。
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: 表达式、编辑器、语法、个性化
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '4857'
ht-degree: 6%

---

# 辅助函数

使用个性化编辑器中的帮助程序功能，通过操作数据、执行计算和格式化内容，准确高效地定义个性化内容体验。 探索并尝试使用这些功能、操作员和助手，了解他们如何协同工作，帮助您打造量身定制的数据驱动历程。

>[!AVAILABILITY]
>
>辅助函数适用于在[简化架构](../simplified-architecture.md)上配置的Journey Optimizer B2B edition环境。

## 聚合函数

使用聚合函数将多个值分组以形成单个汇总值。 您还可以使用数组和列表函数更轻松地定义与数组、列表和字符串的交互。

### 平均 {#average}

使用`average`函数返回数组中所有选定值的算术平均值。

+++句法

```sql
{%= average(array) %}
```

**示例**

以下操作将返回所有订单的平均价格。

```sql
{%=average(orders.order.price)%}
```

+++

### count {#count}

使用`count`函数返回给定数组中的元素数。

+++句法

```sql
{%= count(array) %}
```

**示例**

以下操作返回数组中的订单数。

```sql
{%= count(orders) %}
```

+++

### max {#max}

使用`max`函数返回数组中所有选定值中的最大值。

+++句法

```sql
{%= max(array) %}
```

**示例**

以下操作将返回所有订单的最高价格。

```sql
{%=max(orders.order.price)%}
```

+++

### min {#min}

使用`min`函数返回数组中所有选定值中的最小值。

+++句法

```sql
{%= min(array) %}
```

**示例**

以下工序返回所有订单的最低价格。

```sql
{%=min(orders.order.price) %}
```

+++

### sum {#sum}

使用`sum`函数返回数组中所有选定值的总和。

+++句法

```sql
{%= sum(array) %}
```

**示例**

以下操作返回所有订单价格的总和。

```sql
 {%=sum(orders.order.price)%}
```

+++

## 算术函数 {#maths}

使用算术函数对值执行基本计算。

### 添加 {#add}

使用`+`（相加）函数查找两个参数表达式的总和。

+++句法

```sql
{%= double + double %}
```

**示例**

以下操作对两个不同产品的价格求和。

```sql
{%= product1.price + product2.price %}
```

+++

### 乘 {#multiply}

使用`*`（乘法）函数查找两个参数表达式的乘积。

+++句法

```sql
{%= double * double %}
```

**示例**

以下操作将查找库存的产品和产品价格，以查找产品的总值。

```sql
{%= product.inventory * product.price %}
```

+++

### 减 {#substract}

使用`-`（减法）函数查找两个参数表达式的差异。

+++句法

```sql
{%= double - double %}
```

**示例**

以下操作找出两个不同产品之间的价格差异。

```sql
{%= product1.price - product2.price %}
```

+++

### 除 {#divide}

使用`/` （除）函数查找两个参数表达式的商。

+++句法

```sql
{%= double / double %}
```

**示例**

以下操作将查找已售产品总数与已挣金额总数之间的商数，以查看每个项目的平均成本。

```sql
{%= totalProduct.price / totalProduct.sold %}
```

+++

### 余数 {#remainder}

使用`%`（余数）函数在除以两个参数表达式后查找余数。

+++句法

```sql
{%= double % double %}
```

**示例**

以下操作检查人员的年龄是否可被5岁整除。

```sql
{%= person.age % 5 = 0 %}
```

+++

## 数组和列表函数 {#arrays}

使用这些函数可以更轻松地与数组、列表和字符串进行交互。

### countOnlyNull {#count-only-null}

使用`countOnlyNull`函数计算列表中空值的数量。

+++句法

```sql
{%= countOnlyNull(array) %}
```

**示例**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

返回3。

+++

### countWithNull {#count-with-null}

使用`countWithNull`函数对列表的所有元素（包括null值）进行计数。

+++句法

```sql
{%= countWithNull(array) %}
```

**示例**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

返回6。

+++

### distinct {#distinct}

使用`distinct`函数从已删除重复值的数组或列表中获取值。

+++句法

```sql
{%= distinct(array) %}
```

**示例**

以下操作指定在多个商店下订单的人员。

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

+++

### distinctCountWithNull {#distinct-count-with-null}

使用`distinctCountWithNull`函数计算列表中包括null值的不同值的数量。

+++句法

```sql
{%= distinctCountWithNull(array) %}
```

**示例**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

返回3。

+++

### head {#head}

使用`head`函数返回数组或列表中的第一个项。

+++句法

```sql
{%= head(array) %}
```

**示例**

以下操作将返回价格最高的前五个订单中的第一个。 有关`topN`函数的更多信息，请参见[数组`n`中的第一个](#first-n)。

```sql
{%= head(topN(orders,price, 5)) %}
```

+++

### topN {#first-n}

`topN`函数根据给定的数值表达式以降序排序数组，并返回前`N`项。 如果数组大小小于`N`，则返回整个排序的数组。

+++句法

```sql
{%= topN(array, value, amount) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的数组或列表。 |
| `{VALUE}` | 用于对数组或列表进行排序的属性。 |
| `{AMOUNT}` | 要返回的项目数。 |

**示例**

以下操作将返回价格最低的前五个订单。

```sql
{%= topN(orders,price, 5) %}
```

+++

### in {#in}

使用`in`函数确定项是数组还是列表的成员。

+++句法

```sql
{%= in(value, array) %}
```

**示例**

以下操作定义3月、6月或9月拥有生日的人员。

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

+++

### 包含 {#includes}

使用`includes`函数确定数组或列表是否包含给定项。

+++句法

```sql
{%= includes(array,item) %}
```

**示例**

以下操作定义其最喜爱的颜色包括红色的人员。

```sql
{%= includes(person.favoriteColors,"red") %}
```

+++

### 相交 {#intersects}

`intersects`函数用于确定两个数组或列表是否至少有一个公共成员。

+++句法

```sql
{%= intersects(array1, array2) %}
```

**示例**

以下操作定义其最喜爱的颜色至少包括红色、蓝色或绿色中的一种的人员。

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```

+++

<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

### bottomN {#last-n}

`bottomN`函数根据给定的数值表达式对数组进行升序排序，并返回前`N`项。 如果数组大小小于`N`，则返回整个排序的数组。

+++句法

```sql
{%= bottomN(array, value, amount) %}
```

| 参数 | 描述 |
| --------- | ----------- | 
| `{ARRAY}` | 要排序的数组或列表。 |
| `{VALUE}` | 用于对数组或列表进行排序的属性。 |
| `{AMOUNT}` | 要返回的项目数。 |

**示例**

以下操作将返回具有最高价格的最后5个订单。

```sql
{%= bottomN(orders,price, 5) %}
```

+++

### notIn {#notin}

使用`notIn`函数来确定项是否不是数组或列表的成员。

>[!NOTE]
>
>`notIn`函数&#x200B;*还*&#x200B;确保这两个值都不等于null。 因此，结果不是`in`函数的完全否定。

+++句法

```sql
{%= notIn(value, array) %}
```

**示例**

以下操作定义非三月、六月或九月的生日人员。

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```

+++

### subsetOf {#subset}

使用`subsetOf`函数确定特定数组（数组A）是否是另一个数组（数组B）的子集。 换句话说，数组A中的所有元素都是数组B的元素。

+++句法

```sql
{%= subsetOf(array1, array2) %}
```

**示例**

以下操作定义访问过他们喜欢的所有城市的人。

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

+++

### 超集 {#superset}

使用`supersetOf`函数确定特定数组（数组A）是否是另一个数组（数组B）的超集。 换句话说，该数组A包含数组B中的所有元素。

+++句法

```sql
{%= supersetOf(array1, array2) %}
```

**示例**

以下操作定义至少吃过一次寿司和比萨的人。

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

+++

## 日期和时间函数 {#date-time}

使用日期和时间函数对值执行日期和时间操作。

### addDays {#add-days}

`addDays`函数按指定的天数调整给定日期，使用正值递增和负值递减。

+++句法

```sql
{%= addDays(date, number) %}
```

**示例**

* 输入： `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* 输出： `2024-11-11T17:19:51Z`

+++

### addHours {#add-hours}

`addHours`函数按指定的小时数调整给定日期，使用正值递增，使用负值递减。

+++句法

```sql
{%= addHours(date, number) %}
```

**示例**

* 输入： `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* 输出： `2024-11-01T18:19:51Z`

+++

### addMinutes {#add-minutes}

`addMinutes`函数按指定的分钟数调整给定日期，使用正值递增，使用负值递减。

+++句法

```sql
{%= addMinutes(date, number) %}
```

**示例**

* 输入： `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* 输出： `2024-11-01T18:09:51Z`

+++

### addMonths {#add-months}

`addMonths`函数按指定的月数调整给定日期，使用正值递增，使用负值递减。

+++句法

```sql
{%= addMonths(date, number) %}
```

**示例**

* 输入： `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* 输出： `2025-01-01T17:19:51Z`

+++

### addSeconds {#add-seconds}

`addSeconds`函数使用正值递增和负值递减来按指定的秒数调整给定日期。

+++句法

```sql
{%= addSeconds(date, number) %}
```

**示例**

* 输入： `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* 输出： `2024-11-01T17:20:01Z`

+++

### addYears {#add-years}

`addYears`函数按指定的年数调整给定日期，使用正值递增，使用负值递减。

+++句法

```sql
{%= addYears(date, number) %}
```

**示例**

* 输入： `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* 输出： `2026-11-01T17:19:51Z`

+++

### 年龄 {#age}

使用`age`函数从给定日期检索年龄。

+++句法

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

+++

### ageInDays {#age-days}

`ageInDays`函数计算给定日期与当前日期之间经过的天数。 它对未来日期使用负值，对过去日期使用正值。

+++句法

```sql
{%= ageInDays(date) %}
```

**示例**

currentDate = 2025-01-07T12:17:10.720122+05:30 （亚洲/加尔各答）

* 输入： `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* 输出： `5`

+++

### ageInMonths {#age-months}

`ageInMonths`函数计算从给定日期到当前日期之间经过的月数。 它对未来日期使用负值，对过去日期使用正值。

+++句法

```sql
{%= ageInMonths(date) %}
```

**示例**

currentDate = 2025-01-07T12:22:46.993748+05:30（亚洲/加尔各答）

* 输入： `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* 输出： `12`

+++

### compareDates {#compare-dates}

`compareDates`函数将第一个输入日期与另一个输入日期进行比较。 如果date1等于date2，则返回0；如果date1在date2之前，则返回–1；如果date1在date2之后，则返回1。

+++句法

```sql
{%= compareDates(date1, date2) %}
```

**示例**

* 输入： `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* 输出： `-1`

+++

### convertZonedDateTime {#convert-zoned-date-time}

`convertZonedDateTime`函数将日期时间转换为给定时区。

+++句法

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

**示例**

* 输入： `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* 输出： `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

### currentTimeInMillis {#current-time}

使用`currentTimeInMillis`函数检索当前时间（以纪元毫秒为单位）。

+++句法

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

+++

### dateDiff {#date-diff}

使用`dateDiff`函数检索两个日期之间的天数差。

+++句法

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfMonth {#day-month}

`dayOfMonth`返回表示月份日期的数字。

+++句法

```sql
{%= dayOfMonth(datetime) %}
```

**示例**

* 输入： `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* 输出： `5`

+++

### DayofWeek {#day-week}

使用`dayOfWeek`函数检索星期几。

+++句法

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfYear {#day-year}

使用`dayOfYear`函数检索一年中的第几天。

+++句法

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInSeconds {#diff-seconds}

`diffInSeconds`函数返回两个日期之间的差值（以秒为单位）。

+++句法

```sql
{%= diffInSeconds(endDate, startDate) %}
```

**示例**

* 输入： `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* 输出： `50`

+++

### extractHours {#extract-hours}

`extractHours`函数从给定时间戳中提取小时组件。

+++句法

```sql
{%= extractHours(date) %}
```

**示例**

* 输入： `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `17`

+++

### extractMinutes {#extract-minutes}

`extractMinutes`函数从给定时间戳中提取分钟组件。

+++句法

```sql
{%= extractMinutes(date) %}
```

**示例**

* 输入： `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `19`

+++

### extractMonths {#extract-months}

`extractMonth`函数从给定时间戳中提取月份组件。

+++句法

```sql
{%= extractMonths(date) %}
```

**示例**

* 输入： `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `11`

+++

### extractSeconds {#extract-seconds}

`extractSeconds`函数从给定时间戳中提取第二个组件。

+++句法

```sql
{%= extractSeconds(date) %}
```

**示例**

* 输入： `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `51`

+++

### formatdate {#format-date}

使用`formatDate`函数设置日期时间值的格式。 格式应为有效的Java `DateTimeFormat`模式。

+++句法

```sql
{%= formatDate(datetime, format) %}
```

其中第一个字符串是日期属性，第二个值是您希望如何转换和显示日期。

>[!NOTE]
>
> 如果日期模式无效，日期将恢复为ISO标准格式。
>
> 您可以使用[Oracle文档](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}中概述的Java日期格式函数

**示例**

以下操作将返回以下格式的日期：MM/DD/YY。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

#### 图案字符 {#pattern-characters}

某些样式字母可能看起来类似，但表示不同的概念。

| 模式 | 含义 | 示例（针对`2023-12-31T10:15:30Z`） |
|---------|---------|--------------------------------------|
| `y` | 日历年（标准年） | `2023` |
| `Y` | 基于周的年份(ISO 8601)。 年度边界可能不同。 | `2024` （2023年12月31日为2024年的第一周） |
| `M` | 月份（1-12或文本，如`Jan`、`January`） | `12`或`Dec` |
| `m` | 小时制的分钟(0-59) | `15` |
| `d` | 日期(1-31) | `31` |
| `D` | 每年的某一日(1-366) | `365` |

#### 支持区域设置的日期格式 {#format-date-locale}

您可以使用`formatDate`函数将日期时间值格式化为相应的区分语言的表示形式，如所需的区域设置。 格式应为有效的Java `DateTimeFormat`模式。

+++句法

```sql
{%= formatDate(datetime, format, locale) %}
```

其中第一个字符串是日期属性，第二个值是您希望如何转换和显示日期，第三个值以字符串格式表示区域设置。

>[!NOTE]
>
> 如果日期模式无效，日期将恢复为ISO标准格式。
>
> 您可以使用[Oracle文档](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html)中概述的Java日期格式函数。
>
> 您可以使用[Oracle文档](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html)和[支持的区域设置](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html)中概述的格式设置和有效区域设置。

**示例**

以下操作返回以下格式的日期：MM/dd/YY和区域设置FRANCE。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

+++

### getCurrentZonedDateTime {#get-current-zoned-date-time}

`getCurrentZonedDateTime`函数返回包含时区信息的当前日期和时间。

+++句法

```sql
{%= getCurrentZonedDateTime() %}
```

**示例**

* 输入： `{%= getCurrentZonedDateTime() %}`
* 输出： `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

### diffinHours {#hours-difference}

`diffInHours`函数返回两个日期之间的小时数差。

+++句法

```sql
{%= diffInHours(endDate, startDate) %}
```

**示例**

* 输入： `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* 输出： `10`

+++

### diffinMinutes {#diff-minutes}

`diffInMinutes`函数返回两个日期之间的分钟数差。

+++句法

```sql
{%= diffInMinutes(endDate, startDate) %}
```

**示例**

* 输入： `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* 输出： `60`

+++

### diffinMonths {#months-difference}

`diffInMonths`函数返回两个日期之间的月数差。

+++句法

```sql
{%= diffInMonths(endDate, startDate) %}
```

**示例**

* 输入： `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* 输出： `3`

+++

### setDays {#set-days}

使用`setDays`函数为给定的日期时间设置月中日（该月中的第几天）。

+++句法

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### setHours {#set-hours}

使用`setHours`函数设置日期时间的小时。

+++句法

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### toDateTime {#string-to-date-time}

`toDateTime`函数将字符串转换为日期。 对于无效的输入，它返回纪元日期作为输出。

+++句法

```sql
{%= toDateTime(string, string) %}
```

**示例**

* 输入： `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* 输出： `2024-11-01T17:19:51Z`

+++

### toUTC {#to-utc}

使用`toUTC`函数将日期时间转换为UTC。

+++句法

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### truncateToStartOfDay {#truncate-day}

使用`truncateToStartOfDay`函数，通过将给定日期时间设置为time为00:00的该天开始来修改该日期。

+++句法

```sql
{%= truncateToStartOfDay(date) %}
```

**示例**

* 输入： `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* 输出： `2024-11-01T00:00Z`

+++

### truncatetostartofQuarter {#truncate-quarter}

使用`truncateToStartOfQuarter`函数将日期时间截断为其季度的第一天（如1月1日、4月1日、7月1日、10月1日），时间为00:00。

+++句法

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

**示例**

* 输入： `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `2024-10-01T00:00Z`

+++

### truncateToStartOfWeek {#truncate-week}

`truncateToStartOfWeek`函数通过将给定日期时间设置为一周的开始（星期一为00:00）来修改该日期。

+++句法

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

**示例**

* 输入： `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* 输出： `2024-11-18T00:00Z // monday`

+++

### truncateToStartOfYear {#truncate-year}

使用`truncateToStartOfYear`函数修改给定的日期时间，方法是：在00:00处将其截断为一年的第一天（1月1日）。

+++句法

```sql
{%= truncateToStartOfYear(dateTime) %}
```

**示例**

* 输入： `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `2024-01-01T00:00Z`

+++

### weekOfYear {#week-of-year}

使用`weekOfYear`函数检索年中哪一周。

+++句法

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInYear {#diff-years}

使用`diffInYears`函数返回两个日期之间的年数差。

+++句法

```sql
{%= diffInYears(endDate, startDate) %}: int
```

**示例**

* 输入： `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* 输出： `5`

+++

## 运算符函数 {#operators}

使用布尔和比较函数执行逻辑评估。

### 和 {#and}

`and`函数用于创建逻辑连接。

+++句法

```sql
{%= query1 and query2 %}
```

**示例**

以下操作将返回所有在本国（法国）和出生年（1985年）居住的人。

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

+++

### 或 {#or}

`or`函数用于创建逻辑分离。

+++句法

```sql
{%= query1 or query2 %}
```

**示例**

以下操作将返回所有在本国（法国）或出生年（1985年）居住的人。

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

+++

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

### 等于 {#operator-equals}

`=` （等于）函数检查一个值或表达式是否等于另一个值或表达式。

+++句法

```sql
{%= expression = value %}
```

**示例**

以下操作检查家庭地址国家/地区是否为法国。

```sql
{%= profile.homeAddress.country = "France" %}
```

+++

### 不等于 {#notequal}

`!=` （不等于）函数检查一个值或表达式是&#x200B;**不是**&#x200B;等于另一个值或表达式。

+++句法

```sql
{%= expression != value %}
```

**示例**

以下操作检查家庭地址国家/地区是否不是法国。

```sql
{%= profile.homeAddress.country != "France" %}
```

+++

### 大于 {#greaterthan}

使用`>` （大于）函数检查第一个值是否大于第二个值。

+++句法

```sql
{%= expression1 > expression2 %}
```

**示例**

以下操作严格定义了1970年后出生的人。

```sql
{%= profile.person.birthYear > 1970 %}
```

+++

### 大于或等于 {#greaterthanorequal}

使用`>=` （大于或等于）函数检查第一个值是否大于或等于第二个值。

+++句法

```sql
{%= expression1 >= expression2 %}
```

**示例**

以下操作定义了1970年或之后出生的人。

```sql
{%= profile.person.birthYear >= 1970 %}
```

+++

### 小于 {#lessthan}

使用`<` （小于）比较函数检查第一个值是否小于第二个值。

+++句法

```sql
{%= expression1 < expression2 %}
```

**示例**

以下操作定义了2000年之前出生的人。

```sql
{%= profile.person.birthYear < 2000 %}
```

+++

### 小于或等于{#lessthanorequal}

使用`<=` （小于或等于）比较函数检查第一个值是否小于或等于第二个值。

+++句法

```sql
{%= expression1 <= expression2 %}
```

**示例**

以下操作定义了2000年或之前出生的人。

```sql
{%= profile.person.birthYear <= 2000 %}
```

+++

## 动态函数 {#dynamic-helpers}

使用动态帮助程序函数为动态个性化使用条件评估、迭代和变量分配。

### 默认回退值 {#default-value}

如果属性为空或null，则使用`Default Fallback Value`帮助程序返回默认回退值。 此机制适用于配置文件属性和历程事件。

+++句法

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

在此示例中，如果此配置文件的`there`属性为空或null，则显示值`firstName`。

+++

### if（条件） {#if-function}

`if`帮助程序用于定义条件块。
如果表达式求值返回true，则会呈现块，否则将跳过该块。

+++句法

```sql
{%#if contains(account.accountOrganization.primaryEmailDomain, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

在`if`帮助程序之后，您可以输入`else`语句以指定要执行的代码块（如果相同条件为false）。
`elseif`语句指定了一个新条件以测试第一个语句是否返回false。


**格式**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

<!-- 
**Examples**

* **Render different store links based on conditional expressions**

    ```sql
    {%#if profile.homeAddress.countryCode = "FR"%}
    <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
    {%else%}
    <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
    {%/if%}
    ```

* **Determine email address extension**

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Add a conditional link**

    The following operation adds a link to the `www.adobe.com/academia` website for profiles with '.edu' email addresses only, the `www.adobe.com/org` website for profiles with '.org' email addresses, and the default URL `www.adobe.com/users` for all other profiles:

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Conditional content based on audience membership**

    ```sql
    {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
    Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
    {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
    Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
    {%/if%}
    ```
-->

+++

### Unless {#unless}

使用`unless`帮助程序定义条件块。 通过对`if`帮助程序的反对，如果表达式求值返回false，则呈现块。

+++句法

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**示例**

根据电子邮件地址扩展呈现某些内容：

```sql
{%#unless endsWith(account.accountOrganization.primaryEmailDomain}, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

+++

### 每个 {#each}

使用`each`辅助函数对数组进行迭代。

辅助函数结构为```{{#each ArrayName}}```您的内容`{{/each}}`

您可以在块中使用关键字`this`来引用单个数组项。 使用`{{@index}}`渲染数组元素的索引。

+++句法

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**示例**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**示例**

呈现此用户在其购物车中拥有的产品列表：

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

+++

### 替换为 {#with}

使用`with`帮助程序更改模板部分的评估令牌。

+++句法

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

`with`辅助函数也可用于定义快捷键变量。

**示例**

使用`with`将长变量名称别名为短变量名称：

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

+++

### let {#let}

`let`函数允许将表达式存储为变量，以便稍后在查询中使用。

+++句法

```sql
{% let variable = expression %} {{variable}}
```

**示例**

以下示例允许您计算购物车中价格在100和1000之间的产品的总价。

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

+++

## 执行元数据 {#execution-metadata}

>[!AVAILABILITY]
>
>此功能处于有限可用状态。 请联系 Adobe 代表以获取访问权限。

使用`executionMetadata`动态捕获自定义键值对并将其存储到消息执行上下文中。

利用此功能，您可以将上下文信息附加到营销活动或历程中的任何本机操作。 使用它可将实时投放上下文数据导出到外部系统，以实现各种目的，例如跟踪、分析、个性化和下游处理。

>[!NOTE]
>
>自定义操作不支持`executionMetadata`函数。

例如，您可以使用`executionMetadata`帮助程序将特定ID附加到发送给每个用户档案的每个投放。 此信息在运行时生成，随后可导出扩充的执行元数据以用于与外部报告平台的下游协调。

+++句法

```
{{executionMetadata key="your_key" value="your_value"}}
```

在此语法中，`key`引用元数据名称，`value`是要保留的元数据。

**工作原理**

从营销活动或历程中的渠道内容中选择任何元素，并使用个性化编辑器将`executionMetadata`帮助程序添加到此元素。

>[!NOTE]
>
>显示内容本身时，`executionMetadata`函数不可见。

在运行时，元数据值被添加到现有&#x200B;**[!UICONTROL 消息反馈事件数据集]**&#x200B;中，并添加了以下架构：

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!IMPORTANT]
>
>每个操作的键值对的上限为2kb。 如果超过2Kb限制，则仍会投放消息，但可以截断任何键值对。

**示例**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

在此示例中，假设`profile.person.name.firstName` = &quot;Alex&quot;，则生成的实体为：

```
{
  "key": "firstName",
  "value": "Alex"
}
```

+++

## 映射函数 {#maps}

在个性化中使用映射函数可简化与映射的交互。

### get {#get}

使用`get`函数检索给定键的映射值。

+++句法

```sql
{%= get(map, string) %}
```

**示例**

以下操作获取键`example@example.com`的标识映射值。

```sql
{%= get(identityMap,"example@example.com") %}
```

+++

### 键 {#keys}

使用`keys`函数检索给定映射的所有键。

+++句法

```sql
{%= keys(map) %}
```

**示例**

以下操作检索映射`identityMap`的所有键。

```sql
{%= keys(identityMap) %}
```

+++

### 值 {#values}

`values`函数用于检索给定映射的所有值。

+++句法

```sql
{%= values(map) %}
```

**示例**

以下操作检索映射`identityMap`的所有值。

```sql
{%= values(identityMap) %}
```

+++

## 数学函数 {#math}

了解如何在个性化编辑器中使用数学函数。

### 绝对 {#absolute}

使用`absolute`函数将一个数字转换为其绝对值。

+++句法

```sql
{%= absolute(int) %}: int
```

+++

### 格式数字 {#format-number}

使用`formatNumber`函数将任意数字格式化为其区分语言的表示形式。

它接受一个数字和一个表示区域设置的字符串，并返回所需区域设置中数字的格式化字符串。

+++句法

```sql
{%= formatNumber(number/double,string) %}: string
```

您可以使用[Oracle文档](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html)和[支持的区域设置](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}中概述的格式设置和有效区域设置

**示例**

此查询返回一个阿拉伯文格式字符串(对应于123456.789)作为输入数字。

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

+++

### random {#random}

使用`random`函数返回0到1之间的随机值。

+++句法

```sql
{%= random() %}: double
```

+++

### roundDown {#round-down}

使用`roundDown`函数向下舍入数字。

+++句法

```sql
{%= roundDown(double) %}: double
```

+++

### 汇总 {#round-up}

使用`roundUp`函数对数字进行向上四舍五入。

+++句法

```sql
{%= roundUp(double) %}: double
```

+++

### toHexString {#to-hex-string}

`toHexString`函数将任意数字转换为十六进制字符串。

+++句法

```sql
{%= toHexString(number) %}: string
```

**示例**

此查询返回十六进制值158为9e。

```sql
{%= toHexString(158) %}
```

+++

### toInt {#to-int}

使用`toInt`函数将类型（数字、双精度、整数、长整数、浮点数、短整数、字节、布尔值、字符串）转换为整数。

+++句法

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**示例**

此查询返回42.6的整数值作为42。

```sql
{%= toInt(42.6) %}: integer
```

+++

### toPercentage {#to-percentage}

使用`toPercentage`函数将数字转换为百分比。

+++句法

```sql
{%= toPercentage(double) %}: string
```

+++

### toPrecision {#to-precision}

使用`toPrecision`函数将数字转换为所需的精度。

+++句法

```sql
{%= toPrecision(double,int) %}: string
```

+++

### toString {#to-string}

`toString`函数将任意数字转换为字符串表示形式。

+++句法

```sql
{%= toString(string) %}: string
```

**示例**

此查询返回`"12"`。

```sql
{%= toString(12) %} 
```

+++

## 目标函数 {#objects}

用于查询对象属性或属性的对象函数。

### isNull {#isNull}

`isNull`函数确定对象引用是否不存在。

+++句法

```sql
{%= isNull(object) %}
```

**示例**

以下操作检查人员的家庭地址是否不存在。

```sql
{%= isNull(person.homeAddress) %}
```

+++

### isNotNull {#isNotNull}

`isNotNull`函数确定是否存在对象引用。

+++句法

```sql
{%= isNotNull(object) %}
```

**示例**

以下操作检查人员的家庭地址是否存在。

```sql
{%= isNotNull(person.homeAddress) %}
```

+++

## 字符串函数 {#string-functions}

了解如何在个性化编辑器中使用字符串函数。

### camelCase {#camelCase}

`camelCase`函数将字符串中每个单词的第一个字母变为大写。

+++句法

```sql
{%= camelCase(string)%}
```

**示例**

以下函数将用户档案的街道地址中单词的第一个字母转换为大写。

```sql
{%= camelCase(profile.homeAddress.street) %}
```

+++

### charCodeAt {#char-code-at}

`charCodeAt`函数返回字符的ASCII值，如JavaScript中的`charCodeAt`函数。 它采用字符串和整数（定义字符的位置）作为输入参数，并返回其对应的ASCII值。

+++句法

```sql
{%= charCodeAt(string,int) %}: int
```

**示例**

以下函数返回`o` (111)的ASCII值。

```sql
{%= charCodeAt("some", 1)%}
```

+++

### concat {#concate}

`concat`函数将两个字符串合并为一个。

+++句法

```sql
{%= concat(string,string) %}
```

**示例**

以下函数将用户档案城市和国家/地区组合在一个字符串中。

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

+++

### 包含 {#contains}

使用`contains`函数确定一个字符串是否包含指定的子字符串。

+++句法

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `STRING_1` | 要检查的字符串。 |
| `STRING_2` | 要在第一个字符串中搜索的字符串。 |
| `CASE_SENSITIVE` | 用于确定检查是否区分大小写，的可选参数。 可能的值： true （默认） / false。 |

**示例**

* 以下函数检查用户档案名字是否包含字母A（大写或小写）。 如果配置文件包含，则返回`true`。 如果不是，则返回`false`。

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* 以下查询将区分大小写确定人员的电子邮件地址是否包含字符串`2010@gm`。

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

+++

### doesNotContain {#doesNotContain}

使用`doesNotContain`函数确定一个字符串是否不包含指定的子字符串。

+++句法

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `STRING_1` | 要检查的字符串。 |
| `STRING_2` | 要在第一个字符串中搜索的字符串。 |
| `CASE_SENSITIVE` | 用于确定检查是否区分大小写，的可选参数。 可能的值： true （默认） / false。 |

**示例**

以下查询区分大小写确定人员的电子邮件地址是否不包含字符串`2010@gm`。

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```

+++

### doesNotEndWith {#doesNotEndWith}

使用`doesNotEndWith`函数可确定字符串是否不以指定的子字符串结尾。

+++句法

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写，的可选参数。 可能的值： true （默认） / false。 |

**示例**

以下查询将区分大小写确定此人的电子邮件地址是否不以`.com`结尾。

```sql
doesNotEndWith(person.emailAddress,".com")
```

+++

### doesNotStartWith {#doesNotStartWith}

使用`doesNotStartWith`函数确定字符串是否不以指定的子字符串开头。

+++句法

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写，的可选参数。 可能的值： true （默认） / false。 |

**示例**

以下查询区分大小写确定人员的姓名是否不以`Joe`开头。

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

+++

### encode64 {#encode64}

使用`encode64`函数对字符串进行编码，以保留个人信息(PI)，例如包含在URL中。

+++句法

```sql
{%= encode64(string) %}
```

+++

### endsWith {#endsWith}

使用`endsWith`函数确定字符串是否以指定的子字符串结尾。

+++句法

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写，的可选参数。 可能的值： true （默认） / false。 |

**示例**

以下查询将区分大小写确定此人的电子邮件地址是否以`.com`结尾。

```sql
{%= endsWith(person.emailAddress,".com") %}
```

+++

### 等于 {#equals}

使用`equals`函数可确定字符串是否等于指定的字符串（区分大小写）。

+++句法

```sql
{%= equals(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串进行比较的字符串。 |

**示例**

以下查询将区分大小写确定人员的姓名是否为`John`。

```sql
{%=equals(profile.person.name,"John") %}
```

+++

### equalsIgnoreCase {#equalsIgnoreCase}

使用`equalsIgnoreCase`函数确定一个字符串是否等于指定的字符串，不区分大小写。

+++句法

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串进行比较的字符串。 |

**示例**

以下查询在不区分大小写的情况下确定人员姓名是否为`John`。

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

+++

### extractEmailDomain {#extractEmailDomain}

使用`extractEmailDomain`函数提取电子邮件地址的域。

+++句法

```sql
{%= extractEmailDomain(string) %}
```

**示例**

以下查询提取个人电子邮件地址的电子邮件域。

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

+++

### formatCurrency {#format-currency}

使用`formatCurrency`函数根据第二个参数中作为字符串传递的区域设置，将任意数字转换为相应的区分语言的货币表示形式。

+++句法

```sql
{%= formatCurrency(number/double,string) %}: string
```

**示例**

此查询返回56.00英镑

```sql
{%= formatCurrency(56L,"en_GB") %}
```

+++

### getUrlHost {#get-url-host}

使用`getUrlHost`函数检索URL的主机名。

+++句法

```sql
{%= getUrlHost(string) %}: string
```

**示例**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

返回“www.myurl.com”

+++

### getUrlPath {#get-url-path}

使用`getUrlPath`函数在URL的域名后检索路径。

+++句法

```sql
{%= getUrlPath(string) %}: string
```

**示例**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

返回“/contact.html”

+++

### getUrlProtocol {#get-url-protocol}

使用`getUrlProtocol`函数检索URL的协议。

+++句法

```sql
{%= getUrlProtocol(string) %}: string
```

**示例**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

返回“http”

+++

### indexOf {#index-of}

使用`indexOf`函数返回第二个参数在第一个参数中第一次出现的位置。 如果没有匹配项，则返回–1。

+++句法

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个参数中搜索的字符串 |

**示例**

```sql
{%= indexOf("hello world","world" ) %}
```

返回6。

+++

### isEmpty {#isEmpty}

使用`isEmpty`函数确定字符串是否为空。

+++句法

```sql
{%= isEmpty(string) %}
```

**示例**

如果个人资料的手机号码为空，则以下函数返回“true”。 否则，它将返回`false`。

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

+++

### isNotEmpty {#is-not-empty}

使用`isNotEmpty`函数确定字符串是否不为空。

+++句法

```sql
{= isNotEmpty(string) %}: boolean
```

**示例**

如果个人资料的手机号码不为空，则以下函数返回“true”。 否则，它将返回`false`。

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

+++

### lastIndexOf {#last-index-of}

使用`lastIndexOf`函数返回第二个参数在第一个参数中最后一次出现的位置。 如果没有匹配项，则返回–1。

+++句法

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个参数中搜索的字符串 |

**示例**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

返回7。

+++

### leftTrim {#leftTrim}

使用`leftTrim`函数从字符串的开头删除空格。

+++句法

```sql
{%= leftTrim(string) %}
```

+++

### length {#length}

使用`length`函数获取字符串或表达式中的字符数。

+++句法

```sql
{%= length(string) %}
```

**示例**

以下函数返回用户档案的城市名称的长度。

```sql
{%= length(profile.homeAddress.city) %}
```

+++

### 点赞 {#like}

使用`like`函数确定字符串是否与指定的模式匹配。

+++句法

```sql
{%= like(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串匹配的表达式。 创建表达式时支持使用两个特殊字符： `%`和`_`。 <ul><li>`%`用于表示零个或更多字符。</li><li>`_`只用于表示一个字符。</li></ul> |

**示例**

以下查询将检索用户档案所在的所有城市，这些城市包含模式`es`。

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

+++

### lowerCase {#lower}

使用`lowerCase`函数将字符串转换为小写字母。

+++句法

```sql
{%= lowerCase(string) %}
```

**示例**

此函数将用户档案的名字转换为小写字母。

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

+++

### matches {#matches}

使用`matches`函数确定字符串是否与特定的正则表达式匹配。 有关正则表达式中匹配模式的详细信息，请参阅[Oracle文档](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html)。

+++句法

```sql
{%= matches(STRING_1, STRING_2) %}
```

**示例**

以下查询在不区分大小写的情况下确定人员的名称是否以`John`开头。

```sql
{%= matches(person.name.,"(?i)^John") %}
```

+++

### 蒙版 {#mask}

使用`mask`函数将字符串的一部分替换为“X”字符。

+++句法

```sql
{%= mask(string,integer,integer) %}
```

**示例**

以下查询将“123456789”字符串替换为“X”字符，但前两个字符和后两个字符除外。

```sql
{%= mask("123456789",1,2) %}
```

查询返回`1XXXXXX89`。

+++

### md5 {#md5}

使用`md5`函数计算并返回字符串的md5哈希。

+++句法

```sql
{%= md5(string) %}: string
```

**示例**

```sql
{%= md5("hello world") %}
```

返回“5eb63bbe01eeed093cb22bb8f5acdc3”

+++

### notEqualto {#notEqualTo}

使用`notEqualTo`函数来确定一个字符串是否不等于指定的字符串。

+++句法

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串进行比较的字符串。 |

**示例**

以下查询将区分大小写确定人员的姓名是否为`John`。

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

+++

### notEqualWithIgnoreCase {#not-equal-with-ignore-case}

使用`notEqualWithIgnoreCase`函数比较两个字符串（忽略大小写）。

+++句法

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串进行比较的字符串。 |

**示例**

以下查询确定人员姓名是否为`john`，不区分大小写。

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

+++

### 正则表达式组 {#regexGroup}

使用`regexGroup`函数根据提供的正则表达式提取特定信息。

+++句法

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING}` | 要检查的字符串。 |
| `{EXPRESSION}` | 要与第一个字符串匹配的正则表达式。 |
| `{GROUP}` | 要匹配的表达式组。 |

**示例**

以下查询从电子邮件地址中提取域名。

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

+++

### replace {#replace}

使用`replace`函数将字符串中的给定子字符串替换为另一个子字符串。

+++句法

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 必须替换子字符串的字符串。 |
| `{STRING_2}` | 要替换的子字符串。 |
| `{STRING_3}` | 替换子字符串。 |

**示例**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

返回`Hello Mark, here is your monthly newsletter!`

+++

### replaceAll {#replaceAll}

使用`replaceAll`函数将匹配正则表达式的所有文本子字符串替换为指定的文本替换字符串。 正则表达式对`\`和`+`具有特殊处理，并且所有正则表达式都遵循PQL转义策略。 替换过程从字符串的开头到结尾进行，例如，将字符串`aa`中的`b`替换为`aaa`将导致`ba`而不是`ab`。

+++句法

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> 当用作第二个参数的表达式是特殊正则表达式时，请使用双反斜杠(`//`)。  特殊正则表达式字符包括：[.， +， *， ？， ^， $， (， )， [，]， {， }， |， \.]
> 
> 请参阅[Oracle文档](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}以了解详情。
>

+++

### rightTrim {#rightTrim}

`rightTrim`函数删除字符串末尾的空格。

+++句法

```sql
{%= rightTrim(string) %}
```

+++

### sha256 {#sha256}

`sha256`函数计算并返回字符串的sha256哈希。

+++句法

```sql
{%= sha256(string) %} : string
```

**示例**

```sql
{%= sha256("Eliechxh")%}
```

返回`0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

+++

### split {#split}

使用`split`函数按给定字符拆分字符串。

+++句法

```sql
{%= split(string,string) %}
```

+++

### startsWith {#startsWith}

使用`startsWith`函数确定字符串是否以指定的子字符串开头。

+++句法

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写，的可选参数。 默认情况下，设置为true。 |

**示例**

以下查询区分大小写确定人员的名称是否以`Joe`开头。

```sql
{%= startsWith(person.name,"Joe") %}
```

+++

### stringToDate {#string-to-date}

`stringToDate`函数将一个字符串值转换为日期时间值。 它采用两个参数：日期时间的字符串表示和格式化器的字符串表示。

+++句法

```sql
{= stringToDate("date-time value","formatter" %}
```

**示例**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

+++

### string_to_integer {#string-to-integer}

使用`string_to_integer`函数将字符串值转换为整数值。

+++句法

```sql
{= string_to_integer(string) %}: int
```

+++

### stringToNumber {#string-to-number}

使用`stringToNumber`函数将字符串转换为数字。 对于无效的输入，它返回相同的字符串作为输出。

+++句法

```sql
{%= stringToNumber(string) %}: double
```

+++

### substr {#sub-string}

使用`substr`函数返回字符串表达式在开始索引和结束索引之间的子字符串。

+++句法

```sql
{= substr(string, integer, integer) %}: string
```

+++

### titleCase {#titleCase}

使用`titleCase`函数将字符串中每个单词的首字母大写。

+++句法

```sql
{%= titleCase(string) %}
```

**示例**

如果该人员住在华盛顿商业街，则此函数返回`Washington High Street`。

```sql
{%= titleCase(profile.person.location.Street) %}
```

+++

### toBool {#to-bool}

使用`toBool`函数将参数值转换为布尔值，具体取决于其类型。

+++句法

```sql
{= toBool(string) %}: boolean
```

+++

### toDateTime {#to-date-time}

使用`toDateTime`函数将字符串转换为日期。 对于无效的输入，它返回纪元日期作为输出。

+++句法

```sql
{%= toDateTime(string, string) %}: date-time
```

+++

### toDateTimeOnly {#to-date-time-only}

使用`toDateTimeOnly`函数将参数值转换为仅日期时间值。 对于无效的输入，它返回纪元日期作为输出。 此函数接受字符串、日期、长字段和整数字段类型。

+++句法

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

+++

### trim {#trim}

`trim`函数删除字符串开始和结束位置的所有空格。

+++句法

```sql
{%= trim(string) %}
```

+++

### 大写 {#upper}

`upperCase`函数将字符串转换为大写字母。

+++句法

```sql
{%= upperCase(string) %}
```

**示例**

此函数将用户档案的姓氏转换为大写字母。

```sql
{%= upperCase(profile.person.name.lastName) %}
```

+++

### urlDecode {#url-decode}

使用`urlDecode`函数对url编码的字符串进行解码。

+++句法

```sql
{%= urlDecode(string) %}: string
```

+++

### urlEncode {#url-encode}

使用`urlEncode`函数将字符串编码为URL。

+++句法

```sql
{%= urlEncode(string) %}: string
```

+++
