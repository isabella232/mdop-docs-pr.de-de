---
title: Verwalten von UE-V 1.0-Speicherortvorlagen mithilfe von PowerShell und WMI
description: Verwalten von UE-V 1.0-Speicherortvorlagen mithilfe von PowerShell und WMI
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804268"
---
# Verwalten von UE-V 1.0-Speicherortvorlagen mithilfe von PowerShell und WMI


Microsoft User Experience Virtualization (UE-V) verwendet Einstellungen-Standort Vorlagen (XML-Dateien), die die Einstellungen definieren, die von der Benutzeroberflächen-Virtualisierung erfasst und angewendet werden. UE-V enthält eine Reihe von Standardeinstellungen für Standort Vorlagen. Es enthält auch das UE-V-Generator Tool, mit dem Sie benutzerdefinierte Speicherort Vorlagen für Einstellungen erstellen können. Nach dem Erstellen und Bereitstellen von Einstellungen für Speicherort Vorlagen können Sie diese Vorlagen mithilfe von PowerShell oder WMI verwalten.

## Verwalten von Speicherort Vorlagen für Einstellungen mit WMI und PowerShell


Zu den WMI-und PowerShell-Features von UE-V gehören die Möglichkeit zum Aktivieren, deaktivieren, registrieren, aktualisieren und Aufheben der Registrierung von Einstellungen für Standort Vorlagen. Mithilfe dieser Features können Sie den Prozess der Registrierung, Aktualisierung oder Aufheben der Registrierung von Vorlagen mit dem UE-V-Agent automatisieren. Sie können Vorlagen auch manuell mithilfe von WMI-und PowerShell-Befehlen registrieren. Wenn Sie diese Features in Verbindung mit einer Lösung für die elektronische Softwareverteilung, einer Gruppenrichtlinie oder einer anderen automatisierten Bereitstellungsmethode wie einem Skript verwenden, können Sie diesen Prozess weiter automatisieren.

Sie müssen über Administratorberechtigungen verfügen, um eine Einstellungs Speicherort Vorlage zu aktualisieren, zu registrieren oder die Registrierung aufzuheben. Zum Aktivieren oder Deaktivieren von Vorlagen sind keine Administrator Berechtigungen erforderlich.

**So verwalten Sie Einstellungen für Standort Vorlagen mit PowerShell**

1.  Verwenden Sie ein Konto mit Administratorrechten, um ein Windows PowerShell-Fenster zu öffnen. Zum Importieren des **Microsoft UE-V PowerShell-** Moduls geben Sie an der PowerShell-Eingabeaufforderung den folgenden Befehl ein.

    ``` syntax
    Import-module UEV
    ```

2.  Verwenden Sie die folgenden PowerShell-Cmdlets zum Registrieren und Verwalten der Standort Vorlagen für UE-V-Einstellungen.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>PowerShell-Befehl</strong></th>
    <th align="left"><strong>Beschreibung</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Get-UevTemplate</p></td>
    <td align="left"><p>Listet alle auf dem Computer registrierten Einstellungen für Standort Vorlagen auf.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Registrieren-UevTemplate</p></td>
    <td align="left"><p>Registriert eine Speicherort Vorlage für Einstellungen mit UE-V. Nachdem eine Vorlage registriert wurde, synchronisiert UE-V die in der Vorlage definierten Einstellungen zwischen Computern, auf denen die Vorlage registriert ist.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Registrierung aufheben-UevTemplate</p></td>
    <td align="left"><p>Hebt die Registrierung einer Einstellungs Speicherort Vorlage mit UE-V auf. Sobald eine Vorlage aufgehoben wurde, synchronisiert UE-V nicht mehr die Einstellungen, die in der Vorlage zwischen Computern definiert sind.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Update-UevTemplate</p></td>
    <td align="left"><p>Aktualisiert eine Vorlage für Einstellungs Speicherort mit einer neueren Version der Vorlage. Die neue Vorlage sollte eine neuere Version als die vorhandene aufweisen.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Deaktivieren-UevTemplate</p></td>
    <td align="left"><p>Deaktiviert eine Vorlage für den Einstellungs Speicherort für den aktuellen Benutzer des Computers.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Enable-UevTemplate</p></td>
    <td align="left"><p>Aktiviert eine Vorlage für Einstellungs Speicherort für den aktuellen Benutzer des Computers.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Test-UevTemplate</p></td>
    <td align="left"><p>Bestimmt, ob eine angegebene Speicherort Vorlage für Einstellungen dem XML-Schema entspricht.</p></td>
    </tr>
    </tbody>
    </table>

     

Mit den UE-V PowerShell-Features können Sie eine Gruppe von Einstellungs Vorlagen verwalten, die in Ihrem Unternehmen bereitgestellt werden. Gehen Sie wie folgt vor, um eine Gruppe von Vorlagen mithilfe von PowerShell zu verwalten.

**So verwalten Sie eine Gruppe von Einstellungen-Speicherort Vorlagen mit PowerShell**

1.  Ändern oder aktualisieren Sie die Speicherort Vorlagen für die gewünschten Einstellungen.

2.  Stellen Sie die Speicherort Vorlagen für die gewünschten Einstellungen in einem Ordner bereit, auf den der lokale Computer zugreifen kann.

3.  Öffnen Sie auf dem lokalen Computer ein Windows PowerShell-Fenster mit Administratorrechten.

4.  Importieren Sie das Microsoft UE-V PowerShell-Modul, indem Sie den folgenden Befehl eingeben.

    ``` syntax
    Import-module UEV
    ```

5.  Heben Sie die Registrierung aller zuvor registrierten Versionen der Vorlagen auf, indem Sie den folgenden Befehl eingeben.

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    Dadurch werden alle aktiven Vorlagen auf dem Computer aufgehoben.

6.  Registrieren Sie die aktualisierten Vorlagen, indem Sie den folgenden Befehl eingeben.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Damit werden alle Einstellungen für den Speicherort registriert, die sich im angegebenen Vorlagenordner befinden.

Die Virtualisierung der Benutzeroberfläche bietet die folgenden WMI-Befehle. Administratoren können diese Schnittstellen zum Verwalten von Einstellungen für Standort Vorlagen aus Windows PowerShell und zum Automatisieren von administrativen Vorlagen Aufgaben verwenden.

**So verwalten Sie Einstellungen für Standort Vorlagen mit WMI**

1.  Verwenden Sie ein Konto mit Administratorrechten, um ein Windows PowerShell-Fenster zu öffnen.

2.  Verwenden Sie die folgenden WMI-Befehle zum Registrieren und Verwalten der Standort Vorlagen für UE-V-Einstellungen.

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
    <td align="left"><p>Get-WMIObject-Namespace root\Microsoft\UEV SettingsLocationTemplate | SELECT-Objekt-Vorlagen-Nr, Vorlagenname, TemplateVersion, aktiviert | Format – Tabelle – AutoSize</p></td>
    <td align="left"><p>Listet alle Einstellungen für den Speicherort auf, die für den Computer registriert sind.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Register-Argumentlisten- &lt; Vorlagenpfad&gt;</p></td>
    <td align="left"><p>Registriert eine Speicherort Vorlage für Einstellungen mit UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-argumentlist- &lt; Vorlagen-ID&gt;</p></td>
    <td align="left"><p>Hebt die Registrierung einer Einstellungs Speicherort Vorlage mit UE-V auf. Sobald eine Vorlage aufgehoben wurde, synchronisiert UE-V nicht mehr die Einstellungen, die in der Vorlage zwischen Computern definiert sind.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-argumentlist- &lt; Vorlagen-ID&gt;</p></td>
    <td align="left"><p>Aktiviert eine Vorlage für eine Einstellungsposition mit UE-V</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-argumentlist- &lt; Vorlagen-ID&gt;</p></td>
    <td align="left"><p>Deaktiviert eine Speicherort Vorlage für Einstellungen mit UE-V</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Update – argumentlist- &lt; Vorlagenpfad&gt;</p></td>
    <td align="left"><p>Aktualisiert eine Vorlage für Einstellungs Speicherort mit UE-V. Die neue Vorlage sollte eine höhere Version als die vorhandene aufweisen.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Validate-argumentlist- &lt; Vorlagenpfad&gt;</p></td>
    <td align="left"><p>Bestimmt, ob eine angegebene Speicherort Vorlage für Einstellungen dem XML-Schema entspricht.</p></td>
    </tr>
    </tbody>
    </table>

     

**Bereitstellen des UE-V-Agents mit PowerShell**

1.  Stufen Sie die UE-V-Installationsdatei in einer barrierefreien Netzwerkfreigabe ein.

    **Hinweis**  Verwenden Sie AgentSetup.exe, um sowohl 32-Bit-als auch 64-Bit-Versionen des UE-V-Agents bereitzustellen. Windows Installer-Dateien, AgentSetupx86.msi und AgentSetupx64.msi, stehen für jede Architektur zur Verfügung. Wenn Sie den UE-V-Agent zu einem späteren Zeitpunkt mit der Installationsdatei deinstallieren möchten, müssen Sie denselben Dateityp verwenden.

     

2.  Verwenden Sie einen der folgenden PowerShell-Befehle, um den Agenten zu installieren.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## Verwandte Themen


[Verwalten des UE-V 1.0-Agents und von Paketen mit PowerShell und WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[Verwalten von UE-V 1.0](administering-ue-v-10.md)

[Vorgänge für UE-V 1.0](operations-for-ue-v-10.md)

 

 





