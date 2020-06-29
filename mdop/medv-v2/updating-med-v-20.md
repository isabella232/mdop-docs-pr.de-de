---
title: Aktualisieren von MED-V 2.0
description: Aktualisieren von MED-V 2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810132"
---
# <span data-ttu-id="3bc30-103">Aktualisieren von MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="3bc30-103">Updating MED-V 2.0</span></span>


<span data-ttu-id="3bc30-104">Helfen Sie, Ihr System zu sichern, indem Sie die entsprechenden Sicherheitsupdates für Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 anwenden.</span><span class="sxs-lookup"><span data-stu-id="3bc30-104">Help secure your system by applying the appropriate security updates for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="3bc30-105">Aktualisieren von MED-V</span><span class="sxs-lookup"><span data-stu-id="3bc30-105">Updating MED-V</span></span>


<span data-ttu-id="3bc30-106">Sie können MED-V interaktiv, vom Endbenutzer oder im Hintergrund mithilfe eines elektronischen Softwareverteilungssystems aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3bc30-106">You can update MED-V interactively, by the end user, or silently by using an electronic software distribution system.</span></span> <span data-ttu-id="3bc30-107">Bei der Installation des Med-v-Host-Agents wird der Med-v-Host-Agent aktualisiert, und anschließend wird der Med-v-Arbeitsbereich aktualisiert, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3bc30-107">Installation of the MED-V Host Agent upgrades the MED-V Host Agent and then updates the MED-V workspace if required.</span></span> <span data-ttu-id="3bc30-108">Der MED-V-Host-Agent und Gast-Agent bleiben synchron. Wenn Anwendungen vom Med-v-Arbeitsbereich ausgeführt werden, während der Med-v-Host-Agent aktualisiert wird, ist ein Neustart des Hostcomputers erforderlich, um das Update abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3bc30-108">The MED-V Host Agent and Guest Agent keep in sync. If applications are running from the MED-V workspace while the MED-V Host Agent is being updated, a restart of the host computer is required to complete the update.</span></span> <span data-ttu-id="3bc30-109">Wenn keine Anwendungen ausgeführt werden, wird MED-V automatisch neu gestartet, und das Upgrade wird ohne einen Neustart des Hostcomputers durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bc30-109">If no applications are running, MED-V is restarted automatically and the upgrade is completed without a restart of the host computer.</span></span>

<span data-ttu-id="3bc30-110">Wenn Sie MED-V mithilfe eines elektronischen Softwareverteilungssystems aktualisieren, können Sie das Neustartverhalten steuern.</span><span class="sxs-lookup"><span data-stu-id="3bc30-110">If you are updating MED-V by using an electronic software distribution system, you can control the restart behavior.</span></span> <span data-ttu-id="3bc30-111">Unterdrücken Sie dazu den Neustart, indem Sie bei der Installation von MED-V\_HostAgent\_Setup.exe an der Eingabeaufforderung **Reboot = "ReallySuppress"** eingeben.</span><span class="sxs-lookup"><span data-stu-id="3bc30-111">To do this, suppress the restart by typing **REBOOT=”ReallySuppress”** at the command prompt when installing MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="3bc30-112">Konfigurieren Sie dann das elektronische Softwareverteilungssystem, um den 3010-Rückgabecode zu erfassen (der signalisiert, dass ein Neustart erforderlich ist), und führen Sie das Verhalten für das Festlegen des Neustarts aus.</span><span class="sxs-lookup"><span data-stu-id="3bc30-112">Then, configure the electronic software distribution system to capture the 3010 return code (which signals that a restart is required) and perform the set restart behavior.</span></span>

## <span data-ttu-id="3bc30-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3bc30-113">Related topics</span></span>


[<span data-ttu-id="3bc30-114">Technische Referenz für MED-V</span><span class="sxs-lookup"><span data-stu-id="3bc30-114">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





