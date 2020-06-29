---
title: WMI-Klasse für APP-V-Pakete
description: WMI-Klasse für APP-V-Pakete
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808051"
---
# <span data-ttu-id="c6b6b-103">WMI-Klasse für APP-V-Pakete</span><span class="sxs-lookup"><span data-stu-id="c6b6b-103">App-V Package WMI Class</span></span>


<span data-ttu-id="c6b6b-104">Im Application Virtualization-Client (App-V) ist die **Package** -Klasse eine WMI-Klasse (Windows Management Instrumentation), die alle virtuellen Pakete auf dem Client darstellt.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-104">In the Application Virtualization (App-V) Client, the **Package** class is a Windows Management Instrumentation (WMI) class that represents all the virtual packages on the client.</span></span> <span data-ttu-id="c6b6b-105">Die virtuellen Pakete können viele virtuelle Anwendungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-105">The virtual packages can contain many virtual applications.</span></span>

## <span data-ttu-id="c6b6b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6b6b-106">Syntax</span></span>


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## <span data-ttu-id="c6b6b-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6b6b-107">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="c6b6b-108">Name</span><span class="sxs-lookup"><span data-stu-id="c6b6b-108">Name</span></span>**  
<span data-ttu-id="c6b6b-109">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-109">Data type: **String**</span></span>

<span data-ttu-id="c6b6b-110">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-110">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-111">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-111">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-112">Der benutzerfreundliche Name des virtuellen Pakets.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-112">The user-friendly name of the virtual package.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="c6b6b-113">Version</span><span class="sxs-lookup"><span data-stu-id="c6b6b-113">Version</span></span>**  
<span data-ttu-id="c6b6b-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-114">Data type: **String**</span></span>

<span data-ttu-id="c6b6b-115">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-115">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-116">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-116">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-117">Die Version des virtuellen Pakets.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-117">The version of the virtual package.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="c6b6b-118">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="c6b6b-118">PackageGUID</span></span>**  
<span data-ttu-id="c6b6b-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-119">Data type: **String**</span></span>

<span data-ttu-id="c6b6b-120">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-120">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-121">Qualifizierer: Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c6b6b-121">Qualifiers: Key</span></span>

<span data-ttu-id="c6b6b-122">Der GUID-Bezeichner der Paketkonfiguration und der Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-122">The GUID identifier of the package configuration and source files.</span></span>

<a href="" id="sftpath"></a>**<span data-ttu-id="c6b6b-123">SftPath</span><span class="sxs-lookup"><span data-stu-id="c6b6b-123">SftPath</span></span>**  
<span data-ttu-id="c6b6b-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-124">Data type: **String**</span></span>

<span data-ttu-id="c6b6b-125">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-125">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-126">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-126">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-127">Der Dateipfad der SFT-Datei.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-127">The file path of the SFT file.</span></span>

<a href="" id="totalsize"></a>**<span data-ttu-id="c6b6b-128">TotalSize</span><span class="sxs-lookup"><span data-stu-id="c6b6b-128">TotalSize</span></span>**  
<span data-ttu-id="c6b6b-129">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-129">Data type: **UInt64**</span></span>

<span data-ttu-id="c6b6b-130">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-130">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-131">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-131">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-132">Die Gesamtgröße des virtuellen Pakets in Kilobytes.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-132">The total size of the virtual package, in kilobytes.</span></span>

<a href="" id="cachedsize"></a>**<span data-ttu-id="c6b6b-133">CachedSize</span><span class="sxs-lookup"><span data-stu-id="c6b6b-133">CachedSize</span></span>**  
<span data-ttu-id="c6b6b-134">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-134">Data type: **UInt64**</span></span>

<span data-ttu-id="c6b6b-135">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-135">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-136">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-136">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-137">Die Gesamtgröße des Caches für das virtuelle Paket in Kilobytes.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-137">The total size of the cache for the virtual package, in kilobytes.</span></span>

<a href="" id="launchsize"></a>**<span data-ttu-id="c6b6b-138">LaunchSize</span><span class="sxs-lookup"><span data-stu-id="c6b6b-138">LaunchSize</span></span>**  
<span data-ttu-id="c6b6b-139">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-139">Data type: **UInt64**</span></span>

<span data-ttu-id="c6b6b-140">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-140">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-141">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-141">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-142">Die Gesamtgröße des primären Funktionsblocks des virtuellen Pakets in Kilobytes.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-142">The total size of the virtual package’s primary feature block, in kilobytes.</span></span>

<a href="" id="cachedlaunchsize"></a>**<span data-ttu-id="c6b6b-143">CachedLaunchSize</span><span class="sxs-lookup"><span data-stu-id="c6b6b-143">CachedLaunchSize</span></span>**  
<span data-ttu-id="c6b6b-144">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-144">Data type: **UInt64**</span></span>

<span data-ttu-id="c6b6b-145">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-145">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-146">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-146">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-147">Die Gesamtgröße des primären Feature Blocks des virtuellen Pakets, der zwischengespeichert wurde, in Kilobytes.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-147">Total size of the virtual package’s primary feature block that has been cached, in kilobytes.</span></span>

<a href="" id="inuse"></a>**<span data-ttu-id="c6b6b-148">InUse</span><span class="sxs-lookup"><span data-stu-id="c6b6b-148">InUse</span></span>**  
<span data-ttu-id="c6b6b-149">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-149">Data type: **Boolean**</span></span>

<span data-ttu-id="c6b6b-150">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-150">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-151">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-151">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-152">" **true** ", wenn eine virtuelle Anwendung im virtuellen Paket ausgeführt wird; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-152">**true** if any virtual application in the virtual package is running; otherwise **false**.</span></span>

<a href="" id="locked"></a>**<span data-ttu-id="c6b6b-153">Gesperrt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-153">Locked</span></span>**  
<span data-ttu-id="c6b6b-154">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-154">Data type: **Boolean**</span></span>

<span data-ttu-id="c6b6b-155">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-155">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-156">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-156">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-157">**true** , wenn das virtuelle Paket gesperrt ist, andernfalls false. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-157">**true** if the virtual package is locked; otherwise **false**.</span></span>

<a href="" id="cachedpercentage"></a>**<span data-ttu-id="c6b6b-158">CachedPercentage</span><span class="sxs-lookup"><span data-stu-id="c6b6b-158">CachedPercentage</span></span>**  
<span data-ttu-id="c6b6b-159">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-159">Data type: **UInt16**</span></span>

<span data-ttu-id="c6b6b-160">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-160">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-161">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-161">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-162">Der Prozentsatz der Cachedateien.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-162">The percentage of the cache files.</span></span> <span data-ttu-id="c6b6b-163">Basierend auf der folgenden Formel: CachedSize/TotalSize × 100.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-163">Based on the following formula: CachedSize / TotalSize × 100.</span></span>

<a href="" id="versionguid"></a>**<span data-ttu-id="c6b6b-164">VersionGUID</span><span class="sxs-lookup"><span data-stu-id="c6b6b-164">VersionGUID</span></span>**  
<span data-ttu-id="c6b6b-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6b6b-165">Data type: **String**</span></span>

<span data-ttu-id="c6b6b-166">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6b6b-166">Access type: Read-only</span></span>

<span data-ttu-id="c6b6b-167">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="c6b6b-167">Qualifiers: None</span></span>

<span data-ttu-id="c6b6b-168">Der GUID-Bezeichner der Paketversion.</span><span class="sxs-lookup"><span data-stu-id="c6b6b-168">The GUID identifier of the package version.</span></span>

 

 





