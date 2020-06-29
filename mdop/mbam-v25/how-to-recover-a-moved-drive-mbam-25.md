---
title: So stellen Sie ein verschobenes Laufwerk wieder her
description: So stellen Sie ein verschobenes Laufwerk wieder her
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809898"
---
# <span data-ttu-id="03659-103">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="03659-103">How to Recover a Moved Drive</span></span>
<span data-ttu-id="03659-104">In diesem Thema wird die Verwendung der Website "Verwaltung und Überwachung" (auch als "Helpdesk" bezeichnet) zum Wiederherstellen eines Betriebssystemlaufwerks erläutert, das nach dem Verschlüsseln durch die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="03659-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to recover an operating system drive that was moved after being encrypted by Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="03659-105">Wenn ein Laufwerk verschoben wird, akzeptiert es nicht mehr die PIN, die auf dem vorherigen Computer verwendet wurde, da sich der TPM-Chip (Trusted Platform Module) geändert hat.</span><span class="sxs-lookup"><span data-stu-id="03659-105">When a drive is moved, it no longer accepts the PIN that was used in the previous computer because the Trusted Platform Module (TPM) chip has changed.</span></span> <span data-ttu-id="03659-106">Zum Wiederherstellen des verschobenen Laufwerks müssen Sie die Wiederherstellungsschlüssel-ID abrufen, um das Wiederherstellungskennwort abzurufen.</span><span class="sxs-lookup"><span data-stu-id="03659-106">To recover the moved drive, you must obtain the recovery key ID to retrieve the recovery password.</span></span>

<span data-ttu-id="03659-107">Zum Wiederherstellen eines verschobenen Laufwerks müssen Sie den Bereich **Drive Recovery** der Website Verwaltung und Überwachung verwenden.</span><span class="sxs-lookup"><span data-stu-id="03659-107">To recover a moved drive, you must use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="03659-108">Für den Zugriff auf den **Laufwerk Wiederherstellungs** Bereich müssen Sie der Rolle MBAM Helpdesk-Benutzer oder der MBAM Advanced Helpdesk-Benutzerrolle zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="03659-108">To access the **Drive Recovery** area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="03659-109">Weitere Informationen zu diesen Rollen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="03659-109">For more information about these roles, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

**<span data-ttu-id="03659-110">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="03659-110">To recover a moved drive</span></span>**
1.  <span data-ttu-id="03659-111">Starten Sie den Computer auf dem Computer, auf dem sich das verschobene Laufwerk befindet, im Windows Recovery Environment (WinRE)-Modus, oder starten Sie den Computer mit dem Microsoft Diagnostic and Recovery Toolset (Dart).</span><span class="sxs-lookup"><span data-stu-id="03659-111">On the computer that contains the moved drive, start the computer in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="03659-112">Nachdem der Computer mit WinRE oder Dart gestartet wurde, behandelt MBAM das verschobene Betriebssystemlaufwerk als festes Datenlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="03659-112">After the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a fixed data drive.</span></span> <span data-ttu-id="03659-113">MBAM zeigt dann die Wiederherstellungskennwort-ID des Laufwerks an und fragt nach dem Wiederherstellungskennwort.</span><span class="sxs-lookup"><span data-stu-id="03659-113">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="03659-114">**Hinweis**  In einigen Fällen können Sie möglicherweise auf **Ich habe die PIN** während des Startvorgangs vergessen klicken und dann in den Wiederherstellungsmodus wechseln, um die Wiederherstellungsschlüssel-ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="03659-114">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="03659-115">Verwenden Sie die Wiederherstellungsschlüssel-ID, um das Wiederherstellungskennwort abzurufen, und Entsperren Sie das Laufwerk über die Website Verwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="03659-115">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring Website.</span></span> <span data-ttu-id="03659-116">Anweisungen hierzu finden Sie unter [Wiederherstellen eines Laufwerks im Wiederherstellungsmodus](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="03659-116">For instructions, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span></span>

    <span data-ttu-id="03659-117">Wenn das verschobene Laufwerk für die Verwendung eines TPM-Chips auf dem ursprünglichen Computer konfiguriert wurde, führen Sie die folgenden zusätzlichen Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="03659-117">If the moved drive was configured to use a TPM chip on the original computer, complete the following additional steps.</span></span> <span data-ttu-id="03659-118">Andernfalls ist der Wiederherstellungsvorgang abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="03659-118">Otherwise, the recovery process is complete.</span></span>

4.  <span data-ttu-id="03659-119">Öffnen Sie nach dem Entsperren des Laufwerks und dem Abschluss des Startvorgangs eine Eingabeaufforderung im WinRE-Modus, und verwenden Sie den `manage-bde` Befehl zum Entschlüsseln des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="03659-119">After unlocking the drive and completing the start process, open a command prompt in WinRE mode and use the `manage-bde` command to decrypt the drive.</span></span> <span data-ttu-id="03659-120">Die Verwendung dieses Tools ist die einzige Möglichkeit, das TPM und die PIN-Beschützer ohne den ursprünglichen TPM-Chip zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="03659-120">Using this tool is the only way to remove the TPM plus the PIN protector without the original TPM chip.</span></span> <span data-ttu-id="03659-121">Informationen zum `manage-bde` Befehl finden Sie unter [manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span><span class="sxs-lookup"><span data-stu-id="03659-121">For information about the `manage-bde` command, see [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span></span>

5.  <span data-ttu-id="03659-122">Wenn die Entfernung abgeschlossen ist, starten Sie den Computer in der Regel.</span><span class="sxs-lookup"><span data-stu-id="03659-122">When the removal is completed, start the computer normally.</span></span> <span data-ttu-id="03659-123">Der MBAM-Agent setzt nun die Richtlinie zum Verschlüsseln des Laufwerks mit dem TPM des neuen Computers und der PIN durch.</span><span class="sxs-lookup"><span data-stu-id="03659-123">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus the PIN.</span></span>



## <span data-ttu-id="03659-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="03659-124">Related topics</span></span>


[<span data-ttu-id="03659-125">Durchführen der BitLocker-Verwaltung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="03659-125">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="03659-126">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="03659-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="03659-127">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="03659-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="03659-128">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="03659-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





