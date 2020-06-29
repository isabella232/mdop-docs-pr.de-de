---
title: So ändern Sie die Client-Konfiguration mithilfe von PowerShell
description: So ändern Sie die Client-Konfiguration mithilfe von PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805270"
---
# <span data-ttu-id="52409-103">So ändern Sie die Client-Konfiguration mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="52409-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="52409-104">Gehen Sie wie folgt vor, um die App-V 5,0-Clientkonfiguration zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="52409-104">Use the following procedure to configure the App-V 5.0 client configuration.</span></span>

**<span data-ttu-id="52409-105">So ändern Sie die App-V 5,0-Clientkonfiguration mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="52409-105">To modify App-V 5.0 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="52409-106">Verwenden Sie das Cmdlet " **festlegen-AppvClientConfiguration** ", um die Clienteinstellungen mithilfe von PowerShell zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="52409-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span>

2.  <span data-ttu-id="52409-107">Wenn Sie die Clientkonfiguration ändern möchten, öffnen Sie eine PowerShell-Eingabeaufforderung, und führen Sie das folgende Cmdlet **-AppvClientConfiguration** mit allen erforderlichen Parametern aus.</span><span class="sxs-lookup"><span data-stu-id="52409-107">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="52409-108">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="52409-108">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="52409-109">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="52409-109">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="52409-110">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="52409-110">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="52409-111">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="52409-111">Got an App-V issue?</span></span>** <span data-ttu-id="52409-112">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="52409-112">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="52409-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="52409-113">Related topics</span></span>


[<span data-ttu-id="52409-114">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="52409-114">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





