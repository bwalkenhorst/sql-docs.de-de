---
title: SQLTransact Funktion | Microsoft Docs
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
apiname:
- SQLTransact
apilocation:
- sqlsrv32.dll
apitype: dllExport
f1_keywords:
- SQLTransact
helpviewer_keywords:
- SQLTransact function [ODBC]
ms.assetid: 496249e0-8eff-4c60-8358-5543bc3ead9c
caps.latest.revision: 13
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 30aec4f94ca469f46ea4da6636c847d4a663dc3c
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="sqltransact-function"></a>SQLTransact-Funktion
**Konformität**  
 Version eingeführt: ODBC 1.0 Standardkonformität: veraltet  
  
 **Zusammenfassung**  
 In ODBC 3. *x*, die ODBC 2.*.x* Funktion **SQLTransact** wurde ersetzt durch **SQLEndTran**. Weitere Informationen finden Sie unter [SQLEndTran](../../../odbc/reference/syntax/sqlendtran-function.md).  
  
> [!NOTE]  
>  Das Attribut SQL_ASYNC_DBC_FUNCTION_ENABLE, die in ODBC 3.8 eingeführt wurde, wird nicht von **SQLTransact**. Anwendungen, die mithilfe eines asynchronen Vorgangs für ein Verbindungshandle müssen verwenden **SQLEndTran**.  
  
## <a name="see-also"></a>Siehe auch  
 [ODBC-API-Referenz](../../../odbc/reference/syntax/odbc-api-reference.md)   
 [ODBC-Headerdateien](../../../odbc/reference/install/odbc-header-files.md)
