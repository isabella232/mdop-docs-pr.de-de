---
title: Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche
description: Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811587"
---
# Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche


Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 speichert die Konfigurationseinstellungen in der Registrierung. Die Informationen, die wir hier zur Registrierung einfügen, können Ihnen helfen, ihre MED-V-Dienste besser zu verwalten.

MED-V verwendet den folgenden Suchpfad, wenn Sie nach den resultierenden Einstellungswerten suchen:

MED-V sucht zunächst in der Computerrichtlinie.

Wenn der Wert nicht gefunden wird, sucht MED-V in der Benutzerrichtlinie.

Wenn der Wert nicht gefunden wird, sucht MED-V in der HKEY \ _LOCAL \ _MACHINE \\system-Struktur.

Wenn der Wert nicht gefunden wird, sucht MED-V in der HKEY \ _CURRENT Benutzer Registrierungsstruktur.

Wenn der Wert immer noch nicht gefunden wird, verwendet MED-V den Standardwert.

Eine allgemeine bewährte Vorgehensweise besteht darin, den Wert im HKEY \ _LOCAL \ _MACHINE \\system-Hive oder in der Computerrichtlinie zu definieren. Wenn der Endbenutzer jedoch in der Lage sein soll, eine bestimmte Einstellung zu konfigurieren, sollten Sie ihn verlassen.

**Hinweis:**  
Bevor Sie Ihre Med-v-Arbeitsbereiche bereitstellen, können Sie ein Skript-Editor verwenden, um das Windows PowerShell-Skript (PS1-Datei) zu ändern, das vom Med-v-Arbeitsbereichs Paket erstellt wurde. Weitere Informationen finden Sie unter [Konfigurieren von erweiterten Einstellungen mithilfe von Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

Nachdem Sie Ihre Med-v-Arbeitsbereiche bereitgestellt haben, können Sie bestimmte Med-v-Konfigurationseinstellungen ändern, indem Sie die Registrierungseinträge bearbeiten.



In diesem Abschnitt werden alle konfigurierbaren MED-V-Registrierungsschlüssel aufgelistet und deren Verwendung erläutert.

## Diagnoseschlüssel


Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\diagnostics-Schlüssel verknüpft sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name </th>
<th align="left">Typ </th>
<th align="left">Daten/Standard </th>
<th align="left">Beschreibung </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EventLogLevel </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Standard = 3</p></td>
<td align="left"><p>Der Typ der Informationen, die im Ereignisprotokoll protokolliert werden. Zu den Ebenen gehören die folgenden: 0 (keine), 1 (Fehler), 2 (Warnung), 3 (Informationen), 4 (Debug).</p></td>
</tr>
</tbody>
</table>



## FTS-Taste


Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\fts-Schlüssel verknüpft sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Typ</th>
<th align="left">Daten/Standard</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddUserToAdminGroupEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>Konfiguriert, ob der Endbenutzer von der erstmaligen Einrichtung automatisch zur Gruppe Administrator&#39;s hinzugefügt wird. 0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: bei der erstmaligen Einrichtung wird der Endbenutzer nicht automatisch zur Gruppe Administrator&#39;s hinzugefügt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: bei der erstmaligen Einrichtung wird der Endbenutzer automatisch zur Gruppe Administrator&#39;s hinzugefügt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ComputerNameMask </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>MEDV </p></td>
<td align="left"><p>Die Computernamen Maske, die zum Erstellen des virtuellen Gastcomputers verwendet wird&#39;s-Computername.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Die Maske kann einen% username%-Tag enthalten, um den Benutzernamen als Teil des Computernamens einzufügen. Ebenso fügt das Tag% Hostname% den Namen des Hostcomputers ein.</p>
<p>Jedes &quot; # &quot; Zeichen in der Maske wird durch eine Zufallszahl ersetzt. Ein Sternchen (*)-Zeichen am Ende der Maske wird durch zufällige alphanumerische Zeichen ersetzt.</p>
<p>Eine bestimmte Anzahl von Zeichen aus% Hostname% und% username% kann mithilfe von eckigen Klammern erfasst werden. Beispielsweise &quot; würden% username% [3] &quot; die ersten drei Zeichen des Nutzernamens verwenden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeleteVMStateTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 90</p></td>
<td align="left"><p>Der Timeoutwert in Sekunden, wenn die erstmalige Einrichtung versucht, den virtuellen Computer zu löschen. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DetachVfdTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 120</p></td>
<td align="left"><p>Der Timeoutwert in Sekunden, wenn die erstmalige Einrichtung versucht, die virtuelle Diskette vom virtuellen Computer zu trennen. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogUrl </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Anpassbare URL, die mit der internen Webseite verknüpft ist und beim erstmaligen Einrichten von Dialog Meldungen angezeigt wird. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ExplorerTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 900</p></td>
<td align="left"><p>Der Timeoutwert in Sekunden, bei dem das erstmalige Setup auf den Windows-Explorer wartet. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FailureDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Nachricht wird in der Ressourcendatei gefunden </p></td>
<td align="left"><p>Anpassbare Nachricht, die dem Endbenutzer angezeigt wird, wenn die erstmalige Einrichtung nicht abgeschlossen werden kann.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GiveUserGroupRightsMaxRetryCount </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Standard = 3</p></td>
<td align="left"><p>Die maximale Anzahl von MED-V, die versucht, einer Endbenutzergruppe Rechte zuzuweisen. Wenn der angegebene Retry-Wert überschritten wird, ohne dass die Benutzergruppenrechte erfolgreich vergeben werden können, führt dies wahrscheinlich zu einem Fehler bei der Vorbereitung einer virtuellen Maschine, der dann dem MaxRetryCount-Wert unterliegt. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GiveUserGroupRightsTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 300</p></td>
<td align="left"><p>Der Timeoutwert in Sekunden, wenn einem Benutzergruppenrechte erteilt werden. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFilePaths </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Eine Liste der Protokolldateipfade, die von MED-V bei der erstmaligen Einrichtung erfasst werden. </p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPostponeTime </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 120</p></td>
<td align="left"><p>Die maximale Anzahl von Stunden, die vom Endbenutzer zum erstmaligen Einrichten verschoben werden können. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxRetryCount </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 3</p></td>
<td align="left"><p>Die maximale Anzahl von MED-V, die versucht, einen virtuellen Computer vorzubereiten, wenn jeder Versuch mit einem anderen Fehler als einem Softwarefehler endet. Wenn die Vorbereitung der virtuellen Maschine fehlschlägt und die Anzahl der Neuversuche beim erstmaligen Setup überschritten wird, informiert MED-V den Endbenutzer über den Fehler und gibt keine Möglichkeit zum erneuten Versuch. Die Anzahl wird jedes Mal neu festgesetzt, wenn MED-V gestartet wird. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modus </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Standard = unbeaufsichtigt</p></td>
<td align="left"><p>Konfiguriert, wie das erstmalige Setup mit dem Benutzer interagiert. Mögliche Werte lauten wie folgt:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Teilgenommen.</strong> Der Endbenutzer muss während der erstmaligen Einrichtung Informationen eingeben.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie die Datei "Sysprep. inf" erstellt haben, damit für das Mini Setup eine Benutzereingabe erforderlich ist, müssen Sie den <strong> beaufsichtigten Modus auswählen, </strong> oder es können Probleme beim erstmaligen Einrichten auftreten.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Unbeaufsichtigt </strong> . Der virtuelle Computer wird dem Endbenutzer während der erstmaligen Einrichtung nicht angezeigt, aber der Endbenutzer wird vor dem erstmaligen Setup aufgefordert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Stumm </strong> . Der virtuelle Computer wird dem Endbenutzer während der erstmaligen Einrichtung überhaupt nicht angezeigt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NonInteractiveRetryTimeoutInc </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 15</p></td>
<td align="left"><p>Der Timeoutwert in Minuten, bei dem das erstmalige Einrichten im interaktiven Modus zum erstmaligen Einrichten abgeschlossen werden muss, wenn das Setup erneut versucht wird. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NonInteractiveTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 45</p></td>
<td align="left"><p>Der Timeoutwert in Minuten, bei dem das erstmalige Einrichten im interaktiven Modus für die erstmalige Einrichtung abgeschlossen sein muss. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PostponeUtcDateTimeLimit </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Das Datum und die Uhrzeit im UTC-DateTime-Format, in dem das erstmalige Einrichten verschoben werden kann. Geben Sie in das Format &quot; yyyy-mm-tt hh: mm ein, &quot; wobei die Stunden unter Verwendung des standardmäßigen 24-Stunden-Clock-Standards angegeben sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RetryDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Nachricht wird in der Ressourcendatei gefunden </p></td>
<td align="left"><p>Anpassbare Nachricht, die dem Endbenutzer angezeigt wird, wenn das erstmalige Setup erneut versuchen muss.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetComputerNameEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>Konfiguriert, ob der Eintrag Computername unter dem Abschnitt [UserData] der Datei "Sysprep. inf" im Gast entsprechend der angegebenen ComputerNameMask aktualisiert werden soll.   0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: der Computername-Eintrag in der Datei "Sysprep. inf" wird entsprechend der ComputerNameMask nicht aktualisiert.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: der Computername-Eintrag in der Datei "Sysprep. inf" wird entsprechend der ComputerNameMask aktualisiert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetJoinDomainEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>Konfiguriert, ob die JoinDomain-Einstellung unter dem Abschnitt [Identification] der Datei "Sysprep. inf" im Gast so aktualisiert werden soll, dass Sie den Einstellungen auf dem Host entspricht.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: die JoinDomain-Einstellung in der Datei "Sysprep. inf" wird nicht so aktualisiert, dass Sie den Einstellungen auf dem Host entspricht.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: die JoinDomain-Einstellung in der Datei "Sysprep. inf" wird so aktualisiert, dass Sie den Einstellungen auf dem Host entspricht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetMachineObjectOUEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>Konfiguriert, ob die MachineObjectOU-Einstellung unter dem Abschnitt [Identification] der Datei "Sysprep. inf" im Gast so aktualisiert wird, dass Sie dem Host entspricht.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: die MachineObjectOU-Einstellung in der Datei "Sysprep. inf" wird nicht so aktualisiert, dass Sie den Einstellungen auf dem Host entspricht.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: die MachineObjectOU-Einstellung in der Datei "Sysprep. inf" wird so aktualisiert, dass Sie den Einstellungen auf dem Host entspricht.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetRegionalSettingsEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>Konfiguriert, ob die Einstellungen unter dem Abschnitt [Regional Settings] der Datei "Sysprep. inf" im Gast entsprechend dem Host aktualisiert werden.  0 = falsch; 1 = wahr.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Standardmäßig wird die Einstellung für TimeZone im Gast immer mit der Zeitzone-Einstellung im Host synchronisiert.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: die Einstellungen im Abschnitt [Regional Settings] der Datei "Sysprep. inf" im Gast werden nicht aktualisiert, um dem Host zu entsprechen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: die Einstellungen unter dem Abschnitt [Regional Settings] der Datei "Sysprep. inf" im Gast werden entsprechend dem Host aktualisiert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetUserDataEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>Konfiguriert, ob die FullName-und die OrgName-Einstellungen im Abschnitt [UserData] der Datei "Sysprep. inf" des Gastes so aktualisiert werden, dass Sie den Einstellungen auf dem Host entsprechen.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: die FullName-und OrgName-Einstellungen in der Datei "Sysprep. inf" werden nicht so aktualisiert, dass Sie den Einstellungen auf dem Host entsprechen.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: die FullName-und OrgName-Einstellungen in der Datei "Sysprep. inf" werden aktualisiert, sodass Sie den Einstellungen auf dem Host entsprechen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Nachricht wird in der Ressourcendatei gefunden </p></td>
<td align="left"><p>Anpassbare Nachricht, die dem Endbenutzer angezeigt wird, wenn die erstmalige Einrichtung gestartet werden kann. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TaskCancelTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 30</p></td>
<td align="left"><p>Der Timeoutwert in Sekunden, der bei der erstmaligen Einrichtung auf eine Antwort vom virtuellen Computer für einen Abbruchvorgang wartet. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskVMTurnOffTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 60</p></td>
<td align="left"><p>Der Timeoutwert in Sekunden, der von der erstmaligen Einrichtung auf das Herunterfahren des virtuellen Computers wartet. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UpgradeTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 600</p></td>
<td align="left"><p>Die Zeitdauer in Sekunden, bevor ein Versuchtes Upgrade der MED-V-Gast-Agent-Software ein Timeout hat. Bereich = 0 bis 2147483647.</p></td>
</tr>
</tbody>
</table>



## UserExperience-Taste


Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\userexperience-Schlüssel und dem HKEY \ _CURRENT \ _User \\software\\microsoft\\medv\\v2\\userexperience-Schlüssel verknüpft sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Typ</th>
<th align="left">Daten/Standard</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AppPublishingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Konfiguriert, ob die Anwendungs Publikation vom Gast auf den Host aktiviert ist.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: deaktiviert die Anwendungsveröffentlichung vom Gast auf den Host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: ermöglicht die Anwendungsveröffentlichung vom Gast an den Host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AudioSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Konfiguriert, ob die Freigabe des Audio-e/a-Geräts zwischen dem Gast und dem Host aktiviert ist.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: deaktiviert die Freigabe des Audio-e/a-Geräts zwischen dem Gast und dem Host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: ermöglicht die Freigabe des Audio-I/O-Geräts zwischen dem Gast und dem Host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClipboardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Konfiguriert, ob die Freigabe der Zwischenablage zwischen dem Gast und dem Host aktiviert ist.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: deaktiviert die Freigabe der Zwischenablage zwischen dem Gast und dem Host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: ermöglicht die Freigabe der Zwischenablage zwischen dem Gast und dem Host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 300</p></td>
<td align="left"><p>Die Zeitdauer (in Sekunden) vor dem Timeout des ersten Start Dialogfelds für Setup. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HideVmTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 30</p></td>
<td align="left"><p>Der Timeoutwert in Minuten, in dem das Fenster des virtuellen Computers im Vollbildmodus während eines langen Anmeldeversuchs vom Endbenutzer ausgeblendet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogonStartEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Konfiguriert, ob der Gast gestartet werden soll, wenn sich der Endbenutzer beim Desktop anmeldet oder wenn die erste gastanwendung gestartet wird.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: der Gast wird gestartet, wenn die erste gastanwendung gestartet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: der Gast wird gestartet, wenn sich der Endbenutzer beim Desktop anmeldet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PrinterSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Konfiguriert, ob die Freigabe von Druckern zwischen dem Gast und dem Host aktiviert ist.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: deaktiviert die Freigabe von Druckern zwischen dem Gast und dem Host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: ermöglicht die Freigabe von Druckern zwischen dem Gast und dem Host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RebootAbsoluteDelayTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1440</p></td>
<td align="left"><p>Der Timeoutwert in Minuten, der bei der erstmaligen Einrichtung auf einen Neustart wartet. Bereich = 0 bis 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RedirectUrls </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Angegebene URL-Liste</p></td>
<td align="left"><p>Gibt eine Liste der URLs an, die vom Host an den Gast weitergeleitet werden sollen. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SmartCardLogonEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>Konfiguriert, ob Smartcards zur Authentifizierung von Benutzern für MED-V verwendet werden können. 0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: Smartcards können Endbenutzer nicht an MED-V authentifizieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: ermöglicht Smartcards die Authentifizierung von Endbenutzern für MED-V.</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Wenn SmartCardLogonEnabled und CredentialCacheEnabled beide aktiviert sind, überschreibt SmartCardLogonEnabled CredentialCacheEnabled.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>SmartCardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Konfiguriert, ob die Freigabe von Smartcards zwischen dem Gast und dem Host aktiviert ist.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: deaktiviert die Freigabe von Smartcards zwischen dem Gast und dem Host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: ermöglicht die Freigabe von Smartcards zwischen dem Gast und dem Host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>USBDeviceSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Konfiguriert, ob die Freigabe von USB-Geräten zwischen dem Gast und dem Host aktiviert ist.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: deaktiviert die Freigabe von USB-Geräten zwischen dem Gast und dem Host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: ermöglicht die Freigabe von USB-Geräten zwischen dem Gast und dem Host.</p></td>
</tr>
</tbody>
</table>



## VM-Taste


Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\vm-Schlüssel und dem HKEY \ _CURRENT \ _User \\software\\microsoft\\medv\\v2\\vm-Schlüssel verknüpft sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Typ</th>
<th align="left">Daten/Standard</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CloseAction </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Standard = Ruhezustand</p></td>
<td align="left"><p>Die Aktion, die der virtuelle Computer ausführt, nachdem die letzte ausgeführte Anwendung geschlossen wurde. Diese Einstellung wird ignoriert, wenn der LogonStartEnabled-Wert aktiviert ist. Mögliche Optionen sind wie folgt:</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Ruhezustand </strong> . Mit dieser Option werden alle physikalischen Ressourcen, die der virtuelle Computer verwendet, wie Speicher und CPU, freigegeben, und der Zustand aller ausgeführten Anwendungen und Vorgänge wird gespeichert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Herunterfahren </strong> . Mit dieser Option wird das Gastbetriebssystem sicher heruntergefahren und dann alle physikalischen Ressourcen freigegeben, die vom virtuellen Computer verwendet werden, beispielsweise Arbeitsspeicher und CPU.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Deaktivieren </strong> . Diese Option kann zu Datenverlusten führen, weil Sie mit dem Ausschalten des Netzschalters oder dem Ziehen des Netzkabel auf einem physikalischen Computer identisch ist. Verwenden Sie diese Option nur, wenn Sie eine der beiden anderen Optionen nicht verwenden können.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestMemFromHostMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>378, 512, 1024, 1536, 2048 </p></td>
<td align="left"><p>Eine Liste der Speicherwerte (MB) für den Gast. Dieser Wert wird verwendet, um zu ermitteln, wie viel RAM dem Gast zur Verfügung steht. In Kombination mit HostMemToGuestMem wird eine Nachschlagetabelle erstellt, um zu ermitteln, wie viel RAM auf dem virtuellen Gastcomputer zugewiesen werden soll. Mögliche Werte können von 128 bis 3712 sein.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GuestUpdateDuration </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 240</p></td>
<td align="left"><p>Die Anzahl der Minuten, die MED-V den Gast für die automatische Aktualisierung aufbewahren soll, beginnend mit der im GuestUpdateTime-Wert angegebenen Zeit. Bereich = 0 bis 1440. Wenn dieser Wert auf 0 (null) festgelegt wird, wird die Funktion zum Patchen von Gästen deaktiviert.</p>
<p>Weitere Informationen zu Guest-Patches für die automatische Aktualisierung finden Sie unter <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Verwalten von automatischen Updates für MED-V-Arbeitsbereiche </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestUpdateTime </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Standard = 00:00</p></td>
<td align="left"><p>Die Stunden und Minuten pro Tag, wenn MED-V den Gast für die automatische Aktualisierung reaktivieren soll, mithilfe des standardmäßigen 24-Stunden-Clock-Standards. Angeben der Uhrzeit im Format hh: mm  </p>
<p>Weitere Informationen zu Guest-Patches für die automatische Aktualisierung finden Sie unter <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Verwalten von automatischen Updates für MED-V-Arbeitsbereiche </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>HostMemToGuestMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>1024, 2048, 4096, 8192, 16384 </p></td>
<td align="left"><p>Eine Liste der Speicherwerte (MB) für den Gast, die durch den auf dem Host verfügbaren RAM bestimmt werden. In Kombination mit GuestMemFromHostMem wird eine Nachschlagetabelle erstellt, um zu ermitteln, wie viel RAM auf dem virtuellen Gastcomputer zugewiesen werden soll. Mögliche Werte können von 1024 bis 16384 sein.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HostMemToGuestMemCalcEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Konfiguriert, ob der für den Gast zugewiesene Speicher aus dem auf dem Host vorhandenen Speicher berechnet wird.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: der für den Gast zugewiesene Arbeitsspeicher wird nicht aus dem auf dem Host vorhandenen Speicher berechnet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: der für den Gast zugewiesene Speicher wird aus dem auf dem Host vorhandenen Speicher berechnet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Arbeitsspeicher </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 512</p></td>
<td align="left"><p>Der RAM (MB), der für den virtuellen Gastcomputer reserviert werden soll. Diese Einstellung wird ignoriert, wenn die HostMemToGuestMemEnabled-Einstellung aktiviert ist. Bereich = 128 bis 2048.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MultiUserEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>Konfiguriert, ob mehrere Benutzer denselben MED-V-Arbeitsbereich verwenden.  0 = falsch; 1 = wahr.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falsch: mehrere Benutzer verwenden nicht den gleichen MED-V-Arbeitsbereich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = wahr: mehrere Benutzer verwenden denselben MED-V-Arbeitsbereich.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NetworkingMode </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Standard = NAT</p></td>
<td align="left"><p>Die Art der für den Gast verwendeten Netzwerkverbindung. Mögliche Werte lauten wie folgt:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Überbrückt </strong> . MED-V hat eine eigene Netzwerkadresse, die normalerweise über DHCP abgerufen wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>NAT </strong> . MED-V verwendet die Netzwerkadressübersetzung (Network Address Translation, NAT), um die IP-Adresse des Host-&#39;für ausgehenden Datenverkehr freizugeben.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 600</p></td>
<td align="left"><p>Ein allgemeiner Timeoutwert in Sekunden, auf den MED-V wartet, bis eine Aufgabe abgeschlossen ist, beispielsweise ein Neustart und ein Herunterfahren. Bereich = 0 bis 2147483647.</p></td>
</tr>
</tbody>
</table>



## Einstellungen für Gast Registrierung


In diesem Abschnitt werden die konfigurierbaren MED-V Guest-Registrierungsschlüssel aufgelistet und deren Verwendung erläutert.

### v2

Die folgende Tabelle enthält Informationen zum Registrierungswert Guest, der dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\-Schlüssel zugeordnet ist.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name </th>
<th align="left">Typ </th>
<th align="left">Daten/Standard </th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EnableGPWorkarounds</p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Standard = 1 </p></td>
<td align="left"><p>Konfiguriert, wie MED-V die Tasten BufferPolicyReads und GroupPolicyMinTransferRate behandelt.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Standardmäßig legt MED-V diese Schlüssel wie folgt fest:</p>
<p>BufferPolicyReads = 1 und GroupPolicyMinTransferRate = 0.</p>
<p>Erstellen Sie den EnableGPWorkarounds-Schlüssel, falls erforderlich, und legen Sie den Schlüssel auf NULL, wenn Sie nicht möchten, dass MED-V die Standardeinstellungen von BufferPolicyReads und GroupPolicyMinTransferRate ändert.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Ihr MED-V-Arbeitsbereich im NAT-Modus ausgeführt wird, wirkt sich EnableGPWorkarounds auf die Registrierungsschlüssel BufferPolicyReads und GroupPolicyMinTransferRate aus. Wenn Ihr MED-V-Arbeitsbereich im Bridged-Modus ausgeführt wird, wirkt sich EnableGPWorkarounds nur auf den Registrierungsschlüssel BufferPolicyReads aus.</p>
</div>
<div>

</div>
<p>1 = wahr: med-V legt die Tasten BufferPolicyReads = 1 und GroupPolicyMinTransferRate = 0 (falls im NAT-Modus ausgeführt) oder nur BufferPolicyReads = 1 fest (wenn Sie im Bridge-Modus ausgeführt werden).</p>
<p>0 = falsch: med-V nimmt keine Änderungen an den Tasten BufferPolicyReads und GroupPolicyMinTransferRate vor.</p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[Verwalten von MED-V-Arbeitsbereich Anwendungen](manage-med-v-workspace-applications.md)

[Verwalten von MED-V-URL-Umleitungen](manage-med-v-url-redirection.md)

[Verwalten von MED-V-Arbeitsbereichseinstellungen](manage-med-v-workspace-settings.md)









