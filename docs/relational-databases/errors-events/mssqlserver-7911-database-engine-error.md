---
title: MSSQLSERVER_7911 | Microsoft-Dokumentation
ms.custom: 
ms.date: 04/04/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
helpviewer_keywords:
- 7911 (Database Engine error)
ms.assetid: dd8390f3-0f77-4fb2-ba94-631a56e42bc6
caps.latest.revision: 16
author: BYHAM
ms.author: rickbyh
manager: jhubbard
robots: noindex,nofollow
translationtype: Human Translation
ms.sourcegitcommit: 2edcce51c6822a89151c3c3c76fbaacb5edd54f4
ms.openlocfilehash: a263211de746ed459a1f76c1146671bb0f746301
ms.lasthandoff: 04/11/2017

---
# <a name="mssqlserver7911"></a>MSSQLSERVER_7911
  
## <a name="details"></a>Details  
  
|||  
|-|-|  
|Produktname|SQL Server|  
|Ereignis-ID|7911|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|DBCC2_REPAIR_PAGE_DEALLOCATED|  
|Meldungstext|Reparaturvorgang: Die Zuordnung der Seite P_ID zu Objekt-ID O_ID, Index-ID I_ID, Partitions-ID PN_ID, Zuordnungseinheits-ID A_ID (Typ TYPE) wurde aufgehoben.|  
  
## <a name="explanation"></a>Erklärung  
Dies ist eine Informationsmeldung von REPAIR, die besagt, dass die Zuordnung einer Seite zu dem einseitigen Slotarray einer IAM-Seite (Index Allocation Map) aufgehoben wurde.  
  
## <a name="user-action"></a>Benutzeraktion  
Keine  
  
