---
title: Versionshinweise für MBAM 2.0SP1
description: Versionshinweise für MBAM 2.0SP1
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811242"
---
# <span data-ttu-id="bee3e-103">Versionshinweise für MBAM 2.0SP1</span><span class="sxs-lookup"><span data-stu-id="bee3e-103">Release Notes for MBAM 2.0 SP1</span></span>


<span data-ttu-id="bee3e-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="bee3e-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="bee3e-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 Service Pack 1 (SP1) installieren.</span><span class="sxs-lookup"><span data-stu-id="bee3e-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="bee3e-106">Diese Versionshinweise enthalten Informationen, die erforderlich sind, um die BitLocker-Verwaltung und-Überwachung 2,0 SP1 erfolgreich zu installieren, und Sie enthalten Informationen, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="bee3e-106">These release notes contain information that is required to successfully install BitLocker Administration and Monitoring 2.0 SP1, and they contain information that is not available in the product documentation.</span></span> <span data-ttu-id="bee3e-107">Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderen MBAM 2,0 SP1-Dokumentationen gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="bee3e-107">If there is a difference between these release notes and other MBAM 2.0 SP1 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="bee3e-108">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bee3e-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> <span data-ttu-id="bee3e-109">Bekannte Probleme mit MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="bee3e-109">MBAM 2.0 SP1 known issues</span></span>


<span data-ttu-id="bee3e-110">Dieser Abschnitt enthält bekannte Probleme bei MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="bee3e-110">This section contains known issues for MBAM 2.0 SP1.</span></span>

### <span data-ttu-id="bee3e-111">Upgrade von MBAM mit der integrierten Configuration Manager-Topologie auf MBAM 2,0 SP1 erfordert das manuelle Entfernen von Configuration Manager-Objekten</span><span class="sxs-lookup"><span data-stu-id="bee3e-111">Upgrade of MBAM with Configuration Manager Integrated topology to MBAM 2.0 SP1 requires manual removal of Configuration Manager objects</span></span>

<span data-ttu-id="bee3e-112">Wenn Sie MBAM mit Configuration Manager verwenden und ein Upgrade auf MBAM 2,0 SP1 durchführen möchten, müssen Sie alle Configuration Manager-Objekte, die in Configuration Manager installiert wurden, als Teil der MBAM-Installation manuell entfernen.</span><span class="sxs-lookup"><span data-stu-id="bee3e-112">If you are using MBAM with Configuration Manager, and you want to upgrade to MBAM 2.0 SP1, you must manually remove all of the Configuration Manager objects that were installed into Configuration Manager as a part of the MBAM installation.</span></span> <span data-ttu-id="bee3e-113">Bei den Objekten, die Sie manuell entfernen müssen, handelt es sich um die MBAM-Berichte, die MBAM-unterstützten Computersammlung und die BitLocker-Schutz Konfigurationsbasislinie und die zugehörigen Konfigurationselemente.</span><span class="sxs-lookup"><span data-stu-id="bee3e-113">The objects that you must manually remove are the MBAM reports, MBAM Supported Computers collection, and the BitLocker Protection Configuration Baseline and its associated configuration items.</span></span>

<span data-ttu-id="bee3e-114">**Problemumgehung**: Aktualisieren Sie die Configuration Manager-Objekte, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="bee3e-114">**Workaround**: Upgrade the Configuration Manager objects by completing the following steps:</span></span>

1.  <span data-ttu-id="bee3e-115">Sichern Sie vorhandene Kompatibilitätsdaten in einer externen Datei, wie in den folgenden Schritten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bee3e-115">Back up existing compliance data to an external file, as described in the following steps.</span></span>

    <span data-ttu-id="bee3e-116">**Hinweis**  Alle vorhandenen BitLocker-Konformitätsdaten werden gelöscht, wenn Sie den vorhandenen Basisplan in Configuration Manager löschen.</span><span class="sxs-lookup"><span data-stu-id="bee3e-116">**Note** All existing BitLocker compliance data will be deleted when you delete the existing baseline in Configuration Manager.</span></span> <span data-ttu-id="bee3e-117">Die Daten werden im Laufe der Zeit neu generiert, es wird jedoch empfohlen, dass Sie eine Kopie der Daten speichern, falls Sie die Kompatibilitätsdaten für einen bestimmten Computer benötigen, bevor die Kompatibilitätsdaten erneut generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="bee3e-117">The data will be regenerated over time, but it is recommended that you save a copy of the data in case you need the compliance data for a particular computer before the compliance data has been regenerated.</span></span>

     

    1.  <span data-ttu-id="bee3e-118">Zum Speichern von Verlaufsdaten zur BitLocker-Konformität öffnen Sie den **BitLocker Enterprise Compliance-Detail** Bericht.</span><span class="sxs-lookup"><span data-stu-id="bee3e-118">To save historical BitLocker compliance data, open the **BitLocker Enterprise Compliance Details** Report.</span></span>

    2.  <span data-ttu-id="bee3e-119">Klicken Sie im Bericht auf das Symbol **Speichern** , und wählen Sie **Excel**aus.</span><span class="sxs-lookup"><span data-stu-id="bee3e-119">Click the **Save** icon in the report and select **Excel**.</span></span>

        <span data-ttu-id="bee3e-120">Der gespeicherte Bericht enthält Daten wie den Computernamen, den Domänennamen, den Kompatibilitätsstatus, die Ausnahme, die Geräte Benutzer, die Details zum Kompatibilitätsstatus und das Datum/die Uhrzeit des letzten Kontakts.</span><span class="sxs-lookup"><span data-stu-id="bee3e-120">The saved report will contain data such as the computer name, domain name, compliance status, exemption, device users, compliance status details, and last contact date/time.</span></span> <span data-ttu-id="bee3e-121">Einige Informationen wie detaillierte Lautstärke Informationen und Verschlüsselungsstärke werden nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bee3e-121">Some information, such as detailed volume information and encryption strength, are not saved.</span></span>

2.  <span data-ttu-id="bee3e-122">Deinstallieren Sie **MBAM** vom Server mithilfe des **MBAM** -Installationsprogramms.</span><span class="sxs-lookup"><span data-stu-id="bee3e-122">Uninstall **MBAM** from the server by using the **MBAM** installer.</span></span>

3.  <span data-ttu-id="bee3e-123">Löschen Sie die folgenden Objekte manuell aus Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="bee3e-123">Manually delete the following objects from Configuration Manager:</span></span>

    -   <span data-ttu-id="bee3e-124">MBAM-unterstützte Computersammlung</span><span class="sxs-lookup"><span data-stu-id="bee3e-124">MBAM Supported Computers collection</span></span>

    -   <span data-ttu-id="bee3e-125">BitLocker-Schutz Basislinie</span><span class="sxs-lookup"><span data-stu-id="bee3e-125">BitLocker Protection baseline</span></span>

    -   <span data-ttu-id="bee3e-126">BitLocker-Betriebs System-Laufwerkschutz-Konfigurationselement</span><span class="sxs-lookup"><span data-stu-id="bee3e-126">BitLocker Operating System Drive Protection configuration item</span></span>

    -   <span data-ttu-id="bee3e-127">BitLocker-Konfigurationselement "Fixed Data Drives Protection"</span><span class="sxs-lookup"><span data-stu-id="bee3e-127">BitLocker Fixed Data Drives Protection configuration item</span></span>

4.  <span data-ttu-id="bee3e-128">Löschen Sie den Ordner MBAM Reports auf der Configuration Manager-SQL Server Reporting Services-Website manuell.</span><span class="sxs-lookup"><span data-stu-id="bee3e-128">Manually delete the MBAM Reports folder in the Configuration Manager SQL Server Reporting Services site.</span></span> <span data-ttu-id="bee3e-129">Gehen Sie dazu folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="bee3e-129">To do this:</span></span>

    1.  <span data-ttu-id="bee3e-130">Verwenden Sie Internet Explorer, um zum Reporting Services-Punkt zu navigieren, beispielsweise http:// &lt; yourcmserver &gt; /Reports.</span><span class="sxs-lookup"><span data-stu-id="bee3e-130">Use Internet Explorer to browse to the reporting services point, for example, http://&lt;yourcmserver&gt;/reports.</span></span>

    2.  <span data-ttu-id="bee3e-131">Klicken Sie auf den entsprechenden Link für Configuration Manager-Standortcode.</span><span class="sxs-lookup"><span data-stu-id="bee3e-131">Click the appropriate Configuration Manager site code link.</span></span>

    3.  <span data-ttu-id="bee3e-132">Löschen Sie den Ordner MBAM.</span><span class="sxs-lookup"><span data-stu-id="bee3e-132">Delete the MBAM folder.</span></span>

5.  <span data-ttu-id="bee3e-133">Verwenden Sie das MBAM-Server Installationsprogramm, um die Configuration Manager-Integrationsobjekte erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="bee3e-133">Use the MBAM Server installer to reinstall the Configuration Manager Integration objects.</span></span> <span data-ttu-id="bee3e-134">Auf den Clientcomputern werden die BitLocker-Kompatibilitätsdaten mit der Zeit erneut hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="bee3e-134">The client computers will begin to upload BitLocker compliance data again over time.</span></span>

### <span data-ttu-id="bee3e-135">Schaltfläche "Senden" im Self-Service-Portal funktioniert nicht in Internet Explorer10</span><span class="sxs-lookup"><span data-stu-id="bee3e-135">Submit button on Self-Service Portal does not work in Internet Explorer10</span></span>

<span data-ttu-id="bee3e-136">Wenn Sie die Internet-Explorer10 für den Zugriff auf die Website "Verwaltung und Überwachung" verwenden, funktioniert die Schaltfläche " **senden** " auf der Website nicht.</span><span class="sxs-lookup"><span data-stu-id="bee3e-136">When you use Internet Explorer10 to access the Administration and Monitoring Website, the **Submit** button on the website does not work.</span></span>

<span data-ttu-id="bee3e-137">**Problemumgehung**: Installieren Sie auf dem Server, auf dem Sie die Verwaltungs-und Überwachungs Website installiert haben, [Hotfix für ASP.net-Browserdefinitionsdateien](https://go.microsoft.com/fwlink/?LinkId=317798).</span><span class="sxs-lookup"><span data-stu-id="bee3e-137">**Workaround**: On the server where you installed the Administration and Monitoring Website, install [Hotfix for ASP.NET browser definition files](https://go.microsoft.com/fwlink/?LinkId=317798).</span></span>

### <span data-ttu-id="bee3e-138">Internationale Domänennamen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bee3e-138">International domain names are not supported</span></span>

<span data-ttu-id="bee3e-139">MBAM 2,0 SP1 unterstützt keine internationalen Domänennamen.</span><span class="sxs-lookup"><span data-stu-id="bee3e-139">MBAM 2.0 SP1 does not support international domain names.</span></span>

<span data-ttu-id="bee3e-140">**Problemumgehung**: keine.</span><span class="sxs-lookup"><span data-stu-id="bee3e-140">**Workaround**: None.</span></span>

### <span data-ttu-id="bee3e-141">Berichte auf der Website "Verwaltung und Überwachung" zeigen eine Warnung an, wenn SSL in SSRS nicht konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="bee3e-141">Reports in the Administration and Monitoring website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="bee3e-142">Wenn SQLServer Reporting Services (SSRS) nicht für die Verwendung von Secure Socket Layer (SSL) konfiguriert wurde, wird die URL für die Berichte bei der Installation des MBAM-Servers auf http statt auf HTTPS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bee3e-142">If SQLServer Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="bee3e-143">Wenn Sie dann zur Websiteverwaltung und Überwachung navigieren und einen Bericht auswählen, wird die folgende Meldung angezeigt: "nur sicherer Inhalt wird angezeigt."</span><span class="sxs-lookup"><span data-stu-id="bee3e-143">If you then browse to the Administration and Monitoring website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="bee3e-144">**Problemumgehung**: um dieses Problem zu beheben, konfigurieren Sie SSL im **Reporting Services-Konfigurations-Manager** auf dem MBAM-Server, auf dem SQLServer Reporting Services installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bee3e-144">**Workaround**: To correct this issue, configure SSL in **Reporting Services Configuration Manager** on the MBAM server where SQLServer Reporting Services is installed.</span></span> <span data-ttu-id="bee3e-145">Deinstallieren Sie die Verwaltungs-und Monitoring Server-Website, und installieren Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="bee3e-145">Uninstall and then reinstall the Administration and Monitoring Server website.</span></span>

### <span data-ttu-id="bee3e-146">Wenn Sie im Kompatibilitäts Zusammenfassungsbericht auf Zurück klicken, wird möglicherweise ein Fehler erstellt</span><span class="sxs-lookup"><span data-stu-id="bee3e-146">Clicking Back in the Compliance Summary report might create an error</span></span>

<span data-ttu-id="bee3e-147">Wenn Sie einen Drilldown in einen Kompatibilitäts Zusammenfassungsbericht ausführen und dann im SSRS-Bericht auf den Link **zurück** klicken, kann ein Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="bee3e-147">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might occur.</span></span>

<span data-ttu-id="bee3e-148">**Problemumgehung**: keine.</span><span class="sxs-lookup"><span data-stu-id="bee3e-148">**Workaround**: None.</span></span>

### <span data-ttu-id="bee3e-149">Verwendeter Speicherplatz nur die Verschlüsselung funktioniert nicht ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="bee3e-149">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="bee3e-150">Wenn Sie einen Computer nach der Installation des MBAM-Clients zum ersten Mal verschlüsseln und ein Gruppenrichtlinienobjekt für die Implementierung der nur verwendeter Speicherplatz Verschlüsselung festgesetzt haben, verschlüsselt MBAM fälschlicherweise den gesamten Datenträger, anstatt nur den verwendeten Speicherplatz der Festplatte zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="bee3e-150">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only Encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="bee3e-151">Wenn ein Computer bereits mit verwendeter Speicherplatz Verschlüsselung verschlüsselt ist, bevor Sie den MBAM-Client installieren, und Sie das Gruppenrichtlinienobjekt "nur verwendeter Speicherplatz Verschlüsselung" festgelegt haben, erkennt MBAM die Einstellung und meldet die Verschlüsselung in den Konformitätsberichten ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="bee3e-151">If a computer is already encrypted with Used Space Only Encryption before you install the MBAM Client, and you have set the same Used Space Only Encryption Group Policy Object, MBAM recognizes the setting and reports the encryption correctly in the compliance reports.</span></span>

<span data-ttu-id="bee3e-152">**Problemumgehung**: keine.</span><span class="sxs-lookup"><span data-stu-id="bee3e-152">**Workaround**: None.</span></span>

### <span data-ttu-id="bee3e-153">Die Verschlüsselungsstärke wird im Computer Kompatibilitätsbericht falsch angezeigt</span><span class="sxs-lookup"><span data-stu-id="bee3e-153">Cipher strength displays incorrectly in the Computer Compliance report</span></span>

<span data-ttu-id="bee3e-154">Wenn Sie keine bestimmte Verschlüsselungsstärke in den Gruppenrichtlinienobjekten **"Laufwerksverschlüsselung auswählen" und "Verschlüsselungsstärke"** festlegen, wird der Computer Kompatibilitätsbericht in der integrierten Configuration Manager-Topologie immer für die Verschlüsselungsstärke **unbekannt** angezeigt, selbst wenn die Verschlüsselungsstärke den Standardwert der 128-Bit-Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bee3e-154">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager integrated topology always displays **Unknown** for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="bee3e-155">Der Bericht zeigt die richtige Verschlüsselungsstärke an, wenn Sie eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="bee3e-155">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="bee3e-156">**Problemumgehung**: Legen Sie immer eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt **Auswählen von Laufwerk Verschlüsselungsmethode und Verschlüsselungsstärke** fest.</span><span class="sxs-lookup"><span data-stu-id="bee3e-156">**Workaround**: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="bee3e-157">Kompatibilitäts Status Verteilung nach Laufwerks zeigt alte Daten an, nachdem Sie Konfigurationselemente aktualisiert haben</span><span class="sxs-lookup"><span data-stu-id="bee3e-157">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="bee3e-158">Nachdem Sie MBAM-Konfigurationselemente in SystemCenter2012 ConfigurationManager aktualisiert haben, werden auf dem BitLocker Enterprise Compliance-Dashboard Daten angezeigt, die auf Informationen aus älteren Versionen der Konfigurationselemente basieren.</span><span class="sxs-lookup"><span data-stu-id="bee3e-158">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="bee3e-159">**Problemumgehung**: keine.</span><span class="sxs-lookup"><span data-stu-id="bee3e-159">**Workaround**: None.</span></span> <span data-ttu-id="bee3e-160">Änderungen der MBAM-Konfigurationselemente werden nicht unterstützt, und der Bericht wird möglicherweise nicht wie erwartet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bee3e-160">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="bee3e-161">Verbesserte Sicherheitskonfiguration kann dazu führen, dass Berichte falsch angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="bee3e-161">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="bee3e-162">Wenn Internet Explorer Enhanced Security Configuration (ESC) aktiviert ist, wird möglicherweise eine Meldung für den **Zugriff verweigert** angezeigt, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bee3e-162">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an **Access Denied** message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="bee3e-163">Standardmäßig ist die erweiterte Sicherheitskonfiguration aktiviert, um den Server zu schützen, indem die Anfälligkeit des Servers für potenzielle Angriffe verringert wird, die über Webinhalte und Anwendungsskripts auftreten können.</span><span class="sxs-lookup"><span data-stu-id="bee3e-163">By default, Enhanced Security Configuration is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="bee3e-164">**Problemumgehung**: Wenn die Meldung " **Zugriff verweigert** " angezeigt wird, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen, können Sie ein Gruppenrichtlinienobjekt festlegen oder den Standardwert manuell in Ihrem Bild ändern, um die erweiterte Sicherheitskonfiguration zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bee3e-164">**Workaround**: If the **Access Denied** message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="bee3e-165">Sie können auch die Berichte auf einem anderen Computer anzeigen, auf dem die erweiterte Sicherheitskonfiguration nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bee3e-165">You can also alternatively view the reports from another computer on which Enhanced Security Configuration is not enabled.</span></span>

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> <span data-ttu-id="bee3e-166">MBAM Server-Installation schlägt fehl, wenn Sie von SQLServer2008 auf SQLServer2012 aktualisieren</span><span class="sxs-lookup"><span data-stu-id="bee3e-166">MBAM Server installation fails when you upgrade from SQLServer2008 to SQLServer2012</span></span>

<span data-ttu-id="bee3e-167">Wenn Sie ein Upgrade von SQLServer2008 auf SQLServer2012 durchführen und dann versuchen, die Konformitäts-und Überwachungsdatenbank oder die Wiederherstellungsdatenbank zu installieren, schlägt die Installation fehl, und es wird ein Rollback ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bee3e-167">If you upgrade from SQLServer2008 to SQLServer2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="bee3e-168">Der Fehler tritt auf, weil die erforderliche SQLCMD.exe Datei während des SQLServer-Upgrades entfernt wurde und vom MBAM-Installationsprogramm nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="bee3e-168">The failure occurs because the required SQLCMD.exe file was removed during the SQLServer upgrade, and it cannot be found by the MBAM installer.</span></span> <span data-ttu-id="bee3e-169">Die MSI-Protokolldateizeilen können wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="bee3e-169">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="bee3e-170">RunDbInstallScript Recovery DB ca: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery DB ca: dbinstance-xxxxxx\\I01RunDbInstallScript Recovery DB ca: SqlScript-c:\\Programme Files\\Microsoft\\Microsoft BitLocker-Verwaltung und Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB ca: dbname-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript Recovery DB ca: DefaultFileName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript Recovery DB ca: defaultDataPath-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript Recovery DB ca: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript Recovery DB ca: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-e-S xxxxxxx\\I01-i "c:\\Programme Files\\Microsoft\\Microsoft BitLocker-Verwaltung und Monitoring\\Setup\\KeyRecovery.SQL"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery DB ca: Starten der Ausführung der Wiederherstellungs-Datenbank installieren scriptRunDbInstallScript Recovery DB ca: die sqlcmd-Protokolldatei befindet sich in der C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript-Wiederherstellungs-DB-ca-Ausnahme: benutzerdefinierte Aktion der Wiederherstellungsdatenbank-Befehlszeile-Ausgabe Ausnahme: das System kann die angegebene Datei nicht finden</span><span class="sxs-lookup"><span data-stu-id="bee3e-170">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="bee3e-171">Der MBAM-Server-Windows-Installer ist hart codiert, um den SQLCMD.exe Pfad zu finden, indem Sie den Pfadzeichen folgen Wert in der Registrierung unter HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="bee3e-171">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="bee3e-172">Während der Migration von SQLServer2008 zu SQLServer2012 ist der Schlüssel weiterhin vorhanden, doch der Pfad, auf den der Datenwert verweist, enthält nicht die SQLCMD.exe-Datei, da die Datei vom sqlupgradeprozess entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="bee3e-172">The key is still present during the migration from SQLServer2008 to SQLServer2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQLupgrade process removed the file.</span></span>

<span data-ttu-id="bee3e-173">**Problemumgehung**: benennen Sie den HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup Path-Zeichenfolgenwert vorübergehend in **path \ _old**um, und führen Sie dann Windows Installer auf dem MBAM-Server erneut aus.</span><span class="sxs-lookup"><span data-stu-id="bee3e-173">**Workaround**: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup path string value to **Path\_old**, and then run Windows Installer on the MBAM Server again.</span></span> <span data-ttu-id="bee3e-174">Wenn die Installation erfolgreich abgeschlossen wurde und die Datenbanken in SQLServer2012 erstellt werden, benennen Sie den **Pfad \ _old** in **path**um.</span><span class="sxs-lookup"><span data-stu-id="bee3e-174">When the installation completes successfully and creates the databases in SQLServer2012, rename **Path\_old** to **Path**.</span></span>

## <span data-ttu-id="bee3e-175">Hotfixes und Knowledge Base-Artikel für MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="bee3e-175">Hotfixes and Knowledge Base articles for MBAM 2.0 SP1</span></span>


<span data-ttu-id="bee3e-176">Dieser Abschnitt enthält Hotfixes und KB-Artikel für MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="bee3e-176">This section contains hotfixes and KB articles for MBAM 2.0 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="bee3e-177">KB-Artikel</span><span class="sxs-lookup"><span data-stu-id="bee3e-177">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="bee3e-178">Title</span><span class="sxs-lookup"><span data-stu-id="bee3e-178">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="bee3e-179">Link</span><span class="sxs-lookup"><span data-stu-id="bee3e-179">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee3e-180">2831166</span><span class="sxs-lookup"><span data-stu-id="bee3e-180">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-181">Das Installieren der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 schlägt fehl, wenn &quot; System Center cm-Objekte bereits installiert sind&quot;</span><span class="sxs-lookup"><span data-stu-id="bee3e-181">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="bee3e-182">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-182">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee3e-183">2870849</span><span class="sxs-lookup"><span data-stu-id="bee3e-183">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-184">Benutzer können den BitLocker-Wiederherstellungsschlüssel nicht über das Self-Service-Portal von mbam 2.0 abrufen</span><span class="sxs-lookup"><span data-stu-id="bee3e-184">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="bee3e-185">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-185">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee3e-186">2756402</span><span class="sxs-lookup"><span data-stu-id="bee3e-186">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-187">MBAM-Client schlägt mit Ereignis-ID 4 und Fehlercode 0x8004100E in der Ereignisbeschreibung fehl</span><span class="sxs-lookup"><span data-stu-id="bee3e-187">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="bee3e-188">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-188">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee3e-189">2620287</span><span class="sxs-lookup"><span data-stu-id="bee3e-189">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-190">Fehlermeldung "Server Fehler in der Anwendung"/Reports ", wenn Sie in MBAM auf die Registerkarte" Berichte "klicken</span><span class="sxs-lookup"><span data-stu-id="bee3e-190">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="bee3e-191">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-191">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee3e-192">2639518</span><span class="sxs-lookup"><span data-stu-id="bee3e-192">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-193">Fehler beim Öffnen von Enterprise-oder Computer Kompatibilitätsberichten in MBAM</span><span class="sxs-lookup"><span data-stu-id="bee3e-193">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="bee3e-194">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-194">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee3e-195">2620269</span><span class="sxs-lookup"><span data-stu-id="bee3e-195">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-196">MBAM Enterprise-Berichte werden nicht aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bee3e-196">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="bee3e-197">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-197">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee3e-198">2712461</span><span class="sxs-lookup"><span data-stu-id="bee3e-198">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-199">Die Installation von MBAM auf einem Domänen Controller wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bee3e-199">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="bee3e-200">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-200">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee3e-201">2876732</span><span class="sxs-lookup"><span data-stu-id="bee3e-201">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-202">Sie erhalten Fehlercode 0x80071a90 während des Standalone-oder Configuration Manager-Integrations Setups von mbam 2.0</span><span class="sxs-lookup"><span data-stu-id="bee3e-202">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="bee3e-203">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-203">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee3e-204">2754259</span><span class="sxs-lookup"><span data-stu-id="bee3e-204">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-205">MBAM und sichere Netzwerkkommunikation</span><span class="sxs-lookup"><span data-stu-id="bee3e-205">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="bee3e-206">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-206">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee3e-207">2870842</span><span class="sxs-lookup"><span data-stu-id="bee3e-207">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-208">Mbam 2.0-Setup schlägt während des Configuration Manager-Integrationsszenarios mit SQL Server 2008 fehl</span><span class="sxs-lookup"><span data-stu-id="bee3e-208">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="bee3e-209">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-209">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee3e-210">2668533</span><span class="sxs-lookup"><span data-stu-id="bee3e-210">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-211">MBAM-Setup schlägt fehl, wenn SQL SSRS nicht ordnungsgemäß konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="bee3e-211">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="bee3e-212">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-212">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee3e-213">2870847</span><span class="sxs-lookup"><span data-stu-id="bee3e-213">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-214">MBAM 2,0-Setup schlägt fehl, wenn &quot; Fehler beim Abrufen der Configuration Manager-Server Rolleneinstellungen für &#39;Reporting Services-Point&#39; Rolle auftreten&quot;</span><span class="sxs-lookup"><span data-stu-id="bee3e-214">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="bee3e-215">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-215">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee3e-216">2870839</span><span class="sxs-lookup"><span data-stu-id="bee3e-216">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-217">Mbam 2.0-Enterprise-Berichte werden in der eigenständigen mbam 2.0-Topologie aufgrund des SQL-Auftrags createcache-Fehlers nicht aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bee3e-217">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="bee3e-218">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-218">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee3e-219">2620269</span><span class="sxs-lookup"><span data-stu-id="bee3e-219">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-220">MBAM Enterprise-Berichte werden nicht aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bee3e-220">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="bee3e-221">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-221">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee3e-222">2935997</span><span class="sxs-lookup"><span data-stu-id="bee3e-222">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-223">Kompatibilitätsberichte von MBAM-unterstützten Computern enthalten fehlerhafte nicht unterstützte Produkte</span><span class="sxs-lookup"><span data-stu-id="bee3e-223">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="bee3e-224">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-224">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee3e-225">2612822</span><span class="sxs-lookup"><span data-stu-id="bee3e-225">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee3e-226">Der Computer Eintrag wird in MBAM abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="bee3e-226">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="bee3e-227">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="bee3e-227">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="bee3e-228">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="bee3e-228">Related topics</span></span>


[<span data-ttu-id="bee3e-229">Infos zu MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="bee3e-229">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)

 

 





