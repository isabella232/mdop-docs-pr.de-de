---
title: Leistungsleitfaden zu Application Virtualization 5.0
description: Leistungsleitfaden zu Application Virtualization 5.0
author: dansimp
ms.assetid: 6b3a3255-b957-4b9b-8bfc-a93fe8438a81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b0f5ef07935fc34adce772e7b2fff85a12b01dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805051"
---
# <span data-ttu-id="095cb-103">Leistungsleitfaden zu Application Virtualization 5.0</span><span class="sxs-lookup"><span data-stu-id="095cb-103">Performance Guidance for Application Virtualization 5.0</span></span>


<span data-ttu-id="095cb-104">Erfahren Sie, wie Sie App-V 5,0 für optimale Leistung konfigurieren, virtuelle App-Pakete optimieren und eine bessere Benutzererfahrung mit RDS und VDI bieten.</span><span class="sxs-lookup"><span data-stu-id="095cb-104">Learn how to configure App-V 5.0 for optimal performance, optimize virtual app packages, and provide a better user experience with RDS and VDI.</span></span>

<span data-ttu-id="095cb-105">Durch die Implementierung mehrerer Methoden können Sie die Benutzerfreundlichkeit verbessern.</span><span class="sxs-lookup"><span data-stu-id="095cb-105">Implementing multiple methods can help you improve the end-user experience.</span></span> <span data-ttu-id="095cb-106">Allerdings unterstützt Ihre Umgebung möglicherweise nicht alle Methoden.</span><span class="sxs-lookup"><span data-stu-id="095cb-106">However, your environment may not support all methods.</span></span>

<span data-ttu-id="095cb-107">Lesen und verstehen Sie die folgenden Informationen, bevor Sie dieses Dokument lesen.</span><span class="sxs-lookup"><span data-stu-id="095cb-107">You should read and understand the following information before reading this document.</span></span>

-   [<span data-ttu-id="095cb-108">Microsoft Application Virtualization 5,0-Administrator Handbuch</span><span class="sxs-lookup"><span data-stu-id="095cb-108">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="095cb-109">App-V 5 SP2-Anwendungsveröffentlichung und Client Interaktion</span><span class="sxs-lookup"><span data-stu-id="095cb-109">App-V 5 SP2 Application Publishing and Client Interaction</span></span>](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [<span data-ttu-id="095cb-110">Microsoft Application Virtualization 5,0-Sequenzierungs Handbuch</span><span class="sxs-lookup"><span data-stu-id="095cb-110">Microsoft Application Virtualization 5.0 Sequencing Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=269953)

**<span data-ttu-id="095cb-111">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="095cb-111">Note</span></span>**  
<span data-ttu-id="095cb-112">Einige in diesem Dokument verwendete Begriffe können je nach externer Quelle und Kontext unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="095cb-112">Some terms used in this document may have different meanings depending on external source and context.</span></span> <span data-ttu-id="095cb-113">Weitere Informationen zu den in diesem Dokument verwendeten Begriffen gefolgt von einem Sternchen **\\** \* finden Sie im Abschnitt " [Application Virtualization-Leistungsleitfaden](#bkmk-terms1) " dieses Dokuments.</span><span class="sxs-lookup"><span data-stu-id="095cb-113">For more information about terms used in this document followed by an asterisk **\\**\* review the [Application Virtualization Performance Guidance Terminology](#bkmk-terms1) section of this document.</span></span>



<span data-ttu-id="095cb-114">Schließlich erhalten Sie in diesem Dokument die Informationen zum Konfigurieren des Computers, auf dem der App-V 5,0-Client und die Umgebung ausgeführt werden, um eine optimale Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="095cb-114">Finally, this document will provide you with the information to configure the computer running App-V 5.0 client and the environment for optimal performance.</span></span> <span data-ttu-id="095cb-115">Optimieren Sie Ihre virtuellen Anwendungspakete für die Leistung mithilfe des Sequencers, und verstehen Sie, wie Sie die Benutzeroberflächen-Virtualisierung (UE-v) oder andere Benutzer Umgebungs Verwaltungstechnologien verwenden können, um die optimale Benutzererfahrung mit App-V 5,0 sowohl in Remote Desktop Diensten (RDS) als auch in nicht persistenter virtueller Desktopinfrastruktur (VDI) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="095cb-115">Optimize your virtual application packages for performance using the sequencer, and to understand how to use User Experience Virtualization (UE-V) or other user environment management technologies to provide the optimal user experience with App-V 5.0 in both Remote Desktop Services (RDS) and non-persistent virtual desktop infrastructure (VDI).</span></span>

<span data-ttu-id="095cb-116">Wenn Sie ermitteln möchten, welche Informationen für Ihre Umgebung relevant sind, sollten Sie die Kurzübersicht und die Anwendungs Checkliste für jeden Abschnitt überprüfen.</span><span class="sxs-lookup"><span data-stu-id="095cb-116">To help determine what information is relevant to your environment you should review each section’s brief overview and applicability checklist.</span></span>

## <a href="" id="---------app-v-5-0-in-stateful--non-persistent-deployments"></a> <span data-ttu-id="095cb-117">App-V 5,0 in Stateful \ \* nicht persistente Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="095cb-117">App-V 5.0 in stateful\* non-persistent deployments</span></span>


<span data-ttu-id="095cb-118">Dieser Abschnitt enthält Informationen zu einem Ansatz, der sicherstellt, dass ein Benutzer innerhalb von Sekunden nach der Anmeldung auf alle virtuellen Anwendungen zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="095cb-118">This section provides information about an approach that helps ensure a user will have access to all virtual applications within seconds after logging in.</span></span> <span data-ttu-id="095cb-119">Dies wird erreicht, indem die häufig lange andauernde App-V 5,0-Veröffentlichungsaktualisierung eindeutig adressiert wird.</span><span class="sxs-lookup"><span data-stu-id="095cb-119">This is achieved by uniquely addressing the often long-running App-V 5.0 publishing refresh.</span></span> <span data-ttu-id="095cb-120">Wie Sie feststellen werden, ist die Grundlage des Ansatzes die schnellste Veröffentlichungsaktualisierung, die nicht wirklich etwas tun muss.</span><span class="sxs-lookup"><span data-stu-id="095cb-120">As you will discover the basis of the approach, the fastest publishing refresh, is one that doesn’t have to actually do anything.</span></span> <span data-ttu-id="095cb-121">Es müssen eine Reihe von Bedingungen erfüllt sein, und es werden Schritte ausgeführt, um die optimale Benutzererfahrung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="095cb-121">A number of conditions must be met and steps followed to provide the optimal user experience.</span></span>

<span data-ttu-id="095cb-122">Verwenden Sie die Informationen im folgenden Abschnitt, um weitere Informationen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="095cb-122">Use the information in the following section for more information:</span></span>

<span data-ttu-id="095cb-123">[Verwendungsszenarien](#bkmk-us) – beachten Sie bei der Überprüfung der beiden Szenarien, dass es sich hierbei um extreme Ansätze handelt.</span><span class="sxs-lookup"><span data-stu-id="095cb-123">[Usage Scenarios](#bkmk-us) - As you review the two scenarios, keep in mind that these are the approach extremes.</span></span> <span data-ttu-id="095cb-124">Basierend auf Ihren Nutzungsanforderungen können Sie diese Schritte auf eine Teilmenge von Benutzern und/oder virtuellen Anwendungspaketen anwenden.</span><span class="sxs-lookup"><span data-stu-id="095cb-124">Based on your usage requirements, you may choose to apply these steps to a subset of users and/or virtual applications packages.</span></span>

-   <span data-ttu-id="095cb-125">Optimiert für die Leistung: um die optimale Benutzerfreundlichkeit zu gewährleisten, können Sie davon ausgehen, dass das Basisabbild einige der virtuellen App-V-Anwendungspakete umfasst.</span><span class="sxs-lookup"><span data-stu-id="095cb-125">Optimized for Performance – To provide the optimal experience, you can expect the base image to include some of the App-V virtual application package.</span></span> <span data-ttu-id="095cb-126">Diese und andere Anforderungen werden besprochen.</span><span class="sxs-lookup"><span data-stu-id="095cb-126">This and other requirements are discussed.</span></span>

-   <span data-ttu-id="095cb-127">Optimiert für den Speicher – wenn Sie sich mit den Auswirkungen auf den Speicher befassen, hilft Ihnen dieses Szenario, diese Probleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="095cb-127">Optimized for Storage – If you are concerned with the storage impact, following this scenario will help address those concerns.</span></span>

[<span data-ttu-id="095cb-128">Vorbereiten Ihrer Umgebung</span><span class="sxs-lookup"><span data-stu-id="095cb-128">Preparing your Environment</span></span>](#bkmk-pe)

-   <span data-ttu-id="095cb-129">Schritte zum Vorbereiten des Basis Bilds – egal, ob es sich um eine nicht persistente VDI-oder RDSH-Umgebung handelt, es müssen nur wenige Schritte im Basisabbild ausgeführt werden, um diesen Ansatz zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="095cb-129">Steps to Prepare the Base Image – Whether in a non-persistent VDI or RDSH environment, only a few steps must be completed in the base image to enable this approach.</span></span>

-   <span data-ttu-id="095cb-130">Verwenden Sie UE-v 2,0 als die Benutzerprofilverwaltung (UPM)-Lösung für den App-v-Ansatz – der Eckpfeiler dieses Ansatzes ist die Fähigkeit einer UEM-Lösung, die Inhalte von nur wenigen Registrierungs-und Dateispeicherorten beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="095cb-130">Use UE-V 2.0 as the User Profile Management (UPM) solution for the App-V approach – the cornerstone of this approach is the ability of a UEM solution to persist the contents of just a few registry and file locations.</span></span> <span data-ttu-id="095cb-131">Diese Speicherorte stellen die Benutzer Integrationen \ \* dar.</span><span class="sxs-lookup"><span data-stu-id="095cb-131">These locations constitute the user integrations\*.</span></span> <span data-ttu-id="095cb-132">Überprüfen Sie unbedingt die spezifischen Anforderungen für die UPM-Lösung.</span><span class="sxs-lookup"><span data-stu-id="095cb-132">Be sure to review the specific requirements for the UPM solution.</span></span>

[<span data-ttu-id="095cb-133">Benutzerfreundlichkeit durchlaufen</span><span class="sxs-lookup"><span data-stu-id="095cb-133">User Experience Walk-through</span></span>](#bkmk-uewt)

-   <span data-ttu-id="095cb-134">Durchlaufen – Dies ist ein Schritt-für-Schritt-durchlaufen der APP-v-und UE-v-Vorgänge und die Erwartungen der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="095cb-134">Walk-through – This is a step-by-step walk-through of the App-V and UE-V operations and the expectations users should have.</span></span>

-   <span data-ttu-id="095cb-135">Ergebnis – Dies beschreibt die erwarteten Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="095cb-135">Outcome – This describes the expected results.</span></span>

[<span data-ttu-id="095cb-136">Auswirkungen auf den Paket Lebenszyklus</span><span class="sxs-lookup"><span data-stu-id="095cb-136">Impact to Package Lifecycle</span></span>](#bkmk-plc)

[<span data-ttu-id="095cb-137">Verbessern der VDI-Erfahrung durch Leistungsoptimierung/-Optimierung</span><span class="sxs-lookup"><span data-stu-id="095cb-137">Enhancing the VDI Experience through Performance Optimization/Tuning</span></span>](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a><span data-ttu-id="095cb-138">Anwendungs Checkliste</span><span class="sxs-lookup"><span data-stu-id="095cb-138">Applicability Checklist</span></span>

<span data-ttu-id="095cb-139">Bereitstellungsumgebung</span><span class="sxs-lookup"><span data-stu-id="095cb-139">Deployment Environment</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="095cb-140">Nicht persistente VDI-oder RDSH.</span><span class="sxs-lookup"><span data-stu-id="095cb-140">Non-Persistent VDI or RDSH.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="095cb-141">Benutzeroberflächen-Virtualisierung (UE-V), andere UPM-Lösungen oder Benutzerprofil Datenträger (UPD).</span><span class="sxs-lookup"><span data-stu-id="095cb-141">User Experience Virtualization (UE-V), other UPM solutions or User Profile Disks (UPD).</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="095cb-142">Erwartete Konfiguration</span><span class="sxs-lookup"><span data-stu-id="095cb-142">Expected Configuration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="095cb-143">Benutzeroberflächen-Virtualisierung (UE-v) mit aktivierter App-v-Benutzerstatus Vorlage oder UPM-Software (User Profile Management).</span><span class="sxs-lookup"><span data-stu-id="095cb-143">User Experience Virtualization (UE-V) with the App-V user state template enabled or User Profile Management (UPM) software.</span></span> <span data-ttu-id="095cb-144">Nicht-UE-V UPM-Software muss bei der Anmeldung oder beim Starten und Abmelden von Prozessen/Anwendungen ausgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="095cb-144">Non-UE-V UPM software must be capable of triggering on Login or Process/Application Start and Logoff.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="095cb-145">App-V Shared Content Store (SCS) ist konfiguriert oder kann konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-145">App-V Shared Content Store (SCS) is configured or can be configured.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="095cb-146">IT-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="095cb-146">IT Administration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="095cb-147">Der Administrator muss möglicherweise das VM-Basisabbild regelmäßig aktualisieren, um eine optimale Leistung zu gewährleisten, oder Administrator muss möglicherweise mehrere Bilder für verschiedene Benutzergruppen verwalten.</span><span class="sxs-lookup"><span data-stu-id="095cb-147">Admin may need to update the VM base image regularly to ensure optimal performance or Admin may need to manage multiple images for different user groups.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a><span data-ttu-id="095cb-148">Verwendungsszenario</span><span class="sxs-lookup"><span data-stu-id="095cb-148">Usage Scenario</span></span>

<span data-ttu-id="095cb-149">Beachten Sie beim Überprüfen der beiden Szenarien, dass diese sich den extremen annähern.</span><span class="sxs-lookup"><span data-stu-id="095cb-149">As you review the two scenarios, keep in mind that these approach the extremes.</span></span> <span data-ttu-id="095cb-150">Basierend auf Ihren Nutzungsanforderungen können Sie diese Schritte auf eine Teilmenge von Benutzern, virtuellen Anwendungspaketen oder beides anwenden.</span><span class="sxs-lookup"><span data-stu-id="095cb-150">Based on your usage requirements, you may choose to apply these steps to a subset of users, virtual application packages, or both.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="095cb-151">Optimiert für die Leistung</span><span class="sxs-lookup"><span data-stu-id="095cb-151">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="095cb-152">Optimiert für den Speicher</span><span class="sxs-lookup"><span data-stu-id="095cb-152">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="095cb-153">Damit die optimale Benutzererfahrung gewährleistet wird, nutzt dieser Ansatz die Funktionen einer UPM-Lösung und erfordert eine zusätzliche Bildvorbereitung und kann einen zusätzlichen Overhead bei der Bildverwaltung verursachen.</span><span class="sxs-lookup"><span data-stu-id="095cb-153">To provide the most optimal user experience, this approach leverages the capabilities of a UPM solution and requires additional image preparation and can incur some additional image management overhead.</span></span></p>
<p><span data-ttu-id="095cb-154">Im folgenden werden viele Leistungsverbesserungen in Stateful-nicht persistenten Bereitstellungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="095cb-154">The following describes many performance improvements in stateful non-persistent deployments.</span></span> <span data-ttu-id="095cb-155">Weitere Informationen finden Sie in den <strong> Schritten zur Sequenzierung, um Pakete für die Veröffentlichungs Leistung zu optimieren, </strong> und verweisen auf <strong> App-V 5,0-Sequenzierungs Handbuch </strong> im <strong> Abschnitt Siehe auch dieses Dokuments </strong> .</span><span class="sxs-lookup"><span data-stu-id="095cb-155">For more information, see the <strong>Sequencing Steps to Optimize Packages for Publishing Performance</strong> and reference to <strong>App-V 5.0 Sequencing Guide</strong> in the <strong>See Also section of this document</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-156">Die allgemeinen Erwartungen des vorherigen Szenarios gelten hier weiterhin.</span><span class="sxs-lookup"><span data-stu-id="095cb-156">The general expectations of the previous scenario still apply here.</span></span> <span data-ttu-id="095cb-157">Beachten Sie jedoch, dass VM-Bilder in der Regel in sehr kostspieligen Arrays gespeichert werden. eine geringfügige Änderung des Ansatzes ist zu verzeichnen.</span><span class="sxs-lookup"><span data-stu-id="095cb-157">However, keep in mind that VM images are typically stored in very costly arrays; a slight alteration has been made to the approach.</span></span> <span data-ttu-id="095cb-158">Verwenden Sie keine vorkonfigurierten benutzerbezogenen virtuellen Anwendungspakete im Basisabbild.</span><span class="sxs-lookup"><span data-stu-id="095cb-158">Do not pre-configure user-targeted virtual application packages in the base image.</span></span></p>
<p><span data-ttu-id="095cb-159">Die Auswirkungen dieser Änderung sind im Abschnitt Benutzeroberflächen-Exemplarische Vorgehensweise dieses Dokuments detailliert beschrieben.</span><span class="sxs-lookup"><span data-stu-id="095cb-159">The impact of this alteration is detailed in the User Experience Walkthrough section of this document.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a><span data-ttu-id="095cb-160">Vorbereiten Ihrer Umgebung</span><span class="sxs-lookup"><span data-stu-id="095cb-160">Preparing your Environment</span></span>

<span data-ttu-id="095cb-161">In der folgenden Tabelle werden die erforderlichen Schritte zum Vorbereiten des Basis Bilds und der UE-V-oder einer anderen UPM-Lösung für den Ansatz angezeigt.</span><span class="sxs-lookup"><span data-stu-id="095cb-161">The following table displays the required steps to prepare the base image and the UE-V or another UPM solution for the approach.</span></span>

**<span data-ttu-id="095cb-162">Vorbereiten des Basis Bilds</span><span class="sxs-lookup"><span data-stu-id="095cb-162">Prepare the Base Image</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="095cb-163">Optimiert für die Leistung</span><span class="sxs-lookup"><span data-stu-id="095cb-163">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="095cb-164">Optimiert für den Speicher</span><span class="sxs-lookup"><span data-stu-id="095cb-164">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="095cb-165">Installieren Sie das Hotfix-Paket 4 für Application Virtualization 5,0 SP2-Client Version des Clients.</span><span class="sxs-lookup"><span data-stu-id="095cb-165">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="095cb-166">Installieren Sie UE-v, und laden Sie die APP-v-Einstellungs Vorlage aus dem UE-v-Vorlagenkatalog herunter, und lesen Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="095cb-166">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="095cb-167">Konfigurieren Sie den Modus für freigegebenen Inhaltsspeicher (SCS).</span><span class="sxs-lookup"><span data-stu-id="095cb-167">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="095cb-168">Weitere Informationen finden Sie unter <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> Installieren des App-V 5,0-Clients für den freigegebenen Inhaltsspeicher Modus </a> .</span><span class="sxs-lookup"><span data-stu-id="095cb-168">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="095cb-169">Konfigurieren Sie die Beibehaltung der Benutzer Integrationen im DWORD-Anmelde Registrierungseintrag.</span><span class="sxs-lookup"><span data-stu-id="095cb-169">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="095cb-170">Konfigurieren Sie alle Benutzer-und Global gezielten Pakete, beispielsweise <strong> Add-AppvClientPackage, vor </strong> .</span><span class="sxs-lookup"><span data-stu-id="095cb-170">Pre-configure all user- and global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="095cb-171">Konfigurieren Sie alle Benutzer-und Global-Zielgruppen für Verbindungen, beispielsweise <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="095cb-171">Pre-configure all user- and global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="095cb-172">Veröffentlichen Sie alle Global-Targeted-Pakete vorab.</span><span class="sxs-lookup"><span data-stu-id="095cb-172">Pre-publish all global-targeted packages.</span></span></p>
<p></p>
<p><span data-ttu-id="095cb-173">Alternativ</span><span class="sxs-lookup"><span data-stu-id="095cb-173">Alternatively,</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-174">Durchführen einer globalen Veröffentlichung/Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="095cb-174">Perform a global publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="095cb-175">Durchführen einer Benutzer Veröffentlichung/-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="095cb-175">Perform a user publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="095cb-176">Alle benutzerbezogenen Pakete nicht veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="095cb-176">Un-publish all user-targeted packages.</span></span></p></li>
<li><p><span data-ttu-id="095cb-177">Löschen Sie die folgenden VFS-Einträge (User-Virtual File System).</span><span class="sxs-lookup"><span data-stu-id="095cb-177">Delete the following user-Virtual File System (VFS) entries.</span></span></p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="095cb-178">Installieren Sie das Hotfix-Paket 4 für Application Virtualization 5,0 SP2-Client Version des Clients.</span><span class="sxs-lookup"><span data-stu-id="095cb-178">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="095cb-179">Installieren Sie UE-v, und laden Sie die APP-v-Einstellungs Vorlage aus dem UE-v-Vorlagenkatalog herunter, und lesen Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="095cb-179">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="095cb-180">Konfigurieren Sie den Modus für freigegebenen Inhaltsspeicher (SCS).</span><span class="sxs-lookup"><span data-stu-id="095cb-180">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="095cb-181">Weitere Informationen finden Sie unter <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> Installieren des App-V 5,0-Clients für den freigegebenen Inhaltsspeicher Modus </a> .</span><span class="sxs-lookup"><span data-stu-id="095cb-181">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="095cb-182">Konfigurieren Sie die Beibehaltung der Benutzer Integrationen im DWORD-Anmelde Registrierungseintrag.</span><span class="sxs-lookup"><span data-stu-id="095cb-182">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="095cb-183">Vorkonfigurieren aller Global gezielten Pakete, beispielsweise <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="095cb-183">Pre-configure all global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="095cb-184">Konfigurieren Sie alle Global-Targeted Connection Groups, beispielsweise <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="095cb-184">Pre-configure all global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="095cb-185">Veröffentlichen Sie alle Global-Targeted-Pakete vorab.</span><span class="sxs-lookup"><span data-stu-id="095cb-185">Pre-publish all global-targeted packages.</span></span></p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="095cb-186">**Konfigurationen** – für kritische App-V-Client Konfigurationen und für ein wenig mehr Kontext und Vorgehensweise überprüfen Sie die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="095cb-186">**Configurations** - For critical App-V Client configurations and for a little more context and how-to, review the following information:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="095cb-187">Konfigurationseinstellung</span><span class="sxs-lookup"><span data-stu-id="095cb-187">Configuration Setting</span></span></th>
<th align="left"><span data-ttu-id="095cb-188">Was bedeutet das?</span><span class="sxs-lookup"><span data-stu-id="095cb-188">What does this do?</span></span></th>
<th align="left"><span data-ttu-id="095cb-189">Wie sollte ich es verwenden?</span><span class="sxs-lookup"><span data-stu-id="095cb-189">How should I use it?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="095cb-190">Modus für freigegebene Inhaltsspeicher (SCS)</span><span class="sxs-lookup"><span data-stu-id="095cb-190">Shared Content Store (SCS) Mode</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-191">Konfigurierbar in PowerShell mithilfe von " <strong> AppvClientConfiguration </strong> – <strong> SharedContentStoreMode" </strong> oder</span><span class="sxs-lookup"><span data-stu-id="095cb-191">Configurable in PowerShell using <strong>Set- AppvClientConfiguration</strong> –<strong>SharedContentStoreMode</strong>, or</span></span></p></li>
<li><p><span data-ttu-id="095cb-192">Während der Installation des App-V 5,0-Clients.</span><span class="sxs-lookup"><span data-stu-id="095cb-192">During installation of the App-V 5.0 client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="095cb-193">Beim Ausführen des freigegebenen Inhaltsspeichers werden nur Veröffentlichungsdaten auf der Festplatte verwaltet. andere Ressourcen der virtuellen Anwendung werden im Arbeitsspeicher (RAM) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="095cb-193">When running the shared content store only publishing data is maintained on hard disk; other virtual application assets are maintained in memory (RAM).</span></span></p>
<p><span data-ttu-id="095cb-194">Auf diese Weise können Sie den lokalen Speicherplatz sparen und die Datenträger-e/a pro Sekunde (IOPS) minimieren.</span><span class="sxs-lookup"><span data-stu-id="095cb-194">This helps to conserve local storage and minimize disk I/O per second (IOPS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-195">Diese Vorgehensweise wird empfohlen, wenn Verbindungen zwischen dem App-V-Client Endpunkt und dem SCS-Inhaltsserver San verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="095cb-195">This is recommended when low-latency connections are available between the App-V Client endpoint and the SCS content server, SAN.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="095cb-196">PreserveUserIntegrationsOnLogin</span><span class="sxs-lookup"><span data-stu-id="095cb-196">PreserveUserIntegrationsOnLogin</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-197">Konfigurieren Sie in der Registrierung unter <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> Software </strong>  \  <strong> </strong>  \  <strong> </strong>  \  <strong> -Client </strong>  \  <strong> Integration </strong> von Microsoft AppV.</span><span class="sxs-lookup"><span data-stu-id="095cb-197">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> \ <strong>Client</strong> \ <strong>Integration</strong>.</span></span></p></li>
<li><p><span data-ttu-id="095cb-198">Erstellen Sie den DWORD <strong> -Wert PreserveUserIntegrationsOnLogin </strong> mit dem Wert <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="095cb-198">Create the DWORD value <strong>PreserveUserIntegrationsOnLogin</strong> with a value of <strong>1</strong>.</span></span></p></li>
<li><p><span data-ttu-id="095cb-199">Starten Sie den App-v-Client Dienst neu, oder starten Sie den Computer mit dem App-v-Client neu.</span><span class="sxs-lookup"><span data-stu-id="095cb-199">Restart the App-V client service or restart the computer running the App-V Client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="095cb-200">Wenn Sie ein bestimmtes Paket nicht vorkonfiguriert haben ( <strong> Add-AppvClientPackage </strong> ) und diese Einstellung nicht konfiguriert ist, wird der App-V-Client \* die beibehaltenen Benutzer Integrationen deintegrieren und dann \* erneut integrieren.</span><span class="sxs-lookup"><span data-stu-id="095cb-200">If you have not pre-configured (<strong>Add-AppvClientPackage</strong>) a specific package and this setting is not configured, the App-V Client will de-integrate\* the persisted user integrations, then re-integrate\*.</span></span></p>
<p><span data-ttu-id="095cb-201">Für jedes Paket, das die oben genannten Bedingungen erfüllt, wird die Arbeit beim Veröffentlichen/Aktualisieren effektiv zweimal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="095cb-201">For every package that meets the above conditions, effectively twice the work will be done during publishing/refresh.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-202">Wenn Sie nicht beabsichtigen, alle verfügbaren Benutzer Pakete im Basisabbild vorab zu konfigurieren, verwenden Sie diese Einstellung.</span><span class="sxs-lookup"><span data-stu-id="095cb-202">If you don’t plan to pre-configure every available user package in the base image, use this setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="095cb-203">MaxConcurrentPublishingRefresh</span><span class="sxs-lookup"><span data-stu-id="095cb-203">MaxConcurrentPublishingRefresh</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-204">Konfigurieren Sie in der Registrierung unter <strong> HKEY_LOCAL_MACHINE </strong> &lt; starke &gt; Software für </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong> &lt; starke &gt; Client </strong>  \  <strong> Veröffentlichung </strong> .</span><span class="sxs-lookup"><span data-stu-id="095cb-204">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> &lt;strong&gt;Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> &lt;strong&gt;Client</strong> \ <strong>Publishing</strong>.</span></span></p></li>
<li><p><span data-ttu-id="095cb-205">Erstellen Sie den DWORD <strong> -Wert MaxConcurrentPublishingrefresh </strong> mit der gewünschten maximalen Anzahl gleichzeitiger Veröffentlichungs Aktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="095cb-205">Create the DWORD value <strong>MaxConcurrentPublishingrefresh</strong> with the desired maximum number of concurrent publishing refreshes.</span></span></p></li>
<li><p><span data-ttu-id="095cb-206">Der App-V-Client Dienst und-Computer müssen nicht neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-206">The App-V client service and computer do not need to be restarted.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="095cb-207">Diese Einstellung bestimmt, wie viele Benutzer gleichzeitig eine Veröffentlichungsaktualisierung/-Synchronisierung durchführen können.</span><span class="sxs-lookup"><span data-stu-id="095cb-207">This setting determines the number of users that can perform a publishing refresh/sync at the same time.</span></span> <span data-ttu-id="095cb-208">Die Standardeinstellung ist "No Limit".</span><span class="sxs-lookup"><span data-stu-id="095cb-208">The default setting is no limit.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-209">Das Begrenzen der Anzahl gleichzeitiger Veröffentlichungs Aktualisierungen verhindert eine übermäßige CPU-Auslastung, die sich auf die Computerleistung auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="095cb-209">Limiting the number of concurrent publishing refreshes prevents excessive CPU usage that could impact computer performance.</span></span> <span data-ttu-id="095cb-210">Dieser Grenzwert wird in einer RDS-Umgebung empfohlen, in der sich mehrere Benutzer gleichzeitig an demselben Computer anmelden und eine Veröffentlichungs Aktualisierungs Synchronisierung durchführen können.</span><span class="sxs-lookup"><span data-stu-id="095cb-210">This limit is recommended in an RDS environment, where multiple users can log in to the same computer at the same time and perform a publishing refresh sync.</span></span></p>
<p><span data-ttu-id="095cb-211">Wenn der Schwellenwert für die gleichzeitige Veröffentlichungsaktualisierung erreicht ist, kann die Zeit, die zum Veröffentlichen neuer Anwendungen erforderlich ist, und für Endbenutzer verfügbar machen, nachdem Sie sich angemeldet haben, eine unbestimmte Zeitspanne dauern.</span><span class="sxs-lookup"><span data-stu-id="095cb-211">If the concurrent publishing refresh threshold is reached, the time required to publish new applications and make them available to end users after they log in could take an indeterminate amount of time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="095cb-212">Konfigurieren der UE-v-Lösung für App-v-Ansatz</span><span class="sxs-lookup"><span data-stu-id="095cb-212">Configure UE-V solution for App-V Approach</span></span>

<span data-ttu-id="095cb-213">Wir empfehlen die Verwendung von Microsoft User Experience Virtualization (UE-V), um Anwendungseinstellungen und Windows-Betriebssystemeinstellungen für einen bestimmten Benutzer zu erfassen und zu zentralisieren.</span><span class="sxs-lookup"><span data-stu-id="095cb-213">We recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="095cb-214">Diese Einstellungen werden dann auf die verschiedenen Computer angewendet, auf die der Benutzer zugreifen kann, einschließlich Desktopcomputern, Laptopcomputern und VDI-Sitzungen (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="095cb-214">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span> <span data-ttu-id="095cb-215">UE-V ist für RDS-und VDI-Szenarien optimiert.</span><span class="sxs-lookup"><span data-stu-id="095cb-215">UE-V is optimized for RDS and VDI scenarios.</span></span>

<span data-ttu-id="095cb-216">Weitere Informationen finden Sie unter [Erste Schritte mit der User Experience Virtualization 2,0](https://technet.microsoft.com/library/dn458936.aspx)</span><span class="sxs-lookup"><span data-stu-id="095cb-216">For more information see [Getting Started With User Experience Virtualization 2.0](https://technet.microsoft.com/library/dn458936.aspx)</span></span>

<span data-ttu-id="095cb-217">Im Wesentlichen müssen Sie lediglich den UE-v-Client installieren und die folgende von Microsoft erstellte App-v-Einstellungs Vorlage aus dem [Vorlagenkatalog für Microsoft User Experience Virtualization (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="095cb-217">In essence all that is required is to install the UE-V client and download the following Microsoft authored App-V settings template from the [Microsoft User Experience Virtualization (UE-V) template gallery](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span></span> <span data-ttu-id="095cb-218">Registrieren Sie die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="095cb-218">Register the template.</span></span> <span data-ttu-id="095cb-219">Weitere Informationen zu UE-v-Vorlagen finden Sie in [der UE-v-spezifischen Ressource für den Erwerb und die Registrierung der Vorlage](https://technet.microsoft.com/library/dn458936.aspx).</span><span class="sxs-lookup"><span data-stu-id="095cb-219">For more information around UE-V templates see [The UE-V specific resource for acquiring and registering the template](https://technet.microsoft.com/library/dn458936.aspx).</span></span>

**<span data-ttu-id="095cb-220">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="095cb-220">Note</span></span>**  
<span data-ttu-id="095cb-221">Ohne einen zusätzlichen Konfigurationsschritt zu durchführen, kann die Microsoft-Benutzer Umgebungs-Virtualisierung (UE-V) die Start Menüverknüpfungen (LNK-Dateien) auf dem Zielcomputer nicht synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="095cb-221">Without performing an additional configuration step, the Microsoft User Environment Virtualization (UE-V) will not be able to synchronize the Start menu shortcuts (.lnk files) on the target computer.</span></span> <span data-ttu-id="095cb-222">Der lnk-Dateityp ist standardmäßig ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="095cb-222">The .lnk file type is excluded by default.</span></span>

<span data-ttu-id="095cb-223">UE-V unterstützt nur das Entfernen des lnk-Dateityps aus der Ausschlussliste in den RDS-und VDI-Szenarien, in denen auf dem Gerät jedes Benutzers dieselbe Gruppe von Anwendungen am gleichen Speicherort installiert ist und jede LNK-Datei für alle Geräte der Benutzer gültig ist.</span><span class="sxs-lookup"><span data-stu-id="095cb-223">UE-V will only support removing the .lnk file type from the exclusion list in the RDS and VDI scenarios, where every user’s device will have the same set of applications installed to the same location and every .lnk file is valid for all the users’ devices.</span></span> <span data-ttu-id="095cb-224">UE-V unterstützt beispielsweise derzeit nicht die folgenden 2 Szenarien, da das Ergebnis darin besteht, dass die Verknüpfung auf einem, aber nicht auf allen Geräten gültig ist.</span><span class="sxs-lookup"><span data-stu-id="095cb-224">For example, UE-V would not currently support the following 2 scenarios, because the net result will be that the shortcut will be valid on one but not all devices.</span></span>

-   <span data-ttu-id="095cb-225">Wenn ein Benutzer auf einem Gerät eine Anwendung installiert hat, deren LNK-Dateien aktiviert sind, und die gleiche systemeigene Anwendung auf einem anderen Gerät auf einem anderen Installations Stamm installiert ist und die LNK-Dateien aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="095cb-225">If a user has an application installed on one device with .lnk files enabled and the same native application installed on another device to a different installation root with .lnk files enabled.</span></span>

-   <span data-ttu-id="095cb-226">Wenn ein Benutzer eine Anwendung auf einem Gerät installiert hat, aber nicht eine andere, wenn LNK-Dateien aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="095cb-226">If a user has an application installed on one device but not another with .lnk files enabled.</span></span>



**<span data-ttu-id="095cb-227">Wichtig</span><span class="sxs-lookup"><span data-stu-id="095cb-227">Important</span></span>**  
<span data-ttu-id="095cb-228">In diesem Thema wird beschrieben, wie Sie die Windows-Registrierung mit dem Registrierungs-Editor ändern.</span><span class="sxs-lookup"><span data-stu-id="095cb-228">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="095cb-229">Wenn Sie die Windows-Registrierung falsch ändern, können Sie zu schwerwiegenden Problemen führen, bei denen Sie möglicherweise eine Neuinstallation von Windows erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="095cb-229">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="095cb-230">Bevor Sie die Registrierung ändern, sollten Sie eine Sicherungskopie der Registrierungsdateien (System. dat und User. dat) erstellen.</span><span class="sxs-lookup"><span data-stu-id="095cb-230">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="095cb-231">Microsoft kann nicht garantieren, dass die Probleme, die beim Ändern der Registrierung auftreten, behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="095cb-231">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="095cb-232">Ändern Sie die Registrierung auf Ihr eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="095cb-232">Change the registry at your own risk.</span></span>



<span data-ttu-id="095cb-233">Navigieren Sie mithilfe des Microsoft Registry-Editors (regedit.exe) zu **HKEY \ _LOCAL \ _MACHINE**  \\  **Software**  \\  **Microsoft**  \\  **UEV**  \\  **Agent**  \\  **Configuration**  \\  **ExcludedFileTypes** , und entfernen Sie **lnk** aus den ausgeschlossenen Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="095cb-233">Using the Microsoft Registry Editor (regedit.exe), navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **UEV** \\ **Agent** \\ **Configuration** \\ **ExcludedFileTypes** and remove **.lnk** from the excluded file types.</span></span>

**<span data-ttu-id="095cb-234">Konfigurieren einer anderen UPM-Lösung (User Profile Management) für App-V-Ansatz</span><span class="sxs-lookup"><span data-stu-id="095cb-234">Configure other User Profile Management (UPM) solution for App-V Approach</span></span>**

<span data-ttu-id="095cb-235">Die Erwartung in einer statusbehafteten Umgebung besteht darin, dass eine UPM-Lösung implementiert ist und die Persistenz von Benutzerdaten zwischen Sitzungen und zwischen Anmeldungen unterstützenkann.</span><span class="sxs-lookup"><span data-stu-id="095cb-235">The expectation in a stateful environment is that a UPM solution is implemented and can support persistence of user data across sessions and between logins.</span></span>

<span data-ttu-id="095cb-236">Die Anforderungen für die UPM-Lösung lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="095cb-236">The requirements for the UPM solution are as follows.</span></span>

<span data-ttu-id="095cb-237">Um eine optimierte Anmeldungs Erfahrung zu ermöglichen, beispielsweise den App-V 5,0-Ansatz für den Benutzer, muss die Lösung in der Lage sein:</span><span class="sxs-lookup"><span data-stu-id="095cb-237">To enable an optimized login experience, for example the App-V 5.0 approach for the user, the solution must be capable of:</span></span>

-   <span data-ttu-id="095cb-238">Beibehalten der folgenden Benutzer Integrationen als Teil des Benutzerprofils/der Benutzerrolle</span><span class="sxs-lookup"><span data-stu-id="095cb-238">Persisting the below user integrations as part of the user profile/persona.</span></span>

-   <span data-ttu-id="095cb-239">Auslösen einer Benutzerprofil Synchronisierung bei der Anmeldung (oder Anwendungsstart), die gewährleisten kann, dass alle Benutzer Integrationen vor der Veröffentlichung/Aktualisierung angewendet werden, oder</span><span class="sxs-lookup"><span data-stu-id="095cb-239">Triggering a user profile sync on login (or application start), which can guarantee that all user integrations are applied before publishing/refresh begin, or,</span></span>

-   <span data-ttu-id="095cb-240">Anfügen und Trennen eines Benutzerprofil Datenträgers (UPD) oder einer ähnlichen Technologie, die die Benutzer Integrationen enthält.</span><span class="sxs-lookup"><span data-stu-id="095cb-240">Attaching and detaching a user profile disk (UPD) or similar technology that contains the user integrations.</span></span>

-   <span data-ttu-id="095cb-241">Erfassen von Änderungen an den Speicherorten, die die Benutzer Integrationen darstellen, bevor Sie die Sitzung abmelden.</span><span class="sxs-lookup"><span data-stu-id="095cb-241">Capturing changes to the locations, which constitute the user integrations, prior to session logoff.</span></span>

<span data-ttu-id="095cb-242">Mit App-V 5,0, wenn Sie einen Veröffentlichungsserver (**Add-AppvPublishingServer**) hinzufügen, können Sie die Synchronisierung konfigurieren, beispielsweise beim Aktualisieren während der Anmeldung und/oder nach einem angegebenen Aktualisierungsintervall.</span><span class="sxs-lookup"><span data-stu-id="095cb-242">With App-V 5.0 when you add a publishing server (**Add-AppvPublishingServer**) you can configure synchronization, for example refresh during log on and/or after a specified refresh interval.</span></span> <span data-ttu-id="095cb-243">In beiden Fällen wird eine geplante Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="095cb-243">In both cases a scheduled task is created.</span></span>

<span data-ttu-id="095cb-244">In früheren Versionen von App-V 5,0 wurden beide geplanten Aufgaben mit einem VBScript konfiguriert, das den Benutzer und die globale Aktualisierung initiiert.</span><span class="sxs-lookup"><span data-stu-id="095cb-244">In previous versions of App-V 5.0, both scheduled tasks were configured using a VBScript that would initiate the user and global refresh.</span></span> <span data-ttu-id="095cb-245">Mit dem Hotfix-Paket 4 für Application Virtualization 5,0 SP2 wird die Benutzeraktualisierung bei der Anmeldung von **SyncAppvPublishingServer.exe**initiiert.</span><span class="sxs-lookup"><span data-stu-id="095cb-245">With Hotfix Package 4 for Application Virtualization 5.0 SP2 the user refresh on log on is initiated by **SyncAppvPublishingServer.exe**.</span></span> <span data-ttu-id="095cb-246">Diese Änderung wurde eingeführt, um UPM-Lösungen einen triggerprozess zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="095cb-246">This change was introduced to provide UPM solutions a trigger process.</span></span> <span data-ttu-id="095cb-247">Dieser Vorgang verzögert die Veröffentlichungs-/Refresh, damit die UPM-Lösung die Benutzer Integrationen anwenden kann.</span><span class="sxs-lookup"><span data-stu-id="095cb-247">This process will delay the publish /refresh to allow the UPM solution to apply the user integrations.</span></span> <span data-ttu-id="095cb-248">Sobald die Veröffentlichung/Aktualisierung abgeschlossen ist, wird Sie beendet.</span><span class="sxs-lookup"><span data-stu-id="095cb-248">It will exit once the publishing/refresh is complete.</span></span>

**<span data-ttu-id="095cb-249">Benutzer Integrationen</span><span class="sxs-lookup"><span data-stu-id="095cb-249">User Integrations</span></span>**

<span data-ttu-id="095cb-250">Registrierung – HKEY \ _CURRENT \ _User</span><span class="sxs-lookup"><span data-stu-id="095cb-250">Registry – HKEY\_CURRENT\_USER</span></span>

-   <span data-ttu-id="095cb-251">Path-Software\\Classes</span><span class="sxs-lookup"><span data-stu-id="095cb-251">Path - Software\\Classes</span></span>

    <span data-ttu-id="095cb-252">Ausschließen: lokale Einstellungen, ActivatableClasses, AppX \ \*</span><span class="sxs-lookup"><span data-stu-id="095cb-252">Exclude: Local Settings, ActivatableClasses, AppX\*</span></span>

-   <span data-ttu-id="095cb-253">Path-Software\\Microsoft\\AppV</span><span class="sxs-lookup"><span data-stu-id="095cb-253">Path - Software\\Microsoft\\AppV</span></span>

-   <span data-ttu-id="095cb-254">Path-Software\\Microsoft\\Windows\\CurrentVersion\\App-Pfade</span><span class="sxs-lookup"><span data-stu-id="095cb-254">Path- Software\\Microsoft\\Windows\\CurrentVersion\\App Paths</span></span>

**<span data-ttu-id="095cb-255">Dateispeicherorte</span><span class="sxs-lookup"><span data-stu-id="095cb-255">File Locations</span></span>**

-   <span data-ttu-id="095cb-256">Root – "Umgebungs Variable" APPDATA</span><span class="sxs-lookup"><span data-stu-id="095cb-256">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="095cb-257">Path – Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="095cb-257">Path – Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="095cb-258">Root – "Umgebungs Variable" APPDATA</span><span class="sxs-lookup"><span data-stu-id="095cb-258">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="095cb-259">Path – Microsoft\\AppV\\Client\\Integration</span><span class="sxs-lookup"><span data-stu-id="095cb-259">Path – Microsoft\\AppV\\Client\\Integration</span></span>

-   <span data-ttu-id="095cb-260">Root – "Umgebungs Variable" APPDATA</span><span class="sxs-lookup"><span data-stu-id="095cb-260">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="095cb-261">Path-Microsoft\\Windows\\Start Menu\\Programs</span><span class="sxs-lookup"><span data-stu-id="095cb-261">Path - Microsoft\\Windows\\Start Menu\\Programs</span></span>

-   <span data-ttu-id="095cb-262">(Zum Beibehalten aller Desktopverknüpfungen, virtuell und nicht virtuell)</span><span class="sxs-lookup"><span data-stu-id="095cb-262">(To persist all desktop shortcuts, virtual and non-virtual)</span></span>

    <span data-ttu-id="095cb-263">Root-"KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} filemask-\ \*. lnk</span><span class="sxs-lookup"><span data-stu-id="095cb-263">Root - “KnownFolder” {B4BFCC3A-DB2C-424C-B029-7FE99A87C641}FileMask - \*.lnk</span></span>

**<span data-ttu-id="095cb-264">Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="095cb-264">Microsoft User Experience Virtualization (UE-V)</span></span>**

<span data-ttu-id="095cb-265">Darüber hinaus empfehlen wir die Verwendung von Microsoft User Experience Virtualization (UE-V), um Anwendungseinstellungen und Windows-Betriebssystemeinstellungen für einen bestimmten Benutzer zu erfassen und zu zentralisieren.</span><span class="sxs-lookup"><span data-stu-id="095cb-265">Additionally, we recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="095cb-266">Diese Einstellungen werden dann auf die verschiedenen Computer angewendet, auf die der Benutzer zugreifen kann, einschließlich Desktopcomputern, Laptopcomputern und VDI-Sitzungen (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="095cb-266">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="095cb-267">Weitere Informationen finden Sie unter [Erste Schritte mit Benutzeroberflächen-Virtualisierungs-1,0](https://technet.microsoft.com/library/jj680015.aspx) und [Speicherort Vorlagen für Freigabeeinstellungen mit dem UE-V-Vorlagenkatalog](https://technet.microsoft.com/library/jj679972.aspx).</span><span class="sxs-lookup"><span data-stu-id="095cb-267">For more information see [Getting Started With User Experience Virtualization 1.0](https://technet.microsoft.com/library/jj680015.aspx) and [Sharing Settings Location Templates with the UE-V Template Gallery](https://technet.microsoft.com/library/jj679972.aspx).</span></span>

### <a href="" id="bkmk-uewt"></a><span data-ttu-id="095cb-268">Benutzerfreundlichkeit durchlaufen</span><span class="sxs-lookup"><span data-stu-id="095cb-268">User Experience Walk-through</span></span>

<span data-ttu-id="095cb-269">Im folgenden finden Sie eine schrittweise Einführung in die App-V-und UPM-Vorgänge und die Erwartungen, die Benutzer erwarten sollten.</span><span class="sxs-lookup"><span data-stu-id="095cb-269">This following is a step-by-step walk-through of the App-V and UPM operations and the expectations users should expect.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="095cb-270">Optimiert für die Leistung</span><span class="sxs-lookup"><span data-stu-id="095cb-270">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="095cb-271">Optimiert für den Speicher</span><span class="sxs-lookup"><span data-stu-id="095cb-271">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="095cb-272">Nach der Implementierung dieses Ansatzes in der VDI/RDSH-Umgebung bei der ersten Anmeldung</span><span class="sxs-lookup"><span data-stu-id="095cb-272">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-273">Vorgang Eine Benutzer Veröffentlichung/-Aktualisierung wird initiiert.</span><span class="sxs-lookup"><span data-stu-id="095cb-273">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="095cb-274">Erwartung Wenn ein Benutzer zum ersten Mal virtuelle Anwendungen (beispielsweise nicht persistent) veröffentlicht hat, wird die übliche Dauer einer Veröffentlichung/Aktualisierung übernommen.</span><span class="sxs-lookup"><span data-stu-id="095cb-274">(Expectation) If this is the first time a user has published virtual applications (e.g. non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="095cb-275">Vorgang Nach dem Veröffentlichen/Aktualisieren erfasst die UPM-Lösung die Benutzer Integrationen.</span><span class="sxs-lookup"><span data-stu-id="095cb-275">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="095cb-276">Erwartung Je nachdem, wie die UPM-Lösung konfiguriert ist, kann dies im Rahmen des Abmelde Prozesses erfolgen.</span><span class="sxs-lookup"><span data-stu-id="095cb-276">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="095cb-277">Dies führt zu demselben/ähnlichen Overhead wie das Beibehalten des Benutzerzustands.</span><span class="sxs-lookup"><span data-stu-id="095cb-277">This will incur the same/similar overhead as persisting the user state.</span></span></p></li>
</ul>
<p><span data-ttu-id="095cb-278">Bei nachfolgenden Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="095cb-278">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-279">Vorgang Die UPM-Lösung wendet die Benutzer Integrationen vor der Veröffentlichung/Aktualisierung auf das System an.</span><span class="sxs-lookup"><span data-stu-id="095cb-279">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p>
<p><span data-ttu-id="095cb-280">Erwartung Es werden Tastenkombinationen auf dem Desktop oder im Startmenü angezeigt, die sofort funktionieren.</span><span class="sxs-lookup"><span data-stu-id="095cb-280">(Expectation) There will be shortcuts present on the desktop, or in the start menu, which work immediately.</span></span> <span data-ttu-id="095cb-281">Wenn das Veröffentlichen/Aktualisieren abgeschlossen wird (d. h., dass Paket Ansprüche geändert werden), können einige davon verschwinden.</span><span class="sxs-lookup"><span data-stu-id="095cb-281">When the publishing/refresh completes (i.e., package entitlements change), some may go away.</span></span></p></li>
<li><p><span data-ttu-id="095cb-282">Vorgang Beim Veröffentlichen/Aktualisieren werden Vorgänge zum Veröffentlichen und Veröffentlichen von Änderungen der Benutzerpaket Berechtigungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="095cb-282">(Operation) Publishing/refresh will process un-publish and publish operations for changes in user package entitlements.</span></span> <span data-ttu-id="095cb-283">Erwartung Wenn keine Berechtigungsänderungen vorhanden sind, wird publishing1 in Sekunden abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="095cb-283">(Expectation) If there are no entitlement changes, publishing1 will complete in seconds.</span></span> <span data-ttu-id="095cb-284">Andernfalls wird die Veröffentlichung/Aktualisierung relativ zur Anzahl und Komplexität \* von virtuellen Anwendungen zunehmen.</span><span class="sxs-lookup"><span data-stu-id="095cb-284">Otherwise, the publishing/refresh will increase relative to the number and complexity\* of virtual applications</span></span></p></li>
<li><p><span data-ttu-id="095cb-285">Vorgang Die UPM-Lösung erfasst die Benutzer Integrationen bei der Abmeldung erneut.</span><span class="sxs-lookup"><span data-stu-id="095cb-285">(Operation) UPM solution will capture user integrations again at logoff.</span></span> <span data-ttu-id="095cb-286">Erwartung Wie vorherige.</span><span class="sxs-lookup"><span data-stu-id="095cb-286">(Expectation) Same as previous.</span></span></p></li>
</ul>
<p><span data-ttu-id="095cb-287">¹ der Veröffentlichungsvorgang ( <strong> Publish-AppVClientPackage </strong> ) fügt dem Benutzer Katalogeinträge hinzu, ordnet dem Benutzer den Anspruch zu, identifiziert den lokalen Store und beendet die einzelnen Integrationsschritte.</span><span class="sxs-lookup"><span data-stu-id="095cb-287">¹ The publishing operation (<strong>Publish-AppVClientPackage</strong>) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-288">Nach der Implementierung dieses Ansatzes in der VDI/RDSH-Umgebung bei der ersten Anmeldung</span><span class="sxs-lookup"><span data-stu-id="095cb-288">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-289">Vorgang Eine Benutzer Veröffentlichung/-Aktualisierung wird initiiert.</span><span class="sxs-lookup"><span data-stu-id="095cb-289">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="095cb-290">Erwartung</span><span class="sxs-lookup"><span data-stu-id="095cb-290">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-291">Wenn ein Benutzer zum ersten Mal virtuelle Anwendungen (z. b. nicht persistent) veröffentlicht hat, wird die übliche Dauer einer Veröffentlichung/Aktualisierung übernommen.</span><span class="sxs-lookup"><span data-stu-id="095cb-291">If this is the first time a user has published virtual applications (e.g., non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="095cb-292">Die ersten und nachfolgenden Anmeldungen werden durch die Vorkonfiguration von Paketen (hinzufügen/aktualisieren) beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="095cb-292">First and subsequent logins will be impacted by pre-configuring of packages (add/refresh).</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="095cb-293">Vorgang Nach dem Veröffentlichen/Aktualisieren erfasst die UPM-Lösung die Benutzer Integrationen.</span><span class="sxs-lookup"><span data-stu-id="095cb-293">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="095cb-294">Erwartung Je nachdem, wie die UPM-Lösung konfiguriert ist, kann dies im Rahmen des Abmelde Prozesses erfolgen.</span><span class="sxs-lookup"><span data-stu-id="095cb-294">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="095cb-295">Dies führt zu demselben/ähnlichen Overhead wie das Beibehalten des Benutzerzustands.</span><span class="sxs-lookup"><span data-stu-id="095cb-295">This will incur the same/similar overhead as persisting the user state</span></span></p></li>
</ul>
<p><span data-ttu-id="095cb-296">Bei nachfolgenden Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="095cb-296">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-297">Vorgang Die UPM-Lösung wendet die Benutzer Integrationen vor der Veröffentlichung/Aktualisierung auf das System an.</span><span class="sxs-lookup"><span data-stu-id="095cb-297">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="095cb-298">Vorgang "Hinzufügen/aktualisieren" muss alle benutzerspezifischen Anwendungen vorab konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="095cb-298">(Operation) Add/refresh must pre-configure all user targeted applications.</span></span> <span data-ttu-id="095cb-299">Erwartung</span><span class="sxs-lookup"><span data-stu-id="095cb-299">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-300">Dadurch kann die Verfügbarkeit der Anwendung deutlich verkürzt werden (in der Reihenfolge von 10 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="095cb-300">This may increase the time to application availability significantly (on the order of 10’s of seconds).</span></span></p></li>
<li><p><span data-ttu-id="095cb-301">Dadurch wird die Veröffentlichungs Aktualisierungszeit relativ zur Anzahl und Komplexität \* von virtuellen Anwendungen erhöht.</span><span class="sxs-lookup"><span data-stu-id="095cb-301">This will increase the publishing refresh time relative to the number and complexity\* of virtual applications.</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="095cb-302">Vorgang Beim Veröffentlichen/Aktualisieren werden Vorgänge zum Veröffentlichen und Veröffentlichen von Änderungen an Benutzerpaket Berechtigungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="095cb-302">(Operation) Publishing/refresh will process un-publish and publish operations for changes to user package entitlements.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="095cb-303">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="095cb-303">Outcome</span></span></th>
<th align="left"><span data-ttu-id="095cb-304">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="095cb-304">Outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="095cb-305">Da die Benutzer Integrationen vollständig erhalten sind, wird es keine Arbeit geben, beispielsweise die Integration, um die Veröffentlichung/Aktualisierung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="095cb-305">Because the user integrations are entirely preserved, there will be no work for example, integration for the publishing/refresh to complete.</span></span> <span data-ttu-id="095cb-306">Alle virtuellen Anwendungen werden innerhalb von Sekunden nach der Anmeldung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="095cb-306">All virtual applications will be available within seconds of login.</span></span></p></li>
<li><p><span data-ttu-id="095cb-307">Beim Veröffentlichen/Aktualisieren werden Änderungen an den Benutzern mit dem Titel "virtuelle Anwendungen" verarbeitet, die sich auf die Benutzeroberfläche auswirken.</span><span class="sxs-lookup"><span data-stu-id="095cb-307">The publishing/refresh will process changes to the users entitled virtual applications which impacts the experience.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="095cb-308">Da die Add/Refresh-Konfiguration alle virtuellen Anwendungen auf dem virtuellen Computer neu konfigurieren muss, wird die Veröffentlichungs Aktualisierungszeit bei jeder Anmeldung verlängert.</span><span class="sxs-lookup"><span data-stu-id="095cb-308">Because the add/refresh must re-configure all the virtual applications to the VM, the publishing refresh time on every login will be extended.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a><span data-ttu-id="095cb-309">Auswirkungen auf den Paket Lebenszyklus</span><span class="sxs-lookup"><span data-stu-id="095cb-309">Impact to Package Life Cycle</span></span>

<span data-ttu-id="095cb-310">Das Upgrade eines Pakets ist ein entscheidender Aspekt des Paket Lebenszyklus.</span><span class="sxs-lookup"><span data-stu-id="095cb-310">Upgrading a package is a crucial aspect of the package lifecycle.</span></span> <span data-ttu-id="095cb-311">Wenn Sie sicherstellen möchten, dass Benutzer Zugriff auf die entsprechenden aktualisierten (veröffentlichten) oder herabgestuften (nicht veröffentlichten) virtuellen Anwendungspakete haben, empfiehlt es sich, das Basis Bild so zu aktualisieren, dass diese Änderungen wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-311">To help guarantee users have access to the appropriate upgraded (published) or downgraded (un-published) virtual application packages, it is recommended you update the base image to reflect these changes.</span></span> <span data-ttu-id="095cb-312">Erläutern Sie, warum der folgende Abschnitt überprüft werden sollte:</span><span class="sxs-lookup"><span data-stu-id="095cb-312">To understand why review the following section:</span></span>

<span data-ttu-id="095cb-313">App-V 5,0 SP2 hat das Konzept der ausstehenden Zustände eingeführt.</span><span class="sxs-lookup"><span data-stu-id="095cb-313">App-V 5.0 SP2 introduced the concept of pending states.</span></span> <span data-ttu-id="095cb-314">In der Vergangenheit</span><span class="sxs-lookup"><span data-stu-id="095cb-314">In the past,</span></span>

-   <span data-ttu-id="095cb-315">Wenn ein Administrator die Berechtigungen geändert oder eine neue Version eines Pakets erstellt (aktualisiert) hat und während einer Veröffentlichung/Aktualisierung dieses Paket in Verwendung war, schlägt der Vorgang zum Veröffentlichen oder veröffentlichen fehl.</span><span class="sxs-lookup"><span data-stu-id="095cb-315">If an administrator changed entitlements or created a new version of a package (upgraded) and during a publishing/refresh that package was in-use, the un-publish or publish operation, respectively, would fail.</span></span>

-   <span data-ttu-id="095cb-316">Wenn nun ein Paket in Verwendung ist, wird der Vorgang vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="095cb-316">Now, if a package is in-use the operation will be pended.</span></span> <span data-ttu-id="095cb-317">Die Vorgänge für die Veröffentlichung und Veröffentlichung werden beim Neustart des Diensts verarbeitet, oder es wird ein anderer Befehl zum Veröffentlichen oder deinstallieren veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="095cb-317">The un-publish and publish-pend operations will be processed on service restart or if another publish or un-publish command is issued.</span></span> <span data-ttu-id="095cb-318">Im letzteren Fall verbleibt die virtuelle Anwendung in einem ausstehenden Zustand, wenn die virtuelle Anwendung anderweitig verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="095cb-318">In the latter case, if the virtual application is in-use otherwise, the virtual application will remain in a pending state.</span></span> <span data-ttu-id="095cb-319">Für Global veröffentlichte Pakete wird häufig ein Neustart (oder ein Dienstneustart) benötigt.</span><span class="sxs-lookup"><span data-stu-id="095cb-319">For globally published packages, a restart (or service restart) often needed.</span></span>

<span data-ttu-id="095cb-320">In einer nicht persistenten Umgebung ist es unwahrscheinlich, dass diese vorangestellt-Vorgänge verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-320">In a non-persistent environment, it is unlikely these pended operations will be processed.</span></span> <span data-ttu-id="095cb-321">Die vorangestellt-Vorgänge, beispielsweise Aufgaben, werden unter **HKEY \ _CURRENT \ _User**  \\  **Software**  \\  **Microsoft**  \\  **AppV**  \\  **Client**  \\  **PendingTasks**erfasst.</span><span class="sxs-lookup"><span data-stu-id="095cb-321">The pended operations, for example tasks are captured under **HKEY\_CURRENT\_USER** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **PendingTasks**.</span></span> <span data-ttu-id="095cb-322">Obwohl dieser Speicherort von der UPM-Lösung beibehalten wird, wird er nicht verarbeitet, wenn er vor der Anmeldung nicht auf die Umgebung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="095cb-322">Although this location is persisted by the UPM solution, if it is not applied to the environment prior to log on, it will not be processed.</span></span>

### <a href="" id="bkmk-evdi"></a><span data-ttu-id="095cb-323">Verbessern der VDI-Erfahrung durch Optimierung der Leistungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="095cb-323">Enhancing the VDI Experience through Performance Optimization Tuning</span></span>

<span data-ttu-id="095cb-324">Der folgende Abschnitt enthält Listen mit Informationen zur Microsoft-Dokumentation und Downloads, die bei der Optimierung Ihrer Umgebung für die Leistung hilfreich sein können.</span><span class="sxs-lookup"><span data-stu-id="095cb-324">The following section contains lists with information about Microsoft documentation and downloads that may be useful when optimizing your environment for performance.</span></span>

**<span data-ttu-id="095cb-325">.Net ngen-Blog und-Skript (dringend empfohlen)</span><span class="sxs-lookup"><span data-stu-id="095cb-325">.NET NGEN Blog and Script (Highly Recommended)</span></span>**

<span data-ttu-id="095cb-326">Informationen zu ngen-Technologien</span><span class="sxs-lookup"><span data-stu-id="095cb-326">About NGEN technology</span></span>

-   [<span data-ttu-id="095cb-327">So beschleunigen Sie die ngen-Optimierung</span><span class="sxs-lookup"><span data-stu-id="095cb-327">How to speed up NGEN optimization</span></span>](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [<span data-ttu-id="095cb-328">Skript</span><span class="sxs-lookup"><span data-stu-id="095cb-328">Script</span></span>](https://aka.ms/DrainNGenQueue)

**<span data-ttu-id="095cb-329">Windows Server-und Serverrollen</span><span class="sxs-lookup"><span data-stu-id="095cb-329">Windows Server and Server Roles</span></span>**

<span data-ttu-id="095cb-330">Richtlinien zur Server Leistungsoptimierung für</span><span class="sxs-lookup"><span data-stu-id="095cb-330">Server Performance Tuning Guidelines for</span></span>

-   [<span data-ttu-id="095cb-331">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="095cb-331">Microsoft Windows Server 2012 R2</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [<span data-ttu-id="095cb-332">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="095cb-332">Microsoft Windows Server 2012</span></span>](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [<span data-ttu-id="095cb-333">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="095cb-333">Microsoft Windows Server 2008 R2</span></span>](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**<span data-ttu-id="095cb-334">Server Rollen</span><span class="sxs-lookup"><span data-stu-id="095cb-334">Server Roles</span></span>**

-   [<span data-ttu-id="095cb-335">Host für Remote Desktop-Virtualisierung</span><span class="sxs-lookup"><span data-stu-id="095cb-335">Remote Desktop Virtualization Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [<span data-ttu-id="095cb-336">Host für Remote Desktop Sitzungen</span><span class="sxs-lookup"><span data-stu-id="095cb-336">Remote Desktop Session Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [<span data-ttu-id="095cb-337">IIS-Relevanz: App-V-Verwaltung, Veröffentlichung, Reporting-Webdienste</span><span class="sxs-lookup"><span data-stu-id="095cb-337">IIS Relevance: App-V Management, Publishing, Reporting Web Services</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [<span data-ttu-id="095cb-338">Relevanz für Datei Server (SMB): bei Verwendung für App-V Content-Speicherung und-Zustellung im SCS-Modus</span><span class="sxs-lookup"><span data-stu-id="095cb-338">File Server (SMB) Relevance: If used for App-V Content Storage and Delivery in SCS Mode</span></span>](https://technet.microsoft.com/library/jj134210.aspx)

**<span data-ttu-id="095cb-339">Leitfaden zur Leistungsoptimierung für Windows-Clients (Gastbetriebssystem)</span><span class="sxs-lookup"><span data-stu-id="095cb-339">Windows Client (Guest OS) Performance Tuning Guidance</span></span>**

-   [<span data-ttu-id="095cb-340">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="095cb-340">Microsoft Windows 7</span></span>](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [<span data-ttu-id="095cb-341">Optimierungs Skript: (vom Microsoft-Support bereitgestellt)</span><span class="sxs-lookup"><span data-stu-id="095cb-341">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [<span data-ttu-id="095cb-342">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="095cb-342">Microsoft Windows 8</span></span>](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [<span data-ttu-id="095cb-343">Optimierungs Skript: (vom Microsoft-Support bereitgestellt)</span><span class="sxs-lookup"><span data-stu-id="095cb-343">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## <span data-ttu-id="095cb-344">Schritte zur Sequenzierung zur Optimierung von Paketen für die Veröffentlichungs Leistung</span><span class="sxs-lookup"><span data-stu-id="095cb-344">Sequencing Steps to Optimize Packages for Publishing Performance</span></span>


<span data-ttu-id="095cb-345">App-v 5,0 und App-v 5,0 SP2 liefern in ihren jeweiligen Versionen einen signifikanten Wert.</span><span class="sxs-lookup"><span data-stu-id="095cb-345">App-V 5.0 and App-V 5.0 SP2 provide significant value in their respective releases.</span></span> <span data-ttu-id="095cb-346">Verschiedene Features erleichtern neue Szenarien oder aktivieren neue Kunden Bereitstellungsszenarien.</span><span class="sxs-lookup"><span data-stu-id="095cb-346">Several features facilitate new scenarios or enabled new customer deployment scenarios.</span></span> <span data-ttu-id="095cb-347">Diese folgenden Features können sich auf die Leistung der Veröffentlichungs-und Startvorgänge auswirken.</span><span class="sxs-lookup"><span data-stu-id="095cb-347">These following features can impact the performance of the publishing and launch operations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="095cb-348">Schritt</span><span class="sxs-lookup"><span data-stu-id="095cb-348">Step</span></span></th>
<th align="left"><span data-ttu-id="095cb-349">Überlegung</span><span class="sxs-lookup"><span data-stu-id="095cb-349">Consideration</span></span></th>
<th align="left"><span data-ttu-id="095cb-350">Vorteile</span><span class="sxs-lookup"><span data-stu-id="095cb-350">Benefits</span></span></th>
<th align="left"><span data-ttu-id="095cb-351">Nachteile</span><span class="sxs-lookup"><span data-stu-id="095cb-351">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="095cb-352">Kein Funktionsbaustein 1 (fb1, auch als primärer FB bezeichnet)</span><span class="sxs-lookup"><span data-stu-id="095cb-352">No Feature Block 1 (FB1, also known as Primary FB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-353">Kein fb1 bedeutet, dass die Anwendung sofort gestartet wird und Datenstromfehler (Anwendung erfordert Datei, dll und muss über das Netzwerk Herunterfahren) während des Starts ist. Wenn Netzwerkeinschränkungen vorhanden sind, wird fb1:</span><span class="sxs-lookup"><span data-stu-id="095cb-353">No FB1 means the application will launch immediately and stream fault (application requires file, DLL and must pull down over the network) during launch.If there are network limitations, FB1 will:</span></span></p>
<ul>
<li><p><span data-ttu-id="095cb-354">Verringern Sie die Anzahl der Datenstromfehler und die Netzwerkbandbreite, die beim erstmaligen Starten einer Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-354">Reduce the number of stream faults and network bandwidth used when you launch an application for the first time.</span></span></p></li>
<li><p><span data-ttu-id="095cb-355">Verzögern Sie den Start, bis der gesamte fb1 gestreamt wurde.</span><span class="sxs-lookup"><span data-stu-id="095cb-355">Delay launch until the entire FB1 has been streamed.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="095cb-356">Durch Datenstromfehler wird die Startzeit verringert.</span><span class="sxs-lookup"><span data-stu-id="095cb-356">Stream faulting decreases the launch time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-357">Virtuelle Anwendungspakete mit konfigurierter fb1 müssen neu sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-357">Virtual application packages with FB1 configured will need to be re-sequenced.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="095cb-358">Entfernen von fb1</span><span class="sxs-lookup"><span data-stu-id="095cb-358">Removing FB1</span></span>

<span data-ttu-id="095cb-359">Zum Entfernen von fb1 ist das Installationsprogramm für die ursprüngliche Anwendung nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="095cb-359">Removing FB1 does not require the original application installer.</span></span> <span data-ttu-id="095cb-360">Nachdem Sie die folgenden Schritte ausgeführt haben, wird empfohlen, den Computer, auf dem der Sequencer ausgeführt wird, auf einen sauberen Snapshot zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="095cb-360">After completing the following steps, it is suggested that you revert the computer running the sequencer to a clean snapshot.</span></span>

<span data-ttu-id="095cb-361">**Sequencer UI** – erstellen Sie ein neues virtuelles Anwendungspaket.</span><span class="sxs-lookup"><span data-stu-id="095cb-361">**Sequencer UI** - Create a New Virtual Application Package.</span></span>

1.  <span data-ttu-id="095cb-362">Führen Sie die Schritte zur Sequenzierung bis zum Anpassen- &gt; Streaming aus.</span><span class="sxs-lookup"><span data-stu-id="095cb-362">Complete the sequencing steps up to Customize -&gt; Streaming.</span></span>

2.  <span data-ttu-id="095cb-363">Wählen Sie beim Streaming-Schritt nicht **das Paket für die Bereitstellung über langsames oder unzuverlässiges Netzwerk optimieren**aus.</span><span class="sxs-lookup"><span data-stu-id="095cb-363">At the Streaming step, do not select **Optimize the package for deployment over slow or unreliable network**.</span></span>

3.  <span data-ttu-id="095cb-364">Wenn gewünscht, fahren Sie mit dem **Zielbetriebssystem**fort.</span><span class="sxs-lookup"><span data-stu-id="095cb-364">If desired, move on to **Target OS**.</span></span>

**<span data-ttu-id="095cb-365">Ändern eines vorhandenen virtuellen Anwendungspakets</span><span class="sxs-lookup"><span data-stu-id="095cb-365">Modify an Existing Virtual Application Package</span></span>**

1.  <span data-ttu-id="095cb-366">Führen Sie die Schritte zur Sequenzierung bis zum Streaming durch.</span><span class="sxs-lookup"><span data-stu-id="095cb-366">Complete the sequencing steps up to Streaming.</span></span>

2.  <span data-ttu-id="095cb-367">Wählen Sie **das Paket für die Bereitstellung nicht über ein langsames oder unzuverlässiges Netzwerk optimieren**aus.</span><span class="sxs-lookup"><span data-stu-id="095cb-367">Do not select **Optimize the package for deployment over a slow or unreliable network**.</span></span>

3.  <span data-ttu-id="095cb-368">Zum **Erstellen eines Pakets**wechseln</span><span class="sxs-lookup"><span data-stu-id="095cb-368">Move to **Create Package**.</span></span>

<span data-ttu-id="095cb-369">**PowerShell** – Aktualisieren eines vorhandenen virtuellen Anwendungspakets</span><span class="sxs-lookup"><span data-stu-id="095cb-369">**PowerShell** - Update an Existing Virtual Application Package.</span></span>

1.  <span data-ttu-id="095cb-370">Öffnen Sie eine erweiterte PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="095cb-370">Open an elevated PowerShell session.</span></span>

2.  <span data-ttu-id="095cb-371">Importieren-Modul **appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="095cb-371">Import-module **appvsequencer**.</span></span>

3.  <span data-ttu-id="095cb-372">**Update-AppvSequencerPackage**  -  **AppvPackageFilePath**</span><span class="sxs-lookup"><span data-stu-id="095cb-372">**Update-AppvSequencerPackage** - **AppvPackageFilePath**</span></span>

    <span data-ttu-id="095cb-373">"C:\\Packages\\MyPackage.AppV"-Installationsprogramm</span><span class="sxs-lookup"><span data-stu-id="095cb-373">"C:\\Packages\\MyPackage.appv" -Installer</span></span>

    <span data-ttu-id="095cb-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath</span><span class="sxs-lookup"><span data-stu-id="095cb-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe" -OutputPath</span></span>

    <span data-ttu-id="095cb-375">"C:\\UpgradedPackages"</span><span class="sxs-lookup"><span data-stu-id="095cb-375">"C:\\UpgradedPackages"</span></span>

    **<span data-ttu-id="095cb-376">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="095cb-376">Note</span></span>**  
    <span data-ttu-id="095cb-377">Dieses Cmdlet erfordert eine ausführbare Datei (exe) oder eine Batchdatei (bat).</span><span class="sxs-lookup"><span data-stu-id="095cb-377">This cmdlet requires an executable (.exe) or batch file (.bat).</span></span> <span data-ttu-id="095cb-378">Sie müssen eine leere (tut nichts) ausführbare oder Batchdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="095cb-378">You must provide an empty (does nothing) executable or batch file.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="095cb-379">Schritt</span><span class="sxs-lookup"><span data-stu-id="095cb-379">Step</span></span></th>
<th align="left"><span data-ttu-id="095cb-380">Erwägungen</span><span class="sxs-lookup"><span data-stu-id="095cb-380">Considerations</span></span></th>
<th align="left"><span data-ttu-id="095cb-381">Vorteile</span><span class="sxs-lookup"><span data-stu-id="095cb-381">Benefits</span></span></th>
<th align="left"><span data-ttu-id="095cb-382">Nachteile</span><span class="sxs-lookup"><span data-stu-id="095cb-382">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="095cb-383">Keine SxS-Installation bei Veröffentlichung (Pre-install SxS-Assemblys)</span><span class="sxs-lookup"><span data-stu-id="095cb-383">No SXS Install at Publish (Pre-Install SxS assemblies)</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-384">Virtuelle Anwendungspakete müssen nicht neu sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-384">Virtual Application packages do not need to be re-sequenced.</span></span> <span data-ttu-id="095cb-385">SxS-Assemblys können im virtuellen Anwendungspaket verbleiben.</span><span class="sxs-lookup"><span data-stu-id="095cb-385">SxS Assemblies can remain in the virtual application package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-386">Die Abhängigkeiten der SxS-Assembly werden nicht zur Veröffentlichungszeit installiert.</span><span class="sxs-lookup"><span data-stu-id="095cb-386">The SxS Assembly dependencies will not install at publishing time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-387">SxS-Assemblierungs Abhängigkeiten müssen bereits vorinstalliert sein.</span><span class="sxs-lookup"><span data-stu-id="095cb-387">SxS Assembly dependencies must be pre-installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="095cb-388">Erstellen eines neuen virtuellen Anwendungspakets auf dem Sequenzer</span><span class="sxs-lookup"><span data-stu-id="095cb-388">Creating a new virtual application package on the sequencer</span></span>

<span data-ttu-id="095cb-389">Wenn während der Sequencer-Überwachung eine SxS-Assembly (wie eine VC + +-Laufzeit) als Teil der Installation einer Anwendung installiert wird, wird die SxS-Assembly automatisch erkannt und im Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="095cb-389">If, during sequencer monitoring, an SxS Assembly (such as a VC++ Runtime) is installed as part of an application’s installation, SxS Assembly will be automatically detected and included in the package.</span></span> <span data-ttu-id="095cb-390">Der Administrator wird benachrichtigt und kann die SxS-Assembly ausschließen.</span><span class="sxs-lookup"><span data-stu-id="095cb-390">The administrator will be notified and will have the option to exclude the SxS Assembly.</span></span>

<span data-ttu-id="095cb-391">**Client Seite**:</span><span class="sxs-lookup"><span data-stu-id="095cb-391">**Client Side**:</span></span>

<span data-ttu-id="095cb-392">Beim Veröffentlichen eines virtuellen Anwendungspakets wird vom App-V 5,0 SP2-Client erkannt, ob bereits eine erforderliche SxS-Abhängigkeit installiert ist.</span><span class="sxs-lookup"><span data-stu-id="095cb-392">When publishing a virtual application package, the App-V 5.0 SP2 Client will detect if a required SxS dependency is already installed.</span></span> <span data-ttu-id="095cb-393">Wenn die Abhängigkeit auf dem Computer nicht verfügbar ist und im Paket enthalten ist, wird ein herkömmlicher Windows Installer (.\*\* MSI\*\*) die Installation der SxS-Assembly wird initiiert.</span><span class="sxs-lookup"><span data-stu-id="095cb-393">If the dependency is unavailable on the computer and it is included in the package, a traditional Windows Installer (.**msi**) installation of the SxS assembly will be initiated.</span></span> <span data-ttu-id="095cb-394">Wie zuvor dokumentiert, installieren Sie einfach die Abhängigkeit auf dem Computer, auf dem der Client ausgeführt wird, um sicherzustellen, dass die Windows Installer-Installation (MSI) nicht erfolgt.</span><span class="sxs-lookup"><span data-stu-id="095cb-394">As previously documented, simply install the dependency on the computer running the client to ensure that the Windows Installer (.msi) installation will not occur.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="095cb-395">Schritt</span><span class="sxs-lookup"><span data-stu-id="095cb-395">Step</span></span></th>
<th align="left"><span data-ttu-id="095cb-396">Erwägungen</span><span class="sxs-lookup"><span data-stu-id="095cb-396">Considerations</span></span></th>
<th align="left"><span data-ttu-id="095cb-397">Vorteile</span><span class="sxs-lookup"><span data-stu-id="095cb-397">Benefits</span></span></th>
<th align="left"><span data-ttu-id="095cb-398">Nachteile</span><span class="sxs-lookup"><span data-stu-id="095cb-398">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="095cb-399">Selektives verwenden dynamischer Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="095cb-399">Selectively Employ Dynamic Configuration files</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-400">Der App-V 5,0-Client muss diese dynamischen Konfigurationsdateien analysieren und verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="095cb-400">The App-V 5.0 client must parse and process these Dynamic Configuration files.</span></span></p>
<p><span data-ttu-id="095cb-401">Achten Sie auf die Größe und Komplexität (Skriptausführung, VREG Einschlüsse/Ausschlüsse) der Datei.</span><span class="sxs-lookup"><span data-stu-id="095cb-401">Be conscious of size and complexity (script execution, VREG inclusions/exclusions) of the file.</span></span></p>
<p><span data-ttu-id="095cb-402">Zahlreiche virtuelle Anwendungspakete verfügen möglicherweise bereits über Benutzer-oder computerspezifische Dynamic Configuration Files-Dateien.</span><span class="sxs-lookup"><span data-stu-id="095cb-402">Numerous virtual application packages may already have User- or computer–specific dynamic configurations files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-403">Die Veröffentlichungszeit wird verbessert, wenn diese Dateien selektiv oder überhaupt nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-403">Publishing times will improve if these files are used selectively or not at all.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-404">Virtuelle Anwendungspakete müssten einzeln oder über die App-V Server-Verwaltungskonsole neu konfiguriert werden, um zugeordnete dynamische Konfigurationsdateien zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="095cb-404">Virtual application packages would need to be reconfigured individually or via the App-V server management console to remove associated Dynamic Configuration files.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="095cb-405">Deaktivieren einer dynamischen Konfiguration mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="095cb-405">Disabling a Dynamic Configuration using Powershell</span></span>

-   <span data-ttu-id="095cb-406">Für bereits veröffentlichte Pakete können Sie `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` ohne</span><span class="sxs-lookup"><span data-stu-id="095cb-406">For already published packages, you can use `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` without</span></span>

    <span data-ttu-id="095cb-407">**-DynamicDeploymentConfiguration-** Parameter</span><span class="sxs-lookup"><span data-stu-id="095cb-407">**-DynamicDeploymentConfiguration** parameter</span></span>

-   <span data-ttu-id="095cb-408">Verwenden Sie beim Hinzufügen neuer Pakete `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` nicht die</span><span class="sxs-lookup"><span data-stu-id="095cb-408">Similarly, when adding new packages using `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv`, do not use the</span></span>

    <span data-ttu-id="095cb-409">**-DynamicDeploymentConfiguration-** Parameter.</span><span class="sxs-lookup"><span data-stu-id="095cb-409">**-DynamicDeploymentConfiguration** parameter.</span></span>

<span data-ttu-id="095cb-410">Eine Dokumentation zur Anwendung einer dynamischen Konfiguration finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="095cb-410">For documentation on How to Apply a Dynamic Configuration, see:</span></span>

-   [<span data-ttu-id="095cb-411">So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an</span><span class="sxs-lookup"><span data-stu-id="095cb-411">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

-   [<span data-ttu-id="095cb-412">Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an</span><span class="sxs-lookup"><span data-stu-id="095cb-412">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="095cb-413">Schritt</span><span class="sxs-lookup"><span data-stu-id="095cb-413">Step</span></span></th>
<th align="left"><span data-ttu-id="095cb-414">Erwägungen</span><span class="sxs-lookup"><span data-stu-id="095cb-414">Considerations</span></span></th>
<th align="left"><span data-ttu-id="095cb-415">Vorteile</span><span class="sxs-lookup"><span data-stu-id="095cb-415">Benefits</span></span></th>
<th align="left"><span data-ttu-id="095cb-416">Nachteile</span><span class="sxs-lookup"><span data-stu-id="095cb-416">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="095cb-417">Konto für synchrone Skriptausführung während des Paket Lebenszyklus.</span><span class="sxs-lookup"><span data-stu-id="095cb-417">Account for Synchronous Script Execution during Package Lifecycle.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-418">Wenn Skript Sicherheiten in das Paket eingebettet sind, kann Add (PowerShell) erheblich langsamer sein.</span><span class="sxs-lookup"><span data-stu-id="095cb-418">If script collateral is embedded in the package, Add (Powershell) may be significantly slower.</span></span></p>
<p><span data-ttu-id="095cb-419">Die Ausführung von Skripts während des Starts virtueller Anwendungen (StartVirtualEnvironment, StartProcess) und/oder Add + Publish wirkt sich auf die wahrgenommene Leistung während eines oder mehrerer dieser Lebenszyklus Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="095cb-419">Running of scripts during virtual application launch (StartVirtualEnvironment, StartProcess) and/or Add+Publish will impact the perceived performance during one or more of these lifecycle operations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-420">Durch die Verwendung von asynchronen (nicht blockierenden) Skripts wird sichergestellt, dass die Lebenszyklus Vorgänge effizient abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-420">Use of Asynchronous (Non-Blocking) Scripts will ensure that the lifecycle operations complete efficiently.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-421">Dieser Schritt erfordert Kenntnisse über alle virtuellen Anwendungspakete mit eingebetteten Skript Sicherheiten, denen dynamische Konfigurationsdateien zugeordnet sind, und die synchron Skripts referenzieren und ausführen.</span><span class="sxs-lookup"><span data-stu-id="095cb-421">This step requires working knowledge of all virtual application packages with embedded script collateral, which have associated dynamic configurations files and which reference and run scripts synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="095cb-422">Entfernen Sie überflüssige virtuelle Schriftarten aus dem Paket.</span><span class="sxs-lookup"><span data-stu-id="095cb-422">Remove Extraneous Virtual Fonts from Package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-423">Die Mehrzahl der vom App-V-Produktteam untersuchten Anwendungen enthielt eine geringe Anzahl von Schriftarten, in der Regel weniger als 20.</span><span class="sxs-lookup"><span data-stu-id="095cb-423">The majority of applications investigated by the App-V product team contained a small number of fonts, typically fewer than 20.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-424">Virtuelle Schriftarten wirken sich auf die Veröffentlichungs Aktualisierungsleistung aus.</span><span class="sxs-lookup"><span data-stu-id="095cb-424">Virtual Fonts impact publishing refresh performance.</span></span></p></td>
<td align="left"><p><span data-ttu-id="095cb-425">Die gewünschten Schriftarten müssen nativ aktiviert/installiert werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-425">Desired fonts will need to be enabled/installed natively.</span></span> <span data-ttu-id="095cb-426">Anweisungen hierzu finden Sie unter Installieren oder Deinstallieren von Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="095cb-426">For instructions, see Install or uninstall fonts.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="095cb-427">Ermitteln, welche virtuellen Schriftarten im Paket vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="095cb-427">Determining what virtual fonts exist in the package</span></span>

-   <span data-ttu-id="095cb-428">Erstellen Sie eine Kopie des Pakets.</span><span class="sxs-lookup"><span data-stu-id="095cb-428">Make a copy of the package.</span></span>

-   <span data-ttu-id="095cb-429">Paket umbenennen \ _Copy. AppV zu Package\_copy.zip</span><span class="sxs-lookup"><span data-stu-id="095cb-429">Rename Package\_copy.appv to Package\_copy.zip</span></span>

-   <span data-ttu-id="095cb-430">Öffnen Sie AppxManifest.xml, und suchen Sie nach folgendem:</span><span class="sxs-lookup"><span data-stu-id="095cb-430">Open AppxManifest.xml and locate the following:</span></span>

    <span data-ttu-id="095cb-431">&lt;AppV: Extension Category = "AppV. Fonts"&gt;</span><span class="sxs-lookup"><span data-stu-id="095cb-431">&lt;appv:Extension Category="AppV.Fonts"&gt;</span></span>

    <span data-ttu-id="095cb-432">&lt;AppV: Schriftarten&gt;</span><span class="sxs-lookup"><span data-stu-id="095cb-432">&lt;appv:Fonts&gt;</span></span>

    <span data-ttu-id="095cb-433">&lt;AppV: Font Path = "\ [{Fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /AppV: Font&gt;</span><span class="sxs-lookup"><span data-stu-id="095cb-433">&lt;appv:Font Path="\[{Fonts}\]\\private\\CalibriL.ttf" DelayLoad="true"&gt;&lt;/appv:Font&gt;</span></span>

    **<span data-ttu-id="095cb-434">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="095cb-434">Note</span></span>**  
    <span data-ttu-id="095cb-435">Wenn Schriftarten als " **DelayLoad**" gekennzeichnet sind, wirkt sich dies nicht auf den ersten Start aus.</span><span class="sxs-lookup"><span data-stu-id="095cb-435">If there are fonts marked as **DelayLoad**, those will not impact first launch.</span></span>



~~~
&lt;/appv:Fonts&gt;
~~~

### <span data-ttu-id="095cb-436">Ausschließen virtueller Schriftarten aus dem Paket</span><span class="sxs-lookup"><span data-stu-id="095cb-436">Excluding virtual fonts from the package</span></span>

<span data-ttu-id="095cb-437">Verwenden Sie die dynamische Konfigurationsdatei, die am besten für den Benutzerbereich geeignet ist – Bereitstellungskonfiguration für alle Benutzer auf dem Computer, Benutzerkonfiguration für bestimmte Benutzer oder Benutzer.</span><span class="sxs-lookup"><span data-stu-id="095cb-437">Use the dynamic configuration file that best suits the user scope – deployment configuration for all users on computer, user configuration for specific user or users.</span></span>

-   <span data-ttu-id="095cb-438">Deaktivieren Sie Schriftarten mit der Bereitstellungs-oder Benutzerkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="095cb-438">Disable fonts with the deployment or user configuration.</span></span>

<span data-ttu-id="095cb-439">Schriftarten</span><span class="sxs-lookup"><span data-stu-id="095cb-439">Fonts</span></span>

--&gt;

<span data-ttu-id="095cb-440">&lt;Schriftarten aktiviert = "falsch"/&gt;</span><span class="sxs-lookup"><span data-stu-id="095cb-440">&lt;Fonts Enabled="false" /&gt;</span></span>

<span data-ttu-id="095cb-441">&lt;!--</span><span class="sxs-lookup"><span data-stu-id="095cb-441">&lt;!--</span></span>

## <a href="" id="bkmk-terms1"></a> <span data-ttu-id="095cb-442">App-V 5,0-Terminologie zur Leistungssteuerung</span><span class="sxs-lookup"><span data-stu-id="095cb-442">App-V 5.0 Performance Guidance Terminology</span></span>


<span data-ttu-id="095cb-443">Die folgenden Begriffe werden verwendet, wenn Konzepte und Aktionen im Zusammenhang mit der App-V 5,0-Leistungsoptimierung beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="095cb-443">The following terms are used when describing concepts and actions related to App-V 5.0 performance optimization.</span></span>

-   <span data-ttu-id="095cb-444">**Komplexität** : bezieht sich auf ein oder mehrere Paket Merkmale, die sich auf die Leistung bei der Vorkonfiguration (**Add-AppvClientPackage**) oder Integration (**Publish-AppvClientPackage**) auswirken können.</span><span class="sxs-lookup"><span data-stu-id="095cb-444">**Complexity** – Refers to the one or more package characteristics that may impact performance during pre-configure (**Add-AppvClientPackage**) or integration (**Publish-AppvClientPackage**).</span></span> <span data-ttu-id="095cb-445">Einige Beispiel Merkmale sind: Manifestgröße, Anzahl der virtuellen Schriftarten, Anzahl der Dateien.</span><span class="sxs-lookup"><span data-stu-id="095cb-445">Some example characteristics are: manifest size, number of virtual fonts, number of files.</span></span>

-   <span data-ttu-id="095cb-446">**De-Integration** – entfernt die Benutzer Integrationen</span><span class="sxs-lookup"><span data-stu-id="095cb-446">**De-Integrate** – Removes the user integrations</span></span>

-   <span data-ttu-id="095cb-447">**Re-Integration** – wendet die Benutzer Integrationen an.</span><span class="sxs-lookup"><span data-stu-id="095cb-447">**Re-Integrate** – Applies the user integrations.</span></span>

-   <span data-ttu-id="095cb-448">**Nicht persistent, gebündelt** – erstellt bei jeder Anmeldung einen Computer, auf dem eine virtuelle Umgebung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="095cb-448">**Non-Persistent, Pooled** – Creates a computer running a virtual environment each time they log in.</span></span>

-   <span data-ttu-id="095cb-449">**Persistent, persönlich** – ein Computer mit einer virtuellen Umgebung, der bei jedem Login gleich bleibt.</span><span class="sxs-lookup"><span data-stu-id="095cb-449">**Persistent, Personal** – A computer running a virtual environment that remains the same for every login.</span></span>

-   <span data-ttu-id="095cb-450">**Stateful** -für dieses Dokument impliziert, dass Benutzer Integrationen zwischen Sitzungen beibehalten werden und eine Technologie für die Benutzer Umgebungsverwaltung in Verbindung mit nicht persistenten RDSH oder VDI verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="095cb-450">**Stateful** - For this document, implies that user integrations are persisted between sessions and a user environment management technology is used in conjunction with non-persistent RDSH or VDI.</span></span>

-   <span data-ttu-id="095cb-451">**Statuslos** – stellt ein Szenario dar, in dem kein Benutzerstatus zwischen Sitzungen beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="095cb-451">**Stateless** – Represents a scenario when no user state is persisted between sessions.</span></span>

-   <span data-ttu-id="095cb-452">**Trigger** – (oder systemeigene Aktions Trigger).</span><span class="sxs-lookup"><span data-stu-id="095cb-452">**Trigger** – (or Native Action Triggers).</span></span> <span data-ttu-id="095cb-453">UPM verwendet diese Typen von Triggern, um Überwachungs-oder Synchronisierungsvorgänge zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="095cb-453">UPM uses these types of triggers to initiate monitoring or synchronization operations.</span></span>

-   <span data-ttu-id="095cb-454">**Benutzererfahrung** – im Kontext von App-V 5,0 ist die Benutzeroberfläche quantitativ die Summe der folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="095cb-454">**User Experience** - In the context of App-V 5.0, the user experience, quantitatively, is the sum of the following parts:</span></span>

    -   <span data-ttu-id="095cb-455">Ab dem Punkt, an dem Benutzer eine Anmeldung initiieren, wenn Sie den Desktop manipulieren können.</span><span class="sxs-lookup"><span data-stu-id="095cb-455">From the point that users initiate a log-in to when they are able to manipulate the desktop.</span></span>

    -   <span data-ttu-id="095cb-456">Ab dem Punkt, an dem der Desktop mit dem Punkt interagieren kann, an dem eine Veröffentlichungsaktualisierung beginnt (in PowerShell-Ausdrücken, synchronisieren), wenn die vollständige Serverinfrastruktur von App-V 5,0 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="095cb-456">From the point where the desktop can be interacted with to the point a publishing refresh begins (in PowerShell terms, sync) when using the App-V 5.0 full server infrastructure.</span></span> <span data-ttu-id="095cb-457">In eigenständigen Instanzen werden die PowerShell-Befehle **Add-AppVClientPackage** und **Publish-AppVClientPackage** initiiert.</span><span class="sxs-lookup"><span data-stu-id="095cb-457">In standalone instances, it is when the **Add-AppVClientPackage** and **Publish-AppVClientPackage Powershell** commands are initiated.</span></span>

    -   <span data-ttu-id="095cb-458">Vom Anfang bis zum Abschluss der Veröffentlichungsaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="095cb-458">From start to completion of the publishing refresh.</span></span> <span data-ttu-id="095cb-459">In eigenständigen Instanzen ist dies die erste letzte virtuelle Anwendung, die veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="095cb-459">In standalone instances, this is the first to last virtual application published.</span></span>

    -   <span data-ttu-id="095cb-460">Ab dem Punkt, an dem die virtuelle Anwendung für den Start über eine Verknüpfung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="095cb-460">From the point where the virtual application is available to launch from a shortcut.</span></span> <span data-ttu-id="095cb-461">Alternativ dazu befindet Sie sich ab dem Zeitpunkt, zu dem die Dateitypzuordnung registriert ist, und startet eine angegebene virtuelle Anwendung.</span><span class="sxs-lookup"><span data-stu-id="095cb-461">Alternatively, it is from the point at which the file type association is registered and will launch a specified virtual application.</span></span>

-   <span data-ttu-id="095cb-462">**Verwaltung von Benutzerprofilen** – der kontrollierte und strukturierte Ansatz zum Verwalten von Benutzer Komponenten, die mit der Umgebung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="095cb-462">**User Profile Management** – The controlled and structured approach to managing user components associated with the environment.</span></span> <span data-ttu-id="095cb-463">Beispielsweise Benutzerprofile, Einstellungen und Richtlinienverwaltung, Anwendungssteuerung und Anwendungsbereitstellung.</span><span class="sxs-lookup"><span data-stu-id="095cb-463">For example, user profiles, preference and policy management, application control and application deployment.</span></span> <span data-ttu-id="095cb-464">Sie können mithilfe von Skripting oder Lösungen von Drittanbietern die Umgebung nach Bedarf konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="095cb-464">You can use scripting or third-party solutions configure the environment as needed.</span></span>






## <span data-ttu-id="095cb-465">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="095cb-465">Related topics</span></span>


[<span data-ttu-id="095cb-466">Microsoft Application Virtualization 5,0-Administrator Handbuch</span><span class="sxs-lookup"><span data-stu-id="095cb-466">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)









