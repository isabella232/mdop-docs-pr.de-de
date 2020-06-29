---
title: So stellen Sie ein verschobenes Laufwerk wieder her
description: So stellen Sie ein verschobenes Laufwerk wieder her
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810930"
---
# <span data-ttu-id="8efa0-103">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="8efa0-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="8efa0-104">Wenn Sie ein Betriebssystemlaufwerk verschieben, das mithilfe von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verschlüsselt ist, akzeptiert das Laufwerk die PIN, die auf einem vorherigen Computer verwendet wurde, aufgrund der Änderung des TPM-Chips (Trusted Platform Module) nicht.</span><span class="sxs-lookup"><span data-stu-id="8efa0-104">When you move an operating system drive that is encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), the drive will not accept the PIN that was used in a previous computer because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="8efa0-105">Um das verschobene Laufwerk verwenden zu können, benötigen Sie eine Möglichkeit zum Abrufen der Wiederherstellungsschlüssel-ID, um das Wiederherstellungskennwort abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8efa0-105">To use the moved drive, you will need a way to obtain the recovery key ID to retrieve the recovery password.</span></span> <span data-ttu-id="8efa0-106">Gehen Sie wie folgt vor, um ein Laufwerk wiederherzustellen, das verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="8efa0-106">Use the following procedure to recover a drive that has moved.</span></span>

**<span data-ttu-id="8efa0-107">So stellen Sie ein verschobenes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="8efa0-107">To recover a moved drive</span></span>**

1.  <span data-ttu-id="8efa0-108">Starten Sie den Computer auf dem Computer, auf dem sich das verschobene Laufwerk befindet, im Windows Recovery Environment (WinRE)-Modus, oder starten Sie den Computer mit dem Microsoft Diagnostic and Recovery Toolset (Dart).</span><span class="sxs-lookup"><span data-stu-id="8efa0-108">On the computer that contains the moved drive, start the computer in Windows recovery environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="8efa0-109">Nachdem der Computer mit WinRE oder Dart gestartet wurde, behandelt die Microsoft BitLocker-Verwaltung und-Überwachung das verschobene Betriebssystemlaufwerk als Datenlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="8efa0-109">Once the computer has been started with WinRE or DaRT, Microsoft BitLocker Administration and Monitoring will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="8efa0-110">MBAM zeigt dann die Wiederherstellungskennwort-ID des Laufwerks an und fragt nach dem Wiederherstellungskennwort.</span><span class="sxs-lookup"><span data-stu-id="8efa0-110">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="8efa0-111">**Hinweis**  In einigen Fällen können Sie möglicherweise auf **Ich habe die PIN** während des Startvorgangs vergessen klicken und dann in den Wiederherstellungsmodus wechseln, um die Wiederherstellungsschlüssel-ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8efa0-111">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="8efa0-112">Verwenden Sie die Wiederherstellungsschlüssel-ID, um das Wiederherstellungskennwort abzurufen, und Entsperren Sie das Laufwerk über die Websiteverwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="8efa0-112">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="8efa0-113">Wenn das verschobene Laufwerk für die Verwendung eines TPM-Chips auf dem ursprünglichen Computer konfiguriert wurde, müssen Sie nach dem Entsperren des Laufwerks und Abschließen des Startvorgangs weitere Schritte Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="8efa0-113">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after unlocking the drive and completing the start process.</span></span> <span data-ttu-id="8efa0-114">Öffnen Sie im WinRE-Modus eine Eingabeaufforderung, und verwenden Sie das Tool **manage-bde** , um das Laufwerk zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="8efa0-114">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="8efa0-115">Die Verwendung dieses Tools ist die einzige Möglichkeit, die TPM plus-PIN-Beschützer ohne den ursprünglichen TPM-Chip zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8efa0-115">Using this tool is the only way to remove the TPM plus PIN protector without the original TPM chip.</span></span>

5.  <span data-ttu-id="8efa0-116">Starten Sie den Computer nach Abschluss des Umzugs in der Regel.</span><span class="sxs-lookup"><span data-stu-id="8efa0-116">Once the removal is completed, start the computer normally.</span></span> <span data-ttu-id="8efa0-117">Der MBAM-Agent setzt nun die Richtlinie zum Verschlüsseln des Laufwerks mit der TPM-plus-PIN des neuen Computers durch.</span><span class="sxs-lookup"><span data-stu-id="8efa0-117">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="8efa0-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8efa0-118">Related topics</span></span>


[<span data-ttu-id="8efa0-119">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="8efa0-119">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





