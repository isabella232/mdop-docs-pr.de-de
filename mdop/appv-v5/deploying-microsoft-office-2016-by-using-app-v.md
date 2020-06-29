---
title: Bereitstellen von Microsoft Office2016 mit App-V
description: Bereitstellen von Microsoft Office2016 mit App-V
author: dansimp
ms.assetid: cc675cde-cb8d-4b7c-a700-6104b78f1d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/25/2017
ms.openlocfilehash: dfedab98e0bdf0a0d5f5e407d9bedadbbf56ad69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805864"
---
# <span data-ttu-id="28d1c-103">Bereitstellen von Microsoft Office2016 mit App-V</span><span class="sxs-lookup"><span data-stu-id="28d1c-103">Deploying Microsoft Office 2016 by Using App-V</span></span>


<span data-ttu-id="28d1c-104">Verwenden Sie die Informationen in diesem Artikel, um Microsoft Application Virtualization 5,0 oder höhere Versionen zu verwenden, um Microsoft Office 2016 als virtualisierte Anwendung an Computer in Ihrer Organisation zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="28d1c-104">Use the information in this article to use Microsoft Application Virtualization 5.0, or later versions, to deliver Microsoft Office 2016 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="28d1c-105">Informationen zum Verwenden von App-v für die Bereitstellung von Office 2013 finden Sie unter [Bereitstellen von Microsoft Office 2013 mithilfe von App-v](deploying-microsoft-office-2013-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="28d1c-105">For information about using App-V to deliver Office 2013, see [Deploying Microsoft Office 2013 by Using App-V](deploying-microsoft-office-2013-by-using-app-v.md).</span></span> <span data-ttu-id="28d1c-106">Informationen zum Verwenden von App-v für die Bereitstellung von Office 2010 finden Sie unter [Bereitstellen von Microsoft Office 2010 mithilfe von App-v](deploying-microsoft-office-2010-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="28d1c-106">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v.md).</span></span>

<span data-ttu-id="28d1c-107">Dieses Thema enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="28d1c-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="28d1c-108">Was Sie wissen sollten, bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="28d1c-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="28d1c-109">Erstellen eines Office 2016-Pakets für App-V mit dem Office-Bereitstellungs Tool</span><span class="sxs-lookup"><span data-stu-id="28d1c-109">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="28d1c-110">Veröffentlichen des Office-Pakets für App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="28d1c-110">Publishing the Office package for App-V 5.0</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="28d1c-111">Anpassen und Verwalten von Office App-V-Paketen</span><span class="sxs-lookup"><span data-stu-id="28d1c-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="28d1c-112">Was Sie wissen sollten, bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="28d1c-112">What to know before you start</span></span>


<span data-ttu-id="28d1c-113">Bevor Sie Office 2016 mithilfe von App-V bereitstellen, sollten Sie die folgenden Planungsinformationen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-113">Before you deploy Office 2016 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="28d1c-114">Unterstützte Office-Versionen und Office-Koexistenz</span><span class="sxs-lookup"><span data-stu-id="28d1c-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="28d1c-115">Verwenden Sie die folgende Tabelle, um Informationen zu unterstützten Versionen von Office und zum Ausführen von nebeneinander vorhandenen Versionen von Office zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="28d1c-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="28d1c-116">Zu überprüfende Informationen</span><span class="sxs-lookup"><span data-stu-id="28d1c-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="28d1c-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28d1c-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Supported versions of Microsoft Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="28d1c-118">Unterstützte Versionen von Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="28d1c-118">Supported versions of Microsoft Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28d1c-119">Unterstützte Office-Versionen</span><span class="sxs-lookup"><span data-stu-id="28d1c-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="28d1c-120">Unterstützte Bereitstellungstypen (beispielsweise Desktop, Personal Virtual Desktop Infrastructure (VDI), gebündelter VDI)</span><span class="sxs-lookup"><span data-stu-id="28d1c-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="28d1c-121">Office-Lizenzierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="28d1c-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with coexisting versions of Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)"><span data-ttu-id="28d1c-122">Planen der Verwendung von App-V mit vorhandenen Office-Versionen</span><span class="sxs-lookup"><span data-stu-id="28d1c-122">Planning for Using App-V with coexisting versions of Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28d1c-123">Überlegungen zum Installieren verschiedener Office-Versionen auf demselben Computer</span><span class="sxs-lookup"><span data-stu-id="28d1c-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="28d1c-124">Anforderungen für das Verpacken, veröffentlichen und bereitstellen</span><span class="sxs-lookup"><span data-stu-id="28d1c-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="28d1c-125">Bevor Sie Office mithilfe von App-V bereitstellen, überprüfen Sie die folgenden Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="28d1c-126">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="28d1c-126">Task</span></span></th>
<th align="left"><span data-ttu-id="28d1c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28d1c-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28d1c-128">Verpacken</span><span class="sxs-lookup"><span data-stu-id="28d1c-128">Packaging</span></span></p></td>
<td align="left">
<ul>
<li><p><span data-ttu-id="28d1c-129">Alle Office-Anwendungen, die Sie für Benutzer bereitstellen möchten, müssen sich in einem einzigen Paket befinden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="28d1c-130">In App-V 5,0 und höher müssen Sie das Office-Bereitstellungs Tool verwenden, um Pakete zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-130">In App-V 5.0 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="28d1c-131">Sie können den Sequencer nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="28d1c-132">Wenn Sie Microsoft Visio 2016 und Microsoft Project 2016 zusammen mit Office bereitstellen, müssen Sie diese in das gleiche Paket mit Office einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-132">If you are deploying Microsoft Visio 2016 and Microsoft Project 2016 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="28d1c-133">Weitere Informationen finden Sie unter <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)"> Bereitstellen von Visio 2016 und Project 2016 mit Office </a> .</span><span class="sxs-lookup"><span data-stu-id="28d1c-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2016 and Project 2016 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28d1c-134">Publishing</span><span class="sxs-lookup"><span data-stu-id="28d1c-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28d1c-135">Sie können auf jedem Clientcomputer nur ein Office-Paket veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="28d1c-136">Sie müssen das Office-Paket Global veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-136">You must publish the Office package globally.</span></span> <span data-ttu-id="28d1c-137">Sie können nicht für den Benutzer veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28d1c-138">Bereitstellen eines der folgenden Produkte auf einem freigegebenen Computer, beispielsweise mithilfe von Remote Desktop Diensten:</span><span class="sxs-lookup"><span data-stu-id="28d1c-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="28d1c-139">Microsoft 365-Apps für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="28d1c-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="28d1c-140">Visio pro für Office 365</span><span class="sxs-lookup"><span data-stu-id="28d1c-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="28d1c-141">Project pro für Office 365</span><span class="sxs-lookup"><span data-stu-id="28d1c-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="28d1c-142">Sie müssen die <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> Aktivierung gemeinsam genutzter Computer aktivieren </a> .</span><span class="sxs-lookup"><span data-stu-id="28d1c-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
</td>
</tr>
</tbody>
</table>



### <span data-ttu-id="28d1c-143">Ausschließen von Office-Anwendungen aus einem Paket</span><span class="sxs-lookup"><span data-stu-id="28d1c-143">Excluding Office applications from a package</span></span>

<span data-ttu-id="28d1c-144">In der folgenden Tabelle werden die empfohlenen Methoden zum Ausschließen bestimmter Office-Anwendungen aus einem Paket beschrieben.</span><span class="sxs-lookup"><span data-stu-id="28d1c-144">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="28d1c-145">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="28d1c-145">Task</span></span></th>
<th align="left"><span data-ttu-id="28d1c-146">Details</span><span class="sxs-lookup"><span data-stu-id="28d1c-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28d1c-147">Verwenden <strong> Sie die ExcludeApp </strong> -Einstellung, wenn Sie das Paket mithilfe des Office-Bereitstellungstools erstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-147">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28d1c-148">Ermöglicht das Ausschließen bestimmter Office-Anwendungen aus dem Paket, wenn das Office-Bereitstellungs Tool das Paket erstellt.</span><span class="sxs-lookup"><span data-stu-id="28d1c-148">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="28d1c-149">Mit dieser Einstellung können Sie beispielsweise ein Paket erstellen, das nur Microsoft Word enthält.</span><span class="sxs-lookup"><span data-stu-id="28d1c-149">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="28d1c-150">Weitere Informationen finden Sie unter <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> ExcludeApp-Element </a> .</span><span class="sxs-lookup"><span data-stu-id="28d1c-150">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28d1c-151">Ändern der DeploymentConfig.xml Datei</span><span class="sxs-lookup"><span data-stu-id="28d1c-151">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28d1c-152">Ändern Sie die DeploymentConfig.xml-Datei, nachdem das Paket erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="28d1c-152">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="28d1c-153">Diese Datei enthält die Standardpaket Einstellungen für alle Benutzer auf einem Computer, auf dem der App-V-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28d1c-153">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="28d1c-154">Weitere Informationen finden Sie unter <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)"> Deaktivieren von Office 2016-Anwendungen </a> .</span><span class="sxs-lookup"><span data-stu-id="28d1c-154">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)">Disabling Office 2016 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="28d1c-155">Erstellen eines Office 2016-Pakets für App-V mit dem Office-Bereitstellungs Tool</span><span class="sxs-lookup"><span data-stu-id="28d1c-155">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="28d1c-156">Führen Sie die folgenden Schritte aus, um ein Office 2016-Paket für App-V 5,0 oder höher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-156">Complete the following steps to create an Office 2016 package for App-V 5.0 or later.</span></span>

><span data-ttu-id="28d1c-157">**Important** &nbsp; Wichtig &nbsp; In App-V 5,0 und höher müssen Sie das Office-Bereitstellungs Tool verwenden, um ein Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-157">**Important**&nbsp;&nbsp;In App-V 5.0 and later, you must use the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="28d1c-158">Sie können den Sequencer nicht zum Erstellen von Paketen verwenden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-158">You cannot use the Sequencer to create packages.</span></span>

### <span data-ttu-id="28d1c-159">Überprüfen der Voraussetzungen für die Verwendung des Office-Bereitstellungstools</span><span class="sxs-lookup"><span data-stu-id="28d1c-159">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="28d1c-160">Der Computer, auf dem Sie das Office-Bereitstellungs Tool installieren, muss Folgendes aufweisen:</span><span class="sxs-lookup"><span data-stu-id="28d1c-160">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="28d1c-161">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="28d1c-161">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="28d1c-162">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28d1c-162">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28d1c-163">Erforderliche Software</span><span class="sxs-lookup"><span data-stu-id="28d1c-163">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="28d1c-164">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="28d1c-164">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28d1c-165">Unterstützte Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="28d1c-165">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28d1c-166">64-Bit-Version von Windows 10</span><span class="sxs-lookup"><span data-stu-id="28d1c-166">64-bit version of Windows 10</span></span></p></li>
<li><p><span data-ttu-id="28d1c-167">64-Bit-Version von Windows 8 oder 8,1</span><span class="sxs-lookup"><span data-stu-id="28d1c-167">64-bit version of Windows 8 or 8.1</span></span></p></li>
<li><p><span data-ttu-id="28d1c-168">64-Bit-Version von Windows 7</span><span class="sxs-lookup"><span data-stu-id="28d1c-168">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


><span data-ttu-id="28d1c-169">**Hinweis**  In diesem Thema bezieht sich der Begriff "Office 2016 App-V-Paket" auf die Abonnementlizenzierung.</span><span class="sxs-lookup"><span data-stu-id="28d1c-169">**Note**  In this topic, the term “Office 2016 App-V package” refers to subscription licensing.</span></span>


### <span data-ttu-id="28d1c-170">Erstellen von Office 2016-App-V-Paketen mithilfe des Office-Bereitstellungstools</span><span class="sxs-lookup"><span data-stu-id="28d1c-170">Create Office 2016 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="28d1c-171">Sie erstellen Office 2016-App-V-Pakete mithilfe des Office-Bereitstellungstools.</span><span class="sxs-lookup"><span data-stu-id="28d1c-171">You create Office 2016 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="28d1c-172">Die folgenden Anweisungen erläutern, wie Sie ein Office 2016-App-V-Paket mit Abonnementlizenzierung erstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-172">The following instructions explain how to create an Office 2016 App-V package with Subscription Licensing.</span></span>

<span data-ttu-id="28d1c-173">Erstellen Sie Office 2016-App-V-Pakete auf 64-Bit-Windows-Computern.</span><span class="sxs-lookup"><span data-stu-id="28d1c-173">Create Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="28d1c-174">Nach der Erstellung wird das Office 2016-App-V-Paket auf Computern mit 32-Bit und 64-Bit Windows 7, Windows 8,1 und Windows 10 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28d1c-174">Once created, the Office 2016 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="28d1c-175">Herunterladen des Office-Bereitstellungstools</span><span class="sxs-lookup"><span data-stu-id="28d1c-175">Download the Office Deployment Tool</span></span>

<span data-ttu-id="28d1c-176">Office 2016-App-v-Pakete werden mit dem Office-Bereitstellungs Tool erstellt, das ein Office 2016-App-v-Paket generiert.</span><span class="sxs-lookup"><span data-stu-id="28d1c-176">Office 2016 App-V Packages are created using the Office Deployment Tool, which generates an Office 2016 App-V Package.</span></span> <span data-ttu-id="28d1c-177">Das Paket kann nicht über den App-V-Sequenzer erstellt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-177">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="28d1c-178">So beginnen Sie die Paketerstellung:</span><span class="sxs-lookup"><span data-stu-id="28d1c-178">To begin package creation:</span></span>

1.  <span data-ttu-id="28d1c-179">Laden [Sie das Office 2016-Bereitstellungs Tool für Klick-und-Los](https://www.microsoft.com/download/details.aspx?id=49117)herunter.</span><span class="sxs-lookup"><span data-stu-id="28d1c-179">Download the [Office 2016 Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=49117).</span></span>

> <span data-ttu-id="28d1c-180">**Wichtig** Sie müssen das Office 2016-Bereitstellungs Tool verwenden, um Office 2016-App-V-Pakete zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-180">**Important** You must use the Office 2016 Deployment Tool to create Office 2016 App-V Packages.</span></span>
> 2. <span data-ttu-id="28d1c-181">Führen Sie die exe-Datei aus, und extrahieren Sie die zugehörigen Features an den gewünschten Speicherort.</span><span class="sxs-lookup"><span data-stu-id="28d1c-181">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="28d1c-182">Um diesen Vorgang zu vereinfachen, können Sie einen freigegebenen Netzwerkordner erstellen, in dem die Features gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-182">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    Example: \\\\Server\\Office2016

3. <span data-ttu-id="28d1c-183">Überprüfen Sie, ob eine setup.exe und eine configuration.xml Datei vorhanden sind und sich an dem von Ihnen angegebenen Speicherort befinden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-183">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="28d1c-184">Herunterladen von Office 2016-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="28d1c-184">Download Office 2016 applications</span></span>

<span data-ttu-id="28d1c-185">Nachdem Sie das Office-Bereitstellungs Tool heruntergeladen haben, können Sie es verwenden, um die neuesten Office 2016-Anwendungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="28d1c-185">After you download the Office Deployment Tool, you can use it to get the latest Office 2016 applications.</span></span> <span data-ttu-id="28d1c-186">Nachdem Sie die Office-Anwendungen erhalten haben, erstellen Sie das Office 2016-App-V-Paket.</span><span class="sxs-lookup"><span data-stu-id="28d1c-186">After getting the Office applications, you create the Office 2016 App-V package.</span></span>

<span data-ttu-id="28d1c-187">Die im Office-Bereitstellungs Tool enthaltene XML-Datei gibt die Produkt Details an, beispielsweise die enthaltenen Sprachen und Office-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-187">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1. <span data-ttu-id="28d1c-188">**Passen Sie die Beispiel-XML-Konfigurationsdatei an:** Verwenden Sie die Beispiel-XML-Konfigurationsdatei, die Sie mit dem Office-Bereitstellungs Tool heruntergeladen haben, um die Office-Anwendungen anzupassen:</span><span class="sxs-lookup"><span data-stu-id="28d1c-188">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

   1. <span data-ttu-id="28d1c-189">Öffnen Sie die XML-Beispieldatei im Editor oder in Ihrem bevorzugten Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="28d1c-189">Open the sample XML file in Notepad or your favorite text editor.</span></span>

   2. <span data-ttu-id="28d1c-190">Wenn die Beispiel configuration.xml-Datei geöffnet und zur Bearbeitung bereit ist, können Sie Produkte, Sprachen und den Pfad angeben, in dem Sie die Office 2016-Anwendungen speichern.</span><span class="sxs-lookup"><span data-stu-id="28d1c-190">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2016 applications.</span></span> <span data-ttu-id="28d1c-191">Der folgende Code ist ein einfaches Beispiel für die configuration.xml-Datei:</span><span class="sxs-lookup"><span data-stu-id="28d1c-191">The following is a basic example of the configuration.xml file:</span></span>

      ```xml
      <Configuration>
         <Add SourcePath= "\\Server\Office2016” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      ><span data-ttu-id="28d1c-192">**Hinweis**  Das Konfigurations-XML ist eine XML-Beispieldatei.</span><span class="sxs-lookup"><span data-stu-id="28d1c-192">**Note**  The configuration XML is a sample XML file.</span></span> <span data-ttu-id="28d1c-193">Die Datei enthält Zeilen, die auskommentiert werden. Sie können diese Zeilen "kommentieren", um zusätzliche Einstellungen für die Datei anzupassen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-193">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span> <span data-ttu-id="28d1c-194">Wenn Sie diese Zeilen "kommentieren" möchten, entfernen Sie die "<!</span><span class="sxs-lookup"><span data-stu-id="28d1c-194">To “uncomment” these lines, remove the "<!</span></span> <span data-ttu-id="28d1c-195">--"vom Anfang der Zeile und der"--> "vom Ende der Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="28d1c-195">- -" from the beginning of the line, and the "-- >" from the end of the line.</span></span>

      <span data-ttu-id="28d1c-196">In der obigen XML-Konfigurationsdatei wird angegeben, dass die Office 2016 ProPlus 32-Bit-Edition, einschließlich Visio ProPlus, in Englisch auf das \\\\server\\Office 2016 heruntergeladen wird, dem Speicherort, in dem Office-Anwendungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-196">The above XML configuration file specifies that Office 2016 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2016, which is the location where Office applications will be saved to.</span></span> <span data-ttu-id="28d1c-197">Beachten Sie, dass sich die Produkt-ID der Anwendungen nicht auf die endgültige Lizenzierung von Office auswirkt.</span><span class="sxs-lookup"><span data-stu-id="28d1c-197">Note that the Product ID of the applications will not affect the final licensing of Office.</span></span> <span data-ttu-id="28d1c-198">Office 2016-App-V-Pakete mit unterschiedlicher Lizenzierung können über die gleichen Anwendungen erstellt werden, indem die Lizenzierung in einem späteren Schritt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="28d1c-198">Office 2016 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage.</span></span> <span data-ttu-id="28d1c-199">In der folgenden Tabelle sind die anpassbaren Attribute und Elemente der XML-Datei zusammengefasst:</span><span class="sxs-lookup"><span data-stu-id="28d1c-199">The table below summarizes the customizable attributes and elements of XML file:</span></span>

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left"><span data-ttu-id="28d1c-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28d1c-200">Input</span></span></th>
      <th align="left"><span data-ttu-id="28d1c-201">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28d1c-201">Description</span></span></th>
      <th align="left"><span data-ttu-id="28d1c-202">Beispiel</span><span class="sxs-lookup"><span data-stu-id="28d1c-202">Example</span></span></th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="28d1c-203">Element hinzufügen</span><span class="sxs-lookup"><span data-stu-id="28d1c-203">Add element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="28d1c-204">Gibt die Produkte und Sprachen an, die in das Paket eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-204">Specifies the products and languages to include in the package.</span></span></p></td>
      <td align="left"><p><span data-ttu-id="28d1c-205">n.v.</span><span class="sxs-lookup"><span data-stu-id="28d1c-205">N/A</span></span></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="28d1c-206">OfficeClientEdition (Attribut des Add-Elements)</span><span class="sxs-lookup"><span data-stu-id="28d1c-206">OfficeClientEdition (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="28d1c-207">Gibt die Edition des zu verwendenden Office 2016-Produkts an: 32-Bit oder 64-Bit.</span><span class="sxs-lookup"><span data-stu-id="28d1c-207">Specifies the edition of Office 2016 product to use: 32-bit or 64-bit.</span></span> <span data-ttu-id="28d1c-208">Der Vorgang schlägt fehl <strong> , wenn OfficeClientEdition </strong> nicht auf einen gültigen Wert gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="28d1c-208">The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</span></span></p></td>
      <td align="left"><p><strong><span data-ttu-id="28d1c-209">OfficeClientEdition </strong> = &quot; 32&quot;</span><span class="sxs-lookup"><span data-stu-id="28d1c-209">OfficeClientEdition</strong>=&quot;32&quot;</span></span></p>
      <p><strong><span data-ttu-id="28d1c-210">OfficeClientEdition </strong> = &quot; 64&quot;</span><span class="sxs-lookup"><span data-stu-id="28d1c-210">OfficeClientEdition</strong>=&quot;64&quot;</span></span></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="28d1c-211">Product-Element</span><span class="sxs-lookup"><span data-stu-id="28d1c-211">Product element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="28d1c-212">Gibt die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="28d1c-212">Specifies the application.</span></span> <span data-ttu-id="28d1c-213">Project 2016 und Visio 2016 müssen hier als hinzugefügtes Produkt angegeben werden, das in die Anwendungen aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="28d1c-213">Project 2016 and Visio 2016 must be specified here as an added product to be included in the applications.</span></span>

      <span data-ttu-id="28d1c-214">Weitere Informationen zu den Produkt-IDs finden Sie unter vom <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)"> Office-Bereitstellungs Tool unterstützte Produkt-IDs für Klick-und-los.</span><span class="sxs-lookup"><span data-stu-id="28d1c-214">For more information about the product IDs, see <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)">Product IDs that are supported by the Office Deployment Tool for Click-to-Run</span></span></a>
      </p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      </td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="28d1c-215">Language-Element</span><span class="sxs-lookup"><span data-stu-id="28d1c-215">Language element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="28d1c-216">Gibt die Sprache an, die in den Anwendungen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="28d1c-216">Specifies the language supported in the applications</span></span></p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="28d1c-217">Version (Attribut des Add-Elements)</span><span class="sxs-lookup"><span data-stu-id="28d1c-217">Version (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="28d1c-218">Optional.</span><span class="sxs-lookup"><span data-stu-id="28d1c-218">Optional.</span></span> <span data-ttu-id="28d1c-219">Gibt einen Build an, der für das Paket verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="28d1c-219">Specifies a build to use for the package</span></span></p>
      <p><span data-ttu-id="28d1c-220">Standardwert für den neuesten angekündigten Build (wie in v32.CAB in der Office-Quelle definiert).</span><span class="sxs-lookup"><span data-stu-id="28d1c-220">Defaults to latest advertised build (as defined in v32.CAB at the Office source).</span></span></p></td>
      <td align="left"><p><code>16.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="28d1c-221">SourcePath (Attribut des Add-Elements)</span><span class="sxs-lookup"><span data-stu-id="28d1c-221">SourcePath (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="28d1c-222">Gibt den Speicherort an, in dem die Anwendungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-222">Specifies the location in which the applications will be saved to.</span></span></p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2016”</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="28d1c-223">Kanal (Attribut des Add-Elements)</span><span class="sxs-lookup"><span data-stu-id="28d1c-223">Channel (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="28d1c-224">Optional.</span><span class="sxs-lookup"><span data-stu-id="28d1c-224">Optional.</span></span> <span data-ttu-id="28d1c-225">Gibt den Update Kanal für das Produkt an, das heruntergeladen oder installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="28d1c-225">Specifies the update channel for the product that you want to download or install.</span></span> </p><p><span data-ttu-id="28d1c-226">Weitere Informationen zu Update Kanälen finden Sie unter Übersicht über die Update Kanäle für Microsoft 365-Apps für Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-226">For more information about update channels, see Overview of update channels for Microsoft 365 Apps for enterprise.</span></span></p></td>
      <td align="left"><p><code>Channel=&quot;Deferred&quot;</code></p></td>
      </tr>
      </tbody>
      </table>

      <span data-ttu-id="28d1c-227">Nachdem Sie die configuration.xml-Datei bearbeitet haben, um das gewünschte Produkt, die Sprachen und auch den Speicherort anzugeben, auf dem die Office 2016-Anwendungen gespeichert werden, können Sie beispielsweise die Konfigurationsdatei als Customconfig.xml speichern.</span><span class="sxs-lookup"><span data-stu-id="28d1c-227">After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2016 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.</span></span>

2. <span data-ttu-id="28d1c-228">**Laden Sie die Anwendungen in den angegebenen Speicherort herunter:** Verwenden Sie eine Eingabeaufforderung mit erhöhten Rechten und ein 64-Bit-Betriebssystem, um die Office 2016-Anwendungen herunterzuladen, die später in ein App-V-Paket konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-228">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2016 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="28d1c-229">Im folgenden finden Sie einen Beispielbefehl mit einer Beschreibung der Details:</span><span class="sxs-lookup"><span data-stu-id="28d1c-229">Below is an example command with a description of details:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /download \\server\Office2016\Customconfig.xml
   ```

   <span data-ttu-id="28d1c-230">Im Beispiel:</span><span class="sxs-lookup"><span data-stu-id="28d1c-230">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="28d1c-231">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="28d1c-231">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-232">der Speicherort des Netzwerkspeichers, der das Office-Bereitstellungs Tool und die benutzerdefinierte Configuration.xml Datei enthält, Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="28d1c-232">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="28d1c-233">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="28d1c-233">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-234">ist das Office-Bereitstellungs Tool.</span><span class="sxs-lookup"><span data-stu-id="28d1c-234">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="28d1c-235">/Download</span><span class="sxs-lookup"><span data-stu-id="28d1c-235">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-236">downloadet die Office 2016-Anwendungen, die Sie in der customConfig.xml-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="28d1c-236">downloads the Office 2016 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="28d1c-237">Diese Bits können später in einem Office 2016-App-V-Paket mit Volumenlizenzierung konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-237">These bits can be later converted in an Office 2016 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="28d1c-238">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="28d1c-238">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-239">übergibt die XML-Konfigurationsdatei, die zum Abschließen des Downloadprozesses erforderlich ist, in diesem Beispiel customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="28d1c-239">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="28d1c-240">Nach Verwendung des Befehls "Download" sollten sich die Office-Anwendungen an dem Speicherort befinden, der in der XML-Konfigurationsdatei angegeben ist, in diesem Beispiel \Server\Office2016.</span><span class="sxs-lookup"><span data-stu-id="28d1c-240">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2016.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="28d1c-241">Konvertieren der Office-Anwendungen in ein App-V-Paket</span><span class="sxs-lookup"><span data-stu-id="28d1c-241">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="28d1c-242">Nachdem Sie die Office 2016-Anwendungen über das Office-Bereitstellungstool heruntergeladen haben, verwenden Sie das Office-Bereitstellungstool, um Sie in ein Office 2016 App-V-Paket umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="28d1c-242">After you download the Office 2016 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2016 App-V package.</span></span> <span data-ttu-id="28d1c-243">Führen Sie die Schritte aus, die Ihrem Lizenzierungsmodell entsprechen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-243">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="28d1c-244">Zusammenfassung der erforderlichen Schritte:</span><span class="sxs-lookup"><span data-stu-id="28d1c-244">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="28d1c-245">Erstellen Sie die Office 2016-App-V-Pakete auf 64-Bit-Windows-Computern.</span><span class="sxs-lookup"><span data-stu-id="28d1c-245">Create the Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="28d1c-246">Das Paket wird jedoch auf 32-Bit-und 64-Bit-Computern unter Windows 7, Windows 8 oder 8,1 und Windows 10 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28d1c-246">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8 or 8.1, and Windows 10 computers.</span></span>

-   <span data-ttu-id="28d1c-247">Erstellen Sie mithilfe des Office-Bereitstellungstools ein Office App-V-Paket für das Abonnement Lizenzierungs Paket, und ändern Sie dann die CustomConfig.xml-Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="28d1c-247">Create an Office App-V package for Subscription Licensing package by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="28d1c-248">In der folgenden Tabelle sind die Werte zusammengefasst, die Sie in die CustomConfig.xml-Datei für das verwendete Lizenzierungsmodell eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-248">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="28d1c-249">Die Schritte in den Abschnitten, die der Tabelle folgen, geben die genauen Einträge an, die Sie vornehmen müssen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-249">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

><span data-ttu-id="28d1c-250">**Note** &nbsp; Hinweis &nbsp; Sie können das Office-Bereitstellungs Tool verwenden, um App-V-Pakete für Microsoft 365-Apps für Unternehmen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-250">**Note**&nbsp;&nbsp;You can use the Office Deployment Tool to create App-V packages for Microsoft 365 Apps for enterprise.</span></span> <span data-ttu-id="28d1c-251">Das Erstellen von Paketen für die Volumen lizenzierten Versionen von Office Professional Plus oder Office Standard wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="28d1c-251">Creating packages for the volume-licensed versions of Office Professional Plus or Office Standard is not supported.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="28d1c-252">Produkt-ID</span><span class="sxs-lookup"><span data-stu-id="28d1c-252">Product ID</span></span></th>
<th align="left"><span data-ttu-id="28d1c-253">Abonnementlizenzierung</span><span class="sxs-lookup"><span data-stu-id="28d1c-253">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="28d1c-254">Office2016</span><span class="sxs-lookup"><span data-stu-id="28d1c-254">Office 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="28d1c-255">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="28d1c-255">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="28d1c-256">Office 2016 mit Visio 2016</span><span class="sxs-lookup"><span data-stu-id="28d1c-256">Office 2016 with Visio 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="28d1c-257">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="28d1c-257">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="28d1c-258">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="28d1c-258">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="28d1c-259">Office 2016 mit Visio 2016 und Project 2016</span><span class="sxs-lookup"><span data-stu-id="28d1c-259">Office 2016 with Visio 2016 and Project 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="28d1c-260">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="28d1c-260">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="28d1c-261">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="28d1c-261">VisioProRetail</span></span></p>
<p><span data-ttu-id="28d1c-262">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="28d1c-262">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="28d1c-263">Konvertieren der Office-Anwendungen in ein App-V-Paket</span><span class="sxs-lookup"><span data-stu-id="28d1c-263">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="28d1c-264">Öffnen Sie die CustomConfig.xml Datei in Editor erneut, und nehmen Sie die folgenden Änderungen an der Datei vor:</span><span class="sxs-lookup"><span data-stu-id="28d1c-264">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="28d1c-265">Parameter</span><span class="sxs-lookup"><span data-stu-id="28d1c-265">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="28d1c-266">So ändern Sie den Wert</span><span class="sxs-lookup"><span data-stu-id="28d1c-266">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="28d1c-267">SourcePath</span><span class="sxs-lookup"><span data-stu-id="28d1c-267">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-268">Zeigen Sie auf die zuvor heruntergeladenen Office-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-268">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="28d1c-269">ProductID</span><span class="sxs-lookup"><span data-stu-id="28d1c-269">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-270">Geben Sie die Abonnementlizenzierung an, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="28d1c-270">Specify Subscription licensing, as shown in the following example:</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2016&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="28d1c-271">In diesem Beispiel wurden die folgenden Änderungen zum Erstellen eines Pakets mit Abonnementlizenzierung vorgenommen:</span><span class="sxs-lookup"><span data-stu-id="28d1c-271">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="28d1c-272">SourcePath</span><span class="sxs-lookup"><span data-stu-id="28d1c-272">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-273">ist der Pfad, der geändert wurde, um auf die Office-Anwendungen zu verweisen, die zuvor heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-273">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="28d1c-274">Produkt-ID</span><span class="sxs-lookup"><span data-stu-id="28d1c-274">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-275">für Office wurde geändert in <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="28d1c-275">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="28d1c-276">Produkt-ID</span><span class="sxs-lookup"><span data-stu-id="28d1c-276">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-277">für Visio wurde geändert in <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="28d1c-277">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p></p>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="28d1c-278">ExcludeApp (optional)</span><span class="sxs-lookup"><span data-stu-id="28d1c-278">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-279">Mit dieser Option können Sie Office-Programme angeben, die nicht im App-V-Paket enthalten sein sollen, das vom Office-Bereitstellungs Tool erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="28d1c-279">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="28d1c-280">So können Sie beispielsweise Access und InfoPath ausschließen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-280">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="28d1c-281">PACKAGEGUID (optional)</span><span class="sxs-lookup"><span data-stu-id="28d1c-281">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-282">Standardmäßig verwenden alle App-v-Pakete, die vom Office-Bereitstellungs Tool erstellt wurden, dieselbe App-v-Paket-ID.</span><span class="sxs-lookup"><span data-stu-id="28d1c-282">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="28d1c-283">Sie können PACKAGEGUID verwenden, um eine andere Paket-ID für jedes Paket anzugeben, mit der Sie mehrere App-v-Pakete, die vom Office-Bereitstellungs Tool erstellt wurden, veröffentlichen und mithilfe des App-v-Servers verwalten können.</span><span class="sxs-lookup"><span data-stu-id="28d1c-283">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="28d1c-284">Ein Beispiel für die Verwendung dieses Parameters ist, wenn Sie unterschiedliche Pakete für verschiedene Benutzer erstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-284">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="28d1c-285">So können Sie beispielsweise ein Paket mit Office 2016 für einige Benutzer erstellen und ein weiteres Paket mit Office 2016 und Visio 2016 für eine andere Gruppe von Benutzern erstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-285">For example, you can create a package with just Office 2016 for some users, and create another package with Office 2016 and Visio 2016 for another set of users.</span></span></p>
<span data-ttu-id="28d1c-286">&gt;<strong>Hinweis </strong> auch wenn Sie eindeutige Paket-IDs verwenden, können Sie weiterhin nur ein App-V-Paket auf einem einzelnen Gerät bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-286">&gt;<strong>Note</strong> Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span>
   </td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="28d1c-287">Verwenden Sie den Befehl/Packager, um die Office-Anwendungen in ein Office 2016-App-V-Paket umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="28d1c-287">Use the /packager command to convert the Office applications to an Office 2016 App-V package.</span></span>

   <span data-ttu-id="28d1c-288">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="28d1c-288">For example:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /packager \\server\Office2016\Customconfig.xml  \\server\share\Office2016AppV
   ```

   <span data-ttu-id="28d1c-289">Im Beispiel:</span><span class="sxs-lookup"><span data-stu-id="28d1c-289">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="28d1c-290">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="28d1c-290">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-291">der Speicherort des Netzwerkspeichers, der das Office-Bereitstellungs Tool und die benutzerdefinierte Configuration.xml Datei enthält, Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="28d1c-291">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="28d1c-292">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="28d1c-292">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-293">ist das Office-Bereitstellungs Tool.</span><span class="sxs-lookup"><span data-stu-id="28d1c-293">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="28d1c-294">/packager</span><span class="sxs-lookup"><span data-stu-id="28d1c-294">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-295">erstellt das Office 2016-App-V-Paket mit der Art der Lizenzierung, die in der customConfig.xml-Datei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="28d1c-295">creates the Office 2016 App-V package with the type of licensing specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="28d1c-296">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="28d1c-296">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-297">übergibt die Konfigurations-XML-Datei (in diesem Fall customConfig), die für die Paket Phase vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="28d1c-297">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="28d1c-298">\server\share\Office 2016AppV</span><span class="sxs-lookup"><span data-stu-id="28d1c-298">\server\share\Office 2016AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="28d1c-299">Gibt den Speicherort des neu erstellten Office App-V-Pakets an.</span><span class="sxs-lookup"><span data-stu-id="28d1c-299">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2016 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note** To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="28d1c-300">Überprüfen Sie, ob das Office 2016-App-V-Paket ordnungsgemäß funktioniert:</span><span class="sxs-lookup"><span data-stu-id="28d1c-300">Verify that the Office 2016 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="28d1c-301">Veröffentlichen Sie das von Ihnen Global erstellte Office 2016 App-V-Paket auf einem Testcomputer, und überprüfen Sie, ob die Office 2016-Verknüpfungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-301">Publish the Office 2016 App-V package, which you created globally, to a test computer, and verify that the Office 2016 shortcuts appear.</span></span>

   2.  <span data-ttu-id="28d1c-302">Starten Sie einige Office 2016-Anwendungen wie Excel oder Word, um sicherzustellen, dass Ihr Paket wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="28d1c-302">Start a few Office 2016 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="28d1c-303">Veröffentlichen des Office-Pakets für App-V</span><span class="sxs-lookup"><span data-stu-id="28d1c-303">Publishing the Office package for App-V</span></span>


<span data-ttu-id="28d1c-304">Verwenden Sie die folgenden Informationen zum Veröffentlichen eines Office-Pakets.</span><span class="sxs-lookup"><span data-stu-id="28d1c-304">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="28d1c-305">Methoden zum Veröffentlichen von Office App-V-Paketen</span><span class="sxs-lookup"><span data-stu-id="28d1c-305">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="28d1c-306">Stellen Sie das App-V-Paket für Office 2016 mithilfe der gleichen Methoden bereit, die Sie für jedes andere Paket verwenden:</span><span class="sxs-lookup"><span data-stu-id="28d1c-306">Deploy the App-V package for Office 2016 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="28d1c-307">System Center Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="28d1c-307">System Center Configuration Manager</span></span>

-   <span data-ttu-id="28d1c-308">App-V-Server</span><span class="sxs-lookup"><span data-stu-id="28d1c-308">App-V Server</span></span>

-   <span data-ttu-id="28d1c-309">Eigenständige über PowerShell-Befehle</span><span class="sxs-lookup"><span data-stu-id="28d1c-309">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="28d1c-310">Voraussetzungen und Anforderungen für die Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="28d1c-310">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="28d1c-311">Voraussetzungen oder Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28d1c-311">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="28d1c-312">Details</span><span class="sxs-lookup"><span data-stu-id="28d1c-312">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28d1c-313">Aktivieren von PowerShell-Skripts für die App-V-Clients</span><span class="sxs-lookup"><span data-stu-id="28d1c-313">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="28d1c-314">Zum Veröffentlichen von Office 2016-Paketen müssen Sie ein Skript ausführen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-314">To publish Office 2016 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="28d1c-315">Paket Skripts sind auf App-V-Clients standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="28d1c-315">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="28d1c-316">Führen Sie zum Aktivieren der Skripterstellung den folgenden PowerShell-Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="28d1c-316">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28d1c-317">Veröffentlichen des Office 2016-Pakets auf globaler Ebene</span><span class="sxs-lookup"><span data-stu-id="28d1c-317">Publish the Office 2016 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="28d1c-318">Erweiterungspunkte im Office App-V-Paket erfordern die Installation auf Computerebene.</span><span class="sxs-lookup"><span data-stu-id="28d1c-318">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="28d1c-319">Wenn Sie auf Computerebene veröffentlichen, werden keine Voraussetzungen oder verteilbaren Aktionen benötigt, und das Office 2016-Paket ermöglicht es, dass seine Anwendungen wie nativ installierte Office funktionieren, sodass Administratoren keine Pakete anpassen müssen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-319">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2016 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="28d1c-320">Veröffentlichen eines Office-Pakets</span><span class="sxs-lookup"><span data-stu-id="28d1c-320">How to publish an Office package</span></span>

<span data-ttu-id="28d1c-321">Führen Sie den folgenden Befehl aus, um ein Office-Paket global zu veröffentlichen:</span><span class="sxs-lookup"><span data-stu-id="28d1c-321">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="28d1c-322">Über die Web-Verwaltungskonsole auf dem App-V-Server können Sie einer Gruppe von Computern Berechtigungen hinzufügen, anstatt einer Benutzergruppe, um zu ermöglichen, dass Pakete Global auf den Computern in der entsprechenden Gruppe veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-322">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="28d1c-323">Anpassen und Verwalten von Office App-V-Paketen</span><span class="sxs-lookup"><span data-stu-id="28d1c-323">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="28d1c-324">Zum Verwalten Ihrer Office-App-V-Pakete verwenden Sie die gleichen Vorgänge wie für jedes andere Paket, doch es gibt ein paar Ausnahmen, wie in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="28d1c-324">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="28d1c-325">Aktivieren von Office-Plug-Ins mithilfe von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="28d1c-325">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="28d1c-326">Deaktivieren von Office 2016-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="28d1c-326">Disabling Office 2016 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="28d1c-327">Deaktivieren von Office 2016-Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="28d1c-327">Disabling Office 2016 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="28d1c-328">Verwalten von Office 2016-Paket Upgrades</span><span class="sxs-lookup"><span data-stu-id="28d1c-328">Managing Office 2016 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="28d1c-329">Bereitstellen von Visio 2016 und Project 2016 mit Office</span><span class="sxs-lookup"><span data-stu-id="28d1c-329">Deploying Visio 2016 and Project 2016 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="28d1c-330">Aktivieren von Office-Plug-Ins mithilfe von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="28d1c-330">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="28d1c-331">Führen Sie die Schritte in diesem Abschnitt aus, um Office-Plug-ins mit Ihrem Office-Paket zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="28d1c-331">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="28d1c-332">Um Office-Plug-ins zu verwenden, müssen Sie den App-V-Sequenzer verwenden, um ein separates Paket zu erstellen, das nur die Plug-Ins enthält. Sie können das Office-Bereitstellungs Tool nicht verwenden, um das Plug-in-Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-332">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="28d1c-333">Sie erstellen dann eine Verbindungsgruppe, die das Office-Paket und das Plug-in-Paket enthält, wie in den folgenden Schritten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="28d1c-333">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="28d1c-334">So aktivieren Sie Plug-Ins für Office App-V-Pakete</span><span class="sxs-lookup"><span data-stu-id="28d1c-334">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="28d1c-335">Fügen Sie mithilfe von App-V Server, System Center Configuration Manager oder einem PowerShell-Cmdlet eine Verbindungsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="28d1c-335">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="28d1c-336">Sequenzieren Sie Ihre Plug-Ins mithilfe des App-V-Sequencers.</span><span class="sxs-lookup"><span data-stu-id="28d1c-336">Sequence your plug-ins using the App-V Sequencer.</span></span> <span data-ttu-id="28d1c-337">Stellen Sie sicher, dass Office 2016 auf dem Computer installiert ist, der zur Sequenzierung des Plug-ins verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="28d1c-337">Ensure that Office 2016 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="28d1c-338">Es wird empfohlen, Microsoft 365-Apps für Enterprise (nicht-virtuell) auf dem Sequenzcomputer zu verwenden, wenn Sie Office 2016-Plug-ins abgleichen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-338">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2016 plug-ins.</span></span>

3.  <span data-ttu-id="28d1c-339">Erstellen Sie ein App-V-Paket, das die gewünschten Plug-Ins enthält.</span><span class="sxs-lookup"><span data-stu-id="28d1c-339">Create an App-V package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="28d1c-340">Fügen Sie mithilfe von App-V Server, System Center Configuration Manager oder einem PowerShell-Cmdlet eine Verbindungsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="28d1c-340">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="28d1c-341">Fügen Sie das Office 2016-App-V-Paket und das Plug-in-Paket, das Sie sequenziert haben, zu der von Ihnen erstellten Verbindungsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="28d1c-341">Add the Office 2016 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    ><span data-ttu-id="28d1c-342">**Wichtig** Die Reihenfolge der Pakete in der Verbindungsgruppe bestimmt die Reihenfolge, in der die Paketinhalte zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-342">**Important** The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="28d1c-343">Fügen Sie in ihrer Beschreibungsdatei für die Verbindungsgruppe zuerst das Office 2016-App-v-Paket hinzu, und fügen Sie dann das Plug-in-App-v-Paket hinzu.</span><span class="sxs-lookup"><span data-stu-id="28d1c-343">In your Connection group descriptor file, add the Office 2016 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="28d1c-344">Stellen Sie sicher, dass beide Pakete auf dem Zielcomputer veröffentlicht werden und dass das Plug-in-Paket Global veröffentlicht wird, um die globalen Einstellungen des veröffentlichten Office 2016-App-V-Pakets zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-344">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2016 App-V package.</span></span>

7.  <span data-ttu-id="28d1c-345">Überprüfen Sie, ob die Bereitstellungs Konfigurationsdatei des Plug-in-Pakets die gleichen Einstellungen wie das Office 2016-App-V-Paket aufweist.</span><span class="sxs-lookup"><span data-stu-id="28d1c-345">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2016 App-V package has.</span></span>

    <span data-ttu-id="28d1c-346">Da das Office 2016-App-V-Paket in das Betriebssystem integriert ist, sollten die Einstellungen für das Plug-in-Paket übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-346">Since the Office 2016 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="28d1c-347">Sie können die Konfigurationsdatei für die Bereitstellung nach "com-Modus" Durchsuchen und sicherstellen, dass Ihr Plug-in-Paket diesen Wert als "integriert" festgesetzt hat und sowohl "InProcessEnabled" als auch "OutOfProcessEnabled" den Einstellungen des veröffentlichten Office 2016-App-V-Pakets entsprechen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-347">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2016 App-V package you published.</span></span>

8.  <span data-ttu-id="28d1c-348">Öffnen Sie die Konfigurationsdatei für die Bereitstellung, und legen Sie den Wert für **Objekte** auf **false**fest.</span><span class="sxs-lookup"><span data-stu-id="28d1c-348">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="28d1c-349">Wenn Sie nach der Sequenzierung Änderungen an der Konfigurationsdatei für die Bereitstellung vorgenommen haben, stellen Sie sicher, dass das Plug-in-Paket mit der Datei veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="28d1c-349">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="28d1c-350">Stellen Sie sicher, dass die von Ihnen erstellte Verbindungsgruppe auf dem gewünschten Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="28d1c-350">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="28d1c-351">Die erstellte Verbindungsgruppe wird wahrscheinlich "aussetzen", wenn das Office 2016-App-V-Paket verwendet wird, wenn die Verbindungsgruppe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="28d1c-351">The Connection Group created will likely “pend” if the Office 2016 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="28d1c-352">In diesem Fall müssen Sie den Neustart durchführen, um die Verbindungsgruppe erfolgreich zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="28d1c-352">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="28d1c-353">Nachdem Sie beide Pakete erfolgreich veröffentlicht und die Verbindungsgruppe aktiviert haben, starten Sie die Office 2016-Zielanwendung, und stellen Sie sicher, dass das von Ihnen veröffentlichte und der Verbindungsgruppe hinzugefügte Plug-in wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="28d1c-353">After you successfully publish both packages and enable the Connection Group, start the target Office 2016 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="28d1c-354">Deaktivieren von Office 2016-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="28d1c-354">Disabling Office 2016 applications</span></span>

<span data-ttu-id="28d1c-355">Möglicherweise möchten Sie bestimmte Anwendungen in Ihrem Office App-V-Paket deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="28d1c-355">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="28d1c-356">So können Sie beispielsweise den Zugriff deaktivieren, aber alle anderen Office-Anwendungen Main verfügbar lassen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-356">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="28d1c-357">Wenn Sie eine Anwendung deaktivieren, wird dem Endbenutzer die Verknüpfung für diese Anwendung nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28d1c-357">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="28d1c-358">Sie müssen die Anwendung nicht neu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="28d1c-358">You do not have to re-sequence the application.</span></span> <span data-ttu-id="28d1c-359">Wenn Sie die Konfigurationsdatei für die Bereitstellung nach dem Veröffentlichen des Office 2016-App-v-Pakets ändern, speichern Sie die Änderungen, fügen das Office 2016-App-v-Paket hinzu und veröffentlichen es dann erneut mit der neuen Bereitstellungs Konfigurationsdatei, um die neuen Einstellungen auf Office 2016 App-v-Paketanwendungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-359">When you change the Deployment Configuration File after the Office 2016 App-V package has been published, you will save the changes, add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

><span data-ttu-id="28d1c-360">**Hinweis** Wenn Sie bestimmte Office-Anwendungen (beispielsweise Access und InfoPath) beim Erstellen des App-V-Pakets mit dem Office-Bereitstellungs Tool ausschließen möchten, verwenden Sie die Einstellung **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="28d1c-360">**Note** To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span>


**<span data-ttu-id="28d1c-361">So deaktivieren Sie eine Office 2016-Anwendung</span><span class="sxs-lookup"><span data-stu-id="28d1c-361">To disable an Office 2016 application</span></span>**

1.  <span data-ttu-id="28d1c-362">Öffnen Sie eine Konfigurationsdatei für die Bereitstellung mit einem Text-Editor wie **Editor** , und suchen Sie nach "Anwendungen".</span><span class="sxs-lookup"><span data-stu-id="28d1c-362">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="28d1c-363">Suchen Sie nach der Office-Anwendung, die Sie deaktivieren möchten, beispielsweise Access 2016.</span><span class="sxs-lookup"><span data-stu-id="28d1c-363">Search for the Office application you want to disable, for example, Access 2016.</span></span>

3.  <span data-ttu-id="28d1c-364">Ändern Sie den Wert von "Enabled" von "true" in "false".</span><span class="sxs-lookup"><span data-stu-id="28d1c-364">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="28d1c-365">Speichern Sie die Konfigurationsdatei für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="28d1c-365">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="28d1c-366">Fügen Sie das Office 2016-App-V-Paket mit der neuen Bereitstellungs Konfigurationsdatei hinzu.</span><span class="sxs-lookup"><span data-stu-id="28d1c-366">Add the Office 2016 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot}]\office16\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office16\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="28d1c-367">Fügen Sie das Office 2016-App-v-Paket erneut hinzu, und veröffentlichen Sie es erneut mit der neuen Bereitstellungs Konfigurationsdatei, um die neuen Einstellungen auf Office 2016 App-v-Paketanwendungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-367">Re-add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="28d1c-368">Deaktivieren von Office 2016-Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="28d1c-368">Disabling Office 2016 shortcuts</span></span>

<span data-ttu-id="28d1c-369">Möglicherweise möchten Sie die Tastenkombinationen für bestimmte Office-Anwendungen deaktivieren, anstatt das Paket zu veröffentlichen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-369">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="28d1c-370">Im folgenden Beispiel wird gezeigt, wie Sie Tastenkombinationen für Microsoft Access deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="28d1c-370">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="28d1c-371">So deaktivieren Sie Tastenkombinationen für Office 2016-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="28d1c-371">To disable shortcuts for Office 2016 applications</span></span>**

1.  <span data-ttu-id="28d1c-372">Öffnen Sie eine Konfigurationsdatei für die Bereitstellung in Editor, und suchen Sie nach "Tastenkombinationen".</span><span class="sxs-lookup"><span data-stu-id="28d1c-372">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="28d1c-373">Wenn Sie bestimmte Tastenkombinationen deaktivieren möchten, löschen oder kommentieren Sie die gewünschten Tastenkombinationen aus.</span><span class="sxs-lookup"><span data-stu-id="28d1c-373">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="28d1c-374">Sie müssen das Subsystem vorhanden und aktiviert lassen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-374">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="28d1c-375">Löschen Sie beispielsweise im folgenden Beispiel die Microsoft Access-Tastenkombinationen, während &lt; Sie die Tastenkombination &gt; &lt; /Shortcut intakt halten, &gt; um die Microsoft Access-Verknüpfung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="28d1c-375">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2016\Access 2016.lnk</File>
           <Target>[{AppvPackageRoot}])office16\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office16\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="28d1c-376">Speichern Sie die Konfigurationsdatei für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="28d1c-376">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="28d1c-377">Veröffentlichen Sie das Office 2016 App-V-Paket erneut mit der neuen Bereitstellungs Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="28d1c-377">Republish Office 2016 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="28d1c-378">Viele zusätzliche Einstellungen können durch Ändern der Bereitstellungskonfiguration für App-V-Pakete geändert werden, beispielsweise Dateitypen Zuordnungen, virtuelles Datei System und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="28d1c-378">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="28d1c-379">Weitere Informationen zur Verwendung von Bereitstellungskonfigurationsdateien zum Ändern von App-V-Paketeinstellungen finden Sie im Abschnitt zusätzliche Ressourcen am Ende dieses Dokuments.</span><span class="sxs-lookup"><span data-stu-id="28d1c-379">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="28d1c-380">Verwalten von Office 2016-Paket Upgrades</span><span class="sxs-lookup"><span data-stu-id="28d1c-380">Managing Office 2016 package upgrades</span></span>

<span data-ttu-id="28d1c-381">Verwenden Sie das Office-Bereitstellungs Tool, um ein Office 2016-Paket zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d1c-381">To upgrade an Office 2016 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="28d1c-382">Führen Sie die folgenden Schritte aus, um ein zuvor bereitgestelltes Office 2016-Paket zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d1c-382">To upgrade a previously deployed Office 2016 package, perform the following steps.</span></span>

**<span data-ttu-id="28d1c-383">Aktualisieren eines zuvor bereitgestellten Office 2016-Pakets</span><span class="sxs-lookup"><span data-stu-id="28d1c-383">How to upgrade a previously deployed Office 2016 package</span></span>**

1. <span data-ttu-id="28d1c-384">Erstellen Sie ein neues Office 2016-Paket über das Office-Bereitstellungs Tool, das die neueste Office 2016-Anwendungssoftware verwendet.</span><span class="sxs-lookup"><span data-stu-id="28d1c-384">Create a new Office 2016 package through the Office Deployment Tool that uses the most recent Office 2016 application software.</span></span> <span data-ttu-id="28d1c-385">Die neuesten Office 2016-Bits können immer über die Downloadphase des Erstellens eines Office 2016-App-V-Pakets abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-385">The most recent Office 2016 bits can always be obtained through the download stage of creating an Office 2016 App-V Package.</span></span> <span data-ttu-id="28d1c-386">Das neu erstellte Office 2016-Paket verfügt über die neuesten Updates und eine neue Versions-ID.</span><span class="sxs-lookup"><span data-stu-id="28d1c-386">The newly created Office 2016 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="28d1c-387">Alle Pakete, die mit dem Office-Bereitstellungs Tool erstellt wurden, haben dieselbe Linie.</span><span class="sxs-lookup"><span data-stu-id="28d1c-387">All packages created using the Office Deployment Tool have the same lineage.</span></span>

   > <span data-ttu-id="28d1c-388">**Hinweis** Office App-V-Pakete weisen zwei Versions-IDs auf:</span><span class="sxs-lookup"><span data-stu-id="28d1c-388">**Note** Office App-V packages have two Version IDs:</span></span>
   > <ul>
   > <li><span data-ttu-id="28d1c-389">Eine Office 2016-App-V-paketversions-ID, die für alle mit dem Office-Bereitstellungs Tool erstellten Pakete eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="28d1c-389">An Office 2016 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span></li>
   > <li><span data-ttu-id="28d1c-390">Eine zweite App-V-Paket-Versions-ID, x. x. x. x, beispielsweise im AppX-Manifest, das nur dann geändert wird, wenn eine neue Version von Office selbst vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="28d1c-390">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="28d1c-391">Wenn beispielsweise eine neue Office 2016-Version mit Upgrades verfügbar ist und ein Paket über das Office-Bereitstellungs Tool erstellt wird, um diese Upgrades zu integrieren, ändert sich die x. x. x. x-Version, um zu reflektieren, dass sich die Office-Version selbst geändert hat.</span><span class="sxs-lookup"><span data-stu-id="28d1c-391">For example, if a new Office 2016 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="28d1c-392">Der App-V-Server verwendet die x. x. x. x. x-Versions-ID, um dieses Paket zu unterscheiden und zu erkennen, dass es neue Upgrades für das zuvor veröffentlichte Paket enthält, und als Ergebnis es als Upgrade auf das vorhandene Office 2016-Paket veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-392">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2016 package.</span></span></li>
   > </ul>


2. <span data-ttu-id="28d1c-393">Veröffentlichen Sie die neu erstellten Office 2016-App-V-Pakete Global auf Computern, auf denen Sie die neuen Updates anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="28d1c-393">Globally publish the newly created Office 2016 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="28d1c-394">Da das neue Paket dieselbe Abstammungslinie des älteren Office 2016-App-V-Pakets aufweist, werden durch das Veröffentlichen des neuen Pakets mit den Updates nur die neuen Änderungen auf das alte Paket angewendet, und es wird schnell so sein.</span><span class="sxs-lookup"><span data-stu-id="28d1c-394">Since the new package has the same lineage of the older Office 2016 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3. <span data-ttu-id="28d1c-395">Upgrades werden auf die gleiche Weise wie alle Global veröffentlichten App-V-Pakete angewendet.</span><span class="sxs-lookup"><span data-stu-id="28d1c-395">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="28d1c-396">Da Anwendungen wahrscheinlich verwendet werden, können Upgrades verzögert werden, bis der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="28d1c-396">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>


### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="28d1c-397">Bereitstellen von Visio 2016 und Project 2016 mit Office</span><span class="sxs-lookup"><span data-stu-id="28d1c-397">Deploying Visio 2016 and Project 2016 with Office</span></span>

<span data-ttu-id="28d1c-398">In der folgenden Tabelle werden die Anforderungen und Optionen für die Bereitstellung von Visio 2016 und Project 2016 mit Office beschrieben.</span><span class="sxs-lookup"><span data-stu-id="28d1c-398">The following table describes the requirements and options for deploying Visio 2016 and Project 2016 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="28d1c-399">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="28d1c-399">Task</span></span></th>
<th align="left"><span data-ttu-id="28d1c-400">Details</span><span class="sxs-lookup"><span data-stu-id="28d1c-400">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28d1c-401">Wie kann ich Visio 2016 und Project 2016 mit Office Verpacken und veröffentlichen?</span><span class="sxs-lookup"><span data-stu-id="28d1c-401">How do I package and publish Visio 2016 and Project 2016 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="28d1c-402">Sie müssen Visio 2016 und Project 2016 in das gleiche Paket mit Office einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-402">You must include Visio 2016 and Project 2016 in the same package with Office.</span></span></p>
<p><span data-ttu-id="28d1c-403">Wenn Sie Office nicht bereitstellen, können Sie ein Paket erstellen, das Visio und/oder Project enthält, sofern Sie die in diesem Thema beschriebenen Verpackungs-, Veröffentlichungs-und Bereitstellungsanforderungen befolgen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-403">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow the packaging, publishing, and deployment requirements described in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28d1c-404">Wie kann ich Visio 2016 und Project 2016 für bestimmte Benutzer bereitstellen?</span><span class="sxs-lookup"><span data-stu-id="28d1c-404">How can I deploy Visio 2016 and Project 2016 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="28d1c-405">Verwenden Sie eine der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="28d1c-405">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="28d1c-406">Wenn Sie möchten...</span><span class="sxs-lookup"><span data-stu-id="28d1c-406">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="28d1c-407">... Verwenden Sie dann diese Methode</span><span class="sxs-lookup"><span data-stu-id="28d1c-407">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28d1c-408">Erstellen von zwei unterschiedlichen Paketen und Bereitstellen jeder Person für eine andere Gruppe von Benutzern</span><span class="sxs-lookup"><span data-stu-id="28d1c-408">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="28d1c-409">Erstellen und Bereitstellen der folgenden Pakete:</span><span class="sxs-lookup"><span data-stu-id="28d1c-409">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="28d1c-410">Ein Paket, das nur Office-deploy auf Computern enthält, deren Benutzer nur Office benötigen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-410">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="28d1c-411">Ein Paket mit Office, Visio und Project – deploy auf Computern, deren Benutzer alle drei Anwendungen benötigen.</span><span class="sxs-lookup"><span data-stu-id="28d1c-411">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28d1c-412">Wenn Sie nur ein Paket für die gesamte Organisation verwenden möchten oder wenn Sie über Benutzer verfügen, die Computer freigeben:</span><span class="sxs-lookup"><span data-stu-id="28d1c-412">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="28d1c-413">Führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="28d1c-413">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="28d1c-414">Erstellen Sie ein Paket, das Office, Visio und Project enthält.</span><span class="sxs-lookup"><span data-stu-id="28d1c-414">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="28d1c-415">Bereitstellen des Pakets für alle Benutzer</span><span class="sxs-lookup"><span data-stu-id="28d1c-415">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="28d1c-416">Verwenden Sie <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> , um zu verhindern, dass bestimmte Benutzer Visio und Project verwenden.</span><span class="sxs-lookup"><span data-stu-id="28d1c-416">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="28d1c-417">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="28d1c-417">Additional resources</span></span>


[<span data-ttu-id="28d1c-418">Bereitstellen von Microsoft Office2013 mit App-V</span><span class="sxs-lookup"><span data-stu-id="28d1c-418">Deploying Microsoft Office 2013 by Using App-V</span></span>](deploying-microsoft-office-2013-by-using-app-v.md)

[<span data-ttu-id="28d1c-419">Bereitstellen von Microsoft Office2010 mit App-V</span><span class="sxs-lookup"><span data-stu-id="28d1c-419">Deploying Microsoft Office 2010 by Using App-V</span></span>](deploying-microsoft-office-2010-by-using-app-v.md)

[<span data-ttu-id="28d1c-420">Office 2016-Bereitstellungs Tool für Klick-und-Los</span><span class="sxs-lookup"><span data-stu-id="28d1c-420">Office 2016 Deployment Tool for Click-to-Run</span></span>](https://www.microsoft.com/download/details.aspx?id=49117)

**<span data-ttu-id="28d1c-421">Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="28d1c-421">Connection Groups</span></span>**

[<span data-ttu-id="28d1c-422">Bereitstellen von Verbindungsgruppen in Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="28d1c-422">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="28d1c-423">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="28d1c-423">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="28d1c-424">Dynamische Konfiguration</span><span class="sxs-lookup"><span data-stu-id="28d1c-424">Dynamic Configuration</span></span>**

[<span data-ttu-id="28d1c-425">Informationen zur dynamischen Konfiguration in App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="28d1c-425">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)





