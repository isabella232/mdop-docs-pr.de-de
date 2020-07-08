---
title: Übersicht über Electronic Software Distribution-basierte Szenarien
description: Übersicht über Electronic Software Distribution-basierte Szenarien
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808851"
---
# Übersicht über Electronic Software Distribution-basierte Szenarien


Wenn Sie beabsichtigen, eine ESD-Lösung (Electronic Software Distribution) für die Bereitstellung virtueller Anwendungen zu verwenden, ist es wichtig, die Faktoren zu verstehen, die in diese Entscheidung eingehen und davon betroffen sind. In diesem Thema werden die Vorteile der Verwendung eines ESD-basierten Szenarios beschrieben, und es werden Informationen zu den Veröffentlichungs-und Paketstreaming-Methoden bereitgestellt, die Sie beim Fortsetzen der Bereitstellung in Frage stellen müssen.

**Wichtig**  Je nachdem, welche ESD-Lösung Sie verwenden, müssen Sie mit den Anforderungen ihrer jeweiligen Lösung vertraut sein. Wenn Sie den Microsoft Endpoint Configuration Manager verwenden, lesen Sie die Configuration Manager-Dokumentation unter <https://go.microsoft.com/fwlink/?LinkId=66999> .

 

Die Verwendung eines vorhandenen ESD-Systems bietet Ihnen folgende Vorteile:

-   Beseitigt duale Verwaltungsinfrastrukturen

-   Senkt die Kosten zusätzlicher Hardware

-   Geringere Kosten für zusätzliche Betriebssystem-und Datenbanklizenzen

## Veröffentlichungsmethoden


Bei Verwendung eines ESD-basierten Szenarios haben Sie die folgenden Möglichkeiten, die Anwendung auf den Clients zu veröffentlichen:

-   **Eigenständiger Windows Installer.** Die Windows Installer-Datei enthält das Manifest und die OSD-und ICO-Dateien, die die Clients verwenden, um ein Paket zu konfigurieren. Die Windows Installer-Datei kopiert auch die SFT-Datei auf den Client, da dieses Szenario keinen Server verwendet.

-   **Windows Installer mit dem Paketmanifest.** Die Windows Installer-Datei enthält das Manifest und die OSD-und ICO-Dateien, die die Clients verwenden, um ein Paket zu konfigurieren. Die SFT-Datei wird auf einem Server gespeichert. Ein Befehlszeilenparameter leitet den Client an den Speicherort der SFT-Datei weiter.

-   **SFTMIME-Befehle.** SFTMIME-Befehle werden mit den Manifest-, OSD-, ICO-und SFT-Dateien verwendet, um dem Clientpakete hinzuzufügen. Die Manifestdatei muss sich auf dem Clientcomputer befinden, oder es muss über einen UNC-Pfad zugegriffen werden können. Je nach Clientkonfiguration und Befehlszeilenoptionen können sich die OSD-, ICO-und SFT-Dateien auf dem Clientcomputer oder auf einem Server befinden.

Ausführlichere Informationen zu den vorangehenden Veröffentlichungsmethoden finden Sie unter [Ermitteln der Veröffentlichungsmethode](determine-your-publishing-method.md).

## Streaming-Methoden für Pakete


Sie müssen die Methode ermitteln, die Ihr Application Virtualization System zum Streamen der virtuellen Anwendungspakete oder SFT-Dateien vom Server an die Clients verwenden wird. Die folgenden Streaming-Optionen stehen zur Verfügung:

-   **Application Virtualization Streaming Server.** Wenn Sie in Ihrer Konfiguration einen Application Virtualization Streaming Server verwenden, werden die SFT-Dateien über RTSP-oder RTSPS-Protokolle an die Clients von diesem Server gestreamt. Sie müssen die Server Software auf einem Computer installieren, und Sie müssen Sie über die Registrierung konfigurieren, aber diese Konfiguration ist nicht von Diensten wie SQL-oder Active Directory-Domänendiensten abhängig. Die SFT-Dateien werden auf dem Server an einem Speicherort gespeichert, auf den die Clients zugreifen können. Veröffentlichungsinformationen können über einen beliebigen Verteilungsmechanismus an die Clients verteilt werden. Bei der Konfiguration erhält der Client jedoch automatisch Paketaktualisierungen, und das aktive Upgrade wird unterstützt.

-   **Application Virtualization-Verwaltungs Server.** Wenn Sie in Ihrer Konfiguration einen Application Virtualization Management Server verwenden, werden die SFT-Dateien über RTSP-oder RTSPS-Protokolle an die Clients von diesem Server gestreamt. Sie können diesen Server über die Application Virtualization Management Console verwalten. Diese Konfiguration verwendet eine SQL-Datenbank und Active Directory-Dienste. Der Server kann Veröffentlichungsinformationen an die Clients verteilen, sodass keine zusätzlichen Veröffentlichungsmechanismen erforderlich sind.

-   **Dateiserver.** Wenn Sie einen Dateiserver in Ihrer Konfiguration verwenden, werden die SFT-Dateien mithilfe von SMB-Protokollen an die anderen Clientcomputer gestreamt. Die in dieser Konfiguration verwendeten Dateiserver werden verwaltet, indem Zugriffssteuerungslisten für die Dateifreigaben und SFT-Dateien erstellt werden. Es muss darauf geachtet werden, dass die Clients an die richtigen Dateien auf dem Dateiserver weitergeleitet werden.

-   **IIS-Server.** Wenn Sie einen IIS-Server in Ihrer Konfiguration verwenden, werden die SFT-Dateien über HTTP-oder HTTPS-Protokolle an die Clients von diesem Server gestreamt. Der IIS-Server kann einfach konfiguriert und verwaltet werden. Es muss darauf geachtet werden, dass die Clients an die richtigen Dateien auf dem IIS-Server weitergeleitet werden.

Ausführlichere Informationen zu den vorhergehenden Streaming-Methoden finden Sie unter [Ermitteln der Streaming-Methode](determine-your-streaming-method.md).

## Verwandte Themen


[Befehlszeilenparameter von Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md)

[Application Virtualization Server-basiertes Szenario](application-virtualization-server-based-scenario.md)

[Bestimmen der Veröffentlichungsmethode](determine-your-publishing-method.md)

[Bestimmen der Streaming-Methode](determine-your-streaming-method.md)

[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)

[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)

 

 





