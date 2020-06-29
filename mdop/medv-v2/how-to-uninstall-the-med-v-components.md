---
title: So deinstallieren Sie die MED-V-Komponenten
description: So deinstallieren Sie die MED-V-Komponenten
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804670"
---
# <span data-ttu-id="ecd66-103">So deinstallieren Sie die MED-V-Komponenten</span><span class="sxs-lookup"><span data-stu-id="ecd66-103">How to Uninstall the MED-V Components</span></span>


<span data-ttu-id="ecd66-104">Unter bestimmten Umständen möchten Sie möglicherweise die Microsoft Enterprise Desktop Virtualization (MED-V) 2,0-Komponenten in Ihrem Unternehmen ganz oder teilweise deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="ecd66-104">Under certain circumstances, you might want to uninstall all or part of the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components from your enterprise.</span></span> <span data-ttu-id="ecd66-105">Sie haben beispielsweise alle Kompatibilitätsprobleme des Anwendungs Betriebssystems behoben, oder Sie möchten einen anderen MED-V-Arbeitsbereich in Ihrem Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ecd66-105">For example, you have resolved all application operating system compatibility issues, or you want to deploy a different MED-V workspace in your enterprise.</span></span>

<span data-ttu-id="ecd66-106">In der Regel können Sie Ihr ESD-System (Electronic Software Distribution) so konfigurieren, dass die MED-V-Komponenten mithilfe eines Windows-basierten Installationsprogramms deinstalliert werden.</span><span class="sxs-lookup"><span data-stu-id="ecd66-106">Typically, you can configure your electronic software distribution (ESD) system to uninstall the MED-V components by using a Windows-based Installer.</span></span> <span data-ttu-id="ecd66-107">Alternativ können Sie alle oder einige MED-V-Komponenten manuell deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="ecd66-107">Alternately, you can uninstall all or some MED-V components manually.</span></span>

<span data-ttu-id="ecd66-108">**Wichtig**  Bevor Sie den Med-v-Host-Agent deinstallieren können, müssen Sie zunächst alle installierten Med-v-Arbeitsbereiche deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="ecd66-108">**Important** Before you can uninstall the MED-V Host Agent, you must first uninstall any installed MED-V workspace.</span></span>

 

<span data-ttu-id="ecd66-109">Führen Sie die folgenden Verfahren aus, um die MED-V-Komponenten aus Ihrem Unternehmen zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="ecd66-109">Use the following procedures to uninstall the MED-V components from your enterprise.</span></span>

**<span data-ttu-id="ecd66-110">So deinstallieren Sie MED-V mithilfe eines elektronischen Softwareverteilungssystems</span><span class="sxs-lookup"><span data-stu-id="ecd66-110">To uninstall MED-V using an electronic software distribution System</span></span>**

1.  <span data-ttu-id="ecd66-111">Verwenden Sie Ihr ESD-System, um ein Skript zu verteilen, das das uninstall.exe ausführbare Programm für jeden MED-V-Arbeitsbereich aufruft, den Sie deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ecd66-111">Use your ESD system to distribute a script that invokes the uninstall.exe executable program for every MED-V workspace that you want to uninstall.</span></span> <span data-ttu-id="ecd66-112">Die Datei befindet sich unter C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="ecd66-112">The file is located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span> <span data-ttu-id="ecd66-113">Sie können ein Flag so einrichten, dass das Programm zum Deinstallieren der ausführbaren Datei automatisch ausgeführt wird, damit Endbenutzer die Deinstallation nicht kennen.</span><span class="sxs-lookup"><span data-stu-id="ecd66-113">You can set a flag to run the uninstall executable program silently so that end users are unaware of the uninstallation.</span></span>

2.  <span data-ttu-id="ecd66-114">Erstellen Sie ein Paket, um die Installationsdatei des Med-v-Host-Agents auf jedem Computer zu verteilen, auf dem ein Med-v-Arbeitsbereich deinstalliert wurde.</span><span class="sxs-lookup"><span data-stu-id="ecd66-114">Create a package to distribute the MED-V Host Agent installation file to each computer on which a MED-V workspace was uninstalled.</span></span> <span data-ttu-id="ecd66-115">Konfigurieren Sie das Paket so, dass die Deinstallation im unbeaufsichtigten Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecd66-115">Configure the package to run the uninstallation in silent mode.</span></span>

<span data-ttu-id="ecd66-116">Der ESD-Client erkennt, wann die neuen Pakete verfügbar sind, und beginnt, die Pakete pro Definition und Anforderungen zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="ecd66-116">The ESD client recognizes when the new packages are available and starts to uninstall the packages per the definition and requirements.</span></span>

**<span data-ttu-id="ecd66-117">So deinstallieren Sie einen MED-V-Arbeitsbereich manuell</span><span class="sxs-lookup"><span data-stu-id="ecd66-117">To manually uninstall a MED-V workspace</span></span>**

1.  <span data-ttu-id="ecd66-118">Klicken Sie auf dem Hostcomputer auf **Start**, klicken Sie auf **System**Steuerung, und klicken Sie dann auf **Programme und Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="ecd66-118">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="ecd66-119">Wählen Sie im Fenster **Programme und Funktionen** den MED-V-Arbeitsbereich aus, den Sie entfernen möchten, und klicken Sie dann auf **deinstallieren**.</span><span class="sxs-lookup"><span data-stu-id="ecd66-119">In the **Programs and Features** window, select the MED-V workspace that you want to remove, and then click **Uninstall**.</span></span> <span data-ttu-id="ecd66-120">(Der Med-v Workspace hat den Namen "Med-v Workspace- &lt; *Arbeitsbereich \ _name* &gt; ").</span><span class="sxs-lookup"><span data-stu-id="ecd66-120">(The MED-V workspace is named "MED-V Workspace - &lt;*workspace\_name*&gt;").</span></span> <span data-ttu-id="ecd66-121">Der &lt; *Arbeitsbereich \ _name* &gt; **Setup-Assistent** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ecd66-121">The &lt;*workspace\_name*&gt; **Setup Wizard** opens.</span></span>

3.  <span data-ttu-id="ecd66-122">Klicken Sie im **Setup-Assistenten**auf **weiter**, und klicken Sie dann auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="ecd66-122">On the **Setup Wizard**, click **Next**, and then click **Remove**.</span></span>

4.  <span data-ttu-id="ecd66-123">Wenn Sie dies bevorzugen, aktivieren Sie das Kontrollkästchen, um den von MED-V erstellten Master-VHD-Datenträger und die differenzierenden Datenträger zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ecd66-123">If you prefer, select the check box to delete the master VHD disk and differencing disks created by MED-V.</span></span> <span data-ttu-id="ecd66-124">Dies ist nicht erforderlich, gibt aber Speicherplatz frei, nachdem die Deinstallation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ecd66-124">This is not required, but frees disk space after the uninstallation finishes.</span></span>

5.  <span data-ttu-id="ecd66-125">Klicken Sie auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="ecd66-125">Click **Remove**.</span></span>

    <span data-ttu-id="ecd66-126">**Hinweis**  Wenn MED-V zurzeit ausgeführt wird, wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob Sie es beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="ecd66-126">**Note** If MED-V is currently running, a dialog box appears and prompts you whether you want to shut it down.</span></span> <span data-ttu-id="ecd66-127">Klicken Sie auf **Ja** , um die Deinstallation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="ecd66-127">Click **Yes** to continue with the uninstallation.</span></span> <span data-ttu-id="ecd66-128">Klicken Sie auf **Nein** , um die Deinstallation abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="ecd66-128">Click **No** to cancel the uninstallation.</span></span>

     

<span data-ttu-id="ecd66-129">Alternativ können Sie einen MED-V-Arbeitsbereich entfernen, indem Sie die `uninstall.exe` Datei ausführen, die sich normalerweise unter C:\\ProgramData\\Microsoft\\Medv\\Workspace. befindet.</span><span class="sxs-lookup"><span data-stu-id="ecd66-129">Alternately, you can remove a MED-V workspace by running the `uninstall.exe` file, typically located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span>

**<span data-ttu-id="ecd66-130">So deinstallieren Sie den MED-V-Host-Agent manuell</span><span class="sxs-lookup"><span data-stu-id="ecd66-130">To manually uninstall the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="ecd66-131">Klicken Sie auf dem Windows 7-Hostcomputer auf **Start**, klicken Sie auf **System**Steuerung, und klicken Sie dann auf **Programme und Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="ecd66-131">On the Windows 7 host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="ecd66-132">Wählen Sie im Fenster **Programme und Funktionen** den **MED-V-Host-Agent**aus, und klicken Sie dann auf **deinstallieren**.</span><span class="sxs-lookup"><span data-stu-id="ecd66-132">In the **Programs and Features** window, select **MED-V Host Agent**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="ecd66-133">Der Windows Installer entfernt den MED-V-Host-Agent.</span><span class="sxs-lookup"><span data-stu-id="ecd66-133">The Windows Installer removes the MED-V Host Agent.</span></span>

    <span data-ttu-id="ecd66-134">**Hinweis**  Wenn Sie versuchen, den Med-v-Host-Agent zu deinstallieren, bevor Sie den Med-v-Arbeitsbereich deinstallieren, wird ein Dialogfeld angezeigt, das besagt, dass Sie zuerst den Med-v-Arbeitsbereich deinstallieren müssen.</span><span class="sxs-lookup"><span data-stu-id="ecd66-134">**Note** If you try to uninstall the MED-V Host Agent before you uninstall the MED-V workspace, a dialog box appears that states that you must first uninstall the MED-V workspace.</span></span> <span data-ttu-id="ecd66-135">Klicken Sie auf **OK**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="ecd66-135">Click **OK** to continue.</span></span>

     

**<span data-ttu-id="ecd66-136">So deinstallieren Sie den MED-V Workspace-Paketer manuell</span><span class="sxs-lookup"><span data-stu-id="ecd66-136">To manually uninstall the MED-V Workspace Packager</span></span>**

1.  <span data-ttu-id="ecd66-137">Klicken Sie auf dem Hostcomputer auf **Start**, klicken Sie auf **System**Steuerung, und klicken Sie dann auf **Programme und Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="ecd66-137">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="ecd66-138">Wählen Sie im Fenster **Programme und Features** den Eintrag **MED-V Workspace Packager**aus, und klicken Sie dann auf **deinstallieren**.</span><span class="sxs-lookup"><span data-stu-id="ecd66-138">In the **Programs and Features** window, select **MED-V Workspace Packager**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="ecd66-139">Der Windows Installer entfernt den MED-V Workspace-Paketer.</span><span class="sxs-lookup"><span data-stu-id="ecd66-139">The Windows Installer removes the MED-V Workspace Packager.</span></span>

    <span data-ttu-id="ecd66-140">**Hinweis**  Sie können den Med-v-Arbeitsbereichs-Packager jederzeit deinstallieren, ohne die bereitgestellten Med-v-Arbeitsbereiche zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="ecd66-140">**Note** You can uninstall the MED-V Workspace Packager at any time without affecting any deployed MED-V workspaces.</span></span>

     

## <span data-ttu-id="ecd66-141">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ecd66-141">Related topics</span></span>


[<span data-ttu-id="ecd66-142">Bereitstellen der MED-V-Komponenten</span><span class="sxs-lookup"><span data-stu-id="ecd66-142">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

 

 





