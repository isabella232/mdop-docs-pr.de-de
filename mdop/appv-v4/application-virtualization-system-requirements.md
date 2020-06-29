---
title: Systemanforderungen für Application Virtualization
description: Systemanforderungen für Application Virtualization
author: dansimp
ms.assetid: a2798dd9-168e-45eb-8103-e12e128fae7c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c160a7532b521bb41570b419b22b9e7daaec2987
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807939"
---
# Systemanforderungen für Application Virtualization


In diesem Thema werden die Mindest-Hardware-und Softwareanforderungen für den Microsoft Application Virtualization (App-V)-Verwaltungsserver und den Streamingserver beschrieben.

## Application Virtualization Management und Streaming Server


Die folgende Liste enthält die Mindestanforderungen für Hardware und Software für den App-v-Verwaltungsserver und den App-v-Streamingserver.

### Hardwareanforderungen

-   Prozessor – Intel Pentium III, 1 GHz

-   RAM – 512 MB

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses

### Software Anforderungen

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
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ gilt nur für App-V 4,5 SP1 und SP2.

## Datenspeicher


Die folgende Liste enthält die Mindestanforderungen für Hardware und Software für den Computer, der beim Installieren des Datenspeichers auf einem separaten Server verwendet wird. Der Datenspeicher ist nur für den Application Virtualization-Verwaltungs Server erforderlich.

### Hardwareanforderungen

-   Prozessor – Intel Pentium III, 850 MHz

-   RAM – 512 MB

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz

### Software Anforderungen

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
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ gilt nur für App-V 4,5 SP1 und SP2.

-   Datenbank – Microsoft SQL Server2000 SP3a oder SP4, SQL Server2005 SP1, SP2 oder SP3 oder SQL Server2008, kein Service Pack oder SP1 oder SQL Server2008 R2 (32-Bit oder 64-Bit)

-   Microsoft Data Access-Komponenten – MDAC 2,7

-   Domänencontroller – Active Directory-Domänendienste oder Windows NT 4.0-basierter primärer Domänencontroller (PDC) als zentrale Authentifizierungsstelle

## Verwaltungs-Web-Service


Die folgende Liste enthält die Mindestanforderungen für Hardware und Software für den Application Virtualization Management Web Service, wenn Sie auf einem anderen Computer installiert ist.

### Hardwareanforderungen

-   Prozessor – Intel Pentium III, 800 MHz

-   Arbeitsspeicher – 256 MB

-   Speicherplatz – 50 MB verfügbarer Festplattenspeicherplatz

### Software Anforderungen

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
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ gilt nur für App-V 4,5 SP1 und SP2.

-   Internetinformationsdienste – Internetinformationsdienste (IIS) 6,0, konfiguriert mit Microsoft ASP.net, IIS 7

-   Microsoft .NET Framework 2.0

## Verwaltungskonsole


Die folgende Liste enthält die Mindestanforderungen für Hardware und Software für die Application Virtualization Management Console, wenn Sie auf einem anderen Computer installiert ist.

### Hardwareanforderungen

-   Prozessor – Intel Pentium III, 450 MHz

-   Arbeitsspeicher – 256 MB

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz

### Software Anforderungen

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
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business-, Enterprise-oder Ultimate-Edition</p></td>
<td align="left"><p>Kein Service Pack, SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professional, Enterprise oder Ultimate Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ gilt nur für App-V 4,5 SP1 und SP2.

-   Microsoft Management Console – MMC 3.0 oder höher

-   Microsoft .NET Framework 2.0 SP2 (zumindest)

    **Wichtig**  Die Mindestanforderung ist .NET Framework 2,0 SP2, wenn Sie App-v-Hotfix-KB980850 oder nachfolgende App-v-Hotfixes auf dem Computer installieren müssen, auf dem die APP-v-Verwaltungskonsole ausgeführt wird.

     

## Verwandte Themen


[Hardware- und Softwareanforderungen für Application Virtualization Client](application-virtualization-client-hardware-and-software-requirements.md)

[Hardware- und Softwareanforderungen für Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)

[So konfigurieren Sie Server für die serverbasierte Bereitstellung](how-to-configure-servers-for-server-based-deployment.md)

[So installieren Sie die Server und Systemkomponenten](how-to-install-the-servers-and-system-components.md)

[So aktualisieren Sie die Server und Systemkomponenten](how-to-upgrade-the-servers-and-system-components.md)

 

 





