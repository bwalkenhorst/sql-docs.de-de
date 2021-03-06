---
title: Entwickeln mit ADOMD.NET | Microsoft Docs
ms.custom: 
ms.date: 02/14/2018
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.service: 
ms.component: 
ms.reviewer: 
ms.suite: pro-bi
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: reference
applies_to:
- SQL Server 2016 Preview
helpviewer_keywords:
- ADOMD.NET
ms.assetid: abaf33aa-db55-43bf-8f30-15547559be1d
caps.latest.revision: 
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: 67251d077156d608e249ec44125002bc7cc3cda9
ms.sourcegitcommit: 7519508d97f095afe3c1cd85cf09a13c9eed345f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2018
---
# <a name="developing-with-adomdnet"></a>Entwickeln mit ADOMD.NET
  ADOMD.NET ist ein [!INCLUDE[msCoName](../../../includes/msconame-md.md)] .NET Framework-Datenanbieter, die entwickelt wurde, für die Kommunikation mit [!INCLUDE[msCoName](../../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../../../includes/ssasnoversion-md.md)]. ADOMD.NET verwendet das XML for Analysis-Protokoll für die Kommunikation mit analytischen Datenquellen, indem entweder TCP/IP- oder HTTP-Verbindungen für die Übertragung oder den Empfang von SOAP-Anforderungen oder -Antworten eingesetzt werden, die mit der XML for Analysis-Spezifikation kompatibel sind. Befehle können in Multidimensional Expressions (MDX), Data Mining Extensions (DMX), Analysis Services Scripting Language (ASSL) oder gar einer eingeschränkten SQL-Syntax gesendet werden und geben möglicherweise kein Ergebnis zurück. Analytische Daten, Key Performance Indicators (KPIs) und Miningmodelle können über das ADOMD.NET-Objektmodell abgefragt und geändert werden. Über ADOMD.NET können Sie darüber hinaus Metadaten einsehen oder mit diesen arbeiten, indem entweder OLE DB-kompatible Schemarowsets abgerufen werden oder das ADOMD.NET-Objektmodell verwendet wird.  
  
 Der ADOMD.NET-Datenanbieter wird durch den **Microsoft.AnalysisServices.AdomdClient** -Namespace dargestellt.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
  
|Thema|Description|  
|-----------|-----------------|  
|[ADOMD.NET-Clientprogrammierung](../../../analysis-services/multidimensional-models-adomd-net-client/adomd-net-client-programming.md)|Beschreibt, wie ADOMD.NET-Clientobjekte verwendet werden, um Daten und Metadaten von analytischen Datenquellen abzurufen.|  
|[ADOMD.NET-Serverprogrammierung](../../../analysis-services/multidimensional-models-adomd-net-server/adomd-net-server-programming.md)|Beschreibt, wie ADOMD.NET-Serverobjekte verwendet werden, um gespeicherte Prozeduren und benutzerdefinierte Funktionen zu erstellen.|  
|[Neuverteilen von ADOMD.NET](../../../analysis-services/multidimensional-models/adomd-net/redistributing-adomd-net.md)|Beschreibt den Prozess der Neuverteilung von ADOMD.NET.|  
|<xref:Microsoft.AnalysisServices.AdomdClient>|Listet die Objekte auf, die im **Microsoft.AnalysisServices.AdomdClient** -Namespace enthalten sind.|  
  
## <a name="see-also"></a>Siehe auch  
 [Mehrdimensionale Ausdrücke &#40; MDX &#41; Referenz](../../../mdx/multidimensional-expressions-mdx-reference.md)   
 [Datamining-Erweiterungen &#40; DMX &#41; Referenz](../../../dmx/data-mining-extensions-dmx-reference.md)   
 [Analysis Services-Schemarowsets](../../../analysis-services/schema-rowsets/analysis-services-schema-rowsets.md)   
 [Entwickeln mit Analysis Services Scripting Language &#40; ASSL &#41;](../../../analysis-services/multidimensional-models/scripting-language-assl/developing-with-analysis-services-scripting-language-assl.md)   
 [Datenzugriff auf mehrdimensionale Modelle &#40; Analysis Services – mehrdimensionale Daten &#41;](../../../analysis-services/multidimensional-models/mdx/multidimensional-model-data-access-analysis-services-multidimensional-data.md)  
  
  
