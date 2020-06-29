---
title: Hardware- und Softwareanforderungen für Application Virtualization Client
description: Hardware- und Softwareanforderungen für Application Virtualization Client
author: dansimp
ms.assetid: 8b877a2c-5721-4b22-a47f-e2838d58ab12
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5b828f59ba36099b4f6a545cd5bbcb3c72d24e3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808024"
---
# Hardware- und Softwareanforderungen für Application Virtualization Client


In diesem Thema wird die empfohlene minimale Hardware-und Softwarekonfiguration für die Installation von Application Virtualization Desktop Client und Application Virtualization Client für Remote Desktop Dienste (vormals Terminal Dienste) beschrieben.

## Application Virtualization-Desktop Client


Die folgende Liste enthält die empfohlenen Mindest-Hardware-und Softwareanforderungen für den Application Virtualization Desktop-Client. Die Anforderungen werden zunächst für Microsoft Application Virtualization (app-v) 4.6 SP2 aufgeführt, gefolgt von den Anforderungen für Versionen, die APP-v 4.6 SP2 vorangestellt sind.

**Hinweis**  Der Application Virtualization (App-V)-Desktop Client erfordert keine zusätzlichen Prozessor-oder RAM-Ressourcen über die Anforderungen des Hostbetriebssystems hinaus.

 

### Hardwareanforderungen

Die Hardwareanforderungen gelten für alle Versionen.

-   Prozessor – lesen Sie die empfohlenen Systemanforderungen für das verwendete Betriebssystem.

-   Arbeitsspeicher – lesen Sie die empfohlenen Systemanforderungen für das verwendete Betriebssystem.

-   Datenträger – 30 MB für die Installation und 6 GB für den Cache.

### Software Anforderungen für App-V 4,6 SP2

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
<th align="left">Architektur-SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business-, Enterprise-oder Ultimate-Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professional, Enterprise oder Ultimate Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP1</p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Pro-oder Enterprise-Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
</tbody>
</table>

Die folgenden Softwarevoraussetzungen werden automatisch installiert, wenn Sie die Setup.exe-Methode verwenden. Wenn Sie das Setup.msi-Installationsprogramm verwenden, müssen zuerst die folgenden Produkte installiert werden.
- **Microsoft Visual c++ 2005 SP1 Redistributable Package (x86)**– Weitere Informationen zur Installation von Microsoft Visual c++ 2005 SP1 Redistributable Package (x86) finden Sie unter [Microsoft Visual c++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Laden Sie für Version 4,5 SP2 des App-V-Clients Vcredist\_x86.exe aus dem [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL-Sicherheits Update](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360) .
  -   **Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)**– Weitere Informationen zur Installation von Microsoft Core XML Services (MSXML) 6,0 SP1 (x86) finden Sie unter [Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

Für den 4,6-Desktop Client Application Virtualization (App-V) werden die folgenden zusätzlichen Softwarevoraussetzungen automatisch installiert, wenn Sie die Setup.exe-Methode verwenden. Wenn Sie das Setup.msi-Installationsprogramm verwenden, müssen Sie auch mit den anderen aufgeführten Voraussetzungen installieren.

-   **Microsoft VisualC + + 2008SP1 Redistributable Package (x86)**– Weitere Informationen zur Installation von Microsoft VisualC + + 2008 SP1 Redistributable Package (x86) finden Sie unter [Microsoft VisualC + + 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Software Anforderungen für Versionen, die App-V 4,6 SP2 vorausgehen

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
<th align="left">Architektur-SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 oder SP3</p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business-, Enterprise-oder Ultimate-Edition</p></td>
<td align="left"><p>Kein Service Pack, SP1 oder SP2</p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7 ¹</p></td>
<td align="left"><p>Professional, Enterprise oder Ultimate Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP1</p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
</tbody>
</table>
¹ wird nur für App-v 4,5 SP1 und SP2, App-v 4,6 und 4,6 SP1 unterstützt

Der Application Virtualization (App-V) 4,6-Desktop Client unterstützt x86-und x64-SKUs dieser Betriebssysteme.

Die folgenden Softwarevoraussetzungen werden automatisch installiert, wenn Sie die Setup.exe-Methode verwenden. Wenn Sie das Setup.msi-Installationsprogramm verwenden, müssen zuerst die folgenden Produkte installiert werden.

-   <strong>Microsoft Visual c++ 2005 SP1 Redistributable Package (x86) </strong> – Weitere Informationen zur Installation von Microsoft Visual c++ 2005 SP1 Redistributable Package (x86) finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961)"> Microsoft Visual c++ 2005 SP1 Redistributable Package (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=119961"> https://go.microsoft.com/fwlink/?LinkId=119961 </a> ). Laden Sie für Version 4,5 SP2 des App-V-Clients Vcredist_x86.exe aus dem <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="[Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360)"> Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL-Sicherheits Update </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=169360"> https://go.microsoft.com/fwlink/?LinkId=169360 </a> ) herunter.

-   <strong>Microsoft Core XML Services (MSXML) 6,0 SP1 (x86) </strong> – Weitere Informationen zur Installation von Microsoft Core XML Services (MSXML) 6,0 SP1 (x86) finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="[Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266)"> Microsoft Core XML Services (MSXML) 6,0 SP1 (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=63266"> https://go.microsoft.com/fwlink/?LinkId=63266 </a> ).

-   <strong>Fehlerberichterstattung für Microsoft </strong> -Anwendungen – das Installationsprogramm für diese Software ist im <strong> </strong> Ordner "Support\Watson" in der selbstextrahierenden Archivdatei enthalten.

Für den 4,6-Desktop Client Application Virtualization (App-V) werden die folgenden zusätzlichen Softwarevoraussetzungen automatisch installiert, wenn Sie die Setup.exe-Methode verwenden. Wenn Sie das Setup.msi-Installationsprogramm verwenden, müssen Sie auch mit den anderen aufgeführten Voraussetzungen installieren.

-   <strong>Microsoft Visual c++ 2008 SP1 Redistributable Package (x86) </strong> – Weitere Informationen zur Installation von Microsoft Visual c++ 2008 SP1 Redistributable Package (x86) finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="[Microsoft Visual C++ 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700)"> Microsoft Visual c++ 2008 SP1 Redistributable Package (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=150700"> https://go.microsoft.com/fwlink/?LinkId=150700 </a> ).

## Application Virtualization-Client für Remote Desktop Dienste

Im folgenden finden Sie die empfohlenen Hardware-und Softwareanforderungen für den Application Virtualization-Client für Remote Desktop Dienste. Die Anforderungen werden zunächst für appv461_3 aufgeführt, gefolgt von den Anforderungen für Versionen, die App-V 4,6 SP2 vorangestellt sind.

Der Application Virtualization (App-V)-Client für Remote Desktop Dienste erfordert keine zusätzlichen Prozessor-oder RAM-Ressourcen über die Anforderungen des Hostbetriebssystems hinaus.

### Hardwareanforderungen

Die Hardwareanforderungen gelten für alle Versionen.

-   Prozessor – lesen Sie die empfohlenen Systemanforderungen für das verwendete Betriebssystem.

-   Arbeitsspeicher – lesen Sie die empfohlenen Systemanforderungen für das verwendete Betriebssystem. Diese Anforderungen sind auch von der Anzahl der Benutzer und Anwendungen abhängig.

-   Datenträger – 30 MB für die Installation und 6 GB für den Cache.

### Software Anforderungen für App-V 4,6 SP2

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
<th align="left">Architektur-SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

Die folgenden Softwarevoraussetzungen werden automatisch installiert, wenn Sie die Setup.exe-Methode verwenden. Wenn Sie das Setup.msi-Installationsprogramm verwenden, müssen zuerst die folgenden Produkte installiert werden.

-   **Microsoft VisualC + + 2005SP1 Redistributable Package (x86)**– Weitere Informationen zur Installation von Microsoft VisualC + + 2005 SP1 Redistributable Package (x86) finden Sie unter [Microsoft VisualC + + 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Laden Sie für Version 4.5 SP2 des App-V-Clients Vcredist\_x86.exe aus dem [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL-Sicherheits Update](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360) .

-   **Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)**– Weitere Informationen zur Installation von Microsoft Core XML Services (MSXML) 6.0 SP1 (x86) finden Sie unter [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

-   **Fehlerberichterstattung für Microsoft-Anwendungen**– das Installationsprogramm für diese Software ist im Ordner " **Support\\Watson** " in der selbstextrahierenden Archivdatei enthalten.

Für den 4,6-Desktop Client Application Virtualization (App-V) werden die folgenden zusätzlichen Softwarevoraussetzungen automatisch installiert, wenn Sie die Setup.exe-Methode verwenden. Wenn Sie das Setup.msi-Installationsprogramm verwenden, müssen Sie auch mit den anderen aufgeführten Voraussetzungen installieren.

-   **Microsoft VisualC + + 2008SP1 Redistributable Package (x86)**– Weitere Informationen zur Installation von Microsoft VisualC + + 2008 SP1 Redistributable Package (x86) finden Sie unter [Microsoft VisualC + + 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Software Anforderungen für Versionen, die App-V 4,6 SP2 vorausgehen

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
<th align="left">Architektur-SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP2</p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

Der Application Virtualization (App-V) 4,6-Client für Remote Desktop Dienste unterstützt x86-und x64-SKUs dieser Betriebssysteme.

## Verwandte Themen
- [Hardware- und Softwareanforderungen für Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)
- [Systemanforderungen für Application Virtualization](application-virtualization-system-requirements.md)
- [So installieren Sie den Client über die Befehlszeile](how-to-install-the-client-by-using-the-command-line-new.md)
- [So installieren Sie Application Virtualization Client manuell](how-to-manually-install-the-application-virtualization-client.md)
- [So aktualisieren Sie Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)
