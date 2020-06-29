---
title: Bestimmen der Veröffentlichungsmethode
description: Bestimmen der Veröffentlichungsmethode
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808899"
---
# <span data-ttu-id="513b8-103">Bestimmen der Veröffentlichungsmethode</span><span class="sxs-lookup"><span data-stu-id="513b8-103">Determine Your Publishing Method</span></span>


<span data-ttu-id="513b8-104">Nachdem Sie eine Anwendung mithilfe von Application Virtualization Sequencer sequenziert haben, müssen Sie diese Anwendung für Ihre Benutzer *veröffentlichen* .</span><span class="sxs-lookup"><span data-stu-id="513b8-104">After you sequence an application by using the Application Virtualization Sequencer, you need to *publish* that application to your users.</span></span> <span data-ttu-id="513b8-105">Die Veröffentlichung der Anwendung besteht darin, die Symbole, Paketdefinitionsinformationen und den Speicherort der Inhaltsquelle auf jedem Computer bereitzustellen, auf dem der Application Virtualization-Client installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="513b8-105">Publishing the application consists of delivering the icons, package definition information, and content source location to each computer where the Application Virtualization Client has been installed.</span></span> <span data-ttu-id="513b8-106">In der folgenden Tabelle werden die Veröffentlichungsmethoden beschrieben, die bei der Bereitstellung von Application Virtualization mithilfe eines ESD-Systems (Electronic Software Distribution) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="513b8-106">The following table describes publishing methods that are supported when you deploy Application Virtualization by using an electronic software distribution (ESD) system.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="513b8-107">Methode</span><span class="sxs-lookup"><span data-stu-id="513b8-107">Method</span></span></th>
<th align="left"><span data-ttu-id="513b8-108">Vorteile</span><span class="sxs-lookup"><span data-stu-id="513b8-108">Advantages</span></span></th>
<th align="left"><span data-ttu-id="513b8-109">Nachteile</span><span class="sxs-lookup"><span data-stu-id="513b8-109">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="513b8-110">Generieren Sie eine Windows Installer-Datei während der Sequenzierung als eigenständige Lösung.</span><span class="sxs-lookup"><span data-stu-id="513b8-110">Generate a Windows Installer file during sequencing, as a stand-alone solution.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="513b8-111">Sehr einfach zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="513b8-111">Very simple to use.</span></span></p></li>
<li><p><span data-ttu-id="513b8-112">Das Paket wurde lokal auf jedem Computer in den Cache geladen.</span><span class="sxs-lookup"><span data-stu-id="513b8-112">Package loaded into cache locally on each computer.</span></span></p></li>
<li><p><span data-ttu-id="513b8-113">Symbole, die dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="513b8-113">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="513b8-114">Ähnlich wie herkömmliche Softwarebereitstellung.</span><span class="sxs-lookup"><span data-stu-id="513b8-114">Similar to traditional software deployment.</span></span></p></li>
<li><p><span data-ttu-id="513b8-115">Keine Notwendigkeit für Streaming-Server.</span><span class="sxs-lookup"><span data-stu-id="513b8-115">No need for streaming servers.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="513b8-116">Keine Flexibilität beim Speicherort von Paketinhalten auf Computern – derselbe Standort auf allen Computern.</span><span class="sxs-lookup"><span data-stu-id="513b8-116">No flexibility in location of package contents on computers—same location on all computers.</span></span></p></li>
<li><p><span data-ttu-id="513b8-117">Sie müssen nur Programme hinzufügen/entfernen oder msiexec verwenden, um Anwendungen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="513b8-117">Must use only Add/Remove Programs or msiexec to remove applications.</span></span></p></li>
<li><p><span data-ttu-id="513b8-118">Entfernen und ersetzen durch neue Version, die für die Paketaktualisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="513b8-118">Removal and replacement with new version required for package updating.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="513b8-119">Generieren Sie während der Sequenzierung eine Windows Installer-Datei, die mit den Befehlszeileneigenschaften Mode, Load und OVERRIDEURL und dem Paketmanifest verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="513b8-119">Generate a Windows Installer file during sequencing, used with MODE, LOAD, and OVERRIDEURL command-line properties and the package manifest.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="513b8-120">Einfach zu verwenden, aber mit zusätzlicher Flexibilität.</span><span class="sxs-lookup"><span data-stu-id="513b8-120">Simple to use but with added flexibility.</span></span></p></li>
<li><p><span data-ttu-id="513b8-121">Symbole, die dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="513b8-121">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="513b8-122">SFT-Datei, die die Anwendungen enthält, kann an einem Streaming-Quellspeicherort abgelegt werden, wobei die Clients für die Verwendung dieses Speicherorts konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="513b8-122">SFT file containing the applications can be placed on a streaming source location, with clients configured to use that location.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="513b8-123">Begrenzte Flexibilität – nur der Speicherort des Paketinhalts kann zur Laufzeit gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="513b8-123">Limited flexibility—only the location of the package content can be controlled at run time.</span></span></p></li>
<li><p><span data-ttu-id="513b8-124">Sie müssen nur Programme hinzufügen/entfernen oder msiexec verwenden, um die Anwendung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="513b8-124">Must use only Add/Remove Programs or msiexec to remove the application.</span></span></p></li>
<li><p><span data-ttu-id="513b8-125">Entfernen und ersetzen mit der neuen Version, die für die Paketaktualisierung erforderlich ist, es sei denn, Sie verwenden Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="513b8-125">Removal and replacement with new version required for package updating, unless using streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="513b8-126">Führen Sie SFTMIME-Befehle aus.</span><span class="sxs-lookup"><span data-stu-id="513b8-126">Run SFTMIME commands.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="513b8-127">Vollständige Flexibilität – vollständige Kontrolle über alle Paketverwaltungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="513b8-127">Complete flexibility—full control of all package management functions.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="513b8-128">Befehle müssen für die Verwendung mit dem ESD-System skriptiert werden.</span><span class="sxs-lookup"><span data-stu-id="513b8-128">Commands must be scripted for use with the ESD system.</span></span></p></li>
<li><p><span data-ttu-id="513b8-129">Befehle müssen auf jedem Computer in der richtigen Reihenfolge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="513b8-129">Commands must be run on each computer in correct sequence.</span></span></p></li>
<li><p><span data-ttu-id="513b8-130">Detailliertes Verständnis der Befehlssprache und sorgfältige Planung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="513b8-130">Detailed understanding of command language and careful planning required.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="513b8-131">Weitere Informationen zum Verwenden dieser Veröffentlichungsmethoden finden Sie unter [Veröffentlichen einer virtuellen Anwendung auf dem Client](how-to-publish-a-virtual-application-on-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="513b8-131">For more information about using these publishing methods, see [How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md).</span></span>

## <span data-ttu-id="513b8-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="513b8-132">Related topics</span></span>


[<span data-ttu-id="513b8-133">Bestimmen der Streaming-Methode</span><span class="sxs-lookup"><span data-stu-id="513b8-133">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="513b8-134">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="513b8-134">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="513b8-135">Übersicht über Electronic Software Distribution-basierte Szenarien</span><span class="sxs-lookup"><span data-stu-id="513b8-135">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="513b8-136">So veröffentlichen Sie eine virtuelle Anwendung auf dem Client</span><span class="sxs-lookup"><span data-stu-id="513b8-136">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="513b8-137">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="513b8-137">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





