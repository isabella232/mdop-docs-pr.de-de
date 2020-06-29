---
title: Sicherheitsüberlegungen zu MBAM2.5
description: Sicherheitsüberlegungen zu MBAM2.5
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811995"
---
# <span data-ttu-id="0076d-103">Sicherheitsüberlegungen zu MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="0076d-103">MBAM 2.5 Security Considerations</span></span>


<span data-ttu-id="0076d-104">Dieses Thema enthält die folgenden Informationen zum Sichern der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM):</span><span class="sxs-lookup"><span data-stu-id="0076d-104">This topic contains the following information about how to secure Microsoft BitLocker Administration and Monitoring (MBAM):</span></span>

-   [<span data-ttu-id="0076d-105">Konfigurieren von MBAM zum Escrow-und Speichern von OwnerAuth-Kennwörtern</span><span class="sxs-lookup"><span data-stu-id="0076d-105">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>](#bkmk-tpm)

-   [<span data-ttu-id="0076d-106">Konfigurieren von MBAM so, dass das TPM nach einer Sperrung automatisch freigegeben wird</span><span class="sxs-lookup"><span data-stu-id="0076d-106">Configure MBAM to automatically unlock the TPM after a lockout</span></span>](#bkmk-autounlock)

-   [<span data-ttu-id="0076d-107">Sichere Verbindungen mit SQL Server</span><span class="sxs-lookup"><span data-stu-id="0076d-107">Secure connections to SQL Server</span></span>](#bkmk-secure-databases)

-   [<span data-ttu-id="0076d-108">Erstellen von Konten und Gruppen</span><span class="sxs-lookup"><span data-stu-id="0076d-108">Create accounts and groups</span></span>](#bkmk-accts-groups)

-   [<span data-ttu-id="0076d-109">Verwenden von MBAM-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="0076d-109">Use MBAM log files</span></span>](#bkmk-logfiles)

-   [<span data-ttu-id="0076d-110">Überlegungen zu MBAM Database DSA</span><span class="sxs-lookup"><span data-stu-id="0076d-110">Review MBAM database TDE considerations</span></span>](#bkmk-tde)

-   [<span data-ttu-id="0076d-111">Grundlegendes zu allgemeinen Sicherheitsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="0076d-111">Understand general security considerations</span></span>](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a><span data-ttu-id="0076d-112">Konfigurieren von MBAM zum Escrow-und Speichern von OwnerAuth-Kennwörtern</span><span class="sxs-lookup"><span data-stu-id="0076d-112">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>

<span data-ttu-id="0076d-113">**Hinweis** Für Windows 10, Version 1607 oder höher, kann nur Windows den Besitz des TPM übernehmen.</span><span class="sxs-lookup"><span data-stu-id="0076d-113">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="0076d-114">Darüber hinaus wird das TPM-Besitzerkennwort beim Bereitstellen des TPMs nicht von Windows beibehalten.</span><span class="sxs-lookup"><span data-stu-id="0076d-114">In addition, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="0076d-115">Weitere Informationen finden Sie unter [TPM-Besitzerkennwort](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .</span><span class="sxs-lookup"><span data-stu-id="0076d-115">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="0076d-116">Je nach Konfiguration wird sich das Trusted Platform Module (TPM) in bestimmten Situationen selbst sperren, beispielsweise wenn zu viele falsche Kennwörter eingegeben werden und für einen bestimmten Zeitraum gesperrt bleiben können.</span><span class="sxs-lookup"><span data-stu-id="0076d-116">Depending on its configuration, the Trusted Platform Module (TPM) will lock itself in certain situations ─ such as when too many incorrect passwords are entered ─ and can remain locked for a period of time.</span></span> <span data-ttu-id="0076d-117">Während der TPM-Sperrung kann BitLocker nicht auf die Verschlüsselungsschlüssel zugreifen, um entsperrungs-oder Entschlüsselungsvorgänge durchzuführen, sodass der Benutzer seinen BitLocker-Wiederherstellungsschlüssel für den Zugriff auf das Betriebssystemlaufwerk eingeben muss.</span><span class="sxs-lookup"><span data-stu-id="0076d-117">During TPM lockout, BitLocker cannot access the encryption keys to perform unlock or decryption operations, requiring the user to enter their BitLocker recovery key to access the operating system drive.</span></span> <span data-ttu-id="0076d-118">Um die TPM-Sperrung zurückzusetzen, müssen Sie das TPM-OwnerAuth-Kennwort angeben.</span><span class="sxs-lookup"><span data-stu-id="0076d-118">To reset TPM lockout, you must provide the TPM OwnerAuth password.</span></span>

<span data-ttu-id="0076d-119">MBAM kann das TPM-OwnerAuth-Kennwort in der MBAM-Datenbank speichern, wenn es das TPM besitzt oder das Kennwort Escrows.</span><span class="sxs-lookup"><span data-stu-id="0076d-119">MBAM can store the TPM OwnerAuth password in the MBAM database if it owns the TPM or if it escrows the password.</span></span> <span data-ttu-id="0076d-120">OwnerAuth-Kennwörter können dann auf der Website Verwaltung und Überwachung problemlos aufgerufen werden, wenn Sie eine TPM-Sperrung wiederherstellen müssen, wodurch nicht mehr gewartet werden muss, bis die Sperre für sich selbst aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="0076d-120">OwnerAuth passwords are then easily accessible on the Administration and Monitoring Website when you must recover from a TPM lockout, eliminating the need to wait for the lockout to resolve on its own.</span></span>

### <span data-ttu-id="0076d-121">Treuhandservice für TPM-OwnerAuth in Windows 8 und höher</span><span class="sxs-lookup"><span data-stu-id="0076d-121">Escrowing TPM OwnerAuth in Windows 8 and higher</span></span>

<span data-ttu-id="0076d-122">**Hinweis** Für Windows 10, Version 1607 oder höher, kann nur Windows den Besitz des TPM übernehmen.</span><span class="sxs-lookup"><span data-stu-id="0076d-122">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="0076d-123">In addiiton wird Windows das TPM-Besitzerkennwort beim Bereitstellen des TPMs nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="0076d-123">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="0076d-124">Weitere Informationen finden Sie unter [TPM-Besitzerkennwort](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .</span><span class="sxs-lookup"><span data-stu-id="0076d-124">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="0076d-125">In Windows 8 oder höher muss MBAM nicht mehr das TPM besitzen, um das OwnerAuth-Kennwort speichern zu können, solange das OwnerAuth auf dem lokalen Computer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0076d-125">In Windows 8 or higher, MBAM no longer must own the TPM to store the OwnerAuth password, as long as the OwnerAuth is available on the local machine.</span></span>

<span data-ttu-id="0076d-126">Um MBAM zu aktivieren und dann TPM-OwnerAuth-Kennwörter zu speichern, müssen Sie diese Gruppenrichtlinieneinstellungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0076d-126">To enable MBAM to escrow and then store TPM OwnerAuth passwords, you must configure these Group Policy settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0076d-127">Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="0076d-127">Group Policy Setting</span></span></th>
<th align="left"><span data-ttu-id="0076d-128">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="0076d-128">Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0076d-129">Aktivieren der TPM-Sicherung in Active Directory-Domänendiensten</span><span class="sxs-lookup"><span data-stu-id="0076d-129">Turn on TPM backup to Active Directory Domain Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="0076d-130">Deaktiviert oder nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="0076d-130">Disabled or Not Configured</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0076d-131">Konfigurieren der Ebene der TPM-Besitzer Autorisierungsinformationen, die für das Betriebssystem verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="0076d-131">Configure the level of TPM owner authorization information available to the operating system</span></span></p></td>
<td align="left"><p><span data-ttu-id="0076d-132">Delegiert/keine oder nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="0076d-132">Delegated/None or Not Configured</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0076d-133">Der Speicherort dieser Gruppenrichtlinieneinstellungen ist **Computer Configuration** &gt; **Administrative Templates** &gt; **System** &gt; **Trusted Platform Module Services**.</span><span class="sxs-lookup"><span data-stu-id="0076d-133">The location of these Group Policy settings is **Computer Configuration** &gt; **Administrative Templates** &gt; **System** &gt; **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="0076d-134">**Hinweis**  Windows entfernt die OwnerAuth lokal, nachdem MBAM diese Einstellungen erfolgreich durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="0076d-134">**Note** Windows removes the OwnerAuth locally after MBAM successfully escrows it with these settings.</span></span>

 

### <span data-ttu-id="0076d-135">Treuhandservice für TPM-OwnerAuth in Windows 7</span><span class="sxs-lookup"><span data-stu-id="0076d-135">Escrowing TPM OwnerAuth in Windows 7</span></span>

<span data-ttu-id="0076d-136">In Windows 7 muss MBAM das TPM besitzen, damit TPM-OwnerAuth-Informationen automatisch in der MBAM-Datenbank gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0076d-136">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="0076d-137">Wenn MBAM nicht über das TPM verfügt, müssen Sie die MBAM Active Directory (AD)-Daten Import-Cmdlets verwenden, um TPM-OwnerAuth aus Active Directory in die MBAM-Datenbank zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="0076d-137">If MBAM does not own the TPM, you must use the MBAM Active Directory (AD) Data Import cmdlets to copy TPM OwnerAuth from Active Directory into the MBAM database.</span></span>

### <span data-ttu-id="0076d-138">MBAM-Cmdlets für Active Directory-Daten Import</span><span class="sxs-lookup"><span data-stu-id="0076d-138">MBAM Active Directory Data Import cmdlets</span></span>

<span data-ttu-id="0076d-139">Mit den MBAM-Cmdlets für Active Directory-Daten Import können Sie Wiederherstellungsschlüssel Pakete und OwnerAuth-Kennwörter abrufen, die in Active Directory gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="0076d-139">The MBAM Active Directory Data Import cmdlets let you retrieve recovery key packages and OwnerAuth passwords that are stored in Active Directory.</span></span>

<span data-ttu-id="0076d-140">Der MBAM 2,5 SP1-Server wird mit vier PowerShell-Cmdlets ausgeliefert, die MBAM-Datenbanken mit den in Active Directory gespeicherten Informationen zur Volume-Wiederherstellung und dem TPM-Besitzer auffüllen.</span><span class="sxs-lookup"><span data-stu-id="0076d-140">The MBAM 2.5 SP1 server ships with four PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="0076d-141">Für Volume-Wiederherstellungsschlüssel und-Pakete:</span><span class="sxs-lookup"><span data-stu-id="0076d-141">For Volume Recovery keys and packages:</span></span>

-   <span data-ttu-id="0076d-142">Lesen-ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="0076d-142">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="0076d-143">Write-MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="0076d-143">Write-MbamRecoveryInformation</span></span>

<span data-ttu-id="0076d-144">Informationen zu TPM-Besitzern:</span><span class="sxs-lookup"><span data-stu-id="0076d-144">For TPM Owner Information:</span></span>

-   <span data-ttu-id="0076d-145">Lesen-ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="0076d-145">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="0076d-146">Write-MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="0076d-146">Write-MbamTpmInformation</span></span>

<span data-ttu-id="0076d-147">Zum Zuordnen von Benutzern zu Computern:</span><span class="sxs-lookup"><span data-stu-id="0076d-147">For Associating Users to Computers:</span></span>

-   <span data-ttu-id="0076d-148">Write-MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="0076d-148">Write-MbamComputerUser</span></span>

<span data-ttu-id="0076d-149">Die Read-AD \ \*-Cmdlets lesen Informationen aus Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0076d-149">The Read-AD\* cmdlets read information from Active Directory.</span></span> <span data-ttu-id="0076d-150">Die Write-mbam \ \*-Cmdlets schieben die Daten in die mbam-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="0076d-150">The Write-Mbam\* cmdlets push the data into the MBAM databases.</span></span> <span data-ttu-id="0076d-151">Detaillierte Informationen zu diesen Cmdlets, einschließlich Syntax, Parametern und Beispielen, finden Sie unter [Cmdlet-Referenz für Microsoft BitLocker-Verwaltung und-Überwachung 2,5](https://technet.microsoft.com/library/dn459018.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0076d-151">See [Cmdlet Reference for Microsoft Bitlocker Administration and Monitoring 2.5](https://technet.microsoft.com/library/dn459018.aspx) for detailed information about these cmdlets, including syntax, parameters, and examples.</span></span>

<span data-ttu-id="0076d-152">**Erstellen von Benutzer-zu-Computer-Zuordnungen:** Die MBAM Active Directory-Daten Import-Cmdlets sammeln Informationen aus Active Directory und fügen die Daten in die MBAM-Datenbank ein.</span><span class="sxs-lookup"><span data-stu-id="0076d-152">**Create user-to-computer associations:** The MBAM Active Directory Data Import cmdlets gather information from Active Directory and insert the data into MBAM database.</span></span> <span data-ttu-id="0076d-153">Sie ordnen Benutzer jedoch keinen Volumes zu.</span><span class="sxs-lookup"><span data-stu-id="0076d-153">However, they do not associate users to volumes.</span></span> <span data-ttu-id="0076d-154">Sie können das Add-ComputerUser.ps1 PowerShell-Skript herunterladen, um Benutzer-zu-Computer-Zuordnungen zu erstellen, die Benutzern den Zugriff auf einen Computer über die Verwaltungs-und Überwachungs Website oder über das Self-Service-Portal für die Wiederherstellung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0076d-154">You can download the Add-ComputerUser.ps1 PowerShell script to create user-to-machine associations, which let users regain access to a computer through the Administration and Monitoring Website or by using the Self-Service Portal for recovery.</span></span> <span data-ttu-id="0076d-155">Das Add-ComputerUser.ps1-Skript sammelt Daten aus dem Attribut **Managed by** in Active Directory (AD), dem Objektbesitzer in AD oder aus einer benutzerdefinierten CSV-Datei.</span><span class="sxs-lookup"><span data-stu-id="0076d-155">The Add-ComputerUser.ps1 script gathers data from the **Managed By** attribute in Active Directory (AD), the object owner in AD, or from a custom CSV file.</span></span> <span data-ttu-id="0076d-156">Das Skript fügt die erkannten Benutzer dann dem Pipelineobjekt für Wiederherstellungsinformationen hinzu, das an Write-MbamRecoveryInformation übergeben werden muss, um die Daten in die Wiederherstellungsdatenbank einzufügen.</span><span class="sxs-lookup"><span data-stu-id="0076d-156">The script then adds the discovered users to the recovery information pipeline object, which must be passed to Write-MbamRecoveryInformation to insert the data into the recovery database.</span></span>

<span data-ttu-id="0076d-157">Laden Sie das Add-ComputerUser.ps1 PowerShell-Skript aus dem [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=613122)herunter.</span><span class="sxs-lookup"><span data-stu-id="0076d-157">Download the Add-ComputerUser.ps1 PowerShell script from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=613122).</span></span>

<span data-ttu-id="0076d-158">Sie können **Hilfe Add-ComputerUser.ps1** angeben, um Hilfe zu dem Skript zu erhalten, einschließlich Beispiele für die Verwendung der Cmdlets und des Skripts.</span><span class="sxs-lookup"><span data-stu-id="0076d-158">You can specify **help Add-ComputerUser.ps1** to get help for the script, including examples of how to use the cmdlets and the script.</span></span>

<span data-ttu-id="0076d-159">Verwenden Sie das PowerShell-Cmdlet Write-MbamComputerUser, um Benutzer-zu-Computer-Zuordnungen zu erstellen, nachdem Sie den MBAM-Server installiert haben.</span><span class="sxs-lookup"><span data-stu-id="0076d-159">To create user-to-computer associations after you have installed the MBAM server, use the Write-MbamComputerUser PowerShell cmdlet.</span></span> <span data-ttu-id="0076d-160">Ähnlich wie beim Add-ComputerUser.ps1 PowerShell-Skript können Sie mit diesem Cmdlet Benutzer angeben, die das Self-Service-Portal verwenden können, um TPM-OwnerAuth-Informationen oder Kennwörter für die Volume-Wiederherstellung für den angegebenen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0076d-160">Similar to the Add-ComputerUser.ps1 PowerShell script, this cmdlet lets you specify users that can use the Self-Service Portal to get TPM OwnerAuth information or volume recovery passwords for the specified computer.</span></span>

<span data-ttu-id="0076d-161">**Hinweis**  Der MBAM-Agent überschreibt Benutzer-zu-Computer-Zuordnungen, wenn dieser Computer mit der Berichterstellung an den Server beginnt.</span><span class="sxs-lookup"><span data-stu-id="0076d-161">**Note** The MBAM agent will override user-to-computer associations when that computer begins reporting up to the server.</span></span>

 

<span data-ttu-id="0076d-162">**Voraussetzungen:** Die "Read-AD \ \*"-Cmdlets können Informationen nur von anzeigen abrufen, wenn Sie entweder als hoch privilegiertes Benutzerkonto ausgeführt werden, beispielsweise als Domänen Administrator, oder als Konto in einer benutzerdefinierten Sicherheitsgruppe ausgeführt werden, die Lesezugriff auf die Informationen gewährt (empfohlen).</span><span class="sxs-lookup"><span data-stu-id="0076d-162">**Prerequisites:** The Read-AD\* cmdlets can retrieve information from AD only if they are either run as a highly privileged user account, such as a Domain Administrator, or run as an account in a custom security group granted read access to the information (recommended).</span></span>

<span data-ttu-id="0076d-163">[Leitfaden zur BitLocker-Laufwerkverschlüsselung: das Wiederherstellen verschlüsselter Volumes mit AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) bietet Details zum Erstellen einer benutzerdefinierten Sicherheitsgruppe (oder mehrerer Gruppen) mit Lesezugriff auf die anzeigen Informationen.</span><span class="sxs-lookup"><span data-stu-id="0076d-163">[BitLocker Drive Encryption Operations Guide: Recovering Encrypted Volumes with AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) provides details about creating a custom security group (or multiple groups) with read access to the AD information.</span></span>

<span data-ttu-id="0076d-164">**MBAM Recovery-und Hardware-Webdienst-Schreibberechtigungen:** Die Cmdlets Write-mbam \ \* akzeptieren die URL des mbam-Wiederherstellungs-und-Hardware Diensts, der zum Veröffentlichen der Wiederherstellungs-oder TPM-Informationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0076d-164">**MBAM Recovery and Hardware Web Service Write Permissions:** The Write-Mbam\* cmdlets accept the URL of the MBAM Recovery and Hardware Service, used to publish the recovery or TPM information.</span></span> <span data-ttu-id="0076d-165">In der Regel kann nur ein Domänencomputer Dienstkonto mit dem MBAM-Wiederherstellungs-und-Hardware Dienst kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="0076d-165">Typically, only a domain computer service account can communicate with the MBAM Recovery and Hardware Service.</span></span> <span data-ttu-id="0076d-166">In MBAM 2,5 SP1 können Sie den MBAM-Wiederherstellungs-und-Hardware Dienst mit einer Sicherheitsgruppe namens DataMigrationAccessGroup konfigurieren, deren Mitglieder die Überprüfung des Domänencomputer Dienst-Kontos umgehen dürfen.</span><span class="sxs-lookup"><span data-stu-id="0076d-166">In MBAM 2.5 SP1, you can configure the MBAM Recovery and Hardware Service with a security group called DataMigrationAccessGroup whose members are allowed to bypass the domain computer service account check.</span></span> <span data-ttu-id="0076d-167">Die Cmdlets für Write-mbam \ \* müssen als Benutzer ausgeführt werden, die zu dieser konfigurierten Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="0076d-167">The Write-Mbam\* cmdlets must be run as a user belonging to this configured group.</span></span> <span data-ttu-id="0076d-168">(Alternativ können die Anmeldeinformationen eines einzelnen Benutzers in der konfigurierten Gruppe mithilfe des Parameters "– Credential" in den Cmdlets "Write-mbam \ \*" angegeben werden.)</span><span class="sxs-lookup"><span data-stu-id="0076d-168">(Alternatively, the credentials of an individual user in the configured group can be specified by using the –Credential parameter in the Write-Mbam\* cmdlets.)</span></span>

<span data-ttu-id="0076d-169">Sie können den MBAM-Wiederherstellungs-und-Hardware Dienst mit dem Namen dieser Sicherheitsgruppe auf eine der folgenden Arten konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="0076d-169">You can configure the MBAM Recovery and Hardware Service with the name of this security group in one of these ways:</span></span>

-   <span data-ttu-id="0076d-170">Geben Sie den Namen der Sicherheitsgruppe (oder einzelner) im Parameter-DataMigrationAccessGroup des PowerShell-Cmdlets Enable-MbamWebApplication – agentservice an.</span><span class="sxs-lookup"><span data-stu-id="0076d-170">Provide the name of the security group (or individual) in the -DataMigrationAccessGroup parameter of the Enable-MbamWebApplication –AgentService Powershell cmdlet.</span></span>

-   <span data-ttu-id="0076d-171">Konfigurieren Sie die Gruppe, nachdem der MBAM-Wiederherstellungs-und-Hardware Dienst installiert wurde, indem Sie die web.config-Datei im &lt; Inetpub &gt; \\Microsoft BitLocker Management Solution\\Recovery-und Hardware Service\\-Ordner bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="0076d-171">Configure the group after the MBAM Recovery and Hardware Service has been installed by editing the web.config file in the &lt;inetpub&gt;\\Microsoft Bitlocker Management Solution\\Recovery and Hardware Service\\ folder.</span></span>

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    <span data-ttu-id="0076d-172">wobei &lt; GroupName durch &gt; die Domäne und den Gruppennamen (oder den einzelnen Benutzer) ersetzt wird, der verwendet wird, um die Datenmigration aus Active Directory zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0076d-172">where &lt;groupName&gt; is replaced with the domain and the group name (or the individual user) that will be used to allow data migration from Active Directory.</span></span>

-   <span data-ttu-id="0076d-173">Verwenden Sie den Konfigurations-Editor in IIS-Manager, um diesen appSetting zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="0076d-173">Use the Configuration Editor in IIS Manager to edit this appSetting.</span></span>

<span data-ttu-id="0076d-174">Im folgenden Beispiel wird der Befehl, wenn er als Mitglied der Gruppe "ADRecoveryInformation" und "Benutzer der Daten Migration" ausgeführt wird, die Datenträger Wiederherstellungsinformationen von Computern in der Organisationseinheit der Arbeitsstationen in der contoso.com-Domäne abrufen und mithilfe des MBAM-Wiederherstellungs-und-Hardware Diensts, der auf dem mbam.contoso.com-Server ausgeführt wird, in MBAM schreiben.</span><span class="sxs-lookup"><span data-stu-id="0076d-174">In the following example, the command, when run as a member of both the ADRecoveryInformation group and the Data Migration Users group, will pull the volume recovery information from computers in the WORKSTATIONS organizational unit (OU) in the contoso.com domain and write them to MBAM by using the MBAM Recovery and Hardware Service running on the mbam.contoso.com server.</span></span>

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

<span data-ttu-id="0076d-175">**Read-AD \ \* Cmdlets** akzeptieren den Namen oder die IP-Adresse eines Active Directory-Hostservers, um nach Wiederherstellungs-oder TPM-Informationen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="0076d-175">**Read-AD\* cmdlets** accept the name or IP address of an Active Directory hosting server machine to query for recovery or TPM information.</span></span> <span data-ttu-id="0076d-176">Wir empfehlen, die Distinguished Names der AD-Container anzugeben, in denen sich das Computerobjekt befindet, als den Wert des SearchBase-Parameters.</span><span class="sxs-lookup"><span data-stu-id="0076d-176">We recommend providing the distinguished names of the AD containers in which the computer object resides as the value of the SearchBase parameter.</span></span> <span data-ttu-id="0076d-177">Wenn Computer über mehrere OUs gespeichert werden, können die Cmdlets Pipelineeingaben akzeptieren, damit Sie einmal für jeden Container ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0076d-177">If computers are stored across several OUs, the cmdlets can accept pipeline input to run once for each container.</span></span> <span data-ttu-id="0076d-178">Der Distinguished Name eines anzeigen Containers sieht ähnlich wie ou = machines, DC = contoso, DC = com aus.</span><span class="sxs-lookup"><span data-stu-id="0076d-178">The distinguished name of an AD container will look similar to OU=Machines,DC=contoso,DC=com.</span></span> <span data-ttu-id="0076d-179">Das Durchführen einer Suche, die auf bestimmte Container ausgerichtet ist, bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="0076d-179">Performing a search targeted to specific containers provides the following benefits:</span></span>

-   <span data-ttu-id="0076d-180">Verringert das Risiko von Timeout beim Abfragen eines umfangreichen AD-Datasets für Computerobjekte.</span><span class="sxs-lookup"><span data-stu-id="0076d-180">Reduces the risk of timeout while querying a large AD dataset for computer objects.</span></span>

-   <span data-ttu-id="0076d-181">Sie können OUs mit Rechenzentrums Servern oder anderen Computerklassen auslassen, für die die Sicherung möglicherweise nicht erwünscht oder erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0076d-181">Can omit OUs containing datacenter servers or other classes of computers for which the backup might not be desired or necessary.</span></span>

<span data-ttu-id="0076d-182">Eine weitere Möglichkeit besteht darin, das-recurse-Flag mit oder ohne den optionalen SearchBase bereitzustellen, um in allen Containern unter dem angegebenen SearchBase oder der gesamten Domäne nach Computerobjekten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="0076d-182">Another option is to provide the –Recurse flag with or without the optional SearchBase to search for computer objects across all containers under the specified SearchBase or the entire domain respectively.</span></span> <span data-ttu-id="0076d-183">Wenn Sie das-recurse-Flag verwenden, können Sie auch den-MaxPageSize-Parameter verwenden, um die Menge an lokalem und Remotespeicher zu steuern, die zum Service der Abfrage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0076d-183">When you use the -Recurse flag, you can also use the -MaxPageSize parameter to control the amount of local and remote memory required to service the query.</span></span>

<span data-ttu-id="0076d-184">Diese Cmdlets schreiben in die Pipelineobjekte des Typs PsObject.</span><span class="sxs-lookup"><span data-stu-id="0076d-184">These cmdlets write to the pipeline objects of type PsObject.</span></span> <span data-ttu-id="0076d-185">Jede PsObject-Instanz enthält einen einzelnen Volume-Wiederherstellungsschlüssel oder eine TPM-Besitzer Zeichenfolge mit dem zugehörigen Computernamen, Zeitstempel und anderen Informationen, die für die Veröffentlichung im MBAM-Datenspeicher erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0076d-185">Each PsObject instance contains a single volume recovery key or TPM owner string with its associated computer name, timestamp, and other information required to publish it to the MBAM data store.</span></span>

<span data-ttu-id="0076d-186">**Write-mbam \ \* Cmdlets** akzeptieren die Parameterwerte für Wiederherstellungsinformationen aus der Pipeline nach dem Eigenschaftennamen.</span><span class="sxs-lookup"><span data-stu-id="0076d-186">**Write-Mbam\* cmdlets** accept recovery information parameter values from the pipeline by property name.</span></span> <span data-ttu-id="0076d-187">Auf diese Weise können die Write-mbam \ \*-Cmdlets die Pipelineausgabe der Read-AD \ \*-Cmdlets akzeptieren (beispielsweise Read-ADRecoveryInformation – Server Contoso.com – Rekursion | Write-MbamRecoveryInformation – RecoveryServiceEndpoint mbam.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="0076d-187">This allows the Write-Mbam\* cmdlets to accept the pipeline output of the Read-AD\* cmdlets (for example, Read-ADRecoveryInformation –Server contoso.com –Recurse | Write-MbamRecoveryInformation –RecoveryServiceEndpoint mbam.contoso.com).</span></span>

<span data-ttu-id="0076d-188">Die \*\*Cmdlets Write-mbam \ \*\*\* enthalten optionale Parameter, die Optionen für Fehlertoleranz, ausführliche Protokollierung und Einstellungen für WhatIf und Confirm bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0076d-188">The **Write-Mbam\* cmdlets** include optional parameters that provide options for fault tolerance, verbose logging, and preferences for WhatIf and Confirm.</span></span>

<span data-ttu-id="0076d-189">Die \*\*Cmdlets für Write-mbam \ \*\*\* umfassen auch einen optionalen *Zeit* Parameter, dessen Wert ein **DateTime** -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="0076d-189">The **Write-Mbam\* cmdlets** also include an optional *Time* parameter whose value is a **DateTime** object.</span></span> <span data-ttu-id="0076d-190">Dieses Objekt enthält ein *Kind* -Attribut, das auf, oder festgesetzt werden kann `Local` `UTC` `Unspecified` .</span><span class="sxs-lookup"><span data-stu-id="0076d-190">This object includes a *Kind* attribute that can be set to `Local`, `UTC`, or `Unspecified`.</span></span> <span data-ttu-id="0076d-191">Wenn der *Zeit* Parameter aus den aus Active Directory übernommenen Daten ausgefüllt wird, wird die Uhrzeit in UTC konvertiert, und das Attribut *Art* wird automatisch auf gesetzt `UTC` .</span><span class="sxs-lookup"><span data-stu-id="0076d-191">When the *Time* parameter is populated from data taken from the Active Directory, the time is converted to UTC and this *Kind* attribute is set automatically to `UTC`.</span></span> <span data-ttu-id="0076d-192">Wenn Sie jedoch den *Zeit* Parameter mit einer anderen Quelle, wie etwa einer Textdatei, füllen, müssen Sie das *Kind* -Attribut explizit auf seinen geeigneten Wert setzen.</span><span class="sxs-lookup"><span data-stu-id="0076d-192">However, when populating the *Time* parameter using another source, such as a text file, you must explicitly set the *Kind* attribute to its appropriate value.</span></span>

<span data-ttu-id="0076d-193">**Hinweis**  Die "Read-AD \ \*"-Cmdlets können nicht die Benutzerkonten ermitteln, die die Computer Benutzer darstellen.</span><span class="sxs-lookup"><span data-stu-id="0076d-193">**Note** The Read-AD\* cmdlets do not have the ability to discover the user accounts that represent the computer users.</span></span> <span data-ttu-id="0076d-194">Benutzerkonten Zuordnungen sind für Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="0076d-194">User account associations are needed for the following:</span></span>

-   <span data-ttu-id="0076d-195">Benutzer zum Wiederherstellen von Volume-Kennwörtern/-Paketen mithilfe des Self-Service-Portals</span><span class="sxs-lookup"><span data-stu-id="0076d-195">Users to recover volume passwords/packages by using the Self-Service portal</span></span>

-   <span data-ttu-id="0076d-196">Benutzer, die sich nicht in der Sicherheitsgruppe "Erweiterter Helpdesk-Benutzer" von MBAM befinden, wie Sie während der Installation definiert sind, wiederherstellen im Auftrag anderer Benutzer</span><span class="sxs-lookup"><span data-stu-id="0076d-196">Users who are not in the MBAM Advanced Helpdesk Users security group as defined during installation, recovering on behalf of other users</span></span>

 

## <a href="" id="bkmk-autounlock"></a><span data-ttu-id="0076d-197">Konfigurieren von MBAM so, dass das TPM nach einer Sperrung automatisch freigegeben wird</span><span class="sxs-lookup"><span data-stu-id="0076d-197">Configure MBAM to automatically unlock the TPM after a lockout</span></span>


<span data-ttu-id="0076d-198">Sie können MBAM 2,5 SP1 so konfigurieren, dass das TPM im Falle einer Sperrung automatisch freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0076d-198">You can configure MBAM 2.5 SP1 to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="0076d-199">Wenn TPM-Sperrungs-Auto-Reset aktiviert ist, kann MBAM feststellen, dass ein Benutzer gesperrt ist, und das OwnerAuth-Kennwort aus der MBAM-Datenbank abrufen, um das TPM automatisch für den Benutzer zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="0076d-199">If TPM lockout auto reset is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span> <span data-ttu-id="0076d-200">Das automatische Zurücksetzen der TPM-Sperrung steht nur zur Verfügung, wenn der Betriebssystem Wiederherstellungsschlüssel für diesen Computer über das Self-Service-Portal oder die Website Verwaltung und Überwachung abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="0076d-200">TPM lockout auto reset is only available if the OS recovery key for that computer was retrieved by using the Self Service Portal or the Administration and Monitoring Website.</span></span>

<span data-ttu-id="0076d-201">**Wichtig**  Zum Aktivieren der automatischen Zurücksetzung des TPM-Lockouts müssen Sie dieses Feature sowohl auf der Serverseite als auch in den Gruppenrichtlinien auf der Clientseite konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0076d-201">**Important** To enable TPM lockout auto reset, you must configure this feature on both the server side and in Group Policy on the client side.</span></span>

 

-   <span data-ttu-id="0076d-202">Wenn Sie das automatische Zurücksetzen der TPM-Sperrung auf der Clientseite aktivieren möchten, konfigurieren Sie die Gruppenrichtlinieneinstellung "Automatisches Zurücksetzen der TPM-Sperrung" unter **Computer Konfiguration** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM** - &gt; **Clientverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0076d-202">To enable TPM lockout auto reset on the client side, configure the Group Policy setting "Configure TPM lockout auto reset" located at **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM** &gt; **Client Management**.</span></span>

-   <span data-ttu-id="0076d-203">Wenn Sie das automatische Zurücksetzen der TPM-Sperrung auf der Serverseite aktivieren möchten, können Sie im MBAM-Serverkonfigurations-Assistenten während des Setups die Option "Automatisches Zurücksetzen von TPM-Sperrung aktivieren" aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0076d-203">To enable TPM lockout auto reset on the server side, you can check "Enable TPM lockout auto reset" in the MBAM Server Configuration wizard during setup.</span></span>

    <span data-ttu-id="0076d-204">Sie können das automatische Zurücksetzen der TPM-Sperrung in PowerShell auch aktivieren, indem Sie beim Aktivieren der Agentendienst-Webkomponente den Schalter "-TPM-Sperrungs-Auto-Reset" angeben.</span><span class="sxs-lookup"><span data-stu-id="0076d-204">You can also enable TPM lockout auto reset in PowerShell by specifying the "-TPM lockout auto reset" switch while enabling the agent service web component.</span></span>

<span data-ttu-id="0076d-205">Nachdem ein Benutzer den BitLocker-Wiederherstellungsschlüssel eingegeben hat, den er über das Self-Service-Portal oder die Website Verwaltung und Überwachung erhalten hat, ermittelt der MBAM-Agent, ob das TPM gesperrt ist. Wenn Sie gesperrt ist, wird versucht, die TPM-OwnerAuth für den Computer aus der MBAM-Datenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0076d-205">After a user enters the BitLocker recovery key they obtained from the Self Service Portal or the Administration and Monitoring Website, the MBAM agent will determine if the TPM is locked out. If it is locked out, it will attempt to retrieve the TPM OwnerAuth for the computer from the MBAM database.</span></span> <span data-ttu-id="0076d-206">Wenn die TPM-OwnerAuth erfolgreich abgerufen wurde, wird Sie zum Entsperren des TPMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="0076d-206">If the TPM OwnerAuth is successfully retrieved, it will be used to unlock the TPM.</span></span> <span data-ttu-id="0076d-207">Wenn Sie das TPM entsperren, ist das TPM voll funktionsfähig, und der Benutzer wird nicht gezwungen, das Wiederherstellungskennwort bei nachfolgenden Neustarts aus einer TPM-Sperrung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="0076d-207">Unlocking the TPM makes the TPM fully functional and the user will not be forced to enter the recovery password during subsequent reboots from a TPM lockout.</span></span>

<span data-ttu-id="0076d-208">Das automatische Zurücksetzen von TPM-Sperrungen ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0076d-208">TPM lockout auto reset is disabled by default.</span></span>

<span data-ttu-id="0076d-209">**Hinweis**  Das automatische Zurücksetzen der TPM-Sperrung wird nur auf Computern unterstützt, auf denen TPM-Version 1,2 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0076d-209">**Note** TPM lockout auto reset is only supported on computers running TPM version 1.2.</span></span> <span data-ttu-id="0076d-210">TPM 2,0 bietet integrierte Funktionen zum automatischen Zurücksetzen von Sperren.</span><span class="sxs-lookup"><span data-stu-id="0076d-210">TPM 2.0 provides built-in lockout auto reset functionality.</span></span>

 

<span data-ttu-id="0076d-211">**Der Wiederherstellungs Überwachungsbericht** enthält Ereignisse im Zusammenhang mit dem automatischen Zurücksetzen der TPM-Sperrung.</span><span class="sxs-lookup"><span data-stu-id="0076d-211">**The Recovery Audit Report** includes events related to TPM lockout auto reset.</span></span> <span data-ttu-id="0076d-212">Wenn vom MBAM-Client eine Anforderung zum Abrufen eines TPM-OwnerAuth-Kennworts getroffen wird, wird ein Ereignis protokolliert, um die Wiederherstellung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0076d-212">If a request is made from the MBAM client to retrieve a TPM OwnerAuth password, an event is logged to indicate recovery.</span></span> <span data-ttu-id="0076d-213">Überwachungseinträge sind die folgenden Ereignisse:</span><span class="sxs-lookup"><span data-stu-id="0076d-213">Audit entries will include the following events:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0076d-214">Eintrag</span><span class="sxs-lookup"><span data-stu-id="0076d-214">Entry</span></span></th>
<th align="left"><span data-ttu-id="0076d-215">Wert</span><span class="sxs-lookup"><span data-stu-id="0076d-215">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0076d-216">Überwachungs Anforderungsquelle</span><span class="sxs-lookup"><span data-stu-id="0076d-216">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="0076d-217">Agent-TPM-Sperrung</span><span class="sxs-lookup"><span data-stu-id="0076d-217">Agent TPM unlock</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0076d-218">Schlüsseltyp</span><span class="sxs-lookup"><span data-stu-id="0076d-218">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="0076d-219">TPM-Kenn Wort Hash</span><span class="sxs-lookup"><span data-stu-id="0076d-219">TPM Password Hash</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0076d-220">Beschreibung des Grunds</span><span class="sxs-lookup"><span data-stu-id="0076d-220">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="0076d-221">TPM-Reset</span><span class="sxs-lookup"><span data-stu-id="0076d-221">TPM Reset</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a><span data-ttu-id="0076d-222">Sichere Verbindungen mit SQL Server</span><span class="sxs-lookup"><span data-stu-id="0076d-222">Secure connections to SQL Server</span></span>


<span data-ttu-id="0076d-223">In MBAM kommuniziert SQL Server mit SQL Server Reporting Services und mit den Webdiensten für die Websiteverwaltung und Überwachung sowie Self-Service-Portal.</span><span class="sxs-lookup"><span data-stu-id="0076d-223">In MBAM, SQL Server communicates with SQL Server Reporting Services and with the web services for the Administration and Monitoring Website and Self-Service Portal.</span></span> <span data-ttu-id="0076d-224">Wir empfehlen, die Kommunikation mit SQL Server zu sichern.</span><span class="sxs-lookup"><span data-stu-id="0076d-224">We recommend that you secure the communication with SQL Server.</span></span> <span data-ttu-id="0076d-225">Weitere Informationen finden Sie unter [Verschlüsseln von Verbindungen mit SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span><span class="sxs-lookup"><span data-stu-id="0076d-225">For more information, see [Encrypting Connections to SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span></span>

<span data-ttu-id="0076d-226">Weitere Informationen zum Sichern der MBAM-Websites finden Sie unter [Planen der Sicherung der MBAM-Websites](planning-how-to-secure-the-mbam-websites.md).</span><span class="sxs-lookup"><span data-stu-id="0076d-226">For more information about securing the MBAM websites, see [Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md).</span></span>

## <a href="" id="bkmk-accts-groups"></a><span data-ttu-id="0076d-227">Erstellen von Konten und Gruppen</span><span class="sxs-lookup"><span data-stu-id="0076d-227">Create accounts and groups</span></span>


<span data-ttu-id="0076d-228">Die bewährte Methode zum Verwalten von Benutzerkonten ist das Erstellen globaler Domänengruppen und das Hinzufügen von Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="0076d-228">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="0076d-229">Eine Beschreibung der empfohlenen Konten und Gruppen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="0076d-229">For a description of the recommended accounts and groups, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

## <a href="" id="bkmk-logfiles"></a><span data-ttu-id="0076d-230">Verwenden von MBAM-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="0076d-230">Use MBAM log files</span></span>


<span data-ttu-id="0076d-231">In diesem Abschnitt werden die MBAM Server-und MBAM-Client Protokolldateien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0076d-231">This section describes the MBAM Server and MBAM Client log files.</span></span>

**<span data-ttu-id="0076d-232">MBAM Server Setup-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="0076d-232">MBAM Server Setup log files</span></span>**

<span data-ttu-id="0076d-233">Die **MBAMServerSetup.exe** -Datei generiert die folgenden Protokolldateien im Ordner " **% Temp%** " des Benutzers während der MBAM-Installation:</span><span class="sxs-lookup"><span data-stu-id="0076d-233">The **MBAMServerSetup.exe** file generates the following log files in the user’s **%temp%** folder during the MBAM installation:</span></span>

-   **<span data-ttu-id="0076d-234">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 Numbers &gt; . log</span><span class="sxs-lookup"><span data-stu-id="0076d-234">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14 numbers&gt;.log</span></span>**

    <span data-ttu-id="0076d-235">Protokolliert die Aktionen, die während des MBAM-Setups und der MBAM Server-Feature-Konfiguration ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="0076d-235">Logs the actions taken during the MBAM setup and the MBAM Server feature configuration.</span></span>

-   **<span data-ttu-id="0076d-236">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _Numbers &gt;\_0\_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="0076d-236">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14\_numbers&gt;\_0\_MBAMServer.msi.log</span></span>**

    <span data-ttu-id="0076d-237">Protokolliert zusätzliche während der Installation durchgeführte Aktionen.</span><span class="sxs-lookup"><span data-stu-id="0076d-237">Logs additional action taken during installation.</span></span>

**<span data-ttu-id="0076d-238">MBAM Server-Konfigurationsprotokoll Dateien</span><span class="sxs-lookup"><span data-stu-id="0076d-238">MBAM Server Configuration log files</span></span>**

-   **<span data-ttu-id="0076d-239">Anwendungen und Dienstprotokolle/Microsoft Windows/MBAM-Setup</span><span class="sxs-lookup"><span data-stu-id="0076d-239">Applications and Services Logs/Microsoft Windows/MBAM-Setup</span></span>**

    <span data-ttu-id="0076d-240">Protokolliert die Fehler, die auftreten, wenn Sie Windows PowerShell-Cmdlets verwenden, oder den MBAM-Serverkonfigurations-Assistenten, um die MBAM-Server Features zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0076d-240">Logs the errors that occur when you are using Windows Powershell cmdlets or the MBAM Server Configuration wizard to configure the MBAM Server features.</span></span>

**<span data-ttu-id="0076d-241">MBAM-Client Setup-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="0076d-241">MBAM Client setup log files</span></span>**

-   **<span data-ttu-id="0076d-242">MSI &lt; fünf zufällige Zeichen &gt; . log</span><span class="sxs-lookup"><span data-stu-id="0076d-242">MSI&lt;five random characters&gt;.log</span></span>**

    <span data-ttu-id="0076d-243">Protokolliert die während der MBAM-Client Installation ausgeführten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="0076d-243">Logs the actions taken during the MBAM Client installation.</span></span>

**<span data-ttu-id="0076d-244">MBAM-Web-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="0076d-244">MBAM-Web log files</span></span>**

-   <span data-ttu-id="0076d-245">Zeigt Aktivitäten aus den Webportalen und-Diensten an.</span><span class="sxs-lookup"><span data-stu-id="0076d-245">Shows activity from the web portals and services.</span></span>

## <a href="" id="bkmk-tde"></a><span data-ttu-id="0076d-246">Überlegungen zu MBAM Database DSA</span><span class="sxs-lookup"><span data-stu-id="0076d-246">Review MBAM database TDE considerations</span></span>


<span data-ttu-id="0076d-247">Das in SQL Server verfügbare Feature "transparente Datenverschlüsselung (DSA)" ist eine optionale Installation für die Datenbankinstanzen, in denen die MBAM-Datenbankfeatures gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="0076d-247">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host the MBAM database features.</span></span>

<span data-ttu-id="0076d-248">Mit DSA können Sie die vollständige Verschlüsselung auf Datenbankebene in Echtzeit durchführen.</span><span class="sxs-lookup"><span data-stu-id="0076d-248">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="0076d-249">DSA ist die optimale Lösung für die Massenverschlüsselung, um behördliche Compliance-oder Unternehmensdaten Sicherheitsstandards zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0076d-249">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="0076d-250">DSA funktioniert auf der Dateiebene, die zwei Windows-Features ähnelt: EFS (Encrypting File System) und BitLocker-Laufwerkverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="0076d-250">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption.</span></span> <span data-ttu-id="0076d-251">Beide Funktionen verschlüsseln auch Daten auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="0076d-251">Both features also encrypt data on the hard drive.</span></span> <span data-ttu-id="0076d-252">DSA ersetzt nicht die Verschlüsselung auf Zellenebene, EFS oder BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0076d-252">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="0076d-253">Wenn DSA für eine Datenbank aktiviert ist, werden alle Sicherungen verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="0076d-253">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="0076d-254">Daher muss besonders darauf geachtet werden, dass das zum Schützen des Datenbank-Verschlüsselungsschlüssels verwendete Zertifikat mit der Datenbanksicherung gesichert und verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="0076d-254">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="0076d-255">Wenn dieses Zertifikat (oder Zertifikate) verloren geht, sind die Daten nicht lesbar.</span><span class="sxs-lookup"><span data-stu-id="0076d-255">If this certificate (or certificates) is lost, the data will be unreadable.</span></span>

<span data-ttu-id="0076d-256">Sichern Sie das Zertifikat mit der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0076d-256">Back up the certificate with the database.</span></span> <span data-ttu-id="0076d-257">Für jede Zertifikat Sicherung sollten zwei Dateien vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0076d-257">Each certificate backup should have two files.</span></span> <span data-ttu-id="0076d-258">Beide Dateien sollten archiviert werden.</span><span class="sxs-lookup"><span data-stu-id="0076d-258">Both of these files should be archived.</span></span> <span data-ttu-id="0076d-259">Idealerweise sollten Sie für die Sicherheit separat von der Datenbanksicherungsdatei gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="0076d-259">Ideally for security, they should be backed up separately from the database backup file.</span></span> <span data-ttu-id="0076d-260">Alternativ können Sie die erweiterbare Schlüssel Verwaltungsfunktion (Extensible Key Management, erweiterbare Schlüsselverwaltung) für die Speicherung und Wartung von Schlüsseln verwenden, die für DSA verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0076d-260">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys that are used for TDE.</span></span>

<span data-ttu-id="0076d-261">Ein Beispiel für die Aktivierung von DSA für MBAM-Datenbankinstanzen finden Sie unter [Grundlegendes zur transparenten Datenverschlüsselung (DSA)](https://technet.microsoft.com/library/bb934049.aspx).</span><span class="sxs-lookup"><span data-stu-id="0076d-261">For an example of how to enable TDE for MBAM database instances, see [Understanding Transparent Data Encryption (TDE)](https://technet.microsoft.com/library/bb934049.aspx).</span></span>

## <a href="" id="bkmk-general-security"></a><span data-ttu-id="0076d-262">Grundlegendes zu allgemeinen Sicherheitsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="0076d-262">Understand general security considerations</span></span>


**<span data-ttu-id="0076d-263">Grundlegendes zu den Sicherheitsrisiken</span><span class="sxs-lookup"><span data-stu-id="0076d-263">Understand the security risks.</span></span>** <span data-ttu-id="0076d-264">Das schwerwiegendste Risiko bei der Verwendung der Microsoft BitLocker-Verwaltung und-Überwachung besteht darin, dass die Funktionalität von einem nicht autorisierten Benutzer beeinträchtigt werden kann, der dann die BitLocker-Laufwerkverschlüsselung neu konfigurieren und BitLocker-Verschlüsselungsschlüssel Daten auf MBAM-Clients erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="0076d-264">The most serious risk when you use Microsoft BitLocker Administration and Monitoring is that its functionality could be compromised by an unauthorized user who could then reconfigure BitLocker Drive Encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="0076d-265">Der Verlust von MBAM-Funktionen für kurze Zeit aufgrund eines Denial-of-Service-Angriffs hat jedoch im Allgemeinen keine katastrophalen Auswirkungen, wie beispielsweise das verlieren von e-Mail-oder Netzwerkkommunikation oder der Stromversorgung.</span><span class="sxs-lookup"><span data-stu-id="0076d-265">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, losing e-mail or network communications, or power.</span></span>

<span data-ttu-id="0076d-266">**Physisches sichern ihrer Computer**.</span><span class="sxs-lookup"><span data-stu-id="0076d-266">**Physically secure your computers**.</span></span> <span data-ttu-id="0076d-267">Es gibt keine Sicherheit ohne physische Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="0076d-267">There is no security without physical security.</span></span> <span data-ttu-id="0076d-268">Ein Angreifer, der physischen Zugriff auf einen MBAM-Server erhält, kann ihn potenziell zum Angriff auf die gesamte Clientbasis verwenden.</span><span class="sxs-lookup"><span data-stu-id="0076d-268">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="0076d-269">Alle potenziellen körperlichen Angriffe müssen als Risiko behaftet und entsprechend verringert werden.</span><span class="sxs-lookup"><span data-stu-id="0076d-269">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="0076d-270">MBAM-Server sollten in einem sicheren Serverraum mit kontrolliertem Zugriff gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0076d-270">MBAM Servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="0076d-271">Sichern Sie diese Computer, wenn Administratoren physisch nicht anwesend sind, indem Sie das Betriebssystem sperren oder einen sicheren Bildschirmschoner verwenden.</span><span class="sxs-lookup"><span data-stu-id="0076d-271">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="0076d-272">**Wenden Sie die neuesten Sicherheitsupdates auf alle Computer an**.</span><span class="sxs-lookup"><span data-stu-id="0076d-272">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="0076d-273">Informieren Sie sich über neue Updates für Windows-Betriebssysteme, SQL Server und MBAM, indem Sie den Sicherheitsbenachrichtigungsdienst im [Security TechCenter](https://go.microsoft.com/fwlink/?LinkId=28819)abonnieren.</span><span class="sxs-lookup"><span data-stu-id="0076d-273">Stay informed about new updates for Windows operating systems, SQL Server, and MBAM by subscribing to the Security Notification service at the [Security TechCenter](https://go.microsoft.com/fwlink/?LinkId=28819).</span></span>

<span data-ttu-id="0076d-274">**Verwenden Sie sichere Kennwörter oder Passphrasen**.</span><span class="sxs-lookup"><span data-stu-id="0076d-274">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="0076d-275">Verwenden Sie immer sichere Kennwörter mit 15 oder mehr Zeichen für alle MBAM-Administratorkonten.</span><span class="sxs-lookup"><span data-stu-id="0076d-275">Always use strong passwords with 15 or more characters for all MBAM administrator accounts.</span></span> <span data-ttu-id="0076d-276">Verwenden Sie niemals leere Kennwörter.</span><span class="sxs-lookup"><span data-stu-id="0076d-276">Never use blank passwords.</span></span> <span data-ttu-id="0076d-277">Weitere Informationen zu Kenn Wort Konzepten finden Sie unter [Kennwortrichtlinien](https://technet.microsoft.com/library/hh994572.aspx).</span><span class="sxs-lookup"><span data-stu-id="0076d-277">For more information about password concepts, see [Password Policy](https://technet.microsoft.com/library/hh994572.aspx).</span></span>



## <span data-ttu-id="0076d-278">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0076d-278">Related topics</span></span>


[<span data-ttu-id="0076d-279">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0076d-279">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 
## <span data-ttu-id="0076d-280">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="0076d-280">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0076d-281">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="0076d-281">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="0076d-282">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="0076d-282">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





