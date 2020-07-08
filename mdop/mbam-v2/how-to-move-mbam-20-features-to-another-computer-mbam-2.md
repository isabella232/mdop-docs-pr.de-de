---
title: So verschieben Sie MBAM 2.0-Funktionen auf einen anderen Computer
description: So verschieben Sie MBAM 2.0-Funktionen auf einen anderen Computer
author: dansimp
ms.assetid: 49bc0792-60a4-473f-89cc-ada30191e04a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 340d87e26d87f124a9ab64c63d33e89c293d8a86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810939"
---
# So verschieben Sie MBAM 2.0-Funktionen auf einen anderen Computer


In diesem Thema werden die Schritte beschrieben, die Sie ausführen müssen, um ein oder mehrere Features der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) auf einen anderen Computer zu verschieben. Wenn Sie mehr als ein Microsoft BitLocker-Verwaltungs-und Überwachungsfeature verschieben, sollten Sie Sie in der folgenden Reihenfolge verschieben:

1.  Wiederherstellungsdatenbank

2.  Konformitäts-und Überwachungsdatenbank

3.  Konformitäts-und Überwachungsberichte

4.  Verwaltung und Überwachung

## Verschieben der Wiederherstellungsdatenbank


Wenn Sie die Wiederherstellungsdatenbank von einem Computer auf einen anderen verschieben möchten (beispielsweise von Server a nach Server B), gehen Sie wie folgt vor:

1.  Beenden Sie alle Instanzen der Websiteverwaltung und Überwachung.

2.  Führen Sie MBAM-Setup auf Server B aus.

3.  Sichern Sie die MBAM-Wiederherstellungsdatenbank auf Server A.

4.  Verschieben Sie die MBAM-Wiederherstellungsdatenbank von Server A nach B.

5.  Wiederherstellen der MBAM-Wiederherstellungsdatenbank auf Server B

6.  Konfigurieren Sie den Zugriff auf die MBAM-Wiederherstellungsdatenbank auf Server B.

7.  Aktualisieren Sie die Datenbankverbindungsdaten auf den MBAM-Verwaltungs-und-Überwachungs Servern.

8.  Setzen Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website fort.

**Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu beenden.

2.  Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um die Befehlszeile einzugeben, die der folgenden ähnelt:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Hinweis:**  
    Damit diese PowerShell-Befehlszeile ausgeführt werden kann, muss das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzugefügt werden. Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, um die Ausführung von Skripts zu ermöglichen.



**Ausführen des MBAM-Setups auf Server B**

1.  Führen Sie MBAM-Setup auf Server B aus, und wählen Sie nur die **Wiederherstellungsdatenbank** für die Installation aus.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und der Instanz ein, in die die Wiederherstellungsdatenbank verschoben wird.

    -   $Domain $ \ \ $Servername $ – Geben Sie die Domänen-und Servernamen der einzelnen MBAM-Verwaltungs-und-Überwachungsserver ein, die sich an die Wiederherstellungsdatenbank wenden. Verwenden Sie ein Semikolon, um die einzelnen Domänen-und Server Paare in der Liste zu trennen (beispielsweise $Domain \\Servername $; $Domain \ \ $Servername $ $). Auf jeden Servernamen muss ein "$"-Symbol folgen, wie im Beispiel gezeigt (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $X $ – geben Sie **0** ein, wenn Sie die eigenständige MBAM-Topologie installieren, oder **1** , wenn Sie die MBAM Configuration Manager-Topologie installieren.



**Sichern der Wiederherstellungsdatenbank auf Server A**

1.  Wenn Sie die Wiederherstellungsdatenbank auf Server A sichern möchten, verwenden Sie SQL Server Management Studio und die Aufgabe mit dem Namen sichern. Standardmäßig lautet der Datenbankname **MBAM-Wiederherstellungsdatenbank**.

2.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:

    Ändern Sie die MBAM-Wiederherstellungsdatenbank, um den vollständigen Wiederherstellungsmodus zu verwenden.

    ```sql
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

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Password $ – geben Sie ein Kennwort ein, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwenden werden.



3.  Führen Sie die SQL-Datei mithilfe von SQL Server PowerShell und einer Befehlszeile aus, die der folgenden ähnelt:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und der Instanz ein, aus der die Wiederherstellungsdatenbank gesichert werden soll.



**Verschieben der Wiederherstellungsdatenbank und des Zertifikats von Server a auf Server B**

1.  Verschieben Sie die folgende Datei mithilfe von Windows-Explorer von Server a nach Server B.

    -   MBAM Recovery Database Data. bak

2.  Führen Sie die folgenden Automatisierungsschritte aus, um das Zertifikat für die verschlüsselte Datenbank zu verschieben. Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Hinweis:**  
    Ersetzen Sie den folgenden Wert im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ – Geben Sie den Namen des Servers ein, auf den die Dateien kopiert werden sollen.

    -   $DESTINATIONSHARE $ – geben Sie den Namen der Freigabe und den Pfad ein, in den die Dateien kopiert werden sollen.



**Wiederherstellen der Wiederherstellungsdatenbank auf Server B**

1.  Stellen Sie die Wiederherstellungsdatenbank auf Server B mithilfe von SQL Server Management Studio und der Aufgabe mit dem Namen **Restore Database**wieder her.

2.  Nachdem die Aufgabe abgeschlossen ist, wählen Sie die Datenbanksicherungsdatei aus, indem Sie die Option " **vom Gerät** " auswählen und dann mit dem Befehl " **Hinzufügen** " die Datei "MBAM Recovery Database **Data. bak** " auswählen.

3.  Wählen Sie **OK** aus, um den Wiederherstellungsvorgang abzuschließen.

4.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:

    ```sql
    -- Restore MBAM Recovery Database. 

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

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

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Password $ – geben Sie ein Kennwort ein, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwendet haben.



5.  Sie können Windows PowerShell verwenden, um eine Befehlszeile einzugeben, die der folgenden ähnelt:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Hinweis:**  
    Ersetzen Sie den folgenden Wert im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und der Instanz ein, in der die Wiederherstellungsdatenbank wiederhergestellt werden soll.



**Konfigurieren des Zugriffs auf die Wiederherstellungsdatenbank auf Server B**

1.  Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, der lokalen Gruppe " **MBAM Recovery and Hardware DB Access**" hinzuzufügen.

2.  Überprüfen Sie, ob der SQL **-Anmelde MBAM Recovery-und Hardware DB-Zugriff** in der wiederhergestellten Datenbank dem Anmeldenamen **$MachineName $ \\MBAM Recovery-und Hardware-DB-Zugriff**zugeordnet ist. Wenn Sie nicht wie beschrieben zugeordnet ist, erstellen Sie eine weitere Anmeldung mit ähnlichen Gruppenmitgliedschaften, und ordnen Sie Sie dem Anmeldenamen **$MachineName $ \\MBAM Recovery-und Hardware-DB-Zugriff**zu.

3.  Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell auf Server B verwenden, um eine Befehlszeile einzugeben, die der folgenden ähnelt:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch die anwendbaren Werte für Ihre Umgebung:

    -   $Domain $ \ \ $Servername $ $ – Geben Sie den Namen der Domäne und des Computers des MBAM-Verwaltungs-und-Überwachungsservers ein. Dem Servernamen muss ein $ folgen, wie im Beispiel gezeigt wird (beispielsweise MyDomain\\MyServerName1 $).



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Aktualisieren der Verbindungsdaten der Wiederherstellungsdatenbank auf den MBAM-Verwaltungs-und-Überwachungs Servern**

1. Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die IIS-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die folgenden Anwendungen zu aktualisieren, die auf der Websiteverwaltung und Überwachung gehostet werden:

   -   MBAMAdministrationService

   -   MBAMRecoveryAndHardwareService

2. Wählen Sie jede Anwendung aus, und verwenden Sie das Feature " **Konfigurations-Editor** ", das sich unter dem Abschnitt " **Verwaltung** " der **Funktionsansicht**befindet.

3. Wählen Sie die Option **configurationStrings** im Steuerelement **Abschnittsliste** aus.

4. Wählen Sie die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den **Sammlungs-Editor** , indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.

5. Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen **KeyRecoveryConnectionString** aus, wenn Sie die Konfiguration für die MBAMAdministrationService-Anwendung oder die Zeile mit dem Namen <strong> Microsoft. mbam. RecoveryAndHardwareDataStore aktualisieren. </strong> ConnectionString beim Aktualisieren der Konfiguration für das MBAMRecoveryAndHardwareService.

6. Aktualisieren Sie die **Datenquelle =** Wert für die **configurationStrings** -Eigenschaft, um den Servernamen und die Instanz aufzulisten (beispielsweise $Servername $ \ \ $SqlInstanceName $), in die die Wiederherstellungsdatenbank verschoben wurde.

7. Wenn Sie dieses Verfahren automatisieren möchten, können Sie auf jedem Verwaltungs-und Überwachungs Server mithilfe von Windows eine Befehlszeile eingeben, die der folgenden ähnelt:

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Hinweis:**  
   Ersetzen Sie den folgenden Wert im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

   -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der sich die Wiederherstellungsdatenbank befindet.



**Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.

2.  Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um eine Befehlszeile einzugeben, die der folgenden ähnelt:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Verschieben des Features "Konformitäts-und Überwachungsdatenbank"


Wenn Sie die MBAM-Konformitäts-und Überwachungsdatenbank von einem Computer auf einen anderen verschieben möchten (d. h., verschieben Sie die Datenbank von Server a auf Server B), gehen Sie wie folgt vor: Der Prozess umfasst die folgenden allgemeinen Schritte:

1.  Beenden Sie alle Instanzen der Websiteverwaltung und Überwachung.

2.  Führen Sie MBAM-Setup auf Server B aus.

3.  Sichern Sie die Datenbank auf Server A.

4.  Verschieben Sie die Datenbank von Server A nach B.

5.  Wiederherstellen der Datenbank auf Server B

6.  Konfigurieren Sie den Zugriff auf die Datenbank auf Server B.

7.  Aktualisieren Sie die Datenbankverbindungsdaten auf den MBAM-Verwaltungs-und-Überwachungs Servern.

8.  Aktualisieren Sie die Verbindungszeichenfolge der Datenquelle für SSRS-Berichte mit dem neuen Speicherort der Kompatibilitäts-und Überwachungsdatenbank.

9.  Fortsetzen aller Instanzen der Website "Verwaltung und Überwachung"

**Beenden aller Instanzen der Verwaltungs-und Überwachungs Website**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu beenden.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **Hinweis:**  
    Damit diese Befehlszeile ausgeführt werden kann, müssen Sie das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzufügen. Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, damit Skripts ausgeführt werden können.



**Ausführen des MBAM-Setups auf Server B**

1.  Führen Sie MBAM-Setup auf Server B aus, und wählen Sie nur die **Kompatibilitäts-und Überwachungsdatenbank** für die Installation aus.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **Hinweis:**  
    Hinweis: Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in die die Kompatibilitäts-und Überwachungsdatenbank verschoben wird.

    -   $Domain $ \ \ $Servername $ – Geben Sie die Domänen-und Servernamen der einzelnen MBAM-Verwaltungs-und-Überwachungsserver ein, die sich mit der Konformitäts-und Überwachungsdatenbank in Verbindung setzen. Verwenden Sie ein Semikolon, um jede Domäne und jedes Serverpaar in der Liste zu trennen (beispielsweise $Domain \\Servername $; $Domain \ \ $Servername $ $). Auf jeden Servernamen muss ein "$"-Symbol folgen, wie im Beispiel gezeigt (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $Domain $ \ \ $username $ – geben Sie die Domäne und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Konformitäts-und Überwachungsdatenbank herzustellen.

    -   $X $ – geben Sie **0** ein, wenn Sie die eigenständige MBAM-Topologie installieren, oder **1** , wenn Sie die MBAM Configuration Manager-Topologie installieren.



**Sichern der Konformitäts-und Überwachungsdatenbank auf Server A**

1.  Zum Sichern der Compliance-und Überwachungsdatenbank auf Server A verwenden Sie SQL Server Management Studio und die Aufgabe mit dem Namen **sichern**. Standardmäßig lautet der Datenbankname **MBAM-Kompatibilitäts Status-Datenbank**.

2.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:

    ```sql
    -- Modify the MBAM Compliance Status Database to use the full recovery model.

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

    -- Back up the full MBAM Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Führen Sie die SQL-Datei mithilfe einer Windows PowerShell-Befehlszeile aus, die der folgenden ähnelt:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Hinweis:**  
    Ersetzen Sie den folgenden Wert im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der die Compliance-und Audit-Datenbank gesichert werden soll.



**Verschieben der Konformitäts-und Überwachungsdatenbank von Server A nach B**

1.  Verschieben Sie die folgenden Dateien von Server a auf Server B mithilfe von Windows-Explorer.

    -   MBAM-Kompatibilitäts Status-Datenbankdaten. bak

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ – Geben Sie den Servernamen ein, in den die Dateien kopiert werden sollen.

    -   $DESTINATIONSHARE $ – geben Sie den Namen der Freigabe und des Pfads ein, in den die Dateien kopiert werden sollen.



**Wiederherstellen der Konformitäts-und Überwachungsdatenbank auf Server B**

1.  Wiederherstellen der Konformitäts-und Überwachungsdatenbank auf Server B mithilfe von SQL Server Management Studio und der Aufgabe mit dem Namen **Restore Database**.

2.  Nachdem die Aufgabe abgeschlossen ist, wählen Sie die Datenbanksicherungsdatei aus, indem Sie die Option " **vom Gerät** " auswählen und dann den Befehl " **Hinzufügen** " verwenden, um die Datei "MBAM Compliance Status Database Data. bak" auszuwählen. Wählen Sie **OK** aus, um den Wiederherstellungsvorgang abzuschließen.

3.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Führen Sie die SQL-Datei mithilfe einer Windows PowerShell-Befehlszeile aus, die der folgenden ähnelt:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Hinweis:**  
    Ersetzen Sie den folgenden Wert im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der die Kompatibilitäts-und Überwachungsdatenbank wiederhergestellt werden soll.



**Konfigurieren des Zugriffs auf die Compliance-und Überwachungsdatenbank auf Server B**

1.  Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server hinzuzufügen, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, für die lokale Gruppe mit dem Namen **MBAM-Konformitäts Status DB-Zugriff**.

2.  Überprüfen Sie, ob der SQL-Anmelde **MBAM Compliance Auditing DB-Zugriff** in der wiederhergestellten Datenbank dem Anmeldenamen **$MachineName $ \ \ MBAM Compliance Auditing DB Access**zugeordnet ist. Wenn Sie nicht wie beschrieben zugeordnet ist, erstellen Sie eine weitere Anmeldung mit ähnlichen Gruppenmitgliedschaften, und ordnen Sie Sie dem Anmeldenamen **$MachineName $ \ \ MBAM Compliance Auditing DB Access**zu.

3.  Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um eine Befehlszeile auf Server B einzugeben, die der folgenden ähnelt:

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch die anwendbaren Werte für Ihre Umgebung:

    -   $Domain $ \ \ $Servername $ $ – Geben Sie den Namen der Domäne und des Computers des MBAM-Verwaltungs-und-Überwachungsservers ein. Dem Servernamen muss ein "$" folgen, wie im Beispiel gezeigt. (Beispiel: MyDomain\\MyServerName1 $)

    -   $Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Aktualisieren der Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die folgenden Anwendungen zu aktualisieren, die auf der Websiteverwaltung und Überwachung gehostet werden:

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Wählen Sie jede Anwendung aus, und verwenden Sie das Feature " **Konfigurations-Editor** ", das sich unter dem Abschnitt " **Verwaltung** " der **Funktionsansicht**befindet.

3.  Wählen Sie die Option **configurationStrings** im Steuerelement **Abschnittsliste** aus.

4.  Wählen Sie die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den **Sammlungs-Editor** , indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.

5.  Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen **ComplianceStatusConnectionString** aus, wenn Sie die Konfiguration für die MBAMAdministrationService-Anwendung aktualisieren, oder die Zeile mit dem Namen **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** , wenn Sie die Konfiguration für das MBAMComplianceStatusService aktualisieren.

6.  Aktualisieren Sie die **Datenquelle =** Wert für die **configurationStrings** -Eigenschaft, um den Namen des Servers und der Instanz aufzulisten (beispielsweise $Servername $ \ \ $SqlInstanceName), in die die Wiederherstellungsdatenbank verschoben wurde.

7.  Um dieses Verfahren zu automatisieren, können Sie Windows verwenden, um eine Befehlszeile auf jedem Verwaltungs-und Überwachungs Server einzugeben, die der folgenden ähnelt:

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der sich die Wiederherstellungsdatenbank befindet.



**Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Verschieben der Konformitäts-und Überwachungsberichte


Wenn Sie die MBAM-Konformitäts-und Überwachungsberichte von einem Computer auf einen anderen verschieben möchten (d. h., die Berichte von Server a nach Server B), führen Sie das folgende Verfahren aus, das die folgenden Schritte auf höherer Ebene umfasst:

1.  Führen Sie MBAM-Setup auf Server B aus.

2.  Konfigurieren Sie den Zugriff auf die Konformitäts-und Überwachungsberichte auf Server B.

3.  Beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website.

4.  Aktualisieren Sie die Berichts Verbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern.

5.  Setzen Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website fort.

**Ausführen des MBAM-Setups auf Server B**

1.  Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie nur das Feature **Konformitäts-und Überwachungsberichte** für die Installation aus.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der sich die Konformitäts-und Überwachungsdatenbank befindet.

    -   $Domain $ \ \ $username $ – geben Sie die Domäne und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Konformitäts-und Überwachungsdatenbank herzustellen.

    -   $Password $ – geben Sie das Kennwort für das Benutzerkonto ein, das für die Verbindung mit der Konformitäts-und Überwachungsdatenbank verwendet wird.

    -   $X $ – geben Sie **0** ein, wenn Sie die eigenständige MBAM-Topologie installieren, oder **1** , wenn Sie die MBAM Configuration Manager-Topologie installieren.



**Konfigurieren des Zugriffs auf die Konformitäts-und Überwachungsberichte auf Server B**

1.  Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Benutzerkonten hinzuzufügen, die Zugriff auf die Konformitäts-und Überwachungsberichte erhalten. Fügen Sie die Benutzerkonten der lokalen Gruppe mit dem Namen MBAM-Berichtsbenutzer hinzu.

2.  Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um eine Befehlszeile auf Server B einzugeben, die der folgenden ähnelt:

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch die anwendbaren Werte für Ihre Umgebung:

    -   $Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM Administration and Monitoring Server ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu beenden.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Aktualisieren der Datenbankverbindungsdaten auf den MBAM-Verwaltungs-und-Überwachungs Servern**

1. Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltungs-und Überwachungsserver ausgeführt wird, die IIS-Konsole (Internet Informationsdienste), um die URL für Konformitäts-und Überwachungsberichte zu aktualisieren.

2. Wählen Sie die Website **Microsoft BitLocker-Verwaltung und-Überwachung** aus, und verwenden Sie das **Konfigurations-Editor-** Feature, das sich im Abschnitt **Verwaltung** der **Funktionsansicht**befindet.

3. Wählen Sie die Option **appSettings** im Steuerelement **Abschnittsliste** aus.

4. Wählen Sie die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den **Sammlungs-Editor** , indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.

5. Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen " **Microsoft. mbam. Reports. URL**" aus.

6. Aktualisieren Sie den Wert für **Microsoft. mbam. Reports. URL** , um den Servernamen für Server B anzugeben. Wenn das Feature Konformitäts-und Überwachungsberichte auf einer benannten SQL Reporting Services-Instanz installiert wurde, stellen Sie sicher, dass Sie den Namen der Instanz zur URL hinzufügen oder aktualisieren (beispielsweise http://$Servername $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....).

7. Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um eine Befehlszeile auf jedem Verwaltungs-und Überwachungs Server einzugeben, die der folgenden ähnelt:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **Hinweis:**  
   Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

   -   $Servername $ – Geben Sie den Namen des Server namens ein, auf den die Kompatibilitäts-und Überwachungsberichte installiert wurden.

   -   $SRSINSTANCENAME $ – geben Sie den Namen der SQL Reporting Services-Instanz ein, auf die die Kompatibilitäts-und Überwachungsberichte installiert wurden.



**Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM Administration and Monitoring Server ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Hinweis:**  
    Damit diese Befehlszeile ausgeführt werden kann, müssen Sie das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzufügen. Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, damit Skripts ausgeführt werden können.



## Verschieben des Features "Verwaltung und Überwachung"


Wenn Sie das Feature MBAM-Verwaltung und-Überwachung von einem Computer auf einen anderen verschieben möchten (d. h., verschieben Sie das Feature von Server a auf Server B), führen Sie das folgende Verfahren aus, das die folgenden Schritte auf höherer Ebene umfasst:

1.  Führen Sie MBAM-Setup auf Server B aus.

2.  Konfigurieren Sie den Zugriff auf die Datenbank auf Server B.

**Ausführen des MBAM-Setups auf Server B**

1.  Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie nur die **Verwaltungs-und Überwachungs Server** Funktion für die Installation aus.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie für den COMPLIDB \ _SQLINSTANCE-Parameter den Servernamen und die Instanz ein, in der sich die Konformitäts-und Überwachungsdatenbank befindet. Geben Sie für den RECOVERYANDHWDB \ _SQLINSTANCE-Parameter den Servernamen und die Instanz ein, in der sich die Wiederherstellungsdatenbank befindet.

    -   $Domain $ \ \ $username $ – geben Sie die Domäne und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Konformitäts-und Überwachungsdatenbank herzustellen.

    -   $ REPORTSSERVERURL $ – geben Sie die URL für den Startspeicherort der SQL Reporting Service-Website ein. Wenn die Berichte in einer Standard-SRS-Instanz installiert wurden, weist das URL-Format das Format "http://$Servername $/ReportServer" auf. Wenn die Berichte in einer Standard-SRS-Instanz installiert wurden, weist das URL-Format das Format "http://$Servername $/ReportServer\_ $ SqlInstanceName $" auf.

    -   $X $ – geben Sie **0** ein, wenn Sie die eigenständige MBAM-Topologie installieren, oder **1** , wenn Sie die MBAM Configuration Manager-Topologie installieren.



**Konfigurieren des Zugriffs auf die Datenbanken**

1.  Verwenden Sie auf dem Server oder auf Servern, auf denen die Datenbank für die Wiederherstellung und die Konformitäts-und Überwachungsdatenbank bereitgestellt werden, das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server, auf dem das Feature MBAM-Verwaltungs-und Überwachungsserver ausgeführt wird, den lokalen Gruppen mit dem Namen **MBAM Recovery and Hardware DB Access** **(Recovery** DB

2.  Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um auf dem Server, auf dem die Kompatibilitäts-und Überwachungsdatenbank bereitgestellt wurde, eine Befehlszeile, die der folgenden ähnelt, einzugeben.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  Auf dem Server, auf dem die Wiederherstellungsdatenbank bereitgestellt wurde, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Hinweis:**  
    Ersetzen Sie den folgenden Wert im obigen Beispiel durch die anwendbaren Werte für Ihre Umgebung:

    -   $Domain $ \ \ $Servername $ $ – Geben Sie den Namen der Domäne und des Computers des Verwaltungs-und Überwachungsservers ein. Dem Servernamen muss ein "$"-Symbol folgen, wie im Beispiel gezeigt wird (beispielsweise MyDomain\\MyServerName1 $).

    -   $Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Verwandte Themen


[Verwalten von MBAM 2.0](maintaining-mbam-20-mbam-2.md)









