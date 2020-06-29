---
title: So stellen Sie die MED-V-Komponenten über ein elektronisches Softwareverteilungssystem bereit
description: So stellen Sie die MED-V-Komponenten über ein elektronisches Softwareverteilungssystem bereit
author: dansimp
ms.assetid: 8a800bdf-6fa4-47b4-b417-df053289d4e8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d772702c770340796fe770273146bd0308617a69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810804"
---
# <span data-ttu-id="7770a-103">So stellen Sie die MED-V-Komponenten über ein elektronisches Softwareverteilungssystem bereit</span><span class="sxs-lookup"><span data-stu-id="7770a-103">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>


<span data-ttu-id="7770a-104">Ein elektronisches Softwareverteilungssystem kann Ihnen helfen, Software effizient auf viele Computer über langsame oder schnelle Netzwerkverbindungen zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="7770a-104">An electronic software distribution system can help you efficiently move software to many computers over slow or fast network connections.</span></span> <span data-ttu-id="7770a-105">Der folgende Abschnitt enthält Informationen und Anweisungen, wie Sie die Microsoft Enterprise Desktop Virtualization (MED-V) 2,0-Komponenten in Ihrem Unternehmen mithilfe eines Softwareverteilungssystems bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="7770a-105">The following section provides information and instructions to help you deploy the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components throughout your enterprise by using a software distribution system.</span></span>

**<span data-ttu-id="7770a-106">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7770a-106">Note</span></span>**  
<span data-ttu-id="7770a-107">Je nachdem, welche softwareverteilungslösung Sie verwenden, müssen Sie mit den Anforderungen ihrer jeweiligen Lösung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="7770a-107">Whichever software distribution solution that you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="7770a-108">Wenn Sie System Center Configuration Manager 2007 R2 oder eine neuere Version verwenden, lesen Sie die [Configuration Manager-Dokumentationsbibliothek](https://go.microsoft.com/fwlink/?LinkId=66999) in der Microsoft Technical Library ( https://go.microsoft.com/fwlink/?LinkId=66999) .</span><span class="sxs-lookup"><span data-stu-id="7770a-108">If you are using System Center Configuration Manager 2007 R2 or a later version, see the [Configuration Manager Documentation Library](https://go.microsoft.com/fwlink/?LinkId=66999) in the Microsoft Technical Library (https://go.microsoft.com/fwlink/?LinkId=66999).</span></span>



**<span data-ttu-id="7770a-109">Wichtig</span><span class="sxs-lookup"><span data-stu-id="7770a-109">Important</span></span>**  
<span data-ttu-id="7770a-110">Wenn Sie System Center Configuration Manager 2007 SP2 verwenden und ihre MED-V-Arbeitsbereiche für den Betrieb im **NAT** -Modus konfiguriert sind, werden die virtuellen Computer als Internet basierte Clients klassifiziert und können nicht die nächstgelegenen Verteilungspunkte finden, von denen Inhalte heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7770a-110">If you are using System Center Configuration Manager 2007 SP2 and your MED-V workspaces are configured to operate in **NAT** mode, the virtual machines are classified as Internet-based clients and cannot find the closest distribution points from which to download content.</span></span>

<span data-ttu-id="7770a-111">Der [Hotfix zum Verbessern der Funktionalität für VMS, die von Med-v verwaltet werden](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) fügt neue Funktionen zu virtuellen Computern hinzu, die von Med-v verwaltet werden und für den Betrieb im **NAT** -Modus konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="7770a-111">The [hotfix to improve the functionality for VMs that are managed by MED-V](https://go.microsoft.com/fwlink/?LinkId=201088) (https://go.microsoft.com/fwlink/?LinkId=201088) adds new functionality to virtual machines that are managed by MED-V and that are configured to operate in **NAT** mode.</span></span> <span data-ttu-id="7770a-112">Mit der neuen Funktionalität können virtuelle Maschinen auf die nächstgelegenen Verteilungspunkte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7770a-112">The new functionality lets virtual machines access the closest distribution points.</span></span> <span data-ttu-id="7770a-113">Daher kann der Administrator den virtuellen Computer und den Hostcomputer auf die gleiche Weise verwalten.</span><span class="sxs-lookup"><span data-stu-id="7770a-113">Therefore, the administrator can manage the virtual machine and the host computer in the same manner.</span></span> <span data-ttu-id="7770a-114">Dieser Hotfix muss zuerst auf dem Website Server und dann auf dem Client installiert werden.</span><span class="sxs-lookup"><span data-stu-id="7770a-114">This hotfix must be installed first on the site server and then on the client.</span></span>

<span data-ttu-id="7770a-115">Das Update ist öffentlich verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7770a-115">The update is publicly available.</span></span> <span data-ttu-id="7770a-116">Möglicherweise werden Sie jedoch aufgefordert, eine Vereinbarung für Microsoft-Dienste zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="7770a-116">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="7770a-117">Folgen Sie den Anweisungen auf den nachfolgenden Webseiten, um diesen Hotfix abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7770a-117">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>



**<span data-ttu-id="7770a-118">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7770a-118">Note</span></span>**  
<span data-ttu-id="7770a-119">Bevor Sie die Med-v-Komponenten über Ihr Softwareverteilungssystem bereitstellen können, müssen Sie den Med-v-Arbeitsbereichs-Packager installieren und ihre Med-v-Arbeitsbereiche erstellen.</span><span class="sxs-lookup"><span data-stu-id="7770a-119">You must install the MED-V workspace packager and build your MED-V workspaces before you can deploy the MED-V components through your software distribution system.</span></span> <span data-ttu-id="7770a-120">Weitere Informationen dazu, wie Sie ein Bild vorbereiten und ihre Med-v-Arbeitsbereiche erstellen, finden Sie unter [Operationen für med-v](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="7770a-120">For more information about how to prepare an image and to build your MED-V workspaces, see [Operations for MED-V](operations-for-med-v.md).</span></span>



**<span data-ttu-id="7770a-121">So stellen Sie die MED-V-Komponenten mithilfe eines Softwareverteilungssystems bereit</span><span class="sxs-lookup"><span data-stu-id="7770a-121">To deploy the MED-V components by using a software distribution system</span></span>**

1.  <span data-ttu-id="7770a-122">Definieren Sie eine Gruppe von Computern und Benutzern im elektronischen Softwareverteilungssystem als Zielgruppe von Computern/Benutzern.</span><span class="sxs-lookup"><span data-stu-id="7770a-122">Define a group of computers and users in the electronic software distribution system as the target set of computers/users.</span></span>

2.  <span data-ttu-id="7770a-123">Erstellen Sie Pakete für jede Microsoft-Installationsdatei, die verteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7770a-123">Create packages for each Microsoft installation file that needs to be distributed.</span></span> <span data-ttu-id="7770a-124">Im folgenden finden Sie die erforderlichen Dateien und die Reihenfolge, in der Sie installiert werden müssen:</span><span class="sxs-lookup"><span data-stu-id="7770a-124">The following are the required files and the order in which they must be installed:</span></span>

    1.  <span data-ttu-id="7770a-125">**Windows Virtual PC** – wenn noch nicht installiert (ein Neustart des Computers ist erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7770a-125">**Windows Virtual PC** – if not already installed (a computer restart is required).</span></span> <span data-ttu-id="7770a-126">Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.</span><span class="sxs-lookup"><span data-stu-id="7770a-126">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    2.  <span data-ttu-id="7770a-127">**Windows Virtual PC-Ergänzungen und-Updates** – Falls noch nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="7770a-127">**Windows Virtual PC Additions and Updates** – if not already installed.</span></span> <span data-ttu-id="7770a-128">Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.</span><span class="sxs-lookup"><span data-stu-id="7770a-128">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    3.  <span data-ttu-id="7770a-129">**Installationsdatei des Med-v-Host-Agents** – installiert den Host-Agent (Med-v \ _HostAgent \ _setup Installationsdatei).</span><span class="sxs-lookup"><span data-stu-id="7770a-129">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="7770a-130">Weitere Informationen finden Sie unter [Manuelles Installieren des MED-V-Host-Agents](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="7770a-130">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

        **<span data-ttu-id="7770a-131">Warnung</span><span class="sxs-lookup"><span data-stu-id="7770a-131">Warning</span></span>**  
        <span data-ttu-id="7770a-132">Schließen Sie Internet Explorer, bevor Sie den MED-V-Host-Agent installieren, andernfalls können Konflikte später bei der URL-Umleitung auftreten.</span><span class="sxs-lookup"><span data-stu-id="7770a-132">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="7770a-133">Sie können dies auch tun, indem Sie während einer Verteilung einen Neustart des Computers angeben.</span><span class="sxs-lookup"><span data-stu-id="7770a-133">You can also do this by specifying a computer restart during a distribution.</span></span>   

    4.  <span data-ttu-id="7770a-134">Das **Med-v Workspace-Installationsprogramm, die VHD und die Setup-Datei** , die im **Med-v-Arbeitsbereichs Paket**erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7770a-134">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="7770a-135">Weitere Informationen finden Sie unter [Erstellen eines MED-V-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="7770a-135">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        **<span data-ttu-id="7770a-136">Wichtig</span><span class="sxs-lookup"><span data-stu-id="7770a-136">Important</span></span>**  
        <span data-ttu-id="7770a-137">Die komprimierte virtuelle Festplattendatei (. medv) und das ausführbare Setup Programm (setup.exe) müssen sich im gleichen Ordner wie das MED-V Workspace-Installationsprogramm befinden.</span><span class="sxs-lookup"><span data-stu-id="7770a-137">The compressed virtual hard disk file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="7770a-138">Installieren Sie dann das MED-V Workspace-Installationsprogramm, indem Sie setup.exe ausführen.</span><span class="sxs-lookup"><span data-stu-id="7770a-138">Then, install the MED-V workspace installer by running setup.exe.</span></span>

        **<span data-ttu-id="7770a-139">Tipp</span><span class="sxs-lookup"><span data-stu-id="7770a-139">Tip</span></span>**  
        <span data-ttu-id="7770a-140">Da Probleme auftreten können, wenn Sie Med-v von einem Netzwerkspeicherort installieren, empfehlen wir, dass Sie die Setupdateien des Med-v-Arbeitsbereichs lokal kopieren und dann setup.exe ausführen.</span><span class="sxs-lookup"><span data-stu-id="7770a-140">Because problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>       

3.  <span data-ttu-id="7770a-141">Konfigurieren Sie die Pakete so, dass Sie im unbeaufsichtigten Modus ausgeführt werden (es ist keine Benutzerinteraktion erforderlich).</span><span class="sxs-lookup"><span data-stu-id="7770a-141">Configure the packages to run in silent mode (no user interaction is required).</span></span>

    <span data-ttu-id="7770a-142">Wenn Sie im unbeaufsichtigten Modus ausgeführt wird, wird die Aufforderung zum Schließen von Internet Explorer, wenn Sie ausgeführt wird, und die Aufforderung zum Starten des MED-V-Host-Agents beseitigt.</span><span class="sxs-lookup"><span data-stu-id="7770a-142">Running in silent mode eliminates the prompt to close Internet Explorer if it is running and the prompt to start the MED-V Host Agent.</span></span> <span data-ttu-id="7770a-143">Beide Aktionen werden ausgeführt, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7770a-143">Both actions are performed when the computer is restarted.</span></span>

    **<span data-ttu-id="7770a-144">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7770a-144">Note</span></span>**  
    <span data-ttu-id="7770a-145">Bei der Installation von Windows Virtual PC müssen Sie den Computer neu starten.</span><span class="sxs-lookup"><span data-stu-id="7770a-145">Installation of Windows Virtual PC requires you to restart the computer.</span></span> <span data-ttu-id="7770a-146">Wenn Sie den Neustart unterdrücken und die erforderlichen Voraussetzungen für die Installation von MED-V ignorieren, können Sie einen einzelnen Installationsvorgang erstellen und alle Komponenten gleichzeitig installieren.</span><span class="sxs-lookup"><span data-stu-id="7770a-146">You can create a single installation process and install all the components at the same time if you suppress the restart and ignore the prerequisites necessary for MED-V to install.</span></span> <span data-ttu-id="7770a-147">Sie können dies auch über Befehlszeilenargumente tun.</span><span class="sxs-lookup"><span data-stu-id="7770a-147">You can also do this by using command-line arguments.</span></span> <span data-ttu-id="7770a-148">Ein Beispiel für diese Argumente finden Sie unter [So installieren Sie die MED-V-Komponenten mithilfe einer Batchdatei](#bkmk-batch).</span><span class="sxs-lookup"><span data-stu-id="7770a-148">For an example of these arguments, see [To install the MED-V components by using a batch file](#bkmk-batch).</span></span> <span data-ttu-id="7770a-149">MED-V wird automatisch gestartet, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7770a-149">MED-V automatically starts when the computer is restarted.</span></span>

4.  <span data-ttu-id="7770a-150">Installieren Sie MED-V und die zugehörigen Komponenten, bevor Sie Windows Virtual PC installieren.</span><span class="sxs-lookup"><span data-stu-id="7770a-150">Install MED-V and its components before installing Windows Virtual PC.</span></span> <span data-ttu-id="7770a-151">Lesen Sie die Beispielbatchdatei weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="7770a-151">See the example batch file later in this topic.</span></span>

    **<span data-ttu-id="7770a-152">Wichtig</span><span class="sxs-lookup"><span data-stu-id="7770a-152">Important</span></span>**  
    <span data-ttu-id="7770a-153">Wählen Sie die Option **\ _PREREQUISITES ignorieren** aus, wie in der Beispielbatchdatei gezeigt, damit die MED-V-Komponenten vor den erforderlichen VPC-Komponenten installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="7770a-153">Select the **IGNORE\_PREREQUISITES** option as shown in the example batch file so that the MED-V components can be installed prior to the required VPC components.</span></span> <span data-ttu-id="7770a-154">Installieren Sie die MED-V-Komponenten in dieser Reihenfolge, um den einmaligen Neustart zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7770a-154">Install the MED-V components in this order to allow for the single restart.</span></span>

5.  <span data-ttu-id="7770a-155">Ermitteln Sie alle anderen Anforderungen, die für die Installation und für Ihr Softwareverteilungssystem wie Zielplattformen und den freien Speicherplatz erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7770a-155">Identify any other requirements necessary for the installation and for your software distribution system, such as target platforms and the free disk space.</span></span>

6.  <span data-ttu-id="7770a-156">Weisen Sie die Pakete der Zielgruppe von Computern/Benutzern zu.</span><span class="sxs-lookup"><span data-stu-id="7770a-156">Assign the packages to the target set of computers/users.</span></span>

    <span data-ttu-id="7770a-157">Wenn Computer ausgeführt werden, erkennt der Client für Softwareverteilungssysteme, dass neue Pakete verfügbar sind, und beginnt, die Pakete pro Definition und Anforderungen zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7770a-157">As computers are running, the software distribution system client recognizes that new packages are available and begins to install the packages per the definition and requirements.</span></span> <span data-ttu-id="7770a-158">Die Installationen sollten sequenziell im unbeaufsichtigten Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7770a-158">The installations should run sequentially in silent mode.</span></span> <span data-ttu-id="7770a-159">Wir empfehlen, dass dies als ein einzelner Prozess ausgeführt wird, für den kein Neustart erforderlich ist, bis alle Pakete installiert sind.</span><span class="sxs-lookup"><span data-stu-id="7770a-159">We recommend that this is performed as a single process that does not require a restart until all the packages are installed.</span></span>

7.  <span data-ttu-id="7770a-160">Nachdem die Installation abgeschlossen ist, starten Sie die aktualisierten Computer neu.</span><span class="sxs-lookup"><span data-stu-id="7770a-160">After the installations are complete, restart the updated computers.</span></span>

    <span data-ttu-id="7770a-161">Je nach Softwareverteilungssystem können Sie einen Neustart des Computers planen, oder die Endbenutzer können die Computer während der regulären Arbeit manuell neu starten.</span><span class="sxs-lookup"><span data-stu-id="7770a-161">Depending on the software distribution system, you can schedule a restart of the computer or the end users can restart the computers manually during their regular work.</span></span> <span data-ttu-id="7770a-162">Nachdem der Computer neu gestartet wurde, wird MED-V automatisch gestartet, wenn sich ein Endbenutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="7770a-162">After the computer is restarted, MED-V automatically starts after an end user logs on.</span></span> <span data-ttu-id="7770a-163">Wenn MED-V zum ersten Mal gestartet wird, wird die erstmalige Einrichtung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7770a-163">When MED-V starts for the first time, it runs first time setup.</span></span>

<span data-ttu-id="7770a-164">Das erstmalige Setup wird gestartet und kann einige Minuten dauern, abhängig von der Größe der von Ihnen angegebenen virtuellen Festplatte und der Anzahl der Richtlinien, die beim Start auf den MED-V Workspace angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7770a-164">First time setup starts and might take several minutes to finish, depending on the size of the virtual hard disk that you specified and the number of policies applied to the MED-V workspace on startup.</span></span> <span data-ttu-id="7770a-165">Der Endbenutzer kann den Fortschritt nachverfolgen, indem er das MED-V-Symbol im Infobereich ansieht.</span><span class="sxs-lookup"><span data-stu-id="7770a-165">The end user can track the progress by watching the MED-V icon in the notification area.</span></span> <span data-ttu-id="7770a-166">Weitere Informationen zum erstmaligen Einrichten finden Sie unter [Übersicht über die Bereitstellung von MED-V 2,0](med-v-20-deployment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7770a-166">For more information about first time setup, see [MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md).</span></span>

<a href="" id="bkmk-batch"></a>**<span data-ttu-id="7770a-167">So installieren Sie die MED-V-Komponenten mithilfe einer Batchdatei</span><span class="sxs-lookup"><span data-stu-id="7770a-167">To install the MED-V components by using a batch file</span></span>**

1.  <span data-ttu-id="7770a-168">Führen Sie die Installation an einer Eingabeaufforderung mit Administratorrechten aus.</span><span class="sxs-lookup"><span data-stu-id="7770a-168">Run the installation at a command prompt with administrative credentials.</span></span>

2.  <span data-ttu-id="7770a-169">Stellen Sie die einzelnen Komponenten in einem einzigen Verzeichnis bereit.</span><span class="sxs-lookup"><span data-stu-id="7770a-169">Deploy each component to a single directory.</span></span> <span data-ttu-id="7770a-170">Wenn Sie von einer Netzwerkfreigabe ausführen, ist eine längere Zeit erforderlich, um die medv-Datei zu dekomprimieren.</span><span class="sxs-lookup"><span data-stu-id="7770a-170">If run from a network share, a longer time is required to decompress the .medv file.</span></span>

3.  <span data-ttu-id="7770a-171">Als bewährte Methode können Sie angeben, dass Windows Virtual PC und der Windows Virtual PC-Hotfix nach dem Med-v-Host-Agent und den Med-v-Arbeitsbereichs Paketdateien installiert werden.</span><span class="sxs-lookup"><span data-stu-id="7770a-171">As a best practice, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="7770a-172">Dies bedeutet, dass Windows Update keinen Eingriff in den Installationsvorgang verursacht, da ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7770a-172">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

4.  <span data-ttu-id="7770a-173">Starten Sie den Computer nach Abschluss der Batchdatei neu.</span><span class="sxs-lookup"><span data-stu-id="7770a-173">Restart the computer after the batch file is finished.</span></span>

<span data-ttu-id="7770a-174">Nach dem Neustart wird der Benutzer aufgefordert, das erstmalige Setup auszuführen und die Konfiguration von MED-V abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7770a-174">After the restart, the user is prompted to run first time setup and complete the configuration of MED-V.</span></span>

<span data-ttu-id="7770a-175">Im folgenden Beispiel wird mit den angegebenen Argumenten gezeigt, wie Sie 64-Bit-MED-V-Komponenten in einem einzigen Prozess installieren:</span><span class="sxs-lookup"><span data-stu-id="7770a-175">The following example, with the specified arguments, shows how to install 64-bit MED-V components in a single process:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7770a-176">Argument</span><span class="sxs-lookup"><span data-stu-id="7770a-176">Argument</span></span></th>
<th align="left"><span data-ttu-id="7770a-177">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7770a-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7770a-178">/norestart</span><span class="sxs-lookup"><span data-stu-id="7770a-178">/norestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="7770a-179">Verhindert, dass die Installation von Windows Virtual PC und dem Windows Virtual PC-Update den Hostcomputer neu startet.</span><span class="sxs-lookup"><span data-stu-id="7770a-179">Prevents the installation of Windows Virtual PC and the Windows Virtual PC update from restarting the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7770a-180">/Quiet</span><span class="sxs-lookup"><span data-stu-id="7770a-180">/quiet</span></span></p></td>
<td align="left"><p><span data-ttu-id="7770a-181">Installiert die MED-V-Komponenten im stillen Modus ohne Benutzerinteraktion.</span><span class="sxs-lookup"><span data-stu-id="7770a-181">Installs the MED-V components in quiet mode without user interaction.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7770a-182">/Qn</span><span class="sxs-lookup"><span data-stu-id="7770a-182">/qn</span></span></p></td>
<td align="left"><p><span data-ttu-id="7770a-183">Installiert die MED-V-Komponenten ohne eine Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="7770a-183">Installs the MED-V components without a user interface.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7770a-184">IGNORE_PREREQUISITES</span><span class="sxs-lookup"><span data-stu-id="7770a-184">IGNORE_PREREQUISITES</span></span></p></td>
<td align="left"><p><span data-ttu-id="7770a-185">Installationen ohne Überprüfung auf Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="7770a-185">Installs without checking for Windows Virtual PC.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7770a-186">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7770a-186">Note</span></span></strong><br/><p><span data-ttu-id="7770a-187">Geben Sie dieses Argument nur an, wenn Sie Windows Virtual PC als Teil dieser Installation installieren.</span><span class="sxs-lookup"><span data-stu-id="7770a-187">Only specify this argument if you are installing Windows Virtual PC as part of this installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7770a-188">OVERWRITEVHD</span><span class="sxs-lookup"><span data-stu-id="7770a-188">OVERWRITEVHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="7770a-189">Erzwingt die Installation des MED-V-Arbeitsbereichs und verhindert eventuelle Eingabeaufforderungen.</span><span class="sxs-lookup"><span data-stu-id="7770a-189">Forces the installation of the MED-V workspace and prevents any prompts that it might generate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7770a-190">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7770a-190">Example</span></span>


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## <span data-ttu-id="7770a-191">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7770a-191">Related topics</span></span>


[<span data-ttu-id="7770a-192">Übersicht über die Bereitstellung von MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="7770a-192">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="7770a-193">Bereitstellen der MED-V-Komponenten</span><span class="sxs-lookup"><span data-stu-id="7770a-193">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)









