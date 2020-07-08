---
title: So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung
description: So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807080"
---
# So installieren und konfigurieren Sie die App-V Management Console für eine sicherere Umgebung


Die Standardinstallation der App-V-Verwaltungskonsole umfasst Unterstützung für die sichere Kommunikation. Jede Verwaltungskonsole wird für einzelne Verbindungen konfiguriert, wenn die Konsole zum ersten Mal gestartet wird oder wenn eine Verbindung mit einem zusätzlichen App-V Web Management-Dienst hergestellt wird. Die Standardkonfiguration verwendet SSL über TCP-Port 443. Sie können die Portnummer ändern, wenn die Portnummer auf dem Server geändert wurde. Mithilfe der folgenden Vorgehensweise können Sie eine Verbindung mit einem App-V Web Management-Dienst mithilfe einer sicheren Verbindung herstellen.

**Herstellen einer Verbindung zu einem App-V-Verwaltungsdienst mithilfe einer SSL-Verbindung**

1.  Starten Sie die Application Virtualization-Verwaltungskonsole.

2.  Klicken Sie im Bereich Aktionen der Konsole auf **Verbindung konfigurieren** .

3.  Geben Sie den **Hostnamen des Webdiensts**ein, und stellen Sie sicher, dass **sichere Verbindung verwenden** ausgewählt ist.

    **Wichtig**  Der im Hostnamen des Webdiensts angegebene Name muss mit dem allgemeinen Namen im Zertifikat übereinstimmen, oder die Verbindung schlägt fehl.

     

4.  Wählen Sie die entsprechenden Anmeldeinformationen aus, und klicken Sie auf **OK**.

## Verwandte Themen


[Konfigurieren von Zertifikaten zur Unterstützung des App-V Web Management Service](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 





