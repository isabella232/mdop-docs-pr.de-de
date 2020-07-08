---
title: Übersicht über Application Virtualization
description: Übersicht über Application Virtualization
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806556"
---
# Übersicht über Application Virtualization


Microsoft Application Virtualization (App-V) kann Anwendungen für Endbenutzercomputer verfügbar machen, ohne die Anwendungen direkt auf diesen Computern installieren zu müssen. Dies wird durch einen Prozess ermöglicht, der als *Sequenzierung der Anwendung*bezeichnet wird, wodurch jede Anwendung in ihrer eigenen, eigenständigen virtuellen Umgebung auf dem Clientcomputer ausgeführt werden kann. Die sequenzierten Anwendungen sind voneinander isoliert. Dadurch werden Anwendungskonflikte beseitigt, die Anwendungen können jedoch weiterhin mit dem Clientcomputer interagieren.

Der App-V-Client ist das Feature, mit dem Endbenutzer mit den Anwendungen interagieren können, nachdem Sie auf dem Computer veröffentlicht wurden. Der Client verwaltet die virtuelle Umgebung, in der die virtualisierten Anwendungen auf jedem Computer ausgeführt werden. Nachdem der Client auf einem Computer installiert wurde, müssen die Anwendungen dem Computer über einen als " *Publishing*" bezeichneten Prozess zur Verfügung gestellt werden, mit dem der Endbenutzer die virtuellen Anwendungen ausführen kann. Beim Veröffentlichungsprozess werden die Symbole und Verknüpfungen der virtuellen Anwendung auf den Computer kopiert – normalerweise auf dem Windows-Desktop oder im **Startmenü** – und auch die Zuordnungsinformationen für die Paketdefinition und die Dateitypen werden auf den Computer kopiert. Durch die Veröffentlichung wird der Inhalt des Anwendungspakets auch dem Computer des Endbenutzers zur Verfügung gestellt.

Der Inhalt des virtuellen Anwendungspakets kann auf einen oder mehrere Application Virtualization-Server kopiert werden, damit er bei Bedarf auf die Clients gestreamt und lokal zwischengespeichert werden kann. Dateiserver und Webserver können auch als Streamingserver verwendet werden, oder der Inhalt kann direkt auf den Computer des Endbenutzers kopiert werden – beispielsweise, wenn Sie ein elektronisches Softwareverteilungssystem wie Microsoft Endpoint Configuration Manager verwenden. Bei einer Multi-Server-Implementierung erfordert die Beibehaltung des Paketinhalts und die Aktualität auf allen Streaming-Servern eine umfassende Paketverwaltungslösung. Je nach Größe Ihrer Organisation müssen Sie möglicherweise viele virtuelle Anwendungen für Endbenutzer verfügbar machen, die sich auf der ganzen Welt befinden. Die Verwaltung der Pakete, um sicherzustellen, dass die entsprechenden Anwendungen allen Benutzern zur Verfügung stehen, wenn Sie Zugriff darauf benötigen, ist daher eine wichtige Anforderung.

## Features des Microsoft Application Virtualization-Systems


In der folgenden Tabelle werden die primären Features des Microsoft Application Virtualization-Verwaltungssystems beschrieben.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Feature</th>
<th align="left">Funktion</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization-Verwaltungs Server</p></td>
<td align="left"><p>Verantwortlich für das Streaming des Paketinhalts und die Veröffentlichung der Verknüpfungen und Dateitypzuordnungen zum Application Virtualization Client.</p></td>
<td align="left"><p>Der Application Virtualization-Verwaltungs Server unterstützt das aktive Upgrade, die Lizenzverwaltung und eine Datenbank, die für die Berichterstellung verwendet werden kann.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Inhalts </strong> Ordner</p></td>
<td align="left"><p>Gibt den Speicherort der Application Virtualization-Pakete für Streaming an.</p></td>
<td align="left"><p>Dieser Ordner kann sich auf einer Freigabe auf dem Application Virtualization-Verwaltungs Server befinden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization-Verwaltungskonsole</p></td>
<td align="left"><p>Diese Konsole ist ein MMC 3,0-Snap-in-Verwaltungstool, das für die Microsoft Application Virtualization Server-Verwaltung verwendet wird.</p></td>
<td align="left"><p>Dieses Tool kann auf dem Microsoft Application Virtualization Server oder auf einer separaten Workstation mit Microsoft Management Console (MMC) 3.0 und Microsoft installiert werden. NETFramework 2,0 installiert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization Management Web Service</p></td>
<td align="left"><p>Verantwortlich für die Übermittlung von Lese-und Schreibanforderungen an den Application Virtualization-Datenspeicher.</p></td>
<td align="left"><p>Der Verwaltungs-Web-Service kann auf dem Microsoft Application Virtualization Management Server oder auf einem separaten Computer installiert werden, auf dem Microsoft Internet Information Services (IIS) installiert ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization-Datenspeicher</p></td>
<td align="left"><p>Die App-V SQL Server-Datenbank, die für das Speichern aller Informationen im Zusammenhang mit der Application Virtualization-Infrastruktur verantwortlich ist.</p></td>
<td align="left"><p>Diese Informationen umfassen alle Anwendungsdatensätze, Anwendungszuordnungen und welche Gruppen für die Verwaltung der Application Virtualization-Umgebung verantwortlich sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization Streaming Server</p></td>
<td align="left"><p>Verantwortlich für das Hosten der Application Virtualization-Pakete für das Streaming an Clients in einer Zweigstelle, wobei der Link zurück zum Application Virtualization Management Server als WAN-Verbindung (Wide Area Networks) gilt.</p></td>
<td align="left"><p>Dieser Server enthält nur Streamingfunktionen und stellt weder die Application Virtualization Management Console noch den Application Virtualization Management Web Service bereit.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization-Sequenzer</p></td>
<td align="left"><p>Der Sequencer wird verwendet, um die Installation von Anwendungen zur Erstellung virtueller Anwendungspakete zu überwachen und zu erfassen.</p></td>
<td align="left"><p>Die Ausgabe besteht aus den Symbolen der Anwendung, einer OSD-Datei, die Paketdefinitionsinformationen enthält, einer Paket Manifestdatei und der SFT-Datei, die die Inhaltsdateien des Anwendungsprogramms enthält.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization-Client</p></td>
<td align="left"><p>Der Application Virtualization-Desktop Client und der Application Virtualization-Client für Remote Desktop Dienste bieten und verwalten die virtuelle Umgebung für virtualisierte Anwendungen.</p></td>
<td align="left"><p>Der Microsoft Application Virtualization-Client verwaltet das Paketstreaming in den Zwischenspeicher, Veröffentlichungsaktualisierung, Transport und alle Interaktionen mit den Application Virtualization-Servern.</p></td>
</tr>
</tbody>
</table>

 

 

 





