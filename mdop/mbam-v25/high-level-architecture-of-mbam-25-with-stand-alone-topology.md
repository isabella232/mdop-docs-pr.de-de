---
title: High-Level-Architektur von MBAM 2.5 mit eigenständiger Topologie
description: High-Level-Architektur von MBAM 2.5 mit eigenständiger Topologie
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9ec9b1e4391fde3083564f34b5f89d1c5bd174f7
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910670"
---
# <a name="high-level-architecture-of-mbam-25-with-stand-alone-topology"></a>High-Level-Architektur von MBAM 2.5 mit eigenständiger Topologie


In diesem Thema wird die empfohlene Architektur für die Bereitstellung von Microsoft BitLocker Administration and Monitoring (MBAM) mit der eigenständigen Configuration Manager-Topologie beschrieben. In dieser Topologie wird MBAM als eigenständiges Produkt bereitgestellt. Alternativ können Sie MBAM mit der Configuration Manager-Integrationstopologie bereitstellen, die MBAM in Configuration Manager integriert. Weitere Informationen finden Sie unter ["High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology".](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

Eine Liste der unterstützten Versionen der in diesem Thema erwähnten Software finden Sie unter ["Unterstützte Konfigurationen für MBAM 2.5".](mbam-25-supported-configurations.md)

**Hinweis:**  
Es wird empfohlen, nur in Testumgebungen eine Architektur mit einem einzelnen Server zu verwenden.

 

## <a name="recommended-number-of-servers-and-supported-number-of-clients"></a>Empfohlene Anzahl von Servern und unterstützte Anzahl von Clients


Die empfohlene Anzahl von Servern und die unterstützte Anzahl von Clients in einer Produktionsumgebung lautet wie folgt:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Empfohlene Architektur in einer Produktionsumgebung</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Anzahl der Server und anderer Computer</p></td>
<td align="left"><p>Zwei Server</p>
<p>Eine Arbeitsstation</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anzahl der unterstützten Clientcomputer</p></td>
<td align="left"><p>500,000</p></td>
</tr>
</tbody>
</table>

 

## <a name="recommended-mbam-high-level-architecture-with-the-stand-alone-topology"></a>Empfohlene allgemeine MBAM-Architektur mit der eigenständigen Topologie


Im folgenden Diagramm und in der folgenden Tabelle wird die empfohlene allgemeine Zwei-Server-Architektur für MBAM mit der eigenständigen Topologie beschrieben. MBAM-Bereitstellungen mit mehreren Gesamtstrukturen erfordern eine unidirektionale oder bidirektionale Vertrauensstellung. Unidirektionale Vertrauensstellungen erfordern, dass die Serverdomäne der Clientdomäne vertraut.

![mbam2.](images/mbam2-5-2servers.png)

Serverfeatures, die auf diesem Server für die Beschreibungsdatenbank konfiguriert werden sollen

Compliance- und Überwachungsdatenbank

Dieses Feature ist auf einem Server mit Windows Server konfiguriert und wird SQL Server Instanz unterstützt.

Die **Compliance- und Überwachungsdatenbank** speichert Compliancedaten, die in erster Linie für Berichte verwendet werden, die SQL Server Reporting Services Hosts.

Wiederherstellungsdatenbank

Dieses Feature ist auf einem Server mit Windows Server konfiguriert und wird SQL Server Instanz unterstützt.

Die **Wiederherstellungsdatenbank** speichert Wiederherstellungsdaten, die von MBAM-Clientcomputern gesammelt werden.

Berichte

Dieses Feature ist auf einem Server mit Windows Server konfiguriert und wird SQL Server Instanz unterstützt.

Die **Berichte** enthalten Wiederherstellungsüberwachungs- und Compliancestatusdaten zu den Clientcomputern in Ihrem Unternehmen. Sie können über die Verwaltungs- und Überwachungswebsite oder direkt über SQL Server Reporting Services auf die Berichte zugreifen.

Verwaltungs- und Überwachungsserver

Verwaltungs- und Überwachungswebsite

Dieses Feature wird auf einem Computer konfiguriert, auf dem Windows Server ausgeführt wird.

Die **Verwaltungs- und Überwachungswebsite** wird für Folgendes verwendet:

-   Helfen Sie Endbenutzern, den Zugriff auf ihre Computer wiederzuerlangen, wenn sie gesperrt sind. (Dieser Bereich der Website wird häufig als Helpdesk bezeichnet.)

-   Anzeigen von Berichten, die den Compliancestatus und die Wiederherstellungsaktivität für Clientcomputer anzeigen.

Self-Service Portal

Dieses Feature wird auf einem Computer konfiguriert, auf dem Windows Server ausgeführt wird.

Das **Self-Service-Portal** ist eine Website, mit der sich Endbenutzer auf Clientcomputern unabhängig bei einer Website anmelden können, um einen Wiederherstellungsschlüssel zu erhalten, wenn sie ihr BitLocker-Kennwort verlieren oder vergessen.

Überwachen von Webdiensten für diese Website

Dieses Feature wird auf einem Computer konfiguriert, auf dem Windows Server ausgeführt wird.

Die **Überwachungswebdienste** werden vom MBAM-Client und den Websites für die Kommunikation mit der Datenbank verwendet.

**Wichtig**  
Der Überwachungswebdienst ist in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 nicht mehr verfügbar, da die MBAM-Websites direkt mit der Wiederherstellungsdatenbank kommunizieren.

 

Verwaltungsarbeitsstation

MBAM-Gruppenrichtlinienvorlagen

-   Die MBAM-Gruppenrichtlinienvorlagen sind Gruppenrichtlinieneinstellungen, die Implementierungseinstellungen für MBAM definieren, mit denen Sie die BitLocker-Laufwerkverschlüsselung verwalten können.

-   Bevor Sie MBAM ausführen, müssen Sie die Gruppenrichtlinienvorlagen von Vorlagen zum Abrufen von [MDOP-Gruppenrichtlinien (ADMX)](https://go.microsoft.com/fwlink/p/?LinkId=393941) herunterladen und auf einen Server oder eine Arbeitsstation kopieren, auf dem ein unterstützter Windows Server oder Windows Betriebssystem ausgeführt wird.

-   Die Arbeitsstation muss kein dedizierter Computer sein.

MBAM-Client und Configuration Manager-Clientcomputer

MBAM-Clientsoftware

Der MBAM-Client:

-   Verwendet Gruppenrichtlinienobjekte, um die BitLocker-Laufwerkverschlüsselung auf Clientcomputern im Unternehmen zu erzwingen.

-   Erfasst den Bitlocker-Wiederherstellungsschlüssel für drei Datentypen: Betriebssystemlaufwerke, Festplattenlaufwerke und USB-Datenlaufwerke(Removable).

-   Sammelt Wiederherstellungsinformationen und Computerinformationen zu den Clientcomputern.



## <a name="related-topics"></a>Verwandte Themen


[Erste Schritte mit MBAM 2.5](getting-started-with-mbam-25.md)

[High-Level-Architektur von MBAM 2.5 mit Configuration Manager-Integrationstopologie](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[Beschreibung der Funktionen einer MBAM 2.5-Bereitstellung](illustrated-features-of-an-mbam-25-deployment.md)

 

## <a name="got-a-suggestion-for-mbam"></a>Haben Sie einen Vorschlag für MBAM?
- Hier können Sie [Vorschläge](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)hinzufügen oder abstimmen. 
- Verwenden Sie für MBAM-Probleme das [MBAM TechNet-Forum.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam) 





