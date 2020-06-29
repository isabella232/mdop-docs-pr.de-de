---
title: So stellen Sie die App-V-Datenbanken mithilfe von SQL-Skripts bereit
description: So stellen Sie die App-V-Datenbanken mithilfe von SQL-Skripts bereit
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805483"
---
# <span data-ttu-id="491e8-103">So stellen Sie die App-V-Datenbanken mithilfe von SQL-Skripts bereit</span><span class="sxs-lookup"><span data-stu-id="491e8-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>


<span data-ttu-id="491e8-104">Verwenden Sie die folgenden Anweisungen, um SQL-Skripts anstelle des Windows Installers zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="491e8-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

-   <span data-ttu-id="491e8-105">Installieren der App-V 5,0-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="491e8-105">Install the App-V 5.0 databases</span></span>

-   <span data-ttu-id="491e8-106">Aktualisieren der 5,0-Datenbanken auf eine neuere Version</span><span class="sxs-lookup"><span data-stu-id="491e8-106">Upgrade the 5.0 databases to a later version</span></span>

**<span data-ttu-id="491e8-107">Installieren der App-V-Datenbanken mithilfe von SQL-Skripts</span><span class="sxs-lookup"><span data-stu-id="491e8-107">How to install the App-V databases by using SQL scripts</span></span>**

1. <span data-ttu-id="491e8-108">Bevor Sie die Datenbankskripts installieren, überprüfen und belassen Sie eine Kopie der App-V-Lizenzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="491e8-108">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="491e8-109">Durch Ausführen der Datenbankskripts erklären Sie sich mit den Lizenzbedingungen einverstanden.</span><span class="sxs-lookup"><span data-stu-id="491e8-109">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="491e8-110">Wenn Sie diese nicht akzeptieren, sollten Sie diese Software nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="491e8-110">If you do not accept them, you should not use this software.</span></span>

2. <span data-ttu-id="491e8-111">Kopieren Sie die **appv\_server\_setup.exe** aus dem App-V-Veröffentlichungsmedium an einen temporären Speicherort.</span><span class="sxs-lookup"><span data-stu-id="491e8-111">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>

3. <span data-ttu-id="491e8-112">Führen Sie an einer Eingabeaufforderung **appv\_server\_setup.exe** aus, und geben Sie einen temporären Speicherort zum Extrahieren der Datenbankskripts an.</span><span class="sxs-lookup"><span data-stu-id="491e8-112">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

   <span data-ttu-id="491e8-113">Beispiel: appv\_server\_setup.exe/Layout c:\\ &lt; temporären Standort Pfad&gt;</span><span class="sxs-lookup"><span data-stu-id="491e8-113">Example: appv\_server\_setup.exe /layout c:\\&lt;temporary location path&gt;</span></span>

4. <span data-ttu-id="491e8-114">Navigieren Sie zu dem temporären Speicherort, den Sie erstellt haben, öffnen Sie den extrahierten **DatabaseScripts** -Ordner, und überprüfen Sie die entsprechende Readme.txt Datei, um Anweisungen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="491e8-114">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="491e8-115">Datenbank</span><span class="sxs-lookup"><span data-stu-id="491e8-115">Database</span></span></th>
   <th align="left"><span data-ttu-id="491e8-116">Speicherort der Readme.txt zu verwendenden Datei</span><span class="sxs-lookup"><span data-stu-id="491e8-116">Location of Readme.txt file to use</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="491e8-117">Verwaltungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="491e8-117">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="491e8-118">ManagementDatabase-Unterordner</span><span class="sxs-lookup"><span data-stu-id="491e8-118">ManagementDatabase subfolder</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="491e8-119">Wichtig</span><span class="sxs-lookup"><span data-stu-id="491e8-119">Important</span></span></strong><br/><p><span data-ttu-id="491e8-120">Wenn Sie die APP-v 5,0 SP3-Verwaltungsdatenbank aktualisieren oder installieren, finden Sie weitere Informationen unter <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> SQL-Skripts zum Installieren oder Aktualisieren der APP-v 5,0 SP3-Verwaltungs Server-Datenbank Fehler </a> .</span><span class="sxs-lookup"><span data-stu-id="491e8-120">If you are upgrading to or installing the App-V 5.0 SP3 Management database, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="491e8-121">Berichtsdatenbank</span><span class="sxs-lookup"><span data-stu-id="491e8-121">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="491e8-122">ReportingDatabase-Unterordner</span><span class="sxs-lookup"><span data-stu-id="491e8-122">ReportingDatabase subfolder</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="491e8-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="491e8-123">Related topics</span></span>


[<span data-ttu-id="491e8-124">Bereitstellen des App-V 5.0-Servers</span><span class="sxs-lookup"><span data-stu-id="491e8-124">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

[<span data-ttu-id="491e8-125">So stellen Sie den App-V 5.0-Server bereit</span><span class="sxs-lookup"><span data-stu-id="491e8-125">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)









