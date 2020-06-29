---
title: Übersicht über die Bereitstellung von MED-V 2.0
description: Übersicht über die Bereitstellung von MED-V 2.0
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811557"
---
# <span data-ttu-id="34317-103">Übersicht über die Bereitstellung von MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="34317-103">MED-V 2.0 Deployment Overview</span></span>


<span data-ttu-id="34317-104">Dieser Abschnitt enthält allgemeine Informationen und Anweisungen zum Installieren und Bereitstellen von Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="34317-104">This section provides general information and instructions about how to install and deploy Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="34317-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="34317-105">Overview</span></span>


<span data-ttu-id="34317-106">Med-v 2,0 basiert auf einem Anwendungsmodell, bei dem die gleichen Methoden, die Sie zum Bereitstellen von Anwendungen verwenden, zum Bereitstellen und Verwalten von Med-v verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="34317-106">MED-V 2.0 is based on an application model, where the same methods that you use to deploy applications can be used to deploy and manage MED-V.</span></span> <span data-ttu-id="34317-107">Eine bereitgestellte Med-v-Lösung umfasst zwei Komponenten: den Med-v-Host-Agent und den Gast-Agent.</span><span class="sxs-lookup"><span data-stu-id="34317-107">A deployed MED-V solution includes two components: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="34317-108">Der Med-v-Host-Agent ist auf dem Windows 7-Desktop installiert, und der Med-v-Gast-Agent ist unter Windows XP innerhalb des Med-v-Arbeitsbereichs installiert.</span><span class="sxs-lookup"><span data-stu-id="34317-108">The MED-V Host Agent is installed on the Windows 7 desktop and the MED-V Guest Agent is installed on Windows XP inside the MED-V workspace.</span></span> <span data-ttu-id="34317-109">Med-v enthält auch einen Med-v-Arbeitsbereichs-Packager, der die Informationen und Tools bereitstellt, die für das Erstellen und Konfigurieren von Med-v-Arbeitsbereichen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="34317-109">MED-V also includes a MED-V Workspace Packager that provides the information and tools necessary for creating and configuring MED-V workspaces.</span></span>

**<span data-ttu-id="34317-110">Wichtig</span><span class="sxs-lookup"><span data-stu-id="34317-110">Important</span></span>**  
<span data-ttu-id="34317-111">Med-v unterstützt nur die Installation des Med-v-Arbeitsbereichs Pakets, des Med-v-Host-Agents und des Med-v-Arbeitsbereichs für alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="34317-111">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="34317-112">Wenn Sie Med-v nur für den aktuellen Benutzer installieren, indem Sie **ALLUSERS = ""** auswählen, werden Fehler bei der Installation der Komponenten und beim Einrichten des Med-v-Arbeitsbereichs verursacht.</span><span class="sxs-lookup"><span data-stu-id="34317-112">Installing MED-V for the current user only by selecting **ALLUSERS=””** causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>



### <span data-ttu-id="34317-113">Die MED-V-Installationsdateien</span><span class="sxs-lookup"><span data-stu-id="34317-113">The MED-V Installation Files</span></span>

<span data-ttu-id="34317-114">Med-v umfasst die folgenden Installationsdateien, die für die Ausführung von Med-v erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="34317-114">MED-V includes the following installation files, required for running MED-V:</span></span>

**<span data-ttu-id="34317-115">Die Installationsdatei des MED-V-Host-Agents</span><span class="sxs-lookup"><span data-stu-id="34317-115">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="34317-116">Die Installationsdatei des Host-Agents hat den Namen MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="34317-116">The Host Agent installation file is named MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="34317-117">Diese Datei wird im Rahmen ihrer unternehmensweiten Bereitstellung von MED-V auf jedem relevanten Endbenutzercomputer verteilt und installiert.</span><span class="sxs-lookup"><span data-stu-id="34317-117">This file is distributed and installed on each relevant end-user computer as part of your enterprise-wide deployment of MED-V.</span></span>

**<span data-ttu-id="34317-118">Die Installationsdatei des MED-V-Arbeitsbereichs Pakets</span><span class="sxs-lookup"><span data-stu-id="34317-118">The MED-V Workspace Packager Installation File</span></span>**

<span data-ttu-id="34317-119">Die Installationsdatei des MED-V-Arbeitsbereichs-Packagers hat den Namen MED-V\_WorkspacePackager\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="34317-119">The MED-V Workspace Packager installation file is named MED-V\_WorkspacePackager\_Setup.exe.</span></span> <span data-ttu-id="34317-120">Verwenden Sie diese Datei, um den MED-V Workspace-Paketer auf einem Computer zu installieren, auf dem Sie über Administratorrechte und-Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="34317-120">Use this file to install the MED-V Workspace Packager on a computer where you have administrator rights and permissions.</span></span> <span data-ttu-id="34317-121">Der Desktopadministrator verwendet den Med-v Workspace-Paketer zum Erstellen und Verwalten von Med-v-Arbeitsbereichen.</span><span class="sxs-lookup"><span data-stu-id="34317-121">The desktop administrator uses the MED-V Workspace Packager to create and manage MED-V workspaces.</span></span>

**<span data-ttu-id="34317-122">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="34317-122">Note</span></span>**  
<span data-ttu-id="34317-123">Der MED-V-Gast-Agent wird während der erstmaligen Einrichtung automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="34317-123">The MED-V Guest Agent is installed automatically during first time setup.</span></span>



### <span data-ttu-id="34317-124">Der MED-V-Bereitstellungsprozess</span><span class="sxs-lookup"><span data-stu-id="34317-124">The MED-V Deployment Process</span></span>

<span data-ttu-id="34317-125">Im folgenden wird eine allgemeine Übersicht über den MED-V-Installations-und Bereitstellungsprozess beschrieben:</span><span class="sxs-lookup"><span data-stu-id="34317-125">The following is a high-level overview of the MED-V installation and deployment process:</span></span>

1.  <span data-ttu-id="34317-126">Installieren Sie den Med-v Workspace-Paketer auf dem Computer, auf dem Sie über administrative Anmeldeinformationen verfügen und die Sie zum Erstellen der Med-v-Arbeitsbereichs Pakete verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="34317-126">Install the MED-V Workspace Packager on the computer where you have administrative credentials and that you will be using to build the MED-V workspace packages.</span></span> <span data-ttu-id="34317-127">Weitere Informationen finden Sie unter [so wird es gemacht: Installieren des MED-V-Arbeitsbereichs Pakets](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="34317-127">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

2.  <span data-ttu-id="34317-128">Bereiten Sie Ihr Med-v-Abbild vor, und erstellen Sie Ihre Med-v-Arbeitsbereichs Pakete mithilfe des Med-v-Arbeitsbereichs-Packagers.</span><span class="sxs-lookup"><span data-stu-id="34317-128">Prepare your MED-V image and create your MED-V workspace packages by using the MED-V Workspace Packager.</span></span> <span data-ttu-id="34317-129">Weitere Informationen finden Sie unter [Operationen für MED-V](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="34317-129">For more information, see [Operations for MED-V](operations-for-med-v.md).</span></span>

3.  <span data-ttu-id="34317-130">Stellen Sie die erforderlichen MED-V-Komponenten im gesamten Unternehmen bereit.</span><span class="sxs-lookup"><span data-stu-id="34317-130">Deploy the required MED-V components throughout your enterprise.</span></span> <span data-ttu-id="34317-131">Die erforderlichen Komponenten von Med-v sind Windows Virtual PC, der Med-v-Host-Agent und der Med-v-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="34317-131">The required components of MED-V are Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span>

**<span data-ttu-id="34317-132">Wichtig</span><span class="sxs-lookup"><span data-stu-id="34317-132">Important</span></span>**  
<span data-ttu-id="34317-133">Für die Installation der MED-V-Komponenten sind Administratoranmeldeinformationen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="34317-133">Installation of the MED-V components requires administrative credentials.</span></span> <span data-ttu-id="34317-134">Wenn ein Endbenutzer MED-V installiert, werden Sie aufgefordert, administrative Anmeldeinformationen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="34317-134">If an end user is installing MED-V, they are prompted to enter administrative credentials.</span></span> <span data-ttu-id="34317-135">Alternativ können Administratoranmeldeinformationen im Kontext bereitgestellt werden, wenn Sie mit einem ESD-System (Electronic Software Distribution) installieren.</span><span class="sxs-lookup"><span data-stu-id="34317-135">Alternately, administrative credentials can be provided in context if you are installing by using an electronic software distribution (ESD) system.</span></span>



### <span data-ttu-id="34317-136">Die MED-V-Komponenten</span><span class="sxs-lookup"><span data-stu-id="34317-136">The MED-V Components</span></span>

<span data-ttu-id="34317-137">Die MED-V-Komponenten, die Sie im gesamten Unternehmen bereitstellen, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="34317-137">The MED-V components that you deploy throughout your enterprise consist of the following:</span></span>

**<span data-ttu-id="34317-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="34317-138">Windows Virtual PC</span></span>**

<span data-ttu-id="34317-139">MED-V-Funktionen in Windows Virtual PC-Bildern für Ihre kompatibilitätslösung.</span><span class="sxs-lookup"><span data-stu-id="34317-139">MED-V functions inside Windows Virtual PC images for its compatibility solution.</span></span> <span data-ttu-id="34317-140">Windows Virtual PC und das Update für Windows 7 (KB977206) sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="34317-140">Windows Virtual PC and the update for Windows 7 (KB977206) are required.</span></span> <span data-ttu-id="34317-141">Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.</span><span class="sxs-lookup"><span data-stu-id="34317-141">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

**<span data-ttu-id="34317-142">Die Installationsdatei des MED-V-Host-Agents</span><span class="sxs-lookup"><span data-stu-id="34317-142">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="34317-143">MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="34317-143">MED-V\_HostAgent\_Setup.exe.</span></span>

**<span data-ttu-id="34317-144">Die Installationsdateien für den MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="34317-144">The MED-V Workspace Installation Files</span></span>**

<span data-ttu-id="34317-145">Die Installationsdateien für den Med-v-Arbeitsbereich werden erstellt, wenn Sie Ihr Med-v-Arbeitsbereichs Paket erstellen, das Folgendes umfasst:</span><span class="sxs-lookup"><span data-stu-id="34317-145">The MED-V workspace installation files are created when you build your MED-V workspace package that consists of the following:</span></span>

<span data-ttu-id="34317-146">Ein setup.exe ausführbares Programm, das die Installation des MED-V-Arbeitsbereichs ausführt</span><span class="sxs-lookup"><span data-stu-id="34317-146">A setup.exe executable program that executes the MED-V workspace installation</span></span>

<span data-ttu-id="34317-147">Ein &lt; MED-V \ _workspace \ _name &gt; . MSI-Installationsprogramm</span><span class="sxs-lookup"><span data-stu-id="34317-147">A &lt;MED-V\_workspace\_name&gt;.msi installer</span></span>

<span data-ttu-id="34317-148">Eine &lt; VHD \ _FileName &gt; . medv-Datei, bei der es sich um die komprimierte virtuelle Festplatte handelt</span><span class="sxs-lookup"><span data-stu-id="34317-148">A &lt;VHD\_filename&gt;.medv file, which is the compressed virtual hard disk</span></span>

<span data-ttu-id="34317-149">Die Dateien für Konfigurationseinstellungen ( &lt; Arbeitsbereich \ _name &gt; . reg und &lt; Arbeitsbereich \ _name &gt; . ps1)</span><span class="sxs-lookup"><span data-stu-id="34317-149">The files for configuration settings (&lt;workspace\_name&gt;.reg and &lt;workspace\_name&gt;.ps1)</span></span>

<span data-ttu-id="34317-150">Zum Bereitstellen von MED-V kopieren Sie alle erforderlichen Installationsdateien auf den Hostcomputer oder auf eine Freigabe, auf die der Hostcomputer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="34317-150">To deploy MED-V, copy all the required installation files to the host computer or to a share that can be accessed by the host computer.</span></span> <span data-ttu-id="34317-151">Führen Sie die Komponenten Installationsdateien für Windows Virtual PC, den Med-v-Host-Agent und den Med-v-Arbeitsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="34317-151">Run the component installation files for Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span> <span data-ttu-id="34317-152">Starten Sie dann den Med-v-Host-Agent, um die erstmalige Einrichtung von Med-v abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="34317-152">Then start the MED-V Host Agent to complete the first time setup of MED-V.</span></span>

<span data-ttu-id="34317-153">Sie können die Installation manuell durchführen.</span><span class="sxs-lookup"><span data-stu-id="34317-153">You can perform the installation manually.</span></span> <span data-ttu-id="34317-154">Wir empfehlen jedoch, dass Sie eine elektronische Softwareverteilungsmethode verwenden, um die Bereitstellung der Komponenten zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="34317-154">However, we recommend that you use an electronic software distribution method to automate the deployment of the components.</span></span> <span data-ttu-id="34317-155">Weitere Informationen finden Sie unter [Bereitstellen eines MED-V-Arbeitsbereichs über ein elektronisches Software Verteilungs System](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="34317-155">For more information, see [How to Deploy a MED-V Workspace Through an Electronic Software Distribution System](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span></span>

**<span data-ttu-id="34317-156">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="34317-156">Note</span></span>**  
<span data-ttu-id="34317-157">Informationen zu den verfügbaren Befehlszeilenargumenten, um die Installationsoptionen zu steuern, finden Sie unter [Befehlszeilenoptionen für MED-V-Installationsdateien](command-line-options-for-med-v-installation-files.md).</span><span class="sxs-lookup"><span data-stu-id="34317-157">For information about available command-line arguments to control install options, see [Command-Line Options for MED-V Installation Files](command-line-options-for-med-v-installation-files.md).</span></span>



## <span data-ttu-id="34317-158">Bereitstellungsschritte</span><span class="sxs-lookup"><span data-stu-id="34317-158">Deployment Steps</span></span>


<span data-ttu-id="34317-159">Wenn Sie MED-V im gesamten Unternehmen bereitstellen, gibt es zwei Hauptaspekte: Installation und Erstmaliges Einrichten.</span><span class="sxs-lookup"><span data-stu-id="34317-159">When you deploy MED-V throughout your enterprise, there are two main considerations: installation and first time setup.</span></span>

### <span data-ttu-id="34317-160">Installation</span><span class="sxs-lookup"><span data-stu-id="34317-160">Installation</span></span>

1.  <span data-ttu-id="34317-161">**Windows Virtual PC** – während der Installation überprüft MED-V für Windows Virtual PC und das erforderliche Update für Windows 7 (KB977206).</span><span class="sxs-lookup"><span data-stu-id="34317-161">**Windows Virtual PC** - During installation, MED-V checks for Windows Virtual PC and its required update for Windows 7 (KB977206).</span></span> <span data-ttu-id="34317-162">Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.</span><span class="sxs-lookup"><span data-stu-id="34317-162">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    <span data-ttu-id="34317-163">Sie können diese als Teil der Windows 7-Installationen installieren, bevor Sie Med-v installieren, oder Sie können Sie als Teil der Med-v-Verteilung installieren.</span><span class="sxs-lookup"><span data-stu-id="34317-163">You can install these as part of the Windows 7 installations before you install MED-V, or you can install them as part of the MED-V distribution.</span></span> <span data-ttu-id="34317-164">MED-V enthält jedoch keinen Mechanismus für die Bereitstellung; Sie müssen mithilfe eines ESD-Systems (Electronic Software Distribution) oder als Teil des Windows 7-Images bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="34317-164">However, MED-V does not include a mechanism for their deployment; they must be deployed by using an electronic software distribution (ESD) system or as part of the Windows 7 image.</span></span>

    **<span data-ttu-id="34317-165">Wichtig</span><span class="sxs-lookup"><span data-stu-id="34317-165">Important</span></span>**  
    <span data-ttu-id="34317-166">Wenn Sie die Med-v-Komponenten mithilfe einer Batchdatei installieren, empfiehlt es sich, festzulegen, dass Windows Virtual PC und der Windows Virtual PC-Hotfix nach dem Med-v-Host-Agent und den Med-v-Arbeitsbereichs Paketdateien installiert werden.</span><span class="sxs-lookup"><span data-stu-id="34317-166">When you install the MED-V components by using a batch file, a best practice is to specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="34317-167">Dies bedeutet, dass Windows Update keinen Eingriff in den Installationsvorgang verursacht, da ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="34317-167">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. <span data-ttu-id="34317-168">**Med-v-Host-Agent** – installieren Sie den Med-v-Host-Agent auf dem Windows 7-Computer, auf dem Med-v ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34317-168">**MED-V Host Agent** – Install the MED-V Host Agent on the Windows 7 computer where MED-V will be run.</span></span> <span data-ttu-id="34317-169">Diese muss vor der Installation des MED-V-Arbeitsbereichs installiert werden, und es wird überprüft, ob Windows Virtual PC installiert ist.</span><span class="sxs-lookup"><span data-stu-id="34317-169">This must be installed before installing the MED-V workspace and checks to make sure that Windows Virtual PC is installed.</span></span>

3. <span data-ttu-id="34317-170">**Med-v Workspace** – Sie erstellen die Dateien, die in dieser Installation erforderlich sind, mithilfe des Med-v-Arbeitsbereichs Pakets: die setup.exe-, medv-und MSI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="34317-170">**MED-V workspace** – You create the files that are required in this installation by using the MED-V Workspace Packager: the setup.exe, .medv, and .msi files.</span></span> <span data-ttu-id="34317-171">Führen Sie setup.exe aus, um den MED-V-Arbeitsbereich zu installieren. Dadurch werden die anderen Dateien nach Bedarf ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="34317-171">To install the MED-V workspace, run setup.exe; this triggers the other files as required.</span></span> <span data-ttu-id="34317-172">Die Installation platziert einen Eintrag in der Registrierung unter dem Schlüssel "lokaler Computer ausführen", um den Med-v-Host-Agent zu starten, der immer Med-v ausführt, wenn Windows gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="34317-172">The installation places an entry in the registry under the local machine run key to start the MED-V Host Agent, which always runs MED-V when Windows is started.</span></span>

   **<span data-ttu-id="34317-173">Wichtig</span><span class="sxs-lookup"><span data-stu-id="34317-173">Important</span></span>**  
   <span data-ttu-id="34317-174">Die Installation des MED-V-Arbeitsbereichs kann vom Endbenutzer interaktiv oder lautlos über ein elektronisches Softwareverteilungssystem ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34317-174">The installation of the MED-V workspace can be run interactively by the end user or silently through an electronic software distribution system.</span></span> <span data-ttu-id="34317-175">Die Installation des Med-v-Arbeitsbereichs erfordert administrative Anmeldeinformationen, sodass Endbenutzer Administratoren Ihrer Computer sein müssen, um den Med-v-Arbeitsbereich zu installieren.</span><span class="sxs-lookup"><span data-stu-id="34317-175">Installation of the MED-V workspace requires administrative credentials, so end users must be administrators of their computers to install the MED-V workspace.</span></span> <span data-ttu-id="34317-176">Alternativ wird ein elektronisches Softwareverteilungssystem in der Regel im Systemkontext ausgeführt und verfügt über ausreichende Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="34317-176">Alternately, an electronic software distribution system typically runs in the system context and has sufficient permissions.</span></span>



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### <span data-ttu-id="34317-177">Erstmaliges Einrichten</span><span class="sxs-lookup"><span data-stu-id="34317-177">First Time Setup</span></span>

<span data-ttu-id="34317-178">Nachdem Med-v und die erforderlichen Komponenten installiert sind, muss Med-v konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="34317-178">After MED-V and its required components are installed, MED-V must be configured.</span></span> <span data-ttu-id="34317-179">Die Konfiguration von MED-V wird als Erstmaliges Einrichten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="34317-179">The configuration of MED-V is known as first time setup.</span></span> <span data-ttu-id="34317-180">Mithilfe des **MED-V-Arbeitsbereichs Pakets**können Sie die erstmalige Einrichtung so konfigurieren, dass Sie automatisch oder interaktiv ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34317-180">By using the **MED-V Workspace Packager**, you can configure first time setup to run silently or interactively.</span></span> <span data-ttu-id="34317-181">Bei der erstmaligen Einrichtung von Med-v müssen Endbenutzer Ihr Kennwort eingeben, um sich bei dem Med-v-Arbeitsbereich zu authentifizieren, aber ansonsten kann der Benutzer fast unsichtbar sein.</span><span class="sxs-lookup"><span data-stu-id="34317-181">First time setup of MED-V requires end users to enter their password to authenticate to the MED-V workspace, but otherwise can be almost invisible to the user.</span></span> <span data-ttu-id="34317-182">Benachrichtigungen werden im Infobereich angezeigt, beispielsweise wenn die erstmalige Einrichtung abgeschlossen ist und Anwendungen bereit sind.</span><span class="sxs-lookup"><span data-stu-id="34317-182">Notifications are shown in the notification area, such as when first time setup is complete and applications are ready.</span></span> <span data-ttu-id="34317-183">Im folgenden finden Sie die Aktionen, die bei der erstmaligen Einrichtung von MED-V auftreten:</span><span class="sxs-lookup"><span data-stu-id="34317-183">The following are the actions that occur during first time setup of MED-V:</span></span>

1.  <span data-ttu-id="34317-184">Die virtuelle Festplatte muss konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="34317-184">The virtual hard disk must be configured.</span></span> <span data-ttu-id="34317-185">Das Mini Setup wird ausgeführt und erweitert das Windows XP-Abbild.</span><span class="sxs-lookup"><span data-stu-id="34317-185">Mini-Setup runs and expands the Windows XP image.</span></span> <span data-ttu-id="34317-186">In der Regel tritt dies in einem ausgeblendeten Fenster auf, aber MED-V kann für die Anzeige während dieser Konfiguration konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="34317-186">Typically, this occurs in a hidden window, but MED-V can be configured to display during this configuration.</span></span>

2.  <span data-ttu-id="34317-187">Nach Abschluss der Mini Installation können Sie Befehle ausführen, die für eine zusätzliche Konfiguration erforderlich sind, beispielsweise die Installation von ESD-Software oder anderen Anwendungen oder das Konfigurieren des Bilds.</span><span class="sxs-lookup"><span data-stu-id="34317-187">After Mini-Setup finishes, you can run commands that you must have for additional configuration, such as installing ESD software or other applications, or configuring the image.</span></span> <span data-ttu-id="34317-188">Diese können in der Datei "Sysprep. inf" aufgerufen werden, sind dort aber nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="34317-188">These can be called in the Sysprep.inf file, but are not required there.</span></span> <span data-ttu-id="34317-189">Weitere Informationen finden Sie unter [Konfigurieren eines Windows Virtual PC-Images für MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="34317-189">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

3.  <span data-ttu-id="34317-190">Ftscompletion.exe wird als letzter Schritt in der Konfiguration ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34317-190">Ftscompletion.exe is run as the last step in configuration.</span></span> <span data-ttu-id="34317-191">Dieser Vorgang schließt die Med-v-Konfiguration ab, fügt den Benutzer der RDP-Gruppe hinzu, um den Zugriff auf den Med-v-Arbeitsbereich zu ermöglichen, Protokolle zu kopieren, signalisiert Med-v, dass der Med-v-Arbeitsbereich bereit ist, und startet dann den Med-v-Arbeitsbereich neu.</span><span class="sxs-lookup"><span data-stu-id="34317-191">This process completes the MED-V configuration, adds the user to the RDP group to let them access the MED-V workspace, copies logs, signals MED-V that the MED-V workspace is ready, and then restarts the MED-V workspace.</span></span> <span data-ttu-id="34317-192">Durch diesen Vorgang kann der Benutzer auch als Administrator des Med-v-Arbeitsbereichs hinzugefügt werden, wenn dieser beim Erstellen des Med-v-Arbeitsbereichs konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="34317-192">This process can also add the user as an administrator of the MED-V workspace if this was configured when the MED-V workspace was created.</span></span> <span data-ttu-id="34317-193">Ftscompletion.exe wird in der Regel über die Sysprep-, INF-Datei aufgerufen, kann aber auch über eine andere Methode wie ein Skript ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34317-193">Ftscompletion.exe is typically called through the Sysprep,inf file but can also be run through another method, such as a script.</span></span> <span data-ttu-id="34317-194">Ftscompletion.exe muss jedoch die letzte Aktion sein, die ausgeführt wird, wenn die Workstation konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="34317-194">However, Ftscompletion.exe must be the last action that is performed when the workstation is configured.</span></span> <span data-ttu-id="34317-195">Weitere Informationen finden Sie unter [Konfigurieren eines Windows Virtual PC-Images für MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="34317-195">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

4.  <span data-ttu-id="34317-196">Nachdem der MED-V-Arbeitsbereich durch Ftscompletion.exe neu gestartet wurde, ist der Endbenutzer angemeldet.</span><span class="sxs-lookup"><span data-stu-id="34317-196">After the MED-V workspace is restarted by Ftscompletion.exe, the end user is logged on.</span></span> <span data-ttu-id="34317-197">Wenn Sie Ihr Kennwort bei der erstmaligen Einrichtung nicht gespeichert haben, werden Sie erneut dazu aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="34317-197">If they did not save their password during first time setup, they are prompted for it again.</span></span> <span data-ttu-id="34317-198">Der MED-V-Arbeitsbereich wird dann gestartet und für den Benutzer konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="34317-198">The MED-V workspace is then started and configured for the user.</span></span> <span data-ttu-id="34317-199">Die Konfiguration umfasst das Anwenden von Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="34317-199">Configuration includes applying Group Policy.</span></span>

    <span data-ttu-id="34317-200">Es wird empfohlen, nur die Richtlinien anzuwenden, die in einer Anwendungs Kompatibilitätsumgebung für Windows XP sinnvoll sind.</span><span class="sxs-lookup"><span data-stu-id="34317-200">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="34317-201">Beispielsweise müssen Desktop Personalisierungsrichtlinien normalerweise nicht angewendet werden und sollten deaktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="34317-201">For example, desktop personalization policies do not typically need to be applied and should be disabled.</span></span> <span data-ttu-id="34317-202">Weitere Informationen zum Zulassen nur lokaler Profile finden Sie unter [Gruppenrichtlinieneinstellungen für Roaming-Benutzerprofile](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="34317-202">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

<span data-ttu-id="34317-203">Nach Abschluss der erstmaligen Einrichtung wird der Endbenutzer benachrichtigt, dass die veröffentlichten Anwendungen bereit sind.</span><span class="sxs-lookup"><span data-stu-id="34317-203">After first time setup is complete, the end user is notified that the published applications are ready.</span></span> <span data-ttu-id="34317-204">Sie können dann über das **Startmenü** auf die im MED-V-Arbeitsbereich installierten Anwendungen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="34317-204">They are then able to access the applications installed in the MED-V workspace from their **Start** menu.</span></span>

## <span data-ttu-id="34317-205">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="34317-205">Related topics</span></span>


[<span data-ttu-id="34317-206">Vorbereiten der Bereitstellungsumgebung für MED-V</span><span class="sxs-lookup"><span data-stu-id="34317-206">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

[<span data-ttu-id="34317-207">Bereitstellung von MED-V</span><span class="sxs-lookup"><span data-stu-id="34317-207">Deployment of MED-V</span></span>](deployment-of-med-v.md)









