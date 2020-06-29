---
title: High-Level-Architektur für MBAM 1.0
description: High-Level-Architektur für MBAM 1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811035"
---
# High-Level-Architektur für MBAM 1.0


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ist eine Client/Server-Daten Verschlüsselungslösung, die Ihnen dabei helfen kann, die BitLocker-Bereitstellung und Bereitstellung zu vereinfachen, die BitLocker-Compliance und-Berichterstellung zu verbessern und die Supportkosten zu reduzieren MBAM enthält die Features, die in diesem Thema beschrieben werden.

Darüber hinaus gibt es ein Video, das eine Übersicht über die MBAM-Architektur und das MBAM-Setup bietet. Weitere Informationen finden Sie unter [Übersicht über die Bereitstellung und Architektur von MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258392).

## Übersicht über die Architektur


Das folgende Diagramm zeigt die MBAM-Architektur an. Die MBAM-Bereitstellungstopologie mit einem Server wird angezeigt, um die MBAM-Features einzuführen. Diese MBAM-Bereitstellungstopologie wird jedoch nur für Lab-Umgebungen empfohlen.

**Hinweis**  Für eine Produktionsbereitstellung wird mindestens eine MBAM-Bereitstellungstopologie mit drei Computern empfohlen. Weitere Informationen zu MBAM-Bereitstellungs Topologien finden Sie unter [Bereitstellen der MBAM 1,0-Server Infrastruktur](deploying-the-mbam-10-server-infrastructure.md).

 

![mbam Single Server-Bereitstellungstopologie](images/mbam-1-server.jpg)

1.  **Verwaltungs-und Überwachungs Server**. Der MBAM-Verwaltungs-und-Überwachungsserver ist auf einem Windows-Server installiert und fungiert als Host für die MBAM-Verwaltungs-und-Verwaltungswebsite sowie für die Überwachungs-Webdienste. Die MBAM-Verwaltungs-und-Verwaltungswebsite wird verwendet, um den Status der Unternehmenskonformität zu ermitteln, die Aktivität zu überwachen, die Hardware Funktion zu verwalten und auf Wiederherstellungsdaten wie die BitLocker-Wiederherstellungsschlüssel zuzugreifen. Der Administrations-und Überwachungs Server stellt eine Verbindung mit den folgenden Datenbanken und Diensten her:

    -   Wiederherstellungs-und Hardware Datenbank. Die Wiederherstellungs-und Hardware Datenbank ist auf einem Windows-basierten Server und unterstützten SQLServer-Instanzen installiert. In dieser Datenbank werden Wiederherstellungsdaten und Hardwareinformationen gespeichert, die von MBAM-Clientcomputern erfasst werden.

    -   Konformitäts-und Überwachungsdatenbank. Die Datenbank "Konformitäts-und Überwachungsdatenbank" wird auf einer Windows Server-und unterstützten SQLServer-Instanz installiert. In dieser Datenbank werden Kompatibilitätsdaten für MBAM-Clientcomputer gespeichert. Diese Daten werden hauptsächlich für Berichte verwendet, die von SQL Server Reporting Services (SSRS) gehostet werden.

    -   Konformitäts-und Überwachungsberichte. Die Konformitäts-und Überwachungsberichte werden auf einem auf Windows basierenden Server und unterstützten SQLServer-Instanzen installiert, auf denen das SSRS-Feature installiert ist. Diese Berichte enthalten Berichte zur Microsoft BitLocker-Verwaltung und-Überwachung. Auf diese Berichte kann über die MBAM-Verwaltungs-und-Verwaltungswebsite oder direkt vom SSRS-Server aus zugegriffen werden.

2.  **MBAM-Client**. Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung führt die folgenden Aufgaben aus:

    -   Verwendet Gruppenrichtlinien, um die BitLocker-Verschlüsselung von Clientcomputern im Unternehmen durchzusetzen.

    -   Sammelt den Wiederherstellungsschlüssel für die drei BitLocker-Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und austauschbare Datenlaufwerke (USB).

    -   Sammelt Wiederherstellungsinformationen und Hardwareinformationen zu den Clientcomputern.

    -   Sammelt Kompatibilitätsdaten für den Computer und übergibt die Daten an das Berichterstattungssystem.

3.  **Richtlinienvorlage**aus. Die MBAM-Gruppenrichtlinienvorlage ist auf einem unterstützten Windows-basierten Server oder Clientcomputer installiert. Diese Vorlage wird verwendet, um die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung festzulegen.

## Verwandte Themen


[Erste Schritte mit MBAM 1.0](getting-started-with-mbam-10.md)

 

 





