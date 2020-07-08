---
title: So installieren Sie Application Virtualization Sequencer
description: So installieren Sie Application Virtualization Sequencer
author: dansimp
ms.assetid: 89cdf60d-18b0-4204-aa9f-b402610f8f0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a6fe03f2149504b6c34c70b2b82ce2ba0b55ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807055"
---
# So installieren Sie Application Virtualization Sequencer


Der Microsoft Application Virtualization Sequencer überwacht und zeichnet den Installations-und Einrichtungsprozess für Anwendungen auf, damit die Anwendung als virtuelle Anwendung ausgeführt werden kann. Installieren Sie den Sequencer auf einem Computer, auf dem nur das Betriebssystem installiert ist. Alternativ können Sie den Sequencer auf einem Computer mit einer virtuellen Umgebung installieren – beispielsweise Microsoft Virtual PC. Diese Methode ist hilfreich, da es einfacher ist, eine saubere Sequenz Umgebung beizubehalten, die mit minimaler zusätzlicher Konfiguration wieder verwendet werden kann.

Sie müssen über Administratorrechte auf dem Computer verfügen, den Sie zum Sequenzieren der Anwendung verwenden, und auf dem Computer darf keine Version des Application Virtualization (App-V)-Clients ausgeführt werden. Das Erstellen einer virtuellen Anwendung mithilfe des Sequencers ist sehr ressourcenintensiv, daher ist es wichtig, dass Sie den Sequencer auf einem Computer installieren, der die empfohlenen Anforderungen erfüllt oder überschreitet. Das Ausführen des App-V-Sequencers im abgesicherten Modus wird nicht unterstützt. Weitere Informationen zu den Systemanforderungen finden Sie unter [Application Virtualization System Requirements](application-virtualization-system-requirements.md).

**Wichtig**  Nachdem Sie eine Anwendung sequenziert haben, müssen Sie das Betriebssystem und den Sequencer auf dem Computer, den Sie für die Sequenz Anwendung verwenden, erneut installieren, bevor Sie eine neue Anwendung ordnungsgemäß ablaufen können.

 

**So installieren Sie den Microsoft Application Virtualization Sequencer**

1.  Kopieren Sie die Installationsdateien von Microsoft Application Virtualization Sequencer auf den Computer, auf dem Sie Sie installieren möchten.

2.  Wählen Sie **setup.exe**aus, um den Installations-Assistenten für Microsoft Application Virtualization Sequencer zu starten. Wenn das **Microsoft Visual C++ SP1-verteilbare Paket (x86)** vor der Installation nicht erkannt wird, wird es von **setup.exe** installiert.

3.  Klicken Sie auf der Seite **Willkommen** auf **weiter**.

4.  Wenn Sie auf der Seite " **Lizenzvertrag** " die Bedingungen des Lizenzvertrags akzeptieren möchten, wählen Sie **Ich akzeptiere die Bedingungen des Lizenzvertrags**. Klicken Sie auf **Weiter**.

5.  Klicken Sie auf der Seite **Zielordner** auf **weiter**, um den Standardinstallationsordner zu übernehmen. Wenn Sie einen anderen Zielordner angeben möchten, klicken Sie auf **ändern** , und geben Sie den Installationsordner an, der für die Installation verwendet wird. Klicken Sie auf **Weiter**.

6.  Klicken Sie auf der Seite **bereit zum Installieren des Programms** auf **Installieren**, um die Installation zu starten.

7.  Klicken Sie auf der Seite **abgeschlossen des InstallShield-Assistenten** auf **Fertig stellen**, um den Installations-Assistenten zu schließen und den Sequencer zu öffnen. Wenn Sie den Installations-Assistenten schließen möchten, ohne den Sequencer zu öffnen, deaktivieren Sie **Programm starten** , und klicken Sie auf **Fertig stellen**.

## Verwandte Themen


[So aktualisieren Sie Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)

[Bereitstellungsanforderungen für Application Virtualization](application-virtualization-deployment-requirements.md)

 

 





