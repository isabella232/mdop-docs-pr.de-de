---
title: So weisen Sie die richtigen Anmeldeinformationen für Windows Vista zu
description: So weisen Sie die richtigen Anmeldeinformationen für Windows Vista zu
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808713"
---
# So weisen Sie die richtigen Anmeldeinformationen für Windows Vista zu


Gehen Sie wie folgt vor, um den App-V-Desktop Client für korrekte Windows Vista-Anmeldeinformationen zu konfigurieren.

**Hinweis**  Dieses Verfahren muss auf jedem Computer ohne Domäne abgeschlossen sein. Je nach der Anzahl der nicht an die Domäne angeschlossenen Computer in Ihrer Umgebung kann dies eine sehr mühsame Operation sein. Sie können Skripts und die Befehlszeilenschnittstelle für den Anmelde Informations-Manager verwenden, um Administratoren bei der Automatisierung dieses Prozesses zu unterstützen.

 

**So weisen Sie die richtigen Anmeldeinformationen für App-V-Clients mit Windows Vista zu**

1.  Öffnen Sie mit Administratorrechten auf dem App-V-Desktop Client unter Windows Vista die Systemsteuerung für **Benutzerkonten** (klassisches Control Panel).

2.  Wählen Sie im Bereich links Aufgaben die Option **Netzwerkkennwörter** aus **Benutzerkonten** verwalten aus.

3.  Wählen Sie auf dem Bildschirm **Gespeicherte Benutzernamen und Kennwörter** die Option **Hinzufügen** aus.

4.  Geben Sie auf dem Bildschirm **Eigenschaften der gespeicherten Anmelde** Informationen die Informationen für die App-V-Infrastruktur an:

    1.  **Melden Sie sich bei an:** Externer Name des Veröffentlichungsservers.

    2.  **Benutzername:** Benutzername für den externen Benutzer im Formular Domain\\Username.

    3.  **Kennwort:** Das Kennwort für das Benutzerkonto, das in das Feld " **Benutzername** " eingegeben wurde.

    4.  Geben Sie den **Anmeldeinformationstyp** ausgewählt, und klicken Sie auf **OK**.

5.  Klicken Sie auf **Schließen**. Die Anmeldeinformationen werden im Anmeldeinformationsspeicher für die ordnungsgemäße Authentifizierung in der App-V-Infrastruktur gespeichert.

## Verwandte Themen


[In die Domäne eingebundene und keiner Domäne beigetretene Clients](domain-joined-and-non-domain-joined-clients.md)

[So weisen Sie die richtigen Anmeldeinformationen für Windows XP zu](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





