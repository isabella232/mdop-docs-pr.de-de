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
ms.openlocfilehash: c3b205d4f0b4b18cf8bdbf51982b5a59e5e1b9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804196"
---
# Beschreibung der Funktionen einer MBAM 2.5-Bereitstellung


In diesem Thema werden die einzelnen Features beschrieben, aus denen eine Microsoft BitLocker-MBAM-2,5-Bereitstellung für die folgenden Topologien besteht:

-   MBAM eigenständig

-   Integration von System Center Configuration Manager

**Wichtig**  
Diese Features stellen nicht die empfohlene Architektur für die Bereitstellung von MBAM dar. Verwenden Sie diese Informationen nur als Leitfaden, um die einzelnen Features zu verstehen, die eine MBAM-Bereitstellung ausmachen. Die empfohlene Architektur für MBAM finden Sie unter [allgemeine Architektur für MBAM 2,5](high-level-architecture-for-mbam-25.md) .



Eine Liste der unterstützten Versionen der in diesem Thema erwähnten Software finden Sie unter [unterstützte MBAM 2,5-Konfigurationen](mbam-25-supported-configurations.md).

## <a href="" id="bkmk-standalone"></a> MBAM eigenständige Topologie


In der folgenden Abbildung und Tabelle werden die Features in einer eigenständigen MBAM-Topologie erläutert.

![mbab2\-5](images/mbam2-5-standalonecomponents.png)

|Feature-Typ|Beschreibung|Datenbank|
|-|-|-|
|Wiederherstellungsdatenbank|In dieser Datenbank werden Wiederherstellungsdaten gespeichert, die von MBAM-Clientcomputern erfasst werden.|Dieses Feature ist auf einem Server, auf dem Windows Server ausgeführt wird, und einer unterstützten SQL Server-Instanz konfiguriert.|
|Konformitäts-und Überwachungsdatenbank|In dieser Datenbank werden Kompatibilitätsdaten gespeichert, die hauptsächlich für die Berichte verwendet werden, die von SQL Server Reporting Services gehostet werden.|Dieses Feature ist auf einem Server, auf dem Windows Server ausgeführt wird, und einer unterstützten SQL Server-Instanz konfiguriert.|
|Konformitäts-und Überwachungsberichte|||
|Reporting Web Service|Dieser Webdienst ermöglicht die Kommunikation zwischen der Verwaltungs-und Überwachungs Website und der SQL Server-Instanz, in der die Berichtsdaten gespeichert werden.|Dieses Feature ist auf einem Server installiert, auf dem Windows Server ausgeführt wird.|
|Berichterstellungswebsite (Website "Verwaltung und Überwachung")|Sie können Berichte auf der Website Verwaltung und Überwachung anzeigen. In den Berichten werden Wiederherstellungs Überwachungs-und Kompatibilitätsstatus Daten zu den Clientcomputern in Ihrem Unternehmen bereitgestellt.|Dieses Feature ist auf einem Server konfiguriert, auf dem Windows Server ausgeführt wird.|
|SQL Server Reporting Services (SSRS)|Berichte werden in einer SSRS-Datenbankinstanz konfiguriert. Berichte können direkt in SSRS oder auf der Website Verwaltung und Überwachung angezeigt werden.|Dieses Feature ist auf einem Server mit Windows Server und einer unterstützten SQL Server-Instanz konfiguriert, die SSRS ausführt.|
|Self-Service-Server|||
|Self-Service Web Service|Dieser Webdienst wird vom MBAM-Client und der Website für Verwaltung und Überwachung sowie Self-Service-Portal verwendet, um mit der Wiederherstellungsdatenbank zu kommunizieren.|Dieses Feature ist auf einem Computer mit Windows Server installiert.|
|Self-Service-Website (Self-Service-Portal)|Diese Website ermöglicht es Endbenutzern auf Clientcomputern, sich selbständig bei einer Website anzumelden, um einen Wiederherstellungsschlüssel zu erhalten, wenn Sie Ihr BitLocker-Kennwort verlieren oder vergessen.|Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.|
|Verwaltungs-und Überwachungs Server|||
|Web Service für Verwaltung und Überwachung|Der Monitoring Web Service wird vom MBAM-Client und den Websites für die Kommunikation mit den Datenbanken verwendet.|Dieses Feature ist auf einem Computer mit Windows Server installiert.|

**Wichtig**  
Der Self-Service-Webdienst steht in der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 nicht mehr zur Verfügung, in dem der MBAM-Client, die Verwaltungs-und Überwachungs Website sowie das Self-Service-Portal direkt mit der Wiederherstellungsdatenbank kommunizieren.

**Wichtig**  
Der Monitoring Web Service steht in der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 nicht mehr zur Verfügung, da der MBAM-Client und die Websites direkt mit der Wiederherstellungsdatenbank kommunizieren.


## <a href="" id="bkmk-cmintegrated"></a>System Center Configuration Manager-Integrations Topologie

In der folgenden Abbildung und Tabelle werden die Features in der System Center Configuration Manager-Integrations Topologie erläutert.

![mbam2\-5](images/mbam2-5-cmcomponents.png)

**Wichtig**  
Der Self-Service-Webdienst steht in der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 nicht mehr zur Verfügung, in dem der MBAM-Client, die Verwaltungs-und Überwachungs Website sowie das Self-Service-Portal direkt mit der Wiederherstellungsdatenbank kommunizieren.

**Warnung**  
Der Monitoring Web Service steht in der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 nicht mehr zur Verfügung, da der MBAM-Client und die Websites direkt mit der Wiederherstellungsdatenbank kommunizieren.


|                        Feature-Typ                        |                                                                                                    Beschreibung                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    Self-Service-Server                     |                                                                                                                                                                                                                   |
|                  Self-Service Web Service                  |                                                 Dieser Webdienst wird vom MBAM-Client und dem Self-Service-Portal verwendet, um mit der Wiederherstellungsdatenbank zu kommunizieren.                                                  |
|                    Self-Service-Website                    |                          Diese Website ermöglicht es Endbenutzern auf Clientcomputern, sich selbständig bei einer Website anzumelden, um einen Wiederherstellungsschlüssel zu erhalten, wenn Sie Ihr BitLocker-Kennwort verlieren oder vergessen.                          |
| Verwaltungs-und Überwachungsbericht für Server/Wiederherstellung |                                                                                                                                                                                                                   |
|         Web Service für Verwaltung und Überwachung          |                               Dieser Webdienst ermöglicht die Kommunikation zwischen der Verwaltungs-und Überwachungs Website und den SQL Server-Datenbanken, in denen Berichtsdaten gespeichert werden.                               |
|           Website "Verwaltung und Überwachung"            | Der Bericht zur Wiederherstellungsprüfung wird auf der Website Verwaltung und Überwachung angezeigt. Verwenden Sie die Configuration Manager-Konsole, um alle anderen Berichte anzuzeigen oder Berichte direkt in SQL Server Reporting Services anzuzeigen. |
|                         Datenbanken                          |                                                                                                                                                                                                                   |
|                     Wiederherstellungsdatenbank                      |                                                                 In dieser Datenbank werden Wiederherstellungsdaten gespeichert, die von MBAM-Clientcomputern erfasst werden.                                                                  |
|                       Überwachungsdatenbank                       |                                                                   In dieser Datenbank werden Überwachungsinformationen zu Wiederherstellungsversuchen und Aktivitäten gespeichert.                                                                    |
|               Configuration Manager-Features               |                                                                                                                                                                                                                   |
|          Configuration Manager-Verwaltungskonsole          |                                                                   Diese Konsole ist in Configuration Manager integriert und wird zum Anzeigen von Berichten verwendet.                                                                   |
|               Configuration Manager-Berichte                |                                                             Berichte zeigen Kompatibilitäts-und Wiederherstellungs Überwachungsdaten für Clientcomputer in Ihrem Unternehmen an.                                                              |
|               SQL Server Reporting Services                |                                                SSRS aktiviert die MBAM-Berichte. Berichte können direkt in SSRS oder in der Configuration Manager-Konsole angezeigt werden.                                                 |

## Verwandte Themen

[High-Level-Architektur für MBAM2.5](high-level-architecture-for-mbam-25.md)

[Erste Schritte mit MBAM 2.5](getting-started-with-mbam-25.md)

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




