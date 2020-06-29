---
title: So stellen Sie ein beschädigtes Laufwerk wieder her
description: So stellen Sie ein beschädigtes Laufwerk wieder her
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804607"
---
# So stellen Sie ein beschädigtes Laufwerk wieder her


Zum Wiederherstellen eines beschädigten Laufwerks, das von BitLocker geschützt wurde, muss ein Microsoft BitLocker-MBAM-Helpdesk-Benutzer eine Wiederherstellungsschlüssel-Paketdatei erstellen. Diese Paketdatei kann auf den Computer kopiert werden, auf dem sich das beschädigte Laufwerk befindet, und dann zum Wiederherstellen des Laufwerks verwendet. Gehen Sie dazu wie folgt vor, um dies zu erreichen:

**So stellen Sie ein beschädigtes Laufwerk wieder her**

1.  Öffnen Sie die MBAM-Verwaltungswebsite.

2.  Wählen Sie im Navigationsbereich **Drive Recovery** aus. Geben Sie den Domänennamen und den Benutzernamen des Benutzers, den Grund für die Freigabe des Laufwerks und die Wiederherstellungskennwort-ID des Benutzers ein.

    **Hinweis**  Wenn Sie Mitglied der Rolle "Helpdesk-Administratoren" sind, müssen Sie den Domänennamen oder Benutzernamen des Benutzers nicht eingeben.

     

3.  Klicken Sie auf **Übermitteln**. Der Wiederherstellungsschlüssel wird angezeigt.

4.  Klicken Sie auf **Speichern**, und wählen Sie dann **Wiederherstellungsschlüssel Paket**aus. Das Wiederherstellungsschlüssel Paket wird auf Ihrem Computer erstellt.

5.  Kopieren Sie das Wiederherstellungsschlüssel Paket auf den Computer mit dem beschädigten Laufwerk.

6.  Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten. Klicken Sie dazu auf **Start** , und geben Sie `cmd` im Feld **Programme und Dateien durchsuchen** ein. Klicken Sie in der Liste mit den Suchergebnissen mit der rechten Maustaste auf **cmd.exe** , und wählen Sie **als Administrator ausführen**aus.

7.  Geben Sie an der Eingabeaufforderung Folgendes ein:

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    **Hinweis**  &lt;Geben Sie für das festgelegte Laufwerk &gt; im Befehl ein verfügbares Speichergerät an, auf dem der freie Speicherplatz gleich oder größer als die Daten auf dem beschädigten Laufwerk ist. Daten auf dem beschädigten Laufwerk werden wiederhergestellt und auf das angegebene festgelegte Laufwerk verschoben.

     

## Verwandte Themen


[Verwalten von BitLocker mit MBAM](performing-bitlocker-management-with-mbam.md)

 

 





