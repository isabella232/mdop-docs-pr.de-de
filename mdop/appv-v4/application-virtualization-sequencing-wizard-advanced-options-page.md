---
title: Seite ' Erweiterte Optionen ' für Application Virtualization Sequencer-Assistent
description: Seite ' Erweiterte Optionen ' für Application Virtualization Sequencer-Assistent
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807971"
---
# <span data-ttu-id="ab91f-103">Seite ' Erweiterte Optionen ' für Application Virtualization Sequencer-Assistent</span><span class="sxs-lookup"><span data-stu-id="ab91f-103">Application Virtualization Sequencing Wizard Advanced Options Page</span></span>


<span data-ttu-id="ab91f-104">Verwenden Sie die Seite **Erweiterte Optionen** des Sequence-Assistenten für Application Virtualization (App-V), um erweiterte Optionen für die Installation der Anwendung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ab91f-104">Use the **Advanced Options** page of the Application Virtualization (App-V) Sequencing Wizard to specify advanced options for the application to be installed.</span></span> <span data-ttu-id="ab91f-105">Die Seite enthält die in der folgenden Tabelle beschriebenen Elemente.</span><span class="sxs-lookup"><span data-stu-id="ab91f-105">The page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab91f-106">Name</span><span class="sxs-lookup"><span data-stu-id="ab91f-106">Name</span></span></th>
<th align="left"><span data-ttu-id="ab91f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab91f-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab91f-108">Block Größe</span><span class="sxs-lookup"><span data-stu-id="ab91f-108">Block Size</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-109">Hiermit können Sie die Größe von Blöcken angeben, in die die SFT-Datei aufgeteilt wird, wenn Sie über ein Netzwerk gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="ab91f-109">Use to specify the size of blocks that the SFT file will be divided into when streamed across a network.</span></span> <span data-ttu-id="ab91f-110">Alle Blöcke entsprechen der angegebenen Größe; Allerdings kann der letzte Block kleiner als angegeben sein.</span><span class="sxs-lookup"><span data-stu-id="ab91f-110">All blocks equal the specified size; however, the last block might be smaller than specified.</span></span> <span data-ttu-id="ab91f-111">Wählen Sie einen der folgenden Werte aus:</span><span class="sxs-lookup"><span data-stu-id="ab91f-111">Select one of the following values:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="ab91f-112">4 KB</span><span class="sxs-lookup"><span data-stu-id="ab91f-112">4 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="ab91f-113">16 KB</span><span class="sxs-lookup"><span data-stu-id="ab91f-113">16 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="ab91f-114">32 KB</span><span class="sxs-lookup"><span data-stu-id="ab91f-114">32 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="ab91f-115">64 KB</span><span class="sxs-lookup"><span data-stu-id="ab91f-115">64 KB</span></span></strong></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="ab91f-116">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ab91f-116">Note</span></span></strong><br/><p><span data-ttu-id="ab91f-117">Wenn Sie eine Blockgröße auswählen, sollten Sie die Größe der SFT-Datei und die Netzwerkbandbreite in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="ab91f-117">When you select a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="ab91f-118">Eine Datei mit einer kleineren Blockgröße dauert länger, um über das Netzwerk zu streamen, ist jedoch weniger bandbreitenintensiv.</span><span class="sxs-lookup"><span data-stu-id="ab91f-118">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="ab91f-119">Dateien mit größeren Blockgrößen können schneller gestreamt werden, verwenden aber mehr Netzwerkbandbreite.</span><span class="sxs-lookup"><span data-stu-id="ab91f-119">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="ab91f-120">Durch experimentieren können Sie die optimale Blockgröße für Streaming-Anwendungen in Ihrem Netzwerk ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ab91f-120">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab91f-121">Aktivieren von Microsoft Update während der Überwachung</span><span class="sxs-lookup"><span data-stu-id="ab91f-121">Enable Microsoft Update During Monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-122">Aktiviert die Installation von Microsoft Updates während des Sequenz-Assistenten&#39;s-Überwachungsphase.</span><span class="sxs-lookup"><span data-stu-id="ab91f-122">Enables installation of Microsoft Updates during the Sequencing Wizard&#39;s monitoring phase.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab91f-123">REBASE-DLLs</span><span class="sxs-lookup"><span data-stu-id="ab91f-123">Rebase DLLs</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-124">Ermöglicht die Neuzuordnung unterstützter Dynamic-Link-Bibliotheken zu einem zusammenhängenden Speicherplatz im Arbeitsspeicher, wodurch der Arbeitsspeicher gespart und die Leistung verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="ab91f-124">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM, saving memory and improving performance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab91f-125">Zurück</span><span class="sxs-lookup"><span data-stu-id="ab91f-125">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-126">Greift auf den Sequenz-Assistenten&#39;s vorherige Seite zu.</span><span class="sxs-lookup"><span data-stu-id="ab91f-126">Accesses the Sequencing Wizard&#39;s previous page.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab91f-127">Nächste</span><span class="sxs-lookup"><span data-stu-id="ab91f-127">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-128">Greift auf den Sequenz-Assistenten zu&#39;nächste Seite.</span><span class="sxs-lookup"><span data-stu-id="ab91f-128">Accesses the Sequencing Wizard&#39;s next page.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab91f-129">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="ab91f-129">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-130">Beendet den Vorgang des Sequenz-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="ab91f-130">Terminates operation of the Sequencing Wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="ab91f-131">\ [Vorlage-Tokenwert \]</span><span class="sxs-lookup"><span data-stu-id="ab91f-131">\[Template Token Value\]</span></span>

<span data-ttu-id="ab91f-132">Verwenden Sie die Seite " **Erweiterte Optionen** " des App-V-Sequenz-Assistenten, um erweiterte Optionen für die Anwendung anzugeben, die Sie sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="ab91f-132">Use the **Advanced Options** page of the App-V Sequencing Wizard to specify advanced options for the application you are sequencing.</span></span> <span data-ttu-id="ab91f-133">Diese Seite enthält die in der folgenden Tabelle beschriebenen Elemente.</span><span class="sxs-lookup"><span data-stu-id="ab91f-133">This page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab91f-134">Name</span><span class="sxs-lookup"><span data-stu-id="ab91f-134">Name</span></span></th>
<th align="left"><span data-ttu-id="ab91f-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab91f-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab91f-136">Microsoft Update während der Überwachung ausführen lassen</span><span class="sxs-lookup"><span data-stu-id="ab91f-136">Allow Microsoft Update to run during monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-137">Gibt an, ob Softwareupdates während der Überwachungsphase der Anwendungs Sequenz auf die Anwendung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab91f-137">Specifies whether software updates will be applied to the application during the monitoring phase of application sequencing.</span></span> <span data-ttu-id="ab91f-138">Diese Option ist hilfreich, wenn Updates erforderlich sind, um die Anwendungsinstallation erfolgreich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ab91f-138">This option is helpful if updates are required to successfully complete the application installation.</span></span> <span data-ttu-id="ab91f-139">Diese Option ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab91f-139">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab91f-140">REBASE-DLLs</span><span class="sxs-lookup"><span data-stu-id="ab91f-140">Rebase Dlls</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-141">Ermöglicht die Neuzuordnung unterstützter Dynamic-Link-Bibliotheken zu einem zusammenhängenden Speicherplatz im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ab91f-141">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM.</span></span> <span data-ttu-id="ab91f-142">Wenn Sie diese Option auswählen, können Sie den Arbeitsspeicher verwalten und die Anwendungsleistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="ab91f-142">Selecting this option can help manage memory and improve application performance.</span></span> <span data-ttu-id="ab91f-143">Diese Option ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab91f-143">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab91f-144">Zurück</span><span class="sxs-lookup"><span data-stu-id="ab91f-144">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-145">Wechselt zur vorherigen Seite des Assistenten.</span><span class="sxs-lookup"><span data-stu-id="ab91f-145">Goes to the previous page of the wizard.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab91f-146">Nächste</span><span class="sxs-lookup"><span data-stu-id="ab91f-146">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-147">Wechselt zur nächsten Seite des Assistenten.</span><span class="sxs-lookup"><span data-stu-id="ab91f-147">Goes to the next page of the wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab91f-148">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="ab91f-148">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab91f-149">Verwirft die Einstellungen und beendet den Assistenten.</span><span class="sxs-lookup"><span data-stu-id="ab91f-149">Discards the settings and exits the wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="ab91f-150">\ [Vorlage-Tokenwert \]</span><span class="sxs-lookup"><span data-stu-id="ab91f-150">\[Template Token Value\]</span></span>

## <span data-ttu-id="ab91f-151">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ab91f-151">Related topics</span></span>


[<span data-ttu-id="ab91f-152">Sequenz-Assistent</span><span class="sxs-lookup"><span data-stu-id="ab91f-152">Sequencing Wizard</span></span>](sequencing-wizard.md)









