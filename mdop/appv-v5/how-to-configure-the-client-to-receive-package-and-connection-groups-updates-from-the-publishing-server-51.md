---
title: So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver
description: So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver
author: dansimp
ms.assetid: 23b2d03a-20ce-4973-99ee-748f3b682207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 034cf5255d75bbaf6a5e65357bd5b3d472344f03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805693"
---
# <span data-ttu-id="a81e2-103">So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="a81e2-103">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>


<span data-ttu-id="a81e2-104">Das Bereitstellen von Paketen und Verbindungsgruppen mit dem App-V 5,1-Veröffentlichungsserver ist hilfreich, da es eine Einzelpunkt Verwaltung und eine große Skalierbarkeit bietet.</span><span class="sxs-lookup"><span data-stu-id="a81e2-104">Deploying packages and connection groups using the App-V 5.1 publishing server is helpful because it offers single-point management and high scalability.</span></span>

<span data-ttu-id="a81e2-105">Führen Sie die folgenden Schritte aus, um den App-V 5,1-Client so zu konfigurieren, dass Updates vom Veröffentlichungsserver empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="a81e2-105">Use the following steps to configure the App-V 5.1 client to receive updates from the publishing server.</span></span>

<span data-ttu-id="a81e2-106">**Hinweis**  Für die folgenden Verfahren wurde der Verwaltungsserver auf einem Computer mit dem Namen " **MyMgmtSrv**" installiert, und der Veröffentlichungsserver wurde auf einem Computer mit dem Namen " **MyPubSrv**" installiert.</span><span class="sxs-lookup"><span data-stu-id="a81e2-106">**Note** For the following procedures the management server was installed on a computer named **MyMgmtSrv**, and the publishing server was installed on a computer named **MyPubSrv**.</span></span>

 

**<span data-ttu-id="a81e2-107">So konfigurieren Sie den App-V 5,1-Client für den Empfang von Updates vom Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="a81e2-107">To configure the App-V 5.1 client to receive updates from the publishing server</span></span>**

1.  <span data-ttu-id="a81e2-108">Stellen Sie die App-V 5,1-Verwaltungs-und-Veröffentlichungsserver bereit, und fügen Sie die erforderlichen Pakete und Verbindungsgruppen hinzu.</span><span class="sxs-lookup"><span data-stu-id="a81e2-108">Deploy the App-V 5.1 management and publishing servers, and add the required packages and connection groups.</span></span> <span data-ttu-id="a81e2-109">Weitere Informationen zum Hinzufügen von Paketen und Verbindungsgruppen finden Sie unter so wird es [gemacht: Hinzufügen oder Aktualisieren von Paketen mithilfe der Verwaltungskonsole](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) und [Erstellen einer Verbindungsgruppe](how-to-create-a-connection-group51.md).</span><span class="sxs-lookup"><span data-stu-id="a81e2-109">For more information about adding packages and connection groups, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) and [How to Create a Connection Group](how-to-create-a-connection-group51.md).</span></span>

2.  <span data-ttu-id="a81e2-110">Um die Verwaltungskonsole zu öffnen, klicken Sie auf den folgenden Link, öffnen Sie einen Browser, und geben Sie Folgendes ein: http://MyMgmtSrv/AppvManagement/Console.html in einem Webbrowser, und importieren, veröffentlichen und berechtigen Sie alle Pakete und Verbindungsgruppen, die für eine bestimmte Gruppe von Benutzern erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a81e2-110">To open the management console click the following link, open a browser and type the following: http://MyMgmtSrv/AppvManagement/Console.html in a web browser, and import, publish, and entitle all the packages and connection groups which will be necessary for a particular set of users.</span></span>

3.  <span data-ttu-id="a81e2-111">Öffnen Sie auf dem Computer, auf dem der App-V 5,1-Client ausgeführt wird, eine erweiterte PowerShell-Eingabeaufforderung, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="a81e2-111">On the computer running the App-V 5.1 client, open an elevated PowerShell command prompt, run the following command:</span></span>

    **<span data-ttu-id="a81e2-112">Add-AppvPublishingServer-Name ABC-URL http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="a81e2-112">Add-AppvPublishingServer -Name ABC -URL http:// MyPubSrv/AppvPublishing</span></span>**

    <span data-ttu-id="a81e2-113">Mit diesem Befehl wird der angegebene Veröffentlichungsserver konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a81e2-113">This command will configure the specified publishing server.</span></span> <span data-ttu-id="a81e2-114">Es sollte eine Ausgabe ähnlich der folgenden angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="a81e2-114">You should see output similar to the following:</span></span>

    <span data-ttu-id="a81e2-115">ID: 1</span><span class="sxs-lookup"><span data-stu-id="a81e2-115">Id : 1</span></span>

    <span data-ttu-id="a81e2-116">SetByGroupPolicy: falsch</span><span class="sxs-lookup"><span data-stu-id="a81e2-116">SetByGroupPolicy : False</span></span>

    <span data-ttu-id="a81e2-117">Name: ABC</span><span class="sxs-lookup"><span data-stu-id="a81e2-117">Name : ABC</span></span>

    <span data-ttu-id="a81e2-118">URL: http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="a81e2-118">URL : http:// MyPubSrv/AppvPublishing</span></span>

    <span data-ttu-id="a81e2-119">GlobalRefreshEnabled: falsch</span><span class="sxs-lookup"><span data-stu-id="a81e2-119">GlobalRefreshEnabled : False</span></span>

    <span data-ttu-id="a81e2-120">GlobalRefreshOnLogon: falsch</span><span class="sxs-lookup"><span data-stu-id="a81e2-120">GlobalRefreshOnLogon : False</span></span>

    <span data-ttu-id="a81e2-121">GlobalRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="a81e2-121">GlobalRefreshInterval : 0</span></span>

    <span data-ttu-id="a81e2-122">GlobalRefreshIntervalUnit: Tag</span><span class="sxs-lookup"><span data-stu-id="a81e2-122">GlobalRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="a81e2-123">UserRefreshEnabled: true</span><span class="sxs-lookup"><span data-stu-id="a81e2-123">UserRefreshEnabled : True</span></span>

    <span data-ttu-id="a81e2-124">UserRefreshOnLogon: true</span><span class="sxs-lookup"><span data-stu-id="a81e2-124">UserRefreshOnLogon : True</span></span>

    <span data-ttu-id="a81e2-125">UserRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="a81e2-125">UserRefreshInterval : 0</span></span>

    <span data-ttu-id="a81e2-126">UserRefreshIntervalUnit: Tag</span><span class="sxs-lookup"><span data-stu-id="a81e2-126">UserRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="a81e2-127">Die zurückgegebene ID – in diesem Fall 1</span><span class="sxs-lookup"><span data-stu-id="a81e2-127">The returned Id – in this case 1</span></span>

4.  <span data-ttu-id="a81e2-128">Öffnen Sie auf dem Computer, auf dem der App-V 5,1-Client ausgeführt wird, eine PowerShell-Eingabeaufforderung, und geben Sie den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="a81e2-128">On the computer running the App-V 5.1 client, open a PowerShell command prompt, and type the following command:</span></span>

    **<span data-ttu-id="a81e2-129">Synchronisieren-AppvPublishingServer-Server-Nr. 1</span><span class="sxs-lookup"><span data-stu-id="a81e2-129">Sync-AppvPublishingServer -ServerId 1</span></span>**

    <span data-ttu-id="a81e2-130">Der Befehl fragt den Veröffentlichungsserver nach den Paketen und Verbindungsgruppen ab, die für diesen bestimmten Client basierend auf den Berechtigungen für die Pakete und Verbindungsgruppen, die auf dem Verwaltungsserver konfiguriert sind, hinzugefügt oder entfernt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a81e2-130">The command will query the publishing server for the packages and connection groups that need to be added or removed for this particular client based on the entitlements for the packages and connection groups as configured on the management server.</span></span>

    <span data-ttu-id="a81e2-131">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="a81e2-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a81e2-132">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="a81e2-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a81e2-133">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="a81e2-133">Got an App-V issue?</span></span>** <span data-ttu-id="a81e2-134">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a81e2-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a81e2-135">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a81e2-135">Related topics</span></span>


[<span data-ttu-id="a81e2-136">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a81e2-136">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





