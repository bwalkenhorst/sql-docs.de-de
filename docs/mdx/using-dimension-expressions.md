---
title: Verwenden von Dimensionsausdrücken | Microsoft Docs
ms.custom: ''
ms.date: 03/02/2016
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.service: ''
ms.component: ''
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: language-reference
dev_langs:
- kbMDX
helpviewer_keywords:
- expressions [MDX], dimensions
- dimensions [Analysis Services], MDX
ms.assetid: 1d40cffb-e88f-4284-93cf-d62ab4f08395
caps.latest.revision: 28
author: Minewiskan
ms.author: owend
manager: erikre
ms.workload: Inactive
ms.openlocfilehash: 1417fd747df92c84fe66e2c69996f57ab51875e1
ms.sourcegitcommit: f486d12078a45c87b0fcf52270b904ca7b0c7fc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2018
---
# <a name="using-dimension-expressions"></a>Verwenden von Dimensionsausdrücken
[!INCLUDE[ssas-appliesto-sqlas](../includes/ssas-appliesto-sqlas.md)]

  Dimensions- und Hierarchieausdrücke werden in MDX (Multidimensional Expressions) üblicherweise zur Übergabe von Parametern an Funktionen verwendet, um Elemente, Mengen oder Tupel einer Hierarchie zurückzugeben.  
  
 Dimensionsausdrücke können nur einfache Ausdrücke sein, da sie Objektbezeichner sind. Finden Sie unter [Ausdrücke &#40; MDX &#41; ](../mdx/expressions-mdx.md) eine Erläuterung der einfachen und komplexen Ausdrücken.  
  
## <a name="dimension-expressions"></a>Dimensionsausdrücke  
 Ein Dimensionsausdruck enthält entweder einen Dimensionsbezeichner oder eine Dimensionsfunktion.  
  
 Dimensionsausdrücke werden selten allein verwendet. Normalerweise wird in einer Dimension eine Hierarchie angegeben. Die einzige Ausnahme bildet die Measures-Dimension, die über keine Hierarchien verfügt.  
  
 Das folgende Beispiel zeigt ein berechnetes Element, das den Ausdruck [Measures] mit den Funktionen .Members und Count() verwendet, um die Anzahl der Elemente in der Measures-Dimension zurückzugeben.  
  
 `WITH MEMBER [Measures].[MeasureCount] AS`  
  
 `COUNT([Measures].MEMBERS)`  
  
 `SELECT [Measures].[MeasureCount] ON 0`  
  
 `FROM [Adventure Works]`  
  
 Ein dimensionsbezeichner wird als *Dimension_Name* in der BNF-Schreibweise zur Beschreibung von MDX-Anweisungen.  
  
## <a name="hierarchy-expressions"></a>Hierarchieausdrücke  
 Ein Hierarchieausdruck enthält entweder einen Hierarchiebezeichner oder eine Hierarchiefunktion. Im folgenden Beispiel wird der Hierarchieausdruck [Date].[Calendar] in Verbindung mit der .Levels- und der .Count-Funktion verwendet, um die Anzahl der Ebenen in der Calendar-Hierarchie der Date-Dimension zurückzugeben:  
  
 `WITH MEMBER [Measures].[CalendarLevelCount] AS`  
  
 `[Date].[Calendar].Levels.Count`  
  
 `SELECT [Measures].[CalendarLevelCount] ON 0`  
  
 `FROM [Adventure Works]`  
  
 Am häufigsten werden Hierarchieausdrücke in Verbindung mit der .Members-Funktion verwendet, um die Anzahl aller Elemente einer Hierarchie zurückzugeben. Im folgenden Beispiel werden alle Elemente von [Date].[Calendar] auf der ROWS-Achse zurückgegeben:  
  
 `SELECT [Measures].[Internet Sales Amount] ON 0,`  
  
 `[Date].[Calendar].MEMBERS ON 1`  
  
 `FROM [Adventure Works]`  
  
 Ein hierarchiebezeichner wird als *Dimension_Name**.* *Hierarchiename* in der BNF-Schreibweise zur Beschreibung von MDX-Anweisungen.  
  
## <a name="see-also"></a>Siehe auch  
 [Ausdrücke &#40; MDX &#41;](../mdx/expressions-mdx.md)  
  
  
