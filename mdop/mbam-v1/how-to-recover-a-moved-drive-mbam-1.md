---
title: So stellen Sie ein verschobenes Laufwerk wieder her
description: So stellen Sie ein verschobenes Laufwerk wieder her
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804595"
---
# <span data-ttu-id="aedeb-103">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="aedeb-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="aedeb-104">Wenn Sie ein Betriebssystemlaufwerk verschieben, das zuvor mithilfe von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verschlüsselt wurde, müssen Sie bestimmte Probleme beheben.</span><span class="sxs-lookup"><span data-stu-id="aedeb-104">When you move an operating system drive that has been previously encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), you must resolve certain issues.</span></span> <span data-ttu-id="aedeb-105">Nachdem eine PIN an den neuen Computer angefügt wurde, akzeptiert das Laufwerk nicht die Start-PIN, die auf dem vorherigen Computer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="aedeb-105">After a PIN is attached to the new computer, the drive will not accept the start-up PIN that was used in previous computer.</span></span> <span data-ttu-id="aedeb-106">Das System hält die PIN wegen der Änderung des TPM-Chips (Trusted Platform Module) für ungültig.</span><span class="sxs-lookup"><span data-stu-id="aedeb-106">The system considers the PIN to be invalid because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="aedeb-107">Sie müssen eine Wiederherstellungsschlüssel-ID abrufen, um das Wiederherstellungskennwort abzurufen, um das verschobene Laufwerk verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="aedeb-107">You must obtain a recovery key ID to retrieve the recovery password in order to use the moved drive.</span></span> <span data-ttu-id="aedeb-108">Gehen Sie dazu wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="aedeb-108">To do this, use the following procedure.</span></span>

**<span data-ttu-id="aedeb-109">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="aedeb-109">To recover a moved drive</span></span>**

1.  <span data-ttu-id="aedeb-110">Starten Sie auf dem Computer, auf dem sich das verschobene Laufwerk befindet, im Windows Recovery Environment (WinRE)-Modus, oder starten Sie den Computer mithilfe des Microsoft Diagnostics and Recovery Toolset (Dart).</span><span class="sxs-lookup"><span data-stu-id="aedeb-110">On the computer that contains the moved drive, start in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="aedeb-111">Nachdem der Computer mit WinRE oder Dart gestartet wurde, behandelt MBAM das verschobene Betriebssystemlaufwerk als Datenlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="aedeb-111">Once the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="aedeb-112">MBAM zeigt dann die Wiederherstellungskennwort-ID des Laufwerks an und fragt nach dem Wiederherstellungskennwort.</span><span class="sxs-lookup"><span data-stu-id="aedeb-112">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="aedeb-113">**Hinweis**  In einigen Fällen können Sie möglicherweise auf **Ich vergesse die PIN** während des Startvorgangs klicken, um in den Wiederherstellungsmodus zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="aedeb-113">**Note** In some cases, you might be able to click **I forget the PIN** during the startup process to enter the recovery mode.</span></span> <span data-ttu-id="aedeb-114">Außerdem wird die Wiederherstellungsschlüssel-ID angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aedeb-114">This also displays the recovery key ID.</span></span>

     

3.  <span data-ttu-id="aedeb-115">Verwenden Sie auf der MBAM-Verwaltungswebsite die Wiederherstellungsschlüssel-ID, um das Wiederherstellungskennwort abzurufen und das Laufwerk zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="aedeb-115">On the MBAM administration website, use the recovery key ID to retrieve the recovery password and unlock the drive.</span></span>

4.  <span data-ttu-id="aedeb-116">Wenn das verschobene Laufwerk für die Verwendung eines TPM-Chips auf dem ursprünglichen Computer konfiguriert wurde, müssen Sie nach dem Entsperren des Laufwerks weitere Schritte Unternehmen und den Startvorgang abschließen.</span><span class="sxs-lookup"><span data-stu-id="aedeb-116">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after you unlock the drive and complete the start process.</span></span> <span data-ttu-id="aedeb-117">Öffnen Sie im WinRE-Modus eine Eingabeaufforderung, und verwenden Sie das Tool **manage-bde** , um das Laufwerk zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="aedeb-117">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="aedeb-118">Die Verwendung dieses Tools ist die einzige Möglichkeit, den TPM-plus-PIN-Schutz ohne den ursprünglichen TPM-Chip zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="aedeb-118">The use of this tool is the only way to remove the TPM-plus-PIN protection without the original TPM chip.</span></span>

5.  <span data-ttu-id="aedeb-119">Nachdem der Vorgang abgeschlossen ist, starten Sie das System normal.</span><span class="sxs-lookup"><span data-stu-id="aedeb-119">After the removal is complete, start the system normally.</span></span> <span data-ttu-id="aedeb-120">Der MBAM-Agent setzt die Richtlinie zum Verschlüsseln des Laufwerks mit der TPM-plus-PIN des neuen Computers durch.</span><span class="sxs-lookup"><span data-stu-id="aedeb-120">The MBAM agent will proceed to enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="aedeb-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="aedeb-121">Related topics</span></span>


[<span data-ttu-id="aedeb-122">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="aedeb-122">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





