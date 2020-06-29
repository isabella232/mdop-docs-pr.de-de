---
title: Verwalten von MBAM 2.0 mit PowerShell
description: Verwalten von MBAM 2.0 mit PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809994"
---
# <span data-ttu-id="826ce-103">Verwalten von MBAM 2.0 mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="826ce-103">Administering MBAM 2.0 Using PowerShell</span></span>


<span data-ttu-id="826ce-104">Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) enthält die folgenden aufgelisteten Satz von Windows PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="826ce-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="826ce-105">Administratoren können diese PowerShell-Cmdlets verwenden, um verschiedene Microsoft BitLocker-Verwaltungs-und-Überwachungsserver Aufgaben über die Befehlszeile statt über die MBAM-Verwaltungswebsite durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="826ce-105">Administrators can use these PowerShell cmdlets to perform various Microsoft BitLocker Administration and Monitoring server tasks from the command line rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="826ce-106">Verwalten von MBAM mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="826ce-106">How to Administer MBAM Using PowerShell</span></span>


<span data-ttu-id="826ce-107">Verwenden Sie die hier beschriebenen PowerShell-Cmdlets, um MBAM zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="826ce-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="826ce-108">Name</span><span class="sxs-lookup"><span data-stu-id="826ce-108">Name</span></span></th>
<th align="left"><span data-ttu-id="826ce-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="826ce-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="826ce-110">Installieren-mbam</span><span class="sxs-lookup"><span data-stu-id="826ce-110">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="826ce-111">Installiert die MBAM-Features, die Erweiterte Richtlinien-, Verschlüsselungs-, Schlüssel Wiederherstellungs-und Konformitätsberichte bieten.</span><span class="sxs-lookup"><span data-stu-id="826ce-111">Installs the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="826ce-112">Deinstallieren-mbam</span><span class="sxs-lookup"><span data-stu-id="826ce-112">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="826ce-113">Entfernt die MBAM-Features, die Erweiterte Richtlinien-, Verschlüsselungs-, Schlüssel Wiederherstellungs-und Compliance-Berichterstattungstools bieten.</span><span class="sxs-lookup"><span data-stu-id="826ce-113">Removes the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="826ce-114">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="826ce-114">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="826ce-115">Fordert einen MBAM-Wiederherstellungsschlüssel an, der Benutzern die Sperrung eines Computers oder eines verschlüsselten Laufwerks ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="826ce-115">Requests an MBAM recovery key that will enable users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="826ce-116">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="826ce-116">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="826ce-117">Bietet Benutzern ein TPM-Besitzerkennwort, das Sie zum Entsperren eines Trusted Platform Module (TPM) verwenden können, wenn das TPM Sie gesperrt hat und Ihre PIN nicht mehr akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="826ce-117">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="826ce-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="826ce-118">Related topics</span></span>


[<span data-ttu-id="826ce-119">Vorgänge für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="826ce-119">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





