---
title: So sequenzieren Sie eine neue Anwendung
description: So sequenzieren Sie eine neue Anwendung
author: dansimp
ms.assetid: e01e98cd-2378-478f-9739-f72c465bf79a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aab769256116e2635edbc4bcf55d212e3a2152f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806799"
---
# So sequenzieren Sie eine neue Anwendung


Der Application Virtualization (App-V)-Sequenzer erstellt Anwendungen, die in einer virtuellen Umgebung ausgeführt werden können. Der App-V-Sequencer überwacht den Installations-und Einrichtungsprozess für eine Anwendung und zeichnet die Informationen auf, die für die Ausführung der Anwendung in einer virtuellen Umgebung erforderlich sind. Sie können auch den App-V-Sequenzer verwenden, um zu konfigurieren, welche Dateien und Konfigurationen für alle Benutzer gelten und welche Dateien und Konfigurationen Benutzer anpassen können. Wenn Sie eine Anwendung sequenzieren, sollten Sie das Paket auf einem Laufwerk speichern, das sich lokal auf dem Computer befindet, auf dem Sie die Sequenzierung durchführen.

Eine sequenzierte Anwendung interagiert nicht mit dem Betriebssystem, da jede Anwendung in einer virtuellen Umgebung ausgeführt wird und von anderen Anwendungen isoliert ist, die möglicherweise auf dem Zielcomputer installiert oder ausgeführt werden. Durch diese Isolierung werden Anwendungskonflikte drastisch reduziert und die erforderliche Anzahl von Anwendungstests vor der Bereitstellung verringert.

Nachdem Sie die Anwendung erfolgreich sequenziert haben, steht Sie in der App-V Sequencer-Konsole zur Verfügung. Das Ausführen des App-V-Sequencers im abgesicherten Modus wird nicht unterstützt.

**So Sequenzieren Sie eine neue Anwendung**

1.  Sie müssen das Application Virtualization-Laufwerk erstellen, um eine neue virtuelle Anwendung zu sequenzieren. Zum Erstellen des Application Virtualization-Laufwerks ordnen Sie das Q:\\-Laufwerk einem Speicherort zu, der zum Speichern von Dateien verwendet werden kann, während Sie eine Anwendung sequenzieren. Sie müssen dann einzelne Verzeichnisse für jede Anwendung erstellen, die Sie auf dem Q:\\-Laufwerk abgleichen möchten. Sie können die Zielordner der virtuellen Anwendung erstellen, bevor Sie eine Anwendung sequenzieren, oder Sie können Sie in Schritt 5 dieses Verfahrens erstellen.

2.  Wenn Sie die APP-v Sequencer-Konsole starten möchten, wählen Sie auf dem Computer, auf dem der APP- **Start**v-Sequencer ausgeführt wird, die Option  /  **Programme**  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**starten aus. Wenn Sie den **Sequenz-Assistenten**starten möchten, wählen Sie **Datei**  /  **neues Paket**aus.

3.  Geben Sie auf der Seite **Paketinformationen** den **Paketnamen** an, der der virtuellen Anwendung zugewiesen werden soll. Der Paketname ist erforderlich, um die zugehörige Windows Installer-Datei zu generieren. Sie sollten auch einen optionalen Kommentar hinzufügen, der dem Paket zugewiesen wird und detaillierte Informationen zur virtuellen Anwendung bereitstellt. Wenn Sie die Seite **Erweiterte Optionen** anzeigen möchten, wählen Sie **erweiterte Überwachungsoptionen anzeigen**aus. Klicken Sie auf **Weiter**.

    **Hinweis:**  
    Wenn Sie die Seite **Erweiterte Optionen** anzeigen möchten, müssen Sie **erweiterte Überwachungsoptionen anzeigen**auswählen. Wenn Sie die Seite **Erweiterte Optionen** nicht benötigen, fahren Sie mit Schritt 4 fort.



4.  Wählen Sie auf der Seite **Erweiterte Optionen** die gewünschte Größe aus, um die **Block Größe** für die virtuelle Anwendung festzulegen. Die Blockgröße bestimmt, wie die **SFT-** Datei für das Streaming des Pakets über das Netzwerk auf die Zielcomputer aufgeteilt wird. So lassen Sie Microsoft Update die Anwendung aktualisieren, während Sie sequenziert wird Wählen Sie **zulassen, dass Microsoft Update während der Überwachung ausgeführt wird**. Wenn Sie diese Option auswählen, können Microsoft-Updates während der Überwachungsphase installiert werden, und Sie müssen die zugehörigen Updates akzeptieren, damit Sie installiert werden. Wenn Sie die unterstützten dll-Dateien (Dynamic Link Library) neu zuordnen möchten, damit Sie einen zusammenhängenden Speicherbereich verwenden, wählen Sie **DLLs**erneut erstellen aus. Wenn Sie diese Option auswählen, können Sie Arbeitsspeicher sparen und die Leistung verbessern. Viele Anwendungen unterstützen diese Option nicht, aber Sie ist in Umgebungen mit einem bestimmten RAM-Speicher wie in Terminal Server Szenarien hilfreich. Klicken Sie auf **Weiter**.

5.  Klicken Sie auf der Seite **Monitorinstallation** auf **Überwachung starten**, um die Installation einer Anwendung zu überwachen. Nachdem Sie auf **Überwachung starten**klicken, geben Sie das Verzeichnis auf dem Q:\\-Laufwerk an, auf dem die Anwendung installiert werden soll. Wenn Sie die Anwendung in einem nicht erstellten Ordner installieren möchten, klicken Sie auf **neuen Ordner erstellen**. Sie müssen jede von Ihnen sequenzierte Anwendung in einem separaten Verzeichnis installieren.

    **Wichtig**  
    Der angegebene Ordnername darf nicht länger als 8 Zeichen sein.



~~~
Wait for the virtual environment to load, and then install the application so that the App-V Sequencer can monitor the process. When you have completed the installation, click **Stop Monitoring** and then click **Next**.
~~~

6. Klicken Sie auf der Seite zusätzliche Dateien, die dem virtuellen Datei **System (VFS) zugeordnet** werden sollen, um weitere Dateien anzugeben, die dem virtuellen Dateisystem (VFS) hinzugefügt werden sollen, auf **Hinzufügen**. Navigieren Sie zu der Datei, die Sie hinzufügen möchten, und klicken Sie auf **Öffnen**. Um vorhandene Dateien zu löschen, die hinzugefügt wurden, klicken Sie auf **Zurücksetzen** und dann auf **weiter**.

7. Konfigurieren Sie auf der Seite **Anwendungen konfigurieren** die Verknüpfungen und Dateitypen Zuordnungen, die der virtuellen Anwendung zugeordnet werden. Wählen Sie das Element aus, das Sie aktualisieren möchten, und klicken Sie dann auf **Speicherorte bearbeiten**. Geben Sie die Konfigurationen im Dialogfeld **Verknüpfungs Orte** an. Klicken Sie auf **OK** und dann auf **weiter**.

8. Wählen Sie auf der Seite **Anwendungen starten** die Anwendung aus, um sicherzustellen, dass das Paket für Streaming optimiert ist, und klicken Sie auf **Start**. Dieser Schritt ist nützlich, um zu konfigurieren, wie die Anwendung zunächst auf Zielcomputern ausgeführt wird und welche zugehörigen Lizenzvereinbarungen akzeptiert werden, bevor das Paket für Clients verfügbar gemacht wird. Wenn diesem Paket mehrere Anwendungen zugeordnet sind, können Sie alle **starten** auswählen, um alle Anwendungen zu öffnen. Klicken Sie auf **weiter**, um das Paket zu sequenzieren.

9. Klicken Sie auf der Seite **Sequenzpaket** auf **Fertig stellen**, um den Assistenten zu schließen.

10. Nachdem Sie das Paket erfolgreich erstellt haben, wählen Sie zum Speichern des Pakets in der App-V Sequencer-Konsole **Datei**  /  **Speichern** aus, und geben Sie den Namen und den Speicherort an, an dem das Paket gespeichert werden soll.

## Verwandte Themen


[Aufgaben für den Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)









