---
title: So aktualisieren Sie die Server und Systemkomponenten
description: So aktualisieren Sie die Server und Systemkomponenten
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806700"
---
# <span data-ttu-id="b2060-103">So aktualisieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="b2060-103">How to Upgrade the Servers and System Components</span></span>


<span data-ttu-id="b2060-104">Gehen Sie wie folgt vor, um Softwarekomponenten zu aktualisieren, die auf allen Application Virtualization System-Computern installiert sind.</span><span class="sxs-lookup"><span data-stu-id="b2060-104">Use the following procedure to upgrade software components installed on all Application Virtualization System computers.</span></span> <span data-ttu-id="b2060-105">Application Virtualization-System Dienste werden auf jedem Computer nach dem Upgrade automatisch neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="b2060-105">Application Virtualization System services will be restarted automatically on each computer after it has been upgraded.</span></span>

**<span data-ttu-id="b2060-106">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="b2060-106">Note</span></span>**  
-   <span data-ttu-id="b2060-107">Durch den Upgradevorgang werden alle Application Virtualization System-Dienste angehalten, wodurch das System außer Betrieb genommen wird.</span><span class="sxs-lookup"><span data-stu-id="b2060-107">The upgrade process stops all Application Virtualization System services, thereby taking the system out of service.</span></span> <span data-ttu-id="b2060-108">Benutzersitzungen sollten geschlossen werden, bevor Sie mit dem Upgradevorgang beginnen, und Sie sollten alle Application Virtualization Server-Dienste in Ihrer Umgebung beenden.</span><span class="sxs-lookup"><span data-stu-id="b2060-108">User sessions should be shut down before you begin the upgrade process, and you should stop all Application Virtualization Server services in your environment.</span></span>

-   <span data-ttu-id="b2060-109">Wenn Sie über mehr als einen Server verfügen, der den Zugriff auf die Application Virtualization-Datenbank freigibt, müssen alle diese Server offline geschaltet werden, während die Datenbank aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b2060-109">If you have more than one server that is sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="b2060-110">Sie sollten ihre normalen Geschäftsmethoden für das Datenbankupgrade befolgen, es empfiehlt sich jedoch, das Datenbankupgrade mithilfe einer Sicherungskopie der Datenbank zuerst auf einem Testserver zu testen.</span><span class="sxs-lookup"><span data-stu-id="b2060-110">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="b2060-111">Wählen Sie dann einen der Server für das erste Upgrade aus, um das Datenbankschema zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b2060-111">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="b2060-112">Nachdem die Produktionsdatenbank erfolgreich aktualisiert wurde, können Sie die anderen Server aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b2060-112">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

-   <span data-ttu-id="b2060-113">Sie können ein Upgrade auf Microsoft Application Virtualization (app-v) 4.5 nur von Microsoft Application Virtualization (app-v) 4.1 oder 4.1 SP1 durchführen.</span><span class="sxs-lookup"><span data-stu-id="b2060-113">You can upgrade to Microsoft Application Virtualization (App-V)4.5 only from Microsoft Application Virtualization (App-V)4.1 or4.1 SP1.</span></span> <span data-ttu-id="b2060-114">App-v 4.0 und frühere Versionen müssen vor dem Upgrade auf App-v 4.5 deinstalliert oder auf 4.1 oder 4.1 SP1 aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b2060-114">App-V4.0 and earlier must be uninstalled or upgraded to4.1 or4.1 SP1 before upgrading to App-V4.5.</span></span>

 

**<span data-ttu-id="b2060-115">So aktualisieren Sie Softwarekomponenten auf Computern mit Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="b2060-115">To upgrade software components on Application Virtualization System computers</span></span>**

1.  <span data-ttu-id="b2060-116">Navigieren Sie zum Speicherort des Setup Programms im Netzwerk, führen Sie entweder dieses Programm aus dem Netzwerk aus, oder kopieren Sie das zugehörige Verzeichnis auf den Zielcomputer, und doppelklicken Sie dann auf die Setup.exe-Datei.</span><span class="sxs-lookup"><span data-stu-id="b2060-116">Navigate to the location of the Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the Setup.exe file.</span></span>

2.  <span data-ttu-id="b2060-117">Klicken Sie auf der Seite **Willkommen** des Installations-Assistenten auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2060-117">On the **Welcome** page of the Installation Wizard, click **Next**.</span></span>

3.  <span data-ttu-id="b2060-118">Lesen Sie auf der Seite **Lizenzvertrag** den Lizenzvertrag, aktivieren Sie **Ich akzeptiere die Bedingungen des Lizenzvertrags**, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2060-118">On the **License Agreement** page, read the license agreement, check **I accept the terms in the license agreement**, and click **Next**.</span></span>

4.  <span data-ttu-id="b2060-119">Wenn die Seite **installierte Software** geöffnet wird und eine Liste der installierten Application Virtualization System-Komponenten und die Version der einzelnen Komponenten angezeigt wird, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2060-119">When the **Installed Software** page opens and displays a list of the installed Application Virtualization System components and the version of each component, click **Next**.</span></span>

5.  <span data-ttu-id="b2060-120">Lesen Sie auf der Seite **Warnung zum Verlust der Sitzung** die angezeigte Nachricht, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2060-120">On the **Session Loss Warning** page, read the displayed message and click **Next**.</span></span>

6.  <span data-ttu-id="b2060-121">Überprüfen Sie auf der Seite mit der **Konfigurationsdatenbank verbinden** den Inhalt auf der Seite, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2060-121">On the **Connect to Configuration Database** page, review the content on the page and click **Next**.</span></span>

7.  <span data-ttu-id="b2060-122">Wenn die Seite **Datenbank-Upgrade erforderlich** angezeigt wird, ist eine Datenbankaktualisierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b2060-122">If the **Database Upgrade Required** page is displayed, a database upgrade is required.</span></span> <span data-ttu-id="b2060-123">Geben Sie die Administratoranmeldeinformationen für die Datenbank ein, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2060-123">Enter the database administrative credentials, and then click **Next**.</span></span> <span data-ttu-id="b2060-124">Wenn diese Seite nicht angezeigt wird, fahren Sie mit Schritt 9 fort.</span><span class="sxs-lookup"><span data-stu-id="b2060-124">If this page is not displayed, skip to Step 9.</span></span>

8.  <span data-ttu-id="b2060-125">Aktivieren Sie auf der Seite **Backup-Konfigurationsdatenbank** die entsprechenden Kontrollkästchen, um die Sicherung durchzuführen und an einen vorhandenen Speicherort zu exportieren, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2060-125">On the **Backup Configuration Database** page, check the appropriate boxes to perform the backup and export it to an existing location, and then click **Next**.</span></span>

    <span data-ttu-id="b2060-126">**Wichtig**  Wenn Sie bei einem Fehler beim Upgrade auf die vorherige Version zurückgreifen möchten, stellen Sie sicher, dass Sie das Kontrollkästchen **eine Sicherungskopie der Konfigurationsdatenbank durchführen** oder die Konfigurationsdaten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="b2060-126">**Important** If you want to be able to roll back to the previous version in the event of an upgrade failure, make sure you check the **Perform a backup of the configuration database** box, or you will lose the configuration data.</span></span>

    <span data-ttu-id="b2060-127">Wenn Sie eine Datenbank mit VSS wiederherstellen möchten, müssen Sie zuerst den App-V-Server Dienst auf dem Verwaltungs Server beenden.</span><span class="sxs-lookup"><span data-stu-id="b2060-127">When you want to restore a database with VSS, you must first stop the App-V Server Service on the Management Server.</span></span> <span data-ttu-id="b2060-128">Dies sollte auf jedem Verwaltungsserver erfolgen, wenn mehr als ein Server mit der gleichen Datenbank verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b2060-128">This should be done on every Management server if there is more than one server connected to the same database.</span></span>

     

9.  <span data-ttu-id="b2060-129">Lesen Sie auf der ersten Seite der **Paketüberprüfung** den Inhalt, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2060-129">On the first **Package Validation** page, read the content and then click **Next**.</span></span>

10. <span data-ttu-id="b2060-130">Auf der zweiten **Paket Überprüfungs** Seite haben Sie die Möglichkeit, die Details der Paketüberprüfung in einem Editor-Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2060-130">On the second **Package Validation** page, you have the option of displaying the details of the package validation in a Notepad window.</span></span> <span data-ttu-id="b2060-131">Um die Details anzuzeigen, klicken Sie auf **Details**. Klicken Sie andernfalls auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2060-131">To see the details, click **Details**; otherwise, click **Next**.</span></span>

11. <span data-ttu-id="b2060-132">Klicken Sie auf der Seite **bereit zum Upgrade des Programms** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b2060-132">On the **Ready to Upgrade the Program** page, click **Next**.</span></span>

12. <span data-ttu-id="b2060-133">Klicken Sie auf der Seite **fertig gestellt des Installations-Assistenten** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="b2060-133">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

13. <span data-ttu-id="b2060-134">Wiederholen Sie die Schritte 1 bis 12 auf allen anderen Computern, auf denen Sie die Application Virtualization-Verwaltungskonsole oder die Application Virtualization Server-Softwarekomponente installiert haben.</span><span class="sxs-lookup"><span data-stu-id="b2060-134">Repeat steps 1–12 on all other computers where you installed the Application Virtualization Management Console or the Application Virtualization Server software component.</span></span>

    <span data-ttu-id="b2060-135">Nach dem Upgrade des Datenspeichers können Sie den normalen Vorgang fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="b2060-135">After upgrading the data store, you can resume normal operation.</span></span> <span data-ttu-id="b2060-136">(Der Datenspeicher wird beim Upgrade eines beliebigen Servers oder des App-V-Verwaltungs-Webdiensts aktualisiert.)</span><span class="sxs-lookup"><span data-stu-id="b2060-136">(The data store is upgraded when you upgrade any server or the App-V Management Web Service.)</span></span>

## <span data-ttu-id="b2060-137">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b2060-137">Related topics</span></span>


[<span data-ttu-id="b2060-138">Bereitstellung von Application Virtualization und Upgrade Aspekte</span><span class="sxs-lookup"><span data-stu-id="b2060-138">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





