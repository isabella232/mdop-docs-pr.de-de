---
title: So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit
description: So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit
author: dansimp
ms.assetid: 15c33d7b-9b61-4dbc-8674-399bb33e5f7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/20/2020
ms.openlocfilehash: 579ca685f677aaaa4f5ebb6ac8d2969fdcbe2cd2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805495"
---
# <span data-ttu-id="63c23-103">So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit</span><span class="sxs-lookup"><span data-stu-id="63c23-103">How to Deploy the App-V 5.1 Server Using a Script</span></span>

<span data-ttu-id="63c23-104">Um das Setup des **appv\_server\_setup.exe** Servers erfolgreich über die Befehlszeile abzuschließen, müssen Sie mehrere Parameter angeben und kombinieren.</span><span class="sxs-lookup"><span data-stu-id="63c23-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

## <span data-ttu-id="63c23-105">Installieren des App-V 5,1-Servers mithilfe eines Skripts</span><span class="sxs-lookup"><span data-stu-id="63c23-105">Install the App-V 5.1 server using a script</span></span>

- <span data-ttu-id="63c23-106">Verwenden Sie die folgenden Informationen zum Installieren des App-V 5,1-Servers über die Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="63c23-106">Use the following information about installing the App-V 5.1 server using the command line.</span></span>

    > [!NOTE]
    > <span data-ttu-id="63c23-107">Die Informationen in den folgenden Tabellen können auch über die Befehlszeile aufgerufen werden, indem Sie den folgenden Befehl eingeben: **appv\_server\_setup.exe/?**.</span><span class="sxs-lookup"><span data-stu-id="63c23-107">The information in the following tables can also be accessed using the command line by typing the following command: **appv\_server\_setup.exe /?**.</span></span>

### <span data-ttu-id="63c23-108">Installieren des Verwaltungsservers und der Verwaltungsdatenbank auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="63c23-108">Install the Management server and Management database on a local machine</span></span>

<span data-ttu-id="63c23-109">Die folgenden Parameter sind sowohl für die standardmäßige als auch für die benutzerdefinierte Instanz von Microsoft SQL Server gültig:</span><span class="sxs-lookup"><span data-stu-id="63c23-109">The following parameters are valid with both the default and custom instance of Microsoft SQL Server:</span></span>

- <span data-ttu-id="63c23-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-110">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="63c23-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-111">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="63c23-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-112">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-113">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="63c23-114">/DB_PREDEPLOY_MANAGEMENT</span></span>
- <span data-ttu-id="63c23-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="63c23-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-116">/MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="63c23-117">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="63c23-117">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### <span data-ttu-id="63c23-118">Installieren des Verwaltungsservers mithilfe einer vorhandenen Verwaltungsdatenbank auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="63c23-118">Install the Management server using an existing Management database on a local machine</span></span>

<span data-ttu-id="63c23-119">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-119">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="63c23-120">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-120">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="63c23-121">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-121">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="63c23-122">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-122">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-123">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-123">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="63c23-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="63c23-126">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-126">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="63c23-127">Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie die folgenden Parameter (Unterschied zur Standardinstanz in *Kursivformatierung*):</span><span class="sxs-lookup"><span data-stu-id="63c23-127">To use a custom instance of Microsoft SQL Server, use the following parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="63c23-128">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-128">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="63c23-129">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-129">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="63c23-130">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-130">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-131">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-131">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="63c23-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="63c23-134">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-134">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="63c23-135">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="63c23-135">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="63c23-136">Installieren des Verwaltungsservers mithilfe einer vorhandenen Verwaltungsdatenbank auf einem Remotecomputer</span><span class="sxs-lookup"><span data-stu-id="63c23-136">Install the Management server using an existing Management database on a remote machine</span></span>

<span data-ttu-id="63c23-137">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-137">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="63c23-138">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-138">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="63c23-139">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-139">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="63c23-140">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-140">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-141">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-141">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="63c23-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="63c23-144">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-144">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="63c23-145">Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-145">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="63c23-146">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-146">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="63c23-147">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-147">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="63c23-148">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-148">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-149">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-149">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="63c23-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="63c23-152">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-152">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="63c23-153">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="63c23-153">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="63c23-154">Installieren der Verwaltungsdatenbank und des Verwaltungsservers auf demselben Computer</span><span class="sxs-lookup"><span data-stu-id="63c23-154">Install the Management database and the Management Server on the same computer</span></span>

<span data-ttu-id="63c23-155">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-155">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="63c23-156">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="63c23-156">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="63c23-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="63c23-158">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-158">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="63c23-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="63c23-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="63c23-161">Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-161">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="63c23-162">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="63c23-162">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="63c23-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="63c23-164">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-164">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="63c23-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="63c23-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="63c23-167">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="63c23-167">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="63c23-168">Installieren der Verwaltungsdatenbank auf einem anderen Computer als dem Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="63c23-168">Install the Management database on a different computer than the Management server</span></span>

<span data-ttu-id="63c23-169">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-169">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="63c23-170">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="63c23-170">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="63c23-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="63c23-172">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-172">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="63c23-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="63c23-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="63c23-175">Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-175">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="63c23-176">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="63c23-176">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="63c23-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="63c23-178">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-178">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="63c23-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="63c23-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="63c23-181">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="63c23-181">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="63c23-182">Installieren des Veröffentlichungsservers</span><span class="sxs-lookup"><span data-stu-id="63c23-182">Install the publishing server</span></span>

<span data-ttu-id="63c23-183">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="63c23-183">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span>

- <span data-ttu-id="63c23-184">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-184">/PUBLISHING_SERVER</span></span>
- <span data-ttu-id="63c23-185">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-185">/PUBLISHING_MGT_SERVER</span></span>
- <span data-ttu-id="63c23-186">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-186">/PUBLISHING_WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-187">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-187">/PUBLISHING_WEBSITE_PORT</span></span>

**<span data-ttu-id="63c23-188">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="63c23-188">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### <span data-ttu-id="63c23-189">Installieren des Berichtsservers und der Berichtsdatenbank auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="63c23-189">Install the Reporting server and Reporting database on a local machine</span></span>

<span data-ttu-id="63c23-190">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-190">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="63c23-191">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-191">/REPORTING _SERVER</span></span>
- <span data-ttu-id="63c23-192">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-192">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-193">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-193">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-194">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="63c23-194">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="63c23-195">/Reporting _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="63c23-196">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-196">/REPORTING _DB_NAME</span></span>

<span data-ttu-id="63c23-197">Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-197">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="63c23-198">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-198">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="63c23-199">/Reporting _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-199">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="63c23-200">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-200">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-201">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-201">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-202">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="63c23-202">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="63c23-203">/Reporting _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="63c23-204">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-204">/REPORTING _DB_NAME</span></span>

**<span data-ttu-id="63c23-205">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="63c23-205">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="63c23-206">Installieren des Berichtsservers und Verwenden einer vorhandenen Berichtsdatenbank auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="63c23-206">Install the Reporting server and using an existing Reporting database on a local machine</span></span>

<span data-ttu-id="63c23-207">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-207">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="63c23-208">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-208">/REPORTING _SERVER</span></span>
- <span data-ttu-id="63c23-209">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-209">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-210">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-210">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="63c23-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="63c23-213">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-213">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="63c23-214">Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-214">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="63c23-215">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-215">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="63c23-216">/Reporting _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-216">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="63c23-217">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-217">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-218">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-218">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="63c23-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="63c23-221">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-221">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="63c23-222">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="63c23-222">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="63c23-223">Installieren des Berichtsservers mithilfe einer vorhandenen Berichtsdatenbank auf einem Remotecomputer</span><span class="sxs-lookup"><span data-stu-id="63c23-223">Install the Reporting server using an existing Reporting database on a remote machine</span></span>

<span data-ttu-id="63c23-224">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-224">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="63c23-225">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-225">/REPORTING _SERVER</span></span>
- <span data-ttu-id="63c23-226">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-226">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-227">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-227">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="63c23-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="63c23-230">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-230">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="63c23-231">Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-231">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="63c23-232">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-232">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="63c23-233">/Reporting _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-233">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="63c23-234">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-234">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="63c23-235">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-235">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="63c23-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="63c23-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="63c23-238">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-238">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="63c23-239">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="63c23-239">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="63c23-240">Installieren der Berichtsdatenbank auf demselben Computer wie der Berichtsserver</span><span class="sxs-lookup"><span data-stu-id="63c23-240">Install the Reporting database on the same computer as the Reporting server</span></span>

<span data-ttu-id="63c23-241">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-241">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="63c23-242">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="63c23-242">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="63c23-243">/Reporting _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="63c23-244">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-244">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="63c23-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="63c23-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="63c23-247">Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-247">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="63c23-248">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="63c23-248">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="63c23-249">/Reporting _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="63c23-250">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-250">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="63c23-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="63c23-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="63c23-253">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="63c23-253">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="63c23-254">Installieren der Berichtsdatenbank auf einem anderen Computer als dem Berichtsserver</span><span class="sxs-lookup"><span data-stu-id="63c23-254">Install the Reporting database on a different computer than the Reporting server</span></span>

<span data-ttu-id="63c23-255">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden (Unterschied zu benutzerdefinierter Instanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-255">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="63c23-256">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="63c23-256">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="63c23-257">/Reporting _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="63c23-258">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-258">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="63c23-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="63c23-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="63c23-261">Wenn Sie eine benutzerdefinierte Instanz von Microsoft SQL Server verwenden möchten, verwenden Sie diese Parameter (Unterschied zur Standardinstanz in *kursiv*Schrift):</span><span class="sxs-lookup"><span data-stu-id="63c23-261">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="63c23-262">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="63c23-262">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="63c23-263">/Reporting _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>
- <span data-ttu-id="63c23-264">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-264">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="63c23-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="63c23-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="63c23-267">Beispiel: Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="63c23-267">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="63c23-268">Parameter Definitionen</span><span class="sxs-lookup"><span data-stu-id="63c23-268">Parameter Definitions</span></span>

#### <span data-ttu-id="63c23-269">Allgemeine Parameter</span><span class="sxs-lookup"><span data-stu-id="63c23-269">General Parameters</span></span>

| <span data-ttu-id="63c23-270">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c23-270">Parameter</span></span> | <span data-ttu-id="63c23-271">Information</span><span class="sxs-lookup"><span data-stu-id="63c23-271">Information</span></span> |
|--|--|
| <span data-ttu-id="63c23-272">/Quiet</span><span class="sxs-lookup"><span data-stu-id="63c23-272">/QUIET</span></span> | <span data-ttu-id="63c23-273">Gibt die unbeaufsichtigte Installation an.</span><span class="sxs-lookup"><span data-stu-id="63c23-273">Specifies silent install.</span></span> |
| <span data-ttu-id="63c23-274">/Uninstall</span><span class="sxs-lookup"><span data-stu-id="63c23-274">/UNINSTALL</span></span> | <span data-ttu-id="63c23-275">Gibt eine Deinstallation an.</span><span class="sxs-lookup"><span data-stu-id="63c23-275">Specifies an uninstall.</span></span> |
| <span data-ttu-id="63c23-276">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="63c23-276">/LAYOUT</span></span> | <span data-ttu-id="63c23-277">Gibt die Layout-Aktion an.</span><span class="sxs-lookup"><span data-stu-id="63c23-277">Specifies layout action.</span></span> <span data-ttu-id="63c23-278">Dadurch werden die MSIs-und Skriptdateien in einen Ordner extrahiert, ohne das Produkt tatsächlich zu installieren.</span><span class="sxs-lookup"><span data-stu-id="63c23-278">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="63c23-279">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="63c23-279">No value is expected.</span></span> |
| <span data-ttu-id="63c23-280">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="63c23-280">/LAYOUTDIR</span></span> | <span data-ttu-id="63c23-281">Gibt das layoutverzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="63c23-281">Specifies the layout directory.</span></span> <span data-ttu-id="63c23-282">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="63c23-282">Takes a string.</span></span> <span data-ttu-id="63c23-283">Verwendungsbeispiel: **/LAYOUTDIR = "C:\\Application Virtualization Server"**</span><span class="sxs-lookup"><span data-stu-id="63c23-283">Example usage: **/LAYOUTDIR="C:\\Application Virtualization Server"**</span></span> |
| <span data-ttu-id="63c23-284">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="63c23-284">/INSTALLDIR</span></span> | <span data-ttu-id="63c23-285">Gibt das Installationsverzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="63c23-285">Specifies the installation directory.</span></span> <span data-ttu-id="63c23-286">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="63c23-286">Takes a string.</span></span> <span data-ttu-id="63c23-287">Beispiel Verwendung: **/INSTALLDIR = "c:\\Programme Files\\Application Virtualization\\Server"**</span><span class="sxs-lookup"><span data-stu-id="63c23-287">Example usage: **/INSTALLDIR="C:\\Program Files\\Application Virtualization\\Server"**</span></span> |
| <span data-ttu-id="63c23-288">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="63c23-288">/MUOPTIN</span></span> | <span data-ttu-id="63c23-289">Aktiviert Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="63c23-289">Enables Microsoft Update.</span></span> <span data-ttu-id="63c23-290">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="63c23-290">No value is expected.</span></span> |
| <span data-ttu-id="63c23-291">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="63c23-291">/ACCEPTEULA</span></span> | <span data-ttu-id="63c23-292">Akzeptiert den Lizenzvertrag.</span><span class="sxs-lookup"><span data-stu-id="63c23-292">Accepts the license agreement.</span></span> <span data-ttu-id="63c23-293">Dies ist für eine unbeaufsichtigte Installation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63c23-293">This is required for an unattended installation.</span></span> <span data-ttu-id="63c23-294">Verwendungsbeispiel: **/ACCEPTEULA** oder **/ACCEPTEULA = 1**</span><span class="sxs-lookup"><span data-stu-id="63c23-294">Example usage: **/ACCEPTEULA** or **/ACCEPTEULA=1**</span></span> |

#### <span data-ttu-id="63c23-295">Verwaltungs Server-Installationsparameter</span><span class="sxs-lookup"><span data-stu-id="63c23-295">Management Server Installation Parameters</span></span>

|<span data-ttu-id="63c23-296">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c23-296">Parameter</span></span> |<span data-ttu-id="63c23-297">Information</span><span class="sxs-lookup"><span data-stu-id="63c23-297">Information</span></span> |
|--|--|
| <span data-ttu-id="63c23-298">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-298">/MANAGEMENT_SERVER</span></span> | <span data-ttu-id="63c23-299">Gibt an, dass der Verwaltungsserver installiert wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-299">Specifies that the management server will be installed.</span></span> <span data-ttu-id="63c23-300">Kein Wert erwartet</span><span class="sxs-lookup"><span data-stu-id="63c23-300">No value is expected</span></span> |
| <span data-ttu-id="63c23-301">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-301">/MANAGEMENT_ADMINACCOUNT</span></span> | <span data-ttu-id="63c23-302">Gibt das Konto an, dem Administrator Zugriff auf den Verwaltungsserver gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-302">Specifies the account that will be allowed Administrator access to the management server.</span></span> <span data-ttu-id="63c23-303">Dies kann ein Benutzerkonto oder eine Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="63c23-303">This can be a user account or a group.</span></span> <span data-ttu-id="63c23-304">Beispiel Verwendung: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**.</span><span class="sxs-lookup"><span data-stu-id="63c23-304">Example usage: **/MANAGEMENT_ADMINACCOUNT="mydomain\\admin"**.</span></span> <span data-ttu-id="63c23-305">Wenn **/MANAGEMENT_SERVER** nicht angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63c23-305">If **/MANAGEMENT_SERVER** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="63c23-306">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-306">/MANAGEMENT_WEBSITE_NAME</span></span> | <span data-ttu-id="63c23-307">Gibt den Namen der Website an, die für den Verwaltungsdienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-307">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="63c23-308">Beispiel Verwendung: **/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V-Verwaltungsdienst"**</span><span class="sxs-lookup"><span data-stu-id="63c23-308">Example usage: **/MANAGEMENT_WEBSITE_NAME="Microsoft App-V Management Service"**</span></span> |
| <span data-ttu-id="63c23-309">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-309">MANAGEMENT_WEBSITE_PORT</span></span> | <span data-ttu-id="63c23-310">Gibt die Portnummer an, die vom Verwaltungsdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-310">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="63c23-311">Verwendungsbeispiel: **/MANAGEMENT_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="63c23-311">Example usage: **/MANAGEMENT_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="63c23-312">Parameter für die Verwaltungs Server-Datenbank</span><span class="sxs-lookup"><span data-stu-id="63c23-312">Parameters for the Management Server Database</span></span>

| <span data-ttu-id="63c23-313">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c23-313">Parameter</span></span> | <span data-ttu-id="63c23-314">Information</span><span class="sxs-lookup"><span data-stu-id="63c23-314">Information</span></span> |
|--|--|
| <span data-ttu-id="63c23-315">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="63c23-315">/DB_PREDEPLOY_MANAGEMENT</span></span> | <span data-ttu-id="63c23-316">Gibt an, dass die Verwaltungsdatenbank installiert wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-316">Specifies that the management database will be installed.</span></span> <span data-ttu-id="63c23-317">Sie müssen über ausreichende Datenbankberechtigungen verfügen, um diese Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="63c23-317">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="63c23-318">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="63c23-318">No value is expected.</span></span> |
| <span data-ttu-id="63c23-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="63c23-320">Gibt an, dass die SQL-Standardinstanz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-320">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="63c23-321">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="63c23-321">No value is expected.</span></span> |
| <span data-ttu-id="63c23-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="63c23-323">Gibt den Namen der benutzerdefinierten SQL-Instanz an, die zum Erstellen einer neuen Datenbank verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-323">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="63c23-324">Beispiel Verwendung: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"**.</span><span class="sxs-lookup"><span data-stu-id="63c23-324">Example usage: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**.</span></span> <span data-ttu-id="63c23-325">Wenn **/DB_PREDEPLOY_MANAGEMENT** nicht angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63c23-325">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="63c23-326">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-326">/MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="63c23-327">Gibt den Namen der neuen Verwaltungsdatenbank an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-327">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="63c23-328">Beispiel Verwendung: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="63c23-328">Example usage: **/MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="63c23-329">Wenn **/DB_PREDEPLOY_MANAGEMENT** nicht angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63c23-329">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="63c23-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="63c23-331">Gibt an, ob der Verwaltungsserver, der auf die Datenbank zugreifen soll, auf dem lokalen Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="63c23-331">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="63c23-332">Parameter wechseln, damit kein Wert erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-332">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="63c23-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="63c23-334">Gibt das Computerkonto des Remotecomputers an, auf dem der Verwaltungsserver installiert wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-334">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="63c23-335">Verwendungsbeispiel: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername"**</span><span class="sxs-lookup"><span data-stu-id="63c23-335">Example usage: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="domain\\computername"**</span></span> |
| <span data-ttu-id="63c23-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="63c23-337">Gibt das Administrator Konto an, das zum Installieren des Verwaltungsservers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-337">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="63c23-338">Verwendungsbeispiel: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="63c23-338">Example usage: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT ="domain\\alias"**</span></span> |

#### <span data-ttu-id="63c23-339">Parameter für die Installation des Veröffentlichungsservers</span><span class="sxs-lookup"><span data-stu-id="63c23-339">Parameters for Installing Publishing Server</span></span>

| <span data-ttu-id="63c23-340">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c23-340">Parameter</span></span> | <span data-ttu-id="63c23-341">Information</span><span class="sxs-lookup"><span data-stu-id="63c23-341">Information</span></span> |
|--|--|
| <span data-ttu-id="63c23-342">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-342">/PUBLISHING_SERVER</span></span> | <span data-ttu-id="63c23-343">Gibt an, dass der Veröffentlichungs Server installiert wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-343">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="63c23-344">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="63c23-344">No value is expected.</span></span> |
| <span data-ttu-id="63c23-345">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-345">/PUBLISHING_MGT_SERVER</span></span> | <span data-ttu-id="63c23-346">Gibt die URL des Verwaltungsdiensts an, mit dem der Veröffentlichungsserver eine Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-346">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="63c23-347">Verwendungsbeispiel: **http://- &lt; Verwaltungsservername &gt; : &lt; Verwaltungsserver- &gt; Portnummer**.</span><span class="sxs-lookup"><span data-stu-id="63c23-347">Example usage: **http://&lt;management server name&gt;:&lt;Management server port number&gt;**.</span></span> <span data-ttu-id="63c23-348">Wenn **/PUBLISHING_SERVER** nicht verwendet wird, wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63c23-348">If **/PUBLISHING_SERVER** is not used, this parameter will be ignored.</span></span> |
| <span data-ttu-id="63c23-349">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-349">/PUBLISHING_WEBSITE_NAME</span></span> | <span data-ttu-id="63c23-350">Gibt den Namen der Website an, die für den Veröffentlichungsdienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-350">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="63c23-351">Beispiel Verwendung: **/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"**</span><span class="sxs-lookup"><span data-stu-id="63c23-351">Example usage: **/PUBLISHING_WEBSITE_NAME="Microsoft App-V Publishing Service"**</span></span> |
| <span data-ttu-id="63c23-352">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-352">/PUBLISHING_WEBSITE_PORT</span></span> | <span data-ttu-id="63c23-353">Gibt die vom Veröffentlichungsdienst verwendete Portnummer an.</span><span class="sxs-lookup"><span data-stu-id="63c23-353">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="63c23-354">Verwendungsbeispiel: **/PUBLISHING_WEBSITE_PORT = 83**</span><span class="sxs-lookup"><span data-stu-id="63c23-354">Example usage: **/PUBLISHING_WEBSITE_PORT=83**</span></span> |

#### <span data-ttu-id="63c23-355">Parameter für Reporting Server</span><span class="sxs-lookup"><span data-stu-id="63c23-355">Parameters for Reporting Server</span></span>

| <span data-ttu-id="63c23-356">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c23-356">Parameter</span></span> | <span data-ttu-id="63c23-357">Information</span><span class="sxs-lookup"><span data-stu-id="63c23-357">Information</span></span> |
|--|--|
| <span data-ttu-id="63c23-358">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="63c23-358">/REPORTING_SERVER</span></span> | <span data-ttu-id="63c23-359">Gibt an, dass der Berichts Server installiert wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-359">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="63c23-360">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="63c23-360">No value is expected.</span></span> |
| <span data-ttu-id="63c23-361">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-361">/REPORTING_WEBSITE_NAME</span></span> | <span data-ttu-id="63c23-362">Gibt den Namen der Website an, die für den Berichterstellungsdienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-362">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="63c23-363">Beispiel Verwendung: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"**</span><span class="sxs-lookup"><span data-stu-id="63c23-363">Example usage: **/REPORTING_WEBSITE_NAME="Microsoft App-V ReportingService"**</span></span> |
| <span data-ttu-id="63c23-364">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="63c23-364">/REPORTING_WEBSITE_PORT</span></span> | <span data-ttu-id="63c23-365">Gibt die Portnummer an, die vom Berichterstattungsdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-365">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="63c23-366">Verwendungsbeispiel: **/REPORTING_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="63c23-366">Example usage: **/REPORTING_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="63c23-367">Parameter für die Verwendung einer vorhandenen Berichts Server-Datenbank</span><span class="sxs-lookup"><span data-stu-id="63c23-367">Parameters for using an Existing Reporting Server Database</span></span>

| <span data-ttu-id="63c23-368">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c23-368">Parameter</span></span> | <span data-ttu-id="63c23-369">Information</span><span class="sxs-lookup"><span data-stu-id="63c23-369">Information</span></span> |
|--|--|
| <span data-ttu-id="63c23-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="63c23-371">Gibt an, dass Microsoft SQL Server auf dem lokalen Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="63c23-371">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="63c23-372">Parameter wechseln, damit kein Wert erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-372">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="63c23-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="63c23-374">Gibt den Namen des Remotecomputers an, auf dem SQL Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="63c23-374">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="63c23-375">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="63c23-375">Takes a string.</span></span> <span data-ttu-id="63c23-376">Verwendungsbeispiel: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="63c23-376">Example usage: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="63c23-377">/EXISTING_ Berichterstellung _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-377">/EXISTING_ REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="63c23-378">Gibt an, dass die SQL-Standardinstanz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-378">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="63c23-379">Parameter wechseln, damit kein Wert erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-379">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="63c23-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="63c23-381">Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-381">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="63c23-382">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="63c23-382">Takes a string.</span></span> <span data-ttu-id="63c23-383">Beispiel Verwendung: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"**</span><span class="sxs-lookup"><span data-stu-id="63c23-383">Example usage: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="63c23-384">/EXISTING_ Berichterstellung _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-384">/EXISTING_ REPORTING _DB_NAME</span></span> | <span data-ttu-id="63c23-385">Gibt den Namen der vorhandenen Berichtsdatenbank an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-385">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="63c23-386">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="63c23-386">Takes a string.</span></span> <span data-ttu-id="63c23-387">Verwendungsbeispiel: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"**</span><span class="sxs-lookup"><span data-stu-id="63c23-387">Example usage: **/EXISTING_REPORTING_DB_NAME="AppVReporting"**</span></span> |

#### <span data-ttu-id="63c23-388">Parameter für die Installation der Berichts Server-Datenbank</span><span class="sxs-lookup"><span data-stu-id="63c23-388">Parameters for installing Reporting Server Database</span></span>

| <span data-ttu-id="63c23-389">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c23-389">Parameter</span></span> | <span data-ttu-id="63c23-390">Information</span><span class="sxs-lookup"><span data-stu-id="63c23-390">Information</span></span> |
|--|--|
| <span data-ttu-id="63c23-391">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="63c23-391">/DB_PREDEPLOY_REPORTING</span></span> | <span data-ttu-id="63c23-392">Gibt an, dass die Berichtsdatenbank installiert wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-392">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="63c23-393">Für diese Installation sind DBA-Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63c23-393">DBA permissions are required for this installation.</span></span> <span data-ttu-id="63c23-394">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="63c23-394">No value is expected.</span></span> |
| <span data-ttu-id="63c23-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="63c23-396">Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-396">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="63c23-397">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="63c23-397">Takes a string.</span></span> <span data-ttu-id="63c23-398">Beispiel Verwendung: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"**</span><span class="sxs-lookup"><span data-stu-id="63c23-398">Example usage: **/REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="63c23-399">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-399">/REPORTING_DB_NAME</span></span> | <span data-ttu-id="63c23-400">Gibt den Namen der neuen Berichtsdatenbank an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-400">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="63c23-401">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="63c23-401">Takes a string.</span></span> <span data-ttu-id="63c23-402">Verwendungsbeispiel: **/REPORTING_DB_NAME = "AppVMgmtDB"**</span><span class="sxs-lookup"><span data-stu-id="63c23-402">Example usage: **/REPORTING_DB_NAME="AppVMgmtDB"**</span></span> |
| <span data-ttu-id="63c23-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="63c23-404">Gibt an, dass der Berichtsserver, auf den die Datenbank zugreifen soll, auf dem lokalen Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="63c23-404">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="63c23-405">Parameter wechseln, damit kein Wert erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-405">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="63c23-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="63c23-407">Gibt das Computerkonto des Remotecomputers an, auf dem der Berichtsserver installiert wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-407">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="63c23-408">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="63c23-408">Takes a string.</span></span> <span data-ttu-id="63c23-409">Verwendungsbeispiel: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\ComputerName"**</span><span class="sxs-lookup"><span data-stu-id="63c23-409">Example usage: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="domain\computername"**</span></span> |
| <span data-ttu-id="63c23-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="63c23-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="63c23-411">Gibt das Administrator Konto an, das zum Installieren des App-V-Berichtsservers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-411">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="63c23-412">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="63c23-412">Takes a string.</span></span> <span data-ttu-id="63c23-413">Verwendungsbeispiel: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="63c23-413">Example usage: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="domain\\alias"**</span></span> |

#### <span data-ttu-id="63c23-414">Parameter für die Verwendung einer vorhandenen Verwaltungs Server-Datenbank</span><span class="sxs-lookup"><span data-stu-id="63c23-414">Parameters for using an existing Management Server Database</span></span>

| <span data-ttu-id="63c23-415">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c23-415">Parameter</span></span> | <span data-ttu-id="63c23-416">Information</span><span class="sxs-lookup"><span data-stu-id="63c23-416">Information</span></span> |
|--|--|
| <span data-ttu-id="63c23-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="63c23-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="63c23-418">Gibt an, dass SQL Server auf dem lokalen Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="63c23-418">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="63c23-419">Parameter wechseln, damit kein Wert erwartet wird. Wenn **/DB_PREDEPLOY_MANAGEMENT** angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63c23-419">Switch parameter so no value is expected.If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="63c23-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="63c23-421">Gibt den Namen des Remotecomputers an, auf dem SQL Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="63c23-421">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="63c23-422">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="63c23-422">Takes a string.</span></span> <span data-ttu-id="63c23-423">Verwendungsbeispiel: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="63c23-423">Example usage: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="63c23-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63c23-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="63c23-425">Gibt an, dass die SQL-Standardinstanz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-425">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="63c23-426">Parameter wechseln, damit kein Wert erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="63c23-426">Switch parameter so no value is expected.</span></span> <span data-ttu-id="63c23-427">Wenn **/DB_PREDEPLOY_MANAGEMENT** angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63c23-427">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="63c23-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="63c23-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="63c23-429">Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-429">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="63c23-430">Beispiel Verwendung **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**.</span><span class="sxs-lookup"><span data-stu-id="63c23-430">Example usage **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="AppVManagement"**.</span></span> <span data-ttu-id="63c23-431">Wenn **/DB_PREDEPLOY_MANAGEMENT** angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63c23-431">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="63c23-432">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="63c23-432">/EXISTING_MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="63c23-433">Gibt den Namen der vorhandenen Verwaltungsdatenbank an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c23-433">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="63c23-434">Beispiel Verwendung: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="63c23-434">Example usage: **/EXISTING_MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="63c23-435">Wenn **/DB_PREDEPLOY_MANAGEMENT** angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63c23-435">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |

<span data-ttu-id="63c23-436">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="63c23-436">Got an App-V issue?</span></span> <span data-ttu-id="63c23-437">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="63c23-437">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="63c23-438">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="63c23-438">Related topics</span></span>

[<span data-ttu-id="63c23-439">Bereitstellen des App-V 5.1-Servers</span><span class="sxs-lookup"><span data-stu-id="63c23-439">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)
