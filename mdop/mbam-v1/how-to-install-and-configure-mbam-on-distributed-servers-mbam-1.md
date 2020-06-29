---
title: Installieren und Konfigurieren von MBAM auf verteilten Servern
description: Installieren und Konfigurieren von MBAM auf verteilten Servern
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811287"
---
# <span data-ttu-id="00101-103">Installieren und Konfigurieren von MBAM auf verteilten Servern</span><span class="sxs-lookup"><span data-stu-id="00101-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="00101-104">Die Verfahren in diesem Thema beschreiben die vollständige Installation der Features Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) auf verteilten Servern.</span><span class="sxs-lookup"><span data-stu-id="00101-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on distributed servers.</span></span>

<span data-ttu-id="00101-105">Jedes Server Feature hat bestimmte Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="00101-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="00101-106">Wenn Sie sicherstellen möchten, dass Sie die Voraussetzungen und Hardware-und Softwareanforderungen erfüllt haben, lesen Sie [MBAM 1,0-Bereitstellungsvoraussetzungen](mbam-10-deployment-prerequisites.md) und [MBAM 1,0-unterstützte Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="00101-106">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="00101-107">Darüber hinaus erfordern einige Features, dass Sie während des Installationsvorgangs bestimmte Informationen bereitstellen, um das Feature erfolgreich bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="00101-107">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span>

**<span data-ttu-id="00101-108">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="00101-108">Note</span></span>**  
<span data-ttu-id="00101-109">Um die Setupprotokolldateien zu erhalten, müssen Sie MBAM installieren, indem Sie das **msiexec** -Paket und die Option " \*\*/l &lt; Location &gt; \*\* " verwenden.</span><span class="sxs-lookup"><span data-stu-id="00101-109">To obtain the setup log files, you have to install MBAM by using the **msiexec** package and the **/l &lt;location&gt;** option.</span></span> <span data-ttu-id="00101-110">Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="00101-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="00101-111">Zusätzliche Setupprotokolldateien werden im Ordner "% Temp%" des Benutzers erstellt, der die MBAM-Installation ausführt.</span><span class="sxs-lookup"><span data-stu-id="00101-111">Additional setup log files are created in the %temp% folder of the user that runs the MBAM installation.</span></span>



## <a href="" id="deploy-the-mbam-server-features-"></a><span data-ttu-id="00101-112">Bereitstellen der MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="00101-112">Deploy the MBAM Server features</span></span>


<span data-ttu-id="00101-113">In den folgenden Schritten wird beschrieben, wie die allgemeinen MBAM-Features installiert werden.</span><span class="sxs-lookup"><span data-stu-id="00101-113">The following steps describe how to install the general MBAM features.</span></span>

**<span data-ttu-id="00101-114">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="00101-114">Note</span></span>**  
<span data-ttu-id="00101-115">Stellen Sie sicher, dass Sie das 32-Bit-Setup auf 32-Bit-Servern und das 64-Bit-Setup auf 64-Bit-Servern verwenden.</span><span class="sxs-lookup"><span data-stu-id="00101-115">Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>



**<span data-ttu-id="00101-116">So stellen Sie MBAM-Server Features bereit</span><span class="sxs-lookup"><span data-stu-id="00101-116">To Deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="00101-117">Starten Sie den MBAM-Installations-Assistenten, und klicken Sie auf der Willkommensseite auf **Installieren** .</span><span class="sxs-lookup"><span data-stu-id="00101-117">Start the MBAM installation wizard, and click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="00101-118">Lesen und akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="00101-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="00101-119">Standardmäßig sind alle MBAM-Features für die Installation ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="00101-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="00101-120">Deaktivieren Sie die Features, die Sie an anderer Stelle installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="00101-120">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="00101-121">Features, die Sie auf demselben Computer installieren möchten, müssen alle zur gleichen Zeit installiert sein.</span><span class="sxs-lookup"><span data-stu-id="00101-121">Features that you want to install on the same computer must be installed all at the same time.</span></span> <span data-ttu-id="00101-122">MBAM-Features müssen in der folgenden Reihenfolge installiert werden:</span><span class="sxs-lookup"><span data-stu-id="00101-122">MBAM features must be installed in the following order:</span></span>

    -   <span data-ttu-id="00101-123">Wiederherstellungs-und Hardware Datenbank</span><span class="sxs-lookup"><span data-stu-id="00101-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="00101-124">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="00101-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="00101-125">Konformitätsprüfung und Berichte</span><span class="sxs-lookup"><span data-stu-id="00101-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="00101-126">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="00101-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="00101-127">MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="00101-127">MBAM Group Policy Template</span></span>

    **<span data-ttu-id="00101-128">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="00101-128">Note</span></span>**  
    <span data-ttu-id="00101-129">Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an.</span><span class="sxs-lookup"><span data-stu-id="00101-129">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="00101-130">Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="00101-130">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="00101-131">Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken.</span><span class="sxs-lookup"><span data-stu-id="00101-131">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="00101-132">Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="00101-132">If all prerequisites are met this time, the installation will resume.</span></span>



4.  <span data-ttu-id="00101-133">Der MBAM-Setup-Assistent zeigt die Installationsseiten für die ausgewählten Features an.</span><span class="sxs-lookup"><span data-stu-id="00101-133">The MBAM Setup wizard will display the installation pages for the selected features.</span></span> <span data-ttu-id="00101-134">In den folgenden Abschnitten werden die Installationsverfahren für die einzelnen Features beschrieben.</span><span class="sxs-lookup"><span data-stu-id="00101-134">The following sections describe the installation procedures for each feature.</span></span>

    **<span data-ttu-id="00101-135">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="00101-135">Note</span></span>**  
    <span data-ttu-id="00101-136">In der Regel wird jedes Feature auf einem separaten Server installiert.</span><span class="sxs-lookup"><span data-stu-id="00101-136">Typically, each feature is installed on a separate server.</span></span> <span data-ttu-id="00101-137">Wenn Sie mehrere Features auf einem einzelnen Server installieren möchten, können Sie einige der folgenden Schritte ändern oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="00101-137">If you want to install multiple features on a single server, you may change or eliminate some of the following steps.</span></span>



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   <span data-ttu-id="00101-138">Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="00101-138">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

6. <span data-ttu-id="00101-139">Wenn die ausgewählten MBAM-Funktionsinformationen abgeschlossen sind, können Sie die MBAM-Installation mit dem Setup-Assistenten starten.</span><span class="sxs-lookup"><span data-stu-id="00101-139">When the selected MBAM feature information is complete, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="00101-140">Klicken Sie auf **zurück** , um den Assistenten zu durchlaufen, wenn Sie Ihre Installationseinstellungen überprüfen oder ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="00101-140">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="00101-141">Klicken Sie auf **Installieren** , um mit der Installation zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="00101-141">Click **Install** to begin the installation.</span></span> <span data-ttu-id="00101-142">Klicken Sie auf **Abbrechen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="00101-142">Click **Cancel** to exit the Wizard.</span></span> <span data-ttu-id="00101-143">Setup installiert die von Ihnen ausgewählten MBAM-Features und benachrichtigt Sie, dass die Installation abzuschließen ist.</span><span class="sxs-lookup"><span data-stu-id="00101-143">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

7. <span data-ttu-id="00101-144">Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="00101-144">Click **Finish** to exit the wizard.</span></span>

8. <span data-ttu-id="00101-145">Fügen Sie Benutzer zu geeigneten MBAM-Rollen hinzu, nachdem die MBAM-Server Features installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="00101-145">Add users to appropriate MBAM roles, after the MBAM server features are installed..</span></span> <span data-ttu-id="00101-146">Weitere Informationen finden Sie unter [Planen von MBAM 1,0-Administrator Rollen](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="00101-146">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="00101-147">Konfiguration nach der Installation</span><span class="sxs-lookup"><span data-stu-id="00101-147">Post-installation configuration</span></span>**

1.  <span data-ttu-id="00101-148">Nach Abschluss des MBAM-Setups müssen Sie Benutzerrollen hinzufügen, bevor Benutzer auf Features auf der MBAM-Verwaltungswebsite zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="00101-148">After MBAM Setup is finished, you must add user Roles before users can access to features in the MBAM administration website.</span></span> <span data-ttu-id="00101-149">Fügen Sie auf dem Verwaltungs-und Überwachungs Server den folgenden lokalen Gruppen Benutzer hinzu.</span><span class="sxs-lookup"><span data-stu-id="00101-149">On the Administration and Monitoring Server, add users to the following local groups.</span></span>

    -   <span data-ttu-id="00101-150">**MBAM-Hardware Benutzer**: Mitglieder dieser lokalen Gruppe können auf das Hardware Feature auf der MBAM-Verwaltungswebsite zugreifen.</span><span class="sxs-lookup"><span data-stu-id="00101-150">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="00101-151">**MBAM Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe können auf die Drive Recovery zugreifen und TPM-Features (Trusted Platform Modules) auf der MBAM-Verwaltungswebsite verwalten.</span><span class="sxs-lookup"><span data-stu-id="00101-151">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage Trusted Platform Modules (TPM) features in the MBAM administration website.</span></span> <span data-ttu-id="00101-152">Alle Felder in Laufwerk Wiederherstellung und TPM verwalten sind für einen Helpdesk-Benutzer Pflichtfelder.</span><span class="sxs-lookup"><span data-stu-id="00101-152">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="00101-153">**MBAM Advanced Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe haben erweiterten Zugriff auf die Drive Recovery-und TPM-Features auf der MBAM-Verwaltungswebsite.</span><span class="sxs-lookup"><span data-stu-id="00101-153">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="00101-154">Für erfahrene Helpdesk-Benutzer ist in Drive Recovery nur das Schlüssel-ID-Feld erforderlich.</span><span class="sxs-lookup"><span data-stu-id="00101-154">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="00101-155">In TPM verwalten sind nur das Feld Computerdomäne und das Feld Computer Name erforderlich.</span><span class="sxs-lookup"><span data-stu-id="00101-155">In Manage TPM, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="00101-156">Fügen Sie auf der Verwaltungs-und Überwachungsserver-, Konformitäts-und Überwachungsdatenbank sowie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte gehostet werden, Benutzer zur folgenden lokalen Gruppe hinzu, um Ihnen Zugriff auf das Feature Berichte auf der MBAM-Verwaltungswebsite zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="00101-156">On the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="00101-157">**MBAM-Berichtsbenutzer**: Mitglieder dieser lokalen Gruppe können auf die Berichte auf der MBAM-Verwaltungswebsite zugreifen.</span><span class="sxs-lookup"><span data-stu-id="00101-157">**MBAM Report Users**: Members of this local group can access the Reports in the MBAM administration website.</span></span>

    **<span data-ttu-id="00101-158">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="00101-158">Note</span></span>**  
    <span data-ttu-id="00101-159">Die identische Benutzer-oder Gruppenmitgliedschaft der lokalen Gruppe **MBAM-Berichtsbenutzer** muss auf allen Computern verwaltet werden, auf denen die MBAM-Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie die Kompatibilitäts-und Überwachungsberichte installiert sind.</span><span class="sxs-lookup"><span data-stu-id="00101-159">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="00101-160">Überprüfen der MBAM Server-Feature-Installation</span><span class="sxs-lookup"><span data-stu-id="00101-160">Validate the MBAM Server feature installation</span></span>


<span data-ttu-id="00101-161">Wenn die MBAM-Server Feature-Installation abgeschlossen ist, sollten Sie überprüfen, ob die Installation alle erforderlichen Features für MBAM erfolgreich eingerichtet hat.</span><span class="sxs-lookup"><span data-stu-id="00101-161">When the MBAM Server feature installation is complete, you should validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="00101-162">Gehen Sie wie folgt vor, um zu überprüfen, ob der MBAM-Dienst funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="00101-162">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="00101-163">So überprüfen Sie eine MBAM-Installation</span><span class="sxs-lookup"><span data-stu-id="00101-163">To validate an MBAM installation</span></span>**

1. <span data-ttu-id="00101-164">Öffnen Sie auf jedem Server, auf dem ein MBAM-Feature bereitgestellt wird, die **System**Steuerung, klicken Sie auf **Programme**und dann auf **Programme und Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="00101-164">On each server, where an MBAM feature is deployed, open **Control Panel**, click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="00101-165">Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="00101-165">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="00101-166">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="00101-166">Note</span></span>**  
   <span data-ttu-id="00101-167">Um die MBAM-Installation zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.</span><span class="sxs-lookup"><span data-stu-id="00101-167">To validate the MBAM installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="00101-168">Öffnen Sie auf dem Server, auf dem die Wiederherstellungs-und Hardware Datenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und Hardware** Datenbank installiert ist.</span><span class="sxs-lookup"><span data-stu-id="00101-168">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="00101-169">Öffnen Sie auf dem Server, auf dem die Compliance-und Überwachungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitäts Status** Datenbank installiert ist.</span><span class="sxs-lookup"><span data-stu-id="00101-169">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status** database is installed.</span></span>

4. <span data-ttu-id="00101-170">Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte installiert sind, einen Webbrowser mit Administratorrechten, und navigieren Sie zu "Start" der SQL Server Reporting Services-Website.</span><span class="sxs-lookup"><span data-stu-id="00101-170">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="00101-171">Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz finden Sie unter http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="00101-171">The default Home location of a SQL Server Reporting Services site instance can be found at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="00101-172">Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die während des Setups angegebenen Instanzen aus.</span><span class="sxs-lookup"><span data-stu-id="00101-172">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="00101-173">Vergewissern Sie sich, dass ein Ordner mit dem Namen **Malta-Konformitätsberichte** aufgelistet ist und fünf Berichte und eine Datenquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="00101-173">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="00101-174">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="00101-174">Note</span></span>**  
   <span data-ttu-id="00101-175">Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="00101-175">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



5. <span data-ttu-id="00101-176">Führen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, den **Server-Manager** aus, navigieren Sie zu **Rollen**, wählen Sie **Webserver (IIS)** aus, und klicken Sie dann auf **Internet Informationsdienste (IIS)-Manager**.</span><span class="sxs-lookup"><span data-stu-id="00101-176">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span> <span data-ttu-id="00101-177">Navigieren Sie in **Verbindungen** zu \* &lt; Computer &gt; Name\*, klicken Sie auf **Websites**, und klicken Sie auf **Microsoft BitLocker-Verwaltung und-Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="00101-177">In **Connections** browse to *&lt;computername&gt;*, click **Sites**, and click **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="00101-178">Überprüfen Sie, ob **MBAMAdministrationService**, **MBAMComplianceStatusService**und **MBAMRecoveryAndHardwareService** aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="00101-178">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

6. <span data-ttu-id="00101-179">Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, einen Webbrowser mit Administratorrechten, und navigieren Sie zu den folgenden Speicherorten auf der MBAM-Website, um sicherzustellen, dass Sie erfolgreich geladen werden:</span><span class="sxs-lookup"><span data-stu-id="00101-179">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges and browse to the following locations in the MBAM web site, to verify that they load successfully:</span></span>

   -   <span data-ttu-id="00101-180">*http:// &lt; Computername &gt; /default.aspx* , und bestätigen Sie die einzelnen Links für Navigation und Berichte.</span><span class="sxs-lookup"><span data-stu-id="00101-180">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="00101-181">http:// &lt; Computername &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="00101-181">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="00101-182">http:// &lt; Computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="00101-182">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="00101-183">http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="00101-183">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="00101-184">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="00101-184">Note</span></span>**  
   <span data-ttu-id="00101-185">In der Regel werden Dienste auf dem Standard Port 80 ohne Netzwerk Verschlüsselung installiert.</span><span class="sxs-lookup"><span data-stu-id="00101-185">Typically, services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="00101-186">Wenn die Dienste an einem anderen Port installiert sind, ändern Sie die URLs so, dass Sie den entsprechenden Port umfassen.</span><span class="sxs-lookup"><span data-stu-id="00101-186">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="00101-187">Beispiel\* &lt; : http://Computername &gt; : &lt; Port &gt; \*/default.aspx oder http:// <em> &lt; Hostheadername &gt; / </em> default. aspx</span><span class="sxs-lookup"><span data-stu-id="00101-187">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx</span></span>

   <span data-ttu-id="00101-188">Wenn die Dienste mit Netzwerk Verschlüsselung installiert wurden, ändern Sie http://in https://.</span><span class="sxs-lookup"><span data-stu-id="00101-188">If the services were installed with network encryption, change http:// to https://.</span></span>



~~~
Verify that each web page loads successfully.
~~~

## <span data-ttu-id="00101-189">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="00101-189">Related topics</span></span>


[<span data-ttu-id="00101-190">Bereitstellen der Serverinfrastruktur von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="00101-190">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)









