---
title: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.0-Paket für alle Benutzer eines bestimmten Computers
description: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.0-Paket für alle Benutzer eines bestimmten Computers
ms.assetid: 3ae9996f-71d9-4ca1-9aab-25b599158e55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3c53104907448edeb894cf4eb9dbb0a24d3229e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805312"
---
# <span data-ttu-id="5859a-103">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.0-Paket für alle Benutzer eines bestimmten Computers</span><span class="sxs-lookup"><span data-stu-id="5859a-103">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>

<span data-ttu-id="5859a-104">**Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen.</span><span class="sxs-lookup"><span data-stu-id="5859a-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="5859a-105">Gehen Sie wie folgt vor, um Erweiterungspunkte aus einem App-v 4.6-Paket zu einem App-v 5,0-Paket unter Verwendung der Bereitstellungs Konfigurationsdatei zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="5859a-105">Use the following procedure to migrate extension points from an App-V4.6package to a App-V 5.0 package using the deployment configuration file.</span></span>

<span data-ttu-id="5859a-106">**Hinweis**  Für das folgende Verfahren ist kein App-V 5,0-Verwaltungsserver erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5859a-106">**Note** The following procedure does not require an App-V 5.0 management server.</span></span>

 

**<span data-ttu-id="5859a-107">So migrieren Sie Erweiterungspunkte aus einem Paket aus einem App-v 4.6-Paket zu einem konvertierten App-v 5,0-Paket unter Verwendung der Konfigurationsdatei für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="5859a-107">To migrate extension points from a package from an App-V4.6 package to a converted App-V 5.0 package using the deployment configuration file</span></span>**

1. <span data-ttu-id="5859a-108">Suchen Sie das Verzeichnis, das die Bereitstellungs Konfigurationsdatei für das Paket enthält, das Sie migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5859a-108">Locate the directory that contains the deployment configuration file for the package you want to migrate.</span></span> <span data-ttu-id="5859a-109">Um die Richtlinie einzurichten, führen Sie das folgende Update für den **userConfiguration** -Abschnitt aus:</span><span class="sxs-lookup"><span data-stu-id="5859a-109">To set the policy, make the following update to the **userConfiguration** section:</span></span>

   **<span data-ttu-id="5859a-110">ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; Paket-ID&gt;</span><span class="sxs-lookup"><span data-stu-id="5859a-110">ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;</span></span>**

   <span data-ttu-id="5859a-111">Der folgende Code ist ein Beispiel für Inhalte aus einer Konfigurationsdatei für die Bereitstellung:</span><span class="sxs-lookup"><span data-stu-id="5859a-111">The following is an example of content from a deployment configuration file:</span></span>

   <span data-ttu-id="5859a-112">&lt;? XML-Version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="5859a-112">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="5859a-113">&lt;DeploymentConfiguration</span><span class="sxs-lookup"><span data-stu-id="5859a-113">&lt;DeploymentConfiguration</span></span>

   <span data-ttu-id="5859a-114">xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " Paket &lt; -ID = Paket-ID &gt; Display &lt; Name = Anzeige Name&gt;</span><span class="sxs-lookup"><span data-stu-id="5859a-114">xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration>" PackageId=&lt;Package ID&gt; DisplayName=&lt;Display Name&gt;</span></span>

   <span data-ttu-id="5859a-115">&lt;MachineConfiguration/&gt;</span><span class="sxs-lookup"><span data-stu-id="5859a-115">&lt;MachineConfiguration/&gt;</span></span>

   <span data-ttu-id="5859a-116">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="5859a-116">&lt;UserConfiguration&gt;</span></span>

   <span data-ttu-id="5859a-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="5859a-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="5859a-118">PackageName = &lt; Paket-ID&gt;</span><span class="sxs-lookup"><span data-stu-id="5859a-118">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="5859a-119">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="5859a-119">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="5859a-120">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="5859a-120">&lt;/DeploymentConfiguration&gt;</span></span>

2. <span data-ttu-id="5859a-121">Um das App-V 5,0-Paket hinzuzufügen, geben Sie in einer erhöhten PowerShell-Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="5859a-121">To add the App-V 5.0 package, in an elevated PowerShell command prompt type:</span></span>

   <span data-ttu-id="5859a-122">PS &gt; **$pkg = Add-AppvClientPackage** **–** Path &lt; path to Package Location &gt;  - **DynamicDeploymentConfiguration** &lt; path to the Deployment Configuration File&gt;</span><span class="sxs-lookup"><span data-stu-id="5859a-122">PS&gt;**$pkg= Add-AppvClientPackage** **–Path** &lt;Path to package location&gt; -**DynamicDeploymentConfiguration** &lt;Path to the deployment configuration file&gt;</span></span>

   <span data-ttu-id="5859a-123">PS &gt; **Publish-AppVClientPackage $pkg**</span><span class="sxs-lookup"><span data-stu-id="5859a-123">PS&gt;**Publish-AppVClientPackage $pkg**</span></span>

3. <span data-ttu-id="5859a-124">Um die Migration zu testen, öffnen Sie die virtuelle Anwendung mithilfe zugehöriger Freihandelsabkommen oder Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="5859a-124">To test the migration, open the virtual application using associated FTAs or shortcuts.</span></span> <span data-ttu-id="5859a-125">Die Anwendung wird mit App-V 5,0 geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5859a-125">The application opens with App-V 5.0.</span></span> <span data-ttu-id="5859a-126">Sowohl das App-v 4,6-Paket als auch das konvertierte App-v 5,0-Paket werden für den Benutzer veröffentlicht, aber die FTA-und Tastenkombinationen für die Anwendungen wurden vom APP-v 5,0-Paket übernommen.</span><span class="sxs-lookup"><span data-stu-id="5859a-126">Both, the App-V 4.6 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="5859a-127">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="5859a-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="5859a-128">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="5859a-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="5859a-129">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="5859a-129">Got an App-V issue?</span></span>** <span data-ttu-id="5859a-130">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="5859a-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5859a-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5859a-131">Related topics</span></span>


[<span data-ttu-id="5859a-132">So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück</span><span class="sxs-lookup"><span data-stu-id="5859a-132">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="5859a-133">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="5859a-133">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





