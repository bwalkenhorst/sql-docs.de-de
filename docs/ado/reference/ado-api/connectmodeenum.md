---
title: ConnectModeEnum | Microsoft Docs
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
f1_keywords:
- ConnectModeEnum
helpviewer_keywords:
- ConnectModeEnum enumeration [ADO]
ms.assetid: 3792c294-5161-4538-a908-22a5fc50b85f
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 9f524d7d0385de331abed8d857296c55fcdbdc64
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2018
---
# <a name="connectmodeenum"></a>ConnectModeEnum
Gibt die verfügbaren Berechtigungen zum Ändern von Daten in eine [Verbindung](../../../ado/reference/ado-api/connection-object-ado.md), öffnen eine [Datensatz](../../../ado/reference/ado-api/record-object-ado.md), oder das Angeben von Werten für die [Modus](../../../ado/reference/ado-api/mode-property-ado.md) Eigenschaft von der  **Datensatz** und [Stream](../../../ado/reference/ado-api/stream-object-ado.md) Objekte.  
  
|Konstante|Wert|Description|  
|--------------|-----------|-----------------|  
|**adModeRead**|1|Gibt an, nur-Lese Zugriff.|  
|**adModeReadWrite**|3|Gibt Lese-/Schreibberechtigungen an.|  
|**adModeRecursive**|0x400000|Wird in Verbindung mit den anderen  *\*ShareDeny\**  Werte (**AdModeShareDenyNone**, **AdModeShareDenyWrite**, oder **AdModeShareDenyRead**) freigabebeschränkungen an alle untergeordneten Datensätze des aktuellen weitergegeben **Datensatz**. Es hat keine Auswirkung, wenn die **Datensatz** verfügt nicht über alle untergeordneten Elemente. Ein Laufzeitfehler wird generiert, wenn seine Verwendung **AdModeShareDenyNone** nur. Es kann jedoch verwendet werden, mit **AdModeShareDenyNone** in Kombination mit anderen Werten. Beispielsweise können Sie "**AdModeRead** oder **AdModeShareDenyNone** oder **AdModeRecursive**".|  
|**adModeShareDenyNone**|16|Können andere Benutzer eine Verbindung mit Berechtigungen zu öffnen. Weder Lese-noch Schreibezugriff kann anderen Benutzern verweigert werden.|  
|**adModeShareDenyRead**|4|Verhindert, dass andere Öffnen einer Verbindung mit Leseberechtigungen.|  
|**adModeShareDenyWrite**|8|Verhindert, dass andere Benutzer mit Schreibberechtigungen eine Verbindung geöffnet.|  
|**adModeShareExclusive**|12|Hindert andere Benutzer eine Verbindung zu öffnen.|  
|**adModeUnknown**|0|Standard. Gibt an, dass die Berechtigungen noch nicht festgelegt wurden oder können nicht bestimmt werden.|  
|**adModeWrite**|2|Gibt an, nur-schreiben Berechtigungen.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Paket: **com.ms.wfc.data**  
  
|Konstante|  
|--------------|  
|AdoEnums.ConnectMode.READ|  
|AdoEnums.ConnectMode.READWRITE|  
|(Es gibt keine Entsprechung der AdoEnums.ConnectMode.RECURSIVE)|  
|AdoEnums.ConnectMode.SHAREDENYNONE|  
|AdoEnums.ConnectMode.SHAREDENYREAD|  
|AdoEnums.ConnectMode.SHAREDENYWRITE|  
|AdoEnums.ConnectMode.SHAREEXCLUSIVE|  
|AdoEnums.ConnectMode.UNKNOWN|  
|AdoEnums.ConnectMode.WRITE|  
  
## <a name="applies-to"></a>Gilt für  
  
|||  
|-|-|  
|[Mode-Eigenschaft (ADO)](../../../ado/reference/ado-api/mode-property-ado.md)|[Open-Methode (ADO Record)](../../../ado/reference/ado-api/open-method-ado-record.md)|  
|[Open-Methode (ADO Stream)](../../../ado/reference/ado-api/open-method-ado-stream.md)|[Stream-Objekt (ADO)](../../../ado/reference/ado-api/stream-object-ado.md)|
