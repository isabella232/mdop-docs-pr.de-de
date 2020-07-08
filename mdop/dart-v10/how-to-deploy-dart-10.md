---
title: So stellen Sie DaRT 10 bereit
description: So stellen Sie DaRT 10 bereit
author: dansimp
ms.assetid: 13e8ba20-21c3-4870-94ed-6d3106d69f21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9e78f55e238cce16798525915487e4b753d92e6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804703"
---
# So stellen Sie DaRT 10 bereit


Die folgenden Anweisungen erläutern, wie Sie Microsoft Diagnostics and Recovery Toolset (Dart) 10 in Ihrer Umgebung bereitstellen. Informationen zum Abrufen der Dart-Software finden Sie unter [Abrufen von MDOP](https://go.microsoft.com/fwlink/?LinkId=322049). Es wird davon ausgegangen, dass Sie alle Funktionen auf einem Administratorcomputer installieren. Wenn Sie Dart 10 auf mehreren Computern mithilfe eines elektronischen Softwareverteilungssystems bereitstellen oder deinstallieren müssen, ist es möglicherweise einfacher, Befehlszeilen Installationsoptionen zu verwenden. Beschreibungen und Beispiele der verfügbaren Befehlszeilenoptionen finden Sie in diesem Abschnitt.

**Wichtig**  Bevor Sie Dart installieren, lesen Sie [Dart 10 unterstützte Konfigurationen](dart-10-supported-configurations.md) , um sicherzustellen, dass Sie alle erforderlichen Software installiert haben und der Computer die Mindestsystemanforderungen erfüllt. Auf dem Computer, auf dem Sie Dart installieren, muss Windows 10 ausgeführt werden.

 

Sie können Dart mithilfe einer von zwei unterschiedlichen Konfigurationen installieren:

-   Installieren Sie Dart und alle Dart-Tools auf dem Administratorcomputer.

-   Installieren Sie auf dem Administratorcomputer nur die Tools, die Sie zum Erstellen des DART-Wiederherstellungs Bilds benötigen, und installieren Sie dann den **Remote Verbindungs-Viewer** und optional **Crash Analyzer** auf einem Helpdesk-Computer.

Die Dart-Installationsdatei steht sowohl in 32-Bit-als auch in 64-Bit-Versionen zur Verfügung. Installieren Sie die Version, die der Architektur des Computers entspricht, auf dem Sie den Dart-Wiederherstellungsbild-Assistenten ausführen, nicht die Computerarchitektur des Wiederherstellungs Bilds, das Sie erstellen.

Sie können eine der beiden Versionen der Dart-Installationsdatei verwenden, um ein Wiederherstellungsabbild für 32-Bit-oder 64-Bit-Computer zu erstellen, Sie können jedoch kein Wiederherstellungsabbild für 32-Bit-und 64-Bit-Computer erstellen.

**So installieren Sie Dart und alle Dart-Tools auf einem Administratorcomputer**

1.  Laden Sie die 32-Bit-oder 64-Bit-Version der Dart 10-Installationsdatei herunter. Wählen Sie die Architektur aus, die dem Computer entspricht, auf dem Sie Dart installieren, und führen Sie den Dart-Wiederherstellungsbild-Assistenten aus.

2.  Führen Sie in dem Ordner, in den Sie Dart 10 heruntergeladen haben, die **MSDaRT.msi** Installationsdatei aus, die ihren Systemanforderungen entspricht.

3.  Klicken Sie auf der Seite **Willkommen beim Setup-Assistenten von Microsoft Dart 10** auf **weiter**.

4.  Akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie dann auf **weiter**.

5.  Aktivieren Sie auf der Seite **Microsoft Update** die Option **Microsoft Update verwenden, wenn ich nach Updates Suche**, und klicken Sie dann auf **weiter**.

6.  Wählen Sie auf der Seite **Installationsordner auswählen** einen Ordner aus, oder klicken Sie auf **weiter** , um Dart im Standardinstallationspfad zu installieren.

7.  Wählen Sie auf der Seite **Setup Optionen** die Dart-Features aus, die Sie installieren möchten, oder klicken Sie auf **weiter** , um Dart mit allen Features zu installieren.

8.  Klicken Sie auf **Installieren**, um die Installation zu starten.

9.  Nachdem die Installation erfolgreich abgeschlossen wurde, klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.

## So installieren Sie Dart und alle Dart-Tools auf einem Administratorcomputer mithilfe einer Eingabeaufforderung


Wenn Sie Dart installieren oder deinstallieren, haben Sie die Möglichkeit, die Installationsdateien an der Eingabeaufforderung auszuführen. In diesem Abschnitt werden einige Beispiele für verschiedene Optionen beschrieben, die Sie bei der Installation oder Deinstallation von DART an der Eingabeaufforderung angeben können.

Im folgenden Beispiel wird gezeigt, wie alle DART-Funktionen installiert werden.

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

Im folgenden Beispiel wird gezeigt, wie Sie nur den Dart-Wiederherstellungsbild-Assistenten installieren.

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

Im folgenden Beispiel wird gezeigt, wie nur der Absturzanalyse-und der Dart-Remote Verbindungs Viewer installiert werden.

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

Im folgenden Beispiel wird ein Setupprotokoll für Windows Installer erstellt. Dies ist für das Debuggen hilfreich.

``` syntax
msiexec.exe /i MSDaRT.msi /l*v log.txt 
```

**Hinweis**  Sie können/qn oder/qb hinzufügen, um eine unbeaufsichtigte Installation durchzuführen.

 

**So überprüfen Sie die Dart-Installation**

1.  Klicken Sie auf **Start**, und wählen Sie **Diagnose-und Wiederherstellungs-Toolset**aus.

    Das Fenster " **Diagnose-und Wiederherstellungs-Toolset** " wird geöffnet.

2.  Überprüfen Sie, ob alle Dart-Tools, die Sie für die Installation ausgewählt haben, erfolgreich installiert wurden.

## Verwandte Themen


[Bereitstellen von DaRT 10 für Administratorcomputer](deploying-dart-10-to-administrator-computers.md)

 

 





