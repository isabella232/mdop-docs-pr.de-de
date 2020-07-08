---
title: So installieren Sie den Sequencer
description: So installieren Sie den Sequencer
author: dansimp
ms.assetid: 2cd16427-a0ba-4870-82d1-3e3c79e1959b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 75a0f987fcc76d1ed92631085a4364ae6e06c9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807039"
---
# So installieren Sie den Sequencer


Der Microsoft Application Virtualization (App-V)-Sequenzer überwacht und zeichnet den Installations-und Einrichtungsprozess für Anwendungen auf, damit die Anwendung als virtuelle Anwendung ausgeführt werden kann. Installieren Sie den Sequencer auf einem Computer, auf dem nur das Betriebssystem installiert ist. Alternativ können Sie den Sequencer auf einem Computer mit einer virtuellen Umgebung installieren – beispielsweise Microsoft Virtual PC. Diese Methode ist hilfreich, da es einfacher ist, eine saubere Sequenz Umgebung beizubehalten, die mit minimaler zusätzlicher Konfiguration wieder verwendet werden kann.

Sie müssen über Administratorrechte auf dem Computer verfügen, den Sie verwenden, um die Anwendung zu sequenzieren, und der Computer muss mit dem Netzwerk verbunden sein. Auf dem Computer darf keine Version des Application Virtualization (App-V)-Clients ausgeführt werden. Das Erstellen einer virtuellen Anwendung mithilfe des Sequencers ist sehr ressourcenintensiv, daher ist es wichtig, dass Sie den Sequencer auf einem Computer installieren, der die empfohlenen Anforderungen erfüllt oder überschreitet. Weitere Informationen zu den Systemanforderungen finden Sie unter [Hardware-und Software Anforderungen für Sequencer](sequencer-hardware-and-software-requirements.md)..

**So installieren Sie den Microsoft Application Virtualization Sequencer**

1.  Kopieren Sie die Installationsdateien von Microsoft Application Virtualization Sequencer auf den Computer, auf dem Sie Sie installieren möchten.

2.  Wählen Sie **setup.exe**aus, um den Installations-Assistenten für Microsoft Application Virtualization Sequencer zu starten. Wenn das **Microsoft Visual C++ SP1-verteilbare Paket (x86)** vor der Installation nicht erkannt wird, wird es von **setup.exe** installiert.

3.  Klicken Sie auf der Seite **Willkommen** auf **weiter**.

4.  Wenn Sie auf der Seite " **Lizenzvertrag** " die Bedingungen des Lizenzvertrags akzeptieren möchten, wählen Sie **Ich akzeptiere die Bedingungen des Lizenzvertrags**. Klicken Sie auf **Weiter**.

5.  Klicken Sie auf der Seite **Zielordner** auf **weiter**, um den Standardinstallationsordner zu übernehmen. Wenn Sie einen anderen Zielordner angeben möchten, klicken Sie auf **ändern** , und geben Sie den Installationsordner an, der für die Installation verwendet wird. Klicken Sie auf **Weiter**.

6.  Klicken Sie auf der Seite **bereit zum Installieren des Programms** auf **Installieren**, um die Installation zu starten.

7.  Klicken Sie auf der Seite **abgeschlossen des InstallShield-Assistenten** auf **Fertig stellen**, um den Installations-Assistenten zu schließen und den Sequencer zu öffnen. Wenn Sie den Installations-Assistenten schließen möchten, ohne den Sequencer zu öffnen, deaktivieren Sie **Programm starten** , und klicken Sie auf **Fertig stellen**.

## Verwandte Themen


[Konfigurieren von Application Virtualization Sequencer](configuring-the-application-virtualization-sequencer.md)

 

 





