---
title: So setzen Sie eine TPM-Sperre zurück
description: So setzen Sie eine TPM-Sperre zurück
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809886"
---
# <span data-ttu-id="d560d-103">So setzen Sie eine TPM-Sperre zurück</span><span class="sxs-lookup"><span data-stu-id="d560d-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="d560d-104">In diesem Thema wird erläutert, wie Sie die Website "Verwaltung und Überwachung" (auch als "Helpdesk" bezeichnet) verwenden, um eine TPM-Sperrung zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d560d-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to reset a TPM lockout.</span></span> <span data-ttu-id="d560d-105">TPM-Sperrungen können auftreten, wenn ein Endbenutzer die falsche PIN zu oft eingibt.</span><span class="sxs-lookup"><span data-stu-id="d560d-105">TPM lockouts can occur if an end user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="d560d-106">Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperren von Hersteller zu Hersteller variieren.</span><span class="sxs-lookup"><span data-stu-id="d560d-106">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="d560d-107">Im Bereich " **TPM verwalten** " auf der Website "Verwaltung und Überwachung" können Sie auf das Datensystem für die zentrale Schlüsselwiederherstellung zugreifen, das eine TPM-Besitzerkennwort-Datei bereitstellt, wenn Sie eine Computer-ID und eine zugehörige Benutzer-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="d560d-107">From the **Manage TPM** area of the Administration and Monitoring Website, you can access the centralized Key Recovery data system, which provides a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

<span data-ttu-id="d560d-108">Für den Zugriff auf den Bereich TPM Verwalten der Verwaltungs-und Überwachungs Website müssen Sie der Rolle MBAM Helpdesk-Benutzer oder der MBAM Advanced Helpdesk-Benutzerrolle zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="d560d-108">To access the Manage TPM area of the Administration and Monitoring Website, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="d560d-109">Diese Rollen sind Gruppen, die Administratoren in Active Directory erstellen.</span><span class="sxs-lookup"><span data-stu-id="d560d-109">These roles are groups that administrators create in Active Directory.</span></span> <span data-ttu-id="d560d-110">Sie können einen beliebigen Namen für diese Gruppen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d560d-110">You can use any name for these groups.</span></span> <span data-ttu-id="d560d-111">Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="d560d-111">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="d560d-112">Informationen zu MBAM und TPM-Besitz finden Sie unter [MBAM 2,5-Sicherheitsüberlegungen](mbam-25-security-considerations.md#bkmk-tpm).</span><span class="sxs-lookup"><span data-stu-id="d560d-112">For information about MBAM and TPM ownership, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

**<span data-ttu-id="d560d-113">So setzen Sie eine TPM-Sperrung zurück</span><span class="sxs-lookup"><span data-stu-id="d560d-113">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="d560d-114">Öffnen Sie einen Webbrowser, und navigieren Sie zur **Website Verwaltung und Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="d560d-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="d560d-115">Klicken Sie im linken Bereich auf **TPM verwalten** , um die Seite **TPM verwalten** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d560d-115">In the left pane, click **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="d560d-116">Geben Sie den vollqualifizierten Domänennamen für den Computer und den Computernamen ein.</span><span class="sxs-lookup"><span data-stu-id="d560d-116">Enter the fully qualified domain name for the computer and the computer name.</span></span>

4.  <span data-ttu-id="d560d-117">Geben Sie die Windows-Anmeldedomäne des Endbenutzers und den Benutzernamen ein, um die TPM-Besitzerkennwort-Datei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d560d-117">Enter the end user’s Windows log-on domain and user name to retrieve the TPM owner password file.</span></span>

    <span data-ttu-id="d560d-118">**Hinweis**  Wenn Sie sich in der Gruppe erweiterte Helpdesk-Benutzer von MBAM befinden, sind die Felder Benutzerdomäne und Benutzer-ID nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d560d-118">**Note** If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="d560d-119">Wählen Sie aus der Liste **Grund für das Anfordern einer TPM-Besitzerkennwort-Datei** einen Grund für die Anforderung aus, und klicken Sie auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="d560d-119">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="d560d-120">MBAM gibt eine der folgenden Optionen zurück:</span><span class="sxs-lookup"><span data-stu-id="d560d-120">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="d560d-121">Eine Fehlermeldung, wenn keine übereinstimmende TPM-Besitzerkennwort-Datei gefunden wurde</span><span class="sxs-lookup"><span data-stu-id="d560d-121">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="d560d-122">Die TPM-Besitzerkennwort-Datei für den übermittelten Computer</span><span class="sxs-lookup"><span data-stu-id="d560d-122">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="d560d-123">Nachdem das TPM-Besitzerkennwort abgerufen wurde, wird das Besitzerkennwort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d560d-123">After the TPM owner password is retrieved, the owner password is displayed.</span></span>

6.  <span data-ttu-id="d560d-124">Wenn Sie das Kennwort in einer TPM-Datei speichern möchten, klicken Sie auf die Schaltfläche **Speichern** .</span><span class="sxs-lookup"><span data-stu-id="d560d-124">To save the password to a .tpm file, click the **Save** button.</span></span>

7.  <span data-ttu-id="d560d-125">Wählen Sie im Bereich **TPM verwalten** auf der **Website Verwaltung und Überwachung**die Option **TPM-Sperrung zurücksetzen** aus, und geben Sie die TPM-Besitzerkennwort-Datei an.</span><span class="sxs-lookup"><span data-stu-id="d560d-125">In the **Manage TPM** area of the **Administration and Monitoring Website**, select the **Reset TPM lockout** option and provide the TPM owner password file.</span></span>

    <span data-ttu-id="d560d-126">Die TPM-Sperrung wird zurückgesetzt, und der Zugriff des Endbenutzers wird wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="d560d-126">The TPM lockout is reset and the end user’s access is restored.</span></span>

    <span data-ttu-id="d560d-127">**Wichtig**  Übergeben Sie die TPM-Hashwerte oder die TPM-Besitzerkennwort-Datei nicht an Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="d560d-127">**Important** Do not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="d560d-128">Da sich die TPM-Informationen nicht ändern, stellt die Datei Endbenutzern ein Sicherheitsrisiko dar.</span><span class="sxs-lookup"><span data-stu-id="d560d-128">Because the TPM information does not change, giving the file to end users creates a security risk.</span></span>

     



## <span data-ttu-id="d560d-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d560d-129">Related topics</span></span>


[<span data-ttu-id="d560d-130">Durchführen der BitLocker-Verwaltung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d560d-130">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="d560d-131">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="d560d-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d560d-132">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="d560d-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d560d-133">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d560d-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





