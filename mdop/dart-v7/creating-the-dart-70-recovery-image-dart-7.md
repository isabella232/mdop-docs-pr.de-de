---
title: Erstellen des DaRT 7.0-Wiederherstellungsabbilds
description: Erstellen des DaRT 7.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809862"
---
# Erstellen des DaRT 7.0-Wiederherstellungsabbilds


Microsoft Diagnostics and Recovery Toolset (Dart) 7 umfasst den **Dart-Wiederherstellungs-Bild-Assistenten** , der in Windows zum Erstellen einer startbaren internationalen Organisation für Standardisierungs-Images (ISO) verwendet wird. Bei einem ISO-Bild handelt es sich um eine Datei, die den unformatierten Inhalt einer CD darstellt.

## Verwenden des DART-Wiederherstellungsbild-Assistenten zum Erstellen des Wiederherstellungs Bilds


Die vom Dart-Wiederherstellungsbild-Assistenten erstellte ISO-Datei enthält das DART-Wiederherstellungsbild, mit dem Sie auf einen Problem Computer booten können, auch wenn es sonst nicht gestartet werden kann. Nachdem Sie den Computer in DART gestartet haben, können Sie die verschiedenen Dart-Tools ausführen, um zu versuchen, den Computer zu diagnostizieren und zu reparieren.

Sie können die ISO auf eine beschreibbare CD oder DVD schreiben, Sie auf einem USB-Stick speichern oder in einem Format speichern, das Sie zum Booten von DART von einer Remotepartition oder einer Wiederherstellungspartition verwenden können. Weitere Informationen finden Sie unter [Bereitstellen des DART 7,0-Wiederherstellungsabbilds](deploying-the-dart-70-recovery-image-dart-7.md).

**Hinweis**  Wenn Ihr Computer ein CD-RW-Laufwerk enthält, bietet der Assistent an, das ISO-Abbild auf eine leere CD oder DVD zu brennen. Wenn auf Ihrem Computer kein vom Assistenten unterstütztes Laufwerk enthalten ist, können Sie das ISO-Abbild auf eine CD oder DVD brennen, indem Sie die meisten Programme verwenden, die eine CD oder DVD brennen können.

 

Zum Erstellen einer startbaren CD oder DVD aus dem ISO-Abbild benötigen Sie Folgendes:

-   Ein CD-RW-Laufwerk.

-   Eine beschreibbare CD oder DVD (in einem vom beschreibbaren Laufwerk unterstützten Format).

-   Software, die das beschreibbare Laufwerk unterstützt und das Brennen eines ISO-Images direkt auf CD oder DVD unterstützt.

    **Wichtig**  Testen Sie die CD oder DVD, die Sie erstellen, auf allen verschiedenen Arten von Computern, die Sie unterstützen möchten, weil einige Computer nicht von allen Arten von beschreibbaren Medien gestartet werden können.

     

Um das ISO-Abbild auf einem USB-Flashlaufwerk (USB-Stick) zu speichern, müssen Sie Folgendes haben:

-   Ein korrekt formatiertes USB-Laufwerk.

-   Ein Programm, das Sie zum Bereitstellen des ISO-Images verwenden können.

[So verwenden Sie den Assistent für DaRT-Wiederherstellungsabbilder zum Erstellen des Wiederherstellungsabbilds](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## Erstellen eines zeitlimitierten Wiederherstellungs Bilds


Sie können ein DART-Wiederherstellungsbild erstellen, das nur für eine bestimmte Anzahl von Tagen nach der Generierung verwendet werden kann. Dazu müssen Sie den **Dart-Wiederherstellungsbild-Assistenten** an einer Eingabeaufforderung ausführen und die Anzahl der Tage angeben.

[So erstellen Sie ein zeitlich begrenztes Wiederherstellungsabbild](how-to-create-a-time-limited-recovery-image-dart-7.md)

## Weitere Ressourcen zum Erstellen des DaRT7-Wiederherstellungs Bilds


-   [Bereitstellen von DaRT 7.0](deploying-dart-70-new-ia.md)

 

 





