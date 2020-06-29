---
title: So konfigurieren Sie die MBAM 2.5-Datenbanken
description: So konfigurieren Sie die MBAM 2.5-Datenbanken
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811866"
---
# So konfigurieren Sie die MBAM 2.5-Datenbanken


In diesem Thema wird erläutert, wie Sie die Microsoft BitLocker-MBAM-2,5-Konformitäts-und-Überwachungsdatenbank und die Wiederherstellungsdatenbank mit folgenden Schritten konfigurieren:

-   Ein Windows PowerShell-Cmdlet

-   Der Serverkonfigurations-Assistent von MBAM

Die Anweisungen basieren auf der empfohlenen Architektur in der [Architektur auf hoher Ebene für MBAM 2,5](high-level-architecture-for-mbam-25.md).

**Bevor Sie die Konfiguration starten:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Wo erhalte ich Anweisungen?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Überprüfen Sie die empfohlene Architektur für MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">High-Level-Architektur für MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Überprüfen Sie die unterstützten Konfigurationen für MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Von MBAM 2.5 unterstützte Konfigurationen</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Führen Sie die erforderlichen Voraussetzungen für jeden Server aus.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2,5-Server Voraussetzungen, die nur für die Configuration Manager-Integrations Topologie gelten </a> (falls zutreffend)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren möchten.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Sie können die Datenbanken auf einem SQL Server-Remotecomputer mit Windows PowerShell oder einem exportierten Data-tier Application (DAC)-Paket installieren. Weitere Informationen zu DAC-Paketen finden Sie unter <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> Datenebenen-Anwendungen </a> .</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installieren der MBAM 2.5-Serversoftware</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell, wenn Sie Windows PowerShell-Cmdlets zum Konfigurieren der MBAM-Server Features verwenden möchten.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**So konfigurieren Sie die Datenbanken mithilfe von Windows PowerShell**

1.  Bevor Sie die Konfiguration starten, lesen Sie [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) zum Überprüfen der Voraussetzungen für die Verwendung von Windows PowerShell.

2.  Verwenden Sie das Windows PowerShell **-Cmdlet Enable-MbamDatabase** , um die Datenbanken zu konfigurieren. Um Informationen zu diesem Windows PowerShell-Cmdlet abzurufen, geben **Sie Get-Help enable-MbamDatabase**ein.

**So konfigurieren Sie die Konformitäts-und Überwachungsdatenbank mithilfe des Assistenten**

1. Starten Sie auf dem Server, auf dem Sie die Datenbanken konfigurieren möchten, den **MBAM-Serverkonfigurations** -Assistenten. Sie können **MBAM Server Configuration** im **Startmenü** auswählen, um den Assistenten zu öffnen.

2. Klicken Sie auf **neue Features hinzufügen**, wählen Sie **Compliance und Audit Database** und **Recovery Database**aus, und klicken Sie dann auf **weiter**. Der Assistent überprüft, ob alle Voraussetzungen für die Datenbanken erfüllt sind.

3. Wenn die Voraussetzungsprüfung erfolgreich ist, klicken Sie auf **weiter** , um fortzufahren. Beheben Sie andernfalls alle fehlenden Voraussetzungen, und klicken Sie dann **erneut auf Voraussetzungen prüfen**.

4. Geben Sie anhand der folgenden Beschreibungen die Feldwerte im Assistenten ein:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Feld</th>
   <th align="left">Beschreibung</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>SQL Server-Name</strong></p></td>
   <td align="left"><p>Der Name des Servers, auf dem Sie die Kompatibilitäts-und Überwachungsdatenbank konfigurieren.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Sie müssen auf dem Computer Compliance und Audit Database eine Ausnahme hinzufügen, um eingehenden Datenverkehr auf dem Microsoft SQL Server-Port zu aktivieren. Die Standardportnummer ist 1433.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>SQL Server-Datenbankinstanz</strong></p></td>
   <td align="left"><p>Der Name der Datenbankinstanz, in der die Konformitäts-und Überwachungsdaten gespeichert werden. Sie müssen außerdem angeben, wo sich die Datenbankinformationen befinden sollen.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Datenbankname</strong></p></td>
   <td align="left"><p>Der Name der Datenbank, in der die Kompatibilitätsdaten gespeichert werden.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Wenn Sie ein Upgrade von einer früheren Version von MBAM durchführen, müssen Sie denselben Datenbanknamen wie den Namen verwenden, der in der vorherigen Bereitstellung verwendet wurde.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Lese/Schreib-Zugriffsdomänen Benutzer oder-Gruppe</strong></p></td>
   <td align="left"><p>Domänenbenutzer oder-Gruppe, die über die Berechtigung "Lesen/Schreiben" für diese Datenbank verfügt, damit die Webanwendungen auf die Daten und Berichte in dieser Datenbank zugreifen können.</p>
   <p>Wenn Sie einen Benutzer in dieses Feld eingeben, muss er mit dem Wert im <strong> Feld Domänenkonto des Webdienst-Anwendungspools </strong> auf der <strong> Seite Webanwendungen konfigurieren identisch sein </strong> .</p>
   <p>Wenn Sie eine Gruppe in dieses Feld eingeben, muss der Wert im <strong> Feld "Webdienst-Anwendungspool Domäne" </strong> auf der <strong> Seite "Webanwendungen konfigurieren" </strong> ein Mitglied der Gruppe sein, die Sie in dieses Feld eingeben.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Schreibgeschützter Zugriffsdomänen Benutzer oder-Gruppe</strong></p></td>
   <td align="left"><p>Der Name des Benutzers oder der Gruppe, der über die Berechtigung "schreibgeschützt" für diese Datenbank verfügt, damit die Berichte auf die Kompatibilitätsdaten in dieser Datenbank zugreifen können.</p>
   <p>Wenn Sie einen Benutzer in dieses Feld eingeben, muss er derselbe Benutzer sein, den Sie im <strong> Feld Konformitäts-und Überwachungsdatenbank-Domänenkonto </strong> auf der <strong> Seite Berichte konfigurieren angeben </strong> .</p>
   <p>Wenn Sie eine Gruppe in dieses Feld eingeben, muss der Wert, den Sie im <strong> Feld Compliance und Audit Database Domain Account angeben, </strong> auf der <strong> Seite "Berichte konfigurieren" </strong> ein Mitglied der Gruppe sein, die Sie in diesem Feld angeben.</p></td>
   </tr>
   </tbody>
   </table>



5. Fahren Sie mit dem nächsten Abschnitt fort, um die Wiederherstellungsdatenbank zu konfigurieren.

**So konfigurieren Sie die Wiederherstellungsdatenbank mithilfe des Assistenten**

1. Geben Sie anhand der folgenden Beschreibungen die Feldwerte im Assistenten ein:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Feld</th>
   <th align="left">Beschreibung</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>SQL Server-Name</strong></p></td>
   <td align="left"><p>Der Name des Servers, auf dem Sie die Wiederherstellungsdatenbank konfigurieren.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Sie müssen auf dem Wiederherstellungsdaten Bank Computer eine Ausnahme hinzufügen, um eingehenden Datenverkehr auf dem Microsoft SQL Server-Port zu aktivieren. Die Standardportnummer ist 1433.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>SQL Server-Datenbankinstanz</strong></p></td>
   <td align="left"><p>Der Name der Datenbankinstanz, in der die Wiederherstellungsdaten gespeichert werden. Sie müssen außerdem angeben, wo sich die Datenbankinformationen befinden sollen.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Datenbankname</strong></p></td>
   <td align="left"><p>Der Name der Datenbank, in der die Wiederherstellungsdaten gespeichert werden.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Wenn Sie ein Upgrade von einer früheren Version von MBAM durchführen, müssen Sie denselben Datenbanknamen wie den Namen verwenden, der in der vorherigen Bereitstellung verwendet wurde.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Lese/Schreib-Zugriffsdomänen Benutzer oder-Gruppe</strong></p></td>
   <td align="left"><p>Domänenbenutzer oder-Gruppe, die über die Berechtigung "Lesen/Schreiben" für diese Datenbank verfügt, damit die Webanwendungen auf die Daten und Berichte in dieser Datenbank zugreifen können.</p>
   <p>Wenn Sie einen Benutzer in dieses Feld eingeben, muss er mit dem Wert im <strong> Feld Domänenkonto des Webdienst-Anwendungspools </strong> auf der <strong> Seite Webanwendungen konfigurieren identisch sein </strong> .</p>
   <p>Wenn Sie eine Gruppe in dieses Feld eingeben, muss der Wert im <strong> Feld "Webdienst-Anwendungspool Domäne" </strong> auf der <strong> Seite "Webanwendungen konfigurieren" </strong> ein Mitglied der Gruppe sein, die Sie in dieses Feld eingeben.</p></td>
   </tr>
   </tbody>
   </table>



2. Wenn Sie Ihre Eingaben abgeschlossen haben, klicken Sie auf **weiter**.

   Der Assistent überprüft, ob alle Voraussetzungen für die Datenbanken erfüllt sind.

3. Wenn die Voraussetzungsprüfung erfolgreich ist, klicken Sie auf **weiter** , um fortzufahren. Beheben Sie andernfalls alle fehlenden Voraussetzungen, und klicken Sie dann erneut auf **weiter** .

4. Überprüfen Sie auf der Seite **Zusammenfassung** die Features, die hinzugefügt werden sollen.

   **Hinweis:**  
   Wenn Sie ein Windows PowerShell-Skript der soeben erstellten Einträge erstellen möchten, klicken Sie auf **PowerShell-Skript exportieren**, und speichern Sie dann das Skript.



5. Klicken Sie auf **Hinzufügen** , um die MBAM-Datenbanken auf dem Server hinzuzufügen, und klicken Sie dann auf **Schließen**.



## Verwandte Themen


[Serverereignisprotokolle](server-event-logs.md)

[Konfigurieren der MBAM 2.5-Serverfunktionen](configuring-the-mbam-25-server-features.md)

[So konfigurieren Sie die MBAM 2.5-Berichte](how-to-configure-the-mbam-25-reports.md)

[So konfigurieren Sie die MBAM 2.5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md)

[Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen](validating-the-mbam-25-server-feature-configuration.md)



## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





