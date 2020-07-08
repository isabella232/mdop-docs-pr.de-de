---
title: Leitfaden zur Planung und Bereitstellung für das Application Virtualization System
description: Leitfaden zur Planung und Bereitstellung für das Application Virtualization System
author: dansimp
ms.assetid: 6c012e33-9ac6-4cd8-84ff-54f40973833f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10bcac26fddae2f0e5826dbd7335adda06d3987e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806515"
---
# Leitfaden zur Planung und Bereitstellung für das Application Virtualization System


Microsoft Application Virtualization Management bietet die Möglichkeit, Anwendungen für Endbenutzercomputer verfügbar zu machen, ohne die Anwendungen direkt auf diesen Computern installieren zu müssen. Dies wird durch einen Prozess ermöglicht, der als *Sequenzierung der Anwendung*bezeichnet wird, wodurch jede Anwendung in ihrer eigenen, eigenständigen virtuellen Umgebung auf dem Clientcomputer ausgeführt werden kann. Die sequenzierten Anwendungen werden voneinander isoliert, wodurch Anwendungskonflikte eliminiert werden, Sie können jedoch weiterhin mit dem Clientcomputer interagieren.

Application Virtualization Client ist die Komponente Application Virtualization System, die es dem Endbenutzer ermöglicht, mit den Anwendungen zu interagieren, nachdem Sie auf dem Computer veröffentlicht wurden. Der Client verwaltet die virtuelle Umgebung, in der die virtualisierten Anwendungen auf jedem Computer ausgeführt werden. Nachdem der Client auf einem Computer installiert wurde, müssen die Anwendungen dem Computer über einen als " *Publishing*" bezeichneten Prozess zur Verfügung gestellt werden, mit dem der Endbenutzer die virtuellen Anwendungen ausführen kann. Der Veröffentlichungsprozess platziert die Symbole und Tastenkombinationen für die virtuelle Anwendung auf dem Computer – normalerweise auf dem Windows-Desktop oder im **Startmenü** – und platziert auch die Zuordnungsinformationen für die Paketdefinition und die Dateitypzuordnung auf dem Computer. Durch die Veröffentlichung wird der Inhalt des Anwendungspakets auch dem Computer des Endbenutzers zur Verfügung gestellt.

Der Inhalt des virtuellen Anwendungspakets kann auf einem oder mehreren Application Virtualization-Servern gespeichert werden, damit er bei Bedarf auf die Clients gestreamt und lokal zwischengespeichert werden kann. Dateiserver und Webserver können auch als Streamingserver verwendet werden, oder die Inhalte können direkt auf dem Computer des Endbenutzers abgelegt werden, beispielsweise wenn Sie ein elektronisches Softwareverteilungssystem wie Microsoft Endpoint Configuration Manager verwenden. Bei einer Multi-Server-Implementierung erfordert die Beibehaltung des Paketinhalts und die Aktualität auf allen Streaming-Servern eine umfassende Paketverwaltungslösung. Je nach Größe Ihrer Organisation müssen Sie möglicherweise viele virtuelle Anwendungen für Endbenutzer zugänglich machen, die sich auf der ganzen Welt befinden. Die Verwaltung der Pakete, um sicherzustellen, dass die richtigen Anwendungen allen Benutzern zur Verfügung stehen, wenn Sie Zugriff darauf benötigen, ist daher eine Grundvoraussetzung.

Der Leitfaden zur Planung und Bereitstellung von Application Virtualization bietet Informationen, die Ihnen helfen, die Microsoft Application Virtualization-Anwendung und ihre Komponenten besser zu verstehen und bereitzustellen. Darüber hinaus finden Sie schrittweise Anleitungen zum Implementieren der wichtigsten Bereitstellungsszenarien.

## Inhalt dieses Abschnitts


<a href="" id="planning-for-application-virtualization-system-deployment"></a>[Planen der Bereitstellung von Application Virtualization System](planning-for-application-virtualization-system-deployment.md)  
Bietet die erforderlichen Anleitungen für die Planung der Implementierung und Bereitstellung Ihres Application Virtualization-Systems.

<a href="" id="application-virtualization-deployment-and-upgrade-considerations"></a>[Bereitstellung von Application Virtualization und Upgrade Aspekte](application-virtualization-deployment-and-upgrade-considerations.md)  
Enthält Informationen zu den Hardware-und Softwareanforderungen für die Installation der verschiedenen Application Virtualization-Komponenten sowie Informationen zum Upgrade.

<a href="" id="electronic-software-distribution-based-scenario"></a>[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)  
Enthält Informationen zum Bereitstellen von Application Virtualization mithilfe eines ESD-Systems (Electronic Software Distribution).

<a href="" id="application-virtualization-server-based-scenario"></a>[Application Virtualization Server-basiertes Szenario](application-virtualization-server-based-scenario.md)  
Enthält Informationen zum Bereitstellen von Application Virtualization mithilfe des Application Virtualization Management-Servers.

<a href="" id="stand-alone-delivery-scenario-for-application-virtualization-clients"></a>[Szenario für die eigenständige Bereitstellung für Application Virtualization Clients](stand-alone-delivery-scenario-for-application-virtualization-clients.md)  
Beschreibt, wie Application Virtualization in einem eigenständigen Modus ohne Verwendung von ESD-oder Server basierten Ressourcen bereitgestellt wird.

<a href="" id="application-virtualization-reference"></a>[Application Virtualization-Referenz](application-virtualization-reference.md)  
Enthält detailliertes technisches Referenzmaterial zum Installieren und Verwalten von Systemkomponenten.

 

 





