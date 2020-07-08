---
title: Konfigurieren der Firewall für App-V Server
description: Konfigurieren der Firewall für App-V Server
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808983"
---
# Konfigurieren der Firewall für App-V Server


Nachdem Sie den Microsoft Application Virtualization (App-V)-Verwaltungsserver oder Streamingserver installiert und für die Verwendung des RTSP-oder RTSPS-Protokolls konfiguriert haben, müssen Sie für die APP-v-Programme Firewall-Ausnahmen erstellen.

## Konfigurieren von Firewall-Ausnahmen für Application Virtualization Management Server


Erstellen Sie eine Firewall-Ausnahme für **sghwdsptr.exe** und **sghwsvr.exe**. Diese Programme finden Sie im Ordner c:\\Programme c:\\Programme\\Microsoft System Center App virt Management Server\\App virt Management Server\\bin auf einem 32-Bit-Betriebssystem. Wenn Sie eine 64-Bit-Version des Betriebssystems verwenden, befindet sich der Ordner unter c:\\Programme Files (x86) \\Microsoft System Center App virt Management Server\\App virt Management Server\\bin.

## Konfigurieren von Firewall-Ausnahmen für Application Virtualization Streaming Server


Erstellen Sie eine Firewall-Ausnahme für **sglwdsptr.exe** und **sglwsvr.exe**. Diese Programme finden Sie im Ordner c:\\Programme c:\\Programme\\Microsoft System Center App virt Streaming Server\\App virt-Streaming Server\\bin auf einem 32-Bit-Betriebssystem. Wenn Sie eine 64-Bit-Betriebssystemversion verwenden, befindet sich der Ordner unter c:\\Programme-Dateien (x86) \\Microsoft System Center-App virt-Streaming Server\\App virt-Streaming Server\\bin.

## Verwandte Themen


[So konfigurieren Sie Server für die serverbasierte Bereitstellung](how-to-configure-servers-for-server-based-deployment.md)

[So installieren und konfigurieren Sie die Standardanwendung](how-to-install-and-configure-the-default-application.md)

 

 





