---
title: Übersicht über Application Virtualization Server-basierte Szenarien
description: Übersicht über Application Virtualization Server-basierte Szenarien
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809148"
---
# Übersicht über Application Virtualization Server-basierte Szenarien


Wenn Sie ein serverbasiertes Bereitstellungsszenario für Ihre Microsoft Application Virtualization-Umgebung verwenden möchten, ist es wichtig, die Unterschiede zwischen *Application Virtualization Management Server* und *Application Virtualization Streaming Server*zu verstehen. In diesem Thema werden diese Unterschiede beschrieben und außerdem Informationen zu Paketübermittlungsmethoden, Übertragungsprotokollen und externen Komponenten bereitgestellt, die Sie beim Fortsetzen der Bereitstellung in Frage stellen müssen.

## Application Virtualization-Verwaltungs Server


Der Application Virtualization Management-Server führt sowohl die Veröffentlichungsfunktion als auch die Streamingfunktion aus. Der Server veröffentlicht Anwendungssymbole, Verknüpfungen und Dateitypzuordnungen für die App-V-Clients für autorisierte Benutzer. Wenn Benutzeranforderungen für Anwendungen empfangen werden, strömt der Server diese Daten bei Bedarf an autorisierte Benutzer mithilfe von RTSP-oder RTSPS-Protokollen aus. In den meisten Konfigurationen, die diesen Server verwenden, geben mindestens ein Verwaltungsserver einen gemeinsamen Datenspeicher für Konfigurations-und Paketinformationen frei.

Die Application Virtualization Management-Server verwenden Active Directory-Gruppen, um die Benutzerautorisierung zu verwalten. Neben den Active Directory-Domänendiensten sind auf diesen Servern SQL Server installiert, um die Datenbank und den Datenspeicher zu verwalten. Der Verwaltungs Server wird über die Application Virtualization Management Console, ein Snap-in für die Microsoft Management Console, gesteuert.

Da die Application Virtualization-Verwaltungsserver Anwendungen bei Bedarf an Endbenutzer streamen, eignen sich diese Server ideal für Systemkonfigurationen mit zuverlässigen LANs mit hoher Bandbreite.

## Application Virtualization Streaming Server


Der Application Virtualization Streaming Server bietet die gleichen Streaming-und Paket Aktualisierungsfunktionen, die vom Verwaltungs Server bereitgestellt werden, jedoch ohne die Active Directory-oder SQL Server-Anforderungen. Der Streamingserver verfügt jedoch weder über einen Veröffentlichungsdienst noch über Lizenzierungs-oder Dosier Funktionen. Der Veröffentlichungsdienst eines separaten App-v-Verwaltungsservers wird in Verbindung mit dem App-v-Streamingserver verwendet. Der APP-v-Streamingserver richtet sich an die Anforderungen von Unternehmen, die Application Virtualization an mehreren Speicherorten mit den Streamingfunktionen der klassischen Server Konfiguration verwenden möchten, aber möglicherweise nicht über die Infrastruktur zur Unterstützung von App-V-Verwaltungsservern an jedem Standort verfügen.

Der Application Virtualization Streaming Server kann auch in Umgebungen mit einem vorhandenen elektronischen Softwareverteilungssystem (ESD) verwendet werden. Sie verwenden das ESD-Programm zum Verwalten von Streaming-Anwendungen. Im Gegensatz zum Application Virtualization Management-Server verwendet der Streamingserver keine SQL-oder Verwaltungskonsole. Diese Server verwenden Zugriffssteuerungslisten (ACLs), um die Benutzerautorisierung zu erteilen.

## Paketübermittlungsmethoden


Wenn Sie beabsichtigen, einen Application Virtualization Server als Veröffentlichungs Bereitstellungsmethode zu verwenden, müssen Sie ermitteln, welche der folgenden Paketübermittlungsmethoden Ihr Szenario verwendet:

-   *Dynamische Paketzustellung*

-   *Laden aus Dateipaket Zustellung*

### Dynamische Paketzustellung

Während der dynamischen Paketzustellung übermittelt der Server (Application Virtualization Management Server, Application Virtualization Streaming Server oder IIS-Server) die virtualisierten Anwendungen über die bedarfsgesteuerte Bereitstellung an die Endbenutzer. Der Server übermittelt die virtualisierten Anwendungen und Pakete nur dann an einen Clientcomputer, wenn ein Benutzer zuerst versucht, eine Anwendung (bei Bedarf) zu starten. Der Server streamt nur die Blöcke, die zum Starten der Anwendung erforderlich sind (primärer Feature-Block). Nachdem der primäre Feature-Block an den Client übermittelt wurde, wird die Anwendung ausgeführt; der Client erhält nicht die vollständige Anwendung (inkrementelle Bereitstellung), es sei denn, der Client benötigt Zugriff auf einen Teil der Anwendung, der nicht im primären Feature-Block enthalten ist. In diesem Fall führt der Client eine Out-of-Sequence-Anforderung aus, und der sekundäre Feature-Block wird an den Client gestreamt. Die dynamische Paketzustellung ermöglicht den schnellen Anwendungsstart.

### Laden aus Dateipaket Zustellung

Für das Laden aus der Dateipaket Zustellung übergibt der Server das gesamte virtualisierte Anwendungspaket an einen Clientcomputer, bevor der Benutzer die Anwendung startet. In diesem Szenario werden virtualisierte Anwendungen als vollständige Pakete bereitgestellt und nicht über die dynamische, inkrementelle Methode, die vom dynamischen Übermittlungs Modell verwendet wird.

**Hinweis**  Für jede Zustellungsmethode sind der anfängliche Bereitstellungsprozess für die virtuelle Anwendung und der Aktualisierungsvorgang der virtuellen Anwendung identisch. das aktualisierte virtuelle Anwendungspaket ersetzt das ursprüngliche Anwendungspaket.

 

In der folgenden Tabelle werden die vor-und Nachteile der einzelnen Paketübermittlungsmethoden verglichen.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Vorteile</th>
<th align="left">Nachteile</th>
<th align="left">Anmerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dynamische Paketzustellung</p></td>
<td align="left"><p>Anwendungen werden nach Bedarf bereitgestellt und aktualisiert.</p>
<p>Anwendungen werden bereitgestellt und inkrementell aktualisiert, um die Startzeit zu optimieren.</p>
<p>Updates werden automatisch an den Clientdesktop übermittelt.</p></td>
<td align="left"><p>Größerer Speicherbedarf in der Unternehmenstopologie aufgrund von Server Anforderungen</p>
<p>Das Anwendungsstreaming sollte über ein LAN erfolgen. Bereitstellungsszenarien über ein WAN oder die Verwendung einer unzuverlässigen oder zeitweiligen Verbindung zwischen dem Server und dem Client sind möglicherweise unbrauchbar.</p></td>
<td align="left"><p>Erfordert eine Streaming-Infrastruktur.</p>
<p>Windows Installer, der zum Bereitstellen von Application Virtualization-Desktop Client Software für Endbenutzercomputer verwendet wird.</p>
<p>Große Unternehmen sollten Application Virtualization Streaming Server als Verteilungspunkte verwenden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Laden aus Dateipaket Zustellung</p></td>
<td align="left"><p>Konsistent mit typischen Unternehmensverwaltungsmethoden.</p>
<p>Unterstützt eigenständige Konfigurationsszenarien.</p>
<p>Bietet eine Lösung für das Problem von Micro-Branch Office.</p></td>
<td align="left"><p>Die Anwendungs Zustellung und-Aktualisierung ist bei Bedarf nicht möglich.</p>
<p>Die Anwendungs Zustellung und-Aktualisierung ist nicht inkrementell; Sie erhöht den Ressourcenverbrauch relativ zur dynamischen Zustellung.</p></td>
<td align="left"><p>Die IT-Organisation ist häufig für die Verwaltung von Anwendungslizenzen, Benutzerautorisierung und Authentifizierung verantwortlich.</p></td>
</tr>
</tbody>
</table>

 

## Server bezogene Protokolle und externe Komponenten


In der folgenden Tabelle sind die Servertypen aufgeführt, die in einer Application Virtualization Server-basierten Szenarien verwendet werden können, zusammen mit den entsprechenden Übertragungsprotokollen und den externen Komponenten, die zur Unterstützung der spezifischen Serverkonfiguration erforderlich sind. Die Tabelle enthält auch den Berichterstellungsmechanismus und den aktiven Aktualisierungsmechanismus für die einzelnen Servertypen. Da diese Szenarien alle den Application Virtualization-Verwaltungs Server verwenden, können Sie die internen Berichterstellungsfunktionen verwenden, die in das System integriert sind. Wenn Sie ein Application Virtualization Management oder einen Application Virtualization Streaming Server verwenden, um Pakete an den Client zu übermitteln, werden Pakete auf dem Server automatisch aktualisiert, wenn sich ein Benutzer beim Client anmeldet. Wenn Sie IIS-Server oder eine Datei verwenden, um die Pakete an den Client zu übermitteln, müssen die Pakete auf dem Client manuell aktualisiert werden.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Servertyp</th>
<th align="left">Protokolle</th>
<th align="left">Externe Komponenten erforderlich</th>
<th align="left">Berichterstellung</th>
<th align="left">Aktives Upgrade</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Application Virtualization-Verwaltungs Server</p></td>
<td align="left"><p>RTSP</p>
<p>RTSPS</p></td>
<td align="left"><p>Verwenden Sie bei Verwendung von HTTPS einen IIS-Server zum Herunterladen von ICO-und OSD-Dateien sowie eine Firewall, um den Server vor einer Gefährdung durch das Internet zu schützen.</p></td>
<td align="left"><p>Intern</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="even">
<td align="left"><p>Application Virtualization Streaming Server</p></td>
<td align="left"><p>RTSP</p>
<p>RTSPS</p></td>
<td align="left"><p>Verwenden Sie einen Mechanismus, um den Inhalt zwischen dem Verwaltungsserver und dem Streamingserver zu synchronisieren. Verwenden Sie bei Verwendung von HTTPS einen IIS-Server zum Herunterladen von ICO-und OSD-Dateien, und verwenden Sie eine Firewall, um den Server vor der Gefährdung durch das Internet zu schützen.</p></td>
<td align="left"><p>Intern</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IIS-Server</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>Verwenden Sie einen Mechanismus, um den Inhalt zwischen dem Verwaltungsserver und dem Streamingserver zu synchronisieren. Verwenden Sie bei Verwendung von http oder HTTPS einen IIS-Server zum Herunterladen von ICO-und OSD-Dateien sowie eine Firewall, um den Server vor der Gefährdung durch das Internet zu schützen.</p></td>
<td align="left"><p>Intern</p></td>
<td align="left"><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td align="left"><p>Datei</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>Sie benötigen eine Möglichkeit, den Inhalt zwischen dem Verwaltungsserver und dem Streamingserver zu synchronisieren. Sie benötigen einen Clientcomputer mit Dateifreigabe-oder Streaming-Funktion.</p></td>
<td align="left"><p>Intern</p></td>
<td align="left"><p>Nicht unterstützt</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)

[So konfigurieren Sie Server für die serverbasierte Bereitstellung](how-to-configure-servers-for-server-based-deployment.md)

[So installieren Sie die Server und Systemkomponenten](how-to-install-the-servers-and-system-components.md)

 

 





