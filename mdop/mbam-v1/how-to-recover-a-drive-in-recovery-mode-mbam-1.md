---
title: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
description: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804613"
---
# <span data-ttu-id="85c4d-103">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="85c4d-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="85c4d-104">Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) enthält verschlüsselte Wiederherstellungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="85c4d-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes Encrypted Drive Recovery features.</span></span> <span data-ttu-id="85c4d-105">Diese Features gewährleisten die Erfassung und Speicherung von Daten und die Verfügbarkeit von Tools, die für den Zugriff auf ein von BitLocker geschütztes Volume erforderlich sind, wenn BitLocker das Volume in den Wiederherstellungsmodus versetzt.</span><span class="sxs-lookup"><span data-stu-id="85c4d-105">These features ensure the capture and storage of data and availability of tools that are required to access a BitLocker-protected volume when BitLocker puts that volume into recovery mode.</span></span> <span data-ttu-id="85c4d-106">Ein von BitLocker geschütztes Volume wechselt in den Wiederherstellungsmodus, wenn eine PIN oder ein Kennwort verloren geht oder vergessen wird oder wenn der TPM-Chip (Trusted Module Platform) eine Änderung an den BIOS-oder Startdateien des Computers erkennt.</span><span class="sxs-lookup"><span data-stu-id="85c4d-106">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects a change to the computer's BIOS or startup files.</span></span>

<span data-ttu-id="85c4d-107">Gehen Sie wie folgt vor, um auf das Datensystem für die zentrale Schlüsselwiederherstellung zuzugreifen, das ein Wiederherstellungskennwort bereitstellen kann, wenn eine Wiederherstellungskennwort-ID und die zugehörige Benutzerkennung angegeben</span><span class="sxs-lookup"><span data-stu-id="85c4d-107">Use this procedure to access the centralized Key Recovery data system that can provide a recovery password when a recovery password ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="85c4d-108">**Wichtig**  MBAM generiert Wiederherstellungsschlüssel zur einmaligen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="85c4d-108">**Important** MBAM generates single-use recovery keys.</span></span> <span data-ttu-id="85c4d-109">Unter dieser Einschränkung kann ein Wiederherstellungsschlüssel nur einmal verwendet werden und ist dann nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="85c4d-109">Under this limitation, a recovery key can be used only once and then it is no longer valid.</span></span> <span data-ttu-id="85c4d-110">Die einmalige Verwendung eines Wiederherstellungskennworts wird automatisch auf Betriebssystemlaufwerke und Festplatten angewendet.</span><span class="sxs-lookup"><span data-stu-id="85c4d-110">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="85c4d-111">Auf Wechseldatenträgern wird die einmalige Verwendung angewendet, wenn das Laufwerk entfernt und dann auf einem Computer, auf dem die Gruppenrichtlinieneinstellungen aktiviert sind, um Wechseldatenträger zu verwalten, erneut eingefügt und wieder freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="85c4d-111">On removable drives, the single use is applied when the drive is removed and then re-inserted and unlocked on a computer that has the group policy settings activated to manage removable drives.</span></span>

 

**<span data-ttu-id="85c4d-112">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="85c4d-112">To recover a drive in Recovery Mode</span></span>**

1.  <span data-ttu-id="85c4d-113">Öffnen Sie die MBAM-Website.</span><span class="sxs-lookup"><span data-stu-id="85c4d-113">Open the MBAM website.</span></span>

2.  <span data-ttu-id="85c4d-114">Klicken Sie im Navigationsbereich auf **Laufwerk Wiederherstellung**.</span><span class="sxs-lookup"><span data-stu-id="85c4d-114">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="85c4d-115">Die Webseite **Wiederherstellen des Zugriffs auf eine verschlüsselte Festplatte** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="85c4d-115">The **Recover access to an encrypted drive** webpage opens.</span></span>

3.  <span data-ttu-id="85c4d-116">Geben Sie die Windows-Anmeldedomäne des Benutzers und den Benutzernamen sowie die ersten acht Ziffern der Wiederherstellungsschlüssel-ID ein, um eine Liste der möglichen übereinstimmenden Wiederherstellungsschlüssel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="85c4d-116">Enter the user's Windows Logon domain and user name and the first eight digits of the recovery key ID, to receive a list of possible matching recovery keys.</span></span> <span data-ttu-id="85c4d-117">Sie können auch die gesamte Wiederherstellungsschlüssel-ID eingeben, um den genauen Wiederherstellungsschlüssel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="85c4d-117">Alternatively, enter the entire recovery key ID to receive the exact recovery key.</span></span> <span data-ttu-id="85c4d-118">Wählen Sie eine der vordefinierten Optionen in der Dropdownliste **Grund für Laufwerks Sperrung** aus, und klicken Sie dann auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="85c4d-118">Select one of the predefined options in the **Reason for Drive Unlock** drop-down list, and then click **Submit**.</span></span>

    <span data-ttu-id="85c4d-119">**Hinweis**  Wenn Sie ein MBAM Advanced Helpdesk-Nutzer sind, sind die Benutzerdomänen-und Benutzer-ID-Einträge nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="85c4d-119">**Note** If you are an MBAM Advanced Helpdesk User, the user domain and user ID entries are not required.</span></span>

     

4.  <span data-ttu-id="85c4d-120">MBAM gibt Folgendes zurück:</span><span class="sxs-lookup"><span data-stu-id="85c4d-120">MBAM returns the following:</span></span>

    1.  <span data-ttu-id="85c4d-121">Eine Fehlermeldung, wenn kein passendes Wiederherstellungskennwort gefunden wurde</span><span class="sxs-lookup"><span data-stu-id="85c4d-121">An error message if no matching recovery password is found</span></span>

    2.  <span data-ttu-id="85c4d-122">Mehrere mögliche Übereinstimmungen, wenn der Benutzer über mehrere übereinstimmende Wiederherstellungskennwörter verfügt</span><span class="sxs-lookup"><span data-stu-id="85c4d-122">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    3.  <span data-ttu-id="85c4d-123">Das Wiederherstellungskennwort und das Wiederherstellungs Paket für den übermittelten Benutzer</span><span class="sxs-lookup"><span data-stu-id="85c4d-123">The recovery password and recovery package for the submitted user</span></span>

        <span data-ttu-id="85c4d-124">**Hinweis**  Wenn Sie ein beschädigtes Laufwerk wiederherstellen, bietet BitLocker mit der Option "Wiederherstellungs Paket" die wichtigen Informationen, die für den Versuch der Wiederherstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="85c4d-124">**Note** If you are recovering a damaged drive, the recovery package option provides BitLocker with the critical information necessary to attempt the recovery.</span></span>

         

5.  <span data-ttu-id="85c4d-125">Nachdem das Wiederherstellungskennwort und das Wiederherstellungs Paket abgerufen wurden, wird das Wiederherstellungskennwort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="85c4d-125">After the recovery password and recovery package are retrieved, the recovery password is displayed.</span></span> <span data-ttu-id="85c4d-126">Wenn Sie das Kennwort kopieren möchten, klicken Sie auf **Schlüssel kopieren**, und fügen Sie dann das Wiederherstellungskennwort in eine e-Mail oder eine andere Textdatei für den temporären Speicher ein.</span><span class="sxs-lookup"><span data-stu-id="85c4d-126">To copy the password, click **Copy Key**, and then paste the recovery password into an email or other text file for temporary storage.</span></span> <span data-ttu-id="85c4d-127">Wenn Sie das Wiederherstellungskennwort in einer Datei speichern möchten, klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="85c4d-127">Or, to save the recovery password to a file, click **Save**.</span></span>

6.  <span data-ttu-id="85c4d-128">Wenn der Benutzer das Wiederherstellungskennwort in das System eingibt oder das Wiederherstellungs Paket verwendet, wird das Laufwerk entsperrt.</span><span class="sxs-lookup"><span data-stu-id="85c4d-128">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="85c4d-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="85c4d-129">Related topics</span></span>


[<span data-ttu-id="85c4d-130">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="85c4d-130">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





