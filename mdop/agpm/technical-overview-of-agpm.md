---
title: Technische Übersicht über AGPM
description: Technische Übersicht über AGPM
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807451"
---
# Technische Übersicht über AGPM


Microsoft Advanced Group Policy Management (AGPM) ist eine Client/Server-Anwendung. Der AGPM-Server speichert Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) offline in dem Archiv, das von AGPM im Dateisystem des Servers erstellt wird. Gruppenrichtlinienadministratoren verwenden das AGPM-Snap-in für die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC), um mit GPOs auf dem Server zu arbeiten, der das Archiv hostet. Das Verständnis der Teile von AGPM und verwandter Elemente, deren Speicherung von GPOs im Dateisystem und die Art und Weise, wie Berechtigungen die für jede Benutzerrolle verfügbaren Aktionen steuern, können die Effektivität von Gruppenrichtlinienadministratoren mit AGPM verbessern.

## Terminologie


Im folgenden werden die grundlegenden AGPM-Ausdrücke erläutert.

-   **AGPM-Client:** Einen Computer, auf dem das AGPM-Snap-in für die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) ausgeführt wird und von dem Gruppenrichtlinienadministratoren GPOs verwalten.

-   **AGPM-Snap-in:** Die Softwarekomponente von AGPM, die auf AGPM-Clients installiert ist, damit Sie GPOs verwalten können.

-   **AGPM-Server:** Ein Server, der den AGPM-Dienst ausführt und ein Archiv verwaltet. Jeder AGPM-Server kann nur ein Archiv verwalten, aber ein AGPM-Server kann Archivdaten für mehrere Domänen in einem Archiv verwalten. Ein Archiv kann auf einem anderen Computer als einem AGPM-Server gehostet werden.

-   **AGPM-Dienst:** Die Softwarekomponente von AGPM, die auf einem AGPM-Server als Dienst ausgeführt wird. Der Dienst verwaltet GPOs im Archiv und in der Produktionsumgebung in dieser Gesamtstruktur.

-   **Archivieren:** In AGPM handelt es sich um einen zentralen Speicher, der die gesteuerten GPOs enthält, die der zugeordnete AGPM-Server zusätzlich zum Verlauf für jedes dieser GPOs verwaltet. Dazu gehören alle vorherigen kontrollierten Versionen der einzelnen Gruppenrichtlinienobjekte. Ein Archiv besteht aus einer Archivindexdatei und zugehörigen Archivdaten, die Daten für GPOs in mehreren Domänen enthalten können. Ein Archiv kann auf einem anderen Computer als einem AGPM-Server gehostet werden.

-   **Gesteuertes Gruppenrichtlinienobjekt:** Ein GPO, das von AGPM verwaltet wird. AGPM verwaltet das Protokoll und die Berechtigungen für gesteuerte GPOs, die im Archiv gespeichert werden.

-   **Ungesteuertes Gruppenrichtlinienobjekt:** Ein GPO in der Produktionsumgebung für eine Domäne, das nicht von AGPM verwaltet wird.

## Was AGPM installiert, erstellt und beeinflusst


Auf einem AGPM-Server installiert das AGPM-Setup Programm den AGPM-Dienst. AGPM ändert den Active Directory®-Verzeichnisdienst oder das Schema nicht. Standardmäßig werden die AGPM-Server-Programmdateien in%ProgramFiles%\\Microsoft\\AGPM\\Server. installiert. Sie können den AGPM-Dienst auf einem Domänencontroller installieren, wenn dies der Fall ist. Es wird jedoch empfohlen, den AGPM-Dienst auf einem Mitgliedsserver zu installieren.

Auf einem AGPM-Client installiert das AGPM-Setup Programm das AGPM-Snap-in und fügt jeder Domäne, die in der GPMC angezeigt wird, einen Ordner zum **Ändern des Steuerelements** hinzu. Standardmäßig werden die AGPM-Client Programmdateien in%ProgramFiles%\\Microsoft\\AGPM\\Client. installiert.

Tabelle 1 beschreibt sowohl die Elemente, die AGPM installiert oder erstellt, als auch die Teile des Betriebssystems, die sich auf den AGPM-Vorgang auswirken.

**Tabelle 1: installierte, erstellte oder von AGPM betroffene Elemente**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Element</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AGPM-Dienst</p></td>
<td align="left"><p>Der AGPM-Dienst wird auf dem AGPM-Server ausgeführt. Der Dienst verwaltet das Archiv, das Offline-GPOs enthält, und gesteuerte GPOs in der Produktionsumgebung. Die Standardkonfiguration des AGPM-Diensts lautet wie folgt:</p>
<ul>
<li><p><strong>Dienstname: </strong> AGPM-Dienst</p></li>
<li><p><strong>Anzeigename: </strong> AGPM-Dienst</p></li>
<li><p><strong>Pfad zur ausführbaren Datei: </strong> % Programme% \Microsoft\AGPM\Server\Agpm.exe</p></li>
<li><p><strong>Start: </strong> automatisch</p></li>
<li><p><strong>Melden Sie sich als: </strong> AGPM-Dienstkonto an, das während der Installation von AGPM Server angegeben wurde und die mithilfe von <strong> Programmen und Funktionen </strong> in der Systemsteuerung geändert werden kann <strong> </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>AGPM-Archiv</p></td>
<td align="left"><p>Standardmäßig erstellt AGPM das Archiv in%ProgramData%\Microsoft\AGPM auf dem AGPM-Server. Das Archiv bietet Speicher für Offline-GPOs und kann mehrere Versionen der einzelnen Gruppenrichtlinienobjekte speichern. Änderungen, die AGPM an GPOs im Archiv vornimmt, haben keinen Einfluss auf die Produktionsumgebung, bis ein AGPM-Administrator oder eine genehmigende Person das Gruppenrichtlinienobjekt in der Produktionsumgebung bereitstellt und das Gruppenrichtlinienobjekt mit einer Organisationseinheit verknüpft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows-Firewall</p></td>
<td align="left"><p>Während der Installation aktiviert AGPM eine eingehende Windows-Firewall-Regel, die es dem AGPM-Client ermöglicht, mit dem AGPM-Server zu kommunizieren. Die standardmäßige Windows-Firewall-Regel lautet wie folgt:</p>
<ul>
<li><p><strong>Name: </strong> AGPM-Dienst</p></li>
<li><p><strong>Aktion: </strong> Zulassen der Verbindung</p></li>
<li><p><strong>Programme: </strong> Alle Programme, die den angegebenen Bedingungen entsprechen</p></li>
<li><p><strong>Protokolltyp: </strong> TCP</p></li>
<li><p><strong>Lokaler Port: </strong> 4600</p></li>
<li><p><strong>Remote-Port: </strong> alle Ports</p></li>
<li><p><strong>Lokale IP-Adresse: </strong> Any</p></li>
<li><p><strong>Remote-IP-Adresse: </strong> Any</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>E-Mail-Server</p></td>
<td align="left"><p>AGPM verwendet SMTP (Simple Mail Transfer Protocol) zum Senden von e-Mail-Anforderungen an die Adressen, die auf der <strong> Registerkarte Domänendelegierung konfiguriert sind </strong> . Wenn ein Editor beispielsweise anfordert, dass ein neues Gruppenrichtlinienobjekt erstellt wird, benachrichtigt AGPM jede e-Mail-Adresse, die auf der <strong> Registerkarte "Domänendelegierung" angegeben ist </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AGPM-Snap-in</p></td>
<td align="left"><p>Das AGPM-Snap-in für die GPMC wird auf AGPM-Clients ausgeführt und von Gruppenrichtlinienadministratoren zum Verwalten von GPOs verwendet. Das Snap-in wird in der GPMC als <strong> Ordner für die Änderungssteuerung </strong> in jeder Domäne angezeigt.</p></td>
</tr>
</tbody>
</table>

 

### Weitere Verweise

Weitere Informationen zu den von AGPM installierten Dateien finden Sie im [Planungshandbuch für AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).

## Archiv


Standardmäßig erstellt der AGPM-Server Installationsvorgang das Archiv auf der lokalen Festplatte des AGPM-Servers unter%ProgramData%\\Microsoft\\AGPM. Sie können den Pfad jedoch während der Installation ändern und sogar das Archiv auf einem anderen Server als dem AGPM-Server erstellen.

Das Archiv enthält einen Unterordner für jede Version jedes GPO, das im Archiv enthalten ist. Der Name jedes Unterordners ist eine GUID, die eine Version des Gruppenrichtlinienobjekts identifiziert.

Die gpostate.xml-Datei zeichnet den Status der einzelnen Gruppenrichtlinienobjekte im Archiv auf. Die Datei ist ein Manifest, das den Inhalt des Archivs beschreibt. Beispielsweise kann ein GPO viele Versionen aufweisen, und jede Version befindet sich in einem eigenen Unterordner im Archiv. Die gpostate.xml-Datei gibt an, welche Unterordner verschiedene Versionen eines einzelnen Gruppenrichtlinienobjekts enthalten. Darüber hinaus weisen GPO-Vorlagen Unterordner im Archiv auf, gpostate.xml aber darauf hinweisen, dass es sich um Vorlagen und nicht um gesteuerte GPOs handelt. Wenn Gruppenrichtlinien-Administratoren GPOs löschen, ändert AGPM ihre Status in gpostate.xml, um anzugeben, dass Sie sich im **Papierkorb** befinden, aber die Unterordner der GPOs nicht aus dem Archiv entfernen.

**Vorsicht**  Bearbeiten Sie gpostate.xml oder die GPOs, die das Archiv enthält, nicht manuell. Diese Informationen werden nur bereitgestellt, um das Verständnis des AGPM-Archivs zu verbessern. Verwenden Sie stattdessen das AGPM-Snap-in, um GPOs zu ändern.

 

Wenn AGPM das Archiv erstellt, erhält er Vollzugriff auf System, Administratoren und das AGPM-Dienstkonto (angegeben im Setup von AGPM Server). Durch das Ändern von Berechtigungen mithilfe der AGPM-Benutzeroberfläche im AGPM-Snap-in werden die Berechtigungen für das Archiv nicht geändert, da das AGPM-Dienstkonto alle Vorgänge im Auftrag des angemeldeten Benutzers ausführt.

### Weitere Verweise

Informationen dazu, wie Sie das Archiv sichern, das Archiv aus einer Sicherung wiederherstellen oder sowohl den AGPM-Server als auch das Archiv verschieben, finden Sie im Abschnitt "Ausführen von AGPM-Administrator Aufgaben" im [Betriebshandbuch für AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).

## Rollen und Berechtigungen


Rollen vereinfachen die Delegierung. Anstatt den Gruppenrichtlinienadministratoren detaillierte Berechtigungen zuzuweisen, können AGPM-Administratoren Gruppenrichtlinienadministratoren eine von vier Rollen zuweisen, damit diese Aufgaben im Zusammenhang mit dieser Rolle ausführen können:

-   **AGPM-Administrator:** Gruppenrichtlinienadministratoren, denen die Rolle AGPM-Administrator (Vollzugriff) zugewiesen ist, können beliebige Aufgaben in AGPM ausführen. AGPM-Administratoren können domänenweite Optionen konfigurieren und Berechtigungen an andere Gruppenrichtlinienadministratoren delegieren.

-   **Genehmigende Person:** Gruppenrichtlinienadministratoren, denen die genehmigende Rolle zugewiesen ist, können GPOs für eine Domäne in der Produktionsumgebung bereitstellen. Genehmigende Personen können auch GPOs erstellen und löschen sowie Anforderungen von Editoren genehmigen oder ablehnen. Genehmigende Personen können die Liste der GPOs in einer Domäne anzeigen, die Richtlinieneinstellungen in GPOs anzeigen sowie Berichte zu den Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt erstellen und anzeigen. Sie können die Richtlinieneinstellungen nicht in GPOs bearbeiten, es sei denn, Ihnen wird auch die Rolle "Editor" zugewiesen.

-   **Editor:** Gruppenrichtlinienadministratoren, denen die Editor Rolle zugewiesen ist, können die Liste der GPOs in einer Domäne anzeigen, die Richtlinieneinstellungen in GPOs anzeigen, die Richtlinieneinstellungen in GPOs bearbeiten sowie Berichte über die Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt erstellen und anzeigen. Wenn Sie nicht auch der Rolle genehmigende Person zugewiesen sind, können die Bearbeiter keine GPOs erstellen, bereitstellen oder löschen. Sie können jedoch anfordern, dass GPOs erstellt, bereitgestellt oder gelöscht werden.

-   **Bearbeiter:** Gruppenrichtlinienadministratoren, denen die Prüferrolle zugewiesen ist, können die Liste der GPOs in einer Domäne anzeigen und Berichte zu den Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt erstellen und anzeigen. Sofern Ihnen nicht auch die Rolle des Editors zugewiesen ist, können Sie die Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt nicht bearbeiten.

AGPM bietet AGPM-Administratoren die Flexibilität, Berechtigungen mit dem AGPM-Snap-in auf einer detaillierteren Ebene als Rollen zu konfigurieren. Tabelle 2 beschreibt diese Berechtigungen und gibt die Berechtigungen an, die den einzelnen Rollen standardmäßig gewährt werden.

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
<th align="left">Berechtigung</th>
<th align="left">Beschreibung</th>
<th align="left">AGPM-Administrator</th>
<th align="left">Genehmiger</th>
<th align="left">Editor</th>
<th align="left">Prüfer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Vollzugriff</strong></p></td>
<td align="left"><p>Über alle Berechtigungen verfügen.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Erstellen eines GPO</strong></p></td>
<td align="left"><p>Erstellen von GPOs in einer Domäne</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Listeninhalt</strong></p></td>
<td align="left"><p>Listen Sie die GPOs in einer Domäne auf.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Leseeinstellungen</strong></p></td>
<td align="left"><p>Lesen Sie die Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Bearbeiten von Einstellungen</strong></p></td>
<td align="left"><p>Ändern Sie die Richtlinieneinstellungen in einem Gruppenrichtlinienobjekt.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Gruppenrichtlinienobjekt löschen</strong></p></td>
<td align="left"><p>Löschen eines Gruppenrichtlinienobjekts</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Ändern der Sicherheit</strong></p></td>
<td align="left"><p>Delegieren Sie den Zugriff auf Domänenebene, delegieren Sie den Zugriff auf ein einzelnes GPO, und delegieren Sie den Zugriff auf die Produktionsumgebung.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Bereitstellen von Gruppenrichtlinienobjekten</strong></p></td>
<td align="left"><p>Stellen Sie ein GPO aus dem Archiv in der Produktionsumgebung bereit.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Erstellen einer Vorlage</strong></p></td>
<td align="left"><p>Erstellen einer GPO-Vorlage in AGPM</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Optionen ändern</strong></p></td>
<td align="left"><p>Konfigurieren Sie die AGPM-e-Mail-Benachrichtigung, und begrenzen Sie die im Archiv gespeicherten Versionen von Gruppenrichtlinienobjekten.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Exportieren von Gruppenrichtlinienobjekten</strong></p></td>
<td align="left"><p>Exportieren eines Gruppenrichtlinienobjekts in eine Datei</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Importieren von Gruppenrichtlinienobjekten</strong></p></td>
<td align="left"><p>Importieren Sie ein GPO aus einer Datei.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Hinweis** 
 Berechtigungen zum **Exportieren von Gruppenrichtlinienobjekten** und zum **Importieren von Gruppenrichtlinienobjekten** stehen in AGPM 3,0 oder 2,5 nicht zur Verfügung.

Die Möglichkeit, den Zugriff auf GPOs in der Produktionsumgebung für eine Domäne zu delegieren, und die Möglichkeit, die Anzahl der gespeicherten GPO-Versionen zu begrenzen, sind in AGPM 2,5 nicht verfügbar.

 

### Weitere Verweise

Informationen dazu, welche Aufgaben von Gruppenrichtlinienadministratoren ausgeführt werden können, denen eine bestimmte Rolle zugewiesen wurde oder über welche Berechtigungen zum Ausführen einer bestimmten Aufgabe erforderlich sind, finden Sie im [Betriebshandbuch für AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).

 

 





