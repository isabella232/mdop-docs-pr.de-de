---
title: Informationen zu DaRT 8.0
description: Informationen zu DaRT 8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808662"
---
# Informationen zu DaRT 8.0


Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 unterstützt Sie bei der Problembehandlung und Reparatur von Windows-basierten Computern. Dazu gehören die Computer, die nicht gestartet werden können. Dart 8,0 ist ein leistungsfähiger Satz von Tools, die die Windows-Wiederherstellungsumgebung (WinRE) erweitern. Mithilfe von DART können Sie ein Problem analysieren, um dessen Ursache zu ermitteln, beispielsweise indem Sie das Ereignisprotokoll oder die Systemregistrierung des Computers überprüfen. DART unterstützt die Wiederherstellung von grundlegenden Festplatten, die Partitionen enthalten, beispielsweise primäre Partitionen und logische Laufwerke, und unterstützt die Wiederherstellung von Volumes.

**Hinweis**  DART unterstützt die Wiederherstellung von dynamischen Datenträgern nicht.

 

DART bietet auch Tools, mit denen Sie ein Problem beheben können, sobald Sie die Ursache ermitteln. So können Sie beispielsweise die Tools in DART verwenden, um einen fehlerhaften Gerätetreiber zu deaktivieren, Hotfixes zu entfernen, gelöschte Dateien wiederherzustellen und den Computer auf Malware zu überprüfen, auch wenn Sie das installierte Windows-Betriebssystem nicht starten können oder sollten.

Dart kann Ihnen dabei helfen, Computer mit einer 32-Bit-oder 64-Bit-Version von Windows 8 schnell wiederherzustellen, und zwar in der Regel in kürzerer Zeit, als wenn Sie den Computer umbilden würden.

Mit der Funktion in DART können Sie ein Wiederherstellungsabbild erstellen. Das Wiederherstellungsabbild startet die Windows-Wiederherstellungsumgebung (Windows RE), auf der Sie das Fenster **Diagnose-und Wiederherstellungs-Toolset** starten und auf die Dart-Tools zugreifen können.

Verwenden Sie den **Dart-Wiederherstellungsbild-Assistenten** zum Erstellen des DART-Wiederherstellungs Bilds. Standardmäßig erstellt der Assistent eine Image-Datei für die internationale Organisation für Standardisierung (ISO) und eine WIM-Datei (Windows Imaging Format) und ermöglicht das Brennen des Bilds auf eine CD, DVD oder USB. Sie können das Bild lokal auf den Computern des Endbenutzers bereitstellen, oder Sie können es von einer Remotenetzwerk Partition oder einer Wiederherstellungspartition auf der lokalen Festplatte bereitstellen.

## <a href="" id="what-s-new-in-dart-8-0"></a>Neuerungen in Dart 8,0


Dart 8,0 kann Ihnen dabei helfen, Computer mit einer 32-Bit-oder 64-Bit-Version von Windows 8 schnell wiederherzustellen, in der Regel in kürzerer Zeit, als es für die Neubildung des Computers dauern würde. Dart 8,0 verfügt über die folgenden neuen Features.

### Erstellen von DART-Bildern mithilfe von Windows 8 oder Windows Server 2012

Dart 8,0 ermöglicht Ihnen, Dart-Bilder mithilfe von Windows® 8 oder Windows Server® 2012 zu erstellen. Für Windows-Versionen, die älter als Windows 8 und Windows Server 2012 sind, sollten Kunden weiterhin frühere Versionen von DART verwenden.

### Generieren von 32-und 64-Bit-Bildern auf einem Computer

Dart 8,0 ermöglicht Ihnen, sowohl 32-Bit-als auch 64-Bit-Bilder von einem einzelnen Computer zu generieren, auf dem Dart ausgeführt wird, unabhängig davon, ob es sich bei dem Computer um einen 32-Bit-oder 64-Bit-Computer handelt. In DaRT7 musste das erstellte Bild identisch sein, wie der Computer, auf dem Dart ausgeführt wurde.

### Erstellen eines Bilds, das Computer unterstützt, die über eine BIOS-oder UEFI-Schnittstelle verfügen

Die Unterstützung von Dart 8.0 für die Unified Extensible Firmware Interface (UEFI)-und BIOS-Schnittstellen ermöglicht es Ihnen, nur ein Bild zu erstellen, das mit Computern mit einer der beiden Schnittstellen funktioniert.

### Verwenden einer GUID-Partitionstabelle (GPT) für die Partitionierung

Dart 8,0-Tools unterstützen jetzt Windows 8 GPT-Datenträger, die einen flexibleren Mechanismus für die Partitionierung von Datenträgern bereitstellen, als das MBR-Partitionierungsschema (Master Boot Record). Dart 8,0-Tools unterstützen weiterhin die MBR-Partitionierung.

### Installieren von Windows 8 und Windows Server 2012 auf der lokalen Festplatte

Dart 8,0-Tools können nur verwendet werden, wenn Windows 8 und Windows Server 2012 auf der lokalen Festplatte installiert sind. Derzeit gibt es keine Unterstützung für Windows to go.

### <a href="" id="-------------dart-8-0-release-notes"></a> Dart 8,0-Versionshinweise

Weitere Informationen und aktuelle Nachrichten, die nicht in die Dokumentation eingehen, finden Sie in den Versionshinweisen [zu Dart 8,0](release-notes-for-dart-80--dart-8.md).

## So erhalten Sie Dart 8,0


Diese Technologie ist Teil des Microsoft Desktop Optimization Pack (MDOP). MDOP ist Teil von Microsoft Software Assurance. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Verwandte Themen


[Erste Schritte mit DaRT 8.0](getting-started-with-dart-80-dart-8.md)

[Versionshinweise für DaRT 8.0](release-notes-for-dart-80--dart-8.md)

 

 





