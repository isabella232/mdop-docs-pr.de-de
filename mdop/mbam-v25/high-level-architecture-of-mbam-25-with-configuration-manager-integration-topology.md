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
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811350"
---
# Allgemeine Architektur von MBAM 2,5 mit der Configuration Manager-Integrations Topologie

In diesem Thema wird die empfohlene Architektur für die Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der Configuration Manager-Integrations Topologie beschrieben. Diese Topologie integriert MBAM mit System Center Configuration Manager. Informationen zum Bereitstellen von MBAM mit der eigenständigen Topologie finden Sie unter [Architektur auf höherer Ebene von MBAM 2,5 mit eigenständiger Topologie](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).

Eine Liste der unterstützten Versionen der in diesem Thema erwähnten Software finden Sie unter [unterstützte MBAM 2,5-Konfigurationen](mbam-25-supported-configurations.md).

**Wichtig**  Windows to go wird bei der Installation der Configuration Manager-Integrations Topologie nicht unterstützt, wenn Sie Configuration Manager 2007 verwenden.

 

## Empfohlene Anzahl von Servern und unterstützte Anzahl von Clients


Die empfohlene Anzahl von Servern und unterstützten Clients in einer Produktionsumgebung lautet wie folgt:

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
<p>Eine Workstation</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anzahl der unterstützten Clientcomputer</p></td>
<td align="left"><p>500.000</p></td>
</tr>
</tbody>
</table>

 

## Unterschiede zwischen der Configuration Manager-Integration und eigenständigen Topologien


Die wichtigsten Unterschiede zwischen den Topologien sind:

-   Die Kompatibilitäts-und Berichterstattungsfeatures werden aus MBAM entfernt, und Sie können über den Configuration Manager darauf zugreifen.

-   Berichte werden über die Configuration Manager-Verwaltungskonsole angezeigt, mit Ausnahme des Wiederherstellungs Überwachungsberichts, den Sie weiterhin über die MBAM-Website für Verwaltung und Überwachung anzeigen.

## Empfohlene MBAM-Architektur auf höherer Ebene mit der Configuration Manager-Integrations Topologie


Das folgende Diagramm und die folgende Tabelle beschreiben die empfohlene allgemeine Architektur für MBAM mit der Configuration Manager-Integrations Topologie. MBAM Multi-Forest-Bereitstellungen erfordern eine unidirektionale oder bidirektionale Vertrauensstellung. Unidirektionale Vertrauensstellungen setzen voraus, dass die Server Domäne der Clientdomäne vertraut.

![mbam2\-5](images/mbam2-5-cmserver.png)

### Datenbankserver

#### Wiederherstellungsdatenbank

Dieses Feature ist auf einem Computer mit Windows Server und unterstützten SQL Server-Instanzen konfiguriert.

Die **Wiederherstellungsdatenbank** speichert Wiederherstellungsdaten, die von MBAM-Client Computern erfasst werden.

#### Überwachungsdatenbank

Dieses Feature ist auf einem Computer mit Windows Server und unterstützten SQL Server-Instanzen konfiguriert.

In der **Überwachungsdatenbank** werden Überwachungs Aktivitätsdaten gespeichert, die von Clientcomputern erfasst werden, die auf Wiederherstellungsdaten zugreifen.

#### Berichte

Dieses Feature ist auf einem Computer mit Windows Server und unterstützten SQL Server-Instanzen konfiguriert.

In den **Berichten** werden Wiederherstellungs Überwachungsdaten für die Clientcomputer in Ihrem Unternehmen bereitgestellt. Sie können Berichte über die Configuration Manager-Konsole oder direkt in SQL Server Reporting Services anzeigen.

### Primärer Configuration Manager-Standortserver

System Center Configuration Manager-Integrations Feature

-   Dieses Feature ist auf dem primären Configuration Manager-Standortserver konfiguriert, dem Server der obersten Ebene in Ihrer Configuration Manager-Infrastruktur.

-   Der **Configuration Manager-Server** sammelt die Hardwareinventurinformationen von Clientcomputern und wird verwendet, um die BitLocker-Kompatibilität von Clientcomputern zu melden.

-   Wenn Sie den Setup-Assistenten für die Microsoft BitLocker-Verwaltung und-Überwachung ausführen, um die Server Software zu installieren, werden die Auflistung der MBAM-unterstützten Computer, die Konfigurationsbasislinie und die Berichte auf dem primären Configuration Manager-Standortserver konfiguriert.

-   Die **Configuration Manager-Konsole** muss auf demselben Computer installiert sein, auf dem Sie die MBAM-Server Software installieren.

### Verwaltungs-und Überwachungsserver

#### Website "Verwaltung und Überwachung"

Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.

Die **Websiteverwaltung und Überwachung** wird verwendet, um Folgendes zu tun:

-   Helfen Sie den Endbenutzern beim wieder Zugriff auf Ihre Computer, wenn Sie gesperrt sind. (Dieser Bereich der Website wird im Allgemeinen als Help Desk bezeichnet.)

-   Anzeigen des Wiederherstellungs Überwachungsberichts, in dem Wiederherstellungsaktivitäten für Clientcomputer angezeigt werden. Andere Berichte werden über die Configuration Manager-Konsole angezeigt.

#### Self-Service-Portal

Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.

Das **Self-Service-Portal** ist eine Website, auf der sich Endbenutzer auf Clientcomputern selbstständig an einer Website anmelden können, um einen Wiederherstellungsschlüssel abzurufen, wenn Sie Ihr BitLocker-Kennwort verlieren oder vergessen.

#### Überwachen von Webdiensten für diese Website

Dieses Feature ist auf einem Computer mit Windows Server installiert.

Die **Überwachungs-Webdienste** werden vom MBAM-Client und den Websites verwendet, um mit der Datenbank zu kommunizieren.

**Wichtig**<br>Der Monitoring Web Service steht in der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 nicht mehr zur Verfügung, da die MBAM-Websites direkt mit der Wiederherstellungsdatenbank kommunizieren. 

 

### Verwaltungsarbeitsstation

#### MBAM-Gruppenrichtlinienvorlagen

-   Bei den **MBAM-Gruppenrichtlinienvorlagen** handelt es sich um Gruppenrichtlinieneinstellungen, die Implementierungs Einstellungen für MBAM definieren, mit denen Sie die BitLocker-Laufwerkverschlüsselung verwalten können.

-   Bevor Sie MBAM ausführen, müssen Sie die Gruppenrichtlinienvorlagen herunterladen, indem Sie [MDOP Gruppenrichtlinien (ADMX)-Vorlagen abrufen](https://go.microsoft.com/fwlink/p/?LinkId=393941) und auf einen Server oder eine Workstation kopieren, auf dem ein unterstütztes Windows-Server-oder Windows-Betriebssystem ausgeführt wird.

    **HINWEIS**<br>Die Workstation muss kein dedizierter Computer sein.

     

### MBAM-Client und Configuration Manager-Clientcomputer

#### MBAM-Client Software

Der **MBAM-Client**:

-   Verwendet Gruppenrichtlinienobjekte, um die BitLocker-Laufwerkverschlüsselung auf Clientcomputern im Unternehmen durchzusetzen.

-   Sammelt den BitLocker-Wiederherstellungsschlüssel für drei Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und Wechseldatenträger (USB)-Datenlaufwerke.

-   Sammelt Wiederherstellungsinformationen und Computer Informationen zu den Clientcomputern.

#### Konfigurations-Manager – Client

Der **Configuration Manager-Client** ermöglicht es Configuration Manager, Hardware Kompatibilitätsdaten zu den Client Computern zu sammeln und Kompatibilitätsinformationen zu melden.

 

## Unterschiede in MBAM-Bereitstellung für unterstützte Configuration Manager-Versionen


Wenn Sie MBAM mit der Configuration Manager-Integrations Topologie bereitstellen, können Sie MBAM auf einem primären Standortserver installieren. Die MBAM-Installation funktioniert jedoch anders für den System Center2012-Konfigurations-Manager und die Konfigurations Manager2007.

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
<td align="left"><p>System Center2012 R2-Konfigurations-Manager</p>
<p>System Center2012-Konfigurations-Manager</p></td>
<td align="left"><p>Wenn Sie MBAM auf einem primären Standortserver oder auf einem zentralen Administrationsserver installieren, führt MBAM alle Installationsaktionen auf diesem Website Server aus.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurations-Manager2007 R2</p>
<p>Konfigurations Manager2007</p></td>
<td align="left"><p>Wenn Sie MBAM auf einem primären Standortserver installieren, der Teil einer größeren Configuration Manager-Hierarchie mit einem zentralen Standort übergeordneten Server ist, identifiziert MBAM den übergeordneten zentralen Standortserver und führt alle Installationsaktionen auf dem übergeordneten Server aus. Die Installation umfasst das Überprüfen von Voraussetzungen und das Installieren der Configuration Manager-Objekte und-Berichte.</p>
<p>Wenn Sie beispielsweise MBAM auf einem primären Standortserver installieren, der ein untergeordnetes Element eines übergeordneten zentralen Standortservers ist, installiert MBAM alle Configuration Manager-Objekte und-Berichte auf dem übergeordneten Server. Wenn Sie MBAM auf dem übergeordneten Server installieren, führt MBAM alle Installationsaktionen auf dem übergeordneten Server aus.</p></td>
</tr>
</tbody>
</table>

 

## Funktionsweise von MBAM mit Configuration Manager


Die Integration von MBAM mit Configuration Manager basiert auf einem Konfigurationspaket, mit dem die in der folgenden Tabelle beschriebenen Elemente installiert werden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemente, die in Configuration Manager installiert sind</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Konfigurationsdaten</p></td>
<td align="left"><p>Die Konfigurationsdaten installieren eine Konfigurationsbasislinie mit dem Namen "BitLocker-Schutz", die zwei Konfigurationselemente enthält:</p>
<ul>
<li><p>BitLocker-Betriebs System-Laufwerkschutz</p></li>
<li><p>BitLocker-Datenlaufwerke mit fester Datensicherheit</p></li>
</ul>
<p>Die Konfigurationsbasislinie wird in der MBAM-unterstützten Computersammlung bereitgestellt, die auch bei der Installation von MBAM erstellt wird.</p>
<p>Die beiden Konfigurationselemente stellen die Grundlage für die Auswertung des Kompatibilitätsstatus der Clientcomputer dar. Diese Informationen werden in Configuration Manager erfasst, gespeichert und ausgewertet.</p>
<p>Die Konfigurationselemente basieren auf den Compliance-Anforderungen für Betriebssystemlaufwerke und fest Netzlaufwerke. Die erforderlichen Details für die bereitgestellten Computer werden erfasst, damit die Kompatibilität dieser Laufwerktypen ausgewertet werden kann.</p>
<p>Standardmäßig wertet die Konfigurationsbasislinie den Kompatibilitätsstatus every12 Stunden aus und sendet die Kompatibilitätsdaten an Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM-unterstützte Computersammlung</p></td>
<td align="left"><p>MBAM erstellt eine Sammlung, die als MBAM unterstützte Computer bezeichnet wird. Die Konfigurationsbasislinie richtet sich an Clientcomputer, die in dieser Sammlung enthalten sind.</p>
<p>Hierbei handelt es sich um eine dynamische Sammlung. Standardmäßig wird every12 Stunden ausgeführt, und die Mitgliedschaft wird anhand von drei Kriterien ausgewertet:</p>
<ul>
<li><p>Der Computer ist eine unterstützte Version des Windows-Betriebssystems.</p></li>
<li><p>Der Computer ist ein physikalischer Computer. Virtuelle Computer werden nicht unterstützt.</p></li>
<li><p>Der Computer verfügt über ein Trusted Platform Module (TPM), das verfügbar ist. Eine kompatible Version von TPM 1.2 oder höher ist für Windows7 erforderlich. Für Windows10, Windows 8.1, Windows8 und Windows to go ist kein TPM erforderlich.</p></li>
</ul>
<p>Die Sammlung wird für alle Computer ausgewertet, und es wird eine Teilmenge der kompatiblen Computer erstellt, die die Grundlage für die Kompatibilitäts Auswertung und-Berichterstellung für die MBAM-Integration bildet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Berichte</p></td>
<td align="left"><p>Wenn Sie MBAM mit der Configuration Manager-Integrations Topologie konfigurieren, werden alle Berichte in Configuration Manager mit Ausnahme des Wiederherstellungs Überwachungsberichts angezeigt, von dem Sie auf der Website für die MBAM-Verwaltung und-Überwachung weiterhin angezeigt werden. Die in Configuration Manager verfügbaren Berichte lauten wie folgt:</p>
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
<td align="left"><p>Bietet IT-Administratoren drei Ansichten von Informationen in einem einzigen Bericht: Kompatibilitätsstatus Verteilung, nicht kompatibel – Fehlerverteilung und Kompatibilitätsstatus Verteilung nach Laufwerks. Mit den Drilldown-Optionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem ausgewählten Zustand entsprechen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Details zur BitLocker-Unternehmenskonformität</p></td>
<td align="left"><p>Ermöglicht IT-Administratoren die Anzeige von Informationen über den BitLocker-Verschlüsselungs Kompatibilitätsstatus des Unternehmens und umfasst den Kompatibilitätsstatus für jeden Computer. Mit den Drilldown-Optionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem ausgewählten Zustand entsprechen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker-Computer Konformität</p></td>
<td align="left"><p>Ermöglicht es Administratoren, einen einzelnen Computer anzuzeigen und zu ermitteln, warum er mit dem Status "kompatibel" oder "nicht kompatibel" gemeldet wurde. Der Bericht zeigt auch den Verschlüsselungsstatus der Betriebssystemlaufwerke und fest Netzlaufwerke an.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Zusammenfassung der BitLocker-Unternehmenskonformität</p></td>
<td align="left"><p>Damit können IT-Administratoren den Status der MBAM-Richtlinienkonformität im Unternehmen anzeigen. Der Status jedes Computers wird ausgewertet, und der Bericht zeigt eine Zusammenfassung der Konformität aller Computer im Unternehmen mit der Richtlinie. Mit den Drilldown-Optionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem ausgewählten Zustand entsprechen.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## Verwandte Themen


[Erste Schritte mit MBAM 2.5](getting-started-with-mbam-25.md)

[High-Level-Architektur von MBAM 2.5 mit eigenständiger Topologie](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[Beschreibung der Funktionen einer MBAM 2.5-Bereitstellung](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




