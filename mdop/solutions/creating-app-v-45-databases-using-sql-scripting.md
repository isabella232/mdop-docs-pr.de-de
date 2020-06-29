---
title: Erstellen von App-V 4.5-Datenbanken mithilfe von SQL-Skripts
description: Erstellen von App-V 4.5-Datenbanken mithilfe von SQL-Skripts
author: dansimp
ms.assetid: 6cd0b180-163e-463f-a658-939ab9a7cfa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ab2c102a43701bfdeaac49359b4ca3c4a063fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811479"
---
# <span data-ttu-id="4ac4d-103">Erstellen von App-V 4.5-Datenbanken mithilfe von SQL-Skripts</span><span class="sxs-lookup"><span data-stu-id="4ac4d-103">Creating App-V 4.5 Databases Using SQL Scripting</span></span>


**<span data-ttu-id="4ac4d-104">Für wen ist diese Lösung vorgesehen?</span><span class="sxs-lookup"><span data-stu-id="4ac4d-104">Who is this solution intended for?</span></span>** <span data-ttu-id="4ac4d-105">IT-Experten, die Application Virtualization (App-V) 4,5-Datenbanken verwalten.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-105">Information technology professionals who manage Application Virtualization (App-V) 4.5 databases.</span></span>

**<span data-ttu-id="4ac4d-106">Wie kann Ihnen dieser Leitfaden helfen?</span><span class="sxs-lookup"><span data-stu-id="4ac4d-106">How can this guide help you?</span></span>** <span data-ttu-id="4ac4d-107">Diese Lösung erläutert und dokumentiert das Verfahren zum Installieren des Microsoft Application Virtualization-Servers, wenn die Installation des Administrators nicht über "sysadmin"-Berechtigungen für SQL Server verfügt.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-107">This solution explains and documents the procedure to install the Microsoft Application Virtualization Server when the administrator installing does not have “sysadmin” privileges to the SQL Server.</span></span>

## <span data-ttu-id="4ac4d-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4ac4d-108">Overview</span></span>


<span data-ttu-id="4ac4d-109">Eine der Herausforderungen bei der Installation von Microsoft Application Virtualization 4,5 (App-V) besteht darin, dass das Installationsprogramm davon ausgeht, dass der Benutzer, der die Server Features installiert, nicht nur ein lokaler Computeradministrator ist, sondern auch über SQL-Administratorrechte auf dem SQL Server verfügt, der den Datenspeicher hosten wird.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-109">One of the challenges of installing Microsoft Application Virtualization 4.5 (App-V) is that the install program assumes that the user installing the server features will not only be a local computer administrator, but also have SQL administrator privileges on the SQL server that will host the Data Store.</span></span> <span data-ttu-id="4ac4d-110">Diese Anforderung basiert auf der Tatsache, dass die Datenbank sowie die entsprechenden Rollen und Berechtigungen als Teil der Installation erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-110">This requirement is based on the fact that the database, as well as the appropriate roles and permissions, are created as part of the install.</span></span> <span data-ttu-id="4ac4d-111">In den meisten Unternehmen werden SQL-Server jedoch separat vom Infrastrukturteam verwaltet, das App-V installieren wird.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-111">However, in most enterprises, SQL servers are managed separately from the infrastructure team who will be installing App-V.</span></span> <span data-ttu-id="4ac4d-112">Durch diese Sicherheitsanforderungen wird es schwierig, SQL-Administratoren zu veranlassen, dem Infrastrukturadministrator zu ermöglichen, App-V adäquate Rechte zu installieren. Ebenso verfügen die SQL-Administratoren nicht über die erforderlichen Berechtigungen zum Installieren des Produkts für das Infrastrukturteam.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-112">These security requirements will make it difficult to get SQL administrators to give the infrastructure administrator installing App-V adequate rights; similarly, the SQL administrators will not have the required privileges to install the product for the infrastructure team.</span></span>

<span data-ttu-id="4ac4d-113">Zurzeit muss ein Administrator, der die Installation von App-V versucht, über SQL-"sysadmin"-Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-113">Currently, an administrator attempting the installation of App-V must have SQL “sysadmin” privileges.</span></span> <span data-ttu-id="4ac4d-114">In früheren Versionen des Produkts durften die SQL-Administratoren entweder ein temporäres "sysadmin"-Konto erstellen oder während der Installation anwesend sein, um Anmeldeinformationen mit "sysadmin"-Privilegien bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-114">In previous versions of the product the setup allowed for the SQL administrators to either create a temporary “sysadmin” account or be present during installation to provide credentials with “sysadmin” privileges.</span></span> <span data-ttu-id="4ac4d-115">In dieser Version werden Skripts im veröffentlichten Produkt bereitgestellt, damit alle Administratoren ihre Infrastruktur implementieren können.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-115">In this release, scripts are provided in the released product for all administrators to use when implementing their infrastructure.</span></span>

<span data-ttu-id="4ac4d-116">In diesem Whitepaper wird das Szenario erläutert, in dem die Installation in zwei getrennte Aufgaben aufgeteilt werden muss: Erstellen der SQL-Datenbank und Installieren der App-V-Server Features.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-116">This whitepaper discusses the scenario in which the install will need to be divided into two separate tasks: creating the SQL database, and installing the App-V server features.</span></span> <span data-ttu-id="4ac4d-117">Die SQL-Administratoren können die SQL-Skripts überprüfen und Änderungen vornehmen, um Konflikte mit anderen Datenbanken zu beheben oder die Integration mit anderen Tools zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-117">The SQL administrators would be able to review the SQL scripts and make modifications to resolve any conflicts with other databases, or to support integration with other tools.</span></span> <span data-ttu-id="4ac4d-118">Das Ergebnis der Skripts besteht darin, dass SQL-Administratoren die Datenbank vorbereiten können, damit den Infrastrukturadministratoren keine erweiterten Rechte auf dem SQL Server gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-118">The result of the scripts is to allow SQL administrators to prepare the database so that the infrastructure administrators do not have to be granted any advanced rights on the SQL server.</span></span> <span data-ttu-id="4ac4d-119">Dies ist in Umgebungen wichtig, in denen dies durch Sicherheitsrichtlinien untersagt ist.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-119">This is important in environments where security policies would prohibit this.</span></span>

### <span data-ttu-id="4ac4d-120">Erstellungsprozess für SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="4ac4d-120">SQL Database Creation Process</span></span>

<span data-ttu-id="4ac4d-121">Die SQL-Skripts ermöglichen es SQL-Administratoren, die erforderliche Datenbank zu erstellen und auch die Privilegien für die App-V-Administratoren einzurichten, um die Umgebung erfolgreich zu installieren und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-121">The SQL scripts allow for SQL administrators to create the required database and also set up the privileges for the App-V administrators to successfully install and manage the environment.</span></span> <span data-ttu-id="4ac4d-122">Die Schritte zum Abschließen dieser Aufgaben sind weiter unten in diesem Dokument aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-122">The steps for completing these tasks are listed later in this document.</span></span>

<span data-ttu-id="4ac4d-123">Durch diesen Vorgang werden die Daten Banker stellungs-und Konfigurationsaktionen von der eigentlichen App-V-Installation getrennt.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-123">This process separates the database creation and configuration actions from the actual App-V installation.</span></span>

**<span data-ttu-id="4ac4d-124">Informationen, die SQL-Administratoren bereitgestellt werden sollen</span><span class="sxs-lookup"><span data-stu-id="4ac4d-124">Information to be provided to SQL administrators</span></span>**

-   <span data-ttu-id="4ac4d-125">Der Name der Anzeigengruppe, die die App-V-Administratoren sein wird</span><span class="sxs-lookup"><span data-stu-id="4ac4d-125">Name of AD group that is going to be the App-V admin’s</span></span>

-   <span data-ttu-id="4ac4d-126">Name des Servers, auf dem App-V Management Server installiert wird</span><span class="sxs-lookup"><span data-stu-id="4ac4d-126">Name of the server where App-V Management Server will be installed</span></span>

**<span data-ttu-id="4ac4d-127">Informationen, die an die Infrastrukturadministratoren zurückgegeben werden sollen</span><span class="sxs-lookup"><span data-stu-id="4ac4d-127">Information to be returned to the Infrastructure administrators</span></span>**

-   <span data-ttu-id="4ac4d-128">Name des Datenbankservers oder der Instanz und der Name der App-V-Datenbank</span><span class="sxs-lookup"><span data-stu-id="4ac4d-128">Name of the database server or instance and the name of the App-V database</span></span>

<span data-ttu-id="4ac4d-129">Nachdem die Datenbank vorbereitet wurde, können die APP-v-Administratoren die APP-v-Installation ohne SQL-Administratorrechte ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-129">Once the database has been prepared, the App-V administrators can run the App-V installation without SQL administrator privileges.</span></span>

### <span data-ttu-id="4ac4d-130">Verwenden der SQL-Setup Skripts</span><span class="sxs-lookup"><span data-stu-id="4ac4d-130">Using the SQL Setup Scripts</span></span>

**<span data-ttu-id="4ac4d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ac4d-131">Requirements</span></span>**

<span data-ttu-id="4ac4d-132">Im folgenden finden Sie eine Liste der Anforderungen für die Verwendung der Skripts, die sich im Ordner support\\createdb im Stammverzeichnis des ausgewählten Extraktions Speicherorts befinden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-132">The following is a list of requirements for using the scripts which are located in the support\\createdb folder at the root of the selected extract location.</span></span>

-   <span data-ttu-id="4ac4d-133">Skripts müssen an einen beschreibbaren Speicherort auf dem Computer kopiert werden, auf dem Sie ausgeführt werden (achten Sie darauf, das Attribut "schreibgeschützt" aus diesen Skripts zu entfernen, nachdem Sie kopiert wurden), und die SQL-Clienttools müssen auf diesem Computer geladen werden (osql ist nur für die Ausführung der Beispielbatchdateien auf dem lokalen Computer erforderlich).</span><span class="sxs-lookup"><span data-stu-id="4ac4d-133">Scripts must be copied to a writeable location on the computer where they will be run (be sure to remove the read only attribute from these scripts after they have been copied) and SQL client tools must be loaded on that computer (osql is only required for running the sample batch files on the local computer).</span></span>

-   <span data-ttu-id="4ac4d-134">SQL Server muss die Windows-Authentifizierung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-134">The SQL Server must support Windows Authentication.</span></span>

-   <span data-ttu-id="4ac4d-135">Stellen Sie sicher, dass die SQL Server-Instanz und der SQL-Agent-Dienst ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-135">Ensure that the SQL Server Instance and SQL Agent Service are running.</span></span>

-   <span data-ttu-id="4ac4d-136">Melden Sie sich mit einem Domänenkonto an, bei dem es sich um einen SQL-Administrator (sysadmin) auf dem Computer handelt, auf dem die Skripts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-136">Log on with a domain account that is a SQL administrator (sysadmin) on the computer where the scripts will be done.</span></span>

<span data-ttu-id="4ac4d-137">Die Skripts werden unter den Domänenanmeldeinformationen des angemeldeten Benutzers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-137">The scripts runs under the logged-on user’s domain credentials.</span></span>

**<span data-ttu-id="4ac4d-138">Erstellen von Datenbanken mit SQL-Skripts</span><span class="sxs-lookup"><span data-stu-id="4ac4d-138">Database Creation Using SQL Scripts</span></span>**

**<span data-ttu-id="4ac4d-139">Aufgaben, die von SQL-Administratoren ausgeführt werden sollen:</span><span class="sxs-lookup"><span data-stu-id="4ac4d-139">Tasks to be performed by SQL administrators:</span></span>**

1.  <span data-ttu-id="4ac4d-140">Kopieren Sie die im support\\createdb-Ordner enthaltenen Skripts aus dem Stammverzeichnis des ausgewählten Extrahierungs Speicherorts auf den Computer, auf dem die Skripts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-140">Copy the scripts contained in the support\\createdb folder from the root of the selected extract location to the computer where the scripts will be run.</span></span> <span data-ttu-id="4ac4d-141">Die folgenden Dateien sind für die ordnungsgemäße Ausführung der Skripts erforderlich und müssen in der unten aufgeführten Reihenfolge aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-141">The following files are required for the scripts to run properly and must be called in the order presented below.</span></span>

    -   <span data-ttu-id="4ac4d-142">Database. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-142">database.sql</span></span>

    -   <span data-ttu-id="4ac4d-143">Roles. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-143">roles.sql</span></span>

    -   <span data-ttu-id="4ac4d-144">Tabelle \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-144">table\_CODES.sql</span></span>

    -   <span data-ttu-id="4ac4d-145">Funktionen \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-145">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="4ac4d-146">Tables. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-146">tables.sql</span></span>

    -   <span data-ttu-id="4ac4d-147">Functions. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-147">functions.sql</span></span>

    -   <span data-ttu-id="4ac4d-148">views. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-148">views.sql</span></span>

    -   <span data-ttu-id="4ac4d-149">Procedures. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-149">procedures.sql</span></span>

    -   <span data-ttu-id="4ac4d-150">Triggers. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-150">triggers.sql</span></span>

    -   <span data-ttu-id="4ac4d-151">Data \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-151">data\_codes.sql</span></span>

    -   <span data-ttu-id="4ac4d-152">Data \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-152">data\_messages.sql</span></span>

    -   <span data-ttu-id="4ac4d-153">Data \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-153">data\_defaults.sql</span></span>

    -   <span data-ttu-id="4ac4d-154">Alerts \ _Jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-154">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="4ac4d-155">dbversion. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-155">dbversion.sql</span></span>

2.  <span data-ttu-id="4ac4d-156">Überprüfen und ändern Sie bei Bedarf die `database.sql` Datei.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-156">Review and modify, if necessary, the `database.sql` file.</span></span> <span data-ttu-id="4ac4d-157">Die Standardeinstellungen geben der Datenbank den Namen "APPVIRTDB".</span><span class="sxs-lookup"><span data-stu-id="4ac4d-157">The default settings will name the database “APPVIRTDB.”</span></span>

    -   <span data-ttu-id="4ac4d-158">Ersetzen Sie bei Bedarf Instanzen von `APPVIRTDB` mit dem `database name` , die verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-158">If necessary replace instances of `APPVIRTDB` with the `database name` that will be used.</span></span>

    -   <span data-ttu-id="4ac4d-159">Ändern Sie die `FILENAME` Eigenschaft im Skript mit dem entsprechenden Pfad für den SQL-Server, auf dem die Datenbank erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-159">Modify the `FILENAME` property in the script with the appropriate path for the SQL Server where the database will be created.</span></span>

3.  <span data-ttu-id="4ac4d-160">Überprüfen und ändern Sie bei Bedarf die `database name [APPVIRTDB]` in der `roles.sql` Datei, die in der Datenbank. SQL-Datei verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-160">Review and modify, if necessary, the `database name [APPVIRTDB]` in the `roles.sql` file that was used in the database.sql file.</span></span>

****

### <span data-ttu-id="4ac4d-161">Beispiel für die Automatisierung des Prozesses mithilfe von Batchdateien</span><span class="sxs-lookup"><span data-stu-id="4ac4d-161">Example of how to automate the process using batch files</span></span>

<span data-ttu-id="4ac4d-162">Wenn die beiden Beispielbatchdateien verwendet werden, führen Sie die SQL-Skripts wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="4ac4d-162">If used, the two sample batch files provided run the SQL scripts in the following manner:</span></span>

1.  **<span data-ttu-id="4ac4d-163">Create\_schema.bat (1)</span><span class="sxs-lookup"><span data-stu-id="4ac4d-163">Create\_schema.bat (1)</span></span>**

    -   <span data-ttu-id="4ac4d-164">Database. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-164">database.sql</span></span>

    -   <span data-ttu-id="4ac4d-165">Roles. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-165">roles.sql</span></span>

2.  **<span data-ttu-id="4ac4d-166">Create\_tables.bat (2)</span><span class="sxs-lookup"><span data-stu-id="4ac4d-166">Create\_tables.bat (2)</span></span>**

    -   <span data-ttu-id="4ac4d-167">Tabelle \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-167">table\_CODES.sql</span></span>

    -   <span data-ttu-id="4ac4d-168">Funktionen \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-168">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="4ac4d-169">Tables. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-169">tables.sql</span></span>

    -   <span data-ttu-id="4ac4d-170">Functions. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-170">functions.sql</span></span>

    -   <span data-ttu-id="4ac4d-171">views. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-171">views.sql</span></span>

    -   <span data-ttu-id="4ac4d-172">Procedures. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-172">procedures.sql</span></span>

    -   <span data-ttu-id="4ac4d-173">Triggers. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-173">triggers.sql</span></span>

    -   <span data-ttu-id="4ac4d-174">Data \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-174">data\_codes.sql</span></span>

    -   <span data-ttu-id="4ac4d-175">Data \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-175">data\_messages.sql</span></span>

    -   <span data-ttu-id="4ac4d-176">Data \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-176">data\_defaults.sql</span></span>

    -   <span data-ttu-id="4ac4d-177">Alerts \ _Jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-177">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="4ac4d-178">dbversion. SQL</span><span class="sxs-lookup"><span data-stu-id="4ac4d-178">dbversion.sql</span></span>

**<span data-ttu-id="4ac4d-179">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4ac4d-179">Note</span></span>**  
<span data-ttu-id="4ac4d-180">Sorgfältige Überlegungen beim Ändern der Skripts müssen getroffen werden und sollten nur von einer Person mit dem entsprechenden wissen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-180">Careful consideration when modifying the scripts must be taken and should only be done by someone with the appropriate knowledge.</span></span> <span data-ttu-id="4ac4d-181">Darüber hinaus sollten nur die folgenden Beispieldateien geändert werden: **create\_schema.bat**, **create\_tables.bat**, **Database. SQL**und **Roles. SQL**.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-181">Also, of the sample files presented only the following should be changed: **create\_schema.bat**, **create\_tables.bat**, **database.sql**, and **roles.sql**.</span></span> <span data-ttu-id="4ac4d-182">Alle anderen Dateien sollten in keiner Weise geändert werden, da dies dazu führen kann, dass die Datenbank falsch erstellt wird, was dazu führt, dass App-V-Dienste nicht installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-182">All other files should not be modified in any way as this could cause the database to be created incorrectly, which will lead to the failure of App-V services to be installed.</span></span>



<span data-ttu-id="4ac4d-183">Die beiden Beispielbatchdateien müssen sich im gleichen Verzeichnis befinden, in dem die restlichen SQL-Skripts auf den Computer kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-183">The two sample batch files must be placed in the same directory where the rest of the SQL scripts were copied to on the computer.</span></span>

1.  <span data-ttu-id="4ac4d-184">Führen Sie die Beispiel **create\_schema.bat** -Datei aus, um die Datenbank zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-184">Run the sample **create\_schema.bat** file to create the database.</span></span> <span data-ttu-id="4ac4d-185">Dieses Skript wird einige Sekunden dauern, bis es beendet wird und nicht unterbrochen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-185">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="4ac4d-186">Führen Sie die Create schema.bat-Datei aus dem Verzeichnis aus, in das Sie kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-186">Run the create schema.bat file from the directory where it was copied to.</span></span> <span data-ttu-id="4ac4d-187">Syntax lautet: "Create\_schema.bat `SQLSERVERNAME` "</span><span class="sxs-lookup"><span data-stu-id="4ac4d-187">Syntax is: “Create\_schema.bat `SQLSERVERNAME`”</span></span>

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   <span data-ttu-id="4ac4d-189">Wenn dieses Skript während der Erstellung der neuen "APPVIRTDB"-Datenbank fehlschlägt, überprüfen Sie das Protokoll wie angegeben, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-189">If this script fails during the creation of the new “APPVIRTDB” database, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="4ac4d-190">Es ist notwendig, die Datenbank zu löschen, die mit einer partiellen Ausführung der Skripts erstellt wurde, um sicherzustellen, dass nachfolgende Versuche ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-190">It will be necessary to delete the database that was created with a partial running of the scripts in order to ensure that subsequent attempts will work properly.</span></span>

2.  <span data-ttu-id="4ac4d-191">Führen `create_tables.bat` Sie die Datei aus, um die Tabellen in der Datenbank zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-191">Run the `create_tables.bat` file to create the tables in the database.</span></span> <span data-ttu-id="4ac4d-192">Dieses Skript wird einige Sekunden dauern, bis es beendet wird und nicht unterbrochen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-192">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="4ac4d-193">Führen Sie die create\_tables.bat-Datei aus dem Verzeichnis aus, in dem Sie kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-193">Run the create\_tables.bat file from the directory where it was copied.</span></span> <span data-ttu-id="4ac4d-194">Syntax lautet: "create\_tables.bat `SQLSERVERNAME DBNAME` "</span><span class="sxs-lookup"><span data-stu-id="4ac4d-194">Syntax is: “create\_tables.bat `SQLSERVERNAME DBNAME`”</span></span>

        ![App-v 4,6 SQL create\-table.bat](images/appv46sqlcreate-tablebat.gif)

        <span data-ttu-id="4ac4d-196">Wenn das Skript während der Erstellung der Tabellen fehlschlägt, überprüfen Sie das Protokoll wie angegeben, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-196">If the script fails during the creation of the tables, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="4ac4d-197">Es ist notwendig, die Datenbank zu löschen und create\_schema.bat auszuführen, bevor Sie versuchen, die create\_tables.bat-Datei bei allen nachfolgenden versuchen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-197">It will be necessary to delete the database and run create\_schema.bat before attempting to run the create\_tables.bat file on all subsequent attempts.</span></span>

### <span data-ttu-id="4ac4d-198">Festlegen von Berechtigungen für die App-V-Datenbank</span><span class="sxs-lookup"><span data-stu-id="4ac4d-198">Setting permissions on the App-V database</span></span>

<span data-ttu-id="4ac4d-199">Die folgenden Konten müssen auf dem SQL Server mit bestimmten Berechtigungen und Rollen für die neue Datenbank für die Installation, Bereitstellung und laufende Verwaltung der App-V-Umgebung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-199">The following accounts will need to be created on the SQL server with specific permissions and roles to the new database for the installation, deployment and ongoing administration of the App-V environment.</span></span>

-   <span data-ttu-id="4ac4d-200">Erstellen Sie eine Anmeldung für die APP-v-Administratorengruppe auf dem SQL Server und die APPVIRTDB-Datenbank für die "domain\\App-V-Administratoren" (wobei "Domäne" und "App-v-Administratoren" geändert werden, um Ihre eigene Umgebung zu reflektieren), und fügen Sie Sie der SFTAdmin-und SFTEveryone-Datenbankrolle hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-200">Create a login for the App-V administrators group on the SQL Server and the APPVIRTDB database for the “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment) and add them to the SFTAdmin and SFTEveryone database role.</span></span>

    ![App-v 4,6 SQL-Skriptsatz Berechtigungen und Rollen](images/appv46sqlscriptsetpermsroles.gif)

-   <span data-ttu-id="4ac4d-202">Erteilen Sie dieser Gruppe die Berechtigung "jede Definition anzeigen" auf globaler Ebene (Dies ermöglicht es dem Microsoft Application Virtualization Management Server-Setupprozess, zu überprüfen, ob der Verwaltungsserver-Anmeldename bereits vorhanden ist).</span><span class="sxs-lookup"><span data-stu-id="4ac4d-202">Grant this group “VIEW ANY DEFINITION” permission at the global level (This allows the Microsoft Application Virtualization Management Server setup process to verify that the Management Server login already exists).</span></span> <span data-ttu-id="4ac4d-203">Unter MS-SQL 2005 und höher wurden Zugriffseinschränkungen für die in Master. DB enthaltenen Metadaten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-203">Under MS-SQL 2005 and above access restrictions to the metadata contained in master.db were added.</span></span> <span data-ttu-id="4ac4d-204">Der im vorherigen Schritt erstellte Benutzer verfügt standardmäßig nicht über die Rechte, die von der Server Installation benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-204">The user created in the previous step will by default not have the rights needed by the server installation.</span></span> <span data-ttu-id="4ac4d-205">Öffnen Sie die Eigenschaften der zuvor erstellten Anmeldung, Anmeldeeigenschaften- &gt; sicherungsfähige Elemente.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-205">Open the properties of the previously created login, Login Properties-&gt;Securables.</span></span> <span data-ttu-id="4ac4d-206">Fügen Sie die Datenbankinstanz hinzu, und aktivieren Sie "Grant" für "jede Definition anzeigen", wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-206">Add the Database instance and enable “GRANT” for “View any definition” as shown in the screenshot below.</span></span>

    ![App-v 4,6 SQL-Skript Grant Perm für View any DEF](images/appv46sqlscriptviewanydef.gif)

-   <span data-ttu-id="4ac4d-208">Fügen Sie der Rolle \ _ASSIGNMENTS Tabelle für die im vorherigen Schritt erstellte Anmeldung eine Rolle hinzu, um App-v-Administratoren den Zugriff auf die Application Virtualization Management Console zu ermöglichen, mit Role = "admin" und Group \ _ref = "domain\\App-V-Administratoren" (wobei "Domäne" und "App-v-Administratoren" entsprechend ihrer eigenen Umgebung geändert werden).</span><span class="sxs-lookup"><span data-stu-id="4ac4d-208">Add a role to the ROLE\_ASSIGNMENTS table for the login created in the previous step to allow App-V administrators access to the Application Virtualization Management Console, with role = “ADMIN” and group\_ref = “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

    ![App-v 4,6 SQL-Skript Rollenzuweisung](images/appv46sqlscriptroleassign.gif)

-   <span data-ttu-id="4ac4d-210">Erstellen Sie die Anmeldung für SQL Server und die App-V-Datenbank für den Verwaltungs Server.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-210">Create login for SQL Server and App-V database for the Management Server.</span></span> <span data-ttu-id="4ac4d-211">Dieses Konto wird vom Microsoft Application Virtualization Management Server zum Herstellen einer Verbindung mit dem Datenspeicher verwendet und ist für die Wartung von Clientanforderungen für gestreamte Anwendungen verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-211">This account is used by the Microsoft Application Virtualization Management Server to connect to the data store and is responsible for servicing client requests for streamed applications.</span></span> <span data-ttu-id="4ac4d-212">Je nachdem, wo SQL Server und Verwaltungsserver installiert werden sollen, gibt es zwei Optionen:</span><span class="sxs-lookup"><span data-stu-id="4ac4d-212">There are two options, depending on where the SQL Server and Management Server are to be installed:</span></span>

    1.  <span data-ttu-id="4ac4d-213">Wenn Verwaltungs Server und SQL Server auf demselben Computer installiert werden, fügen Sie einen Anmeldenamen für den NT-AUTHORITY\\NETWORK-Dienst hinzu, und fügen Sie ihn den Datenbankrollen SFTUser und SFTEveryone hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-213">If Management Server and SQL Server are going to be installed on the same computer, add a login for NT AUTHORITY\\NETWORK SERVICE and add it to the SFTUser and SFTEveryone database roles.</span></span>

    2.  <span data-ttu-id="4ac4d-214">Wenn der Verwaltungsserver und SQL Server auf unterschiedlichen Computern installiert werden sollen, fügen Sie eine Anmeldung für "domain\\App-V Servername $" hinzu (wobei "App-v Servername" der Name des Servers ist, auf dem der APP-v-Verwaltungsserver installiert wird), und fügen Sie ihn den Datenbankrollen SFTUser und SFTEveryone hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-214">If the Management Server and SQL Server are to be installed on different computers, add a login for “domain\\App-V Server Name$” (where “App-V Server Name” is the name of the server where the App-V Management Server will be installed) and add it to the SFTUser and SFTEveryone database roles.</span></span>

-   <span data-ttu-id="4ac4d-215">Öffnen Sie das Abfragefenster im SQL-Fenster, und führen Sie das folgende SQL aus:</span><span class="sxs-lookup"><span data-stu-id="4ac4d-215">Open the query window on the SQL window and run the following SQL:</span></span>

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    <span data-ttu-id="4ac4d-216">Hierbei handelt es sich um den Namen der APP-v-Datenbank, die im vorherigen Schritt auf dem SQL Server erstellt wurde, und der Benutzer, der die Installation des App-v-Servers durchführen soll, muss ein Mitglied von "domain\\App-V-Administratoren" sein (wobei "Domäne" und "App-v-Administratoren" geändert werden, um Ihre eigene Umgebung APPVIRTDB).</span><span class="sxs-lookup"><span data-stu-id="4ac4d-216">Where the APPVIRTDB is the name of the App-V Database created on the SQL Server in the previous step, and the user who is going to do the install of the App-v server needs to be a member of “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

### <span data-ttu-id="4ac4d-217">Aufgaben, die von den Infrastrukturadministratoren ausgeführt werden sollen</span><span class="sxs-lookup"><span data-stu-id="4ac4d-217">Tasks to be performed by the Infrastructure administrators</span></span>

1.  <span data-ttu-id="4ac4d-218">Der Administrator in der Gruppe "App-v-Administratoren" sollte App-v installieren.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-218">Administrator in the “App-V Admins” group should install App-V.</span></span>

    <span data-ttu-id="4ac4d-219">Verwenden Sie Informationen der SQL-Administratoren zum Auswählen des SQL-Servers und der Datenbank, die in den vorherigen Schritten erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-219">Use information from the SQL administrators for selecting the SQL Server and database created in the previous steps.</span></span>

2.  <span data-ttu-id="4ac4d-220">Der Administrator in der Gruppe "App-V-Administratoren" meldet sich bei Application Virtualization Management Console an und löscht die folgenden Objekte aus der Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-220">Administrator in the “App-V Admins” group logs in to Application Virtualization Management Console and deletes the following objects from the Management Console.</span></span>

    **<span data-ttu-id="4ac4d-221">Warnung</span><span class="sxs-lookup"><span data-stu-id="4ac4d-221">Warning</span></span>**  
    <span data-ttu-id="4ac4d-222">Dies ist erforderlich, da das herkömmliche Setup bestimmte Datensätze in der Datenbank auffüllt, die nicht ausgefüllt werden, wenn Sie die Installation für eine bereits vorhandene Datenbank ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-222">This is required as the traditional setup populates certain records in the database that are not populated if you run the install against an already existing database.</span></span> <span data-ttu-id="4ac4d-223">Löschen Sie die folgenden Objekte:</span><span class="sxs-lookup"><span data-stu-id="4ac4d-223">Delete the following objects:</span></span>

    -   <span data-ttu-id="4ac4d-224">Löschen Sie unter "Servergruppen" "Standardserver Gruppe" "Application Virtualization Management Server".</span><span class="sxs-lookup"><span data-stu-id="4ac4d-224">Under “Server Groups,” “Default Server Group,” delete “Application Virtualization Management Server”</span></span>

    -   <span data-ttu-id="4ac4d-225">Löschen Sie unter "Servergruppen" die Standardserver Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-225">Under “Server Groups,” delete “Default Server Group”</span></span>

    -   <span data-ttu-id="4ac4d-226">Löschen Sie unter "Anbieterrichtlinien" den Eintrag "Standardanbieter".</span><span class="sxs-lookup"><span data-stu-id="4ac4d-226">Under “Provider Policies,” delete “Default Provider”</span></span>



3.  <span data-ttu-id="4ac4d-227">Der Administrator in der App-V-Administratorengruppe sollte dann Folgendes erstellen:</span><span class="sxs-lookup"><span data-stu-id="4ac4d-227">Administrator in the App-V admins group should then create:</span></span>

    -   <span data-ttu-id="4ac4d-228">Erstellen Sie unter "Anbieterrichtlinien" eine neue Anbieterrichtlinie</span><span class="sxs-lookup"><span data-stu-id="4ac4d-228">Under “Provider Policies,” create a New Provider Policy</span></span>

    -   <span data-ttu-id="4ac4d-229">Erstellen einer "Standard Server Gruppe"</span><span class="sxs-lookup"><span data-stu-id="4ac4d-229">Create a “Default Server Group”</span></span>

        **<span data-ttu-id="4ac4d-230">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4ac4d-230">Note</span></span>**  
        <span data-ttu-id="4ac4d-231">Sie müssen eine "Standard Server"-Gruppe erstellen, auch wenn Sie nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-231">You must create a “Default Server” group even if you will not be used.</span></span> <span data-ttu-id="4ac4d-232">Das Serverinstallationsprogramm sucht nur nach der "Standardserver Gruppe", wenn Sie versuchen, den Server hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-232">The server installer only looks for the "Default Server Group" when trying to add the server.</span></span>  <span data-ttu-id="4ac4d-233">Wenn keine "Standard Server Gruppe" vorhanden ist, tritt bei der Installation ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-233">If there is no "Default Server Group" then the installation will fail.</span></span> <span data-ttu-id="4ac4d-234">Wenn Sie beabsichtigen, andere Servergruppen als die standardmäßige Verwendung zu verwenden, müssen Sie nur die "Standardserver Gruppe" beibehalten, wenn Sie beabsichtigen, nachfolgende App-V-Verwaltungsserver zu Ihrer Infrastruktur hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-234">If you plan on using server groups other than the default that is fine, it’s just necessary to retain the "Default Server Group" if you plan on adding subsequent App-V Management Servers to your infrastructure.</span></span>



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <span data-ttu-id="4ac4d-235">Fazit</span><span class="sxs-lookup"><span data-stu-id="4ac4d-235">Conclusion</span></span>


<span data-ttu-id="4ac4d-236">Abschließend können die Informationen in diesem Dokument einem Administrator helfen, mit den SQL-Administratoren zusammenzuarbeiten, um einen Bereitstellungspfad zu entwickeln, der für die Sicherheits-und Verwaltungsabteilungen in einer Organisation verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-236">In conclusion, the information in this document allows an administrator to work with the SQL administrators to develop a deployment path that works for the security and administrative divisions in an organization.</span></span> <span data-ttu-id="4ac4d-237">Nach dem Lesen dieses Dokuments und dem Testen der dokumentierten Aufgaben sollte ein Administrator bereit sein, die App-V-Infrastruktur in dieser Art von Umgebung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="4ac4d-237">After reading this document and testing the tasks documented, an administrator should be ready to implement their App-V infrastructure in this type of environment.</span></span>









