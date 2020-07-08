---
title: So stellen Sie DaRT 7.0 bereit
description: So stellen Sie DaRT 7.0 bereit
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804685"
---
# So stellen Sie DaRT 7.0 bereit


In diesem Thema finden Sie Anweisungen zum Bereitstellen von Microsoft Diagnostics and Recovery Toolset (Dart) 7 in Ihrer Umgebung. Im ersten Verfahren in diesem Thema wird davon ausgegangen, dass Sie alle Funktionen auf einem Administratorcomputer installieren. Wenn Sie Dart auf mehreren Computern mithilfe eines elektronischen Softwareverteilungssystems bereitstellen oder deinstallieren müssen, ist es möglicherweise einfacher, Befehlszeilen Installationsoptionen zu verwenden. Diese Optionen werden in der zweiten Vorgehensweise in diesem Thema definiert, die eine Beispiel Verwendung für die verfügbaren Befehlszeilenoptionen bietet.

**Wichtig**  Bevor Sie Dart installieren, stellen Sie sicher, dass der Computer die Mindestsystemanforderungen erfüllt, die in [Dart 7,0-unterstützten Konfigurationen](dart-70-supported-configurations-dart-7.md)aufgeführt sind.

 

**So installieren Sie Dart auf einem Administratorcomputer**

1.  Suchen Sie die Dart-Installationsdateien, die Sie im Rahmen Ihres Software Downloads erhalten haben.

2.  Doppelklicken Sie auf die Dart-Installationsdatei, die ihren Systemanforderungen entspricht, entweder 32-Bit oder 64-Bit. Die Dart-Installationsdatei hat den Namen **MSDaRT70.msi**.

3.  Akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie dann auf **weiter**.

4.  Wählen Sie den Zielordner für die Installation von DART aus, wählen Sie aus, ob Dart für alle Benutzer oder nur für den aktuellen Benutzer installiert werden soll, und klicken Sie dann auf **weiter**.

5.  Wählen Sie aus, ob die Installation **Normal**, **Benutzerdefiniert**oder **abgeschlossen**sein soll, und klicken Sie dann auf **weiter**.

    -   **Standard** installiert die Tools, die am häufigsten verwendet werden. Diese Methode wird für die meisten Benutzer empfohlen.

    -   Mit **Benutzerdefiniert** können Sie die Tools auswählen, die installiert sind und wo Sie installiert werden. Dies wird für erfahrene Benutzer empfohlen, insbesondere dann, wenn Sie verschiedene Dart-Tools auf verschiedenen Helpdesk-Computern installieren.

    -   **Complete** installiert alle Dart-Tools und benötigt den meisten Speicherplatz.

    Nachdem Sie Ihre Installationsmethode ausgewählt haben, klicken Sie auf **weiter**.

6.  Klicken Sie auf **Installieren**, um die Installation zu starten.

7.  Nachdem die Installation erfolgreich abgeschlossen wurde, klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.

**So installieren Sie Dart an der Eingabeaufforderung**

1.  Im folgenden Beispiel wird gezeigt, wie alle DART-Funktionen installiert werden.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  Im folgenden Beispiel wird gezeigt, wie Sie nur den **Dart-Wiederherstellungsbild-Assistenten**installieren.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  Im folgenden Beispiel wird gezeigt, wie nur der Absturzanalyse-und der Dart-Remote Verbindungs Viewer installiert werden.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  Im folgenden Beispiel wird ein Setupprotokoll für Windows Installer erstellt. Dies ist für das Debuggen hilfreich.

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

**Hinweis**  Sie können/qn oder/qb zu einer der Optionen für die Eingabeaufforderung zur Dart-Installation hinzufügen, um eine unbeaufsichtigte Installation durchzuführen.

 

## Verwandte Themen


[Bereitstellen von DaRT 7.0 für Administratorcomputer](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





