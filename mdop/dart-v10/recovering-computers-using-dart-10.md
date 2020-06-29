---
title: Wiederherstellen von Computern mithilfe von DaRT 10
description: Wiederherstellen von Computern mithilfe von DaRT 10
author: dansimp
ms.assetid: 2ad7fab0-c22d-4171-8b5a-b2b7d7c0ad2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2031d55427e24638e41dfc6ed7b0ef437922e9c4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809667"
---
# Wiederherstellen von Computern mithilfe von DaRT 10


Nach der Bereitstellung des Microsoft Diagnostics and Recovery Toolset (Dart) 10-Wiederherstellungsabbilds können Sie Dart 10 zum Wiederherstellen von Computern verwenden. Die Informationen in diesem Abschnitt beschreiben die Wiederherstellungsaufgaben, die Sie ausführen können.

Je nachdem, wie Sie das DART-Wiederherstellungsbild bereitstellen, stehen Ihnen verschiedene Methoden zum Starten von DART zur Auswahl.

-   Legen Sie eine Dart-Wiederherstellungs-Image-CD,-DVD oder ein USB-Flashlaufwerk in den Problem Computer ein, und verwenden Sie es zum Booten in den Computer.

-   Starten Sie DART von einer Wiederherstellungspartition auf dem Problem Computer.

-   Starten Sie DART von einer Remotepartition im Netzwerk.

Informationen zu den vor-und Nachteilen der einzelnen Methoden finden Sie unter [Planen des Speicherns und Bereitstellen des Wiederherstellungs Bilds von DART 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).

Unabhängig davon, welche Methode Sie zum Starten von DART verwenden, müssen Sie das Startgerät im BIOS für die Startoption oder die Optionen aktivieren, die Sie dem Endbenutzer zur Verfügung stellen möchten.

**Hinweis**  Je nach Art der Festplatte, Netzwerkadapter und anderer Hardware, die in Ihrer Organisation verwendet wird, ist die Konfiguration des BIOS einzigartig.

 

## Wiederherstellen eines lokalen Computers mithilfe des DART-Wiederherstellungs Bilds


Wenn Sie einen lokalen Computer mithilfe von DART wiederherstellen möchten, müssen Sie physisch auf dem Computer des Endbenutzers anwesend sein, bei dem Probleme auftreten, bei denen Dart erforderlich ist.

[So stellen Sie lokale Computer mit dem DaRT-Wiederherstellungsabbild wieder her](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md)

## Wiederherstellen eines Remotecomputers mithilfe des DART-Wiederherstellungs Bilds


Mit der Funktion Remote Verbindung in DART kann ein IT-Administrator die Dart-Tools Remote auf einem Endbenutzercomputer ausführen. Nachdem der Endbenutzer bestimmte Informationen bereitgestellt hat (oder von einem Helpdesk-Fachmann, der auf dem Computer des Endbenutzers arbeitet), kann der IT-Administrator oder der Helpdesk-Mitarbeiter die Kontrolle über den Computer des Endbenutzers übernehmen und die erforderlichen Dart-Tools Remote ausführen.

**Wichtig**  Die beiden Computer, die eine Remoteverbindung herstellen, müssen Teil desselben Netzwerks sein.

 

Das Fenster " **Diagnose-und Wiederherstellungs-Toolset** " enthält die Option, Dart auf einem Endbenutzercomputer von einem Administratorcomputer aus Remote auszuführen. Der Endbenutzer öffnet die Dart-Tools auf dem Problem Computer und startet die Remotesitzung durch Klicken auf **Remoteverbindung**.

Das Remote Verbindungs Feature auf dem Endbenutzercomputer erstellt die folgenden Verbindungsinformationen: eine Ticketnummer, einen Port und eine Liste aller verfügbaren IP-Adressen. Die Ticketnummer und der Port werden nach dem Zufallsprinzip generiert.

Der IT-Administrator oder Helpdesk-Mitarbeiter gibt diese Informationen in die **Dart-Remote Verbindungsanzeige** ein, um die Terminaldienste-Verbindung mit dem Endbenutzercomputer herzustellen. Mit der eingerichteten Terminaldienste-Verbindung kann ein IT-Administrator Remote mit den Dart-Tools auf dem Endbenutzercomputer interagieren. Der Endbenutzercomputer verarbeitet dann die Verbindungsinformationen, teilt seinen Bildschirm und antwortet auf Anweisungen vom Computer des IT-Administrators.

[So stellen Sie Remotecomputer mit dem DaRT-Wiederherstellungsabbild wieder her](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md)

## Weitere Ressourcen zum Wiederherstellen von Computern mithilfe von DART 10


[Vorgänge für DaRT 10](operations-for-dart-10.md)

 

 





