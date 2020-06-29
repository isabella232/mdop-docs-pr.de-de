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
# <span data-ttu-id="ed85e-103">So verschieben Sie MBAM 2.0-Funktionen auf einen anderen Computer</span><span class="sxs-lookup"><span data-stu-id="ed85e-103">How to Move MBAM 2.0 Features to Another Computer</span></span>


<span data-ttu-id="ed85e-104">In diesem Thema werden die Schritte beschrieben, die Sie ausführen müssen, um ein oder mehrere Features der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) auf einen anderen Computer zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ed85e-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="ed85e-105">Wenn Sie mehr als ein Microsoft BitLocker-Verwaltungs-und Überwachungsfeature verschieben, sollten Sie Sie in der folgenden Reihenfolge verschieben:</span><span class="sxs-lookup"><span data-stu-id="ed85e-105">When moving more than one Microsoft BitLocker Administration and Monitoring feature, you should move them in the following order:</span></span>

1.  <span data-ttu-id="ed85e-106">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="ed85e-106">Recovery Database</span></span>

2.  <span data-ttu-id="ed85e-107">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="ed85e-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="ed85e-108">Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="ed85e-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="ed85e-109">Verwaltung und Überwachung</span><span class="sxs-lookup"><span data-stu-id="ed85e-109">Administration and Monitoring</span></span>

## <span data-ttu-id="ed85e-110">Verschieben der Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="ed85e-110">Moving the Recovery Database</span></span>


<span data-ttu-id="ed85e-111">Wenn Sie die Wiederherstellungsdatenbank von einem Computer auf einen anderen verschieben möchten (beispielsweise von Server a nach Server B), gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="ed85e-111">To move the Recovery Database from one computer to another (for example, from Server A to Server B), use the following procedure.</span></span>

1.  <span data-ttu-id="ed85e-112">Beenden Sie alle Instanzen der Websiteverwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="ed85e-112">Stop all instances of the Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="ed85e-113">Führen Sie MBAM-Setup auf Server B aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-113">Run MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="ed85e-114">Sichern Sie die MBAM-Wiederherstellungsdatenbank auf Server A.</span><span class="sxs-lookup"><span data-stu-id="ed85e-114">Back up the MBAM Recovery Database on Server A.</span></span>

4.  <span data-ttu-id="ed85e-115">Verschieben Sie die MBAM-Wiederherstellungsdatenbank von Server A nach B.</span><span class="sxs-lookup"><span data-stu-id="ed85e-115">Move the MBAM Recovery Database from Server A to B.</span></span>

5.  <span data-ttu-id="ed85e-116">Wiederherstellen der MBAM-Wiederherstellungsdatenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-116">Restore the MBAM Recovery Database on Server B.</span></span>

6.  <span data-ttu-id="ed85e-117">Konfigurieren Sie den Zugriff auf die MBAM-Wiederherstellungsdatenbank auf Server B.</span><span class="sxs-lookup"><span data-stu-id="ed85e-117">Configure access to the MBAM Recovery Database on Server B.</span></span>

7.  <span data-ttu-id="ed85e-118">Aktualisieren Sie die Datenbankverbindungsdaten auf den MBAM-Verwaltungs-und-Überwachungs Servern.</span><span class="sxs-lookup"><span data-stu-id="ed85e-118">Update the database connection data on MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="ed85e-119">Setzen Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website fort.</span><span class="sxs-lookup"><span data-stu-id="ed85e-119">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="ed85e-120">Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="ed85e-120">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="ed85e-121">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ed85e-121">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="ed85e-122">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um die Befehlszeile einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-122">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="ed85e-123">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-123">Note</span></span>**  
    <span data-ttu-id="ed85e-124">Damit diese PowerShell-Befehlszeile ausgeführt werden kann, muss das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ed85e-124">To run this PowerShell command line, the IIS Module for PowerShell must be added to current instance of PowerShell.</span></span> <span data-ttu-id="ed85e-125">Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, um die Ausführung von Skripts zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-125">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



**<span data-ttu-id="ed85e-126">Ausführen des MBAM-Setups auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-126">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="ed85e-127">Führen Sie MBAM-Setup auf Server B aus, und wählen Sie nur die **Wiederherstellungsdatenbank** für die Installation aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-127">Run MBAM Setup on Server B and select only the **Recovery Database** for installation.</span></span>

2.  <span data-ttu-id="ed85e-128">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-128">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="ed85e-129">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-129">Note</span></span>**  
    <span data-ttu-id="ed85e-130">Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-130">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-131">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und der Instanz ein, in die die Wiederherstellungsdatenbank verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="ed85e-131">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be moved.</span></span>

    -   <span data-ttu-id="ed85e-132">$Domain $ \ \ $Servername $ – Geben Sie die Domänen-und Servernamen der einzelnen MBAM-Verwaltungs-und-Überwachungsserver ein, die sich an die Wiederherstellungsdatenbank wenden.</span><span class="sxs-lookup"><span data-stu-id="ed85e-132">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Recovery Database.</span></span> <span data-ttu-id="ed85e-133">Verwenden Sie ein Semikolon, um die einzelnen Domänen-und Server Paare in der Liste zu trennen (beispielsweise $Domain \\Servername $; $Domain \ \ $Servername $ $).</span><span class="sxs-lookup"><span data-stu-id="ed85e-133">Use a semi-colon to separate each domain and server pairs in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="ed85e-134">Auf jeden Servernamen muss ein "$"-Symbol folgen, wie im Beispiel gezeigt (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="ed85e-134">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="ed85e-135">$X $ – geben Sie **0** ein, wenn Sie die eigenständige MBAM-Topologie installieren, oder **1** , wenn Sie die MBAM Configuration Manager-Topologie installieren.</span><span class="sxs-lookup"><span data-stu-id="ed85e-135">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="ed85e-136">Sichern der Wiederherstellungsdatenbank auf Server A</span><span class="sxs-lookup"><span data-stu-id="ed85e-136">Back Up the Recovery Database on Server A</span></span>**

1.  <span data-ttu-id="ed85e-137">Wenn Sie die Wiederherstellungsdatenbank auf Server A sichern möchten, verwenden Sie SQL Server Management Studio und die Aufgabe mit dem Namen sichern.</span><span class="sxs-lookup"><span data-stu-id="ed85e-137">To back up the Recovery Database on Server A, use SQL Server Management Studio and the Task named Back Up.</span></span> <span data-ttu-id="ed85e-138">Standardmäßig lautet der Datenbankname **MBAM-Wiederherstellungsdatenbank**.</span><span class="sxs-lookup"><span data-stu-id="ed85e-138">By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="ed85e-139">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="ed85e-139">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="ed85e-140">Ändern Sie die MBAM-Wiederherstellungsdatenbank, um den vollständigen Wiederherstellungsmodus zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed85e-140">Modify the MBAM Recovery Database to use the full recovery mode.</span></span>

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

    **<span data-ttu-id="ed85e-141">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-141">Note</span></span>**  
    <span data-ttu-id="ed85e-142">Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-142">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-143">$Password $ – geben Sie ein Kennwort ein, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="ed85e-143">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="ed85e-144">Führen Sie die SQL-Datei mithilfe von SQL Server PowerShell und einer Befehlszeile aus, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-144">Run the SQL File by using SQL Server PowerShell and a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="ed85e-145">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-145">Note</span></span>**  
    <span data-ttu-id="ed85e-146">Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-146">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-147">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und der Instanz ein, aus der die Wiederherstellungsdatenbank gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed85e-147">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance from which the Recovery Database will be backed up.</span></span>



**<span data-ttu-id="ed85e-148">Verschieben der Wiederherstellungsdatenbank und des Zertifikats von Server a auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-148">Move the Recovery Database and Certificate from Server A to Server B</span></span>**

1.  <span data-ttu-id="ed85e-149">Verschieben Sie die folgende Datei mithilfe von Windows-Explorer von Server a nach Server B.</span><span class="sxs-lookup"><span data-stu-id="ed85e-149">Move the following file from Server A to Server B by using Windows Explorer.</span></span>

    -   <span data-ttu-id="ed85e-150">MBAM Recovery Database Data. bak</span><span class="sxs-lookup"><span data-stu-id="ed85e-150">MBAM Recovery Database data.bak</span></span>

2.  <span data-ttu-id="ed85e-151">Führen Sie die folgenden Automatisierungsschritte aus, um das Zertifikat für die verschlüsselte Datenbank zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ed85e-151">To move the certificate for the encrypted database, use the following automation steps.</span></span> <span data-ttu-id="ed85e-152">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-152">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="ed85e-153">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-153">Note</span></span>**  
    <span data-ttu-id="ed85e-154">Ersetzen Sie den folgenden Wert im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-154">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-155">$Servername $ – Geben Sie den Namen des Servers ein, auf den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-155">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="ed85e-156">$DESTINATIONSHARE $ – geben Sie den Namen der Freigabe und den Pfad ein, in den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-156">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="ed85e-157">Wiederherstellen der Wiederherstellungsdatenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-157">Restore the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="ed85e-158">Stellen Sie die Wiederherstellungsdatenbank auf Server B mithilfe von SQL Server Management Studio und der Aufgabe mit dem Namen **Restore Database**wieder her.</span><span class="sxs-lookup"><span data-stu-id="ed85e-158">Restore the Recovery Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="ed85e-159">Nachdem die Aufgabe abgeschlossen ist, wählen Sie die Datenbanksicherungsdatei aus, indem Sie die Option " **vom Gerät** " auswählen und dann mit dem Befehl " **Hinzufügen** " die Datei "MBAM Recovery Database **Data. bak** " auswählen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-159">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Recovery database **Data.bak** file.</span></span>

3.  <span data-ttu-id="ed85e-160">Wählen Sie **OK** aus, um den Wiederherstellungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-160">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="ed85e-161">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="ed85e-161">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

    **<span data-ttu-id="ed85e-162">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-162">Note</span></span>**  
    <span data-ttu-id="ed85e-163">Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-163">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-164">$Password $ – geben Sie ein Kennwort ein, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="ed85e-164">$PASSWORD$ - Enter a password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="ed85e-165">Sie können Windows PowerShell verwenden, um eine Befehlszeile einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-165">You can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="ed85e-166">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-166">Note</span></span>**  
    <span data-ttu-id="ed85e-167">Ersetzen Sie den folgenden Wert im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-167">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-168">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und der Instanz ein, in der die Wiederherstellungsdatenbank wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed85e-168">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be restored.</span></span>



**<span data-ttu-id="ed85e-169">Konfigurieren des Zugriffs auf die Wiederherstellungsdatenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-169">Configure Access to the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="ed85e-170">Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, der lokalen Gruppe " **MBAM Recovery and Hardware DB Access**" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-170">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="ed85e-171">Überprüfen Sie, ob der SQL **-Anmelde MBAM Recovery-und Hardware DB-Zugriff** in der wiederhergestellten Datenbank dem Anmeldenamen **$MachineName $ \\MBAM Recovery-und Hardware-DB-Zugriff**zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ed85e-171">Verify that the SQL login **MBAM Recovery and Hardware DB Access** on the restored database is mapped to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span> <span data-ttu-id="ed85e-172">Wenn Sie nicht wie beschrieben zugeordnet ist, erstellen Sie eine weitere Anmeldung mit ähnlichen Gruppenmitgliedschaften, und ordnen Sie Sie dem Anmeldenamen **$MachineName $ \\MBAM Recovery-und Hardware-DB-Zugriff**zu.</span><span class="sxs-lookup"><span data-stu-id="ed85e-172">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span>

3.  <span data-ttu-id="ed85e-173">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell auf Server B verwenden, um eine Befehlszeile einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-173">To automate this procedure, you can use Windows PowerShell on Server B to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="ed85e-174">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-174">Note</span></span>**  
    <span data-ttu-id="ed85e-175">Ersetzen Sie die folgenden Werte im obigen Beispiel durch die anwendbaren Werte für Ihre Umgebung:</span><span class="sxs-lookup"><span data-stu-id="ed85e-175">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="ed85e-176">$Domain $ \ \ $Servername $ $ – Geben Sie den Namen der Domäne und des Computers des MBAM-Verwaltungs-und-Überwachungsservers ein.</span><span class="sxs-lookup"><span data-stu-id="ed85e-176">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="ed85e-177">Dem Servernamen muss ein $ folgen, wie im Beispiel gezeigt wird (beispielsweise MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="ed85e-177">The server name must be followed by a $, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="ed85e-178">Aktualisieren der Verbindungsdaten der Wiederherstellungsdatenbank auf den MBAM-Verwaltungs-und-Überwachungs Servern</span><span class="sxs-lookup"><span data-stu-id="ed85e-178">Update the Recovery Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="ed85e-179">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die IIS-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die folgenden Anwendungen zu aktualisieren, die auf der Websiteverwaltung und Überwachung gehostet werden:</span><span class="sxs-lookup"><span data-stu-id="ed85e-179">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="ed85e-180">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="ed85e-180">MBAMAdministrationService</span></span>

   -   <span data-ttu-id="ed85e-181">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="ed85e-181">MBAMRecoveryAndHardwareService</span></span>

2. <span data-ttu-id="ed85e-182">Wählen Sie jede Anwendung aus, und verwenden Sie das Feature " **Konfigurations-Editor** ", das sich unter dem Abschnitt " **Verwaltung** " der **Funktionsansicht**befindet.</span><span class="sxs-lookup"><span data-stu-id="ed85e-182">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="ed85e-183">Wählen Sie die Option **configurationStrings** im Steuerelement **Abschnittsliste** aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-183">Select the **configurationStrings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="ed85e-184">Wählen Sie die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den **Sammlungs-Editor** , indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-184">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="ed85e-185">Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen **KeyRecoveryConnectionString** aus, wenn Sie die Konfiguration für die MBAMAdministrationService-Anwendung oder die Zeile mit dem Namen <strong> Microsoft. mbam. RecoveryAndHardwareDataStore aktualisieren. </strong> ConnectionString beim Aktualisieren der Konfiguration für das MBAMRecoveryAndHardwareService.</span><span class="sxs-lookup"><span data-stu-id="ed85e-185">In the **Collection Editor**, select the row named **KeyRecoveryConnectionString** when updating the configuration for the MBAMAdministrationService application or the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString when updating the configuration for the MBAMRecoveryAndHardwareService.</span></span>

6. <span data-ttu-id="ed85e-186">Aktualisieren Sie die **Datenquelle =** Wert für die **configurationStrings** -Eigenschaft, um den Servernamen und die Instanz aufzulisten (beispielsweise $Servername $ \ \ $SqlInstanceName $), in die die Wiederherstellungsdatenbank verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="ed85e-186">Update the **Data Source=** value for the **configurationStrings** property to list the server name and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME$) where the Recovery Database was moved to.</span></span>

7. <span data-ttu-id="ed85e-187">Wenn Sie dieses Verfahren automatisieren möchten, können Sie auf jedem Verwaltungs-und Überwachungs Server mithilfe von Windows eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-187">To automate this procedure, you can use Windows to enter a command line, that is similar to the following, on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="ed85e-188">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-188">Note</span></span>**  
   <span data-ttu-id="ed85e-189">Ersetzen Sie den folgenden Wert im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-189">Replace the following value in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="ed85e-190">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der sich die Wiederherstellungsdatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="ed85e-190">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is.</span></span>



**<span data-ttu-id="ed85e-191">Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="ed85e-191">Resume all Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="ed85e-192">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.</span><span class="sxs-lookup"><span data-stu-id="ed85e-192">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="ed85e-193">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um eine Befehlszeile einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-193">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="ed85e-194">Verschieben des Features "Konformitäts-und Überwachungsdatenbank"</span><span class="sxs-lookup"><span data-stu-id="ed85e-194">Moving the Compliance and Audit Database Feature</span></span>


<span data-ttu-id="ed85e-195">Wenn Sie die MBAM-Konformitäts-und Überwachungsdatenbank von einem Computer auf einen anderen verschieben möchten (d. h., verschieben Sie die Datenbank von Server a auf Server B), gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="ed85e-195">If you want to move the MBAM Compliance and Audit Database from one computer to another (that is, move the database from Server A to Server B), use the following procedure.</span></span> <span data-ttu-id="ed85e-196">Der Prozess umfasst die folgenden allgemeinen Schritte:</span><span class="sxs-lookup"><span data-stu-id="ed85e-196">The process includes the following high-level steps:</span></span>

1.  <span data-ttu-id="ed85e-197">Beenden Sie alle Instanzen der Websiteverwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="ed85e-197">Stop all instances of the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="ed85e-198">Führen Sie MBAM-Setup auf Server B aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-198">Run MBAM setup on Server B.</span></span>

3.  <span data-ttu-id="ed85e-199">Sichern Sie die Datenbank auf Server A.</span><span class="sxs-lookup"><span data-stu-id="ed85e-199">Back up the Database on Server A.</span></span>

4.  <span data-ttu-id="ed85e-200">Verschieben Sie die Datenbank von Server A nach B.</span><span class="sxs-lookup"><span data-stu-id="ed85e-200">Move the Database from Server A to B.</span></span>

5.  <span data-ttu-id="ed85e-201">Wiederherstellen der Datenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-201">Restore the Database on Server B.</span></span>

6.  <span data-ttu-id="ed85e-202">Konfigurieren Sie den Zugriff auf die Datenbank auf Server B.</span><span class="sxs-lookup"><span data-stu-id="ed85e-202">Configure access to the Database on Server B.</span></span>

7.  <span data-ttu-id="ed85e-203">Aktualisieren Sie die Datenbankverbindungsdaten auf den MBAM-Verwaltungs-und-Überwachungs Servern.</span><span class="sxs-lookup"><span data-stu-id="ed85e-203">Update the database connection data on the MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="ed85e-204">Aktualisieren Sie die Verbindungszeichenfolge der Datenquelle für SSRS-Berichte mit dem neuen Speicherort der Kompatibilitäts-und Überwachungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="ed85e-204">Update the SSRS reports data source connection string with the new location of the Compliance and Audit Database.</span></span>

9.  <span data-ttu-id="ed85e-205">Fortsetzen aller Instanzen der Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="ed85e-205">Resume all instances of the Administration and Monitoring website.</span></span>

**<span data-ttu-id="ed85e-206">Beenden aller Instanzen der Verwaltungs-und Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="ed85e-206">Stop All Instances of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="ed85e-207">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ed85e-207">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="ed85e-208">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-208">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="ed85e-209">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-209">Note</span></span>**  
    <span data-ttu-id="ed85e-210">Damit diese Befehlszeile ausgeführt werden kann, müssen Sie das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-210">To run this command line, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="ed85e-211">Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, damit Skripts ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="ed85e-211">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



**<span data-ttu-id="ed85e-212">Ausführen des MBAM-Setups auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-212">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="ed85e-213">Führen Sie MBAM-Setup auf Server B aus, und wählen Sie nur die **Kompatibilitäts-und Überwachungsdatenbank** für die Installation aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-213">Run MBAM Setup on Server B and select only the **Compliance and Audit Database** for installation.</span></span>

2.  <span data-ttu-id="ed85e-214">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-214">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="ed85e-215">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-215">Note</span></span>**  
    <span data-ttu-id="ed85e-216">Hinweis: Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-216">Note: Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-217">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in die die Kompatibilitäts-und Überwachungsdatenbank verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="ed85e-217">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be moved to.</span></span>

    -   <span data-ttu-id="ed85e-218">$Domain $ \ \ $Servername $ – Geben Sie die Domänen-und Servernamen der einzelnen MBAM-Verwaltungs-und-Überwachungsserver ein, die sich mit der Konformitäts-und Überwachungsdatenbank in Verbindung setzen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-218">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Compliance and Audit Database.</span></span> <span data-ttu-id="ed85e-219">Verwenden Sie ein Semikolon, um jede Domäne und jedes Serverpaar in der Liste zu trennen (beispielsweise $Domain \\Servername $; $Domain \ \ $Servername $ $).</span><span class="sxs-lookup"><span data-stu-id="ed85e-219">Use a semi-colon to separate each domain and server pair in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="ed85e-220">Auf jeden Servernamen muss ein "$"-Symbol folgen, wie im Beispiel gezeigt (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="ed85e-220">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="ed85e-221">$Domain $ \ \ $username $ – geben Sie die Domäne und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Konformitäts-und Überwachungsdatenbank herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-221">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="ed85e-222">$X $ – geben Sie **0** ein, wenn Sie die eigenständige MBAM-Topologie installieren, oder **1** , wenn Sie die MBAM Configuration Manager-Topologie installieren.</span><span class="sxs-lookup"><span data-stu-id="ed85e-222">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="ed85e-223">Sichern der Konformitäts-und Überwachungsdatenbank auf Server A</span><span class="sxs-lookup"><span data-stu-id="ed85e-223">Back Up the Compliance and Audit Database on Server A</span></span>**

1.  <span data-ttu-id="ed85e-224">Zum Sichern der Compliance-und Überwachungsdatenbank auf Server A verwenden Sie SQL Server Management Studio und die Aufgabe mit dem Namen **sichern**.</span><span class="sxs-lookup"><span data-stu-id="ed85e-224">To back up the Compliance and Audit Database on Server A, use SQL Server Management Studio and the task named **Back Up**.</span></span> <span data-ttu-id="ed85e-225">Standardmäßig lautet der Datenbankname **MBAM-Kompatibilitäts Status-Datenbank**.</span><span class="sxs-lookup"><span data-stu-id="ed85e-225">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="ed85e-226">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="ed85e-226">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="ed85e-227">Führen Sie die SQL-Datei mithilfe einer Windows PowerShell-Befehlszeile aus, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-227">Run the SQL file by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="ed85e-228">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-228">Note</span></span>**  
    <span data-ttu-id="ed85e-229">Ersetzen Sie den folgenden Wert im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-229">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-230">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der die Compliance-und Audit-Datenbank gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed85e-230">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit database will be backed up from.</span></span>



**<span data-ttu-id="ed85e-231">Verschieben der Konformitäts-und Überwachungsdatenbank von Server A nach B</span><span class="sxs-lookup"><span data-stu-id="ed85e-231">Move the Compliance and Audit Database from Server A to B</span></span>**

1.  <span data-ttu-id="ed85e-232">Verschieben Sie die folgenden Dateien von Server a auf Server B mithilfe von Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="ed85e-232">Move the following files from Server A to Server B using Windows Explorer.</span></span>

    -   <span data-ttu-id="ed85e-233">MBAM-Kompatibilitäts Status-Datenbankdaten. bak</span><span class="sxs-lookup"><span data-stu-id="ed85e-233">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="ed85e-234">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-234">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="ed85e-235">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-235">Note</span></span>**  
    <span data-ttu-id="ed85e-236">Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-236">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-237">$Servername $ – Geben Sie den Servernamen ein, in den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-237">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="ed85e-238">$DESTINATIONSHARE $ – geben Sie den Namen der Freigabe und des Pfads ein, in den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-238">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="ed85e-239">Wiederherstellen der Konformitäts-und Überwachungsdatenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-239">Restore the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="ed85e-240">Wiederherstellen der Konformitäts-und Überwachungsdatenbank auf Server B mithilfe von SQL Server Management Studio und der Aufgabe mit dem Namen **Restore Database**.</span><span class="sxs-lookup"><span data-stu-id="ed85e-240">Restore the Compliance and Audit Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="ed85e-241">Nachdem die Aufgabe abgeschlossen ist, wählen Sie die Datenbanksicherungsdatei aus, indem Sie die Option " **vom Gerät** " auswählen und dann den Befehl " **Hinzufügen** " verwenden, um die Datei "MBAM Compliance Status Database Data. bak" auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-241">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="ed85e-242">Wählen Sie **OK** aus, um den Wiederherstellungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-242">Select **OK** to complete the restoration process.</span></span>

3.  <span data-ttu-id="ed85e-243">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="ed85e-243">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="ed85e-244">Führen Sie die SQL-Datei mithilfe einer Windows PowerShell-Befehlszeile aus, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-244">Run the SQL File by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="ed85e-245">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-245">Note</span></span>**  
    <span data-ttu-id="ed85e-246">Ersetzen Sie den folgenden Wert im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-246">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-247">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der die Kompatibilitäts-und Überwachungsdatenbank wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed85e-247">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be restored to.</span></span>



**<span data-ttu-id="ed85e-248">Konfigurieren des Zugriffs auf die Compliance-und Überwachungsdatenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-248">Configure Access to the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="ed85e-249">Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server hinzuzufügen, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, für die lokale Gruppe mit dem Namen **MBAM-Konformitäts Status DB-Zugriff**.</span><span class="sxs-lookup"><span data-stu-id="ed85e-249">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the local group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="ed85e-250">Überprüfen Sie, ob der SQL-Anmelde **MBAM Compliance Auditing DB-Zugriff** in der wiederhergestellten Datenbank dem Anmeldenamen **$MachineName $ \ \ MBAM Compliance Auditing DB Access**zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ed85e-250">Verify that the SQL login **MBAM Compliance Auditing DB Access** on the restored database is mapped to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span> <span data-ttu-id="ed85e-251">Wenn Sie nicht wie beschrieben zugeordnet ist, erstellen Sie eine weitere Anmeldung mit ähnlichen Gruppenmitgliedschaften, und ordnen Sie Sie dem Anmeldenamen **$MachineName $ \ \ MBAM Compliance Auditing DB Access**zu.</span><span class="sxs-lookup"><span data-stu-id="ed85e-251">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span>

3.  <span data-ttu-id="ed85e-252">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um eine Befehlszeile auf Server B einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-252">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="ed85e-253">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-253">Note</span></span>**  
    <span data-ttu-id="ed85e-254">Ersetzen Sie die folgenden Werte im obigen Beispiel durch die anwendbaren Werte für Ihre Umgebung:</span><span class="sxs-lookup"><span data-stu-id="ed85e-254">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="ed85e-255">$Domain $ \ \ $Servername $ $ – Geben Sie den Namen der Domäne und des Computers des MBAM-Verwaltungs-und-Überwachungsservers ein.</span><span class="sxs-lookup"><span data-stu-id="ed85e-255">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="ed85e-256">Dem Servernamen muss ein "$" folgen, wie im Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed85e-256">The server name must be followed by a “$” as shown in the example.</span></span> <span data-ttu-id="ed85e-257">(Beispiel: MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="ed85e-257">(for example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="ed85e-258">$Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ed85e-258">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="ed85e-259">Aktualisieren der Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern</span><span class="sxs-lookup"><span data-stu-id="ed85e-259">Update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="ed85e-260">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die folgenden Anwendungen zu aktualisieren, die auf der Websiteverwaltung und Überwachung gehostet werden:</span><span class="sxs-lookup"><span data-stu-id="ed85e-260">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the connection string information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="ed85e-261">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="ed85e-261">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="ed85e-262">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="ed85e-262">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="ed85e-263">Wählen Sie jede Anwendung aus, und verwenden Sie das Feature " **Konfigurations-Editor** ", das sich unter dem Abschnitt " **Verwaltung** " der **Funktionsansicht**befindet.</span><span class="sxs-lookup"><span data-stu-id="ed85e-263">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="ed85e-264">Wählen Sie die Option **configurationStrings** im Steuerelement **Abschnittsliste** aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-264">Select the **configurationStrings** option from the **Section list** control.</span></span>

4.  <span data-ttu-id="ed85e-265">Wählen Sie die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den **Sammlungs-Editor** , indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-265">Select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="ed85e-266">Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen **ComplianceStatusConnectionString** aus, wenn Sie die Konfiguration für die MBAMAdministrationService-Anwendung aktualisieren, oder die Zeile mit dem Namen **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** , wenn Sie die Konfiguration für das MBAMComplianceStatusService aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ed85e-266">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString** when updating the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString** when updating the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="ed85e-267">Aktualisieren Sie die **Datenquelle =** Wert für die **configurationStrings** -Eigenschaft, um den Namen des Servers und der Instanz aufzulisten (beispielsweise $Servername $ \ \ $SqlInstanceName), in die die Wiederherstellungsdatenbank verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="ed85e-267">Update the **Data Source=** value for the **configurationStrings** property to list the name of the server and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

7.  <span data-ttu-id="ed85e-268">Um dieses Verfahren zu automatisieren, können Sie Windows verwenden, um eine Befehlszeile auf jedem Verwaltungs-und Überwachungs Server einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-268">To automate this procedure, you can use Windows to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="ed85e-269">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-269">Note</span></span>**  
    <span data-ttu-id="ed85e-270">Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-270">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-271">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der sich die Wiederherstellungsdatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="ed85e-271">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is located.</span></span>



**<span data-ttu-id="ed85e-272">Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="ed85e-272">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="ed85e-273">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.</span><span class="sxs-lookup"><span data-stu-id="ed85e-273">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="ed85e-274">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-274">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="ed85e-275">Verschieben der Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="ed85e-275">Moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="ed85e-276">Wenn Sie die MBAM-Konformitäts-und Überwachungsberichte von einem Computer auf einen anderen verschieben möchten (d. h., die Berichte von Server a nach Server B), führen Sie das folgende Verfahren aus, das die folgenden Schritte auf höherer Ebene umfasst:</span><span class="sxs-lookup"><span data-stu-id="ed85e-276">If you want to move the MBAM Compliance and Audit Reports from one computer to another (that is, move the reports from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="ed85e-277">Führen Sie MBAM-Setup auf Server B aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-277">Run MBAM setup on Server B.</span></span>

2.  <span data-ttu-id="ed85e-278">Konfigurieren Sie den Zugriff auf die Konformitäts-und Überwachungsberichte auf Server B.</span><span class="sxs-lookup"><span data-stu-id="ed85e-278">Configure access to the Compliance and Audit Reports on Server B.</span></span>

3.  <span data-ttu-id="ed85e-279">Beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="ed85e-279">Stop all instances of the MBAM Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="ed85e-280">Aktualisieren Sie die Berichts Verbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern.</span><span class="sxs-lookup"><span data-stu-id="ed85e-280">Update the reports connection data on MBAM Administration and Monitoring servers.</span></span>

5.  <span data-ttu-id="ed85e-281">Setzen Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website fort.</span><span class="sxs-lookup"><span data-stu-id="ed85e-281">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="ed85e-282">Ausführen des MBAM-Setups auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-282">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="ed85e-283">Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie nur das Feature **Konformitäts-und Überwachungsberichte** für die Installation aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-283">Run MBAM Setup on Server B and select only the **Compliance and Audit Reports** feature for installation.</span></span>

2.  <span data-ttu-id="ed85e-284">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-284">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **<span data-ttu-id="ed85e-285">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-285">Note</span></span>**  
    <span data-ttu-id="ed85e-286">Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-286">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-287">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der sich die Konformitäts-und Überwachungsdatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="ed85e-287">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database is located.</span></span>

    -   <span data-ttu-id="ed85e-288">$Domain $ \ \ $username $ – geben Sie die Domäne und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Konformitäts-und Überwachungsdatenbank herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-288">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="ed85e-289">$Password $ – geben Sie das Kennwort für das Benutzerkonto ein, das für die Verbindung mit der Konformitäts-und Überwachungsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed85e-289">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="ed85e-290">$X $ – geben Sie **0** ein, wenn Sie die eigenständige MBAM-Topologie installieren, oder **1** , wenn Sie die MBAM Configuration Manager-Topologie installieren.</span><span class="sxs-lookup"><span data-stu-id="ed85e-290">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="ed85e-291">Konfigurieren des Zugriffs auf die Konformitäts-und Überwachungsberichte auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-291">Configure Access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="ed85e-292">Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Benutzerkonten hinzuzufügen, die Zugriff auf die Konformitäts-und Überwachungsberichte erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed85e-292">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="ed85e-293">Fügen Sie die Benutzerkonten der lokalen Gruppe mit dem Namen MBAM-Berichtsbenutzer hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed85e-293">Add the user accounts to the local group named MBAM Report Users.</span></span>

2.  <span data-ttu-id="ed85e-294">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um eine Befehlszeile auf Server B einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-294">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="ed85e-295">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-295">Note</span></span>**  
    <span data-ttu-id="ed85e-296">Ersetzen Sie die folgenden Werte im obigen Beispiel durch die anwendbaren Werte für Ihre Umgebung:</span><span class="sxs-lookup"><span data-stu-id="ed85e-296">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="ed85e-297">$Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ed85e-297">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="ed85e-298">Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="ed85e-298">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="ed85e-299">Verwenden Sie auf jedem Server, auf dem das Feature MBAM Administration and Monitoring Server ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ed85e-299">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="ed85e-300">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-300">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="ed85e-301">Aktualisieren der Datenbankverbindungsdaten auf den MBAM-Verwaltungs-und-Überwachungs Servern</span><span class="sxs-lookup"><span data-stu-id="ed85e-301">Update the Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="ed85e-302">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltungs-und Überwachungsserver ausgeführt wird, die IIS-Konsole (Internet Informationsdienste), um die URL für Konformitäts-und Überwachungsberichte zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ed85e-302">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to update the Compliance and Audit Reports URL.</span></span>

2. <span data-ttu-id="ed85e-303">Wählen Sie die Website **Microsoft BitLocker-Verwaltung und-Überwachung** aus, und verwenden Sie das **Konfigurations-Editor-** Feature, das sich im Abschnitt **Verwaltung** der **Funktionsansicht**befindet.</span><span class="sxs-lookup"><span data-stu-id="ed85e-303">Select the **Microsoft BitLocker Administration and Monitoring** website, and use the **Configuration Editor** feature that is location under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="ed85e-304">Wählen Sie die Option **appSettings** im Steuerelement **Abschnittsliste** aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-304">Select the **appSettings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="ed85e-305">Wählen Sie die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den **Sammlungs-Editor** , indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-305">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="ed85e-306">Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen " **Microsoft. mbam. Reports. URL**" aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-306">In the **Collection Editor**, select the row named **Microsoft.Mbam.Reports.Url**.</span></span>

6. <span data-ttu-id="ed85e-307">Aktualisieren Sie den Wert für **Microsoft. mbam. Reports. URL** , um den Servernamen für Server B anzugeben. Wenn das Feature Konformitäts-und Überwachungsberichte auf einer benannten SQL Reporting Services-Instanz installiert wurde, stellen Sie sicher, dass Sie den Namen der Instanz zur URL hinzufügen oder aktualisieren (beispielsweise http://$Servername $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....).</span><span class="sxs-lookup"><span data-stu-id="ed85e-307">Update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B. If the Compliance and Audit Reports feature was installed on a named SQL Reporting Services instance, be sure to add or update the name of the instance to the URL (for example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....)</span></span>

7. <span data-ttu-id="ed85e-308">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um eine Befehlszeile auf jedem Verwaltungs-und Überwachungs Server einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-308">To automate this procedure, you can use Windows PowerShell to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **<span data-ttu-id="ed85e-309">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-309">Note</span></span>**  
   <span data-ttu-id="ed85e-310">Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-310">Replace the following values in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="ed85e-311">$Servername $ – Geben Sie den Namen des Server namens ein, auf den die Kompatibilitäts-und Überwachungsberichte installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ed85e-311">$SERVERNAME$ - Enter the name of the server name to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="ed85e-312">$SRSINSTANCENAME $ – geben Sie den Namen der SQL Reporting Services-Instanz ein, auf die die Kompatibilitäts-und Überwachungsberichte installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ed85e-312">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="ed85e-313">Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="ed85e-313">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="ed85e-314">Verwenden Sie auf jedem Server, auf dem das Feature MBAM Administration and Monitoring Server ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.</span><span class="sxs-lookup"><span data-stu-id="ed85e-314">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="ed85e-315">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-315">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="ed85e-316">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-316">Note</span></span>**  
    <span data-ttu-id="ed85e-317">Damit diese Befehlszeile ausgeführt werden kann, müssen Sie das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-317">To run this command line, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="ed85e-318">Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, damit Skripts ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="ed85e-318">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



## <span data-ttu-id="ed85e-319">Verschieben des Features "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="ed85e-319">Moving the Administration and Monitoring Feature</span></span>


<span data-ttu-id="ed85e-320">Wenn Sie das Feature MBAM-Verwaltung und-Überwachung von einem Computer auf einen anderen verschieben möchten (d. h., verschieben Sie das Feature von Server a auf Server B), führen Sie das folgende Verfahren aus, das die folgenden Schritte auf höherer Ebene umfasst:</span><span class="sxs-lookup"><span data-stu-id="ed85e-320">If you want to move the MBAM Administration and Monitoring Reports feature from one computer to another (that is, move the feature from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="ed85e-321">Führen Sie MBAM-Setup auf Server B aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-321">Run MBAM Setup on Server B.</span></span>

2.  <span data-ttu-id="ed85e-322">Konfigurieren Sie den Zugriff auf die Datenbank auf Server B.</span><span class="sxs-lookup"><span data-stu-id="ed85e-322">Configure access to the Database on Server B.</span></span>

**<span data-ttu-id="ed85e-323">Ausführen des MBAM-Setups auf Server B</span><span class="sxs-lookup"><span data-stu-id="ed85e-323">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="ed85e-324">Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie nur die **Verwaltungs-und Überwachungs Server** Funktion für die Installation aus.</span><span class="sxs-lookup"><span data-stu-id="ed85e-324">Run MBAM Setup on Server B and select only the **Administration and Monitoring Server** feature for installation.</span></span>

2.  <span data-ttu-id="ed85e-325">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-325">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **<span data-ttu-id="ed85e-326">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-326">Note</span></span>**  
    <span data-ttu-id="ed85e-327">Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="ed85e-327">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="ed85e-328">$Servername $ \ \ $SqlInstanceName $ – geben Sie für den COMPLIDB \ _SQLINSTANCE-Parameter den Servernamen und die Instanz ein, in der sich die Konformitäts-und Überwachungsdatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="ed85e-328">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, enter the server name and instance where the Compliance and Audit Database is located.</span></span> <span data-ttu-id="ed85e-329">Geben Sie für den RECOVERYANDHWDB \ _SQLINSTANCE-Parameter den Servernamen und die Instanz ein, in der sich die Wiederherstellungsdatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="ed85e-329">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, enter the server name and instance where the Recovery Database is located.</span></span>

    -   <span data-ttu-id="ed85e-330">$Domain $ \ \ $username $ – geben Sie die Domäne und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Konformitäts-und Überwachungsdatenbank herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ed85e-330">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="ed85e-331">$ REPORTSSERVERURL $ – geben Sie die URL für den Startspeicherort der SQL Reporting Service-Website ein.</span><span class="sxs-lookup"><span data-stu-id="ed85e-331">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="ed85e-332">Wenn die Berichte in einer Standard-SRS-Instanz installiert wurden, weist das URL-Format das Format "http://$Servername $/ReportServer" auf.</span><span class="sxs-lookup"><span data-stu-id="ed85e-332">If the reports were installed to a default SRS instance, the URL format will have the format “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="ed85e-333">Wenn die Berichte in einer Standard-SRS-Instanz installiert wurden, weist das URL-Format das Format "http://$Servername $/ReportServer\_ $ SqlInstanceName $" auf.</span><span class="sxs-lookup"><span data-stu-id="ed85e-333">If the reports were installed to a default SRS instance, the URL format will have the format “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>

    -   <span data-ttu-id="ed85e-334">$X $ – geben Sie **0** ein, wenn Sie die eigenständige MBAM-Topologie installieren, oder **1** , wenn Sie die MBAM Configuration Manager-Topologie installieren.</span><span class="sxs-lookup"><span data-stu-id="ed85e-334">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="ed85e-335">Konfigurieren des Zugriffs auf die Datenbanken</span><span class="sxs-lookup"><span data-stu-id="ed85e-335">Configure Access to the Databases</span></span>**

1.  <span data-ttu-id="ed85e-336">Verwenden Sie auf dem Server oder auf Servern, auf denen die Datenbank für die Wiederherstellung und die Konformitäts-und Überwachungsdatenbank bereitgestellt werden, das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server, auf dem das Feature MBAM-Verwaltungs-und Überwachungsserver ausgeführt wird, den lokalen Gruppen mit dem Namen **MBAM Recovery and Hardware DB Access** **(Recovery** DB</span><span class="sxs-lookup"><span data-stu-id="ed85e-336">On the server or servers where the Recovery Database and Compliance and Audit Database are deployed, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring Server feature to the local groups named **MBAM Recovery and Hardware DB Access** (Recovery DB Server) and **MBAM Compliance Status DB Access** (Compliance and Audit Database Server).</span></span>

2.  <span data-ttu-id="ed85e-337">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um auf dem Server, auf dem die Kompatibilitäts-und Überwachungsdatenbank bereitgestellt wurde, eine Befehlszeile, die der folgenden ähnelt, einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ed85e-337">To automate this procedure, you can use Windows PowerShell to enter a command line, that is similar to the following, on the server where the Compliance and Audit Database was deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  <span data-ttu-id="ed85e-338">Auf dem Server, auf dem die Wiederherstellungsdatenbank bereitgestellt wurde, können Sie mithilfe von Windows PowerShell eine Befehlszeile eingeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="ed85e-338">On the server where the Recovery database was deployed, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="ed85e-339">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ed85e-339">Note</span></span>**  
    <span data-ttu-id="ed85e-340">Ersetzen Sie den folgenden Wert im obigen Beispiel durch die anwendbaren Werte für Ihre Umgebung:</span><span class="sxs-lookup"><span data-stu-id="ed85e-340">Replace the following value in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="ed85e-341">$Domain $ \ \ $Servername $ $ – Geben Sie den Namen der Domäne und des Computers des Verwaltungs-und Überwachungsservers ein.</span><span class="sxs-lookup"><span data-stu-id="ed85e-341">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the Administration and Monitoring Server.</span></span> <span data-ttu-id="ed85e-342">Dem Servernamen muss ein "$"-Symbol folgen, wie im Beispiel gezeigt wird (beispielsweise MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="ed85e-342">The server name must be followed by a “$” symbol, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>

    -   <span data-ttu-id="ed85e-343">$Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ed85e-343">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="ed85e-344">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ed85e-344">Related topics</span></span>


[<span data-ttu-id="ed85e-345">Verwalten von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ed85e-345">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)









