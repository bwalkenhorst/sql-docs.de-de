---
title: Source-Eigenschaft (ADO-Fehler) | Microsoft Docs
ms.prod: sql-non-specified
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
apitype: COM
f1_keywords:
- Error::get_Source
- Error::Source
- Error::GetSource
helpviewer_keywords:
- Source property [ADO Error]
ms.assetid: 4044ba15-f013-4c4c-9fe1-b4410fe9a778
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 86c95ebdbacfffcee3e1be83c33ff3c5261352a6
ms.contentlocale: de-de
ms.lasthandoff: 09/09/2017

---
# <a name="source-property-ado-error"></a>Source-Eigenschaft (ADO-Fehler)
Gibt den Namen des Objekts oder der Anwendung, die ursprünglich ein Fehler generiert.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt eine **Zeichenfolge** Wert, der den Namen eines Objekts oder einer Anwendung angibt.  
  
## <a name="remarks"></a>Hinweise  
 Verwenden der **Quelle** Eigenschaft auf eine [Fehler](../../../ado/reference/ado-api/error-object.md) Objekts bestimmen, den Namen des Objekts oder der Anwendung, die ursprünglich ein Fehler generiert. Dies könnte Klassennamen oder die ProgID des Objekts sein. Bei Fehlern in ADO den Wert der Eigenschaft werden **ADODB.** *ObjectName*, wobei *ObjectName* ist der Name des Objekts, das den Fehler ausgelöst hat. ADOX und ADO MD, wird der Wert **ADOX.** *ObjectName* und **ADOMD.** *ObjectName,* bzw.  
  
 Basierend auf der Fehlerdokumentation aus der **Quelle**, [Anzahl](../../../ado/reference/ado-api/number-property-ado.md), und [Beschreibung](../../../ado/reference/ado-api/description-property.md) Eigenschaften des **Fehler** Objekte aufweist, können Sie Code schreiben die wird den Fehler entsprechend behandelt.  
  
 Die **Quelle** Eigenschaft ist schreibgeschützt und für **Fehler** Objekte.  
  
## <a name="applies-to"></a>Gilt für  
 [Error-Objekt](../../../ado/reference/ado-api/error-object.md)  
  
## <a name="see-also"></a>Siehe auch  
 [Beschreibung, HelpContext HelpFile, NativeError, Anzahl, Quelle und SQLState-Eigenschaften-Beispiel (VB)](../../../ado/reference/ado-api/description-helpcontext-helpfile-nativeerror-number-source-example-vb.md)   
 [Beschreibung, HelpContext HelpFile, NativeError, Anzahl, Quelle und SQLState Eigenschaften (VC++-Beispiel)](../../../ado/reference/ado-api/description-helpcontext-helpfile-nativeerror-number-source-example-vc.md)   
 [Description-Eigenschaft](../../../ado/reference/ado-api/description-property.md)   
 [HelpContext HelpFile-Eigenschaften](../../../ado/reference/ado-api/helpcontext-helpfile-properties.md)   
 [Number-Eigenschaft (ADO)](../../../ado/reference/ado-api/number-property-ado.md)   
 [Source-Eigenschaft (ADO-Datensatz)](../../../ado/reference/ado-api/source-property-ado-record.md)   
 [Source-Eigenschaft (ADO-Recordset)](../../../ado/reference/ado-api/source-property-ado-recordset.md)
