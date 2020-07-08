---
title: So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück
description: So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805195"
---
# So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück

*Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen. Im folgenden wird davon ausgegangen, dass der App-V 4,6 SP3-Client bereits installiert ist.

Gehen Sie wie folgt vor, um Erweiterungspunkte aus einem App-v 5,0-Paket mit der Bereitstellungs Konfigurationsdatei auf das App-v 4,6-Dateiformat zurückzusetzen.

**So kehren Sie ein Paket zurück**

1.  Stellen Sie sicher, dass das App-v 4,6-Paket für die Benutzer veröffentlicht wird, die frei Hand-und Tastenkombinationen aber vom APP-v 5,0-Paket unter Verwendung der folgenden Migrationsmethode angenommen wurden, [wie Sie Erweiterungspunkte aus einem App-v 4,6-Paket zu einem konvertierten App-v 5,0-Paket für alle Benutzer auf einem bestimmten Computer migrieren](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).

    Wenn Sie im Abschnitt **userConfiguration** der Bereitstellungs Konfigurationsdatei für das konvertierte Paket die Richtlinie festlegen möchten, führen Sie folgendes Update für den **userConfiguration** -Abschnitt aus: **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; Paket-ID &gt; **

2.  Geben Sie an einer Eingabeaufforderung mit erhöhten Rechten Folgendes ein:

    PS &gt; **-Satz-AppvClientPackage $pkg – DynamicDeploymentConfiguration** - &lt; Pfad zur Deployment-Konfigurationsdatei&gt;

    PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationType useDeploymentConfiguration**

3.  Führen Sie eine Veröffentlichungsaktualisierung durch, oder warten Sie auf die nächste geplante Veröffentlichungsaktualisierung für das App-V 4,6 SP2-Paket.

    Öffnen Sie die Anwendung über FTA oder Tastenkombinationen. Die Anwendung sollte nun mit App-V 4,6 geöffnet werden.

    **Hinweis:**  
    Wenn Sie das App-v 5,0-Paket nicht mehr benötigen, können Sie die Veröffentlichung des App-v 5,0-Pakets aufheben, und die Erweiterungspunkte werden automatisch auf App-v 4,6 zurückgesetzt.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Verwandte Themen


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)









