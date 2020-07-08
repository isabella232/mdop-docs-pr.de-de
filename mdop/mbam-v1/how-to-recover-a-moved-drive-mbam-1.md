---
title: So stellen Sie ein verschobenes Laufwerk wieder her
description: So stellen Sie ein verschobenes Laufwerk wieder her
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804595"
---
# So stellen Sie ein verschobenes Laufwerk wieder her


Wenn Sie ein Betriebssystemlaufwerk verschieben, das zuvor mithilfe von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verschlüsselt wurde, müssen Sie bestimmte Probleme beheben. Nachdem eine PIN an den neuen Computer angefügt wurde, akzeptiert das Laufwerk nicht die Start-PIN, die auf dem vorherigen Computer verwendet wurde. Das System hält die PIN wegen der Änderung des TPM-Chips (Trusted Platform Module) für ungültig. Sie müssen eine Wiederherstellungsschlüssel-ID abrufen, um das Wiederherstellungskennwort abzurufen, um das verschobene Laufwerk verwenden zu können. Gehen Sie dazu wie folgt vor:

**So stellen Sie ein verschobenes Laufwerk wieder her**

1.  Starten Sie auf dem Computer, auf dem sich das verschobene Laufwerk befindet, im Windows Recovery Environment (WinRE)-Modus, oder starten Sie den Computer mithilfe des Microsoft Diagnostics and Recovery Toolset (Dart).

2.  Nachdem der Computer mit WinRE oder Dart gestartet wurde, behandelt MBAM das verschobene Betriebssystemlaufwerk als Datenlaufwerk. MBAM zeigt dann die Wiederherstellungskennwort-ID des Laufwerks an und fragt nach dem Wiederherstellungskennwort.

    **Hinweis**  In einigen Fällen können Sie möglicherweise auf **Ich vergesse die PIN** während des Startvorgangs klicken, um in den Wiederherstellungsmodus zu wechseln. Außerdem wird die Wiederherstellungsschlüssel-ID angezeigt.

     

3.  Verwenden Sie auf der MBAM-Verwaltungswebsite die Wiederherstellungsschlüssel-ID, um das Wiederherstellungskennwort abzurufen und das Laufwerk zu entsperren.

4.  Wenn das verschobene Laufwerk für die Verwendung eines TPM-Chips auf dem ursprünglichen Computer konfiguriert wurde, müssen Sie nach dem Entsperren des Laufwerks weitere Schritte Unternehmen und den Startvorgang abschließen. Öffnen Sie im WinRE-Modus eine Eingabeaufforderung, und verwenden Sie das Tool **manage-bde** , um das Laufwerk zu entschlüsseln. Die Verwendung dieses Tools ist die einzige Möglichkeit, den TPM-plus-PIN-Schutz ohne den ursprünglichen TPM-Chip zu entfernen.

5.  Nachdem der Vorgang abgeschlossen ist, starten Sie das System normal. Der MBAM-Agent setzt die Richtlinie zum Verschlüsseln des Laufwerks mit der TPM-plus-PIN des neuen Computers durch.

## Verwandte Themen


[Verwalten von BitLocker mit MBAM](performing-bitlocker-management-with-mbam.md)

 

 





