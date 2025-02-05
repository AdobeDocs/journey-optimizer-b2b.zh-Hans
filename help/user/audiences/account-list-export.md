---
title: 导出帐户列表
description: 了解如何根据购买组筛选器导出帐户列表。
source-git-commit: c51ee8c8b58e8154c81f6a2ffada3f58a08eb6b4
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# 导出帐户列表

使用&#x200B;_导出帐户列表_&#x200B;功能，根据您定义的筛选条件导出所有帐户或一组帐户。 导出过程会生成一个CSV文件，并在脉冲通知中发送所存储文件的URL。 如果需要，您可以使用此功能将帐户移至第三方平台。

1. 在Journey Optimizer B2B edition的左侧导航栏中，转到&#x200B;**[!UICONTROL 帐户]** > **[!UICONTROL 购买群组]**。

1. 选择&#x200B;**[!UICONTROL 浏览]**&#x200B;选项卡。

1. 单击右上方的&#x200B;**[!UICONTROL 导出帐户]**。

   ![编辑帐户详细信息](./assets/export-accounts.png){width="800" zoomable="yes"}

1. 在对话框中，定义要导出的帐户受众的参数。

   ![指定帐户受众筛选](./assets/export-accounts-dialog.png){width="400"}

   对于&#x200B;**[!UICONTROL 参与度分数]**，运算符`Between`是包含的，百分比范围也是。 例如，5.1和5都是介于&#x200B;_5和6之间的_。

   空筛选参数的处理方式与`Is Any`相同。

1. 单击&#x200B;**[!UICONTROL 导出帐户]**&#x200B;以使用指定的筛选器生成CSV文件。

1. 当您收到导出完成的通知时，请单击通知链接以访问CSV文件。

   ![单击通知以下载导出的帐户列表CSV文件](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >如果您在Adobe用户帐户首选项中设置了电子邮件通知的通知订阅，则可能是电子邮件通知。

   应用程序页面将重定向到&#x200B;_购买组_&#x200B;浏览选项卡，系统保存文件对话框将提示您将文件保存到系统中。 如果需要共享数据，您可以使用团队的文件共享系统。
