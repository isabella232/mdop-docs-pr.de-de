---
title: So stellen Sie ein beschädigtes Laufwerk wieder her
description: So stellen Sie ein beschädigtes Laufwerk wieder her
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809616"
---
# So stellen Sie ein beschädigtes Laufwerk wieder her


Zum Wiederherstellen eines beschädigten Laufwerks, das von BitLocker geschützt ist, muss ein Helpdesk-Benutzer für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) eine Wiederherstellungsschlüssel-Paketdatei erstellen. Diese Paketdatei kann dann auf den Computer kopiert werden, auf dem sich das beschädigte Laufwerk befindet, und dann zum Wiederherstellen des Laufwerks verwendet. Gehen Sie wie folgt vor, um die erforderlichen Schritte auszuführen.

**Wichtig**  Um einen möglichen Datenverlust zu vermeiden, wird dringend empfohlen, dass Sie die Hilfe zu "reparieren-BDE" lesen und klar verstehen, wie Sie den Befehl verwenden, bevor Sie die folgenden Anweisungen ausführen.

 

**So stellen Sie ein beschädigtes Laufwerk wieder her**

1.  Wenn Sie das für die Wiederherstellung eines beschädigten Laufwerks erforderliche Wiederherstellungsschlüssel Paket erstellen möchten, starten Sie einen Webbrowser, und öffnen Sie die Website MBAM-Verwaltung und-Überwachung.

2.  Wählen Sie im linken Navigationsbereich **Drive Recovery** aus. Geben Sie den Domänennamen des Benutzers, den Benutzernamen, den Grund für die Freigabe des Laufwerks und die Wiederherstellungskennwort-ID des Benutzers ein.

    **Hinweis**  Wenn Sie Mitglied der Rolle "Helpdesk-Administratoren" sind, müssen Sie den Domänennamen oder Benutzernamen des Benutzers nicht eingeben.

     

3.  Klicken Sie auf **Übermitteln**. Der Wiederherstellungsschlüssel wird angezeigt.

4.  Klicken Sie auf **Speichern**, und wählen Sie dann **Wiederherstellungsschlüssel Paket**aus. Das Wiederherstellungsschlüssel Paket wird auf Ihrem Computer erstellt.

5.  Kopieren Sie das Wiederherstellungsschlüssel Paket auf den Computer mit dem beschädigten Laufwerk.

6.  Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten. Klicken Sie dazu auf **Start** , und geben Sie `cmd` im **Feld Programme und Dateien durchsuchen**ein. Klicken Sie mit der rechten Maustaste auf **cmd.exe** , und wählen Sie **als Administrator ausführen**aus.

7.  Geben Sie an der Eingabeaufforderung Folgendes ein:

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **Hinweis**  Ersetzen Sie das &lt; festgelegte Laufwerk &gt; durch ein verfügbares Festplattenlaufwerk, auf dem der freie Speicherplatz gleich oder größer als die Daten auf dem beschädigten Laufwerk ist. Daten auf dem beschädigten Laufwerk werden wiederhergestellt und auf das festgelegte Festplattenlaufwerk verschoben.

     

## Verwandte Themen


[Verwalten von BitLocker mit MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





