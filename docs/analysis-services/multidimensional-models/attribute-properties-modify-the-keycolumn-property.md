---
title: "Ändern der KeyColumns-Eigenschaft eines Attributs | Microsoft Docs"
ms.custom: 
ms.date: 03/01/2017
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.service: 
ms.component: data-mining
ms.reviewer: 
ms.suite: pro-bi
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- binding attributes [Analysis Services]
- attributes [Analysis Services], binding
- key columns [Analysis Services]
ms.assetid: a2643be4-8123-4cc3-baf9-e5ec54a1669d
caps.latest.revision: 
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: e745159dbb8a8e329ad5cbdee64831ce284439c8
ms.sourcegitcommit: 7519508d97f095afe3c1cd85cf09a13c9eed345f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2018
---
# <a name="attribute-properties---modify-the-keycolumn-property"></a>Attributeigenschaften – Ändern der KeyColumns-Eigenschaft
[!INCLUDE[ssas-appliesto-sqlas](../../includes/ssas-appliesto-sqlas.md)]
Sie können die **KeyColumns** -Eigenschaft eines Attributs ändern. Nehmen wir beispielsweise an, Sie möchten einen zusammengesetzten Schlüssel statt eines einzelnen Schlüssels für das Attribut verwenden.  
  
### <a name="to-modify-the-keycolumns-property-of-an-attribute"></a>So ändern Sie die KeyColumns-Eigenschaft eines Attributs  
  
1.  Öffnen Sie in [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)]das Projekt, in dem Sie die **KeyColumns** -Eigenschaft ändern möchten.  
  
2.  Öffnen Sie den Dimensions-Designer, indem Sie eine der folgenden Aktionen ausführen:  
  
    -   Klicken Sie im **Projektmappen-Explorer**im Ordner **Dimensionen** mit der rechten Maustaste auf die Dimension, und klicken Sie anschließend entweder auf **Öffnen** oder **Sicht-Designer**.  
  
         – oder –  
  
    -   Im Cube-Designer auf die **Cubestruktur** Registerkarte, erweitern Sie die Cubedimension in der **Dimensionen** Bereich, und klicken Sie auf **bearbeiten \<Dimension >**.  
  
3.  Klicken Sie im Bereich **Attribute** der Registerkarte **Dimensionsstruktur** auf das Attribut, dessen **KeyColumns** -Eigenschaft Sie ändern möchten.  
  
4.  Klicken Sie im Fenster **Eigenschaften** auf den Wert für die **KeyColumns** -Eigenschaft.  
  
5.  Klicken Sie auf die Schaltfläche zum Durchsuchen **(...)** , die in der Wertzelle des Eigenschaftenfelds angezeigt wird.  
  
     Das Dialogfeld **Schlüsselspalten** wird geöffnet.  
  
6.  Um eine vorhandene Schlüsselspalte zu entfernen, wählen Sie die Spalte in der Liste **Schlüsselspalten** aus, und klicken Sie anschließend auf die Schaltfläche **\<** .  
  
7.  Um eine Schlüsselspalte hinzuzufügen, wählen Sie die Spalte in der Liste **Verfügbare Spalten** aus, und klicken Sie anschließend auf die Schaltfläche **>** .  
  
    > [!NOTE]  
    >  Wenn Sie mehrere Schlüsselspalten definieren, bestimmt die Reihenfolge, in der diese Spalten in der Liste **Schlüsselspalten** aufgeführt sind, die Anzeigereihenfolge. Beispielsweise verfügt ein Month-Attribut über zwei Schlüsselspalten: Month und Year. Wenn die Year-Spalte in der Liste vor der Month-Spalte steht, sortiert [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] zuerst nach Jahr und dann nach Monat. Wenn die Month-Spalte vor der Year-Spalte steht, sortiert [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] zuerst nach Monat und dann nach Jahr.  
  
8.  Um die Reihenfolge von Schlüsselspalten zu ändern, wählen Sie eine Spalte aus und klicken dann auf die Schaltfläche **Nach oben** oder **Nach unten** .  
  
## <a name="see-also"></a>Siehe auch  
 [Dimensionsattributeigenschaftenverweis](../../analysis-services/multidimensional-models/dimension-attribute-properties-reference.md)  
  
  
