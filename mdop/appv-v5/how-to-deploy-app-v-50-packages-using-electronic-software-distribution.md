---
title: Bereitstellen von App-V 5.0-Paketen mithilfe einer ESD-Lösung (Electronic Software Distribution)
description: Bereitstellen von App-V 5.0-Paketen mithilfe einer ESD-Lösung (Electronic Software Distribution)
author: dansimp
ms.assetid: 08e5e05b-dbb8-4be7-b2d8-721ef627da81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 33af02c5e9fad7408f9719ecd1a7fa90eacfeb29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805540"
---
# <span data-ttu-id="595c9-103">Bereitstellen von App-V 5.0-Paketen mithilfe einer ESD-Lösung (Electronic Software Distribution)</span><span class="sxs-lookup"><span data-stu-id="595c9-103">How to deploy App-V 5.0 Packages Using Electronic Software Distribution</span></span>


<span data-ttu-id="595c9-104">Sie können ein ESD-System (Electronic Software Distribution) verwenden, um App-v 5,0-virtuelle Anwendungen für App-v-Clients bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="595c9-104">You can use an electronic software distribution (ESD) system to deploy App-V 5.0 virtual applications to App-V clients.</span></span> <span data-ttu-id="595c9-105">Einzelheiten finden Sie in der Dokumentation, die mit dem von Ihnen verwendeten ESD-Dokument zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="595c9-105">For details, see the documentation available with the ESD you are using.</span></span>

<span data-ttu-id="595c9-106">Komponentenanforderungen und Optionen für die Verwendung eines ESD zur Bereitstellung von App-v-Paketen finden Sie unter [Planen der Bereitstellung von App-v 5,0 mit einem elektronischen Software Verteilungs System](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="595c9-106">For component requirements and options for using an ESD to deploy App-V packages, see [Planning to Deploy App-V 5.0 with an Electronic Software Distribution System](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md).</span></span>

<span data-ttu-id="595c9-107">Verwenden Sie eine der folgenden Methoden, um Pakete auf App-V-Clientcomputern mit einem ESD-Code zu veröffentlichen:</span><span class="sxs-lookup"><span data-stu-id="595c9-107">Use one of the following methods to publish packages to App-V client computers with an ESD:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="595c9-108">Methode</span><span class="sxs-lookup"><span data-stu-id="595c9-108">Method</span></span></th>
<th align="left"><span data-ttu-id="595c9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="595c9-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="595c9-110">Funktionen, die von einem Drittanbieter-ESD bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="595c9-110">Functionality provided by a third-party ESD</span></span></p></td>
<td align="left"><p><span data-ttu-id="595c9-111">Verwenden Sie die Funktionalität in einem Drittanbieter-ESD.</span><span class="sxs-lookup"><span data-stu-id="595c9-111">Use the functionality in a third-party ESD.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="595c9-112">Eigenständiges Windows Installer</span><span class="sxs-lookup"><span data-stu-id="595c9-112">Stand-alone Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="595c9-113">Installieren Sie die Anwendung auf dem Zielclientcomputer mithilfe der zugehörigen Windows Installer-Datei (MSI), die bei der ersten Sequenzierung einer Anwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="595c9-113">Install the application on the target client computer by using the associated Windows Installer (.msi) file that is created when you initially sequence an application.</span></span> <span data-ttu-id="595c9-114">Die Windows Installer-Datei enthält die zugehörigen App-V 5,0-Paketdatei Informationen, die zum Konfigurieren eines Pakets verwendet werden, und kopiert die erforderlichen Paketdateien auf den Client.</span><span class="sxs-lookup"><span data-stu-id="595c9-114">The Windows Installer file contains the associated App-V 5.0 package file information used to configure a package and copies the required package files to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="595c9-115">PowerShell</span><span class="sxs-lookup"><span data-stu-id="595c9-115">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="595c9-116">Verwenden Sie PowerShell-Cmdlets zum Bereitstellen virtualisierter Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="595c9-116">Use PowerShell cmdlets to deploy virtualized applications.</span></span> <span data-ttu-id="595c9-117">Weitere Informationen zur Verwendung von PowerShell und App-v 5,0 finden Sie unter <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)"> Verwalten von App-v mithilfe von PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="595c9-117">For more information about using PowerShell and App-V 5.0, see <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)">Administering App-V by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="595c9-118">So stellen Sie App-V 5,0-Pakete mithilfe eines ESD bereit</span><span class="sxs-lookup"><span data-stu-id="595c9-118">To deploy App-V 5.0 packages by using an ESD</span></span>**

1.  <span data-ttu-id="595c9-119">Installieren Sie den App-V 5,0-Sequenzer auf einem Computer in Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="595c9-119">Install the App-V 5.0 Sequencer on a computer in your environment.</span></span> <span data-ttu-id="595c9-120">Weitere Informationen zum Installieren des Sequencers finden Sie unter [so wird es gemacht: Installieren des Sequencers](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="595c9-120">For more information about installing the sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="595c9-121">Verwenden Sie den App-V 5,0-Sequenzer zum Erstellen einer virtuellen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="595c9-121">Use the App-V 5.0 Sequencer to create virtual application.</span></span> <span data-ttu-id="595c9-122">Informationen zum Erstellen einer virtuellen Anwendung finden Sie unter [Erstellen und Verwalten von virtualisierten Anwendungen in App-V 5,0](creating-and-managing-app-v-50-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="595c9-122">For information about creating a virtual application, see [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

3.  <span data-ttu-id="595c9-123">Nachdem Sie die virtuelle Anwendung erstellt haben, müssen Sie das Paket mithilfe ihrer ESD-Lösung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="595c9-123">After you create the virtual application, deploy the package by using your ESD solution.</span></span>

    <span data-ttu-id="595c9-124">Wenn Sie den System Center Configuration Manager verwenden, überprüfen Sie zunächst [die Einführung in die Anwendungsverwaltung in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) , um Informationen zur Verwendung von App-V 5,0 und dem System Center2012-Konfigurations-Manager zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="595c9-124">If you are using System Center Configuration Manager, start by reviewing [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) for information about using App-V 5.0 and System Center2012 Configuration Manager.</span></span>

    <span data-ttu-id="595c9-125">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="595c9-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="595c9-126">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="595c9-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="595c9-127">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="595c9-127">Got an App-V issue?</span></span>** <span data-ttu-id="595c9-128">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="595c9-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="595c9-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="595c9-129">Related topics</span></span>


[<span data-ttu-id="595c9-130">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="595c9-130">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





