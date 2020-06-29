---
title: So konfigurieren Sie Application Virtualization Streaming Server
description: So konfigurieren Sie Application Virtualization Streaming Server
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807260"
---
# So konfigurieren Sie Application Virtualization Streaming Server


Bevor virtuelle Anwendungen an den Application Virtualization-Desktop Client oder den Client für Remote Desktop Dienste (vormals Terminal Dienste) gestreamt werden können, müssen die Application Virtualization Streaming-Server konfiguriert sein. Wenn Sie die Server konfigurieren, richten Sie das *Inhaltsverzeichnis* ein, in dem die SFT-Dateien geladen und gespeichert werden. Die SFT-Dateien enthalten die virtuelle Anwendung (oder Anwendungen).

**Wichtig**  Application Virtualization-Server streamen SFT-Dateien mit nur RTSP-oder RTSPS-Protokollen an den Desktop Client und den Client für Remote Desktop Dienste. Die ICO-Datei (Symbol) und die OSD-Datei (Open Software Descriptor) können so konfiguriert werden, dass Sie von einer anderen Datei oder einem anderen HTTP-Server gestreamt wird.

 

**So konfigurieren Sie die Application Virtualization Streaming Server**

1.  Führen Sie das Installationsverfahren für den Application Virtualization Streaming Server aus. Während des Installationsvorgangs geben Sie den Speicherort des \\Content-Verzeichnisses auf dem Bildschirm " **Inhaltspfad** " an.

2.  Navigieren Sie zu dem Speicherort, den Sie für das \\Content-Verzeichnis angegeben haben, und erstellen Sie bei Bedarf das Verzeichnis.

3.  Wenn das Inhaltsverzeichnis erstellt wird, konfigurieren Sie dieses Verzeichnis als Standarddateifreigabe.

4.  Konfigurieren Sie die NTFS-Dateisystemberechtigungen für das Inhaltsverzeichnis und die Paketordner unter dem Inhaltsverzeichnis. Sie sollten Sicherheitsgruppen in Active Directory-Domänendiensten verwenden, die definieren, welche Benutzer auf jede Anwendung zugreifen können.

## Verwandte Themen


[Application Virtualization Server-basiertes Szenario](application-virtualization-server-based-scenario.md)

[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)

[So konfigurieren Sie Anwendung Virtualisierung Management Server](how-to-configure-the-application-virtualization-management-servers.md)

[So konfigurieren Sie den Dateiserver](how-to-configure-the-file-server.md)

[So konfigurieren Sie den Server für IIS](how-to-configure-the-server-for-iis.md)

 

 





