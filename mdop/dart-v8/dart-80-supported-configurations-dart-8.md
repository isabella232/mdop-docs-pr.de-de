---
title: Von DaRT 8.0 unterstützte Konfigurationen
description: Von DaRT 8.0 unterstützte Konfigurationen
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810249"
---
# Von DaRT 8.0 unterstützte Konfigurationen


In diesem Thema werden die Voraussetzungen für Software und unterstützte Konfigurationen angegeben, die erforderlich sind, um Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 in Ihrer Umgebung zu installieren und auszuführen. Die Betriebssystemanforderungen und die Systemanforderungen, die für die Ausführung von Dart 8,0 erforderlich sind, werden angegeben. Informationen zu den Voraussetzungen, die Sie beim Erstellen des DART-Wiederherstellungs Bilds beachten müssen, finden Sie unter [Planen der Erstellung des Dart 8,0-Wiederherstellungs Bilds](planning-to-create-the-dart-80-recovery-image-dart-8.md).

Informationen zu unterstützten Konfigurationen, die für spätere Versionen gelten, finden Sie in der Dokumentation zur jeweiligen Version.

Sie können Dart auf eine von zwei Arten installieren. Sie können alle Funktionen auf einem IT-Administratorcomputer installieren, in dem Sie alle Aufgaben ausführen, die mit der Ausführung von DART verbunden sind. Alternativ können Sie auf dem Administratorcomputer nur die Dart-Funktionalität installieren, die das Wiederherstellungsabbild erstellt, und dann die Funktionalität installieren, die zum Ausführen von DART (also der Dart-Remote Verbindungsanzeige) auf einem Helpdesk-Computer verwendet wird.

## <a href="" id="---------dart-8-0-prerequisite-software"></a> Dart 8,0-Voraussetzungs Software


Stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind, bevor Sie Dart installieren.

### Voraussetzungen für Administrator Computer

In der folgenden Tabelle sind die Installationsvoraussetzungen für den Administratorcomputer aufgeführt, wenn Sie Dart 8,0 und alle Dart-Tools installieren.

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
<td align="left"><p><strong>.NET Framework 4,5</strong></p></td>
<td align="left"><p>Erforderlich für den Dart-Wiederherstellungsbild-Assistenten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows Development Kit oder Software Development Kit (optional)</strong></p></td>
<td align="left"><p>Für Crash Analyzer sind die Windows 8-Debugging-Tools aus dem Windows Driver Kit zum Analysieren von Speicherabbilddateien erforderlich.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows 8 64-Bit ISO-Abbild</strong></p></td>
<td align="left"><p>Für Dart ist die Windows-Wiederherstellungsumgebung (Windows RE)-Abbild von Windows 8 Media erforderlich. Laden Sie die 32-Bit-oder 64-Bit-Version von Windows 8 herunter, je nach dem Typ des DART-Wiederherstellungs Bilds, das Sie erstellen möchten. Wenn Sie beide Systemtypen in Ihrer Umgebung unterstützen, laden Sie beide Versionen von Windows 8 herunter.</p></td>
</tr>
</tbody>
</table>

 

### Voraussetzungen für Helpdesk-Computer

In der folgenden Tabelle sind die Installationsvoraussetzungen für den Helpdesk-Computer aufgeführt, wenn Sie die Dart 8,0-Remote Verbindungsanzeige ausführen.

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
<td align="left"><p><strong>Dart 8,0-Remote Verbindungsanzeige</strong></p></td>
<td align="left"><p>Muss unter einem Windows 8-Betriebssystem installiert sein.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>NET Framework 4,5</strong></p></td>
<td align="left"><p>Erforderlich für den Dart-Wiederherstellungsbild-Assistenten</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Debugging-Tools für Windows</strong></p></td>
<td align="left"><p>Nur erforderlich, wenn Sie das Crash Analyzer-Tool installieren</p></td>
</tr>
</tbody>
</table>

 

### Voraussetzungen für Endbenutzercomputer

Es gibt keine erforderliche Software, die auf Endbenutzercomputern installiert werden muss, mit Ausnahme des Betriebssystems Windows 8.

## <a href="" id="---------dart-operating-system-requirements"></a> Dart-Betriebssystemanforderungen


### Systemanforderungen für Administrator Computer

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des DART-Administratorcomputers unterstützt werden.

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
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise, Rechenzentrum</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>512MB</p></td>
<td align="left"><p>1.0 GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> Systemanforderungen für Dart-Helpdesk-Computer

Wenn Sie einem Helpdesk die Remote Behandlung von Computern gestatten, muss die Remote Verbindungsanzeige auf dem Helpdesk-Computer installiert sein. Sie können das Crash Analyzer-Tool optional auf dem Helpdesk-Computer installieren.

Dart 8,0 ermöglicht einem Helpdesk-Mitarbeiter, mithilfe des DART 7,0-oder Dart 8,0-Remote Verbindungs-Viewers eine Verbindung mit einem Dart 8,0-Computer herzustellen. Die Dart 7,0-Remote Verbindungsanzeige erfordert ein Windows 7-Betriebssystem, während die Dart 8,0-Remote Verbindungsanzeige Windows 8 erfordert. Die Dart 8,0-Remote Verbindungsanzeige und alle anderen Dart 8,0-Tools können nur auf einem Computer mit Windows 8 installiert werden.

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
<td align="left"><p>51</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
</tbody>
</table>

 

DART verfügt auch über die folgenden Mindestanforderungen an die Hardware für den Endbenutzercomputer:

Ein CD-oder DVD-Laufwerk oder ein USB-Anschluss – nur erforderlich, wenn Sie Dart in Ihrem Unternehmen mit einer CD, DVD oder einem USB-Gerät bereitstellen.

BIOS-Unterstützung für das Starten des Computers von einer CD oder DVD, einem USB-Flashlaufwerk oder von einer Remote-oder Wiederherstellungspartition.

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> Systemanforderungen für Dart-Endbenutzercomputer

Das Fenster Diagnose-und Wiederherstellungs-Toolset in DART setzt voraus, dass der Endbenutzercomputer eines der folgenden Betriebssysteme zusammen mit dem angegebenen verfügbaren Speicherplatz für Dart verwendet:

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
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Alle Editionen</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>32 Bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise, Rechenzentrum</p></td>
<td align="left"><p>n.v.</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>512MB</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Planen der Bereitstellung von DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





