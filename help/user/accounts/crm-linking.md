---
title: 对详细信息页面的CRM内访问权限
description: 了解销售团队成员如何直接从他们的客户关系管理(CRM)工具(如Salesforce或Microsoft Dynamics)访问有关客户、联系人和潜在客户的详细页面。
feature: Integrations, Sales Insights
role: Admin, User
badgeBeta: label="Beta 版" type="informative" tooltip="此功能当前为有限测试版"
source-git-commit: d50e7eb067e40bdcc18c93baec1a0b6713bf793c
workflow-type: tm+mt
source-wordcount: '1438'
ht-degree: 0%

---

# 对详细信息页面的CRM内访问权限

Adobe Journey Optimizer B2B edition允许销售团队成员和客户经理直接从他们的客户关系管理(CRM)工具(如Salesforce或Microsoft Dynamics)访问有关帐户和购买群组信息的详细页面。 利用此集成，销售代表可以快速访问实时帐户和购买群组洞察，例如参与历史记录、意图信号和AI生成的推荐。 这一能力使销售团队能够更快地开展外联工作，更明智地确定优先顺序，更好地与营销部门保持一致。

要使销售团队成员能够从CRM中查看Journey Optimizer B2B edition中的[帐户详细信息](account-details.md)和[人员详细信息](person-details.md)页面，Salesforce或Dynamics管理员可以从帐户、联系人或潜在客户视图添加Journey Optimizer B2B edition链接。

当销售团队成员使用CRM实例中的链接时，沙盒应为&#x200B;_Prod_，并根据以下顺序逻辑确定IMS组织：

1. 用户访问的最新组织
1. 列表中的第一个按字母顺序排序
1. 在其偏好设置中选择的组织

## Salesforce链接

具有&#x200B;_自定义应用程序_&#x200B;权限的Salesforce管理员可以在“帐户”、“联系人”或“潜在客户”布局中配置链接。 通过配置的链接，销售用户能够访问Adobe Journey Optimizer B2B edition中相应的帐户详细信息或人员详细信息页面。

在Salesforce中，将自定义链接添加为按钮、超链接或链接图标，并根据您团队的偏好对其进行自定义。

Salesforce中的![自定义链接](./assets/crm-linking-sfdc-account-examples.png){width="800" zoomable="yes"}

有关在Salesforce中添加自定义链接的详细信息，请参阅Salesforce文档中的[定义自定义按钮和链接](https://help.salesforce.com/s/articleView?id=platform.defining_custom_links.htm&type=5)。

定义链接的目标URL时，您可以使用帐户、联系人或潜在客户布局，并将其链接到Journey Optimizer B2B edition中对应的详细信息页面：

* **帐户** - `https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/account/[18-character ID of account]`

* **联系人** - `https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/contact/[18-character ID of contact]`

* **潜在客户** - `https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/lead/[18-character ID of lead]`

使用`Account`对象获取帐户18个字符的ID，如`CASESAFEID(Account.Id)`或`CASESAFEID(Id)`。

**_示例:_**

+++字段链接

1. 在Salesforce中，转到&#x200B;**[!UICONTROL 设置]** > **[!UICONTROL 对象管理器]** > **[!UICONTROL 帐户]**/**[!UICONTROL 联系人]**/**[!UICONTROL 潜在客户]** > **[!UICONTROL 字段和关系]**。
1. 单击&#x200B;**[!UICONTROL 新建]**&#x200B;以创建公式（文本）字段，并将其添加到&#x200B;_帐户_、_联系人_&#x200B;或&#x200B;_潜在客户_&#x200B;布局。

   对于公式，使用以下示例作为指导。

   **_文本超链接:_**

   * 帐户 — `HYPERLINK("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/account/" & CASESAFEID(Id), "View in AJO B2B")`
   * 联系人 — `HYPERLINK("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/contact/" & CASESAFEID(Id), "View in AJO B2B")`
   * 潜在客户 — `HYPERLINK("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/lead/" & CASESAFEID(Id), "View in AJO B2B")`

   **_图标超链接:_**

   * 帐户 — `HYPERLINK("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/account/" & CASESAFEID(Id), IMAGE("https://cdn.experience.adobe.net/assets/HeroIcons.6620f5dc.svg#AdobeExperienceSubCloud", "View in AJO B2B", 24, 24))`
   * 联系人 — `HYPERLINK("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/contact/" & CASESAFEID(Id), IMAGE("https://cdn.experience.adobe.net/assets/HeroIcons.6620f5dc.svg#AdobeExperienceSubCloud", "View in AJO B2B", 24, 24))`
   * 联系人 — `HYPERLINK("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/lead/" & CASESAFEID(Id), IMAGE("https://cdn.experience.adobe.net/assets/HeroIcons.6620f5dc.svg#AdobeExperienceSubCloud", "View in AJO B2B", 24, 24))`

   Salesforce中的![字段链接配置](./assets/crm-linking-sfdc-field-link-config.png){width="800" zoomable="yes"}

1. 刷新页面以显示布局更改。 转到&#x200B;**[!UICONTROL 配置文件]**，然后在&#x200B;**[!UICONTROL 显示密度]**&#x200B;下选择其他选项。

   ![在Salesforce中刷新页面](./assets/crm-linking-sfdc-field-link-refresh.png){width="450" zoomable="yes"}

+++

+++详细信息页面链接

1. 在Salesforce中，转到&#x200B;**[!UICONTROL 设置]** > **[!UICONTROL 对象管理器]** > **[!UICONTROL 帐户]**/**[!UICONTROL 联系人]**/**[!UICONTROL 潜在客户]** > **[!UICONTROL 按钮、链接和操作]**。
1. 单击右上角的&#x200B;**[!UICONTROL 新建按钮或链接]**，然后创建详细信息页面链接。

   对于公式，使用以下示例作为指导。

   * 帐户 — `{!URLFOR("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/account/" & CASESAFEID(Account.Id), null)}`
   * 联系人 — `{!URLFOR("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/contact/" & CASESAFEID(Contact.Id), null)}`
   * 潜在客户 — `{!URLFOR("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/lead/" & CASESAFEID(Lead.Id), null)}`

   在Salesforce中![详细页面链接配置](./assets/crm-linking-sfdc-detail-page-link-config.png){width="800" zoomable="yes"}

1. 在左侧导航中转到&#x200B;**[!UICONTROL 页面布局]**。

1. 将链接从&#x200B;**[!UICONTROL 自定义链接]**&#x200B;拖放到布局中的&#x200B;_自定义链接_&#x200B;部分。

+++

+++详细信息页面按钮

1. 在Salesforce中，转到&#x200B;**[!UICONTROL 设置]** > **[!UICONTROL 对象管理器]** > **[!UICONTROL 帐户]**/**[!UICONTROL 联系人]**/**[!UICONTROL 潜在客户]** > **[!UICONTROL 按钮、链接和操作]**。
1. 单击右上角的&#x200B;**[!UICONTROL 新建按钮或链接]**&#x200B;并创建详细信息页面按钮。

   对于&#x200B;**[!UICONTROL 显示类型]**，请选择&#x200B;**[!UICONTROL 详细信息页面链接]**。

   对于公式，使用以下示例作为指导。

   * 帐户 — `{!URLFOR("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/account/" & CASESAFEID(Account.Id), null)}`
   * 联系人 — `{!URLFOR("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/contact/" & CASESAFEID(Contact.Id), null)}`
   * 潜在客户 — `{!URLFOR("https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/lead/" & CASESAFEID(Lead.Id), null)}`

   Salesforce中的![详细信息页面按钮配置](./assets/crm-linking-sfdc-detail-page-button-config.png){width="800" zoomable="yes"}

1. 在左侧导航中转到&#x200B;**[!UICONTROL 页面布局]**。

1. 从&#x200B;**[!UICONTROL 移动和闪电动作]**&#x200B;中拖动该按钮，并将其放入布局中的&#x200B;**[!UICONTROL Salesforce移动和闪电体验动作]**&#x200B;部分。

   ![将按钮添加到布局](./assets/crm-linking-sfdc-detail-page-button-layout.png){width="800" zoomable="yes"}

+++

## Microsoft Dynamics链接

Dynamics开发人员可以扩展Account、Contact或Lead实体以添加链接字段。 通过配置的链接，销售用户能够访问Adobe Journey Optimizer B2B edition中相应的帐户详细信息或人员详细信息页面。

将自定义链接添加为按钮、超链接或链接图标链接，并根据您团队的偏好对其进行自定义。

Dynamics中的![自定义链接](./assets/crm-linking-dynamics-account-examples.png){width="800" zoomable="yes"}

使用Power Apps自定义Microsoft模型驱动应用程序，例如Dynamics组件。 有关使用Power Apps在Dynamics中添加自定义链接的详细信息，请参阅[PowerApps文档](https://learn.microsoft.com/en-us/power-apps/maker/model-driven-apps/create-edit-web-resources)。

定义链接的目标URL时，您可以使用帐户、联系人或潜在客户视图，并将其链接到Journey Optimizer B2B edition中相应的详细信息页面：

* **帐户** - `https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/account/[Account ID]`

* **联系人** - `https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/contact/[Contact ID]`

* **潜在客户** - `https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm/lead/[Lead ID]`

**_示例:_**

+++URL字段

按照以下任务序列将自定义链接添加为URL字段：

**1 — 配置解决方案字段**

1. 转到&#x200B;**[!UICONTROL 高级设置]** > **[!UICONTROL 自定义系统]**&#x200B;并选择&#x200B;**[!UICONTROL 解决方案]**&#x200B;选项卡。
1. 选择&#x200B;**[!UICONTROL 实体]** > **[!UICONTROL 帐户]**/**[!UICONTROL 联系人]**/**[!UICONTROL 潜在客户]** > **[!UICONTROL 字段]**。
1. 单击&#x200B;**[!UICONTROL 新建]**&#x200B;并配置新字段。

   ![联系人实体的新字段](./assets/crm-linking-dynamics-url-field-new.png){width="800" zoomable="yes"}

1. 保存字段配置。
1. 从&#x200B;_[!UICONTROL 解决方案]_&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Web资源]**。
1. 单击&#x200B;**[!UICONTROL 新建]**&#x200B;并配置以下脚本(JScript) Web资源：

   ```js
   function setViewInAjoB2b(executionContext) {
    var url = "https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm";
   
    var formContext = executionContext.getFormContext();
   
    // Get the entity ID (GUID)
    var id = formContext.data.entity.getId();
   
    // Get the entity type (account, lead, contact)
    var type = formContext.data.entity.getEntityName().toLowerCase();
   
    if (id && type) {
        // Remove curly braces
        id = id.replace(/[{}]/g, "").toLowerCase();
   
        // Set the value in the custom field (Ensure this field exists on the form)
        formContext.getAttribute("new_viewinajob2b").setValue(url + "/" + type + "/" + id);
       }
   }
   ```

   ![添加jScript Web资源](./assets/crm-linking-dynamics-url-field-jscript.png){width="800" zoomable="yes"}

1. 在页面顶部，单击&#x200B;**[!UICONTROL 保存]**，然后单击&#x200B;**[!UICONTROL 发布]**。

**2 — 配置表单**

1. 在&#x200B;_解决方案_&#x200B;选项卡上，选择&#x200B;**[!UICONTROL 实体]** > **[!UICONTROL 帐户]**/**[!UICONTROL 联系人]**/**[!UICONTROL 潜在客户]** > **[!UICONTROL Forms]** > **[!UICONTROL 帐户]**/**[!UICONTROL 联系人]**/**[!UICONTROL 潜在客户]**。
1. 将您在第一个任务中创建的新字段从&#x200B;**[!UICONTROL 字段资源管理器]**&#x200B;拖入&#x200B;**[!UICONTROL 摘要]**&#x200B;部分。

   ![将URL链接字段添加到“摘要”部分](./assets/crm-linking-dynamics-url-field-forms.png){width="800" zoomable="yes"}

1. 双击&#x200B;_摘要_&#x200B;部分中的字段并配置其属性。

   ![设置字段属性](./assets/crm-linking-dynamics-url-field-properties.png){width="800" zoomable="yes"}

   属性配置完成后，单击&#x200B;**[!UICONTROL 确定]**。

1. 在页面顶部的功能区中，单击&#x200B;**[!UICONTROL 保存]**，然后单击&#x200B;**[!UICONTROL 发布]**。

**3 — 将JS Web资源添加到表单库**

1. 在顶部的&#x200B;_[!UICONTROL 主页]_&#x200B;选项卡上，单击&#x200B;**[!UICONTROL 表单属性]**。
1. 单击&#x200B;**[!UICONTROL 添加]**。

   ![添加表单属性](./assets/crm-linking-dynamics-url-form-properties.png){width="500" zoomable="yes"}

1. 找到该资源，将其选中，然后单击&#x200B;**[!UICONTROL 添加]**。

   ![添加Web资源](./assets/crm-linking-dynamics-url-form-field-libraries.png){width="500" zoomable="yes"}

1. 选择添加的资源后，单击&#x200B;**[!UICONTROL 事件处理程序]**&#x200B;下的&#x200B;_[!UICONTROL 添加]_。
1. 将`setViewInAjoB2b`函数添加到&#x200B;**[!UICONTROL 事件处理程序]**。
1. 在&#x200B;_[!UICONTROL 事件处理程序]_&#x200B;列表中选择函数后，将&#x200B;**[!UICONTROL Control]**&#x200B;设置为`Form`，将&#x200B;**[!UICONTROL Event]**&#x200B;设置为`OnLoad`。

   ![添加处理程序](./assets/crm-linking-dynamics-url-handler-properties.png){width="500" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 确定]**。

1. 在顶部的&#x200B;_[!UICONTROL 主页]_&#x200B;选项卡上，单击&#x200B;**[!UICONTROL 保存]**，然后单击&#x200B;**[!UICONTROL 发布]**。

**4 — 验证链接**

要验证链接，请检查Dynamics中的“帐户”、“联系人”或“潜在客户”视图。

![添加表单属性](./assets/crm-linking-dynamics-url-field-displayed.png){width="500" zoomable="yes"}

如果未显示链接，请尝试转到Dynamics主页上&#x200B;**[!UICONTROL 客户]**&#x200B;下的“帐户”、“联系人”或“潜在客户”。 然后返回特定的帐户、联系人或潜在客户视图。 您也可以尝试注销并重新登录。

+++

+++HTML Web资源

按照以下任务序列将自定义链接添加为HTML Web资源：

>[!NOTE]
>
>此示例取决于Dynamics如何使用网页Web资源。

**1 — 配置解决方案Web资源**

1. 转到&#x200B;**[!UICONTROL 高级设置]** > **[!UICONTROL 自定义系统]**&#x200B;并选择&#x200B;**[!UICONTROL 解决方案]**&#x200B;选项卡。

1. 在&#x200B;_[!UICONTROL 解决方案]_&#x200B;选项卡上，选择&#x200B;**[!UICONTROL Web资源]**。

1. 单击&#x200B;**[!UICONTROL 新建]**&#x200B;并使用以下函数配置以下脚本(JScript) Web资源：

   ```js
   function getFormContext(executionContext) {
       window.top["formContext"] = executionContext.getFormContext();
   }
   ```

   ![添加Web资源函数](./assets/crm-linking-dynamics-web-resources-getFormContext.png){width="800" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 新建]**&#x200B;以创建其他Web资源，并使用以下HTML配置网页(HTML) Web资源：

   ```html
   <html>
   <head>
       <script>
       function onLoad(){
           // Adobe URL
           var url = "https://experience.adobe.com/#/journey-optimizer-b2b/accounts/crm";
   
           // Get the entity ID (GUID)
           var id = window.top.formContext.data.entity.getId();
   
           // Get the entity type (account, lead, contact)
           var type = window.top.formContext.data.entity.getEntityName().toLowerCase();
   
           if (id && type) {
               // Remove curly braces
               id = id.replace(/[{}]/g, "").toLowerCase();
               var url = url + "/" + type + "/" + id;
   
               // Find the hyperlink and set the href value
               var link = document.getElementById("link");
               link.href = url;
           }
       }
       </script>
   </head>
   <body onload="onLoad()" style="margin-left: 0;">
       <a id="link" style="text-decoration: none; font-family: sans-serif; font-size: 13px;" target="_blank">
           <img style="vertical-align: middle;" src="https://experience.adobe.net/assets/HeroIcons.6620f5dc.svg#AdobeExperienceSubCloud" focusable="false" width="24" height="24">
           <span style="vertical-align: middle;">View in AJOB2B</span>
       </a>
   </body>
   </html>
   ```

1. 在页面顶部，单击&#x200B;**[!UICONTROL 保存]**，然后单击&#x200B;**[!UICONTROL 发布]**。

**2 — 将JS Web资源添加到表单库**

1. 在&#x200B;_解决方案_&#x200B;选项卡上，选择&#x200B;**[!UICONTROL 实体]** > **[!UICONTROL 帐户]**/**[!UICONTROL 联系人]**/**[!UICONTROL 潜在客户]** > **[!UICONTROL Forms]** > **[!UICONTROL 帐户]**/**[!UICONTROL 联系人]**/**[!UICONTROL 潜在客户]**。

1. 在顶部的&#x200B;_主页_&#x200B;选项卡上，单击&#x200B;**[!UICONTROL 表单属性]**。

1. 单击&#x200B;**[!UICONTROL 添加]**。

1. 找到您创建的JScript Web资源(`new_getFormContext`)，选择它，然后单击&#x200B;**[!UICONTROL 添加]**。

   ![添加Web资源](./assets/crm-linking-dynamics-web-resources-add-form-property.png){width="500" zoomable="yes"}

1. 选择添加的资源后，单击&#x200B;**[!UICONTROL 事件处理程序]**&#x200B;下的&#x200B;_[!UICONTROL 添加]_。
1. 将`getFormContext`函数添加到&#x200B;**[!UICONTROL 事件处理程序]**。
1. 在&#x200B;_[!UICONTROL 事件处理程序]_&#x200B;列表中选择函数后，将&#x200B;**[!UICONTROL Control]**&#x200B;设置为`Form`，将&#x200B;**[!UICONTROL Event]**&#x200B;设置为`OnLoad`。

   ![添加处理程序](./assets/crm-linking-dynamics-web-resources-handler-properties.png){width="500" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 确定]**。

1. 在顶部的&#x200B;_[!UICONTROL 主页]_&#x200B;选项卡上，单击&#x200B;**[!UICONTROL 保存]**，然后单击&#x200B;**[!UICONTROL 发布]**。

**3 — 配置表单**

1. 在帐户、联系人或潜在客户表单的&#x200B;**[!UICONTROL 主页]**&#x200B;选项卡上，选择&#x200B;**[!UICONTROL 正文]**（在&#x200B;_摘要_&#x200B;分区中创建链接资源）或&#x200B;**[!UICONTROL 标题]**（在标题菜单中创建）。

   ![选择表单区域](./assets/crm-linking-dynamics-web-resource-form-select.png){width="500" zoomable="yes"}

1. 选择顶部的&#x200B;**[!UICONTROL 插入]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL Web资源]**。

1. 插入您创建的Web资源并配置属性。

   ![Web资源](./assets//crm-linking-dynamics-web-resource-form-properties.png){width="500" zoomable="yes"}

   有关Web资源属性和格式化的详细信息，请参阅[Power Apps文档](https://learn.microsoft.com/en-us/power-apps/maker/model-driven-apps/web-resource-properties-legacy)。

1. 单击&#x200B;**[!UICONTROL 确定]**。

   如果为Web资源选择了“正文/摘要”位置，则它将显示在表单布局中。

   ![Web资源已添加到表单](./assets/crm-linking-dynamics-web-resource-layout-displayed.png){width="800" zoomable="yes"}的摘要部分

1. 在顶部的&#x200B;_[!UICONTROL 主页]_&#x200B;选项卡上，单击&#x200B;**[!UICONTROL 保存]**，然后单击&#x200B;**[!UICONTROL 发布]**。

**4 — 验证链接**

要验证链接，请检查Dynamics中的“帐户”、“联系人”或“潜在客户”视图。

![添加表单属性](./assets/crm-linking-dynamics-web-resource-displayed.png){width="500" zoomable="yes"}

如果未显示链接，请尝试转到Dynamics主页上&#x200B;**[!UICONTROL 客户]**&#x200B;下的“帐户”、“联系人”或“潜在客户”。 然后返回特定的帐户、联系人或潜在客户视图。 您也可以尝试注销并重新登录。

+++
