---
title: Konfigurieren von Windows Server 2008 für App-V Management Server
description: Konfigurieren von Windows Server 2008 für App-V Management Server
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807220"
---
# Konfigurieren von Windows Server 2008 für App-V Management Server


Auf dem Windows Server 2008-Server, auf dem Sie den Microsoft Application Virtualization (App-V)-Verwaltungs-Webdienst installieren, müssen Internet Informationsdienste (IIS) als Rolle auf dem Server installiert sein. Gehen Sie wie folgt vor, um Windows Server 2008 so zu konfigurieren, dass die APP-vserver-Installation unterstützt wird.

**So installieren Sie IIS auf einem Windows Server2008-Computer**

1.  Klicken Sie auf dem Windows Server2008-Computer auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Server-Manager** , um den Server-Manager zu starten. Klicken Sie im Server-Manager mit der rechten Maustaste auf den Knoten **Rollen** , und klicken Sie auf **Rollen hinzufügen** , um den **Assistenten zum Hinzufügen von Rollen**zu starten.

2.  Wählen Sie im **Assistenten zum Hinzufügen von Rollen**auf der Seite **Server Rollen auswählen** die Option **Webserver (IIS)** aus. Wenn Sie dazu aufgefordert werden, klicken Sie auf **erforderliche Features hinzufügen** , um die abhängigen Features hinzuzufügen.

3.  Klicken Sie auf der Seite **Server Rollen auswählen** auf **weiter**, und klicken Sie dann erneut auf **weiter** .

4.  Klicken Sie im **Assistenten zum Hinzufügen von Rollen**auf der Seite **Rollendienste auswählen** auf:

    1.  Wählen Sie unter **Anwendungsentwicklung**die Option **ASP.net** aus, und klicken Sie bei der entsprechenden Aufforderung auf **Erforderliche Rollendienste hinzufügen** , um die Dienste und Features der abhängigen Rollen hinzuzufügen.

    2.  Wählen Sie unter **Sicherheit**die Option **Windows-Authentifizierung**aus.

    3.  Wählen Sie im Knoten **Verwaltungstools** die Option **IIS-Verwaltungsskripts und-Tools**aus. Stellen Sie unter **IIS6-Verwaltungskompatibilität**sicher, dass sowohl die **IIS6-Metabase-Kompatibilität** als auch die IIS6-WMI- **Kompatibilität** ausgewählt sind, und klicken Sie dann auf **weiter**.

5.  Klicken Sie auf der Seite **Installationsauswahl bestätigen** auf **Installieren**, und führen Sie dann den restlichen Assistenten aus.

6.  Klicken Sie auf **Schließen** , um den **Assistenten zum Hinzufügen von Rollen**zu beenden, und schließen Sie dann Server-Manager.

## Verwandte Themen


[Bereitstellungsanforderungen für Application Virtualization](application-virtualization-deployment-requirements.md)

[Bereitstellung und Upgrade von Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





