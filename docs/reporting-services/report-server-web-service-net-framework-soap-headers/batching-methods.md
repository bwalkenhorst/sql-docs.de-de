---
title: Methoden der Batchverarbeitung | Microsoft-Dokumentation
ms.custom: 
ms.date: 03/04/2017
ms.prod: reporting-services
ms.prod_service: reporting-services-native
ms.service: 
ms.component: report-server-web-service-net-framework-soap-headers
ms.reviewer: 
ms.suite: pro-bi
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: reference
applies_to: SQL Server 2016 Preview
helpviewer_keywords:
- methods [Reporting Services], batches
- BatchHeader SOAP header
- Web service [Reporting Services], methods
- Report Server Web service, batching
- batches [Reporting Services]
- XML Web service [Reporting Services], methods
- locking [Reporting Services]
- multiple Web service methods
ms.assetid: 86435534-c9fe-4b49-b88c-7fb6d21976b0
caps.latest.revision: "36"
author: markingmyname
ms.author: maghan
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: ea3dc6c1bd099482234c779914336ec1c01475ae
ms.sourcegitcommit: 7e117bca721d008ab106bbfede72f649d3634993
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2018
---
# <a name="batching-methods"></a>Methoden der Batchverarbeitung
  Durch die Verwendung von SOAP-Headern in [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] können Sie mehrere Webdienstmethoden in einen einzelnen Vorgang aufnehmen. Die Methoden werden im Rahmen einer Datenbanktransaktion in der Reihenfolge ihres Aufrufs ausgeführt.  
  
 Rollback hat den Vorteil, dass aus mehreren Methoden bestehende Batchvorgänge verwendet werden können. Wenn ein Fehler in einem der Methodenaufrufe auftritt, während ein Batch ausgeführt wird, stoppt der Berichtsserver die Verarbeitung und führt ein Rollback aller vorherigen Vorgänge aus. Dies ist dann sinnvoll, wenn ein Methodenaufruf von der erfolgreichen Durchführung anderer Methodenaufrufe im Batch abhängt.  
  
 Der Webdienst enthält keine Sperrsemantik für aus mehreren Methoden bestehende Batchvorgänge. Zeilen in einer Berichtsserver-Datenbank werden erst dann für das Update gesperrt, wenn die Meldung an den Server gesendet wird und der Execute-Befehl aufgerufen wird.  
  
 Es ist keine Parallelitätssteuerung vorhanden, die sicherstellt, dass die Datenbank nicht geändert wurde, seit die Daten zum letzten Mal gelesen wurden. Wenn zwei Clients dasselbe Element ändern, ist das letzte Update erfolgreich, wenn die Parameter noch gültig sind (z. B. wenn das Element nicht umbenannt wurde).  
  
 Im folgenden Beispiel wird die <xref:ReportService2005.ReportingService2005.CreateFolder%2A>-Methode dreimal aufgerufen, und diese Aufrufe werden in einem Batch ausgeführt. Wenn einer der Aufrufe von <xref:ReportService2005.ReportingService2005.CreateFolder%2A> fehlschlägt, wird der gesamte Batch abgebrochen.  
  
```vb  
Imports System  
Imports System.Web.Services.Protocols  
Imports myNamespace.MyReferenceName  
  
Class Sample  
    Sub Main(args() As String)  
        Dim rs As New ReportingService2005()  
        rs.Credentials = System.Net.CredentialCache.DefaultCredentials  
      ' Set the base Web service URL of the source server  
      rs.Url = "http://<Server Name>/reportserver/ReportService2005.asmx"  
  
        Dim bh As New BatchHeader()  
  
        bh.BatchId = service.CreateBatch()  
        rs.BatchHeaderValue = bh  
        rs.CreateFolder("New Folder1", "/", Nothing)  
        rs.CreateFolder("New Folder2", "/", Nothing)  
        rs.CreateFolder("New Folder3", "/", Nothing)  
  
        Console.WriteLine("Creating folders...")  
        rs.BatchHeaderValue = bh  
        rs.ExecuteBatch()  
        Console.WriteLine("Folders created successfully.")  
  
        rs.BatchHeaderValue = Nothing  
    End Sub  
End Class  
```  
  
```csharp  
using System;  
using System.Web.Services.Protocols;   
using myNamespace.MyReferenceName;  
  
class Sample  
{  
    static void Main(string[] args)  
    {  
        ReportingService2005 rs = new ReportingService2005();  
        rs.Credentials = System.Net.CredentialCache.DefaultCredentials;  
      // Set the base Web service URL of the source server  
      rs.Url = "http://<Server Name>/reportserver/ReportService2005.asmx"  
  
        BatchHeader bh = new BatchHeader();  
  
        bh1.BatchID = service.CreateBatch();  
        rs.BatchHeaderValue = bh;  
        rs.CreateFolder("New Folder1", "/", null);  
        rs.CreateFolder("New Folder2", "/", null);  
        rs.CreateFolder("New Folder3", "/", null);  
  
        Console.WriteLine("Creating folders...");  
        rs.BatchHeaderValue = bh1;  
        rs.ExecuteBatch();  
        Console.WriteLine("Folders created successfully.");  
  
        rs.BatchHeaderValue = null;  
    }  
}  
```  
  
## <a name="see-also"></a>Weitere Informationen finden Sie unter  
 <xref:ReportService2005.ReportingService2005.CancelBatch%2A>   
 <xref:ReportService2005.ReportingService2005.CreateBatch%2A>   
 [Technische Referenz (SSRS)](../../reporting-services/technical-reference-ssrs.md)   
 [Using Reporting Services SOAP Headers (Verwenden von Reporting Services SOAP-Headern)](../../reporting-services/report-server-web-service-net-framework-soap-headers/using-reporting-services-soap-headers.md)  
  
  
