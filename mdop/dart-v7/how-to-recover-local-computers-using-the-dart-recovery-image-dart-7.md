---
title: So stellen Sie lokale Computer mithilfe des DaRT-Wiederherstellungsabbilds wieder her
description: So stellen Sie lokale Computer mithilfe des DaRT-Wiederherstellungsabbilds wieder her
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810150"
---
# <span data-ttu-id="c6222-103">So stellen Sie lokale Computer mithilfe des DaRT-Wiederherstellungsabbilds wieder her</span><span class="sxs-lookup"><span data-stu-id="c6222-103">How to Recover Local Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="c6222-104">Wenn Sie einen lokalen Computer mithilfe von Microsoft Diagnostics and Recovery Toolset (Dart) 7 wiederherstellen möchten, müssen Sie physisch auf dem Computer des Endbenutzers anwesend sein, bei dem Probleme auftreten, bei denen Dart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c6222-104">To recover a local computer by using Microsoft Diagnostics and Recovery Toolset (DaRT) 7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span> <span data-ttu-id="c6222-105">Sie können Dart auch remote ausführen, indem Sie die Anweisungen zum [Wiederherstellen von Remotecomputern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)befolgen.</span><span class="sxs-lookup"><span data-stu-id="c6222-105">You can also run DaRT remotely by following the instructions at [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

**<span data-ttu-id="c6222-106">So stellen Sie einen lokalen Computer mithilfe von DART wieder her</span><span class="sxs-lookup"><span data-stu-id="c6222-106">To recover a local computer by using DaRT</span></span>**

1.  <span data-ttu-id="c6222-107">Wenn der Computer in das DART-Wiederherstellungsabbild gestartet wird, wird das Dialogfeld " **netstart** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6222-107">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="c6222-108">Sie werden gefragt, ob Sie Netzwerkdienste initialisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c6222-108">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="c6222-109">Wenn Sie auf **Ja**klicken, wird davon ausgegangen, dass ein DHCP-Server im Netzwerk vorhanden ist, und es wird versucht, eine IP-Adresse vom Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6222-109">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="c6222-110">Wenn das Netzwerk statische IP-Adressen statt DHCP verwendet, können Sie später das **TCP/IP-Konfigurations** Tool in DART verwenden, um eine statische IP-Adresse anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c6222-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="c6222-111">Wenn Sie den Netzwerk Initialisierungsprozess überspringen möchten, klicken Sie auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="c6222-111">To skip the network initialization process, click **No**.</span></span>

2.  <span data-ttu-id="c6222-112">Nachdem Sie das Dialogfeld Netzwerk Initialisierung aufgerufen haben, werden Sie gefragt, ob Sie die Laufwerkbuchstaben neu zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6222-112">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="c6222-113">Wenn Sie Windows Online ausführen, wird das System Volume in der Regel Laufwerk C zugeordnet. Wenn Sie jedoch Windows offline unter WinRE ausführen, wird das ursprüngliche System Volume möglicherweise einem anderen Laufwerk zugeordnet, was zu Verwirrung führen kann.</span><span class="sxs-lookup"><span data-stu-id="c6222-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="c6222-114">Wenn Sie sich für die Neuzuordnung entscheiden, versucht Dart, die Offline Laufwerkbuchstaben den Online Laufwerkbuchstaben zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c6222-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="c6222-115">Eine Neuzuordnung wird nur ausgeführt, wenn ein Offline Betriebssystem später im Startvorgang ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c6222-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

3.  <span data-ttu-id="c6222-116">Nach dem Dialogfeld erneute Zuordnung wird ein Dialogfeld **System Wiederherstellungsoptionen** angezeigt, in dem Sie aufgefordert werden, ein Tastaturlayout auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c6222-116">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="c6222-117">Anschließend werden das Systemstammverzeichnis, die Art des installierten Betriebssystems und die Partitionsgröße angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6222-117">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="c6222-118">Wenn Ihr Betriebssystem nicht aufgeführt ist und Sie vermuten, dass das Fehlen von Treibern eine mögliche Ursache für den Fehler ist, klicken Sie auf **Treiber laden** , um die Verdächtigen Treiber zu laden.</span><span class="sxs-lookup"><span data-stu-id="c6222-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="c6222-119">Sie werden aufgefordert, das Installationsmedium für das Gerät einzufügen und den Treiber auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c6222-119">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="c6222-120">Wählen Sie die Installation aus, die Sie reparieren oder diagnostizieren möchten, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="c6222-120">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="c6222-121">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="c6222-121">Note</span></span>**  
    <span data-ttu-id="c6222-122">Wenn die Windows-Wiederherstellungsumgebung (WinRE) erkennt oder vermutet, dass Windows 7 beim letzten Versuch nicht ordnungsgemäß gestartet wurde, wird die **Startreparatur** möglicherweise automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="c6222-122">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. <span data-ttu-id="c6222-123">Klicken Sie im Fenster **System Wiederherstellungsoptionen** auf **Microsoft-Diagnose-und Wiederherstellungs-Toolset**.</span><span class="sxs-lookup"><span data-stu-id="c6222-123">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="c6222-124">Das Fenster " **Diagnose-und Wiederherstellungs-Toolset** " wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c6222-124">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="c6222-125">Sie können nun alle einzelnen Tools oder Assistenten ausführen, die beim Erstellen des DART-Wiederherstellungs Bilds enthalten waren.</span><span class="sxs-lookup"><span data-stu-id="c6222-125">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="c6222-126">Sie können im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf **Hilfe** klicken, um die Clienthilfedatei zu öffnen, die detaillierte Anweisungen und Informationen zum Ausführen der einzelnen Dart-Tools enthält.</span><span class="sxs-lookup"><span data-stu-id="c6222-126">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="c6222-127">Sie können auch im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf den **Lösungs-Assistenten** klicken, um das optimale Tool für die Situation zu wählen, das auf einem kurzen, vom Assistenten bereitgestellten Interview basiert.</span><span class="sxs-lookup"><span data-stu-id="c6222-127">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="c6222-128">Allgemeine Informationen zu den Dart-Tools finden Sie unter [Übersicht über die Tools in DART 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="c6222-128">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

**<span data-ttu-id="c6222-129">So führen Sie Dart an der Eingabeaufforderung aus</span><span class="sxs-lookup"><span data-stu-id="c6222-129">To run DaRT at the command prompt</span></span>**

1. <span data-ttu-id="c6222-130">Sie können Dart an der Eingabeaufforderung ausführen, indem Sie den Befehl **netstart.exe** angeben und einen der folgenden Parameter verwenden:</span><span class="sxs-lookup"><span data-stu-id="c6222-130">You can run DaRT at the command prompt by specifying the **netstart.exe** command and by using any of the following parameters:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="c6222-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6222-131">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="c6222-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6222-132">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="c6222-133">-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="c6222-133">-network</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c6222-134">Initialisiert die Netzwerkdienste.</span><span class="sxs-lookup"><span data-stu-id="c6222-134">Initializes the network services.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="c6222-135">-Erneutes Einhängen</span><span class="sxs-lookup"><span data-stu-id="c6222-135">-remount</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c6222-136">Ordnet die Laufwerkbuchstaben erneut zu.</span><span class="sxs-lookup"><span data-stu-id="c6222-136">Remaps the drive letters.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="c6222-137">-Aufforderung</span><span class="sxs-lookup"><span data-stu-id="c6222-137">-prompt</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c6222-138">Zeigt Nachrichten an, in denen der Endbenutzer angeben soll, ob das Netzwerk initialisiert und die Laufwerke neu zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6222-138">Displays messages asking the end user to specify whether to initialize the network and remap the drives.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="c6222-139">Wichtig</span><span class="sxs-lookup"><span data-stu-id="c6222-139">Important</span></span></strong><br/><p><span data-ttu-id="c6222-140">Die Antwort des Endbenutzers auf die Eingabeaufforderungen überschreibt die Switches-Netzwerk und-erneute Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c6222-140">The end user’s response to the prompts overrides the -network and -remount switches.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="c6222-141">Sie können Dart so anpassen, dass ein Computer, der in DART bootet, automatisch das **Remote Verbindungs** Tool öffnet, das zum Einrichten einer Remoteverbindung mit dem Helpdesk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6222-141">You can customize DaRT so that a computer that boots into DaRT automatically opens the **Remote Connection** tool that is used to establish a remote connection with the help desk.</span></span>

## <span data-ttu-id="c6222-142">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c6222-142">Related topics</span></span>


[<span data-ttu-id="c6222-143">Wiederherstellen von Computern mithilfe von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="c6222-143">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









