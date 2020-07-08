---
title: So aktualisieren Sie die Server und Systemkomponenten
description: So aktualisieren Sie die Server und Systemkomponenten
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806700"
---
# So aktualisieren Sie die Server und Systemkomponenten


Gehen Sie wie folgt vor, um Softwarekomponenten zu aktualisieren, die auf allen Application Virtualization System-Computern installiert sind. Application Virtualization-System Dienste werden auf jedem Computer nach dem Upgrade automatisch neu gestartet.

**Hinweis:**  
-   Durch den Upgradevorgang werden alle Application Virtualization System-Dienste angehalten, wodurch das System außer Betrieb genommen wird. Benutzersitzungen sollten geschlossen werden, bevor Sie mit dem Upgradevorgang beginnen, und Sie sollten alle Application Virtualization Server-Dienste in Ihrer Umgebung beenden.

-   Wenn Sie über mehr als einen Server verfügen, der den Zugriff auf die Application Virtualization-Datenbank freigibt, müssen alle diese Server offline geschaltet werden, während die Datenbank aktualisiert wird. Sie sollten ihre normalen Geschäftsmethoden für das Datenbankupgrade befolgen, es empfiehlt sich jedoch, das Datenbankupgrade mithilfe einer Sicherungskopie der Datenbank zuerst auf einem Testserver zu testen. Wählen Sie dann einen der Server für das erste Upgrade aus, um das Datenbankschema zu aktualisieren. Nachdem die Produktionsdatenbank erfolgreich aktualisiert wurde, können Sie die anderen Server aktualisieren.

-   Sie können ein Upgrade auf Microsoft Application Virtualization (app-v) 4.5 nur von Microsoft Application Virtualization (app-v) 4.1 oder 4.1 SP1 durchführen. App-v 4.0 und frühere Versionen müssen vor dem Upgrade auf App-v 4.5 deinstalliert oder auf 4.1 oder 4.1 SP1 aktualisiert werden.

 

**So aktualisieren Sie Softwarekomponenten auf Computern mit Application Virtualization System**

1.  Navigieren Sie zum Speicherort des Setup Programms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf die Setup.exe-Datei.

2.  Klicken Sie auf der Seite **Willkommen** des Installations-Assistenten auf **weiter**.

3.  Lesen Sie auf der Seite **Lizenzvertrag** den Lizenzvertrag, aktivieren Sie **Ich akzeptiere die Bedingungen des Lizenzvertrags**, und klicken Sie auf **weiter**.

4.  Wenn die Seite **installierte Software** geöffnet wird und eine Liste der installierten Application Virtualization System-Komponenten und die Version der einzelnen Komponenten angezeigt wird, klicken Sie auf **weiter**.

5.  Lesen Sie auf der Seite **Warnung zum Verlust der Sitzung** die angezeigte Nachricht, und klicken Sie auf **weiter**.

6.  Überprüfen Sie auf der Seite mit der **Konfigurationsdatenbank verbinden** den Inhalt auf der Seite, und klicken Sie auf **weiter**.

7.  Wenn die Seite **Datenbank-Upgrade erforderlich** angezeigt wird, ist eine Datenbankaktualisierung erforderlich. Geben Sie die Administratoranmeldeinformationen für die Datenbank ein, und klicken Sie auf **weiter**. Wenn diese Seite nicht angezeigt wird, fahren Sie mit Schritt 9 fort.

8.  Aktivieren Sie auf der Seite **Backup-Konfigurationsdatenbank** die entsprechenden Kontrollkästchen, um die Sicherung durchzuführen und an einen vorhandenen Speicherort zu exportieren, und klicken Sie dann auf **weiter**.

    **Wichtig**  Wenn Sie bei einem Fehler beim Upgrade auf die vorherige Version zurückgreifen möchten, stellen Sie sicher, dass Sie das Kontrollkästchen **eine Sicherungskopie der Konfigurationsdatenbank durchführen** oder die Konfigurationsdaten verloren gehen.

    Wenn Sie eine Datenbank mit VSS wiederherstellen möchten, müssen Sie zuerst den App-V-Server Dienst auf dem Verwaltungs Server beenden. Dies sollte auf jedem Verwaltungsserver erfolgen, wenn mehr als ein Server mit der gleichen Datenbank verbunden ist.

     

9.  Lesen Sie auf der ersten Seite der **Paketüberprüfung** den Inhalt, und klicken Sie dann auf **weiter**.

10. Auf der zweiten **Paket Überprüfungs** Seite haben Sie die Möglichkeit, die Details der Paketüberprüfung in einem Editor-Fenster anzuzeigen. Um die Details anzuzeigen, klicken Sie auf **Details**. Klicken Sie andernfalls auf **weiter**.

11. Klicken Sie auf der Seite **bereit zum Upgrade des Programms** auf **weiter**.

12. Klicken Sie auf der Seite **fertig gestellt des Installations-Assistenten** auf **Fertig stellen**.

13. Wiederholen Sie die Schritte 1 bis 12 auf allen anderen Computern, auf denen Sie die Application Virtualization-Verwaltungskonsole oder die Application Virtualization Server-Softwarekomponente installiert haben.

    Nach dem Upgrade des Datenspeichers können Sie den normalen Vorgang fortsetzen. (Der Datenspeicher wird beim Upgrade eines beliebigen Servers oder des App-V-Verwaltungs-Webdiensts aktualisiert.)

## Verwandte Themen


[Bereitstellung von Application Virtualization und Upgrade Aspekte](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





