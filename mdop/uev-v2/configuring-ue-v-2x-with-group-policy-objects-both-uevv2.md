---
title: Konfigurieren von UE-V 2. x mit Gruppenrichtlinienobjekten
description: Konfigurieren von UE-V 2. x mit Gruppenrichtlinienobjekten
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
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810546"
---
# Konfigurieren von UE-V 2. x mit Gruppenrichtlinienobjekten


Einige Gruppenrichtlinieneinstellungen für Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 können für Computer definiert werden, und andere Gruppenrichtlinieneinstellungen können für benutzerdefiniert werden. Informationen zum Installieren von ADMX-Dateien für UE-v-Gruppenrichtlinien finden Sie unter [Installieren der ADMX-Vorlagen für Gruppenrichtlinien für UE-v 2](https://technet.microsoft.com/library/dn458891.aspx#admx).

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
<th align="left">Name der Gruppenrichtlinieneinstellung</th>
<th align="left">Ziel</th>
<th align="left">Beschreibung der Gruppenrichtlinieneinstellung</th>
<th align="left">Konfigurationsoptionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Kontakt mit dem Link Text</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung gibt den Text des Links für die URL der Kontaktadresse im Unternehmenseinstellungen-Center an.</p></td>
<td align="left"><p>Wenn Sie diese Gruppenrichtlinieneinstellung aktivieren, wird im Unternehmens Einstellungs Center der angegebene Text im Link zur URL des Kontakts angezeigt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kontakt-URL</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung gibt die URL für den Link "Kontakt" im Unternehmenseinstellungen-Center an.</p></td>
<td align="left"><p>Wenn Sie diese Einstellung aktivieren, kontaktiert das Unternehmenseinstellungen-Center die Text-Links zur angegebenen URL. Der Link kann aus einem beliebigen Standardprotokoll wie http oder mailto sein.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwenden Sie nicht den Synchronisierungsanbieter.</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mithilfe dieser Gruppenrichtlinieneinstellung können Sie konfigurieren, ob UE-V das Feature "Synchronisierungsanbieter" verwendet. Mit dieser Richtlinieneinstellung können Sie auch die Benachrichtigung aktivieren, die angezeigt wird, wenn der Import von Benutzereinstellungen verzögert wird.</p></td>
<td align="left"><p>Aktivieren Sie diese Einstellung, um den UE-V-Agent so zu konfigurieren, dass der Synchronisierungsanbieter nicht verwendet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Benachrichtigung zur ersten Verwendung</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung aktiviert eine Benachrichtigung im Infobereich, die angezeigt wird, wenn die UE-V</p>
<p>der Agent wird zum ersten Mal ausgeführt.</p></td>
<td align="left"><p>Der Standardwert ist aktiviert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Roaming-Windows-Einstellungen</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung konfiguriert die Synchronisierung von Windows-Einstellungen.</p></td>
<td align="left"><p>Wählen Sie aus, welche Windows-Einstellungen zwischen Computern synchronisiert werden sollen.</p>
<p>Standardmäßig werden in Windows-Designs, Desktopeinstellungen und Einstellungen für den erleichterten Zugriff Einstellungen zwischen Computern der gleichen Betriebssystemversion synchronisiert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Warnungsschwellenwert für Einstellungen-Paketgröße</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Gruppenrichtlinieneinstellung können Sie den UE-V-Agent so konfigurieren, dass er meldet, wenn die Dateigröße eines Einstellungen-Pakets einen festgelegten Schwellenwert erreicht.</p></td>
<td align="left"><p>Geben Sie den bevorzugten Schwellenwert für die Größe des Einstellungs Pakets in Kilobyte (KB) an.</p>
<p>Standardmäßig hat der UE-V-Agent keinen Schwellenwert für die Paketdatei Größe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Speicherpfad für Einstellungen</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung konfiguriert, wo die Benutzereinstellungen gespeichert werden sollen.</p></td>
<td align="left"><p>Geben Sie einen UNC-Pfad (Universal Naming Convention) und Variablen wie \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Katalogpfad für Einstellungs Vorlagen</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung konfiguriert, wo die Speicherort Vorlagen für benutzerdefinierte Einstellungen gespeichert werden. Mit dieser Richtlinieneinstellung wird auch konfiguriert, ob der Katalog zum Ersetzen der Microsoft-Standardvorlagen verwendet werden soll, die mit dem UE-V-Agent installiert werden.</p></td>
<td align="left"><p>Geben Sie einen UNC-Pfad (Universal Naming Convention) wie \Server\TemplateShare oder einen Ordnerspeicherort auf dem Computer ein.</p>
<p>Aktivieren Sie das Kontrollkästchen, um die standardmäßigen Microsoft-Vorlagen zu ersetzen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronisierungseinstellungen über getaktete Verbindungen</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung legt fest, ob UE-V Einstellungen über getaktete Verbindungen synchronisiert.</p></td>
<td align="left"><p>Standardmäßig synchronisiert der UE-V-Agent die Einstellungen nicht über eine getaktete Verbindung.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Synchronisierungseinstellungen über getaktete Verbindungen auch beim Roaming</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung legt fest, ob UE-V Einstellungen über getaktete Verbindungen außerhalb des Home-Provider-Netzwerks synchronisiert, beispielsweise, wenn sich die Datenverbindung im roamingmodus befindet.</p></td>
<td align="left"><p>Standardmäßig synchronisiert UE-V die Einstellungen für eine getaktete Verbindung nicht, wenn sich der Roaming-Modus befindet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronisierungs Timeout</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Gruppenrichtlinieneinstellung wird die Anzahl der Millisekunden konfiguriert, die der Computer vor einem Timeout wartet, wenn er Benutzereinstellungen vom Speicherort der Remoteeinstellungen abruft. Wenn der Remotespeicher Standort nicht verfügbar ist und der Benutzer den Synchronisierungsanbieter nicht verwendet, wird der Anwendungsstart um diese Zahl von Millisekunden verzögert.</p></td>
<td align="left"><p>Geben Sie das bevorzugte Synchronisierungs Timeout in Millisekunden an. Der Standardwert ist 2000 Millisekunden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Taskleistensymbol</p></td>
<td align="left"><p>Nur Computer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung aktiviert das Taskleistensymbol für die Benutzeroberflächen-Virtualisierung (UE-V).</p></td>
<td align="left"><p>Der Standardwert ist aktiviert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwenden der Benutzeroberflächen-Virtualisierung (UE-V)</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Gruppenrichtlinieneinstellung können Sie die Virtualisierung der Benutzeroberfläche (UE-V) aktivieren oder deaktivieren.</p></td>
<td align="left"><p>Aktivieren oder deaktivieren Sie diese Gruppenrichtlinieneinstellung.</p></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Darüber hinaus stehen Gruppenrichtlinieneinstellungen für viele Desktopanwendungen und Windows-Apps zur Verfügung. Sie können diese Einstellungen verwenden, um die Synchronisierung von Einstellungen für bestimmte Anwendungen zu aktivieren oder zu deaktivieren.

 

**Gruppenrichtlinieneinstellungen für Windows-apps**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name der Gruppenrichtlinieneinstellung</th>
<th align="left">Ziel</th>
<th align="left">Beschreibung der Gruppenrichtlinieneinstellung</th>
<th align="left">Konfigurationsoptionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows-apps nicht synchronisieren</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung legt fest, ob der UE-V-Agent die Einstellungen für Windows-apps synchronisiert.</p></td>
<td align="left"><p>Standardmäßig werden Windows-apps synchronisiert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows-App-Liste</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Mit dieser Einstellung werden die Familienpaket Namen der Windows-apps aufgelistet, und es wird ausdrücklich angegeben, ob UE-V die Einstellungen dieser APP synchronisiert.</p></td>
<td align="left"><p>Mit dieser Einstellung können Sie festlegen, dass die Einstellungen einer APP nie von UE-V synchronisiert werden, selbst wenn die Einstellungen aller anderen Windows-apps synchronisiert sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronisieren nicht aufgelisteter Windows-apps</p></td>
<td align="left"><p>Computer und Benutzer</p></td>
<td align="left"><p>Diese Gruppenrichtlinieneinstellung definiert das Standardeinstellungen-Synchronisierungsverhalten des UE-V-Agents für Windows-apps, die nicht explizit in der Windows-App-Liste aufgeführt sind.</p></td>
<td align="left"><p>Standardmäßig synchronisiert der UE-V-Agent nur die Einstellungen dieser Windows-apps, die in der Windows-App-Liste enthalten sind.</p></td>
</tr>
</tbody>
</table>

 

Weitere Informationen zum Synchronisieren von Windows-apps finden Sie unter [Windows-App-Liste](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

**So konfigurieren Sie computerbezogene Gruppenrichtlinieneinstellungen**

1.  Verwenden Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) auf dem Computer, der als Domänencontroller fungiert, um Gruppenrichtlinieneinstellungen für UE-V-Computer zu verwalten. Navigieren Sie zu **Computer Konfiguration**, wählen Sie **Richtlinien**aus, wählen Sie **Administrative Vorlagen**aus, klicken Sie auf **Windows-Komponenten**, und wählen Sie dann **Microsoft User Experience Virtualization**aus.

2.  Wählen Sie die zu bearbeitende Gruppenrichtlinieneinstellung aus.

**So konfigurieren Sie benutzerbezogene Gruppenrichtlinieneinstellungen**

1.  Verwenden Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder das erweiterte Tool für die Gruppenrichtlinienverwaltung (AGPM) im Microsoft Desktop Optimization Pack (MDOP) auf dem Domänencontrollercomputer, um die Gruppenrichtlinieneinstellungen für UE-V zu verwalten. Navigieren Sie zu **Benutzerkonfiguration**, wählen Sie **Richtlinien**aus, wählen Sie **Administrative Vorlagen**aus, klicken Sie auf **Windows-Komponenten**, und wählen Sie dann **Microsoft User Experience Virtualization**aus.

2.  Wählen Sie die bearbeitete Gruppenrichtlinieneinstellung aus.

Der UE-V-Agent verwendet die folgende Rangfolge, um die Synchronisierung zu ermitteln.

**Rangfolge der UE-V-Einstellungen**

1.  Benutzerbezogene Einstellungen, die von Gruppenrichtlinieneinstellungen verwaltet werden – diese Konfigurationseinstellungen werden im Registrierungsschlüssel nach Gruppenrichtlinie unter gespeichert `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Computer gesteuerte Einstellungen, die von Gruppenrichtlinieneinstellungen verwaltet werden – diese Konfigurationseinstellungen werden im Registrierungsschlüssel nach Gruppenrichtlinie unter gespeichert `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Konfigurationseinstellungen, die vom aktuellen Benutzer mithilfe von Windows PowerShell oder Windows-Verwaltungsinstrumentation (WMI) definiert werden – diese Konfigurationseinstellungen werden vom UE-V-Agent unter diesem Registrierungsspeicherort gespeichert: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Konfigurationseinstellungen, die für den Computer mithilfe von Windows PowerShell oder WMI definiert sind. Diese Konfigurationseinstellungen werden vom UE-V-Agent unter diesem Registrierungsspeicherort `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` gespeichert:

    Sie **haben einen Vorschlag für UE-V**? [Hier](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Haben Sie ein UE-V-Problem**? Verwenden Sie das [UE-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Verwandte Themen


[Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Verwalten von Konfigurationen für UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





