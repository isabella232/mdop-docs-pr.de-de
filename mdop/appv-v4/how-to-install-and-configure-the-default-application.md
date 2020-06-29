---
title: So installieren und konfigurieren Sie die Standardanwendung
description: So installieren und konfigurieren Sie die Standardanwendung
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807079"
---
# <span data-ttu-id="93ddd-103">So installieren und konfigurieren Sie die Standardanwendung</span><span class="sxs-lookup"><span data-stu-id="93ddd-103">How to Install and Configure the Default Application</span></span>


<span data-ttu-id="93ddd-104">Die Standardanwendung wird als Teil der Installation bereitgestellt und während der Installation automatisch auf den Microsoft Application Virtualization (App-V)-Verwaltungs Server kopiert.</span><span class="sxs-lookup"><span data-stu-id="93ddd-104">The default application is provided as part of the installation and is automatically copied to the Microsoft Application Virtualization (App-V) Management Server during installation.</span></span> <span data-ttu-id="93ddd-105">Sie wird verwendet, um zu überprüfen, ob der Verwaltungs Server ordnungsgemäß installiert und konfiguriert wurde, muss aber auf dem Microsoft Application Virtualization (App-V)-Client veröffentlicht werden, damit der Benutzer darauf zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="93ddd-105">It is used to verify that the Management Server was installed and configured correctly, but it has to be published to the Microsoft Application Virtualization (App-V) Client so that the user can access it.</span></span>

<span data-ttu-id="93ddd-106">Führen Sie die folgenden Verfahren aus, um die Standardanwendung zu veröffentlichen und zu streamen.</span><span class="sxs-lookup"><span data-stu-id="93ddd-106">Use the following procedures to publish the default application and to stream it.</span></span>

**<span data-ttu-id="93ddd-107">So veröffentlichen Sie die Standardanwendung</span><span class="sxs-lookup"><span data-stu-id="93ddd-107">To publish the default application</span></span>**

1.  <span data-ttu-id="93ddd-108">Melden Sie sich beim APP-v-Verwaltungs Server mit einem Konto an, das Mitglied der während der Installation angegebenen app-v-Administratorengruppe ist.</span><span class="sxs-lookup"><span data-stu-id="93ddd-108">Log on to the App-V Management Server by using an account that is a member of the App-V Administrators group specified during installation.</span></span>

2.  <span data-ttu-id="93ddd-109">Klicken Sie auf dem App-V-Verwaltungs Server auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Application Virtualization Management Console**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-109">On the App-V Management Server, click **Start**, click **Administrative Tools**, and then click **Application Virtualization Management Console**.</span></span>

3.  <span data-ttu-id="93ddd-110">Klicken Sie in der App-V-Verwaltungskonsole auf **Aktionen**, und klicken Sie dann auf mit **Application Virtualization System verbinden**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-110">In the App-V Management Console, click **Actions**, and then click **Connect to Application Virtualization System**.</span></span>

4.  <span data-ttu-id="93ddd-111">Deaktivieren Sie auf der Seite **Verbindung konfigurieren** das Kontrollkästchen **sichere Verbindung verwenden** .</span><span class="sxs-lookup"><span data-stu-id="93ddd-111">On the **Configure Connection** page, clear the **Use Secure Connection** check box.</span></span>

5.  <span data-ttu-id="93ddd-112">Geben Sie im Feld **Hostname des Webdiensts** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des App-V-Verwaltungsservers ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-112">In the **Web Service Host Name** box, type the fully qualified domain name (FQDN) of the App-V Management Server, and then click **OK**.</span></span>

    <span data-ttu-id="93ddd-113">**Hinweis**  Sie können **localhost** auch für den Webdienst-Hostnamen verwenden, wenn er auf dem Verwaltungs Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="93ddd-113">**Note** You can also use **localhost** for the Web Service Host name if it is installed on the Management Server.</span></span>

     

6.  <span data-ttu-id="93ddd-114">Klicken Sie in der App-V-Verwaltungskonsole mit der rechten Maustaste auf den **Server** Knoten, und klicken Sie auf **System Optionen**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-114">In the App-V Management Console, right-click the **Server** node, and click **System Options**.</span></span>

7.  <span data-ttu-id="93ddd-115">Geben Sie auf der Registerkarte **Allgemein** im Feld **Standardinhalts Pfad** den UNC-Pfad (Universal Naming Convention) zu dem Inhaltsordner ein, den Sie während der Installation auf dem Server erstellt haben. Beispiel: \ \ \ \ &lt; Server Name &gt; \\Content, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-115">On the **General** tab, in the **Default Content Path** box, enter the Universal Naming Convention (UNC) path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and then click **OK**.</span></span>

    <span data-ttu-id="93ddd-116">**Wichtig**  Verwenden Sie den FQDN für den Servernamen, damit der Client den Namen richtig auflösen kann.</span><span class="sxs-lookup"><span data-stu-id="93ddd-116">**Important** Use the FQDN for the server name so that the client can resolve the name correctly.</span></span>

     

8.  <span data-ttu-id="93ddd-117">Erweitern Sie in der App-V-Verwaltungskonsole im Navigationsbereich den **Server** Knoten, und klicken Sie dann auf **Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-117">In the App-V Management Console, in the navigation pane, expand the **Server** node, and then click **Applications**.</span></span>

9.  <span data-ttu-id="93ddd-118">Klicken Sie im Themenbereich auf **Standardanwendung**, und klicken Sie dann im Bereich **Aktionen** auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-118">In the topic pane, click **Default Application**, and then, in the **Actions** pane, click **Properties**.</span></span>

10. <span data-ttu-id="93ddd-119">Klicken Sie im Dialogfeld **Eigenschaften** neben dem Feld **OSD-Pfad** auf **Durchsuchen**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-119">In the **Properties** dialog box, next to the **OSD Path** box, click **Browse**.</span></span>

11. <span data-ttu-id="93ddd-120">Geben Sie im Dialogfeld **Öffnen** den UNC-Pfad zu dem Inhaltsordner ein, den Sie während der Installation auf dem Server erstellt haben. Beispiel: \ \ \ \ &lt; Server Name &gt; \\Content, und drücken Sie die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="93ddd-120">In the **Open** dialog box, enter the UNC path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and press ENTER.</span></span> <span data-ttu-id="93ddd-121">Sie müssen den tatsächlichen Servernamen verwenden und den **localhost** hier nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="93ddd-121">You must use the actual server name and cannot use the **localhost** here.</span></span>

    <span data-ttu-id="93ddd-122">**Wichtig**  Stellen Sie sicher, dass sich die Werte in den Feldern " **OSD-Pfad** **" und "Symbolpfad"** im UNC-Format befinden (beispielsweise \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ &lt; Server Name &gt; \\Content\\DefaultApp.ico) und auf den Inhaltsordner</span><span class="sxs-lookup"><span data-stu-id="93ddd-122">**Important** Ensure that the values in both the **OSD Path** and **Icon Path** boxes are in UNC format (for example, \\\\&lt;Server Name&gt;\\Content\\DefaultApp.ico), and point to the Content folder you created when installing the server.</span></span> <span data-ttu-id="93ddd-123">Verwenden Sie keine **localhost** -Datei oder einen Dateipfad, der einen Laufwerkbuchstaben wie c:\\Programme Files\\.. \\.. Inhalts.</span><span class="sxs-lookup"><span data-stu-id="93ddd-123">Do not use **localhost** or a file path containing a drive letter such as C:\\Program Files\\..\\..\\Content.</span></span>

     

12. <span data-ttu-id="93ddd-124">Wählen Sie die DefaultApp. OSD-Datei aus, und klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-124">Select the DefaultApp.osd file, and click **Open**.</span></span>

13. <span data-ttu-id="93ddd-125">Wiederholen Sie die vorherigen Schritte zum Konfigurieren des Symbolpfads.</span><span class="sxs-lookup"><span data-stu-id="93ddd-125">Repeat the previous steps to configure the icon path.</span></span>

14. <span data-ttu-id="93ddd-126">Klicken Sie auf die Registerkarte **Zugriffsberechtigungen** , und vergewissern Sie sich, dass die App-V-Benutzergruppe über Zugriffsberechtigungen für die Anwendung verfügt.</span><span class="sxs-lookup"><span data-stu-id="93ddd-126">Click the **Access Permissions** tab, and confirm that the App-V Users group has access permissions to the application.</span></span>

15. <span data-ttu-id="93ddd-127">Klicken Sie auf die Registerkarte **Verknüpfungen** , und klicken Sie dann auf **auf dem Desktop des Benutzers veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-127">Click the **Shortcuts** tab, and then click **Publish to User’s Desktop**.</span></span> <span data-ttu-id="93ddd-128">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="93ddd-128">Click **OK**.</span></span>

16. <span data-ttu-id="93ddd-129">Öffnen Sie den Windows-Explorer, und suchen Sie nach dem Inhaltsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="93ddd-129">Open Windows Explorer, and locate the Content directory.</span></span>

17. <span data-ttu-id="93ddd-130">Doppelklicken Sie auf die DefaultApp. OSD-Datei, und öffnen Sie Sie mit Editor.</span><span class="sxs-lookup"><span data-stu-id="93ddd-130">Double-click the DefaultApp.osd file, and open it with Notepad.</span></span>

18. <span data-ttu-id="93ddd-131">Suchen Sie die Zeile, die das **href** -Tag enthält, und ändern Sie Sie in den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="93ddd-131">Locate the line that contains the **HREF** tag, and change it to the following code:</span></span>

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    <span data-ttu-id="93ddd-132">Wenn Sie RTSPS verwenden:</span><span class="sxs-lookup"><span data-stu-id="93ddd-132">Or, if you are using RTSPS:</span></span>

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. <span data-ttu-id="93ddd-133">Schließen Sie die DefaultApp. OSD-Datei, und speichern Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="93ddd-133">Close the DefaultApp.osd file, and save the changes.</span></span>

**<span data-ttu-id="93ddd-134">So streamen Sie die Standardanwendung</span><span class="sxs-lookup"><span data-stu-id="93ddd-134">To stream the default application</span></span>**

1.  <span data-ttu-id="93ddd-135">Melden Sie sich auf dem Computer, auf dem der App-V-Client installiert ist, als Benutzer an, der Mitglied der Application Virtualization users-Gruppe ist, die während der Server Installation angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="93ddd-135">On the computer that has the App-V Client installed, log on as a user who is a member of the Application Virtualization Users group specified during server installation.</span></span>

2.  <span data-ttu-id="93ddd-136">Auf dem Desktop wird die **Standardtastenkombination der Application Virtualization-Anwendung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="93ddd-136">On the desktop, the **Default Application Virtualization Application** shortcut appears.</span></span> <span data-ttu-id="93ddd-137">Doppelklicken Sie auf die Verknüpfung, um die Anwendung zu starten.</span><span class="sxs-lookup"><span data-stu-id="93ddd-137">Double-click the shortcut to start the application.</span></span>

3.  <span data-ttu-id="93ddd-138">Eine Statusleiste, die über dem Windows-Infobereich angezeigt wird, gibt an, dass die Anwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="93ddd-138">A status bar, displayed above the Windows notification area, reports that the application is starting.</span></span> <span data-ttu-id="93ddd-139">Wenn der Anwendungsstart erfolgreich ist, wird der Titelbildschirm für die Standardanwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="93ddd-139">If the application startup is successful, the title screen for the default application is displayed.</span></span> <span data-ttu-id="93ddd-140">Klicken Sie auf **OK** , um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="93ddd-140">Click **OK** to close the dialog box.</span></span> <span data-ttu-id="93ddd-141">Sie haben nun bestätigt, dass das App-V-System ordnungsgemäß ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93ddd-141">You have now confirmed that the App-V system is running correctly.</span></span>

## <span data-ttu-id="93ddd-142">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="93ddd-142">Related topics</span></span>


[<span data-ttu-id="93ddd-143">So konfigurieren Sie Server für die serverbasierte Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="93ddd-143">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





