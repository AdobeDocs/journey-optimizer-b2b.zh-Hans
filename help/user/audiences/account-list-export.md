---
title: 导出帐户
description: 在Journey Optimizer B2B edition中将筛选后的帐户列表导出到CSV，以供具有购买组和参与度得分过滤器的第三方平台使用。
feature: Audiences
role: User
exl-id: 3ec8e8fd-1bc2-4efa-840f-f06520099060
source-git-commit: ae1885dbe724dcc751a72325d90641decd355a4c
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 91%

---

# 导出帐户

使用&#x200B;_导出帐户_&#x200B;功能可以根据您定义的筛选方式导出所有帐户或一组帐户。导出过程会生成一个 CSV 文件，并在脉冲通知中发送已保存文件的 URL。您可以在需要时使用此功能将帐户转移到第三方平台。

1. 在 Journey Optimizer B2B Edition 中，前往左侧导航栏中的&#x200B;**[!UICONTROL 帐户]** > **[!UICONTROL 购买群组]**。

1. 选择&#x200B;**[!UICONTROL 浏览]**&#x200B;选项卡。

1. 单击右上角的&#x200B;**[!UICONTROL 导出帐户]**。

   ![编辑帐户详细信息](./assets/export-accounts.png){width="800" zoomable="yes"}

1. 在对话框中，定义要导出的帐户受众的参数。

   ![指定帐户受众筛选方式](./assets/export-accounts-dialog.png){width="400"}

   对于&#x200B;**[!UICONTROL 参与度评分]**，运算符 `Between` 和百分比范围都已包含。例如，5.1 和 5 均在 5 和 6 _之间_。

   空的筛选参数被视为 `Is Any`。

1. 单击&#x200B;**[!UICONTROL 导出帐户]**，使用指定的过滤器生成 CSV 文件。

1. 当您收到导出完成的通知时，单击通知链接即可访问 CSV 文件。

   ![单击通知即可下载已导出的帐户列表 CSV 文件](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >如果您在 Adobe 用户帐户偏好设置中设置了电子邮件通知订阅，则可能发送电子邮件通知。

   应用程序页面会重定向到&#x200B;_购买群组_&#x200B;浏览选项卡，系统保存文件对话框会提示您将文件保存到系统。如果您需要共享数据，可以使用团队的文件共享系统。
