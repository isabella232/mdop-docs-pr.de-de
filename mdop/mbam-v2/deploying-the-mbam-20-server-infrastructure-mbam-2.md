---
title: Bereitstellen der Serverinfrastruktur von MBAM 2.0
description: Bereitstellen der Serverinfrastruktur von MBAM 2.0
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8aee322b9a1aacbf98ff8362e95e21c2dd3d289a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910800"
---
# <a name="deploying-the-mbam-20-server-infrastructure"></a>Bereitstellen der Serverinfrastruktur von MBAM 2.0


Microsoft BitLocker Administration and Monitoring (MBAM)-Serverfeatures für die eigenständige Topologie können in unterschiedlichen Konfigurationen auf zwei oder mehr Servern in einer Produktionsumgebung installiert werden. Die empfohlene Konfiguration besteht aus zwei Servern für eine Produktionsumgebung, je nach Ihren Skalierbarkeitsanforderungen. Verwenden Sie einen einzelnen Server für eine MBAM-Installation nur in Testumgebungen. Weitere Informationen zur Planung der MBAM Server-Featurebereitstellung finden Sie unter [Planning for MBAM 2.0 Server Deployment.](planning-for-mbam-20-server-deployment-mbam-2.md)

Das folgende Diagramm zeigt ein Beispiel dafür, wie Sie die empfohlene Zwei-Server-MBAM-Bereitstellung konfigurieren können. Diese Konfiguration unterstützt bis zu 200.000 MBAM-Clients in einer Produktionsumgebung. Die Serverfeatures und Datenbanken im Architekturimage werden im folgenden Abschnitt beschrieben und unter dem Computer oder Server aufgeführt, auf dem sie installiert werden sollten.

![Zweiserver-Bereitstellungstopologie von mbam 2.](images/mbam2-3-servers.gif)

## <a name="administration-and-monitoring-server"></a>Verwaltungs- und Überwachungsserver


Die folgenden Features werden auf diesem Server installiert:

-   **Administration and Monitoring Server**. Das Feature "Verwaltungs- und Überwachungsserver" wird auf einem Windows Server installiert und besteht aus der Helpdesk-Website und den Überwachungswebdiensten.

-   **Self-Service Portal**. Das Self-Service-Portal wird auf einem Windows Server installiert. Das Self-Service-Portal ermöglicht Endbenutzern auf Clientcomputern die unabhängige Anmeldung bei einer Website, auf der sie einen Wiederherstellungsschlüssel erhalten können, um ein gesperrtes BitLocker-Volume wiederherzustellen.

## <a name="database-server"></a>Datenbankserver


Die folgenden Features werden auf diesem Server installiert:

-   **Wiederherstellungsdatenbank**. Die Wiederherstellungsdatenbank wird auf einem Windows Server und einer unterstützten Instanz von Microsoft SQL Server installiert. Diese Datenbank speichert Wiederherstellungsdaten, die von MBAM-Clientcomputern gesammelt werden.

-   **Compliance- und Überwachungsdatenbank**. Die Konformitäts- und Überwachungsdatenbank wird auf einem Windows Server und einer unterstützten Instanz von SQL Server installiert. In dieser Datenbank werden Kompatibilitätsdaten für MBAM-Clientcomputer gespeichert. Diese Daten werden in erster Linie für Berichte verwendet, die SSRS-Hosts (SQL Server Reporting Services).

-   **Compliance- und Überwachungsberichte**. Die Konformitäts- und Überwachungsberichte werden auf einem Windows Server und einer unterstützten Instanz von SQL Server installiert, auf dem das Feature SQL Server Reporting Services (SSRS) installiert ist. Diese Berichte stellen MBAM-Berichte bereit, auf die Sie über die Helpdesk-Website oder direkt vom SSRS-Server aus zugreifen können.

## <a name="management-workstation"></a>Verwaltungsarbeitsstation


Das folgende Feature ist auf der Verwaltungsarbeitsstation installiert, bei der es sich um einen Windows-Server oder einen Clientcomputer handelt.

-   **Richtlinienvorlage**. Die Richtlinienvorlage besteht aus Gruppenrichtlinien, die MBAM-Implementierungseinstellungen für die BitLocker-Laufwerkverschlüsselung definieren. Sie können die Richtlinienvorlage auf einem beliebigen Server oder jeder Arbeitsstation installieren, sie wird jedoch häufig auf einer Verwaltungsarbeitsstation installiert, bei der es sich um einen unterstützten Windows Server- oder Clientcomputer handelt. Die Arbeitsstation muss kein dedizierter Computer sein.

## <a name="mbam-client"></a><a href="" id="---------mbam-client"></a> MBAM-Client


Der MBAM-Client wird auf einem Windows Computer installiert und weist die folgenden Merkmale auf:

-   Verwendet Gruppenrichtlinien, um die BitLocker-Laufwerkverschlüsselung von Clientcomputern im Unternehmen zu erzwingen.

-   Erfasst den Wiederherstellungsschlüssel für die drei BitLocker-Datentypen: Betriebssystemlaufwerke, Festplattenlaufwerke und USB-Laufwerke (Wechseldaten).

-   Sammelt Compliancedaten für den Computer und übergibt die Daten an das Berichterstellungssystem.

## <a name="other-resources-for-deploying-mbam-20-server-features"></a>Weitere Ressourcen für die Bereitstellung von MBAM 2.0-Serverfeatures


[Bereitstellen von MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





