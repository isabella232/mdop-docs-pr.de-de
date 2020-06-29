---
title: So stellen Sie ein beschädigtes Laufwerk wieder her
description: So stellen Sie ein beschädigtes Laufwerk wieder her
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809424"
---
# <span data-ttu-id="07958-103">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="07958-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="07958-104">Sie können dieses Verfahren mit der Websiteverwaltung und Überwachung (auch als Helpdesk bezeichnet) verwenden, um ein beschädigtes Laufwerk wiederherzustellen, das durch BitLocker geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="07958-104">You can use this procedure with the Administration and Monitoring Website (also referred to as the Help Desk) Website to recover a corrupted drive that is protected by BitLocker.</span></span> <span data-ttu-id="07958-105">Führen Sie dazu die Aufgaben aus, die in der folgenden Tabelle beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="07958-105">To do this, you will complete the tasks outlined in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="07958-106">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="07958-106">Task</span></span></th>
<th align="left"><span data-ttu-id="07958-107">Details und weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="07958-107">Details and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07958-108">Erstellen Sie eine Wiederherstellungs Schlüsselpaket-Datei, indem Sie auf den <strong> Bereich Drive Recovery </strong> der Verwaltungs-und Überwachungs Website zugreifen.</span><span class="sxs-lookup"><span data-stu-id="07958-108">Create a recovery key package file by accessing the <strong>Drive Recovery</strong> area of the Administration and Monitoring Website.</span></span></p></td>
<td align="left"><p><span data-ttu-id="07958-109">Für den Zugriff auf den <strong> Laufwerk Wiederherstellungs </strong> Bereich müssen Sie der Rolle MBAM Helpdesk-Benutzer oder der MBAM Advanced Helpdesk-Benutzerrolle zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="07958-109">To access the <strong>Drive Recovery</strong> area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="07958-110">Sie haben diesen Rollen möglicherweise unterschiedliche Namen gegeben, als Sie Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="07958-110">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="07958-111">Weitere Informationen finden Sie unter <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> Planen von MBAM 2,5-Gruppen und-Konten </a> .</span><span class="sxs-lookup"><span data-stu-id="07958-111">For more information, see <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)">Planning for MBAM 2.5 Groups and Accounts</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07958-112">Kopieren Sie die Paketdatei auf den Computer, auf dem sich das beschädigte Laufwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="07958-112">Copy the package file to the computer that contains the corrupted drive.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07958-113">Verwenden Sie den <code>repair-bde</code> Befehl, um den Wiederherstellungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="07958-113">Use the <code>repair-bde</code> command to complete the recovery process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="07958-114">Um einen möglichen Datenverlust zu vermeiden, wird dringend empfohlen, den <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> Befehl manage-bde zu überprüfen, </a> bevor Sie ihn verwenden.</span><span class="sxs-lookup"><span data-stu-id="07958-114">To avoid a potential loss of data, it is strongly recommended that you review the <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)">Manage-bde</a> command before using it.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="07958-115">So stellen Sie ein beschädigtes Laufwerk wieder her</span><span class="sxs-lookup"><span data-stu-id="07958-115">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="07958-116">Öffnen Sie einen Webbrowser, und navigieren Sie zur **Website Verwaltung und Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="07958-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="07958-117">Wählen Sie im linken Bereich **Drive Recovery** aus, um die Seite **Wiederherstellen des Zugriffs auf eine verschlüsselte Festplatte** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="07958-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="07958-118">Geben Sie die Windows-Anmeldedomäne und den Benutzernamen des Endbenutzers, den Grund für die Freigabe des Laufwerks und die Wiederherstellungskennwort-ID des Endbenutzers ein.</span><span class="sxs-lookup"><span data-stu-id="07958-118">Enter the end user’s Windows log-on domain and user name, the reason for unlocking the drive, and the end user’s recovery password ID.</span></span>

    <span data-ttu-id="07958-119">**Hinweis**  Wenn Sie Mitglied der Gruppe "Erweiterte Helpdesk-Benutzer" sind, müssen Sie den Domänennamen oder Benutzernamen des Benutzers nicht eingeben.</span><span class="sxs-lookup"><span data-stu-id="07958-119">**Note** If you are a member of the Advanced Helpdesk Users access group, you do not have to enter the user’s domain name or user name.</span></span>

     

4.  <span data-ttu-id="07958-120">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="07958-120">Click **Submit**.</span></span> <span data-ttu-id="07958-121">Der Wiederherstellungsschlüssel wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07958-121">The recovery key will be displayed.</span></span>

5.  <span data-ttu-id="07958-122">Klicken Sie auf **Speichern**, und wählen Sie dann **Wiederherstellungsschlüssel Paket**aus.</span><span class="sxs-lookup"><span data-stu-id="07958-122">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="07958-123">Das Wiederherstellungsschlüssel Paket wird auf Ihrem Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="07958-123">The recovery key package will be created on your computer.</span></span>

6.  <span data-ttu-id="07958-124">Kopieren Sie das Wiederherstellungsschlüssel Paket auf den Computer mit dem beschädigten Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="07958-124">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

7.  <span data-ttu-id="07958-125">Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="07958-125">Open an elevated command prompt.</span></span> <span data-ttu-id="07958-126">Klicken Sie dazu auf **Start** , und geben Sie `cmd` das Textfeld **Programme und Dateien durchsuchen** ein.</span><span class="sxs-lookup"><span data-stu-id="07958-126">To do this, click **Start** and type `cmd` in the **Search programs and files** text box.</span></span> <span data-ttu-id="07958-127">Klicken Sie mit der rechten Maustaste auf **cmd.exe**, und wählen Sie **als Administrator ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="07958-127">Right-click **cmd.exe**, and select **Run as Administrator**.</span></span>

8.  <span data-ttu-id="07958-128">Geben Sie an der Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="07958-128">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="07958-129">**Hinweis**  Ersetzen Sie das &lt; *festgelegte Laufwerk* &gt; durch ein verfügbares Festplattenlaufwerk, auf dem der freie Speicherplatz gleich oder größer als die Daten auf dem beschädigten Laufwerk ist.</span><span class="sxs-lookup"><span data-stu-id="07958-129">**Note** Replace &lt;*fixed drive*&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="07958-130">Daten auf dem beschädigten Laufwerk werden wiederhergestellt und auf das festgelegte Festplattenlaufwerk verschoben.</span><span class="sxs-lookup"><span data-stu-id="07958-130">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     


## <span data-ttu-id="07958-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="07958-131">Related topics</span></span>


[<span data-ttu-id="07958-132">Durchführen der BitLocker-Verwaltung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="07958-132">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="07958-133">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="07958-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="07958-134">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="07958-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="07958-135">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="07958-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





