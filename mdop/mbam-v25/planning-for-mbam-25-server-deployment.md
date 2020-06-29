---
title: Planen der Serverbereitstellung für MBAM 2.5
description: Planen der Serverbereitstellung für MBAM 2.5
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811620"
---
# Planen der Serverbereitstellung für MBAM 2.5


In diesem Thema sind die Features aufgeführt, die Sie für die eigenständige und Configuration Manager-Topologie von MBAM bereitstellen, und es wird die Reihenfolge aufgeführt, in der Sie bereitgestellt werden müssen. Es gibt eine empfohlene Konfiguration für jede Topologie. Sie können jedoch MBAM-Server Datenbanken und-Features je nach Ihren Skalierbarkeitsanforderungen in unterschiedlichen Konfigurationen und auf mehreren Servern konfigurieren.

## Wichtige Planungsüberlegungen für Topologien


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Erwägungen</th>
<th align="left">Details oder Zweck</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Überprüfen Sie die folgenden Punkte, bevor Sie die Bereitstellung starten:</p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Von MBAM 2.5 unterstützte Konfigurationen</a></p></li>
</ul></td>
<td align="left"><p>Jedes MBAM-Feature hat bestimmte Voraussetzungen, die erfüllt sein müssen, bevor Sie die MBAM-Installation starten.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker-Wiederherstellungsschlüssel in MBAM verfallen nach einer einmaligen Verwendung.</p></td>
<td align="left"><p>Eine einmalige Verwendung bedeutet, dass der Wiederherstellungsschlüssel über die Website "Verwaltung und Überwachung" (auch als "Helpdesk" bezeichnet), Self-Service-Portal oder mithilfe des <strong> Windows PowerShell-Cmdlets Get-MbamBitLockerRecoveryKey abgerufen wurde </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verfolgen Sie die Namen der Computer, auf denen Sie die einzelnen Features konfigurieren. Diese Informationen werden während des gesamten Konfigurationsprozesses verwendet.</p></td>
<td align="left"><p>Möglicherweise möchten Sie die <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> MBAM 2,5-Bereitstellungscheckliste </a> für diesen Zweck verwenden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren Sie nur die Gruppenrichtlinieneinstellungen im MDOP-MBAM (BitLocker-Verwaltungsknoten). Ändern Sie nicht die Gruppenrichtlinieneinstellungen im BitLocker Drive Encryption-Knoten.</p></td>
<td align="left"><p>Wenn Sie die Gruppenrichtlinieneinstellungen im Knoten BitLocker Drive Encryption ändern, funktioniert MBAM nicht.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a>Planen der MBAM Server-Bereitstellung – eigenständige Topologie


Für die eigenständige Topologie wird eine Konfiguration mit zwei Servern für Produktionsumgebungen empfohlen, obwohl Konfigurationen von drei bis vier Servern verwendet werden können.

Die Server Infrastruktur für die eigenständige MBAM-Topologie umfasst die folgenden Features, die in der angegebenen Reihenfolge konfiguriert werden müssen:

1.  Datenbanken (Compliance-und Audit-Datenbank und Wiederherstellungsdatenbank)

2.  Berichte

3.  Web Applications (und die entsprechenden Webdienste)

    -   Website "Verwaltung und Überwachung"

    -   Self-Service-Portal

Eine Beschreibung dieser Features finden Sie unter [Architektur auf höherer Ebene von MBAM 2,5 mit eigenständiger Topologie](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a>Planen der MBAM Server Bereitstellung – Configuration Manager-Topologie


Für die Configuration Manager-Integrations Topologie wird eine Konfiguration mit drei Servern für Produktionsumgebungen empfohlen, auch wenn Konfigurationen von zusätzlichen Servern verwendet werden können.

Die Server Infrastruktur für die MBAM Configuration Manager-Topologie enthält die folgenden Features, die in der angegebenen Reihenfolge konfiguriert oder ausgeführt werden müssen:

1.  Datenbanken (Compliance-und Audit-Datenbank und Wiederherstellungsdatenbank)

2.  Berichte

3.  Web Applications (und die entsprechenden Webdienste)

    -   Website "Verwaltung und Überwachung"

    -   Self-Service-Portal

4.  Integration von System Center Configuration Manager

Eine Beschreibung dieser Features finden Sie unter [Architektur auf höherer Ebene in MBAM 2,5 mit der Configuration Manager-Integrations Topologie](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).



## Verwandte Themen


[Planen der Bereitstellung von MBAM 2.5](planning-to-deploy-mbam-25.md)

[Bereitstellen der Serverinfrastruktur von MBAM 2.5](deploying-the-mbam-25-server-infrastructure.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





