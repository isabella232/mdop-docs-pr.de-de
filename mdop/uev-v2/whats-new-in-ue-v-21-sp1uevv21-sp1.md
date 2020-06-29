---
title: Neuigkeiten in UE-V 2.1 SP1
description: Neuigkeiten in UE-V 2.1 SP1
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812349"
---
# <span data-ttu-id="28404-103">Neuigkeiten in UE-V 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="28404-103">What's New in UE-V 2.1 SP1</span></span>


<span data-ttu-id="28404-104">Die Benutzeroberflächen-Virtualisierung 2,1 SP1 bietet diese neuen Features und Funktionen im Vergleich zu UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="28404-104">User Experience Virtualization 2.1 SP1 provides these new features and functionality compared to UE-V 2.1.</span></span> <span data-ttu-id="28404-105">In den Versionshinweisen für [Microsoft User Experience Virtualization (UE-v) 2,1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) finden Sie weitere Informationen zur Version UE-v 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="28404-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) provide more information about the UE-V 2.1 SP1 release.</span></span>

## <span data-ttu-id="28404-106">Unterstützung für Windows 10</span><span class="sxs-lookup"><span data-stu-id="28404-106">Support for Windows 10</span></span>


<span data-ttu-id="28404-107">UE-v 2,1 SP1 bietet zusätzlich zur gleichen Software, die in früheren Versionen von UE-v unterstützt wird, Unterstützung für Windows 10.</span><span class="sxs-lookup"><span data-stu-id="28404-107">UE-V 2.1 SP1 adds support for Windows 10, in addition to the same software that is supported in earlier versions of UE-V.</span></span>

### <span data-ttu-id="28404-108">Kompatibilität mit Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="28404-108">Compatibility with Microsoft Azure</span></span>

<span data-ttu-id="28404-109">Windows 10 ermöglicht es Unternehmensbenutzern, Windows-App-Einstellungen und Windows-Betriebssystemeinstellungen zu Azure anstatt zu OneDrive zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="28404-109">Windows 10 lets enterprise users synchronize Windows app settings and Windows operating system settings to Azure instead of to OneDrive.</span></span> <span data-ttu-id="28404-110">Sie können die Windows 10 Enterprise-Synchronisierungs Funktionalität zusammen mit UE-V für lokale Domänen verbundene Computer verwenden.</span><span class="sxs-lookup"><span data-stu-id="28404-110">You can use the Windows 10 enterprise sync functionality together with UE-V for on-premises domain-joined computers only.</span></span> <span data-ttu-id="28404-111">Um die Koexistenz zwischen Windows 10 und UE-v zu aktivieren, müssen Sie die folgenden UE-v-Vorlagen mithilfe von PowerShell auf jedem Client oder in einer Gruppenrichtlinie deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="28404-111">To enable coexistence between Windows 10 and UE-V, you must disable the following UE-V templates using either PowerShell on each client or Group Policy.</span></span>

<span data-ttu-id="28404-112">Konfigurieren Sie in Gruppenrichtlinien unter dem Knoten Microsoft User Experience Virtualization die folgenden Richtlinieneinstellungen:</span><span class="sxs-lookup"><span data-stu-id="28404-112">In Group Policy, under the Microsoft User Experience Virtualization node, configure these policy settings:</span></span>

-   <span data-ttu-id="28404-113">Aktivieren von "Windows-apps nicht synchronisieren"</span><span class="sxs-lookup"><span data-stu-id="28404-113">Enable “Do Not Synchronize Windows Apps”</span></span>

-   <span data-ttu-id="28404-114">Deaktivieren von "Windows-Synchronisierungseinstellungen"</span><span class="sxs-lookup"><span data-stu-id="28404-114">Disable “Sync Windows Settings”</span></span>

### <span data-ttu-id="28404-115">Einstellungen-Synchronisierungsverhalten für Windows 10-Unterstützung geändert</span><span class="sxs-lookup"><span data-stu-id="28404-115">Settings Synchronization Behavior Changed for Windows 10 Support</span></span>

<span data-ttu-id="28404-116">UE-V 2,1 SP1 durchstreift die Taskleisteneinstellungen zwischen Windows 10-Geräten.</span><span class="sxs-lookup"><span data-stu-id="28404-116">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="28404-117">UE-V synchronisiert jedoch keine Taskleisteneinstellungen zwischen Windows 10-Geräten und Geräten, auf denen frühere Betriebssysteme ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="28404-117">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>

<span data-ttu-id="28404-118">Darüber hinaus synchronisiert UE-V 2,1 SP1 keine Einstellungen zwischen dem Microsoft-Rechner in Windows 10 und dem Microsoft-Rechner in früheren Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="28404-118">In addition, UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>

## <span data-ttu-id="28404-119">Support für Roaming-Netzwerkdrucker hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="28404-119">Support Added for Roaming Network Printers</span></span>


<span data-ttu-id="28404-120">Mit UE-V 2,1 SP1 können Netzwerkdrucker zwischen Geräten Roaming durchlaufen, damit ein Benutzer auf seine Netzwerkdrucker zugreifen kann, wenn er sich bei einem beliebigen Gerät im Netzwerk anmeldet.</span><span class="sxs-lookup"><span data-stu-id="28404-120">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="28404-121">Dies umfasst das Roaming des Druckers, den Sie als Standard festlegen.</span><span class="sxs-lookup"><span data-stu-id="28404-121">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="28404-122">Für das Drucker-Roaming in UE-V ist eines der folgenden Szenarien erforderlich:</span><span class="sxs-lookup"><span data-stu-id="28404-122">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="28404-123">Der Druckserver kann den erforderlichen Treiber herunterladen, wenn er auf ein neues Gerät wechselt.</span><span class="sxs-lookup"><span data-stu-id="28404-123">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="28404-124">Der Treiber für den Roaming-Netzwerkdrucker ist auf allen Geräten vorinstalliert, die auf diesen Netzwerkdrucker zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="28404-124">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="28404-125">Der Druckertreiber kann über Windows Update abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="28404-125">The printer driver can be obtained from Windows Update.</span></span>

<span data-ttu-id="28404-126">**Hinweis**  Das UE-V Printer-Roaming-Feature unterstützt **keine** Druckereinstellungen oder-Einstellungen, beispielsweise das doppelseitige Drucken.</span><span class="sxs-lookup"><span data-stu-id="28404-126">**Note** The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>

 

## <span data-ttu-id="28404-127">Office 2013-Einstellungen, Speicherort Vorlage</span><span class="sxs-lookup"><span data-stu-id="28404-127">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="28404-128">UE-V 2,1 und 2,1 SP1 beinhalten die Vorlage Microsoft Office 2013 Settings Location mit verbesserter Unterstützung für Outlook-Signaturen.</span><span class="sxs-lookup"><span data-stu-id="28404-128">UE-V 2.1 and 2.1 SP1 include the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="28404-129">Wir haben die Synchronisierung von standardmäßigen Signatureinstellungen für neue, Antworten und weitergeleitete e-Mails hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="28404-129">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="28404-130">Kunden müssen die standardmäßigen Signatureinstellungen nicht mehr auswählen.</span><span class="sxs-lookup"><span data-stu-id="28404-130">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="28404-131">**Hinweis**  Für jedes Gerät, auf dem ein Benutzer seine Outlook-Signatur synchronisieren möchte, muss ein Outlook-Profil erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="28404-131">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="28404-132">Wenn das Profil noch nicht erstellt wurde, kann der Benutzer eine erstellen und dann Outlook auf diesem Gerät neu starten, um die Signatur Synchronisierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="28404-132">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="28404-133">Zuvor enthielt UE-v die Microsoft Office 2010-Einstellungen für Standort Vorlagen, die automatisch verteilt und beim UE-v-Agent registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="28404-133">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="28404-134">UE-V 2,1 arbeitet mit Office 365, um festzustellen, ob die Office 2013-Einstellungen von Office 365 durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="28404-134">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="28404-135">Wenn die Einstellungen von Office 365 durchlaufen werden, werden Sie nicht von UE-V durchsucht.</span><span class="sxs-lookup"><span data-stu-id="28404-135">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="28404-136">Eine Übersicht über die [Einstellungen für Benutzer und Roaming für Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) bietet weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="28404-136">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="28404-137">Führen Sie eine der folgenden Aktionen aus, um die Synchronisierung von Einstellungen mithilfe von UE-V 2,1 zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="28404-137">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="28404-138">Verwenden von Gruppenrichtlinien zum Deaktivieren der Office 365-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="28404-138">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="28404-139">Aktivieren der Office 365-Synchronisierungs Erfahrung während der Installation von Office 2013</span><span class="sxs-lookup"><span data-stu-id="28404-139">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="28404-140">UE-V 2,1 liefert [Office 2013-und Office 2010-Vorlagen](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="28404-140">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="28404-141">Diese Version entfernt die Office 2007-Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="28404-141">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="28404-142">Benutzer können weiterhin Office 2007-Vorlagen aus UE-v 2,0 oder früheren Versionen verwenden und können weiterhin die Vorlagen aus dem [hier](https://go.microsoft.com/fwlink/p/?LinkID=246589)befindlichen UE-v-Vorlagenkatalog abrufen.</span><span class="sxs-lookup"><span data-stu-id="28404-142">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>






## <span data-ttu-id="28404-143">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="28404-143">Related topics</span></span>


[<span data-ttu-id="28404-144">Erste Schritte mit UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="28404-144">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="28404-145">Vorbereiten einer UE-V 2. x-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="28404-145">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="28404-146">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="28404-146">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





