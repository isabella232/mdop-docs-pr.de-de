---
title: Bewährte Methoden für MED-V 2.0
description: Bewährte Methoden für MED-V 2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811560"
---
# <span data-ttu-id="1e123-103">Bewährte Methoden für MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="1e123-103">MED-V 2.0 Best Practices</span></span>


<span data-ttu-id="1e123-104">Wenn Sie MED-V in Ihrem Unternehmen planen, bereitstellen und verwalten, finden Sie möglicherweise die Empfehlungen für bewährte Methoden als hilfreich.</span><span class="sxs-lookup"><span data-stu-id="1e123-104">When you are planning, deploying, and managing MED-V in your enterprise, you may find the best practice recommendations to be useful.</span></span>

### <span data-ttu-id="1e123-105">Konfigurieren der erstmaligen Einrichtung für die unbeaufsichtigte Ausführung</span><span class="sxs-lookup"><span data-stu-id="1e123-105">Configure first time setup to run unattended</span></span>

<span data-ttu-id="1e123-106">Obwohl Sie alle gewünschten Einstellungen angeben können, ist es eine bewährte Methode von MED-V, die Datei "Sysprep. inf" zu erstellen, damit das erstmalige Setup im **unbeaufsichtigten** Modus ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1e123-106">Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode.</span></span> <span data-ttu-id="1e123-107">Dies erfordert, dass Sie alle erforderlichen Einstellungsinformationen angeben, während Sie den **Setup-Manager-** Assistenten fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="1e123-107">This requires you to provide all the required settings information as you continue through the **Setup Manager** wizard.</span></span> <span data-ttu-id="1e123-108">Weitere Informationen zum Konfigurieren des Med-v-Images finden Sie unter [Konfigurieren eines Windows Virtual PC-Images für med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="1e123-108">For more information about how to configure the MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="1e123-109">Deaktivieren von Wiederherstellungspunkten auf dem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="1e123-109">Disable restore points on the virtual machine</span></span>

<span data-ttu-id="1e123-110">Bevor Sie das MED-V Workspace-Paket erstellen, empfehlen wir, die Wiederherstellungspunkte auf dem virtuellen Computer zu deaktivieren, um zu verhindern, dass der differenzierende Datenträger unbegrenzt wächst.</span><span class="sxs-lookup"><span data-stu-id="1e123-110">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="1e123-111">Weitere Informationen finden Sie unter [so wird es gemacht: deaktivieren und Aktivieren der System Wiederherstellung unter Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="1e123-111">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

### <span data-ttu-id="1e123-112">Konfigurieren von MED-V-Bildern für die Verwendung lokaler Profile</span><span class="sxs-lookup"><span data-stu-id="1e123-112">Configure MED-V image to use local profiles</span></span>

<span data-ttu-id="1e123-113">Es wird empfohlen, nur die Richtlinien anzuwenden, die in einer Anwendungs Kompatibilitätsumgebung für Windows XP sinnvoll sind.</span><span class="sxs-lookup"><span data-stu-id="1e123-113">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="1e123-114">Beispielsweise müssen die Richtlinien für die Desktop Anpassung normalerweise nicht angewendet werden und sollten deaktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="1e123-114">For example, desktop customization policies do not typically have to be applied and should be disabled.</span></span> <span data-ttu-id="1e123-115">Weitere Informationen zum Zulassen nur lokaler Profile finden Sie unter [Gruppenrichtlinieneinstellungen für Roaming-Benutzerprofile](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="1e123-115">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

### <span data-ttu-id="1e123-116">Konfigurieren einer Leistungs Aktualisierung für Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="1e123-116">Configure a Group Policy performance update</span></span>

<span data-ttu-id="1e123-117">Standardmäßig wird die Gruppenrichtlinie jeweils um ein Byte auf einen Computer heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="1e123-117">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="1e123-118">Dies verursacht Verzögerungen, wenn MED-V zur Domäne hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1e123-118">This causes delays when MED-V is being joined to the domain.</span></span> <span data-ttu-id="1e123-119">Wenn Sie die Leistung von Gruppenrichtlinien erhöhen möchten, empfiehlt es sich, den folgenden Registrierungsschlüsselwert auf die Registrierung festzulegen:</span><span class="sxs-lookup"><span data-stu-id="1e123-119">To increase the performance of Group Policy, we recommend that you set the following registry key value to the registry:</span></span>

<span data-ttu-id="1e123-120">Registrierungsunterschlüssel: HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="1e123-120">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="1e123-121">Eintrag: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="1e123-121">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="1e123-122">Geben Sie Folgendes ein: DWORD</span><span class="sxs-lookup"><span data-stu-id="1e123-122">Type: DWORD</span></span>

<span data-ttu-id="1e123-123">Wert: 1</span><span class="sxs-lookup"><span data-stu-id="1e123-123">Value: 1</span></span>

### <span data-ttu-id="1e123-124">Verteilen des rechtlichen Hinweises über Gruppenrichtlinien anstelle des MED-V-Bilds</span><span class="sxs-lookup"><span data-stu-id="1e123-124">Distribute legal notice through Group Policy instead of in the MED-V image</span></span>

<span data-ttu-id="1e123-125">Wenn Endbenutzern vor dem Zugriff auf MED-V eine Vereinbarung zum Service Level (SLA) angezeigt werden soll, empfehlen wir, dass Sie die SLA später über Gruppenrichtlinien erzwingen, damit die SLA dem Endbenutzer nach Abschluss der erstmaligen Einrichtung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1e123-125">If you want end users to see a service level agreement (SLA) before they access MED-V, we recommend that you enforce the SLA through Group Policy later so that the SLA is displayed to the end user after the first time setup is finished.</span></span>

<span data-ttu-id="1e123-126">**Vorsicht**  Obwohl es bewährte Methode ist, das erstmalige Einrichten im **unbeaufsichtigten** Modus durchzuführen, wenn Sie sich entscheiden, die lokale Richtlinie oder den Registrierungseintrag so festzulegen, dass Sie eine SLA in Ihr Abbild (virtuelle Festplatte) einschließt, müssen Sie auch angeben, dass die erstmalige Einrichtung im **beaufsichtigten** Modus ausgeführt wird oder dass die erstmalige Einrichtung fehlschlagen kann.</span><span class="sxs-lookup"><span data-stu-id="1e123-126">**Caution** Even though a best practice is to run first time setup in **Unattended** mode, if you decide to set the local policy or registry entry to include an SLA in your image (virtual hard disk), you must also specify that first time setup is run in **Attended** mode, or first time setup can fail.</span></span>

 

### <span data-ttu-id="1e123-127">Komprimieren der virtuellen Festplatte</span><span class="sxs-lookup"><span data-stu-id="1e123-127">Compact the virtual hard disk</span></span>

<span data-ttu-id="1e123-128">Wir empfehlen, dass Sie Ihre virtuelle Festplatte komprimieren, um leeren Speicherplatz freizugeben und die Größe der virtuellen Festplatte zu verringern.</span><span class="sxs-lookup"><span data-stu-id="1e123-128">We recommend that you compact your virtual hard disk to reclaim empty disk space and reduce the size of the virtual hard disk.</span></span> <span data-ttu-id="1e123-129">Weitere Informationen zum Komprimieren Ihrer virtuellen Festplatte finden Sie unter [Komprimieren der virtuellen MED-V-Festplatte](compacting-the-med-v-virtual-hard-disk.md).</span><span class="sxs-lookup"><span data-stu-id="1e123-129">For more information about how to compact your virtual hard disk, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

### <span data-ttu-id="1e123-130">Konfigurieren des virtuellen Computers zum Neustart auf dem Bluescreen-Absturz</span><span class="sxs-lookup"><span data-stu-id="1e123-130">Configure virtual machine to restart on blue screen crash</span></span>

<span data-ttu-id="1e123-131">Wir empfehlen, dass Sie den virtuellen Computer des MED-V-Arbeitsbereichs so konfigurieren, dass er automatisch neu gestartet wird, wenn ein Absturz des blauen Bildschirms auftritt.</span><span class="sxs-lookup"><span data-stu-id="1e123-131">We recommend that you configure the MED-V workspace virtual machine to automatically restart when it encounters a blue screen crash.</span></span> <span data-ttu-id="1e123-132">Wenn Sie diese Einstellung im Gast konfigurieren möchten, legen Sie den Wert für den AutoReboot im HKEY \ _LOCAL \ _MACHINE \\system\\currentcontrolset\\control\\crashcontrol-Taste auf "1" fest.</span><span class="sxs-lookup"><span data-stu-id="1e123-132">To configure this setting in the guest, set the AutoReboot value in the HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\CrashControl key to “1”.</span></span>

<span data-ttu-id="1e123-133">Sie können diese Einstellung auch konfigurieren, indem Sie auf **Start**und **dann auf**Systemsteuerung und dann auf **System**klicken.</span><span class="sxs-lookup"><span data-stu-id="1e123-133">You can also configure this setting by clicking **Start**, clicking **Control Panel**, and then clicking **System**.</span></span> <span data-ttu-id="1e123-134">Klicken Sie dann im **Start-und Wiederherstellungs** Bereich der Registerkarte **erweitert** auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="1e123-134">Then, in the **Startup and Recovery** area of the **Advanced** tab, click **Settings**.</span></span> <span data-ttu-id="1e123-135">Aktivieren Sie das Kontrollkästchen **automatisch neu starten** , und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e123-135">Select the **Automatically restart** check box and click **OK**.</span></span>

### <span data-ttu-id="1e123-136">MED-V-Bild vor dem versiegeln sichern</span><span class="sxs-lookup"><span data-stu-id="1e123-136">Back up MED-V image before sealing it</span></span>

<span data-ttu-id="1e123-137">Wir empfehlen, dass Sie eine Sicherungskopie des MED-V-Bilds erstellen, bevor Sie es versiegeln.</span><span class="sxs-lookup"><span data-stu-id="1e123-137">We recommend that you create a backup copy of the MED-V image before you seal it.</span></span> <span data-ttu-id="1e123-138">Weitere Informationen zum Abdichten Ihres Med-v-Bilds finden Sie unter [Konfigurieren eines Windows Virtual PC-Images für med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="1e123-138">For more information about sealing your MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="1e123-139">Installieren von Windows Virtual PC zuletzt bei der Installation aus einer Batchdatei</span><span class="sxs-lookup"><span data-stu-id="1e123-139">Install Windows Virtual PC last when installing from a batch file</span></span>

<span data-ttu-id="1e123-140">Wenn Sie die Med-v-Komponenten mithilfe einer Batchdatei installieren, geben Sie an, dass Windows Virtual PC und der Windows Virtual PC-Hotfix nach dem Med-v-Host-Agent und den Med-v-Arbeitsbereichs Paketdateien installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e123-140">When you install the MED-V components by using a batch file, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="1e123-141">Dadurch wird sichergestellt, dass Windows Update keinen Eingriff in den Installationsvorgang verursacht, da ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1e123-141">This ensures that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

### <span data-ttu-id="1e123-142">Installieren des MED-V-Arbeitsbereichs aus dem lokalen Ordner</span><span class="sxs-lookup"><span data-stu-id="1e123-142">Install MED-V workspace from local folder</span></span>

<span data-ttu-id="1e123-143">Aufgrund von Problemen, die bei der Installation von Med-v von einem Netzwerkspeicherort auftreten können, empfiehlt es sich, die Setupdateien des Med-v-Arbeitsbereichs lokal zu kopieren und dann setup.exe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1e123-143">Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a><span data-ttu-id="1e123-144">Verwalten der Druckerumleitung nur auf eine Weise</span><span class="sxs-lookup"><span data-stu-id="1e123-144">Manage printer redirection in one manner only</span></span>

<span data-ttu-id="1e123-145">Wenn ein Drucker manuell auf dem virtuellen MED-V-Gastcomputer installiert ist und der gleiche Drucker später auf dem Hostcomputer installiert ist, ist das Ergebnis, dass er zwei Mal im Gast installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e123-145">If a printer is manually installed on the MED-V guest virtual machine, and the same printer is later installed on the host computer, the result is that it is installed two times in the guest.</span></span> <span data-ttu-id="1e123-146">Um dies zu vermeiden, empfehlen wir, dass Sie die Druckerumleitung nur auf eine Art und Weise verwalten: Deaktivieren Sie die Umleitung, und installieren Sie Drucker manuell auf dem Gast, oder aktivieren Sie die Umleitung, und installieren Sie Drucker nicht manuell auf dem Gast.</span><span class="sxs-lookup"><span data-stu-id="1e123-146">To avoid this situation, we recommend as MED-V best practice that you manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a><span data-ttu-id="1e123-147">Konfigurieren von Einstellungen für MED-V Guest-Patches</span><span class="sxs-lookup"><span data-stu-id="1e123-147">Configure settings for MED-V guest patching</span></span>

<span data-ttu-id="1e123-148">Sie können steuern, wann und wie lange der virtuelle MED-V-Computer aufwacht, um automatische Updates zu erhalten, indem Sie die entsprechenden Konfigurationswerte in der Registrierung definieren.</span><span class="sxs-lookup"><span data-stu-id="1e123-148">You can control when and for how long the MED-V virtual machine awakens to receive automatic updates by defining the relevant configuration values in the registry.</span></span> <span data-ttu-id="1e123-149">Eine optimale Methode für med-v besteht darin, das Aktivierungsintervall so festzulegen, dass es dem Zeitpunkt entspricht, zu dem Sie reguläre Updates für MED-V Virtual Machines geplant haben.</span><span class="sxs-lookup"><span data-stu-id="1e123-149">A MED-V best practice is to set your wake-up interval to match the time when you have scheduled regular updates for MED-V virtual machines.</span></span> <span data-ttu-id="1e123-150">Darüber hinaus empfiehlt es sich, diese Einstellungen so zu konfigurieren, dass Sie dem Verhalten des Hostcomputers ähneln.</span><span class="sxs-lookup"><span data-stu-id="1e123-150">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

<span data-ttu-id="1e123-151">Weitere Informationen zum Konfigurieren von Einstellungen für med-v Guest-Patches finden Sie unter [Verwalten von automatischen Updates für med-v-Arbeitsbereiche](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="1e123-151">For more information about how to configure settings for MED-V guest patching, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

### <span data-ttu-id="1e123-152">Konfigurieren von Antivirus/Sicherungssoftware</span><span class="sxs-lookup"><span data-stu-id="1e123-152">Configure antivirus/backup software</span></span>

<span data-ttu-id="1e123-153">Um zu verhindern, dass Antivirenprogramme die Leistung des virtuellen Desktops beeinträchtigen, empfehlen wir, dass Sie die folgenden virtuellen Computerdatei Typen von einem beliebigen Antivirus-oder Sicherungsprozess ausschließen, der auf dem MED-V-Hostcomputer ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="1e123-153">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend that when you can, you exclude the following virtual machine file types from any antivirus or backup process that is running on the MED-V host computer:</span></span>

-   <span data-ttu-id="1e123-154">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="1e123-154">\*.VMC</span></span>

-   <span data-ttu-id="1e123-155">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="1e123-155">\*.VUD</span></span>

-   <span data-ttu-id="1e123-156">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="1e123-156">\*.VSV</span></span>

-   <span data-ttu-id="1e123-157">\*. VHD</span><span class="sxs-lookup"><span data-stu-id="1e123-157">\*.VHD</span></span>

## <span data-ttu-id="1e123-158">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1e123-158">Related topics</span></span>


[<span data-ttu-id="1e123-159">Sicherheit und Schutz für MED-V</span><span class="sxs-lookup"><span data-stu-id="1e123-159">Security and Protection for MED-V</span></span>](security-and-protection-for-med-v.md)

 

 





