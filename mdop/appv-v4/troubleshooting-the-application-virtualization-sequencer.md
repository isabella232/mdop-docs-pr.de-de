---
title: Problembehandlung für Application Virtualization Sequencer
description: Problembehandlung für Application Virtualization Sequencer
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806204"
---
# <span data-ttu-id="d5c4f-103">Problembehandlung für Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="d5c4f-103">Troubleshooting the Application Virtualization Sequencer</span></span>


<span data-ttu-id="d5c4f-104">Dieses Thema enthält Informationen, die Sie bei der Behandlung allgemeiner Probleme beim Application Virtualization (App-V)-Sequenzer verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="d5c4f-105">Durch das Erstellen einer SFTD-Datei mithilfe von App-V Sequencer wird die Versionsnummer unerwartet erhöht</span><span class="sxs-lookup"><span data-stu-id="d5c4f-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="d5c4f-106">Die Versionsnummer, die einer SFTD-Datei zugeordnet ist, nimmt unerwartet zu.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-106">The version number associated with an SFTD file increases unexpectedly.</span></span>

**<span data-ttu-id="d5c4f-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="d5c4f-107">Solution</span></span>**

<span data-ttu-id="d5c4f-108">Verwenden Sie die Befehlszeile, um eine neue SFT-Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-108">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="d5c4f-109">Wenn Sie die SFT-Datei über die Befehlszeile erstellen möchten, geben Sie an der Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="d5c4f-109">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="d5c4f-110">mkdiffpkg.exe &lt; Base SFT-Dateinamen &gt; &lt; diff SFT-Dateiname&gt;</span><span class="sxs-lookup"><span data-stu-id="d5c4f-110">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="d5c4f-111">Der Dateiname in der OSD-Datei ist nach dem Paket Upgrade nicht richtig</span><span class="sxs-lookup"><span data-stu-id="d5c4f-111">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="d5c4f-112">Nach dem Upgrade eines vorhandenen Pakets ist der Dateiname nicht richtig.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-112">After you upgrade an existing package, the file name is not correct.</span></span>

**<span data-ttu-id="d5c4f-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="d5c4f-113">Solution</span></span>**

<span data-ttu-id="d5c4f-114">Wenn Sie ein Paket für das Upgrade öffnen, sollten Sie das Root-Q:\\-Laufwerk als Ausgabespeicherort für das Paket angeben.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-114">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="d5c4f-115">Geben Sie keinen zugeordneten Dateinamen mit dem Ausgabespeicherort an.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-115">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="d5c4f-116">Die Microsoft Word2003-Standardinstallation führt zu einem Fehler beim Streamen an einen Client.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-116">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="d5c4f-117">Wenn Sie Microsoft Word2003 zu einem Client streamen, wird ein Fehler zurückgegeben, aber Microsoft Word wird weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-117">When you stream Microsoft Word2003 to a client, an error is returned but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="d5c4f-118">Lösung</span><span class="sxs-lookup"><span data-stu-id="d5c4f-118">Solution</span></span>**

<span data-ttu-id="d5c4f-119">Umsequenzieren Sie das virtuelle Anwendungspaket, und wählen Sie **vollständige Installation**aus.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-119">Resequence the virtual application package, and select **Full Install**.</span></span>

## <span data-ttu-id="d5c4f-120">Das Paket Upgrade funktioniert nicht, wenn Sie ein abhängiges Paket erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-120">Package Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="d5c4f-121">Wenn Sie ein abhängiges Paket erstellen, indem Sie die Paketaktualisierung verwenden und neue Registrierungseinträge hinzufügen, scheint es korrekt zu funktionieren, aber die aktualisierten Registrierungseinträge sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-121">When you create a dependent package by using package upgrade and add new registry entries, it appears to function correctly but the updated registry entries are not available.</span></span>

**<span data-ttu-id="d5c4f-122">Lösung</span><span class="sxs-lookup"><span data-stu-id="d5c4f-122">Solution</span></span>**

<span data-ttu-id="d5c4f-123">Registrierungseinstellungen werden immer mit der ursprünglichen Version des Pakets gespeichert, sodass Updates für das Paket nur dann verfügbar sind, wenn Sie das ursprüngliche Paket repariert haben.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-123">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="d5c4f-124">Fehler beim Sequenz Versuch. NET 2.0</span><span class="sxs-lookup"><span data-stu-id="d5c4f-124">Error When Trying to Sequence .NET2.0</span></span>


<span data-ttu-id="d5c4f-125">Wenn Sie ein Paket sequenzieren, das erfordert. NET 2.0 erhalten Sie eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-125">When you sequence a package that requires .NET2.0, you get an error.</span></span>

**<span data-ttu-id="d5c4f-126">Lösung</span><span class="sxs-lookup"><span data-stu-id="d5c4f-126">Solution</span></span>**

<span data-ttu-id="d5c4f-127">Sequenzierung von Paketen, die erforderlich sind. NET 2.0 wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d5c4f-127">Sequencing packages that require .NET2.0 is not supported.</span></span>

## <span data-ttu-id="d5c4f-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d5c4f-128">Related topics</span></span>


[<span data-ttu-id="d5c4f-129">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="d5c4f-129">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





