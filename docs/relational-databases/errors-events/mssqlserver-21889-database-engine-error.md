---
title: MSSQLSERVER_21889 | Microsoft-Dokumentation
ms.custom: 
ms.date: 04/04/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: errors-events
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
helpviewer_keywords:
- 21889 (Database Engine error)
ms.assetid: ae199540-7986-4cc2-b782-cd22793236d3
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 44c79bc99f26399ec6494deb249342ce3037123a
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="mssqlserver21889"></a>MSSQLSERVER_21889
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  
## <a name="details"></a>Details  
  
|||  
|-|-|  
|Produktname|SQL Server|  
|Ereignis-ID|21889|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|SQLErrorNum21889|  
|Meldungstext|Die [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Instanz '%s' ist kein Replikationsverleger. Führen Sie **sp_adddistributor** auf der [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Instanz '%s' mit dem Verteiler '%s' aus, um die Instanz als Host der Veröffentlichungsdatenbank '%s' zu aktivieren. Stellen Sie sicher, dass Sie die gleiche Anmeldung und das gleiche Kennwort angeben, die für den ursprünglichen Verleger verwendet worden sind.|  
  
## <a name="explanation"></a>Erklärung  
Um die Verlegerdatenbank hosten zu können, muss die Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ein Replikationsverleger sein. **sp_validate_redirected_publisher** ruft **sp_helpdistributor** auf dem Remoteserver auf, um zu bestimmen, ob es sich beim Server um einen Replikationsverleger handelt. Dieser Fehler wird zurückgegeben, wenn die Ausführung der gespeicherten Prozedur **sp_helpdistributor** ergibt, dass die Zielinstanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] kein Replikationsverleger ist.  
  
## <a name="user-action"></a>Benutzeraktion  
Führen Sie **sp_adddistributor** bei der Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] aus, die als Host der Verlegerdatenbank fungiert. Wenn Sie **sp_adddistributor** ausführen, geben Sie den richtigen Verteiler an. Verwenden Sie den Wert für den *@password*-Parameter, der verwendet wurde, als **sp_adddistributor** zum ersten Mal beim Verteiler ausgeführt wurde.  
  
