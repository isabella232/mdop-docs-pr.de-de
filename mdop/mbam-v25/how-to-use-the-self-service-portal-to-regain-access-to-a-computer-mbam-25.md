---
title: So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können
description: So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811914"
---
# <span data-ttu-id="668e3-103">So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können</span><span class="sxs-lookup"><span data-stu-id="668e3-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="668e3-104">Das Self-Service-Portal ist eine Website, die von IT-Administratoren im Rahmen Ihrer Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5-Bereitstellung konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="668e3-104">The Self-Service Portal is a website that IT administrators configure as part of their Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 deployment.</span></span> <span data-ttu-id="668e3-105">Die Website ermöglicht es Endbenutzern, den Zugriff auf Ihre Computer unabhängig voneinander wiederherzustellen, wenn Sie von Windows ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="668e3-105">The website enables end users to independently regain access to their computers if they get locked out of Windows.</span></span> <span data-ttu-id="668e3-106">Das Self-Service-Portal erfordert keine Unterstützung durch das Helpdesk-Personal.</span><span class="sxs-lookup"><span data-stu-id="668e3-106">The Self-Service Portal requires no assistance from Help Desk staff.</span></span>

<span data-ttu-id="668e3-107">Die folgenden Anweisungen werden aus der Perspektive der Endbenutzer geschrieben, aber die Informationen können für IT-Administratoren nützlich sein, um Sie zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="668e3-107">The following instructions are written from the perspective of end users, but the information may be useful for IT administrators to understand.</span></span>

<span data-ttu-id="668e3-108">**Wichtig**  Ein Endbenutzer muss sich physisch mindestens einmal erfolgreich am Computer (nicht Remote) angemeldet haben, um seinen Schlüssel über das Self-Service-Portal wiederherstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="668e3-108">**Important** An end user must have physically logged on to the computer (not remotely) at least one time successfully to be able to recover their key using the Self-Service Portal.</span></span> <span data-ttu-id="668e3-109">Andernfalls müssen Sie das Helpdesk-Portal für die Schlüsselwiederherstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="668e3-109">Otherwise, they must use the Helpdesk Portal for key recovery.</span></span>

 

<span data-ttu-id="668e3-110">Endbenutzer können Aussperrungen erfahren, wenn Sie:</span><span class="sxs-lookup"><span data-stu-id="668e3-110">End users may experience lockouts if they:</span></span>

-   <span data-ttu-id="668e3-111">Kennwort oder PIN vergessen</span><span class="sxs-lookup"><span data-stu-id="668e3-111">Forget their password or PIN</span></span>

-   <span data-ttu-id="668e3-112">Ändern von Betriebssystemdateien, dem BIOS oder dem Trusted Platform Module (TPM)</span><span class="sxs-lookup"><span data-stu-id="668e3-112">Change operating system files, the BIOS, or the Trusted Platform Module (TPM)</span></span>

<span data-ttu-id="668e3-113">**Hinweis**  Wenn der IT-Administrator einen Timeout für den IIS-Sitzungszustand konfiguriert hat, wird im Self-Service-Portal 60 Sekunden vor dem Timeout eine Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="668e3-113">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed in the Self-Service Portal 60 seconds prior to the time-out.</span></span>

 

**<span data-ttu-id="668e3-114">So verwenden Sie das Self-Service-Portal zum wieder Zugriff auf einen Computer</span><span class="sxs-lookup"><span data-stu-id="668e3-114">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="668e3-115">Geben Sie im Feld **Wiederherstellungs KeyId** eine der 32-stelligen BitLocker-Schlüssel-IDs ein, die auf dem BitLocker-Wiederherstellungsbildschirm Ihres Computers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="668e3-115">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span> <span data-ttu-id="668e3-116">Wenn die ersten acht Ziffern mit mehreren Schlüsseln übereinstimmen, wird eine Meldung angezeigt, in der Sie alle 32-Ziffern der Wiederherstellungsschlüssel-ID eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="668e3-116">If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

2.  <span data-ttu-id="668e3-117">Wählen Sie im Feld **Grund** einen Grund für Ihre Anforderung für den Wiederherstellungsschlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="668e3-117">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="668e3-118">Klicken Sie auf **Schlüssel abrufen**.</span><span class="sxs-lookup"><span data-stu-id="668e3-118">Click **Get Key**.</span></span> <span data-ttu-id="668e3-119">Ihr BitLocker-Wiederherstellungsschlüssel wird im Feld **BitLocker-Wiederherstellungsschlüssel** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="668e3-119">Your BitLocker recovery key is displayed in the **Your BitLocker Recovery Key** field.</span></span>

4.  <span data-ttu-id="668e3-120">Geben Sie den 48-stelligen Code in den BitLocker-Wiederherstellungsbildschirm auf dem Computer ein, um wieder Zugriff auf den Computer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="668e3-120">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>



## <span data-ttu-id="668e3-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="668e3-121">Related topics</span></span>


[<span data-ttu-id="668e3-122">Durchführen der BitLocker-Verwaltung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="668e3-122">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="668e3-123">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="668e3-123">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="668e3-124">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="668e3-124">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="668e3-125">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="668e3-125">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





