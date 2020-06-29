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
# <span data-ttu-id="737ad-103">So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück</span><span class="sxs-lookup"><span data-stu-id="737ad-103">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>


<span data-ttu-id="737ad-104">Gehen Sie wie folgt vor, um ein App-v 5,1-Paket mit der Benutzerkonfigurationsdatei auf das App-v-Dateiformat zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="737ad-104">Use the following procedure to revert an App-V 5.1 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="737ad-105">So kehren Sie ein Paket zurück</span><span class="sxs-lookup"><span data-stu-id="737ad-105">To revert a package</span></span>**

1.  <span data-ttu-id="737ad-106">Stellen Sie sicher, dass das App-v 4,6-Paket für die Benutzer veröffentlicht wird, aber die FTA und Tastenkombinationen wurden vom APP-v 5,1-Paket unter Verwendung der folgenden Migrationsmethode angenommen, [wie Sie Erweiterungspunkte aus einem App-v 4,6-Paket zu app-v 5,1 für einen bestimmten Benutzer migrieren](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="737ad-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span></span>

    <span data-ttu-id="737ad-107">Wenn Sie im Abschnitt **userConfiguration** der Bereitstellungs Konfigurationsdatei für das konvertierte Paket die Richtlinie festlegen möchten, führen Sie folgendes Update für den **userConfiguration** -Abschnitt aus: \*\*ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; Paket-ID &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="737ad-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="737ad-108">Geben Sie an einer Eingabeaufforderung mit erhöhten Rechten Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="737ad-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="737ad-109">PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationPath** &lt; Pfad zur Benutzerkonfigurationsdatei&gt;</span><span class="sxs-lookup"><span data-stu-id="737ad-109">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="737ad-110">Führen Sie eine Veröffentlichungsaktualisierung durch, oder warten Sie, bis die nächste geplante Veröffentlichungsaktualisierung für die App-V 4,6 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="737ad-110">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="737ad-111">Öffnen Sie die Anwendung über FTA oder Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="737ad-111">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="737ad-112">Die Anwendung sollte nun mit App-V 4,6 geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="737ad-112">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="737ad-113">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="737ad-113">Note</span></span>**  
    <span data-ttu-id="737ad-114">Wenn Sie das App-v 5,1-Paket nicht mehr benötigen, können Sie die Veröffentlichung des App-v 5,1-Pakets aufheben, und die Erweiterungspunkte werden automatisch auf App-v 4,6 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="737ad-114">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="737ad-115">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="737ad-115">Related topics</span></span>


[<span data-ttu-id="737ad-116">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="737ad-116">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









