---
title: Angeben des Momentaufnahmeformats (SQL Server Management Studio) | Microsoft Dokumentation
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: replication
ms.reviewer: 
ms.suite: sql
ms.technology:
- replication
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- snapshots [SQL Server replication], formats
- snapshot replication [SQL Server], formats
ms.assetid: 7c95f545-731a-4743-9acb-0b325ef9b98b
caps.latest.revision: 
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: c5bae3f755eaca45f2388a7d855a8c034cc5901a
ms.sourcegitcommit: ab25b08a312d35489a2c4a6a0d29a04bbd90f64d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2018
---
# <a name="specify-snapshot-format-sql-server-management-studio"></a>Angeben des Momentaufnahmeformats (SQL Server Management Studio)
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  Geben Sie das Momentaufnahmeformat auf der Seite **Momentaufnahme** des Dialogfelds **Veröffentlichungseigenschaften - \<Veröffentlichung>** an. Weitere Informationen zum Zugreifen auf dieses Dialogfeld finden Sie unter [View and Modify Publication Properties](../../../relational-databases/replication/publish/view-and-modify-publication-properties.md).  
  
### <a name="to-specify-snapshot-format"></a>So geben Sie das Momentaufnahmeformat an  
  
1.  Wählen Sie auf der Seite **Momentaufnahme** des Dialogfelds **Veröffentlichungseigenschaften - \<Veröffentlichung>** die Option **Natives Format von SQL Server - alle Abonnenten müssen Server mit SQL Server sein** oder **Zeichen - erforderlich, wenn auf einem Verleger oder Abonnenten SQL Server nicht ausgeführt wird** aus.  
  
    > [!NOTE]  
    >  Sie sollten das systemeigene Format auswählen, sofern diese Veröffentlichung keine Abonnements für eine [!INCLUDE[ssEW](../../../includes/ssew-md.md)] -Datenbank und keine Nicht-[!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] -Datenbank unterstützen muss.  
  
2.  [!INCLUDE[clickOK](../../../includes/clickok-md.md)]  
  
## <a name="see-also"></a>Weitere Informationen finden Sie unter  
 [Konfigurieren von Momentaufnahmeeigenschaften &#40;Replikationsprogrammierung mit Transact-SQL&#41;](../../../relational-databases/replication/publish/configure-snapshot-properties-replication-transact-sql-programming.md)   
 [Ändern von Veröffentlichungs- und Artikeleigenschaften](../../../relational-databases/replication/publish/change-publication-and-article-properties.md)   
 [Initialisieren eines Abonnements mit einer Momentaufnahme](../../../relational-databases/replication/initialize-a-subscription-with-a-snapshot.md)  
  
  
