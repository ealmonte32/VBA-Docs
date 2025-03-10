---
title: MsoSyncEventType enumeration (Office)
ms.prod: office
api_name:
- Office.MsoSyncEventType
ms.assetid: d9f4d2fa-9574-7ac1-c703-82897ff99c37
ms.date: 01/31/2019
ms.localizationpriority: medium
---


# MsoSyncEventType enumeration (Office)

Specifies the return value of a **Sync** event. In Microsoft Word, used with the **Sync** event of the **Document** object or the **DocumentSync** event of the **Application** object. In Microsoft Excel, used with the **Sync** event of the **Workbook** object or the **WorkbookSync** event of the **Application** object. In Microsoft PowerPoint, used with the **PresentationSync** event of the **Application** object.

> [!NOTE] 
> Beginning with Microsoft Office 2010, this object or member has been deprecated and should not be used.

|Name|Value|Description|
|:-----|:-----|:-----|
|**msoSyncEventDownloadFailed**|2|Download failed.|
|**msoSyncEventDownloadInitiated**|0|Download initiated.|
|**msoSyncEventDownloadNoChange**|6|No change detected.|
|**msoSyncEventDownloadSucceeded**|1|Download succeeded.|
|**msoSyncEventOffline**|7|Offline.|
|**msoSyncEventUploadFailed**|5|Upload failed.|
|**msoSyncEventUploadInitiated**|3|Upload initiated.|
|**msoSyncEventUploadSucceeded**|4|Upload succeeded.|

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]