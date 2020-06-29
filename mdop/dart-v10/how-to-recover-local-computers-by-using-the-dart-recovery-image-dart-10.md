---
title: So stellen Sie lokale Computer mit dem DaRT-Wiederherstellungsabbild wieder her
description: So stellen Sie lokale Computer mit dem DaRT-Wiederherstellungsabbild wieder her
author: dansimp
ms.assetid: a6adc717-827c-45e8-b9c3-06d0e919e0bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06e8ad82f869568c9fa25fcbb16825b2abff06f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809445"
---
# <span data-ttu-id="a0f33-103">So stellen Sie lokale Computer mit dem DaRT-Wiederherstellungsabbild wieder her</span><span class="sxs-lookup"><span data-stu-id="a0f33-103">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="a0f33-104">Verwenden Sie diese Anweisungen zum Wiederherstellen eines Computers, wenn Sie physisch am Endbenutzercomputer anwesend sind, bei dem Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="a0f33-104">Use these instructions to recover a computer when you are physically present at the end-user computer that is experiencing problems.</span></span>

**<span data-ttu-id="a0f33-105">Wiederherstellen eines lokalen Computers mithilfe des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="a0f33-105">How to recover a local computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="a0f33-106">Starten Sie den Endbenutzercomputer mithilfe des Microsoft Diagnostics and Recovery Toolset (Dart) 10-Wiederherstellungsabbilds.</span><span class="sxs-lookup"><span data-stu-id="a0f33-106">Boot the end-user computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

    <span data-ttu-id="a0f33-107">Wenn der Computer in das DART 10-Wiederherstellungsabbild gestartet wird, wird das Dialogfeld " **netstart** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a0f33-107">As the computer is booting into the DaRT 10 recovery image, the **NetStart** dialog box appears.</span></span>

2.  <span data-ttu-id="a0f33-108">Wenn Sie gefragt werden, ob Sie Netzwerkdienste initialisieren möchten, wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="a0f33-108">When you are asked whether you want to initialize network services, select one of the following:</span></span>

    <span data-ttu-id="a0f33-109">**Ja** – es wird davon ausgegangen, dass ein DHCP-Server im Netzwerk vorhanden ist, und es wird versucht, eine IP-Adresse vom Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a0f33-109">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="a0f33-110">Wenn das Netzwerk statische IP-Adressen statt DHCP verwendet, können Sie später das **TCP/IP-Konfigurations** Tool in DART verwenden, um eine statische IP-Adresse anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a0f33-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="a0f33-111">**Nein** – überspringen Sie den Netzwerk Initialisierungsprozess.</span><span class="sxs-lookup"><span data-stu-id="a0f33-111">**No** - skip the network initialization process.</span></span>

3.  <span data-ttu-id="a0f33-112">Geben Sie an, ob Sie die Laufwerkbuchstaben neu zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="a0f33-112">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="a0f33-113">Wenn Sie Windows Online ausführen, wird das System Volume in der Regel Laufwerk C zugeordnet. Wenn Sie jedoch Windows offline unter WinRE ausführen, wird das ursprüngliche System Volume möglicherweise einem anderen Laufwerk zugeordnet, was zu Verwirrung führen kann.</span><span class="sxs-lookup"><span data-stu-id="a0f33-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="a0f33-114">Wenn Sie sich für die Neuzuordnung entscheiden, versucht Dart, die Offline Laufwerkbuchstaben den Online Laufwerkbuchstaben zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a0f33-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="a0f33-115">Eine Neuzuordnung wird nur ausgeführt, wenn ein Offline Betriebssystem später im Startvorgang ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a0f33-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="a0f33-116">Wählen Sie im Dialogfeld **System Wiederherstellungsoptionen** ein Tastaturlayout aus.</span><span class="sxs-lookup"><span data-stu-id="a0f33-116">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5.  <span data-ttu-id="a0f33-117">Überprüfen Sie das angezeigte Systemstammverzeichnis, die Art des installierten Betriebssystems und die Partitionsgröße.</span><span class="sxs-lookup"><span data-stu-id="a0f33-117">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="a0f33-118">Wenn Ihr Betriebssystem nicht aufgeführt ist und Sie vermuten, dass das Fehlen von Treibern eine mögliche Ursache für den Fehler ist, klicken Sie auf **Treiber laden** , um die Verdächtigen Treiber zu laden, und legen Sie dann das Installationsmedium für das Gerät ein, und wählen Sie den Treiber aus.</span><span class="sxs-lookup"><span data-stu-id="a0f33-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6.  <span data-ttu-id="a0f33-119">Wählen Sie die Installation aus, die Sie reparieren oder diagnostizieren möchten, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0f33-119">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="a0f33-120">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="a0f33-120">Note</span></span>**  
    <span data-ttu-id="a0f33-121">Wenn die Windows-Wiederherstellungsumgebung (WinRE) erkennt oder vermutet, dass Windows 10 beim letzten Versuch nicht ordnungsgemäß gestartet wurde, wird die **Startreparatur** möglicherweise automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="a0f33-121">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 10 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="a0f33-122">Klicken Sie im Fenster **System Wiederherstellungsoptionen** auf **Microsoft-Diagnose-und Wiederherstellungs-Toolset**.</span><span class="sxs-lookup"><span data-stu-id="a0f33-122">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="a0f33-123">Das Fenster " **Diagnose-und Wiederherstellungs-Toolset** " wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a0f33-123">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="a0f33-124">Sie können nun alle einzelnen Tools oder Assistenten ausführen, die beim Erstellen des DART-Wiederherstellungs Bilds enthalten waren.</span><span class="sxs-lookup"><span data-stu-id="a0f33-124">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="a0f33-125">Sie können im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf **Hilfe** klicken, um die Clienthilfedatei zu öffnen, die detaillierte Anweisungen und Informationen zum Ausführen der einzelnen Dart-Tools enthält.</span><span class="sxs-lookup"><span data-stu-id="a0f33-125">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="a0f33-126">Sie können auch im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf den **Lösungs-Assistenten** klicken, um das optimale Tool für die Situation zu wählen, das auf einem kurzen, vom Assistenten bereitgestellten Interview basiert.</span><span class="sxs-lookup"><span data-stu-id="a0f33-126">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="a0f33-127">Allgemeine Informationen zu den Dart-Tools finden Sie unter [Übersicht über die Tools in DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="a0f33-127">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

**<span data-ttu-id="a0f33-128">Ausführen von DART an der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="a0f33-128">How to run DaRT at the command prompt</span></span>**

- <span data-ttu-id="a0f33-129">Wenn Sie Dart an der Eingabeaufforderung ausführen möchten, geben Sie den Befehl **netstart.exe** an, und verwenden Sie dann einen der folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="a0f33-129">To run DaRT at the command prompt, specify the **netstart.exe** command then use any of the following parameters:</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong><span data-ttu-id="a0f33-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0f33-130">Parameter</span></span></strong></p></td>
  <td align="left"><p><strong><span data-ttu-id="a0f33-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0f33-131">Description</span></span></strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="a0f33-132">-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="a0f33-132">-network</span></span></p></td>
  <td align="left"><p><span data-ttu-id="a0f33-133">Initialisiert die Netzwerkdienste.</span><span class="sxs-lookup"><span data-stu-id="a0f33-133">Initializes the network services.</span></span></p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="a0f33-134">-Erneutes Einhängen</span><span class="sxs-lookup"><span data-stu-id="a0f33-134">-remount</span></span></p></td>
  <td align="left"><p><span data-ttu-id="a0f33-135">Ordnet die Laufwerkbuchstaben erneut zu.</span><span class="sxs-lookup"><span data-stu-id="a0f33-135">Remaps the drive letters.</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="a0f33-136">-Aufforderung</span><span class="sxs-lookup"><span data-stu-id="a0f33-136">-prompt</span></span></p></td>
  <td align="left"><p><span data-ttu-id="a0f33-137">Zeigt Nachrichten an, die den Endbenutzer bitten, anzugeben, ob das Netzwerk initialisiert und die Laufwerke neu zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a0f33-137">Displays messages that ask the end user to specify whether to initialize the network and remap the drives.</span></span></p>
  <div class="alert">
  <strong><span data-ttu-id="a0f33-138">Warnung</span><span class="sxs-lookup"><span data-stu-id="a0f33-138">Warning</span></span></strong><br/><p><span data-ttu-id="a0f33-139">Die Antwort des Endbenutzers auf die Eingabeaufforderung überschreibt die Switches – Netzwerk und – erneute Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="a0f33-139">The end user’s response to the prompt overrides the –network and –remount switches.</span></span></p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## <span data-ttu-id="a0f33-140">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a0f33-140">Related topics</span></span>


[<span data-ttu-id="a0f33-141">Vorgänge für DaRT 10</span><span class="sxs-lookup"><span data-stu-id="a0f33-141">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="a0f33-142">Wiederherstellen von Computern mithilfe von DaRT 10</span><span class="sxs-lookup"><span data-stu-id="a0f33-142">Recovering Computers Using DaRT 10</span></span>](recovering-computers-using-dart-10.md)









