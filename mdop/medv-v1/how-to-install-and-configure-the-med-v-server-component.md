---
title: So installieren und konfigurieren Sie die MED-V-Serverkomponente
description: So installieren und konfigurieren Sie die MED-V-Serverkomponente
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812079"
---
# <span data-ttu-id="48d50-103">So installieren und konfigurieren Sie die MED-V-Serverkomponente</span><span class="sxs-lookup"><span data-stu-id="48d50-103">How to Install and Configure the MED-V Server Component</span></span>


<span data-ttu-id="48d50-104">In diesem Abschnitt wird erläutert, wie Sie den MED-V-Server [Installieren](#bkmk-howtoinstallthemedvserver) und [Konfigurieren](#bkmk-howtoconfigurethemedvserver) .</span><span class="sxs-lookup"><span data-stu-id="48d50-104">This section explains how to [install](#bkmk-howtoinstallthemedvserver) and [configure](#bkmk-howtoconfigurethemedvserver) the MED-V server.</span></span>

## <a href="" id="bkmk-howtoinstallthemedvserver"></a><span data-ttu-id="48d50-105">Installieren des MED-V-Servers</span><span class="sxs-lookup"><span data-stu-id="48d50-105">How to Install the MED-V Server</span></span>


**<span data-ttu-id="48d50-106">So installieren Sie den MED-V-Server</span><span class="sxs-lookup"><span data-stu-id="48d50-106">To install the MED-V server</span></span>**

1.  <span data-ttu-id="48d50-107">Installieren Sie das MED-V Server. MSI-Paket.</span><span class="sxs-lookup"><span data-stu-id="48d50-107">Install the MED-V Server .msi package.</span></span>

    <span data-ttu-id="48d50-108">Das MED-V Server. MSI-Paket heißt *MED-V\_Server\_x.msi*, wobei x die Versionsnummer ist.</span><span class="sxs-lookup"><span data-stu-id="48d50-108">The MED-V Server .msi package is called *MED-V\_Server\_x.msi*, where x is the version number.</span></span>

    <span data-ttu-id="48d50-109">Beispiel: *MED-V\_Server\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="48d50-109">For example, *MED-V\_Server\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="48d50-110">Wenn der **Begrüßungs** Bildschirm des InstallShield-Assistenten angezeigt wird, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="48d50-110">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

3.  <span data-ttu-id="48d50-111">Lesen Sie auf dem Bildschirm **Lizenzvertrag** den Lizenzvertrag, klicken Sie auf **Ich stimme den Bedingungen des Lizenzvertrags**zu, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="48d50-111">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

    <span data-ttu-id="48d50-112">Der Bildschirm **Zielordner** wird angezeigt, und der Standardinstallationsordner wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48d50-112">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="48d50-113">Der Standardinstallationsordner ist *%systemdrive%\\Program c:\\Programme\\Microsoft Enterprise Desktop Virtualization\\*.</span><span class="sxs-lookup"><span data-stu-id="48d50-113">The default installation folder is *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.</span></span>

    -   <span data-ttu-id="48d50-114">Wenn Sie den Ordner ändern möchten, in dem MED-V installiert werden soll, klicken Sie auf **ändern** , und navigieren Sie zu einem vorhandenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="48d50-114">To change the folder where MED-V should be installed, click **Change** and browse to an existing folder.</span></span>

4.  <span data-ttu-id="48d50-115">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="48d50-115">Click **Next**.</span></span>

5.  <span data-ttu-id="48d50-116">Klicken Sie auf dem Bildschirm **bereit zum Installieren des Programms** auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="48d50-116">On the **Ready to Install the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="48d50-117">Die Installation von MED-V Server wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="48d50-117">The MED-V server installation starts.</span></span> <span data-ttu-id="48d50-118">Dies kann mehrere Minuten dauern, und auf dem Bildschirm wird möglicherweise kein Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48d50-118">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="48d50-119">Während der Installation werden mehrere Status Bildschirme angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48d50-119">During installation, several progress screens appear.</span></span> <span data-ttu-id="48d50-120">Wenn eine Meldung angezeigt wird, folgen Sie den Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="48d50-120">If a message appears, follow the instructions provided.</span></span>

6.  <span data-ttu-id="48d50-121">Wenn der Bildschirm **InstallShield-Assistent abgeschlossen** angezeigt wird, klicken Sie auf **Fertig stellen** , um den Assistenten abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="48d50-121">When the **InstallShield Wizard Completed** screen appears, click **Finish** to complete the wizard.</span></span>

**<span data-ttu-id="48d50-122">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="48d50-122">Note</span></span>**  
<span data-ttu-id="48d50-123">Wenn Sie den MED-V-Server über Microsoft Remote Desktop installieren, verwenden Sie die folgende Syntax: **mstsc/Administrator**. Stellen Sie sicher, dass Ihre RDP-Sitzung an die Konsole weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="48d50-123">If you are installing the MED-V server via Microsoft Remote Desktop, use the following syntax: **mstsc/admin**. Ensure that your RDP session is directed to the console.</span></span>



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a><span data-ttu-id="48d50-124">Konfigurieren des MED-V-Servers</span><span class="sxs-lookup"><span data-stu-id="48d50-124">How to Configure the MED-V Server</span></span>


<span data-ttu-id="48d50-125">Die folgenden Servereinstellungen können konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="48d50-125">The following server settings can be configured:</span></span>

-   [<span data-ttu-id="48d50-126">Verbindungen</span><span class="sxs-lookup"><span data-stu-id="48d50-126">Connections</span></span>](#bkmk-configuringconnections)

-   [<span data-ttu-id="48d50-127">Images</span><span class="sxs-lookup"><span data-stu-id="48d50-127">Images</span></span>](#bkmk-configuringimages)

-   [<span data-ttu-id="48d50-128">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="48d50-128">Permissions</span></span>](#bkmk-configuringpermissions)

-   [<span data-ttu-id="48d50-129">Berichte</span><span class="sxs-lookup"><span data-stu-id="48d50-129">Reports</span></span>](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a><span data-ttu-id="48d50-130">Konfigurieren von Verbindungen</span><span class="sxs-lookup"><span data-stu-id="48d50-130">Configuring Connections</span></span>

**<span data-ttu-id="48d50-131">So konfigurieren Sie Verbindungen</span><span class="sxs-lookup"><span data-stu-id="48d50-131">To configure connections</span></span>**

1.  <span data-ttu-id="48d50-132">Wählen Sie im Windows-Startmenü **Alle Programme &gt; Med-v &gt; Med-v Server Configuration Manager**aus.</span><span class="sxs-lookup"><span data-stu-id="48d50-132">On the Windows Start menu, select **All Programs &gt; MED-V &gt; MED-V Server Configuration Manager**.</span></span>

    **<span data-ttu-id="48d50-133">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="48d50-133">Note</span></span>**  
    <span data-ttu-id="48d50-134">Hinweis: Wenn Sie während der Server Installation das Kontrollkästchen **Med-v Server-Konfigurations-Manager starten** aktiviert haben, wird der Med-v Server-Konfigurations-Manager automatisch gestartet, nachdem die Server Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="48d50-134">Note: If you selected the **Launch MED-V Server Configuration Manager** check box during the server installation, the MED-V server configuration manager starts automatically after the server installation is complete.</span></span>



~~~
The MED-V Server Configuration Manager appears.
~~~

2. <span data-ttu-id="48d50-135">Konfigurieren Sie auf der Registerkarte **Verbindungen** die folgenden Clientverbindungseinstellungen:</span><span class="sxs-lookup"><span data-stu-id="48d50-135">On the **Connections** tab, configure the following client connections settings:</span></span>

   -   <span data-ttu-id="48d50-136">**Aktivieren von nicht verschlüsselten Verbindungen (http) mithilfe von Port**– aktivieren Sie dieses Kontrollkästchen, um unverschlüsselte Verbindungen über einen angegebenen Port zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="48d50-136">**Enable unencrypted connections (http), using port**—Select this check box to enable unencrypted connections using a specified port.</span></span> <span data-ttu-id="48d50-137">Geben Sie im Feld Port den Serverport ein, auf dem unverschlüsselte Verbindungen (http) akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="48d50-137">In the port box, enter the server port on which to accept unencrypted connections (http).</span></span>

   -   <span data-ttu-id="48d50-138">**Aktivieren von verschlüsselten Verbindungen (HTTPS) mithilfe von Port**– aktivieren Sie dieses Kontrollkästchen, um verschlüsselte Verbindungen über einen angegebenen Port zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="48d50-138">**Enable encrypted connections (https), using port**—Select this check box to enable encrypted connections using a specified port.</span></span> <span data-ttu-id="48d50-139">Geben Sie im Feld Port den Serverport ein, auf dem verschlüsselte Verbindungen (HTTPS) akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="48d50-139">In the port box, enter the server port on which to accept encrypted connections (https).</span></span>

       <span data-ttu-id="48d50-140">HTTPS ist eine optionale Konfiguration, mit der Sie sichere Transaktionen zwischen dem Med-v-Server und Med-v-Clients sicherstellen können.</span><span class="sxs-lookup"><span data-stu-id="48d50-140">Https is an optional configuration which can be set to ensure secure transactions between the MED-V server and MED-V clients.</span></span> <span data-ttu-id="48d50-141">Um HTTPS zu konfigurieren, müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="48d50-141">To configure https, you must perform the following procedures:</span></span>

       -   <span data-ttu-id="48d50-142">Konfigurieren Sie ein Zertifikat auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="48d50-142">Configure a certificate on the server.</span></span>

       -   <span data-ttu-id="48d50-143">Ordnen Sie das Serverzertifikat dem mit Netsh angegebenen Port zu.</span><span class="sxs-lookup"><span data-stu-id="48d50-143">Associate the server certificate with the port specified using netsh.</span></span> <span data-ttu-id="48d50-144">Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="48d50-144">For information, see the following:</span></span>

           -   [<span data-ttu-id="48d50-145">Netsh-Befehle für Hypertext Transfer Protocol (http)</span><span class="sxs-lookup"><span data-stu-id="48d50-145">Netsh Commands for Hypertext Transfer Protocol (HTTP)</span></span>](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [<span data-ttu-id="48d50-146">So wird es gemacht: Konfigurieren eines Ports mit einem SSL-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="48d50-146">How to: Configure a Port with an SSL Certificate</span></span>](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [<span data-ttu-id="48d50-147">So wird es gemacht: Konfigurieren eines Ports mit einem SSL-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="48d50-147">How to: Configure a Port with an SSL Certificate</span></span>](https://msdn.microsoft.com/library/ms733791.aspx)

3. <span data-ttu-id="48d50-148">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="48d50-148">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringimages"></a><span data-ttu-id="48d50-149">Konfigurieren von Bildern</span><span class="sxs-lookup"><span data-stu-id="48d50-149">Configuring Images</span></span>

**<span data-ttu-id="48d50-150">So konfigurieren Sie Bilder</span><span class="sxs-lookup"><span data-stu-id="48d50-150">To configure images</span></span>**

1.  <span data-ttu-id="48d50-151">Klicken Sie auf die Registerkarte **Bilder** .</span><span class="sxs-lookup"><span data-stu-id="48d50-151">Click the **Images** tab.</span></span>

2.  <span data-ttu-id="48d50-152">Konfigurieren Sie die folgenden Einstellungen für die Bildverwaltung:</span><span class="sxs-lookup"><span data-stu-id="48d50-152">Configure the following image management settings:</span></span>

    -   <span data-ttu-id="48d50-153">**VMS-Verzeichnis**– das Verzeichnis der virtuellen Computer (das Verzeichnis, in dem die Bilder gespeichert sind).</span><span class="sxs-lookup"><span data-stu-id="48d50-153">**VMs Directory**—The virtual machine directory (the directory where the images are stored).</span></span> <span data-ttu-id="48d50-154">Dieses Feld enthält einen UNC-Pfad zum Bildverzeichnis auf dem Bildverteilungsserver, auf das vom MED-V-Server aus zugegriffen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="48d50-154">This field contains a UNC path to the image directory on the image distribution server that should be accessible from the MED-V server.</span></span>

    -   <span data-ttu-id="48d50-155">**VMS-URL**– der Speicherort des Servers, auf dem die Bilder gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="48d50-155">**VMs URL**—The location of the server where the images are stored.</span></span>

3.  <span data-ttu-id="48d50-156">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="48d50-156">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringpermissions"></a><span data-ttu-id="48d50-157">Konfigurieren von Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="48d50-157">Configuring Permissions</span></span>

**<span data-ttu-id="48d50-158">So konfigurieren Sie Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="48d50-158">To configure permissions</span></span>**

1.  <span data-ttu-id="48d50-159">Klicken Sie auf die Registerkarte **Berechtigungen** .</span><span class="sxs-lookup"><span data-stu-id="48d50-159">Click the **Permissions** tab.</span></span>

2.  <span data-ttu-id="48d50-160">Es wird eine Liste aller Benutzer bereitgestellt, die sich anmelden können.</span><span class="sxs-lookup"><span data-stu-id="48d50-160">A list of all users who can log in is provided.</span></span> <span data-ttu-id="48d50-161">Wenn Sie Lese-und Schreibberechtigungen für einen Benutzer anwenden möchten, aktivieren Sie das Kontrollkästchen neben dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="48d50-161">To apply read and write permissions to a user, select the check box next to the user.</span></span> <span data-ttu-id="48d50-162">Deaktivieren Sie das Kontrollkästchen, um einem Benutzer schreibgeschützte Berechtigungen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="48d50-162">To apply read-only permissions to a user, clear the check box.</span></span>

3.  <span data-ttu-id="48d50-163">Klicken Sie zum Hinzufügen von Domänenbenutzern oder-Gruppen auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="48d50-163">To add domain users or groups, click **Add**.</span></span>

    <span data-ttu-id="48d50-164">Das Dialogfeld **Benutzer-oder Gruppennamen eingeben** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48d50-164">The **Enter User or Group names** dialog box appears.</span></span>

    1.  <span data-ttu-id="48d50-165">Wählen Sie Domänenbenutzer oder-Gruppen aus, indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="48d50-165">Select domain users or groups by doing one of the following:</span></span>

        -   <span data-ttu-id="48d50-166">Geben Sie im Feld **Benutzer-oder Gruppennamen eingeben** einen Benutzer oder eine Gruppe ein, der in der Domäne vorhanden oder als lokaler Benutzer oder eine Gruppe auf dem Computer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="48d50-166">In the **Enter User or Group names** field, type a user or group that exists in the domain or exists as a local user or group on the computer.</span></span> <span data-ttu-id="48d50-167">Klicken Sie dann auf **Namen überprüfen** , um Sie in den vollständigen vorhandenen Namen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="48d50-167">Then click **Check Names** to resolve it to the full existent name.</span></span>

        -   <span data-ttu-id="48d50-168">Klicken Sie auf **Suchen** , um das Dialogfeld **Benutzer oder Gruppen Standard auswählen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="48d50-168">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="48d50-169">Wählen Sie dann Domänenbenutzer oder Gruppen aus.</span><span class="sxs-lookup"><span data-stu-id="48d50-169">Then select domain users or groups.</span></span>

    2.  <span data-ttu-id="48d50-170">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="48d50-170">Click **OK**.</span></span>

4.  <span data-ttu-id="48d50-171">Wenn Sie Domänenbenutzer oder-Gruppen entfernen möchten, wählen Sie einen Benutzer oder eine Gruppe aus, und klicken Sie auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="48d50-171">To remove domain users or groups, select a user or group and click **Remove**.</span></span>

5.  <span data-ttu-id="48d50-172">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="48d50-172">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringreports"></a><span data-ttu-id="48d50-173">Konfigurieren von Berichten</span><span class="sxs-lookup"><span data-stu-id="48d50-173">Configuring Reports</span></span>

**<span data-ttu-id="48d50-174">So konfigurieren Sie Berichte</span><span class="sxs-lookup"><span data-stu-id="48d50-174">To configure reports</span></span>**

1.  <span data-ttu-id="48d50-175">Klicken Sie auf die Registerkarte **Berichte** .</span><span class="sxs-lookup"><span data-stu-id="48d50-175">Click the **Reports** tab.</span></span>

2.  <span data-ttu-id="48d50-176">Wenn Sie Berichte unterstützen möchten, wählen Sie **Berichte aktivieren**aus.</span><span class="sxs-lookup"><span data-stu-id="48d50-176">To support reports, select **Enable reports**.</span></span>

3.  <span data-ttu-id="48d50-177">Geben Sie im Feld **Verbindungszeichenfolge** eine Verbindungszeichenfolge für die MSSQL-Datenbank ein.</span><span class="sxs-lookup"><span data-stu-id="48d50-177">In the **Connection String** box, enter a connection string for the MSSQL database.</span></span>

    -   <span data-ttu-id="48d50-178">Wenn SQL Server auf einem Remoteserver installiert ist, verwenden Sie die folgende Verbindungszeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="48d50-178">When SQL Server is installed on a remote server, use the following connection string:</span></span>

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **<span data-ttu-id="48d50-179">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="48d50-179">Note</span></span>**  
        <span data-ttu-id="48d50-180">Hinweis: zum Herstellen einer Verbindung mit SQL Express verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="48d50-180">Note: To connect to SQL Express, use:</span></span> `Data Source=<ServerName>\sqlexpress.`



4.  <span data-ttu-id="48d50-181">Klicken Sie zum Erstellen der Datenbank auf **Datenbank erstellen**.</span><span class="sxs-lookup"><span data-stu-id="48d50-181">To create the database, click **Create Database**.</span></span>

5.  <span data-ttu-id="48d50-182">Klicken Sie auf **Verbindung testen**, um die Verbindung zu testen.</span><span class="sxs-lookup"><span data-stu-id="48d50-182">To test the connection, click **Test Connection**.</span></span>

6.  <span data-ttu-id="48d50-183">Klicken Sie auf **Optionen löschen**, um die Optionen zum Löschen von Datenbanken zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="48d50-183">To configure database clearing options, click **Clear Options**.</span></span>

    <span data-ttu-id="48d50-184">Das Dialogfeld **Datenbankoptionen löschen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48d50-184">The **Clear Database Options** dialog box appears.</span></span>

    1.  <span data-ttu-id="48d50-185">Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="48d50-185">Choose one of the following options:</span></span>

        -   <span data-ttu-id="48d50-186">**Löschen von Daten**, die älter als sind, löschen Sie alle Daten, die älter als die angegebene Anzahl von Tagen sind. Geben Sie im Feld Zahl eine Anzahl von Tagen ein.</span><span class="sxs-lookup"><span data-stu-id="48d50-186">**Clear data older than**—Clear all data older than the number of days specified; in the number box, enter a number of days.</span></span>

        -   <span data-ttu-id="48d50-187">**Löschen aller Daten aus einer Datenbank**– löschen Sie alle vorhandenen Daten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="48d50-187">**Clear all data from database**—Clear all existent data in the database.</span></span>

        -   <span data-ttu-id="48d50-188">**Drop Database**– löschen Sie die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="48d50-188">**Drop database**—Delete the database.</span></span>

    2.  <span data-ttu-id="48d50-189">Klicken Sie auf **OK** , um Änderungen zu übernehmen und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="48d50-189">Click **OK** to apply changes and close the dialog box.</span></span>

7.  <span data-ttu-id="48d50-190">Klicken Sie auf **OK** , um die Änderungen zu speichern, oder auf **Abbrechen** , um das Dialogfeld zu schließen, ohne die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="48d50-190">Click **OK** to save the changes, or click **Cancel** to close the dialog box without saving changes.</span></span>

8.  <span data-ttu-id="48d50-191">Wenn Sie dazu aufgefordert werden, starten Sie den MED-V-Server Dienst neu, um Änderungen auf die Netzwerkeinstellungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="48d50-191">If prompted, restart the MED-V server service to apply changes to the network settings.</span></span>

## <span data-ttu-id="48d50-192">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="48d50-192">Related topics</span></span>


[<span data-ttu-id="48d50-193">Unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="48d50-193">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="48d50-194">Entwerfen der MED-V-Server-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="48d50-194">Design the MED-V Server Infrastructure</span></span>](design-the-med-v-server-infrastructure.md)









