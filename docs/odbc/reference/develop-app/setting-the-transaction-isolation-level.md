---
title: Festlegen der Transaktionsisolation | Microsoft Docs
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: odbc
ms.reviewer: 
ms.suite: sql
ms.technology: drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- isolation levels [ODBC]
- transaction isolation [ODBC]
- transactions [ODBC], isolation
ms.assetid: 64a037f0-5065-4f45-9669-6710404a540c
caps.latest.revision: "6"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 74c345bb8bdfae60a06576b43b655ef78e4a6dfc
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="setting-the-transaction-isolation-level"></a>Die Transaction Isolation festlegen Level
Um die Isolationsebene der Transaktion festgelegt, verwendet eine Anwendung das Verbindungsattribut SQL_ATTR_TXN_ISOLATION. Wenn die Datenquelle die angeforderte Isolationsstufe nicht unterstützt, kann der Treiber oder die Datenquelle eine höhere Ebene festgelegt. Um zu bestimmen, welche Transaktionsisolationsstufen wird eine Datenquelle unterstützt, und welche die Standardisolationsstufe ist, eine Anwendung ruft **SQLGetInfo** mit den Optionen dem SQL_TXN_ISOLATION_OPTION und SQL_DEFAULT_TXN_ISOLATION bzw.  
  
 Höheres Maß an Isolation jeder Transaktion bieten, die meisten Schutz für die Integrität von Datenbankdaten. Serialisierbare Transaktionen sind nicht betroffen von anderen Transaktionen garantiert, und daher sichergestellt, dass Datenbankintegrität zu wahren.  
  
 Ein höheres Maß an Isolation jeder Transaktion kann jedoch Leistungseinbußen führen, da es die Wahrscheinlichkeit, die die Anwendung Sperren für Daten erhöht, die veröffentlicht werden gewartet hat. Eine Anwendung kann eine niedrigere Ebene der Isolation zum Erhöhen der Leistung in den folgenden Fällen angeben:  
  
-   Wenn sichergestellt werden kann, dass keine anderen Transaktionen, die vorhanden sind, möglicherweise mit Transaktionen für eine Anwendung beeinträchtigen. Diese Situation tritt nur unter bestimmten Umständen, z. B. wenn eine Person in einem kleinen Unternehmen dBASE-Dateien verwaltet, die persönliche Daten auf einem Computer enthalten und teilt diese Dateien nicht.  
  
-   Wenn die Geschwindigkeit ist wichtiger ist als die Genauigkeit und ggf. aufgetretenen Fehlern wahrscheinlich klein sind. Nehmen wir beispielsweise an, dass ein Unternehmen viele kleine Verkäufe macht und große Sales selten sind. Eine Transaktion, die den Gesamtwert der Verkäufe aller geöffneten schätzt kann problemlos mit Read Uncommitted-Isolationsstufe verwenden. Obwohl die Transaktion Aufträge enthält, die geöffnet oder geschlossen und anschließend werden Rollback, würden diese miteinander im Allgemeinen Abbrechen und Transaktion würde viel schneller werden, da er nicht blockiert wird, jedes Mal, wenn diese It solche eine Bestellung auftritt.  
  
 Weitere Informationen finden Sie unter [vollständige Parallelität](../../../odbc/reference/develop-app/optimistic-concurrency.md).
