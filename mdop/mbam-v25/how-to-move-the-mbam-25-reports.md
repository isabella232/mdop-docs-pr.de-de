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
# So verschieben Sie MBAM 2.5-Berichte


Verwenden Sie diese Verfahren, um das Berichtsfeature von einem Computer auf einen anderen zu verschieben, d. h., um das Berichtsfeature von Server a auf Server B zu verschieben.

Die allgemeinen Schritte zum Verschieben des Berichtsfeatures sind:

1.  Beenden Sie alle Instanzen der MBAM-Verwaltungs-und-Überwachungs Website.

2.  Installieren Sie die MBAM 2,5-Server Software auf Server b, und konfigurieren Sie das Feature Berichte auf Server b.

3.  Aktualisieren Sie die Berichts Verbindungsdaten auf den MBAM-Verwaltungs-und-Überwachungs Servern.

4.  Setzen Sie die Instanz der MBAM-Verwaltungs-und-Überwachungs Website fort.

**Hinweis**  Wenn Sie die Beispiel-Windows PowerShell-Skripts in diesem Thema ausführen möchten, müssen Sie die Windows PowerShell-Ausführungsrichtlinie aktualisieren, damit Skripts ausgeführt werden können. Anweisungen finden Sie unter [Ausführen von Windows PowerShell-Skripts](https://technet.microsoft.com/library/ee176949.aspx) .

 

**Beenden der MBAM-Verwaltungs-und-Überwachungs Website**

-   Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu beenden.

    Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl einzugeben, der der folgenden ähnelt:

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**Installieren der MBAM-Server Software und Ausführen des MBAM-Serverkonfigurations-Assistenten auf Server B**

1.  Installieren Sie die MBAM-Server Software auf Server B. Anweisungen hierzu finden Sie unter [Installieren der MBAM 2,5-Server Software](installing-the-mbam-25-server-software.md).

2.  Starten Sie auf Server B den MBAM-Serverkonfigurations-Assistenten, klicken Sie auf **neue Features hinzufügen**, und wählen Sie dann nur das Feature **Berichte** aus.

    Alternativ können Sie das Windows PowerShell **-Cmdlet Enable-MbamReport** verwenden, um die Berichte zu konfigurieren.

    Anweisungen zum Konfigurieren der Berichte finden Sie unter [Konfigurieren der MBAM 2,5-Berichte](how-to-configure-the-mbam-25-reports.md).

**Aktualisieren der Verbindungsdaten für Berichte auf dem Verwaltungs-und Überwachungs Server**

1.  Verwenden Sie auf dem Server, auf dem das Feature Berichte ausgeführt wird, die IIS-Manager-Konsole, um die Berichts-URL zu aktualisieren.

2.  Erweitern Sie **Microsoft BitLocker-Verwaltung und-Überwachung**, und wählen Sie dann den Knoten **Helpdesk** aus.

3.  Wählen Sie im Abschnitt **Verwaltung** der **Ansicht Features**den Eintrag **Konfigurations-Editor**aus.

4.  Wählen Sie im Feld **Abschnitt** die Option **appSettings**aus.

5.  Wählen Sie die **Sammlungs** Zeile aus, und klicken Sie dann auf die Schaltfläche "Ellipsen" **(...)** ganz rechts im Bereich, um den **Sammlungs-Editor**zu öffnen.

6.  Wählen Sie im **Sammlungs-Editor**die Zeile aus, die **Microsoft. mbam. Reports. URL**enthält, und aktualisieren Sie den Wert für **Microsoft. mbam. Reports. URL** so, dass der Servername für Server B wiedergibt.

    Wenn Sie das Feature Berichte zuvor in einer benannten Instanz von SQL Server Reporting Services konfiguriert haben, fügen Sie den Namen der Instanz zur URL hinzu, oder aktualisieren Sie ihn, beispielsweise:

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  Um dieses Verfahren zu automatisieren, können Sie mithilfe von Windows PowerShell einen Befehl auf dem Verwaltungs-und Überwachungs Server ausführen, der mit dem folgenden Codebeispiel vergleichbar ist.

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    Ersetzen Sie anhand der Beschreibungen in der folgenden Tabelle die Werte im Codebeispiel durch Werte, die Ihrer Umgebung entsprechen.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parameter</th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>$Servername $</p></td>
    <td align="left"><p>Der Name des Servers, auf den die Berichte verschoben wurden.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$SRSINSTANCENAME $</p></td>
    <td align="left"><p>Der Name der Instanz von SQL Server Reporting Services, in die die Berichte verschoben wurden.</p></td>
    </tr>
    </tbody>
    </table>

     

**Fortsetzen der Instanz der Website "Verwaltung und Überwachung"**

1.  Verwenden Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website ausgeführt wird, die Internetinformationsdienste (IIS)-Manager-Konsole, um die Verwaltungs-und Überwachungs Website zu starten.

2.  Um dieses Verfahren zu automatisieren, können Sie Windows PowerShell verwenden, um einen Befehl auszuführen, der der folgenden ähnelt:

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    **Hinweis**  Zum Ausführen dieses Befehls müssen Sie das IIS-Modul für Windows PowerShell der aktuellen Instanz von Windows PowerShell hinzufügen.

     



## Verwandte Themen


[So konfigurieren Sie die MBAM 2.5-Berichte](how-to-configure-the-mbam-25-reports.md)

[Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Verschieben von MBAM 2.5-Funktionen auf einen anderen Server](moving-mbam-25-features-to-another-server.md)

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





