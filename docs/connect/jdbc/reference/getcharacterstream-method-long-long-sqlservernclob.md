---
title: GetCharacterStream-Methode (long, Long) (SQLServerNClob) | Microsoft Docs
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
ms.assetid: 5a8028bc-c877-4668-b662-0746d462040e
caps.latest.revision: "14"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: ee42e6ef541b8f3c8298d467b6eb72237016efb4
ms.sourcegitcommit: 2713f8e7b504101f9298a0706bacd84bf2eaa174
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2017
---
# <a name="getcharacterstream-method-long-long-sqlservernclob"></a>getCharacterStream-Methode (long, long) (SQLServerNClob)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ruft die **NCLOB** Daten als ein **Reader** Objekt oder als zeichendatenstrom mit angegebener Position und Länge.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public java.io.Reader getCharacterStream(long pos,  
                                  long length)  
```  
  
#### <a name="parameters"></a>Parameter  
 *POS*  
  
 Ein **lange** , die angibt, dass des Offsets zum ersten Zeichen des abzurufenden abgerufen werden sollen.  
  
 *length*  
  
 Ein **lang** , der angibt, dass der Länge in Zeichen des abzurufenden abgerufen werden sollen.  
  
## <a name="return-value"></a>Rückgabewert  
 Ein Readerobjekt, enthält die **NCLOB** Daten.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Hinweise  
 Diese GetCharacterStream-Methode wird von der GetCharacterStream-Methode in der java.sql.NClob-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Siehe auch  
 [GetCharacterStream-Methode &#40; SQLServerNClob &#41;](../../../connect/jdbc/reference/getcharacterstream-method-sqlservernclob.md)   
 [SQLServerNClob-Methoden](../../../connect/jdbc/reference/sqlservernclob-methods.md)   
 [SQLServerNClob-Elemente](../../../connect/jdbc/reference/sqlservernclob-members.md)   
 [SQLServerNClob-Klasse](../../../connect/jdbc/reference/sqlservernclob-class.md)  
  
  
