---
title: Informationen zu DaRT 7.0
description: Informationen zu DaRT 7.0
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809856"
---
# <span data-ttu-id="7f5cc-103">Informationen zu DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7f5cc-103">About DaRT 7.0</span></span>


<span data-ttu-id="7f5cc-104">Microsoft Diagnostics and Recovery Toolset (Dart) 7 hilft Ihnen bei der Problembehandlung und Reparatur von Windows-basierten Desktops.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 helps you troubleshoot and repair Windows-based desktops.</span></span> <span data-ttu-id="7f5cc-105">Dazu gehören die Desktops, die nicht gestartet werden können.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-105">This includes those desktops that cannot be started.</span></span> <span data-ttu-id="7f5cc-106">Dart ist ein leistungsfähiger Satz von Tools, die die Windows-Wiederherstellungsumgebung (WinRE) verlängern.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-106">DaRT is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="7f5cc-107">Mithilfe von DART können Sie ein Problem analysieren, um dessen Ursache zu ermitteln, beispielsweise indem Sie das Ereignisprotokoll oder die Systemregistrierung des Computers überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span>

<span data-ttu-id="7f5cc-108">DART bietet auch Tools, mit denen Sie ein Problem beheben können, sobald Sie die Ursache ermitteln.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-108">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="7f5cc-109">So können Sie beispielsweise die Tools in DART verwenden, um einen fehlerhaften Gerätetreiber zu deaktivieren, Hotfixes zu entfernen, gelöschte Dateien wiederherzustellen und den Computer auf Malware zu überprüfen, auch wenn Sie das installierte Windows-Betriebssystem nicht starten können oder sollten.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-109">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="7f5cc-110">Dart kann Ihnen dabei helfen, Computer mit einer 32-Bit-oder 64-Bit-Version von Windows 7 schnell wiederherzustellen, in der Regel in kürzerer Zeit als beim neubilden des Computers.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-110">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 7, typically in less time than it would take to reimage the computer.</span></span>

## <span data-ttu-id="7f5cc-111">Informationen zum Wiederherstellungsbild von DART 7</span><span class="sxs-lookup"><span data-stu-id="7f5cc-111">About the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="7f5cc-112">Mit der Funktionalität in DART können Sie ein Wiederherstellungsabbild erstellen, das auf WinRE basiert, kombiniert mit einer Reihe von Tools, die Dart bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-112">Functionality in DaRT lets you create a recovery image that is based on WinRE combined with a set of tools that DaRT provides.</span></span> <span data-ttu-id="7f5cc-113">Das Dart-Wiederherstellungsabbild nutzt WinRE, aus dem Sie auf das Fenster **Diagnose-und Wiederherstellungs-Toolset** zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-113">The DaRT recovery image takes advantage of WinRE, from which you can access the **Diagnostics and Recovery Toolset** window.</span></span>

<span data-ttu-id="7f5cc-114">Verwenden Sie den **Dart-Wiederherstellungsbild-Assistenten** zum Erstellen des DART-Wiederherstellungs Bilds.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-114">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="7f5cc-115">Standardmäßig erstellt der Assistent eine Image-Datei für die internationale Organisation für Standardisierung (ISO) auf dem Desktop mit dem Namen "DaRT70. ISO", obwohl Sie einen anderen Speicherort und einen anderen Dateinamen angeben können.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-115">By default, the wizard creates an International Organization for Standardization (ISO) image file on your desktop that is named DaRT70.iso, although you can specify a different location and file name.</span></span> <span data-ttu-id="7f5cc-116">Mit dem Assistenten können Sie auch das Bild auf eine CD oder DVD brennen.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-116">The wizard also lets you burn the image to a CD or DVD.</span></span> <span data-ttu-id="7f5cc-117">Nach Abschluss des Assistenten können Sie das Wiederherstellungsabbild auf einem USB-Flashlaufwerk speichern oder in einem Format speichern, das Sie zum Erstellen einer Remotepartition oder einer Wiederherstellungspartition verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-117">After you have finished the wizard, you can save the recovery image to a USB flash drive or save it in a format that you can use to create a remote partition or a recovery partition.</span></span>

<span data-ttu-id="7f5cc-118">Wenn Sie DART verwenden müssen, um einen Endbenutzercomputer zu starten, der nicht gestartet wird, können Sie die Anweisungen zum [Wiederherstellen von lokalen Computern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)befolgen.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-118">When you have to use DaRT to startup an end-user computer that will not start, you can follow the instructions at [How to Recover Local Computers Using the DaRT Recovery Image](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="7f5cc-119">Detaillierte Informationen zu den Tools in DART finden Sie unter [Übersicht über die Tools in DART 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="7f5cc-119">For detailed information about the tools in DaRT, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

## <a href="" id="what-s-new-in-dart-7"></a><span data-ttu-id="7f5cc-120">Neuerungen in DART 7</span><span class="sxs-lookup"><span data-stu-id="7f5cc-120">What’s New in DaRT 7</span></span>


<span data-ttu-id="7f5cc-121">DaRT7 unterstützt weiterhin alle in früheren Versionen enthaltenen Szenarien und fügt zusätzlich zu drei neuen Bereitstellungsoptionen ein neues Remote Verbindungs Feature hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-121">DaRT7 continues to support all the scenarios included in previous versions and it adds a new Remote Connection feature in addition to three new deployment options.</span></span>

### <span data-ttu-id="7f5cc-122">Dart 7-Bild Erstellung</span><span class="sxs-lookup"><span data-stu-id="7f5cc-122">DaRT 7 Image Creation</span></span>

<span data-ttu-id="7f5cc-123">Der Assistent, den Sie zum Erstellen von DART-ISO-Bildern verwenden, wird nun als **Dart-Wiederherstellungsbild** bezeichnet und unterstützt nun eine Option zum Aktivieren oder Deaktivieren des neuen Remote Verbindungs Features.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-123">The wizard that you use to create DaRT ISO images is now called **DaRT Recovery Image** and it now supports an option to enable or disable the new Remote Connection feature.</span></span> <span data-ttu-id="7f5cc-124">Mit der Remoteverbindung kann ein Helpdesk-Mitarbeiter die Dart-Tools von einem Remotestandort aus ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-124">Remote Connection lets a helpdesk agent run the DaRT tools from a remote location.</span></span> <span data-ttu-id="7f5cc-125">In früheren Versionen musste der Helpdesk-Agent physisch auf dem Computer des Endbenutzers anwesend sein, um die Dart-Tools ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-125">In previous releases, the helpdesk agent had to be physically present at the end-user computer to run the DaRT tools.</span></span>

<span data-ttu-id="7f5cc-126">Mit dem Assistenten können Sie auch die Willkommensnachricht für das Feature "Remoteverbindung" anpassen (die Meldung wird angezeigt, wenn Endbenutzer das Remoteverbindungstool ausführen).</span><span class="sxs-lookup"><span data-stu-id="7f5cc-126">The wizard also lets you customize the Welcome message for the Remote Connection feature (the message is shown when end users run the Remote Connection tool).</span></span> <span data-ttu-id="7f5cc-127">IT-Administratoren können auch konfigurieren, welche Port Nummer von der Remote Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-127">IT Admins can also configure which Port Number should be used by Remote Connection.</span></span>

<span data-ttu-id="7f5cc-128">Weitere Informationen zum Dart- **Wiederherstellungsbild-Assistenten** oder zur Remote Verbindung finden Sie unter [Erstellen des DART 7,0-Wiederherstellungsabbilds](creating-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="7f5cc-128">For more information about the **DaRT Recovery Image Wizard** or Remote Connection, see [Creating the DaRT 7.0 Recovery Image](creating-the-dart-70-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="7f5cc-129">Dart 7 ISO-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="7f5cc-129">DaRT 7 ISO Deployment</span></span>

<span data-ttu-id="7f5cc-130">Neben dem Brennen auf eine CD oder DVD fügt DaRT7 drei neue Optionen hinzu, wenn Sie die ISO-Datei bereitstellen, die das DART-Wiederherstellungsabbild enthält:</span><span class="sxs-lookup"><span data-stu-id="7f5cc-130">In addition to burning to a CD or DVD, DaRT7 adds three new options when you deploy the ISO that contains the DaRT recovery image:</span></span>

-   <span data-ttu-id="7f5cc-131">Bereitstellung von USB-Flashlaufwerken</span><span class="sxs-lookup"><span data-stu-id="7f5cc-131">USB flash drive deployment</span></span>

-   <span data-ttu-id="7f5cc-132">Bereitstellung von Remote Partitionen</span><span class="sxs-lookup"><span data-stu-id="7f5cc-132">Remote partition deployment</span></span>

-   <span data-ttu-id="7f5cc-133">Bereitstellung der Wiederherstellungspartition</span><span class="sxs-lookup"><span data-stu-id="7f5cc-133">Recovery partition deployment</span></span>

<span data-ttu-id="7f5cc-134">Mit der Deployment-Option für das USB-Flashlaufwerk kann ein Unternehmen Dart auf Computern verwenden, auf denen keine CD-oder DVD-Laufwerke verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-134">The USB flash drive deployment option lets a company use DaRT on computers that do not have CD or DVD drives available.</span></span> <span data-ttu-id="7f5cc-135">Die Optionen für die Wiederherstellung und die Remotepartition ermöglichen Endbenutzern den einfachen Zugriff auf das DART-Bild und die Remote Verbindungsfunktion.</span><span class="sxs-lookup"><span data-stu-id="7f5cc-135">The recovery and remote partition options let end users have easy access to the DaRT image and to enable the Remote Connection functionality.</span></span>

<span data-ttu-id="7f5cc-136">Weitere Informationen zum Bereitstellen von DART-Wiederherstellungs Bildern finden Sie unter [Bereitstellen des DART 7,0-Wiederherstellungsabbilds](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="7f5cc-136">For more information about how to deploy DaRT recovery images, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="7f5cc-137">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7f5cc-137">Related topics</span></span>


[<span data-ttu-id="7f5cc-138">Erste Schritte mit DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7f5cc-138">Getting Started with DaRT 7.0</span></span>](getting-started-with-dart-70-new-ia.md)

[<span data-ttu-id="7f5cc-139">Versionshinweise für DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7f5cc-139">Release Notes for DaRT 7.0</span></span>](release-notes-for-dart-70-new-ia.md)

 

 





