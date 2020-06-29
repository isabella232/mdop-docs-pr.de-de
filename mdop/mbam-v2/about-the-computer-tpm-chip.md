---
title: Informationen zum TPM-Chip des Computers
description: Informationen zum TPM-Chip des Computers
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810012"
---
# <span data-ttu-id="36fde-103">Informationen zum TPM-Chip des Computers</span><span class="sxs-lookup"><span data-stu-id="36fde-103">About the Computer TPM Chip</span></span>


<span data-ttu-id="36fde-104">BitLocker bietet zusätzlichen Schutz, wenn es mit einem TPM-Chip (Trusted Platform Module) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36fde-104">BitLocker provides additional protection when it is used with a Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="36fde-105">Der TPM-Chip ist eine Hardwarekomponente, die von den Computerherstellern auf vielen neueren Computern installiert wird.</span><span class="sxs-lookup"><span data-stu-id="36fde-105">The TPM chip is a hardware component that is installed in many newer computers by the computer manufacturers.</span></span> <span data-ttu-id="36fde-106">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verwendet BitLocker zusätzlich zum TPM-Chip, um zusätzlichen Schutz Ihrer Daten zu gewährleisten und sicherzustellen, dass Ihr Computer nicht manipuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="36fde-106">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker, in addition to the TPM chip, to help provide additional protection of your data and to make sure that your computer has not been tampered with.</span></span>

## <span data-ttu-id="36fde-107">Einrichten Ihres TPMs</span><span class="sxs-lookup"><span data-stu-id="36fde-107">How to Set Up Your TPM</span></span>


<span data-ttu-id="36fde-108">Wenn Sie den BitLocker-Laufwerk Verschlüsselungs-Assistenten auf Ihrem Computer starten, überprüft BitLocker nach einem TPM-Chip, wenn Ihre Organisation BitLocker für die Verwendung eines TPM-Chips konfiguriert hat.</span><span class="sxs-lookup"><span data-stu-id="36fde-108">When you start the BitLocker Drive Encryption wizard on your computer, BitLocker checks for a TPM chip if your organization has configured BitLocker to use a TPM chip.</span></span> <span data-ttu-id="36fde-109">Wenn BitLocker einen kompatiblen TPM-Chip findet, werden Sie möglicherweise aufgefordert, Ihren Computer neu zu starten, um den TPM-Chip zur Verwendung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="36fde-109">If BitLocker finds a compatible TPM chip, you may be prompted to restart your computer to enable the TPM chip for use.</span></span> <span data-ttu-id="36fde-110">Sobald Ihr Computer neu gestartet wurde, folgen Sie den Anweisungen, um den TPM-Chip im BIOS zu konfigurieren (das BIOS ist eine Pre-Windows-Schicht ihrer Computer Software).</span><span class="sxs-lookup"><span data-stu-id="36fde-110">As soon as your computer has restarted, follow the instructions to configure the TPM chip in the BIOS (the BIOS is a pre-Windows layer of your computer software).</span></span>

<span data-ttu-id="36fde-111">Nachdem BitLocker konfiguriert wurde, können Sie auf zusätzliche Informationen zum TPM-Chip zugreifen, indem Sie das Tool BitLocker-Verschlüsselungsoptionen in der Windows-Systemsteuerung öffnen und dann die **TPM-Verwaltung**auswählen.</span><span class="sxs-lookup"><span data-stu-id="36fde-111">After BitLocker is configured, you can access additional information about the TPM chip by opening the BitLocker Encryption Options tool in the Windows Control Panel, and then selecting **TPM Administration**.</span></span>

<span data-ttu-id="36fde-112">**Hinweis**  Sie müssen über Administratorrechte auf dem Computer verfügen, um auf dieses Tool zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="36fde-112">**Note** You must have administrative credentials on your computer to access this tool.</span></span>

 

<span data-ttu-id="36fde-113">Bei einem TPM-Fehler, einer Änderung im BIOS oder bestimmten Windows-Updates sperrt BitLocker Ihren Computer und fordert Sie auf, sich an Ihren Helpdesk zu wenden, um ihn zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="36fde-113">In a TPM failure, a change in the BIOS, or certain Windows Updates, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="36fde-114">Sie müssen den Namen Ihres Computers und die Domäne Ihres Computers angeben.</span><span class="sxs-lookup"><span data-stu-id="36fde-114">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="36fde-115">Der Helpdesk kann Ihnen eine Kennwort-Datei zur Verfügung stellen, mit der Sie Ihren Computer entsperren können.</span><span class="sxs-lookup"><span data-stu-id="36fde-115">Help Desk can give you a password file that can be used to unlock your computer.</span></span>

## <span data-ttu-id="36fde-116">Behandeln von Problemen mit TPM</span><span class="sxs-lookup"><span data-stu-id="36fde-116">Troubleshooting TPM Issues</span></span>


<span data-ttu-id="36fde-117">Wenn ein TPM-Fehler, eine Änderung im BIOS oder bestimmte Windows-Updates auftreten, sperrt BitLocker Ihren Computer und fordert Sie auf, sich an Ihren Helpdesk zu wenden, um ihn zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="36fde-117">If a TPM failure, change in the BIOS, or certain Windows Updates occur, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="36fde-118">Sie müssen den Namen Ihres Computers und die Domäne Ihres Computers angeben.</span><span class="sxs-lookup"><span data-stu-id="36fde-118">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="36fde-119">Der Helpdesk kann Ihnen eine Kennwortdatei zur Verfügung stellen, die Sie zum Entsperren Ihres Computers verwenden können.</span><span class="sxs-lookup"><span data-stu-id="36fde-119">The Help Desk can give you a password file that you can use to unlock your computer.</span></span>

## <span data-ttu-id="36fde-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="36fde-120">Related topics</span></span>


[<span data-ttu-id="36fde-121">Unterstützung für Endbenutzer beim Verwalten von BitLocker</span><span class="sxs-lookup"><span data-stu-id="36fde-121">Helping End Users Manage BitLocker</span></span>](helping-end-users-manage-bitlocker.md)

[<span data-ttu-id="36fde-122">Verwenden Ihrer PIN oder Ihres Kennworts</span><span class="sxs-lookup"><span data-stu-id="36fde-122">Using Your PIN or Password</span></span>](using-your-pin-or-password.md)

 

 





