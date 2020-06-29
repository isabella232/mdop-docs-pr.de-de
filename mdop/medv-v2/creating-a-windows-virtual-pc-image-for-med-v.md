---
title: Erstellen eines Windows Virtual PC-Images für MED-V
description: Erstellen eines Windows Virtual PC-Images für MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804412"
---
# <span data-ttu-id="109e9-103">Erstellen eines Windows Virtual PC-Images für MED-V</span><span class="sxs-lookup"><span data-stu-id="109e9-103">Creating a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="109e9-104">Bevor Sie einen Med-v-Arbeitsbereich für Benutzer bereitstellen können, müssen Sie zuerst eine virtuelle Festplatte vorbereiten, die Sie zum Erstellen des Med-v Workspace-Installationspakets für Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 verwenden.</span><span class="sxs-lookup"><span data-stu-id="109e9-104">Before you can deliver a MED-V workspace to users, you have to first prepare a virtual hard disk that you use to build the MED-V workspace installer package for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="109e9-105">Um die erforderliche virtuelle Festplatte vorzubereiten, müssen Sie ein Windows Virtual PC-Abbild erstellen, das das erforderliche Betriebssystem, Updates und Software enthält, damit Sie später Anwendungen und URL-Umleitungsinformationen für Benutzer bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="109e9-105">To prepare the necessary virtual hard disk, you must create a Windows Virtual PC image that contains the required operating system, updates, and software to let you later deploy applications and URL redirection information to users.</span></span> <span data-ttu-id="109e9-106">Dieser Abschnitt enthält Anleitungen zum Erstellen der virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="109e9-106">This section provides guidance about how to create the virtual hard disk.</span></span>

<span data-ttu-id="109e9-107">Zum Erstellen eines virtuellen Bilds für MED-V müssen Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="109e9-107">To create a virtual image for MED-V, you must follow these steps.</span></span>

1.  [<span data-ttu-id="109e9-108">Erstellen eines Windows Virtual PC-Bilds</span><span class="sxs-lookup"><span data-stu-id="109e9-108">Create a Windows Virtual PC image</span></span>](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [<span data-ttu-id="109e9-109">Installieren von Windows XP auf dem Bild</span><span class="sxs-lookup"><span data-stu-id="109e9-109">Install Windows XP on the image</span></span>](#bkmk-installingwindowsxpontovpc)

3.  [<span data-ttu-id="109e9-110">Installieren von .NET Framework auf dem Bild</span><span class="sxs-lookup"><span data-stu-id="109e9-110">Install the .NET Framework on the image</span></span>](#bkmk-installingnet)

4.  [<span data-ttu-id="109e9-111">Anwenden von Updates auf das Bild</span><span class="sxs-lookup"><span data-stu-id="109e9-111">Apply updates to the image</span></span>](#bkmk-applypatchestovpc)

5.  [<span data-ttu-id="109e9-112">Installieren von Integrationskomponenten</span><span class="sxs-lookup"><span data-stu-id="109e9-112">Install Integration Components</span></span>](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="109e9-113">Erstellen eines Windows Virtual PC-Bilds</span><span class="sxs-lookup"><span data-stu-id="109e9-113">Creating a Windows Virtual PC Image</span></span>


<span data-ttu-id="109e9-114">Informationen zum Erstellen eines Windows Virtual PC-Bilds finden Sie in der Windows Virtual PC-Dokumentation:</span><span class="sxs-lookup"><span data-stu-id="109e9-114">To create a Windows Virtual PC image, see the Windows Virtual PC documentation:</span></span>

-   <span data-ttu-id="109e9-115">[Startseite für Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .</span><span class="sxs-lookup"><span data-stu-id="109e9-115">[Windows Virtual PC Home Page](https://go.microsoft.com/fwlink/?LinkId=148103) (https://go.microsoft.com/fwlink/?LinkId=148103).</span></span>

-   <span data-ttu-id="109e9-116">[Hilfe zu Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="109e9-116">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="109e9-117">Wenn Sie bereits über eine Windows Imaging-Datei (WIM) verfügen, die Sie als Grundlage für Ihr virtuelles Bild verwenden möchten, können Sie Sie alternativ in eine VHD konvertieren, die Sie zum Erstellen des MED-V-Arbeitsbereichs verwenden.</span><span class="sxs-lookup"><span data-stu-id="109e9-117">Alternately, if you already have a Windows Imaging (WIM) file that you want to use as the basis for your virtual image, you can convert it to a VHD that you use to build the MED-V workspace.</span></span> <span data-ttu-id="109e9-118">Weitere Informationen zum Konvertieren einer WIM auf eine virtuelle Festplatte finden Sie unter [Unterstützung für Native VHD in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .</span><span class="sxs-lookup"><span data-stu-id="109e9-118">For more information about how to convert a WIM to a virtual hard disk, see [Native VHD Support in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) (https://go.microsoft.com/fwlink/?LinkId=195922).</span></span>

<span data-ttu-id="109e9-119">**Wichtig**  MED-V unterstützt nur eine virtuelle Festplatte pro virtuellen Computer und nur eine Partition auf jedem virtuellen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="109e9-119">**Important** MED-V only supports one virtual hard disk per virtual machine and only one partition on each virtual disk.</span></span>

 

<span data-ttu-id="109e9-120">Nachdem Sie Ihre virtuelle Festplatte erstellt haben, installieren Sie Windows XP auf dem Bild.</span><span class="sxs-lookup"><span data-stu-id="109e9-120">After you have created your virtual hard disk, install Windows XP on the image.</span></span>

## <a href="" id="bkmk-installingwindowsxpontovpc"></a><span data-ttu-id="109e9-121">Installieren von Windows XP auf einem Windows Virtual PC-Abbild</span><span class="sxs-lookup"><span data-stu-id="109e9-121">Installing Windows XP on a Windows Virtual PC Image</span></span>


<span data-ttu-id="109e9-122">Für med-v muss Windows XP SP3 auf dem Windows Virtual PC-Abbild installiert sein, bevor Sie den Med-v-Arbeitsbereich erstellen.</span><span class="sxs-lookup"><span data-stu-id="109e9-122">MED-V requires that Windows XP SP3 is installed on the Windows Virtual PC image before you build the MED-V workspace.</span></span>

<span data-ttu-id="109e9-123">Weitere Informationen zum Installieren von Windows XP finden Sie unter [Erstellen eines virtuellen Computers und Installieren eines Gastbetriebssystems](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .</span><span class="sxs-lookup"><span data-stu-id="109e9-123">For more information about how to install Windows XP, see [Create a virtual machine and install a guest operating system](https://go.microsoft.com/fwlink/?LinkId=182379) (https://go.microsoft.com/fwlink/?LinkId=182379).</span></span>

## <a href="" id="bkmk-installingnet"></a><span data-ttu-id="109e9-124">Installieren von .NET Framework 3,5 SP1 auf einem Windows Virtual PC-Abbild</span><span class="sxs-lookup"><span data-stu-id="109e9-124">Installing the .NET Framework 3.5 SP1 on a Windows Virtual PC Image</span></span>


<span data-ttu-id="109e9-125">Sie müssen .NET Framework 3,5 SP1 und das Update KB959209 manuell in das Windows Virtual PC-Abbild installieren, das Sie für die Verwendung mit MED-V vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="109e9-125">You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="109e9-126">Das Update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) behebt verschiedene bekannte Anwendungskompatibilitätsprobleme.</span><span class="sxs-lookup"><span data-stu-id="109e9-126">The update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950) addresses several known application compatibility issues.</span></span>

## <a href="" id="bkmk-applypatchestovpc"></a><span data-ttu-id="109e9-127">Anwenden von Updates auf das Windows Virtual PC-Abbild</span><span class="sxs-lookup"><span data-stu-id="109e9-127">Applying Updates to the Windows Virtual PC Image</span></span>


<span data-ttu-id="109e9-128">Nachdem Sie Windows XP auf dem virtuellen Computer installiert haben, installieren Sie alle erforderlichen Windows XP-Updates auf dem Bild, wie etwa SP3.</span><span class="sxs-lookup"><span data-stu-id="109e9-128">After you have installed Windows XP on your virtual machine, install any required Windows XP updates on the image, such as SP3.</span></span> <span data-ttu-id="109e9-129">Sie können auch bestimmte optionale Updates installieren, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="109e9-129">You can also install certain optional updates for better performance.</span></span>

<span data-ttu-id="109e9-130">**Wichtig**  Für MED-V muss Windows XP SP3 auf dem Gastbetriebssystem ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="109e9-130">**Important** MED-V requires that Windows XP SP3 be running on the guest operating system.</span></span>

 

<span data-ttu-id="109e9-131">**Warnung**  Wenn Sie Updates für Windows XP installieren, stellen Sie sicher, dass Sie die Version von Internet Explorer in dem Gast verbleiben, den Sie im MED-V-Arbeitsbereich verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="109e9-131">**Warning** When you install updates to Windows XP, make sure that you remain on the version of Internet Explorer in the guest that you intend to use in the MED-V workspace.</span></span> <span data-ttu-id="109e9-132">Wenn Sie beispielsweise Internet Explorer 6 im MED-V-Arbeitsbereich ausführen möchten, stellen Sie sicher, dass alle Updates, die Sie jetzt installieren, nicht mit Internet Explorer 7 oder Internet Explorer 8 verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="109e9-132">For example, if you intend to run Internet Explorer 6 in the MED-V workspace, make sure that any updates that you install now do not include Internet Explorer 7 or Internet Explorer 8.</span></span> <span data-ttu-id="109e9-133">Darüber hinaus empfiehlt es sich, die Registrierung zu konfigurieren, um zu verhindern, dass automatische Updates Internet Explorer aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="109e9-133">In addition, we recommend that you configure the registry to prevent automatic updates from upgrading Internet Explorer.</span></span>

 

### <span data-ttu-id="109e9-134">Installieren eines optionalen Leistungsupdates</span><span class="sxs-lookup"><span data-stu-id="109e9-134">Installing an Optional Performance Update</span></span>

<span data-ttu-id="109e9-135">Obwohl dies optional ist, empfehlen wir, dass Sie das folgende Update für [Hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) .</span><span class="sxs-lookup"><span data-stu-id="109e9-135">Although it is optional, we recommend that you install the following update for [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) (https://go.microsoft.com/fwlink/?LinkId=201077).</span></span> <span data-ttu-id="109e9-136">Dieses Update verbessert die Leistung von freigegebenen Ordnern in einer Terminaldienstesitzung:</span><span class="sxs-lookup"><span data-stu-id="109e9-136">This update increases the performance of shared folders in a Terminal Services session:</span></span>

<span data-ttu-id="109e9-137">**Hinweis**  Das Update ist öffentlich verfügbar.</span><span class="sxs-lookup"><span data-stu-id="109e9-137">**Note** The update is publicly available.</span></span> <span data-ttu-id="109e9-138">Möglicherweise werden Sie jedoch aufgefordert, eine Vereinbarung für Microsoft-Dienste zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="109e9-138">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="109e9-139">Folgen Sie den Anweisungen auf den nachfolgenden Webseiten, um diesen Hotfix abzurufen.</span><span class="sxs-lookup"><span data-stu-id="109e9-139">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>

 

### <span data-ttu-id="109e9-140">Konfigurieren einer Leistungs Aktualisierung für Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="109e9-140">Configuring a Group Policy Performance Update</span></span>

<span data-ttu-id="109e9-141">Standardmäßig wird die Gruppenrichtlinie jeweils um ein Byte auf einen Computer heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="109e9-141">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="109e9-142">Dies verursacht Verzögerungen, während MED-V zur Domäne hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="109e9-142">This causes delays while MED-V is being joined to the domain.</span></span> <span data-ttu-id="109e9-143">Wenn Sie die Leistung von Gruppenrichtlinien erhöhen möchten, setzen Sie den folgenden Registrierungsschlüsselwert auf die Registrierung:</span><span class="sxs-lookup"><span data-stu-id="109e9-143">To increase the performance of Group Policy, set the following registry key value to the registry:</span></span>

<span data-ttu-id="109e9-144">Registrierungsunterschlüssel: HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="109e9-144">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="109e9-145">Eintrag: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="109e9-145">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="109e9-146">Geben Sie Folgendes ein: DWORD</span><span class="sxs-lookup"><span data-stu-id="109e9-146">Type: DWORD</span></span>

<span data-ttu-id="109e9-147">Wert: 1</span><span class="sxs-lookup"><span data-stu-id="109e9-147">Value: 1</span></span>

## <a href="" id="bkmk-installintegration"></a><span data-ttu-id="109e9-148">Installieren von Integrationskomponenten</span><span class="sxs-lookup"><span data-stu-id="109e9-148">Installing Integration Components</span></span>


<span data-ttu-id="109e9-149">Windows Virtual PC enthält das Integrationskomponenten-Paket.</span><span class="sxs-lookup"><span data-stu-id="109e9-149">Windows Virtual PC includes the Integration Components package.</span></span> <span data-ttu-id="109e9-150">Dies bietet Funktionen, die die Interaktion zwischen der virtuellen Umgebung und dem physikalischen Computer verbessern.</span><span class="sxs-lookup"><span data-stu-id="109e9-150">This provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="109e9-151">So können Sie beispielsweise mit dem Integrationskomponenten-Paket die Maus zwischen dem Host und den Gastcomputern bewegen.</span><span class="sxs-lookup"><span data-stu-id="109e9-151">For example, the Integration Components package lets your mouse move between the host and the guest computers.</span></span>

<span data-ttu-id="109e9-152">**Wichtig**  Für MED-V ist die Installation des Integrationskomponentenpakets erforderlich.</span><span class="sxs-lookup"><span data-stu-id="109e9-152">**Important** MED-V requires the installation of the Integration Components package.</span></span>

 

<span data-ttu-id="109e9-153">Wenn Sie das virtuelle Bild für die Zusammenarbeit mit MED-V konfigurieren, müssen Sie das Integrationskomponenten-Paket manuell auf dem Gastbetriebssystem installieren, um die verfügbaren Integrationsfeatures zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="109e9-153">When you configure the virtual image to work with MED-V, you must manually install the Integration Components package on the guest operating system to make the integration features that are available.</span></span>

<span data-ttu-id="109e9-154">Weitere Informationen zum Installieren und Verwenden des Integrationskomponentenpakets finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="109e9-154">For more information about how to install and use the Integration Components package, see the following:</span></span>

-   <span data-ttu-id="109e9-155">[Installieren oder Aktualisieren des Integrationskomponentenpakets](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .</span><span class="sxs-lookup"><span data-stu-id="109e9-155">[Install or Upgrade the Integration Components Package](https://go.microsoft.com/fwlink/?LinkId=195923) (https://go.microsoft.com/fwlink/?LinkId=195923).</span></span>

-   <span data-ttu-id="109e9-156">[Informationen zu Integrations Features](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .</span><span class="sxs-lookup"><span data-stu-id="109e9-156">[About Integration Features](https://go.microsoft.com/fwlink/?LinkId=195924) (https://go.microsoft.com/fwlink/?LinkId=195924).</span></span>

### <span data-ttu-id="109e9-157">Installieren der RemoteApp-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="109e9-157">Installing RemoteApp Update</span></span>

<span data-ttu-id="109e9-158">Nachdem Sie das Integrationskomponenten-Paket installiert haben, werden Sie aufgefordert, das folgende Update zu installieren: "Update für Windows XP SP3 zum Aktivieren von RemoteApp".</span><span class="sxs-lookup"><span data-stu-id="109e9-158">After you install the Integration Components package, you are prompted to install the following update: "Update for Windows XP SP3 to enable RemoteApp."</span></span> <span data-ttu-id="109e9-159">Dies ist eine erforderliche Komponente für MED-V.</span><span class="sxs-lookup"><span data-stu-id="109e9-159">This is a required component for MED-V.</span></span>

<span data-ttu-id="109e9-160">**Wichtig**  Wenn Sie nicht aufgefordert werden, das RemoteApp-Update zu installieren, müssen Sie es manuell herunterladen und installieren.</span><span class="sxs-lookup"><span data-stu-id="109e9-160">**Important** If you are not prompted to install the RemoteApp update, you must download and install it manually.</span></span> <span data-ttu-id="109e9-161">Weitere Informationen und Anweisungen zum Herunterladen dieses Updates finden Sie unter [Update für Windows XP SP3 zum Aktivieren von RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) ( https://go.microsoft.com/fwlink/?LinkId=195925) .</span><span class="sxs-lookup"><span data-stu-id="109e9-161">For more information and instructions about how to download this update, see [Update for Windows XP SP3 to enable RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) (https://go.microsoft.com/fwlink/?LinkId=195925).</span></span>

 

### <span data-ttu-id="109e9-162">Aktivieren von Remote Desktop</span><span class="sxs-lookup"><span data-stu-id="109e9-162">Enabling Remote Desktop</span></span>

<span data-ttu-id="109e9-163">Standardmäßig ist der Remote Desktop nach der Installation des Integrationskomponentenpakets aktiviert.</span><span class="sxs-lookup"><span data-stu-id="109e9-163">By default, Remote Desktop is enabled after you install the Integration Components package.</span></span> <span data-ttu-id="109e9-164">Damit MED-V funktionsfähig ist, stellen Sie sicher, dass der Remote Desktop aktiviert ist, und verteilen Sie keine Gruppenrichtlinien, die ihn deaktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="109e9-164">For MED-V to be operational, ensure that Remote Desktop is enabled, and do not distribute any Group Policy that disables it.</span></span>

<span data-ttu-id="109e9-165">Informationen zum Aktivieren von Remote Desktop finden Sie unter [Aktivieren oder Deaktivieren von Remote Desktop](https://go.microsoft.com/fwlink/?LinkId=201162) ( https://go.microsoft.com/fwlink/?LinkId=201162) .</span><span class="sxs-lookup"><span data-stu-id="109e9-165">For information about how to enable Remote Desktop, see [Enable or disable Remote Desktop](https://go.microsoft.com/fwlink/?LinkId=201162) (https://go.microsoft.com/fwlink/?LinkId=201162).</span></span>

## <span data-ttu-id="109e9-166">Anpassen von Internet Explorer mit dem Internet Explorer-Verwaltungskit</span><span class="sxs-lookup"><span data-stu-id="109e9-166">Customizing Internet Explorer by Using the Internet Explorer Administration Kit</span></span>


<span data-ttu-id="109e9-167">Wenn Sie möchten, können Sie Internet Explorer mit dem Internet Explorer-Verwaltungskit auf dem Gastbetriebssystem anpassen.</span><span class="sxs-lookup"><span data-stu-id="109e9-167">If you want, you can use the Internet Explorer Administration Kit to customize Internet Explorer on the guest operating system.</span></span> <span data-ttu-id="109e9-168">Weitere Informationen finden Sie im [Internet Explorer 6-Administrations-Kit und im Bereitstellungshandbuch](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?linkid=200007).</span><span class="sxs-lookup"><span data-stu-id="109e9-168">For more information, see the [Internet Explorer 6 Administration Kit and Deployment Guide](https://go.microsoft.com/fwlink/?LinkId=200007) (http:// go.microsoft.com/fwlink/?LinkId=200007).</span></span>

<span data-ttu-id="109e9-169">**Warnung**  Bedenken Sie die Sicherheitsaspekte, die mit dem Anpassen von Internet Explorer im MED-V-Arbeitsbereich verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="109e9-169">**Warning** You should consider security concerns associated with customizing Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="109e9-170">Weitere Informationen finden Sie unter [bewährte Methoden für die Sicherheit von MED-V-Vorgängen](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="109e9-170">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>

 

<span data-ttu-id="109e9-171">Nachdem die virtuelle Festplatte mit einem aktuellen Gastbetriebssystem installiert wurde, können Sie Anwendungen auf dem Bild installieren.</span><span class="sxs-lookup"><span data-stu-id="109e9-171">After your virtual hard disk is installed with an up-to-date guest operating system, you can install applications on the image.</span></span>

## <span data-ttu-id="109e9-172">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="109e9-172">Related topics</span></span>


[<span data-ttu-id="109e9-173">Installieren von Anwendungen auf einem virtuellen Windows-PC-Image</span><span class="sxs-lookup"><span data-stu-id="109e9-173">Installing Applications on a Windows Virtual PC Image</span></span>](installing-applications-on-a-windows-virtual-pc-image.md)

[<span data-ttu-id="109e9-174">Konfigurieren eines virtuellen Windows-PC-Images für MED-V</span><span class="sxs-lookup"><span data-stu-id="109e9-174">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





