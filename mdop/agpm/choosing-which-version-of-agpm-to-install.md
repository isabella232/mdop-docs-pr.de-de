---
title: Welche Version von AGPM zur Installation auswählen
description: Welche Version von AGPM zur Installation auswählen
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: f8a69fb323d9f47c5b906ac3abc6ec59376ee6f7
ms.sourcegitcommit: 0a7dee11289780336d9c24ebbf27c5c1ffee441c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/04/2020
ms.locfileid: "10905602"
---
# Welche Version von AGPM zur Installation auswählen


Jede Version von MicrosoftAdvanced Group Policy Management (AGPM) unterstützt bestimmte Versionen des Windows-Betriebssystems. Wir empfehlen dringend, dass Sie den AGPM-Client und AGPM-Server auf der gleichen Betriebssystem Zeile ausführen. Beispiel: Windows 10 mit Windows Server 2016, Windows 8.1 mit Windows Server2012 R2 usw.

Wir empfehlen, den AGPM-Server unter der neuesten Version des Betriebssystems in der Domäne zu installieren. AGPM verwendet die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) zum Sichern und Wiederherstellen von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs). Da neuere Versionen der GPMC zusätzliche Richtlinieneinstellungen bereitstellen, die in früheren Versionen nicht verfügbar sind, können Sie weitere Richtlinieneinstellungen mithilfe der neuesten Version des Betriebssystems verwalten.

In allen Versionen von AGPM können nur die Richtlinieneinstellungen verwaltet werden, die in der gleichen Version oder einer früheren Version des Betriebssystems, auf dem AGPM ausgeführt wird, eingeführt wurden. Wenn Sie beispielsweise AGPM 4.0 SP2 unter Windows Server 2012 installieren, können Sie Richtlinieneinstellungen verwalten, die in Windows Server 2012 oder früher eingeführt wurden, Sie können jedoch keine Richtlinieneinstellungen verwalten, die später in Windows 8.1 oder Windows Server2012 R2 eingeführt wurden.

Wenn die Version der GPMC auf dem AGPM-Server älter als die Version auf den Computern ist, die von Administratoren zum Verwalten von Gruppenrichtlinien verwendet werden, kann der AGPM-Server keine Richtlinieneinstellungen speichern, die in der älteren Version der GPMC nicht verfügbar sind. Eine Tabelle mit den Gruppenrichtlinieneinstellungen in Windows finden Sie unter [Referenz zu Gruppenrichtlinieneinstellungen für Windows und Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).

## AGPM 4.0 SP3


Wenn Sie Computer, auf denen Windows 10 ausgeführt wird, zum Verwalten von GPOs verwenden, müssen Sie AGPM 4,0 SP3 verwenden. Frühere Versionen von AGPM können auf Computern, auf denen das Betriebssystem Windows 10 ausgeführt wird, nicht installiert werden.

Tabelle 1 listet die Betriebssysteme auf, auf denen Sie AGPM 4.0 SP3 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 SP3 verwalten können.

**Tabelle 1: AGPM 4,0 SP3 unterstützte Betriebssysteme und Richtlinieneinstellungen**

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
<td align="left"><p>Windows Server 2019 oder Windows 10</p></td>
<td align="left"><p>Windows Server 2019 oder Windows 10</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
 <tr class="even">
<td align="left"><p>Windows Server 2019 oder Windows 10</p></td>
<td align="left"><p>Windows Server 2019 oder Windows 10</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="edd">
<td align="left"><p>Windows Server2012 R2</p></td>
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Unterstützt durch die in KB 4015786 beschriebenen Einschränkungen <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"></a>
</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2 oder Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 oder Windows 8.1</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 oder Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 oder Windows 8,1</p></td>
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
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 oder Windows7</p></td>
<td align="left"><p>Nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, jedoch können keine Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, gemeldet oder bearbeitet werden</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP2


Wenn Sie Computer, auf denen Windows Server2012 R2 oder Windows 8.1 ausgeführt wird, zum Verwalten von GPOs verwenden, müssen Sie AGPM 4.0 SP2 verwenden. Frühere Versionen von AGPM können auf Computern, auf denen diese Betriebssysteme ausgeführt werden, nicht installiert werden.

Tabelle 1 listet die Betriebssysteme auf, auf denen Sie AGPM 4.0 SP2 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 SP2 verwalten können.

**Tabelle 2: von AGPM 4.0 SP2 unterstützte Betriebssysteme und Richtlinieneinstellungen**

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
<td align="left"><p>Windows Server2012 R2 oder Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 oder Windows 8.1</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 oder Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 oder Windows 8,1</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit Service Pack 1 (SP1)</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, jedoch können keine Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, gemeldet oder bearbeitet werden</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP1


In Tabelle 2 sind die Betriebssysteme aufgelistet, auf denen Sie AGPM 4,0 SP1 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 SP1 verwalten können.

**Tabelle 3: von AGPM 4.0 SP1 unterstützte Betriebssysteme und Richtlinieneinstellungen**

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
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8,1 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht gemeldet oder bearbeitet werden</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0


In Tabelle 3 sind die Betriebssysteme aufgeführt, auf denen Sie AGPM 4,0 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 verwalten können.

**Tabelle 4: von AGPM 4.0 unterstützte Betriebssysteme und Richtlinieneinstellungen**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Unterstützte Betriebssysteme für den AGPM-Server</th>
<th align="left">Unterstützte Betriebssysteme für den AGPM-Client</th>
<th align="left">AGPM-Unterstützung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht gemeldet oder bearbeitet werden</p></td>
</tr>
</tbody>
</table>

 

## Versionen von AGPM, die einem AGPM 4.0 vorausgehen


Tabelle 4 listet die Betriebssysteme auf, auf denen Sie die Versionen von AGPM installieren können, die AGPM 4.0 vorangestellt sind. Wenn ein Betriebssystem nicht aufgeführt ist, können Sie AGPM auf diesem Betriebssystem nicht installieren.

**Tabelle 5: Unterstützte Betriebssysteme für Versionen von AGPM, die AGPM 4.0 vorausgehen**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Version von AGPM, die installiert werden kann</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>3.0</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista mit SP1</p></td>
<td align="left"><p>3.0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Vista ohne installiertes Service Pack (32-Bit)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 (32-Bit)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
</tbody>
</table>

 

## So erhalten Sie MDOP-Technologien


AGPM 4,0 SP2 ist Teil des Microsoft Desktop Optimization Pack (MDOP). MDOP ist Teil von Microsoft Software Assurance. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Verwandte Themen


[Advanced Group Policy Management](index.md)

 

 





