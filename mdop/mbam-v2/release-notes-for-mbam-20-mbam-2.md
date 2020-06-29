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
# <span data-ttu-id="d33a4-103">Versionshinweise für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d33a4-103">Release Notes for MBAM 2.0</span></span>


<span data-ttu-id="d33a4-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="d33a4-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="d33a4-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft BitLockerAdministration and Monitoring (MBAM) 2.0 installieren.</span><span class="sxs-lookup"><span data-stu-id="d33a4-105">Read these release notes thoroughly before you install Microsoft BitLockerAdministration and Monitoring(MBAM)2.0.</span></span> <span data-ttu-id="d33a4-106">Diese Versionshinweise enthalten Informationen, die erforderlich sind, um BitLockerAdministration und Monitoring 2.0 erfolgreich zu installieren und Informationen zu enthalten, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d33a4-106">These release notes contain information that is required to successfully install BitLockerAdministration and Monitoring2.0 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="d33a4-107">Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderer mbam 2.0-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="d33a4-107">If there is a difference between these release notes and other MBAM2.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="d33a4-108">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d33a4-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-known-issues"></a> <span data-ttu-id="d33a4-109">Bekannte Probleme mit mbam 2.0</span><span class="sxs-lookup"><span data-stu-id="d33a4-109">MBAM2.0 Known Issues</span></span>


<span data-ttu-id="d33a4-110">Dieser Abschnitt enthält Anmerkungen zu dieser Version von mbam 2.0.</span><span class="sxs-lookup"><span data-stu-id="d33a4-110">This section contains release notes for MBAM2.0.</span></span>

### <span data-ttu-id="d33a4-111">Das Feld "Computer Name" wird möglicherweise nicht in den Berichten zur BitLocker-Computer Konformität und BitLocker Enterprise-Konformitäts Details angezeigt, wenn Sie MBAM mit Microsoft System Center Configuration Manager 2007 ausführen</span><span class="sxs-lookup"><span data-stu-id="d33a4-111">Computer Name field may not appear in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007</span></span>

<span data-ttu-id="d33a4-112">Das Feld Computer Name ist möglicherweise in den Berichten BitLocker Computer Compliance und BitLocker Enterprise Compliance Details leer, wenn Sie MBAM mit Configuration Manager 2007 verwenden.</span><span class="sxs-lookup"><span data-stu-id="d33a4-112">The Computer Name field may be blank in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you use MBAM with Configuration Manager 2007.</span></span>

<span data-ttu-id="d33a4-113">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="d33a4-113">WORKAROUND: None.</span></span>

### <span data-ttu-id="d33a4-114">Der Enterprise-Konformitätsbericht kann nach dem Upgrade der eigenständigen MBAM-Serverinfrastruktur nicht aktualisiert werden</span><span class="sxs-lookup"><span data-stu-id="d33a4-114">Enterprise Compliance Report fails to update after you upgrade the Stand-alone MBAM server infrastructure</span></span>

<span data-ttu-id="d33a4-115">Wenn Sie die eigenständige MBAM-Topologie verwenden und die Serverinfrastruktur von Version 1,0 auf 2,0 aktualisieren, kann der Enterprise-Konformitätsbericht nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d33a4-115">If you are using the MBAM Stand-alone topology, and you upgrade the server infrastructure from version 1.0 to 2.0, the Enterprise Compliance Report fails to update.</span></span>

<span data-ttu-id="d33a4-116">Problemumgehung: führen Sie nach dem Upgrade das folgende Skript in der Datenbank Compliance und Audit aus:</span><span class="sxs-lookup"><span data-stu-id="d33a4-116">WORKAROUND: After the upgrade, run the following script on the Compliance and Audit Database:</span></span>

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

### <span data-ttu-id="d33a4-117">Berichte auf dem Helpdesk-Portal zeigen eine Warnung an, wenn SSL in SSRS nicht konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="d33a4-117">Reports in the Help Desk Portal display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="d33a4-118">Wenn SQL Server Reporting Services (SSRS) nicht für die Verwendung von Secure Socket Layer (SSL) konfiguriert wurde, wird die URL für die Berichte bei der Installation des MBAM-Servers auf http statt auf HTTPS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d33a4-118">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="d33a4-119">Wenn Sie dann zum Helpdesk-Portal wechseln und einen Bericht auswählen, wird die folgende Meldung angezeigt: "nur sicherer Inhalt wird angezeigt."</span><span class="sxs-lookup"><span data-stu-id="d33a4-119">If you then browse to the Help Desk Portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="d33a4-120">Problemumgehung: Wenn Sie den Bericht anzeigen möchten, klicken Sie auf **alle Inhalte anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="d33a4-120">WORKAROUND: To show the report, click **Show All Content**.</span></span> <span data-ttu-id="d33a4-121">Um dieses Problem zu beheben, wechseln Sie zum MBAM-Computer, auf dem SQL Server Reporting Services installiert ist, führen Sie den **Reporting Services-Konfigurations-Manager**aus, und klicken Sie dann auf **Webdienst-URL**.</span><span class="sxs-lookup"><span data-stu-id="d33a4-121">To address this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="d33a4-122">Wählen Sie das entsprechende SSL-Zertifikat für den Server aus, geben Sie den entsprechenden SSL-Port ein (der Standardport ist 443), und klicken Sie dann auf über **nehmen**.</span><span class="sxs-lookup"><span data-stu-id="d33a4-122">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="d33a4-123">Nicht standardmäßige Instanzen der Configuration Manager-Datenbank werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d33a4-123">Non-default instances of the Configuration Manager database are not supported</span></span>

<span data-ttu-id="d33a4-124">MBAM sucht nur nach der Standardinstanz der Configuration Manager-Datenbank in Configuration Manager 2007 und SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="d33a4-124">MBAM looks only for the default instance of the Configuration Manager database in Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="d33a4-125">Wenn Sie eine nicht standardmäßige Instanz verwenden, können Sie MBAM nicht installieren.</span><span class="sxs-lookup"><span data-stu-id="d33a4-125">If you use a non-default instance, you cannot install MBAM.</span></span>

<span data-ttu-id="d33a4-126">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="d33a4-126">WORKAROUND: None.</span></span>

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a><span data-ttu-id="d33a4-127">Wenn Sie im Kompatibilitäts Zusammenfassungsbericht auf "zurück" klicken, wird möglicherweise ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d33a4-127">Clicking “Back” in the Compliance Summary report might throw an error</span></span>

<span data-ttu-id="d33a4-128">Wenn Sie einen Drilldown in einen Kompatibilitäts Zusammenfassungsbericht ausführen und dann im SSRS-Bericht auf den Link **zurück** klicken, wird möglicherweise ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d33a4-128">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="d33a4-129">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="d33a4-129">WORKAROUND: None.</span></span>

### <span data-ttu-id="d33a4-130">Verwendeter Speicherplatz nur die Verschlüsselung funktioniert nicht ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="d33a4-130">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="d33a4-131">Wenn Sie einen Computer nach der Installation des MBAM-Clients zum ersten Mal verschlüsseln und ein Gruppenrichtlinienobjekt für die Implementierung der nur verwendeter Speicherplatz Verschlüsselung festgesetzt haben, verschlüsselt MBAM fälschlicherweise den gesamten Datenträger, anstatt nur den verwendeten Speicherplatz der Festplatte zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="d33a4-131">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="d33a4-132">Wenn ein Computer bereits verschlüsselt ist, wenn Sie den MBAM-Client installieren, und Sie das gleiche Gruppenrichtlinienobjekt festgesetzt haben, funktioniert die Verschlüsselung ordnungsgemäß und verschlüsselt nur den verwendeten Speicherplatz auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="d33a4-132">If a computer is already encrypted when you install the MBAM Client, and you have set the same Group Policy Object, the encryption works correctly and encrypts only the used disk space on your computer.</span></span>

<span data-ttu-id="d33a4-133">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="d33a4-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="d33a4-134">Die Verschlüsselungsstärke wird im Computer Kompatibilitätsbericht falsch angezeigt</span><span class="sxs-lookup"><span data-stu-id="d33a4-134">Cipher strength displays incorrectly on the Computer Compliance report</span></span>

<span data-ttu-id="d33a4-135">Wenn Sie keine bestimmte Verschlüsselungsstärke in den Gruppenrichtlinienobjekten " **Laufwerksverschlüsselung auswählen" und "Verschlüsselungsstärke"** festlegen, wird im Bericht zur Computer Konformität in der Configuration Manager-Integrations Topologie immer "unbekannt" für die Verschlüsselungsstärke angezeigt, selbst wenn die Verschlüsselungsstärke den Standardwert der 128-Bit-Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d33a4-135">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager Integration topology always displays “unknown” for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="d33a4-136">Der Bericht zeigt die richtige Verschlüsselungsstärke an, wenn Sie eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="d33a4-136">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="d33a4-137">Problemumgehung: Legen Sie immer eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt **Auswählen von Laufwerk Verschlüsselungsmethode und Verschlüsselungsstärke** fest.</span><span class="sxs-lookup"><span data-stu-id="d33a4-137">WORKAROUND: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="d33a4-138">Kompatibilitäts Status Verteilung nach Laufwerks zeigt alte Daten an, nachdem Sie Konfigurationselemente aktualisiert haben</span><span class="sxs-lookup"><span data-stu-id="d33a4-138">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="d33a4-139">Nachdem Sie MBAM-Konfigurationselemente in SystemCenter2012 ConfigurationManager aktualisiert haben, werden auf dem BitLocker Enterprise Compliance-Dashboard Daten angezeigt, die auf Informationen aus älteren Versionen der Konfigurationselemente basieren.</span><span class="sxs-lookup"><span data-stu-id="d33a4-139">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="d33a4-140">Problemumgehung: keine.</span><span class="sxs-lookup"><span data-stu-id="d33a4-140">WORKAROUND: None.</span></span> <span data-ttu-id="d33a4-141">Änderungen der MBAM-Konfigurationselemente werden nicht unterstützt, und der Bericht wird möglicherweise nicht wie erwartet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d33a4-141">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="d33a4-142">Verbesserte Sicherheitskonfiguration kann dazu führen, dass Berichte falsch angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="d33a4-142">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="d33a4-143">Wenn Internet Explorer Enhanced Security Configuration (ESC) aktiviert ist, wird möglicherweise eine Meldung "Zugriff verweigert" angezeigt, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d33a4-143">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an “Access Denied” message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="d33a4-144">Standardmäßig ist ESC aktiviert, um den Server zu schützen, indem die Anfälligkeit des Servers für potenzielle Angriffe verringert wird, die über Webinhalte und Anwendungsskripts auftreten können.</span><span class="sxs-lookup"><span data-stu-id="d33a4-144">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="d33a4-145">Problemumgehung: Wenn die Meldung "Zugriff verweigert" angezeigt wird, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen, können Sie ein Gruppenrichtlinienobjekt festlegen oder den Standardwert manuell in Ihrem Bild ändern, um die erweiterte Sicherheitskonfiguration zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d33a4-145">WORKAROUND: If the “Access Denied” message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="d33a4-146">Sie können auch die Berichte auf einem anderen Computer anzeigen, auf dem ESC nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d33a4-146">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="d33a4-147">MBAM Server-Installation schlägt beim Upgrade von SQL Server 2008 auf SQL Server 2012 fehl</span><span class="sxs-lookup"><span data-stu-id="d33a4-147">MBAM Server installation fails when you upgrade from SQL Server 2008 to SQL Server 2012</span></span>

<span data-ttu-id="d33a4-148">Wenn Sie ein Upgrade von SQL Server 2008 auf SQL Server 2012 durchführen und dann versuchen, die Kompatibilitäts-und Überwachungsdatenbank oder die Wiederherstellungsdatenbank zu installieren, schlägt die Installation fehl, und es wird ein Rollback ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d33a4-148">If you upgrade from SQL Server 2008 to SQL Server 2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="d33a4-149">Der Fehler tritt auf, weil die erforderliche SQLCMD.exe Datei während des SQL-Upgrades entfernt wurde und vom MBAM-Installationsprogramm nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="d33a4-149">The failure occurs because the required SQLCMD.exe file was removed during the SQL upgrade and cannot be found by the MBAM installer.</span></span> <span data-ttu-id="d33a4-150">Die MSI-Protokolldateizeilen können wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="d33a4-150">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="d33a4-151">RunDbInstallScript Recovery DB ca: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery DB ca: dbinstance-xxxxxx\\I01RunDbInstallScript Recovery DB ca: SqlScript-c:\\Programme Files\\Microsoft\\Microsoft BitLocker-Verwaltung und Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB ca: dbname-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript Recovery DB ca: DefaultFileName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript Recovery DB ca: defaultDataPath-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript Recovery DB ca: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript Recovery DB ca: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-e-S xxxxxxx\\I01-i "c:\\Programme Files\\Microsoft\\Microsoft BitLocker-Verwaltung und Monitoring\\Setup\\KeyRecovery.SQL"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery DB ca: Starten der Ausführung der Wiederherstellungs-Datenbank installieren scriptRunDbInstallScript Recovery DB ca: die sqlcmd-Protokolldatei befindet sich in der C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript-Wiederherstellungs-DB-ca-Ausnahme: benutzerdefinierte Aktion der Wiederherstellungsdatenbank-Befehlszeile-Ausgabe Ausnahme: das System kann die angegebene Datei nicht finden</span><span class="sxs-lookup"><span data-stu-id="d33a4-151">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="d33a4-152">Der MBAM-Server-Windows-Installer ist hart codiert, um den SQLCMD.exe Pfad zu finden, indem Sie in der Registrierung unter HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup. den Pfadzeichen folgen Wert suchen.</span><span class="sxs-lookup"><span data-stu-id="d33a4-152">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="d33a4-153">Der Schlüssel ist weiterhin während der Migration von SQL Server 2008 zu SQL Server 2012 vorhanden, aber der Pfad, auf den der Datenwert verweist, enthält die SQLCMD.exe Datei nicht, da der SQL-Upgradeprozess die Datei entfernt hat.</span><span class="sxs-lookup"><span data-stu-id="d33a4-153">The key is still present during the migration from SQL Server 2008 to SQL Server 2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQL upgrade process removed the file.</span></span>

<span data-ttu-id="d33a4-154">Problemumgehung: benennen Sie den HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path-Zeichenfolgenwert vorübergehend in **path \ _old**um, und führen Sie dann den MBAM Server Windows Installer erneut aus.</span><span class="sxs-lookup"><span data-stu-id="d33a4-154">WORKAROUND: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path string value to **Path\_old**, and then re-run the MBAM Server Windows Installer.</span></span> <span data-ttu-id="d33a4-155">Wenn die Installation erfolgreich abgeschlossen und die Datenbanken in SQL Server 2012 erstellt wurde, benennen Sie den **Pfad \ _old** Wert in **path**um.</span><span class="sxs-lookup"><span data-stu-id="d33a4-155">When the installation completes successfully and creates the databases in SQL Server 2012, rename the **Path\_old** value to **Path**.</span></span>

## <span data-ttu-id="d33a4-156">Hotfixes und Knowledge Base-Artikel für mbam 2.0</span><span class="sxs-lookup"><span data-stu-id="d33a4-156">Hotfixes and Knowledge Base articles for MBAM2.0</span></span>


<span data-ttu-id="d33a4-157">Dieser Abschnitt enthält Hotfixes und KB-Artikel für mbam 2.0.</span><span class="sxs-lookup"><span data-stu-id="d33a4-157">This section contains hotfixes and KB articles for MBAM2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="d33a4-158">KB-Artikel</span><span class="sxs-lookup"><span data-stu-id="d33a4-158">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="d33a4-159">Title</span><span class="sxs-lookup"><span data-stu-id="d33a4-159">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="d33a4-160">Link</span><span class="sxs-lookup"><span data-stu-id="d33a4-160">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d33a4-161">2831166</span><span class="sxs-lookup"><span data-stu-id="d33a4-161">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-162">Das Installieren der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 schlägt fehl, wenn &quot; System Center cm-Objekte bereits installiert sind&quot;</span><span class="sxs-lookup"><span data-stu-id="d33a4-162">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="d33a4-163">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-163">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d33a4-164">2870849</span><span class="sxs-lookup"><span data-stu-id="d33a4-164">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-165">Benutzer können den BitLocker-Wiederherstellungsschlüssel nicht über das Self-Service-Portal von mbam 2.0 abrufen</span><span class="sxs-lookup"><span data-stu-id="d33a4-165">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="d33a4-166">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-166">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d33a4-167">2756402</span><span class="sxs-lookup"><span data-stu-id="d33a4-167">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-168">MBAM-Client schlägt mit Ereignis-ID 4 und Fehlercode 0x8004100E in der Ereignisbeschreibung fehl</span><span class="sxs-lookup"><span data-stu-id="d33a4-168">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="d33a4-169">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-169">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d33a4-170">2620287</span><span class="sxs-lookup"><span data-stu-id="d33a4-170">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-171">Fehlermeldung "Server Fehler in der Anwendung"/Reports ", wenn Sie in MBAM auf die Registerkarte" Berichte "klicken</span><span class="sxs-lookup"><span data-stu-id="d33a4-171">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="d33a4-172">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-172">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d33a4-173">2639518</span><span class="sxs-lookup"><span data-stu-id="d33a4-173">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-174">Fehler beim Öffnen von Enterprise-oder Computer Kompatibilitätsberichten in MBAM</span><span class="sxs-lookup"><span data-stu-id="d33a4-174">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="d33a4-175">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-175">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d33a4-176">2620269</span><span class="sxs-lookup"><span data-stu-id="d33a4-176">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-177">MBAM Enterprise-Berichte werden nicht aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d33a4-177">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="d33a4-178">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-178">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d33a4-179">2712461</span><span class="sxs-lookup"><span data-stu-id="d33a4-179">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-180">Die Installation von MBAM auf einem Domänen Controller wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d33a4-180">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="d33a4-181">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-181">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d33a4-182">2876732</span><span class="sxs-lookup"><span data-stu-id="d33a4-182">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-183">Sie erhalten Fehlercode 0x80071a90 während des Standalone-oder Configuration Manager-Integrations Setups von mbam 2.0</span><span class="sxs-lookup"><span data-stu-id="d33a4-183">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="d33a4-184">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-184">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d33a4-185">2754259</span><span class="sxs-lookup"><span data-stu-id="d33a4-185">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-186">MBAM und sichere Netzwerkkommunikation</span><span class="sxs-lookup"><span data-stu-id="d33a4-186">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="d33a4-187">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-187">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d33a4-188">2870842</span><span class="sxs-lookup"><span data-stu-id="d33a4-188">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-189">Mbam 2.0-Setup schlägt während des Configuration Manager-Integrationsszenarios mit SQL Server 2008 fehl</span><span class="sxs-lookup"><span data-stu-id="d33a4-189">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="d33a4-190">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-190">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d33a4-191">2668533</span><span class="sxs-lookup"><span data-stu-id="d33a4-191">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-192">MBAM-Setup schlägt fehl, wenn SQL SSRS nicht ordnungsgemäß konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="d33a4-192">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="d33a4-193">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-193">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d33a4-194">2870847</span><span class="sxs-lookup"><span data-stu-id="d33a4-194">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-195">MBAM 2,0-Setup schlägt fehl, wenn &quot; Fehler beim Abrufen der Configuration Manager-Server Rolleneinstellungen für &#39;Reporting Services-Point&#39; Rolle auftreten&quot;</span><span class="sxs-lookup"><span data-stu-id="d33a4-195">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="d33a4-196">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-196">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d33a4-197">2870839</span><span class="sxs-lookup"><span data-stu-id="d33a4-197">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-198">Mbam 2.0-Enterprise-Berichte werden in der eigenständigen mbam 2.0-Topologie aufgrund des SQL-Auftrags createcache-Fehlers nicht aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d33a4-198">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="d33a4-199">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-199">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d33a4-200">2620269</span><span class="sxs-lookup"><span data-stu-id="d33a4-200">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-201">MBAM Enterprise-Berichte werden nicht aktualisiert</span><span class="sxs-lookup"><span data-stu-id="d33a4-201">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="d33a4-202">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-202">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d33a4-203">2935997</span><span class="sxs-lookup"><span data-stu-id="d33a4-203">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-204">Kompatibilitätsberichte von MBAM-unterstützten Computern enthalten fehlerhafte nicht unterstützte Produkte</span><span class="sxs-lookup"><span data-stu-id="d33a4-204">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="d33a4-205">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-205">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d33a4-206">2612822</span><span class="sxs-lookup"><span data-stu-id="d33a4-206">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="d33a4-207">Der Computer Eintrag wird in MBAM abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="d33a4-207">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="d33a4-208">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="d33a4-208">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d33a4-209">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d33a4-209">Related topics</span></span>


[<span data-ttu-id="d33a4-210">Informationen zu MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d33a4-210">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)

 

 





