---
title: Funktionsweise erweiterter gespeicherter Prozeduren | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.service: ''
ms.component: extended-stored-procedures
ms.reviewer: ''
ms.suite: sql
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- extended stored procedures [SQL Server], about extended stored procedures
ms.assetid: 6e946d8c-3268-4b59-8a1c-1637909cd701
caps.latest.revision: 33
author: rothja
ms.author: jroth
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 98432d9a5274883ff98be97ca618d60fc5b82c63
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="how-extended-stored-procedures-work"></a>Funktionsweise erweiterter gespeicherter Prozeduren
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
    
> [!IMPORTANT]  
>  [!INCLUDE[ssNoteDepFutureDontUse](../../includes/ssnotedepfuturedontuse-md.md)] Verwenden Sie stattdessen die CLR-Integration.  
  
 Der Funktionsablauf einer erweiterten gespeicherten Prozedur kann folgendermaßen beschrieben werden:  
  
1.  Wenn ein Client eine erweiterte gespeicherte Prozedur ausgeführt wird, wird die Anforderung im tabular Data Stream (TDS) oder (SOAP, Simple Object Access Protocol)-Format von der Clientanwendung zum Übertragen [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)].  
  
2.  [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] sucht nach der mit der erweiterten gespeicherten Prozedur verknüpften DLL und lädt diese DLL, falls dies nicht bereits geschehen ist.  
  
3.  [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ruft die angeforderte erweiterte gespeicherte Prozedur, die als Funktion in der DLL implementiert ist, auf.  
  
4.  Die erweiterte gespeicherte Prozedur übergibt über die API für erweiterte gespeicherte Prozeduren Resultsets und Rückgabeparameter an den Server zurück.  
  
## <a name="see-also"></a>Siehe auch  
 [Datenbankmodul – Programmierung der erweiterten gespeicherten Prozedur](../../relational-databases/database-engine-extended-stored-procedure-programming.md)  
  
  
