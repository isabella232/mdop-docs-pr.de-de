---
title: Neuigkeiten in App-V 5.0 SP1
description: Neuigkeiten in App-V 5.0 SP1
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804811"
---
# <span data-ttu-id="ea9f7-103">Neuigkeiten in App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="ea9f7-103">What's new in App-V 5.0 SP1</span></span>


<span data-ttu-id="ea9f7-104">Dieser Abschnitt richtet sich an Benutzer, die bereits mit App-v vertraut sind und wissen möchten, was sich in App-v 5,0 SP1 geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 SP1.</span></span> <span data-ttu-id="ea9f7-105">Wenn Sie noch nicht mit App-v vertraut sind, sollten Sie zunächst die [Planung für App-v 5,0](planning-for-app-v-50-rc.md)lesen.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-105">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="ea9f7-106">Änderungen der Standard Funktionalität</span><span class="sxs-lookup"><span data-stu-id="ea9f7-106">Changes in Standard Functionality</span></span>


<span data-ttu-id="ea9f7-107">Die folgenden Abschnitte enthalten Informationen zu den Änderungen in den Standardfunktionen für App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-107">The following sections contain information about the changes in standard functionality for App-V 5.0 SP1.</span></span>

### <span data-ttu-id="ea9f7-108">Änderungen an unterstützten Sprachen</span><span class="sxs-lookup"><span data-stu-id="ea9f7-108">Changes to Supported Languages</span></span>

<span data-ttu-id="ea9f7-109">Weitere Informationen finden Sie unter [Informationen zu App-V 5,0 SP1](about-app-v-50-sp1.md).</span><span class="sxs-lookup"><span data-stu-id="ea9f7-109">For more information, see [About App-V 5.0 SP1](about-app-v-50-sp1.md).</span></span>

<span data-ttu-id="ea9f7-110">Die folgende Liste enthält weitere Informationen zu den neuen Sprachpaketen:</span><span class="sxs-lookup"><span data-stu-id="ea9f7-110">The following list contains more information about the new Language Packs:</span></span>

-   <span data-ttu-id="ea9f7-111">Die APP-v 5.0 SP1-Sprachpakete sind im **appv\_xxx\_setup.exe** -Installationsprogramm für alle App-v 5,0-Komponenten gebündelt.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-111">The App-V 5.0SP1 language packs are bundled into the **appv\_xxx\_setup.exe** installer for all the App-V 5.0 Components.</span></span>

-   <span data-ttu-id="ea9f7-112">Wenn Sie das Installationsprogramm ausführen, wird automatisch das am besten geeignete Sprachpaket installiert, das auf dem Gebietsschema des zugehörigen Betriebssystems basiert, das auf dem Zielcomputer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-112">When you run the installer it will automatically install the most appropriate language pack based on the locale of the associated operating system running on the target computer.</span></span>

-   <span data-ttu-id="ea9f7-113">Wenn zusätzliche Sprachpakete erforderlich sind, müssen Sie diese Sprachpakete aus dem Installationsprogramm extrahieren, indem Sie den folgenden Befehl ausführen: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` .</span><span class="sxs-lookup"><span data-stu-id="ea9f7-113">If additional language packs are required, you must extract these language packs from the installer by running the following command: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”`.</span></span> <span data-ttu-id="ea9f7-114">Nachdem dies ausgeführt wurde, wird der Inhalt des Installationsprogramms an den angegebenen Speicherort extrahiert.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-114">After this has been run, the contents of the installer are extracted to the specified location.</span></span>

-   <span data-ttu-id="ea9f7-115">Sie müssen das gewünschte Sprachpaket installieren, indem Sie die entsprechende Windows-Installationsdatei für das Sprachpaket anwenden.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-115">You must install the desired language pack by applying the appropriate Language pack Windows Installation file.</span></span> <span data-ttu-id="ea9f7-116">Beispielsweise **appv\_hib\_LP\_jmmb\_x86.msi** oder **appv\_hib\_LP\_jmmb\_x64.msi**, wobei **Hib** sich auf die Komponente bezieht und **jmmb** auf das Gebietsschema verweist.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-116">For example, **appv\_hib\_LP\_jmmb\_x86.msi** or **appv\_hib\_LP\_jmmb\_x64.msi**, where **hib** refers to the component and **jmmb** refers to the locale.</span></span>

## <span data-ttu-id="ea9f7-117">Erweiterte Unterstützung für Microsoft Office2010</span><span class="sxs-lookup"><span data-stu-id="ea9f7-117">Enhanced Support for Microsoft Office2010</span></span>


<span data-ttu-id="ea9f7-118">**Microsoft Office 2010-Sequenzierung-Kit für Application Virtualization 5,0** – hilft Benutzern eine konsistente Benutzeroberfläche mit einer virtualisierten Version von Microsoft Office2010 zu bieten.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-118">**Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** – helps provide users with a consistent experience using a virtualized version of Microsoft Office2010.</span></span> <span data-ttu-id="ea9f7-119">Das **Microsoft Office 2010-Sequenzierung-Kit für Application Virtualization 5,0** wird in Verbindung mit dem **Microsoft Office 2010 Deployment Kit für App-V** verwendet und bietet außerdem den erforderlichen Microsoft Office2010-Lizenzierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-119">The **Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** is used in conjunction with the **Microsoft Office 2010 Deployment Kit for App-V** and also provides the required Microsoft Office2010 licensing service.</span></span>






## <span data-ttu-id="ea9f7-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ea9f7-120">Related topics</span></span>


[<span data-ttu-id="ea9f7-121">Informationen zu App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ea9f7-121">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





