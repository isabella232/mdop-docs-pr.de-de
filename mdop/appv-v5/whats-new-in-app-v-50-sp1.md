---
title: Neuigkeiten in App-V 5.0 SP1
description: Neuigkeiten in App-V 5.0 SP1
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804811"
---
# Neuigkeiten in App-V 5.0 SP1


Dieser Abschnitt richtet sich an Benutzer, die bereits mit App-v vertraut sind und wissen möchten, was sich in App-v 5,0 SP1 geändert hat. Wenn Sie noch nicht mit App-v vertraut sind, sollten Sie zunächst die [Planung für App-v 5,0](planning-for-app-v-50-rc.md)lesen.

## Änderungen der Standard Funktionalität


Die folgenden Abschnitte enthalten Informationen zu den Änderungen in den Standardfunktionen für App-V 5,0 SP1.

### Änderungen an unterstützten Sprachen

Weitere Informationen finden Sie unter [Informationen zu App-V 5,0 SP1](about-app-v-50-sp1.md).

Die folgende Liste enthält weitere Informationen zu den neuen Sprachpaketen:

-   Die APP-v 5.0 SP1-Sprachpakete sind im **appv\_xxx\_setup.exe** -Installationsprogramm für alle App-v 5,0-Komponenten gebündelt.

-   Wenn Sie das Installationsprogramm ausführen, wird automatisch das am besten geeignete Sprachpaket installiert, das auf dem Gebietsschema des zugehörigen Betriebssystems basiert, das auf dem Zielcomputer ausgeführt wird.

-   Wenn zusätzliche Sprachpakete erforderlich sind, müssen Sie diese Sprachpakete aus dem Installationsprogramm extrahieren, indem Sie den folgenden Befehl ausführen: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` . Nachdem dies ausgeführt wurde, wird der Inhalt des Installationsprogramms an den angegebenen Speicherort extrahiert.

-   Sie müssen das gewünschte Sprachpaket installieren, indem Sie die entsprechende Windows-Installationsdatei für das Sprachpaket anwenden. Beispielsweise **appv\_hib\_LP\_jmmb\_x86.msi** oder **appv\_hib\_LP\_jmmb\_x64.msi**, wobei **Hib** sich auf die Komponente bezieht und **jmmb** auf das Gebietsschema verweist.

## Erweiterte Unterstützung für Microsoft Office2010


**Microsoft Office 2010-Sequenzierung-Kit für Application Virtualization 5,0** – hilft Benutzern eine konsistente Benutzeroberfläche mit einer virtualisierten Version von Microsoft Office2010 zu bieten. Das **Microsoft Office 2010-Sequenzierung-Kit für Application Virtualization 5,0** wird in Verbindung mit dem **Microsoft Office 2010 Deployment Kit für App-V** verwendet und bietet außerdem den erforderlichen Microsoft Office2010-Lizenzierungsdienst.






## Verwandte Themen


[Informationen zu App-V 5.0](about-app-v-50.md)

 

 





