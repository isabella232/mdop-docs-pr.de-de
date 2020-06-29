---
title: So verschieben Sie die MBAM 2.5-Datenbanken
description: So verschieben Sie die MBAM 2.5-Datenbanken
author: dansimp
ms.assetid: 34b46f2d-0add-4377-8e4e-04b628fdfcf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 63c509e7ae1460ece815ef6c0a22350f76b52018
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804199"
---
# <span data-ttu-id="20a31-103">So verschieben Sie die MBAM 2.5-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="20a31-103">How to Move the MBAM 2.5 Databases</span></span>

<span data-ttu-id="20a31-104">Gehen Sie wie folgt vor, um die folgenden Datenbanken von einem Computer auf einen anderen zu verschieben. von Server A nach Server B, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="20a31-104">Use these procedures to move the following databases from one computer to another; from Server A to Server B, for example:</span></span>

-   <span data-ttu-id="20a31-105">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="20a31-105">Compliance and Audit Database</span></span>

-   <span data-ttu-id="20a31-106">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="20a31-106">Recovery Database</span></span>

>[!NOTE]
><span data-ttu-id="20a31-107">Es ist wichtig, dass die Datenbanken auf Computer B wiederhergestellt werden, bevor Sie den MBAM-Konfigurations-Assistenten ausführen, um Sie zu aktualisieren/zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="20a31-107">It is important that the databases be restored to Machine B PRIOR to running the MBAM Configuration Wizard to update/configure them.</span></span>

<span data-ttu-id="20a31-108">Wenn die Datenbanken nicht vorhanden sind, erstellt der Konfigurations-Assistent neue, leere Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="20a31-108">If the databases are NOT present, the Configuration Wizard creates NEW, empty, databases.</span></span> <span data-ttu-id="20a31-109">Wenn Ihre vorhandenen Datenbanken wiederhergestellt werden, wird durch diesen Vorgang die MBAM-Konfiguration unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="20a31-109">When your existing databases are then restored, this process will break the MBAM configuration.</span></span>

<span data-ttu-id="20a31-110">Stellen Sie zuerst die Datenbanken wieder her, und führen Sie dann den MBAM-Konfigurations-Assistenten aus, wählen Sie die Option Datenbank aus, und der Konfigurations-Assistent wird mit den wiederhergestellten Datenbanken verbunden. Sie können Sie bei Bedarf im Rahmen des Prozesses aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="20a31-110">Restore the databases FIRST, then run the MBAM Configuration Wizard, choose the database option, and the Configuration Wizard will “connect” to the databases you restored; upgrading them if needed as part of the process.</span></span>

**<span data-ttu-id="20a31-111">Wenn Sie mehrere Features verschieben, verschieben Sie Sie in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="20a31-111">If you are moving multiple features, move them in the following order:</span></span>**

1.  <span data-ttu-id="20a31-112">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="20a31-112">Recovery Database</span></span>

2.  <span data-ttu-id="20a31-113">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="20a31-113">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="20a31-114">Berichte</span><span class="sxs-lookup"><span data-stu-id="20a31-114">Reports</span></span>

4.  <span data-ttu-id="20a31-115">Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="20a31-115">Administration and Monitoring Website</span></span>

5.  <span data-ttu-id="20a31-116">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="20a31-116">Self-Service Portal</span></span>

>[!Note]
><span data-ttu-id="20a31-117">Wenn Sie die in diesem Thema bereitgestellten Beispiel-Windows PowerShell-Skripts ausführen möchten, müssen Sie die Windows PowerShell-Ausführungsrichtlinie aktualisieren, damit Skripts ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="20a31-117">To run the example Windows PowerShell scripts provided in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="20a31-118">Anweisungen finden Sie unter [Ausführen von Windows PowerShell-Skripts](https://technet.microsoft.com/library/ee176949.aspx) .</span><span class="sxs-lookup"><span data-stu-id="20a31-118">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

## <span data-ttu-id="20a31-119">Verschieben der Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="20a31-119">Move the Recovery Database</span></span>

<span data-ttu-id="20a31-120">Die allgemeinen Schritte zum Verschieben der Wiederherstellungsdatenbank lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="20a31-120">The high-level steps for moving the Recovery Database are:</span></span>

1.  <span data-ttu-id="20a31-121">Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="20a31-121">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="20a31-122">Sichern der Wiederherstellungsdatenbank auf Server A</span><span class="sxs-lookup"><span data-stu-id="20a31-122">Back up the Recovery Database on Server A</span></span>

3.  <span data-ttu-id="20a31-123">Verschieben der Wiederherstellungsdatenbank von Server a auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-123">Move the Recovery Database from Server A to Server B</span></span>

4.  <span data-ttu-id="20a31-124">Wiederherstellen der Wiederherstellungsdatenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-124">Restore the Recovery Database on Server B</span></span>

5.  <span data-ttu-id="20a31-125">Konfigurieren des Zugriffs auf die Datenbank auf Server B und Aktualisieren von Verbindungsdaten</span><span class="sxs-lookup"><span data-stu-id="20a31-125">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="20a31-126">Installieren der MBAM-Server Software und Ausführen des MBAM-Serverkonfigurations-Assistenten auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-126">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="20a31-127">Fortsetzen der Instanz der Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="20a31-127">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="20a31-128">Verschieben der Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="20a31-128">How to move the Recovery Database</span></span>

**<span data-ttu-id="20a31-129">Beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="20a31-129">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>** <span data-ttu-id="20a31-130">Verwenden Sie auf jedem Server, auf dem die MBAM-Verwaltungs-und Monitoring Server-Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu beenden.</span><span class="sxs-lookup"><span data-stu-id="20a31-130">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="20a31-131">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="20a31-131">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="20a31-132">Zum Ausführen dieses Befehls müssen Sie das IIS-Modul (Internet Information Services) für Windows PowerShell der aktuellen Instanz von Windows PowerShell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="20a31-132">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="20a31-133">Sichern der Wiederherstellungsdatenbank auf Server A</span><span class="sxs-lookup"><span data-stu-id="20a31-133">Back up the Recovery Database on Server A</span></span>

1.  <span data-ttu-id="20a31-134">Verwenden Sie die **Sicherungs** Aufgabe in SQL Server Management Studio, um die Wiederherstellungsdatenbank auf Server A zu sichern.  Standardmäßig lautet der Datenbankname **MBAM-Wiederherstellungsdatenbank**.</span><span class="sxs-lookup"><span data-stu-id="20a31-134">Use the **Back Up** task in SQL Server Management Studio to back up the Recovery Database on Server A.  By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="20a31-135">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält, und ändern Sie die MBAM-Wiederherstellungsdatenbank, um den vollständigen Wiederherstellungsmodus zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="20a31-135">To automate this procedure, create a SQL file (.sql) that contains the following SQL script, and change the MBAM Recovery Database to use the full recovery mode:</span></span>

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Recovery Database Data and MBAM Recovery logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery Database Data.bak';

    GO

    -- Back up the full MBAM Recovery Database.

    BACKUP DATABASE [MBAM Recovery and Hardware] TO [MBAM Recovery and Hardware Database Data Device];

    GO

    BACKUP CERTIFICATE [MBAM Recovery Encryption Certificate]

    TO FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    ENCRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

3.  <span data-ttu-id="20a31-136">Verwenden Sie den folgenden Wert, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="20a31-136">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="20a31-137">**$Password $** -Kennwort, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="20a31-137">**$PASSWORD$** - password that you use to encrypt the Private Key file.</span></span>

4.  <span data-ttu-id="20a31-138">Führen Sie in Windows PowerShell das Skript aus, das in der Datei gespeichert ist, und ähnlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="20a31-138">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  <span data-ttu-id="20a31-139">Verwenden Sie den folgenden Wert, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="20a31-139">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="20a31-140">**$Servername $ \ $SqlInstanceName $** -Servername und Instanz, aus der die Wiederherstellungsdatenbank gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="20a31-140">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Recovery Database will be backed up.</span></span>

### <span data-ttu-id="20a31-141">Verschieben der Wiederherstellungsdatenbank von Server a auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-141">Move the Recovery Database from Server A to Server B</span></span>

<span data-ttu-id="20a31-142">Verwenden Sie den Windows-Explorer, um die Datei **MBAM Recovery Database Data. bak** von Server a auf Server B zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="20a31-142">Use Windows Explorer to move the **MBAM Recovery Database Data.bak** file from Server A to Server B.</span></span>

<span data-ttu-id="20a31-143">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl auszuführen, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="20a31-143">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
<span data-ttu-id="20a31-144">Verwenden Sie die Informationen in der folgenden Tabelle, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="20a31-144">Use the information in the following table to replace the values in the code example with values that match your environment.</span></span>

| **<span data-ttu-id="20a31-145">Parameter</span><span class="sxs-lookup"><span data-stu-id="20a31-145">Parameter</span></span>**        | **<span data-ttu-id="20a31-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20a31-146">Description</span></span>**  |
|----------------------|------------------|
| <span data-ttu-id="20a31-147">$Servername $</span><span class="sxs-lookup"><span data-stu-id="20a31-147">$SERVERNAME$</span></span>       | <span data-ttu-id="20a31-148">Der Name des Servers, auf den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20a31-148">Name of the server to which the files will be copied.</span></span> |
| <span data-ttu-id="20a31-149">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="20a31-149">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="20a31-150">Name der Freigabe und des Pfads, in den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20a31-150">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="20a31-151">Wiederherstellen der Wiederherstellungsdatenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-151">Restore the Recovery Database on Server B</span></span>

1.  <span data-ttu-id="20a31-152">Stellen Sie die Wiederherstellungsdatenbank auf Server B mithilfe der Aufgabe **Datenbank wiederherstellen** in SQL Server Management Studio wieder her.</span><span class="sxs-lookup"><span data-stu-id="20a31-152">Restore the Recovery Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="20a31-153">Wenn die vorherige Aufgabe abgeschlossen ist, wählen Sie **vom Gerät aus**, und wählen Sie dann die Datenbanksicherungsdatei aus.</span><span class="sxs-lookup"><span data-stu-id="20a31-153">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="20a31-154">Verwenden Sie den Befehl **Hinzufügen** , um die Datei **MBAM Recovery Database Data. bak** auszuwählen, und klicken Sie auf **OK** , um den Wiederherstellungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="20a31-154">Use the **Add** command to select the **MBAM Recovery Database Data.bak** file, and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="20a31-155">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="20a31-155">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Restore MBAM Recovery Database.

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO

    -- Restore the MBAM Recovery Database data and log files.

    RESTORE DATABASE [MBAM Recovery and Hardware]

    FROM DISK = 'Z:\MBAM Recovery Database Data.bak'

    WITH REPLACE
    ```

5.  <span data-ttu-id="20a31-156">Verwenden Sie den folgenden Wert, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="20a31-156">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="20a31-157">**$Password $** -Kennwort, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="20a31-157">**$PASSWORD$** - password that you used to encrypt the Private Key file.</span></span>

6.  <span data-ttu-id="20a31-158">Führen Sie in Windows PowerShell das Skript aus, das in der Datei gespeichert ist, und ähnlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="20a31-158">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  <span data-ttu-id="20a31-159">Verwenden Sie den folgenden Wert, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="20a31-159">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="20a31-160">**$Servername $ \ $SqlInstanceName $** -Server Name und Instanz, in die die Wiederherstellungsdatenbank wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="20a31-160">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Recovery Database will be restored.</span></span>

### <span data-ttu-id="20a31-161">Konfigurieren des Zugriffs auf die Datenbank auf Server B und Aktualisieren von Verbindungsdaten</span><span class="sxs-lookup"><span data-stu-id="20a31-161">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="20a31-162">Überprüfen Sie, ob die Microsoft SQL Server-Benutzeranmeldung, die den Zugriff auf die Wiederherstellung der Datenbank in der wiederhergestellten Datenbank ermöglicht, dem Zugriffskonto zugeordnet ist, das Sie während des Konfigurationsprozesses angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="20a31-162">Verify that the Microsoft SQL Server user login that enables Recovery Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="20a31-163">Wenn die Anmeldung nicht identisch ist, erstellen Sie eine Anmeldung mithilfe von SQL Server Management Studio, und ordnen Sie Sie dem vorhandenen Datenbankbenutzer zu.</span><span class="sxs-lookup"><span data-stu-id="20a31-163">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="20a31-164">Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die MBAM-Websites zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="20a31-164">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the MBAM websites.</span></span>

3. <span data-ttu-id="20a31-165">Bearbeiten Sie den folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="20a31-165">Edit the following registry key:</span></span>

   **<span data-ttu-id="20a31-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="20a31-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span></span>**

4. <span data-ttu-id="20a31-167">Aktualisieren Sie den Wert der **Datenquelle** mit dem Namen des Servers und der Instanz (beispielsweise \ $Servername \ $ \ \ \ $SqlInstanceName), in die die Wiederherstellungsdatenbank verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="20a31-167">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="20a31-168">Aktualisieren Sie den **ursprünglichen Katalog** Wert mit dem wiederhergestellten Datenbanknamen.</span><span class="sxs-lookup"><span data-stu-id="20a31-168">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="20a31-169">Um diesen Vorgang zu automatisieren, können Sie die Windows PowerShell-Eingabeaufforderung verwenden, um eine Befehlszeile auf dem Verwaltungs-und Überwachungs Server einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="20a31-169">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\\Microsoft\MBAM Server\\Web" /v
   RecoveryDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f

   Set-WebConfigurationProperty
   'connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath
   "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data
   Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and
   Hardware;Integrated Security=SSPI;"

   Set-WebConfigurationProperty
   'connectionStrings/add[\@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]'
   -PSPath "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value
   "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery
   and Hardware;Integrated Security=SSPI;"
   ```

   >[!Note]
   ><span data-ttu-id="20a31-170">Diese Verbindungszeichenfolge wird von allen lokalen MBAM-Webanwendungen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="20a31-170">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="20a31-171">Daher muss Sie nur einmal pro Server aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="20a31-171">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="20a31-172">Verwenden Sie die folgende Tabelle, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="20a31-172">Use the following table to replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="20a31-173">Parameter</span><span class="sxs-lookup"><span data-stu-id="20a31-173">Parameter</span></span>|<span data-ttu-id="20a31-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20a31-174">Description</span></span>|
   |---------|-----------|
   |<span data-ttu-id="20a31-175">$Servername $/\ $SqlInstanceName $</span><span class="sxs-lookup"><span data-stu-id="20a31-175">$SERVERNAME$/\$SQLINSTANCENAME$</span></span>|<span data-ttu-id="20a31-176">Servername und Instanz von SQL Server, auf der sich die Wiederherstellungsdatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="20a31-176">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="20a31-177">$Database $</span><span class="sxs-lookup"><span data-stu-id="20a31-177">$DATABASE$</span></span>|<span data-ttu-id="20a31-178">Der Name der Wiederherstellungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="20a31-178">Name of the Recovery database.</span></span>|


### <span data-ttu-id="20a31-179">Installieren der MBAM-Server Software und Ausführen des MBAM-Serverkonfigurations-Assistenten auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-179">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="20a31-180">Installieren Sie die MBAM 2,5-Server Software auf Server B. Ausführliche Informationen finden Sie unter [Installieren der MBAM 2,5-Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="20a31-180">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="20a31-181">Starten Sie auf Server B den MBAM-Serverkonfigurations-Assistenten, klicken Sie auf **neue Features hinzufügen**, und wählen Sie dann nur das Feature **Wiederherstellungsdatenbank** aus.</span><span class="sxs-lookup"><span data-stu-id="20a31-181">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Recovery Database** feature.</span></span> <span data-ttu-id="20a31-182">Ausführliche Informationen zum Konfigurieren der Datenbanken finden Sie unter [Konfigurieren der MBAM 2,5-Datenbanken](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="20a31-182">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="20a31-183">Alternativ können Sie das Windows PowerShell **-Cmdlet Enable-MbamDatabase** verwenden, um die Wiederherstellungsdatenbank zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="20a31-183">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Recovery Database.</span></span>


### <span data-ttu-id="20a31-184">Fortsetzen der Instanz der Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="20a31-184">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="20a31-185">Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu starten.</span><span class="sxs-lookup"><span data-stu-id="20a31-185">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="20a31-186">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl auszuführen, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="20a31-186">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="20a31-187">Zum Ausführen dieses Befehls müssen Sie das IIS-Modul für Windows PowerShell der aktuellen Instanz von Windows PowerShell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="20a31-187">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

## <span data-ttu-id="20a31-188">Verschieben der Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="20a31-188">Move the Compliance and Audit Database</span></span>

<span data-ttu-id="20a31-189">Die allgemeinen Schritte zum Verschieben der Kompatibilitäts-und Überwachungsdatenbank lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="20a31-189">The high-level steps for moving the Compliance and Audit Database are:</span></span>

1.  <span data-ttu-id="20a31-190">Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="20a31-190">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="20a31-191">Sichern der Konformitäts-und Überwachungsdatenbank auf Server A</span><span class="sxs-lookup"><span data-stu-id="20a31-191">Back up the Compliance and Audit Database on Server A</span></span>

3.  <span data-ttu-id="20a31-192">Verschieben der Konformitäts-und Überwachungsdatenbank von Server a auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-192">Move the Compliance and Audit Database from Server A to Server B</span></span>

4.  <span data-ttu-id="20a31-193">Wiederherstellen der Konformitäts-und Überwachungsdatenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-193">Restore the Compliance and Audit Database on Server B</span></span>

5.  <span data-ttu-id="20a31-194">Konfigurieren des Zugriffs auf die Datenbank auf Server B und Aktualisieren von Verbindungsdaten</span><span class="sxs-lookup"><span data-stu-id="20a31-194">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="20a31-195">Installieren der MBAM-Server Software und Ausführen des MBAM-Serverkonfigurations-Assistenten auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-195">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="20a31-196">Fortsetzen der Instanz der Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="20a31-196">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="20a31-197">Verschieben der Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="20a31-197">How to move the Compliance and Audit Database</span></span>

**<span data-ttu-id="20a31-198">Beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="20a31-198">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>**  <span data-ttu-id="20a31-199">Verwenden Sie auf jedem Server, auf dem die MBAM-Verwaltungs-und Monitoring Server-Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu beenden.</span><span class="sxs-lookup"><span data-stu-id="20a31-199">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="20a31-200">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="20a31-200">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="20a31-201">Zum Ausführen dieses Befehls müssen Sie das IIS-Modul (Internet Information Services) für Windows PowerShell der aktuellen Instanz von Windows PowerShell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="20a31-201">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="20a31-202">Sichern der Konformitäts-und Überwachungsdatenbank auf Server A</span><span class="sxs-lookup"><span data-stu-id="20a31-202">Back up the Compliance and Audit Database on Server A</span></span>

1.  <span data-ttu-id="20a31-203">Verwenden Sie die **Sicherungs** Aufgabe in SQL Server Management Studio, um die Konformitäts-und Überwachungsdatenbank auf Server A zu sichern. Standardmäßig lautet der Datenbankname **MBAM-Kompatibilitäts Status-Datenbank**.</span><span class="sxs-lookup"><span data-stu-id="20a31-203">Use the **Back Up** task in SQL Server Management Studio to back up the Compliance and Audit Database on Server A. By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="20a31-204">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="20a31-204">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Compliance Status"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Compliance Status Data logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Compliance Status Database Data Device',

    'Z: \MBAM Compliance Status Database Data.bak';

    GO

    -- Back up the full MBAM Compliance Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO

    ```

3.  <span data-ttu-id="20a31-205">Führen Sie das Skript aus, das in der SQL-Datei gespeichert ist, indem Sie einen Windows PowerShell-Befehl verwenden, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="20a31-205">Run the script that is stored in the .sql file by using a Windows PowerShell command that is similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  <span data-ttu-id="20a31-206">Ersetzen Sie mithilfe des folgenden Werts die Werte im Codebeispiel durch Werte, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="20a31-206">Using the following value, replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="20a31-207">**$Servername $ \ $SqlInstanceName $** -Servername und Instanz, aus der die Compliance-und Überwachungsdatenbank gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="20a31-207">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Compliance and Audit Database will be backed up.</span></span>

### <span data-ttu-id="20a31-208">Verschieben der Konformitäts-und Überwachungsdatenbank von Server a auf Server B \* \*</span><span class="sxs-lookup"><span data-stu-id="20a31-208">Move the Compliance and Audit Database from Server A to Server B\*\*</span></span>

1.  <span data-ttu-id="20a31-209">Verwenden Sie den Windows-Explorer, um die Datei " **MBAM Compliance Status Database Data. bak** " von Server a auf Server B zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="20a31-209">Use Windows Explorer to move the **MBAM Compliance Status Database Data.bak** file from Server A to Server B.</span></span>

2.  <span data-ttu-id="20a31-210">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl auszuführen, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="20a31-210">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  <span data-ttu-id="20a31-211">Ersetzen Sie anhand der folgenden Tabelle die Werte im Codebeispiel durch Werte, die Ihrer Umgebung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="20a31-211">Using the following table, replace the values in the code example with values that match your environment.</span></span>

    | **<span data-ttu-id="20a31-212">Parameter</span><span class="sxs-lookup"><span data-stu-id="20a31-212">Parameter</span></span>**        | **<span data-ttu-id="20a31-213">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20a31-213">Description</span></span>**                                               |
    |----------------------|---------------------------------------------------------------|
    | <span data-ttu-id="20a31-214">$Servername $</span><span class="sxs-lookup"><span data-stu-id="20a31-214">$SERVERNAME$</span></span>       | <span data-ttu-id="20a31-215">Der Name des Servers, auf den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20a31-215">Name of the server to which the files will be copied.</span></span>         |
    | <span data-ttu-id="20a31-216">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="20a31-216">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="20a31-217">Name der Freigabe und des Pfads, in den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="20a31-217">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="20a31-218">Wiederherstellen der Konformitäts-und Überwachungsdatenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-218">Restore the Compliance and Audit Database on Server B</span></span>

1.  <span data-ttu-id="20a31-219">Wiederherstellen der Konformitäts-und Überwachungsdatenbank auf Server B mithilfe des Tasks **Datenbank wiederherstellen** in SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="20a31-219">Restore the Compliance and Audit Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="20a31-220">Wenn die vorherige Aufgabe abgeschlossen ist, wählen Sie **vom Gerät aus**, und wählen Sie dann die Datenbanksicherungsdatei aus.</span><span class="sxs-lookup"><span data-stu-id="20a31-220">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="20a31-221">Verwenden Sie den Befehl **Hinzufügen** , um die Datei **Data. bak der MBAM-Konformitäts Status-Datenbank** auszuwählen, und klicken Sie auf **OK** , um den Wiederherstellungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="20a31-221">Use the **Add** command to select the **MBAM Compliance Status Database Data.bak** file and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="20a31-222">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="20a31-222">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  <span data-ttu-id="20a31-223">Führen Sie in Windows PowerShell das Skript aus, das in der Datei gespeichert ist, und ähnlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="20a31-223">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  <span data-ttu-id="20a31-224">Ersetzen Sie die Werte im Codebeispiel mit dem folgenden Wert durch Werte, die Ihrer Umgebung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="20a31-224">Using the following value, replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="20a31-225">**$Servername $ \ $SqlInstanceName $** -Server Name und Instanz, auf die die Konformitäts-und Überwachungsdatenbank wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="20a31-225">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Compliance and Audit Database will be restored.</span></span>

### <span data-ttu-id="20a31-226">Konfigurieren des Zugriffs auf die Datenbank auf Server B und Aktualisieren von Verbindungsdaten</span><span class="sxs-lookup"><span data-stu-id="20a31-226">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="20a31-227">Überprüfen Sie, ob die Microsoft SQL Server-Benutzeranmeldung, die den Zugriff auf die Compliance-und Überwachungsdatenbank in der wiederhergestellten Datenbank ermöglicht, dem Zugriffskonto zugeordnet ist, das Sie während des Konfigurationsprozesses angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="20a31-227">Verify that the Microsoft SQL Server user login that enables Compliance and Audit Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="20a31-228">Wenn die Anmeldung nicht identisch ist, erstellen Sie eine Anmeldung mithilfe von SQL Server Management Studio, und ordnen Sie Sie dem vorhandenen Datenbankbenutzer zu.</span><span class="sxs-lookup"><span data-stu-id="20a31-228">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="20a31-229">Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die Website zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="20a31-229">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the Website.</span></span>

3. <span data-ttu-id="20a31-230">Bearbeiten Sie den folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="20a31-230">Edit the following registry key:</span></span>

   **<span data-ttu-id="20a31-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="20a31-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span></span>**

4. <span data-ttu-id="20a31-232">Aktualisieren Sie den Wert der **Datenquelle** mit dem Namen des Servers und der Instanz (beispielsweise \ $Servername \ $ \ \ \ $SqlInstanceName), in die die Wiederherstellungsdatenbank verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="20a31-232">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="20a31-233">Aktualisieren Sie den **ursprünglichen Katalog** Wert mit dem wiederhergestellten Datenbanknamen.</span><span class="sxs-lookup"><span data-stu-id="20a31-233">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="20a31-234">Um diesen Vorgang zu automatisieren, können Sie die Windows PowerShell-Eingabeaufforderung verwenden, um eine Befehlszeile auf dem Verwaltungs-und Überwachungs Server einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="20a31-234">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   ><span data-ttu-id="20a31-235">Diese Verbindungszeichenfolge wird von allen lokalen MBAM-Webanwendungen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="20a31-235">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="20a31-236">Daher muss Sie nur einmal pro Server aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="20a31-236">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="20a31-237">Ersetzen Sie anhand der folgenden Tabelle die Werte im Codebeispiel durch Werte, die Ihrer Umgebung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="20a31-237">Using the following table, replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="20a31-238">Parameter</span><span class="sxs-lookup"><span data-stu-id="20a31-238">Parameter</span></span> | <span data-ttu-id="20a31-239">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20a31-239">Description</span></span> |
   |---------|------------|
   |<span data-ttu-id="20a31-240">$Servername $ \ $SqlInstanceName $</span><span class="sxs-lookup"><span data-stu-id="20a31-240">$SERVERNAME$\$SQLINSTANCENAME$</span></span> | <span data-ttu-id="20a31-241">Servername und Instanz von SQL Server, auf der sich die Wiederherstellungsdatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="20a31-241">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="20a31-242">$Database $</span><span class="sxs-lookup"><span data-stu-id="20a31-242">$DATABASE$</span></span>|<span data-ttu-id="20a31-243">Der Name der wiederhergestellten Datenbank.</span><span class="sxs-lookup"><span data-stu-id="20a31-243">Name of the recovered database.</span></span>|

### <span data-ttu-id="20a31-244">Installieren der MBAM-Server Software und Ausführen des MBAM-Serverkonfigurations-Assistenten auf Server B</span><span class="sxs-lookup"><span data-stu-id="20a31-244">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="20a31-245">Installieren Sie die MBAM 2,5-Server Software auf Server B. Ausführliche Informationen finden Sie unter [Installieren der MBAM 2,5-Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="20a31-245">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="20a31-246">Starten Sie auf Server B den MBAM-Serverkonfigurations-Assistenten, klicken Sie auf **neue Features hinzufügen**, und wählen Sie dann nur das Feature **Konformitäts-und Überwachungsdatenbank** aus.</span><span class="sxs-lookup"><span data-stu-id="20a31-246">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Compliance and Audit Database** feature.</span></span> <span data-ttu-id="20a31-247">Ausführliche Informationen zum Konfigurieren der Datenbanken finden Sie unter [Konfigurieren der MBAM 2,5-Datenbanken](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="20a31-247">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="20a31-248">Alternativ können Sie das Windows PowerShell **-Cmdlet Enable-MbamDatabase** verwenden, um die Kompatibilitäts-und Überwachungsdatenbank zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="20a31-248">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Compliance and Audit Database.</span></span>


### <span data-ttu-id="20a31-249">Fortsetzen der Instanz der Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="20a31-249">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="20a31-250">Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu starten.</span><span class="sxs-lookup"><span data-stu-id="20a31-250">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="20a31-251">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl auszuführen, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="20a31-251">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="20a31-252">Zum Ausführen dieses Befehls müssen Sie das IIS-Modul für Windows PowerShell der aktuellen Instanz von Windows PowerShell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="20a31-252">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>
