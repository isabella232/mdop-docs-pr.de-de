---
title: Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x
description: Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810549"
---
# Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x


Das Microsoft User Experience Virtualization (UE-v) 2,0, 2,1 oder 2,1 SP1-Agent-Installationsprogramm, AgentSetup.exe, erstellt die folgenden geplanten Aufgaben während der Installation des UE-v-Agents:

-   **Überwachen von Anwendungseinstellungen**

-   **Synchronisierungs-Controller-Anwendung**

-   **Synchronisieren von Einstellungen beim Abmelden**

-   **Automatische Aktualisierung der Vorlage**

-   **Sammeln von CEIP-Daten**

-   **Hochladen von CEIP-Daten**

**Hinweis**  Mit Ausnahme von CEIP-Daten sammeln müssen diese Aufgaben aktiviert bleiben, da UE-V nicht ohne Sie funktionieren kann.

 

Diese geplanten Aufgaben können mit den UE-V-Tools nicht konfiguriert werden. Administratoren, die die geplante Aufgabe für diese Elemente ändern möchten, können ein Skript erstellen, das die Schtasks.exe Befehlszeilenoptionen verwendet.

Weitere Informationen zu Schtasks.exe finden Sie unter [so wird es gemacht: Verwenden von schtasks, exe zum Planen von Aufgaben in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).

Weitere Informationen zu

## Geplante Aufgaben in UE-V


Die folgenden geplanten Aufgaben sind in UE-V 2 mit Konfigurationsbefehlen für geplante Aufgaben enthalten.

### Sammeln von CEIP-Daten

Wenn sich der Benutzer oder Administrator bei der Installation für die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit (CEIP) entschieden hat, sammelt UE-V Daten, um das Produkt in zukünftigen Versionen zu verbessern. Dieser geplante Task wird nur bei der Anmeldung ausgeführt. Der Task " **CEIP-Daten sammeln** " führt die UevSqmSession.exe aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabenname</th>
<th align="left">Standardereignis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Collect-CEIP-Daten</p></td>
<td align="left"><p>Anmelde</p></td>
</tr>
</tbody>
</table>

 

### Überwachen von Anwendungseinstellungen

Mit der Aufgabe " **Monitor-Anwendungseinstellungen** " werden die Einstellungen für Windows-apps synchronisiert. Sie wird bei der Anmeldung ausgeführt, wird aber um 30 Sekunden verzögert, um die Anmeldung nicht schädlich zu beeinflussen. Die Aufgabe "Monitor Application Status" führt die UevAppMonitor.exe-Datei aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabenname</th>
<th align="left">Standardereignis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Monitor-Anwendungs Status</p></td>
<td align="left"><p>Anmelde</p></td>
</tr>
</tbody>
</table>

 

### Synchronisierungs-Controller-Anwendung

Der Synchronisierungs **Controller-Anwendungs** Task wird verwendet, um den Synchronisierungs Controller zu starten, um die Einstellungen vom Computer zum Speicherort der Einstellungen zu synchronisieren. Standardmäßig wird die Aufgabe alle 30 Minuten ausgeführt. Zu diesem Zeitpunkt werden lokale Einstellungen mit dem Speicherort der Einstellungen synchronisiert, und die aktualisierten Einstellungen für den Speicherort der Einstellungen werden mit dem Computer synchronisiert. Die Synchronisierungs Controller Anwendung führt die Microsoft.Uev.SyncController.exe aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.
**Hinweis:** Gemäß der Aufgabe " **Anwendungseinstellungen überwachen** " wird diese Aufgabe bei der Anmeldung ausgeführt, Sie wird jedoch um 30 Sekunden verzögert, um die Anmeldung nicht schädlich zu beeinflussen.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabenname</th>
<th align="left">Standardereignis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Sync-Controller Anwendung</p></td>
<td align="left"><p>Anmeldung und anschließend alle 30 Minuten</p></td>
</tr>
</tbody>
</table>

 

Mit dem folgenden Befehl wird beispielsweise der Agent so konfiguriert, dass die Einstellungen alle 15 Minuten anstelle des standardmäßigen 30-minütigen synchronisiert werden.

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### Synchronisieren von Einstellungen beim Abmelden

Mit der Aufgabe **Synchronisierungseinstellungen beim Abmelden** wird eine Anwendung bei der Anmeldung gestartet, die die Synchronisierung von Anwendungen bei der Abmeldung für UE-V steuert. Der Task "Einstellungen beim Abmelden synchronisieren" führt die Microsoft.Uev.SyncController.exe-Datei aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabenname</th>
<th align="left">Standardereignis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Synchronize-Einstellungen beim Abmelden</p></td>
<td align="left"><p>Anmelde</p></td>
</tr>
</tbody>
</table>

 

### Automatische Aktualisierung der Vorlage

Mit dem **automatischen Aktualisierungs** Vorgang der Vorlage wird der Einstellungs Vorlagenkatalog auf neue, aktualisierte oder entfernte Vorlagen überprüft. Diese Aufgabe wird nur ausgeführt, wenn die SettingsTemplateCatalog konfiguriert ist. Der Task " **Automatische Aktualisierung der Vorlage** " führt die ApplySettingsCatalog.exe-Datei aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabenname</th>
<th align="left">Standardereignis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Template Auto Update</p></td>
<td align="left"><p>System Start und um 3:30 Uhr täglich, zu einem beliebigen Zeitpunkt innerhalb eines 1-Stunden-Fensters</p></td>
</tr>
</tbody>
</table>

 

**Beispiel:** Mit dem folgenden Befehl wird der UE-V-Agent so konfiguriert, dass der Katalog Speicher für Einstellungs Vorlagen stündlich überprüft wird.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### Hochladen von CEIP-Daten

Der Task " **CEIP-Daten hochladen** " wird während der Installation ausgeführt, wenn der Benutzer oder der Administrator sich für die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit (CEIP) entschieden hat. Mit dieser Aufgabe werden die Daten auf die CEIP-Server hochgeladen, auf denen die Daten zur Verbesserung des Produkts für zukünftige Versionen von UE-V verwendet werden. Diese geplante Aufgabe wird bei der Anmeldung und anschließend alle 4 Stunden ausgeführt. Der Task " **CEIP-Daten hochladen** " führt die UevSqmUploader.exe-Datei aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabenname</th>
<th align="left">Standardereignis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Upload-CEIP-Daten</p></td>
<td align="left"><p>Bei der Anmeldung und alle 4 Stunden</p></td>
</tr>
</tbody>
</table>

 

## Informationen zu geplanten Aufgaben in UE-V 2


Das folgende Diagramm enthält zusätzliche Informationen zu geplanten Aufgaben für UE-V 2:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Vorgangsname </strong> (Dateiname)</p></td>
<td align="left"><p><strong>Standardhäufigkeit</strong></p></td>
<td align="left"><p><strong>Power-Umschaltfläche</strong></p></td>
<td align="left"><p><strong>Nur im Leerlauf</strong></p></td>
<td align="left"><p><strong>Netzwerkverbindung</strong></p></td>
<td align="left"><p><strong>Beschreibung</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Überwachen von Anwendungseinstellungen </strong> (UevAppMonitor.exe)</p></td>
<td align="left"><p>Startet 30 Sekunden nach der Anmeldung und wird bis zur Abmeldung fortgesetzt.</p></td>
<td align="left"><p>Nein.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>–</p></td>
<td align="left"><p>Synchronisiert Einstellungen für Windows-Apps (AppX).</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Synchronisierungs Controller Anwendung </strong> (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>Bei der Anmeldung und danach alle 30 Minuten.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nur, wenn das Netzwerk verbunden ist</p></td>
<td align="left"><p>Startet den Synchronisierungs Controller, der lokale Einstellungen mit dem Speicherort für Einstellungen synchronisiert.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Synchronisieren von Einstellungen beim Abmelden </strong> (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>Wird bei der Anmeldung ausgeführt und wartet auf Abmelden, um die Einstellungen zu synchronisieren.</p></td>
<td align="left"><p>Nein.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>–</p></td>
<td align="left"><p>Starten Sie bei der Anmeldung eine Anwendung, die die Synchronisierung von Anwendungen bei der Abmeldung steuert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Automatische Aktualisierung der Vorlage </strong> (ApplySettingsCatalog.exe)</p></td>
<td align="left"><p>Wird bei der Erstanmeldung und bei 3:30 am Tag danach ausgeführt.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>n.a.</p></td>
<td align="left"><p>Überprüft den Vorlagenkatalog der Einstellungen auf neue, aktualisierte oder entfernte Vorlagen. Diese Aufgabe wird nur ausgeführt, wenn SettingsTemplateCatalog konfiguriert ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Sammeln von CEIP </strong> -Daten (UevSqmSession.exe)</p></td>
<td align="left"><p>Bei der Anmeldung wird der Dienst gestartet.</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>n.a.</p></td>
<td align="left"><p>Wenn sich der Benutzer oder Administrator für das Programm zur Verbesserung der Benutzerfreundlichkeit einsetzt, sammelt diese Aufgabe Daten, die zur Verbesserung der zukünftigen Versionen von UE-V beitragen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Hochladen von CEIP </strong> -Daten (UevSqmUploader.exe)</p></td>
<td align="left"><p>Wird bei der Anmeldung und bei 4:00 am Tag danach ausgeführt.</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nur, wenn das Netzwerk verbunden ist</p></td>
<td align="left"><p>Wenn der Benutzer oder Administrator sich für das Programm zur Verbesserung der Benutzerfreundlichkeit einsetzt, werden die Daten von dieser Aufgabe auf die CEIP-Server hochgeladen.</p></td>
</tr>
</tbody>
</table>

 

**Legende**

-   **Power Toggle** – der Aufgabenplaner optimiert den Energieverbrauch, wenn er nicht mit dem Stromnetz verbunden ist. Die Aufgabe kann nicht mehr ausgeführt werden, wenn der Computer in den Batteriebetrieb wechselt.

-   **Nur im Leerlauf** – die Aufgabe wird nicht mehr ausgeführt, wenn der Computer nicht mehr im Leerlauf ist. Standardmäßig wird die Aufgabe nicht neu gestartet, wenn sich der Computer wieder im Leerlauf befindet. Stattdessen wird die Aufgabe beim nächsten Aufgaben Auslöser erneut gestartet.

-   **Netzwerkverbindung** – Aufgaben, die mit "Ja" gekennzeichnet sind, werden nur ausgeführt, wenn auf dem Computer eine Netzwerkverbindung verfügbar ist. Aufgaben, die mit "N/A" gekennzeichnet sind, werden unabhängig von der Netzwerkkonnektivität ausgeführt.

### Verwalten von geplanten Aufgaben

Führen Sie die folgenden Schritte aus, um geplante Aufgaben zu finden:

1.  Öffnen Sie "Aufgaben planen" auf dem Computer des Benutzers.

2.  Navigieren Sie zu: Aufgabenplanung- &gt; Taskplaner-Bibliothek- &gt; Microsoft- &gt; UE-V

3.  Wählen Sie im Detailbereich die geplante Aufgabe aus, die Sie verwalten und konfigurieren möchten.

### Weitere Informationen

Die folgenden zusätzlichen Informationen gelten für geplante UE-V-Aufgaben:

-   ll-Tasksequenz Programme befinden sich standardmäßig im Installationsordner des UE-V-Agents `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` .

-   Die geplante Aufgabe der Synchronisierungs Controller Anwendung ist die entscheidende Komponente, wenn die UE-v-SyncMethod auf "SyncProvider" (UE-v 2-Standardkonfiguration) festgelegt ist. Mit dieser geplanten Aufgabe bleibt der SettingsSToragePath mit den lokal zwischengespeicherten Versionen der Einstellungspaket Dateien synchronisiert. Wenn Benutzer sich beschweren, dass die Einstellungen nicht oft genug synchronisiert werden, können Sie die Einstellung für den geplanten Vorgang auf nur 1 Minute reduzieren.Sie können bei Bedarf auch den Standardwert von 30 Minuten auf einen höheren Betrag erhöhen. Wenn Benutzer sich beschweren, dass die Einstellungen bei der Anmeldung nicht schnell genug synchronisiert werden, können Sie die Verzögerungseinstellung für den geplanten Vorgang entfernen. (Sie können die Einstellung Verzögerung im Dialogfeld **Trigger bearbeiten** finden)

-   Sie müssen den geplanten Aufgabenplan automatisch aktualisieren nicht deaktivieren, wenn Sie eine andere Methode verwenden, um die Vorlagen der Clients synchron zu halten (also Gruppenrichtlinien-oder Configuration Manager-Basispläne). Wenn der Wert der SettingsTemplateCatalog-Eigenschaft leer bleibt, verhindert UE-V, dass der Einstellungs Katalog für benutzerdefinierte Vorlagen überprüft wird. Dieser geplante Task wird ApplySettingsCatalog.exe ausgeführt und wird im wesentlichen sofort zurückgegeben.

-   Der geplante Task "Anwendungseinstellungen überwachen" aktualisiert die Windows-App-Einstellungen (AppX) in Echtzeit basierend auf den Windows-app-Programm Einstellungs Triggern, die in jede APP integriert sind.






## Verwandte Themen


[Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





