---
title: Beispiele für VM-Konfigurationen
description: Beispiele für VM-Konfigurationen
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810645"
---
# <span data-ttu-id="4b0c2-103">Beispiele für VM-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="4b0c2-103">Examples of Virtual Machine Configurations</span></span>


<span data-ttu-id="4b0c2-104">Im folgenden finden Sie Beispiele für typische Konfigurationen virtueller Computer: eine in einem beständigen Med-v-Arbeitsbereich und eine in einem revertible Med-v-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4b0c2-104">The following are examples of typical virtual machine configurations: one in a persistent MED-V workspace and one in a revertible MED-V workspace.</span></span>

<span data-ttu-id="4b0c2-105">**Hinweis**  Diese Beispiele sind nicht für die Verwendung in allen Umgebungen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="4b0c2-105">**Note** These examples are not intended for use in all environments.</span></span> <span data-ttu-id="4b0c2-106">Passen Sie die Konfiguration entsprechend Ihrer Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="4b0c2-106">Adjust the configuration according to your environment.</span></span>

 

**<span data-ttu-id="4b0c2-107">So konfigurieren Sie eine typische Domänen Einrichtung in einem beständigen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="4b0c2-107">To configure a typical domain setup in a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="4b0c2-108">Konfigurieren Sie Sysprep für das Basis Bild, um eine eindeutige SID zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b0c2-108">Configure Sysprep on the base image to create a unique SID.</span></span> <span data-ttu-id="4b0c2-109">Weitere Informationen finden Sie unter [Erstellen eines virtuellen PC-Images für MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span><span class="sxs-lookup"><span data-stu-id="4b0c2-109">For more information, see [Creating a Virtual PC Image for MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span></span>

2.  <span data-ttu-id="4b0c2-110">Aktivieren Sie auf der Registerkarte **VM-Setup** das Kontrollkästchen **VM-Setup ausführen** .</span><span class="sxs-lookup"><span data-stu-id="4b0c2-110">On the **VM Setup** tab, select the **Run VM Setup** check box.</span></span>

3.  <span data-ttu-id="4b0c2-111">Konfigurieren Sie im Abschnitt **VM-Computer Namensmuster** das Muster für den Computerabbild Namen.</span><span class="sxs-lookup"><span data-stu-id="4b0c2-111">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="4b0c2-112">Weitere Informationen finden Sie unter [Konfigurieren von Eigenschaften des VM-Computer namens Musters](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="4b0c2-112">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

4.  <span data-ttu-id="4b0c2-113">Klicken Sie auf **Skript-Editor**, und konfigurieren Sie im Dialogfeld **VM-Setup-Skript-Editor** die folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="4b0c2-113">Click **Script Editor**, and in the **VM Setup Script Editor** dialog box, configure the following actions:</span></span>

    1.  **<span data-ttu-id="4b0c2-114">Computer umbenennen</span><span class="sxs-lookup"><span data-stu-id="4b0c2-114">Rename Computer</span></span>**

    2.  **<span data-ttu-id="4b0c2-115">Windows neu starten</span><span class="sxs-lookup"><span data-stu-id="4b0c2-115">Restart Windows</span></span>**

    3.  **<span data-ttu-id="4b0c2-116">Überprüfen der Konnektivität</span><span class="sxs-lookup"><span data-stu-id="4b0c2-116">Check Connectivity</span></span>**

    4.  **<span data-ttu-id="4b0c2-117">Domäne beitreten</span><span class="sxs-lookup"><span data-stu-id="4b0c2-117">Join Domain</span></span>**

    5.  **<span data-ttu-id="4b0c2-118">Deaktivieren der automatischen Anmeldung</span><span class="sxs-lookup"><span data-stu-id="4b0c2-118">Disable Auto-Logon</span></span>**

    <span data-ttu-id="4b0c2-119">Weitere Informationen finden Sie unter [so wird es gemacht: Einrichten von Skriptaktionen](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4b0c2-119">For more information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

5.  <span data-ttu-id="4b0c2-120">Klicken Sie im Menü **Richtlinie** auf **Commit**.</span><span class="sxs-lookup"><span data-stu-id="4b0c2-120">On the **Policy** menu, click **Commit**.</span></span>

**<span data-ttu-id="4b0c2-121">So konfigurieren Sie ein typisches Setup in einem revertible-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="4b0c2-121">To configure a typical setup in a revertible workspace</span></span>**

1.  <span data-ttu-id="4b0c2-122">Aktivieren Sie auf der Registerkarte **VM-Setup** das Kontrollkästchen VM auf der **Grundlage des Computernamens Musters umbenennen** .</span><span class="sxs-lookup"><span data-stu-id="4b0c2-122">On the **VM Setup** tab, select the **Rename the VM based on the computer name pattern** check box.</span></span>

2.  <span data-ttu-id="4b0c2-123">Konfigurieren Sie im Abschnitt **VM-Computer Namensmuster** das Muster für den Computerabbild Namen.</span><span class="sxs-lookup"><span data-stu-id="4b0c2-123">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="4b0c2-124">Weitere Informationen finden Sie unter [Konfigurieren von Eigenschaften des VM-Computer namens Musters](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="4b0c2-124">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

3.  <span data-ttu-id="4b0c2-125">Klicken Sie im Menü **Richtlinie** auf **Commit**.</span><span class="sxs-lookup"><span data-stu-id="4b0c2-125">On the **Policy** menu, click **Commit**.</span></span>

## <span data-ttu-id="4b0c2-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4b0c2-126">Related topics</span></span>


[<span data-ttu-id="4b0c2-127">So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="4b0c2-127">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="4b0c2-128">So konfigurieren Sie die Eigenschaften der Namensmuster virtueller Computer</span><span class="sxs-lookup"><span data-stu-id="4b0c2-128">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[<span data-ttu-id="4b0c2-129">So richten Sie Skriptaktionen ein</span><span class="sxs-lookup"><span data-stu-id="4b0c2-129">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

 

 





