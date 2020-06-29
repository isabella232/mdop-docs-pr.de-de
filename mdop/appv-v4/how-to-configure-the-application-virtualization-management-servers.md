---
title: So konfigurieren Sie Anwendung Virtualisierung Management Server
description: So konfigurieren Sie Anwendung Virtualisierung Management Server
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807268"
---
# So konfigurieren Sie Anwendung Virtualisierung Management Server


Bevor virtualisierte Anwendungen an den Application Virtualization-Desktop Client oder den Client für Remote Desktop Dienste (vormals Terminal Dienste) gestreamt werden können, muss der Application Virtualization-Verwaltungs Server konfiguriert sein. Wenn Sie den Server konfigurieren, richten Sie das *Inhaltsverzeichnis* ein, in dem die SFT-Dateien geladen und gespeichert werden. Die SFT-Dateien enthalten die virtualisierte Anwendung (oder Anwendungen).

**Wichtig**  Application Virtualization-Server streamen SFT-Dateien mit nur RTSP-oder RTSPS-Protokollen an den Desktop Client und den Client für Remote Desktop Dienste. Die ICO-Datei (Symbol) und die OSD-Datei (Open Software Descriptor) können so konfiguriert werden, dass Sie von einer anderen Datei oder einem anderen HTTP-Server gestreamt wird.

 

**So konfigurieren Sie den Application Virtualization-Verwaltungs Server**

1.  Führen Sie die folgenden Schritte aus:

    [So installieren Sie Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

    **Hinweis**  Während des Installationsvorgangs geben Sie den Speicherort des \\Content-Verzeichnisses auf dem Bildschirm " **Inhaltspfad** " an.

     

2.  Navigieren Sie zu dem Speicherort, den Sie für das \\Content-Verzeichnis angegeben haben, und erstellen Sie bei Bedarf das Verzeichnis.

3.  Wenn das Inhaltsverzeichnis erstellt wird, konfigurieren Sie dieses Verzeichnis als Standarddateifreigabe.

## Verwandte Themen


[Application Virtualization Server-basiertes Szenario](application-virtualization-server-based-scenario.md)

[Systemanforderungen für Application Virtualization](application-virtualization-system-requirements.md)

[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)

[So konfigurieren Sie Server für die serverbasierte Bereitstellung](how-to-configure-servers-for-server-based-deployment.md)

 

 





