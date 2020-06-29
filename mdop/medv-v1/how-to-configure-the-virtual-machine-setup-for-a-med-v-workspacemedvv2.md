---
title: So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich
description: So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812136"
---
# <span data-ttu-id="cdde5-103">So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="cdde5-103">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>


<span data-ttu-id="cdde5-104">Alle Konfigurationseinstellungen für das virtuelle Computer Setup werden im **Richtlinien** Modul auf der Registerkarte **VM-Setup** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="cdde5-104">All virtual machine setup configuration settings are configured in the **Policy** module, on the **VM Setup** tab.</span></span>

## <span data-ttu-id="cdde5-105">Konfigurieren der Einrichtung eines virtuellen Computers für einen beständigen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="cdde5-105">How to Configure the Virtual Machine Setup for a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="cdde5-106">So konfigurieren Sie die Einrichtung eines virtuellen Computers für einen beständigen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="cdde5-106">To configure the virtual machine setup for a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="cdde5-107">Klicken Sie auf einen persistenten MED-V-Arbeitsbereich, der konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cdde5-107">Click a persistent MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="cdde5-108">Konfigurieren Sie im Abschnitt **persistent VM Setup** die Eigenschaften wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cdde5-108">In the **Persistent VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="cdde5-109">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="cdde5-109">Note</span></span>**  
    <span data-ttu-id="cdde5-110">Die beständigen VM-Setupeigenschaften sind nur für einen beständigen MED-V-Arbeitsbereich aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cdde5-110">The persistent VM setup properties are enabled only for a persistent MED-V workspace.</span></span>



3.  <span data-ttu-id="cdde5-111">Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.</span><span class="sxs-lookup"><span data-stu-id="cdde5-111">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="cdde5-112">Beständige VM-Setup Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cdde5-112">Persistent VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cdde5-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cdde5-113">Property</span></span></th>
<th align="left"><span data-ttu-id="cdde5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdde5-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdde5-115">Ausführen des VM-Setups</span><span class="sxs-lookup"><span data-stu-id="cdde5-115">Run VM Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdde5-116">Aktivieren Sie dieses Kontrollkästchen, um ein Setupskript auszuführen, wenn der MED-V-Arbeitsbereich zum ersten Mal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cdde5-116">Select this check box to run a setup script the first time the MED-V workspace is run.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdde5-117">Skript-Editor</span><span class="sxs-lookup"><span data-stu-id="cdde5-117">Script Editor</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdde5-118">Klicken Sie hier, um das Setupskript zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cdde5-118">Click to configure the setup script.</span></span> <span data-ttu-id="cdde5-119">Weitere Informationen finden Sie unter <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> so wird es gemacht: Einrichten von Skriptaktionen </a> .</span><span class="sxs-lookup"><span data-stu-id="cdde5-119">For more information, see <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)">How to Set Up Script Actions</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cdde5-120">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="cdde5-120">Note</span></span></strong><br/><p><span data-ttu-id="cdde5-121">Diese Schaltfläche ist nur aktiviert <strong> , wenn das VM-Setup Skript ausführen </strong> ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="cdde5-121">This button is enabled only when <strong>Run VM Setup script</strong> is selected.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdde5-122">Meldung, die angezeigt wird, wenn Skript ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="cdde5-122">Message displayed when script is running</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdde5-123">Eine Meldung, die angezeigt werden soll, während das Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cdde5-123">A message to be displayed while the script is running.</span></span> <span data-ttu-id="cdde5-124">Wenn Sie leer bleiben, wird die Standardmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdde5-124">If left blank, the default message is displayed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cdde5-125">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="cdde5-125">Note</span></span></strong><br/><p><span data-ttu-id="cdde5-126">Dieses Feld ist nur aktiviert, wenn das <strong> VM-Setup Skript ausführen aktiviert </strong> ist.</span><span class="sxs-lookup"><span data-stu-id="cdde5-126">This field is enabled only when <strong>Run VM Setup script</strong> is checked.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="cdde5-127">Konfigurieren der Einrichtung eines virtuellen Computers für einen Revertible MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="cdde5-127">How to Configure the Virtual Machine Setup for a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="cdde5-128">So konfigurieren Sie die Einrichtung eines virtuellen Computers für einen revertible MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="cdde5-128">To configure the virtual machine setup for a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="cdde5-129">Klicken Sie auf einen revertible MED-V-Arbeitsbereich, den Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cdde5-129">Click a revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="cdde5-130">Konfigurieren Sie im Abschnitt **Revertible VM Setup** die Eigenschaften wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cdde5-130">In the **Revertible VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="cdde5-131">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="cdde5-131">Note</span></span>**  
    <span data-ttu-id="cdde5-132">Die Setupeigenschaften von revertible VM sind nur für einen revertible MED-V-Arbeitsbereich aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cdde5-132">The revertible VM setup properties are enabled only for a revertible MED-V workspace.</span></span>



3.  <span data-ttu-id="cdde5-133">Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.</span><span class="sxs-lookup"><span data-stu-id="cdde5-133">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="cdde5-134">Revertible-VM-Setup Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cdde5-134">Revertible VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cdde5-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cdde5-135">Property</span></span></th>
<th align="left"><span data-ttu-id="cdde5-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdde5-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdde5-137">Umbenennen des virtuellen Computers basierend auf dem Computernamens Muster</span><span class="sxs-lookup"><span data-stu-id="cdde5-137">Rename the VM based on the computer name pattern</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdde5-138">Aktivieren Sie dieses Kontrollkästchen, um jedem Computer mit dem Med-v-Arbeitsbereich einen eindeutigen Namen zuzuweisen, damit Sie zwischen mehreren Computern unterscheiden können, die denselben Med-v-Arbeitsbereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="cdde5-138">Select this check box to assign a unique name to each computer using the MED-V workspace so that you can differentiate between multiple computers using the same MED-V workspace.</span></span></p>
<p><span data-ttu-id="cdde5-139">Weitere Informationen zum Konfigurieren von Computerabbild Namen finden Sie unter <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> Konfigurieren von VM-Computernamens Mustereigenschaften </a> .</span><span class="sxs-lookup"><span data-stu-id="cdde5-139">For more information on configuring computer image names, see <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)">How to Configure VM Computer Name Pattern Properties</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="cdde5-140">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="cdde5-140">Related topics</span></span>


[<span data-ttu-id="cdde5-141">Über die Benutzeroberfläche der MED-V-Management-Konsole</span><span class="sxs-lookup"><span data-stu-id="cdde5-141">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="cdde5-142">Erstellen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="cdde5-142">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="cdde5-143">Beispiele für VM-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="cdde5-143">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









