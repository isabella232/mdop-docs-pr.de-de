---
title: Installieren von Anwendungen auf einem virtuellen Windows-PC-Image
description: Installieren von Anwendungen auf einem virtuellen Windows-PC-Image
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811992"
---
# Installieren von Anwendungen auf einem virtuellen Windows-PC-Image


Nachdem Sie ein Windows Virtual PC-Abbild für die Verwendung mit Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 erstellt haben, können Sie andere Komponenten installieren, die bei der Ausführung von Med-v hilfreich sind, beispielsweise ein ESD-System (Electronic Software Distribution) und eine Antivirus-Software.

Der folgende Abschnitt enthält Informationen, die Sie bei der Installation von Software auf dem MED-V-Abbild unterstützen.

**Vorsicht**  Um die Verwaltung von Med-v Workspace nach der Bereitstellung zu vereinfachen, empfehlen wir, die Anzahl der Komponenten, die Sie auf dem Med-v-Abbild installieren, auf die Komponenten zu begrenzen, die erforderlich sind oder die bei Verwendung von Med-v hilfreich sind. Wenn Sie beispielsweise nicht für med-v erforderlich sind, können Sie ein ESD-System installieren, um es später für die Installation von Anwendungen in einem Med-v-Arbeitsbereich und einer Antivirensoftware zur Sicherheit des Bilds zu verwenden.

 

**Installieren von Software auf einem MED-V-Abbild**

1.  Wenn es derzeit nicht ausgeführt wird, öffnen Sie den virtuellen MED-V-Computer.

    1.  Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Windows Virtual PC** , und klicken Sie dann auf **Windows Virtual PC**.

    2.  Doppelklicken Sie auf den virtuellen MED-V-Computer.

2.  Suchen Sie im Betriebssystem des virtuellen Computers die Installationsdateien für die Software, die Sie installieren möchten.

3.  Befolgen Sie die Installationsanweisungen, die vom Softwarehersteller bereitgestellt werden.

    **Hinweis**  Nachdem die Installation abgeschlossen ist, müssen Sie möglicherweise den virtuellen Computer schließen und neu starten.

     

Wiederholen Sie diese Schritte für jede Software oder Anwendung, die Sie auf dem MED-V-Abbild installieren möchten. Wir empfehlen, dass Sie die Anzahl der Anwendungen begrenzen, die Sie auf dem Bild vorinstallieren. Die empfohlene Vorgehensweise zum Installieren von Anwendungen und anderer Software auf dem Bild besteht darin, jetzt ein ESD-System vorinstallieren und es später zum Bereitstellen von Software auf dem Bild zu verwenden. Alternativ können Sie auch Gruppenrichtlinien oder App-v verwenden, um Anwendungen in einem Med-v-Arbeitsbereich hinzuzufügen oder zu entfernen. Weitere Informationen finden Sie unter [Verwalten von Anwendungen, die in MED-V-Arbeitsbereichen bereitgestellt werden](managing-applications-deployed-to-med-v-workspaces.md).

Weitere Informationen dazu, wie Sie Software auf einem virtuellen Bild installieren, finden Sie in den folgenden Artikeln:

-   [Veröffentlichen und Verwenden von virtuellen Anwendungen](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .

-   [Hilfe zu Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

Nachdem Sie alle gewünschten Software auf dem MED-V-Bild installiert haben, kann Ihr Bild verpackt werden.

## Verwandte Themen


[Konfigurieren eines virtuellen Windows-PC-Images für MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

[Vorbereiten eines MED-V-Images](prepare-a-med-v-image.md)

 

 





