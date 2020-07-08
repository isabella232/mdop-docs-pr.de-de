---
title: So konfigurieren Sie den Dateiserver
description: So konfigurieren Sie den Dateiserver
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807244"
---
# So konfigurieren Sie den Dateiserver


Mit dem folgenden Verfahren können Sie einen lokalen Computer konfigurieren, der als Dateifreigabe-und Datenstrom Anwendungen für den Application Virtualization-Desktop Client und den Client für Remote Desktop Dienste (vormals Terminal Dienste) verwendet wird. Dieses Szenario wird verwendet, wenn Sie Ihrer vorhandenen Hardwareumgebung keine zusätzliche Serverinfrastruktur hinzufügen möchten.

Wenn Sie einen Application Virtualization Management Server als Verteilungspunkt für die Dateifreigabe verwenden, die in lokalen Niederlassungen installiert ist, müssen Sie diesen Server konfigurieren, bevor virtuelle Anwendungen auf die Computer gestreamt werden können, die als Dateifreigaben verwendet werden. Wenn Sie die Server und die Dateifreigaben konfigurieren, müssen Sie das Inhaltsverzeichnis einrichten, in dem die SFT-Dateien geladen und gespeichert werden. Die SFT-Dateien enthalten die virtuelle Anwendung (oder Anwendungen).

**Wichtig**  Damit Anwendungen ordnungsgemäß an den Application Virtualization-Desktop Client und den Client für Remote Desktop Dienste gestreamt werden können, strömt die SFT-Datei aus dem Inhaltsverzeichnis auf dem Server, auf dem Sie die virtuelle Anwendung speichern, aus. die ICO-Datei (Symbol) und die OSD-Datei (Open Software Descriptor) können so konfiguriert werden, dass Sie von einem anderen Server gestreamt wird.

 

**So konfigurieren Sie den Application Virtualization-Dateiserver**

1.  Führen Sie das folgende Installationsverfahren aus, um den als Verteilungspunkt verwendeten Server zu konfigurieren:

    [So installieren Sie Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

    **Hinweis**  Während des Installationsvorgangs geben Sie den Speicherort des \\Content-Verzeichnisses auf dem Bildschirm " **Inhaltspfad** " an.

     

2.  Erstellen Sie auf jedem Computer, den Sie als Dateifreigabe verwenden, ein \\Content-Verzeichnis, das dem beim Installieren des Servers angegebenen Verzeichnis entspricht.

    **Wichtig**  Konfigurieren Sie die Application Virtualization-Desktop Clients so, dass Anwendungen von dem Computer, den Sie als Dateifreigabe verwenden, und nicht von einem Application Virtualization Server oder IIS-Server gestreamt werden.

     

3.  Wenn das \\Content-Verzeichnis erstellt wird, konfigurieren Sie dieses Verzeichnis als Standarddateifreigabe.

## Verwandte Themen


[Application Virtualization Server-basiertes Szenario](application-virtualization-server-based-scenario.md)

[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)

[So konfigurieren Sie Anwendung Virtualisierung Management Server](how-to-configure-the-application-virtualization-management-servers.md)

[So konfigurieren Sie Application Virtualization Streaming Server](how-to-configure-the-application-virtualization-streaming-servers.md)

[So konfigurieren Sie den Server für IIS](how-to-configure-the-server-for-iis.md)

 

 





