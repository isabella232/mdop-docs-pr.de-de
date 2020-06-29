---
title: Neuigkeiten in AGPM 4.0 SP3
description: Neuigkeiten in AGPM 4.0 SP3
author: dansimp
ms.assetid: df495d55-9fbf-4f7e-a7af-3905f4f8790e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: a98bda82fab561113522382b4de6539a9dc23d0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808179"
---
# Neuigkeiten in AGPM 4.0 SP3


Dieser Inhalt beschreibt Verbesserungen und unterstützte Konfigurationen für Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack3 (SP3). Wenn es einen Unterschied zwischen diesem Inhalt und anderer AGPM-Dokumentation gibt, sollten Sie diesen Inhalt als autorisierend ansehen und davon ausgehen, dass er die andere Dokumentation ersetzt.

## <a href="" id="what-s-new"></a>Neuigkeiten 


AGPM 4.0 SP3 unterstützt die folgenden Features und Funktionen.

### Unterstützung für Windows10

AGPM 4.0 SP3 bietet Unterstützung für die Windows10-und Windows Server 2016-Betriebssysteme.

### Unterstützung für PowerShell

AGPM 4.0 SP3 bietet Unterstützung für PowerShell-Cmdlets. Eine Liste der in AGPM 4.0 SP3 verfügbaren Cmdlets, einschließlich Beschreibungen und Syntax, finden Sie unter [Automatisierung des Microsoft-Desktop Optimierungs Pakets mit Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).

### Kundenfeedback und Hotfix-Rollup

AGPM 4,0 SP3 umfasst ein Rollup aller Fixes bis einschließlich Microsoft Advanced Group Policy Management 4,0 SP2 sowie alle Behebungen für Probleme, die seit AGPM 4,0 SP2 gefunden wurden.

### Möglichkeit zum Upgrade auf AGPM 4.0 SP3 ohne erneutes Eingeben von Konfigurationsparametern

Sie können den AGPM-Client oder AGPM-Server auf AGPM 4.0 SP3 aktualisieren, ohne dazu aufgefordert zu werden, die Konfigurationsparameter (so genannte Smart Upgrade) nur von AGPM 4.0 und höher erneut einzugeben, wie in der folgenden Tabelle dargestellt. Wenn Sie ein Upgrade von anderen AGPM-Versionen auf AGPM 4.0 SP3 durchführen, wie in der Tabelle gezeigt, müssen Sie das klassische Upgrade verwenden, bei dem Sie die Konfigurationsparameter erneut eingeben müssen. Da jede Version von AGPM einem bestimmten Betriebssystem zugeordnet ist, lesen Sie [Auswählen der zu installierenden AGPM-Version](https://go.microsoft.com/fwlink/?LinkId=254350) , und stellen Sie sicher, dass Sie das Betriebssystem entsprechend aktualisieren, bevor Sie AGPM aktualisieren.

**Unterstützte Upgrades für AGPM 4,0 SP3**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>AGPM-Version, auf der Sie ein Upgrade durchführen können</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3.0</strong></p></td>
<td align="left"><p><strong>4.0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
<td align="left"><p><strong>4,0 SP2</strong></p></td>
<td align="left"><p><strong>4,0 SP3</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Klassisches Upgrade</p></td>
<td align="left"><p>Klassisches Upgrade</p></td>
<td align="left"><p>Die Installation ist blockiert</p></td>
<td align="left"><p>Die Installation ist blockiert</p></td>
<td align="left"><p>Die Installation ist blockiert</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3.0</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Klassisches Upgrade</p></td>
<td align="left"><p>Die Installation ist blockiert</p></td>
<td align="left"><p>Die Installation ist blockiert</p></td>
<td align="left"><p>Die Installation ist blockiert</p></td>
</tr>
<tr class="even">
<td align="left"><p>4.0</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Nicht anwendbar</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Intelligentes Upgrade</p></td>
<td align="left"><p>Intelligentes Upgrade</p></td>
<td align="left"><p>Intelligentes Upgrade</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,0 SP1</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Nicht anwendbar</p></td>
<td align="left"><p>Nicht anwendbar</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Intelligentes Upgrade</p></td>
<td align="left"><p>Intelligentes Upgrade</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0 SP2</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Nicht anwendbar</p></td>
<td align="left"><p>Nicht anwendbar</p></td>
<td align="left"><p>Nicht anwendbar</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Intelligentes Upgrade</p></td>
</tr>
</tbody>
</table>

 

## Unterstützte Konfigurationen


AGPM 4.0 SP3 unterstützt die Konfigurationen in der folgenden Tabelle. Obwohl AGPM Gemischte Konfigurationen unterstützt, wird dringend empfohlen, den AGPM-Client und AGPM-Server auf derselben Betriebssystem Zeile auszuführen, beispielsweise Windows10 mit Windows Server 2016, Windows 8,1 mit Windows Server 2012 R2 usw.

**AGPM 4.0 SP3 unterstützte Betriebssysteme und Richtlinieneinstellungen**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Unterstützte Konfigurationen für den AGPM-Server</strong></th>
<th align="left"><strong>Unterstützte Konfigurationen für den AGPM-Client</strong></th>
<th align="left"><strong>AGPM-Unterstützung</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2016 oder Windows 10</p></td>
<td align="left"><p>Windows10</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2 oder Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 oder Windows 8.1</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 oder Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit Service Pack 1 (SP1)</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, jedoch können keine Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, gemeldet oder bearbeitet werden</p></td>
</tr>
</tbody>
</table>

 

## Voraussetzungen für die Installation von AGPM 4.0 SP3

In der folgenden Tabelle wird das Verhalten von AGPM 4.0 SP3-Client-und Server Installationsprogrammen beschrieben, wenn .NET Framework 4.5.1, PowerShell 3,0 oder die GPMC in den Remote Server-Verwaltungs Tools fehlt.

| AGPM-Client            |                                                                                                 |                                                                            | AGPM-Server                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Betriebssystem       | .NET Framework                                                                                  | PowerShell                                                                 | Remoteserver-Verwaltungstools                                              | .NET Framework                                                                                  | Remoteserver-Verwaltungstools                                              |
| Windows 10             | Wenn .NET Framework 4.5.1 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation. | Wenn PowerShell 3,0 nicht installiert ist, blockiert das Installationsprogramm die Installation. | Wenn die GPMC nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation. | Wenn .NET Framework 4.5.1 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation. | Wenn die GPMC nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation. |
| Windows8.1            | Wenn .NET Framework 4.5.1 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation. | Wenn PowerShell 3,0 nicht installiert ist, blockiert das Installationsprogramm die Installation. | Wenn die GPMC nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation. | Wenn .NET Framework 4.5.1 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation. | Wenn die GPMC nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation. |
| Windows Server 2012 R2 | Wenn .NET Framework 4.5.1 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation. | Wenn PowerShell 3,0 nicht installiert ist, blockiert das Installationsprogramm die Installation. | Wenn die GPMC nicht aktiviert ist, wird Sie während der Installation von dem Installationsprogramm aktiviert.   | Wenn .NET Framework 4.5.1 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation. | Wenn die GPMC nicht aktiviert ist, wird Sie während der Installation von dem Installationsprogramm aktiviert.   |

 

## So erhalten Sie MDOP-Technologien


AGPM 4,0 SP3 ist Teil des Microsoft Desktop Optimization Pack (MDOP) seit MDOP 2015. MDOP ist Teil von Microsoft Software Assurance. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Verwandte Themen


[Advanced Group Policy Management](index.md)

[Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP3](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[Welche Version von AGPM zur Installation auswählen](choosing-which-version-of-agpm-to-install.md)

 

 





