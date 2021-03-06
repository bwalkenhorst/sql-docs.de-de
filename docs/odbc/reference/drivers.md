---
title: Treiber | Microsoft Docs
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
- ODBC architecture [ODBC], drivers
- drivers [ODBC]
- drivers [ODBC], about drivers
ms.assetid: d6795d92-877e-44e1-b7d5-2ff2fd3989bd
caps.latest.revision: 7
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 96e2052feaeef1a7b752afc8f2b81babe820e08a
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="drivers"></a>Treiber
*Treiber* sind Bibliotheken, die die Funktionen der ODBC-API zu implementieren. Jede bezieht sich auf ein bestimmtes DBMS; z. B. keinen Treiber für Oracle direkten Zugriff auf Daten in einer Informix-DBMS. Treiber verfügbar machen, das die Funktionen des zugrunde liegenden DBMS. Sie sind nicht erforderlich, zum Implementieren von Funktionen, die nicht vom DBMS unterstützt. Sollten Sie den Treiber z. B. wenn das zugrunde liegende DBMS outer-Joins dann weder nicht unterstützt. Nur wichtige Ausnahme ist, dass die Treiber für DBMS-Systeme, die keine eigenständigen Datenbankmodule, z. B. Xbase, eine Datenbank-Engine implementieren müssen, die mindestens eine minimale Menge an SQL unterstützt.  
  
 Dieser Abschnitt enthält die folgenden Themen.  
  
-   [Treiber-Aufgaben](../../odbc/reference/driver-tasks.md)  
  
-   [Treiberarchitektur](../../odbc/reference/driver-architecture.md)  
  
## <a name="see-also"></a>Siehe auch  
 [Von Microsoft gelieferte ODBC-Treiber](../../odbc/microsoft/microsoft-supplied-odbc-drivers.md)
