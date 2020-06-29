---
title: Informationen zur App-V 5.0-Berichterstellung
description: Informationen zur App-V 5.0-Berichterstellung
author: dansimp
ms.assetid: 27c33dda-f017-41e3-8a78-1b681543ec4f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a29585886aa20233f49c85101cff570a098c69ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806140"
---
# <span data-ttu-id="46607-103">Informationen zur App-V 5.0-Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="46607-103">About App-V 5.0 Reporting</span></span>


<span data-ttu-id="46607-104">Microsoft Application Virtualization (app-v) 5,0 enthält ein integriertes Berichterstattungsfeature, mit dem Sie Informationen zu Computern sammeln können, auf denen der APP-v 5,0-Client ausgeführt wird, sowie Informationen zur Verwendung des virtuellen Anwendungspakets.</span><span class="sxs-lookup"><span data-stu-id="46607-104">Microsoft Application Virtualization (App-V) 5.0 includes a built-in reporting feature that helps you collect information about computers running the App-V 5.0 client as well as information about virtual application package usage.</span></span> <span data-ttu-id="46607-105">Sie können diese Informationen verwenden, um Berichte aus einer zentralisierten Datenbank zu generieren.</span><span class="sxs-lookup"><span data-stu-id="46607-105">You can use this information to generate reports from a centralized database.</span></span>

## <a href="" id="---------app-v-5-0-reporting-overview"></a> <span data-ttu-id="46607-106">App-V 5,0-Berichtsübersicht</span><span class="sxs-lookup"><span data-stu-id="46607-106">App-V 5.0 Reporting Overview</span></span>


<span data-ttu-id="46607-107">In der folgenden Liste wird der End-to-End-Workflow auf hoher Ebene für die Berichterstellung in App-V 5,0 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46607-107">The following list displays the end–to-end high-level workflow for reporting in App-V 5.0.</span></span>

1.  <span data-ttu-id="46607-108">Der Microsoft Application Virtualization (App-V) 5,0-Berichtsserver verfügt über die folgenden Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="46607-108">The Microsoft Application Virtualization (App-V) 5.0 Reporting server has the following prerequisites:</span></span>

    -   <span data-ttu-id="46607-109">IIS-Webserverrolle (Internet Informationsdienst)</span><span class="sxs-lookup"><span data-stu-id="46607-109">Internet Information Service (IIS) web server role</span></span>

    -   <span data-ttu-id="46607-110">Windows-authentifizierungsrolle (unter **IIS/Sicherheit**)</span><span class="sxs-lookup"><span data-stu-id="46607-110">Windows Authentication role (under **IIS / Security**)</span></span>

    -   <span data-ttu-id="46607-111">SQL Server-Installation und-Ausführung mit SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="46607-111">SQL Server installed and running with SQL Server Reporting Services (SSRS)</span></span>

    <span data-ttu-id="46607-112">Um zu bestätigen, dass SQL Server Reporting Services ausgeführt wird, zeigen Sie `http://localhost/Reports` in einem Webbrowser als Administrator auf dem Server an, auf dem die App-V 5,0-Berichterstellung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="46607-112">To confirm SQL Server Reporting Services is running, view `http://localhost/Reports` in a web browser as administrator on the server that will host App-V 5.0 Reporting.</span></span> <span data-ttu-id="46607-113">Die SQL Server Reporting Services-Startseite sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="46607-113">The SQL Server Reporting Services Home page should display.</span></span>

2.  <span data-ttu-id="46607-114">Installieren Sie den App-V 5,0-Berichtsserver und die zugehörige Datenbank.</span><span class="sxs-lookup"><span data-stu-id="46607-114">Install the App-V 5.0 reporting server and associated database.</span></span> <span data-ttu-id="46607-115">Weitere Informationen zum Installieren des Berichtsservers finden Sie unter [so wird es gemacht: Installieren des Berichtsservers auf einem eigenständigen Computer und Herstellen einer Verbindung mit der Datenbank](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md).</span><span class="sxs-lookup"><span data-stu-id="46607-115">For more information about installing the reporting server see [How to install the Reporting Server on a Standalone Computer and Connect it to the Database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md).</span></span> <span data-ttu-id="46607-116">Konfigurieren Sie den Zeitpunkt, zu dem der Computer, auf dem der App-V 5,0-Client ausgeführt wird, Daten an den Berichtsserver senden soll.</span><span class="sxs-lookup"><span data-stu-id="46607-116">Configure the time when the computer running the App-V 5.0 client should send data to the reporting server.</span></span>

3.  <span data-ttu-id="46607-117">Wenn Sie kein elektronisches Softwareverteilungssystem wie Configuration Manager zum Anzeigen von Berichten verwenden, können Sie Berichte im SQL Server-Berichterstattungsdienst definieren.</span><span class="sxs-lookup"><span data-stu-id="46607-117">If you are not using an electronic software distribution system such as Configuration Manager to view reports then you can define reports in SQL Server Reporting Service.</span></span> <span data-ttu-id="46607-118">Laden Sie vordefinierte appvshort-Berichte aus dem Download Center unter herunter <https://go.microsoft.com/fwlink/?LinkId=397255> .</span><span class="sxs-lookup"><span data-stu-id="46607-118">Download predefined appvshort Reports from the Download Center at <https://go.microsoft.com/fwlink/?LinkId=397255>.</span></span>

    <span data-ttu-id="46607-119">**Hinweis**  Wenn Sie die Configuration Manager-Integration in App-v 5,0 verwenden, werden die meisten Berichte vom Configuration Manager und nicht von App-v 5,0 generiert.</span><span class="sxs-lookup"><span data-stu-id="46607-119">**Note** If you are using the Configuration Manager integration with App-V 5.0, most reports are generated from Configuration Manager rather than from App-V 5.0.</span></span>

     

4.  <span data-ttu-id="46607-120">Nachdem Sie das App-v 5,0 PowerShell-Modul mit `Import-Module AppvClient` als Administrator importiert haben, aktivieren Sie den App-v 5,0-Client.</span><span class="sxs-lookup"><span data-stu-id="46607-120">After importing the App-V 5.0 PowerShell module using `Import-Module AppvClient` as administrator, enable the App-V 5.0 client.</span></span> <span data-ttu-id="46607-121">Dieses PowerShell-Beispiel-Cmdlet ermöglicht die App-V 5,0-Berichterstellung:</span><span class="sxs-lookup"><span data-stu-id="46607-121">This sample PowerShell cmdlet enables App-V 5.0 reporting:</span></span>

    ``` syntax
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    <span data-ttu-id="46607-122">Wenn Sie App-v 5,0-Berichtsdaten sofort senden möchten, führen Sie `Send-AppvClientReport` den App-v 5,0-Client aus.</span><span class="sxs-lookup"><span data-stu-id="46607-122">To immediately send App-V 5.0 report data, run `Send-AppvClientReport` on the App-V 5.0 client.</span></span>

    <span data-ttu-id="46607-123">Weitere Informationen zum Installieren des App-V 5,0-Clients mit aktivierter Berichterstellung finden Sie unter Informationen [zu Clientkonfigurationseinstellungen](about-client-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="46607-123">For more information about installing the App-V 5.0 client with reporting enabled see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span> <span data-ttu-id="46607-124">Informationen zum Verwalten von App-v 5,0-Berichten mit Windows PowerShell finden Sie unter [Aktivieren der Berichterstellung auf dem App-v 5,0-Client mithilfe von PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="46607-124">To administer App-V 5.0 Reporting with Windows PowerShell, see [How to Enable Reporting on the App-V 5.0 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md).</span></span>

5.  <span data-ttu-id="46607-125">Nachdem der Berichtsserver die Daten vom App-V 5,0-Client empfangen hat, sendet er die Daten an die Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="46607-125">After the reporting server receives the data from the App-V 5.0 client it sends the data to the reporting database.</span></span> <span data-ttu-id="46607-126">Wenn die Datenbank die Client Daten empfängt und verarbeitet, wird eine erfolgreiche Antwort an den Berichtsserver gesendet, und dann wird eine Benachrichtigung an den App-V 5,0-Client gesendet.</span><span class="sxs-lookup"><span data-stu-id="46607-126">When the database receives and processes the client data, a successful reply is sent to the reporting server and then a notification is sent to the App-V 5.0 client.</span></span>

6.  <span data-ttu-id="46607-127">Wenn der App-V 5,0-Client die Erfolgsbenachrichtigung erhält, leert er den Datencache, um Platz zu sparen.</span><span class="sxs-lookup"><span data-stu-id="46607-127">When the App-V 5.0 client receives the success notification, it empties the data cache to conserve space.</span></span>

    <span data-ttu-id="46607-128">**Hinweis**  Standardmäßig wird der Cache gelöscht, nachdem der Server den Empfang von Daten bestätigt hat.</span><span class="sxs-lookup"><span data-stu-id="46607-128">**Note** By default the cache is cleared after the server confirms receipt of data.</span></span> <span data-ttu-id="46607-129">Sie können den Client manuell konfigurieren, um den Datencache zu speichern.</span><span class="sxs-lookup"><span data-stu-id="46607-129">You can manually configure the client to save the data cache.</span></span>

     

~~~
If the App-V 5.0 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval. Clients continue to collect data and add it to the cache.
~~~

### <a href="" id="-------------app-v-5-0-reporting-server-frequently-asked-questions"></a> <span data-ttu-id="46607-130">App-V 5,0 Reporting Server – häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="46607-130">App-V 5.0 reporting server frequently asked questions</span></span>

<span data-ttu-id="46607-131">In der folgenden Tabelle werden Antworten auf häufig gestellte Fragen zu App-V 5,0-Berichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46607-131">The following table displays answers to common questions about App-V 5.0 reporting</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46607-132">Frage</span><span class="sxs-lookup"><span data-stu-id="46607-132">Question</span></span></th>
<th align="left"><span data-ttu-id="46607-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="46607-133">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46607-134">Was ist die Häufigkeit, mit der Berichtsinformationen an die Berichtsdatenbank gesendet werden?</span><span class="sxs-lookup"><span data-stu-id="46607-134">What is the frequency that reporting information is sent to the reporting database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-135">Die Häufigkeit hängt davon ab, wie die Berichterstattungs Aufgabe auf dem Computer konfiguriert ist, auf dem der App-V 5,0-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46607-135">The frequency depends on how the reporting task is configured on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="46607-136">Sie müssen die Häufigkeit/das Intervall für das Senden der Berichtsdaten konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="46607-136">You must configure the frequency / interval for sending the reporting data.</span></span> <span data-ttu-id="46607-137">App-V 5,0-Berichterstattung ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="46607-137">App-V 5.0 Reporting is not enabled by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46607-138">Welche Informationen werden in der Berichtsserver-Datenbank gespeichert?</span><span class="sxs-lookup"><span data-stu-id="46607-138">What information is stored in the reporting server database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-139">In der folgenden Liste wird angezeigt, was in der Berichtsdatenbank gespeichert ist:</span><span class="sxs-lookup"><span data-stu-id="46607-139">The following list displays what is stored in the reporting database:</span></span></p>
<ul>
<li><p><span data-ttu-id="46607-140">Das Betriebssystem, das auf dem Computer ausgeführt wird, auf dem der App-V 5,0-Client ausgeführt wird: Hostname, Version, Service Pack, Typ-Client/Server, Prozessorarchitektur.</span><span class="sxs-lookup"><span data-stu-id="46607-140">The operating system running on the computer running the App-V 5.0 client: host name, version, service pack, type - client/server, processor architecture.</span></span></p></li>
<li><p><span data-ttu-id="46607-141">App-V 5,0-Client Informationen: Version.</span><span class="sxs-lookup"><span data-stu-id="46607-141">App-V 5.0 Client information: version.</span></span></p></li>
<li><p><span data-ttu-id="46607-142">Liste der veröffentlichten Pakete: GUID, Versions-GUID, Name.</span><span class="sxs-lookup"><span data-stu-id="46607-142">Published package list: GUID, version GUID, name.</span></span></p></li>
<li><p><span data-ttu-id="46607-143">Anwendungs Nutzungsinformationen: Name, Version, Streamingserver, Benutzer (DOMAIN\alias), paketversions-GUID, Startstatus und-Zeit, Shutdown-Zeit.</span><span class="sxs-lookup"><span data-stu-id="46607-143">Application usage information: name, version, streaming server, user (domain\alias), package version GUID, launch status and time, shutdown time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46607-144">Wie lauten die durchschnittlichen Datenmengen, die an den Berichtsserver gesendet werden?</span><span class="sxs-lookup"><span data-stu-id="46607-144">What is the average volume of information that is sent to the reporting server?</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-145">Das hängt davon ab.</span><span class="sxs-lookup"><span data-stu-id="46607-145">It depends.</span></span> <span data-ttu-id="46607-146">In der folgenden Liste werden die drei Sätze der an den Berichtsserver gesendeten Daten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="46607-146">The following list displays the three sets of the data sent to the reporting server:</span></span></p>
<ol>
<li><p><span data-ttu-id="46607-147">Betriebssystem-und App-V 5,0-Clientinformationen.</span><span class="sxs-lookup"><span data-stu-id="46607-147">Operating system, and App-V 5.0 client information.</span></span> <span data-ttu-id="46607-148">~ 150 Bytes, jedes Mal, wenn diese Daten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="46607-148">~150 Bytes, every time this data is sent.</span></span></p></li>
<li><p><span data-ttu-id="46607-149">Liste der veröffentlichten Pakete</span><span class="sxs-lookup"><span data-stu-id="46607-149">Published package list.</span></span> <span data-ttu-id="46607-150">~ 7 KB für 30 Pakete.</span><span class="sxs-lookup"><span data-stu-id="46607-150">~7 KB for 30 packages.</span></span> <span data-ttu-id="46607-151">Diese wird nur gesendet, wenn die Paketliste mit einer Veröffentlichungsaktualisierung aktualisiert wird, die selten erfolgt; Wenn keine Änderung erfolgt, werden diese Informationen nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="46607-151">This is sent only when the package list is updated with a publishing refresh, which is done infrequently; if there is no change, this information is not sent.</span></span></p></li>
<li><p><span data-ttu-id="46607-152">Informationen zur Verwendung virtueller Anwendungen – ungefähr 0,25 KB pro Ereignis.</span><span class="sxs-lookup"><span data-stu-id="46607-152">Virtual application usage information – about 0.25KB per event.</span></span> <span data-ttu-id="46607-153">Öffnen und schließen zählen als ein Ereignis, wenn beide vor dem Senden der Informationen auftreten.</span><span class="sxs-lookup"><span data-stu-id="46607-153">Opening and closing count as one event if both occur before sending the information.</span></span> <span data-ttu-id="46607-154">Beim Senden mit einer geplanten Aufgabe werden nur die Daten seit dem letzten erfolgreichen Upload an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="46607-154">When sending using a scheduled task, only the data since the last successful upload is sent to the server.</span></span> <span data-ttu-id="46607-155">Wenn Sie manuell über das PowerShell-Cmdlet senden, gibt es ein optionales Argument, das steuert, ob die Daten beim nächsten Mal erneut gesendet werden müssen – dieses Argument ist <strong> DeleteOnSuccess </strong> .</span><span class="sxs-lookup"><span data-stu-id="46607-155">If sending manually through the PowerShell cmdlet, there is an optional argument that controls if the data needs to be re-sent next time around – that argument is <strong>DeleteOnSuccess</strong>.</span></span></p>
<p></p>
<p><span data-ttu-id="46607-156">Wenn beispielsweise zwanzig Anwendungen geöffnet und geschlossen sind und die Berichtsinformationen täglich gesendet werden sollen, sollte der typische tägliche Datenverkehr etwa 0.15 KB + 20 x 0,25 KB oder über 5KB/Benutzer sein.</span><span class="sxs-lookup"><span data-stu-id="46607-156">So for example, if twenty applications are opened and closed and reporting information is scheduled to be sent daily, the typical daily traffic should be about 0.15KB + 20 x 0.25KB, or about 5KB/user</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46607-157">Können Berichte geplant werden?</span><span class="sxs-lookup"><span data-stu-id="46607-157">Can reporting be scheduled?</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-158">Ja.</span><span class="sxs-lookup"><span data-stu-id="46607-158">Yes.</span></span> <span data-ttu-id="46607-159">Neben dem manuellen Senden von Berichten mithilfe von PowerShell-Cmdlets ( <strong> Send-AppvClientReport </strong> ) kann die Aufgabe so geplant werden, dass Sie automatisch erfolgt.</span><span class="sxs-lookup"><span data-stu-id="46607-159">Besides manually sending reporting using PowerShell Cmdlets (<strong>Send-AppvClientReport</strong>), the task can be scheduled so it will happen automatically.</span></span> <span data-ttu-id="46607-160">Es gibt zwei Möglichkeiten, die Berichterstellung zu planen:</span><span class="sxs-lookup"><span data-stu-id="46607-160">There are two ways to schedule the reporting:</span></span></p>
<ol>
<li><p><span data-ttu-id="46607-161">Verwenden von PowerShell-Cmdlets- <strong> AppvClientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="46607-161">Using PowerShell cmdlets - <strong>Set-AppvClientConfiguration</strong>.</span></span> <span data-ttu-id="46607-162">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="46607-162">For example:</span></span></p>
<p><span data-ttu-id="46607-163">Satz-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span><span class="sxs-lookup"><span data-stu-id="46607-163">Set-AppvClientConfiguration -ReportingEnabled 1 - ReportingServerURL <a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span></span></a></p>
<p></p>
<p><span data-ttu-id="46607-164">Eine vollständige Liste der Clientkonfigurationseinstellungen finden Sie unter <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)"> Informationen zu Clientkonfigurationseinstellungen, </a> und suchen Sie nach den folgenden Einträgen: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay </strong> , <strong> ReportingInterval </strong> .</span><span class="sxs-lookup"><span data-stu-id="46607-164">For a complete list of client configuration settings see <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)">About Client Configuration Settings</a> and look for the following entries: <strong>ReportingEnabled</strong>, <strong>ReportingServerURL</strong>, <strong>ReportingDataCacheLimit</strong>, <strong>ReportingDataBlockSize</strong>, <strong>ReportingStartTime</strong>, <strong>ReportingRandomDelay</strong>, <strong>ReportingInterval</strong>.</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="46607-165">Mithilfe von Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="46607-165">By using Group Policy.</span></span> <span data-ttu-id="46607-166">Bei einer Verteilung mithilfe des Domänencontrollers sind die Einstellungen mit den zuvor aufgelisteten identisch.</span><span class="sxs-lookup"><span data-stu-id="46607-166">If distributed using the domain controller, the settings are the same as previously listed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="46607-167">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="46607-167">Note</span></span></strong><br/><p><span data-ttu-id="46607-168">Die Gruppenrichtlinieneinstellungen überschreiben die mit PowerShell konfigurierten lokalen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="46607-168">Group Policy settings override local settings configured using PowerShell.</span></span></p>
</div>
<div>

</div></li>
</ol></td>
</tr>
</tbody>
</table>
 


## <a href="" id="---------app-v-5-0-client-reporting"></a> <span data-ttu-id="46607-169">App-V 5,0-Client Berichte</span><span class="sxs-lookup"><span data-stu-id="46607-169">App-V 5.0 Client Reporting</span></span>


<span data-ttu-id="46607-170">Wenn Sie die APP-v 5,0-Berichterstellung verwenden möchten, müssen Sie den App-v 5,0-Client installieren und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="46607-170">To use App-V 5.0 reporting you must install and configure the App-V 5.0 client.</span></span> <span data-ttu-id="46607-171">Nachdem der Client installiert wurde, verwenden Sie das PowerShell-Cmdlet " **festlegen-AppVClientConfiguration** " oder die **ADMX-Vorlage** , um die Berichterstellung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="46607-171">After the client has been installed, use the **Set-AppVClientConfiguration** PowerShell cmdlet or the **ADMX Template** to configure reporting.</span></span> <span data-ttu-id="46607-172">Die Cmdlets für das Berichterstattungsfeature sind über den folgenden Link verfügbar und werden durch die **Berichterstellung**vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="46607-172">The reporting feature cmdlets are available by using the following link and are prefaced by **Reporting**.</span></span> <span data-ttu-id="46607-173">Eine vollständige Liste der Clientkonfigurationseinstellungen finden Sie unter [Informationen zu Clientkonfigurationseinstellungen](about-client-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="46607-173">For a complete list of client configuration settings see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span> <span data-ttu-id="46607-174">Der folgende Abschnitt enthält Beispiele für die Konfiguration der App-V 5,0-Client Berichterstattung mithilfe von PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46607-174">The following section provides examples of App-V 5.0 client reporting configuration using PowerShell.</span></span>

### <span data-ttu-id="46607-175">Konfigurieren von App-V-Client Berichten mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="46607-175">Configuring App-V Client reporting using PowerShell</span></span>

<span data-ttu-id="46607-176">Die folgenden Beispiele zeigen, wie PowerShell-Parameter die Berichterstattungsfeatures des App-V 5,0-Clients konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="46607-176">The following examples show how PowerShell parameters can configure the reporting features of the App-V 5.0 client.</span></span>

**<span data-ttu-id="46607-177">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="46607-177">Note</span></span>**  
<span data-ttu-id="46607-178">Die folgende Konfigurationsaufgabe kann auch mithilfe von Gruppenrichtlinieneinstellungen in der App-V 5,0 ADMX-Vorlage konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="46607-178">The following configuration task can also be configured using Group Policy settings in the App-V 5.0 ADMX template.</span></span> <span data-ttu-id="46607-179">Weitere Informationen zur Verwendung der ADMX-Vorlage finden Sie unter [Ändern der App-V 5,0-Client Konfiguration mithilfe der ADMX-Vorlage und der Gruppenrichtlinie](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md).</span><span class="sxs-lookup"><span data-stu-id="46607-179">For more information about using the ADMX template, see [How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md).</span></span>
 


<span data-ttu-id="46607-180">**So aktivieren Sie die Berichterstellung und initiieren die Datensammlung auf dem Computer, auf dem der App-V 5,0-Client ausgeführt wird**:</span><span class="sxs-lookup"><span data-stu-id="46607-180">**To enable reporting and to initiate data collection on the computer running the App-V 5.0 client**:</span></span>

`Set-AppVClientConfiguration –ReportingEnabled 1`

<span data-ttu-id="46607-181">**So konfigurieren Sie den Client so, dass Daten automatisch an einen bestimmten Berichtsserver gesendet**werden:</span><span class="sxs-lookup"><span data-stu-id="46607-181">**To configure the client to automatically send data to a specific reporting server**:</span></span>

``` syntax
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30
```

`-ReportingInterval 1 -ReportingRandomDelay 30`

<span data-ttu-id="46607-182">In diesem Beispiel wird der Client so konfiguriert, dass die Berichtsdaten automatisch an die Berichtsserver-URL gesendet werden <strong> http://MyReportingServer:MyPort/ </strong> .</span><span class="sxs-lookup"><span data-stu-id="46607-182">This example configures the client to automatically send the reporting data to the reporting server URL <strong>http://MyReportingServer:MyPort/</strong>.</span></span> <span data-ttu-id="46607-183">Darüber hinaus werden die Berichterstellungsdaten täglich zwischen 8:00 und 8:30 Uhr gesendet, abhängig von der Zufalls Verzögerung, die für die Sitzung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="46607-183">Additionally, the reporting data will be sent daily between 8:00 and 8:30 PM, depending on the random delay generated for the session.</span></span>

<span data-ttu-id="46607-184">**So begrenzen Sie die Größe des Datencaches auf dem Client**:</span><span class="sxs-lookup"><span data-stu-id="46607-184">**To limit the size of the data cache on the client**:</span></span>

`Set-AppvClientConfiguration –ReportingDataCacheLimit 100`

<span data-ttu-id="46607-185">Konfiguriert die maximale Größe des Berichtscaches auf dem Computer, auf dem der App-V 5,0-Client ausgeführt wird, auf 100 MB.</span><span class="sxs-lookup"><span data-stu-id="46607-185">Configures the maximum size of the reporting cache on the computer running the App-V 5.0 client to 100 MB.</span></span> <span data-ttu-id="46607-186">Wenn die Cache Grenze erreicht ist, bevor die Daten an den Server gesendet werden, wird das Protokoll überschrieben, und die Daten werden nach Bedarf überschrieben.</span><span class="sxs-lookup"><span data-stu-id="46607-186">If the cache limit is reached before the data is sent to the server, then the log rolls over and data will be overwritten as necessary.</span></span>

<span data-ttu-id="46607-187">**So konfigurieren Sie die Datenblockgröße, die über das Netzwerk zwischen dem Client und dem Server übertragen wird**:</span><span class="sxs-lookup"><span data-stu-id="46607-187">**To configure the data block size transmitted across the network between the client and the server**:</span></span>

`Set-AppvClientConfiguration –ReportingDataBlockSize 10240`

<span data-ttu-id="46607-188">Gibt den maximalen Datenblock an, der vom Client an 10240 MB gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="46607-188">Specifies the maximum data block that the client sends to 10240 MB.</span></span>

### <span data-ttu-id="46607-189">Gesammelte Datentypen</span><span class="sxs-lookup"><span data-stu-id="46607-189">Types of data collected</span></span>

<span data-ttu-id="46607-190">In der folgenden Tabelle sind die Informationstypen aufgeführt, die Sie mithilfe der App-V 5,0-Berichterstellung erfassen können.</span><span class="sxs-lookup"><span data-stu-id="46607-190">The following table displays the types of information you can collect by using App-V 5.0 reporting.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46607-191">Client Informationen</span><span class="sxs-lookup"><span data-stu-id="46607-191">Client Information</span></span></th>
<th align="left"><span data-ttu-id="46607-192">Paketinformationen</span><span class="sxs-lookup"><span data-stu-id="46607-192">Package Information</span></span></th>
<th align="left"><span data-ttu-id="46607-193">Anwendungsverwendung</span><span class="sxs-lookup"><span data-stu-id="46607-193">Application Usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46607-194">Hostname</span><span class="sxs-lookup"><span data-stu-id="46607-194">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-195">Paket Name</span><span class="sxs-lookup"><span data-stu-id="46607-195">Package Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-196">Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="46607-196">Start and End Times</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46607-197">App-V 5,0-Client Version</span><span class="sxs-lookup"><span data-stu-id="46607-197">App-V 5.0 Client Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-198">Paket Version</span><span class="sxs-lookup"><span data-stu-id="46607-198">Package Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-199">Ausführungs Status</span><span class="sxs-lookup"><span data-stu-id="46607-199">Run Status</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46607-200">Prozessorarchitektur</span><span class="sxs-lookup"><span data-stu-id="46607-200">Processor Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-201">Paketquelle</span><span class="sxs-lookup"><span data-stu-id="46607-201">Package Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-202">Shutdown-Status</span><span class="sxs-lookup"><span data-stu-id="46607-202">Shutdown State</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46607-203">Version des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="46607-203">Operating System Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-204">Prozent zwischengespeichert</span><span class="sxs-lookup"><span data-stu-id="46607-204">Percent Cached</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-205">Name der Anwendung</span><span class="sxs-lookup"><span data-stu-id="46607-205">Application Name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46607-206">Service Pack-Ebene</span><span class="sxs-lookup"><span data-stu-id="46607-206">Service Pack Level</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="46607-207">Anwendungs Version</span><span class="sxs-lookup"><span data-stu-id="46607-207">Application Version</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46607-208">Typ des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="46607-208">Operating System Type</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="46607-209">Benutzername</span><span class="sxs-lookup"><span data-stu-id="46607-209">Username</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="46607-210">Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="46607-210">Connection Group</span></span></p></td>
</tr>
</tbody>
</table>
 


<span data-ttu-id="46607-211">Der Client sammelt und speichert diese Daten im **XML-** Format.</span><span class="sxs-lookup"><span data-stu-id="46607-211">The client collects and saves this data in an **.xml** format.</span></span> <span data-ttu-id="46607-212">Der Datencache ist standardmäßig ausgeblendet und erfordert Administratorrechte, um die XML-Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="46607-212">The data cache is hidden by default and requires administrator rights to open the XML file.</span></span>

### <span data-ttu-id="46607-213">Senden von Daten an den Server</span><span class="sxs-lookup"><span data-stu-id="46607-213">Sending data to the server</span></span>

<span data-ttu-id="46607-214">Sie können den Computer, auf dem der App-V 5,0-Client ausgeführt wird, so konfigurieren, dass Daten automatisch an den angegebenen Berichtsserver gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="46607-214">You can configure the computer that is running the App-V 5.0 client to automatically send data to the specified reporting server.</span></span> <span data-ttu-id="46607-215">Wenn Sie den Server angeben möchten, verwenden Sie das Cmdlet " **festlegen-AppvClientConfiguration** " mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="46607-215">To specify the server use the **Set-AppvClientConfiguration** cmdlet with the following settings:</span></span>

-   <span data-ttu-id="46607-216">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="46607-216">ReportingEnabled</span></span>

-   <span data-ttu-id="46607-217">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="46607-217">ReportingServerURL</span></span>

-   <span data-ttu-id="46607-218">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="46607-218">ReportingStartTime</span></span>

-   <span data-ttu-id="46607-219">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="46607-219">ReportingInterval</span></span>

-   <span data-ttu-id="46607-220">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="46607-220">ReportingRandomDelay</span></span>

<span data-ttu-id="46607-221">Nachdem Sie die vorherigen Einstellungen konfiguriert haben, müssen Sie einen geplanten Vorgang erstellen.</span><span class="sxs-lookup"><span data-stu-id="46607-221">After you configure the previous settings, you must create a scheduled task.</span></span> <span data-ttu-id="46607-222">Der geplante Task setzt sich mit dem Server in Verbindung, der durch die **ReportingServerURL** -Einstellung angegeben wird, und initiiert die Übertragung.</span><span class="sxs-lookup"><span data-stu-id="46607-222">The scheduled task will contact the server specified by the **ReportingServerURL** setting and will initiate the transfer.</span></span> <span data-ttu-id="46607-223">Wenn Sie Daten manuell außerhalb der geplanten Zeiten senden möchten, verwenden Sie das folgende PowerShell-Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="46607-223">If you want to manually send data outside of the scheduled times, use the following PowerShell cmdlet:</span></span>

`Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess`

<span data-ttu-id="46607-224">Wenn der Berichtsserver zuvor konfiguriert wurde, kann der **URL-** Parameter ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="46607-224">If the reporting server has been previously configured, then the **–URL** parameter can be omitted.</span></span> <span data-ttu-id="46607-225">Wenn die Daten an einen anderen Speicherort gesendet werden sollen, geben Sie alternativ eine andere URL an, um die konfigurierte **ReportingServerURL** für diese Datensammlung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="46607-225">Alternatively, if the data should be sent to an alternate location, specify a different URL to override the configured **ReportingServerURL** for this data collection.</span></span>

<span data-ttu-id="46607-226">Der Parameter **-DeleteOnSuccess** gibt an, dass der Datencache gelöscht wird, wenn die Übertragung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="46607-226">The **-DeleteOnSuccess** parameter indicates that if the transfer is successful, then the data cache is cleared.</span></span> <span data-ttu-id="46607-227">Wenn dies nicht angegeben ist, wird der Cache nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="46607-227">If this is not specified, then the cache will not be cleared.</span></span>

### <span data-ttu-id="46607-228">Manuelle Datensammlung</span><span class="sxs-lookup"><span data-stu-id="46607-228">Manual Data Collection</span></span>

<span data-ttu-id="46607-229">Sie können auch das Cmdlet **Send-AppVClientReport** verwenden, um Daten manuell zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="46607-229">You can also use the **Send-AppVClientReport** cmdlet to manually collect data.</span></span> <span data-ttu-id="46607-230">Diese Lösung ist mit oder ohne einen vorhandenen Berichtsserver hilfreich.</span><span class="sxs-lookup"><span data-stu-id="46607-230">This solution is helpful with or without an existing reporting server.</span></span> <span data-ttu-id="46607-231">In der folgenden Liste werden Informationen zum Sammeln von Daten mit oder ohne Berichtsserver angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46607-231">The following list displays information about collecting data with or without a reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46607-232">Mit einem Berichts Server</span><span class="sxs-lookup"><span data-stu-id="46607-232">With a Reporting Server</span></span></th>
<th align="left"><span data-ttu-id="46607-233">Ohne einen Berichts Server</span><span class="sxs-lookup"><span data-stu-id="46607-233">Without a Reporting Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46607-234">Wenn Sie über einen vorhandenen App-V 5,0-Berichts Server verfügen, erstellen Sie einen benutzerdefinierten geplanten Task oder ein angepasstes Skript.</span><span class="sxs-lookup"><span data-stu-id="46607-234">If you have an existing App-V 5.0 reporting Server, create a customized scheduled task or script.</span></span> <span data-ttu-id="46607-235">Geben Sie an, dass der Client die Daten an den angegebenen Speicherort mit der gewünschten Häufigkeit senden soll.</span><span class="sxs-lookup"><span data-stu-id="46607-235">Specify that the client send the data to the specified location with the desired frequency.</span></span></p></td>
<td align="left"><p><span data-ttu-id="46607-236">Wenn Sie nicht über einen vorhandenen App-V 5,0-Berichts Server verfügen, verwenden Sie den <strong> URL- </strong> Parameter, um die Daten an eine bestimmte Freigabe zu senden.</span><span class="sxs-lookup"><span data-stu-id="46607-236">If you do not have an existing App-V 5.0 reporting Server, use the <strong>–URL</strong> parameter to send the data to a specified share.</span></span> <span data-ttu-id="46607-237">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="46607-237">For example:</span></span></p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p><span data-ttu-id="46607-238">Im vorherigen Beispiel werden die Berichtsdaten an <strong> \MyShare\MyData &lt; /Strong-Speicherort gesendet, der &gt; durch den <strong> -URL-Parameter angegeben wird </strong> .</span><span class="sxs-lookup"><span data-stu-id="46607-238">The previous example will send the reporting data to <strong>\MyShare\MyData&lt;/strong&gt; location indicated by the <strong>-URL</strong> parameter.</span></span> <span data-ttu-id="46607-239">Nachdem die Daten gesendet wurden, wird der Cache gelöscht.</span><span class="sxs-lookup"><span data-stu-id="46607-239">After the data has been sent, the cache is cleared.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="46607-240">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="46607-240">Note</span></span></strong><br/><p><span data-ttu-id="46607-241">Wenn ein anderer Speicherort als der Berichts Server angegeben ist, werden die Daten mithilfe des <strong> XML- </strong> Formats ohne zusätzliche Verarbeitung gesendet.</span><span class="sxs-lookup"><span data-stu-id="46607-241">If a location other than the Reporting Server is specified, the data is sent using <strong>.xml</strong> format with no additional processing.</span></span></p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="46607-242">Erstellen von Berichten</span><span class="sxs-lookup"><span data-stu-id="46607-242">Creating Reports</span></span>

<span data-ttu-id="46607-243">Sie müssen eine der folgenden Methoden verwenden, um Berichtsinformationen abzurufen und Berichte mithilfe von App-V 5,0 zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="46607-243">To retrieve report information and create reports using App-V 5.0 you must use one of the following methods:</span></span>

-   <span data-ttu-id="46607-244">**Microsoft SQL Server Reporting Services (SSRS)** – Microsoft SQL Server Reporting Services steht in Microsoft SQL Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="46607-244">**Microsoft SQL Server Reporting Services (SSRS)** - Microsoft SQL Server Reporting Services is available with Microsoft SQL Server.</span></span> <span data-ttu-id="46607-245">SSRS wird nicht installiert, wenn Sie den App-V 5,0-Berichtsserver installieren.</span><span class="sxs-lookup"><span data-stu-id="46607-245">SSRS is not installed when you install the App-V 5.0 reporting server.</span></span> <span data-ttu-id="46607-246">Sie muss separat bereitgestellt werden, um die zugehörigen Berichte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="46607-246">It must be deployed separately to generate the associated reports.</span></span>

    <span data-ttu-id="46607-247">Verwenden Sie den folgenden Link, um weitere Informationen zur Verwendung von [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="46607-247">Use the following link for more information about using [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span></span>

-   <span data-ttu-id="46607-248">**Skripting** – Sie können Berichte erstellen, indem Sie direkt mit der App-V 5,0-Berichtsdatenbank Skripting durchführen.</span><span class="sxs-lookup"><span data-stu-id="46607-248">**Scripting** – You can generate reports by scripting directly against the App-V 5.0 reporting database.</span></span> <span data-ttu-id="46607-249">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="46607-249">For example:</span></span>

    **<span data-ttu-id="46607-250">Gespeicherte Prozedur:</span><span class="sxs-lookup"><span data-stu-id="46607-250">Stored Procedure:</span></span>**

    <span data-ttu-id="46607-251">**spProcessClientReport** ist für die Ausführung um Mitternacht oder 12:00 Uhr vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="46607-251">**spProcessClientReport** is scheduled to run at midnight or 12:00 AM.</span></span>

    <span data-ttu-id="46607-252">Damit die geplante gespeicherte Prozedur Microsoft SQL Server ausgeführt werden kann, muss der Microsoft SQL Server-Agent ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="46607-252">To run the Microsoft SQL Server Scheduled Stored procedure, the Microsoft SQL Server Agent must be running.</span></span> <span data-ttu-id="46607-253">Stellen Sie sicher, dass der Microsoft SQL Server-Agent auf **Autostart**fest eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="46607-253">You should ensure that the Microsoft SQL Server Agent is set to **AutoStart**.</span></span> <span data-ttu-id="46607-254">Weitere Informationen finden Sie unter [Autostart-SQL Server-Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span><span class="sxs-lookup"><span data-stu-id="46607-254">For more information see [Autostart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span></span>

    <span data-ttu-id="46607-255">Die gespeicherte Prozedur wird auch bei Verwendung der App-V 5,0-Datenbankskripts erstellt.</span><span class="sxs-lookup"><span data-stu-id="46607-255">The stored procedure is also created when using the App-V 5.0 database scripts.</span></span>

<span data-ttu-id="46607-256">Darüber hinaus sollten Sie sicherstellen, dass die **Maximale Anzahl gleichzeitiger Verbindungen** des Reporting Server-Webdiensts auf einen Wert festgesetzt ist, der vom Server verwaltet werden kann, ohne dass die Verfügbarkeit beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="46607-256">You should also ensure that the reporting server web service’s **Maximum Concurrent Connections** is set to a value that the server will be able to manage without impacting availability.</span></span> <span data-ttu-id="46607-257">Die empfohlene Anzahl der **maximalen gleichzeitigen Verbindungen** für den **Reporting Web Service** lautet **10.000**.</span><span class="sxs-lookup"><span data-stu-id="46607-257">The recommended number of **Maximum Concurrent Connections** for the **Reporting Web Service** is **10,000**.</span></span>






## <span data-ttu-id="46607-258">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="46607-258">Related topics</span></span>


[<span data-ttu-id="46607-259">Bereitstellen des App-V 5.0-Servers</span><span class="sxs-lookup"><span data-stu-id="46607-259">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

[<span data-ttu-id="46607-260">So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank</span><span class="sxs-lookup"><span data-stu-id="46607-260">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

 

 





