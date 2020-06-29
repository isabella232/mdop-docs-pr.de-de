---
title: Versionshinweise für DaRT 8.1
description: Versionshinweise für DaRT 8.1
author: dansimp
ms.assetid: 44303107-60f4-485c-848a-7e0529f142d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d0ba817ddd5bbdefcf7fed833f4c47e7b9d9ce0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810750"
---
# <span data-ttu-id="aad32-103">Versionshinweise für DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="aad32-103">Release Notes for DaRT 8.1</span></span>


**<span data-ttu-id="aad32-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="aad32-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="aad32-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft Diagnostics and Recovery Toolset (Dart) 8,1 installieren.</span><span class="sxs-lookup"><span data-stu-id="aad32-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1.</span></span>

<span data-ttu-id="aad32-106">Diese Versionshinweise enthalten Informationen, die erforderlich sind, um die Diagnose-und Wiederherstellungs-Toolset 8,1 erfolgreich zu installieren.</span><span class="sxs-lookup"><span data-stu-id="aad32-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.1.</span></span> <span data-ttu-id="aad32-107">Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="aad32-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="aad32-108">Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderer Dart-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="aad32-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="aad32-109">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="aad32-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="aad32-110">Bekannte Probleme mit Dart 8,1</span><span class="sxs-lookup"><span data-stu-id="aad32-110">Known issues with DaRT 8.1</span></span>


### <span data-ttu-id="aad32-111">Disk Commander kann einen beschädigten Master-Boot-Eintrag in einer physikalischen Partition in Windows 8,1 nicht reparieren</span><span class="sxs-lookup"><span data-stu-id="aad32-111">Disk Commander is unable to repair a corrupt master boot record in a physical partition in Windows 8.1</span></span>

<span data-ttu-id="aad32-112">In Windows 8,1 kann der "Master Boot Record (MBR) wiederherstellen" oder die Kopfzeile der GUID-Partitionstabelle (GPT)-Option in Disk Commander keinen beschädigten Master-Boot-Eintrag in einer physikalischen Partition reparieren, und der Clientcomputer kann daher nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="aad32-112">In Windows 8.1, the “Restore the Master Boot Record (MBR) or the header of the GUID Partition Table (GPT)” option in Disk Commander is unable to repair a corrupt master boot record in a physical partition, and therefore is unable to boot the client computer.</span></span>

<span data-ttu-id="aad32-113">**Problemumgehung:** Starten Sie die **Systemstartreparatur**, klicken Sie auf **Problembehandlung**, klicken Sie auf **Erweiterte Optionen**, und klicken Sie dann auf **Reparieren**.</span><span class="sxs-lookup"><span data-stu-id="aad32-113">**Workaround:** Start **Startup Repair**, click **Troubleshoot**, click **Advanced options**, and then click **Start repair**.</span></span>

### <span data-ttu-id="aad32-114">Mehrere Instanzen des Datenträger Abwischens, die auf dasselbe Laufwerk ausgerichtet sind, führen dazu, dass alle Instanzen, mit Ausnahme der letzten, einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="aad32-114">Multiple instances of Disk Wipe that target the same drive cause all instances except the last one to report a failure</span></span>

<span data-ttu-id="aad32-115">Wenn Sie mehrere Instanzen der Datenträger Zurücksetzung starten und dann versuchen, dasselbe Laufwerk mithilfe von zwei separaten Datenträger Zurücksetzungs Instanzen zu wischen, melden alle Instanzen mit Ausnahme des letzten einen Fehler beim wischen des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="aad32-115">If you start multiple instances of Disk Wipe, and then try to wipe the same drive by using two separate Disk Wipe instances, all instances except the last one report a failure to wipe the drive.</span></span>

<span data-ttu-id="aad32-116">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="aad32-116">**Workaround:** None.</span></span>

### <span data-ttu-id="aad32-117">Bei der Datenträger Zurücksetzung werden möglicherweise nicht alle Daten auf Solid-State-Laufwerken mit Flash Speicher gelöscht</span><span class="sxs-lookup"><span data-stu-id="aad32-117">Disk Wipe may not clear all data on solid-state drives that have flash memory</span></span>

<span data-ttu-id="aad32-118">Wenn Sie Daten auf einem Solid-State-Laufwerk (SSD) mit Flash-Speicher löschen, werden alle Daten möglicherweise nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="aad32-118">If you use Disk Wipe to clear data on a solid-state drive (SSD) that has flash memory, all of the data may not be erased.</span></span> <span data-ttu-id="aad32-119">Dieses Problem tritt auf, weil die SSD-Firmware den physikalischen Standort von Schreibvorgängen steuert, während die Datenträgerbereinigung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aad32-119">This issue occurs because the SSD firmware controls the physical location of writes while Disk Wipe is running.</span></span>

<span data-ttu-id="aad32-120">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="aad32-120">**Workaround:** None.</span></span>

### <span data-ttu-id="aad32-121">System Wiederherstellung schlägt fehl, wenn Sie den Schlosser-Assistenten oder den Registrierungs-Editor ausführen</span><span class="sxs-lookup"><span data-stu-id="aad32-121">System restore fails when you run Locksmith Wizard or Registry Editor</span></span>

<span data-ttu-id="aad32-122">Wenn Sie den Schlosser-Assistenten, den Registrierungs-Editor und möglicherweise andere Tools ausführen, schlägt die System Wiederherstellung fehl.</span><span class="sxs-lookup"><span data-stu-id="aad32-122">If you run Locksmith Wizard, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="aad32-123">**Problemumgehung:** Schließen Sie Dart, und starten Sie es erneut, und starten Sie dann die System Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="aad32-123">**Workaround:** Close and restart DaRT, and then start System Restore.</span></span>

### <span data-ttu-id="aad32-124">Der System Datei-Checker-Scan (SFC) kann nicht ausgeführt werden, nachdem Sie den Schlosser-Assistenten oder die Computer Verwaltung gestartet und geschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="aad32-124">System File Checker (SFC) Scan fails to run after you start and close Locksmith Wizard or Computer Management</span></span>

<span data-ttu-id="aad32-125">Wenn Sie den Schlosser-Assistenten oder die Tools in der Computer Verwaltung starten und dann schließen, kann die System Dateiprüfung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="aad32-125">If you start and then close Locksmith Wizard or tools in Computer Management, System File Checker fails to run.</span></span>

<span data-ttu-id="aad32-126">**Problemumgehung:** Schließen Sie Dart, und starten Sie es erneut, und starten Sie dann die System Dateiprüfung.</span><span class="sxs-lookup"><span data-stu-id="aad32-126">**Workaround:** Close and restart DaRT, and then start System File Checker.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> <span data-ttu-id="aad32-127">Dart-Installationsprogramm schlägt nicht fehl, wenn das Windows Assessment-und Deployment Kit nicht installiert ist</span><span class="sxs-lookup"><span data-stu-id="aad32-127">DaRT installer does not fail when the Windows Assessment and Deployment Kit is not installed</span></span>

<span data-ttu-id="aad32-128">Wenn Sie Dart 8,1 über die Befehlszeile zum Ausführen des Windows Installers (MSI) installieren und das Windows Assessment and Deployment Kit (WindowsADK) nicht installiert wurde, sollte die Dart-Installation fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="aad32-128">If you install DaRT 8.1 by using the command line to run the Windows Installer (.msi), and the Windows Assessment and Deployment Kit (WindowsADK) has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="aad32-129">Derzeit installiert das Dart 8,1-Installationsprogramm alle Komponenten mit Ausnahme des DART-Wiederherstellungs Bilds.</span><span class="sxs-lookup"><span data-stu-id="aad32-129">Currently, the DaRT 8.1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="aad32-130">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="aad32-130">**Workaround:** None.</span></span>

### <span data-ttu-id="aad32-131">Windows Defender kann nicht gestartet werden, nachdem der Schlosser-Assistent, der Registrierungs-Editor, Crash Analyzer und die Computer Verwaltung gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="aad32-131">Windows Defender cannot start after Locksmith Wizard, Registry Editor, Crash Analyzer, and Computer Management are started</span></span>

<span data-ttu-id="aad32-132">Windows Defender wird nicht gestartet, wenn Sie Schlosser-Assistent, Registrierungs-Editor, Crash Analyzer und Computer Verwaltung bereits begonnen haben.</span><span class="sxs-lookup"><span data-stu-id="aad32-132">Windows Defender does not start if you have already started Locksmith Wizard, Registry Editor, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="aad32-133">**Problemumgehung:** Schließen Sie Dart, und starten Sie es erneut, und starten Sie dann Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="aad32-133">**Workaround:** Close and restart DaRT, and then start Windows Defender.</span></span>

### <span data-ttu-id="aad32-134">Windows Defender kann langsam gestartet werden</span><span class="sxs-lookup"><span data-stu-id="aad32-134">Windows Defender may be slow to start</span></span>

<span data-ttu-id="aad32-135">Windows Defender benötigt manchmal einige Minuten, um zu starten.</span><span class="sxs-lookup"><span data-stu-id="aad32-135">Windows Defender sometimes takes a few minutes to start.</span></span> <span data-ttu-id="aad32-136">Auf der Statusleiste wird der aktuelle Ladestatus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aad32-136">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="aad32-137">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="aad32-137">**Workaround:** None.</span></span>

## <span data-ttu-id="aad32-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="aad32-138">Related topics</span></span>


[<span data-ttu-id="aad32-139">Informationen zu DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="aad32-139">About DaRT 8.1</span></span>](about-dart-81.md)

 

 





