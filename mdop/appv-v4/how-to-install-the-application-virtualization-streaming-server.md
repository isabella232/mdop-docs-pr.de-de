---
title: So installieren Sie die Application Virtualization Streaming Server
description: So installieren Sie die Application Virtualization Streaming Server
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807063"
---
# So installieren Sie die Application Virtualization Streaming Server


Der Application Virtualization Streaming Server veröffentlicht seine Anwendungen für Clients. In einer Umgebung mit Lastenausgleich, die für große Bereitstellungen typisch ist, sollten alle Server in einer Servergruppe dieselben Anwendungen streamen. Wenn Application Virtualization Streaming-Server verschiedene Anwendungen streamen sollen, weisen Sie die Server verschiedenen Servergruppen zu. In diesem Fall müssen Sie möglicherweise auch die Kapazität einer Servergruppe erhöhen.

Wenn Sie einen Zielcomputer im Netzwerk festgelegt haben, mit einem Anmeldekonto, das über lokale Administratorrechte verfügt, können Sie mit dem folgenden Verfahren den Application Virtualization Streaming Server installieren und der entsprechenden Servergruppe zuweisen.

**Hinweis**  Der Installations-Assistent kann einen Servergruppen Eintrag erstellen, wenn er nicht vorhanden ist, und einen Eintrag der Application Virtualization Streaming Server-Mitgliedschaft in dieser Gruppe.

 

Nachdem Sie den Installationsvorgang abgeschlossen haben, starten Sie den Server neu.

**So installieren Sie einen Application Virtualization Streaming Server**

1.  Stellen Sie sicher, dass auf Ihrem Zielcomputer keine früheren Versionen von Application Virtualization Streaming Server installiert sind.

    **Wichtig**  Stellen Sie sicher, dass der App-V-Verwaltungs Server auf diesem Computer nicht installiert ist. Die beiden Produkte können nicht auf demselben Computer installiert werden.

     

2.  Navigieren Sie zum Speicherort des Application Virtualization System Setup-Programms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf die **Setup.exe** -Datei.

3.  Klicken Sie auf der Seite **Willkommen** auf **weiter**.

4.  Wählen Sie auf der Seite **Lizenzvertrag** die Option **Ich akzeptiere die**Lizenzbedingungen aus, und klicken Sie dann auf **weiter**, um die Lizenzbedingungen zu akzeptieren.

5.  Geben Sie auf der Seite **Kundeninformationen** den **Benutzernamen** und die Organisation an, und klicken Sie dann auf **weiter**.

6.  Klicken Sie auf der Seite **Installationspfad** auf **Durchsuchen**, geben Sie den Speicherort an, an dem Sie den Streamingserver installieren möchten, und klicken Sie dann auf **weiter**.

7.  Wählen Sie auf der Seite **Verbindungssicherheitsmodus** in der Dropdownliste das gewünschte Zertifikat aus, und klicken Sie dann auf **weiter**.

    **Hinweis**  Bei der Einstellung für den **sicheren Verbindungsmodus** muss der Server über ein Serverzertifikat verfügen, das von einer öffentlichen Schlüsselinfrastruktur bereitgestellt wird. Wenn ein Serverzertifikat nicht auf dem Server installiert ist, ist diese Option nicht verfügbar und kann nicht ausgewählt werden. Sie müssen dem Netzwerkdienstkonto Lesezugriff auf das verwendete Zertifikat gewähren.

     

8.  Wählen Sie auf der Seite **TCP-Portkonfiguration** die Option **Standardanschluss verwenden (554)** aus, um den Standardport (554) zu verwenden. Wenn Sie einen benutzerdefinierten Port angeben möchten, wählen Sie **benutzerdefinierten Port verwenden**aus, geben Sie die Portnummer in dem bereitgestellten Feld an, und klicken Sie dann auf **weiter**.

    **Hinweis**  Wenn Sie den Server in einem nicht sicheren Szenario installieren, können Sie den Standardport (554) verwenden, oder Sie können einen benutzerdefinierten Port definieren.

     

9.  Geben Sie auf der Seite **Inhaltsstamm** den Speicherort auf dem Zielcomputer an, auf dem SFT-Dateien gespeichert werden, und klicken Sie dann auf **weiter**.

    **Hinweis**  Wenn der http-oder RTSP-Port für den Virtual Application Streaming Server bereits zugewiesen ist, werden Sie aufgefordert, einen neuen Port auszuwählen. Geben Sie den gewünschten Port an, und klicken Sie dann auf **weiter**.

     

10. Geben Sie auf dem Bildschirm **Erweiterte Einstellungen** die folgenden Informationen ein:

    1.  **Max-Clientverbindungen**

    2.  **Verbindungstimeout (Sek.)**

    3.  **RTSP-Threadpoolgröße**

    4.  **RTSP-Timeout (Sek.)**

    5.  **Anzahl der Kernprozesse**

    6.  **Core-Timeout (Sek.)**

    7.  **Aktivieren der Benutzerauthentifizierung**

    8.  **Aktivieren der Benutzerautorisierung**

    9.  **Cache Blockgröße (KB)**

    10. **Maximale Cachegröße (MB)**

    **Hinweis**  Der App-V-Streamingserver verwendet NTFS-Dateisystemberechtigungen zum Steuern des Zugriffs auf die Anwendungen unter der Inhaltsfreigabe. Verwenden Sie **Benutzerauthentifizierung aktivieren** , und aktivieren Sie die **Benutzerautorisierung** , um zu steuern, ob der Server diese Zugriffssteuerungslisten (ACLs) überprüft und erzwingt.

     

11. Klicken Sie auf der Seite **bereit zum Installieren des Programms** auf **Installieren**, um die Installation zu starten.

12. Klicken Sie auf dem Bildschirm **Installations-Assistent abgeschlossen** auf **Fertig stellen**, um den Assistenten zu schließen.

    **Wichtig**  Es kann einige Minuten dauern, bis die Installation abgeschlossen ist. Über dem Windows-Desktop-Benachrichtigungsbereich blinkt eine Statusmeldung, die darauf hinweist, dass die Installation erfolgreich war.

    Es ist nicht erforderlich, den Computer neu zu starten, wenn Sie dazu aufgefordert werden. Um die Systemleistung zu optimieren, empfehlen wir jedoch einen Neustart.

     

13. Wiederholen Sie die Schritte 1 bis 12 für jeden virtuellen Anwendungs Server, den Sie installieren müssen.

## Verwandte Themen


[So installieren Sie die Server und Systemkomponenten](how-to-install-the-servers-and-system-components.md)

 

 





