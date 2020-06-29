---
title: So konfigurieren Sie den Client für den Abruf von Anwendungspaketen
description: So konfigurieren Sie den Client für den Abruf von Anwendungspaketen
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807263"
---
# So konfigurieren Sie den Client für den Abruf von Anwendungspaketen


Wenn der Client mit einem Application Virtualization (App-V)-Verwaltungsserver als Veröffentlichungsserver konfiguriert ist, ruft der Clientstandard mäßig beim nächsten Veröffentlichungs Aktualisierungszyklus vom Server die Open Software Descriptor (OSD)-und Paket Manifestdateien für jedes Paket ab, das der Benutzer für die Verwendung autorisiert hat. Der Client verwendet die in diesen Dateien definierten Paketquellinformationen, um zu bestimmen, wo die Paketinhalte, Symbole und Dateitypzuordnungen zu finden sind.

Wenn der Client den Paketinhalt (SFT-Datei) von einem lokalen app-v-Streamingserver oder einer anderen alternativen Quelle wie einem Webserver oder Dateiserver anstatt vom APP-v-Verwaltungsserver abrufen soll, können Sie den ApplicationSourceRoot-Registrierungsschlüsselwert auf dem Computer so konfigurieren, dass er auf die lokale Inhaltsfreigabe auf dem anderen Server verweist. Die OSD-Datei definiert weiterhin den ursprünglichen Quellpfad für den Paketinhalt. Der Client verwendet jedoch den Wert der ApplicationSourceRoot-Einstellung anstelle des Servers und der Freigabe, die im Inhaltspfad in der OSD-Datei angegeben sind. Dadurch wird der Client umgeleitet, um den Inhalt vom anderen Server abzurufen.

Sie können auch die Registrierungsschlüsselwerte für OSDSourceRoot und IconSourceRoot konfigurieren, wenn Sie diese Einstellungen in der Paket Manifestdatei oder in den von einem Veröffentlichungsserver gesendeten Pfaden überschreiben möchten. OSDSourceRoot gibt einen Quellspeicherort für das Abrufen von OSD-Dateien für ein Anwendungspaket während der Veröffentlichung an. Der IconSourceRoot gibt einen Quellspeicherort für den Symbol Abruf für ein Anwendungspaket während der Veröffentlichung an.

**Hinweis:**  
-   Die IconSourceRoot-und OSDSourceRoot-Einstellungen setzen die Werte in der Paket Manifestdatei außer Kraft, wenn Sie also versuchen, ein Paket mithilfe der Windows Installer-Datei Methode (MSI) bereitzustellen, werden auch die Werte in der Paket Manifestdatei überschrieben, die in dieser MSI-Datei enthalten sind.

-   Während der Veröffentlichungs-und http (S)-Streaming-Vorgänge verwenden App-V 4,5 SP1-Clients die Proxyservereinstellungen, die in Internet Explorer auf dem Computer des Benutzers konfiguriert sind.



**So konfigurieren Sie den ApplicationSourceRoot-Registrierungsschlüsselwert**

-   Konfigurieren Sie den ApplicationSourceRoot im folgenden Registrierungsschlüsselwert mit einem UNC-Pfad oder einer URL:

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\applicationsourceroot

    Das richtige Format für den UNC-Pfad (Universal Naming Convention) ist **\\\\computername\\sharefolder\\\ [Folder \] \ [\ \ \]**, wobei **Folder** optional ist. Bei **Computer** Name kann es sich um einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder eine IP-Adresse handeln, und **sharefolder** kann ein Laufwerkbuchstabe sein. Es wird nur der **\\\\computername\\sharedfolder** -oder Laufwerkbuchstaben Bereich des OSD-Pfads ersetzt.

    Das richtige Format für den URL-Pfad ist **Protocol://Servername: \ [Port \] \ [/path\] \ [/\]**, wobei **Port** und **path** optional sind. Wenn **Port** nicht angegeben wird, wird der Standardport für das Protokoll verwendet. Nur der Abschnitt **Protocol://Server: Port** der OSD-URL wird ersetzt.

    **Wichtig**  
    Umgebungsvariablen werden in der ApplicationSourceRoot-Definition nicht unterstützt.



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**So konfigurieren Sie den OSDSourceRoot-Wert**

-   Konfigurieren Sie den OSDSourceRoot im folgenden Registrierungsschlüsselwert mit einem UNC-Pfad oder einer URL:

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\osdsourceroot

    Zulässige Formate für die OSDSourceRoot sind UNC-Pfade und-URLs, wie im folgenden Beispiel gezeigt:

    **\\\\computername\\sharefolder\\resource** oder **\\\\computername\\content** oder ** &lt; Laufwerk &gt; : \\foldername**

    **http://computername/productivity/** oder**https://computername/productivity/**

**So konfigurieren Sie den IconSourceRoot-Wert**

-   Konfigurieren Sie den IconSourceRoot im folgenden Registrierungsschlüsselwert mit einem UNC-Pfad oder einer URL:

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\iconsourceroot

    Zulässige Formate für die IconSourceRoot sind UNC-Pfade und-URLs, wie im folgenden Beispiel gezeigt:

    **\\\\computername\\sharefolder\\resource** oder **\\\\computername\\content** oder ** &lt; Laufwerk &gt; : \\foldername**

    **http://computername/productivity/** oder**https://computername/productivity/**

## Verwandte Themen


[So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









