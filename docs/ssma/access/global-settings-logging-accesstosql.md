---
title: Globale Einstellungen (Protokollierung) (AccessToSQL) | Microsoft Docs
ms.prod: sql-non-specified
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.technology:
- sql-ssma
ms.tgt_pltfrm: 
ms.topic: article
applies_to:
- Azure SQL Database
- SQL Server
ms.assetid: 835b09b5-eb42-47ea-b46e-e115d4d6461f
caps.latest.revision: 4
author: Shamikg
ms.author: Shamikg
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: ceb01feacc5557b9e7a0d1979e4f9c3d79242abe
ms.contentlocale: de-de
ms.lasthandoff: 08/02/2017

---
# <a name="global-settings-logging-accesstosql"></a>Globale Einstellungen (Protokollierung) (AccessToSQL)
Verwenden der **globale Einstellungen** (Dialogfeld), um die protokollierungseinstellungen für SSMA anzugeben. In der Regel ändern Sie diese Einstellungen nur bei der Arbeit mit Microsoft Support Services.  
  
Zum Zugriff auf dieses Dialogfeld, in dem **Tools** klicken Sie im Menü **globale Einstellungen** , und klicken Sie dann auf die **Protokollierung** unten im linken Bereich.  
  
## <a name="options"></a>enthalten  
**Nachrichten-Ebene**  
Die folgenden Optionen sind verfügbar unter **Nachrichten Ebene**:  
  
|Option|Description|  
|----------|---------------|  
|**[alle Kategorien]**|Verwendet, um den Protokolliergrad auf für alle der folgenden Optionen festlegen.|  
|**Collector**|Metadaten über das Quellschema sammelt und speichert es in das Projekt.|  
|**Konverter**|Strukturen der Quell-Datenbankobjekte wie Tabellen und gespeicherte Prozeduren in entsprechende konvertiert [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] Strukturen.|  
|**Daten migrator**|Migration von Daten aus der Quelldatenbank in [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)].|  
|**Formatierer**|Unterkomponente des Konverters, die generiert Skripts für die [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] Schema.|  
|**Grafische Benutzeroberfläche**|Nachrichten, die angezeigt werden, wenn Sie das SSMA-Tool verwenden.|  
|**Linker**|Löst SQL-Bezeichner auf und enthält Informationen zu anderen Komponenten.|  
|**Andere**|Alle Nachrichten, die nicht in einer beliebigen anderen Kategorie vorhanden sind.|  
|**Parser**|Analysiert das Quellschema an.|  
|**Für die domänensynchronisierung**|Lädt Datenquelle Datenbankobjekte in [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)].|  
|**TreeConverter**|Konvertiert Objekte in der Quell-Metadaten in [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] Metadaten.|  
  
Für jede einzelne Option unter **Nachrichten Ebene**, konfigurieren Sie einen der folgenden Protokolliergrade für SSMA:  
  
|||  
|-|-|  
|**Schwerwiegender Fehler**|Geschrieben Sie nur schwerwiegende Meldungen in das Protokoll.|  
|**Fehler**|Geschrieben Sie Fehler und schwerwiegende Meldungen in das Protokoll.|  
|**Warnung**|Geschrieben Sie Warnung, Fehler und schwerwiegende Meldungen in das Protokoll.|  
|**Info**|Geschrieben Sie Information, Warnung, Fehler und schwerwiegende Meldungen in das Protokoll.|  
|**Debuggen**|Alle Nachrichten, einschließlich Debugmeldungen in das Protokoll zu schreiben.|  
  
**Protokolldateipfad**  
Der Dateipfad und der Name der SSMA-Protokolldateien. Um einen anderen Namen anzugeben, klicken Sie auf den aktuellen Pfad aus, und klicken Sie dann auf die Schaltfläche zum Durchsuchen (**...** ) Schaltfläche.  
  
**Die Größe der Protokolldatei**  
Die maximale Größe der Protokolldatei in KB. Die Mindestgröße beträgt 10 KB. Die Standardgröße ist 10240 KB.  
  
**Gesamtanzahl der Protokolldateien**  
Wenn ein Protokoll gefüllt wird, wird SSMA benennen Sie die Log-Datei und einen neuen startet. Geben Sie mit dieser Einstellung die maximale Anzahl von Protokolldateien beibehalten. Der Mindestwert beträgt 2.  
  
