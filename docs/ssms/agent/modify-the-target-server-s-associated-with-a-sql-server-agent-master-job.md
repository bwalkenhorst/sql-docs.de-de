---
title: "Ändern des mit dem Masterauftrag des Agents verknüpften Zielservers | Microsoft-Dokumentation"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- tools-ssms
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 176e73b6-08aa-48ec-b349-e84b431e65cc
caps.latest.revision: 5
author: stevestein
ms.author: sstein
manager: jhubbard
ms.translationtype: Human Translation
ms.sourcegitcommit: 2edcce51c6822a89151c3c3c76fbaacb5edd54f4
ms.openlocfilehash: f431174986975cc5b5d6f25c6e9aa89469ee94b4
ms.contentlocale: de-de
ms.lasthandoff: 06/22/2017

---
# <a name="modify-the-target-servers-associated-with-a-sql-server-agent-master-job"></a>Ändern der einem Masterauftrag für den SQL Server-Agent zugewiesenen Zielserver
In diesem Thema wird beschrieben, wie Sie die Zielserver, die einem Masterauftrag für den SQL Server-Agent zugewiesen sind, mithilfe von [!INCLUDE[ssCurrent](../../includes/sscurrent_md.md)] oder [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull_md.md)] in [!INCLUDE[tsql](../../includes/tsql_md.md)]ändern.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Security](#Security)  
  
-   **Ändern der Zielserver, die einem Masterauftrag für den SQL Server-Agent zugewiesen sind, mit:**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Ein Masterauftrag für den [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] -Agent kann nicht gleichzeitig lokale Server und Remoteserver als Ziel haben.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Sie können nur Aufträge ändern, die in Ihrem Besitz sind, es sei denn, Sie sind ein Mitglied der festen Serverrolle **sysadmin** . Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../../ssms/agent/implement-sql-server-agent-security.md).  
  
## <a name="SSMSProcedure"></a>Verwenden von SQL Server Management Studio  
  
#### <a name="to-modify-the-target-servers-associated-with-a-sql-server-agent-master-job"></a>So ändern Sie die Zielserver, die einem Masterauftrag für den SQL Server-Agent zugewiesen sind  
  
1.  Klicken Sie im **Objekt-Explorer** auf das Pluszeichen, um den Server zu erweitern, der den Auftrag mit dem zu ändernden Zielserver enthält.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Aufträge** zu erweitern.  
  
4.  Klicken Sie mit der rechten Maustaste auf den Auftrag, dessen Zielserver Sie ändern möchten, und wählen Sie **Eigenschaften**aus.  
  
5.  Wählen Sie im Dialogfeld **Auftragseigenschaften –***Auftragsname* unter **Seite auswählen** die Option **Ziele** aus. Weitere Informationen zu den verfügbaren Optionen auf dieser Seite finden Sie unter [Auftragseigenschaften – Neuer Auftrag &#40;Seite „Ziele“&#41;](../../ssms/agent/job-properties-new-job-targets-page.md).  
  
6.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Verwenden von Transact-SQL  
  
#### <a name="to-delete-a-target-server-currently-associated-with-a-sql-server-agent-master-job"></a>So löschen Sie einen Zielserver, der derzeit einem Masterauftrag für den SQL Server-Agent zugewiesen ist  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../../includes/ssde_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- removes the server SEATTLE2 from processing the Weekly Sales Backupsjob   
    -- assumes that the Weekly Sales Backups job exists  
    USE msdb ;  
    GO  
  
    EXEC sp_delete_jobserver  
        @job_name = N'Weekly Sales Backups',  
        @server_name = N'SEATTLE2' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [sp_delete_jobserver (Transact-SQL)](http://msdn.microsoft.com/en-us/6d63ed32-68cf-4d8f-aa40-05a3826e05b8).  
  
#### <a name="to-associate-a-target-server-with-the-current-sql-server-agent-master-job"></a>So weisen Sie dem aktuellen Masterauftrag für den SQL Server-Agent einen Zielserver zu  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../../includes/ssde_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- assigns the multiserver job Weekly Sales Backups to the server SEATTLE2   
    -- assumes that the Weekly Sales Backups job already exists and that   
    -- SEATTLE2 is registered as a target server for the current instance  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_add_jobserver  
        @job_name = N'Weekly Sales Backups',  
        @server_name = N'SEATTLE2' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [sp_add_jobserver (Transact-SQL)](http://msdn.microsoft.com/en-us/485252cc-0081-490a-9bd1-cbbd68eea286).  
  
