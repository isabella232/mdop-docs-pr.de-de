---
title: So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste
description: So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805417"
---
# <span data-ttu-id="e2d12-103">So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste</span><span class="sxs-lookup"><span data-stu-id="e2d12-103">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>


<span data-ttu-id="e2d12-104">Gehen Sie wie folgt vor, um den Datenbankserver und den Verwaltungsserver auf unterschiedlichen Computern zu installieren.</span><span class="sxs-lookup"><span data-stu-id="e2d12-104">Use the following procedure to install the database server and management server on different computers.</span></span> <span data-ttu-id="e2d12-105">Auf dem Computer, auf dem Sie den Datenbankserver installieren möchten, muss eine unterstützte Version von Microsoft SQL ausgeführt werden, oder die Installation schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="e2d12-105">The computer you plan to install the database server on must be running a supported version of Microsoft SQL or the installation will fail.</span></span>

**<span data-ttu-id="e2d12-106">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e2d12-106">Note</span></span>**  
<span data-ttu-id="e2d12-107">Nachdem Sie die Bereitstellung abgeschlossen haben, müssen der **Microsoft SQL Server-Name**, der **Instanzname** und der **Datenbankname** vom Administrator installiert werden, um eine Verbindung mit diesen Datenbanken herstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="e2d12-107">After you complete the deployment, the **Microsoft SQL Server name**, **instance name** and **database name** will be required by the administrator installing the service to be able to connect to these databases.</span></span>



**<span data-ttu-id="e2d12-108">So installieren Sie die Verwaltungsdatenbank und den Verwaltungsserver auf separaten Computern</span><span class="sxs-lookup"><span data-stu-id="e2d12-108">To install the management database and the management server on separate computers</span></span>**

1.  <span data-ttu-id="e2d12-109">Kopieren Sie die App-V 5,0 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e2d12-109">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="e2d12-110">Um die App-V 5,0 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="e2d12-110">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="e2d12-111">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-111">Click **Install**.</span></span>

2.  <span data-ttu-id="e2d12-112">Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-112">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="e2d12-113">Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).**</span><span class="sxs-lookup"><span data-stu-id="e2d12-113">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="e2d12-114">Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="e2d12-114">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="e2d12-115">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-115">Click **Next**.</span></span>

4.  <span data-ttu-id="e2d12-116">Wählen Sie auf der Seite **Featureauswahl** die Komponenten aus, die Sie installieren möchten, indem Sie das Kontrollkästchen **Verwaltungs Server-Datenbank** auswählen und auf **weiter**klicken.</span><span class="sxs-lookup"><span data-stu-id="e2d12-116">On the **Feature Selection** page, select the components you want to install by selecting the **Management Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="e2d12-117">Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-117">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="e2d12-118">Übernehmen Sie auf der **Seite erste neue Verwaltungs Server-Datenbank erstellen**die Standardauswahl, falls zutreffend, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-118">On the initial **Create New Management Server Database page**, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="e2d12-119">Wenn Sie eine benutzerdefinierte SQL Server-Instanz verwenden, wählen Sie **benutzerdefinierte Instanz verwenden** aus, und geben Sie den Namen der Instanz ein.</span><span class="sxs-lookup"><span data-stu-id="e2d12-119">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="e2d12-120">Wenn Sie einen benutzerdefinierten Datenbanknamen verwenden, wählen Sie **benutzerdefinierte Konfiguration** aus, und geben Sie den Datenbanknamen ein.</span><span class="sxs-lookup"><span data-stu-id="e2d12-120">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="e2d12-121">Wählen Sie auf der nächsten Seite **neue Verwaltungs Server-Datenbank erstellen** die Option **Remotecomputer verwenden**aus, und geben Sie das Konto des Remotecomputers mit dem folgenden Format ein: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-121">On the next **Create New Management Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="e2d12-122">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e2d12-122">Note</span></span>**  
    <span data-ttu-id="e2d12-123">Wenn Sie den Verwaltungsserver auf demselben Computer bereitstellen möchten, müssen Sie **diesen lokalen Computer verwenden**auswählen.</span><span class="sxs-lookup"><span data-stu-id="e2d12-123">If you plan to deploy the management server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="e2d12-124">Klicken Sie auf **Installieren**, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="e2d12-124">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="e2d12-125">So installieren Sie die Berichtsdatenbank und den Berichtsserver auf separaten Computern</span><span class="sxs-lookup"><span data-stu-id="e2d12-125">To install the reporting database and the reporting server on separate computers</span></span>**

1.  <span data-ttu-id="e2d12-126">Kopieren Sie die App-V 5,0 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e2d12-126">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="e2d12-127">Um die App-V 5,0 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="e2d12-127">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="e2d12-128">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-128">Click **Install**.</span></span>

2.  <span data-ttu-id="e2d12-129">Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-129">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="e2d12-130">Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).**</span><span class="sxs-lookup"><span data-stu-id="e2d12-130">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="e2d12-131">Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="e2d12-131">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="e2d12-132">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-132">Click **Next**.</span></span>

4.  <span data-ttu-id="e2d12-133">Wählen Sie auf der Seite **Featureauswahl** die Komponenten aus, die Sie installieren möchten, indem Sie das Kontrollkästchen **Berichts Server-Datenbank** auswählen und auf **weiter**klicken.</span><span class="sxs-lookup"><span data-stu-id="e2d12-133">On the **Feature Selection** page, select the components you want to install by selecting the **Reporting Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="e2d12-134">Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-134">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="e2d12-135">Übernehmen Sie auf der Seite erste **neue Berichts Server-Datenbank erstellen** die Standardauswahl, falls zutreffend, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-135">On the initial **Create New Reporting Server Database** page, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="e2d12-136">Wenn Sie eine benutzerdefinierte SQL Server-Instanz verwenden, wählen Sie **benutzerdefinierte Instanz verwenden** aus, und geben Sie den Namen der Instanz ein.</span><span class="sxs-lookup"><span data-stu-id="e2d12-136">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="e2d12-137">Wenn Sie einen benutzerdefinierten Datenbanknamen verwenden, wählen Sie **benutzerdefinierte Konfiguration** aus, und geben Sie den Datenbanknamen ein.</span><span class="sxs-lookup"><span data-stu-id="e2d12-137">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="e2d12-138">Wählen Sie auf der nächsten Seite **neue Berichts Server-Datenbank erstellen** die Option **Remotecomputer verwenden**aus, und geben Sie das Konto des Remotecomputers mit dem folgenden Format ein: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-138">On the next **Create New Reporting Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="e2d12-139">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e2d12-139">Note</span></span>**  
    <span data-ttu-id="e2d12-140">Wenn Sie den Berichtsserver auf demselben Computer bereitstellen möchten, müssen Sie **diesen lokalen Computer verwenden**auswählen.</span><span class="sxs-lookup"><span data-stu-id="e2d12-140">If you plan to deploy the reporting server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="e2d12-141">Klicken Sie auf **Installieren**, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="e2d12-141">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="e2d12-142">So installieren Sie die Verwaltungs-und Berichtsdatenbanken mithilfe von App-V 5,0-Datenbankskripts</span><span class="sxs-lookup"><span data-stu-id="e2d12-142">To install the management and reporting databases using App-V 5.0 database scripts</span></span>**

1.  <span data-ttu-id="e2d12-143">Kopieren Sie die App-V 5,0 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e2d12-143">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span>

2.  <span data-ttu-id="e2d12-144">Wenn Sie die App-V 5,0-Datenbankskripts extrahieren möchten, öffnen Sie eine Eingabeaufforderung, geben Sie den Speicherort der Installationsdateien an, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="e2d12-144">To extract the App-V 5.0 database scripts, open a command prompt and specify the location where the installation files are saved and run the following command:</span></span>

    <span data-ttu-id="e2d12-145">**appv\_server\_setup.exe** **/Layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-145">**appv\_server\_setup.exe** **/LAYOUT** **/LAYOUTDIR=”InstallationExtractionLocation”**.</span></span>

3.  <span data-ttu-id="e2d12-146">Nachdem die Extrahierung abgeschlossen wurde, können Sie auf die App-V 5,0-Datenbankskripts und Anweisungen in der Readme-Datei zugreifen:</span><span class="sxs-lookup"><span data-stu-id="e2d12-146">After the extraction has been completed, to access the App-V 5.0 database scripts and instructions readme file:</span></span>

    -   <span data-ttu-id="e2d12-147">Die Readme-Datei für die App-V 5,0-Verwaltungsdatenbank und die Anweisungen für die Anleitung finden Sie im folgenden Ordner: **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Management Database**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-147">The App-V 5.0 Management Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Management Database**.</span></span>

    -   <span data-ttu-id="e2d12-148">Die Readme-Datei für die App-V 5,0-Berichtsdatenbank und die Anweisungen für die Anleitung finden Sie im folgenden Ordner: **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Reporting Database**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-148">The App-V 5.0 Reporting Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Reporting Database**.</span></span>

4.  <span data-ttu-id="e2d12-149">Kopieren Sie für jede Datenbank die Skripts auf eine Freigabe, und ändern Sie Sie, und folgen Sie den Anweisungen in der Readme-Datei.</span><span class="sxs-lookup"><span data-stu-id="e2d12-149">For each database, copy the scripts to a share and modify them following the instructions in the readme file.</span></span>

    **<span data-ttu-id="e2d12-150">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e2d12-150">Note</span></span>**  
    <span data-ttu-id="e2d12-151">Weitere Informationen zum Ändern der in den Skripts enthaltenen erforderlichen SIDs finden Sie unter [Installieren der App-V-Datenbanken und Konvertieren der zugehörigen Sicherheitsbezeichner mithilfe von PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="e2d12-151">For more information about modifying the required SIDs contained in the scripts see, [How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span></span>



5.  <span data-ttu-id="e2d12-152">Führen Sie die Skripts auf dem Computer aus, auf dem Microsoft SQL Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2d12-152">Run the scripts on the computer running Microsoft SQL Server.</span></span>

    <span data-ttu-id="e2d12-153">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="e2d12-153">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="e2d12-154">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="e2d12-154">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="e2d12-155">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="e2d12-155">Got an App-V issue?</span></span>** <span data-ttu-id="e2d12-156">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="e2d12-156">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="e2d12-157">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e2d12-157">Related topics</span></span>


[<span data-ttu-id="e2d12-158">Bereitstellen von App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e2d12-158">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









