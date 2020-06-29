---
title: So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver
description: So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805690"
---
# <span data-ttu-id="d601a-103">So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="d601a-103">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>


<span data-ttu-id="d601a-104">Das Bereitstellen von Paketen und Verbindungsgruppen mit dem App-V 5,0-Veröffentlichungsserver ist hilfreich, da es eine Einzelpunkt Verwaltung und eine große Skalierbarkeit bietet.</span><span class="sxs-lookup"><span data-stu-id="d601a-104">Deploying packages and connection groups using the App-V 5.0 publishing server is helpful because it offers single-point management and high scalability.</span></span>

<span data-ttu-id="d601a-105">Führen Sie die folgenden Schritte aus, um den App-V 5,0-Client so zu konfigurieren, dass Updates vom Veröffentlichungsserver empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="d601a-105">Use the following steps to configure the App-V 5.0 client to receive updates from the publishing server.</span></span>

<span data-ttu-id="d601a-106">**Hinweis**  Für die folgenden Verfahren wurde der Verwaltungsserver auf einem Computer mit dem Namen " **MyMgmtSrv**" installiert, und der Veröffentlichungsserver wurde auf einem Computer mit dem Namen " **MyPubSrv**" installiert.</span><span class="sxs-lookup"><span data-stu-id="d601a-106">**Note** For the following procedures the management server was installed on a computer named **MyMgmtSrv**, and the publishing server was installed on a computer named **MyPubSrv**.</span></span>

 

**<span data-ttu-id="d601a-107">So konfigurieren Sie den App-V 5,0-Client für den Empfang von Updates vom Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="d601a-107">To configure the App-V 5.0 client to receive updates from the publishing server</span></span>**

1.  <span data-ttu-id="d601a-108">Stellen Sie die App-V 5,0-Verwaltungs-und-Veröffentlichungsserver bereit, und fügen Sie die erforderlichen Pakete und Verbindungsgruppen hinzu.</span><span class="sxs-lookup"><span data-stu-id="d601a-108">Deploy the App-V 5.0 management and publishing servers, and add the required packages and connection groups.</span></span> <span data-ttu-id="d601a-109">Weitere Informationen zum Hinzufügen von Paketen und Verbindungsgruppen finden Sie unter so wird es [gemacht: Hinzufügen oder Aktualisieren von Paketen mithilfe der Verwaltungskonsole](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) und [Erstellen einer Verbindungsgruppe](how-to-create-a-connection-group.md).</span><span class="sxs-lookup"><span data-stu-id="d601a-109">For more information about adding packages and connection groups, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Create a Connection Group](how-to-create-a-connection-group.md).</span></span>

2.  <span data-ttu-id="d601a-110">Um die Verwaltungskonsole zu öffnen, klicken Sie auf den folgenden Link, öffnen Sie einen Browser, und geben Sie Folgendes ein: http://MyMgmtSrv/AppvManagement/Console.html in einem Webbrowser, und importieren, veröffentlichen und berechtigen Sie alle Pakete und Verbindungsgruppen, die für eine bestimmte Gruppe von Benutzern erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d601a-110">To open the management console click the following link, open a browser and type the following: http://MyMgmtSrv/AppvManagement/Console.html in a web browser, and import, publish, and entitle all the packages and connection groups which will be necessary for a particular set of users.</span></span>

3.  <span data-ttu-id="d601a-111">Öffnen Sie auf dem Computer, auf dem der App-V 5,0-Client ausgeführt wird, eine erweiterte PowerShell-Eingabeaufforderung, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="d601a-111">On the computer running the App-V 5.0 client, open an elevated PowerShell command prompt, run the following command:</span></span>

    **<span data-ttu-id="d601a-112">Add-AppvPublishingServer-Name ABC-URL http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="d601a-112">Add-AppvPublishingServer -Name ABC -URL http:// MyPubSrv/AppvPublishing</span></span>**

    <span data-ttu-id="d601a-113">Mit diesem Befehl wird der angegebene Veröffentlichungsserver konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d601a-113">This command will configure the specified publishing server.</span></span> <span data-ttu-id="d601a-114">Es sollte eine Ausgabe ähnlich der folgenden angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="d601a-114">You should see output similar to the following:</span></span>

    <span data-ttu-id="d601a-115">ID: 1</span><span class="sxs-lookup"><span data-stu-id="d601a-115">Id : 1</span></span>

    <span data-ttu-id="d601a-116">SetByGroupPolicy: falsch</span><span class="sxs-lookup"><span data-stu-id="d601a-116">SetByGroupPolicy : False</span></span>

    <span data-ttu-id="d601a-117">Name: ABC</span><span class="sxs-lookup"><span data-stu-id="d601a-117">Name : ABC</span></span>

    <span data-ttu-id="d601a-118">URL: http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="d601a-118">URL : http:// MyPubSrv/AppvPublishing</span></span>

    <span data-ttu-id="d601a-119">GlobalRefreshEnabled: falsch</span><span class="sxs-lookup"><span data-stu-id="d601a-119">GlobalRefreshEnabled : False</span></span>

    <span data-ttu-id="d601a-120">GlobalRefreshOnLogon: falsch</span><span class="sxs-lookup"><span data-stu-id="d601a-120">GlobalRefreshOnLogon : False</span></span>

    <span data-ttu-id="d601a-121">GlobalRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="d601a-121">GlobalRefreshInterval : 0</span></span>

    <span data-ttu-id="d601a-122">GlobalRefreshIntervalUnit: Tag</span><span class="sxs-lookup"><span data-stu-id="d601a-122">GlobalRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="d601a-123">UserRefreshEnabled: true</span><span class="sxs-lookup"><span data-stu-id="d601a-123">UserRefreshEnabled : True</span></span>

    <span data-ttu-id="d601a-124">UserRefreshOnLogon: true</span><span class="sxs-lookup"><span data-stu-id="d601a-124">UserRefreshOnLogon : True</span></span>

    <span data-ttu-id="d601a-125">UserRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="d601a-125">UserRefreshInterval : 0</span></span>

    <span data-ttu-id="d601a-126">UserRefreshIntervalUnit: Tag</span><span class="sxs-lookup"><span data-stu-id="d601a-126">UserRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="d601a-127">Die zurückgegebene ID – in diesem Fall 1</span><span class="sxs-lookup"><span data-stu-id="d601a-127">The returned Id – in this case 1</span></span>

4.  <span data-ttu-id="d601a-128">Öffnen Sie auf dem Computer, auf dem der App-V 5,0-Client ausgeführt wird, eine PowerShell-Eingabeaufforderung, und geben Sie den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="d601a-128">On the computer running the App-V 5.0 client, open a PowerShell command prompt, and type the following command:</span></span>

    **<span data-ttu-id="d601a-129">Synchronisieren-AppvPublishingServer-Server-Nr. 1</span><span class="sxs-lookup"><span data-stu-id="d601a-129">Sync-AppvPublishingServer -ServerId 1</span></span>**

    <span data-ttu-id="d601a-130">Der Befehl fragt den Veröffentlichungsserver nach den Paketen und Verbindungsgruppen ab, die für diesen bestimmten Client basierend auf den Berechtigungen für die Pakete und Verbindungsgruppen, die auf dem Verwaltungsserver konfiguriert sind, hinzugefügt oder entfernt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d601a-130">The command will query the publishing server for the packages and connection groups that need to be added or removed for this particular client based on the entitlements for the packages and connection groups as configured on the management server.</span></span>

    <span data-ttu-id="d601a-131">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="d601a-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="d601a-132">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="d601a-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="d601a-133">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="d601a-133">Got an App-V issue?</span></span>** <span data-ttu-id="d601a-134">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="d601a-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="d601a-135">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d601a-135">Related topics</span></span>


[<span data-ttu-id="d601a-136">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="d601a-136">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





