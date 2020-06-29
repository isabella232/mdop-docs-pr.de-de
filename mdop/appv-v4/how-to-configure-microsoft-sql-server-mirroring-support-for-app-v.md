---
title: So konfigurieren Sie die Unterstützung von Microsoft SQL Server-Spiegelungen für App-V
description: So konfigurieren Sie die Unterstützung von Microsoft SQL Server-Spiegelungen für App-V
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807304"
---
# <span data-ttu-id="32494-103">So konfigurieren Sie die Unterstützung von Microsoft SQL Server-Spiegelungen für App-V</span><span class="sxs-lookup"><span data-stu-id="32494-103">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>


<span data-ttu-id="32494-104">Mit dem folgenden Verfahren können Sie Ihre Microsoft Application Virtualization-Umgebung (App-V) für die Verwendung der Microsoft SQL Server-Datenbankspiegelung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="32494-104">You can use the following procedure to configure your Microsoft Application Virtualization (App-V) environment to use Microsoft SQL Server database mirroring.</span></span> <span data-ttu-id="32494-105">Das Konfigurieren der Datenbankspiegelung kann bei Disaster Recovery-und Failover-Szenarien helfen.</span><span class="sxs-lookup"><span data-stu-id="32494-105">Configuring database mirroring can help with disaster recovery and failover scenarios.</span></span> <span data-ttu-id="32494-106">App-V 4,5 SP2 unterstützt alle Modi der Datenbankspiegelung, die derzeit für Microsoft SQL Server 2005 und SQL Server 2008 verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="32494-106">App-V 4.5 SP2 supports all modes of database mirroring currently available for Microsoft SQL Server 2005 and SQL Server 2008.</span></span>

**<span data-ttu-id="32494-107">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="32494-107">Note</span></span>**  
<span data-ttu-id="32494-108">Dieses Verfahren wurde für Administratoren geschrieben, die mit dem Einrichten und Konfigurieren von SQL Server-Datenbanken und der Datenbankspiegelung mit Microsoft SQL Server vertraut sind, und umfasst daher nur die spezifischen Konfigurationseinstellungen, die für App-V eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="32494-108">This procedure is written for administrators who are familiar with setting up and configuring SQL Server databases and database mirroring with Microsoft SQL Server, and therefore covers only the specific configuration settings that are unique to App-V.</span></span>



**<span data-ttu-id="32494-109">So konfigurieren Sie Ihre App-V-Umgebung für die Verwendung der Microsoft SQL Server-Datenbankspiegelung</span><span class="sxs-lookup"><span data-stu-id="32494-109">To configure your App-V environment to use Microsoft SQL Server database mirroring</span></span>**

1.  <span data-ttu-id="32494-110">Richten Sie die SQL Server-Datenbankspiegelung der App-V-Datenbank nach Ihren Standard Geschäftsmethoden für die Datenbankspiegelung ein.</span><span class="sxs-lookup"><span data-stu-id="32494-110">Set up SQL Server database mirroring of the App-V database following your standard business practices for database mirroring.</span></span> <span data-ttu-id="32494-111">Verwenden Sie die folgenden Links, um allgemeine Informationen zum Implementieren der Microsoft SQL Server-Datenbankspiegelung zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="32494-111">Use the following links for general information about implementing Microsoft SQL Server database mirroring:</span></span>

    -   <span data-ttu-id="32494-112">**Microsoft SQL 2005**–[Einrichten der Datenbankspiegelung](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span><span class="sxs-lookup"><span data-stu-id="32494-112">**Microsoft SQL 2005**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span></span>

    -   <span data-ttu-id="32494-113">**Microsoft SQL 2008**–[Einrichten der Datenbankspiegelung](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span><span class="sxs-lookup"><span data-stu-id="32494-113">**Microsoft SQL 2008**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span></span>

    <span data-ttu-id="32494-114">Darüber hinaus finden Sie Informationen zu bewährten Methoden unter [bewährte Methoden für die Datenbankspiegelung und Leistungsüberlegungen](https://go.microsoft.com/fwlink/?LinkId=190270) ( https://go.microsoft.com/fwlink/?LinkId=190270) .</span><span class="sxs-lookup"><span data-stu-id="32494-114">In addition, you can find Best Practices information in [Database Mirroring Best Practices and Performance Considerations](https://go.microsoft.com/fwlink/?LinkId=190270) (https://go.microsoft.com/fwlink/?LinkId=190270).</span></span>

2.  <span data-ttu-id="32494-115">Überprüfen Sie nach der Einrichtung der Spiegelung, ob die App-V-Datenbank den Status **(Prinzipal, synchronisiert)** aufweist, und die gespiegelte Datenbank zeigt den Status **(gespiegelt, synchronisiert/wiederherstellen)**.</span><span class="sxs-lookup"><span data-stu-id="32494-115">After mirroring has been set up, verify that the App-V database shows a status of **(Principal, Synchronized)**, and the mirrored database shows a status of **(Mirror, Synchronized / Restoring)**.</span></span> <span data-ttu-id="32494-116">Beheben Sie alle Spiegelungs Probleme, bevor Sie mit dem nächsten Schritt fortfahren.</span><span class="sxs-lookup"><span data-stu-id="32494-116">Resolve any mirroring issues before proceeding to the next step.</span></span> <span data-ttu-id="32494-117">Weitere Informationen zum Überwachen des Status finden Sie unter über [Wachen des Spiegelungsstatus](https://go.microsoft.com/fwlink/?LinkId=190279) ( https://go.microsoft.com/fwlink/?LinkId=190279) .</span><span class="sxs-lookup"><span data-stu-id="32494-117">For additional information about monitoring the status, see [Monitoring Mirroring Status](https://go.microsoft.com/fwlink/?LinkId=190279) (https://go.microsoft.com/fwlink/?LinkId=190279).</span></span>

3.  <span data-ttu-id="32494-118">Erstellen Sie auf dem SQL Server-Computer, der die Spiegelung der APP-v-Datenbank hostet, die SQL Server-Anmeldung für das Netzwerkdienstkonto des App-v-Verwaltungsservers unter Verwendung des \*\* &lt; Domänen &gt; \\ &lt; ManagementServerHostName &gt; $ \*\*des Kontonamens.</span><span class="sxs-lookup"><span data-stu-id="32494-118">On the SQL Server computer that hosts the mirror of the App-V database, create the SQL Server Login for the network service account of the App-V Management Server by using the account name **&lt;domain&gt;\\&lt;ManagementServerHostName&gt;$**.</span></span>

4.  <span data-ttu-id="32494-119">Installieren Sie den Microsoft SQL Server Native Client auf dem App-v-Verwaltungs Server und auf dem Computer mit dem App-v-Verwaltungs-Webdienst, wenn Sie auf einem anderen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="32494-119">Install the Microsoft SQL Server Native Client on the App-V Management Server, and on the computer running the App-V Management Web Service if installed on a different computer.</span></span> <span data-ttu-id="32494-120">Wenn Sie beabsichtigen, zusätzliche App-V-Verwaltungsserver zum Lastenausgleich mit der gespiegelten SQL-Datenbank zu verbinden, müssen Sie auch den Microsoft SQL Server Native Client auf diesen Computern installieren.</span><span class="sxs-lookup"><span data-stu-id="32494-120">If you plan to have additional App-V Management Servers connect to the mirrored SQL database for load balancing, you must install the Microsoft SQL Server Native Client on those computers as well.</span></span> <span data-ttu-id="32494-121">Sie können den Microsoft SQL Server Native Client von der [Microsoft SQL Server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) -Seite im Microsoft Download Center herunterladen ( https://go.microsoft.com/fwlink/?LinkId=187479) .</span><span class="sxs-lookup"><span data-stu-id="32494-121">You can download the Microsoft SQL Server Native Client from the [Microsoft SQL Server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) page in the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=187479).</span></span>

5.  <span data-ttu-id="32494-122">Überprüfen Sie den Registrierungsschlüssel **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** , und stellen Sie sicher, dass er nur den Hostnamen des SQL-Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="32494-122">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerName** and make sure that it contains only the host name of the SQL Server.</span></span> <span data-ttu-id="32494-123">Wenn Sie einen Instanznamen enthält, beispielsweise *serverhostname\\instancename*, muss der Instanzname entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="32494-123">If it includes an instance name, for example *serverhostname\\instancename*, the instance name must be removed.</span></span>

    **<span data-ttu-id="32494-124">Wichtig</span><span class="sxs-lookup"><span data-stu-id="32494-124">Important</span></span>**  
    <span data-ttu-id="32494-125">Der App-V-Verwaltungs Server verwendet die TCP/IP-Netzwerkbibliothek, um mit dem SQL Server zu kommunizieren, wenn die Datenbankspiegelung aktiviert ist, und daher können keine Instanznamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32494-125">The App-V Management Server uses the TCP/IP networking library to communicate with the SQL Server when database mirroring is enabled, and therefore instance names cannot be used.</span></span> <span data-ttu-id="32494-126">Die Portnummern müssen stattdessen in den Registrierungsschlüsseln angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="32494-126">The port numbers must be specified in the registry keys instead.</span></span>



6.  <span data-ttu-id="32494-127">Überprüfen Sie den Registrierungsschlüssel **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** , und stellen Sie sicher, dass er die Portnummer enthält, die für SQL auf dem SQL Server-Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="32494-127">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerPort** and make sure that it contains the port number that is used for SQL on the SQL Server computer.</span></span> <span data-ttu-id="32494-128">Wenn Sie eine benannte Instanz verwenden, muss dieser Schlüsselwert auf den Port festgesetzt werden, der für die benannte Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="32494-128">If you are using a named instance this key value must be set to the port that is used for the named instance.</span></span>

7.  <span data-ttu-id="32494-129">Erstellen Sie den Registrierungsschlüssel **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverservername** als reg \ _SZ, und legen Sie dann den Wert auf den Hostnamen des SQL-Servers fest, der die Spiegelung hostet.</span><span class="sxs-lookup"><span data-stu-id="32494-129">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerName** as REG\_SZ and then set the value to the host name of the SQL Server that hosts the mirror.</span></span>

8.  <span data-ttu-id="32494-130">Erstellen Sie den Registrierungsschlüssel **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverserverport** als DWORD, und legen Sie dann den Wert auf die Portnummer fest, die für SQL auf dem Computer verwendet wird, auf dem SQL Server ausgeführt wird, um die Spiegelung zu hosten.</span><span class="sxs-lookup"><span data-stu-id="32494-130">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerPort** as DWORD and then set the value to the port number that is used for SQL on the computer that is running SQL Server to host the mirror.</span></span> <span data-ttu-id="32494-131">Wenn Sie eine benannte Instanz für die Spiegelung verwenden, muss dieser Schlüsselwert auf die Portnummer festgesetzt werden, die für die benannte Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="32494-131">If you are using a named instance for the mirror this key value must be set to the port number that is used for the named instance.</span></span>

9.  <span data-ttu-id="32494-132">Konfigurieren Sie auf dem Computer, auf dem der App-V Management Web Service ausgeführt wird, die UDL-Textdatei (Universal Data Link).</span><span class="sxs-lookup"><span data-stu-id="32494-132">On the computer that is running the App-V Management Web Service, configure the Universal Data Link (UDL) text file.</span></span> <span data-ttu-id="32494-133">Doppelklicken Sie in dem Verzeichnis, in dem App-V installiert ist, auf **SftMgmt. udl** , und geben Sie die folgenden Werte an:</span><span class="sxs-lookup"><span data-stu-id="32494-133">In the directory where App-V is installed, double-click **SftMgmt.udl** and specify the following values:</span></span>

    -   <span data-ttu-id="32494-134">Wählen Sie auf der Registerkarte **Anbieter** den OLE DB-Anbieter **SQL Server Native Client 10,0**aus.</span><span class="sxs-lookup"><span data-stu-id="32494-134">On the **Provider** tab, select the OLE DB provider **SQL Server Native Client 10.0**.</span></span>

    -   <span data-ttu-id="32494-135">Klicken Sie auf **weiter** , um die Registerkarte **Verbindung** auszuwählen. Geben Sie im Feld **Servername** den Servernamen des SQL-Servers ein.</span><span class="sxs-lookup"><span data-stu-id="32494-135">Click **Next** to select the **Connection** tab. In the **Server Name** box, enter the server name of the SQL Server.</span></span> <span data-ttu-id="32494-136">Wählen Sie als nächstes **Windows NT Integrated Security verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="32494-136">Next, select **Use Windows NT Integrated Security**.</span></span> <span data-ttu-id="32494-137">Klicken Sie abschließend auf die Liste **Wählen Sie die Datenbank aus**, und wählen Sie dann den Namen der App-V-Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="32494-137">Finally, click the list **Select the database**, and then select the App-V database name.</span></span>

    -   <span data-ttu-id="32494-138">Klicken Sie auf die Registerkarte **alle** , und wählen Sie dann den Eintrag **Failover-Partner**aus.</span><span class="sxs-lookup"><span data-stu-id="32494-138">Click the **All** tab, and then select the entry **Failover Partner**.</span></span> <span data-ttu-id="32494-139">Klicken Sie auf **Wert bearbeiten**, und geben Sie dann den Servernamen des SQL Server-Failovers ein.</span><span class="sxs-lookup"><span data-stu-id="32494-139">Click **Edit Value**, and then enter the server name of the failover SQL Server.</span></span> <span data-ttu-id="32494-140">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="32494-140">Click **OK**.</span></span>

    **<span data-ttu-id="32494-141">Wichtig</span><span class="sxs-lookup"><span data-stu-id="32494-141">Important</span></span>**  
    <span data-ttu-id="32494-142">Das App-V-System verwendet die Kerberos-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="32494-142">The App-V system uses Kerberos authentication.</span></span> <span data-ttu-id="32494-143">Wenn Sie die SQL-Spiegelung so konfigurieren, dass die Kerberos-Authentifizierung auf dem SQL Server aktiviert ist und der SQL Server-Dienst unter einem Domänenbenutzerkonto ausgeführt wird, müssen Sie einen SPN manuell konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="32494-143">Therefore, when you configure SQL mirroring where Kerberos Authentication is enabled on the SQL Server and the SQL Server service runs under a domain user account, you must manually configure an SPN.</span></span> <span data-ttu-id="32494-144">Weitere Informationen finden Sie unter "Wenn der SQL-Dienstdomänen basiertes Konto verwendet" im Artikel [Konfigurieren der App-V-Verwaltung für eine verteilte Umgebung](https://go.microsoft.com/fwlink/?LinkId=203186) ( https://go.microsoft.com/fwlink/?LinkId=203186) .</span><span class="sxs-lookup"><span data-stu-id="32494-144">For more information, see “When SQL Service Uses Domain-Based Account” in the article [Configuring App-V Administration for a Distributed Environment](https://go.microsoft.com/fwlink/?LinkId=203186) (https://go.microsoft.com/fwlink/?LinkId=203186).</span></span>



10. <span data-ttu-id="32494-145">Um zu überprüfen, ob die Datenbankspiegelung ordnungsgemäß ausgeführt wird, testen Sie das Failover, und vergewissern Sie sich, dass der App-V-Verwaltungs Server weiterhin ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="32494-145">To verify that database mirroring is running correctly, test the failover and confirm that the App-V Management Server continues to function correctly.</span></span>

    **<span data-ttu-id="32494-146">Wichtig</span><span class="sxs-lookup"><span data-stu-id="32494-146">Important</span></span>**  
    <span data-ttu-id="32494-147">Gehen Sie mit Bedacht vor, und befolgen Sie Ihre standardmäßigen Geschäftsmethoden, um sicherzustellen, dass die Systemvorgänge bei einem Fehler nicht gestört werden.</span><span class="sxs-lookup"><span data-stu-id="32494-147">Proceed with care, and follow your standard business practices to ensure that system operations are not disrupted in the event of a failure.</span></span>



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## <span data-ttu-id="32494-148">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="32494-148">Related topics</span></span>


[<span data-ttu-id="32494-149">So führen Sie Verwaltungsaufgaben in der Application Virtualization Server Management Console durch</span><span class="sxs-lookup"><span data-stu-id="32494-149">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









