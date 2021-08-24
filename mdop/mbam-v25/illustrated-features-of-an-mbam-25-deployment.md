---
title: Beschreibung der Funktionen einer MBAM 2.5-Bereitstellung
description: Beschreibung der Funktionen einer MBAM 2.5-Bereitstellung
author: dansimp
ms.assetid: 7b5eff42-af8c-4bd0-a20a-18cc2e779f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 139980fb6712b40685a41bab45610da670803afa
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910620"
---
# <a name="illustrated-features-of-an-mbam-25-deployment"></a>Beschreibung der Funktionen einer MBAM 2.5-Bereitstellung


In diesem Thema werden die einzelnen Features beschrieben, die eine Microsoft BitLocker Administration and Monitoring (MBAM) 2.5-Bereitstellung für die folgenden Topologien bilden:

-   EIGENSTÄNDIGES MBAM

-   System Center Configuration Manager Integration

**Wichtig**  
Diese Features stellen nicht die empfohlene Architektur für die Bereitstellung von MBAM dar. Verwenden Sie diese Informationen nur als Leitfaden, um die einzelnen Features einer MBAM-Bereitstellung zu verstehen. Die empfohlene Architektur für MBAM finden Sie [unter "Allgemeine Architektur für MBAM 2.5".](high-level-architecture-for-mbam-25.md)



Eine Liste der unterstützten Versionen der in diesem Thema erwähnten Software finden Sie unter ["Unterstützte Konfigurationen für MBAM 2.5".](mbam-25-supported-configurations.md)

## <a name="mbam-stand-alone-topology"></a><a href="" id="bkmk-standalone"></a> Eigenständige MBAM-Topologie


In der folgenden Abbildung und Tabelle werden die Features in einer eigenständigen MBAM-Topologie erläutert.

![mbab2\-5.](images/mbam2-5-standalonecomponents.png)

|Featuretyp|Beschreibung|Datenbank|
|-|-|-|
|Wiederherstellungsdatenbank|Diese Datenbank speichert Wiederherstellungsdaten, die von MBAM-Clientcomputern gesammelt werden.|Dieses Feature ist auf einem Server mit Windows Server und einer unterstützten SQL Server Instanz konfiguriert.|
|Compliance- und Überwachungsdatenbank|Diese Datenbank speichert Compliancedaten, die in erster Linie für die Berichte verwendet werden, die SQL Server Reporting Services Hosts.|Dieses Feature ist auf einem Server mit Windows Server und einer unterstützten SQL Server Instanz konfiguriert.|
|Compliance- und Überwachungsberichte|||
|Reporting Web Service|Dieser Webdienst ermöglicht die Kommunikation zwischen der Verwaltungs- und Überwachungswebsite und der SQL Server Instanz, in der Berichtsdaten gespeichert sind.|Dieses Feature wird auf einem Server installiert, auf dem Windows Server ausgeführt wird.|
|Berichtswebsite (Verwaltungs- und Überwachungswebsite)|Sie können Berichte von der Verwaltungs- und Überwachungswebsite anzeigen. Die Berichte enthalten Wiederherstellungsüberwachungs- und Compliancestatusdaten zu den Clientcomputern in Ihrem Unternehmen.|Dieses Feature ist auf einem Server konfiguriert, auf dem Windows Server ausgeführt wird.|
|SQL Server Reporting Services (SSRS)|Berichte werden in einer SSRS-Datenbankinstanz konfiguriert. Berichte können direkt über SSRS oder über die Verwaltungs- und Überwachungswebsite angezeigt werden.|Dieses Feature ist auf einem Server mit Windows Server und einer unterstützten SQL Server Instanz mit SSRS konfiguriert.|
|Self-Service Server|||
|Self-Service-Webdienst|Dieser Webdienst wird vom MBAM-Client und der Verwaltungs- und Überwachungswebsite und Self-Service-Portal für die Kommunikation mit der Wiederherstellungsdatenbank verwendet.|Dieses Feature wird auf einem Computer installiert, auf dem Windows Server ausgeführt wird.|
|Self-Service-Website (Self-Service-Portal)|Diese Website ermöglicht Endbenutzern auf Clientcomputern die unabhängige Anmeldung bei einer Website, um einen Wiederherstellungsschlüssel zu erhalten, wenn sie ihr BitLocker-Kennwort verlieren oder vergessen.|Dieses Feature wird auf einem Computer konfiguriert, auf dem Windows Server ausgeführt wird.|
|Verwaltungs- und Überwachungsserver|||
|Verwaltungs- und Überwachungswebdienst|Der Überwachungswebdienst wird vom MBAM-Client und den Websites für die Kommunikation mit den Datenbanken verwendet.|Dieses Feature wird auf einem Computer installiert, auf dem Windows Server ausgeführt wird.|

**Wichtig**  
Der Self-Service Webdienst ist nicht mehr in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 verfügbar, in dem der MBAM-Client, die Verwaltungs- und Überwachungswebsite und das Self-Service-Portal direkt mit der Wiederherstellungsdatenbank kommunizieren.

**Wichtig**  
Der Überwachungswebdienst ist in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 nicht mehr verfügbar, da der MBAM-Client und die Websites direkt mit der Wiederherstellungsdatenbank kommunizieren.


## <a name="system-center-configuration-manager-integration-topology"></a><a href="" id="bkmk-cmintegrated"></a>System Center Configuration Manager Integrationstopologie

In der folgenden Abbildung und Tabelle werden die Features in der System Center Configuration Manager-Integrationstopologie erläutert.

![mbam2\-5.](images/mbam2-5-cmcomponents.png)

**Wichtig**  
Der Self-Service Webdienst ist nicht mehr in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 verfügbar, in dem der MBAM-Client, die Verwaltungs- und Überwachungswebsite und das Self-Service-Portal direkt mit der Wiederherstellungsdatenbank kommunizieren.

**Warnung**  
Der Überwachungswebdienst ist in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 nicht mehr verfügbar, da der MBAM-Client und die Websites direkt mit der Wiederherstellungsdatenbank kommunizieren.


|                        Featuretyp                        |                                                                                                    Beschreibung                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    Self-Service Server                     |                                                                                                                                                                                                                   |
|                  Self-Service-Webdienst                  |                                                 Dieser Webdienst wird vom MBAM-Client und dem Self-Service-Portal für die Kommunikation mit der Wiederherstellungsdatenbank verwendet.                                                  |
|                    Self-Service-Website                    |                          Diese Website ermöglicht Endbenutzern auf Clientcomputern die unabhängige Anmeldung bei einer Website, um einen Wiederherstellungsschlüssel zu erhalten, wenn sie ihr BitLocker-Kennwort verlieren oder vergessen.                          |
| Verwaltungs- und Überwachungsserver/Wiederherstellungsüberwachungsbericht |                                                                                                                                                                                                                   |
|         Verwaltungs- und Überwachungswebdienst          |                               Dieser Webdienst ermöglicht die Kommunikation zwischen der Verwaltungs- und Überwachungswebsite und den SQL Server Datenbanken, in denen Berichtsdaten gespeichert sind.                               |
|           Verwaltungs- und Überwachungswebsite            | Der Wiederherstellungsüberwachungsbericht wird auf der Verwaltungs- und Überwachungswebsite angezeigt. Verwenden Sie die Configuration Manager-Konsole, um alle anderen Berichte oder Berichte direkt aus SQL Server Reporting Services anzuzeigen. |
|                         Datenbanken                          |                                                                                                                                                                                                                   |
|                     Wiederherstellungsdatenbank                      |                                                                 Diese Datenbank speichert Wiederherstellungsdaten, die von MBAM-Clientcomputern gesammelt werden.                                                                  |
|                       Überwachungsdatenbank                       |                                                                   Diese Datenbank speichert Überwachungsinformationen zu Wiederherstellungsversuchen und -aktivitäten.                                                                    |
|               Configuration Manager-Features               |                                                                                                                                                                                                                   |
|          Configuration Manager-Verwaltungskonsole          |                                                                   Diese Konsole ist in Configuration Manager integriert und wird zum Anzeigen von Berichten verwendet.                                                                   |
|               Configuration Manager-Berichte                |                                                             Berichte zeigen Compliance- und Wiederherstellungsüberwachungsdaten für Clientcomputer in Ihrem Unternehmen an.                                                              |
|               SQL Server Reporting Services                |                                                SSRS aktiviert die MBAM-Berichte. Berichte können direkt über SSRS oder über die Configuration Manager-Konsole angezeigt werden.                                                 |

## <a name="related-topics"></a>Verwandte Themen

[High-Level-Architektur für MBAM 2.5](high-level-architecture-for-mbam-25.md)

[Erste Schritte mit MBAM 2.5](getting-started-with-mbam-25.md)

## <a name="got-a-suggestion-for-mbam"></a>Haben Sie einen Vorschlag für MBAM?
- Hier können Sie [Vorschläge](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)hinzufügen oder abstimmen. 
- Verwenden Sie für MBAM-Probleme das [MBAM TechNet-Forum.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)




