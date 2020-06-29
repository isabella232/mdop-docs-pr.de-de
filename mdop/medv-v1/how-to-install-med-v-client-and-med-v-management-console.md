---
title: So installieren Sie den MED-V-Client und die MED-V-Verwaltungskonsole
description: So installieren Sie den MED-V-Client und die MED-V-Verwaltungskonsole
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812082"
---
# So installieren Sie den MED-V-Client und die MED-V-Verwaltungskonsole


Die folgenden MED-V-Komponenten sind im Client. MSI-Paket enthalten:

-   Med-v-Client – die Med-v-Software, die auf Clientcomputern für die Ausführung von Med-v-Arbeitsbereichen installiert werden muss.

-   Med-v-Verwaltungskonsole – das Verwaltungstool, das Administratoren verwenden können, um Bilder, Med-v-Arbeitsbereiche und Richtlinien zu erstellen und zu verwalten.

Die Med-v-Verwaltungskonsole und der Med-v-Client sind beide aus dem Med-v-Client. MSI-Paket installiert. Der Med-v-Client kann jedoch unabhängig von der Med-v-Verwaltungskonsole installiert werden, indem das Kontrollkästchen **Installieren der Med-v-Verwaltungsanwendung** während der Installation deaktiviert wird.

**Hinweis:**  
Der Med-v-Client und die Med-v-Verwaltungskonsole können nur auf Computern unter Windows 7, Windows Vista und Windows XP installiert werden. Sie können nicht auf Serverprodukten installiert werden.



**Hinweis:**  
Installieren Sie den MED-V-Client nicht mit dem Befehl Windows **runas** .



**So installieren Sie den MED-V-Client**

1.  Melden Sie sich als Benutzer mit lokalen Administratorrechten auf dem lokalen Computer an.

2.  Führen Sie das MED-V. MSI-Paket aus.

    Das MED-V. MSI-Paket heißt *MED-V\_x.msi*, wobei *x* die Versionsnummer ist.

    Beispiel: *MED-V\_1.0.65.msi*.

3.  Wenn der **Begrüßungs** Bildschirm des InstallShield-Assistenten angezeigt wird, klicken Sie auf **weiter**.

4.  Lesen Sie auf dem Bildschirm **Lizenzvertrag** den Lizenzvertrag, klicken Sie auf **Ich stimme den Bedingungen des Lizenzvertrags**zu, und klicken Sie auf **weiter**.

    Der Bildschirm **Zielordner** wird angezeigt, und der Standardinstallationsordner wird angezeigt.

    Der Standardinstallationsordner ist das Verzeichnis, in dem das Betriebssystem installiert ist.

    -   Wenn Sie den Ordner ändern möchten, in dem MED-V installiert werden soll, klicken Sie auf **ändern**, und navigieren Sie zu einem vorhandenen Ordner.

5.  Klicken Sie auf **Weiter**.

6.  Konfigurieren Sie auf dem Bildschirm **Med-v-Einstellungen** die Med-v-Installation wie folgt:

    -   Aktivieren Sie das Kontrollkästchen **MED-V-Verwaltungsanwendung installieren** , um die Verwaltungskomponente in die Installation einzubeziehen.

        **Hinweis:**  
        Administratoren von Unternehmens Desktop-Virtualisierung sollten die MED-V-Verwaltungsanwendung installieren. Diese Anwendung ist für die Konfiguration von Desktop Bildern und MED-V-Arbeitsbereichen erforderlich.



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. Klicken Sie auf **Weiter**.

8. Klicken Sie auf dem Bildschirm **bereit zum Installieren des Programms** auf **Installieren**.

   Die MED-V-Clientinstallation wird gestartet. Dies kann mehrere Minuten dauern, und auf dem Bildschirm wird möglicherweise kein Text angezeigt. Während der Installation werden mehrere Status Bildschirme angezeigt. Wenn eine Meldung angezeigt wird, folgen Sie den Anweisungen.

   Nach erfolgreicher Installation wird der Bildschirm **InstallShield-Assistent abgeschlossen** angezeigt.

9. Klicken Sie auf **Fertig stellen** , um den Assistenten zu schließen.

## Verwandte Themen


[Unterstützte Konfigurationen](supported-configurationsmedv-orientation.md)

[Installations- und Aktualisierungsprüflisten](installation-and-upgrade-checklists.md)









