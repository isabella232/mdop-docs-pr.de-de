---
title: So installieren Sie die Application Virtualization Streaming Server
description: So installieren Sie die Application Virtualization Streaming Server
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807063"
---
# <span data-ttu-id="52eba-103">So installieren Sie die Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="52eba-103">How to Install the Application Virtualization Streaming Server</span></span>


<span data-ttu-id="52eba-104">Der Application Virtualization Streaming Server veröffentlicht seine Anwendungen für Clients.</span><span class="sxs-lookup"><span data-stu-id="52eba-104">The Application Virtualization Streaming Server publishes its applications to clients.</span></span> <span data-ttu-id="52eba-105">In einer Umgebung mit Lastenausgleich, die für große Bereitstellungen typisch ist, sollten alle Server in einer Servergruppe dieselben Anwendungen streamen.</span><span class="sxs-lookup"><span data-stu-id="52eba-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="52eba-106">Wenn Application Virtualization Streaming-Server verschiedene Anwendungen streamen sollen, weisen Sie die Server verschiedenen Servergruppen zu.</span><span class="sxs-lookup"><span data-stu-id="52eba-106">If Application Virtualization Streaming Servers are to stream different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="52eba-107">In diesem Fall müssen Sie möglicherweise auch die Kapazität einer Servergruppe erhöhen.</span><span class="sxs-lookup"><span data-stu-id="52eba-107">In this case, you might also have to increase a server group's capacity.</span></span>

<span data-ttu-id="52eba-108">Wenn Sie einen Zielcomputer im Netzwerk festgelegt haben, mit einem Anmeldekonto, das über lokale Administratorrechte verfügt, können Sie mit dem folgenden Verfahren den Application Virtualization Streaming Server installieren und der entsprechenden Servergruppe zuweisen.</span><span class="sxs-lookup"><span data-stu-id="52eba-108">If you have designated a target computer on the network, with a logon account having local administrative privileges, you can use the following procedure to install the Application Virtualization Streaming Server and assign it to the appropriate server group.</span></span>

<span data-ttu-id="52eba-109">**Hinweis**  Der Installations-Assistent kann einen Servergruppen Eintrag erstellen, wenn er nicht vorhanden ist, und einen Eintrag der Application Virtualization Streaming Server-Mitgliedschaft in dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="52eba-109">**Note** The Installation Wizard can create a server group record, if one does not exist, and a record of the Application Virtualization Streaming Server membership in this group.</span></span>

 

<span data-ttu-id="52eba-110">Nachdem Sie den Installationsvorgang abgeschlossen haben, starten Sie den Server neu.</span><span class="sxs-lookup"><span data-stu-id="52eba-110">After you complete the installation process, restart the server.</span></span>

**<span data-ttu-id="52eba-111">So installieren Sie einen Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="52eba-111">To install an Application Virtualization Streaming Server</span></span>**

1.  <span data-ttu-id="52eba-112">Stellen Sie sicher, dass auf Ihrem Zielcomputer keine früheren Versionen von Application Virtualization Streaming Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="52eba-112">Verify that no earlier versions of the Application Virtualization Streaming Server are installed on your target computer.</span></span>

    <span data-ttu-id="52eba-113">**Wichtig**  Stellen Sie sicher, dass der App-V-Verwaltungs Server auf diesem Computer nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="52eba-113">**Important** Make sure that the App-V Management Server is not installed on this computer.</span></span> <span data-ttu-id="52eba-114">Die beiden Produkte können nicht auf demselben Computer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="52eba-114">The two products cannot be installed on the same computer.</span></span>

     

2.  <span data-ttu-id="52eba-115">Navigieren Sie zum Speicherort des Application Virtualization System Setup-Programms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf die **Setup.exe** -Datei.</span><span class="sxs-lookup"><span data-stu-id="52eba-115">Navigate to the location of the Application Virtualization System Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="52eba-116">Klicken Sie auf der Seite **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="52eba-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="52eba-117">Wählen Sie auf der Seite **Lizenzvertrag** die Option **Ich akzeptiere die**Lizenzbedingungen aus, und klicken Sie dann auf **weiter**, um die Lizenzbedingungen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="52eba-117">On the **License Agreement** page, to accept the license terms, select **I accept the licensing terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="52eba-118">Geben Sie auf der Seite **Kundeninformationen** den **Benutzernamen** und die Organisation an, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="52eba-118">On the **Customer Information** page, specify the **User name** and the organization, and then click **Next**.</span></span>

6.  <span data-ttu-id="52eba-119">Klicken Sie auf der Seite **Installationspfad** auf **Durchsuchen**, geben Sie den Speicherort an, an dem Sie den Streamingserver installieren möchten, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="52eba-119">On the **Installation Path** page, click **Browse**, specify the location where you want to install the Streaming Server, and then click **Next**.</span></span>

7.  <span data-ttu-id="52eba-120">Wählen Sie auf der Seite **Verbindungssicherheitsmodus** in der Dropdownliste das gewünschte Zertifikat aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="52eba-120">On the **Connection Security Mode** page, select the desired certificate from the drop-down list, and then click **Next**.</span></span>

    <span data-ttu-id="52eba-121">**Hinweis**  Bei der Einstellung für den **sicheren Verbindungsmodus** muss der Server über ein Serverzertifikat verfügen, das von einer öffentlichen Schlüsselinfrastruktur bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="52eba-121">**Note** The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="52eba-122">Wenn ein Serverzertifikat nicht auf dem Server installiert ist, ist diese Option nicht verfügbar und kann nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="52eba-122">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="52eba-123">Sie müssen dem Netzwerkdienstkonto Lesezugriff auf das verwendete Zertifikat gewähren.</span><span class="sxs-lookup"><span data-stu-id="52eba-123">You must grant the Network Service account read access to the certificate being used.</span></span>

     

8.  <span data-ttu-id="52eba-124">Wählen Sie auf der Seite **TCP-Portkonfiguration** die Option **Standardanschluss verwenden (554)** aus, um den Standardport (554) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="52eba-124">On the **TCP Port Configuration** page, to use the standard port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="52eba-125">Wenn Sie einen benutzerdefinierten Port angeben möchten, wählen Sie **benutzerdefinierten Port verwenden**aus, geben Sie die Portnummer in dem bereitgestellten Feld an, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="52eba-125">To specify a custom port, select **Use custom port**, specify the port number in the field provided, and then click **Next**.</span></span>

    <span data-ttu-id="52eba-126">**Hinweis**  Wenn Sie den Server in einem nicht sicheren Szenario installieren, können Sie den Standardport (554) verwenden, oder Sie können einen benutzerdefinierten Port definieren.</span><span class="sxs-lookup"><span data-stu-id="52eba-126">**Note** When you install the server in a nonsecure scenario, you can use the default port (554), or you can define a custom port.</span></span>

     

9.  <span data-ttu-id="52eba-127">Geben Sie auf der Seite **Inhaltsstamm** den Speicherort auf dem Zielcomputer an, auf dem SFT-Dateien gespeichert werden, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="52eba-127">On the **Content Root** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

    <span data-ttu-id="52eba-128">**Hinweis**  Wenn der http-oder RTSP-Port für den Virtual Application Streaming Server bereits zugewiesen ist, werden Sie aufgefordert, einen neuen Port auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="52eba-128">**Note** If the HTTP or RTSP port for the Virtual Application Streaming Server is already allocated, you will be prompted to select a new port.</span></span> <span data-ttu-id="52eba-129">Geben Sie den gewünschten Port an, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="52eba-129">Specify the desired port, and then click **Next**.</span></span>

     

10. <span data-ttu-id="52eba-130">Geben Sie auf dem Bildschirm **Erweiterte Einstellungen** die folgenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="52eba-130">On the **Advanced Setting** screen, enter the following information:</span></span>

    1.  **<span data-ttu-id="52eba-131">Max-Clientverbindungen</span><span class="sxs-lookup"><span data-stu-id="52eba-131">Max client connections</span></span>**

    2.  **<span data-ttu-id="52eba-132">Verbindungstimeout (Sek.)</span><span class="sxs-lookup"><span data-stu-id="52eba-132">Connection timeout (sec)</span></span>**

    3.  **<span data-ttu-id="52eba-133">RTSP-Threadpoolgröße</span><span class="sxs-lookup"><span data-stu-id="52eba-133">RTSP thread pool size</span></span>**

    4.  **<span data-ttu-id="52eba-134">RTSP-Timeout (Sek.)</span><span class="sxs-lookup"><span data-stu-id="52eba-134">RTSP timeout (sec)</span></span>**

    5.  **<span data-ttu-id="52eba-135">Anzahl der Kernprozesse</span><span class="sxs-lookup"><span data-stu-id="52eba-135">Number of core processes</span></span>**

    6.  **<span data-ttu-id="52eba-136">Core-Timeout (Sek.)</span><span class="sxs-lookup"><span data-stu-id="52eba-136">Core timeout (sec)</span></span>**

    7.  **<span data-ttu-id="52eba-137">Aktivieren der Benutzerauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="52eba-137">Enable User authentication</span></span>**

    8.  **<span data-ttu-id="52eba-138">Aktivieren der Benutzerautorisierung</span><span class="sxs-lookup"><span data-stu-id="52eba-138">Enable User authorization</span></span>**

    9.  **<span data-ttu-id="52eba-139">Cache Blockgröße (KB)</span><span class="sxs-lookup"><span data-stu-id="52eba-139">Cache block size (KB)</span></span>**

    10. **<span data-ttu-id="52eba-140">Maximale Cachegröße (MB)</span><span class="sxs-lookup"><span data-stu-id="52eba-140">Maximum cache size (MB)</span></span>**

    <span data-ttu-id="52eba-141">**Hinweis**  Der App-V-Streamingserver verwendet NTFS-Dateisystemberechtigungen zum Steuern des Zugriffs auf die Anwendungen unter der Inhaltsfreigabe.</span><span class="sxs-lookup"><span data-stu-id="52eba-141">**Note** The App-V Streaming Server uses NTFS file system permissions to control access to the applications under the Content share.</span></span> <span data-ttu-id="52eba-142">Verwenden Sie **Benutzerauthentifizierung aktivieren** , und aktivieren Sie die **Benutzerautorisierung** , um zu steuern, ob der Server diese Zugriffssteuerungslisten (ACLs) überprüft und erzwingt.</span><span class="sxs-lookup"><span data-stu-id="52eba-142">Use **Enable User authentication** and **Enable User authorization** to control whether the server checks and enforces those access control lists (ACLs) or not.</span></span>

     

11. <span data-ttu-id="52eba-143">Klicken Sie auf der Seite **bereit zum Installieren des Programms** auf **Installieren**, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="52eba-143">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

12. <span data-ttu-id="52eba-144">Klicken Sie auf dem Bildschirm **Installations-Assistent abgeschlossen** auf **Fertig stellen**, um den Assistenten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="52eba-144">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="52eba-145">**Wichtig**  Es kann einige Minuten dauern, bis die Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="52eba-145">**Important** The installation can take several minutes to finish.</span></span> <span data-ttu-id="52eba-146">Über dem Windows-Desktop-Benachrichtigungsbereich blinkt eine Statusmeldung, die darauf hinweist, dass die Installation erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="52eba-146">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

    <span data-ttu-id="52eba-147">Es ist nicht erforderlich, den Computer neu zu starten, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="52eba-147">It is not required to restart the computer when you are prompted.</span></span> <span data-ttu-id="52eba-148">Um die Systemleistung zu optimieren, empfehlen wir jedoch einen Neustart.</span><span class="sxs-lookup"><span data-stu-id="52eba-148">However, to optimize system performance, we recommend a restart.</span></span>

     

13. <span data-ttu-id="52eba-149">Wiederholen Sie die Schritte 1 bis 12 für jeden virtuellen Anwendungs Server, den Sie installieren müssen.</span><span class="sxs-lookup"><span data-stu-id="52eba-149">Repeat Steps 1–12 for each Virtual Application Server that you have to install.</span></span>

## <span data-ttu-id="52eba-150">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="52eba-150">Related topics</span></span>


[<span data-ttu-id="52eba-151">So installieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="52eba-151">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





