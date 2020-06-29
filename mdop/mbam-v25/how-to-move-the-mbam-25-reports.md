---
title: So verschieben Sie MBAM 2.5-Berichte
description: So verschieben Sie MBAM 2.5-Berichte
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804193"
---
# <span data-ttu-id="e84a0-103">So verschieben Sie MBAM 2.5-Berichte</span><span class="sxs-lookup"><span data-stu-id="e84a0-103">How to Move the MBAM 2.5 Reports</span></span>


<span data-ttu-id="e84a0-104">Verwenden Sie diese Verfahren, um das Berichtsfeature von einem Computer auf einen anderen zu verschieben, d. h., um das Berichtsfeature von Server a auf Server B zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="e84a0-104">Use these procedures to move the Reports feature from one computer to another, that is, to move the Reports feature from Server A to Server B.</span></span>

<span data-ttu-id="e84a0-105">Die allgemeinen Schritte zum Verschieben des Berichtsfeatures sind:</span><span class="sxs-lookup"><span data-stu-id="e84a0-105">The high-level steps for moving the Reports feature are:</span></span>

1.  <span data-ttu-id="e84a0-106">Beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="e84a0-106">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="e84a0-107">Installieren Sie die MBAM 2,5-Server Software auf Server b, und konfigurieren Sie das Feature Berichte auf Server b.</span><span class="sxs-lookup"><span data-stu-id="e84a0-107">Install the MBAM 2.5 Server software on Server B and configure the Reports feature on Server B.</span></span>

3.  <span data-ttu-id="e84a0-108">Aktualisieren Sie die Berichts Verbindungsdaten auf den MBAM-Verwaltungs-und-Überwachungs Servern.</span><span class="sxs-lookup"><span data-stu-id="e84a0-108">Update the reports connection data on the MBAM Administration and Monitoring servers.</span></span>

4.  <span data-ttu-id="e84a0-109">Setzen Sie die Instanz der MBAM-Verwaltungs-und-Überwachungs Website fort.</span><span class="sxs-lookup"><span data-stu-id="e84a0-109">Resume the instance of the MBAM Administration and Monitoring Website.</span></span>

<span data-ttu-id="e84a0-110">**Hinweis**  Wenn Sie die Beispiel-Windows PowerShell-Skripts in diesem Thema ausführen möchten, müssen Sie die Windows PowerShell-Ausführungsrichtlinie aktualisieren, damit Skripts ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="e84a0-110">**Note** To run the example Windows PowerShell scripts in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="e84a0-111">Anweisungen finden Sie unter [Ausführen von Windows PowerShell-Skripts](https://technet.microsoft.com/library/ee176949.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e84a0-111">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

 

**<span data-ttu-id="e84a0-112">Beenden der MBAM-Verwaltungs-und-Überwachungs Website</span><span class="sxs-lookup"><span data-stu-id="e84a0-112">Stop the MBAM Administration and Monitoring Website</span></span>**

-   <span data-ttu-id="e84a0-113">Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e84a0-113">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="e84a0-114">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="e84a0-114">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**<span data-ttu-id="e84a0-115">Installieren der MBAM-Server Software und Ausführen des MBAM-Serverkonfigurations-Assistenten auf Server B</span><span class="sxs-lookup"><span data-stu-id="e84a0-115">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>**

1.  <span data-ttu-id="e84a0-116">Installieren Sie die MBAM-Server Software auf Server B. Anweisungen hierzu finden Sie unter [Installieren der MBAM 2,5-Server Software](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="e84a0-116">Install the MBAM Server software on Server B. For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="e84a0-117">Starten Sie auf Server B den MBAM-Serverkonfigurations-Assistenten, klicken Sie auf **neue Features hinzufügen**, und wählen Sie dann nur das Feature **Berichte** aus.</span><span class="sxs-lookup"><span data-stu-id="e84a0-117">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Reports** feature.</span></span>

    <span data-ttu-id="e84a0-118">Alternativ können Sie das Windows PowerShell **-Cmdlet Enable-MbamReport** verwenden, um die Berichte zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e84a0-118">Alternatively, you can use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span>

    <span data-ttu-id="e84a0-119">Anweisungen zum Konfigurieren der Berichte finden Sie unter [Konfigurieren der MBAM 2,5-Berichte](how-to-configure-the-mbam-25-reports.md).</span><span class="sxs-lookup"><span data-stu-id="e84a0-119">For instructions on how to configure the Reports, see [How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md).</span></span>

**<span data-ttu-id="e84a0-120">Aktualisieren der Verbindungsdaten für Berichte auf dem Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="e84a0-120">Update the reports connection data on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="e84a0-121">Verwenden Sie auf dem Server, auf dem das Feature Berichte ausgeführt wird, die IIS-Manager-Konsole, um die Berichts-URL zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e84a0-121">On the server that is running the Reports feature, use the Internet Information Services (IIS) Manager console to update the Reports URL.</span></span>

2.  <span data-ttu-id="e84a0-122">Erweitern Sie **Microsoft BitLocker-Verwaltung und-Überwachung**, und wählen Sie dann den Knoten **Helpdesk** aus.</span><span class="sxs-lookup"><span data-stu-id="e84a0-122">Expand **Microsoft BitLocker Administration and Monitoring**, and then select the **HelpDesk** node.</span></span>

3.  <span data-ttu-id="e84a0-123">Wählen Sie im Abschnitt **Verwaltung** der **Ansicht Features**den Eintrag **Konfigurations-Editor**aus.</span><span class="sxs-lookup"><span data-stu-id="e84a0-123">In the **Management** section of the **Features View**, select **Configuration Editor**.</span></span>

4.  <span data-ttu-id="e84a0-124">Wählen Sie im Feld **Abschnitt** die Option **appSettings**aus.</span><span class="sxs-lookup"><span data-stu-id="e84a0-124">In the **Section** field, select **appSettings**.</span></span>

5.  <span data-ttu-id="e84a0-125">Wählen Sie die **Sammlungs** Zeile aus, und klicken Sie dann auf die Schaltfläche "Ellipsen" **(...)** ganz rechts im Bereich, um den **Sammlungs-Editor**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e84a0-125">Select the **Collection** row, and then click the "ellipses" button **(…)** at the far right of the pane to open the **Collection Editor**.</span></span>

6.  <span data-ttu-id="e84a0-126">Wählen Sie im **Sammlungs-Editor**die Zeile aus, die **Microsoft. mbam. Reports. URL**enthält, und aktualisieren Sie den Wert für **Microsoft. mbam. Reports. URL** so, dass der Servername für Server B wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="e84a0-126">In the **Collection Editor**, select the row that contains **Microsoft.Mbam.Reports.Url**, and update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B.</span></span>

    <span data-ttu-id="e84a0-127">Wenn Sie das Feature Berichte zuvor in einer benannten Instanz von SQL Server Reporting Services konfiguriert haben, fügen Sie den Namen der Instanz zur URL hinzu, oder aktualisieren Sie ihn, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="e84a0-127">If you previously configured the Reports feature on a named instance of SQL Server Reporting Services, add or update the name of the instance to the URL, for example:</span></span>

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  <span data-ttu-id="e84a0-128">Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl auf dem Verwaltungs-und Überwachungs Server ausführen, der mit dem folgenden Codebeispiel vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="e84a0-128">To automate this procedure, you can use Windows PowerShell to run a command on the Administration and Monitoring Server that is similar to the following code example.</span></span>

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    <span data-ttu-id="e84a0-129">Ersetzen Sie anhand der Beschreibungen in der folgenden Tabelle die Werte im Codebeispiel durch Werte, die Ihrer Umgebung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e84a0-129">Using the descriptions in the following table, replace the values in the code example with values that match your environment.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="e84a0-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="e84a0-130">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="e84a0-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e84a0-131">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e84a0-132">$Servername $</span><span class="sxs-lookup"><span data-stu-id="e84a0-132">$SERVERNAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e84a0-133">Der Name des Servers, auf den die Berichte verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="e84a0-133">Name of the server to which the Reports were moved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="e84a0-134">$SRSINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="e84a0-134">$SRSINSTANCENAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e84a0-135">Der Name der Instanz von SQL Server Reporting Services, in die die Berichte verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="e84a0-135">Name of the instance of SQL Server Reporting Services to which the Reports were moved.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="e84a0-136">Fortsetzen der Instanz der Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="e84a0-136">Resume the instance of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="e84a0-137">Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu starten.</span><span class="sxs-lookup"><span data-stu-id="e84a0-137">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="e84a0-138">Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl auszuführen, der der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="e84a0-138">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    <span data-ttu-id="e84a0-139">**Hinweis**  Zum Ausführen dieses Befehls müssen Sie das IIS-Modul für Windows PowerShell der aktuellen Instanz von Windows PowerShell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e84a0-139">**Note** To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

     



## <span data-ttu-id="e84a0-140">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e84a0-140">Related topics</span></span>


[<span data-ttu-id="e84a0-141">So konfigurieren Sie die MBAM 2.5-Berichte</span><span class="sxs-lookup"><span data-stu-id="e84a0-141">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="e84a0-142">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e84a0-142">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="e84a0-143">Verschieben von MBAM 2.5-Funktionen auf einen anderen Server</span><span class="sxs-lookup"><span data-stu-id="e84a0-143">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 
## <span data-ttu-id="e84a0-144">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="e84a0-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e84a0-145">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="e84a0-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="e84a0-146">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="e84a0-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





