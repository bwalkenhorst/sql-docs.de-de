---
title: Datenbank-Netzwerkzugriff | Microsoft Docs
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- ODBC [ODBC], database access
- SQL [ODBC], database access
- database access [ODBC]
- network database access [ODBC]
- standardizing database access [ODBC], network
ms.assetid: f31dd938-e992-436b-b613-145c23973064
caps.latest.revision: 8
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 5220da346aea15e2dc56224001b0d803c90e0047
ms.contentlocale: de-de
ms.lasthandoff: 09/09/2017

---
# <a name="network-database-access"></a>Netzwerk-Datenbankzugriff
Zugreifen auf eine Datenbank in einem Netzwerk erfordert eine Reihe von Komponenten, von die jedes ist unabhängig von, und befindet sich unterhalb der Programmierschnittstelle. Diese Komponenten sind in der folgenden Abbildung dargestellt.  
  
 ![Komponenten eine Datenbank in einem Netzwerk über den Zugriff auf](../../odbc/reference/media/pr04.gif "pr04")  
  
 Eine weitere Beschreibung der einzelnen Komponenten lautet folgendermaßen:  
  
-   **Programmierschnittstelle** wie weiter oben in diesem Abschnitt beschrieben wird, enthält die Programmierschnittstelle Aufrufe, die von der Anwendung. Diese Schnittstellen (embedded SQL, SQL-Modulen und Aufrufebene Schnittstellen) in der Regel für jeden DBMS spezifisch sind, auch wenn sie in der Regel ein ANSI oder ISO-Standard basieren.  
  
-   **Data Stream-Protokoll** Data Stream-Protokoll beschreibt den Datenstrom zwischen DBMS und den Client übertragen. Erfordert z. B. das Protokoll möglicherweise das erste Byte beschreiben, was der Rest des Datenstroms enthält: eine SQL-Anweisung ausgeführt wird, einen Wert gab den Fehlercode oder hat Daten zurückgegeben werden. Das Format der Rest der Daten in den Stream würde dieses Flag klicken Sie dann abhängig. Beispielsweise kann ein fehlerdatenstroms das Flag, ein 2-Byte-Ganzzahl-Fehlercode Nachrichtenlänge für eine 2-Byte-Ganzzahl-Fehler und eine Fehlermeldung enthalten.  
  
     Das Data Stream-Protokoll ist ein logisches Protokoll und ist unabhängig von der Protokolle, die vom zugrunde liegenden Netzwerk verwendet. Daher kann ein einzelnes Data Stream-Protokoll in der Regel auf eine Anzahl von unterschiedlichen Netzwerken verwendet werden. Data Stream-Protokolle sind in der Regel proprietär und wurden optimiert, um ein bestimmtes DBMS zu arbeiten.  
  
-   **Prozessübergreifende Kommunikationsmechanismus** der prozessübergreifenden Kommunikation (IPC)-Mechanismus ist der Prozess, mit dem ein Prozess mit einem anderen kommuniziert. Beispiele sind benannte Pipes, TCP/IP-Sockets und DECnet-Sockets. Die Auswahl der IPC-Mechanismus wird durch das Betriebssystem und Netzwerk verwendeten eingeschränkt.  
  
-   **Netzwerkprotokoll** das Netzwerkprotokoll wird verwendet, um den Datenstrom über ein Netzwerk zu transportieren. Sie können die Aufgaben, die berücksichtigt werden, dass unterstützt die IPC-Mechanismen verwendet, um die Daten zu implementieren Protokoll sowie die unterstützenden grundlegende Vorgänge wie dateiübertragungen stream und Druckerfreigabe. Netzwerkprotokolle gehören NetBEUI, TCP/IP, DECnet und SPX/IPX und gelten für jedes Netzwerk.