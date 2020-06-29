---
title: WMI-Klasse für App-V-Anwendungen
description: WMI-Klasse für App-V-Anwendungen
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809286"
---
# <span data-ttu-id="6aff2-103">WMI-Klasse für App-V-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6aff2-103">App-V Application WMI Class</span></span>


<span data-ttu-id="6aff2-104">Beim Application Virtualization-Client (App-V) handelt es sich bei der **Anwendungs** Klasse um eine WMI-Klasse (Windows Management Instrumentation), die alle virtuellen Anwendungen auf dem Client darstellt.</span><span class="sxs-lookup"><span data-stu-id="6aff2-104">In the Application Virtualization (App-V) Client, the **Application** class is a Windows Management Instrumentation (WMI) class that represents all the virtual applications on the client.</span></span>

<span data-ttu-id="6aff2-105">Die folgende Syntax ist vom MOF-Code (Managed Object Format) vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="6aff2-105">The following syntax is simplified from Managed Object Format (MOF) code.</span></span> <span data-ttu-id="6aff2-106">Der Code enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6aff2-106">The code includes all the inherited properties.</span></span>

## <span data-ttu-id="6aff2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6aff2-107">Syntax</span></span>


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## <span data-ttu-id="6aff2-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6aff2-108">Requirements</span></span>


## <span data-ttu-id="6aff2-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6aff2-109">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="6aff2-110">Name</span><span class="sxs-lookup"><span data-stu-id="6aff2-110">Name</span></span>**  
<span data-ttu-id="6aff2-111">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aff2-111">Data type: **String**</span></span>

<span data-ttu-id="6aff2-112">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aff2-112">Access type: Read-only</span></span>

<span data-ttu-id="6aff2-113">Qualifizierer: Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6aff2-113">Qualifiers: Key</span></span>

<span data-ttu-id="6aff2-114">Der Anzeigename der virtuellen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6aff2-114">The display name of the virtual application.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="6aff2-115">Version</span><span class="sxs-lookup"><span data-stu-id="6aff2-115">Version</span></span>**  
<span data-ttu-id="6aff2-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aff2-116">Data type: **String**</span></span>

<span data-ttu-id="6aff2-117">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aff2-117">Access type: Read-only</span></span>

<span data-ttu-id="6aff2-118">Qualifizierer: Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6aff2-118">Qualifiers: Key</span></span>

<span data-ttu-id="6aff2-119">Die Version der virtuellen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6aff2-119">The version of the virtual application.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="6aff2-120">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="6aff2-120">PackageGUID</span></span>**  
<span data-ttu-id="6aff2-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aff2-121">Data type: **String**</span></span>

<span data-ttu-id="6aff2-122">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aff2-122">Access type: Read-only</span></span>

<span data-ttu-id="6aff2-123">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="6aff2-123">Qualifiers: None</span></span>

<span data-ttu-id="6aff2-124">Die GUID des Pakets, dem die virtuelle Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6aff2-124">The GUID of the package that the virtual application is associated with.</span></span>

<a href="" id="lastlaunchonsystem"></a>**<span data-ttu-id="6aff2-125">LastLaunchOnSystem</span><span class="sxs-lookup"><span data-stu-id="6aff2-125">LastLaunchOnSystem</span></span>**  
<span data-ttu-id="6aff2-126">Datentyp: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6aff2-126">Data type: **DateTime**</span></span>

<span data-ttu-id="6aff2-127">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aff2-127">Access type: Read-only</span></span>

<span data-ttu-id="6aff2-128">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="6aff2-128">Qualifiers: None</span></span>

<span data-ttu-id="6aff2-129">Das Datum und die Uhrzeit des letzten Starts der virtuellen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6aff2-129">The last date and time that the virtual application was launched.</span></span>

<a href="" id="globalrunningcount"></a>**<span data-ttu-id="6aff2-130">GlobalRunningCount</span><span class="sxs-lookup"><span data-stu-id="6aff2-130">GlobalRunningCount</span></span>**  
<span data-ttu-id="6aff2-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6aff2-131">Data type: **UInt32**</span></span>

<span data-ttu-id="6aff2-132">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aff2-132">Access type: Read-only</span></span>

<span data-ttu-id="6aff2-133">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="6aff2-133">Qualifiers: None</span></span>

<span data-ttu-id="6aff2-134">Die Anzahl der ausgeführten Instanzen der virtuellen Anwendung, die direkt gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="6aff2-134">A count of the running instances of the virtual application that were started directly.</span></span>

<a href="" id="loading"></a>**<span data-ttu-id="6aff2-135">Laden</span><span class="sxs-lookup"><span data-stu-id="6aff2-135">Loading</span></span>**  
<span data-ttu-id="6aff2-136">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="6aff2-136">Data type: **Boolean**</span></span>

<span data-ttu-id="6aff2-137">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aff2-137">Access type: Read-only</span></span>

<span data-ttu-id="6aff2-138">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="6aff2-138">Qualifiers: None</span></span>

<span data-ttu-id="6aff2-139">" **true** ", wenn die virtuelle Anwendung gestartet wird; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="6aff2-139">**true** if the virtual application is being started; otherwise **false**.</span></span>

<a href="" id="originalosdpath"></a>**<span data-ttu-id="6aff2-140">OriginalOsdPath</span><span class="sxs-lookup"><span data-stu-id="6aff2-140">OriginalOsdPath</span></span>**  
<span data-ttu-id="6aff2-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aff2-141">Data type: **String**</span></span>

<span data-ttu-id="6aff2-142">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aff2-142">Access type: Read-only</span></span>

<span data-ttu-id="6aff2-143">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="6aff2-143">Qualifiers: None</span></span>

<span data-ttu-id="6aff2-144">Der ursprüngliche Dateipfad der OSD-Datei, die beim App-V-Client registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="6aff2-144">The original file path of the OSD file that was registered with the App-V Client.</span></span>

<a href="" id="cachedosdpath"></a>**<span data-ttu-id="6aff2-145">CachedOsdPath</span><span class="sxs-lookup"><span data-stu-id="6aff2-145">CachedOsdPath</span></span>**  
<span data-ttu-id="6aff2-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aff2-146">Data type: **String**</span></span>

<span data-ttu-id="6aff2-147">Access-Typ: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aff2-147">Access type: Read-only</span></span>

<span data-ttu-id="6aff2-148">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="6aff2-148">Qualifiers: None</span></span>

<span data-ttu-id="6aff2-149">Der Dateipfad der OSD-Datei, wenn der App-V-Client die OSD-Datei lokal zwischengespeichert hat.</span><span class="sxs-lookup"><span data-stu-id="6aff2-149">The file path of the OSD file if the App-V Client has cached the OSD file locally.</span></span>

 

 





