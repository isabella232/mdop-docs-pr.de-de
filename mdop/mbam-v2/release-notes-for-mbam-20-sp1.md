---
title: Versionshinweise für MBAM 2.0SP1
description: Versionshinweise für MBAM 2.0SP1
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811242"
---
# Versionshinweise für MBAM 2.0SP1


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 Service Pack 1 (SP1) installieren. Diese Versionshinweise enthalten Informationen, die erforderlich sind, um die BitLocker-Verwaltung und-Überwachung 2,0 SP1 erfolgreich zu installieren, und Sie enthalten Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderen MBAM 2,0 SP1-Dokumentationen gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> Bekannte Probleme mit MBAM 2,0 SP1


Dieser Abschnitt enthält bekannte Probleme bei MBAM 2,0 SP1.

### Upgrade von MBAM mit der integrierten Configuration Manager-Topologie auf MBAM 2,0 SP1 erfordert das manuelle Entfernen von Configuration Manager-Objekten

Wenn Sie MBAM mit Configuration Manager verwenden und ein Upgrade auf MBAM 2,0 SP1 durchführen möchten, müssen Sie alle Configuration Manager-Objekte, die in Configuration Manager installiert wurden, als Teil der MBAM-Installation manuell entfernen. Bei den Objekten, die Sie manuell entfernen müssen, handelt es sich um die MBAM-Berichte, die MBAM-unterstützten Computersammlung und die BitLocker-Schutz Konfigurationsbasislinie und die zugehörigen Konfigurationselemente.

**Problemumgehung**: Aktualisieren Sie die Configuration Manager-Objekte, indem Sie die folgenden Schritte ausführen:

1.  Sichern Sie vorhandene Kompatibilitätsdaten in einer externen Datei, wie in den folgenden Schritten beschrieben.

    **Hinweis**  Alle vorhandenen BitLocker-Konformitätsdaten werden gelöscht, wenn Sie den vorhandenen Basisplan in Configuration Manager löschen. Die Daten werden im Laufe der Zeit neu generiert, es wird jedoch empfohlen, dass Sie eine Kopie der Daten speichern, falls Sie die Kompatibilitätsdaten für einen bestimmten Computer benötigen, bevor die Kompatibilitätsdaten erneut generiert wurden.

     

    1.  Zum Speichern von Verlaufsdaten zur BitLocker-Konformität öffnen Sie den **BitLocker Enterprise Compliance-Detail** Bericht.

    2.  Klicken Sie im Bericht auf das Symbol **Speichern** , und wählen Sie **Excel**aus.

        Der gespeicherte Bericht enthält Daten wie den Computernamen, den Domänennamen, den Kompatibilitätsstatus, die Ausnahme, die Geräte Benutzer, die Details zum Kompatibilitätsstatus und das Datum/die Uhrzeit des letzten Kontakts. Einige Informationen wie detaillierte Lautstärke Informationen und Verschlüsselungsstärke werden nicht gespeichert.

2.  Deinstallieren Sie **MBAM** vom Server mithilfe des **MBAM** -Installationsprogramms.

3.  Löschen Sie die folgenden Objekte manuell aus Configuration Manager:

    -   MBAM-unterstützte Computersammlung

    -   BitLocker-Schutz Basislinie

    -   BitLocker-Betriebs System-Laufwerkschutz-Konfigurationselement

    -   BitLocker-Konfigurationselement "Fixed Data Drives Protection"

4.  Löschen Sie den Ordner MBAM Reports auf der Configuration Manager-SQL Server Reporting Services-Website manuell. Gehen Sie dazu folgendermaßen vor:

    1.  Verwenden Sie Internet Explorer, um zum Reporting Services-Punkt zu navigieren, beispielsweise http:// &lt; yourcmserver &gt; /Reports.

    2.  Klicken Sie auf den entsprechenden Link für Configuration Manager-Standortcode.

    3.  Löschen Sie den Ordner MBAM.

5.  Verwenden Sie das MBAM-Server Installationsprogramm, um die Configuration Manager-Integrationsobjekte erneut zu installieren. Auf den Clientcomputern werden die BitLocker-Kompatibilitätsdaten mit der Zeit erneut hochgeladen.

### Schaltfläche "Senden" im Self-Service-Portal funktioniert nicht in Internet Explorer10

Wenn Sie die Internet-Explorer10 für den Zugriff auf die Website "Verwaltung und Überwachung" verwenden, funktioniert die Schaltfläche " **senden** " auf der Website nicht.

**Problemumgehung**: Installieren Sie auf dem Server, auf dem Sie die Verwaltungs-und Überwachungs Website installiert haben, [Hotfix für ASP.net-Browserdefinitionsdateien](https://go.microsoft.com/fwlink/?LinkId=317798).

### Internationale Domänennamen werden nicht unterstützt.

MBAM 2,0 SP1 unterstützt keine internationalen Domänennamen.

**Problemumgehung**: keine.

### Berichte auf der Website "Verwaltung und Überwachung" zeigen eine Warnung an, wenn SSL in SSRS nicht konfiguriert ist

Wenn SQLServer Reporting Services (SSRS) nicht für die Verwendung von Secure Socket Layer (SSL) konfiguriert wurde, wird die URL für die Berichte bei der Installation des MBAM-Servers auf http statt auf HTTPS festgelegt. Wenn Sie dann zur Websiteverwaltung und Überwachung navigieren und einen Bericht auswählen, wird die folgende Meldung angezeigt: "nur sicherer Inhalt wird angezeigt."

**Problemumgehung**: um dieses Problem zu beheben, konfigurieren Sie SSL im **Reporting Services-Konfigurations-Manager** auf dem MBAM-Server, auf dem SQLServer Reporting Services installiert ist. Deinstallieren Sie die Verwaltungs-und Monitoring Server-Website, und installieren Sie Sie erneut.

### Wenn Sie im Kompatibilitäts Zusammenfassungsbericht auf Zurück klicken, wird möglicherweise ein Fehler erstellt

Wenn Sie einen Drilldown in einen Kompatibilitäts Zusammenfassungsbericht ausführen und dann im SSRS-Bericht auf den Link **zurück** klicken, kann ein Fehler auftreten.

**Problemumgehung**: keine.

### Verwendeter Speicherplatz nur die Verschlüsselung funktioniert nicht ordnungsgemäß

Wenn Sie einen Computer nach der Installation des MBAM-Clients zum ersten Mal verschlüsseln und ein Gruppenrichtlinienobjekt für die Implementierung der nur verwendeter Speicherplatz Verschlüsselung festgesetzt haben, verschlüsselt MBAM fälschlicherweise den gesamten Datenträger, anstatt nur den verwendeten Speicherplatz der Festplatte zu verschlüsseln. Wenn ein Computer bereits mit verwendeter Speicherplatz Verschlüsselung verschlüsselt ist, bevor Sie den MBAM-Client installieren, und Sie das Gruppenrichtlinienobjekt "nur verwendeter Speicherplatz Verschlüsselung" festgelegt haben, erkennt MBAM die Einstellung und meldet die Verschlüsselung in den Konformitätsberichten ordnungsgemäß.

**Problemumgehung**: keine.

### Die Verschlüsselungsstärke wird im Computer Kompatibilitätsbericht falsch angezeigt

Wenn Sie keine bestimmte Verschlüsselungsstärke in den Gruppenrichtlinienobjekten **"Laufwerksverschlüsselung auswählen" und "Verschlüsselungsstärke"** festlegen, wird der Computer Kompatibilitätsbericht in der integrierten Configuration Manager-Topologie immer für die Verschlüsselungsstärke **unbekannt** angezeigt, selbst wenn die Verschlüsselungsstärke den Standardwert der 128-Bit-Verschlüsselung verwendet. Der Bericht zeigt die richtige Verschlüsselungsstärke an, wenn Sie eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt festlegen.

**Problemumgehung**: Legen Sie immer eine bestimmte Verschlüsselungsstärke im Gruppenrichtlinienobjekt **Auswählen von Laufwerk Verschlüsselungsmethode und Verschlüsselungsstärke** fest.

### Kompatibilitäts Status Verteilung nach Laufwerks zeigt alte Daten an, nachdem Sie Konfigurationselemente aktualisiert haben

Nachdem Sie MBAM-Konfigurationselemente in SystemCenter2012 ConfigurationManager aktualisiert haben, werden auf dem BitLocker Enterprise Compliance-Dashboard Daten angezeigt, die auf Informationen aus älteren Versionen der Konfigurationselemente basieren.

**Problemumgehung**: keine. Änderungen der MBAM-Konfigurationselemente werden nicht unterstützt, und der Bericht wird möglicherweise nicht wie erwartet angezeigt.

### Verbesserte Sicherheitskonfiguration kann dazu führen, dass Berichte falsch angezeigt werden

Wenn Internet Explorer Enhanced Security Configuration (ESC) aktiviert ist, wird möglicherweise eine Meldung für den **Zugriff verweigert** angezeigt, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen. Standardmäßig ist die erweiterte Sicherheitskonfiguration aktiviert, um den Server zu schützen, indem die Anfälligkeit des Servers für potenzielle Angriffe verringert wird, die über Webinhalte und Anwendungsskripts auftreten können.

**Problemumgehung**: Wenn die Meldung " **Zugriff verweigert** " angezeigt wird, wenn Sie versuchen, Berichte auf dem MBAM-Server anzuzeigen, können Sie ein Gruppenrichtlinienobjekt festlegen oder den Standardwert manuell in Ihrem Bild ändern, um die erweiterte Sicherheitskonfiguration zu deaktivieren. Sie können auch die Berichte auf einem anderen Computer anzeigen, auf dem die erweiterte Sicherheitskonfiguration nicht aktiviert ist.

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> MBAM Server-Installation schlägt fehl, wenn Sie von SQLServer2008 auf SQLServer2012 aktualisieren

Wenn Sie ein Upgrade von SQLServer2008 auf SQLServer2012 durchführen und dann versuchen, die Konformitäts-und Überwachungsdatenbank oder die Wiederherstellungsdatenbank zu installieren, schlägt die Installation fehl, und es wird ein Rollback ausgeführt. Der Fehler tritt auf, weil die erforderliche SQLCMD.exe Datei während des SQLServer-Upgrades entfernt wurde und vom MBAM-Installationsprogramm nicht gefunden werden kann. Die MSI-Protokolldateizeilen können wie folgt aussehen:

RunDbInstallScript Recovery DB ca: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery DB ca: dbinstance-xxxxxx\\I01RunDbInstallScript Recovery DB ca: SqlScript-c:\\Programme Files\\Microsoft\\Microsoft BitLocker-Verwaltung und Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB ca: dbname-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript Recovery DB ca: DefaultFileName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript Recovery DB ca: defaultDataPath-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript Recovery DB ca: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript Recovery DB ca: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-e-S xxxxxxx\\I01-i "c:\\Programme Files\\Microsoft\\Microsoft BitLocker-Verwaltung und Monitoring\\Setup\\KeyRecovery.SQL"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery DB ca: Starten der Ausführung der Wiederherstellungs-Datenbank installieren scriptRunDbInstallScript Recovery DB ca: die sqlcmd-Protokolldatei befindet sich in der C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript-Wiederherstellungs-DB-ca-Ausnahme: benutzerdefinierte Aktion der Wiederherstellungsdatenbank-Befehlszeile-Ausgabe Ausnahme: das System kann die angegebene Datei nicht finden

Der MBAM-Server-Windows-Installer ist hart codiert, um den SQLCMD.exe Pfad zu finden, indem Sie den Pfadzeichen folgen Wert in der Registrierung unter HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup. Während der Migration von SQLServer2008 zu SQLServer2012 ist der Schlüssel weiterhin vorhanden, doch der Pfad, auf den der Datenwert verweist, enthält nicht die SQLCMD.exe-Datei, da die Datei vom sqlupgradeprozess entfernt wurde.

**Problemumgehung**: benennen Sie den HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup Path-Zeichenfolgenwert vorübergehend in **path \ _old**um, und führen Sie dann Windows Installer auf dem MBAM-Server erneut aus. Wenn die Installation erfolgreich abgeschlossen wurde und die Datenbanken in SQLServer2012 erstellt werden, benennen Sie den **Pfad \ _old** in **path**um.

## Hotfixes und Knowledge Base-Artikel für MBAM 2,0 SP1


Dieser Abschnitt enthält Hotfixes und KB-Artikel für MBAM 2,0 SP1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>KB-Artikel</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>Das Installieren der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 schlägt fehl, wenn &quot; System Center cm-Objekte bereits installiert sind&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>Benutzer können den BitLocker-Wiederherstellungsschlüssel nicht über das Self-Service-Portal von mbam 2.0 abrufen</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>MBAM-Client schlägt mit Ereignis-ID 4 und Fehlercode 0x8004100E in der Ereignisbeschreibung fehl</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>Fehlermeldung "Server Fehler in der Anwendung"/Reports ", wenn Sie in MBAM auf die Registerkarte" Berichte "klicken</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Fehler beim Öffnen von Enterprise-oder Computer Kompatibilitätsberichten in MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM Enterprise-Berichte werden nicht aktualisiert</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>Die Installation von MBAM auf einem Domänen Controller wird nicht unterstützt.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>Sie erhalten Fehlercode 0x80071a90 während des Standalone-oder Configuration Manager-Integrations Setups von mbam 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM und sichere Netzwerkkommunikation</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>Mbam 2.0-Setup schlägt während des Configuration Manager-Integrationsszenarios mit SQL Server 2008 fehl</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>MBAM-Setup schlägt fehl, wenn SQL SSRS nicht ordnungsgemäß konfiguriert ist</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>MBAM 2,0-Setup schlägt fehl, wenn &quot; Fehler beim Abrufen der Configuration Manager-Server Rolleneinstellungen für &#39;Reporting Services-Point&#39; Rolle auftreten&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>Mbam 2.0-Enterprise-Berichte werden in der eigenständigen mbam 2.0-Topologie aufgrund des SQL-Auftrags createcache-Fehlers nicht aktualisiert</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM Enterprise-Berichte werden nicht aktualisiert</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>Kompatibilitätsberichte von MBAM-unterstützten Computern enthalten fehlerhafte nicht unterstützte Produkte</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>Der Computer Eintrag wird in MBAM abgelehnt.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Infos zu MBAM 2.0 SP1](about-mbam-20-sp1.md)

 

 





