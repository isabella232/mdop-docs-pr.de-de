---
title: Übersicht über die Tools in DaRT 10
description: Übersicht über die Tools in DaRT 10
author: dansimp
ms.assetid: 752467dd-b646-4335-82ce-9090d4651f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8bef2b92e998bebffae526d4288c76be081fe0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809688"
---
# Übersicht über die Tools in DaRT 10


Im Fenster **Diagnose-und Wiederherstellungs-Toolset** in Microsoft Diagnostics and Recovery Toolset (Dart) 10 können Sie alle einzelnen Tools starten, die Sie beim Erstellen des DART 10-Wiederherstellungs Bilds angeben. Informationen zum Zugriff auf das Toolset " **Diagnose-und Wiederherstellungstools** " finden Sie unter [Wiederherstellen von lokalen Computern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md).

Wenn Sie verfügbar ist, können Sie den **Lösungs-Assistenten** im Fenster **Diagnose-und Wiederherstellungstool Toolset** verwenden, um das Tool auszuwählen, das für Ihr jeweiliges Problem am besten geeignet ist, basierend auf einem kurzen Interview, das der Assistent bereitstellt.

## Erkunden der Dart-Tools


Eine Beschreibung der Dart 10-Tools folgt.

### Computerverwaltung

**Computerverwaltung** ist eine Sammlung von Windows-Verwaltungstools, die Ihnen bei der Problembehandlung eines Problem Computers helfen. Sie können die Tools für die **Computer Verwaltung** in DART verwenden, um Systeminformationen und Ereignisprotokolle anzuzeigen, Datenträger zu verwalten, Autoruns aufzulisten und Dienste und Treiber zu verwalten. Die **Computer Verwaltungs** Konsole ist so angepasst, dass Sie Probleme diagnostizieren und beheben können, die das Starten des Windows-Betriebssystems verhindern könnten.

**Hinweis**  Die Wiederherstellung von dynamischen Datenträgern mit Dart wird nicht unterstützt.

 

### Absturzanalyse

Verwenden Sie den **Crash Analyzer-Assistenten** , um die Ursache für einen Computer Fehler schnell zu ermitteln, indem Sie die Speicherabbilddatei unter dem Windows-Betriebssystem analysieren, das Sie reparieren. **Crash Analyzer** untersucht die Speicherabbilddatei für den Treiber, der einen Fehler bei einem Computer verursacht hat. Sie können dann den Problemgeräte Treiber mithilfe des Knotens **Dienste und Treiber** im Tool **Computer Verwaltung** deaktivieren.

Der **Absturzanalyse-Assistent** erfordert die Debugging-Tools für Windows und Symboldateien für das Betriebssystem, das Sie reparieren. Beim Erstellen des DART-Wiederherstellungs Bilds können beide Anforderungen berücksichtigt werden. Wenn Sie nicht im Wiederherstellungsabbild enthalten sind und Sie auf dem zu reparierenden Computer keinen Zugriff darauf haben, können Sie die Speicherabbilddatei auf einen anderen Computer kopieren und die eigenständige Version von **Crash Analyzer** verwenden, um das Problem zu diagnostizieren.

Das Ausführen von **Crash Analyzer** ist eine gute Idee, auch wenn Sie den Computer umbilden möchten. Das Bild kann einen fehlerhaften Treiber aufweisen, der Probleme in Ihrer Umgebung verursacht. Durch Ausführen von **Crash Analyzer**können Sie Problem Treiber identifizieren und die Bildstabilität verbessern.

Weitere Informationen zu **Crash Analyzer**finden Sie unter [Diagnostizieren von System Fehlern mit Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md).

### Disk Commander

Mit **Disk Commander** können Sie Datenträgerpartitionen oder-Volumes mithilfe eines der folgenden Wiederherstellungsprozesse wiederherstellen und reparieren:

-   Wiederherstellen des Master Boot Record (MBR)

-   Wiederherstellen eines oder mehrerer verlorener Volumes

-   Wiederherstellen von Partitionstabellen aus der **Disk Commander** -Sicherung

-   Speichern von Partitionstabellen auf der **Disk Commander** -Sicherung

**Warnung**  Wir empfehlen, dass Sie eine Diskette sichern, bevor Sie **Disk Commander** verwenden, um Sie zu reparieren. Durch die Verwendung von **Disk Commander**können Sie Volumes potenziell beschädigen und darauf zugreifen. Darüber hinaus können Änderungen an einem Volume Auswirkungen auf andere Volumes haben, da Volumes auf einem Datenträger eine Partitionstabelle freigeben.

 

**Hinweis**  Die Wiederherstellung von dynamischen Datenträgern mit Dart wird nicht unterstützt.

 

### Datenträger Zurücksetzung

Sie können die Daten **Träger** Zurücksetzung verwenden, um alle Daten von einem Datenträger oder Volume zu löschen, selbst die Daten, die nach dem Neuformatieren einer Festplatte zurückbleiben. Mit der **Datenträger** Zurücksetzung können Sie entweder ein Single-Pass-Überschreibungs-oder ein vier-Pass-überschreiben auswählen, das den aktuellen US-Standards für Verteidigungsministeriums entspricht.

**Warnung**  Nach dem abwischen einer Festplatte oder eines Volumes können Sie die Daten nicht wiederherstellen. Überprüfen Sie die Größe und Beschriftung eines Volumes, bevor Sie es löschen.

 

### Explorer

Mit dem **Explorer** -Tool können Sie das Dateisystem und die Netzwerkfreigaben des Computers durchsuchen, damit Sie wichtige Daten entfernen können, die der Benutzer auf dem lokalen Laufwerk gespeichert hat, bevor Sie versuchen, den Computer zu reparieren oder zu reimagen. Und da Sie Laufwerkbuchstaben zu Netzwerkfreigaben zuordnen können, können Sie Dateien problemlos vom Computer in das Netzwerk kopieren und verschieben, um Sie zu verwahren oder vom Netzwerk auf den Computer zu übertragen, um Sie wiederherzustellen.

### Datei Wiederherstellung

Mit der **Datei Wiederherstellung** können Sie versuchen, Dateien wiederherzustellen, die versehentlich gelöscht wurden oder die zu groß waren, um in den Papierkorb zu passen. Die **Datei Wiederherstellung** ist nicht auf reguläre Datenträger Volumes limitiert, kann aber Dateien auf verlorenen Volumes oder auf Volumes finden und wiederherstellen, die von BitLocker verschlüsselt wurden.

**Hinweis**  Die Wiederherstellung von dynamischen Datenträgern mit Dart wird nicht unterstützt.

 

### Dateisuche

Bevor Sie einen Computer erneut abbilden, ist das Wiederherstellen von Dateien von der lokalen Festplatte wichtig, insbesondere dann, wenn der Benutzer die Dateien möglicherweise nicht anderweitig gesichert oder gespeichert hat.

Das **Such** Tool öffnet ein **Datei Such** Fenster, das Sie zum Suchen von Dokumenten verwenden können, wenn Sie den Dateipfad nicht kennen oder nach allgemeinen Arten von Dateien auf allen lokalen Festplatten suchen. In bestimmten Pfaden können Sie nach bestimmten Dateinamen Mustern suchen. Sie können die Ergebnisse auch auf einen Datumsbereich oder einen Größenbereich begrenzen.

### Hotfix-Deinstallation

Mit dem **Hotfix-Deinstallations-Assistenten** können Sie Hotfixes oder Service Packs vom Windows-Betriebssystem auf dem Computer entfernen, den Sie reparieren. Verwenden Sie dieses Tool, wenn ein Hotfix oder Service Pack vermutet wird, um zu verhindern, dass das Betriebssystem gestartet wird.

Wir empfehlen, dass Sie nur jeweils einen Hotfix deinstallieren, auch wenn Sie mit dem Tool mehr als eine deinstallieren können.

**Wichtig**  Programme, die nach der Installation eines Hotfixes installiert oder aktualisiert wurden, funktionieren möglicherweise nicht mehr ordnungsgemäß, nachdem Sie einen Hotfix deinstalliert haben.

 

### Schlosser

Mit dem **Schlosser-Assistenten** können Sie das Kennwort für ein lokales Konto auf dem Windows-Betriebssystem festlegen oder ändern, das Sie analysieren oder reparieren. Sie müssen das aktuelle Kennwort nicht kennen. Das von Ihnen festgelegte Kennwort muss jedoch allen Anforderungen entsprechen, die von einem lokalen Gruppenrichtlinienobjekt definiert werden. Dazu gehören Kennwortlänge und-Komplexität.

Sie können **Schlosser** verwenden, wenn das Kennwort für ein lokales Konto, beispielsweise das lokale Administrator Konto, unbekannt ist. Sie können **Schlosser** nicht verwenden, um Kennwörter für Domänenkonten einzurichten.

### Registrierungs-Editor

Sie können den **Registrierungs-Editor** verwenden, um auf die Registrierung des Windows-Betriebssystems zuzugreifen und diese zu ändern, das Sie analysieren oder reparieren. Dazu gehören das Hinzufügen, entfernen und Bearbeiten von Schlüsseln und Werten sowie das Importieren von Registrierungsdateien (reg).

**Warnung**  Ernsthafte Probleme können auftreten, wenn Sie die Registrierung mit dem **Registrierungs-Editor**falsch ändern. Diese Probleme können dazu führen, dass Sie das Betriebssystem neu installieren müssen. Bevor Sie Änderungen an der Registrierung vornehmen, sollten Sie alle wichtigen Daten auf dem Computer sichern. Ändern Sie die Registrierung auf Ihr eigenes Risiko.

 

### SFC-Scan

Das **sfc-Scan** -Tool startet den **Systemdateireparatur-Assistenten** und ermöglicht Ihnen, Systemdateien zu reparieren, die das Starten des installierten Windows-Betriebssystems verhindern. Der **Systemdatei-Reparatur-Assistent** kann Systemdateien, die beschädigt oder nicht vorhanden sind, automatisch reparieren, oder Sie können Sie vor dem Ausführen von Reparaturen auffordern.

### Lösungs-Assistent

Der **Lösungs-Assistent** stellt eine Reihe von Fragen und empfiehlt dann basierend auf Ihren Antworten das beste Tool für die Situation. Dieser Assistent hilft Ihnen bei der Entscheidung, welches Tool Sie verwenden sollen, wenn Sie mit den Tools in DART nicht vertraut sind.

### TCP/IP-Konfiguration

Wenn Sie einen Problem Computer in DART starten, wird er so eingestellt, dass seine TCP/IP-Konfiguration (IP-Adresse und DNS-Server) automatisch vom Dynamic Host Configuration Protocol (DHCP) abgerufen wird. Wenn DHCP nicht verfügbar ist, können Sie TCP/IP mithilfe des **TCP/IP-Konfigurations** Tools manuell konfigurieren. Wählen Sie zuerst einen Netzwerkadapter aus, und konfigurieren Sie dann die IP-Adresse und den DNS-Server für diesen Adapter.

## Verwandte Themen


[Erste Schritte mit DaRT 10](getting-started-with-dart-10.md)

 

 





