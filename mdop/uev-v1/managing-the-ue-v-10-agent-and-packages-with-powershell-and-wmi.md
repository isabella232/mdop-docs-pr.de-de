---
title: Verwalten des UE-V 1.0-Agents und von Paketen mit PowerShell und WMI
description: Verwalten des UE-V 1.0-Agents und von Paketen mit PowerShell und WMI
author: dansimp
ms.assetid: c8989b01-1769-4e69-82b1-4aadb261d2d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79268e3384aaaf08bdd4e9b92d74b039ce96596a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807851"
---
# Verwalten des UE-V 1.0-Agents und von Paketen mit PowerShell und WMI


Sie können WMI und PowerShell verwenden, um die Konfiguration und das Synchronisierungsverhalten der Microsoft User Experience Virtualization (UE-V)-Agents zu verwalten.

**Bereitstellen des UE-V-Agents mit PowerShell**

1.  Stufen Sie die UE-V-Installationsdatei in einer barrierefreien Netzwerkfreigabe ein.

    **Hinweis:**  
    Verwenden Sie AgentSetup.exe, um sowohl 32-Bit-als auch 64-Bit-Versionen des UE-V-Agents bereitzustellen. Windows Installer-Dateien, AgentSetupx86.msi und AgentSetupx64.msi, stehen für jede Architektur zur Verfügung. Wenn Sie den UE-V-Agent zu einem späteren Zeitpunkt mit der Installationsdatei deinstallieren möchten, müssen Sie denselben Dateityp verwenden.



2.  Verwenden Sie einen der folgenden PowerShell-Befehle, um den Agenten zu installieren.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Konfigurieren des UE-V-Agents mit PowerShell**

1.  Verwenden Sie ein Konto mit Administratorrechten, um ein PowerShell-Fenster zu öffnen. Importieren Sie das UE-V PowerShell-Modul mithilfe des folgenden Befehls.

    ``` syntax
    Import-module UEV
    ```

2.  Verwenden Sie die folgenden PowerShell-Befehle zum Konfigurieren des Agents.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>PowerShell-Befehl</strong></p></td>
    <td align="left"><p><strong>Beschreibung</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration</p>
    <p></p></td>
    <td align="left"><p>Zeigen Sie die effektiven Einstellungen des UE-V-Agents an. Benutzerspezifische Einstellungen haben Vorrang vor den Computereinstellungen.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-UevConfiguration-CurrentComputerUser</p>
    <p></p></td>
    <td align="left"><p>Anzeigen der Einstellungen des UE-V-Agents nur für den aktuellen Benutzer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration-Computer</p></td>
    <td align="left"><p>Zeigen Sie die Werte für die Konfigurationseinstellungen des UE-V-Agents für alle Benutzer auf dem Computer an.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Satz-UevConfiguration-Computer-SettingsStoragePath &lt; Pfad zu _settings_storage_location&gt;</p></td>
    <td align="left"><p>Definieren Sie einen Speicherort für pro Computer-Einstellungen.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Satz-UevConfiguration-CurrentComputerUser-SettingsStoragePath- &lt; Pfad zu _settings_storage_location&gt;</p></td>
    <td align="left"><p>Definieren Sie einen Speicherort für benutzerspezifische Einstellungen.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UevConfiguration-Computer-SyncTimeoutInMilliseconds &lt; Timeout in Millisekunden&gt;</p></td>
    <td align="left"><p>Einstellen des Synchronisierungs Timeouts in Millisekunden</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds- &lt; Timeout in Millisekunden&gt;</p></td>
    <td align="left"><p>Setzen Sie das Synchronisierungs Timeout für den aktuellen Benutzer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Satz-UevConfiguration-Computer-MaxPackageSizeInBytes &lt; Größe in Bytes&gt;</p></td>
    <td align="left"><p>Konfigurieren Sie den UE-V-Agent so, dass er meldet, wenn die Dateigröße eines Einstellungen-Pakets einen definierten Schwellenwert erreicht. Festlegen der Größe des Schwellenwert Pakets in Bytes</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Satz-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; Größe in Bytes&gt;</p></td>
    <td align="left"><p>Festlegen des warnungsschwellenwerts für die Paketgröße für den aktuellen Benutzer</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Satz-UevConfiguration – Computer – SettingsTemplateCatalogPath &lt; Pfad zum Katalog&gt;</p></td>
    <td align="left"><p>Festlegen des Katalog Pfads für die Einstellungs Vorlage</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Satz-UevConfiguration-Computer-SyncMethod- &lt; Synchronisierungsmethode&gt;</p></td>
    <td align="left"><p>Setzen Sie die Synchronisierungsmethode: Offlinedateien oder None.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Satz-UevConfiguration-CurrentComputerUser-SyncMethod- &lt; Synchronisierungsmethode&gt;</p></td>
    <td align="left"><p>Stellen Sie die Synchronisierungsmethode für den aktuellen Benutzer ein: Offlinedateien oder None.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Satz-UEVConfiguration-Computer – EnableSettingsImportNotify</p></td>
    <td align="left"><p>Benachrichtigung kann auftreten, wenn der Import von Benutzereinstellungen verzögert wird.</p>
    <p>Verwenden Sie – DisableSettingsImportNotify, um die Benachrichtigung zu deaktivieren.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Satz-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</p></td>
    <td align="left"><p>Benachrichtigung für den aktuellen Benutzer aktivieren, wenn der Import von Benutzereinstellungen verzögert wird.</p>
    <p>Verwenden Sie – DisableSettingsImportNotify, um die Benachrichtigung zu deaktivieren.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Satz-UEVConfiguration-Computer-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Angeben der Uhrzeit in Sekunden, bevor der Benutzer benachrichtigt wird</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Satz-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Geben Sie die Zeitdauer in Sekunden vor der Benachrichtigung für den aktuellen Benutzer an.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Satz-UevConfiguration – Computer – DisableSync</p></td>
    <td align="left"><p>Deaktivieren Sie UE-V für alle Benutzer auf dem Computer.</p>
    <p>Verwenden Sie – EnableSync zum Aktivieren oder erneuten Aktivieren.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Satz-UevConfiguration – CurrentComputerUser-DisableSync</p></td>
    <td align="left"><p>Deaktivieren Sie UE-V für den aktuellen Benutzer auf dem Computer.</p>
    <p>Verwenden Sie – EnableSync zum Aktivieren oder erneuten Aktivieren.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Clear-UevConfiguration – Name der Computer &lt; Einstellung&gt;</p></td>
    <td align="left"><p>Deaktivieren Sie eine bestimmte Einstellung für alle Benutzer auf dem Computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Clear-UevConfiguration – CurrentComputerUser- &lt; Einstellungsname&gt;</p></td>
    <td align="left"><p>Deaktivieren Sie eine bestimmte Einstellung nur für den aktuellen Benutzer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Migrationsdatei für Export-UevConfiguration- &lt; Einstellungen&gt;</p></td>
    <td align="left"><p>Exportieren Sie die UE-V-Computerkonfiguration in eine Migrationsdatei für Einstellungen. Die Dateierweiterung muss ". UEV" sein.</p>
    <p>Mit dem Export-Cmdlet werden alle UE-V-Agent-Einstellungen exportiert, die mit dem-Computer-Parameter konfigurierbar sind.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Migrationsdatei für Import-UevConfiguration- &lt; Einstellungen&gt;</p></td>
    <td align="left"><p>Importieren Sie die UE-V-Computerkonfiguration aus einer Einstellungs Migrationsdatei (UEV-Datei).</p></td>
    </tr>
    </tbody>
    </table>



**Exportieren von UE-v-Paketeinstellungen und Reparieren von UE-v-Vorlagen mit PowerShell**

1.  Öffnen Sie ein PowerShell-Fenster als Administrator. Importieren Sie das UE-V PowerShell-Modul mit dem folgenden Befehl.

    ``` syntax
    Import-module UEV
    ```

2.  Verwenden Sie die folgenden PowerShell-Befehle zum Konfigurieren des Agents.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>PowerShell-Befehl</strong></p></td>
    <td align="left"><p><strong>Beschreibung</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Export-UevPackage MicrosoftCalculator6. pkgx</p></td>
    <td align="left"><p>Extrahiert die Einstellungen aus einer Microsoft Calculator-Paketdatei und wandelt sie in ein menschlich lesbares Format in XML um.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Reparieren-UevTemplateIndex</p></td>
    <td align="left"><p>Repariert den Index der Standort Vorlagen für UE-V-Einstellungen.</p></td>
    </tr>
    </tbody>
    </table>



**Konfigurieren des UE-V-Agents mit WMI**

1.  Die Virtualisierung der Benutzeroberfläche bietet die folgenden WMI-Befehle. Administratoren können diese Schnittstelle verwenden, um den UE-V-Agent über die Befehlszeile zu konfigurieren und typische Konfigurationsaufgaben zu automatisieren.

    Verwenden Sie ein Konto mit Administratorrechten, um ein PowerShell-Fenster zu öffnen.

2.  Verwenden Sie die folgenden WMI-Befehle zum Konfigurieren des Agents.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">PowerShell-Befehl</th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Get-WMIObject-Namespace-root\Microsoft\UEV-Konfiguration</p>
    <p></p></td>
    <td align="left"><p>Anzeigen der aktiven UE-V-Agenteneinstellungen Benutzerspezifische Einstellungen haben Vorrang vor den Computereinstellungen.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WMIObject-Namespace root\Microsoft\UEV UserConfiguration</p></td>
    <td align="left"><p>Anzeigen der für den benutzerdefinierten UE-V-Agent-Konfiguration.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</p></td>
    <td align="left"><p>Anzeigen der für den Computer definierten UE-V-Agent-Konfiguration.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Definieren Sie einen Speicherort für pro Computer-Einstellungen.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WMIObject-Namespace root\Microsoft\UEV UserConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Definieren Sie einen Speicherort für benutzerspezifische Einstellungen.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Setzen Sie das Synchronisierungs Timeout in Millisekunden.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Konfigurieren Sie den UE-V-Agent so, dass er meldet, wenn die Dateigröße eines Einstellungen-Pakets einen definierten Schwellenwert erreicht. Legen Sie die Schwellenwert-Paketdatei Größe in Bytes fest.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncMethod = &lt; sync_method&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Setzen Sie die Synchronisierungsmethode: Offlinedateien oder None.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; Einstellungs &gt;  =  &lt; Wert für Name&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Aktualisieren Sie eine bestimmte Einstellung pro Computer. Verwenden Sie $NULL als Einstellungswert, um die Einstellung zu löschen.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; Einstellungs &gt;  =  &lt; Wert für Name&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Aktualisieren einer bestimmten Einstellung für jeden Benutzer Verwenden Sie $NULL als Einstellungswert, um die Einstellung zu löschen.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## Verwandte Themen


[Verwalten von UE-V 1.0](administering-ue-v-10.md)

[Vorgänge für UE-V 1.0](operations-for-ue-v-10.md)









