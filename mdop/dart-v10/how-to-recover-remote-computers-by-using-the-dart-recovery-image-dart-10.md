---
title: So stellen Sie Remotecomputer mit dem DaRT-Wiederherstellungsabbild wieder her
description: So stellen Sie Remotecomputer mit dem DaRT-Wiederherstellungsabbild wieder her
author: dansimp
ms.assetid: c0062208-39cd-4e01-adf8-36a11386e2ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 42d49c6c5c494da866785764e1c93a6bda2d667e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809448"
---
# <span data-ttu-id="1b3d1-103">So stellen Sie Remotecomputer mit dem DaRT-Wiederherstellungsabbild wieder her</span><span class="sxs-lookup"><span data-stu-id="1b3d1-103">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="1b3d1-104">Verwenden Sie das Feature Remote Verbindung in Microsoft Diagnostics and Recovery Toolset (Dart) 10, um die Dart-Tools Remote auf einem Endbenutzercomputer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-104">Use the Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 10 to run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="1b3d1-105">Nachdem der Endbenutzer bestimmte Informationen dem Administrator oder Helpdesk-Mitarbeiter zur Verfügung gestellt hat, kann der IT-Administrator oder der Helpdesk-Mitarbeiter die Kontrolle über den Computer des Endbenutzers übernehmen und die erforderlichen Dart-Tools Remote ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-105">After the end user provides the administrator or help desk worker with certain information, the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="1b3d1-106">Wenn Sie die Dart-Tools beim Erstellen des Wiederherstellungsabbilds deaktiviert haben, können Sie weiterhin auf alle Tools zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-106">If you disabled the DaRT tools when you created the recovery image, you still have access to all of the tools.</span></span> <span data-ttu-id="1b3d1-107">Alle Tools, mit Ausnahme der Remote Verbindung, stehen Endbenutzern nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-107">All of the tools, except Remote Connection, are unavailable to end users.</span></span>

**<span data-ttu-id="1b3d1-108">So stellen Sie einen Remotecomputer mithilfe des DART-Wiederherstellungs Bilds wieder her</span><span class="sxs-lookup"><span data-stu-id="1b3d1-108">To recover a remote computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="1b3d1-109">Starten Sie einen Endbenutzercomputer mithilfe des DART-Wiederherstellungs Bilds.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="1b3d1-110">In der Regel verwenden Sie eine der folgenden Methoden, um in DART zu booten, um einen Remotecomputer wiederherzustellen, je nachdem, wie das DART-Wiederherstellungsabbild bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="1b3d1-111">Weitere Informationen zum Bereitstellen des DART-Wiederherstellungs Bilds finden Sie unter [Bereitstellen von DART 10](deploying-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="1b3d1-111">For more information about deploying the DaRT recovery image, see [Deploying DaRT 10](deploying-dart-10.md).</span></span>

    -   <span data-ttu-id="1b3d1-112">Starten Sie DART von einer Wiederherstellungspartition auf dem Problem Computer.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="1b3d1-113">Starten Sie DART von einer Remotepartition im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="1b3d1-114">Informationen zu den vor-und Nachteilen der einzelnen Methoden finden Sie unter [Planen des Speicherns und Bereitstellen des Wiederherstellungs Bilds von DART 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="1b3d1-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

    <span data-ttu-id="1b3d1-115">Unabhängig davon, welche Methode Sie zum Starten von DART verwenden, müssen Sie das Startgerät im BIOS für die Startoption oder die Optionen aktivieren, die Sie dem Endbenutzer zur Verfügung stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="1b3d1-116">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1b3d1-116">Note</span></span>**  
    <span data-ttu-id="1b3d1-117">Je nach Art der Festplatte, Netzwerkadapter und anderer Hardware, die in Ihrer Organisation verwendet wird, ist die Konfiguration des BIOS einzigartig.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. <span data-ttu-id="1b3d1-118">Wenn Sie gefragt werden, ob Sie Netzwerkdienste initialisieren möchten, wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="1b3d1-118">When you are asked whether you want to initialize network services, select one of the following:</span></span>

   <span data-ttu-id="1b3d1-119">**Ja** – es wird davon ausgegangen, dass ein DHCP-Server im Netzwerk vorhanden ist, und es wird versucht, eine IP-Adresse vom Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-119">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="1b3d1-120">Wenn das Netzwerk statische IP-Adressen statt DHCP verwendet, können Sie später das **TCP/IP-Konfigurations** Tool in DART verwenden, um eine statische IP-Adresse anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-120">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

   <span data-ttu-id="1b3d1-121">**Nein** – überspringen Sie den Netzwerk Initialisierungsprozess.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-121">**No** - skip the network initialization process.</span></span>

3. <span data-ttu-id="1b3d1-122">Geben Sie an, ob Sie die Laufwerkbuchstaben neu zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-122">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="1b3d1-123">Wenn Sie Windows Online ausführen, wird das System Volume in der Regel Laufwerk C zugeordnet. Wenn Sie jedoch Windows offline unter WinRE ausführen, wird das ursprüngliche System Volume möglicherweise einem anderen Laufwerk zugeordnet, was zu Verwirrung führen kann.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-123">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="1b3d1-124">Wenn Sie sich für die Neuzuordnung entscheiden, versucht Dart, die Offline Laufwerkbuchstaben den Online Laufwerkbuchstaben zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-124">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="1b3d1-125">Eine Neuzuordnung wird nur ausgeführt, wenn ein Offline Betriebssystem später im Startvorgang ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-125">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4. <span data-ttu-id="1b3d1-126">Wählen Sie im Dialogfeld **System Wiederherstellungsoptionen** ein Tastaturlayout aus.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-126">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5. <span data-ttu-id="1b3d1-127">Überprüfen Sie das angezeigte Systemstammverzeichnis, die Art des installierten Betriebssystems und die Partitionsgröße.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-127">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="1b3d1-128">Wenn Ihr Betriebssystem nicht aufgeführt ist und Sie vermuten, dass das Fehlen von Treibern eine mögliche Ursache für den Fehler ist, klicken Sie auf **Treiber laden** , um die Verdächtigen Treiber zu laden, und legen Sie dann das Installationsmedium für das Gerät ein, und wählen Sie den Treiber aus.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-128">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6. <span data-ttu-id="1b3d1-129">Wählen Sie die Installation aus, die Sie reparieren oder diagnostizieren möchten, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-129">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

   **<span data-ttu-id="1b3d1-130">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1b3d1-130">Note</span></span>**  
   <span data-ttu-id="1b3d1-131">Wenn die Windows-Wiederherstellungsumgebung (WinRE) erkennt oder vermutet, dass Windows 10 beim letzten Versuch nicht ordnungsgemäß gestartet wurde, wird die **Startreparatur** möglicherweise automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-131">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 10 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="1b3d1-132">Informationen zum Beheben dieses Problems finden Sie unter [Problembehandlung bei Dart 10](troubleshooting-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="1b3d1-132">For information about how to resolve this issue, see [Troubleshooting DaRT 10](troubleshooting-dart-10.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="1b3d1-133">Klicken Sie im Fenster **System Wiederherstellungsoptionen** auf **Microsoft-Diagnose-und Wiederherstellungs-Toolset** , um das **Toolset Diagnose und Wiederherstellung**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-133">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset**.</span></span>

8. <span data-ttu-id="1b3d1-134">Klicken Sie im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf **Remoteverbindung** , um das **Dart-Remote Verbindungs** Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-134">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="1b3d1-135">Wenn Sie aufgefordert werden, dem Helpdesk den Remotezugriff zu gewähren, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-135">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="1b3d1-136">Das Fenster Dart-Remote Verbindung wird geöffnet, und es werden eine Ticketnummer, eine IP-Adresse und Portinformationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-136">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

9. <span data-ttu-id="1b3d1-137">Öffnen Sie auf dem Helpdesk-Computer die **Dart-Remote Verbindungsanzeige**.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-137">On the help desk computer, open the **DaRT Remote Connection Viewer**.</span></span>

10. <span data-ttu-id="1b3d1-138">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Dart 10**und dann auf **Dart Remote Connection Viewer**.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-138">Click **Start**, click **All Programs**, click **Microsoft DaRT 10**, and then click **DaRT Remote Connection Viewer**.</span></span>

11. <span data-ttu-id="1b3d1-139">Geben Sie im Fenster **Dart Remote Connection** die erforderlichen Tickets, IP-Adressen und Portinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-139">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="1b3d1-140">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1b3d1-140">Note</span></span>**  
   <span data-ttu-id="1b3d1-141">Diese Informationen werden auf dem Computer des Endbenutzers erstellt und müssen vom Endbenutzer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-141">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="1b3d1-142">Es können mehrere IP-Adressen zur Auswahl stehen, je nachdem, wie viele auf dem Endbenutzercomputer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-142">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



12. <span data-ttu-id="1b3d1-143">Klicken Sie auf **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-143">Click **Connect**.</span></span>

<span data-ttu-id="1b3d1-144">Der IT-Administrator übernimmt nun die Kontrolle über den Computer des Endbenutzers und kann die Dart-Tools Remote ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-144">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="1b3d1-145">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1b3d1-145">Note</span></span>**  
<span data-ttu-id="1b3d1-146">Es wird eine Datei mit dem Namen inv32.xml und Remote Verbindungsinformationen wie Portnummer und IP-Adresse bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-146">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="1b3d1-147">Standardmäßig befindet sich die Datei in der Regel unter%windir%\\system32.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-147">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="1b3d1-148">So passen Sie den Remote Verbindungsprozess an</span><span class="sxs-lookup"><span data-stu-id="1b3d1-148">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="1b3d1-149">Sie können den Remote Verbindungsprozess anpassen, indem Sie die winpeshl.ini Datei bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-149">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="1b3d1-150">Weitere Informationen zum Bearbeiten der winpeshl.ini Datei finden Sie unter [Winpeshl.ini Dateien](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="1b3d1-150">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="1b3d1-151">Geben Sie die folgenden Befehle und Parameter an, um das Einrichten einer Remoteverbindung mit einem Endbenutzercomputer anzupassen:</span><span class="sxs-lookup"><span data-stu-id="1b3d1-151">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="1b3d1-152">Befehl</span><span class="sxs-lookup"><span data-stu-id="1b3d1-152">Command</span></span></th>
   <th align="left"><span data-ttu-id="1b3d1-153">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b3d1-153">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="1b3d1-154">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b3d1-154">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1b3d1-155">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="1b3d1-155">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1b3d1-156">-nomessage</span><span class="sxs-lookup"><span data-stu-id="1b3d1-156">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1b3d1-157">Gibt an, dass die Bestätigungsaufforderung nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-157">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="1b3d1-158">Die Remote Verbindung </strong> wird fortgesetzt, als ob der Endbenutzer &quot; &quot; auf die Bestätigungsaufforderung "Ja" reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-158">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1b3d1-159">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="1b3d1-159">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1b3d1-160">keine</span><span class="sxs-lookup"><span data-stu-id="1b3d1-160">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1b3d1-161">Verhindert, dass ein benutzerdefiniertes Skript fortgesetzt <strong> wird, bis entweder die Remote Verbindung </strong> nicht ausgeführt wird oder eine gültige Verbindung mit dem Endbenutzercomputer hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-161">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="1b3d1-162">Wichtig</span><span class="sxs-lookup"><span data-stu-id="1b3d1-162">Important</span></span></strong><br/><p><span data-ttu-id="1b3d1-163">Dieser Befehl dient keine Funktion, wenn er unabhängig voneinander angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-163">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="1b3d1-164">Sie muss in einem Skript angegeben werden, damit Sie ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-164">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="1b3d1-165">Der folgende Code ist ein Beispiel für eine winpeshl.ini-Datei, die so angepasst wird, dass das **Remote Verbindungs** Tool geöffnet wird, sobald versucht wird, in DART zu booten:</span><span class="sxs-lookup"><span data-stu-id="1b3d1-165">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

<span data-ttu-id="1b3d1-166">Wenn Dart gestartet wird, wird die Datei inv32.xml auf der RAM-Diskette in \\Windows\\System32\\ erstellt.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-166">When DaRT starts, it creates the file inv32.xml in \\Windows\\System32\\ on the RAM disk.</span></span> <span data-ttu-id="1b3d1-167">Diese Datei enthält Verbindungsinformationen: IP-Adresse, Port und Ticketnummer.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-167">This file contains connection information: IP address, port, and ticket number.</span></span> <span data-ttu-id="1b3d1-168">Sie können diese Datei auf eine Netzwerkfreigabe kopieren, um einen Helpdesk-Workflow auszulösen.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-168">You can copy this file to a network share to trigger a Help desk workflow.</span></span> <span data-ttu-id="1b3d1-169">Ein benutzerdefiniertes Programm kann beispielsweise die Netzwerkfreigabe für Verbindungsdateien überprüfen und dann ein Support Ticket erstellen oder e-Mail-Benachrichtigungen senden.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-169">For example, a custom program can check the network share for connection files, and then create a support ticket or send email notifications.</span></span>

**<span data-ttu-id="1b3d1-170">So führen Sie die Remote Verbindungsanzeige an der Eingabeaufforderung aus</span><span class="sxs-lookup"><span data-stu-id="1b3d1-170">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="1b3d1-171">Wenn Sie die **Dart-Remote Verbindungsanzeige** an der Eingabeaufforderung ausführen möchten, geben Sie den Befehl **DartRemoteViewer.exe** an, und verwenden Sie die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="1b3d1-171">To run the **DaRT Remote Connection Viewer** at the command prompt, specify the **DartRemoteViewer.exe** command and use the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="1b3d1-172">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b3d1-172">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="1b3d1-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b3d1-173">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1b3d1-174">-Ticket = &lt; <em> ticketnumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="1b3d1-174">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1b3d1-175">Wobei &lt; <em> ticketnumber </em> &gt; die Ticketnummer ist, einschließlich der Striche, die von der Remote Verbindung generiert werden.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-175">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1b3d1-176">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="1b3d1-176">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1b3d1-177">Dabei &lt; <em> </em> &gt; ist IPAddress die IP-Adresse, die von der Remote Verbindung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-177">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1b3d1-178">-Port = &lt; <em> Port</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="1b3d1-178">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1b3d1-179">Wobei &lt; <em> Port </em> &gt; der Port ist, der der angegebenen IP-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-179">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="1b3d1-180">Wenn alle drei Parameter angegeben sind und die Daten gültig sind, wird beim Starten des Programms sofort eine Verbindung versucht.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-180">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="1b3d1-181">Wenn ein Parameter ungültig ist, wird das Programm so gestartet, als ob keine Parameter angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="1b3d1-181">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="1b3d1-182">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1b3d1-182">Related topics</span></span>


[<span data-ttu-id="1b3d1-183">Vorgänge für DaRT 10</span><span class="sxs-lookup"><span data-stu-id="1b3d1-183">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="1b3d1-184">Wiederherstellen von Computern mithilfe von DaRT 10</span><span class="sxs-lookup"><span data-stu-id="1b3d1-184">Recovering Computers Using DaRT 10</span></span>](recovering-computers-using-dart-10.md)









