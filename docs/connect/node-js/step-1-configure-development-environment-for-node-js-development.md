---
title: "Schritt 1: Konfigurieren der Entwicklungsumgebung für die Entwicklung von Node.js | Microsoft Docs"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: node-js
ms.reviewer: 
ms.suite: sql
ms.technology: drivers
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 2dad01f1-fadf-4ac9-9b4d-26be3d301886
caps.latest.revision: "17"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: On Demand
ms.openlocfilehash: 7d723913fbc63e65a28031421da004e942f49f6e
ms.sourcegitcommit: 2713f8e7b504101f9298a0706bacd84bf2eaa174
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2017
---
# <a name="step-1--configure-development-environment-for-nodejs-development"></a>Schritt 1: Konfigurieren der Entwicklungsumgebung für Node.js-Entwicklung
Sie müssen Ihre Entwicklungsumgebung mit den Voraussetzungen zu konfigurieren, um die Entwicklung einer Anwendung mithilfe der Node.js-Treiber für SQL Server.  Die häufigste Methode ist die Verwendung den Knoten-Paket-Manager (Npm) das mühsame-Modul installieren, jedoch mühsam Moduls direkt zum download [Github](https://github.com/pekim/tedious) Falls gewünscht.  
  
Beachten Sie, dass der Treiber für Node.js TDS-Protokolls, die standardmäßig in SQL Server und Azure SQL-Datenbank aktiviert ist.  Es ist keine zusätzliche Konfiguration erforderlich.  
  
## <a name="windows"></a>Windows  
  
1. **Node.js-Laufzeit und Npm-Paket-Manager installieren**  
a. Wechseln Sie zu [Node.js](https://nodejs.org/en/download/)  
b. Klicken Sie auf den entsprechenden Windows Installer-Msi-Link.   
c. Nachdem das Download abgeschlossen ist, führen Sie die MSI-Datei zum Installieren von Node.js  
  
2. **Öffnen von cmd.exe**  
  
3. **Erstellen Sie ein Projektverzeichnis** , und navigieren Sie zu.    
```  
> mkdir HelloWorld  
> cd HelloWorld  
```  
4. **Erstellen Sie eine Knoten-Projekt.**  Um während der projekterstellung die Standardeinstellungen beibehalten möchten, drücken Sie die EINGABETASTE, bis das Projekt erstellt wurde. Am Ende dieses Schritts sehen Sie eine Datei für "Package.JSON" im Projektverzeichnis.  
```  
> npm init  
```  
  
5. **Installieren Sie mühsam-Modul in Ihrem Projekt ein.**  Dies ist die Implementierung des TDS-Protokolls, die der Treiber verwendet wird, um die Kommunikation mit SQL Server.  
```  
> npm install tedious  
```  
  
## <a name="ubuntu-linux"></a>Ubuntu Linux  
  
1.  **Geöffneten Terminaldienste**  
  
2. **Installieren Sie Node.js-Laufzeit**  
```  
>sudo apt-get install node  
```  
3. **Installieren Sie Npm (Knoten der Paket-Manager)**  
```  
> sudo apt-get install npm  
```  
4. **Erstellen Sie ein Projektverzeichnis** , und navigieren Sie zu.    
```  
> mkdir HelloWorld  
> cd HelloWorld  
```  
  
5. **Erstellen Sie eine Knoten-Projekt.**  Um während der projekterstellung die Standardeinstellungen beibehalten möchten, drücken Sie die EINGABETASTE, bis das Projekt erstellt wurde. Am Ende dieses Schritts sehen Sie eine Datei für "Package.JSON" im Projektverzeichnis.  
```  
> sudo npm init  
```  
  
6. **Installieren Sie mühsam-Modul in Ihrem Projekt ein.**  Dies ist die Implementierung des TDS-Protokolls, die der Treiber verwendet wird, um die Kommunikation mit SQL Server.  
```  
> sudo npm install tedious  
```  
  
## <a name="mac"></a>Mac  
  
1. **Node.js-Laufzeit und Npm-Paket-Manager installieren**  
a. Wechseln Sie zu [Node.js](https://nodejs.org/en/download/)  
b. Klicken Sie auf den entsprechenden Link für die Mac OS-Installer.  
c. Nachdem das Download abgeschlossen ist, führen Sie die Dmg zum Installieren von Node.js  
  
2. **Geöffneten Terminaldienste**  
  
3. **Erstellen Sie ein Projektverzeichnis** , und navigieren Sie zu.    
```  
> mkdir HelloWorld  
> cd HelloWorld  
```  
  
4. **Erstellen Sie eine Knoten-Projekt.**  Um während der projekterstellung die Standardeinstellungen beibehalten möchten, drücken Sie die EINGABETASTE, bis das Projekt erstellt wurde. Am Ende dieses Schritts sehen Sie eine Datei für "Package.JSON" im Projektverzeichnis.  
```  
> npm init  
```  
  
5. **Installieren Sie mühsam-Modul in Ihrem Projekt ein.**  Dies ist die Implementierung des TDS-Protokolls, die der Treiber verwendet wird, um die Kommunikation mit SQL Server.  
```  
> npm install tedious  
```  
  
