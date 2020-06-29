---
title: SFTTRAY-Befehlsreferenz
description: SFTTRAY-Befehlsreferenz
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806272"
---
# <span data-ttu-id="7299f-103">SFTTRAY-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="7299f-103">SFTTRAY Command Reference</span></span>


<span data-ttu-id="7299f-104">Die Microsoft Application Virtualization (app-v)-Client Fachanwendung, sfttray.exe, ist das Hauptelement der Benutzeroberfläche des App-v-Clients, mit dem Benutzer während der normalen Verwendung interagieren können.</span><span class="sxs-lookup"><span data-stu-id="7299f-104">The Microsoft Application Virtualization (App-V) Client Tray application, sfttray.exe, is the main user interface element of the App-V Client that users will interact with during normal use.</span></span> <span data-ttu-id="7299f-105">Dieses Programm steuert das Streaming und den Start aller virtuellen Anwendungen und wird aufgerufen, indem Sie mit der rechten Maustaste auf das im Infobereich angezeigte Symbol klicken, um das Menü der Clientfunktionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7299f-105">This program controls the streaming and starting of all virtual applications and is accessed by right-clicking the icon displayed in the notification area to display the menu of client functions.</span></span> <span data-ttu-id="7299f-106">Das Menü ermöglicht es dem Benutzer, Anwendungen zu laden, eine Veröffentlichungsaktualisierung zu starten, eine Anforderung abzubrechen oder den Client in den Offlinemodus zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7299f-106">The menu enables the user to load applications, start a publishing refresh, cancel a request, or change the client to offline mode.</span></span> <span data-ttu-id="7299f-107">Der Benutzer kann auch die Application Virtualization Client Tray-Anwendung und alle aktiven Anwendungen schließen, indem Sie auf **Beenden**klicken.</span><span class="sxs-lookup"><span data-stu-id="7299f-107">The user can also close the Application Virtualization Client Tray application and all active applications by clicking **Exit**.</span></span>

<span data-ttu-id="7299f-108">Standardmäßig wird das Symbol immer dann angezeigt, wenn eine virtuelle Anwendung gestartet wird, obwohl Sie dieses Verhalten mithilfe von SFTTRAY-Befehlen steuern können.</span><span class="sxs-lookup"><span data-stu-id="7299f-108">By default, the icon is displayed whenever a virtual application is started, although you can control this behavior by using SFTTRAY commands.</span></span> <span data-ttu-id="7299f-109">Die Application Virtualization Client Tray-Anwendung zeigt auch eine Statusleiste für jede gestartete Anwendung sowie Statusmeldungen zu aktiven Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="7299f-109">The Application Virtualization Client Tray application also displays a progress bar for each application that is started, as well as status messages about active applications.</span></span> <span data-ttu-id="7299f-110">Durch Klicken auf die Statusleiste wird eine Meldung angezeigt, die es Ihnen ermöglicht, das Laden oder Starten einer Anwendung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="7299f-110">Clicking the progress bar displays a message that allows you to cancel the loading or starting of an application.</span></span>

## <span data-ttu-id="7299f-111">SFTTRAY-Befehle</span><span class="sxs-lookup"><span data-stu-id="7299f-111">SFTTRAY Commands</span></span>


<span data-ttu-id="7299f-112">Die Liste der Befehle und Befehlszeilenoptionen kann angezeigt werden, indem Sie den folgenden Befehl in einem Befehlsfenster ausführen.</span><span class="sxs-lookup"><span data-stu-id="7299f-112">The list of commands and command-line switches can be displayed by running the following command from a command window.</span></span>

**<span data-ttu-id="7299f-113">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7299f-113">Note</span></span>**  
<span data-ttu-id="7299f-114">Es gibt nur eine Instanz der Application Virtualization-Client Taskleiste für jeden Benutzerkontext, wenn Sie also einen neuen SFTTRAY-Befehl starten, wird er an das Programm weitergeleitet, das bereits ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7299f-114">There is only one Application Virtualization Client Tray instance for each user context, so if you start a new SFTTRAY command, it will be passed to the program that is already running.</span></span>



`Sfttray.exe /?`

### <span data-ttu-id="7299f-115">Befehlsverwendung</span><span class="sxs-lookup"><span data-stu-id="7299f-115">Command Usage</span></span>

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### <span data-ttu-id="7299f-116">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="7299f-116">Command-Line Switches</span></span>

<span data-ttu-id="7299f-117">Die SFTTRAY-Befehlszeilenoptionen werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7299f-117">The SFTTRAY command-line switches are described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7299f-118">Schalter</span><span class="sxs-lookup"><span data-stu-id="7299f-118">Switch</span></span></th>
<th align="left"><span data-ttu-id="7299f-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7299f-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7299f-120">/Hide</span><span class="sxs-lookup"><span data-stu-id="7299f-120">/HIDE</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-121">Blendet das SFTTRAY-Symbol im Windows-Benachrichtigungsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="7299f-121">Hides the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7299f-122">/Show</span><span class="sxs-lookup"><span data-stu-id="7299f-122">/SHOW</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-123">Zeigt das SFTTRAY-Symbol im Windows-Infobereich an.</span><span class="sxs-lookup"><span data-stu-id="7299f-123">Displays the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7299f-124">/Quiet</span><span class="sxs-lookup"><span data-stu-id="7299f-124">/QUIET</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-125">Unterstützt die unbeaufsichtigte Verwendung, indem Fehler beim Anzeigen von Meldungsfeldern verhindert werden, die eine Benutzerbestätigung erfordern.</span><span class="sxs-lookup"><span data-stu-id="7299f-125">Supports unattended usage by preventing errors from displaying message boxes that require user acknowledgement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7299f-126">/EXE &lt; Alternate-exe&gt;</span><span class="sxs-lookup"><span data-stu-id="7299f-126">/EXE &lt;alternate-exe&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-127">Wird mit/Launch verwendet, um anzugeben, dass ein ausführbares Programm in der virtuellen Umgebung gestartet werden soll, wenn anstelle der im OSD angegebenen Ziel Datei eine virtuelle Anwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7299f-127">Used with /LAUNCH to specify that an executable program is to be started in the virtual environment when a virtual application is started in place of the target file specified in the OSD.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7299f-128">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7299f-128">Note</span></span></strong><br/><p><span data-ttu-id="7299f-129">Verwenden Sie beispielsweise "SFTTRAY.EXE/exe REGEDIT.EXE/Launch- &lt; app", damit &gt; Sie die Registrierung der virtuellen Umgebung untersuchen können, in der die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7299f-129">For example, use “SFTTRAY.EXE /EXE REGEDIT.EXE /LAUNCH &lt;app&gt;” to enable you to examine the registry of the virtual environment in which the application is running.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7299f-130">/Launch- &lt; App &gt; [ &lt; args &gt; ]</span><span class="sxs-lookup"><span data-stu-id="7299f-130">/LAUNCH &lt;app&gt; [&lt;args&gt;]</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-131">Startet eine virtuelle Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7299f-131">Starts a virtual application.</span></span> <span data-ttu-id="7299f-132">Geben Sie den Namen und die Version einer Anwendung oder den Pfad zu einer OSD-Datei an.</span><span class="sxs-lookup"><span data-stu-id="7299f-132">Specify the name and version of an application or the path to an OSD file.</span></span> <span data-ttu-id="7299f-133">Optional können Befehlszeilenargumente an die virtuelle Anwendung übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="7299f-133">Optionally, command-line arguments can be passed to the virtual application.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7299f-134">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7299f-134">Note</span></span></strong><br/><p><span data-ttu-id="7299f-135">Verwenden Sie den Befehl "SFTMIME.EXE/Query obj: App/Short", um eine Liste der Namen und Versionen der verfügbaren virtuellen Anwendungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7299f-135">Use the command “SFTMIME.EXE /QUERY OBJ:APP /SHORT” to obtain a list of the names and versions of available virtual applications.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7299f-136">/Load</span><span class="sxs-lookup"><span data-stu-id="7299f-136">/LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-137">Lädt oder importiert eine virtuelle Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7299f-137">Loads or imports a virtual application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7299f-138">/LOADALL</span><span class="sxs-lookup"><span data-stu-id="7299f-138">/LOADALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-139">Lädt alle Anwendungen in den Cache.</span><span class="sxs-lookup"><span data-stu-id="7299f-139">Loads all applications into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7299f-140">/REFRESHALL</span><span class="sxs-lookup"><span data-stu-id="7299f-140">/REFRESHALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-141">Startet eine Veröffentlichungsaktualisierung für alle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="7299f-141">Starts a publishing refresh for all applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7299f-142">&lt;eindeutige/LAUNCHRESULT-ID&gt;</span><span class="sxs-lookup"><span data-stu-id="7299f-142">/LAUNCHRESULT &lt;UNIQUE ID&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-143">Gibt den Startcode für den Start des Prozesses zurück, der sfttray.exe mithilfe eines globalen Ereignisses und einer Speicher zugeordneten Datei startet, die auf dem angegebenen Stammnamen für die eindeutige ID basieren. ¹</span><span class="sxs-lookup"><span data-stu-id="7299f-143">Returns the launch result code to the process that launches sfttray.exe by using a global event and a memory mapped file that are based on the specified root name for the UNIQUE ID.¹</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7299f-144">/SFTFILE &lt; SFT&gt;</span><span class="sxs-lookup"><span data-stu-id="7299f-144">/SFTFILE &lt;sft&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-145">Optionaler Schalter, der mit/Load verwendet wird, um den Pfad zur SFT-Datei der Anwendung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7299f-145">Optional switch used with /LOAD to specify the path to the application’s SFT file.</span></span> <span data-ttu-id="7299f-146">Wenn angegeben, wird die Anwendung importiert und nicht geladen.</span><span class="sxs-lookup"><span data-stu-id="7299f-146">If specified, the application is imported rather than loaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7299f-147">/EXIT</span><span class="sxs-lookup"><span data-stu-id="7299f-147">/EXIT</span></span></p></td>
<td align="left"><p><span data-ttu-id="7299f-148">Schließt das SFTTRAY-Programm und alle aktiven virtuellen Anwendungen und entfernt das Symbol aus dem Windows-Benachrichtigungsbereich.</span><span class="sxs-lookup"><span data-stu-id="7299f-148">Closes the SFTTRAY program and all active virtual applications and removes the icon from the Windows notification area.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="7299f-149">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7299f-149">Note</span></span>**  
<span data-ttu-id="7299f-150">¹ der */LAUNCHRESULT* -Befehlszeilenparameter bietet eine Möglichkeit für den Prozess, mit dem sfttray.exe gestartet wird, um den Stammnamen für ein globales Ereignis und eine Speicher zugeordnete Datei anzugeben, die verwendet wird, um den Start Ergebniscode an den Prozess zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="7299f-150">¹ The */LAUNCHRESULT* command line parameter provides a means for the process that launches sfttray.exe to specify the root name for a global event and a memory mapped file that are used to return the launch result code to the process.</span></span> <span data-ttu-id="7299f-151">Der Name des eindeutigen Bezeichners sollte mit "SFT-" beginnen, um zu verhindern, dass der Ereignisname virtualisiert wird, wenn der Startvorgang innerhalb einer virtuellen Umgebung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7299f-151">The unique identifier name should start with “SFT-” to prevent the event name from getting virtualized when the launching process is invoked within a virtual environment.</span></span> <span data-ttu-id="7299f-152">Der Speicher zugeordnete Bereich ist 64 Bits groß.</span><span class="sxs-lookup"><span data-stu-id="7299f-152">The memory mapped region will be 64 bits in size.</span></span>

<span data-ttu-id="7299f-153">Um diesen Parameter zu verwenden, erstellt der Startvorgang ein Ereignis mit dem Namen " &lt; eindeutige ID &gt; -Ergebnis \ _Event", eine Speicher zugeordnete Datei mit dem Namen " &lt; eindeutige ID &gt; -Ergebnis \ _Value" und optional ein Ereignis mit dem Namen " &lt; Unique ID &gt; -Shutdown \ _Event", und der Startvorgang startet sfttray.exe und wartet darauf, dass das Ereignis signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7299f-153">To use this parameter, the launching process creates an event with the name “&lt;UNIQUE ID&gt;-result\_event”, a memory mapped file with the name “&lt;UNIQUE ID&gt;-result\_value”, and optionally an event with the name “&lt;UNIQUE ID&gt;-shutdown\_event”, and then the launching process launches sfttray.exe and waits on the event to be signaled.</span></span> <span data-ttu-id="7299f-154">Nachdem das Ereignis " &lt; eindeutige ID &gt; -Ergebnis \ _Event" signalisiert wurde, ruft der Startprozess den 64-Bit-Rückgabecode aus dem zugeordneten Speicherbereich ab.</span><span class="sxs-lookup"><span data-stu-id="7299f-154">After the event “&lt;UNIQUE ID&gt;-result\_event” is signaled, the launching process retrieves the 64-bit return code from the memory mapped region.</span></span>

<span data-ttu-id="7299f-155">Wenn das optionale Ereignis " &lt; eindeutige ID &gt; -Shutdown \ _Event" vorhanden ist, wenn die virtuelle Anwendung beendet wird, wird das Ereignis sfttray.exe geöffnet und signalisiert.</span><span class="sxs-lookup"><span data-stu-id="7299f-155">If the optional event “&lt;UNIQUE ID&gt;-shutdown\_event” exists when the virtual application exits, sfttray.exe opens and signals the event.</span></span> <span data-ttu-id="7299f-156">Der Startprozess wartet auf dieses Shutdown-Ereignis, wenn es ermitteln muss, wann die virtuelle Anwendung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7299f-156">The launching process waits on this shutdown event if it needs to determine when the virtual application exits.</span></span>











