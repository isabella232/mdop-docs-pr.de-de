---
title: High-Level-Architektur von MBAM 2.5 mit Configuration Manager-Integrationstopologie
description: High-Level-Architektur von MBAM 2.5 mit Configuration Manager-Integrationstopologie
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: a0f9349391794100a670e382bb18d0713f4b5b60
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910720"
---
# <a name="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology"></a>Allgemeine Architektur von MBAM 2.5 mit Configuration Manager-Integrationstopologie

In diesem Thema wird die empfohlene Architektur für die Bereitstellung von Microsoft BitLocker Administration and Monitoring (MBAM) mit der Configuration Manager-Integrationstopologie beschrieben. Diese Topologie integriert MBAM in System Center Configuration Manager. Informationen zum Bereitstellen von MBAM mit der eigenständigen Topologie finden Sie unter ["High-Level Architecture of MBAM 2.5 with Stand-alone Topology".](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

Eine Liste der unterstützten Versionen der in diesem Thema erwähnten Software finden Sie unter ["Unterstützte Konfigurationen für MBAM 2.5".](mbam-25-supported-configurations.md)

**Wichtig**  
Windows To Go wird für die Configuration Manager-Integrationstopologieinstallation bei Verwendung von Configuration Manager 2007 nicht unterstützt.

 

## <a name="recommended-number-of-servers-and-supported-number-of-clients"></a>Empfohlene Anzahl von Servern und unterstützte Anzahl von Clients


Die empfohlene Anzahl von Servern und die unterstützte Anzahl von Clients in einer Produktionsumgebung lautet wie folgt:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Empfohlene Architektur</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Anzahl der Server und anderer Computer</p></td>
<td align="left"><p>Drei Server</p>
<p>Eine Arbeitsstation</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anzahl der unterstützten Clientcomputer</p></td>
<td align="left"><p>500,000</p></td>
</tr>
</tbody>
</table>

 

## <a name="differences-between-configuration-manager-integration-and-stand-alone-topologies"></a>Unterschiede zwischen Configuration Manager-Integration und eigenständigen Topologien


Die hauptunterschiede zwischen den Topologien sind:

-   Die Compliance- und Berichterstellungsfeatures werden aus MBAM entfernt und über Configuration Manager aufgerufen.

-   Berichte werden in der Configuration Manager-Verwaltungskonsole angezeigt, mit Ausnahme des Wiederherstellungsüberwachungsberichts, den Sie weiterhin von der MBAM-Verwaltungs- und Überwachungswebsite anzeigen.

## <a name="recommended-mbam-high-level-architecture-with-the-configuration-manager-integration-topology"></a>Empfohlene allgemeine MBAM-Architektur mit der Configuration Manager-Integrationstopologie


Im folgenden Diagramm und in der folgenden Tabelle wird die empfohlene allgemeine Architektur für MBAM mit der Configuration Manager-Integrationstopologie beschrieben. MBAM-Bereitstellungen mit mehreren Gesamtstrukturen erfordern eine unidirektionale oder bidirektionale Vertrauensstellung. Unidirektionale Vertrauensstellungen erfordern, dass die Serverdomäne der Clientdomäne vertraut.

![mbam2\-5.](images/mbam2-5-cmserver.png)

### <a name="database-server"></a>Datenbankserver

#### <a name="recovery-database"></a>Wiederherstellungsdatenbank

Dieses Feature ist auf einem Computer mit Windows Server konfiguriert und wird SQL Server Instanz unterstützt.

Die **Wiederherstellungsdatenbank** speichert Wiederherstellungsdaten, die von MBAM-Clientcomputern gesammelt werden.

#### <a name="audit-database"></a>Überwachungsdatenbank

Dieses Feature ist auf einem Computer mit Windows Server konfiguriert und wird SQL Server Instanz unterstützt.

Die **Überwachungsdatenbank** speichert Überwachungsaktivitätsdaten, die von Clientcomputern gesammelt werden, die auf Wiederherstellungsdaten zugegriffen haben.

#### <a name="reports"></a>Berichte

Dieses Feature ist auf einem Computer mit Windows Server konfiguriert und wird SQL Server Instanz unterstützt.

Die **Berichte** stellen Wiederherstellungsüberwachungsdaten für die Clientcomputer in Ihrem Unternehmen bereit. Sie können Berichte über die Configuration Manager-Konsole oder direkt über SQL Server Reporting Services anzeigen.

### <a name="configuration-manager-primary-site-server"></a>Configuration Manager – Primärer Standortserver

System Center Configuration Manager Integrationsfeature

-   Dieses Feature wird auf dem primären Konfigurations-Manager-Standortserver konfiguriert, der der oberste Server in Ihrer Configuration Manager-Infrastruktur ist.

-   Der **Configuration Manager-Server** sammelt die Hardwareinventurinformationen von Clientcomputern und wird verwendet, um die BitLocker-Kompatibilität von Clientcomputern zu melden.

-   Wenn Sie den Setup-Assistenten für die Verwaltung und Überwachung von Microsoft BitLocker ausführen, um die Serversoftware zu installieren, werden die Mbam Supported Computers-Auflistung, konfigurationsgrundwerte und Berichte auf dem primären Konfigurations-Manager-Standortserver konfiguriert.

-   Die **Configuration Manager-Konsole** muss auf demselben Computer installiert sein, auf dem Sie die MBAM Server-Software installieren.

### <a name="administration-and-monitoring-server"></a>Verwaltungs- und Überwachungsserver

#### <a name="administration-and-monitoring-website"></a>Verwaltungs- und Überwachungswebsite

Dieses Feature wird auf einem Computer konfiguriert, auf dem Windows Server ausgeführt wird.

Die **Verwaltungs- und Überwachungswebsite** wird für Folgendes verwendet:

-   Helfen Sie Endbenutzern, den Zugriff auf ihre Computer wiederzuerlangen, wenn sie gesperrt sind. (Dieser Bereich der Website wird häufig als Helpdesk bezeichnet.)

-   Zeigen Sie den Wiederherstellungsüberwachungsbericht an, der die Wiederherstellungsaktivität für Clientcomputer anzeigt. Andere Berichte werden in der Configuration Manager-Konsole angezeigt.

#### <a name="self-service-portal"></a>Self-Service-Portal

Dieses Feature wird auf einem Computer konfiguriert, auf dem Windows Server ausgeführt wird.

Das **Self-Service-Portal** ist eine Website, mit der sich Endbenutzer auf Clientcomputern unabhängig bei einer Website anmelden können, um einen Wiederherstellungsschlüssel zu erhalten, wenn sie ihr BitLocker-Kennwort verlieren oder vergessen.

#### <a name="monitoring-web-services-for-this-website"></a>Überwachen von Webdiensten für diese Website

Dieses Feature wird auf einem Computer installiert, auf dem Windows Server ausgeführt wird.

Die **Überwachungswebdienste** werden vom MBAM-Client und den Websites für die Kommunikation mit der Datenbank verwendet.

**Wichtig**<br>Der Überwachungswebdienst ist in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 nicht mehr verfügbar, da die MBAM-Websites direkt mit der Wiederherstellungsdatenbank kommunizieren. 

 

### <a name="management-workstation"></a>Verwaltungsarbeitsstation

#### <a name="mbam-group-policy-templates"></a>Vorlagen für MBAM-Gruppenrichtlinien

-   Die **MBAM-Gruppenrichtlinienvorlagen** sind Gruppenrichtlinieneinstellungen, die Implementierungseinstellungen für MBAM definieren, mit denen Sie die BitLocker-Laufwerkverschlüsselung verwalten können.

-   Bevor Sie MBAM ausführen, müssen Sie die Gruppenrichtlinienvorlagen von Vorlagen zum Abrufen von [MDOP-Gruppenrichtlinien (ADMX)](https://go.microsoft.com/fwlink/p/?LinkId=393941) herunterladen und auf einen Server oder eine Arbeitsstation kopieren, auf dem ein unterstützter Windows Server oder Windows Betriebssystem ausgeführt wird.

    **HINWEIS**<br>Die Arbeitsstation muss kein dedizierter Computer sein.

     

### <a name="mbam-client-and-configuration-manager-client-computer"></a>Computer mit MBAM-Client und Configuration Manager-Client

#### <a name="mbam-client-software"></a>MBAM-Clientsoftware

Der **MBAM-Client:**

-   Verwendet Gruppenrichtlinienobjekte, um die BitLocker-Laufwerkverschlüsselung auf Clientcomputern im Unternehmen zu erzwingen.

-   Erfasst den BitLocker-Wiederherstellungsschlüssel für drei Datentypen: Betriebssystemlaufwerke, Festplattenlaufwerke und USB-Datenlaufwerke (Wechseldatenträger).

-   Sammelt Wiederherstellungsinformationen und Computerinformationen zu den Clientcomputern.

#### <a name="configuration-manager-client"></a>Konfigurations-Manager – Client

Der **Configuration Manager-Client** ermöglicht Configuration Manager das Sammeln von Hardwarekompatibilitätsdaten über die Clientcomputer und das Melden von Kompatibilitätsinformationen.

 

## <a name="differences-in-mbam-deployment-for-supported-configuration-manager-versions"></a>Unterschiede bei der MBAM-Bereitstellung für unterstützte Configuration Manager-Versionen


Wenn Sie MBAM mit der Configuration Manager-Integrationstopologie bereitstellen, können Sie MBAM auf einem primären Standortserver installieren. Die MBAM-Installation funktioniert jedoch für System Center 2012 Configuration Manager und Configuration Manager 2007 unterschiedlich.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuration Manager-Version</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>System Center 2012 R2 Configuration Manager</p>
<p>System Center 2012 Configuration Manager</p></td>
<td align="left"><p>Wenn Sie MBAM auf einem primären Standortserver oder auf einem Zentraladministrationsserver installieren, führt MBAM alle Installationsaktionen auf diesem Standortserver aus.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 2007 R2</p>
<p>Configuration Manager 2007</p></td>
<td align="left"><p>Wenn Sie MBAM auf einem primären Standortserver installieren, der Teil einer größeren Configuration Manager-Hierarchie mit einem zentralen übergeordneten Standortserver ist, identifiziert MBAM den zentralen übergeordneten Standortserver und führt alle Installationsaktionen auf diesem übergeordneten Server aus. Die Installation umfasst die Überprüfung der Voraussetzungen und die Installation der Configuration Manager-Objekte und -Berichte.</p>
<p>Wenn Sie beispielsweise MBAM auf einem primären Standortserver installieren, der ein untergeordnetes Element eines zentralen übergeordneten Standortservers ist, installiert MBAM alle Configuration Manager-Objekte und -Berichte auf dem übergeordneten Server. Wenn Sie MBAM auf dem übergeordneten Server installieren, führt MBAM alle Installationsaktionen auf diesem übergeordneten Server aus.</p></td>
</tr>
</tbody>
</table>

 

## <a name="how-mbam-works-with-configuration-manager"></a>Funktionsweise von MBAM mit Configuration Manager


Die Integration von MBAM in Configuration Manager basiert auf einem Konfigurationspaket, das die in der folgenden Tabelle beschriebenen Elemente installiert.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">In Configuration Manager installierte Elemente</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Konfigurationsdaten</p></td>
<td align="left"><p>Die Konfigurationsdaten installieren eine Konfigurationsbaseline namens "BitLocker Protection", die zwei Konfigurationselemente enthält:</p>
<ul>
<li><p>BitLocker-Betriebssystemlaufwerkschutz</p></li>
<li><p>Schutz von BitLocker-Festplattenlaufwerken</p></li>
</ul>
<p>Der Konfigurationsbasisplan wird in der Mbam Supported Computers -Auflistung bereitgestellt, die auch erstellt wird, wenn MBAM installiert wird.</p>
<p>Die beiden Konfigurationselemente bieten die Grundlage für die Bewertung des Kompatibilitätsstatus der Clientcomputer. Diese Informationen werden in Configuration Manager erfasst, gespeichert und ausgewertet.</p>
<p>Die Konfigurationselemente basieren auf den Complianceanforderungen für Betriebssystemlaufwerke und Festplattenlaufwerke. Die erforderlichen Details für die bereitgestellten Computer werden gesammelt, damit die Kompatibilität für diese Laufwerkstypen ausgewertet werden kann.</p>
<p>Standardmäßig wertet der Konfigurationsbaseline den Compliancestatus alle 12 Stunden aus und sendet die Compliancedaten an Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Supported Computers-Auflistung</p></td>
<td align="left"><p>MBAM erstellt eine Sammlung, die als MBAM-unterstützte Computer bezeichnet wird. Der Konfigurationsbaseline ist auf Clientcomputer in dieser Sammlung ausgerichtet.</p>
<p>Dies ist eine dynamische Sammlung. Standardmäßig wird sie alle 12 Stunden ausgeführt und wertet die Mitgliedschaft basierend auf drei Kriterien aus:</p>
<ul>
<li><p>Der Computer ist eine unterstützte Version des Windows Betriebssystems.</p></li>
<li><p>Der Computer ist ein physischer Computer. Virtuelle Computer werden nicht unterstützt.</p></li>
<li><p>Der Computer verfügt über ein Trusted Platform Module (TPM), das verfügbar ist. Für Windows 7 ist eine kompatible Version von TPM 1.2 oder höher erforderlich. Windows 10, Windows 8.1, Windows 8 und Windows To Go erfordern kein TPM.</p></li>
</ul>
<p>Die Sammlung wird für alle Computer ausgewertet, und es wird eine Teilmenge kompatibler Computer erstellt, die die Grundlage für die Compliancebewertung und Berichterstellung für die MBAM-Integration bietet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Berichte</p></td>
<td align="left"><p>Wenn Sie MBAM mit der Configuration Manager-Integrationstopologie konfigurieren, zeigen Sie alle Berichte in Configuration Manager an, mit Ausnahme des Wiederherstellungsüberwachungsberichts, dessen letzterer Sie weiterhin auf der MBAM-Verwaltungs- und Überwachungswebsite anzeigen. Die in Configuration Manager verfügbaren Berichte sind:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Bericht</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>BitLocker Enterprise Compliance-Dashboard</p></td>
<td align="left"><p>Bietet IT-Administratoren drei Ansichten von Informationen in einem einzigen Bericht: Compliancestatusverteilung, nicht konform – Fehlerverteilung und Verteilung des Compliancestatus nach Laufwerkstyp. Mithilfe von Drilldownoptionen für den Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem ausgewählten Status entsprechen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker Enterprise Compliancedetails</p></td>
<td align="left"><p>Ermöglicht IT-Administratoren das Anzeigen von Informationen zum BitLocker-Verschlüsselungscompliancestatus des Unternehmens und schließt den Compliancestatus für jeden Computer ein. Mithilfe von Drilldownoptionen für den Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem ausgewählten Status entsprechen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker-Computerkompatibilität</p></td>
<td align="left"><p>Ermöglicht IT-Administratoren, einen einzelnen Computer anzuzeigen und zu bestimmen, warum er mit dem Status "kompatibel" oder "nicht kompatibel" gemeldet wurde. Der Bericht zeigt auch den Verschlüsselungsstatus der Betriebssystemlaufwerke und Festplattenlaufwerke an.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker Enterprise Compliancezusammenfassung</p></td>
<td align="left"><p>Ermöglicht IT-Administratoren das Anzeigen des Status der COMPLIANCE von MBAM-Richtlinien im Unternehmen. Jeder Computerstatus wird ausgewertet, und der Bericht enthält eine Zusammenfassung der Kompatibilität aller Computer im Unternehmen mit der Richtlinie. Mithilfe von Drilldownoptionen für den Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem ausgewählten Status entsprechen.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <a name="related-topics"></a>Verwandte Themen


[Erste Schritte mit MBAM 2.5](getting-started-with-mbam-25.md)

[High-Level-Architektur von MBAM 2.5 mit eigenständiger Topologie](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[Beschreibung der Funktionen einer MBAM 2.5-Bereitstellung](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <a name="got-a-suggestion-for-mbam"></a>Haben Sie einen Vorschlag für MBAM?
- Hier können Sie [Vorschläge](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)hinzufügen oder abstimmen. 
- Verwenden Sie für MBAM-Probleme das [MBAM TechNet-Forum.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)




