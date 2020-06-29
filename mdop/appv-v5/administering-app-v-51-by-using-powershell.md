---
title: Verwalten von App-V 5.1 mithilfe von PowerShell
description: Verwalten von App-V 5.1 mithilfe von PowerShell
author: dansimp
ms.assetid: 9e10ff07-2cd9-4dc1-9e99-582f90c36081
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0c64d7e0330ff5d737dfa02d87f156cc3236b04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806053"
---
# <span data-ttu-id="4f5c1-103">Verwalten von App-V 5.1 mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f5c1-103">Administering App-V 5.1 by Using PowerShell</span></span>


<span data-ttu-id="4f5c1-104">Microsoft Application Virtualization (app-v) 5,1 bietet Windows PowerShell-Cmdlets, mit deren Hilfe Administratoren verschiedene App-v 5,1-Aufgaben ausführen können.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-104">Microsoft Application Virtualization (App-V) 5.1 provides Windows PowerShell cmdlets, which can help administrators perform various App-V 5.1 tasks.</span></span> <span data-ttu-id="4f5c1-105">Die folgenden Abschnitte enthalten weitere Informationen zur Verwendung von PowerShell mit App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-105">The following sections provide more information about using PowerShell with App-V 5.1.</span></span>

## <span data-ttu-id="4f5c1-106">Verwalten von App-V 5,1 mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f5c1-106">How to administer App-V 5.1 by using PowerShell</span></span>


<span data-ttu-id="4f5c1-107">Verwenden Sie die folgenden PowerShell-Verfahren, um verschiedene App-V 5,1-Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-107">Use the following PowerShell procedures to perform various App-V 5.1 tasks.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4f5c1-108">Name</span><span class="sxs-lookup"><span data-stu-id="4f5c1-108">Name</span></span></th>
<th align="left"><span data-ttu-id="4f5c1-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f5c1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md" data-raw-source="[How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md)"><span data-ttu-id="4f5c1-110">So laden Sie die PowerShell-Cmdlets und rufen die Cmdlet-Hilfe auf</span><span class="sxs-lookup"><span data-stu-id="4f5c1-110">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-111">Es wird beschrieben, wie Sie die PowerShell-Cmdlets installieren und die Hilfe und Beispiele für das Cmdlet finden.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-111">Describes how to install the PowerShell cmdlets and find cmdlet help and examples.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="4f5c1-112">So verwalten Sie App-V 5.1-Pakete auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f5c1-112">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-113">Beschreibt, wie Sie den Clientpaket-Lebenszyklus auf einem eigenständigen Computer mithilfe von PowerShell verwalten.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-113">Describes how to manage the client package lifecycle on a stand-alone computer using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md)"><span data-ttu-id="4f5c1-114">So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f5c1-114">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-115">Beschreibt, wie Verbindungsgruppen mithilfe von PowerShell verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-115">Describes how to manage connection groups using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-modify-client-configuration-by-using-powershell51.md" data-raw-source="[How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell51.md)"><span data-ttu-id="4f5c1-116">So ändern Sie die Client-Konfiguration mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f5c1-116">How to Modify Client Configuration by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-117">Beschreibt, wie der Client mithilfe von PowerShell geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-117">Describes how to modify the client using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-apply-the-user-configuration-file-by-using-powershell51.md" data-raw-source="[How to Apply the User Configuration File by Using PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)"><span data-ttu-id="4f5c1-118">So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an</span><span class="sxs-lookup"><span data-stu-id="4f5c1-118">How to Apply the User Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-119">Beschreibt, wie eine Benutzerkonfigurationsdatei mithilfe von PowerShell angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-119">Describes how to apply a user configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-apply-the-deployment-configuration-file-by-using-powershell51.md" data-raw-source="[How to Apply the Deployment Configuration File by Using PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)"><span data-ttu-id="4f5c1-120">Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an</span><span class="sxs-lookup"><span data-stu-id="4f5c1-120">How to Apply the Deployment Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-121">Beschreibt, wie eine Bereitstellungs Konfigurationsdatei mithilfe von PowerShell angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-121">Describes how to apply a deployment configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-sequence-a-package--by-using-powershell-51.md" data-raw-source="[How to Sequence a Package by Using PowerShell](how-to-sequence-a-package--by-using-powershell-51.md)"><span data-ttu-id="4f5c1-122">Sequenzierung eines Pakets mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f5c1-122">How to Sequence a Package by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-123">Beschreibt, wie Sie mithilfe von PowerShell ein neues Paket erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-123">Describes how to create a new package using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-package-accelerator-by-using-powershell51.md" data-raw-source="[How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md)"><span data-ttu-id="4f5c1-124">So erstellen Sie einen Package Accelerator mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f5c1-124">How to Create a Package Accelerator by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-125">Beschreibt, wie ein Paket Beschleuniger mithilfe von PowerShell erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-125">Describes how to create a package accelerator using PowerShell.</span></span> <span data-ttu-id="4f5c1-126">Sie können Paket Beschleuniger verwenden, um große, komplexe Anwendungen automatisch zu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-126">You can use package accelerators automatically sequence large, complex applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md" data-raw-source="[How to Enable Reporting on the App-V 5.1 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)"><span data-ttu-id="4f5c1-127">So aktivieren Sie die Berichterstellung auf dem App-V 5.1-Client mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f5c1-127">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-128">Beschreibt, wie der Computer, auf dem die App-V 5,1 ausgeführt wird, Bericht Erstellungsinformationen senden kann.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-128">Describes how to enable the computer running the App-V 5.1 to send reporting information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md" data-raw-source="[How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md)"><span data-ttu-id="4f5c1-129">Installieren der App-V-Datenbanken und Konvertieren der zugehörigen Sicherheitsbezeichner mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f5c1-129">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-130">Beschreibt, wie Sie eine Reihe von Kontonamen erstellen und diese in die entsprechende SID in Standard-und hexadezimal Formaten konvertieren können.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-130">Describes how to take an array of account names and to convert each of them to the corresponding SID in standard and hexadecimal formats.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4f5c1-131">**Wichtig**  Stellen Sie sicher, dass alle Skripts, die Sie mit ihren App-V-Paketen ausführen, mit der Ausführungsrichtlinie übereinstimmen, die Sie für PowerShell konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-131">**Important** Make sure that any script you execute with your App-V packages matches the execution policy that you have configured for PowerShell.</span></span>

 

## <span data-ttu-id="4f5c1-132">PowerShell-Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="4f5c1-132">PowerShell Error Handling</span></span>


<span data-ttu-id="4f5c1-133">Verwenden Sie die folgende Tabelle, um Informationen zur Fehlerbehandlung der App-V 5,1 PowerShell zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4f5c1-133">Use the following table for information about App-V 5.1 PowerShell error handling.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4f5c1-134">Ereignis</span><span class="sxs-lookup"><span data-stu-id="4f5c1-134">Event</span></span></th>
<th align="left"><span data-ttu-id="4f5c1-135">Aktion</span><span class="sxs-lookup"><span data-stu-id="4f5c1-135">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f5c1-136">Verwenden des RollbackOnError-Attributs mit eingebetteten Skripts</span><span class="sxs-lookup"><span data-stu-id="4f5c1-136">Using the RollbackOnError attribute with embedded scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-137">Wenn Sie das <strong> RollbackOnError </strong> -Attribut mit eingebetteten Skripts verwenden, wird das Attribut für die folgenden Ereignisse ignoriert:</span><span class="sxs-lookup"><span data-stu-id="4f5c1-137">When you use the <strong>RollbackOnError</strong> attribute with embedded scripts, the attribute is ignored for the following events:</span></span></p>
<ul>
<li><p><span data-ttu-id="4f5c1-138">Entfernen eines Pakets</span><span class="sxs-lookup"><span data-stu-id="4f5c1-138">Removing a package</span></span></p></li>
<li><p><span data-ttu-id="4f5c1-139">Aufheben der Veröffentlichung eines Pakets</span><span class="sxs-lookup"><span data-stu-id="4f5c1-139">Unpublishing a package</span></span></p></li>
<li><p><span data-ttu-id="4f5c1-140">Beenden einer virtuellen Umgebung</span><span class="sxs-lookup"><span data-stu-id="4f5c1-140">Terminating a virtual environment</span></span></p></li>
<li><p><span data-ttu-id="4f5c1-141">Beenden eines Prozesses</span><span class="sxs-lookup"><span data-stu-id="4f5c1-141">Terminating a process</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f5c1-142">Der Paket Name enthält<strong>$</span><span class="sxs-lookup"><span data-stu-id="4f5c1-142">Package name contains <strong>$</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4f5c1-143">Wenn ein Paketname das Zeichen ( <strong> $ </strong> ) enthält, müssen Sie ein einfaches Anführungszeichen ( <strong> ") verwenden </strong> , beispielsweise</span><span class="sxs-lookup"><span data-stu-id="4f5c1-143">If a package name contains the character ( <strong>$</strong> ), you must use a single-quote ( <strong>‘</strong> ), for example,</span></span></p>
<p><strong><span data-ttu-id="4f5c1-144">Add-AppvClientPackage "Contoso $ app. AppV"</span><span class="sxs-lookup"><span data-stu-id="4f5c1-144">Add-AppvClientPackage ‘Contoso$App.appv’</span></span></strong></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="4f5c1-145">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4f5c1-145">Related topics</span></span>


[<span data-ttu-id="4f5c1-146">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4f5c1-146">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





