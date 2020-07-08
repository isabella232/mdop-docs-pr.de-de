---
title: So konfigurieren Sie einen schreibgeschützten Cache für App-V Client (RDS)
description: So konfigurieren Sie einen schreibgeschützten Cache für App-V Client (RDS)
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807311"
---
# So konfigurieren Sie einen schreibgeschützten Cache für App-V Client (RDS)


**Wichtig**  Sie müssen App-V 4,6, SP1 ausführen, um dieses Verfahren verwenden zu können.

 

Sie können den App-V-Client mithilfe eines freigegebenen Caches bereitstellen, der mit allen Anwendungen aufgefüllt ist, die für alle Benutzer erforderlich sind. Anschließend konfigurieren Sie die App-V-Remote Desktop Dienste (RDS)-Clients so, dass Sie dieselbe Cachedatei verwenden. Benutzern wird mithilfe des App-V-Veröffentlichungsprozesses der Zugriff auf bestimmte Anwendungen gewährt. Da der Cache bereits mit allen Anwendungen vorinstalliert ist, erfolgt kein Streaming, wenn ein Benutzer eine Anwendung startet. Die Pakete, die zum Vorfüllen des Caches verwendet werden, müssen jedoch auf einem App-v-Server abgelegt werden, der RTSP-Streaming (Real Time Streaming Protocol) unterstützt und den App-v-Clients Zugriffsberechtigungen gewährt. Wenn Sie die Anwendungen mithilfe eines App-V-Verwaltungsservers veröffentlichen, können Sie diese Funktion zum Bereitstellen dieser Streamingfunktion verwenden.

**Hinweis**  Die in diesen Verfahren beschriebenen Details sind nur als Beispiele vorgesehen. Sie können verschiedene Methoden verwenden, um den gesamten Prozess abzuschließen.

 

## Bereitstellen des App-V-Clients in einem RDS-Szenario


Der Bereitstellungsprozess besteht aus vier Hauptaufgaben:

-   Erstellen und Auffüllen der freigegebenen mastercachedatei

-   Kopieren der freigegebenen Cachedatei in den Server Speicher

-   Konfigurieren der App-V-Client Software

-   Verwalten des Update Bereitstellungszyklus für die freigegebene Cachedatei nach der ersten Bereitstellung

Für diese Aufgaben ist eine sorgfältige Planung erforderlich. Wir empfehlen, dass Sie einen methodischen, reproduzierbaren Prozess vorbereiten und dokumentieren, dem Ihre Organisation folgen kann. Dies ist besonders wichtig für die Vorbereitung und Bereitstellung der freigegebenen mastercachedatei sowie für die laufende Verwaltung von Anwendungsupdates, für die jeweils eine Aktualisierung des freigegebenen Master Caches erforderlich ist. Führen Sie die folgenden Verfahren aus, um diese primären Aufgaben auszuführen.

**Hinweis**  Obwohl Sie die Anwendungen mithilfe verschiedener Methoden veröffentlichen können, basieren die folgenden Verfahren auf der Verwendung eines App-V-Verwaltungsservers für die Veröffentlichung.

 

**So konfigurieren Sie den schreibgeschützten Cache für die Erstbereitstellung**

1. Einrichten und Konfigurieren eines App-V-Verwaltungsservers zum Bereitstellen von Benutzerauthentifizierung und Veröffentlichungs Unterstützung.

2. Füllen Sie den Inhaltsordner dieses Verwaltungsservers mit allen Anwendungspaketen, die für alle Benutzer erforderlich sind.

3. Richten Sie einen Bereitstellungscomputer ein, auf dem der App-V-Client installiert ist. Melden Sie sich bei dem Stagingcomputer mit einem Konto an, das Zugriff auf alle Anwendungen hat, damit der vollständige Satz der Anwendungen auf dem Computer veröffentlicht wird, und Streamen Sie die Anwendungen dann in den Zwischenspeicher, damit Sie vollständig geladen werden.

   **Wichtig**  
   Der Bereitstellungscomputer muss denselben Betriebssystemtyp und dieselbe Systemarchitektur wie die von den VMS verwenden, auf denen der App-V-Client ausgeführt wird.

     

4. Starten Sie den Bereitstellungscomputer im abgesicherten Modus neu, um sicherzustellen, dass die Treiber nicht gestartet werden, da hierdurch die Cachedatei gesperrt wird.

   **Hinweis:**  
   Alternativ können Sie den Application Virtualization Service beenden und deaktivieren und dann den Computer neu starten. Denken Sie nach dem Kopieren der Datei daran, den Dienst erneut zu aktivieren und zu starten.

     

5. Kopieren Sie die sftfs. FSD-Cachedatei in ein San, in dem alle RDS-Server darauf zugreifen können, beispielsweise in einem freigegebenen Ordner. Legen Sie die Berechtigungen für den Ordner Zugriff für die Gruppe Jeder und für Administratoren, die die Cachedatei Updates verwalten, auf schreibgeschützt. Der Speicherort der Cachedatei kann über die Registrierungs-AppFS\\FileName. abgerufen werden.

   **Wichtig**  
   Sie müssen die FSD-Datei an einem Speicherort ablegen, auf dem die Reaktionsfähigkeit und Zuverlässigkeit der lokal angeschlossenen Speicherleistung entspricht, beispielsweise einem San.

     

6. Installieren Sie den App-V RDS-Client auf jedem RDS-Server, und konfigurieren Sie ihn für die Verwendung des schreibgeschützten Caches, indem Sie dem AppFS-Schlüssel auf dem Client die folgenden Registrierungsschlüsselwerte hinzufügen. Der AppFS-Schlüssel befindet sich unter HKEY \ _LOCAL \ _MACHINE \\software\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS für 32-Bit-Computer und bei HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\client\\appfs für 64-Bit-Computer.

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Key</th>
   <th align="left">Typ</th>
   <th align="left">Wert</th>
   <th align="left">Zweck</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>FileName</p></td>
   <td align="left"><p>Zeichenfolge</p></td>
   <td align="left"><p>Pfad von FSD</p></td>
   <td align="left"><p>Gibt den Pfad der freigegebenen Cachedatei an, beispielsweise \RDSServername\Sharefolder\SFTFS. FSD (erforderlich).</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReadOnlyFSD</p></td>
   <td align="left"><p>DWORD</p></td>
   <td align="left"><p>1</p></td>
   <td align="left"><p>Konfiguriert den Client so, dass er im schreibgeschützten Modus ausgeführt wird. Dadurch wird sichergestellt, dass der Client nicht versucht, Aktualisierungen an den Paketcache zu streamen. (Erforderlich)</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ErrorLogLocation</p></td>
   <td align="left"><p>Zeichenfolge</p></td>
   <td align="left"><p>Pfad der Fehlerprotokolldatei (ETL)</p></td>
   <td align="left"><p>Eintrag, der zum Angeben des Pfads des Fehlerprotokolls verwendet wird. Empfohlen. Verwenden Sie einen lokalen Pfad wie C:\Logs\Sftfs.ETL).</p></td>
   </tr>
   </tbody>
   </table>

     

7. Konfigurieren Sie die einzelnen RDS-Server in der Farm so, dass Sie den Veröffentlichungsserver verwenden, und verwenden Sie die Veröffentlichungsaktualisierung, wenn sich Benutzer anmelden. Wenn sich Benutzer bei den RDS-Servern anmelden, wird ein Veröffentlichungs Aktualisierungszyklus durchgeführt, und es werden alle Anwendungen veröffentlicht, für die Ihr Konto autorisiert wurde. Diese Anwendungen werden im freigegebenen Cache ausgeführt.

**So konfigurieren Sie den RDS-Client für die Paketaktualisierung**

1.  Führen Sie das Upgrade und Testen des Anwendungspakets durch.

2.  Aktualisieren Sie das Paket auf dem App-V-Server. Veröffentlichen und Streamen Sie dann die neue Version der Anwendungen auf dem Bereitstellungscomputer auf dem Client, damit Sie vollständig in den Cache geladen werden.

3.  Starten Sie den Bereitstellungscomputer im abgesicherten Modus neu, um sicherzustellen, dass die Treiber nicht gestartet werden.

    **Hinweis**  Oder Sie können den Application Virtualization Service zunächst beenden und dann im Services. msc deaktivieren und den Computer neu starten. Nachdem die Datei kopiert wurde, denken Sie daran, den Dienst erneut zu aktivieren und zu starten.

     

4.  Kopieren Sie die sftfs. FSD-Cachedatei in ein San, in dem alle RDS-Server darauf zugreifen können, beispielsweise in einem freigegebenen Ordner. Sie können einen anderen Dateinamen verwenden, beispielsweise SFTFS \ _V2. FSD, um die neue Version zu unterscheiden.

5.  Um den App-V RDS-Client auf jedem RDS-Server in der Farm so zu konfigurieren, dass die aktualisierte freigegebene Cachedatei verwendet wird, ändern Sie den FileName-Wert des AppFS-Registrierungsschlüssels so, dass er auf den Speicherort der aktualisierten Datei verweist, beispielsweise \\\\RDSServername\\Sharefolder\\SFTFS\ _V2. FSD. Dadurch wird sichergestellt, dass jeder RDS-Server die aktualisierte Kopie des Caches erhält, wenn die APP-innerhalb seiner vClient-Treiber neu gestartet werden.

    **Wichtig**  Sie müssen die RDS-Server neu starten, um die aktualisierte freigegebene Cachedatei verwenden zu können.

     

## Verwenden symbolischer Links beim Aktualisieren des Caches


Anstatt den AppFS-Schlüsseldatei Namen jedes Mal zu ändern, wenn eine neue Cachedatei bereitgestellt wird, die neue oder aktualisierte Pakete enthält, können Sie in den folgenden Betriebssystemen einen symbolischen Link verwenden: Windows Vista, Windows 7 und Windows Server 2008. Weitere Informationen zu symbolischen Links finden Sie unter [symbolische Links](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) . Im Gegensatz dazu unterstützt Windows XP nicht die Verwendung symbolischer Links, und Sie müssen stattdessen Abzweigungspunkte verwenden. Weitere Informationen zu Junctions finden Sie im [Artikel 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in der Microsoft Knowledge Base ( https://go.microsoft.com/fwlink/?LinkId=182553) und auch in der Tool [Verzweigung v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ( https://go.microsoft.com/fwlink/?LinkId=182554) .

**So konfigurieren Sie einen symbolischen Link, um auf den Cache zu verweisen**

1.  Öffnen Sie während der anfänglichen Bereitstellungsphase ein Eingabeaufforderungsfenster als lokaler Administrator auf dem RDS-Server-Betriebssystem.

2.  Erstellen Sie einen symbolischen Link mit dem Befehl mklink, und konfigurieren Sie ihn so, dass er auf die Datei sftfs. FSD verweist.

    **     mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.FSD**

3.  Öffnen Sie auf dem VDI-Master-VM-Bild ein Eingabeaufforderungsfenster, indem Sie die Option " **als Administrator ausführen** " verwenden und Remote Link Berechtigungen erteilen, damit der VM auf den symbolischen Link auf dem VDI-Host Betriebssystem zugreifen kann. Standardmäßig sind Remote Link-Berechtigungen deaktiviert.

    **fsutil-Verhaltens Satz SymlinkEvaluation R2R: 1**

    **Hinweis**  Auf dem Speicherserver müssen entsprechende Link Berechtigungen aktiviert sein. Je nach Speicherort des Links und der Datei "sftfs. FSD" sind die Berechtigungen **L2L: 1** oder **L2R: 1** oder **R2L: 1** oder **R2R: 1**.

     

4.  Wenn Sie den App-V RDS-Client konfigurieren, legen Sie den AppFS-Schlüssel FileName-Wert gleich dem UNC-Pfad der FSD-Datei fest, die den symbolischen Link verwendet. Legen Sie beispielsweise den Dateinamen auf \\\\VDIHostserver\\Symlinkname. Wenn der App-V-Client zuerst auf den Cache zugreift, übergibt der symbolische Link an den Client ein Handle für die Cachedatei. Der Client verwendet dieses Handle weiterhin, solange der Client ausgeführt wird. Der Wert des symbolischen Links kann auch dann sicher aktualisiert werden, wenn vorhandene Clients den alten freigegebenen Cache geöffnet haben.

5.  Wenn Sie ein Paket aktualisieren oder dem Cache ein neues Paket hinzufügen müssen, führen Sie die Schritte 1 bis 4 des Aktualisierungsvorgangs aus. Löschen Sie dann den symbolischen Link, und erstellen Sie ihn erneut, um auf die neue Version der freigegebenen Cachedatei zu verweisen. Dadurch wird sichergestellt, dass jeder RDS-Server die aktualisierte Kopie des Caches erhält, wenn die App-V-Clienttreiber neu gestartet werden. Beim Neustart des RDS-Servers erhält der App-V-Client ein Handle für die aktualisierte Kopie des Caches, da der Client den Pfad verwendet, der den aktualisierten symbolischen Link enthält. Dann können die Benutzer auf die neuen und aktualisierten Anwendungen zugreifen.

## Verwandte Themen


[So installieren Sie Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

[So installieren Sie Application Virtualization Client manuell](how-to-manually-install-the-application-virtualization-client.md)

[So installieren Sie den Client über die Befehlszeile](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





