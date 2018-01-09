---
title: Herunterladen und installieren Sie Microsoft SQL Operations Studio (Vorschau) | Microsoft Docs
description: "Herunterladen und installieren Sie Microsoft SQL Operations Studio (Vorschau) für Windows, Mac OS oder Linux"
ms.custom: tools|sos
ms.date: 12/19/2017
ms.prod: sql-non-specified
ms.reviewer: alayu; erickang; sstein
ms.suite: sql
ms.prod_service: sql-tools
ms.component: sos
ms.tgt_pltfrm: 
ms.topic: article
author: stevestein
ms.author: sstein
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 3a34a03b447e26f072b6c8064cd115333600fef4
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="download-and-install-sql-operations-studio-preview"></a>Herunterladen und Installieren von SQL-Vorgänge Studio (Vorschau)

[!INCLUDE[name-sos](../includes/name-sos.md)]auf Windows, Mac OS und Linux ausgeführt wird.

Herunterladen und installieren Sie die neueste Version der *öffentliche Vorschau Dezember*:

|Platform|Herunterladen|Veröffentlichungsdatum|
|:---|:---|:---|
|Windows|[Installationsprogramm](https://go.microsoft.com/fwlink/?linkid=865305)<br>[ZIP](https://go.microsoft.com/fwlink/?linkid=865304)|19 Dezember 2017 |
|MacOS|[ZIP](https://go.microsoft.com/fwlink/?linkid=865306)|19 Dezember 2017 |
|Linux|[.Deb](https://go.microsoft.com/fwlink/?linkid=865308)<br>[entsprechende](https://go.microsoft.com/fwlink/?linkid=865309)<br>[. weswegen](https://go.microsoft.com/fwlink/?linkid=865307)|19 Dezember 2017|

Einzelheiten über die neueste Version finden Sie unter der [Anmerkungen zu dieser Version](release-notes.md).

## <a name="get-sql-operations-studio-preview-for-windows"></a>Abrufen von SQL-Vorgänge Studio (Vorschau) für Windows

Diese Version von [!INCLUDE[name-sos](../includes/name-sos-short.md)] enthält einen standardmäßigen Windows Installer-Umgebung und eine ZIP: 

**Installationsprogramm**

1. Herunterladen und Ausführen der [ [!INCLUDE[name-sos](../includes/name-sos-short.md)] für Windows Installer](https://go.microsoft.com/fwlink/?linkid=865305).
1. Starten Sie den [!INCLUDE[name-sos-short](../includes/name-sos-short.md)] app.


**ZIP-Datei**

1. Herunterladen [ [!INCLUDE[name-sos](../includes/name-sos-short.md)] ZIP für Windows](https://go.microsoft.com/fwlink/?linkid=865304).
2. Rufen Sie die heruntergeladene Datei, und extrahieren Sie es.
3. Ausführen von `\sqlops-windows\sqlops.exe`


## <a name="get-sql-operations-studio-preview-for-macos"></a>Abrufen von SQL-Vorgänge Studio (Vorschau) für macOS

1. Herunterladen [ [!INCLUDE[name-sos](../includes/name-sos-short.md)] für MacOS](https://go.microsoft.com/fwlink/?linkid=865306).
2. Doppelklicken Sie darauf, um den Inhalt der ZIP-Datei zu erweitern.
3. Vornehmen [!INCLUDE[name-sos](../includes/name-sos-short.md)] zur Verfügung, in der *Launchpad*, ziehen Sie *sqlops.app* auf die *Anwendungen* Ordner.


## <a name="get-sql-operations-studio-preview-for-linux"></a>Abrufen von SQL-Vorgänge Studio (Vorschau) für Linux

1. Herunterladen [ [!INCLUDE[name-sos](../includes/name-sos-short.md)] für Linux](https://go.microsoft.com/fwlink/?linkid=865307).
1. Extrahieren Sie die Datei, und starten Sie [!INCLUDE[name-sos](../includes/name-sos-short.md)], öffnen Sie ein neues Terminal-Fenster, und geben Sie die folgenden Befehle:

   ```bash
   cd ~
   cp ~/Downloads/sqlops-linux-<version string>.tar.gz ~
   tar -xvf ~/sqlops-linux-<version string>.tar.gz
   echo 'export PATH="$PATH:~/sqlops-linux-x64"' >> ~/.bashrc
   source ~/.bashrc
   sqlops
   ```

   > [!NOTE]
   > Auf Ubuntu und Redhat müssen Sie möglicherweise fehlenden Abhängigkeiten. Verwenden Sie die folgenden Befehle aus, um diese Abhängigkeiten abhängig von Ihrer Version von Linux zu installieren:
   
   **Ubuntu:** 
   ```bash
   sudo apt-get install libxss1

   sudo apt-get install libgconf-2-4

   sudo apt-get install libunwind8
   ```

   **RedHat:** 
   ```bash
   yum install libXScrnSaver
   ```

## <a name="uninstall-sql-operations-studio-preview"></a>Deinstallieren Sie SQL-Vorgänge Studio (Vorschau)

Wenn Sie installiert [!INCLUDE[name-sos-short](../includes/name-sos-short.md)] mithilfe von Windows Installer, deinstallieren Sie die gleiche Weise wie Sie jede Windows-Anwendung entfernen.

Wenn Sie installiert [!INCLUDE[name-sos-short](../includes/name-sos-short.md)] mit einem ZIP- oder andere Archiv, klicken Sie dann einfach löschen Sie die Dateien.

## <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

[!INCLUDE[name-sos](../includes/name-sos-short.md)]unter Windows, Mac OS und Linux ausgeführt wird, und wird auf folgenden Plattformen unterstützt:

### <a name="windows"></a>Windows
- Windows 10 (64-Bit)
- Windows 8.1 (64-Bit)
- Windows 8 (64-Bit)
- Windows 7 (SP1) (64-Bit) erfordert [KB2533623](https://www.microsoft.com/en-us/download/details.aspx?id=26767)
- Windows Server 2016
- Windows Server 2012 R2 (64-Bit)
- Windows Server 2012 (64-Bit)
- Windows Server 2008 R2 (64-Bit)

### <a name="macos"></a>MacOS
- MacOS 10,13 hohe Sierra
- MacOS 10.12 Sierra

### <a name="linux"></a>Linux
- Red Hat Enterprise Linux 7.4
- Red Hat Enterprise Linux 7.3
- SUSE Linux Enterprise Server v12 SP2
- Ubuntu 16.04



## <a name="next-steps"></a>Next Steps

Finden Sie in der folgenden Schnellstarts für den Einstieg:
- [Eine Verbindung herstellen und Abfragen von SQLServer](quickstart-sql-server.md)
- [Eine Verbindung herstellen und Abfragen von Azure SQL-Datenbank](quickstart-sql-database.md)
- [Eine Verbindung herstellen und Abfragen von Azure Datawarehouse](quickstart-sql-dw.md)

Tragen zu [!INCLUDE[name-sos](../includes/name-sos-short.md)]:
- [https://github.com/Microsoft/sqlopsstudio](https://github.com/Microsoft/sqlopsstudio) 

[Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839) und [Sammlung von Verwendungsdaten](usage-data-collection.md).