---
title: So passen Sie mithilfe der Verwaltungskonsole virtuelle Anwendungserweiterungen für eine spezifische AD-Gruppe an
description: So passen Sie mithilfe der Verwaltungskonsole virtuelle Anwendungserweiterungen für eine spezifische AD-Gruppe an
author: dansimp
ms.assetid: dd71df05-512f-4eb4-a55f-e5b93601323d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bf086da3fbb6938a4fc602af5ab63adb1621532
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805591"
---
# So passen Sie mithilfe der Verwaltungskonsole virtuelle Anwendungserweiterungen für eine spezifische AD-Gruppe an


Gehen Sie wie folgt vor, um die Erweiterungen der virtuellen Anwendung für eine Active Directory-Gruppe (AD) anzupassen.

**So passen Sie die Erweiterungen virtueller Anwendungen für eine Anzeigengruppe an**

1.  Um das Paket anzuzeigen, das Sie konfigurieren möchten, öffnen Sie die App-V 5,1-Verwaltungskonsole. Wenn Sie die Konfiguration anzeigen möchten, die einer bestimmten Benutzergruppe zugewiesen ist, wählen Sie das Paket aus, klicken Sie mit der rechten Maustaste auf den Paketnamen, und wählen Sie **Active Directory-Zugriff bearbeiten**aus. Alternativ können Sie das Paket auswählen und im Bereich **anzeigen Zugriff** auf **Bearbeiten** klicken.

2.  Zum Anpassen einer Anzeigengruppe können Sie die Gruppe in der Liste der **anzeigen Entitäten mit Access**finden. Wählen Sie dann über das Dropdownfeld im Bereich **zugewiesene Konfiguration** die Option **Benutzerdefiniert**aus, und klicken Sie dann auf **Bearbeiten**.

3.  Um alle Erweiterungen für eine bestimmte Anwendung zu deaktivieren, deaktivieren Sie **aktivieren**.

    Wenn Sie eine neue Verknüpfung für die ausgewählte Anwendung hinzufügen möchten, klicken Sie im Bereich " **Verknüpfungen** " mit der rechten Maustaste auf die Anwendung, und wählen Sie **neue Verknüpfung hinzufügen**aus. Um eine Verknüpfung zu entfernen, klicken Sie im Bereich " **Verknüpfungen** " mit der rechten Maustaste auf die Anwendung, und wählen Sie **Verknüpfung entfernen**aus. Wenn Sie eine vorhandene Verknüpfung bearbeiten möchten, klicken Sie mit der rechten Maustaste auf die Anwendung, und wählen Sie **Verknüpfung bearbeiten**aus.

4.  Wenn Sie weitere Anwendungserweiterungen anzeigen möchten, klicken Sie auf **erweitert**, und klicken Sie dann auf **Konfiguration exportieren**. Geben Sie einen Dateinamen ein, und klicken Sie auf **Speichern**. Mit der Konfigurationsdatei können Sie alle Anwendungserweiterungen anzeigen, die dem Paket zugeordnet sind.

5.  Wenn Sie zusätzliche Anwendungserweiterungen bearbeiten möchten, ändern Sie die Konfigurationsdatei, und klicken Sie auf **importieren, und überschreiben Sie diese Konfiguration**. Wählen Sie die geänderte Datei aus, und klicken Sie auf **Öffnen**. Klicken Sie im Dialogfeld auf über **Schreiben** , um den Vorgang abzuschließen.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

 

 





