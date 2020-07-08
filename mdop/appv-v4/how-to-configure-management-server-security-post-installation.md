---
title: So konfigurieren Sie Management Server Security-Nachinstallation
description: So konfigurieren Sie Management Server Security-Nachinstallation
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807307"
---
# So konfigurieren Sie Management Server Security-Nachinstallation


Verwenden Sie die APP-v-Verwaltungskonsole, um das Zertifikat hinzuzufügen und den App-v-Verwaltungs Server für erhöhte Sicherheit zu konfigurieren. Mit dem folgenden Verfahren können Sie die Sicherheits nach Installation konfigurieren.

**So konfigurieren Sie die nach Installation von Management Server-Sicherheit**

1.  Öffnen Sie die APP-v-Verwaltungskonsole, und stellen Sie eine Verbindung mit dem **Verwaltungsdienst** mit App-v-Administratorprivilegien her.

2.  Erweitern Sie den Server, erweitern Sie **Servergruppen**, und wählen Sie dann die entsprechende Servergruppe aus, für die der Verwaltungsserver registriert wurde.

3.  Klicken Sie mit der rechten Maustaste auf das Verwaltungs Server Objekt, und wählen Sie **Eigenschaften**aus.

4.  Klicken Sie auf der Registerkarte **Ports** auf **Server Zertifikat** , und schließen Sie den Assistenten ab, um das ordnungsgemäß bereitgestellte Zertifikat auszuwählen.

    **Hinweis**  Wenn im Assistenten keine Zertifikate angezeigt werden, wurde kein Zertifikat bereitgestellt, oder das Zertifikat erfüllt die Anforderungen von App-V.

     

5.  Klicken Sie auf **weiter** , um zur Seite **Willkommen beim Zertifikat-Assistenten** weiter zu gehen.

6.  Wählen Sie im Bildschirm **Verfügbare Zertifikate** das richtige Zertifikat aus.

7.  Klicken Sie auf **Fertig stellen**.

8.  Nachdem Sie den Assistenten abgeschlossen haben, löschen Sie **RTSP** als verfügbaren Abhör-Port. Dadurch wird verhindert, dass Verbindungen über einen nicht sicheren Kommunikationskanal hergestellt werden.

9.  Klicken Sie auf über **nehmen**, und starten Sie den **Microsoft Virtual Application Server** -Dienst erneut. Verwenden Sie das MMC-Snap-in des Diensts, um diese Aufgabe auszuführen.

## Verwandte Themen


[So konfigurieren Sie die Streaming Server Security-Nachinstallation](how-to-configure-streaming-server-security-post-installation.md)

[Behandeln von Problemen mit Zertifikatberechtigungen](troubleshooting-certificate-permission-issues.md)

 

 





