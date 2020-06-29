---
title: So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank
description: So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank
author: dansimp
ms.assetid: d186bdb7-e522-4124-bc6d-7d5a41ba8266
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f20f1ce16c3f0168d1c797efd816d4125c0f1f53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805387"
---
# <span data-ttu-id="f9510-103">So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank</span><span class="sxs-lookup"><span data-stu-id="f9510-103">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="f9510-104">Gehen Sie wie folgt vor, um den Berichtsserver auf einem eigenständigen Computer zu installieren und mit der Datenbank zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="f9510-104">Use the following procedure to install the reporting server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="f9510-105">Wichtig</span><span class="sxs-lookup"><span data-stu-id="f9510-105">Important</span></span>**  
<span data-ttu-id="f9510-106">Bevor Sie die folgenden Schritte ausführen, sollten Sie die [App-V 5,0-Berichterstellung](about-app-v-50-reporting.md)lesen und verstehen.</span><span class="sxs-lookup"><span data-stu-id="f9510-106">Before performing the following procedure you should read and understand [About App-V 5.0 Reporting](about-app-v-50-reporting.md).</span></span>



**<span data-ttu-id="f9510-107">So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank</span><span class="sxs-lookup"><span data-stu-id="f9510-107">To install the reporting server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="f9510-108">Kopieren Sie die App-V 5,0 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f9510-108">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="f9510-109">Um die App-V 5,0 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="f9510-109">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="f9510-110">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="f9510-110">Click **Install**.</span></span>

2.  <span data-ttu-id="f9510-111">Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="f9510-111">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="f9510-112">Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).**</span><span class="sxs-lookup"><span data-stu-id="f9510-112">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="f9510-113">Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="f9510-113">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="f9510-114">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f9510-114">Click **Next**.</span></span>

4.  <span data-ttu-id="f9510-115">Aktivieren Sie auf der Seite **Featureauswahl** das Kontrollkästchen **Berichts Server** , und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="f9510-115">On the **Feature Selection** page, select the **Reporting Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="f9510-116">Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="f9510-116">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="f9510-117">Wählen Sie auf der Seite **vorhandene Berichtsdatenbank konfigurieren** die Option **SQL-Remoteserver verwenden**aus, und geben Sie den Computernamen des Computers ein, auf dem Microsoft SQL Server ausgeführt wird, beispielsweise **Sie SQLSERVERMACHINE**.</span><span class="sxs-lookup"><span data-stu-id="f9510-117">On the **Configure Existing Reporting Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL Server, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="f9510-118">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="f9510-118">Note</span></span>**  
    <span data-ttu-id="f9510-119">Wenn Microsoft SQL Server auf demselben Server bereitgestellt wird, wählen Sie **lokalen SQL Server verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="f9510-119">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.
~~~

7. <span data-ttu-id="f9510-120">Klicken Sie auf der Seite **Konfigurieren der Berichts Server Konfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f9510-120">On the **Configure Reporting Server Configuration** page.</span></span>

   -   <span data-ttu-id="f9510-121">Geben Sie den Website Namen an, den Sie für den Berichterstellungsdienst verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f9510-121">Specify the Website Name that you want to use for the Reporting Service.</span></span> <span data-ttu-id="f9510-122">Lassen Sie den Standardwert unverändert, wenn Sie keinen benutzerdefinierten Namen haben.</span><span class="sxs-lookup"><span data-stu-id="f9510-122">Leave the default unchanged if you do not have a custom name.</span></span>

   -   <span data-ttu-id="f9510-123">Geben Sie für die **Portbindung**eine eindeutige Portnummer an, die von App-V 5,0, beispielsweise **55555**, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9510-123">For the **Port binding**, specify a unique port number that will be used by App-V 5.0, for example **55555**.</span></span> <span data-ttu-id="f9510-124">Sie sollten auch sicherstellen, dass der angegebene Port nicht von einer anderen Website verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9510-124">You should also ensure that the port specified is not being used by another website.</span></span>

8. <span data-ttu-id="f9510-125">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="f9510-125">Click **Install**.</span></span>

   <span data-ttu-id="f9510-126">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="f9510-126">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f9510-127">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="f9510-127">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f9510-128">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="f9510-128">Got an App-V issue?</span></span>** <span data-ttu-id="f9510-129">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f9510-129">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f9510-130">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f9510-130">Related topics</span></span>


[<span data-ttu-id="f9510-131">Informationen zur App-V 5.0-Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="f9510-131">About App-V 5.0 Reporting</span></span>](about-app-v-50-reporting.md)

[<span data-ttu-id="f9510-132">Bereitstellen von App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f9510-132">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="f9510-133">So aktivieren Sie die Berichterstellung auf dem App-V 5.0-Client mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9510-133">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)









