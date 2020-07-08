---
title: Informationen zu DaRT 7.0
description: Informationen zu DaRT 7.0
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809856"
---
# Informationen zu DaRT 7.0


Microsoft Diagnostics and Recovery Toolset (Dart) 7 hilft Ihnen bei der Problembehandlung und Reparatur von Windows-basierten Desktops. Dazu gehören die Desktops, die nicht gestartet werden können. Dart ist ein leistungsfähiger Satz von Tools, die die Windows-Wiederherstellungsumgebung (WinRE) verlängern. Mithilfe von DART können Sie ein Problem analysieren, um dessen Ursache zu ermitteln, beispielsweise indem Sie das Ereignisprotokoll oder die Systemregistrierung des Computers überprüfen.

DART bietet auch Tools, mit denen Sie ein Problem beheben können, sobald Sie die Ursache ermitteln. So können Sie beispielsweise die Tools in DART verwenden, um einen fehlerhaften Gerätetreiber zu deaktivieren, Hotfixes zu entfernen, gelöschte Dateien wiederherzustellen und den Computer auf Malware zu überprüfen, auch wenn Sie das installierte Windows-Betriebssystem nicht starten können oder sollten.

Dart kann Ihnen dabei helfen, Computer mit einer 32-Bit-oder 64-Bit-Version von Windows 7 schnell wiederherzustellen, in der Regel in kürzerer Zeit als beim neubilden des Computers.

## Informationen zum Wiederherstellungsbild von DART 7


Mit der Funktionalität in DART können Sie ein Wiederherstellungsabbild erstellen, das auf WinRE basiert, kombiniert mit einer Reihe von Tools, die Dart bereitstellt. Das Dart-Wiederherstellungsabbild nutzt WinRE, aus dem Sie auf das Fenster **Diagnose-und Wiederherstellungs-Toolset** zugreifen können.

Verwenden Sie den **Dart-Wiederherstellungsbild-Assistenten** zum Erstellen des DART-Wiederherstellungs Bilds. Standardmäßig erstellt der Assistent eine Image-Datei für die internationale Organisation für Standardisierung (ISO) auf dem Desktop mit dem Namen "DaRT70. ISO", obwohl Sie einen anderen Speicherort und einen anderen Dateinamen angeben können. Mit dem Assistenten können Sie auch das Bild auf eine CD oder DVD brennen. Nach Abschluss des Assistenten können Sie das Wiederherstellungsabbild auf einem USB-Flashlaufwerk speichern oder in einem Format speichern, das Sie zum Erstellen einer Remotepartition oder einer Wiederherstellungspartition verwenden können.

Wenn Sie DART verwenden müssen, um einen Endbenutzercomputer zu starten, der nicht gestartet wird, können Sie die Anweisungen zum [Wiederherstellen von lokalen Computern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)befolgen.

Detaillierte Informationen zu den Tools in DART finden Sie unter [Übersicht über die Tools in DART 7,0](overview-of-the-tools-in-dart-70-new-ia.md).

## <a href="" id="what-s-new-in-dart-7"></a>Neuerungen in DART 7


DaRT7 unterstützt weiterhin alle in früheren Versionen enthaltenen Szenarien und fügt zusätzlich zu drei neuen Bereitstellungsoptionen ein neues Remote Verbindungs Feature hinzu.

### Dart 7-Bild Erstellung

Der Assistent, den Sie zum Erstellen von DART-ISO-Bildern verwenden, wird nun als **Dart-Wiederherstellungsbild** bezeichnet und unterstützt nun eine Option zum Aktivieren oder Deaktivieren des neuen Remote Verbindungs Features. Mit der Remoteverbindung kann ein Helpdesk-Mitarbeiter die Dart-Tools von einem Remotestandort aus ausführen. In früheren Versionen musste der Helpdesk-Agent physisch auf dem Computer des Endbenutzers anwesend sein, um die Dart-Tools ausführen zu können.

Mit dem Assistenten können Sie auch die Willkommensnachricht für das Feature "Remoteverbindung" anpassen (die Meldung wird angezeigt, wenn Endbenutzer das Remoteverbindungstool ausführen). IT-Administratoren können auch konfigurieren, welche Port Nummer von der Remote Verbindung verwendet werden soll.

Weitere Informationen zum Dart- **Wiederherstellungsbild-Assistenten** oder zur Remote Verbindung finden Sie unter [Erstellen des DART 7,0-Wiederherstellungsabbilds](creating-the-dart-70-recovery-image-dart-7.md).

### Dart 7 ISO-Bereitstellung

Neben dem Brennen auf eine CD oder DVD fügt DaRT7 drei neue Optionen hinzu, wenn Sie die ISO-Datei bereitstellen, die das DART-Wiederherstellungsabbild enthält:

-   Bereitstellung von USB-Flashlaufwerken

-   Bereitstellung von Remote Partitionen

-   Bereitstellung der Wiederherstellungspartition

Mit der Deployment-Option für das USB-Flashlaufwerk kann ein Unternehmen Dart auf Computern verwenden, auf denen keine CD-oder DVD-Laufwerke verfügbar sind. Die Optionen für die Wiederherstellung und die Remotepartition ermöglichen Endbenutzern den einfachen Zugriff auf das DART-Bild und die Remote Verbindungsfunktion.

Weitere Informationen zum Bereitstellen von DART-Wiederherstellungs Bildern finden Sie unter [Bereitstellen des DART 7,0-Wiederherstellungsabbilds](deploying-the-dart-70-recovery-image-dart-7.md).

## Verwandte Themen


[Erste Schritte mit DaRT 7.0](getting-started-with-dart-70-new-ia.md)

[Versionshinweise für DaRT 7.0](release-notes-for-dart-70-new-ia.md)

 

 





