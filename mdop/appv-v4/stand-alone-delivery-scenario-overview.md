---
title: Übersicht über die Szenarien für die eigenständige Bereitstellung
description: Übersicht über die Szenarien für die eigenständige Bereitstellung
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806255"
---
# Übersicht über die Szenarien für die eigenständige Bereitstellung


Das eigenständige Zustellungs Szenario ist eine ideale Application Virtualization-Lösung für Umgebungen, in denen eine Verbindung mit niedriger Bandbreite oder keine Konnektivität die Möglichkeit des Application Virtualization Desktop-Clients zum Streamen von Anwendungen von zentralisierten Servern begrenzt. In diesen Umgebungen arbeiten Benutzer häufig Remote, und Gerätebesitzer installieren Anwendungen mithilfe von Windows Installer-Dateien.

Sie können den Application Virtualization Sequencer verwenden, um sequenzierte Anwendungen zu erstellen, die Windows Installer-Dateien enthalten. Diese Pakete umfassen virtualisierte Anwendungen, Veröffentlichungsinformationen und die erforderlichen Installationsroutinen für die Installation der Pakete auf den Clientsystemen. Das Installationsprogramm fügt das virtuelle Anwendungspaket dem Microsoft Application Virtualization-Desktop Client hinzu. Die Veröffentlichungsinformationen sind so konfiguriert, dass Anwendungen von einem lokalen Speicherort geladen werden, anstatt Sie über ein WAN zu streamen. Benutzer können temporär eine Verbindung mit einem Netzwerk herstellen, um die Windows Installer-Dateien abzurufen, oder Sie können Sie von einer DVD ausführen.

Das eigenständige Zustellungs Szenario bietet Benutzern die folgenden Vorteile:

-   Einfacher Bereitstellungsvorgang.

-   Netzwerk und Server werden zur Laufzeit nicht benötigt.

-   Anwendungen werden vorab zwischengespeichert und allen Benutzern zur Verfügung gestellt.

Für das eigenständige Zustellungs Szenario gelten die folgenden Einschränkungen:

-   Integrierte, automatisierte Berichte sind nicht verfügbar. Berichte müssen mit externen Berichterstellungstools erstellt werden.

-   Anwendungen müssen wie die ursprünglichen Windows Installer-Dateien manuell an den Client übermittelt werden.

## Verwandte Themen


[So installieren Sie Application Virtualization Client manuell](how-to-manually-install-the-application-virtualization-client.md)

[So veröffentlichen Sie eine virtuelle Anwendung auf dem Client](how-to-publish-a-virtual-application-on-the-client.md)

 

 





