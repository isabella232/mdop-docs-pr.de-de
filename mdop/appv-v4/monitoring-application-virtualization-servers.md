---
title: Überwachen von Application Virtualization Servern
description: Überwachen von Application Virtualization Servern
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806588"
---
# Überwachen von Application Virtualization Servern


Zur Vereinfachung der Application Virtualization-Server Verwaltung (App-V) können Sie das System Center Operations Manager2007-Management Pack verwenden. Dieses Management Pack unterstützt nur Application Virtualization (App-V) 4,5-Server; frühere Server Versionen werden nicht unterstützt. Das Management Pack maximiert die APP-v Server-Verfügbarkeit für die Behandlung von App-v-Client Anforderungen.

## Status anzeigen


Die Statusanzeige des App-V-Servers ist farblich gekennzeichnet. Die Farben stellen die folgenden Statuswerte dar:

-   Keine Farbe gibt an, dass der Server ohne nicht BEHEB Bare Fehler ausgeführt wird.

-   Gelb gibt an, dass eine der Komponenten nicht ordnungsgemäß funktioniert. Die Gesamtfunktionalität des Servers wird beeinträchtigt, der Server steht jedoch weiterhin zur Verfügung.

-   Rot gibt an, dass der Server nicht verfügbar ist und keine wichtigen Dienste bereitstellen oder mit externen Dienstabhängigkeiten kommunizieren kann.

## Überwachungskriterien


Das Management Pack überwacht die folgenden Aspekte des Serverzustands:

-   Server Status: überwacht Serverereignisse, um zu überprüfen, ob der Server die erwarteten Dienste bereitstellt.

-   Zugriff auf Datenspeicher: verfolgt die Möglichkeit eines oder mehrerer App-v-Verwaltungsserver, auf den App-v-Datenspeicher zuzugreifen und mit ihm zu kommunizieren.

-   Zugriff auf Inhaltsdaten: überwacht den Zugriff auf das \\Content-Verzeichnis, das ein lokales Verzeichnis oder eine Netzwerkfreigabe sein kann, und die Möglichkeit, die angeforderten Dateien zu lesen.

-   Sicherheit – meldet Fehler mit dem Zertifikat des App-V-Servers und der sicheren Kommunikation.

-   Client Anforderungsbehandlung – überwacht die Fähigkeit eines oder mehrerer App-V-Server, Clientanforderungen zu verarbeiten und auf diese ordnungsgemäß zu reagieren. Diese Anforderungen umfassen das Veröffentlichen von Elementen wie Konfigurationsanforderungen, Paket Ladeanforderungen und außerhalb von Sequenz Anforderungen.

-   Serverkonfiguration: überprüft die Konfigurationseinstellungen des App-V-Servers. Diese Konfigurationseinstellungen umfassen die Einstellungen in der Registrierung und im App-V-Datenspeicher.

## Server Unterschiede


Die wichtigsten Unterschiede zwischen dem App-v-Verwaltungsserver und dem App-v-Streamingserver lauten wie folgt:

-   App-V-Verwaltungsserver können Veröffentlichungs-, Streaming-, Verwaltungs-und Berichterstattungs Dienste bereitstellen. Daher kann das Management Pack mehr Aspekte des App-v-Verwaltungsservers verwalten, als auf dem App-v-Streamingserver verwaltet werden können, der nur Paketstreaming bereitstellt.

-   Der APP-v-Streamingserver hat keinen App-v-Datenspeicher, daher wird der Zugriff auf den Datenspeicher nicht überwacht. Die Konfigurationsinformationen für den App-V-Streamingserver werden in der Registrierung verwaltet.

-   Der APP-v-Streamingserver verwendet nicht die Schnittstelle der APP-v Server-Verwaltungskonsole. Verwenden Sie andere Tools, um die Konfiguration zu verwalten.

## Verwandte Themen


[Application Virtualization Server](application-virtualization-server.md)

 

 





