---
title: sys.pdw_health_component_properties (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: pdw
ms.service: ''
ms.component: system-catalog-views
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 66999c0c-dc43-4327-99fb-8366f465e69d
caps.latest.revision: 7
author: barbkess
ms.author: barbkess
manager: craigg
ms.workload: Inactive
monikerRange: '>= aps-pdw-2016 || = sqlallproducts-allversions'
ms.openlocfilehash: 628432368c30d81f8a89b97baf1534ce9502403b
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="syspdwhealthcomponentproperties-transact-sql"></a>sys.pdw_health_component_properties (Transact-SQL)
[!INCLUDE[tsql-appliesto-xxxxxx-xxxx-xxxx-pdw-md](../../includes/tsql-appliesto-xxxxxx-xxxx-xxxx-pdw-md.md)]

  Speichert die Eigenschaften, die ein Gerät zu beschreiben. Einige Eigenschaften zeigen Gerätestatus, und einige Eigenschaften beschreiben das Gerät selbst.  
  
|Spaltenname|Datentyp|Description|Bereich|  
|-----------------|---------------|-----------------|-----------|  
|property_id|**int**|Eindeutiger Bezeichner der Eigenschaft einer Komponente.<br /><br /> Property_id und Component_id bilden den Schlüssel für diese Ansicht ein.|NOT NULL|  
|component_id|**int**|Die ID der Komponente. Finden Sie unter [sys.pdw_health_components &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-pdw-health-components-transact-sql.md).<br /><br /> Property_id und Component_id bilden den Schlüssel für diese Ansicht ein.|NOT NULL|  
|property_name|**nvarchar(255)**|Der Name der Eigenschaft.|NOT NULL|  
|physical_name|**nvarchar(32)**|Eigenschaftenname, wie vom Hersteller definiert.|NOT NULL|  
|is_key|**bit**|Bestimmt, ob der Geräteinstanz eindeutig oder nicht eindeutig ist.|NOT NULL<br /><br /> 0 – Geräteinstanz ist eindeutig.<br /><br /> 1 - Geräteinstanz ist nicht eindeutig.|  
  
## <a name="see-also"></a>Siehe auch  
 [SQL Datawarehouse und Parallel Datawarehouse-Katalogsichten](../../relational-databases/system-catalog-views/sql-data-warehouse-and-parallel-data-warehouse-catalog-views.md)  
  
  
