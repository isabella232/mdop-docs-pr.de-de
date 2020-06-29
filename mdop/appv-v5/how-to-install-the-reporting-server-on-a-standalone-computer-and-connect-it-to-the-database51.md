---
title: So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank
description: So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805378"
---
# <span data-ttu-id="6bafc-103">So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank</span><span class="sxs-lookup"><span data-stu-id="6bafc-103">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>

<span data-ttu-id="6bafc-104">Gehen Sie wie folgt vor, um den Berichtsserver auf einem eigenständigen Computer zu installieren und mit der Datenbank zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="6bafc-104">Use the following procedure to install the reporting server on a standalone computer and connect it to the database.</span></span>

<span data-ttu-id="6bafc-105">**Wichtig** Bevor Sie die folgenden Schritte ausführen, sollten Sie die [App-V 5,1-Berichterstellung](about-app-v-51-reporting.md)lesen und verstehen.</span><span class="sxs-lookup"><span data-stu-id="6bafc-105">**Important** Before performing the following procedure you should read and understand [About App-V 5.1 Reporting](about-app-v-51-reporting.md).</span></span>

## <span data-ttu-id="6bafc-106">So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank</span><span class="sxs-lookup"><span data-stu-id="6bafc-106">To install the reporting server on a standalone computer and connect it to the database</span></span>

1. <span data-ttu-id="6bafc-107">Kopieren Sie die App-V 5,1 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6bafc-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="6bafc-108">Um die App-V 5,1 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="6bafc-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="6bafc-109">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="6bafc-109">Click **Install**.</span></span>

2. <span data-ttu-id="6bafc-110">Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="6bafc-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="6bafc-111">Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).**</span><span class="sxs-lookup"><span data-stu-id="6bafc-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="6bafc-112">Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="6bafc-112">To disable Microsoft updates, select **I don't want to use Microsoft Update**.</span></span> <span data-ttu-id="6bafc-113">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="6bafc-113">Click **Next**.</span></span>

4. <span data-ttu-id="6bafc-114">Aktivieren Sie auf der Seite **Featureauswahl** das Kontrollkästchen **Berichts Server** , und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="6bafc-114">On the **Feature Selection** page, select the **Reporting Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="6bafc-115">Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="6bafc-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="6bafc-116">Wählen Sie auf der Seite **vorhandene Berichtsdatenbank konfigurieren** die Option **SQL-Remoteserver verwenden**aus, und geben Sie den Computernamen des Computers ein, auf dem Microsoft SQL Server ausgeführt wird, beispielsweise **Sie SQLSERVERMACHINE**.</span><span class="sxs-lookup"><span data-stu-id="6bafc-116">On the **Configure Existing Reporting Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL Server, for example **SqlServerMachine**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6bafc-117">Wenn Microsoft SQL Server auf demselben Server bereitgestellt wird, wählen Sie **lokalen SQL Server verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="6bafc-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>

    <span data-ttu-id="6bafc-118">Wählen Sie für die SQL Server-Instanz **die Option Standardinstanz verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="6bafc-118">For the SQL Server Instance, select **Use the default instance**.</span></span> <span data-ttu-id="6bafc-119">Wenn Sie eine benutzerdefinierte Microsoft SQL Server-Instanz verwenden, müssen Sie **eine benutzerdefinierte Instanz verwenden** auswählen und dann den Namen der Instanz eingeben.</span><span class="sxs-lookup"><span data-stu-id="6bafc-119">If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.</span></span>

    <span data-ttu-id="6bafc-120">Geben Sie den **SQL Server-Datenbanknamen** an, den dieser Berichtsserver verwenden soll, beispielsweise **AppvReporting**.</span><span class="sxs-lookup"><span data-stu-id="6bafc-120">Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.</span></span>

7. <span data-ttu-id="6bafc-121">Klicken Sie auf der Seite **Konfigurieren der Berichts Server Konfiguration** .</span><span class="sxs-lookup"><span data-stu-id="6bafc-121">On the **Configure Reporting Server Configuration** page.</span></span>

   - <span data-ttu-id="6bafc-122">Geben Sie den Website Namen an, den Sie für den Berichterstellungsdienst verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="6bafc-122">Specify the Website Name that you want to use for the Reporting Service.</span></span> <span data-ttu-id="6bafc-123">Lassen Sie den Standardwert unverändert, wenn Sie keinen benutzerdefinierten Namen haben.</span><span class="sxs-lookup"><span data-stu-id="6bafc-123">Leave the default unchanged if you do not have a custom name.</span></span>

   - <span data-ttu-id="6bafc-124">Geben Sie für die **Portbindung**eine eindeutige Portnummer an, die von App-V 5,1, beispielsweise **55555**, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bafc-124">For the **Port binding**, specify a unique port number that will be used by App-V 5.1, for example **55555**.</span></span> <span data-ttu-id="6bafc-125">Sie sollten auch sicherstellen, dass der angegebene Port nicht von einer anderen Website verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bafc-125">You should also ensure that the port specified is not being used by another website.</span></span>

8. <span data-ttu-id="6bafc-126">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="6bafc-126">Click **Install**.</span></span>

**<span data-ttu-id="6bafc-127">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="6bafc-127">Got an App-V issue?</span></span>** <span data-ttu-id="6bafc-128">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6bafc-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="6bafc-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6bafc-129">Related topics</span></span>

[<span data-ttu-id="6bafc-130">Informationen zur App-V 5.1-Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="6bafc-130">About App-V 5.1 Reporting</span></span>](about-app-v-51-reporting.md)

[<span data-ttu-id="6bafc-131">Bereitstellen von App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="6bafc-131">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="6bafc-132">So aktivieren Sie die Berichterstellung auf dem App-V 5.1-Client mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="6bafc-132">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
