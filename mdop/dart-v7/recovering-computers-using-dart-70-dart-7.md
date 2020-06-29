---
title: Wiederherstellen von Computern mithilfe von DaRT 7.0
description: Wiederherstellen von Computern mithilfe von DaRT 7.0
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809553"
---
# <span data-ttu-id="34b01-103">Wiederherstellen von Computern mithilfe von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="34b01-103">Recovering Computers Using DaRT 7.0</span></span>


<span data-ttu-id="34b01-104">Es gibt zwei Methoden zum Wiederherstellen von Computern mit Microsoft Diagnostics und Recovery Toolset (Dart) 7.</span><span class="sxs-lookup"><span data-stu-id="34b01-104">There are two methods available to recover computers using Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span> <span data-ttu-id="34b01-105">Sie können entweder das DaRT7-Wiederherstellungsabbild lokal ausführen oder das in DaRT7 verfügbare Remote Verbindungs Feature zum Wiederherstellen eines Remotecomputers verwenden.</span><span class="sxs-lookup"><span data-stu-id="34b01-105">You can either run the DaRT7 recovery image locally or use The Remote Connection feature available in DaRT7 to recover a remote computer.</span></span> <span data-ttu-id="34b01-106">Beide Methoden werden in diesem Abschnitt ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="34b01-106">Both methods are described in more detail in this section.</span></span>

## <span data-ttu-id="34b01-107">Wiederherstellen von lokalen Computern mithilfe des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="34b01-107">Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="34b01-108">Wenn Sie einen lokalen Computer mithilfe von DaRT7 wiederherstellen möchten, müssen Sie physisch auf dem Computer des Endbenutzers anwesend sein, bei dem Probleme auftreten, bei denen Dart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="34b01-108">To recover a local computer by using DaRT7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

<span data-ttu-id="34b01-109">Je nachdem, wie Sie das DART-Wiederherstellungsbild bereitstellen, stehen Ihnen verschiedene Methoden zum Starten von DART zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="34b01-109">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="34b01-110">Legen Sie eine Dart-Wiederherstellungs-Image-CD,-DVD oder ein USB-Flashlaufwerk in den Problem Computer ein, und verwenden Sie es zum Booten in den Computer.</span><span class="sxs-lookup"><span data-stu-id="34b01-110">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="34b01-111">Starten Sie DART von einer Wiederherstellungspartition auf dem Problem Computer.</span><span class="sxs-lookup"><span data-stu-id="34b01-111">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="34b01-112">Starten Sie DART von einer Remotepartition im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="34b01-112">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="34b01-113">Informationen zu den vor-und Nachteilen der einzelnen Methoden finden Sie unter [Planen des Speicherns und Bereitstellen des DART 7,0-Wiederherstellungsabbilds](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="34b01-113">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

<span data-ttu-id="34b01-114">Unabhängig davon, welche Methode Sie zum Starten von DART verwenden, müssen Sie das Startgerät im BIOS für die Startoption oder die Optionen aktivieren, die Sie dem Endbenutzer zur Verfügung stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="34b01-114">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="34b01-115">**Hinweis**  Je nach Art der Festplatte, Netzwerkadapter und anderer Hardware, die in Ihrer Organisation verwendet wird, ist die Konfiguration des BIOS einzigartig.</span><span class="sxs-lookup"><span data-stu-id="34b01-115">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

[<span data-ttu-id="34b01-116">So stellen Sie lokale Computer mithilfe des DaRT-Wiederherstellungsabbilds wieder her</span><span class="sxs-lookup"><span data-stu-id="34b01-116">How to Recover Local Computers Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="34b01-117">Wiederherstellen von Remote Computern mithilfe des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="34b01-117">Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="34b01-118">Mit der Funktion Remote Verbindung in DART kann ein IT-Administrator die Dart-Tools Remote auf einem Endbenutzercomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="34b01-118">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="34b01-119">Nachdem der Endbenutzer bestimmte Informationen bereitgestellt hat (oder von einem Helpdesk-Mitarbeiter, der auf dem Endbenutzercomputer arbeitet), kann der IT-Administrator oder Helpdesk-Agent den Computer des Endbenutzers Steuern und die erforderlichen Dart-Tools Remote ausführen.</span><span class="sxs-lookup"><span data-stu-id="34b01-119">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="34b01-120">**Wichtig**  Die beiden Computer, die eine Remoteverbindung herstellen, müssen Teil desselben Netzwerks sein.</span><span class="sxs-lookup"><span data-stu-id="34b01-120">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="34b01-121">Das Fenster " **Diagnose-und Wiederherstellungs-Toolset** " enthält die Option, Dart auf einem Endbenutzercomputer von einem Administratorcomputer aus Remote auszuführen.</span><span class="sxs-lookup"><span data-stu-id="34b01-121">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="34b01-122">Der Endbenutzer öffnet die Dart-Tools auf dem Problem Computer und startet die Remotesitzung durch Klicken auf **Remoteverbindung**.</span><span class="sxs-lookup"><span data-stu-id="34b01-122">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="34b01-123">Das Remote Verbindungs Feature auf dem Endbenutzercomputer erstellt die folgenden Verbindungsinformationen: eine Ticketnummer, einen Port und eine Liste aller verfügbaren IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="34b01-123">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="34b01-124">Die Ticketnummer und der Port werden nach dem Zufallsprinzip generiert.</span><span class="sxs-lookup"><span data-stu-id="34b01-124">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="34b01-125">Der IT-Administrator oder Helpdesk-Agent gibt diese Informationen in die **Dart-Remote Verbindungsanzeige** ein, um die Terminaldienste-Verbindung mit dem Endbenutzercomputer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="34b01-125">The IT administrator or helpdesk agent enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="34b01-126">Mit der eingerichteten Terminaldienste-Verbindung kann ein IT-Administrator Remote mit den Dart-Tools auf dem Endbenutzercomputer interagieren.</span><span class="sxs-lookup"><span data-stu-id="34b01-126">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="34b01-127">Der Endbenutzercomputer verarbeitet dann die Verbindungsinformationen, teilt seinen Bildschirm und antwortet auf Anweisungen vom Computer des IT-Administrators.</span><span class="sxs-lookup"><span data-stu-id="34b01-127">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="34b01-128">So stellen Sie Remotecomputer mithilfe des DaRT-Wiederherstellungsabbilds wieder her</span><span class="sxs-lookup"><span data-stu-id="34b01-128">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="34b01-129">Weitere Ressourcen zum Wiederherstellen von Computern mithilfe von DaRT7</span><span class="sxs-lookup"><span data-stu-id="34b01-129">Other resources for recovering computers using DaRT7</span></span>


[<span data-ttu-id="34b01-130">Vorgänge für DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="34b01-130">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





