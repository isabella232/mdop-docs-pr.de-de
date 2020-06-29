---
title: So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an
description: So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an
author: dansimp
ms.assetid: 986e638c-4a0c-4a7e-be73-f4615e8b8000
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97b3db253993d6d855384ee5d9771a7f9ff5b64d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805720"
---
# <span data-ttu-id="041b2-103">So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an</span><span class="sxs-lookup"><span data-stu-id="041b2-103">How to Apply the User Configuration File by Using PowerShell</span></span>


<span data-ttu-id="041b2-104">Die Dynamic User-Konfigurationsdatei wird angewendet, wenn ein Paket für einen bestimmten Benutzer veröffentlicht wird, und bestimmt, wie das Paket ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="041b2-104">The dynamic user configuration file is applied when a package is published to a specific user and determines how the package will run.</span></span>

<span data-ttu-id="041b2-105">Gehen Sie wie folgt vor, um eine benutzerspezifische Konfigurationsdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="041b2-105">Use the following procedure to specify a user-specific configuration file.</span></span> <span data-ttu-id="041b2-106">Das folgende Verfahren basiert auf dem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="041b2-106">The following procedure is based on the example:</span></span>

**<span data-ttu-id="041b2-107">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="041b2-107">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="041b2-108">So wenden Sie eine Benutzerkonfigurationsdatei an</span><span class="sxs-lookup"><span data-stu-id="041b2-108">To apply a user Configuration file</span></span>**

1.  <span data-ttu-id="041b2-109">Geben Sie den folgenden Befehl ein, um das Paket auf dem Computer mithilfe der PowerShell-Konsole hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="041b2-109">To add the package to the computer using the PowerShell console type the following command:</span></span>

    <span data-ttu-id="041b2-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.AppV**.</span><span class="sxs-lookup"><span data-stu-id="041b2-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**.</span></span>

2.  <span data-ttu-id="041b2-111">Verwenden Sie den folgenden Befehl, um das Paket für den Benutzer zu veröffentlichen und die aktualisierte Dynamic User-Konfigurationsdatei anzugeben:</span><span class="sxs-lookup"><span data-stu-id="041b2-111">Use the following command to publish the package to the user and specify the updated the dynamic user configuration file:</span></span>

    **<span data-ttu-id="041b2-112">Publish-AppVClientPackage $pkg – DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span><span class="sxs-lookup"><span data-stu-id="041b2-112">Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span></span>**

    <span data-ttu-id="041b2-113">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="041b2-113">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="041b2-114">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="041b2-114">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="041b2-115">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="041b2-115">Got an App-V issue?</span></span>** <span data-ttu-id="041b2-116">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="041b2-116">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="041b2-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="041b2-117">Related topics</span></span>


[<span data-ttu-id="041b2-118">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="041b2-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





