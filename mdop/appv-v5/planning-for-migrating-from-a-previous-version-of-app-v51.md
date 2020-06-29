---
title: Planen der Migration von einer früheren Version von App-V
description: Planen der Migration von einer früheren Version von App-V
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805000"
---
# <span data-ttu-id="513c6-103">Planen der Migration von einer früheren Version von App-V</span><span class="sxs-lookup"><span data-stu-id="513c6-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="513c6-104">Verwenden Sie die folgenden Informationen, um die Migration zu Microsoft Application Virtualization (app-v) 5,1 aus früheren Versionen von App-v zu planen.</span><span class="sxs-lookup"><span data-stu-id="513c6-104">Use the following information to plan how to migrate to Microsoft Application Virtualization (App-V) 5.1 from previous versions of App-V.</span></span>

## <span data-ttu-id="513c6-105">Migrationsanforderungen</span><span class="sxs-lookup"><span data-stu-id="513c6-105">Migration requirements</span></span>


<span data-ttu-id="513c6-106">Überprüfen Sie vor dem Starten von Upgrades die folgenden Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="513c6-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="513c6-107">Wenn Sie ein Upgrade von einer älteren Version als App-v 4,6 SP2 durchführen, aktualisieren Sie zuerst auf Version App-v 4,6 SP3, bevor Sie auf App-v 5,1 oder höher aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="513c6-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.1 or later.</span></span> <span data-ttu-id="513c6-108">Aktualisieren Sie in diesem Szenario zuerst die App-V-Clients, und aktualisieren Sie dann die Server Komponenten.</span><span class="sxs-lookup"><span data-stu-id="513c6-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="513c6-109">**Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen.</span><span class="sxs-lookup"><span data-stu-id="513c6-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="513c6-110">App-v 5,1 unterstützt nur Pakete, die mit App-v 5,0 oder App-v 5,1 erstellt wurden, oder Pakete, die in das **AppV** -Format konvertiert wurden.</span><span class="sxs-lookup"><span data-stu-id="513c6-110">App-V 5.1 supports only packages that are created using App-V 5.0 or App-V 5.1, or packages that have been converted to the **.appv** format.</span></span>

-   <span data-ttu-id="513c6-111">Wenn Sie den App-v-Server von App-v 5,0 SP1 aktualisieren, lesen Sie [Informationen zu app-v 5,1](about-app-v-51.md#bkmk-migrate-to-51) .</span><span class="sxs-lookup"><span data-stu-id="513c6-111">If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51) for instructions.</span></span>

## <span data-ttu-id="513c6-112">Gleichzeitige Ausführung des App-v 5,1-Clients mit App-v 4,6</span><span class="sxs-lookup"><span data-stu-id="513c6-112">Running the App-V 5.1 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="513c6-113">Sie können den App-v 5,1-Client gleichzeitig auf demselben Computer mit dem App-v 4.6 SP3-Client ausführen.</span><span class="sxs-lookup"><span data-stu-id="513c6-113">You can run the App-V 5.1 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="513c6-114">Wenn Sie vorhandene App-V-Clients ausführen, haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="513c6-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="513c6-115">Konvertieren Sie ein App-v 4,6 SP3-Paket in das App-v 5,1-Format, und veröffentlichen Sie beide Pakete, wenn beide Clients ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="513c6-115">Convert an App-V 4.6 SP3 package to the App-V 5.1 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="513c6-116">Definieren Sie die Migrations Richtlinie für das konvertierte Paket, sodass das konvertierte App-v 5,1-Paket die Dateitypzuordnungen und Verknüpfungen aus dem App-v 4,6-Paket übernimmt.</span><span class="sxs-lookup"><span data-stu-id="513c6-116">Define the migration policy for the converted package, which allows the converted App-V 5.1 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="513c6-117">Unterstützte Koexistenz-Szenarien</span><span class="sxs-lookup"><span data-stu-id="513c6-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="513c6-118">In der folgenden Tabelle werden die unterstützten App-V-Koexistenz-Szenarien dargestellt.</span><span class="sxs-lookup"><span data-stu-id="513c6-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="513c6-119">Wir empfehlen, dass Sie die neuesten verfügbaren Updates einer bestimmten Version installieren, wenn Sie vorhandene Clients ausführen.</span><span class="sxs-lookup"><span data-stu-id="513c6-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="513c6-120">App-V 4,6-Clienttyp</span><span class="sxs-lookup"><span data-stu-id="513c6-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="513c6-121">App-V 5,1-Clienttyp</span><span class="sxs-lookup"><span data-stu-id="513c6-121">App-V 5.1 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="513c6-122">App-V 4,6 SP3</span><span class="sxs-lookup"><span data-stu-id="513c6-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="513c6-123">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="513c6-123">App-V 5.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="513c6-124">App-V 4,6 SP3 RDS</span><span class="sxs-lookup"><span data-stu-id="513c6-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="513c6-125">App-V 5,1 RDS</span><span class="sxs-lookup"><span data-stu-id="513c6-125">App-V 5.1 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="513c6-126">Voraussetzungen für die Ausführung von vorhandenen Clients</span><span class="sxs-lookup"><span data-stu-id="513c6-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="513c6-127">Damit Sie vorhandene Clients ausführen können, müssen Sie:</span><span class="sxs-lookup"><span data-stu-id="513c6-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="513c6-128">Installieren Sie den App-v 4.6-Client, bevor Sie den App-v 5,1-Client installieren.</span><span class="sxs-lookup"><span data-stu-id="513c6-128">Install the App-V4.6 client before you install the App-V 5.1 client.</span></span>

-   <span data-ttu-id="513c6-129">Aktivieren Sie die Gruppenrichtlinieneinstellung **Migrationsmodus aktivieren** , die sich im Knoten Koexistenz des **App-V-** &gt; **Clients** befindet.</span><span class="sxs-lookup"><span data-stu-id="513c6-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="513c6-130">Informationen zum Bereitstellen der ADMX-Vorlage finden Sie unter [herunterladen und Bereitstellen von MDOP-Gruppenrichtlinienvorlagen (ADMX)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="513c6-130">To deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

<span data-ttu-id="513c6-131">**Hinweis**  App-v 5,1-Pakete können parallel zu app-v 4,6-Paketen ausgeführt werden, wenn Sie über nebeneinander vorhandene Installationen von App-v 5,1 und 4,6 verfügen.</span><span class="sxs-lookup"><span data-stu-id="513c6-131">**Note** App-V 5.1 packages can run side by side with App-V 4.6 packages if you have coexisting installations of App-V 5.1 and 4.6.</span></span> <span data-ttu-id="513c6-132">App-v 5,1-Pakete können jedoch nicht mit App-v 4,6-Paketen in derselben virtuellen Umgebung interagieren.</span><span class="sxs-lookup"><span data-stu-id="513c6-132">However, App-V 5.1 packages cannot interact with App-V 4.6 packages in the same virtual environment.</span></span>

 

### <span data-ttu-id="513c6-133">Client Downloads und-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="513c6-133">Client downloads and documentation</span></span>

<span data-ttu-id="513c6-134">Die folgende Tabelle enthält Links zu den App-V 4,6-Clientdownloads und zur TechNet-Dokumentation zu den Versionen.</span><span class="sxs-lookup"><span data-stu-id="513c6-134">The following table provides links to the App-V 4.6 client downloads and to the TechNet documentation about the releases.</span></span> <span data-ttu-id="513c6-135">Zu den Downloads gehören die App-V "reguläre" und RDS-Clients.</span><span class="sxs-lookup"><span data-stu-id="513c6-135">The downloads include the App-V “regular” and RDS clients.</span></span> <span data-ttu-id="513c6-136">Die TechNet-Dokumentation zum App-V-Client gilt für beide Clients, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="513c6-136">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="513c6-137">App-V-Version</span><span class="sxs-lookup"><span data-stu-id="513c6-137">App-V version</span></span></th>
<th align="left"><span data-ttu-id="513c6-138">Link zur TechNet-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="513c6-138">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="513c6-139">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="513c6-139">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="513c6-140">Informationen zu Microsoft Application Virtualization 4.6SP3</span><span class="sxs-lookup"><span data-stu-id="513c6-140">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="513c6-141">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="513c6-141">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)"><span data-ttu-id="513c6-142">Informationen zu Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="513c6-142">About Microsoft Application Virtualization 5.1</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="513c6-143">Weitere Informationen zum Konfigurieren der Koexistenz von App-V 5,1-Clients finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="513c6-143">For more information about how to configure App-V 5.1 client coexistence, see:</span></span>

-   [<span data-ttu-id="513c6-144">Bereitstellen der APP-v 4,6 und des App-v 5,1-Clients auf demselben Computer</span><span class="sxs-lookup"><span data-stu-id="513c6-144">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [<span data-ttu-id="513c6-145">App-V 5,0 Koexistenz und Migration</span><span class="sxs-lookup"><span data-stu-id="513c6-145">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="513c6-146">Konvertieren von Paketen der vorherigen Version mithilfe des Paket Konverters</span><span class="sxs-lookup"><span data-stu-id="513c6-146">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="513c6-147">Bevor Sie ein Paket, das mit App-4.6 SP2 oder früher erstellt wurde, zu App-V 5,1 migrieren, überprüfen Sie die folgenden Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="513c6-147">Before migrating a package, created using App-4.6SP2 or earlier, to App-V 5.1, review the following requirements:</span></span>

-   <span data-ttu-id="513c6-148">Sie müssen das Paket in das **AppV-** Dateiformat konvertieren.</span><span class="sxs-lookup"><span data-stu-id="513c6-148">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="513c6-149">Der Paket Konverter unterstützt nur die direkte Konvertierung von Paketen, die mithilfe von App-V 4,5 und höher erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="513c6-149">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="513c6-150">Wenn Sie den Paket Konverter für ein Paket verwenden möchten, das mit einer früheren Version erstellt wurde, müssen Sie eine APP-v 4.5 oder höhere Version des Sequencers verwenden, um das Paket zu aktualisieren, und dann können Sie die Paketkonvertierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="513c6-150">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="513c6-151">Weitere Informationen zur Verwendung des Paket Konverters zum Konvertieren eines Pakets finden Sie unter so wird es [gemacht: Konvertieren eines Pakets, das in einer früheren Version von App-V erstellt wurde](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="513c6-151">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span></span> <span data-ttu-id="513c6-152">Nachdem Sie die Datei konvertiert haben, können Sie Sie auf Zielcomputern bereitstellen, auf denen der App-V 5,1-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="513c6-152">After you convert the file, you can deploy it to target computers that run the App-V 5.1 client.</span></span>






## <span data-ttu-id="513c6-153">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="513c6-153">Related topics</span></span>


[<span data-ttu-id="513c6-154">Planen der Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="513c6-154">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





