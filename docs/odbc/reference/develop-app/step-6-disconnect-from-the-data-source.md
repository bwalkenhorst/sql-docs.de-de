---
title: 'Schritt 6: Trennen Sie die Datenquelle | Microsoft Docs'
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
- application process [ODBC], disconnecting from data source
- data sources [ODBC], disconnecting
- disconnecting from data source [ODBC]
ms.assetid: 6ad759ba-4721-4d8f-9b26-de976d4fc1a0
caps.latest.revision: 8
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 5271ba2554e726cc3855cb933f10882afad76fa0
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="step-6-disconnect-from-the-data-source"></a>Schritt 6: Aus der Datenquelle zu trennen
Der letzte Schritt besteht aus der Datenquelle zu trennen, wie in der folgenden Abbildung dargestellt. Die Anwendung zunächst durch Aufrufen von alle Anweisungshandles freigibt **SQLFreeHandle**. Weitere Informationen finden Sie unter [Freigabe ein Anweisungshandle](../../../odbc/reference/develop-app/freeing-a-statement-handle-odbc.md).  
  
 ![Trennen von einer Datenquelle zeigt](../../../odbc/reference/develop-app/media/pr17.gif "pr17")  
  
 Als Nächstes die Datenquelle mit die Anwendung trennt **SQLDisconnect** und das Verbindungshandle mit freigegeben **SQLFreeHandle**. Weitere Informationen finden Sie unter [Trennen von einer Datenquelle oder Treiber](../../../odbc/reference/develop-app/disconnecting-from-a-data-source-or-driver.md).  
  
 Schließlich gibt die Anwendung das Umgebungshandle mit **SQLFreeHandle** und entladen wird der Treiber-Manager. Weitere Informationen finden Sie unter [Reservieren der Umgebung behandelt](../../../odbc/reference/develop-app/allocating-the-environment-handle.md).
