---
title: Xp_sprintf (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.service: ''
ms.component: system-stored-procedures
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- xp_sprintf_TSQL
- xp_sprintf
dev_langs:
- TSQL
helpviewer_keywords:
- xp_sprintf
ms.assetid: 1eedd65c-03cc-4eab-b76e-04684fdfec52
caps.latest.revision: 33
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
monikerRange: '>= aps-pdw-2016 || = azuresqldb-current || = azure-sqldw-latest || >= sql-server-2016 || = sqlallproducts-allversions'
ms.openlocfilehash: d19cd0ef278b0750f589d6526f3caf553df214c3
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="xpsprintf-transact-sql"></a>xp_sprintf (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all-md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  Formatiert und speichert eine Folge von Zeichen und Werten im Ausgabeparameter vom Zeichenfolgendatentyp. Jedes Formatierungsargument wird dabei durch das entsprechende Argument ersetzt.  
  
 ![Themenlinksymbol](../../database-engine/configure-windows/media/topic-link.gif "Topic link icon") [Transact-SQL Syntax Conventions (Transact-SQL-Syntaxkonventionen)](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
  
xp_sprintf { string OUTPUT , format }  
     [ , argument [ ,...n ] ]  
```  
  
## <a name="arguments"></a>Argumente  
 *Zeichenfolge*  
 Eine **varchar** -Variable für die Ausgabe.  
  
 OUTPUT  
 Wenn dieser Parameter angegeben wird, wird der Wert der Variablen in den Ausgabeparameter gesetzt.  
  
 *format*  
 Eine Formatierungszeichenfolge mit Platzhaltern für *argument* -Werte, ähnlich wie bei der **sprintf** -Funktion der Programmiersprache C. Derzeit wird nur das %s-Formatierungsargument unterstützt.  
  
 *argument*  
 Eine Zeichenfolge, die den Wert des entsprechenden Formatierungsarguments darstellt.  
  
 *n*  
 Ein Platzhalter, der anzeigt, dass bis zu 50 Argumente angegeben werden können.  
  
## <a name="return-code-values"></a>Rückgabecodewerte  
 0 (Erfolg) oder 1 (Fehler)  
  
## <a name="result-sets"></a>Resultsets  
 **xp_sprintf** gibt die folgende Nachricht zurück:  
  
 `The command(s) completed successfully.`  
  
## <a name="permissions"></a>Berechtigungen  
 Erfordert die Mitgliedschaft in der **public** -Rolle.  
  
## <a name="see-also"></a>Siehe auch  
 [Gespeicherte Systemprozeduren &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)   
 [Gespeicherte allgemeine erweiterte Prozeduren &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/general-extended-stored-procedures-transact-sql.md)   
 [Xp_sscanf &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/xp-sscanf-transact-sql.md)  
  
  
