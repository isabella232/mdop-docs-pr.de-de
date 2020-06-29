---
title: So installieren Sie eine Datenbank
description: So installieren Sie eine Datenbank
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807083"
---
# So installieren Sie eine Datenbank


Mit dem folgenden Verfahren können Sie eine Datenbank für Ihre serverbasierte Bereitstellung von Application Virtualization installieren, wenn noch keine Datenbank verfügbar ist. In einer Produktionsumgebung stellen Sie normalerweise eine Verbindung mit einer vorhandenen Datenbank her.

**Wichtig**  Um die Datenbank zu installieren, müssen Sie ein Netzwerkkonto mit den entsprechenden Berechtigungen verwenden. Wenn Ihre Organisation erfordert, dass nur Datenbankadministratoren Datenbankaktualisierungen erstellen und durchführen können, stehen Skripts zur Verfügung, mit denen diese Aufgabe ausgeführt werden kann.

 

**So installieren Sie eine Datenbank**

1.  Navigieren Sie zum Speicherort des Application Virtualization System-Setupprogramms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf **Setup.exe**.

2.  Klicken Sie auf der **Seite Willkommen**auf **weiter**.

3.  Wählen Sie auf der Seite **Lizenzvertrag** die Option **Ich akzeptiere die Lizenzbedingungen**aus, um den Lizenzvertrag anzunehmen, und klicken Sie auf **weiter**.

4.  Geben Sie auf der Seite **Registrierungsinformationen** den **Benutzernamen** und die **Organisations** Informationen an, und klicken Sie dann auf **weiter**.

5.  Wählen Sie auf der Seite **Setuptyp** die Option **Benutzerdefiniert** aus, und klicken Sie dann auf **weiter**.

6.  Deaktivieren Sie auf der Seite **Benutzerdefiniertes Setup** alle Application Virtualization System-Komponenten außer **Application Virtualization Server**, und klicken Sie dann auf **weiter**.

    **Hinweis**  Wenn eine Komponente bereits auf dem Computer installiert ist, wird Sie im **benutzerdefinierten Setup** -Bildschirm automatisch deinstalliert.

     

7.  Geben Sie auf der Seite **Daten Bank Server** die Kennwörter ein, weisen Sie einen Installationspfad zu, speichern Sie die Informationen, und klicken Sie auf **weiter**.

8.  Wählen Sie einen Namen für die Datenbank aus, und klicken Sie dann auf **weiter**.

    **Hinweis**  Wenn bei dem Versuch, diesen Schritt abzuschließen, Fehler 25109 angezeigt wird, haben Sie die erforderlichen Berechtigungen zum Installieren der Datenbank falsch eingerichtet. Weitere Informationen zum Einrichten der erforderlichen SQL-Berechtigungen finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=132144> .

     

9.  Geben Sie auf dem Bildschirm **Verzeichnis Server** einen Domänennamen und die Anmeldeinformationen ein, die von Application Virtualization Server und dem Verwaltungs-Webdienst für den Zugriff auf Ihren Domänencontroller verwendet werden, speichern Sie diese Informationen, und klicken Sie dann auf **weiter**.

    **Hinweis**  Bei der Installation wird standardmäßig die Domäne des aktuellen Computers verwendet.

     

10. Geben Sie auf der Seite **Administratorgruppe** den Namen einer Gruppe ein, die über Administratorrechte verfügen soll, speichern Sie diese Informationen, und klicken Sie dann auf **weiter**.

    **Hinweis**  Sie können auch die ersten Zeichen des Namens einer Gruppe eingeben, die über Administratorrechte verfügen, klicken Sie auf **weiter**, und wählen Sie auf der Seite **Administrator Gruppe auswählen** die Gruppe aus der resultierenden Liste aus. Speichern Sie diese Informationen, und klicken Sie auf **weiter**.

     

11. Geben Sie auf der Seite **Standardanbietergruppe** den vollständigen Namen einer Gruppe ein, die den Zugriff auf Anwendungen steuern soll, speichern Sie diese Informationen, und klicken Sie dann auf **weiter**.

    **Hinweis**  Sie können auch die ersten Zeichen des Namens einer Gruppe eingeben, die den Zugriff auf Anwendungen steuern soll, klicken Sie auf **weiter**, und wählen Sie auf dem Bildschirm **Standardanbietergruppe auswählen** die Gruppe in der Liste aus. Speichern Sie diese Informationen, und klicken Sie auf **weiter**.

     

12. Klicken Sie auf der Seite **abgeschlossen des Installations-Assistenten** auf **Fertig stellen**, um den Assistenten zu schließen.

    **Wichtig**  Es kann einige Minuten dauern, bis die Installation abgeschlossen ist. Über dem Windows-Desktop-Benachrichtigungsbereich blinkt eine Statusmeldung, die angibt, ob die Installation erfolgreich war.

     

## Verwandte Themen


[So installieren Sie die Server und Systemkomponenten](how-to-install-the-servers-and-system-components.md)

 

 





