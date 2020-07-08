---
title: Erstellen des DaRT 8.0-Wiederherstellungsabbilds
description: Erstellen des DaRT 8.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: 39001b8e-86c0-45ef-8f34-2d6199f9922d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/21/2017
ms.openlocfilehash: 79ce5859e7d0eacf95124c2a7409ff6c21890d65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804313"
---
# Erstellen des DaRT 8.0-Wiederherstellungsabbilds


Nachdem Sie Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 installiert haben, erstellen Sie ein Dart 8,0-Wiederherstellungsabbild. Das Wiederherstellungsabbild startet Windows RE, aus dem Sie dann die Dart-Tools starten können. Sie können internationale Organisation für Standardisierungs Dateien (ISO) und Wim-Bilder (Windows Imaging Format) erstellen. Darüber hinaus können Sie mithilfe von PowerShell Skripts generieren, die die Einstellungen verwenden, die Sie im Dart-Wiederherstellungsbild-Assistenten ausgewählt haben. Sie können das Skript später verwenden, um Wiederherstellungs Bilder mithilfe der gleichen Einstellungen wiederherzustellen. Das Wiederherstellungsabbild bietet eine Reihe von Wiederherstellungstools. Eine Beschreibung der Tools finden Sie unter [Übersicht über die Tools in Dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).

Nachdem Sie den Computer in DART gestartet haben, können Sie die verschiedenen Dart-Tools ausführen, um zu versuchen, den Computer zu diagnostizieren und zu reparieren. In diesem Abschnitt werden Sie durch den Vorgang zum Erstellen des DART-Wiederherstellungs Bilds geführt, in dem Sie die Tools und Features auswählen können, die Sie als Teil des Bilds einfügen möchten.

Sie können das DART-Wiederherstellungsabbild mithilfe einer der beiden folgenden Methoden erstellen:

-   Verwenden Sie den Dart-Wiederherstellungsbild-Assistenten, der in einer Windows-Umgebung ausgeführt wird.

-   Ändern Sie ein Beispiel-PowerShell-Skript mit den gewünschten Werten. Weitere Informationen finden Sie unter [so wird es gemacht: Verwenden eines PowerShell-Skripts zum Erstellen des Wiederherstellungsabbilds](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-8.md).

Sie können die ISO auf eine beschreibbare CD oder DVD schreiben, Sie auf einem USB-Stick speichern oder in einem Format speichern, das Sie zum Booten von DART von einer Remotepartition oder einer Wiederherstellungspartition verwenden können.

Nachdem Sie das ISO-Abbild erstellt haben, können Sie es auf eine leere CD oder DVD brennen (wenn Ihr Computer über ein CD-oder DVD-Laufwerk verfügt). Wenn Ihr Computer nicht über ein Laufwerk für diesen Zweck verfügt, können Sie die meisten generischen Programme verwenden, mit denen CDs oder DVDs gebrannt werden.

## Auswählen der Bildarchitektur und angeben des Pfads


Auf der Windows 8 Media-Seite Wählen Sie aus, ob Sie ein 32-Bit-oder 64-Bit-Dart-Wiederherstellungsbild erstellen möchten. Verwenden Sie das 32-Bit-Fenster zum Erstellen von 32-Bit-Dart-Wiederherstellungs Bildern und 64-Bit-Windows zum Erstellen von 64-Bit-Dart-Wiederherstellungs Bildern. Sie können einen einzelnen Computer verwenden, um Wiederherstellungs Bilder für beide Architekturtypen zu erstellen, Sie können jedoch kein einzelnes Bild erstellen, das sowohl auf 32-Bit-als auch auf 64-Bit-Architekturen funktioniert. Außerdem geben Sie den Pfad der Windows 8-Installationsmedien an. Wählen Sie die Architektur aus, die dem von Ihnen erstellten Wiederherstellungsbild entspricht.

**So wählen Sie die Bildarchitektur aus und geben den Pfad an**

1.  Wählen Sie auf der Seite **Windows 8 Media** eine der folgenden Optionen aus:

    -   Wenn Sie ein Wiederherstellungsabbild für 64-Bit-Computer erstellen, wählen Sie **x64-(64-Bit-) Dart-Bild erstellen**aus.

    -   Wenn Sie ein Wiederherstellungsabbild für 32-Bit-Computer erstellen, wählen Sie **x86 (32-Bit) Dart-Bild erstellen**aus.

2.  Geben Sie im Feld **Geben Sie den Stammpfad des Windows 8 &lt; 64-Bit-oder 32-Bit- &gt; Installationsmediums** an den Pfad der Windows 8-Installationsdateien ein. Verwenden Sie einen Pfad, der der Architektur des Wiederherstellungs Bilds entspricht, das Sie erstellen.

3.  Klicken Sie auf **Weiter**.

## Auswählen der Tools, die in das Wiederherstellungsabbild aufgenommen werden sollen


Auf der Seite Extras können Sie zahlreiche Tools auswählen, die in das Wiederherstellungsabbild aufgenommen werden sollen. Diese Tools stehen Endbenutzern zur Verfügung, wenn Sie in das DART-Bild Booten. Wenn Sie jedoch beim Erstellen des DART-Bilds die Remotekonnektivität aktivieren, stehen alle Tools zur Verfügung, wenn ein Mitarbeiter des Helpdesks eine Verbindung mit dem Computer des Endbenutzers herstellt, unabhängig davon, welche Tools Sie in das Bild aufgenommen haben.

Wenn Sie den Endbenutzer Zugriff auf diese Tools einschränken, aber weiterhin den vollständigen Zugriff auf die Tools über die Remote Verbindungsanzeige behalten möchten, wählen Sie diese Tools auf der Seite Tools nicht aus. Endbenutzer können nur die Remote Verbindung verwenden und können alle Tools, die Sie aus dem Wiederherstellungsabbild ausschließen, sehen, aber nicht darauf zugreifen.

**So wählen Sie die Tools aus, die Sie in das Wiederherstellungsabbild einbeziehen möchten**

1.  Aktivieren Sie auf der Seite **Extras** das Kontrollkästchen neben jedem Tool, das Sie in das Bild einbeziehen möchten.

2.  Klicken Sie auf **Weiter**.

## Auswählen, ob die Remotekonnektivität von einem Helpdesk zugelassen werden soll


Auf der Seite Remote Verbindung können Sie festlegen, dass ein Helpdesk-Mitarbeiter eine Remoteverbindung herstellen und die Dart-Tools auf dem Computer eines Endbenutzers ausführen soll. Die Option Remotekonnektivität wird dann im Fenster Diagnose-und Wiederherstellungs-Toolset als verfügbare Option angezeigt. Nachdem die Helpdesk-Mitarbeiter eine Remoteverbindung hergestellt haben, können Sie die Dart-Tools auf dem Endbenutzercomputer von einem Remotestandort aus ausführen.

**So wählen Sie aus, ob die Remotekonnektivität von Helpdesk-Mitarbeitern zugelassen werden soll**

1.  Aktivieren Sie auf der Seite **Remoteverbindung** das Kontrollkästchen **Remoteverbindungen zulassen** , um Remoteverbindungen zuzulassen, oder deaktivieren Sie das Kontrollkästchen, um Remoteverbindungen zu verhindern.

2.  Wenn Sie das Kontrollkästchen **Remoteverbindungen zulassen** deaktiviert haben, klicken Sie auf **weiter**. Fahren Sie andernfalls mit dem nächsten Schritt fort, um die Konfiguration der Remotekonnektivität fortzusetzen.

3.  Wählen Sie eine der folgenden Optionen:

    -   Lassen Sie Windows eine offene Portnummer auswählen.

    -   Geben Sie die Portnummer an. Wenn Sie diese Option auswählen, geben Sie eine Portnummer zwischen 1 und 65535 in das Feld unterhalb der Option ein. Diese Portnummer wird beim Einrichten einer Remoteverbindung verwendet. Wir empfehlen, dass die Portnummer 1024 oder höher ist, um die Möglichkeit eines Konflikts zu minimieren.

4.  (Optional) erstellen Sie im Dialogfeld "Willkommensnachricht für **Remoteverbindung** " eine benutzerdefinierte Nachricht, die Endbenutzer erhalten, wenn Sie eine Remoteverbindung herstellen. Die Nachricht kann maximal 2048 Zeichen umfassen.

5.  Klicken Sie auf **Weiter**.

    Weitere Informationen dazu, wie Sie die Dart-Tools Remote ausführen können, finden Sie unter [Wiederherstellen von Remotecomputern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md).

## Hinzufügen von Treibern zum Wiederherstellungsabbild


Auf der Registerkarte "Treiber" auf der Seite "Erweiterte Optionen" können Sie zusätzliche Gerätetreiber hinzufügen, die Sie möglicherweise benötigen, wenn Sie einen Computer reparieren. Diese können in der Regelspeicher-oder Netzwerk Controller enthalten, die von Windows 8 nicht bereitgestellt werden. Treiber werden installiert, wenn das Bild erstellt wird.

**Wichtig**  Beachten Sie bei der Auswahl der zu berücksichtigenden Treiber, dass drahtlose Verbindungen (wie Bluetooth oder 802.11 a/b/g/n) in DART nicht unterstützt werden.

 

**So fügen Sie dem Wiederherstellungsabbild Treiber hinzu**

1.  Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **Treiber** .

2.  Klicken Sie auf **Hinzufügen**.

3.  Navigieren Sie zu der Datei, die für den Treiber hinzugefügt werden soll, und klicken Sie dann auf **Öffnen**.

    **Hinweis**  Die Treiberdatei wird vom Hersteller des Speichers oder des Netzwerkcontrollers bereitgestellt.

     

4.  Wiederholen Sie die Schritte 2 und 3 für jeden Treiber, den Sie einbeziehen möchten.

5.  Klicken Sie auf **Weiter**.

## Hinzufügen von optionalen WinPE-Paketen zum Wiederherstellungsabbild


Auf der Registerkarte "WinPE" auf der Seite "Erweiterte Optionen" können Sie dem Dart-Bild optionale WinPE-Pakete hinzufügen. Diese Pakete sind Teil des Windows ADK, das eine Installationsvoraussetzung für den Dart-Wiederherstellungsbild-Assistenten ist. Die Tools, die Sie auswählen können, sind alle optional. Alle erforderlichen Pakete werden automatisch basierend auf den Tools hinzugefügt, die Sie auf der Seite "Tools" ausgewählt haben.

Sie können auch die Größe des Scratch-Space angeben. Scratch-Speicherplatz ist die Größe des RAM-Speicherplatzes, der für die Ausführung von DART reserviert ist. Der Scratch-Bereich ist nützlich, wenn die Festplatte des Endbenutzers nicht verfügbar ist. Wenn Sie zusätzliche Tools und Treiber ausführen, möchten Sie möglicherweise den Scratch-Platz erhöhen.

**So fügen Sie dem Wiederherstellungsabbild optionale WinPE-Pakete hinzu**

1.  Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **WinPE** .

2.  Aktivieren Sie das Kontrollkästchen neben jedem Paket, das Sie in das Bild einbeziehen möchten, oder klicken Sie auf das Kontrollkästchen **Name** , um alle Pakete auszuwählen.

3.  Wählen Sie im Feld **Scratch Space** den RAM-Speicherplatz aus, der für die Ausführung von DART reserviert werden soll, falls die Festplatte des Endbenutzers nicht verfügbar ist.

4.  Klicken Sie auf **Weiter**.

## Hinzufügen der Debugging-Tools für Crash Analyzer


Wenn Sie das Tool Absturzanalyse in das ISO-Abbild einbeziehen, müssen Sie auch die Debugging-Tools für Windows einbeziehen. Auf der Seite "Erweiterte Optionen" auf der Registerkarte Crash Analyzer geben Sie den Pfad der Windows 8-Debugging-Tools ein, die von Crash Analyzer zum Analysieren von Speicherabbilddateien verwendet werden. Sie können die Tools verwenden, die sich auf dem Computer befinden, auf dem Sie den Dart-Wiederherstellungsbild-Assistenten ausführen, oder Sie können die Tools verwenden, die sich auf dem Computer des Endbenutzers befinden. Wenn Sie die Tools auf dem Endbenutzercomputer verwenden möchten, denken Sie daran, dass auf jedem Computer, den Sie diagnostizieren, die Debug-Tools installiert sein müssen.

Wenn Sie das Microsoft Windows Software Development Kit (SDK) oder das Microsoft Windows Development Kit (WDK) installiert haben, werden die Windows 8-Debugging-Tools standardmäßig zum Wiederherstellungsbild hinzugefügt, und der Pfad zu den Debugging-Tools wird automatisch ausgefüllt. Sie können den Pfad der Windows 8-Debugging-Tools ändern, wenn sich die Dateien an einem anderen Ort als dem durch den Standard Dateipfad angegebenen Speicherort befinden. Mit einem Link im Assistenten können Sie Debugging-Tools für Windows herunterladen und installieren, wenn diese noch nicht installiert sind.

Informationen zum Herunterladen der Windows-Debugging-Tools finden Sie unter [Debuggen von Tools für Windows](https://go.microsoft.com/fwlink/?LinkId=266248). Installieren Sie die Debug-Tools am Standardspeicherort.

**Hinweis**  Der Dart-Assistent überprüft die Tools im `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` Registrierungsschlüssel. Wenn der Registrierungswert nicht vorhanden ist, sucht der Assistent je nach ihrer Systemarchitektur an einem der folgenden Speicherorte:

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x86`

 

**So fügen Sie die Debugging-Tools für Crash Analyzer hinzu**

1.  Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **Crash Analyzer** .

2.  Optional Klicken Sie auf **Debug-Tools herunterladen** , um die Debugging-Tools für Windows herunterzuladen.

3.  Wählen Sie eine der folgenden Optionen aus:

    -   **Schließen Sie die Windows 8 &lt; 64-Bit-oder 32-Bit- &gt; Debugging-Tools ein**. Wenn Sie diese Option auswählen, navigieren Sie zu dem Speicherort der Tools, und wählen Sie ihn aus, wenn der Pfad noch nicht angezeigt wird.

    -   **Verwenden Sie die Debugging-Tools des Systems, das gedebuggt wird**. Wenn Sie diese Option auswählen, funktioniert der Absturzanalyse Programm nicht, wenn die Debugging-Tools für Windows auf dem Problem Computer nicht gefunden werden.

4.  Klicken Sie auf **Weiter**.

## Hinzufügen von Definitionen für das Defender-Tool


Auf der Registerkarte Defender der Seite Erweiterte Optionen fügen Sie Definitionen hinzu, die vom Defender-Tool verwendet werden, um zu ermitteln, ob Software, die versucht, die Einstellungen auf einem Computer zu installieren, auszuführen oder zu ändern, unerwünschte oder bösartige Software ist.

**So fügen Sie Definitionen für das Defender-Tool hinzu**

1.  Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **Defender** .

2.  Wählen Sie eine der folgenden Optionen aus:

    -   **Laden Sie die neuesten Definitionen herunter (empfohlen)** – das Definitionsupdate wird automatisch gestartet, und die Definitionen werden dem Dart-Wiederherstellungsbild hinzugefügt. Diese Option wird empfohlen, damit Sie Fälle vermeiden können, in denen die Definitionen möglicherweise nicht verfügbar sind. Sie müssen mit dem Internet verbunden sein, um die Definitionen herunterladen zu können.

    -   **Herunterladen der Definitionen später** – Definitionen werden nicht im Dart-Wiederherstellungsbild enthalten sein, und Sie müssen die Definitionen von dem Computer herunterladen, auf dem Dart ausgeführt wird.

        Wenn Sie sich entschließen, die neuesten Definitionen nicht in das Wiederherstellungsabbild aufzunehmen, oder wenn die Definitionen, die in dem Wiederherstellungsabbild enthalten sind, nicht mehr aktuell sind, wenn Sie Defender verwenden möchten, besorgen Sie sich die neuesten Definitionen, bevor Sie mit dem Scannen beginnen, indem Sie die Anweisungen befolgen, die in Defender bereitgestellt werden.

        **Wichtig**  Sie können nicht überprüfen, ob keine Definitionen vorhanden sind.

         

3.  Klicken Sie auf **Weiter**.

## Auswählen der zu erstellende Typen von Wiederherstellungsbild Dateien


Wählen Sie auf der Seite "Bild erstellen" einen Ausgabeordner für das Wiederherstellungsabbild aus, geben Sie einen Bildnamen ein, und wählen Sie die Typen von DART-Wiederherstellungsbild Dateien aus, die Sie erstellen möchten. Während der Erstellung des Wiederherstellungsprozesses werden die Windows-Quelldateien entpackt, Dart-Dateien werden kopiert, und das Bild wird dann in die Dateiformate, die Sie auf dieser Seite ausgewählt haben, "neu verpackt".

Die verfügbaren Bilddateitypen sind:

-   **Windows Imaging-Datei (WIM)** – wird zum Bereitstellen von Dart in einer PXE-Umgebung (Preboot Execution Environment) oder einer lokalen Partition verwendet.

-   **ISO-Abbilddatei** – wird für die Bereitstellung auf CD oder DVD oder für die Verwendung in virtuellen Maschinen (VM) s) verwendet. Der Assistent setzt voraus, dass das ISO-Abbild eine ISO-Dateinamenerweiterung aufweist, da für die meisten Programme, die eine CD oder DVD brennen, diese Erweiterung erforderlich ist. Wenn Sie keinen anderen Speicherort angeben, wird das ISO-Abbild auf dem Desktop mit dem Namen DaRT8. ISO erstellt.

-   **PowerShell-Skript** – erstellt ein DART-Wiederherstellungsbild mit Befehlen, die im wesentlichen dieselben Optionen bieten, die Sie mithilfe des DART-Wiederherstellungsbild-Assistenten auswählen können. Mit dem Skript können Sie auch Dateien im Dart-Wiederherstellungsbild hinzufügen oder ändern.

Wenn Sie auf dieser Seite das Kontrollkästchen Bild bearbeiten aktivieren, können Sie das Wiederherstellungsbild während des Bild Erstellungsvorgangs anpassen. So können Sie beispielsweise die Datei "winpeshl.ini" ändern, um eine benutzerdefinierte Startreihenfolge zu erstellen oder Tools von Drittanbietern hinzuzufügen.

**So wählen Sie die Typen von Wiederherstellungsbild Dateien aus, die erstellt werden sollen**

1.  Klicken Sie auf der Seite **Bild erstellen** auf **Durchsuchen** , um den Ausgabeordner für die Bilddatei auszuwählen.

    **Hinweis**  Die Größe des Bilds hängt von den ausgewählten Tools und den Dateien ab, die Sie im Assistenten hinzufügen.

     

2.  Geben Sie im Feld **Bildname** einen Namen für das DART-Wiederherstellungsbild ein, oder übernehmen Sie den Standardnamen DaRT8.

    Der Assistent erstellt einen Unterordner im Ausgabepfad mit diesem Namen.

3.  Wählen Sie die Typen von Bilddateien aus, die Sie erstellen möchten.

4.  Wählen Sie eine der folgenden Optionen aus:

    -   Wenn Sie die Dateien im Wiederherstellungsabbild ändern möchten, bevor Sie die Bilddateien erstellen, aktivieren Sie das Kontrollkästchen **Bild bearbeiten** , und klicken Sie dann auf **vorbereiten**.

    -   Wenn Sie das Wiederherstellungsabbild erstellen möchten, ohne die Dateien zu ändern, klicken Sie auf **Erstellen**.

5.  

    Klicken Sie auf **Weiter**.

## Bearbeiten der Wiederherstellungsbild Dateien


Sie können das Wiederherstellungsbild nur bearbeiten, wenn Sie auf der Seite Bild erstellen das Kontrollkästchen Bild bearbeiten aktiviert haben. Nachdem das Wiederherstellungsabbild für die Bearbeitung vorbereitet wurde, können Sie die Wiederherstellungsabbild Dateien hinzufügen und ändern, bevor Sie das startfähige Medium erstellen. So können Sie beispielsweise eine benutzerdefinierte Reihenfolge für den Start erstellen, verschiedene Tools von Drittanbietern hinzufügen usw.

**So bearbeiten Sie die Wiederherstellungsbild Dateien**

1.  Klicken Sie auf der Seite **Bild bearbeiten** auf in Windows-Explorer **Öffnen** .

2.  Erstellen Sie einen Unterordner in dem Ordner, der im Dialogfeld aufgeführt ist.

3.  Kopieren Sie die gewünschten Dateien in den neuen Unterordner, oder entfernen Sie die Dateien, die Sie nicht benötigen.

4.  Klicken Sie auf **Erstellen** , um die Erstellung des Wiederherstellungs Bilds zu starten.

## Generieren der Wiederherstellungsbild Dateien


Auf der Seite "Dateien generieren" wird das DART-Wiederherstellungsbild für die Dateitypen generiert, die Sie auf der Seite "Bild erstellen" ausgewählt haben.

**So generieren Sie die Wiederherstellungsbild Dateien**

-   Klicken Sie auf der Seite **Dateien generieren** auf **weiter** , um die Wiederherstellungsabbild Dateien zu generieren.

## Kopieren des Wiederherstellungs Bilds auf eine CD, DVD oder USB


Auf der Seite startbare Medien erstellen können Sie die Bilddatei optional auf eine CD, DVD oder ein USB-Flashlaufwerk (USB-Stick) kopieren. Sie können auf dieser Seite auch weitere startbare Medien erstellen, indem Sie den Assistenten erneut starten.

**Hinweis**  Die PXE-Installation (Preboot Execution Environment) und die Bereitstellung lokaler Bilder werden von diesem Tool nicht nativ unterstützt, da Sie zusätzliche Enterprise-Tools wie System Center Configuration Manager-Server und Microsoft Development Toolkit erfordern.

 

**So kopieren Sie das Wiederherstellungsabbild auf eine CD, DVD oder USB**

1.  Wählen Sie auf der Seite startbare **Medien erstellen** die ISO-Datei aus, die Sie kopieren möchten.

2.  Legen Sie eine CD, DVD oder USB ein, und wählen Sie dann das Laufwerk aus.

    **Hinweis**  Wenn ein Laufwerk nicht erkannt wird und Sie ein neues Laufwerk installieren, können Sie auf **Aktualisieren** klicken, um den Assistenten zu zwingen, die Liste der verfügbaren Laufwerke zu aktualisieren.

     

3.  Klicken Sie auf die Schaltfläche **startfähige Medien erstellen** .

4.  Wenn Sie ein weiteres Wiederherstellungsabbild erstellen möchten, klicken Sie auf neu starten, oder klicken Sie auf **Schließen** , wenn Sie mit dem Erstellen aller gewünschten Medien fertig sind.

## Verwandte Themen


[Übersicht über die Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md)

[Bereitstellen von DaRT 8.0](deploying-dart-80-dart-8.md)

 

 





