---
title: So sequenzieren Sie eine neue Middleware Anwendung (App-V 4.6 SP1)
description: So sequenzieren Sie eine neue Middleware Anwendung (App-V 4.6 SP1)
author: dansimp
ms.assetid: 304045c2-5e5e-4c91-b59e-a91fdf2500fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b26559b8f5c451d01fefe899e96a83dd388b8140
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806800"
---
# So sequenzieren Sie eine neue Middleware Anwendung (App-V 4.6 SP1)


Gehen Sie wie folgt vor, um ein neues Middleware Virtual Application-Paket mit Application Virtualization (App-V) Sequencer zu erstellen. Eine Middleware-Anwendung ist Software, die Softwaremodule oder Anwendungen verbindet. Weitere Informationen zu den Arten von Anwendungen, die Sie abbilden können, finden Sie unter so wird es [gemacht: Ermitteln des zu sequenzenden Anwendungstyps (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

Verwenden Sie diesen Pakettyp mithilfe der Dynamic Suite-Komposition in App-V. Mit der Dynamic Suite-Komposition können Sie ein virtuelles Anwendungspaket definieren, das von einem anderen virtuellen Anwendungspaket abhängig ist. Die Abhängigkeit ermöglicht der Anwendung die Interaktion mit der Middleware oder dem Plug-in in der virtuellen Umgebung, in der in der Regel diese Interaktion verhindert wird. Dies ist hilfreich, da ein sekundäres Anwendungspaket mit mehreren anderen primären Anwendungen verwendet werden kann, wodurch jede primäre Anwendung auf dasselbe sekundäre Paket verweisen kann. Weitere Informationen zum Verwenden der Dynamic Suite-Komposition finden Sie unter [Verwenden der Dynamic Suite-Komposition](https://go.microsoft.com/fwlink/?LinkID=203804&clcid=0x409) in der Microsoft Technical Library ( https://go.microsoft.com/fwlink/?LinkID=203804&clcid=0x409) .

**Wichtig**  
Wenn der Computer, auf dem der App-V-Sequenzer ausgeführt wird, Windows Vista oder Windows 7 ausführt und ein Neustart außerhalb der virtuellen Umgebung initiiert wird, beispielsweise **Start**  /  **Herunterfahren**, müssen Sie während der Sequenzierung auf **Abbrechen** klicken, wenn Sie aufgefordert werden, das Programm zu schließen, das verhindert, dass Windows beendet wird. Wenn Sie auf **Beenden erzwingen**klicken, schlägt die Paketerstellung fehl. Wenn Sie auf **Abbrechen**klicken, zeichnet App-V Sequencer den Neustart erfolgreich auf, während die Anwendung sequenziert wird.



**So Sequenzieren Sie eine neue Middleware-Anwendung**

1.  Um App-v Sequencer zu starten, klicken Sie auf dem Computer, auf dem App-v Sequencer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Klicken Sie zum Starten des **Assistenten zum Erstellen eines neuen Pakets**auf **Neues virtuelles Anwendungspaket erstellen**. Wenn Sie das Paket erstellen möchten, wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.

3.  Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt, oder wenn das Paket unnötige Daten enthält. Wir empfehlen dringend, dass Sie alle potenziellen Probleme beheben, bevor Sie fortfahren. Nachdem Sie die Konflikte behoben haben, klicken Sie auf **Aktualisieren**, um die angezeigten Informationen zu aktualisieren. Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.

    **Wichtig**  
    Wenn Sie die Virenscansoftware deaktivieren möchten, müssen Sie den Computer scannen, auf dem die APP-VSequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder bösartigen Dateien hinzugefügt werden können.



4.  Wählen Sie auf der Seite **Art der Anwendung** **Middleware**aus, und klicken Sie dann auf **weiter**.

    Weitere Informationen zu den Arten von Anwendungen, die Sie abbilden können, finden Sie unter so wird es [gemacht: Ermitteln des zu sequenzenden Anwendungstyps (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für die Anwendung an. Wenn die Anwendung keine zugeordnete Installationsdatei hat und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.

6.  Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll. Mit dem Namen können Sie den Zweck und die Version der Anwendung ermitteln, die dem Paket hinzugefügt werden soll. Der Paketname wird auch in der App-V-Verwaltungskonsole angezeigt. Der **Installationsspeicherort** zeigt den Application Virtualization Path an, in dem die Anwendung installiert wird. Um diesen Speicherort zu bearbeiten, wählen Sie **Bearbeiten (erweitert)** aus.

    **Wichtig**  
    Das Bearbeiten des Application Virtualization path ist eine erweiterte Konfigurationsaufgabe. Sie sollten die Auswirkungen einer Änderung des Pfads vollständig verstehen. Für die meisten Anwendungen empfehlen wir den Standardpfad.



~~~
Click **Next**.
~~~

7. Installieren Sie die Anwendung auf der **Installations** Seite, wenn der Installationsprogramm für Sequencer und Middleware bereit ist, so, dass der Sequencer den Installationsvorgang überwachen kann. Führen Sie die Installation mithilfe des Installationsvorgangs der Anwendung durch. Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen**, um die zusätzlichen Installationsdateien zu suchen und auszuführen. Wenn Sie die Installation abgeschlossen haben, aktivieren Sie das Kontrollkästchen **Ich habe die Installation abgeschlossen** , und klicken Sie dann auf **weiter**.

8. Warten Sie auf der **Installations** Seite, während der Sequencer das virtuelle Anwendungspaket konfiguriert.

9. Auf der Seite **Installationsbericht** können Sie Informationen zu dem soeben sequenzierten virtuellen Anwendungspaket überprüfen. Eine detailliertere Erläuterung der Informationen, die in **zusätzlichen Informationen**angezeigt werden, finden Sie, indem Sie auf das Ereignis doppelklicken. Nachdem Sie die Informationen überprüft haben, klicken Sie auf **weiter**.

10. Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann. Wenn Sie alle unterstützten Betriebssysteme in Ihrer Umgebung zum Ausführen dieses Pakets aktivieren möchten, aktivieren Sie das Kontrollkästchen **Dieses Paket kann auf einem beliebigen Betriebssystem ausgeführt** werden. Wenn Sie dieses Paket so konfigurieren möchten, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, aktivieren Sie das Kontrollkästchen **Dieses Paket darf nur auf dem folgenden Betriebssystem ausgeführt** werden, und wählen Sie die Betriebssysteme aus, mit denen dieses Paket ausgeführt werden kann. Klicken Sie auf **Weiter**.

11. Wenn Sie das Paket auf der Seite **Paket erstellen** ändern möchten, ohne es zu speichern, aktivieren Sie das Kontrollkästchen **Paket ohne Speichern mithilfe des Paket-Editors weiter ändern** . Wenn Sie diese Option auswählen, wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können. Klicken Sie auf **Weiter**.

   Wenn Sie das Paket sofort speichern möchten, aktivieren Sie das Kontrollkästchen Standard, das **Paket jetzt speichern** . Fügen Sie im Feld **Kommentare** , das dem Paket zugeordnet ist, optionale Kommentare hinzu. Kommentare sind hilfreich, um Version und andere Informationen zum Paket zu identifizieren. Der Standard **Speicherort** wird ebenfalls angezeigt. Wenn Sie den Standardspeicherort ändern möchten, klicken Sie auf **Durchsuchen**, und geben Sie dann den neuen Speicherort an. Die Größe des unkomprimierten Pakets wird angezeigt. Wenn die Paketgröße 4 GB (unkomprimiert) überschreitet und Sie das Paket auf Zielcomputer streamen möchten, müssen Sie **Paket komprimieren**auswählen. Klicken Sie auf **Erstellen**.

12. Klicken Sie auf der Seite **Fertigstellung** nach dem Überprüfen der Informationen, die im Bereich **Bericht des virtuellen Anwendungspakets** angezeigt werden, auf **Schließen**. Die Informationen, die im Bereich " **Bericht des virtuellen Anwendungspakets** " angezeigt werden, sind auch in dem in Schritt 11 dieses Verfahrens angegebenen Verzeichnis in einer Datei mit dem Namen **Report.xml**verfügbar.

   Das Paket steht jetzt im Sequencer zur Verfügung. Um die Paketeigenschaften zu bearbeiten, klicken Sie auf **Bearbeiten \ [Package Name \]**. Weitere Informationen zum Ändern eines Pakets finden Sie unter [so wird es gemacht: Ändern eines vorhandenen virtuellen Anwendungspakets (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)

   **Wichtig**  
   Nachdem Sie ein virtuelles Anwendungspaket erfolgreich erstellt haben, können Sie das virtuelle Anwendungspaket nicht auf dem Computer ausführen, auf dem der Sequencer ausgeführt wird.



## Verwandte Themen


[Aufgaben für Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Ermitteln, welche Art von Anwendung zu sequenzieren ist (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









