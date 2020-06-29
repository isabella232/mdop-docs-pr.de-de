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
# So verschieben Sie die MBAM 2.5-Datenbanken

Gehen Sie wie folgt vor, um die folgenden Datenbanken von einem Computer auf einen anderen zu verschieben. von Server A nach Server B, beispielsweise:

-   Konformitäts-und Überwachungsdatenbank

-   Wiederherstellungsdatenbank

>[!NOTE]
>Es ist wichtig, dass die Datenbanken auf Computer B wiederhergestellt werden, bevor Sie den MBAM-Konfigurations-Assistenten ausführen, um Sie zu aktualisieren/zu konfigurieren.

Wenn die Datenbanken nicht vorhanden sind, erstellt der Konfigurations-Assistent neue, leere Datenbanken. Wenn Ihre vorhandenen Datenbanken wiederhergestellt werden, wird durch diesen Vorgang die MBAM-Konfiguration unterbrochen.

Stellen Sie zuerst die Datenbanken wieder her, und führen Sie dann den MBAM-Konfigurations-Assistenten aus, wählen Sie die Option Datenbank aus, und der Konfigurations-Assistent wird mit den wiederhergestellten Datenbanken verbunden. Sie können Sie bei Bedarf im Rahmen des Prozesses aktualisieren.

**Wenn Sie mehrere Features verschieben, verschieben Sie Sie in der folgenden Reihenfolge:**

1.  Wiederherstellungsdatenbank

2.  Konformitäts-und Überwachungsdatenbank

3.  Berichte

4.  Website "Verwaltung und Überwachung"

5.  Self-Service-Portal

>[!Note]
>Wenn Sie die in diesem Thema bereitgestellten Beispiel-Windows PowerShell-Skripts ausführen möchten, müssen Sie die Windows PowerShell-Ausführungsrichtlinie aktualisieren, damit Skripts ausgeführt werden können. Anweisungen finden Sie unter [Ausführen von Windows PowerShell-Skripts](https://technet.microsoft.com/library/ee176949.aspx) .

## Verschieben der Wiederherstellungsdatenbank

Die allgemeinen Schritte zum Verschieben der Wiederherstellungsdatenbank lauten wie folgt:

1.  Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website

2.  Sichern der Wiederherstellungsdatenbank auf Server A

3.  Verschieben der Wiederherstellungsdatenbank von Server a auf Server B

4.  Wiederherstellen der Wiederherstellungsdatenbank auf Server B

5.  Konfigurieren des Zugriffs auf die Datenbank auf Server B und Aktualisieren von Verbindungsdaten

6.  Installieren der MBAM-Server Software und Ausführen des MBAM-Serverkonfigurations-Assistenten auf Server B

7.  Fortsetzen der Instanz der Website "Verwaltung und Überwachung"

### Verschieben der Wiederherstellungsdatenbank

**Beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website.** Verwenden Sie auf jedem Server, auf dem die MBAM-Verwaltungs-und Monitoring Server-Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu beenden.

Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Zum Ausführen dieses Befehls müssen Sie das IIS-Modul (Internet Information Services) für Windows PowerShell der aktuellen Instanz von Windows PowerShell hinzufügen.

### Sichern der Wiederherstellungsdatenbank auf Server A

1.  Verwenden Sie die **Sicherungs** Aufgabe in SQL Server Management Studio, um die Wiederherstellungsdatenbank auf Server A zu sichern.  Standardmäßig lautet der Datenbankname **MBAM-Wiederherstellungsdatenbank**.

2.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält, und ändern Sie die MBAM-Wiederherstellungsdatenbank, um den vollständigen Wiederherstellungsmodus zu verwenden:

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

3.  Verwenden Sie den folgenden Wert, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen:

    **$Password $** -Kennwort, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwenden.

4.  Führen Sie in Windows PowerShell das Skript aus, das in der Datei gespeichert ist, und ähnlich der folgenden:

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  Verwenden Sie den folgenden Wert, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen:

    **$Servername $ \ $SqlInstanceName $** -Servername und Instanz, aus der die Wiederherstellungsdatenbank gesichert wird.

### Verschieben der Wiederherstellungsdatenbank von Server a auf Server B

Verwenden Sie den Windows-Explorer, um die Datei **MBAM Recovery Database Data. bak** von Server a auf Server B zu verschieben.

Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl auszuführen, der der folgenden ähnelt:

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
Verwenden Sie die Informationen in der folgenden Tabelle, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen.

| **Parameter**        | **Beschreibung**  |
|----------------------|------------------|
| $Servername $       | Der Name des Servers, auf den die Dateien kopiert werden sollen. |
| $DESTINATIONSHARE $ | Name der Freigabe und des Pfads, in den die Dateien kopiert werden sollen. |


### Wiederherstellen der Wiederherstellungsdatenbank auf Server B

1.  Stellen Sie die Wiederherstellungsdatenbank auf Server B mithilfe der Aufgabe **Datenbank wiederherstellen** in SQL Server Management Studio wieder her.

2.  Wenn die vorherige Aufgabe abgeschlossen ist, wählen Sie **vom Gerät aus**, und wählen Sie dann die Datenbanksicherungsdatei aus.

3.  Verwenden Sie den Befehl **Hinzufügen** , um die Datei **MBAM Recovery Database Data. bak** auszuwählen, und klicken Sie auf **OK** , um den Wiederherstellungsvorgang abzuschließen.

4.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:

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

5.  Verwenden Sie den folgenden Wert, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen.

    **$Password $** -Kennwort, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwendet haben.

6.  Führen Sie in Windows PowerShell das Skript aus, das in der Datei gespeichert ist, und ähnlich der folgenden:

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  Verwenden Sie den folgenden Wert, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen.

    **$Servername $ \ $SqlInstanceName $** -Server Name und Instanz, in die die Wiederherstellungsdatenbank wiederhergestellt wird.

### Konfigurieren des Zugriffs auf die Datenbank auf Server B und Aktualisieren von Verbindungsdaten

1. Überprüfen Sie, ob die Microsoft SQL Server-Benutzeranmeldung, die den Zugriff auf die Wiederherstellung der Datenbank in der wiederhergestellten Datenbank ermöglicht, dem Zugriffskonto zugeordnet ist, das Sie während des Konfigurationsprozesses angegeben haben.

   >[!NOTE]
   >Wenn die Anmeldung nicht identisch ist, erstellen Sie eine Anmeldung mithilfe von SQL Server Management Studio, und ordnen Sie Sie dem vorhandenen Datenbankbenutzer zu.

2. Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die MBAM-Websites zu aktualisieren.

3. Bearbeiten Sie den folgenden Registrierungsschlüssel:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString**

4. Aktualisieren Sie den Wert der **Datenquelle** mit dem Namen des Servers und der Instanz (beispielsweise \ $Servername \ $ \ \ \ $SqlInstanceName), in die die Wiederherstellungsdatenbank verschoben wurde.

5. Aktualisieren Sie den **ursprünglichen Katalog** Wert mit dem wiederhergestellten Datenbanknamen.

6. Um diesen Vorgang zu automatisieren, können Sie die Windows PowerShell-Eingabeaufforderung verwenden, um eine Befehlszeile auf dem Verwaltungs-und Überwachungs Server einzugeben, die der folgenden ähnelt:

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
   >Diese Verbindungszeichenfolge wird von allen lokalen MBAM-Webanwendungen freigegeben. Daher muss Sie nur einmal pro Server aktualisiert werden.


7. Verwenden Sie die folgende Tabelle, um die Werte im Codebeispiel durch Werte zu ersetzen, die Ihrer Umgebung entsprechen.

   |Parameter|Beschreibung|
   |---------|-----------|
   |$Servername $/\ $SqlInstanceName $|Servername und Instanz von SQL Server, auf der sich die Wiederherstellungsdatenbank befindet.|
   |$Database $|Der Name der Wiederherstellungsdatenbank.|


### Installieren der MBAM-Server Software und Ausführen des MBAM-Serverkonfigurations-Assistenten auf Server B

1.  Installieren Sie die MBAM 2,5-Server Software auf Server B. Ausführliche Informationen finden Sie unter [Installieren der MBAM 2,5-Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  Starten Sie auf Server B den MBAM-Serverkonfigurations-Assistenten, klicken Sie auf **neue Features hinzufügen**, und wählen Sie dann nur das Feature **Wiederherstellungsdatenbank** aus. Ausführliche Informationen zum Konfigurieren der Datenbanken finden Sie unter [Konfigurieren der MBAM 2,5-Datenbanken](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >Alternativ können Sie das Windows PowerShell **-Cmdlet Enable-MbamDatabase** verwenden, um die Wiederherstellungsdatenbank zu konfigurieren.


### Fortsetzen der Instanz der Website "Verwaltung und Überwachung"

Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu starten.

Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl auszuführen, der der folgenden ähnelt:

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Zum Ausführen dieses Befehls müssen Sie das IIS-Modul für Windows PowerShell der aktuellen Instanz von Windows PowerShell hinzufügen.

## Verschieben der Konformitäts-und Überwachungsdatenbank

Die allgemeinen Schritte zum Verschieben der Kompatibilitäts-und Überwachungsdatenbank lauten wie folgt:

1.  Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website

2.  Sichern der Konformitäts-und Überwachungsdatenbank auf Server A

3.  Verschieben der Konformitäts-und Überwachungsdatenbank von Server a auf Server B

4.  Wiederherstellen der Konformitäts-und Überwachungsdatenbank auf Server B

5.  Konfigurieren des Zugriffs auf die Datenbank auf Server B und Aktualisieren von Verbindungsdaten

6.  Installieren der MBAM-Server Software und Ausführen des MBAM-Serverkonfigurations-Assistenten auf Server B

7.  Fortsetzen der Instanz der Website "Verwaltung und Überwachung"

### Verschieben der Konformitäts-und Überwachungsdatenbank

**Beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website.**  Verwenden Sie auf jedem Server, auf dem die MBAM-Verwaltungs-und Monitoring Server-Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu beenden.

Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Zum Ausführen dieses Befehls müssen Sie das IIS-Modul (Internet Information Services) für Windows PowerShell der aktuellen Instanz von Windows PowerShell hinzufügen.

### Sichern der Konformitäts-und Überwachungsdatenbank auf Server A

1.  Verwenden Sie die **Sicherungs** Aufgabe in SQL Server Management Studio, um die Konformitäts-und Überwachungsdatenbank auf Server A zu sichern. Standardmäßig lautet der Datenbankname **MBAM-Kompatibilitäts Status-Datenbank**.

2.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:

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

3.  Führen Sie das Skript aus, das in der SQL-Datei gespeichert ist, indem Sie einen Windows PowerShell-Befehl verwenden, der der folgenden ähnelt:

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  Ersetzen Sie mithilfe des folgenden Werts die Werte im Codebeispiel durch Werte, die Ihrer Umgebung entsprechen:

    **$Servername $ \ $SqlInstanceName $** -Servername und Instanz, aus der die Compliance-und Überwachungsdatenbank gesichert wird.

### Verschieben der Konformitäts-und Überwachungsdatenbank von Server a auf Server B * *

1.  Verwenden Sie den Windows-Explorer, um die Datei " **MBAM Compliance Status Database Data. bak** " von Server a auf Server B zu verschieben.

2.  Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl auszuführen, der der folgenden ähnelt:

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  Ersetzen Sie anhand der folgenden Tabelle die Werte im Codebeispiel durch Werte, die Ihrer Umgebung entsprechen.

    | **Parameter**        | **Beschreibung**                                               |
    |----------------------|---------------------------------------------------------------|
    | $Servername $       | Der Name des Servers, auf den die Dateien kopiert werden sollen.         |
    | $DESTINATIONSHARE $ | Name der Freigabe und des Pfads, in den die Dateien kopiert werden sollen. |


### Wiederherstellen der Konformitäts-und Überwachungsdatenbank auf Server B

1.  Wiederherstellen der Konformitäts-und Überwachungsdatenbank auf Server B mithilfe des Tasks **Datenbank wiederherstellen** in SQL Server Management Studio

2.  Wenn die vorherige Aufgabe abgeschlossen ist, wählen Sie **vom Gerät aus**, und wählen Sie dann die Datenbanksicherungsdatei aus.

3.  Verwenden Sie den Befehl **Hinzufügen** , um die Datei **Data. bak der MBAM-Konformitäts Status-Datenbank** auszuwählen, und klicken Sie auf **OK** , um den Wiederherstellungsvorgang abzuschließen.

4.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  Führen Sie in Windows PowerShell das Skript aus, das in der Datei gespeichert ist, und ähnlich der folgenden:

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  Ersetzen Sie die Werte im Codebeispiel mit dem folgenden Wert durch Werte, die Ihrer Umgebung entsprechen.

    **$Servername $ \ $SqlInstanceName $** -Server Name und Instanz, auf die die Konformitäts-und Überwachungsdatenbank wiederhergestellt wird.

### Konfigurieren des Zugriffs auf die Datenbank auf Server B und Aktualisieren von Verbindungsdaten

1. Überprüfen Sie, ob die Microsoft SQL Server-Benutzeranmeldung, die den Zugriff auf die Compliance-und Überwachungsdatenbank in der wiederhergestellten Datenbank ermöglicht, dem Zugriffskonto zugeordnet ist, das Sie während des Konfigurationsprozesses angegeben haben.

   >[!NOTE]
   >Wenn die Anmeldung nicht identisch ist, erstellen Sie eine Anmeldung mithilfe von SQL Server Management Studio, und ordnen Sie Sie dem vorhandenen Datenbankbenutzer zu.

2. Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die Website zu aktualisieren.

3. Bearbeiten Sie den folgenden Registrierungsschlüssel:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString**

4. Aktualisieren Sie den Wert der **Datenquelle** mit dem Namen des Servers und der Instanz (beispielsweise \ $Servername \ $ \ \ \ $SqlInstanceName), in die die Wiederherstellungsdatenbank verschoben wurde.

5. Aktualisieren Sie den **ursprünglichen Katalog** Wert mit dem wiederhergestellten Datenbanknamen.

6. Um diesen Vorgang zu automatisieren, können Sie die Windows PowerShell-Eingabeaufforderung verwenden, um eine Befehlszeile auf dem Verwaltungs-und Überwachungs Server einzugeben, die der folgenden ähnelt:

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   >Diese Verbindungszeichenfolge wird von allen lokalen MBAM-Webanwendungen freigegeben. Daher muss Sie nur einmal pro Server aktualisiert werden.


7. Ersetzen Sie anhand der folgenden Tabelle die Werte im Codebeispiel durch Werte, die Ihrer Umgebung entsprechen.

   |Parameter | Beschreibung |
   |---------|------------|
   |$Servername $ \ $SqlInstanceName $ | Servername und Instanz von SQL Server, auf der sich die Wiederherstellungsdatenbank befindet.|
   |$Database $|Der Name der wiederhergestellten Datenbank.|

### Installieren der MBAM-Server Software und Ausführen des MBAM-Serverkonfigurations-Assistenten auf Server B

1.  Installieren Sie die MBAM 2,5-Server Software auf Server B. Ausführliche Informationen finden Sie unter [Installieren der MBAM 2,5-Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  Starten Sie auf Server B den MBAM-Serverkonfigurations-Assistenten, klicken Sie auf **neue Features hinzufügen**, und wählen Sie dann nur das Feature **Konformitäts-und Überwachungsdatenbank** aus. Ausführliche Informationen zum Konfigurieren der Datenbanken finden Sie unter [Konfigurieren der MBAM 2,5-Datenbanken](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >Alternativ können Sie das Windows PowerShell **-Cmdlet Enable-MbamDatabase** verwenden, um die Kompatibilitäts-und Überwachungsdatenbank zu konfigurieren.


### Fortsetzen der Instanz der Website "Verwaltung und Überwachung"

Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu starten.

Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl auszuführen, der der folgenden ähnelt:

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Zum Ausführen dieses Befehls müssen Sie das IIS-Modul für Windows PowerShell der aktuellen Instanz von Windows PowerShell hinzufügen.
