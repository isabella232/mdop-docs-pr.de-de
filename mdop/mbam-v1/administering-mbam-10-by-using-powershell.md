---
title: Verwalten von MBAM 1.0 mithilfe von PowerShell
description: Verwalten von MBAM 1.0 mithilfe von PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810975"
---
# <span data-ttu-id="c0ddd-103">Verwalten von MBAM 1.0 mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0ddd-103">Administering MBAM 1.0 by Using PowerShell</span></span>


<span data-ttu-id="c0ddd-104">Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) enthält die folgenden aufgelisteten Satz von Windows PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="c0ddd-105">Administratoren können mithilfe dieser PowerShell-Cmdlets verschiedene MBAM-Serveraufgaben über die Eingabeaufforderung statt über die MBAM-Verwaltungswebsite ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-105">Administrators can use these PowerShell cmdlets to perform various MBAM server tasks from the command prompt rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="c0ddd-106">Verwalten von MBAM mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0ddd-106">How to administer MBAM by using PowerShell</span></span>


<span data-ttu-id="c0ddd-107">Verwenden Sie die hier beschriebenen PowerShell-Cmdlets, um MBAM zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0ddd-108">Name</span><span class="sxs-lookup"><span data-stu-id="c0ddd-108">Name</span></span></th>
<th align="left"><span data-ttu-id="c0ddd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0ddd-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0ddd-110">Add-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="c0ddd-110">Add-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0ddd-111">Fügt ein neues Hardwaremodell zur MBAM-Hardwareinventur hinzu.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-111">Adds a new hardware model to the MBAM hardware inventory.</span></span> <span data-ttu-id="c0ddd-112">Dieses Cmdlet kann auch angeben, ob die Hardware für die BitLocker-Laufwerkverschlüsselung unterstützt oder nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-112">This cmdlet can also specify whether the hardware is supported or unsupported for BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0ddd-113">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="c0ddd-113">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0ddd-114">Fordert einen MBAM-Wiederherstellungsschlüssel an, mit dem ein Benutzer einen Computer oder ein verschlüsseltes Laufwerk entsperren kann.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-114">Requests an MBAM recovery key that will enable a user to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0ddd-115">Get-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="c0ddd-115">Get-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0ddd-116">Ruft eine Master-Hardwareinventur ab, die Daten enthält, die angeben, ob Hardware Modelle kompatibel oder mit der BitLocker-Laufwerkverschlüsselung nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-116">Gets a master hardware inventory that contains data that indicates whether hardware models are compatible or incompatible with BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0ddd-117">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="c0ddd-117">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0ddd-118">Stellt ein TPM-Besitzerkennwort für einen Benutzer zum Verwalten des TPM-Zugriffs (Trusted Platform Module) bereit.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-118">Provides a TPM owner password for a user to manage their TPM (Trusted Platform Module) access.</span></span> <span data-ttu-id="c0ddd-119">Hilft Benutzern, wenn TPM Sie gesperrt hat und Ihre PIN nicht mehr akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-119">Helps users when TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0ddd-120">Installieren-mbam</span><span class="sxs-lookup"><span data-stu-id="c0ddd-120">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0ddd-121">Installiert MBAM-Features, die erweiterte Gruppenrichtlinien-, Verschlüsselungs-, Schlüssel Wiederherstellungs-und Kompatibilitäts Berichterstattungstools bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-121">Installs MBAM features that provide advanced group policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0ddd-122">Remove-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="c0ddd-122">Remove-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0ddd-123">Entfernt die Hardware Modelle aus der Hardwareinventur.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-123">Removes the hardware models from the hardware inventory.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0ddd-124">Satz-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="c0ddd-124">Set-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0ddd-125">Ermöglicht die Verwaltung einer Master-Hardwareinventur, um festzulegen, ob Hardware Modelle für die BitLocker-Verschlüsselung geeignet oder nicht geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-125">Allows management of a master hardware inventory to designate whether or not hardware models are capable or incapable to perform BitLocker encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0ddd-126">Deinstallieren-mbam</span><span class="sxs-lookup"><span data-stu-id="c0ddd-126">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0ddd-127">Entfernt zuvor installierte MBAM-Features, die Erweiterte Richtlinien-, Verschlüsselungs-, Schlüssel Wiederherstellungs-und Kompatibilitäts Berichterstattungstools bieten.</span><span class="sxs-lookup"><span data-stu-id="c0ddd-127">Removes previously installed MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c0ddd-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c0ddd-128">Related topics</span></span>


[<span data-ttu-id="c0ddd-129">Vorgänge für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c0ddd-129">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





