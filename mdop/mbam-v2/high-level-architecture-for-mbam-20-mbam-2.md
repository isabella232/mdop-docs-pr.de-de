---
title: High-Level-Architektur für MBAM2.0
description: High-Level-Architektur für MBAM2.0
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
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810714"
---
# High-Level-Architektur für MBAM2.0


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ist eine Client/Server-Lösung, die Ihnen dabei helfen kann, die BitLocker-Bereitstellung und Bereitstellung zu vereinfachen, die Compliance und die Berichterstellung für BitLocker zu verbessern und die Supportkosten zu senken. Die Microsoft BitLocker-Verwaltung und-Überwachung umfasst die Features, die in diesem Thema beschrieben werden.

Die Microsoft BitLocker-Verwaltung und-Überwachung kann in der eigenständigen Topologie oder in einer Topologie bereitgestellt werden, die in Microsoft System Center Configuration Manager 2007 oder MicrosoftSystemCenter2012 ConfigurationManager integriert ist. In diesem Thema wird die Architektur für die eigenständige Topologie beschrieben. Informationen zum Bereitstellen in der integrierten Configuration Manager-Topologie finden Sie unter [Verwenden von MBAM mit Configuration Manager](using-mbam-with-configuration-manager.md).

Das folgende Diagramm zeigt die empfohlene MBAM-Architektur für eine Produktionsumgebung, die aus zwei Servern und einer Verwaltungsarbeitsstation besteht. Diese Architektur unterstützt bis zu 200.000 MBAM-Clients. Die Server Features und-Datenbanken im Architektur Bild werden im folgenden Abschnitt beschrieben und unter dem Computer oder Server aufgelistet, auf dem wir die Installation empfehlen.

**Hinweis**  Eine Architektur mit einem Server sollte nur in Testumgebungen verwendet werden.

 

![mbam 2 2-Server Bereitstellungstopologie](images/mbam2-3-servers.gif)

## Verwaltungs-und Überwachungs Server


Die folgenden Features sind auf diesem Server installiert:

-   **Verwaltungs-und Überwachungs Server**. Die Verwaltungs-und Überwachungs Server Funktion ist auf einem Windows-Server installiert und besteht aus der Websiteverwaltung und Überwachung, die die Berichte und das Helpdesk-Portal sowie die Überwachungs-Webdienste umfasst.

-   **Self-Service-Portal**. Das Self-Service-Portal ist auf einem Windows-Server installiert. Das Self-Service-Portal ermöglicht Endbenutzern auf Clientcomputern die unabhängige Anmeldung bei einer Website, auf der Sie einen Wiederherstellungsschlüssel zum Wiederherstellen eines gesperrten BitLocker-Volumes abrufen können.

## Daten Bank Server


Die folgenden Features sind auf diesem Server installiert:

-   **Wiederherstellungsdatenbank**. Die Wiederherstellungsdatenbank ist auf einem Windows-Server und einer unterstützten Instanz von Microsoft SQLServer installiert. In dieser Datenbank werden Wiederherstellungsdaten gespeichert, die von MBAM-Clientcomputern erfasst werden.

-   **Konformitäts-und Überwachungsdatenbank**. Die Compliance-und Überwachungsdatenbank ist auf einem Windows-Server und einer unterstützten Instanz von SQLServer installiert. In dieser Datenbank werden Kompatibilitätsdaten für MBAM-Clientcomputer gespeichert. Diese Daten werden hauptsächlich für Berichte verwendet, die von SQL Server Reporting Services (SSRS) gehostet werden.

-   **Konformitäts-und Überwachungsberichte**. Die Kompatibilitäts-und Überwachungsberichte sind auf einem Windows-Server und einer unterstützten Instanz von SQLServer installiert, auf der das Feature SQL Server Reporting Services (SSRS) installiert ist. Diese Berichte enthalten MBAM-Berichte, auf die Sie über die Websiteverwaltung und Überwachung oder direkt vom SSRS-Server aus zugreifen können.

## Verwaltungsarbeitsstation


Das folgende Feature ist auf der Verwaltungsarbeitsstation installiert, die ein Windows-Server oder ein Clientcomputer sein kann.

-   **Richtlinienvorlage**aus. Die Richtlinienvorlage besteht aus Gruppenrichtlinieneinstellungen, die die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren. Sie können die Richtlinienvorlage auf einem beliebigen Server oder auf einer Arbeitsstation installieren, Sie wird jedoch häufig auf einer Verwaltungsarbeitsstation installiert, die ein unterstützter Windows-Server oder-Clientcomputer ist. Die Workstation muss kein dedizierter Computer sein.

## <a href="" id="---------mbam-client"></a> MBAM-Client


Der MBAM-Client ist auf einem Windows-Computer installiert und weist die folgenden Merkmale auf:

-   Verwendet Gruppenrichtlinien, um die BitLocker-Laufwerkverschlüsselung von Clientcomputern im Unternehmen zu erzwingen.

-   Sammelt den Wiederherstellungsschlüssel für die drei BitLocker-Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und austauschbare Datenlaufwerke (USB).

-   Sammelt Kompatibilitätsdaten für den Computer und übergibt die Daten an das Berichterstattungssystem.

## Verwandte Themen


[Erste Schritte mit MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





