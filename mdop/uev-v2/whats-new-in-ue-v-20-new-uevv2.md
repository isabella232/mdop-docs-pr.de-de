---
title: Neuigkeiten in UE-V 2.0
description: Neuigkeiten in UE-V 2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810870"
---
# <span data-ttu-id="9bdf5-103">Neuigkeiten in UE-V 2.0</span><span class="sxs-lookup"><span data-stu-id="9bdf5-103">What's New in UE-V 2.0</span></span>


<span data-ttu-id="9bdf5-104">Microsoft User Experience Virtualization (UE-v) 2,0 stellt diese neuen Features und Funktionen im Vergleich zu UE-v 1,0 zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-104">Microsoft User Experience Virtualization (UE-V) 2.0 provides these new features and functionality compared to UE-V 1.0.</span></span> <span data-ttu-id="9bdf5-105">Die [Microsoft User Experience Virtualization (UE-v) 2,0-Versionshinweise](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) bieten weitere Informationen zur Version UE-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-105">The [Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) provide more information about the UE-V 2.0 release.</span></span>

## <span data-ttu-id="9bdf5-106">Client seitiger Cache (CSC) nicht mehr erforderlich</span><span class="sxs-lookup"><span data-stu-id="9bdf5-106">Client-side cache (CSC) no longer required</span></span>


<span data-ttu-id="9bdf5-107">Diese Version von UE-V führt den **Synchronisierungsanbieter**ein, der die Anforderung für das Windows-Feature "Offline Dateien" ersetzt, um einen clientseitigen Cache von Einstellungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-107">This version of UE-V introduces the **sync provider**, which replaces the requirement for the Windows Offline Files feature to support a client-side cache of settings.</span></span>

<span data-ttu-id="9bdf5-108">Während UE-V zum Synchronisieren von Einstellungen nur verwendet wird, wenn eine Anwendung geöffnet, geschlossen oder wenn Windows gesperrt oder entriegelt wurde, oder bei der Anmeldung oder Abmeldung der Synchronisierungsanbieter auch...</span><span class="sxs-lookup"><span data-stu-id="9bdf5-108">Whereas UE-V used to synchronize settings only when an application opened, closed, or when Windows locked or unlocked, or at logon or logoff, the sync provider also …</span></span>

-   <span data-ttu-id="9bdf5-109">Synchronisiert lokale Anwendungs-und Windows-Einstellungen out-of-Band mit "**Trigger-Ereignisse**"</span><span class="sxs-lookup"><span data-stu-id="9bdf5-109">Synchronizes local application and Windows settings out-of-band using "**trigger events**"</span></span>

-   <span data-ttu-id="9bdf5-110">Verwendet eine **geplante Aufgabe** zum Synchronisieren des Einstellungen-Speicher Pakets in einem beliebigen Intervall, das Sie für Ihre Unternehmensanforderungen auswählen (standardmäßig alle 30 Minuten)</span><span class="sxs-lookup"><span data-stu-id="9bdf5-110">Uses a **scheduled task** to sync the settings storage package in any interval you choose for your enterprise requirements (every 30 minutes by default)</span></span>

<span data-ttu-id="9bdf5-111">Bestimmte Bedingungen bieten eine häufigere Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-111">Certain conditions provide more frequent synchronization.</span></span>

-   <span data-ttu-id="9bdf5-112">Einstellungen werden synchronisiert, wenn der Benutzer auf die Schaltfläche " **Jetzt synchronisieren** " in der neuen Unternehmenseinstellungen-Center-Anwendung klickt.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-112">Settings synchronize when the user clicks the **Sync Now** button in the new Company Settings Center application.</span></span>

-   <span data-ttu-id="9bdf5-113">Der Synchronisierungsanbieter kann auch für eine einzelne Anwendung gestartet werden, ohne auf den geplanten Synchronisierungstask zu warten.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-113">The sync provider can also start for a single application without waiting for the scheduled synchronization task.</span></span> <span data-ttu-id="9bdf5-114">Wenn beispielsweise eine Anwendung geschlossen wird, werden alle Einstellungsänderungen in den lokalen Cache geschrieben, und der Synchronisierungsanbieter Prozess wird asynchron ausgeführt, um diese neuen Einstellungsänderungen in den Speicherort der Einstellungen zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-114">For example, when an application is closed, any settings changes are written to the local cache, and the sync provider process runs asynchronously to move those new settings changes to the settings storage location.</span></span>

## <span data-ttu-id="9bdf5-115">Windows-App-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="9bdf5-115">Windows app synchronization</span></span>


<span data-ttu-id="9bdf5-116">Der Entwickler einer Windows-App kann definieren, welche Einstellungen, falls vorhanden, synchronisiert werden sollen, und diese Einstellungen können nun mit UE-V erfasst und synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-116">The developer of a Windows app can define which settings, if any, are to be synchronized, and these settings can now be captured and synchronized with UE-V.</span></span>

<span data-ttu-id="9bdf5-117">Standardmäßig synchronisiert UE-V die Einstellungen für viele der Windows-apps, die in Windows 8 und Windows 8,1 enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-117">By default, UE-V synchronizes the settings of many of the Windows apps included in Windows 8 and Windows 8.1.</span></span> <span data-ttu-id="9bdf5-118">Sie können die Liste synchronisierter apps mit Windows PowerShell, Windows-Verwaltungsinstrumentation (WMI) oder Gruppenrichtlinie ändern.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-118">You can modify the list of synchronized apps with Windows PowerShell, Windows Management Instrumentation (WMI), or Group Policy.</span></span>

<span data-ttu-id="9bdf5-119">**Hinweis**  UE-V synchronisiert keine Windows-App-Einstellungen, wenn die Domänenbenutzer Ihre Anmeldeinformationen mit Ihrem Microsoft-Konto verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-119">**Note** UE-V does not synchronize Windows app settings if the domain users link their sign-in credentials to their Microsoft account.</span></span> <span data-ttu-id="9bdf5-120">Diese Verknüpfung synchronisiert Einstellungen mit Microsoft OneDrive, damit UE-V nur die Desktopanwendungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-120">This linking synchronizes settings to Microsoft OneDrive so UE-V only synchronizes the desktop applications.</span></span>

 

## <span data-ttu-id="9bdf5-121">Verknüpfung des Microsoft-Kontos</span><span class="sxs-lookup"><span data-stu-id="9bdf5-121">Microsoft account linking</span></span>


<span data-ttu-id="9bdf5-122">Die Synchronisierung von Einstellungen über OneDrive ist neu bei Windows 8, wenn Sie mit einem Microsoft-Konto angemeldet sind oder wenn Sie Ihr Microsoft-Konto mit Ihrem Domänenkonto verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-122">Settings synchronization via OneDrive is new to Windows 8 when you are signed in with a Microsoft account or if you link your Microsoft account to your domain account.</span></span> <span data-ttu-id="9bdf5-123">Wenn ein Domänenbenutzer UE-V verwendet und sich bei einem Microsoft-Konto angemeldet hat,...</span><span class="sxs-lookup"><span data-stu-id="9bdf5-123">If a domain user uses UE-V and has signed in to a Microsoft account, then…</span></span>

-   <span data-ttu-id="9bdf5-124">UE-V synchronisiert nur Einstellungen für Desktopanwendungen</span><span class="sxs-lookup"><span data-stu-id="9bdf5-124">UE-V only synchronizes settings for desktop applications</span></span>

-   <span data-ttu-id="9bdf5-125">Microsoft-Konto verarbeitet Windows-App-Einstellungen und Windows-Desktopeinstellungen</span><span class="sxs-lookup"><span data-stu-id="9bdf5-125">Microsoft account handles Windows app settings and Windows desktop settings</span></span>

## <span data-ttu-id="9bdf5-126">Unternehmenseinstellungen (Center)</span><span class="sxs-lookup"><span data-stu-id="9bdf5-126">Company Settings Center</span></span>


<span data-ttu-id="9bdf5-127">Sie können Ihren Benutzern eine gewisse Kontrolle darüber bieten, welche Einstellungen über eine Anwendung in UE-V 2 mit dem Namen Unternehmenseinstellungen-Center synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-127">You can provide your users with some control over which settings are synchronized through an application in UE-V 2 called Company Settings Center.</span></span> <span data-ttu-id="9bdf5-128">Das Unternehmenseinstellungen-Center wird zusammen mit dem UE-v-Agent installiert, und die Benutzer können über die Systemsteuerung, das **Startmenü** oder den **Start** Bildschirm sowie über das Symbol UE-v-Benachrichtigungsbereich darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-128">Company Settings Center is installed along with the UE-V Agent, and users can access it from Control Panel, the **Start** menu or **Start** screen, and from the UE-V notification area icon.</span></span>

<span data-ttu-id="9bdf5-129">Das Unternehmenseinstellungen-Center zeigt an, welche Einstellungen synchronisiert sind, und ermöglicht Benutzern, den Synchronisierungsstatus von UE-V anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-129">Company Settings Center displays which settings are synchronized and lets users see the synchronization status of UE-V.</span></span> <span data-ttu-id="9bdf5-130">Wenn Sie Sie zulassen, können Benutzer mithilfe des Unternehmenseinstellungen-Centers auswählen, welche Einstellungen synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-130">If you let them, users can use Company Settings Center to select which settings to synchronize.</span></span> <span data-ttu-id="9bdf5-131">Sie können auch auf die Schaltfläche " **Jetzt synchronisieren** " klicken, um alle Einstellungen sofort zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="9bdf5-131">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span>






## <span data-ttu-id="9bdf5-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9bdf5-132">Related topics</span></span>


[<span data-ttu-id="9bdf5-133">Erste Schritte mit UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="9bdf5-133">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="9bdf5-134">Vorbereiten einer UE-V 2. x-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="9bdf5-134">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="9bdf5-135">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="9bdf5-135">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





