---
title: So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit
description: So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810666"
---
# <span data-ttu-id="7ca4f-103">So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit</span><span class="sxs-lookup"><span data-stu-id="7ca4f-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="7ca4f-104">Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="7ca4f-105">Wenn Computer, die über einen TPM-Chip (Trusted Platform Module) verfügen, kann der BitLocker-Client in eine Organisation integriert werden, indem die BitLocker-Verwaltung und-Verschlüsselung auf Clientcomputern im Rahmen des Imaging-und Windows-Bereitstellungsprozesses aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-105">If computers that have a Trusted Platform Module (TPM) chip, the BitLocker client can be integrated into an organization by enabling BitLocker management and encryption on client computers as part of the imaging and Windows deployment process.</span></span>

**<span data-ttu-id="7ca4f-106">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7ca4f-106">Note</span></span>**  
<span data-ttu-id="7ca4f-107">Informationen zum Überprüfen der Systemanforderungen für die Microsoft BitLocker-Verwaltung und-Überwachung finden Sie unter [unterstützte MBAM 2,0-Konfigurationen](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="7ca4f-107">To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



<span data-ttu-id="7ca4f-108">Das Verschlüsseln von Clientcomputern mit BitLocker während der anfänglichen Abbild Erstellungsphase einer Windows-Bereitstellung kann den administrativen Overhead verringern, der für die Implementierung von MBAM in einer Organisation erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-108">Encrypting client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead necessary for implementing MBAM in an organization.</span></span> <span data-ttu-id="7ca4f-109">Außerdem wird sichergestellt, dass auf jedem bereitgestellten Computer bereits BitLocker ausgeführt wird und ordnungsgemäß konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-109">It also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="7ca4f-110">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7ca4f-110">Note</span></span>**  
<span data-ttu-id="7ca4f-111">Das Verfahren in diesem Thema beschreibt das Ändern der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-111">The procedure in this topic describes modifying the Windows registry.</span></span> <span data-ttu-id="7ca4f-112">Wenn Sie den Registrierungs-Editor falsch verwenden, kann dies zu schwerwiegenden Problemen führen, die eine Neuinstallation von Windows erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-112">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="7ca4f-113">Microsoft kann nicht garantieren, dass Probleme, die sich aus der fehlerhaften Verwendung des Registrierungs-Editors ergeben, behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-113">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="7ca4f-114">Verwenden Sie den Registrierungs-Editor auf eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-114">Use Registry Editor at your own risk.</span></span>



**<span data-ttu-id="7ca4f-115">So verschlüsseln Sie einen Computer als Teil der Windows-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="7ca4f-115">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="7ca4f-116">Wenn Ihre Organisation die Verwendung des TPM-Beschützers (Trusted Platform Module) oder der TPM + PIN Protector-Optionen in BitLocker plant, müssen Sie den TPM-Chip vor der anfänglichen Bereitstellung von MBAM aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-116">If your organization is planning to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="7ca4f-117">Wenn Sie den TPM-Chip aktivieren, vermeiden Sie später einen Neustart des Prozesses, und Sie stellen sicher, dass die TPM-Chips entsprechend den Anforderungen Ihrer Organisation ordnungsgemäß konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-117">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="7ca4f-118">Sie müssen den TPM-Chip manuell im BIOS des Computers aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-118">You must activate the TPM chip manually in the BIOS of the computer.</span></span>

    **<span data-ttu-id="7ca4f-119">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7ca4f-119">Note</span></span>**  
    <span data-ttu-id="7ca4f-120">Einige Anbieter stellen Tools bereit, mit denen Sie den TPM-Chip im BIOS innerhalb des Betriebssystems aktivieren und aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-120">Some vendors provide tools to turn on and activate the TPM chip in the BIOS from within the operating system.</span></span> <span data-ttu-id="7ca4f-121">Weitere Informationen zum Konfigurieren des TPM-Chips finden Sie in der Herstellerdokumentation.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-121">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>



2.  <span data-ttu-id="7ca4f-122">Installieren Sie den Client-Agent für Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-122">Install the Microsoft BitLocker Administration and Monitoring client agent.</span></span>

3.  <span data-ttu-id="7ca4f-123">Verbinden Sie den Computer mit einer Domäne (empfohlen).</span><span class="sxs-lookup"><span data-stu-id="7ca4f-123">Join the computer to a domain (recommended).</span></span>

    -   <span data-ttu-id="7ca4f-124">Wenn der Computer nicht der Domäne beigetreten ist, wird das Wiederherstellungskennwort nicht im MBAM-Schlüssel Wiederherstellungs Dienst gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-124">If the computer is not joined to the domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="7ca4f-125">Standardmäßig lässt MBAM keine Verschlüsselung zu, es sei denn, der Wiederherstellungsschlüssel kann gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-125">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="7ca4f-126">Wenn ein Computer im Wiederherstellungsmodus gestartet wird, bevor der Wiederherstellungsschlüssel auf dem MBAM-Server gespeichert wird, muss der Computer erneut abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-126">If a computer starts in recovery mode before the recovery key is stored on the MBAM Server, the computer has to be reimaged.</span></span> <span data-ttu-id="7ca4f-127">Es steht keine Wiederherstellungsmethode zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-127">No recovery method is available.</span></span>

4.  <span data-ttu-id="7ca4f-128">Führen Sie die Eingabeaufforderung als Administrator aus, beenden Sie den MBAM-Dienst, und legen Sie den Dienst auf **manuell** oder **bei Bedarf**, und beginnen Sie dann mit der Eingabe der folgenden Befehle:</span><span class="sxs-lookup"><span data-stu-id="7ca4f-128">Run the command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**, and then start by typing the following commands:</span></span>

    **<span data-ttu-id="7ca4f-129">NET STOP mbamagent</span><span class="sxs-lookup"><span data-stu-id="7ca4f-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="7ca4f-130">SC config mbamagent Start = Demand</span><span class="sxs-lookup"><span data-stu-id="7ca4f-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="7ca4f-131">Festlegen der Registrierungseinstellungen für den MBAM-Agent, um Gruppenrichtlinien zu ignorieren und das TPM nur für das **Betriebssystem zu verschlüsseln** , indem Sie **Regedit**ausführen und dann die Registrierungsschlüssel Vorlage aus c:\\Programme Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg. importieren</span><span class="sxs-lookup"><span data-stu-id="7ca4f-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** by running **Regedit**, and then importing the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="7ca4f-132">Wechseln Sie in regedit zu HKLM\\SOFTWARE\\Microsoft\\MBAM, und konfigurieren Sie die Einstellungen, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM, and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="7ca4f-133">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="7ca4f-133">Registry entry</span></span>

    <span data-ttu-id="7ca4f-134">Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="7ca4f-134">Configuration settings</span></span>

    <span data-ttu-id="7ca4f-135">Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="7ca4f-135">DeploymentTime</span></span>

    <span data-ttu-id="7ca4f-136">0 = aus</span><span class="sxs-lookup"><span data-stu-id="7ca4f-136">0 = OFF</span></span>

    <span data-ttu-id="7ca4f-137">1 = Verwenden von Bereitstellungszeit Richtlinieneinstellungen (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ca4f-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="7ca4f-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="7ca4f-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="7ca4f-139">0 = Schlüssel Escrow nicht verwenden (die nächsten beiden Registrierungseinträge sind in diesem Fall nicht erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7ca4f-139">0 = Do not use key escrow ( the next two registry entries are not required in this case)</span></span>

    <span data-ttu-id="7ca4f-140">1 = Verwenden des Schlüssels Escrow in Key Recovery System (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ca4f-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="7ca4f-141">Empfohlen: der Computer muss mit dem Schlüssel Wiederherstellungs Dienst kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="7ca4f-142">Vergewissern Sie sich, dass der Computer mit dem Dienst kommunizieren kann, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="7ca4f-143">Keyrecoveryoptions</span><span class="sxs-lookup"><span data-stu-id="7ca4f-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="7ca4f-144">0 = nur Uploads des Wiederherstellungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="7ca4f-144">0 = Uploads Recovery Key Only</span></span>

    <span data-ttu-id="7ca4f-145">1 = Uploads-Wiederherstellungsschlüssel und Schlüssel Wiederherstellungs Paket (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ca4f-145">1 = Uploads Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="7ca4f-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="7ca4f-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="7ca4f-147">Setzen Sie diesen Wert auf die URL für den Key Recovery Web Server, beispielsweise http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-147">Set this value to the URL for the Key Recovery web server, for example, http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. <span data-ttu-id="7ca4f-148">Der MBAM-Agent startet das System während der MBAM-Clientbereitstellung neu.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-148">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="7ca4f-149">Wenn Sie für diesen Neustart bereit sind, führen Sie den folgenden Befehl an einer Eingabeaufforderung als Administrator aus:</span><span class="sxs-lookup"><span data-stu-id="7ca4f-149">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="7ca4f-150">NET Start mbamagent</span><span class="sxs-lookup"><span data-stu-id="7ca4f-150">net start mbamagent</span></span>**

8. <span data-ttu-id="7ca4f-151">Wenn die Computer neu gestartet werden und das BIOS Sie auffordert, eine TPM-Änderung zu akzeptieren, übernehmen Sie die Änderung.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-151">When the computers restarts, and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="7ca4f-152">Wenn Sie während des Windows-Client-Betriebssystem-Imaging-Prozesses die Verschlüsselung starten möchten, starten Sie den MBAM-Agent-Dienst neu, und legen Sie Start to **Automatic** ab, indem Sie eine Eingabeaufforderung als Administrator ausführen und die folgenden Befehle eingeben:</span><span class="sxs-lookup"><span data-stu-id="7ca4f-152">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service, and set start to **automatic** by running a command prompt as an administrator and typing the following commands:</span></span>

   **<span data-ttu-id="7ca4f-153">SC config mbamagent Start = automatisch</span><span class="sxs-lookup"><span data-stu-id="7ca4f-153">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="7ca4f-154">NET Start mbamagent</span><span class="sxs-lookup"><span data-stu-id="7ca4f-154">net start mbamagent</span></span>**

10. <span data-ttu-id="7ca4f-155">Entfernen Sie die Registrierungswerte umgehen, indem Sie regedit ausführen, und wechseln Sie zum Registrierungseintrag HKLM\\SOFTWARE\\Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-155">Remove the bypass registry values by running Regedit and going to the HKLM\\SOFTWARE\\Microsoft registry entry.</span></span> <span data-ttu-id="7ca4f-156">Um den **MBAM** -Knoten zu löschen, klicken Sie mit der rechten Maustaste auf den Knoten, und klicken Sie auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-156">To delete the **MBAM** node, right-click the node and click **Delete**.</span></span>

## <span data-ttu-id="7ca4f-157">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7ca4f-157">Related topics</span></span>


[<span data-ttu-id="7ca4f-158">Bereitstellen des MBAM 2.0-Clients</span><span class="sxs-lookup"><span data-stu-id="7ca4f-158">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)









