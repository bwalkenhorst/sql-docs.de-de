---
title: SetCharacterStream-Methode (java.lang.String, java.io.Reader, Int) | Microsoft Docs
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
apiname: SQLServerCallableStatement.setCharacterStream
apilocation: sqljdbc.jar
apitype: Assembly
ms.assetid: 88a8e89e-8817-4161-85b1-9a9a2fd01cdb
caps.latest.revision: "23"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: a631792bcc17563e935716b9046af58dc1729da1
ms.sourcegitcommit: 2713f8e7b504101f9298a0706bacd84bf2eaa174
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2017
---
# <a name="setcharacterstream-method-javalangstring-javaioreader-int"></a>setCharacterStream-Methode (java.lang.String, java.io.Reader, int)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Legt den angegebenen Parameter auf das SpecifiedReader-Objekt, das die angegebeneanzahl von Zeichen lang ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public final void setCharacterStream(java.lang.String parameterName,  
                              java.io.Reader value,  
                              int length)  
```  
  
#### <a name="parameters"></a>Parameter  
 *parameterName*  
  
 Ein **Zeichenfolge** , die den Namen des Parameters enthält.  
  
 *value*  
  
 Ein Readerobjekt, das die Unicode-Daten enthält.  
  
 *length*  
  
 Ein **Int** , der die Länge in Zeichen angibt.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Hinweise  
 Diese SetCharacterStream-Methode wird von der SetCharacterStream-Methode in der java.sql.CallableStatement-Schnittstelle angegeben.  
  
 Wenn die Länge des Datenstroms, angegeben unterscheidet die *Länge* Parameter, der JDBC-Treiber löst eine Ausnahme aus, wenn die Zeile aktualisiert oder eingefügt wird.  
  
 Wenn die Länge des Datenstroms unbekannt ist, ist die *Länge* Parameter kann auf-1 festgelegt werden, um anzugeben, dass der Treiber den Datenstrom unabhängig von seiner Länge akzeptiert werden sollen. Bei "sqljdbc4.jar", empfehlen wir, dass Sie die JDBC 4.0-Methode verwenden [SetCharacterStream-Methode (java.lang.String, java.io.Reader)](../../../connect/jdbc/reference/setcharacterstream-method-java-lang-string-java-io-reader.md) bei die Anwendung möchte, um die Spalte aus einem Stream zu aktualisieren, deren Länge unbekannt ist.  
  
## <a name="see-also"></a>Siehe auch  
 [SQLServerCallableStatement-Elemente](../../../connect/jdbc/reference/sqlservercallablestatement-members.md)   
 [SQLServerCallableStatement-Klasse](../../../connect/jdbc/reference/sqlservercallablestatement-class.md)  
  
  
