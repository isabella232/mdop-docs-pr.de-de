---
title: Installieren der MBAM 2.5-Serversoftware
description: Installieren der MBAM 2.5-Serversoftware
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809928"
---
# Installieren der MBAM 2.5-Serversoftware


In diesem Thema wird beschrieben, wie Sie die Microsoft BitLocker-Verwaltungs-und Überwachungssoftware (MBAM) 2,5-Server Software mithilfe des Setup-Assistenten für die Microsoft BitLocker-Verwaltung und-Überwachung oder mithilfe von Befehlszeilenparametern installieren. Wiederholen Sie den Server Installationsvorgang für jeden Server, auf dem Sie die MBAM 2,5-Server Features konfigurieren. Nachdem Sie die Installation abgeschlossen haben, lesen Sie [Konfigurieren der MBAM 2,5-Server Features](configuring-the-mbam-25-server-features.md) , um Schritte zum Konfigurieren der Server Features zu erhalten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Vorbereitung</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Überprüfen der MBAM 2,5-Planungsinformationen</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Von MBAM 2.5 unterstützte Konfigurationen</a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">High-Level-Architektur für MBAM2.5</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Lesen Sie, wie Protokolldateien abgerufen werden.</p></td>
<td align="left"><p>Standardmäßig werden Protokolldateien im Ordner% Temp% des lokalen Computers erstellt. Wenn Sie die Protokolldateien an einen bestimmten Speicherort anstatt in den <strong> Ordner% Temp </strong> % schreiben möchten, verwenden Sie das <strong> /log- </strong> &lt; <em> Standort </em> &gt; Argument.</p>
<p>Zusätzliche Ereignisse werden möglicherweise in der Ereignisanzeige in den <strong> MBAM-Setup- </strong> oder <strong> MBAM-Web- </strong> Knoten unter <strong> Anwendungen und Dienste protokolliert &gt; Microsoft &gt; Windows protokolliert </strong> . Wenn Sie beispielsweise MBAM deinstallieren, wird das Deinstallationsprogramm auch die MBAM-und MBAM-Web-Protokolle in Event Viewer deinstallieren.</p></td>
</tr>
</tbody>
</table>

 

## Installieren der MBAM 2,5-Server Software mithilfe des Setup-Assistenten für die Microsoft BitLocker-Verwaltung und-Überwachung


Führen Sie die folgenden Schritte aus, um die MBAM-Server Software mithilfe des Setup-Assistenten für die Microsoft BitLocker-Verwaltung und-Überwachung zu installieren.

**So installieren Sie die MBAM 2,5-Server Software mithilfe des Assistenten**

1.  Führen Sie auf dem Server, auf dem Sie MBAM installieren möchten, **MBAMserversetup.exe** aus, um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung zu starten.

2.  Klicken Sie auf der Seite **Willkommen** auf **weiter**.

3.  Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

4.  Wählen Sie aus, ob Sie Microsoft Update verwenden möchten, wenn Sie nach Updates suchen, und klicken Sie dann auf **weiter**.

5.  Wählen Sie aus, ob Sie am Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen möchten, und klicken Sie dann auf **weiter**.

6.  Klicken Sie auf **Installieren**, um die Installation zu starten.

7.  Wenn Sie die Server Features nach Abschluss der Installation der MBAM-Server Software konfigurieren möchten, aktivieren Sie das Kontrollkästchen **MBAM-Serverkonfiguration ausführen, nachdem der Assistent geschlossen** wurde. Alternativ können Sie MBAM später mithilfe der **MBAM-Server Konfigurations** Verknüpfung konfigurieren, die von der Server Installation im **Startmenü** erstellt wird.

8.  Klicken Sie auf **Fertig stellen**.

## Installieren der MBAM 2,5-Server Software über ein Eingabeaufforderungsfenster


Geben Sie an der Eingabeaufforderung einen Befehl ähnlich dem folgenden Befehl ein, um die MBAM-Server Software zu installieren.

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

In der folgenden Tabelle werden die Befehlszeilenparameter für die Installation der MBAM 2,5-Server Software beschrieben.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parameter</th>
<th align="left">Parameter Wert</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CEIPENABLED</p></td>
<td align="left"><p>Wahr falsch</p></td>
<td align="left"><p>True – nehmen Sie am Programm zur Verbesserung der Benutzerfreundlichkeit Teil, das Microsoft dabei hilft, zu ermitteln, welche MBAM-Features verbessert werden können.</p>
<p>Falsch – nehmen Sie nicht am Programm zur Verbesserung der Benutzerfreundlichkeit teil.</p></td>
</tr>
<tr class="even">
<td align="left"><p>OPTIN_FOR_MICROSOFT_UPDATES</p></td>
<td align="left"><p>Wahr falsch</p></td>
<td align="left"><p>True – verwenden Sie Microsoft Update, um Ihren Computer für Windows und andere Microsoft-Produkte, einschließlich MBAM, zu schützen und auf dem neuesten Stand zu halten.</p>
<p>Falsch – Microsoft Update nicht verwenden</p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;Pfad&gt;</p></td>
<td align="left"><p>Der Speicherort, an dem Sie MBAM installieren möchten.</p>
<p>Beispiel:</p>
<p>INSTALLDIR = c:\mbaminstall</p></td>
</tr>
<tr class="even">
<td align="left"><p>FORCE_UNINSTALL</p></td>
<td align="left"><p>Wahr falsch</p></td>
<td align="left"><p>True: setzen Sie den Vorgang der Deinstallation von MBAM fort, auch wenn Features nicht entfernt werden können.</p>
<p>False (Standard), wenn die benutzerdefinierte Aktion "Deinstallation" ein hinzugefügtes MBAM-Server Feature nicht entfernen kann, die Deinstallation fehlschlägt und MBAM weiterhin installiert ist.</p>
<p>In beiden Fällen bleiben alle Features, die während des Versuchs zur Deinstallation von MBAM erfolgreich entfernt wurden, entfernt.</p></td>
</tr>
</tbody>
</table>

 



## Verwandte Themen


[Bereitstellen von MBAM 2.5](deploying-mbam-25.md)

[Konfigurieren der MBAM 2.5-Serverfunktionen](configuring-the-mbam-25-server-features.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





