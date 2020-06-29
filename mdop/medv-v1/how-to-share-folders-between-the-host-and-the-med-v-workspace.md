---
title: So teilen Sie Ordner zwischen dem Host und dem MED-V-Arbeitsbereich
description: So teilen Sie Ordner zwischen dem Host und dem MED-V-Arbeitsbereich
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811344"
---
# <span data-ttu-id="14f2b-103">So teilen Sie Ordner zwischen dem Host und dem MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="14f2b-103">How to Share Folders Between the Host and the MED-V Workspace</span></span>


<span data-ttu-id="14f2b-104">Sie können Ordner zwischen dem Host und dem MED-V-Arbeitsbereich freigeben.</span><span class="sxs-lookup"><span data-stu-id="14f2b-104">You can share folders between the host and the MED-V workspace.</span></span> <span data-ttu-id="14f2b-105">Die freigegebenen Ordner können wie folgt gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="14f2b-105">The shared folders can be stored on the following:</span></span>

-   <span data-ttu-id="14f2b-106">Ein externer Computer im Netzwerk</span><span class="sxs-lookup"><span data-stu-id="14f2b-106">An external computer on the network</span></span>

-   <span data-ttu-id="14f2b-107">Der Hostcomputer</span><span class="sxs-lookup"><span data-stu-id="14f2b-107">The host computer</span></span>

<span data-ttu-id="14f2b-108">Die folgenden Verfahren veranschaulichen, wie Sie Ordner zwischen dem Host und dem MED-V-Arbeitsbereich freigeben.</span><span class="sxs-lookup"><span data-stu-id="14f2b-108">The following procedures demonstrate how to share folders between the host and the MED-V workspace.</span></span>

**<span data-ttu-id="14f2b-109">So geben Sie im Netzwerk befindliche Ordner frei</span><span class="sxs-lookup"><span data-stu-id="14f2b-109">To share folders located on the network</span></span>**

1.  <span data-ttu-id="14f2b-110">Konfigurieren Sie MED-V im vollständigen Desktopmodus.</span><span class="sxs-lookup"><span data-stu-id="14f2b-110">Configure MED-V in full desktop mode.</span></span>

2.  <span data-ttu-id="14f2b-111">Klicken Sie in MED-V-Verwaltung auf der Registerkarte Netzwerk auf **andere IP-Adresse als Host verwenden (Bridge)**.</span><span class="sxs-lookup"><span data-stu-id="14f2b-111">In MED-V management, on the Network tab, click **Use different IP address than host (Bridge)**.</span></span>

3.  <span data-ttu-id="14f2b-112">Gehen Sie auf dem Hostcomputer wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="14f2b-112">Do the following on the host computer:</span></span>

    1.  <span data-ttu-id="14f2b-113">Klicken Sie in der Systemsteuerung auf **Netzwerkstatus und Aufgaben anzeigen**, und wählen Sie **Netzwerkermittlung** auf **ein aus**.</span><span class="sxs-lookup"><span data-stu-id="14f2b-113">In Control Panel, click **View network status and tasks**, and set **Network discovery** to **On**.</span></span>

    2.  <span data-ttu-id="14f2b-114">Klicken Sie im Startmenü mit der rechten Maustaste auf **Computer**, und klicken Sie auf **Netzlaufwerk zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="14f2b-114">On the Start menu, right-click **Computer**, and click **Map network drive**.</span></span>

    3.  <span data-ttu-id="14f2b-115">Wählen Sie im Dialogfeld **Netzlaufwerk zuordnen** im Feld **Laufwerk** ein Laufwerk aus.</span><span class="sxs-lookup"><span data-stu-id="14f2b-115">In the **Map Network Drive** dialog box, in the **Drive** field, select a drive.</span></span>

        <span data-ttu-id="14f2b-116">**Hinweis**  Stellen Sie sicher, dass derselbe Laufwerkbuchstabe nicht auf beiden Computern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14f2b-116">**Note** Ensure that the same drive letter is not in use on both computers.</span></span>

         

    4.  <span data-ttu-id="14f2b-117">Klicken Sie auf **Browse**.</span><span class="sxs-lookup"><span data-stu-id="14f2b-117">Click **Browse**.</span></span>

    5.  <span data-ttu-id="14f2b-118">Navigieren Sie im Dialogfeld **Ordner suchen** zum freigegebenen Laufwerk, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="14f2b-118">In the **Browse For Folder** dialog box, browse to the shared drive, and click **OK**.</span></span>

    6.  <span data-ttu-id="14f2b-119">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="14f2b-119">Click **Finish**.</span></span>

4.  <span data-ttu-id="14f2b-120">Wiederholen Sie Schritt 3 im MED-V-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="14f2b-120">Repeat step 3 in the MED-V workspace.</span></span> <span data-ttu-id="14f2b-121">Zeigen Sie auf das gleiche Laufwerk wie auf dem Hostcomputer.</span><span class="sxs-lookup"><span data-stu-id="14f2b-121">Point to the same drive as on the host computer.</span></span>

**<span data-ttu-id="14f2b-122">So geben Sie auf dem Host befindliche Ordner frei</span><span class="sxs-lookup"><span data-stu-id="14f2b-122">To share folders located on the host</span></span>**

1.  <span data-ttu-id="14f2b-123">Konfigurieren Sie den Ordner, der mit den entsprechenden Berechtigungen freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="14f2b-123">Configure the folder to be shared with the appropriate permissions.</span></span>

2.  <span data-ttu-id="14f2b-124">Wechseln Sie im MED-V-Arbeitsbereich zu **meine Netzwerkumgebung** , und suchen Sie den freigegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="14f2b-124">From the MED-V workspace, go to **My network places** and locate the shared folder.</span></span>

3.  <span data-ttu-id="14f2b-125">Suchen Sie im MED-V-Arbeitsbereich den freigegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="14f2b-125">From the MED-V workspace, locate the shared folder.</span></span>

<span data-ttu-id="14f2b-126">**Hinweis**  Stellen Sie sicher, dass sich der Host-und der MED-V-Arbeitsbereichs Computer in derselben Domäne oder Arbeitsgruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="14f2b-126">**Note** Ensure that both the host and MED-V workspace computers are in the same domain or workgroup.</span></span>

 

 

 





