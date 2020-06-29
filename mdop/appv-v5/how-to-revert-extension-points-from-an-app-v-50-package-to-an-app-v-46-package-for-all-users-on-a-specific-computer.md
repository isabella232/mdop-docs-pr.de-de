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
# <span data-ttu-id="d39ae-103">So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück</span><span class="sxs-lookup"><span data-stu-id="d39ae-103">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>

<span data-ttu-id="d39ae-104">*Hinweis:*\* App-V 4,6 hat den Mainstream-Support verlassen.</span><span class="sxs-lookup"><span data-stu-id="d39ae-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="d39ae-105">Im folgenden wird davon ausgegangen, dass der App-V 4,6 SP3-Client bereits installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d39ae-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="d39ae-106">Gehen Sie wie folgt vor, um Erweiterungspunkte aus einem App-v 5,0-Paket mit der Bereitstellungs Konfigurationsdatei auf das App-v 4,6-Dateiformat zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d39ae-106">Use the following procedure to revert extension points from an App-V 5.0 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="d39ae-107">So kehren Sie ein Paket zurück</span><span class="sxs-lookup"><span data-stu-id="d39ae-107">To revert a package</span></span>**

1.  <span data-ttu-id="d39ae-108">Stellen Sie sicher, dass das App-v 4,6-Paket für die Benutzer veröffentlicht wird, die frei Hand-und Tastenkombinationen aber vom APP-v 5,0-Paket unter Verwendung der folgenden Migrationsmethode angenommen wurden, [wie Sie Erweiterungspunkte aus einem App-v 4,6-Paket zu einem konvertierten App-v 5,0-Paket für alle Benutzer auf einem bestimmten Computer migrieren](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="d39ae-108">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="d39ae-109">Wenn Sie im Abschnitt **userConfiguration** der Bereitstellungs Konfigurationsdatei für das konvertierte Paket die Richtlinie festlegen möchten, führen Sie folgendes Update für den **userConfiguration** -Abschnitt aus: \*\*ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; Paket-ID &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="d39ae-109">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="d39ae-110">Geben Sie an einer Eingabeaufforderung mit erhöhten Rechten Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="d39ae-110">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="d39ae-111">PS &gt; **-Satz-AppvClientPackage $pkg – DynamicDeploymentConfiguration** - &lt; Pfad zur Deployment-Konfigurationsdatei&gt;</span><span class="sxs-lookup"><span data-stu-id="d39ae-111">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="d39ae-112">PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d39ae-112">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="d39ae-113">Führen Sie eine Veröffentlichungsaktualisierung durch, oder warten Sie auf die nächste geplante Veröffentlichungsaktualisierung für das App-V 4,6 SP2-Paket.</span><span class="sxs-lookup"><span data-stu-id="d39ae-113">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 SP2 package.</span></span>

    <span data-ttu-id="d39ae-114">Öffnen Sie die Anwendung über FTA oder Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="d39ae-114">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="d39ae-115">Die Anwendung sollte nun mit App-V 4,6 geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="d39ae-115">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="d39ae-116">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="d39ae-116">Note</span></span>**  
    <span data-ttu-id="d39ae-117">Wenn Sie das App-v 5,0-Paket nicht mehr benötigen, können Sie die Veröffentlichung des App-v 5,0-Pakets aufheben, und die Erweiterungspunkte werden automatisch auf App-v 4,6 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d39ae-117">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="d39ae-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d39ae-118">Related topics</span></span>


[<span data-ttu-id="d39ae-119">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="d39ae-119">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









