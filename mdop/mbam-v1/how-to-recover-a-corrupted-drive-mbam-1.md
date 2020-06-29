---
title: So stellen Sie ein beschädigtes Laufwerk wieder her
description: So stellen Sie ein beschädigtes Laufwerk wieder her
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804607"
---
# <span data-ttu-id="5a574-103">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="5a574-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="5a574-104">Zum Wiederherstellen eines beschädigten Laufwerks, das von BitLocker geschützt wurde, muss ein Microsoft BitLocker-MBAM-Helpdesk-Benutzer eine Wiederherstellungsschlüssel-Paketdatei erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a574-104">To recover a corrupted drive that has been protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) help desk user must create a recovery key package file.</span></span> <span data-ttu-id="5a574-105">Diese Paketdatei kann auf den Computer kopiert werden, auf dem sich das beschädigte Laufwerk befindet, und dann zum Wiederherstellen des Laufwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a574-105">This package file can be copied to the computer that contains the corrupted drive and then used to recover the drive.</span></span> <span data-ttu-id="5a574-106">Gehen Sie dazu wie folgt vor, um dies zu erreichen:</span><span class="sxs-lookup"><span data-stu-id="5a574-106">To accomplish this, use the following procedure.</span></span>

**<span data-ttu-id="5a574-107">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="5a574-107">To Recover a Corrupted Drive</span></span>**

1.  <span data-ttu-id="5a574-108">Öffnen Sie die MBAM-Verwaltungswebsite.</span><span class="sxs-lookup"><span data-stu-id="5a574-108">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="5a574-109">Wählen Sie im Navigationsbereich **Drive Recovery** aus.</span><span class="sxs-lookup"><span data-stu-id="5a574-109">Select **Drive Recovery** from the navigation pane.</span></span> <span data-ttu-id="5a574-110">Geben Sie den Domänennamen und den Benutzernamen des Benutzers, den Grund für die Freigabe des Laufwerks und die Wiederherstellungskennwort-ID des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="5a574-110">Enter the user’s domain name and user name, the reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="5a574-111">**Hinweis**  Wenn Sie Mitglied der Rolle "Helpdesk-Administratoren" sind, müssen Sie den Domänennamen oder Benutzernamen des Benutzers nicht eingeben.</span><span class="sxs-lookup"><span data-stu-id="5a574-111">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="5a574-112">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="5a574-112">Click **Submit**.</span></span> <span data-ttu-id="5a574-113">Der Wiederherstellungsschlüssel wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5a574-113">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="5a574-114">Klicken Sie auf **Speichern**, und wählen Sie dann **Wiederherstellungsschlüssel Paket**aus.</span><span class="sxs-lookup"><span data-stu-id="5a574-114">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="5a574-115">Das Wiederherstellungsschlüssel Paket wird auf Ihrem Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a574-115">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="5a574-116">Kopieren Sie das Wiederherstellungsschlüssel Paket auf den Computer mit dem beschädigten Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="5a574-116">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="5a574-117">Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="5a574-117">Open an elevated command prompt.</span></span> <span data-ttu-id="5a574-118">Klicken Sie dazu auf **Start** , und geben Sie `cmd` im Feld **Programme und Dateien durchsuchen** ein.</span><span class="sxs-lookup"><span data-stu-id="5a574-118">To do this, click **Start** and type `cmd` in the **Search programs and files** box.</span></span> <span data-ttu-id="5a574-119">Klicken Sie in der Liste mit den Suchergebnissen mit der rechten Maustaste auf **cmd.exe** , und wählen Sie **als Administrator ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="5a574-119">In the search results list, right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="5a574-120">Geben Sie an der Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="5a574-120">At the command prompt, type the following:</span></span>

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="5a574-121">**Hinweis**  &lt;Geben Sie für das festgelegte Laufwerk &gt; im Befehl ein verfügbares Speichergerät an, auf dem der freie Speicherplatz gleich oder größer als die Daten auf dem beschädigten Laufwerk ist.</span><span class="sxs-lookup"><span data-stu-id="5a574-121">**Note** For the &lt;fixed drive&gt; in the command, specify an available storage device that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="5a574-122">Daten auf dem beschädigten Laufwerk werden wiederhergestellt und auf das angegebene festgelegte Laufwerk verschoben.</span><span class="sxs-lookup"><span data-stu-id="5a574-122">Data on the corrupted drive is recovered and moved to the specified fixed drive.</span></span>

     

## <span data-ttu-id="5a574-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5a574-123">Related topics</span></span>


[<span data-ttu-id="5a574-124">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="5a574-124">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





