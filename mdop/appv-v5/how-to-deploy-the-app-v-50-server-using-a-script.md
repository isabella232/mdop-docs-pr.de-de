---
title: So stellen Sie den App-V 5.0-Server mithilfe eines Skripts bereit
description: So stellen Sie den App-V 5.0-Server mithilfe eines Skripts bereit
author: dansimp
ms.assetid: b91a35c8-df9e-4065-9187-abafbe565b84
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: aeb16d166fe7b1c4bb418c212024c49f6b151b94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805525"
---
# <span data-ttu-id="7609e-103">So stellen Sie den App-V 5.0-Server mithilfe eines Skripts bereit</span><span class="sxs-lookup"><span data-stu-id="7609e-103">How to Deploy the App-V 5.0 Server Using a Script</span></span>


<span data-ttu-id="7609e-104">Um das Setup des **appv\_server\_setup.exe** Servers erfolgreich über die Befehlszeile abzuschließen, müssen Sie mehrere Parameter angeben und kombinieren.</span><span class="sxs-lookup"><span data-stu-id="7609e-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

<span data-ttu-id="7609e-105">Verwenden Sie die folgenden Tabellen, um weitere Informationen zum Installieren des App-V 5,0-Servers über die Befehlszeile zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7609e-105">Use the following tables for more information about installing the App-V 5.0 server using the command line.</span></span>

>[!NOTE]
> <span data-ttu-id="7609e-106">Die Informationen in den folgenden Tabellen können auch über die Befehlszeile aufgerufen werden, indem Sie den folgenden Befehl eingeben:</span><span class="sxs-lookup"><span data-stu-id="7609e-106">The information in the following tables can also be accessed using the command line by typing the following command:</span></span>
>```
> appv\_server\_setup.exe /?
>```

## <span data-ttu-id="7609e-107">Allgemeine Parameter und Beispiele</span><span class="sxs-lookup"><span data-stu-id="7609e-107">Common parameters and Examples</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-108">So installieren Sie den Verwaltungsserver und die Verwaltungsdatenbank auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="7609e-108">To Install the Management server and Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-109">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-109">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-110">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-111">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-112">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-113">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7609e-114">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-116">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-117">Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-117">To use a custom instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-118">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-118">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-119">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-119">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-120">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-120">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-121">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-121">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-122">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7609e-122">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7609e-124">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-124">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-125">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-125">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7609e-126">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-126">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7609e-127">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-127">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="7609e-128">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="7609e-128">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="7609e-129">/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV-Verwaltungsdienst"</span><span class="sxs-lookup"><span data-stu-id="7609e-129">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="7609e-130">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="7609e-130">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="7609e-131">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7609e-131">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="7609e-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="7609e-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7609e-133">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="7609e-133">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>
     
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-134">So installieren Sie den Verwaltungsserver mithilfe einer vorhandenen Verwaltungsdatenbank auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="7609e-134">To Install the Management server using an existing Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-135">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-135">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-136">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-136">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-137">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-137">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-138">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-138">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-139">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-139">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7609e-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-142">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-142">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-143">Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-143">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-144">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-144">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-145">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-145">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-146">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-146">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-147">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-147">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7609e-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7609e-150">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-150">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-151">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-151">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7609e-152">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-152">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7609e-153">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-153">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="7609e-154">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="7609e-154">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="7609e-155">/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV-Verwaltungsdienst"</span><span class="sxs-lookup"><span data-stu-id="7609e-155">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="7609e-156">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="7609e-156">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="7609e-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="7609e-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="7609e-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7609e-159">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="7609e-159">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>  

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-160">So installieren Sie den Verwaltungsserver mithilfe einer vorhandenen Verwaltungsdatenbank auf einem Remotecomputer</span><span class="sxs-lookup"><span data-stu-id="7609e-160">To install the Management server using an existing Management database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-161">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-161">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-162">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-162">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-163">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-163">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-164">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-164">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-165">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-165">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-168">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-168">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-169">Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-169">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-170">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-170">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-171">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-171">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-172">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-172">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-173">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-173">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7609e-176">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-176">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-177">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-177">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7609e-178">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-178">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7609e-179">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-179">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="7609e-180">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="7609e-180">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="7609e-181">/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV-Verwaltungsdienst"</span><span class="sxs-lookup"><span data-stu-id="7609e-181">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="7609e-182">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="7609e-182">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="7609e-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "Sie SQLSERVERMACHINE. Domain Name"</span><span class="sxs-lookup"><span data-stu-id="7609e-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME=”SqlServermachine.domainName”</span></span></p>
    <p><span data-ttu-id="7609e-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="7609e-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7609e-185">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="7609e-185">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-186">So installieren Sie die Verwaltungsdatenbank und den Verwaltungs Server auf demselben Computer</span><span class="sxs-lookup"><span data-stu-id="7609e-186">To Install the Management database and the Management Server on the same computer.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-187">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-187">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-188">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7609e-188">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-190">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-190">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7609e-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-193">Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-193">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-194">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7609e-194">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7609e-196">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-196">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7609e-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-199">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-199">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7609e-200">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-200">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7609e-201">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7609e-201">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="7609e-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="7609e-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7609e-203">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="7609e-203">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="7609e-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="7609e-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="7609e-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-206">So installieren Sie die Verwaltungsdatenbank auf einem anderen Computer als der Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="7609e-206">To install the Management database on a different computer than the Management server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-207">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-207">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-208">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7609e-208">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-210">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-210">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-213">Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-213">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-214">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7609e-214">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7609e-216">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-216">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-219">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-219">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7609e-220">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-220">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7609e-221">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7609e-221">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="7609e-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="7609e-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7609e-223">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="7609e-223">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="7609e-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="7609e-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="7609e-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="7609e-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-226">So installieren Sie den Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="7609e-226">To Install the publishing server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-227">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-227">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-228">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-228">/PUBLISHING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-229">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-229">/PUBLISHING_MGT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-230">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-230">/PUBLISHING_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-231">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-231">/PUBLISHING_WEBSITE_PORT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-232">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-232">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7609e-233">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-233">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7609e-234">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-234">/PUBLISHING_SERVER</span></span></p>
    <p><span data-ttu-id="7609e-235">/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</span><span class="sxs-lookup"><span data-stu-id="7609e-235">/PUBLISHING_MGT_SERVER=”http://ManagementServerName:ManagementPort”</span></span></p>
    <p><span data-ttu-id="7609e-236">/PUBLISHING_WEBSITE_NAME = "Microsoft AppV Publishing Service"</span><span class="sxs-lookup"><span data-stu-id="7609e-236">/PUBLISHING_WEBSITE_NAME=”Microsoft AppV Publishing Service”</span></span></p>
    <p><span data-ttu-id="7609e-237">/PUBLISHING_WEBSITE_PORT = "8081"</span><span class="sxs-lookup"><span data-stu-id="7609e-237">/PUBLISHING_WEBSITE_PORT=”8081”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-238">So installieren Sie den Berichtsserver und die Berichtsdatenbank auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="7609e-238">To Install the Reporting server and Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-239">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-239">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-240">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-240">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-241">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-241">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-242">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-242">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-243">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7609e-243">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7609e-244">/Reporting _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-245">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-245">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-246">Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-246">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-247">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-247">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-248">/Reporting _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-248">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-249">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-249">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-250">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-250">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-251">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7609e-251">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7609e-252">/Reporting _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7609e-253">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-253">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-254">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-254">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-255">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-255">/appv_server_setup.exe /QUIET</span></span></p></li>
    <li><p><span data-ttu-id="7609e-256">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-256">/REPORTING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-257">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="7609e-257">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p></li>
    <li><p><span data-ttu-id="7609e-258">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="7609e-258">/REPORTING_WEBSITE_PORT=”8082”</span></span></p></li>
    <li><p><span data-ttu-id="7609e-259">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7609e-259">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7609e-260">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="7609e-260">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p></li>
    <li><p><span data-ttu-id="7609e-261">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="7609e-261">/REPORTING_DB_NAME=”AppVReporting”</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-262">So installieren Sie den Berichtsserver und verwenden eine vorhandene Berichtsdatenbank auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="7609e-262">To Install the Reporting server and using an existing Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-263">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-263">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-264">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-264">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-265">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-265">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-266">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-266">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7609e-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-269">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-269">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-270">Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-270">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-271">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-271">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-272">/Reporting _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-272">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-273">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-273">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-274">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-274">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7609e-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7609e-277">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-277">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-278">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-278">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7609e-279">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-279">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7609e-280">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-280">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="7609e-281">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="7609e-281">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="7609e-282">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="7609e-282">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="7609e-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="7609e-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="7609e-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7609e-285">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="7609e-285">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-286">So installieren Sie den Berichtsserver mithilfe einer vorhandenen Berichtsdatenbank auf einem Remotecomputer</span><span class="sxs-lookup"><span data-stu-id="7609e-286">To Install the Reporting server using an existing Reporting database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-287">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-287">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-288">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-288">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-289">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-289">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-290">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-290">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-293">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-293">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-294">Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-294">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-295">/Reporting _SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-295">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7609e-296">/Reporting _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-296">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-297">/Reporting _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-297">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-298">/Reporting _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-298">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7609e-301">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-301">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-302">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-302">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7609e-303">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-303">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7609e-304">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-304">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="7609e-305">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="7609e-305">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="7609e-306">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="7609e-306">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="7609e-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "Sie SQLSERVERMACHINE. Domain Name"</span><span class="sxs-lookup"><span data-stu-id="7609e-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME=”SqlServerMachine.DomainName”</span></span></p>
    <p><span data-ttu-id="7609e-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="7609e-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7609e-309">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="7609e-309">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-310">So installieren Sie die Berichtsdatenbank auf demselben Computer wie der Berichtsserver</span><span class="sxs-lookup"><span data-stu-id="7609e-310">To install the Reporting database on the same computer as the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-311">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-311">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-312">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7609e-312">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7609e-313">/Reporting _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-314">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-314">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7609e-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-317">Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-317">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-318">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7609e-318">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7609e-319">/Reporting _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7609e-320">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-320">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7609e-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-323">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-323">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7609e-324">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-324">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7609e-325">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7609e-325">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="7609e-326">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="7609e-326">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7609e-327">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="7609e-327">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="7609e-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="7609e-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="7609e-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-330">So installieren Sie die Berichtsdatenbank auf einem anderen Computer als der Berichtsserver</span><span class="sxs-lookup"><span data-stu-id="7609e-330">To install the Reporting database on a different computer than the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-331">Verwenden Sie die folgenden Parameter, um die Standardinstanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-331">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-332">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7609e-332">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7609e-333">/Reporting _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-334">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-334">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-337">Verwenden Sie die folgenden Parameter, um eine benutzerdefinierte Instanz von Microsoft SQL Server zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="7609e-337">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7609e-338">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7609e-338">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7609e-339">/Reporting _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7609e-340">/Reporting _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-340">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7609e-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7609e-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7609e-343">Verwenden einer benutzerdefinierten Instanz von Microsoft SQL Server-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7609e-343">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7609e-344">/appv_server_setup.exe/quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-344">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7609e-345">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7609e-345">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="7609e-346">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="7609e-346">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7609e-347">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="7609e-347">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="7609e-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="7609e-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="7609e-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="7609e-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

## <span data-ttu-id="7609e-350">Parameter Definitionen</span><span class="sxs-lookup"><span data-stu-id="7609e-350">Parameter Definitions</span></span>

### <span data-ttu-id="7609e-351">Allgemeine Parameter</span><span class="sxs-lookup"><span data-stu-id="7609e-351">General Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7609e-352">Parameter</span><span class="sxs-lookup"><span data-stu-id="7609e-352">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7609e-353">Information</span><span class="sxs-lookup"><span data-stu-id="7609e-353">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-354">/Quiet</span><span class="sxs-lookup"><span data-stu-id="7609e-354">/QUIET</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-355">Gibt die unbeaufsichtigte Installation an.</span><span class="sxs-lookup"><span data-stu-id="7609e-355">Specifies silent install.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-356">/Uninstall</span><span class="sxs-lookup"><span data-stu-id="7609e-356">/UNINSTALL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-357">Gibt eine Deinstallation an.</span><span class="sxs-lookup"><span data-stu-id="7609e-357">Specifies an uninstall.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-358">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="7609e-358">/LAYOUT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-359">Gibt die Layout-Aktion an.</span><span class="sxs-lookup"><span data-stu-id="7609e-359">Specifies layout action.</span></span> <span data-ttu-id="7609e-360">Dadurch werden die MSIs-und Skriptdateien in einen Ordner extrahiert, ohne das Produkt tatsächlich zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7609e-360">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="7609e-361">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="7609e-361">No value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-362">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="7609e-362">/LAYOUTDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-363">Gibt das layoutverzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="7609e-363">Specifies the layout directory.</span></span> <span data-ttu-id="7609e-364">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7609e-364">Takes a string.</span></span> <span data-ttu-id="7609e-365">Beispiel:/LAYOUTDIR = "C:\Application Virtualization Server"</span><span class="sxs-lookup"><span data-stu-id="7609e-365">For example, /LAYOUTDIR=”C:\Application Virtualization Server”</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-366">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="7609e-366">/INSTALLDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-367">Gibt das Installationsverzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="7609e-367">Specifies the installation directory.</span></span> <span data-ttu-id="7609e-368">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7609e-368">Takes a string.</span></span> <span data-ttu-id="7609e-369">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-369">E.g.</span></span> <span data-ttu-id="7609e-370">/INSTALLDIR = "C:\Program Files\Application Virtualization\Server"</span><span class="sxs-lookup"><span data-stu-id="7609e-370">/INSTALLDIR=”C:\Program Files\Application Virtualization\Server”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-371">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="7609e-371">/MUOPTIN</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-372">Aktiviert Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="7609e-372">Enables Microsoft Update.</span></span> <span data-ttu-id="7609e-373">Kein Wert erwartet</span><span class="sxs-lookup"><span data-stu-id="7609e-373">No value is expected</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-374">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="7609e-374">/ACCEPTEULA</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-375">Akzeptiert den Lizenzvertrag.</span><span class="sxs-lookup"><span data-stu-id="7609e-375">Accepts the license agreement.</span></span> <span data-ttu-id="7609e-376">Dies ist für eine unbeaufsichtigte Installation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7609e-376">This is required for an unattended installation.</span></span> <span data-ttu-id="7609e-377">Beispiel Verwendung: <strong> /ACCEPTEULA </strong> oder <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="7609e-377">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7609e-378">Verwaltungs Server-Installationsparameter</span><span class="sxs-lookup"><span data-stu-id="7609e-378">Management Server Installation Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7609e-379">Parameter</span><span class="sxs-lookup"><span data-stu-id="7609e-379">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7609e-380">Information</span><span class="sxs-lookup"><span data-stu-id="7609e-380">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-381">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-381">/MANAGEMENT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-382">Gibt an, dass der Verwaltungsserver installiert wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-382">Specifies that the management server will be installed.</span></span> <span data-ttu-id="7609e-383">Kein Wert erwartet</span><span class="sxs-lookup"><span data-stu-id="7609e-383">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-384">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-384">/MANAGEMENT_ADMINACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-385">Gibt das Konto an, das dem Administrator Zugriff auf den Verwaltungsserver gewährt wird. dieses Konto kann ein einzelnes Benutzerkonto oder eine Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="7609e-385">Specifies the account that will be allowed to Administrator access to the management server This account can be an individual user account or a group.</span></span> <span data-ttu-id="7609e-386">Beispiel Verwendung: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> .</span><span class="sxs-lookup"><span data-stu-id="7609e-386">Example usage: <strong>/MANAGEMENT_ADMINACCOUNT=”mydomain\admin”</strong>.</span></span> <span data-ttu-id="7609e-387">Wenn <strong> /MANAGEMENT_SERVER </strong> nicht angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7609e-387">If <strong>/MANAGEMENT_SERVER</strong> is not specified, this will be ignored.</span></span> <span data-ttu-id="7609e-388">Gibt das Konto an, das dem Administrator Zugriff auf den Verwaltungsserver gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-388">Specifies the account that will be allowed to Administrator access to the management server.</span></span> <span data-ttu-id="7609e-389">Dies kann ein Benutzerkonto oder eine Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="7609e-389">This can be a user account or a group.</span></span> <span data-ttu-id="7609e-390">Beispiel: <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</span><span class="sxs-lookup"><span data-stu-id="7609e-390">For example, <strong>/MANAGEMENT_ADMINACCOUNT=&quot;mydomain\admin&quot;</strong>.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-391">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-391">/MANAGEMENT_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-392">Gibt den Namen der Website an, die für den Verwaltungsdienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-392">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="7609e-393">Beispiel:/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V-Verwaltungsdienst"</span><span class="sxs-lookup"><span data-stu-id="7609e-393">For example, /MANAGEMENT_WEBSITE_NAME=”Microsoft App-V Management Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-394">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-394">MANAGEMENT_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-395">Gibt die Portnummer an, die vom Verwaltungsdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-395">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="7609e-396">Beispiel:/MANAGEMENT_WEBSITE_PORT = 82.</span><span class="sxs-lookup"><span data-stu-id="7609e-396">For example, /MANAGEMENT_WEBSITE_PORT=82.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7609e-397">Parameter für die Verwaltungs Server-Datenbank</span><span class="sxs-lookup"><span data-stu-id="7609e-397">Parameters for the Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7609e-398">Parameter</span><span class="sxs-lookup"><span data-stu-id="7609e-398">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7609e-399">Information</span><span class="sxs-lookup"><span data-stu-id="7609e-399">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-400">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7609e-400">/DB_PREDEPLOY_MANAGEMENT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-401">Gibt an, dass die Verwaltungsdatenbank installiert wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-401">Specifies that the management database will be installed.</span></span> <span data-ttu-id="7609e-402">Sie müssen über ausreichende Datenbankberechtigungen verfügen, um diese Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7609e-402">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="7609e-403">Kein Wert erwartet</span><span class="sxs-lookup"><span data-stu-id="7609e-403">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-405">Gibt an, dass die SQL-Standardinstanz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-405">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="7609e-406">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="7609e-406">No value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-408">Gibt den Namen der benutzerdefinierten SQL-Instanz an, die zum Erstellen einer neuen Datenbank verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-408">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="7609e-409">Beispiel Verwendung: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MySqlServer" </strong> .</span><span class="sxs-lookup"><span data-stu-id="7609e-409">Example usage: <strong>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”MYSQLSERVER”</strong>.</span></span> <span data-ttu-id="7609e-410">Wenn/DB_PREDEPLOY_MANAGEMENT nicht angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7609e-410">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-411">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-411">/MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-412">Gibt den Namen der neuen Verwaltungsdatenbank an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-412">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="7609e-413">Beispiel Verwendung: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="7609e-413">Example usage: <strong>/MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="7609e-414">Wenn/DB_PREDEPLOY_MANAGEMENT nicht angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7609e-414">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-416">Gibt an, ob der Verwaltungsserver, der auf die Datenbank zugreifen soll, auf dem lokalen Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7609e-416">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="7609e-417">Parameter wechseln, damit kein Wert erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-417">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-419">Gibt das Computerkonto des Remotecomputers an, auf dem der Verwaltungsserver installiert wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-419">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="7609e-420">Verwendungsbeispiel: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\ComputerName"</span><span class="sxs-lookup"><span data-stu-id="7609e-420">Example usage: <strong>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”domain\computername”</span></span></strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-422">Gibt das Administrator Konto an, das zum Installieren des Verwaltungsservers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-422">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="7609e-423">Verwendungsbeispiel: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "DOMAIN\alias"</span><span class="sxs-lookup"><span data-stu-id="7609e-423">Example usage: <strong>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT =”domain\alias”</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7609e-424">Parameter für die Installation des Veröffentlichungsservers</span><span class="sxs-lookup"><span data-stu-id="7609e-424">Parameters for Installing Publishing Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7609e-425">Parameter</span><span class="sxs-lookup"><span data-stu-id="7609e-425">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7609e-426">Information</span><span class="sxs-lookup"><span data-stu-id="7609e-426">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-427">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-427">/PUBLISHING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-428">Gibt an, dass der Veröffentlichungs Server installiert wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-428">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="7609e-429">Kein Wert erwartet</span><span class="sxs-lookup"><span data-stu-id="7609e-429">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-430">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-430">/PUBLISHING_MGT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-431">Gibt die URL des Verwaltungsdiensts an, mit dem der Veröffentlichungsserver eine Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-431">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="7609e-432">Verwendungsbeispiel: <strong> http:// &lt; -Verwaltungsservername &gt; : &lt; Verwaltungsserver-Portnummer &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="7609e-432">Example usage: <strong>http://&lt;management server name&gt;:&lt;Management server port number&gt;</strong>.</span></span> <span data-ttu-id="7609e-433">Wenn/PUBLISHING_SERVER nicht verwendet wird, wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7609e-433">If /PUBLISHING_SERVER is not used, this parameter will be ignored</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-434">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-434">/PUBLISHING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-435">Gibt den Namen der Website an, die für den Veröffentlichungsdienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-435">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="7609e-436">Beispiel:/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"</span><span class="sxs-lookup"><span data-stu-id="7609e-436">For example, /PUBLISHING_WEBSITE_NAME=”Microsoft App-V Publishing Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-437">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-437">/PUBLISHING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-438">Gibt die vom Veröffentlichungsdienst verwendete Portnummer an.</span><span class="sxs-lookup"><span data-stu-id="7609e-438">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="7609e-439">Beispiel:/PUBLISHING_WEBSITE_PORT = 83</span><span class="sxs-lookup"><span data-stu-id="7609e-439">For example, /PUBLISHING_WEBSITE_PORT=83</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7609e-440">Parameter für Reporting Server</span><span class="sxs-lookup"><span data-stu-id="7609e-440">Parameters for Reporting Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7609e-441">Parameter</span><span class="sxs-lookup"><span data-stu-id="7609e-441">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7609e-442">Information</span><span class="sxs-lookup"><span data-stu-id="7609e-442">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-443">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7609e-443">/REPORTING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-444">Gibt an, dass der Berichts Server installiert wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-444">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="7609e-445">Kein Wert erwartet</span><span class="sxs-lookup"><span data-stu-id="7609e-445">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-446">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-446">/REPORTING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-447">Gibt den Namen der Website an, die für den Berichterstellungsdienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-447">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="7609e-448">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-448">E.g.</span></span> <span data-ttu-id="7609e-449">/REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</span><span class="sxs-lookup"><span data-stu-id="7609e-449">/REPORTING_WEBSITE_NAME=&quot;Microsoft App-V ReportingService&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-450">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7609e-450">/REPORTING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-451">Gibt die Portnummer an, die vom Berichterstattungsdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-451">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="7609e-452">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-452">E.g.</span></span> <span data-ttu-id="7609e-453">/REPORTING_WEBSITE_PORT = 82</span><span class="sxs-lookup"><span data-stu-id="7609e-453">/REPORTING_WEBSITE_PORT=82</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

### <span data-ttu-id="7609e-454">Parameter für die Verwendung einer vorhandenen Berichts Server-Datenbank</span><span class="sxs-lookup"><span data-stu-id="7609e-454">Parameters for using an Existing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7609e-455">Parameter</span><span class="sxs-lookup"><span data-stu-id="7609e-455">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7609e-456">Information</span><span class="sxs-lookup"><span data-stu-id="7609e-456">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-458">Gibt an, dass Microsoft SQL Server auf dem lokalen Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7609e-458">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="7609e-459">Parameter wechseln, damit kein Wert erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-459">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-461">Gibt den Namen des Remotecomputers an, auf dem SQL Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7609e-461">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="7609e-462">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7609e-462">Takes a string.</span></span> <span data-ttu-id="7609e-463">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-463">E.g.</span></span> <span data-ttu-id="7609e-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="7609e-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-465">/EXISTING_ Berichterstellung <em> DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-465">/EXISTING_ REPORTING <em>DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-466">Gibt an, dass die SQL-Standardinstanz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-466">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="7609e-467">Parameter wechseln, damit kein Wert erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-467">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-468">/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-468">/EXISTING</em> REPORTING_DB_CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-469">Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-469">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="7609e-470">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7609e-470">Takes a string.</span></span> <span data-ttu-id="7609e-471">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-471">E.g.</span></span> <span data-ttu-id="7609e-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MySQLServer&quot;</span><span class="sxs-lookup"><span data-stu-id="7609e-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-473">/EXISTING_ Berichterstellung _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-473">/EXISTING_ REPORTING _DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-474">Gibt den Namen der vorhandenen Berichtsdatenbank an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-474">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="7609e-475">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7609e-475">Takes a string.</span></span> <span data-ttu-id="7609e-476">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-476">E.g.</span></span> <span data-ttu-id="7609e-477">/EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</span><span class="sxs-lookup"><span data-stu-id="7609e-477">/EXISTING_REPORTING_DB_NAME=&quot;AppVReporting&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7609e-478">Parameter für die Installation der Berichts Server-Datenbank</span><span class="sxs-lookup"><span data-stu-id="7609e-478">Parameters for installing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7609e-479">Parameter</span><span class="sxs-lookup"><span data-stu-id="7609e-479">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7609e-480">Information</span><span class="sxs-lookup"><span data-stu-id="7609e-480">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-481">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7609e-481">/DB_PREDEPLOY_REPORTING</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-482">Gibt an, dass die Berichtsdatenbank installiert wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-482">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="7609e-483">Für diese Installation sind DBA-Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7609e-483">DBA permissions are required for this installation.</span></span> <span data-ttu-id="7609e-484">Kein Wert erwartet</span><span class="sxs-lookup"><span data-stu-id="7609e-484">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-486">Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-486">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="7609e-487">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7609e-487">Takes a string.</span></span> <span data-ttu-id="7609e-488">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-488">E.g.</span></span> <span data-ttu-id="7609e-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MySQLServer&quot;</span><span class="sxs-lookup"><span data-stu-id="7609e-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-490">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-490">/REPORTING_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-491">Gibt den Namen der neuen Berichtsdatenbank an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-491">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="7609e-492">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7609e-492">Takes a string.</span></span> <span data-ttu-id="7609e-493">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-493">E.g.</span></span> <span data-ttu-id="7609e-494">/REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</span><span class="sxs-lookup"><span data-stu-id="7609e-494">/REPORTING_DB_NAME=&quot;AppVMgmtDB&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-496">Gibt an, dass der Berichtsserver, auf den die Datenbank zugreifen soll, auf dem lokalen Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7609e-496">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="7609e-497">Parameter wechseln, damit kein Wert erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-497">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-499">Gibt das Computerkonto des Remotecomputers an, auf dem der Berichtsserver installiert wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-499">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="7609e-500">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7609e-500">Takes a string.</span></span> <span data-ttu-id="7609e-501">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-501">E.g.</span></span> <span data-ttu-id="7609e-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; Domain\ComputerName&quot;</span><span class="sxs-lookup"><span data-stu-id="7609e-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot;domain\computername&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7609e-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-504">Gibt das Administrator Konto an, das zum Installieren des App-V-Berichtsservers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-504">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="7609e-505">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7609e-505">Takes a string.</span></span> <span data-ttu-id="7609e-506">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-506">E.g.</span></span> <span data-ttu-id="7609e-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; DOMAIN\alias&quot;</span><span class="sxs-lookup"><span data-stu-id="7609e-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot;domain\alias&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7609e-508">Parameter für die Verwendung einer vorhandenen Verwaltungs Server-Datenbank</span><span class="sxs-lookup"><span data-stu-id="7609e-508">Parameters for using an existing Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7609e-509">Parameter</span><span class="sxs-lookup"><span data-stu-id="7609e-509">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7609e-510">Information</span><span class="sxs-lookup"><span data-stu-id="7609e-510">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7609e-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-512">Gibt an, dass SQL Server auf dem lokalen Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7609e-512">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="7609e-513">Parameter wechseln, damit kein Wert erwartet wird. Wenn/DB_PREDEPLOY_MANAGEMENT angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7609e-513">Switch parameter so no value is expected.If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-515">Gibt den Namen des Remotecomputers an, auf dem SQL Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7609e-515">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="7609e-516">Nimmt eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="7609e-516">Takes a string.</span></span> <span data-ttu-id="7609e-517">z.B.</span><span class="sxs-lookup"><span data-stu-id="7609e-517">E.g.</span></span> <span data-ttu-id="7609e-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="7609e-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7609e-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-520">Gibt an, dass die SQL-Standardinstanz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-520">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="7609e-521">Parameter wechseln, damit kein Wert erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="7609e-521">Switch parameter so no value is expected.</span></span> <span data-ttu-id="7609e-522">Wenn/DB_PREDEPLOY_MANAGEMENT angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7609e-522">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7609e-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7609e-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-524">Gibt den Namen der benutzerdefinierten SQL-Instanz an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-524">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="7609e-525">Beispiel Verwendung <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> .</span><span class="sxs-lookup"><span data-stu-id="7609e-525">Example usage <strong>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”AppVManagement”</strong>.</span></span> <span data-ttu-id="7609e-526">Wenn/DB_PREDEPLOY_MANAGEMENT angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7609e-526">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7609e-527">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7609e-527">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7609e-528">Gibt den Namen der vorhandenen Verwaltungsdatenbank an, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7609e-528">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="7609e-529">Beispiel Verwendung: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="7609e-529">Example usage: <strong>/EXISTING_MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="7609e-530">Wenn/DB_PREDEPLOY_MANAGEMENT angegeben ist, wird diese ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7609e-530">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p>
    <p></p>
    <p><strong><span data-ttu-id="7609e-531">Sie haben einen Vorschlag für App-V </strong> ?</span><span class="sxs-lookup"><span data-stu-id="7609e-531">Got a suggestion for App-V</strong>?</span></span> <span data-ttu-id="7609e-532">Hier können Sie Vorschläge hinzufügen oder abstimmen <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="7609e-532">Add or vote on suggestions <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)">here</a>.</span></span> <strong><span data-ttu-id="7609e-533">Haben Sie eine App-V Issu </strong> e?</span><span class="sxs-lookup"><span data-stu-id="7609e-533">Got an App-V issu</strong>e?</span></span> <span data-ttu-id="7609e-534">Verwenden Sie das <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> App-V TechNet-Forum </a> .</span><span class="sxs-lookup"><span data-stu-id="7609e-534">Use the <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)">App-V TechNet Forum</a>.</span></span></p></td>
</tr>
</tbody>
</table>
  

## <span data-ttu-id="7609e-535">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7609e-535">Related topics</span></span>

[<span data-ttu-id="7609e-536">Bereitstellen des App-V 5.0-Servers</span><span class="sxs-lookup"><span data-stu-id="7609e-536">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

 

 





