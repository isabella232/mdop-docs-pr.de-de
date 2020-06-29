---
title: So setzen Sie eine TPM-Sperre zurück
description: So setzen Sie eine TPM-Sperre zurück
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804589"
---
# <span data-ttu-id="da366-103">So setzen Sie eine TPM-Sperre zurück</span><span class="sxs-lookup"><span data-stu-id="da366-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="da366-104">Das Feature für die Wiederherstellung verschlüsselter Laufwerke in Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) umfasst sowohl die Erfassung und Speicherung von Daten als auch die Verfügbarkeit für Tools, die für die Verwaltung des Trusted Platform Module (TPM) erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="da366-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are required to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="da366-105">In diesem Thema wird erläutert, wie Sie auf das Datensystem für die zentralisierte Schlüsselwiederherstellung auf der Website "Bit \ _admmon \ _tlanextref Administration" zugreifen.</span><span class="sxs-lookup"><span data-stu-id="da366-105">This topic covers how to access the centralized Key Recovery data system in the bit\_admmon\_tlanextref administration website.</span></span> <span data-ttu-id="da366-106">Das Schlüssel Wiederherstellungsdaten System kann eine TPM-Besitzerkennwort-Datei bereitstellen, wenn die Computeridentität und die zugehörige Benutzer-ID bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="da366-106">The Key Recovery data system can provide a TPM owner password file when the computer identity and the associated user identifier are supplied.</span></span>

<span data-ttu-id="da366-107">Eine TPM-Sperrung kann auftreten, wenn ein Benutzer zu oft eine falsche PIN eingibt.</span><span class="sxs-lookup"><span data-stu-id="da366-107">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="da366-108">Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperrung auf der Spezifikation des Computerherstellers basiert.</span><span class="sxs-lookup"><span data-stu-id="da366-108">The number of times that a user can enter an incorrect PIN before the TPM lockout is based on the computer manufacturer's specification.</span></span>

**<span data-ttu-id="da366-109">So setzen Sie eine TPM-Sperrung zurück</span><span class="sxs-lookup"><span data-stu-id="da366-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="da366-110">Öffnen Sie die MBAM-Verwaltungswebsite.</span><span class="sxs-lookup"><span data-stu-id="da366-110">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="da366-111">Wählen Sie im Navigationsbereich **TPM verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="da366-111">In the navigation pane, select **Manage TPM**.</span></span> <span data-ttu-id="da366-112">Dadurch wird die Seite **TPM verwalten** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="da366-112">This opens the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="da366-113">Geben Sie den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für den Computer und den Computernamen ein.</span><span class="sxs-lookup"><span data-stu-id="da366-113">Enter the fully qualified domain name (FQDN) for the computer and the computer name.</span></span> <span data-ttu-id="da366-114">Geben Sie die Windows-Anmeldedomäne des Benutzers und den Benutzernamen des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="da366-114">Enter the user’s Windows Logon domain and the user’s user name.</span></span> <span data-ttu-id="da366-115">Wählen Sie eine der vordefinierten Optionen im Dropdownmenü " **Grund für das Anfordern der TPM-Besitzer Kennwortdatei** " aus.</span><span class="sxs-lookup"><span data-stu-id="da366-115">Select one of the predefined options in the **Reason for requesting TPM owner password file** drop-down menu.</span></span> <span data-ttu-id="da366-116">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="da366-116">Click **Submit**.</span></span>

4.  <span data-ttu-id="da366-117">MBAM gibt eine der folgenden Optionen zurück:</span><span class="sxs-lookup"><span data-stu-id="da366-117">MBAM will return one of the following:</span></span>

    -   <span data-ttu-id="da366-118">Eine Fehlermeldung, wenn keine übereinstimmende TPM-Besitzerkennwort-Datei gefunden wurde</span><span class="sxs-lookup"><span data-stu-id="da366-118">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="da366-119">Die TPM-Besitzerkennwort-Datei für den übermittelten Computer</span><span class="sxs-lookup"><span data-stu-id="da366-119">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="da366-120">**Hinweis**  Wenn Sie ein erweiterter Helpdesk-Benutzer sind, sind die Felder Benutzerdomäne und Benutzer-ID nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="da366-120">**Note** If you are an Advanced Helpdesk User, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="da366-121">Beim Abrufen wird das Kennwort des Besitzers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da366-121">Upon retrieval, the owner password is displayed.</span></span> <span data-ttu-id="da366-122">Wenn Sie dieses Kennwort in einer TPM-Datei speichern möchten, klicken Sie auf die Schaltfläche **Speichern** .</span><span class="sxs-lookup"><span data-stu-id="da366-122">To save this password to a .tpm file, click the **Save** button.</span></span>

6.  <span data-ttu-id="da366-123">Der Benutzer führt die TPM-Verwaltungskonsole aus und wählt die TPM- **Sperrungs Option Zurücksetzen** aus, und stellt die TPM-Besitzerkennwort-Datei bereit, um die TPM-Sperrung zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="da366-123">The user will run the TPM management console and select the **Reset TPM lockout** option and provide the TPM owner password file to reset the TPM lockout.</span></span>

## <span data-ttu-id="da366-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="da366-124">Related topics</span></span>


[<span data-ttu-id="da366-125">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="da366-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





