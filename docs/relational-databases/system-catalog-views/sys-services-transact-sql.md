---
title: Sys.Services (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.service: ''
ms.component: system-catalog-views
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- sys.services
- services
- services_TSQL
- sys.services_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.services catalog view
ms.assetid: 16d0b0c5-5cce-469b-aa3d-4b9248e0c085
caps.latest.revision: 34
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 78dc605705ec54d912adcf32a7c03441eacefa57
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="sysservices-transact-sql"></a>sys.services (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Diese Katalogsicht enthält eine Zeile für jeden Dienst in der Datenbank.  
  
|Spaltenname|Datentyp|Description|  
|-----------------|---------------|-----------------|  
|**name**|**sysname**|Nach Groß-/Kleinschreibung unterschiedener Name des in der Datenbank eindeutigen Diensts. Lässt keine NULL-Werte zu.|  
|**service_id**|**int**|Bezeichner des Diensts. Lässt keine NULL-Werte zu.|  
|**principal_id**|**int**|Bezeichner des Datenbankprinzipals, der diesen Dienst besitzt. Lässt NULL-Werte zu.|  
|**service_queue_id**|**int**|Objekt-ID der Warteschlange, die dieser Dienst verwendet. Lässt keine NULL-Werte zu.|  
  
## <a name="permissions"></a>Berechtigungen  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)] Weitere Informationen finden Sie unter [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md).  
  
  
