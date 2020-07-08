---
title: Diagnostizieren von Systemfehlern mit Crash Analyzer
description: Diagnostizieren von Systemfehlern mit Crash Analyzer
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809973"
---
# Diagnostizieren von Systemfehlern mit Crash Analyzer


Mit dem Crash Analyzer in Microsoft Diagnostics and Recovery Toolset (Dart) 7 können Sie eine Absturzspeicherabbild Datei auf einem Windows-basierten Computer Debuggen und dann alle zugehörigen Computer Fehler diagnostizieren. Der Crash-Analyzer verwendet die Microsoft-Debugging-Tools für Windows, um eine Absturzspeicherabbild Datei für den Treiber zu untersuchen, der den Computer fehlerhaft verursacht hat.

## Ausführen von Crash Analyzer auf einem Endbenutzer Computer


In der Regel führen Sie Crash Analyzer im Fenster Diagnose-und Wiederherstellungs-Toolset auf einem Endbenutzercomputer aus, auf dem Probleme auftreten. Der Absturzanalyse-Analyzer versucht, die Debugging-Tools für Windows auf dem Problem Computer zu finden. Wenn das Dialogfeld Verzeichnispfad leer ist, müssen Sie den Speicherort eingeben oder den Speicherort der Debugging Tools für Windows Durchsuchen (Sie können die Dateien von Microsoft herunterladen). Sie müssen auch einen Pfad angeben, in dem sich die Symboldateien befinden.

Wenn Sie die Microsoft-Debugging-Tools für Windows und die Symboldateien beim Erstellen des DART-Wiederherstellungsabbilds einbezogen haben, sollten diese verfügbar sein, wenn Sie den Crash Analyzer auf dem Problem Computer ausführen.

[So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## Ausführen von Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer


Der Absturzanalyse-Analyzer versucht, die Debugging-Tools für Windows auf dem Problem Computer zu finden. Wenn das Dialogfeld Verzeichnispfad leer ist, müssen Sie den Speicherort eingeben oder den Speicherort der Debugging Tools für Windows Durchsuchen (Sie können die Dateien von Microsoft herunterladen). Sie müssen auch einen Pfad angeben, in dem sich die Symboldateien befinden.

Wenn Sie die Microsoft-Debugging-Tools für Windows und die Symboldateien beim Erstellen des DART-Wiederherstellungsabbilds nicht einbezogen haben oder wenn die Datenträgergröße oder Netzwerkverbindungsprobleme Sie daran hindern, Sie zu erhalten, können Sie die Speicherabbilddatei vom Problem Computer kopieren und auf einem Computer analysieren, auf dem die eigenständige Version von Crash Analyzer installiert ist. , beispielsweise den Computer eines Helpdesk-Administrators.

[So führen Sie Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer aus](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## Sicherstellen, dass Crash Analyzer auf Symboldateien zugreifen kann


In der Regel werden Debuginformationen in einer Symboldatei gespeichert, die von der ausführbaren Datei getrennt ist. Sie müssen Zugriff auf die Symbol Informationen haben, wenn Sie eine Anwendung debuggen, die nicht mehr reagiert, beispielsweise wenn Sie abgestürzt ist.

Symbol Dateien werden beim Ausführen von Crash Analyzer automatisch heruntergeladen. Wenn der Computer nicht über eine Internet Verbindung verfügt oder das Netzwerk den Computer für den Zugriff auf einen HTTP-Proxy Server benötigt, können die Symboldateien nicht heruntergeladen werden.

[So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## Weitere Ressourcen zum Diagnostizieren von Systemfehlern mit Crash Analyzer


[Vorgänge für DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





