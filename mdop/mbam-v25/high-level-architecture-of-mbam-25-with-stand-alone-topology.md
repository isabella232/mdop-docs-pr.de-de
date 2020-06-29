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
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811827"
---
# High-Level-Architektur von MBAM 2.5 mit eigenständiger Topologie


In diesem Thema wird die empfohlene Architektur für die Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der eigenständigen Configuration Manager-Topologie beschrieben. In dieser Topologie wird MBAM als eigenständiges Produkt bereitgestellt. Sie können MBAM auch mit der Configuration Manager-Integrations Topologie bereitstellen, die MBAM mit Configuration Manager integriert. Weitere Informationen finden Sie unter [Architektur auf höherer Ebene in MBAM 2,5 mit der Configuration Manager-Integrations Topologie](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).

Eine Liste der unterstützten Versionen der in diesem Thema erwähnten Software finden Sie unter [unterstützte MBAM 2,5-Konfigurationen](mbam-25-supported-configurations.md).

**Hinweis**  Wir empfehlen, nur in Testumgebungen eine Architektur mit einem Server zu verwenden.

 

## Empfohlene Anzahl von Servern und unterstützte Anzahl von Clients


Die empfohlene Anzahl von Servern und unterstützten Clients in einer Produktionsumgebung lautet wie folgt:

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
<p>Eine Workstation</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anzahl der unterstützten Clientcomputer</p></td>
<td align="left"><p>500.000</p></td>
</tr>
</tbody>
</table>

 

## Empfohlene MBAM-Architektur auf höherer Ebene mit der eigenständigen Topologie


Das folgende Diagramm und die folgende Tabelle beschreiben die empfohlene Architektur für zwei Server auf hoher Ebene für MBAM mit der eigenständigen Topologie. MBAM Multi-Forest-Bereitstellungen erfordern eine unidirektionale oder bidirektionale Vertrauensstellung. Unidirektionale Vertrauensstellungen setzen voraus, dass die Server Domäne der Clientdomäne vertraut.

![mbam2](images/mbam2-5-2servers.png)

Server Features zum Konfigurieren auf diesem Server Beschreibungsdaten Bankserver

Konformitäts-und Überwachungsdatenbank

Dieses Feature ist auf einem Server konfiguriert, auf dem Windows Server ausgeführt wird, und die SQL Server-Instanz unterstützt.

Die **Compliance-und Überwachungsdatenbank** speichert Kompatibilitätsdaten, die hauptsächlich für Berichte verwendet werden, die von SQL Server Reporting Services gehostet werden.

Wiederherstellungsdatenbank

Dieses Feature ist auf einem Server konfiguriert, auf dem Windows Server ausgeführt wird, und die SQL Server-Instanz unterstützt.

Die **Wiederherstellungsdatenbank** speichert Wiederherstellungsdaten, die von MBAM-Clientcomputern erfasst werden.

Berichte

Dieses Feature ist auf einem Server konfiguriert, auf dem Windows Server ausgeführt wird, und die SQL Server-Instanz unterstützt.

In den **Berichten** werden Wiederherstellungs Überwachungs-und Kompatibilitätsstatus Daten zu den Clientcomputern in Ihrem Unternehmen bereitgestellt. Sie können auf die Berichte über die Website Verwaltung und Überwachung oder direkt in SQL Server Reporting Services zugreifen.

Verwaltungs-und Überwachungs Server

Website "Verwaltung und Überwachung"

Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.

Die **Website Verwaltung und Überwachung** wird verwendet, um Folgendes zu tun:

-   Helfen Sie den Endbenutzern beim wieder Zugriff auf Ihre Computer, wenn Sie gesperrt sind. (Dieser Bereich der Website wird im Allgemeinen als Help Desk bezeichnet.)

-   Anzeigen von Berichten, die den Kompatibilitätsstatus und die Wiederherstellungs Aktivität für Clientcomputer anzeigen

Self-Service-Portal

Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.

Das **Self-Service-Portal** ist eine Website, auf der sich Endbenutzer auf Clientcomputern selbstständig an einer Website anmelden können, um einen Wiederherstellungsschlüssel abzurufen, wenn Sie Ihr BitLocker-Kennwort verlieren oder vergessen.

Überwachen von Webdiensten für diese Website

Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.

Die **Überwachungs-Webdienste** werden vom MBAM-Client und den Websites verwendet, um mit der Datenbank zu kommunizieren.

**Wichtig**  Der Monitoring Web Service steht in der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 nicht mehr zur Verfügung, da die MBAM-Websites direkt mit der Wiederherstellungsdatenbank kommunizieren.

 

Verwaltungsarbeitsstation

MBAM-Gruppenrichtlinienvorlagen

-   Bei den MBAM-Gruppenrichtlinienvorlagen handelt es sich um Gruppenrichtlinieneinstellungen, die Implementierungs Einstellungen für MBAM definieren, mit denen Sie die BitLocker-Laufwerkverschlüsselung verwalten können.

-   Bevor Sie MBAM ausführen, müssen Sie die Gruppenrichtlinienvorlagen herunterladen, indem Sie [MDOP Gruppenrichtlinien (ADMX)-Vorlagen abrufen](https://go.microsoft.com/fwlink/p/?LinkId=393941) und auf einen Server oder eine Workstation kopieren, auf dem ein unterstütztes Windows-Server-oder Windows-Betriebssystem ausgeführt wird.

-   Die Workstation muss kein dedizierter Computer sein.

MBAM-Client und Configuration Manager-Clientcomputer

MBAM-Client Software

Der MBAM-Client:

-   Verwendet Gruppenrichtlinienobjekte, um die BitLocker-Laufwerkverschlüsselung auf Clientcomputern im Unternehmen durchzusetzen.

-   Sammelt den BitLocker-Wiederherstellungsschlüssel für drei Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und Wechseldatenträger (USB)-Datenlaufwerke.

-   Sammelt Wiederherstellungsinformationen und Computer Informationen zu den Clientcomputern.



## Verwandte Themen


[Erste Schritte mit MBAM 2.5](getting-started-with-mbam-25.md)

[High-Level-Architektur von MBAM 2.5 mit Configuration Manager-Integrationstopologie](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[Beschreibung der Funktionen einer MBAM 2.5-Bereitstellung](illustrated-features-of-an-mbam-25-deployment.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





