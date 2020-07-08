---
title: Planen einer Streaminglösung in einer ESD-Implementierung (Electronic Software Distribution)
description: Planen einer Streaminglösung in einer ESD-Implementierung (Electronic Software Distribution)
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806475"
---
# Planen einer Streaminglösung in einer ESD-Implementierung (Electronic Software Distribution)


Wenn Sie sich entschließen, Streamingserver in Verbindung mit Ihrem ESD-System zu verwenden, um Anwendungsinhalte auf Ihren Endbenutzercomputern zur Verfügung zu stellen, können Sie aus verschiedenen alternativen auswählen und dabei die Infrastruktur nutzen, die bereits vorhanden ist. Wenn Ihr ESD-System beispielsweise über Softwareverteilungsfreigaben auf Servern in ihren Außendienst Niederlassungen verfügt, können Sie die Application Virtualization \\CONTENT-Freigabe auf diesen Servern platzieren und dann die Clients so konfigurieren, dass Sie diese Inhaltsfreigabe als Anwendungsinhalts Quelle verwenden. Zu den unterstützten Optionen gehört die Verwendung eines Dateiservers oder eines IIS-Servers. Sie können den Application Virtualization Streaming Server auch auf einem vorhandenen Dateiserver oder IIS-Server installieren.

Der Application Virtualization Streaming Server bietet Unterstützung für das aktive Upgrade-Feature in Application Virtualization. Das Feature "Aktives Upgrade" ermöglicht das Hinzufügen einer neuen Version einer Anwendung zu einem App-V-Verwaltungsserver oder Streamingserver, ohne dass dies Auswirkungen auf die Benutzer hat, die die Anwendung zurzeit ausführen. Die APP-v-Clients erhalten automatisch die neueste Version der Anwendung vom APP-v-Verwaltungsserver oder Streamingserver, wenn der Benutzer die Anwendung das nächste Mal startet. Für dieses Feature ist die Verwendung des RTSP (S)-Protokolls erforderlich. Wenn Sie den Application Virtualization Streaming Server nicht verwenden möchten, müssen Sie Anwendungspaket-Upgrades explizit mithilfe des ESD-Systems verwalten.

**Hinweis**  Der Zugriff auf die Anwendungen wird mithilfe von Sicherheitsgruppen in den Active Directory-Domänendiensten gesteuert, daher müssen Sie einen Prozess für das Einrichten einer Sicherheitsgruppe für jede virtuelle Anwendung und für die Verwaltung der Benutzer planen, die jeder Gruppe hinzugefügt werden. Der Application Virtualization System-Administrator konfiguriert jeden Streamingserver so, dass diese Active Directory-Gruppen verwendet werden, indem ACLs auf die Anwendungsverzeichnisse unter der Inhaltsfreigabe angewendet werden, die den Zugriff auf die Pakete auf Grundlage der Active Directory-Gruppenmitgliedschaft steuert.

 

Die Merkmale der verfügbaren Streaming-Optionen sind in der folgenden Tabelle zusammengefasst.

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
<td align="left"><p>SMB</p></td>
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
<li><p>Unterstützt erweiterte Sicherheit mithilfe des HTTPS-Protokolls</p></li>
<li><p>Unterstützt das Streaming an Remotecomputer über das Internet</p></li>
<li><p>Nur ein Port in der Firewall zu öffnen</p></li>
<li><p>Skalierbare</p></li>
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
<li><p>Nur ein Port in der Firewall zu öffnen</p></li>
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


[So konfigurieren Sie Servern für die ESD-basierte Bereitstellung](how-to-configure-servers-for-esd-based-deployment.md)

[Übersicht über Sicherheit und Schutz](security-and-protection-overview.md)

[Veröffentlichen von virtuellen Anwendungen mit Electronic Software Distribution](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





