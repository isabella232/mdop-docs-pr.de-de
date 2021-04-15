---
title: Konfigurieren von UE-V 2.x mit Gruppenrichtlinienobjekten
description: Konfigurieren von UE-V 2.x mit Gruppenrichtlinienobjekten
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494060"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a>Konfigurieren von UE-V 2.x mit Gruppenrichtlinienobjekten


Einige Gruppenrichtlinieneinstellungen für Microsoft User Experience Virtualization (UE-V) 2.0, 2.1 und 2.1 SP1 können für Computer definiert werden, und andere Gruppenrichtlinieneinstellungen können für Benutzer definiert werden. Informationen zum Installieren von UE-V-Gruppenrichtlinien-ADMX-Dateien finden Sie unter [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).

Die folgenden Richtlinieneinstellungen können für UE-V konfiguriert werden.

**Gruppenrichtlinieneinstellungen**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Gruppenrichtlinieneinstellungsname</th>
<th align="left">Ziel</th>
<th align="left">Beschreibung der Gruppenrichtlinieneinstellung</th>
<th align="left">Konfigurationsoptionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Konfigurieren der Synchronisierungsmethode</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mithilfe dieser Gruppenrichtlinieneinstellung können Sie konfigurieren, ob die User Experience Virtualization (UE-V) das Synchronisierungsanbieterfeature verwendet. Mit dieser Richtlinieneinstellung können Sie auch aktivieren, dass eine Benachrichtigung angezeigt wird, wenn der Import von Benutzereinstellungen verzögert wird.</p></td>
<td align="left"><p>Aktivieren Sie diese Einstellung, um den UE-V-Agent so zu konfigurieren, dass er weder den Synchronisierungsanbieter noch das externe Synchronisierungsmodul verwendet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kontakt IT Link Text</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung gibt den Text des Hyperlinks für die Kontakt-IT-URL im Unternehmenseinstellungscenter an.</p></td>
<td align="left"><p>Wenn Sie diese Gruppenrichtlinieneinstellung aktivieren, zeigt das Unternehmenseinstellungscenter den angegebenen Text im Link zur KONTAKT-IT-URL an.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kontaktieren der IT-URL</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung gibt die URL für den Link Kontakt-IT im Unternehmenseinstellungscenter an.</p></td>
<td align="left"><p>Wenn Sie diese Einstellung aktivieren, wird im Unternehmenseinstellungscenter It-Text kontaktieren mit der angegebenen URL verknüpft. Der Link kann eines beliebigen Standardprotokolls sein, z. B. HTTP oder mailto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>First Use Notification</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung aktiviert eine Benachrichtigung im Benachrichtigungsbereich, die angezeigt wird, wenn UE-V</p>
<p>Agent wird zum ersten Mal ausgeführt.</p></td>
<td align="left"><p>Die Standardeinstellung ist aktiviert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pingen des Speicherorts der Einstellungen vor der Synchronisierung</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Richtlinieneinstellung ermöglicht der Konfiguration des UE-V-Synchronisierungsanbieters das Pingen des Speicherpfads für Einstellungen, bevor Versucht wird, Einstellungen zu synchronisieren, um die Verbindung zu überprüfen.</p></td>
<td align="left"><p>Aktivieren oder Deaktivieren dieser Gruppenrichtlinieneinstellung.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Warnungsschwellenwert für Die Größe des Einstellungspakets</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Gruppenrichtlinieneinstellung können Sie den UE-V-Agent so konfigurieren, dass er berichtet, wenn die Größe einer Einstellungspaketdatei einen definierten Schwellenwert erreicht.</p></td>
<td align="left"><p>Geben Sie den bevorzugten Schwellenwert für Einstellungspaketgrößen in Kilobyte (KB) an.</p>
<p>Standardmäßig verfügt der UE-V-Agent nicht über einen Schwellenwert für die Paketdateigröße.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Speicherpfad für Einstellungen</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung konfiguriert, wo die Benutzereinstellungen gespeichert werden sollen.</p></td>
<td align="left"><p>Geben Sie einen UNC-Pfad (Universal Naming Convention) und Variablen wie \Server\SettingsShare%username%ein.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pfad des Einstellungsvorlagenkatalogs</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Mit dieser Gruppenrichtlinieneinstellung wird konfiguriert, wo benutzerdefinierte Einstellungsspeicherortvorlagen gespeichert werden. Mit dieser Richtlinieneinstellung wird außerdem konfiguriert, ob der Katalog zum Ersetzen der standardmäßigen Microsoft-Vorlagen verwendet werden soll, die durch den UE-V-Agent installiert sind.</p></td>
<td align="left"><p>Geben Sie einen UNC-Pfad (Universal Naming Convention) ein, z. B. \Server\TemplateShare oder einen Ordnerspeicherort auf dem Computer.</p>
<p>Aktivieren Sie das Kontrollkästchen, um die Standardmäßigen Microsoft-Vorlagen zu ersetzen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronisieren von Einstellungen über gemessene Verbindungen</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung definiert, ob UE-V Einstellungen über gemessene Verbindungen synchronisiert.</p></td>
<td align="left"><p>Standardmäßig synchronisiert der UE-V-Agent die Einstellungen nicht über eine gemessene Verbindung.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Synchronisieren von Einstellungen über gemessene Verbindungen auch beim Roaming</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung definiert, ob UE-V Einstellungen über gemessene Verbindungen außerhalb des Heimanbieternetzwerks synchronisiert, z. B. wenn sich die Datenverbindung im Roamingmodus befindet.</p></td>
<td align="left"><p>Standardmäßig synchronisiert UE-V die Einstellungen nicht über eine gemessene Verbindung, wenn sie sich im Roamingmodus befindet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronisierungstimeout</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Gruppenrichtlinieneinstellung wird die Anzahl von Millisekunden konfiguriert, die der Computer vor einem Zeit-Out wartet, wenn Benutzereinstellungen vom Remoteeinstellungsspeicherort abgerufen werden. Wenn der Remotespeicherort nicht verfügbar ist und der Benutzer den Synchronisierungsanbieter nicht verwendet, verzögert sich der Anwendungsstart um so viele Millisekunden.</p></td>
<td align="left"><p>Geben Sie das bevorzugte Synchronisierungs-Time-Out in Millisekunden an. Der Standardwert ist 2000 Millisekunden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Synchronisieren von Windows-Einstellungen </p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung konfiguriert die Synchronisierung von Windows-Einstellungen.</p></td>
<td align="left"><p>Wählen Sie aus, welche Windows-Einstellungen zwischen Computern synchronisiert werden.</p>
<p>Standardmäßig synchronisieren Windows-Designs, Desktopeinstellungen und Einstellungen für die Benutzerfreundlichkeit Einstellungen zwischen Computern derselben Betriebssystemversion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tablettsymbol</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung aktiviert das UE-V-Traysymbol.</p></td>
<td align="left"><p>Die Standardeinstellung ist aktiviert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verwenden der Benutzeroberflächenvirtualisierung (UE-V)</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Gruppenrichtlinieneinstellung können Sie UE-V aktivieren oder deaktivieren.</p></td>
<td align="left"><p>Aktivieren oder Deaktivieren dieser Gruppenrichtlinieneinstellung.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VDI-Konfiguration</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Richtlinieneinstellung wird die Synchronisierung von UE-V-Rollbackinformationen für Computer konfiguriert, die in einer gepoolten VDI-Umgebung ausgeführt werden. Wenn diese Richtlinie aktiviert ist, wird der UE-V-Rollbackstatus in den Speicherort der Einstellungen bei der Anmeldung kopiert und bei der Anmeldung wiederhergestellt.</p></td>
<td align="left"><p>Aktivieren oder Deaktivieren dieser Gruppenrichtlinieneinstellung.</p></td>
</tr>
</tbody>
</table>

 

**Hinweis:**  
Darüber hinaus sind Gruppenrichtlinieneinstellungen für viele Desktopanwendungen und Windows-Apps verfügbar. Sie können diese Einstellungen verwenden, um die Einstellungssynchronisierung für bestimmte Anwendungen zu aktivieren oder zu deaktivieren.

 

**Windows App-Gruppenrichtlinieneinstellungen**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Gruppenrichtlinieneinstellungsname</th>
<th align="left">Ziel</th>
<th align="left">Beschreibung der Gruppenrichtlinieneinstellung</th>
<th align="left">Konfigurationsoptionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Keine Synchronisierung von Windows Apps</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung definiert, ob der UE-V-Agent Einstellungen für Windows-Apps synchronisiert.</p></td>
<td align="left"><p>Die Standardeinstellung ist die Synchronisierung von Windows-Apps.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows-App-Liste</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Einstellung listet die Familienpaketnamen der Windows-Apps auf und gibt ausdrücklich an, ob UE-V die Einstellungen dieser App synchronisiert.</p></td>
<td align="left"><p>Sie können diese Einstellung verwenden, um anzugeben, dass die Einstellungen einer App niemals von UE-V synchronisiert werden, auch wenn die Einstellungen aller anderen Windows-Apps synchronisiert werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronisieren nicht aufgelisteter Windows Apps</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung definiert das Synchronisierungsverhalten der Standardeinstellungen des UE-V-Agents für Windows-Apps, die nicht explizit in der Windows-App-Liste aufgeführt sind.</p></td>
<td align="left"><p>Standardmäßig synchronisiert der UE-V-Agent nur die Einstellungen der Windows-Apps, die in der Windows-App-Liste enthalten sind.</p></td>
</tr>
</tbody>
</table>

 

Weitere Informationen zum Synchronisieren von Windows-Apps finden Sie unter [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

**So konfigurieren Sie computerorientierte Gruppenrichtlinieneinstellungen**

1.  Verwenden Sie die Gruppenrichtlinienverwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Advanced Group Policy Management, AGPM) auf dem Computer, der als Domänencontroller fungiert, um Gruppenrichtlinieneinstellungen für UE-V-Computer zu verwalten. Navigieren Sie **zu Computerkonfiguration,** wählen **Sie Richtlinien**aus, wählen Sie Administrative **Vorlagen aus,** klicken Sie auf **Windows-Komponenten,** und wählen Sie dann Microsoft User Experience Virtualization **aus.**

2.  Wählen Sie die Zu bearbeitende Gruppenrichtlinieneinstellung aus.

**So konfigurieren Sie benutzerorientierte Gruppenrichtlinieneinstellungen**

1.  Verwenden Sie die Gruppenrichtlinienverwaltungskonsole (Group Policy Management Console, GPMC) oder das Tool für die erweiterte Gruppenrichtlinienverwaltung (Advanced Group Policy Management, AGPM) in Microsoft Desktop Optimization Pack (MDOP) auf dem Domänencontrollercomputer, um Gruppenrichtlinieneinstellungen für UE-V zu verwalten. Navigieren Sie **zu Benutzerkonfiguration,** wählen **Sie Richtlinien**aus, wählen Sie Administrative **Vorlagen aus,** klicken Sie auf Windows-Komponenten, und wählen Sie **dann Microsoft User Experience Virtualization aus.** ****

2.  Wählen Sie die bearbeitete Gruppenrichtlinieneinstellung aus.

Der UE-V-Agent verwendet die folgende Rangfolge, um die Synchronisierung zu bestimmen.

**Rangfolge für UE-V-Einstellungen**

1.  Benutzerorientierte Einstellungen, die von Gruppenrichtlinieneinstellungen verwaltet werden – Diese Konfigurationseinstellungen werden im Registrierungsschlüssel von der Gruppenrichtlinie unter `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` gespeichert.

2.  Computerorientierte Einstellungen, die von Gruppenrichtlinieneinstellungen verwaltet werden – Diese Konfigurationseinstellungen werden im Registrierungsschlüssel von der Gruppenrichtlinie unter `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` gespeichert.

3.  Konfigurationseinstellungen, die vom aktuellen Benutzer mithilfe von Windows PowerShell oder Windows Management Instrumentation (WMI) definiert werden – Diese Konfigurationseinstellungen werden vom UE-V-Agent unter diesem Registrierungsspeicherort gespeichert: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Konfigurationseinstellungen, die für den Computer mithilfe von Windows PowerShell oder WMI definiert werden. Diese Konfigurationseinstellungen werden vom UE-V-Agent unter diesem Registrierungsspeicherort gespeichert: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .

    **Haben Sie einen Vorschlag für UE-V ?** Fügen Sie hier Vorschläge hinzu, oder stimmen Sie [über diese ab.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization) **Haben Sie ein UE-V-Problem?** Verwenden Sie [das UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## <a name="related-topics"></a>Verwandte Themen


[Verwalten von UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

[Verwalten von Konfigurationen für UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
