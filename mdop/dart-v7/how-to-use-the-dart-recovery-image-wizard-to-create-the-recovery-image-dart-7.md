---
title: So verwenden Sie den Assistent für DaRT-Wiederherstellungsabbilder zum Erstellen des Wiederherstellungsabbilds
description: So verwenden Sie den Assistent für DaRT-Wiederherstellungsabbilder zum Erstellen des Wiederherstellungsabbilds
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809646"
---
# So verwenden Sie den Assistent für DaRT-Wiederherstellungsabbilder zum Erstellen des Wiederherstellungsabbilds


Microsoft Diagnostics and Recovery Toolset (Dart) 7 umfasst den **Dart-Wiederherstellungs-Bild-Assistenten** , der in Windows zum Erstellen einer startbaren internationalen Organisation für Standardisierungs-Images (ISO) verwendet wird. Bei einem ISO-Bild handelt es sich um eine Datei, die den unformatierten Inhalt einer CD darstellt.

Der **Dart-Wiederherstellungsbild-Assistent** benötigt die folgenden Informationen:

-   **Startabbild**° ° Sie müssen den Pfad einer Windows 7-DVD oder Windows 7-Quelldateien angeben, die zum Erstellen des DART-Wiederherstellungs Bilds erforderlich sind.

-   **Werkzeug Auswahl**° ° Sie können die Tools auswählen, die in das DART-Wiederherstellungsbild aufgenommen werden sollen.

-   **Remoteverbindungen**° ° Sie können auswählen, ob das DART-Wiederherstellungsabbild die Möglichkeit zum Einrichten einer Remote Verbindung zwischen dem Helpdesk und dem Endbenutzercomputer aufweisen soll.

-   **Debugging-Tools für Windows**° ° Sie werden aufgefordert, den Speicherort der Debugging-Tools für Windows anzugeben.

-   **Definitionen für Standalone-System Sweeper**° ° Sie können entscheiden, ob Sie die neuesten Definitionen zu dem Zeitpunkt herunterladen möchten, zu dem Sie das Wiederherstellungsabbild erstellt haben, oder die Definitionen später herunterladen.

-   **Treiber**° ° Sie werden gefragt, ob Sie dem ISO-Abbild Treiber hinzufügen möchten.

-   **Weitere Dateien**° ° Sie können dem ISO-Abbilddateien hinzufügen, die möglicherweise beim Diagnostizieren von Problemen helfen.

-   **ISO-Bildposition**° ° Sie werden aufgefordert anzugeben, wo sich das ISO-Abbild befinden soll.

-   **CD/DVD-Laufwerk**° ° Sie werden aufgefordert anzugeben, ob das CD-oder DVD-Laufwerk zum Brennen der CD oder DVD verwendet werden soll.

**Hinweis**  Die ISO-Bildgröße kann je nach den im **Dart-Wiederherstellungsbild-Assistenten**ausgewählten Tools variieren.

 

## So erstellen Sie das Wiederherstellungsabbild mithilfe des DART-Wiederherstellungsbild-Assistenten


Befolgen Sie diese Anweisungen, um das DART-Wiederherstellungsabbild mithilfe des **Dart-Wiederherstellungsbild-Assistenten** zu erstellen.

### So wählen Sie die Tools aus, die Sie in das DART-Wiederherstellungsabbild einbeziehen möchten

Der **Dart-Wiederherstellungsbild-Assistent** zeigt ein Dialogfeld für die **Tool Auswahl** an. Sie können Tools aus der Liste der Tools auswählen oder entfernen, die im Dart-Wiederherstellungsbild enthalten sein sollen, indem Sie ein Tool markieren und dann auf die Schaltflächen **aktivieren** oder **Deaktivieren** klicken.

Nachdem Sie alle Tools ausgewählt haben, die Sie in das Wiederherstellungsabbild aufnehmen möchten, klicken Sie auf **weiter**.

### So fügen Sie die Option zum Zulassen der Remotekonnektivität hinzu

Sie können das Kontrollkästchen **Remoteverbindungen zulassen** aktivieren, um die Option im Fenster **Diagnose-und Wiederherstellungs-Toolset** bereitzustellen, um eine Remoteverbindung zwischen dem Helpdesk-Agenten und einem Endbenutzercomputer herzustellen. Nachdem ein Helpdesk-Agent eine Remoteverbindung hergestellt hat, können Sie die Dart-Tools auf dem Endbenutzercomputer von einem Remotestandort aus ausführen.

Sie können das Kontrollkästchen **Portnummer angeben** aktivieren, um eine bestimmte Portnummer einzugeben, die beim Einrichten einer Remoteverbindung verwendet wird. Sie können eine Portnummer zwischen 1 und 65535 angeben. Wir empfehlen, dass die Portnummer 1024 oder höher ist, um die Möglichkeit eines Konflikts zu minimieren.

Sie können auch eine angepasste Nachricht erstellen, die ein Endbenutzer erhält, wenn er eine Remoteverbindung herstellt. Die Nachricht kann maximal 2048 Zeichen umfassen.

Weitere Informationen zum Remote Ausführen der Dart-Tools finden Sie unter [Wiederherstellen von Remotecomputern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).

### So fügen Sie dem Dart-Wiederherstellungsabbild die Debug-Tools für Windows hinzu

Im Dialogfeld **Absturzanalyse** des Bild- **Assistenten für Dart-Wiederherstellung**werden Sie aufgefordert, den Speicherort der Debugging-Tools für Windows anzugeben. Wenn Sie nicht über eine Kopie der Tools verfügen, können Sie Sie von Microsoft herunterladen. Der folgende Link zur Download-Seite wird im Assistenten bereitgestellt: [herunterladen und Installieren von Debugging-Tools für Windows](https://go.microsoft.com/fwlink/?LinkId=99934).

Sie können entweder den Speicherort der Debug-Tools auf dem Computer angeben, auf dem Sie den **Dart-Wiederherstellungsbild-Assistenten**ausführen, oder Sie können die Tools verwenden, die sich auf dem Zielcomputer befinden. Wenn Sie sich entscheiden, eine Kopie auf einem anderen Computer zu verwenden, müssen Sie sicherstellen, dass die Tools auf jedem Computer installiert sind, auf dem Sie einen Absturz diagnostizieren.

**Hinweis**  Wenn Sie **Crash Analyzer** in das ISO-Abbild einbeziehen, empfehlen wir, dass Sie auch die Debugging-Tools für Windows einbeziehen.

 

Führen Sie die folgenden Schritte aus, um die Debugging-Tools für Windows hinzuzufügen:

1.  Optional Klicken Sie auf den Link, um die Debugging-Tools für Windows herunterzuladen.

2.  Wählen Sie eine der folgenden Optionen aus:

    -   **Verwenden Sie die Debugging-Tools für Windows an der folgenden Position**. Wenn Sie diese Option auswählen, können Sie zum Speicherort der Tools navigieren.

    -   **Suchen Sie die Debugging-Tools für Windows auf dem System, das Sie reparieren möchten**. Wenn Sie diese Option auswählen, funktioniert der **Absturzanalyse** Programm nicht, wenn die Debugging-Tools für Windows auf dem Problem Computer nicht gefunden werden.

3.  Klicken Sie abschließend auf **weiter**.

### So fügen Sie dem Dart-Wiederherstellungsabbild Definitionen für eigenständige System Sweeper hinzu

Definitionen sind ein Repository bekannter Schadsoftware und anderer potenziell unerwünschter Software. Da Malware kontinuierlich entwickelt wird, setzt **Standalone-System Sweeper** auf aktuelle Definitionen, um festzustellen, ob Software, die versucht, die Einstellungen auf einem Computer zu installieren, auszuführen oder zu ändern, potenziell unerwünschte oder bösartige Software ist.

Wenn Sie die neuesten Definitionen in das DART-Wiederherstellungsabbild einbeziehen möchten (empfohlen), klicken Sie auf **Ja, um die neuesten Definitionen herunterzuladen.** Das Definitionsupdate wird automatisch gestartet. Sie müssen mit dem Internet verbunden sein, um diesen Vorgang abzuschließen.

Wenn Sie das Definitionsupdate überspringen möchten, klicken Sie auf **Nein, Definitionen später manuell herunterladen**. Definitionen werden nicht in das DART-Wiederherstellungsbild aufgenommen.

Wenn Sie sich entschließen, die neuesten Definitionen nicht in das Wiederherstellungsabbild aufzunehmen, oder wenn die im Wiederherstellungsabbild enthaltenen Definitionen nicht mehr aktuell sind, wenn Sie bereit sind, **eigenständiges System Sweeper**zu verwenden, besorgen Sie sich die neuesten Definitionen, bevor Sie mit dem Scannen beginnen, indem Sie die Anweisungen befolgen, die im **eigenständigen System Sweeper**bereitgestellt werden

**Wichtig**  Sie können nicht überprüfen, ob keine Definitionen vorhanden sind.

 

Klicken Sie abschließend auf **weiter**.

### So fügen Sie dem Dart-Wiederherstellungsabbild Treiber hinzu

**Vorsicht**  Wenn Sie dem Dart-Wiederherstellungsabbild einen Treiber hinzufügen, werden standardmäßig alle weiteren Dateien und Unterordner, die sich in diesem Ordner befinden, dem Wiederherstellungsabbild hinzugefügt. Weitere Informationen finden Sie unter [Problembehandlung bei Dart 7,0](troubleshooting-dart-70-new-ia.md).

 

Sie sollten zusätzliche Treiber für das Wiederherstellungsabbild für DaRT7 hinzufügen, die Sie möglicherweise benötigen, wenn Sie einen Computer reparieren. Diese können in der Regelspeicher-oder Netzwerk Controller enthalten, die nicht auf der Windows-DVD enthalten sind.

**Wichtig**  Beachten Sie bei der Auswahl der zu berücksichtigenden Treiber, dass drahtlose Verbindungen (wie Bluetooth oder 802.11 a/b/g/n) in DART nicht unterstützt werden.

 

**So fügen Sie dem Wiederherstellungsabbild einen Speicher-oder Netzwerk Controller Treiber hinzu**

1.  Klicken Sie im Dialogfeld **zusätzliche Treiber** des **Bild-Assistenten für Dart-Wiederherstellung**auf **Gerät hinzufügen**.

2.  Navigieren Sie zu der Datei, die für den Treiber hinzugefügt werden soll, und klicken Sie dann auf **Öffnen**.

    **Hinweis**  Die **Treiber** Datei wird vom Hersteller des Speichers oder des Netzwerkcontrollers bereitgestellt.

     

3.  Wiederholen Sie die Schritte 1 und 2 für jeden Treiber, den Sie einbeziehen möchten.

4.  Klicken Sie abschließend auf **weiter**.

### So fügen Sie dem Dart-Wiederherstellungsabbild Dateien hinzu

Führen Sie die folgenden Schritte aus, um dem Wiederherstellungsabbild Dateien hinzuzufügen, damit Sie diese zum Diagnostizieren von Computerproblemen verwenden können.

1.  Klicken Sie im Dialogfeld **Weitere Dateien** des **Assistenten für Dart-Wiederherstellungs Bilder**auf **Dateien anzeigen**. Dadurch wird ein Explorer-Fenster geöffnet, in dem der Ordner angezeigt wird, in dem die freigegebenen Dateien gespeichert sind.

2.  Erstellen Sie einen Unterordner in dem Ordner, der im Dialogfeld aufgeführt ist.

3.  Kopieren Sie die gewünschten Dateien in den neuen Unterordner.

4.  Klicken Sie abschließend auf **Weiter.**

### So wählen Sie einen Speicherort für die ISO-Datei aus, die das DART-Wiederherstellungsabbild enthält

Führen Sie die folgenden Schritte aus, um den Speicherort für die Erstellung des ISO-Images anzugeben:

1.  Klicken Sie im Dialogfeld **Startabbild erstellen** des **Dart-Wiederherstellungsbild-Assistenten**auf **Durchsuchen**.

2.  Navigieren Sie im Fenster **Speichern** unter zu dem bevorzugten Speicherort, und klicken Sie dann auf **Speichern**.

3.  Klicken Sie abschließend auf **weiter**.

Die Größe des ISO-Bilds hängt von den ausgewählten Tools und den Dateien ab, die Sie im Assistenten hinzufügen.

Der Assistent erfordert eine ISO **-** Dateinamenerweiterung, da für die meisten Programme, die eine CD oder DVD brennen, diese Erweiterung erforderlich ist. Wenn Sie keinen anderen Speicherort angeben, wird das ISO-Abbild auf dem Desktop mit dem Namen **DaRT70. ISO**erstellt.

### So brennen Sie das Wiederherstellungsabbild auf eine CD oder DVD

Wenn der **Dart-Wiederherstellungs-Bild-Assistent** ein kompatibles CD-RW-Laufwerk auf dem Computer erkennt, bietet es an, das ISO-Image auf einen Datenträger zu brennen. Wenn Sie eine CD oder DVD brennen möchten und der Assistent Ihr Laufwerk nicht erkennt, müssen Sie ein anderes Programm verwenden, beispielsweise das Programm, das im Lieferumfang Ihres Laufwerks enthalten war. Sie können einen Duplizierer, einen Duplizierungs Dienst oder eine CD-oder DVD-Brennsoftware verwenden, um zusätzliche Kopien zu erstellen.

1.  Wählen Sie im Dialogfeld " **auf eine beschreibbare CD/DVD brennen** " des **Assistenten für Dart-Wiederherstellungs Bilder**die Option **Image auf das folgende beschreibbare CD/DVD-Laufwerk brennen**aus.

2.  Wählen Sie das CD-oder DVD-Laufwerk aus.

    **Hinweis**  Wenn ein Laufwerk nicht erkannt wird und Sie ein neues Laufwerk installieren, können Sie auf **Laufwerkliste aktualisieren** klicken, um den Assistenten zu zwingen, die Liste der verfügbaren Laufwerke zu aktualisieren.

     

3.  Klicken Sie auf **Weiter**.

## Verwandte Themen


[Erstellen des DaRT 7.0-Wiederherstellungsabbilds](creating-the-dart-70-recovery-image-dart-7.md)

 

 





