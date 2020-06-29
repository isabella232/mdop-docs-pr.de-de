---
title: So stellen Sie ein beschädigtes Laufwerk wieder her
description: So stellen Sie ein beschädigtes Laufwerk wieder her
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809616"
---
# <span data-ttu-id="fcb68-103">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="fcb68-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="fcb68-104">Zum Wiederherstellen eines beschädigten Laufwerks, das von BitLocker geschützt ist, muss ein Helpdesk-Benutzer für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) eine Wiederherstellungsschlüssel-Paketdatei erstellen.</span><span class="sxs-lookup"><span data-stu-id="fcb68-104">To recover a corrupted drive protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) Help Desk user will need to create a recovery key package file.</span></span> <span data-ttu-id="fcb68-105">Diese Paketdatei kann dann auf den Computer kopiert werden, auf dem sich das beschädigte Laufwerk befindet, und dann zum Wiederherstellen des Laufwerks verwendet.</span><span class="sxs-lookup"><span data-stu-id="fcb68-105">This package file can then be copied to the computer that contains the corrupted drive, and then used to recover the drive.</span></span> <span data-ttu-id="fcb68-106">Gehen Sie wie folgt vor, um die erforderlichen Schritte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fcb68-106">Use the following procedure for the steps needed to do this.</span></span>

<span data-ttu-id="fcb68-107">**Wichtig**  Um einen möglichen Datenverlust zu vermeiden, wird dringend empfohlen, dass Sie die Hilfe zu "reparieren-BDE" lesen und klar verstehen, wie Sie den Befehl verwenden, bevor Sie die folgenden Anweisungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcb68-107">**Important** To avoid a potential loss of data, it is strongly recommended that you read the “repair-bde” help and clearly understand how to use the command before completing the following instructions.</span></span>

 

**<span data-ttu-id="fcb68-108">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="fcb68-108">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="fcb68-109">Wenn Sie das für die Wiederherstellung eines beschädigten Laufwerks erforderliche Wiederherstellungsschlüssel Paket erstellen möchten, starten Sie einen Webbrowser, und öffnen Sie die Website MBAM-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="fcb68-109">To create the recovery key package necessary to recover a corrupted drive, start a web browser and open the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="fcb68-110">Wählen Sie im linken Navigationsbereich **Drive Recovery** aus.</span><span class="sxs-lookup"><span data-stu-id="fcb68-110">Select **Drive Recovery** from the left navigation pane.</span></span> <span data-ttu-id="fcb68-111">Geben Sie den Domänennamen des Benutzers, den Benutzernamen, den Grund für die Freigabe des Laufwerks und die Wiederherstellungskennwort-ID des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="fcb68-111">Enter the user’s domain name, user name, reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="fcb68-112">**Hinweis**  Wenn Sie Mitglied der Rolle "Helpdesk-Administratoren" sind, müssen Sie den Domänennamen oder Benutzernamen des Benutzers nicht eingeben.</span><span class="sxs-lookup"><span data-stu-id="fcb68-112">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="fcb68-113">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="fcb68-113">Click **Submit**.</span></span> <span data-ttu-id="fcb68-114">Der Wiederherstellungsschlüssel wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fcb68-114">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="fcb68-115">Klicken Sie auf **Speichern**, und wählen Sie dann **Wiederherstellungsschlüssel Paket**aus.</span><span class="sxs-lookup"><span data-stu-id="fcb68-115">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="fcb68-116">Das Wiederherstellungsschlüssel Paket wird auf Ihrem Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="fcb68-116">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="fcb68-117">Kopieren Sie das Wiederherstellungsschlüssel Paket auf den Computer mit dem beschädigten Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="fcb68-117">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="fcb68-118">Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="fcb68-118">Open an elevated command prompt.</span></span> <span data-ttu-id="fcb68-119">Klicken Sie dazu auf **Start** , und geben Sie `cmd` im **Feld Programme und Dateien durchsuchen**ein.</span><span class="sxs-lookup"><span data-stu-id="fcb68-119">To do this, click **Start** and type `cmd` in the **Search programs and files box**.</span></span> <span data-ttu-id="fcb68-120">Klicken Sie mit der rechten Maustaste auf **cmd.exe** , und wählen Sie **als Administrator ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="fcb68-120">Right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="fcb68-121">Geben Sie an der Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="fcb68-121">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="fcb68-122">**Hinweis**  Ersetzen Sie das &lt; festgelegte Laufwerk &gt; durch ein verfügbares Festplattenlaufwerk, auf dem der freie Speicherplatz gleich oder größer als die Daten auf dem beschädigten Laufwerk ist.</span><span class="sxs-lookup"><span data-stu-id="fcb68-122">**Note** Replace &lt;fixed drive&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="fcb68-123">Daten auf dem beschädigten Laufwerk werden wiederhergestellt und auf das festgelegte Festplattenlaufwerk verschoben.</span><span class="sxs-lookup"><span data-stu-id="fcb68-123">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     

## <span data-ttu-id="fcb68-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="fcb68-124">Related topics</span></span>


[<span data-ttu-id="fcb68-125">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="fcb68-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





