---
title: ExecuteOptions-Eigenschaft (RDS) | Microsoft Docs
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: ado
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: sql
ms.tgt_pltfrm: 
ms.topic: article
apitype: COM
helpviewer_keywords:
- ExecuteOptions property [ADO], VBScript example
ms.assetid: 62a4fd88-afc3-4f1f-b978-40710a30c4e9
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 7cc52b6deb9915abd9f90b8596edee5ded07f816
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2018
---
# <a name="executeoptions-property-rds"></a>ExecuteOptions-Eigenschaft (RDS)
Gibt an, ob asynchrone Ausführung aktiviert ist.  
  
> [!IMPORTANT]
>  Ab Windows 8 und Windows Server 2012, sind nicht mehr RDS-Server-Komponenten in Windows-Betriebssystems enthalten (finden Sie unter Windows 8 und [Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/en-us/download/details.aspx?id=27416) detailliertere). RDS-Clientkomponenten werden in einer zukünftigen Version von Windows entfernt werden. Verwenden Sie diese Funktion beim Entwickeln neuer Anwendungen nicht, und planen Sie das Ändern von Anwendungen, in denen es zurzeit verwendet wird. Anwendungen, die RDS verwenden sollten migrieren [WCF Data Service](http://go.microsoft.com/fwlink/?LinkId=199565).  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt fest oder gibt einen der folgenden Werte zurück.  
  
|Konstante|Description|  
|--------------|-----------------|  
|**adcExecSync**|Führt die nächste Aktualisierung von der [Recordset](../../../ado/reference/ado-api/recordset-object-ado.md) synchron.|  
|**adcExecAsync**|Standard. Führt die nächste Aktualisierung von der **Recordset** asynchron.|  
  
> [!NOTE]
>  Jede ausführbare Datei, die diese Konstanten verwendet muss die Deklarationen für sie bereitstellen. Sie können Ausschneiden und Einfügen von Konstanten Deklarationen, die Sie aus der Datei Adcvbs.inc, in den standardmäßigen Installationsordner für die RDS-Bibliothek gespeichert werden soll.  
  
## <a name="remarks"></a>Hinweise  
 Wenn **ExecuteOptions** auf festgelegt ist **AdcExecAsync**, und dies asynchron die nächste führt **aktualisieren** rufen Sie für die [RDS. DataControl](../../../ado/reference/rds-api/datacontrol-object-rds.md) des Objekts **Recordset**.  
  
 Wenn Sie versuchen, rufen Sie [zurücksetzen](../../../ado/reference/rds-api/reset-method-rds.md), [aktualisieren](../../../ado/reference/rds-api/refresh-method-rds.md), [SubmitChanges](../../../ado/reference/rds-api/submitchanges-method-rds.md), [CancelUpdate](../../../ado/reference/ado-api/cancelupdate-method-ado.md), oder [Recordset](../../../ado/reference/rds-api/recordset-sourcerecordset-properties-rds.md) ein anderer asynchronen Vorgang, die sich ändern, kann dagegen die [RDS. DataControl](../../../ado/reference/rds-api/datacontrol-object-rds.md) des Objekts **Recordset** ausgeführt wird, wird ein Fehler auftritt.  
  
 Wenn ein Fehler, während einer asynchronen Operation auftritt der **RDS. DataControl** des Objekts [ReadyState](../../../ado/reference/rds-api/readystate-property-rds.md) Wert ändert sich von **AdcReadyStateLoaded** auf **AdcReadyStateComplete**, und die  **Recordset** Eigenschaftswert bleibt *nichts*.  
  
## <a name="applies-to"></a>Gilt für  
 [DataControl-Objekt (RDS)](../../../ado/reference/rds-api/datacontrol-object-rds.md)  
  
## <a name="see-also"></a>Siehe auch  
 [ExecuteOptions und FetchOptions Eigenschaften Beispiel (VBScript)](../../../ado/reference/rds-api/executeoptions-and-fetchoptions-properties-example-vbscript.md)   
 [Cancel-Methode (RDS)](../../../ado/reference/rds-api/cancel-method-rds.md)


