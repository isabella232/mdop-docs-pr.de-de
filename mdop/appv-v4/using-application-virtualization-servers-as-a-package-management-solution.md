---
title: Verwenden von Application Virtualization-Servern als Paketverwaltungslösung
description: Verwenden von Application Virtualization-Servern als Paketverwaltungslösung
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806180"
---
# Verwenden von Application Virtualization-Servern als Paketverwaltungslösung


Wenn Sie nicht über ein vorhandenes ESD-System zum Bereitstellen Ihrer Application Virtualization-Lösung verfügen oder keines verwenden möchten, müssen Sie einen oder mehrere Application Virtualization Management-Server als Kern ihrer Systemarchitektur installieren. Der Application Virtualization Management-Server erfordert einen dedizierten Server Computer und benötigt eine Microsoft SQL Server-Datenbank. Die Datenbank kann sich auf demselben Server befinden oder auf einem Unternehmensdatenbankserver konfiguriert werden, auf den der Application Virtualization Management-Server über eine Hochgeschwindigkeits-LAN-Verbindung zugreifen kann. Darüber hinaus müssen Sie die Microsoft Application Virtualization Management Console entweder auf dem Application Virtualization-Verwaltungsserver oder auf einer bestimmten Verwaltungsarbeitsstation installieren, und Sie müssen den Microsoft Application Virtualization Management Web Service installieren, der auch auf dem Application Virtualization Management Server oder auf einem separaten IIS-Server installiert werden kann. Die Application Virtualization-Verwaltungskonsole wird zum Herstellen einer Verbindung mit dem Application Virtualization Management Web Service verwendet, sodass der System Administrator mit dem Application Virtualization Management Server interagieren kann.

**Hinweis**  Der Zugriff auf die Anwendungen wird mithilfe von Sicherheitsgruppen in den Active Directory-Domänendiensten gesteuert, sodass Sie einen Prozess planen müssen, um eine Sicherheitsgruppe für jede virtualisierte Anwendung einzurichten und zu verwalten, welche Benutzer zu jeder Gruppe hinzugefügt werden. Der Application Virtualization Management Server-Administrator konfiguriert den Server für die Verwendung dieser Active Directory-Gruppen, und der Server steuert dann automatisch den Zugriff auf die Pakete basierend auf der Active Directory-Gruppenmitgliedschaft.

 

## Inhalt dieses Abschnitts


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[Übersicht über die Application Virtualization-Systemkomponenten](overview-of-the-application-virtualization-system-components.md)  
Listet die primären Komponenten des Microsoft Application Virtualization-Verwaltungssystems auf und beschreibt sie.

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
Bietet einen kurzen Überblick darüber, wie virtuelle Anwendungen in einem Server basierten Bereitstellungsszenario für Application Virtualization veröffentlicht werden.

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
Beschreibt die verfügbaren Optionen für die Verwendung von Application Virtualization Streaming Servern in Verbindung mit ihrer auf Application Virtualization Management Server basierenden Implementierung.

## Verwandte Themen


[Application Virtualization Server-basiertes Szenario](application-virtualization-server-based-scenario.md)

[Planen der Bereitstellung von Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

 

 





