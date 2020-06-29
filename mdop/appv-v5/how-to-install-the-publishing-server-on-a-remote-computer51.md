---
title: So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer
description: So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer
author: dansimp
ms.assetid: 1c903f78-0558-458d-a149-d5f6fb55aefb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a085d68305057538228599e35dd9500957342ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805384"
---
# <span data-ttu-id="b2e25-103">So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer</span><span class="sxs-lookup"><span data-stu-id="b2e25-103">How to Install the Publishing Server on a Remote Computer</span></span>


<span data-ttu-id="b2e25-104">Gehen Sie wie folgt vor, um den Veröffentlichungsserver auf einem separaten Computer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b2e25-104">Use the following procedure to install the publishing server on a separate computer.</span></span> <span data-ttu-id="b2e25-105">Bevor Sie die folgenden Schritte ausführen, stellen Sie sicher, dass die Datenbank und der Verwaltungsserver verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b2e25-105">Before you perform the following procedure, ensure the database and management server are available.</span></span>

**<span data-ttu-id="b2e25-106">So installieren Sie den Veröffentlichungsserver auf einem separaten Computer</span><span class="sxs-lookup"><span data-stu-id="b2e25-106">To install the publishing server on a separate computer</span></span>**

1. <span data-ttu-id="b2e25-107">Kopieren Sie die App-V 5,1 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b2e25-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="b2e25-108">Um die App-V 5,1 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="b2e25-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="b2e25-109">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="b2e25-109">Click **Install**.</span></span>

2. <span data-ttu-id="b2e25-110">Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2e25-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="b2e25-111">Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).**</span><span class="sxs-lookup"><span data-stu-id="b2e25-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="b2e25-112">Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="b2e25-112">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="b2e25-113">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2e25-113">Click **Next**.</span></span>

4. <span data-ttu-id="b2e25-114">Aktivieren Sie auf der Seite **Featureauswahl** das Kontrollkästchen **Veröffentlichungs Server** , und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2e25-114">On the **Feature Selection** page, select the **Publishing Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="b2e25-115">Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2e25-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="b2e25-116">Geben Sie auf der Seite **Configure Publishing Server Configuration** die folgenden Elemente an:</span><span class="sxs-lookup"><span data-stu-id="b2e25-116">On the **Configure Publishing Server Configuration** page, specify the following items:</span></span>

   -   <span data-ttu-id="b2e25-117">Die URL für den Verwaltungsdienst, mit dem der Veröffentlichungsserver eine Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="b2e25-117">The URL for the management service that the publishing server will connect to.</span></span> <span data-ttu-id="b2e25-118">Beispiel: **http://ManagementServerName:12345** .</span><span class="sxs-lookup"><span data-stu-id="b2e25-118">For example, **http://ManagementServerName:12345**.</span></span>

   -   <span data-ttu-id="b2e25-119">Geben Sie den Websitenamen an, den Sie für den Veröffentlichungsdienst verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b2e25-119">Specify the website name that you want to use for the publishing service.</span></span> <span data-ttu-id="b2e25-120">Übernehmen Sie die Standardeinstellung, wenn Sie keinen benutzerdefinierten Namen haben.</span><span class="sxs-lookup"><span data-stu-id="b2e25-120">Accept the default if you do not have a custom name.</span></span>

   -   <span data-ttu-id="b2e25-121">Geben Sie für die **Portbindung**eine eindeutige Portnummer an, die von App-V 5,1, beispielsweise **54321**, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2e25-121">For the **Port Binding**, specify a unique port number that will be used by App-V 5.1, for example **54321**.</span></span>

7. <span data-ttu-id="b2e25-122">Klicken Sie auf der Seite **bereit zur Installation** auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="b2e25-122">On the **Ready to Install** page, click **Install**.</span></span>

8. <span data-ttu-id="b2e25-123">Nachdem die Installation abgeschlossen ist, muss der Veröffentlichungsserver beim Verwaltungsserver registriert sein.</span><span class="sxs-lookup"><span data-stu-id="b2e25-123">After the installation is complete, the publishing server must be registered with the management server.</span></span> <span data-ttu-id="b2e25-124">Führen Sie in der App-V 5,1-Verwaltungskonsole die folgenden Schritte aus, um den Server zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="b2e25-124">In the App-V 5.1 management console, use the following steps to register the server:</span></span>

   1.  <span data-ttu-id="b2e25-125">Öffnen Sie die App-V 5,1 Management Server-Konsole.</span><span class="sxs-lookup"><span data-stu-id="b2e25-125">Open the App-V 5.1 management server console.</span></span>

   2.  <span data-ttu-id="b2e25-126">Wählen Sie im linken Bereich **Server**aus, und wählen Sie dann **neuen Server registrieren**aus.</span><span class="sxs-lookup"><span data-stu-id="b2e25-126">In the left pane, select **Servers**, and then select **Register New Server**.</span></span>

   3.  <span data-ttu-id="b2e25-127">Geben Sie den Namen dieses Servers und eine Beschreibung (falls erforderlich) ein, und klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="b2e25-127">Type the name of this server and a description (if required) and click **Add**.</span></span>

9. <span data-ttu-id="b2e25-128">Um zu überprüfen, ob der Veröffentlichungsserver ordnungsgemäß ausgeführt wird, sollten Sie ein Paket auf den Verwaltungsserver importieren, das Paket zu einer Anzeigengruppe berechtigen und das Paket veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="b2e25-128">To verify if the publishing server is running correctly, you should import a package to the management server, entitle the package to an AD group, and publish the package.</span></span> <span data-ttu-id="b2e25-129">Öffnen Sie die folgende URL über einen Internet Browser: <strong> http://publishingserver:pubport </strong></span><span class="sxs-lookup"><span data-stu-id="b2e25-129">Using an internet browser, open the following URL: <strong>http://publishingserver:pubport</strong>.</span></span> <span data-ttu-id="b2e25-130">Wenn der Server ordnungsgemäß ausgeführt wird, werden Informationen ähnlich der folgenden angezeigt:</span><span class="sxs-lookup"><span data-stu-id="b2e25-130">If the server is running correctly information similar to the following will be displayed:</span></span>

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   <span data-ttu-id="b2e25-131">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="b2e25-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="b2e25-132">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="b2e25-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="b2e25-133">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="b2e25-133">Got an App-V issue?</span></span>** <span data-ttu-id="b2e25-134">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="b2e25-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="b2e25-135">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b2e25-135">Related topics</span></span>


[<span data-ttu-id="b2e25-136">Bereitstellen von App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b2e25-136">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

 

 





