---
title: Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell
description: Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809595"
---
# Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell


Nachdem Sie die MBAM 2,5-Server Software installiert haben, können Sie mithilfe von Windows PowerShell-Cmdlets oder dem MBAM-Serverkonfigurations-Assistenten MBAM 2,5-Server Features konfigurieren. In diesem Thema wird beschrieben, wie Sie MBAM 2,5 mithilfe der Windows PowerShell-Cmdlets konfigurieren. Informationen zum Verwenden des Assistenten finden Sie unter [Konfigurieren der MBAM 2,5-Server Features](configuring-the-mbam-25-server-features.md).

## Inhalt dieses Themas


Dieses Thema enthält die folgenden Informationen zur Verwendung von Windows PowerShell zum Konfigurieren von MBAM:

-   [Laden der Windows PowerShell-Hilfe für MBAM 2,5](#bkmk-load-posh-help)

-   [So erhalten Sie Hilfe zu einem MBAM Windows PowerShell-Cmdlet](#bkmk-help-specific-cmdlet)

-   [Konfigurationen, die Sie nur mit Windows PowerShell ausführen können, aber nicht mit dem Serverkonfigurations-Assistenten von MBAM](#bkmk-config-only-posh)

-   [Voraussetzungen und Voraussetzungen für die Verwendung von Windows PowerShell zum Konfigurieren von MBAM-Server Features](#bkmk-prereqs-posh-mbamsvr)

-   [Verwenden von Windows PowerShell zum Konfigurieren von MBAM auf einem Remotecomputer](#bkmk-remote-config)

-   [Erforderliche Konten und entsprechende Windows PowerShell-Cmdlet-Parameter](#bkmk-reqd-posh-accts)

Informationen zu den Windows PowerShell-Cmdlets " **Get-MbamBitLockerRecoveryKey** " und " **Get-MbamTPMOwnerPassword** ", die für die Verwaltung von MBAM verwendet werden, finden Sie unter [Verwenden von Windows PowerShell zum Verwalten von MBAM 2,5](using-windows-powershell-to-administer-mbam-25.md).

## <a href="" id="bkmk-load-posh-help"></a>Laden der Windows PowerShell-Hilfe für MBAM 2,5


Eine Liste der Windows PowerShell-Cmdlets auf TechNet finden Sie unter [Automatisierung des Microsoft-Desktop Optimierungs Pakets mit Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).

**So laden Sie die MBAM 2,5-Hilfe für Windows PowerShell-Cmdlets nach der Installation der MBAM-Server Software**

1.  Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).

2.  Geben Sie **Update-Help-Module Microsoft. MBAM**.

## <a href="" id="bkmk-help-specific-cmdlet"></a>So erhalten Sie Hilfe zu einem MBAM Windows PowerShell-Cmdlet


Die Windows PowerShell-Hilfe für MBAM ist in den folgenden Formaten verfügbar:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows PowerShell-Hilfeformat</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Geben Sie an einer Windows PowerShell-Eingabeaufforderung <strong> Get-Help- </strong> &lt; <em> Cmdlet ein.</em>&gt;</p></td>
<td align="left"><p>Wenn Sie die neuesten Windows PowerShell-Cmdlets hochladen möchten, befolgen Sie die Anweisungen im vorherigen Abschnitt zum Laden der Windows PowerShell-Hilfe für MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Auf TechNet als Webseiten</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Im Download Center als Word. docx-Datei</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Im Download Center als PDF-Datei</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a>Konfigurationen, die Sie nur mit Windows PowerShell ausführen können, aber nicht mit dem Serverkonfigurations-Assistenten von MBAM


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Konfigurationen, die nur mithilfe von Windows PowerShell möglich sind</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Installieren Sie die Webdienste auf einem anderen Computer als die Webanwendungen.</p></td>
<td align="left"><p>Sie müssen die Webdienste und Webanwendungen mithilfe des Assistenten auf demselben Computer installieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aktivieren Sie Berichte auf einem separaten Reporting Services-Punkt, ohne alle Configuration Manager-Objekte zu installieren.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Löschen Sie alle Objekte aus Configuration Manager.</p></td>
<td align="left"><p>Wenn Sie die Objekte löschen, werden alle Kompatibilitätsdaten aus Configuration Manager gelöscht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Geben Sie eine benutzerdefinierte Verbindungszeichenfolge für die Datenbanken ein.</p></td>
<td align="left"><p>Beispiel: Wenn Sie die Webanwendungen so konfigurieren möchten, dass Sie mit der Spiegelung arbeiten, müssen Sie das <strong> Cmdlet Enable-MbamWebApplication verwenden </strong> , um die entsprechende Failover-Partner-Syntax in der Verbindungszeichenfolge anzugeben.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Überspringen Sie die Validierung, und konfigurieren Sie ein Feature, obwohl die Voraussetzungen nicht überprüft wurden.</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Sie können die MBAM-Datenbanken mit einem Windows PowerShell-Cmdlet oder dem Serverkonfigurations-Assistenten für MBAM nicht deaktivieren. Um zu verhindern, dass Ihre Konformitäts-und Überwachungsdaten versehentlich entfernt werden, müssen Datenbankadministratoren Datenbanken manuell entfernen.

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a>Voraussetzungen und Voraussetzungen für die Verwendung von Windows PowerShell zum Konfigurieren von MBAM-Server Features


Bevor Sie mit der Konfiguration beginnen, führen Sie die folgenden Voraussetzungen aus.

**Kontobezogene Voraussetzungen**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzung</th>
<th align="left">Details oder weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Erstellen Sie die erforderlichen Konten.</p></td>
<td align="left"><p>Weitere Informationen finden Sie <strong> </strong> weiter unten in diesem Thema unter Abschnitt erforderliche Konten und entsprechende Windows PowerShell-Cmdlet-Parameter.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Benutzerkonten und Gruppen, die Sie als Parameter an die Windows PowerShell-Cmdlets übergeben, müssen gültige Konten in der Domäne sein.</p></td>
<td align="left"><p>Sie können keine lokalen Konten verwenden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Geben Sie Konten im Format der untergeordneten Ebene an.</p></td>
<td align="left"><p>Beispiele:</p>
<p>domainNetBiosName\userdomainNetBiosName\group</p></td>
</tr>
</tbody>
</table>

 

**Berechtigungsbezogene Voraussetzungen**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzung</th>
<th align="left">Details oder weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sie müssen ein Administrator auf dem lokalen Computer sein, auf dem Sie das MBAM-Feature konfigurieren.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Verwenden Sie eine erweiterte Windows PowerShell-Eingabeaufforderung, um alle Windows PowerShell-Cmdlets auszuführen.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nur für das <strong> Cmdlet Enable-MbamDatabase </strong> :</p>
<p>Sie müssen &quot; über CREATE ANY DATABASE &quot; -Berechtigungen für die Instanz der Microsoft SQL Server-Zieldatenbank verfügen.</p>
<p>Dieses Benutzerkonto muss Teil der lokalen Gruppe Administratoren oder der Gruppe Sicherungs-Operatoren sein, um den VSS-Writer (MBAM Volume Shadow Copy Service) registrieren zu können.</p></td>
<td align="left"><p>Standardmäßig verfügt der Datenbankadministrator oder System Administrator über die erforderlichen &quot; CREATE ANY DATABASE- &quot; Berechtigungen.</p>
<p></p>
<p>Weitere Informationen zu VSS Writer finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> Volumeschattenkopie-Dienst </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nur für das <strong> System Center Configuration Manager-Integrations </strong> Feature:</p>
<p>Der Benutzer, der dieses Feature aktiviert, muss über diese Rechte in Configuration Manager verfügen:</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Art der Rechte in Configuration Manager</th>
<th align="left">Erforderliche Rechte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuration Manager-Website Rechte:</p></td>
<td align="left"><p>- Lesen</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sammlungs Rechte für Configuration Manager:</p></td>
<td align="left"><p>- Erstellen – Löschen – lesen – ändern – Bereitstellen von Konfigurationselementen</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager-Konfigurationselement Rechte:</p></td>
<td align="left"><p>- Erstellen-Löschen-lesen</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a>Verwenden von Windows PowerShell zum Konfigurieren von MBAM auf einem Remotecomputer


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Verwendung dieser Funktion</strong></p></td>
<td align="left"><p>Wenn Sie die MBAM 2,5-Server Features auf einem Remotecomputer konfigurieren möchten. Die Windows PowerShell-Cmdlets werden auf einem Computer ausgeführt, und Sie konfigurieren die Features auf einem anderen Remotecomputer.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Was Sie tun müssen</strong></p></td>
<td align="left"><p>Wenn Sie Windows PowerShell zum Konfigurieren der MBAM 2,5-Server Features auf einem Remotecomputer verwenden möchten, müssen Sie Folgendes ausführen:</p>
<ul>
<li><p>Stellen Sie sicher, dass die MBAM 2,5-Server Software auf dem Remotecomputer installiert wurde.</p></li>
<li><p>Verwenden Sie das CredSSP-Protokoll (Credential Security Support Provider), um die Windows PowerShell-Sitzung zu öffnen.</p></li>
<li><p>Aktivieren Sie die Windows-Remote Verwaltung (WinRM). Wenn Sie WinRM nicht aktivieren und richtig konfigurieren, <strong> </strong> zeigt das in dieser Tabelle beschriebene Cmdlet New-PSSession einen Fehler an, und es wird beschrieben, wie Sie das Problem beheben können. Weitere Informationen zu WinRM finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> Verwenden der Windows-Remote Verwaltung </a> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Warum müssen Sie das tun?</strong></p></td>
<td align="left"><p>Dieses Protokoll ermöglicht es den Windows PowerShell-Cmdlets, mithilfe der administrativen Anmeldeinformationen des Benutzers eine Verbindung mit Active Directory-Domänendiensten herzustellen. Möglicherweise erhalten Sie einen Überprüfungsfehler, wenn Sie die Windows PowerShell-Sitzung ohne dieses Protokoll starten.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Starten einer Windows PowerShell-Sitzung mit dem CredSSP-Protokoll</strong></p></td>
<td align="left"><p>Geben Sie den folgenden Code an der Windows PowerShell-Eingabeaufforderung ein:</p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p>Der folgende Code zeigt ein Beispiel.</p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a>Erforderliche Konten und entsprechende Windows PowerShell-Cmdlet-Parameter


In der folgenden Tabelle werden die Konten beschrieben, die für die Konfiguration der MBAM 2,5-Server Features erforderlich sind. Außerdem werden das entsprechende Windows PowerShell-Cmdlet und der zugehörige Parameter aufgelistet, für die Sie das Konto während der Konfiguration angeben müssen.

Cmdlet-Parametertyp (Benutzer oder Gruppe) Description enable-MBAMDatabase

AccessAccount

Benutzer oder Gruppe

Geben Sie einen Domänenbenutzer oder eine Gruppe mit Lese-/Schreibzugriff für diese Datenbank an, damit die Webanwendungen auf Daten und Berichte in dieser Datenbank zugreifen können. Wenn der Wert ein Domänenbenutzer ist, muss der **WebServiceApplicationPoolCredential** -Parameter, der beim Ausführen des Cmdlets **enable-MbamWebApplication** verwendet wird, dasselbe Benutzerkonto verwenden. Wenn es sich bei dem Wert um eine Domänenbenutzergruppe handelt, muss das vom **WebServiceApplicationPoolCredential** -Parameter verwendete Domänenkonto Mitglied dieser Gruppe sein.

ReportAccount

Benutzer oder Gruppe

Geben Sie einen Domänenbenutzer oder eine Benutzergruppe an, die über die Berechtigung "schreibgeschützt" für diese Datenbank verfügt, um dem MBAM-Berichtzugriff auf die Konformitäts-und Überwachungsdaten bereitzustellen. Wenn der Wert ein Domänenbenutzer ist, muss der **ComplianceAndAuditDBCredential** -Parameter des Cmdlets **enable-MbamReport** das gleiche Benutzerkonto verwenden. Wenn es sich bei dem Wert um eine Domänenbenutzergruppe handelt, muss das vom **ComplianceAndAuditDBCredential** -Parameter verwendete Domänenkonto Mitglied dieser Gruppe sein.

Enable-MbamReport

ComplianceAndAuditDBCredential

Benutzer

Gibt die Administratoranmeldeinformationen an, die von der lokalen SSRS-Instanz für die Verbindung mit der MBAM-Konformitäts-und Überwachungsdatenbank verwendet werden. Der Domänenbenutzer in den administrativen Anmeldeinformationen muss mit dem Benutzerkonto identisch sein, das für den **ReportAccount** -Parameter verwendet wird, der während der Ausführung des Cmdlets **enable-MbamDatabase** verwendet wird. Wenn eine Gruppe von Domänenbenutzern mit dem **ReportAccount** -Parameter verwendet wurde, sollte dieses Konto ein Mitglied dieser Gruppe sein.

**Wichtig**  Das in den administrativen Anmeldeinformationen angegebene Konto sollte über beschränkte Benutzerrechte verfügen, um die Sicherheit zu verbessern. Außerdem sollte das Kennwort des Kontos auf nicht ablaufen festgesetzt werden.

 

ReportsReadOnlyAccessGroup

Gruppe

Gibt die Domänenbenutzergruppe an, die über Leseberechtigungen für die Berichte verfügt. Die angegebene Gruppe muss dieselbe Gruppe sein, die für den **ReportsReadOnlyAccessGroup** -Parameter im Cmdlet **enable-MbamWebApplication** verwendet wird.

Enable-MBAMWebApplication

AdvancedHelpdeskAccessGroup

Gruppe

Gibt die Gruppe "Domänenbenutzer" an, die auf alle Bereiche der Verwaltungs-und Überwachungs Website mit Ausnahme des Bereichs "Berichte" zugreifen kann.

HelpdeskAccessGroup

Gruppe

Gibt die Gruppe "Domänenbenutzer" an, die Zugriff auf die Bereiche " **TPM verwalten** " und " **Laufwerk Wiederherstellung** " der Website "Verwaltung und Überwachung" hat.

ReportsReadOnlyAccessGroup

Gruppe

Gibt die Gruppe "Domänenbenutzer" an, die über die Berechtigung "lesen" für den Bereich " **Berichte** " der Website "Verwaltung und Überwachung" verfügt. Die angegebene Gruppe muss dieselbe Gruppe sein, die für den **ReportsReadOnlyAccessGroup** -Parameter im Cmdlet **enable-MbamReport** verwendet wird.

WebServiceApplicationPoolCredential

Benutzer

Gibt den Domänenbenutzer an, der vom Anwendungspool für die MBAM-Webanwendungen verwendet werden soll. Es muss sich um das gleiche Domänenbenutzerkonto handeln, das im **AccessAccount** -Parameter des Cmdlets **enable-MbamDatabase** angegeben ist. Wenn der **AccessAccount** -Parameter beim Ausführen des **enable-MbamDatabase-** Cmdlets eine Domänenbenutzergruppe verwendet hat, muss der hier angegebene Domänenbenutzer ein Mitglied dieser Gruppe sein. Wenn Sie die administrativen Anmeldeinformationen nicht angeben, werden die Administratoranmeldeinformationen verwendet, die von einer zuvor aktivierten Webanwendung angegeben wurden. Alle Webanwendungen verwenden dieselbe Anwendungspoolidentität. Wenn Sie mehrmals angegeben wird, wird der zuletzt angegebene Wert verwendet.

**Wichtig**  Um die Sicherheit zu verbessern, legen Sie das in den administrativen Anmeldeinformationen angegebene Konto auf begrenzte Benutzerrechte fest. Legen Sie außerdem das Kennwort des Kontos so ein, dass es nie abläuft. Stellen Sie sicher, dass entweder das integrierte IIS \ _IUSRS-Konto oder das Konto, das für den **WebServiceApplicationPoolCredential** -Parameter verwendet wird, zur Einstellung für den **Identitätswechsel zu einem Client nach der Authentifizierungs** lokalen Sicherheit hinzugefügt wurde.

Wenn Sie die lokale Sicherheitseinstellung anzeigen möchten, öffnen Sie den **lokalen Sicherheitsrichtlinien-Editor**, erweitern Sie den Knoten **lokale Richtlinien** , wählen Sie den Knoten **Benutzerrechtezuweisung** aus, und doppelklicken Sie dann im Detailbereich auf die Einstellungen für **Client nach Authentifizierung** und **Anmeldung als Stapelverarbeitungsauftrag** .

 

 




## Verwandte Themen


[Konfigurieren der MBAM 2.5-Serverfunktionen](configuring-the-mbam-25-server-features.md)

[Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen](validating-the-mbam-25-server-feature-configuration.md)

[Verwenden von Windows PowerShell zum Verwalten von MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md)

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





