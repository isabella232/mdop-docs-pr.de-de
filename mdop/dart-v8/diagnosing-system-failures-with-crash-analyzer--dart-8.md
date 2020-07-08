---
title: Diagnostizieren von Systemfehlern mit Crash Analyzer
description: Diagnostizieren von Systemfehlern mit Crash Analyzer
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810618"
---
# Diagnostizieren von Systemfehlern mit Crash Analyzer


Mit dem **Crash Analyzer** in Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 können Sie eine Speicherabbilddatei auf einem Windows-basierten Computer Debuggen und dann alle zugehörigen Computer Fehler diagnostizieren. Der **Crash-Analyzer** verwendet die Microsoft-Debugging-Tools für Windows, um eine Speicherabbilddatei für den Treiber zu untersuchen, der den Computer fehlerhaft verursacht hat. Sie können Crash Analyzer auf einem Endbenutzercomputer oder im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer ausführen.

## Ausführen von Crash Analyzer auf einem Endbenutzercomputer


In der Regel führen Sie **Crash Analyzer** im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf einem Endbenutzercomputer aus, auf dem das Problem auftritt. Der **Absturzanalyse-Analyzer** versucht, die Debugging-Tools für Windows auf dem Problem Computer zu finden. Wenn das Dialogfeld Verzeichnispfad leer ist, müssen Sie den Speicherort eingeben, oder navigieren Sie zum Speicherort der Debugging Tools für Windows (Sie können die Dateien von Microsoft herunterladen). Sie müssen auch einen Pfad angeben, in dem sich die Symboldateien befinden.

Wenn Sie die Microsoft-Debugging-Tools für Windows und die Symboldateien beim Erstellen des Dart 8,0-Wiederherstellungsabbilds einbezogen haben, sollten die Tools und Symboldateien verfügbar sein, wenn Sie den **Crash Analyzer** auf dem Problem Computer ausführen. Wenn Sie Sie nicht in das DART-Wiederherstellungsabbild aufgenommen haben, oder wenn die Datenträgergröße oder Netzwerkverbindungsprobleme Sie daran hindern, Sie zu erhalten, können Sie alternativ den Crash Analyzer im eigenständigen Modus auf einem anderen Computer als dem Computer des Endbenutzers ausführen, wie im folgenden Abschnitt beschrieben.

[So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a>Ausführen von Crash Analyzer im eigenständigen Modus auf einem anderen Computer als dem Computer eines Endbenutzers


Obwohl Sie in der Regel **Crash Analyzer** auf dem Endbenutzercomputer ausführen, auf dem das Problem auftritt, können Sie den Crash Analyzer auch im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer ausführen. Sie können diese Option auswählen, wenn Sie die Windows-Debugging-Tools nicht in das DART-Wiederherstellungsabbild aufgenommen haben oder wenn die Datenträgergröße oder Netzwerkverbindungsprobleme verhindern, dass Sie die Debugging-Tools erhalten. In diesem Fall können Sie die Speicherabbilddatei vom Problem Computer kopieren und auf einem Computer analysieren, auf dem die eigenständige Version von **Crash Analyzer** installiert ist, beispielsweise auf dem Computer eines Helpdesk-Agents.

[So führen Sie Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer aus](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann


Zum Debuggen von Anwendungen, die nicht mehr reagiert haben, benötigen Sie Zugriff auf die Symboldatei, die vom Programm getrennt ist. Obwohl Symboldateien beim Ausführen von Crash Analyzer automatisch heruntergeladen werden, kann es vorkommen, dass der Problem Computer keinen Zugriff auf das Internet hat. Es gibt mehrere Möglichkeiten, um sicherzustellen, dass Ihnen der Zugriff auf Symboldateien garantiert ist.

[So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## Weitere Ressourcen zum Diagnostizieren von Systemfehlern mit Crash Analyzer


[Vorgänge für DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





