---
title: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1
description: Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1
author: dansimp
ms.assetid: 79a36c77-fa0c-4651-8028-4a79763a2fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0677dda93f2c2dc60ec627ae0c3f4bd8c199db6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811059"
---
# Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1


Drücken Sie STRG + F, um die Microsoft User Experience Virtualization (UE-V) 2,0-Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie UE-V installieren. Die Anmerkungen zu dieser Version enthalten Informationen, die erforderlich sind, um die Virtualisierung der Benutzeroberfläche erfolgreich zu installieren, und zusätzliche Informationen enthalten, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es Unterschiede zwischen diesen Versionshinweisen und anderen UE-V-Dokumentationen gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Abgeben von Feedback


Teilen Sie uns Ihre Meinung zu unserer Dokumentation zu MDOP mit, indem Sie uns Feedback und Kommentare geben. Senden Sie Ihr Feedback zur Dokumentation an [mdopdocs@Microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Bekannte Probleme in UE-V


Dieser Abschnitt enthält Anmerkungen zu dieser Version für die Virtualisierung der Benutzeroberfläche.

### Standort Vorlagen für die UE-V-Einstellungen für Skype führen zum Absturz von Skype

Wenn ein Benutzer eine gültige Einstellungen-Standort Vorlage für die Skype-Desktopanwendung erstellt, diese registriert und dann die Skype-Desktopanwendung startet, stürzt Skype ab. Eine Access-_VIOLATION wird im Ereignisprotokoll der Anwendung aufgezeichnet.

Problemumgehung: Entfernen Sie die Skype-Vorlage, oder heben Sie die Registrierung auf, damit Skype wieder funktioniert.

### Vorhandene Skripts für unbeaufsichtigte Installationen von UE-V können fehlschlagen

Zwei Änderungen am UE-v-Installationsprogramm können dazu führen, dass Silent-Installationsskripts, die bei früheren Versionen von UE-v funktioniert haben, bei der Installation von UE-v 2,1 einen Fehler verursachen. Die erste ist eine neue Anforderung, dass Benutzer die Lizenzbedingungen akzeptieren und die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit (User Experience Improvement Program, CEIP) zustimmen oder ablehnen müssen, selbst während einer unbeaufsichtigten Installation. Die Verwendung des/q-Parameters reicht nicht mehr aus, um die Akzeptanz der Lizenzbedingungen und der Vereinbarung zur Teilnahme am CEIP anzugeben.

Zweitens erzwingt das Installationsprogramm nach der Installation des UE-V-Agents nun einen Neustart des Computers. Dies kann dazu führen, dass ein Installationsskript fehlschlägt, wenn der Neustart nicht erwartet wird (beispielsweise wird zuerst der UE-V-Agent installiert und dann der Generator sofort installiert).

Problemumgehung: das UE-V-Installationsprogramm (MSI) verfügt über zwei neue Befehlszeilenparameter, die unbeaufsichtigte Installationen unterstützen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parameter</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>/ACCEPTLICENSETERMS = wahr</strong></p></td>
<td align="left"><p>Legen Sie diesen Parameter auf "true" fest <strong> </strong> , um UE-V lautlos zu installieren. Das Hinzufügen dieses Parameters impliziert, dass der Benutzer die UE-V-Lizenzbestimmungen akzeptiert, die hier (standardmäßig) gefunden werden:%ProgramFiles%\Microsoft-Benutzeroberflächen-Virtualization\Agent</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>/NORESTART</strong></p></td>
<td align="left"><p>Dieser Parameter verhindert den obligatorischen Neustart nach der Installation des UE-V-Agents. Ein Rückgabecode von 3010 gibt an, dass vor der Verwendung von UE-V ein Neustart erforderlich ist.</p></td>
</tr>
</tbody>
</table>

 

### Registrierungseinstellungen werden nicht zwischen App-V und systemeigenen Anwendungen auf demselben Computer synchronisiert.

Wenn ein Computer über eine Anwendung verfügt, die sowohl über Application Virtualization (App-V) als auch lokal mit einer Windows Installer-Datei (MSI) installiert ist, werden die registrierungsbasierten Einstellungen nicht zwischen den Technologien synchronisiert.

Problemumgehung: um dieses Problem zu beheben, führen Sie die Anwendung aus, indem Sie eine der beiden Technologien auswählen, aber nicht beide.

### Unvorhersehbare Ergebnisse mit installiertem Office 2010 und Office 2013

Wenn ein Benutzer sowohl Office 2010 als auch Office 2013 installiert hat, werden alle gängigen Einstellungen zwischen den beiden Office-Versionen von UE-V durchsucht. Dies kann dazu führen, dass die Größe des Office 2010-Pakets recht groß ist oder zu unvorhersehbaren Konflikten mit 2013 führt, insbesondere dann, wenn Office 365 verwendet wird.

Problemumgehung: Installieren Sie nur eine Version von Office, oder begrenzen Sie, welche Einstellungen von UE-V synchronisiert werden.

### Deinstallieren und erneutes Installieren der Windows 8-App kehrt Einstellungen in den Anfangszustand zurück

Bei Verwendung der UE-V-Synchronisierungseinstellungen für eine Windows 8-App werden die Einstellungen der APP wieder auf die Standardwerte zurückgesetzt, wenn der Benutzer die APP deinstalliert und die APP dann neu installiert.Dies geschieht, weil die Deinstallation die lokale (zwischengespeicherte) Kopie der App-Einstellungen entfernt, aber nicht das lokale UE-V-Einstellungspaket entfernt.Wenn die APP neu installiert und gestartet wird, sammeln UE-V die App-Einstellungen, die auf die APP-Standardeinstellungen zurückgesetzt wurden, und laden dann die Standardeinstellungen an den zentralen Speicherort hoch.Auf anderen Computern, auf denen die app ausgeführt wird, werden die Standardeinstellungen heruntergeladen.Dieses Verhalten ist mit dem Verhalten von Desktopanwendungen identisch.

Problemumgehung: keine.

### UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Microsoft Office.

Wir empfehlen, die 32-Bit-Version von Microsoft Office sowohl für 32-Bit-als auch für 64-Bit-Betriebssysteme zu installieren. Wenn Sie die von Ihnen benötigte Microsoft Office-Version auswählen möchten, klicken Sie hier. ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)). UE-V unterstützt Roamingeinstellungen zwischen identischen Architekturversionen von Office. Beispielsweise werden die Office-Einstellungen für 32-Bit zwischen allen 32-Bit-Office-Instanzen durchlaufen. UE-V unterstützt keine Roamingeinstellungen zwischen 32-Bit-und 64-Bit-Versionen von Office.

Problemumgehung: keine

### <a href="" id="msi-s-are-not-localized"></a>MSI-Versionen sind nicht lokalisiert

UE-v 2,0 umfasst ein lokalisiertes Setupprogramm für den UE-v-Agent und den UE-v-Generator. Diese MSI-Dateien sind weiterhin verfügbar, die Benutzeroberfläche wird jedoch minimiert, und die MSI-Datei wird nur in Englisch angezeigt. Obwohl die Datei in Englisch ist, werden alle unterstützten Sprachen während der Installation von dem Setup-Programm installiert.

Problemumgehung: keine

### Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht durchwandert

Die Favicons, die mit Internet Explorer 9-Favoriten verknüpft sind, werden nicht von der Benutzeroberflächen-Virtualisierung durchlaufen und nicht angezeigt, wenn die Favoriten auf einem neuen Computer erstmalig angezeigt werden.

Problemumgehung: Favicons werden mit den zugehörigen Favoriten angezeigt, sobald die Textmarke verwendet und im Internet Explorer 9-Browser zwischengespeichert wurde.

### Datei Einstellungs Pfade werden in der Registrierung gespeichert

In einigen Anwendungseinstellungen werden die Pfade Ihrer Konfigurations-und Einstellungsdateien als Werte in der Registrierung gespeichert. Die Dateien, die als Pfade in der Registrierung referenziert werden, müssen synchronisiert werden, wenn die Einstellungen zwischen Computern durchlaufen werden.

Problemumgehung: Verwenden Sie die Ordnerumleitung oder eine andere Technologie, um sicherzustellen, dass alle Dateien, auf die als Pfad für Datei Einstellungen verwiesen wird, vorhanden sind und auf allen Computern, auf denen die Einstellungen durchlaufen werden, an derselben Stelle abgelegt werden.

### Lange Einstellungen Speicherpfade können einen Fehler verursachen

Behalten Sie die Einstellungen für den Speicherpfad so kurz wie möglich. Lange Pfade können die Auflösung oder Synchronisierung verhindern. UE-V verwendet den Einstellungsspeicher Pfad als Teil des berechneten Pfads zum Speichern von Einstellungen. Dieser Pfad wird folgendermaßen berechnet: Einstellungsspeicher Pfad + "settingspackages" + Paket dir (Vorlagen-ID) + Paketname (Vorlagen-ID) +. pkgx. Wenn der berechnete Pfad 260 Zeichen überschreitet, schlägt der Paketspeicher fehl, und es wird die folgende Fehlermeldung im operationellen UE-V-Ereignisprotokoll generiert:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Zum Überprüfen der Betriebsprotokoll Ereignisse öffnen Sie die Ereignisanzeige, und navigieren Sie zu Anwendungen und Dienstprotokolle/Microsoft/User Experience Virtualization/Logging/Operational.

Problemumgehung: keine.

### Einige Betriebssystemeinstellungen wechseln nur zwischen Betriebssystemversionen

Die Betriebssystemeinstellungen für Sprachausgaben und Währungszeichen, die für das gebietsschemaspezifisch sind (also sprach-und Regionaleinstellungen), werden nur über die Betriebssystemversionen von Windows durchlaufen. Währungszeichen werden beispielsweise nicht zwischen Windows 7 und Windows 8 durchwandert.

Problemumgehung: keine

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a>UE-v 1-Agent generiert Fehler beim Ausführen von UE-v 2-Vorlagen

Wenn eine Standort Vorlage für die UE-v 2-Einstellungen an einen Computer verteilt wird, der mit einem UE-v 1-Agent installiert ist, können einige Einstellungen nicht zwischen Computern synchronisiert werden, und der Agent meldet Fehler im Ereignisprotokoll.

Problemumgehung: Wenn Sie von UE-v 1 zu UE-v 2 migrieren und wahrscheinlich Computer mit der vorherigen Version des Agents ausgeführt werden, erstellen Sie einen separaten UE-v 2,0-Katalog zur Unterstützung des UE-v 2,0-Agents und der Vorlagen.

## Hotfixes und Knowledge Base-Artikel für UE-V 2,1


Dieser Abschnitt enthält Hotfixes und KB-Artikel für UE-V 2,1.

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
<td align="left"><p>3018608</p></td>
<td align="left"><p>UE-v 2,1 – TemplateConsole.exe stürzt ab, wenn UE-v-WMI-Klassen fehlen</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3018608/EN-US" data-raw-source="[support.microsoft.com/kb/3018608/EN-US](https://support.microsoft.com/kb/3018608/EN-US)">support.microsoft.com/kb/3018608/EN-US</a></p></td>
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
<td align="left"><p>2769631</p></td>
<td align="left"><p>Reparieren einer beschädigten UE-V-Installation</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)">support.microsoft.com/kb/2769631/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850989</p></td>
<td align="left"><p>Das Migrieren von MAPI-Profilen mit Microsoft UE-V wird nicht unterstützt.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)">support.microsoft.com/kb/2850989/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769586</p></td>
<td align="left"><p>UE-V durchstreift leere Ordner und Registrierungsschlüssel</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)">support.microsoft.com/kb/2769586/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2782997</p></td>
<td align="left"><p>Aktivieren der Debug-Protokollierung in Microsoft User Experience Virtualization (UE-V)</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)">support.microsoft.com/kb/2782997/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769570</p></td>
<td align="left"><p>UE-V aktualisiert das Design nicht in RDS-oder VDI-Sitzungen.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)">support.microsoft.com/kb/2769570/EN-US</a></p></td>
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

 






 

 





