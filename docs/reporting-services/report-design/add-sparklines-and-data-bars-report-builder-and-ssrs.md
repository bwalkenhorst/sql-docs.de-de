---
title: "Hinzufügen von Sparklines und Datenbalken (Berichts-Generator und SSRS) | Microsoft-Dokumentation"
ms.custom: 
ms.date: 03/03/2017
ms.prod: reporting-services
ms.prod_service: reporting-services-sharepoint, reporting-services-native
ms.service: 
ms.component: report-design
ms.reviewer: 
ms.suite: pro-bi
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 0b297c2e-d48b-41b0-aabd-29680cdcdb05
caps.latest.revision: "8"
author: maggiesMSFT
ms.author: maggies
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: 20f192f6480b392e611f875c85d0f65d9dc639b4
ms.sourcegitcommit: 7e117bca721d008ab106bbfede72f649d3634993
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2018
---
# <a name="add-sparklines-and-data-bars-report-builder-and-ssrs"></a>Hinzufügen von Sparklines und Datenbalken (Berichts-Generator und SSRS)
  Sparklines und Datenbalken sind kleine, zusätzliche Diagramme, die viele Information mit wenig relevanten Details vermitteln. Weitere Informationen dazu finden Sie unter [Sparklines und Datenbalken &#40;Berichts-Generator und SSRS&#41;](../../reporting-services/report-design/sparklines-and-data-bars-report-builder-and-ssrs.md).  
  
 In paginierten [!INCLUDE[ssRSnoversion_md](../../includes/ssrsnoversion-md.md)] -Berichten werden Sparklines und Datenbalken meist in die Zellen einer Tabelle oder Matrix eingefügt. Sparklines zeigen normalerweise jeweils nur eine Reihe an. Datenbalken können einen oder mehrere Datenpunkte enthalten. Sowohl Sparklines als auch Datenbalken gewinnen dadurch an Bedeutung, dass sie die Reiheninformationen für jede Zeile in der Tabelle oder der Matrix wiederholen.  
  
## <a name="to-add-a-sparkline-or-data-bar-to-a-table-or-matrix"></a>So fügen Sie einer Sparkline oder einem Datenbalken eine Tabelle oder Matrix hinzu  
  
1.  Erstellen Sie eine [Tabelle](../../reporting-services/report-design/tables-report-builder-and-ssrs.md) oder eine [Matrix](../../reporting-services/report-design/create-a-matrix-report-builder-and-ssrs.md) mit den Daten, die angezeigt werden sollen, falls Sie dies nicht bereits getan haben.  
  
2.  Fügen Sie eine Spalte in die Tabelle oder Matrix ein. Weitere Informationen finden Sie unter [Einfügen oder Löschen einer Spalte (Berichts-Generator und SSRS)](../../reporting-services/report-design/insert-or-delete-a-column-report-builder-and-ssrs.md).  
  
3.  Klicken Sie auf der Registerkarte **Einfügen** auf **Sparkline** oder **Datenbalken**, und klicken Sie dann in eine Zelle in der neuen Spalte.  
  
    > [!NOTE]  
    >  Sie können Sparklines nicht in die Detailgruppe in einer Tabelle einfügen. Sie müssen in eine Zelle eingefügt werden, die einer Gruppe zugeordnet ist.  
  
4.  Klicken Sie im Dialogfeld **Sparkline-/Datenleistentyp ändern** auf die gewünschte Sparkline- oder Datenbalkenart und anschließend auf **OK**.  
  
5.  Klicken Sie auf die Sparkline oder den Datenbalken.  
  
     Der Bereich **Diagrammdaten** wird geöffnet.  
  
6.  Klicken Sie im Bereich **Werte** auf das Pluszeichen ( **) bei** Felder hinzufügen**+**und anschließend auf das Feld, dessen Werte Sie als Diagramm darstellen möchten.  
  
7.  Klicken Sie im Bereich **Kategoriegruppen** auf das Pluszeichen ( **) bei** Felder hinzufügen**+**und anschließend auf das Feld, nach dessen Werten Sie gruppieren möchten.  
  
     In der Regel fügen Sie bei Sparklines und Datenbalken dem Bereich **Reihengruppe** kein Feld hinzu, da Sie nur eine Reihe für jede Zeile möchten.  
  
## <a name="see-also"></a>Weitere Informationen finden Sie unter  
 [Diagramme &#40;Berichts-Generator und SSRS&#41;](../../reporting-services/report-design/charts-report-builder-and-ssrs.md)   
 [Ausrichten von Diagrammdaten in einer Tabelle oder einer Matrix &#40;Berichts-Generator und SSRS&#41;](../../reporting-services/report-design/align-the-data-in-a-chart-in-a-table-or-matrix-report-builder-and-ssrs.md)  
  
  
