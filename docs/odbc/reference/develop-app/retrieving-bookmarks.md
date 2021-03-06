---
title: Abrufen von Lesezeichen | Microsoft Docs
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
- retrieving bookmarks [ODBC]
- result sets [ODBC], bookmarks
- bookmarks [ODBC]
ms.assetid: a34c8f09-b786-4835-a44b-b7294c970aff
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 0d31e012efba212b1acbac0d4127459147508fd1
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="retrieving-bookmarks"></a>Abrufen von Lesezeichen
Wenn die Anwendung zu Lesezeichen verwenden, muss er das SQL_ATTR_USE_BOOKMARKS-Anweisungsattribut auf SQL_UB_VARIABLE vor dem Vorbereiten oder Ausführen der Anweisung festgelegt. Dies ist erforderlich, da erstellen und Verwalten von Lesezeichen ein aufwendiger Vorgang sein können, damit Lesezeichen aktiviert werden soll, nur, wenn eine Anwendung gute vornehmen, kann diese verwenden.  
  
 Lesezeichen werden als 0-Spalte des Resultsets zurückgegeben. Es gibt drei Möglichkeiten, die eine Anwendung abgerufen werden kann:  
  
-   Binden Sie die Spalte 0 des Resultsets. **SQLFetch** oder **SQLFetchScroll** gibt das Lesezeichen für jede Zeile im Rowset zusammen mit den Daten für andere Spalten gebunden.  
  
-   Rufen Sie **SQLSetPos** auf eine Zeile im Rowset zu positionieren, und rufen Sie anschließend **SQLGetData** für die Spalte 0. Wenn ein Treiber Lesezeichen unterstützt, muss es immer die Möglichkeit zum Aufruf unterstützen **SQLGetData** für die Spalte 0, auch wenn dies nicht zulässt, dass aufrufen, **SQLGetData** für andere Spalten vor der letzten gebundenen die Spalte.  
  
-   Rufen Sie **SQLBulkOperations** mit der *Vorgang* Argument auf SQL_ADD festgelegt, und die Spalte 0 gebunden. Der Cursor die Zeile eingefügt, und gibt das Lesezeichen für die Zeile in der gebundenen Puffer zurück.
