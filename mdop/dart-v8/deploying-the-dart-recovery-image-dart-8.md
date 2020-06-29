---
title: Bereitstellen der DaRT-Recovery-Images
description: Bereitstellen der DaRT-Recovery-Images
author: dansimp
ms.assetid: df5cb54a-be8c-4ed2-89ea-d3c67c2ef4d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e445873324f005455ba3c96319847dea8ba761ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810360"
---
# Bereitstellen der DaRT-Recovery-Images


Nachdem Sie die Datei für die internationale Organisation für Standardisierung (ISO) erstellt haben, die das Microsoft Diagnostics and Recovery Toolset (Dart) 8,0-Wiederherstellungsabbild enthält, können Sie das Dart 8,0-Wiederherstellungsabbild im gesamten Unternehmen bereitstellen, damit es für Endbenutzer und Helpdesk-Mitarbeiter zur Verfügung steht. Es gibt vier unterstützte Methoden, mit denen Sie das DART-Wiederherstellungsbild bereitstellen können. Informationen zum Überprüfen der vor-und Nachteile der einzelnen Methoden finden Sie unter [Planen des Speicherns und Bereitstellen des Dart 8,0-Wiederherstellungsabbilds](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

Brennen der ISO-Abbilddatei auf eine CD oder DVD mithilfe des DART-Wiederherstellungs-Bild-Assistenten

Speichern des Inhalts der ISO-Abbilddatei auf einem USB-Flash Laufwerk (USB-Stick) mithilfe des DART-Wiederherstellungs-Bild-Assistenten

Extrahieren Sie die Datei "Boot. wim" aus dem ISO-Abbild, und stellen Sie Sie als Remotepartition bereit, die für Endbenutzercomputer verfügbar ist.

Extrahieren der Datei "Boot. wim" aus dem ISO-Abbild und Bereitstellen in der Wiederherstellungspartition einer neuen Windows 8-Installation

**Wichtig**  Der **Dart-Wiederherstellungs-Bild-Assistent** bietet die Möglichkeit, das Bild auf eine CD, DVD oder ein USB-Laufwerk zu brennen, aber die anderen Methoden zum Speichern und Bereitstellen des Wiederherstellungsabbilds erfordern zusätzliche Schritte, die Tools beinhalten, die nicht in DART enthalten sind. In diesem Abschnitt finden Sie einige Anleitungen und Links zu diesen anderen Methoden.

 

## Bereitstellen des DART-Wiederherstellungs Bilds als Teil einer Wiederherstellungspartition


Nachdem Sie den Dart-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Wiederherstellungspartition in einem Windows 8-Abbild bereitstellen.

[So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-8.md)

## Bereitstellen des DART-Wiederherstellungs Bilds als Remotepartition


Sie können das Wiederherstellungsabbild auf einem zentralen Netzwerk-Start Server wie Windows-Bereitstellungsdienste hosten und Benutzern oder Supportmitarbeitern die Möglichkeit geben, das Bild bei Bedarf auf Computer zu streamen.

[Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-8.md)

## Weitere Ressourcen für die Bereitstellung des DART-Wiederherstellungs Bilds


[Bereitstellen von DaRT 8.0](deploying-dart-80-dart-8.md)

 

 





