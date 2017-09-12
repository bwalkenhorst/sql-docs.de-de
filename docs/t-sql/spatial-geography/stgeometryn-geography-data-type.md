---
title: STGeometryN (Geography-Datentyp) | Microsoft Docs
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- STGeometryN (geography Data Type)
dev_langs:
- TSQL
helpviewer_keywords:
- STGeometryN method
ms.assetid: 53755f69-cd50-475b-b3b8-a1a9157cf03a
caps.latest.revision: 15
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: d5d11dc77ce692543068cba6739ef982bc8264c8
ms.contentlocale: de-de
ms.lasthandoff: 09/01/2017

---
# <a name="stgeometryn-geography-data-type"></a>STGeometryN (geography-Datentyp)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx_md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

  Gibt ein angegebenes **Geography** Element in einem **GeometryCollection** oder einem seiner Untertypen. Bei Verendung STGeometryN() für einen Untertyp einer **GeometryCollection**, wie z. B. **MultiPoint** oder **MultiLineString**, gibt diese Methode die **Geography**  Instanz, wenn N = 1 aufgerufen.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
.STGeometryN ( expression )  
```  
  
## <a name="arguments"></a>Argumente  
 *expression*  
 Ist ein **Int** -Ausdruck zwischen 1 und die Anzahl der **Geography** -Instanzen lautet in der **GeometryCollection**.  
  
## <a name="return-types"></a>Rückgabetypen  
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]Rückgabetyp: **Geography**  
  
 CLR-Rückgabetyp: **SqlGeography**  
  
## <a name="remarks"></a>Hinweise  
 Diese Methode gibt null, wenn der Parameter größer als das Ergebnis der [STNumGeometries()](../../t-sql/spatial-geography/stnumgeometries-geography-data-type.md) und löst eine **ArgumentOutOfRangeException** Wenn die *Ausdruck* -Parameter ist kleiner als 1.  
  
## <a name="examples"></a>Beispiele  
 Das folgende Beispiel erstellt eine `MultiPoint``geography` Instanz und verwendet `STGeometryN()` finden Sie die zweite `geography` -Instanz die **GeometryCollection**.  
  
```  
DECLARE @g geography;  
SET @g = geography::STGeomFromText('MULTIPOINT(-122.360 47.656, -122.343 47.656)', 4326);  
SELECT @g.STGeometryN(2).ToString();  
```  
  
## <a name="see-also"></a>Siehe auch  
 [OGC-Methoden für Geography-Instanzen](../../t-sql/spatial-geography/ogc-methods-on-geography-instances.md)  
  
  