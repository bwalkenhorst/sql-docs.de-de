---
title: '&lt;&gt; (ungleich) (Transact-SQL) | Microsoft-Dokumentation'
ms.custom: 
ms.date: 03/13/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.service: 
ms.component: t-sql|language-elements
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- <>
- <>_TSQL
- Not Equal To
- Not Equal
- <>(Not Equal To)
- NOT
- Equal
dev_langs:
- TSQL
helpviewer_keywords:
- not equal to operator (<>)
- <> (not equal to operator)
ms.assetid: 34cf9b38-d589-4be9-925a-116e224609a0
caps.latest.revision: 
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: Active
ms.openlocfilehash: ffacad3e57cd9c9ab1331e0dbe52335ae1d6ddf1
ms.sourcegitcommit: 9e6a029456f4a8daddb396bc45d7874a43a47b45
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2018
---
# <a name="not-equal-to-transact-sql---traditional"></a>Ungleich (Transact SQL) – Standard
[!INCLUDE[tsql-appliesto-ss2008-all-md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  Vergleicht zwei Ausdrücke (ein Vergleichsoperator). Beim Vergleich von Ausdrücken, die ungleich NULL sind, ist das Ergebnis TRUE, wenn der linke Operand einen anderen Wert als der rechte Operand besitzt; andernfalls ist das Ergebnis FALSE. Wenn einer der Operanden oder beide Operanden NULL sind, finden Sie weitere Informationen unter [SET ANSI_NULLS &#40;Transact-SQL&#41;](../../t-sql/statements/set-ansi-nulls-transact-sql.md).  
  
 ![Themenlinksymbol](../../database-engine/configure-windows/media/topic-link.gif "Topic link icon") [Transact-SQL Syntax Conventions (Transact-SQL-Syntaxkonventionen)](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
expression <> expression  
```  
  
## <a name="arguments"></a>Argumente  
 *expression*  
 Ein gültiger [Ausdruck](../../t-sql/language-elements/expressions-transact-sql.md). Beide Ausdrücke müssen implizit konvertierbare Datentypen besitzen. Die Konvertierung hängt von den [Rangfolgeregeln für Datentypen](../../t-sql/data-types/data-type-precedence-transact-sql.md) ab.  
  
## <a name="result-types"></a>Ergebnistypen  
 **Boolean**  
  
## <a name="examples"></a>Beispiele  
  
### <a name="a-using--in-a-simple-query"></a>A. Verwenden von <> in einer einfachen Abfrage  
 Im folgenden Beispiel werden alle Zeilen in der `Production.ProductCategory`-Tabelle zurückgegeben, die in `ProductCategoryID` über keinen Wert gleich 3 oder 2 verfügen.  
  
```  
-- Uses AdventureWorks  
  
SELECT ProductCategoryID, Name  
FROM Production.ProductCategory  
WHERE ProductCategoryID <> 3 AND ProductCategoryID <> 2;  
  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
```  
ProductCategoryID Name  
----------------- --------------------------------------------------  
1                 Bikes  
4                 Accessories  
  
(2 row(s) affected)  
  
```  
  
## <a name="see-also"></a>Weitere Informationen finden Sie unter  
 [Datentypen &#40;Transact-SQL&#41;](../../t-sql/data-types/data-types-transact-sql.md)   
 [Operatoren &#40;Transact-SQL&#41;](../../t-sql/language-elements/operators-transact-sql.md)   
 [Comparison Operators &#40;Transact-SQL&#41; (Vergleichsoperatoren (Transact-SQL))](../../t-sql/language-elements/comparison-operators-transact-sql.md)  
  
  
