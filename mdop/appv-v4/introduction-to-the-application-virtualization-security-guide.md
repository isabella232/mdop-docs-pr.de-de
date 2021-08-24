---
title: Einführung in den Application Virtualization Security Guide
description: Einführung in den Application Virtualization Security Guide
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
ms.openlocfilehash: 82914de48a5a5777f6ce4b50fe3e8af34dd82494
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910780"
---
# <a name="introduction-to-the-application-virtualization-security-guide"></a>Einführung in den Application Virtualization Security Guide


Dieses Sicherheitshandbuch für Microsoft Application Virtualization (App-V) enthält Anweisungen für Administratoren, die für die Konfiguration der Sicherheitsfeatures verantwortlich sind, die für die App-V-Bereitstellung ausgewählt wurden.

**Hinweis:**  
Diese Dokumentation enthält keine Anleitungen für die Auswahl der spezifischen Sicherheitsoptionen. Diese Informationen finden Sie im Whitepaper zu bewährten Methoden für die App-V-Sicherheit unter <https://go.microsoft.com/fwlink/?LinkId=127120> .

 

Als App-V-Administrator, der dieses Handbuch verwendet, sollten Sie mit den folgenden sicherheitsrelevanten Technologien vertraut sein:

-   Active Directory Domain Services

-   Public Key-Infrastruktur (PKI)

-   Internetprotokollsicherheit (Internet Protocol Security, IPsec)

-   Gruppenrichtlinien

-   Internetinformationsdienste (IIS)

## <a name="app-v-infrastructure-components"></a>APP-V-Infrastrukturkomponenten


Bei der Planung einer erweiterten Sicherheits-App-V-Umgebung können Sie verschiedene Infrastrukturmodelle berücksichtigen.

**Hinweis:**  
Weitere Informationen zu App-V-Infrastrukturmodellen finden Sie in der folgenden Dokumentation:

-   [App-V-Planungs- und Bereitstellungshandbuch](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [Reihe "Leitfaden zur Infrastrukturplanung und -entwurf"](https://go.microsoft.com/fwlink/?LinkId=151986)

 

Diese Modelle verwenden einige, aber möglicherweise nicht alle app-V-Komponenten, die in der folgenden Abbildung dargestellt sind.

![App-v-Zweigstellendiagramm.](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>Application Virtualization (App-V)-Verwaltungsserver  
Der App-V-Verwaltungsserver streamt den Paketinhalt und veröffentlicht die Verknüpfungen und Dateitypzuordnungen an den App-V-Client. Der App-V-Verwaltungsserver unterstützt auch das aktive Upgrade, die Lizenzverwaltung und eine Datenbank, die für die Berichterstellung verwendet werden kann.

<a href="" id="application-virtualization--app-v--streaming-server"></a>Application Virtualization (App-V) Streaming Server  
Der App-V-Streamingserver hostet die Pakete für das Streaming auf App-V-Clients in Umgebungen wie Zweigstellen, in denen die Bandbreite der Verbindung mit dem App-V-Verwaltungsserver nicht ausreicht, um Inhalte von Streamingpaketen an Clients zu streamen. Der Streamingserver enthält nur Streamingfunktionen und stellt ihnen weder die App-V-Verwaltungskonsole noch den App-V-Verwaltungswebdienst zur Verfügung.

<a href="" id="application-virtualization--app-v--data-store"></a>Application Virtualization (App-V)-Daten Store  
Der App-V-Datenspeicher in der SQL-Datenbank behält Informationen im Zusammenhang mit der App-V-Infrastruktur bei. Die Informationen im App-V-Datenspeicher umfassen alle Anwendungseinträge, Anwendungszuweisungen und welche Gruppen die Application Virtualization-Umgebung verwalten.

<a href="" id="application-virtualization--app-v--management-service"></a>Application Virtualization (App-V)-Verwaltungsdienst  
Der App-V-Verwaltungsdienst kommuniziert Lese-/Schreibanforderungen an den Application Virtualization-Datenspeicher. Diese Komponente kann auf demselben Computer wie der App-V-Verwaltungsserver oder auf einem separaten Computer installiert werden, auf dem IIS installiert ist.

<a href="" id="application-virtualization--app-v--management-console"></a>Application Virtualization (App-V)-Verwaltungskonsole  
Die App-V-Verwaltungskonsole ist ein Snap-In-Verwaltungsprogramm für die App-V-Serververwaltung. Diese Komponente kann auf demselben Computer wie der App-V-Server oder auf einer separaten Arbeitsstation installiert werden, auf der MMC 3.0 und .NET 2.0 installiert sind.

<a href="" id="application-virtualization--app-v--sequencer"></a>Application Virtualization (App-V) Sequencer  
Der App-V Sequencer überwacht und erfasst die Installation von Anwendungen und erstellt virtuelle Anwendungspakete. Die Ausgabe des Sequencer besteht aus dem Anwendungssymbol, der OSD-Datei mit Anwendungsdefinitionsinformationen, einer Paketmanifestdatei und einer SFT-Datei mit den Inhaltsdateien der Anwendung. Optional kann eine Windows Installer-Datei für die Installation des Pakets erstellt werden, ohne die App-V-Infrastruktur zu verwenden.

<a href="" id="application-virtualization--app-v--client"></a>Application Virtualization (App-V)-Client  
Der App-V-Client wird auf dem App-V-Desktopclientcomputer oder auf dem App-V-Terminaldienste-Clientcomputer installiert. Es stellt die virtuelle Umgebung für die virtuellen Anwendungspakete bereit. Der App-V-Client verwaltet das Paketstreaming im Cache, die Aktualisierung der Veröffentlichung virtueller Anwendungen und die Interaktion mit den Application Virtualization Servers.

 

 





