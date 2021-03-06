---
title: Angeben von Partition und Optionen für die Rollenbereitstellung | Microsoft Docs
ms.custom: ''
ms.date: 03/27/2018
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.service: ''
ms.component: data-mining
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- input files [Analysis Services]
- partitions [Analysis Services], deployment options
- Analysis Services deployments, roles
- Analysis Services deployments, partitions
- Analysis Services Deployment Wizard, roles
- Analysis Services Deployment Wizard, partitions
- deploying [Analysis Services], roles
- roles [Analysis Services], deployment options
- deploying [Analysis Services], partitions
- modifying role deployments
- modifying partition deployments
ms.assetid: e9b9ca57-a5cc-4fc0-87b5-305257038d56
caps.latest.revision: ''
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: 74983fd59a7262f7deb116d50709273e57743f18
ms.sourcegitcommit: d6881107b51e1afe09c2d8b88b98d075589377de
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="deployment-script-files---partition-and-role-deployment-options"></a>Bereitstellung Skriptdateien - Partition und Optionen für die Rollenbereitstellung
[!INCLUDE[ssas-appliesto-sqlas-all-aas](../../includes/ssas-appliesto-sqlas-all-aas.md)]

  Die [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] -Bereitstellungsassistent liest die Bereitstellungsoptionen für Partitionen und Rollen aus der \< *Projektname*> .deploymentoptions-Datei. [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)]Diese Datei erstellt, beim Erstellen der [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] Projekt. [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)] verwendet die Bereitstellungsoptionen für Partitionen und Rollen des aktuellen Projekts, wenn die \< *Projektname*> .deploymentoptions-Datei wird erstellt. Weitere Informationen zu den Konfigurationseinstellungen finden Sie unter [Grundlegendes zu den zum Erstellen des Bereitstellungsskripts verwendeten Eingabedateien](../../analysis-services/multidimensional-models/deployment-script-files-input-used-to-create-deployment-script.md).  
  
## <a name="reviewing-the-partition-and-role-deployment-options"></a>Überprüfen der Bereitstellungsoptionen für Partitionen und Rollen  
 Die Bereitstellungsoptionen in der \< *Projektname*> .deploymentoptions Datei sind unter anderem folgende:  
  
 **Bereitstellungsoptionen für Partitionen**  
 Die \< *Projektname*> Datei .deploymentoptions gibt an, ob vorhandene Partitionen in der Zieldatenbank beibehalten oder überschrieben (Standard). Wenn vorhandene Partitionen beibehalten werden, werden nur neue Partitionen bereitgestellt, und der Partitions- bzw. Aggregationsentwurf in allen vorhandenen Measuregruppen wird nicht geändert.  
  
> [!NOTE]  
>  Wird die Measuregruppe, in der die Partition vorhanden ist, gelöscht, wird die Partition automatisch gelöscht.  
  
 **Bereitstellungsoptionen für Rollen**  
 Die \< *Projektname*> .deploymentoptions Datei gibt einen der folgenden Optionen für die Bereitstellung:  
  
-   Vorhandene Rollen und Rollenelemente in der Zieldatenbank werden beibehalten, und nur neue Rollen und Rollenelemente werden bereitgestellt.  
  
-   Alle in der Zieldatenbank vorhandenen Rollen und Elemente werden durch die bereitgestellten Rollen und Elemente ersetzt.  
  
-   Vorhandene Rollen und Rollenelemente in der Zieldatenbank werden beibehalten, neue Rollen werden nicht bereitgestellt.  
  
-   **Hinweis:** Wenn vorhandene Rollen und Elemente beibehalten werden, werden die Berechtigungen, die diesen Rollen zugeordnet sind, zurückgesetzt. Sicherheitsberechtigungen sind in den Objekten enthalten, die sie sichern, und nicht in den Sicherheitsrollen, denen sie zugeordnet sind. Weitere Informationen zum Arbeiten mit diesem Verhalten mithilfe des Analysis Services-Bereitstellungs-Assistenten finden Sie im Abschnitt zum Beibehalten von Rollen und Elementen in der Microsoft Knowledge Base.  
  
## <a name="modifying-the-partition-and-role-deployment-options"></a>Ändern der Bereitstellungsoptionen für Partitionen und Rollen  
 Möglicherweise müssen Sie die Bereitstellung der [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] -Projekt mit verschiedenen Optionen von Partitionen und Rollen als in der \< *Projektname*> .deploymentoptions-Datei. Sie möchten z. B. beibehalten der vorhandenen Partitionen, Rollen und Rollenmitglieder, anstatt zu ersetzen alle vorhandenen Partitionen, Rollen und Mitglieder gemäß der \< *Projektname*> .deploymentoptions-Datei.  
  
 So ändern Sie die Bereitstellung von Partitionen und Rollen in einer [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] -Projekt die Partitions- und rolleneinstellungen Einstellungen innerhalb des Projekts kann nicht geändert werden, weil die  *\<Projektname >* **Eigenschaftenseiten**  im Dialogfeld [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)] diese Optionen nicht angezeigt. Wenn Sie die Bereitstellungsoptionen für Rollen und Partitionen ändern möchten, müssen Sie diese Informationen im Ändern der \< *Projektname*> .deploymentoptions-Datei selbst. Das folgende Verfahren beschreibt, wie so ändern Sie die Bereitstellungsoptionen für Partitionen und Rollen innerhalb der \< *Projektname*> .deploymentoptions-Datei.  
  
#### <a name="to-change-the-deployment-of-partitions-or-roles-after-the-input-files-have-been-generated"></a>So ändern Sie die Bereitstellung von Partitionen und Rollen, nachdem die Eingabedateien generiert wurden  
  
-   Führen Sie den Bereitstellungs-Assistenten für [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] interaktiv aus, und geben Sie auf der Seite **Bereitstellungsoptionen für Partitionen und Rollen** neue Bereitstellungsoptionen für die Partitionen und Rollen an.  
  
     – oder –  
  
-   Führen Sie den Bereitstellungs-Assistenten für [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] an der Eingabeaufforderung aus, und legen Sie fest, dass der Assistent im Antwortdateimodus ausgeführt wird. Weitere Informationen zum Antwortdateimodus finden Sie unter [Ausführen des Bereitstellungs-Assistenten für Analysis Services](../../analysis-services/multidimensional-models/running-the-analysis-services-deployment-wizard.md).  
  
     – oder –  
  
-   Öffnen der \< *Projektname*> .deploymentoptions in einem beliebigen Texteditor und manuell die Optionen ändern.  
  
## <a name="see-also"></a>Siehe auch  
 [Angeben des Installationszieles](../../analysis-services/multidimensional-models/deployment-script-files-specifying-the-installation-target.md)   
 [Angeben der Konfigurationseinstellungen für die Lösungsbereitstellung](../../analysis-services/multidimensional-models/deployment-script-files-solution-deployment-config-settings.md)   
 [Angeben von Verarbeitungsoptionen](../../analysis-services/multidimensional-models/deployment-script-files-specifying-processing-options.md)  
  
  
