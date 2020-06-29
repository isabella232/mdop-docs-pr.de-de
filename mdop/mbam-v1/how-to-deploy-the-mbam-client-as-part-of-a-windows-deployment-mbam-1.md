---
title: So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit
description: So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810840"
---
# <span data-ttu-id="015f4-103">So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit</span><span class="sxs-lookup"><span data-stu-id="015f4-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="015f4-104">Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="015f4-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="015f4-105">Der BitLocker-Client kann in eine Organisation integriert werden, indem die BitLocker-Verwaltung und-Verschlüsselung auf Client Computern während des Computer Imaging-und Windows-Bereitstellungsprozesses aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="015f4-105">The BitLocker Client can be integrated into an organization by enabling BitLocker management and encryption on client computers during the computer imaging and Windows deployment process.</span></span>

**<span data-ttu-id="015f4-106">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="015f4-106">Note</span></span>**  
<span data-ttu-id="015f4-107">Informationen zum Überprüfen der MBAM-Client Systemanforderungen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="015f4-107">To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>



<span data-ttu-id="015f4-108">Die Verschlüsselung von Clientcomputern mit BitLocker während der anfänglichen Abbild Erstellungsphase einer Windows-Bereitstellung kann den Verwaltungsaufwand für die MBAM-Implementierung senken.</span><span class="sxs-lookup"><span data-stu-id="015f4-108">Encryption of client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead for MBAM implementation.</span></span> <span data-ttu-id="015f4-109">Durch diesen Ansatz wird auch sichergestellt, dass alle bereitgestellten Computer bereits BitLocker ausführen und ordnungsgemäß konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="015f4-109">This approach also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="015f4-110">Warnung</span><span class="sxs-lookup"><span data-stu-id="015f4-110">Warning</span></span>**  
<span data-ttu-id="015f4-111">In diesem Thema wird beschrieben, wie Sie die Windows-Registrierung mit dem Registrierungs-Editor ändern.</span><span class="sxs-lookup"><span data-stu-id="015f4-111">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="015f4-112">Wenn Sie die Windows-Registrierung falsch ändern, können Sie zu schwerwiegenden Problemen führen, bei denen Sie möglicherweise eine Neuinstallation von Windows erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="015f4-112">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="015f4-113">Bevor Sie die Registrierung ändern, sollten Sie eine Sicherungskopie der Registrierungsdateien (System. dat und User. dat) erstellen.</span><span class="sxs-lookup"><span data-stu-id="015f4-113">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="015f4-114">Microsoft kann nicht garantieren, dass die Probleme, die beim Ändern der Registrierung auftreten, behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="015f4-114">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="015f4-115">Ändern Sie die Registrierung auf Ihr eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="015f4-115">Change the registry at your own risk.</span></span>



**<span data-ttu-id="015f4-116">So verschlüsseln Sie einen Computer als Teil der Windows-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="015f4-116">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="015f4-117">Wenn Ihre Organisation die Verwendung des TPM-Beschützers (Trusted Platform Module) oder der TPM + PIN Protector-Optionen in BitLocker plant, müssen Sie den TPM-Chip vor der anfänglichen Bereitstellung von MBAM aktivieren.</span><span class="sxs-lookup"><span data-stu-id="015f4-117">If your organization plans to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="015f4-118">Wenn Sie den TPM-Chip aktivieren, vermeiden Sie später einen Neustart des Prozesses, und Sie stellen sicher, dass die TPM-Chips entsprechend den Anforderungen Ihrer Organisation ordnungsgemäß konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="015f4-118">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="015f4-119">Sie müssen den TPM-Chip manuell im BIOS des Computers aktivieren.</span><span class="sxs-lookup"><span data-stu-id="015f4-119">You must activate the TPM chip manually in the computer's BIOS.</span></span> <span data-ttu-id="015f4-120">Weitere Informationen zum Konfigurieren des TPM-Chips finden Sie in der Herstellerdokumentation.</span><span class="sxs-lookup"><span data-stu-id="015f4-120">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>

2.  <span data-ttu-id="015f4-121">Installieren Sie den MBAM-Client-Agent.</span><span class="sxs-lookup"><span data-stu-id="015f4-121">Install the MBAM client agent.</span></span>

3.  <span data-ttu-id="015f4-122">Wir empfehlen, dass Sie den Computer einer Domäne hinzufügen...</span><span class="sxs-lookup"><span data-stu-id="015f4-122">We recommend that you join the computer to a domain...</span></span>

    -   <span data-ttu-id="015f4-123">Wenn der Computer nicht zu einer Domäne gehört, wird das Wiederherstellungskennwort nicht im MBAM-Schlüssel Wiederherstellungs Dienst gespeichert.</span><span class="sxs-lookup"><span data-stu-id="015f4-123">If the computer is not joined to a domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="015f4-124">Standardmäßig lässt MBAM keine Verschlüsselung zu, es sei denn, der Wiederherstellungsschlüssel kann gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="015f4-124">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="015f4-125">Wenn ein Computer im Wiederherstellungsmodus gestartet wird, bevor der Wiederherstellungsschlüssel auf dem MBAM-Server gespeichert wird, muss der Computer erneut abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="015f4-125">If a computer starts in recovery mode before the recovery key is stored on the MBAM server, the computer has to be reimaged.</span></span> <span data-ttu-id="015f4-126">Es steht keine Wiederherstellungsmethode zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="015f4-126">No recovery method is available.</span></span>

4.  <span data-ttu-id="015f4-127">Öffnen Sie eine Eingabeaufforderung als Administrator, beenden Sie den MBAM-Dienst, und setzen Sie den Dienst auf **manuell** oder **bei Bedarf**.</span><span class="sxs-lookup"><span data-stu-id="015f4-127">Open a command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**.</span></span> <span data-ttu-id="015f4-128">Führen Sie dann die folgende Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="015f4-128">Then, run the following commands:</span></span>

    **<span data-ttu-id="015f4-129">NET STOP mbamagent</span><span class="sxs-lookup"><span data-stu-id="015f4-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="015f4-130">SC config mbamagent Start = Demand</span><span class="sxs-lookup"><span data-stu-id="015f4-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="015f4-131">Festlegen der Registrierungseinstellungen für den MBAM-Agent zum Ignorieren von Gruppenrichtlinien und Ausführen der Verschlüsselung für das TPM nur für das **Betriebssystem** , um dies zu tun, führen Sie **Regedit**aus, und importieren Sie dann die Registrierungsschlüssel Vorlage aus c:\\Programme Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="015f4-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** To do this, run **regedit**, and then import the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="015f4-132">Wechseln Sie in regedit zu HKLM\\SOFTWARE\\Microsoft\\MBAM, und konfigurieren Sie die Einstellungen, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="015f4-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="015f4-133">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="015f4-133">Registry entry</span></span>

    <span data-ttu-id="015f4-134">Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="015f4-134">Configuration settings</span></span>

    <span data-ttu-id="015f4-135">Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="015f4-135">DeploymentTime</span></span>

    <span data-ttu-id="015f4-136">0 = aus</span><span class="sxs-lookup"><span data-stu-id="015f4-136">0 = OFF</span></span>

    <span data-ttu-id="015f4-137">1 = Verwenden von Bereitstellungszeit Richtlinieneinstellungen (Standard)</span><span class="sxs-lookup"><span data-stu-id="015f4-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="015f4-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="015f4-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="015f4-139">0 = Schlüssel Escrow nicht verwenden (die nächsten beiden Registrierungseinträge sind in diesem Fall nicht erforderlich.)</span><span class="sxs-lookup"><span data-stu-id="015f4-139">0 = Do not use key escrow (The next two registry entries are not required in this case.)</span></span>

    <span data-ttu-id="015f4-140">1 = Verwenden des Schlüssels Escrow in Key Recovery System (Standard)</span><span class="sxs-lookup"><span data-stu-id="015f4-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="015f4-141">Empfohlen: der Computer muss mit dem Schlüssel Wiederherstellungs Dienst kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="015f4-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="015f4-142">Vergewissern Sie sich, dass der Computer mit dem Dienst kommunizieren kann, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="015f4-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="015f4-143">Keyrecoveryoptions</span><span class="sxs-lookup"><span data-stu-id="015f4-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="015f4-144">0 = nur Wiederherstellungsschlüssel hochladen</span><span class="sxs-lookup"><span data-stu-id="015f4-144">0 = Upload Recovery Key Only</span></span>

    <span data-ttu-id="015f4-145">1 = Upload-Wiederherstellungsschlüssel und Schlüssel Wiederherstellungs Paket (Standard)</span><span class="sxs-lookup"><span data-stu-id="015f4-145">1 = Upload Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="015f4-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="015f4-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="015f4-147">Setzen Sie diesen Wert auf die URL für den Key Recovery Web Server.</span><span class="sxs-lookup"><span data-stu-id="015f4-147">Set this value to the URL for the Key Recovery web server.</span></span>

    <span data-ttu-id="015f4-148">Beispiel: http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.</span><span class="sxs-lookup"><span data-stu-id="015f4-148">Example: http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. <span data-ttu-id="015f4-149">Der MBAM-Agent startet das System während der MBAM-Clientbereitstellung neu.</span><span class="sxs-lookup"><span data-stu-id="015f4-149">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="015f4-150">Wenn Sie für diesen Neustart bereit sind, führen Sie den folgenden Befehl an einer Eingabeaufforderung als Administrator aus:</span><span class="sxs-lookup"><span data-stu-id="015f4-150">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="015f4-151">NET Start mbamagent</span><span class="sxs-lookup"><span data-stu-id="015f4-151">net start mbamagent</span></span>**

8. <span data-ttu-id="015f4-152">Wenn die Computer neu gestartet werden und das BIOS Sie auffordert, eine TPM-Änderung zu akzeptieren, übernehmen Sie die Änderung.</span><span class="sxs-lookup"><span data-stu-id="015f4-152">When the computers restarts and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="015f4-153">Starten Sie während des Windows-Client-Betriebssystem-Imaging-Prozesses den MBAM-Agentdienst neu, wenn Sie bereit sind, die Verschlüsselung zu starten.</span><span class="sxs-lookup"><span data-stu-id="015f4-153">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service.</span></span> <span data-ttu-id="015f4-154">Öffnen Sie dann zum Einrichten von Start auf **automatisch**eine Eingabeaufforderung als Administrator, und führen Sie die folgenden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="015f4-154">Then, to set start to **automatic**, open a command prompt as an administrator and run the following commands:</span></span>

   **<span data-ttu-id="015f4-155">SC config mbamagent Start = automatisch</span><span class="sxs-lookup"><span data-stu-id="015f4-155">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="015f4-156">NET Start mbamagent</span><span class="sxs-lookup"><span data-stu-id="015f4-156">net start mbamagent</span></span>**

10. <span data-ttu-id="015f4-157">Entfernen Sie die Registrierungswerte umgehen.</span><span class="sxs-lookup"><span data-stu-id="015f4-157">Remove the bypass registry values.</span></span> <span data-ttu-id="015f4-158">Führen Sie dazu Regedit aus, navigieren Sie zum Registrierungseintrag HKLM\\SOFTWARE\\Microsoft, klicken Sie mit der rechten Maustaste auf den **MBAM** -Knoten, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="015f4-158">To do this, run regedit, browse to the HKLM\\SOFTWARE\\Microsoft registry entry, right-click the **MBAM** node, and then click **Delete**.</span></span>

## <span data-ttu-id="015f4-159">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="015f4-159">Related topics</span></span>


[<span data-ttu-id="015f4-160">Bereitstellen des MBAM 1.0-Clients</span><span class="sxs-lookup"><span data-stu-id="015f4-160">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)









