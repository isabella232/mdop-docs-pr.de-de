---
title: Identifizieren der Anzahl und Typen von MED-V-Arbeitsbereichen
description: Identifizieren der Anzahl und Typen von MED-V-Arbeitsbereichen
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812250"
---
# <span data-ttu-id="3f4b6-103">Identifizieren der Anzahl und Typen von MED-V-Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="3f4b6-103">Identifying the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="3f4b6-104">MED-V erstellt eine virtuelle Umgebung zum Ausführen von Anwendungen, die Windows XP erfordern oder für die eine Version von Internet Explorer erforderlich ist, die von der Version auf dem Hostcomputer abweicht.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-104">MED-V creates a virtual environment for running applications that require Windows XP or that require a version of Internet Explorer that differs from the version on the host computer.</span></span> <span data-ttu-id="3f4b6-105">Diese virtuelle Umgebung wird als MED-V-Arbeitsbereich bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-105">This virtual environment is known as a MED-V workspace.</span></span>

<span data-ttu-id="3f4b6-106">Je nach den Anwendungs Kompatibilitätsanforderungen, die Ihre Organisation bei der Migration zu Windows 7 hat, können nur bestimmte Benutzer oder Abteilungen MED-V-Arbeitsbereiche benötigen.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-106">Depending on the application compatibility requirements faced by your organization as you migrate to Windows 7, only certain users or departments might require MED-V workspaces.</span></span> <span data-ttu-id="3f4b6-107">Bei der Planung der Bereitstellung müssen Sie die Anzahl der MED-V-Arbeitsbereiche ermitteln, die für Ihr Unternehmen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-107">As you plan your deployment, you have to determine the number of MED-V workspaces required in your enterprise.</span></span> <span data-ttu-id="3f4b6-108">Darüber hinaus müssen Sie die Anforderungen für jeden MED-V-Arbeitsbereich definieren.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-108">You also have to define the requirements of each MED-V workspace.</span></span>

## <span data-ttu-id="3f4b6-109">Ermitteln der Anzahl und Typen von MED-V-Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="3f4b6-109">Identify the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="3f4b6-110">Identifizieren Sie die Computer und Gruppen in Ihrem Unternehmen, für die Sie MED-V-Arbeitsbereiche erstellen werden.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-110">Identify the computers and groups in your enterprise for which you will be creating MED-V workspaces.</span></span> <span data-ttu-id="3f4b6-111">In der Regel sind dies die Benutzer, die Zugriff auf die Anwendungen benötigen, die nicht zu Windows 7 migriert werden können.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-111">Typically, these are the users who require access to those applications that cannot be migrated to Windows 7.</span></span> <span data-ttu-id="3f4b6-112">Identifizieren Sie die Anwendungen, die nicht migriert werden können, und die Benutzer, die einen MED-V-Arbeitsbereich zum Ausführen dieser Anwendungen benötigen.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-112">Identify those applications that cannot be migrated and the users who require a MED-V workspace to run these applications.</span></span>

<span data-ttu-id="3f4b6-113">Möglicherweise haben Sie auch Intranet-Adressen, die noch nicht für Windows 7 optimiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-113">You might also have intranet addresses that have not yet been optimized for Windows 7.</span></span> <span data-ttu-id="3f4b6-114">Der MED-V-Arbeitsbereich bietet einen Internet Explorer-Browser, über den Endbenutzer besser auf diese Webadressen zugreifen können, die noch nicht für die Migration zu Windows 7 bereit sind.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-114">The MED-V workspace provides an Internet Explorer browser through which end users can better access those web addresses that are not yet ready for the migration to Windows 7.</span></span> <span data-ttu-id="3f4b6-115">Während Sie Ihre Med-v-Bereitstellung vorbereiten und planen, müssen Sie eine Liste der URL-Adressen identifizieren und kompilieren, die von Internet Explorer auf dem Hostcomputer an Internet Explorer im Med-v-Arbeitsbereich umgeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-115">As you are preparing and planning your MED-V deployment, you will have to identify and compile a list of the URL addresses to redirect from Internet Explorer on the host computer to Internet Explorer in the MED-V workspace.</span></span>

<span data-ttu-id="3f4b6-116">Schließlich müssen Sie Ihre Speicherplatzanforderungen auswerten.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-116">Finally, you have to evaluate your disk space requirements.</span></span> <span data-ttu-id="3f4b6-117">Die meisten MED-V-Arbeitsbereiche sind 2 Gigabyte (GB) oder größer.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-117">Most MED-V workspaces are 2 gigabytes (GB) or larger.</span></span> <span data-ttu-id="3f4b6-118">Je nach Anzahl der Benutzer und der Konfiguration von MED-V kann der verfügbare Speicherplatz auf einem System schnell genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-118">The available disk space on a system can be consumed quickly, depending on the number of users and the configuration of MED-V.</span></span> <span data-ttu-id="3f4b6-119">Außerdem kann die bevorzugte Verteilungsmethode Ihres Unternehmens zusätzlichen Speicherplatz benötigen.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-119">Also, your company’s preferred method of distribution can require additional space.</span></span> <span data-ttu-id="3f4b6-120">Im Allgemeinen sollten Sie eine Mindestmenge von 10 GB Speicherplatz für einen MED-V-Arbeitsbereich freigeben, doch variiert dies je nach Größe des Bilds erheblich.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-120">Generally, you should free a minimum of 10 GB of disk space for a MED-V workspace, but this varies greatly, depending on the size of the image.</span></span>

### <span data-ttu-id="3f4b6-121">Berechnen der Speicherplatzanforderungen für MED-V-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="3f4b6-121">Calculate the Disk Space Requirements for MED-V Workspaces</span></span>

<span data-ttu-id="3f4b6-122">Ein MED-V-Arbeitsbereich erfordert Arbeitsspeicher und Speicherplatz auf dem Hostcomputer, auf dem er installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-122">A MED-V workspace requires memory and disk space from the host computer on which it is installed.</span></span> <span data-ttu-id="3f4b6-123">Auf dem Host sind mindestens 2 GB Speicherplatz erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-123">At a minimum, 2 GB of disk space are required on the host.</span></span> <span data-ttu-id="3f4b6-124">Der Speicherplatz ist variabel und hängt von der Anzahl der Anwendungen und den Daten im MED-V-Arbeitsbereich eines Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-124">Disk space is variable and depends on the number of applications and the data in a user’s MED-V workspace.</span></span>

<span data-ttu-id="3f4b6-125">Wir empfehlen einen Mindestspeicher von 10 GB Speicherplatz für MED-V.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-125">We recommend a minimum of 10 GB of disk space for MED-V.</span></span> <span data-ttu-id="3f4b6-126">Dieser Betrag ermöglicht einen einfachen Windows XP-Arbeitsbereich und einige grundlegende installierte Anwendungen und die webumleitung.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-126">This amount allows for a basic Windows XP workspace and some basic installed applications and web redirection.</span></span> <span data-ttu-id="3f4b6-127">Darüber hinaus steht der Speicherplatz für das Host-Swap-Laufwerk zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-127">It also provides available space for the host swap drive.</span></span> <span data-ttu-id="3f4b6-128">In einer einfachen Konfiguration verbraucht Med-v und ein einzelner bereitgestellter Med-v-Arbeitsbereich so viel wie 6 bis 8 GB.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-128">In a basic configuration, MED-V and a single deployed MED-V workspace consume as much as 6 to 8 GB.</span></span> <span data-ttu-id="3f4b6-129">Wenn Sie viele Anwendungen in den Med-v-Arbeitsbereich einbeziehen oder mehr als einen Benutzer pro Computer haben, können Sie die folgende Berechnung verwenden, um den von Ihrem Med-v-Arbeitsbereich benötigten Speicherplatz genauer zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="3f4b6-129">If you include lots of applications on the MED-V workspace or have more than one user per computer, then you can use the following calculation to more accurately determine the disk space your MED-V workspace requires:</span></span>

*<span data-ttu-id="3f4b6-130">Basis-VHD + (Benutzer pro Computer x (Differenzdaten Träger + gespeicherter Zustand))</span><span class="sxs-lookup"><span data-stu-id="3f4b6-130">Base VHD + (User per computer x (Difference Disk + Saved State))</span></span>*

<span data-ttu-id="3f4b6-131">Um den erforderlichen Speicherplatz zu berechnen, müssen Sie Folgendes ermitteln:</span><span class="sxs-lookup"><span data-stu-id="3f4b6-131">To calculate the required disk space, determine the following:</span></span>

-   <span data-ttu-id="3f4b6-132">**Größe der Basis-VHD** – die virtuelle Festplatte, die zum Erstellen des MED-V-Arbeitsbereichs verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-132">**Size of the base VHD** – the virtual hard disk that was used to create the MED-V workspace.</span></span>

    <span data-ttu-id="3f4b6-133">**Wichtig**  Verwenden Sie die medv-Dateigröße für Ihre Berechnung nicht, da die medv-Datei komprimiert ist.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-133">**Important** Do not use the .medv file size for your calculation because the .medv file is compressed.</span></span>

     

-   <span data-ttu-id="3f4b6-134">**Benutzer pro Computer** – Med-v erstellt einen Med-v-Arbeitsbereich für jeden Benutzer auf einem Computer; der Med-v-Arbeitsbereich beansprucht Speicherplatz, während sich jeder Benutzer anmeldet und der Med-v-Arbeitsbereich erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-134">**Users per computer** – MED-V creates a MED-V workspace for each user on a computer; the MED-V workspace consumes disk space as each user logs on and the MED-V workspace is created.</span></span>

-   <span data-ttu-id="3f4b6-135">**Die Größe des differenzierenden Datenträgers** – wird verwendet, um den Unterschied zur Basisfestplatte zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-135">**Size of the differencing disk** – used to track the difference from the base VHD.</span></span> <span data-ttu-id="3f4b6-136">Diese Größe variiert beim Hinzufügen von Anwendungen und Softwareupdates zur virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-136">This size varies as you add applications and software updates to the virtual hard disk.</span></span> <span data-ttu-id="3f4b6-137">Für jeden Med-v-Benutzer wird ein differenzierender Datenträger erstellt, wenn Sie Med-v zum ersten Mal starten.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-137">A differencing disk is created for each MED-V user when they start MED-V for the first time.</span></span>

-   <span data-ttu-id="3f4b6-138">**Die Größe der gespeicherten Zustandsdatei** – wird verwendet, um den Zustand auf dem virtuellen Computer beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-138">**Size of the Saved State file** – used to maintain state in the virtual machine.</span></span> <span data-ttu-id="3f4b6-139">In der Regel ist dies nur ein bisschen größer als der zugewiesene Arbeitsspeicher für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-139">Typically, this is just a bit larger than the allocated RAM for the virtual machine.</span></span> <span data-ttu-id="3f4b6-140">Beispielsweise erstellt 1 GB Arbeitsspeicher eine Datei über 1.081.000 KB.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-140">For example, 1 GB of RAM allocated creates a file about 1,081,000 KB.</span></span>

<span data-ttu-id="3f4b6-141">Das folgende Beispiel zeigt eine Berechnung auf der Grundlage von drei Benutzern eines MED-V-Arbeitsbereichs mit einer virtuellen 2,6 GB-Festplatte:</span><span class="sxs-lookup"><span data-stu-id="3f4b6-141">The following example shows a calculation based on three users of a MED-V workspace that has a 2.6 GB virtual hard disk:</span></span>

*<span data-ttu-id="3f4b6-142">2.6 GB + (3 x (1,5 GB + 1GB)) = 10,1 GB</span><span class="sxs-lookup"><span data-stu-id="3f4b6-142">2.6gb + (3 x (1.5gb + 1gb)) = 10.1gb</span></span>*

<span data-ttu-id="3f4b6-143">**Hinweis**  Eine optimale Methode für MED-V besteht darin, den erforderlichen Speicherplatz mithilfe einer Lab-Bereitstellung zu berechnen, um die Anforderungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-143">**Note** A MED-V best practice is to calculate the required space by using a lab deployment to validate the requirements.</span></span>

 

### <span data-ttu-id="3f4b6-144">Suchen der Dateien zum Ermitteln der Dateigröße</span><span class="sxs-lookup"><span data-stu-id="3f4b6-144">Locate the Files to Determine File Size</span></span>

<span data-ttu-id="3f4b6-145">Die folgenden Speicherorte enthalten die Dateien für die Computer-und Benutzereinstellungen:</span><span class="sxs-lookup"><span data-stu-id="3f4b6-145">The following locations contain the files for the computer and user settings:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3f4b6-146">Typ</span><span class="sxs-lookup"><span data-stu-id="3f4b6-146">Type</span></span></th>
<th align="left"><span data-ttu-id="3f4b6-147">Pfad</span><span class="sxs-lookup"><span data-stu-id="3f4b6-147">Location</span></span></th>
<th align="left"><span data-ttu-id="3f4b6-148">Dateien</span><span class="sxs-lookup"><span data-stu-id="3f4b6-148">Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f4b6-149">Basis-VHD</span><span class="sxs-lookup"><span data-stu-id="3f4b6-149">Base VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f4b6-150">%ProgramData%\Microsoft\Medv\Workspace</span><span class="sxs-lookup"><span data-stu-id="3f4b6-150">%ProgramData%\Microsoft\Medv\Workspace</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="3f4b6-151">InternalName </em> . VHD – wobei <em> internalname </em> der Name der virtuellen Festplatte ist, die Sie im MED-V Workspace-Paketer ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-151">InternalName</em>.vhd - Where <em>InternalName</em> is the name of the virtual hard disk that you selected in the MED-V Workspace Packager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3f4b6-152">Differenzierender Datenträger</span><span class="sxs-lookup"><span data-stu-id="3f4b6-152">Differencing Disk</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f4b6-153">%LocalAppData%\Microsoft\MEDV\v2\Virtual-Maschinen</span><span class="sxs-lookup"><span data-stu-id="3f4b6-153">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="3f4b6-154">WorkspaceName </em> . VHD</span><span class="sxs-lookup"><span data-stu-id="3f4b6-154">WorkspaceName</em>.vhd</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f4b6-155">Gespeicherte Statusdatei</span><span class="sxs-lookup"><span data-stu-id="3f4b6-155">Saved State File</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f4b6-156">%LocalAppData%\Microsoft\MEDV\v2\Virtual-Maschinen</span><span class="sxs-lookup"><span data-stu-id="3f4b6-156">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="3f4b6-157">WorkspaceName </em> . VSV</span><span class="sxs-lookup"><span data-stu-id="3f4b6-157">WorkspaceName</em>.vsv</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3f4b6-158">Berechnen der Speicherplatzanforderungen für freigegebene MED-V-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="3f4b6-158">Calculate the Disk Space Requirements for Shared MED-V Workspaces</span></span>

<span data-ttu-id="3f4b6-159">Wenn Sie für eine freigegebene Med-v Workspace-Bereitstellung auf einem einzelnen Computer berechnen, ist die Anzahl der Benutzer pro Computer in ihrer Berechnung immer "1", da Med-v nur einen einzelnen differenzierenden Datenträger für alle Benutzer konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-159">If you are calculating for a shared MED-V workspace deployment on a single computer, then the number of users per computer in your calculation is always “1” because MED-V only configures a single differencing disk for all users.</span></span>

<span data-ttu-id="3f4b6-160">Sie können den differenzierenden Datenträger und die gespeicherte Zustandsdatei für freigegebene MED-V-Arbeitsbereiche in%ProgramData%\\Microsoft\\Medv\\AllUsers. finden.</span><span class="sxs-lookup"><span data-stu-id="3f4b6-160">You can find the differencing disk and the saved state file for shared MED-V workspaces in %ProgramData%\\Microsoft\\Medv\\AllUsers.</span></span>

## <span data-ttu-id="3f4b6-161">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3f4b6-161">Related topics</span></span>


[<span data-ttu-id="3f4b6-162">Definieren und Planen der MED-V-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3f4b6-162">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

[<span data-ttu-id="3f4b6-163">Planen für MED-V</span><span class="sxs-lookup"><span data-stu-id="3f4b6-163">Planning for MED-V</span></span>](planning-for-med-v.md)

 

 





