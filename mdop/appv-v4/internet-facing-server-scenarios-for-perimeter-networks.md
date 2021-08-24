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
ms.openlocfilehash: 7415cf7a97edc646653df552723667bac8d25fdc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910690"
---
# <a name="internet-facing-server-scenarios-for-perimeter-networks"></a>Mit dem Internet verbundene Szenarien für Umkreisnetzwerke


App-V 4.5 unterstützt Internet-bezogene Serverszenarien, in denen Benutzer, die nicht mit dem Unternehmensnetzwerk verbunden sind oder keine Verbindung mit dem Netzwerk herstellen, weiterhin App-V verwenden können. Wie in der folgenden Abbildung dargestellt, wird nur die Verwendung sicherer Protokolle im Internet (RTSPS und HTTPS) unterstützt.

![App-v-Firewall-Positionierungsdiagramm.](images/appvfirewalls.gif)

Sie können eine Internetlösung mithilfe eines ISA-Servers einrichten, auf dem sich die App-V-Infrastruktur im internen Netzwerk auf folgende Weise befindet:

-   Erstellen Sie eine Webveröffentlichungsregel für den IIS-Server, der die ICO- und OSD-Dateien hostet , und optional die Pakete für streaming, die sich im internen Netzwerk befinden. Detaillierte Schritte finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151982> .

-   Erstellen Sie eine Serververöffentlichungsregel für den App-V Web Management Server (RTSPS). Detaillierte Schritte finden Sie unter [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .

Wie in der folgenden Abbildung dargestellt, müssen, wenn die Infrastruktur andere Firewalls zwischen dem Client und dem ISA-Server oder zwischen dem ISA-Server und dem internen Netzwerk implementiert hat, sowohl RTSPS -Firewallregeln (TCP 322) als auch HTTPS-Firewallregeln (TCP 443) erstellt werden, um den Datenverkehrsfluss zu unterstützen. Wenn Firewalls zwischen dem ISA-Server und dem internen Netzwerk implementiert wurden, muss der für Domänenmitglieder erforderliche Standarddatenverkehr auch zum Tunneln über die Firewall (DNS, LDAP, Kerberos, SMB/CIFS) zulässig sein.

![App-v-Umkreisnetzwerkfirewalldiagramm.](images/appvperimeternetworkfirewall.gif)

Da die Firewalllösungen von Umgebung zu Umgebung variieren, werden in den Anleitungen in diesem Thema der Datenverkehr beschrieben, der erforderlich wäre, um eine mit dem Internet verbundene App-V-Umgebung im Umkreisnetzwerk zu konfigurieren. Diese Informationen umfassen auch die empfohlenen internen Netzwerkserver.

Platzieren Sie die folgenden Server im Umkreisnetzwerk:

-   App-V-Verwaltungsserver

-   IIS-Server für Veröffentlichung und Streaming

**Hinweis:**  
Es ist eine bewährte Methode, den Verwaltungsserver und iis-Server auf separaten Computern zu platzieren.

 

Platzieren Sie die folgenden Server im internen Netzwerk:

-   Inhaltsserver

-   Datenspeicher (SQL Server)

-   Active Directory-Domänencontroller

## <a name="traffic-requirements"></a>Datenverkehrsanforderungen


In den folgenden Tabellen sind die Datenverkehrsanforderungen für die Kommunikation aus dem Internet und dem Umkreisnetzwerk sowie vom Umkreisnetzwerk zum internen Netzwerk aufgeführt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Datenverkehrsanforderungen vom Internet zum Umkreisnetzwerk</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSPS (Veröffentlichung von Aktualisierungs- und Streamingpaketen)</p></td>
<td align="left"><p>TCP 322 standardmäßig; Dies kann im App-V-Verwaltungsserver geändert werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPS (Veröffentlichen von ICO- und OSD-Dateien und Streamingpaketen)</p></td>
<td align="left"><p>TCP 443 standardmäßig; dies kann in der IIS-Konfiguration geändert werden.</p></td>
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
<td align="left"><p>TCP 1433 ist die Standardeinstellung, kann aber in SQL Server konfiguriert werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>Wenn sich das Inhaltsverzeichnis remote von den Verwaltungsservern oder IIS-Servern befindet (empfohlen).</p></td>
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
<td align="left"><p>Für die Namensauflösung interner Ressourcen (kann durch die Verwendung der Hostdatei auf Umkreisnetzwerkservern eliminiert werden)</p></td>
</tr>
</tbody>
</table>

 

 

 





