---
title: 从受管辖模板创作
description: 了解如何将电子邮件创作与包含锁定内容组件的受管模板结合使用。
feature: Email Authoring, Content
role: User
exl-id: 1af996a6-a010-4899-96e9-bad76f93865c
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---

# 从受管辖模板创作

创建电子邮件模板时，内容设计者可以启用[管理（_内容锁定_）](./template-content-governance.md)。 利用治理功能，他们可以指定在帐户历程中使用时无法更改的设计部分。 当您[选择保存的模板](./email-authoring.md#select-a-template)来创作电子邮件时，可视设计器将加载该模板，以便您可以将其用作电子邮件的基础。

如果模板启用了管理，则右侧的“属性”面板中会显示警报。 您可以打开画布顶部的&#x200B;**[!UICONTROL 突出显示可编辑区域]**，以查看可在历程中使用的组件和内容元素。

![在受管辖的模板中查看可编辑区域](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

您还可以使用&#x200B;_导航树_&#x200B;确定锁定或可编辑的元素。 单击画布左侧的&#x200B;_导航树_&#x200B;图标（![链接图标](../assets/do-not-localize/icon-navigation-tree.svg)）以显示树。

![在受管辖的模板中查看可编辑区域](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

这些图标指示已应用的内容锁定设置。

| 图标 | 名称 | 描述 |
|------|------|-------------|
| ![只读图标](../assets/do-not-localize/icon-tree-lock.svg) | 只读 | 组件已锁定，无法编辑。 在根（_[!UICONTROL 正文]_）级别应用时，所有子组件都将被锁定且无法编辑。 |
| ![内容编辑图标](../assets/do-not-localize/icon-tree-content-lock.svg) | 内容锁定 | 在组件级别应用内容锁定。 |
| ![可编辑图标](../assets/do-not-localize/icon-edit.svg) | 可编辑 | 该组件是完全可编辑的。 但是，您可能无法删除该元素。 |
| ![内容编辑图标](../assets/do-not-localize/icon-tree-edit-text.svg) | 可编辑 — 仅内容 | 组件和样式是静态的，但您可以更改内容（如文本或图像）。 |
