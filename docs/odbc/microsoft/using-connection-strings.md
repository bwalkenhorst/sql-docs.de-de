---
title: Verwenden von Verbindungszeichenfolgen | Microsoft Docs
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
- connection strings [ODBC]
- connecting to data source [ODBC], Visual FoxPro
- Visual FoxPro data source [ODBC], connecting
ms.assetid: 57634960-47e9-49bf-95c1-6e3702ac8166
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: a44ad994ff70c2597c1cf67be16695ea7e1198c5
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="using-connection-strings"></a>Verwenden von Verbindungszeichenfolgen
Sie können eine Verbindungszeichenfolge für die Verbindung mit einer Visual FoxPro-Datenquelle verwenden.  
  
 Um eine Verbindung herzustellen, auf die Datenquelle TasTrade und überschreiben die aktuelle Einstellung der exklusive mit der Datenquelle zugeordnet ist, verwenden Sie z. B. die Zeichenfolge:  
  
```  
DSN=TasTrade;Exclusive=Yes  
```  
  
 Eine Liste der Attribut-Schlüsselwörter und der Werte, die Sie in der Verbindungszeichenfolge enthalten können, finden Sie unter [SQLDriverConnect](../../odbc/microsoft/sqldriverconnect-visual-foxpro-odbc-driver.md).  
  
 Eine vollständige Erläuterung der Syntax für Verbindungszeichenfolgen finden Sie unter [SQLBrowseConnect](../../odbc/reference/syntax/sqlbrowseconnect-function.md) in der *ODBC Programmer's Reference*.
