---
title: So stellen Sie ein beschädigtes Laufwerk wieder her
description: So stellen Sie ein beschädigtes Laufwerk wieder her
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809424"
---
# So stellen Sie ein beschädigtes Laufwerk wieder her


Sie können dieses Verfahren mit der Websiteverwaltung und Überwachung (auch als Helpdesk bezeichnet) verwenden, um ein beschädigtes Laufwerk wiederherzustellen, das durch BitLocker geschützt ist. Führen Sie dazu die Aufgaben aus, die in der folgenden Tabelle beschrieben sind.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Details und weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Erstellen Sie eine Wiederherstellungs Schlüsselpaket-Datei, indem Sie auf den <strong> Bereich Drive Recovery </strong> der Verwaltungs-und Überwachungs Website zugreifen.</p></td>
<td align="left"><p>Für den Zugriff auf den <strong> Laufwerk Wiederherstellungs </strong> Bereich müssen Sie der Rolle MBAM Helpdesk-Benutzer oder der MBAM Advanced Helpdesk-Benutzerrolle zugewiesen sein. Sie haben diesen Rollen möglicherweise unterschiedliche Namen gegeben, als Sie Sie erstellt haben. Weitere Informationen finden Sie unter <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> Planen von MBAM 2,5-Gruppen und-Konten </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kopieren Sie die Paketdatei auf den Computer, auf dem sich das beschädigte Laufwerk befindet.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwenden Sie den <code>repair-bde</code> Befehl, um den Wiederherstellungsvorgang abzuschließen.</p></td>
<td align="left"><p>Um einen möglichen Datenverlust zu vermeiden, wird dringend empfohlen, den <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> Befehl manage-bde zu überprüfen, </a> bevor Sie ihn verwenden.</p></td>
</tr>
</tbody>
</table>

 

**So stellen Sie ein beschädigtes Laufwerk wieder her**

1.  Öffnen Sie einen Webbrowser, und navigieren Sie zur **Website Verwaltung und Überwachung**.

2.  Wählen Sie im linken Bereich **Drive Recovery** aus, um die Seite **Wiederherstellen des Zugriffs auf eine verschlüsselte Festplatte** zu öffnen.

3.  Geben Sie die Windows-Anmeldedomäne und den Benutzernamen des Endbenutzers, den Grund für die Freigabe des Laufwerks und die Wiederherstellungskennwort-ID des Endbenutzers ein.

    **Hinweis**  Wenn Sie Mitglied der Gruppe "Erweiterte Helpdesk-Benutzer" sind, müssen Sie den Domänennamen oder Benutzernamen des Benutzers nicht eingeben.

     

4.  Klicken Sie auf **Übermitteln**. Der Wiederherstellungsschlüssel wird angezeigt.

5.  Klicken Sie auf **Speichern**, und wählen Sie dann **Wiederherstellungsschlüssel Paket**aus. Das Wiederherstellungsschlüssel Paket wird auf Ihrem Computer erstellt.

6.  Kopieren Sie das Wiederherstellungsschlüssel Paket auf den Computer mit dem beschädigten Laufwerk.

7.  Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten. Klicken Sie dazu auf **Start** , und geben Sie `cmd` das Textfeld **Programme und Dateien durchsuchen** ein. Klicken Sie mit der rechten Maustaste auf **cmd.exe**, und wählen Sie **als Administrator ausführen**aus.

8.  Geben Sie an der Eingabeaufforderung Folgendes ein:

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **Hinweis**  Ersetzen Sie das &lt; *festgelegte Laufwerk* &gt; durch ein verfügbares Festplattenlaufwerk, auf dem der freie Speicherplatz gleich oder größer als die Daten auf dem beschädigten Laufwerk ist. Daten auf dem beschädigten Laufwerk werden wiederhergestellt und auf das festgelegte Festplattenlaufwerk verschoben.

     


## Verwandte Themen


[Durchführen der BitLocker-Verwaltung mit MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





