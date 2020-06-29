---
title: Planen der Kapazität für App-V 5.0
description: Planen der Kapazität für App-V 5.0
author: dansimp
ms.assetid: 56f48b00-cd91-4280-9481-5372a0e2e792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e828457a286f6f686c227a935828679514d87ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806038"
---
# Planen der Kapazität für App-V 5.0


Die folgenden Empfehlungen können als Basis für die Ermittlung der Kapazitäts Planungsinformationen verwendet werden, die für die App-V 5,0-Infrastruktur Ihrer Organisation geeignet sind.

**Wichtig**  Verwenden Sie die Informationen in diesem Abschnitt nur als Allgemeinen Leitfaden für die Planung Ihrer App-V 5,0-Bereitstellung. Die Anforderungen an die Systemkapazität hängen von den spezifischen Details Ihrer Hardware-und Anwendungsumgebung ab. Darüber hinaus sind die in diesem Dokument angezeigten Leistungsnummern Beispiele, und ihre Ergebnisse können variieren.

 

## Ermitteln des Projektumfangs


Bevor Sie die App-V 5,0-Infrastruktur entwerfen, müssen Sie den Projektbereich ermitteln. Der Bereich besteht darin, zu ermitteln, welche Anwendungen virtuell verfügbar sind, und um auch die Zielbenutzer und deren Speicherorte zu identifizieren. Mithilfe dieser Informationen können Sie ermitteln, welche Art von App-V 5,0-Infrastruktur implementiert werden soll. Entscheidungen bezüglich des Projektumfangs müssen auf den spezifischen Anforderungen Ihrer Organisation basieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ermitteln des Anwendungsbereichs</p></td>
<td align="left"><p>Je nachdem, welche Anwendungen virtualisiert werden sollen, kann die App-V 5,0-Infrastruktur auf unterschiedliche Weise eingerichtet werden. Die erste Aufgabe besteht darin, zu definieren, welche Anwendungen virtualisiert werden sollen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bestimmen des Positions Bereichs</p></td>
<td align="left"><p>Der Speicherort Bereich bezieht sich auf die physischen Standorte (beispielsweise unternehmensweit oder einen bestimmten geografischen Standort), in denen Sie die virtualisierten Anwendungen ausführen möchten. Sie kann sich auch auf die Benutzerpopulation beziehen (beispielsweise auf eine einzelne Abteilung), die die virtuellen Anwendungen ausführt. Sie sollten eine Netzwerkübersicht erhalten, die die Verbindungspfade sowie die verfügbare Bandbreite für jeden Standort sowie die Anzahl der Benutzer, die virtualisierte Anwendungen verwenden, und die WAN-Verbindungsgeschwindigkeit umfasst.</p></td>
</tr>
</tbody>
</table>

 

## Ermitteln, welche App-V 5,0-Infrastruktur erforderlich ist


**Wichtig**  Bei den beiden folgenden Modellen muss der App-V 5,0-Client auf dem Computer installiert sein, auf dem Sie virtuelle Anwendungen ausführen möchten.

Sie können Ihre App-V 5,0-Umgebung auch mithilfe einer ESD-Lösung (Electronic Software Distribution) wie Microsoft Systems Center Configuration Manager verwalten. Weitere Informationen finden Sie unter [Bereitstellen von App-V 5,0-Paketen mithilfe von ESD (Electronic Software Distribution)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).

 

-   **Eigenständiges Modell** : das eigenständige Modell ermöglicht es virtuellen Anwendungen, Windows Installer für die Verteilung ohne Streaming zu aktivieren. App-V 5,0 im Standalone-Modus besteht aus Sequencer und Client; Es sind keine zusätzlichen Komponenten erforderlich. Anwendungen werden mithilfe eines Prozesses, der als Sequenzierung bezeichnet wird, für die Virtualisierung vorbereitet. Weitere Informationen finden Sie unter [Planen der App-V 5,0-Sequenzer und Client Bereitstellung](planning-for-the-app-v-50-sequencer-and-client-deployment.md). Das eigenständige Modell wird für die folgenden Szenarien empfohlen:

    -   Mit getrennten Remotebenutzern, die keine Verbindung mit der App-V 5,0-Infrastruktur herstellen können.

    -   Wenn Sie ein Softwareverwaltungssystem wie Configuration Manager 2012 ausführen.

    -   Wenn Netzwerkbandbreite-Einschränkungen die elektronische Softwareverteilung hemmen.

-   **Vollständiges Infrastrukturmodell** – das vollständige Infrastrukturmodell bietet Software Verteilungs-, Verwaltungs-und Berichterstattungsfunktionen. Darüber hinaus wird das Streaming von Anwendungen im gesamten Netzwerk berücksichtigt. Das vollständige Infrastrukturmodell der APP-v 5,0 besteht aus einem oder mehreren App-v 5,0-Verwaltungsservern. Der Verwaltungs Server kann zum Veröffentlichen von Anwendungen für alle Clients verwendet werden. Beim Veröffentlichungsprozess werden die virtuellen Anwendungssymbole und-Verknüpfungen auf dem Zielcomputer platziert. Sie kann Anwendungen auch an lokale Benutzer streamen. Weitere Informationen zum Installieren des Verwaltungsservers finden Sie unter [Planen der App-V 5,0-Server Bereitstellung](planning-for-the-app-v-50-server-deployment.md). Das vollständige Infrastrukturmodell wird für die folgenden Szenarien empfohlen:

    **Wichtig**  Das vollständige Infrastrukturmodell der App-V 5,0 erfordert, dass Microsoft SQL Server Konfigurationsdaten speichert. Weitere Informationen finden Sie unter [unterstützte Konfigurationen für App-V 5,0](app-v-50-supported-configurations.md).

     

    -   Wenn Sie den Verwaltungs Server verwenden möchten, um die Anwendung auf Zielcomputern zu veröffentlichen.

    -   Schnelle Bereitstellung von Anwendungen für die Zielcomputer.

    -   Wenn Sie die App-V 5,0-Berichterstellung verwenden möchten.

## Richtlinien für die End-to-End-Server Größe


Der folgende Abschnitt enthält Informationen zur End-to-End-App-V 5,0-Größenanpassung und-Planung. Weitere spezifische Informationen finden Sie in den folgenden Abschnitten.

**Hinweis**  Die Antwortzeit für Roundtrips auf dem Client ist die Zeit, die der Computer mit dem App-V 5,0-Client erhält, um eine erfolgreiche Benachrichtigung vom Veröffentlichungsserver zu erhalten. Die Antwortzeit für Roundtrips auf dem Veröffentlichungsserver ist die Zeit, die der Computer, auf dem der Veröffentlichungsserver ausgeführt wird, zum Empfangen einer erfolgreichen Paketmetadaten-Aktualisierung vom Verwaltungsserver einnimmt.

 

-   20.000-Clients können auf einen einzelnen Veröffentlichungsserver Zielen, um die Paketaktualisierungen in einer akzeptablen Roundtrip-Zeit zu erhalten. ( &lt; 3 Sekunden)

-   Ein einzelner Verwaltungsserver kann bis zu 50-Publishing Server für die Aktualisierung von Paketmetadaten in einer akzeptablen Roundtrip-Zeit unterstützen. ( &lt; 5 Sekunden)

## <a href="" id="---------app-v-5-0-management-server-capacity-planning-recommendations"></a> Empfehlungen für die Kapazitätsplanung für App-V 5,0-Verwaltungs Server


Für die App-V 5,0-Veröffentlichungsserver ist der Verwaltungsserver für Paket Aktualisierungsanforderungen und Paket Aktualisierungs Antworten erforderlich. Der Verwaltungsserver sendet dann die Informationen an die Verwaltungsdatenbank, um Informationen abzurufen. Weitere Informationen zu den unterstützten Konfigurationen des App-v 5,0-Verwaltungsservers finden Sie unter [unterstützte Konfigurationen für App-v 5,0](app-v-50-supported-configurations.md).

**Hinweis**  Die standardmäßige Aktualisierungszeit auf dem App-V 5,0-Veröffentlichungsserver beträgt zehn Minuten.

 

Wenn mehrere gleichzeitige Veröffentlichungsserver einen einzelnen Verwaltungsserver für die Aktualisierung von Paketmetadaten kontaktieren, beeinflussen die folgenden drei Faktoren die Antwortzeit für Roundtrips auf dem Veröffentlichungsserver:

1.  Die Anzahl von Veröffentlichungsservern, die gleichzeitige Anforderungen stellen.

2.  Die Anzahl der auf dem Verwaltungsserver konfigurierten Verbindungsgruppen.

3.  Die Anzahl der auf dem Verwaltungsserver konfigurierten Zugriffsgruppen.

In der folgenden Tabelle werden weitere Informationen zu jedem Faktor angezeigt, der sich auf die Roundtrip-Zeit auswirkt.

**Hinweis**  "Roundtrip-Antwortzeit" ist die Zeit, die der Computer ausführt, auf dem der App-V 5,0-Publishing Server ausgeführt wird, um ein erfolgreiches Paketmetadaten-Update vom Verwaltungsserver zu erhalten.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Faktoren, die sich auf die Reaktionszeit von Roundtrips auswirken</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Die Anzahl der Veröffentlichungsserver, die Paketmetadaten gleichzeitig anfordern, wird aktualisiert.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Ein einzelner Verwaltungsserver kann auf bis zu 320-Publishing Servern Antworten, die gleichzeitig Veröffentlichungsmetadaten anfordern.</p></li>
<li><p>Die Antwortzeit für Roundtrips für 320-pub-Server beträgt ~ 40 Sekunden.</p></li>
<li><p>Bei &lt; 50-Publishing Servern, die Metadaten gleichzeitig anfordern, beträgt die Antwortzeit für Roundtrips &lt; 5 Sekunden.</p></li>
<li><p>Von 50 zu 320-Publishing Servern vergrößert sich die Antwortzeit linear (ca. 2x).</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Die Anzahl der auf dem Verwaltungsserver konfigurierten Verbindungsgruppen.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Für bis zu 100-Verbindungsgruppen gibt es keine signifikante Änderung der Roundtrip-Antwortzeit auf dem Veröffentlichungsserver.</p></li>
<li><p>Bei 100-400-Verbindungsgruppen gibt es eine geringfügige lineare Erhöhung der Antwortzeit für Roundtrips.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Die Anzahl der Zugriffsgruppen, die auf dem Verwaltungsserver konfiguriert sind.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Für bis zu 40-Zugriffsgruppen gibt es eine lineare (ungefähr 3X) höhere Vergrößerung der Roundtrip-Antwortzeit auf dem Veröffentlichungsserver.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

In der folgenden Tabelle werden die Beispielwerte für die einzelnen vorherigen Faktoren angezeigt. In jeder Variation werden 120-Pakete vom App-V 5.0-Verwaltungsserver aktualisiert.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Szenario</th>
<th align="left">Variante</th>
<th align="left">Anzahl der Verbindungsgruppen</th>
<th align="left">Anzahl der Zugriffsgruppen</th>
<th align="left">Anzahl der Veröffentlichungsserver</th>
<th align="left">Netzwerkverbindungstyp, Veröffentlichungsserver/Verwaltungsserver</th>
<th align="left">Roundtrip-Antwortzeit auf dem Veröffentlichungsserver (in Sekunden)</th>
<th align="left">CPU-Auslastung auf dem Verwaltungsserver</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publishing Server wenden sich gleichzeitig an den Verwaltungsserver, um Metadaten zu veröffentlichen.</p></td>
<td align="left"><p>Anzahl der Veröffentlichungsserver</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>300</p></li>
<li><p>315</p></li>
<li><p>320</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>5</p></li>
<li><p>10</p></li>
<li><p>19</p></li>
<li><p>32</p></li>
<li><p>30</p></li>
<li><p>37</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>17</p></li>
<li><p>17</p></li>
<li><p>17</p></li>
<li><p>15</p></li>
<li><p>17</p></li>
<li><p>15</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Veröffentlichungsmetadaten enthält Verbindungsgruppen</p></td>
<td align="left"><p>Anzahl der Verbindungsgruppen</p></td>
<td align="left"><p></p>
<ul>
<li><p>10</p></li>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>150</p></li>
<li><p>300</p></li>
<li><p>400</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>10</p></li>
<li><p>11</p></li>
<li><p>11</p></li>
<li><p>16</p></li>
<li><p>22</p></li>
<li><p>25</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>17</p></li>
<li><p>19</p></li>
<li><p>22</p></li>
<li><p>19</p></li>
<li><p>20</p></li>
<li><p>20</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Veröffentlichungsmetadaten enthalten Zugriffsgruppen</p></td>
<td align="left"><p>Anzahl der Zugriffsgruppen</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>10</p></li>
<li><p>20</p></li>
<li><p>40</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>10</p></li>
<li><p>43</p></li>
<li><p>153</p></li>
<li><p>535</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>17</p></li>
<li><p>26</p></li>
<li><p>24</p></li>
<li><p>24</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Die CPU-Auslastung des Computers, auf dem der Verwaltungsserver ausgeführt wird, beträgt rund 25%, unabhängig davon, wie viele Veröffentlichungsserver darauf ausgerichtet sind. Die Microsoft SQL Server-Datenbank Transaktionen/Sek., Batchanforderungen/Sek. und Benutzer Verbindungen sind unabhängig von der Anzahl der Veröffentlichungsserver identisch. Beispiel: Transaktionen/Sek ist ~ 30, Batchanforderungen ~ 200, und der Benutzer verbindet ~ 6.

Bei Verwendung einer geografisch verteilten Bereitstellung, bei der der Verwaltungsserver & Veröffentlichungsserver ein langsames Verbindungsnetzwerk zwischen Ihnen verwenden, liegt die Antwortzeit für Roundtrips auf den Veröffentlichungsservern innerhalb akzeptabler Zeiträume ( &lt; 5 Sekunden), auch bei gleichzeitigen 100-Anforderungen auf einem einzigen Verwaltungsserver.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Szenario</th>
<th align="left">Variante</th>
<th align="left">Anzahl der Verbindungsgruppen</th>
<th align="left">Anzahl der Zugriffsgruppen</th>
<th align="left">Anzahl der Veröffentlichungsserver</th>
<th align="left">Netzwerkverbindungstyp, Veröffentlichungsserver/Verwaltungsserver</th>
<th align="left">Roundtrip-Antwortzeit auf dem Veröffentlichungsserver (in Sekunden)</th>
<th align="left">CPU-Auslastung auf dem Verwaltungsserver</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Netzwerkverbindung zwischen dem Veröffentlichungsserver und dem Verwaltungsserver</p></td>
<td align="left"><p>1,5 Mbps Slow Link-Netzwerk</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1,5 MBit/s Kabel-DSL</p></li>
<li><p>1,5 MBit/s Kabel-DSL</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>4</p></li>
<li><p>5</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Netzwerkverbindung zwischen dem Veröffentlichungsserver und dem Verwaltungsserver</p></td>
<td align="left"><p>LAN/WLAN-Netzwerk</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>WLAN</p></li>
<li><p>WLAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>11</p></li>
<li><p>20</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>15</p></li>
<li><p>17</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Unabhängig davon, ob der Verwaltungsserver und die Veröffentlichungsserver über ein langsames Verbindungsnetzwerk oder ein Hochgeschwindigkeits-Netzwerk verbunden sind, kann der Verwaltungsserver ca. 15.000-Paket Aktualisierungsanforderungen in 30 Minuten verarbeiten.

## <a href="" id="---------app-v-5-0-reporting-server-capacity-planning-recommendations"></a> App-V 5,0 Reporting Server-Kapazitäts Planungsempfehlungen


App-V 5,0-Clients senden Berichtsdaten an den Berichtsserver. Der Berichtsserver zeichnet dann die Informationen in der Microsoft SQL Server-Datenbank auf und gibt eine erfolgreiche Benachrichtigung zurück an den Computer mit dem App-V 5,0-Client. Weitere Informationen zu den unterstützten Konfigurationen von App-v 5,0-Berichtsservern finden Sie unter [unterstützte Konfigurationen für App-v 5,0](app-v-50-supported-configurations.md).

**Hinweis**  "Roundtrip-Antwortzeit" ist die Zeit, die der Computer ausführt, auf dem der App-V 5,0-Client ausgeführt wird, um die Bericht Erstellungsinformationen an den Berichtsserver zu senden und eine erfolgreiche Benachrichtigung vom Berichtsserver zu erhalten.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Szenario</th>
<th align="left">Zusammenfassung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Mehrere App-V 5,0-Clients senden Bericht Erstellungsinformationen gleichzeitig an den Berichtsserver.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Die Antwortzeit für Roundtrips vom Berichtsserver beträgt 2,6 Sekunden für 500-Clients.</p></li>
<li><p>Die Antwortzeit für Roundtrips vom Berichtsserver beträgt 5,65 Sekunden für 1000-Clients.</p></li>
<li><p>Die Antwortzeit für Roundtrips erhöht sich linear abhängig von der Anzahl der Clients.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Vom Berichtsserver verarbeitete Anforderungen pro Sekunde.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Mit einem einzelnen Berichtsserver und einer einzelnen Datenbank können maximal 139-Anforderungen pro Sekunde verarbeitet werden. Der Mittelwert ist 121-Anforderungen/Sekunde.</p></li>
<li><p>Bei Verwendung von zwei Berichtsservern, die an dieselbe Microsoft SQL Server-Datenbank Bericht erstatten, ähnelt die durchschnittliche Anforderung/Sekunde einem einzelnen Berichtsserver = ~ 127 mit einem max. 278-Anforderungen/Sekunde.</p></li>
<li><p>Ein einzelner Berichtsserver kann 500 Concurrent/Active Connections verarbeiten.</p></li>
<li><p>Ein einzelner Berichtsserver kann maximal 1500 gleichzeitige Verbindungen verarbeiten.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Berichtsdatenbank.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Das Sperren von Konflikten auf dem Computer, auf dem Microsoft SQL Server ausgeführt wird, ist der limitierende Faktor für Anforderungen/Sekunde.</p></li>
<li><p>Durchsatz und Antwortzeit sind unabhängig von der Datenbankgröße.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Berechnen der Zufalls Verzögerung**:

Die zufällige Verzögerung gibt die maximale Verzögerung (in Minuten) für Daten an, die an den Berichtsserver gesendet werden sollen. Wenn der geplante Task gestartet wird, generiert der Client eine zufällige Verzögerung zwischen **0** und **ReportingRandomDelay** und wartet die angegebene Dauer vor dem Senden von Daten.

Zufällige Verzögerung = 4 \ * Anzahl der Clients/durchschnittliche Anforderungen pro Sekunde.

Beispiel: bei 500-Clients mit 120-Anforderungen pro Sekunde beträgt die zufällige Verzögerung 4 \ * 500/120 = ~ 17 Minuten.

## <a href="" id="---------app-v-5-0-publishing-server-capacity-planning-recommendations"></a> Empfehlungen für die Kapazitätsplanung von App-V 5,0 Publishing Server


Computer, auf denen der APP-v 5,0-Client ausgeführt wird, stellen eine Verbindung mit dem App-v 5,0-Veröffentlichungsserver her, um eine Veröffentlichungs Aktualisierungsanforderung zu senden und eine Antwort zu erhalten. Die Antwortzeit für Roundtrips wird auf dem Computer gemessen, auf dem der App-V 5,0-Client ausgeführt wird. Die Prozessorzeit wird auf dem Veröffentlichungsserver gemessen. Weitere Informationen zu den unterstützten Konfigurationen des App-v 5,0-Publishing Servers finden Sie unter [unterstützte Konfigurationen für App-v 5,0](app-v-50-supported-configurations.md).

**Wichtig**  In der folgenden Liste sind die Hauptfaktoren aufgeführt, die beim Einrichten des App-V 5,0-Publishing Servers zu berücksichtigen sind:

-   Die Anzahl der Clients, die gleichzeitig mit einem einzelnen Veröffentlichungsserver verbunden sind.

-   Die Anzahl der Pakete in jeder Aktualisierung.

-   Die verfügbare Netzwerkbandbreite in Ihrer Umgebung zwischen dem Client und dem App-V 5,0-Veröffentlichungsserver.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Szenario</th>
<th align="left">Zusammenfassung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Mehrere App-V 5,0-Clients stellen gleichzeitig eine Verbindung mit einem einzelnen Veröffentlichungsserver her.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Ein Publishing Server, auf dem Dual-Core-Prozessoren ausgeführt werden, kann auf höchstens 5000-Clients antworten, die eine Aktualisierung gleichzeitig anfordern.</p></li>
<li><p>Für 5000-10000-Clients erfordert der Veröffentlichungsserver mindestens einen Quad-Core.</p></li>
<li><p>Für 10000-20000-Clients sollte der Veröffentlichungsserver über zwei Quad-Cores verfügen, um die Antwortzeiten effizienter zu gestalten.</p></li>
<li><p>Ein Veröffentlichungsserver mit einem Quad-Core kann innerhalb von 3 Sekunden bis zu 10000-Pakete aktualisieren. (Unterstützung von 10000-Clients gleichzeitig)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Die Anzahl der Pakete in jeder Aktualisierung.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Steigende Anzahl von Paketen erhöht die Antwortzeit um ~ 40% (bis zu 1000-Pakete).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Netzwerk zwischen dem App-V 5,0-Client und dem Veröffentlichungsserver.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>In einem langsamen Netzwerk (1,5 Mbps-Bandbreite) gibt es eine Steigerung der Antwortzeit von 97% im Vergleich zu LAN (bis zu 1000 Benutzern).</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Die CPU-Auslastung des Veröffentlichungsservers ist im Zeitintervall immer sehr groß, wenn Sie gleichzeitige Anforderungen verarbeiten muss ( &gt; in den meisten Fällen 90%). Der Veröffentlichungsserver kann in einer Sekunde 1500-Clientanforderungen verarbeiten.

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Szenario</th>
<th align="left">Variante</th>
<th align="left">Anzahl der App-V 5,0-Clients</th>
<th align="left">Anzahl der Pakete</th>
<th align="left">Prozessorkonfiguration auf dem Veröffentlichungsserver</th>
<th align="left">Netzwerkverbindungstyp, Veröffentlichungsserver/App-V 5,0-Client</th>
<th align="left">Roundtrip-Zeit auf dem App-V 5,0-Client (in Sekunden)</th>
<th align="left">CPU-Auslastung auf dem Veröffentlichungsserver (in%)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0-Client sendet Antwort auf Veröffentlichungs Aktualisierungsanforderung &amp; , jede Anforderung, die 120-Pakete enthält</p></td>
<td align="left"><p>Anzahl der Clients</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>1000</p></li>
<li><p>5000</p></li>
<li><p>10000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Dual-Core</p></li>
<li><p>Dual-Core</p></li>
<li><p>Quad-Core</p></li>
<li><p>Quad-Core</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>2</p></li>
<li><p>2</p></li>
<li><p>3</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>99</p></li>
<li><p>89</p></li>
<li><p>77</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Mehrere Pakete in jeder Aktualisierung</p></td>
<td align="left"><p>Anzahl der Pakete</p></td>
<td align="left"><p></p>
<ul>
<li><p>1000</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Quad-Core</p></li>
<li><p>Quad-Core</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>2</p></li>
<li><p>3</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>92</p></li>
<li><p>91</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Netzwerk zwischen Client und Veröffentlichungsserver</p></td>
<td align="left"><p>1,5 Mbps Slow Link-Netzwerk</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Quad-Core</p></li>
<li><p>Quad-Core</p></li>
<li><p>Quad-Core</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1,5 Mbps Intra-Continental-Netzwerk</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3</p></li>
<li><p>10 (mit 0,2% Ausfallrate)</p></li>
<li><p>17 (mit einer Ausfallrate von 1%)</p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-0-streaming-capacity-planning-recommendations"></a> Empfehlungen für App-V 5,0-Streaming-Kapazitätsplanung


Auf Computern, auf denen der App-V 5,0-Client ausgeführt wird, wird das virtuelle Anwendungspaket vom Streamingserver gestreamt. Die Antwortzeit für Roundtrips wird auf dem Computer gemessen, auf dem der App-V 5,0-Client ausgeführt wird, und es wird die Zeit zum Streamen des gesamten Pakets übernommen.

**Wichtig**  In der folgenden Liste sind die Hauptfaktoren aufgeführt, die beim Einrichten des App-V 5,0-Streaming Servers zu berücksichtigen sind:

-   Die Anzahl der Clients, die Anwendungspakete gleichzeitig von einem einzelnen Streamingserver streamen.

-   Die Größe des zu streamenden Pakets.

-   Die verfügbare Netzwerkbandbreite in Ihrer Umgebung zwischen dem Client und dem Streamingserver.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Szenario</th>
<th align="left">Zusammenfassung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Mehrere App-V 5,0-Clients streamen Anwendungen gleichzeitig von einem einzelnen Streamingserver.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Wenn die Anzahl der Clients, die gleichzeitig vom gleichen Server gestreamt werden, zunimmt, gibt es eine lineare Beziehung mit der Download/Streaming-Zeit des Pakets.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Die Größe des zu streamenden Pakets.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Die Größe des Pakets hat erhebliche Auswirkungen auf die Streaming/Download-Zeit nur für größere Pakete mit einer Größe von ~ 1GB. Bei Paketgrößen von 3 MB bis 100 MB beträgt die streamingzeit zwischen 20 Sekunden und 100 Sekunden, mit 100 gleichzeitigen Clients.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Netzwerk zwischen dem App-V 5,0-Client und dem Streaming-Server.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>In einem langsamen Netzwerk (1,5 Mbps-Bandbreite) gibt es eine Steigerung der Antwortzeit von 70-80% im Vergleich zu LAN (bis zu 100 Benutzern).</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

In der folgenden Tabelle werden die Beispielwerte für die einzelnen Faktoren in der vorherigen Liste angezeigt:

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
<th align="left">Szenario</th>
<th align="left">Variante</th>
<th align="left">Anzahl der App-V 5,0-Clients</th>
<th align="left">Größe der einzelnen Pakete</th>
<th align="left">Netzwerkverbindungstyp Streaming Server/App-V 5,0 Client</th>
<th align="left">Roundtrip-Zeit auf dem App-V 5,0-Client (in Sekunden)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Mehrere App-V 5,0-Clients, die virtuelle Anwendungspakete von einem Streamingserver streamen.</p></td>
<td align="left"><p>Die Anzahl der Clients.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3,5 MB</p></li>
<li><p>3,5 MB</p></li>
<li><p>3,5 MB</p></li>
<li><p></p></li>
<li><p>5 MB</p></li>
<li><p>5 MB</p></li>
<li><p>5 MB</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p></p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>29</p></li>
<li><p>39</p></li>
<li><p>391</p></li>
<li><p></p></li>
<li><p>35</p></li>
<li><p>68</p></li>
<li><p>461</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Die Größe der einzelnen Pakete, die gestreamt werden.</p></td>
<td align="left"><p>Die Größe jedes Pakets.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>21 MB</p></li>
<li><p>21 MB</p></li>
<li><p></p></li>
<li><p>109</p></li>
<li><p>109</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p></p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<p>33</p>
<p>83</p>
<p></p>
<p>100</p>
<p>160</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Netzwerkverbindung zwischen Client und App-V 5,0 Streaming Server.</p></td>
<td align="left"><p>1,5 Mbps Slow Link-Netzwerk.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p></p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3,5 MB</p></li>
<li><p></p></li>
<li><p>5 MB</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1,5 Mbps Intra-Continental-Netzwerk</p></li>
</ul></td>
<td align="left"><p></p>
<p>102</p>
<p></p>
<p>121</p></td>
</tr>
</tbody>
</table>

 

Jeder App-V 5,0-Streamingserver sollte in der Lage sein, ein minimales 200-Client-Streaming mit virtualisierten Anwendungen gleichzeitig zu verarbeiten.

**Hinweis**  Die tatsächliche Zeit für den Datenstrom wird in erster Linie durch die Anzahl der gleichzeitigen Streaming-Clients, die Anzahl der Pakete, die Paketgröße, die Netzwerkaktivität des Servers und die Netzwerkbedingungen bestimmt.

 

Beispielsweise kann ein durchschnittlicher Benutzer ein 100-MB-Paket in weniger als zwei Minuten streamen, wenn 100 gleichzeitige Clients vom Server gestreamt werden. Ein Paket mit einer Größe von 1 GB kann jedoch bis zu 30 Minuten dauern. In den meisten realen Umgebungen, in denen die Streaming-Nachfrage nicht gleichmäßig verteilt ist, müssen Sie die ungefähren Peak-Streaming-Anforderungen verstehen, die in Ihrer Umgebung vorhanden sind, um die Anzahl der erforderlichen Streamingserver richtig zu ändern.

Die Anzahl der Clients, die ein Streamingserver unterstützenkann, kann erheblich erhöht werden, und die Spitzen-Streaming-Anforderungen werden verringert, wenn Sie Ihre Anwendungen Vorabzwischenspeichern. Sie können auch die Anzahl der Clients erhöhen, die ein Streamingserver unterstützt, indem Sie on-Demand-Streaming-Übermittlung und Datenstrom optimierte Pakete verwenden.

## Kombinieren von App-V 5,0-Server Rollen


Diskontierung von Skalierungs-und Fehlertoleranzanforderungen: die Mindestanzahl von Servern, die für einen Standort mit Active Directory-Konnektivität benötigt wird. Dieser Server hostet den Verwaltungsserver, den Verwaltungsserverdienst und die Microsoft SQL Server-Rollen. Server Rollen können daher in jeder gewünschten Kombination angeordnet werden, da Sie nicht miteinander in Konflikt stehen.

Wenn Sie die Skalierungsanforderungen ignorieren, beträgt die Mindestanzahl von Servern, die für die Bereitstellung einer fehlertoleranten Implementierung erforderlich sind, vier. Der Verwaltungsserver und die Microsoft SQL Server-Rollen unterstützen die Platzierung in fehlertoleranten Konfigurationen. Der Verwaltungsserverdienst kann mit jeder der Rollen kombiniert werden, bleibt aber ein einzelner Fehlerpunkt.

Obwohl eine Reihe von Strategien und Technologien zur Fehlertoleranz verfügbar sind, gelten nicht alle für einen bestimmten Dienst. Wenn App-V 5,0-Rollen kombiniert werden, gelten möglicherweise bestimmte Fehlertoleranzoptionen aufgrund von Inkompatibilitäten nicht mehr.






## Verwandte Themen


[Unterstützte App-V 5.0-Konfigurationen](app-v-50-supported-configurations.md)

[Planen für hohe Verfügbarkeit mit App-V 5.0](planning-for-high-availability-with-app-v-50.md)

[Planen der Bereitstellung von App-V](planning-to-deploy-app-v.md)

 

 





