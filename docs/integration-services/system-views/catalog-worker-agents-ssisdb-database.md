---
title: catalog.worker_agents (SSISDB-Datenbank) | Microsoft-Dokumentation
ms.custom: 
ms.date: 12/16/2016
ms.prod: sql-non-specified
ms.prod_service: integration-services
ms.service: 
ms.component: system-views
ms.reviewer: 
ms.suite: sql
ms.technology:
- integration-services
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 0bd0d827-e2f1-44fe-aa90-6bf922d68d16
caps.latest.revision: 
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 5b3d7ae2666a6adc774093a8496863685457e7e6
ms.sourcegitcommit: 9e6a029456f4a8daddb396bc45d7874a43a47b45
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2018
---
# <a name="catalogworkeragents-ssisdb-database"></a>catalog.worker_agents (SSISDB-Datenbank)
[!INCLUDE[tsql-appliesto-ss2016-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2016-xxxx-xxxx-xxx-md.md)]

Zeigt die Informationen für den [!INCLUDE[ssISnoversion](../../includes/ssisnoversion-md.md)] Scale Out-Worker an.

|Spaltenname|Datentyp|Description|  
|-----------------|---------------|-----------------|  
|WorkerAgentId|**uniqueidentifier**|Die Worker-Agent-ID für den Scale Out-Worker.|
|isEnabled|**bit**|Gibt an, ob der Scale Out-Worker aktiviert ist.|
|DisplayName|**nvarchar(256)**|Der Anzeigename des Scale Out-Workers.|
|Description|**nvarchar(256)**|Die Beschreibung des Scale Out-Workers.|
|MachineName|**nvarchar(256)**|Der Computername für den Scale Out-Worker.|
|Tags|**nvarchar(max)**|Die Tags des Scale Out-Workers.|
|UserAccount|**nvarchar(256)**|Das Benutzerkonto, unter dem der Dienst für den Scale Out-Worker ausgeführt wird.|
|LastOnlineTime|**datetimeoffset(7)**|Der letzte Zeitpunkt, zu dem der Scale Out-Worker online war.|

## <a name="remarks"></a>Remarks
In dieser Ansicht wird eine Zeile für jeden Scale Out-Worker angezeigt, der eine Verbindung mit dem Scale Out-Master herstellt, der mit dem SSISDB-Katalog zusammenarbeitet.

## <a name="permissions"></a>Berechtigungen
Diese Sicht erfordert eine der folgenden Berechtigungen:

- Mitgliedschaft in der Datenbankrolle **ssis_admin**

- Mitgliedschaft in der Datenbankrolle **ssis_cluster_executor**

- Mitgliedschaft in der Serverrolle **sysadmin**
