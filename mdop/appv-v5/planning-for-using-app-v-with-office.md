---
title: Planen der Verwendung von App-V mit Office
description: Planen der Verwendung von App-V mit Office
author: dansimp
ms.assetid: c4371869-4bfc-4d13-9198-ef19f99fc192
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff523c8f8827e295c8fb9a2d9fd0e02d5b019aa8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804967"
---
# <span data-ttu-id="3d224-103">Planen der Verwendung von App-V mit Office</span><span class="sxs-lookup"><span data-stu-id="3d224-103">Planning for Using App-V with Office</span></span>


<span data-ttu-id="3d224-104">Verwenden Sie die folgenden Informationen, um zu planen, wie Office mithilfe von App-V bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3d224-104">Use the following information to plan how to deploy Office by using App-V.</span></span> <span data-ttu-id="3d224-105">Dieser Artikel enthält:</span><span class="sxs-lookup"><span data-stu-id="3d224-105">This article includes:</span></span>

-   [<span data-ttu-id="3d224-106">App-V-Unterstützung für Sprachpakete</span><span class="sxs-lookup"><span data-stu-id="3d224-106">App-V support for Language Packs</span></span>](#bkmk-lang-pack)

-   [<span data-ttu-id="3d224-107">Unterstützte Versionen von Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="3d224-107">Supported versions of Microsoft Office</span></span>](#bkmk-office-vers-supp-appv)

-   [<span data-ttu-id="3d224-108">Planen der Verwendung von App-V mit vorhandenen Office-Versionen</span><span class="sxs-lookup"><span data-stu-id="3d224-108">Planning for using App-V with coexisting versions of Office</span></span>](#bkmk-plan-coexisting)

-   [<span data-ttu-id="3d224-109">Integration von Office in Windows bei der Bereitstellung von use App-V für die Bereitstellung von Office</span><span class="sxs-lookup"><span data-stu-id="3d224-109">How Office integrates with Windows when you deploy use App-V to deploy Office</span></span>](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a><span data-ttu-id="3d224-110">App-V-Unterstützung für Sprachpakete</span><span class="sxs-lookup"><span data-stu-id="3d224-110">App-V support for Language Packs</span></span>


<span data-ttu-id="3d224-111">Sie können den App-V 5,0-Sequenzer verwenden, um Plug-in-Pakete für Sprachpakete, Sprachschnittstellen Pakete, Korrekturhilfen und QuickInfo-Sprachen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d224-111">You can use the App-V 5.0 Sequencer to create plug-in packages for Language Packs, Language Interface Packs, Proofing Tools and ScreenTip Languages.</span></span> <span data-ttu-id="3d224-112">Sie können dann zusammen mit dem Office 2013-Paket, das Sie mit dem Office Deployment Toolkit erstellen, die Plug-in-Pakete in eine Verbindungsgruppe einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="3d224-112">You can then include the plug-in packages in a Connection Group, along with the Office 2013 package that you create by using the Office Deployment Toolkit.</span></span> <span data-ttu-id="3d224-113">Die Office-Anwendungen und die Plug-in-Sprachpakete interagieren nahtlos in derselben Verbindungsgruppe, genau wie alle anderen Pakete, die in einer Verbindungsgruppe gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="3d224-113">The Office applications and the plug-in Language Packs interact seamlessly in the same connection group, just like any other packages that are grouped together in a connection group.</span></span>

<span data-ttu-id="3d224-114">**Hinweis**  Microsoft Visio und Microsoft Project bieten keine Unterstützung für das Thai-Sprachpaket.</span><span class="sxs-lookup"><span data-stu-id="3d224-114">**Note** Microsoft Visio and Microsoft Project do not provide support for the Thai Language Pack.</span></span>

 

## <a href="" id="bkmk-office-vers-supp-appv"></a><span data-ttu-id="3d224-115">Unterstützte Versionen von Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="3d224-115">Supported versions of Microsoft Office</span></span>


<span data-ttu-id="3d224-116">In der folgenden Tabelle sind die Versionen von Microsoft Office aufgeführt, die App-V unterstützt, Methoden zur Erstellung von Office-Paketen, unterstützte Lizenzierung und unterstützte Bereitstellungen.</span><span class="sxs-lookup"><span data-stu-id="3d224-116">The following table lists the versions of Microsoft Office that App-V supports, methods of Office package creation, supported licensing, and supported deployments.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d224-117">Unterstützte Office-Version</span><span class="sxs-lookup"><span data-stu-id="3d224-117">Supported Office Version</span></span></th>
<th align="left"><span data-ttu-id="3d224-118">Unterstützte App-V-Versionen</span><span class="sxs-lookup"><span data-stu-id="3d224-118">Supported App-V Versions</span></span></th>
<th align="left"><span data-ttu-id="3d224-119">Paketerstellung</span><span class="sxs-lookup"><span data-stu-id="3d224-119">Package Creation</span></span></th>
<th align="left"><span data-ttu-id="3d224-120">Unterstützte Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="3d224-120">Supported Licensing</span></span></th>
<th align="left"><span data-ttu-id="3d224-121">Unterstützte Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="3d224-121">Supported Deployments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-122">Microsoft 365-Apps für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="3d224-122">Microsoft 365 Apps for enterprise</span></span></p>
<p><span data-ttu-id="3d224-123">Ebenfalls unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3d224-123">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="3d224-124">Visio pro für Office 365</span><span class="sxs-lookup"><span data-stu-id="3d224-124">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="3d224-125">Project pro für Office 365</span><span class="sxs-lookup"><span data-stu-id="3d224-125">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3d224-126">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3d224-126">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="3d224-127">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="3d224-127">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="3d224-128">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="3d224-128">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="3d224-129">Office-Bereitstellungs Tool</span><span class="sxs-lookup"><span data-stu-id="3d224-129">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-130">Abonnement</span><span class="sxs-lookup"><span data-stu-id="3d224-130">Subscription</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3d224-131">Desktop</span><span class="sxs-lookup"><span data-stu-id="3d224-131">Desktop</span></span></p></li>
<li><p><span data-ttu-id="3d224-132">Persönlicher VDI</span><span class="sxs-lookup"><span data-stu-id="3d224-132">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="3d224-133">Gebündelter VDI</span><span class="sxs-lookup"><span data-stu-id="3d224-133">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="3d224-134">RDS</span><span class="sxs-lookup"><span data-stu-id="3d224-134">RDS</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-135">Office Professional Plus 2013</span><span class="sxs-lookup"><span data-stu-id="3d224-135">Office Professional Plus 2013</span></span></p>
<p><span data-ttu-id="3d224-136">Ebenfalls unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3d224-136">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="3d224-137">Visio Professional 2013</span><span class="sxs-lookup"><span data-stu-id="3d224-137">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="3d224-138">Project Professional 2013</span><span class="sxs-lookup"><span data-stu-id="3d224-138">Project Professional 2013</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3d224-139">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3d224-139">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="3d224-140">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="3d224-140">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="3d224-141">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="3d224-141">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="3d224-142">Office-Bereitstellungs Tool</span><span class="sxs-lookup"><span data-stu-id="3d224-142">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-143">Volumenlizenzierung</span><span class="sxs-lookup"><span data-stu-id="3d224-143">Volume Licensing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3d224-144">Desktop</span><span class="sxs-lookup"><span data-stu-id="3d224-144">Desktop</span></span></p></li>
<li><p><span data-ttu-id="3d224-145">Persönlicher VDI</span><span class="sxs-lookup"><span data-stu-id="3d224-145">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="3d224-146">Gebündelter VDI</span><span class="sxs-lookup"><span data-stu-id="3d224-146">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="3d224-147">RDS</span><span class="sxs-lookup"><span data-stu-id="3d224-147">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-plan-coexisting"></a><span data-ttu-id="3d224-148">Planen der Verwendung von App-V mit vorhandenen Office-Versionen</span><span class="sxs-lookup"><span data-stu-id="3d224-148">Planning for using App-V with coexisting versions of Office</span></span>


<span data-ttu-id="3d224-149">Sie können mehr als eine Version von Microsoft Office nebeneinander auf demselben Computer installieren, indem Sie "Microsoft Office-Koexistenz" verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d224-149">You can install more than one version of Microsoft Office side by side on the same computer by using “Microsoft Office coexistence.”</span></span> <span data-ttu-id="3d224-150">Mithilfe der Windows Installer-basierten (MSI)-Version von Office, Klick-und-Los und App-V 5,0 SP2 können Sie die Office-Koexistenz mit Kombinationen aus allen Hauptversionen von Office und den Installationsmethoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="3d224-150">You can implement Office coexistence with combinations of all major versions of Office and with installation methods, as applicable, by using the Windows Installer-based (MSi) version of Office, Click-to-Run, and App-V 5.0 SP2.</span></span> <span data-ttu-id="3d224-151">Die Verwendung der Office-Koexistenz wird von Microsoft jedoch nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="3d224-151">However, using Office coexistence is not recommended by Microsoft.</span></span>

<span data-ttu-id="3d224-152">Microsoft empfiehlt bewährte Methoden, die Zusammenarbeit von Office komplett zu vermeiden, um Kompatibilitätsprobleme zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3d224-152">Microsoft’s recommended best practice is to avoid Office coexistence completely to prevent compatibility issues.</span></span> <span data-ttu-id="3d224-153">Wenn Sie jedoch zu einer neueren Version von Office migrieren, treten gelegentlich Probleme auf, die nicht sofort behoben werden können, sodass Sie die Koexistenz vorübergehend implementieren können, um eine schnellere Migration zur neuesten Produktversion zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3d224-153">However, when you are migrating to a newer version of Office, issues occasionally arise that can’t be resolved immediately, so you can temporarily implement coexistence to help facilitate a faster migration to the latest product version.</span></span> <span data-ttu-id="3d224-154">Die Verwendung von Office-Koexistenz auf lange Sicht wird nie empfohlen, und Ihre Organisation sollte in nächster Zukunft einen Plan für den vollständigen Übergang haben.</span><span class="sxs-lookup"><span data-stu-id="3d224-154">Using Office coexistence on a long-term basis is never recommended, and your organization should have a plan to fully transition in the immediate future.</span></span>

### <span data-ttu-id="3d224-155">Bevor Sie die Office-Koexistenz implementieren</span><span class="sxs-lookup"><span data-stu-id="3d224-155">Before you implement Office coexistence</span></span>

<span data-ttu-id="3d224-156">Bevor Sie die Office-Koexistenz implementieren, lesen Sie die folgende Office-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3d224-156">Before implementing Office coexistence, review the following Office documentation.</span></span> <span data-ttu-id="3d224-157">Wählen Sie den Artikel aus, der der neuesten Version von Office entspricht, für die Sie die Koexistenz durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="3d224-157">Choose the article that corresponds to the newest version of Office for which you plan to implement coexistence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d224-158">Office-Version</span><span class="sxs-lookup"><span data-stu-id="3d224-158">Office version</span></span></th>
<th align="left"><span data-ttu-id="3d224-159">Link zur Anleitung</span><span class="sxs-lookup"><span data-stu-id="3d224-159">Link to guidance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-160">Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d224-160">Office 2013</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)"><span data-ttu-id="3d224-161">Informationen zur Verwendung von Office 2013-Suites und-Programmen (MSI-Bereitstellung) auf einem Computer, auf dem eine andere Version von Office ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="3d224-161">Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-162">Office 2010</span><span class="sxs-lookup"><span data-stu-id="3d224-162">Office 2010</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)"><span data-ttu-id="3d224-163">Informationen zum Verwenden von Office 2010-Suites und-Programmen auf einem Computer, auf dem eine andere Office-Version ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="3d224-163">Information about how to use Office 2010 suites and programs on a computer that is running another version of Office</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3d224-164">Die Office-Dokumentation bietet umfassende Anleitungen zur Koexistenz für Windows Installer-basierte (MSI)-und Klick-und-Los-Installationen von Office.</span><span class="sxs-lookup"><span data-stu-id="3d224-164">The Office documentation provides extensive guidance on coexistence for Windows Installer-based (MSi) and Click-to-Run installations of Office.</span></span> <span data-ttu-id="3d224-165">Dieses app-v-Thema zur Koexistenz ergänzt die Office-Anleitung mit Informationen, die für App-v-Bereitstellungen spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="3d224-165">This App-V topic on coexistence supplements the Office guidance with information that is more specific to App-V deployments.</span></span>

### <span data-ttu-id="3d224-166">Unterstützte Szenarien für die Koexistenz von Office</span><span class="sxs-lookup"><span data-stu-id="3d224-166">Supported Office coexistence scenarios</span></span>

<span data-ttu-id="3d224-167">In den folgenden Tabellen werden die unterstützten Koexistenz-Szenarien zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="3d224-167">The following tables summarize the supported coexistence scenarios.</span></span> <span data-ttu-id="3d224-168">Sie werden gemäß der Version und der Bereitstellungsmethode organisiert, mit der Sie beginnen, und der Version und Bereitstellungsmethode, zu der Sie migrieren.</span><span class="sxs-lookup"><span data-stu-id="3d224-168">They are organized according to the version and deployment method you’re starting with and the version and deployment method you are migrating to.</span></span> <span data-ttu-id="3d224-169">Testen Sie alle Koexistenz-Lösungen unbedingt, bevor Sie Sie für eine Produktionsgruppe bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3d224-169">Be sure to fully test all coexistence solutions before deploying them to a production audience.</span></span>

<span data-ttu-id="3d224-170">**Hinweis**  Microsoft unterstützt nicht die Verwendung mehrerer Office-Versionen in Windows Server-Umgebungen, in denen der Rollendienst "Remote Desktop-Sitzungs Host" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3d224-170">**Note** Microsoft does not support the use of multiple versions of Office in Windows Server environments that have the Remote Desktop Session Host role service enabled.</span></span> <span data-ttu-id="3d224-171">Zum Ausführen von Szenarien für die Koexistenz von Office müssen Sie diesen Rollendienst deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3d224-171">To run Office coexistence scenarios, you must disable this role service.</span></span>

 

### <span data-ttu-id="3d224-172">Windows-Integrationen & Office-Koexistenz</span><span class="sxs-lookup"><span data-stu-id="3d224-172">Windows integrations & Office coexistence</span></span>

<span data-ttu-id="3d224-173">Die Windows Installer-basierten und Klick-und-Los-Installationsmethoden werden in bestimmte Punkte des zugrunde liegenden Windows-Betriebssystems integriert.</span><span class="sxs-lookup"><span data-stu-id="3d224-173">The Windows Installer-based and Click-to-Run Office installation methods integrate with certain points of the underlying Windows operating system.</span></span> <span data-ttu-id="3d224-174">Wenn Sie die Koexistenz verwenden, können allgemeine Betriebssystem Integrationen zwischen zwei Office-Versionen zu Konflikten führen, wodurch Kompatibilitäts-und Benutzer Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="3d224-174">When you use coexistence, common operating system integrations between two Office versions can conflict, causing compatibility and user experience issues.</span></span> <span data-ttu-id="3d224-175">Mit App-V können Sie bestimmte Office-Versionen abgleichen, um Integrationen auszuschließen, wodurch Sie aus dem Betriebssystem "isoliert" werden.</span><span class="sxs-lookup"><span data-stu-id="3d224-175">With App-V, you can sequence certain versions of Office to exclude integrations, thereby “isolating” them from the operating system.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="3d224-176">Modus, in dem App-V diese Version von Office Sequenzieren kann</span><span class="sxs-lookup"><span data-stu-id="3d224-176">Mode in which App-V can sequence this version of Office</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-177">Office 2007</span><span class="sxs-lookup"><span data-stu-id="3d224-177">Office 2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-178">Immer nicht integriert.</span><span class="sxs-lookup"><span data-stu-id="3d224-178">Always non-integrated.</span></span> <span data-ttu-id="3d224-179">App-V bietet keine Betriebssystem Integrationen mit einer virtualisierten Version von Office 2007.</span><span class="sxs-lookup"><span data-stu-id="3d224-179">App-V does not offer any operating system integrations with a virtualized version of Office 2007.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-180">Office 2010</span><span class="sxs-lookup"><span data-stu-id="3d224-180">Office 2010</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-181">Integrierter und nicht integrierter Modus.</span><span class="sxs-lookup"><span data-stu-id="3d224-181">Integrated and non-integrated mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-182">Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d224-182">Office 2013</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-183">Immer integriert.</span><span class="sxs-lookup"><span data-stu-id="3d224-183">Always integrated.</span></span> <span data-ttu-id="3d224-184">Windows-Betriebssystem Integrationen können nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="3d224-184">Windows operating system integrations cannot be disabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3d224-185">Microsoft empfiehlt, dass Sie die Office-Koexistenz mit nur einer integrierten Office-Instanz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3d224-185">Microsoft recommends that you deploy Office coexistence with only one integrated Office instance.</span></span> <span data-ttu-id="3d224-186">Wenn Sie beispielsweise App-V zum Bereitstellen von Office 2010 und Office 2013 verwenden, sollten Sie Office 2010 im nicht integrierten Modus sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="3d224-186">For example, if you’re using App-V to deploy Office 2010 and Office 2013, you should sequence Office 2010 in non-integrated mode.</span></span> <span data-ttu-id="3d224-187">Weitere Informationen zur Sequenzierung von Office im nicht Integrationsmodus (isoliert) finden Sie unter [so wird es gemacht: Sequenzierung von Microsoft Office 2010 in Microsoft Application Virtualization 5,0](https://support.microsoft.com/kb/2830069).</span><span class="sxs-lookup"><span data-stu-id="3d224-187">For more information about sequencing Office in non-integration (isolated) mode, see [How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0](https://support.microsoft.com/kb/2830069).</span></span>

### <span data-ttu-id="3d224-188">Bekannte Einschränkungen von Szenarien für die Koexistenz von Office</span><span class="sxs-lookup"><span data-stu-id="3d224-188">Known limitations of Office coexistence scenarios</span></span>

<span data-ttu-id="3d224-189">In den folgenden Abschnitten werden einige Probleme beschrieben, die bei der Verwendung von App-V zur Implementierung der Koexistenz mit Office auftreten können.</span><span class="sxs-lookup"><span data-stu-id="3d224-189">The following sections describe some issues that you might encounter when using App-V to implement coexistence with Office.</span></span>

### <span data-ttu-id="3d224-190">Einschränkungen, die für Windows Installer-basierte/Klick-und-Los-und App-V-Koexistenz-Szenarien üblich sind</span><span class="sxs-lookup"><span data-stu-id="3d224-190">Limitations common to Windows Installer-based/Click-to-Run and App-V Office coexistence scenarios</span></span>

<span data-ttu-id="3d224-191">Die folgenden Einschränkungen können auftreten, wenn Sie die folgenden Office-Versionen auf demselben Computer installieren:</span><span class="sxs-lookup"><span data-stu-id="3d224-191">The following limitations can occur when you install the following versions of Office on the same computer:</span></span>

-   <span data-ttu-id="3d224-192">Office 2010 mit Windows Installer-basierter Version</span><span class="sxs-lookup"><span data-stu-id="3d224-192">Office 2010 by using the Windows Installer-based version</span></span>

-   <span data-ttu-id="3d224-193">Office 2013 mithilfe von App-V</span><span class="sxs-lookup"><span data-stu-id="3d224-193">Office 2013 by using App-V</span></span>

<span data-ttu-id="3d224-194">Nachdem Sie Office 2013 mithilfe von App-V nebeneinander mit einer früheren Version des Windows Installer-basierten Office 2010 veröffentlicht haben, kann dies auch dazu führen, dass Windows Installer gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3d224-194">After you publish Office 2013 by using App-V side by side with an earlier version of the Windows Installer-based Office 2010 might also cause the Windows Installer to start.</span></span> <span data-ttu-id="3d224-195">Dies liegt daran, dass die Windows Installer-basierte oder Klick-und-Los-Version von Office 2010 versucht, sich automatisch auf dem Computer zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="3d224-195">This is because the Windows Installer-based or Click-to-Run version of Office 2010 is trying to automatically register itself to the computer.</span></span>

<span data-ttu-id="3d224-196">Führen Sie die folgenden Schritte aus, um den automatischen Registrierungsvorgang für systemeigene Word 2010 zu umgehen:</span><span class="sxs-lookup"><span data-stu-id="3d224-196">To bypass the auto-registration operation for native Word 2010, follow these steps:</span></span>

1.  <span data-ttu-id="3d224-197">Beenden Sie Word 2010.</span><span class="sxs-lookup"><span data-stu-id="3d224-197">Exit Word 2010.</span></span>

2.  <span data-ttu-id="3d224-198">Starten Sie den Registrierungs-Editor, indem Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="3d224-198">Start the Registry Editor by doing the following:</span></span>

    -   <span data-ttu-id="3d224-199">Unter Windows 7: Klicken Sie auf **Start**, geben Sie im Feld Suche starten den **Befehl regedit** ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="3d224-199">In Windows 7: Click **Start**, type **regedit** in the Start Search box, and then press Enter.</span></span>

    -   <span data-ttu-id="3d224-200">Geben Sie in Windows 8 **Regedit** auf der Start Seite drücken Sie die EINGABETASTE ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="3d224-200">In Windows 8, type **regedit** press Enter on the Start page and then press Enter.</span></span>

    <span data-ttu-id="3d224-201">Wenn Sie zur Eingabe eines Administratorkennworts oder zur Bestätigung aufgefordert werden, geben Sie das Kennwort ein, oder klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3d224-201">If you are prompted for an administrator password or for a confirmation, type the password, or click **Continue**.</span></span>

3.  <span data-ttu-id="3d224-202">Suchen Sie den folgenden Registrierungsunterschlüssel, und wählen Sie ihn aus:</span><span class="sxs-lookup"><span data-stu-id="3d224-202">Locate and then select the following registry subkey:</span></span>

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  <span data-ttu-id="3d224-203">Klicken Sie im Menü **Bearbeiten** auf **neu**, und klicken Sie dann auf **DWORD-Wert**.</span><span class="sxs-lookup"><span data-stu-id="3d224-203">On the **Edit** menu, click **New**, and then click **DWORD Value**.</span></span>

5.  <span data-ttu-id="3d224-204">Geben Sie **NoReReg**ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="3d224-204">Type **NoReReg**, and then press Enter.</span></span>

6.  <span data-ttu-id="3d224-205">Klicken Sie mit der rechten Maustaste auf **NoReReg** , und klicken Sie dann auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="3d224-205">Right-click **NoReReg** and then click **Modify**.</span></span>

7.  <span data-ttu-id="3d224-206">Geben Sie im Feld **Valuedata** **1 ein**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d224-206">In the **Valuedata** box, type **1**, and then click **OK**.</span></span>

8.  <span data-ttu-id="3d224-207">Klicken Sie im Menü Datei auf **Beenden** , um den Registrierungs-Editor zu schließen.</span><span class="sxs-lookup"><span data-stu-id="3d224-207">On the File menu, click **Exit** to close Registry Editor.</span></span>

## <a href="" id="bkmk-office-integration-win"></a><span data-ttu-id="3d224-208">Integration von Office in Windows bei Verwendung von App-V zum Bereitstellen von Office</span><span class="sxs-lookup"><span data-stu-id="3d224-208">How Office integrates with Windows when you use App-V to deploy Office</span></span>


<span data-ttu-id="3d224-209">Wenn Sie Office 2013 mithilfe von App-v bereitstellen, ist Office vollständig in das Betriebssystem integriert, das Endbenutzern dieselben Features und Funktionen wie Office bietet, wenn es ohne APP-v bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3d224-209">When you deploy Office 2013 by using App-V, Office is fully integrated with the operating system, which provides end users with the same features and functionality as Office has when it is deployed without App-V.</span></span>

<span data-ttu-id="3d224-210">Das Office 2013-App-V-Paket unterstützt die folgenden Integrationspunkte mit dem Windows-Betriebssystem:</span><span class="sxs-lookup"><span data-stu-id="3d224-210">The Office 2013 App-V package supports the following integration points with the Windows operating system:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d224-211">Erweiterungspunkt</span><span class="sxs-lookup"><span data-stu-id="3d224-211">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="3d224-212">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d224-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-213">Lync-Besprechungsteilnahme-Plug-in für Firefox und Chrome</span><span class="sxs-lookup"><span data-stu-id="3d224-213">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-214">Benutzer können über Firefox und Chrome an lync-Besprechungen teilnehmen</span><span class="sxs-lookup"><span data-stu-id="3d224-214">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-215">An den OneNote-Druckertreiber gesendet</span><span class="sxs-lookup"><span data-stu-id="3d224-215">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-216">Benutzer kann in OneNote drucken</span><span class="sxs-lookup"><span data-stu-id="3d224-216">User can print to OneNote</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-217">Verknüpfte OneNote-Notizen</span><span class="sxs-lookup"><span data-stu-id="3d224-217">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-218">Verknüpfte OneNote-Notizen</span><span class="sxs-lookup"><span data-stu-id="3d224-218">OneNote Linked Notes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-219">An OneNote Internet Explorer-Add-in senden</span><span class="sxs-lookup"><span data-stu-id="3d224-219">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-220">Benutzer kann von IE an OneNote senden</span><span class="sxs-lookup"><span data-stu-id="3d224-220">User can send to OneNote from IE</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-221">Firewall-Ausnahme für lync und Outlook</span><span class="sxs-lookup"><span data-stu-id="3d224-221">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-222">Firewall-Ausnahme für lync und Outlook</span><span class="sxs-lookup"><span data-stu-id="3d224-222">Firewall Exception for Lync and Outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-223">MAPI-Client</span><span class="sxs-lookup"><span data-stu-id="3d224-223">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-224">Systemeigene apps und Add-Ins können mit Virtual Outlook über MAPI interagieren</span><span class="sxs-lookup"><span data-stu-id="3d224-224">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-225">SharePoint-Plug-in für Firefox</span><span class="sxs-lookup"><span data-stu-id="3d224-225">SharePoint Plug-in for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-226">Benutzer kann SharePoint-Features in Firefox verwenden</span><span class="sxs-lookup"><span data-stu-id="3d224-226">User can use SharePoint features in Firefox</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-227">Applet für Mail-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="3d224-227">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-228">Der Benutzer erhält das Applet für die Mail-Systemsteuerung in Outlook</span><span class="sxs-lookup"><span data-stu-id="3d224-228">User gets the mail control panel applet in Outlook</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-229">Primäre Interop-Assemblys</span><span class="sxs-lookup"><span data-stu-id="3d224-229">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-230">Unterstützung verwalteter Add-ins</span><span class="sxs-lookup"><span data-stu-id="3d224-230">Support managed add-ins</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-231">Cache Handler für Office-Dokumente</span><span class="sxs-lookup"><span data-stu-id="3d224-231">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-232">Ermöglicht den Dokumenten Cache für Office-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3d224-232">Allows Document Cache for Office applications</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-233">Outlook-Protokoll such Handler</span><span class="sxs-lookup"><span data-stu-id="3d224-233">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-234">Benutzer kann in Outlook suchen</span><span class="sxs-lookup"><span data-stu-id="3d224-234">User can search in outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-235">ActiveX-Steuerelemente:</span><span class="sxs-lookup"><span data-stu-id="3d224-235">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-236">Weitere Informationen zu ActiveX-Steuerelementen finden Sie unter <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API-Referenz für ActiveX-Steuerelemente </a> .</span><span class="sxs-lookup"><span data-stu-id="3d224-236">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d224-237">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="3d224-237">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-238">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-238">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d224-239">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="3d224-239">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-240">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-240">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d224-241">SharePoint. OpenDocuments</span><span class="sxs-lookup"><span data-stu-id="3d224-241">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-242">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-242">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d224-243">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="3d224-243">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-244">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-244">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d224-245">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="3d224-245">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-246">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-246">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d224-247">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="3d224-247">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-248">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-248">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d224-249">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="3d224-249">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-250">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-250">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d224-251">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="3d224-251">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-252">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-252">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d224-253">SharePoint. XMLDocuments</span><span class="sxs-lookup"><span data-stu-id="3d224-253">Sharepoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-254">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-254">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d224-255">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="3d224-255">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-256">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-256">Active X control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d224-257">Winproj. Activator</span><span class="sxs-lookup"><span data-stu-id="3d224-257">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-258">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-258">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d224-259">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="3d224-259">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-260">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-260">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d224-261">STSUPld. CopyCtl</span><span class="sxs-lookup"><span data-stu-id="3d224-261">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-262">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-262">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d224-263">CommunicatorMeetingJoinAx. joinmanager</span><span class="sxs-lookup"><span data-stu-id="3d224-263">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-264">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-264">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d224-265">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="3d224-265">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-266">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d224-266">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d224-267">OneDrive pro-Browser-Helfer</span><span class="sxs-lookup"><span data-stu-id="3d224-267">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-268">Active X-Steuerelement]</span><span class="sxs-lookup"><span data-stu-id="3d224-268">Active X Control]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-269">OneDrive pro-symbolüberlagerungen</span><span class="sxs-lookup"><span data-stu-id="3d224-269">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d224-270">Windows Explorer-Shell-Symbol Overlays, wenn Benutzerordner OneDrive pro-Ordner anzeigen</span><span class="sxs-lookup"><span data-stu-id="3d224-270">Windows Explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-271">-Shell-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="3d224-271">Shell extensions</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d224-272">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="3d224-272">Shortcuts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d224-273">Windows Search</span><span class="sxs-lookup"><span data-stu-id="3d224-273">Windows Search</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





