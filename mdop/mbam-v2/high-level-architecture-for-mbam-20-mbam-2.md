---
title: High-Level-Architektur für MBAM 2.0
description: High-Level-Architektur für MBAM 2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19480b5797362e6e4119fff9a14afd9d5a74d98
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910500"
---
# <a name="high-level-architecture-for-mbam-20"></a>High-Level-Architektur für MBAM 2.0


Microsoft BitLocker Administration and Monitoring (MBAM) ist eine Client-/Serverlösung, die Ihnen dabei helfen kann, die BitLocker-Bereitstellung und -Bereitstellung zu vereinfachen, die Compliance und Berichterstellung auf BitLocker zu verbessern und Supportkosten zu senken. Die Verwaltung und Überwachung von Microsoft BitLocker umfasst die in diesem Thema beschriebenen Features.

Die Verwaltung und Überwachung von Microsoft BitLocker kann in der eigenständigen Topologie oder in einer Topologie bereitgestellt werden, die in Microsoft System Center Configuration Manager 2007 oder Microsoft System Center 2012 Configuration Manager integriert ist. In diesem Thema wird die Architektur für die eigenständige Topologie beschrieben. Informationen zur Bereitstellung in der integrierten Configuration Manager-Topologie finden Sie unter [Verwenden von MBAM mit Configuration Manager.](using-mbam-with-configuration-manager.md)

Das folgende Diagramm zeigt die empfohlene MBAM-Architektur für eine Produktionsumgebung, die aus zwei Servern und einer Verwaltungsarbeitsstation besteht. Diese Architektur unterstützt bis zu 200.000 MBAM-Clients. Die Serverfeatures und Datenbanken im Architekturimage werden im folgenden Abschnitt beschrieben und unter dem Computer oder Server aufgeführt, auf dem sie installiert werden sollten.

**Hinweis:**  
Eine Architektur mit einem einzelnen Server sollte nur in Testumgebungen verwendet werden.

 

![Zweiserver-Bereitstellungstopologie von mbam 2.](images/mbam2-3-servers.gif)

## <a name="administration-and-monitoring-server"></a>Verwaltungs- und Überwachungsserver


Die folgenden Features werden auf diesem Server installiert:

-   **Administration and Monitoring Server**. Das Feature "Verwaltungs- und Überwachungsserver" wird auf einem Windows Server installiert und besteht aus der Verwaltungs- und Überwachungswebsite, die die Berichte und das Helpdesk-Portal sowie die Überwachungswebdienste enthält.

-   **Self-Service Portal**. Das Self-Service-Portal wird auf einem Windows Server installiert. Das Self-Service-Portal ermöglicht Endbenutzern auf Clientcomputern die unabhängige Anmeldung bei einer Website, auf der sie einen Wiederherstellungsschlüssel erhalten können, um ein gesperrtes BitLocker-Volume wiederherzustellen.

## <a name="database-server"></a>Datenbankserver


Die folgenden Features werden auf diesem Server installiert:

-   **Wiederherstellungsdatenbank**. Die Wiederherstellungsdatenbank wird auf einem Windows Server und einer unterstützten Instanz von Microsoft SQL Server installiert. Diese Datenbank speichert Wiederherstellungsdaten, die von MBAM-Clientcomputern gesammelt werden.

-   **Compliance- und Überwachungsdatenbank**. Die Konformitäts- und Überwachungsdatenbank wird auf einem Windows Server und einer unterstützten Instanz von SQL Server installiert. In dieser Datenbank werden Kompatibilitätsdaten für MBAM-Clientcomputer gespeichert. Diese Daten werden in erster Linie für Berichte verwendet, die SSRS-Hosts (SQL Server Reporting Services).

-   **Compliance- und Überwachungsberichte**. Die Konformitäts- und Überwachungsberichte werden auf einem Windows Server und einer unterstützten Instanz von SQL Server installiert, auf dem das Feature SQL Server Reporting Services (SSRS) installiert ist. Diese Berichte stellen MBAM-Berichte bereit, auf die Sie über die Verwaltungs- und Überwachungswebsite oder direkt über den SSRS-Server zugreifen können.

## <a name="management-workstation"></a>Verwaltungsarbeitsstation


Das folgende Feature ist auf der Verwaltungsarbeitsstation installiert, bei der es sich um einen Windows-Server oder einen Clientcomputer handelt.

-   **Richtlinienvorlage**. Die Richtlinienvorlage besteht aus Gruppenrichtlinieneinstellungen, die MBAM-Implementierungseinstellungen für die BitLocker-Laufwerkverschlüsselung definieren. Sie können die Richtlinienvorlage auf einem beliebigen Server oder jeder Arbeitsstation installieren, sie wird jedoch häufig auf einer Verwaltungsarbeitsstation installiert, bei der es sich um einen unterstützten Windows Server- oder Clientcomputer handelt. Die Arbeitsstation muss kein dedizierter Computer sein.

## <a name="mbam-client"></a><a href="" id="---------mbam-client"></a> MBAM-Client


Der MBAM-Client wird auf einem Windows Computer installiert und weist die folgenden Merkmale auf:

-   Verwendet Gruppenrichtlinien, um die BitLocker-Laufwerkverschlüsselung von Clientcomputern im Unternehmen zu erzwingen.

-   Erfasst den Wiederherstellungsschlüssel für die drei BitLocker-Datentypen: Betriebssystemlaufwerke, Festplattenlaufwerke und USB-Laufwerke (Wechseldaten).

-   Sammelt Compliancedaten für den Computer und übergibt die Daten an das Berichterstellungssystem.

## <a name="related-topics"></a>Verwandte Themen


[Erste Schritte mit MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





