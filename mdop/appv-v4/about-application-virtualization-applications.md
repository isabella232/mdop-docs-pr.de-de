---
title: Informationen zu Application Virtualization-Anwendungen
description: Informationen zu Application Virtualization-Anwendungen
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808167"
---
# Informationen zu Application Virtualization-Anwendungen


In Application Virtualization ist eine *Anwendung* ein ausführbares Programm wie Microsoft Visio, das über einen Application Virtualization-Verwaltungs Server an den Application Virtualization-Desktop Client oder-Client für Remote Desktop Dienste (ehemals Terminal Dienste) gestreamt wird. Bevor eine Anwendung an einen Client gestreamt werden kann, muss die Anwendung für das Streaming vorbereitet werden, indem Sie Sie mit dem Application Virtualization Sequencer verarbeitet.

## Verwalten von Anwendungen


Sie müssen dem Systemanwendungen hinzufügen, bevor Sie die Anwendungen Benutzern zur Verfügung stellen können. Die häufigste Methode zum Hinzufügen von Anwendungen zum System besteht darin, Sie zu importieren. Um auf dieses Feature zuzugreifen, klicken Sie in der Application Virtualization Server-Verwaltungskonsole mit der rechten Maustaste auf den Knoten **Anwendungen** , und wählen Sie **Anwendungen importieren**aus.

Sie können mehr als eine OSD-Datei (Open Software Descriptor) gleichzeitig importieren, oder Sie können eine Sequenzer-Projektdatei (SPRJ) importieren, die mehrere OSD-Dateien enthalten kann. Mit dieser Funktion können Sie verwandte Anwendungen ähnlich konfigurieren.

Sie können auch die folgenden Features verwenden, um Ihnen bei der Verwaltung Ihrer Anwendungen zu helfen:

-   **Anwendungsgruppen**– ermöglicht Ihnen, logische Gruppen von Anwendungen für vereinfachte Verwaltung zu erstellen. Wenn Änderungen an einer Gruppe vorgenommen wurden (beispielsweise Zugriffsberechtigungen), werden die Änderungen auf alle Anwendungen in der Gruppe angewendet. Anwendungen in einer Gruppe können aus unterschiedlichen Paketen stammen.

-   **Mehrfachauswahl**– Sie können mehrere Anwendungen gleichzeitig auswählen, indem Sie die STRG-Taste gedrückt halten, wenn Sie auf eine Anwendung klicken, um die Anwendungseigenschaften zu ändern. Wenn Sie jedoch eine Beziehung zwischen den Anwendungen aufrecht erhalten möchten, sollten Sie eine Anwendungsgruppe erstellen, in der die Anwendungen enthalten sind.

-   **System übergreifende Kopie**– ermöglicht das Kopieren von Anwendungen aus einer Umgebung in eine andere Umgebung, in der dieselbe Version von App-V in einem Schritt ausgeführt wird. Angenommen, Sie verfügen über eine Testumgebung für Benutzerakzeptanz, in der Sie zunächst Anwendungen bereitstellen und konfigurieren. Nachdem Sie die Testphase abgeschlossen haben, möchten Sie möglicherweise denselben Satz von Anwendungen (einschließlich Berechtigungen) in die Produktionsumgebung replizieren.

## Verwandte Themen


[Informationen zu Application Virtualization-Paketen](about-application-virtualization-packages.md)

[Informationen zur Application Virtualization Server Management Console](about-the-application-virtualization-server-management-console.md)

[So verwalten Sie Anwendungsgruppen in der Server Management Console](how-to-manage-application-groups-in-the-server-management-console.md)

[So verwalten Sie Anwendungen in der Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





