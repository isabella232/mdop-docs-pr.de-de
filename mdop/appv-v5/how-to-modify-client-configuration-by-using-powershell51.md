---
title: So ändern Sie die Client-Konfiguration mithilfe von PowerShell
description: So ändern Sie die Client-Konfiguration mithilfe von PowerShell
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805258"
---
# <span data-ttu-id="8d381-103">So ändern Sie die Client-Konfiguration mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d381-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="8d381-104">Gehen Sie wie folgt vor, um die App-V 5,1-Clientkonfiguration zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8d381-104">Use the following procedure to configure the App-V 5.1 client configuration.</span></span>

**<span data-ttu-id="8d381-105">So ändern Sie die App-V 5,1-Clientkonfiguration mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d381-105">To modify App-V 5.1 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="8d381-106">Verwenden Sie das Cmdlet " **festlegen-AppvClientConfiguration** ", um die Clienteinstellungen mithilfe von PowerShell zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8d381-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span> <span data-ttu-id="8d381-107">Weitere Informationen zum Installieren von PowerShell und einer Liste mit Cmdlets finden Sie unter [Laden der PowerShell-Cmdlets und Abrufen der Cmdlet-Hilfe](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span><span class="sxs-lookup"><span data-stu-id="8d381-107">For more information about installing PowerShell, and a list of cmdlets see, [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span></span>

2.  <span data-ttu-id="8d381-108">Wenn Sie die Clientkonfiguration ändern möchten, öffnen Sie eine PowerShell-Eingabeaufforderung, und führen Sie das folgende Cmdlet **-AppvClientConfiguration** mit allen erforderlichen Parametern aus.</span><span class="sxs-lookup"><span data-stu-id="8d381-108">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="8d381-109">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8d381-109">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="8d381-110">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="8d381-110">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="8d381-111">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="8d381-111">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="8d381-112">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="8d381-112">Got an App-V issue?</span></span>** <span data-ttu-id="8d381-113">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="8d381-113">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="8d381-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8d381-114">Related topics</span></span>


[<span data-ttu-id="8d381-115">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="8d381-115">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





