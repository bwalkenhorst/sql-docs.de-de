---
title: MSqreader_agents (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.service: ''
ms.component: system-tables
ms.reviewer: ''
ms.suite: sql
ms.technology:
- replication
ms.tgt_pltfrm: ''
ms.topic: language-reference
applies_to:
- SQL Server
f1_keywords:
- MSqreader_agents_TSQL
- MSqreader_agents
dev_langs:
- TSQL
helpviewer_keywords:
- MSqreader_agents system table
ms.assetid: dfa1f45e-c531-4385-a097-0a9edd1d7eab
caps.latest.revision: 28
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 5eb1b2dc7fee99982131c0abeae250b403c50786
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="msqreaderagents-transact-sql"></a>MSqreader_agents (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Die **MSqreader_agents** -Tabelle enthält eine Zeile für jede auf dem lokalen Verteiler ausgeführten Warteschlangenlese-Agent. Diese Tabelle wird in der Verteilungsdatenbank gespeichert.  
  
|Spaltenname|Datentyp|Description|  
|-----------------|---------------|-----------------|  
|**id**|**int**|Die ID des Warteschlangenlese-Agents.|  
|**name**|**Nvarchar(100)**|Der Name des Warteschlangenlese-Agents.|  
|**job_id**|**Binary(16)**|Die eindeutige Auftrags-ID-Nummer aus **Sysjobs** Tabelle.|  
|**profile_id**|**int**|Die Profil-ID aus der **MSagent_profiles** Tabelle.|  
|**job_step_uid**|**uniqueidentifier**|Die eindeutige ID des Auftragsschritts des [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Agents, in dem der Agent gestartet wird.|  
  
## <a name="see-also"></a>Siehe auch  
 [Replikationstabellen &#40;Transact-SQL&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
