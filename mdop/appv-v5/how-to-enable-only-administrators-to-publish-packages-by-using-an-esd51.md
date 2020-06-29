---
title: So schränken Sie die Veröffentlichung von Paketen mithilfe einer ESD auf Administratoren ein
description: So schränken Sie die Veröffentlichung von Paketen mithilfe einer ESD auf Administratoren ein
author: dansimp
ms.assetid: bbc9fda2-fc09-4d72-8d9a-e83d2fcfe234
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22de7f62f540ceff274862c3f16b1f89d9459093
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805468"
---
# <span data-ttu-id="0b1d2-103">So schränken Sie die Veröffentlichung von Paketen mithilfe einer ESD auf Administratoren ein</span><span class="sxs-lookup"><span data-stu-id="0b1d2-103">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span>


<span data-ttu-id="0b1d2-104">Ab App-v 5,0 SP3 können Sie den App-v-Client so konfigurieren, dass nur Administratoren (nicht Endbenutzer) Pakete veröffentlichen oder deren Veröffentlichung aufheben können.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-104">Starting in App-V 5.0 SP3, you can configure the App-V client so that only administrators (not end users) can publish or unpublish packages.</span></span> <span data-ttu-id="0b1d2-105">In früheren Versionen von App-V konnten Sie nicht verhindern, dass Endbenutzer diese Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

**<span data-ttu-id="0b1d2-106">So aktivieren Sie nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen</span><span class="sxs-lookup"><span data-stu-id="0b1d2-106">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="0b1d2-107">Navigieren Sie zum folgenden Gruppenrichtlinien-Objektknoten:</span><span class="sxs-lookup"><span data-stu-id="0b1d2-107">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="0b1d2-108">**Computer Konfiguration &gt; Richtlinien &gt; Administrative Vorlagen &gt; System &gt; App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-108">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="0b1d2-109">Aktivieren Sie die Gruppenrichtlinieneinstellung **Veröffentlichung als Administrator anfordern** .</span><span class="sxs-lookup"><span data-stu-id="0b1d2-109">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="0b1d2-110">Informationen zum Verwenden von PowerShell zum Einrichten dieses Elements finden Sie unter [Verwalten von App-V 5,1-Paketen, die mit PowerShell auf einem eigenständigen Computer ausgeführt](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)werden.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-110">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="0b1d2-111">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="0b1d2-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="0b1d2-112">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="0b1d2-113">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="0b1d2-113">Got an App-V issue?</span></span>** <span data-ttu-id="0b1d2-114">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="0b1d2-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 





