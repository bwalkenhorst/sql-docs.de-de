---
title: MSSQL_REPL020011 | Microsoft-Dokumentation
ms.custom: 
ms.date: 03/03/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- replication
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- MSSQL_REPL020011 error
ms.assetid: f72072d7-bbb6-48ad-ac88-afa74aeb4d58
caps.latest.revision: 16
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: Human Translation
ms.sourcegitcommit: f3481fcc2bb74eaf93182e6cc58f5a06666e10f4
ms.openlocfilehash: 7a00f6e4b34636b7788427ca12dcb98df8c01070
ms.contentlocale: de-de
ms.lasthandoff: 06/22/2017

---
# <a name="mssqlrepl020011"></a>MSSQL_REPL020011
    
## <a name="message-details"></a>Meldungsdetails  
  
|||  
|-|-|  
|Produktname|SQL Server|  
|Ereignis-ID|20011|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|[!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)]|  
|Symbolischer Name||  
|Meldungstext|Der Prozess konnte '%1' nicht auf '%2' ausführen.|  
  
## <a name="explanation"></a>Erklärung  
 Dieser Fehler kann unter verschiedenen Bedingungen während der Transaktionsreplikationsverarbeitung ausgelöst werden, z.B., wenn der Protokolllese-Agent **sp_replcmds** ausführt (Der Prozess konnte „sp_replcmds“ nicht auf \<Servername> ausführen) oder **sp_repldone** ausführt (Der Prozess konnte „sp_repldone“ nicht auf \<Servername> ausführen).  
  
## <a name="user-action"></a>Benutzeraktion  
 Wenn der Fehler in einer Datenbank ausgelöst wird, die Sie gerade erst aus einer Sicherung wiederhergestellt haben, müssen Sie sicherstellen, dass die in der Dokumentation zum Sichern und Wiederherstellen genannten Schritte ausgeführt wurden. Dazu zählt bei Bedarf auch die Ausführung von **sp_replrestart** . Weitere Informationen finden Sie unter [Strategien zum Sichern und Wiederherstellen einer Momentaufnahme- und Transaktionsreplikation](../../relational-databases/replication/administration/strategies-for-backing-up-and-restoring-snapshot-and-transactional-replication.md).  
  
 Bei diesem Fehler handelt es sich um einen internen Verarbeitungsfehler. Wenn er nicht im Zusammenhang mit einer Wiederherstellung ausgelöst wird, weist er in der Regel darauf hin, dass die Replikation entfernt und neu konfiguriert werden muss. Wenn das Entfernen der Replikation nicht möglich ist, wenden Sie sich an den Kundendienst.  
  
## <a name="see-also"></a>Siehe auch  
 [Fehler- und Ereignisreferenz &#40;Replikation&#41;](../../relational-databases/replication/errors-and-events-reference-replication.md)   
 [sp_replcmds &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-replcmds-transact-sql.md)   
 [sp_repldone &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-repldone-transact-sql.md)  
  
  