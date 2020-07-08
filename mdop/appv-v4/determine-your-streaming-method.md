---
title: Bestimmen der Streaming-Methode
description: Bestimmen der Streaming-Methode
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808893"
---
# Bestimmen der Streaming-Methode


Wenn ein Benutzer zum ersten Mal auf das Symbol doppelklickt, das über den Veröffentlichungsprozess auf einem Computer gespeichert wurde, erhält der Application Virtualization-Client den Inhalt des virtuellen Anwendungspakets von einem Streaming Source-Speicherort.

**Hinweis** 
 *Streaming* ist der Ausdruck, der verwendet wird, um den Prozess zum Abrufen von Inhalten aus einem sequenzierten Anwendungspaket zu beschreiben, beginnend mit dem primären Feature-Block und anschließendes Abrufen zusätzlicher Blöcke nach Bedarf.

 

Der Speicherort der Streaming-Quelle ist in der Regel ein Server, auf den der Computer des Benutzers zugreifen kann. einige elektronische Verteilungssysteme wie Microsoft Endpoint Configuration Manager können die SFT-Datei jedoch auf dem Computer des Benutzers verteilen und dann das virtuelle Anwendungspaket lokal aus dem Cache dieses Computers streamen.

**Hinweis**  Ein Streaming-Quellspeicherort für virtuelle Pakete kann auf einem Computer eingerichtet werden, auf dem es sich nicht um einen Server handelt. Dies ist besonders hilfreich in einer kleinen Zweigstelle, die keinen Server hat.

 

Die Streaming-Quellen, die zum Speichern sequenzierter Anwendungen verwendet werden können, werden in der folgenden Tabelle beschrieben.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Servertyp</th>
<th align="left">Protokoll</th>
<th align="left">Vorteile</th>
<th align="left">Nachteile</th>
<th align="left">Links</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dateiserver</p></td>
<td align="left"><p>Datei</p></td>
<td align="left"><ul>
<li><p>Einfache, kostengünstige Lösung zum Konfigurieren eines vorhandenen Dateiservers mit \Content-Freigabe</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Kein aktives Upgrade</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)">So konfigurieren Sie den Dateiserver</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>IIS-Server</p></td>
<td align="left"><p>HTTP/https</p></td>
<td align="left"><ul>
<li><p>Unterstützt erhöhte Sicherheit mit HTTPS-Protokoll.</p></li>
<li><p>Unterstützt das Streaming an Remotecomputer über das Internet</p></li>
<li><p>Nur ein Port in der Firewall zu öffnen</p></li>
<li><p>Hochgradig skalierbar</p></li>
<li><p>Vertrautes Protokoll</p></li>
</ul></td>
<td align="left"><ul>
<li><p>IIS muss verwaltet werden</p></li>
<li><p>Kein aktives Upgrade</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)">So konfigurieren Sie den Server für IIS</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Application Virtualization Streaming Server</p></td>
<td align="left"><p>RTSP/RTSPS</p></td>
<td align="left"><ul>
<li><p>Aktives Upgrade</p></li>
<li><p>Unterstützt erweiterte Sicherheit mithilfe des RTSPS-Protokolls</p></li>
<li><p>Nur ein Port in der Firewall zu öffnen (nur RTSPS)</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Duale Infrastruktur</p></li>
<li><p>Server Verwaltungsanforderung</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">So konfigurieren Sie Anwendung Virtualisierung Management Server</a></p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)

[Übersicht über Electronic Software Distribution-basierte Szenarien](electronic-software-distribution-based-scenario-overview.md)

[Bestimmen der Veröffentlichungsmethode](determine-your-publishing-method.md)

 

 





