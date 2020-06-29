---
title: So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus
description: So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus
author: dansimp
ms.assetid: 10334800-ff8e-43ac-a9c2-d28807473ec2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4abf1ba2ae1a0cb1dfb129c1f5a26e11f5045290
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809493"
---
# So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus


Zum Ausführen von **Crash Analyzer** aus dem Fenster " **Diagnose-und Wiederherstellungs-Toolset** " auf einem Endbenutzercomputer, auf dem Probleme auftreten, müssen die Microsoft-Debugging-Tools für Windows und die Symboldateien installiert sein. Informationen zum Herunterladen der Windows-Debugging-Tools finden Sie unter [Debuggen von Tools für Windows](https://go.microsoft.com/fwlink/?LinkId=266248).

**So führen Sie den Crash Analyzer auf einem Endbenutzercomputer aus**

1.  Klicken Sie im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf einem Endbenutzercomputer auf **Crash Analyzer**.

2.  Geben Sie die erforderlichen Informationen für die Microsoft-Debugging-Tools für Windows ein.

3.  Geben Sie die erforderlichen Informationen für die Symboldateien an. Weitere Informationen zu Symboldateien finden Sie unter [So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).

4.  Geben Sie die erforderlichen Informationen für eine Speicherabbilddatei an. So ermitteln Sie den Speicherort der Speicherabbilddatei:

    1.  Öffnen Sie das Fenster **System Eigenschaften** .

    2.  Klicken Sie auf **Start**, geben Sie **sysdm.cpl**ein, und drücken Sie dann die **Eingabe**Taste.

    3.  Klicken Sie auf die Registerkarte **Erweitert**.

    4.  Klicken Sie im Bereich **Start und Wiederherstellung** auf **Einstellungen**.

        Wenn Sie keinen Zugriff auf das Fenster " **System Eigenschaften** " haben, können Sie mithilfe des **Such** Tools in Microsoft Diagnostics and Recovery Toolset (Dart) 10 nach Dumpdateien auf dem Endbenutzercomputer suchen.

    Der **Crash Analyzer** scannt die Speicherabbilddatei und meldet eine mögliche Ursache des Problems. Sie können weitere Informationen zu dem Fehler anzeigen, beispielsweise die spezifische Speicherabbild Nachricht und-Beschreibung, die Treiber, die zum Zeitpunkt des Fehlers geladen wurden, und die vollständige Ausgabe der Analyse.

5.  Ermitteln Sie die geeignete Strategie zur Behebung des Problems. Bei der Strategie kann es erforderlich sein, den Gerätetreiber, der den Fehler verursacht hat, mithilfe des Knotens **Dienste und Treiber** des **Computerverwaltungs** -Tools in DART 10 zu deaktivieren oder zu aktualisieren.

## Verwandte Themen


[Diagnostizieren von Systemfehlern mit Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)

[Vorgänge für DaRT 10](operations-for-dart-10.md)

 

 





