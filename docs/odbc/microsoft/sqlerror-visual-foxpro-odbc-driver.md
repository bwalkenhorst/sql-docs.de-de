---
title: SQLError (Visual FoxPro-ODBC-Treiber) | Microsoft Docs
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
- SQLError function [ODBC], Visual FoxPro ODBC Driver
ms.assetid: 8315ec16-1c22-447a-a577-39bd94f61070
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 7b18b8a103df01f0ff6200b2a5630ef6dca8ae68
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="sqlerror-visual-foxpro-odbc-driver"></a>SQLError (Visual FoxPro-ODBC-Treiber)
> [!NOTE]  
>  Dieses Thema enthält Visual FoxPro-ODBC-Treiber-spezifische Informationen. Allgemeine Informationen zu dieser Funktion finden Sie unter den entsprechenden Themen unter [ODBC API Reference](../../odbc/reference/syntax/odbc-api-reference.md).  
  
 Unterstützung: vollständige  
  
 : ODBC-API Core Konformitätsgrad  
  
 Fehler oder Status Informationen zu den letzten Fehler zurückgegeben. Der Treiber behält einen Stapel oder eine Liste von Fehlern, die für zurückgegeben werden, können die *Befehls beschäftigt*, *Hdbc*, und *Henv* Argumente, je nachdem, wie der Aufruf von **SQLError**  erfolgt. Die Fehlerwarteschlange wird nach jeder Anweisung geleert.  
  
 Die folgende Tabelle beschreibt die **SQLError** Argumente und Rückgabewerte, die vom Treiber verwendet wird.  
  
|SQLError-argument|Rückgabewert-Beschreibung|  
|-----------------------|------------------------------|  
|*szSQLState*|Der Wert für den SQLSTATE, dargestellt durch den Fehler.|  
|*pfNativeError*|Gibt ein Wert ungleich NULL an eine [Visual FoxPro-ODBC-Treiber systemeigene Fehlermeldung](../../odbc/microsoft/visual-foxpro-odbc-driver-native-error-messages.md). Der Wert 0 (null) gibt an, der Fehler vom Treiber erkannt wurden und auf die entsprechenden zugeordnet wurde [ODBC-Fehlercode](../../odbc/microsoft/odbc-error-codes-visual-foxpro-odbc-driver.md).|  
|*von SQLDiagRec()*|Der Text für die systemeigene oder ODBC-Fehler.|  
|*pcbErrorMsg*|Die Länge der den Meldungstext plus die Länge der Bezeichner.|  
  
 Weitere Informationen zu Fehlermeldungen Treiber finden Sie unter [Fehler (Übersicht)](../../odbc/microsoft/error-messages-visual-foxpro-odbc-driver.md). Weitere Informationen zu dieser Funktion finden Sie unter [SQLError](../../odbc/reference/syntax/sqlerror-function.md) in der *ODBC Programmer's Reference*.
