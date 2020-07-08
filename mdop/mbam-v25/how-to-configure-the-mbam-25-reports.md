---
title: So konfigurieren Sie die MBAM 2.5-Berichte
description: So konfigurieren Sie die MBAM 2.5-Berichte
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811863"
---
# So konfigurieren Sie die MBAM 2.5-Berichte


In diesem Thema wird erläutert, wie Sie das 2,5-Feature für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mithilfe von folgendem konfigurieren:

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
<td align="left"><p>Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren möchten.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installieren der MBAM 2.5-Serversoftware</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell, wenn Sie Windows PowerShell-Cmdlets zum Konfigurieren der MBAM-Server Features verwenden möchten.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**So konfigurieren Sie die Berichte mithilfe von Windows PowerShell**

1.  Bevor Sie die Konfiguration starten, lesen Sie [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) zum Überprüfen der Voraussetzungen für die Verwendung von Windows PowerShell.

2.  Verwenden Sie das Windows PowerShell **-Cmdlet Enable-MbamReport** , um die Berichte zu konfigurieren. Um Informationen zu diesem Windows PowerShell-Cmdlet abzurufen, geben **Sie Get-Help enable-MbamReport**ein.

**So konfigurieren Sie die Berichte mit dem Assistenten**

1. Starten Sie auf dem Server, auf dem Sie die Berichte konfigurieren möchten, den **MBAM-Serverkonfigurations** -Assistenten. Sie können **MBAM Server Configuration** im **Startmenü** auswählen, um den Assistenten zu öffnen.

2. Klicken Sie auf **neue Features hinzufügen**, wählen Sie **Berichte**aus, und klicken Sie dann auf **weiter**. Der Assistent überprüft, ob alle Voraussetzungen für die Berichte erfüllt wurden.

3. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

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
   <td align="left"><p><strong>SQL Server Reporting Services-Instanz</strong></p></td>
   <td align="left"><p>Instanz von SQL Server Reporting Services, in der die Berichte konfiguriert werden.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Gruppe "Berichtsrolle-Domäne"</strong></p></td>
   <td align="left"><p>Name der Gruppe "Domänenbenutzer", deren Mitglieder über Rechte für den Zugriff auf die Berichte auf dem Verwaltungs-und Überwachungs Server verfügen</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>SQL Server-Name</strong></p></td>
   <td align="left"><p>Der Name des Servers, auf dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>SQL Server-Datenbankinstanz</strong></p></td>
   <td align="left"><p>Der Name der Instanz von SQL Server (beispielsweise <em> MSSQLSERVER </em> ), in der die Compliance-und Überwachungsdatenbank konfiguriert ist.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Sie müssen auf dem Computer "Berichte" eine Ausnahme hinzufügen, um eingehenden Datenverkehr am Port des Berichtsservers zu aktivieren (der Standardport ist 80).</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Datenbankname</strong></p></td>
   <td align="left"><p>Der Name der Konformitäts-und Überwachungsdatenbank. Standardmäßig ist der Datenbankname <strong> MBAM-Konformitäts Status </strong> , obwohl Sie den Namen ändern können, wenn Sie die Kompatibilitäts-und Überwachungsdatenbank konfigurieren.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Wenn Sie ein Upgrade von einer früheren Version von MBAM durchführen, müssen Sie denselben Datenbanknamen wie den in der vorherigen Bereitstellung verwendeten Namen verwenden.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Compliance-und Audit-Daten Bank Domänenkonto</strong></p></td>
   <td align="left"><p>Domänenbenutzerkonto und Kennwort für den Zugriff auf die Datenbank "Konformitäts-und Überwachungsdatenbank".</p>
   <p>Wenn der Wert, den Sie in das <strong> Feld "Schreibgeschützter Zugriffsdomänen Benutzer" oder "Gruppe" </strong> auf der <strong> Seite "Datenbanken konfigurieren </strong> " eingeben, ein Benutzer ist, müssen Sie diesen Wert in dieses Feld eingeben.</p>
   <p>Wenn der Wert, den Sie in das <strong> Feld "Schreibgeschützter Zugriffsdomänen Benutzer" oder "Gruppe" </strong> auf der <strong> Seite "Datenbanken konfigurieren" eingeben </strong> , eine Gruppe ist, muss der Wert, den Sie in dieses Feld eingeben, Mitglied dieser Gruppe sein.</p>
   <p>Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft. Das Benutzerkonto sollte auf alle Daten zugreifen können, die für die Gruppe MBAM-Berichte Benutzer verfügbar sind.</p></td>
   </tr>
   </tbody>
   </table>



5. Wenn Sie Ihre Eingaben abgeschlossen haben, klicken Sie auf **weiter**.

   Der Assistent überprüft, ob alle Voraussetzungen für das Berichtsfeature erfüllt wurden.

6. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

7. Überprüfen Sie auf der Seite **Zusammenfassung** die Features, die hinzugefügt werden sollen.

   **Hinweis:**  
   Wenn Sie ein Windows PowerShell-Skript der soeben erstellten Einträge erstellen möchten, klicken Sie auf **PowerShell-Skript exportieren**, und speichern Sie dann das Skript.



8. Klicken Sie auf **Hinzufügen** , um die Berichte auf dem Server hinzuzufügen, und klicken Sie dann auf **Schließen**.



## Verwandte Themen


[Serverereignisprotokolle](server-event-logs.md)

[Konfigurieren der MBAM 2.5-Serverfunktionen](configuring-the-mbam-25-server-features.md)

[So konfigurieren Sie die MBAM 2.5-Webanwendungen](how-to-configure-the-mbam-25-web-applications.md)

[Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen](validating-the-mbam-25-server-feature-configuration.md)


## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






