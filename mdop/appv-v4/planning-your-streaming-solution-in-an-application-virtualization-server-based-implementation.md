---
title: Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung
description: Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806479"
---
# Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung


Wenn Sie Application Virtualization-Streamingserver in Verbindung mit ihrer auf Application Virtualization Management Server basierenden Implementierung verwenden möchten, können Sie aus verschiedenen alternativen auswählen und dabei die Infrastruktur nutzen, die bereits vorhanden ist. Wenn Sie beispielsweise bereits über Server in ihren Außendienst Niederlassungen verfügen, können Sie die Application Virtualization \\CONTENT-Freigabe auf diesen Servern platzieren und dann die Clients so konfigurieren, dass Sie diese Inhaltsfreigabe als Anwendungsinhalts Quelle verwenden. Wenn Sie sich für die Verwendung von Application Virtualization-Verwaltungsservern entscheiden, beispielsweise weil Sie nur über ein einzelnes Office verfügen, können die Clients Inhalte von diesem Server streamen.

Zu den unterstützten Optionen zählen die Verwendung eines Dateiservers, eines IIS-Servers oder eines Application Virtualization Streaming-Servers. Sie können den Application Virtualization Streaming Server auch auf einem vorhandenen Dateiserver oder IIS-Server installieren. Die Merkmale dieser verschiedenen Optionen sind in der folgenden Tabelle zusammengefasst.

**Hinweis**  Das Feature "Aktives Upgrade" ermöglicht das Hinzufügen einer neuen Version einer Anwendung zu einem App-V-Verwaltungsserver oder Streamingserver, ohne dass dies Auswirkungen auf die Benutzer hat, die die Anwendung zurzeit ausführen. Die APP-v-Clients erhalten automatisch die neueste Version der Anwendung vom APP-v-Verwaltungsserver oder Streamingserver, wenn der Benutzer die Anwendung das nächste Mal startet. Für dieses Feature ist die Verwendung des RTSP (S)-Protokolls erforderlich.

 

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
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)">So konfigurieren Sie Application Virtualization Streaming Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Application Virtualization-Verwaltungs Server</p></td>
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


[Application Virtualization Server-basiertes Szenario](application-virtualization-server-based-scenario.md)

[Übersicht über die Application Virtualization-Systemkomponenten](overview-of-the-application-virtualization-system-components.md)

[Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





