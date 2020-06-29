---
title: Konfigurieren der Umgebungsvoraussetzungen
description: Konfigurieren der Umgebungsvoraussetzungen
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811761"
---
# <span data-ttu-id="49709-103">Konfigurieren der Umgebungsvoraussetzungen</span><span class="sxs-lookup"><span data-stu-id="49709-103">Configure Environment Prerequisites</span></span>


<span data-ttu-id="49709-104">Bevor Sie Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 bereitstellen und ausführen können, müssen Sie sicherstellen, dass Ihre Umgebung die folgenden Mindestvoraussetzungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="49709-104">Before you can deploy and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you must ensure that your environment meets the following minimum prerequisites.</span></span>

**<span data-ttu-id="49709-105">Windows7</span><span class="sxs-lookup"><span data-stu-id="49709-105">Windows 7</span></span>**

<span data-ttu-id="49709-106">Der Med-v-Host-Agent und der Med-v-Arbeitsbereichs-Packager werden nur in Windows 7 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="49709-106">The MED-V Host Agent and the MED-V Workspace Packager are only supported in Windows 7 or newer.</span></span>

**<span data-ttu-id="49709-107">Windows XP SP3</span><span class="sxs-lookup"><span data-stu-id="49709-107">Windows XP SP3</span></span>**

<span data-ttu-id="49709-108">Der MED-V-Gast-Agent wird nur in Windows XP SP3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="49709-108">The MED-V Guest Agent is only supported in Windows XP SP3.</span></span>

**<span data-ttu-id="49709-109">.NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="49709-109">.NET Framework 3.5 SP1</span></span>**

<span data-ttu-id="49709-110">Für den Med-v-Host und die Guest-Agents sowie für den Med-v-Arbeitsbereichs-Packager ist Microsoft .NET Framework 3,5 SP1 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="49709-110">The MED-V Host and Guest agents and the MED-V Workspace Packager require the Microsoft .NET Framework 3.5 SP1.</span></span>

<span data-ttu-id="49709-111">**Wichtig**  Sie müssen auch das Update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) , das mehrere bekannte Probleme mit der Anwendungskompatibilität behebt, installieren.</span><span class="sxs-lookup"><span data-stu-id="49709-111">**Important** You must also install the update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950), which addresses several known application compatibility issues.</span></span>

 

<span data-ttu-id="49709-112">**Hinweis**  Sie müssen .NET Framework 3,5 SP1 und das Update KB959209 manuell in das Windows Virtual PC-Abbild installieren, das Sie für die Verwendung mit MED-V vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="49709-112">**Note** You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="49709-113">Standardmäßig sind jedoch Microsoft .NET Framework 3,5 SP1 und das Update enthalten, wenn Sie Windows 7 auf dem Hostcomputer installieren.</span><span class="sxs-lookup"><span data-stu-id="49709-113">However, by default, the Microsoft .NET Framework 3.5 SP1 and the update are included when you install Windows 7 on the host computer.</span></span>

 

**<span data-ttu-id="49709-114">Eine Active Directory-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="49709-114">An Active Directory Infrastructure</span></span>**

<span data-ttu-id="49709-115">Gruppenrichtlinien stellen die zentralisierte Verwaltung und Konfiguration von Betriebssystemen, Anwendungen und Benutzereinstellungen in einer Active Directory-Umgebung bereit.</span><span class="sxs-lookup"><span data-stu-id="49709-115">Group Policy provides the centralized management and configuration of operating systems, applications, and users' settings in an Active Directory environment.</span></span>

## <span data-ttu-id="49709-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="49709-116">Related topics</span></span>


[<span data-ttu-id="49709-117">Konfigurieren der Installationsvoraussetzungen</span><span class="sxs-lookup"><span data-stu-id="49709-117">Configure Installation Prerequisites</span></span>](configure-installation-prerequisites.md)

[<span data-ttu-id="49709-118">High-Level-Architektur</span><span class="sxs-lookup"><span data-stu-id="49709-118">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="49709-119">Von MED 2.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="49709-119">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





