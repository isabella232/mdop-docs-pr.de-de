---
ms.reviewer: ''
title: So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück
description: So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück
ms.assetid: f1d2ab1f-0831-4976-b49f-169511d3382a
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2a0660024734806c508043cc2db030c96cfd16a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805204"
---
# <span data-ttu-id="d13c4-103">So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück</span><span class="sxs-lookup"><span data-stu-id="d13c4-103">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>

<span data-ttu-id="d13c4-104">*Hinweis:*\* App-V 4,6 hat den Mainstream-Support verlassen.</span><span class="sxs-lookup"><span data-stu-id="d13c4-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="d13c4-105">Gehen Sie wie folgt vor, um ein App-v 5,0-Paket mit der Benutzerkonfigurationsdatei auf das App-v-Dateiformat zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d13c4-105">Use the following procedure to revert an App-V 5.0 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="d13c4-106">So kehren Sie ein Paket zurück</span><span class="sxs-lookup"><span data-stu-id="d13c4-106">To revert a package</span></span>**

1.  <span data-ttu-id="d13c4-107">Stellen Sie sicher, dass das App-v 4,6-Paket für die Benutzer veröffentlicht wird, aber die FTA und Tastenkombinationen wurden vom APP-v 5,0-Paket unter Verwendung der folgenden Migrationsmethode angenommen, [wie Sie Erweiterungspunkte aus einem App-v 4,6-Paket zu app-v 5,0 für einen bestimmten Benutzer migrieren](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="d13c4-107">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span></span>

    <span data-ttu-id="d13c4-108">Wenn Sie im Abschnitt **userConfiguration** der Bereitstellungs Konfigurationsdatei für das konvertierte Paket die Richtlinie festlegen möchten, führen Sie folgendes Update für den **userConfiguration** -Abschnitt aus: \*\*ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; Paket-ID &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="d13c4-108">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="d13c4-109">Geben Sie an einer Eingabeaufforderung mit erhöhten Rechten Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="d13c4-109">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="d13c4-110">PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationPath** &lt; Pfad zur Benutzerkonfigurationsdatei&gt;</span><span class="sxs-lookup"><span data-stu-id="d13c4-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="d13c4-111">Führen Sie eine Veröffentlichungsaktualisierung durch, oder warten Sie, bis die nächste geplante Veröffentlichungsaktualisierung für die App-V 4,6 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d13c4-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="d13c4-112">Öffnen Sie die Anwendung über FTA oder Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="d13c4-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="d13c4-113">Die Anwendung sollte nun mit App-V 4,6 SP2 geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="d13c4-113">The Application should now open using App-V 4.6 SP2.</span></span>

    **<span data-ttu-id="d13c4-114">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="d13c4-114">Note</span></span>**  
    <span data-ttu-id="d13c4-115">Wenn Sie das App-v 5,0-Paket nicht mehr benötigen, können Sie die Veröffentlichung des App-v 5,0-Pakets aufheben, und die Erweiterungspunkte werden automatisch auf App-v 4,6 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d13c4-115">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="d13c4-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d13c4-116">Related topics</span></span>


[<span data-ttu-id="d13c4-117">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="d13c4-117">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)












