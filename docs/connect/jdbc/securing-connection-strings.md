---
title: Sichern von Verbindungszeichenfolgen | Microsoft Docs
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: jdbc
ms.reviewer: 
ms.suite: sql
ms.technology: drivers
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 69ce8557-5260-4ea4-81b8-d0c5481f0868
caps.latest.revision: "9"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 588166b41e7a66a442b1b5b49fbdcaf0d6d13320
ms.sourcegitcommit: 2713f8e7b504101f9298a0706bacd84bf2eaa174
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2017
---
# <a name="securing-connection-strings"></a>Sichern von Verbindungszeichenfolgen
[!INCLUDE[Driver_JDBC_Download](../../includes/driver_jdbc_download.md)]

  Beim Schutz des Zugriffs auf die Datenquelle handelt es sich um eine der wichtigsten Aufgaben, um eine Anwendung zu sichern. Um den Zugriff auf die Datenquelle zu beschränken, müssen Sie entsprechenden Vorsichtsmaßnahmen vorsehen, die Verbindungsinformationen wie Benutzer-ID, Kennwort und Datenquellennamen sichern. Das Speichern von Benutzer-ID und Kennwort in unverschlüsselter Form, z. B. im Quellcode, bildet ein schwerwiegendes Sicherheitsproblem. Selbst dann, wenn Sie eine kompilierte Version des Codes bereitstellen, die Benutzer-ID- und Kennwortinformationen in einer externen Quelle enthält, kann der kompilierte Code disassembliert werden, sodass Benutzer-ID und Kennwort offen gelegt werden. Daher dürfen kritische Informationen wie Benutzer-ID und Kennwort keinesfalls im Code vorhanden sein.  
  
 Sie sollten das Kennwort auf keinen Fall zusammen mit der Verbindungs-URL im Quellcode der Anwendung speichern, sondern das Kennwort in einer getrennten Datei mit eingeschränktem Zugriff speichern. Der Zugriff auf diese Datei kann dem Kontext gewährt werden, in dem die Anwendung ausgeführt wird.  
  
 Eine andere Möglichkeit besteht darin, das verschlüsselte Kennwort in einer Datei zu speichern. Sie müssen unbedingt eine Verschlüsselungs-API verwenden, die nicht voraussetzt, dass der Schlüssel in irgendeiner Form gespeichert ist und nicht vom Kennwort eines Benutzers abgeleitet wird. Sie können beispielsweise die Verwendung von zertifikatbasierenden öffentlichen/privaten Schlüsselpaaren erwägen oder ein Verfahren verwenden, in dem zwei Beteiligte ein Schlüsselvereinbarungsprotokoll (Diffie-Hellman-Algorithmus) verwenden, das identische geheime Schlüssel für die Verschlüsselung generiert, ohne dass der geheime Schlüssel übertragen werden muss.  
  
 Wenn die Informationen für die Verbindungszeichenfolge aus einer externen Quelle stammen (z. B. Eingabe von Benutzer-ID und Kennwort durch den Benutzer), müssen Sie alle Eingaben der Quelle überprüfen, um sicherzustellen, dass das richtige Format eingehalten wird und keine zusätzlichen Parameter enthalten sind, die die Verbindung beeinflussen.  
  
## <a name="see-also"></a>Siehe auch  
 [Sichern von JDBC-Treiberanwendungen](../../connect/jdbc/securing-jdbc-driver-applications.md)  
  
  
