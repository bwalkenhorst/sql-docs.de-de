---
title: Extrahieren eines Skripts aus einer Ablaufverfolgung (SQL Server Profiler) | Microsoft Docs
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.prod_service: sql-tools
ms.service: 
ms.component: sql-server-profiler
ms.reviewer: 
ms.suite: sql
ms.technology: database-engine
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- scripts [SQL Server], traces
- extracting script from trace [SQL Server]
ms.assetid: 431126a6-ff91-4818-8763-4442152bd571
caps.latest.revision: "20"
author: stevestein
ms.author: sstein
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 80d6996f5a6ccdd9f5ada54e30800dad22c4ad20
ms.sourcegitcommit: b6116b434d737d661c09b78d0f798c652cf149f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2018
---
# <a name="extract-a-script-from-a-trace-sql-server-profiler"></a>Extrahieren eines Skripts aus einer Ablaufverfolgung (SQL Server Profiler)
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]In diesem Thema wird beschrieben, wie extrahiert [!INCLUDE[tsql](../../includes/tsql-md.md)] -Ereignissen aus einer Ablaufverfolgungsdatei oder-Tabelle sowie das Speichern einer [!INCLUDE[tsql](../../includes/tsql-md.md)] -Skriptdatei mithilfe [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)].  
  
### <a name="to-extract-a-transact-sql-script-from-a-trace-file-or-table"></a>So extrahieren Sie ein Transact-SQL-Skript aus einer Ablaufverfolgungsdatei oder -tabelle  
  
1.  Öffnen Sie eine Ablaufverfolgungsdatei oder -tabelle, die [!INCLUDE[tsql](../../includes/tsql-md.md)]-Ereignisse enthält, die Sie in einer [!INCLUDE[tsql](../../includes/tsql-md.md)]-Skriptdatei speichern möchten. Weitere Informationen finden Sie unter [Öffnen einer Ablaufverfolgungsdatei &#40;SQL Server Profiler&#41;](../../tools/sql-server-profiler/open-a-trace-file-sql-server-profiler.md) oder [Öffnen einer Ablaufverfolgungstabelle &#40;SQL Server Profiler&#41;](../../tools/sql-server-profiler/open-a-trace-table-sql-server-profiler.md).  
  
2.  Zeigen Sie im Menü **Datei** auf **Exportieren**, zeigen Sie auf **SQL Server-Ereignisse extrahieren**, und klicken Sie dann auf **Transact-SQL-Ereignisse extrahieren**.  
  
3.  Geben Sie im Dialogfeld **Speichern unter** einen Namen für die [!INCLUDE[tsql](../../includes/tsql-md.md)] -Datei ein, und klicken Sie dann auf **Speichern**.  
  
## <a name="see-also"></a>Siehe auch  
 [SQL Server Profiler](../../tools/sql-server-profiler/sql-server-profiler.md)  
  
  
