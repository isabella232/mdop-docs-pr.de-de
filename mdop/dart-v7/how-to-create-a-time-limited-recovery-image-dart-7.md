---
title: So erstellen Sie ein zeitlich begrenztes Wiederherstellungsabbild
description: So erstellen Sie ein zeitlich begrenztes Wiederherstellungsabbild
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804373"
---
# So erstellen Sie ein zeitlich begrenztes Wiederherstellungsabbild


Sie können ein DART-Wiederherstellungsbild erstellen, das nur für eine bestimmte Anzahl von Tagen nach der Generierung verwendet werden kann. Dazu müssen Sie den **Dart-Wiederherstellungsbild-Assistenten** an einer Eingabeaufforderung ausführen und die Anzahl der Tage angeben.

**So erstellen Sie ein Wiederherstellungsbild mit einem Zeitlimit**

1.  Öffnen Sie eine Eingabeaufforderung mit Administratoranmeldeinformationen.

2.  Ändern Sie das Verzeichnis in den Speicherort des ERDC.exe-Programms.

3.  Führen Sie mit der folgenden Syntax den **Dart-Wiederherstellungsbild-Assistenten**aus. *NumberOfDays* ist eine positive ganze Zahl, die die Anzahl der Tage darstellt, für die das DART-Wiederherstellungsbild verwendet werden kann.

    ``` syntax
    ERDC /e NumberOfDays
    ```

## Verwandte Themen


[Erstellen des DaRT 7.0-Wiederherstellungsabbilds](creating-the-dart-70-recovery-image-dart-7.md)

 

 





