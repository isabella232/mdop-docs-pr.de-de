---
title: Wiederherstellen des Archivs aus einer Sicherung
description: Wiederherstellen des Archivs aus einer Sicherung
author: dansimp
ms.assetid: b83f6173-a236-4da2-b16e-8df20920d4cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3a1b7039ad587cf9c8d7f914fe3b963e12ba8949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807491"
---
# Wiederherstellen des Archivs aus einer Sicherung


Wenn ein Notfall auftritt und das Archiv für Advanced Group Policy Management (AGPM) beschädigt oder zerstört ist, kann ein AGPM-Administrator (Vollzugriff) das Archiv aus einer im Voraus vorbereiteten Sicherungskopie wiederherstellen und dann aus der Produktionsumgebung der Domäne alle Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) importieren, die sich nicht im Archiv befinden oder für die die Version in der Produktion aktueller ist als im Informationen zum Wiederherstellen einer Archivsicherung auf einem anderen Server finden Sie unter [Verschieben des AGPM-Servers und des Archivs](move-the-agpm-server-and-the-archive-agpm40.md).

Ein Benutzerkonto, das Zugriff auf den AGPM-Server (den Computer, auf dem der AGPM-Dienst installiert ist) und den Ordner mit dem Archiv hat, ist erforderlich, um dieses Verfahren ausführen zu können.

**So stellen Sie das Archiv aus einer Sicherung wieder her**

1.  Beenden Sie den AGPM-Dienst. Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm40.md).

2.  Entfernen des vorhandenen Archivs Standardmäßig ist der Archivordner%ProgramData%\\Microsoft\\AGPM, doch der AGPM-Administrator, der den Microsoft Advanced Group Policy Management-Server installiert hat, hat möglicherweise während des Setups einen anderen Speicherort eingegeben.

3.  Erstellen Sie den Archivordner neu, indem Sie den Archivierungspfad, das AGPM-Dienstkonto, den Archiv Besitzer und den Abhör-Port konfigurieren. Es ist nicht erforderlich, dieselben Werte wie bei der ursprünglichen Installation zu verwenden. Weitere Informationen finden Sie unter [Ändern des AGPM-Diensts](modify-the-agpm-service-agpm40.md).

4.  Kopieren Sie den Inhalt der Archivsicherung in den Archivordner, kopieren Sie die Unterordner und Dateien, um sicherzustellen, dass jeder Unterordner und jede Datei die Berechtigungen des Archivordners erbt. Achten Sie darauf, den Archivordner nicht zu überschreiben.

5.  Wenn Sie nicht sicher sind, ob ein GPO in der Archivsicherung aktueller als die Kopie dieses Gruppenrichtlinienobjekts in der Produktion ist, erstellen Sie einen Unterschiedsbericht, und vergleichen Sie deren Einstellungen. Weitere Informationen finden Sie unter [Identifizieren von Unterschieden zwischen GPOs, GPO-Versionen oder Vorlagen](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md).

6.  Starten Sie den AGPM-Dienst erneut. Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm40.md).

### Weitere Verweise

-   [Sichern des Archivs](back-up-the-archive-agpm40.md)

-   [Verschieben des AGPM-Servers und -Archivs](move-the-agpm-server-and-the-archive-agpm40.md)

-   [Verwalten des Archivs](managing-the-archive-agpm40.md)

 

 





