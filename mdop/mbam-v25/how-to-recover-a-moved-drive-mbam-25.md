---
title: So stellen Sie ein verschobenes Laufwerk wieder her
description: So stellen Sie ein verschobenes Laufwerk wieder her
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809898"
---
# So stellen Sie ein verschobenes Laufwerk wieder her
In diesem Thema wird die Verwendung der Website "Verwaltung und Überwachung" (auch als "Helpdesk" bezeichnet) zum Wiederherstellen eines Betriebssystemlaufwerks erläutert, das nach dem Verschlüsseln durch die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verschoben wurde. Wenn ein Laufwerk verschoben wird, akzeptiert es nicht mehr die PIN, die auf dem vorherigen Computer verwendet wurde, da sich der TPM-Chip (Trusted Platform Module) geändert hat. Zum Wiederherstellen des verschobenen Laufwerks müssen Sie die Wiederherstellungsschlüssel-ID abrufen, um das Wiederherstellungskennwort abzurufen.

Zum Wiederherstellen eines verschobenen Laufwerks müssen Sie den Bereich **Drive Recovery** der Website Verwaltung und Überwachung verwenden. Für den Zugriff auf den **Laufwerk Wiederherstellungs** Bereich müssen Sie der Rolle MBAM Helpdesk-Benutzer oder der MBAM Advanced Helpdesk-Benutzerrolle zugewiesen sein. Weitere Informationen zu diesen Rollen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

**So stellen Sie ein verschobenes Laufwerk wieder her**
1.  Starten Sie den Computer auf dem Computer, auf dem sich das verschobene Laufwerk befindet, im Windows Recovery Environment (WinRE)-Modus, oder starten Sie den Computer mit dem Microsoft Diagnostic and Recovery Toolset (Dart).

2.  Nachdem der Computer mit WinRE oder Dart gestartet wurde, behandelt MBAM das verschobene Betriebssystemlaufwerk als festes Datenlaufwerk. MBAM zeigt dann die Wiederherstellungskennwort-ID des Laufwerks an und fragt nach dem Wiederherstellungskennwort.

    **Hinweis**  In einigen Fällen können Sie möglicherweise auf **Ich habe die PIN** während des Startvorgangs vergessen klicken und dann in den Wiederherstellungsmodus wechseln, um die Wiederherstellungsschlüssel-ID anzuzeigen.

     

3.  Verwenden Sie die Wiederherstellungsschlüssel-ID, um das Wiederherstellungskennwort abzurufen, und Entsperren Sie das Laufwerk über die Website Verwaltung und Überwachung. Anweisungen hierzu finden Sie unter [Wiederherstellen eines Laufwerks im Wiederherstellungsmodus](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).

    Wenn das verschobene Laufwerk für die Verwendung eines TPM-Chips auf dem ursprünglichen Computer konfiguriert wurde, führen Sie die folgenden zusätzlichen Schritte aus. Andernfalls ist der Wiederherstellungsvorgang abgeschlossen.

4.  Öffnen Sie nach dem Entsperren des Laufwerks und dem Abschluss des Startvorgangs eine Eingabeaufforderung im WinRE-Modus, und verwenden Sie den `manage-bde` Befehl zum Entschlüsseln des Laufwerks. Die Verwendung dieses Tools ist die einzige Möglichkeit, das TPM und die PIN-Beschützer ohne den ursprünglichen TPM-Chip zu entfernen. Informationen zum `manage-bde` Befehl finden Sie unter [manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).

5.  Wenn die Entfernung abgeschlossen ist, starten Sie den Computer in der Regel. Der MBAM-Agent setzt nun die Richtlinie zum Verschlüsseln des Laufwerks mit dem TPM des neuen Computers und der PIN durch.



## Verwandte Themen


[Durchführen der BitLocker-Verwaltung mit MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





