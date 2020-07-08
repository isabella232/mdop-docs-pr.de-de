---
title: Verwalten des UE-V 2. x-Agents und der Pakete mit Windows PowerShell und WMI
description: Verwalten des UE-V 2. x-Agents und der Pakete mit Windows PowerShell und WMI
author: dansimp
ms.assetid: 56e6780b-8b2c-4717-91c8-2af63062ab75
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6a709d2c66266cf33b8e89ddd905aa0f21eb7dfe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811974"
---
# Verwalten des UE-V 2. x-Agents und der Pakete mit Windows PowerShell und WMI


Sie können Windows-Verwaltungsinstrumentation (WMI) und Windows PowerShell verwenden, um die Konfiguration und das Synchronisierungsverhalten von Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 zu verwalten. Eine vollständige Liste der UE-v PowerShell-Cmdlets finden Sie unter [UE-v 2-Cmdlet-Referenz](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .

**Bereitstellen des UE-V-Agents mithilfe von Windows PowerShell**

1.  Stufen Sie die UE-V-Installationsdatei in einer barrierefreien Netzwerkfreigabe ein.

    **Hinweis:**  
    Verwenden Sie AgentSetup.exe, um sowohl 32-Bit-als auch 64-Bit-Versionen des UE-V-Agents bereitzustellen. Windows Installer-Pakete, AgentSetupx86.msi und AgentSetupx64.msi, stehen für jede Architektur zur Verfügung. Wenn Sie den UE-V-Agent zu einem späteren Zeitpunkt mithilfe der Installationsdatei deinstallieren möchten, müssen Sie denselben Dateityp verwenden.



2.  Verwenden Sie einen der folgenden Windows PowerShell-Befehle, um den UE-V-Agent zu installieren.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**So konfigurieren Sie den UE-V-Agent mithilfe von Windows PowerShell**

1. Öffnen Sie ein Windows PowerShell-Fenster. Öffnen Sie das Fenster mit einem Konto, das über Administratorrechte verfügt, um Computereinstellungen zu verwalten, die sich auf alle Benutzer des Computers auswirken, indem Sie den Parameter *Computer* verwenden.

2. Verwenden Sie die folgenden Windows PowerShell-Befehle zum Konfigurieren des Agents.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Windows PowerShell-Befehl</th>
   <th align="left">Beschreibung</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p>Ruft die effektiven Einstellungen des UE-V-Agents ab. Benutzerspezifische Einstellungen haben Vorrang vor den Computereinstellungen.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p>Ruft die Einstellungen des UE-V-Agents nur für den aktuellen Benutzer ab.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p>Ruft die Werte für die Konfigurationseinstellungen des UE-V-Agents für alle Benutzer auf dem Computer ab.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p>Ruft die Details für jede Konfigurationseinstellung ab. Zeigt an, wo die Einstellung konfiguriert ist oder ob Sie den Standardwert verwendet. Wird angezeigt, wenn die aktuelle Einstellung gültig ist.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p>Legt den Text fest, der im Unternehmenseinstellungen-Center für den Link "Hilfe" angezeigt wird.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p>Legt die URL des Links im Unternehmenseinstellungen-Center für den Link Hilfe fest. Jedes URL-Protokoll kann verwendet werden.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Konfiguriert den UE-V-Agent so, dass keine Windows-Apps für alle Benutzer auf dem Computer synchronisiert werden.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Konfiguriert den UE-V-Agent so, dass keine Windows-Apps für den aktuellen Computer Benutzer synchronisiert werden.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p>Konfiguriert den UE-V-Agent so, dass die Benachrichtigung angezeigt wird, wenn der Agent zum ersten Mal für alle Benutzer auf dem Computer ausgeführt wird.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p>Konfiguriert den UE-V-Agent so, dass keine Benachrichtigung angezeigt wird, wenn der Agent zum ersten Mal für alle Benutzer auf dem Computer ausgeführt wird.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Konfiguriert den UE-V-Agent so, dass alle Benutzer auf dem Computer benachrichtigt werden, wenn die Synchronisierung der Einstellungen verzögert wird.</p>
   <p>Verwenden Sie den <em> DisableSettingsImportNotify </em> -Parameter, um die Benachrichtigung zu deaktivieren.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Konfiguriert den UE-V-Agent so, dass der aktuelle Benutzer benachrichtigt wird, wenn die Synchronisierung der Einstellungen verzögert wird.</p>
   <p>Verwenden Sie den <em> DisableSettingsImportNotify </em> -Parameter, um die Benachrichtigung zu deaktivieren.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Konfiguriert den UE-V-Agent so, dass alle Windows-apps synchronisiert werden, die nicht explizit durch die Windows-App-Liste für alle Benutzer des Computers deaktiviert sind. Weitere Informationen finden Sie unter &quot; Get-UevAppxPackage &quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Verwalten von Standort Vorlagen für die Einstellungen für UE-V 2. x mit Windows PowerShell und WMI </a> .</p>
   <p>Verwenden Sie den <em> DisableSyncUnlistedWindows8Apps </em> -Parameter, um den UE-V-Agent so zu konfigurieren, dass nur Windows-apps synchronisiert werden, die explizit von der Windows-App-Liste aktiviert werden.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Konfiguriert den UE-V-Agent so, dass alle Windows-apps synchronisiert werden, die nicht explizit durch die Windows-App-Liste für den aktuellen Benutzer auf dem Computer deaktiviert sind. Weitere Informationen finden Sie unter &quot; Get-UevAppxPackage &quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Verwalten von Standort Vorlagen für die Einstellungen für UE-V 2. x mit Windows PowerShell und WMI </a> .</p>
   <p>Verwenden Sie den <em> DisableSyncUnlistedWindows8Apps </em> -Parameter, um den UE-V-Agent so zu konfigurieren, dass nur Windows-apps synchronisiert werden, die explizit von der Windows-App-Liste aktiviert werden.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p>Deaktiviert UE-V für alle Benutzer auf dem Computer.</p>
   <p>Verwenden Sie den <em> EnableSync </em> -Parameter zum Aktivieren oder erneuten Aktivieren.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p>Deaktiviert UE-V für den aktuellen Benutzer auf dem Computer.</p>
   <p>Verwenden Sie den <em> EnableSync </em> -Parameter zum Aktivieren oder erneuten Aktivieren.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p>Aktiviert das UE-V-Symbol im Infobereich für alle Benutzer des Computers.</p>
   <p>Verwenden Sie den <em> DisableTrayIcon </em> -Parameter, um das Symbol zu deaktivieren.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Konfiguriert den UE-V-Agent so, dass er meldet, wenn die Dateigröße des Einstellungen-Pakets den festgelegten Schwellenwert für alle Benutzer auf dem Computer erreicht. Legt die Größe des Schwellenwert Pakets in Bytes fest.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Konfiguriert den UE-V-Agent so, dass er meldet, wenn die Dateigröße des Einstellungen-Pakets den definierten Schwellenwert erreicht hat. Legt den Schwellenwert für die Paketgrößen Warnung für den aktuellen Benutzer fest.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Gibt die Zeit in Sekunden an, bevor der Benutzer für alle Benutzer des Computers benachrichtigt wird.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Gibt die Zeitdauer in Sekunden an, bevor die Benachrichtigung für den aktuellen Benutzer gesendet wird.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Definiert einen Speicherplatz für computerspezifische Einstellungen für alle Benutzer des Computers.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Definiert einen Speicherort für benutzerspezifische Einstellungen.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p>Legt den Katalogpfad der Einstellungs Vorlage für alle Benutzer des Computers fest.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Legt die Synchronisierungsmethode für alle Benutzer des Computers fest: SyncProvider oder None.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Legt die Synchronisierungsmethode für den aktuellen Benutzer fest: SyncProvider oder None.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Legt das Synchronisierungs Timeout in Millisekunden für alle Benutzer des Computers fest.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Das Synchronisierungs Timeout für den aktuellen Benutzer festzulegen.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Löscht die angegebene Einstellung für alle Benutzer auf dem Computer.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Löscht die angegebene Einstellung nur für den aktuellen Benutzer.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Exportiert die UE-V-Computerkonfiguration in eine Migrationsdatei für Einstellungen. Die Dateinamenerweiterung muss UEV sein.</p>
   <p>Das <code>Export</code> Cmdlet exportiert alle UE-V-Agenteneinstellungen, die mit dem <em> Computer </em> Parameter konfigurierbar sind.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Importiert die UE-V-Computerkonfiguration aus einer Migrationsdatei für Einstellungen. Die Dateinamenerweiterung muss UEV sein.</p></td>
   </tr>
   </tbody>
   </table>



**So exportieren Sie UE-v-Paketeinstellungen und reparieren UE-v-Vorlagen mithilfe von Windows PowerShell**

1.  Öffnen Sie ein Windows PowerShell-Fenster als Administrator.

2.  Verwenden Sie die folgenden Windows PowerShell-Befehle zum Konfigurieren des Agents.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Windows PowerShell-Befehl</strong></p></td>
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



**So konfigurieren Sie den UE-V-Agent mithilfe von WMI**

1.  Die Virtualisierung der Benutzeroberfläche bietet die folgenden WMI-Befehle. Administratoren können diese Schnittstelle verwenden, um den UE-V-Agent über die Befehlszeile zu konfigurieren und typische Konfigurationsaufgaben zu automatisieren.

    Verwenden Sie ein Konto mit Administratorrechten, um ein Windows PowerShell-Fenster zu öffnen.

2.  Verwenden Sie die folgenden WMI-Befehle zum Konfigurieren des Agents.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p>Zeigt die aktiven UE-V-Agenteneinstellungen an. Benutzerspezifische Einstellungen haben Vorrang vor den Computereinstellungen.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p>Zeigt die für einen benutzerdefinierte UE-V-Agent-Konfiguration an.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p>Zeigt die für einen Computer definierte UE-V-Agent-Konfiguration an.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p>Zeigt die Details für jedes Konfigurationselement an.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Definiert einen Speicherort für pro Computer-Einstellungen.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Definiert einen Speicherort für benutzerspezifische Einstellungen.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Legt das Synchronisierungs Timeout in Millisekunden für alle Benutzer des Computers fest.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Konfiguriert den UE-V-Agent so, dass er meldet, wenn die Dateigröße eines Einstellungen-Pakets einen festgelegten Schwellenwert erreicht. Legen Sie die Schwellenwert-Paketdatei Größe in Bytes für alle Benutzer des Computers fest.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Legt die Synchronisierungsmethode für alle Benutzer des Computers fest: SyncProvider oder None.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Wenn Sie eine bestimmte Einstellung pro Computer aktivieren möchten, deaktivieren Sie die Einstellung, und verwenden Sie <em> $NULL </em> als Einstellungswert. Verwenden Sie UserConfiguration für benutzerspezifische Einstellungen.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Wenn Sie eine bestimmte Einstellung pro Computer deaktivieren möchten, deaktivieren Sie die Einstellung, und verwenden Sie <em> $NULL </em> als Einstellungswert. Verwenden Sie die Benutzerkonfiguration für benutzerspezifische Einstellungen.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Aktualisiert eine bestimmte Einstellung pro Computer. Verwenden Sie <em> $null als Einstellungswert, um die Einstellung zu löschen </em> .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code>$config. &lt; Einstellungs &gt;  =  &lt; Wert für Name&gt;</p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Aktualisiert eine bestimmte pro-Benutzer-Einstellung für alle Benutzer des Computers. Verwenden Sie <em> $null als Einstellungswert, um die Einstellung zu löschen </em> .</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**So exportieren Sie UE-v-Paketeinstellungen und reparieren UE-v-Vorlagen mithilfe von WMI**

1.  UE-V bietet den folgenden Satz von WMI-Befehlen. Administratoren können diese Schnittstelle verwenden, um ein Paket zu exportieren oder UE-V-Vorlagen zu reparieren.

2.  Verwenden Sie die folgenden WMI-Befehle.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">WMI-Befehl</th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p>Extrahiert die Einstellungen aus einer Paketdatei und wandelt sie in ein menschlich lesbares Format in XML um.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p>Repariert den Index der Standort Vorlagen für UE-V-Einstellungen. Muss als Administrator ausgeführt werden.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## Verwandte Themen


[Verwalten von UE-V 2. x mit Windows PowerShell und WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









