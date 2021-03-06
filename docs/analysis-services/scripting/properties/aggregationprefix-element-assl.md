---
title: AggregationPrefix-Element (ASSL) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.service: ''
ms.component: ''
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- AggregationPrefix Element
apilocation:
- http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to:
- SQL Server 2016 Preview
f1_keywords:
- AggregationPrefix
helpviewer_keywords:
- AggregationPrefix element
ms.assetid: 1581e0df-ae8e-41ce-9c92-f0f7cac487f2
caps.latest.revision: 36
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: adfde1b3c3f7b02407181f3123cd9ba708493c7c
ms.sourcegitcommit: f486d12078a45c87b0fcf52270b904ca7b0c7fc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2018
---
# <a name="aggregationprefix-element-assl"></a>AggregationPrefix-Element (ASSL)
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]Definiert das gemeinsame Präfix, das für Aggregationsnamen innerhalb des zugeordneten übergeordneten Elements verwendet werden.  
  
## <a name="syntax"></a>Syntax  
  
```xml  
  
<Cube> <!-- or Database, MeasureGroup, Partition -->  
   ...  
   <AggregationPrefix>...</AggregationPrefix>  
   ...  
</Database>  
```  
  
## <a name="element-characteristics"></a>Elementmerkmale  
  
|Merkmal|Description|  
|--------------------|-----------------|  
|Datentyp und -länge|Zeichenfolge|  
|Standardwert|InclusionThresholdSetting|  
|Cardinality|0-1: Optionales Element, das nur einmal auftreten kann.|  
  
## <a name="element-relationships"></a>Elementbeziehungen  
  
|Beziehung|Element|  
|------------------|-------------|  
|Übergeordnete Elemente|[Cube](../../../analysis-services/scripting/objects/cube-element-assl.md), [Datenbank](../../../analysis-services/scripting/objects/database-element-assl.md), [MeasureGroup](../../../analysis-services/scripting/objects/measuregroup-element-assl.md), [Partition](../../../analysis-services/scripting/objects/partition-element-assl.md)|  
|Untergeordnete Elemente|InclusionThresholdSetting|  
  
## <a name="remarks"></a>Hinweise  
 Aggregationspräfixe generieren Aggregationsnamen in [!INCLUDE[msCoName](../../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../../../includes/ssasnoversion-md.md)], und generieren zusätzlich Tabellennamen in der relationalen Datenbank für Aggregationen, die in einer Partition, relationale OLAP (ROLAP) gespeichert.  
  
 Ein voll erweiterter Aggregationsname setzt sich aus folgenden Teilen zusammen:  
  
 *\<DatabasePrefix >\<CubePrefix >\<MeasureGroupPrefix >\<PartitionPrefix >\<AggregationID >*  
  
 Die ersten vier Teile des Aggregationsnamens bilden das Aggregationspräfix. Der Benutzer stellt die ersten vier Teile bereit:  
  
-   *DatabasePrefix* stellt den Wert des einem **AggregationPrefix** -Element zugeordneten **Database** -Elements dar.  
  
-   *CubePrefix* stellt den Wert des einem **AggregationPrefix** -Element zugeordneten **Cube** -Elements dar.  
  
-   *MeasureGroupPrefix* stellt den Wert des einem **AggregationPrefix** -Element zugeordneten **MeasureGroup** -Elements dar.  
  
-   *PartitionPrefix* stellt den Wert des einem **AggregationPrefix** -Element zugeordneten **Partition** -Elements dar.  
  
 Der fünfte Teil des Namens, *AggregationID*, ist eine systemdefinierte ID. Benutzer haben keinen Einfluss auf diesen Teil des Namens.  
  
 Die Elemente, die den übergeordneten Elementen von entsprechen **AggregationPrefix** im Objektmodell von Analysis Management Objects (AMO) sind <xref:Microsoft.AnalysisServices.Cube>, <xref:Microsoft.AnalysisServices.Database>, <xref:Microsoft.AnalysisServices.MeasureGroup>, und <xref:Microsoft.AnalysisServices.Partition>.  
  
## <a name="see-also"></a>Siehe auch  
 [Datenbankeigenschaften &#40; ASSL &#41;](../../../analysis-services/scripting/properties/properties-assl.md)  
  
  
