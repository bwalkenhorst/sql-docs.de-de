---
title: Numerische Funktionen (Visual FoxPro-ODBC-Treiber) | Microsoft Docs
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
- ODBC numeric functions [ODBC]
- Visual FoxPro ODBC driver [ODBC], numeric functions
- numeric functions [ODBC]
- FoxPro ODBC driver [ODBC], numeric functions
ms.assetid: 7caab48e-cbb5-4bbc-a09b-5cf902e5bc45
caps.latest.revision: 8
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 91c5e11ea258dc70b6d527259bf938119317861e
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="numeric-functions-visual-foxpro-odbc-driver"></a>Numerische Funktionen (Visual FoxPro-ODBC-Treiber)
Die folgende Tabelle beschreibt die numerische ODBC-Funktionen von der Visual FoxPro-ODBC-Treiber unterstützt; Wenn die Visual FoxPro-Grammatik für dieselbe Funktion aus der ODBC-Syntax unterscheidet, wird der entsprechende Visual FoxPro aufgeführt.  
  
|ODBC-Grammatik|Visual FoxPro-Grammatik|  
|------------------|---------------------------|  
|ABS *(Numeric_exp)*||  
|ACOS *(Float_exp)*||  
|ASIN *(Float_exp)*||  
|ATAN *(Float_exp)*||  
|Atan2 *(float_exp1 float_exp2)*|ATN2 (*float_exp1 float_exp2*)|  
|CEILING- *(Numeric_exp)*||  
|COS *(Float_exp)*||  
|COT *(Float_exp)*||  
|Grad *(Numeric_exp)*|RTOD *(Numeric_exp)*|  
|EXP *(Float_exp)*||  
|FLOOR *(Numeric_exp)*||  
|Protokoll *(Float_exp)*||  
|Log10 *(Float_exp)*||  
|MOD *(integer_exp1 integer_exp2)*||  
|PI *)*||  
|BOGENMAß *(Numeric_exp)*|DTOR *(Numeric_exp)*|  
|RAND *([Integer_exp])*||  
|ROUND *(Numeric_exp Integer_exp)*||  
|Anmeldung *(Numeric_exp)*||  
|SIN *(Float_exp)*||  
|SQRT *(Float_exp)*||  
|TAN *(Float_exp)*||  
  
 Die folgenden numerischen Funktionen werden nicht unterstützt:  
  
 POWER *(Numeric_exp Integer_exp)*  
  
 TRUNCATE *(Numeric_exp Integer_exp)*
