---
title: Konfigurieren der MBAM 2.5-Serverfunktionen
description: Konfigurieren der MBAM 2.5-Serverfunktionen
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809727"
---
# Konfigurieren der MBAM 2.5-Serverfunktionen


Verwenden Sie diese Informationen als Ausgangspunkt für die Konfiguration der Microsoft BitLocker-MBAM-2,5-Server Features nach [der Installation der MBAM 2,5-Server Software](installing-the-mbam-25-server-software.md). Es gibt zwei Methoden, mit denen Sie MBAM konfigurieren können:

-   MBAM-Serverkonfigurations-Assistent

-   Windows PowerShell-Cmdlets

## Bevor Sie mit dem Konfigurieren der MBAM-Server Features beginnen


Überprüfen und führen Sie die folgenden Schritte aus, bevor Sie mit dem Konfigurieren der MBAM-Server Features beginnen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Wo erhalte ich Anweisungen?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Überprüfen Sie die empfohlene Architektur für MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">High-Level-Architektur für MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Überprüfen Sie die unterstützten Konfigurationen für MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Von MBAM 2.5 unterstützte Konfigurationen</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Führen Sie die erforderlichen Voraussetzungen für jeden Server aus.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installieren der MBAM 2.5-Serversoftware</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell zum Konfigurieren von MBAM-Server Features (wenn Sie diese Methode zum Konfigurieren von MBAM-Server Features verwenden).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>

 

## Schritte zum Konfigurieren der MBAM-Server Features


In jeder Zeile in der folgenden Tabelle werden die Features beschrieben, die Sie auf einem separaten Server konfigurieren, entsprechend der empfohlenen [allgemeinen Architektur für MBAM 2,5](high-level-architecture-for-mbam-25.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Zu installierende Features</th>
<th align="left">Wo erhalte ich Anweisungen?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Konfigurieren Sie die Datenbanken.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">So konfigurieren Sie die MBAM 2.5-Datenbanken</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren Sie die Berichte.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">So konfigurieren Sie die MBAM 2.5-Berichte</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Konfigurieren Sie die Webanwendungen.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">So konfigurieren Sie die MBAM 2.5-Webanwendungen</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren Sie die System Center Configuration Manager-Integration (falls zutreffend).</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager</a></p></td>
</tr>
</tbody>
</table>

 

Eine Liste der Ereignisse zur Konfiguration von MBAM Server-Features finden Sie unter [Serverereignisprotokolle](server-event-logs.md).



## Verwandte Themen


Konfigurieren der MBAM 2.5-Serverfunktionen
 

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




