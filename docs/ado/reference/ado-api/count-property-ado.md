---
title: Count-Eigenschaft (ADO) | Microsoft Docs
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
apitype: COM
f1_keywords:
- _Collection::Count
helpviewer_keywords:
- Count property [ADO]
ms.assetid: da9ccd1f-d402-41a2-940c-45556fc5340d
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 2f9ae68eda44e92834ca54613aca0a68afffc979
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2018
---
# <a name="count-property-ado"></a>Count-Eigenschaft (ADO)
Gibt die Anzahl der Objekte in einer Auflistung an.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt eine **lange** Wert.  
  
## <a name="remarks"></a>Hinweise  
 Verwenden der **Anzahl** Eigenschaft, um zu bestimmen, wie viele Objekte in einer bestimmten Sammlung sind.  
  
 Nummerierung für Mitglieder einer Sammlung mit 0 (null) beginnt, Sie sollten immer code Schleifen, beginnend mit 0 (null) dem Element und endend mit dem Wert der **Anzahl** Eigenschaft minus 1. Wenn Sie Microsoft Visual Basic verwenden und, die Mitglieder einer Sammlung ohne Überprüfung durchlaufen möchten die **Anzahl** -Eigenschaft die **für jede... Nächste** Befehl.  
  
 Wenn die **Anzahl** Eigenschaft ist 0 (null), es sind keine Objekte in der Auflistung.  
  
## <a name="applies-to"></a>Gilt für  
  
||||  
|-|-|-|  
|[Die Achsenauflistung (ADO MD)](../../../ado/reference/ado-md-api/axes-collection-ado-md.md)|[Columns-Auflistung (ADOX)](../../../ado/reference/adox-api/columns-collection-adox.md)|[CubeDefs-Auflistung (ADO MD)](../../../ado/reference/ado-md-api/cubedefs-collection-ado-md.md)|  
|[Auflistung von Dimensionen (ADO MD)](../../../ado/reference/ado-md-api/dimensions-collection-ado-md.md)|[Errors-Collection (ADO)](../../../ado/reference/ado-api/errors-collection-ado.md)|[Fields-Collection (ADO)](../../../ado/reference/ado-api/fields-collection-ado.md)|  
|[Groups-Auflistung (ADOX)](../../../ado/reference/adox-api/groups-collection-adox.md)|[Hierarchies Collection (ADO MD) (Hierarchy-Auflistung (ADO MD))](../../../ado/reference/ado-md-api/hierarchies-collection-ado-md.md)|[Auflistung von Indizes (ADOX)](../../../ado/reference/adox-api/indexes-collection-adox.md)|  
|[Keys Collection (ADOX) (Keys-Auflistung (ADOX))](../../../ado/reference/adox-api/keys-collection-adox.md)|[Levels-Auflistung (ADO MD)](../../../ado/reference/ado-md-api/levels-collection-ado-md.md)|[Members-Auflistung (ADO MD)](../../../ado/reference/ado-md-api/members-collection-ado-md.md)|  
|[Parameters-Collection (ADO)](../../../ado/reference/ado-api/parameters-collection-ado.md)|[Positionen-Auflistung (ADO MD)](../../../ado/reference/ado-md-api/positions-collection-ado-md.md)|[Procedures Collection (ADOX) (Procedures-Auflistung (ADOX))](../../../ado/reference/adox-api/procedures-collection-adox.md)|  
|[Properties-Collection (ADO)](../../../ado/reference/ado-api/properties-collection-ado.md)|[Tables-Auflistung (ADOX)](../../../ado/reference/adox-api/tables-collection-adox.md)|[Users-Auflistung (ADOX)](../../../ado/reference/adox-api/users-collection-adox.md)|  
|[Views-Auflistung (ADOX)](../../../ado/reference/adox-api/views-collection-adox.md)|||  
  
## <a name="see-also"></a>Siehe auch  
 [Beispiel der Count-Eigenschaft (VB)](../../../ado/reference/ado-api/count-property-example-vb.md)   
 [Count-Eigenschaft (VC++-Beispiel)](../../../ado/reference/ado-api/count-property-example-vc.md)   
 [Refresh-Methode (ADO)](../../../ado/reference/ado-api/refresh-method-ado.md)
