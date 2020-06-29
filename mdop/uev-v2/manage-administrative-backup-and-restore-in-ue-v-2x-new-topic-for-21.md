---
title: Verwalten der administrativen Sicherung und Wiederherstellung in UE-V 2. x
description: Verwalten der administrativen Sicherung und Wiederherstellung in UE-V 2. x
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812325"
---
# Verwalten der administrativen Sicherung und Wiederherstellung in UE-V 2. x


Als Administrator von Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 oder 2,1 SP1 können Sie die Anwendungs-und Windows-Einstellungen in Ihrem ursprünglichen Zustand wiederherstellen. Und neu in UE-V 2,1 können Sie auch zusätzliche Einstellungen wiederherstellen, wenn ein Benutzer ein neues Gerät annimmt.

## Wiederherstellen von Einstellungen in UE-v 2,1 oder UE-v 2,1 SP1, wenn ein Benutzer ein neues Gerät annimmt


Wenn Sie die Einstellungen wiederherstellen möchten, wenn ein Benutzer ein neues Gerät annimmt, können Sie eine Vorlage für die Einstellungen-Position im **Backup** -oder Roam-Profil **(Standard)** mit dem PowerShell-Cmdlet "UevTemplateProfile" setzen. Auf diese Weise können Computereinstellungen zusätzlich zu den Benutzereinstellungen mit dem neuen Computer synchronisiert werden. Vorlagen, die dem Sicherungsprofil zugewiesen sind, werden für dieses Gerät gesichert und auf Gerätebasis konfiguriert. Verwenden Sie zum Sichern von Einstellungen für eine Vorlage das folgende Cmdlet in Windows PowerShell:

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   &lt;Vorlagen &gt; -ID ist die UE-V-Vorlagen-ID

-   &lt;Backup &gt; kann entweder ein Backup oder ein Roaming sein

Beim Ersetzen des Geräts eines Benutzers werden die Einstellungen von UE-V automatisch wiederhergestellt, wenn die Domäne, der Benutzername und der Gerätename des Benutzers übereinstimmen. Alle synchronisierten und alle Sicherungsdaten werden auf dem Gerät automatisch wiederhergestellt.

Sie können auch das neue PowerShell-Cmdlet Restore-UevBackup verwenden, um die Einstellungen von einem anderen Gerät wiederherzustellen. Wenn Sie die Einstellungs Pakete für das neue Gerät Klonen möchten, verwenden Sie das folgende Cmdlet in Windows PowerShell:

``` syntax
Restore-UevBackup –Machine <MachineName>
```

dabei &lt; &gt; ist MachineName der Computername des Geräts.

Vorlagen wie die Office 2013-Vorlage, die viele Anwendungen beinhalten, können entweder alle in das Roaming (Standard) oder ein gesichertes Profil aufgenommen werden. Einzelne apps in einer vorlagensuite Folgen der Gruppe. Office 2013 in-Box-Vorlagen beinhalten sowohl Roaming-als auch nur-Backup-Einstellungen. Backup-Only-Einstellungen können nicht in ein Roaming-Profil aufgenommen werden.

Im Rahmen des Sicherungs-und Wiederherstellungsfeatures hat UE-V die Optionen für das Rollback zu den Einstellungen als **Letztes bekanntes gut (LKG)** hinzugefügt. In dieser Version können Sie die ursprünglichen Einstellungen oder LKG-Einstellungen wiederherstellen. Mit den LKG-Einstellungen können Benutzer einen zwischen-und einen stabilen Punkt vor dem Zustand Pre-UE-V der Einstellungen wiederherstellen.

### So wird es gemacht: Sichern/Wiederherstellen von Vorlagen mit UE-V

Hierbei handelt es sich um die wichtigsten Sicherungs-und Wiederherstellungskomponenten von UE-V:

-   Vorlagen profile

-   Speicherort der Einstellungs Pakete in der Vorlage "Einstellungen-Speicherort"

-   Sicherungs Trigger

-   Wiederherstellen von Einstellungen

**Vorlagen profile**

Ein UE-V-Vorlagenprofil wird definiert, wenn die Vorlage auf dem Gerät registriert oder über das PowerShell/WMI-Konfigurationsdienstprogramm nach der Registrierung bereit steht. Zu den Profiltypen gehören:

-   Roaming (Standard)

-   Sicherung

-   Nach unten

Wenn Sie registriert sind, werden alle Vorlagen in das Roaming-Profil aufgenommen, sofern nicht anders angegeben. Mit diesen Vorlagen werden die Einstellungen für alle UE-V-aktivierten Geräte synchronisiert, wobei die entsprechende Vorlage aktiviert ist.

Vorlagen können mithilfe des Cmdlets "Satz-UevTemplateProfile" zum Sicherungsprofil mit PowerShell oder WMI hinzugefügt werden. Vorlagen im Sicherungsprofil sichern Sie diese Einstellungen auf den Speicherort für Einstellungen in einem speziellen Verzeichnis für Gerätenamen. Die angegebenen Einstellungen werden an diesem Speicherort gesichert.

Vorlagen, die für das betreffende Gerät zu einem bestimmten Zeitpunkt vorgesehen sind, sollten nur dann synchronisiert werden, wenn Sie explizit wiederhergestellt werden. Diese Einstellungen werden im gleichen gerätespezifischen Einstellungen-Paketspeicherort auf dem Speicherstandort "Einstellungen" als gesicherten-Einstellungen gespeichert. Für diese Vorlagen ist in der Vorlage ein spezieller Bezeichner eingebettet, der angibt, dass Sie Teil dieses Profils sein sollen.

**Speicherort der Einstellungs Pakete in der Vorlage "Einstellungen-Speicherort"**

Einstellungen für das Roaming-Profil werden am Speicherort der Einstellungen gespeichert. Vorlagen, die der Sicherung oder dem backuponly-Profil zugewiesen sind, speichern Ihre Einstellungen am Speicherort für Einstellungen in einem speziellen Verzeichnis für Gerätenamen. Jedes Gerät mit Vorlagen in diesen Profilen verfügt über einen eigenen Gerätenamen. UE-V bereinigt diese Verzeichnisse nicht.

**Sicherungs Trigger**

Die Sicherung wird von denselben Ereignissen ausgelöst, die eine UE-V-Synchronisierung auslösen.

**Wiederherstellen von Einstellungen**

Durch das Wiederherstellen des Geräts eines Benutzers werden die Einstellungen der aktuell registrierten Vorlage aus dem Sicherungsordner eines anderen Geräts und alle synchronisierten Einstellungen auf dem aktuellen Computer wiederhergestellt. Die Einstellungen werden auf diese zwei Arten wiederhergestellt:

-   **Automatische Wiederherstellung**

    Wenn die Einstellungen für den Speicherpfad, die Domäne und den Computer Namen des Benutzers mit dem aktuellen Benutzer übereinstimmen, werden alle Einstellungen für diesen Benutzer synchronisiert, wobei nur die neuesten Einstellungen angewendet werden. Wenn sich ein Benutzer zum ersten Mal bei einem neuen Gerät anmeldet und diese Kriterien erfüllt sind, werden die Einstellungsdaten auf dieses Gerät angewendet.

    **Hinweis:**  
    Die Einstellungen für Barrierefreiheit und Windows-Desktop erfordern, dass der Benutzer sich erneut bei Windows anmeldet, um angewendet zu werden.



-   **Manuelle Wiederherstellung**

    Wenn Sie Benutzer beim Wiederherstellen eines Geräts während einer Aktualisierung unterstützen möchten, können Sie das Cmdlet Restore-UevBackup verwenden. Dieser Befehl bewirkt, dass die Einstellungen des Benutzers vom Speicherort für Einstellungen heruntergeladen werden.

## Wiederherstellen von Anwendungs-und Windows-Einstellungen auf den ursprünglichen Zustand


Mit WMI-und Windows PowerShell-Befehlen können Sie die Anwendungs-und Windows-Einstellungen auf die Einstellungswerte zurücksetzen, die sich auf dem Computer befanden, als die Anwendung zum ersten Mal gestartet wurde, nachdem der UE-V-Agent installiert wurde. Diese Wiederherstellungsaktion wird für einzelne Anwendungs-oder Windows-Einstellungen ausgeführt. Die Einstellungen werden beim nächsten Ausführen der Anwendung wiederhergestellt, oder die Einstellungen werden wiederhergestellt, wenn sich der Benutzer beim Betriebssystem anmeldet.

**So stellen Sie Anwendungseinstellungen und Windows-Einstellungen mit Windows PowerShell für UE-V 2. x wieder her**

1.  Öffnen Sie das Windows PowerShell-Fenster.

2.  Geben Sie das folgende Windows PowerShell-Cmdlet ein, um die Anwendungseinstellungen und Windows-Einstellungen wiederherzustellen.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Windows PowerShell-Cmdlet</strong></th>
    <th align="left"><strong>Beschreibung</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p>Wiederherstellen der Benutzereinstellungen für eine Anwendung oder Wiederherstellen einer Gruppe von Windows-Einstellungen</p></td>
    </tr>
    </tbody>
    </table>



**So stellen Sie Anwendungseinstellungen und Windows-Einstellungen mit WMI wieder her**

1.  Öffnen Sie ein Windows PowerShell-Fenster.

2.  Geben Sie den folgenden WMI-Befehl ein, um Anwendungseinstellungen und Windows-Einstellungen wiederherzustellen.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>WMI-Befehl</strong></th>
    <th align="left"><strong>Beschreibung</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p>Wiederherstellen der Benutzereinstellungen für eine Anwendung oder Wiederherstellen einer Gruppe von Windows-Einstellungen</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## Verwandte Themen


[Verwalten von UE-V 2. x mit Windows PowerShell und WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









