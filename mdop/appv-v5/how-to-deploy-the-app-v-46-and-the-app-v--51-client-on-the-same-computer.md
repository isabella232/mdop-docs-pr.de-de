---
title: Bereitstellen der APP-v 4,6 und des App-v 5,1-Clients auf demselben Computer
description: Bereitstellen der APP-v 4,6 und des App-v 5,1-Clients auf demselben Computer
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805528"
---
# <span data-ttu-id="28a6c-103">Bereitstellen der APP-v 4,6 und des App-v 5,1-Clients auf demselben Computer</span><span class="sxs-lookup"><span data-stu-id="28a6c-103">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>

<span data-ttu-id="28a6c-104">**Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen.</span><span class="sxs-lookup"><span data-stu-id="28a6c-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="28a6c-105">Verwenden Sie die folgenden Informationen, um den Microsoft Application Virtualization (app-v) 5,1-Client (vorzugsweise mit den neuesten Service Packs und Hotfixes) und dem App-v 4.6 SP2-Client oder dem App-v 4.6 s3-Client auf demselben Computer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="28a6c-105">Use the following information to install the Microsoft Application Virtualization (App-V) 5.1 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP2 client or the App-V 4.6S3 client on the same computer.</span></span> <span data-ttu-id="28a6c-106">Unterstützte Versionen, Anforderungen und andere Planungsinformationen finden Sie unter [Planen der Migration von einer früheren Version von App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="28a6c-106">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span></span>

**<span data-ttu-id="28a6c-107">So stellen Sie den App-v 5,1-Client und den App-v 4,6-Client auf demselben Computer bereit</span><span class="sxs-lookup"><span data-stu-id="28a6c-107">To deploy the App-V 5.1 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="28a6c-108">Installieren Sie die folgende Version des App-v-Clients auf dem Computer, auf dem App-v 4,6 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28a6c-108">Install the following version of the App-V client on the computer that is running App-V 4.6.</span></span>

    -   [<span data-ttu-id="28a6c-109">Microsoft Application Virtualization 4,6 Service Pack 3</span><span class="sxs-lookup"><span data-stu-id="28a6c-109">Microsoft Application Virtualization 4.6 Service Pack 3</span></span>](https://www.microsoft.com/download/details.aspx?id=41187)

2.  <span data-ttu-id="28a6c-110">Installieren Sie den App-v 5,1-Client auf dem Computer, auf dem die APP-v 4,6 SP3-Version des Clients ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28a6c-110">Install the App-V 5.1 client on the computer that is running the App-V 4.6 SP3 version of the client.</span></span> <span data-ttu-id="28a6c-111">Um optimale Ergebnisse zu erzielen, empfehlen wir, alle verfügbaren Updates für den App-V 5,1-Client zu installieren.</span><span class="sxs-lookup"><span data-stu-id="28a6c-111">For best results, we recommend that you install all available updates to the App-V 5.1 client.</span></span>

3.  <span data-ttu-id="28a6c-112">Konvertieren Sie die Pakete allmählich, oder führen Sie eine Neusequenzierung durch.</span><span class="sxs-lookup"><span data-stu-id="28a6c-112">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="28a6c-113">Verwenden Sie zum Konvertieren der Pakete den App-v 5,1-Paket Konverter, und konvertieren Sie die erforderlichen Pakete in das App-v 5,1-Dateiformat (**AppV**).</span><span class="sxs-lookup"><span data-stu-id="28a6c-113">To convert the packages, use the App-V 5.1 package converter and convert the required packages to the App-V 5.1 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="28a6c-114">Um die Pakete neu zu sequenzieren, sollten Sie die neueste Version des Sequencers verwenden, um optimale Ergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="28a6c-114">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="28a6c-115">Weitere Informationen zum Veröffentlichen von Paketen finden Sie unter [Veröffentlichen eines Pakets mithilfe der Verwaltungskonsole](how-to-publish-a-package-by-using-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="28a6c-115">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md).</span></span>

4.  <span data-ttu-id="28a6c-116">Bereitstellen von Paketen auf den Clientcomputern</span><span class="sxs-lookup"><span data-stu-id="28a6c-116">Deploy packages to the client computers.</span></span>

5.  <span data-ttu-id="28a6c-117">Konvertieren Sie nach Bedarf Erweiterungspunkte.</span><span class="sxs-lookup"><span data-stu-id="28a6c-117">Convert extension points, as needed.</span></span> <span data-ttu-id="28a6c-118">Weitere Informationen finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="28a6c-118">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="28a6c-119">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.1-Paket für alle Benutzer eines bestimmten Computers</span><span class="sxs-lookup"><span data-stu-id="28a6c-119">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="28a6c-120">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.1 für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="28a6c-120">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [<span data-ttu-id="28a6c-121">So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="28a6c-121">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  <span data-ttu-id="28a6c-122">Testen Sie, ob Ihre App-V 5,1-Pakete erfolgreich sind, und entfernen Sie dann die 4,6-Pakete.</span><span class="sxs-lookup"><span data-stu-id="28a6c-122">Test that your App-V 5.1 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="28a6c-123">Wenn Sie den Benutzerstatus Ihrer Clientcomputer überprüfen möchten, empfehlen wir, dass Sie die [Virtualisierung der Benutzeroberfläche](https://technet.microsoft.com/library/dn458947.aspx) oder ein anderes Tool für die Benutzer Umgebungsverwaltung verwenden.</span><span class="sxs-lookup"><span data-stu-id="28a6c-123">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="28a6c-124">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="28a6c-124">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="28a6c-125">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="28a6c-125">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="28a6c-126">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="28a6c-126">Got an App-V issue?</span></span>** <span data-ttu-id="28a6c-127">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="28a6c-127">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="28a6c-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="28a6c-128">Related topics</span></span>


[<span data-ttu-id="28a6c-129">Planen der Migration von einer früheren Version von App-V</span><span class="sxs-lookup"><span data-stu-id="28a6c-129">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[<span data-ttu-id="28a6c-130">Bereitstellen von App-V 5.1-Sequencer und -Client</span><span class="sxs-lookup"><span data-stu-id="28a6c-130">Deploying the App-V 5.1 Sequencer and Client</span></span>](deploying-the-app-v-51-sequencer-and-client.md)

 

 





