---
title: So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück
description: So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück
author: dansimp
ms.assetid: 64640b8e-de6b-4006-a33e-353d285af15e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: ce8d5cc0e79be46fd9680a3bea0236bbeb93ea83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805192"
---
# <span data-ttu-id="e6c74-103">So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück</span><span class="sxs-lookup"><span data-stu-id="e6c74-103">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>


<span data-ttu-id="e6c74-104">Gehen Sie wie folgt vor, um Erweiterungspunkte aus einem App-v 5,1-Paket mit der Bereitstellungs Konfigurationsdatei auf das App-v 4,6-Dateiformat zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="e6c74-104">Use the following procedure to revert extension points from an App-V 5.1 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="e6c74-105">So kehren Sie ein Paket zurück</span><span class="sxs-lookup"><span data-stu-id="e6c74-105">To revert a package</span></span>**

1.  <span data-ttu-id="e6c74-106">Stellen Sie sicher, dass das App-v 4,6-Paket für die Benutzer veröffentlicht wird, die frei Hand-und Tastenkombinationen aber vom APP-v 5,1-Paket unter Verwendung der folgenden Migrationsmethode angenommen wurden, [wie Sie Erweiterungspunkte aus einem App-v 4,6-Paket zu einem konvertierten App-v 5,1-Paket für alle Benutzer auf einem bestimmten Computer migrieren](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="e6c74-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="e6c74-107">Wenn Sie im Abschnitt **userConfiguration** der Bereitstellungs Konfigurationsdatei für das konvertierte Paket die Richtlinie festlegen möchten, führen Sie folgendes Update für den **userConfiguration** -Abschnitt aus: \*\*ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; Paket-ID &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="e6c74-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="e6c74-108">Geben Sie an einer Eingabeaufforderung mit erhöhten Rechten Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="e6c74-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="e6c74-109">PS &gt; **-Satz-AppvClientPackage $pkg – DynamicDeploymentConfiguration** - &lt; Pfad zur Deployment-Konfigurationsdatei&gt;</span><span class="sxs-lookup"><span data-stu-id="e6c74-109">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="e6c74-110">PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="e6c74-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="e6c74-111">Führen Sie eine Veröffentlichungsaktualisierung durch, oder warten Sie auf die nächste geplante Veröffentlichungsaktualisierung für das App-V 4,6-Paket.</span><span class="sxs-lookup"><span data-stu-id="e6c74-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 package.</span></span>

    <span data-ttu-id="e6c74-112">Öffnen Sie die Anwendung über FTA oder Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="e6c74-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="e6c74-113">Die Anwendung sollte nun mit App-V 4,6 geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="e6c74-113">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="e6c74-114">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e6c74-114">Note</span></span>**  
    <span data-ttu-id="e6c74-115">Wenn Sie das App-v 5,1-Paket nicht mehr benötigen, können Sie die Veröffentlichung des App-v 5,1-Pakets aufheben, und die Erweiterungspunkte werden automatisch auf App-v 4,6 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="e6c74-115">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="e6c74-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e6c74-116">Related topics</span></span>


[<span data-ttu-id="e6c74-117">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="e6c74-117">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









