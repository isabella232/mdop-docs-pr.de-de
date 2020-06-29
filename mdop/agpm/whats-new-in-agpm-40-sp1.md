---
title: Neuigkeiten in AGPM 4.0 SP1
description: Neuigkeiten in AGPM 4.0 SP1
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807392"
---
# Neuigkeiten in AGPM 4.0 SP1


Dieser Inhalt "Neuerungen" beschreibt Verbesserungen und unterstützte Konfigurationen für Microsoft Advanced Group Policy Management (AGPM) 4,0 SP1. Wenn es einen Unterschied zwischen diesem Inhalt und einer anderen AGPM-Dokumentation gibt, sollte dieser Inhalt als autorisierend gelten und den in diesem Produkt enthaltenen Inhalt ersetzen.

## <a href="" id="what-s-new"></a>Neuigkeiten 


AGPM 4,0 SP1 unterstützt die folgenden Verbesserungen:

### Neue und geänderte clientseitige Erweiterungen

Für AGPM wurden Gruppenrichtlinien-clientseitige Erweiterungen (CSES) hinzugefügt oder geändert, um neue Gruppenrichtlinien in Windows 8 und Windows Server 2012 zu unterstützen. Mithilfe dieser Gruppenrichtlinien können Gruppenrichtlinienadministratoren Windows 8-spezifische Gruppenrichtlinieneinstellungen verwalten und nachvollziehen, die zwischen zwei Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) oder Vorlagen geändert werden. Sie können auch benutzerdefinierte GPOs mit Windows 8-spezifischen Einstellungen erstellen und die GPOs als Vorlage konfigurieren und speichern. Verwenden Sie zum Anzeigen Ihrer CSEs die Einstellungen und Differenz Berichte, die im AGPM 4,0 SP1-Client verfügbar sind.

Die neuen und geänderten Gruppenrichtlinien-clientseitigen Erweiterungen lauten wie folgt:

-   **Zentrale Zugriffsrichtlinie:** Ermöglicht Gruppenrichtlinienadministratoren, zentrale Zugriffsrichtlinien auf Gruppenrichtlinien Servern anzugeben, beispielsweise Dateiserver. Bei der zentralen Zugriffsrichtlinie handelt es sich um eine Autorisierungsrichtlinie, die durch ein GPO-Element angegeben und auf Richtlinienziele angewendet wird, um den zentralisierten Zugriff und die Steuerung von Ressourcen zu vereinfachen. Diese Richtlinien für den zentralen Zugriff müssen auf einem Gruppenrichtlinien-Clientcomputer in Active Directory konfiguriert sein. Eine Gruppenrichtlinie verteilt die Kenntnisse einer anwendbaren zentralen Zugriffsrichtlinie auf die Computer, die Sie erzwingen müssen.

-   **Richtlinienänderungen zur Namensauflösung:** Ermöglicht Gruppenrichtlinienadministratoren, Einstellungen für DNS-Sicherheit und DirectAccess auf DNS-Clientcomputern zu konfigurieren. Neue Registerkarten zum Konfigurieren von generischen DNS-Server Einstellungen und Codierungseinstellungen wurden hinzugefügt.

-   **Änderungen der Gruppenrichtlinieneinstellungen:** Fügt Unterstützung für die Konfiguration und Verwaltung von Internet Explorer 10-Einstellungen hinzu, die für Windows 8 hinzugefügt wurden.

-   **Remote Anwendungen und Desktop Verbindungen:** Ermöglicht Gruppenrichtlinienadministratoren die Angabe der Standard Verbindungs-URL, die für Remote Anwendungen und Desktop Verbindungen verwendet wird.

-   **Windows to go-Startoptionen:** Ermöglicht Gruppenrichtlinienadministratoren, zu konfigurieren, ob der Computer mit Windows to go gestartet wird, wenn ein USB-Gerät mit einem Windows to go-Arbeitsbereich verbunden ist.

-   **Windows to go-Optionen für den Ruhezustand:** Ermöglicht Gruppenrichtlinienadministratoren, zu konfigurieren, ob ein Computer den Ruhezustands Ruhezustand (S4) verwenden kann, wenn der Computer von einem Windows to go-Arbeitsbereich gestartet wird.

### Kundenfeedback und Hotfix-Rollup

AGPM 4,0 SP1 enthält ein Rollup mit Korrekturen zur Behebung von Problemen, die seit der AGPM 4,0-Version gefunden wurden. AGPM 4,0 SP1 enthält die neuesten Fixes bis einschließlich Microsoft Advanced Group Policy Management 4,0 Hotfix 1.

### Einstellungen und Differenz Berichte zeigen neue Gruppenrichtlinienerweiterungen an

Die neuen Gruppenrichtlinienerweiterungen wurden zu den Einstellungen und Unterschiedsberichten hinzugefügt.

### Änderungen und Support für das Installationsprogramm

Die Änderungen und Unterstützung für das AGPM 4,0 SP1-Installationsprogramm sind:

-   Wenn Sie AGPM 4,0 SP1 unter Windows 8 oder Windows Server 2012 installieren, überprüft das AGPM-Installationsprogramm, ob die erforderliche erforderliche Software (Gruppenrichtlinien-Verwaltungskonsole und .NET 3,5-Framework) installiert ist. Wenn diese Voraussetzungen nicht installiert sind, ist die Installation von AGPM 4,0 SP1 blockiert.

-   Wenn Sie AGPM 4,0 SP1 installieren, werden die WCF-Aktivierung, die nicht-HTTP-Aktivierung und der Windows-Prozessaktivierungsdienst automatisch aktiviert.

-   Laden Sie unter Windows Vista, Windows 7 und Windows 8-Clientbetriebssysteme die entsprechende Version des Remote System Administration Toolkit für Ihr Betriebs System herunter, bevor Sie AGPM 4,0 SP1 installieren.

-   Abwärtskompatibilität mit älteren unterstützten Betriebssystemen wird unterstützt.

### Möglichkeit zum Upgraden oder Aktualisieren auf AGPM 4,0 SP1 ohne erneutes Eingeben von Konfigurationsparametern

Sie können den AGPM-Client oder-Server nur von AGPM 4,0 auf AGPM 4,0 SP1 aktualisieren, ohne dazu aufgefordert zu werden, die Konfigurationsparameter erneut einzugeben (so genannte "Smart Upgrade"), wie in der folgenden Tabelle dargestellt. Wenn Sie ein Upgrade auf AGPM 4,0 SP1 aus anderen Versionen von AGPM durchführen, wie in der Tabelle gezeigt, müssen Sie das "klassische Upgrade" verwenden, bei dem Sie die Konfigurationsparameter erneut eingeben müssen. Da jede Version von AGPM einem bestimmten Betriebssystem zugeordnet ist, lesen Sie [auswählen, welche Version von AGPM installiert](https://go.microsoft.com/fwlink/?LinkId=254350)werden soll, und stellen Sie sicher, dass Sie vor dem Durchführen eines Upgrades Ihr Betriebssystem entsprechend aktualisieren.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>AGPM-Version, auf der Sie ein Upgrade durchführen können</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3.0</strong></p></td>
<td align="left"><p><strong>4.0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Nicht zutreffend</p></td>
<td align="left"><p>Klassisches Upgrade</p></td>
<td align="left"><p>Klassisches Upgrade</p></td>
<td align="left"><p>Die Installation ist blockiert</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3.0</p></td>
<td align="left"><p>Nicht zutreffend</p></td>
<td align="left"><p>Nicht zutreffend</p></td>
<td align="left"><p>Klassisches Upgrade</p></td>
<td align="left"><p>Die Installation ist blockiert</p></td>
</tr>
<tr class="even">
<td align="left"><p>4.0</p></td>
<td align="left"><p>Nicht zutreffend</p></td>
<td align="left"><p>Nicht zutreffend</p></td>
<td align="left"><p>Nicht zutreffend</p></td>
<td align="left"><p>Intelligentes Upgrade</p></td>
</tr>
</tbody>
</table>

 

## Unterstützte Konfigurationen


AGPM unterstützt die Konfigurationen in der folgenden Tabelle. Obwohl AGPM Gemischte Konfigurationen unterstützt, wird dringend empfohlen, dass Sie den AGPM-Client und Server unter derselben Betriebssystemfamilie ausführen, beispielsweise Windows 8 mit Windows Server 2012, Windows 7 mit Windows Server 2008 R2 usw.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Unterstützte Konfigurationen für AGPM 4,0 SP1-Server</strong></p></td>
<td align="left"><p><strong>Unterstützte Konfigurationen für AGPM 4,0 SP1-Client</strong></p></td>
<td align="left"><p><strong>Unterstützung für AGPM 4,0 SP1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8 oder Windows Server 2012</p></td>
<td align="left"><p>Windows 8 oder Windows Server 2012</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2 oder Windows 7</p></td>
<td align="left"><p>Windows Server 2008 R2 oder Windows 7</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2 oder Windows 7 oder Windows 8 oder Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server 2008 R2 oder Windows 7 oder Windows 8 vorhanden sind, können nicht bearbeitet werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server 2008 R2 oder Windows 7 oder Windows 8 oder Windows Server 2012</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server 2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server 2008 R2 oder Windows 7 oder Windows 8 vorhanden sind, können nicht gemeldet oder bearbeitet werden</p></td>
</tr>
</tbody>
</table>

 

## Voraussetzungen für die Installation von AGPM 4,0 SP1


In der folgenden Tabelle wird das Verhalten unter Windows 8 von AGPM 4,0 SP1-Client-und Server Installationsprogrammen beschrieben, wenn .NET 3,5 oder die Gruppenrichtlinien-Verwaltungskonsole in den Remote Server-Verwaltungs Tools (Remoteserver Administration Tools, Remoteserver-Verwaltungs Tools) fehlt.

**AGPM-Client 4,0 SP1**

**AGPM Server 4,0 SP1**

**Betriebssystem**

**.NET**

**RSAT**

**.NET**

**RSAT**

**Windows 8**

Wenn .NET 3,5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.

Wenn die GPMC nicht aktiviert oder auf dem System installiert ist, blockiert das Installationsprogramm die Installation.

Wenn .NET 3,5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.

Wenn die GPMC nicht aktiviert oder auf dem System installiert ist, blockiert das Installationsprogramm die Installation.

**Windows Server 2012**

Wenn .NET 3,5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.

Wenn die GPMC nicht aktiviert ist, wird Sie während der Installation von dem Installationsprogramm aktiviert.

Wenn .NET 3,5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.

Wenn die GPMC nicht aktiviert ist, wird Sie während der Installation von dem Installationsprogramm aktiviert.

 

## Verwandte Themen


[Advanced Group Policy Management](index.md)

[Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP1](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





