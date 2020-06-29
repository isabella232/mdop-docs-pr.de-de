---
title: Vorbereiten einer UE-V 2. x-Bereitstellung
description: Vorbereiten einer UE-V 2. x-Bereitstellung
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811746"
---
# <span data-ttu-id="b8e26-103">Vorbereiten einer UE-V 2. x-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="b8e26-103">Prepare a UE-V 2.x Deployment</span></span>


<span data-ttu-id="b8e26-104">Bevor Sie Microsoft User Experience Virtualization (UE-V) 2,0 oder 2,1 als Lösung für die Synchronisierung von Einstellungen zwischen Geräten bereitstellen, auf die Benutzer in Ihrem Unternehmen zugreifen, müssen Sie einige Schritte planen und vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="b8e26-104">There is some planning and preparation to do before you deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 as a solution for synchronizing settings between devices that users access in your enterprise.</span></span> <span data-ttu-id="b8e26-105">In diesem Thema erfahren Sie, welche Art von Bereitstellung Sie ausführen werden und welche Vorbereitungen Sie im Voraus vornehmen können, damit Ihre Bereitstellung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="b8e26-105">This topic helps you determine what type of deployment you'll be doing and what preparation you can make beforehand so that your deployment is successful.</span></span>

<span data-ttu-id="b8e26-106">Sehen wir uns zunächst die Aufgaben an, die Sie für die Bereitstellung von UE-V ausführen werden:</span><span class="sxs-lookup"><span data-stu-id="b8e26-106">First, let’s look at the tasks you’ll do to deploy UE-V:</span></span>

-   <span data-ttu-id="b8e26-107">Planen der UE-V-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="b8e26-107">Plan your UE-V Deployment</span></span>

    <span data-ttu-id="b8e26-108">Bevor Sie etwas bereitstellen, besteht ein guter erster Schritt darin, etwas zu planen, damit Sie ermitteln können, welche UE-V-Features bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-108">Before you deploy anything, a good first step is to do a little bit of planning so that you can determine which UE-V features you’ll deploy.</span></span> <span data-ttu-id="b8e26-109">Wenn Sie diese Seite nun belassen, sollten Sie die folgenden Planungsinformationen durchlesen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-109">So if you leave this page, make sure you come back and read through the planning information below.</span></span>

-   [<span data-ttu-id="b8e26-110">Bereitstellen der erforderlichen Features für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="b8e26-110">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    <span data-ttu-id="b8e26-111">Für jede UE-V-Bereitstellung sind diese Aktivitäten erforderlich:</span><span class="sxs-lookup"><span data-stu-id="b8e26-111">Every UE-V deployment requires these activities:</span></span>

    -   [<span data-ttu-id="b8e26-112">Definieren eines Speicherorts für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-112">Define a settings storage location</span></span>](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [<span data-ttu-id="b8e26-113">Entscheiden, wie der UE-v-Agent bereitgestellt und UE-v-Konfigurationen verwaltet werden</span><span class="sxs-lookup"><span data-stu-id="b8e26-113">Decide how to deploy the UE-V Agent and manage UE-V configurations</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   <span data-ttu-id="b8e26-114">[Installieren des UE-V-Agents](https://technet.microsoft.com/library/dn458891.aspx#agent) auf jedem Benutzer Computer, auf dem die Einstellungen synchronisiert werden müssen</span><span class="sxs-lookup"><span data-stu-id="b8e26-114">[Install the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) on every user computer that needs settings synchronized</span></span>

-   <span data-ttu-id="b8e26-115">Optional können Sie [UE-V 2. x für benutzerdefinierte Anwendungen bereitstellen.](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span><span class="sxs-lookup"><span data-stu-id="b8e26-115">Optionally, you can [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span></span>

    <span data-ttu-id="b8e26-116">Die Planung hilft Ihnen herauszufinden, ob UE-v die Synchronisierung von Einstellungen für benutzerdefinierte Anwendungen (Drittanbieter oder Branchen) unterstützen soll, für die diese UE-v-Features erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="b8e26-116">Planning will help you figure out whether you want UE-V to support the synchronization of settings for custom applications (third-party or line-of-business), which requires these UE-V features:</span></span>

    -   <span data-ttu-id="b8e26-117">[Installieren des UEV-Generators](https://technet.microsoft.com/library/dn458942.aspx#uevgen) zum Erstellen, bearbeiten und Überprüfen der Speicherort Vorlagen für benutzerdefinierte Einstellungen, die zum Synchronisieren von benutzerdefinierten Anwendungseinstellungen erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="b8e26-117">[Install the UEV Generator](https://technet.microsoft.com/library/dn458942.aspx#uevgen) so you can create, edit, and validate the custom settings location templates required to synchronize custom application settings</span></span>

    -   <span data-ttu-id="b8e26-118">[Erstellen von Speicherort Vorlagen für benutzerdefinierte Einstellungen](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) mithilfe des UE-V-Generators</span><span class="sxs-lookup"><span data-stu-id="b8e26-118">[Create custom settings location templates](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) by using the UE-V Generator</span></span>

    -   <span data-ttu-id="b8e26-119">[Bereitstellen eines UE-V-Einstellungs Vorlagen Katalogs](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) , mit dem Sie die Speicherort Vorlagen für benutzerdefinierte Einstellungen speichern</span><span class="sxs-lookup"><span data-stu-id="b8e26-119">[Deploy a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) that you use to store your custom settings location templates</span></span>

<span data-ttu-id="b8e26-120">Dieses Workflowdiagramm bietet eine allgemeine Übersicht über eine UE-v-Bereitstellung und die Entscheidungen, die bestimmen, wie UE-v in Ihrem Unternehmen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b8e26-120">This workflow diagram provides a high-level understanding of a UE-V deployment and the decisions that determine how you deploy UE-V in your enterprise.</span></span>

![deploymentworkflow](images/deploymentworkflow.png)

<span data-ttu-id="b8e26-122">**Planen einer UE-V-Bereitstellung:** Zunächst möchten Sie etwas planen, damit Sie ermitteln können, welche UE-V-Komponenten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-122">**Planning a UE-V deployment:** First, you want to do a little bit of planning so that you can determine which UE-V components you’ll be deploying.</span></span> <span data-ttu-id="b8e26-123">Die Planung einer UE-V-Bereitstellung umfasst folgende Dinge:</span><span class="sxs-lookup"><span data-stu-id="b8e26-123">Planning a UE-V deployment involves these things:</span></span>

-   [<span data-ttu-id="b8e26-124">Entscheiden, ob Einstellungen für benutzerdefinierte Anwendungen synchronisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="b8e26-124">Decide whether to synchronize settings for custom applications</span></span>](#deciding)

    <span data-ttu-id="b8e26-125">Dadurch wird bestimmt, ob Sie den UE-V-Generator während der Bereitstellung installieren, wodurch Sie benutzerdefinierte Speicherort Vorlagen für Einstellungen erstellen können.</span><span class="sxs-lookup"><span data-stu-id="b8e26-125">This determines whether you will install the UE-V Generator during deployment, which lets you create custom settings location templates.</span></span> <span data-ttu-id="b8e26-126">Sie umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b8e26-126">It involves the following:</span></span>

    <span data-ttu-id="b8e26-127">Überprüfen Sie die [Einstellungen, die automatisch in einer UE-V-Bereitstellung synchronisiert werden](#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="b8e26-127">Review the [settings that are synchronized automatically in a UE-V deployment](#autosyncsettings).</span></span>

    <span data-ttu-id="b8e26-128">[Ermitteln Sie, ob die Einstellungen für andere Anwendungen synchronisiert werden müssen](#determinesettingssync).</span><span class="sxs-lookup"><span data-stu-id="b8e26-128">[Determine whether you need settings synchronized for other applications](#determinesettingssync).</span></span>

-   <span data-ttu-id="b8e26-129">Lesen Sie [Weitere Überlegungen zur Bereitstellung von UE-V](#considerations), wie beispielsweise die Höchstverfügbarkeit und die Kapazitätsplanung.</span><span class="sxs-lookup"><span data-stu-id="b8e26-129">Review [other considerations for deploying UE-V](#considerations), such as high availability and capacity planning.</span></span>

-   [<span data-ttu-id="b8e26-130">Voraussetzungen und unterstützte Konfigurationen für UE-V bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8e26-130">Confirm prerequisites and supported configurations for UE-V</span></span>](#prereqs)

## <a href="" id="deciding"></a><span data-ttu-id="b8e26-131">Entscheiden, ob Einstellungen für benutzerdefinierte Anwendungen synchronisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="b8e26-131">Decide Whether to Synchronize Settings for Custom Applications</span></span>


<span data-ttu-id="b8e26-132">In einer UE-V-Bereitstellung werden viele Einstellungen automatisch synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="b8e26-132">In a UE-V deployment, many settings are automatically synchronized.</span></span> <span data-ttu-id="b8e26-133">Sie können UE-V aber auch so anpassen, dass Einstellungen für andere Anwendungen wie Branchen-und Drittanbieter-apps synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-133">But you can also customize UE-V to synchronize settings for other applications, such as line-of-business and third-party apps.</span></span>

<span data-ttu-id="b8e26-134">Die Entscheidung, ob UE-v die Einstellungen für benutzerdefinierte Anwendungen synchronisieren soll, ist wahrscheinlich der wichtigste Teil bei der Planung Ihrer UE-v-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="b8e26-134">Deciding if you want UE-V to synchronize settings for custom applications is probably the most important part of planning your UE-V deployment.</span></span> <span data-ttu-id="b8e26-135">Die Themen in diesem Abschnitt werden Ihnen bei der Entscheidung helfen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-135">The topics in this section will help you make that decision.</span></span>

### <a href="" id="autosyncsettings"></a><span data-ttu-id="b8e26-136">Einstellungen, die in einer UE-V-Bereitstellung automatisch synchronisiert werden</span><span class="sxs-lookup"><span data-stu-id="b8e26-136">Settings that are automatically synchronized in a UE-V deployment</span></span>

<span data-ttu-id="b8e26-137">Dieser Abschnitt enthält Informationen zu den Einstellungen, die in UE-V standardmäßig synchronisiert werden, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="b8e26-137">This section provides information about the settings that are synchronized by default in UE-V, including the following:</span></span>

<span data-ttu-id="b8e26-138">Desktop Anwendungen, deren Einstellungen standardmäßig synchronisiert werden</span><span class="sxs-lookup"><span data-stu-id="b8e26-138">Desktop applications whose settings are synchronized by default</span></span>

<span data-ttu-id="b8e26-139">Windows-Desktopeinstellungen, die standardmäßig synchronisiert werden</span><span class="sxs-lookup"><span data-stu-id="b8e26-139">Windows desktop settings that are synchronized by default</span></span>

<span data-ttu-id="b8e26-140">Eine Erklärung zur Unterstützung für die Synchronisierung der Windows-App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-140">A statement of support for Windows app setting synchronization</span></span>

<span data-ttu-id="b8e26-141">Eine vollständige Liste der Einstellungen für Microsoft Office 2013, Microsoft Office 2010 und Microsoft Office 2007, die von UE-v synchronisiert werden, finden Sie unter [Vorlagen für die Benutzeroberflächen-Virtualisierung (UE-v) für Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) .</span><span class="sxs-lookup"><span data-stu-id="b8e26-141">See [User Experience Virtualization (UE-V) settings templates for Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) to download a complete list of the specific Microsoft Office 2013, Microsoft Office 2010, and Microsoft Office 2007 settings that are synchronized by UE-V.</span></span>

### <span data-ttu-id="b8e26-142">Standardmäßig synchronisierte Desktop Anwendungen in UE-v 2,1 und UE-v 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="b8e26-142">Desktop applications synchronized by default in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="b8e26-143">Wenn Sie den UE-V 2,1-oder 2,1 SP1-Agent installieren, registriert er eine Standardgruppe von Einstellungen-Standort Vorlagen, mit denen die Einstellungswerte für diese gängigen Microsoft-Anwendungen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-143">When you install the UE-V 2.1 or 2.1 SP1 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="b8e26-144">Tipp</span><span class="sxs-lookup"><span data-stu-id="b8e26-144">Tip</span></span>**  
<span data-ttu-id="b8e26-145">**Synchronisierung von Microsoft Office 2007-Einstellungen** – in UE-V 2,1 und 2,1 SP1 ist eine Vorlage für den Einstellungs Speicherort standardmäßig nicht mehr für Office 2007-Anwendungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b8e26-145">**Microsoft Office 2007 Settings Synchronization** – In UE-V 2.1 and 2.1 SP1, a settings location template is no longer included by default for Office 2007 applications.</span></span> <span data-ttu-id="b8e26-146">Sie können jedoch weiterhin Office 2007-Vorlagen von UE-v 2,0 oder früher verwenden und die Vorlagen aus dem [UE-v-Vorlagenkatalog](https://go.microsoft.com/fwlink/p/?LinkID=246589)abrufen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-146">However, you can still use Office 2007 templates from UE-V 2.0 or earlier and can get the templates from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="b8e26-147">Anwendungskategorie</span><span class="sxs-lookup"><span data-stu-id="b8e26-147">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="b8e26-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8e26-148">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e26-149">Microsoft Office 2010-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-149">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="b8e26-150">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Eine Liste aller synchronisierten Einstellungen herunterladen </a> )</span><span class="sxs-lookup"><span data-stu-id="b8e26-150">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-151">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-151">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="b8e26-152">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-152">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="b8e26-153">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-153">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="b8e26-154">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-154">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="b8e26-155">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-155">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="b8e26-156">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-156">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="b8e26-157">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-157">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="b8e26-158">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-158">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="b8e26-159">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-159">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="b8e26-160">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-160">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="b8e26-161">Microsoft lync 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-161">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="b8e26-162">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-162">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="b8e26-163">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-163">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e26-164">Microsoft Office 2013-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-164">Microsoft Office 2013 applications</span></span></p>
<p><span data-ttu-id="b8e26-165">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Eine Liste aller synchronisierten Einstellungen herunterladen </a> )</span><span class="sxs-lookup"><span data-stu-id="b8e26-165">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-166">Microsoft Word 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-166">Microsoft Word 2013</span></span></p>
<p><span data-ttu-id="b8e26-167">Microsoft Excel 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-167">Microsoft Excel 2013</span></span></p>
<p><span data-ttu-id="b8e26-168">Microsoft Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-168">Microsoft Outlook 2013</span></span></p>
<p><span data-ttu-id="b8e26-169">Microsoft Access 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-169">Microsoft Access 2013</span></span></p>
<p><span data-ttu-id="b8e26-170">Microsoft Project 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-170">Microsoft Project 2013</span></span></p>
<p><span data-ttu-id="b8e26-171">Microsoft PowerPoint 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-171">Microsoft PowerPoint 2013</span></span></p>
<p><span data-ttu-id="b8e26-172">Microsoft Publisher 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-172">Microsoft Publisher 2013</span></span></p>
<p><span data-ttu-id="b8e26-173">Microsoft Visio 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-173">Microsoft Visio 2013</span></span></p>
<p><span data-ttu-id="b8e26-174">Microsoft InfoPath 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-174">Microsoft InfoPath 2013</span></span></p>
<p><span data-ttu-id="b8e26-175">Microsoft lync 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-175">Microsoft Lync 2013</span></span></p>
<p><span data-ttu-id="b8e26-176">Microsoft OneNote 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-176">Microsoft OneNote 2013</span></span></p>
<p><span data-ttu-id="b8e26-177">Microsoft SharePoint Designer 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-177">Microsoft SharePoint Designer 2013</span></span></p>
<p><span data-ttu-id="b8e26-178">Microsoft Office 2013 Upload Center</span><span class="sxs-lookup"><span data-stu-id="b8e26-178">Microsoft Office 2013 Upload Center</span></span></p>
<p><span data-ttu-id="b8e26-179">Microsoft OneDrive for Business 2013</span><span class="sxs-lookup"><span data-stu-id="b8e26-179">Microsoft OneDrive for Business 2013</span></span></p>
<p><span data-ttu-id="b8e26-180">Die Standort Vorlagen für UE-V 2,1 und 2,1 SP1 Microsoft Office 2013-Einstellungen umfassen eine verbesserte Unterstützung für Outlook-Signaturen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-180">The UE-V 2.1 and 2.1 SP1 Microsoft Office 2013 settings location templates include improved Outlook signature support.</span></span> <span data-ttu-id="b8e26-181">Wir haben die Synchronisierung von standardmäßigen Signatureinstellungen für neue, Antworten und weitergeleitete e-Mails hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8e26-181">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b8e26-182">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-182">Note</span></span></strong><br/><p><span data-ttu-id="b8e26-183">Für jedes Gerät, auf dem ein Benutzer seine Outlook-Signatur synchronisieren möchte, muss ein Outlook-Profil erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-183">An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="b8e26-184">Wenn das Profil noch nicht erstellt wurde, kann der Benutzer eine erstellen und dann Outlook auf diesem Gerät neu starten, um die Signatur Synchronisierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-184">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e26-185">Browser Optionen: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 und Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="b8e26-185">Browser options: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10, and Internet Explorer 11</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-186">Favoriten, Startseite, Tabstopps und Symbolleisten.</span><span class="sxs-lookup"><span data-stu-id="b8e26-186">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b8e26-187">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-187">Note</span></span></strong><br/><p><span data-ttu-id="b8e26-188">UE-V führt keine Roaming-Einstellungen für Internet Explorer-Cookies durch.</span><span class="sxs-lookup"><span data-stu-id="b8e26-188">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e26-189">Windows-Zubehör</span><span class="sxs-lookup"><span data-stu-id="b8e26-189">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-190">Microsoft Calculator, Notepad, WordPad.</span><span class="sxs-lookup"><span data-stu-id="b8e26-190">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="b8e26-191">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-191">Note</span></span>**  
<span data-ttu-id="b8e26-192">UE-V 2,1 SP1 synchronisiert keine Einstellungen zwischen dem Microsoft-Rechner in Windows 10 und dem Microsoft-Rechner in früheren Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-192">UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>



### <span data-ttu-id="b8e26-193">Standardmäßig synchronisierte Desktop Anwendungen in UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="b8e26-193">Desktop applications synchronized by default in UE-V 2.0</span></span>

<span data-ttu-id="b8e26-194">Wenn Sie den UE-V 2,0-Agent installieren, registriert er eine Standardgruppe von Einstellungen-Standort Vorlagen, mit denen die Einstellungswerte für diese gängigen Microsoft-Anwendungen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-194">When you install the UE-V 2.0 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="b8e26-195">Tipp</span><span class="sxs-lookup"><span data-stu-id="b8e26-195">Tip</span></span>**  
<span data-ttu-id="b8e26-196">**Synchronisierung von Microsoft Office 2013-Einstellungen** – in UE-v 2,0 ist eine Vorlage für den einstellungensort nicht standardmäßig für Office 2013-Anwendungen enthalten, steht aber aus dem [UE-v-Vorlagenkatalog](https://go.microsoft.com/fwlink/p/?LinkID=246589)zum Download zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b8e26-196">**Microsoft Office 2013 Settings Synchronization** – In UE-V 2.0, a settings location template is not included by default for Office 2013 applications, but is available for download from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span> <span data-ttu-id="b8e26-197">Beim [Synchronisieren von Office 2013 mit UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) werden Details zu den unterstützten Vorlagen bereitgestellt, mit denen die Office 2013-Einstellungen synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-197">[Synchronizing Office 2013 with UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) provides details about the supported templates that synchronize Office 2013 settings.</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="b8e26-198">Anwendungskategorie</span><span class="sxs-lookup"><span data-stu-id="b8e26-198">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="b8e26-199">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8e26-199">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e26-200">Microsoft Office 2007-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-200">Microsoft Office 2007 applications</span></span></p>
<p><span data-ttu-id="b8e26-201">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Eine Liste aller synchronisierten Einstellungen herunterladen </a> )</span><span class="sxs-lookup"><span data-stu-id="b8e26-201">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-202">Microsoft Access 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-202">Microsoft Access 2007</span></span></p>
<p><span data-ttu-id="b8e26-203">Microsoft Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-203">Microsoft Communicator 2007</span></span></p>
<p><span data-ttu-id="b8e26-204">Microsoft Excel 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-204">Microsoft Excel 2007</span></span></p>
<p><span data-ttu-id="b8e26-205">Microsoft InfoPath 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-205">Microsoft InfoPath 2007</span></span></p>
<p><span data-ttu-id="b8e26-206">Microsoft OneNote 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-206">Microsoft OneNote 2007</span></span></p>
<p><span data-ttu-id="b8e26-207">Microsoft Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-207">Microsoft Outlook 2007</span></span></p>
<p><span data-ttu-id="b8e26-208">Microsoft PowerPoint 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-208">Microsoft PowerPoint 2007</span></span></p>
<p><span data-ttu-id="b8e26-209">Microsoft Project 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-209">Microsoft Project 2007</span></span></p>
<p><span data-ttu-id="b8e26-210">Microsoft Publisher 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-210">Microsoft Publisher 2007</span></span></p>
<p><span data-ttu-id="b8e26-211">Microsoft SharePoint Designer 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-211">Microsoft SharePoint Designer 2007</span></span></p>
<p><span data-ttu-id="b8e26-212">Microsoft Visio 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-212">Microsoft Visio 2007</span></span></p>
<p><span data-ttu-id="b8e26-213">Microsoft Word 2007</span><span class="sxs-lookup"><span data-stu-id="b8e26-213">Microsoft Word 2007</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e26-214">Microsoft Office 2010-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-214">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="b8e26-215">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Eine Liste aller synchronisierten Einstellungen herunterladen </a> )</span><span class="sxs-lookup"><span data-stu-id="b8e26-215">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-216">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-216">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="b8e26-217">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-217">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="b8e26-218">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-218">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="b8e26-219">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-219">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="b8e26-220">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-220">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="b8e26-221">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-221">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="b8e26-222">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-222">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="b8e26-223">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-223">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="b8e26-224">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-224">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="b8e26-225">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-225">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="b8e26-226">Microsoft lync 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-226">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="b8e26-227">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-227">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="b8e26-228">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="b8e26-228">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e26-229">Browser Optionen: Internet Explorer 8, Internet Explorer 9 und Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="b8e26-229">Browser options: Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-230">Favoriten, Startseite, Tabstopps und Symbolleisten.</span><span class="sxs-lookup"><span data-stu-id="b8e26-230">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b8e26-231">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-231">Note</span></span></strong><br/><p><span data-ttu-id="b8e26-232">UE-V führt keine Roaming-Einstellungen für Internet Explorer-Cookies durch.</span><span class="sxs-lookup"><span data-stu-id="b8e26-232">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e26-233">Windows-Zubehör</span><span class="sxs-lookup"><span data-stu-id="b8e26-233">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-234">Microsoft Calculator, Notepad, WordPad.</span><span class="sxs-lookup"><span data-stu-id="b8e26-234">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a><span data-ttu-id="b8e26-235">Standardmäßige Synchronisierung von Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-235">Windows settings synchronized by default</span></span>

<span data-ttu-id="b8e26-236">UE-V enthält Einstellungen für Standort Vorlagen, mit denen die Einstellungswerte für diese Windows-Einstellungen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-236">UE-V includes settings location templates that capture settings values for these Windows settings.</span></span>

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
<th align="left"><span data-ttu-id="b8e26-237">Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-237">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="b8e26-238">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8e26-238">Description</span></span></th>
<th align="left"><span data-ttu-id="b8e26-239">Anwenden auf</span><span class="sxs-lookup"><span data-stu-id="b8e26-239">Apply on</span></span></th>
<th align="left"><span data-ttu-id="b8e26-240">Exportieren auf</span><span class="sxs-lookup"><span data-stu-id="b8e26-240">Export on</span></span></th>
<th align="left"><span data-ttu-id="b8e26-241">Standardzustand</span><span class="sxs-lookup"><span data-stu-id="b8e26-241">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e26-242">Desktophintergrund</span><span class="sxs-lookup"><span data-stu-id="b8e26-242">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-243">Derzeit aktiver Desktop Hintergrund oder Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="b8e26-243">Currently active desktop background or wallpaper.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-244">Anmelden, entsperren, Remoteverbindung, geplante Aufgaben Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b8e26-244">Logon, unlock, remote connect, Scheduled Task events.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-245">Abmelden, sperren, Remote Trennung, Benutzer: <strong> jetzt </strong> im Unternehmenseinstellungen-Center auf "synchronisieren" klicken oder Intervall für geplante Aufgaben</span><span class="sxs-lookup"><span data-stu-id="b8e26-245">Logoff, lock, remote disconnect, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-246">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b8e26-246">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e26-247">Erleichterte Bedienung</span><span class="sxs-lookup"><span data-stu-id="b8e26-247">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-248">Barrierefreiheits-und Eingabeeinstellungen, Microsoft-Bildschirmlupe, Sprachausgabe und Bildschirmtastatur.</span><span class="sxs-lookup"><span data-stu-id="b8e26-248">Accessibility and input settings, Microsoft Magnifier, Narrator, and on-Screen Keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-249">Nur Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="b8e26-249">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-250">Abmelden, Benutzer klickt <strong> jetzt </strong> im Unternehmenseinstellungen-Center auf "synchronisieren" oder geplantes Aufgaben Intervall</span><span class="sxs-lookup"><span data-stu-id="b8e26-250">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-251">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b8e26-251">Enabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e26-252">Desktop Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-252">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-253">Startmenü-und Taskleisteneinstellungen, Ordneroptionen, Standard Desktopsymbole, zusätzliche Uhren sowie Regions-und Spracheinstellungen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-253">Start menu and Taskbar settings, Folder options, Default desktop icons, Additional clocks, and Region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-254">Nur Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="b8e26-254">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-255">Abmelden, Benutzer klickt <strong> jetzt </strong> im Unternehmenseinstellungen-Center auf "synchronisieren" oder geplanter Vorgang</span><span class="sxs-lookup"><span data-stu-id="b8e26-255">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-256">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b8e26-256">Enabled</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="b8e26-257">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-257">Note</span></span>**  
<span data-ttu-id="b8e26-258">Ab Windows 8 durchlaufen UE-V keine Einstellungen, die sich auf den Start Bildschirm beziehen, beispielsweise Elemente und Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="b8e26-258">Starting in Windows 8, UE-V does not roam settings related to the Start screen, such as items and locations.</span></span> <span data-ttu-id="b8e26-259">Darüber hinaus unterstützt UE-V keine Synchronisierung von angehefteten Taskleisten Elementen oder Windows-Dateiverknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-259">In addition, UE-V does not support synchronization of pinned taskbar items or Windows file shortcuts.</span></span>



**<span data-ttu-id="b8e26-260">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b8e26-260">Important</span></span>**  
<span data-ttu-id="b8e26-261">UE-V 2,1 SP1 durchstreift die Taskleisteneinstellungen zwischen Windows 10-Geräten.</span><span class="sxs-lookup"><span data-stu-id="b8e26-261">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="b8e26-262">UE-V synchronisiert jedoch keine Taskleisteneinstellungen zwischen Windows 10-Geräten und Geräten, auf denen frühere Betriebssysteme ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-262">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8e26-263">Einstellungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b8e26-263">Settings group</span></span></th>
<th align="left"><span data-ttu-id="b8e26-264">Kategorie</span><span class="sxs-lookup"><span data-stu-id="b8e26-264">Category</span></span></th>
<th align="left"><span data-ttu-id="b8e26-265">Erfassen</span><span class="sxs-lookup"><span data-stu-id="b8e26-265">Capture</span></span></th>
<th align="left"><span data-ttu-id="b8e26-266">„Anwenden“</span><span class="sxs-lookup"><span data-stu-id="b8e26-266">Apply</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b8e26-267">Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-267">Application Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b8e26-268">Windows-Apps  </span><span class="sxs-lookup"><span data-stu-id="b8e26-268">Windows apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-269">APP schließen</span><span class="sxs-lookup"><span data-stu-id="b8e26-269">Close app</span></span></p>
<p><span data-ttu-id="b8e26-270">Change-Ereignis für Windows-App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-270">Windows app settings change event</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-271">Starten des UE-V-App-Monitors beim Start</span><span class="sxs-lookup"><span data-stu-id="b8e26-271">Start the UE-V App Monitor at startup</span></span></p>
<p><span data-ttu-id="b8e26-272">APP öffnen</span><span class="sxs-lookup"><span data-stu-id="b8e26-272">Open app</span></span></p>
<p><span data-ttu-id="b8e26-273">Change-Ereignis für Windows-App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-273">Windows App Settings change event</span></span></p>
<p><span data-ttu-id="b8e26-274">Eintreffen eines Einstellungs Pakets</span><span class="sxs-lookup"><span data-stu-id="b8e26-274">Arrival of a settings package</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b8e26-275">Desktopanwendungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-275">Desktop applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-276">Anwendung wird geschlossen</span><span class="sxs-lookup"><span data-stu-id="b8e26-276">Application closes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-277">Anwendung wird geöffnet und geschlossen</span><span class="sxs-lookup"><span data-stu-id="b8e26-277">Application opens and closes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b8e26-278">Desktop Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-278">Desktop settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b8e26-279">Desktophintergrund</span><span class="sxs-lookup"><span data-stu-id="b8e26-279">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-280">Sperren oder abmelden</span><span class="sxs-lookup"><span data-stu-id="b8e26-280">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-281">Logon, entsperren, Remote Connect, Benachrichtigung über die Ankunft des neuen Pakets, Benutzer klickt <strong> jetzt </strong> im Unternehmenseinstellungen Center auf "synchronisieren" oder geplanter Task wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8e26-281">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b8e26-282">Erleichterte Bedienung (häufig – Barrierefreiheit, Sprachausgabe, Bildschirmlupe, Bildschirmtastatur)</span><span class="sxs-lookup"><span data-stu-id="b8e26-282">Ease of Access (Common – Accessibility, Narrator, Magnifier, On-Screen-Keyboard)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-283">Sperren oder abmelden</span><span class="sxs-lookup"><span data-stu-id="b8e26-283">Lock or Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-284">Anmelde</span><span class="sxs-lookup"><span data-stu-id="b8e26-284">Logon</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b8e26-285">Erleichterte Bedienung (Shell-Audio, Barrierefreiheit, Tastatur, Maus)</span><span class="sxs-lookup"><span data-stu-id="b8e26-285">Ease of Access (Shell - Audio, Accessibility, Keyboard, Mouse)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-286">Sperren oder abmelden</span><span class="sxs-lookup"><span data-stu-id="b8e26-286">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-287">Anmelden, entsperren, Remoteverbindung, Benachrichtigung über das Eintreffen neuer Pakete, Benutzer klickt <strong> auf "Jetzt synchronisieren" </strong> im Unternehmenseinstellungen-Center oder geplante Task-Läufe</span><span class="sxs-lookup"><span data-stu-id="b8e26-287">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b8e26-288">Desktop Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-288">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-289">Sperren oder abmelden</span><span class="sxs-lookup"><span data-stu-id="b8e26-289">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-290">Anmelde</span><span class="sxs-lookup"><span data-stu-id="b8e26-290">Logon</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="b8e26-291">UE-V – Unterstützung für Windows-apps</span><span class="sxs-lookup"><span data-stu-id="b8e26-291">UE-V-support for Windows Apps</span></span>

<span data-ttu-id="b8e26-292">Für Windows-apps gibt der App-Entwickler die Einstellungen an, die synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-292">For Windows apps, the app developer specifies the settings that are synchronized.</span></span> <span data-ttu-id="b8e26-293">Sie können angeben, welche Windows-Apps für die Synchronisierung von Einstellungen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="b8e26-293">You can specify which Windows apps are enabled for settings synchronization.</span></span>

<span data-ttu-id="b8e26-294">Um eine Liste der Windows-apps anzuzeigen, die die Einstellungen auf einem Computer mit dem Namen der paketfamilie, dem aktivierten Status und der aktivierten Quelle synchronisieren können, geben Sie an einer Windows PowerShell-Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="b8e26-294">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="b8e26-295">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-295">Note</span></span>**  
<span data-ttu-id="b8e26-296">Ab Windows 8 synchronisiert UE-V keine Windows-App-Einstellungen, wenn der Domänenbenutzer seine Anmeldeinformationen mit seinem Microsoft-Konto verknüpft.</span><span class="sxs-lookup"><span data-stu-id="b8e26-296">As of Windows 8, UE-V does not synchronize Windows app settings if the domain user links their sign-in credentials to their Microsoft Account.</span></span> <span data-ttu-id="b8e26-297">Diese Verknüpfung synchronisiert Einstellungen mit Microsoft OneDrive so UE-V, wodurch die Synchronisierung der Windows-App-Einstellungen deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="b8e26-297">This linking synchronizes settings to Microsoft OneDrive so UE-V, which disables synchronization of Windows app settings.</span></span>



### <span data-ttu-id="b8e26-298">UE-V-Unterstützung für Roaming-Drucker</span><span class="sxs-lookup"><span data-stu-id="b8e26-298">UE-V-support for Roaming Printers</span></span>

<span data-ttu-id="b8e26-299">Mit UE-V 2,1 SP1 können Netzwerkdrucker zwischen Geräten Roaming durchlaufen, damit ein Benutzer auf seine Netzwerkdrucker zugreifen kann, wenn er sich bei einem beliebigen Gerät im Netzwerk anmeldet.</span><span class="sxs-lookup"><span data-stu-id="b8e26-299">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="b8e26-300">Dies umfasst das Roaming des Druckers, den Sie als Standard festlegen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-300">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="b8e26-301">Für das Drucker-Roaming in UE-V ist eines der folgenden Szenarien erforderlich:</span><span class="sxs-lookup"><span data-stu-id="b8e26-301">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="b8e26-302">Der Druckserver kann den erforderlichen Treiber herunterladen, wenn er auf ein neues Gerät wechselt.</span><span class="sxs-lookup"><span data-stu-id="b8e26-302">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="b8e26-303">Der Treiber für den Roaming-Netzwerkdrucker ist auf allen Geräten vorinstalliert, die auf diesen Netzwerkdrucker zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-303">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="b8e26-304">Der Druckertreiber kann über Windows Update abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-304">The printer driver can be obtained from Windows Update.</span></span>

**<span data-ttu-id="b8e26-305">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-305">Note</span></span>**  
<span data-ttu-id="b8e26-306">Das UE-V Printer-Roaming-Feature unterstützt **keine** Druckereinstellungen oder-Einstellungen, beispielsweise das doppelseitige Drucken.</span><span class="sxs-lookup"><span data-stu-id="b8e26-306">The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>



### <a href="" id="determinesettingssync"></a><span data-ttu-id="b8e26-307">Ermitteln, ob Einstellungen für andere Anwendungen synchronisiert werden müssen</span><span class="sxs-lookup"><span data-stu-id="b8e26-307">Determine whether you need settings synchronized for other applications</span></span>

<span data-ttu-id="b8e26-308">Nachdem Sie die Einstellungen überprüft haben, die automatisch in einer UE-v-Bereitstellung synchronisiert werden, möchten Sie entscheiden, ob Sie die Einstellungen für andere Anwendungen synchronisieren, da dadurch festgelegt wird, wie Sie UE-v im gesamten Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-308">After you have reviewed the settings that are synchronized automatically in a UE-V deployment, you want to decide whether you will synchronize settings for other applications since this determines how you deploy UE-V throughout your enterprise.</span></span>

<span data-ttu-id="b8e26-309">Wenn Sie als Administrator berücksichtigen, welche Desktopanwendungen in Ihre UE-V-Lösung einbezogen werden sollen, sollten Sie berücksichtigen, welche Einstellungen von Benutzern angepasst werden können und wie und wo die Anwendung die Einstellungen speichert.</span><span class="sxs-lookup"><span data-stu-id="b8e26-309">As an administrator, when you consider which desktop applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="b8e26-310">Nicht alle Desktopanwendungen verfügen über Einstellungen, die angepasst oder regelmäßig von Benutzern angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="b8e26-310">Not all desktop applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="b8e26-311">Darüber hinaus können nicht alle Desktopanwendungen-Einstellungen sicher über mehrere Computer oder Umgebungen synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-311">In addition, not all desktop applications settings can safely be synchronized across multiple computers or environments.</span></span>

<span data-ttu-id="b8e26-312">Im Allgemeinen können Sie Einstellungen synchronisieren, die den folgenden Kriterien entsprechen:</span><span class="sxs-lookup"><span data-stu-id="b8e26-312">In general, you can synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="b8e26-313">Einstellungen, die in Benutzer zugänglichen Speicherorten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b8e26-313">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="b8e26-314">Synchronisieren Sie beispielsweise nicht die Einstellungen, die in System32 oder außerhalb des HKEY \ _CURRENT \ _User (HKCU)-Abschnitts der Registrierung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b8e26-314">For example, do not synchronize settings that are stored in System32 or outside the HKEY\_CURRENT\_USER (HKCU) section of the registry.</span></span>

-   <span data-ttu-id="b8e26-315">Einstellungen, die nicht für den jeweiligen Computer spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="b8e26-315">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="b8e26-316">Schließen Sie beispielsweise Netzwerk-oder Hardwarekonfigurationen aus.</span><span class="sxs-lookup"><span data-stu-id="b8e26-316">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="b8e26-317">Einstellungen, die zwischen Computern synchronisiert werden können, ohne dass ein Risiko für beschädigte Daten besteht.</span><span class="sxs-lookup"><span data-stu-id="b8e26-317">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="b8e26-318">Verwenden Sie beispielsweise keine Einstellungen, die in einer Datenbankdatei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b8e26-318">For example, do not use settings that are stored in a database file.</span></span>

### <a href="" id="checklistsettingssync"></a><span data-ttu-id="b8e26-319">Prüfliste für die Auswertung benutzerdefinierter Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-319">Checklist for evaluating custom applications</span></span>

<span data-ttu-id="b8e26-320">Wenn Sie sich für die Synchronisierung von Einstellungen für andere Anwendungen entschieden haben, können Sie anhand dieser Checkliste ermitteln, welche Anwendungen Sie aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-320">If you’ve decided that you need settings synchronized for other applications, you can use this checklist to help figure out which applications you’ll include.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="b8e26-321">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8e26-321">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="b8e26-322">Enthält diese Anwendung Einstellungen, die vom Benutzer angepasst werden können?</span><span class="sxs-lookup"><span data-stu-id="b8e26-322">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="b8e26-323">Ist es für den Benutzer wichtig, dass diese Einstellungen synchronisiert werden?</span><span class="sxs-lookup"><span data-stu-id="b8e26-323">Is it important for the user that these settings are synchronized?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="b8e26-324">Werden diese Benutzereinstellungen bereits von einer Anwendungs Verwaltungs-oder Einstellungsrichtlinien Lösung verwaltet?</span><span class="sxs-lookup"><span data-stu-id="b8e26-324">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="b8e26-325">UE-V wendet Anwendungseinstellungen beim Start von Anwendungen und Windows-Einstellungen bei Anmeldung, entsperren oder Remote Verbindungsereignissen an.</span><span class="sxs-lookup"><span data-stu-id="b8e26-325">UE-V applies application settings at application startup and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="b8e26-326">Wenn Sie UE-V mit anderen Lösungen für die Freigabe von Einstellungen verwenden, können Benutzer in synchronisierten Einstellungen Inkonsistenzen erfahren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-326">If you use UE-V with other settings sharing solutions, users might experience inconsistency across synchronized settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="b8e26-327">Sind die Anwendungseinstellungen für den Computer spezifisch?</span><span class="sxs-lookup"><span data-stu-id="b8e26-327">Are the application settings specific to the computer?</span></span> <span data-ttu-id="b8e26-328">Anwendungseinstellungen und Anpassungen, die Hardware oder bestimmten Computerkonfigurationen zugeordnet sind, werden nicht konsistent zwischen Sitzungen synchronisiert und können zu einer unzureichenden Anwendungsumgebung führen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-328">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently synchronize across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="b8e26-329">Speichert die Anwendung die Einstellungen im Verzeichnis "Programmdateien" oder im Dateiverzeichnis, das sich im <strong> Verzeichnis Benutzer </strong> [Benutzername] &lt; Strong &gt; AppData </strong> &lt; Strong &gt; LocalLow befindet </strong> ?</span><span class="sxs-lookup"><span data-stu-id="b8e26-329">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong>[User name]&lt;strong&gt;AppData</strong>&lt;strong&gt;LocalLow</strong> directory?</span></span> <span data-ttu-id="b8e26-330">Anwendungsdaten, die an einem dieser Speicherorte gespeichert sind, sollten normalerweise nicht mit dem Benutzer synchronisiert werden, da diese Daten für den Computer spezifisch sind oder weil die Daten für die Synchronisierung zu groß sind.</span><span class="sxs-lookup"><span data-stu-id="b8e26-330">Application data that is stored in either of these locations usually should not synchronize with the user, because this data is specific to the computer or because the data is too large to synchronize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="b8e26-331">Speichert die Anwendung alle Einstellungen in einer Datei, die andere Anwendungsdaten enthält, die nicht synchronisiert werden sollen?</span><span class="sxs-lookup"><span data-stu-id="b8e26-331">Does the application store any settings in a file that contains other application data that should not synchronize?</span></span> <span data-ttu-id="b8e26-332">UE-V synchronisiert Dateien als einzelne Einheit.</span><span class="sxs-lookup"><span data-stu-id="b8e26-332">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="b8e26-333">Wenn Einstellungen in Dateien gespeichert werden, die Anwendungsdaten außer Einstellungen enthalten, kann das Synchronisieren dieser zusätzlichen Daten zu einer unzureichenden Anwendungsumgebung führen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-333">If settings are stored in files that include application data other than settings, then synchronizing this additional data can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="b8e26-334">Wie groß sind die Dateien, die die Einstellungen enthalten?</span><span class="sxs-lookup"><span data-stu-id="b8e26-334">How large are the files that contain the settings?</span></span> <span data-ttu-id="b8e26-335">Die Leistung der Synchronisierung von Einstellungen kann von umfangreichen Dateien beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-335">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="b8e26-336">Das einbeziehen großer Dateien kann sich auf die Leistung der Synchronisierung von Einstellungen auswirken.</span><span class="sxs-lookup"><span data-stu-id="b8e26-336">Including large files can affect the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a><span data-ttu-id="b8e26-337">Weitere Überlegungen beim Vorbereiten einer UE-V-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="b8e26-337">Other Considerations when Preparing a UE-V Deployment</span></span>


<span data-ttu-id="b8e26-338">Sie sollten diese Aspekte auch berücksichtigen, wenn Sie die Bereitstellung von UE-V vorbereiten:</span><span class="sxs-lookup"><span data-stu-id="b8e26-338">You should also consider these things when you are preparing to deploy UE-V:</span></span>

-   [<span data-ttu-id="b8e26-339">Verwalten der Anmeldeinformationen-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="b8e26-339">Managing credentials synchronization</span></span>](#creds)

-   [<span data-ttu-id="b8e26-340">Synchronisierung der Windows-App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-340">Windows app settings synchronization</span></span>](#appxsettings)

-   [<span data-ttu-id="b8e26-341">Benutzerdefinierte Standort Vorlagen für UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-341">Custom UE-V settings location templates</span></span>](#custom)

-   [<span data-ttu-id="b8e26-342">Unbeabsichtigte Konfigurationen für Benutzereinstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-342">Unintentional user settings configurations</span></span>](#prevent)

-   [<span data-ttu-id="b8e26-343">Leistung und Kapazität</span><span class="sxs-lookup"><span data-stu-id="b8e26-343">Performance and capacity</span></span>](#capacity)

-   [<span data-ttu-id="b8e26-344">Hohe Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="b8e26-344">High availability</span></span>](#high)

-   [<span data-ttu-id="b8e26-345">Synchronisierung des Computer Takts</span><span class="sxs-lookup"><span data-stu-id="b8e26-345">Computer clock synchronization</span></span>](#clocksync)

### <a href="" id="creds"></a><span data-ttu-id="b8e26-346">Verwalten der Anmeldeinformationen für die Synchronisierung in UE-v 2,1 und UE-v 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="b8e26-346">Managing credentials synchronization in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="b8e26-347">Viele Enterprise-Anwendungen, einschließlich Microsoft Outlook und lync, fordern Benutzer bei der Anmeldung zur Eingabe Ihrer Domänenanmeldeinformationen auf.</span><span class="sxs-lookup"><span data-stu-id="b8e26-347">Many enterprise applications, including Microsoft Outlook and Lync, prompt users for their domain credentials at login.</span></span> <span data-ttu-id="b8e26-348">Benutzer haben die Möglichkeit, Ihre Anmeldeinformationen auf einem Datenträger zu speichern, um zu verhindern, dass Sie bei jedem Öffnen dieser Anwendungen eingegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-348">Users have the option of saving their credentials to disk to prevent having to enter them every time they open these applications.</span></span> <span data-ttu-id="b8e26-349">Durch das Aktivieren der Synchronisierung von Roaming-Anmeldeinformationen können Benutzer ihre Anmeldeinformationen auf einem Computer speichern und Sie nicht auf jedem Computer, den Sie in Ihrer Umgebung verwenden, erneut eingeben.</span><span class="sxs-lookup"><span data-stu-id="b8e26-349">Enabling roaming credentials synchronization lets users save their credentials on one computer and avoid re-entering them on every computer they use in their environment.</span></span> <span data-ttu-id="b8e26-350">Benutzer können einige Domänenanmeldeinformationen mit UE-V 2,1 und 2,1 SP1 synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-350">Users can synchronize some domain credentials with UE-V 2.1 and 2.1 SP1.</span></span>

**<span data-ttu-id="b8e26-351">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b8e26-351">Important</span></span>**  
<span data-ttu-id="b8e26-352">Die Synchronisierung der Anmeldeinformationen ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8e26-352">Credentials synchronization is disabled by default.</span></span> <span data-ttu-id="b8e26-353">Sie müssen die Anmeldeinformationen-Synchronisierung während der Bereitstellung explizit aktivieren, um dieses Feature zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-353">You must explicitly enable credentials synchronization during deployment to implement this feature.</span></span>



<span data-ttu-id="b8e26-354">UE-V 2,1 und 2,1 SP1 können Enterprise-Anmeldeinformationen synchronisieren, jedoch keine Roaming-Anmeldeinformationen, die nur für die Verwendung auf dem lokalen Computer vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="b8e26-354">UE-V 2.1 and 2.1 SP1 can synchronize enterprise credentials, but do not roam credentials intended only for use on the local computer.</span></span>

<span data-ttu-id="b8e26-355">Anmeldeinformationen sind synchrone Einstellungen, was bedeutet, dass Sie bei der ersten Anmeldung an Ihrem Computer nach UE-V synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-355">Credentials are synchronous settings, meaning they are applied to your profile the first time you log in to your computer after UE-V synchronizes.</span></span>

<span data-ttu-id="b8e26-356">Die Synchronisierung der Anmeldeinformationen wird durch eine eigene Einstellungen-Speicherort Vorlage verwaltet, die standardmäßig deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b8e26-356">Credentials synchronization is managed by its own settings location template, which is disabled by default.</span></span> <span data-ttu-id="b8e26-357">Sie können diese Vorlage über die für andere Vorlagen verwendeten Methoden aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-357">You can enable or disable this template through the same methods used for other templates.</span></span> <span data-ttu-id="b8e26-358">Der Vorlagenbezeichner für dieses Feature lautet RoamingCredentialSettings.</span><span class="sxs-lookup"><span data-stu-id="b8e26-358">The template identifier for this feature is RoamingCredentialSettings.</span></span>

**<span data-ttu-id="b8e26-359">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b8e26-359">Important</span></span>**  
<span data-ttu-id="b8e26-360">Wenn Sie das Roaming von Active Directory-Anmeldeinformationen in Ihrer Umgebung verwenden, empfiehlt es sich, die Vorlage für die Roaming-Anmeldeinformationen in UE-V nicht zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-360">If you are using Active Directory Credential Roaming in your environment, we recommend that you don’t enable the UE-V credential roaming template.</span></span>



<span data-ttu-id="b8e26-361">Verwenden Sie eine der folgenden Methoden, um die Synchronisierung der Anmeldeinformationen zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="b8e26-361">Use one of these methods to enable credentials synchronization:</span></span>

-   <span data-ttu-id="b8e26-362">Unternehmenseinstellungen (Center)</span><span class="sxs-lookup"><span data-stu-id="b8e26-362">Company Settings Center</span></span>

-   <span data-ttu-id="b8e26-363">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8e26-363">PowerShell</span></span>

-   <span data-ttu-id="b8e26-364">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b8e26-364">Group Policy</span></span>

**<span data-ttu-id="b8e26-365">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-365">Note</span></span>**  
<span data-ttu-id="b8e26-366">Anmeldeinformationen werden während der Synchronisierung verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="b8e26-366">Credentials are encrypted during synchronization.</span></span>



<span data-ttu-id="b8e26-367">[Unternehmens Einstellungs Center](https://technet.microsoft.com/library/dn458903.aspx)**:** aktivieren Sie das Kontrollkästchen Einstellungen für Roaming-Anmeldeinformationen unter Windows-Einstellungen, um die Synchronisierung der Anmeldeinformationen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-367">[Company Settings Center](https://technet.microsoft.com/library/dn458903.aspx)**:** Check the Roaming Credential Settings check box under Windows Settings to enable credential synchronization.</span></span> <span data-ttu-id="b8e26-368">Deaktivieren Sie das Kontrollkästchen, um es zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-368">Uncheck the box to disable it.</span></span> <span data-ttu-id="b8e26-369">Dieses Kontrollkästchen wird nur im Unternehmenseinstellungen-Center angezeigt, wenn Ihr Konto nicht so konfiguriert ist, dass die Einstellungen mit einem Microsoft-Konto synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-369">This check box only appears in Company Settings Center if your account is not configured to synchronize settings using a Microsoft Account.</span></span>

<span data-ttu-id="b8e26-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** dieses PowerShell-Cmdlet ermöglicht die Synchronisierung von Anmeldeinformationen:</span><span class="sxs-lookup"><span data-stu-id="b8e26-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** This PowerShell cmdlet enables credential synchronization:</span></span>

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="b8e26-371">Dieses PowerShell-Cmdlet deaktiviert die Synchronisierung von Anmeldeinformationen:</span><span class="sxs-lookup"><span data-stu-id="b8e26-371">This PowerShell cmdlet disables credential synchronization:</span></span>

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="b8e26-372">[Gruppenrichtlinie](https://technet.microsoft.com/library/dn458893.aspx)**:** Sie müssen [die neueste MDOP-ADMX-Vorlage bereitstellen](https://go.microsoft.com/fwlink/p/?LinkId=393944) , um die Synchronisierung von Anmeldeinformationen über Gruppenrichtlinien zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-372">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You must [deploy the latest MDOP ADMX template](https://go.microsoft.com/fwlink/p/?LinkId=393944) to enable credential synchronization through group policy.</span></span> <span data-ttu-id="b8e26-373">Die Synchronisierung der Anmeldeinformationen wird mit den Windows-Einstellungen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b8e26-373">Credentials synchronization is managed with the Windows settings.</span></span> <span data-ttu-id="b8e26-374">Wenn Sie dieses Feature mit Gruppenrichtlinien verwalten möchten, aktivieren Sie die Richtlinie Windows-Einstellungen synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-374">To manage this feature with Group Policy, enable the Synchronize Windows settings policy.</span></span>

1.  <span data-ttu-id="b8e26-375">Öffnen Sie den Gruppenrichtlinien-Editor, und navigieren Sie zu **Benutzerkonfiguration – Administrative Vorlagen – Windows-Komponenten – Microsoft User Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="b8e26-375">Open Group Policy Editor and navigate to **User Configuration – Administrative Templates – Windows Components – Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="b8e26-376">Doppelklicken Sie auf **Windows-Einstellungen synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="b8e26-376">Double-click on **Synchronize Windows settings**.</span></span>

3.  <span data-ttu-id="b8e26-377">Wenn diese Richtlinie aktiviert ist, können Sie die Synchronisierung der Anmeldeinformationen aktivieren, indem Sie das Kontrollkästchen **Roaming-Anmeldeinformationen** aktivieren, oder die Synchronisierung von Anmeldeinformationen deaktivieren, indem Sie Sie deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-377">If this policy is enabled, you can enable credentials synchronization by checking the **Roaming Credentials** check box, or disable credentials synchronization by unchecking it.</span></span>

4.  <span data-ttu-id="b8e26-378">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e26-378">Click **OK**.</span></span>

### <span data-ttu-id="b8e26-379">Von UE-V synchronisierte Speicherorte für Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="b8e26-379">Credential locations synchronized by UE-V</span></span>

<span data-ttu-id="b8e26-380">Von Anwendungen gespeicherte Anmeldeinformationsdateien an den folgenden Speicherorten werden synchronisiert:</span><span class="sxs-lookup"><span data-stu-id="b8e26-380">Credential files saved by applications into the following locations are synchronized:</span></span>

-   <span data-ttu-id="b8e26-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span><span class="sxs-lookup"><span data-stu-id="b8e26-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span></span>\\

-   <span data-ttu-id="b8e26-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span><span class="sxs-lookup"><span data-stu-id="b8e26-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span></span>\\

-   <span data-ttu-id="b8e26-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span><span class="sxs-lookup"><span data-stu-id="b8e26-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span></span>\\

-   <span data-ttu-id="b8e26-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span><span class="sxs-lookup"><span data-stu-id="b8e26-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span></span>\\

<span data-ttu-id="b8e26-385">An anderen Speicherorten gespeicherte Anmeldeinformationen werden nicht von UE-V synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="b8e26-385">Credentials saved to other locations are not synchronized by UE-V.</span></span>

### <a href="" id="appxsettings"></a><span data-ttu-id="b8e26-386">Synchronisierung der Windows-App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-386">Windows app settings synchronization</span></span>

<span data-ttu-id="b8e26-387">UE-V verwaltet die Synchronisierung der Windows-App-Einstellungen auf drei Arten:</span><span class="sxs-lookup"><span data-stu-id="b8e26-387">UE-V manages Windows app settings synchronization in three ways:</span></span>

-   <span data-ttu-id="b8e26-388">**Synchronisieren von Windows-apps:** Zulassen oder Verweigern einer Windows-App-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="b8e26-388">**Sync Windows Apps:** Allow or deny any Windows app synchronization</span></span>

-   <span data-ttu-id="b8e26-389">**Windows-App-Liste:** Synchronisieren einer Liste von Windows-apps</span><span class="sxs-lookup"><span data-stu-id="b8e26-389">**Windows App List:** Synchronize a list of Windows apps</span></span>

-   <span data-ttu-id="b8e26-390">Nicht **aufgelistetes Standard Synchronisierungsverhalten:** Bestimmen Sie das Synchronisierungsverhalten von Windows-apps, die nicht in der Windows-App-Liste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b8e26-390">**Unlisted Default Sync Behavior:** Determine the synchronization behavior of Windows apps that are not in the Windows app list.</span></span>

<span data-ttu-id="b8e26-391">Weitere Informationen finden Sie in der [Windows-App-Liste](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="b8e26-391">For more information, see the [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

### <a href="" id="custom"></a><span data-ttu-id="b8e26-392">Benutzerdefinierte Standort Vorlagen für UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-392">Custom UE-V settings location templates</span></span>

<span data-ttu-id="b8e26-393">Wenn Sie UE-v zum Synchronisieren von Einstellungen für benutzerdefinierte Anwendungen bereitstellen, verwenden Sie den UE-v-Generator, um benutzerdefinierte Speicherort Vorlagen für diese Desktopanwendungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-393">If you are deploying UE-V to synchronize settings for custom applications, you will use the UE-V Generator to create custom settings location templates for those desktop applications.</span></span> <span data-ttu-id="b8e26-394">Nachdem Sie eine Standort Vorlage für benutzerdefinierte Einstellungen in einer Testumgebung erstellt und getestet haben, können Sie die Einstellungen-Speicherort Vorlagen auf Computern im Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-394">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="b8e26-395">Speicherort Vorlagen für benutzerdefinierte Einstellungen müssen mit einer vorhandenen Bereitstellungsinfrastruktur bereitgestellt werden, wie eine ESD-Methode (Enterprise Software Distribution) wie System Center Configuration Manager, mit Einstellungen oder durch Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs.</span><span class="sxs-lookup"><span data-stu-id="b8e26-395">Custom settings location templates must be deployed with an existing deployment infrastructure, like an enterprise software distribution (ESD) method such as System Center Configuration Manager, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="b8e26-396">Vorlagen, die mit Configuration Manager oder Gruppenrichtlinien bereitgestellt werden, müssen mit UE-V WMI oder Windows PowerShell registriert werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-396">Templates that are deployed with Configuration Manager or Group Policy must be registered by using UE-V WMI or Windows PowerShell.</span></span>

<span data-ttu-id="b8e26-397">Weitere Informationen zu den Standort Vorlagen für benutzerdefinierte Einstellungen finden Sie unter [Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="b8e26-397">For more information about custom settings location templates, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span> <span data-ttu-id="b8e26-398">Weitere Informationen zur Verwendung von UE-v mit Configuration Manager finden Sie unter [Konfigurieren von UE-v 2. x mit System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="b8e26-398">For more information about using UE-V with Configuration Manager, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

### <a href="" id="prevent"></a><span data-ttu-id="b8e26-399">Verhindern der unbeabsichtigten Konfiguration von Benutzereinstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-399">Prevent unintentional user settings configuration</span></span>

<span data-ttu-id="b8e26-400">UE-V downloadet neue Benutzereinstellungsinformationen von einem Einstellungs Speicherort und wendet die Einstellungen in diesen Fällen auf den lokalen Computer an:</span><span class="sxs-lookup"><span data-stu-id="b8e26-400">UE-V downloads new user settings information from a settings storage location and applies the settings to the local computer in these instances:</span></span>

-   <span data-ttu-id="b8e26-401">Jedes Mal, wenn eine Anwendung gestartet wird, die über eine registrierte UE-V-Vorlage verfügt.</span><span class="sxs-lookup"><span data-stu-id="b8e26-401">Every time an application is started that has a registered UE-V template.</span></span>

-   <span data-ttu-id="b8e26-402">Wenn sich ein Benutzer an einem Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="b8e26-402">When a user logs on to a computer.</span></span>

-   <span data-ttu-id="b8e26-403">Wenn ein Benutzer einen Computer entsperrt.</span><span class="sxs-lookup"><span data-stu-id="b8e26-403">When a user unlocks a computer.</span></span>

-   <span data-ttu-id="b8e26-404">Wenn eine Verbindung mit einem Remote Desktopcomputer hergestellt wird, auf dem UE-V installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b8e26-404">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

-   <span data-ttu-id="b8e26-405">Wenn der geplante Task der Synchronisierungs Controller Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8e26-405">When the Sync Controller Application scheduled task is run.</span></span>

<span data-ttu-id="b8e26-406">Wenn UE-V auf Computer a und Computer B installiert ist und die für die Anwendung gewünschten Einstellungen sich auf Computer a befinden, sollte Computer a die Anwendung zuerst öffnen und schließen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-406">If UE-V is installed on computer A and computer B, and the settings that you want for the application are on computer A, then computer A should open and close the application first.</span></span> <span data-ttu-id="b8e26-407">Wenn die Anwendung zuerst auf Computer b geöffnet und geschlossen wird, werden die Anwendungseinstellungen auf Computer A für die Anwendungseinstellungen auf Computer b konfiguriert. die Einstellungen werden pro Anwendung zwischen Computern synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="b8e26-407">If the application is opened and closed on computer B first, then the application settings on computer A are configured to the application settings on computer B. Settings are synchronized between computers on per-application basis.</span></span> <span data-ttu-id="b8e26-408">Im Laufe der Zeit werden die Einstellungen zwischen Computern konsistent, während Sie mit bevorzugten Einstellungen geöffnet und geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-408">Over time, settings become consistent between computers as they are opened and closed with preferred settings.</span></span>

<span data-ttu-id="b8e26-409">Dieses Szenario gilt auch für Windows-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-409">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="b8e26-410">Wenn die Windows-Einstellungen auf Computer B mit den Windows-Einstellungen auf Computer a identisch sein sollten, sollte sich der Benutzer zuerst anmelden und den Computer abmelden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-410">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should log on and log off computer A first.</span></span>

<span data-ttu-id="b8e26-411">Wenn die Benutzereinstellungen, die der Benutzer wünscht, in der falschen Reihenfolge angewendet werden, können Sie wiederhergestellt werden, indem Sie einen Wiederherstellungsvorgang für die jeweilige Anwendung oder Windows-Konfiguration auf dem Computer ausführen, auf dem die Einstellungen überschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-411">If the user settings that the user wants are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="b8e26-412">Weitere Informationen finden Sie unter [Verwalten der administrativen Sicherung und Wiederherstellung in UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span><span class="sxs-lookup"><span data-stu-id="b8e26-412">For more information, see [Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span></span>

### <a href="" id="capacity"></a><span data-ttu-id="b8e26-413">Leistungs-und Kapazitätsplanung</span><span class="sxs-lookup"><span data-stu-id="b8e26-413">Performance and capacity planning</span></span>

<span data-ttu-id="b8e26-414">Geben Sie Ihre Anforderungen für UE-V mit Standardfestplatten Kapazität und Netzwerkstatusüberwachung an.</span><span class="sxs-lookup"><span data-stu-id="b8e26-414">Specify your requirements for UE-V with standard disk capacity and network health monitoring.</span></span>

<span data-ttu-id="b8e26-415">UE-V verwendet eine SMB-Freigabe (Server Message Block) für die Speicherung von Einstellungspaketen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-415">UE-V uses a Server Message Block (SMB) share for the storage of settings packages.</span></span> <span data-ttu-id="b8e26-416">Die Größe der Einstellungs Pakete hängt von den Einstellungsinformationen für die einzelnen Anwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="b8e26-416">The size of settings packages varies depending on the settings information for each application.</span></span> <span data-ttu-id="b8e26-417">Während die meisten Einstellungs Pakete klein sind, kann die Synchronisierung von potenziell umfangreichen Dateien, wie etwa Desktop Bildern, zu einer schlechten Leistung führen, insbesondere bei langsameren Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="b8e26-417">While most settings packages are small, the synchronization of potentially large files, such as desktop images, can result in poor performance, particularly on slower networks.</span></span>

<span data-ttu-id="b8e26-418">Wenn Sie Probleme mit der Netzwerklatenz verringern möchten, erstellen Sie die Speicherorte für Einstellungen in den lokalen Netzwerken, in denen sich die Computer der Benutzer befinden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-418">To reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="b8e26-419">Für den Speicherort der Einstellungen empfehlen wir pro Nutzer 20 MB Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="b8e26-419">We recommend 20 MB of disk space per user for the settings storage location.</span></span>

<span data-ttu-id="b8e26-420">Standardmäßig wird die UE-V-Synchronisierung nach 2 Sekunden durchgeführt, um zu hohen Verzögerungen aufgrund eines umfangreichen Einstellungs Pakets zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="b8e26-420">By default, UE-V synchronization times out after 2 seconds to prevent excessive lag due to a large settings package.</span></span> <span data-ttu-id="b8e26-421">Sie können die Einstellung SyncMethod = SyncProvider mithilfe von [Gruppenrichtlinienobjekten](https://technet.microsoft.com/library/dn458893.aspx)konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b8e26-421">You can configure the SyncMethod=SyncProvider setting by using [Group Policy Objects](https://technet.microsoft.com/library/dn458893.aspx).</span></span>

### <a href="" id="high"></a><span data-ttu-id="b8e26-422">Höhere Verfügbarkeit für UE-V</span><span class="sxs-lookup"><span data-stu-id="b8e26-422">High Availability for UE-V</span></span>

<span data-ttu-id="b8e26-423">Der Speicherstandort und der Einstellungs Vorlagenkatalog für UE-V-Einstellungen unterstützen das Speichern von Benutzerdaten auf einer beliebigen schreibbaren Freigabe.</span><span class="sxs-lookup"><span data-stu-id="b8e26-423">The UE-V settings storage location and settings template catalog support storing user data on any writable share.</span></span> <span data-ttu-id="b8e26-424">Führen Sie die folgenden Kriterien aus, um eine höhere Verfügbarkeit zu gewährleisten:</span><span class="sxs-lookup"><span data-stu-id="b8e26-424">To ensure high availability, follow these criteria:</span></span>

-   <span data-ttu-id="b8e26-425">Formatieren Sie das Speichervolume mit einem NTFS-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="b8e26-425">Format the storage volume with an NTFS file system.</span></span>

-   <span data-ttu-id="b8e26-426">Die Freigabe kann Distributed File System (DFS) verwenden, es gibt jedoch Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-426">The share can use Distributed File System (DFS) but there are restrictions.</span></span>
<span data-ttu-id="b8e26-427">Insbesondere wird die verteilte Datei systemreplizierung (DFS-R) mit einer einzelnen Zielkonfiguration mit oder ohne einen verteilten Dateisystem-Namespace (DFS-N) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8e26-427">Specifically, Distributed File System Replication (DFS-R) single target configuration with or without a Distributed File System Namespace (DFS-N) is supported.</span></span>
<span data-ttu-id="b8e26-428">Ebenso wird nur eine Zielkonfiguration mit DFS-N unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8e26-428">Likewise, only single target configuration is supported with DFS-N.</span></span>
<span data-ttu-id="b8e26-429">Detaillierte Informationen finden Sie [in der Microsoft-Support-Anweisung rund um replizierte Benutzerprofildaten](https://go.microsoft.com/fwlink/p/?LinkId=313991) und auch [Informationen zur Microsoft-Supportrichtlinie für ein DFS-R-und DFS-N-Bereitstellungsszenario](https://support.microsoft.com/kb/2533009).</span><span class="sxs-lookup"><span data-stu-id="b8e26-429">For detailed information, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://go.microsoft.com/fwlink/p/?LinkId=313991) and also [Information about Microsoft support policy for a DFS-R and DFS-N deployment scenario](https://support.microsoft.com/kb/2533009).</span></span>

    <span data-ttu-id="b8e26-430">Da SYSVOL auch DFS-R für die Replikation verwendet, kann SYSVOL nicht für die UE-V-Datendatei Replikation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-430">In addition, because SYSVOL uses DFS-R for replication, SYSVOL cannot be used for UE-V data file replication.</span></span>

-   <span data-ttu-id="b8e26-431">Konfigurieren Sie die Freigabeberechtigungen und NTFS-Zugriffssteuerungslisten (ACLs) gemäß [den Angaben unter Bereitstellen des Speicherorts für die Einstellungen für UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span><span class="sxs-lookup"><span data-stu-id="b8e26-431">Configure the share permissions and NTFS access control lists (ACLs) as specified in [Deploying the Settings Storage Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span></span>

-   <span data-ttu-id="b8e26-432">Verwenden Sie das Dateiserver-Clustering zusammen mit dem UE-V-Agent, um den Zugriff auf Kopien von Benutzerzustandsdaten im Falle von Kommunikationsfehlern zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-432">Use file server clustering along with the UE-V Agent to provide access to copies of user state data in the event of communications failures.</span></span>

-   <span data-ttu-id="b8e26-433">Sie können die Einstellungen Speicherpfad Daten (Benutzerdaten) und Vorlagen für Vorlagen für Vorlagen auf gruppierten Freigaben, auf DFS-N-Freigaben oder auf beiden speichern.</span><span class="sxs-lookup"><span data-stu-id="b8e26-433">You can store the settings storage path data (user data) and settings template catalog templates on clustered shares, on DFS-N shares, or on both.</span></span>

### <a href="" id="clocksync"></a><span data-ttu-id="b8e26-434">Synchronisieren von Computeruhren für die Synchronisierung von UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b8e26-434">Synchronize computer clocks for UE-V settings synchronization</span></span>

<span data-ttu-id="b8e26-435">Computer, auf denen der UE-V-Agent ausgeführt wird, müssen einen Zeitserver verwenden, um eine konsistente Einstellungen zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="b8e26-435">Computers that run the UE-V Agent must use a time server to maintain a consistent settings experience.</span></span> <span data-ttu-id="b8e26-436">UE-V verwendet Zeitstempel, um festzustellen, ob die Einstellungen vom Speicherort der Einstellungen synchronisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-436">UE-V uses time stamps to determine if settings must be synchronized from the settings storage location.</span></span> <span data-ttu-id="b8e26-437">Wenn die Uhrzeit des Computers falsch ist, können ältere Einstellungen neuere Einstellungen überschreiben, oder die neuen Einstellungen werden möglicherweise nicht am Speicherort des Einstellungs Speichers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b8e26-437">If the computer clock is inaccurate, older settings can overwrite newer settings, or the new settings might not be saved to the settings storage location.</span></span>

## <a href="" id="prereqs"></a><span data-ttu-id="b8e26-438">Voraussetzungen und unterstützte Konfigurationen für UE-V bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8e26-438">Confirm Prerequisites and Supported Configurations for UE-V</span></span>


<span data-ttu-id="b8e26-439">Bevor Sie fortfahren, stellen Sie sicher, dass Ihre Umgebung die folgenden Voraussetzungen für die Ausführung von UE-V umfasst.</span><span class="sxs-lookup"><span data-stu-id="b8e26-439">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

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
<th align="left"><strong><span data-ttu-id="b8e26-440">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="b8e26-440">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="b8e26-441">Edition</span><span class="sxs-lookup"><span data-stu-id="b8e26-441">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="b8e26-442">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b8e26-442">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="b8e26-443">System Architektur</span><span class="sxs-lookup"><span data-stu-id="b8e26-443">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="b8e26-444">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8e26-444">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="b8e26-445">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="b8e26-445">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e26-446">Windows7</span><span class="sxs-lookup"><span data-stu-id="b8e26-446">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-447">Ultimate-, Enterprise-oder Professional-Edition</span><span class="sxs-lookup"><span data-stu-id="b8e26-447">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-448">SP1</span><span class="sxs-lookup"><span data-stu-id="b8e26-448">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-449">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="b8e26-449">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-450">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8e26-450">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-451">.NET Framework 4,5 oder höher für UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="b8e26-451">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="b8e26-452">.NET Framework 4 oder höher für UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="b8e26-452">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e26-453">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8e26-453">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-454">Standard, Enterprise, Datacenter oder Web Server</span><span class="sxs-lookup"><span data-stu-id="b8e26-454">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-455">SP1</span><span class="sxs-lookup"><span data-stu-id="b8e26-455">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-456">64Bit</span><span class="sxs-lookup"><span data-stu-id="b8e26-456">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-457">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8e26-457">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-458">.NET Framework 4,5 oder höher für UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="b8e26-458">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="b8e26-459">.NET Framework 4 oder höher für UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="b8e26-459">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e26-460">Windows 8 und Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="b8e26-460">Windows 8 and Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-461">Enterprise oder pro</span><span class="sxs-lookup"><span data-stu-id="b8e26-461">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-462">Keine</span><span class="sxs-lookup"><span data-stu-id="b8e26-462">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-463">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="b8e26-463">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-464">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8e26-464">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-465">.NET Framework 4,5 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8e26-465">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e26-466">Windows 10, Version vor 1607</span><span class="sxs-lookup"><span data-stu-id="b8e26-466">Windows 10, pre-1607 version</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b8e26-467">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-467">Note</span></span></strong><br/><p><span data-ttu-id="b8e26-468">Nur UE-V 2,1 SP1 unterstützt Windows 10, Pre-1607-Version</span><span class="sxs-lookup"><span data-stu-id="b8e26-468">Only UE-V 2.1 SP1 supports Windows 10, pre-1607 version</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b8e26-469">Enterprise oder pro</span><span class="sxs-lookup"><span data-stu-id="b8e26-469">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-470">Keine</span><span class="sxs-lookup"><span data-stu-id="b8e26-470">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-471">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="b8e26-471">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-472">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8e26-472">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-473">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="b8e26-473">.NET Framework 4.6</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e26-474">Windows Server 2012 und Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b8e26-474">Windows Server 2012 and Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-475">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="b8e26-475">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-476">Keine</span><span class="sxs-lookup"><span data-stu-id="b8e26-476">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-477">64Bit</span><span class="sxs-lookup"><span data-stu-id="b8e26-477">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-478">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8e26-478">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-479">.NET Framework 4,5 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8e26-479">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e26-480">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b8e26-480">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-481">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="b8e26-481">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-482">Keine</span><span class="sxs-lookup"><span data-stu-id="b8e26-482">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-483">64Bit</span><span class="sxs-lookup"><span data-stu-id="b8e26-483">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-484">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8e26-484">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e26-485">.NET Framework 4,6 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8e26-485">.NET Framework 4.6 or higher</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b8e26-486">Auch...</span><span class="sxs-lookup"><span data-stu-id="b8e26-486">Also…</span></span>

-   <span data-ttu-id="b8e26-487">**MDOP-Lizenz:** Diese Technologie ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="b8e26-487">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="b8e26-488">Unternehmenskunden können MDOP mit Microsoft Software Assurance erhalten.</span><span class="sxs-lookup"><span data-stu-id="b8e26-488">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="b8e26-489">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter wie erhalte ich MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="b8e26-489">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="b8e26-490">**Administratoranmeldeinformationen** für jeden Computer, auf dem die Installation erfolgen soll</span><span class="sxs-lookup"><span data-stu-id="b8e26-490">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

**<span data-ttu-id="b8e26-491">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-491">Note</span></span>**  

-   <span data-ttu-id="b8e26-492">Ab Windows 10, Version 1607, ist UE-V in [Windows 10 für Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) enthalten und nicht mehr Teil des Microsoft-Desktop Optimierungs Pakets.</span><span class="sxs-lookup"><span data-stu-id="b8e26-492">Starting with WIndows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack.</span></span>

-   <span data-ttu-id="b8e26-493">Das Windows PowerShell-Feature UE-v des UE-v-Agents erfordert .NET Framework 4 oder höher und Windows PowerShell 3,0 oder höher, um aktiviert zu werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-493">The UE-V Windows PowerShell feature of the UE-V Agent requires .NET Framework 4 or higher and Windows PowerShell 3.0 or higher to be enabled.</span></span> <span data-ttu-id="b8e26-494">Laden Sie Windows PowerShell 3,0 [hier](https://go.microsoft.com/fwlink/?LinkId=309609)herunter.</span><span class="sxs-lookup"><span data-stu-id="b8e26-494">Download Windows PowerShell 3.0 [here](https://go.microsoft.com/fwlink/?LinkId=309609).</span></span>

-   <span data-ttu-id="b8e26-495">Installieren Sie .NET Framework 4 oder .NET Framework 4,5 auf Computern, auf denen das BetriebssystemWindows 7 oder Windows Server 2008 R2 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8e26-495">Install .NET Framework 4 or .NET Framework 4.5 on computers that run the Windows 7 or the Windows Server 2008 R2 operating system.</span></span> <span data-ttu-id="b8e26-496">Die Betriebssysteme Windows 8, Windows 8,1 und Windows Server 2012 sind mit .NET Framework 4,5 installiert.</span><span class="sxs-lookup"><span data-stu-id="b8e26-496">The Windows 8, Windows 8.1, and Windows Server 2012 operating systems come with .NET Framework 4.5 installed.</span></span> <span data-ttu-id="b8e26-497">Das Betriebssystem Windows 10 ist mit .NET Framework 4,6 installiert.</span><span class="sxs-lookup"><span data-stu-id="b8e26-497">The Windows 10 operating system comes with .NET Framework 4.6 installed.</span></span>
-   <span data-ttu-id="b8e26-498">Die Richtlinie "Roaming-Cache löschen" für obligatorische Profile wird von UE-V nicht unterstützt und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-498">The “Delete Roaming Cache” policy for Mandatory profiles is not supported with UE-V and should not be used.</span></span>



<span data-ttu-id="b8e26-499">Es gibt keine speziellen RAM-Anforderungen (Random Access Memory), die für UE-V spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="b8e26-499">There are no special random access memory (RAM) requirements specific to UE-V.</span></span>

### <span data-ttu-id="b8e26-500">Synchronisierung von Einstellungen über den Synchronisierungsanbieter</span><span class="sxs-lookup"><span data-stu-id="b8e26-500">Synchronization of Settings through the Sync Provider</span></span>

<span data-ttu-id="b8e26-501">Der Synchronisierungsanbieter ist die Standardeinstellung für Benutzer, die einen lokalen Cache mit dem Speicherort für Einstellungen in diesen Instanzen synchronisiert:</span><span class="sxs-lookup"><span data-stu-id="b8e26-501">Sync Provider is the default setting for users, which synchronizes a local cache with the settings storage location in these instances:</span></span>

-   <span data-ttu-id="b8e26-502">Anmelden/Abmelden</span><span class="sxs-lookup"><span data-stu-id="b8e26-502">Logon/logoff</span></span>

-   <span data-ttu-id="b8e26-503">Sperren/Entsperren</span><span class="sxs-lookup"><span data-stu-id="b8e26-503">Lock/unlock</span></span>

-   <span data-ttu-id="b8e26-504">Verbinden/Trennen des Remote Desktops</span><span class="sxs-lookup"><span data-stu-id="b8e26-504">Remote desktop connect/disconnect</span></span>

-   <span data-ttu-id="b8e26-505">Anwendung öffnen/schließen</span><span class="sxs-lookup"><span data-stu-id="b8e26-505">Application open/close</span></span>

<span data-ttu-id="b8e26-506">Ein geplanter Task verwaltet diese Synchronisierung von Einstellungen alle 30 Minuten oder durch bestimmte Trigger-Ereignisse für bestimmte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-506">A scheduled task manages this synchronization of settings every 30 minutes or through certain trigger events for certain applications.</span></span> <span data-ttu-id="b8e26-507">Weitere Informationen finden Sie unter [Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="b8e26-507">For more information, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="b8e26-508">Der UE-V-Agent synchronisiert Benutzereinstellungen für Computer, die nicht immer mit dem Unternehmensnetzwerk (Remotecomputer und Laptops) verbunden sind, und Computern, die immer mit dem Netzwerk verbunden sind (Computer, auf denen Windows Server ausgeführt wird, und Host Virtual Desktop Interface (VDI)-Sitzungen).</span><span class="sxs-lookup"><span data-stu-id="b8e26-508">The UE-V Agent synchronizes user settings for computers that are not always connected to the enterprise network (remote computers and laptops) and computers that are always connected to the network (computers that run Windows Server and host virtual desktop interface (VDI) sessions).</span></span>

<span data-ttu-id="b8e26-509">**Synchronisierung für Computer mit immer verfügbaren Verbindungen:** Wenn Sie UE-v auf Computern verwenden, die immer mit dem Netzwerk verbunden sind, müssen Sie den UE-v-Agent so konfigurieren, dass die Einstellungen mithilfe des *SyncMethod = None* -Parameters synchronisiert werden, der den Einstellungen-Speicherserver als standardmäßige Netzwerkfreigabe behandelt.</span><span class="sxs-lookup"><span data-stu-id="b8e26-509">**Synchronization for computers with always-available connections:** When you use UE-V on computers that are always connected to the network, you must configure the UE-V Agent to synchronize settings by using the *SyncMethod=None* parameter, which treats the settings storage server as a standard network share.</span></span> <span data-ttu-id="b8e26-510">In dieser Konfiguration kann der UE-V-Agent so konfiguriert werden, dass er benachrichtigt, wenn der Import der Anwendungseinstellungen verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="b8e26-510">In this configuration, the UE-V Agent can be configured to notify if the import of the application settings is delayed.</span></span>

<span data-ttu-id="b8e26-511">Aktivieren Sie diese Konfiguration mithilfe einer der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="b8e26-511">Enable this configuration through one of these methods:</span></span>

-   <span data-ttu-id="b8e26-512">Legen Sie während der UE-V-Installation an der Eingabeaufforderung oder in einer Batchdatei den AgentSetup.exe-Parameter *SyncMethod = None*.</span><span class="sxs-lookup"><span data-stu-id="b8e26-512">During UE-V installation, at the command prompt or in a batch file, set the AgentSetup.exe parameter *SyncMethod = None*.</span></span> <span data-ttu-id="b8e26-513">[Die Bereitstellung des UE-V 2. x-Agents](https://technet.microsoft.com/library/dn458891.aspx#agent) bietet weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-513">[Deploying the UE-V 2.x Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more information.</span></span>

-   <span data-ttu-id="b8e26-514">Verwenden Sie nach der UE-V-Installation das Feature einstellungenverwaltung in System Center 2012 Configuration Manager oder die MDOP ADMX-Vorlagen, um die *SyncMethod = None* -Konfiguration zu drücken.</span><span class="sxs-lookup"><span data-stu-id="b8e26-514">After the UE-V installation, use the Settings Management feature in System Center 2012 Configuration Manager or the MDOP ADMX templates to push the *SyncMethod = None* configuration.</span></span>

-   <span data-ttu-id="b8e26-515">Verwenden Sie Windows PowerShell oder WMI (Windows Management Instrumentation), um die *SyncMethod = None* -Konfiguration einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b8e26-515">Use Windows PowerShell or Windows Management Instrumentation (WMI) to set the *SyncMethod = None* configuration.</span></span>

    **<span data-ttu-id="b8e26-516">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-516">Note</span></span>**  
    <span data-ttu-id="b8e26-517">Diese beiden letzten Methoden funktionieren nicht für Umgebungen mit Pooling Virtual Desktop Infrastructure (VDI).</span><span class="sxs-lookup"><span data-stu-id="b8e26-517">These last two methods do not work for pooled virtual desktop infrastructure (VDI) environments.</span></span>



<span data-ttu-id="b8e26-518">Sie müssen den Computer neu starten, bevor die Einstellungen für die Synchronisierung beginnen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-518">You must restart the computer before the settings start to synchronize.</span></span>

**<span data-ttu-id="b8e26-519">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-519">Note</span></span>**  
<span data-ttu-id="b8e26-520">Wenn Sie *SyncMethod = None*festlegen, werden Änderungen an den Einstellungen direkt auf dem Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b8e26-520">If you set *SyncMethod = None*, any settings changes are saved directly to the server.</span></span> <span data-ttu-id="b8e26-521">Wenn die Netzwerkverbindung mit dem Einstellungsspeicher Pfad nicht gefunden wird, werden die Einstellungsänderungen auf dem Gerät zwischengespeichert und beim nächsten Ausführen des Synchronisierungsanbieters synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="b8e26-521">If the network connection to the settings storage path is not found, then the settings changes are cached on the device and are synchronized the next time that the sync provider runs.</span></span> <span data-ttu-id="b8e26-522">Wenn der Speicherpfad für Einstellungen nicht gefunden wird und das Benutzerprofil bei der Abmeldung aus einer gepoolten VDI-Umgebung entfernt wird, gehen die Änderungen an den Einstellungen verloren, und der Benutzer muss die Änderung erneut anwenden, wenn der Computer erneut mit dem Speicherpfad der Einstellungen verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b8e26-522">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, settings changes are lost and the user must reapply the change when the computer is reconnected to the settings storage path.</span></span>



<span data-ttu-id="b8e26-523">**Synchronisierung für externe Synchronisierungs Module:** Der *SyncMethod = External* -Parameter gibt an, dass wenn UE-V-Einstellungen in einen lokalen Ordner auf dem Benutzer Computer geschrieben werden, dann ein externes Synchronisierungsmodul (wie OneDrive for Business, Arbeitsordner, SharePoint oder Dropbox) verwendet werden kann, um diese Einstellungen auf die verschiedenen Computer anzuwenden, auf die Benutzer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b8e26-523">**Synchronization for external sync engines:** The *SyncMethod=External* parameter specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

<span data-ttu-id="b8e26-524">**Unterstützung für freigegebene VDI-Sitzungen:** UE-V 2,1 und 2,1 SP1 bieten Unterstützung für VDI-Sitzungen, die für Endbenutzer freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-524">**Support for shared VDI sessions:** UE-V 2.1 and 2.1 SP1 provide support for VDI sessions that are shared among end users.</span></span> <span data-ttu-id="b8e26-525">Sie können eine spezielle VDI-Vorlage registrieren und konfigurieren, die sicherstellt, dass UE-V alle Funktionen für nicht persistente VDI-Sitzungen intakt hält.</span><span class="sxs-lookup"><span data-stu-id="b8e26-525">You can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

**<span data-ttu-id="b8e26-526">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b8e26-526">Note</span></span>**  
<span data-ttu-id="b8e26-527">Wenn Sie den VDI-Modus nicht für nicht persistente VDI-Sitzungen aktivieren, funktionieren bestimmte Features nicht, beispielsweise " [sichern/wiederherstellen" und "Letzte als funktionierend bekannt" (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8e26-527">If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as [back-up/restore and last known good (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span></span>



<span data-ttu-id="b8e26-528">Die VDI-Vorlage wird mit UE-V 2,1 und 2,1 SP1 bereitgestellt und ist in der Regel nach der Installation hier verfügbar: c:\\Programme c:\\Programme\\Microsoft-Benutzeroberfläche Virtualization\\Templates\\VdiState.xml</span><span class="sxs-lookup"><span data-stu-id="b8e26-528">The VDI template is provided with UE-V 2.1 and 2.1 SP1 and is typically available here after installation: C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml</span></span>

### <span data-ttu-id="b8e26-529">Voraussetzungen für die Unterstützung des UE-V-Generators</span><span class="sxs-lookup"><span data-stu-id="b8e26-529">Prerequisites for UE-V Generator support</span></span>

<span data-ttu-id="b8e26-530">Installieren Sie den UE-V-Generator auf dem Computer, der zum Erstellen benutzerdefinierter Einstellungen für Standort Vorlagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8e26-530">Install the UE-V Generator on the computer that is used to create custom settings location templates.</span></span> <span data-ttu-id="b8e26-531">Dieser Computer sollte in der Lage sein, die Anwendungen auszuführen, deren Einstellungen synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8e26-531">This computer should be able to run the applications whose settings are synchronized.</span></span> <span data-ttu-id="b8e26-532">Sie müssen ein Mitglied der Gruppe Administratoren auf dem Computer sein, auf dem die UE-V-Generator Software ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8e26-532">You must be a member of the Administrators group on the computer that runs the UE-V Generator software.</span></span>

<span data-ttu-id="b8e26-533">Der UE-V-Generator muss auf einem Computer installiert sein, auf dem ein NTFS-Dateisystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8e26-533">The UE-V Generator must be installed on a computer that uses an NTFS file system.</span></span> <span data-ttu-id="b8e26-534">Die UE-V-Generator Software erfordert .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="b8e26-534">The UE-V Generator software requires .NET Framework 4.</span></span> <span data-ttu-id="b8e26-535">Weitere Informationen finden Sie unter [Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="b8e26-535">For more information, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <span data-ttu-id="b8e26-536">Weitere Ressourcen für dieses Produkt</span><span class="sxs-lookup"><span data-stu-id="b8e26-536">Other resources for this product</span></span>


-   [<span data-ttu-id="b8e26-537">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="b8e26-537">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="b8e26-538">Erste Schritte mit UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="b8e26-538">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="b8e26-539">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="b8e26-539">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="b8e26-540">Problembehandlung bei UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="b8e26-540">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="b8e26-541">Technische Referenz für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="b8e26-541">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)














