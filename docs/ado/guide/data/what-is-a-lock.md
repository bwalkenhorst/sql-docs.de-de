---
title: Was ist eine Sperre? | Microsoft Docs
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
helpviewer_keywords:
- cursors [ADO], locking
- locks [ADO], about locking
ms.assetid: f8989555-28c6-4c17-9bf8-7f44a8a5c407
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 945416224804a6e3b384981912d2375351012a8c
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2018
---
# <a name="what-is-a-lock"></a>Was ist eine Sperre?
Sperren ist der Prozess, der ein DBMS nach dem Zugriff auf eine Zeile in einer mehrbenutzerumgebung einschränkt. Wenn eine Zeile oder Spalte exklusiv gesperrt ist, sind andere Benutzer nicht zulässig, auf die gesperrten Daten zugreifen, bis die Sperre aufgehoben wird. Dadurch wird sichergestellt, dass zwei Benutzer gleichzeitig derselben Spalte in einer Zeile nicht aktualisieren können.  
  
 Sperren können im Hinblick auf Ressource sehr teuer sein und sollte nur bei Bedarf verwendet werden, um die Datenintegrität beizubehalten. In einer Datenbank, in dem Hunderten oder Tausenden von Benutzern versuchen konnte, einen Datensatz pro Sekunde zugreifen – z. B. eine Datenbank mit dem Internet verbundenen – unnötige sperren kann schnell zu Leistungseinbußen in Ihrer Anwendung führen.  
  
 Sie können steuern, wie die Datenquelle und die ADO-Cursorbibliothek Parallelität zu verwalten durch Auswahl der entsprechenden Sperren Option.  
  
 Legen Sie die **LockType** Eigenschaft vor dem Öffnen einer **Recordset** angeben, welche Art von Sperren des Anbieters verwenden soll, beim Öffnen. Lesen die Eigenschaft, um die Sperren auf ein offenes Rückgabetyp **Recordset** Objekt.  
  
 Anbieter unterstützen möglicherweise nicht alle Typen von Sperren. Wenn ein Anbieter nicht die angeforderte unterstützt **LockType** festlegen, ersetzen sie einen anderen Typ von Sperren. Um zu bestimmen, die eigentliche Sperre Funktionen, die in einem **Recordset** -Objekts die [unterstützt](../../../ado/reference/ado-api/supports-method.md) Methode mit **AdUpdate** und **AdUpdateBatch**.  
  
 Die **AdLockPessimistic** Einstellung wird nicht unterstützt, wenn die [CursorLocation](../../../ado/reference/ado-api/cursorlocation-property-ado.md) -Eigenschaftensatz auf **AdUseClient.** Wenn ein nicht unterstützter Wert festgelegt ist, wird kein Fehler gemeldet. unterstützt die nächstgelegene **LockType** wird stattdessen verwendet.  
  
 Die **LockType** Eigenschaft gilt Lese-/Schreibzugriff bei der **Recordset** geschlossen und schreibgeschützt ist, wenn er geöffnet ist.  
  
 Dieser Abschnitt enthält die folgenden Themen.  
  
-   [Typen von Sperren](../../../ado/guide/data/types-of-locks.md)
