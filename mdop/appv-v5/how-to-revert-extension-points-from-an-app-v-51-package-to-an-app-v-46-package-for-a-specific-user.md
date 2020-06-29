---
title: So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück
description: So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück
author: dansimp
ms.assetid: bd53c5d6-7fd2-4816-b03b-d59da0a35819
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a69d6fb5b180161f39aa89e03b52227f32ce4879
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805198"
---
# So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück


Gehen Sie wie folgt vor, um ein App-v 5,1-Paket mit der Benutzerkonfigurationsdatei auf das App-v-Dateiformat zurückzusetzen.

**So kehren Sie ein Paket zurück**

1.  Stellen Sie sicher, dass das App-v 4,6-Paket für die Benutzer veröffentlicht wird, aber die FTA und Tastenkombinationen wurden vom APP-v 5,1-Paket unter Verwendung der folgenden Migrationsmethode angenommen, [wie Sie Erweiterungspunkte aus einem App-v 4,6-Paket zu app-v 5,1 für einen bestimmten Benutzer migrieren](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).

    Wenn Sie im Abschnitt **userConfiguration** der Bereitstellungs Konfigurationsdatei für das konvertierte Paket die Richtlinie festlegen möchten, führen Sie folgendes Update für den **userConfiguration** -Abschnitt aus: **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; Paket-ID &gt; **

2.  Geben Sie an einer Eingabeaufforderung mit erhöhten Rechten Folgendes ein:

    PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationPath** &lt; Pfad zur Benutzerkonfigurationsdatei&gt;

3.  Führen Sie eine Veröffentlichungsaktualisierung durch, oder warten Sie, bis die nächste geplante Veröffentlichungsaktualisierung für die App-V 4,6 ausgeführt wird. Öffnen Sie die Anwendung über FTA oder Tastenkombinationen. Die Anwendung sollte nun mit App-V 4,6 geöffnet werden.

    **Hinweis:**  
    Wenn Sie das App-v 5,1-Paket nicht mehr benötigen, können Sie die Veröffentlichung des App-v 5,1-Pakets aufheben, und die Erweiterungspunkte werden automatisch auf App-v 4,6 zurückgesetzt.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)









