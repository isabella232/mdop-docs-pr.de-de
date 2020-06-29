---
title: So ändern Sie ein vorhandenes virtuelles Anwendungspaket
description: So ändern Sie ein vorhandenes virtuelles Anwendungspaket
author: dansimp
ms.assetid: 86b0fe21-52b0-4a9c-9a66-c78935fe74f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 55fbaaa1f3bf4f406d813215146c58e7da2bfe59
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805288"
---
# So ändern Sie ein vorhandenes virtuelles Anwendungspaket


In diesem Thema wird erläutert, wie Sie:

-   [Aktualisieren einer Anwendung in einem vorhandenen virtuellen Anwendungspaket](#bkmk-update-app-in-pkg)

-   [Ändern der Eigenschaften, die einem vorhandenen virtuellen Anwendungspaket zugeordnet sind](#bkmk-chg-props-in-pkg)

-   [Hinzufügen einer neuen Anwendung zu einem vorhandenen virtuellen Anwendungspaket](#bkmk-add-app-to-pkg)

**Bevor Sie ein Paket aktualisieren:**

-   Stellen Sie sicher, dass Sie den Microsoft Application Virtualization (App-V)-Sequenzer installiert haben, der zum Ändern eines virtuellen Anwendungspakets erforderlich ist. Informationen zum Installieren von App-V Sequencer finden Sie unter so wird es [gemacht: Installieren des Sequencers](how-to-install-the-sequencer-beta-gb18030.md).

-   Speichern Sie die AppV-Datei an einem sicheren Speicherort, und Vertrauen Sie der Quelle immer, bevor Sie versuchen, das Paket zur Bearbeitung zu öffnen.

-   Der Abschnitt "Verwaltungsautorität" wird irrtümlich aus der Bereitstellungs Konfigurationsdatei entfernt, wenn Sie ein Paket aktualisieren. Kopieren Sie vor dem Starten des Updates den Abschnitt "Verwaltungsautorität" aus der vorhandenen Bereitstellungs Konfigurationsdatei, und fügen Sie den kopierten Abschnitt dann in die neue Konfigurationsdatei ein, nachdem die Konvertierung abgeschlossen ist.

-   Wenn Sie im Sequencer auf **vorhandenes virtuelles Anwendungspaket ändern** klicken, um ein Paket zu bearbeiten, aber dann keine Änderungen vorzunehmen und das Paket zu schließen, wird das Streaming-Verhalten des Pakets geändert. Der primäre Feature-Block wird aus der StreamMap.xml-Datei entfernt, und alle im Veröffentlichungsfeature-Block aufgeführten Dateien werden entfernt. Benutzer, die das bearbeitete Paket erhalten, erleben dieses Paket so, als ob es Datenstromfehler Haft war, unabhängig davon, wie das ursprüngliche Paket konfiguriert wurde.

<a href="" id="bkmk-update-app-in-pkg"></a>**Aktualisieren einer Anwendung in einem vorhandenen virtuellen Anwendungspaket**

1.  Klicken Sie auf dem Computer, auf dem der Sequencer ausgeführt wird, auf **Alle Programme**, zeigen Sie auf **Microsoft Application Virtualization**, und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie im App-V-Sequencer auf **vorhandenes virtuelles Anwendungspaket ändern** &gt; **als nächstes**.

3.  Klicken Sie auf der Seite **Aufgabe auswählen** auf **Anwendung in bestehendem Paket** &gt; **weiter**aktualisieren.

4.  Klicken Sie auf der Seite **Paket auswählen** auf **Durchsuchen** , um nach dem virtuellen Anwendungspaket zu suchen, das die zu aktualisierende Anwendung enthält, und klicken Sie dann auf **weiter**.

5.  Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Anwendungsaktualisierung fehlschlägt oder die aktualisierte Anwendung keine unnötigen Daten enthält. Beheben Sie alle potenziellen Probleme, bevor Sie fortfahren. Klicken Sie nach dem vornehmen von Korrekturen und dem Beheben aller potenziellen **Refresh** Probleme auf &gt; **weiter**aktualisieren.

    **Wichtig**  Wenn Sie die Virenscansoftware deaktivieren müssen, überprüfen Sie zuerst den Computer, der den Sequencer ausführt, um sicherzustellen, dass dem Paket keine unerwünschten oder bösartigen Dateien hinzugefügt werden.

6.  Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Update Installationsdatei für die Anwendung an. Wenn dem Update keine Installationsdatei zugeordnet ist und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.

7.  Wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, können Sie auf der **Installations** Seite fortfahren, das Anwendungsupdate zu installieren, damit der Sequencer den Installationsvorgang überwachen kann. Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen**, und suchen Sie dann die zusätzlichen Installationsdateien, und führen Sie Sie aus. Wenn Sie die Installation abgeschlossen haben, wählen Sie **Ich habe die Installation abgeschlossen**aus. Klicken Sie auf **Weiter**.

    **Hinweis**  Der Sequencer überwacht alle Änderungen und Installationen, die auf dem Computer erfolgen, auf dem der Sequencer ausgeführt wird. Dies umfasst alle Änderungen und Installationen, die außerhalb des Sequenz-Assistenten ausgeführt werden.

8.  Auf der Seite " **Installationsbericht** " können Sie Informationen zur aktualisierten virtuellen Anwendung anzeigen. Wenn Sie weitere **Informationen**benötigen, doppelklicken Sie auf das Ereignis, um detailliertere Informationen zu erhalten. Klicken Sie auf **weiter**, um fortzufahren.

9.  Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann. Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden. Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden, und klicken Sie dann auf **weiter**.

    **Hinweis**  Sie können verhindern, dass eine Anwendung während dieses Schritts geladen wird. Klicken Sie im Dialogfeld **Anwendungsstart** auf **Beenden**, und wählen Sie dann entweder **alle Anwendungen beenden** oder **nur diese Anwendung beenden**aus.

10. Aktivieren Sie auf der Seite **Paket erstellen** das Kontrollkästchen zum Ändern des Pakets **ohne Speichern mithilfe des Paket-Editors**, um das Paket zu ändern, ohne es zu speichern. Wenn Sie diese Option auswählen, wird das Paket in der App-V Sequencer-Konsole geöffnet, in der Sie das Paket vor dem Speichern ändern können. Klicken Sie auf **Weiter**.

    Wenn Sie das Paket sofort speichern möchten, wählen Sie das Standard **Paket jetzt speichern**aus. Fügen Sie optionale **Kommentare** hinzu, die dem Paket zugeordnet werden sollen. Kommentare sind hilfreich, um die Anwendungsversion zu identifizieren und weitere Informationen zum Paket bereitzustellen. Der Standard **Speicherort** wird ebenfalls angezeigt. Wenn Sie den Standardspeicherort ändern möchten, klicken Sie auf **Durchsuchen** , und geben Sie den neuen Speicherort an. Klicken Sie auf **Erstellen**.

11. Klicken Sie auf der Seite **Fertigstellung** auf **Schließen** , um den Assistenten zu schließen. Das Paket steht jetzt im Sequencer zur Verfügung.

<a href="" id="bkmk-chg-props-in-pkg"></a>**Ändern der Eigenschaften, die einem vorhandenen virtuellen Anwendungspaket zugeordnet sind**

1.  Klicken Sie auf dem Computer, auf dem der Sequencer ausgeführt wird, auf **Alle Programme**, zeigen Sie auf **Microsoft Application Virtualization**, und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie im App-V-Sequencer auf **vorhandenes virtuelles Anwendungspaket ändern** &gt; **als nächstes**.

3.  Klicken Sie auf der Seite **Aufgabe auswählen** auf nächstes **Paket bearbeiten** &gt; **Next**.

4.  Klicken Sie auf der Seite **Paket auswählen** auf **Durchsuchen** , um das virtuelle Anwendungspaket zu finden, das die zu ändernden Anwendungseigenschaften enthält, und klicken Sie dann auf **Bearbeiten**.

5.  Führen Sie in der App-V Sequencer-Konsole nach Bedarf die folgenden Aufgaben aus:

    -   Anzeigen von Paketeigenschaften.

    -   Anzeigen zugehöriger Paketdateien

    -   Bearbeiten Sie die Registrierungseinstellungen.

    -   Überprüfen Sie die zusätzlichen Paketeinstellungen (mit Ausnahme der Dateieigenschaften des Betriebssystems).

    -   Einrichten des virtualisierten Registrierungsschlüssel Zustands (überschreiben oder zusammenführen)

    -   Legen Sie den Status eines virtualisierten Ordners fest.

    -   Hinzufügen oder Bearbeiten von Verknüpfungen und Dateitypzuordnungen

        **Hinweis**  Um Verknüpfungen oder Dateitypzuordnungen zu bearbeiten, müssen Sie zuerst das Paket für das Upgrade öffnen, um eine neue Anwendung hinzuzufügen, und dann zur letzten Bearbeitungsseite weiter gehen.

6.  Wenn Sie mit dem Ändern der Paketeigenschaften fertig sind, klicken Sie auf **Datei** &gt; **Speichern** , um das Paket zu speichern.

<a href="" id="bkmk-add-app-to-pkg"></a>**Hinzufügen einer neuen Anwendung zu einem vorhandenen virtuellen Anwendungspaket**

1.  Klicken Sie auf dem Computer, auf dem der Sequencer ausgeführt wird, auf **Alle Programme**, zeigen Sie auf **Microsoft Application Virtualization**, und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie im App-V-Sequencer auf **vorhandenes virtuelles Anwendungspaket ändern** &gt; **als nächstes**.

3.  Klicken Sie auf der Seite **Aufgabe auswählen** auf weitere **Anwendung hinzufügen** &gt; **Next**.

4.  Klicken Sie auf der Seite **Paket auswählen** auf **Durchsuchen** , um nach dem virtuellen Anwendungspaket zu suchen, dem Sie die Anwendung hinzufügen möchten, und klicken Sie dann auf **weiter**.

5.  Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt oder das überarbeitete Paket keine unnötigen Daten enthält. Beheben Sie alle potenziellen Probleme, bevor Sie fortfahren. Klicken Sie nach dem vornehmen von Korrekturen und dem Beheben aller potenziellen **Refresh** Probleme auf &gt; **weiter**aktualisieren.

    **Wichtig**  Wenn Sie die Virenscansoftware deaktivieren müssen, überprüfen Sie zuerst den Computer, der den Sequencer ausführt, um sicherzustellen, dass dem Paket keine unerwünschten oder bösartigen Dateien hinzugefügt werden können.

6.  Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für die Anwendung an. Wenn die Anwendung keine zugeordnete Installationsdatei hat und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.

7.  Installieren Sie die Anwendung auf der **Installations** Seite, wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, so, dass der Sequencer den Installationsvorgang überwachen kann. Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen**, und suchen Sie die zusätzlichen Installationsdateien, und führen Sie Sie aus. Wenn Sie die Installation abgeschlossen haben, wählen Sie **Ich habe** die Installation &gt; **als nächstes**abgeschlossen aus. Geben Sie im Dialogfeld **Ordner suchen** das primäre Verzeichnis an, in dem die Anwendung installiert werden soll. Stellen Sie sicher, dass es sich um einen neuen Speicherort handelt, damit Sie die vorhandene Version des virtuellen Anwendungspakets nicht überschreiben.

    **Hinweis**  Der Sequencer überwacht alle Änderungen und Installationen, die auf dem Computer erfolgen, auf dem der Sequencer ausgeführt wird. Dies umfasst alle Änderungen und Installationen, die außerhalb des Sequenz-Assistenten ausgeführt werden.

8.  Führen Sie auf der Seite **Software konfigurieren** optional die Programme aus, die im Paket enthalten sind. Dieser Schritt schließt alle zugehörigen Lizenz-oder Konfigurationsaufgaben ab, die erforderlich sind, um die Anwendung auszuführen, bevor Sie das Paket auf Zielcomputern bereitstellen und ausführen. Wenn Sie alle Programme gleichzeitig ausführen möchten, wählen Sie mindestens ein Programm aus, und klicken Sie dann auf **alle ausführen**. Wenn Sie bestimmte Programme ausführen möchten, wählen Sie das Programm oder die Programme aus, die Sie ausführen möchten, und klicken Sie dann auf **ausgewählte ausführen**. Führen Sie die erforderlichen Konfigurationsaufgaben aus, und schließen Sie dann die Anwendungen. Es kann mehrere Minuten dauern, bis alle Programme ausgeführt werden. Klicken Sie auf **Weiter**.

9.  Auf der Seite " **Installationsbericht** " können Sie Informationen zur aktualisierten virtuellen Anwendung anzeigen. Wenn Sie weitere **Informationen**benötigen, doppelklicken Sie auf das Ereignis, um detailliertere Informationen zu erhalten, und klicken Sie dann auf **weiter** , um die Seite **Anpassen** zu öffnen.

10. Wenn Sie die Installation und Konfiguration der virtuellen Anwendung abgeschlossen haben, wählen Sie **jetzt beenden** aus, und fahren Sie mit Schritt 13 dieses Verfahrens fort. Wenn Sie die folgende beschriebene Anpassung durchführen möchten, klicken Sie auf **Anpassen**.

    Wenn Sie eine Anpassung vornehmen, bereiten Sie das virtuelle Paket für das Streaming vor, und klicken Sie dann auf **weiter**. Durch Streaming wird die Benutzerfreundlichkeit verbessert, wenn das virtuelle Anwendungspaket auf Zielcomputern ausgeführt wird.

11. Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann. Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden. Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden, und klicken Sie dann auf **weiter**.

    **Hinweis**  Sie können verhindern, dass eine Anwendung während dieses Schritts geladen wird. Klicken Sie im Dialogfeld **Anwendungsstart** auf **Beenden** , und wählen Sie dann entweder **alle Anwendungen beenden** oder **nur diese Anwendung beenden**aus.

12. Wenn Sie das Paket auf der Seite **Paket erstellen** ändern möchten, ohne es zu speichern, aktivieren Sie das Kontrollkästchen **Paket ohne Speichern mithilfe des Paket-Editors weiter ändern** . Wenn Sie diese Option auswählen, wird das Paket in der App-V Sequencer-Konsole geöffnet, in der Sie das Paket vor dem Speichern ändern können. Klicken Sie auf **Weiter**.

    Wenn Sie das Paket sofort speichern möchten, wählen Sie das Standard **Paket jetzt speichern**aus. Fügen Sie optionale **Kommentare** hinzu, die dem Paket zugeordnet werden sollen. Kommentare sind hilfreich für die Bereitstellung von Anwendungsversionen und anderen Informationen über das Paket. Der Standard **Speicherort** wird ebenfalls angezeigt. Wenn Sie den Standardspeicherort ändern möchten, klicken Sie auf **Durchsuchen** , und geben Sie den neuen Speicherort an. Die Größe des unkomprimierten Pakets wird angezeigt. Klicken Sie auf **Erstellen**.

13. Klicken Sie auf der Seite **Fertigstellung** auf **Schließen**. Das Paket steht jetzt im Sequencer zur Verfügung.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen

[Vorgänge für App-V 5.0](operations-for-app-v-50.md)

 

 





