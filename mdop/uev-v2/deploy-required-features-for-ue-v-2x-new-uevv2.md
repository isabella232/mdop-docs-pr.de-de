---
title: Bereitstellen der erforderlichen Features für UE-V 2.x
description: Bereitstellen der erforderlichen Features für UE-V 2.x
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810693"
---
# Bereitstellen der erforderlichen Features für UE-V 2.x


Für alle Microsoft User Experience Virtualization (UE-V) 2,0-, 2,1-und 2,1 SP1-Bereitstellungen sind diese Features erforderlich.

-   [Bereitstellen eines Speicherorts für Einstellungen](#ssl) , auf den Endbenutzer zugreifen können

    Hierbei handelt es sich um eine standardmäßige Netzwerkfreigabe, die Benutzereinstellungen speichert und abruft.

-   [Auswählen der Konfigurationsmethode für UE-V](#config)

    UE-V kann mithilfe allgemeiner Verwaltungstools wie Gruppenrichtlinien, Configuration Manager oder Windows-Verwaltungsinfrastruktur und PowerShell bereitgestellt und konfiguriert werden.

-   [Stellen Sie einen UE-V-Agent bereit](#agent) , der auf jedem Computer installiert werden soll, der die Einstellungen synchronisiert.

    Damit werden registrierte Anwendungen und das Betriebssystem für alle Einstellungen geändert und die Einstellungen zwischen Computern synchronisiert.

In den Themen in diesem Abschnitt wird beschrieben, wie diese Features bereitgestellt werden.

## <a href="" id="ssl"></a>Bereitstellen eines Speicherorts für UE-V-Einstellungen


UE-V erfordert einen Speicherort, an dem Benutzereinstellungen in den Einstellungen-Paketdateien gespeichert werden. Sie können diesen Einstellungs Speicherort auf eine der folgenden Arten konfigurieren:

-   Erstellen eines eigenen Speicherorts für Einstellungen

-   Verwenden des vorhandenen Active Directory für den Speicherort der Einstellungen

Wenn Sie keinen Speicherplatz für Einstellungen erstellen, wird standardmäßig Active Directory (AD) vom UE-V-Agent verwendet.

**Hinweis:**  
Im Hinblick auf die [Leistungs-und Kapazitätsplanung](https://technet.microsoft.com/library/dn458932.aspx#capacity) und die Verringerung von Problemen mit der Netzwerklatenz können Sie die Speicherorte für Einstellungen in denselben lokalen Netzwerken erstellen, in denen sich die Computer der Benutzer befinden. Für den Speicherort der Einstellungen empfehlen wir pro Nutzer 20 MB Speicherplatz.



### Erstellen eines Speicherorts für UE-V-Einstellungen

Vor dem Definieren des Speicherorts für Einstellungen müssen Sie ein Stammverzeichnis mit Lese-/Schreibzugriff für Benutzer erstellen, die die Einstellungen für die Freigabe speichern. Der UE-V-Agent erstellt benutzerspezifische Ordner unter diesem Stammverzeichnis.

Der Speicherort der Einstellungen wird durch Festlegen der SettingsStoragePath-Konfigurationsoption definiert, die mithilfe einer der folgenden Methoden konfiguriert werden kann:

-   Wenn Sie [den UE-V-Agent](#agent) über einen Befehlszeilenparameter oder in einem Batchskript bereitstellen

-   Über [Gruppenrichtlinien](https://technet.microsoft.com/library/dn458893.aspx) Einstellungen

-   Mit dem [System Center-Konfigurationspaket](https://technet.microsoft.com/library/dn458917.aspx) für UE-V

-   Nach der Installation des UE-V-Agents mithilfe von [Windows PowerShell oder Windows-Verwaltungsinstrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)

Der Pfad muss sich im UNC-Pfad (Universal Naming Convention) des Servers und der Freigabe befinden. Beispiel: **\\\\Server\\Settingsshare\\**. Diese Konfigurationsoption unterstützt die Verwendung von Variablen, um bestimmte Synchronisierungsszenarien zu ermöglichen. So können Sie beispielsweise die `%username%\%computername%` Variablen verwenden, um die Benutzereinstellungen für Endbenutzer in diesen Szenarien beizubehalten:

-   Endbenutzer, die mehrere physische Computer in Ihrem Unternehmen verwenden

-   Unternehmens Computer, die von mehreren Endbenutzern verwendet werden

Der UE-V-Agent erstellt dynamisch einen benutzerspezifischen Einstellungsspeicher Pfad mit dem Namen eines versteckten Systemordners `SettingsPackages` basierend auf der Konfigurationseinstellung von **SettingsStoragePath**. Der Agent liest und schreibt Einstellungen an diesen Speicherort, wie Sie von den registrierten UE-V-Einstellungen für Standort Vorlagen definiert werden.

Die **UE-V-Einstellungen werden durch die Regel "letzte Write-WINS" bestimmt:** Wenn der Speicherort für Einstellungen für Benutzer mit mehreren verwalteten Computern identisch ist, liest und schreibt ein UE-V-Agent unabhängig von Agents, die auf anderen Computern ausgeführt werden, den Speicherort für die Einstellungen. Die letzten geschriebenen Einstellungen und Werte sind diejenigen, die angewendet werden, wenn der nächste Agent vom Speicherort für Einstellungen liest.

**Bereitstellen des Speicherorts für Einstellungen:** Führen Sie die folgenden Schritte aus, um den Speicherort für Einstellungen zu definieren, anstatt den vorhandenen Active Directory-Dienst zu verwenden. Sie sollten den Zugriff auf die Speicherfreigabe für Einstellungen auf die Benutzer beschränken, die dies erfordern, wie in den folgenden Tabellen dargestellt.

**So stellen Sie die UE-V-Netzwerkfreigabe bereit**

1.  Erstellen Sie eine neue Sicherheitsgruppe für UE-V-Benutzer.

2.  Erstellen Sie einen neuen Ordner auf dem zentral gelegenen Computer, auf dem die UE-v-Einstellungs Pakete gespeichert sind, und gewähren Sie dem UE-v-Benutzer Zugriff mit Gruppen Berechtigungen für den Ordner. Der Administrator, der UE-V unterstützt, muss über Berechtigungen für diesen freigegebenen Ordner verfügen.

3.  Legen Sie die folgenden SMB-Berechtigungen (Share-Level-Server-Nachrichten Block) für den Ordner "Settings-Speicherort" ein.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Benutzerkonto</strong></th>
    <th align="left"><strong>Empfohlene Berechtigungen</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Jeder</p></td>
    <td align="left"><p>Keine Berechtigungen</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Sicherheitsgruppe der UE-V-Benutzer</p></td>
    <td align="left"><p>Vollzugriff</p></td>
    </tr>
    </tbody>
    </table>



4.  Legen Sie die folgenden NTFS-Dateisystemberechtigungen für den Ordner "Settings Storage Location" ein.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Benutzerkonto</strong></th>
    <th align="left"><strong>Empfohlene Berechtigungen</strong></th>
    <th align="left"><strong>Ordner</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Ersteller/Besitzer</p></td>
    <td align="left"><p>Vollzugriff</p></td>
    <td align="left"><p>Nur Unterordner und Dateien</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Sicherheitsgruppe der UE-V-Benutzer</p></td>
    <td align="left"><p>Ordner auflisten/Daten lesen, Ordner erstellen/Daten anfügen</p></td>
    <td align="left"><p>Nur diesen Ordner</p></td>
    </tr>
    </tbody>
    </table>



Mit dieser Konfiguration erstellt und sichert der UE-V-Agent einen Settingspackage-Ordner, während er im Kontext des Benutzers ausgeführt wird, und gewährt jedem Benutzer die Berechtigung zum Erstellen von Ordnern für die Speicherung von Einstellungen. Benutzer erhalten Vollzugriff auf Ihren Settingspackage-Ordner, während andere Benutzer nicht darauf zugreifen können.

**Hinweis:**  
Wenn Sie die Speicherfreigabe für Einstellungen auf einem Computer erstellen, auf dem ein Windows Server-Betriebssystem ausgeführt wird, konfigurieren Sie UE-V, um zu überprüfen, ob die lokale Gruppe Administratoren oder der aktuelle Benutzer der Besitzer des Ordners ist, in dem die Einstellungs Pakete gespeichert sind. Um diese zusätzliche Sicherheit zu aktivieren, geben Sie diese Einstellung im Windows Server-Registrierungs-Editor an:

1.  Fügen Sie einen Registrierungsschlüssel " **reg \ _DWORD** " mit dem Namen **"RepositoryOwnerCheckEnabled"** zu **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.

2.  Stellen Sie den Wert für den Registrierungsschlüssel auf *1 ein*.



### Verwenden von Active Directory mit UE-V 2. x

Der UE-V-Agent verwendet standardmäßig Active Directory (AD), wenn ein Speicherort für Einstellungen nicht anderweitig definiert ist. In diesen Fällen erstellt der UE-V-Agent dynamisch den Einstellungsspeicher Ordner unter dem Stammverzeichnis des AD Home-Verzeichnisses jedes Benutzers. Wenn jedoch eine benutzerdefinierte Verzeichnis Einstellung in AD konfiguriert ist, wird stattdessen dieses Verzeichnis verwendet.

## <a href="" id="config"></a>Wählen Sie die Konfigurationsmethode für UE-V 2. x aus.


Sie möchten ermitteln, welche Konfigurationsmethode Sie für die Verwaltung von UE-v nach der Bereitstellung verwenden werden, da es sich hierbei um die Konfigurationsmethode handelt, die Sie zum Bereitstellen des UE-v-Agents verwenden. In der Regel ist dies die Konfigurationsmethode, die Sie bereits in Ihrer Umgebung verwenden, beispielsweise Windows PowerShell oder Configuration Manager.

Je nach verwendeter Konfigurationsmethode können Sie UE-v vor, während oder nach der Installation des UE-v-Agents konfigurieren.

-   [Gruppenrichtlinie](https://technet.microsoft.com/library/dn458893.aspx)**:** Sie können Ihre vorhandene Gruppenrichtlinieninfrastruktur verwenden, um UE-v vor oder nach der Bereitstellung des UE-v-Agents zu konfigurieren. Die Vorlage UE-v-Gruppenrichtlinien-ADMX ermöglicht die zentrale Verwaltung der allgemeinen Konfigurationsoptionen des UE-v-Agents und umfasst Einstellungen für die Konfiguration der UE-v-Synchronisierung.

    **Installieren der ADMX-Vorlagen für UE-V-Gruppenrichtlinien:** ADMX-Vorlagen für Gruppenrichtlinien für UE-v konfigurieren Sie die Synchronisierungseinstellungen für den UE-v-Agent, und aktivieren Sie die zentrale Verwaltung der allgemeinen Konfigurationseinstellungen des UE-v-Agents mithilfe einer vorhandenen Gruppenrichtlinien-Infrastruktur.

    Unterstützte Betriebssysteme für den Domänencontroller, der die Gruppenrichtlinienobjekte bereitstellt, umfassen Folgendes:

    Windows Server 2008 R2

    Windows Server 2012 und Windows Server 2012 R2

-   [Konfigurations-Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** mit dem UE-v-Konfigurationspaket können Sie das Feature "Konformitäts Einstellungen" von System Center Configuration Manager 2012 SP1 oder höher verwenden, um konsistente Konfigurationen auf Websites anzuwenden, auf denen UE-v und Configuration Manager installiert sind.

-   [Windows PowerShell und WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** Sie können mithilfe von skriptbasierten Befehlen für Windows PowerShell und Windows-Verwaltungsinstrumentation (WMI) Konfigurationen nach der Installation des UE-V-Agents ändern.

    **Hinweis:**  
    Die Änderung der Registrierung kann zu Datenverlusten führen, oder der Computer reagiert nicht mehr. Wir empfehlen, dass Sie andere Konfigurationsmethoden verwenden.



-   **Befehlszeilen-oder Batch Skript Installation:** Parameter, die beim [Bereitstellen des UE-v-Agents](#agent) verwendet werden, konfigurieren viele UE-v-Einstellungen. Elektronische Softwareverteilungssysteme wie System Center 2012 Configuration Manager verwenden diese Parameter, um Ihre Clients beim Bereitstellen und Installieren der UE-V-Agent-Software zu konfigurieren.

## <a href="" id="agent"></a>Bereitstellen des UE-V 2. x-Agents


Der UE-v-Agent ist der Kern einer UE-v-Bereitstellung und muss auf jedem Computer ausgeführt werden, der UE-v verwendet, um die Anwendungs-und Windows-Einstellungen zu synchronisieren.

**Installationsdateien des UE-V-Agents:** Eine einzelne Installationsdatei, AgentSetup.exe, installiert den UE-V-Agent sowohl auf 32-Bit-als auch 64-Bit-Betriebssystemen. Darüber hinaus werden AgentSetupx86.msi oder AgentSetupx64.msi architekturspezifische Windows Installer-Dateien bereitgestellt, und da Sie kleiner sind, können Sie die Agenten Bereitstellungen rationalisieren. Die [Befehlszeilenparameter für das AgentSetup.exe-Installationsprogramm](#params) werden auch für die Windows Installer-Installation unterstützt.

**Wichtig**  
Bei der Installation oder Deinstallation von UE-V-Agents können Sie entweder die AgentSetup.exe-Datei oder die Sie AgentSetup &lt; arch &gt; . msi-Datei verwenden, aber nicht beide. Die gleiche Datei muss zum Deinstallieren des UE-v-Agents verwendet werden, der zum Installieren des UE-v-Agents verwendet wurde.



### Bereitstellen des UE-V-Agents

Sie können die folgenden Methoden zum Bereitstellen des UE-V-Agents verwenden:

-   Ein ESD-Lösungssystem (Electronic Software Distribution) wie Configuration Manager, mit dem eine Windows Installer-Datei (MSI) installiert werden kann.

-   Ein Installationsskript, das auf die Windows Installer-Datei (MSI) verweist, die zentral auf einer Freigabe gespeichert ist.

-   Ein Installationsprogramm, das Sie manuell auf dem Computer ausführen.

Gehen Sie wie folgt vor, um den UE-V-Agent über eine Netzwerkfreigabe bereitzustellen.

**So installieren und konfigurieren Sie den UE-V-Agent über eine Netzwerkfreigabe**

1.  Stufen Sie die Installationsdatei des UE-V-Agents auf einer Netzwerkfreigabe AgentSetup.exe, auf die Benutzer die Berechtigung "lesen" haben.

2.  Stellen Sie ein Skript auf Benutzercomputern bereit, die den UE-V-Agent installieren. Das Skript sollte den Speicherort für Einstellungen angeben.

**Bereitstellungsoptionen:** Achten Sie beim Installieren des UE-V-Agents darauf, das richtige Variablen Format zu verwenden. Die folgende Tabelle enthält Beispiele für Bereitstellungsoptionen für die Verwendung der AgentSetup.exe-oder Windows Installer-Dateien (MSI).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Bereitstellungstyp</strong></th>
<th align="left"><strong>Bereitstellungs Beschreibung</strong></th>
<th align="left"><strong>Beispiel</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Eingabeaufforderung</p></td>
<td align="left"><p>Wenn Sie den UE-V-Agent an einer Eingabeaufforderung installieren, verwenden Sie das <em> Variable Format% ^ username% </em> . Wenn Anführungszeichen aufgrund von Leerzeichen im Einstellungsspeicher Pfad erforderlich sind, verwenden Sie eine Batchskriptdatei für die Bereitstellung.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Batch Skript</p></td>
<td align="left"><p>Wenn Sie den UE-V-Agent aus einer Batchskriptdatei installieren, verwenden Sie das <em> Variable Format%% username%% </em> . Wenn Sie diese Installationsmethode verwenden, müssen Sie der Variablen mit den%% Zeichen entkommen. Ohne dieses Zeichen erweitert das Skript die <em> Benutzername </em> -Variable zur Installationszeit anstatt zur Laufzeit, wodurch UE-V dazu veranlasst wird, einen einzelnen Einstellungs Speicherort für alle Benutzer zu verwenden.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell</p></td>
<td align="left"><p>Wenn Sie den UE-V-Agent über eine Windows PowerShell-Eingabeaufforderung oder ein Windows PowerShell-Skript installieren, verwenden Sie das <em> Variable Format% username% </em> .</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Elektronische Softwareverteilung, beispielsweise Bereitstellung der Configuration Manager-Softwarebereitstellung</p></td>
<td align="left"><p>Wenn Sie den UE-V-Agent mithilfe von Configuration Manager installieren, verwenden Sie das <em> Variablen Format ^% username ^% </em> .</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**Hinweis:**  
Die Installation des UE-v-Agents erfordert Administratorrechte, und der Computer erfordert einen Neustart, bevor der UE-v-Agent ausgeführt werden kann.



### <a href="" id="params"></a>Befehlszeilenparameter für die Bereitstellung von UE-V-Agents

Die Befehlszeilenparameter des UE-V-Agents lauten wie folgt:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Befehlszeilenparameter</strong></th>
<th align="left"><strong>Definition</strong></th>
<th align="left"><strong>Anmerkungen</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Help oder/h oder/?</p></td>
<td align="left"><p>Zeigt das Dialogfeld "AgentSetup.exe Verwendung" an.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>Gibt den UNC-Pfad (Universal Naming Convention) an, der definiert, wo die Einstellungen gespeichert werden.</p></td>
<td align="left"><div class="alert">
<strong>Wichtig</strong><br/><p>Sie müssen eine SettingsStoragePath in UE-v 2,1 und UE-v 2,1 SP1 angeben. Sie können die AdHomePath-Zeichenfolge festlegen, um anzugeben, dass der Active Directory-Start Pfad des Benutzers&#39;verwendet wird. Beispiel: <code>SettingsStoragePath = \share\path|AdHomePath</code>.</p>
<p>In UE-V 2,0 können Sie SettingsStoragePath leer lassen, um stattdessen den Active Directory-Start Pfad zu verwenden.</p>
</div>
<div>

</div>
<p>% Username% oder% Computername% Umgebungsvariablen werden akzeptiert. Für Skripting können maskierte Variablen erforderlich sein.</p>
<p><strong>Standard </strong> : &lt; keine&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsStoragePathReg</p></td>
<td align="left"><p>Ruft während der Installation den SettingsStoragePath-Wert aus der Registrierung ab.</p></td>
<td align="left"><p>Geben Sie an der Eingabeaufforderung Folgendes Beispiel ein, um UE-V zu zwingen, den Active Directory-Start Pfad anstelle eines bestimmten UNC-Pfads zu verwenden.</p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Gibt den UNC-Pfad (Universal Naming Convention) an, der den Speicherort definiert, der auf neue Einstellungen für Standort Vorlagen überprüft wurde.</p></td>
<td align="left"><p>Nur für benutzerdefinierte Einstellungen für Standort Vorlagen erforderlich</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Gibt an, ob die Microsoft-Standardvorlagen während der Installation registriert werden sollen.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Standard </strong> : true</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncMethod</p></td>
<td align="left"><p>Gibt an, welche Synchronisierungsmethode verwendet werden soll.</p></td>
<td align="left"><p>SyncProvider | Keine</p>
<p><strong>Standard </strong> : SyncProvider</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Gibt die Anzahl der Millisekunden an, die der Computer vor dem Timeout wartet, wenn er Benutzereinstellungen vom Speicherort für Einstellungen abruft.</p></td>
<td align="left"><p><strong>Standard </strong> : 2000 Millisekunden</p>
<p>(bis zu 2 Sekunden warten)</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Gibt an, ob die UE-V-Synchronisierung aktiviert oder deaktiviert ist.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Standard </strong> : true</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Gibt eine Dateigröße des Einstellungen-Pakets in Byte an, wenn der UE-V-Agent meldet, dass Dateien den Schwellenwert überschreiten.</p></td>
<td align="left"><p>&lt;Größe&gt;</p>
<p><strong>Standard </strong> : None (kein Warnungsschwellenwert)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Gibt die Einstellung für die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit an. Wenn die Einstellung <strong> auf </strong> "true" festgelegt ist, werden die Installationsinformationen auf die Microsoft-Website zur Verbesserung der Benutzerfreundlichkeit hochgeladen. Wenn Sie auf "false" festgelegt <strong> </strong> ist, werden keine Informationen hochgeladen.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Standard </strong> : falsch</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NoRestart</p></td>
<td align="left"><p>Unterstützt die Verzögerung des Neustarts des Computers, nachdem der UE-V-Agent installiert wurde.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>INSTALLFOLDER</p></td>
<td align="left"><p>Ermöglicht das Einstellen eines anderen Installationsordners für den UE-v-Agent oder UE-v-Generator.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>MUENABLED</p></td>
<td align="left"><p>Ermöglicht es Setup, die Option zu akzeptieren, die im Microsoft Update-Programm enthalten sein soll.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ACCEPTLICENSETERMS</p></td>
<td align="left"><p>Ermöglicht die unbeaufsichtigte Installation von UE-V. Diese muss auf "true" festgelegt werden <strong> </strong> , um UE-v im Hintergrund zu installieren und die Anforderung zu umgehen, dass der Benutzer die UE-v-Lizenzbedingungen akzeptiert. Wenn <strong> </strong> der Benutzer auf "false" festgelegt oder leer gelassen wird, erhält er eine Fehlermeldung, und UE-V ist nicht installiert.</p></td>
<td align="left"><div class="alert">
<strong>Wichtig</strong><br/><p>Dieser Parameter ist erforderlich, um UE-V im Hintergrund zu installieren.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>NORESTART</p></td>
<td align="left"><p>Verhindert einen obligatorischen Neustart nach der Installation des UE-V-Agents.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Aktualisieren des UE-V-Agents

Updates für die UE-V-Agent-Software werden über Microsoft Update bereitgestellt. Sie können UE-V-Agenten Updates mithilfe von ESD-Infrastruktursystemen (Enterprise Software Distribution) bereitstellen.

Während eines UE-V-Agent-Upgrades können die standardmäßigen Einstellungen für die Standort Vorlagen für allgemeine Microsoft-Anwendungen und Windows-Einstellungen aktualisiert werden.

### Upgrade des UE-V 2. x-Agents

Der UE-V 2. x-Agent führt viele neue Features ein und ändert, wie und wann der Agent Inhalte in die Speicherfreigabe für Einstellungen hochlädt. Der Upgradeprozess automatisiert diese Änderungen. Wenn Sie den UE-v-Agent aktualisieren möchten, führen Sie das UE-v-Agent-Installationspaket (AgentSetup.exe, AgentSetupx86.msi oder AgentSetupx64.msi) auf den Computern der Benutzer aus.

**Hinweis:**  
Wenn Sie den UE-v-Agent aktualisieren, müssen Sie denselben Installationstyp (exe-Datei oder MSI-Paket) verwenden, der den vorherigen UE-v-Agent installiert hat. Verwenden Sie beispielsweise die AgentSetup.exe UE-v 2, um UE-v 1,0-Agents zu aktualisieren, die mithilfe von AgentSetup.exe installiert wurden.



Die folgenden Konfigurationen bleiben erhalten, wenn das Agent-Setup Programm ausgeführt wird:

-   Speicherpfad für Einstellungen

-   Registrierungseinstellungen

-   Geplante Vorgänge (Intervalleinstellungen werden auf ihre Standardeinstellungen zurückgesetzt)

**Hinweis:**  
Ein Computer mit Standort Vorlagen für UE-v 2. x-Einstellungen, die bei der Registrierung des UE-v 1,0-Agents im Windows-Ereignisprotokoll registriert sind.



Sie können den Microsoft System Center 2012-Konfigurations-Manager oder ein anderes Tool für die Unternehmenssoftware Verteilung verwenden, um das Upgrade des UE-V-Agents zu automatisieren und zu verteilen.

**Empfehlungen:** Wir empfehlen, dass Sie alle UE-V 1,0-Agents in einer Computerumgebung aktualisieren, dies ist jedoch nicht erforderlich. Die Standort Vorlagen für die UE-v 2. x-Einstellungen können mit einem UE-v 1,0-Agent interagieren, da Sie nur die Einstellungen aus dem Speicherpfad für Einstellungen freigeben. Wir empfehlen jedoch, dass Sie die Bereitstellungen zu einer einzigen Agentenversion verschieben, um die Verwaltung zu vereinfachen und UE-V zu unterstützen.

### Reparieren des UE-V-Agents nach einem erfolglosen Upgrade

Nachdem Sie einen der folgenden Vorgänge ausgeführt haben, können Fehler auftreten:

-   Upgrade von UE-v 1,0 auf UE-v 2

-   Aktualisieren Sie auf eine neuere Version von Windows, beispielsweise von Windows 7 auf Windows 8 oder von Windows 8 auf Windows 8,1.

-   Deinstallieren des Agents nach dem Upgrade des UE-V-Agents

Um Probleme zu beheben, versuchen Sie, den UE-V-Agent zu reparieren, indem Sie diesen Befehl an einer Eingabeaufforderung auf dem Computer eingeben, auf dem der Agent installiert ist.

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

Sie können dann den Deinstallationsvorgang oder das Upgrade wiederholen, indem Sie die neuere Version des UE-V-Agents installieren.






## Verwandte Themen


[Vorbereiten einer UE-V 2. x-Bereitstellung](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









