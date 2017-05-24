---
title: "Konfigurieren eines Servers für das Ausführen der Richtlinie „Standardmäßig aus“ | Microsoft-Dokumentation"
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- dbe-query-tuning
ms.tgt_pltfrm: 
ms.topic: article
applies_to:
- SQL Server 2016
ms.assetid: 41c3022d-ab13-443e-ac64-ba1d64584f79
caps.latest.revision: 23
author: BYHAM
ms.author: rickbyh
manager: jhubbard
translationtype: Human Translation
ms.sourcegitcommit: 2edcce51c6822a89151c3c3c76fbaacb5edd54f4
ms.openlocfilehash: efc87d23faa17dca299560764b0e26bdbb05ff9a
ms.lasthandoff: 04/11/2017

---
# <a name="lesson-1-2---configure-a-server-to-run-the-off-by-default-policy"></a>Lektion 1-2 – Konfigurieren eines Servers für das Ausführen der Richtlinie „Standardmäßig aus“
Nun verfügen Sie über eine Richtlinie mit dem Namen Standardmäßig aus. In dieser Aufgabe überprüfen Sie, ob Ihr Server die Anforderungen dieser Richtlinie einhält.  
  
### <a name="to-run-the-off-by-default-policy"></a>So führen Sie die Richtlinie 'Standardmäßig aus' aus  
  
1.  Klicken Sie im Objekt-Explorer mit der rechten Maustaste auf Ihre Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], zeigen Sie auf **Richtlinien**, und klicken Sie anschließend auf **Auswerten**.  
  
2.  Im Dialogfeld **Richtlinien auswerten** können Sie Richtlinien aus einer anderen Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] oder aus einer Datei auswählen. Für diesen Schritt belassen Sie als Einstellung für **Quelle** Ihre Instanz von [!INCLUDE[ssDE](../../includes/ssde-md.md)].  
  
3.  Wählen Sie im Abschnitt **Richtlinien** die Richtlinie **Standardmäßig aus** aus.  
  
4.  Um zu sehen, ob der Server diese Richtlinie einhält, klicken Sie auf **Auswerten**.  
  
5.  Im Bereich **Ergebnisse** wird ein grüner Kreis mit einem Häkchen angezeigt, wenn [!INCLUDE[ssDE](../../includes/ssde-md.md)] die Richtlinie einhält. Ein roter Kreis mit einem X wird angezeigt, wenn [!INCLUDE[ssDE](../../includes/ssde-md.md)] die Richtlinie nicht einhält.  
  
6.  Im Bereich **Zieldetails** werden weitere Informationen in der Spalte **Meldung** angezeigt, wenn ein Fehler auftritt. Klicken Sie in der Spalte **Meldung** auf **Anzeigen** , um einen Bericht anzuzeigen, der die Überprüfungsergebnisse für jede überprüfte Facet-Eigenschaft enthält.  
  
7.  Die Richtlinienbeschreibung wird unten auf der Seite angezeigt, und im Abschnitt **Zusätzliche Hilfe** wird der Link angezeigt, den Sie für die Richtlinie konfiguriert haben. Klicken Sie auf den Meldungslink, um die Webseite zu öffnen, die Sie beim Erstellen der Richtlinie angegeben haben.  
  
8.  Schließen Sie den Browser, und schließen Sie dann das Dialogfeld **Ergebnisse, Detailansicht** .  
  
9. Wenn der Server die Richtlinie nicht einhält und Sie Datenbank-E-Mail deaktivieren möchten, klicken Sie auf der Seite **Auswertungsergebnisse** auf **Anwenden** .  
  
10. Schließen Sie das Dialogfeld **Ergebnisse, Detailansicht** und das Dialogfeld **Richtlinien auswerten** .  
  
## <a name="next-lesson"></a>Nächste Lektion  
[Lektion 2: Erstellen und Anwenden einer Richtlinie für Benennungsstandards](../../relational-databases/policy-based-management/lesson-2-create-and-apply-a-naming-standards-policy.md)  
  
  
  
