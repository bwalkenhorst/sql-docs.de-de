---
title: Schema-Element (ASSL) | Microsoft Docs
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
- Schema Element
apilocation:
- http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to:
- SQL Server 2016 Preview
f1_keywords:
- Schema
helpviewer_keywords:
- Schema element
ms.assetid: 4b6375fb-7ad8-4d5f-88b1-abd3da2654db
caps.latest.revision: 34
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: f5359475a30fbd0f7caf65eab589b7e64ce3a588
ms.sourcegitcommit: f486d12078a45c87b0fcf52270b904ca7b0c7fc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2018
---
# <a name="schema-element-assl"></a>Schema-Element (ASSL)
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]Enthält das Schema der Datenquellensicht.  
  
## <a name="syntax"></a>Syntax  
  
```xml  
  
<DataSourceView>  
   ...  
   <Schema>...</Schema>  
   ...  
</DataSourceView>  
```  
  
## <a name="element-characteristics"></a>Elementmerkmale  
  
|Merkmal|Description|  
|--------------------|-----------------|  
|Datentyp und -länge|Schema|  
|Standardwert|InclusionThresholdSetting|  
|Cardinality|1-1: Erforderliches Element, das nur einmal auftritt.|  
  
## <a name="element-relationships"></a>Elementbeziehungen  
  
|Beziehung|Element|  
|------------------|-------------|  
|Übergeordnetes Element|[DataSourceView-Objekt](../../../analysis-services/scripting/objects/datasourceview-element-assl.md)|  
|Untergeordnete Elemente|InclusionThresholdSetting|  
  
## <a name="remarks"></a>Remarks  
 Die **Schema** wird dargestellt, mit dem XML-Schemadefinition (XSD) Sprachformat des DataSets in der [!INCLUDE[msCoName](../../../includes/msconame-md.md)] .NET Framework, wobei einige Erweiterungen für DataSets und andere spezifisch für die Verwendung in der Definition Datendefinitionssprache (DDL). DataSets definieren eine flexible Zuordnung von XSD zu einem relationalen Schema, aber geben XSD in einer kanonischeren Form zurück. Nur diese kanonische Form ist innerhalb der Datenquellen gültig.  
  
 Das Element, das das übergeordnete Element des entspricht **Schema** im Objekt Analysis Management Objects (AMO) Modell ist <xref:Microsoft.AnalysisServices.DataSourceView>.  
  
## <a name="see-also"></a>Weitere Informationen finden Sie unter  
 [Datenbankeigenschaften &#40; ASSL &#41;](../../../analysis-services/scripting/properties/properties-assl.md)  
  
  
