---
title: So sequenzieren Sie eine neue Anwendung (App-V 4.6)
description: So sequenzieren Sie eine neue Anwendung (App-V 4.6)
author: dansimp
ms.assetid: f2c398c6-9200-4be3-b502-e00386fcd150
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a36021adf45f0f4c80ab08bcabbf9f18bf6e66b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806811"
---
# So sequenzieren Sie eine neue Anwendung (App-V 4.6)


Verwenden Sie das folgende Verfahren zum Erstellen einer neuen virtuellen Anwendung mithilfe von Application Virtualization (App-V) Sequencer. Sie können auch den App-V-Sequenzer verwenden, um zu konfigurieren, welche Dateien und Konfigurationen für alle Benutzer gelten und welche Dateien und Konfigurationen Benutzer anpassen können. Nachdem Sie die Anwendung erfolgreich sequenziert haben, steht Sie im App-V-Sequenzer zur Verfügung.

**Wichtig**  
Wenn während der Sequenzierung auf dem Computer, auf dem der Sequencer ausgeführt wird, Windows Vista oder Windows 7 ausgeführt wird und ein Neustart außerhalb der virtuellen Umgebung initiiert wird, beispielsweisedurch klicken auf **Start**  /  **Herunterfahren**, müssen Sie auf **Abbrechen** klicken, wenn Sie aufgefordert werden, das Programm zu schließen, das verhindert, dass Windows beendet wird. Wenn Sie auf " **Herunterfahren erzwingen**" klicken, schlägt die Paketerstellung fehl, und der Computer wird neu gestartet. Wenn Sie auf **Abbrechen**klicken, zeichnet der Sequencer den Neustart erfolgreich auf, während die Anwendung sequenziert wird.



**So Sequenzieren Sie eine neue Anwendung**

1.  Zum Erstellen des App-V-Laufwerks konfigurieren Sie Laufwerk Q als Speicherort, der zum Speichern von Dateien verwendet werden kann, während Sie eine Anwendung sequenzieren. Sie müssen dann für jede Anwendung, die Sie auf Laufwerk Q abgleichen möchten, einzelne Verzeichnisse erstellen. Sie können die Zielordner der virtuellen Anwendung erstellen, bevor Sie eine Anwendung sequenzieren, oder Sie können Sie in Schritt 5 dieses Verfahrens erstellen.

    **Hinweis:**  
    Auf dem von Ihnen festgelegten App-V-Laufwerk muss auf den Zielcomputern zugegriffen werden können. Wenn auf Laufwerk Q nicht zugegriffen werden kann, können Sie einen anderen Laufwerkbuchstaben auswählen.



2.  Wenn Sie die APP-v Sequencer-Konsole starten möchten, wählen Sie auf dem Computer, auf dem der APP- **Start**v-Sequencer ausgeführt wird, die Option  /  **Programme**  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**starten aus. Klicken Sie zum Starten des Sequenz-Assistenten auf **Paket erstellen**.

3.  Geben Sie auf der Seite **Paketinformationen** den **Paketnamen** an, der der virtuellen Anwendung zugewiesen werden soll. Der Paketname ist erforderlich, um die zugehörige Windows Installer-Datei zu generieren. Sie sollten auch einen optionalen Kommentar hinzufügen, der dem Paket zugewiesen wird und detaillierte Informationen zur virtuellen Anwendung bereitstellt. Wenn Sie die Seite **Erweiterte Optionen** anzeigen möchten, wählen Sie **erweiterte Überwachungsoptionen anzeigen**aus, und klicken Sie dann auf **weiter**. fahren Sie andernfalls mit Schritt 5 fort.

4.  Wählen Sie auf der Seite **Erweiterte Optionen** aus, damit Microsoft Update die Anwendung während der Reihenfolge aktualisieren kann, und aktivieren Sie die **Ausführung von Microsoft Update während der Überwachung**. Wenn Sie diese Option auswählen, können Microsoft-Updates während der Überwachungsphase installiert werden, und Sie müssen die zugehörigen Updates akzeptieren, damit Sie installiert werden. Wenn Sie die unterstützten dll-Dateien (Dynamic Link Library) neu zuordnen möchten, damit Sie einen zusammenhängenden Speicherbereich verwenden, wählen Sie **DLLs**erneut erstellen aus. Wenn Sie diese Option auswählen, können Sie Arbeitsspeicher sparen und die Leistung verbessern. Viele Anwendungen unterstützen diese Option nicht, aber Sie ist in Umgebungen mit einem bestimmten RAM-Speicher wie in Terminal Server Szenarien hilfreich. Klicken Sie auf **Weiter**.

5.  Wenn Sie bereit sind, die Anwendung zu installieren, klicken Sie auf der Seite **Monitor Installation** auf **Überwachung starten**, und geben Sie im Dialogfeld **Ordner suchen** das Verzeichnis auf Laufwerk Q an, in dem die Anwendung installiert werden soll. Wenn Sie Laufwerk Q nicht konfiguriert und einen anderen Laufwerkbuchstaben für das Application Virtualization Drive verwendet haben, wählen Sie den Laufwerkbuchstaben aus, den Sie in Schritt 1 dieses Verfahrens angegeben haben. Klicken Sie auf **neuen Ordner erstellen**, um die Anwendung in einem Ordner zu installieren, der nicht auf dem Application Virtualization-Laufwerk erstellt wurde. Nachdem Sie den Ordner angegeben haben, warten Sie, während der Sequencer den Computer für die Sequenzierung konfiguriert.

    **Wichtig**  
    Sie müssen jede von Ihnen sequenzierte Anwendung in einem separaten Verzeichnis auf dem virtuellen Anwendungs Laufwerk installieren, und der zugehörige Ordnername darf nicht mehr als acht Zeichen umfassen.



~~~
After the computer has been configured for sequencing, install the application so that the App-V Sequencer can monitor the installation; when you are finished, click **Stop Monitoring**, and then click **Next**.
~~~

6. Konfigurieren Sie bei Bedarf auf der Seite **Anwendungen konfigurieren** die Verknüpfungen und Dateitypzuordnungen, die der virtuellen Anwendung zugeordnet werden. Wenn Sie eine neue Dateitypzuordnung oder Verknüpfung hinzufügen möchten, klicken Sie auf **hinzu**fügen, und geben Sie im Dialogfeld **Anwendung hinzufügen** das neue Element an. Wenn Sie eine vorhandene Verknüpfung oder Dateitypzuordnung entfernen möchten, klicken Sie auf **Entfernen**. Wenn Sie ein vorhandenes Element bearbeiten möchten, wählen Sie das zu ändernde Element aus, und klicken Sie dann auf **Bearbeiten**. Geben Sie die Konfigurationen im Dialogfeld " **Anwendung bearbeiten** " an. Klicken Sie auf **Speichern**und dann auf **weiter**.

7. Wählen Sie auf der Seite **Anwendungen starten** aus, um die Anwendung zu starten, um sicherzustellen, dass das Paket ordnungsgemäß installiert wurde und für das Streaming optimiert ist, das Paket, und klicken Sie dann auf **Start**. Dieser Schritt ist nützlich, um zu konfigurieren, wie die Anwendung zunächst auf Zielcomputern ausgeführt wird und welche zugehörigen Lizenzvereinbarungen akzeptiert werden, bevor das Paket für App-V-Clients verfügbar wird. Wenn diesem Paket mehrere Anwendungen zugeordnet sind, können Sie alle **starten** auswählen, um alle Anwendungen zu öffnen. Klicken Sie auf **weiter**, um das Paket zu sequenzieren.

8. Nachdem Sie das Paket erfolgreich erstellt haben, wählen Sie in der App-V Sequencer-Konsole **Datei**  /  **Speichern** aus, und geben Sie den Namen und den Speicherort des virtuellen Laufwerks an, in dem das Paket gespeichert werden soll.

   Optional können Sie eine zugeordnete Windows Installer-Datei (**MSI**) erstellen, um das virtuelle Anwendungspaket auf Zielcomputern zu installieren. Um eine Windows Installer-Datei zu erstellen, öffnen Sie das Paket im Sequencer, und wählen Sie **Tools**  /  **Create MSI**aus. Die Windows Installer-Datei wird in dem Verzeichnis erstellt und gespeichert, in dem das virtuelle Anwendungspaket gespeichert ist.

   **Wichtig**  
   Nachdem Sie ein virtuelles Anwendungspaket erfolgreich erstellt haben, können Sie das virtuelle Anwendungspaket nicht auf dem Computer ausführen, auf dem der Sequencer ausgeführt wird.



## Verwandte Themen


[So aktualisieren Sie ein virtuelles Anwendungspaket (App-V 4.6)](how-to-upgrade-a-virtual-application-package--app-v-46-.md)









