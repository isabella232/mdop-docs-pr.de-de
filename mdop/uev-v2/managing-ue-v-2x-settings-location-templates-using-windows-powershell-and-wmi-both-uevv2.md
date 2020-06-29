---
title: Verwalten von Standort Vorlagen für die UE-V 2. x-Einstellungen mithilfe von Windows PowerShell und WMI
description: Verwalten von Standort Vorlagen für die UE-V 2. x-Einstellungen mithilfe von Windows PowerShell und WMI
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804559"
---
# Verwalten von Standort Vorlagen für die UE-V 2. x-Einstellungen mithilfe von Windows PowerShell und WMI


Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 verwenden Sie Vorlagen für XML-Einstellungen, um die Einstellungen zu definieren, die von der Benutzer Experience Virtualization erfasst und angewendet werden. UE-V enthält eine Reihe von Standardeinstellungen für Standort Vorlagen. Es enthält auch das UE-V-Generator Tool, mit dem Sie benutzerdefinierte Speicherort Vorlagen für Einstellungen erstellen können. Nachdem Sie die Vorlagen für Speicherort für Einstellungen erstellt und bereitgestellt haben, können Sie diese Vorlagen mithilfe von Windows PowerShell und der Windows-Verwaltungsinstrumentation (WMI) verwalten. Eine vollständige Liste der UE-v PowerShell-Cmdlets finden Sie unter [UE-v 2-Cmdlet-Referenz](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .

## Verwalten von Standort Vorlagen für die UE-V 2-Einstellungen mithilfe von Windows PowerShell


Die WMI-und Windows PowerShell-Features von UE-V umfassen die Möglichkeit, Einstellungen für Standort Vorlagen zu aktivieren, zu deaktivieren, zu registrieren, zu aktualisieren und die Registrierung aufzuheben. Mithilfe dieser Features können Sie den Prozess der Registrierung, Aktualisierung oder Aufheben der Registrierung von Vorlagen mit dem UE-V-Agent automatisieren. Sie können Vorlagen auch manuell mithilfe von WMI-und Windows PowerShell-Befehlen registrieren. Wenn Sie diese Features in Verbindung mit einer Lösung für die elektronische Softwareverteilung, einer Gruppenrichtlinie oder einer anderen automatisierten Bereitstellungsmethode wie einem Skript verwenden, können Sie diesen Prozess weiter automatisieren.

Sie müssen über Administratorberechtigungen verfügen, um eine Einstellungs Speicherort Vorlage zu aktualisieren, zu registrieren oder die Registrierung aufzuheben. Zum Aktivieren, deaktivieren oder Auflisten von Vorlagen sind keine Administrator Berechtigungen erforderlich.

***<em>So verwalten Sie Einstellungen für Standort Vorlagen mithilfe von Windows PowerShellell</em>***

1.  Verwenden Sie ein Konto mit Administratorrechten, um eine Windows PowerShell-Eingabeaufforderung zu öffnen.

2.  Verwenden Sie die folgenden Windows PowerShell-Cmdlets zum Registrieren und Verwalten der Standort Vorlagen für UE-V-Einstellungen.

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
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p>Listet alle Einstellungen-Speicherort Vorlagen auf, die auf dem Computer registriert sind.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p>Listet alle Einstellungen-Speicherort Vorlagen auf, die auf dem Computer registriert sind, auf dem der Anwendungsname oder der Vorlagenname eine &lt; Zeichenfolge enthält &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p>Listet alle Einstellungen-Standort Vorlagen auf, die auf dem Computer registriert sind, auf dem die Vorlagen-ID eine &lt; Zeichenfolge enthält &gt; .</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p>Listet alle Einstellungen-Speicherort Vorlagen auf, die auf dem Computer registriert sind, auf dem der Anwendungs-oder Vorlagenname oder die Vorlagen-ID eine &lt; Zeichenfolge enthält &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Ruft den Namen des Programms und der Versionsinformationen ab, die von der Vorlagen-ID abhängen.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p>Ruft die effektive Liste der Windows-apps ab.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p>Ruft die Liste der Windows-apps ab, die für den Computer konfiguriert sind.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Ruft die Liste der Windows-apps ab, die für den aktuellen Benutzer konfiguriert sind.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Registriert eine oder mehrere Einstellungen Speicherort Vorlage mit UE-V, indem relative Pfade und/oder Platzhalterzeichen in Dateipfaden verwendet werden. Nachdem eine Vorlage registriert wurde, synchronisiert UE-V die in der Vorlage definierten Einstellungen zwischen Computern, auf denen die Vorlage registriert ist.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Registriert eine oder mehrere Einstellungen Speicherort Vorlage mit UE-V mithilfe von literalen Pfaden, in denen keine Zeichen als Platzhalterzeichen interpretiert werden können. Nachdem eine Vorlage registriert wurde, synchronisiert UE-V die in der Vorlage definierten Einstellungen zwischen Computern, auf denen die Vorlage registriert ist.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Hebt die Registrierung einer Einstellungs Speicherort Vorlage mit UE-V auf. Wenn eine Vorlage nicht registriert ist, synchronisiert UE-V nicht mehr die Einstellungen, die in der Vorlage zwischen Computern definiert sind.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p>Hebt die Registrierung aller Einstellungen-Standort Vorlagen mit UE-V auf. Wenn eine Vorlage nicht registriert ist, synchronisiert UE-V nicht mehr die Einstellungen, die in der Vorlage zwischen Computern definiert sind.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Aktualisiert eine oder mehrere Einstellungen-Speicherort Vorlagen mit einer neueren Version der Vorlage. Verwenden Sie relative Pfade und/oder Platzhalterzeichen in den Dateipfaden. Die neue Vorlage sollte eine neuere Version als die vorhandene Vorlage sein.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Aktualisiert eine oder mehrere Einstellungen-Speicherort Vorlagen mit einer neueren Version der Vorlage. Verwenden Sie vollständige Pfade für Vorlagendateien, bei denen keine Zeichen als Platzhalterzeichen interpretiert werden können. Die neue Vorlage sollte eine neuere Version als die vorhandene Vorlage sein.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Entfernt eine oder mehrere Windows-Apps aus der Windows-App-Liste der Computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Entfernt die Windows-App aus der Windows-App-Liste der aktuellen Benutzer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p>Entfernt alle Windows-Apps aus der Windows-App-Liste der Computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Entfernt eine oder mehrere Windows-Apps aus der Windows-App-Liste der aktuellen Benutzer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p>Entfernt alle Windows-Apps aus der Windows-App-Liste der aktuellen Benutzer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Deaktiviert eine Vorlage für den Einstellungs Speicherort für den aktuellen Benutzer des Computers.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Deaktiviert eine oder mehrere Windows-apps in der Windows-App-Liste der Computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Deaktiviert eine oder mehrere Windows-apps in der Windows-App-Liste der aktuellen Benutzer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Aktiviert eine Vorlage für Einstellungs Speicherort für den aktuellen Benutzer des Computers.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Aktiviert mindestens eine Windows-app in der Liste der Computer-Windows-apps.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Aktiviert eine oder mehrere Windows-apps in der Windows-App-Liste der aktuellen Benutzer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Bestimmt, ob eine oder mehrere Einstellungen-Speicherort Vorlagen dem XML-Schema entsprechen. Relative Pfade und Platzhalterzeichen können verwendet werden.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Bestimmt, ob eine oder mehrere Einstellungen-Speicherort Vorlagen dem XML-Schema entsprechen. Der Pfad muss ein vollständiger Pfad zur Vorlagendatei sein, enthält jedoch keine Platzhalterzeichen.</p></td>
    </tr>
    </tbody>
    </table>



Mit den UE-V Windows PowerShell-Features können Sie eine Gruppe von Einstellungs Vorlagen verwalten, die in Ihrem Unternehmen bereitgestellt werden. Gehen Sie wie folgt vor, um eine Gruppe von Vorlagen mithilfe von Windows PowerShell zu verwalten.

**So verwalten Sie eine Gruppe von Einstellungen für Standort Vorlagen mithilfe von Windows PowerShell**

1.  Ändern oder aktualisieren Sie die Speicherort Vorlagen für die gewünschten Einstellungen.

2.  Wenn Sie die Einstellungen-Speicherort Vorlagen ändern oder aktualisieren möchten, stellen Sie die Speicherort Vorlagen für Einstellungen in einem Ordner bereit, auf den der lokale Computer zugreifen kann.

3.  Öffnen Sie auf dem lokalen Computer ein Windows PowerShell-Fenster mit Administratorrechten.

4.  Heben Sie die Registrierung aller zuvor registrierten Versionen der Vorlagen auf, indem Sie den folgenden Befehl eingeben.

    ``` syntax
    Unregister-UevTemplate -All
    ```

    Mit diesem Befehl werden alle aktiven Vorlagen auf dem Computer aufgehoben.

5.  Registrieren Sie die aktualisierten Vorlagen, indem Sie den folgenden Befehl eingeben.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Dieser Befehl registriert alle Einstellungen-Standort Vorlagen, die sich im angegebenen Vorlagenordner befinden.

### <a href="" id="win8applist"></a>Windows-App-Liste

Durch Auflisten einer Windows-app in der Windows-App-Liste geben Sie an, ob die APP für die Synchronisierung von Einstellungen aktiviert oder deaktiviert ist. Apps werden in der Liste nach dem Namen der paketfamilie identifiziert und festgelegt, ob die Synchronisierung der Einstellungen für diese APP aktiviert oder deaktiviert werden soll. Wenn Sie diese Einstellungen zusammen mit der Einstellung für das Standard Synchronisierungsverhalten nicht aufgelistet verwenden, können Sie steuern, ob Windows-apps synchronisiert werden.

Wenn Sie den Namen der paketfamilie von installierten Windows-apps anzeigen möchten, geben Sie an einer Windows PowerShell-Eingabeaufforderung Folgendes ein:

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

Um eine Liste der Windows-apps anzuzeigen, die die Einstellungen auf einem Computer mit dem Namen der paketfamilie, dem aktivierten Status und der aktivierten Quelle synchronisieren können, geben Sie an einer Windows PowerShell-Eingabeaufforderung Folgendes ein: `Get-UevAppxPackage`

**Definitionen von Get-UevAppxPackage-Eigenschaften**

<a href="" id="displayname"></a>**DisplayName**  
Der Name, der dem Benutzer in der Anwendung "Unternehmenseinstellungen Center" angezeigt wird. Die `DisplayName` Eigenschaft wird von der `PackageFamilyName` Eigenschaft abgeleitet.

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
Der Name des Pakets, das für den aktuellen Benutzer installiert ist.

<a href="" id="enabled"></a>**Aktiviert**  
Definiert, ob die Einstellungen für die APP für die Synchronisierung konfiguriert sind.

<a href="" id="enabledsource"></a>**EnabledSource**  
Der Speicherort, an dem die Konfiguration, die die App aktiviert oder deaktiviert, festgesetzt ist. Mögliche Werte sind: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*und *PolicyUser*.

<a href="" id="notset"></a>**NotSet**  
Die Richtlinie ist nicht für die Synchronisierung dieser APP konfiguriert.

<a href="" id="localmachine"></a>**LocalMachine**  
Der Status "aktiviert" wird im Abschnitt "lokaler Computer" der Registrierung festgesetzt.

<a href="" id="localuser"></a>**LocalUser**  
Der Status "aktiviert" wird im Abschnitt "aktueller Benutzer" der Registrierung festgesetzt.

<a href="" id="policymachine"></a>**PolicyMachine**  
Der Status "aktiviert" wird im Abschnitt "Richtlinie" des Abschnitts "lokaler Computer" der Registrierung festgesetzt.

Um die Benutzer konfigurierte Liste der Windows-apps abzurufen, geben Sie an der Windows PowerShell-Eingabeaufforderung Folgendes ein: `Get-UevAppxPackage –CurrentComputerUser`

Um die Computer konfigurierte Liste der Windows-apps abzurufen, geben Sie an der Windows PowerShell-Eingabeaufforderung Folgendes ein: `Get-UevAppxPackage –Computer`

Für Parameter, CurrentComputerUser oder Computer gibt das Cmdlet eine Liste der Windows-apps zurück, die auf dem Benutzer oder auf Computerebene konfiguriert sind.

**Definitionen von Eigenschaften**

<a href="" id="displayname"></a>**DisplayName**  
Der Name, der dem Benutzer in der Anwendung "Unternehmenseinstellungen Center" angezeigt wird. Die `DisplayName` Eigenschaft wird von der `PackageFamilyName` Eigenschaft abgeleitet.

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
Der Name des Pakets, das für den aktuellen Benutzer installiert ist.

<a href="" id="enabled"></a>**Aktiviert**  
Definiert, ob die Einstellungen für die APP für die Synchronisierung für den angegebenen Schalter ( **Benutzer** oder **Computer**) konfiguriert sind.

<a href="" id="installed"></a>**Installiert**  
"True", wenn die APP, also die PackageFamilyName, für den aktuellen Benutzer installiert ist.

### Verwalten von Standort Vorlagen für die UE-V 2-Einstellungen mithilfe von WMI

Die Virtualisierung der Benutzeroberfläche bietet die folgenden WMI-Befehle. Administratoren können diese Schnittstellen zum Verwalten von Einstellungen für Standort Vorlagen aus Windows PowerShell und zum Automatisieren von administrativen Vorlagen Aufgaben verwenden.

**So verwalten Sie Einstellungen für Standort Vorlagen mithilfe von WMI**

1.  Verwenden Sie ein Konto mit Administratorrechten, um ein Windows PowerShell-Fenster zu öffnen.

2.  Verwenden Sie die folgenden WMI-Befehle zum Registrieren und Verwalten der Standort Vorlagen für UE-V-Einstellungen.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p>Listet alle Einstellungen-Speicherort Vorlagen auf, die für den Computer registriert sind.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p>Ruft den Namen des Programms und die Versionsinformationen ab, die vom Vorlagennamen abhängen.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p>Ruft die effektive Liste der Windows-apps ab.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WMIObject-Namespace root\Microsoft\UEV MachineConfiguredWindows8App</p></td>
    <td align="left"><p>Ruft die Liste der Windows-apps ab, die für den Computer konfiguriert sind.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p>Ruft die Liste der Windows-apps ab, die für den aktuellen Benutzer konfiguriert sind.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p>Registriert eine Speicherort Vorlage für Einstellungen mit UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Hebt die Registrierung einer Einstellungs Speicherort Vorlage mit UE-V auf. Sobald eine Vorlage aufgehoben wurde, synchronisiert UE-V nicht mehr die Einstellungen, die in der Vorlage zwischen Computern definiert sind.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Aktualisiert eine Vorlage für Einstellungs Speicherort mit UE-V. Die neue Vorlage sollte eine neuere Version als die vorhandene sein.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Entfernt eine oder mehrere Windows-Apps aus der Windows-App-Liste der Computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Entfernt eine oder mehrere Windows-Apps aus der Windows-App-Liste der aktuellen Benutzer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Deaktiviert eine oder mehrere Einstellungen-Standort Vorlagen mit UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Deaktiviert eine oder mehrere Windows-apps in der Windows-App-Liste der Computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Deaktiviert eine oder mehrere Windows-apps in der Windows-App-Liste der aktuellen Benutzer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Aktiviert eine Einstellungs Speicherort Vorlage mit UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Aktiviert Windows-apps in der Windows-App-Liste der Computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Aktiviert Windows-apps in der Windows-App-Liste der aktuellen Benutzer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Bestimmt, ob eine angegebene Speicherort Vorlage für Einstellungen dem XML-Schema entspricht.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### Bereitstellen des UE-V-Agents mithilfe von Windows PowerShell

**Bereitstellen des UE-V-Agents mithilfe von Windows PowerShell**

1.  Stufen Sie das Installationspaket des UE-V-Agents in einer barrierefreien Netzwerkfreigabe ein.

    **Hinweis:**  
    Verwenden Sie AgentSetup.exe, um sowohl 32-Bit-als auch 64-Bit-Versionen des UE-V-Agents bereitzustellen. Die Windows Installer-Pakete, AgentSetupx86.msi und AgentSetupx64.msi, stehen für jede Architektur zur Verfügung. Wenn Sie den UE-V-Agent zu einem späteren Zeitpunkt mithilfe der Installationsdatei deinstallieren möchten, müssen Sie denselben Dateityp verwenden.



2.  Verwenden Sie einen der folgenden Windows PowerShell-Befehle, um den UE-V-Agent zu installieren.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

Sie **haben einen Vorschlag für UE-V**? [Hier](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Haben Sie ein UE-V-Problem**? Verwenden Sie das [UE-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Verwandte Themen


[Verwalten von UE-V 2. x mit Windows PowerShell und WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









