---
title: So stellen Sie Remotecomputer mithilfe des DaRT-Wiederherstellungsabbilds wieder her
description: So stellen Sie Remotecomputer mithilfe des DaRT-Wiederherstellungsabbilds wieder her
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809568"
---
# <span data-ttu-id="a8685-103">So stellen Sie Remotecomputer mithilfe des DaRT-Wiederherstellungsabbilds wieder her</span><span class="sxs-lookup"><span data-stu-id="a8685-103">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="a8685-104">Mit dem Feature Remote Verbindung in Microsoft Diagnostics and Recovery Toolset (Dart) 7 können IT-Administratoren die Dart-Tools Remote auf einem Endbenutzercomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8685-104">The Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="a8685-105">Nachdem der Endbenutzer bestimmte Informationen bereitgestellt hat (oder von einem Helpdesk-Mitarbeiter, der auf dem Endbenutzercomputer arbeitet), kann der IT-Administrator oder Helpdesk-Agent den Computer des Endbenutzers Steuern und die erforderlichen Dart-Tools Remote ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8685-105">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

**<span data-ttu-id="a8685-106">Wichtig</span><span class="sxs-lookup"><span data-stu-id="a8685-106">Important</span></span>**  
<span data-ttu-id="a8685-107">Die beiden Computer, die eine Remoteverbindung herstellen, müssen Teil desselben Netzwerks sein.</span><span class="sxs-lookup"><span data-stu-id="a8685-107">The two computers establishing a remote connection must be part of the same network.</span></span>



**<span data-ttu-id="a8685-108">So stellen Sie einen Remotecomputer mithilfe von DART wieder her</span><span class="sxs-lookup"><span data-stu-id="a8685-108">To recover a remote computer by using DaRT</span></span>**

1.  <span data-ttu-id="a8685-109">Starten Sie einen Endbenutzercomputer mithilfe des DART-Wiederherstellungs Bilds.</span><span class="sxs-lookup"><span data-stu-id="a8685-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="a8685-110">In der Regel verwenden Sie eine der folgenden Methoden, um in DART zu booten, um einen Remotecomputer wiederherzustellen, je nachdem, wie das DART-Wiederherstellungsabbild bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a8685-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="a8685-111">Weitere Informationen zum Bereitstellen des DART-Wiederherstellungs Bilds finden Sie unter [Bereitstellen des DART 7,0-Wiederherstellungs](deploying-the-dart-70-recovery-image-dart-7.md)Abbilds.</span><span class="sxs-lookup"><span data-stu-id="a8685-111">For more information about deploying the DaRT recovery image, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

    -   <span data-ttu-id="a8685-112">Starten Sie DART von einer Wiederherstellungspartition auf dem Problem Computer.</span><span class="sxs-lookup"><span data-stu-id="a8685-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="a8685-113">Starten Sie DART von einer Remotepartition im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a8685-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="a8685-114">Informationen zu den vor-und Nachteilen der einzelnen Methoden finden Sie unter [Planen des Speicherns und Bereitstellen des DART 7,0-Wiederherstellungsabbilds](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="a8685-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

    <span data-ttu-id="a8685-115">Unabhängig davon, welche Methode Sie zum Starten von DART verwenden, müssen Sie das Startgerät im BIOS für die Startoption oder die Optionen aktivieren, die Sie dem Endbenutzer zur Verfügung stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="a8685-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="a8685-116">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="a8685-116">Note</span></span>**  
    <span data-ttu-id="a8685-117">Je nach Art der Festplatte, Netzwerkadapter und anderer Hardware, die in Ihrer Organisation verwendet wird, ist die Konfiguration des BIOS einzigartig.</span><span class="sxs-lookup"><span data-stu-id="a8685-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



2.  <span data-ttu-id="a8685-118">Wenn der Computer in das DART-Wiederherstellungsabbild gestartet wird, wird das Dialogfeld " **netstart** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8685-118">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="a8685-119">Sie werden gefragt, ob Sie Netzwerkdienste initialisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a8685-119">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="a8685-120">Wenn Sie auf **Ja**klicken, wird davon ausgegangen, dass ein DHCP-Server im Netzwerk vorhanden ist, und es wird versucht, eine IP-Adresse vom Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a8685-120">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="a8685-121">Wenn das Netzwerk statische IP-Adressen statt DHCP verwendet, können Sie später das **TCP/IP-Konfigurations** Tool in DART verwenden, um eine statische IP-Adresse anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a8685-121">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="a8685-122">Wenn Sie den Netzwerk Initialisierungsprozess überspringen möchten, klicken Sie auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="a8685-122">To skip the network initialization process, click **No**.</span></span>

3.  <span data-ttu-id="a8685-123">Nachdem Sie das Dialogfeld Netzwerk Initialisierung aufgerufen haben, werden Sie gefragt, ob Sie die Laufwerkbuchstaben neu zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="a8685-123">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="a8685-124">Wenn Sie Windows Online ausführen, wird das System Volume in der Regel Laufwerk C zugeordnet. Wenn Sie jedoch Windows offline unter WinRE ausführen, wird das ursprüngliche System Volume möglicherweise einem anderen Laufwerk zugeordnet, was zu Verwirrung führen kann.</span><span class="sxs-lookup"><span data-stu-id="a8685-124">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="a8685-125">Wenn Sie sich für die Neuzuordnung entscheiden, versucht Dart, die Offline Laufwerkbuchstaben den Online Laufwerkbuchstaben zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a8685-125">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="a8685-126">Eine Neuzuordnung wird nur ausgeführt, wenn ein Offline Betriebssystem später im Startvorgang ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a8685-126">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="a8685-127">Nach dem Dialogfeld erneute Zuordnung wird ein Dialogfeld **System Wiederherstellungsoptionen** angezeigt, in dem Sie aufgefordert werden, ein Tastaturlayout auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a8685-127">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="a8685-128">Anschließend werden das Systemstammverzeichnis, die Art des installierten Betriebssystems und die Partitionsgröße angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8685-128">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="a8685-129">Wenn Ihr Betriebssystem nicht aufgeführt ist und Sie vermuten, dass das Fehlen von Treibern eine mögliche Ursache für den Fehler ist, klicken Sie auf **Treiber laden** , um die Verdächtigen Treiber zu laden.</span><span class="sxs-lookup"><span data-stu-id="a8685-129">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="a8685-130">Sie werden aufgefordert, das Installationsmedium für das Gerät einzufügen und den Treiber auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a8685-130">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="a8685-131">Wählen Sie die Installation aus, die Sie reparieren oder diagnostizieren möchten, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a8685-131">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="a8685-132">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="a8685-132">Note</span></span>**  
    <span data-ttu-id="a8685-133">Wenn die Windows-Wiederherstellungsumgebung (WinRE) erkennt oder vermutet, dass Windows 7 beim letzten Versuch nicht ordnungsgemäß gestartet wurde, wird die **Startreparatur** möglicherweise automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="a8685-133">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="a8685-134">Informationen zu dieser Situation, einschließlich der Lösungsanleitung, finden Sie unter [Problembehandlung bei Dart 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="a8685-134">For information about this situation including how to resolve it, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. <span data-ttu-id="a8685-135">Wählen Sie im Fenster **System Wiederherstellungsoptionen** die Option **Microsoft Diagnostics and Recovery Toolset** aus, um das **Diagnose-und Wiederherstellungs-Toolset** -Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a8685-135">On the **System Recovery Options** window, select **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset** window.</span></span>

6. <span data-ttu-id="a8685-136">Klicken Sie im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf **Remoteverbindung** , um das **Dart-Remote Verbindungs** Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a8685-136">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="a8685-137">Wenn Sie aufgefordert werden, dem Helpdesk den Remotezugriff zu gewähren, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8685-137">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="a8685-138">Das Fenster Dart-Remote Verbindung wird geöffnet, und es werden eine Ticketnummer, eine IP-Adresse und Portinformationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8685-138">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

7. <span data-ttu-id="a8685-139">Öffnen Sie auf dem Helpdesk-Agent-Computer die **Dart-Remote Verbindungsanzeige**.</span><span class="sxs-lookup"><span data-stu-id="a8685-139">On the helpdesk agent computer, open the **DaRT Remote Connection Viewer**.</span></span>

   <span data-ttu-id="a8685-140">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Dart 7**, und klicken Sie dann auf **Dart Remote Connection Viewer**.</span><span class="sxs-lookup"><span data-stu-id="a8685-140">Click **Start**, click **All Programs**, click **Microsoft DaRT 7**, and then click **DaRT Remote Connection Viewer**.</span></span>

8. <span data-ttu-id="a8685-141">Geben Sie im Fenster **Dart Remote Connection** die erforderlichen Tickets, IP-Adressen und Portinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="a8685-141">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="a8685-142">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="a8685-142">Note</span></span>**  
   <span data-ttu-id="a8685-143">Diese Informationen werden auf dem Computer des Endbenutzers erstellt und müssen vom Endbenutzer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a8685-143">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="a8685-144">Es können mehrere IP-Adressen zur Auswahl stehen, je nachdem, wie viele auf dem Endbenutzercomputer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a8685-144">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



9. <span data-ttu-id="a8685-145">Klicken Sie auf **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="a8685-145">Click **Connect**.</span></span>

<span data-ttu-id="a8685-146">Der IT-Administrator übernimmt nun die Kontrolle über den Computer des Endbenutzers und kann die Dart-Tools Remote ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8685-146">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="a8685-147">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="a8685-147">Note</span></span>**  
<span data-ttu-id="a8685-148">Es wird eine Datei mit dem Namen inv32.xml und Remote Verbindungsinformationen wie Portnummer und IP-Adresse bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a8685-148">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="a8685-149">Standardmäßig befindet sich die Datei in der Regel unter%windir%\\system32.</span><span class="sxs-lookup"><span data-stu-id="a8685-149">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="a8685-150">So passen Sie den Remote Verbindungsprozess an</span><span class="sxs-lookup"><span data-stu-id="a8685-150">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="a8685-151">Sie können den Remote Verbindungsprozess anpassen, indem Sie die winpeshl.ini Datei bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a8685-151">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="a8685-152">Weitere Informationen zum Bearbeiten der winpeshl.ini Datei finden Sie unter [Winpeshl.ini Dateien](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="a8685-152">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="a8685-153">Geben Sie die folgenden Befehle und Parameter an, um das Einrichten einer Remoteverbindung mit einem Endbenutzercomputer anzupassen:</span><span class="sxs-lookup"><span data-stu-id="a8685-153">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a8685-154">Befehl</span><span class="sxs-lookup"><span data-stu-id="a8685-154">Command</span></span></th>
   <th align="left"><span data-ttu-id="a8685-155">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8685-155">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="a8685-156">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8685-156">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a8685-157">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="a8685-157">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a8685-158">-nomessage</span><span class="sxs-lookup"><span data-stu-id="a8685-158">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a8685-159">Gibt an, dass die Bestätigungsaufforderung nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a8685-159">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="a8685-160">Die Remote Verbindung </strong> wird fortgesetzt, als ob der Endbenutzer &quot; &quot; auf die Bestätigungsaufforderung "Ja" reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="a8685-160">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="a8685-161">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="a8685-161">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a8685-162">keine</span><span class="sxs-lookup"><span data-stu-id="a8685-162">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a8685-163">Verhindert, dass ein benutzerdefiniertes Skript fortgesetzt <strong> wird, bis entweder die Remote Verbindung </strong> nicht ausgeführt wird oder eine gültige Verbindung mit dem Endbenutzercomputer hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a8685-163">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a8685-164">Wichtig</span><span class="sxs-lookup"><span data-stu-id="a8685-164">Important</span></span></strong><br/><p><span data-ttu-id="a8685-165">Dieser Befehl dient keine Funktion, wenn er unabhängig voneinander angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a8685-165">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="a8685-166">Sie muss in einem Skript angegeben werden, damit Sie ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a8685-166">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="a8685-167">Der folgende Code ist ein Beispiel für eine winpeshl.ini-Datei, die so angepasst wird, dass das **Remote Verbindungs** Tool geöffnet wird, sobald versucht wird, in DART zu booten:</span><span class="sxs-lookup"><span data-stu-id="a8685-167">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

**<span data-ttu-id="a8685-168">So führen Sie die Remote Verbindungsanzeige an der Eingabeaufforderung aus</span><span class="sxs-lookup"><span data-stu-id="a8685-168">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="a8685-169">Sie können die **Dart-Remote Verbindungsanzeige** an der Eingabeaufforderung ausführen, indem Sie den Befehl **DartRemoteViewer.exe** angeben und die folgenden Parameter verwenden:</span><span class="sxs-lookup"><span data-stu-id="a8685-169">You can run the **DaRT Remote Connection Viewer** at the command prompt by specifying the **DartRemoteViewer.exe** command and by using the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a8685-170">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8685-170">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="a8685-171">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8685-171">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a8685-172">-Ticket = &lt; <em> ticketnumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="a8685-172">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8685-173">Wobei &lt; <em> ticketnumber </em> &gt; die Ticketnummer ist, einschließlich der Striche, die von der Remote Verbindung generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a8685-173">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a8685-174">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="a8685-174">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8685-175">Dabei &lt; <em> </em> &gt; ist IPAddress die IP-Adresse, die von der Remote Verbindung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="a8685-175">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a8685-176">-Port = &lt; <em> Port</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="a8685-176">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8685-177">Wobei &lt; <em> Port </em> &gt; der Port ist, der der angegebenen IP-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="a8685-177">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="a8685-178">Wenn alle drei Parameter angegeben sind und die Daten gültig sind, wird beim Starten des Programms sofort eine Verbindung versucht.</span><span class="sxs-lookup"><span data-stu-id="a8685-178">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="a8685-179">Wenn ein Parameter ungültig ist, wird das Programm so gestartet, als ob keine Parameter angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="a8685-179">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="a8685-180">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a8685-180">Related topics</span></span>


[<span data-ttu-id="a8685-181">Wiederherstellen von Computern mithilfe von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="a8685-181">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









