---
title: Von DaRT 10 unterstützte Konfigurationen
description: Von DaRT 10 unterstützte Konfigurationen
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804751"
---
# Von DaRT 10 unterstützte Konfigurationen


In diesem Thema werden die Voraussetzungen für Software und unterstützte Konfigurationen angegeben, die zum Installieren und Ausführen von Microsoft Diagnostics and Recovery Toolset (Dart) 10 in Ihrer Umgebung erforderlich sind. Die Betriebssystemanforderungen und die Systemanforderungen, die für die Ausführung von DART 10 erforderlich sind, werden angegeben. Informationen zu den Voraussetzungen, die Sie beim Erstellen des DART-Wiederherstellungs Bilds beachten müssen, finden Sie unter [Planen der Erstellung des DART 10-Wiederherstellungs Bilds](planning-to-create-the-dart-10-recovery-image.md).

Informationen zu unterstützten Konfigurationen, die für spätere Versionen gelten, finden Sie in der Dokumentation zur jeweiligen Version.

Sie können Dart auf eine von zwei Arten installieren. Sie können alle Funktionen auf einem IT-Administratorcomputer installieren, in dem Sie alle Aufgaben ausführen, die mit der Ausführung von DART verbunden sind. Alternativ können Sie auf dem Administratorcomputer nur die Dart-Funktionalität installieren, die das Wiederherstellungsabbild erstellt, und dann die Funktionalität installieren, die zum Ausführen von DART (also der Dart-Remote Verbindungsanzeige) auf einem Helpdesk-Computer verwendet wird.

## Dart 10-Voraussetzungs Software


Stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind, bevor Sie Dart installieren.

### Voraussetzungen für Administrator Computer

In der folgenden Tabelle sind die Installationsvoraussetzungen für den Administratorcomputer aufgeführt, wenn Sie Dart 10 und alle Dart-Tools installieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzung</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Windows Assessment and Development Kit (ADK)</strong></p></td>
<td align="left"><p>Erforderlich für den Dart-Wiederherstellungsbild-Assistenten. Enthält die Bereitstellungs Tools, die verwendet werden, um Windows-Abbilder anzupassen, bereitzustellen und zu verwenden, und enthält die Windows-Vorinstallationsumgebung (Windows PE). Das ADK ist nicht erforderlich, wenn Sie nur den Remote Connection Viewer und/oder Crash Analyzer installieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows Development Kit oder Software Development Kit (optional)</strong></p></td>
<td align="left"><p>Für Crash Analyzer sind die Windows 10-Debugging-Tools aus dem Windows Driver Kit zum Analysieren von Speicherabbilddateien erforderlich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows 10 64-Bit-oder 32-Bit-ISO-Abbild</strong></p></td>
<td align="left"><p>Für Dart ist die Windows-Wiederherstellungsumgebung (Windows RE)-Abbild von Windows 10 Media erforderlich. Laden Sie die 32-Bit-oder 64-Bit-Version von Windows 10 herunter, je nach dem Typ des DART-Wiederherstellungs Bilds, das Sie erstellen möchten. Wenn Sie beide Systemtypen in Ihrer Umgebung unterstützen, laden Sie beide Versionen von Windows 10 herunter.</p></td>
</tr>
</tbody>
</table>

 

### Voraussetzungen für Helpdesk-Computer

In der folgenden Tabelle sind die Voraussetzungen für die Installation des Helpdesk-Computers aufgeführt, wenn Sie den Dart 10 Remote Connection Viewer ausführen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzung</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Dart 10-Remote Verbindungsanzeige</strong></p></td>
<td align="left"><p>Muss unter einem Windows 10-Betriebssystem installiert sein.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Debugging-Tools für Windows</strong></p></td>
<td align="left"><p>Nur erforderlich, wenn Sie das Crash Analyzer-Tool installieren</p></td>
</tr>
</tbody>
</table>

 

### Voraussetzungen für Endbenutzercomputer

Es gibt keine erforderliche Software, die auf Endbenutzercomputern installiert werden muss, außer dem Betriebssystem Windows 10.

## <a href="" id="---------dart-10-operating-system-requirements"></a> Dart 10-Betriebssystemanforderungen


### Systemanforderungen für Administrator Computer

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von DART 10-Administrator Computern unterstützt werden.

**Hinweis**  Stellen Sie sicher, dass Sie genügend Speicherplatz für alle zusätzlichen Tools zuweisen, die Sie auf dem Administratorcomputer installieren möchten.

 

**Hinweis**  Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
<th align="left">Betriebssystemanforderungen</th>
<th align="left">RAM-Anforderung für die Ausführung von Dart</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> Systemanforderungen für Dart-Helpdesk-Computer

Wenn Sie einem Helpdesk die Remote Behandlung von Computern gestatten, muss die Remote Verbindungsanzeige auf dem Helpdesk-Computer installiert sein. Sie können das Crash Analyzer-Tool optional auf dem Helpdesk-Computer installieren.

Dart 10 ermöglicht einem Helpdesk-Mitarbeiter, mithilfe des DART 7,0, Dart 8,0, Dart 8,1 oder Dart 10 Remote Connection Viewer eine Verbindung mit einem Dart 10-Computer herzustellen. Die Dart 7,0, Dart 8,0 und Dart 8,1, Remote Verbindungs-Viewer erfordern Windows 7-, Windows 8-oder Windows 8,1-Betriebssysteme, während die Dart 10-Remote Verbindungsanzeige Windows 10 erfordert. Die Dart 10-Remote Verbindungsanzeige und alle anderen Tools von DART 10 können nur auf einem Computer mit Windows 10 installiert werden.

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des DART-Helpdesk-Computers unterstützt werden.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
<th align="left">Betriebssystemanforderungen</th>
<th align="left">RAM-Anforderungen für die Ausführung von Dart</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows10 (nur mit Remote Connection Viewer 10,0)</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8 (nur mit Remote Connection Viewer 8,0)</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 (nur mit Remote Connection Viewer 7,0)</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64-Bit oder 32-Bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>n.v.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise, Rechenzentrum</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Standard, Enterprise, Rechenzentrum</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
</tbody>
</table>

 

DART verfügt auch über die folgenden Mindestanforderungen an die Hardware für den Endbenutzercomputer:

Ein CD-oder DVD-Laufwerk oder ein USB-Anschluss – nur erforderlich, wenn Sie Dart in Ihrem Unternehmen mit einer CD, DVD oder einem USB-Gerät bereitstellen.

BIOS-Unterstützung für das Starten des Computers von einer CD oder DVD, einem USB-Flashlaufwerk oder von einer Remote-oder Wiederherstellungspartition.

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> Dart 10 – Systemanforderungen für Endbenutzercomputer

Das Fenster Diagnose-und Wiederherstellungs-Toolset in DART 10 setzt voraus, dass der Endbenutzercomputer eines der folgenden Betriebssysteme zusammen mit dem angegebenen verfügbaren Speicherplatz für Dart verwendet:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
<th align="left">Betriebssystemanforderungen</th>
<th align="left">RAM-Anforderungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Planen der Bereitstellung von DaRT 10](planning-to-deploy-dart-10.md)

 

 





