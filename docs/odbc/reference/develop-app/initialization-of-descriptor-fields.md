---
title: Initialisierung von Deskriptorfelder | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: drivers
ms.service: ''
ms.component: odbc
ms.reviewer: ''
ms.suite: sql
ms.technology:
- drivers
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- descriptors [ODBC], allocating and freeing
- initializing descriptor fields [ODBC]
- allocating and freeing descriptors [ODBC]
ms.assetid: 1da157cb-8ea9-4a56-983b-1c45650217c5
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: f982613a92246c96b4980997026e09d8f30e7cf4
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="initialization-of-descriptor-fields"></a>Initialisierung des Deskriptorfelder
Wenn eine Anwendung Zeilendeskriptor belegt wurde, erhalten ihre Felder Anfangswerte gemäß [SQLSetDescField](../../../odbc/reference/syntax/sqlsetdescfield-function.md). Der Anfangswert des Felds SQL_DESC_TYPE ist SQL_DEFAULT. Dies bietet sich für eine standardmäßige Behandlung von Datenbankdaten für die Darstellung der Anwendung. Die Anwendung möglicherweise eine unterschiedliche Behandlung der Daten durch Festlegen von Feldern von Deskriptordatensatz angeben.  
  
 Der Anfangswert von SQL_DESC_ARRAY_SIZE im Deskriptor-Header ist 1. Die Anwendung kann dieses Feld, um die mehrzeilige Fetch aktivieren ändern.  
  
 Das Konzept der Standardwert ist für die Felder des ein IRD ungültig. Eine Anwendung erhalten Zugriff auf die Felder einer IRD nur, wenn eine vorbereitete oder ausgeführte zugeordnet Anweisung.  
  
 Bestimmte Felder von einem IPD werden definiert, nachdem die IPD automatisch vom Treiber aufgefüllt wurde. Falls nicht, sind sie nicht definiert. Diese Felder sind SQL_DESC_CASE_SENSITIVE, SQL_DESC_FIXED_PREC_SCALE SQL_DESC_TYPE_NAME, SQL_DESC_UNSIGNED und SQL_DESC_LOCAL_TYPE_NAME.
