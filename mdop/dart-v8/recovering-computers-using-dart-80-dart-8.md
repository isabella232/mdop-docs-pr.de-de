---
title: Wiederherstellen von Computern mithilfe von DaRT 8.0
description: Wiederherstellen von Computern mithilfe von DaRT 8.0
author: dansimp
ms.assetid: 0caeb7d9-c1e6-4f32-bc27-157b91630989
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39bab02488252b53deb971d35bc6872c0a2df73b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810813"
---
# Wiederherstellen von Computern mithilfe von DaRT 8.0


Nach der Bereitstellung des Microsoft Diagnostics and Recovery Toolset (Dart) 8,0-Wiederherstellungsabbilds können Sie Dart 8,0 zum Wiederherstellen von Computern verwenden. Die Informationen in diesem Abschnitt beschreiben die Wiederherstellungsaufgaben, die Sie ausführen können.

Je nachdem, wie Sie das DART-Wiederherstellungsbild bereitstellen, stehen Ihnen verschiedene Methoden zum Starten von DART zur Auswahl.

-   Legen Sie eine Dart-Wiederherstellungs-Image-CD,-DVD oder ein USB-Flashlaufwerk in den Problem Computer ein, und verwenden Sie es zum Booten in den Computer.

-   Starten Sie DART von einer Wiederherstellungspartition auf dem Problem Computer.

-   Starten Sie DART von einer Remotepartition im Netzwerk.

Informationen zu den vor-und Nachteilen der einzelnen Methoden finden Sie unter [Planen des Speicherns und Bereitstellen des Dart 8,0-Wiederherstellungsabbilds](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

Unabhängig davon, welche Methode Sie zum Starten von DART verwenden, müssen Sie das Startgerät im BIOS für die Startoption oder die Optionen aktivieren, die Sie dem Endbenutzer zur Verfügung stellen möchten.

**Hinweis**  Je nach Art der Festplatte, Netzwerkadapter und anderer Hardware, die in Ihrer Organisation verwendet wird, ist die Konfiguration des BIOS einzigartig.

 

## Wiederherstellen eines lokalen Computers mithilfe des DART-Wiederherstellungs Bilds


Wenn Sie einen lokalen Computer mithilfe von DART wiederherstellen möchten, müssen Sie physisch auf dem Computer des Endbenutzers anwesend sein, bei dem Probleme auftreten, bei denen Dart erforderlich ist.

[So stellen Sie lokale Computer mit dem DaRT-Wiederherstellungsabbild wieder her](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md)

## Wiederherstellen eines Remotecomputers mithilfe des DART-Wiederherstellungs Bilds


Mit der Funktion Remote Verbindung in DART kann ein IT-Administrator die Dart-Tools Remote auf einem Endbenutzercomputer ausführen. Nachdem der Endbenutzer bestimmte Informationen bereitgestellt hat (oder von einem Helpdesk-Fachmann, der auf dem Computer des Endbenutzers arbeitet), kann der IT-Administrator oder der Helpdesk-Mitarbeiter die Kontrolle über den Computer des Endbenutzers übernehmen und die erforderlichen Dart-Tools Remote ausführen.

**Wichtig**  Die beiden Computer, die eine Remoteverbindung herstellen, müssen Teil desselben Netzwerks sein.

 

Das Fenster " **Diagnose-und Wiederherstellungs-Toolset** " enthält die Option, Dart auf einem Endbenutzercomputer von einem Administratorcomputer aus Remote auszuführen. Der Endbenutzer öffnet die Dart-Tools auf dem Problem Computer und startet die Remotesitzung durch Klicken auf **Remoteverbindung**.

Das Remote Verbindungs Feature auf dem Endbenutzercomputer erstellt die folgenden Verbindungsinformationen: eine Ticketnummer, einen Port und eine Liste aller verfügbaren IP-Adressen. Die Ticketnummer und der Port werden nach dem Zufallsprinzip generiert.

Der IT-Administrator oder Helpdesk-Mitarbeiter gibt diese Informationen in die **Dart-Remote Verbindungsanzeige** ein, um die Terminaldienste-Verbindung mit dem Endbenutzercomputer herzustellen. Mit der eingerichteten Terminaldienste-Verbindung kann ein IT-Administrator Remote mit den Dart-Tools auf dem Endbenutzercomputer interagieren. Der Endbenutzercomputer verarbeitet dann die Verbindungsinformationen, teilt seinen Bildschirm und antwortet auf Anweisungen vom Computer des IT-Administrators.

[So stellen Sie Remotecomputer mit dem DaRT-Wiederherstellungsabbild wieder her](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md)

## Weitere Ressourcen zum Wiederherstellen von Computern mithilfe von Dart 8,0


[Vorgänge für DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





