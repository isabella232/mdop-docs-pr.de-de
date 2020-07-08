---
title: So stellen Sie Remotecomputer mithilfe des DaRT-Wiederherstellungsabbilds wieder her
description: So stellen Sie Remotecomputer mithilfe des DaRT-Wiederherstellungsabbilds wieder her
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809568"
---
# So stellen Sie Remotecomputer mithilfe des DaRT-Wiederherstellungsabbilds wieder her


Mit dem Feature Remote Verbindung in Microsoft Diagnostics and Recovery Toolset (Dart) 7 können IT-Administratoren die Dart-Tools Remote auf einem Endbenutzercomputer ausführen. Nachdem der Endbenutzer bestimmte Informationen bereitgestellt hat (oder von einem Helpdesk-Mitarbeiter, der auf dem Endbenutzercomputer arbeitet), kann der IT-Administrator oder Helpdesk-Agent den Computer des Endbenutzers Steuern und die erforderlichen Dart-Tools Remote ausführen.

**Wichtig**  
Die beiden Computer, die eine Remoteverbindung herstellen, müssen Teil desselben Netzwerks sein.



**So stellen Sie einen Remotecomputer mithilfe von DART wieder her**

1.  Starten Sie einen Endbenutzercomputer mithilfe des DART-Wiederherstellungs Bilds.

    In der Regel verwenden Sie eine der folgenden Methoden, um in DART zu booten, um einen Remotecomputer wiederherzustellen, je nachdem, wie das DART-Wiederherstellungsabbild bereitgestellt wird. Weitere Informationen zum Bereitstellen des DART-Wiederherstellungs Bilds finden Sie unter [Bereitstellen des DART 7,0-Wiederherstellungs](deploying-the-dart-70-recovery-image-dart-7.md)Abbilds.

    -   Starten Sie DART von einer Wiederherstellungspartition auf dem Problem Computer.

    -   Starten Sie DART von einer Remotepartition im Netzwerk.

    Informationen zu den vor-und Nachteilen der einzelnen Methoden finden Sie unter [Planen des Speicherns und Bereitstellen des DART 7,0-Wiederherstellungsabbilds](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).

    Unabhängig davon, welche Methode Sie zum Starten von DART verwenden, müssen Sie das Startgerät im BIOS für die Startoption oder die Optionen aktivieren, die Sie dem Endbenutzer zur Verfügung stellen möchten.

    **Hinweis:**  
    Je nach Art der Festplatte, Netzwerkadapter und anderer Hardware, die in Ihrer Organisation verwendet wird, ist die Konfiguration des BIOS einzigartig.



2.  Wenn der Computer in das DART-Wiederherstellungsabbild gestartet wird, wird das Dialogfeld " **netstart** " angezeigt. Sie werden gefragt, ob Sie Netzwerkdienste initialisieren möchten. Wenn Sie auf **Ja**klicken, wird davon ausgegangen, dass ein DHCP-Server im Netzwerk vorhanden ist, und es wird versucht, eine IP-Adresse vom Server abzurufen. Wenn das Netzwerk statische IP-Adressen statt DHCP verwendet, können Sie später das **TCP/IP-Konfigurations** Tool in DART verwenden, um eine statische IP-Adresse anzugeben.

    Wenn Sie den Netzwerk Initialisierungsprozess überspringen möchten, klicken Sie auf **Nein**.

3.  Nachdem Sie das Dialogfeld Netzwerk Initialisierung aufgerufen haben, werden Sie gefragt, ob Sie die Laufwerkbuchstaben neu zuordnen möchten. Wenn Sie Windows Online ausführen, wird das System Volume in der Regel Laufwerk C zugeordnet. Wenn Sie jedoch Windows offline unter WinRE ausführen, wird das ursprüngliche System Volume möglicherweise einem anderen Laufwerk zugeordnet, was zu Verwirrung führen kann. Wenn Sie sich für die Neuzuordnung entscheiden, versucht Dart, die Offline Laufwerkbuchstaben den Online Laufwerkbuchstaben zuzuordnen. Eine Neuzuordnung wird nur ausgeführt, wenn ein Offline Betriebssystem später im Startvorgang ausgewählt wird.

4.  Nach dem Dialogfeld erneute Zuordnung wird ein Dialogfeld **System Wiederherstellungsoptionen** angezeigt, in dem Sie aufgefordert werden, ein Tastaturlayout auszuwählen. Anschließend werden das Systemstammverzeichnis, die Art des installierten Betriebssystems und die Partitionsgröße angezeigt. Wenn Ihr Betriebssystem nicht aufgeführt ist und Sie vermuten, dass das Fehlen von Treibern eine mögliche Ursache für den Fehler ist, klicken Sie auf **Treiber laden** , um die Verdächtigen Treiber zu laden. Sie werden aufgefordert, das Installationsmedium für das Gerät einzufügen und den Treiber auszuwählen. Wählen Sie die Installation aus, die Sie reparieren oder diagnostizieren möchten, und klicken Sie dann auf **weiter**.

    **Hinweis:**  
    Wenn die Windows-Wiederherstellungsumgebung (WinRE) erkennt oder vermutet, dass Windows 7 beim letzten Versuch nicht ordnungsgemäß gestartet wurde, wird die **Startreparatur** möglicherweise automatisch gestartet. Informationen zu dieser Situation, einschließlich der Lösungsanleitung, finden Sie unter [Problembehandlung bei Dart 7,0](troubleshooting-dart-70-new-ia.md).



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. Wählen Sie im Fenster **System Wiederherstellungsoptionen** die Option **Microsoft Diagnostics and Recovery Toolset** aus, um das **Diagnose-und Wiederherstellungs-Toolset** -Fenster zu öffnen.

6. Klicken Sie im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf **Remoteverbindung** , um das **Dart-Remote Verbindungs** Fenster zu öffnen. Wenn Sie aufgefordert werden, dem Helpdesk den Remotezugriff zu gewähren, klicken Sie auf **OK**.

   Das Fenster Dart-Remote Verbindung wird geöffnet, und es werden eine Ticketnummer, eine IP-Adresse und Portinformationen angezeigt.

7. Öffnen Sie auf dem Helpdesk-Agent-Computer die **Dart-Remote Verbindungsanzeige**.

   Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Dart 7**, und klicken Sie dann auf **Dart Remote Connection Viewer**.

8. Geben Sie im Fenster **Dart Remote Connection** die erforderlichen Tickets, IP-Adressen und Portinformationen ein.

   **Hinweis:**  
   Diese Informationen werden auf dem Computer des Endbenutzers erstellt und müssen vom Endbenutzer bereitgestellt werden. Es können mehrere IP-Adressen zur Auswahl stehen, je nachdem, wie viele auf dem Endbenutzercomputer verfügbar sind.



9. Klicken Sie auf **Verbinden**.

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

**So führen Sie die Remote Verbindungsanzeige an der Eingabeaufforderung aus**

1.  Sie können die **Dart-Remote Verbindungsanzeige** an der Eingabeaufforderung ausführen, indem Sie den Befehl **DartRemoteViewer.exe** angeben und die folgenden Parameter verwenden:

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


[Wiederherstellen von Computern mithilfe von DaRT 7.0](recovering-computers-using-dart-70-dart-7.md)









