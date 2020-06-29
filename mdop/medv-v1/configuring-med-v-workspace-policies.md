---
title: Konfigurieren von MED-V-Arbeitsbereichsrichtlinien
description: Konfigurieren von MED-V-Arbeitsbereichsrichtlinien
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810807"
---
# <span data-ttu-id="70bb4-103">Konfigurieren von MED-V-Arbeitsbereichsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="70bb4-103">Configuring MED-V Workspace Policies</span></span>


<span data-ttu-id="70bb4-104">Eine MED-V-Arbeitsbereichs Richtlinie ist eine Gruppe von konfigurierbaren Einstellungen, die definieren, wie die virtualisierte Umgebung und Anwendungen auf dem Hostcomputer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70bb4-104">A MED-V workspace policy is a group of configurable settings that define how the virtualized environment and applications perform on the host machine.</span></span> <span data-ttu-id="70bb4-105">In den Themen in diesem Abschnitt werden alle konfigurierbaren Einstellungen in der Med-v-Arbeitsbereichs Richtlinie sowie die Auswirkungen dieser Einstellungen auf den Med-v-Arbeitsbereich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="70bb4-105">The topics in this section describe all the configurable settings in the MED-V workspace policy as well as how these settings influence the MED-V workspace.</span></span>

<span data-ttu-id="70bb4-106">Die folgenden MED-V-Arbeitsbereichstypen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="70bb4-106">The following MED-V workspace types are available:</span></span>

-   <span data-ttu-id="70bb4-107">**Persistent**– in einem beständigen Med-v-Arbeitsbereich werden alle Änderungen und Ergänzungen, die der Benutzer am Med-v-Arbeitsbereich vornimmt, im Med-v-Arbeitsbereich zwischen Sitzungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="70bb4-107">**Persistent**—In a persistent MED-V workspace, all changes and additions the user makes to the MED-V workspace are saved in the MED-V workspace between sessions.</span></span> <span data-ttu-id="70bb4-108">Darüber hinaus wird ein beständiger MED-V-Arbeitsbereich in der Regel in einer Domänenumgebung verwendet.</span><span class="sxs-lookup"><span data-stu-id="70bb4-108">Additionally, a persistent MED-V workspace is generally used in a domain environment.</span></span>

-   <span data-ttu-id="70bb4-109">**Revertible**– in einem Revertible Med-v-Arbeitsbereich wird nach Abschluss jeder Sitzung (d. h., wenn der Med-v-Arbeitsbereich beendet wird) der Med-v-Arbeitsbereich während der Bereitstellung in seinen ursprünglichen Zustand zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="70bb4-109">**Revertible**—In a revertible MED-V workspace, at the completion of each session (that is, when the MED-V workspace is stopped), the MED-V workspace reverts to its original state during deployment.</span></span> <span data-ttu-id="70bb4-110">Keine Änderungen oder Ergänzungen, die der Benutzer vorgenommen hat, werden im MED-V-Arbeitsbereich zwischen Sitzungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="70bb4-110">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span> <span data-ttu-id="70bb4-111">Ein revertible MED-V-Arbeitsbereich kann in einer Domänenumgebung nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70bb4-111">A revertible MED-V workspace cannot be used in a domain environment.</span></span>

<span data-ttu-id="70bb4-112">Es ist wichtig, dass Sie sich für den Typ des Med-v-Arbeitsbereichs entscheiden, den Sie vor der Bereitstellung des Med-v-Arbeitsbereichs erstellen, da es nicht empfehlenswert ist, den Typ des Med-v-Arbeitsbereichs neu zu konfigurieren, nachdem eine Richtlinie für die Benutzer bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="70bb4-112">It is important to decide on the type of MED-V workspace you are creating before deploying the MED-V workspace, because it is not recommended to reconfigure the type of MED-V workspace after a policy has been deployed to users.</span></span>

<span data-ttu-id="70bb4-113">**Hinweis**  Beim Konfigurieren einer Richtlinie wird neben obligatorischen Feldern, die nicht ausgefüllt sind, ein Warnsymbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70bb4-113">**Note** When configuring a policy, a warning symbol appears next to mandatory fields that are not filled in.</span></span> <span data-ttu-id="70bb4-114">Wenn ein Pflichtfeld nicht ausgefüllt ist, wird das Symbol ebenfalls auf der Registerkarte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70bb4-114">If a mandatory field is not filled in, the symbol appears on the tab as well.</span></span>

 

## <span data-ttu-id="70bb4-115">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="70bb4-115">In This Section</span></span>


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="70bb4-116">So wenden Sie allgemeine Einstellungen auf einen MED-V-Arbeitsbereich an</span><span class="sxs-lookup"><span data-stu-id="70bb4-116">How to Apply General Settings to a MED-V Workspace</span></span>](how-to-apply-general-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="70bb4-117">Beschreibt die allgemeinen Einstellungen eines MED-V-Arbeitsbereichs und erläutert, wie Sie auf eine Richtlinie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="70bb4-117">Describes the general settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="70bb4-118">So wenden Sie die Einstellungen des virtuellen Computers auf einen MED-V-Arbeitsbereich an</span><span class="sxs-lookup"><span data-stu-id="70bb4-118">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="70bb4-119">Beschreibt die Einstellungen für den virtuellen Computer für einen MED-V-Arbeitsbereich und erläutert, wie Sie auf eine Richtlinie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="70bb4-119">Describes the virtual machine settings for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[<span data-ttu-id="70bb4-120">So konfigurieren Sie einen Domänenbenutzer oder eine Gruppe</span><span class="sxs-lookup"><span data-stu-id="70bb4-120">How to Configure a Domain User or Group</span></span>](how-to-configure-a-domain-user-or-groupmedvv2.md)  
<span data-ttu-id="70bb4-121">Beschreibt, wie Domänenbenutzer und-Gruppen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="70bb4-121">Describes how to configure domain users and groups.</span></span>

<a href="" id="how-to-configure-published-applications"></a>[<span data-ttu-id="70bb4-122">So konfigurieren Sie veröffentlichte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="70bb4-122">How to Configure Published Applications</span></span>](how-to-configure-published-applicationsmedvv2.md)  
<span data-ttu-id="70bb4-123">Beschreibt veröffentlichte Anwendungen und Menüs sowie Informationen dazu, wie Sie auf eine Richtlinie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="70bb4-123">Describes published applications and menus, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[<span data-ttu-id="70bb4-124">So konfigurieren Sie Webeinstellungen für einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="70bb4-124">How to Configure Web Settings for a MED-V Workspace</span></span>](how-to-configure-web-settings-for-a-med-v-workspace.md)  
<span data-ttu-id="70bb4-125">Beschreibt die Webeinstellungen, die für einen MED-V-Arbeitsbereich verfügbar sind, und erläutert, wie Sie auf eine Richtlinie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="70bb4-125">Describes the Web settings available for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[<span data-ttu-id="70bb4-126">So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="70bb4-126">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
<span data-ttu-id="70bb4-127">Beschreibt das Einrichten eines virtuellen Computers für einen MED-V-Arbeitsbereich und die Anwendung auf eine Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="70bb4-127">Describes the virtual machine setup for a MED-V workspace, and how to apply it to a policy.</span></span>

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="70bb4-128">Anwenden von Netzwerkeinstellungen auf einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="70bb4-128">How to Apply Network Settings to a MED-V Workspace</span></span>](how-to-apply-network-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="70bb4-129">Beschreibt die Netzwerkeinstellungen eines MED-V-Arbeitsbereichs und erläutert, wie Sie auf eine Richtlinie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="70bb4-129">Describes the network settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="70bb4-130">So wenden Sie Leistungseinstellungen auf einen MED-V-Arbeitsbereich an</span><span class="sxs-lookup"><span data-stu-id="70bb4-130">How to Apply Performance Settings to a MED-V Workspace</span></span>](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="70bb4-131">Beschreibt die Leistungseinstellungen eines MED-V-Arbeitsbereichs und erläutert, wie Sie auf eine Richtlinie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="70bb4-131">Describes the performance settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-import-and-export-a-policy"></a>[<span data-ttu-id="70bb4-132">Importieren und Exportieren einer Richtlinie</span><span class="sxs-lookup"><span data-stu-id="70bb4-132">How to Import and Export a Policy</span></span>](how-to-import-and-export-a-policy.md)  
<span data-ttu-id="70bb4-133">Beschreibt, wie Sie eine Richtlinie importieren und exportieren.</span><span class="sxs-lookup"><span data-stu-id="70bb4-133">Describes how to import and export a policy.</span></span>

 

 





