---
title: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0
description: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811062"
---
# Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0


Drücken Sie STRG + F, um die Microsoft User Experience Virtualization (UE-V) 2,0-Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie UE-V installieren. Die Anmerkungen zu dieser Version enthalten Informationen, die erforderlich sind, um die Virtualisierung der Benutzeroberfläche erfolgreich zu installieren, und zusätzliche Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es Unterschiede zwischen diesen Versionshinweisen und anderen UE-V-Dokumentationen gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Abgeben von Feedback


Teilen Sie uns Ihre Meinung zu unserer Dokumentation zu MDOP mit, indem Sie uns Feedback und Kommentare geben. Senden Sie Ihr Feedback zur Dokumentation an [mdopdocs@Microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Bekannte Probleme in UE-V


Dieser Abschnitt enthält Anmerkungen zu dieser Version für die Virtualisierung der Benutzeroberfläche.

### Registrierungseinstellungen werden nicht zwischen App-V und systemeigenen Anwendungen auf demselben Computer synchronisiert.

Wenn ein Computer über eine Anwendung verfügt, die über Application Virtualization (App-V) und eine lokal mit einer Windows Installer-Datei (MSI) installiert ist, werden die registrierungsbasierten Einstellungen nicht zwischen den Technologien synchronisiert.

**Problemumgehung:** Um dieses Problem zu beheben, führen Sie die Anwendung aus, indem Sie eine der beiden Technologien auswählen, aber nicht beide.

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a>Einstellungen werden nicht synchronisiert, wenn die Netzwerkfreigabe außerhalb der Benutzerdomäne liegt

Wenn Windows® 8 die Synchronisierung der Betriebssystem Einstellungen versucht, schlägt die Synchronisierung mit der folgenden Fehlermeldung fehl: **Boost:: File System:: EXISTS:: Falscher Benutzername oder Kennwort**. Dieser Fehler kann darauf hindeuten, dass sich die Netzwerkfreigabe außerhalb der Domäne des Benutzers oder einer Domäne mit einer Vertrauensstellung zu dieser Domäne befindet. Wenn Sie nach Betriebsprotokoll Ereignissen suchen möchten, öffnen Sie die **Ereignisanzeige** , und navigieren Sie zu **Anwendungen und Dienstprotokolle**, die  /  **Microsoft**  /  **User Experience Virtualization**-  /  **Protokollierung**in  /  **Betrieb**sind. Netzwerkfreigaben, die für die Speicherorte der UE-V-Einstellungen verwendet werden, sollten sich in derselben Active Directory-Domäne wie der Benutzer oder einer vertrauenswürdigen Domäne der Domäne des Benutzers befinden.

**Problemumgehung:** Verwenden Sie Netzwerkfreigaben aus derselben Active Directory-Domäne wie der Benutzer.

### Unvorhersehbare Ergebnisse mit installiertem Office 2010 und Office 2013

Wenn ein Benutzer sowohl Office 2010 als auch Office 2013 installiert hat, werden alle gängigen Einstellungen zwischen den beiden Office-Versionen von UE-V durchsucht. Dies kann dazu führen, dass die Größe des Office 2010-Pakets recht groß ist oder zu unvorhersehbaren Konflikten mit 2013 führt, insbesondere dann, wenn Office 365 verwendet wird.

**Problemumgehung:** Installieren Sie nur eine Version von Office, oder begrenzen Sie, welche Einstellungen von UE-V synchronisiert werden.

### Deinstallieren und erneutes Installieren der Windows 8-App kehrt Einstellungen in den Anfangszustand zurück

Bei Verwendung der UE-V-Synchronisierungseinstellungen für eine Windows 8-App werden die Einstellungen der APP wieder auf die Standardwerte zurückgesetzt, wenn der Benutzer die APP deinstalliert und die APP dann neu installiert.Dies geschieht, weil die Deinstallation die lokale (zwischengespeicherte) Kopie der App-Einstellungen entfernt, aber nicht das lokale UE-V-Einstellungspaket entfernt.Wenn die APP neu installiert und gestartet wird, sammeln UE-V die App-Einstellungen, die auf die APP-Standardeinstellungen zurückgesetzt wurden, und laden dann die Standardeinstellungen an den zentralen Speicherort hoch.Auf anderen Computern, auf denen die app ausgeführt wird, werden die Standardeinstellungen heruntergeladen.Dieses Verhalten ist mit dem Verhalten von Desktopanwendungen identisch.

**Problemumgehung:** Keine.

### E-Mail-Signatur-Roaming für Outlook 2010

UE-V durchstreift die Outlook 2010-Signaturdateien zwischen Geräten. Die standardmäßigen Signaturoptionen für neue Nachrichten und Antworten oder Weiterleitungen werden jedoch nicht synchronisiert. Diese beiden Einstellungen werden im Outlook-Profil gespeichert, das UE-V nicht durchwandert.

**Problemumgehung:** Keine.

### UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Microsoft Office.

Wir empfehlen, dass Sie die 64-Bit-Version von Microsoft Office für moderne Computer installieren. Wenn Sie feststellen möchten, welche Version Sie benötigen, [Klicken Sie hier](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions). UE-V unterstützt Roamingeinstellungen zwischen identischen Architekturversionen von Office. Beispielsweise werden die Office-Einstellungen für 32-Bit zwischen allen 32-Bit-Office-Instanzen durchlaufen. UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Office.

**Problemumgehung:** Keine

### <a href="" id="msi-s-are-not-localized"></a>MSI-Versionen sind nicht lokalisiert

UE-v 2,0 umfasst ein lokalisiertes Setupprogramm für den UE-v-Agent und den UE-v-Generator. Diese MSI-Dateien sind weiterhin verfügbar, die Benutzeroberfläche wird jedoch minimiert, und die MSI-Datei wird nur in Englisch angezeigt. Obwohl die Datei in Englisch ist, werden alle unterstützten Sprachen während der Installation von dem Setup-Programm installiert.

**Problemumgehung:** Keine

### Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht durchwandert

Die Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht von der Benutzeroberflächen-Virtualisierung durchlaufen und nicht angezeigt, wenn die Favoriten auf einem neuen Computer erstmalig angezeigt werden.

**Problemumgehung:** Favicons werden mit den zugehörigen Favoriten angezeigt, sobald die Textmarke verwendet und im Internet Explorer 9-Browser zwischengespeichert wurde.

### Datei Einstellungs Pfade werden in der Registrierung gespeichert

In einigen Anwendungseinstellungen werden die Pfade Ihrer Konfigurations-und Einstellungsdateien als Werte in der Registrierung gespeichert. Die Dateien, die als Pfade in der Registrierung referenziert werden, müssen synchronisiert werden, wenn die Einstellungen zwischen Computern durchlaufen werden.

**Problemumgehung:** Verwenden Sie die Ordnerumleitung oder eine andere Technologie, um sicherzustellen, dass alle Dateien, auf die als Pfad für Datei Einstellungen verwiesen wird, vorhanden sind und sich auf allen Computern, auf denen die Einstellungen durchlaufen, an demselben Speicherort befinden.

### Lange Einstellungen Speicherpfade können einen Fehler verursachen

Behalten Sie die Einstellungen für den Speicherpfad so kurz wie möglich. Lange Pfade können die Auflösung oder Synchronisierung verhindern. UE-V verwendet den Einstellungsspeicher Pfad als Teil des berechneten Pfads zum Speichern von Einstellungen. Dieser Pfad wird folgendermaßen berechnet: Einstellungsspeicher Pfad + "settingspackages" + Paket dir (Vorlagen-ID) + Paketname (Vorlagen-ID) +. pkgx. Wenn der berechnete Pfad 260 Zeichen überschreitet, schlägt der Paketspeicher fehl, und es wird die folgende Fehlermeldung im operationellen UE-V-Ereignisprotokoll generiert:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Zum Überprüfen der Betriebsprotokoll Ereignisse öffnen Sie die Ereignisanzeige, und navigieren Sie zu Anwendungen und Dienstprotokolle/Microsoft/User Experience Virtualization/Logging/Operational.

**Problemumgehung:** Keine.

### Einige Betriebssystemeinstellungen wechseln nur zwischen Betriebssystemversionen

Die Betriebssystemeinstellungen für Sprachausgaben und Währungszeichen, die für das gebietsschemaspezifisch sind (also sprach-und Regionaleinstellungen), werden nur über die Betriebssystemversionen von Windows durchlaufen. Währungszeichen werden beispielsweise nicht zwischen Windows 7 und Windows 8 durchwandert.

**Problemumgehung:** Keine

### Bei Windows 8-Apps werden die Einstellungen nicht synchronisiert, wenn die APP neu gestartet wird, nachdem Sie unerwartet geschlossen wurde.

Wenn eine Windows 8-App kurz nach dem Start unerwartet geschlossen wird, werden die Einstellungen für die Anwendung möglicherweise nicht synchronisiert, wenn die Anwendung neu gestartet wird.

**Problemumgehung:** Schließen Sie die Windows 8-APP, schließen Sie die UevAppMonitor.exe-Anwendung, und starten Sie Sie neu (kann Task Manager verwenden), und starten Sie dann die Windows 8-APP neu.

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a>UE-v 1-Agent generiert Fehler beim Ausführen von UE-v 2-Vorlagen

Wenn eine Standort Vorlage für die UE-v 2-Einstellungen an einen Computer verteilt wird, der mit einem UE-v 1-Agent installiert ist, können einige Einstellungen nicht zwischen Computern synchronisiert werden, und der Agent meldet Fehler im Ereignisprotokoll.

**Problemumgehung:** Wenn Sie von UE-v 1 zu UE-v 2 migrieren und wahrscheinlich auf Computern die vorherige Version des Agents ausgeführt wird, erstellen Sie einen separaten UE-v 2,0-Katalog zur Unterstützung des UE-v 2,0-Agents und der Vorlagen.

## Hotfixes und Knowledge Base-Artikel für UE-V 2,0


Dieser Abschnitt enthält Hotfixes und KB-Artikel für UE-V 2,0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>KB-Artikel</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2927019</p></td>
<td align="left"><p>Hotfix-Paket 1 für Microsoft User Experience Virtualization 2,0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)">support.microsoft.com/kb/2927019</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2903501</p></td>
<td align="left"><p>UE-v: User Experience Virtualization (UE-v)-Kompatibilität mit Benutzerprofilen</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)">support.microsoft.com/kb/2903501/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2770042</p></td>
<td align="left"><p>UE-V-Registrierungseinstellungen</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)">support.microsoft.com/kb/2770042/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2847017</p></td>
<td align="left"><p>Von Internet Explorer replizierte UE-V-Einstellungen</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)">support.microsoft.com/kb/2847017/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2930271</p></td>
<td align="left"><p>Grundlegendes zu den Einschränkungen beim Roaming von Outlook-Signaturen in Microsoft UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)">support.microsoft.com/kb/2930271/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769631</p></td>
<td align="left"><p>Reparieren einer beschädigten UE-V-Installation</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)">support.microsoft.com/kb/2769631/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2850989</p></td>
<td align="left"><p>Das Migrieren von MAPI-Profilen mit Microsoft UE-V wird nicht unterstützt.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)">support.microsoft.com/kb/2850989/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769586</p></td>
<td align="left"><p>UE-V durchstreift leere Ordner und Registrierungsschlüssel</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)">support.microsoft.com/kb/2769586/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2782997</p></td>
<td align="left"><p>Aktivieren der Debug-Protokollierung in Microsoft User Experience Virtualization (UE-V)</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)">support.microsoft.com/kb/2782997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769570</p></td>
<td align="left"><p>UE-V aktualisiert das Design nicht in RDS-oder VDI-Sitzungen.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)">support.microsoft.com/kb/2769570/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2901856</p></td>
<td align="left"><p>Anwendungseinstellungen werden nicht synchronisiert, nachdem Sie einen Neustart auf einem UE-V-fähigen Computer erzwungen haben</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)">support.microsoft.com/kb/2901856/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850582</p></td>
<td align="left"><p>Verwenden der Microsoft-Benutzeroberflächen-Virtualisierung mit App-V-Anwendungen</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)">support.microsoft.com/kb/2850582/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3041879</p></td>
<td align="left"><p>Aktuelle Dateiversionen für Microsoft User Experience Virtualization</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)">support.microsoft.com/kb/3041879/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2843592</p></td>
<td align="left"><p>Informationen zur Benutzeroberflächen-Virtualisierung und zu einer höheren Verfügbarkeit</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)">support.microsoft.com/kb/2843592/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

 

 





