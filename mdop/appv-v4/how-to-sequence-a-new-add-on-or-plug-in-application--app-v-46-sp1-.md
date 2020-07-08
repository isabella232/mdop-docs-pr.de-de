---
title: So sequenzieren Sie eine neue Add-On- oder Plug-In-Anwendung (App-V 4.6 SP1)
description: So sequenzieren Sie eine neue Add-On- oder Plug-In-Anwendung (App-V 4.6 SP1)
author: dansimp
ms.assetid: 2c018215-66e5-4301-8481-159891a6b35b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5c5bc1e96ead819459cda3879127ebdaf94f0ee7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806815"
---
# So sequenzieren Sie eine neue Add-On- oder Plug-In-Anwendung (App-V 4.6 SP1)


Gehen Sie wie folgt vor, um ein neues Add-on-oder Plug-in-virtuelles Anwendungspaket zu erstellen, indem Sie den Application Virtualization (App-V)-Sequenzer verwenden. Bei einer Add-on-oder Plug-in-Anwendung handelt es sich um eine Anwendung, die die Funktionalität einer Anwendung erweitert, beispielsweise ein Plug-in für Microsoft Excel. Weitere Informationen zu den Arten von Anwendungen, die Sie abbilden können, finden Sie unter [So ermitteln Sie, welche Art von Anwendung in der Reihenfolge ausgeführt wird (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

**Wichtig**  
Bevor Sie das folgende Verfahren ausführen, installieren Sie die übergeordnete Anwendung lokal auf dem Computer, auf dem der Sequencer ausgeführt wird. Wenn Sie beispielsweise ein Plug-in für Microsoft Excel sequenzieren, installieren Sie Microsoft Excel lokal auf dem Computer, auf dem der Sequencer ausgeführt wird. Installieren Sie die übergeordnete Anwendung auch im gleichen Verzeichnis, in dem die Anwendung auf den Zielcomputern installiert ist. Wenn das Plug-in oder Add-on mit einem vorhandenen virtuellen Anwendungspaket verwendet werden soll, installieren Sie die Anwendung auf dem virtuellen Anwendungs Laufwerk, das beim Erstellen des übergeordneten virtuellen Anwendungspakets verwendet wurde.



Sie können auch ein vorhandenes virtuelles Anwendungspaket als übergeordnete Anwendung verwenden. Gehen Sie wie folgt vor, um ein vorhandenes virtuelles Anwendungspaket zu verwenden, bevor Sie das neue Add-on oder Plug-in sequenzieren.

1.  Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Wenn Sie ein vorhandenes Paket auf den Computer erweitern möchten, auf dem der Sequencer ausgeführt wird, klicken Sie auf **Extras**  /  **Paket auf Lokales System erweitern**.

3.  Navigieren Sie zu dem Paket (**SPRJ** -Datei), das Sie erweitern möchten, und wählen Sie es aus, und klicken Sie dann auf **Öffnen**. Fahren Sie mit dem folgenden Verfahren fort.

**So Sequenzieren Sie ein neues Add-on oder eine Plug-in-Anwendung**

1.  Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie zum Starten des **Assistenten zum Erstellen eines neuen Pakets**auf **Neues virtuelles Anwendungspaket erstellen**. Wenn Sie das Paket erstellen möchten, wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.

3.  Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt, oder wenn das Paket unnötige Daten enthält. Wir empfehlen dringend, dass Sie alle potenziellen Probleme beheben, bevor Sie fortfahren. Nachdem Sie die Konflikte behoben haben, klicken Sie auf **Aktualisieren**, um die angezeigten Informationen zu aktualisieren. Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.

    **Wichtig**  
    Wenn Sie die Virenscansoftware deaktivieren müssen, überprüfen Sie den Computer, auf dem der Sequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder bösartigen Dateien hinzugefügt werden können.



4.  Wählen Sie auf der Seite **Art der Anwendung** **Add-on oder Plug-in**aus, und klicken Sie dann auf **weiter**.

    Weitere Informationen zu den Arten von Anwendungen, die Sie abbilden können, finden Sie unter so wird es [gemacht: Ermitteln des zu sequenzenden Anwendungstyps (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für das Add-on oder das Plug-in an. Wenn die Anwendung keine zugeordnete Installationsdatei hat und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.

6.  Klicken Sie auf der Seite **primäre auswählen** auf **Durchsuchen** , und geben Sie die übergeordnete Anwendung an.

    **Wichtig**  
    Wenn die übergeordnete Anwendung, die das Add-on oder das Plug-in, das Sie installieren, unterstützt wird, nicht lokal installiert wurde, beenden Sie hier, und installieren Sie die Anwendung auf dem Computer, auf dem der Sequencer ausgeführt wird. Beispielsweise muss die **Excel.exe** -Programmdatei lokal für ein Microsoft Excel-Plug-in installiert werden.



~~~
Click **Next**.
~~~

7. Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll. Verwenden Sie einen Namen, der hilft, den Zweck und die Version der Anwendung zu identifizieren, die dem Paket hinzugefügt werden soll. Der Paket Name wird auch in der App-V-Verwaltungskonsole angezeigt. Der **Installationsspeicherort** zeigt den Application Virtualization Path an, in dem die Anwendung installiert wird. Um diesen Speicherort zu bearbeiten, wählen Sie **Bearbeiten (erweitert)** aus.

   **Wichtig**  
   Das Bearbeiten des Application Virtualization path ist eine erweiterte Konfigurationsaufgabe. Sie sollten die Auswirkungen einer Änderung des Pfads vollständig verstehen. Für die meisten Anwendungen empfehlen wir den Standardpfad.



~~~
Click **Next**.
~~~

8. Installieren Sie auf der Seite **Installation** das Plug-in oder die Add-in-Anwendung, wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, damit der Sequencer den Installationsvorgang überwachen kann. Führen Sie die Installation mithilfe des Installationsvorgangs der Anwendung durch. Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen** , und führen Sie die zusätzlichen Installationsdateien aus. Wenn Sie die Installation abgeschlossen haben, wählen Sie **Ich habe die Installation abgeschlossen**aus, und klicken Sie dann auf **weiter**.

9. Auf der Seite **Installationsbericht** können Sie Informationen zu dem soeben sequenzierten virtuellen Anwendungspaket überprüfen. Eine detailliertere Erläuterung der Informationen, die in **zusätzlichen Informationen**angezeigt werden, finden Sie, indem Sie auf das Ereignis doppelklicken. Nachdem Sie die Informationen überprüft haben, klicken Sie auf **weiter**.

10. Wenn Sie die Installation und Konfiguration der virtuellen Anwendung abgeschlossen haben, wählen Sie auf der Seite **Anpassen** die Option **jetzt beenden** aus, und fahren Sie mit Schritt 14 dieser Vorgehensweise fort. Wenn Sie die Elemente in der folgenden Liste anpassen möchten, wählen Sie **Anpassen**aus.

    -   Bearbeiten Sie die Dateitypzuordnungen, die einer Anwendung zugeordnet sind.

    -   Vorbereiten des virtuellen Pakets für Streaming. Durch Streaming wird die Benutzerfreundlichkeit verbessert, wenn das virtuelle Anwendungspaket auf Zielcomputern ausgeführt wird.

    -   Geben Sie die Betriebssysteme an, die dieses Paket ausführen können.

    Klicken Sie auf **Weiter**.

11. Auf der Seite **Verknüpfungen bearbeiten** können Sie optional die Dateitypen Zuordnungen (FTA) konfigurieren, die den verschiedenen Anwendungen im Paket zugeordnet werden. Wenn Sie ein neues FTA erstellen möchten, wählen Sie im linken Bereich die Anwendung aus, die Sie anpassen möchten, und klicken Sie dann auf **Hinzufügen**. Geben Sie im Dialogfeld **Dateitypzuordnung hinzufügen** die erforderlichen Informationen für das neue FTA an. Wählen Sie unter der Anwendung **Verknüpfungen** aus, um die Verknüpfungsinformationen zu überprüfen, die einer Anwendung zugeordnet sind. Im Bereich **Speicherort** können Sie die Symboldatei Informationen überprüfen. Wenn Sie ein vorhandenes FTA bearbeiten möchten, klicken Sie auf **Bearbeiten**. Wenn Sie ein FTA entfernen möchten, wählen Sie das FTA aus, und klicken Sie dann auf **Entfernen**. Klicken Sie auf **Weiter**.

12. Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann. Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden. Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden, und klicken Sie dann auf **weiter**.

   **Hinweis:**  
   Wenn Sie verhindern möchten, dass eine Anwendung während dieses Schritts geladen wird, klicken Sie im Dialogfeld **Anwendungsstart** auf **Beenden** , und aktivieren Sie eines der Kontrollkästchen, **Beenden Sie alle Anwendungen** , oder **Beenden Sie nur diese Anwendung**.



13. Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann. Wenn Sie alle unterstützten Betriebssysteme in Ihrer Umgebung zum Ausführen dieses Pakets aktivieren möchten, aktivieren Sie das Kontrollkästchen **Dieses Paket kann auf einem beliebigen Betriebssystem ausgeführt** werden. Um dieses Paket so zu konfigurieren, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, aktivieren Sie das Kontrollkästchen **Dieses Paket nur auf den folgenden Betriebssystemen ausführen lassen** , und wählen Sie dann die Betriebssysteme aus, die dieses Paket ausführen können. Klicken Sie auf **Weiter**.

14. Wenn Sie das Paket auf der Seite **Paket erstellen** ändern möchten, ohne es zu speichern, wählen Sie **zum Ändern des Pakets ohne Speichern über das** Kontrollkästchen Paket-Editor die Option weiter aus. Wenn Sie diese Option auswählen, wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können. Klicken Sie auf **Weiter**.

   Wenn Sie das Paket sofort speichern möchten, wählen Sie das Standard **Paket jetzt speichern**aus. Optional können Sie **Kommentare** auswählen, um Kommentare hinzuzufügen, die dem Paket zugeordnet werden. Kommentare sind hilfreich, um Version und andere Informationen zum Paket zu identifizieren. Der Standard **Speicherort** wird ebenfalls angezeigt. Wenn Sie den Standardspeicherort ändern möchten, klicken Sie auf **Durchsuchen** , und geben Sie den neuen Speicherort an. Die Größe des unkomprimierten Pakets wird angezeigt. Wenn die Paketgröße 4 GB (unkomprimiert) überschreitet und Sie das Paket auf Zielcomputer streamen möchten, müssen Sie **Paket komprimieren**auswählen. Klicken Sie auf **Erstellen**.

15. Klicken Sie auf der Seite **Fertigstellung** auf **Schließen**, nachdem Sie die Informationen überprüft haben, die im **Bericht Bereich erfolgreiches virtuelles Anwendungspaket** angezeigt werden. Die Informationen, die im Bereich für den **erfolgreichen virtuellen Anwendungspaket Bericht** angezeigt werden, sind auch in dem in Schritt 14 dieses Verfahrens angegebenen Verzeichnis in einer Datei mit dem Namen **Reports.xml**verfügbar.

   Das Paket steht jetzt im Sequencer zur Verfügung. Klicken Sie auf **Bearbeiten \ [Package Name \]** , um die Paketeigenschaften zu bearbeiten. Weitere Informationen zum Ändern eines Pakets finden Sie unter [so wird es gemacht: Ändern eines vorhandenen virtuellen Anwendungspakets (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).

   **Wichtig**  
   Nachdem Sie ein virtuelles Anwendungspaket erfolgreich erstellt haben, können Sie das virtuelle Anwendungspaket nicht auf dem Computer ausführen, auf dem der Sequencer ausgeführt wird.



## Verwandte Themen


[Aufgaben für Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Ermitteln, welche Art von Anwendung zu sequenzieren ist (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









