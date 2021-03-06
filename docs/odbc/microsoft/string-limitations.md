---
title: String-Einschränkungen | Microsoft Docs
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
- ODBC desktop database drivers [ODBC]
- desktop database drivers [ODBC]
ms.assetid: ec1da65f-c69d-415d-bf75-8fda8aa2b39f
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 8a8e90ace4e237b7945da4a43ad869b79c657ab2
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2018
---
# <a name="string-limitations"></a>Zeichenfolge-Einschränkungen
Die maximale Länge einer Zeichenfolge, SQL-Anweisung ist 65.000 Zeichen.  
  
 Wenn der Microsoft Access-Treiber verwendet wird, werden nur SQL-92 Zeichenfolgenkonstanten (durch einfache Anführungszeichen, keine doppelten Anführungszeichen) unterstützt.  
  
 Einen senkrechten Strich (&#124;) kann nicht in einer Zeichenfolge verwendet werden, ob das Zeichen in Back Anführungszeichen eingeschlossen ist.  
  
 Für eine optimale Interoperabilität Anwendungen sollten Zeichenfolgen Parameter übergeben, anstatt Übergabe in Anführungszeichen in Zeichenfolgen.
