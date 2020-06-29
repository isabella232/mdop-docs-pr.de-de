---
title: So aktivieren Sie die Berichterstellung auf dem App-V 5.1-Client mithilfe von PowerShell
description: So aktivieren Sie die Berichterstellung auf dem App-V 5.1-Client mithilfe von PowerShell
author: dansimp
ms.assetid: c4c58be6-cc50-44f6-bf4f-8346fc5d0c0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1d8c0d5e1930020ed1ce354f806f8917a9644e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805453"
---
# <span data-ttu-id="44bcf-103">So aktivieren Sie die Berichterstellung auf dem App-V 5.1-Client mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="44bcf-103">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>


<span data-ttu-id="44bcf-104">Gehen Sie wie folgt vor, um die App-V 5,1 für die Berichterstellung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="44bcf-104">Use the following procedure to configure the App-V 5.1 for reporting.</span></span>

**<span data-ttu-id="44bcf-105">So konfigurieren Sie den Computer mit dem App-V 5,1-Client für Berichte</span><span class="sxs-lookup"><span data-stu-id="44bcf-105">To configure the computer running the App-V 5.1 client for reporting</span></span>**

1. <span data-ttu-id="44bcf-106">Installieren Sie den App-V 5,1-Client.</span><span class="sxs-lookup"><span data-stu-id="44bcf-106">Install the App-V 5.1 client.</span></span> <span data-ttu-id="44bcf-107">Weitere Informationen zum Installieren des Clients finden Sie unter [Bereitstellen des App-V-Clients](how-to-deploy-the-app-v-client-51gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="44bcf-107">For more information about installing the client see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md).</span></span>

2. <span data-ttu-id="44bcf-108">Nachdem Sie den App-V 5,1-Client installiert haben, verwenden Sie die PowerShell " **AppvClientConfiguration** ", um die entsprechenden Konfigurationseinstellungen für Berichte zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="44bcf-108">After you have installed the App-V 5.1 client, use the **Set-AppvClientConfiguration** PowerShell to configure appropriate Reporting Configuration settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="44bcf-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="44bcf-109">Setting</span></span></th>
   <th align="left"><span data-ttu-id="44bcf-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44bcf-110">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="44bcf-111">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="44bcf-111">ReportingEnabled</span></span></p></td>
   <td align="left"><p><span data-ttu-id="44bcf-112">Ermöglicht es dem Client, Informationen an einen Berichtsserver zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="44bcf-112">Enables the client to return information to a reporting server.</span></span> <span data-ttu-id="44bcf-113">Diese Einstellung ist erforderlich, damit der Client die Berichtsdaten auf dem Client sammelt.</span><span class="sxs-lookup"><span data-stu-id="44bcf-113">This setting is required for the client to collect the reporting data on the client.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="44bcf-114">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="44bcf-114">ReportingServerURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="44bcf-115">Gibt den Speicherort auf dem Berichtsserver an, auf dem Clientinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="44bcf-115">Specifies the location on the reporting server where client information is saved.</span></span> <span data-ttu-id="44bcf-116">Beispiel &lt; : http://reportingservername &gt; : &lt; reportingportnumber &gt; .</span><span class="sxs-lookup"><span data-stu-id="44bcf-116">For example, http://&lt;reportingservername&gt;:&lt;reportingportnumber&gt;.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="44bcf-117">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="44bcf-117">Note</span></span></strong><br/><p><span data-ttu-id="44bcf-118">Hierbei handelt es sich um die Portnummer, die während des Berichts Server-Setups zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="44bcf-118">This is the port number that was assigned during the Reporting Server setup</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="44bcf-119">Anfangszeit für Berichte</span><span class="sxs-lookup"><span data-stu-id="44bcf-119">Reporting Start Time</span></span></p></td>
   <td align="left"><p><span data-ttu-id="44bcf-120">Dies ist so eingestellt, dass der Client automatisch die Daten an den Server sendet.</span><span class="sxs-lookup"><span data-stu-id="44bcf-120">This is set to schedule the client to automatically send the data to the server.</span></span> <span data-ttu-id="44bcf-121">Diese Einstellung zeigt die Stunde an, zu der die Berichtsdaten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="44bcf-121">This setting will indicate the hour at which the reporting data will start to send.</span></span> <span data-ttu-id="44bcf-122">Es ist im 24-Stunden-Format und nimmt eine Zahl zwischen 0-23.</span><span class="sxs-lookup"><span data-stu-id="44bcf-122">It is in the 24 hour format and will take a number between 0-23.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="44bcf-123">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="44bcf-123">ReportingRandomDelay</span></span></p></td>
   <td align="left"><p><span data-ttu-id="44bcf-124">Gibt die maximale Verzögerung (in Minuten) für Daten an, die an den Berichtsserver gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="44bcf-124">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="44bcf-125">Wenn der geplante Task gestartet wird, generiert der Client eine zufällige Verzögerung zwischen 0 und ReportingRandomDelay und wartet die angegebene Dauer vor dem Senden von Daten.</span><span class="sxs-lookup"><span data-stu-id="44bcf-125">When the scheduled task is started, the client generates a random delay between 0 and ReportingRandomDelay and will wait the specified duration before sending data.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="44bcf-126">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="44bcf-126">ReportingInterval</span></span></p></td>
   <td align="left"><p><span data-ttu-id="44bcf-127">Gibt das Wiederholungsintervall an, das vom Client zum erneuten Senden von Daten an den Berichtsserver verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44bcf-127">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="44bcf-128">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="44bcf-128">ReportingDataCacheLimit</span></span></p></td>
   <td align="left"><p><span data-ttu-id="44bcf-129">Gibt die maximale Größe in Megabyte (MB) des XML-Caches zum Speichern von Berichtsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="44bcf-129">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="44bcf-130">Die Größe bezieht sich auf den Cache im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="44bcf-130">The size applies to the cache in memory.</span></span> <span data-ttu-id="44bcf-131">Wenn das Limit erreicht ist, wird die Protokolldatei überschrieben.</span><span class="sxs-lookup"><span data-stu-id="44bcf-131">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="44bcf-132">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="44bcf-132">ReportingDataBlockSize</span></span></p></td>
   <td align="left"><p><span data-ttu-id="44bcf-133">Gibt die maximale Größe in Megabyte (MB) des XML-Caches zum Speichern von Berichtsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="44bcf-133">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="44bcf-134">Die Größe bezieht sich auf den Cache im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="44bcf-134">The size applies to the cache in memory.</span></span> <span data-ttu-id="44bcf-135">Wenn das Limit erreicht ist, wird die Protokolldatei überschrieben.</span><span class="sxs-lookup"><span data-stu-id="44bcf-135">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="44bcf-136">Nachdem die entsprechenden Einstellungen konfiguriert wurden, sammelt der Computer, auf dem der App-V 5,1-Client ausgeführt wird, automatisch Daten, und die Daten werden an den Berichtsserver zurückgesendet.</span><span class="sxs-lookup"><span data-stu-id="44bcf-136">After the appropriate settings have been configured, the computer running the App-V 5.1 client will automatically collect data and will send the data back to the reporting server.</span></span>

   <span data-ttu-id="44bcf-137">Darüber hinaus können Administratoren die Daten mithilfe des PowerShell-Cmdlets " **Send-AppvClientReport** " manuell zurücksenden.</span><span class="sxs-lookup"><span data-stu-id="44bcf-137">Additionally, administrators can manually send the data back in an on-demand manner using the **Send-AppvClientReport** PowerShell cmdlet.</span></span>

   <span data-ttu-id="44bcf-138">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="44bcf-138">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="44bcf-139">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="44bcf-139">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="44bcf-140">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="44bcf-140">Got an App-V issue?</span></span>** <span data-ttu-id="44bcf-141">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="44bcf-141">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="44bcf-142">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="44bcf-142">Related topics</span></span>


[<span data-ttu-id="44bcf-143">Verwalten von App-V 5.1 mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="44bcf-143">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)









