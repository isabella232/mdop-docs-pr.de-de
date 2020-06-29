---
title: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.1 für einen bestimmten Benutzer
description: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.1 für einen bestimmten Benutzer
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805300"
---
# <span data-ttu-id="ee8ea-103">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.1 für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="ee8ea-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>


<span data-ttu-id="ee8ea-104">Gehen Sie wie folgt vor, um mit App-V erstellte Pakete mithilfe der Benutzerkonfigurationsdatei zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="ee8ea-104">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

<span data-ttu-id="ee8ea-105">**Hinweis**  Bei diesem Verfahren wird davon ausgegangen, dass Sie die neueste Version von App-V 4,6 ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee8ea-105">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>

**<span data-ttu-id="ee8ea-106">So konvertieren Sie ein Paket</span><span class="sxs-lookup"><span data-stu-id="ee8ea-106">To convert a package</span></span>**

1. <span data-ttu-id="ee8ea-107">Suchen Sie die Benutzerkonfigurationsdatei für das Paket, das Sie konvertieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ee8ea-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="ee8ea-108">Um die Richtlinie festzulegen, führen Sie die folgenden Updates im **userConfiguration** -Abschnitt aus: \*\*ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; Paket-ID &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="ee8ea-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="ee8ea-109">Der folgende Code ist ein Beispiel für eine Benutzerkonfigurationsdatei:</span><span class="sxs-lookup"><span data-stu-id="ee8ea-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="ee8ea-110">&lt;? XML-Version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="ee8ea-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="ee8ea-111">&lt;UserConfiguration &lt; -Paket-ID = Paket-ID &gt; Display &lt; Name = Name des Pakets&gt;</span><span class="sxs-lookup"><span data-stu-id="ee8ea-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="ee8ea-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="ee8ea-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="ee8ea-113">PackageName = &lt; Paket-ID&gt;</span><span class="sxs-lookup"><span data-stu-id="ee8ea-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="ee8ea-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="ee8ea-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="ee8ea-115">Zum Hinzufügen des App-V 5,1-Pakets geben Sie Folgendes in ein erweitertes PowerShell-Eingabeaufforderungsfenster ein:</span><span class="sxs-lookup"><span data-stu-id="ee8ea-115">To add the App-V 5.1 package, type the following in an elevated PowerShell command prompt window:</span></span>

   <span data-ttu-id="ee8ea-116">PS &gt; **$pkg = Add-AppvClientPackage – Pfad** &lt; zum Paketspeicherort&gt;</span><span class="sxs-lookup"><span data-stu-id="ee8ea-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="ee8ea-117">PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfiguration** &lt; Pfad zur Benutzerkonfigurationsdatei&gt;</span><span class="sxs-lookup"><span data-stu-id="ee8ea-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="ee8ea-118">Öffnen Sie die Anwendung jetzt über FTA oder Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="ee8ea-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="ee8ea-119">Die Anwendung sollte mit App-V 5,1 geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ee8ea-119">The application should open using App-V 5.1.</span></span>

   <span data-ttu-id="ee8ea-120">Das App-v 4,6-Paket und das konvertierte App-v 5,1-Paket werden für den Benutzer veröffentlicht, aber die FTA-und Tastenkombinationen für die Anwendungen wurden vom APP-v 5,1-Paket übernommen.</span><span class="sxs-lookup"><span data-stu-id="ee8ea-120">The App-V 4.6 package and the converted App-V 5.1 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.1 package.</span></span>

   <span data-ttu-id="ee8ea-121">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="ee8ea-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ee8ea-122">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="ee8ea-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ee8ea-123">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="ee8ea-123">Got an App-V issue?</span></span>** <span data-ttu-id="ee8ea-124">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ee8ea-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ee8ea-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ee8ea-125">Related topics</span></span>


[<span data-ttu-id="ee8ea-126">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ee8ea-126">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="ee8ea-127">So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück</span><span class="sxs-lookup"><span data-stu-id="ee8ea-127">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





