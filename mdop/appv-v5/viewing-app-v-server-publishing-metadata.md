---
title: Anzeigen von App-V-Server-Veröffentlichungsmetadaten
description: Anzeigen von App-V-Server-Veröffentlichungsmetadaten
author: dansimp
ms.assetid: 048dd42a-24d4-4cc4-81f6-7a919aadd9b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 304aa656de98a0c9d59f0a6166811ead911033ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804847"
---
# Anzeigen von App-V-Server-Veröffentlichungsmetadaten


Gehen Sie wie folgt vor, um Veröffentlichungsmetadaten anzuzeigen, die Ihnen bei der Behebung von Problemen mit der Veröffentlichung helfen können. Sie müssen den App-V-Verwaltungsserver verwenden, um dieses Verfahren verwenden zu können.

Dieser Artikel enthält die folgenden Informationen:

-   [App-V 5,0 SP3-Anforderungen für das Anzeigen von Veröffentlichungsmetadaten](#bkmk-50sp3-reqs-pub-meta)

-   [Syntax für die Anzeige von Veröffentlichungsmetadaten](#bkmk-syntax-view-pub-meta)

-   [Abfrage Werte für Clientbetriebssystem und-Version](#bkmk-values-query-pub-meta)

-   [Definition von Veröffentlichungsmetadaten](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-50sp3-reqs-pub-meta"></a>App-V 5,0 SP3-Anforderungen für das Anzeigen von Veröffentlichungsmetadaten


In App-v 5,0 SP3 müssen Sie die folgenden Werte in der Adresse angeben, wenn Sie den App-v-Veröffentlichungsserver nach Metadaten Abfragen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Wert</th>
<th align="left">Zusätzliche Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Wenn Sie den <strong> Clientversion </strong> -Parameter aus der Abfrage weglassen, schließen die Metadaten die neuen App-V 5,0 SP3-Features aus.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Kunden</strong></p></td>
<td align="left"><p>Sie müssen diesen Wert nur angeben, wenn Sie beim Sequenzieren des Pakets bestimmte Clientbetriebssysteme auswählen. Wenn Sie die Standardeinstellung (alle Betriebssysteme) auswählen, geben Sie diesen Wert in der Abfrage nicht an.</p>
<p>Wenn Sie den <strong> Client </strong> -Parameter aus der Abfrage weglassen, werden nur die Pakete, die für die Unterstützung eines beliebigen Betriebssystems sequenziert wurden, in den Metadaten angezeigt.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a>Abfragesyntax für das Anzeigen von Veröffentlichungsmetadaten


Die folgende Tabelle enthält die Beispiele für Syntax und Abfrage.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version von App-V</th>
<th align="left">Abfragesyntax</th>
<th align="left">Parameter Beschreibungen</th>
<th align="left">Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parameter</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;"Pubserver&gt;</p></td>
<td align="left"><p>Der Name des App-V-Veröffentlichungsservers.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Veröffentlichungs-Port #&gt;</p></td>
<td align="left"><p>Port zu dem App-V-Veröffentlichungsserver, den Sie bei der Konfiguration des Veröffentlichungsservers festgelegt haben.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Clientversion = &lt; AppvClientVersion&gt;</p></td>
<td align="left"><p>Die Version des App-V-Clients. In der folgenden Tabelle finden Sie den richtigen zu verwendenden Wert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Clients = &lt; OSStringValue&gt;</p></td>
<td align="left"><p>Das Betriebssystem des Computers, auf dem der App-V-Client ausgeführt wird. In der folgenden Tabelle finden Sie den richtigen zu verwendenden Wert.</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p>Wenn Sie den Namen des Veröffentlichungsservers und die Portnummer (http:// &lt; "pubserver &gt; : &lt; Publishing Port # &gt; ) vom App-V-Client abrufen möchten, sehen Sie sich die URL-Konfiguration des <strong> PowerShell-Cmdlets Get-AppvPublishingServer an </strong> .</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p>Im Beispiel:</p>
<ul>
<li><p>Ein Windows Server 2012 R2 mit dem Namen "pubsvr01" hostet den Veröffentlichungsdienst.</p></li>
<li><p>Der Windows-Client ist Windows 8,1 64-Bit.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 5,0 über APP-v 5,0 SP2</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong>Hinweis:</strong><br/><p><strong>Clientversion </strong> und <strong> -Clients </strong> werden nur in App-V 5,0 SP3 unterstützt.</p>
</div>
<div>

</div></td>
<td align="left"><p>Lesen Sie die Informationen für App-V 5,0 SP3.</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p>Im Beispiel hostet ein Windows Server 2012 R2 mit dem Namen "pubsvr01" die Verwaltungs-und Veröffentlichungsdienste.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a>Abfrage Werte für Clientbetriebssystem und-Version


Geben Sie in ihrer Veröffentlichungsmetadaten-Abfrage die Zeichenfolgenwerte ein, die dem verwendeten Clientbetriebssystem und der verwendeten Version entsprechen.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Architektur</th>
<th align="left">Zeichenfolgenwert für die Zeichenfolge</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows8.1</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8.1</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>WindowsClient_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>WindowsClient_6.1_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>WindowsServer_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>WindowsServer_6.1_x86</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a>Definition von Veröffentlichungsmetadaten


Wenn Pakete auf einem Computer veröffentlicht werden, auf dem der App-V-Client ausgeführt wird, werden Metadaten an diesen Computer gesendet, der angibt, welche Pakete und Verbindungsgruppen veröffentlicht werden. Der App-V-Client führt zwei getrennte Anforderungen für die folgenden Aktionen aus:

-   Pakete und Verbindungsgruppen, die für den Clientcomputer berechtigt sind.

-   Pakete und Verbindungsgruppen, die für den aktuellen Benutzer berechtigt sind.

Der Veröffentlichungsserver kommuniziert mit dem Verwaltungsserver, um zu ermitteln, welche Pakete und Verbindungsgruppen für den anfordernden verfügbar sind. Der Veröffentlichungsserver muss beim Verwaltungsserver registriert sein, damit die Metadaten generiert werden.

Sie können die Metadaten für jede Anforderung in einem Internet Browser anzeigen, indem Sie eine Abfrage verwenden, die sich im Kontext des jeweiligen Benutzers oder Computers befindet.






## Verwandte Themen


[Technische Referenz zu App-V 5.0](technical-reference-for-app-v-50.md)









