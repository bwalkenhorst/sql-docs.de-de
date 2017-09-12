---
title: "Berechtigungen für Hierarchieelemente (Master Data Services) | Microsoft Docs"
ms.custom: 
ms.date: 03/01/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- master-data-services
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- members [Master Data Services], permissions
- permissions [Master Data Services], members
ms.assetid: b3880eed-1bf6-4f65-ab23-b08c194cc858
caps.latest.revision: 11
author: sabotta
ms.author: carlasab
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f3481fcc2bb74eaf93182e6cc58f5a06666e10f4
ms.openlocfilehash: 5df8a0f0c01842c00c3698146e84ed78e6320683
ms.contentlocale: de-de
ms.lasthandoff: 08/02/2017

---
# <a name="hierarchy-member-permissions-master-data-services"></a>Berechtigungen für Hierarchieelemente (Master Data Services)
  Berechtigungen für Hierarchieelemente sind optional und sollten nur verwendet werden, wenn ein Benutzer beschränkten Zugriff auf bestimmte Elemente erhalten soll. Wenn Sie keine Berechtigungen auf der Registerkarte **Hierarchieelemente** zuweisen, basieren die Berechtigungen eines Benutzers ausschließlich auf den Berechtigungen, die auf der Registerkarte **Modelle** zugewiesen wurden.  
  
 Berechtigungen für Hierarchieelemente werden in der [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)] -Benutzeroberfläche im Funktionsbereich **Benutzer- und Gruppenberechtigungen** auf der Registerkarte **Hierarchieelemente** zugewiesen. Von diesen Berechtigungen hängt es ab, auf welche Elemente ein Benutzer im Funktionsbereich **Explorer** der Benutzeroberfläche zugreifen kann.  
  
 Auf der Registerkarte **Hierarchieelemente** wird jede Hierarchie als Baumstruktur dargestellt. Wenn Sie eine Berechtigung für einen Knoten in der Struktur zuweisen, erben alle untergeordneten Elemente diese Berechtigung, sofern sie nicht auf einer niedrigeren Ebene explizit zugewiesen wurde.  
  
> [!NOTE]  
>  Wenn Sie einem Hierarchieknoten eine Berechtigung zuweisen, werden alle Elemente in den anderen Knoten auf gleicher oder höherer Ebene implizit verweigert.  
  
 Im **Explorer**werden die Elementberechtigungen überall dort angewendet, wo das Element angezeigt wird. Ein Element mit **Leseberechtigung** kann beispielsweise alle Entitäten, Hierarchien und Sammlungen lesen, denen es angehört.  
  
 Berechtigungen für Hierarchieelemente gelten für die Modellversion, denen sie zugewiesen werden, sowie für alle zukünftigen Kopien der Version. Sie gelten nicht für Vorgängerversionen der Version, der sie zugewiesen wurden.  
  
|Berechtigung|Description|  
|----------------|-----------------|  
|**Leseberechtigung**|Die Elemente werden angezeigt.<br /><br /> <br /><br /> Hinweis: Wenn Sie nur dem **Stamm** die **Leseberechtigung**zuweisen, sind die Elemente unter **Stamm** schreibgeschützt. In expliziten Hierarchien und Sammlungen kann der Benutzer jedoch Elemente in den **Stamm** verschieben und dem **Stamm**neue Elemente hinzufügen.|  
|**Create**|Die Hierarchieelementberechtigung enthält keine Berechtigung zum Erstellen.|  
|**Update**|Die Elemente werden angezeigt und können vom Benutzer geändert werden. Der Benutzer kann die Elemente außerdem in beliebigen expliziten Hierarchien oder Auflistungen verschieben, denen die Elemente angehören.|  
|**Delete**|Die Elemente werden angezeigt und können vom Benutzer gelöscht werden.|  
|**Verweigern**|Die Elemente werden nicht angezeigt.|  
  
 Auf der Registerkarte **Hierarchieelemente** werden die zugewiesenen Berechtigungen nicht sofort wirksam. Wie häufig die Berechtigungen angewendet werden, hängt von der Einstellung **Member security processing interval setting** (Intervall für die Verarbeitung der Mitgliedersicherheit) ab, die Sie in der Tabelle „Systemeinstellungen“ der [!INCLUDE[ssMDSshort](../includes/ssmdsshort-md.md)] -Datenbank vornehmen. Eine Anleitung für die sofortige Anwendung von Elementberechtigungen finden Sie unter [Sofortiges Anwenden von Elementberechtigungen &#40;Master Data Services&#41;](../master-data-services/immediately-apply-member-permissions-master-data-services.md)neue Elemente hinzufügen.  
  
> [!NOTE]  
>  Sie können rekursiven Hierarchien, abgeleiteten Hierarchien mit expliziten Abschlüssen und abgeleiteten Hierarchien mit ausgeblendeten Ebenen keine Hierarchieelementberechtigungen zuweisen.  
  
## <a name="possible-overlapping-permissions"></a>Mögliche Überlappungen bei Berechtigungen  
 Wenn Sie Elementen eine Berechtigung zuweisen, müssen möglicherweise überlappende Berechtigungen aufgelöst werden.  
  
### <a name="when-a-member-belongs-to-multiple-hierarchies"></a>Wenn ein Element mehreren Hierarchien angehört  
 Das gleiche Element kann in zwei oder mehr Hierarchien enthalten sein.  
  
-   Wenn einem Hierarchieknoten die Berechtigung **Aktualisieren** und einem anderen die **Leseberechtigung**zugewiesen wird, sind die Elemente im Knoten **leseberechtigt**.  
  
-   Wenn einem Hierarchieknoten die Berechtigungen **Aktualisieren** und **Erstellen** und einem anderen die Berechtigungen **Aktualisieren** und **Löschen** zugewiesen sind, können die Elemente im Knoten aktualisiert werden.  
  
-   Wenn einem Hierarchieknoten eine beliebige Kombination der Berechtigungen **Erstellen**/**Lesen**/**Aktualisieren**/**Löschen** und einem anderen Knoten die Berechtigung **Ablehnen** zugewiesen wird, wird der Zugriff auf die Elemente im Knoten verweigert.  
  
## <a name="external-resources"></a>Externe Ressourcen  
 Blogbeitrag [Sicherheitsverbesserungen](http://go.microsoft.com/fwlink/p/?LinkId=615376), auf msdn.com.  
  
## <a name="see-also"></a>Siehe auch  
 [Zuweisen von Hierarchieelementberechtigungen &#40;Master Data Services&#41;](../master-data-services/assign-hierarchy-member-permissions-master-data-services.md)   
 [Vorgehensweise: Festlegen von Berechtigungen &#40;Master Data Services&#41;](../master-data-services/how-permissions-are-determined-master-data-services.md)   
 [Mitglieder &#40; Master Data Services &#41;](../master-data-services/members-master-data-services.md)   
 [Hierarchien &#40; Master Data Services &#41;](../master-data-services/hierarchies-master-data-services.md)   
 [Sofortiges Anwenden von Elementberechtigungen &#40; Master Data Services &#41;](../master-data-services/immediately-apply-member-permissions-master-data-services.md)  
  
  