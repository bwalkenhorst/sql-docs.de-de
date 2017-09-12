---
title: Geben Sie als Datumstabelle markieren | Microsoft Docs
ms.custom: 
ms.date: 03/01/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
- analysis-services/multidimensional-tabular
- analysis-services/data-mining
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 30841d1f-0c3b-4575-8f4a-27a1492e248c
caps.latest.revision: 5
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: c23ab7153ce90c55c9858dde6a0f0083bc92def7
ms.contentlocale: de-de
ms.lasthandoff: 09/01/2017

---
# <a name="specify-mark-as-date-table-for-use-with-time-intelligence"></a>Geben Sie für die Verwendung mit Zeitintelligenz markieren als Date-Tabelle
  Um die Verwendung von zeitintelligenzfunktionen in DAX-Formeln verwenden, müssen Sie eine Datumstabelle und eine eindeutige Bezeichnerspalte (Datetime) des Date-Datentyps angeben. Sobald eine Spalte in der Datumstabelle als eindeutiger Bezeichner angegeben wird, können Sie Beziehungen zwischen Spalten in der Datumstabelle und beliebigen Faktentabellen erstellen.  
  
 Wenn Sie zeitintelligenzfunktionen verwenden, gelten die folgenden Regeln:  
  
-   Geben Sie bei Verwendung von DAX-zeitintelligenzfunktionen niemals eine Datetime-Spalte aus einer Faktentabelle. Erstellen Sie im Modell immer eine separate Datumstabelle, die mindestens eine datetime-Spalte des Date-Datentyps mit eindeutigen Werten enthält.  
  
-   Stellen Sie sicher, dass die Datumstabelle über einen fortlaufenden Datumsbereich verfügt.  
  
-   Die datetime-Spalte in der Datumstabelle sollte Tagesgranularität (ohne Unterteilung der Tage) aufweisen.  
  
-   Sie müssen eine Datumstabelle und eine eindeutige Bezeichnerspalte im Dialogfeld **Als Datumstabelle markieren** angeben.  
  
-   Erstellen Sie Beziehungen zwischen Faktentabellen und Spalten des Date-Datentyps in der Datumstabelle.  
  
#### <a name="to-specify-a-date-table-and-unique-identifier"></a>So geben Sie eine Datumstabelle und einen eindeutigen Bezeichner an  
  
1.  Klicken Sie im Modell-Designer auf die Datumstabelle.  
  
2.  Klicken Sie im Menü **Tabelle** auf **Datum**, und klicken Sie dann auf **Als Datumstabelle markieren**  
  
3.  Wählen Sie im Dialogfeld **Als Datumstabelle markieren** im Listenfeld **Datum** eine Spalte aus, die als eindeutiger Bezeichner verwendet wird. Diese Spalte muss eindeutige Werte enthalten und sollte den Date-Datentyp aufweisen. Beispiel:  
  
    |Datum|  
    |----------|  
    |7/1/2010 12:00:00 AM|  
    |7/2/2010 12:00:00 AM|  
    |7/3/2010 12:00:00 AM|  
    |7/4/2010 12:00:00 AM|  
    |7/5/2010 12:00:00 AM|  
  
4.  Erstellen Sie ggf. Beziehungen zwischen Faktentabellen und der Datumstabelle.  
  
## <a name="see-also"></a>Siehe auch  
 [Berechnungen](../../analysis-services/tabular-models/calculations-ssas-tabular.md)   
 [Zeitintelligenzfunktionen (DAX)](http://msdn.microsoft.com/en-us/91df278d-4b28-40c1-a572-cdb91f081517)  
  
  