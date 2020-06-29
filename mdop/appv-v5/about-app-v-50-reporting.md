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
# Informationen zur App-V 5.0-Berichterstellung


Microsoft Application Virtualization (app-v) 5,0 enthält ein integriertes Berichterstattungsfeature, mit dem Sie Informationen zu Computern sammeln können, auf denen der APP-v 5,0-Client ausgeführt wird, sowie Informationen zur Verwendung des virtuellen Anwendungspakets. Sie können diese Informationen verwenden, um Berichte aus einer zentralisierten Datenbank zu generieren.

## <a href="" id="---------app-v-5-0-reporting-overview"></a> App-V 5,0-Berichtsübersicht


In der folgenden Liste wird der End-to-End-Workflow auf hoher Ebene für die Berichterstellung in App-V 5,0 angezeigt.

1.  Der Microsoft Application Virtualization (App-V) 5,0-Berichtsserver verfügt über die folgenden Voraussetzungen:

    -   IIS-Webserverrolle (Internet Informationsdienst)

    -   Windows-authentifizierungsrolle (unter **IIS/Sicherheit**)

    -   SQL Server-Installation und-Ausführung mit SQL Server Reporting Services (SSRS)

    Um zu bestätigen, dass SQL Server Reporting Services ausgeführt wird, zeigen Sie `http://localhost/Reports` in einem Webbrowser als Administrator auf dem Server an, auf dem die App-V 5,0-Berichterstellung gehostet wird. Die SQL Server Reporting Services-Startseite sollte angezeigt werden.

2.  Installieren Sie den App-V 5,0-Berichtsserver und die zugehörige Datenbank. Weitere Informationen zum Installieren des Berichtsservers finden Sie unter [so wird es gemacht: Installieren des Berichtsservers auf einem eigenständigen Computer und Herstellen einer Verbindung mit der Datenbank](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md). Konfigurieren Sie den Zeitpunkt, zu dem der Computer, auf dem der App-V 5,0-Client ausgeführt wird, Daten an den Berichtsserver senden soll.

3.  Wenn Sie kein elektronisches Softwareverteilungssystem wie Configuration Manager zum Anzeigen von Berichten verwenden, können Sie Berichte im SQL Server-Berichterstattungsdienst definieren. Laden Sie vordefinierte appvshort-Berichte aus dem Download Center unter herunter <https://go.microsoft.com/fwlink/?LinkId=397255> .

    **Hinweis**  Wenn Sie die Configuration Manager-Integration in App-v 5,0 verwenden, werden die meisten Berichte vom Configuration Manager und nicht von App-v 5,0 generiert.

     

4.  Nachdem Sie das App-v 5,0 PowerShell-Modul mit `Import-Module AppvClient` als Administrator importiert haben, aktivieren Sie den App-v 5,0-Client. Dieses PowerShell-Beispiel-Cmdlet ermöglicht die App-V 5,0-Berichterstellung:

    ``` syntax
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    Wenn Sie App-v 5,0-Berichtsdaten sofort senden möchten, führen Sie `Send-AppvClientReport` den App-v 5,0-Client aus.

    Weitere Informationen zum Installieren des App-V 5,0-Clients mit aktivierter Berichterstellung finden Sie unter Informationen [zu Clientkonfigurationseinstellungen](about-client-configuration-settings.md). Informationen zum Verwalten von App-v 5,0-Berichten mit Windows PowerShell finden Sie unter [Aktivieren der Berichterstellung auf dem App-v 5,0-Client mithilfe von PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md).

5.  Nachdem der Berichtsserver die Daten vom App-V 5,0-Client empfangen hat, sendet er die Daten an die Berichtsdatenbank. Wenn die Datenbank die Client Daten empfängt und verarbeitet, wird eine erfolgreiche Antwort an den Berichtsserver gesendet, und dann wird eine Benachrichtigung an den App-V 5,0-Client gesendet.

6.  Wenn der App-V 5,0-Client die Erfolgsbenachrichtigung erhält, leert er den Datencache, um Platz zu sparen.

    **Hinweis**  Standardmäßig wird der Cache gelöscht, nachdem der Server den Empfang von Daten bestätigt hat. Sie können den Client manuell konfigurieren, um den Datencache zu speichern.

     

~~~
If the App-V 5.0 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval. Clients continue to collect data and add it to the cache.
~~~

### <a href="" id="-------------app-v-5-0-reporting-server-frequently-asked-questions"></a> App-V 5,0 Reporting Server – häufig gestellte Fragen

In der folgenden Tabelle werden Antworten auf häufig gestellte Fragen zu App-V 5,0-Berichten angezeigt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Frage</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Was ist die Häufigkeit, mit der Berichtsinformationen an die Berichtsdatenbank gesendet werden?</p></td>
<td align="left"><p>Die Häufigkeit hängt davon ab, wie die Berichterstattungs Aufgabe auf dem Computer konfiguriert ist, auf dem der App-V 5,0-Client ausgeführt wird. Sie müssen die Häufigkeit/das Intervall für das Senden der Berichtsdaten konfigurieren. App-V 5,0-Berichterstattung ist standardmäßig nicht aktiviert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Welche Informationen werden in der Berichtsserver-Datenbank gespeichert?</p></td>
<td align="left"><p>In der folgenden Liste wird angezeigt, was in der Berichtsdatenbank gespeichert ist:</p>
<ul>
<li><p>Das Betriebssystem, das auf dem Computer ausgeführt wird, auf dem der App-V 5,0-Client ausgeführt wird: Hostname, Version, Service Pack, Typ-Client/Server, Prozessorarchitektur.</p></li>
<li><p>App-V 5,0-Client Informationen: Version.</p></li>
<li><p>Liste der veröffentlichten Pakete: GUID, Versions-GUID, Name.</p></li>
<li><p>Anwendungs Nutzungsinformationen: Name, Version, Streamingserver, Benutzer (DOMAIN\alias), paketversions-GUID, Startstatus und-Zeit, Shutdown-Zeit.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Wie lauten die durchschnittlichen Datenmengen, die an den Berichtsserver gesendet werden?</p></td>
<td align="left"><p>Das hängt davon ab. In der folgenden Liste werden die drei Sätze der an den Berichtsserver gesendeten Daten angezeigt:</p>
<ol>
<li><p>Betriebssystem-und App-V 5,0-Clientinformationen. ~ 150 Bytes, jedes Mal, wenn diese Daten gesendet werden.</p></li>
<li><p>Liste der veröffentlichten Pakete ~ 7 KB für 30 Pakete. Diese wird nur gesendet, wenn die Paketliste mit einer Veröffentlichungsaktualisierung aktualisiert wird, die selten erfolgt; Wenn keine Änderung erfolgt, werden diese Informationen nicht gesendet.</p></li>
<li><p>Informationen zur Verwendung virtueller Anwendungen – ungefähr 0,25 KB pro Ereignis. Öffnen und schließen zählen als ein Ereignis, wenn beide vor dem Senden der Informationen auftreten. Beim Senden mit einer geplanten Aufgabe werden nur die Daten seit dem letzten erfolgreichen Upload an den Server gesendet. Wenn Sie manuell über das PowerShell-Cmdlet senden, gibt es ein optionales Argument, das steuert, ob die Daten beim nächsten Mal erneut gesendet werden müssen – dieses Argument ist <strong> DeleteOnSuccess </strong> .</p>
<p></p>
<p>Wenn beispielsweise zwanzig Anwendungen geöffnet und geschlossen sind und die Berichtsinformationen täglich gesendet werden sollen, sollte der typische tägliche Datenverkehr etwa 0.15 KB + 20 x 0,25 KB oder über 5KB/Benutzer sein.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Können Berichte geplant werden?</p></td>
<td align="left"><p>Ja. Neben dem manuellen Senden von Berichten mithilfe von PowerShell-Cmdlets ( <strong> Send-AppvClientReport </strong> ) kann die Aufgabe so geplant werden, dass Sie automatisch erfolgt. Es gibt zwei Möglichkeiten, die Berichterstellung zu planen:</p>
<ol>
<li><p>Verwenden von PowerShell-Cmdlets- <strong> AppvClientConfiguration </strong> . Beispiel:</p>
<p>Satz-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</a></p>
<p></p>
<p>Eine vollständige Liste der Clientkonfigurationseinstellungen finden Sie unter <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)"> Informationen zu Clientkonfigurationseinstellungen, </a> und suchen Sie nach den folgenden Einträgen: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay </strong> , <strong> ReportingInterval </strong> .</p>
<p></p></li>
<li><p>Mithilfe von Gruppenrichtlinien. Bei einer Verteilung mithilfe des Domänencontrollers sind die Einstellungen mit den zuvor aufgelisteten identisch.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Die Gruppenrichtlinieneinstellungen überschreiben die mit PowerShell konfigurierten lokalen Einstellungen.</p>
</div>
<div>

</div></li>
</ol></td>
</tr>
</tbody>
</table>
 


## <a href="" id="---------app-v-5-0-client-reporting"></a> App-V 5,0-Client Berichte


Wenn Sie die APP-v 5,0-Berichterstellung verwenden möchten, müssen Sie den App-v 5,0-Client installieren und konfigurieren. Nachdem der Client installiert wurde, verwenden Sie das PowerShell-Cmdlet " **festlegen-AppVClientConfiguration** " oder die **ADMX-Vorlage** , um die Berichterstellung zu konfigurieren. Die Cmdlets für das Berichterstattungsfeature sind über den folgenden Link verfügbar und werden durch die **Berichterstellung**vorangestellt. Eine vollständige Liste der Clientkonfigurationseinstellungen finden Sie unter [Informationen zu Clientkonfigurationseinstellungen](about-client-configuration-settings.md). Der folgende Abschnitt enthält Beispiele für die Konfiguration der App-V 5,0-Client Berichterstattung mithilfe von PowerShell.

### Konfigurieren von App-V-Client Berichten mithilfe von PowerShell

Die folgenden Beispiele zeigen, wie PowerShell-Parameter die Berichterstattungsfeatures des App-V 5,0-Clients konfigurieren können.

**Hinweis:**  
Die folgende Konfigurationsaufgabe kann auch mithilfe von Gruppenrichtlinieneinstellungen in der App-V 5,0 ADMX-Vorlage konfiguriert werden. Weitere Informationen zur Verwendung der ADMX-Vorlage finden Sie unter [Ändern der App-V 5,0-Client Konfiguration mithilfe der ADMX-Vorlage und der Gruppenrichtlinie](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md).
 


**So aktivieren Sie die Berichterstellung und initiieren die Datensammlung auf dem Computer, auf dem der App-V 5,0-Client ausgeführt wird**:

`Set-AppVClientConfiguration –ReportingEnabled 1`

**So konfigurieren Sie den Client so, dass Daten automatisch an einen bestimmten Berichtsserver gesendet**werden:

``` syntax
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30
```

`-ReportingInterval 1 -ReportingRandomDelay 30`

In diesem Beispiel wird der Client so konfiguriert, dass die Berichtsdaten automatisch an die Berichtsserver-URL gesendet werden <strong> http://MyReportingServer:MyPort/ </strong> . Darüber hinaus werden die Berichterstellungsdaten täglich zwischen 8:00 und 8:30 Uhr gesendet, abhängig von der Zufalls Verzögerung, die für die Sitzung generiert wurde.

**So begrenzen Sie die Größe des Datencaches auf dem Client**:

`Set-AppvClientConfiguration –ReportingDataCacheLimit 100`

Konfiguriert die maximale Größe des Berichtscaches auf dem Computer, auf dem der App-V 5,0-Client ausgeführt wird, auf 100 MB. Wenn die Cache Grenze erreicht ist, bevor die Daten an den Server gesendet werden, wird das Protokoll überschrieben, und die Daten werden nach Bedarf überschrieben.

**So konfigurieren Sie die Datenblockgröße, die über das Netzwerk zwischen dem Client und dem Server übertragen wird**:

`Set-AppvClientConfiguration –ReportingDataBlockSize 10240`

Gibt den maximalen Datenblock an, der vom Client an 10240 MB gesendet wird.

### Gesammelte Datentypen

In der folgenden Tabelle sind die Informationstypen aufgeführt, die Sie mithilfe der App-V 5,0-Berichterstellung erfassen können.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Client Informationen</th>
<th align="left">Paketinformationen</th>
<th align="left">Anwendungsverwendung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Hostname</p></td>
<td align="left"><p>Paket Name</p></td>
<td align="left"><p>Anfangs-und Endzeit</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0-Client Version</p></td>
<td align="left"><p>Paket Version</p></td>
<td align="left"><p>Ausführungs Status</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Prozessorarchitektur</p></td>
<td align="left"><p>Paketquelle</p></td>
<td align="left"><p>Shutdown-Status</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version des Betriebssystems</p></td>
<td align="left"><p>Prozent zwischengespeichert</p></td>
<td align="left"><p>Name der Anwendung</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Service Pack-Ebene</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Anwendungs Version</p></td>
</tr>
<tr class="even">
<td align="left"><p>Typ des Betriebssystems</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Benutzername</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Verbindungsgruppe</p></td>
</tr>
</tbody>
</table>
 


Der Client sammelt und speichert diese Daten im **XML-** Format. Der Datencache ist standardmäßig ausgeblendet und erfordert Administratorrechte, um die XML-Datei zu öffnen.

### Senden von Daten an den Server

Sie können den Computer, auf dem der App-V 5,0-Client ausgeführt wird, so konfigurieren, dass Daten automatisch an den angegebenen Berichtsserver gesendet werden. Wenn Sie den Server angeben möchten, verwenden Sie das Cmdlet " **festlegen-AppvClientConfiguration** " mit den folgenden Einstellungen:

-   ReportingEnabled

-   ReportingServerURL

-   ReportingStartTime

-   ReportingInterval

-   ReportingRandomDelay

Nachdem Sie die vorherigen Einstellungen konfiguriert haben, müssen Sie einen geplanten Vorgang erstellen. Der geplante Task setzt sich mit dem Server in Verbindung, der durch die **ReportingServerURL** -Einstellung angegeben wird, und initiiert die Übertragung. Wenn Sie Daten manuell außerhalb der geplanten Zeiten senden möchten, verwenden Sie das folgende PowerShell-Cmdlet:

`Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess`

Wenn der Berichtsserver zuvor konfiguriert wurde, kann der **URL-** Parameter ausgelassen werden. Wenn die Daten an einen anderen Speicherort gesendet werden sollen, geben Sie alternativ eine andere URL an, um die konfigurierte **ReportingServerURL** für diese Datensammlung zu überschreiben.

Der Parameter **-DeleteOnSuccess** gibt an, dass der Datencache gelöscht wird, wenn die Übertragung erfolgreich ist. Wenn dies nicht angegeben ist, wird der Cache nicht gelöscht.

### Manuelle Datensammlung

Sie können auch das Cmdlet **Send-AppVClientReport** verwenden, um Daten manuell zu sammeln. Diese Lösung ist mit oder ohne einen vorhandenen Berichtsserver hilfreich. In der folgenden Liste werden Informationen zum Sammeln von Daten mit oder ohne Berichtsserver angezeigt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Mit einem Berichts Server</th>
<th align="left">Ohne einen Berichts Server</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Wenn Sie über einen vorhandenen App-V 5,0-Berichts Server verfügen, erstellen Sie einen benutzerdefinierten geplanten Task oder ein angepasstes Skript. Geben Sie an, dass der Client die Daten an den angegebenen Speicherort mit der gewünschten Häufigkeit senden soll.</p></td>
<td align="left"><p>Wenn Sie nicht über einen vorhandenen App-V 5,0-Berichts Server verfügen, verwenden Sie den <strong> URL- </strong> Parameter, um die Daten an eine bestimmte Freigabe zu senden. Beispiel:</p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p>Im vorherigen Beispiel werden die Berichtsdaten an <strong> \MyShare\MyData &lt; /Strong-Speicherort gesendet, der &gt; durch den <strong> -URL-Parameter angegeben wird </strong> . Nachdem die Daten gesendet wurden, wird der Cache gelöscht.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn ein anderer Speicherort als der Berichts Server angegeben ist, werden die Daten mithilfe des <strong> XML- </strong> Formats ohne zusätzliche Verarbeitung gesendet.</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### Erstellen von Berichten

Sie müssen eine der folgenden Methoden verwenden, um Berichtsinformationen abzurufen und Berichte mithilfe von App-V 5,0 zu erstellen:

-   **Microsoft SQL Server Reporting Services (SSRS)** – Microsoft SQL Server Reporting Services steht in Microsoft SQL Server zur Verfügung. SSRS wird nicht installiert, wenn Sie den App-V 5,0-Berichtsserver installieren. Sie muss separat bereitgestellt werden, um die zugehörigen Berichte zu generieren.

    Verwenden Sie den folgenden Link, um weitere Informationen zur Verwendung von [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596)zu erhalten.

-   **Skripting** – Sie können Berichte erstellen, indem Sie direkt mit der App-V 5,0-Berichtsdatenbank Skripting durchführen. Beispiel:

    **Gespeicherte Prozedur:**

    **spProcessClientReport** ist für die Ausführung um Mitternacht oder 12:00 Uhr vorgesehen.

    Damit die geplante gespeicherte Prozedur Microsoft SQL Server ausgeführt werden kann, muss der Microsoft SQL Server-Agent ausgeführt werden. Stellen Sie sicher, dass der Microsoft SQL Server-Agent auf **Autostart**fest eingestellt ist. Weitere Informationen finden Sie unter [Autostart-SQL Server-Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).

    Die gespeicherte Prozedur wird auch bei Verwendung der App-V 5,0-Datenbankskripts erstellt.

Darüber hinaus sollten Sie sicherstellen, dass die **Maximale Anzahl gleichzeitiger Verbindungen** des Reporting Server-Webdiensts auf einen Wert festgesetzt ist, der vom Server verwaltet werden kann, ohne dass die Verfügbarkeit beeinträchtigt wird. Die empfohlene Anzahl der **maximalen gleichzeitigen Verbindungen** für den **Reporting Web Service** lautet **10.000**.






## Verwandte Themen


[Bereitstellen des App-V 5.0-Servers](deploying-the-app-v-50-server.md)

[So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

 

 





