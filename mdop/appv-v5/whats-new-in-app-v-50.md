---
title: Neuigkeiten in App-V 5.0
description: Neuigkeiten in App-V 5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804814"
---
# Neuigkeiten in App-V 5.0


Dieser Abschnitt richtet sich an Benutzer, die bereits mit App-v vertraut sind und wissen möchten, was sich in App-v 5,0 geändert hat, wenn Sie noch nicht mit App-v vertraut sind, sollten Sie zunächst die [Planung für App-v 5,0](planning-for-app-v-50-rc.md)lesen.

## Änderungen der Standard Funktionalität


Die folgenden Abschnitte enthalten Informationen zu den Änderungen in den Standardfunktionen für App-V 5,0.

### Änderungen an unterstützten Betriebssystemen

Weitere Informationen finden Sie unter [unterstützte App-V 5,0-Konfigurationen](app-v-50-supported-configurations.md).

## Änderungen am Sequencer


Die folgenden Abschnitte enthalten Informationen zu den Änderungen im App-V 5,0-Sequenzer.

### Spezifische Änderung des Sequencers

In der folgenden Tabelle werden Informationen zu den Änderungen mit dem App-V 5,0-Sequenzer angezeigt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sequencer-Feature</th>
<th align="left">App-V 5,0-Sequenzer-Funktionalität</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Neustart-Verarbeitung</p></td>
<td align="left"><p>Wenn eine Anwendung nach einem Neustart auffordert, sollten Sie der Anwendung den Neustart des Computers mit dem Sequencer gestatten. Der Computer, auf dem der Sequencer ausgeführt wird, wird neu gestartet, und der Sequencer wird im Überwachungsmodus fortgesetzt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Angeben des virtuellen Anwendungsverzeichnisses</p></td>
<td align="left"><p>Das virtuelle Anwendungsverzeichnis ist ein obligatorischer Parameter. Die besten Ergebnisse erzielen Sie, wenn Sie dem Installationsverzeichnis des Anwendungs Installationsprogramms entsprechen. Dies führt zu einer optimierten Leistung und Anwendungskompatibilität.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Bearbeiten von Verknüpfungen/Freihandelsabkommen</p></td>
<td align="left"><p>Die Seite "Verknüpfungen/FTA" befindet sich auf der Seite " <strong> Erweiterte </strong> Bearbeitung" nach Abschluss des Sequenz-Assistenten.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registerkarte „Verlauf ändern“</p></td>
<td align="left"><p>Die Registerkarte Änderungsverlauf wurde für App-V 5,0 entfernt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registerkarte „OSD“</p></td>
<td align="left"><p>Die Registerkarte "OSD" wurde für App-V 5,0 entfernt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registerkarte „Virtuelle Dienste“</p></td>
<td align="left"><p>Die Registerkarte Virtuelle Dienste wurde für App-V 5,0 entfernt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registerkarte "Dateien/virtuelles Datei System"</p></td>
<td align="left"><p>Diese Registerkarten werden kombiniert, und Sie können Paketdateien ändern.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registerkarte „Bereitstellung“</p></td>
<td align="left"><p>Es gibt keine weiteren Optionen zum Konfigurieren der Server-URL in den Paketen. Sie sollten dies jetzt mithilfe der Bereitstellungskonfiguration oder des Verwaltungsservers konfigurieren.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paket Konverter-Tool</p></td>
<td align="left"><p>Sie können jetzt mithilfe von PowerShell Pakete konvertieren, die in früheren Versionen erstellt wurden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Add-on/Middleware</p></td>
<td align="left"><p>Sie können übergeordnete Pakete erweitern, wenn Sie eine Add-on-oder Middleware-Anwendung sequenzieren. Add-ons und Middleware-Pakete müssen über Verbindungsgruppen in App-V 5,0 verbunden sein.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ausgabe von Dateien</p></td>
<td align="left"><p>Die folgenden Dateien werden mit App-V 5,0, Windows Installer (MSI), AppV, Bereitstellungskonfiguration, Benutzerkonfiguration und dem Report.XML erstellt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Komprimierungs-/Sicherheitsbeschreibungen/MSI-Pakete</p></td>
<td align="left"><p>Die Komprimierung und das Erstellen einer Windows Installer-Datei (MSI) sind für alle Pakete automatisch, und Sie können Sicherheitsbeschreibungen nicht mehr außer Kraft setzen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Extras/Optionen</p></td>
<td align="left"><p>Das Diagnosefenster wurde entfernt sowie verschiedene andere Einstellungen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Installationslaufwerk</p></td>
<td align="left"><p>Wenn Sie eine Anwendung installieren, ist kein Installationslaufwerk mehr erforderlich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OOS-Streaming</p></td>
<td align="left"><p>Wenn keine Datenstromoptimierung durchgeführt wird, sind Pakete Datenstromfehler Haft, wenn Sie von Computern angefordert werden, auf denen der App-V 5,0-Client ausgeführt wird, bis Sie gestartet werden können.</p></td>
</tr>
<tr class="even">
<td align="left"><p>F: &lt; /p&gt;</td>
<td align="left"><p>App-V 5,0 verwendet das systemeigene Dateisystem und erfordert keine q: mehr</p></td>
</tr>
</tbody>
</table>

 

## Fehlererkennung bei der Sequenzierung


Der App-V 5,0-Sequenzer kann häufige Sequenzierungs Probleme während der Sequenzierung erkennen. Auf der Seite " **Installationsbericht** " am Ende des Sequenz-Assistenten werden in Abhängigkeit vom Schweregrad des Problems diagnostische Nachrichten angezeigt, die in **Fehler**, **Warnungen**und **Informationen** kategorisiert sind.

Wenn Sie ausführlichere Informationen zu einem Ereignis anzeigen möchten, doppelklicken Sie auf das Element, das Sie im Bericht überprüfen möchten. Die Sequenzierungs Probleme sowie Vorschläge zur Behebung der Probleme werden angezeigt. Wenn Sie mit dem Erstellen eines Pakets fertig sind, werden die Informationen aus dem Bericht zur Systemvorbereitung und dem Installationsbericht zusammengefasst. In der folgenden Liste werden die im Bericht verfügbaren Problemtypen angezeigt:

-   Ausgeschlossene Dateien.

-   Treiberinformationen.

-   Unterschiede bei com+-Systemen.

-   Nebeneinander (SxS)-Konflikte.

-   Shell-Erweiterungen.

-   Informationen zu nicht unterstützten Diensten.

-   DCOM.

## Verbindungsgruppen


Das App-v-Feature, das früher als " **Dynamic Suite Composition** " bezeichnet wird, wird nun in App-V 5,0 als **Verbindungsgruppen** bezeichnet. Weitere Informationen zum Verwenden von Verbindungsgruppen finden Sie unter [Verwalten von Verbindungsgruppen](managing-connection-groups.md).

## Lizenzierungs-und Dosierungs Funktionen


Die Anwendungs-und Lizenzierungs Funktionalität wurde in App-V 5,0 entfernt. Die tatsächlichen Lizenz Positionen in Ihrer Umgebung hängen von den spezifischen Softwaretitel Lizenzen und Nutzungsrechten ab, die durch die zugehörigen Lizenzbedingungen gewährt werden.

## Datei-und Anwendungs Cache


In App-V 5,0 steht kein Datei-oder Anwendungscache zur Verfügung.






## Verwandte Themen


[Informationen zu App-V 5.0](about-app-v-50.md)

 

 





