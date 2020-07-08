---
title: Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0
description: Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804391"
---
# Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0


Nachdem Sie die Datei für die internationale Organisation für Standardisierung (ISO) erstellt haben, die das Wiederherstellungsabbild Microsoft Diagnostics and Recovery Toolset (Dart) 7 enthält, können Sie das DART-Wiederherstellungsabbild im gesamten Unternehmen bereitstellen, damit es für Endbenutzer und Helpdesk-Agents verfügbar ist. Es gibt vier unterstützte Methoden, mit denen Sie das DART-Wiederherstellungsbild bereitstellen können.

-   Brennen der ISO-Abbilddatei auf eine CD oder DVD

-   Speichern des Inhalts der ISO-Abbilddatei auf einem USB-Flash Laufwerk

-   Extrahieren Sie die Datei "Boot. wim" aus dem ISO-Abbild, und stellen Sie Sie als Remotepartition bereit, die für Endbenutzercomputer verfügbar ist.

-   Extrahieren der Datei "Boot. wim" aus dem ISO-Abbild und Bereitstellen in der Wiederherstellungspartition einer neuen Windows 7-Installation

**Wichtig**  Der **Dart-Wiederherstellungsbild-Assistent** bietet nur die Option zum Brennen einer CD oder DVD. Alle anderen Methoden zum Speichern und Bereitstellen des Wiederherstellungsabbilds erfordern zusätzliche Schritte, die Tools beinhalten, die nicht in DART enthalten sind. In diesem Abschnitt finden Sie einige Anleitungen und Links zu diesen anderen Methoden.

 

## Bereitstellen des DART-Wiederherstellungs Bilds mithilfe eines USB-Flash Laufwerks


Nachdem Sie den Bild-Assistenten für die Dart-Wiederherstellung ausgeführt haben, können Sie das Tool unter verwenden, um <https://go.microsoft.com/fwlink/?LinkId=218888> die ISO-Bilddatei auf ein USB-Flashlaufwerk (USB-Stick) zu kopieren.

[So stellen Sie das DaRT-Wiederherstellungsabbild über ein USB-Flashlaufwerk bereit](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## Bereitstellen des DART-Wiederherstellungs Bilds als Teil einer Wiederherstellungs Partition


Nachdem Sie den Dart-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Wiederherstellungspartition in einem Windows 7-Abbild bereitstellen.

[So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## Bereitstellen des DART-Wiederherstellungs Bilds als Remote Partition


Nachdem Sie den Dart-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Remotepartition im Netzwerk bereitstellen.

[Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## Weitere Ressourcen zum Verwalten der Bereitstellung des DART-Wiederherstellungs Bilds


-   [Bereitstellen von DaRT 7.0](deploying-dart-70-new-ia.md)

 

 





