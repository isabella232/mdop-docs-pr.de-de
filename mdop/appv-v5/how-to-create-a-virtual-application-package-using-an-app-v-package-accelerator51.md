---
title: So erstellen Sie ein virtuelles Anwendungspaket mit einem App-V Package Accelerator
description: So erstellen Sie ein virtuelles Anwendungspaket mit einem App-V Package Accelerator
author: dansimp
ms.assetid: eae1e4f8-f14f-4bc8-9867-052561c37297
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15376ae52a19b2d220f9ea0031f3ad5649ca487d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805603"
---
# So erstellen Sie ein virtuelles Anwendungspaket mit einem App-V Package Accelerator


**Wichtig**  
Der App-V 5,1-Sequenzer gewährt der Softwareanwendung, die Sie zum Erstellen des Paket Beschleunigers verwenden, keine Lizenzrechte. Sie müssen sich an alle Endbenutzer-Lizenzbestimmungen für die von Ihnen verwendete Anwendung halten. Sie müssen sicherstellen, dass die Lizenzbestimmungen der Softwareanwendung es Ihnen ermöglichen, einen Paket Beschleuniger mit dem App-V 5,1-Sequenzer zu erstellen.



Gehen Sie wie folgt vor, um ein virtuelles Anwendungspaket mit dem App-V 5,1-Paket Beschleuniger zu erstellen.

**Hinweis:**  
Bevor Sie mit diesem Verfahren beginnen, kopieren Sie den erforderlichen Paket Beschleuniger lokal auf den Computer, auf dem der App-V 5,1-Sequenzer ausgeführt wird. Sie sollten auch alle erforderlichen Installationsdateien für das Paket in ein lokales Verzeichnis auf dem Computer kopieren, auf dem der Sequencer ausgeführt wird. Dies ist das Verzeichnis, das Sie in Schritt 5 dieses Verfahrens angeben müssen.



**So erstellen Sie ein virtuelles Anwendungspaket mit einem App-V 5,1-Paket Beschleuniger**

1.  Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v 5,1- **Start**Sequenzer ausgeführt wird, auf  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie zum Starten des **Assistenten zum Erstellen eines neuen Pakets**auf **Neues virtuelles Anwendungspaket erstellen**. Wenn Sie das Paket erstellen möchten, aktivieren Sie das Kontrollkästchen **Paket mithilfe eines Paket Beschleunigers erstellen** , und klicken Sie dann auf **weiter**.

3.  Wenn Sie den Paket Beschleuniger angeben möchten, der zum Erstellen des neuen virtuellen Anwendungspakets verwendet wird, klicken Sie auf der Seite **Paket Beschleuniger auswählen** auf **Durchsuchen** . Klicken Sie auf **Weiter**.

    **Wichtig**  
    Wenn der Herausgeber des Paket Beschleunigers nicht überprüft werden kann und keine gültige digitale Signatur enthält, müssen Sie vor dem Klicken auf **Ausführen**bestätigen, dass Sie der Quelle des Paket Beschleunigers Vertrauen. Bestätigen Sie Ihre Auswahl im Dialogfeld **Sicherheitswarnung** .



4.  Überprüfen Sie auf der Seite **Anleitungen** die Informationen zum veröffentlichungsleitfaden, die im Informationsbereich angezeigt werden. Diese Informationen wurden beim Erstellen des Paket Beschleunigers hinzugefügt und enthält Anleitungen zum Erstellen und Veröffentlichen des Pakets. Wenn Sie die Anleitungen in eine Textdatei (txt) exportieren möchten, klicken Sie auf **exportieren** , und geben Sie den Speicherort an, an dem die Datei gespeichert werden soll, und klicken Sie dann auf **weiter**.

5.  Klicken Sie auf der Seite **Installationsdateien auswählen** auf **neuen Ordner** erstellen, um einen lokalen Ordner zu erstellen, der alle erforderlichen Installationsdateien für das Paket enthält, und geben Sie an, wo der Ordner gespeichert werden soll. Sie müssen auch einen Namen angeben, der dem Ordner zugewiesen werden soll. Sie müssen dann alle erforderlichen Installationsdateien an den von Ihnen angegebenen Speicherort kopieren. Wenn der Ordner, der die Installationsdateien enthält, bereits auf dem Computer vorhanden ist, auf dem der Sequencer ausgeführt wird, klicken Sie auf **Durchsuchen** , um den Ordner auszuwählen.

    Wenn Sie die Installationsdateien bereits in ein Verzeichnis auf diesem Computer kopiert haben, klicken Sie alternativ auf **neuen Ordner erstellen**, navigieren Sie zu dem Ordner, der die Installationsdateien enthält, und klicken Sie dann auf **weiter**.

    **Hinweis:**  
    Sie können die folgenden Typen unterstützter Installationsdateien angeben:

    -   Windows Installer-Dateien (**MSI**)

    -   CAB-Dateien (CAB)

    -   Komprimierte Dateien mit einer ZIP-Dateinamenerweiterung

    -   Die eigentlichen Anwendungsdateien

    Die folgenden Dateitypen werden nicht unterstützt: **MSP** -und **exe** -Dateien. Wenn Sie eine **exe** -Datei angeben, müssen Sie die Installationsdateien manuell extrahieren.



~~~
If the package accelerator requires an application to be installed before you apply the Package Accelerator, and if you have already installed the required application, select **I have installed all applications**, and then click **Next** on the **Local Installation** page.
~~~

6. Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll. Der von Ihnen angegebene Name identifiziert das Paket in der App-V-Verwaltungskonsole. Klicken Sie auf **Weiter**.

7. Geben Sie auf der Seite **Paket erstellen** Kommentare ein, die dem Paket zugeordnet werden. Die Kommentare sollten identifizierende Informationen zu dem zu erstellenden Paket enthalten. Wenn Sie den Speicherort des Pakets bestätigen möchten, überprüfen Sie die Informationen, die unter **Speicherort gespeichert**werden. Um das Paket zu komprimieren, wählen Sie **Paket komprimieren**aus. Aktivieren Sie das Kontrollkästchen **Paket komprimieren** , wenn das Paket über das Netzwerk gestreamt wird oder wenn die Paketgröße 4 GB überschreitet.

   Klicken Sie auf **Erstellen**, um das Paket zu erstellen. Nachdem das Paket erstellt wurde, klicken Sie auf **weiter**.

8. Wählen Sie auf der Seite **Software konfigurieren** aus, um den Sequencer zu aktivieren, um die Anwendungen zu konfigurieren, die im Paket enthalten sind, und wählen Sie **Software konfigurieren**aus. In diesem Schritt können Sie alle zugehörigen Aufgaben konfigurieren, die ausgeführt werden müssen, damit die Anwendung auf den Zielcomputern ausgeführt werden kann. So können Sie beispielsweise alle zugehörigen Lizenzvereinbarungen konfigurieren.

   Wenn Sie **Software konfigurieren**auswählen, können die folgenden Elemente mithilfe des Sequencers als Teil dieses Schritts konfiguriert werden:

   -   **Laden**Sie das Paket. Der Sequencer lädt die Dateien, die dem Paket zugeordnet sind. Das Decodieren des Pakets kann mehrere Sekunden bis zu einer Stunde dauern.

   -   **Führen Sie die einzelnen Programme**aus. Führen Sie optional die Programme aus, die im Paket enthalten sind. Dieser Schritt ist hilfreich, um alle zugehörigen Lizenz-oder Konfigurationsaufgaben abzuschließen, die erforderlich sind, um die Anwendung auszuführen, bevor Sie das Paket auf Zielcomputern bereitstellen und ausführen. Wenn Sie alle Programme auf einmal ausführen möchten, wählen Sie mindestens ein Programm aus, und klicken Sie dann auf **alle ausführen**. Wenn Sie bestimmte Programme ausführen möchten, wählen Sie das Programm oder die Programme aus, die Sie ausführen möchten, und klicken Sie dann auf **ausgewählte ausführen**. Führen Sie die erforderlichen Konfigurationsaufgaben aus, und schließen Sie dann die Anwendungen. Es kann mehrere Minuten dauern, bis alle Programme ausgeführt werden. Klicken Sie auf **Weiter**.

   -   **Paket speichern**. Der Sequencer speichert das Paket.

   -   **Primärer Feature-Block**. Der Sequencer optimiert das Paket für das Streaming, indem der primäre Feature-Block neu erstellt wird.

   Wenn Sie die Anwendungen nicht konfigurieren möchten, klicken Sie auf **diesen Schritt überspringen**, und fahren Sie mit Schritt 9 dieses Verfahrens fort, und klicken Sie dann auf **weiter**.

9. Klicken Sie auf der Seite **Fertigstellung** nach dem Überprüfen der Informationen, die im Bereich **Bericht des virtuellen Anwendungspakets** angezeigt werden, auf **Schließen**.

   Das Paket steht jetzt im Sequencer zur Verfügung. Um die Paketeigenschaften zu bearbeiten, klicken Sie auf **Bearbeiten \ [Package Name \]**. Weitere Informationen zum Ändern eines Pakets finden Sie unter so wird es [gemacht: Ändern eines vorhandenen virtuellen Anwendungspakets](how-to-modify-an-existing-virtual-application-package-beta.md).

   Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)









