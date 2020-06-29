---
title: Wiederherstellen von Computern mithilfe von DaRT 8.0
description: Wiederherstellen von Computern mithilfe von DaRT 8.0
author: dansimp
ms.assetid: 0caeb7d9-c1e6-4f32-bc27-157b91630989
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39bab02488252b53deb971d35bc6872c0a2df73b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810813"
---
# <span data-ttu-id="1fda7-103">Wiederherstellen von Computern mithilfe von DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="1fda7-103">Recovering Computers Using DaRT 8.0</span></span>


<span data-ttu-id="1fda7-104">Nach der Bereitstellung des Microsoft Diagnostics and Recovery Toolset (Dart) 8,0-Wiederherstellungsabbilds können Sie Dart 8,0 zum Wiederherstellen von Computern verwenden.</span><span class="sxs-lookup"><span data-stu-id="1fda7-104">After deploying the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image, you can use DaRT 8.0 to recover computers.</span></span> <span data-ttu-id="1fda7-105">Die Informationen in diesem Abschnitt beschreiben die Wiederherstellungsaufgaben, die Sie ausführen können.</span><span class="sxs-lookup"><span data-stu-id="1fda7-105">The information in this section describes the recovery tasks that you can perform.</span></span>

<span data-ttu-id="1fda7-106">Je nachdem, wie Sie das DART-Wiederherstellungsbild bereitstellen, stehen Ihnen verschiedene Methoden zum Starten von DART zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="1fda7-106">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="1fda7-107">Legen Sie eine Dart-Wiederherstellungs-Image-CD,-DVD oder ein USB-Flashlaufwerk in den Problem Computer ein, und verwenden Sie es zum Booten in den Computer.</span><span class="sxs-lookup"><span data-stu-id="1fda7-107">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="1fda7-108">Starten Sie DART von einer Wiederherstellungspartition auf dem Problem Computer.</span><span class="sxs-lookup"><span data-stu-id="1fda7-108">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="1fda7-109">Starten Sie DART von einer Remotepartition im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1fda7-109">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="1fda7-110">Informationen zu den vor-und Nachteilen der einzelnen Methoden finden Sie unter [Planen des Speicherns und Bereitstellen des Dart 8,0-Wiederherstellungsabbilds](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="1fda7-110">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="1fda7-111">Unabhängig davon, welche Methode Sie zum Starten von DART verwenden, müssen Sie das Startgerät im BIOS für die Startoption oder die Optionen aktivieren, die Sie dem Endbenutzer zur Verfügung stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="1fda7-111">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="1fda7-112">**Hinweis**  Je nach Art der Festplatte, Netzwerkadapter und anderer Hardware, die in Ihrer Organisation verwendet wird, ist die Konfiguration des BIOS einzigartig.</span><span class="sxs-lookup"><span data-stu-id="1fda7-112">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

## <span data-ttu-id="1fda7-113">Wiederherstellen eines lokalen Computers mithilfe des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="1fda7-113">Recover a local computer by using the DaRT recovery image</span></span>


<span data-ttu-id="1fda7-114">Wenn Sie einen lokalen Computer mithilfe von DART wiederherstellen möchten, müssen Sie physisch auf dem Computer des Endbenutzers anwesend sein, bei dem Probleme auftreten, bei denen Dart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1fda7-114">To recover a local computer by using DaRT, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

[<span data-ttu-id="1fda7-115">So stellen Sie lokale Computer mit dem DaRT-Wiederherstellungsabbild wieder her</span><span class="sxs-lookup"><span data-stu-id="1fda7-115">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md)

## <span data-ttu-id="1fda7-116">Wiederherstellen eines Remotecomputers mithilfe des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="1fda7-116">Recover a remote computer by using the DaRT recovery image</span></span>


<span data-ttu-id="1fda7-117">Mit der Funktion Remote Verbindung in DART kann ein IT-Administrator die Dart-Tools Remote auf einem Endbenutzercomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fda7-117">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="1fda7-118">Nachdem der Endbenutzer bestimmte Informationen bereitgestellt hat (oder von einem Helpdesk-Fachmann, der auf dem Computer des Endbenutzers arbeitet), kann der IT-Administrator oder der Helpdesk-Mitarbeiter die Kontrolle über den Computer des Endbenutzers übernehmen und die erforderlichen Dart-Tools Remote ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fda7-118">After certain information is provided by the end user (or by a help desk professional working on the end-user computer), the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="1fda7-119">**Wichtig**  Die beiden Computer, die eine Remoteverbindung herstellen, müssen Teil desselben Netzwerks sein.</span><span class="sxs-lookup"><span data-stu-id="1fda7-119">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="1fda7-120">Das Fenster " **Diagnose-und Wiederherstellungs-Toolset** " enthält die Option, Dart auf einem Endbenutzercomputer von einem Administratorcomputer aus Remote auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1fda7-120">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="1fda7-121">Der Endbenutzer öffnet die Dart-Tools auf dem Problem Computer und startet die Remotesitzung durch Klicken auf **Remoteverbindung**.</span><span class="sxs-lookup"><span data-stu-id="1fda7-121">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="1fda7-122">Das Remote Verbindungs Feature auf dem Endbenutzercomputer erstellt die folgenden Verbindungsinformationen: eine Ticketnummer, einen Port und eine Liste aller verfügbaren IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="1fda7-122">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="1fda7-123">Die Ticketnummer und der Port werden nach dem Zufallsprinzip generiert.</span><span class="sxs-lookup"><span data-stu-id="1fda7-123">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="1fda7-124">Der IT-Administrator oder Helpdesk-Mitarbeiter gibt diese Informationen in die **Dart-Remote Verbindungsanzeige** ein, um die Terminaldienste-Verbindung mit dem Endbenutzercomputer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="1fda7-124">The IT administrator or help desk worker enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="1fda7-125">Mit der eingerichteten Terminaldienste-Verbindung kann ein IT-Administrator Remote mit den Dart-Tools auf dem Endbenutzercomputer interagieren.</span><span class="sxs-lookup"><span data-stu-id="1fda7-125">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="1fda7-126">Der Endbenutzercomputer verarbeitet dann die Verbindungsinformationen, teilt seinen Bildschirm und antwortet auf Anweisungen vom Computer des IT-Administrators.</span><span class="sxs-lookup"><span data-stu-id="1fda7-126">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="1fda7-127">So stellen Sie Remotecomputer mit dem DaRT-Wiederherstellungsabbild wieder her</span><span class="sxs-lookup"><span data-stu-id="1fda7-127">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md)

## <span data-ttu-id="1fda7-128">Weitere Ressourcen zum Wiederherstellen von Computern mithilfe von Dart 8,0</span><span class="sxs-lookup"><span data-stu-id="1fda7-128">Other resources for recovering computers using DaRT 8.0</span></span>


[<span data-ttu-id="1fda7-129">Vorgänge für DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="1fda7-129">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





