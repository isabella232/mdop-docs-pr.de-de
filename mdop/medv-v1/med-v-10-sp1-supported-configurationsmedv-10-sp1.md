---
title: Von MED-V 1.0 SP1 unterstützte Konfigurationen
description: Von MED-V 1.0 SP1 unterstützte Konfigurationen
author: dansimp
ms.assetid: 4dcf37c4-a061-43d2-878c-28efc87c3cdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5a707e8a3d59a423308f9f735ff38df9e235fbf5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810393"
---
# Von MED-V 1.0 SP1 unterstützte Konfigurationen


In diesem Thema werden die Anforderungen festgelegt, die erforderlich sind, um Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 Service Pack 1 (SP1) in Ihrer Umgebung zu installieren und auszuführen.

## MED-V 1,0 SP1-Client System Anforderungen


### Anforderungen des MED-V-Client-Betriebssystems

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die MED-V 1,0 SP1-Clientinstallation unterstützt werden.

**Hinweis:**  
Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zur Unterstützung der Zeitpläne für Ihr Produkt finden Sie unter vom [Lifecycle unterstützte Service Packs](https://go.microsoft.com/fwlink/?LinkId=31975) ( https://go.microsoft.com/fwlink/?LinkId=31975) . Weitere Informationen zu den Microsoft-Supportlebenszyklus Richtlinien finden Sie im [Microsoft Support Lifecycle-Supportrichtlinien-FAQ](https://go.microsoft.com/fwlink/?LinkId=31976) ( https://go.microsoft.com/fwlink/?LinkId=31976) .



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 oder SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise oder Ultimate</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professional, Enterprise oder Ultimate</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
</tbody>
</table>



**Hinweis:**  
Der MED-V-Client wird im systemeigenen x64-Modus nicht ausgeführt. Stattdessen wird MED-V im Windows-64-Bit-Modus (WOW64) auf 64-Bit-Computern ausgeführt.



In der folgenden Tabelle ist der minimale Arbeitsspeicher für jedes Betriebssystem aufgeführt, das in MED-V 1,0 SP1 unterstützt wird.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Minimal erforderlicher Arbeitsspeicher</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows XP Professional</p></td>
<td align="left"><p>1 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 x86</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7 x64</p></td>
<td align="left"><p>3 GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-client-configuration-"></a>MED-V 1,0 SP1-Client Konfiguration

**.NET Framework-Version**

Die folgenden Versionen von Microsoft .NET Framework werden für die MED-V 1,0 SP1-Clientinstallation unterstützt:

-   .NET Framework 2,0 oder .NET Framework 2,0 SP1

-   .NET Framework 3,0 oder .NET Framework 3,0 SP1

-   .NET Framework 3,5 oder .NET Framework 3,5 SP1

**Virtualisierungs-Engine**

Microsoft Virtual PC 2007 SP1 mit dem Hotfix, der im Microsoft Knowledge Base-Artikel 974918 beschrieben wird, wird für die MED-V 1,0 SP1-Clientinstallation in den folgenden Konfigurationen unterstützt:

-   Statische virtuelle Festplatte (VHD)-Datei

-   Mehrere VHD-Dateien, die sich im gleichen Verzeichnis befinden

-   Dynamische VHD-Datei

**Internet Browser**

Windows Internet Explorer 7 und Windows Internet Explorer 8 werden für die MED-V 1,0 SP1-Clientinstallation unterstützt.

**Microsoft Hyper-V Server**

Der Med-v-Client wird in einer Microsoft Hyper-v-Server Umgebung nicht unterstützt.

## System Anforderungen für MED-V 1,0 SP1-Arbeitsbereiche


Med-v 1,0 SP1 führt Änderungen an den Systemanforderungen von denen für med-v 1,0 ein.

### Betriebs System Anforderungen für den MED-V-Arbeitsbereich

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für MED-V 1,0 SP1-Arbeitsbereiche unterstützt werden.

**Hinweis:**  
Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zur Unterstützung der Zeitpläne für Ihr Produkt finden Sie unter vom [Lifecycle unterstützte Service Packs](https://go.microsoft.com/fwlink/?LinkId=31975) ( https://go.microsoft.com/fwlink/?LinkId=31975) . Weitere Informationen zu den Microsoft-Supportlebenszyklus Richtlinien finden Sie im [Microsoft Support Lifecycle-Supportrichtlinien-FAQ](https://go.microsoft.com/fwlink/?LinkId=31976) ( https://go.microsoft.com/fwlink/?LinkId=31976) .



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 2000</p></td>
<td align="left"><p>Professional</p></td>
<td align="left"><p>SP4</p></td>
<td align="left"><p>X86</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 oder SP3</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>SP3 wird empfohlen, um sicherzustellen, dass der Med-v-Arbeitsbereich mit zukünftigen Versionen von Med-v kompatibel ist.</p>
</div>
<div>

</div></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-workspace-configuration-"></a>MED-V 1,0 SP1-Arbeitsbereichskonfiguration

**.NET Framework-Version**

Für med-v ist eine der folgenden unterstützten Versionen der Microsoft .NET Framework für med-v 1,0 SP1-Arbeitsbereichs Installation erforderlich:

-   .NET Framework 2,0 SP1

-   .NET Framework 3,0 SP1

-   .NET Framework 3,5 oder .NET Framework 3,5 SP1

**Hinweis:**  
Wir empfehlen .NET Framework 3,5 SP1, um sicherzustellen, dass der Med-v-Arbeitsbereich mit zukünftigen Versionen von Med-v kompatibel ist.



**Internet Browser**

Windows Internet Explorer 6 SP2 und Windows Internet Explorer 7 werden für die MED-V 1,0 SP1-Arbeitsbereichs Installation unterstützt.

### <a href="" id="med-v-workspace-images-"></a>MED-V-Arbeitsbereichs Bilder

MED-V-Arbeitsbereichs Bilder müssen mithilfe von Virtual PC 2007 SP1 erstellt werden.

## MED-V 1,0 SP1-Server System Anforderungen


Med-v 1,0 SP1 führt Änderungen an den Systemanforderungen von denen für med-v 1,0 ein.

### Anforderungen des MED-V 1,0 Server-Betriebssystems

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für MED-V 1,0 SP1-Server Installationen unterstützt werden.

**Hinweis:**  
Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zur Unterstützung der Zeitpläne für Ihr Produkt finden Sie unter vom [Lifecycle unterstützte Service Packs](https://go.microsoft.com/fwlink/?LinkId=31975) ( https://go.microsoft.com/fwlink/?LinkId=31975) . Weitere Informationen zu den Microsoft-Supportlebenszyklus Richtlinien finden Sie im [Microsoft Support Lifecycle-Supportrichtlinien-FAQ](https://go.microsoft.com/fwlink/?LinkId=31976) ( https://go.microsoft.com/fwlink/?LinkId=31976) .



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Standard oder Enterprise</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>X86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard oder Enterprise</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-server-configuration-"></a>MED-V 1,0 SP1-Server Konfiguration

**.NET Framework-Version**

Für med-v ist eine der folgenden unterstützten Versionen der Microsoft .NET Framework für med-v 1,0 SP1-Arbeitsbereichs Installation erforderlich:

-   .NET Framework 2,0 oder .NET Framework 2,0 SP1

-   .NET Framework 3,0 oder .NET Framework 3,0 SP1

-   .NET Framework 3,5 oder .NET Framework 3,5 SP1

**Microsoft SQL Server-Version**

Die folgenden Versionen von Microsoft SQL Server werden für med-v 1,0 SP1 unterstützt, wenn SQL Server lokal oder Remote vom Med-v 1,0 SP1-Server installiert wird:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">SQL Server-Version</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server 2005</p></td>
<td align="left"><p>Express-, Standard-oder Enterprise-Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>X86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server 2008</p></td>
<td align="left"><p>Express, Standard oder Enterprise</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>X86 oder x64</p></td>
</tr>
</tbody>
</table>



**Microsoft Hyper-V Server**

Der Med-v-Server wird in einer Microsoft Hyper-v-Server Umgebung unterstützt.

## MED-V 1,0 SP1 – Globalisierungsinformationen


Obwohl Med-v nicht in anderen Sprachen als Englisch verfügbar ist, werden die folgenden Sprachversionen des Windows-Betriebssystems für die Med-v 1,0 SP1-Client-, Workspace-und Server Installationen unterstützt:

-   Englisch

-   Französisch

-   Deutsch

-   Italienisch

-   Spanisch

-   Portugiesisch (Brasilien)

-   Niederländisch (Niederlande)

-   Japanisch









