---
title: "Geänderte Funktionen (Enthaltene Datenbank) | Microsoft-Dokumentation"
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- contained database, modifications to DBs
ms.assetid: a2942509-39a2-4903-b504-ae80a300a9de
caps.latest.revision: 27
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: Human Translation
ms.sourcegitcommit: f3481fcc2bb74eaf93182e6cc58f5a06666e10f4
ms.openlocfilehash: ebdd30b879d7ef5d2cd4439ab9e4c05ffb386d37
ms.contentlocale: de-de
ms.lasthandoff: 06/22/2017

---
# <a name="modified-features-contained-database"></a>Geänderte Funktionen (Enthaltene Datenbank)
  Die folgenden Funktionen wurden geändert, damit sie von einer teilweise eigenständigen Datenbank unterstützt werden. Funktionen wurden i. d. R. so geändert, dass sie die Datenbankbegrenzung nicht überschreiten.  
  
 Weitere Informationen finden Sie unter [Contained Databases](../../relational-databases/databases/contained-databases.md).  
  
## <a name="alter-database"></a>ALTER DATABASE  
  
### <a name="application-level"></a>Anwendungsebene  
 Wenn die ALTER DATABASE-Anweisung aus einer enthaltenen Datenbank heraus verwendet wird, unterscheidet sich die Syntax von der für eine nicht enthaltene Datenbank. Zu diesen Unterschieden zählen u. a. Einschränkungen für die Elemente der Anweisung, die sich über die Datenbank hinaus zur Instanz erstrecken. Weitere Informationen finden Sie unter [ALTER DATABASE &#40;Transact-SQL&#41;](../../t-sql/statements/alter-database-transact-sql.md).  
  
### <a name="instance-level"></a>Instanzebene  
 Die Syntax für ALTER DATABASE bei Verwendung außerhalb einer enthaltenen Datenbank unterscheidet sich von der für nicht enthaltene Datenbanken. Diese Änderungen verhindern, dass die Datenbankbegrenzung überschritten wird. Weitere Informationen finden Sie unter [ALTER DATABASE &#40;Transact-SQL&#41;](../../t-sql/statements/alter-database-transact-sql.md).  
  
## <a name="create-database"></a>CREATE DATABASE  
 Die CREATE DATABASE-Syntax für eine enthaltene Datenbank unterscheidet sich von der für eine nicht enthaltene Datenbank. Informationen zu neuen Syntaxanforderungen und -optionen finden Sie unter [CREATE DATABASE &#40;SQL Server Transact-SQL&#41;](../../t-sql/statements/create-database-sql-server-transact-sql.md).  
  
## <a name="temporary-tables"></a>Temporäre Tabellen  
 Lokale temporäre Tabellen sind in einer enthaltenen Datenbank zulässig, ihr Verhalten unterscheidet sich jedoch von dem temporärer Tabellen in nicht enthaltenen Datenbanken. In abhängigen Datenbanken werden temporäre Tabellendaten in der Sortierung von **tempdb**sortiert. In einer enthaltenen Datenbank werden temporäre Tabellendaten in der Sortierung der enthaltenen Datenbank sortiert.  
  
 Sämtliche Metadaten, die temporären Tabellen zugeordnet sind (z. B. Tabellen- und Spaltennamen, Indizes usw.) liegen in der Katalogsortierung vor.  
  
 Benannte Einschränkungen dürfen in temporären Tabellen nicht verwendet werden.  
  
 Temporäre Tabellen dürfen nicht auf benutzerdefinierte Typen, XML-Schemaauflistungen und benutzerdefinierte Funktionen verweisen.  
  
## <a name="collation"></a>Sortierung  
 Im abhängigen Datenbankmodell sind drei separate Sortierungstypen vorhanden: Datenbanksortierung, Instanzsortierung und tempdb-Sortierung. In enthaltenen Datenbanken hingegen werden nur zwei Sortierungen verwendet: die Datenbanksortierung und die neue Katalogsortierung. Weitere Details zur Sortierung in eigenständigen Datenbanken finden Sie unter [Contained Database Collations](../../relational-databases/databases/contained-database-collations.md) .  
  
## <a name="user-options"></a>user options  
 Beim Aktivieren eigenständiger Datenbanken muss die [Benutzeroptionen-Option](../../database-engine/configure-windows/configure-the-user-options-server-configuration-option.md) für die Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]auf 0 (null) festgelegt sein.  
  
## <a name="see-also"></a>Siehe auch  
 [Contained Database Collations](../../relational-databases/databases/contained-database-collations.md)   
 [Contained Databases](../../relational-databases/databases/contained-databases.md)  
  
  