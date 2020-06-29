---
title: Informationen zur App-V 5.1-Berichterstellung
description: Informationen zur App-V 5.1-Berichterstellung
author: dansimp
ms.assetid: 385dca00-7178-4e35-8d86-c58867ebd65c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 827343d538238ca638b57a74ae5d2d74bc6c5968
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806112"
---
# <span data-ttu-id="1aadf-103">Informationen zur App-V 5.1-Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="1aadf-103">About App-V 5.1 Reporting</span></span>

<span data-ttu-id="1aadf-104">Microsoft Application Virtualization (app-v) 5,1 enthält ein integriertes Berichterstattungsfeature, mit dem Sie Informationen zu Computern sammeln können, auf denen der APP-v 5,1-Client ausgeführt wird, sowie Informationen zur Verwendung des virtuellen Anwendungspakets.</span><span class="sxs-lookup"><span data-stu-id="1aadf-104">Microsoft Application Virtualization (App-V) 5.1 includes a built-in reporting feature that helps you collect information about computers running the App-V 5.1 client as well as information about virtual application package usage.</span></span> <span data-ttu-id="1aadf-105">Sie können diese Informationen verwenden, um Berichte aus einer zentralisierten Datenbank zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1aadf-105">You can use this information to generate reports from a centralized database.</span></span>

## <a href="" id="---------app-v-5-1-reporting-overview"></a> <span data-ttu-id="1aadf-106">App-V 5,1-Berichtsübersicht</span><span class="sxs-lookup"><span data-stu-id="1aadf-106">App-V 5.1 Reporting Overview</span></span>

<span data-ttu-id="1aadf-107">In der folgenden Liste wird der End-to-End-Workflow auf hoher Ebene für die Berichterstellung in App-V 5,1 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1aadf-107">The following list displays the end–to-end high-level workflow for reporting in App-V 5.1.</span></span>

1. <span data-ttu-id="1aadf-108">Der App-V 5,1-Berichtsserver verfügt über die folgenden Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="1aadf-108">The App-V 5.1 Reporting server has the following prerequisites:</span></span>

    - <span data-ttu-id="1aadf-109">IIS-Webserverrolle (Internet Informationsdienst)</span><span class="sxs-lookup"><span data-stu-id="1aadf-109">Internet Information Service (IIS) web server role</span></span>

    - <span data-ttu-id="1aadf-110">Windows-authentifizierungsrolle (unter **IIS/Sicherheit**)</span><span class="sxs-lookup"><span data-stu-id="1aadf-110">Windows Authentication role (under **IIS / Security**)</span></span>

    - <span data-ttu-id="1aadf-111">SQL Server-Installation und-Ausführung mit SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="1aadf-111">SQL Server installed and running with SQL Server Reporting Services (SSRS)</span></span>

    <span data-ttu-id="1aadf-112">Um zu bestätigen, dass SQL Server Reporting Services ausgeführt wird, zeigen Sie `http://localhost/Reports` in einem Webbrowser als Administrator auf dem Server an, auf dem die App-V 5,1-Berichterstellung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="1aadf-112">To confirm SQL Server Reporting Services is running, view `http://localhost/Reports` in a web browser as administrator on the server that will host App-V 5.1 Reporting.</span></span> <span data-ttu-id="1aadf-113">Die SQL Server Reporting Services-Startseite sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1aadf-113">The SQL Server Reporting Services Home page should display.</span></span>

2. <span data-ttu-id="1aadf-114">Installieren Sie den App-V 5,1-Berichtsserver und die zugehörige Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1aadf-114">Install the App-V 5.1 reporting server and associated database.</span></span> <span data-ttu-id="1aadf-115">Weitere Informationen zum Installieren des Berichtsservers finden Sie unter [so wird es gemacht: Installieren des Berichtsservers auf einem eigenständigen Computer und Herstellen einer Verbindung mit der Datenbank](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md).</span><span class="sxs-lookup"><span data-stu-id="1aadf-115">For more information about installing the reporting server see [How to install the Reporting Server on a Standalone Computer and Connect it to the Database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md).</span></span> <span data-ttu-id="1aadf-116">Konfigurieren Sie den Zeitpunkt, zu dem der Computer, auf dem der App-V 5,1-Client ausgeführt wird, Daten an den Berichtsserver senden soll.</span><span class="sxs-lookup"><span data-stu-id="1aadf-116">Configure the time when the computer running the App-V 5.1 client should send data to the reporting server.</span></span>

3. <span data-ttu-id="1aadf-117">Wenn Sie kein elektronisches Softwareverteilungssystem wie Configuration Manager zum Anzeigen von Berichten verwenden, können Sie Berichte im SQL Server-Berichterstattungsdienst definieren.</span><span class="sxs-lookup"><span data-stu-id="1aadf-117">If you are not using an electronic software distribution system such as Configuration Manager to view reports then you can define reports in SQL Server Reporting Service.</span></span> <span data-ttu-id="1aadf-118">Laden Sie vordefinierte SSRS-Berichte aus dem [Download Center](https://go.microsoft.com/fwlink/?LinkId=397255)herunter.</span><span class="sxs-lookup"><span data-stu-id="1aadf-118">Download predefined SSRS Reports from the [Download Center](https://go.microsoft.com/fwlink/?LinkId=397255).</span></span>

    > [!NOTE]
    > <span data-ttu-id="1aadf-119">Wenn Sie die Configuration Manager-Integration in App-v 5,1 verwenden, werden die meisten Berichte vom Configuration Manager und nicht von App-v 5,1 generiert.</span><span class="sxs-lookup"><span data-stu-id="1aadf-119">If you are using the Configuration Manager integration with App-V 5.1, most reports are generated from Configuration Manager rather than from App-V 5.1.</span></span>

4. <span data-ttu-id="1aadf-120">Nachdem Sie das App-v 5,1 PowerShell-Modul mit `Import-Module AppvClient` als Administrator importiert haben, aktivieren Sie den App-v 5,1-Client.</span><span class="sxs-lookup"><span data-stu-id="1aadf-120">After importing the App-V 5.1 PowerShell module using `Import-Module AppvClient` as administrator, enable the App-V 5.1 client.</span></span> <span data-ttu-id="1aadf-121">Dieses PowerShell-Beispiel-Cmdlet ermöglicht die App-V 5,1-Berichterstellung:</span><span class="sxs-lookup"><span data-stu-id="1aadf-121">This sample PowerShell cmdlet enables App-V 5.1 reporting:</span></span>

    ```powershell
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    <span data-ttu-id="1aadf-122">Wenn Sie App-v 5,1-Berichtsdaten sofort senden möchten, führen Sie `Send-AppvClientReport` den App-v 5,1-Client aus.</span><span class="sxs-lookup"><span data-stu-id="1aadf-122">To immediately send App-V 5.1 report data, run `Send-AppvClientReport` on the App-V 5.1 client.</span></span>

    <span data-ttu-id="1aadf-123">Weitere Informationen zum Installieren des App-V 5,1-Clients mit aktivierter Berichterstellung finden Sie unter Informationen [zu Clientkonfigurationseinstellungen](about-client-configuration-settings51.md).</span><span class="sxs-lookup"><span data-stu-id="1aadf-123">For more information about installing the App-V 5.1 client with reporting enabled see [About Client Configuration Settings](about-client-configuration-settings51.md).</span></span> <span data-ttu-id="1aadf-124">Informationen zum Verwalten von App-v 5,1-Berichten mit Windows PowerShell finden Sie unter [Aktivieren der Berichterstellung auf dem App-v 5,1-Client mithilfe von PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="1aadf-124">To administer App-V 5.1 Reporting with Windows PowerShell, see [How to Enable Reporting on the App-V 5.1 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).</span></span>

5. <span data-ttu-id="1aadf-125">Nachdem der Berichtsserver die Daten vom App-V 5,1-Client empfangen hat, sendet er die Daten an die Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1aadf-125">After the reporting server receives the data from the App-V 5.1 client it sends the data to the reporting database.</span></span> <span data-ttu-id="1aadf-126">Wenn die Datenbank die Client Daten empfängt und verarbeitet, wird eine erfolgreiche Antwort an den Berichtsserver gesendet, und dann wird eine Benachrichtigung an den App-V 5,1-Client gesendet.</span><span class="sxs-lookup"><span data-stu-id="1aadf-126">When the database receives and processes the client data, a successful reply is sent to the reporting server and then a notification is sent to the App-V 5.1 client.</span></span>

6. <span data-ttu-id="1aadf-127">Wenn der App-V 5,1-Client die Erfolgsbenachrichtigung erhält, leert er den Datencache, um Platz zu sparen.</span><span class="sxs-lookup"><span data-stu-id="1aadf-127">When the App-V 5.1 client receives the success notification, it empties the data cache to conserve space.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1aadf-128">Standardmäßig wird der Cache gelöscht, nachdem der Server den Empfang von Daten bestätigt hat.</span><span class="sxs-lookup"><span data-stu-id="1aadf-128">By default the cache is cleared after the server confirms receipt of data.</span></span> <span data-ttu-id="1aadf-129">Sie können den Client manuell konfigurieren, um den Datencache zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1aadf-129">You can manually configure the client to save the data cache.</span></span>

<span data-ttu-id="1aadf-130">Wenn das App-V 5,1-Clientgerät keine Erfolgsbenachrichtigung vom Server erhält, behält es Daten im Cache bei und versucht, Daten beim nächsten konfigurierten Intervall erneut zu senden.</span><span class="sxs-lookup"><span data-stu-id="1aadf-130">If the App-V 5.1 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval.</span></span> <span data-ttu-id="1aadf-131">Clients sammeln weiterhin Daten und fügen Sie dem Cache hinzu.</span><span class="sxs-lookup"><span data-stu-id="1aadf-131">Clients continue to collect data and add it to the cache.</span></span>

### <a href="" id="-------------app-v-5-1-reporting-server-frequently-asked-questions"></a> <span data-ttu-id="1aadf-132">App-V 5,1 Reporting Server – häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="1aadf-132">App-V 5.1 reporting server frequently asked questions</span></span>

<span data-ttu-id="1aadf-133">In der folgenden Tabelle werden Antworten auf häufig gestellte Fragen zu App-V 5,1-Berichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1aadf-133">The following table displays answers to common questions about App-V 5.1 reporting</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1aadf-134">Frage</span><span class="sxs-lookup"><span data-stu-id="1aadf-134">Question</span></span></th>
<th align="left"><span data-ttu-id="1aadf-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1aadf-135">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1aadf-136">Was ist die Häufigkeit, mit der Berichtsinformationen an die Berichtsdatenbank gesendet werden?</span><span class="sxs-lookup"><span data-stu-id="1aadf-136">What is the frequency that reporting information is sent to the reporting database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="1aadf-137">Die Häufigkeit hängt davon ab, wie die Berichterstattungs Aufgabe auf dem Computer konfiguriert ist, auf dem der App-V 5,1-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1aadf-137">The frequency depends on how the reporting task is configured on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="1aadf-138">Sie müssen die Häufigkeit/das Intervall für das Senden der Berichtsdaten konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1aadf-138">You must configure the frequency / interval for sending the reporting data.</span></span> <span data-ttu-id="1aadf-139">App-V 5,1-Berichterstattung ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1aadf-139">App-V 5.1 Reporting is not enabled by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1aadf-140">Welche Informationen werden in der Berichtsserver-Datenbank gespeichert?</span><span class="sxs-lookup"><span data-stu-id="1aadf-140">What information is stored in the reporting server database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="1aadf-141">In der folgenden Liste wird angezeigt, was in der Berichtsdatenbank gespeichert ist:</span><span class="sxs-lookup"><span data-stu-id="1aadf-141">The following list displays what is stored in the reporting database:</span></span></p>
<ul>
<li><p><span data-ttu-id="1aadf-142">Das Betriebssystem, das auf dem Computer ausgeführt wird, auf dem der App-V 5,1-Client ausgeführt wird: Hostname, Version, Service Pack, Typ-Client/Server, Prozessorarchitektur.</span><span class="sxs-lookup"><span data-stu-id="1aadf-142">The operating system running on the computer running the App-V 5.1 client: host name, version, service pack, type - client/server, processor architecture.</span></span></p></li>
<li><p><span data-ttu-id="1aadf-143">App-V 5,1-Client Informationen: Version.</span><span class="sxs-lookup"><span data-stu-id="1aadf-143">App-V 5.1 Client information: version.</span></span></p></li>
<li><p><span data-ttu-id="1aadf-144">Liste der veröffentlichten Pakete: GUID, Versions-GUID, Name.</span><span class="sxs-lookup"><span data-stu-id="1aadf-144">Published package list: GUID, version GUID, name.</span></span></p></li>
<li><p><span data-ttu-id="1aadf-145">Anwendungs Nutzungsinformationen: Name, Version, Streamingserver, Benutzer (DOMAIN\alias), paketversions-GUID, Startstatus und-Zeit, Shutdown-Zeit.</span><span class="sxs-lookup"><span data-stu-id="1aadf-145">Application usage information: name, version, streaming server, user (domain\alias), package version GUID, launch status and time, shutdown time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1aadf-146">Wie lauten die durchschnittlichen Datenmengen, die an den Berichtsserver gesendet werden?</span><span class="sxs-lookup"><span data-stu-id="1aadf-146">What is the average volume of information that is sent to the reporting server?</span></span></p></td>
<td align="left"><p><span data-ttu-id="1aadf-147">Das hängt davon ab.</span><span class="sxs-lookup"><span data-stu-id="1aadf-147">It depends.</span></span> <span data-ttu-id="1aadf-148">In der folgenden Liste werden die drei Sätze der an den Berichtsserver gesendeten Daten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="1aadf-148">The following list displays the three sets of the data sent to the reporting server:</span></span></p>
<ol>
<li><p><span data-ttu-id="1aadf-149">Betriebssystem-und App-V 5,1-Clientinformationen.</span><span class="sxs-lookup"><span data-stu-id="1aadf-149">Operating system, and App-V 5.1 client information.</span></span> <span data-ttu-id="1aadf-150">~ 150 Bytes, jedes Mal, wenn diese Daten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="1aadf-150">~150 Bytes, every time this data is sent.</span></span></p></li>
<li><p><span data-ttu-id="1aadf-151">Liste der veröffentlichten Pakete</span><span class="sxs-lookup"><span data-stu-id="1aadf-151">Published package list.</span></span> <span data-ttu-id="1aadf-152">~ 7 KB für 30 Pakete.</span><span class="sxs-lookup"><span data-stu-id="1aadf-152">~7 KB for 30 packages.</span></span> <span data-ttu-id="1aadf-153">Diese wird nur gesendet, wenn die Paketliste mit einer Veröffentlichungsaktualisierung aktualisiert wird, die selten erfolgt; Wenn keine Änderung erfolgt, werden diese Informationen nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="1aadf-153">This is sent only when the package list is updated with a publishing refresh, which is done infrequently; if there is no change, this information is not sent.</span></span></p></li>
<li><p><span data-ttu-id="1aadf-154">Informationen zur Verwendung virtueller Anwendungen – ungefähr 0,25 KB pro Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1aadf-154">Virtual application usage information – about 0.25KB per event.</span></span> <span data-ttu-id="1aadf-155">Öffnen und schließen zählen als ein Ereignis, wenn beide vor dem Senden der Informationen auftreten.</span><span class="sxs-lookup"><span data-stu-id="1aadf-155">Opening and closing count as one event if both occur before sending the information.</span></span> <span data-ttu-id="1aadf-156">Beim Senden mit einer geplanten Aufgabe werden nur die Daten seit dem letzten erfolgreichen Upload an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="1aadf-156">When sending using a scheduled task, only the data since the last successful upload is sent to the server.</span></span> <span data-ttu-id="1aadf-157">Wenn Sie manuell über das PowerShell-Cmdlet senden, gibt es ein optionales Argument, das steuert, ob die Daten beim nächsten Mal erneut gesendet werden müssen – dieses Argument ist <strong> DeleteOnSuccess </strong> .</span><span class="sxs-lookup"><span data-stu-id="1aadf-157">If sending manually through the PowerShell cmdlet, there is an optional argument that controls if the data needs to be re-sent next time around – that argument is <strong>DeleteOnSuccess</strong>.</span></span></p>
<p></p>
<p><span data-ttu-id="1aadf-158">Wenn beispielsweise zwanzig Anwendungen geöffnet und geschlossen sind und die Berichtsinformationen täglich gesendet werden sollen, sollte der typische tägliche Datenverkehr etwa 0.15 KB + 20 x 0,25 KB oder über 5KB/Benutzer sein.</span><span class="sxs-lookup"><span data-stu-id="1aadf-158">So for example, if twenty applications are opened and closed and reporting information is scheduled to be sent daily, the typical daily traffic should be about 0.15KB + 20 x 0.25KB, or about 5KB/user</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1aadf-159">Können Berichte geplant werden?</span><span class="sxs-lookup"><span data-stu-id="1aadf-159">Can reporting be scheduled?</span></span></p></td>
<td align="left"><p><span data-ttu-id="1aadf-160">Ja.</span><span class="sxs-lookup"><span data-stu-id="1aadf-160">Yes.</span></span> <span data-ttu-id="1aadf-161">Neben dem manuellen Senden von Berichten mithilfe von PowerShell-Cmdlets ( <strong> Send-AppvClientReport </strong> ) kann die Aufgabe so geplant werden, dass Sie automatisch erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1aadf-161">Besides manually sending reporting using PowerShell Cmdlets (<strong>Send-AppvClientReport</strong>), the task can be scheduled so it will happen automatically.</span></span> <span data-ttu-id="1aadf-162">Es gibt zwei Möglichkeiten, die Berichterstellung zu planen:</span><span class="sxs-lookup"><span data-stu-id="1aadf-162">There are two ways to schedule the reporting:</span></span></p>
<ol>
<li><p><span data-ttu-id="1aadf-163">Verwenden von PowerShell-Cmdlets- <strong> AppvClientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="1aadf-163">Using PowerShell cmdlets - <strong>Set-AppvClientConfiguration</strong>.</span></span> <span data-ttu-id="1aadf-164">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1aadf-164">For example:</span></span></p>
<p><span data-ttu-id="1aadf-165">Satz-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span><span class="sxs-lookup"><span data-stu-id="1aadf-165">Set-AppvClientConfiguration -ReportingEnabled 1 - ReportingServerURL <a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span></span></a></p>
<p></p>
<p><span data-ttu-id="1aadf-166">Eine vollständige Liste der Clientkonfigurationseinstellungen finden Sie unter <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)"> Informationen zu Clientkonfigurationseinstellungen, </a> und suchen Sie nach den folgenden Einträgen: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay </strong> , <strong> ReportingInterval </strong> .</span><span class="sxs-lookup"><span data-stu-id="1aadf-166">For a complete list of client configuration settings see <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)">About Client Configuration Settings</a> and look for the following entries: <strong>ReportingEnabled</strong>, <strong>ReportingServerURL</strong>, <strong>ReportingDataCacheLimit</strong>, <strong>ReportingDataBlockSize</strong>, <strong>ReportingStartTime</strong>, <strong>ReportingRandomDelay</strong>, <strong>ReportingInterval</strong>.</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="1aadf-167">Mithilfe von Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="1aadf-167">By using Group Policy.</span></span> <span data-ttu-id="1aadf-168">Bei einer Verteilung mithilfe des Domänencontrollers sind die Einstellungen mit den zuvor aufgelisteten identisch.</span><span class="sxs-lookup"><span data-stu-id="1aadf-168">If distributed using the domain controller, the settings are the same as previously listed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1aadf-169">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1aadf-169">Note</span></span></strong><br/><p><span data-ttu-id="1aadf-170">Die Gruppenrichtlinieneinstellungen überschreiben die mit PowerShell konfigurierten lokalen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="1aadf-170">Group Policy settings override local settings configured using PowerShell.</span></span></p>
</div>
<div>
</div></li>
</ol></td>
</tr>
</tbody>
</table>

## <a href="" id="---------app-v-5-1-client-reporting"></a> <span data-ttu-id="1aadf-171">App-V 5,1-Client Berichte</span><span class="sxs-lookup"><span data-stu-id="1aadf-171">App-V 5.1 Client Reporting</span></span>

<span data-ttu-id="1aadf-172">Wenn Sie die APP-v 5,1-Berichterstellung verwenden möchten, müssen Sie den App-v 5,1-Client installieren und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1aadf-172">To use App-V 5.1 reporting you must install and configure the App-V 5.1 client.</span></span> <span data-ttu-id="1aadf-173">Nachdem der Client installiert wurde, verwenden Sie das PowerShell-Cmdlet " **festlegen-AppVClientConfiguration** " oder die **ADMX-Vorlage** , um die Berichterstellung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1aadf-173">After the client has been installed, use the **Set-AppVClientConfiguration** PowerShell cmdlet or the **ADMX Template** to configure reporting.</span></span> <span data-ttu-id="1aadf-174">Die Cmdlets für das Berichterstattungsfeature sind über den folgenden Link verfügbar und werden durch die **Berichterstellung**vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="1aadf-174">The reporting feature cmdlets are available by using the following link and are prefaced by **Reporting**.</span></span> <span data-ttu-id="1aadf-175">Eine vollständige Liste der Clientkonfigurationseinstellungen finden Sie unter [Informationen zu Clientkonfigurationseinstellungen](about-client-configuration-settings51.md).</span><span class="sxs-lookup"><span data-stu-id="1aadf-175">For a complete list of client configuration settings see [About Client Configuration Settings](about-client-configuration-settings51.md).</span></span> <span data-ttu-id="1aadf-176">Der folgende Abschnitt enthält Beispiele für die Konfiguration der App-V 5,1-Client Berichterstattung mithilfe von PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1aadf-176">The following section provides examples of App-V 5.1 client reporting configuration using PowerShell.</span></span>

### <span data-ttu-id="1aadf-177">Konfigurieren von App-V-Client Berichten mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="1aadf-177">Configuring App-V Client reporting using PowerShell</span></span>

<span data-ttu-id="1aadf-178">Die folgenden Beispiele zeigen, wie PowerShell-Parameter die Berichterstattungsfeatures des App-V 5,1-Clients konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="1aadf-178">The following examples show how PowerShell parameters can configure the reporting features of the App-V 5.1 client.</span></span>

> [!NOTE]
> <span data-ttu-id="1aadf-179">Die folgende Konfigurationsaufgabe kann auch mithilfe von Gruppenrichtlinieneinstellungen in der App-V 5,1 ADMX-Vorlage konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="1aadf-179">The following configuration task can also be configured using Group Policy settings in the App-V 5.1 ADMX template.</span></span> <span data-ttu-id="1aadf-180">Weitere Informationen zur Verwendung der ADMX-Vorlage finden Sie unter [Ändern der App-V 5,1-Client Konfiguration mithilfe der ADMX-Vorlage und der Gruppenrichtlinie](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).</span><span class="sxs-lookup"><span data-stu-id="1aadf-180">For more information about using the ADMX template, see [How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).</span></span>

<span data-ttu-id="1aadf-181">**So aktivieren Sie die Berichterstellung und initiieren die Datensammlung auf dem Computer, auf dem der App-V 5,1-Client ausgeführt wird**:</span><span class="sxs-lookup"><span data-stu-id="1aadf-181">**To enable reporting and to initiate data collection on the computer running the App-V 5.1 client**:</span></span>

```powershell
Set-AppVClientConfiguration –ReportingEnabled 1
```

<span data-ttu-id="1aadf-182">**So konfigurieren Sie den Client so, dass Daten automatisch an einen bestimmten Berichtsserver gesendet**werden:</span><span class="sxs-lookup"><span data-stu-id="1aadf-182">**To configure the client to automatically send data to a specific reporting server**:</span></span>

```powershell
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30 -ReportingInterval 1 -ReportingRandomDelay 30
```

<span data-ttu-id="1aadf-183">In diesem Beispiel wird der Client so konfiguriert, dass die Berichtsdaten automatisch an die Berichtsserver-URL gesendet werden **http://MyReportingServer:MyPort/** .</span><span class="sxs-lookup"><span data-stu-id="1aadf-183">This example configures the client to automatically send the reporting data to the reporting server URL **http://MyReportingServer:MyPort/**.</span></span> <span data-ttu-id="1aadf-184">Darüber hinaus werden die Berichterstellungsdaten täglich zwischen 8:00 und 8:30 Uhr gesendet, abhängig von der Zufalls Verzögerung, die für die Sitzung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1aadf-184">Additionally, the reporting data will be sent daily between 8:00 and 8:30 PM, depending on the random delay generated for the session.</span></span>

<span data-ttu-id="1aadf-185">**So begrenzen Sie die Größe des Datencaches auf dem Client**:</span><span class="sxs-lookup"><span data-stu-id="1aadf-185">**To limit the size of the data cache on the client**:</span></span>

```powershell
Set-AppvClientConfiguration –ReportingDataCacheLimit 100
```

<span data-ttu-id="1aadf-186">Konfiguriert die maximale Größe des Berichtscaches auf dem Computer, auf dem der App-V 5,1-Client ausgeführt wird, auf 100 MB.</span><span class="sxs-lookup"><span data-stu-id="1aadf-186">Configures the maximum size of the reporting cache on the computer running the App-V 5.1 client to 100 MB.</span></span> <span data-ttu-id="1aadf-187">Wenn die Cache Grenze erreicht ist, bevor die Daten an den Server gesendet werden, wird das Protokoll überschrieben, und die Daten werden nach Bedarf überschrieben.</span><span class="sxs-lookup"><span data-stu-id="1aadf-187">If the cache limit is reached before the data is sent to the server, then the log rolls over and data will be overwritten as necessary.</span></span>

<span data-ttu-id="1aadf-188">**So konfigurieren Sie die Datenblockgröße, die über das Netzwerk zwischen dem Client und dem Server übertragen wird**:</span><span class="sxs-lookup"><span data-stu-id="1aadf-188">**To configure the data block size transmitted across the network between the client and the server**:</span></span>

```powershell
Set-AppvClientConfiguration –ReportingDataBlockSize 10240
```

<span data-ttu-id="1aadf-189">Gibt den maximalen Datenblock an, der vom Client an 10240 MB gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1aadf-189">Specifies the maximum data block that the client sends to 10240 MB.</span></span>

### <span data-ttu-id="1aadf-190">Gesammelte Datentypen</span><span class="sxs-lookup"><span data-stu-id="1aadf-190">Types of data collected</span></span>

<span data-ttu-id="1aadf-191">In der folgenden Tabelle sind die Informationstypen aufgeführt, die Sie mithilfe der App-V 5,1-Berichterstellung erfassen können.</span><span class="sxs-lookup"><span data-stu-id="1aadf-191">The following table displays the types of information you can collect by using App-V 5.1 reporting.</span></span>

|<span data-ttu-id="1aadf-192">Client Informationen</span><span class="sxs-lookup"><span data-stu-id="1aadf-192">Client Information</span></span>  |<span data-ttu-id="1aadf-193">Paketinformationen</span><span class="sxs-lookup"><span data-stu-id="1aadf-193">Package Information</span></span>  |<span data-ttu-id="1aadf-194">Anwendungsverwendung</span><span class="sxs-lookup"><span data-stu-id="1aadf-194">Application Usage</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="1aadf-195">Hostname</span><span class="sxs-lookup"><span data-stu-id="1aadf-195">Host Name</span></span> |<span data-ttu-id="1aadf-196">Paket Name</span><span class="sxs-lookup"><span data-stu-id="1aadf-196">Package Name</span></span>|<span data-ttu-id="1aadf-197">Anfangs-und Endzeit</span><span class="sxs-lookup"><span data-stu-id="1aadf-197">Start and End Times</span></span>|
|<span data-ttu-id="1aadf-198">App-V 5,1-Client Version</span><span class="sxs-lookup"><span data-stu-id="1aadf-198">App-V 5.1 Client Version</span></span> |<span data-ttu-id="1aadf-199">Paket Version</span><span class="sxs-lookup"><span data-stu-id="1aadf-199">Package Version</span></span>|<span data-ttu-id="1aadf-200">Ausführungs Status</span><span class="sxs-lookup"><span data-stu-id="1aadf-200">Run Status</span></span>|
|<span data-ttu-id="1aadf-201">Prozessorarchitektur</span><span class="sxs-lookup"><span data-stu-id="1aadf-201">Processor Architecture</span></span> |<span data-ttu-id="1aadf-202">Paketquelle</span><span class="sxs-lookup"><span data-stu-id="1aadf-202">Package Source</span></span>|<span data-ttu-id="1aadf-203">Shutdown-Status</span><span class="sxs-lookup"><span data-stu-id="1aadf-203">Shutdown State</span></span>|
|<span data-ttu-id="1aadf-204">Version des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="1aadf-204">Operating System Version</span></span>|<span data-ttu-id="1aadf-205">Prozent zwischengespeichert</span><span class="sxs-lookup"><span data-stu-id="1aadf-205">Percent Cached</span></span>|<span data-ttu-id="1aadf-206">Name der Anwendung</span><span class="sxs-lookup"><span data-stu-id="1aadf-206">Application Name</span></span>|
|<span data-ttu-id="1aadf-207">Service Pack-Ebene</span><span class="sxs-lookup"><span data-stu-id="1aadf-207">Service Pack Level</span></span>| |<span data-ttu-id="1aadf-208">Anwendungs Version</span><span class="sxs-lookup"><span data-stu-id="1aadf-208">Application Version</span></span>|
|<span data-ttu-id="1aadf-209">Typ des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="1aadf-209">Operating System Type</span></span>| |<span data-ttu-id="1aadf-210">Benutzername</span><span class="sxs-lookup"><span data-stu-id="1aadf-210">Username</span></span>|
| | |<span data-ttu-id="1aadf-211">Verbindungsgruppe</span><span class="sxs-lookup"><span data-stu-id="1aadf-211">Connection Group</span></span>|

<span data-ttu-id="1aadf-212">Der Client sammelt und speichert diese Daten im **XML-** Format.</span><span class="sxs-lookup"><span data-stu-id="1aadf-212">The client collects and saves this data in an **.xml** format.</span></span> <span data-ttu-id="1aadf-213">Der Datencache ist standardmäßig ausgeblendet und erfordert Administratorrechte, um die XML-Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1aadf-213">The data cache is hidden by default and requires administrator rights to open the XML file.</span></span>

### <span data-ttu-id="1aadf-214">Senden von Daten an den Server</span><span class="sxs-lookup"><span data-stu-id="1aadf-214">Sending data to the server</span></span>

<span data-ttu-id="1aadf-215">Sie können den Computer, auf dem der App-V 5,1-Client ausgeführt wird, so konfigurieren, dass Daten automatisch an den angegebenen Berichtsserver gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="1aadf-215">You can configure the computer that is running the App-V 5.1 client to automatically send data to the specified reporting server.</span></span> <span data-ttu-id="1aadf-216">Wenn Sie den Server angeben möchten, verwenden Sie das Cmdlet " **festlegen-AppvClientConfiguration** " mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="1aadf-216">To specify the server use the **Set-AppvClientConfiguration** cmdlet with the following settings:</span></span>

- <span data-ttu-id="1aadf-217">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="1aadf-217">ReportingEnabled</span></span>
- <span data-ttu-id="1aadf-218">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="1aadf-218">ReportingServerURL</span></span>
- <span data-ttu-id="1aadf-219">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="1aadf-219">ReportingStartTime</span></span>
- <span data-ttu-id="1aadf-220">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="1aadf-220">ReportingInterval</span></span>
- <span data-ttu-id="1aadf-221">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="1aadf-221">ReportingRandomDelay</span></span>

<span data-ttu-id="1aadf-222">Nachdem Sie die vorherigen Einstellungen konfiguriert haben, müssen Sie einen geplanten Vorgang erstellen.</span><span class="sxs-lookup"><span data-stu-id="1aadf-222">After you configure the previous settings, you must create a scheduled task.</span></span> <span data-ttu-id="1aadf-223">Der geplante Task setzt sich mit dem Server in Verbindung, der durch die **ReportingServerURL** -Einstellung angegeben wird, und initiiert die Übertragung.</span><span class="sxs-lookup"><span data-stu-id="1aadf-223">The scheduled task will contact the server specified by the **ReportingServerURL** setting and will initiate the transfer.</span></span> <span data-ttu-id="1aadf-224">Wenn Sie Daten manuell außerhalb der geplanten Zeiten senden möchten, verwenden Sie das folgende PowerShell-Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1aadf-224">If you want to manually send data outside of the scheduled times, use the following PowerShell cmdlet:</span></span>

```powershell
Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess
```

<span data-ttu-id="1aadf-225">Wenn der Berichtsserver zuvor konfiguriert wurde, kann der **URL-** Parameter ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="1aadf-225">If the reporting server has been previously configured, then the **–URL** parameter can be omitted.</span></span> <span data-ttu-id="1aadf-226">Wenn die Daten an einen anderen Speicherort gesendet werden sollen, geben Sie alternativ eine andere URL an, um die konfigurierte **ReportingServerURL** für diese Datensammlung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="1aadf-226">Alternatively, if the data should be sent to an alternate location, specify a different URL to override the configured **ReportingServerURL** for this data collection.</span></span>

<span data-ttu-id="1aadf-227">Der Parameter **-DeleteOnSuccess** gibt an, dass der Datencache gelöscht wird, wenn die Übertragung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1aadf-227">The **-DeleteOnSuccess** parameter indicates that if the transfer is successful, then the data cache is cleared.</span></span> <span data-ttu-id="1aadf-228">Wenn dies nicht angegeben ist, wird der Cache nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1aadf-228">If this is not specified, then the cache will not be cleared.</span></span>

### <span data-ttu-id="1aadf-229">Manuelle Datensammlung</span><span class="sxs-lookup"><span data-stu-id="1aadf-229">Manual Data Collection</span></span>

<span data-ttu-id="1aadf-230">Sie können auch das Cmdlet **Send-AppVClientReport** verwenden, um Daten manuell zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="1aadf-230">You can also use the **Send-AppVClientReport** cmdlet to manually collect data.</span></span> <span data-ttu-id="1aadf-231">Diese Lösung ist mit oder ohne einen vorhandenen Berichtsserver hilfreich.</span><span class="sxs-lookup"><span data-stu-id="1aadf-231">This solution is helpful with or without an existing reporting server.</span></span> <span data-ttu-id="1aadf-232">In der folgenden Liste werden Informationen zum Sammeln von Daten mit oder ohne Berichtsserver angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1aadf-232">The following list displays information about collecting data with or without a reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1aadf-233">Mit einem Berichts Server</span><span class="sxs-lookup"><span data-stu-id="1aadf-233">With a Reporting Server</span></span></th>
<th align="left"><span data-ttu-id="1aadf-234">Ohne einen Berichts Server</span><span class="sxs-lookup"><span data-stu-id="1aadf-234">Without a Reporting Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1aadf-235">Wenn Sie über einen vorhandenen App-V 5,1-Berichts Server verfügen, erstellen Sie einen benutzerdefinierten geplanten Task oder ein angepasstes Skript.</span><span class="sxs-lookup"><span data-stu-id="1aadf-235">If you have an existing App-V 5.1 reporting Server, create a customized scheduled task or script.</span></span> <span data-ttu-id="1aadf-236">Geben Sie an, dass der Client die Daten an den angegebenen Speicherort mit der gewünschten Häufigkeit senden soll.</span><span class="sxs-lookup"><span data-stu-id="1aadf-236">Specify that the client send the data to the specified location with the desired frequency.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1aadf-237">Wenn Sie nicht über einen vorhandenen App-V 5,1-Berichts Server verfügen, verwenden Sie den <strong> URL- </strong> Parameter, um die Daten an eine bestimmte Freigabe zu senden.</span><span class="sxs-lookup"><span data-stu-id="1aadf-237">If you do not have an existing App-V 5.1 reporting Server, use the <strong>–URL</strong> parameter to send the data to a specified share.</span></span> <span data-ttu-id="1aadf-238">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1aadf-238">For example:</span></span></p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p><span data-ttu-id="1aadf-239">Im vorherigen Beispiel werden die Berichtsdaten an <strong> \MyShare\MyData &lt; /Strong-Speicherort gesendet, der &gt; durch den <strong> -URL-Parameter angegeben wird </strong> .</span><span class="sxs-lookup"><span data-stu-id="1aadf-239">The previous example will send the reporting data to <strong>\MyShare\MyData&lt;/strong&gt; location indicated by the <strong>-URL</strong> parameter.</span></span> <span data-ttu-id="1aadf-240">Nachdem die Daten gesendet wurden, wird der Cache gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1aadf-240">After the data has been sent, the cache is cleared.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1aadf-241">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1aadf-241">Note</span></span></strong><br/><p><span data-ttu-id="1aadf-242">Wenn ein anderer Speicherort als der Berichts Server angegeben ist, werden die Daten mithilfe des <strong> XML- </strong> Formats ohne zusätzliche Verarbeitung gesendet.</span><span class="sxs-lookup"><span data-stu-id="1aadf-242">If a location other than the Reporting Server is specified, the data is sent using <strong>.xml</strong> format with no additional processing.</span></span></p>
</div>
<div>
</div></td>
</tr>
</tbody>
</table>

### <span data-ttu-id="1aadf-243">Erstellen von Berichten</span><span class="sxs-lookup"><span data-stu-id="1aadf-243">Creating Reports</span></span>

<span data-ttu-id="1aadf-244">Sie müssen eine der folgenden Methoden verwenden, um Berichtsinformationen abzurufen und Berichte mithilfe von App-V 5,1 zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="1aadf-244">To retrieve report information and create reports using App-V 5.1 you must use one of the following methods:</span></span>

- <span data-ttu-id="1aadf-245">**Microsoft SQL Server Reporting Services (SSRS)** – Microsoft SQL Server Reporting Services steht in Microsoft SQL Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1aadf-245">**Microsoft SQL Server Reporting Services (SSRS)** - Microsoft SQL Server Reporting Services is available with Microsoft SQL Server.</span></span> <span data-ttu-id="1aadf-246">SSRS wird nicht installiert, wenn Sie den App-V 5,1-Berichtsserver installieren.</span><span class="sxs-lookup"><span data-stu-id="1aadf-246">SSRS is not installed when you install the App-V 5.1 reporting server.</span></span> <span data-ttu-id="1aadf-247">Sie muss separat bereitgestellt werden, um die zugehörigen Berichte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1aadf-247">It must be deployed separately to generate the associated reports.</span></span>

    <span data-ttu-id="1aadf-248">Verwenden Sie den folgenden Link, um weitere Informationen zur Verwendung von [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1aadf-248">Use the following link for more information about using [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span></span>

- <span data-ttu-id="1aadf-249">**Skripting** – Sie können Berichte erstellen, indem Sie direkt mit der App-V 5,1-Berichtsdatenbank Skripting durchführen.</span><span class="sxs-lookup"><span data-stu-id="1aadf-249">**Scripting** – You can generate reports by scripting directly against the App-V 5.1 reporting database.</span></span> <span data-ttu-id="1aadf-250">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1aadf-250">For example:</span></span>

    **<span data-ttu-id="1aadf-251">Gespeicherte Prozedur:</span><span class="sxs-lookup"><span data-stu-id="1aadf-251">Stored Procedure:</span></span>**

    <span data-ttu-id="1aadf-252">**spProcessClientReport** ist für die Ausführung um Mitternacht oder 12:00 Uhr vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="1aadf-252">**spProcessClientReport** is scheduled to run at midnight or 12:00 AM.</span></span>

    <span data-ttu-id="1aadf-253">Damit die geplante gespeicherte Prozedur Microsoft SQL Server ausgeführt werden kann, muss der Microsoft SQL Server-Agent ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1aadf-253">To run the Microsoft SQL Server Scheduled Stored procedure, the Microsoft SQL Server Agent must be running.</span></span> <span data-ttu-id="1aadf-254">Stellen Sie sicher, dass der Microsoft SQL Server-Agent auf **Autostart**fest eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="1aadf-254">You should ensure that the Microsoft SQL Server Agent is set to **AutoStart**.</span></span> <span data-ttu-id="1aadf-255">Weitere Informationen finden Sie unter [Autostart-SQL Server-Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span><span class="sxs-lookup"><span data-stu-id="1aadf-255">For more information see [Autostart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span></span>

    <span data-ttu-id="1aadf-256">Die gespeicherte Prozedur wird auch bei Verwendung der App-V 5,1-Datenbankskripts erstellt.</span><span class="sxs-lookup"><span data-stu-id="1aadf-256">The stored procedure is also created when using the App-V 5.1 database scripts.</span></span>

<span data-ttu-id="1aadf-257">Darüber hinaus sollten Sie sicherstellen, dass die **Maximale Anzahl gleichzeitiger Verbindungen** des Reporting Server-Webdiensts auf einen Wert festgesetzt ist, der vom Server verwaltet werden kann, ohne dass die Verfügbarkeit beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="1aadf-257">You should also ensure that the reporting server web service's **Maximum Concurrent Connections** is set to a value that the server will be able to manage without impacting availability.</span></span> <span data-ttu-id="1aadf-258">Die empfohlene Anzahl der **maximalen gleichzeitigen Verbindungen** für den **Reporting Web Service** lautet **10.000**.</span><span class="sxs-lookup"><span data-stu-id="1aadf-258">The recommended number of **Maximum Concurrent Connections** for the **Reporting Web Service** is **10,000**.</span></span>

## <span data-ttu-id="1aadf-259">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1aadf-259">Related topics</span></span>

[<span data-ttu-id="1aadf-260">Bereitstellen des App-V 5.1-Servers</span><span class="sxs-lookup"><span data-stu-id="1aadf-260">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="1aadf-261">So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank</span><span class="sxs-lookup"><span data-stu-id="1aadf-261">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)
