---
title: So sequenzieren Sie eine neue Standardanwendung (App-V 4.6 SP1)
description: So sequenzieren Sie eine neue Standardanwendung (App-V 4.6 SP1)
author: dansimp
ms.assetid: c4a2eb33-def8-4535-b93a-3d2de21ce29f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47c93b4880d0095c87a98292fda743acc1659e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806796"
---
# So sequenzieren Sie eine neue Standardanwendung (App-V 4.6 SP1)


Gehen Sie wie folgt vor, um ein neues Standardpaket für virtuelle Anwendungen mithilfe von Application Virtualization (App-V) Sequencer zu erstellen. Dieses Verfahren gilt für die meisten Anwendungen, die Sie abgleichen. Weitere Informationen zu den Arten von Anwendungen, die Sie abbilden können, finden Sie unter [So ermitteln Sie, welche Art von Anwendung in der Reihenfolge ausgeführt wird (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md). Sie müssen den Sequencer (**SFTSequencer.exe**) mithilfe eines Kontos ausführen, das über Administratorberechtigungen verfügt, weil die Änderungen, die der Sequencer am lokalen System vornimmt, ausgeführt werden. Diese Änderungen können das Schreiben von Dateien in das **c:\\Programme-Datei** Verzeichnis, das vornehmen von Registrierungsänderungen, das Starten und Beenden von Diensten, das Aktualisieren von Sicherheitsbeschreibungen für Dateien und das Ändern von Berechtigungen umfassen.

**Wichtig**  
Wenn während der Sequenzierung auf dem Computer, auf dem der Sequencer ausgeführt wird, Windows Vista oder Windows 7 ausgeführt wird und ein Neustart außerhalb der virtuellen Umgebung initiiert wird, beispielsweise **Start**  /  **Herunterfahren**, müssen Sie auf **Abbrechen** klicken, wenn Sie aufgefordert werden, das Programm zu schließen, das verhindert, dass Windows Vista oder Windows beendet wird. Wenn Sie auf **Beenden erzwingen**klicken, schlägt die Paketerstellung fehl. Wenn Sie auf **Abbrechen**klicken, zeichnet der Sequencer den Neustart erfolgreich auf, während die Anwendung sequenziert wird.



**Hinweis:**  
Das Ausführen des App-V-Sequencers im abgesicherten Modus wird nicht unterstützt.



**So Sequenzieren Sie eine neue Standardanwendung**

1.  Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie zum Starten des **Assistenten zum Erstellen eines neuen Pakets**auf **Neues virtuelles Anwendungspaket erstellen**. Wenn Sie das Paket erstellen möchten, wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.

3.  Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt, oder dass das Paket unnötige Daten enthält. Wir empfehlen dringend, dass Sie alle potenziellen Probleme beheben, bevor Sie fortfahren. Nachdem Sie die Konflikte behoben haben, klicken Sie auf **Aktualisieren**, um die angezeigten Informationen zu aktualisieren. Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.

    **Wichtig**  
    Wenn Sie die Virenscansoftware deaktivieren müssen, überprüfen Sie den Computer, auf dem der Sequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder bösartigen Dateien hinzugefügt werden können.



4.  Klicken Sie auf der Seite **Typ der Anwendung** auf **Standardanwendung (Standard)** , und klicken Sie dann auf **weiter**.

    Weitere Informationen zu den Arten von Anwendungen, die Sie abbilden können, finden Sie unter so wird es [gemacht: Ermitteln des zu sequenzenden Anwendungstyps (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für die Anwendung an. Wenn die Anwendung keine zugeordnete Installationsdatei hat und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **benutzerdefinierte Installation durchführen** , und klicken Sie dann auf **weiter**.

6.  Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll. Mit dem Namen können Sie den Zweck und die Version der Anwendung ermitteln, die dem Paket hinzugefügt werden. Der Paketname wird auch in der App-V-Verwaltungskonsole angezeigt. Das **primäre virtuelle Anwendungsverzeichnis** zeigt den Application Virtualization Path an, in dem die Anwendung auf den Zielcomputern installiert wird. Um diesen Speicherort zu bearbeiten, wählen Sie **Bearbeiten (erweitert)** aus.

    **Wichtig**  
    Das Bearbeiten des Application Virtualization path ist eine erweiterte Konfigurationsaufgabe. Sie sollten die Auswirkungen einer Änderung des Pfads vollständig verstehen. Bei den meisten Anwendungen wird der Standardpfad empfohlen.



~~~
Click **Next**.
~~~

7. Installieren Sie die Anwendung auf der **Installations** Seite, wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, so, dass der Sequencer den Installationsvorgang überwachen kann. Führen Sie die Installation mithilfe des Installationsvorgangs der Anwendung durch. Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen** , um die zusätzlichen Installationsdateien zu suchen und auszuführen. Wenn Sie die Installation abgeschlossen haben, wählen Sie **Ich habe die Installation abgeschlossen**aus. Klicken Sie auf **Weiter**.

8. Warten Sie auf der **Installations** Seite, während der Sequencer das virtuelle Anwendungspaket konfiguriert.

9. Führen Sie auf der Seite **Software konfigurieren** optional die Programme aus, die im Paket enthalten sind. Mit diesem Schritt können Sie alle zugehörigen Lizenz-oder Konfigurationsaufgaben ausführen, die für die Ausführung der Anwendung erforderlich sind, bevor Sie das Paket auf Zielcomputern bereitstellen und ausführen. Wenn Sie alle Programme auf einmal ausführen möchten, wählen Sie mindestens ein Programm aus, und klicken Sie dann auf **alle ausführen**. Wenn Sie bestimmte Programme ausführen möchten, wählen Sie das Programm oder die Programme aus, die Sie ausführen möchten, und klicken Sie dann auf **ausgewählte ausführen**. Führen Sie die erforderlichen Konfigurationsaufgaben aus, und schließen Sie dann die Anwendungen. Es kann mehrere Minuten dauern, bis alle Programme ausgeführt werden. Klicken Sie auf **Weiter**.

10. Auf der Seite **Installationsbericht** können Sie Informationen zu dem soeben sequenzierten virtuellen Anwendungspaket überprüfen. Eine detailliertere Erläuterung der Informationen, die in **zusätzlichen Informationen**angezeigt werden, finden Sie, indem Sie auf das Ereignis doppelklicken. Nachdem Sie die Informationen überprüft haben, klicken Sie auf **weiter**.

11. Wenn Sie die Installation und Konfiguration der virtuellen Anwendung abgeschlossen haben, wählen Sie auf der Seite **Anpassen** die Option **jetzt beenden** aus, und fahren Sie mit Schritt 15 dieser Vorgehensweise fort. Wenn Sie die Elemente in der folgenden Liste anpassen möchten, wählen Sie **Anpassen**aus.

    -   Bearbeiten Sie die Dateitypen Zuordnungen und die Symbole, die einer Anwendung zugeordnet sind.

    -   Vorbereiten des virtuellen Pakets für Streaming. Durch Streaming wird die Benutzerfreundlichkeit verbessert, wenn das virtuelle Anwendungspaket auf Zielcomputern ausgeführt wird.

    -   Geben Sie die Betriebssysteme an, die dieses Paket ausführen können.

    Klicken Sie auf **Weiter**.

12. Auf der Seite " **Verknüpfungen bearbeiten** " können Sie optional die Dateitypen Zuordnungen (FTA) und die verknüpfungsspeicher Orte konfigurieren, die den verschiedenen Anwendungen im Paket zugeordnet werden. Wenn Sie ein neues FTA erstellen möchten, wählen Sie im linken Bereich die Anwendung aus, die Sie anpassen möchten, und klicken Sie dann auf **Hinzufügen**. Geben Sie im Dialogfeld **Dateitypzuordnung hinzufügen** die erforderlichen Informationen für das neue FTA an. Um die Verknüpfungsinformationen zu überprüfen, die einer Anwendung zugeordnet sind, wählen Sie unter der Anwendung **Verknüpfungen**aus, und im Bereich **Speicherort** können Sie die Symboldatei Informationen bearbeiten. Wenn Sie ein vorhandenes FTA bearbeiten möchten, klicken Sie auf **Bearbeiten**. Wenn Sie ein FTA entfernen möchten, wählen Sie das FTA aus, und klicken Sie dann auf **Entfernen**. Klicken Sie auf **Weiter**.

13. Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann. Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden. Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden, und klicken Sie dann auf **weiter**.

   **Hinweis:**  
   Wenn Sie verhindern möchten, dass eine Anwendung während dieses Schritts geladen wird, klicken Sie im Dialogfeld **Anwendungsstart** auf **Beenden**, und aktivieren Sie eines der Kontrollkästchen, **Beenden Sie alle Anwendungen** , oder **Beenden Sie nur diese Anwendung**, je nachdem, was Sie möchten.



14. Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann. Wenn Sie alle unterstützten Betriebssysteme in Ihrer Umgebung zum Ausführen dieses Pakets aktivieren möchten, wählen Sie zulassen, dass **Dieses Paket unter einem beliebigen Betriebssystem ausgeführt**wird. Wenn Sie dieses Paket so konfigurieren möchten, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, wählen Sie zulassen, dass **Dieses Paket nur für die folgenden Betriebssysteme ausgeführt** wird, und geben Sie die Betriebssysteme an, die dieses Paket ausführen können. Klicken Sie auf **Weiter**.

   **Wichtig**  
   Die während dieses Schritts angegebenen Betriebssysteme reflektieren die Betriebssysteme auf den Zielcomputern, die für die Ausführung des Pakets aktiviert sind. Sie müssen sicherstellen, dass die angegebenen Betriebssysteme von der von Ihnen sequenzierten Anwendung unterstützt werden.



15. Wenn Sie das Paket auf der Seite **Paket erstellen** ändern möchten, ohne es zu speichern, wählen Sie weiter aus, um das Paket **ohne Speichern mithilfe des Paket-Editors zu ändern**. Wenn Sie diese Option auswählen, wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können. Klicken Sie auf **Weiter**.

   Wenn Sie das Paket sofort speichern möchten, wählen Sie das Standard **Paket jetzt speichern**aus. Hinzufügen optionaler **Kommentare** , die dem Paket zugeordnet werden. Kommentare sind hilfreich, um Version und andere Informationen zum Paket zu identifizieren. Der Standard **Speicherort** wird ebenfalls angezeigt. Wenn Sie den Standardspeicherort ändern möchten, klicken Sie auf **Durchsuchen** , und geben Sie den neuen Speicherort an. Die Größe des unkomprimierten Pakets wird angezeigt. Wenn die Paketgröße 4 GB (unkomprimiert) überschreitet und Sie das Paket auf Zielcomputer streamen möchten, müssen Sie **Paket komprimieren**auswählen. Klicken Sie auf **Erstellen**.

16. Klicken Sie auf der Seite **Fertigstellung** nach dem Überprüfen der Informationen, die im Bereich **Bericht des virtuellen Anwendungspakets** angezeigt werden, auf **Schließen**. Die Informationen, die im Bereich " **virtueller Anwendungspaket Bericht** " angezeigt werden, sind auch in dem in Schritt 15 dieses Verfahrens angegebenen Verzeichnis in einer Datei mit dem Namen **Report.xml**verfügbar.

    Das Paket steht jetzt im Sequencer zur Verfügung. Um die Paketeigenschaften zu bearbeiten, klicken Sie auf **Bearbeiten \ [Package Name \]**. Weitere Informationen zum Ändern eines Pakets finden Sie unter [so wird es gemacht: Ändern eines vorhandenen virtuellen Anwendungspakets (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)

    **Wichtig**  
    Nachdem Sie ein virtuelles Anwendungspaket erfolgreich erstellt haben, können Sie das virtuelle Anwendungspaket nicht auf dem Computer ausführen, auf dem der Sequencer ausgeführt wird.



## Verwandte Themen


[Aufgaben für Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Ermitteln, welche Art von Anwendung zu sequenzieren ist (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









