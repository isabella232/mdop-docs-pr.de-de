---
title: Neuigkeiten in AGPM 4.0 SP2
description: Neuigkeiten in AGPM 4.0 SP2
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807391"
---
# Neuigkeiten in AGPM 4.0 SP2


Dieser Inhalt beschreibt Verbesserungen und unterstützte Konfigurationen für Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack2 (SP2). Wenn es einen Unterschied zwischen diesem Inhalt und anderer AGPM-Dokumentation gibt, sollten Sie diesen Inhalt als autorisierend ansehen und davon ausgehen, dass er die andere Dokumentation ersetzt.

## <a href="" id="what-s-new"></a>Neuigkeiten 


AGPM 4.0 SP2 unterstützt die folgenden Features und Funktionen.

### Unterstützung für Windows 8.1 und Windows Server2012 R2

AGPM 4.0 SP2 bietet Unterstützung für die Windows 8.1-und Windows Server2012 R2-Betriebssysteme.

### Neue und geänderte clientseitige Erweiterungen

Clientseitige Gruppenrichtlinienerweiterungen wurden hinzugefügt oder geändert, damit AGPM neue Richtlinieneinstellungen in Windows 8.1 unterstützt. Mithilfe dieser Richtlinieneinstellungen können Gruppenrichtlinienadministratoren Windows 8.1-spezifische Richtlinieneinstellungen verwalten und nachvollziehen, die zwischen zwei Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) oder Vorlagen geändert werden. Verwenden Sie zum Anzeigen der clientseitigen Erweiterungen die im AGPM-Client verfügbaren Einstellungen und Differenz Berichte.

Die neuen und geänderten Gruppenrichtlinien-clientseitigen Erweiterungen lauten wie folgt:

-   **Geben Sie die Einstellungen für Arbeitsordner an**. Wenn Sie diese Richtlinieneinstellung aktivieren, können IT-Administratoren Arbeitsordner so konfigurieren, dass Sie automatisch erstellt werden. Das Feature "Arbeitsordner" ermöglicht es Endbenutzern, Dateien von Ihren Windows-Desktopgeräten mit ihren anderen Geräten zu synchronisieren. Verwenden Sie diese Richtlinieneinstellung, um die Synchronisierungsbeziehung auf den Geräten eines Endbenutzers zu erstellen und zu konfigurieren, wie der Dateiserver identifiziert wird, in dem die Arbeitsordner des Benutzers gespeichert sind. Wenn Sie das Kontrollkästchen **Synchronisierung automatisch bereit** stellen aktivieren, wird die Synchronisierungspartnerschaft ohne Benutzereingabe erstellt, und die Daten werden automatisch mit dem Gerät des Benutzers synchronisiert. Wenn Sie das Kontrollkästchen **Synchronisierung automatisch bereit** stellen nicht aktivieren, müssen die Benutzereingaben angeben, um die Synchronisierung zu starten.

-   **Erzwingen der automatischen Einrichtung für alle Benutzer** Wenn Sie diese Richtlinieneinstellung aktivieren, können IT-Administratoren ermitteln, ob die Arbeitsordner Partnerschaft automatisch auf Endbenutzergeräten ohne Eingabe von Endbenutzern erstellt werden soll. Wenn Sie diese Richtlinieneinstellung aktivieren, wird die Synchronisierung so eingerichtet, wie Sie die Richtlinieneinstellung " **Arbeitsordner angeben** " konfigurieren. Wenn Sie die Richtlinieneinstellung " **automatische Einrichtung für alle Benutzer erzwingen** " auf " **deaktiviert** " oder " **nicht konfiguriert**" festlegen, wird die Partnerschaft "Arbeitsordner" entsprechend der Festlegung der Option für die **automatische Bereitstellung** in der Richtlinieneinstellung für die **Einstellungen für Arbeitsordner** festlegen konfiguriert.

Weitere Informationen zum Feature "Arbeitsordner" finden Sie unter [Übersicht über Arbeitsordner](https://go.microsoft.com/fwlink/?LinkId=330444).

### Kundenfeedback und Hotfix-Rollup

AGPM 4.0 SP2 enthält ein Rollup von Hotfixes, um Probleme zu beheben, die seit der Version AGPM 4.0 Service Pack1 (SP1) gefunden wurden. AGPM 4.0 SP2 enthält die neuesten Fixes bis einschließlich Microsoft Advanced Group Policy Management 4.0 SP1-Hotfix1. Weitere Informationen finden Sie im Knowledge Base-Artikel [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).

### Neue Gruppenrichtlinienerweiterungen in Einstellungen und Unterschiedsberichten

Die neuen Gruppenrichtlinienerweiterungen wurden zu den Einstellungen und Unterschiedsberichten hinzugefügt.

### Änderungen und Support für das Installationsprogramm

Die Änderungen und Unterstützung für das AGPM 4.0 SP2-Installationsprogramm sind:

-   Wenn Sie AGPM 4.0 SP2 unter dem BetriebssystemWindows 8 oder Windows Server 2012 oder höher installieren, überprüft das AGPM-Installationsprogramm, ob die erforderliche erforderliche Software (die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) und Microsoft .NET Framework 3.5) installiert ist. Wenn diese erforderliche Software nicht installiert ist, ist die Installation von AGPM 4.0 SP2 blockiert.

-   Wenn Sie den AGPM-Server installieren, werden die WCF-Aktivierung, die nicht-HTTP-Aktivierung und der Windows-Prozessaktivierungsdienst automatisch aktiviert.

-   Laden Sie auf dem Windows Vista-Clientbetriebssystem und neueren Betriebssystemen die entsprechende Version der Remote System-Verwaltungs Tools für Ihr Betriebssystem herunter, bevor Sie AGPM 4.0 SP2 installieren.

-   AGPM 4.0 SP2 unterstützt die Abwärtskompatibilität mit älteren unterstützten Betriebssystemen.

### Möglichkeit zum Upgrade auf AGPM 4.0 SP2 ohne erneutes Eingeben von Konfigurationsparametern

Sie können den AGPM-Client oder AGPM-Server auf AGPM 4.0 SP2 aktualisieren, ohne dazu aufgefordert zu werden, die Konfigurationsparameter (so genannte Smart Upgrade) nur von AGPM 4.0 weiter einzugeben, wie in der folgenden Tabelle dargestellt. Wenn Sie von anderen Versionen von AGPM auf AGPM 4.0 SP2 aktualisieren, wie in der Tabelle gezeigt, müssen Sie das klassische Upgrade verwenden, das eine erneute Eingabe der Konfigurationsparameter erfordert. Da jede Version von AGPM einem bestimmten Betriebssystem zugeordnet ist, lesen Sie [Auswählen der zu installierenden AGPM-Version](https://go.microsoft.com/fwlink/?LinkId=254350) , und stellen Sie sicher, dass Sie das Betriebssystem entsprechend aktualisieren, bevor Sie AGPM aktualisieren.

**Unterstützte Upgrades für AGPM 4,0 SP2**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>AGPM-Version, auf der Sie ein Upgrade durchführen können</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3.0</strong></p></td>
<td align="left"><p><strong>4.0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
<td align="left"><p><strong>4,0 SP2</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Klassisches Upgrade</p></td>
<td align="left"><p>Klassisches Upgrade</p></td>
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
</tr>
<tr class="even">
<td align="left"><p>4.0</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
<td align="left"><p>Nicht anwendbar</p></td>
<td align="left"><p>Nicht verfügbar</p></td>
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
</tr>
</tbody>
</table>

 

## Unterstützte Konfigurationen


AGPM 4.0 SP2 unterstützt die Konfigurationen in der folgenden Tabelle. Obwohl AGPM Gemischte Konfigurationen unterstützt, wird dringend empfohlen, den AGPM-Client und AGPM-Server auf derselben Betriebssystem Zeile auszuführen, beispielsweise Windows 8.1 mit Windows Server2012 R2, Windows 8 mit Windows Server 2012 usw.

**AGPM 4.0 SP2 unterstützte Betriebssysteme und Richtlinieneinstellungen**

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
<td align="left"><p>Windows Server2012 R2, Windows Server 2012, Windows 8.1 oder Windows 8</p></td>
<td align="left"><p>Windows Server 2012 oder Windows 8</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur unter Windows 8.1 oder Windows 8 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 oder Windows7</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit Service Pack 1 (SP1)</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 oder Windows7 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 oder Windows7</p></td>
<td align="left"><p>Nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, jedoch können keine Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 oder Windows7 vorhanden sind, gemeldet oder bearbeitet werden</p></td>
</tr>
</tbody>
</table>

 

## Voraussetzungen für die Installation von AGPM 4.0 SP2


In der folgenden Tabelle wird das Verhalten von AGPM 4.0 SP2-Client-und Server-Installationsprogrammen unter Windows 8.1 beschrieben, wenn .NET Framework 3.5 oder die GPMC in den Remote Server-Verwaltungs Tools nicht vorhanden ist.

**AGPM-Client**

**AGPM-Server**

**Betriebssystem**

**.NET Framework**

**Remoteserver-Verwaltungstools**

**.NET Framework**

**Remoteserver-Verwaltungstools**

**Windows 8.1**

Wenn .NET Framework 3.5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.

Wenn die GPMC nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.

Wenn .NET Framework 3.5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.

Wenn die GPMC nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.

**Windows Server2012 R2**

Wenn .NET Framework 3.5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.

Wenn die GPMC nicht aktiviert ist, wird Sie während der Installation von dem Installationsprogramm aktiviert.

Wenn .NET Framework 3.5 nicht aktiviert oder installiert ist, blockiert das Installationsprogramm die Installation.

Wenn die GPMC nicht aktiviert ist, wird Sie während der Installation von dem Installationsprogramm aktiviert.

 

## So erhalten Sie MDOP-Technologien


AGPM 4,0 SP2 ist Teil des Microsoft Desktop Optimization Pack (MDOP). MDOP ist Teil von Microsoft Software Assurance. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Verwandte Themen


[Advanced Group Policy Management](index.md)

[Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP2](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[Welche Version von AGPM zur Installation auswählen](choosing-which-version-of-agpm-to-install.md)

 

 





