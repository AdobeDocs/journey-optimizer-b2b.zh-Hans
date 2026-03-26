---
title: 简化的架构设置
description: 在简化的架构上设置Journey Optimizer B2B edition 。 配置XDM架构、电子邮件/短信渠道、Marketo Engage历程操作和用户。
feature: Setup, Administration
role: Admin, Data Engineer
exl-id: 81232976-09d6-4e10-a034-5c193a63b7df
source-git-commit: 53bf3ce685079df16752af49c3b61f583f0b72e7
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 100%

---

# 简化的架构设置

Adobe Journey Optimizer B2B Edition 现已采用简化架构。 凭借此架构，Journey Optimizer B2B edition和Marketo Engage将不再位于同一系统和同一数据存储中。 Journey Optimizer B2B Edition 仅从 Adobe Experience Platform 接收数据。 但是，它继续依赖Marketo Engage权利和一些后端功能（如电子邮件投放）来配置和配置系统。

简化的架构是解锁Journey Optimizer B2B edition中新功能的基础：

* **轻松统一和扩展您的数据：**&#x200B;新平台支持复杂的数据模型，包括自定义对象、购买群组和帐户事件。

* **连接多个Adobe Marketo Engage实例：**&#x200B;在一个位置管理和统一多个Marketo Engage环境中的数据。

* **保护您的数据安全：**&#x200B;高级隐私和安全功能有助于保护您的客户信息。 （_即将推出_）

* **面向未来构建：**&#x200B;此升级为您准备好持续的改进和创新。

对于为此架构配置的环境，请使用以下配置准则。

使用此核对清单按照简化的架构完成Journey Optimizer B2B edition设置。

## &#x200B;1. 生成B2B命名空间和架构

<table>
<thead>
<tr>
<th colspan="2">任务</th>
<th>详细信息和说明</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>环境设置：</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>从GitHub下载命名空间和架构自动生成实用程序。</td>
<td><a href="./data/namespaces-schemas.md#set-up-the-auto-generation-utility">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>收集Experience Platform API凭据和所需的标头。</td>
<td><a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/landing/platform-apis/api-guide">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>将环境值应用于您的Postman环境。</td>
<td><a href="./data/namespaces-schemas.md#environment-values">了解详情</a></td>
</tr>
<tr>
<td colspan="2"><strong>运行脚本：</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>在Postman中运行<em>命名空间和架构</em>生成实用工具，并确认已创建命名空间和架构。</td>
<td><a href="./data/namespaces-schemas.md#run-the-scripts">了解详情</a></td>
</tr>
</tbody>
</table>

## &#x200B;2. 配置XDM字段和事件

<table>
<thead>
<tr>
<th colspan="2">任务</th>
<th>详细信息和说明</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>标准XDM类</strong>：设置XDM个人配置文件和XDM业务帐户类。</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>选择要为历程、购买群组和电子邮件个性化显示的托管字段。</td>
<td><a href="./admin/xdm-field-management.md#standard-classes">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>编辑架构的可更新字段。</td>
<td><a href="./admin/xdm-field-management.md#updatable-fields">了解详情</a></td>
</tr>
<tr>
<td colspan="2"><strong>关系架构</strong>：选择关系XDM类（帐户多对一自定义对象）。</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>确保架构具有所需的配置值。</td>
<td><a href="./admin/xdm-field-management.md#relational-schemas">了解详情</a></td>
</tr>
<tr>
<td colspan="2"><strong>事件</strong>：配置Experience Platform事件类型和字段。</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>使用要在历程决策/拆分路径中支持的字段配置每个Experience Platform事件类型。</td>
<td><a href="./admin/configure-aep-events.md">了解详情</a></td>
</tr>
</tbody>
</table>

## &#x200B;3. 配置跟踪和电子邮件可投放性

若要在简化的架构上从[!DNL Journey Optimizer B2B Edition]发送电子邮件，请在附加的[!DNL Marketo Engage]生产实例和[!DNL Journey Optimizer B2B Edition]应用程序中配置电子邮件跟踪和可投放性。

<table>
<thead>
<tr>
<th colspan="2">任务</th>
<th>详细信息和说明</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">所附加Marketo Engage实例的<strong>初始设置</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>为DNS记录中的跟踪链接配置新CNAME</td>
<td><a href="./start/email-protocols.md#create-dns-records-for-landing-pages-and-email">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>为连接的Marketo Engage实例配置品牌策略域</td>
<td><a href="./start/branding-domains.md">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>为连接的Marketo Engage实例配置DKIM和SPF</td>
<td><a href="./start/email-protocols.md#set-up-spf-and-dkim">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>设置 DMARC</td>
<td><a href="./start/email-protocols.md#set-up-dmarc">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>为您的域设置 MX 记录</td>
<td><a href="./start/email-protocols.md#set-up-mx-records-for-your-domain">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>将出站IP地址添加到允许列表</td>
<td><a href="./start/email-protocols.md#outbound-ip-addresses">了解详情</a></td>
</tr>
<tr>
<td colspan="2">所附的Marketo Engage实例的<strong>电子邮件设置</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>配置<em>From Email</em>和<em>From Label</em>（可选）</td>
<td><a href="./start/email-setup.md#from-email-and-label">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>配置<em>取消订阅HTML</em>和<em>取消订阅文本</em></td>
<td><a href="./start/email-setup.md#unsubscribe-messaging">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>配置<em>以网页HTML查看</em>和<em>以网页文本查看</em></td>
<td><a href="./start/email-setup.md#view-as-web-page">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>配置<em>自定义对象检索限制</em></td>
<td><a href="./start/email-setup.md#custom-object-retrieval-limits">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>配置<em>自定义标头选项</em></td>
<td><a href="./start/email-setup.md#custom-header-options">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>配置<em>机器人活动</em>筛选</td>
<td><a href="./start/email-setup.md#filter-email-bots">了解详情</a></td>
</tr>
<tr>
<td colspan="2">Journey Optimizer B2B edition的<strong>电子邮件渠道配置</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>在Journey Optimizer B2B edition中配置<em>通信限制</em></td>
<td><a href="./admin/configure-channels-emails.md#communication-limits">了解详情</a></td>
</tr>
</tbody>
</table>

<!-- TBD for later 

<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Email CC Settings</em></td>
<td>[Learn more](TBD)</td>
</tr>

<tr>
<td colspan="2"><strong>Additional configurations</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Location Settings</em> for the attached Marketo Engage instance</td>
<td>< [Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Define and configure which Binding Groups / IPs to move over</td>
<td>[Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Test Email Send</td>
<td>[Learn more](TBD)</td>
</tr>
-->

## &#x200B;4. 配置其他内容渠道

要支持营销人员在其历程中包含其他渠道，请配置其他渠道。

<table>
<thead>
<tr>
<th colspan="2">任务</th>
<th>详细信息和说明</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">Journey Optimizer B2B edition的<strong>短信</strong>渠道配置。</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>配置要支持的每个短信帐户。</td>
<td><a href="./admin/configure-channels-sms.md">了解详情</a></td>
</tr>
<tr>
<td colspan="2">Journey Optimizer B2B edition的<strong>登陆页面</strong> (Beta)渠道配置。</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>完成登陆页面设置以支持创作和发布这些页面的营销人员</td>
<td><a href="./admin/landing-page-settings.md">了解详情</a></td>
</tr>
<tr>
<td colspan="2">Journey Optimizer B2B edition的<strong>Web</strong> (Beta)渠道配置</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>配置您的商业网站以支持Adobe Experience Platform Web SDK。</td>
<td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>按传送内容的URL添加Web属性。</td>
<td><a href="./admin/configure-channels-web.md">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>指示Web体验作者安装Adobe Experience Cloud可视化编辑帮助程序浏览器扩展。</td>
<td><a href="./content/web-experiences.md#install-the-visual-editing-helper-extension">了解详情</a></td>
</tr>
</tbody>
</table>

## &#x200B;5. 连接Marketo Engage实例以支持历程操作（可选）

如果您计划通过Journey Optimizer B2B edition中的活动和项目来补充Marketo Engage的功能，请为Marketo Engage操作设置支持。 这些操作允许您的营销团队在Journey Optimizer B2B edition中协调其&#x200B;_基于帐户的_&#x200B;营销活动，在Marketo Engage中协调其&#x200B;_基于潜在客户的_&#x200B;营销活动。

<table>
<thead>
<tr>
<th colspan="2">任务</th>
<th>详细信息和说明</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>每个Marketo Engage实例</strong>支持历程操作</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>创建Marketo Engage自定义服务</td>
<td><a href="./admin/marketo-actions-connect.md#create-the-marketo-engage-custom-service">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>在Journey Optimizer B2B edition中添加集成</td>
<td><a href="./admin/marketo-actions-connect.md#add-the-integration">了解详情</a></td>
</tr>
</tbody>
</table>

## &#x200B;6. 启用用户访问权限

配置完成后，绑定沙盒并完成初始设置任务后，为团队和用户配置Journey Optimizer B2B edition和Marketo Engage访问权限。

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
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>在Adobe Admin Console中创建Marketo Engage产品配置文件（仅限新的Marketo Engage实例）</td>
<td><a href="./admin/user-management.md#marketo-engage-profile">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>为配置文件添加用户组</td>
<td><a href="./admin/user-management.md#add-user-group">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>配置B2B用户角色</td>
<td><a href="./admin/user-management.md#b2b-built-in-roles">了解详情</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="复选框"/></td>
<td>将用户或组添加到角色</td>
<td><a href="./admin/user-management.md#add-users-to-a-role">了解详情</a></td>
</tr>
</tbody>
</table>
