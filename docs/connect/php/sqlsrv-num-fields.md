---
title: Sqlsrv_num_fields | Microsoft Docs
ms.custom: ''
ms.date: 03/23/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: ''
ms.component: php
ms.reviewer: ''
ms.suite: sql
ms.technology:
- drivers
ms.tgt_pltfrm: ''
ms.topic: article
apiname:
- sqlsrv_num_fields
apitype: NA
helpviewer_keywords:
- sqlsrv_num_fields
- API Reference, sqlsrv_num_fields
ms.assetid: 03ca1860-01ed-408c-862a-57a7355de4bf
caps.latest.revision: ''
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 80028fcf1b4a1c3d947bef49c2a4edc617f9d2d1
ms.sourcegitcommit: 2e130e9f3ce8a7ffe373d7fba8b09e937c216386
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="sqlsrvnumfields"></a>sqlsrv_num_fields
[!INCLUDE[Driver_PHP_Download](../../includes/driver_php_download.md)]

Ruft die Anzahl der Felder in einem aktiven Resultset ab. Diese Funktion kann für jede vorbereitete Anweisung, vor oder nach der Ausführung aufgerufen werden.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
sqlsrv_num_fields( resource $stmt)  
```  
  
#### <a name="parameters"></a>Parameter  
*$stmt*: Die Anweisung, zu der das Zielresultset aktiv ist.  
  
## <a name="return-value"></a>Rückgabewert  
Ein ganzzahliger Wert, der die Anzahl der Felder im aktiven Resultset darstellt. Falls ein Fehler auftritt, wird der boolesche Wert **false** zurückgegeben.  
  
## <a name="example"></a>Beispiel  
Das folgende Beispiel führt eine Abfrage zum Abrufen aller Felder für die oberen drei Zeilen in der *HumanResources.Department* Tabelle der AdventureWorks-Datenbank. Die Funktion **sqlsrv_num_fields** bestimmt die Anzahl der Felder im Resultset. Dies erlaubt die Darstellung der Daten indem in einem Iterationsverfahren durch jede ausgegebenen Zeile durchgegangen wird.  
  
Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/adventure-works) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
```  
<?php  
/* Connect to the local server using Windows Authentication and   
specify the AdventureWorks database as the database in use. */  
$serverName = "(local)";  
$connectionInfo = array( "Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false )  
{  
     echo "Could not connect.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Define and execute the query. */  
$tsql = "SELECT TOP (3) * FROM HumanResources.Department";  
$stmt = sqlsrv_query($conn, $tsql);  
if( $stmt === false)  
{  
     echo "Error in executing query.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve the number of fields. */  
$numFields = sqlsrv_num_fields( $stmt );  
  
/* Iterate through each row of the result set. */  
while( sqlsrv_fetch( $stmt ))  
{  
     /* Iterate through the fields of each row. */  
     for($i = 0; $i < $numFields; $i++)  
     {  
          echo sqlsrv_get_field($stmt, $i,   
                   SQLSRV_PHPTYPE_STRING(SQLSRV_ENC_CHAR))." ";  
     }  
     echo "\n";  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt );  
sqlsrv_close( $conn );  
?>  
```  
  
## <a name="see-also"></a>Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../../connect/php/sqlsrv-driver-api-reference.md)  

[sqlsrv_field_metadata](../../connect/php/sqlsrv-field-metadata.md)  

[Informationen zu den Codebeispielen in der Dokumentation](../../connect/php/about-code-examples-in-the-documentation.md)  
  
