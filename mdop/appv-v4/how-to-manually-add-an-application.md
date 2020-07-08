---
title: So fügen Sie eine Anwendung manuell hinzu
description: So fügen Sie eine Anwendung manuell hinzu
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806971"
---
# So fügen Sie eine Anwendung manuell hinzu


Beim Hinzufügen einer Anwendung zum Application Virtualization Management Server wird empfohlen, Sie zu importieren. Sie können eine Anwendung manuell hinzufügen, aber Sie müssen die genauen, detaillierten Informationen über die in diesem Abschnitt aufgerufene Anwendung angeben.

**So fügen Sie eine neue Anwendung manuell hinzu**

1.  Klicken Sie im linken Bereich mit der rechten Maustaste auf den Knoten **Anwendungen** , und wählen Sie **neue Anwendung**aus.

2.  Füllen Sie im **Assistenten für neue Anwendungen**das Dialogfeld **Allgemeine Informationen** aus:

    1.  **Anwendungsname**: Geben Sie den Namen ein, der den Benutzern angezeigt werden soll.

    2.  **Version**– geben Sie die Anwendungsversion ein.

    3.  **Aktiviert**– dieses Feld muss ausgewählt sein, um die Anwendung nach der Erstellung zu streamen.

    4.  **Beschreibung**: Geben Sie eine optionale Beschreibung für die administrative Verwendung ein.

    5.  **OSD-Pfad**: Durchsuchen Sie das Netzwerk zur OSD-Datei (Open Software Descriptor) der Anwendung. Diese Datei muss sich in einem freigegebenen Netzwerkordner befinden.

    6.  **Symbolpfad**– navigieren Sie zur ICO-Datei der Anwendung.

    7.  **Anwendungslizenzgruppe**– Wenn Sie Lizenzgruppen eingerichtet haben, können Sie die Anwendung einer anderen zuweisen, indem Sie Sie in der Dropdownliste auswählen.

    8.  **Servergruppe**: Wenn Sie über mehrere Application Virtualization-Server verfügen, können Sie die Anwendung einer anderen zuweisen, indem Sie Sie in der Dropdownliste auswählen.

3.  Klicken Sie auf **Weiter**.

4.  Wählen Sie im Dialogfeld **Paket auswählen** das zugehörige Paket aus, und klicken Sie auf **weiter**.

5.  Aktivieren Sie auf dem Bildschirm **veröffentlichte Verknüpfungen** die Kontrollkästchen für die Speicherorte, an denen die Anwendungsverknüpfungen auf den Clientcomputern angezeigt werden sollen, und klicken Sie auf **weiter**.

6.  Auf dem Bildschirm " **Dateizuordnungen** " können Sie dieser Anwendung neue Typendatei Zuordnungen hinzufügen. Klicken Sie dazu auf **Hinzufügen**, geben Sie die Durchwahl (ohne einen vorhergehenden Punkt) ein, geben Sie eine Beschreibung ein, und klicken Sie auf **OK**.

7.  Klicken Sie auf **Weiter**.

8.  Klicken Sie im Dialogfeld **Zugriffsberechtigungen** auf **Hinzufügen**.

9.  Navigieren Sie im Dialogfeld **Benutzergruppe hinzufügen/bearbeiten** zur Gruppe Benutzer. Sie können auch die Domäne und die Gruppe eingeben, indem Sie die Informationen in die entsprechenden Felder eingeben. Wenn Sie fertig sind, klicken Sie auf **OK**. Sie können weitere Gruppen mit denselben Seiten hinzufügen.

10. Klicken Sie auf **Weiter**.

11. Auf dem **Zusammenfassungs** Bildschirm können Sie die Importeinstellungen überprüfen. Klicken Sie auf **Fertig stellen** , um die Anwendung hinzuzufügen, klicken Sie auf **zurück** , um die Informationen zu ändern, oder klicken Sie auf **Abbrechen**.

## Verwandte Themen


[So verwalten Sie Anwendungen in der Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





