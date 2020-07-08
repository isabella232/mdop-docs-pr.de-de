---
title: So installieren Sie die Verwaltungskonsole
description: So installieren Sie die Verwaltungskonsole
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807052"
---
# So installieren Sie die Verwaltungskonsole


Sie können das folgende Verfahren zum Installieren der Application Virtualization-Verwaltungskonsole auf einem Zielcomputer im Netzwerk verwenden. Sie müssen ein Netzwerkkonto verwenden, das über Administratorrechte auf dem Zielcomputer verfügt. Sie können die Konsole zum Konfigurieren und Verwalten der Application Virtualization System-Plattform verwenden.

Bevor Sie diese Schritte ausführen können, müssen Sie den Application Virtualization Management Web Service auf diesem oder einem anderen Computer installieren. Mit dem Verwaltungs-Web-Service können Sie auf den Datenspeicher und den Domänencontroller zugreifen. Weitere Informationen zum Installieren des Webdiensts finden Sie unter so wird es [gemacht: Installieren des Verwaltungs-Webdiensts](how-to-install-the-management-web-service.md).

**So installieren Sie die Verwaltungskonsole**

1.  Vergewissern Sie sich, dass auf dem Zielcomputer keine vorherigen Versionen der Verwaltungskonsole installiert sind.

2.  Navigieren Sie zum Speicherort des Application Virtualization System-Setupprogramms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf **Setup.exe**.

3.  Klicken Sie auf der **Seite Willkommen**auf **weiter**.

4.  Wählen Sie auf der Seite **Lizenzvertrag** die Option **Ich akzeptiere die Lizenzbedingungen**aus, um den Lizenzvertrag anzunehmen, und klicken Sie dann auf **weiter**.

5.  Geben Sie auf der Seite **Registrierungsinformationen** den **Benutzernamen** und die **Organisations** Informationen an, und klicken Sie dann auf **weiter**.

6.  Klicken Sie auf der Seite **Setuptyp** auf **Benutzerdefiniert** , und klicken Sie dann auf **weiter**.

7.  Deaktivieren Sie auf der Seite **benutzerdefinierte Einrichtung** die Option Alle Komponenten des Application Virtualization System-Ausnahme **Management Console**, und klicken Sie dann auf **weiter**.

    **Hinweis**  Wenn eine Komponente bereits auf dem Computer installiert ist, wird Sie automatisch deinstalliert, indem Sie Sie auf dem Bildschirm "benutzerdefiniertes Setup" aufheben.

     

8.  Klicken Sie auf dem Bildschirm **bereit zum Ändern des Programms** auf **Installieren**.

    **Hinweis**  Wenn es sich um die erste Komponente handelt, die Sie installieren, wird die Seite " **bereit zum Installieren des Programms** " angezeigt. Klicken Sie auf **Installieren**, um die Installation zu starten.

     

9.  Klicken Sie im Bildschirm **Installationsassistent abgeschlossen** auf **Fertig stellen**. Klicken Sie auf **OK** , um den Computer neu zu starten und die Installation abzuschließen.

10. Doppelklicken Sie in der Windows-Systemsteuerung auf **Verwaltungs Tools** , und klicken Sie dann auf **Application Virtualization Management Console** , um die Verwaltungskonsole anzuzeigen.

11. Klicken Sie auf das Symbol **verbinden** , oder klicken Sie mit der rechten Maustaste auf den Container **Application Virtualization Systems** , und klicken Sie dann auf **mit Application Virtualization System verbinden**.

12. Geben Sie auf dem Bildschirm mit **Application Virtualization System verbinden** den Hostnamen und den Port des Management Web Service-Computers ein, ändern Sie bei Bedarf die Sicherheitsinformationen und Anmeldeinformationen, und klicken Sie dann auf **OK**.

13. Nachdem Sie eine Verbindung mit dem Management Web Service-Computer hergestellt haben, klicken Sie im Menü **Konsole** auf **Datei** , und klicken Sie dann auf **Beenden**. Klicken Sie auf **Ja** , um die Konsoleneinstellungen zu speichern.

## Verwandte Themen


[So installieren Sie die Server und Systemkomponenten](how-to-install-the-servers-and-system-components.md)

 

 





