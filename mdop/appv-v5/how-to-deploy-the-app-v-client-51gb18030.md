---
title: So stellen Sie App-V-Client bereit
description: So stellen Sie App-V-Client bereit
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805492"
---
# So stellen Sie App-V-Client bereit


Gehen Sie wie folgt vor, um den Microsoft Application Virtualization (App-V) 5,1-Client und den Remote Desktop Dienste-Client zu installieren. Sie müssen die Version des Clients installieren, die dem Betriebssystem des Zielcomputers entspricht.

<a href="" id="bkmk-clt-install-prereqs"></a>**Was zu tun ist, bevor Sie beginnen**

1. Überprüfen und installieren Sie die erforderlichen Softwarevoraussetzungen:

   Installieren Sie die erforderliche Software, die der Version von App-V entspricht, die Sie installieren:

   -   [Informationen zu App-V 5.1](about-app-v-51.md)

   -   [Voraussetzungen für App-V 5.1](app-v-51-prerequisites.md)

2. Überprüfen Sie die Client Koexistenz und die nicht unterstützten Szenarios, wie Sie für Ihre Installation gelten:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Bereitstellen von nebeneinander vorhandenen App-V-Clients</p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)">Planen für die Bereitstellung von App-V 5.1 Sequencer und App-V-Client</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Nicht unterstützte oder begrenzte Installationsszenarien</p></td>
   <td align="left"><p>Weitere Informationen finden Sie im Abschnitt "Client" in <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> App-V 5,1 Unterstützte Konfigurationen</a></p></td>
   </tr>
   </tbody>
   </table>



3. Überprüfen Sie die Speicherorte für Clientregistrierung, Protokoll und Informationen zur Problembehandlung:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Client Registrierungsinformationen</p></td>
<td align="left"><ul>
<li><p>Standardmäßig werden die Clientinformationen nach der Installation des App-V 5,1-Clients in der Registrierung im folgenden Registrierungsschlüssel gespeichert:</p>
<p><strong>HKEY_LOCAL_MACHINE \ Software \ Microsoft \ APPV \ Client</strong></p></li>
<li><p>Wenn Sie ein virtualisiertes Paket auf einem Computer bereitstellen, auf dem der App-V-Client ausgeführt wird, werden die zugehörigen Paketdaten an folgendem Speicherort gespeichert:</p>
<p><strong>C: \ ProgramData \ App-V</strong></p>
<p>Sie können diesen Speicherort jedoch mit dem folgenden Registrierungsschlüssel neu konfigurieren:</p>
<p><strong>HKEY_LOCAL_MACHINE \ Software \ Microsoft \ Software \ Microsoft \ APPV \ Client \ Streaming \ PACKAGEINSTALLATIONROOT</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Client Protokolldateien</p></td>
<td align="left"><ul>
<li><p>Suchen Sie für Protokolldateiinformationen, die dem App-V 5,1-Client zugeordnet sind, im folgenden Protokoll:</p>
<p><strong>Ereignisprotokolle/Anwendungen und Dienstprotokolle/Microsoft/AppV</strong></p></li>
<li><p>In App-V 5,0 SP3 wurden einige Protokolle konsolidiert und an den folgenden Speicherort verschoben:</p>
<p><strong>Ereignisprotokolle/Anwendungen und Dienstprotokolle/Microsoft/AppV/ServiceLog</strong></p>
<p>Eine Liste der verschobenen Protokolle finden Sie unter <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> Informationen zu App-V 5,0 SP3 </a> .</p></li>
<li><p>Pakete, die derzeit auf Computern gespeichert sind, auf denen der App-V 5,1-Client ausgeführt wird, werden an folgendem Speicherort gespeichert:</p>
<p><strong>C:\ProgramData\App-V &amp; lt; Paket-ID &gt; &amp; lt; Versions-ID&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Informationen zur Problembehandlung bei der Client Installation</p></td>
<td align="left"><p>Sehen Sie sich das Fehlerprotokoll im <strong> Ordner% Temp% an </strong> . Wenn Sie die Protokolldateien überprüfen möchten, klicken Sie auf <strong> Start </strong> , geben Sie <strong> % Temp% </strong> ein, und suchen Sie dann nach dem <strong> appv_ Protokoll </strong> .</p></td>
</tr>
</tbody>
</table>



**So installieren Sie den App-V 5,1-Client**

1.  Kopieren Sie die App-V 5,1-Clientinstallationsdatei auf den Computer, auf dem Sie installiert werden soll. Wählen Sie eine der folgenden Clienttypen aus:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Clienttyp</th>
    <th align="left">Zu verwendende Datei</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Standard Version des Clients</p></td>
    <td align="left"><p><strong>appv_client_setup.exe</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Version des Clients für Remote Desktop Dienste</p></td>
    <td align="left"><p><strong>appv_client_setup_rds.exe</strong></p></td>
    </tr>
    </tbody>
    </table>



2.  Doppelklicken Sie auf die Installationsdatei, und klicken Sie auf **Installieren**. Vor Beginn der Installation überprüft das Installationsprogramm den Computer auf alle fehlenden [App-V 5,1-Voraussetzungen](app-v-51-prerequisites.md).

3.  Überprüfen und akzeptieren Sie die Software-Lizenzbestimmungen, wählen Sie aus, ob Sie Microsoft Update verwenden möchten und ob Sie am Programm zur Verbesserung der Benutzerfreundlichkeit von Microsoft teilnehmen möchten, und klicken Sie auf **Installieren**.

4.  Klicken Sie auf der Seite **Setup erfolgreich abgeschlossen** auf **Schließen**.

    Bei der Installation werden die folgenden Einträge für den App-V-Client in **Programmen**erstellt:

    -   **EXE**

    -   **.msi**

    -   **Sprachpaket**

        **Hinweis:**  
        Nach der Installation kann nur die exe-Datei deinstalliert werden.



**So installieren Sie den App-V 5,1-Client mithilfe eines Skripts**

1. Installieren Sie alle erforderlichen Softwarevoraussetzungen auf den Zielcomputern. Schauen Sie [sich an, was Sie vor Beginn tun sollten](#bkmk-clt-install-prereqs). Wenn Sie den Client mithilfe einer MSI-Datei installieren, schlägt die Installation fehl, wenn keine Voraussetzungen vorhanden sind.

2. Wenn Sie ein Skript zum Installieren des App-V 5,1-Clients verwenden möchten, verwenden Sie die folgenden Parameter mit **appv\_client\_setup.exe**.

   **Hinweis:**  
   Der Client Windows Installer (MSI) unterstützt den gleichen Satz von Schaltern, mit Ausnahme des **/Log** -Parameters.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>/INSTALLDIR</p></td>
   <td align="left"><p>Gibt das Installationsverzeichnis an. Verwendungsbeispiel: <strong> /INSTALLDIR = C:\Program Files\AppV Client</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/CEIPOPTIN</p></td>
   <td align="left"><p>Ermöglicht die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit. Beispiel Verwendung: <strong> /CEIPOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/MUOPTIN</p></td>
   <td align="left"><p>Aktiviert Microsoft Update. Beispiel Verwendung: <strong> /MUOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/PACKAGEINSTALLATIONROOT</p></td>
   <td align="left"><p>Gibt das Verzeichnis an, in dem alle neuen Anwendungen und Updates installiert werden sollen. Beispiel Verwendung: <strong> /PACKAGEINSTALLATIONROOT =&#39;C:\app-V-Pakete&#39;</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/PACKAGESOURCEROOT</p></td>
   <td align="left"><p>Überschreibt den Quellspeicherort zum Herunterladen von Paketinhalten. Beispiel Verwendung: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/AUTOLOAD</p></td>
   <td align="left"><p>Gibt an, wie neue Pakete von App-V 5,1 auf einem bestimmten Computer geladen werden. Die folgenden Optionen sind aktiviert: [1]; Alle Pakete automatisch laden [2]; oder laden Sie keine Pakete automatisch [0]. <strong> Beispiel Verwendung:/AUTOLOAD = [0 | 1 | 2]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/SHAREDCONTENTSTOREMODE</p></td>
   <td align="left"><p>Gibt an, dass Streaming-Paketinhalt nicht auf der lokalen Festplatte gespeichert werden soll. Beispiel Verwendung: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/MIGRATIONMODE</p></td>
   <td align="left"><p>Ermöglicht es dem App-V 5,1-Client, die Verknüpfungen und FTA zu ändern, die den Paketen zugeordnet sind, die mit einer früheren Version erstellt wurden. Beispiel Verwendung: <strong> /MIGRATIONMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ENABLEPACKAGESCRIPTS</p></td>
   <td align="left"><p>Aktiviert die Skripts, die in der Datei des paketmanifests oder der Konfigurationsdateien definiert sind, die ausgeführt werden sollen. Beispiel Verwendung: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/ROAMINGREGISTRYEXCLUSIONS</p></td>
   <td align="left"><p>Gibt die Registrierungspfade an, die nicht mit einem Benutzerprofil durchlaufen werden. Verwendungsbeispiel: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; Software\Clients</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ROAMINGFILEEXCLUSIONS</p></td>
   <td align="left"><p>Gibt die Dateipfade relativ zu% User Profile% an, die nicht mit einem Benutzer&#39;s-Profil Roaming durchlaufen. Beispiel Verwendung: <strong> /ROAMINGFILEEXCLUSIONS &#39;Desktop; meine Bilder&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERNAME</p></td>
   <td align="left"><p>Zeigt den Namen des Veröffentlichungsservers an. Verwendungsbeispiel: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERURL</p></td>
   <td align="left"><p>Zeigt die URL des Veröffentlichungsservers an. Verwendungsbeispiel: <strong> /S2PUBLISHINGSERVERURL = \pubserver</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHENABLED-</p></td>
   <td align="left"><p>Aktiviert eine globale Veröffentlichungsaktualisierung. Beispiel Verwendung: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHONLOGON</p></td>
   <td align="left"><p>Initiiert eine globale Veröffentlichungsaktualisierung, wenn sich ein Benutzer anmeldet. Beispiel Verwendung: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVAL-</p></td>
   <td align="left"><p>Gibt das Aktualisierungsintervall für die Veröffentlichung an, wobei <strong> 0 angibt, dass </strong> Sie nicht regelmäßig aktualisiert werden. Verwendungsbeispiel: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Gibt die Intervalleinheit an (Stunden [0], Tage [1]). Beispiel Verwendung: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHENABLED</p></td>
   <td align="left"><p>Aktiviert die Aktualisierung der Benutzer Veröffentlichung. Beispiel Verwendung: <strong> /S2USERREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHONLOGON</p></td>
   <td align="left"><p>Initiiert eine Aktualisierung der Benutzer Veröffentlichung, wenn sich ein Benutzer anmeldet. Beispiel Verwendung: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVAL-</p></td>
   <td align="left"><p>Gibt das Aktualisierungsintervall für die Veröffentlichung an, wobei <strong> 0 angibt, dass </strong> Sie nicht regelmäßig aktualisiert werden. Verwendungsbeispiel: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Gibt die Intervalleinheit an (Stunden [0], Tage [1]). Beispiel Verwendung: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/Log</p></td>
   <td align="left"><p>Gibt einen Speicherort an, an dem die Protokollinformationen gespeichert werden. Der Standardspeicherort ist% Temp%. Verwendungsbeispiel: <strong> /Log C:\logs\log.log</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/q</p></td>
   <td align="left"><p>Gibt eine unbeaufsichtigte Installation an.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/Repair</p></td>
   <td align="left"><p>Repariert eine vorherige Clientinstallation.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/NORESTART</p></td>
   <td align="left"><p>Verhindert, dass der Computer nach der Clientinstallation neu gestartet wird.</p>
   <p>Der Parameter verhindert, dass der Computer des Endbenutzers nach jedem Update neu gestartet wird, und Sie können den Neustart nach Belieben planen. So können Sie beispielsweise App-V 5,1 installieren und dann das Hotfix-Paket Y installieren, ohne nach der Installation des Service Packs einen Neustart durchführen zu müssen. Nach der Installation müssen Sie den Computer neu starten, bevor Sie App-V verwenden.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/Uninstall</p></td>
   <td align="left"><p>Deinstalliert den Client.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ACCEPTEULA</p></td>
   <td align="left"><p>Akzeptiert den Lizenzvertrag. Dies ist für eine unbeaufsichtigte Installation erforderlich. Beispiel Verwendung: <strong> /ACCEPTEULA </strong> oder <strong> /ACCEPTEULA = 1 </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/LAYOUT</p></td>
   <td align="left"><p>Gibt die zugeordnete Layout-Aktion an. Außerdem werden die Windows Installer-Dateien (MSI) und Skriptdateien in einen Ordner extrahiert, ohne App-V 5,1 zu installieren. Es wird kein Wert erwartet.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/LAYOUTDIR</p></td>
   <td align="left"><p>Gibt das layoutverzeichnis an. Erfordert einen Zeichenfolgenwert. Beispielsyntax: <strong> /LAYOUTDIR = "C:\Application Virtualization Client" </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/?,/h,/Help</p></td>
   <td align="left"><p>Fordert Hilfe zu den vorherigen Installationsparametern an.</p></td>
   </tr>
   </tbody>
   </table>



**So installieren Sie den App-V 5,1-Client mithilfe der Windows Installer-Datei (MSI)**

1.  Installieren Sie die erforderlichen Voraussetzungen auf den Zielcomputern. Schauen Sie [sich an, was Sie vor Beginn tun sollten](#bkmk-clt-install-prereqs). Wenn keine Voraussetzungen erfüllt sind, schlägt die Installation fehl.

2.  Stellen Sie sicher, dass die Zielcomputer keine ausstehenden Neustarts haben, bevor Sie den Client mithilfe der App-V 5,1 Windows Installer-Dateien (MSI) installieren. Die Windows Installer-Dateien kennzeichnen keinen ausstehenden Neustart.

3.  Stellen Sie eine der folgenden Windows Installer-Dateien auf dem Zielcomputer bereit. Die von Ihnen angegebene Datei muss der Konfiguration des Zielcomputers entsprechen.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Art der Bereitstellung</th>
    <th align="left">Diese Datei bereitstellen</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Auf dem Computer befindet sich ein Microsoft Windows-32-Bit-Betriebssystem</p></td>
    <td align="left"><p>appv_client_MSI_x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Auf dem Computer befindet sich ein Microsoft Windows-64-Bit-Betriebssystem</p></td>
    <td align="left"><p>appv_client_MSI_x64.msi</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Sie stellen den App-V 5,1-Client für Remote Desktop Dienste bereit.</p></td>
    <td align="left"><p>appv_client_rds_MSI_x64.msi</p></td>
    </tr>
    </tbody>
    </table>



4.  Wählen Sie anhand der Informationen in der folgenden Tabelle auf der Grundlage der gewünschten Sprache für den Zielcomputer das entsprechende Sprachpaket **. msi** aus, das Sie installieren möchten. **Xxxx** in der Tabelle bezieht sich auf das Zielgebietsschema des Sprachpakets.

    **Was Sie wissen sollten, bevor Sie beginnen:**

    -   Die Sprachpakete sind sowohl für den standardmäßigen App-v 5,1-Client als auch für die Remote Desktop Dienste-Version des App-v 5,1-Clients üblich.

    -   Wenn Sie den App-V 5,1-Client mithilfe der **exe**-Datei installieren, wird vom Installationsprogramm nur das Sprachpaket bereitgestellt, das dem auf dem Zielcomputer ausgeführten Betriebssystem entspricht.

    -   Zum Bereitstellen weiterer Sprachpakete auf einem Zielcomputer verwenden Sie das Verfahren **zum Installieren des App-V 5,1-Clients mithilfe der Windows Installer-Datei (MSI)**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Art der Bereitstellung</th>
    <th align="left">Diese Datei bereitstellen</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Auf dem Computer befindet sich ein Microsoft Windows-32-Bit-Betriebssystem</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Auf dem Computer befindet sich ein Microsoft Windows-64-Bit-Betriebssystem</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x64.msi</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Verwandte Themen


[Bereitstellen von App-V 5.1](deploying-app-v-51.md)

[Informationen über Clientkonfigurationseinstellungen](about-client-configuration-settings51.md)

[So deinstallieren Sie den App-V 5.1-Client](how-to-uninstall-the-app-v-51-client.md)









