---
title: Planen der Bereitstellung von DaRT 7.0
description: Planen der Bereitstellung von DaRT 7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808683"
---
# Planen der Bereitstellung von DaRT 7.0


Es gibt eine Reihe unterschiedlicher Bereitstellungskonfigurationen und Voraussetzungen, die Sie berücksichtigen müssen, bevor Sie Ihren Bereitstellungsplan erstellen. Dieser Abschnitt enthält Informationen, die Ihnen bei der Erfassung der Informationen helfen können, die Sie benötigen, um einen Bereitstellungsplan zu formulieren, der Ihren geschäftlichen Anforderungen am besten entspricht.

Wenn Sie die Installation von Microsoft Diagnostics and Recovery Toolset (Dart) 7 planen, sollten Sie Folgendes bedenken:

-   Wenn Sie Dart installieren, können Sie entweder alle Funktionen auf einem IT-Administratorcomputer installieren, auf dem Sie alle Aufgaben ausführen, die mit der Ausführung von DART verbunden sind. Oder Sie können nur die Dart-Funktionalität installieren, die das Wiederherstellungsabbild auf dem IT-Administratorcomputer erstellt. Installieren Sie dann die zum Ausführen von DART verwendete Funktionalität wie **Dart Remote Connection Viewer** und **Crash Analyzer**auf einem Helpdesk-Agent-Computer.

-   Damit Sie Dart Remote ausführen können, stellen Sie sicher, dass sich der Helpdesk-Agent-Computer und alle Computer, für die Sie möglicherweise eine Remote Behandlung durchführen, im gleichen Netzwerk befinden.

-   Bevor Sie Dart in die Produktion einführen, können Sie zunächst eine Lab-Umgebung für Tests erstellen. Ein Testlabor sollte mindestens zwei Computer umfassen, eines, das als IT-Administrator/Helpdesk-Agent-Computer fungiert, und eines, das als Endbenutzercomputer fungieren soll. Sie können auch drei Computer in der Übungseinheit verwenden, wenn Sie die Zuständigkeiten des IT-Administrators von denen des Helpdesk-Agents trennen möchten.

## Überprüfen der unterstützten Konfigurationen


Überprüfen Sie die unterstützten Konfigurationsinformationen des Microsoft Diagnostics and Recovery Toolset (Dart) 7, um zu bestätigen, dass die Computer, die Sie für die Client-oder Feature-Installation ausgewählt haben, die Mindestanforderungen für Hardware und Betriebssystem erfüllen.

[Von DaRT 7.0 unterstützte Konfigurationen](dart-70-supported-configurations-dart-7.md)

## Planen des Erstellens des DART-Wiederherstellungs Bilds


Wenn Sie das DART-Wiederherstellungsbild erstellen, müssen Sie entscheiden, welche Tools in das Bild aufgenommen werden sollen. Beachten Sie, dass die Endbenutzer möglicherweise gelegentlich Zugriff auf die verschiedenen Dart-Tools haben, wenn Sie diese Entscheidung treffen. Wenn Sie das Wiederherstellungsabbild erstellen, geben Sie auch an, ob Sie weitere Treiber oder Dateien einbeziehen möchten. Ermitteln Sie die Speicherorte zusätzlicher Treiber oder Dateien, die Sie in das DART-Wiederherstellungsabbild einbeziehen möchten.

Beachten Sie die Voraussetzungen und weitere zusätzliche Planungsempfehlungen für die Erstellung des DART-Wiederherstellungs Bilds.

[Planen der Erstellung des DaRT 7.0-Wiederherstellungsabbilds](planning-to-create-the-dart-70-recovery-image.md)

## Planen des Speicherns und Bereitstellens des DART-Wiederherstellungs Bilds


Zum Speichern und Bereitstellen des DART-Wiederherstellungs Bilds können verschiedene Methoden verwendet werden. Berücksichtigen Sie die vor-und Nachteile der einzelnen Methoden, wenn Sie die Methode ermitteln, die Sie verwenden werden. Denken Sie auch daran, wie Sie Dart in Ihrem Unternehmen verwenden möchten.

**Hinweis**  Möglicherweise möchten Sie in Ihrer Organisation mehr als eine Methode verwenden. So können Sie beispielsweise für die meisten Situationen in DART von einer Remotepartition Booten und einen USB-Stick zur Verfügung stellen, falls der Endbenutzercomputer keine Verbindung mit dem Netzwerk herstellen kann.

 

[Planen der Speicherung und Bereitstellung des DaRT 7.0-Wiederherstellungsabbilds](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## Weitere Ressourcen für die Planung der Bereitstellung von Dart


[Planen von DaRT 7.0](planning-for-dart-70-new-ia.md)

 

 





