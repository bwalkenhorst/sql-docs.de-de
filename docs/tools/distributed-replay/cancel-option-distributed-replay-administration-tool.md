---
title: Option Abbrechen (Verwaltungstool Distributed Replay) | Microsoft Docs
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: fea376de-307a-4b45-b7e2-37df88f3681a
caps.latest.revision: 15
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f3481fcc2bb74eaf93182e6cc58f5a06666e10f4
ms.openlocfilehash: 2eda4d5628a755f6312bb13f573d306e4650294d
ms.contentlocale: de-de
ms.lasthandoff: 08/02/2017

---
# <a name="cancel-option-distributed-replay-administration-tool"></a>Option Abbrechen (Verwaltungstool Distributed Replay)
  Das Verwaltungstool [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Distributed Replay ( **DReplay.exe**) ist ein Befehlszeilentool, das Sie für die Kommunikation mit dem Distributed Replay-Controller verwenden können. In diesem Thema werden die **cancel** -Befehlszeilenoption und die entsprechende Syntax beschrieben.  
  
 Die **cancel** -Option bricht den aktuellen Vorgang ab, der auf dem Controller ausgeführt wird.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Thema Linksymbol") Weitere Informationen zu den Syntaxkonventionen, die für das Verwaltungstool verwendet werden, finden Sie unter [Transact-SQL-Syntaxkonventionen &#40; Transact-SQL &#41; ](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md).  
  
## <a name="syntax"></a>Syntax  
  
```  
  
dreplay cancel [-m controller] [-q]   
```  
  
#### <a name="parameters"></a>Parameter  
 **-m** *controller*  
 Der Computername des Controllers. Sie können mit "`localhost`" oder "`.`" auf den lokalen Computer verweisen.  
  
 Wenn der **-m** -Parameter nicht angegeben ist, wird der lokale Computer verwendet.  
  
 **-q**  
 Stiller Modus. Fordert nicht zur Bestätigung auf.  
  
 Der **-q** -Parameter ist optional.  
  
## <a name="examples"></a>Beispiele  
 Im folgenden Beispiel wird eine Abbruchanforderung im stillen Modus gesendet. Der Wert `localhost` gibt an, dass der Controllerdienst auf demselben Computer wie das Verwaltungstool ausgeführt wird.  
  
```  
dreplay cancel –m localhost -q  
```  
  
## <a name="permissions"></a>Berechtigungen  
 Sie müssen das Verwaltungstool als interaktiver Benutzer mit einem lokalen Benutzerkonto oder Domänenbenutzerkonto ausführen. Um ein lokales Benutzerkonto zu verwenden, müssen das Verwaltungstool und der Controller auf demselben Computer ausgeführt werden.  
  
 Weitere Informationen finden Sie unter [Distributed Replay Security](../../tools/distributed-replay/distributed-replay-security.md).  
  
## <a name="see-also"></a>Siehe auch  
 [SQL Server Distributed Replay](../../tools/distributed-replay/sql-server-distributed-replay.md)  
  
  