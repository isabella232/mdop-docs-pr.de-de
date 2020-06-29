---
title: Anwenden eines Paket Beschleunigers zum Erstellen eines virtuellen Anwendungspakets (App-V 4,6 SP1)
description: Anwenden eines Paket Beschleunigers zum Erstellen eines virtuellen Anwendungspakets (App-V 4,6 SP1)
author: dansimp
ms.assetid: ca0bd514-2bbf-4130-8c77-98d991cbe016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce6960fb95cce7f5e0eeb111412f27f945b0c1a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808722"
---
# Anwenden eines Paket Beschleunigers zum Erstellen eines virtuellen Anwendungspakets (App-V 4,6 SP1)


Sie können App-V-Paket Beschleuniger verwenden, um automatisch ein neues virtuelles Anwendungspaket zu generieren. Weitere Informationen zu Paket Beschleunigern finden Sie unter [Informationen zu app-v-Paket Beschleunigern (app-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).

**Wichtig**  
Haftungsausschluss: der Application Virtualization Sequencer gibt Ihnen keine Lizenzrechte für die Softwareanwendung, die Sie zum Erstellen eines Paket Beschleunigers verwenden. Sie müssen sich an alle Endnutzer-Lizenzbestimmungen für diese Anwendung halten. Sie müssen sicherstellen, dass die Lizenzbestimmungen der Softwareanwendung es Ihnen ermöglichen, mithilfe von Application Virtualization Sequencer einen Paket Beschleuniger zu erstellen.



**Hinweis:**  
Bevor Sie mit diesem Verfahren beginnen, kopieren Sie den erforderlichen Paket Beschleuniger lokal auf den Computer, auf dem der App-V-Sequencer ausgeführt wird. Sie sollten auch alle erforderlichen Installationsdateien für das Paket in ein lokales Verzeichnis auf dem Computer kopieren, auf dem der Sequencer ausgeführt wird. Dies ist das Verzeichnis, das Sie in Schritt 5 dieses Verfahrens angeben müssen.



Verwenden Sie das folgende Verfahren zum Erstellen eines virtuellen Anwendungspakets mithilfe eines Paket Beschleunigers.

**So erstellen Sie ein virtuelles Anwendungspaket mithilfe eines App-V-Paket Beschleunigers**

1. Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2. Klicken Sie zum Starten des **Assistenten zum Erstellen eines neuen Pakets**auf **Neues virtuelles Anwendungspaket erstellen**. Wenn Sie das Paket erstellen möchten, aktivieren Sie das Kontrollkästchen **Paket mithilfe eines Paket Beschleunigers erstellen** , und klicken Sie dann auf **weiter**.

3. Klicken Sie auf der Seite **Paket Beschleuniger auswählen** zum Angeben des Paket Beschleunigers, der zum Erstellen des neuen virtuellen Anwendungspakets verwendet werden soll, auf **Durchsuchen** , um nach dem zu verwendenden Paket Beschleuniger zu suchen. Klicken Sie auf **Weiter**.

   **Wichtig**  
   Wenn der Herausgeber des Paket Beschleunigers nicht überprüft werden kann und keine gültige digitale Signatur enthält, müssen Sie im Dialogfeld **Sicherheitswarnung** bestätigen, dass Sie der Quelle des Paket Beschleunigers Vertrauen, bevor Sie auf **Ausführen**klicken.



4. Überprüfen Sie auf der Seite **Anleitungen** die Informationen zum veröffentlichungsleitfaden, die im Informationsbereich angezeigt werden. Die angezeigten Informationen wurden beim Erstellen des Paket Beschleunigers hinzugefügt und enthalten Informationen zum Erstellen und Veröffentlichen des Pakets. Wenn Sie die Anleitungen in eine Textdatei (txt) exportieren möchten, klicken Sie auf **exportieren** , und geben Sie den Speicherort an, an dem die Datei gespeichert werden soll, und klicken Sie dann auf **weiter**.

5. Klicken Sie auf der Seite **Installationsdateien auswählen** zum Erstellen eines lokalen Ordners, der alle erforderlichen Installationsdateien für das Paket enthält, auf **neuen Ordner** erstellen, und geben Sie an, wo der Ordner gespeichert werden soll. Sie müssen auch einen Namen angeben, der dem Ordner zugewiesen werden soll. Sie müssen dann alle erforderlichen Installationsdateien an den von Ihnen angegebenen Speicherort kopieren. Wenn der Ordner, der die Installationsdateien enthält, bereits auf dem Computer vorhanden ist, auf dem der Sequencer ausgeführt wird, klicken Sie auf **Durchsuchen** , um den Ordner auszuwählen.

   Wenn Sie die Installationsdateien bereits in ein Verzeichnis auf diesem Computer kopiert haben, klicken Sie alternativ auf **neuen Ordner erstellen**, navigieren Sie zu dem Ordner, der die Installationsdateien enthält, und klicken Sie dann auf **weiter**.

   **Hinweis:**  
   Sie können die folgenden Typen unterstützter Installationsdateien angeben:

   -   Windows Installer-Dateien (**MSI**

   -   CAB-Dateien

   -   Komprimierte Dateien mit einer ZIP-Dateinamenerweiterung

   -   Die eigentlichen Anwendungsdateien

   Die folgenden Dateitypen werden nicht unterstützt: **MSP** -und <strong> exe- </strong> Dateien. Wenn Sie eine **exe-** Datei angeben, müssen Sie die Installationsdateien manuell extrahieren.



~~~
If the Package Accelerator requires an application be installed prior to applying the Package Accelerator and you have installed the application, on the **Local Installation** page, select the check box **I have installed all applications**, and then click **Next**.
~~~

6. Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll. Der angegebene Name identifiziert das Paket in der App-V-Verwaltungskonsole. Klicken Sie auf **Weiter**.

7. Geben Sie auf der Seite **Paket erstellen** Kommentare ein, die dem Paket zugeordnet werden. Die Kommentare sollten identifizierende Informationen zu dem zu erstellenden Paket enthalten. Wenn Sie den Speicherort des Pakets bestätigen möchten, überprüfen Sie die Informationen, die unter **Speicherort gespeichert**werden. Um das Paket zu komprimieren, wählen Sie **Paket komprimieren**aus. Aktivieren Sie das Kontrollkästchen **Paket komprimieren** , wenn das Paket über das Netzwerk gestreamt wird oder wenn die Paketgröße 4 GB überschreitet.

   Klicken Sie auf **Erstellen**, um das Paket zu erstellen. Nachdem das Paket erstellt wurde, klicken Sie auf **weiter**.

8. Wählen Sie auf der Seite **Software konfigurieren** aus, um den Sequencer zum Konfigurieren der im Paket enthaltenen Anwendungen zu aktivieren, **Software konfigurieren**. Dieser Schritt ist nützlich, um alle zugehörigen Aufgaben zu konfigurieren, die ausgeführt werden müssen, um die Anwendung auf Zielcomputern auszuführen, beispielsweise die Konfiguration zugehöriger Lizenzvereinbarungen.

   Wenn Sie **Software konfigurieren**auswählen, werden die folgenden Elemente im Rahmen dieses Schritts vom Sequencer konfiguriert:

   -   **Laden**Sie das Paket. Der Sequencer lädt die Dateien, die dem Paket zugeordnet sind. Das Decodieren des Pakets kann mehrere Sekunden bis zu einer Stunde dauern.

   -   **Führen Sie die einzelnen Programme**aus. Führen Sie optional die Programme aus, die im Paket enthalten sind. Dieser Schritt ist hilfreich, um alle zugehörigen Lizenz-oder Konfigurationsaufgaben abzuschließen, die erforderlich sind, um die Anwendung auszuführen, bevor Sie das Paket auf Zielcomputern bereitstellen und ausführen. Wenn Sie alle Programme auf einmal ausführen möchten, wählen Sie mindestens ein Programm aus, und klicken Sie dann auf **alle ausführen**. Wenn Sie bestimmte Programme ausführen möchten, wählen Sie das Programm oder die Programme aus, die Sie ausführen möchten, und klicken Sie dann auf **ausgewählte ausführen**. Führen Sie die erforderlichen Konfigurationsaufgaben aus, und schließen Sie dann die Anwendungen. Es kann mehrere Minuten dauern, bis alle Programme ausgeführt werden. Klicken Sie auf **Weiter**.

   -   **Paket speichern**. Der Sequencer speichert das Paket.

   -   **Primärer Feature-Block**. Der Sequencer optimiert das Paket für das Streaming, indem der primäre Feature-Block neu erstellt wird.

   Wenn Sie die Anwendungen nicht konfigurieren möchten, klicken Sie auf **diesen Schritt überspringen**, und fahren Sie mit Schritt 9 dieses Verfahrens fort, und klicken Sie dann auf **weiter**.

9. Klicken Sie auf der Seite **Fertigstellung** nach dem Überprüfen der Informationen, die im Bereich **Bericht des virtuellen Anwendungspakets** angezeigt werden, auf **Schließen**.

   Das Paket steht jetzt im Sequencer zur Verfügung. Um die Paketeigenschaften zu bearbeiten, klicken Sie auf **Bearbeiten \ [Package Name \]**. Weitere Informationen zum Ändern eines Pakets finden Sie unter [so wird es gemacht: Ändern eines vorhandenen virtuellen Anwendungspakets (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).

## Verwandte Themen


[Konfigurieren von Application Virtualization Sequencer (App-V 4.6 SP1)](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[So erstellen Sie App-V Package Accelerators (App-V 4.6 SP1)](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)









