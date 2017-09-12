---
title: "Optionen für die Abonnementüberprüfung (Transaktionsabonnements) | Microsoft Dokumentation"
ms.custom: 
ms.date: 03/01/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- replication
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- sql13.rep.validate.options.f1
helpviewer_keywords:
- Subscription Validation Options dialog box
ms.assetid: fd66ad1f-df01-4240-9e89-8f41bff12c1e
caps.latest.revision: 18
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: Human Translation
ms.sourcegitcommit: f3481fcc2bb74eaf93182e6cc58f5a06666e10f4
ms.openlocfilehash: da21a38bf0797bf5368ddba1d1c2a47824bad369
ms.contentlocale: de-de
ms.lasthandoff: 06/22/2017

---
# <a name="subscription-validation-options-transactional-subscriptions"></a>Optionen für die Abonnementüberprüfung (Transaktionsabonnements)
  Mithilfe des Dialogfelds **Optionen für die Abonnementüberprüfung** können Sie angeben, ob zur Überprüfung nur die Zeilenanzahl oder die Zeilenanzahl und eine binäre Prüfsumme verwendet werden soll.  
  
## <a name="options"></a>Optionen  
 **Überprüfen Sie, ob der Abonnent die gleiche Anzahl von Zeilen mit replizierten Daten enthält wie der Verleger**  
 Wählen Sie den Typ der Zeilenanzahlüberprüfung aus, die ausgeführt werden soll. Bei Oracle-Veröffentlichungen ist die einzig verfügbare Option **Tatsächliche Zeilenanzahl durch direktes Abfragen der Tabellen berechnen**.  
  
 **Prüfsummen vergleichen, um die Zeilendaten zu überprüfen**  
 Zusätzlich zum Einbinden einer Reihe von Zeilen auf Verleger- und Abonnentenebene wird eine Prüfsumme aller Daten mit dem binären Prüfsummenalgorithmus berechnet. Ist die Zeilenanzahl fehlerhaft, wird die Berechnung der Prüfsumme nicht ausgeführt.  
  
 **Verteilungs-Agent nach Abschluss der Überprüfung beenden**  
 Standardmäßig wird der Verteilungs-Agent ununterbrochen ausgeführt. Wählen Sie diese Option aus, um den Agent nach dem Ausführen der Überprüfung zu beenden. Dadurch können Sie prüfen, ob die Überprüfung erfolgreich verlaufen ist, bevor die Replikation der Daten an den Abonnenten fortgesetzt wird.  
  
## <a name="see-also"></a>Siehe auch  
 [Überprüfen der Daten am Abonnenten](../../relational-databases/replication/validate-data-at-the-subscriber.md)   
 [Überprüfen von replizierten Daten](../../relational-databases/replication/validate-replicated-data.md)  
  
  