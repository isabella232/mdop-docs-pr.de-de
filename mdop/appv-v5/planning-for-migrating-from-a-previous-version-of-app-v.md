---
title: Planen der Migration von einer früheren Version von App-V
description: Planen der Migration von einer früheren Version von App-V
author: dansimp
ms.assetid: d4ca8f09-86fd-456f-8ec2-242ff94ae9a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2242f58a29473e116506ec013b94a79d1bb814a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805003"
---
# <span data-ttu-id="5616c-103">Planen der Migration von einer früheren Version von App-V</span><span class="sxs-lookup"><span data-stu-id="5616c-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="5616c-104">Verwenden Sie die folgenden Informationen, um zu planen, wie Sie aus früheren Versionen von App-v zu app-v 5,0 migrieren.</span><span class="sxs-lookup"><span data-stu-id="5616c-104">Use the following information to plan how to migrate to App-V 5.0 from previous versions of App-V.</span></span>

## <span data-ttu-id="5616c-105">Migrationsanforderungen</span><span class="sxs-lookup"><span data-stu-id="5616c-105">Migration requirements</span></span>


<span data-ttu-id="5616c-106">Überprüfen Sie vor dem Starten von Upgrades die folgenden Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="5616c-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="5616c-107">Wenn Sie ein Upgrade von einer älteren Version als App-v 4,6 SP2 durchführen, aktualisieren Sie zuerst auf Version App-v 4,6 SP3, bevor Sie auf App-v 5,0 oder höher aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5616c-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.0 or later.</span></span> <span data-ttu-id="5616c-108">Aktualisieren Sie in diesem Szenario zuerst die App-V-Clients, und aktualisieren Sie dann die Server Komponenten.</span><span class="sxs-lookup"><span data-stu-id="5616c-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="5616c-109">**Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen.</span><span class="sxs-lookup"><span data-stu-id="5616c-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="5616c-110">App-v 5,0 unterstützt nur Pakete, die mit App-v 5,0 erstellt wurden, oder Pakete, die in das App-v 5,0-Format (**AppV**) konvertiert wurden.</span><span class="sxs-lookup"><span data-stu-id="5616c-110">App-V 5.0 supports only packages that are created using App-V 5.0, or packages that have been converted to the App-V 5.0 (**.appv**) format.</span></span>

-   <span data-ttu-id="5616c-111">Nur App-v 5,0 SP3: Wenn Sie den App-v-Server von App-v 5,0 SP1 aktualisieren, finden Sie unter [Informationen zu app-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="5616c-111">App-V 5.0 SP3 only: If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) for instructions.</span></span>

## <span data-ttu-id="5616c-112">Gleichzeitige Ausführung des App-v 5,0-Clients mit App-v 4,6</span><span class="sxs-lookup"><span data-stu-id="5616c-112">Running the App-V 5.0 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="5616c-113">Sie können den App-v 5,0-Client gleichzeitig auf demselben Computer mit dem App-v 4.6 SP3-Client ausführen.</span><span class="sxs-lookup"><span data-stu-id="5616c-113">You can run the App-V 5.0 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="5616c-114">Wenn Sie vorhandene App-V-Clients ausführen, haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="5616c-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="5616c-115">Konvertieren Sie ein App-v 4,6 SP3-Paket in das App-v 5,0-Format, und veröffentlichen Sie beide Pakete, wenn beide Clients ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5616c-115">Convert an App-V 4.6 SP3 package to the App-V 5.0 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="5616c-116">Definieren Sie die Migrations Richtlinie für das konvertierte Paket, sodass das konvertierte App-v 5,0-Paket die Dateitypzuordnungen und Verknüpfungen aus dem App-v 4,6-Paket übernimmt.</span><span class="sxs-lookup"><span data-stu-id="5616c-116">Define the migration policy for the converted package, which allows the converted App-V 5.0 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="5616c-117">Unterstützte Koexistenz-Szenarien</span><span class="sxs-lookup"><span data-stu-id="5616c-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="5616c-118">In der folgenden Tabelle werden die unterstützten App-V-Koexistenz-Szenarien dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5616c-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="5616c-119">Wir empfehlen, dass Sie die neuesten verfügbaren Updates einer bestimmten Version installieren, wenn Sie vorhandene Clients ausführen.</span><span class="sxs-lookup"><span data-stu-id="5616c-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5616c-120">App-V 4,6-Clienttyp</span><span class="sxs-lookup"><span data-stu-id="5616c-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="5616c-121">App-V 5,0-Clienttyp</span><span class="sxs-lookup"><span data-stu-id="5616c-121">App-V 5.0 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5616c-122">App-V 4,6 SP3</span><span class="sxs-lookup"><span data-stu-id="5616c-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="5616c-123">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="5616c-123">App-V 5.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5616c-124">App-V 4,6 SP3 RDS</span><span class="sxs-lookup"><span data-stu-id="5616c-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="5616c-125">App-V 5,0 RDS</span><span class="sxs-lookup"><span data-stu-id="5616c-125">App-V 5.0 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="5616c-126">Voraussetzungen für die Ausführung von vorhandenen Clients</span><span class="sxs-lookup"><span data-stu-id="5616c-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="5616c-127">Damit Sie vorhandene Clients ausführen können, müssen Sie:</span><span class="sxs-lookup"><span data-stu-id="5616c-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="5616c-128">Installieren Sie den App-v 4.6-Client, bevor Sie den App-v 5,0-Client installieren.</span><span class="sxs-lookup"><span data-stu-id="5616c-128">Install the App-V4.6 client before you install the App-V 5.0 client.</span></span>

-   <span data-ttu-id="5616c-129">Aktivieren Sie die Gruppenrichtlinieneinstellung **Migrationsmodus aktivieren** , die sich im Knoten Koexistenz des **App-V-** &gt; **Clients** befindet.</span><span class="sxs-lookup"><span data-stu-id="5616c-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="5616c-130">Informationen zum Bereitstellen der ADMX-Vorlage finden Sie unter [herunterladen und Bereitstellen von MDOP-Vorlagen für Gruppenrichtlinien (ADMX)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="5616c-130">To get the deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

### <span data-ttu-id="5616c-131">Client Downloads und-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5616c-131">Client downloads and documentation</span></span>

<span data-ttu-id="5616c-132">Die folgende Tabelle enthält einen Link zur TechNet-Dokumentation zu den Versionen.</span><span class="sxs-lookup"><span data-stu-id="5616c-132">The following table provides link to the TechNet documentation about the releases.</span></span> <span data-ttu-id="5616c-133">Die TechNet-Dokumentation zum App-V-Client gilt für beide Clients, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="5616c-133">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5616c-134">App-V-Version</span><span class="sxs-lookup"><span data-stu-id="5616c-134">App-V version</span></span></th>
<th align="left"><span data-ttu-id="5616c-135">Link zur TechNet-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5616c-135">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5616c-136">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="5616c-136">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="5616c-137">Informationen zu Microsoft Application Virtualization 4.6SP3</span><span class="sxs-lookup"><span data-stu-id="5616c-137">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5616c-138">App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="5616c-138">App-V 5.0SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-50-sp3.md" data-raw-source="[About Microsoft Application Virtualization 5.0 SP3](about-app-v-50-sp3.md)"><span data-ttu-id="5616c-139">Informationen zu Microsoft Application Virtualization 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="5616c-139">About Microsoft Application Virtualization 5.0 SP3</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5616c-140">Weitere Informationen zum Konfigurieren der Koexistenz von App-V 5,0-Clients finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="5616c-140">For more information about how to configure App-V 5.0 client coexistence, see:</span></span>

-   [<span data-ttu-id="5616c-141">Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf demselben Computer</span><span class="sxs-lookup"><span data-stu-id="5616c-141">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

-   [<span data-ttu-id="5616c-142">App-V 5,0 Koexistenz und Migration</span><span class="sxs-lookup"><span data-stu-id="5616c-142">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="5616c-143">Konvertieren von Paketen der vorherigen Version mithilfe des Paket Konverters</span><span class="sxs-lookup"><span data-stu-id="5616c-143">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="5616c-144">Bevor Sie ein Paket, das mit App-v 4.6 SP3 oder früher erstellt wurde, zu app-v 5,0 migrieren, überprüfen Sie die folgenden Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="5616c-144">Before migrating a package, created using App-V4.6SP3 or earlier, to App-V 5.0, review the following requirements:</span></span>

-   <span data-ttu-id="5616c-145">Sie müssen das Paket in das **AppV-** Dateiformat konvertieren.</span><span class="sxs-lookup"><span data-stu-id="5616c-145">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="5616c-146">Der Paket Konverter unterstützt nur die direkte Konvertierung von Paketen, die mithilfe von App-V 4,5 und höher erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5616c-146">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="5616c-147">Wenn Sie den Paket Konverter für ein Paket verwenden möchten, das mit einer früheren Version erstellt wurde, müssen Sie eine APP-v 4.5 oder höhere Version des Sequencers verwenden, um das Paket zu aktualisieren, und dann können Sie die Paketkonvertierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="5616c-147">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="5616c-148">Weitere Informationen zur Verwendung des Paket Konverters zum Konvertieren eines Pakets finden Sie unter so wird es [gemacht: Konvertieren eines Pakets, das in einer früheren Version von App-V erstellt wurde](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="5616c-148">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md).</span></span> <span data-ttu-id="5616c-149">Nachdem Sie die Datei konvertiert haben, können Sie Sie auf Zielcomputern bereitstellen, auf denen der App-V 5,0-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5616c-149">After you convert the file, you can deploy it to target computers that run the App-V 5.0 client.</span></span>






## <span data-ttu-id="5616c-150">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5616c-150">Related topics</span></span>


[<span data-ttu-id="5616c-151">Planen der Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="5616c-151">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





