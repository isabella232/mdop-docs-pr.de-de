---
title: So konfigurieren Sie den Server für IIS
description: So konfigurieren Sie den Server für IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807228"
---
# So konfigurieren Sie den Server für IIS


Bevor virtuelle Anwendungen an den Application Virtualization-Desktop Client und den Client für Remote Desktop Dienste (vormals Terminal Dienste) gestreamt werden können, müssen die IIS-Server konfiguriert sein. Wenn Sie die Server konfigurieren, richten Sie das Inhaltsverzeichnis ein, in dem die SFT-Dateien geladen und gespeichert werden. Die SFT-Dateien enthalten die virtuelle Anwendung (oder Anwendungen).

**So konfigurieren Sie das Inhaltsverzeichnis auf dem IIS-Server**

1.  Suchen Sie auf dem Server, auf dem IIS ausgeführt wird, nach dem Verzeichnis, das Sie als Inhaltsverzeichnis verwenden möchten, oder erstellen Sie das Verzeichnis, falls es nicht vorhanden ist. Konfigurieren Sie dieses Verzeichnis als Standarddateifreigabe.

2.  Öffnen Sie auf dem Server, auf dem IIS ausgeführt wird, **IIS-Manager**, und erstellen Sie unter der Standardwebsite ein virtuelles Verzeichnis, das dem Inhaltsverzeichnis entspricht, das Sie auf dem Server erstellt haben. Vergewissern Sie sich, dass " **Lesen** " aktiviert ist.

3.  Geben Sie dem neu erstellten virtuellen Verzeichnis den Alias **Inhalt**.

4.  Akzeptieren Sie alle anderen Standardeinstellungen für dieses virtuelle Verzeichnis.

5.  Konfigurieren Sie die NTFS-Dateisystemberechtigungen für das Inhaltsverzeichnis und die Paketordner unter dem Inhaltsverzeichnis, indem Sie die Sicherheitsgruppen in den Active Directory-Domänendiensten verwenden, die Sie zuvor definiert haben.

**Hinweis**  Wenn Sie IIS zum Veröffentlichen der ICO-und OSD-Dateien verwenden, müssen Sie einen MIME-Typ für OSD = txt konfigurieren. Andernfalls dient IIS nicht für die ICO-und OSD-Dateien für Clients. Wenn Sie IIS zum Veröffentlichen von Paketen (SFT-Dateien) verwenden, müssen Sie einen MIME-Typ für SFT = Binary konfigurieren. Andernfalls dient IIS nicht für die SFT-Dateien für Clients.

 

## Verwandte Themen


[Application Virtualization Server-basiertes Szenario](application-virtualization-server-based-scenario.md)

[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)

[So konfigurieren Sie Anwendung Virtualisierung Management Server](how-to-configure-the-application-virtualization-management-servers.md)

[So konfigurieren Sie Application Virtualization Streaming Server](how-to-configure-the-application-virtualization-streaming-servers.md)

[So konfigurieren Sie den Dateiserver](how-to-configure-the-file-server.md)

 

 





