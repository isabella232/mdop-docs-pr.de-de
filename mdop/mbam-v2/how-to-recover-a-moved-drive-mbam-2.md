---
title: So stellen Sie ein verschobenes Laufwerk wieder her
description: So stellen Sie ein verschobenes Laufwerk wieder her
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810930"
---
# So stellen Sie ein verschobenes Laufwerk wieder her


Wenn Sie ein Betriebssystemlaufwerk verschieben, das mithilfe von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verschlüsselt ist, akzeptiert das Laufwerk die PIN, die auf einem vorherigen Computer verwendet wurde, aufgrund der Änderung des TPM-Chips (Trusted Platform Module) nicht. Um das verschobene Laufwerk verwenden zu können, benötigen Sie eine Möglichkeit zum Abrufen der Wiederherstellungsschlüssel-ID, um das Wiederherstellungskennwort abzurufen. Gehen Sie wie folgt vor, um ein Laufwerk wiederherzustellen, das verschoben wurde.

**So stellen Sie ein verschobenes Laufwerk wieder her**

1.  Starten Sie den Computer auf dem Computer, auf dem sich das verschobene Laufwerk befindet, im Windows Recovery Environment (WinRE)-Modus, oder starten Sie den Computer mit dem Microsoft Diagnostic and Recovery Toolset (Dart).

2.  Nachdem der Computer mit WinRE oder Dart gestartet wurde, behandelt die Microsoft BitLocker-Verwaltung und-Überwachung das verschobene Betriebssystemlaufwerk als Datenlaufwerk. MBAM zeigt dann die Wiederherstellungskennwort-ID des Laufwerks an und fragt nach dem Wiederherstellungskennwort.

    **Hinweis**  In einigen Fällen können Sie möglicherweise auf **Ich habe die PIN** während des Startvorgangs vergessen klicken und dann in den Wiederherstellungsmodus wechseln, um die Wiederherstellungsschlüssel-ID anzuzeigen.

     

3.  Verwenden Sie die Wiederherstellungsschlüssel-ID, um das Wiederherstellungskennwort abzurufen, und Entsperren Sie das Laufwerk über die Websiteverwaltung und Überwachung.

4.  Wenn das verschobene Laufwerk für die Verwendung eines TPM-Chips auf dem ursprünglichen Computer konfiguriert wurde, müssen Sie nach dem Entsperren des Laufwerks und Abschließen des Startvorgangs weitere Schritte Unternehmen. Öffnen Sie im WinRE-Modus eine Eingabeaufforderung, und verwenden Sie das Tool **manage-bde** , um das Laufwerk zu entschlüsseln. Die Verwendung dieses Tools ist die einzige Möglichkeit, die TPM plus-PIN-Beschützer ohne den ursprünglichen TPM-Chip zu entfernen.

5.  Starten Sie den Computer nach Abschluss des Umzugs in der Regel. Der MBAM-Agent setzt nun die Richtlinie zum Verschlüsseln des Laufwerks mit der TPM-plus-PIN des neuen Computers durch.

## Verwandte Themen


[Verwalten von BitLocker mit MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





