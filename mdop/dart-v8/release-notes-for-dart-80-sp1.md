---
title: Versionshinweise für DaRT 8.0 SP1
description: Versionshinweise für DaRT 8.0 SP1
author: dansimp
ms.assetid: fa7512d8-fb00-4c27-8f65-c15f3a8ff1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a4c49d12fed07f507d2db4d56969d8e7b0559c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810756"
---
# <span data-ttu-id="09a53-103">Versionshinweise für DaRT 8.0 SP1</span><span class="sxs-lookup"><span data-stu-id="09a53-103">Release Notes for DaRT 8.0 SP1</span></span>


**<span data-ttu-id="09a53-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="09a53-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="09a53-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 Service Pack 1 (SP1) installieren.</span><span class="sxs-lookup"><span data-stu-id="09a53-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Service Pack 1 (SP1).</span></span>

<span data-ttu-id="09a53-106">Diese Versionshinweise enthalten Informationen, die erforderlich sind, um die Diagnose-und Wiederherstellungs-Toolset 8,0 SP1 erfolgreich zu installieren.</span><span class="sxs-lookup"><span data-stu-id="09a53-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.0 SP1.</span></span> <span data-ttu-id="09a53-107">Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="09a53-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="09a53-108">Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderer Dart-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="09a53-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="09a53-109">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="09a53-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="09a53-110">Informationen zur Produktdokumentation</span><span class="sxs-lookup"><span data-stu-id="09a53-110">About the product documentation</span></span>


<span data-ttu-id="09a53-111">Informationen zur Dokumentation für Dart finden Sie auf der [Dart-Startseite](https://go.microsoft.com/fwlink/?LinkID=252096) auf Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="09a53-111">For information about documentation for DaRT, see the [DaRT home page](https://go.microsoft.com/fwlink/?LinkID=252096) on Microsoft TechNet.</span></span>

## <span data-ttu-id="09a53-112">Bekannte Probleme mit Dart 8,0 SP1</span><span class="sxs-lookup"><span data-stu-id="09a53-112">Known issues with DaRT 8.0 SP1</span></span>


### <span data-ttu-id="09a53-113">System Wiederherstellung schlägt fehl, wenn Sie den Schlosser-oder Registrierungs-Editor ausführen</span><span class="sxs-lookup"><span data-stu-id="09a53-113">System restore fails when you run Locksmith or Registry Editor</span></span>

<span data-ttu-id="09a53-114">Wenn Sie Schlosser, Registrierungs-Editor und möglicherweise andere Tools ausführen, schlägt die System Wiederherstellung fehl.</span><span class="sxs-lookup"><span data-stu-id="09a53-114">If you run Locksmith, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="09a53-115">**Problemumgehung:** Schließen Sie Dart, und starten Sie es erneut, und starten Sie dann die System Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="09a53-115">**Workaround:** Close and restart DaRT and then start System Restore.</span></span>

### <span data-ttu-id="09a53-116">Der SFC-Scan läuft nach dem Starten und Schließen der Schlosser-oder Computer Verwaltung nicht.</span><span class="sxs-lookup"><span data-stu-id="09a53-116">SFC scan fails to run after you launch and close Locksmith or Computer Management</span></span>

<span data-ttu-id="09a53-117">Wenn Sie die Schlosser-oder Computer Verwaltungstools starten und dann schließen, kann die System Dateiprüfung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="09a53-117">If you start and then close the Locksmith or Computer Management tools, System File Checker fails to run.</span></span>

<span data-ttu-id="09a53-118">**Problemumgehung:** Schließen Sie Dart, und starten Sie dann den SFC.</span><span class="sxs-lookup"><span data-stu-id="09a53-118">**Workaround:** Close and restart DaRT and then start SFC.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> <span data-ttu-id="09a53-119">Dart-Installationsprogramm schlägt nicht fehl, wenn ADK nicht installiert wurde</span><span class="sxs-lookup"><span data-stu-id="09a53-119">DaRT installer does not fail when ADK has not been installed</span></span>

<span data-ttu-id="09a53-120">Wenn Sie Dart 8,0 SP1 über die Befehlszeile zum Ausführen der MSI-Version installieren und das ADK nicht installiert wurde, sollte die Dart-Installation fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="09a53-120">If you install DaRT 8.0 SP1 by using the command line to run the MSI, and the ADK has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="09a53-121">Derzeit installiert das Dart 8,0 SP1-Installationsprogramm alle Komponenten mit Ausnahme des DART-Wiederherstellungs Bilds.</span><span class="sxs-lookup"><span data-stu-id="09a53-121">Currently, the DaRT 8.0 SP1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="09a53-122">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="09a53-122">**Workaround:** None.</span></span>

### <span data-ttu-id="09a53-123">Defender kann nicht gestartet werden, nachdem Schlosser, regedit, Crash Analyzer und Computer Verwaltung gestartet wurden</span><span class="sxs-lookup"><span data-stu-id="09a53-123">Defender cannot be launched after Locksmith, RegEdit, Crash Analyzer, and Computer Management are launched</span></span>

<span data-ttu-id="09a53-124">Defender startet nicht, wenn Sie bereits Schlosser, regedit, Crash Analyzer und Computer Verwaltung gestartet haben.</span><span class="sxs-lookup"><span data-stu-id="09a53-124">Defender does not launch if you have already launched Locksmith, RegEdit, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="09a53-125">**Problemumgehung:** Schließen und starten Sie Dart neu, und starten Sie dann Defender.</span><span class="sxs-lookup"><span data-stu-id="09a53-125">**Workaround:** Close and restart DaRT and then launch Defender.</span></span>

### <span data-ttu-id="09a53-126">Defender kann langsam starten</span><span class="sxs-lookup"><span data-stu-id="09a53-126">Defender may be slow to launch</span></span>

<span data-ttu-id="09a53-127">Defender benötigt manchmal einige Minuten, um zu starten.</span><span class="sxs-lookup"><span data-stu-id="09a53-127">Defender sometimes takes a few minutes to launch.</span></span> <span data-ttu-id="09a53-128">Auf der Statusleiste wird der aktuelle Ladestatus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="09a53-128">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="09a53-129">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="09a53-129">**Workaround:** None.</span></span>

## <span data-ttu-id="09a53-130">Anmerkungen zu dieser Version Copyright-Informationen</span><span class="sxs-lookup"><span data-stu-id="09a53-130">Release notes copyright information</span></span>


<span data-ttu-id="09a53-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune und WindowsPowerShell sind Marken der Microsoft-Unternehmensgruppe.</span><span class="sxs-lookup"><span data-stu-id="09a53-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="09a53-132">Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.</span><span class="sxs-lookup"><span data-stu-id="09a53-132">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="09a53-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="09a53-133">Related topics</span></span>


[<span data-ttu-id="09a53-134">Informationen zu DaRT 8.0 SP1</span><span class="sxs-lookup"><span data-stu-id="09a53-134">About DaRT 8.0 SP1</span></span>](about-dart-80-sp1.md)

 

 





