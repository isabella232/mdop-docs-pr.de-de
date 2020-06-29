---
title: Bereitstellen von Microsoft Office2013 mit App-V
description: Bereitstellen von Microsoft Office2013 mit App-V
author: dansimp
ms.assetid: 9a7be05e-2a7a-4874-af25-09c0f5037876
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: f6a54cadce79ff3680fd69206eba8ac3fbe83a68
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805870"
---
# <span data-ttu-id="3edb4-103">Bereitstellen von Microsoft Office2013 mit App-V</span><span class="sxs-lookup"><span data-stu-id="3edb4-103">Deploying Microsoft Office 2013 by Using App-V</span></span>


<span data-ttu-id="3edb4-104">Verwenden Sie die Informationen in diesem Artikel, um Microsoft Application Virtualization (App-V) 5,1 oder höhere Versionen zu verwenden, um Microsoft Office 2013 als virtualisierte Anwendung an Computer in Ihrer Organisation zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="3edb4-104">Use the information in this article to use Microsoft Application Virtualization (App-V) 5.1, or later versions, to deliver Microsoft Office 2013 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="3edb4-105">Informationen zum Verwenden von App-v für die Bereitstellung von Office 2010 finden Sie unter [Bereitstellen von Microsoft Office 2010 mithilfe von App-v](deploying-microsoft-office-2010-by-using-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="3edb4-105">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v51.md).</span></span> <span data-ttu-id="3edb4-106">Damit Sie Office 2013 mit App-v erfolgreich bereitstellen können, müssen Sie mit Office 2013 und App-v vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="3edb4-106">To successfully deploy Office 2013 with App-V, you need to be familiar with Office 2013 and App-V.</span></span>

<span data-ttu-id="3edb4-107">Dieses Thema enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="3edb4-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3edb4-108">Was Sie wissen sollten, bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="3edb4-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="3edb4-109">Erstellen eines Office 2013-Pakets für App-V mit dem Office-Bereitstellungs Tool</span><span class="sxs-lookup"><span data-stu-id="3edb4-109">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="3edb4-110">Veröffentlichen des Office-Pakets für App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3edb4-110">Publishing the Office package for App-V 5.1</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="3edb4-111">Anpassen und Verwalten von Office App-V-Paketen</span><span class="sxs-lookup"><span data-stu-id="3edb4-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="3edb4-112">Was Sie wissen sollten, bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="3edb4-112">What to know before you start</span></span>


<span data-ttu-id="3edb4-113">Bevor Sie Office 2013 mithilfe von App-V bereitstellen, sollten Sie die folgenden Planungsinformationen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-113">Before you deploy Office 2013 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="3edb4-114">Unterstützte Office-Versionen und Office-Koexistenz</span><span class="sxs-lookup"><span data-stu-id="3edb4-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="3edb4-115">Verwenden Sie die folgende Tabelle, um Informationen zu unterstützten Versionen von Office und zum Ausführen von nebeneinander vorhandenen Versionen von Office zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3edb4-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3edb4-116">Zu überprüfende Informationen</span><span class="sxs-lookup"><span data-stu-id="3edb4-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="3edb4-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3edb4-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office51.md#bkmk-office-vers-supp-appv" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office51.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="3edb4-118">Planen der Verwendung von App-V mit Office</span><span class="sxs-lookup"><span data-stu-id="3edb4-118">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3edb4-119">Unterstützte Office-Versionen</span><span class="sxs-lookup"><span data-stu-id="3edb4-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="3edb4-120">Unterstützte Bereitstellungstypen (beispielsweise Desktop, Personal Virtual Desktop Infrastructure (VDI), gebündelter VDI)</span><span class="sxs-lookup"><span data-stu-id="3edb4-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="3edb4-121">Office-Lizenzierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="3edb4-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office51.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office51.md#bkmk-plan-coexisting)"><span data-ttu-id="3edb4-122">Planen der Verwendung von App-V mit Office</span><span class="sxs-lookup"><span data-stu-id="3edb4-122">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="3edb4-123">Überlegungen zum Installieren verschiedener Office-Versionen auf demselben Computer</span><span class="sxs-lookup"><span data-stu-id="3edb4-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>


### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="3edb4-124">Anforderungen für das Verpacken, veröffentlichen und bereitstellen</span><span class="sxs-lookup"><span data-stu-id="3edb4-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="3edb4-125">Bevor Sie Office mithilfe von App-V bereitstellen, überprüfen Sie die folgenden Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3edb4-126">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3edb4-126">Task</span></span></th>
<th align="left"><span data-ttu-id="3edb4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3edb4-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3edb4-128">Verpacken</span><span class="sxs-lookup"><span data-stu-id="3edb4-128">Packaging</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3edb4-129">Alle Office-Anwendungen, die Sie für Benutzer bereitstellen möchten, müssen sich in einem einzigen Paket befinden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="3edb4-130">In App-V 5,1 und höher müssen Sie das Office-Bereitstellungs Tool verwenden, um Pakete zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-130">In App-V 5.1 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="3edb4-131">Sie können den Sequencer nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="3edb4-132">Wenn Sie Microsoft Visio 2013 und Microsoft Project 2013 zusammen mit Office bereitstellen, müssen Sie diese in das gleiche Paket mit Office einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-132">If you are deploying Microsoft Visio 2013 and Microsoft Project 2013 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="3edb4-133">Weitere Informationen finden Sie unter <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)"> Bereitstellen von Visio 2013 und Project 2013 mit Office </a> .</span><span class="sxs-lookup"><span data-stu-id="3edb4-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2013 and Project 2013 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3edb4-134">Publishing</span><span class="sxs-lookup"><span data-stu-id="3edb4-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3edb4-135">Sie können auf jedem Clientcomputer nur ein Office-Paket veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="3edb4-136">Sie müssen das Office-Paket Global veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-136">You must publish the Office package globally.</span></span> <span data-ttu-id="3edb4-137">Sie können nicht für den Benutzer veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3edb4-138">Bereitstellen eines der folgenden Produkte auf einem freigegebenen Computer, beispielsweise mithilfe von Remote Desktop Diensten:</span><span class="sxs-lookup"><span data-stu-id="3edb4-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="3edb4-139">Microsoft 365-Apps für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="3edb4-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="3edb4-140">Visio pro für Office 365</span><span class="sxs-lookup"><span data-stu-id="3edb4-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="3edb4-141">Project pro für Office 365</span><span class="sxs-lookup"><span data-stu-id="3edb4-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="3edb4-142">Sie müssen die <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> Aktivierung gemeinsam genutzter Computer aktivieren </a> .</span><span class="sxs-lookup"><span data-stu-id="3edb4-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
<p><span data-ttu-id="3edb4-143">Wenn Sie ein Volumen lizenziertes Produkt bereitstellen, verwenden Sie keine freigegebene Computeraktivierung, wie beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="3edb4-143">You don’t use shared computer activation if you’re deploying a volume licensed product, such as:</span></span></p>
<ul>
<li><p><span data-ttu-id="3edb4-144">Office Professional Plus 2013</span><span class="sxs-lookup"><span data-stu-id="3edb4-144">Office Professional Plus 2013</span></span></p></li>
<li><p><span data-ttu-id="3edb4-145">Visio Professional 2013</span><span class="sxs-lookup"><span data-stu-id="3edb4-145">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="3edb4-146">Project Professional 2013</span><span class="sxs-lookup"><span data-stu-id="3edb4-146">Project Professional 2013</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="3edb4-147">Ausschließen von Office-Anwendungen aus einem Paket</span><span class="sxs-lookup"><span data-stu-id="3edb4-147">Excluding Office applications from a package</span></span>

<span data-ttu-id="3edb4-148">In der folgenden Tabelle werden die empfohlenen Methoden zum Ausschließen bestimmter Office-Anwendungen aus einem Paket beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3edb4-148">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3edb4-149">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3edb4-149">Task</span></span></th>
<th align="left"><span data-ttu-id="3edb4-150">Details</span><span class="sxs-lookup"><span data-stu-id="3edb4-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3edb4-151">Verwenden <strong> Sie die ExcludeApp </strong> -Einstellung, wenn Sie das Paket mithilfe des Office-Bereitstellungstools erstellen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-151">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3edb4-152">Ermöglicht das Ausschließen bestimmter Office-Anwendungen aus dem Paket, wenn das Office-Bereitstellungs Tool das Paket erstellt.</span><span class="sxs-lookup"><span data-stu-id="3edb4-152">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="3edb4-153">Mit dieser Einstellung können Sie beispielsweise ein Paket erstellen, das nur Microsoft Word enthält.</span><span class="sxs-lookup"><span data-stu-id="3edb4-153">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="3edb4-154">Weitere Informationen finden Sie unter <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> ExcludeApp-Element </a> .</span><span class="sxs-lookup"><span data-stu-id="3edb4-154">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3edb4-155">Ändern der DeploymentConfig.xml Datei</span><span class="sxs-lookup"><span data-stu-id="3edb4-155">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3edb4-156">Ändern Sie die DeploymentConfig.xml-Datei, nachdem das Paket erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3edb4-156">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="3edb4-157">Diese Datei enthält die Standardpaket Einstellungen für alle Benutzer auf einem Computer, auf dem der App-V-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3edb4-157">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="3edb4-158">Weitere Informationen finden Sie unter <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)"> Deaktivieren von Office 2013-Anwendungen </a> .</span><span class="sxs-lookup"><span data-stu-id="3edb4-158">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)">Disabling Office 2013 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="3edb4-159">Erstellen eines Office 2013-Pakets für App-V mit dem Office-Bereitstellungs Tool</span><span class="sxs-lookup"><span data-stu-id="3edb4-159">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="3edb4-160">Führen Sie die folgenden Schritte aus, um ein Office 2013-Paket für App-V 5,1 oder höher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-160">Complete the following steps to create an Office 2013 package for App-V 5.1 or later.</span></span>

**<span data-ttu-id="3edb4-161">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3edb4-161">Important</span></span>**  
<span data-ttu-id="3edb4-162">In App-V 5,1 und höher müssen Sie das Office-Bereitstellungs Tool zum Erstellen eines Pakets einrichten.</span><span class="sxs-lookup"><span data-stu-id="3edb4-162">In App-V 5.1 and later, you must the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="3edb4-163">Sie können den Sequencer nicht zum Erstellen von Paketen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-163">You cannot use the Sequencer to create packages.</span></span>



### <span data-ttu-id="3edb4-164">Überprüfen der Voraussetzungen für die Verwendung des Office-Bereitstellungstools</span><span class="sxs-lookup"><span data-stu-id="3edb4-164">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="3edb4-165">Der Computer, auf dem Sie das Office-Bereitstellungs Tool installieren, muss Folgendes aufweisen:</span><span class="sxs-lookup"><span data-stu-id="3edb4-165">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3edb4-166">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="3edb4-166">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="3edb4-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3edb4-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3edb4-168">Erforderliche Software</span><span class="sxs-lookup"><span data-stu-id="3edb4-168">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="3edb4-169">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="3edb4-169">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3edb4-170">Unterstützte Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="3edb4-170">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3edb4-171">64-Bit-Version von Windows 8 oder höher</span><span class="sxs-lookup"><span data-stu-id="3edb4-171">64-bit version of Windows 8 or later</span></span></p></li>
<li><p><span data-ttu-id="3edb4-172">64-Bit-Version von Windows 7</span><span class="sxs-lookup"><span data-stu-id="3edb4-172">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="3edb4-173">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3edb4-173">Note</span></span>**  
<span data-ttu-id="3edb4-174">In diesem Thema bezieht sich der Begriff "Office 2013 App-V-Paket" auf die Abonnementlizenzierung und die Volumenlizenzierung.</span><span class="sxs-lookup"><span data-stu-id="3edb4-174">In this topic, the term “Office 2013 App-V package” refers to subscription licensing and volume licensing.</span></span>



### <span data-ttu-id="3edb4-175">Erstellen von Office 2013-App-V-Paketen mithilfe des Office-Bereitstellungstools</span><span class="sxs-lookup"><span data-stu-id="3edb4-175">Create Office 2013 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="3edb4-176">Sie erstellen Office 2013-App-V-Pakete mithilfe des Office-Bereitstellungstools.</span><span class="sxs-lookup"><span data-stu-id="3edb4-176">You create Office 2013 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="3edb4-177">Die folgenden Anweisungen erläutern, wie Sie ein Office 2013-App-V-Paket mit Volumenlizenzierung oder Abonnementlizenzierung erstellen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-177">The following instructions explain how to create an Office 2013 App-V package with Volume Licensing or Subscription Licensing.</span></span>

<span data-ttu-id="3edb4-178">Erstellen Sie Office 2013-App-V-Pakete auf 64-Bit-Windows-Computern.</span><span class="sxs-lookup"><span data-stu-id="3edb4-178">Create Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="3edb4-179">Nach der Erstellung wird das Office 2013-App-V-Paket auf Computern mit 32-Bit und 64-Bit Windows 7, Windows 8,1 und Windows 10 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3edb4-179">Once created, the Office 2013 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="3edb4-180">Herunterladen des Office-Bereitstellungstools</span><span class="sxs-lookup"><span data-stu-id="3edb4-180">Download the Office Deployment Tool</span></span>

<span data-ttu-id="3edb4-181">Office 2013-App-v-Pakete werden mit dem Office-Bereitstellungs Tool erstellt, das ein Office 2013-App-v-Paket generiert.</span><span class="sxs-lookup"><span data-stu-id="3edb4-181">Office 2013 App-V Packages are created using the Office Deployment Tool, which generates an Office 2013 App-V Package.</span></span> <span data-ttu-id="3edb4-182">Das Paket kann nicht über den App-V-Sequenzer erstellt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-182">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="3edb4-183">So beginnen Sie die Paketerstellung:</span><span class="sxs-lookup"><span data-stu-id="3edb4-183">To begin package creation:</span></span>

1.  <span data-ttu-id="3edb4-184">Laden [Sie das Office-Bereitstellungs Tool für Klick-und-Los](https://www.microsoft.com/download/details.aspx?id=36778)herunter.</span><span class="sxs-lookup"><span data-stu-id="3edb4-184">Download the [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=36778).</span></span>

2.  <span data-ttu-id="3edb4-185">Führen Sie die exe-Datei aus, und extrahieren Sie die zugehörigen Features an den gewünschten Speicherort.</span><span class="sxs-lookup"><span data-stu-id="3edb4-185">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="3edb4-186">Um diesen Vorgang zu vereinfachen, können Sie einen freigegebenen Netzwerkordner erstellen, in dem die Features gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-186">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    <span data-ttu-id="3edb4-187">Beispiel: \\\\Server\\Office2013</span><span class="sxs-lookup"><span data-stu-id="3edb4-187">Example: \\\\Server\\Office2013</span></span>

3.  <span data-ttu-id="3edb4-188">Überprüfen Sie, ob eine setup.exe und eine configuration.xml Datei vorhanden sind und sich an dem von Ihnen angegebenen Speicherort befinden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-188">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="3edb4-189">Herunterladen von Office 2013-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3edb4-189">Download Office 2013 applications</span></span>

<span data-ttu-id="3edb4-190">Nachdem Sie das Office-Bereitstellungs Tool heruntergeladen haben, können Sie es verwenden, um die neuesten Office 2013-Anwendungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3edb4-190">After you download the Office Deployment Tool, you can use it to get the latest Office 2013 applications.</span></span> <span data-ttu-id="3edb4-191">Nachdem Sie die Office-Anwendungen erhalten haben, erstellen Sie das Office 2013-App-V-Paket.</span><span class="sxs-lookup"><span data-stu-id="3edb4-191">After getting the Office applications, you create the Office 2013 App-V package.</span></span>

<span data-ttu-id="3edb4-192">Die im Office-Bereitstellungs Tool enthaltene XML-Datei gibt die Produkt Details an, beispielsweise die enthaltenen Sprachen und Office-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-192">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1.  <span data-ttu-id="3edb4-193">**Passen Sie die Beispiel-XML-Konfigurationsdatei an:** Verwenden Sie die Beispiel-XML-Konfigurationsdatei, die Sie mit dem Office-Bereitstellungs Tool heruntergeladen haben, um die Office-Anwendungen anzupassen:</span><span class="sxs-lookup"><span data-stu-id="3edb4-193">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

    1.  <span data-ttu-id="3edb4-194">Öffnen Sie die XML-Beispieldatei im Editor oder in Ihrem bevorzugten Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="3edb4-194">Open the sample XML file in Notepad or your favorite text editor.</span></span>

    2.  <span data-ttu-id="3edb4-195">Wenn die Beispiel configuration.xml-Datei geöffnet und zur Bearbeitung bereit ist, können Sie Produkte, Sprachen und den Pfad angeben, in dem Sie die Office 2013-Anwendungen speichern.</span><span class="sxs-lookup"><span data-stu-id="3edb4-195">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2013 applications.</span></span> <span data-ttu-id="3edb4-196">Der folgende Code ist ein einfaches Beispiel für die configuration.xml-Datei:</span><span class="sxs-lookup"><span data-stu-id="3edb4-196">The following is a basic example of the configuration.xml file:</span></span>

        ```xml
        <Configuration>
           <Add SourcePath= ”\\Server\Office2013” OfficeClientEdition="32" >
            <Product ID="O365ProPlusRetail ">
              <Language ID="en-us" />
            </Product>
            <Product ID="VisioProRetail">
              <Language ID="en-us" />
            </Product>
          </Add>
        </Configuration>
        ```

        **<span data-ttu-id="3edb4-197">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3edb4-197">Note</span></span>**  
        <span data-ttu-id="3edb4-198">Das Konfigurations-XML ist eine XML-Beispieldatei.</span><span class="sxs-lookup"><span data-stu-id="3edb4-198">The configuration XML is a sample XML file.</span></span> <span data-ttu-id="3edb4-199">Die Datei enthält Zeilen, die auskommentiert werden. Sie können diese Zeilen "kommentieren", um zusätzliche Einstellungen für die Datei anzupassen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-199">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span>



~~~
    The above XML configuration file specifies that Office 2013 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2013, which is the location where Office applications will be saved to. Note that the Product ID of the applications will not affect the final licensing of Office. Office 2013 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage. The table below summarizes the customizable attributes and elements of XML file:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Input</th>
    <th align="left">Description</th>
    <th align="left">Example</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Add element</p></td>
    <td align="left"><p>Specifies the products and languages to include in the package.</p></td>
    <td align="left"><p>N/A</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>OfficeClientEdition (attribute of Add element)</p></td>
    <td align="left"><p>Specifies the edition of Office 2013 product to use: 32-bit or 64-bit. The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</p></td>
    <td align="left"><p><strong>OfficeClientEdition</strong>=&quot;32&quot;</p>
    <p><strong>OfficeClientEdition</strong>=&quot;64&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Product element</p></td>
    <td align="left"><p>Specifies the application. Project 2013 and Visio 2013 must be specified here as an added product to be included in the applications.</p></td>
    <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
    <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
    <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
    <p><code>Product ID =&quot;ProPlusVolume&quot;</code></p>
    <p><code>Product ID =&quot;VisioProVolume&quot;</code></p>
    <p><code>Product ID = &quot;ProjectProVolume&quot;</code></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Language element</p></td>
    <td align="left"><p>Specifies the language supported in the applications</p></td>
    <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Version (attribute of Add element)</p></td>
    <td align="left"><p>Optional. Specifies a build to use for the package</p>
    <p>Defaults to latest advertised build (as defined in v32.CAB at the Office source).</p></td>
    <td align="left"><p><code>15.1.2.3</code></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>SourcePath (attribute of Add element)</p></td>
    <td align="left"><p>Specifies the location in which the applications will be saved to.</p></td>
    <td align="left"><p><code>Sourcepath = &quot;\\Server\Office2013”</code></p></td>
    </tr>
    </tbody>
    </table>



    After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2013 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.
~~~

2. <span data-ttu-id="3edb4-200">**Laden Sie die Anwendungen in den angegebenen Speicherort herunter:** Verwenden Sie eine Eingabeaufforderung mit erhöhten Rechten und ein 64-Bit-Betriebssystem, um die Office 2013-Anwendungen herunterzuladen, die später in ein App-V-Paket konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-200">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2013 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="3edb4-201">Im folgenden finden Sie einen Beispielbefehl mit einer Beschreibung der Details:</span><span class="sxs-lookup"><span data-stu-id="3edb4-201">Below is an example command with description of details:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /download \\server\Office2013\Customconfig.xml
   ```

   <span data-ttu-id="3edb4-202">Im Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3edb4-202">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3edb4-203">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="3edb4-203">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-204">der Speicherort des Netzwerkspeichers, der das Office-Bereitstellungs Tool und die benutzerdefinierte Configuration.xml Datei enthält, Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="3edb4-204">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="3edb4-205">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="3edb4-205">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-206">ist das Office-Bereitstellungs Tool.</span><span class="sxs-lookup"><span data-stu-id="3edb4-206">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3edb4-207">/Download</span><span class="sxs-lookup"><span data-stu-id="3edb4-207">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-208">downloadet die Office 2013-Anwendungen, die Sie in der customConfig.xml-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="3edb4-208">downloads the Office 2013 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="3edb4-209">Diese Bits können später in einem Office 2013-App-V-Paket mit Volumenlizenzierung konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-209">These bits can be later converted in an Office 2013 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="3edb4-210">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="3edb4-210">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-211">übergibt die XML-Konfigurationsdatei, die zum Abschließen des Downloadprozesses erforderlich ist, in diesem Beispiel customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="3edb4-211">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="3edb4-212">Nach Verwendung des Befehls "Download" sollten sich die Office-Anwendungen an dem Speicherort befinden, der in der XML-Konfigurationsdatei angegeben ist, in diesem Beispiel \Server\Office2013.</span><span class="sxs-lookup"><span data-stu-id="3edb4-212">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2013.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="3edb4-213">Konvertieren der Office-Anwendungen in ein App-V-Paket</span><span class="sxs-lookup"><span data-stu-id="3edb4-213">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="3edb4-214">Nachdem Sie die Office 2013-Anwendungen über das Office-Bereitstellungstool heruntergeladen haben, verwenden Sie das Office-Bereitstellungstool, um Sie in ein Office 2013 App-V-Paket umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="3edb4-214">After you download the Office 2013 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2013 App-V package.</span></span> <span data-ttu-id="3edb4-215">Führen Sie die Schritte aus, die Ihrem Lizenzierungsmodell entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-215">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="3edb4-216">Zusammenfassung der erforderlichen Schritte:</span><span class="sxs-lookup"><span data-stu-id="3edb4-216">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="3edb4-217">Erstellen Sie die Office 2013-App-V-Pakete auf 64-Bit-Windows-Computern.</span><span class="sxs-lookup"><span data-stu-id="3edb4-217">Create the Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="3edb4-218">Das Paket wird jedoch auf 32-Bit-und 64-Bit-Computern unter Windows 7, Windows 8 und Windows 10 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3edb4-218">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8, and Windows 10 computers.</span></span>

-   <span data-ttu-id="3edb4-219">Erstellen Sie ein Office App-V-Paket für das Abonnement Lizenzierungs Paket oder die Volumenlizenzierung mithilfe des Office-Bereitstellungstools, und ändern Sie dann die CustomConfig.xml-Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="3edb4-219">Create an Office App-V package for either Subscription Licensing package or Volume Licensing by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="3edb4-220">In der folgenden Tabelle sind die Werte zusammengefasst, die Sie in die CustomConfig.xml-Datei für das verwendete Lizenzierungsmodell eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-220">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="3edb4-221">Die Schritte in den Abschnitten, die der Tabelle folgen, geben die genauen Einträge an, die Sie vornehmen müssen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-221">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3edb4-222">Produkt-ID</span><span class="sxs-lookup"><span data-stu-id="3edb4-222">Product ID</span></span></th>
<th align="left"><span data-ttu-id="3edb4-223">Volumenlizenzierung</span><span class="sxs-lookup"><span data-stu-id="3edb4-223">Volume Licensing</span></span></th>
<th align="left"><span data-ttu-id="3edb4-224">Abonnementlizenzierung</span><span class="sxs-lookup"><span data-stu-id="3edb4-224">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3edb4-225">Office 2013</span><span class="sxs-lookup"><span data-stu-id="3edb4-225">Office 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3edb4-226">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="3edb4-226">ProPlusVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="3edb4-227">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="3edb4-227">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3edb4-228">Office 2013 mit Visio 2013</span><span class="sxs-lookup"><span data-stu-id="3edb4-228">Office 2013 with Visio 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3edb4-229">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="3edb4-229">ProPlusVolume</span></span></p>
<p><span data-ttu-id="3edb4-230">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="3edb4-230">VisioProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="3edb4-231">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="3edb4-231">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="3edb4-232">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="3edb4-232">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3edb4-233">Office 2013 mit Visio 2013 und Project 2013</span><span class="sxs-lookup"><span data-stu-id="3edb4-233">Office 2013 with Visio 2013 and Project 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3edb4-234">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="3edb4-234">ProPlusVolume</span></span></p>
<p><span data-ttu-id="3edb4-235">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="3edb4-235">VisioProVolume</span></span></p>
<p><span data-ttu-id="3edb4-236">ProjectProVolume</span><span class="sxs-lookup"><span data-stu-id="3edb4-236">ProjectProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="3edb4-237">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="3edb4-237">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="3edb4-238">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="3edb4-238">VisioProRetail</span></span></p>
<p><span data-ttu-id="3edb4-239">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="3edb4-239">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="3edb4-240">Konvertieren der Office-Anwendungen in ein App-V-Paket</span><span class="sxs-lookup"><span data-stu-id="3edb4-240">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="3edb4-241">Öffnen Sie die CustomConfig.xml Datei in Editor erneut, und nehmen Sie die folgenden Änderungen an der Datei vor:</span><span class="sxs-lookup"><span data-stu-id="3edb4-241">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="3edb4-242">Parameter</span><span class="sxs-lookup"><span data-stu-id="3edb4-242">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="3edb4-243">So ändern Sie den Wert</span><span class="sxs-lookup"><span data-stu-id="3edb4-243">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3edb4-244">SourcePath</span><span class="sxs-lookup"><span data-stu-id="3edb4-244">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-245">Zeigen Sie auf die zuvor heruntergeladenen Office-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-245">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3edb4-246">ProductID</span><span class="sxs-lookup"><span data-stu-id="3edb4-246">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-247">Geben Sie den Lizenzierungstyp an, wie in den folgenden Beispielen gezeigt:</span><span class="sxs-lookup"><span data-stu-id="3edb4-247">Specify the type of licensing, as shown in the following examples:</span></span></p>
   <ul>
   <li><p><span data-ttu-id="3edb4-248">Abonnementlizenzierung</span><span class="sxs-lookup"><span data-stu-id="3edb4-248">Subscription Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="3edb4-249">In diesem Beispiel wurden die folgenden Änderungen zum Erstellen eines Pakets mit Abonnementlizenzierung vorgenommen:</span><span class="sxs-lookup"><span data-stu-id="3edb4-249">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3edb4-250">SourcePath</span><span class="sxs-lookup"><span data-stu-id="3edb4-250">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-251">ist der Pfad, der geändert wurde, um auf die Office-Anwendungen zu verweisen, die zuvor heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-251">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="3edb4-252">Produkt-ID</span><span class="sxs-lookup"><span data-stu-id="3edb4-252">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-253">für Office wurde geändert in <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="3edb4-253">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3edb4-254">Produkt-ID</span><span class="sxs-lookup"><span data-stu-id="3edb4-254">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-255">für Visio wurde geändert in <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="3edb4-255">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   <li><p><span data-ttu-id="3edb4-256">Volumenlizenzierung</span><span class="sxs-lookup"><span data-stu-id="3edb4-256">Volume Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\Server\Office2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;ProPlusVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt;</code></pre>
   <p><span data-ttu-id="3edb4-257">In diesem Beispiel wurden die folgenden Änderungen vorgenommen, um ein Paket mit Volumenlizenzierung zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="3edb4-257">In this example, the following changes were made to create a package with Volume licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3edb4-258">SourcePath</span><span class="sxs-lookup"><span data-stu-id="3edb4-258">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-259">ist der Pfad, der geändert wurde, um auf die Office-Anwendungen zu verweisen, die zuvor heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-259">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="3edb4-260">Produkt-ID</span><span class="sxs-lookup"><span data-stu-id="3edb4-260">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-261">für Office wurde geändert in <code>ProPlusVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="3edb4-261">for Office was changed to <code>ProPlusVolume</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3edb4-262">Produkt-ID</span><span class="sxs-lookup"><span data-stu-id="3edb4-262">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-263">für Visio wurde geändert in <code>VisioProVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="3edb4-263">for Visio was changed to <code>VisioProVolume</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3edb4-264">ExcludeApp (optional)</span><span class="sxs-lookup"><span data-stu-id="3edb4-264">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-265">Mit dieser Option können Sie Office-Programme angeben, die nicht im App-V-Paket enthalten sein sollen, das vom Office-Bereitstellungs Tool erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3edb4-265">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="3edb4-266">So können Sie beispielsweise Access und InfoPath ausschließen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-266">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3edb4-267">PACKAGEGUID (optional)</span><span class="sxs-lookup"><span data-stu-id="3edb4-267">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-268">Standardmäßig verwenden alle App-v-Pakete, die vom Office-Bereitstellungs Tool erstellt wurden, dieselbe App-v-Paket-ID.</span><span class="sxs-lookup"><span data-stu-id="3edb4-268">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="3edb4-269">Sie können PACKAGEGUID verwenden, um eine andere Paket-ID für jedes Paket anzugeben, mit der Sie mehrere App-v-Pakete, die vom Office-Bereitstellungs Tool erstellt wurden, veröffentlichen und mithilfe des App-v-Servers verwalten können.</span><span class="sxs-lookup"><span data-stu-id="3edb4-269">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="3edb4-270">Ein Beispiel für die Verwendung dieses Parameters ist, wenn Sie unterschiedliche Pakete für verschiedene Benutzer erstellen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-270">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="3edb4-271">So können Sie beispielsweise ein Paket mit Office 2013 für einige Benutzer erstellen und ein weiteres Paket mit Office 2013 und Visio 2013 für eine andere Gruppe von Benutzern erstellen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-271">For example, you can create a package with just Office 2013 for some users, and create another package with Office 2013 and Visio 2013 for another set of users.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="3edb4-272">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3edb4-272">Note</span></span></strong><br/><p><span data-ttu-id="3edb4-273">Auch wenn Sie eindeutige Paket-IDs verwenden, können Sie weiterhin nur ein App-V-Paket auf einem einzelnen Gerät bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-273">Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="3edb4-274">Verwenden Sie den Befehl/Packager, um die Office-Anwendungen in ein Office 2013-App-V-Paket umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="3edb4-274">Use the /packager command to convert the Office applications to an Office 2013 App-V package.</span></span>

   <span data-ttu-id="3edb4-275">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3edb4-275">For example:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /packager \\server\Office2013\Customconfig.xml  \\server\share\Office2013AppV
   ```

   <span data-ttu-id="3edb4-276">Im Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3edb4-276">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3edb4-277">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="3edb4-277">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-278">der Speicherort des Netzwerkspeichers, der das Office-Bereitstellungs Tool und die benutzerdefinierte Configuration.xml Datei enthält, Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="3edb4-278">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="3edb4-279">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="3edb4-279">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-280">ist das Office-Bereitstellungs Tool.</span><span class="sxs-lookup"><span data-stu-id="3edb4-280">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3edb4-281">/packager</span><span class="sxs-lookup"><span data-stu-id="3edb4-281">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-282">erstellt das Office 2013-App-V-Paket mit Volumenlizenzierung, wie in der customConfig.xml-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="3edb4-282">creates the Office 2013 App-V package with Volume Licensing as specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="3edb4-283">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="3edb4-283">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-284">übergibt die Konfigurations-XML-Datei (in diesem Fall customConfig), die für die Paket Phase vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="3edb4-284">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="3edb4-285">\server\share\Office 2013AppV</span><span class="sxs-lookup"><span data-stu-id="3edb4-285">\server\share\Office 2013AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="3edb4-286">Gibt den Speicherort des neu erstellten Office App-V-Pakets an.</span><span class="sxs-lookup"><span data-stu-id="3edb4-286">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2013 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note**  
To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="3edb4-287">Überprüfen Sie, ob das Office 2013-App-V-Paket ordnungsgemäß funktioniert:</span><span class="sxs-lookup"><span data-stu-id="3edb4-287">Verify that the Office 2013 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="3edb4-288">Veröffentlichen Sie das von Ihnen Global erstellte Office 2013 App-V-Paket auf einem Testcomputer, und überprüfen Sie, ob die Office 2013-Verknüpfungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-288">Publish the Office 2013 App-V package, which you created globally, to a test computer, and verify that the Office 2013 shortcuts appear.</span></span>

   2.  <span data-ttu-id="3edb4-289">Starten Sie einige Office 2013-Anwendungen wie Excel oder Word, um sicherzustellen, dass Ihr Paket wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3edb4-289">Start a few Office 2013 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="3edb4-290">Veröffentlichen des Office-Pakets für App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3edb4-290">Publishing the Office package for App-V 5.1</span></span>


<span data-ttu-id="3edb4-291">Verwenden Sie die folgenden Informationen zum Veröffentlichen eines Office-Pakets.</span><span class="sxs-lookup"><span data-stu-id="3edb4-291">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="3edb4-292">Methoden zum Veröffentlichen von Office App-V-Paketen</span><span class="sxs-lookup"><span data-stu-id="3edb4-292">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="3edb4-293">Stellen Sie das App-V-Paket für Office 2013 mithilfe der gleichen Methoden bereit, die Sie für jedes andere Paket verwenden:</span><span class="sxs-lookup"><span data-stu-id="3edb4-293">Deploy the App-V package for Office 2013 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="3edb4-294">System Center Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="3edb4-294">System Center Configuration Manager</span></span>

-   <span data-ttu-id="3edb4-295">App-V-Server</span><span class="sxs-lookup"><span data-stu-id="3edb4-295">App-V Server</span></span>

-   <span data-ttu-id="3edb4-296">Eigenständige über PowerShell-Befehle</span><span class="sxs-lookup"><span data-stu-id="3edb4-296">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="3edb4-297">Voraussetzungen und Anforderungen für die Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="3edb4-297">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3edb4-298">Voraussetzungen oder Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3edb4-298">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="3edb4-299">Details</span><span class="sxs-lookup"><span data-stu-id="3edb4-299">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3edb4-300">Aktivieren von PowerShell-Skripts für die App-V-Clients</span><span class="sxs-lookup"><span data-stu-id="3edb4-300">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="3edb4-301">Zum Veröffentlichen von Office 2013-Paketen müssen Sie ein Skript ausführen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-301">To publish Office 2013 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="3edb4-302">Paket Skripts sind auf App-V-Clients standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3edb4-302">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="3edb4-303">Führen Sie zum Aktivieren der Skripterstellung den folgenden PowerShell-Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="3edb4-303">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3edb4-304">Veröffentlichen des Office 2013-Pakets auf globaler Ebene</span><span class="sxs-lookup"><span data-stu-id="3edb4-304">Publish the Office 2013 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="3edb4-305">Erweiterungspunkte im Office App-V-Paket erfordern die Installation auf Computerebene.</span><span class="sxs-lookup"><span data-stu-id="3edb4-305">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="3edb4-306">Wenn Sie auf Computerebene veröffentlichen, werden keine Voraussetzungen oder verteilbaren Aktionen benötigt, und das Office 2013-Paket ermöglicht es, dass seine Anwendungen wie nativ installierte Office funktionieren, sodass Administratoren keine Pakete anpassen müssen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-306">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2013 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="3edb4-307">Veröffentlichen eines Office-Pakets</span><span class="sxs-lookup"><span data-stu-id="3edb4-307">How to publish an Office package</span></span>

<span data-ttu-id="3edb4-308">Führen Sie den folgenden Befehl aus, um ein Office-Paket global zu veröffentlichen:</span><span class="sxs-lookup"><span data-stu-id="3edb4-308">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="3edb4-309">Über die Web-Verwaltungskonsole auf dem App-V-Server können Sie einer Gruppe von Computern Berechtigungen hinzufügen, anstatt einer Benutzergruppe, um zu ermöglichen, dass Pakete Global auf den Computern in der entsprechenden Gruppe veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-309">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="3edb4-310">Anpassen und Verwalten von Office App-V-Paketen</span><span class="sxs-lookup"><span data-stu-id="3edb4-310">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="3edb4-311">Zum Verwalten Ihrer Office-App-V-Pakete verwenden Sie die gleichen Vorgänge wie für jedes andere Paket, doch es gibt ein paar Ausnahmen, wie in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3edb4-311">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="3edb4-312">Aktivieren von Office-Plug-Ins mithilfe von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="3edb4-312">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="3edb4-313">Deaktivieren von Office 2013-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3edb4-313">Disabling Office 2013 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="3edb4-314">Deaktivieren von Office 2013-Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="3edb4-314">Disabling Office 2013 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="3edb4-315">Verwalten von Office 2013-Paket Upgrades</span><span class="sxs-lookup"><span data-stu-id="3edb4-315">Managing Office 2013 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="3edb4-316">Verwalten von Office 2013-Lizenzierungs Updates</span><span class="sxs-lookup"><span data-stu-id="3edb4-316">Managing Office 2013 licensing upgrades</span></span>](#bkmk-manage-office-lic-upgrd)

-   [<span data-ttu-id="3edb4-317">Bereitstellen von Visio 2013 und Project 2013 mit Office</span><span class="sxs-lookup"><span data-stu-id="3edb4-317">Deploying Visio 2013 and Project 2013 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="3edb4-318">Aktivieren von Office-Plug-Ins mithilfe von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="3edb4-318">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="3edb4-319">Führen Sie die Schritte in diesem Abschnitt aus, um Office-Plug-ins mit Ihrem Office-Paket zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3edb4-319">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="3edb4-320">Um Office-Plug-ins zu verwenden, müssen Sie den App-V-Sequenzer verwenden, um ein separates Paket zu erstellen, das nur die Plug-Ins enthält. Sie können das Office-Bereitstellungs Tool nicht verwenden, um das Plug-in-Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-320">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="3edb4-321">Sie erstellen dann eine Verbindungsgruppe, die das Office-Paket und das Plug-in-Paket enthält, wie in den folgenden Schritten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3edb4-321">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="3edb4-322">So aktivieren Sie Plug-Ins für Office App-V-Pakete</span><span class="sxs-lookup"><span data-stu-id="3edb4-322">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="3edb4-323">Fügen Sie mithilfe von App-V Server, System Center Configuration Manager oder einem PowerShell-Cmdlet eine Verbindungsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="3edb4-323">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="3edb4-324">Sequenzieren Sie Ihre Plug-ins mit dem App-V 5,1-Sequenzer.</span><span class="sxs-lookup"><span data-stu-id="3edb4-324">Sequence your plug-ins using the App-V 5.1 Sequencer.</span></span> <span data-ttu-id="3edb4-325">Stellen Sie sicher, dass Office 2013 auf dem Computer installiert ist, der zur Sequenzierung des Plug-ins verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3edb4-325">Ensure that Office 2013 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="3edb4-326">Es wird empfohlen, Microsoft 365-Apps für Enterprise (nicht-virtuell) auf dem Sequenzcomputer zu verwenden, wenn Sie Office 2013-Plug-ins abgleichen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-326">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2013 plug-ins.</span></span>

3.  <span data-ttu-id="3edb4-327">Erstellen Sie ein App-V 5,1-Paket, das die gewünschten Plug-Ins enthält.</span><span class="sxs-lookup"><span data-stu-id="3edb4-327">Create an App-V 5.1 package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="3edb4-328">Fügen Sie mithilfe von App-V Server, System Center Configuration Manager oder einem PowerShell-Cmdlet eine Verbindungsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="3edb4-328">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="3edb4-329">Fügen Sie das Office 2013-App-V-Paket und das Plug-in-Paket, das Sie sequenziert haben, zu der von Ihnen erstellten Verbindungsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="3edb4-329">Add the Office 2013 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    **<span data-ttu-id="3edb4-330">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3edb4-330">Important</span></span>**  
    <span data-ttu-id="3edb4-331">Die Reihenfolge der Pakete in der Verbindungsgruppe bestimmt die Reihenfolge, in der die Paketinhalte zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-331">The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="3edb4-332">Fügen Sie in ihrer Beschreibungsdatei für die Verbindungsgruppe zuerst das Office 2013-App-v-Paket hinzu, und fügen Sie dann das Plug-in-App-v-Paket hinzu.</span><span class="sxs-lookup"><span data-stu-id="3edb4-332">In your Connection group descriptor file, add the Office 2013 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="3edb4-333">Stellen Sie sicher, dass beide Pakete auf dem Zielcomputer veröffentlicht werden und dass das Plug-in-Paket Global veröffentlicht wird, um die globalen Einstellungen des veröffentlichten Office 2013-App-V-Pakets zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-333">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2013 App-V package.</span></span>

7.  <span data-ttu-id="3edb4-334">Überprüfen Sie, ob die Bereitstellungs Konfigurationsdatei des Plug-in-Pakets die gleichen Einstellungen wie das Office 2013-App-V-Paket aufweist.</span><span class="sxs-lookup"><span data-stu-id="3edb4-334">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2013 App-V package has.</span></span>

    <span data-ttu-id="3edb4-335">Da das Office 2013-App-V-Paket in das Betriebssystem integriert ist, sollten die Einstellungen für das Plug-in-Paket übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-335">Since the Office 2013 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="3edb4-336">Sie können die Konfigurationsdatei für die Bereitstellung nach "com-Modus" Durchsuchen und sicherstellen, dass Ihr Plug-in-Paket diesen Wert als "integriert" festgesetzt hat und sowohl "InProcessEnabled" als auch "OutOfProcessEnabled" den Einstellungen des veröffentlichten Office 2013-App-V-Pakets entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-336">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2013 App-V package you published.</span></span>

8.  <span data-ttu-id="3edb4-337">Öffnen Sie die Konfigurationsdatei für die Bereitstellung, und legen Sie den Wert für **Objekte** auf **false**fest.</span><span class="sxs-lookup"><span data-stu-id="3edb4-337">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="3edb4-338">Wenn Sie nach der Sequenzierung Änderungen an der Konfigurationsdatei für die Bereitstellung vorgenommen haben, stellen Sie sicher, dass das Plug-in-Paket mit der Datei veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="3edb4-338">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="3edb4-339">Stellen Sie sicher, dass die von Ihnen erstellte Verbindungsgruppe auf dem gewünschten Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3edb4-339">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="3edb4-340">Die erstellte Verbindungsgruppe wird wahrscheinlich "aussetzen", wenn das Office 2013-App-V-Paket verwendet wird, wenn die Verbindungsgruppe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3edb4-340">The Connection Group created will likely “pend” if the Office 2013 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="3edb4-341">In diesem Fall müssen Sie den Neustart durchführen, um die Verbindungsgruppe erfolgreich zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3edb4-341">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="3edb4-342">Nachdem Sie beide Pakete erfolgreich veröffentlicht und die Verbindungsgruppe aktiviert haben, starten Sie die Office 2013-Zielanwendung, und stellen Sie sicher, dass das von Ihnen veröffentlichte und der Verbindungsgruppe hinzugefügte Plug-in wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3edb4-342">After you successfully publish both packages and enable the Connection Group, start the target Office 2013 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="3edb4-343">Deaktivieren von Office 2013-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3edb4-343">Disabling Office 2013 applications</span></span>

<span data-ttu-id="3edb4-344">Möglicherweise möchten Sie bestimmte Anwendungen in Ihrem Office App-V-Paket deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3edb4-344">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="3edb4-345">So können Sie beispielsweise den Zugriff deaktivieren, aber alle anderen Office-Anwendungen Main verfügbar lassen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-345">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="3edb4-346">Wenn Sie eine Anwendung deaktivieren, wird dem Endbenutzer die Verknüpfung für diese Anwendung nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3edb4-346">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="3edb4-347">Sie müssen die Anwendung nicht neu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="3edb4-347">You do not have to re-sequence the application.</span></span> <span data-ttu-id="3edb4-348">Wenn Sie die Konfigurationsdatei für die Bereitstellung nach dem Veröffentlichen des Office 2013-App-v-Pakets ändern, speichern Sie die Änderungen, fügen das Office 2013-App-v-Paket hinzu und veröffentlichen es dann erneut mit der neuen Bereitstellungs Konfigurationsdatei, um die neuen Einstellungen auf Office 2013 App-v-Paketanwendungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-348">When you change the Deployment Configuration File after the Office 2013 App-V package has been published, you will save the changes, add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

**<span data-ttu-id="3edb4-349">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3edb4-349">Note</span></span>**  
<span data-ttu-id="3edb4-350">Wenn Sie bestimmte Office-Anwendungen (beispielsweise Access und InfoPath) beim Erstellen des App-V-Pakets mit dem Office-Bereitstellungs Tool ausschließen möchten, verwenden Sie die Einstellung **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="3edb4-350">To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span> <span data-ttu-id="3edb4-351">Weitere Informationen finden Sie unter [Referenz für Klick-und-Los-configuration.xml-Datei](https://technet.microsoft.com/library/jj219426.aspx).</span><span class="sxs-lookup"><span data-stu-id="3edb4-351">For more information, see [Reference for Click-to-Run configuration.xml file](https://technet.microsoft.com/library/jj219426.aspx).</span></span>



**<span data-ttu-id="3edb4-352">So deaktivieren Sie eine Office 2013-Anwendung</span><span class="sxs-lookup"><span data-stu-id="3edb4-352">To disable an Office 2013 application</span></span>**

1.  <span data-ttu-id="3edb4-353">Öffnen Sie eine Konfigurationsdatei für die Bereitstellung mit einem Text-Editor wie **Editor** , und suchen Sie nach "Anwendungen".</span><span class="sxs-lookup"><span data-stu-id="3edb4-353">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="3edb4-354">Suchen Sie nach der Office-Anwendung, die Sie deaktivieren möchten, beispielsweise Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3edb4-354">Search for the Office application you want to disable, for example, Access 2013.</span></span>

3.  <span data-ttu-id="3edb4-355">Ändern Sie den Wert von "Enabled" von "true" in "false".</span><span class="sxs-lookup"><span data-stu-id="3edb4-355">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="3edb4-356">Speichern Sie die Konfigurationsdatei für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="3edb4-356">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="3edb4-357">Fügen Sie das Office 2013-App-V-Paket mit der neuen Bereitstellungs Konfigurationsdatei hinzu.</span><span class="sxs-lookup"><span data-stu-id="3edb4-357">Add the Office 2013 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot)]\officefl5\INFOPATH.EXE" Enabled="true">
      <VisualElements>
        <Name>InfoPath Filler 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[{AppVPackageRoot}]\office15\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office15\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="3edb4-358">Fügen Sie das Office 2013-App-v-Paket erneut hinzu, und veröffentlichen Sie es erneut mit der neuen Bereitstellungs Konfigurationsdatei, um die neuen Einstellungen auf Office 2013 App-v-Paketanwendungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-358">Re-add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="3edb4-359">Deaktivieren von Office 2013-Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="3edb4-359">Disabling Office 2013 shortcuts</span></span>

<span data-ttu-id="3edb4-360">Möglicherweise möchten Sie die Tastenkombinationen für bestimmte Office-Anwendungen deaktivieren, anstatt das Paket zu veröffentlichen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-360">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="3edb4-361">Im folgenden Beispiel wird gezeigt, wie Sie Tastenkombinationen für Microsoft Access deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3edb4-361">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="3edb4-362">So deaktivieren Sie Tastenkombinationen für Office 2013-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3edb4-362">To disable shortcuts for Office 2013 applications</span></span>**

1.  <span data-ttu-id="3edb4-363">Öffnen Sie eine Konfigurationsdatei für die Bereitstellung in Editor, und suchen Sie nach "Tastenkombinationen".</span><span class="sxs-lookup"><span data-stu-id="3edb4-363">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="3edb4-364">Wenn Sie bestimmte Tastenkombinationen deaktivieren möchten, löschen oder kommentieren Sie die gewünschten Tastenkombinationen aus.</span><span class="sxs-lookup"><span data-stu-id="3edb4-364">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="3edb4-365">Sie müssen das Subsystem vorhanden und aktiviert lassen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-365">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="3edb4-366">Löschen Sie beispielsweise im folgenden Beispiel die Microsoft Access-Tastenkombinationen, während &lt; Sie die Tastenkombination &gt; &lt; /Shortcut intakt halten, &gt; um die Microsoft Access-Verknüpfung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3edb4-366">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2013\Access 2013.lnk</File>
           <Target>[{AppvPackageRoot}])office15\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office15\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="3edb4-367">Speichern Sie die Konfigurationsdatei für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="3edb4-367">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="3edb4-368">Veröffentlichen Sie das Office 2013 App-V-Paket erneut mit der neuen Bereitstellungs Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="3edb4-368">Republish Office 2013 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="3edb4-369">Viele zusätzliche Einstellungen können durch Ändern der Bereitstellungskonfiguration für App-V-Pakete geändert werden, beispielsweise Dateitypen Zuordnungen, virtuelles Datei System und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="3edb4-369">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="3edb4-370">Weitere Informationen zur Verwendung von Bereitstellungskonfigurationsdateien zum Ändern von App-V-Paketeinstellungen finden Sie im Abschnitt zusätzliche Ressourcen am Ende dieses Dokuments.</span><span class="sxs-lookup"><span data-stu-id="3edb4-370">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="3edb4-371">Verwalten von Office 2013-Paket Upgrades</span><span class="sxs-lookup"><span data-stu-id="3edb4-371">Managing Office 2013 package upgrades</span></span>

<span data-ttu-id="3edb4-372">Verwenden Sie das Office-Bereitstellungs Tool, um ein Office 2013-Paket zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3edb4-372">To upgrade an Office 2013 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="3edb4-373">Führen Sie die folgenden Schritte aus, um ein zuvor bereitgestelltes Office 2013-Paket zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3edb4-373">To upgrade a previously deployed Office 2013 package, perform the following steps.</span></span>

**<span data-ttu-id="3edb4-374">Aktualisieren eines zuvor bereitgestellten Office 2013-Pakets</span><span class="sxs-lookup"><span data-stu-id="3edb4-374">How to upgrade a previously deployed Office 2013 package</span></span>**

1.  <span data-ttu-id="3edb4-375">Erstellen Sie ein neues Office 2013-Paket über das Office-Bereitstellungs Tool, das die neueste Office 2013-Anwendungssoftware verwendet.</span><span class="sxs-lookup"><span data-stu-id="3edb4-375">Create a new Office 2013 package through the Office Deployment Tool that uses the most recent Office 2013 application software.</span></span> <span data-ttu-id="3edb4-376">Die neuesten Office 2013-Bits können immer über die Downloadphase des Erstellens eines Office 2013-App-V-Pakets abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-376">The most recent Office 2013 bits can always be obtained through the download stage of creating an Office 2013 App-V Package.</span></span> <span data-ttu-id="3edb4-377">Das neu erstellte Office 2013-Paket verfügt über die neuesten Updates und eine neue Versions-ID.</span><span class="sxs-lookup"><span data-stu-id="3edb4-377">The newly created Office 2013 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="3edb4-378">Alle Pakete, die mit dem Office-Bereitstellungs Tool erstellt wurden, haben dieselbe Linie.</span><span class="sxs-lookup"><span data-stu-id="3edb4-378">All packages created using the Office Deployment Tool have the same lineage.</span></span>

    **<span data-ttu-id="3edb4-379">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3edb4-379">Note</span></span>**  
    <span data-ttu-id="3edb4-380">Office App-V-Pakete weisen zwei Versions-IDs auf:</span><span class="sxs-lookup"><span data-stu-id="3edb4-380">Office App-V packages have two Version IDs:</span></span>

    -   <span data-ttu-id="3edb4-381">Eine Office 2013-App-V-paketversions-ID, die für alle mit dem Office-Bereitstellungs Tool erstellten Pakete eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="3edb4-381">An Office 2013 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span>

    -   <span data-ttu-id="3edb4-382">Eine zweite App-V-Paket-Versions-ID, x. x. x. x, beispielsweise im AppX-Manifest, das nur dann geändert wird, wenn eine neue Version von Office selbst vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3edb4-382">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="3edb4-383">Wenn beispielsweise eine neue Office 2013-Version mit Upgrades verfügbar ist und ein Paket über das Office-Bereitstellungs Tool erstellt wird, um diese Upgrades zu integrieren, ändert sich die x. x. x. x-Version, um zu reflektieren, dass sich die Office-Version selbst geändert hat.</span><span class="sxs-lookup"><span data-stu-id="3edb4-383">For example, if a new Office 2013 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="3edb4-384">Der App-V-Server verwendet die x. x. x. x. x-Versions-ID, um dieses Paket zu unterscheiden und zu erkennen, dass es neue Upgrades für das zuvor veröffentlichte Paket enthält, und als Ergebnis es als Upgrade auf das vorhandene Office 2013-Paket veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-384">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2013 package.</span></span>



2.  <span data-ttu-id="3edb4-385">Veröffentlichen Sie die neu erstellten Office 2013-App-V-Pakete Global auf Computern, auf denen Sie die neuen Updates anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3edb4-385">Globally publish the newly created Office 2013 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="3edb4-386">Da das neue Paket dieselbe Abstammungslinie des älteren Office 2013-App-V-Pakets aufweist, werden durch das Veröffentlichen des neuen Pakets mit den Updates nur die neuen Änderungen auf das alte Paket angewendet, und es wird schnell so sein.</span><span class="sxs-lookup"><span data-stu-id="3edb4-386">Since the new package has the same lineage of the older Office 2013 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3.  <span data-ttu-id="3edb4-387">Upgrades werden auf die gleiche Weise wie alle Global veröffentlichten App-V-Pakete angewendet.</span><span class="sxs-lookup"><span data-stu-id="3edb4-387">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="3edb4-388">Da Anwendungen wahrscheinlich verwendet werden, können Upgrades verzögert werden, bis der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3edb4-388">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>

### <a href="" id="bkmk-manage-office-lic-upgrd"></a><span data-ttu-id="3edb4-389">Verwalten von Office 2013-Lizenzierungs Updates</span><span class="sxs-lookup"><span data-stu-id="3edb4-389">Managing Office 2013 licensing upgrades</span></span>

<span data-ttu-id="3edb4-390">Wenn ein neues Office 2013-App-v-Paket eine andere Lizenz als das derzeit bereitgestellte Office 2013-App-v-Paket aufweist.</span><span class="sxs-lookup"><span data-stu-id="3edb4-390">If a new Office 2013 App-V Package has a different license than the Office 2013 App-V Package currently deployed.</span></span> <span data-ttu-id="3edb4-391">Beispielsweise ist das Office 2013-Paket, das bereitgestellt wird, ein abonnementbasiertes Office 2013, und das neue Office 2013-Paket basiert auf Volumenlizenzierung, die folgenden Anweisungen müssen befolgt werden, um ein reibungsloses Lizenzierungs Upgrade zu gewährleisten:</span><span class="sxs-lookup"><span data-stu-id="3edb4-391">For instance, the Office 2013 package deployed is a subscription based Office 2013 and the new Office 2013 package is Volume Licensing based, the following instructions must be followed to ensure smooth licensing upgrade:</span></span>

**<span data-ttu-id="3edb4-392">Aktualisieren einer Office 2013-Lizenz</span><span class="sxs-lookup"><span data-stu-id="3edb4-392">How to upgrade an Office 2013 License</span></span>**

1.  <span data-ttu-id="3edb4-393">Heben Sie die Veröffentlichung des bereits bereitgestellten App-V-Pakets für Office 2013-Abonnementlizenzierung auf.</span><span class="sxs-lookup"><span data-stu-id="3edb4-393">Unpublish the already deployed Office 2013 Subscription Licensing App-V package.</span></span>

2.  <span data-ttu-id="3edb4-394">Entfernen Sie das nicht veröffentlichte Office 2013-Abonnement Lizenzierungs-App-V-Paket.</span><span class="sxs-lookup"><span data-stu-id="3edb4-394">Remove the unpublished Office 2013 Subscription Licensing App-V package.</span></span>

3.  <span data-ttu-id="3edb4-395">Starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="3edb4-395">Restart the computer.</span></span>

4.  <span data-ttu-id="3edb4-396">Fügen Sie die neue Office 2013-App-V-Paket-Volumenlizenzierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="3edb4-396">Add the new Office 2013 App-V Package Volume Licensing.</span></span>

5.  <span data-ttu-id="3edb4-397">Veröffentlichen Sie das hinzugefügte Office 2013 App-V-Paket mit Volumenlizenzierung.</span><span class="sxs-lookup"><span data-stu-id="3edb4-397">Publish the added Office 2013 App-V Package with Volume Licensing.</span></span>

<span data-ttu-id="3edb4-398">Ein Office 2013-App-V-Paket mit der von Ihnen ausgewählten Lizenzierung wird erfolgreich bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3edb4-398">An Office 2013 App-V Package with your chosen licensing will be successfully deployed.</span></span>

### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="3edb4-399">Bereitstellen von Visio 2013 und Project 2013 mit Office</span><span class="sxs-lookup"><span data-stu-id="3edb4-399">Deploying Visio 2013 and Project 2013 with Office</span></span>

<span data-ttu-id="3edb4-400">In der folgenden Tabelle werden die Anforderungen und Optionen für die Bereitstellung von Visio 2013 und Project 2013 mit Office beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3edb4-400">The following table describes the requirements and options for deploying Visio 2013 and Project 2013 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3edb4-401">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3edb4-401">Task</span></span></th>
<th align="left"><span data-ttu-id="3edb4-402">Details</span><span class="sxs-lookup"><span data-stu-id="3edb4-402">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3edb4-403">Wie kann ich Visio 2013 und Project 2013 mit Office Verpacken und veröffentlichen?</span><span class="sxs-lookup"><span data-stu-id="3edb4-403">How do I package and publish Visio 2013 and Project 2013 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="3edb4-404">Sie müssen Visio 2013 und Project 2013 in das gleiche Paket mit Office einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-404">You must include Visio 2013 and Project 2013 in the same package with Office.</span></span></p>
<p><span data-ttu-id="3edb4-405">Wenn Sie Office nicht bereitstellen, können Sie ein Paket erstellen, das Visio und/oder Project enthält, sofern Sie <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)"> die Bereitstellung von Microsoft Office 2010 mithilfe von App-V befolgen </a> .</span><span class="sxs-lookup"><span data-stu-id="3edb4-405">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)">Deploying Microsoft Office 2010 by Using App-V</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3edb4-406">Wie kann ich Visio 2013 und Project 2013 für bestimmte Benutzer bereitstellen?</span><span class="sxs-lookup"><span data-stu-id="3edb4-406">How can I deploy Visio 2013 and Project 2013 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="3edb4-407">Verwenden Sie eine der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="3edb4-407">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3edb4-408">Wenn Sie möchten...</span><span class="sxs-lookup"><span data-stu-id="3edb4-408">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="3edb4-409">... Verwenden Sie dann diese Methode</span><span class="sxs-lookup"><span data-stu-id="3edb4-409">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3edb4-410">Erstellen von zwei unterschiedlichen Paketen und Bereitstellen jeder Person für eine andere Gruppe von Benutzern</span><span class="sxs-lookup"><span data-stu-id="3edb4-410">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="3edb4-411">Erstellen und Bereitstellen der folgenden Pakete:</span><span class="sxs-lookup"><span data-stu-id="3edb4-411">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="3edb4-412">Ein Paket, das nur Office-deploy auf Computern enthält, deren Benutzer nur Office benötigen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-412">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="3edb4-413">Ein Paket mit Office, Visio und Project – deploy auf Computern, deren Benutzer alle drei Anwendungen benötigen.</span><span class="sxs-lookup"><span data-stu-id="3edb4-413">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3edb4-414">Wenn Sie nur ein Paket für die gesamte Organisation verwenden möchten oder wenn Sie über Benutzer verfügen, die Computer freigeben:</span><span class="sxs-lookup"><span data-stu-id="3edb4-414">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="3edb4-415">Führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="3edb4-415">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="3edb4-416">Erstellen Sie ein Paket, das Office, Visio und Project enthält.</span><span class="sxs-lookup"><span data-stu-id="3edb4-416">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="3edb4-417">Bereitstellen des Pakets für alle Benutzer</span><span class="sxs-lookup"><span data-stu-id="3edb4-417">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="3edb4-418">Verwenden Sie <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> , um zu verhindern, dass bestimmte Benutzer Visio und Project verwenden.</span><span class="sxs-lookup"><span data-stu-id="3edb4-418">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3edb4-419">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3edb4-419">Additional resources</span></span>


**<span data-ttu-id="3edb4-420">Office 2013-App-V-Pakete – zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3edb4-420">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="3edb4-421">Office-Bereitstellungs Tool für Klick-und-Los</span><span class="sxs-lookup"><span data-stu-id="3edb4-421">Office Deployment Tool for Click-to-Run</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=330672)

[<span data-ttu-id="3edb4-422">Unterstützte Szenarien für die Bereitstellung von Microsoft Office als sequenziertes App-V-Paket</span><span class="sxs-lookup"><span data-stu-id="3edb4-422">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="3edb4-423">Office 2010-App-V-Pakete</span><span class="sxs-lookup"><span data-stu-id="3edb4-423">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="3edb4-424">Microsoft Office 2010-Sequenzierung-Kit für Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="3edb4-424">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="3edb4-425">Bekannte Probleme beim Erstellen oder Verwenden eines App-V 5,0 Office 2010-Pakets</span><span class="sxs-lookup"><span data-stu-id="3edb4-425">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="3edb4-426">Sequenzierung von Microsoft Office 2010 in Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="3edb4-426">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="3edb4-427">Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="3edb4-427">Connection Groups</span></span>**

[<span data-ttu-id="3edb4-428">Bereitstellen von Verbindungsgruppen in Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="3edb4-428">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="3edb4-429">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="3edb4-429">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="3edb4-430">Dynamische Konfiguration</span><span class="sxs-lookup"><span data-stu-id="3edb4-430">Dynamic Configuration</span></span>**

[<span data-ttu-id="3edb4-431">Informationen zur dynamischen Konfiguration in App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="3edb4-431">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)














