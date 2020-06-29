---
title: So installieren Sie Application Virtualization Management Server
description: So installieren Sie Application Virtualization Management Server
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807076"
---
# <span data-ttu-id="9be94-103">So installieren Sie Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="9be94-103">How to Install Application Virtualization Management Server</span></span>


<span data-ttu-id="9be94-104">Der Application Virtualization Management Server veröffentlicht seine Anwendungen für Clients.</span><span class="sxs-lookup"><span data-stu-id="9be94-104">The Application Virtualization Management Server publishes its applications to clients.</span></span> <span data-ttu-id="9be94-105">In einer Umgebung mit Lastenausgleich, die für große Bereitstellungen typisch ist, sollten alle Server in einer Servergruppe dieselben Anwendungen streamen.</span><span class="sxs-lookup"><span data-stu-id="9be94-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="9be94-106">Wenn Application Virtualization-Verwaltungsserver verschiedene Anwendungen veröffentlichen sollen, weisen Sie die Server verschiedenen Servergruppen zu.</span><span class="sxs-lookup"><span data-stu-id="9be94-106">If Application Virtualization Management Servers are to publish different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="9be94-107">In diesem Fall müssen Sie möglicherweise auch die Kapazität einer Servergruppe erhöhen.</span><span class="sxs-lookup"><span data-stu-id="9be94-107">In this case, you also might need to increase a server group's capacity.</span></span>

<span data-ttu-id="9be94-108">Wenn Sie einen Zielcomputer im Netzwerk festgelegt haben, mit einem Anmeldekonto, das über lokale Administrator Rechte verfügt, können Sie mit dem folgenden Verfahren den Application Virtualization-Verwaltungsserver installieren und der entsprechenden Servergruppe zuweisen.</span><span class="sxs-lookup"><span data-stu-id="9be94-108">If you have designated a target computer on the network, with a login account having local Administrator privileges, you can use the following procedure to install the Application Virtualization Management Server and assign it to the appropriate server group.</span></span>

**<span data-ttu-id="9be94-109">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9be94-109">Note</span></span>**  
<span data-ttu-id="9be94-110">Der Installations-Assistent kann einen Servergruppen Eintrag erstellen, wenn er nicht vorhanden ist, sowie einen Eintrag über die Mitgliedschaft des Application Virtualization Management Servers in dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9be94-110">The Installation Wizard can create a server group record, if one does not exist, as well as a record of the Application Virtualization Management Server's membership in this group.</span></span>



<span data-ttu-id="9be94-111">Nachdem Sie den Installationsvorgang abgeschlossen haben, starten Sie den Server neu.</span><span class="sxs-lookup"><span data-stu-id="9be94-111">After you complete the installation process, reboot the server.</span></span>

**<span data-ttu-id="9be94-112">So installieren Sie einen Application Virtualization-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="9be94-112">To install an Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="9be94-113">Überprüfen und deinstallieren Sie bei Bedarf frühere Versionen des Application Virtualization Management Servers, die auf dem Zielcomputer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="9be94-113">Verify and, if necessary, uninstall previous versions of the Application Virtualization Management Server that are installed on the target computer.</span></span>

2.  <span data-ttu-id="9be94-114">Navigieren Sie zum Öffnen des **Microsoft Application Virtualization Management Server-Installations** -Assistenten zum Speicherort des Application Virtualization System **setup.exe** -Programms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf die **Setup.exe** -Datei.</span><span class="sxs-lookup"><span data-stu-id="9be94-114">To open the **Microsoft Application Virtualization Management Server installation** wizard, navigate to the location of the Application Virtualization System **setup.exe** program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="9be94-115">Klicken Sie auf der Seite **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-115">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="9be94-116">Lesen Sie auf der Seite **Lizenzvertrag** den Lizenzvertrag, und wählen Sie zum Akzeptieren des Lizenzvertrags die Option **Ich akzeptiere die Lizenzbedingungen**aus.</span><span class="sxs-lookup"><span data-stu-id="9be94-116">On the **License Agreement** page, read the license agreement and, to accept the license agreement, select **I accept the license terms and conditions**.</span></span> <span data-ttu-id="9be94-117">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-117">Click **Next**.</span></span>

5.  <span data-ttu-id="9be94-118">Auf der Seite **Registrierungsinformationen** müssen Sie den Benutzernamen und die **Organisation**eingeben.</span><span class="sxs-lookup"><span data-stu-id="9be94-118">On the **Registering Information** page, you must enter the user name and the **Organization**.</span></span> <span data-ttu-id="9be94-119">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-119">Click **Next**.</span></span>

6.  <span data-ttu-id="9be94-120">Wählen Sie auf der Seite **Setuptyp** die Option **Benutzerdefiniert**aus.</span><span class="sxs-lookup"><span data-stu-id="9be94-120">On the **Setup Type** page, select **Custom**.</span></span> <span data-ttu-id="9be94-121">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-121">Click **Next**.</span></span> <span data-ttu-id="9be94-122">Deaktivieren Sie auf der Seite **Benutzerdefiniertes Setup** alle Application Virtualization System-Komponenten außer **Application Virtualization Server**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-122">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    **<span data-ttu-id="9be94-123">Achtung</span><span class="sxs-lookup"><span data-stu-id="9be94-123">Caution</span></span>**  
    <span data-ttu-id="9be94-124">Wenn eine Komponente bereits auf dem Computer installiert ist, wird die Komponente automatisch deinstalliert, wenn Sie Sie im **benutzerdefinierten Setup** Fenster deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9be94-124">If a component is already installed on the computer, when you deselect it in the **Custom Setup** window, the component is automatically uninstalled.</span></span>



7.  <span data-ttu-id="9be94-125">Wählen Sie auf der Seite **Konfigurationsdatenbank** in der Liste der verfügbaren Server einen Datenbankserver aus, oder fügen Sie einen Server hinzu, indem Sie **den folgenden Hostnamen verwenden** und den **Servernamen** und die **Port Nummern** angeben.</span><span class="sxs-lookup"><span data-stu-id="9be94-125">On the **Configuration Database** page, select a database server from the list of available servers or add a server by selecting **Use the following host name** and specifying the **Server Name** and **Port Number** data.</span></span> <span data-ttu-id="9be94-126">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-126">Click **Next**.</span></span>

    **<span data-ttu-id="9be94-127">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9be94-127">Note</span></span>**  
    <span data-ttu-id="9be94-128">Der Application Virtualization-Verwaltungs Server unterstützt keine Groß-/Kleinschreibung SQL.</span><span class="sxs-lookup"><span data-stu-id="9be94-128">The Application Virtualization Management Server does not support case sensitive SQL.</span></span>



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. <span data-ttu-id="9be94-129">Wählen Sie auf der Seite **Verbindungssicherheitsmodus** in der Dropdownliste das gewünschte Zertifikat aus.</span><span class="sxs-lookup"><span data-stu-id="9be94-129">On the **Connection Security Mode** page, select the desired certificate from the drop-down list.</span></span> <span data-ttu-id="9be94-130">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-130">Click **Next**.</span></span>

   **<span data-ttu-id="9be94-131">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9be94-131">Note</span></span>**  
   <span data-ttu-id="9be94-132">Bei der Einstellung für den **sicheren Verbindungsmodus** muss der Server über ein Serverzertifikat verfügen, das von einer öffentlichen Schlüsselinfrastruktur bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9be94-132">The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="9be94-133">Wenn ein Serverzertifikat nicht auf dem Server installiert ist, ist diese Option nicht verfügbar und kann nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="9be94-133">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="9be94-134">Sie müssen dem Netzwerkdienstkonto Lesezugriff auf das verwendete Zertifikat gewähren.</span><span class="sxs-lookup"><span data-stu-id="9be94-134">You must grant the Network Service account read access to the certificate being used.</span></span>



9. <span data-ttu-id="9be94-135">Klicken Sie auf der Seite **TCP-Port Konfiguration** auf **Standardanschluss verwenden (554)**, um den Standardport (554) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9be94-135">On the **TCP Port Configuration** page, to use the default port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="9be94-136">Wenn Sie einen benutzerdefinierten Port angeben möchten, wählen Sie **benutzerdefinierten Port verwenden** aus, und geben Sie die Portnummer an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9be94-136">To specify a custom port, select **Use custom port** and specify the port number that will be used.</span></span> <span data-ttu-id="9be94-137">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-137">Click **Next**.</span></span>

   **<span data-ttu-id="9be94-138">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9be94-138">Note</span></span>**  
   <span data-ttu-id="9be94-139">Wenn Sie den Server in einer nicht sicheren Umgebung installieren, können Sie den Standardport (554) verwenden, oder Sie können einen benutzerdefinierten Port definieren.</span><span class="sxs-lookup"><span data-stu-id="9be94-139">When you install the server in a nonsecure environment, you can use the default port (554) or you can define a custom port.</span></span>



10. <span data-ttu-id="9be94-140">Geben Sie auf der Seite **Administrator Gruppe** den Namen der Sicherheitsgruppe an, die zum Verwalten dieses Servers unter **Gruppenname**autorisiert ist.</span><span class="sxs-lookup"><span data-stu-id="9be94-140">On the **Administrator Group** page, specify the name of the security group authorized to manage this server in **Group Name**.</span></span> <span data-ttu-id="9be94-141">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-141">Click **Next**.</span></span> <span data-ttu-id="9be94-142">Bestätigen Sie die angegebene Gruppe, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-142">Confirm the group specified and click **Next**.</span></span>

11. <span data-ttu-id="9be94-143">Geben Sie auf der Seite **Standardanbietergruppe** den Namen der Standardanbietergruppe an, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-143">On the **Default Provider Group** page, specify the name of the default provider group, and then click **Next**.</span></span>

12. <span data-ttu-id="9be94-144">Geben Sie auf der Seite **Inhaltspfad** den Speicherort auf dem Zielcomputer an, auf dem SFT-Dateien gespeichert werden, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-144">On the **Content Path** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

   **<span data-ttu-id="9be94-145">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9be94-145">Note</span></span>**  
   <span data-ttu-id="9be94-146">Wenn der http-oder RTSP-Port für den Verwaltungs Server bereits zugewiesen ist, werden Sie aufgefordert, einen neuen Port zu wählen.</span><span class="sxs-lookup"><span data-stu-id="9be94-146">If the HTTP or RTSP port for the Management Server is already allocated, you will be prompted to choose a new port.</span></span> <span data-ttu-id="9be94-147">Wählen Sie den gewünschten Port aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="9be94-147">Select the desired port, and then click **Next**.</span></span>



13. <span data-ttu-id="9be94-148">Klicken Sie auf der Seite **bereit zum Installieren des Programms** auf **Installieren**, um den Application Virtualization-Verwaltungs Server zu installieren.</span><span class="sxs-lookup"><span data-stu-id="9be94-148">On the **Ready to Install the Program** page, to install the Application Virtualization Management Server, click **Install**.</span></span>

   **<span data-ttu-id="9be94-149">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9be94-149">Note</span></span>**  
   <span data-ttu-id="9be94-150">Wenn bei dem Versuch, diesen Schritt auszuführen, Fehler 25120 angezeigt wird, müssen Sie IIS- **Verwaltungsskripts und-Tools**aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9be94-150">If error 25120 is displayed when you try to complete this step, you need to enable IIS **Management Scripts and Tools**.</span></span> <span data-ttu-id="9be94-151">Um dieses Windows-Feature zu aktivieren, öffnen Sie die Systemsteuerung **Programme und Funktionen** , wählen Sie **Windows-Features aktivieren oder deaktivieren aus**, und navigieren Sie zu **Internet Informationsdienste.**</span><span class="sxs-lookup"><span data-stu-id="9be94-151">To enable this Windows feature, open the **Programs and Features** control panel, select **Turn Windows features on or off**, and navigate to **Internet Information Services.**</span></span>

   <span data-ttu-id="9be94-152">Aktivieren Sie unter **Webverwaltungstools**die **IIS-Verwaltungsskripts und-Tools**.</span><span class="sxs-lookup"><span data-stu-id="9be94-152">Under **Web Management Tools**, enable **IIS Management Scripts and Tools**.</span></span>



14. <span data-ttu-id="9be94-153">Klicken Sie auf dem Bildschirm **Installations-Assistent abgeschlossen** auf **Fertig stellen**, um den Assistenten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="9be94-153">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

   **<span data-ttu-id="9be94-154">Wichtig</span><span class="sxs-lookup"><span data-stu-id="9be94-154">Important</span></span>**  
   <span data-ttu-id="9be94-155">Es kann einige Minuten dauern, bis die Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9be94-155">The installation can take a few minutes to finish.</span></span> <span data-ttu-id="9be94-156">Über dem Windows-Desktop-Benachrichtigungsbereich blinkt eine Statusmeldung, die darauf hinweist, dass die Installation erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9be94-156">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

   <span data-ttu-id="9be94-157">Es ist nicht erforderlich, den Computer neu zu starten, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="9be94-157">It is not necessary to reboot the computer when prompted.</span></span> <span data-ttu-id="9be94-158">Um die Systemleistung zu optimieren, wird jedoch ein Neustart empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9be94-158">However, to optimize system performance, a reboot is recommended.</span></span>



## <span data-ttu-id="9be94-159">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9be94-159">Related topics</span></span>


[<span data-ttu-id="9be94-160">So installieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="9be94-160">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)









