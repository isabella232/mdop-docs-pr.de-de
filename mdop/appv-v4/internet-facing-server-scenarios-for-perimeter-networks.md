---
title: Mit dem Internet verbundene Szenarien für Umkreisnetzwerke
description: Mit dem Internet verbundene Szenarien für Umkreisnetzwerke
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806644"
---
# Mit dem Internet verbundene Szenarien für Umkreisnetzwerke


App-v 4.5 unterstützt Server Szenarien mit Internet Verbindung, bei denen Benutzer, die nicht mit dem Unternehmensnetzwerk verbunden sind oder die Verbindung mit dem Netzwerk trennen, weiterhin App-v verwenden können. Wie in der folgenden Abbildung zu sehen ist, wird nur die Verwendung von sicheren Protokollen im Internet (RTSPS und HTTPS) unterstützt.

![App-v-Firewall-Positionierungs Diagramm](images/appvfirewalls.gif)

Sie können eine mit dem Internet verbundene Lösung mithilfe eines ISA-Servers einrichten, in dem sich die App-V-Infrastruktur wie folgt auf dem internen Netzwerk befindet:

-   Erstellen Sie eine Webveröffentlichungsregel für den IIS-Server, auf dem sich die ICO-und OSD-Dateien befinden – und optional die Pakete für Streaming –, die sich im internen Netzwerk befinden. Detaillierte Anweisungen finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151982> .

-   Erstellen Sie eine Server Veröffentlichungsregel für den App-V Web Management Server (RTSPS). Detaillierte Anweisungen finden Sie unter [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .

Wie in der folgenden Abbildung dargestellt: Wenn die Infrastruktur andere Firewalls zwischen dem Client und dem ISA-Server oder zwischen dem ISA-Server und dem internen Netzwerk implementiert hat, müssen sowohl RTSPS (TCP 322) als auch HTTPS-Firewallregeln (TCP 443) erstellt werden, um den Datenfluss zu unterstützen. Wenn Firewalls zwischen dem ISA-Server und dem internen Netzwerk implementiert wurden, muss der für Domänenmitglieder erforderliche Standarddaten Verkehr zum Tunneln durch die Firewall zugelassen werden (DNS, LDAP, Kerberos, SMB/CIFS).

![App-v Umkreisnetzwerk-Firewall-Diagramm](images/appvperimeternetworkfirewall.gif)

Da die Firewall-Lösungen von Umgebung zu Umgebung unterschiedlich sind, werden in diesem Thema die Anleitungen beschrieben, die erforderlich sind, um eine mit dem Internet verbundene App-V-Umgebung im Umkreisnetzwerk zu konfigurieren. Diese Informationen enthalten auch die empfohlenen internen Netzwerkserver.

Platzieren Sie die folgenden Server im Umkreisnetzwerk:

-   App-V-Verwaltungs Server

-   IIS-Server für Veröffentlichung und Streaming

**Hinweis**  Es wird empfohlen, den Verwaltungsserver und den IIS-Server auf separaten Computern zu platzieren.

 

Platzieren Sie die folgenden Server im internen Netzwerk:

-   Content Server

-   Datenspeicher (SQL Server)

-   Active Directory-Domänen Controller

## Verkehrsanforderungen


In den folgenden Tabellen sind die Datenverkehrsanforderungen für die Kommunikation aus dem Internet und dem Umkreisnetzwerk sowie vom Umkreisnetzwerk zum internen Netzwerk aufgeführt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Datenverkehrsanforderungen vom Internet zu Umkreisnetzwerk</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSPS (Veröffentlichungs Aktualisierungs-und Streaming-Pakete)</p></td>
<td align="left"><p>TCP 322 standardmäßig; Dies kann in App-V Management Server geändert werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPS (Veröffentlichungs-ICO-und OSD-Dateien und Streaming-Pakete)</p></td>
<td align="left"><p>TCP 443 standardmäßig; Dies kann in der IIS-Konfiguration geändert werden.</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Datenverkehrsanforderungen vom Umkreisnetzwerk zum internen Netzwerk</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQLServer</p></td>
<td align="left"><p>TCP 1433 ist der Standard, kann aber in SQL Server konfiguriert werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>Wenn sich das Inhaltsverzeichnis Remote vom Verwaltungs Server oder IIS-Server befindet (empfohlen).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kerberos</p></td>
<td align="left"><p>TCP und UDP 88</p></td>
</tr>
<tr class="even">
<td align="left"><p>LDAP</p></td>
<td align="left"><p>TCP und UDP 389</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DNS</p></td>
<td align="left"><p>Für die Namensauflösung interner Ressourcen (kann mit der Verwendung der Host-Datei auf Umkreisnetzwerk Servern eliminiert werden)</p></td>
</tr>
</tbody>
</table>

 

 

 





