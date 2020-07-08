---
title: Einführung in das Application Virtualization Security Guide
description: Einführung in das Application Virtualization Security Guide
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806639"
---
# Einführung in das Application Virtualization Security Guide


Dieser Microsoft Application Virtualization (app-v)-Sicherheitsleitfaden enthält Anweisungen für Administratoren, die für die Konfiguration der Sicherheitsfeatures verantwortlich sind, die für die APP-v-Bereitstellung ausgewählt wurden.

**Hinweis**  Diese Dokumentation bietet keine Anleitungen für die Auswahl der spezifischen Sicherheitsoptionen. Diese Informationen finden Sie im Whitepaper zu App-V Security Best Practices, das unter verfügbar ist <https://go.microsoft.com/fwlink/?LinkId=127120> .

 

Als App-V-Administrator mit diesem Leitfaden sollten Sie mit den folgenden sicherheitsrelevanten Technologien vertraut sein:

-   Active Directory Domain Services

-   Infrastruktur öffentlicher Schlüssel (PKI)

-   IPSec (Internet Protocol Security)

-   Gruppenrichtlinien

-   Internet Informationsdienste (IIS)

## App-V-Infrastrukturkomponenten


Wenn Sie eine erweiterte Sicherheits-App-V-Umgebung planen, können Sie verschiedene Infrastrukturmodelle in Frage stellen.

**Hinweis**  Weitere Informationen zu App-V-Infrastrukturmodellen finden Sie in der folgenden Dokumentation:

-   [Leitfaden zur Planung und Bereitstellung von App-V](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [Leitfaden für Infrastrukturplanung und-Entwurf](https://go.microsoft.com/fwlink/?LinkId=151986)

 

Diese Modelle verwenden einige, aber möglicherweise nicht alle App-V-Komponenten, die in der folgenden Abbildung dargestellt sind.

![App-v Branch Office-Diagramm](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>Application Virtualization (App-V)-Verwaltungs Server  
Der APP-v-Verwaltungs Server strömt den Paketinhalt aus und veröffentlicht die Verknüpfungen und Dateitypen Zuordnungen für den App-v-Client. Der App-V-Verwaltungs Server unterstützt auch das aktive Upgrade, die Lizenzverwaltung und eine Datenbank, die für die Berichterstellung verwendet werden kann.

<a href="" id="application-virtualization--app-v--streaming-server"></a>Application Virtualization (App-V)-Streamingserver  
Der APP-v-Streamingserver hostet die Pakete für das Streaming an App-v-Clients in Umgebungen wie Zweigstellen, bei denen die Bandbreite der Verbindung zum App-v-Verwaltungsserver nicht ausreicht, um Paketinhalte an Clients zu streamen. Der Streamingserver enthält nur Streamingfunktionen und stellt Ihnen keine app-v-Verwaltungskonsole oder den App-v-Verwaltungs-Webdienst zur Verfügung.

<a href="" id="application-virtualization--app-v--data-store"></a>Application Virtualization (App-V)-Datenspeicher  
Der APP-v-Datenspeicher in der SQL-Datenbank speichert Informationen zur APP-v-Infrastruktur. Die Informationen im App-V-Datenspeicher umfassen alle Anwendungsdatensätze, Anwendungszuordnungen und die Gruppen, die die Application Virtualization-Umgebung verwalten.

<a href="" id="application-virtualization--app-v--management-service"></a>Application Virtualization (App-V)-Verwaltungsdienst  
Der App-V-Verwaltungsdienst kommuniziert Lese-und Schreibanforderungen an den Application Virtualization-Datenspeicher. Diese Komponente kann auf demselben Computer wie der App-V-Verwaltungs Server oder auf einem anderen Computer installiert sein, auf dem IIS installiert ist.

<a href="" id="application-virtualization--app-v--management-console"></a>Application Virtualization (App-V)-Verwaltungskonsole  
Die APP-v-Verwaltungskonsole ist ein Snap-in-Verwaltungsdienstprogramm für die APP-v Server-Verwaltung. Diese Komponente kann auf demselben Computer wie der App-V-Server oder auf einer separaten Workstation mit MMC 3.0 und installiert werden. NET 2.0 installiert ist.

<a href="" id="application-virtualization--app-v--sequencer"></a>Application Virtualization (App-V)-Sequenzer  
Der App-V-Sequencer überwacht und erfasst die Installation von Anwendungen und erstellt virtuelle Anwendungspakete. Die Ausgabe des Sequencers besteht aus dem Anwendungssymbol, der OSD-Datei mit Anwendungs Definitionsinformationen, einer Paket Manifestdatei und einer SFT-Datei mit den Inhaltsdateien der Anwendung. Optional kann eine Windows Installer-Datei für die Installation des Pakets erstellt werden, ohne die App-V-Infrastruktur zu verwenden.

<a href="" id="application-virtualization--app-v--client"></a>Application Virtualization (App-V)-Client  
Der APP-v-Client ist auf dem App-v-Desktop Clientcomputer oder auf dem App-v-Terminaldiensteclient installiert. Sie stellt die virtuelle Umgebung für die virtuellen Anwendungspakete bereit. Der App-V-Client verwaltet das Streaming des Pakets in den Cache, die Aktualisierung der virtuellen Anwendungsveröffentlichung und die Interaktion mit den Application Virtualization-Servern.

 

 





