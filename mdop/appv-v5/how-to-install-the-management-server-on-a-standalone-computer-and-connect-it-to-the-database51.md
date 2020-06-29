---
title: So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank
description: So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank
author: dansimp
ms.assetid: 3f83c335-d976-4abd-b8f8-d7f5e50b4318
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2cce96f914f65e7432b5ed9e7c5ecb1a6306990
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805408"
---
# <span data-ttu-id="143be-103">So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank</span><span class="sxs-lookup"><span data-stu-id="143be-103">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="143be-104">Gehen Sie wie folgt vor, um den Verwaltungsserver auf einem eigenständigen Computer zu installieren und mit der Datenbank zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="143be-104">Use the following procedure to install the management server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="143be-105">So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank</span><span class="sxs-lookup"><span data-stu-id="143be-105">To install the management server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="143be-106">Kopieren Sie die App-V 5,1 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="143be-106">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="143be-107">Um die App-V 5,1 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="143be-107">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="143be-108">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="143be-108">Click **Install**.</span></span>

2.  <span data-ttu-id="143be-109">Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="143be-109">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="143be-110">Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).**</span><span class="sxs-lookup"><span data-stu-id="143be-110">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="143be-111">Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="143be-111">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="143be-112">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="143be-112">Click **Next**.</span></span>

4.  <span data-ttu-id="143be-113">Aktivieren Sie auf der Seite **Featureauswahl** das Kontrollkästchen **Verwaltungs Server** , und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="143be-113">On the **Feature Selection** page, select the **Management Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="143be-114">Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="143be-114">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="143be-115">Wählen Sie auf der Seite **vorhandene Verwaltungsdatenbank konfigurieren** die Option **SQL-Remote Server verwenden**aus, und geben Sie den Computernamen des Computers ein, auf dem Microsoft SQL SQL ausgeführt wird, beispielsweise **Sie SQLSERVERMACHINE**.</span><span class="sxs-lookup"><span data-stu-id="143be-115">On the **Configure Existing Management Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL SQL, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="143be-116">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="143be-116">Note</span></span>**  
    <span data-ttu-id="143be-117">Wenn Microsoft SQL Server auf demselben Server bereitgestellt wird, wählen Sie **lokalen SQL Server verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="143be-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. <span data-ttu-id="143be-118">Geben Sie auf der Seite **Konfigurieren der Verwaltungs Server Konfiguration** die Anzeigengruppe oder das Konto an, das für administrative Zwecke eine Verbindung mit der Verwaltungskonsole herstellen soll, beispielsweise **MyDomain\\MyUser** oder **MyDomain\\AdminGroup**.</span><span class="sxs-lookup"><span data-stu-id="143be-118">On the **Configure Management Server Configuration** page, specify the AD group or account that will connect to the management console for administrative purposes for example **MyDomain\\MyUser** or **MyDomain\\AdminGroup**.</span></span> <span data-ttu-id="143be-119">Das von Ihnen angegebene Konto oder die Anzeigengruppe wird aktiviert, um den Server über die Verwaltungskonsole zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="143be-119">The account or AD group you specify will be enabled to manage the server through the management console.</span></span> <span data-ttu-id="143be-120">Sie können weitere Benutzer oder Gruppen mithilfe der Verwaltungskonsole nach der Installation hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="143be-120">You can add additional users or groups using the management console after installation</span></span>

   <span data-ttu-id="143be-121">Geben Sie den **Website Namen** an, den Sie für den Verwaltungsdienst verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="143be-121">Specify the **Website Name** that you want to use for the management service.</span></span> <span data-ttu-id="143be-122">Übernehmen Sie die Standardeinstellung, wenn Sie keinen benutzerdefinierten Namen haben.</span><span class="sxs-lookup"><span data-stu-id="143be-122">Accept the default if you do not have a custom name.</span></span> <span data-ttu-id="143be-123">Geben Sie für die **Portbindung**eine eindeutige Portnummer an, die verwendet werden soll, beispielsweise **12345**.</span><span class="sxs-lookup"><span data-stu-id="143be-123">For the **Port Binding**, specify a unique port number to be used, for example **12345**.</span></span>

8. <span data-ttu-id="143be-124">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="143be-124">Click **Install**.</span></span>

9. <span data-ttu-id="143be-125">Um zu bestätigen, dass das Setup erfolgreich abgeschlossen wurde, öffnen Sie einen Webbrowser, und geben Sie die folgende URL ein: http://managementserver:portnumber/Console .</span><span class="sxs-lookup"><span data-stu-id="143be-125">To confirm that the setup has completed successfully, open a web browser, and type the following URL: http://managementserver:portnumber/Console.</span></span> <span data-ttu-id="143be-126">Wenn die Installation erfolgreich war, sollten Sie sehen, dass die **Verwaltungskonsole** angezeigt wird, ohne dass Fehlermeldungen oder Warnungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="143be-126">If the installation was successful, you should see the **Management Console** appear without any error messages or warnings being displayed.</span></span>

   <span data-ttu-id="143be-127">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="143be-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="143be-128">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="143be-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="143be-129">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="143be-129">Got an App-V issue?</span></span>** <span data-ttu-id="143be-130">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="143be-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="143be-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="143be-131">Related topics</span></span>


[<span data-ttu-id="143be-132">Bereitstellen von App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="143be-132">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)









