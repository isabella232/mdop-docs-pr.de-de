---
title: Informationen über Clientkonfigurationseinstellungen
description: Informationen über Clientkonfigurationseinstellungen
author: dansimp
ms.assetid: 18bb307a-7eda-4dd6-a83e-6afaefd99470
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb547eedf63bf165b1e8f5fd024839b3c2af3e4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806107"
---
# Informationen über Clientkonfigurationseinstellungen


Der Microsoft Application Virtualization (App-V) 5,1-Client speichert seine Konfiguration in der Registrierung. Sie können einige nützliche Informationen zu dem Client sammeln, wenn Sie das Format der Daten in der Registrierung verstehen. Sie können auch viele Clientaktionen konfigurieren, indem Sie Registrierungseinträge ändern. In diesem Thema werden die Konfigurationseinstellungen des App-V 5,1-Clients sowie deren Verwendung erläutert. Sie können PowerShell verwenden, um die Clientkonfigurationseinstellungen zu ändern. Weitere Informationen zur Verwendung von PowerShell und App-v 5,1 finden Sie unter [Verwalten von App-v 5,1 mithilfe von PowerShell](administering-app-v-51-by-using-powershell.md).

## <a href="" id="---------app-v-5-1-client-configuration-settings"></a> App-V 5,1-Client Konfigurationseinstellungen


In der folgenden Tabelle werden Informationen zu den Clientkonfigurationseinstellungen für App-V 5,1 angezeigt:

|Einstellungsname | Setup-Flag | Beschreibung | Einstellungsoptionen | Registrierungsschlüsselwert | Deaktivierte Richtlinien Zustandsschlüssel und-Werte |
|-------------|------------|-------------|-----------------|--------------------|--------------------------------------|
| PackageInstallationRoot | PACKAGEINSTALLATIONROOT | Gibt das Verzeichnis an, in dem alle neuen Anwendungen und Updates installiert werden. | Zeichenfolge | Streaming\PackageInstallationRoot | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| PackageSourceRoot | PACKAGESOURCEROOT | Überschreibt den Quellspeicherort zum Herunterladen von Paketinhalten. | Zeichenfolge | Streaming\PackageSourceRoot | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| AllowHighCostLaunch | Ist nicht verfügbar. |Mit dieser Einstellung wird gesteuert, ob virtualisierte Anwendungen auf Windows 10-Computern gestartet werden, die über eine getaktete Netzwerkverbindung verbunden sind (beispielsweise 4G). | True (aktiviert); Falsch (deaktivierter Zustand) | Streaming\AllowHighCostLaunch | 0 |
| ReestablishmentRetries | Ist nicht verfügbar. | Gibt an, wie oft eine gelöschte Sitzung wiederholt werden soll. | Ganzzahl (0-99) | Streaming\ReestablishmentRetries | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| ReestablishmentInterval | Ist nicht verfügbar. | Gibt die Anzahl der Sekunden zwischen den versuchen, eine gelöschte Sitzung wiederherzustellen, an. | Ganzzahl (0-3600) | Streaming\ReestablishmentInterval | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| LocationProvider | Ist nicht verfügbar. | Gibt die CLSID für eine kompatible Implementierung der IAppvPackageLocationProvider-Schnittstelle an. | Zeichenfolge | Streaming\LocationProvider | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| CertFilterForClientSsl | Ist nicht verfügbar. | Gibt den Pfad zu einem gültigen Zertifikat im Zertifikatspeicher an. | Zeichenfolge | Streaming\CertFilterForClientSsl | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| VerifyCertificateRevocationList | Ist nicht verfügbar. | Überprüft den Sperrungsstatus des Server Zertifikats vor dem dämpfen mithilfe von HTTPS. | True (aktiviert); Falsch (deaktivierter Zustand) | Streaming\VerifyCertificateRevocationList | 0 |
| SharedContentStoreMode | SHAREDCONTENTSTOREMODE | Gibt an, dass Streaming-Paketinhalt nicht auf der lokalen Festplatte gespeichert werden soll. | True (aktiviert); Falsch (deaktivierter Zustand) | Streaming\SharedContentStoreMode | 0 |
| Name<br>**Hinweis** Diese Einstellung kann mit dem cmdLet " **AppvclientConfiguration** " nicht geändert werden. Sie müssen das Cmdlet " **Satz-AppvPublishingServer** " verwenden. | PUBLISHINGSERVERNAME | Zeigt den Namen des Veröffentlichungsservers an. | Zeichenfolge | Publishing\Servers\ {Server-Nr} \ FriendlyName | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| URL<br>**Hinweis** Diese Einstellung kann mit dem cmdLet " **AppvclientConfiguration** " nicht geändert werden. Sie müssen das Cmdlet " **Satz-AppvPublishingServer** " verwenden. | PUBLISHINGSERVERURL | Zeigt die URL des Veröffentlichungsservers an. | Zeichenfolge | Publishing\Servers\ {Server-Nr} \ URL | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| GlobalRefreshEnabled<br>**Hinweis** Diese Einstellung kann mit dem cmdLet " **AppvclientConfiguration** " nicht geändert werden. Sie müssen das Cmdlet " **Satz-AppvPublishingServer** " verwenden. | GLOBALREFRESHENABLED | Aktivieren der globalen Veröffentlichungsaktualisierung (boolescher Wert) | True (aktiviert); Falsch (deaktivierter Zustand) | Publishing\Servers\ {Server-Nr} \ GlobalEnabled | False |
| GlobalRefreshOnLogon<br>**Hinweis** Diese Einstellung kann mit dem cmdLet " **AppvclientConfiguration** " nicht geändert werden. Sie müssen das Cmdlet " **Satz-AppvPublishingServer** " verwenden. | GLOBALREFRESHONLOGON | Löst eine Aktualisierung der globalen Veröffentlichung bei der Anmeldung aus. Boolean | True (aktiviert); Falsch (deaktivierter Zustand) | Publishing\Servers\ {Server-Nr} \ GlobalLogonRefresh | False |
| GlobalRefreshInterval<br>**Hinweis** Diese Einstellung kann mit dem cmdLet " **AppvclientConfiguration** " nicht geändert werden. Sie müssen das Cmdlet " **Satz-AppvPublishingServer** " verwenden. | GLOBALREFRESHINTERVAL | Gibt das Aktualisierungsintervall für die Veröffentlichung mithilfe von GlobalRefreshIntervalUnit an. Um die Paketaktualisierung zu deaktivieren, wählen Sie 0 aus. | Ganzzahl (0-744) | Publishing\Servers\ {Server-Nr} \ GlobalPeriodicRefreshInterval | 0 |
| GlobalRefreshIntervalUnit <br>**Hinweis** Diese Einstellung kann mit dem cmdLet " **AppvclientConfiguration** " nicht geändert werden. Sie müssen das Cmdlet " **Satz-AppvPublishingServer** " verwenden. | GLOBALREFRESHINTERVALUNI | Gibt die Intervalleinheit an (Stunde 0-23; Tag 0-31). | 0 für Stunde, 1 für Tag | Publishing\Servers\ {Server-Nr} \ GlobalPeriodicRefreshIntervalUnit | 1 |
| UserRefreshEnabled<br>**Hinweis** Diese Einstellung kann mit dem cmdLet " **AppvclientConfiguration** " nicht geändert werden. Sie müssen das Cmdlet " **Satz-AppvPublishingServer** " verwenden. | USERREFRESHENABLED | Aktiviert die Aktualisierung der Benutzer Veröffentlichung (boolescher Wert) | True (aktiviert); Falsch (deaktivierter Zustand) | Publishing\Servers\ {Server-Nr} \ UserEnabled | False |
| UserRefreshOnLogon<br>**Hinweis** Diese Einstellung kann mit dem cmdLet " **AppvclientConfiguration** " nicht geändert werden. Sie müssen das Cmdlet " **Satz-AppvPublishingServer** " verwenden. | USERREFRESHONLOGON | Löst eine Benutzer Veröffentlichungsaktualisierung onlogon aus. Boolean<br>Wortanzahl (mit Leerzeichen): 60 | True (aktiviert); Falsch (deaktivierter Zustand) | Publishing\Servers\ {Server-Nr} \ UserLogonRefresh | False |
| UserRefreshInterval<br>**Hinweis** Diese Einstellung kann mit dem cmdLet " **AppvclientConfiguration** " nicht geändert werden. Sie müssen das Cmdlet " **Satz-AppvPublishingServer** " verwenden. | USERREFRESHINTERVAL | Gibt das Aktualisierungsintervall für die Veröffentlichung mithilfe von UserRefreshIntervalUnit an. Um die Paketaktualisierung zu deaktivieren, wählen Sie 0 aus. | Wortanzahl (mit Leerzeichen): 85<br>Ganzzahl (0-744 Stunden) | Publishing\Servers\ {Server-Nr} \ UserPeriodicRefreshInterval | 0 |
| UserRefreshIntervalUnit<br>**Hinweis** Diese Einstellung kann mit dem cmdLet " **AppvclientConfiguration** " nicht geändert werden. Sie müssen das Cmdlet " **Satz-AppvPublishingServer** " verwenden. | USERREFRESHINTERVALUNIT | Gibt die Intervalleinheit an (Stunde 0-23; Tag 0-31). | 0 für Stunde, 1 für Tag | Publishing\Servers\ {Server-Nr} \ UserPeriodicRefreshIntervalUnit | 1 |
| MigrationMode | MIGRATIONMODE | Der Migrationsmodus ermöglicht es dem App-v-Client, Tastenkombinationen und FTA für Pakete zu ändern, die mit einer früheren Version von App-v erstellt wurden. | True (aktivierter Zustand); Falsch (deaktivierter Zustand) | Coexistence\MigrationMode | |
| CEIPOPTIN | CEIPOPTIN | Ermöglicht es dem Computer, der den App-V 5,1-Client ausführt, bestimmte Nutzungsinformationen zu sammeln und zurückzugeben, damit wir die Anwendung weiter verbessern können. | 0 für disabled; 1 für aktiviert | Software/Microsoft/AppV/CEIP/CEIPEnable | 0 | 
| EnablePackageScripts | ENABLEPACKAGESCRIPTS | Aktiviert Skripts, die im Paketmanifest der Konfigurationsdateien definiert sind, die ausgeführt werden sollen. | True (aktiviert); Falsch (deaktivierter Zustand) | \Scripting\EnablePackageScripts | | 
| RoamingFileExclusions | ROAMINGFILEEXCLUSIONS | Gibt die Dateipfade relativ zu% User Profile% an, die nicht mit dem Profil eines Benutzers Roamen. Verwendungsbeispiel:/ROAMINGFILEEXCLUSIONS = ' Desktop; meine Bilder ' | | | |
| RoamingRegistryExclusions | ROAMINGREGISTRYEXCLUSIONS | Gibt die Registrierungspfade an, die nicht mit einem Benutzerprofil durchlaufen werden. Verwendungsbeispiel:/ROAMINGREGISTRYEXCLUSIONS = software\\classes; software\\clients | Zeichenfolge | Integration\RoamingRegistryExclusions | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| IntegrationRootUser | Ist nicht verfügbar. | Gibt den Ort an, an dem symbolische Links erstellt werden, die der aktuellen Version eines pro Benutzer veröffentlichten Pakets zugeordnet sind. alle virtuellen Anwendungserweiterungen, beispielsweise Verknüpfungen und Dateitypzuordnungen, verweisen auf diesen Pfad. Wenn Sie keinen Pfad angeben, werden beim Veröffentlichen des Pakets symbolische Links nicht verwendet. Beispiel:%localappdata%\Microsoft\AppV\Client\Integration.| Zeichenfolge | Integration\IntegrationRootUser | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
|IntegrationRootGlobal | Ist nicht verfügbar.| Gibt den Ort an, an dem symbolische Links erstellt werden, die der aktuellen Version eines Global veröffentlichten Pakets zugeordnet sind. alle virtuellen Anwendungserweiterungen, beispielsweise Verknüpfungen und Dateitypzuordnungen, verweisen auf diesen Pfad. Wenn Sie keinen Pfad angeben, werden beim Veröffentlichen des Pakets symbolische Links nicht verwendet. Beispiel:%ALLUSERSPROFILE%\Microsoft\AppV\Client\Integration | Zeichenfolge | Integration\IntegrationRootGlobal | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| VirtualizableExtensions | Ist nicht verfügbar. | Eine durch trennzeichengetrennte Liste mit Dateinamenerweiterungen, die verwendet werden kann, um zu ermitteln, ob eine lokal installierte Anwendung in der virtuellen Umgebung ausgeführt werden kann.<br>Wenn während der Veröffentlichung Verknüpfungen, FTA und andere Erweiterungspunkte erstellt werden, vergleicht App-V die Dateinamenerweiterung mit der Liste, wenn die Anwendung, die dem Erweiterungspunkt zugeordnet ist, lokal installiert ist. Wenn sich die Erweiterung befindet, wird der **RunVirtual** -Befehlszeilenparameter hinzugefügt, und die Anwendung wird praktisch ausgeführt.<br>Weitere Informationen zum **RunVirtual** -Parameter finden Sie unter [Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierten Anwendungen](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications51.md). | Zeichenfolge | Integration\VirtualizableExtensions | Richtlinienwert nicht geschrieben |
| ReportingEnabled | Ist nicht verfügbar. | Ermöglicht es dem Client, Informationen an einen Berichtsserver zurückzugeben. | True (aktiviert); Falsch (deaktivierter Zustand) | Reporting\EnableReporting | False |
| ReportingServerURL | Ist nicht verfügbar. | Gibt den Speicherort auf dem Berichtsserver an, auf dem Clientinformationen gespeichert werden. | Zeichenfolge | Reporting\ReportingServer | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| ReportingDataCacheLimit | Ist nicht verfügbar. | Gibt die maximale Größe in Megabyte (MB) des XML-Caches zum Speichern von Berichtsinformationen an. Die Größe bezieht sich auf den Cache im Arbeitsspeicher. Wenn das Limit erreicht ist, wird die Protokolldatei überschrieben. Zwischen 0 und 1024. | Ganzzahl [0-1024] | Reporting\DataCacheLimit | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| ReportingDataBlockSize| Ist nicht verfügbar. | Gibt die maximale Größe in Bytes an, die an den Server gesendet werden soll, um Upload-Anforderungen zu melden. Dies kann dazu beitragen, dauerhafte Übertragungsfehler zu vermeiden, wenn das Protokoll eine signifikante Größe erreicht hat. Zwischen 1024 und unbegrenzt eingestellt. | Ganzzahl [1024-unbegrenzt] | Reporting\DataBlockSize | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| ReportingStartTime | Ist nicht verfügbar. | Gibt den Zeitpunkt an, zu dem der Client initiiert werden soll, um Daten an den Berichtsserver zu senden. Sie müssen eine gültige Ganzzahl zwischen 0-23 angeben, die der Stunde des Tages entspricht. Standardmäßig wird der **ReportingStartTime** am aktuellen Tag um 10 P. M oder 22 gestartet.<br>**Hinweis** Sie sollten diese Einstellung auf einen Zeitpunkt konfigurieren, zu dem Computer, auf denen der App-V 5,1-Client ausgeführt wird, am ehesten offline sind. | Ganzzahl (0 – 23) | Berichterstellung \ Startzeit | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| ReportingInterval | Ist nicht verfügbar. | Gibt das Wiederholungsintervall an, das vom Client zum erneuten Senden von Daten an den Berichtsserver verwendet wird. | Ganze Zahl | Reporting\RetryInterval | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| ReportingRandomDelay | Ist nicht verfügbar. | Gibt die maximale Verzögerung (in Minuten) für Daten an, die an den Berichtsserver gesendet werden sollen. Wenn der geplante Task gestartet wird, generiert der Client eine zufällige Verzögerung zwischen 0 und **ReportingRandomDelay** und wartet die angegebene Dauer vor dem Senden von Daten. Dies kann dazu beitragen, Kollisionen auf dem Server zu verhindern. | Ganzzahl [0-ReportingRandomDelay] | Reporting\RandomDelay | Richtlinienwert nicht geschrieben (identisch mit nicht konfiguriert) |
| EnableDynamicVirtualization<br>**Wichtig** Diese Einstellung ist nur mit App-V 5,0 SP2 oder höher verfügbar. | Ist nicht verfügbar. | Ermöglicht unterstützte Shell-Erweiterungen, Browser-helferobjekte und ActiveX-Steuerelemente, die virtualisiert und mit virtuellen Anwendungen ausgeführt werden können. | 1 (aktiviert), 0 (deaktiviert) | HKEY_LOCAL_MACHINE \software\microsoft\appv\client\virtualization | |
| EnablePublishingRefreshUI<br>**Wichtig** Diese Einstellung ist nur mit App-V 5,0 SP2 verfügbar. | Ist nicht verfügbar. | Aktiviert die Statusleiste für die Veröffentlichungsaktualisierung für den Computer, auf dem der App-V 5,1-Client ausgeführt wird. | 1 (aktiviert), 0 (deaktiviert) | HKEY_LOCAL_MACHINE \software\microsoft\appv\client\publishing | |
| HideUI<br>**Wichtig**  Diese Einstellung ist nur mit App-V 5,0 SP2 verfügbar.| Ist nicht verfügbar. | Blendet die Statusleiste der Veröffentlichungsaktualisierung aus. | 1 (aktiviert), 0 (deaktiviert) | | |
| ProcessesUsingVirtualComponents | Ist nicht verfügbar. | Gibt eine Liste von Prozess Pfaden an (die möglicherweise Platzhalter enthalten), die Kandidaten für die Verwendung der dynamischen Virtualisierung sind (unterstützte Shell-Erweiterungen, Browser-helferobjekte und ActiveX-Steuerelemente). Nur Prozesse, deren vollständiger Pfad einem dieser Elemente entspricht, können Dynamic Virtualization verwenden. | Zeichenfolge | Virtualization\ProcessesUsingVirtualComponents | Leere Zeichenfolge. |






## Verwandte Themen


[Bereitstellen von App-V 5.1-Sequencer und -Client](deploying-the-app-v-51-sequencer-and-client.md)

[Ändern der App-V 5.1-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

[So stellen Sie App-V-Client bereit](how-to-deploy-the-app-v-client-51gb18030.md)

 

 





