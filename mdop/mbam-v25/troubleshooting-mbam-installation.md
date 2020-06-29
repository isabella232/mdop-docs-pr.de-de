---
title: Problembehandlung für MBAM 2.5-Installationsfehlern
description: Hier erfahren Sie, wie Sie MBAM 2,5-Installationsprobleme beheben.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804547"
---
# <span data-ttu-id="b4038-103">Problembehandlung für MBAM 2.5-Installationsfehlern</span><span class="sxs-lookup"><span data-stu-id="b4038-103">Troubleshooting MBAM 2.5 installation problems</span></span>

<span data-ttu-id="b4038-104">In diesem Artikel wird erläutert, wie Sie Probleme mit der 2,5-Installation von Microsoft BitLocker Administration and Monitoring (MBAM) in einer eigenständigen Konfiguration beheben.</span><span class="sxs-lookup"><span data-stu-id="b4038-104">This article introduces how to troubleshoot Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 installation issues in a standalone configuration.</span></span>

## <span data-ttu-id="b4038-105">Verweisen auf MBAM-Protokolldateien zur Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="b4038-105">Referring MBAM log files for troubleshooting</span></span>

<span data-ttu-id="b4038-106">MBAM umfasst die Protokollierung für die Server Installation, die Clientinstallation und die Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b4038-106">MBAM includes logging for server installation, client installation, and events.</span></span> <span data-ttu-id="b4038-107">Auf diese Protokollierung sollte zur Problembehandlung verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b4038-107">This logging should be referred to for troubleshooting.</span></span> 
 
### <span data-ttu-id="b4038-108">MBAM-Server Installationsprotokolldateien</span><span class="sxs-lookup"><span data-stu-id="b4038-108">MBAM server installation log files</span></span>

<span data-ttu-id="b4038-109">MBAMServerSetup.exe generiert die folgenden Protokolldateien im Ordner "% Temp%" des Benutzers während der MBAM-Installation:</span><span class="sxs-lookup"><span data-stu-id="b4038-109">MBAMServerSetup.exe generates the following log files in the user’s %temp% folder during MBAM installation:</span></span><br /> **<span data-ttu-id="b4038-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 Nummern>. log</span><span class="sxs-lookup"><span data-stu-id="b4038-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 numbers>.log</span></span>**

<span data-ttu-id="b4038-111">MBAMServerSetup.exe protokolliert die Aktionen, die während der Installation des MBAM-Setups und der MBAM-Server Features ausgeführt wurden:</span><span class="sxs-lookup"><span data-stu-id="b4038-111">MBAMServerSetup.exe logs the actions that were taken during MBAM setup and MBAM server feature installation:</span></span><br /> **<span data-ttu-id="b4038-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="b4038-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log</span></span>**

<span data-ttu-id="b4038-113">MBAMServerSetup.exe protokolliert weitere Aktionen, die während der Installation ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="b4038-113">MBAMServerSetup.exe logs additional actions that were taken during installation.</span></span>

### <span data-ttu-id="b4038-114">MBAM-Client Installationsprotokolldatei</span><span class="sxs-lookup"><span data-stu-id="b4038-114">MBAM client installation log file</span></span>

<span data-ttu-id="b4038-115">Die Clientinstallation wird in der folgenden Protokolldatei im Ordner "% Temp%" (oder an einem benutzerdefinierten Speicherort) aufgezeichnet, je nachdem, wie der Client installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b4038-115">The client installation is recorded in the following log file in the %temp% folder (or a custom location, depending on how the client was installed):</span></span> <br />**<span data-ttu-id="b4038-116">MSI \<five random characters\> . log</span><span class="sxs-lookup"><span data-stu-id="b4038-116">MSI\<five random characters\>.log</span></span>**

<span data-ttu-id="b4038-117">Dieses Protokoll enthält die Aktionen, die während der MBAM-Clientinstallation ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b4038-117">This log contains the actions that are taken during MBAM client installation.</span></span>
 
### <span data-ttu-id="b4038-118">MBAM-Clientereignisprotokoll Kanal</span><span class="sxs-lookup"><span data-stu-id="b4038-118">MBAM client event-logging channel</span></span>

<span data-ttu-id="b4038-119">MBAM verfügt über separate Ereignis Protokollierungs Kanäle.</span><span class="sxs-lookup"><span data-stu-id="b4038-119">MBAM has separate event-logging channels.</span></span> <span data-ttu-id="b4038-120">Die Administrator-, Analyse-und Betriebsprotokoll Dateien befinden sich in der Ereignisanzeige unter **Anwendungs-und Dienstprotokolle**  >  **Microsoft**  >  **Windows**-  >  **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="b4038-120">The Admin, Analytical, and Operational log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span>

<span data-ttu-id="b4038-121">Die folgende Tabelle enthält eine kurze Beschreibung der einzelnen Ereignisprotokolle.</span><span class="sxs-lookup"><span data-stu-id="b4038-121">The following table provides a brief description of each event log.</span></span>
 
|<span data-ttu-id="b4038-122">Ereignisprotokoll</span><span class="sxs-lookup"><span data-stu-id="b4038-122">Event log</span></span>| <span data-ttu-id="b4038-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4038-123">Description</span></span>|
|----------|-------|
|<span data-ttu-id="b4038-124">Microsoft-Windows-MBAM/Administrator</span><span class="sxs-lookup"><span data-stu-id="b4038-124">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="b4038-125">Enthält Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="b4038-125">Contains error messages</span></span>|
|<span data-ttu-id="b4038-126">Microsoft-Windows-MBAM/Analyse</span><span class="sxs-lookup"><span data-stu-id="b4038-126">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="b4038-127">Enthält erweiterte Protokollierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="b4038-127">Contains advanced logging information</span></span>|
|<span data-ttu-id="b4038-128">Microsoft-Windows-MBAM/betriebsbereit</span><span class="sxs-lookup"><span data-stu-id="b4038-128">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="b4038-129">Enthält Erfolgs Nachrichten</span><span class="sxs-lookup"><span data-stu-id="b4038-129">Contains success messages</span></span>|

### <span data-ttu-id="b4038-130">MBAM Server-Ereignisprotokollkanal</span><span class="sxs-lookup"><span data-stu-id="b4038-130">MBAM server event-logging channel</span></span>

<span data-ttu-id="b4038-131">Die Protokolldateien befinden sich in der Ereignisanzeige unter **Anwendungs-und Dienstprotokolle**  >  **Microsoft**  >  **Windows**-  >  **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="b4038-131">The log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span> <span data-ttu-id="b4038-132">Die folgende Tabelle enthält Serverereignisprotokolle, die in MBAM 2,5 eingeführt wurden:</span><span class="sxs-lookup"><span data-stu-id="b4038-132">The following table includes server event logs that were introduced in MBAM 2.5:</span></span>

|<span data-ttu-id="b4038-133">Ereignisprotokoll</span><span class="sxs-lookup"><span data-stu-id="b4038-133">Event log</span></span>| <span data-ttu-id="b4038-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4038-134">Description</span></span>|
|--------|-------------|
|<span data-ttu-id="b4038-135">Microsoft-Windows-MBAM/Administrator</span><span class="sxs-lookup"><span data-stu-id="b4038-135">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="b4038-136">Enthält Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="b4038-136">Contains error messages</span></span>|
|<span data-ttu-id="b4038-137">Microsoft-Windows-MBAM/Analyse</span><span class="sxs-lookup"><span data-stu-id="b4038-137">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="b4038-138">Enthält erweiterte Protokollierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="b4038-138">Contains advanced logging information</span></span>|
|<span data-ttu-id="b4038-139">Microsoft-Windows-MBAM/betriebsbereit</span><span class="sxs-lookup"><span data-stu-id="b4038-139">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="b4038-140">Enthält Erfolgs Nachrichten</span><span class="sxs-lookup"><span data-stu-id="b4038-140">Contains success messages</span></span>|

### <span data-ttu-id="b4038-141">MBAM-Webdienstprotokolle</span><span class="sxs-lookup"><span data-stu-id="b4038-141">MBAM web service logs</span></span>

<span data-ttu-id="b4038-142">Jedes MBAM-Webdienstprotokoll schreibt Protokollierungsinformationen in eine SVCLOG-Datei.</span><span class="sxs-lookup"><span data-stu-id="b4038-142">Each MBAM web service log writes logging information to an SVCLOG file.</span></span> <span data-ttu-id="b4038-143">Standardmäßig schreibt jeder Webdienst die Ablaufverfolgungsdatei unter einen Ordner, dessen Namen im C:\inetpub\Microsoft BitLocker-Verwaltungs Solution\Logs-Ordner verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4038-143">By default, each web service writes the trace file under a folder that uses its name in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span>

<span data-ttu-id="b4038-144">Sie können das Tool Dienstablauf Verfolgungs Anzeige (Teil von Microsoft Visual Studio) verwenden, um die SVCLOG-Ablaufverfolgungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b4038-144">You can use the service trace viewer tool (part of Microsoft Visual Studio) to review the svclog traces.</span></span>

## <span data-ttu-id="b4038-145">Problembehandlung bei Verschlüsselungs-und Berichterstattungsproblemen</span><span class="sxs-lookup"><span data-stu-id="b4038-145">Troubleshooting encryption and reporting issues</span></span>

<span data-ttu-id="b4038-146">Dieser Abschnitt enthält Informationen zur Problembehandlung für Serverfunktionen, Clientfunktionen, Konfigurationseinstellungen und bekannte Probleme:</span><span class="sxs-lookup"><span data-stu-id="b4038-146">This section contains troubleshooting information for server functionality, client functionality, configuration settings, and known issues:</span></span>
 
### <span data-ttu-id="b4038-147">MBAM-Clientinstallation, Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="b4038-147">MBAM client installation, Group Policy settings</span></span>

<span data-ttu-id="b4038-148">Ermitteln Sie, ob der MBAM-Agent auf dem Clientcomputer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b4038-148">Determine whether the MBAM agent is installed on the client computer.</span></span> <span data-ttu-id="b4038-149">Wenn MBAM installiert ist, wird ein Dienst mit dem Namen BitLocker-Verwaltungs Client Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="b4038-149">When MBAM is installed, it creates a service that is named BitLocker Management Client Service.</span></span> <span data-ttu-id="b4038-150">Dieser Dienst ist so konfiguriert, dass er automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b4038-150">This service is configured to start automatically.</span></span> <span data-ttu-id="b4038-151">Ermitteln Sie, ob der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4038-151">Determine whether the service is running.</span></span>

<span data-ttu-id="b4038-152">Stellen Sie sicher, dass MBAM-Gruppenrichtlinieneinstellungen auf dem Clientcomputer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4038-152">Make sure that MBAM Group Policy settings are applied on the client computer.</span></span> <span data-ttu-id="b4038-153">Der folgende Registrierungsunterschlüssel wird erstellt, wenn die Gruppenrichtlinieneinstellungen auf dem Clientcomputer angewendet wurden: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**</span><span class="sxs-lookup"><span data-stu-id="b4038-153">The following registry subkey is created if the Group Policy settings were applied on the client computer: **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**</span></span>

<span data-ttu-id="b4038-154">Überprüfen Sie, ob dieser Schlüssel vorhanden ist und mit Werten pro Gruppenrichtlinieneinstellungen gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="b4038-154">Verify that this key exists and is populated by using values per Group Policy settings.</span></span>

### <span data-ttu-id="b4038-155">MBAM-Agent in der anfänglichen Verzögerungszeit</span><span class="sxs-lookup"><span data-stu-id="b4038-155">MBAM Agent in the initial delay period</span></span>

<span data-ttu-id="b4038-156">Der MBAM-Client startet den Vorgang nicht unmittelbar nach der Installation.</span><span class="sxs-lookup"><span data-stu-id="b4038-156">The MBAM client doesn't start the operation immediately after installation.</span></span> <span data-ttu-id="b4038-157">Es gibt eine anfängliche zufällige Verzögerung von 1 bis 18 Minuten, bevor der MBAM-Agent seinen Vorgang startet.</span><span class="sxs-lookup"><span data-stu-id="b4038-157">There is an initial random delay of 1–18 minutes before the MBAM Agent starts its operation.</span></span> <span data-ttu-id="b4038-158">Zusätzlich zu der anfänglichen Verzögerung gibt es eine Verzögerung von mindestens 90 Minuten.</span><span class="sxs-lookup"><span data-stu-id="b4038-158">In addition to the initial delay, there is a delay of at least 90 minutes.</span></span> <span data-ttu-id="b4038-159">(Die Verzögerung hängt von den Gruppenrichtlinieneinstellungen ab, die für die Häufigkeit der Überprüfung des Clientstatus konfiguriert sind.) Daher ist die Gesamtverzögerung, bevor ein Client den Vorgang *random startup delay*startet, die  +  *Häufigkeits Verzögerung für den Client zur Überprüfung der Häufigkeit*beim Start verzögert.</span><span class="sxs-lookup"><span data-stu-id="b4038-159">(The delay depends on the Group Policy settings that are configured for the frequency of checking the client status.) Therefore, the total delay before a client starts operation is *random startup delay* + *client checking frequency delay*.</span></span>

<span data-ttu-id="b4038-160">Wenn die Ereignisprotokolle für Betriebs-und Administratoren leer sind, hat der Client den Vorgang noch nicht begonnen und befindet sich in der zuvor erwähnten Verzögerungszeit.</span><span class="sxs-lookup"><span data-stu-id="b4038-160">If the Operational and Admin event logs are blank, the client has not started the operation yet and is in the delay period that was mentioned earlier.</span></span> <span data-ttu-id="b4038-161">Wenn Sie die Verzögerung umgehen möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="b4038-161">If you want to bypass the delay, follow these steps:</span></span>
 
1. <span data-ttu-id="b4038-162">Beenden des BitLocker-Verwaltungs Client-Dienst Diensts</span><span class="sxs-lookup"><span data-stu-id="b4038-162">Stop the BitLocker Management Client Service service.</span></span>

2. <span data-ttu-id="b4038-163">Erstellen Sie unter dem Registrierungsschlüssel **HKEY_LOCAL_MACHINE \software\microsoft\mbam** den Registrierungswert **NoStartupDelay** , legen Sie seinen Typ auf **REG_DWORD**, und legen Sie dann seinen Wert auf **1**.</span><span class="sxs-lookup"><span data-stu-id="b4038-163">Under the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** registry subkey, create the **NoStartupDelay** registry value, set its type to **REG_DWORD**, and then set its value to **1**.</span></span>

3. <span data-ttu-id="b4038-164">Setzen Sie unter **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**die Werte für **ClientWakeupFrequency** und **StatusReportingFrequency** auf **1**.</span><span class="sxs-lookup"><span data-stu-id="b4038-164">Under **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**, set the **ClientWakeupFrequency** and **StatusReportingFrequency** values to **1**.</span></span> <span data-ttu-id="b4038-165">Diese Werte werden auf die ursprünglichen Einstellungen zurückgesetzt, nachdem die Gruppenrichtlinienupdates auf dem Computer installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b4038-165">These values will revert to their original settings after Group Policy updates are on the computer.</span></span>

4. <span data-ttu-id="b4038-166">Starten Sie den BitLocker-Verwaltungs Client-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b4038-166">Start the BitLocker Management Client Service service.</span></span>

<span data-ttu-id="b4038-167">Wenn Sie sich nach dem Start des Diensts lokal auf dem Computer anmelden und keine Fehler auftreten, sollten Sie eine Anforderung erhalten, den Computer innerhalb einer Minute zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="b4038-167">After the service starts, if you log in locally on the computer and there are no errors, you should receive a request to encrypt the computer within one minute.</span></span> <span data-ttu-id="b4038-168">Wenn Sie keine Anforderung erhalten, sollten Sie die MBAM-Administrator Protokolle auf Fehlereinträge überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b4038-168">If you do not receive a request, you should review the MBAM Admin logs for any error entries.</span></span>

### <span data-ttu-id="b4038-169">Der Computer verfügt nicht über ein TPM-Gerät, oder das TPM-Gerät ist im BIOS nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b4038-169">Computer does not have a TPM device, or the TPM device is not enabled in the BIOS</span></span>

<span data-ttu-id="b4038-170">Überprüfen Sie das MBAM-Administrator Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="b4038-170">Review the MBAM Admin event log.</span></span> <span data-ttu-id="b4038-171">Im MBAM-Administrator Ereignisprotokoll sehen Sie einen Ereigniseintrag, der wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="b4038-171">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

<span data-ttu-id="b4038-172">Öffnen Sie die TPM-Verwaltung (TPM. msc), und überprüfen Sie, ob auf dem Computer ein TPM-Gerät installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b4038-172">Open TPM Management (tpm.msc), and check whether the computer has a TPM device.</span></span> <span data-ttu-id="b4038-173">Wenn TPM. msc kein Gerät anzeigt, öffnen Sie den Geräte-Manager (devmgmt. msc), und suchen Sie unter Sicherheitsgeräten nach einem vertrauenswürdigen Plattformmodul.</span><span class="sxs-lookup"><span data-stu-id="b4038-173">If tpm.msc does not show a device, open Device Manager (devmgmt.msc), and check for a Trusted Platform Module under Security Devices.</span></span> <span data-ttu-id="b4038-174">Wenn kein Trusted Platform Module-Gerät angezeigt wird, kann dies aus einem der folgenden Gründe zutreffen:</span><span class="sxs-lookup"><span data-stu-id="b4038-174">If you do not see a Trusted Platform Module device, this might be true for one of the following reasons:</span></span>

* <span data-ttu-id="b4038-175">Ihr System verfügt nicht über ein Trusted Platform Module (TPM/Security)-Gerät.</span><span class="sxs-lookup"><span data-stu-id="b4038-175">Your system doesn't have a Trusted Platform Module (TPM/Security) device.</span></span>

* <span data-ttu-id="b4038-176">Das TPM-Gerät ist im BIOS deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b4038-176">The TPM device is disabled in the BIOS.</span></span>

* <span data-ttu-id="b4038-177">Das TPM-Gerät ist im BIOS aktiviert, die Verwaltung des TPM-Geräts aus der Betriebssystem Einstellung ist im BIOS jedoch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b4038-177">TPM Device is enabled in the BIOS, but management of the TPM device from the operating system setting is disabled in the BIOS.</span></span>

* <span data-ttu-id="b4038-178">Sie verwenden keinen Microsoft-Treiber für das TPM-Gerät.</span><span class="sxs-lookup"><span data-stu-id="b4038-178">You aren't using a Microsoft driver for the TPM device.</span></span> <span data-ttu-id="b4038-179">Überprüfen Sie die Geräte, die im Geräte-Manager aufgeführt sind, um den Microsoft TPM-Gerätetreiber zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b4038-179">Review the devices that are listed in device manager to identify the Microsoft TPM device driver.</span></span>

<span data-ttu-id="b4038-180">Wenn das TPM-Gerät nicht den C:\Windows\System32\tpm.sys Treiber verwendet, sollten Sie den Treiber aktualisieren, indem Sie die C:\Windows\Inf\tpm.inf-Datei auswählen.</span><span class="sxs-lookup"><span data-stu-id="b4038-180">If the TPM device is not using the C:\Windows\System32\tpm.sys driver, you should update the driver by selecting the C:\Windows\Inf\tpm.inf file.</span></span>

### <span data-ttu-id="b4038-181">Computer hat keine gültige System Partition</span><span class="sxs-lookup"><span data-stu-id="b4038-181">Computer does not have a valid SYSTEM partition</span></span>

<span data-ttu-id="b4038-182">Überprüfen Sie das MBAM-Administrator Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="b4038-182">Review the MBAM Admin event log.</span></span> <span data-ttu-id="b4038-183">Im MBAM-Administrator Ereignisprotokoll sehen Sie einen Ereigniseintrag, der wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="b4038-183">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

<span data-ttu-id="b4038-184">Für BitLocker ist eine System Partition erforderlich, um die Verschlüsselung zu aktivieren ([BitLocker-Laufwerkverschlüsselung in Windows 7: häufig gestellte Fragen](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span><span class="sxs-lookup"><span data-stu-id="b4038-184">BitLocker requires a SYSTEM partition to enable encryption ([BitLocker Drive Encryption in Windows 7: Frequently Asked Questions](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span></span>

<span data-ttu-id="b4038-185">MBAM erstellt die Systempartition nicht automatisch.</span><span class="sxs-lookup"><span data-stu-id="b4038-185">MBAM doesn't create the system partition automatically.</span></span> <span data-ttu-id="b4038-186">Sie können das BitLocker Drive Preparation Utility (bdehdcfg.exe) verwenden, um die Systempartition zu erstellen und die erforderlichen Startdateien zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="b4038-186">You can use the BitLocker drive preparation utility (bdehdcfg.exe) to create the system partition and move the required startup files.</span></span>

<span data-ttu-id="b4038-187">So können Sie beispielsweise den Befehl **% Windir% \system32\bdeHdCfg.exe-Target Standardgröße 300 – quiet** verwenden, um das Laufwerk im Hintergrund vorzubereiten, bevor Sie MBAM bereitstellen, um die Laufwerke zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="b4038-187">For example, you can use the command **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** to prepare the drive silently before you deploy MBAM to encrypt the drives.</span></span> <span data-ttu-id="b4038-188">Hierfür ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b4038-188">This requires a restart.</span></span> <span data-ttu-id="b4038-189">Sie können die Aktion auch erstellen, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b4038-189">You can also script the action if this is required.</span></span> <span data-ttu-id="b4038-190">Das folgende Dokument beschreibt das BitLocker-Laufwerk Vorbereitungs Tool:</span><span class="sxs-lookup"><span data-stu-id="b4038-190">The following document describes the BitLocker Drive Preparation Tool:</span></span>

[<span data-ttu-id="b4038-191">Beschreibung des BitLocker-Laufwerk Vorbereitungstools</span><span class="sxs-lookup"><span data-stu-id="b4038-191">Description of the BitLocker Drive Preparation Tool</span></span>](https://support.microsoft.com/help/933246)

### <span data-ttu-id="b4038-192">Laufwerke sind nicht für ein kompatibles Dateisystem formatiert</span><span class="sxs-lookup"><span data-stu-id="b4038-192">Drives are not formatted to have a compatible file system</span></span>

<span data-ttu-id="b4038-193">Informationen zu den [Dateisystemanforderungen für BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements)finden Sie im TechNet-Artikel.</span><span class="sxs-lookup"><span data-stu-id="b4038-193">See the [TechNet article for file system requirements for BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span></span>

### <span data-ttu-id="b4038-194">Gruppenrichtlinienkonflikt</span><span class="sxs-lookup"><span data-stu-id="b4038-194">Group Policy conflict</span></span>

<span data-ttu-id="b4038-195">Im MBAM-Administrator Ereignisprotokoll sehen Sie einen Ereigniseintrag, der wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="b4038-195">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

<span data-ttu-id="b4038-196">Überprüfen Sie Ihre Gruppenrichtlinieneinstellungen, um sicherzustellen, dass Sie keine widersprüchlichen Einstellungen zwischen den MBAM-Gruppenrichtlinieneinstellungen haben.</span><span class="sxs-lookup"><span data-stu-id="b4038-196">Verify your Group Policy settings to make sure that you do not have a conflicting setting among the MBAM Group Policy settings.</span></span>

<span data-ttu-id="b4038-197">Sie sollten die Gruppenrichtlinie mithilfe der MDOP-MBAM-Vorlage und nicht mit der BitLocker-Laufwerk Verschlüsselungs Vorlage konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b4038-197">You should configure Group Policy by using the MDOP MBAM template and not the BitLocker Drive Encryption template.</span></span>

<span data-ttu-id="b4038-198">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b4038-198">For example:</span></span>

<span data-ttu-id="b4038-199">Unter Verschlüsselungseinstellungen für das Betriebssystemlaufwerk haben Sie TPM als Protector ausgewählt, und Sie haben auch die Option **Erweiterte Pins für den Start zulassen**ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b4038-199">Under Operating system drive encryption settings, you selected TPM as the protector, and you also selected **Allow enhanced PINs for startup**.</span></span> <span data-ttu-id="b4038-200">Hierbei handelt es sich um in Konflikt stehende Einstellungen, da für den TPM-only-Schutz keine PIN erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b4038-200">These are conflicting settings because TPM-only protection doesn't require a PIN.</span></span> <span data-ttu-id="b4038-201">Daher sollten Sie die Einstellung für erweiterte Pins deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b4038-201">Therefore, you should disable the enhanced PINs setting.</span></span>

### <span data-ttu-id="b4038-202">Der Benutzer hat möglicherweise eine Ausnahme beantragt.</span><span class="sxs-lookup"><span data-stu-id="b4038-202">User may have requested an exemption</span></span>

<span data-ttu-id="b4038-203">Wenn Sie die Gruppenrichtlinieneinstellung "Computer Configuration\Administrative Vorlagen\Windows-Komponenten\Internet Components\MDOP MBAM (BitLocker-Verwaltung) \Client Management\Configure Benutzer Freistellungs Richtlinien aktiviert haben, wird Benutzern die Möglichkeit angeboten, eine Ausnahme zu beantragen.</span><span class="sxs-lookup"><span data-stu-id="b4038-203">If you enabled the Computer Configuration\Administrative Templates\Windows Components\MDOP MBAM (BitLocker Management)\Client Management\Configure user exemption policy Group Policy setting, users will be offered the option to request an exemption.</span></span>

<span data-ttu-id="b4038-204">Wenn der Benutzer eine Befreiung anfordert, ist die Ausnahme standardmäßig 7 Tage gültig, und der Benutzer erhält während dieses Zeitraums keine Aufforderungen zur Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="b4038-204">By default, if the user requests an exemption, the exemption will be valid for 7 days, and the user will not receive prompts to encrypt during this period.</span></span> <span data-ttu-id="b4038-205">(Der Standardwert kann während der Richtlinienkonfiguration erhöht oder verringert werden.) Nachdem der frei stellungs Zeitraum beendet ist, wird der Benutzer aufgefordert, zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="b4038-205">(The default value can be increased or decreased during policy configuration.) After the exemption period is over, the user is prompted to encrypt.</span></span>

<span data-ttu-id="b4038-206">Der folgende Eintrag wird im MBAM-Administrator Ereignisprotokoll angezeigt, wenn ein Computer unter einer Benutzer Befreiung steht:</span><span class="sxs-lookup"><span data-stu-id="b4038-206">You will see the following entry in the MBAM Admin event log when a computer is under user exemption:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

<span data-ttu-id="b4038-207">Wenn Sie die Benutzer Befreiung für einen Computer manuell außer Kraft setzen möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="b4038-207">If you want to manually override user exemption for a computer, follow these steps:</span></span>
 
1. <span data-ttu-id="b4038-208">Setzen Sie den AllowUserExemption-Wert unter dem folgenden Registrierungsunterschlüssel auf **0** :</span><span class="sxs-lookup"><span data-stu-id="b4038-208">Set the AllowUserExemption value to **0** under the following registry subkey:</span></span> <br />
**<span data-ttu-id="b4038-209">HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement</span><span class="sxs-lookup"><span data-stu-id="b4038-209">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

2. <span data-ttu-id="b4038-210">Löschen Sie alle Registrierungswerte unter dem folgenden Registrierungsunterschlüssel, mit Ausnahme von **Agentversion**, **EncodedComputerName**und **installiert**:</span><span class="sxs-lookup"><span data-stu-id="b4038-210">Delete all the registry values under the following registry subkey except for **AgentVersion**, **EncodedComputerName**, and **Installed**:</span></span><br />
**<span data-ttu-id="b4038-211">HKEY_LOCAL_MACHINE \software\microsoft\mbam</span><span class="sxs-lookup"><span data-stu-id="b4038-211">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM</span></span>**

    <span data-ttu-id="b4038-212">**Hinweis** Sie müssen den MBAM-Agent neu starten, damit die Änderungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="b4038-212">**Note** You must restart the MBAM agent for the changes to take effect.</span></span>

<span data-ttu-id="b4038-213">Beachten Sie, dass diese Werte möglicherweise auf die ursprünglichen Einstellungen zurückgesetzt werden, nachdem Sie die Gruppenrichtlinie auf den Computer angewendet haben.</span><span class="sxs-lookup"><span data-stu-id="b4038-213">Be aware that after you apply Group Policy to the computer, these values may revert to their original settings.</span></span>

### <span data-ttu-id="b4038-214">WMI-Problem</span><span class="sxs-lookup"><span data-stu-id="b4038-214">WMI issue</span></span>

<span data-ttu-id="b4038-215">MBAM verwendet Methoden der Win32_EncryptableVolume-Klasse zum Verwalten von BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b4038-215">MBAM uses methods of the win32_encryptablevolume class to manage BitLocker.</span></span> <span data-ttu-id="b4038-216">Wenn dieses Modul nicht registriert oder beschädigt ist, funktioniert der MBAM-Client nicht ordnungsgemäß, und der folgende Ereigniseintrag wird im MBAM-Administrator Ereignisprotokoll angezeigt:</span><span class="sxs-lookup"><span data-stu-id="b4038-216">If this module is unregistered or corrupted, the MBAM client will not operate correctly, and you will see the following event entry in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

<span data-ttu-id="b4038-217">Darüber hinaus werden Sie möglicherweise feststellen, dass die Wiederherstellungs-und Hardware Richtlinien nicht mit Fehler Code 0x8007007e angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4038-217">Additionally, you may notice that the Recovery and Hardware policies do not apply with Error Code 0x8007007e.</span></span> <span data-ttu-id="b4038-218">Dies wird in "das angegebene Modul konnte nicht gefunden werden" übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b4038-218">This translates to "The specified module could not be found."</span></span>

<span data-ttu-id="b4038-219">Um dieses Problem zu beheben, sollten Sie die **Win32_EncryptableVolume** Klasse mithilfe des folgenden Befehls erneut registrieren:</span><span class="sxs-lookup"><span data-stu-id="b4038-219">To resolve this issue, you should reregister the **win32_encryptablevolume** class by using the following command:</span></span>

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <span data-ttu-id="b4038-220">Behandeln von Problemen mit der MBAM-Agent-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="b4038-220">Troubleshooting MBAM Agent communication issues</span></span>

<span data-ttu-id="b4038-221">Dieser Abschnitt enthält Informationen zur Problembehandlung für die folgenden Probleme, die sich auf die Kommunikation zwischen MBAM-Agents beziehen:</span><span class="sxs-lookup"><span data-stu-id="b4038-221">This section contains troubleshooting information for the following issues that are related to MBAM agent communication:</span></span>

### <span data-ttu-id="b4038-222">Falsche MBAM-Dienst-URL</span><span class="sxs-lookup"><span data-stu-id="b4038-222">Incorrect MBAM service URL</span></span>

<span data-ttu-id="b4038-223">Wenn der Wert des MBAM-Kompatibilitäts Status Diensts oder des Wiederherstellungs-und Hardware Diensts falsch ist, wird im MBAM-Administrator Ereignisprotokoll auf dem Clientcomputer ein Ereigniseintrag angezeigt, der wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="b4038-223">If the value of MBAM Compliance Status Service or Recovery and Hardware Service is incorrect, you'll see an event entry that resembles the following in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

<span data-ttu-id="b4038-224">Überprüfen Sie die Werte von **KeyRecoveryServiceEndPoint** und **StatusReportingServiceEndpoint** unter dem folgenden Registrierungsunterschlüssel auf dem Clientcomputer:</span><span class="sxs-lookup"><span data-stu-id="b4038-224">Verify the values of **KeyRecoveryServiceEndPoint** and **StatusReportingServiceEndpoint** under the following registry subkey on the client computer:</span></span> <br />
**<span data-ttu-id="b4038-225">HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement</span><span class="sxs-lookup"><span data-stu-id="b4038-225">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

<span data-ttu-id="b4038-226">Standardmäßig weist die URL für KeyRecoveryServiceEndPoint (MBAM-Wiederherstellungs-und Hardware Dienstendpunkt) das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="b4038-226">By default, the URL for KeyRecoveryServiceEndPoint (MBAM Recovery and Hardware service endpoint) is in the following format:</span></span> <br />
**<span data-ttu-id="b4038-227">http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="b4038-227">http://\<servername\>:\<port\>/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>**

<span data-ttu-id="b4038-228">Standardmäßig weist die URL für StatusReportingServiceEndpoint (MBAM Status Reporting Service Endpoint) das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="b4038-228">By default, the URL for StatusReportingServiceEndpoint (MBAM Status reporting service endpoint) is in the following format:</span></span><br />
**<span data-ttu-id="b4038-229">http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="b4038-229">http://\<servername\>:\<port\>/MBAMComplianceStatusService/StatusReportingService.svc</span></span>**

> [!Note]
> <span data-ttu-id="b4038-230">Die URL darf keine Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b4038-230">There should be no spaces in the URL.</span></span>

<span data-ttu-id="b4038-231">Wenn die Dienst-URL falsch ist, sollten Sie die Dienst-URL in der folgenden Gruppenrichtlinieneinstellung korrigieren:</span><span class="sxs-lookup"><span data-stu-id="b4038-231">If the service URL is incorrect, you should correct the service URL in the following Group Policy setting:</span></span>

<span data-ttu-id="b4038-232">**Computer Konfiguration**  >  **Richtlinien**  >  **Administrative Vorlagen**  >  **Windows-Komponenten**  >  **MDOP MBAM (BitLocker-Verwaltung)**  >  **Client Verwaltung**  >  **Konfigurieren von MBAM-Diensten**</span><span class="sxs-lookup"><span data-stu-id="b4038-232">**Computer configuration** > **Policies** > **Administrative Templates** > **Windows Components** > **MDOP MBAM (BitLocker Management)** > **Client Management** > **Configure MBAM Services**</span></span>

### <span data-ttu-id="b4038-233">Verbindungsproblem mit Auswirkungen auf den MBAM-Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="b4038-233">Connectivity issue that affects the MBAM administration server</span></span>

<span data-ttu-id="b4038-234">Der MBAM-Agent kann keine Aktualisierungen an der Datenbank Posten, wenn Verbindungsprobleme zwischen dem Client-Agent und dem MBAM-Verwaltungsserver bestehen.</span><span class="sxs-lookup"><span data-stu-id="b4038-234">The MBAM agent will be unable to post any updates to the database if connectivity issues exist between the client agent and the MBAM administration server.</span></span> <span data-ttu-id="b4038-235">In diesem Fall werden Verbindungsfehler Einträge im MBAM-Administrator Ereignisprotokoll auf dem Clientcomputer festgestellt:</span><span class="sxs-lookup"><span data-stu-id="b4038-235">In this case, you will notice connectivity failure entries in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

<span data-ttu-id="b4038-236">Grundlegende Überprüfungen:</span><span class="sxs-lookup"><span data-stu-id="b4038-236">Basic checks:</span></span>

* <span data-ttu-id="b4038-237">Überprüfen Sie die grundlegende Konnektivität, indem Sie den MBAM-Verwaltungsserver nach Name und IP-Adresse anpingen.</span><span class="sxs-lookup"><span data-stu-id="b4038-237">Verify basic connectivity by pinging the MBAM administration server by name and IP.</span></span> <span data-ttu-id="b4038-238">Überprüfen Sie, ob Sie über Telnet oder PortQry eine Verbindung mit der MBAM-Verwaltungswebsite oder dem Dienst Port herstellen können.</span><span class="sxs-lookup"><span data-stu-id="b4038-238">Check whether you can connect to the MBAM administration website or service port by using telnet or portqry.</span></span>

* <span data-ttu-id="b4038-239">Überprüfen Sie, ob der IIS-Dienst auf dem MBAM-Verwaltungs-und-Überwachungsserver ausgeführt wird und dass der MBAM-Webdienst denselben Port überwacht, der auf dem MBAM-Clientcomputer konfiguriert ist ( `netstat –ano | find "portnumber"` ).</span><span class="sxs-lookup"><span data-stu-id="b4038-239">Verify that the IIS service is running on the MBAM administration and monitoring server and that the MBAM web service is listening on the same port that is configured on the MBAM client computer (`netstat –ano | find "portnumber"`).</span></span>

* <span data-ttu-id="b4038-240">Überprüfen Sie, ob die für die MBAM-Website konfigurierte Portnummer IIS-Manager (inetmgr) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4038-240">Verify that the port number that is configured for the MBAM website is using IIS Manager (inetmgr).</span></span> <span data-ttu-id="b4038-241">Stellen Sie sicher, dass die Portnummer mit der Portnummer übereinstimmt, auf die der Client lauscht.</span><span class="sxs-lookup"><span data-stu-id="b4038-241">Make sure that the port number is the same as the port number on which the client is listening.</span></span> <span data-ttu-id="b4038-242">Stellen Sie sicher, dass die Portnummer nicht von einer anderen Anwendung freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b4038-242">Make sure that the port number is not shared by another application.</span></span> <span data-ttu-id="b4038-243">Beispielsweise sollte eine andere Anwendung auf dem Server nicht denselben Port verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4038-243">For example, another application on the server should not be using the same port.</span></span>

* <span data-ttu-id="b4038-244">Wenn eine Firewall vorhanden ist, stellen Sie sicher, dass der Port in der Firewall oder dem Proxy Server geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="b4038-244">If there is a firewall, make sure that the port is open in the firewall or proxy server.</span></span>

* <span data-ttu-id="b4038-245">Wenn die Kommunikation zwischen Client und Server sicher ist, stellen Sie sicher, dass Sie ein gültiges SSL-Zertifikat verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4038-245">If the communication between client and server is secure, make sure that you are using a valid SSL certificate.</span></span>

* <span data-ttu-id="b4038-246">Überprüfen Sie die Netzwerkkonnektivität zwischen dem Webserver und dem Datenbankserver, an den die Daten zum Einfügen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4038-246">Verify network connectivity between the web server and the database server to which the data is sent for insertion.</span></span> <span data-ttu-id="b4038-247">Sie können die Datenbankkonnektivität vom Webserver auf den Datenbankserver überprüfen, indem Sie den ODBC-Datenquellen Administrator verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4038-247">You can check database connectivity from the web server to the database server by using ODBC Data Source Administrator.</span></span> <span data-ttu-id="b4038-248">Detaillierte Informationen zur Problembehandlung der SQL Server-Verbindung finden Sie unter Problem [Behandlung beim Herstellen einer Verbindung mit dem SQL Server-Datenbankmodul](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span><span class="sxs-lookup"><span data-stu-id="b4038-248">Detailed SQL Server connection troubleshooting information is available in [How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span></span>

#### <span data-ttu-id="b4038-249">Problembehandlung des Verbindungsproblems</span><span class="sxs-lookup"><span data-stu-id="b4038-249">Troubleshooting the connectivity issue</span></span>

<span data-ttu-id="b4038-250">Stellen Sie sicher, dass die auf dem Client konfigurierte Dienst-URL richtig ist.</span><span class="sxs-lookup"><span data-stu-id="b4038-250">Make sure that the service URL that is configured on the client is correct.</span></span> <span data-ttu-id="b4038-251">Kopieren Sie den Wert der URL für KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) aus der Registrierung, und öffnen Sie Sie in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b4038-251">Copy the value of the URL for KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) from the registry, and open it in Internet Explorer.</span></span>

<span data-ttu-id="b4038-252">Kopieren Sie ebenfalls den Wert der URL für StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**), und öffnen Sie Sie in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b4038-252">Similarly, copy the value of the URL for StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**), and open it in Internet Explorer.</span></span>

> [!Note]
> <span data-ttu-id="b4038-253">Wenn Sie nicht von dem Clientcomputer zur URL navigieren können, sollten Sie die grundlegende Netzwerkkonnektivität vom Client zu dem Server testen, auf dem IIS ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4038-253">If you cannot browse to the URL from the client computer, you should test basic network connectivity from the client to the server that is running IIS.</span></span> <span data-ttu-id="b4038-254">Siehe die Punkte 1, 2, 3 und 4 im vorherigen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="b4038-254">See points 1, 2, 3, and 4 in the previous section.</span></span>

<span data-ttu-id="b4038-255">Überprüfen Sie darüber hinaus die Anwendungsprotokolle auf dem Administrations-und Überwachungsserver auf Fehler.</span><span class="sxs-lookup"><span data-stu-id="b4038-255">Additionally, review the Application logs on the administration and monitoring server for any errors.</span></span>

<span data-ttu-id="b4038-256">Sie können eine gleichzeitige Netzwerkablaufverfolgung zwischen dem Client und dem Server vornehmen und die Ablaufverfolgung überprüfen, um die Ursache für einen Verbindungsfehler zwischen dem Client-Agent und dem MBAM-Verwaltungsserver zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b4038-256">You can make a concurrent network trace between the client and the server, and review the trace to determine the cause of connection failure between the client agent and the MBAM administration server.</span></span>

> [!Note]
> <span data-ttu-id="b4038-257">Wenn Sie auf dem Clientcomputer zu den Dienst-URLs navigieren können und Verbindungsfehler Einträge in den MBAM-Administrator Ereignisprotokollen vorhanden sind, kann dies auf einen Verbindungsfehler zwischen dem Verwaltungsserver und dem Datenbankserver zurückzuführen sein.</span><span class="sxs-lookup"><span data-stu-id="b4038-257">If you can browse to the service URLs from the client computer and there are connectivity error entries in the MBAM admin event logs, this might be because of a connectivity failure between the administration server and the database server.</span></span>

<span data-ttu-id="b4038-258">Wenn Sie beide Dienst-URLs erfolgreich durchsuchen können und die Konnektivität zwischen dem Client und dem ausgeführten Server besteht, funktioniert IIS.</span><span class="sxs-lookup"><span data-stu-id="b4038-258">If you can successfully browse to both service URLs, and there is connectivity between the client and the server that is running, IIS is working.</span></span> <span data-ttu-id="b4038-259">Es gibt jedoch möglicherweise ein Problem bei der Kommunikation zwischen dem Server, auf dem IIS und dem Datenbankserver ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4038-259">However, there may be a problem in communication between the server that is running IIS and the database server.</span></span>

<span data-ttu-id="b4038-260">Möglicherweise können die MBAM-Dienste keine Verbindung mit dem Datenbankserver herstellen, weil ein Netzwerkproblem auftritt oder eine falsche Datenbankverbindungszeichenfolge festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="b4038-260">The MBAM services may be unable to connect to the database server because of a network issue or an incorrect database connection string setting.</span></span> <span data-ttu-id="b4038-261">Überprüfen Sie die Anwendungsprotokolle auf dem Verwaltungs-und Überwachungsserver.</span><span class="sxs-lookup"><span data-stu-id="b4038-261">Review the Application logs on the administration and monitoring server.</span></span> <span data-ttu-id="b4038-262">Möglicherweise werden Fehlereinträge oder Warnungen aus Quell ASP.NET 2.0.50727.0 angezeigt, die dem folgenden Protokolleintrag ähneln:</span><span class="sxs-lookup"><span data-stu-id="b4038-262">You might see errors entries or warnings from source ASP.NET 2.0.50727.0 that resemble the following log entry:</span></span>

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <span data-ttu-id="b4038-263">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="b4038-263">Possible causes</span></span>

##### <span data-ttu-id="b4038-264">Ursache 1</span><span class="sxs-lookup"><span data-stu-id="b4038-264">Cause 1</span></span>

<span data-ttu-id="b4038-265">Der Administrator hat während der Installation von Administrations-und Monitoring Server-Komponenten möglicherweise einen ungültigen Namen/Datenbanknamen für die Datenbankinstanz angegeben.</span><span class="sxs-lookup"><span data-stu-id="b4038-265">The administrator may have specified an invalid database instance name/database name during installation of administration and monitoring server components.</span></span>

<span data-ttu-id="b4038-266">Sie können die Datenbankverbindungszeichenfolgen mithilfe der IIS-Verwaltungskonsole überprüfen und korrigieren.</span><span class="sxs-lookup"><span data-stu-id="b4038-266">You can verify and correct the database connection strings by using the IIS Management console.</span></span> <span data-ttu-id="b4038-267">Öffnen Sie dazu den IIS-Manager, und navigieren Sie zu Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="b4038-267">To do this, open IIS Manager, and browse to Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="b4038-268">Führen Sie für jeden Dienst, der auf der linken Seite aufgeführt ist, die folgenden Schritte aus, um die Datenbankverbindungszeichenfolgen zu ändern:</span><span class="sxs-lookup"><span data-stu-id="b4038-268">For each service that is listed on the left side, follow these steps to change the database connection strings:</span></span>

1. <span data-ttu-id="b4038-269">Doppelklicken Sie in der **Ansicht Features**auf **Verbindungszeichenfolgen**.</span><span class="sxs-lookup"><span data-stu-id="b4038-269">In **Features View**, double-select **Connection Strings**.</span></span>

2. <span data-ttu-id="b4038-270">Wählen Sie auf der Seite **Verbindungszeichenfolgen** die Verbindungszeichenfolge aus, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="b4038-270">On the **Connection Strings** page, select the connection string that you want to change.</span></span>

3. <span data-ttu-id="b4038-271">Wählen Sie im Bereich **Aktionen** die Option **Bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="b4038-271">In the **Actions** pane, select **Edit**.</span></span>

4. <span data-ttu-id="b4038-272">Ändern Sie im Dialogfeld **Verbindungszeichenfolge bearbeiten** die Eigenschaften, die Sie ändern möchten, und wählen Sie dann **OK**aus.</span><span class="sxs-lookup"><span data-stu-id="b4038-272">In the **Edit Connection String** dialog box, change the properties that you want to change, and then select **OK**.</span></span>

##### <span data-ttu-id="b4038-273">Ursache 2</span><span class="sxs-lookup"><span data-stu-id="b4038-273">Cause 2</span></span>

<span data-ttu-id="b4038-274">SQL Server-Port, der in der Firewall blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="b4038-274">SQL Server port blocked in firewall.</span></span> <span data-ttu-id="b4038-275">Überprüfen Sie die Portnummer, für die SQL Server für die Überwachung konfiguriert ist, und stellen Sie sicher, dass der Port in der Firewall zwischen dem Verwaltungsserver und dem Datenbankserver geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="b4038-275">Verify the port number to which SQL Server is configured to listen, and make sure that the port is open in the firewall between the administration server and database server.</span></span>

##### <span data-ttu-id="b4038-276">Ursache 3</span><span class="sxs-lookup"><span data-stu-id="b4038-276">Cause 3</span></span>

<span data-ttu-id="b4038-277">Falsche SQL Server-TCP/IP-Bindungen.</span><span class="sxs-lookup"><span data-stu-id="b4038-277">Incorrect SQL server TCP/IP bindings.</span></span> <span data-ttu-id="b4038-278">Überprüfen Sie die SQL-TCP/IP-Bindungen im SQL Server-Konfigurations-Manager auf dem Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="b4038-278">Verify SQL TCP/IP bindings in SQL Server Configuration Manager on the database server.</span></span> <span data-ttu-id="b4038-279">MBAM erfordert, dass die Protokolle TCP/IP und Named Pipes für die Verbindung mit der Datenbank aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="b4038-279">MBAM requires that the TCP/IP and Named Pipes protocols are enabled to connect to the database.</span></span>

##### <span data-ttu-id="b4038-280">Ursache 4</span><span class="sxs-lookup"><span data-stu-id="b4038-280">Cause 4</span></span>

<span data-ttu-id="b4038-281">Das NT-AUTHORITY\NETWORK-Dienstkonto oder das Computerkonto des MBAM-Verwaltungsservers verfügen nicht über die erforderlichen Berechtigungen zum Herstellen einer Verbindung mit der SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b4038-281">The NT Authority\Network Service account or the MBAM Administration Server’s computer account doesn't have the required permissions to connect to the SQL database.</span></span>

<span data-ttu-id="b4038-282">Während der Installation von Datenbankkomponenten auf dem Datenbankserver erstellt das Installationsprogramm zwei lokale Gruppen: MBAM Compliance Auditing DB Access und MBAM Recovery and Hardware DB Access.</span><span class="sxs-lookup"><span data-stu-id="b4038-282">During the installation of database components on the database server, the installer creates two local groups: MBAM Compliance Auditing DB Access and MBAM Recovery and Hardware DB Access.</span></span>

<span data-ttu-id="b4038-283">Das NT-AUTHORITY\NETWORK-Dienstkonto, das Computerkonto des MBAM-Verwaltungsservers und der Benutzer, der die Datenbankkomponenten installiert, werden diesen Gruppen automatisch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b4038-283">The NT Authority\Network Service account, the MBAM administration server’s computer account, and the user who installs the database components are automatically added to these groups.</span></span>

<span data-ttu-id="b4038-284">Diesen Gruppen werden während der Installation die erforderlichen Berechtigungen für die Datenbank gewährt.</span><span class="sxs-lookup"><span data-stu-id="b4038-284">These groups are granted the required permissions on the database during the installation.</span></span> <span data-ttu-id="b4038-285">Alle Benutzer, die Teil dieser Gruppe sind, erhalten automatisch die erforderlichen Berechtigungen für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b4038-285">All users who are part of this group automatically receive the required permissions on the database.</span></span>

<span data-ttu-id="b4038-286">Der Webdienst kann aufgrund eines Berechtigungsproblems keine Verbindung mit dem Datenbankserver herstellen, wenn mindestens eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b4038-286">The web service may not connect to the database server because of a permissions issue if one or more of the following conditions are true:</span></span>

* <span data-ttu-id="b4038-287">Die zuvor erwähnten Gruppen werden aus den lokalen Gruppen auf dem Datenbankserver entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4038-287">The groups that were mentioned earlier are removed from the local groups on the database server.</span></span>

* <span data-ttu-id="b4038-288">Das NT-AUTHORITY\NETWORK-Dienstkonto und das Computerkonto des MBAM-Verwaltungsservers sind keine Mitglieder dieser Gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4038-288">The NT Authority\Network Service account and the MBAM administration server’s computer account are not members of these groups.</span></span>

* <span data-ttu-id="b4038-289">Diese Gruppen verfügen nicht über die erforderlichen Berechtigungen für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b4038-289">These groups do not have the required permissions on the database.</span></span>

<span data-ttu-id="b4038-290">In den Anwendungsprotokollen auf dem MBAM-Verwaltungs-und-Überwachungsserver werden Sie auf berechtigungsbezogene Fehler hinweisen, wenn eine der vorherigen Bedingungen erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="b4038-290">You will notice permissions-related errors in the Application logs on the MBAM administration and monitoring server if any of the previous conditions are true.</span></span> <span data-ttu-id="b4038-291">In diesem Fall sollten Sie das NT-AUTHORITY\NETWORK-Dienstkonto und das Computerkonto des MBAM-Verwaltungsservers manuell hinzufügen und ihm eine serverweite öffentliche Rolle auf dem SQL-Datenbankserver gewähren, der SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b4038-291">In that case, you should manually add the NT Authority\Network Service account and MBAM administration server’s computer account and grant them a server-wide public role on the SQL database server that is using SQL Server Management Studio (https://msdn.microsoft.com/library/aa337562.aspx).</span></span>

#### <span data-ttu-id="b4038-292">Überprüfen der Webdienstprotokolle</span><span class="sxs-lookup"><span data-stu-id="b4038-292">Review the web service logs</span></span>

<span data-ttu-id="b4038-293">Wenn in den Anwendungsprotokollen auf dem MBAM-Verwaltungsserver keine Ereignisse protokolliert werden, sollten Sie die Webdienstprotokolle (. SVCLOG) des MBAM-Webdiensts überprüfen, der auf dem MBAM-Verwaltungs-und-Überwachungsserver gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="b4038-293">If no events are logged in the Application logs on the MBAM administration server, it’s time to review the web service logs (.svclog) of the MBAM web service that is hosted on the MBAM administration and monitoring server.</span></span> <span data-ttu-id="b4038-294">Sie müssen das Tool für die Dienstablauf Verfolgungs Anzeige (SvcTraceViewer.exe) verwenden https://msdn.microsoft.com/library/ms732023.aspx , um die Protokolldatei anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b4038-294">You will have to use the Service Trace Viewer Tool (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx to view the log file.</span></span>

<span data-ttu-id="b4038-295">Sie sollten in erster Linie die Dienstablauf Verfolgungsprotokolle von RecoveryandHardwareService und ComplianceStatusService untersuchen.</span><span class="sxs-lookup"><span data-stu-id="b4038-295">You should primarily investigate the service trace logs of RecoveryandHardwareService and ComplianceStatusService.</span></span> <span data-ttu-id="b4038-296">Standardmäßig befinden sich Webdienstprotokolle im C:\inetpub\Microsoft BitLocker-Verwaltungs Solution\Logs-Ordner.</span><span class="sxs-lookup"><span data-stu-id="b4038-296">By default, web service logs are located in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span> <span data-ttu-id="b4038-297">Dort schreibt jeder Dienst seine SVCLOG-Datei unter seinen eigenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="b4038-297">There, each service writes its .svclog file under its own folder.</span></span>

<span data-ttu-id="b4038-298">Überprüfen Sie die Aktivität im Dienstablauf Verfolgungsprotokoll auf Fehler-oder Warnungs Einträge.</span><span class="sxs-lookup"><span data-stu-id="b4038-298">Review the activity in the service trace log for any error or warning entries.</span></span> <span data-ttu-id="b4038-299">Fehlereinträge sind standardmäßig rot hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="b4038-299">By default, error entries are highlighted in red.</span></span> <span data-ttu-id="b4038-300">Wählen Sie im rechten Bereich des Ablaufverfolgungs-Viewers die Fehlerbeschreibung aus, um detaillierte Informationen zum Fehlereintrag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b4038-300">Select the error description on the right pane of the trace viewer to view detailed information about the error entry.</span></span> <span data-ttu-id="b4038-301">Im folgenden wird ein Beispiel für einen Fehlereintrag aus dem Ablaufverfolgungsprotokoll angezeigt:</span><span class="sxs-lookup"><span data-stu-id="b4038-301">The following is a sample error entry from the trace log:</span></span>

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <span data-ttu-id="b4038-302">Erneute Installation oder Neukonfiguration der MBAM-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="b4038-302">Re-installation or reconfiguration of MBAM infrastructure</span></span>

<span data-ttu-id="b4038-303">Um die MBAM-Infrastruktur erneut zu installieren oder neu zu konfigurieren, müssen Sie die folgenden Punkte kennen:</span><span class="sxs-lookup"><span data-stu-id="b4038-303">To re-install or reconfigure MBAM infrastructure, you must know the following things:</span></span>

* <span data-ttu-id="b4038-304">Anwendungs Pool Konto</span><span class="sxs-lookup"><span data-stu-id="b4038-304">Application Pool account</span></span>

* <span data-ttu-id="b4038-305">MBAM-Gruppen (Helpdesk, erweitert, Gruppe "Berichtsbenutzer")</span><span class="sxs-lookup"><span data-stu-id="b4038-305">MBAM Groups (Helpdesk, Advanced, Report Users Group)</span></span>

* <span data-ttu-id="b4038-306">MBAM-Berichts-URL</span><span class="sxs-lookup"><span data-stu-id="b4038-306">MBAM Reports URL</span></span>

* <span data-ttu-id="b4038-307">SQL Server-Name und Datenbanknamen</span><span class="sxs-lookup"><span data-stu-id="b4038-307">SQL Server name and database names</span></span>

* <span data-ttu-id="b4038-308">MBAM ReadWrite-und ReadOnly-Konten</span><span class="sxs-lookup"><span data-stu-id="b4038-308">MBAM ReadWrite and ReadOnly Accounts</span></span>

### <span data-ttu-id="b4038-309">Anwendungs Pool Konto</span><span class="sxs-lookup"><span data-stu-id="b4038-309">Application Pool account</span></span>

<span data-ttu-id="b4038-310">Um das Anwendungs Pool Konto zu finden, melden Sie sich beim MBAM-Webserver an, öffnen Sie **Internet Informationsdienste (IIS)-Manager**, und wählen Sie dann **Anwendungs Pools**aus:</span><span class="sxs-lookup"><span data-stu-id="b4038-310">To find the Application Pool account, log on to the MBAM Web Server, open **Internet Information Services (IIS) Manager**, and then select **Application Pools**:</span></span>

![Anwendungspools](images/troubleshooting-MBAM-installation-1.png)

<span data-ttu-id="b4038-312">Der Dienstprinzipal Name (SPN) muss in diesem Konto eingestellt sein.</span><span class="sxs-lookup"><span data-stu-id="b4038-312">The Service Principal Name (SPN) must be set in this account.</span></span> <span data-ttu-id="b4038-313">Diese Einstellung ist für die Funktionalität von MBAM sehr wichtig.</span><span class="sxs-lookup"><span data-stu-id="b4038-313">This setting is very important to the functionality of MBAM.</span></span>

### <span data-ttu-id="b4038-314">MBAM-Gruppen (Helpdesk, erweitert, Gruppe "Berichtsbenutzer" und URL für Berichte)</span><span class="sxs-lookup"><span data-stu-id="b4038-314">MBAM Groups (Helpdesk, Advanced, Report Users Group and Reports URL)</span></span>

![MBAM-Gruppen](images/troubleshooting-MBAM-installation-2.png)

<span data-ttu-id="b4038-316">Hier finden Sie Informationen wie die Helpdesk-Gruppe, die erweiterte Helpdesk-Gruppe, die Berichtsbenutzer Gruppe und die MBAM-Berichts-URL.</span><span class="sxs-lookup"><span data-stu-id="b4038-316">This provides information such as Helpdesk Group, Advanced Helpdesk Group, Report Users group, and MBAM Reports URL.</span></span> <span data-ttu-id="b4038-317">Die URL des MBAM-Berichts muss im MBAM-Setup bereitgestellt werden und sollte wie folgt gelesen werden: http (s)://servername/reportserver.</span><span class="sxs-lookup"><span data-stu-id="b4038-317">The MBAM Reports URL must be provided in the MBAM setup and should read as: http(s)://servername/ReportServer.</span></span>

### <span data-ttu-id="b4038-318">SQL Server-Namen und Daten Bank Namen (DB)</span><span class="sxs-lookup"><span data-stu-id="b4038-318">SQL Server name and database (DB) names</span></span>

<span data-ttu-id="b4038-319">Um die SQL Server-Namen und-Instanzen zu finden, die das MBAM DBS hosten, melden Sie sich beim MBAM Web (IIS)-Server an, und navigieren Sie zum Registrierungsunterschlüssel Folowing:</span><span class="sxs-lookup"><span data-stu-id="b4038-319">To find the SQL Server names and instances hosting the MBAM DBs, log on to the MBAM Web (IIS) server and browse to the folowing registry subkey:</span></span>

**<span data-ttu-id="b4038-320">HKEY_LOCAL_MACHINE \software\microsoft\mbam Server\Web</span><span class="sxs-lookup"><span data-stu-id="b4038-320">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web</span></span>**

![Regedit](images/troubleshooting-MBAM-installation-3.png)

<span data-ttu-id="b4038-322">Die hervorgehobenen Abschnitte sind Verbindungszeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="b4038-322">The highlighted portions are connection strings.</span></span> <span data-ttu-id="b4038-323">Diese sollten den SQL Server-Namen, Datenbanknamen und Instanzen (sofern benannt) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b4038-323">These should have the SQL Server name, database names, and instances (if named).</span></span>

### <span data-ttu-id="b4038-324">MBAM ReadWrite-und ReadOnly-Konten</span><span class="sxs-lookup"><span data-stu-id="b4038-324">MBAM ReadWrite and ReadOnly accounts</span></span>

<span data-ttu-id="b4038-325">Diese Informationen befinden sich in der SQL Server-Datenbank, für die der Name bereits vom Webserver gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="b4038-325">This information will be in the SQL Server database, for which we already found the name from the web server.</span></span>

#### <span data-ttu-id="b4038-326">ReadWrite-Konto</span><span class="sxs-lookup"><span data-stu-id="b4038-326">ReadWrite account</span></span>

1. <span data-ttu-id="b4038-327">Melden Sie sich bei SQL Management Studio an.</span><span class="sxs-lookup"><span data-stu-id="b4038-327">Log in to the SQL Management Studio.</span></span>

2. <span data-ttu-id="b4038-328">Klicken Sie mit der rechten Maustaste auf **MBAM-Wiederherstellung und-Hardware**, wählen Sie **Eigenschaften**aus, und wählen Sie dann **Berechtigungen**aus.</span><span class="sxs-lookup"><span data-stu-id="b4038-328">Right-click **MBAM Recovery and Hardware**, select **Properties**, and then select **Permissions**.</span></span>

<span data-ttu-id="b4038-329">Der Name des Lab-Kontos lautet beispielsweise **MBAMWrite**.</span><span class="sxs-lookup"><span data-stu-id="b4038-329">For example, The the lab account name is **MBAMWrite**.</span></span> <span data-ttu-id="b4038-330">Der Anwendungs Pool und die ReadWrite-Konten sind so eingestellt, dass Sie identisch sind.</span><span class="sxs-lookup"><span data-stu-id="b4038-330">The Application Pool and ReadWrite accounts are set to be the same.</span></span>

![SQL DB](images/troubleshooting-MBAM-installation-4.png)

![DB-Eigenschaften](images/troubleshooting-MBAM-installation-5.png)

<span data-ttu-id="b4038-333">Navigieren Sie zu **Sicherheit** , und **melden** Sie sich dann in SQL Management Studio an.</span><span class="sxs-lookup"><span data-stu-id="b4038-333">Browse to **Security** and then **Logins** in SQL Management Studio.</span></span> <span data-ttu-id="b4038-334">Navigieren Sie zu dem Konto, das im vorherigen Screenshot angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="b4038-334">Browse to the account shown in the previous screenshot.</span></span>

![SQL-Sicherheit](images/troubleshooting-MBAM-installation-6.png)

<span data-ttu-id="b4038-336">Klicken Sie mit der rechten Maustaste auf die Konten, wechseln Sie zu **Eigenschaften Benutzerzuordnung**, und suchen Sie nach der MBAM-Wiederherstellungs-und-Hardware Datenbank:</span><span class="sxs-lookup"><span data-stu-id="b4038-336">Right-click the accounts, go to **Properties User Mapping**, and locate the MBAM Recovery and Hardware database:</span></span>

![Benutzerzuordnung](images/troubleshooting-MBAM-installation-7.png)

#### <span data-ttu-id="b4038-338">ReadOnly-Konto</span><span class="sxs-lookup"><span data-stu-id="b4038-338">ReadOnly account</span></span>

<span data-ttu-id="b4038-339">Öffnen Sie den SQL Server Reporting Services-Konfigurations-Manager auf dem SSRS-Server.</span><span class="sxs-lookup"><span data-stu-id="b4038-339">Open SQL Server Reporting Services Configuration Manager on the SSRS Server.</span></span> <span data-ttu-id="b4038-340">Wählen Sie **Berichts-Manager-URL**aus, und Durchsuchen Sie dann die **URLs**:</span><span class="sxs-lookup"><span data-stu-id="b4038-340">Select **Report Manager URL**, and then browse the **URLs**:</span></span>

![Berichts-Manager](images/troubleshooting-MBAM-installation-8.png)

<span data-ttu-id="b4038-342">Wählen Sie **Microsoft BitLocker-Verwaltung und-Überwachung**aus:</span><span class="sxs-lookup"><span data-stu-id="b4038-342">Select **Microsoft Bitlocker Administration and Monitoring**:</span></span>

![BitLocker-Verwaltung und-Überwachung](images/troubleshooting-MBAM-installation-9.png)

<span data-ttu-id="b4038-344">Wählen Sie **MaltaDatasource**:</span><span class="sxs-lookup"><span data-stu-id="b4038-344">Select **MaltaDatasource**:</span></span>

![DBS](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

<span data-ttu-id="b4038-347">MaltaDataSource sollte über den Namen des ReadOnly-Kontos verfügen und in MBAM-Setup verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4038-347">MaltaDataSource should have the ReadOnly Account name and should be used in MBAM setup.</span></span>

## <span data-ttu-id="b4038-348">Verweis</span><span class="sxs-lookup"><span data-stu-id="b4038-348">Reference</span></span>

<span data-ttu-id="b4038-349">Weitere Informationen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="b4038-349">For more information, see the following articles:</span></span>

[<span data-ttu-id="b4038-350">Bereitstellen von MBAM 2,5 in einer eigenständigen Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b4038-350">Deploying MBAM 2.5 in a standalone configuration</span></span>](https://support.microsoft.com/help/3046555)

[<span data-ttu-id="b4038-351">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="b4038-351">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
