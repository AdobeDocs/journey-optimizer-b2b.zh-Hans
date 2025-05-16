---
title: 配置Experience Manager资源存储库
description: 了解如何配置与Experience Manager Assets存储库的连接，以用于Journey Optimizer B2B edition内容创作。
feature: Assets, Integrations
role: Admin
exl-id: 4cdfc8bc-823f-4320-a2c3-08226f26eec2
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# 配置Experience Manager资源存储库

Adobe Journey Optimizer B2B edition与Adobe Experience Manager Assets as a Cloud Service集成，从而不仅允许在帐户历程中使用电子邮件等资产。 它通过与Experience Manager Assets交换信息确保透明度。 配置与Adobe Experience Assets的连接以启用此功能。

Adobe Experience Manager Cloud Manager分为多个项目，每个项目都有多个环境和存储库（[了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/programs/program-types){target="_blank"}）。 在Adobe Journey Optimizer B2B edition中配置Adobe Experience Manager Assets时，您需要设置与要用于访问数字资源的每个存储库的连接。

{{aem-assets-licensing-note}}

## 先决条件

* 在AEM Headless Developer Console上为所需的环境生成服务凭据（[了解更多](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials#generate-service-credentials){target="_blank"}）。
* 获取连接所需的证书。 作为最佳实践，请确保证书在过期前至少还有六个月。 证书每365天过期一次。
* Adobe Journey Optimizer B2B edition支持一次访问一个数字资产管理源。 切换之前，请确保所需的资源在Adobe Experience Manager中可用。

>[!IMPORTANT]
>
>服务凭据是真实的，并包含私钥。 必须根据贵组织的IT和安全策略存储、管理和访问这些凭据。

## 添加存储库连接

1. 在左侧导航中，选择&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 配置]**。

1. 单击中间面板上的&#x200B;**[!UICONTROL Assets]**。

   ![访问Assets配置空间](./assets/configuration-assets-aem.png){width="700" zoomable="yes"}

<!--   The default digital asset management option is configured as `Adobe Marketo Engage`.
-->
在这里，您可以逐一配置与每个AEM环境存储库的连接。

1. 在&#x200B;_[!UICONTROL Adobe Experience Manager Assets]_&#x200B;框中，单击&#x200B;**[!UICONTROL 配置存储库]**&#x200B;旁边的箭头并选择存储库。

   ![选择AEM Assets存储库](./assets/configure-assets-aem-choose-respository.png){width="500"}

1. 单击&#x200B;**[!UICONTROL 添加证书]**&#x200B;并使用对话框工具上载文件。

   您可以上传.json文件，方法是将其拖动到对话框上或单击链接以查找并从系统中选择文件（确保该文件是有效的JSON类型）。

   ![上载证书JSON文件](./assets/configuration-assets-aem-upload-cert.png){width="500"}

   上传后，证书将显示在底部。

   >[!NOTE]
   >
   >如果使用无效文件，对话框底部会显示错误。

   单击&#x200B;**[!UICONTROL 添加]**&#x200B;以完成证书。

1. 单击“上一步(←)”箭头返回主配置页。

   配置的存储库将显示在选择面板下的表格中。 您可以通过重复步骤3-4来添加另一个存储库。

   ![查看配置的AEM资源存储库](./assets/configuration-assets-aem-repositories.png){width="600" zoomable="yes"}

配置完存储库后，团队成员可以在创作内容时选择Adobe Experience Manager Assets 。

>[!NOTE]
>
>Adobe Journey Optimizer B2B edition支持在创作内容时一次访问一个数字资产管理源。 

## 替换证书

证书自创建日期起每365天过期。 在过期之前替换它，以确保您的团队可以继续访问资产。

>[!NOTE]
>
>Adobe Journey Optimizer B2B edition与Experience Manager资源通信以了解使用信息。 连接必须保持活动状态才能可靠的使用数据同步并防止数据差异。 管理员用户会通过应用程序内通知收到有关证书过期的通知。 他们还可以在“管理”区域的“Assets”子部分“数字资源管理”中注意过期日期。

1. 在数字资产管理页面上，找到已配置存储库的列表。

1. 单击所需的存储库以替换证书。

1. 单击证书文件的省略号(**...**)图标，显示对其执行操作的选项。

   ![访问AEM资源存储库证书的选项菜单](./assets/configuration-assets-aem-repo-menu.png){width="600" zoomable="yes"}

1. 选择&#x200B;**[!UICONTROL 替换]**&#x200B;打开文件上载对话框。

1. 通过将文件拖到对话框上或使用链接上传文件。 确保文件为json类型。

   ![上载替代的AEM资源存储库证书JSON文件](./assets/configuration-assets-aem-upload-replacement-cert.png){width="500"}

1. 单击&#x200B;**[!UICONTROL 替换]**&#x200B;以确认上载。

## 查看证书

您可以查看与存储库连接关联的证书JSON文件。

1. 在数字资产管理页面上，找到已配置存储库的列表。

1. 单击连接的存储库。

1. 单击证书文件的省略号(**...**)图标，显示对其执行操作的选项。

1. 选择&#x200B;**[!UICONTROL 视图]**。

   ![查看连接的AEM资源存储库的证书JSON文件](./assets/configuration-assets-aem-view-cert.png){width="600"}

1. 单击&#x200B;**[!UICONTROL 关闭]**&#x200B;以返回到“配置存储库”页面。

## 删除存储库连接

删除存储库会移除用户对Journey Optimizer B2B edition中Experience Manager Assets环境的访问权限。

1. 在&#x200B;_[!UICONTROL 数字资源管理]_&#x200B;页面上，找到已配置的资源存储库列表。

1. 单击所需的存储库名称以编辑连接。

1. 单击证书文件的省略号(**...**)图标，显示对其执行操作的选项。

1. 选择&#x200B;**[!UICONTROL 删除]**。

1. 在确认对话框中点击&#x200B;**[!UICONTROL 删除]**。
<!--

## Switch back to Adobe Marketo Engage Assets

Select Adobe Marketo Engage digital asset management in the Assets section.

After the confirmation, the Adobe Marketo Engage assets library is available for users.
-->
