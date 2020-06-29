---
title: So setzen Sie eine TPM-Sperre zurück
description: So setzen Sie eine TPM-Sperre zurück
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810924"
---
# <span data-ttu-id="25e72-103">So setzen Sie eine TPM-Sperre zurück</span><span class="sxs-lookup"><span data-stu-id="25e72-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="25e72-104">Das Feature für die Wiederherstellung verschlüsselter Laufwerke in Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) umfasst sowohl die Erfassung und Speicherung von Daten als auch die Verfügbarkeit für Tools, die für die Verwaltung des Trusted Platform Module (TPM) erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="25e72-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are needed to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="25e72-105">In diesem Thema wird erläutert, wie Sie auf der Website "Verwaltung und Überwachung" auf das System für die zentrale Schlüsselwiederherstellung zugreifen können, das eine TPM-Besitzerkennwort-Datei bereitstellen kann, wenn eine Computer-ID und eine zugeordnete Benutzerkennung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="25e72-105">This topic covers how to access the centralized Key Recovery data system in the Administration and Monitoring website, which can provide a TPM owner password file when a computer ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="25e72-106">Eine TPM-Sperrung kann auftreten, wenn ein Benutzer die falsche PIN zu oft eingibt.</span><span class="sxs-lookup"><span data-stu-id="25e72-106">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="25e72-107">Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperren von Hersteller zu Hersteller variieren.</span><span class="sxs-lookup"><span data-stu-id="25e72-107">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="25e72-108">Sie können eine TPM-Sperrung nur zurücksetzen, wenn MBAM das TPM besitzt.</span><span class="sxs-lookup"><span data-stu-id="25e72-108">You can reset a TPM lockout only if MBAM owns the TPM.</span></span>

**<span data-ttu-id="25e72-109">So setzen Sie eine TPM-Sperrung zurück</span><span class="sxs-lookup"><span data-stu-id="25e72-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="25e72-110">Öffnen Sie einen Webbrowser, und navigieren Sie zur Websiteverwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="25e72-110">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="25e72-111">Wählen Sie im linken Navigationsbereich **TPM verwalten** aus, um die Seite **TPM verwalten** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="25e72-111">In the left navigation pane, select **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="25e72-112">Geben Sie den vollqualifizierten Domänennamen für den Computer und den Computernamen ein, und geben Sie die Windows-Anmeldedomäne des Benutzers und den Benutzernamen des Benutzers ein, um die TPM-Besitzerkennwort-Datei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="25e72-112">Enter the fully qualified domain name for the computer and the computer name, and enter the user’s Windows logon domain and the user’s user name to retrieve the TPM owner password file.</span></span>

4.  <span data-ttu-id="25e72-113">Wählen Sie aus der Liste **Grund für das Anfordern einer TPM-Besitzerkennwort-Datei** einen Grund für die Anforderung aus, und klicken Sie auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="25e72-113">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="25e72-114">MBAM gibt eine der folgenden Optionen zurück:</span><span class="sxs-lookup"><span data-stu-id="25e72-114">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="25e72-115">Eine Fehlermeldung, wenn keine übereinstimmende TPM-Besitzerkennwort-Datei gefunden wurde</span><span class="sxs-lookup"><span data-stu-id="25e72-115">An error message, if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="25e72-116">Die TPM-Besitzerkennwort-Datei für den übermittelten Computer</span><span class="sxs-lookup"><span data-stu-id="25e72-116">The TPM owner password file for the submitted computer</span></span>

    **<span data-ttu-id="25e72-117">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="25e72-117">Note</span></span>**  
    <span data-ttu-id="25e72-118">Wenn Sie ein erweiterter Helpdesk-Benutzer sind, sind die Felder Benutzerdomäne und Benutzer-ID nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="25e72-118">If you are an Advanced Helpdesk user, the user domain and user ID fields are not required.</span></span>



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. <span data-ttu-id="25e72-119">Wenn Sie das Kennwort in einer TPM-Datei speichern möchten, klicken Sie auf die Schaltfläche **Speichern** .</span><span class="sxs-lookup"><span data-stu-id="25e72-119">To save the password to a .tpm file, click the **Save** button.</span></span>

   <span data-ttu-id="25e72-120">Der Benutzer führt die TPM-Verwaltungskonsole aus, wählt die Option **TPM-Sperrung zurücksetzen** aus, und stellt die TPM-Besitzerkennwort-Datei bereit, um die TPM-Sperrung zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="25e72-120">The user will run the TPM management console, select the **Reset TPM lockout** option, and provide the TPM owner password file to reset the TPM lockout.</span></span>

   **<span data-ttu-id="25e72-121">Wichtig</span><span class="sxs-lookup"><span data-stu-id="25e72-121">Important</span></span>**  
   <span data-ttu-id="25e72-122">Helpdesk-Administratoren sollten Endbenutzern den TPM-Hashwert oder die TPM-Besitzerkennwort-Datei nicht zuweisen.</span><span class="sxs-lookup"><span data-stu-id="25e72-122">Help Desk administrators should not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="25e72-123">Die TPM-Informationen werden nicht geändert, daher kann es ein Sicherheitsrisiko darstellen, wenn die Datei an Endbenutzer übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="25e72-123">The TPM information does not change, so it could pose a security risk if the file is given to end users.</span></span>



## <span data-ttu-id="25e72-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="25e72-124">Related topics</span></span>


[<span data-ttu-id="25e72-125">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="25e72-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









