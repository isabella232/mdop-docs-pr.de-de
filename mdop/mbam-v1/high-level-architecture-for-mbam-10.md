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
ms.openlocfilehash: d06c7bd801a9dd63916d310af75e88a307e7226a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910410"
---
# <a name="high-level-architecture-for-mbam-10"></a>High-Level-Architektur für MBAM 1.0


Microsoft BitLocker Administration and Monitoring (MBAM) ist eine Client-/Server-Datenverschlüsselungslösung, mit der Sie die BitLocker-Bereitstellung und -Bereitstellung vereinfachen, die BitLocker-Compliance und -Berichterstellung verbessern und Supportkosten senken können. MBAM enthält die In diesem Thema beschriebenen Features.

Darüber hinaus gibt es ein Video, das eine Übersicht über die MBAM-Architektur und das MBAM-Setup bietet. Weitere Informationen finden Sie unter [MBAM Deployment and Architecture Overview](https://go.microsoft.com/fwlink/p/?LinkId=258392).

## <a name="architecture-overview"></a>Übersicht über die Architektur


Das folgende Diagramm zeigt die MBAM-Architektur. Die Mbam-Bereitstellungstopologie mit einem Server wird gezeigt, um die MBAM-Features einzuführen. Diese MBAM-Bereitstellungstopologie wird jedoch nur für Laborumgebungen empfohlen.

**Hinweis:**  
Für eine Produktionsbereitstellung wird mindestens eine DREI-Computer-MBAM-Bereitstellungstopologie empfohlen. Weitere Informationen zu MBAM-Bereitstellungstopologien finden Sie unter [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).

 

![Mbam-Bereitstellungstopologie mit einem Server.](images/mbam-1-server.jpg)

1.  **Administration and Monitoring Server**. Der MBAM-Verwaltungs- und -Überwachungsserver wird auf einem Windows-Server installiert und hostet die MBAM-Verwaltungswebsite und die Überwachungswebdienste. Die MBAM-Verwaltungswebsite wird verwendet, um den Unternehmenscompliancestatus zu ermitteln, Aktivitäten zu überwachen, die Hardwarefunktionen zu verwalten und um auf Wiederherstellungsdaten wie die BitLocker-Wiederherstellungsschlüssel zuzugreifen. Der Verwaltungs- und Überwachungsserver stellt eine Verbindung mit den folgenden Datenbanken und Diensten her:

    -   Wiederherstellungs- und Hardwaredatenbank. Die Wiederherstellungs- und Hardwaredatenbank wird auf einem Windows-basierten Server installiert und SQL Server Instanz unterstützt. Diese Datenbank speichert Wiederherstellungsdaten und Hardwareinformationen, die von MBAM-Clientcomputern gesammelt werden.

    -   Compliance- und Überwachungsdatenbank. Die Konformitäts- und Überwachungsdatenbank wird auf einem Windows Server installiert und SQL Server Instanz unterstützt. In dieser Datenbank werden Kompatibilitätsdaten für MBAM-Clientcomputer gespeichert. Diese Daten werden in erster Linie für Berichte verwendet, die von SQL Server Reporting Services (SSRS) gehostet werden.

    -   Compliance- und Überwachungsberichte. Die Konformitäts- und Überwachungsberichte werden auf einem Windows-basierten Server installiert und SQL Server Instanz unterstützt, auf der das SSRS-Feature installiert ist. Diese Berichte enthalten Microsoft BitLocker-Verwaltungs- und Überwachungsberichte. Auf diese Berichte kann über die MBAM-Verwaltungswebsite oder direkt über den SSRS-Server zugegriffen werden.

2.  **MBAM-Client**. Der Microsoft BitLocker-Verwaltungs- und Überwachungsclient führt die folgenden Aufgaben aus:

    -   Verwendet Gruppenrichtlinien, um die BitLocker-Verschlüsselung von Clientcomputern im Unternehmen zu erzwingen.

    -   Erfasst den Wiederherstellungsschlüssel für die drei BitLocker-Datentypen: Betriebssystemlaufwerke, Festplattenlaufwerke und USB-Laufwerke (Wechseldaten).

    -   Sammelt Wiederherstellungsinformationen und Hardwareinformationen zu den Clientcomputern.

    -   Sammelt Compliancedaten für den Computer und übergibt die Daten an das Berichterstellungssystem.

3.  **Richtlinienvorlage**. Die MBAM-Gruppenrichtlinienvorlage wird auf einem unterstützten Windows-basierten Server oder Clientcomputer installiert. Diese Vorlage wird verwendet, um die MBAM-Implementierungseinstellungen für die BitLocker-Laufwerkverschlüsselung anzugeben.

## <a name="related-topics"></a>Verwandte Themen


[Erste Schritte mit MBAM 1.0](getting-started-with-mbam-10.md)

 

 





