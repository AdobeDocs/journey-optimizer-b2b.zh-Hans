---
title: 个性化语法
description: 了解Journey Optimizer B2B edition中基于Handlebars的个性化语法，包括表达式、帮助程序、文本类型和格式规则。
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: 表达式、编辑器、语法、个性化
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 2%

---

# 个性化语法 {#personalization-syntax}

[!DNL Journey Optimizer B2B Edition] [个性化编辑器](./personalization.md#personalization-editor)中的表达式基于&#x200B;_Handlebars_&#x200B;模板语法。 它使用模板和输入对象来生成HTML或其他文本格式。 Handlebars模板看起来像包含嵌入Handlebars表达式的常规文本。

有关Handlebars及其工作方式的更多详细信息，请参阅[HandlebarsJS文档](https://handlebarsjs.com/){target="_blank"}。

## 一般规则

简单表达式示例：

```
{{account.accountName}}
```

其中：

* `account`是一个命名空间。
* `accountName`是由属性组成的令牌。

  >[!NOTE]
  >
  >在[Adobe Experience Platform XDM架构](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/home){target="_blank"}中定义了属性结构。

* 标识符可以是除以下字符之外的任意Unicode字符：

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* 语法区分大小写。

* 仅在路径表达式的第一部分中允许使用单词&#x200B;**true**、**false**、**null**&#x200B;和&#x200B;**undefined**。

* 在Handlebars中，{\{expression}\}返回的值是&#x200B;_HTML转义_。 如果表达式包含`&`，则返回的HTML转义输出将生成为`&amp;`。 如果不希望Handlebars转义值，请使用+triple-stash_。

<!-- For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. -->

* 对于文本函数参数，模板化语言解析器不支持单个未转义的反斜杠(`\`)符号。 此字符必须使用额外的反斜杠(`\`)符号进行转义。 例如：

  ```
  {%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}
  ```

## 辅助程序 {#helpers-all}

Handlebars辅助函数是可以附加参数的简单标识符。 每个参数都是一个Handlebars表达式。 可以从电子邮件模板中的任何上下文中访问这些帮助程序。

```sql
{{#each account.accountOrganization.annualRevenue.amount}}
    <li>{{this.name}}</li>
{{/each }}
```

<!-- These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name. 

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). -->

有关这些函数的更多详细信息，请参阅[辅助函数](./personalization-helper-functions.md)。

## 文本类型 {#literal-types}

[!DNL Adobe Journey Optimizer B2B Edition]支持以下文本类型：

| 文本 | 定义 |
| ------- | ---------- |
| 字符串 | 由双引号括起来的字符组成的数据类型。 <br>示例： `"prospect"`，`"jobs"`，`"articles"` |
| 布尔值 | true或false的数据类型。 |
| 整数 | 表示整数的数据类型。 它可以是正数、负数或零。 <br>示例： `-201`，`0`，`412` |
| 数组 | 由一组其他文字值组成的数据类型。 它使用方括号将不同的值分组，并使用逗号分隔不同的值。<br> **注意：**&#x200B;您不能直接访问数组中项的属性。 <br>示例： `[1, 4, 7]`，`["US", "FR"]` |

>[!CAUTION]
>
>**xEvent**&#x200B;变量的使用在个性化表达式中不可用。 对xEvent的任何引用都会导致验证失败。
