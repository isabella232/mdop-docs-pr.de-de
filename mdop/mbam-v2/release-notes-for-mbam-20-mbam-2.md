---
title: Versionshinweise für MBAM 2.0
description: Versionshinweise für MBAM 2.0
author: dansimp
ms.assetid: c3f16cf3-94f2-47ac-b3a4-3dc505c6a8dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d5d3c7d539cf2828d28c1844321bc34ab7736ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811245"
---
# Versionshinweise für MBAM 2.0


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft BitLockerAdministration and Monitoring (MBAM) 2.0 installieren. Diese Versionshinweise enthalten Informationen, die erforderlich sind, um BitLockerAdministration und Monitoring 2.0 erfolgreich zu installieren und Informationen zu enthalten, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderer mbam 2.0-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## <a href="" id="---------mbam-2-0-known-issues"></a> Bekannte Probleme mit mbam 2.0


Dieser Abschnitt enthält Anmerkungen zu dieser Version von mbam 2.0.

### Das Feld "Computer Name" wird möglicherweise nicht in den Berichten zur BitLocker-Computer Konformität und BitLocker Enterprise-Konformitäts Details angezeigt, wenn Sie MBAM mit Microsoft System Center Configuration Manager 2007 ausführen

Das Feld Computer Name ist möglicherweise in den Berichten BitLocker Computer Compliance und BitLocker Enterprise Compliance Details leer, wenn Sie MBAM mit Configuration Manager 2007 verwenden.

Problemumgehung: keine.

### Der Enterprise-Konformitätsbericht kann nach dem Upgrade der eigenständigen MBAM-Serverinfrastruktur nicht aktualisiert werden

Wenn Sie die eigenständige MBAM-Topologie verwenden und die Serverinfrastruktur von Version 1,0 auf 2,0 aktualisieren, kann der Enterprise-Konformitätsbericht nicht aktualisiert werden.

Problemumgehung: führen Sie nach dem Upgrade das folgende Skript in der Datenbank Compliance und Audit aus:

```sql
-- =============================================
-- Script Template
-- =============================================

DECLARE @DatabaseName nvarchar(255);
SET @DatabaseName = DB_NAME()

USE msdb;

DECLARE @JobID BINARY(16)
SELECT @JobID = job_id
FROM msdb.dbo.sysjobs
WHERE (name = N'CreateCache')

if (@JobID IS NOT NULL)
BEGIN
    EXEC dbo.sp_delete_job
         @job_name = N'CreateCache';
END

EXEC dbo.sp_add_job
    @job_name = N'CreateCache',
    @enabled = 1;

EXEC dbo.sp_add_jobstep
     @job_name = N'CreateCache',
     @step_name = N'Copy Data',
     @subsystem = N'TSQL',
     @command = N'EXEC [ComplianceCore].UpdateCache',
     @database_name = @DatabaseName,
     @retry_attempts = 5,
     @retry_interval = 5;


EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 010000,
     @active_end_time = 020000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 070000,
     @active_end_time = 080000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 130000,
     @active_end_time = 140000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1pm';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 190000,
     @active_end_time = 200000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7pm';

EXEC dbo.sp_add_jobserver
     @job_name = N'CreateCache';
```

### Berichte auf dem Helpdesk-Portal zeigen eine Warnung an, wenn SSL in SSRS nicht konfiguriert ist

Wenn SQL Server Reporting Services (SSRS) nicht für die Verwendung von Secure Socket Layer (SSL) konfiguriert wurde, wird die URL für die Berichte bei der Installation des MBAM-Servers auf http statt auf HTTPS festgelegt. Wenn Sie dann zum Helpdesk-Portal wechseln und einen Bericht auswählen, wird die folgende Meldung angezeigt: "nur sicherer Inhalt wird angezeigt."

Problemumgehung: Wenn Sie den Bericht anzeigen möchten, klicken Sie auf **alle Inhalte anzeigen**. Um dieses Problem zu beheben, wechseln Sie zum MBAM-Computer, auf dem SQL Server Reporting Services installiert ist, führen Sie den **Reporting Services-Konfigurations-Manager**aus, und klicken Sie dann auf **Webdienst-URL**. Wählen Sie das entsprechende SSL-Zertifikat für den Server aus, geben Sie den entsprechenden SSL-Port ein (der Standardport ist 443), und klicken Sie dann auf über **nehmen**.

### Nicht standardmäßige Instanzen der Configuration Manager-Datenbank werden nicht unterstützt.

MBAM sucht nur nach der Standardinstanz der Configuration Manager-Datenbank in Configuration Manager 2007 und SystemCenter2012 ConfigurationManager. Wenn Sie eine nicht standardmäßige Instanz verwenden, können Sie MBAM nicht installieren.

Problemumgehung: keine.

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a>Wenn Sie im Kompatibilitäts Zusammenfassungsbericht auf "zurück" klicken, wird möglicherweise ein Fehler ausgelöst.

Wenn Sie einen Drilldown in einen Kompatibilitäts Zusammenfassungsbericht ausführen und dann im SSRS-Bericht auf den Link **zurück** klicken, wird möglicherweise ein Fehler ausgelöst.

Problemumgehung: keine.

### Verwendeter Speicherplatz nur die Verschlüsselung funktioniert nicht ordnungsgemäß

Wenn Sie einen Computer nach der Installation des MBAM-Clients zum ersten Mal verschlüsseln und ein Gruppenrichtlinienobjekt für die Implementierung der nur verwendeter Speicherplatz Verschlüsselung festgesetzt haben, verschlüsselt MBAM fälschlicherweise den gesamten Datenträger, anstatt nur den verwendeten Speicherplatz der Festplatte zu verschlüsseln. Wenn ein Computer bereits verschlüsselt ist, wenn Sie den MBAM-Client installieren, und Sie das gleiche Gruppenrichtlinienobjekt festgesetzt haben, funktioniert die Verschlüsselung ordnungsgemäß und verschlüsselt nur den verwendeten Speicherplatz auf Ihrem Computer.

Problemumgehung: keine.

### Die Verschlüsselungsstärke wird im Computer Kompatibilitätsbericht falsch angezeigt

Wenn Sie keine bestimmte Verschlüsselungsstärke in den Gruppenrichtlinienobjekten " **Laufwerksverschlüsselung auswählen" und "Verschlüsselungsstärke"** festlegen, wird im Bericht zur Computer Konformität in der Configuration Manager-Integrations Topologie immer "unbekannt" für die Verschlüsselungsstärke angezeigt, selbst wenn die Verschlüsselungsstärke den Standardwert der 128-Bit-Verschlüsselung verwendet. Der Bericht zeigt die richtige Verschlüsselungsstärke an, wenn Sie eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt festlegen.

Problemumgehung: Legen Sie immer eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt **Auswählen von Laufwerk Verschlüsselungsmethode und Verschlüsselungsstärke** fest.

### Kompatibilitäts Status Verteilung nach Laufwerks zeigt alte Daten an, nachdem Sie Konfigurationselemente aktualisiert haben

Nachdem Sie MBAM-Konfigurationselemente in SystemCenter2012 ConfigurationManager aktualisiert haben, werden auf dem BitLocker Enterprise Compliance-Dashboard Daten angezeigt, die auf Informationen aus älteren Versionen der Konfigurationselemente basieren.

Problemumgehung: keine. Änderungen der MBAM-Konfigurationselemente werden nicht unterstützt, und der Bericht wird möglicherweise nicht wie erwartet angezeigt.

### Verbesserte Sicherheitskonfiguration kann dazu führen, dass Berichte falsch angezeigt werden

Wenn Internet Explorer Enhanced Security Configuration (ESC) aktiviert ist, wird möglicherweise eine Meldung "Zugriff verweigert" angezeigt, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen. Standardmäßig ist ESC aktiviert, um den Server zu schützen, indem die Anfälligkeit des Servers für potenzielle Angriffe verringert wird, die über Webinhalte und Anwendungsskripts auftreten können.

Problemumgehung: Wenn die Meldung "Zugriff verweigert" angezeigt wird, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen, können Sie ein Gruppenrichtlinienobjekt festlegen oder den Standardwert manuell in Ihrem Bild ändern, um die erweiterte Sicherheitskonfiguration zu deaktivieren. Sie können auch die Berichte auf einem anderen Computer anzeigen, auf dem ESC nicht aktiviert ist.

### MBAM Server-Installation schlägt beim Upgrade von SQL Server 2008 auf SQL Server 2012 fehl

Wenn Sie ein Upgrade von SQL Server 2008 auf SQL Server 2012 durchführen und dann versuchen, die Kompatibilitäts-und Überwachungsdatenbank oder die Wiederherstellungsdatenbank zu installieren, schlägt die Installation fehl, und es wird ein Rollback ausgeführt. Der Fehler tritt auf, weil die erforderliche SQLCMD.exe Datei während des SQL-Upgrades entfernt wurde und vom MBAM-Installationsprogramm nicht gefunden werden kann. Die MSI-Protokolldateizeilen können wie folgt aussehen:

RunDbInstallScript Recovery DB ca: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery DB ca: dbinstance-xxxxxx\\I01RunDbInstallScript Recovery DB ca: SqlScript-c:\\Programme Files\\Microsoft\\Microsoft BitLocker-Verwaltung und Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB ca: dbname-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript Recovery DB ca: DefaultFileName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript Recovery DB ca: defaultDataPath-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript Recovery DB ca: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript Recovery DB ca: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-e-S xxxxxxx\\I01-i "c:\\Programme Files\\Microsoft\\Microsoft BitLocker-Verwaltung und Monitoring\\Setup\\KeyRecovery.SQL"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery DB ca: Starten der Ausführung der Wiederherstellungs-Datenbank installieren scriptRunDbInstallScript Recovery DB ca: die sqlcmd-Protokolldatei befindet sich in der C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript-Wiederherstellungs-DB-ca-Ausnahme: benutzerdefinierte Aktion der Wiederherstellungsdatenbank-Befehlszeile-Ausgabe Ausnahme: das System kann die angegebene Datei nicht finden

Der MBAM-Server-Windows-Installer ist hart codiert, um den SQLCMD.exe Pfad zu finden, indem Sie in der Registrierung unter HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup. den Pfadzeichen folgen Wert suchen. Der Schlüssel ist weiterhin während der Migration von SQL Server 2008 zu SQL Server 2012 vorhanden, aber der Pfad, auf den der Datenwert verweist, enthält die SQLCMD.exe Datei nicht, da der SQL-Upgradeprozess die Datei entfernt hat.

Problemumgehung: benennen Sie den HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path-Zeichenfolgenwert vorübergehend in **path \ _old**um, und führen Sie dann den MBAM Server Windows Installer erneut aus. Wenn die Installation erfolgreich abgeschlossen und die Datenbanken in SQL Server 2012 erstellt wurde, benennen Sie den **Pfad \ _old** Wert in **path**um.

## Hotfixes und Knowledge Base-Artikel für mbam 2.0


Dieser Abschnitt enthält Hotfixes und KB-Artikel für mbam 2.0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>KB-Artikel</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>Das Installieren der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 schlägt fehl, wenn &quot; System Center cm-Objekte bereits installiert sind&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>Benutzer können den BitLocker-Wiederherstellungsschlüssel nicht über das Self-Service-Portal von mbam 2.0 abrufen</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>MBAM-Client schlägt mit Ereignis-ID 4 und Fehlercode 0x8004100E in der Ereignisbeschreibung fehl</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>Fehlermeldung "Server Fehler in der Anwendung"/Reports ", wenn Sie in MBAM auf die Registerkarte" Berichte "klicken</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Fehler beim Öffnen von Enterprise-oder Computer Kompatibilitätsberichten in MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM Enterprise-Berichte werden nicht aktualisiert</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>Die Installation von MBAM auf einem Domänen Controller wird nicht unterstützt.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>Sie erhalten Fehlercode 0x80071a90 während des Standalone-oder Configuration Manager-Integrations Setups von mbam 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM und sichere Netzwerkkommunikation</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>Mbam 2.0-Setup schlägt während des Configuration Manager-Integrationsszenarios mit SQL Server 2008 fehl</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>MBAM-Setup schlägt fehl, wenn SQL SSRS nicht ordnungsgemäß konfiguriert ist</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>MBAM 2,0-Setup schlägt fehl, wenn &quot; Fehler beim Abrufen der Configuration Manager-Server Rolleneinstellungen für &#39;Reporting Services-Point&#39; Rolle auftreten&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>Mbam 2.0-Enterprise-Berichte werden in der eigenständigen mbam 2.0-Topologie aufgrund des SQL-Auftrags createcache-Fehlers nicht aktualisiert</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM Enterprise-Berichte werden nicht aktualisiert</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>Kompatibilitätsberichte von MBAM-unterstützten Computern enthalten fehlerhafte nicht unterstützte Produkte</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>Der Computer Eintrag wird in MBAM abgelehnt.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Informationen zu MBAM 2.0](about-mbam-20-mbam-2.md)

 

 





