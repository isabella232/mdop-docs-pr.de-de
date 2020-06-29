---
title: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
description: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810927"
---
# <span data-ttu-id="9beee-103">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="9beee-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="9beee-104">Die verschlüsselten Laufwerk Wiederherstellungsfeatures von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) gewährleisten die Erfassung und Speicherung von Daten und die Verfügbarkeit von Tools für den Zugriff auf ein BitLocker-geschütztes Volume, wenn BitLocker in den Wiederherstellungsmodus wechselt.</span><span class="sxs-lookup"><span data-stu-id="9beee-104">The encrypted drive recovery features of Microsoft BitLocker Administration and Monitoring (MBAM) ensure the capture and storage of data and availability of tools required to access a BitLocker-protected volume when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="9beee-105">Ein von BitLocker geschütztes Volume wechselt in den Wiederherstellungsmodus, wenn eine PIN oder ein Kennwort verloren geht oder vergessen wird oder wenn der TPM-Chip (Trusted Module Platform) Änderungen an den BIOS-oder Startdateien eines Computers erkennt.</span><span class="sxs-lookup"><span data-stu-id="9beee-105">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="9beee-106">Gehen Sie wie folgt vor, um auf das Datensystem für die zentralisierte Schlüsselwiederherstellung zuzugreifen, das ein Wiederherstellungskennwort bereitstellen kann, wenn eine Wiederherstellungskennwort-ID und die zugehörige Benutzerkennung angegeben werden</span><span class="sxs-lookup"><span data-stu-id="9beee-106">Use this procedure to access the centralized key recovery data system, which can provide a recovery password if a recovery password ID and associated user identifier are supplied.</span></span>

**<span data-ttu-id="9beee-107">Wichtig</span><span class="sxs-lookup"><span data-stu-id="9beee-107">Important</span></span>**  
<span data-ttu-id="9beee-108">Die Microsoft BitLocker-Verwaltung und-Überwachung verwendet Wiederherstellungsschlüssel zur einmaligen Verwendung, die bei der Verwendung ablaufen.</span><span class="sxs-lookup"><span data-stu-id="9beee-108">Microsoft BitLocker Administration and Monitoring uses single-use recovery keys that expire upon use.</span></span> <span data-ttu-id="9beee-109">Die einmalige Verwendung eines Wiederherstellungskennworts wird automatisch auf Betriebssystemlaufwerke und Festplatten angewendet.</span><span class="sxs-lookup"><span data-stu-id="9beee-109">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="9beee-110">Auf Wechseldatenträgern wird Sie angewendet, wenn das Laufwerk entfernt und dann auf einem Computer, auf dem die Gruppenrichtlinieneinstellungen aktiviert sind, um Wechseldatenträger zu verwalten, erneut eingefügt und wieder freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9beee-110">On removable drives, it is applied when the drive is removed and then re-inserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="9beee-111">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</span><span class="sxs-lookup"><span data-stu-id="9beee-111">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="9beee-112">Öffnen Sie einen Webbrowser, und navigieren Sie zur Websiteverwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="9beee-112">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="9beee-113">Klicken Sie im Navigationsbereich auf **Laufwerk Wiederherstellung**.</span><span class="sxs-lookup"><span data-stu-id="9beee-113">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="9beee-114">Die Webseite "Zugriff auf verschlüsselte Laufwerke wiederherstellen" wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9beee-114">The “Recover access to an encrypted drive” webpage opens.</span></span>

3.  <span data-ttu-id="9beee-115">Geben Sie die Windows-Anmeldedomäne und den Benutzernamen des Benutzers ein, um die Wiederherstellungsinformationen und die ersten acht Ziffern der Wiederherstellungsschlüssel-ID anzuzeigen, um eine Liste der möglichen übereinstimmenden Wiederherstellungsschlüssel oder der gesamten Wiederherstellungsschlüssel-ID zu erhalten, um den genauen Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="9beee-115">Enter the Windows Logon domain and user name of the user to view recovery information and the first eight digits of the recovery key ID to receive a list of possible matching recovery keys or the entire recovery key ID to receive the exact recovery key.</span></span>

4.  <span data-ttu-id="9beee-116">Wählen Sie eine der vordefinierten Optionen aus der Liste **Grund für Laufwerks Sperrung** aus, und klicken Sie dann auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="9beee-116">Select one of the predefined options from the **Reason for Drive Unlock** list, and then click **Submit**.</span></span>

    **<span data-ttu-id="9beee-117">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9beee-117">Note</span></span>**  
    <span data-ttu-id="9beee-118">Wenn Sie ein MBAM Advanced Helpdesk-Nutzer sind, sind die Benutzerdomänen-und Benutzer-ID-Einträge nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9beee-118">If you are an MBAM Advanced Helpdesk user, the user domain and user ID entries are not required.</span></span>



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. <span data-ttu-id="9beee-119">Wenn Sie das Kennwort kopieren möchten, klicken Sie auf **Schlüssel kopieren**, und fügen Sie dann das Wiederherstellungskennwort in eine e-Mail-Nachricht ein.</span><span class="sxs-lookup"><span data-stu-id="9beee-119">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="9beee-120">Klicken Sie alternativ auf **Speichern** , um das Wiederherstellungskennwort in einer Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9beee-120">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="9beee-121">Wenn der Benutzer das Wiederherstellungskennwort in das System eingibt oder das Wiederherstellungs Paket verwendet, wird das Laufwerk entsperrt.</span><span class="sxs-lookup"><span data-stu-id="9beee-121">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="9beee-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9beee-122">Related topics</span></span>


[<span data-ttu-id="9beee-123">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="9beee-123">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









