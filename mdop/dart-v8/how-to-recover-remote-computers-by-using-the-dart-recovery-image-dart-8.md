---
title: So stellen Sie Remotecomputer mit dem DaRT-Wiederherstellungsabbild wieder her
description: So stellen Sie Remotecomputer mit dem DaRT-Wiederherstellungsabbild wieder her
author: dansimp
ms.assetid: 363ccd48-6820-4b5b-a43a-323c0b208a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b3e3155dbea8da18338b8a167d22f73b1c8e4bb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810531"
---
# So stellen Sie Remotecomputer mit dem DaRT-Wiederherstellungsabbild wieder her


Verwenden Sie das Feature Remoteverbindung in Microsoft Diagnostics and Recovery Toolset (Dart) 8,0, um die Dart-Tools Remote auf einem Endbenutzercomputer auszuführen. Nachdem der Endbenutzer bestimmte Informationen dem Administrator oder Helpdesk-Mitarbeiter zur Verfügung gestellt hat, kann der IT-Administrator oder der Helpdesk-Mitarbeiter die Kontrolle über den Computer des Endbenutzers übernehmen und die erforderlichen Dart-Tools Remote ausführen.

Wenn Sie die Dart-Tools beim Erstellen des Wiederherstellungsabbilds deaktiviert haben, können Sie weiterhin auf alle Tools zugreifen. Alle Tools, mit Ausnahme der Remote Verbindung, stehen Endbenutzern nicht zur Verfügung.

**So stellen Sie einen Remotecomputer mithilfe des DART-Wiederherstellungs Bilds wieder her**

1.  Starten Sie einen Endbenutzercomputer mithilfe des DART-Wiederherstellungs Bilds.

    In der Regel verwenden Sie eine der folgenden Methoden, um in DART zu booten, um einen Remotecomputer wiederherzustellen, je nachdem, wie das DART-Wiederherstellungsabbild bereitgestellt wird. Weitere Informationen zum Bereitstellen des DART-Wiederherstellungs Bilds finden Sie unter [Bereitstellen von Dart 8,0](deploying-dart-80-dart-8.md).

    -   Starten Sie DART von einer Wiederherstellungspartition auf dem Problem Computer.

    -   Starten Sie DART von einer Remotepartition im Netzwerk.

    Informationen zu den vor-und Nachteilen der einzelnen Methoden finden Sie unter [Planen des Speicherns und Bereitstellen des Dart 8,0-Wiederherstellungsabbilds](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

    Unabhängig davon, welche Methode Sie zum Starten von DART verwenden, müssen Sie das Startgerät im BIOS für die Startoption oder die Optionen aktivieren, die Sie dem Endbenutzer zur Verfügung stellen möchten.

    **Hinweis:**  
    Je nach Art der Festplatte, Netzwerkadapter und anderer Hardware, die in Ihrer Organisation verwendet wird, ist die Konfiguration des BIOS einzigartig.



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. Wenn Sie gefragt werden, ob Sie Netzwerkdienste initialisieren möchten, wählen Sie eine der folgenden Optionen aus:

   **Ja** – es wird davon ausgegangen, dass ein DHCP-Server im Netzwerk vorhanden ist, und es wird versucht, eine IP-Adresse vom Server abzurufen. Wenn das Netzwerk statische IP-Adressen statt DHCP verwendet, können Sie später das **TCP/IP-Konfigurations** Tool in DART verwenden, um eine statische IP-Adresse anzugeben.

   **Nein** – überspringen Sie den Netzwerk Initialisierungsprozess.

3. Geben Sie an, ob Sie die Laufwerkbuchstaben neu zuordnen möchten. Wenn Sie Windows Online ausführen, wird das System Volume in der Regel Laufwerk C zugeordnet. Wenn Sie jedoch Windows offline unter WinRE ausführen, wird das ursprüngliche System Volume möglicherweise einem anderen Laufwerk zugeordnet, was zu Verwirrung führen kann. Wenn Sie sich für die Neuzuordnung entscheiden, versucht Dart, die Offline Laufwerkbuchstaben den Online Laufwerkbuchstaben zuzuordnen. Eine Neuzuordnung wird nur ausgeführt, wenn ein Offline Betriebssystem später im Startvorgang ausgewählt wird.

4. Wählen Sie im Dialogfeld **System Wiederherstellungsoptionen** ein Tastaturlayout aus.

5. Überprüfen Sie das angezeigte Systemstammverzeichnis, die Art des installierten Betriebssystems und die Partitionsgröße. Wenn Ihr Betriebssystem nicht aufgeführt ist und Sie vermuten, dass das Fehlen von Treibern eine mögliche Ursache für den Fehler ist, klicken Sie auf **Treiber laden** , um die Verdächtigen Treiber zu laden, und legen Sie dann das Installationsmedium für das Gerät ein, und wählen Sie den Treiber aus.

6. Wählen Sie die Installation aus, die Sie reparieren oder diagnostizieren möchten, und klicken Sie dann auf **weiter**.

   **Hinweis:**  
   Wenn die Windows-Wiederherstellungsumgebung (WinRE) erkennt oder vermutet, dass Windows 8 beim letzten Versuch nicht ordnungsgemäß gestartet wurde, wird die **Startreparatur** möglicherweise automatisch gestartet. Informationen zum Beheben dieses Problems finden Sie unter [Problembehandlung bei Dart 8,0](troubleshooting-dart-80-dart-8.md).



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. Klicken Sie im Fenster **System Wiederherstellungsoptionen** auf **Microsoft-Diagnose-und Wiederherstellungs-Toolset** , um das **Toolset Diagnose und Wiederherstellung**zu öffnen.

8. Klicken Sie im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf **Remoteverbindung** , um das **Dart-Remote Verbindungs** Fenster zu öffnen. Wenn Sie aufgefordert werden, dem Helpdesk den Remotezugriff zu gewähren, klicken Sie auf **OK**.

   Das Fenster Dart-Remote Verbindung wird geöffnet, und es werden eine Ticketnummer, eine IP-Adresse und Portinformationen angezeigt.

9. Öffnen Sie auf dem Helpdesk-Computer die **Dart-Remote Verbindungsanzeige**.

10. Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Dart 8,0**, und klicken Sie dann auf **Dart Remote Connection Viewer**.

11. Geben Sie im Fenster **Dart Remote Connection** die erforderlichen Tickets, IP-Adressen und Portinformationen ein.

   **Hinweis:**  
   Diese Informationen werden auf dem Computer des Endbenutzers erstellt und müssen vom Endbenutzer bereitgestellt werden. Es können mehrere IP-Adressen zur Auswahl stehen, je nachdem, wie viele auf dem Endbenutzercomputer verfügbar sind.



12. Klicken Sie auf **Verbinden**.

Der IT-Administrator übernimmt nun die Kontrolle über den Computer des Endbenutzers und kann die Dart-Tools Remote ausführen.

**Hinweis:**  
Es wird eine Datei mit dem Namen inv32.xml und Remote Verbindungsinformationen wie Portnummer und IP-Adresse bereitgestellt. Standardmäßig befindet sich die Datei in der Regel unter%windir%\\system32.



**So passen Sie den Remote Verbindungsprozess an**

1. Sie können den Remote Verbindungsprozess anpassen, indem Sie die winpeshl.ini Datei bearbeiten. Weitere Informationen zum Bearbeiten der winpeshl.ini Datei finden Sie unter [Winpeshl.ini Dateien](https://go.microsoft.com/fwlink/?LinkId=219413).

   Geben Sie die folgenden Befehle und Parameter an, um das Einrichten einer Remoteverbindung mit einem Endbenutzercomputer anzupassen:

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Befehl</th>
   <th align="left">Parameter</th>
   <th align="left">Beschreibung</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>RemoteRecovery.exe</strong></p></td>
   <td align="left"><p>-nomessage</p></td>
   <td align="left"><p>Gibt an, dass die Bestätigungsaufforderung nicht angezeigt wird. <strong>Die Remote Verbindung </strong> wird fortgesetzt, als ob der Endbenutzer &quot; &quot; auf die Bestätigungsaufforderung "Ja" reagiert hat.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>WaitForConnection.exe</strong></p></td>
   <td align="left"><p>keine</p></td>
   <td align="left"><p>Verhindert, dass ein benutzerdefiniertes Skript fortgesetzt <strong> wird, bis entweder die Remote Verbindung </strong> nicht ausgeführt wird oder eine gültige Verbindung mit dem Endbenutzercomputer hergestellt wird.</p>
   <div class="alert">
   <strong>Wichtig</strong><br/><p>Dieser Befehl dient keine Funktion, wenn er unabhängig voneinander angegeben wird. Sie muss in einem Skript angegeben werden, damit Sie ordnungsgemäß funktioniert.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Der folgende Code ist ein Beispiel für eine winpeshl.ini-Datei, die so angepasst wird, dass das **Remote Verbindungs** Tool geöffnet wird, sobald versucht wird, in DART zu booten:

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

Wenn Dart gestartet wird, wird die Datei inv32.xml auf der RAM-Diskette in \\Windows\\System32\\ erstellt. Diese Datei enthält Verbindungsinformationen: IP-Adresse, Port und Ticketnummer. Sie können diese Datei auf eine Netzwerkfreigabe kopieren, um einen Helpdesk-Workflow auszulösen. Ein benutzerdefiniertes Programm kann beispielsweise die Netzwerkfreigabe für Verbindungsdateien überprüfen und dann ein Support Ticket erstellen oder e-Mail-Benachrichtigungen senden.

**So führen Sie die Remote Verbindungsanzeige an der Eingabeaufforderung aus**

1.  Wenn Sie die **Dart-Remote Verbindungsanzeige** an der Eingabeaufforderung ausführen möchten, geben Sie den Befehl **DartRemoteViewer.exe** an, und verwenden Sie die folgenden Parameter:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parameter</th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>-Ticket = &lt; <em> ticketnumber</em>&gt;</p></td>
    <td align="left"><p>Wobei &lt; <em> ticketnumber </em> &gt; die Ticketnummer ist, einschließlich der Striche, die von der Remote Verbindung generiert werden.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>-IPAddress = &lt; <em> IPAddress</em>&gt;</p></td>
    <td align="left"><p>Dabei &lt; <em> </em> &gt; ist IPAddress die IP-Adresse, die von der Remote Verbindung generiert wird.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>-Port = &lt; <em> Port</em>&gt;</p></td>
    <td align="left"><p>Wobei &lt; <em> Port </em> &gt; der Port ist, der der angegebenen IP-Adresse entspricht.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. Wenn alle drei Parameter angegeben sind und die Daten gültig sind, wird beim Starten des Programms sofort eine Verbindung versucht. Wenn ein Parameter ungültig ist, wird das Programm so gestartet, als ob keine Parameter angegeben wurden.

## Verwandte Themen


[Vorgänge für DaRT 8.0](operations-for-dart-80-dart-8.md)

[Wiederherstellen von Computern mithilfe von DaRT 8.0](recovering-computers-using-dart-80-dart-8.md)









