---
title: So stellen Sie die App-V-Datenbanken mithilfe von SQL-Skripts bereit
description: So stellen Sie die App-V-Datenbanken mithilfe von SQL-Skripts bereit
author: dansimp
ms.assetid: 1183b1bc-d4d7-4914-a049-06e82bf2d96d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4695d105c1aa6732efb6b8ed05169cf29e7f972b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805477"
---
# <span data-ttu-id="97269-103">So stellen Sie die App-V-Datenbanken mithilfe von SQL-Skripts bereit</span><span class="sxs-lookup"><span data-stu-id="97269-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>

<span data-ttu-id="97269-104">Verwenden Sie die folgenden Anweisungen, um SQL-Skripts anstelle des Windows Installers zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="97269-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

- <span data-ttu-id="97269-105">Installieren der App-V 5,1-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="97269-105">Install the App-V 5.1 databases</span></span>
- <span data-ttu-id="97269-106">Aktualisieren der App-V-Datenbanken auf eine neuere Version</span><span class="sxs-lookup"><span data-stu-id="97269-106">Upgrade the App-V databases to a later version</span></span>

> [!NOTE]
> <span data-ttu-id="97269-107">Wenn Sie die APP-v 5,0 SP3-Datenbank bereits bereitgestellt haben, müssen die SQL-Skripts nicht auf App-v 5,1 aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="97269-107">If you have already deployed the App-V 5.0 SP3 database, the SQL scripts are not required to upgrade to App-V 5.1.</span></span>

## <span data-ttu-id="97269-108">Installieren der App-V-Datenbanken mithilfe von SQL-Skripts</span><span class="sxs-lookup"><span data-stu-id="97269-108">How to install the App-V databases by using SQL scripts</span></span>

1. <span data-ttu-id="97269-109">Bevor Sie die Datenbankskripts installieren, überprüfen und belassen Sie eine Kopie der App-V-Lizenzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="97269-109">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="97269-110">Durch Ausführen der Datenbankskripts erklären Sie sich mit den Lizenzbedingungen einverstanden.</span><span class="sxs-lookup"><span data-stu-id="97269-110">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="97269-111">Wenn Sie diese nicht akzeptieren, sollten Sie diese Software nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="97269-111">If you do not accept them, you should not use this software.</span></span>
1. <span data-ttu-id="97269-112">Kopieren Sie die **appv\_server\_setup.exe** aus dem App-V-Veröffentlichungsmedium an einen temporären Speicherort.</span><span class="sxs-lookup"><span data-stu-id="97269-112">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>
1. <span data-ttu-id="97269-113">Führen Sie an einer Eingabeaufforderung **appv\_server\_setup.exe** aus, und geben Sie einen temporären Speicherort zum Extrahieren der Datenbankskripts an.</span><span class="sxs-lookup"><span data-stu-id="97269-113">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

    <span data-ttu-id="97269-114">Beispiel: appv\_server\_setup.exe/Layout c:\\ &lt; _temporären Standort Pfad_&gt;</span><span class="sxs-lookup"><span data-stu-id="97269-114">Example: appv\_server\_setup.exe /layout c:\\&lt;_temporary location path_&gt;</span></span>

1. <span data-ttu-id="97269-115">Navigieren Sie zu dem temporären Speicherort, den Sie erstellt haben, öffnen Sie den extrahierten **DatabaseScripts** -Ordner, und überprüfen Sie die entsprechende Readme.txt Datei, um Anweisungen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="97269-115">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

    | <span data-ttu-id="97269-116">Datenbank</span><span class="sxs-lookup"><span data-stu-id="97269-116">Database</span></span> | <span data-ttu-id="97269-117">Speicherort der Readme.txt zu verwendenden Datei</span><span class="sxs-lookup"><span data-stu-id="97269-117">Location of Readme.txt file to use</span></span> |
    |--|--|
    | <span data-ttu-id="97269-118">Verwaltungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="97269-118">Management database</span></span> | <span data-ttu-id="97269-119">ManagementDatabase-Unterordner</span><span class="sxs-lookup"><span data-stu-id="97269-119">ManagementDatabase subfolder</span></span> |
    | <span data-ttu-id="97269-120">Berichtsdatenbank</span><span class="sxs-lookup"><span data-stu-id="97269-120">Reporting database</span></span> | <span data-ttu-id="97269-121">ReportingDatabase-Unterordner</span><span class="sxs-lookup"><span data-stu-id="97269-121">ReportingDatabase subfolder</span></span> |

> [!CAUTION]
> <span data-ttu-id="97269-122">Die readme.txt-Datei im ManagementDatabase-Unterordner ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="97269-122">The readme.txt file in the ManagementDatabase subfolder is out of date.</span></span> <span data-ttu-id="97269-123">Die Informationen in den aktualisierten Readme-Dateien unten sind die aktuellsten und sollten die Readme-Informationen ersetzen, die in den **DatabaseScripts** -Ordnern zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="97269-123">The information in the updated readme files below is the most current and should supersede the readme information provided in the **DatabaseScripts** folders.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97269-124">Das InsertVersionInfo. SQL-Skript ist für Versionen der APP-v-Verwaltungsdatenbank später als App-v 5,0 SP3 nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="97269-124">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="97269-125">Das Skript "Permissions. SQL" sollte gemäß **Schritt 2** im [KB-Artikel 3031340](https://support.microsoft.com/kb/3031340)aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="97269-125">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span> <span data-ttu-id="97269-126">**Schritt 1** ist für Versionen von App-v später als App-v 5,0 SP3 nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="97269-126">**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

## <span data-ttu-id="97269-127">Aktualisierte Informationen zur Verwaltungsdatenbank-Readme-Datei</span><span class="sxs-lookup"><span data-stu-id="97269-127">Updated management database README file content</span></span>

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************


Steps to install "AppVManagement" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
    Permissions.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the
    necessary SQL Server client software is installed and available from
    the specified location.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVManagement".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
##     in the file will not work.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. Run the following scripts against the "AppVManagement" database using the
    same account as above in order.

    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
##     Permissions.sql

```

## <span data-ttu-id="97269-128">Aktualisierte Informationen zur Berichtsdatenbank-Readme-Datei</span><span class="sxs-lookup"><span data-stu-id="97269-128">Updated reporting database README file content</span></span>

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************

Steps to install "AppVReporting" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    UpgradeDatabase.sql
    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
    ScheduleReportingJob.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the 
    necessary SQL Server client software is installed and executable from
    the location you have chosen.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVReporting".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
    in the file will not work.

 3. Review the ScheduleReportingJob.sql file and make sure that the stored proc schedule
    time is acceptable. The default stored proc schedule time is at 12.01 AM (line 84). 
    If this time is not suitable, you can change this to a more suitable time. The time is
##     in the format HHMMSS.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. If upgrading the database, run UpgradeDatabase.sql This will upgrade database schema.

 2. Run the following scripts against the "AppVReporting" database using the
    same account as above in order.

    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
##     ScheduleReportingJob.sql

```

**<span data-ttu-id="97269-129">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="97269-129">Got an App-V issue?</span></span>** <span data-ttu-id="97269-130">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="97269-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="97269-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="97269-131">Related topics</span></span>

[<span data-ttu-id="97269-132">Bereitstellen des App-V 5.1-Servers</span><span class="sxs-lookup"><span data-stu-id="97269-132">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="97269-133">So stellen Sie den App-V 5.1-Server bereit</span><span class="sxs-lookup"><span data-stu-id="97269-133">How to Deploy the App-V 5.1 Server</span></span>](how-to-deploy-the-app-v-51-server.md)
