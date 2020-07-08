---
title: So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus
description: So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810195"
---
# So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus


In der Regel führen Sie den Microsoft Diagnostics and Recovery Toolset (Dart) 7 Crash Analyzer aus dem Fenster Diagnose-und Wiederherstellungs-Toolset auf einem Endbenutzercomputer mit Problemen aus. Der Absturzanalyse-Analyzer versucht, die Debugging-Tools für Windows auf dem Problem Computer zu finden. Wenn das Dialogfeld Verzeichnispfad leer ist, müssen Sie den Speicherort eingeben oder den Speicherort der Debugging Tools für Windows Durchsuchen (Sie können die Dateien von Microsoft herunterladen). Sie müssen auch einen Pfad angeben, in dem sich die Symboldateien befinden.

**So öffnen und führen Sie den Crash Analyzer auf einem Endbenutzercomputer**

1.  Klicken Sie im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf einem Endbenutzercomputer auf **Crash Analyzer**.

2.  Geben Sie die erforderlichen Informationen für Folgendes an:

    -   Microsoft-Debugging-Tools für Windows

    -   Symbol Dateien

        Weitere Informationen zu Symboldateien finden Sie unter [So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).

    -   Eine Absturzspeicherabbild Datei

        Führen Sie die folgenden Schritte aus, um den Speicherort der Absturzspeicherabbild Datei zu ermitteln:

        1.  Öffnen Sie das Fenster **System Eigenschaften** .

            Klicken Sie auf **Start**, geben Sie sysdm.cpl ein, und drücken Sie dann die EINGABETASTE.

        2.  Klicken Sie auf die Registerkarte **Erweitert**.

        3.  Klicken Sie im Bereich **Start und Wiederherstellung** auf **Einstellungen**.

        **Hinweis**  Wenn Sie keinen Zugriff auf das Fenster " **System Eigenschaften** " haben, können Sie mithilfe des **Such** Tools in DART nach Dumpdateien auf dem Endbenutzercomputer suchen.

         

3.  **Crash Analyzer** scannt die Absturzspeicherabbild Datei und meldet eine mögliche Ursache für den Absturz. Sie können weitere Informationen zum Absturz anzeigen, beispielsweise die spezifische Absturzmeldung und Beschreibung, die zum Zeitpunkt des Absturzes geladenen Treiber und die vollständige Ausgabe der Analyse.

4.  Entscheiden Sie sich für eine geeignete Strategie zur Lösung des Problems. Möglicherweise müssen Sie den Gerätetreiber, der den Absturz verursacht hat, mithilfe des Knotens **Dienste und Treiber** des **Computer Verwaltungs** Tools in DART deaktivieren oder aktualisieren.

## Verwandte Themen


[Diagnostizieren von Systemfehlern mit Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





