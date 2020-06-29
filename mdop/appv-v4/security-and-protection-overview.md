---
title: Übersicht über Sicherheit und Schutz
description: Übersicht über Sicherheit und Schutz
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806395"
---
# Übersicht über Sicherheit und Schutz


Microsoft Application Virtualization 4.5 bietet die folgenden erweiterten Sicherheitsfeatures, die Ihnen bei der Planung und Implementierung einer sichereren Bereitstellungsstrategie helfen:

-   Application Virtualization unterstützt jetzt TLS (Transport Layer Security) mithilfe von X. 509 v3-Zertifikaten. Vorausgesetzt, dass ein Serverzertifikat dem geplanten Application Virtualization Management oder Streaming Server bereitgestellt wurde, wird die Installation standardmäßig mit dem RTSPS-Protokoll über Port 322 gesichert. Durch die Verwendung von RTSPS wird sichergestellt, dass die Kommunikation zwischen den Application Virtualization-Servern und den Application Virtualization-Clients signiert und verschlüsselt ist. Wenn dem Server während der Installation von Application Virtualization Server kein Zertifikat zugewiesen ist, wird die Kommunikation auf RTSP über Port 554 eingestellt.

    **Sicherheitshinweis:**

    Damit Sie eine sichere Einrichtung des Servers gewährleisten können, müssen Sie sicherstellen, dass die RTSP-Ports deaktiviert sind, auch wenn Sie alle Pakete für die Verwendung von RTSPS konfiguriert haben.

    Wenn Sie dem Server nach der Installation des Servers Sicherheitszertifikate hinzufügen, werden die Zertifikate möglicherweise nicht vom Server erkannt. Um die Erkennung von Sicherheitszertifikaten zu gewährleisten, starten Sie den Server nach dem Hinzufügen der Zertifikate neu.

-   Der Client muss so konfiguriert sein, dass er dasselbe Protokoll und denselben Port wie der Server verwendet, oder er kann nicht mit dem Server kommunizieren. Der Client muss auch dem Aussteller des Zertifikats Vertrauen und mit mehreren primären Anbietern im vertrauenswürdigen Stammspeicher ausgeliefert werden. Sie können selbstsignierte Zertifikate verwenden, doch müssen Sie die Clients aktualisieren.

-   Wenn Sie IIS-Server für die Verwendung des HTTPS-Protokolls für Streaming konfigurieren, müssen Sie SSL (Secure Sockets Layer) auf dem IIS-Server einrichten und das Zertifikat für den Server bereitstellen. Die Clients müssen auch so konfiguriert werden, dass Sie der Stammzertifizierungsstelle vertrauen, die das Serverzertifikat ausgestellt hat.

-   Die Kerberos-Authentifizierung wurde Microsoft Application Virtualization als Standardauthentifizierungsmechanismus hinzugefügt. Frühere Versionen haben sich auf NTLM v2 für die Authentifizierung verlassen. Die Verwendung der Kerberos-Authentifizierung stärkt die Sicherheit der Kommunikation zwischen dem Client und dem Application Virtualization Server. Wenn eine Verbindung vom Client initiiert wurde, überprüft der Application Virtualization Server das Sitzungsticket mit dem Schlüssel Verteilungs Center (Key Distribution Center, KDC).

-   Aufgrund der Unterstützung für die Verwendung von Serverzertifikaten und die Verwendung von RTSPS-oder HTTPS-Protokollen können Sie nun Clients außerhalb des Unternehmensnetzwerks unterstützen. Dies kann dazu beitragen, dass Mobile Benutzer keine sichere Verbindung mit dem Unternehmensnetzwerk (VPN, RAS usw.) einrichten müssen, bevor Sie die bereitgestellten Application Virtualization-Anwendungen starten.

Die folgenden wichtigen Sicherheitsüberlegungen sollten Sie berücksichtigen:

-   Halten Sie die Server immer vollständig aktualisiert und geschützt.

-   Wenn Sie ein Zertifikat hinzufügen möchten, um eine sicherere Kommunikation mit dem Application Virtualization Management Server zu ermöglichen, müssen die folgenden Kriterien erfüllt sein:

    -   Der Benutzer, der das Zertifikat hinzufügen wird, muss ein Administrator auf dem Server sein, auf dem sich der Zertifikatspeicher befindet.

    -   Der Server Dienst muss gestartet werden.

    -   Port 139 auf dem Verwaltungs Server muss für den Webdienst server'sIP geöffnet sein.

-   Verwenden Sie Zugriffssteuerungslisten (ACLs), um sicherzustellen, dass die Anwendungspakete und alle Paketdateien geschützt sind und nicht manipuliert werden können. ACLs beschränken den Zugriff auf den Speicherort oder den Ordner, in dem Sie die Pakete speichern, sodass der Zugriff nur auf bestimmte Konten möglich ist.

-   Stellen Sie sicher, dass der Kanal zwischen dem Application Virtualization-Verwaltungs Server und der Datenbank gesichert ist, beispielsweise mithilfe von IPSec.

-   Wenn Pakete auf einem SAN oder NAS gespeichert werden, stellen Sie sicher, dass die Verbindung zwischen dem zentralen Speichergerät und den Application Virtualization-Servern geschützt ist.

-   Alle Kommunikationskanäle für den Client sollten geschützt werden – einschließlich Verbindungen mit dem Veröffentlichungsserver, dem Application Virtualization Server und dem Pfad zu den OSD-und ICO-Dateien – mithilfe eines Protokolls wie HTTPS oder IPSec. 

-   Client Berechtigungen sollten so konfiguriert werden, dass Sie sicherstellen, dass Pakete nicht von Benutzern manipuliert werden können. Es ist besonders wichtig, dass Sie Benutzern keine Berechtigung zum Hinzufügen oder Aktualisieren von Paketen auf Systemen gewähren, wie etwa RDSession-Hostserver (Remote Desktop-Sitzungshost), die für mehrere Benutzer freigegeben wurden.

-   Die Kerberos-Authentifizierung muss in Domänen-oder Gesamtstrukturumgebungen zulässig sein, damit die Server Verwaltungskonsole ordnungsgemäß funktioniert.

-   Diese Version der Software unterstützt nicht das Hosten eines Kerberos-basierten RTSP-Servers und eines Microsoft NTLM-basierten IIS-Servers auf demselben Computer. Wenn Sie einen RTSP-Server und einen IIS-Server auf demselben Computer hosten möchten, entfernen Sie den SPN vom IIS-Server, und verwenden Sie die NTLM-Authentifizierung.

## Verwandte Themen


[Planen der Bereitstellung von Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

 

 





