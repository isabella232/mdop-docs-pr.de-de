---
title: Infos zu MBAM 2.5 SP1
description: Infos zu MBAM 2.5 SP1
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810162"
---
# <span data-ttu-id="2b204-103">Infos zu MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="2b204-103">About MBAM 2.5 SP1</span></span>


<span data-ttu-id="2b204-104">MBAM 2,5 SP1 bietet eine vereinfachte Verwaltungsoberfläche für die BitLocker-Laufwerkverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="2b204-104">MBAM 2.5 SP1 provides a simplified administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="2b204-105">BitLocker bietet erweiterten Schutz vor Datendiebstahl oder Datengefährdung für Computer, die verloren gehen oder gestohlen werden.</span><span class="sxs-lookup"><span data-stu-id="2b204-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="2b204-106">BitLocker verschlüsselt alle Daten, die auf dem Windows-Betriebssystem gespeichert sind, und Laufwerke und konfigurierte Datenlaufwerke.</span><span class="sxs-lookup"><span data-stu-id="2b204-106">BitLocker encrypts all data that is stored on the Windows operating system and drives and configured data drives.</span></span>

## <span data-ttu-id="2b204-107">Übersicht über MBAM</span><span class="sxs-lookup"><span data-stu-id="2b204-107">Overview of MBAM</span></span>


<span data-ttu-id="2b204-108">MBAM 2,5 SP1 bietet die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="2b204-108">MBAM 2.5 SP1 has the following features:</span></span>

-   <span data-ttu-id="2b204-109">Administratoren können die Verschlüsselung von Volumes auf Clientcomputern unternehmensweit automatisieren.</span><span class="sxs-lookup"><span data-stu-id="2b204-109">Enables administrators to automate the process of encrypting volumes on client computers across the enterprise.</span></span>

-   <span data-ttu-id="2b204-110">Sicherheitsbeauftragte können den Kompatibilitätszustand einzelner Computer oder sogar des ganzen Unternehmens schnell ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2b204-110">Enables security officers to quickly determine the compliance state of individual computers or even of the enterprise itself.</span></span>

-   <span data-ttu-id="2b204-111">Berichterstellung und Hardwareverwaltung können zentral mit Microsoft System Center Configuration Manager erfolgen.</span><span class="sxs-lookup"><span data-stu-id="2b204-111">Provides centralized reporting and hardware management with Microsoft System Center Configuration Manager.</span></span>

-   <span data-ttu-id="2b204-112">Verringert die Arbeitsbelastung des Helpdesks, um Endbenutzern die BitLocker-PIN-und Wiederherstellungsschlüssel Anforderungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2b204-112">Reduces the workload on the Help Desk to assist end users with BitLocker PIN and recovery key requests.</span></span>

-   <span data-ttu-id="2b204-113">Endbenutzer können verschlüsselte Geräte mithilfe des Self-Service-Portals eigenständig wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="2b204-113">Enables end users to recover encrypted devices independently by using the Self-Service Portal.</span></span>

-   <span data-ttu-id="2b204-114">Ermöglicht es Sicherheitsbeauftragten, den Zugriff auf die Wiederherstellung wichtiger Informationen einfach zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="2b204-114">Enables security officers to easily audit access to recover key information.</span></span>

-   <span data-ttu-id="2b204-115">Windows Enterprise-Benutzer können standortunabhängig arbeiten und sich dabei darauf verlassen, dass ihre Unternehmensdaten geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="2b204-115">Empowers Windows Enterprise users to continue working anywhere with the assurance that their corporate data is protected.</span></span>

<span data-ttu-id="2b204-116">MBAM erzwingt die BitLocker-Verschlüsselungsrichtlinien Optionen, die Sie für Ihr Unternehmen festzulegen, überwacht die Kompatibilität von Clientcomputern mit diesen Richtlinien und meldet den Verschlüsselungsstatus der Computer des Unternehmens und der einzelnen Personen.</span><span class="sxs-lookup"><span data-stu-id="2b204-116">MBAM enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of the enterprise’s and individual’s computers.</span></span> <span data-ttu-id="2b204-117">Darüber hinaus können Sie mit MBAM auf die Wiederherstellungsschlüssel Informationen zugreifen, wenn Benutzer Ihre PIN oder Ihr Kennwort vergessen oder wenn sich die BIOS-oder Startdatensätze ändern.</span><span class="sxs-lookup"><span data-stu-id="2b204-117">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot records change.</span></span>

<span data-ttu-id="2b204-118">Die folgenden Gruppen sind möglicherweise an der Verwendung von MBAM für die Verwaltung von BitLocker interessiert:</span><span class="sxs-lookup"><span data-stu-id="2b204-118">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="2b204-119">Administratoren, IT-Sicherheitsexperten und Compliance Officer, die dafür verantwortlich sind, sicherzustellen, dass vertrauliche Daten nicht ohne Autorisierung freigegeben werden</span><span class="sxs-lookup"><span data-stu-id="2b204-119">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="2b204-120">Administratoren, die für die Computersicherheit in Remote-oder Zweigstellen zuständig sind</span><span class="sxs-lookup"><span data-stu-id="2b204-120">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="2b204-121">Administratoren, die für Clientcomputer mit Windows verantwortlich sind</span><span class="sxs-lookup"><span data-stu-id="2b204-121">Administrators who are responsible for client computers that are running Windows</span></span>

<span data-ttu-id="2b204-122">**Hinweis**  BitLocker wird in dieser MBAM-Dokumentation nicht ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="2b204-122">**Note** BitLocker is not explained in detail in this MBAM documentation.</span></span> <span data-ttu-id="2b204-123">Weitere Informationen finden Sie unter [Übersicht über die BitLocker-Laufwerkverschlüsselung](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span><span class="sxs-lookup"><span data-stu-id="2b204-123">For more information, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a><span data-ttu-id="2b204-124">Neuerungen in MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="2b204-124">What’s new in MBAM 2.5 SP1</span></span>


<span data-ttu-id="2b204-125">In diesem Abschnitt werden die neuen Features in MBAM 2,5 SP1 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2b204-125">This section describes the new features in MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="2b204-126">Neu unterstützte Sprachen für den MBAM 2,5 SP1-Client</span><span class="sxs-lookup"><span data-stu-id="2b204-126">Newly Supported Languages for the MBAM 2.5 SP1 Client</span></span>

<span data-ttu-id="2b204-127">Die folgenden zusätzlichen Sprachen werden jetzt in MBAM 2,5 SP1 nur für den MBAM-Client unterstützt, einschließlich des Self-Service-Portals:</span><span class="sxs-lookup"><span data-stu-id="2b204-127">The following additional languages are now supported in MBAM 2.5 SP1 for the MBAM Client only, including the Self-Service Portal:</span></span>

<span data-ttu-id="2b204-128">Tschechische Republik (Tschechien) cs-cz</span><span class="sxs-lookup"><span data-stu-id="2b204-128">Czech (Czech Republic) cs-CZ</span></span>

<span data-ttu-id="2b204-129">Dänisch (Dänemark) da-DK</span><span class="sxs-lookup"><span data-stu-id="2b204-129">Danish (Denmark) da-DK</span></span>

<span data-ttu-id="2b204-130">Niederländisch (Niederlande) nl-nl</span><span class="sxs-lookup"><span data-stu-id="2b204-130">Dutch (Netherlands) nl-NL</span></span>

<span data-ttu-id="2b204-131">Finnisch (Finnland) fi-fi</span><span class="sxs-lookup"><span data-stu-id="2b204-131">Finnish (Finland) fi-FI</span></span>

<span data-ttu-id="2b204-132">Griechisch (Griechenland) el-gr</span><span class="sxs-lookup"><span data-stu-id="2b204-132">Greek (Greece) el-GR</span></span>

<span data-ttu-id="2b204-133">Ungarisch (Ungarn) hu-hu</span><span class="sxs-lookup"><span data-stu-id="2b204-133">Hungarian (Hungary) hu-HU</span></span>

<span data-ttu-id="2b204-134">Norwegisch, Nynorsk (Norwegen) NB-Nein</span><span class="sxs-lookup"><span data-stu-id="2b204-134">Norwegian, Bokmål (Norway) nb-NO</span></span>

<span data-ttu-id="2b204-135">Polnisch (Polen) pl-pl</span><span class="sxs-lookup"><span data-stu-id="2b204-135">Polish (Poland) pl-PL</span></span>

<span data-ttu-id="2b204-136">Portugiesisch (Portugal) pt-pt</span><span class="sxs-lookup"><span data-stu-id="2b204-136">Portuguese (Portugal) pt-PT</span></span>

<span data-ttu-id="2b204-137">Slowakisch (Slowakei) sk-SK</span><span class="sxs-lookup"><span data-stu-id="2b204-137">Slovak (Slovakia) sk-SK</span></span>

<span data-ttu-id="2b204-138">Slowenisch (Slowenien) SL-SI</span><span class="sxs-lookup"><span data-stu-id="2b204-138">Slovenian (Slovenia) sl-SI</span></span>

<span data-ttu-id="2b204-139">SV-SE für Schwedisch (Schweden)</span><span class="sxs-lookup"><span data-stu-id="2b204-139">Swedish (Sweden) sv-SE</span></span>

<span data-ttu-id="2b204-140">Türkisch (Türkei) tr-TR</span><span class="sxs-lookup"><span data-stu-id="2b204-140">Turkish (Turkey) tr-TR</span></span>

<span data-ttu-id="2b204-141">Eine Liste aller für Client und Server unterstützten Sprachen in MBAM 2,5 und MBAM 2,5 SP1 finden Sie unter [unterstützte Konfigurationen in MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="2b204-141">For a list of all languages supported for client and server in MBAM 2.5 and MBAM 2.5 SP1, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

### <span data-ttu-id="2b204-142">Unterstützung für Windows 10</span><span class="sxs-lookup"><span data-stu-id="2b204-142">Support for Windows 10</span></span>

<span data-ttu-id="2b204-143">MBAM 2,5 SP1 bietet zusätzlich zu der Software, die in früheren Versionen von MBAM unterstützt wird, Unterstützung für Windows 10 und Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2b204-143">MBAM 2.5 SP1 adds support for Windows 10 and Windows Server 2016, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

<span data-ttu-id="2b204-144">Windows 10 wird sowohl in MBAM 2,5 als auch in MBAM 2,5 SP1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b204-144">Windows 10 is supported in both MBAM 2.5 and MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="2b204-145">Unterstützung für Microsoft SQL Server 2014 SP1</span><span class="sxs-lookup"><span data-stu-id="2b204-145">Support for Microsoft SQL Server 2014 SP1</span></span>

<span data-ttu-id="2b204-146">MBAM 2,5 SP1 bietet zusätzlich zu der Software, die in früheren Versionen von MBAM unterstützt wird, Unterstützung für Microsoft SQL Server 2014 SP1.</span><span class="sxs-lookup"><span data-stu-id="2b204-146">MBAM 2.5 SP1 adds support for Microsoft SQL Server 2014 SP1, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

### <span data-ttu-id="2b204-147">MBAM wird nicht mehr mit separatem MSI ausgeliefert</span><span class="sxs-lookup"><span data-stu-id="2b204-147">MBAM no longer ships with separate MSI</span></span>

<span data-ttu-id="2b204-148">Ab MBAM 2,5 SP1 ist eine separate MSI-Version nicht mehr im MBAM-Produkt enthalten.</span><span class="sxs-lookup"><span data-stu-id="2b204-148">Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="2b204-149">Sie können die MSI-Datei jedoch aus der ausführbaren Datei (. exe) extrahieren, die im Lieferumfang des Produkts enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2b204-149">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

### <span data-ttu-id="2b204-150">MBAM können OwnerAuth-Kennwörter über Escrow-Konto ohne TPM besitzen</span><span class="sxs-lookup"><span data-stu-id="2b204-150">MBAM can escrow OwnerAuth passwords without owning the TPM</span></span>

<span data-ttu-id="2b204-151">Wenn MBAM das TPM zuvor nicht besitzt, konnte das TPM-OwnerAuth nicht an die MBAM-Datenbank überlassen werden.</span><span class="sxs-lookup"><span data-stu-id="2b204-151">Previously, if MBAM did not own the TPM, the TPM OwnerAuth could not be escrowed to the MBAM database.</span></span> <span data-ttu-id="2b204-152">Um MBAM für das TPM zu konfigurieren und die Kennwörter zu speichern, mussten Sie die TPM-automatische Bereitstellung deaktivieren und das TPM auf dem Clientcomputer löschen.</span><span class="sxs-lookup"><span data-stu-id="2b204-152">To configure MBAM to own the TPM and to store the passwords, you had to disable TPM auto-provisioning and clear the TPM on the client computer.</span></span>

<span data-ttu-id="2b204-153">In Windows 8 und höher kann MBAM 2,5 SP1 nun die OwnerAuth-Kennwörter über einen Treuhandservice verwerten, ohne das TPM besitzen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="2b204-153">In Windows 8 and higher, MBAM 2.5 SP1 can now escrow the OwnerAuth passwords without owning the TPM.</span></span> <span data-ttu-id="2b204-154">Während des Starts des Diensts MBAM Abfragen, ob das TPM bereits im Besitz ist, und wenn dies der Fall ist, fordert es die Kennwörter des Betriebssystems an.</span><span class="sxs-lookup"><span data-stu-id="2b204-154">During service startup, MBAM queries to see if the TPM is already owned and if so, it requests the passwords from the operating system.</span></span> <span data-ttu-id="2b204-155">Die Kennwörter werden dann in der MBAM-Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2b204-155">The passwords are then escrowed to the MBAM database.</span></span> <span data-ttu-id="2b204-156">Darüber hinaus muss die Gruppenrichtlinie so eingestellt sein, dass die OwnerAuth nicht lokal gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2b204-156">In addition, Group Policy must be set to prevent the OwnerAuth from being deleted locally.</span></span>

<span data-ttu-id="2b204-157">In Windows 7 muss MBAM das TPM besitzen, damit TPM-OwnerAuth-Informationen automatisch in der MBAM-Datenbank gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2b204-157">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="2b204-158">Wenn MBAM nicht über die TPM-und Active Directory (AD)-Sicherung des TPM verfügt, das über Gruppenrichtlinien konfiguriert ist, müssen Sie die **MBAM Active Directory (AD)-Daten Import-Cmdlets** verwenden, um die TPM-OwnerAuth aus AD in die MBAM-Datenbank zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="2b204-158">If MBAM does not own the TPM and Active Directory (AD) backup of the TPM is configured through Group Policy, you must use the **MBAM Active Directory (AD) Data Import cmdlets** to copy TPM OwnerAuth from AD into the MBAM database.</span></span> <span data-ttu-id="2b204-159">Hierbei handelt es sich um fünf neue PowerShell-Cmdlets, die MBAM-Datenbanken mit den in Active Directory gespeicherten Informationen zur Volume-Wiederherstellung und den TPM-Besitzern vorab ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="2b204-159">These are five new PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="2b204-160">Weitere Informationen finden Sie unter [Sicherheitsüberlegungen zu MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).</span><span class="sxs-lookup"><span data-stu-id="2b204-160">For more information, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

### <span data-ttu-id="2b204-161">MBAM kann das TPM nach einer Sperrung automatisch entsperren</span><span class="sxs-lookup"><span data-stu-id="2b204-161">MBAM can automatically unlock the TPM after a lockout</span></span>

<span data-ttu-id="2b204-162">Auf Computern mit TPM 1,2 können Sie jetzt MBAM so konfigurieren, dass das TPM bei einer Sperrung automatisch freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2b204-162">On computers running TPM 1.2, you can now configure MBAM to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="2b204-163">Wenn die Funktion zum automatischen Zurücksetzen der TPM-Sperrung aktiviert ist, kann MBAM feststellen, dass ein Benutzer gesperrt ist, und das OwnerAuth-Kennwort aus der MBAM-Datenbank abrufen, um das TPM automatisch für den Benutzer zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="2b204-163">If the TPM lockout auto reset feature is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span>

<span data-ttu-id="2b204-164">Dieses Feature muss sowohl auf der Serverseite als auch in den Gruppenrichtlinien auf der Clientseite aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="2b204-164">This feature must be enabled on both the server side and in Group Policy on the client side.</span></span> <span data-ttu-id="2b204-165">Weitere Informationen finden Sie unter [Sicherheitsüberlegungen zu MBAM 2,5](mbam-25-security-considerations.md#bkmk-autounlock).</span><span class="sxs-lookup"><span data-stu-id="2b204-165">For more information, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-autounlock).</span></span>

### <span data-ttu-id="2b204-166">Unterstützung für FIPS-kompatiblen BitLocker-Kennwortschutz</span><span class="sxs-lookup"><span data-stu-id="2b204-166">Support for FIPS-compliant BitLocker numerical password protectors</span></span>

<span data-ttu-id="2b204-167">In mbam 2.5 wurde die Unterstützung für FIPS (Federal Information Processing Standard)-kompatible BitLocker-Wiederherstellungsschlüssel auf Geräten mit dem Betriebssystem Windows 8,1 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2b204-167">In MBAM2.5, support was added for Federal Information Processing Standard (FIPS)-compliant BitLocker recovery keys on devices running the Windows 8.1 operating system.</span></span> <span data-ttu-id="2b204-168">Windows hat jedoch FIPS-konforme Wiederherstellungsschlüssel in Windows 7 nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2b204-168">However, Windows did not implement FIPS-compliant recovery keys in Windows 7.</span></span> <span data-ttu-id="2b204-169">Daher ist für Windows 7-und Windows 8-Geräte weiterhin ein Daten Wiederherstellungs-Agent (DRA)-Schutz für die Wiederherstellung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2b204-169">Therefore, Windows 7 and Windows 8 devices still required a Data Recovery Agent (DRA) protector for recovery.</span></span>

<span data-ttu-id="2b204-170">Das Windows-Team hat FIPS-konforme Wiederherstellungsschlüssel mit einem Hotfix und MBAM 2,5 SP1 ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b204-170">The Windows team has backported FIPS-compliant recovery keys with a hotfix, and MBAM 2.5 SP1 has added support for them as well.</span></span>

<span data-ttu-id="2b204-171">**Hinweis**  Auf Client Computern, auf denen das Windows8-Betriebssystem ausgeführt wird, ist weiterhin eine DRA-Schutzkomponente erforderlich, da der Hotfix nicht auf dieses Betriebssystem portiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2b204-171">**Note** Client computers that are running the Windows8 operating system still require a DRA protector since the hotfix was not backported to that OS.</span></span> <span data-ttu-id="2b204-172">Informationen zum herunterladen und Installieren des BitLocker-Hotfixes für Windows 7-und Windows 8-Computer finden Sie unter [Hotfix-Paket 2 für die BitLocker-Verwaltung und-Überwachung 2,5](https://support.microsoft.com/kb/3015477) .</span><span class="sxs-lookup"><span data-stu-id="2b204-172">See [Hotfix Package 2 for BitLocker Administration and Monitoring 2.5](https://support.microsoft.com/kb/3015477) to download and install the BitLocker hotfix for Windows 7 and Windows 8 computers.</span></span> <span data-ttu-id="2b204-173">Informationen zu DRA finden Sie unter [Verwenden von Daten Wiederherstellungs-Agents mit BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span><span class="sxs-lookup"><span data-stu-id="2b204-173">For information about DRA, see [Using Data Recovery Agents with BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span></span>

 

<span data-ttu-id="2b204-174">Um die FIPS-Konformität in Ihrer Organisation zu aktivieren, müssen Sie die FIPS-Gruppenrichtlinieneinstellungen (Federal Information Processing Standard) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2b204-174">To enable FIPS compliance in your organization, you must configure the Federal Information Processing Standard (FIPS) Group Policy settings.</span></span> <span data-ttu-id="2b204-175">Konfigurationsanweisungen finden Sie unter [BitLocker-Gruppenrichtlinieneinstellungen](https://go.microsoft.com/fwlink/?LinkId=393560).</span><span class="sxs-lookup"><span data-stu-id="2b204-175">For configuration instructions, see [BitLocker Group Policy Settings](https://go.microsoft.com/fwlink/?LinkId=393560).</span></span>

### <span data-ttu-id="2b204-176">Anpassen der Pre-Boot-Wiederherstellungs Nachricht und-URL mit der neuen Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="2b204-176">Customize pre-boot recovery message and URL with new Group Policy setting</span></span>

<span data-ttu-id="2b204-177">Mit einer neuen Gruppenrichtlinieneinstellung, **Konfiguration der Pre-Boot-Wiederherstellungs Nachricht und-URL**, können Sie eine benutzerdefinierte Wiederherstellungs Nachricht konfigurieren oder eine URL angeben, die auf dem BitLocker-Wiederherstellungsbildschirm vor dem Start angezeigt wird, wenn das Betriebssystemlaufwerk gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="2b204-177">A new Group Policy setting, **Configure pre-boot recovery message and URL**, lets you configure a custom recovery message or specify a URL that is then displayed on the pre-boot BitLocker recovery screen when the OS drive is locked.</span></span> <span data-ttu-id="2b204-178">Diese Einstellung steht nur auf Clientcomputern mit Windows 10 zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2b204-178">This setting is only available on client computers running Windows 10.</span></span>

<span data-ttu-id="2b204-179">Wenn Sie diese Richtlinieneinstellung aktivieren, können Sie eine der folgenden Optionen für die Wiederherstellungs Nachricht vor dem Start auswählen:</span><span class="sxs-lookup"><span data-stu-id="2b204-179">If you enable this policy setting, you can you can select one of these options for the pre-boot recovery message:</span></span>

-   <span data-ttu-id="2b204-180">**Benutzerdefinierte Wiederherstellungs Nachricht verwenden**: Wählen Sie diese Option aus, um eine benutzerdefinierte Nachricht in den BitLocker-Wiederherstellungsbildschirm vor dem Start einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="2b204-180">**Use custom recovery message**: Select this option to include a custom message in the pre-boot BitLocker recovery screen.</span></span>

-   <span data-ttu-id="2b204-181">**Benutzerdefinierte Wiederherstellungs-URL verwenden**: Wählen Sie diese Option aus, um die Standard-URL zu ersetzen, die auf dem BitLocker-Wiederherstellungsbildschirm vor dem Start angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2b204-181">**Use custom recovery URL**: Select this option to replace the default URL that is displayed in the pre-boot BitLocker recovery screen.</span></span>

-   <span data-ttu-id="2b204-182">**Standard-Wiederherstellungs Nachricht und-URL verwenden**: Wählen Sie diese Option aus, um die standardmäßige BitLocker-Wiederherstellungs Nachricht und-URL im Pre-Boot BitLocker-Wiederherstellungsbildschirm anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="2b204-182">**Use default recovery message and URL**: Select this option to display the default BitLocker recovery message and URL in the pre-boot BitLocker recovery screen.</span></span> <span data-ttu-id="2b204-183">Wenn Sie zuvor eine benutzerdefinierte Wiederherstellungs Nachricht oder-URL konfiguriert haben und die Standardnachricht wiederherstellen möchten, müssen Sie diese Richtlinie aktivieren und diese Option auswählen.</span><span class="sxs-lookup"><span data-stu-id="2b204-183">If you previously configured a custom recovery message or URL and want to revert to the default message, you must enable this policy and select this option.</span></span>

<span data-ttu-id="2b204-184">Die neue Gruppenrichtlinieneinstellung befindet sich im folgenden GPO-Knoten: **Computerkonfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)-** &gt; **Betriebs System Laufwerk**.</span><span class="sxs-lookup"><span data-stu-id="2b204-184">The new Group Policy setting is located in the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** &gt; **Operating System Drive**.</span></span> <span data-ttu-id="2b204-185">Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppenrichtlinienanforderungen](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2b204-185">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

### <span data-ttu-id="2b204-186">MBAM hat Unterstützung für die verwendete Speicherplatz Verschlüsselung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2b204-186">MBAM added support for Used Space Encryption</span></span>

<span data-ttu-id="2b204-187">Wenn Sie in MBAM 2,5 SP1 die gebrauchte Speicherplatz Verschlüsselung über BitLocker-Gruppenrichtlinien aktivieren, ehrt der MBAM-Client diesen.</span><span class="sxs-lookup"><span data-stu-id="2b204-187">In MBAM 2.5 SP1, if you enable Used Space Encryption via BitLocker Group Policy, the MBAM Client honors it.</span></span>

<span data-ttu-id="2b204-188">Diese Gruppenrichtlinieneinstellung wird **auf Betriebssystemlaufwerken als Erzwingen des Laufwerk Verschlüsselungstyps** bezeichnet und befindet sich im folgenden GPO-Knoten: **Computerkonfigurations** - &gt; **Administrative Vorlagen** &gt; **Windows-Komponenten** &gt; **BitLocker Drive Encryption** - &gt; **Betriebssystemlaufwerke**.</span><span class="sxs-lookup"><span data-stu-id="2b204-188">This Group Policy setting is called **Enforce drive encryption type on operating system drives** and is located in the following GPO node: **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **BitLocker Drive Encryption** &gt; **Operating System Drives**.</span></span> <span data-ttu-id="2b204-189">Wenn Sie diese Richtlinie aktivieren und den Verschlüsselungstyp als **nur verwendeter Speicherplatz Verschlüsselung**auswählen, wird die Richtlinie von MBAM berücksichtigt, und BitLocker verschlüsselt nur den auf dem Volume verwendeten Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="2b204-189">If you enable this policy and select the encryption type as **Used Space Only encryption**, MBAM will honor the policy and BitLocker will only encrypt disk space that is used on the volume.</span></span>

<span data-ttu-id="2b204-190">Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppenrichtlinienanforderungen](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2b204-190">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

### <span data-ttu-id="2b204-191">MBAM-Client Unterstützung für verschlüsselte Festplatten</span><span class="sxs-lookup"><span data-stu-id="2b204-191">MBAM Client support for Encrypted Hard Drives</span></span>

<span data-ttu-id="2b204-192">MBAM unterstützt BitLocker auf verschlüsselten Festplatten, die die TCG-Spezifikationsanforderungen für Opal-und IEEE-1667-Standards erfüllen.</span><span class="sxs-lookup"><span data-stu-id="2b204-192">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="2b204-193">Wenn BitLocker auf diesen Geräten aktiviert ist, generiert es Schlüssel und führt Verwaltungsfunktionen auf dem verschlüsselten Laufwerk aus.</span><span class="sxs-lookup"><span data-stu-id="2b204-193">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="2b204-194">Weitere Informationen finden Sie unter [verschlüsselte Festplatte](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2b204-194">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>

### <span data-ttu-id="2b204-195">Delegierungs Konfiguration wird beim Registrieren von SPNs nicht mehr benötigt</span><span class="sxs-lookup"><span data-stu-id="2b204-195">Delegation configuration no longer required when registering SPNs</span></span>

<span data-ttu-id="2b204-196">Die Anforderung zum Konfigurieren einer beschränkten Delegierung für SPNs, die Sie für das Anwendungspoolkonto registrieren, ist in MBAM 2,5 SP1 nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2b204-196">The requirement to configure constrained delegation for SPNs that you register for the application pool account is no longer necessary in MBAM 2.5 SP1.</span></span> <span data-ttu-id="2b204-197">Es ist jedoch weiterhin eine Voraussetzung für MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="2b204-197">However, it is still a requirement for MBAM 2.5.</span></span>

### <span data-ttu-id="2b204-198">Aktivieren von BitLocker mithilfe von MBAM als Teil einer Windows-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="2b204-198">Enable BitLocker using MBAM as Part of a Windows Deployment</span></span>

<span data-ttu-id="2b204-199">In MBAM 2,5 SP1 können Sie ein PowerShell-Skript verwenden, um die BitLocker-Laufwerkverschlüsselung und die Escrow-Wiederherstellungsschlüssel für den MBAM-Server zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2b204-199">In MBAM 2.5 SP1, you can use a PowerShell script to configure BitLocker drive encryption and escrow recovery keys to the MBAM Server.</span></span>

<span data-ttu-id="2b204-200">Weitere Informationen finden Sie unter so wird [es gemacht: Aktivieren von BitLocker mithilfe von MBAM als Teil einer Windows-Bereitstellung](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)</span><span class="sxs-lookup"><span data-stu-id="2b204-200">For more information, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)</span></span>

### <span data-ttu-id="2b204-201">Self-Service-Portal kann mithilfe von PowerShell oder dem SSP-Anpassungs-Assistenten angepasst werden</span><span class="sxs-lookup"><span data-stu-id="2b204-201">Self-Service Portal can be customized by using either PowerShell or the SSP customization wizard</span></span>

<span data-ttu-id="2b204-202">Ab MBAM 2,5 SP1 kann das Self-Service-Portal mithilfe des Anpassungs-Assistenten und mithilfe von PowerShell konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="2b204-202">As of MBAM 2.5 SP1, the Self-Service Portal can be configured by using the customization wizard as well as by using PowerShell.</span></span> <span data-ttu-id="2b204-203">Weitere Informationen finden Sie unter [Konfigurieren der MBAM 2,5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="2b204-203">See [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

### <span data-ttu-id="2b204-204">Webbrowser wird nicht mehr versehentlich als Administrator ausgeführt</span><span class="sxs-lookup"><span data-stu-id="2b204-204">Web browser no longer unintentionally runs as administrator</span></span>

<span data-ttu-id="2b204-205">Ein Problem in MBAM 2,5 hat dazu geführt, dass die Hilfe Links im Serverkonfigurations Tool dazu führen, dass Browserfenster mit Administratorrechten geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="2b204-205">An issue in MBAM 2.5 caused help links in the Server Configuration tool to cause browser windows to open with administrator rights.</span></span> <span data-ttu-id="2b204-206">Dieses Problem wurde in MBAM 2,5 SP1 behoben.</span><span class="sxs-lookup"><span data-stu-id="2b204-206">This issue is fixed in MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="2b204-207">Sie müssen die JavaScript-Dateien nicht mehr herunterladen, um das Self-Service-Portal zu konfigurieren, wenn auf das CDN nicht zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b204-207">No longer need to download the JavaScript files to configure the Self-Service Portal when the CDN is inaccessible</span></span>

<span data-ttu-id="2b204-208">In MBAM 2,5 und früheren Versionen mussten die für die Konfiguration des Self-Service-Portals verwendeten jQuery-Dateien im Voraus aus dem CDN heruntergeladen werden, wenn Clients, die auf das Self-Service-Portal zugreifen, keinen Internetzugriff hatten.</span><span class="sxs-lookup"><span data-stu-id="2b204-208">In MBAM 2.5 and earlier, the jQuery files used for configuration of the Self-Service Portal had to be downloaded from the CDN in advance if clients accessing the Self-Service Portal did not have internet access.</span></span> <span data-ttu-id="2b204-209">In MBAM 2,5 SP1 sind alle JavaScript-Dateien im Produkt enthalten, daher ist das Herunterladen unnötig.</span><span class="sxs-lookup"><span data-stu-id="2b204-209">In MBAM 2.5 SP1, all JavaScript files are included in the product, so downloading them is unnecessary.</span></span>

### <span data-ttu-id="2b204-210">Berichte können im Berichts-Generator 3,0 geöffnet werden</span><span class="sxs-lookup"><span data-stu-id="2b204-210">Reports can be opened in Report Builder 3.0</span></span>

<span data-ttu-id="2b204-211">In MBAM 2,5 SP1 wurden die Berichte auf das neueste Schema der Berichtsdefinitionssprache aktualisiert, sodass Benutzer die Berichte im Berichts-Generator 3,0 öffnen und anpassen und diese sofort speichern können, ohne die Berichtsdatei zu beschädigen.</span><span class="sxs-lookup"><span data-stu-id="2b204-211">In MBAM 2.5 SP1, the reports have been updated to the latest report definition language schema, allowing users to open and customize the reports in Report Builder 3.0 and save them immediately without corrupting the report file.</span></span>

### <span data-ttu-id="2b204-212">Neue PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2b204-212">New PowerShell cmdlets</span></span>

<span data-ttu-id="2b204-213">Mit den neuen PowerShell-Cmdlets für MBAM 2,5 SP1 können Sie verschiedene MBAM-Features wie Datenbanken, Berichte und Webanwendungen konfigurieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="2b204-213">New PowerShell cmdlets for MBAM 2.5 SP1 enable you to configure and manage different MBAM features, including databases, reports, and web applications.</span></span> <span data-ttu-id="2b204-214">Jedes Feature verfügt über ein entsprechendes PowerShell-Cmdlet, das Sie zum Aktivieren oder Deaktivieren von Features oder zum Abrufen von Informationen über das Feature verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2b204-214">Each feature has a corresponding PowerShell cmdlet that you can use to enable or disable features, or to get information about the feature.</span></span>

<span data-ttu-id="2b204-215">Die folgenden Cmdlets wurden für MBAM 2,5 SP1 implementiert:</span><span class="sxs-lookup"><span data-stu-id="2b204-215">The following cmdlets have been implemented for MBAM 2.5 SP1:</span></span>

-   <span data-ttu-id="2b204-216">Write-MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="2b204-216">Write-MbamTpmInformation</span></span>

-   <span data-ttu-id="2b204-217">Write-MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="2b204-217">Write-MbamRecoveryInformation</span></span>

-   <span data-ttu-id="2b204-218">Lesen-ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="2b204-218">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="2b204-219">Lesen-ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="2b204-219">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="2b204-220">Write-MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="2b204-220">Write-MbamComputerUser</span></span>

<span data-ttu-id="2b204-221">Die folgenden Parameter wurden in den Cmdlets Enable-MbamWebApplication und Test-MbamWebApplication für MBAM 2,5 SP1 implementiert:</span><span class="sxs-lookup"><span data-stu-id="2b204-221">The following parameters have been implemented in the Enable-MbamWebApplication and Test-MbamWebApplication cmdlets for MBAM 2.5 SP1:</span></span>

-   <span data-ttu-id="2b204-222">DataMigrationAccessGroup</span><span class="sxs-lookup"><span data-stu-id="2b204-222">DataMigrationAccessGroup</span></span>

-   <span data-ttu-id="2b204-223">TpmAutoUnlock</span><span class="sxs-lookup"><span data-stu-id="2b204-223">TpmAutoUnlock</span></span>

<span data-ttu-id="2b204-224">Informationen zu den Cmdlets finden Sie unter Hilfe zu den [MBAM 2,5-Sicherheitsüberlegungen](mbam-25-security-considerations.md) und [Microsoft BitLocker-Cmdlets für Verwaltung und Überwachung](https://technet.microsoft.com/library/dn720418.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b204-224">For information about the cmdlets, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md) and [Microsoft Bitlocker Administration and Monitoring Cmdlet Help](https://technet.microsoft.com/library/dn720418.aspx).</span></span>

### <span data-ttu-id="2b204-225">MBAM-Agent erkennt Präsentationsmodus</span><span class="sxs-lookup"><span data-stu-id="2b204-225">MBAM agent detects presentation mode</span></span>

<span data-ttu-id="2b204-226">Der MBAM-Agent kann erkennen, wenn sich der Computer im Präsentationsmodus befindet, und vermeiden, dass die MBAM-Benutzeroberfläche zu diesem Zeitpunkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2b204-226">The MBAM agent can detect when the computer is in presentation mode and avoid invoking the MBAM UI at that time.</span></span>

### <span data-ttu-id="2b204-227">MBAM-Agent-Dienst ist jetzt für die Verwendung des verzögerten Starts konfiguriert</span><span class="sxs-lookup"><span data-stu-id="2b204-227">MBAM agent service now configured to use delayed start</span></span>

<span data-ttu-id="2b204-228">Nach der Installation wird der Dienst den MBAM-Agent-Dienst so einrichten, dass er den verzögerten Start verwendet, wodurch die Zeit verkürzt wird, die zum Starten von Windows benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2b204-228">After installation, the service will now set the MBAM agent service to use delayed start, decreasing the amount of time it takes to start Windows.</span></span>

### <span data-ttu-id="2b204-229">Gesperrte feste Datenvolumina werden jetzt als kompatibel gemeldet</span><span class="sxs-lookup"><span data-stu-id="2b204-229">Locked Fixed Data volumes now report as Compliant</span></span>

<span data-ttu-id="2b204-230">Die Logik für die Kompatibilitäts Berechnung für die Volumes "gesperrte feste Daten" wurde geändert, um die Volumes als "kompatibel" zu melden, aber mit einem Protector-Zustand und einem Verschlüsselungsstatus von "unbekannt" und mit einem Kompatibilitäts Status ("Volume ist gesperrt").</span><span class="sxs-lookup"><span data-stu-id="2b204-230">The compliance calculation logic for "Locked Fixed Data" volumes has been changed to report the volumes as "Compliant," but with a Protector State and Encryption State of "Unknown" and with a Compliance Status Detail of "Volume is locked".</span></span> <span data-ttu-id="2b204-231">Zuvor wurden gesperrte Volumes als "nicht kompatibel", als Schutzstatus "verschlüsselt", als Verschlüsselungsstatus "unbekannt" und als Kompatibilitätsstatus Detail "ein unbekannter Fehler" gemeldet.</span><span class="sxs-lookup"><span data-stu-id="2b204-231">Previously, locked volumes were reported as “Non-Compliant”, a Protector State of "Encrypted", an Encryption State of "Unknown", and a Compliance Status Detail of "An unknown error".</span></span>


## <span data-ttu-id="2b204-232">So erhalten Sie MDOP-Technologien</span><span class="sxs-lookup"><span data-stu-id="2b204-232">How to Get MDOP Technologies</span></span>


<span data-ttu-id="2b204-233">MBAM ist ein Bestandteil des Microsoft-Desktop Optimierungs Pakets (MDOP).</span><span class="sxs-lookup"><span data-stu-id="2b204-233">MBAM is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="2b204-234">MDOP ist Teil des Microsoft Software Assurance-Programms.</span><span class="sxs-lookup"><span data-stu-id="2b204-234">MDOP is part of the Microsoft Software Assurance program.</span></span> <span data-ttu-id="2b204-235">Weitere Informationen zum Microsoft Software Assurance-Programm und zum Erwerb der MDOP finden Sie unter [wie erhalte ich MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="2b204-235">For more information about the Microsoft Software Assurance program and how to acquire the MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="2b204-236">MBAM 2,5 SP1-Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="2b204-236">MBAM 2.5 SP1 Release Notes</span></span>


<span data-ttu-id="2b204-237">Weitere Informationen und aktuelle Neuigkeiten, die nicht in dieser Dokumentation enthalten sind, finden Sie unter [Versionshinweise zu MBAM 2,5 SP1](release-notes-for-mbam-25-sp1.md).</span><span class="sxs-lookup"><span data-stu-id="2b204-237">For more information and late-breaking news that is not included in this documentation, see [Release Notes for MBAM 2.5 SP1](release-notes-for-mbam-25-sp1.md).</span></span>

## <span data-ttu-id="2b204-238">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="2b204-238">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2b204-239">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="2b204-239">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2b204-240">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="2b204-240">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="2b204-241">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2b204-241">Related topics</span></span>


[<span data-ttu-id="2b204-242">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="2b204-242">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="2b204-243">Erste Schritte mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2b204-243">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

 

 





