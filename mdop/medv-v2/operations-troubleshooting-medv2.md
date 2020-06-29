---
title: Problembehandlung bei Vorgängen
description: Problembehandlung bei Vorgängen
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804454"
---
# <span data-ttu-id="350cc-103">Problembehandlung bei Vorgängen</span><span class="sxs-lookup"><span data-stu-id="350cc-103">Operations Troubleshooting</span></span>


<span data-ttu-id="350cc-104">Dieses Thema enthält Informationen, die Sie bei der Behandlung allgemeiner operativer Probleme in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 verwenden können.</span><span class="sxs-lookup"><span data-stu-id="350cc-104">This topic includes information that you can use to help troubleshoot general operational issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="350cc-105">Behandeln von Problemen bei MED-V-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="350cc-105">Troubleshooting Issues in MED-V Operations</span></span>


<span data-ttu-id="350cc-106">Im folgenden finden Sie einige Probleme, die Endbenutzer beim Ausführen von MED-V und Lösungen zur Behebung dieser Probleme auftreten können:</span><span class="sxs-lookup"><span data-stu-id="350cc-106">The following are some issues end users might encounter when they run MED-V and solutions to help troubleshoot these issues:</span></span>

<span data-ttu-id="350cc-107">Die **Dokumentations Umleitung schlägt fehl**.</span><span class="sxs-lookup"><span data-stu-id="350cc-107">**Documentation Redirection Fails**.</span></span> <span data-ttu-id="350cc-108">Dieses Problem tritt in der Regel auf, wenn der Ordner "eigene Dateien" des Endbenutzers auf einen Netzwerkspeicherort verweist.</span><span class="sxs-lookup"><span data-stu-id="350cc-108">This issue typically occurs when an end user’s My Documents folder points to a network location.</span></span> <span data-ttu-id="350cc-109">Das Erstellen einer Freigabe aus einem anderen freigegebenen Ordner wird von Windows nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="350cc-109">Windows does not support creating a share from another shared folder.</span></span> <span data-ttu-id="350cc-110">Wenn ein Laufwerk oder ein Ordner an den Gast umgeleitet wird, erstellt RDP\\Windows Virtual PC eine Freigabe für diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="350cc-110">When a drive or folder is redirected to the guest, RDP\\Windows Virtual PC creates a share for that folder.</span></span> <span data-ttu-id="350cc-111">Wenn der Ordner "eigene Dateien" auf dem Host bereits auf eine Freigabe zeigt, kann RDP\\Windows Virtual PC daher keine Freigabe einer Freigabe erstellen.</span><span class="sxs-lookup"><span data-stu-id="350cc-111">Therefore, if the My Documents folder on the host is already pointing to a share, RDP\\Windows Virtual PC cannot create a share of a share.</span></span>

<span data-ttu-id="350cc-112">Eine weitere mögliche Ursache für dieses Problem besteht darin, dass die Anmeldeinformationen, die zum Herstellen einer Verbindung mit der Netzwerkressource erforderlich sind, möglicherweise von den Domänenanmeldeinformationen des Benutzers abweichen.</span><span class="sxs-lookup"><span data-stu-id="350cc-112">Another possible cause of this issue is that the credentials that are required to connect to the network resource might differ from the user’s domain credentials.</span></span> <span data-ttu-id="350cc-113">Möglicherweise erkennt MED-V, dass Dokumente auf dem Host umgeleitet werden, senden Sie diese Informationen an den Gast, und versuchen Sie dann, die Netzwerkressource erneut zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="350cc-113">MED-V might be detecting that documents are redirected on the host, send that information to the guest, and then try to reconnect the network resource.</span></span> <span data-ttu-id="350cc-114">Wenn sich die Anmeldeinformationen des Benutzers nicht authentifizieren, versucht MED-V möglicherweise nicht mehr, sich zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="350cc-114">If the user’s credentials do not authenticate, MED-V might stop trying to authenticate.</span></span>

**<span data-ttu-id="350cc-115">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-115">Solution</span></span>**

<span data-ttu-id="350cc-116">Führen Sie eine der folgenden Aktionen aus, um dieses Problem zu beheben:</span><span class="sxs-lookup"><span data-stu-id="350cc-116">Try one of the following to resolve this issue:</span></span>

-   <span data-ttu-id="350cc-117">Setzen Sie das Stammverzeichnis des Benutzers in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="350cc-117">Set the user’s root directory inside Active Directory.</span></span> <span data-ttu-id="350cc-118">Der Gast und der Host sollten dann eine Verbindung mit der gleichen Netzwerkressource herstellen.</span><span class="sxs-lookup"><span data-stu-id="350cc-118">The guest and host should then connect to the same network resource.</span></span>

-   <span data-ttu-id="350cc-119">Anstatt den Ordner "eigene Dateien" an einen UNC-Pfad umzuleiten, ordnen Sie ihn einem Laufwerksbuchstaben zu (auf dem Host ordnen Sie ein Laufwerk zu, das auf die Netzwerkressource verweist).</span><span class="sxs-lookup"><span data-stu-id="350cc-119">Instead of redirecting the My Documents folder to a UNC path, map it to a drive letter (on the host, map a drive that points to the network resource).</span></span> <span data-ttu-id="350cc-120">Der Ordner "eigene Dateien" kann dann so festgesetzt werden, dass der Laufwerkbuchstabe anstelle des UNC-Pfads verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="350cc-120">The My Documents folder can then be set to use the drive letter instead of the UNC path.</span></span> <span data-ttu-id="350cc-121">Der Gast wird dann wie erwartet auf das gleiche zugeordnete Laufwerk umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="350cc-121">The guest will then redirect to that same mapped drive as expected.</span></span>

-   <span data-ttu-id="350cc-122">Erstellen Sie ein Startskript im Gast, das den Ordner "eigene Dateien" an die Netzwerkressource umleitet und bei Bedarf zusätzliche Anmeldeinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="350cc-122">Create a startup script in the guest that redirects the My Documents folder to the network resource and provides additional credentials as needed.</span></span>

<span data-ttu-id="350cc-123">Die **URL-Umleitung schlägt fehl**.</span><span class="sxs-lookup"><span data-stu-id="350cc-123">**URL Redirection Fails**.</span></span> <span data-ttu-id="350cc-124">Eine URL, die Sie für die Umleitung vom Host zum Gast angegeben haben, wird nicht wie beabsichtigt umgeleitet oder gibt eine Fehlermeldung zurück, die angibt, dass die Website nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="350cc-124">A URL that you have specified for redirection from the host to the guest is not redirecting as intended or is returning an error message that indicates that the website does not exist.</span></span>

**<span data-ttu-id="350cc-125">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-125">Solution</span></span>**

<span data-ttu-id="350cc-126">Dieser Fehler kann auftreten, wenn in den URL-Umleitungsinformationen ein Rechtschreibfehler oder eine falsche Verwendung von Zeichen wie Sternchen (\ \*) vorliegt.</span><span class="sxs-lookup"><span data-stu-id="350cc-126">This error can occur when there is a misspelling or incorrect use of characters, such as asterisk (\*), in the URL redirection information.</span></span> <span data-ttu-id="350cc-127">Überprüfen Sie den Registrierungswert auf URL-Umleitung, und korrigieren Sie alle Fehler.</span><span class="sxs-lookup"><span data-stu-id="350cc-127">Check the registry value for URL redirection and correct any mistakes.</span></span>

<span data-ttu-id="350cc-128">Der Registrierungsschlüssel wird aufgerufen `RedirectUrls` und befindet sich normalerweise unter:</span><span class="sxs-lookup"><span data-stu-id="350cc-128">The registry key is called `RedirectUrls` and is typically located at:</span></span>

<span data-ttu-id="350cc-129">Computer\\HKEY\ _LOCAL \ _MACHINE \\software\\microsoft\\medv\\v2\\userexperience</span><span class="sxs-lookup"><span data-stu-id="350cc-129">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="350cc-130">**Symbol in der Taskleiste irreführend**.</span><span class="sxs-lookup"><span data-stu-id="350cc-130">**Icon in Taskbar Misleading**.</span></span> <span data-ttu-id="350cc-131">Standardmäßig ist das Symbol, das auf der Taskleiste eines Endbenutzers für veröffentlichte Anwendungen und umgeleitete URLs angezeigt wird, das Symbol für Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="350cc-131">By default, the icon that appears in an end user’s taskbar for published applications and redirected URLs is the icon for Windows Virtual PC.</span></span> <span data-ttu-id="350cc-132">Wenn ein Endbenutzer dieses Standardverhalten nicht kennt, kann er verwirrt werden, wenn Sie die Taskleiste suchen, um die Anwendung zu finden.</span><span class="sxs-lookup"><span data-stu-id="350cc-132">If an end user is not aware of this default behavior, they can become confused when looking at the taskbar to locate their application.</span></span>

**<span data-ttu-id="350cc-133">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-133">Solution</span></span>**

<span data-ttu-id="350cc-134">Die einzige Möglichkeit, dieses Standardverhalten zu vermeiden, besteht darin, die Benutzereinstellungen für die Taskleisteneigenschaften wie folgt zu ändern:</span><span class="sxs-lookup"><span data-stu-id="350cc-134">The only way to avoid this default behavior is to change the user settings for the taskbar properties as follows:</span></span>

1.  <span data-ttu-id="350cc-135">Klicken Sie mit der rechten Maustaste auf die Taskleiste, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="350cc-135">Right-click the taskbar and then click **Properties**.</span></span>

2.  <span data-ttu-id="350cc-136">Klicken Sie im Dialogfeld **Eigenschaften von Taskleiste und Startmenü** auf die Registerkarte **Taskleiste** .</span><span class="sxs-lookup"><span data-stu-id="350cc-136">In the **Taskbar and Start Menu Properties** dialog box, click the **Taskbar** tab.</span></span>

3.  <span data-ttu-id="350cc-137">Wählen Sie in der Dropdownleiste für das Feld **Schaltflächen für die Taskleiste** die Option **nie kombinieren**aus.</span><span class="sxs-lookup"><span data-stu-id="350cc-137">In the drop-down bar for the **Taskbar buttons** box, select **Never combine**.</span></span>

4.  <span data-ttu-id="350cc-138">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="350cc-138">Click **OK**.</span></span>

<span data-ttu-id="350cc-139">Die erwarteten Symbole für veröffentlichte Anwendungen und umgeleitete URLs werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="350cc-139">The expected icons for published applications and redirected URLs are displayed.</span></span>

<span data-ttu-id="350cc-140">**Warnung wird ausgegeben, wenn der zweite Benutzer versucht, sich anzumelden oder wenn der virtuelle Computer verwendet wird**.</span><span class="sxs-lookup"><span data-stu-id="350cc-140">**Warning Issued if Second User Attempts Log on or if Virtual Machine is in Use**.</span></span> <span data-ttu-id="350cc-141">Eine Warnmeldung wird ausgegeben, wenn sich ein zweiter Benutzer bei einem Med-v-Arbeitsbereich anmeldet, während ein erster Benutzer noch Med-v ausführt.</span><span class="sxs-lookup"><span data-stu-id="350cc-141">A warning message is issued when a second user logs on to a MED-V workspace while a first user is still running MED-V.</span></span> <span data-ttu-id="350cc-142">Die Warnung wird auch ausgegeben, wenn MED-V gestartet wird, während der virtuelle Computer verwendet wird, beispielsweise, wenn der virtuelle Computer über den Windows Virtual PC im **Startmenü** gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="350cc-142">The warning is also issued if MED-V is started while the virtual machine is being used, for example, if the virtual machine was started through Windows Virtual PC on the **Start** menu.</span></span> <span data-ttu-id="350cc-143">Wenn der Endbenutzer die Warnmeldung annimmt, wird MED-V heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="350cc-143">When the end user accepts the warning message, MED-V shuts down.</span></span>

**<span data-ttu-id="350cc-144">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-144">Solution</span></span>**

<span data-ttu-id="350cc-145">Ein Endbenutzer muss sicherstellen, dass alle anderen Benutzer von MED-V abgemeldet werden, bevor Sie versuchen, sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="350cc-145">An end user must verify that all other users are logged off MED-V before they try to log on.</span></span> <span data-ttu-id="350cc-146">Dadurch wird sichergestellt, dass keine andere Instanz von MED-V ausgeführt wird und dass Windows Virtual PC nicht die Kontrolle über den virtuellen Computer hat.</span><span class="sxs-lookup"><span data-stu-id="350cc-146">This ensures that no other instance of MED-V is running and that Windows Virtual PC is not in control of the virtual machine.</span></span>

<span data-ttu-id="350cc-147">**Akustische Signale während der erstmaligen Einrichtung**.</span><span class="sxs-lookup"><span data-stu-id="350cc-147">**Beeps Heard During First Time Setup**.</span></span> <span data-ttu-id="350cc-148">Gelegentlich werden Pieptöne abgehört, während MED-V beim erstmaligen Einrichten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="350cc-148">Occasionally, beeps are heard while MED-V is running first time setup.</span></span> <span data-ttu-id="350cc-149">Dies kann für einen Endbenutzer verwirrend sein.</span><span class="sxs-lookup"><span data-stu-id="350cc-149">This can be confusing to an end user.</span></span> <span data-ttu-id="350cc-150">Die Pieptöne stammen vom virtuellen Computer, wenn bestimmte Aktionen wie das Herunterfahren ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="350cc-150">The beeps are originating from the virtual machine when it performs certain actions, such as shutting down.</span></span>

**<span data-ttu-id="350cc-151">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-151">Solution</span></span>**

<span data-ttu-id="350cc-152">Sie können den Signalton Dienst beenden, indem Sie am Anfang jeder Startsequenz für den virtuellen Computer den Befehl "net stop Beep" angeben.</span><span class="sxs-lookup"><span data-stu-id="350cc-152">You can stop the beep service by specifying the "net stop beep" command at the beginning of each virtual machine start sequence.</span></span> <span data-ttu-id="350cc-153">Sie können den Signalton Dienst auch deaktivieren, indem Sie den Befehl "SC config Beep Start = disabled" angeben.</span><span class="sxs-lookup"><span data-stu-id="350cc-153">Or you can disable the beep service by specifying the “sc config beep start= disabled" command.</span></span> <span data-ttu-id="350cc-154">Sie können diese Befehle entweder vor dem Versiegeln des Bilds oder als Teil von Sysprep angeben.</span><span class="sxs-lookup"><span data-stu-id="350cc-154">You can specify these commands either before you seal the image or as part of Sysprep.</span></span>

<span data-ttu-id="350cc-155">**Mehrere Netzwerkverbindungen, die für MED-V-Arbeitsbereiche im Überbrückungsmodus erstellt wurden**.</span><span class="sxs-lookup"><span data-stu-id="350cc-155">**Multiple Network Connections Created for MED-V Workspaces in BRIDGED Mode**.</span></span> <span data-ttu-id="350cc-156">Wenn die erstmalige Einrichtung einen MED-V-Arbeitsbereich erstellt, der für den NAT-Modus konfiguriert ist, wird nur eine einzige Netzwerkverbindung in Windows Virtual PC erstellt.</span><span class="sxs-lookup"><span data-stu-id="350cc-156">If first time setup is creating a MED-V workspace that is configured for NAT mode, it only creates a single network connection in Windows Virtual PC.</span></span> <span data-ttu-id="350cc-157">Wenn allerdings das erstmalige Setup einen Med-v-Arbeitsbereich erstellt, der für den Überbrückungsmodus konfiguriert ist, wird für jeden auf dem Computer installierten Netzwerkadapter eine separate Netzwerkverbindung erstellt, weil Med-v nicht ermitteln kann, welcher Netzwerkadapter aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="350cc-157">However, if first time setup is creating a MED-V workspace that is configured for BRIDGED mode, it creates a separate network connection for each network adapter that is installed in the computer, because MED-V cannot determine which network adapter is active.</span></span> <span data-ttu-id="350cc-158">Dadurch wird auch sichergestellt, dass Roaming-Benutzer immer über einen Netzwerkadapter für verdrahtete und drahtlose Verbindungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="350cc-158">This also ensures that roaming users always have a network adapter available for wired and wireless connections.</span></span>

**<span data-ttu-id="350cc-159">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-159">Solution</span></span>**

<span data-ttu-id="350cc-160">Keine</span><span class="sxs-lookup"><span data-stu-id="350cc-160">None.</span></span>

<span data-ttu-id="350cc-161">**Die MED-V-Anwendung reagiert beim Schließen zu lange nicht**mehr.</span><span class="sxs-lookup"><span data-stu-id="350cc-161">**MED-V Application is Unresponsive for Too Long when Closing**.</span></span> <span data-ttu-id="350cc-162">In einigen Fällen reagiert eine MED-V-Anwendung nicht mehr, wenn Sie versucht, Sie zu schließen.</span><span class="sxs-lookup"><span data-stu-id="350cc-162">In some instances, a MED-V application stops responding when it is trying to close.</span></span>

**<span data-ttu-id="350cc-163">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-163">Solution</span></span>**

<span data-ttu-id="350cc-164">Sie können die Zeitdauer angeben, die MED-V wartet, um nicht reagierende Anwendungen zu schließen, indem Sie den WaitToKillAppTimeout-Registrierungsschlüssel auf dem virtuellen Gastcomputer festlegen.</span><span class="sxs-lookup"><span data-stu-id="350cc-164">You can specify the length of time that MED-V waits to close unresponsive applications by setting the WaitToKillAppTimeout registry key in the guest virtual machine.</span></span> <span data-ttu-id="350cc-165">Weitere Informationen finden Sie unter so wird es [gemacht: verbessern der Zeit für das Herunterfahren, damit Prozesse in Windows XP ordnungsgemäß beendet werden können](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .</span><span class="sxs-lookup"><span data-stu-id="350cc-165">For more information, see [How To Increase Shutdown Time So That Processes Can Quit Properly in Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) (https://go.microsoft.com/fwlink/?LinkId=206819).</span></span>

<span data-ttu-id="350cc-166">**Durch Umbenennen einer veröffentlichten Anwendungsverknüpfung auf dem virtuellen Gastcomputer wird der veröffentlichte Name im Host nicht geändert**.</span><span class="sxs-lookup"><span data-stu-id="350cc-166">**Renaming a Published Application Shortcut in the Guest Virtual Machine does not Change the Published Name in the Host**.</span></span> <span data-ttu-id="350cc-167">Wenn Sie eine Anwendung veröffentlichen, indem Sie eine Verknüpfung erstellen und dann die Verknüpfung auf der virtuellen Gastmaschine umbenennen, verbleibt der ursprüngliche Anwendungsname **im Startmenü des Hosts.**</span><span class="sxs-lookup"><span data-stu-id="350cc-167">When you publish an application by creating a shortcut and then rename the shortcut in the guest virtual machine, the original application name remains in the host **Start** menu.</span></span> <span data-ttu-id="350cc-168">Das Programm wird weiterhin erwartungsgemäß ausgeführt, jedoch behält das Programm immer den ursprünglichen Namen bei.</span><span class="sxs-lookup"><span data-stu-id="350cc-168">The program continues to run as expected, however the program will always retain the original name.</span></span>

**<span data-ttu-id="350cc-169">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-169">Solution</span></span>**

<span data-ttu-id="350cc-170">Keine</span><span class="sxs-lookup"><span data-stu-id="350cc-170">None.</span></span> <span data-ttu-id="350cc-171">Dies ist ein bekanntes Verhalten von Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="350cc-171">This is a known behavior of Windows Virtual PC.</span></span>

<span data-ttu-id="350cc-172">Wenn Sie **eine Verknüpfung auf dem virtuellen Gastcomputer verschieben, wird der Speicherort im Startmenü des Host Computers nicht aktualisiert**.</span><span class="sxs-lookup"><span data-stu-id="350cc-172">**Moving a Shortcut in the Guest Virtual Machine does not Update the Location on the Host Computer Start Menu**.</span></span> <span data-ttu-id="350cc-173">MED-V-Anwendungsverknüpfungen, die im **Start** Menü des Hostcomputers veröffentlicht werden, werden in der Registrierung katalogisiert.</span><span class="sxs-lookup"><span data-stu-id="350cc-173">MED-V application shortcuts that are published to the host computer **Start** menu are cataloged in the registry.</span></span> <span data-ttu-id="350cc-174">Wenn Sie eine Anwendungsverknüpfung in einen Unterordner verschieben, wird die Registrierung nicht aktualisiert, um die Änderung wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="350cc-174">If you move an application shortcut into a subfolder, the registry is not updated to reflect the change.</span></span>

**<span data-ttu-id="350cc-175">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-175">Solution</span></span>**

<span data-ttu-id="350cc-176">Führen Sie die folgenden Schritte aus, um den Speicherort einer MED-V-Anwendungsverknüpfung zu ändern:</span><span class="sxs-lookup"><span data-stu-id="350cc-176">Follow these steps to change the location of a MED-V application shortcut:</span></span>

1.  <span data-ttu-id="350cc-177">Wenn Med-v ausgeführt wird, öffnen Sie Windows-Explorer auf dem virtuellen Med-v Guest-Computer.</span><span class="sxs-lookup"><span data-stu-id="350cc-177">When MED-V is running, open up Windows Explorer on the MED-V guest virtual machine.</span></span>

2.  <span data-ttu-id="350cc-178">Navigieren Sie zum Verzeichnis "%ALLUSERSPROFILE%\\Start Menu\\Programs".</span><span class="sxs-lookup"><span data-stu-id="350cc-178">Browse to the "%ALLUSERSPROFILE%\\Start Menu\\Programs" directory.</span></span>

3.  <span data-ttu-id="350cc-179">Verschieben Sie die Anwendungsverknüpfungen aus den Ordnern "Startmenü" oder "Programme".</span><span class="sxs-lookup"><span data-stu-id="350cc-179">Move the application shortcuts out of the startmenu or programs folders.</span></span>

4.  <span data-ttu-id="350cc-180">Überprüfen Sie nach ungefähr 30 Sekunden, ob die Verknüpfungen aus dem **Startmenü** des Hostcomputers entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="350cc-180">After about 30 seconds, validate that the shortcuts are removed from the host computer **Start** menu.</span></span>

5.  <span data-ttu-id="350cc-181">Verschieben Sie die Anwendungsverknüpfungen wieder in die neuen Programmordner unter dem Verzeichnis Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="350cc-181">Move the application shortcuts back in to the new program folders under the Start Menu\\Programs directory.</span></span>

6.  <span data-ttu-id="350cc-182">Überprüfen Sie nach ungefähr 30 Sekunden, ob die Verknüpfungen im **Startmenü** des Hostcomputers aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="350cc-182">After about 30 seconds, validate that the shortcuts are updated in the host computer **Start** Menu.</span></span>

<span data-ttu-id="350cc-183">**Veröffentlichte Anwendungen können ein Timeout aufweisen, nachdem Sie im Leerlauf sitzen**.</span><span class="sxs-lookup"><span data-stu-id="350cc-183">**Published Applications can Time Out after Sitting Idle**.</span></span> <span data-ttu-id="350cc-184">In einigen Fällen können veröffentlichte Anwendungen ausfallen, wenn Sie sich längere Zeit im Leerlauf befinden.</span><span class="sxs-lookup"><span data-stu-id="350cc-184">In some cases, published applications will time out if they have sat idle for some time.</span></span> <span data-ttu-id="350cc-185">Diese Situation tritt nur auf, wenn IPSec aktiviert ist und der MED-V-Arbeitsbereich für den NAT-Modus konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="350cc-185">This situation only occurs if IPsec is enabled and the MED-V workspace is configured for NAT mode.</span></span> <span data-ttu-id="350cc-186">Diese Situation tritt nicht auf, wenn Sie im Überbrückungsmodus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="350cc-186">This situation does not occur if running in BRIDGED mode.</span></span>

**<span data-ttu-id="350cc-187">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-187">Solution</span></span>**

<span data-ttu-id="350cc-188">Deaktivieren Sie IPSec, wenn Sie den MED-V-Arbeitsbereich im NAT-Modus ausführen.</span><span class="sxs-lookup"><span data-stu-id="350cc-188">Disable IPsec when you are running the MED-V workspace in NAT mode.</span></span>

<span data-ttu-id="350cc-189">**Das Anheften einer veröffentlichten Anwendung an die Taskleiste umgeht MED-V**.</span><span class="sxs-lookup"><span data-stu-id="350cc-189">**Pinning a Published Application to the Taskbar Bypasses MED-V**.</span></span> <span data-ttu-id="350cc-190">Wenn ein Endbenutzer eine veröffentlichte Anwendung an die Taskleiste anstiftet und dann die Anwendung schließt, wird MED-V beim nächsten Öffnen der Anwendung über das Taskleistensymbol umgangen.</span><span class="sxs-lookup"><span data-stu-id="350cc-190">If an end user pins a published application to the taskbar and then closes the application, MED-V is bypassed the next time that the application is opened from the taskbar icon.</span></span> <span data-ttu-id="350cc-191">Stattdessen wird die Anwendung direkt in einem VMSAL-Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="350cc-191">Instead, the application opens directly in a VMSAL window.</span></span>

**<span data-ttu-id="350cc-192">Lösung</span><span class="sxs-lookup"><span data-stu-id="350cc-192">Solution</span></span>**

<span data-ttu-id="350cc-193">Anheften Sie die in MED-V veröffentlichten Anwendungen nicht an die Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="350cc-193">Do not pin the applications published in MED-V to the taskbar.</span></span>

## <span data-ttu-id="350cc-194">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="350cc-194">Related topics</span></span>


[<span data-ttu-id="350cc-195">Bewährte Sicherheitsmethoden für MED-V-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="350cc-195">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)

[<span data-ttu-id="350cc-196">Problembehandlung bei der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="350cc-196">Deployment Troubleshooting</span></span>](deployment-troubleshooting.md)

 

 





