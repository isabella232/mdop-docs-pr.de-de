---
title: So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können
description: So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811539"
---
# <span data-ttu-id="66d2a-103">So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können</span><span class="sxs-lookup"><span data-stu-id="66d2a-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="66d2a-104">Wenn Endbenutzer von BitLocker von Windows gesperrt werden, weil Sie Ihr Kennwort oder Ihre PIN vergessen haben, oder weil Sie die Betriebssystemdateien geändert oder das BIOS oder das Trusted Platform Module (TPM) geändert haben, können Sie das Self-Service-Portal verwenden, um wieder Zugriff auf Windows zu erhalten, ohne den Helpdesk um Unterstützung bitten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="66d2a-104">If end users get locked out of Windows by BitLocker because they forgot their password or PIN, or because they changed operating system files or changed the BIOS or the Trusted Platform Module (TPM), they can use the Self-Service Portal to regain access to Windows without having to ask their Help Desk for assistance.</span></span>

<span data-ttu-id="66d2a-105">**Hinweis**  Wenn der IT-Administrator einen Timeout für den IIS-Sitzungszustand konfiguriert hat, wird eine Meldung 60 Sekunden vor dem Timeout angezeigt.</span><span class="sxs-lookup"><span data-stu-id="66d2a-105">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed 60 seconds prior to the time-out.</span></span>

 

<span data-ttu-id="66d2a-106">**Hinweis**  Diese Anweisungen sind für und aus der Perspektive von Endbenutzern geschrieben.</span><span class="sxs-lookup"><span data-stu-id="66d2a-106">**Note** These instructions are written for and from the perspective of end users.</span></span>

 

**<span data-ttu-id="66d2a-107">So verwenden Sie das Self-Service-Portal zum wieder Zugriff auf einen Computer</span><span class="sxs-lookup"><span data-stu-id="66d2a-107">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="66d2a-108">Geben Sie im Feld **Wiederherstellungs KeyId** eine der 32-stelligen BitLocker-Schlüssel-IDs ein, die auf dem BitLocker-Wiederherstellungsbildschirm Ihres Computers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="66d2a-108">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span>

    <span data-ttu-id="66d2a-109">**Hinweis**  Wenn die ersten acht Ziffern mit mehreren Schlüsseln übereinstimmen, wird eine Meldung angezeigt, in der Sie alle 32-Ziffern der Wiederherstellungsschlüssel-ID eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="66d2a-109">**Note** If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

     

2.  <span data-ttu-id="66d2a-110">Wählen Sie im Feld **Grund** einen Grund für Ihre Anforderung für den Wiederherstellungsschlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="66d2a-110">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="66d2a-111">Klicken Sie auf **Schlüssel abrufen**.</span><span class="sxs-lookup"><span data-stu-id="66d2a-111">Click **Get Key**.</span></span> <span data-ttu-id="66d2a-112">Ihr BitLocker-Wiederherstellungsschlüssel wird im Feld "Ihr BitLocker-Wiederherstellungsschlüssel" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="66d2a-112">Your BitLocker recovery key is displayed in the “Your BitLocker Recovery Key” field.</span></span>

4.  <span data-ttu-id="66d2a-113">Geben Sie den 48-stelligen Code in den BitLocker-Wiederherstellungsbildschirm auf dem Computer ein, um wieder Zugriff auf den Computer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="66d2a-113">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>

## <span data-ttu-id="66d2a-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="66d2a-114">Related topics</span></span>


[<span data-ttu-id="66d2a-115">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="66d2a-115">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





