---
title: 设置核对清单
description: 完成Journey Optimizer B2B Prime实例的初始设置任务，包括用户访问配置和电子邮件可投放性基础架构。
autotag-review: '2026-06-12T23:06:52.179Z'
TQID: 'https://experienceleague.adobe.com/D8qXM-F4anA8IVYmdlaclUoxgTwqQptN36xYFpsuvHY'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f467931a-9b22-4ca8-869f-adfbd64061ceid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: de83abd4ca48e2dfda8a1900f7c8074232bb9d8e
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 11%

---

# 设置核对清单

完成这些任务以在您配置的[!DNL Journey Optimizer B2B Prime]实例中启用功能。

## 启用用户访问权限 {#enable-user-access}

当配置完成并且沙盒绑定后，为团队和用户配置[!DNL Journey Optimizer B2B Edition]访问权限。

<table>
<thead>
<tr>
<th colspan="2">任务</th>
<th>详细信息和说明</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>为用户提供产品访问和权限</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="任务的复选框"/></td>
<td>在Admin Console中创建Journey Optimizer B2B edition产品配置文件（仅限一次性/初始设置）</td>
<td><a href="./user-management.md#create-profile">创建配置文件</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="任务的复选框"/></td>
<td>在Admin Console中添加用户群组</td>
<td><a href="./user-management.md#add-user-group">添加用户群组</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="任务的复选框"/></td>
<td>编辑内置角色或创建具有产品权限的自定义角色</td>
<td><a href="./user-management.md#edit-role-permissions">编辑角色</a> <br/> <a href="./user-management.md#create-a-custom-role">创建自定义角色</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="任务的复选框"/></td>
<td>在Adobe Experience Platform中将用户或组添加到角色</td>
<td><a href="./user-management.md#add-users-to-a-role">添加用户</a><br/><a href="./user-management.md#add-user-groups-to-a-role">添加组</a></td>
</tr>
</tbody>
</table>

## 电子邮件送达率 {#email-deliverability}

在营销人员从历程发送电子邮件之前，请为您的组织配置发送基础架构，包括子域委派、电子邮件身份验证和渠道设置。

<table>
<thead>
<tr>
<th colspan="2">任务</th>
<th>详细信息和说明</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>配置电子邮件可投放性和渠道设置</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="任务的复选框"/></td>
<td>将子域委派给Adobe（完全委派或CNAME）</td>
<td><a href="./admin/configuration-email-deliverability.md#delegate-fully-delegated">已完全委派</a> <br/> <a href="./admin/configuration-email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="任务的复选框"/></td>
<td>为子域配置DMARC</td>
<td><a href="./admin/configuration-email-deliverability.md#configure-dmarc">配置DMARC</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="任务的复选框"/></td>
<td>查看和分配IP池</td>
<td><a href="./admin/configuration-email-deliverability.md#review-ip-pool">审查IP池</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="任务的复选框"/></td>
<td>创建电子邮件渠道配置</td>
<td><a href="./admin/configuration-email-deliverability.md#create-email-channel-configuration">配置电子邮件渠道</a></td>
</tr>
</tbody>
