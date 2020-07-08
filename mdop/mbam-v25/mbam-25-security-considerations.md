---
title: Sicherheitsüberlegungen zu MBAM2.5
description: Sicherheitsüberlegungen zu MBAM2.5
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811995"
---
# Sicherheitsüberlegungen zu MBAM2.5


Dieses Thema enthält die folgenden Informationen zum Sichern der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM):

-   [Konfigurieren von MBAM zum Escrow-und Speichern von OwnerAuth-Kennwörtern](#bkmk-tpm)

-   [Konfigurieren von MBAM so, dass das TPM nach einer Sperrung automatisch freigegeben wird](#bkmk-autounlock)

-   [Sichere Verbindungen mit SQL Server](#bkmk-secure-databases)

-   [Erstellen von Konten und Gruppen](#bkmk-accts-groups)

-   [Verwenden von MBAM-Protokolldateien](#bkmk-logfiles)

-   [Überlegungen zu MBAM Database DSA](#bkmk-tde)

-   [Grundlegendes zu allgemeinen Sicherheitsüberlegungen](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a>Konfigurieren von MBAM zum Escrow-und Speichern von OwnerAuth-Kennwörtern

**Hinweis** Für Windows 10, Version 1607 oder höher, kann nur Windows den Besitz des TPM übernehmen. Darüber hinaus wird das TPM-Besitzerkennwort beim Bereitstellen des TPMs nicht von Windows beibehalten. Weitere Informationen finden Sie unter [TPM-Besitzerkennwort](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .

Je nach Konfiguration wird sich das Trusted Platform Module (TPM) in bestimmten Situationen selbst sperren, beispielsweise wenn zu viele falsche Kennwörter eingegeben werden und für einen bestimmten Zeitraum gesperrt bleiben können. Während der TPM-Sperrung kann BitLocker nicht auf die Verschlüsselungsschlüssel zugreifen, um entsperrungs-oder Entschlüsselungsvorgänge durchzuführen, sodass der Benutzer seinen BitLocker-Wiederherstellungsschlüssel für den Zugriff auf das Betriebssystemlaufwerk eingeben muss. Um die TPM-Sperrung zurückzusetzen, müssen Sie das TPM-OwnerAuth-Kennwort angeben.

MBAM kann das TPM-OwnerAuth-Kennwort in der MBAM-Datenbank speichern, wenn es das TPM besitzt oder das Kennwort Escrows. OwnerAuth-Kennwörter können dann auf der Website Verwaltung und Überwachung problemlos aufgerufen werden, wenn Sie eine TPM-Sperrung wiederherstellen müssen, wodurch nicht mehr gewartet werden muss, bis die Sperre für sich selbst aufgelöst wird.

### Treuhandservice für TPM-OwnerAuth in Windows 8 und höher

**Hinweis** Für Windows 10, Version 1607 oder höher, kann nur Windows den Besitz des TPM übernehmen. In addiiton wird Windows das TPM-Besitzerkennwort beim Bereitstellen des TPMs nicht beibehalten. Weitere Informationen finden Sie unter [TPM-Besitzerkennwort](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .

In Windows 8 oder höher muss MBAM nicht mehr das TPM besitzen, um das OwnerAuth-Kennwort speichern zu können, solange das OwnerAuth auf dem lokalen Computer verfügbar ist.

Um MBAM zu aktivieren und dann TPM-OwnerAuth-Kennwörter zu speichern, müssen Sie diese Gruppenrichtlinieneinstellungen konfigurieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Gruppenrichtlinieneinstellung</th>
<th align="left">Konfiguration</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aktivieren der TPM-Sicherung in Active Directory-Domänendiensten</p></td>
<td align="left"><p>Deaktiviert oder nicht konfiguriert</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren der Ebene der TPM-Besitzer Autorisierungsinformationen, die für das Betriebssystem verfügbar sind</p></td>
<td align="left"><p>Delegiert/keine oder nicht konfiguriert</p></td>
</tr>
</tbody>
</table>

 

Der Speicherort dieser Gruppenrichtlinieneinstellungen ist **Computer Configuration** &gt; **Administrative Templates** &gt; **System** &gt; **Trusted Platform Module Services**.

**Hinweis**  Windows entfernt die OwnerAuth lokal, nachdem MBAM diese Einstellungen erfolgreich durchgeführt hat.

 

### Treuhandservice für TPM-OwnerAuth in Windows 7

In Windows 7 muss MBAM das TPM besitzen, damit TPM-OwnerAuth-Informationen automatisch in der MBAM-Datenbank gespeichert werden. Wenn MBAM nicht über das TPM verfügt, müssen Sie die MBAM Active Directory (AD)-Daten Import-Cmdlets verwenden, um TPM-OwnerAuth aus Active Directory in die MBAM-Datenbank zu kopieren.

### MBAM-Cmdlets für Active Directory-Daten Import

Mit den MBAM-Cmdlets für Active Directory-Daten Import können Sie Wiederherstellungsschlüssel Pakete und OwnerAuth-Kennwörter abrufen, die in Active Directory gespeichert sind.

Der MBAM 2,5 SP1-Server wird mit vier PowerShell-Cmdlets ausgeliefert, die MBAM-Datenbanken mit den in Active Directory gespeicherten Informationen zur Volume-Wiederherstellung und dem TPM-Besitzer auffüllen.

Für Volume-Wiederherstellungsschlüssel und-Pakete:

-   Lesen-ADRecoveryInformation

-   Write-MbamRecoveryInformation

Informationen zu TPM-Besitzern:

-   Lesen-ADTpmInformation

-   Write-MbamTpmInformation

Zum Zuordnen von Benutzern zu Computern:

-   Write-MbamComputerUser

Die Read-AD \ *-Cmdlets lesen Informationen aus Active Directory. Die Write-mbam \ *-Cmdlets schieben die Daten in die mbam-Datenbanken. Detaillierte Informationen zu diesen Cmdlets, einschließlich Syntax, Parametern und Beispielen, finden Sie unter [Cmdlet-Referenz für Microsoft BitLocker-Verwaltung und-Überwachung 2,5](https://technet.microsoft.com/library/dn459018.aspx) .

**Erstellen von Benutzer-zu-Computer-Zuordnungen:** Die MBAM Active Directory-Daten Import-Cmdlets sammeln Informationen aus Active Directory und fügen die Daten in die MBAM-Datenbank ein. Sie ordnen Benutzer jedoch keinen Volumes zu. Sie können das Add-ComputerUser.ps1 PowerShell-Skript herunterladen, um Benutzer-zu-Computer-Zuordnungen zu erstellen, die Benutzern den Zugriff auf einen Computer über die Verwaltungs-und Überwachungs Website oder über das Self-Service-Portal für die Wiederherstellung ermöglichen. Das Add-ComputerUser.ps1-Skript sammelt Daten aus dem Attribut **Managed by** in Active Directory (AD), dem Objektbesitzer in AD oder aus einer benutzerdefinierten CSV-Datei. Das Skript fügt die erkannten Benutzer dann dem Pipelineobjekt für Wiederherstellungsinformationen hinzu, das an Write-MbamRecoveryInformation übergeben werden muss, um die Daten in die Wiederherstellungsdatenbank einzufügen.

Laden Sie das Add-ComputerUser.ps1 PowerShell-Skript aus dem [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=613122)herunter.

Sie können **Hilfe Add-ComputerUser.ps1** angeben, um Hilfe zu dem Skript zu erhalten, einschließlich Beispiele für die Verwendung der Cmdlets und des Skripts.

Verwenden Sie das PowerShell-Cmdlet Write-MbamComputerUser, um Benutzer-zu-Computer-Zuordnungen zu erstellen, nachdem Sie den MBAM-Server installiert haben. Ähnlich wie beim Add-ComputerUser.ps1 PowerShell-Skript können Sie mit diesem Cmdlet Benutzer angeben, die das Self-Service-Portal verwenden können, um TPM-OwnerAuth-Informationen oder Kennwörter für die Volume-Wiederherstellung für den angegebenen Computer abzurufen.

**Hinweis**  Der MBAM-Agent überschreibt Benutzer-zu-Computer-Zuordnungen, wenn dieser Computer mit der Berichterstellung an den Server beginnt.

 

**Voraussetzungen:** Die "Read-AD \ *"-Cmdlets können Informationen nur von anzeigen abrufen, wenn Sie entweder als hoch privilegiertes Benutzerkonto ausgeführt werden, beispielsweise als Domänen Administrator, oder als Konto in einer benutzerdefinierten Sicherheitsgruppe ausgeführt werden, die Lesezugriff auf die Informationen gewährt (empfohlen).

[Leitfaden zur BitLocker-Laufwerkverschlüsselung: das Wiederherstellen verschlüsselter Volumes mit AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) bietet Details zum Erstellen einer benutzerdefinierten Sicherheitsgruppe (oder mehrerer Gruppen) mit Lesezugriff auf die anzeigen Informationen.

**MBAM Recovery-und Hardware-Webdienst-Schreibberechtigungen:** Die Cmdlets Write-mbam \ * akzeptieren die URL des mbam-Wiederherstellungs-und-Hardware Diensts, der zum Veröffentlichen der Wiederherstellungs-oder TPM-Informationen verwendet wird. In der Regel kann nur ein Domänencomputer Dienstkonto mit dem MBAM-Wiederherstellungs-und-Hardware Dienst kommunizieren. In MBAM 2,5 SP1 können Sie den MBAM-Wiederherstellungs-und-Hardware Dienst mit einer Sicherheitsgruppe namens DataMigrationAccessGroup konfigurieren, deren Mitglieder die Überprüfung des Domänencomputer Dienst-Kontos umgehen dürfen. Die Cmdlets für Write-mbam \ * müssen als Benutzer ausgeführt werden, die zu dieser konfigurierten Gruppe gehören. (Alternativ können die Anmeldeinformationen eines einzelnen Benutzers in der konfigurierten Gruppe mithilfe des Parameters "– Credential" in den Cmdlets "Write-mbam \ *" angegeben werden.)

Sie können den MBAM-Wiederherstellungs-und-Hardware Dienst mit dem Namen dieser Sicherheitsgruppe auf eine der folgenden Arten konfigurieren:

-   Geben Sie den Namen der Sicherheitsgruppe (oder einzelner) im Parameter-DataMigrationAccessGroup des PowerShell-Cmdlets Enable-MbamWebApplication – agentservice an.

-   Konfigurieren Sie die Gruppe, nachdem der MBAM-Wiederherstellungs-und-Hardware Dienst installiert wurde, indem Sie die web.config-Datei im &lt; Inetpub &gt; \\Microsoft BitLocker Management Solution\\Recovery-und Hardware Service\\-Ordner bearbeiten.

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    wobei &lt; GroupName durch &gt; die Domäne und den Gruppennamen (oder den einzelnen Benutzer) ersetzt wird, der verwendet wird, um die Datenmigration aus Active Directory zu ermöglichen.

-   Verwenden Sie den Konfigurations-Editor in IIS-Manager, um diesen appSetting zu bearbeiten.

Im folgenden Beispiel wird der Befehl, wenn er als Mitglied der Gruppe "ADRecoveryInformation" und "Benutzer der Daten Migration" ausgeführt wird, die Datenträger Wiederherstellungsinformationen von Computern in der Organisationseinheit der Arbeitsstationen in der contoso.com-Domäne abrufen und mithilfe des MBAM-Wiederherstellungs-und-Hardware Diensts, der auf dem mbam.contoso.com-Server ausgeführt wird, in MBAM schreiben.

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

**Read-AD \ * Cmdlets** akzeptieren den Namen oder die IP-Adresse eines Active Directory-Hostservers, um nach Wiederherstellungs-oder TPM-Informationen abzufragen. Wir empfehlen, die Distinguished Names der AD-Container anzugeben, in denen sich das Computerobjekt befindet, als den Wert des SearchBase-Parameters. Wenn Computer über mehrere OUs gespeichert werden, können die Cmdlets Pipelineeingaben akzeptieren, damit Sie einmal für jeden Container ausgeführt werden. Der Distinguished Name eines anzeigen Containers sieht ähnlich wie ou = machines, DC = contoso, DC = com aus. Das Durchführen einer Suche, die auf bestimmte Container ausgerichtet ist, bietet die folgenden Vorteile:

-   Verringert das Risiko von Timeout beim Abfragen eines umfangreichen AD-Datasets für Computerobjekte.

-   Sie können OUs mit Rechenzentrums Servern oder anderen Computerklassen auslassen, für die die Sicherung möglicherweise nicht erwünscht oder erforderlich ist.

Eine weitere Möglichkeit besteht darin, das-recurse-Flag mit oder ohne den optionalen SearchBase bereitzustellen, um in allen Containern unter dem angegebenen SearchBase oder der gesamten Domäne nach Computerobjekten zu suchen. Wenn Sie das-recurse-Flag verwenden, können Sie auch den-MaxPageSize-Parameter verwenden, um die Menge an lokalem und Remotespeicher zu steuern, die zum Service der Abfrage erforderlich ist.

Diese Cmdlets schreiben in die Pipelineobjekte des Typs PsObject. Jede PsObject-Instanz enthält einen einzelnen Volume-Wiederherstellungsschlüssel oder eine TPM-Besitzer Zeichenfolge mit dem zugehörigen Computernamen, Zeitstempel und anderen Informationen, die für die Veröffentlichung im MBAM-Datenspeicher erforderlich sind.

**Write-mbam \ * Cmdlets** akzeptieren die Parameterwerte für Wiederherstellungsinformationen aus der Pipeline nach dem Eigenschaftennamen. Auf diese Weise können die Write-mbam \ *-Cmdlets die Pipelineausgabe der Read-AD \ *-Cmdlets akzeptieren (beispielsweise Read-ADRecoveryInformation – Server Contoso.com – Rekursion | Write-MbamRecoveryInformation – RecoveryServiceEndpoint mbam.contoso.com).

Die **Cmdlets Write-mbam \ *** enthalten optionale Parameter, die Optionen für Fehlertoleranz, ausführliche Protokollierung und Einstellungen für WhatIf und Confirm bereitstellen.

Die **Cmdlets für Write-mbam \ *** umfassen auch einen optionalen *Zeit* Parameter, dessen Wert ein **DateTime** -Objekt ist. Dieses Objekt enthält ein *Kind* -Attribut, das auf, oder festgesetzt werden kann `Local` `UTC` `Unspecified` . Wenn der *Zeit* Parameter aus den aus Active Directory übernommenen Daten ausgefüllt wird, wird die Uhrzeit in UTC konvertiert, und das Attribut *Art* wird automatisch auf gesetzt `UTC` . Wenn Sie jedoch den *Zeit* Parameter mit einer anderen Quelle, wie etwa einer Textdatei, füllen, müssen Sie das *Kind* -Attribut explizit auf seinen geeigneten Wert setzen.

**Hinweis**  Die "Read-AD \ *"-Cmdlets können nicht die Benutzerkonten ermitteln, die die Computer Benutzer darstellen. Benutzerkonten Zuordnungen sind für Folgendes erforderlich:

-   Benutzer zum Wiederherstellen von Volume-Kennwörtern/-Paketen mithilfe des Self-Service-Portals

-   Benutzer, die sich nicht in der Sicherheitsgruppe "Erweiterter Helpdesk-Benutzer" von MBAM befinden, wie Sie während der Installation definiert sind, wiederherstellen im Auftrag anderer Benutzer

 

## <a href="" id="bkmk-autounlock"></a>Konfigurieren von MBAM so, dass das TPM nach einer Sperrung automatisch freigegeben wird


Sie können MBAM 2,5 SP1 so konfigurieren, dass das TPM im Falle einer Sperrung automatisch freigegeben wird. Wenn TPM-Sperrungs-Auto-Reset aktiviert ist, kann MBAM feststellen, dass ein Benutzer gesperrt ist, und das OwnerAuth-Kennwort aus der MBAM-Datenbank abrufen, um das TPM automatisch für den Benutzer zu entsperren. Das automatische Zurücksetzen der TPM-Sperrung steht nur zur Verfügung, wenn der Betriebssystem Wiederherstellungsschlüssel für diesen Computer über das Self-Service-Portal oder die Website Verwaltung und Überwachung abgerufen wurde.

**Wichtig**  Zum Aktivieren der automatischen Zurücksetzung des TPM-Lockouts müssen Sie dieses Feature sowohl auf der Serverseite als auch in den Gruppenrichtlinien auf der Clientseite konfigurieren.

 

-   Wenn Sie das automatische Zurücksetzen der TPM-Sperrung auf der Clientseite aktivieren möchten, konfigurieren Sie die Gruppenrichtlinieneinstellung "Automatisches Zurücksetzen der TPM-Sperrung" unter **Computer Konfiguration** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM** - &gt; **Clientverwaltung**.

-   Wenn Sie das automatische Zurücksetzen der TPM-Sperrung auf der Serverseite aktivieren möchten, können Sie im MBAM-Serverkonfigurations-Assistenten während des Setups die Option "Automatisches Zurücksetzen von TPM-Sperrung aktivieren" aktivieren.

    Sie können das automatische Zurücksetzen der TPM-Sperrung in PowerShell auch aktivieren, indem Sie beim Aktivieren der Agentendienst-Webkomponente den Schalter "-TPM-Sperrungs-Auto-Reset" angeben.

Nachdem ein Benutzer den BitLocker-Wiederherstellungsschlüssel eingegeben hat, den er über das Self-Service-Portal oder die Website Verwaltung und Überwachung erhalten hat, ermittelt der MBAM-Agent, ob das TPM gesperrt ist. Wenn Sie gesperrt ist, wird versucht, die TPM-OwnerAuth für den Computer aus der MBAM-Datenbank abzurufen. Wenn die TPM-OwnerAuth erfolgreich abgerufen wurde, wird Sie zum Entsperren des TPMs verwendet. Wenn Sie das TPM entsperren, ist das TPM voll funktionsfähig, und der Benutzer wird nicht gezwungen, das Wiederherstellungskennwort bei nachfolgenden Neustarts aus einer TPM-Sperrung einzugeben.

Das automatische Zurücksetzen von TPM-Sperrungen ist standardmäßig deaktiviert.

**Hinweis**  Das automatische Zurücksetzen der TPM-Sperrung wird nur auf Computern unterstützt, auf denen TPM-Version 1,2 ausgeführt wird. TPM 2,0 bietet integrierte Funktionen zum automatischen Zurücksetzen von Sperren.

 

**Der Wiederherstellungs Überwachungsbericht** enthält Ereignisse im Zusammenhang mit dem automatischen Zurücksetzen der TPM-Sperrung. Wenn vom MBAM-Client eine Anforderung zum Abrufen eines TPM-OwnerAuth-Kennworts getroffen wird, wird ein Ereignis protokolliert, um die Wiederherstellung anzuzeigen. Überwachungseinträge sind die folgenden Ereignisse:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Eintrag</th>
<th align="left">Wert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Überwachungs Anforderungsquelle</p></td>
<td align="left"><p>Agent-TPM-Sperrung</p></td>
</tr>
<tr class="even">
<td align="left"><p>Schlüsseltyp</p></td>
<td align="left"><p>TPM-Kenn Wort Hash</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Beschreibung des Grunds</p></td>
<td align="left"><p>TPM-Reset</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a>Sichere Verbindungen mit SQL Server


In MBAM kommuniziert SQL Server mit SQL Server Reporting Services und mit den Webdiensten für die Websiteverwaltung und Überwachung sowie Self-Service-Portal. Wir empfehlen, die Kommunikation mit SQL Server zu sichern. Weitere Informationen finden Sie unter [Verschlüsseln von Verbindungen mit SQL Server](https://technet.microsoft.com/library/ms189067.aspx).

Weitere Informationen zum Sichern der MBAM-Websites finden Sie unter [Planen der Sicherung der MBAM-Websites](planning-how-to-secure-the-mbam-websites.md).

## <a href="" id="bkmk-accts-groups"></a>Erstellen von Konten und Gruppen


Die bewährte Methode zum Verwalten von Benutzerkonten ist das Erstellen globaler Domänengruppen und das Hinzufügen von Benutzerkonten. Eine Beschreibung der empfohlenen Konten und Gruppen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md).

## <a href="" id="bkmk-logfiles"></a>Verwenden von MBAM-Protokolldateien


In diesem Abschnitt werden die MBAM Server-und MBAM-Client Protokolldateien beschrieben.

**MBAM Server Setup-Protokolldateien**

Die **MBAMServerSetup.exe** -Datei generiert die folgenden Protokolldateien im Ordner " **% Temp%** " des Benutzers während der MBAM-Installation:

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 Numbers &gt; . log**

    Protokolliert die Aktionen, die während des MBAM-Setups und der MBAM Server-Feature-Konfiguration ausgeführt wurden.

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _Numbers &gt;\_0\_MBAMServer.msi. log**

    Protokolliert zusätzliche während der Installation durchgeführte Aktionen.

**MBAM Server-Konfigurationsprotokoll Dateien**

-   **Anwendungen und Dienstprotokolle/Microsoft Windows/MBAM-Setup**

    Protokolliert die Fehler, die auftreten, wenn Sie Windows PowerShell-Cmdlets verwenden, oder den MBAM-Serverkonfigurations-Assistenten, um die MBAM-Server Features zu konfigurieren.

**MBAM-Client Setup-Protokolldateien**

-   **MSI &lt; fünf zufällige Zeichen &gt; . log**

    Protokolliert die während der MBAM-Client Installation ausgeführten Aktionen.

**MBAM-Web-Protokolldateien**

-   Zeigt Aktivitäten aus den Webportalen und-Diensten an.

## <a href="" id="bkmk-tde"></a>Überlegungen zu MBAM Database DSA


Das in SQL Server verfügbare Feature "transparente Datenverschlüsselung (DSA)" ist eine optionale Installation für die Datenbankinstanzen, in denen die MBAM-Datenbankfeatures gehostet werden.

Mit DSA können Sie die vollständige Verschlüsselung auf Datenbankebene in Echtzeit durchführen. DSA ist die optimale Lösung für die Massenverschlüsselung, um behördliche Compliance-oder Unternehmensdaten Sicherheitsstandards zu erfüllen. DSA funktioniert auf der Dateiebene, die zwei Windows-Features ähnelt: EFS (Encrypting File System) und BitLocker-Laufwerkverschlüsselung. Beide Funktionen verschlüsseln auch Daten auf der Festplatte. DSA ersetzt nicht die Verschlüsselung auf Zellenebene, EFS oder BitLocker.

Wenn DSA für eine Datenbank aktiviert ist, werden alle Sicherungen verschlüsselt. Daher muss besonders darauf geachtet werden, dass das zum Schützen des Datenbank-Verschlüsselungsschlüssels verwendete Zertifikat mit der Datenbanksicherung gesichert und verwaltet wird. Wenn dieses Zertifikat (oder Zertifikate) verloren geht, sind die Daten nicht lesbar.

Sichern Sie das Zertifikat mit der Datenbank. Für jede Zertifikat Sicherung sollten zwei Dateien vorhanden sein. Beide Dateien sollten archiviert werden. Idealerweise sollten Sie für die Sicherheit separat von der Datenbanksicherungsdatei gesichert werden. Alternativ können Sie die erweiterbare Schlüssel Verwaltungsfunktion (Extensible Key Management, erweiterbare Schlüsselverwaltung) für die Speicherung und Wartung von Schlüsseln verwenden, die für DSA verwendet werden.

Ein Beispiel für die Aktivierung von DSA für MBAM-Datenbankinstanzen finden Sie unter [Grundlegendes zur transparenten Datenverschlüsselung (DSA)](https://technet.microsoft.com/library/bb934049.aspx).

## <a href="" id="bkmk-general-security"></a>Grundlegendes zu allgemeinen Sicherheitsüberlegungen


**Grundlegendes zu den Sicherheitsrisiken** Das schwerwiegendste Risiko bei der Verwendung der Microsoft BitLocker-Verwaltung und-Überwachung besteht darin, dass die Funktionalität von einem nicht autorisierten Benutzer beeinträchtigt werden kann, der dann die BitLocker-Laufwerkverschlüsselung neu konfigurieren und BitLocker-Verschlüsselungsschlüssel Daten auf MBAM-Clients erhalten kann. Der Verlust von MBAM-Funktionen für kurze Zeit aufgrund eines Denial-of-Service-Angriffs hat jedoch im Allgemeinen keine katastrophalen Auswirkungen, wie beispielsweise das verlieren von e-Mail-oder Netzwerkkommunikation oder der Stromversorgung.

**Physisches sichern ihrer Computer**. Es gibt keine Sicherheit ohne physische Sicherheit. Ein Angreifer, der physischen Zugriff auf einen MBAM-Server erhält, kann ihn potenziell zum Angriff auf die gesamte Clientbasis verwenden. Alle potenziellen körperlichen Angriffe müssen als Risiko behaftet und entsprechend verringert werden. MBAM-Server sollten in einem sicheren Serverraum mit kontrolliertem Zugriff gespeichert werden. Sichern Sie diese Computer, wenn Administratoren physisch nicht anwesend sind, indem Sie das Betriebssystem sperren oder einen sicheren Bildschirmschoner verwenden.

**Wenden Sie die neuesten Sicherheitsupdates auf alle Computer an**. Informieren Sie sich über neue Updates für Windows-Betriebssysteme, SQL Server und MBAM, indem Sie den Sicherheitsbenachrichtigungsdienst im [Security TechCenter](https://go.microsoft.com/fwlink/?LinkId=28819)abonnieren.

**Verwenden Sie sichere Kennwörter oder Passphrasen**. Verwenden Sie immer sichere Kennwörter mit 15 oder mehr Zeichen für alle MBAM-Administratorkonten. Verwenden Sie niemals leere Kennwörter. Weitere Informationen zu Kenn Wort Konzepten finden Sie unter [Kennwortrichtlinien](https://technet.microsoft.com/library/hh994572.aspx).



## Verwandte Themen


[Planen der Bereitstellung von MBAM 2.5](planning-to-deploy-mbam-25.md)

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





