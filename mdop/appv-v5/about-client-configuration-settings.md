---
title: Informationen über Clientkonfigurationseinstellungen
description: Informationen über Clientkonfigurationseinstellungen
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806104"
---
# Informationen über Clientkonfigurationseinstellungen


Der Microsoft Application Virtualization (App-V) 5,0-Client speichert seine Konfiguration in der Registrierung. Sie können einige nützliche Informationen zu dem Client sammeln, wenn Sie das Format der Daten in der Registrierung verstehen. Sie können auch viele Clientaktionen konfigurieren, indem Sie Registrierungseinträge ändern. In diesem Thema werden die Konfigurationseinstellungen des App-V 5,0-Clients sowie deren Verwendung erläutert. Sie können PowerShell verwenden, um die Clientkonfigurationseinstellungen zu ändern. Weitere Informationen zur Verwendung von PowerShell und App-v 5,0 finden Sie unter [Verwalten von App-v mithilfe von PowerShell](administering-app-v-by-using-powershell.md).

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> App-V 5,0-Client Konfigurationseinstellungen


In der folgenden Tabelle werden Informationen zu den Clientkonfigurationseinstellungen für App-V 5,0 angezeigt:

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
<th align="left">Einstellungs Name</th>
<th align="left">Setup-Flag</th>
<th align="left">Beschreibung</th>
<th align="left">Einstellungsoptionen</th>
<th align="left">Registrierungsschlüsselwert</th>
<th align="left">Deaktivierte Richtlinien Zustandsschlüssel und-Werte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>PACKAGEINSTALLATIONROOT</p></td>
<td align="left"><p>Gibt das Verzeichnis an, in dem alle neuen Anwendungen und Updates installiert werden.</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Streaming\PackageInstallationRoot</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>PACKAGESOURCEROOT</p></td>
<td align="left"><p>Überschreibt den Quellspeicherort zum Herunterladen von Paketinhalten.</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Streaming\PackageSourceRoot</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Mit dieser Einstellung wird gesteuert, ob virtualisierte Anwendungen auf Windows 8-Computern gestartet werden, die über eine getaktete Netzwerkverbindung verbunden sind (beispielsweise 4G).</p></td>
<td align="left"><p>True (aktiviert); Falsch (deaktivierter Zustand)</p></td>
<td align="left"><p>Streaming\AllowHighCostLaunch</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt an, wie oft eine gelöschte Sitzung wiederholt werden soll.</p></td>
<td align="left"><p>Ganzzahl (0-99)</p></td>
<td align="left"><p>Streaming\ReestablishmentRetries</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt die Anzahl der Sekunden zwischen den versuchen, eine gelöschte Sitzung wiederherzustellen, an.</p></td>
<td align="left"><p>Ganzzahl (0-3600)</p></td>
<td align="left"><p>Streaming\ReestablishmentInterval</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>AUTOLOAD</p></td>
<td align="left"><p>Gibt an, wie neue Pakete automatisch von App-V auf einem bestimmten Computer geladen werden sollen.</p></td>
<td align="left"><p>(0x0) keine; (0x1) zuvor verwendet; (0x2) alle</p></td>
<td align="left"><p>Streaming\AutoLoad</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocationProvider</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt die CLSID für eine kompatible Implementierung der IAppvPackageLocationProvider-Schnittstelle an.</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Streaming\LocationProvider</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CertFilterForClientSsl</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt den Pfad zu einem gültigen Zertifikat im Zertifikatspeicher an.</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Streaming\CertFilterForClientSsl</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VerifyCertificateRevocationList</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Überprüft den Sperrungsstatus des Server Zertifikats vor dem dämpfen mithilfe von HTTPS.</p></td>
<td align="left"><p>True (aktiviert); Falsch (deaktivierter Zustand)</p></td>
<td align="left"><p>Streaming\VerifyCertificateRevocationList</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>SHAREDCONTENTSTOREMODE</p></td>
<td align="left"><p>Gibt an, dass Streaming-Paketinhalt nicht auf der lokalen Festplatte gespeichert werden soll.</p></td>
<td align="left"><p>True (aktiviert); Falsch (deaktivierter Zustand)</p></td>
<td align="left"><p>Streaming\SharedContentStoreMode</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Name</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> . Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERNAME</p></td>
<td align="left"><p>Zeigt den Namen des Veröffentlichungsservers an.</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Publishing\Servers {Server-Nr} \ FriendlyName</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> . Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERURL</p></td>
<td align="left"><p>Zeigt die URL des Veröffentlichungsservers an.</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Publishing\Servers {Server-Nr} \ URL</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshEnabled</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> . Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHENABLED</p></td>
<td align="left"><p>Aktivieren der globalen Veröffentlichungsaktualisierung (boolescher Wert)</p></td>
<td align="left"><p>True (aktiviert); Falsch (deaktivierter Zustand)</p></td>
<td align="left"><p>Publishing\Servers {Server-Nr} \ GlobalEnabled</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshOnLogon</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> . Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHONLOGON</p></td>
<td align="left"><p>Löst eine Aktualisierung der globalen Veröffentlichung bei der Anmeldung aus. Boolean</p></td>
<td align="left"><p>True (aktiviert); Falsch (deaktivierter Zustand)</p></td>
<td align="left"><p>Publishing\Servers {Server-Nr} \ GlobalLogonRefresh</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshInterval</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> . Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVAL  </p></td>
<td align="left"><p>Gibt das Aktualisierungsintervall für die Veröffentlichung mithilfe von GlobalRefreshIntervalUnit an. Um die Paketaktualisierung zu deaktivieren, wählen Sie 0 aus.</p></td>
<td align="left"><p>Ganzzahl (0-744</p></td>
<td align="left"><p>Publishing\Servers {Server-Nr} \ GlobalPeriodicRefreshInterval</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshIntervalUnit</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> . Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVALUNI</p></td>
<td align="left"><p>Gibt die Intervalleinheit an (Stunde 0-23; Tag 0-31). </p></td>
<td align="left"><p>0 für Stunde, 1 für Tag</p></td>
<td align="left"><p>Publishing\Servers {Server-Nr} \ GlobalPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshEnabled</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> . Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHENABLED </p></td>
<td align="left"><p>Aktiviert die Aktualisierung der Benutzer Veröffentlichung (boolescher Wert)</p></td>
<td align="left"><p>True (aktiviert); Falsch (deaktivierter Zustand)</p></td>
<td align="left"><p>Publishing\Servers {Server-Nr} \ UserEnabled</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshOnLogon</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> . Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHONLOGON</p></td>
<td align="left"><p>Löst eine Benutzer Veröffentlichungsaktualisierung onlogon aus. Boolean</p>
<p>Wortanzahl (mit Leerzeichen): 60</p></td>
<td align="left"><p>True (aktiviert); Falsch (deaktivierter Zustand)</p></td>
<td align="left"><p>Publishing\Servers {Server-Nr} \ UserLogonRefresh</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshInterval</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> . Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVAL     </p></td>
<td align="left"><p>Gibt das Aktualisierungsintervall für die Veröffentlichung mithilfe von UserRefreshIntervalUnit an. Um die Paketaktualisierung zu deaktivieren, wählen Sie 0 aus.</p>
<p>Wortanzahl (mit Leerzeichen): 85</p></td>
<td align="left"><p>Ganzzahl (0-744 Stunden)</p></td>
<td align="left"><p>Publishing\Servers {Server-Nr} \ UserPeriodicRefreshInterval</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshIntervalUnit</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellung kann mit dem cmdLet "AppvclientConfiguration" nicht geändert werden <strong> </strong> . Sie müssen das <strong> Cmdlet "Satz-AppvPublishingServer" verwenden </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVALUNIT  </p></td>
<td align="left"><p>Gibt die Intervalleinheit an (Stunde 0-23; Tag 0-31). </p></td>
<td align="left"><p>0 für Stunde, 1 für Tag</p></td>
<td align="left"><p>Publishing\Servers {Server-Nr} \ UserPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MigrationMode</p></td>
<td align="left"><p>MIGRATIONMODE</p></td>
<td align="left"><p>Der Migrationsmodus ermöglicht es dem App-v-Client, Tastenkombinationen und FTA für Pakete zu ändern, die mit einer früheren Version von App-v erstellt wurden.</p></td>
<td align="left"><p>True (aktivierter Zustand); Falsch (deaktivierter Zustand)</p></td>
<td align="left"><p>Coexistence\MigrationMode</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>Ermöglicht es dem Computer, der den App-V 5,0-Client ausführt, bestimmte Nutzungsinformationen zu sammeln und zurückzugeben, damit wir die Anwendung weiter verbessern können.</p></td>
<td align="left"><p>0 für disabled; 1 für aktiviert</p></td>
<td align="left"><p>Software/Microsoft/AppV/CEIP/CEIPEnable</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePackageScripts</p></td>
<td align="left"><p>ENABLEPACKAGESCRIPTS</p></td>
<td align="left"><p>Aktiviert Skripts, die im Paketmanifest der Konfigurationsdateien definiert sind, die ausgeführt werden sollen.</p></td>
<td align="left"><p>True (aktiviert); Falsch (deaktivierter Zustand)</p></td>
<td align="left"><p>\Scripting\EnablePackageScripts</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>RoamingFileExclusions</p></td>
<td align="left"><p>ROAMINGFILEEXCLUSIONS</p></td>
<td align="left"><p>Gibt die Dateipfade relativ zu% User Profile% an, die nicht mit einem Benutzer&#39;s-Profil Roaming durchlaufen. Beispiel Verwendung:/ROAMINGFILEEXCLUSIONS =&#39;Desktop; meine Bilder&#39;</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>RoamingRegistryExclusions</p></td>
<td align="left"><p>ROAMINGREGISTRYEXCLUSIONS</p></td>
<td align="left"><p>Gibt die Registrierungspfade an, die nicht mit einem Benutzerprofil durchlaufen werden. Verwendungsbeispiel:/ROAMINGREGISTRYEXCLUSIONS = software\classes; Software\Clients</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Integration\RoamingRegistryExclusions</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="even">
<td align="left"><p>IntegrationRootUser</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt den Ort an, an dem symbolische Links erstellt werden, die der aktuellen Version eines pro Benutzer veröffentlichten Pakets zugeordnet sind. alle virtuellen Anwendungserweiterungen, beispielsweise Verknüpfungen und Dateitypzuordnungen, verweisen auf diesen Pfad. Wenn Sie keinen Pfad angeben, werden beim Veröffentlichen des Pakets symbolische Links nicht verwendet. Beispiel:%localappdata%\Microsoft\AppV\Client\Integration.</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Integration\IntegrationRootUser</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IntegrationRootGlobal</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt den Ort an, an dem symbolische Links erstellt werden, die der aktuellen Version eines Global veröffentlichten Pakets zugeordnet sind. alle virtuellen Anwendungserweiterungen, beispielsweise Verknüpfungen und Dateitypzuordnungen, verweisen auf diesen Pfad. Wenn Sie keinen Pfad angeben, werden beim Veröffentlichen des Pakets symbolische Links nicht verwendet. Beispiel:%ALLUSERSPROFILE%\Microsoft\AppV\Client\Integration</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Integration\IntegrationRootGlobal</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="even">
<td align="left"><p>VirtualizableExtensions</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Eine durch trennzeichengetrennte Liste mit Dateinamenerweiterungen, die verwendet werden kann, um zu ermitteln, ob eine lokal installierte Anwendung in der virtuellen Umgebung ausgeführt werden kann.</p>
<p>Wenn während der Veröffentlichung Verknüpfungen, FTA und andere Erweiterungspunkte erstellt werden, vergleicht App-V die Dateinamenerweiterung mit der Liste, wenn die Anwendung, die dem Erweiterungspunkt zugeordnet ist, lokal installiert ist. Wenn sich die Erweiterung befindet, <strong> wird der RunVirtual- </strong> Befehlszeilenparameter hinzugefügt, und die Anwendung wird praktisch ausgeführt.</p>
<p>Weitere Informationen zum <strong> RunVirtual </strong> -Parameter finden Sie unter <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierten Anwendungen </a> .</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Integration\VirtualizableExtensions</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingEnabled</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Ermöglicht es dem Client, Informationen an einen Berichtsserver zurückzugeben.</p></td>
<td align="left"><p>True (aktiviert); Falsch (deaktivierter Zustand)</p></td>
<td align="left"><p>Reporting\EnableReporting</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingServerURL</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt den Speicherort auf dem Berichtsserver an, auf dem Clientinformationen gespeichert werden.</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Reporting\ReportingServer</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingDataCacheLimit</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt die maximale Größe in Megabyte (MB) des XML-Caches zum Speichern von Berichtsinformationen an. Die Größe bezieht sich auf den Cache im Arbeitsspeicher. Wenn das Limit erreicht ist, wird die Protokolldatei überschrieben. Zwischen 0 und 1024.</p></td>
<td align="left"><p>Ganzzahl [0-1024]</p></td>
<td align="left"><p>Reporting\DataCacheLimit</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingDataBlockSize</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt die maximale Größe in Bytes an, die an den Server gesendet werden soll, um Upload-Anforderungen zu melden. Dies kann dazu beitragen, dauerhafte Übertragungsfehler zu vermeiden, wenn das Protokoll eine signifikante Größe erreicht hat. Zwischen 1024 und unbegrenzt eingestellt.</p></td>
<td align="left"><p>Ganzzahl [1024-unbegrenzt]</p></td>
<td align="left"><p>Reporting\DataBlockSize</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingStartTime</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt den Zeitpunkt an, zu dem der Client initiiert werden soll, um Daten an den Berichtsserver zu senden. Sie müssen eine gültige Ganzzahl zwischen 0-23 angeben, die der Stunde des Tages entspricht. Standardmäßig <strong> wird der ReportingStartTime am </strong> aktuellen Tag um 10 P. M oder 22 gestartet.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Sie sollten diese Einstellung auf einen Zeitpunkt konfigurieren, zu dem Computer, auf denen der App-V 5,0-Client ausgeführt wird, am ehesten offline sind.</p>
</div>
<div>

</div></td>
<td align="left"><p>Ganzzahl (0 – 23)</p></td>
<td align="left"><p>Berichterstellung \ Startzeit</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingInterval</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt das Wiederholungsintervall an, das vom Client zum erneuten Senden von Daten an den Berichtsserver verwendet wird.</p></td>
<td align="left"><p>Ganze Zahl</p></td>
<td align="left"><p>Reporting\RetryInterval</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingRandomDelay</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt die maximale Verzögerung (in Minuten) für Daten an, die an den Berichtsserver gesendet werden sollen. Wenn der geplante Task gestartet wird, generiert der Client eine zufällige Verzögerung zwischen 0 und <strong> ReportingRandomDelay </strong> und wartet die angegebene Dauer vor dem Senden von Daten. Dies kann dazu beitragen, Kollisionen auf dem Server zu verhindern.</p></td>
<td align="left"><p>Ganzzahl [0-ReportingRandomDelay]</p></td>
<td align="left"><p>Reporting\RandomDelay</p></td>
<td align="left"><p>Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert)</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableDynamicVirtualization</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Diese Einstellung ist nur mit App-V 5,0 SP2 oder höher verfügbar.</p>
</div>
<div>

</div></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Ermöglicht unterstützte Shell-Erweiterungen, Browser-helferobjekte und ActiveX-Steuerelemente, die virtualisiert und mit virtuellen Anwendungen ausgeführt werden können.</p></td>
<td align="left"><p>1 (aktiviert), 0 (deaktiviert)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \software\microsoft\appv\client\virtualization</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePublishingRefreshUI</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Diese Einstellung ist nur mit App-V 5,0 SP2 verfügbar.</p>
</div>
<div>

</div></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Aktiviert die Statusleiste für die Veröffentlichungsaktualisierung für den Computer, auf dem der App-V 5,0-Client ausgeführt wird.</p></td>
<td align="left"><p>1 (aktiviert), 0 (deaktiviert)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \software\microsoft\appv\client\publishing</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>HideUI</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Diese Einstellung ist nur mit App-V 5,0 SP2 verfügbar.</p>
</div>
<div>

</div></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Blendet die Statusleiste der Veröffentlichungsaktualisierung aus.</p></td>
<td align="left"><p>1 (aktiviert), 0 (deaktiviert)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Ist nicht verfügbar.</p></td>
<td align="left"><p>Gibt eine Liste von Prozess Pfaden an (die möglicherweise Platzhalter enthalten), die Kandidaten für die Verwendung der dynamischen Virtualisierung sind (unterstützte Shell-Erweiterungen, Browser-helferobjekte und ActiveX-Steuerelemente). Nur Prozesse, deren vollständiger Pfad einem dieser Elemente entspricht, können Dynamic Virtualization verwenden.</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Virtualization\ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Leere Zeichenfolge.</p></td>
</tr>
</tbody>
</table>








## Verwandte Themen


[Bereitstellen von App-V 5.0-Sequencer und -Client](deploying-the-app-v-50-sequencer-and-client.md)

[So ändern Sie die App-V 5.0-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[So stellen Sie App-V-Client bereit](how-to-deploy-the-app-v-client-gb18030.md)









