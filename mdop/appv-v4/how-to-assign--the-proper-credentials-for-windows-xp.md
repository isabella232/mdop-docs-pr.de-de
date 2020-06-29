---
title: So weisen Sie die richtigen Anmeldeinformationen für Windows XP zu
description: So weisen Sie die richtigen Anmeldeinformationen für Windows XP zu
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807860"
---
# So weisen Sie die richtigen Anmeldeinformationen für Windows XP zu


Gehen Sie wie folgt vor, um den App-V-Desktop Client für korrekte WindowsXP-Anmeldeinformationen zu konfigurieren.

**Hinweis**  Nach Abschluss dieses Verfahrens kann der nicht der Domäne beige tretene Client eine Veröffentlichungsaktualisierung durchführen, ohne mit einer Domäne verbunden zu sein.

 

**So weisen Sie die richtigen Anmeldeinformationen für App-V-Clients mit WindowsXP zu**

1.  Öffnen Sie mit Administratorrechten auf dem App-V-Client, auf dem WindowsXP ausgeführt wird, die Systemsteuerung für **Benutzerkonten** (klassisches Control Panel).

2.  Klicken Sie auf die **Registerkarte Erweitert**, und wählen Sie dann **Kennwörter verwalten**aus.

3.  Klicken Sie auf dem Bildschirm **Gespeicherte Benutzernamen und Kennwörter** auf **Hinzufügen**.

4.  Füllen Sie auf dem Bildschirm **Anmeldeinformationen Eigenschaften** die folgenden Felder mit Informationen aus der App-V-Infrastruktur aus:

    1.  **Server:** Name des externen Namens des Veröffentlichungsservers.

    2.  **Benutzername:** Benutzername für externen Benutzer im Formular Domain\\username.

    3.  **Kennwort:** Das Kennwort für das Benutzerkonto, das in das Feld " **Benutzername** " eingegeben wurde.

5.  Klicken Sie auf **OK**. Die Anmeldeinformationen werden auf dem Client gespeichert.

## Verwandte Themen


[In die Domäne eingebundene und keiner Domäne beigetretene Clients](domain-joined-and-non-domain-joined-clients.md)

[So weisen Sie die richtigen Anmeldeinformationen für Windows Vista zu](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





