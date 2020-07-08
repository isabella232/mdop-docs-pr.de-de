---
title: So installieren Sie Application Virtualization Management Server
description: So installieren Sie Application Virtualization Management Server
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807076"
---
# So installieren Sie Application Virtualization Management Server


Der Application Virtualization Management Server veröffentlicht seine Anwendungen für Clients. In einer Umgebung mit Lastenausgleich, die für große Bereitstellungen typisch ist, sollten alle Server in einer Servergruppe dieselben Anwendungen streamen. Wenn Application Virtualization-Verwaltungsserver verschiedene Anwendungen veröffentlichen sollen, weisen Sie die Server verschiedenen Servergruppen zu. In diesem Fall müssen Sie möglicherweise auch die Kapazität einer Servergruppe erhöhen.

Wenn Sie einen Zielcomputer im Netzwerk festgelegt haben, mit einem Anmeldekonto, das über lokale Administrator Rechte verfügt, können Sie mit dem folgenden Verfahren den Application Virtualization-Verwaltungsserver installieren und der entsprechenden Servergruppe zuweisen.

**Hinweis:**  
Der Installations-Assistent kann einen Servergruppen Eintrag erstellen, wenn er nicht vorhanden ist, sowie einen Eintrag über die Mitgliedschaft des Application Virtualization Management Servers in dieser Gruppe.



Nachdem Sie den Installationsvorgang abgeschlossen haben, starten Sie den Server neu.

**So installieren Sie einen Application Virtualization-Verwaltungs Server**

1.  Überprüfen und deinstallieren Sie bei Bedarf frühere Versionen des Application Virtualization Management Servers, die auf dem Zielcomputer installiert sind.

2.  Navigieren Sie zum Öffnen des **Microsoft Application Virtualization Management Server-Installations** -Assistenten zum Speicherort des Application Virtualization System **setup.exe** -Programms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf die **Setup.exe** -Datei.

3.  Klicken Sie auf der Seite **Willkommen** auf **weiter**.

4.  Lesen Sie auf der Seite **Lizenzvertrag** den Lizenzvertrag, und wählen Sie zum Akzeptieren des Lizenzvertrags die Option **Ich akzeptiere die Lizenzbedingungen**aus. Klicken Sie auf **Weiter**.

5.  Auf der Seite **Registrierungsinformationen** müssen Sie den Benutzernamen und die **Organisation**eingeben. Klicken Sie auf **Weiter**.

6.  Wählen Sie auf der Seite **Setuptyp** die Option **Benutzerdefiniert**aus. Klicken Sie auf **Weiter**. Deaktivieren Sie auf der Seite **Benutzerdefiniertes Setup** alle Application Virtualization System-Komponenten außer **Application Virtualization Server**, und klicken Sie dann auf **weiter**.

    **Achtung**  
    Wenn eine Komponente bereits auf dem Computer installiert ist, wird die Komponente automatisch deinstalliert, wenn Sie Sie im **benutzerdefinierten Setup** Fenster deaktivieren.



7.  Wählen Sie auf der Seite **Konfigurationsdatenbank** in der Liste der verfügbaren Server einen Datenbankserver aus, oder fügen Sie einen Server hinzu, indem Sie **den folgenden Hostnamen verwenden** und den **Servernamen** und die **Port Nummern** angeben. Klicken Sie auf **Weiter**.

    **Hinweis:**  
    Der Application Virtualization-Verwaltungs Server unterstützt keine Groß-/Kleinschreibung SQL.



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. Wählen Sie auf der Seite **Verbindungssicherheitsmodus** in der Dropdownliste das gewünschte Zertifikat aus. Klicken Sie auf **Weiter**.

   **Hinweis:**  
   Bei der Einstellung für den **sicheren Verbindungsmodus** muss der Server über ein Serverzertifikat verfügen, das von einer öffentlichen Schlüsselinfrastruktur bereitgestellt wird. Wenn ein Serverzertifikat nicht auf dem Server installiert ist, ist diese Option nicht verfügbar und kann nicht ausgewählt werden. Sie müssen dem Netzwerkdienstkonto Lesezugriff auf das verwendete Zertifikat gewähren.



9. Klicken Sie auf der Seite **TCP-Port Konfiguration** auf **Standardanschluss verwenden (554)**, um den Standardport (554) zu verwenden. Wenn Sie einen benutzerdefinierten Port angeben möchten, wählen Sie **benutzerdefinierten Port verwenden** aus, und geben Sie die Portnummer an, die verwendet werden soll. Klicken Sie auf **Weiter**.

   **Hinweis:**  
   Wenn Sie den Server in einer nicht sicheren Umgebung installieren, können Sie den Standardport (554) verwenden, oder Sie können einen benutzerdefinierten Port definieren.



10. Geben Sie auf der Seite **Administrator Gruppe** den Namen der Sicherheitsgruppe an, die zum Verwalten dieses Servers unter **Gruppenname**autorisiert ist. Klicken Sie auf **Weiter**. Bestätigen Sie die angegebene Gruppe, und klicken Sie auf **weiter**.

11. Geben Sie auf der Seite **Standardanbietergruppe** den Namen der Standardanbietergruppe an, und klicken Sie dann auf **weiter**.

12. Geben Sie auf der Seite **Inhaltspfad** den Speicherort auf dem Zielcomputer an, auf dem SFT-Dateien gespeichert werden, und klicken Sie dann auf **weiter**.

   **Hinweis:**  
   Wenn der http-oder RTSP-Port für den Verwaltungs Server bereits zugewiesen ist, werden Sie aufgefordert, einen neuen Port zu wählen. Wählen Sie den gewünschten Port aus, und klicken Sie dann auf **weiter**.



13. Klicken Sie auf der Seite **bereit zum Installieren des Programms** auf **Installieren**, um den Application Virtualization-Verwaltungs Server zu installieren.

   **Hinweis:**  
   Wenn bei dem Versuch, diesen Schritt auszuführen, Fehler 25120 angezeigt wird, müssen Sie IIS- **Verwaltungsskripts und-Tools**aktivieren. Um dieses Windows-Feature zu aktivieren, öffnen Sie die Systemsteuerung **Programme und Funktionen** , wählen Sie **Windows-Features aktivieren oder deaktivieren aus**, und navigieren Sie zu **Internet Informationsdienste.**

   Aktivieren Sie unter **Webverwaltungstools**die **IIS-Verwaltungsskripts und-Tools**.



14. Klicken Sie auf dem Bildschirm **Installations-Assistent abgeschlossen** auf **Fertig stellen**, um den Assistenten zu schließen.

   **Wichtig**  
   Es kann einige Minuten dauern, bis die Installation abgeschlossen ist. Über dem Windows-Desktop-Benachrichtigungsbereich blinkt eine Statusmeldung, die darauf hinweist, dass die Installation erfolgreich war.

   Es ist nicht erforderlich, den Computer neu zu starten, wenn Sie dazu aufgefordert werden. Um die Systemleistung zu optimieren, wird jedoch ein Neustart empfohlen.



## Verwandte Themen


[So installieren Sie die Server und Systemkomponenten](how-to-install-the-servers-and-system-components.md)









