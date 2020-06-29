---
title: Verwenden von Windows PowerShell zum Verwalten von MBAM 2.5
description: Verwenden von Windows PowerShell zum Verwalten von MBAM 2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804451"
---
# <span data-ttu-id="381e2-103">Verwenden von Windows PowerShell zum Verwalten von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="381e2-103">Using Windows PowerShell to Administer MBAM 2.5</span></span>


<span data-ttu-id="381e2-104">In diesem Thema werden die Windows PowerShell-Cmdlets für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) beschrieben, die sich auf das Wiederherstellen von Computern oder Laufwerken beziehen, wenn Benutzer gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="381e2-104">This topic describes Windows PowerShell cmdlets for Microsoft BitLocker Administration and Monitoring (MBAM) that relate to recovering computers or drives when users get locked out.</span></span>

<span data-ttu-id="381e2-105">Informationen zu Cmdlets, die Sie zum Konfigurieren der MBAM-Server Features verwenden, finden Sie unter [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="381e2-105">For cmdlets that you use to configure MBAM Server features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a><span data-ttu-id="381e2-106">Cmdlets zum Herstellen von Computern oder Laufwerken, die von MBAM verwaltet werden</span><span class="sxs-lookup"><span data-stu-id="381e2-106">Cmdlets for recovering computers or drives that are managed by MBAM</span></span>


<span data-ttu-id="381e2-107">Verwenden Sie die folgenden Windows PowerShell-Cmdlets zum Wiederherstellen von Computern oder Laufwerken, die von MBAM verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="381e2-107">Use the following Windows PowerShell cmdlets to recover computers or drives that are managed by MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="381e2-108">Name</span><span class="sxs-lookup"><span data-stu-id="381e2-108">Name</span></span></th>
<th align="left"><span data-ttu-id="381e2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="381e2-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="381e2-110">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="381e2-110">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="381e2-111">Fordert einen MBAM-Wiederherstellungsschlüssel an, der Benutzern das Entsperren eines Computers oder eines verschlüsselten Laufwerks ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="381e2-111">Requests an MBAM recovery key that enables users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="381e2-112">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="381e2-112">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="381e2-113">Bietet Benutzern ein TPM-Besitzerkennwort, das Sie zum Entsperren eines Trusted Platform Module (TPM) verwenden können, wenn das TPM Sie gesperrt hat und Ihre PIN nicht mehr akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="381e2-113">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> <span data-ttu-id="381e2-114">Hilfe zu MBAM-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="381e2-114">MBAM cmdlet Help</span></span>


<span data-ttu-id="381e2-115">Die Windows PowerShell-Hilfe für MBAM-Cmdlets steht in den folgenden Formaten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="381e2-115">Windows PowerShell Help for MBAM cmdlets is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="381e2-116">Windows PowerShell-Hilfeformat</span><span class="sxs-lookup"><span data-stu-id="381e2-116">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="381e2-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="381e2-117">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="381e2-118">Geben Sie an einer Windows PowerShell-Eingabeaufforderung <strong> Get-Help- </strong> &lt; <em> Cmdlet ein.</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="381e2-118">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="381e2-119">Wenn Sie die neuesten Windows PowerShell-Cmdlets hochladen möchten, befolgen Sie die Anweisungen unter <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="381e2-119">To upload the latest Windows PowerShell cmdlets, follow the instructions in <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="381e2-120">Auf TechNet als Webseiten</span><span class="sxs-lookup"><span data-stu-id="381e2-120">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="381e2-121">Im Download Center als Word. docx-Datei</span><span class="sxs-lookup"><span data-stu-id="381e2-121">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="381e2-122">Im Download Center als PDF-Datei</span><span class="sxs-lookup"><span data-stu-id="381e2-122">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="381e2-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="381e2-123">Related topics</span></span>


[<span data-ttu-id="381e2-124">Verwalten von MBAM 2.5-Funktionen</span><span class="sxs-lookup"><span data-stu-id="381e2-124">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="381e2-125">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="381e2-125">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## <span data-ttu-id="381e2-126">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="381e2-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="381e2-127">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="381e2-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="381e2-128">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="381e2-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





