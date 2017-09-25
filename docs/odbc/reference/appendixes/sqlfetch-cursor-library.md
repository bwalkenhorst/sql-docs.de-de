---
title: SQLFetch (Cursorbibliothek) | Microsoft Docs
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- SQLFetch function [ODBC], Cursor Library
ms.assetid: 35a0d493-778b-4fb1-84ee-a13540e2fe0e
caps.latest.revision: 8
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 1e5cabca53c503e2cd0c12147248b11da84ed157
ms.contentlocale: de-de
ms.lasthandoff: 09/09/2017

---
# <a name="sqlfetch-cursor-library"></a>SQLFetch (Cursor Library)
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt werden. Verwenden Sie diese Funktion beim Entwickeln neuer Anwendungen und Planen von Anwendungen zu ändern, die dieses Feature verwenden. Microsoft empfiehlt die Verwendung der Cursorfunktionalität der Treiber.  
  
 In diesem Thema erläutert die Verwendung von der **SQLFetch** -Funktion in der Cursorbibliothek. Allgemeine Informationen zur **SQLFetch**, finden Sie unter [SQLFetch-Funktion](../../../odbc/reference/syntax/sqlfetch-function.md).  
  
 Wenn die Cursorbibliothek verwendet wird, Aufrufe von **SQLFetch** kann nicht kombiniert werden, mit der Aufrufe von **SQLFetchScroll** oder **SQLExtendedFetch**.  
  
 Wenn **SQLFetch** heißt mit SQL_ATTR_ROW_ARRAY_SIZE auf einen Wert größer als 1 festgelegt, wird die Cursorbibliothek den Aufruf an den Treiber übergeben. Wenn der Treiber eine ODBC-2 ist. *x* -Treiber die Rowsetgröße wird ignoriert und der Aufruf von **SQLFetch** wird eine einzelne Zeile mit Daten zurückgegeben.  
  
 Wenn die Cursorbibliothek mit einer ODBC 2. verwendet wird. *x* -Treiber verwenden, eine Bindung mit dem offset (gemäß der SQL_ATTR_ROW_BIND_OFFSET_PTR-Anweisungsattribut) wird nicht verwendet, wenn **SQLFetch** aufgerufen wird.  
  
 Eine Anwendung kann nicht aufgerufen, wenn die Cursorbibliothek geladen ist, **SQLFetch** Lesezeichenspalten abgerufen. Die Cursorbibliothek übergibt den Aufruf von **SQLFetch** über den Treiber, aber die Funktion aufruft, zum Aktivieren von Lesezeichen und binden die Lesezeichenspalte abgefangen werden durch die Cursorbibliothek.