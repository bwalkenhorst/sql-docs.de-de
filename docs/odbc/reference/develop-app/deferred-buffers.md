---
title: Verzögerte Puffer | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: drivers
ms.service: ''
ms.component: odbc
ms.reviewer: ''
ms.suite: sql
ms.technology:
- drivers
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- buffers [ODBC], deferred
- deferred buffers [ODBC]
ms.assetid: 02c9a75c-2103-4f68-a1db-e31f7e0f1f03
caps.latest.revision: 6
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 5273f48c96039e543e24c2945cd5cda14d352e6d
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="deferred-buffers"></a>Verzögerte Puffer
Ein *verzögerte Puffer* ist, deren Wert, zu einem Zeitpunkt verwendet wird *nach* in einem Funktionsaufruf angegeben ist. Beispielsweise **SQLBindParameter** wird verwendet, um zuzuordnen, oder *zu binden,* einen Datenpuffer mit einem Parameter in einer SQL-Anweisung. Die Anwendung gibt die Anzahl der Parameter und übergibt die Adresse, die Bytelänge und den Typ des Puffers. Der Treiber speichert diese Informationen jedoch nicht zur Untersuchung von Inhalten aus dem Puffer. Später, wenn die Anwendung die Anweisung ausführt, der Treiber Ruft die Informationen ab und verwendet, um die Parameterdaten abrufen und an die Datenquelle gesendet. Aus diesem Grund wird die Eingabe von Daten in den Puffer verzögert. Da verzögerte Puffer werden in eine bestimmte Funktion angegeben und in einer anderen verwendet, ist es ein anwendungsprogrammierungsfehler Fehler um eine verzögerte Puffer freizugeben, während der Treiber noch vorhanden sein, erwartet; Weitere Informationen finden Sie unter [Allocating und Freigeben von Puffern](../../../odbc/reference/develop-app/allocating-and-freeing-buffers.md)weiter unten in diesem Abschnitt.  
  
 Sowohl Eingabe- und Ausgabepuffern können verschoben werden. In der folgenden Tabelle werden die Verwendungen der verzögerten Puffer zusammengefasst. Beachten Sie, dass die verzögerte Puffer, die gebundenen Spalten im Ergebnis angegeben werden, mit **SQLBindCol**, und verzögerte Puffer an SQL-Anweisungsparameter gebunden werden mit **SQLBindParameter**.  
  
|Puffer verwenden|Typ|Mit angegeben wird|Verwendet von|  
|----------------|----------|--------------------|-------------|  
|Senden von Daten für Eingabeparameter|Verzögerte Eingabe|**SQLBindParameter**|**SQLExecute**<br /> **SQLExecDirect**|  
|Sendende von Daten zu aktualisieren, oder fügen Sie eine Zeile in einem Resultset festlegen|Verzögerte Eingabe|**SQLBindCol**|**SQLSetPos**|  
|Zurückgeben von Daten für die Ausgabe und Eingabe/Ausgabe-Parameter|Verzögerte Ausgabe|**SQLBindParameter**|**SQLExecute**<br /> **SQLExecDirect**|  
|Setzen Sie Resultsets zurückgeben|Verzögerte Ausgabe|**SQLBindCol**|**SQLFetch**<br /> **SQLFetchScroll SQLSetPos**|
