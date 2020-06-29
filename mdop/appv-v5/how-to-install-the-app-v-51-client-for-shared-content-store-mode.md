---
title: Installieren des App-V 5.1-Clients für den SCS-Modus (Shared Content Store)
description: Installieren des App-V 5.1-Clients für den SCS-Modus (Shared Content Store)
author: dansimp
ms.assetid: 6f3ecb1b-b5b5-4ae0-8de9-b4ffdfd2c216
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7ce8114a44762180bf9bb0240913dca50c55d31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805438"
---
# <span data-ttu-id="68b3d-103">Installieren des App-V 5.1-Clients für den SCS-Modus (Shared Content Store)</span><span class="sxs-lookup"><span data-stu-id="68b3d-103">How to Install the App-V 5.1 Client for Shared Content Store Mode</span></span>


<span data-ttu-id="68b3d-104">Gehen Sie wie folgt vor, um den Microsoft Application Virtualization (app-v) 5,1-Client so zu installieren, dass der APP-v 5,1 Shared Content Store (SCS)-Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68b3d-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 client so that it uses the App-V 5.1 Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="68b3d-105">Stellen Sie sicher, dass alle erforderlichen Voraussetzungen auf dem Computer installiert sind, auf dem Sie die Installation planen.</span><span class="sxs-lookup"><span data-stu-id="68b3d-105">You should ensure that all required prerequisites are installed on the computer you plan to install to.</span></span> <span data-ttu-id="68b3d-106">Verwenden Sie den folgenden Link, um die [Voraussetzungen für App-V 5,1](app-v-51-prerequisites.md)anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="68b3d-106">Use the following link to see [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

<span data-ttu-id="68b3d-107">**Hinweis**  Bevor Sie diesen Vorgang ausführen, falls erforderlich, deinstallieren Sie eine vorhandene Version des App-V 5,1-Clients.</span><span class="sxs-lookup"><span data-stu-id="68b3d-107">**Note** Before performing this procedure if necessary uninstall any existing version of the App-V 5.1 client.</span></span>

 

<span data-ttu-id="68b3d-108">Weitere Informationen zum SCS-Modus finden Sie unter [freigegebenen Inhaltsspeicher in Microsoft App-V 5,0 – Behind the Scenes](https://go.microsoft.com/fwlink/?LinkId=316879) ( https://go.microsoft.com/fwlink/?LinkId=316879) .</span><span class="sxs-lookup"><span data-stu-id="68b3d-108">For more information about SCS mode, see [Shared Content Store in Microsoft App-V 5.0 – Behind the Scenes](https://go.microsoft.com/fwlink/?LinkId=316879) (https://go.microsoft.com/fwlink/?LinkId=316879).</span></span>

**<span data-ttu-id="68b3d-109">Installieren und Konfigurieren des App-V 5,1-Clients für den SCS-Modus</span><span class="sxs-lookup"><span data-stu-id="68b3d-109">Install and configure the App-V 5.1 client for SCS mode</span></span>**

1.  <span data-ttu-id="68b3d-110">Kopieren Sie die App-V 5,1-Clientinstallationsdateien auf den Computer, auf dem Sie installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="68b3d-110">Copy the App-V 5.1 client installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="68b3d-111">Öffnen Sie eine Befehlszeile, und geben Sie in dem Verzeichnis, in dem die Installationsdateien gespeichert sind, je nach der Version des zu installierenden Clients eine der folgenden Optionen ein:</span><span class="sxs-lookup"><span data-stu-id="68b3d-111">Open a command line and from the directory where the installation files are saved type one of the following options depending on the version of the client you are installing:</span></span>

    -   <span data-ttu-id="68b3d-112">So installieren Sie die RDS-Version des App-V 5,1-Clienttyps: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="68b3d-112">To install the RDS version of the App-V 5.1 client type: **appv\_client\_setup\_rds.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

    -   <span data-ttu-id="68b3d-113">So installieren Sie die Standard Version des App-V 5,1-Clienttyps: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="68b3d-113">To install the standard version of the App-V 5.1 client type: **appv\_client\_setup.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

        <span data-ttu-id="68b3d-114">**Wichtig**  Sie müssen eine unbeaufsichtigte Installation durchführen, oder die Installation schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="68b3d-114">**Important** You must perform a silent installation or the installation will fail.</span></span>

         

2.  <span data-ttu-id="68b3d-115">Nachdem Sie die Installation abgeschlossen haben, können Sie Pakete auf dem Computer bereitstellen, auf dem der Client ausgeführt wird, und alle Paketinhalte werden über das Netzwerk gestreamt.</span><span class="sxs-lookup"><span data-stu-id="68b3d-115">After you have completed the installation you can deploy packages to the computer running the client and all package contents will be streamed across the network.</span></span>

    <span data-ttu-id="68b3d-116">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="68b3d-116">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="68b3d-117">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="68b3d-117">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="68b3d-118">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="68b3d-118">Got an App-V issue?</span></span>** <span data-ttu-id="68b3d-119">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="68b3d-119">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="68b3d-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="68b3d-120">Related topics</span></span>


[<span data-ttu-id="68b3d-121">Bereitstellen von App-V 5.1-Sequencer und -Client</span><span class="sxs-lookup"><span data-stu-id="68b3d-121">Deploying the App-V 5.1 Sequencer and Client</span></span>](deploying-the-app-v-51-sequencer-and-client.md)

 

 




