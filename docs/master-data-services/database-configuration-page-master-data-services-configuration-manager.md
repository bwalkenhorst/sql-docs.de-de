---
title: Seite "Konfiguration" (Master Data Services-Konfigurations-Manager)-Datenbank | Microsoft Docs
ms.custom: 
ms.date: 03/20/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- master-data-services
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- sql13.mds.configmanager.dbpg.f1
ms.assetid: dd72220e-a599-465d-8b84-9bb6a7433216
caps.latest.revision: 8
author: sabotta
ms.author: carlasab
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: 212031f92de47da41ad2716b81740c6a42487e59
ms.contentlocale: de-de
ms.lasthandoff: 08/02/2017

---
# <a name="database-configuration-page-master-data-services-configuration-manager"></a>Datenbankkonfiguration (Seite im Konfigurations-Manager für Master Data Services)
  Verwenden Sie die Seite **Datenbankkonfiguration** , um Systemeinstellungen einer [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank zu bearbeiten. Systemeinstellungen wirken sich auf alle Webanwendungen und Webdienste aus, die der ausgewählten [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank zugewiesen sind. Sie müssen eine [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank auswählen oder erstellen, damit Systemeinstellungen aktiviert und zur Konfiguration verfügbar sind.  
  
## <a name="current-database"></a>Aktuelle Datenbank  
 Wählen Sie eine vorhandene [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank aus, oder erstellen Sie eine neue Datenbank, deren Systemeinstellungen Sie bearbeiten. Die neue Datenbank ist nach der Erstellung ausgewählt.  
  
|Steuerelementname|Description|  
|------------------|-----------------|  
|**SQL Server-Instanz**|Zeigt den Namen der ausgewählten [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] -Instanz an. Dieses Feld bleibt so lange leer, bis Sie eine Verbindung mit einer Instanz herstellen und dann eine [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank auswählen oder erstellen.|  
|**Master Data Services-Datenbank**|Zeigt den Namen der ausgewählten [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank an. Dieses Feld bleibt so lange leer, bis Sie eine Verbindung mit einer Instanz herstellen und dann eine [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank auswählen oder erstellen.|  
|**Master Data Services-Datenbankversion**|Die Version des [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbankschemas.|  
|**Datenbank erstellen**|Öffnet den Assistenten **Datenbank erstellen** , von dem aus Sie eine Verbindung mit einer [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] -Instanz herstellen und eine [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank für diese Instanz erstellen.|  
|**Datenbank auswählen**|Öffnet das Dialogfeld **Verbindung mit Datenbank herstellen** , in dem Sie eine Verbindung mit einer [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] -Instanz herstellen und eine [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank auswählen.|  
|**Datenbank aktualisieren**|Öffnet einen Assistenten, in dem Sie eine angegebene [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank aktualisieren können. Diese Schaltfläche ist nur aktiviert, wenn die angegebene Datenbank ein Upgrade erfordert.|  
|**Reparieren der Datenbank**|Klicken Sie auf diese Schaltfläche, um sicherzustellen, dass die MDS-Datenbank ordnungsgemäß installiert ist. Dies kann nützlich sein, wenn Sie eine MDS-Datenbank in einer [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] -Instanz sichern und wiederherstellen, die nie eine MDS-Datenbank gehostet hat.|  
  
## <a name="system-settings"></a>Systemeinstellungen  
 Bearbeiten Sie Systemeinstellungen für alle Webanwendungen und Webdienste, die der ausgewählten [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank zugeordnet sind.  
  
 Diese Einstellungen sind in [!INCLUDE[ssMDScfgmgr](../includes/ssmdscfgmgr-md.md)] verfügbar und werden in der Datenbank in der Tabelle Systemeinstellungen (mdm.tblSystemSetting) gespeichert. Eine Liste mit allen Einstellungen finden Sie unter [Systemeinstellungen &#40;Master Data Services&#41;](../master-data-services/system-settings-master-data-services.md).  
  
## <a name="see-also"></a>Siehe auch  
[Master Data Services-Installation und Konfiguration](../master-data-services/master-data-services-installation-and-configuration.md) [Datenbank Anforderungen &#40; Master Data Services &#41;](../master-data-services/install-windows/database-requirements-master-data-services.md)  
  
  