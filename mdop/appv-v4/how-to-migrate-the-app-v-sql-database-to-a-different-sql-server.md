---
title: So migrieren Sie die SQL-Datenbank von App-V zu einem anderen SQL Server
description: So migrieren Sie die SQL-Datenbank von App-V zu einem anderen SQL Server
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806960"
---
# <span data-ttu-id="357c2-103">So migrieren Sie die SQL-Datenbank von App-V zu einem anderen SQL Server</span><span class="sxs-lookup"><span data-stu-id="357c2-103">How to Migrate the App-V SQL Database to a Different SQL Server</span></span>


<span data-ttu-id="357c2-104">In den folgenden Verfahren wird ausführlich beschrieben, wie Sie die SQL-Datenbank des Microsoft Application Virtualization (App-V)-Verwaltungsservers zu einem anderen SQL Server migrieren.</span><span class="sxs-lookup"><span data-stu-id="357c2-104">The following procedures describe in detail how to migrate the SQL database of the Microsoft Application Virtualization (App-V) Management Server to a different SQL Server.</span></span>

<span data-ttu-id="357c2-105">**Wichtig**  Diese Vorgehensweise setzt voraus, dass der App-V Server-Dienst beendet wird und dadurch verhindert wird, dass Endbenutzer Ihre Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="357c2-105">**Important** This procedure requires that the App-V server service is stopped and this will prevent end-users from using their applications.</span></span>

 

**<span data-ttu-id="357c2-106">So sichern Sie die App-V SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="357c2-106">To back up the App-V SQL database</span></span>**

1.  <span data-ttu-id="357c2-107">Öffnen Sie das Programm "Services. msc", und beenden Sie den App-V-Verwaltungsserverdienst auf allen Verwaltungsservern, die die zu migrierende Datenbank verwenden.</span><span class="sxs-lookup"><span data-stu-id="357c2-107">Open the Services.msc program and stop the App-V Management Server service on all Management Servers that use the database to be migrated.</span></span>

2.  <span data-ttu-id="357c2-108">Öffnen Sie auf dem Computer, auf dem sich die App-V-Datenbank befindet, SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="357c2-108">On the computer where the App-V database is located, open SQL Server Management Studio.</span></span>

3.  <span data-ttu-id="357c2-109">Erweitern Sie den Knoten **Datenbanken** , und suchen Sie die App-V-Datenbank (Standardname lautet APPVIRT).</span><span class="sxs-lookup"><span data-stu-id="357c2-109">Expand the **Databases** node and locate the App-V database (default name is APPVIRT).</span></span>

4.  <span data-ttu-id="357c2-110">Klicken Sie mit der rechten Maustaste auf die Datenbank, wählen Sie **Aufgaben** aus, und wählen Sie dann **sichern**aus.</span><span class="sxs-lookup"><span data-stu-id="357c2-110">Right-click the database and select **Tasks** and then select **Back Up**.</span></span>

5.  <span data-ttu-id="357c2-111">Stellen Sie sicher, dass das **Wiederherstellungsmodell** auf " **einfach** " und der **Sicherungstyp** auf " **voll**" festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="357c2-111">Verify that **Recovery model** is set to **SIMPLE** and the **Backup type** is set to **Full**.</span></span> <span data-ttu-id="357c2-112">Ändern Sie bei Bedarf den **Sicherungssatz** und die **Ziel** Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="357c2-112">Change the **Backup set** and **Destination** settings if it is necessary.</span></span>

6.  <span data-ttu-id="357c2-113">Klicken Sie auf **OK** , um die Datenbank zu sichern.</span><span class="sxs-lookup"><span data-stu-id="357c2-113">Click **OK** to back up the database.</span></span> <span data-ttu-id="357c2-114">Nachdem die Sicherung erfolgreich abgeschlossen wurde, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="357c2-114">After the backup has completed successfully, click **OK**.</span></span>

7.  <span data-ttu-id="357c2-115">Öffnen Sie Windows-Explorer, und navigieren Sie zu dem Ordner, der die Datenbanksicherungsdatei enthält, beispielsweise APPVIRT. BAK.</span><span class="sxs-lookup"><span data-stu-id="357c2-115">Open Windows Explorer and browse to the folder that contains the database backup file, for example APPVIRT.BAK.</span></span> <span data-ttu-id="357c2-116">Kopieren Sie die Datenbanksicherungsdatei auf den Zielcomputer, auf dem SQL Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="357c2-116">Copy the database backup file to the destination computer that is running SQL Server.</span></span>

**<span data-ttu-id="357c2-117">So stellen Sie die App-V SQL-Datenbank auf dem Zielcomputer wieder her</span><span class="sxs-lookup"><span data-stu-id="357c2-117">To restore the App-V SQL database to the destination computer</span></span>**

1.  <span data-ttu-id="357c2-118">Öffnen Sie auf dem Zielcomputer SQL Server Management Studio, klicken Sie mit der rechten Maustaste auf den Knoten **Datenbanken** , und wählen Sie **Datenbank wiederherstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="357c2-118">On the destination computer, open SQL Server Management Studio, right-click the **Databases** node and select **Restore Database**.</span></span>

2.  <span data-ttu-id="357c2-119">Wählen Sie unter **Quelle für wiederherstellen**die Option **vom Gerät aus** , und klicken Sie dann auf das Symbol "**..**.".</span><span class="sxs-lookup"><span data-stu-id="357c2-119">Under **Source for Restore**, choose **From device** and then click the “**…**”</span></span> <span data-ttu-id="357c2-120">.</span><span class="sxs-lookup"><span data-stu-id="357c2-120">button.</span></span>

3.  <span data-ttu-id="357c2-121">Stellen Sie im Dialogfeld **Sicherung angeben** sicher, dass das **Sicherungsmedium** auf **Datei** festgelegt ist, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="357c2-121">In the **Specify Backup** dialog box, make sure that the **Backup Media** is set to **File** and then click **Add**.</span></span>

4.  <span data-ttu-id="357c2-122">Wählen Sie die Sicherungsdatei aus, die Sie von dem ursprünglichen Computer, auf dem SQL Server ausgeführt wird, kopiert haben, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="357c2-122">Select the backup file that you copied from the original computer that is running SQL Server, and then click **OK**.</span></span>

5.  <span data-ttu-id="357c2-123">Klicken Sie auf **OK** , und wählen Sie dann den wiederherzustellenden Sicherungssatz aus.</span><span class="sxs-lookup"><span data-stu-id="357c2-123">Click **OK** and then click to select the backup set to restore.</span></span>

6.  <span data-ttu-id="357c2-124">Klicken Sie unter **Ziel für Wiederherstellung**auf die Dropdownliste für die **Datenbank** , und wählen Sie den Namen der App-V-Datenbank aus, beispielsweise APPVIRT.</span><span class="sxs-lookup"><span data-stu-id="357c2-124">Under **Destination for restore**, click the drop-down for **To database** and select the App-V database name, for example APPVIRT.</span></span>

7.  <span data-ttu-id="357c2-125">Klicken Sie auf **OK** , um die Wiederherstellung zu starten.</span><span class="sxs-lookup"><span data-stu-id="357c2-125">Click **OK** to start the restore.</span></span> <span data-ttu-id="357c2-126">Nachdem die Wiederherstellung erfolgreich abgeschlossen wurde, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="357c2-126">After the restore has completed successfully, click **OK**.</span></span>

8.  <span data-ttu-id="357c2-127">Erweitern Sie den Knoten **Sicherheit** , klicken Sie mit der rechten Maustaste auf **Anmeldungen** , und wählen Sie **neue Anmeldung**aus.</span><span class="sxs-lookup"><span data-stu-id="357c2-127">Expand the **Security** node, right-click **Logins** and select **New Login**.</span></span>

9.  <span data-ttu-id="357c2-128">Geben Sie im Feld **Anmelde Name** die Details des Netzwerkdienstkontos für den App-V-Verwaltungs Server im Format DOMAIN\\SERVERNAME $ ein.</span><span class="sxs-lookup"><span data-stu-id="357c2-128">In the **Login Name** field, enter the Network Service account details for the App-V Management Server in the format of DOMAIN\\SERVERNAME$.</span></span>

10. <span data-ttu-id="357c2-129">Wählen Sie auf der Seite **Allgemein** unter **Standarddatenbank** den Namen der App-V-Datenbank aus, beispielsweise APPVIRT, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="357c2-129">On the **General** page under **Default database** select the App-V database name, for example, APPVIRT, and then click **OK**.</span></span>

11. <span data-ttu-id="357c2-130">Klicken Sie unter **Seite auswählen**auf die Seite **Benutzerzuordnung** .</span><span class="sxs-lookup"><span data-stu-id="357c2-130">Under **Select a page**, click to select the **User Mapping** page.</span></span> <span data-ttu-id="357c2-131">Klicken Sie unter Benutzern, die **dieser Anmeldung zugeordnet**sind, auf das Kontrollkästchen in der Spalte **Karte** , um die App-V-Datenbank auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="357c2-131">Under **Users mapped to this login**, click the check box in the **Map** column to select the App-V database.</span></span>

12. <span data-ttu-id="357c2-132">Klicken Sie unter \*\*Datenbankrollenmitgliedschaft für: &lt; appvdatabasename &gt; \*\*auf **SFTEveryone** , und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="357c2-132">Under **Database role membership for: &lt;appvdatabasename&gt;**, click to select **SFTEveryone** and then click **OK**.</span></span>

13. <span data-ttu-id="357c2-133">Stellen Sie sicher, dass die Windows-Firewall auf dem neuen Computer, auf dem SQL Server ausgeführt wird, so konfiguriert ist, dass der App-V-Verwaltungs Server auf das System zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="357c2-133">Make sure that the Windows Firewall on the new computer that is running SQL Server is configured to allow the App-V Management Server to access the system.</span></span> <span data-ttu-id="357c2-134">Verwenden Sie unter **Verwaltungs Tools**das Programm **Windows-Firewall mit erweiterter Sicherheit** , um eine **Eingehende Regel** für den von SQL Server verwendeten Port zu erstellen (Standard ist Port 1433).</span><span class="sxs-lookup"><span data-stu-id="357c2-134">Under **Administrative Tools**, use the **Windows Firewall with Advanced Security** program to create an **Inbound Rule** for the port that is used by SQL Server (default is port 1433).</span></span>

**<span data-ttu-id="357c2-135">So migrieren Sie die Aufträge des App-V-SQL Server-Agents</span><span class="sxs-lookup"><span data-stu-id="357c2-135">To migrate the App-V SQL Server Agent jobs</span></span>**

1.  <span data-ttu-id="357c2-136">Erweitern Sie auf dem ursprünglichen Computer, auf dem SQL Server ausgeführt wird, in SQL Server Management Studio den Knoten **SQL Server-Agent** , und erweitern Sie dann den Knoten **Aufträge** .</span><span class="sxs-lookup"><span data-stu-id="357c2-136">On the original computer that is running SQL Server, in SQL Server Management Studio, expand the **SQL Server Agent** node, and then expand the **Jobs** node.</span></span>

2.  <span data-ttu-id="357c2-137">Klicken Sie mit der rechten Maustaste auf die folgenden vier App-V-Aufträge, und wählen Sie **Skript Auftrag als | aus. Erstellen in | Datei**, und speichern Sie jedes Skript in einem Ordner, und geben Sie jedem Skript einen aussagekräftigen Namen.</span><span class="sxs-lookup"><span data-stu-id="357c2-137">Right-click the following four App-V jobs and select **Script Job as | CREATE to | File**, and save each script to a folder and give each script a descriptive name.</span></span>

    -   **<span data-ttu-id="357c2-138">SoftGrid-Datenbank (appvdbname) Überprüfen des Verwendungs Verlaufs</span><span class="sxs-lookup"><span data-stu-id="357c2-138">Softgrid Database (appvdbname) Check Usage History</span></span>**

    -   **<span data-ttu-id="357c2-139">SoftGrid-Datenbank (appvdbname) schließen verwaister Sitzungen</span><span class="sxs-lookup"><span data-stu-id="357c2-139">Softgrid Database (appvdbname) Close Orphaned Sessions</span></span>**

    -   **<span data-ttu-id="357c2-140">SoftGrid-Datenbank (appvdbname) Größenbeschränkung erzwingen</span><span class="sxs-lookup"><span data-stu-id="357c2-140">Softgrid Database (appvdbname) Enforce Size Limit</span></span>**

    -   **<span data-ttu-id="357c2-141">SoftGrid-Datenbank (appvdbname) Monitor Benachrichtigung/Auftrags Status</span><span class="sxs-lookup"><span data-stu-id="357c2-141">Softgrid Database (appvdbname) Monitor Alert/Job Status</span></span>**

3.  <span data-ttu-id="357c2-142">Kopieren Sie die vier Skriptdateien (SQL) auf den Zielcomputer, auf dem SQL Server ausgeführt wird, und öffnen Sie SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="357c2-142">Copy the four script files (.sql) to the destination computer that is running SQL Server and open SQL Server Management Studio.</span></span>

4.  <span data-ttu-id="357c2-143">Klicken Sie im Windows-Explorer mit der rechten Maustaste auf jede SQL-Datei, und klicken Sie dann auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="357c2-143">In Windows Explorer, right-click each .sql file and then click **Run**.</span></span> <span data-ttu-id="357c2-144">Jedes Skript wird in einem Abfragefenster in SQL Server Management Studio geöffnet.</span><span class="sxs-lookup"><span data-stu-id="357c2-144">Each script will open in a query window in SQL Server Management Studio.</span></span> <span data-ttu-id="357c2-145">Klicken Sie für jedes Skript auf **Ausführen** , und überprüfen Sie, ob die einzelnen Skripts erfolgreich abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="357c2-145">Click **Execute** for each script and verify that each is completed successfully.</span></span>

5.  <span data-ttu-id="357c2-146">Aktualisieren Sie den Knoten **Aufträge** unter dem Knoten **SQL Server-Agent** , und bestätigen Sie, dass die vier Aufträge erfolgreich erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="357c2-146">Refresh the **Jobs** node under the **SQL Server Agent** node and confirm that the four jobs are created successfully.</span></span>

**<span data-ttu-id="357c2-147">So aktualisieren Sie die Konfiguration des App-V-Verwaltungsservers</span><span class="sxs-lookup"><span data-stu-id="357c2-147">To update the configuration of the App-V Management Server</span></span>**

1.  <span data-ttu-id="357c2-148">Ändern Sie auf dem App-V-Verwaltungs Server die folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="357c2-148">On the App-V Management Server, modify the following registry keys:</span></span>

    -   <span data-ttu-id="357c2-149">**SQLServerName**  =  &lt; Servername&gt;</span><span class="sxs-lookup"><span data-stu-id="357c2-149">**SQLServerName** = &lt;newservername&gt;</span></span>

    -   <span data-ttu-id="357c2-150">**SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;</span><span class="sxs-lookup"><span data-stu-id="357c2-150">**SQLServerPort** = &lt;newserverport&gt;</span></span>

    <span data-ttu-id="357c2-151">Starten Sie den App-V Server-Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="357c2-151">Then restart the App-V server service.</span></span>

2.  <span data-ttu-id="357c2-152">Navigieren Sie zu der Datei SftMgmt. udl unter dem App-V Management Server-Installationsverzeichnis (Standard ist c:\\Programme c:\\Programme\\Microsoft System Center App virt Management Server\\App virt-Verwaltungsdienst).</span><span class="sxs-lookup"><span data-stu-id="357c2-152">Browse to find the file SftMgmt.udl under the App-V Management Server installation directory (default is C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service).</span></span> <span data-ttu-id="357c2-153">Klicken Sie mit der rechten Maustaste auf die Datei, und wählen Sie **Öffnen**aus.</span><span class="sxs-lookup"><span data-stu-id="357c2-153">Right-click the file and select **Open**.</span></span>

3.  <span data-ttu-id="357c2-154">Geben Sie auf der Registerkarte **Verbindung** den Namen des Zielcomputers ein, auf dem SQL Server ausgeführt wird, und klicken Sie dann auf **Verbindung testen**.</span><span class="sxs-lookup"><span data-stu-id="357c2-154">On the **Connection** tab, enter the name of the destination computer that is running SQL Server, and then click **Test Connection**.</span></span> <span data-ttu-id="357c2-155">Wenn der Test erfolgreich war, klicken Sie auf **OK** , und klicken Sie dann erneut auf **OK** .</span><span class="sxs-lookup"><span data-stu-id="357c2-155">When the test is successful, click **OK** and then click **OK** again.</span></span>

4.  <span data-ttu-id="357c2-156">Für App-V Management Server-Versionen vor 4,5 SP2 müssen Sie die SQL-Protokollierungseinstellungen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="357c2-156">For App-V Management Server versions before 4.5 SP2, you must update the SQL Logging settings.</span></span> <span data-ttu-id="357c2-157">Klicken Sie unter **Servergruppen**mit der rechten Maustaste auf die Servergruppe, der der Server angehört, und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="357c2-157">Under **Server Groups**, right-click the server group the server is a member of and select **Properties**.</span></span>

5.  <span data-ttu-id="357c2-158">Klicken Sie auf der Registerkarte **Protokollierung** auf den Eintrag **SQL-Datenbank** , und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="357c2-158">On the **Logging** tab click to select the **SQL Database** entry and then click **Edit**.</span></span>

6.  <span data-ttu-id="357c2-159">Ändern Sie den **Namen des DNS-Hosts** in den Hostnamen des neuen Computers, auf dem SQL Server ausgeführt wird, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="357c2-159">Change the **DNS Host Name** to the host name of the new computer that is running SQL Server and then click **OK**.</span></span> <span data-ttu-id="357c2-160">Klicken Sie zwei Mal auf **OK** , und starten Sie den App-V-Server Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="357c2-160">Click **OK** two times more, and then restart the App-V server service.</span></span>

7.  <span data-ttu-id="357c2-161">Öffnen Sie die App-V-Verwaltungskonsole, klicken Sie mit der rechten Maustaste auf den Knoten **Anwendungen** , und wählen Sie **Aktualisieren**aus.</span><span class="sxs-lookup"><span data-stu-id="357c2-161">Open the App-V Management Console, right-click the **Applications** node and select **Refresh**.</span></span> <span data-ttu-id="357c2-162">Die Liste der Anwendungen sollte wie zuvor angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="357c2-162">The list of applications should be displayed as before.</span></span>

 

 





