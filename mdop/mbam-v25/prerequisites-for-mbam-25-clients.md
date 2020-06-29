---
title: Voraussetzungen für MBAM 2.5-Clients
description: Voraussetzungen für MBAM 2.5-Clients
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812073"
---
# <span data-ttu-id="85090-103">Voraussetzungen für MBAM 2.5-Clients</span><span class="sxs-lookup"><span data-stu-id="85090-103">Prerequisites for MBAM 2.5 Clients</span></span>


<span data-ttu-id="85090-104">Bevor Sie die MBAM-Client Software auf den Computern der Endbenutzer installieren, stellen Sie sicher, dass Ihre Umgebung und die Clientcomputer die folgenden Voraussetzungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="85090-104">Before you install the MBAM Client software on end users' computers, ensure that your environment and the client computers meet the following prerequisites.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="85090-105">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="85090-105">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="85090-106">Details</span><span class="sxs-lookup"><span data-stu-id="85090-106">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85090-107">Die Unternehmensdomäne muss mindestens einen Windows Server 2008-Domänencontroller (oder höher) enthalten.</span><span class="sxs-lookup"><span data-stu-id="85090-107">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85090-108">Der Clientcomputer muss beim Unternehmensintranet angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="85090-108">The client computer must be logged on to the enterprise intranet.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85090-109">Nur für Clientcomputer unter Windows 7: jeder Client muss über eine TPM-Funktion (Trusted Platform Module) verfügen (TPM 1,2 oder höher).</span><span class="sxs-lookup"><span data-stu-id="85090-109">For Windows 7 client computers only: Each client must have Trusted Platform Module (TPM) capability (TPM 1.2 or later).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85090-110">Für Windows 8,1, Windows 10 RTM oder Windows 10, Version 1511, nur Clientcomputer: Wenn MBAM in der Lage sein soll, die TPM-Wiederherstellungsschlüssel zu speichern und zu verwalten, muss die TPM-automatische Bereitstellung deaktiviert sein, und MBAM muss als Besitzer des TPM eingestellt sein, bevor Sie MBAM bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="85090-110">For Windows 8.1, Windows 10 RTM or Windows 10 version 1511 client computers only: If you want MBAM to be able to store and manage the TPM recovery keys, TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p>
<p><span data-ttu-id="85090-111">In MBAM 2,5 SP1 müssen Sie die TPM-automatische Bereitstellung nicht mehr deaktivieren, aber Sie müssen sicherstellen, dass die TPM-Gruppenrichtlinienobjekte auf nicht Escrow-TPM-OwnerAuth zu Active Directory festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="85090-111">In MBAM 2.5 SP1 only, you no longer need to turn off TPM auto-provisioning, but you must make sure that the TPM Group Policy Objects are set to not escrow TPM OwnerAuth to Active Directory.</span></span></p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)"><span data-ttu-id="85090-112">Sicherheitsüberlegungen zu MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="85090-112">MBAM 2.5 Security Considerations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85090-113">Für Windows 10, Version 1607 oder höher, kann nur Windows den Besitz des TPM übernehmen.</span><span class="sxs-lookup"><span data-stu-id="85090-113">For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="85090-114">In addiiton wird Windows das TPM-Besitzerkennwort beim Bereitstellen des TPMs nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="85090-114">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span></p>
<p><span data-ttu-id="85090-115">In MBAM 2,5 SP1 müssen Sie die automatische Bereitstellung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="85090-115">In MBAM 2.5 SP1, you must turn on auto-provisioning.</span></span></p>
</p></td>
<td align="left"><p><span data-ttu-id="85090-116">Weitere Informationen finden Sie unter <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> TPM-Besitzerkennwort </a> .</span><span class="sxs-lookup"><span data-stu-id="85090-116">See <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)">TPM owner password</a> for further details.</span></span>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85090-117">Der TPM-Chip muss im BIOS aktiviert sein und vom Betriebssystem Rückstellen.</span><span class="sxs-lookup"><span data-stu-id="85090-117">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="85090-118">Weitere Informationen finden Sie in der BIOS-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="85090-118">See the BIOS documentation for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85090-119">Die Festplatte des Computers muss mindestens zwei Partitionen enthalten und muss mit dem NTFS-Dateisystem formatiert sein.</span><span class="sxs-lookup"><span data-stu-id="85090-119">The computer’s hard disk must have at least two partitions and must be formatted with the NTFS file system.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85090-120">Die Festplatte des Computers muss ein BIOS aufweisen, das mit TPM kompatibel ist und USB-Geräte während des Computerstarts unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85090-120">The computer’s hard disk must have a BIOS that is compatible with TPM and that supports USB devices during computer startup.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="85090-121">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="85090-121">Note</span></span></strong><br/><p><span data-ttu-id="85090-122">Stellen Sie sicher, dass die Tastatur, das Video oder die Maus direkt verbunden sind und nicht über einen KVM-Schalter (Keyboard, Video oder Maus) verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="85090-122">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="85090-123">Ein KVM-Switch kann die Fähigkeit des Computers stören, die physische Anwesenheit von Hardware zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="85090-123">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85090-124">Wenn Sie einen Proxy verwenden, muss er im Systemkontext sichtbar sein.</span><span class="sxs-lookup"><span data-stu-id="85090-124">If you use a proxy, it must be visible in the system context.</span></span> <span data-ttu-id="85090-125">MBAM wird im Systemkontext und nicht im Benutzerkontext ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85090-125">MBAM runs under the system context, not the user context.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="85090-126">Wichtig</span><span class="sxs-lookup"><span data-stu-id="85090-126">Important</span></span>**  
<span data-ttu-id="85090-127">Wenn BitLocker ohne MBAM verwendet wurde, kann MBAM installiert werden und die vorhandenen TPM-Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="85090-127">If BitLocker was used without MBAM, MBAM can be installed and utilize the existing TPM information.</span></span>




## <span data-ttu-id="85090-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="85090-128">Related topics</span></span>


[<span data-ttu-id="85090-129">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="85090-129">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="85090-130">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="85090-130">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)


## <span data-ttu-id="85090-131">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="85090-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="85090-132">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="85090-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="85090-133">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="85090-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






