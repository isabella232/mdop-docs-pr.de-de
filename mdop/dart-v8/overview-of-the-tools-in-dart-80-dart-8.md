---
title: Übersicht über die Tools in DaRT 8.0
description: Übersicht über die Tools in DaRT 8.0
author: dansimp
ms.assetid: 1766c82e-c099-47d4-b186-4689b026a7e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: a058f6018888f446782aa8f3a18ee89570840c2a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810663"
---
# <span data-ttu-id="fcc26-103">Übersicht über die Tools in DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="fcc26-103">Overview of the Tools in DaRT 8.0</span></span>


<span data-ttu-id="fcc26-104">Im Fenster **Diagnose-und Wiederherstellungs-Toolset** in Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 können Sie alle einzelnen Tools starten, die Sie beim Erstellen des Dart 8,0-Wiederherstellungs Bilds hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-104">From the **Diagnostics and Recovery Toolset** window in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, you can start any of the individual tools that you include when you create the DaRT 8.0 recovery image.</span></span> <span data-ttu-id="fcc26-105">Informationen zum Zugriff auf das Toolset " **Diagnose-und Wiederherstellungstools** " finden Sie unter [Wiederherstellen von lokalen Computern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="fcc26-105">For information about how to access the **Diagnostics and Recovery Toolset** window, see [How to Recover Local Computers by Using the DaRT Recovery Image](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="fcc26-106">Wenn Sie verfügbar ist, können Sie den **Lösungs-Assistenten** im Fenster **Diagnose-und Wiederherstellungstool Toolset** verwenden, um das Tool auszuwählen, das für Ihr jeweiliges Problem am besten geeignet ist, basierend auf einem kurzen Interview, das der Assistent bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fcc26-106">If it is available, you can use the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to select the tool that best addresses your particular issue, based on a brief interview that the wizard provides.</span></span>

## <span data-ttu-id="fcc26-107">Erkunden der Dart-Tools</span><span class="sxs-lookup"><span data-stu-id="fcc26-107">Exploring the DaRT tools</span></span>


<span data-ttu-id="fcc26-108">Eine Beschreibung der Dart-8,0-Tools folgt.</span><span class="sxs-lookup"><span data-stu-id="fcc26-108">A description of the DaRT 8.0 tools follows.</span></span>

### <span data-ttu-id="fcc26-109">Computerverwaltung</span><span class="sxs-lookup"><span data-stu-id="fcc26-109">Computer Management</span></span>

<span data-ttu-id="fcc26-110">**Computerverwaltung** ist eine Sammlung von Windows-Verwaltungstools, die Ihnen bei der Problembehandlung eines Problem Computers helfen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-110">**Computer Management** is a collection of Windows administrative tools that help you troubleshoot a problem computer.</span></span> <span data-ttu-id="fcc26-111">Sie können die Tools für die **Computer Verwaltung** in DART verwenden, um Systeminformationen und Ereignisprotokolle anzuzeigen, Datenträger zu verwalten, Autoruns aufzulisten und Dienste und Treiber zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="fcc26-111">You can use the **Computer Management** tools in DaRT to view system information and event logs, manage disks, list autoruns, and manage services and drivers.</span></span> <span data-ttu-id="fcc26-112">Die **Computer Verwaltungs** Konsole ist so angepasst, dass Sie Probleme diagnostizieren und beheben können, die das Starten des Windows-Betriebssystems verhindern könnten.</span><span class="sxs-lookup"><span data-stu-id="fcc26-112">The **Computer Management** console is customized to help you diagnose and repair problems that might be preventing the Windows operating system from starting.</span></span>

<span data-ttu-id="fcc26-113">**Hinweis**  Die Wiederherstellung von dynamischen Datenträgern mit Dart wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fcc26-113">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="fcc26-114">Absturzanalyse</span><span class="sxs-lookup"><span data-stu-id="fcc26-114">Crash Analyzer</span></span>

<span data-ttu-id="fcc26-115">Verwenden Sie den **Crash Analyzer-Assistenten** , um die Ursache für einen Computer Fehler schnell zu ermitteln, indem Sie die Speicherabbilddatei unter dem Windows-Betriebssystem analysieren, das Sie reparieren.</span><span class="sxs-lookup"><span data-stu-id="fcc26-115">Use the **Crash Analyzer Wizard** to quickly determine the cause of a computer failure by analyzing the memory dump file on the Windows operating system that you are repairing.</span></span> <span data-ttu-id="fcc26-116">**Crash Analyzer** untersucht die Speicherabbilddatei für den Treiber, der einen Fehler bei einem Computer verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="fcc26-116">**Crash Analyzer** examines the memory dump file for the driver that caused a computer to fail.</span></span> <span data-ttu-id="fcc26-117">Sie können dann den Problemgeräte Treiber mithilfe des Knotens **Dienste und Treiber** im Tool **Computer Verwaltung** deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fcc26-117">You can then disable the problem device driver by using the **Services and Drivers** node in the **Computer Management** tool.</span></span>

<span data-ttu-id="fcc26-118">Der **Absturzanalyse-Assistent** erfordert die Debugging-Tools für Windows und Symboldateien für das Betriebssystem, das Sie reparieren.</span><span class="sxs-lookup"><span data-stu-id="fcc26-118">The **Crash Analyzer Wizard** requires the Debugging Tools for Windows and symbol files for the operating system that you are repairing.</span></span> <span data-ttu-id="fcc26-119">Beim Erstellen des DART-Wiederherstellungs Bilds können beide Anforderungen berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="fcc26-119">You can include both requirements when you create the DaRT recovery image.</span></span> <span data-ttu-id="fcc26-120">Wenn Sie nicht im Wiederherstellungsabbild enthalten sind und Sie auf dem zu reparierenden Computer keinen Zugriff darauf haben, können Sie die Speicherabbilddatei auf einen anderen Computer kopieren und die eigenständige Version von **Crash Analyzer** verwenden, um das Problem zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="fcc26-120">If they are not included on the recovery image and you do not have access to them on the computer that you are repairing, you can copy the memory dump file to another computer and use the stand-alone version of **Crash Analyzer** to diagnose the problem.</span></span>

<span data-ttu-id="fcc26-121">Das Ausführen von **Crash Analyzer** ist eine gute Idee, auch wenn Sie den Computer umbilden möchten.</span><span class="sxs-lookup"><span data-stu-id="fcc26-121">Running **Crash Analyzer** is a good idea even if you plan to reimage the computer.</span></span> <span data-ttu-id="fcc26-122">Das Bild kann einen fehlerhaften Treiber aufweisen, der Probleme in Ihrer Umgebung verursacht.</span><span class="sxs-lookup"><span data-stu-id="fcc26-122">The image could have a defective driver that is causing problems in your environment.</span></span> <span data-ttu-id="fcc26-123">Durch Ausführen von **Crash Analyzer**können Sie Problem Treiber identifizieren und die Bildstabilität verbessern.</span><span class="sxs-lookup"><span data-stu-id="fcc26-123">By running **Crash Analyzer**, you can identify problem drivers and improve the image stability.</span></span>

<span data-ttu-id="fcc26-124">Weitere Informationen zu **Crash Analyzer**finden Sie unter [Diagnostizieren von System Fehlern mit Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="fcc26-124">For more information about **Crash Analyzer**, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md).</span></span>

### <span data-ttu-id="fcc26-125">Defender</span><span class="sxs-lookup"><span data-stu-id="fcc26-125">Defender</span></span>

<span data-ttu-id="fcc26-126">**Wichtig**  In Umgebungen mit dem bereitgestellten Dart Defender sollte stattdessen das WDOLHQ-Schutz Bild (Microsoft Defender offline) für die Malware Erkennung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcc26-126">**Important** Environments with the DaRT Defender deployed should instead use the Microsoft Defender Offline (WDO) protection image for malware detection.</span></span> <span data-ttu-id="fcc26-127">Aufgrund der Integration des Defender-Tools in DART können alle unterstützten Dart-Versions Bereitstellungen diese Antispamaktualisierungen nicht auf Ihre Dart-Bilder anwenden.</span><span class="sxs-lookup"><span data-stu-id="fcc26-127">Because of how the Defender tool integrates into DaRT, all supported DaRT version deployments cannot apply these anti-malware updates to their DaRT images.</span></span> <span data-ttu-id="fcc26-128">Weitere Informationen finden Sie unter [Microsoft Diagnostics and Recovery Toolset (Dart) Benutzer sollten Microsoft Defender Offline (WDOLHQ) für die Malware Erkennung verwenden – >](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md).</span><span class="sxs-lookup"><span data-stu-id="fcc26-128">For more information, see  [Microsoft Diagnostics and Recovery Toolset (DaRT) users should use Microsoft Defender Offline (WDO) for malware detection-->](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md).</span></span>

 

<span data-ttu-id="fcc26-129">**Defender** kann dabei helfen, Malware und unerwünschte Software zu erkennen, und warnt Sie vor Sicherheitsrisiken.</span><span class="sxs-lookup"><span data-stu-id="fcc26-129">**Defender** can help detect malware and unwanted software and warn you of security risks.</span></span> <span data-ttu-id="fcc26-130">Sie können dieses Tool verwenden, um einen Computer zu überprüfen und Malware zu entfernen, selbst wenn das installierte Windows-Betriebssystem nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcc26-130">You can use this tool to scan a computer for and remove malware even when the installed Windows operating system is not running.</span></span> <span data-ttu-id="fcc26-131">Wenn **Defender** bösartige oder unerwünschte Software erkennt, werden Sie aufgefordert, die einzelnen Elemente zu entfernen, zu isolieren oder zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="fcc26-131">When **Defender** detects malicious or unwanted software, it prompts you to remove, quarantine, or allow for each item.</span></span>

<span data-ttu-id="fcc26-132">Malware, die Rootkits verwendet, kann sich selbst vom ausgeführten Betriebssystem maskieren.</span><span class="sxs-lookup"><span data-stu-id="fcc26-132">Malware that uses rootkits can mask itself from the running operating system.</span></span> <span data-ttu-id="fcc26-133">Wenn sich ein Rootkit-fähiger Virus oder eine Spyware auf einem Computer befindet, können die meisten Tools zur Echtzeitüberprüfung und-Entfernung Sie nicht mehr sehen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-133">If a rootkit-enabled virus or spyware is in a computer, most real-time scanning and removal tools can no longer see it or remove it.</span></span> <span data-ttu-id="fcc26-134">Da Sie das Problem Computer in DART Booten und das installierte Betriebssystem offline ist, können Sie das Rootkit erkennen, ohne dass es sich selbst maskieren kann.</span><span class="sxs-lookup"><span data-stu-id="fcc26-134">Because you boot the problem computer into DaRT and the installed operating system is offline, you can detect the rootkit without it being able to mask itself.</span></span>

### <span data-ttu-id="fcc26-135">Disk Commander</span><span class="sxs-lookup"><span data-stu-id="fcc26-135">Disk Commander</span></span>

<span data-ttu-id="fcc26-136">Mit **Disk Commander** können Sie Datenträgerpartitionen oder-Volumes mithilfe eines der folgenden Wiederherstellungsprozesse wiederherstellen und reparieren:</span><span class="sxs-lookup"><span data-stu-id="fcc26-136">**Disk Commander** lets you recover and repair disk partitions or volumes by using one of the following recovery processes:</span></span>

-   <span data-ttu-id="fcc26-137">Wiederherstellen des Master Boot Record (MBR)</span><span class="sxs-lookup"><span data-stu-id="fcc26-137">Restore the master boot record (MBR)</span></span>

-   <span data-ttu-id="fcc26-138">Wiederherstellen eines oder mehrerer verlorener Volumes</span><span class="sxs-lookup"><span data-stu-id="fcc26-138">Recover one or more lost volumes</span></span>

-   <span data-ttu-id="fcc26-139">Wiederherstellen von Partitionstabellen aus der **Disk Commander** -Sicherung</span><span class="sxs-lookup"><span data-stu-id="fcc26-139">Restore partition tables from **Disk Commander** backup</span></span>

-   <span data-ttu-id="fcc26-140">Speichern von Partitionstabellen auf der **Disk Commander** -Sicherung</span><span class="sxs-lookup"><span data-stu-id="fcc26-140">Save partition tables to **Disk Commander** backup</span></span>

<span data-ttu-id="fcc26-141">**Warnung**  Wir empfehlen, dass Sie eine Diskette sichern, bevor Sie **Disk Commander** verwenden, um Sie zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="fcc26-141">**Warning** We recommend that you back up a disk before you use **Disk Commander** to repair it.</span></span> <span data-ttu-id="fcc26-142">Durch die Verwendung von **Disk Commander**können Sie Volumes potenziell beschädigen und darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-142">By using **Disk Commander**, you can potentially damage volumes and make them inaccessible.</span></span> <span data-ttu-id="fcc26-143">Darüber hinaus können Änderungen an einem Volume Auswirkungen auf andere Volumes haben, da Volumes auf einem Datenträger eine Partitionstabelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="fcc26-143">Additionally, changes to one volume can affect other volumes because volumes on a disk share a partition table.</span></span>

 

<span data-ttu-id="fcc26-144">**Hinweis**  Die Wiederherstellung von dynamischen Datenträgern mit Dart wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fcc26-144">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="fcc26-145">Datenträger Zurücksetzung</span><span class="sxs-lookup"><span data-stu-id="fcc26-145">Disk Wipe</span></span>

<span data-ttu-id="fcc26-146">Sie können die Daten **Träger** Zurücksetzung verwenden, um alle Daten von einem Datenträger oder Volume zu löschen, selbst die Daten, die nach dem Neuformatieren einer Festplatte zurückbleiben.</span><span class="sxs-lookup"><span data-stu-id="fcc26-146">You can use **Disk Wipe** to delete all data from a disk or volume, even the data that is left behind after you reformat a hard disk drive.</span></span> <span data-ttu-id="fcc26-147">Mit der **Datenträger** Zurücksetzung können Sie entweder ein Single-Pass-Überschreibungs-oder ein vier-Pass-überschreiben auswählen, das den aktuellen US-Standards für Verteidigungsministeriums entspricht.</span><span class="sxs-lookup"><span data-stu-id="fcc26-147">**Disk Wipe** lets you select from either a single-pass overwrite or a four-pass overwrite, which meets current U.S. Department of Defense standards.</span></span>

<span data-ttu-id="fcc26-148">**Warnung**  Nach dem abwischen einer Festplatte oder eines Volumes können Sie die Daten nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-148">**Warning** After wiping a disk or volume, you cannot recover the data.</span></span> <span data-ttu-id="fcc26-149">Überprüfen Sie die Größe und Beschriftung eines Volumes, bevor Sie es löschen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-149">Verify the size and label of a volume before erasing it.</span></span>

 

### <span data-ttu-id="fcc26-150">Explorer</span><span class="sxs-lookup"><span data-stu-id="fcc26-150">Explorer</span></span>

<span data-ttu-id="fcc26-151">Mit dem **Explorer** -Tool können Sie das Dateisystem und die Netzwerkfreigaben des Computers durchsuchen, damit Sie wichtige Daten entfernen können, die der Benutzer auf dem lokalen Laufwerk gespeichert hat, bevor Sie versuchen, den Computer zu reparieren oder zu reimagen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-151">The **Explorer** tool lets you browse the computer’s file system and network shares so that you can remove important data that the user stored on the local drive before you try to repair or reimage the computer.</span></span> <span data-ttu-id="fcc26-152">Und da Sie Laufwerkbuchstaben zu Netzwerkfreigaben zuordnen können, können Sie Dateien problemlos vom Computer in das Netzwerk kopieren und verschieben, um Sie zu verwahren oder vom Netzwerk auf den Computer zu übertragen, um Sie wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-152">And because you can map drive letters to network shares, you can easily copy and move files from the computer to the network for safekeeping or from the network to the computer to restore them.</span></span>

### <span data-ttu-id="fcc26-153">Datei Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="fcc26-153">File Restore</span></span>

<span data-ttu-id="fcc26-154">Mit der **Datei Wiederherstellung** können Sie versuchen, Dateien wiederherzustellen, die versehentlich gelöscht wurden oder die zu groß waren, um in den Papierkorb zu passen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-154">**File Restore** lets you try to restore files that were accidentally deleted or that were too big to fit in the Recycle Bin.</span></span> <span data-ttu-id="fcc26-155">Die **Datei Wiederherstellung** ist nicht auf reguläre Datenträger Volumes limitiert, kann aber Dateien auf verlorenen Volumes oder auf Volumes finden und wiederherstellen, die von BitLocker verschlüsselt wurden.</span><span class="sxs-lookup"><span data-stu-id="fcc26-155">**File Restore** is not limited to regular disk volumes, but can find and restore files on lost volumes or on volumes that are encrypted by BitLocker.</span></span>

<span data-ttu-id="fcc26-156">**Hinweis**  Die Wiederherstellung von dynamischen Datenträgern mit Dart wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fcc26-156">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="fcc26-157">Dateisuche</span><span class="sxs-lookup"><span data-stu-id="fcc26-157">File Search</span></span>

<span data-ttu-id="fcc26-158">Bevor Sie einen Computer erneut abbilden, ist das Wiederherstellen von Dateien von der lokalen Festplatte wichtig, insbesondere dann, wenn der Benutzer die Dateien möglicherweise nicht anderweitig gesichert oder gespeichert hat.</span><span class="sxs-lookup"><span data-stu-id="fcc26-158">Before reimaging a computer, recovering files from the local hard disk is important, especially when the user might not have backed up or stored the files elsewhere.</span></span>

<span data-ttu-id="fcc26-159">Das **Such** Tool öffnet ein **Datei Such** Fenster, das Sie zum Suchen von Dokumenten verwenden können, wenn Sie den Dateipfad nicht kennen oder nach allgemeinen Arten von Dateien auf allen lokalen Festplatten suchen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-159">The **Search** tool opens a **File Search** window that you can use to find documents when you do not know the file path or to search for general kinds of files across all local hard disks.</span></span> <span data-ttu-id="fcc26-160">In bestimmten Pfaden können Sie nach bestimmten Dateinamen Mustern suchen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-160">You can search for specific file-name patterns in specific paths.</span></span> <span data-ttu-id="fcc26-161">Sie können die Ergebnisse auch auf einen Datumsbereich oder einen Größenbereich begrenzen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-161">You can also limit results to a date range or size range.</span></span>

### <span data-ttu-id="fcc26-162">Hotfix-Deinstallation</span><span class="sxs-lookup"><span data-stu-id="fcc26-162">Hotfix Uninstall</span></span>

<span data-ttu-id="fcc26-163">Mit dem **Hotfix-Deinstallations-Assistenten** können Sie Hotfixes oder Service Packs vom Windows-Betriebssystem auf dem Computer entfernen, den Sie reparieren.</span><span class="sxs-lookup"><span data-stu-id="fcc26-163">The **Hotfix Uninstall Wizard** lets you remove hotfixes or service packs from the Windows operating system on the computer that you are repairing.</span></span> <span data-ttu-id="fcc26-164">Verwenden Sie dieses Tool, wenn ein Hotfix oder Service Pack vermutet wird, um zu verhindern, dass das Betriebssystem gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="fcc26-164">Use this tool when a hotfix or service pack is suspected in preventing the operating system from starting.</span></span>

<span data-ttu-id="fcc26-165">Wir empfehlen, dass Sie nur jeweils einen Hotfix deinstallieren, auch wenn Sie mit dem Tool mehr als eine deinstallieren können.</span><span class="sxs-lookup"><span data-stu-id="fcc26-165">We recommend that you uninstall only one hotfix at a time, even though the tool lets you uninstall more than one.</span></span>

<span data-ttu-id="fcc26-166">**Wichtig**  Programme, die nach der Installation eines Hotfixes installiert oder aktualisiert wurden, funktionieren möglicherweise nicht mehr ordnungsgemäß, nachdem Sie einen Hotfix deinstalliert haben.</span><span class="sxs-lookup"><span data-stu-id="fcc26-166">**Important** Programs that were installed or updated after a hotfix was installed might not work correctly after you uninstall a hotfix.</span></span>

 

### <span data-ttu-id="fcc26-167">Schlosser</span><span class="sxs-lookup"><span data-stu-id="fcc26-167">Locksmith</span></span>

<span data-ttu-id="fcc26-168">Mit dem **Schlosser-Assistenten** können Sie das Kennwort für ein lokales Konto auf dem Windows-Betriebssystem festlegen oder ändern, das Sie analysieren oder reparieren.</span><span class="sxs-lookup"><span data-stu-id="fcc26-168">The **Locksmith Wizard** lets you set or change the password for any local account on the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="fcc26-169">Sie müssen das aktuelle Kennwort nicht kennen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-169">You do not have to know the current password.</span></span> <span data-ttu-id="fcc26-170">Das von Ihnen festgelegte Kennwort muss jedoch allen Anforderungen entsprechen, die von einem lokalen Gruppenrichtlinienobjekt definiert werden.</span><span class="sxs-lookup"><span data-stu-id="fcc26-170">However, the password that you set must comply with any requirements that are defined by a local Group Policy Object.</span></span> <span data-ttu-id="fcc26-171">Dazu gehören Kennwortlänge und-Komplexität.</span><span class="sxs-lookup"><span data-stu-id="fcc26-171">This includes password length and complexity.</span></span>

<span data-ttu-id="fcc26-172">Sie können **Schlosser** verwenden, wenn das Kennwort für ein lokales Konto, beispielsweise das lokale Administrator Konto, unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="fcc26-172">You can use **Locksmith** when the password for a local account, such as the local Administrator account, is unknown.</span></span> <span data-ttu-id="fcc26-173">Sie können **Schlosser** nicht verwenden, um Kennwörter für Domänenkonten einzurichten.</span><span class="sxs-lookup"><span data-stu-id="fcc26-173">You cannot use **Locksmith** to set passwords for domain accounts.</span></span>

### <span data-ttu-id="fcc26-174">Registrierungs-Editor</span><span class="sxs-lookup"><span data-stu-id="fcc26-174">Registry Editor</span></span>

<span data-ttu-id="fcc26-175">Sie können den **Registrierungs-Editor** verwenden, um auf die Registrierung des Windows-Betriebssystems zuzugreifen und diese zu ändern, das Sie analysieren oder reparieren.</span><span class="sxs-lookup"><span data-stu-id="fcc26-175">You can use **Registry Editor** to access and change the registry of the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="fcc26-176">Dazu gehören das Hinzufügen, entfernen und Bearbeiten von Schlüsseln und Werten sowie das Importieren von Registrierungsdateien (reg).</span><span class="sxs-lookup"><span data-stu-id="fcc26-176">This includes adding, removing, and editing keys and values, and importing registry (.reg) files.</span></span>

<span data-ttu-id="fcc26-177">**Warnung**  Ernsthafte Probleme können auftreten, wenn Sie die Registrierung mit dem **Registrierungs-Editor**falsch ändern.</span><span class="sxs-lookup"><span data-stu-id="fcc26-177">**Warning** Serious problems can occur if you change the registry incorrectly by using **Registry Editor**.</span></span> <span data-ttu-id="fcc26-178">Diese Probleme können dazu führen, dass Sie das Betriebssystem neu installieren müssen.</span><span class="sxs-lookup"><span data-stu-id="fcc26-178">These problems might require you to reinstall the operating system.</span></span> <span data-ttu-id="fcc26-179">Bevor Sie Änderungen an der Registrierung vornehmen, sollten Sie alle wichtigen Daten auf dem Computer sichern.</span><span class="sxs-lookup"><span data-stu-id="fcc26-179">Before you make changes to the registry, you should back up any valued data on the computer.</span></span> <span data-ttu-id="fcc26-180">Ändern Sie die Registrierung auf Ihr eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="fcc26-180">Change the registry at your own risk.</span></span>

 

### <span data-ttu-id="fcc26-181">SFC-Scan</span><span class="sxs-lookup"><span data-stu-id="fcc26-181">SFC Scan</span></span>

<span data-ttu-id="fcc26-182">Das **sfc-Scan** -Tool startet den **Systemdateireparatur-Assistenten** und ermöglicht Ihnen, Systemdateien zu reparieren, die das Starten des installierten Windows-Betriebssystems verhindern.</span><span class="sxs-lookup"><span data-stu-id="fcc26-182">The **SFC Scan** tool starts the **System File Repair Wizard** and lets you repair system files that are preventing the installed Windows operating system from starting.</span></span> <span data-ttu-id="fcc26-183">Der **Systemdatei-Reparatur-Assistent** kann Systemdateien, die beschädigt oder nicht vorhanden sind, automatisch reparieren, oder Sie können Sie vor dem Ausführen von Reparaturen auffordern.</span><span class="sxs-lookup"><span data-stu-id="fcc26-183">The **System File Repair Wizard** can automatically repair system files that are corrupted or missing, or it can prompt you before it performs any repairs.</span></span>

### <span data-ttu-id="fcc26-184">Lösungs-Assistent</span><span class="sxs-lookup"><span data-stu-id="fcc26-184">Solution Wizard</span></span>

<span data-ttu-id="fcc26-185">Der **Lösungs-Assistent** stellt eine Reihe von Fragen und empfiehlt dann basierend auf Ihren Antworten das beste Tool für die Situation.</span><span class="sxs-lookup"><span data-stu-id="fcc26-185">The **Solution Wizard** presents a series of questions and then recommends the best tool for the situation, based on your answers.</span></span> <span data-ttu-id="fcc26-186">Dieser Assistent hilft Ihnen bei der Entscheidung, welches Tool Sie verwenden sollen, wenn Sie mit den Tools in DART nicht vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="fcc26-186">This wizard helps you determine which tool to use when you are not familiar with the tools in DaRT.</span></span>

### <span data-ttu-id="fcc26-187">TCP/IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="fcc26-187">TCP/IP Config</span></span>

<span data-ttu-id="fcc26-188">Wenn Sie einen Problem Computer in DART starten, wird er so eingestellt, dass seine TCP/IP-Konfiguration (IP-Adresse und DNS-Server) automatisch vom Dynamic Host Configuration Protocol (DHCP) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fcc26-188">When you boot a problem computer into DaRT, it is set to automatically obtain its TCP/IP configuration (IP address and DNS server) from Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="fcc26-189">Wenn DHCP nicht verfügbar ist, können Sie TCP/IP mithilfe des **TCP/IP-Konfigurations** Tools manuell konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fcc26-189">If DHCP is unavailable, you can manually configure TCP/IP by using the **TCP/IP Config** tool.</span></span> <span data-ttu-id="fcc26-190">Wählen Sie zuerst einen Netzwerkadapter aus, und konfigurieren Sie dann die IP-Adresse und den DNS-Server für diesen Adapter.</span><span class="sxs-lookup"><span data-stu-id="fcc26-190">You first select a network adapter, and then configure the IP address and DNS server for that adapter.</span></span>

## <span data-ttu-id="fcc26-191">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="fcc26-191">Related topics</span></span>


[<span data-ttu-id="fcc26-192">Erste Schritte mit DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="fcc26-192">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

 

 





