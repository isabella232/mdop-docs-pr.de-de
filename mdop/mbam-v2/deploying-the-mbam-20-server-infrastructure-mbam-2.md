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
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810747"
---
# Bereitstellen der Serverinfrastruktur von MBAM 2.0


Die Microsoft BitLocker-MBAM-Server Features für die eigenständige Topologie können in verschiedenen Konfigurationen auf zwei oder mehr Servern in einer Produktionsumgebung installiert werden. Die empfohlene Konfiguration sind zwei Server für eine Produktionsumgebung, je nach Ihren Skalierbarkeitsanforderungen. Verwenden Sie einen einzelnen Server für eine MBAM-Installation nur in Testumgebungen. Weitere Informationen zum Planen der Bereitstellung von MBAM Server Features finden Sie unter [Planen der MBAM 2,0-Server Bereitstellung](planning-for-mbam-20-server-deployment-mbam-2.md).

Das folgende Diagramm zeigt ein Beispiel, wie Sie die empfohlene MBAM-Bereitstellung mit zwei Servern konfigurieren können. Mit dieser Konfiguration werden bis zu 200.000 MBAM-Clients in einer Produktionsumgebung unterstützt. Die Server Features und-Datenbanken im Architektur Bild werden im folgenden Abschnitt beschrieben und unter dem Computer oder Server aufgelistet, auf dem wir die Installation empfehlen.

![mbam 2 2-Server Bereitstellungstopologie](images/mbam2-3-servers.gif)

## Verwaltungs-und Überwachungs Server


Die folgenden Features sind auf diesem Server installiert:

-   **Verwaltungs-und Überwachungs Server**. Die Verwaltungs-und Überwachungs Server Funktion ist auf einem Windows-Server installiert und besteht aus der Helpdesk-Website und den Überwachungs-Webdiensten.

-   **Self-Service-Portal**. Das Self-Service-Portal ist auf einem Windows-Server installiert. Das Self-Service-Portal ermöglicht Endbenutzern auf Clientcomputern die unabhängige Anmeldung bei einer Website, auf der Sie einen Wiederherstellungsschlüssel zum Wiederherstellen eines gesperrten BitLocker-Volumes abrufen können.

## Daten Bank Server


Die folgenden Features sind auf diesem Server installiert:

-   **Wiederherstellungsdatenbank**. Die Wiederherstellungsdatenbank ist auf einem Windows-Server und einer unterstützten Instanz von Microsoft SQLServer installiert. In dieser Datenbank werden Wiederherstellungsdaten gespeichert, die von MBAM-Clientcomputern erfasst werden.

-   **Konformitäts-und Überwachungsdatenbank**. Die Compliance-und Überwachungsdatenbank ist auf einem Windows-Server und einer unterstützten Instanz von SQLServer installiert. In dieser Datenbank werden Kompatibilitätsdaten für MBAM-Clientcomputer gespeichert. Diese Daten werden hauptsächlich für Berichte verwendet, die von SQL Server Reporting Services (SSRS) gehostet werden.

-   **Konformitäts-und Überwachungsberichte**. Die Kompatibilitäts-und Überwachungsberichte sind auf einem Windows-Server und einer unterstützten Instanz von SQLServer installiert, auf der das Feature SQL Server Reporting Services (SSRS) installiert ist. Diese Berichte enthalten MBAM-Berichte, auf die Sie über die Helpdesk-Website oder direkt vom SSRS-Server aus zugreifen können.

## Verwaltungsarbeitsstation


Das folgende Feature ist auf der Verwaltungsarbeitsstation installiert, die ein Windows-Server oder ein Clientcomputer sein kann.

-   **Richtlinienvorlage**aus. Die Richtlinienvorlage besteht aus Gruppenrichtlinien, die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren. Sie können die Richtlinienvorlage auf einem beliebigen Server oder auf einer Arbeitsstation installieren, Sie wird jedoch häufig auf einer Verwaltungsarbeitsstation installiert, die ein unterstützter Windows-Server oder-Clientcomputer ist. Die Workstation muss kein dedizierter Computer sein.

## <a href="" id="---------mbam-client"></a> MBAM-Client


Der MBAM-Client ist auf einem Windows-Computer installiert und weist die folgenden Merkmale auf:

-   Verwendet Gruppenrichtlinien, um die BitLocker-Laufwerkverschlüsselung von Clientcomputern im Unternehmen zu erzwingen.

-   Sammelt den Wiederherstellungsschlüssel für die drei BitLocker-Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und austauschbare Datenlaufwerke (USB).

-   Sammelt Kompatibilitätsdaten für den Computer und übergibt die Daten an das Berichterstattungssystem.

## Weitere Ressourcen für die Bereitstellung von MBAM 2,0-Server Features


[Bereitstellen von MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





