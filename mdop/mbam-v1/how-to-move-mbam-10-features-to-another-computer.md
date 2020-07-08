---
title: Vorgehensweise beim Verschieben von MBAM 1.0-Funktionen auf einen anderen Computer
description: Vorgehensweise beim Verschieben von MBAM 1.0-Funktionen auf einen anderen Computer
author: dansimp
ms.assetid: e1907d92-6b42-4ba3-b0e4-60a9cc8285cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 874c3983220f341e39fa5fb7c60f655e2f208082
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804610"
---
# Vorgehensweise beim Verschieben von MBAM 1.0-Funktionen auf einen anderen Computer


In diesem Thema werden die Schritte beschrieben, die Sie ausführen müssen, um ein oder mehrere Features der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) auf einen anderen Computer zu verschieben. Wenn Sie mehr als ein MBAM-Feature auf einen anderen Computer verschieben, sollten Sie es in der folgenden Reihenfolge verschieben:

1.  Wiederherstellungs-und Hardware Datenbank

2.  Konformitäts-und Überwachungsdatenbank

3.  Konformitäts-und Überwachungsberichte

4.  Verwaltung und Überwachung

## So verschieben Sie die Wiederherstellungs-und Hardware Datenbank


Mit dem folgenden Verfahren können Sie die MBAM-Wiederherstellungs-und-Hardware Datenbank von einem Computer auf einen anderen verschieben (Sie können dieses MBAM-Server Feature von Server a auf Server B verschieben):

****

1.  Beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website.

2.  Führen Sie das MBAM-Setup auf Server B aus.

3.  Sichern Sie die MBAM-Wiederherstellungs-und-Hardware Datenbank auf Server A.

4.  MBAM Recovery and Hardware Database from Server A to B

5.  Wiederherstellen der MBAM-Wiederherstellungs-und-Hardware Datenbank auf Server B

6.  Konfigurieren des Zugriffs auf die MBAM-Wiederherstellungs-und-Hardware Datenbank auf Server B

7.  Aktualisieren der Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern

8.  Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website

**So beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website**

1.  Verwenden Sie die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website auf jedem Server zu beenden, auf dem das Feature für die Verwaltung und Überwachung von MBAM ausgeführt wird. Die MBAM-Website hat den Namen **Microsoft BitLocker-Verwaltung und-Überwachung**.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl an der Eingabeaufforderung verwenden, die mit der folgenden ähnelt:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Hinweis:**  
    Um diese PowerShell-Eingabeaufforderung ausführen zu können, müssen Sie das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzufügen. Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, um die Ausführung von Skripts zu ermöglichen.



**So führen Sie das MBAM-Setup auf Server B aus**

1.  Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie die Wiederherstellungs-und Hardware Datenbank für die Installation aus.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl an der Eingabeaufforderung verwenden, die mit der folgenden ähnelt:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **Hinweis:**  
    Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und der Instanz ein, auf die die Wiederherstellungs-und Hardware Datenbank verschoben wird.

    -   $Domain $ \ \ $Servername $ – Geben Sie die Domänen-und Servernamen jeder MBAM-Anwendung und des Überwachungsservers ein, die sich mit der Wiederherstellungs-und Hardware Datenbank in Verbindung setzen. Wenn mehrere Domänen-und Servernamen vorhanden sind, verwenden Sie ein Semikolon, um die einzelnen Namen in der Liste zu trennen. Beispiel: $Domain \\Servername $; $Domain \ \ $Servername $ $. Darüber hinaus muss jeder Servername von a gefolgt werden **$** . Beispiel: MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.



**So sichern Sie die Datenbank auf Server A**

1.  Wenn Sie die Wiederherstellungs-und Hardware Datenbank auf Server A sichern möchten, verwenden Sie SQL Server Management Studio und die Aufgabe mit dem Namen **sichern.**.. Standardmäßig ist der Datenbankname **MBAM-Wiederherstellungs-und-Hardware Datenbank**.

2.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:

    Ändern Sie die MBAM-Wiederherstellungs-und Hardware Datenbank, um den vollständigen Wiederherstellungsmodus zu verwenden.

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    Erstellen Sie MBAM-Wiederherstellungs-und Hardware Datenbank-und MBAM-Wiederherstellungs-logische Sicherungsmedien.

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    Sichern Sie die vollständige MBAM-Wiederherstellungs-und-Hardware Datenbank.

    ```sql
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
    Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Password $ – geben Sie ein Kennwort ein, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwenden werden.



3.  Führen Sie die SQL-Datei mithilfe von SQL Server PowerShell und einem Befehl aus, der der folgenden ähnelt:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Hinweis:**  
    Ersetzen Sie den Wert im vorherigen Beispiel durch die Werte, die mit Ihrer Umgebung übereinstimmen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und die Instanz ein, von der Sie die Wiederherstellungs-und Hardware Datenbank sichern.



**So verschieben Sie die Datenbank und das Zertifikat von Server A nach B**

1.  Verschieben Sie die MBAM-Wiederherstellungs-und Hardware-Datenbankdaten. bak von Server A auf Server B mithilfe von Windows-Explorer.

2.  Um das Zertifikat für die verschlüsselte Datenbank zu verschieben, müssen Sie die folgenden Automatisierungsschritte verwenden. Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Hinweis:**  
    Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:

    -   $Servername $ – Geben Sie den Namen des Servers ein, auf den die Dateien kopiert werden sollen.

    -   $DESTINATIONSHARE $ – geben Sie den Namen der Freigabe und den Pfad ein, in den die Dateien kopiert werden sollen.



**So stellen Sie die Datenbank auf Server B wieder her**

1.  Stellen Sie die Wiederherstellungs-und Hardware Datenbank auf Server B mithilfe von SQL Server Management Studio und der Aufgabe mit dem Namen **Restore Database**wieder her.

2.  Nachdem die Aufgabe ausgeführt wurde, wählen Sie die Datenbanksicherungsdatei aus, indem Sie die Option **vom Gerät** auswählen, und verwenden Sie dann den Befehl **Hinzufügen** , um die Datei MBAM Recovery and Hardware Database **Data. bak** auszuwählen.

3.  Wählen Sie **OK** aus, um den Wiederherstellungsvorgang abzuschließen.

4.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    Legen Sie das vom MBAM-Setup erstellte Zertifikat ab.

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    Zertifikat hinzufügen

    ```sql
    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

        FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

        DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

    Wiederherstellen der MBAM-Wiederherstellungs-und Hardware-Datenbankdaten und der Protokolldateien

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **Hinweis:**  
    Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Password $ – geben Sie das Kennwort ein, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwendet haben.



5.  Verwenden Sie Windows PowerShell, um eine Befehlszeile einzugeben, die der folgenden ähnelt:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Hinweis:**  
    Ersetzen Sie den Wert aus dem Beispiel für den Rückzug durch die Werte, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und die Instanz ein, auf die die Wiederherstellungs-und Hardware Datenbank wiederhergestellt werden soll.



**Konfigurieren des Zugriffs auf die Datenbank auf Server B**

1.  Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, der lokalen Gruppe " **MBAM Recovery and Hardware DB Access**" hinzuzufügen.

2.  Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell auf Server B verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Hinweis:**  
    Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch die anwendbaren Werte für Ihre Umgebung:

    -   $Domain $ \ \ $Servername $ $ – Geben Sie den Domänennamen und den Computernamen des MBAM-Verwaltungs-und-Überwachungsservers ein. Auf den Servernamen muss ein, Beispiels **$** Weise MyDomain\\MyServerName1 $, folgen.



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**So aktualisieren Sie die Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern**

1. Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die IIS-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die folgenden Anwendungen zu aktualisieren, die auf der Website Microsoft BitLocker-Verwaltung und-Überwachung gehostet werden:

   -   MBAM-Verwaltungsdienst

   -   MBAM-Wiederherstellungs-und Hardware Dienst

2. Wählen Sie jede Anwendung aus, und verwenden Sie das Feature " **Konfigurations-Editor** ", das sich unter dem Abschnitt " **Verwaltung** " der **Funktionsansicht**befindet.

3. Wählen Sie die Option **configurationStrings** im Steuerelement Abschnittsliste aus.

4. Wählen Sie die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den **Sammlungs-Editor** , indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.

5. Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen **KeyRecoveryConnectionString** aus, wenn Sie die Konfiguration für die Anwendung "MBAMAdministrationService" aktualisiert haben, oder wählen Sie die Zeile mit dem Namen " <strong> Microsoft. mbam. RecoveryAndHardwareDataStore" aus. </strong> ConnectionString beim Aktualisieren der Konfiguration für das "MBAMRecoveryAndHardwareService".

6. Aktualisieren Sie die **Datenquelle =** Wert für die **configurationStrings** -Eigenschaft, um den Servernamen und die Instanz aufzulisten, in die die Wiederherstellungs-und Hardware Datenbank verschoben wurde. Beispiel: $Servername $ \ \ $SQLInstanceName $.

7. Um dieses Verfahren zu automatisieren, können Sie einen Befehl verwenden, der mit dem folgenden vergleichbar ist, indem Sie Windows PowerShell auf den einzelnen Verwaltungs-und Überwachungs Servern verwenden:

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Hinweis:**  
   Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:

   -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der sich die Wiederherstellungs-und Hardware Datenbank befindet.



**So setzen Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website fort**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## So verschieben Sie das Feature "Kompatibilitäts Status Datenbank"


Wenn Sie sich entscheiden, das Feature MBAM-Konformitäts Status-Datenbank von einem Computer auf einen anderen zu verschieben, beispielsweise von Server a auf Server B, sollten Sie das folgende Verfahren verwenden:

1.  Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website

2.  Ausführen des MBAM-Setups auf Server B

3.  Sichern der Datenbank auf Server A

4.  Verschieben der Datenbank von Server A nach B

5.  Wiederherstellen der Datenbank auf Server B

6.  Konfigurieren des Zugriffs auf die Datenbank auf Server B

7.  Aktualisieren von Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern

8.  Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website

**So beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu beenden.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Hinweis:**  
    Zum Ausführen dieses Befehls müssen Sie das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzufügen. Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, um die Ausführung von Skripts zu ermöglichen.



**So führen Sie das MBAM-Setup auf Server B aus**

1.  Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie das Feature Kompatibilitäts Status-Datenbank für die Installation aus.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **Hinweis:**  
    Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in die die Kompatibilitäts Status Datenbank verschoben wird.

    -   $Domain $ \ \ $Servername $ – Geben Sie die Domänennamen und Servernamen jeder MBAM-Anwendung und des Überwachungsservers ein, die sich an die Kompatibilitäts Status Datenbank wenden. Wenn mehrere Domänennamen und Servernamen vorhanden sind, verwenden Sie ein Semikolon, um die einzelnen Namen in der Liste zu trennen. Beispiel: $Domain \\Servername $; $Domain \ \ $Servername $ $. Auf jeden Servernamen muss a folgen **$** , wie im Beispiel gezeigt. Beispiel: MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.

    -   $Domain $ \ \ $username $ – geben Sie die Domäne und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Kompatibilitäts Status Datenbank herzustellen.



**So sichern Sie die Kompatibilitätsdatenbank auf Server A**

1.  Wenn Sie die Kompatibilitätsdatenbank auf Server A sichern möchten, verwenden Sie SQL Server Management Studio und die Aufgabe mit dem Namen **sichern.**.. Standardmäßig lautet der Datenbankname **MBAM-Kompatibilitäts Status-Datenbank**.

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

    -- Back up the full MBAM Recovery and Hardware database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Führen Sie die SQL-Datei mit einem Befehl aus, der der folgenden ähnelt, indem Sie die SQL Server-PowerShell verwenden:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Hinweis:**  
    Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, aus der die Datenbank des Kompatibilitäts Status gesichert werden soll.



**So verschieben Sie die Datenbank von Server A nach B**

1.  Verschieben Sie die folgenden Dateien von Server a auf Server B mithilfe von Windows-Explorer:

    -   MBAM-Kompatibilitäts Status-Datenbankdaten. bak

2.  Um dieses Verfahren zu automatisieren, können Sie einen Befehl verwenden, der mit Windows PowerShell ähnlich wie der folgende ist:

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Hinweis:**  
    Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:

    -   $Servername $ – Geben Sie den Servernamen ein, in den die Dateien kopiert werden sollen.

    -   $DESTINATIONSHARE $ – geben Sie den Namen der Freigabe und des Pfads ein, in den die Dateien kopiert werden sollen.



**So stellen Sie die Datenbank auf Server B wieder her**

1.  Wiederherstellen der Kompatibilitäts Status Datenbank auf Server B mithilfe von SQL Server Management Studio und der Aufgabe mit dem Namen **Restore Database.**...

2.  Nachdem die Aufgabe ausgeführt wurde, wählen Sie die Datenbanksicherungsdatei aus, indem Sie die Option vom Gerät auswählen, und verwenden Sie dann den Befehl hinzufügen, um die Datei MBAM Compliance Status Database Data. bak auszuwählen. Klicken Sie auf OK, um den Wiederherstellungsvorgang abzuschließen.

3.  Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Führen Sie die SQL-Datei mit einem Befehl aus, der der folgenden ähnelt, indem Sie die SQL Server-PowerShell verwenden:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Hinweis:**  
    Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der die Kompatibilitäts Status Datenbank wiederhergestellt werden soll.



**So konfigurieren Sie den Zugriff auf die Datenbank auf Server B**

1.  Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server hinzuzufügen, der das Feature MBAM-Verwaltung und-Überwachung ausführt, in der lokalen Gruppe mit dem Namen **MBAM-Konformitäts Status DB Access**.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell auf Server B einen Befehl verwenden, der dem folgenden ähnelt:

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Hinweis:**  
    Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die anwendbaren Werte für Ihre Umgebung:

    -   $Domain $ \ \ $Servername $ $ – Geben Sie den Namen der Domäne und des Computers des MBAM-Verwaltungs-und-Überwachungsservers ein. Auf den Servernamen muss ein folgen **$** . Beispiel: MyDomain\\MyServerName1 $.

    -   $Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**So aktualisieren Sie die Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die IIS-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die folgenden Anwendungen zu aktualisieren, die auf der Website Microsoft BitLocker-Verwaltung und-Überwachung gehostet werden:

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Wählen Sie jede Anwendung aus, und verwenden Sie das Feature " **Konfigurations-Editor** ", das sich unter dem Abschnitt " **Verwaltung** " der **Funktionsansicht**befindet.

3.  Wählen Sie die Option **configurationStrings** im Steuerelement Abschnittsliste aus.

4.  Wählen Sie die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den Sammlungs-Editor, indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.

5.  Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen **ComplianceStatusConnectionString**aus, wenn Sie die Konfiguration für die MBAMAdministrationService-Anwendung aktualisieren, oder die Zeile mit dem Namen **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, wenn Sie die Konfiguration für die MBAMComplianceStatusService aktualisieren.

6.  Aktualisieren Sie die **Datenquelle =** Wert für die **configurationStrings** -Eigenschaft, um den Servernamen und den Instanzennamen aufzulisten. Beispiel: $Servername $ \ \ $SqlInstanceName, auf die die Wiederherstellungs-und Hardware Datenbank verschoben wurde.

7.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl eingeben, der auf den einzelnen Verwaltungs-und Überwachungs Servern mit dem folgenden vergleichbar ist:

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Hinweis:**  
    Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und den Instanznamen ein, in dem sich die Wiederherstellungs-und Hardware Datenbank befindet.



**So setzen Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website fort**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.

2.  Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:

    **PS C:\\ &gt; Start-Website "Microsoft BitLocker-Verwaltung und-Überwachung"**

## So verschieben Sie die Konformitäts-und Überwachungsberichte


Wenn Sie die MBAM-Konformitäts-und Überwachungsberichte von einem Computer auf einen anderen verschieben möchten (insbesondere, wenn Sie das Feature von Server a auf Server B verschieben), sollten Sie die folgenden Schritte ausführen:

1.  Ausführen des MBAM-Setups auf Server B

2.  Konfigurieren des Zugriffs auf die Konformitäts-und Überwachungsberichte auf Server B

3.  Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website

4.  Aktualisieren der Verbindungsdaten für Berichte auf MBAM-Verwaltungs-und-Überwachungs Servern

5.  Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website

**So führen Sie das MBAM-Setup auf Server B aus**

1.  Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie nur das Feature Compliance und Überwachung für die Installation aus.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen ähnlichen Befehl wie den folgenden verwenden:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **Hinweis:**  
    Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der sich die Kompatibilitäts Status Datenbank befindet.

    -   $Domain $ \ \ $username $ – geben Sie den Domänennamen und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Kompatibilitäts Status Datenbank herzustellen.

    -   $Password $ – geben Sie das Kennwort für das Benutzerkonto ein, das zum Herstellen einer Verbindung mit der Kompatibilitäts Status Datenbank verwendet wird.



**So konfigurieren Sie den Zugriff auf die Konformitäts-und Überwachungsberichte auf Server B**

1.  Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Benutzerkonten hinzuzufügen, die Zugriff auf die Konformitäts-und Überwachungsberichte erhalten. Fügen Sie die Benutzerkonten der lokalen Gruppe mit dem Namen "MBAM-Berichtsbenutzer" hinzu.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell auf Server B einen ähnlichen Befehl wie den folgenden verwenden.

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Hinweis:**  
    Ersetzen Sie den folgenden Wert aus dem vorhergehenden Beispiel durch die anwendbaren Werte für Ihre Umgebung:

    -   $Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**So beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu beenden.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**So aktualisieren Sie die Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern**

1. Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die URL für die Konformitätsberichte mithilfe der Internet Informationsdienste (IIS)-Manager-Konsole.

2. Wählen Sie die Website **Microsoft BitLocker-Verwaltung und-Überwachung** aus, und verwenden Sie das Feature **Konfigurations-Editor** , das unter dem Abschnitt **Verwaltung** der **Featureansicht**zu finden ist.

3. Wählen Sie die Option **appSettings** im Steuerelement Abschnittsliste aus.

4. Wählen Sie hier die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den **Sammlungs-Editor** , indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.

5. Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen "Microsoft. mbam. Reports. URL" aus.

6. Aktualisieren Sie den Wert für Microsoft. mbam. Reports. URL, um den Servernamen für Server B anzugeben. Wenn das Feature Konformitäts-und Überwachungsberichte auf einer benannten SQL Reporting Services-Instanz installiert wurde, stellen Sie sicher, dass Sie den Namen der Instanz zur URL hinzufügen oder aktualisieren. Beispiel: http://$Servername $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....

7. Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl eingeben, der auf den einzelnen Verwaltungs-und Überwachungs Servern mit dem folgenden vergleichbar ist:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **Hinweis:**  
   Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:

   -   $Servername $ – Geben Sie den Namen des Servers ein, auf dem die Konformitäts-und Überwachungsberichte installiert wurden.

   -   $SRSINSTANCENAME $ – geben Sie den Namen der SQL Reporting Services-Instanz ein, auf die die Kompatibilitäts-und Überwachungsberichte installiert wurden.



**So setzen Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website fort**

1.  Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Hinweis:**  
    Zum Ausführen dieses Befehls muss das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzugefügt werden. Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, um die Ausführung von Skripts zu ermöglichen.



## So verschieben Sie das Feature "Verwaltung und Überwachung"


Wenn Sie das Feature MBAM-Verwaltungs-und Überwachungsberichte von einem Computer auf einen anderen verschieben möchten (wenn Sie das Feature von Server a auf Server B verschieben), sollten Sie das folgende Verfahren verwenden. Der Prozess umfasst die folgenden Schritte:

1.  Ausführen des MBAM-Setups auf Server B

2.  Konfigurieren des Zugriffs auf die Datenbank auf Server B

**So führen Sie das MBAM-Setup auf Server B aus**

1.  Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie nur das Verwaltungsfeature für die Installation aus.

2.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **Hinweis:**  
    Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:

    -   $Servername $ \ \ $SqlInstanceName $ – geben Sie für den COMPLIDB \ _SQLINSTANCE-Parameter den Servernamen und die Instanz ein, in der sich die Kompatibilitäts Status Datenbank befindet. Geben Sie für den RECOVERYANDHWDB \ _SQLINSTANCE-Parameter den Servernamen und die Instanz ein, in der sich die Wiederherstellungs-und Hardware Datenbank befindet.

    -   $Domain $ \ \ $username $ – geben Sie die Domäne und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Kompatibilitäts Status Datenbank herzustellen.

    -   $ REPORTSSERVERURL $ – geben Sie die URL für den Startspeicherort der SQL Reporting Service-Website ein. Wenn die Berichte in einer Standard-SRS-Instanz installiert wurden, wird das URL-Format "http://$Servername $/ReportServer" formatiert. Wenn die Berichte in einer Standard-SRS-Instanz installiert wurden, wird das URL-Format auf "http://$Servername $/ReportServer\_ $ SqlInstanceName $" formatiert.



**So konfigurieren Sie den Zugriff auf die Datenbanken**

1.  Auf dem Server oder auf Servern, auf denen die Wiederherstellung und die Hardware und Konformitäts-und Überwachungsdatenbanken bereitgestellt werden, verwenden Sie das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server, auf dem die MBAM-Verwaltungs-und-Überwachungsfunktion ausgeführt wird, den lokalen Gruppen "MBAM Recovery and Hardware DB Access" (Recovery and Hardware DB Server) und "MBAM Compliance Status DB-Server" hinzuzufügen.

2.  Um dieses Verfahren zu automatisieren, können Sie einen Befehl verwenden, der mit dem folgenden vergleichbar ist, indem Sie Windows PowerShell auf dem Server verwenden, auf dem die Kompatibilitäts-und Überwachungsdatenbanken bereitgestellt wurden.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  Führen Sie auf dem Server, auf dem die Wiederherstellungs-und Hardware Datenbanken bereitgestellt wurden, mithilfe von Windows PowerShell einen Befehl aus, der mit dem folgenden vergleichbar ist.

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Hinweis:**  
    Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die anwendbaren Werte für Ihre Umgebung:

    -   $Domain $ \ \ $Servername $ $ – Geben Sie den Namen der Domäne und des Computers des MBAM-Verwaltungs-und-Überwachungsservers ein. Auf den Servernamen muss ein folgen **$** . Beispiel: MyDomain\\MyServerName1 $)

    -   $Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Verwandte Themen


[Verwalten von MBAM 1.0-Funktionen](administering-mbam-10-features.md)









