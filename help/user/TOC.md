---
user-guide-title: Journey Optimizer B2B Edition 文档
user-guide-description: 了解 Adobe Journey Optimizer B2B Edition 以及如何使用它通过内置的生成式 AI 和行业领先的自动化来编排帐户及购买群组历程。
source-git-commit: ef3c33a769bf8f794bbc1a61f77feabc9db961e7
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 80%

---


# Journey Optimizer B2B Edition 用户指南 {#user}

+ [Adobe Journey Optimizer B2B Edition 文档](guide-overview.md)
+ [发行说明](./release-notes/release-notes.md)
+ 快速入门 {#get-started}
   + [Journey Optimizer B2B Edition 概述](about-journey-optimizer-b2b-edition.md)
   + [登录和主页](home-page.md)
   + [入门指南](./start/get-started.md)
   + [跟踪和电子邮件协议](./start/email-protocols.md)
+ AI 助手 {#ai-assistant}
   + [概述](./ai-assistant/ai-assistant-overview.md)
   + [启用 AI 助手访问](./ai-assistant/enable-ai-assistant-access.md)
   + [问题指导](./ai-assistant/question-guidance.md)
   + [使用 AI 助手](./ai-assistant/use-ai-assistant.md)
   + 代理 {#ai-agents}
      + [Audience 代理](./agents/audience-agent-b2b.md)
      + [历程生成代理B2B](./agents/journey-agent.md)
      + [销售限定词](./agents/sales-qualifier.md)
+ 帐户历程 {#account-journeys}
   + [概述](./journeys/journey-overview.md)
   + [创建和发布历程](./journeys/create-publish-journey.md)
   + [历程节点](./journeys/journey-nodes.md)
   + 历程节点 {#journey-nodes}
      + [帐户受众](./journeys/account-audience-nodes.md)
      + [执行操作](./journeys/action-nodes.md)
      + [侦听事件](./journeys/listen-for-event-nodes.md)
      + [拆分和合并路径](./journeys/split-merge-paths-nodes.md)
      + [等待](./journeys/wait-nodes.md)
   + [历程详细信息](./journeys/journey-details.md)
+ 历程内容 {#journey-content}
   + [短信渠道](./content/sms-authoring.md)
   + 电子邮件渠道 {#email-channel}
      + [添加电子邮件](./content/add-email.md)
      + [电子邮件创作](./content/email-authoring.md)
      + [电子邮件创作的 AI 助手](./content/ai-assistant-emails.md)
      + [GenStudio 工作流](./content/genstudio-email-workflow.md)
      + [用于电子邮件设计的深色模式](./content/email-dark-mode.md)
      + [受监管的模板](./content/email-authoring-governance.md)
      + [销售警报电子邮件](./content/sales-alert-email.md)
      + [电子邮件重复数据删除](./content/email-deduplication.md)
   + Web渠道(Beta) {#web-channel}
      + [概述](./content/web-experiences.md)
      + [Web体验设计](./content/web-experience-design.md)
      + [单页应用程序](./content/web-single-page-applications.md)
   + [自定义个性化令牌](./content/personalization-my-tokens.md)
+ Audiences {#audiences}
   + [Experience Platform受众](./audiences/account-audience-overview.md)
   + [定位外部受众](./audiences/target-external-audience.md)
   + [LinkedIn帐户匹配的受众](./data/linkedin-account-matched-audiences.md)
+ 帐户 {#accounts}
   + 购买群组 {#buying-groups}
      + [概述](./buying-groups/buying-groups-overview.md)
      + [解决方案兴趣](./buying-groups/solution-interests.md)
      + [角色模板](./buying-groups/buying-groups-role-templates.md)
      + [默认和自定义角色](./buying-groups/default-custom-roles.md)
      + [角色洞察](./buying-groups/buying-group-role-insights.md)
      + 购买群组评分 {#scoring}
         + [参与度评分](./buying-groups/engagement-scores.md)
         + [完整性评分](./buying-groups/completeness-scores.md)
      + [购买群组阶段](./buying-groups/buying-group-stages.md)
      + [创建购买群组](./buying-groups/buying-groups-create.md)
      + [导出帐户](./audiences/account-list-export.md)
      + [Marketo Engage 中的购买群组过滤器](./buying-groups/marketo-engage-smart-list-buying-group-filters.md)
      + [In-CRM Insights](./buying-groups/incrm-insights.md)
   + 帐户列表 {#account-lists}
      + [概述](./accounts/account-lists.md)
      + [用于历程和计划](./accounts/account-lists-journeys.md)
   + 销售体验 {#sales-experience}
      + [帐户详细信息](./accounts/account-details.md)
      + [购买群组详细信息](./buying-groups/buying-group-details.md)
      + [个人详细信息](./accounts/person-details.md)
      + [CRM 链接](./accounts/crm-linking.md)
+ 内容管理 {#content-management}
   + 电子邮件 {#emails}
      + [处理电子邮件内容](./content/emails-list.md)
      + [设计可访问的内容](./content/email-accessible-content.md)
      + 预览和验证 {#preview}
         + [模拟内容](./content/email-simulate-content.md)
         + [测试电子邮件渲染](./content/email-test-rendering.md)
         + [垃圾邮件报告](./content/email-spam-report.md)
      + [电子邮件协作](./content/email-collaboration-tools.md)
   + 资产 {#assets}
      + [概述](./content/assets-overview.md)
      + 内部资产 {#internal-dam}
         + [使用内部资产](./content/internal-image-assets.md)
         + [使用 Adobe Express 编辑图像](./content/image-edit-adobe-express.md)
      + [Experience Manager 图像资产](./content/aem-assets.md)
   + 模板 {#templates}
      + [内容监管](./content/template-content-governance.md)
      + 电子邮件模板 {#email-templates}
         + [概述](./content/email-templates.md)
         + [电子邮件模板创作](./content/email-template-authoring.md)
         + [将图像转换为模板](./content/email-template-image-convert.md)
      + 登陆页面模板 (Beta) {#landing-page-templates}
         + [概述](./content/landing-page-templates.md)
         + [登陆页面模板设计](./content/landing-page-template-design.md)
   + 片段 {#visual-fragments}
      + [概述](./content/fragments.md)
      + [片段创作](./content/fragment-authoring.md)
   + Forms（Beta 版） {#forms}
      + [概述](./content/forms.md)
      + [表单设计](./content/form-design.md)
   + 登陆页面（Beta 版） {#landing-pages}
      + [概述](./content/landing-pages.md)
      + [登陆页面设计](./content/landing-page-design.md)
   + 内容设计工具 {#content-design}
      + [结构组件](./content/structure-components.md)
      + [内容组件](./content/content-components.md)
      + [自定义 CSS](./content/design-custom-css.md)
   + 品牌（Beta 版） {#brands}
      + [概述](./content/brands-overview.md)
      + [管理和创建](./content/brands-manage-create.md)
      + [品牌一致性](./content/brand-alignment.md)
   + [品牌主题](./content/brand-themes.md)
   + [条件内容](./content/conditional-content.md)
   + 个性化 {#personalization}
      + [概述](./content/personalization.md)
      + [个性化语法](./content/personalization-syntax.md)
      + [辅助函数列表](./content/personalization-helper-functions.md)
+ 智能仪表板 {#dashboards}
   + [分析仪表板](./dashboards/intelligent-dashboard.md)
   + [参与仪表板](./dashboards/engagement-dashboard.md)
   + [Web参与仪表板](./dashboards/web-engagement-dashboard.md)
   + [购买组仪表板](./dashboards/buying-groups-dashboard.md)
   + [帐户历程仪表板](./dashboards/journeys-dashboard.md)
+ 管理 {#admin}
   + [治理](./admin/governance.md)
   + [Marketo操作配置](./admin/marketo-actions-connect.md)
   + [用户画像映射](./admin/persona-mapping.md)
   + [用户管理](./admin/user-management.md)
   + XDM字段管理 {#xdm-field-management}
      + [XDM类](admin/xdm-field-management.md)
      + [体验事件和字段](./admin/configure-aep-events.md)
      + [默认XDM字段](./admin/field-mapping.md)
   + 渠道 {#channels}
      + [电子邮件配置](./admin/configure-channels-emails.md)
      + [短信配置](./admin/configure-channels-sms.md)
      + [Web渠道配置(Beta)](./admin/configure-channels-web.md)
      + [登陆页面设置(Beta)](./admin/landing-page-settings.md)
      + [配置数据流以进行事件收集](./data/aep-event-collection.md)
   + 配置 {#configurations}
      + [AEM Assets 存储库](./admin/configure-aem-repositories.md)
      + [意图数据](./admin/intent-data.md)
      + [参与度评分权重](./admin/engagement-score-weighting.md)
   + [简化的架构设置](simplified-architecture.md)
