---
title: "Verwenden von SQL Server Profiler zum Überwachen von Analysis Services | Microsoft Docs"
ms.custom: 
ms.date: 01/23/2018
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
- SQL Server Profiler, Analysis Services
- monitoring Analysis Services [SQL Server]
- performance [Analysis Services], SQL Server Profiler
- Profiler [SQL Server Profiler], Analysis Services
ms.assetid: 8b77dafc-4584-4e93-8ad7-299304391bfd
caps.latest.revision: 
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: On Demand
ms.openlocfilehash: 736b5de1af85d3143e8b258de0a3b388e5d2ea01
ms.sourcegitcommit: 7519508d97f095afe3c1cd85cf09a13c9eed345f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2018
---
# <a name="use-sql-server-profiler-to-monitor-analysis-services"></a>Verwenden von SQL Server Profiler zum Überwachen von Analysis Services
[!INCLUDE[ssas-appliesto-sqlas-all-aas](../../includes/ssas-appliesto-sqlas-all-aas.md)]

  [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] verfolgt Modulprozessereignisse wie das Starten eines Batches oder einer Transaktion und erfasst Daten zu diesen Ereignissen. So können Sie die Server- und Datenbankaktivität überwachen (z.B. Benutzerabfragen oder Anmeldeaktivität). Sie können [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] -Daten in einer [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] -Tabelle oder -Datei aufzeichnen und später analysieren oder die aufgezeichneten Ereignisse in der gleichen oder einer anderen [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] -Instanz wiedergeben, um den genauen Ablauf anzuzeigen. Ereignisse können in Echtzeit oder schrittweise wiedergegeben werden. Sehr hilfreich ist es auch, die Ablaufverfolgungsereignisse zusammen mit den Leistungsindikatoren auf dem gleichen Computer auszuführen. Der Profiler kann diese auf der Grundlage von Zeit korrelieren und gemeinsam in einer einzelnen Zeitskala anzeigen. Ablaufverfolgungsereignisse bieten Ihnen mehr Details, während Leistungsindikatoren eine Aggregatsicht liefern. Informationen zum Erstellen und Ausführen von Ablaufverfolgungen finden Sie unter [Erstellen von Profilerablaufverfolgungen für Replay &#40;Analysis Services&#41;](../../analysis-services/instances/create-profiler-traces-for-replay-analysis-services.md).  
  
 In der folgenden Tabelle werden die Themen in diesem Abschnitt beschrieben.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
  
|Thema|Description|  
|-----------|-----------------|  
|[Einführung in die Überwachung von Analysis Services mit SQL Server Profiler](../../analysis-services/instances/introduction-to-monitoring-analysis-services-with-sql-server-profiler.md)|Beschreibt das Verwenden von [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] zum Überwachen einer [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] -Instanz.|  
|[Erstellen von Profilerablaufverfolgungen für Replay &#40;Analysis Services&#41;](../../analysis-services/instances/create-profiler-traces-for-replay-analysis-services.md)|Beschreibt die Anforderungen für das Erstellen einer Ablaufverfolgung zur Wiedergabe mithilfe von [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)].|  
|[Analysis Services-Ablaufverfolgungsereignisse](../../analysis-services/trace-events/analysis-services-trace-events.md)|Beschreibt [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] -Ereignisklassen. Diese Ereignisklassen sind Aktionen zugeordnet, die von [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] generiert werden, und werden zum Wiedergeben von Ablaufverfolgungen verwendet.|  
  
## <a name="see-also"></a>Siehe auch  
 [Überwachen einer Instanz von Analysis Services](../../analysis-services/instances/monitor-an-analysis-services-instance.md)  
  
  
