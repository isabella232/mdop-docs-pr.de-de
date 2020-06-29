---
title: So konfigurieren Sie Windows Server 2003 Firewall für App-V
description: So konfigurieren Sie Windows Server 2003 Firewall für App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807223"
---
# So konfigurieren Sie Windows Server 2003 Firewall für App-V


Gehen Sie wie folgt vor, um die Windows Server 2003-Firewall für App-V zu konfigurieren.

**So konfigurieren Sie die Windows Server 2003-Firewall für App-V**

1.  Öffnen Sie in der **System**Steuerung die **Windows-Firewall**.

    **Hinweis**  Wenn der Server nicht so konfiguriert ist, dass der Firewalldienst vor diesem Schritt ausgeführt wird, werden Sie aufgefordert, den Firewalldienst zu starten.

     

2.  Wenn ICO-und OSD-Dateien über SMB veröffentlicht werden, stellen Sie sicher, dass die **Datei-und Druckerfreigabe** auf der Registerkarte **Ausnahmen** aktiviert ist.

    **Hinweis**  Wenn ICO-und OSD-Dateien über HTTP/HTTPS auf dem Verwaltungs Server veröffentlicht werden, müssen Sie möglicherweise eine Ausnahme für http oder HTTPS hinzufügen. Wenn der IIS-Server, der die ICO-und OSD-Dateien hostet, auf einem Computer gehostet wird, der vom Verwaltungsserver getrennt ist, müssen Sie die Ausnahme diesem Computer hinzufügen. Um die Leistung zu maximieren, sollten Sie die ICO-und OSD-Dateien auf einem separaten Server vom Verwaltungsserver hosten.

     

3.  Fügen Sie eine Programmausnahme für hinzu `sghwdsptr.exe` , die die ausführbare Verwaltungs Server-Dienstdatei ist. Der Standardpfad zu dieser ausführbaren Datei ist `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

    **Hinweis**  Wenn der Verwaltungs Server RTSP für die Kommunikation verwendet, müssen Sie auch eine Programmausnahme für hinzufügen `sghwsvr.exe` .

    Der App-V Streaming-Server erfordert eine Programmausnahme `sglwdsptr.exe` für die RTSPS-Kommunikation. Der App-V-Streamingserver, der RTSP für die Kommunikation verwendet, erfordert auch eine Programmausnahme für `sglwsvr.exe` .

     

4.  Stellen Sie sicher, dass der richtige Bereich für jede Ausnahme konfiguriert ist. Um das Risiko zu verringern, entfernen Sie jeden Computer, und begrenzen Sie die IP-Adressen, auf die der Server antwortet.

## Verwandte Themen


[So konfigurieren Sie Windows Server 2008 Firewall für App-V](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





