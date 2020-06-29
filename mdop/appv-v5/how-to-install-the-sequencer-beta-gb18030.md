---
title: So installieren Sie den Sequencer
description: So installieren Sie den Sequencer
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805363"
---
# So installieren Sie den Sequencer


Gehen Sie wie folgt vor, um den Microsoft Application Virtualization (App-V) 5,0-Sequenzer zu installieren. Auf dem Computer, auf dem der Sequencer ausgeführt wird, darf keine Version des App-V 5,0-Clients ausgeführt werden.

Das Upgrade einer vorherigen Installation des App-V-Sequencers wird nicht unterstützt.

**Wichtig**  Eine vollständige Liste der Sequencer-Anforderungen finden Sie unter Sequencer [-Abschnitte der APP-v 5,0-Voraussetzungen](app-v-50-prerequisites.md) und [unterstützten Konfigurationen für App-v 5,0](app-v-50-supported-configurations.md).

 

Sie können auch die Befehlszeile verwenden, um den App-V 5,0-Sequenzer zu installieren. In der folgenden Liste werden Informationen zu den Optionen für die Installation des Sequencers über die Befehlszeile und **appv\_sequencer\_setup.exe**angezeigt:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Befehl</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/INSTALLDIR</p></td>
<td align="left"><p>Gibt das Installationsverzeichnis an.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CEIPOPTIN</p></td>
<td align="left"><p>Ermöglicht die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit von Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Log</p></td>
<td align="left"><p>Gibt an, wo das Installationsprotokoll gespeichert werden soll, der Standardspeicherort ist <strong> % Temp% </strong> . Beispiel: " <strong> c" Logs \ Log. log </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>/q</p></td>
<td align="left"><p>Gibt eine ruhige oder unbeaufsichtigte Installation an.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Uninstall</p></td>
<td align="left"><p>Gibt das Entfernen des Sequencers an.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/ACCEPTEULA</p></td>
<td align="left"><p>Akzeptiert den Lizenzvertrag. Dies ist für eine unbeaufsichtigte Installation erforderlich. Beispiel Verwendung: <strong> /ACCEPTEULA </strong> oder <strong> /ACCEPTEULA = 1 </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LAYOUT</p></td>
<td align="left"><p>Gibt die zugeordnete Layout-Aktion an. Außerdem werden die Windows Installer-Dateien (MSI) und Skriptdateien in einen Ordner extrahiert, ohne App-V 5,0 zu installieren. Es wird kein Wert erwartet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LAYOUTDIR</p></td>
<td align="left"><p>Gibt das layoutverzeichnis an. Erfordert einen Zeichenfolgenwert. Beispielsyntax: <strong> /LAYOUTDIR = "C:\Application Virtualization Client" </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/? Oder/h oder/Help</p></td>
<td align="left"><p>Zeigt die zugehörige Hilfe an.</p></td>
</tr>
</tbody>
</table>

 

**So installieren Sie den App-V 5,0-Sequenzer**

1.  Kopieren Sie die Installationsdateien der App-V 5,0 Sequencer auf den Computer, auf dem Sie installiert werden soll. Doppelklicken Sie auf **appv\_sequencer\_setup.exe** , und klicken Sie dann auf **Installieren**.

2.  Auf der Seite **Software-Lizenzbestimmungen** sollten Sie die Lizenzbestimmungen überprüfen. Wenn Sie die Lizenzbestimmungen akzeptieren möchten, wählen Sie **Ich akzeptiere die Lizenzbestimmungen.** Klicken Sie auf **Weiter**.

3.  Verwenden Sie **Microsoft Update, um die sichere und aktuelle Seite Ihres Computers zu Gewähr** leisten, um Microsoft Updates zu aktivieren, wählen Sie **Microsoft Update verwenden aus, wenn ich auf Updates Suche (empfohlen).** Wenn Sie Microsoft Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus. Klicken Sie auf **Weiter**.

4.  Wählen Sie auf der Seite **Programm zur Verbesserung der Benutzerfreundlichkeit** an dem Programm teilnehmen an dem Programm zur **Verbesserung der Benutzerfreundlichkeit**teilnehmen aus. Auf diese Weise können Informationen darüber gesammelt werden, wie Sie App-V 5,0 verwenden. Wenn Sie nicht an dem Programm teilnehmen möchten, wählen Sie **Ich möchte zurzeit nicht an dem Programm**teilnehmen. Klicken Sie auf **Installieren**.

5.  Klicken Sie zum Öffnen des Sequencers auf **Start** , und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.

**So beheben Sie die Problembehandlung bei der Installation von App-V 5,0 Sequencer**

-   Wenn Sie weitere Informationen zur Sequencer-Installation wünschen, können Sie das Fehlerprotokoll im Ordner **% Temp%** anzeigen. Wenn Sie die Protokolldateien überprüfen möchten, klicken Sie auf **Start**, geben Sie **% Temp%** ein, und suchen Sie dann nach dem **appv\_-Protokoll**.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Planen der Bereitstellung von App-V](planning-to-deploy-app-v.md)

 

 





