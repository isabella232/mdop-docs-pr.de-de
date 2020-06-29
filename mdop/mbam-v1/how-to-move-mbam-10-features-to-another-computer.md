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
# <span data-ttu-id="1755b-103">Vorgehensweise beim Verschieben von MBAM 1.0-Funktionen auf einen anderen Computer</span><span class="sxs-lookup"><span data-stu-id="1755b-103">How to Move MBAM 1.0 Features to Another Computer</span></span>


<span data-ttu-id="1755b-104">In diesem Thema werden die Schritte beschrieben, die Sie ausführen müssen, um ein oder mehrere Features der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) auf einen anderen Computer zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="1755b-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="1755b-105">Wenn Sie mehr als ein MBAM-Feature auf einen anderen Computer verschieben, sollten Sie es in der folgenden Reihenfolge verschieben:</span><span class="sxs-lookup"><span data-stu-id="1755b-105">When you move more than one MBAM feature to another computer, you should move them in the following order:</span></span>

1.  <span data-ttu-id="1755b-106">Wiederherstellungs-und Hardware Datenbank</span><span class="sxs-lookup"><span data-stu-id="1755b-106">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="1755b-107">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="1755b-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="1755b-108">Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="1755b-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="1755b-109">Verwaltung und Überwachung</span><span class="sxs-lookup"><span data-stu-id="1755b-109">Administration and Monitoring</span></span>

## <span data-ttu-id="1755b-110">So verschieben Sie die Wiederherstellungs-und Hardware Datenbank</span><span class="sxs-lookup"><span data-stu-id="1755b-110">To move the Recovery and Hardware Database</span></span>


<span data-ttu-id="1755b-111">Mit dem folgenden Verfahren können Sie die MBAM-Wiederherstellungs-und-Hardware Datenbank von einem Computer auf einen anderen verschieben (Sie können dieses MBAM-Server Feature von Server a auf Server B verschieben):</span><span class="sxs-lookup"><span data-stu-id="1755b-111">You can use the following procedure to move the MBAM Recovery and Hardware Database from one computer to another (you can move this MBAM Server feature from Server A to Server B):</span></span>

****

1.  <span data-ttu-id="1755b-112">Beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="1755b-112">Stop all instances of the MBAM Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="1755b-113">Führen Sie das MBAM-Setup auf Server B aus.</span><span class="sxs-lookup"><span data-stu-id="1755b-113">Run the MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="1755b-114">Sichern Sie die MBAM-Wiederherstellungs-und-Hardware Datenbank auf Server A.</span><span class="sxs-lookup"><span data-stu-id="1755b-114">Back up the MBAM Recovery and Hardware database on Server A.</span></span>

4.  <span data-ttu-id="1755b-115">MBAM Recovery and Hardware Database from Server A to B</span><span class="sxs-lookup"><span data-stu-id="1755b-115">MBAM Recovery and Hardware database from Server A to B</span></span>

5.  <span data-ttu-id="1755b-116">Wiederherstellen der MBAM-Wiederherstellungs-und-Hardware Datenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-116">Restore the MBAM Recovery and Hardware database on Server B</span></span>

6.  <span data-ttu-id="1755b-117">Konfigurieren des Zugriffs auf die MBAM-Wiederherstellungs-und-Hardware Datenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-117">Configure the access to the MBAM Recovery and Hardware database on Server B</span></span>

7.  <span data-ttu-id="1755b-118">Aktualisieren der Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern</span><span class="sxs-lookup"><span data-stu-id="1755b-118">Update the database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="1755b-119">Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="1755b-119">Resume all instances of the MBAM Administration and Monitoring web site</span></span>

**<span data-ttu-id="1755b-120">So beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="1755b-120">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="1755b-121">Verwenden Sie die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website auf jedem Server zu beenden, auf dem das Feature für die Verwaltung und Überwachung von MBAM ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1755b-121">Use the Internet Information Services (IIS) Manager console to stop the MBAM website on each of the servers that run the MBAM Administration and Monitoring feature.</span></span> <span data-ttu-id="1755b-122">Die MBAM-Website hat den Namen **Microsoft BitLocker-Verwaltung und-Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="1755b-122">The MBAM website is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="1755b-123">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl an der Eingabeaufforderung verwenden, die mit der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-123">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="1755b-124">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-124">Note</span></span>**  
    <span data-ttu-id="1755b-125">Um diese PowerShell-Eingabeaufforderung ausführen zu können, müssen Sie das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1755b-125">To run this PowerShell command prompt, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="1755b-126">Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, um die Ausführung von Skripts zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1755b-126">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="1755b-127">So führen Sie das MBAM-Setup auf Server B aus</span><span class="sxs-lookup"><span data-stu-id="1755b-127">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="1755b-128">Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie die Wiederherstellungs-und Hardware Datenbank für die Installation aus.</span><span class="sxs-lookup"><span data-stu-id="1755b-128">Run the MBAM setup on Server B and select the Recovery and Hardware Database for installation.</span></span>

2.  <span data-ttu-id="1755b-129">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl an der Eingabeaufforderung verwenden, die mit der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-129">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="1755b-130">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-130">Note</span></span>**  
    <span data-ttu-id="1755b-131">Ersetzen Sie die folgenden Werte im obigen Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-131">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-132">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und der Instanz ein, auf die die Wiederherstellungs-und Hardware Datenbank verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="1755b-132">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery and Hardware database will be moved.</span></span>

    -   <span data-ttu-id="1755b-133">$Domain $ \ \ $Servername $ – Geben Sie die Domänen-und Servernamen jeder MBAM-Anwendung und des Überwachungsservers ein, die sich mit der Wiederherstellungs-und Hardware Datenbank in Verbindung setzen.</span><span class="sxs-lookup"><span data-stu-id="1755b-133">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Application and Monitoring Server that will contact the Recovery and Hardware database.</span></span> <span data-ttu-id="1755b-134">Wenn mehrere Domänen-und Servernamen vorhanden sind, verwenden Sie ein Semikolon, um die einzelnen Namen in der Liste zu trennen.</span><span class="sxs-lookup"><span data-stu-id="1755b-134">If there are multiple domain and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="1755b-135">Beispiel: $Domain \\Servername $; $Domain \ \ $Servername $ $.</span><span class="sxs-lookup"><span data-stu-id="1755b-135">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="1755b-136">Darüber hinaus muss jeder Servername von a gefolgt werden **$** .</span><span class="sxs-lookup"><span data-stu-id="1755b-136">Additionally, each server name must be followed by a **$**.</span></span> <span data-ttu-id="1755b-137">Beispiel: MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="1755b-137">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>



**<span data-ttu-id="1755b-138">So sichern Sie die Datenbank auf Server A</span><span class="sxs-lookup"><span data-stu-id="1755b-138">To back up the Database on Server A</span></span>**

1.  <span data-ttu-id="1755b-139">Wenn Sie die Wiederherstellungs-und Hardware Datenbank auf Server A sichern möchten, verwenden Sie SQL Server Management Studio und die Aufgabe mit dem Namen **sichern.**..</span><span class="sxs-lookup"><span data-stu-id="1755b-139">To back up the Recovery and Hardware database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="1755b-140">Standardmäßig ist der Datenbankname **MBAM-Wiederherstellungs-und-Hardware Datenbank**.</span><span class="sxs-lookup"><span data-stu-id="1755b-140">By default, the database name is **MBAM Recovery and Hardware Database**.</span></span>

2.  <span data-ttu-id="1755b-141">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="1755b-141">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="1755b-142">Ändern Sie die MBAM-Wiederherstellungs-und Hardware Datenbank, um den vollständigen Wiederherstellungsmodus zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1755b-142">Modify the MBAM Recovery and Hardware Database to use the full recovery mode.</span></span>

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    <span data-ttu-id="1755b-143">Erstellen Sie MBAM-Wiederherstellungs-und Hardware Datenbank-und MBAM-Wiederherstellungs-logische Sicherungsmedien.</span><span class="sxs-lookup"><span data-stu-id="1755b-143">Create MBAM Recovery and Hardware Database Data and MBAM Recovery logical backup devices.</span></span>

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    <span data-ttu-id="1755b-144">Sichern Sie die vollständige MBAM-Wiederherstellungs-und-Hardware Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1755b-144">Back up the full MBAM Recovery and Hardware database.</span></span>

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

    **<span data-ttu-id="1755b-145">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-145">Note</span></span>**  
    <span data-ttu-id="1755b-146">Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-146">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-147">$Password $ – geben Sie ein Kennwort ein, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="1755b-147">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="1755b-148">Führen Sie die SQL-Datei mithilfe von SQL Server PowerShell und einem Befehl aus, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-148">Execute the SQL file by using SQL Server PowerShell and a command that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="1755b-149">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-149">Note</span></span>**  
    <span data-ttu-id="1755b-150">Ersetzen Sie den Wert im vorherigen Beispiel durch die Werte, die mit Ihrer Umgebung übereinstimmen:</span><span class="sxs-lookup"><span data-stu-id="1755b-150">Replace the value in the previous example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-151">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und die Instanz ein, von der Sie die Wiederherstellungs-und Hardware Datenbank sichern.</span><span class="sxs-lookup"><span data-stu-id="1755b-151">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance from which you back up the Recovery and Hardware database.</span></span>



**<span data-ttu-id="1755b-152">So verschieben Sie die Datenbank und das Zertifikat von Server A nach B</span><span class="sxs-lookup"><span data-stu-id="1755b-152">To move the Database and Certificate from Server A to B</span></span>**

1.  <span data-ttu-id="1755b-153">Verschieben Sie die MBAM-Wiederherstellungs-und Hardware-Datenbankdaten. bak von Server A auf Server B mithilfe von Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="1755b-153">Move the MBAM Recovery and Hardware database data.bak from Server A to Server B by using Windows Explorer.</span></span>

2.  <span data-ttu-id="1755b-154">Um das Zertifikat für die verschlüsselte Datenbank zu verschieben, müssen Sie die folgenden Automatisierungsschritte verwenden.</span><span class="sxs-lookup"><span data-stu-id="1755b-154">To move the certificate for the encrypted database, you will need to use the following automation steps.</span></span> <span data-ttu-id="1755b-155">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-155">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="1755b-156">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-156">Note</span></span>**  
    <span data-ttu-id="1755b-157">Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-157">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-158">$Servername $ – Geben Sie den Namen des Servers ein, auf den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1755b-158">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="1755b-159">$DESTINATIONSHARE $ – geben Sie den Namen der Freigabe und den Pfad ein, in den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1755b-159">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="1755b-160">So stellen Sie die Datenbank auf Server B wieder her</span><span class="sxs-lookup"><span data-stu-id="1755b-160">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="1755b-161">Stellen Sie die Wiederherstellungs-und Hardware Datenbank auf Server B mithilfe von SQL Server Management Studio und der Aufgabe mit dem Namen **Restore Database**wieder her.</span><span class="sxs-lookup"><span data-stu-id="1755b-161">Restore the Recovery and Hardware database on Server B by using the SQL Server Management Studio and the Task named **Restore Database**.</span></span>

2.  <span data-ttu-id="1755b-162">Nachdem die Aufgabe ausgeführt wurde, wählen Sie die Datenbanksicherungsdatei aus, indem Sie die Option **vom Gerät** auswählen, und verwenden Sie dann den Befehl **Hinzufügen** , um die Datei MBAM Recovery and Hardware Database **Data. bak** auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1755b-162">Once the task has been executed, choose the database backup file by selecting the **From Device** option, and then use the **Add** command to choose the MBAM Recovery and Hardware database **Data.bak** file.</span></span>

3.  <span data-ttu-id="1755b-163">Wählen Sie **OK** aus, um den Wiederherstellungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1755b-163">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="1755b-164">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="1755b-164">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    <span data-ttu-id="1755b-165">Legen Sie das vom MBAM-Setup erstellte Zertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="1755b-165">Drop the certificate created by MBAM Setup.</span></span>

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    <span data-ttu-id="1755b-166">Zertifikat hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1755b-166">Add certificate</span></span>

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

    <span data-ttu-id="1755b-167">Wiederherstellen der MBAM-Wiederherstellungs-und Hardware-Datenbankdaten und der Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="1755b-167">Restore the MBAM Recovery and Hardware database data and the log files.</span></span>

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **<span data-ttu-id="1755b-168">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-168">Note</span></span>**  
    <span data-ttu-id="1755b-169">Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-169">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-170">$Password $ – geben Sie das Kennwort ein, das Sie zum Verschlüsseln der privaten Schlüsseldatei verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="1755b-170">$PASSWORD$ - Enter the password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="1755b-171">Verwenden Sie Windows PowerShell, um eine Befehlszeile einzugeben, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-171">Use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="1755b-172">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-172">Note</span></span>**  
    <span data-ttu-id="1755b-173">Ersetzen Sie den Wert aus dem Beispiel für den Rückzug durch die Werte, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-173">Replace the value from the receding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-174">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Namen des Servers und die Instanz ein, auf die die Wiederherstellungs-und Hardware Datenbank wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1755b-174">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance to which the Recovery and Hardware Database will be restored.</span></span>



**<span data-ttu-id="1755b-175">Konfigurieren des Zugriffs auf die Datenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-175">Configure the access to the Database on Server B</span></span>**

1.  <span data-ttu-id="1755b-176">Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, der lokalen Gruppe " **MBAM Recovery and Hardware DB Access**" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1755b-176">On Server B, use the Local user and Groups snap-in from Server Manager, to add the computer accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="1755b-177">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell auf Server B verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-177">To automate this procedure, you can use Windows PowerShell on Server B to enter a command that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="1755b-178">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-178">Note</span></span>**  
    <span data-ttu-id="1755b-179">Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch die anwendbaren Werte für Ihre Umgebung:</span><span class="sxs-lookup"><span data-stu-id="1755b-179">Replace the values from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="1755b-180">$Domain $ \ \ $Servername $ $ – Geben Sie den Domänennamen und den Computernamen des MBAM-Verwaltungs-und-Überwachungsservers ein.</span><span class="sxs-lookup"><span data-stu-id="1755b-180">$DOMAIN$\\$SERVERNAME$$ - Enter the domain name and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="1755b-181">Auf den Servernamen muss ein, Beispiels **$** Weise MyDomain\\MyServerName1 $, folgen.</span><span class="sxs-lookup"><span data-stu-id="1755b-181">The server name must be followed by a **$**, for example, MyDomain\\MyServerName1$.</span></span>



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="1755b-182">So aktualisieren Sie die Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern</span><span class="sxs-lookup"><span data-stu-id="1755b-182">To update the Database Connection data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="1755b-183">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die IIS-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die folgenden Anwendungen zu aktualisieren, die auf der Website Microsoft BitLocker-Verwaltung und-Überwachung gehostet werden:</span><span class="sxs-lookup"><span data-stu-id="1755b-183">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="1755b-184">MBAM-Verwaltungsdienst</span><span class="sxs-lookup"><span data-stu-id="1755b-184">MBAM Administration Service</span></span>

   -   <span data-ttu-id="1755b-185">MBAM-Wiederherstellungs-und Hardware Dienst</span><span class="sxs-lookup"><span data-stu-id="1755b-185">MBAM Recovery And Hardware Service</span></span>

2. <span data-ttu-id="1755b-186">Wählen Sie jede Anwendung aus, und verwenden Sie das Feature " **Konfigurations-Editor** ", das sich unter dem Abschnitt " **Verwaltung** " der **Funktionsansicht**befindet.</span><span class="sxs-lookup"><span data-stu-id="1755b-186">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="1755b-187">Wählen Sie die Option **configurationStrings** im Steuerelement Abschnittsliste aus.</span><span class="sxs-lookup"><span data-stu-id="1755b-187">Select the **configurationStrings** option from the Section list control.</span></span>

4. <span data-ttu-id="1755b-188">Wählen Sie die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den **Sammlungs-Editor** , indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.</span><span class="sxs-lookup"><span data-stu-id="1755b-188">Choose the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="1755b-189">Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen **KeyRecoveryConnectionString** aus, wenn Sie die Konfiguration für die Anwendung "MBAMAdministrationService" aktualisiert haben, oder wählen Sie die Zeile mit dem Namen " <strong> Microsoft. mbam. RecoveryAndHardwareDataStore" aus. </strong> ConnectionString beim Aktualisieren der Konfiguration für das "MBAMRecoveryAndHardwareService".</span><span class="sxs-lookup"><span data-stu-id="1755b-189">In the **Collection Editor**, choose the row named **KeyRecoveryConnectionString** when you updated the configuration for the ‘MBAMAdministrationService’ application, or choose the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString, when updating the configuration for the ‘MBAMRecoveryAndHardwareService’.</span></span>

6. <span data-ttu-id="1755b-190">Aktualisieren Sie die **Datenquelle =** Wert für die **configurationStrings** -Eigenschaft, um den Servernamen und die Instanz aufzulisten, in die die Wiederherstellungs-und Hardware Datenbank verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="1755b-190">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance where the Recovery and Hardware Database was moved to.</span></span> <span data-ttu-id="1755b-191">Beispiel: $Servername $ \ \ $SQLInstanceName $.</span><span class="sxs-lookup"><span data-stu-id="1755b-191">For example, $SERVERNAME$\\$SQLINSTANCENAME$.</span></span>

7. <span data-ttu-id="1755b-192">Um dieses Verfahren zu automatisieren, können Sie einen Befehl verwenden, der mit dem folgenden vergleichbar ist, indem Sie Windows PowerShell auf den einzelnen Verwaltungs-und Überwachungs Servern verwenden:</span><span class="sxs-lookup"><span data-stu-id="1755b-192">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="1755b-193">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-193">Note</span></span>**  
   <span data-ttu-id="1755b-194">Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-194">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="1755b-195">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der sich die Wiederherstellungs-und Hardware Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="1755b-195">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery and Hardware database is.</span></span>



**<span data-ttu-id="1755b-196">So setzen Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website fort</span><span class="sxs-lookup"><span data-stu-id="1755b-196">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="1755b-197">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.</span><span class="sxs-lookup"><span data-stu-id="1755b-197">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="1755b-198">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-198">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="1755b-199">So verschieben Sie das Feature "Kompatibilitäts Status Datenbank"</span><span class="sxs-lookup"><span data-stu-id="1755b-199">To move the Compliance Status Database feature</span></span>


<span data-ttu-id="1755b-200">Wenn Sie sich entscheiden, das Feature MBAM-Konformitäts Status-Datenbank von einem Computer auf einen anderen zu verschieben, beispielsweise von Server a auf Server B, sollten Sie das folgende Verfahren verwenden:</span><span class="sxs-lookup"><span data-stu-id="1755b-200">If you choose to move the MBAM Compliance Status Database feature from one computer to another, such as from Server A to Server B, you should use the following procedure:</span></span>

1.  <span data-ttu-id="1755b-201">Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="1755b-201">Stop all instances of the MBAM Administration and Monitoring website</span></span>

2.  <span data-ttu-id="1755b-202">Ausführen des MBAM-Setups auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-202">Run MBAM setup on Server B</span></span>

3.  <span data-ttu-id="1755b-203">Sichern der Datenbank auf Server A</span><span class="sxs-lookup"><span data-stu-id="1755b-203">Backup the Database on Server A</span></span>

4.  <span data-ttu-id="1755b-204">Verschieben der Datenbank von Server A nach B</span><span class="sxs-lookup"><span data-stu-id="1755b-204">Move the Database from Server A to B</span></span>

5.  <span data-ttu-id="1755b-205">Wiederherstellen der Datenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-205">Restore the Database on Server B</span></span>

6.  <span data-ttu-id="1755b-206">Konfigurieren des Zugriffs auf die Datenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-206">Configure Access to the Database on Server B</span></span>

7.  <span data-ttu-id="1755b-207">Aktualisieren von Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern</span><span class="sxs-lookup"><span data-stu-id="1755b-207">Update database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="1755b-208">Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="1755b-208">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="1755b-209">So beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="1755b-209">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="1755b-210">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu beenden.</span><span class="sxs-lookup"><span data-stu-id="1755b-210">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="1755b-211">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-211">To automate this procedure, you can use a command that is similar to the following one,by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="1755b-212">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-212">Note</span></span>**  
    <span data-ttu-id="1755b-213">Zum Ausführen dieses Befehls müssen Sie das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1755b-213">To execute this command, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="1755b-214">Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, um die Ausführung von Skripts zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1755b-214">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="1755b-215">So führen Sie das MBAM-Setup auf Server B aus</span><span class="sxs-lookup"><span data-stu-id="1755b-215">To run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="1755b-216">Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie das Feature Kompatibilitäts Status-Datenbank für die Installation aus.</span><span class="sxs-lookup"><span data-stu-id="1755b-216">Run MBAM Setup on Server B and select the Compliance Status Database feature for installation.</span></span>

2.  <span data-ttu-id="1755b-217">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-217">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **<span data-ttu-id="1755b-218">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-218">Note</span></span>**  
    <span data-ttu-id="1755b-219">Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-219">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-220">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in die die Kompatibilitäts Status Datenbank verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="1755b-220">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be moved to.</span></span>

    -   <span data-ttu-id="1755b-221">$Domain $ \ \ $Servername $ – Geben Sie die Domänennamen und Servernamen jeder MBAM-Anwendung und des Überwachungsservers ein, die sich an die Kompatibilitäts Status Datenbank wenden.</span><span class="sxs-lookup"><span data-stu-id="1755b-221">$DOMAIN$\\$SERVERNAME$ - Enter the domain names and server names of each MBAM Application and Monitoring Server that will contact the Compliance Status Database.</span></span> <span data-ttu-id="1755b-222">Wenn mehrere Domänennamen und Servernamen vorhanden sind, verwenden Sie ein Semikolon, um die einzelnen Namen in der Liste zu trennen.</span><span class="sxs-lookup"><span data-stu-id="1755b-222">If there are multiple domain names and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="1755b-223">Beispiel: $Domain \\Servername $; $Domain \ \ $Servername $ $.</span><span class="sxs-lookup"><span data-stu-id="1755b-223">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="1755b-224">Auf jeden Servernamen muss a folgen **$** , wie im Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1755b-224">Each server name must be followed by a **$** as shown in the example.</span></span> <span data-ttu-id="1755b-225">Beispiel: MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="1755b-225">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>

    -   <span data-ttu-id="1755b-226">$Domain $ \ \ $username $ – geben Sie die Domäne und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Kompatibilitäts Status Datenbank herzustellen.</span><span class="sxs-lookup"><span data-stu-id="1755b-226">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="1755b-227">So sichern Sie die Kompatibilitätsdatenbank auf Server A</span><span class="sxs-lookup"><span data-stu-id="1755b-227">To back up the Compliance Database on Server A</span></span>**

1.  <span data-ttu-id="1755b-228">Wenn Sie die Kompatibilitätsdatenbank auf Server A sichern möchten, verwenden Sie SQL Server Management Studio und die Aufgabe mit dem Namen **sichern.**..</span><span class="sxs-lookup"><span data-stu-id="1755b-228">To back up the Compliance Database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="1755b-229">Standardmäßig lautet der Datenbankname **MBAM-Kompatibilitäts Status-Datenbank**.</span><span class="sxs-lookup"><span data-stu-id="1755b-229">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="1755b-230">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="1755b-230">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="1755b-231">Führen Sie die SQL-Datei mit einem Befehl aus, der der folgenden ähnelt, indem Sie die SQL Server-PowerShell verwenden:</span><span class="sxs-lookup"><span data-stu-id="1755b-231">Run the SQL file with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="1755b-232">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-232">Note</span></span>**  
    <span data-ttu-id="1755b-233">Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-233">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-234">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, aus der die Datenbank des Kompatibilitäts Status gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1755b-234">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and the instance from where the Compliance Status database will be backed up.</span></span>



**<span data-ttu-id="1755b-235">So verschieben Sie die Datenbank von Server A nach B</span><span class="sxs-lookup"><span data-stu-id="1755b-235">To move the Database from Server A to B</span></span>**

1.  <span data-ttu-id="1755b-236">Verschieben Sie die folgenden Dateien von Server a auf Server B mithilfe von Windows-Explorer:</span><span class="sxs-lookup"><span data-stu-id="1755b-236">Move the following files from Server A to Server B, by using Windows Explorer:</span></span>

    -   <span data-ttu-id="1755b-237">MBAM-Kompatibilitäts Status-Datenbankdaten. bak</span><span class="sxs-lookup"><span data-stu-id="1755b-237">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="1755b-238">Um dieses Verfahren zu automatisieren, können Sie einen Befehl verwenden, der mit Windows PowerShell ähnlich wie der folgende ist:</span><span class="sxs-lookup"><span data-stu-id="1755b-238">To automate this procedure, you can use a command that is similar to the following using Windows PowerShell:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="1755b-239">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-239">Note</span></span>**  
    <span data-ttu-id="1755b-240">Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-240">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-241">$Servername $ – Geben Sie den Servernamen ein, in den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1755b-241">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="1755b-242">$DESTINATIONSHARE $ – geben Sie den Namen der Freigabe und des Pfads ein, in den die Dateien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1755b-242">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="1755b-243">So stellen Sie die Datenbank auf Server B wieder her</span><span class="sxs-lookup"><span data-stu-id="1755b-243">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="1755b-244">Wiederherstellen der Kompatibilitäts Status Datenbank auf Server B mithilfe von SQL Server Management Studio und der Aufgabe mit dem Namen **Restore Database.**...</span><span class="sxs-lookup"><span data-stu-id="1755b-244">Restore the Compliance Status database on Server B by using SQL Server Management Studio and the Task named **Restore Database…**.</span></span>

2.  <span data-ttu-id="1755b-245">Nachdem die Aufgabe ausgeführt wurde, wählen Sie die Datenbanksicherungsdatei aus, indem Sie die Option vom Gerät auswählen, und verwenden Sie dann den Befehl hinzufügen, um die Datei MBAM Compliance Status Database Data. bak auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1755b-245">Once the task is executed, select the database backup file, by selecting the From Device option, and then use the Add command to choose the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="1755b-246">Klicken Sie auf OK, um den Wiederherstellungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1755b-246">Click OK to complete the restoration process.</span></span>

3.  <span data-ttu-id="1755b-247">Wenn Sie dieses Verfahren automatisieren möchten, erstellen Sie eine SQL-Datei (SQL), die das folgende SQL-Skript enthält:</span><span class="sxs-lookup"><span data-stu-id="1755b-247">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="1755b-248">Führen Sie die SQL-Datei mit einem Befehl aus, der der folgenden ähnelt, indem Sie die SQL Server-PowerShell verwenden:</span><span class="sxs-lookup"><span data-stu-id="1755b-248">Run the SQL File with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="1755b-249">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-249">Note</span></span>**  
    <span data-ttu-id="1755b-250">Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-250">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-251">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der die Kompatibilitäts Status Datenbank wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1755b-251">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be restored to.</span></span>



**<span data-ttu-id="1755b-252">So konfigurieren Sie den Zugriff auf die Datenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-252">To configure the Access to the Database on Server B</span></span>**

1.  <span data-ttu-id="1755b-253">Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server hinzuzufügen, der das Feature MBAM-Verwaltung und-Überwachung ausführt, in der lokalen Gruppe mit dem Namen **MBAM-Konformitäts Status DB Access**.</span><span class="sxs-lookup"><span data-stu-id="1755b-253">On Server B use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="1755b-254">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell auf Server B einen Befehl verwenden, der dem folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-254">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on Server B:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="1755b-255">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-255">Note</span></span>**  
    <span data-ttu-id="1755b-256">Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die anwendbaren Werte für Ihre Umgebung:</span><span class="sxs-lookup"><span data-stu-id="1755b-256">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="1755b-257">$Domain $ \ \ $Servername $ $ – Geben Sie den Namen der Domäne und des Computers des MBAM-Verwaltungs-und-Überwachungsservers ein.</span><span class="sxs-lookup"><span data-stu-id="1755b-257">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="1755b-258">Auf den Servernamen muss ein folgen **$** . Beispiel: MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="1755b-258">The server name must be followed by a **$**.For example, MyDomain\\MyServerName1$.</span></span>

    -   <span data-ttu-id="1755b-259">$Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1755b-259">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**<span data-ttu-id="1755b-260">So aktualisieren Sie die Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern</span><span class="sxs-lookup"><span data-stu-id="1755b-260">To update the database connection data on MBAM Administration and Monitoring servers</span></span>**

1.  <span data-ttu-id="1755b-261">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die IIS-Manager-Konsole, um die Verbindungszeichenfolgen-Informationen für die folgenden Anwendungen zu aktualisieren, die auf der Website Microsoft BitLocker-Verwaltung und-Überwachung gehostet werden:</span><span class="sxs-lookup"><span data-stu-id="1755b-261">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following Applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="1755b-262">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="1755b-262">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="1755b-263">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="1755b-263">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="1755b-264">Wählen Sie jede Anwendung aus, und verwenden Sie das Feature " **Konfigurations-Editor** ", das sich unter dem Abschnitt " **Verwaltung** " der **Funktionsansicht**befindet.</span><span class="sxs-lookup"><span data-stu-id="1755b-264">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="1755b-265">Wählen Sie die Option **configurationStrings** im Steuerelement Abschnittsliste aus.</span><span class="sxs-lookup"><span data-stu-id="1755b-265">Select the **configurationStrings** option from the Section list control.</span></span>

4.  <span data-ttu-id="1755b-266">Wählen Sie die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den Sammlungs-Editor, indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.</span><span class="sxs-lookup"><span data-stu-id="1755b-266">Select the row named **(Collection)**, and open the Collection Editor by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="1755b-267">Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen **ComplianceStatusConnectionString**aus, wenn Sie die Konfiguration für die MBAMAdministrationService-Anwendung aktualisieren, oder die Zeile mit dem Namen **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, wenn Sie die Konfiguration für die MBAMComplianceStatusService aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1755b-267">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString**, when you update the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString**, when you update the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="1755b-268">Aktualisieren Sie die **Datenquelle =** Wert für die **configurationStrings** -Eigenschaft, um den Servernamen und den Instanzennamen aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="1755b-268">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance name.</span></span> <span data-ttu-id="1755b-269">Beispiel: $Servername $ \ \ $SqlInstanceName, auf die die Wiederherstellungs-und Hardware Datenbank verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="1755b-269">For example, $SERVERNAME$\\$SQLINSTANCENAME, to which the Recovery and Hardware Database was moved.</span></span>

7.  <span data-ttu-id="1755b-270">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl eingeben, der auf den einzelnen Verwaltungs-und Überwachungs Servern mit dem folgenden vergleichbar ist:</span><span class="sxs-lookup"><span data-stu-id="1755b-270">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="1755b-271">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-271">Note</span></span>**  
    <span data-ttu-id="1755b-272">Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-272">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-273">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und den Instanznamen ein, in dem sich die Wiederherstellungs-und Hardware Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="1755b-273">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance name where the Recovery and Hardware Database is located.</span></span>



**<span data-ttu-id="1755b-274">So setzen Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website fort</span><span class="sxs-lookup"><span data-stu-id="1755b-274">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="1755b-275">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.</span><span class="sxs-lookup"><span data-stu-id="1755b-275">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="1755b-276">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-276">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    **<span data-ttu-id="1755b-277">PS C:\\ &gt; Start-Website "Microsoft BitLocker-Verwaltung und-Überwachung"</span><span class="sxs-lookup"><span data-stu-id="1755b-277">PS C:\\&gt; Start-Website “Microsoft BitLocker Administration and Monitoring”</span></span>**

## <span data-ttu-id="1755b-278">So verschieben Sie die Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="1755b-278">To moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="1755b-279">Wenn Sie die MBAM-Konformitäts-und Überwachungsberichte von einem Computer auf einen anderen verschieben möchten (insbesondere, wenn Sie das Feature von Server a auf Server B verschieben), sollten Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="1755b-279">If you choose to move the MBAM Compliance and Audit Reports from one computer to another (specifically, if you move feature from Server A to Server B), you should use the following procedure and steps:</span></span>

1.  <span data-ttu-id="1755b-280">Ausführen des MBAM-Setups auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-280">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="1755b-281">Konfigurieren des Zugriffs auf die Konformitäts-und Überwachungsberichte auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-281">Configure Access to the Compliance and Audit Reports on Server B</span></span>

3.  <span data-ttu-id="1755b-282">Beenden aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="1755b-282">Stop all instances of the MBAM Administration and Monitoring website</span></span>

4.  <span data-ttu-id="1755b-283">Aktualisieren der Verbindungsdaten für Berichte auf MBAM-Verwaltungs-und-Überwachungs Servern</span><span class="sxs-lookup"><span data-stu-id="1755b-283">Update the reports connection data on MBAM Administration and Monitoring servers</span></span>

5.  <span data-ttu-id="1755b-284">Fortsetzen aller Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="1755b-284">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="1755b-285">So führen Sie das MBAM-Setup auf Server B aus</span><span class="sxs-lookup"><span data-stu-id="1755b-285">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="1755b-286">Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie nur das Feature Compliance und Überwachung für die Installation aus.</span><span class="sxs-lookup"><span data-stu-id="1755b-286">Run MBAM setup on Server B and only select the Compliance and Audit feature for installation.</span></span>

2.  <span data-ttu-id="1755b-287">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen ähnlichen Befehl wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="1755b-287">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **<span data-ttu-id="1755b-288">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-288">Note</span></span>**  
    <span data-ttu-id="1755b-289">Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-289">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-290">$Servername $ \ \ $SqlInstanceName $ – geben Sie den Servernamen und die Instanz ein, in der sich die Kompatibilitäts Status Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="1755b-290">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database is located.</span></span>

    -   <span data-ttu-id="1755b-291">$Domain $ \ \ $username $ – geben Sie den Domänennamen und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Kompatibilitäts Status Datenbank herzustellen.</span><span class="sxs-lookup"><span data-stu-id="1755b-291">$DOMAIN$\\$USERNAME$ - Enter the domain name and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="1755b-292">$Password $ – geben Sie das Kennwort für das Benutzerkonto ein, das zum Herstellen einer Verbindung mit der Kompatibilitäts Status Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1755b-292">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="1755b-293">So konfigurieren Sie den Zugriff auf die Konformitäts-und Überwachungsberichte auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-293">To configure the access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="1755b-294">Verwenden Sie auf Server B das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Benutzerkonten hinzuzufügen, die Zugriff auf die Konformitäts-und Überwachungsberichte erhalten.</span><span class="sxs-lookup"><span data-stu-id="1755b-294">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="1755b-295">Fügen Sie die Benutzerkonten der lokalen Gruppe mit dem Namen "MBAM-Berichtsbenutzer" hinzu.</span><span class="sxs-lookup"><span data-stu-id="1755b-295">Add the user accounts to the local group named “MBAM Report Users”.</span></span>

2.  <span data-ttu-id="1755b-296">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell auf Server B einen ähnlichen Befehl wie den folgenden verwenden.</span><span class="sxs-lookup"><span data-stu-id="1755b-296">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell on Server B.</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="1755b-297">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-297">Note</span></span>**  
    <span data-ttu-id="1755b-298">Ersetzen Sie den folgenden Wert aus dem vorhergehenden Beispiel durch die anwendbaren Werte für Ihre Umgebung:</span><span class="sxs-lookup"><span data-stu-id="1755b-298">Replace the following value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="1755b-299">$Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1755b-299">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="1755b-300">So beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="1755b-300">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="1755b-301">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internet Informationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu beenden.</span><span class="sxs-lookup"><span data-stu-id="1755b-301">On each of the servers that run the MBAM Administration and Monitoring Feature use the Internet Information Services (IIS) Manager console to Stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="1755b-302">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-302">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="1755b-303">So aktualisieren Sie die Datenbankverbindungsdaten auf MBAM-Verwaltungs-und-Überwachungs Servern</span><span class="sxs-lookup"><span data-stu-id="1755b-303">To update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="1755b-304">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die URL für die Konformitätsberichte mithilfe der Internet Informationsdienste (IIS)-Manager-Konsole.</span><span class="sxs-lookup"><span data-stu-id="1755b-304">On each of the servers that run the MBAM Administration and Monitoring Feature, use the Internet Information Services (IIS) Manager console to update the Compliance Reports URL.</span></span>

2. <span data-ttu-id="1755b-305">Wählen Sie die Website **Microsoft BitLocker-Verwaltung und-Überwachung** aus, und verwenden Sie das Feature **Konfigurations-Editor** , das unter dem Abschnitt **Verwaltung** der **Featureansicht**zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="1755b-305">Select the **Microsoft BitLocker Administration and Monitoring** website and use the **Configuration Editor** feature which can be found under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="1755b-306">Wählen Sie die Option **appSettings** im Steuerelement Abschnittsliste aus.</span><span class="sxs-lookup"><span data-stu-id="1755b-306">Select the **appSettings** option from the Section list control.</span></span>

4. <span data-ttu-id="1755b-307">Wählen Sie hier die Zeile mit dem Namen **(Sammlung)** aus, und öffnen Sie den **Sammlungs-Editor** , indem Sie die Schaltfläche auf der rechten Seite der Zeile auswählen.</span><span class="sxs-lookup"><span data-stu-id="1755b-307">From here, select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="1755b-308">Wählen Sie im **Sammlungs-Editor**die Zeile mit dem Namen "Microsoft. mbam. Reports. URL" aus.</span><span class="sxs-lookup"><span data-stu-id="1755b-308">In the **Collection Editor**, select the row named “Microsoft.Mbam.Reports.Url”.</span></span>

6. <span data-ttu-id="1755b-309">Aktualisieren Sie den Wert für Microsoft. mbam. Reports. URL, um den Servernamen für Server B anzugeben. Wenn das Feature Konformitäts-und Überwachungsberichte auf einer benannten SQL Reporting Services-Instanz installiert wurde, stellen Sie sicher, dass Sie den Namen der Instanz zur URL hinzufügen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1755b-309">Update the value for Microsoft.Mbam.Reports.Url to reflect the server name for Server B. If the Compliance and Audit reports feature was installed on a named SQL Reporting Services instance, make sure that you add or update the name of the instance to the URL.</span></span> <span data-ttu-id="1755b-310">Beispiel: http://$Servername $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....</span><span class="sxs-lookup"><span data-stu-id="1755b-310">For example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....</span></span>

7. <span data-ttu-id="1755b-311">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl eingeben, der auf den einzelnen Verwaltungs-und Überwachungs Servern mit dem folgenden vergleichbar ist:</span><span class="sxs-lookup"><span data-stu-id="1755b-311">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **<span data-ttu-id="1755b-312">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-312">Note</span></span>**  
   <span data-ttu-id="1755b-313">Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die Werte, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-313">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="1755b-314">$Servername $ – Geben Sie den Namen des Servers ein, auf dem die Konformitäts-und Überwachungsberichte installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1755b-314">$SERVERNAME$ - Enter the name of the server to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="1755b-315">$SRSINSTANCENAME $ – geben Sie den Namen der SQL Reporting Services-Instanz ein, auf die die Kompatibilitäts-und Überwachungsberichte installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1755b-315">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="1755b-316">So setzen Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website fort</span><span class="sxs-lookup"><span data-stu-id="1755b-316">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="1755b-317">Verwenden Sie auf jedem Server, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die MBAM-Website mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung**zu starten.</span><span class="sxs-lookup"><span data-stu-id="1755b-317">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="1755b-318">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-318">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="1755b-319">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-319">Note</span></span>**  
    <span data-ttu-id="1755b-320">Zum Ausführen dieses Befehls muss das IIS-Modul für PowerShell der aktuellen Instanz von PowerShell hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1755b-320">To execute this command, the IIS Module for PowerShell must be added to the current instance of PowerShell.</span></span> <span data-ttu-id="1755b-321">Darüber hinaus müssen Sie die PowerShell-Ausführungsrichtlinie aktualisieren, um die Ausführung von Skripts zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1755b-321">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



## <span data-ttu-id="1755b-322">So verschieben Sie das Feature "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="1755b-322">To move the Administration and Monitoring feature</span></span>


<span data-ttu-id="1755b-323">Wenn Sie das Feature MBAM-Verwaltungs-und Überwachungsberichte von einem Computer auf einen anderen verschieben möchten (wenn Sie das Feature von Server a auf Server B verschieben), sollten Sie das folgende Verfahren verwenden.</span><span class="sxs-lookup"><span data-stu-id="1755b-323">If you choose to move the MBAM Administration and Monitoring Reports feature from one computer to another, (if you move feature from Server A to Server B), you should use the following procedure.</span></span> <span data-ttu-id="1755b-324">Der Prozess umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="1755b-324">The process includes the following steps:</span></span>

1.  <span data-ttu-id="1755b-325">Ausführen des MBAM-Setups auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-325">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="1755b-326">Konfigurieren des Zugriffs auf die Datenbank auf Server B</span><span class="sxs-lookup"><span data-stu-id="1755b-326">Configure Access to the Database on Server B</span></span>

**<span data-ttu-id="1755b-327">So führen Sie das MBAM-Setup auf Server B aus</span><span class="sxs-lookup"><span data-stu-id="1755b-327">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="1755b-328">Führen Sie das MBAM-Setup auf Server B aus, und wählen Sie nur das Verwaltungsfeature für die Installation aus.</span><span class="sxs-lookup"><span data-stu-id="1755b-328">Run MBAM setup on Server B and only select the Administration feature for installation.</span></span>

2.  <span data-ttu-id="1755b-329">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl verwenden, der dem folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="1755b-329">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **<span data-ttu-id="1755b-330">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-330">Note</span></span>**  
    <span data-ttu-id="1755b-331">Ersetzen Sie die Werte aus dem vorhergehenden Beispiel durch diejenigen, die Ihrer Umgebung entsprechen:</span><span class="sxs-lookup"><span data-stu-id="1755b-331">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="1755b-332">$Servername $ \ \ $SqlInstanceName $ – geben Sie für den COMPLIDB \ _SQLINSTANCE-Parameter den Servernamen und die Instanz ein, in der sich die Kompatibilitäts Status Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="1755b-332">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, input the server name and instance where the Compliance Status Database is located.</span></span> <span data-ttu-id="1755b-333">Geben Sie für den RECOVERYANDHWDB \ _SQLINSTANCE-Parameter den Servernamen und die Instanz ein, in der sich die Wiederherstellungs-und Hardware Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="1755b-333">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, input the server name and instance where the Recovery and Hardware Database is located.</span></span>

    -   <span data-ttu-id="1755b-334">$Domain $ \ \ $username $ – geben Sie die Domäne und den Benutzernamen ein, die vom Feature Konformitäts-und Überwachungsberichte verwendet werden, um eine Verbindung mit der Kompatibilitäts Status Datenbank herzustellen.</span><span class="sxs-lookup"><span data-stu-id="1755b-334">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="1755b-335">$ REPORTSSERVERURL $ – geben Sie die URL für den Startspeicherort der SQL Reporting Service-Website ein.</span><span class="sxs-lookup"><span data-stu-id="1755b-335">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="1755b-336">Wenn die Berichte in einer Standard-SRS-Instanz installiert wurden, wird das URL-Format "http://$Servername $/ReportServer" formatiert.</span><span class="sxs-lookup"><span data-stu-id="1755b-336">If the reports were installed to a default SRS instance the URL format will formatted “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="1755b-337">Wenn die Berichte in einer Standard-SRS-Instanz installiert wurden, wird das URL-Format auf "http://$Servername $/ReportServer\_ $ SqlInstanceName $" formatiert.</span><span class="sxs-lookup"><span data-stu-id="1755b-337">If the reports were installed to a default SRS instance, the URL format will be formatted to “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>



**<span data-ttu-id="1755b-338">So konfigurieren Sie den Zugriff auf die Datenbanken</span><span class="sxs-lookup"><span data-stu-id="1755b-338">To configure the Access to the Databases</span></span>**

1.  <span data-ttu-id="1755b-339">Auf dem Server oder auf Servern, auf denen die Wiederherstellung und die Hardware und Konformitäts-und Überwachungsdatenbanken bereitgestellt werden, verwenden Sie das Snap-in lokale Benutzer und Gruppen aus dem Server-Manager, um die Computerkonten von jedem Server, auf dem die MBAM-Verwaltungs-und-Überwachungsfunktion ausgeführt wird, den lokalen Gruppen "MBAM Recovery and Hardware DB Access" (Recovery and Hardware DB Server) und "MBAM Compliance Status DB-Server" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1755b-339">On server or servers where the Recovery and Hardware, and Compliance and Audit databases are deployed, use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that run the MBAM Administration and Monitoring feature to the Local Groups named “MBAM Recovery and Hardware DB Access” (Recovery and Hardware DB Server) and “MBAM Compliance Status DB Access” (Compliance and Audit DB Server).</span></span>

2.  <span data-ttu-id="1755b-340">Um dieses Verfahren zu automatisieren, können Sie einen Befehl verwenden, der mit dem folgenden vergleichbar ist, indem Sie Windows PowerShell auf dem Server verwenden, auf dem die Kompatibilitäts-und Überwachungsdatenbanken bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="1755b-340">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on the server where the Compliance and Audit databases were deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  <span data-ttu-id="1755b-341">Führen Sie auf dem Server, auf dem die Wiederherstellungs-und Hardware Datenbanken bereitgestellt wurden, mithilfe von Windows PowerShell einen Befehl aus, der mit dem folgenden vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="1755b-341">On the server where the Recovery and Hardware databases were deployed, run a command that is similar to the following one, by using Windows PowerShell.</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="1755b-342">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1755b-342">Note</span></span>**  
    <span data-ttu-id="1755b-343">Ersetzen Sie den Wert aus dem vorhergehenden Beispiel durch die anwendbaren Werte für Ihre Umgebung:</span><span class="sxs-lookup"><span data-stu-id="1755b-343">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="1755b-344">$Domain $ \ \ $Servername $ $ – Geben Sie den Namen der Domäne und des Computers des MBAM-Verwaltungs-und-Überwachungsservers ein.</span><span class="sxs-lookup"><span data-stu-id="1755b-344">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="1755b-345">Auf den Servernamen muss ein folgen **$** .</span><span class="sxs-lookup"><span data-stu-id="1755b-345">The server name must be followed by a **$**.</span></span> <span data-ttu-id="1755b-346">Beispiel: MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="1755b-346">For example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="1755b-347">$Domain $ \ \ $REPORTSUSERNAME $ – geben Sie den Namen des Benutzerkontos ein, das zum Konfigurieren der Datenquelle für die Konformitäts-und Überwachungsberichte verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1755b-347">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="1755b-348">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1755b-348">Related topics</span></span>


[<span data-ttu-id="1755b-349">Verwalten von MBAM 1.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1755b-349">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)









