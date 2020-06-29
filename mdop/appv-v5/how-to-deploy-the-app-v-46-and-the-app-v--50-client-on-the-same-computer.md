---
title: Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf demselben Computer
description: Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf demselben Computer
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805534"
---
# <span data-ttu-id="d98eb-103">Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf demselben Computer</span><span class="sxs-lookup"><span data-stu-id="d98eb-103">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>

<span data-ttu-id="d98eb-104">**Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen.</span><span class="sxs-lookup"><span data-stu-id="d98eb-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="d98eb-105">Im folgenden wird davon ausgegangen, dass der App-V 4,6 SP3-Client bereits installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d98eb-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="d98eb-106">Verwenden Sie die folgenden Informationen, um den App-v 5,0-Client (vorzugsweise mit den neuesten Service Packs und Hotfixes) und dem App-v 4.6 SP3-Client auf demselben Computer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d98eb-106">Use the following information to install the App-V 5.0 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP3 client on the same computer.</span></span> <span data-ttu-id="d98eb-107">Unterstützte Versionen, Anforderungen und andere Planungsinformationen finden Sie unter [Planen der Migration von einer früheren Version von App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="d98eb-107">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span></span>

**<span data-ttu-id="d98eb-108">So stellen Sie den App-v 5,0-Client und den App-v 4,6-Client auf demselben Computer bereit</span><span class="sxs-lookup"><span data-stu-id="d98eb-108">To deploy the App-V 5.0 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="d98eb-109">Installieren Sie den App-v 5,0 SP3-Client auf dem Computer, auf dem die APP-v 4,6-Version des Clients ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d98eb-109">Install the App-V 5.0 SP3 client on the computer that is running the App-V 4.6 version of the client.</span></span> <span data-ttu-id="d98eb-110">Um optimale Ergebnisse zu erzielen, empfehlen wir, alle verfügbaren Updates für den App-V 5,0 SP3-Client zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d98eb-110">For best results, we recommend that you install all available updates to the App-V 5.0 SP3 client.</span></span>

2.  <span data-ttu-id="d98eb-111">Konvertieren Sie die Pakete allmählich, oder führen Sie eine Neusequenzierung durch.</span><span class="sxs-lookup"><span data-stu-id="d98eb-111">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="d98eb-112">Verwenden Sie zum Konvertieren der Pakete den App-v 5,0-Paket Konverter, und konvertieren Sie die erforderlichen Pakete in das App-v 5,0-Dateiformat (**AppV**).</span><span class="sxs-lookup"><span data-stu-id="d98eb-112">To convert the packages, use the App-V 5.0 package converter and convert the required packages to the App-V 5.0 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="d98eb-113">Um die Pakete neu zu sequenzieren, sollten Sie die neueste Version des Sequencers verwenden, um optimale Ergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="d98eb-113">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="d98eb-114">Weitere Informationen zum Veröffentlichen von Paketen finden Sie unter [Veröffentlichen eines Pakets mithilfe der Verwaltungskonsole](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="d98eb-114">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

3.  <span data-ttu-id="d98eb-115">Bereitstellen von Paketen auf den Clientcomputern</span><span class="sxs-lookup"><span data-stu-id="d98eb-115">Deploy packages to the client computers.</span></span>

4.  <span data-ttu-id="d98eb-116">Konvertieren Sie nach Bedarf Erweiterungspunkte.</span><span class="sxs-lookup"><span data-stu-id="d98eb-116">Convert extension points, as needed.</span></span> <span data-ttu-id="d98eb-117">Weitere Informationen finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="d98eb-117">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="d98eb-118">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.0-Paket für alle Benutzer eines bestimmten Computers</span><span class="sxs-lookup"><span data-stu-id="d98eb-118">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="d98eb-119">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="d98eb-119">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [<span data-ttu-id="d98eb-120">So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="d98eb-120">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  <span data-ttu-id="d98eb-121">Testen Sie, ob Ihre App-V 5,0-Pakete erfolgreich sind, und entfernen Sie dann die 4,6-Pakete.</span><span class="sxs-lookup"><span data-stu-id="d98eb-121">Test that your App-V 5.0 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="d98eb-122">Wenn Sie den Benutzerstatus Ihrer Clientcomputer überprüfen möchten, empfehlen wir, dass Sie die [Virtualisierung der Benutzeroberfläche](https://technet.microsoft.com/library/dn458947.aspx) oder ein anderes Tool für die Benutzer Umgebungsverwaltung verwenden.</span><span class="sxs-lookup"><span data-stu-id="d98eb-122">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="d98eb-123">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="d98eb-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="d98eb-124">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="d98eb-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="d98eb-125">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="d98eb-125">Got an App-V issue?</span></span>** <span data-ttu-id="d98eb-126">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="d98eb-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="d98eb-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d98eb-127">Related topics</span></span>


[<span data-ttu-id="d98eb-128">Planen der Migration von einer früheren Version von App-V</span><span class="sxs-lookup"><span data-stu-id="d98eb-128">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v.md)

[<span data-ttu-id="d98eb-129">Bereitstellen von App-V 5.0-Sequencer und -Client</span><span class="sxs-lookup"><span data-stu-id="d98eb-129">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





