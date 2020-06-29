---
title: Befehlszeilenoptionen für MED-V-Installationsdateien
description: Befehlszeilenoptionen für MED-V-Installationsdateien
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811773"
---
# <span data-ttu-id="dcd81-103">Befehlszeilenoptionen für MED-V-Installationsdateien</span><span class="sxs-lookup"><span data-stu-id="dcd81-103">Command-Line Options for MED-V Installation Files</span></span>


<span data-ttu-id="dcd81-104">Wenn Sie Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 installieren oder deinstallieren, haben Sie die Möglichkeit, die Installationsdateien an der Eingabeaufforderung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dcd81-104">When you install or uninstall Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="dcd81-105">In diesem Abschnitt werden verschiedene Optionen beschrieben, die Sie bei der Installation oder Deinstallation von MED-V an der Eingabeaufforderung angeben können.</span><span class="sxs-lookup"><span data-stu-id="dcd81-105">This section describes different options that you can specify when you install or uninstall MED-V at the command prompt.</span></span>

### <span data-ttu-id="dcd81-106">Befehlszeilenargumente</span><span class="sxs-lookup"><span data-stu-id="dcd81-106">Command-Line Arguments</span></span>

<span data-ttu-id="dcd81-107">Sie können die folgenden Befehlszeilenargumente zusammen mit den jeweiligen MED-V-Installationsdateien verwenden.</span><span class="sxs-lookup"><span data-stu-id="dcd81-107">You can use the following command-line arguments together with their respective MED-V installation files.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dcd81-108">Installationsdatei</span><span class="sxs-lookup"><span data-stu-id="dcd81-108">Installation File</span></span></th>
<th align="left"><span data-ttu-id="dcd81-109">Argument</span><span class="sxs-lookup"><span data-stu-id="dcd81-109">Argument</span></span></th>
<th align="left"><span data-ttu-id="dcd81-110">Akzeptierte Werte</span><span class="sxs-lookup"><span data-stu-id="dcd81-110">Accepted Values</span></span></th>
<th align="left"><span data-ttu-id="dcd81-111">Typ</span><span class="sxs-lookup"><span data-stu-id="dcd81-111">Type</span></span></th>
<th align="left"><span data-ttu-id="dcd81-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dcd81-112">Description</span></span></th>
<th align="left"><span data-ttu-id="dcd81-113">Standard</span><span class="sxs-lookup"><span data-stu-id="dcd81-113">Default</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dcd81-114">Host-Agent</span><span class="sxs-lookup"><span data-stu-id="dcd81-114">Host Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-115">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="dcd81-115">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-116">&lt;Installationspfad&gt;</span><span class="sxs-lookup"><span data-stu-id="dcd81-116">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-117">Installation</span><span class="sxs-lookup"><span data-stu-id="dcd81-117">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-118">Installiertes Verzeichnis ändern</span><span class="sxs-lookup"><span data-stu-id="dcd81-118">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-119">Die Installation wechselt zu Programme\Microsoft Enterprise Desktop Virtualization.</span><span class="sxs-lookup"><span data-stu-id="dcd81-119">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dcd81-120">MED-V-Arbeitsbereichs Paket</span><span class="sxs-lookup"><span data-stu-id="dcd81-120">MED-V Workspace Packager</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-121">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="dcd81-121">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-122">&lt;Installationspfad&gt;</span><span class="sxs-lookup"><span data-stu-id="dcd81-122">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-123">Installation</span><span class="sxs-lookup"><span data-stu-id="dcd81-123">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-124">Installiertes Verzeichnis ändern</span><span class="sxs-lookup"><span data-stu-id="dcd81-124">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-125">Die Installation wechselt zu Programme\Microsoft Enterprise Desktop Virtualization.</span><span class="sxs-lookup"><span data-stu-id="dcd81-125">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dcd81-126">MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="dcd81-126">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-127">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="dcd81-127">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-128">&lt;Installationspfad&gt;</span><span class="sxs-lookup"><span data-stu-id="dcd81-128">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-129">Installation</span><span class="sxs-lookup"><span data-stu-id="dcd81-129">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-130">Installiertes Verzeichnis ändern</span><span class="sxs-lookup"><span data-stu-id="dcd81-130">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-131">Die Installation geht zu ProgramData\Microsoft\Medv\Workspace.</span><span class="sxs-lookup"><span data-stu-id="dcd81-131">Installation goes to ProgramData\Microsoft\Medv\Workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dcd81-132">MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="dcd81-132">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-133">VHD überschreiben</span><span class="sxs-lookup"><span data-stu-id="dcd81-133">OVERWRITE VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-134">0 oder 1</span><span class="sxs-lookup"><span data-stu-id="dcd81-134">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-135">Installation</span><span class="sxs-lookup"><span data-stu-id="dcd81-135">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-136">Fehler bei der Installation, wenn VHD vorhanden ist (0) oder vorhandene VHD überschrieben wird (1).</span><span class="sxs-lookup"><span data-stu-id="dcd81-136">Fail installation if VHD exists(0) or overwrite existing VHD(1).</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-137">Overwrite tritt nicht auf, und die Installation schlägt fehl, wenn bereits eine virtuelle Festplatte (VHD) vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dcd81-137">Overwrite does not occur and installation fails if a virtual hard disk (VHD) already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dcd81-138">MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="dcd81-138">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-139">SUPPRESSMEDVLAUNCH</span><span class="sxs-lookup"><span data-stu-id="dcd81-139">SUPPRESSMEDVLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-140">0 oder 1</span><span class="sxs-lookup"><span data-stu-id="dcd81-140">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-141">Installation</span><span class="sxs-lookup"><span data-stu-id="dcd81-141">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-142">Starten Sie (0) oder starten Sie (1) med-v nach der Installation von Med-v Workspace nicht.</span><span class="sxs-lookup"><span data-stu-id="dcd81-142">Start(0) or do not start(1) MED-V after MED-V workspace is installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-143">Wenn der Med-v-Arbeitsbereich mit der Benutzeroberfläche (UI) installiert wurde, steuert ein Kontrollkästchen auf der <strong> Seite fertig stellen, </strong> ob Med-v gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dcd81-143">If the MED-V workspace was installed with the user interface (UI), a check box on the <strong>Finish</strong> page controls whether to start MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dcd81-144">MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="dcd81-144">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-145">DELETEDIFFDISKS</span><span class="sxs-lookup"><span data-stu-id="dcd81-145">DELETEDIFFDISKS</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-146">0 oder 1</span><span class="sxs-lookup"><span data-stu-id="dcd81-146">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-147">Deinstallation</span><span class="sxs-lookup"><span data-stu-id="dcd81-147">Uninstallation</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-148">Von MED-V erstellte virtuelle Festplatten beibehalten (0) oder löschen (1)</span><span class="sxs-lookup"><span data-stu-id="dcd81-148">Keep(0) or delete(1) VHDs created by MED-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="dcd81-149">Keine virtuellen Festplatten werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dcd81-149">No VHDs are deleted.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="dcd81-150">Beispiele für Befehlszeilenargumente</span><span class="sxs-lookup"><span data-stu-id="dcd81-150">Examples of Command-Line Arguments</span></span>

<span data-ttu-id="dcd81-151">Im folgenden Beispiel wird der vom Med-v Workspace-Paketer erstellte Med-v-Arbeitsbereich installiert.</span><span class="sxs-lookup"><span data-stu-id="dcd81-151">The following example installs the MED-V workspace created by the MED-V workspace Packager.</span></span> <span data-ttu-id="dcd81-152">Die Installationsdatei erstellt eine Protokolldatei im temporären Verzeichnis und führt die Installationsdatei im stillen Modus aus, startet aber den MED-V-Host-Agent nicht nach Abschluss.</span><span class="sxs-lookup"><span data-stu-id="dcd81-152">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode, but does not start the MED-V Host Agent on completion.</span></span> <span data-ttu-id="dcd81-153">Die Installationsdatei überschreibt alle VHD-Dateien, die von einer vorherigen Installation mit demselben Namen zurückgelassen wurden.</span><span class="sxs-lookup"><span data-stu-id="dcd81-153">The installation file overwrites any VHD left behind by a previous installation that has the same name.</span></span>

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

<span data-ttu-id="dcd81-154">Im folgenden Beispiel wird der zuvor installierte MED-V-Arbeitsbereich deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="dcd81-154">The following example uninstalls the MED-V workspace that was previously installed.</span></span> <span data-ttu-id="dcd81-155">Die Installationsdatei erstellt eine Protokolldatei im temporären Verzeichnis und führt die Installationsdatei im stillen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="dcd81-155">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode.</span></span> <span data-ttu-id="dcd81-156">Die Installationsdatei löscht alle verbleibenden virtuellen Festplattendateien aus dem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="dcd81-156">The installation file deletes any remaining virtual hard disk files from the file system.</span></span>

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## <span data-ttu-id="dcd81-157">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dcd81-157">Related topics</span></span>


[<span data-ttu-id="dcd81-158">Bereitstellen der MED-V-Komponenten</span><span class="sxs-lookup"><span data-stu-id="dcd81-158">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

[<span data-ttu-id="dcd81-159">Technische Referenz für MED-V</span><span class="sxs-lookup"><span data-stu-id="dcd81-159">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





