---
title: Behandeln von Problemen mit Application Virtualization Sequencer
description: Behandeln von Problemen mit Application Virtualization Sequencer
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806228"
---
# <span data-ttu-id="226ba-103">Behandeln von Problemen mit Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="226ba-103">Troubleshooting Application Virtualization Sequencer Issues</span></span>


<span data-ttu-id="226ba-104">Dieses Thema enthält Informationen, die Sie bei der Behandlung allgemeiner Probleme beim Application Virtualization (App-V)-Sequenzer verwenden können.</span><span class="sxs-lookup"><span data-stu-id="226ba-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="226ba-105">Durch das Erstellen einer SFTD-Datei mithilfe von App-V Sequencer wird die Versionsnummer unerwartet erhöht</span><span class="sxs-lookup"><span data-stu-id="226ba-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="226ba-106">Verwenden Sie die Befehlszeile, um eine neue SFT-Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="226ba-106">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="226ba-107">Wenn Sie die SFT-Datei über die Befehlszeile erstellen möchten, geben Sie an der Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="226ba-107">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="226ba-108">mkdiffpkg.exe &lt; Base SFT-Dateinamen &gt; &lt; diff SFT-Dateiname&gt;</span><span class="sxs-lookup"><span data-stu-id="226ba-108">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="226ba-109">Der Dateiname in der OSD-Datei ist nach dem Paket Upgrade nicht richtig</span><span class="sxs-lookup"><span data-stu-id="226ba-109">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="226ba-110">Wenn Sie ein Paket für das Upgrade öffnen, sollten Sie das Root-Q:\\-Laufwerk als Ausgabespeicherort für das Paket angeben.</span><span class="sxs-lookup"><span data-stu-id="226ba-110">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="226ba-111">Geben Sie keinen zugeordneten Dateinamen mit dem Ausgabespeicherort an.</span><span class="sxs-lookup"><span data-stu-id="226ba-111">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="226ba-112">Die Microsoft Word2003-Standardinstallation führt zu einem Fehler beim Streamen an einen Client.</span><span class="sxs-lookup"><span data-stu-id="226ba-112">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="226ba-113">Wenn Sie Microsoft Word2003 zu einem Client streamen, wird ein Fehler zurückgegeben, aber Microsoft Word wird weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="226ba-113">When you stream Microsoft Word2003 to a client, an error is returned, but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="226ba-114">Lösung</span><span class="sxs-lookup"><span data-stu-id="226ba-114">Solution</span></span>**

<span data-ttu-id="226ba-115">Umsequenzieren Sie das virtuelle Anwendungspaket, und wählen Sie **vollständige Installation**aus.</span><span class="sxs-lookup"><span data-stu-id="226ba-115">Resequence the virtual application package and select **Full Install**.</span></span>

## <span data-ttu-id="226ba-116">Das aktive Upgrade funktioniert nicht, wenn Sie ein abhängiges Paket erstellen.</span><span class="sxs-lookup"><span data-stu-id="226ba-116">Active Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="226ba-117">Wenn Sie ein abhängiges Paket erstellen, indem Sie das aktive Upgrade verwenden und neue Registrierungseinträge hinzufügen, scheint es korrekt zu funktionieren, aber die aktualisierten Registrierungseinträge sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="226ba-117">When you create a dependent package by using active upgrade and add new registry entries, it appears to function correctly, but the updated registry entries are not available.</span></span>

**<span data-ttu-id="226ba-118">Lösung</span><span class="sxs-lookup"><span data-stu-id="226ba-118">Solution</span></span>**

<span data-ttu-id="226ba-119">Registrierungseinstellungen werden immer mit der ursprünglichen Version des Pakets gespeichert, sodass Updates für das Paket nur dann verfügbar sind, wenn Sie das ursprüngliche Paket repariert haben.</span><span class="sxs-lookup"><span data-stu-id="226ba-119">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="226ba-120">Detaillierte Informationen sind für Microsoft office2007-Dokumente auf der Seite "Eigenschaften" nicht sichtbar</span><span class="sxs-lookup"><span data-stu-id="226ba-120">Detailed information is not visible for Microsoft Office2007 documents by using the properties page</span></span>


<span data-ttu-id="226ba-121">Wenn Sie versuchen, detaillierte Informationen zu einem Microsoft office2007-Dokument mithilfe der Eigenschaftenseite anzuzeigen, werden die detaillierten Informationen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="226ba-121">When you try to view detailed information associated with a Microsoft Office2007 document by using the properties page, the detailed information is not visible.</span></span>

**<span data-ttu-id="226ba-122">Lösung</span><span class="sxs-lookup"><span data-stu-id="226ba-122">Solution</span></span>**

<span data-ttu-id="226ba-123">App-V unterstützt nicht die erforderlichen Shell-Erweiterungen für diese Eigenschaftenseiten.</span><span class="sxs-lookup"><span data-stu-id="226ba-123">App-V does not support the required shell extensions for these property pages.</span></span>

## <span data-ttu-id="226ba-124">Einige Registrierungsschlüssel werden nicht erfasst, wenn Sie 16-Bit-Anwendungen abgleichen</span><span class="sxs-lookup"><span data-stu-id="226ba-124">Some registry keys are not captured when you sequence 16-bit applications</span></span>


<span data-ttu-id="226ba-125">In App-V 4,5 wurde das Registrierungs-Hooking vom Kernelmodus in den Benutzermodus verschoben.</span><span class="sxs-lookup"><span data-stu-id="226ba-125">In App-V 4.5, registry hooking has been moved from kernel mode to user mode.</span></span> <span data-ttu-id="226ba-126">Wenn Sie eine 16-Bit-Anwendung oder eine Anwendung, die ein 16-Bit-Installationsprogramm verwendet, abgleichen möchten, müssen Sie zuerst den Sequencer-Computer so konfigurieren, dass der Prozess in einer eigenen Kopie des Windows NT Virtual DOS Machine (NTVDM) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="226ba-126">If you want to sequence a 16-bit application or an application that uses a 16-bit installer, you must first configure the sequencer computer so that the process runs in its own copy of the Windows NT Virtual DOS Machine (NTVDM).</span></span>

**<span data-ttu-id="226ba-127">Lösung</span><span class="sxs-lookup"><span data-stu-id="226ba-127">Solution</span></span>**

<span data-ttu-id="226ba-128">Bevor Sie die Anwendung sequenzieren, setzen Sie den folgenden globalen REGSZ-Registrierungsschlüsselwert auf "Ja" auf dem Sequenzcomputer:</span><span class="sxs-lookup"><span data-stu-id="226ba-128">Before you sequence the application, set the following global REGSZ registry key value to "yes" on the sequencing computer:</span></span>

<span data-ttu-id="226ba-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span><span class="sxs-lookup"><span data-stu-id="226ba-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span></span>

<span data-ttu-id="226ba-130">Sie müssen den Computer neu starten, bevor dies wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="226ba-130">You must restart the computer before this takes effect.</span></span>

## <span data-ttu-id="226ba-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="226ba-131">Related topics</span></span>


[<span data-ttu-id="226ba-132">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="226ba-132">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





