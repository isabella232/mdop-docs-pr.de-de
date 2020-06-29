---
title: Übersicht über die Application Virtualization-Systemkomponenten
description: Übersicht über die Application Virtualization-Systemkomponenten
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806552"
---
# Übersicht über die Application Virtualization-Systemkomponenten


In der folgenden Tabelle werden die primären Komponenten des Microsoft Application Virtualization-Verwaltungssystems beschrieben. Weitere Informationen zum Bereitstellen dieser Systemkomponenten finden Sie unter [Server basiertes Application Virtualization-Szenario](application-virtualization-server-based-scenario.md).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Komponente</th>
<th align="left">Funktion</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization-Verwaltungs Server</p></td>
<td align="left"><p>Die Komponente, die für das Streaming des Paketinhalts und die Veröffentlichung der Verknüpfungen und Dateitypzuordnungen zum Application Virtualization Client verantwortlich ist.</p></td>
<td align="left"><p>Der Application Virtualization-Verwaltungs Server unterstützt das aktive Upgrade, die Lizenzverwaltung und eine Datenbank, die für die Berichterstellung verwendet werden kann.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Inhalts </strong> Ordner</p></td>
<td align="left"><p>Der Speicherort der Application Virtualization-Pakete für Streaming.</p></td>
<td align="left"><p>Dieser Ordner kann sich auf einer Freigabe auf dem Application Virtualization-Verwaltungs Server befinden. Der Ordner kann sich auch in einem SAN (Storage Area Network) befinden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization-Verwaltungskonsole</p></td>
<td align="left"><p>Ein MMC 3,0-Snap-in-Verwaltungsdienstprogramm für die Microsoft Application Virtualization Server-Verwaltung.</p></td>
<td align="left"><p>Diese Komponente kann auf dem Microsoft Application Virtualization Server oder auf einer separaten Workstation mit MMC 3.0 und installiert werden. NET 2.0 installiert ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization Management Web Service</p></td>
<td align="left"><p>Die Komponente, die für die Kommunikation von Lese-und Schreibanforderungen an den Application Virtualization-Datenspeicher verantwortlich ist.</p></td>
<td align="left"><p>Diese Komponente kann auf dem Microsoft Application Virtualization Server oder auf einem anderen Computer installiert sein, auf dem IIS installiert ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization-Datenspeicher</p></td>
<td align="left"><p>Die in der SQL-Datenbank gespeicherte Komponente, die für die Speicherung aller Informationen im Zusammenhang mit der Application Virtualization-Infrastruktur verantwortlich ist.</p></td>
<td align="left"><p>Diese Informationen umfassen alle Anwendungsdatensätze, Anwendungszuordnungen und welche Gruppen für die Verwaltung der Application Virtualization-Umgebung verantwortlich sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization Streaming Server</p></td>
<td align="left"><p>Die Komponente, die für das Hosten der Application Virtualization-Pakete für das Streaming an Clients in einer Zweigstelle verantwortlich ist, in der der Link zurück zum Application Virtualization Management-Server als WAN angesehen wird.</p></td>
<td align="left"><p>Dieser Server enthält nur Streamingfunktionen und stellt weder die Application Virtualization Management Console noch den Application Virtualization Management Web Service bereit.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization-Sequenzer</p></td>
<td align="left"><p>Die Komponente, die zum Überwachen und Aufzeichnen der Installation von Anwendungen zum Erstellen von virtuellen Anwendungspaketen verwendet wird.</p></td>
<td align="left"><p>Die Ausgabe besteht aus den Symbolen der Anwendung, einer OSD-Datei mit Paketdefinitionsinformationen, einer Paket Manifestdatei und der SFT-Datei mit den Inhaltsdateien des Anwendungsprogramms.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization-Client</p></td>
<td align="left"><p>Die Komponente, die auf dem Application Virtualization-Desktop Client oder auf dem Application Virtualization-Client für Remote Desktop Dienste (vormals Terminal Dienste) installiert ist und die virtuelle Umgebung für virtualisierte Anwendungen bereitstellt.</p></td>
<td align="left"><p>Der Microsoft Application Virtualization-Client verwaltet das Paketstreaming in den Zwischenspeicher, Veröffentlichungsaktualisierung, Transport und alle Interaktionen mit den Application Virtualization-Servern.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Application Virtualization Server-basiertes Szenario](application-virtualization-server-based-scenario.md)

[Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





