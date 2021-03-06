---
title: ConnectComplete und Disconnect-Ereignisse (ADO) | Microsoft Docs
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
- Disconnect
- Connection::ConnectComplete
- ConnectComplete
- Connection::Disconnect
helpviewer_keywords:
- Disconnect event [ADO]
- ConnectComplete event [ADO]
ms.assetid: 568f5252-d069-4d99-a01b-2ada87ad1304
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 7ca521c0e850dd7fdacee6cd594b5c9f23a289d3
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2018
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>ConnectComplete und Disconnect-Ereignisse (ADO)
Die **ConnectComplete** Ereignis wird aufgerufen, nachdem eine Verbindung gestartet wird. Die **trennen** Ereignis wird aufgerufen, nachdem eine Verbindung beendet.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
ConnectComplete pError, adStatus, pConnection  
Disconnect adStatus, pConnection  
```  
  
#### <a name="parameters"></a>Parameter  
 *pError*  
 Ein [Fehler](../../../ado/reference/ado-api/error-object.md) Objekt. Wenn aufgetretenen Fehlers beschrieben der Wert der *AdStatus* ist **AdStatusErrorsOccurred**; andernfalls ist es nicht festgelegt.  
  
 *adStatus*  
 Ein [EventStatusEnum](../../../ado/reference/ado-api/eventstatusenum.md) Wert, der immer gibt **AdStatusOK**.  
  
 Wenn **ConnectComplete** wird aufgerufen, wird dieser Parameter auf festgelegt **AdStatusCancel** Wenn eine **WillConnect** Ereignis hat den Abbruch der ausstehenden Verbindung angefordert.  
  
 Bevor entweder Ereignis zurückgegeben wird, legen Sie diesen Parameter auf **AdStatusUnwantedEvent** um nachfolgende Benachrichtigungen zu verhindern. Allerdings schließen und erneutes Öffnen der [Verbindung](../../../ado/reference/ado-api/connection-object-ado.md) bewirkt, dass diese Ereignisse erneut auftreten.  
  
 *pConnection*  
 Die **Verbindung** -Objekt für die dieses Ereignis angewendet wird.  
  
## <a name="see-also"></a>Siehe auch  
 [ADO-Ereignisse Modell (VC++-Beispiel)](../../../ado/reference/ado-api/ado-events-model-example-vc.md)   
 [ADO-Ereignishandler – Zusammenfassung](../../../ado/guide/data/ado-event-handler-summary.md)
