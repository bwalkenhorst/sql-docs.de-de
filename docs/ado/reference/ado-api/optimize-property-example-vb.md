---
title: Optimieren Sie die Beispiel-Eigenschaft (VB) | Microsoft Docs
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: ado
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: sql
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
helpviewer_keywords:
- Optimize property [ADO], Visual Basic example
ms.assetid: 652194af-cfa4-4aa0-a6d6-fa409bbc3f98
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 0cbc84bfbbd4f6f26bf82bc9fe373606c965451a
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2018
---
# <a name="optimize-property-example-vb"></a>Optimieren Sie die Beispiel-Eigenschaft (VB)
Dieses Beispiel zeigt die [Feld](../../../ado/reference/ado-api/field-object.md) des Objekts dynamische **optimieren** Eigenschaft. Die ***Zip*** Feld der ***Autoren*** -Tabelle in der ***Pubs*** Datenbank ist nicht indiziert. Festlegen der [optimieren](../../../ado/reference/ado-api/optimize-property-dynamic-ado.md) Eigenschaft **"true"** auf die ***Zip*** Feld autorisiert ADO zum Erstellen eines Indexes, die die Leistung verbessert die [Suchen](../../../ado/reference/ado-api/find-method-ado.md)Methode.  
  
```  
'BeginOptimizeVB  
Public Sub Main()  
    On Error GoTo ErrorHandler  
  
    'To integrate this code  
    'replace the data source and initial catalog values  
    'in the connection string.  
  
    ' Declare the recordset and connection variables.  
    Dim Cnxn As ADODB.Connection  
    Dim rstAuthors As ADODB.Recordset  
    Dim strCnxn As String  
    Dim strSQLAuthors As String  
  
     ' Open connection.  
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _  
        "Initial Catalog='Pubs';Integrated Security='SSPI';"  
    Set Cnxn = New ADODB.Connection  
    Cnxn.Open strCnxn  
  
     ' open recordset client-side to enable index creation.  
    Set rstAuthors = New ADODB.Recordset  
    rstAuthors.CursorLocation = adUseClient  
    strSQLAuthors = "SELECT * FROM Authors"  
    rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText  
     ' Create the index.  
    rstAuthors!zip.Properties("Optimize") = True  
     ' Find Akiko Yokomoto  
    rstAuthors.Find "zip = '94595'"  
  
     ' Show results.  
    Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname & " " & _  
             rstAuthors!address & " " & rstAuthors!city & " " & rstAuthors!State  
    rstAuthors!zip.Properties("Optimize") = False  'Delete the index.  
  
    ' Clean up.  
    rstAuthors.Close  
    Cnxn.Close  
    Set rstAuthors = Nothing  
    Set Cnxn = Nothing  
    Exit Sub  
  
ErrorHandler:  
    ' clean up  
    If Not rstAuthors Is Nothing Then  
        If rstAuthors.State = adStateOpen Then rstAuthors.Close  
    End If  
    Set rstAuthors = Nothing  
  
    If Not Cnxn Is Nothing Then  
        If Cnxn.State = adStateOpen Then Cnxn.Close  
    End If  
    Set Cnxn = Nothing  
  
    If Err <> 0 Then  
        MsgBox Err.Source & "-->" & Err.Description, , "Error"  
    End If  
End Sub  
'EndOptimizeVB  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Field-Objekt](../../../ado/reference/ado-api/field-object.md)   
 [Dynamische Eigenschaft Optimize (ADO)](../../../ado/reference/ado-api/optimize-property-dynamic-ado.md)
