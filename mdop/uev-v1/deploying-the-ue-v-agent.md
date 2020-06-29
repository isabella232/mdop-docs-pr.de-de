---
title: Bereitstellen von UE-V-Agent
description: Bereitstellen von UE-V-Agent
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812202"
---
# Bereitstellen von UE-V-Agent


Der Microsoft User Experience Virtualization (UE-v)-Agent muss auf jedem Computer ausgeführt werden, auf dem UE-v verwendet wird, um die Anwendungs-und Windows-Einstellungen zu durchlaufen. Eine einzelne Installationsdatei, AgentSetup.exe, installiert den UE-V-Agent sowohl auf 32-als auch 64-Bit-Betriebssystemen. Die Befehlszeilenparameter des UE-V-Agents lauten wie folgt:

**AgentSetup.exe Befehlszeilenparameter**

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
<td align="left"><p>% Username% oder% Computername% Umgebungsvariablen werden akzeptiert. Für Skripts sind möglicherweise Escape-Variablen erforderlich.</p>
<p><strong>Standard </strong> : &lt; None &gt; (Active Directory-Benutzer Start)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Gibt den UNC-Pfad (Universal Naming Convention) an, der den Speicherort definiert, der auf neue Einstellungen für Standort Vorlagen überprüft wurde.</p></td>
<td align="left"><p>Nur für benutzerdefinierte Einstellungen für Standort Vorlagen erforderlich</p></td>
</tr>
<tr class="even">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Gibt an, ob die Microsoft-Standardvorlagen während der Installation registriert werden sollen.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Standard </strong> : true</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncMethod</p></td>
<td align="left"><p>Gibt an, welche Synchronisierungsmethode verwendet werden soll.</p></td>
<td align="left"><p>Offlinedateien | Keine</p>
<p><strong>Standard </strong> : Offlinedateien</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Gibt die Anzahl der Millisekunden an, die der Computer vor dem Timeout wartet, wenn er Benutzereinstellungen vom Speicherort für Einstellungen abruft.</p></td>
<td align="left"><p><strong>Standard </strong> : 2000 Millisekunden</p>
<p>(bis zu 2 Sekunden warten)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Gibt an, ob die UE-V-Synchronisierung aktiviert oder deaktiviert ist.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Standard </strong> : true</p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Gibt eine Dateigröße des Einstellungen-Pakets in Byte an, wenn der UE-V-Agent meldet, dass Dateien den Schwellenwert überschreiten.</p></td>
<td align="left"><p>&lt;Größe&gt;</p>
<p><strong>Standard </strong> : None (kein Warnungsschwellenwert)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Gibt die Einstellung für die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit an. Wenn die Einstellung auf "true" festgelegt ist, werden die Installationsinformationen auf die Microsoft-Website zur Verbesserung der Benutzerfreundlichkeit hochgeladen. Wenn Sie auf "false" festgelegt ist, werden keine Informationen hochgeladen.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Standard </strong> : falsch</p>
<p><strong>Unter Windows 7 </strong> : true</p></td>
</tr>
</tbody>
</table>

 

Während der Installation gibt der SettingsStoragePath-Befehlszeilenparameter den Speicherort für Einstellungen für die Einstellungswerte an. Vor der Bereitstellung des UE-V-Agents kann ein Einstellungs Speicherort definiert werden. Wenn kein Speicherort für Einstellungen festgelegt ist, verwendet UE-V das Active Directory-Benutzerstammverzeichnis als Speicherort für Einstellungen. Wenn Sie während des Setups die SettingsStoragePath-Konfiguration angeben und den% username% als Teil des Werts verwenden, wird dadurch dieselbe Benutzereinstellungen-Oberfläche auf allen Computern oder Sitzungen durchlaufen, bei denen sich ein Benutzer anmeldet. Wenn Sie die%username%\\%Computername%-Variablen als Teil des SettingsStoragePath-Werts angeben, bleibt die Einstellungs Oberfläche für jeden Computer erhalten.

Architekturspezifische Windows Installer-Dateien (MSI) werden für die UE-V-Agent-Installation zusätzlich zum kombinierten 32-Bit-und 64-Bit-Installationsprogramm bereitgestellt. Die AgentSetupx86.msi-oder AgentSetupx64.msi Installationsdateien sind kleiner als die AgentSetup.exe Datei und können die Agenten Bereitstellungen rationalisieren. Die Befehlszeilenparameter für das AgentSetup.exe-Installationsprogramm werden für die Windows Installer-Installation (MSI) unterstützt.

**Hinweis**  Bei der Installation oder Deinstallation des UE-V-Agents können Sie entweder die AgentSetup.exe-Datei oder die Sie AgentSetup &lt; arch &gt; . msi-Datei verwenden, aber nicht beide. Die gleiche Datei muss verwendet werden, um den UE-v-Agent zu deinstallieren, wie er zum Installieren des UE-v-Agents verwendet wurde.

 

Achten Sie beim Installieren des UE-V-Agents darauf, das richtige Variablen Format zu verwenden. Die folgende Tabelle enthält Beispiele für Bereitstellungsoptionen für die Verwendung der AgentSetup.exe-oder Windows Installer-Installationsdateien (MSI).

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
<td align="left"><p>Wenn Sie den UE-V-Agent über eine Eingabeaufforderung installieren, verwenden Sie das Variable Format% ^ username%. Wenn Anführungszeichen aufgrund von Leerzeichen im Einstellungsspeicher Pfad erforderlich sind, verwenden Sie eine Batchskriptdatei für die Bereitstellung.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Batch Skript</p></td>
<td align="left"><p>Wenn Sie den UE-V-Agent aus einer Batchskriptdatei installieren, verwenden Sie das Variable Format%% username%%. Wenn Sie diese Installationsmethode verwenden, müssen Sie der Variablen mit den%% Zeichen entkommen. Ohne dieses Zeichen erweitert das Skript die Benutzername-Variable zum Zeitpunkt der Installation, anstatt zur Laufzeit, wodurch UE-V einen einzelnen Einstellungen-Speicherort für alle Benutzer verwendet.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Wenn Sie den UE-V-Agent über eine PowerShell-Eingabeaufforderung oder ein PowerShell-Skript installieren, verwenden Sie das Variable Format% username%.</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Elektronische Softwareverteilung, wie etwa die Bereitstellung der Configuration Manager-Softwarebereitstellung)</p></td>
<td align="left"><p>Verwenden Sie beim Installieren des UE-V-Agents mit Configuration Manager das Variablen Format ^% username ^%.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Für die Installation des U-EV-Agents sind Administrator Rechte erforderlich, und der Computer erfordert einen Neustart, bevor der UE-V-Agent ausgeführt werden kann.

 

## Bereitstellungsmethoden für UE-V-Agents von einer Netzwerkfreigabe


Sie können die folgenden Methoden zum Bereitstellen des UE-V-Agents verwenden:

-   Eine ESD-Lösung (Electronic Software Distribution), die eine Windows Installer-Datei (MSI) installieren kann.

-   Ein Installationsskript, das auf die Windows Installer-Datei (MSI) verweist, die zentral auf einer Freigabe gespeichert ist.

-   Manuelles Ausführen des Installationsprogramms auf dem Computer.

Führen Sie die folgenden Schritte aus, um den UE-V-Agent über eine Netzwerkfreigabe bereitzustellen:

**So installieren und konfigurieren Sie den UE-V-Agent über eine Netzwerkfreigabe**

1.  Stufen Sie die Installationsdatei des UE-V-Agents (AgentSetup.exe) auf einer Netzwerkfreigabe ein, auf die Benutzer die Berechtigung "lesen" haben.

2.  Stellen Sie ein Skript auf Benutzercomputern bereit, die den UE-V-Agent installieren. Das Skript sollte den Speicherort für Einstellungen angeben.

**Aktualisieren des UE-V-Agents**

Updates für die UE-V-Agent-Software werden über Microsoft Update bereitgestellt. Bei einem UE-V-Agent-Upgrade kann die Standardgruppe der Einstellungen für den Speicherort für allgemeine Microsoft-Anwendungen und Windows-Einstellungen aktualisiert werden. Updates für UE-V-Agents können mithilfe von ESD-Infrastruktur (Enterprise Software Distribution) bereitgestellt werden.

## Verwandte Themen


[Bereitstellen von UE-V 1.0](deploying-ue-v-10.md)

[Unterstützte Konfigurationen für UE-V 1.0](supported-configurations-for-ue-v-10.md)

[Bereitstellen des Speicherorts für die Einstellungen für UE-V 1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Installieren von UE-V-Generator](installing-the-ue-v-generator.md)

Bereitstellen des Benutzeroberflächen-Virtualisierungs-Agents
 

 





