---
title: So konfigurieren Sie die Eigenschaften der Namensmuster virtueller Computer
description: So konfigurieren Sie die Eigenschaften der Namensmuster virtueller Computer
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812139"
---
# <span data-ttu-id="9d4a7-103">So konfigurieren Sie die Eigenschaften der Namensmuster virtueller Computer</span><span class="sxs-lookup"><span data-stu-id="9d4a7-103">How to Configure VM Computer Name Pattern Properties</span></span>


<span data-ttu-id="9d4a7-104">Ein Computernamens Muster für virtuelle Computer kann sowohl für revertible als auch für persistente MED-V-Arbeitsbereiche zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-104">A virtual machine computer name pattern can be assigned both for revertible and for persistent MED-V workspaces.</span></span>

-   <span data-ttu-id="9d4a7-105">Revertible – Administratoren können jeder Revertible Med-v Workspace-Instanz einen eindeutigen Namen zuweisen, um zwischen mehreren Computern unterscheiden zu können, die denselben Med-v-Arbeitsbereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-105">Revertible—Administrators can assign a unique name to each revertible MED-V workspace instance to differentiate between multiple computers using the same MED-V workspace.</span></span>

-   <span data-ttu-id="9d4a7-106">Persistent – in einem persistenten MED-V-Arbeitsbereich können Administratoren einen Computer so einrichten, dass er während eines Setupskripts umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-106">Persistent—In a persistent MED-V workspace, administrators can set a computer to be renamed during a setup script.</span></span>

## <span data-ttu-id="9d4a7-107">Zuweisen eines Computername-Musters für einen virtuellen Computer zu einem Revertible MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="9d4a7-107">How to Assign a Virtual Machine Computer Name Pattern to a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="9d4a7-108">So weisen Sie einem revertible MED-V-Arbeitsbereich ein Computernamens Muster eines virtuellen Computers zu</span><span class="sxs-lookup"><span data-stu-id="9d4a7-108">To assign a virtual machine computer name pattern to a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="9d4a7-109">Klicken Sie auf den revertible MED-V-Arbeitsbereich, den Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-109">Click the revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="9d4a7-110">Aktivieren Sie im Abschnitt **Revertible VM Setup** das Kontrollkästchen **VM auf der Grundlage des Computernamens Musters umbenennen** .</span><span class="sxs-lookup"><span data-stu-id="9d4a7-110">In the **Revertible VM Setup** section, select the **Rename the VM based on the computer name pattern** check box.</span></span>

3.  <span data-ttu-id="9d4a7-111">Geben Sie im Abschnitt **VM-Computer Namensmuster** das Muster ein, das für die Benennung von Bildern virtueller Computer verwendet werden soll, und verwenden Sie die folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="9d4a7-111">In the **VM Computer Name Pattern** section, enter the pattern to use for naming virtual machine images, using the following options:</span></span>

    -   <span data-ttu-id="9d4a7-112">**Konstant**– geben Sie freien Text ein, der auf allen Computern mit dem MED-V-Arbeitsbereich konstant ist.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-112">**Constant**—Enter free text that will be constant on all computers using the MED-V workspace.</span></span>

    -   <span data-ttu-id="9d4a7-113">**Variabel**– geben Sie eine Variable ein, indem Sie auf **Variable einfügen**klicken, und wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="9d4a7-113">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="9d4a7-114">Benutzername</span><span class="sxs-lookup"><span data-stu-id="9d4a7-114">User name</span></span>**

        -   **<span data-ttu-id="9d4a7-115">Domänenname</span><span class="sxs-lookup"><span data-stu-id="9d4a7-115">Domain name</span></span>**

        -   **<span data-ttu-id="9d4a7-116">Hostname</span><span class="sxs-lookup"><span data-stu-id="9d4a7-116">Host name</span></span>**

        -   **<span data-ttu-id="9d4a7-117">Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="9d4a7-117">Workspace name</span></span>**

        -   **<span data-ttu-id="9d4a7-118">Name des virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="9d4a7-118">Virtual machine name</span></span>**

        <span data-ttu-id="9d4a7-119">Die ausgewählte Variable ist spezifisch für den Computer, der den MED-V-Arbeitsbereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-119">The variable selected will be specific to the computer using the MED-V workspace.</span></span> <span data-ttu-id="9d4a7-120">Wenn beispielsweise der **Domänenname** ausgewählt ist, enthält der eindeutige Name für jeden Computer den Domänennamen des Computers.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-120">For example, if **Domain name** is selected, the unique name for each computer will include the computer's domain name.</span></span>

    -   <span data-ttu-id="9d4a7-121">**Zufällige Zeichen**: Geben Sie "\ #" für jedes zufällige Zeichen ein, das in das Muster aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-121">**Random characters**—Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="9d4a7-122">Jeder Computer, der den MED-V-Arbeitsbereich verwendet, hat ein Suffix der angegebenen Länge, das willkürlich generiert wird.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-122">Each computer using the MED-V workspace will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="9d4a7-123">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9d4a7-123">Note</span></span>**  
    <span data-ttu-id="9d4a7-124">Der Computername hat eine Grenze von 15 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-124">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="9d4a7-125">Wenn das Muster die Grenze überschreitet, wird es abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-125">If the pattern exceeds the limit, it will be truncated.</span></span>



4.  <span data-ttu-id="9d4a7-126">Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-126">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="9d4a7-127">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9d4a7-127">Note</span></span>**  
    <span data-ttu-id="9d4a7-128">Ein revertible VM-Computernamens Muster kann nur zugewiesen werden, wenn **der VM-Name auf der Grundlage der Computernamens Muster** (im Abschnitt **revertible VM-Setup** ) umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-128">A revertible VM computer name pattern can be assigned only when **Rename the VM based on the computer name patterns** (in the **Revertible VM Setup** section) is checked.</span></span>



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## <span data-ttu-id="9d4a7-129">Zuweisen eines Computer namens Musters für einen virtuellen Computer zu einem persistenten MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="9d4a7-129">How to Assign a Virtual Machine Computer Name Pattern to a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="9d4a7-130">So weisen Sie einem persistenten MED-V-Arbeitsbereich ein Computernamens Muster eines virtuellen Computers zu</span><span class="sxs-lookup"><span data-stu-id="9d4a7-130">To assign a virtual machine computer name pattern to a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="9d4a7-131">Klicken Sie auf den persistenten MED-V-Arbeitsbereich, den Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-131">Click the persistent MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="9d4a7-132">Klicken Sie im Abschnitt **persistent VM Setup** auf **Skript-Editor**.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-132">In the **Persistent VM Setup** section, click **Script Editor**.</span></span>

3.  <span data-ttu-id="9d4a7-133">Klicken Sie im Dialogfeld **Skriptaktionen** auf **Hinzufügen**, und klicken Sie im Untermenü auf **Computer umbenennen**.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-133">In the **Script Actions** dialog box, click **Add**, and on the submenu, click **Rename Computer**.</span></span>

4.  <span data-ttu-id="9d4a7-134">Klicken Sie auf **OK** , um das Dialogfeld **Skriptaktionen** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-134">Click **OK** to close the **Script Actions** dialog box.</span></span>

5.  <span data-ttu-id="9d4a7-135">Geben Sie auf der Registerkarte **VM-Setup** im Abschnitt **VM-Computer Namensmuster** das Muster ein, das zum Umbenennen des Computers verwendet werden soll, indem Sie Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="9d4a7-135">On the **VM Setup** tab, in the **VM Computer Name Pattern** section, enter the pattern to use for renaming the computer, using the following:</span></span>

    -   <span data-ttu-id="9d4a7-136">**Konstant**– geben Sie kostenlosen Text ein, der in den Computernamen aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-136">**Constant**— Enter free text that will be included in the computer name.</span></span>

    -   <span data-ttu-id="9d4a7-137">**Variabel**– geben Sie eine Variable ein, indem Sie auf **Variable einfügen**klicken, und wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="9d4a7-137">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="9d4a7-138">Benutzername</span><span class="sxs-lookup"><span data-stu-id="9d4a7-138">User name</span></span>**

        -   **<span data-ttu-id="9d4a7-139">Domänenname</span><span class="sxs-lookup"><span data-stu-id="9d4a7-139">Domain name</span></span>**

        -   **<span data-ttu-id="9d4a7-140">Hostname</span><span class="sxs-lookup"><span data-stu-id="9d4a7-140">Host name</span></span>**

        -   **<span data-ttu-id="9d4a7-141">Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="9d4a7-141">Workspace name</span></span>**

        -   **<span data-ttu-id="9d4a7-142">Name des virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="9d4a7-142">Virtual machine name</span></span>**

        <span data-ttu-id="9d4a7-143">Die ausgewählte Variable ist spezifisch für den Computer, der umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-143">The variable selected will be specific to the computer that is being renamed.</span></span> <span data-ttu-id="9d4a7-144">Wenn beispielsweise **Domänenname** ausgewählt ist, enthält der Computername den Domänennamen des Computers.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-144">For example, if **Domain name** is selected, the computer name will include the computer's domain name.</span></span>

    -   <span data-ttu-id="9d4a7-145">**Zufällige Zeichen**: Geben Sie "\ #" für jedes zufällige Zeichen ein, das in das Muster aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-145">**Random characters**— Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="9d4a7-146">Auf dem Computer wird ein Suffix der angegebenen Länge angegeben, das nach dem Zufallsprinzip generiert wird.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-146">The computer will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="9d4a7-147">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9d4a7-147">Note</span></span>**  
    <span data-ttu-id="9d4a7-148">Der Computername hat eine Grenze von 15 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-148">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="9d4a7-149">Wenn das Muster die Grenze überschreitet, wird es abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-149">If the pattern exceeds the limit, it will be truncated.</span></span>



6.  <span data-ttu-id="9d4a7-150">Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-150">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="9d4a7-151">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9d4a7-151">Note</span></span>**  
    <span data-ttu-id="9d4a7-152">Der Computer wird nur dann umbenannt, wenn er im Dialogfeld **Skriptaktionen** als Aktion eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="9d4a7-152">The computer will be renamed only if it is set as an action in the **Script Actions** dialog box.</span></span> <span data-ttu-id="9d4a7-153">Ausführliche Informationen finden Sie unter [so wird es gemacht: Einrichten von Skriptaktionen](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9d4a7-153">For detailed information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>



## <span data-ttu-id="9d4a7-154">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9d4a7-154">Related topics</span></span>


[<span data-ttu-id="9d4a7-155">Über die Benutzeroberfläche der MED-V-Management-Konsole</span><span class="sxs-lookup"><span data-stu-id="9d4a7-155">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="9d4a7-156">Erstellen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="9d4a7-156">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="9d4a7-157">So richten Sie Skriptaktionen ein</span><span class="sxs-lookup"><span data-stu-id="9d4a7-157">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

[<span data-ttu-id="9d4a7-158">Beispiele für VM-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="9d4a7-158">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









