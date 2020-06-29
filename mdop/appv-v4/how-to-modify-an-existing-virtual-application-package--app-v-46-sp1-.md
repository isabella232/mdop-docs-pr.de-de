---
title: So ändern Sie ein vorhandenes virtuelles Anwendungspaket (App-V 4.6 SP1)
description: So ändern Sie ein vorhandenes virtuelles Anwendungspaket (App-V 4.6 SP1)
author: dansimp
ms.assetid: f43a9927-4325-4b2d-829f-3068e4e84349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0e9d45a32afa240ce7f6fb2ee5dfbc51889c1fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806947"
---
# So ändern Sie ein vorhandenes virtuelles Anwendungspaket (App-V 4.6 SP1)


Gehen Sie wie folgt vor, um ein vorhandenes virtuelles Anwendungspaket zu ändern. Sie können diese Verfahren für folgende Zwecke verwenden:

-   Aktualisieren Sie eine Anwendung, die Teil eines vorhandenen virtuellen Anwendungspakets ist. Verwenden Sie zum Ausführen dieser Aufgabe das Verfahren **"so aktualisieren Sie eine Anwendung in einem vorhandenen Anwendungspaket"** in diesem Dokument.

-   Ändern Sie die Eigenschaften, die einem vorhandenen virtuellen Anwendungspaket zugeordnet sind. Verwenden Sie zum Ausführen dieser Aufgabe das Verfahren **"so ändern Sie die Eigenschaften, die einem vorhandenen virtuellen Anwendungspaket zugeordnet sind"** in diesem Dokument.

-   Hinzufügen einer neuen Anwendung zu einem vorhandenen virtuellen Anwendungspaket Verwenden Sie zum Ausführen dieser Aufgabe das Verfahren **"So fügen Sie eine neue Anwendung zu einem vorhandenen virtuellen Anwendungspaket hinzu"** in diesem Dokument ein.

Zum Ändern eines virtuellen Anwendungspakets muss der App-V Sequencer installiert sein. Weitere Informationen zum Installieren des App-v-Sequencers finden Sie unter so wird es [gemacht: Installieren des Sequencers (app-v 4,6 SP1)](how-to-install-the-sequencer---app-v-46-sp1-.md).

**So aktualisieren Sie eine Anwendung in einem vorhandenen virtuellen Anwendungspaket**

1.  Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie im App-V-Sequencer auf **vorhandenes virtuelles Anwendungspaket ändern**, und klicken Sie dann auf **weiter**.

3.  Klicken Sie auf der Seite **Aufgabe auswählen** auf **Anwendung in bestehendem Paket aktualisieren**, und klicken Sie dann auf **weiter**.

4.  Klicken Sie auf der Seite **Paket auswählen** auf **Durchsuchen** , um das virtuelle Anwendungspaket zu finden, das die Anwendung enthält, die Sie aktualisieren möchten, und klicken Sie dann auf **weiter**.

5.  Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Aktualisierung der Anwendung fehlschlägt, oder dass das Anwendungsupdate unnötige Daten enthält. Wir empfehlen dringend, dass Sie alle potenziellen Probleme beheben, bevor Sie fortfahren. Nachdem Sie die Konflikte behoben haben, klicken Sie auf **Aktualisieren**, um die angezeigten Informationen zu aktualisieren. Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.

    **Wichtig**  Wenn Sie die Virenscansoftware deaktivieren müssen, überprüfen Sie den Computer, auf dem der Sequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder bösartigen Dateien hinzugefügt werden.

     

6.  Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Update Installationsdatei für die Anwendung an. Wenn dem Update keine Installationsdatei zugeordnet ist und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.

7.  Installieren Sie auf der **Installations** Seite, wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, das Anwendungsupdate, damit der Sequencer den Installationsvorgang überwachen kann. Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen** , und führen Sie die zusätzlichen Installationsdateien aus. Wenn Sie die Installation abgeschlossen haben, wählen Sie **Ich habe die Installation abgeschlossen**aus. Klicken Sie auf **Weiter**.

    **Hinweis**  Der Sequencer überwacht alle Änderungen und Installationen auf dem Computer, auf dem der Sequencer ausgeführt wird, einschließlich der Änderungen und Installationen, die außerhalb des Sequenz-Assistenten ausgeführt werden.

     

8.  Auf der Seite " **Installationsbericht** " können Sie Informationen zu der soeben aktualisierten virtuellen Anwendung anzeigen. Eine detailliertere Erläuterung der Informationen, die in **zusätzlichen Informationen**angezeigt werden, finden Sie, indem Sie auf das Ereignis doppelklicken. Nachdem Sie die Informationen überprüft haben, klicken Sie auf **weiter**.

9.  Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann. Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden. Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden, und klicken Sie dann auf **weiter**.

    **Hinweis**  Wenn Sie verhindern möchten, dass eine Anwendung während dieses Schritts geladen wird, klicken Sie im Dialogfeld **Anwendungsstart** auf **Beenden**, und klicken Sie dann auf eine der folgenden Optionen: **alle Anwendungen beenden** oder **nur diese Anwendung beenden**, je nachdem, was Sie wünschen.

     

10. Wenn Sie das Paket auf der Seite **Paket erstellen** ändern möchten, ohne es zu speichern, aktivieren Sie das Kontrollkästchen **Paket ohne Speichern mithilfe des Paket-Editors weiter ändern** . Wenn Sie diese Option auswählen, wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können. Klicken Sie auf **Weiter**.

    Wenn Sie das Paket sofort speichern möchten, wählen Sie das Standard **Paket jetzt speichern**aus. Hinzufügen optionaler **Kommentare** , die dem Paket zugeordnet werden. Kommentare sind hilfreich, um Version und andere Informationen zum Paket zu identifizieren. Der Standard **Speicherort** wird ebenfalls angezeigt. Wenn Sie den Standardspeicherort ändern möchten, klicken Sie auf **Durchsuchen** , und geben Sie den neuen Speicherort an. Die Größe des unkomprimierten Pakets wird angezeigt. Wenn die Paketgröße 4 GB überschreitet (unkomprimiert) und Sie das Paket auf die Zielcomputer streamen möchten, müssen Sie **Paket komprimieren**auswählen und dann auf **Erstellen**klicken.

11. Klicken Sie auf der Seite **Fertigstellung** auf **Schließen** , um den Assistenten zu schließen. Das Paket steht jetzt im Sequencer zur Verfügung.

**So ändern Sie die Eigenschaften, die einem vorhandenen virtuellen Anwendungspaket zugeordnet sind**

1.  Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie im App-V-Sequencer auf **vorhandenes virtuelles Anwendungspaket ändern**, und klicken Sie dann auf **weiter**.

3.  Klicken Sie auf der Seite **Aufgabe auswählen** auf **Paket bearbeiten**, und klicken Sie dann auf **weiter**.

4.  Klicken Sie auf der Seite **Paket auswählen** auf **Durchsuchen** , um das virtuelle Anwendungspaket zu finden, das die Anwendungseigenschaften enthält, die Sie ändern möchten, und klicken Sie dann auf **Bearbeiten**.

5.  In der Sequencer-Konsole können Sie eine der folgenden Aufgaben ausführen:

    -   Anzeigen von Paketeigenschaften.

    -   Anzeigen des Paket Änderungsverlaufs

    -   Anzeigen zugehöriger Paketdateien

    -   Bearbeiten Sie die Registrierungseinstellungen.

    -   Überprüfen Sie die zusätzlichen Paketeinstellungen (mit Ausnahme der Dateieigenschaften des Betriebssystems).

    -   Erstellen Sie einen zugehörigen Windows Installer (MSI).

    -   OSD-Datei ändern.

    -   Komprimieren und Dekomprimieren des Pakets.

    -   Dateitypzuordnungen hinzufügen.

    -   Einrichten des virtualisierten Registrierungsschlüssel Zustands (überschreiben oder zusammenführen)

    -   Legen Sie den Status eines virtualisierten Ordners fest.

    -   Bearbeiten von virtuellen Dateisystem Zuordnungen

6.  Wenn Sie die Paketeigenschaften geändert haben, klicken Sie auf **Datei**  /  **Speichern** , um das Paket zu speichern.

**So fügen Sie eine neue Anwendung zu einem vorhandenen virtuellen Anwendungspaket hinzu**

1.  Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie im App-V-Sequencer auf **vorhandenes virtuelles Anwendungspaket ändern**, und klicken Sie dann auf **weiter**.

3.  Klicken Sie auf der Seite **Aufgabe auswählen** auf **neue Anwendung hinzufügen**, und klicken Sie dann auf **weiter**.

4.  Klicken Sie auf der Seite **Paket auswählen** auf **Durchsuchen** , um nach dem virtuellen Anwendungspaket zu suchen, dem Sie die Anwendung hinzufügen möchten, und klicken Sie dann auf **weiter**.

5.  Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt, oder wenn die Aktualisierung keine unnötigen Daten enthält. Wir empfehlen dringend, dass Sie alle potenziellen Probleme beheben, bevor Sie fortfahren. Nachdem Sie die Konflikte behoben haben, klicken Sie auf **Aktualisieren**, um die angezeigten Informationen zu aktualisieren. Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.

    **Wichtig**  Wenn Sie die Virenscansoftware deaktivieren müssen, überprüfen Sie den Computer, auf dem der Sequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder bösartigen Dateien hinzugefügt werden können.

     

6.  Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für die Anwendung an. Wenn die Anwendung keine zugeordnete Installationsdatei hat und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.

7.  Installieren Sie die Anwendung auf der **Installations** Seite, wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, damit der Sequencer den Installationsvorgang überwachen kann. Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen**, und suchen Sie die zusätzlichen Installationsdateien, und führen Sie Sie aus. Wenn Sie die Installation abgeschlossen haben, wählen Sie **Ich habe die Installation abgeschlossen**aus. Klicken Sie auf **Weiter**. Geben Sie im Dialogfeld **Ordner suchen** das primäre Verzeichnis an, in dem die Anwendung installiert werden soll. Dies sollte ein neuer Speicherort sein, damit Sie die vorhandene Version des virtuellen Anwendungspakets nicht überschreiben.

    **Hinweis**  Alle Änderungen und Installationen auf dem Computer, auf dem der Sequencer ausgeführt wird, werden vom Sequencer überwacht, einschließlich der Änderungen und Installationen, die außerhalb des Sequenz-Assistenten ausgeführt werden.

     

8.  Führen Sie auf der Seite **Software konfigurieren** optional die Programme aus, die im Paket enthalten sind. Mit diesem Schritt können Sie alle zugehörigen Lizenz-oder Konfigurationsaufgaben ausführen, die für die Ausführung der Anwendung erforderlich sind, bevor Sie das Paket auf Zielcomputern bereitstellen und ausführen. Wenn Sie alle Programme gleichzeitig ausführen möchten, wählen Sie mindestens ein Programm aus, und klicken Sie dann auf **alle ausführen**. Wenn Sie bestimmte Programme ausführen möchten, wählen Sie das Programm oder die Programme aus, die Sie ausführen möchten, und klicken Sie dann auf **ausgewählte ausführen**. Führen Sie die erforderlichen Konfigurationsaufgaben aus, und schließen Sie dann die Anwendungen. Es kann mehrere Minuten dauern, bis alle Programme ausgeführt werden. Klicken Sie auf **Weiter**.

9.  Auf der Seite " **Installationsbericht** " können Sie Informationen zu der soeben aktualisierten virtuellen Anwendung anzeigen. Eine detailliertere Erläuterung der Informationen, die in **zusätzlichen Informationen**angezeigt werden, finden Sie, indem Sie auf das Ereignis doppelklicken. Nachdem Sie die Informationen überprüft haben, klicken Sie auf **weiter**.

10. Wenn Sie die Installation und Konfiguration der virtuellen Anwendung abgeschlossen haben, wählen Sie auf der Seite **Anpassen** die Option **jetzt beenden** aus, und fahren Sie mit Schritt 14 dieser Vorgehensweise fort. Wenn Sie die Elemente in der folgenden Liste anpassen möchten, klicken Sie auf **Anpassen**.

    -   Bearbeiten Sie die Dateitypzuordnungen, die einer Anwendung zugeordnet sind.

    -   Vorbereiten des virtuellen Pakets für Streaming. Durch Streaming wird die Benutzerfreundlichkeit verbessert, wenn das virtuelle Anwendungspaket auf Zielcomputern ausgeführt wird.

    Klicken Sie auf **Weiter**.

11. Auf der Seite **Verknüpfungen bearbeiten** können Sie optional die Dateitypen Zuordnungen (FTA) konfigurieren, die den verschiedenen Anwendungen im Paket zugeordnet werden. Wenn Sie ein neues FTA erstellen möchten, wählen Sie im linken Bereich die Anwendung aus, die Sie anpassen möchten, und erweitern Sie Sie, und klicken Sie dann auf **Hinzufügen**. Geben Sie im Dialogfeld **Dateitypzuordnung hinzufügen** die erforderlichen Informationen für das neue FTA an. Um die Verknüpfungsinformationen zu überprüfen, die einer Anwendung zugeordnet sind, aktivieren Sie unter der Anwendung das Kontrollkästchen **Verknüpfungen** , und im Bereich **Speicherort** können Sie die Informationen zu den Symboldateien überprüfen. Wenn Sie ein vorhandenes FTA bearbeiten möchten, klicken Sie auf **Bearbeiten**. Wenn Sie ein FTA entfernen möchten, wählen Sie das FTA aus, und klicken Sie dann auf **Entfernen**. Klicken Sie auf **Weiter**.

12. Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann. Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden. Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden, und klicken Sie dann auf **weiter**.

    **Hinweis**  Wenn Sie verhindern möchten, dass eine Anwendung während dieses Schritts geladen wird, klicken Sie im Dialogfeld **Anwendungsstart** auf **Beenden** , und aktivieren Sie je nach Wunsch entweder das Kontrollkästchen **alle Anwendungen beenden** oder **nur diese Anwendung beenden** .

     

13. Aktivieren Sie auf der Seite **Paket erstellen** das Kontrollkästchen Paket **-Editor weiterhin ohne Speichern verwenden** , um das Paket ohne speichern zu ändern. Wenn Sie diese Option auswählen, wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können. Klicken Sie auf **Weiter**.

    Wählen Sie das Standard **Paket jetzt speichern**aus, um das Paket sofort zu speichern. Hinzufügen optionaler **Kommentare** , die dem Paket zugeordnet werden. Kommentare sind hilfreich, um Version und andere Informationen zum Paket zu identifizieren. Der Standard **Speicherort** wird ebenfalls angezeigt. Wenn Sie den Standardspeicherort ändern möchten, klicken Sie auf **Durchsuchen** , und geben Sie den neuen Speicherort an. Die Größe des unkomprimierten Pakets wird angezeigt. Wenn die Paketgröße 4 GB (unkomprimiert) überschreitet und Sie das Paket auf Zielcomputer streamen möchten, müssen Sie **Paket komprimieren**auswählen. Klicken Sie auf **Erstellen**.

14. Klicken Sie auf der Seite **Fertigstellung** auf **Schließen**. Das Paket steht jetzt im Sequencer zur Verfügung.

## Verwandte Themen


[Aufgaben für Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





