---
title: Anhang - 1 (DB2ToSQL) | Microsoft Docs
ms.prod: sql-non-specified
ms.prod_service: sql-tools
ms.service: ''
ms.component: ssma-db2
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.technology:
- sql-ssma
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Azure SQL Database
- SQL Server
ms.assetid: c6a30367-d56f-4fcc-8920-c6a6b0335a67
caps.latest.revision: 6
author: Shamikg
ms.author: Shamikg
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 2e06f1f7e7152bb65f6c6625c87ad3fdb7542ac7
ms.sourcegitcommit: 9351e8b7b68f599a95fb8e76930ab886db737e5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/06/2018
---
# <a name="appendix---1-db2tosql"></a>Anhang - 1 (DB2ToSQL)
Kurze Übersicht über die Befehlszeilenoptionen SSMA-Konsole:  
  
|Sl. Nein.|Schalter|Erforderlich?|Switch-Argument|Zulässige Werte|  
|-----------|----------|-------------|-------------------|--------------------|  
|1|-s/script|ja|scriptfile|XML-Dateiname ist ungültig.<br /><br />-Konsole Definition Skriptdatei an.|  
|2|-V-variable|nein|variablevaluefile|XML-Dateiname ist ungültig.<br /><br />Wenn Variablen in einer Skriptdatei verwendet werden, muss diese Datei angegeben werden.|  
|3|-c/serverconnection|nein|serverconnectionfile|XML-Dateiname ist ungültig.<br /><br />Diese Datei enthält Informationen zur Serververbindung.|  
|4|-x/xmloutput|nein|xmloutputfile|Diese Option gibt die Konsolenausgabe in das XML-Format an. Wenn diese Option nicht angegeben ist, wird die standardmäßigen Ausgabe im Textformat.<br /><br />Wenn Xmloutputfile nicht angegeben ist, wird die XML-Ausgabe an "stdout" umgeleitet.<br /><br />Xmloutputfile ist der Name der Datei, die in die Konsolenausgabe in das XML-Format geschrieben wird.|  
|5|-l/log|nein|logfile|Der Dateiname ist ungültig.|  
|6|-e/projectenvironment|nein|projectenvironmentfolder|Gültigen Ordnernamen an, die Dateien der SSMA-Projekt enthält.|  
|7|-p/securepassword|nein|-a/hinzufügen {< Server_id > [,... n] &#124; alle} – C&#124;Serverconnection < Server-Verbindungsdatei > [-V&#124;Variable < Variable-Wert-Datei >] [-o/overwrite]<br /><br />oder<br /><br />-a/add {<server_id> [,…n] &#124; all} –s&#124;script <script-file> [-v&#124;variable <variable-value-file>] [-o/overwrite]<br /><br />–r/remove {<server_id> [, …n] &#124; all}<br /><br />-l/list<br /><br />–e/export {<server-id> [, …n] &#124; all} <encrypted-password -file><br /><br />–i/import {<server-id> [, …n] &#124; all} <encrypted-password-file>|Wenn angegeben, muss diese Option nicht mit anderen Optionen kombiniert werden.<br /><br />Server-Id: eine eindeutige ID für einen Server {String} bereitgestellt<br /><br />Server-Verbindungsdatei: Server-Definitionsdatei (Serverconnectionfile oder Scriptfile).<br /><br />Variable-Wert-Datei: Es ist eine Variablendefinition-Datei und in Server-Verbindungsdatei verwendet.<br /><br />verschlüsselt ein Kennwort – Datei: eine Datei mit Servern Kennwörter verschlüsselt mit einer Passphrase Benutzer angegeben ist.|  
|8|-?|nein|Nicht zutreffend|Nicht zutreffend|  
  
## <a name="see-also"></a>Siehe auch  
[Executing the SSMA Console (Ausführen der SSMA-Konsole)](http://msdn.microsoft.com/en-us/ce63f633-067d-4f04-b8e9-e1abd7ec740b)  
  
