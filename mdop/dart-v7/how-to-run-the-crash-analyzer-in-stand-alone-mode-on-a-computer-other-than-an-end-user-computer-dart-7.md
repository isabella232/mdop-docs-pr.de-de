---
title: So führen Sie Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer aus
description: So führen Sie Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer aus
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809565"
---
# So führen Sie Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer aus


Wenn Sie nicht auf die Microsoft Debugging Tools für Windows oder die Symboldateien auf dem Endbenutzercomputer zugreifen können, können Sie die Speicherabbilddatei vom Problem Computer kopieren und auf einem Computer analysieren, auf dem die eigenständige Version von Crash Analyzer installiert ist, beispielsweise den Computer eines Helpdesk-Administrators.

**So führen Sie den Crash Analyzer im eigenständigen Modus aus**

1.  Klicken Sie auf einem Computer, auf dem **Start**DaRT7 installiert ist, auf  /  **Alle Programme**starten  /  **Microsoft Dart 7**.

2.  Geben Sie die erforderlichen Informationen für Folgendes an:

    -   Microsoft-Debugging-Tools für Windows

    -   Symbol Dateien

        Weitere Informationen zu Symboldateien finden Sie unter [So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).

    -   Eine Absturzspeicherabbild Datei

        **Hinweis**  Verwenden Sie das Such Tool in DaRT7, um die kopierte Absturzspeicherabbild Datei zu finden.

         

3.  **Crash Analyzer** scannt die Absturzspeicherabbild Datei und meldet eine mögliche Ursache für den Absturz. Sie können weitere Informationen zum Absturz anzeigen, beispielsweise die spezifische Absturzmeldung und Beschreibung, die zum Zeitpunkt des Absturzes geladenen Treiber und die vollständige Ausgabe der Analyse.

4.  Entscheiden Sie sich für eine geeignete Strategie zur Lösung des Problems. Möglicherweise müssen Sie den Gerätetreiber, der den Absturz verursacht hat, mithilfe des Knotens **Dienste und Treiber** des **Computer Verwaltungs** Tools in DART deaktivieren oder aktualisieren.

## Verwandte Themen


[Diagnostizieren von Systemfehlern mit Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





