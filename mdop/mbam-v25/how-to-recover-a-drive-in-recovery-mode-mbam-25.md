---
title: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
description: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809913"
---
# <span data-ttu-id="b407a-103">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="b407a-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="b407a-104">In diesem Thema wird erläutert, wie Sie die Website "Verwaltung und Überwachung" (auch als "Helpdesk" bezeichnet) verwenden, um ein Wiederherstellungskennwort abzurufen, das den Endbenutzern zur Verfügung steht, wenn Ihr mit BitLocker geschütztes Laufwerk in den Wiederherstellungsmodus wechselt.</span><span class="sxs-lookup"><span data-stu-id="b407a-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to get a recovery password to give to end users if their BitLocker-protected drive goes into recovery mode.</span></span> <span data-ttu-id="b407a-105">Laufwerke gehen in den Wiederherstellungsmodus, wenn Benutzer Ihre PIN oder Ihr Kennwort verlieren oder vergessen oder wenn der TPM-Chip (Trusted Module Platform) Änderungen an den BIOS-oder Startdateien eines Computers erkennt.</span><span class="sxs-lookup"><span data-stu-id="b407a-105">Drives go into recovery mode if users lose or forget their PIN or password or if the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="b407a-106">Verwenden Sie zum Abrufen eines Wiederherstellungskennworts den Bereich **Drive Recovery** der Verwaltungs-und Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="b407a-106">To get a recovery password, use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="b407a-107">Sie müssen der MBAM Helpdesk-Benutzerrolle oder der MBAM Advanced Helpdesk-Benutzerrolle zugewiesen sein, um auf diesen Bereich der Website zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="b407a-107">You must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role to access this area of the website.</span></span>

**<span data-ttu-id="b407a-108">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b407a-108">Note</span></span>**  
<span data-ttu-id="b407a-109">Sie haben diesen Rollen möglicherweise unterschiedliche Namen gegeben, als Sie Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b407a-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="b407a-110">Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="b407a-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>



**<span data-ttu-id="b407a-111">Wichtig</span><span class="sxs-lookup"><span data-stu-id="b407a-111">Important</span></span>**  
<span data-ttu-id="b407a-112">Wiederherstellungskennwörter verfallen nach einer einmaligen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="b407a-112">Recovery passwords expire after a single use.</span></span> <span data-ttu-id="b407a-113">Auf Betriebssystemlaufwerken und festen Datenlaufwerken wird die Regel für einmalige Verwendung automatisch angewendet.</span><span class="sxs-lookup"><span data-stu-id="b407a-113">On operating system drives and fixed data drives, the single-use rule is applied automatically.</span></span> <span data-ttu-id="b407a-114">Auf Wechseldatenträgern wird Sie angewendet, wenn das Laufwerk entfernt und dann auf einem Computer, auf dem die Gruppenrichtlinieneinstellungen aktiviert sind, um Wechseldatenträger zu verwalten, erneut eingefügt und wieder freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b407a-114">On removable drives, it is applied when the drive is removed and then reinserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="b407a-115">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="b407a-115">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="b407a-116">Öffnen Sie einen Webbrowser, und navigieren Sie zur **Website Verwaltung und Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="b407a-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="b407a-117">Wählen Sie im linken Bereich **Drive Recovery** aus, um die Seite **Wiederherstellen des Zugriffs auf eine verschlüsselte Festplatte** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b407a-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="b407a-118">Geben Sie die Windows-Anmeldedomäne und den Benutzernamen des Endbenutzers ein, um Wiederherstellungsinformationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b407a-118">Enter the end user’s Windows log-on domain and user name to view recovery information.</span></span>

    **<span data-ttu-id="b407a-119">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b407a-119">Note</span></span>**  
    <span data-ttu-id="b407a-120">Wenn Sie sich in der Gruppe erweiterte Helpdesk-Benutzer von MBAM befinden, sind die Felder Benutzerdomäne und Benutzer-ID nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b407a-120">If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>



4.  <span data-ttu-id="b407a-121">Geben Sie die ersten acht Ziffern der Wiederherstellungsschlüssel-ID ein, um eine Liste möglicher übereinstimmender Wiederherstellungsschlüssel anzuzeigen, oder geben Sie die gesamte Wiederherstellungsschlüssel-ID ein, um den genauen Wiederherstellungsschlüssel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b407a-121">Enter the first eight digits of the recovery key ID to see a list of possible matching recovery keys, or enter the entire recovery key ID to get the exact recovery key.</span></span>

5.  <span data-ttu-id="b407a-122">Wählen Sie in der Liste **Grund für Laufwerks Sperrung** eine der vordefinierten Optionen aus, und klicken Sie dann auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="b407a-122">From the **Reason for Drive Unlock** list, select one of the predefined options, and then click **Submit**.</span></span>

    <span data-ttu-id="b407a-123">MBAM gibt Folgendes zurück:</span><span class="sxs-lookup"><span data-stu-id="b407a-123">MBAM returns the following:</span></span>

    -   <span data-ttu-id="b407a-124">Eine Fehlermeldung, wenn kein passendes Wiederherstellungskennwort gefunden wurde</span><span class="sxs-lookup"><span data-stu-id="b407a-124">An error message if no matching recovery password is found</span></span>

    -   <span data-ttu-id="b407a-125">Mehrere mögliche Übereinstimmungen, wenn der Benutzer über mehrere übereinstimmende Wiederherstellungskennwörter verfügt</span><span class="sxs-lookup"><span data-stu-id="b407a-125">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    -   <span data-ttu-id="b407a-126">Das Wiederherstellungskennwort und das Wiederherstellungs Paket für den übermittelten Benutzer</span><span class="sxs-lookup"><span data-stu-id="b407a-126">The recovery password and recovery package for the submitted user</span></span>

        **<span data-ttu-id="b407a-127">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b407a-127">Note</span></span>**  
        <span data-ttu-id="b407a-128">Wenn Sie ein beschädigtes Laufwerk wiederherstellen, bietet BitLocker mit der Option "Wiederherstellungs Paket" wichtige Informationen, die für die Wiederherstellung des Laufwerks erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b407a-128">If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.</span></span>



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. <span data-ttu-id="b407a-129">Wenn Sie das Kennwort kopieren möchten, klicken Sie auf **Schlüssel kopieren**, und fügen Sie dann das Wiederherstellungskennwort in eine e-Mail-Nachricht ein.</span><span class="sxs-lookup"><span data-stu-id="b407a-129">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="b407a-130">Klicken Sie alternativ auf **Speichern** , um das Wiederherstellungskennwort in einer Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b407a-130">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="b407a-131">Wenn der Benutzer das Wiederherstellungskennwort in das System eingibt oder das Wiederherstellungs Paket verwendet, wird das Laufwerk entsperrt.</span><span class="sxs-lookup"><span data-stu-id="b407a-131">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>



## <span data-ttu-id="b407a-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b407a-132">Related topics</span></span>


[<span data-ttu-id="b407a-133">Durchführen der BitLocker-Verwaltung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b407a-133">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)



## <span data-ttu-id="b407a-134">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="b407a-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b407a-135">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="b407a-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b407a-136">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b407a-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





