---
title: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer
description: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805306"
---
# <span data-ttu-id="02108-103">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="02108-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>

<span data-ttu-id="02108-104">*Hinweis:*\* App-V 4,6 hat den Mainstream-Support verlassen.</span><span class="sxs-lookup"><span data-stu-id="02108-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="02108-105">Gehen Sie wie folgt vor, um mit App-V erstellte Pakete mithilfe der Benutzerkonfigurationsdatei zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="02108-105">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

**<span data-ttu-id="02108-106">So konvertieren Sie ein Paket</span><span class="sxs-lookup"><span data-stu-id="02108-106">To convert a package</span></span>**

1. <span data-ttu-id="02108-107">Suchen Sie die Benutzerkonfigurationsdatei für das Paket, das Sie konvertieren möchten.</span><span class="sxs-lookup"><span data-stu-id="02108-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="02108-108">Um die Richtlinie festzulegen, führen Sie die folgenden Updates im **userConfiguration** -Abschnitt aus: \*\*ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; Paket-ID &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="02108-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="02108-109">Der folgende Code ist ein Beispiel für eine Benutzerkonfigurationsdatei:</span><span class="sxs-lookup"><span data-stu-id="02108-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="02108-110">&lt;? XML-Version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="02108-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="02108-111">&lt;UserConfiguration &lt; -Paket-ID = Paket-ID &gt; Display &lt; Name = Name des Pakets&gt;</span><span class="sxs-lookup"><span data-stu-id="02108-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="02108-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="02108-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="02108-113">PackageName = &lt; Paket-ID&gt;</span><span class="sxs-lookup"><span data-stu-id="02108-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="02108-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="02108-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="02108-115">Zum Hinzufügen des App-V 5,0-Pakets geben Sie Folgendes in einer erhöhten PowerShell-Eingabeaufforderung ein:</span><span class="sxs-lookup"><span data-stu-id="02108-115">To add the App-V 5.0 package type the following in an elevated PowerShell command prompt:</span></span>

   <span data-ttu-id="02108-116">PS &gt; **$pkg = Add-AppvClientPackage – Pfad** &lt; zum Paketspeicherort&gt;</span><span class="sxs-lookup"><span data-stu-id="02108-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="02108-117">PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfiguration** &lt; Pfad zur Benutzerkonfigurationsdatei&gt;</span><span class="sxs-lookup"><span data-stu-id="02108-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="02108-118">Öffnen Sie die Anwendung jetzt über FTA oder Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="02108-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="02108-119">Die Anwendung sollte mit App-V 5,0 geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="02108-119">The application should open using App-V 5.0.</span></span>

   <span data-ttu-id="02108-120">Das App-v SP2-Paket und das konvertierte App-v 5,0-Paket werden für den Benutzer veröffentlicht, aber die FTA-und Tastenkombinationen für die Anwendungen wurden vom APP-v 5,0-Paket übernommen.</span><span class="sxs-lookup"><span data-stu-id="02108-120">The App-V SP2 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="02108-121">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="02108-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="02108-122">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="02108-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="02108-123">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="02108-123">Got an App-V issue?</span></span>** <span data-ttu-id="02108-124">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="02108-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="02108-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="02108-125">Related topics</span></span>


[<span data-ttu-id="02108-126">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="02108-126">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





