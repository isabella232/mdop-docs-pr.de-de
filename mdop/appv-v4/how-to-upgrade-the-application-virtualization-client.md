---
title: So aktualisieren Sie Application Virtualization Client
description: So aktualisieren Sie Application Virtualization Client
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806712"
---
# <span data-ttu-id="f3b4f-103">So aktualisieren Sie Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="f3b4f-103">How to Upgrade the Application Virtualization Client</span></span>


<span data-ttu-id="f3b4f-104">Sie können die folgenden Verfahren zum Upgrade des Application Virtualization (app-v)-Desktop Clients oder des App-v-Clients für Remote Desktop Dienste (ehemals Terminal Dienste) verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-104">You can use the following procedures to upgrade the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="f3b4f-105">Sie aktualisieren den Client, indem Sie eine neue Version über die zuvor installierte ältere Version installieren.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-105">You upgrade the client by installing a new version over the previously installed older version.</span></span> <span data-ttu-id="f3b4f-106">Wenn Sie die Clients aktualisieren, werden die Einstellungen des Benutzers für virtuelle Anwendungen automatisch von der Installationssoftware beibehalten und migriert.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-106">When you upgrade the clients, the installer software automatically preserves and migrates the user’s settings for virtual applications.</span></span> <span data-ttu-id="f3b4f-107">Zum Ausführen des Setup-Programms sind Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-107">Administrative rights are required to run the setup program.</span></span>

<span data-ttu-id="f3b4f-108">**Hinweis**  Während des Upgrades auf Application Virtualization (App-V) 4.5 oder höhere Versionen werden die Berechtigungen für den Registrierungsschlüssel HKCU geändert.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-108">**Note** During the upgrade to Application Virtualization (App-V)4.5 or later versions, the permissions to the HKCU registry key are changed.</span></span> <span data-ttu-id="f3b4f-109">Aus diesem Grund verlieren Benutzer die zuvor festgelegten Benutzerkonfigurationen wie Benutzer konfigurierte Einstellungen für den getrennten Modus.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-109">Because of this, users will lose user configurations that were set previously, such as user-configured Disconnected Mode settings.</span></span> <span data-ttu-id="f3b4f-110">Wenn der Benutzer nicht aktiv vom Konfigurieren des Verhaltens der Clientbenutzeroberfläche durch eine Berechtigungs Sperre eingeschränkt wird, kann der Benutzer diese Einstellungen nach einer Veröffentlichungsaktualisierung zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-110">If the user is not actively restricted from configuring client user interface behavior through a permission lockdown, the user can reset these preferences after a publishing refresh.</span></span>

 

<span data-ttu-id="f3b4f-111">**Wichtig**  Wenn Sie auf Version 4.6 oder eine neuere Version des App-V-Clients aktualisieren, müssen Sie das richtige Installationsprogramm für das Betriebssystem des Computers, 32-Bit oder 64-Bit verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-111">**Important** When upgrading to version4.6 or a later version of the App-V Client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="f3b4f-112">Bei der Installation tritt ein Fehler auf, und es wird eine Fehlermeldung angezeigt, wenn Sie das falsche Installationsprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-112">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

 

**<span data-ttu-id="f3b4f-113">So aktualisieren Sie den Application Virtualization-Desktop Client</span><span class="sxs-lookup"><span data-stu-id="f3b4f-113">To upgrade the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="f3b4f-114">Beenden Sie alle virtuellen Anwendungen, klicken Sie mit der rechten Maustaste auf das App-V-Desktop Client Symbol, das im Windows-Desktopbenachrichtigungsbereich angezeigt wird, und wählen Sie **Beenden** aus, um den vorhandenen Client zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-114">Shut down all virtual applications, right-click the App-V Desktop Client icon displayed in the Windows desktop notification area, and select **Exit** to shut down the existing client.</span></span>

2.  <span data-ttu-id="f3b4f-115">Nachdem Sie die richtige Installationsarchiv Datei abgerufen und auf Ihrem Computer gespeichert haben, doppelklicken Sie darauf, um das Archiv zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-115">After you have obtained the correct installer archive file and saved it to your computer, double-click it to expand the archive.</span></span>

3.  <span data-ttu-id="f3b4f-116">Suchen Sie nach der setup.exe-Datei, und doppelklicken Sie auf setup.exe, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-116">Browse to find the setup.exe file, and double-click setup.exe to start the installation.</span></span>

4.  <span data-ttu-id="f3b4f-117">Der Assistent überprüft das System, um sicherzustellen, dass alle erforderlichen Software installiert ist, und fordert Sie auf, eine der folgenden Komponenten zu installieren, wenn Sie nicht vorhanden sind:</span><span class="sxs-lookup"><span data-stu-id="f3b4f-117">The wizard checks the system to ensure that all prerequisite software is installed and will prompt you to install any of the following, if missing:</span></span>

    -   <span data-ttu-id="f3b4f-118">Microsoft VisualC + + 2005SP1-Paket (x86)</span><span class="sxs-lookup"><span data-stu-id="f3b4f-118">Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>

    -   <span data-ttu-id="f3b4f-119">Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="f3b4f-119">Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

    -   <span data-ttu-id="f3b4f-120">Microsoft-Anwendungsfehler Berichterstattung</span><span class="sxs-lookup"><span data-stu-id="f3b4f-120">Microsoft Application Error Reporting</span></span>

    <span data-ttu-id="f3b4f-121">**Hinweis**  Für Version 4.6 und höher wird der Assistent auch die folgende Softwarevoraussetzungen installieren:</span><span class="sxs-lookup"><span data-stu-id="f3b4f-121">**Note** For version4.6 and higher, the wizard will also install the following software prerequisite:</span></span>

    -   <span data-ttu-id="f3b4f-122">Microsoft VisualC + + 2008SP1-Paket (x86)</span><span class="sxs-lookup"><span data-stu-id="f3b4f-122">Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

     

5.  <span data-ttu-id="f3b4f-123">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-123">Click **Install**.</span></span> <span data-ttu-id="f3b4f-124">Der Installationsfortschritt wird angezeigt, und der Status wechselt von " **Ausstehend** " in " **Installieren**".</span><span class="sxs-lookup"><span data-stu-id="f3b4f-124">Installation progress is displayed, and the status changes from **Pending** to **Installing**.</span></span> <span data-ttu-id="f3b4f-125">Der Installationsstatus ändert sich **in erfolgreich,** wenn jeder Schritt erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-125">Installation status changes to **Succeeded** as each step is completed successfully.</span></span>

6.  <span data-ttu-id="f3b4f-126">Wenn das Dialogfeld **Application Virtualization Desktop Client** angezeigt wird und eine Meldung angezeigt wird, die besagt, dass eine ältere Version des Clients auf dem Computer gefunden wurde, klicken Sie auf **weiter** , um auf die neue Version zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-126">When the **Application Virtualization Desktop Client** dialog appears and displays a message stating that an older version of the client has been found on the computer, click **Next** to upgrade to the new version.</span></span>

7.  <span data-ttu-id="f3b4f-127">Wenn der Bildschirm " **Lizenzvertrag** " angezeigt wird, lesen Sie den Lizenzvertrag, und wenn Sie damit einverstanden sind, klicken Sie auf **Ich stimme den Bedingungen des Lizenzvertrags**zu, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-127">When the **License Agreement** screen is displayed, read the license agreement, and if you agree, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

8.  <span data-ttu-id="f3b4f-128">Wenn der InstallShield-Assistent das Dialogfeld " **bereit zum Upgrade des Programms** " anzeigt, klicken Sie auf **Upgrade** , um mit dem Upgrade zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-128">When the InstallShield Wizard displays the **Ready to Upgrade the Program** dialog screen, click **Upgrade** to begin the upgrade.</span></span> <span data-ttu-id="f3b4f-129">Auf dem nächsten Bildschirm wird angezeigt, dass der Client installiert wird.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-129">The next screen indicates that the client is being installed.</span></span>

    <span data-ttu-id="f3b4f-130">**Warnung**  Wenn Sie das Clientprogramm in Schritt 1 nicht heruntergefahren haben, wird möglicherweise eine Warnung " **Dateien in Verwendung** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-130">**Warning** If you did not shut down the client program in step 1, you might see a **Files In Use** warning displayed.</span></span> <span data-ttu-id="f3b4f-131">Wenn dies der Fall ist, klicken Sie mit der rechten Maustaste auf das App-V-Clientsymbol, das im Desktopbenachrichtigungsbereich angezeigt wird, und wählen Sie **Beenden** aus, um den vorhandenen Client zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-131">If this happens, right-click the App-V Client icon displayed in the desktop notification area and select **Exit** to shut down the existing client.</span></span> <span data-ttu-id="f3b4f-132">Klicken Sie dann auf wieder **holen** , um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-132">Then click **Retry** to continue.</span></span>

     

9.  <span data-ttu-id="f3b4f-133">Wenn die Installation erfolgreich abgeschlossen wurde, werden Sie aufgefordert, den Computer neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-133">When the installation completes successfully, you will be prompted to restart the computer.</span></span> <span data-ttu-id="f3b4f-134">Sie müssen den Computer neu starten, um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-134">You need to restart the computer to complete the installation.</span></span>

    <span data-ttu-id="f3b4f-135">**Vorsicht**  Wenn das Upgrade aus irgendeinem Grund fehlschlägt, müssen Sie den Computer neu starten, bevor Sie das Upgrade erneut versuchen.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-135">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

**<span data-ttu-id="f3b4f-136">So aktualisieren Sie den Application Virtualization-Client mithilfe der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="f3b4f-136">To upgrade the Application Virtualization Client by Using the Command Line</span></span>**

1.  <span data-ttu-id="f3b4f-137">Wenn Sie den App-V-Client mithilfe des setup.msi-Programms aktualisieren, stellen Sie sicher, dass alle erforderlichen Softwarekomponenten installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-137">If upgrading the App-V client using the setup.msi program, ensure that any necessary prerequisite software has been installed.</span></span>

    **<span data-ttu-id="f3b4f-138">Wichtig</span><span class="sxs-lookup"><span data-stu-id="f3b4f-138">Important</span></span>**  
    -   <span data-ttu-id="f3b4f-139">Für Version 4.6 und höher des App-V-Clients überprüft das setup.msi-Programm das System und schlägt mit einer Fehlermeldung fehl, die darauf hinweist, dass die Installation nicht fortgesetzt werden kann, wenn die erforderliche Software nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-139">For version4.6 and later of the App-V client, the setup.msi program checks the system and will fail with an error message indicating that installation cannot continue if prerequisite software is not installed.</span></span>

    -   <span data-ttu-id="f3b4f-140">Für App-V Version 4.6 können Befehlszeilenparameter während eines Upgrades nicht verwendet werden und werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-140">For App-V version4.6, command-line parameters cannot be used during an upgrade and will be ignored.</span></span>

     

2.  <span data-ttu-id="f3b4f-141">Im folgenden Befehlszeilenbeispiel wird die setup.msi-Datei verwendet, um den App-V-Client zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-141">The following command-line example uses the setup.msi file to upgrade the App-V Client.</span></span> <span data-ttu-id="f3b4f-142">Sie müssen das richtige Clientinstallationsprogramm verwenden, je nachdem, ob Sie den App-v-Desktop Client oder den App-v-Client für Remote Desktop Dienste (ehemals Terminal Dienste) aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-142">You will need to use the correct client installer program depending on whether you are upgrading the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span>

    **<span data-ttu-id="f3b4f-143">msiexec.exe/i "setup.msi"</span><span class="sxs-lookup"><span data-stu-id="f3b4f-143">msiexec.exe /i "setup.msi"</span></span>**

    <span data-ttu-id="f3b4f-144">**Wichtig**  Die Anführungszeichen sind nur erforderlich, wenn der Wert ein Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-144">**Important** The quotation marks are required only when the value contains a space.</span></span> <span data-ttu-id="f3b4f-145">Aus Gründen der Konsistenz werden alle Instanzen im vorherigen Beispiel als Anführungszeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-145">For consistency, all instances in the preceding example are shown as having quotation marks.</span></span>

     

**<span data-ttu-id="f3b4f-146">So aktualisieren Sie den Application Virtualization-Client für Remote Desktop Dienste</span><span class="sxs-lookup"><span data-stu-id="f3b4f-146">To upgrade the Application Virtualization Client for Remote Desktop Services</span></span>**

1.  <span data-ttu-id="f3b4f-147">Befolgen Sie die Standardrichtlinien Ihrer Organisation zum Installieren oder Aktualisieren von Anwendungen auf dem Remote Desktop-Sitzungshost Server (RDSession-Host).</span><span class="sxs-lookup"><span data-stu-id="f3b4f-147">Follow your organization’s standard policies for installing or upgrading applications on the Remote Desktop Session Host (RDSession Host) server.</span></span> <span data-ttu-id="f3b4f-148">Wenn das System Teil einer Farm ist, entfernen Sie den RDSession-Host aus der Serverfarm.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-148">If the system is part of a farm, remove the RDSession Host from the server farm.</span></span>

2.  <span data-ttu-id="f3b4f-149">Um den App-V-Client für Remote Desktop Dienste (vormals Terminal Dienste) zu aktualisieren, müssen Sie die Befehlszeile verwenden, da Sie den Client nicht manuell auf dem RDSession-Host aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-149">To upgrade the App-V Client for Remote Desktop Services (formerly Terminal Services), you must use the command line because you cannot upgrade the client manually on the RDSession Host.</span></span>

    <span data-ttu-id="f3b4f-150">**Hinweis**  In App-V Version 4,6 und höher können Sie zusätzlich zur Verwendung der Befehlszeile zum Upgrade des Clients auch eine Remote Desktop Sitzung verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-150">**Note** In App-V version 4.6 and later, in addition to using the command line to upgrade the client, you can also use a Remote Desktop session.</span></span> <span data-ttu-id="f3b4f-151">Zum Starten der Remote Desktop Sitzung sind keine speziellen Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-151">No special parameters are required to start the Remote Desktop session.</span></span>

     

3.  <span data-ttu-id="f3b4f-152">Nachdem der Client für das Upgrade der Remote Desktop Dienste abgeschlossen ist, starten Sie den Computer neu, und melden Sie sich beim RDSession-Host an.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-152">After the Client for Remote Desktop Services upgrade is complete, restart and log in to the RDSession Host.</span></span>

4.  <span data-ttu-id="f3b4f-153">Nachdem das System neu gestartet wurde, fügen Sie den Server der Serverfarm hinzu.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-153">After the system is restarted, add the server to the server farm.</span></span>

    <span data-ttu-id="f3b4f-154">**Vorsicht**  Wenn das Upgrade aus irgendeinem Grund fehlschlägt, müssen Sie den Computer neu starten, bevor Sie das Upgrade erneut versuchen.</span><span class="sxs-lookup"><span data-stu-id="f3b4f-154">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

## <span data-ttu-id="f3b4f-155">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f3b4f-155">Related topics</span></span>


[<span data-ttu-id="f3b4f-156">Bereitstellung von Application Virtualization und Upgrade Aspekte</span><span class="sxs-lookup"><span data-stu-id="f3b4f-156">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





