---
title: So installieren Sie Management Web Service
description: So installieren Sie Management Web Service
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807043"
---
# So installieren Sie Management Web Service


Gehen Sie wie folgt vor, um den Application Virtualization Management Web Service auf einem Zielcomputer im Netzwerk zu installieren, wobei ein Anmeldekonto über lokale Administratorrechte verfügt. Auch wenn dies nicht erforderlich ist, empfehlen wir, diese Komponente auf dem Webserver zu installieren.

**So installieren Sie den Verwaltungs-Web-Service**

1.  Vergewissern Sie sich, dass auf dem Zielcomputer keine vorherigen Versionen des Application Virtualization-Webdiensts installiert sind.

2.  Navigieren Sie zum Speicherort des Application Virtualization System-Setupprogramms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf **Setup.exe**.

3.  Klicken Sie nach dem Öffnen des Installations-Assistenten auf der Seite **Willkommen** auf **weiter**.

4.  Wählen Sie auf der Seite **Lizenzvertrag** die Option **Ich akzeptiere die Lizenzbedingungen**aus, um den Lizenzvertrag anzunehmen, und klicken Sie dann auf **weiter**.

5.  Geben Sie auf der Seite **Registrierungsinformationen** den **Benutzernamen** und die Organisationsinformationen an, und klicken Sie dann auf **weiter**.

6.  Klicken Sie auf der Seite **Setuptyp** auf **Benutzerdefiniert**, und klicken Sie dann auf **weiter**.

    **Hinweis**  Wenn es sich nicht um die erste Komponente handelt, die Sie auf diesem Computer installiert haben, wird die Seite **Programmwartung** angezeigt. Klicken Sie auf der Seite **Programmwartung** auf **ändern**.

     

7.  Deaktivieren Sie auf der Seite **Benutzerdefiniertes Setup** alle Application Virtualization System-Komponenten mit Ausnahme des **App virt-Verwaltungsdiensts**, und klicken Sie dann auf **weiter**.

    **Hinweis**  Wenn eine Komponente bereits auf dem Computer installiert ist, können Sie Sie automatisch deinstallieren, indem Sie Sie auf der **benutzerdefinierten Setup** Seite löschen.

     

8.  Klicken Sie auf der Seite **Daten Bank Server** auf **Verbindung mit verfügbarer Datenbank herstellen**, und klicken Sie dann auf **weiter**.

    **Hinweis**  In einer Produktionsumgebung geht Microsoft davon aus, dass Sie eine Verbindung mit einer vorhandenen Datenbank herstellen. Wenn Sie eine Datenbank installieren möchten, lesen Sie [so wird es gemacht: Installieren einer Datenbank](how-to-install-a-database.md). Nachdem Sie die Datenbank installiert haben, fahren Sie mit Schritt 13 fort.

     

9.  Wählen Sie auf der Seite **Daten Bank** Servertyp einen Datenbanktyp aus der Liste aus, und klicken Sie dann auf **weiter**.

10. Wählen Sie auf der Seite **Speicherort des Datenbankservers** in der Liste der verfügbaren Server einen Datenbankserver aus, oder fügen Sie einen Server hinzu, indem Sie das Kontrollkästchen **folgenden Hostnamen verwenden** und Informationen in die Felder **Server Name** und **Port Nummer** eingeben und dann auf **weiter**klicken.

11. Wählen Sie auf der Seite **Datenbank auswählen** die gewünschte Datenbank aus, und klicken Sie dann auf **weiter**.

12. Geben Sie auf der Seite **Datenbankbenutzer Konfiguration** die Anmeldeinformationen ein, die der Verwaltungs-Webdienst für den Zugriff auf den Datenspeicher verwenden wird, und klicken Sie dann auf **weiter**.

13. Klicken Sie auf der Seite **bereit zum Ändern des Programms** auf **Installieren**.

    **Hinweis**  Wenn es sich um die erste Komponente handelt, die Sie installieren, wird die Seite " **bereit zum Installieren des Programms** " angezeigt. Klicken Sie auf der Seite auf **Installieren**.

     

14. Klicken Sie auf der Seite **fertig gestellt des Installations-Assistenten** auf **Fertig stellen**.

## Verwandte Themen


[So installieren Sie die Server und Systemkomponenten](how-to-install-the-servers-and-system-components.md)

 

 





