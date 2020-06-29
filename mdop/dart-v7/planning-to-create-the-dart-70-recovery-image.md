---
title: Planen der Erstellung des DaRT 7.0-Wiederherstellungsabbilds
description: Planen der Erstellung des DaRT 7.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808692"
---
# Planen der Erstellung des DaRT 7.0-Wiederherstellungsabbilds


Verwenden Sie die Informationen in diesem Abschnitt, wenn Sie die Erstellung des Microsoft Diagnostics and Recovery Toolset (Dart) 7-Wiederherstellungs Bilds planen.

## Planen des Erstellens des DART 7-Wiederherstellungs Bilds


Wenn Sie das DART-Wiederherstellungsbild erstellen, müssen Sie entscheiden, welche Tools in das Bild aufgenommen werden sollen. Beachten Sie, dass die Endbenutzer möglicherweise gelegentlich Zugriff auf die verschiedenen Dart-Tools haben, wenn Sie diese Entscheidung treffen. Weitere Informationen zu den Dart-Tools finden Sie unter [Übersicht über die Tools in DART 7,0](overview-of-the-tools-in-dart-70-new-ia.md). Weitere Informationen dazu, wie Sie bei der Erstellung eines sicheren Wiederherstellungs Bilds helfen können, finden Sie unter [Sicherheitsüberlegungen für Dart 7,0](security-considerations-for-dart-70-dart-7.md).

Wenn Sie das DART-Wiederherstellungsabbild erstellen, geben Sie auch an, ob Sie weitere Treiber oder Dateien einbeziehen möchten. Ermitteln Sie die Speicherorte zusätzlicher Treiber oder Dateien, die Sie in das DART-Wiederherstellungsabbild einbeziehen möchten.

## Voraussetzungen


Die folgenden Elemente sind für das Erstellen des DART-Wiederherstellungs Bilds erforderlich oder empfohlen:

-   Windows 7-Quelldateien

    Sie müssen den Pfad einer Windows 7-DVD oder von Windows 7-Quelldateien angeben. Zum Erstellen des DART-Wiederherstellungs Bilds sind Windows 7-Quelldateien erforderlich.

-   Windows-Debugging-Tools für Ihre Plattform

    Windows-Debugging-Tools sind erforderlich, wenn Sie **Crash Analyzer** ausführen, um die Ursache für einen Computerabsturz zu ermitteln. Wir empfehlen, dass Sie den Pfad der Windows-Debugging-Tools angeben, wenn Sie das DART-Wiederherstellungsabbild erstellen. Wenn dies erforderlich ist, können Sie die Windows-Debugging-Tools hier herunterladen: [herunterladen und Installieren von Debugging-Tools für Windows](https://go.microsoft.com/fwlink/?LinkId=99934).

-   Optional: **eigenständige System Sweeper** -Definitionen

    Wenn Sie dieses Tool ausführen, sind die neuesten Definitionen für das **Standalone-System Sweeper** erforderlich. Obwohl Sie die Definitionen herunterladen können, wenn Sie **Standalone-System Sweeper**ausführen, empfehlen wir, dass Sie die neuesten Definitionen zum Zeitpunkt der Erstellung des DART-Wiederherstellungsabbilds herunterladen. Auf diese Weise können Sie das Tool weiterhin mit den neuesten Definitionen ausführen, auch wenn der Problem Computer nicht über Netzwerkkonnektivität verfügt.

-   Optional: Windows-Symbole-Dateien für die Verwendung mit **Crash Analyzer**

    In der Regel werden Debuginformationen in einer Symboldatei gespeichert, die von der ausführbaren Datei getrennt ist. Sie müssen Zugriff auf die Symbol Informationen haben, wenn Sie eine Anwendung debuggen, die nicht mehr reagiert, beispielsweise wenn Sie abgestürzt ist. Weitere Informationen finden Sie unter [Diagnostizieren von System Fehlern mit Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).

## Verwandte Themen


[Planen der Bereitstellung von DaRT 7.0](planning-to-deploy-dart-70.md)

 

 





