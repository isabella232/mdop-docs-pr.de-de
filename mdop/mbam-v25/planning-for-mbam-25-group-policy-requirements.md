---
title: Planen der Gruppenrichtlinienanforderungen für MBAM 2.5
description: Planen der Gruppenrichtlinienanforderungen für MBAM 2.5
author: dansimp
ms.assetid: 82d545dc-3fbf-4b46-b62f-47fe178a7c44
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4beeb9f88f16e7d48d145861c398a90fa29f3491
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810153"
---
# Planen der Gruppenrichtlinienanforderungen für MBAM 2.5


Verwenden Sie die folgenden Informationen, um die Typen von BitLocker-Beschützern zu ermitteln, die Sie zum Verwalten der Microsoft BitLocker-MBAM-Clientcomputer in Ihrem Unternehmen verwenden können.

## Typen von BitLocker-Beschützern, die von MBAM unterstützt werden


MBAM unterstützt die folgenden Typen von BitLocker-Beschützern.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Typ des Laufwerks oder Volumes</th>
<th align="left">Unterstützte BitLocker-Schutzvorrichtungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Betriebssystem-Volumes</p></td>
<td align="left"><ul>
<li><p><strong>Trusted Platform Module (TPM)</strong></p></li>
<li><p><strong>TPM + PIN</strong></p></li>
<li><p><strong>TPM + USB </strong> -Schlüssel – wird nur unterstützt, wenn das Betriebssystemvolume verschlüsselt ist, bevor MBAM installiert wird.</p></li>
<li><p><strong>TPM + PIN + USB-Taste wird </strong> - nur unterstützt, wenn das Betriebssystemvolume verschlüsselt ist, bevor MBAM installiert wird.</p></li>
<li><p><strong>Kennwort, </strong> - das nur für Windows to go-Geräte, fest Netzlaufwerke und Windows 8-, Windows 8,1-und Windows 10-Geräte unterstützt wird, die kein TPM besitzen</p></li>
<li><p><strong>Numerisches Kennwort wird </strong> - automatisch als Teil der Datenträgerverschlüsselung angewendet und muss nicht konfiguriert werden, mit Ausnahme des FIPS-Modus unter Windows 7</p></li>
<li><p><strong>Daten Wiederherstellungs-Agent (DRA)</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Feste Datenlaufwerke</p></td>
<td align="left"><ul>
<li><p><strong>Kennwort</strong></p></li>
<li><p><strong>Automatisches entsperren</strong></p></li>
<li><p><strong>Numerisches Kennwort wird </strong> - automatisch als Teil der Datenträgerverschlüsselung angewendet und muss nicht konfiguriert werden, mit Ausnahme des FIPS-Modus unter Windows 7</p></li>
<li><p><strong>Daten Wiederherstellungs-Agent (DRA)</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Austauschbare Laufwerke</p></td>
<td align="left"><ul>
<li><p><strong>Kennwort</strong></p></li>
<li><p><strong>Automatisches entsperren</strong></p></li>
<li><p><strong>Numerisches Kennwort wird </strong> - automatisch als Teil der Datenträgerverschlüsselung angewendet und muss nicht konfiguriert werden</p></li>
<li><p><strong>Daten Wiederherstellungs-Agent (DRA)</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>



### Unterstützung für die BitLocker-Richtlinie für die verwendete Speicherverschlüsselung

Wenn Sie in MBAM 2,5 SP1 die gebrauchte Speicherplatz Verschlüsselung über BitLocker-Gruppenrichtlinien aktivieren, ehrt der MBAM-Client diesen.

Diese Gruppenrichtlinieneinstellung wird **auf Betriebssystemlaufwerken als Erzwingen des Laufwerk Verschlüsselungstyps** bezeichnet und befindet sich im folgenden GPO-Knoten: **Computerkonfigurations** - &gt; **Administrative Vorlagen** &gt; **Windows-Komponenten** &gt; **BitLocker Drive Encryption** - &gt; **Betriebssystemlaufwerke**. Wenn Sie diese Richtlinie aktivieren und den Verschlüsselungstyp als **nur verwendeter Speicherplatz Verschlüsselung**auswählen, wird die Richtlinie von MBAM berücksichtigt, und BitLocker verschlüsselt nur den auf dem Volume verwendeten Speicherplatz.

## Abrufen der MBAM-Gruppenrichtlinienvorlagen und Bearbeiten der Einstellungen


Wenn Sie bereit sind, die gewünschten MBAM-Gruppenrichtlinieneinstellungen zu konfigurieren, gehen Sie folgendermaßen vor:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Zu befolgende Schritte</th>
<th align="left">Wo erhalte ich Anweisungen?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Kopieren Sie die MBAM-Gruppenrichtlinienvorlagen aus <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> , wie Sie MDOP-Gruppenrichtlinien (ADMX)-Vorlagen abrufen </a> und auf einem Computer installieren können, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren Sie die Gruppenrichtlinieneinstellungen, die Sie in Ihrem Unternehmen verwenden möchten.</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>



## Beschreibungen der MBAM-Gruppenrichtlinieneinstellungen


Der **MDOP MBAM (BitLocker Management)-** GPO-Knoten enthält vier globale Richtlinieneinstellungen und vier untergeordnete GPO-Knoten: **Client Verwaltung**, **festes Laufwerk**, **Betriebs System Laufwerk**und **Wechsellaufwerk**. In den folgenden Abschnitten werden die Einstellungen für die Gruppenrichtlinieneinstellungen von MBAM beschrieben und vorgeschlagen.

**Wichtig**  
Ändern Sie die Gruppenrichtlinieneinstellungen im **BitLocker Drive Encryption** -Knoten nicht, oder MBAM wird nicht ordnungsgemäß funktionieren. MBAM konfiguriert die Einstellungen in diesem Knoten automatisch, wenn Sie die Einstellungen im **MDOP MBAM (BitLocker-Verwaltungsknoten)** konfigurieren.



### Definitionen globaler Gruppenrichtlinien

In diesem Abschnitt werden die Definitionen globaler MBAM-Gruppenrichtlinien auf dem folgenden GPO-Knoten beschrieben: **Computer Konfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker-Verwaltung)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinienname</th>
<th align="left">Übersicht und vorgeschlagene Gruppenrichtlinieneinstellungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Wählen Sie Laufwerk Verschlüsselungsmethode und Verschlüsselungsstärke aus.</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Konfigurieren Sie diese Richtlinie für die Verwendung einer bestimmten Verschlüsselungsmethode und Verschlüsselungsstärke.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, verwendet BitLocker die Standardverschlüsselungsmethode: AES 128-Bit mit Diffusor.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Ein Problem mit dem BitLocker-Computer Kompatibilitätsbericht führt dazu, dass es &quot; &quot; für die Verschlüsselungsstärke unbekannt angezeigt wird, auch wenn Sie den Standardwert verwenden. Um dieses Problem zu umgehen, stellen Sie sicher, dass Sie diese Einstellung aktivieren, und legen Sie einen Wert für Verschlüsselungsstärke fest.</p>
</div>
<div>

</div>
<ul>
<li><p>AES 128-Bit mit Diffusor – nur für Windows 7</p></li>
<li><p>AES 128 für Windows 8, Windows 8,1 und Windows 10</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Verhindern, dass beim Neustart Speicher überschrieben wird</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie, um die Neustart Leistung zu verbessern, ohne BitLocker-Geheimnisse beim Neustart überschreiben zu müssen.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, werden BitLocker-Geheimnisse aus dem Arbeitsspeicher entfernt, wenn der Computer neu gestartet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Überprüfen der Verwendungs Regel für Smartcard-Zertifikate</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie für die Verwendung von Smartcard-Zertifikat basiertem BitLocker-Schutz.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, wird die standardmäßige Objekt-ID 1.3.6.1.4.1.311.67.1.1 verwendet, um ein Zertifikat anzugeben.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bereitstellen der eindeutigen Bezeichner für Ihre Organisation</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie für die Verwendung eines zertifikatbasierten Daten Wiederherstellungs-Agents oder des BitLocker To Go-Readers.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, <strong> </strong> wird das Feld ID nicht verwendet.</p>
<p>Wenn in Ihrem Unternehmen höhere Sicherheitsmaße erforderlich sind, können Sie das Feld "Identifikation" so konfigurieren, <strong> </strong> dass alle USB-Geräte dieses Feld festgelegt haben, und dass Sie mit dieser Gruppenrichtlinieneinstellung ausgerichtet sind.</p></td>
</tr>
</tbody>
</table>



### Definitionen für Gruppenrichtlinien für Client Verwaltung

In diesem Abschnitt werden die Definitionen der clientverwaltungsrichtlinien für MBAM auf dem folgenden GPO-Knoten beschrieben: **Computerkonfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker-Verwaltung)** &gt; **Client Verwaltung**.

Sie können die gleichen Gruppenrichtlinieneinstellungen für die eigenständigen und System Center Configuration Manager-Integrations Topologien festlegen, mit einer Ausnahme: Deaktivieren Sie die Einstellung **MBAM Services &gt; MBAM Status Reporting Service Endpoint konfigurieren** , wenn Sie die Configuration Manager-Integrations Topologie verwenden, wie in der folgenden Tabelle angegeben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinienname</th>
<th align="left">Übersicht und vorgeschlagene Gruppenrichtlinieneinstellungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Konfigurieren von MBAM-Diensten</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<ul>
<li><p><strong>MBAM-Wiederherstellungs-und Hardware </strong> Dienstendpunkt Verwenden Sie diese Einstellung, um die MBAM-Client-BitLocker-Verschlüsselungs Verwaltung zu aktivieren. Geben Sie einen Endpunkt Speicherort ein, der dem folgenden Beispiel ähnelt: <strong> http (s):// </strong><em> &lt; MBAM Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; der Port, an den der Webdienst an/MBAMRecoveryAndHardwareService/CoreService.svc gebunden ist &gt; </em><strong> </strong> .</p></li>
<li><p><strong>Wählen Sie die zu speichernden BitLocker-Wiederherstellungsinformationen aus </strong> . Mit dieser Richtlinieneinstellung können Sie den Schlüssel Wiederherstellungs Dienst so konfigurieren, dass BitLocker-Wiederherstellungsinformationen gesichert werden. Darüber hinaus können Sie einen Statusberichts Dienst für das Sammeln von Berichten konfigurieren. Die Richtlinie stellt eine administrative Methode zur Verfügung, die von BitLocker verschlüsselte Daten zurückgibt, um Datenverluste aufgrund fehlender Schlüsselinformationen zu verhindern. Der Statusbericht und die Schlüssel Wiederherstellungs Aktivität werden automatisch und lautlos an den konfigurierten Speicherort des Berichtsservers gesendet.</p>
<p>Wenn Sie diese Richtlinieneinstellung nicht konfigurieren oder deaktivieren, werden die Schlüssel Wiederherstellungsinformationen nicht gespeichert, und der Statusbericht und die Schlüssel Wiederherstellungs Aktivität werden nicht an den Server gemeldet. Wenn diese Einstellung auf <strong> Wiederherstellungskennwort und Schlüsselpaket festgelegt ist </strong> , werden das Wiederherstellungskennwort und das Schlüsselpaket automatisch und lautlos auf dem konfigurierten Speicherort des Schlüssel Wiederherstellungs Servers gesichert.</p></li>
<li><p><strong>Geben Sie die Status Häufigkeit der Clientüberprüfung in Minuten ein </strong> . Diese Richtlinieneinstellung verwaltet, wie häufig der Client die BitLocker-Schutzrichtlinien und den Status auf dem Clientcomputer überprüft. Diese Richtlinie verwaltet auch die Häufigkeit, mit der der Client Kompatibilitätsstatus auf dem Server gespeichert wird. Der Client überprüft die BitLocker-Schutzrichtlinien und den Status auf dem Clientcomputer und stellt auch den Client Wiederherstellungsschlüssel unter der konfigurierten Häufigkeit sicher.</p>
<p>Legen Sie diese Häufigkeit basierend auf der Anforderung Ihres Unternehmens für die Häufigkeit der Überprüfung des Kompatibilitätsstatus des Computers und die Häufigkeit der Sicherung des Client Wiederherstellungsschlüssels auf.</p></li>
<li><p><strong>MBAM-Status Berichterstattungsdienst Endpunkt:</strong></p>
<p><strong>Für MBAM in einer eigenständigen Topologie </strong> : Sie müssen diese Einstellung so konfigurieren, dass die MBAM-Client-BitLocker-Verschlüsselungs Verwaltung aktiviert wird.</p>
<p>Geben Sie einen Endpunkt Speicherort ein, der mit dem folgenden Beispiel vergleichbar ist:</p>
<p><strong>http (s):// </strong><em> &lt; MBAM Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; der Port, an den der Webdienst gebunden ist &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.svc</strong></p>
<p><strong>Für MBAM in der Configuration Manager-Integrations Topologie </strong> : Deaktivieren Sie diese Einstellung.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren von Benutzer Freistellungs Richtlinien</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie eine Websiteadresse, e-Mail-Adresse oder Telefonnummer konfigurieren, die einen Benutzer anweist, eine Ausnahme von der BitLocker-Verschlüsselung anzufordern.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren und eine Websiteadresse, e-Mail-Adresse oder Telefonnummer angeben, wird ein Dialogfeld angezeigt, in dem die Benutzer Anweisungen zum beantragen einer Ausnahme vom BitLocker-Schutz erhalten. Weitere Informationen zum Aktivieren von BitLocker-Verschlüsselungs Ausnahmen für Benutzer finden Sie unter <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md)"> so wird es gemacht: Verwalten von Benutzer-BitLocker-Verschlüsselungs Ausnahmen </a> .</p>
<p>Wenn Sie diese Richtlinieneinstellung entweder deaktivieren oder nicht konfigurieren, werden die Anweisungen für die ausnahmeanforderung nicht für die Benutzer angezeigt.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Die Benutzer Befreiung wird pro Benutzer und nicht pro Computer verwaltet. Wenn sich mehrere Benutzer am gleichen Computer anmelden und ein Benutzer nicht freigestellt ist, wird der Computer verschlüsselt.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Programm zur Verbesserung der Benutzerfreundlichkeit konfigurieren</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie konfigurieren, wie MBAM-Benutzer an dem Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen können. Dieses Programm sammelt Informationen zur Computer Hardware und wie Benutzer MBAM verwenden, ohne Ihre Arbeit zu unterbrechen. Mithilfe dieser Informationen kann Microsoft ermitteln, welche MBAM-Features verbessert werden können. Microsoft verwendet diese Informationen nicht, um MBAM-Benutzer zu identifizieren oder zu kontaktieren.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, können Benutzer am Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren, können Benutzer nicht am Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen.</p>
<p>Wenn Sie diese Richtlinieneinstellung nicht konfigurieren, können Benutzer am Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Angeben der URL für den Link "Sicherheitsrichtlinie"</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Verwenden Sie diese Richtlinieneinstellung, um eine URL anzugeben, die Endbenutzern als Link " &quot; Unternehmenssicherheitsrichtlinie" angezeigt wird. &quot; Der Link verweist auf die internen Sicherheitsrichtlinien Ihres Unternehmens und stellt Endbenutzern Informationen zu den Verschlüsselungsanforderungen zur Verfügung. Der Link wird angezeigt, wenn Benutzer von MBAM aufgefordert werden, ein Laufwerk zu verschlüsseln.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, können Sie die URL für den Sicherheitsrichtlinien Link konfigurieren.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren oder nicht konfigurieren, wird der Link Sicherheitsrichtlinie für die Benutzer nicht angezeigt.</p></td>
</tr>
</tbody>
</table>



### Definitionen für Festplatten-Gruppenrichtlinien

In diesem Abschnitt werden die Definitionen fester Laufwerk Richtlinien für die Microsoft BitLocker-Verwaltung und-Überwachung auf dem folgenden GPO-Knoten beschrieben: **Computerkonfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker-Verwaltung)** &gt; **festes Laufwerk**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinienname</th>
<th align="left">Übersicht und vorgeschlagene Gruppenrichtlinieneinstellungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Einstellungen für die Verschlüsselung fester Datenlaufwerke</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie verwalten, ob fest Netzlaufwerke verschlüsselt werden müssen.</p>
<p>Wenn das Volume des Betriebssystems verschlüsselt werden muss, klicken Sie auf <strong> Automatisches Entsperren des festen Datenlaufwerks aktivieren </strong> .</p>
<p>Wenn Sie diese Richtlinie aktivieren, dürfen Sie die <strong> Richtlinie "Verwendung von Kennwort für feste Datenlaufwerke konfigurieren" nicht deaktivieren, </strong> es sei denn, Sie aktivieren oder erfordern die Verwendung der automatischen Sperrung für feste Datenlaufwerke.</p>
<p>Wenn Sie die automatische Sperrung für feste Datenlaufwerke verwenden müssen, müssen Sie die Betriebssystemdatenträger so konfigurieren, dass Sie verschlüsselt werden.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, müssen Benutzer alle festen Datenlaufwerke unter BitLocker-Schutz setzen, und die Datenlaufwerke werden dann verschlüsselt.</p>
<p>Wenn Sie diese Richtlinieneinstellung nicht konfigurieren, müssen Benutzer keine festen Datenlaufwerke unter BitLocker-Schutz speichern. Wenn Sie diese Richtlinie nach dem Verschlüsseln fester Datenlaufwerke anwenden, entschlüsselt der MBAM-Agent die verschlüsselten fest Netzlaufwerke.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren, können Benutzer ihre festen Datenlaufwerke nicht unter BitLocker-Schutz stellen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Schreibzugriff auf Festplattenlaufwerke verweigern, die nicht durch BitLocker geschützt sind</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Diese Richtlinieneinstellung bestimmt, ob ein BitLocker-Schutz erforderlich ist, damit feste Datenlaufwerke auf einem Computer beschreibbar sind. Diese Richtlinieneinstellung wird angewendet, wenn Sie BitLocker aktivieren.</p>
<p>Wenn die Richtlinie nicht konfiguriert ist, werden alle festen Datenlaufwerke auf dem Computer mit der Berechtigung "Lesen/Schreiben" bereitgestellt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gewähren des Zugriffs auf von BitLocker geschützte Festplatten aus früheren Versionen von Windows</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, damit Festplatten mit dem FAT-Dateisystem auf Computern, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird, freigegeben und angezeigt werden können.</p>
<p>Wenn die Richtlinie aktiviert oder nicht konfiguriert ist, können Festplatten, die mit dem FAT-Dateisystem formatiert sind, freigegeben werden und deren Inhalt auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird. Diese Betriebssysteme verfügen über eine Leseberechtigung für BitLocker-geschützte Laufwerke.</p>
<p>Wenn die Richtlinie deaktiviert ist, können feste Laufwerke, die mit dem FAT-Dateisystem formatiert sind, nicht entsperrt werden, und der Inhalt kann nicht auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren der Verwendung des Kennworts für feste Laufwerke</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Verwenden Sie diese Richtlinie, um anzugeben, ob ein Kennwort zum Entsperren von mit BitLocker geschützten festen Datenlaufwerken erforderlich ist.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, können Benutzer ein Kennwort konfigurieren, das die von Ihnen definierten Anforderungen erfüllt. BitLocker ermöglicht Benutzern das Entsperren eines Laufwerks mit einem der auf dem Laufwerk verfügbaren Schutzvorrichtungen.</p>
<p>Diese Einstellungen werden erzwungen, wenn Sie BitLocker aktivieren, nicht, wenn Sie ein Volume entsperren.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren, ist es Benutzern nicht gestattet, ein Kennwort zu verwenden.</p>
<p>Wenn die Richtlinie nicht konfiguriert ist, werden Kennwörter mit den Standardeinstellungen unterstützt, die keine Anforderungen an die Kennwortkomplexität enthalten und nur acht Zeichen erfordern.</p>
<p>Aktivieren Sie für höhere Sicherheit diese Richtlinie, und wählen Sie dann <strong> Kennwort für festes Datenlaufwerk anfordern aus </strong> , klicken Sie auf <strong> Kennwortkomplexität anfordern </strong> , und legen Sie die <strong> gewünschte minimale Kennwortlänge fest </strong> .</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren, ist es Benutzern nicht gestattet, ein Kennwort zu verwenden.</p>
<p>Wenn Sie diese Richtlinieneinstellung nicht konfigurieren, werden Kennwörter mit den Standardeinstellungen unterstützt, die keine Anforderungen an die Kennwortkomplexität enthalten und nur acht Zeichen erfordern.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswählen, wie BitLocker-geschützte Festplatten wiederhergestellt werden können</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie, um den BitLocker-Daten Wiederherstellungs-Agent zu aktivieren oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) zu speichern.</p>
<p>Wenn die Richtlinie nicht konfiguriert ist, ist der BitLocker-Daten Wiederherstellungs-Agent zulässig, und Wiederherstellungsinformationen werden nicht in AD DS gesichert. Für MBAM müssen keine Wiederherstellungsinformationen in AD DS gesichert werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Einstellungen für die Verschlüsselungsrichtlinien Erzwingung</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Verwenden Sie diese Richtlinieneinstellung, um die Anzahl von Tagen zu konfigurieren, die fest Netzlaufwerke nicht kompatibel bleiben können, bis Sie gezwungen sind, die MBAM-Richtlinien einzuhalten. Benutzer können die erforderliche Aktion nicht verschieben oder nach der Nachfrist eine Befreiung davon anfordern. Die Kulanzzeit beginnt, wenn festgestellt wird, dass das fest Netzlaufwerk nicht kompatibel ist. Die Richtlinie für feste Datenlaufwerke wird jedoch erst erzwungen, wenn das Betriebssystemlaufwerk kompatibel ist.</p>
<p>Wenn die Nachfrist abgelaufen ist und das festgelegte Datenlaufwerk weiterhin nicht kompatibel ist, haben Benutzer nicht die Möglichkeit, eine Ausnahme zu verschieben oder zu beantragen. Wenn für den Verschlüsselungsprozess Benutzereingaben erforderlich sind, wird ein Dialogfeld angezeigt, das Benutzer nicht schließen können, bis Sie die erforderlichen Informationen bereitstellen.</p>
<p>Geben <strong> Sie </strong> im Feld <strong> Konfigurieren der Kulanzzeit für nicht Konformitäts Tage für feste Laufwerke den Wert 0 ein </strong> , um zu erzwingen, dass der Verschlüsselungsprozess unmittelbar nach Ablauf des Kulanzzeitraums für das Betriebssystemlaufwerk beginnt.</p>
<p>Wenn Sie diese Einstellung deaktivieren oder nicht konfigurieren, sind die Benutzer nicht gezwungen, die MBAM-Richtlinien einzuhalten.</p>
<p>Wenn zum Hinzufügen eines Beschützers keine Benutzerinteraktion erforderlich ist, beginnt die Verschlüsselung im Hintergrund, nachdem die Kulanzzeit abgelaufen ist.</p></td>
</tr>
</tbody>
</table>



### Gruppenrichtlinien Definitionen für das Betriebs System Laufwerk

In diesem Abschnitt werden die Richtlinien Definitionen für das Betriebssystemlaufwerk für die Microsoft BitLocker-Verwaltung und-Überwachung auf dem folgenden GPO-Knoten beschrieben: **Computerkonfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** - &gt; **Betriebs System Laufwerk**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinienname</th>
<th align="left">Übersicht und vorgeschlagene Gruppenrichtlinieneinstellungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verschlüsselungseinstellungen für das Betriebssystemlaufwerk</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie verwalten, ob das Betriebssystemlaufwerk verschlüsselt sein muss.</p>
<p>Für höhere Sicherheit sollten Sie die folgenden Richtlinieneinstellungen in den <strong> </strong> &gt; <strong> Standbymodus-Einstellungen für Energieverwaltung deaktivieren, </strong> &gt; <strong> </strong> Wenn Sie diese mit TPM + PIN Protector aktivieren:</p>
<ul>
<li><p>Standby-Status (S1-S3) beim schlafen zulassen (angeschlossen)</p></li>
<li><p>Standby-Status (S1-S3) beim schlafen zulassen (auf Akku)</p></li>
</ul>
<p>Wenn Sie Microsoft Windows 8 oder höher ausführen und BitLocker auf einem Computer ohne TPM verwenden möchten, aktivieren Sie das <strong> Kontrollkästchen BitLocker ohne kompatibles TPM zulassen </strong> . In diesem Modus ist für den Start ein Kennwort erforderlich. Wenn Sie das Kennwort vergessen haben, müssen Sie eine der BitLocker-Wiederherstellungsoptionen verwenden, um auf das Laufwerk zuzugreifen.</p>
<p>Auf einem Computer mit einem kompatiblen TPM können zwei Arten von Authentifizierungsmethoden beim Start verwendet werden, um zusätzlichen Schutz für verschlüsselte Daten bereitzustellen. Wenn der Computer gestartet wird, kann er nur das TPM zur Authentifizierung verwenden, oder es kann auch die Eingabe einer persönlichen Identifikationsnummer (PIN) erforderlich sein.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, müssen die Benutzer das Betriebssystemlaufwerk unter BitLocker-Schutz setzen, und dann wird das Laufwerk verschlüsselt.</p>
<p>Wenn Sie diese Richtlinie deaktivieren, können Benutzer das Betriebssystemlaufwerk nicht unter BitLocker-Schutz stellen. Wenn Sie diese Richtlinie anwenden, nachdem das Betriebssystemlaufwerk verschlüsselt wurde, wird das Laufwerk entschlüsselt.</p>
<p>Wenn Sie diese Richtlinie nicht konfigurieren, muss das Betriebssystemlaufwerk nicht unter BitLocker-Schutz gespeichert werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erweiterte Pins für den Start zulassen</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Verwenden Sie diese Richtlinieneinstellung, um zu konfigurieren, ob erweiterte Start Pins für BitLocker verwendet werden. Erweiterte Start Pins ermöglichen die Verwendung von Zeichen wie groß-und Kleinbuchstaben, Symbolen, Zahlen und Leerzeichen. Diese Richtlinieneinstellung wird angewendet, wenn Sie BitLocker aktivieren.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, können Endbenutzer durch alle neuen BitLocker-Start Pins erweiterte Pins erstellen. Allerdings können nicht alle Computer erweiterte Pins in der Pre-Boot-Umgebung unterstützen. Wir empfehlen dringend, dass Administratoren bewerten, ob Ihre Systeme mit diesem Feature kompatibel sind, bevor Sie die Verwendung aktivieren.</p>
<p>Aktivieren Sie das <strong> Kontrollkästchen nur-ASCII-Pins erfordern, damit </strong> verbesserte Pins besser mit Computern kompatibel sind, die den Typ oder die Anzahl der Zeichen einschränken, die in die Pre-Boot-Umgebung eingegeben werden können.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren oder nicht konfigurieren, werden keine erweiterten Pins verwendet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswählen, wie BitLocker-geschützte Betriebssystemlaufwerke wiederhergestellt werden können</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie, um den BitLocker-Daten Wiederherstellungs-Agent zu aktivieren oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) zu speichern.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, wird der Daten Wiederherstellungs-Agent zugelassen, und Wiederherstellungsinformationen werden nicht in AD DS gesichert.</p>
<p>Für den MBAM-Vorgang müssen keine Wiederherstellungsinformationen in AD DS gesichert werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren der Verwendung von Kennwörtern für Betriebssystemlaufwerke</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Verwenden Sie diese Richtlinieneinstellung, um die Einschränkungen für Kennwörter festzulegen, die für die Sperrung von BitLocker-geschützten Betriebssystemlaufwerken verwendet werden. Wenn nicht-TPM-Beschützer auf Betriebssystemlaufwerken zulässig sind, können Sie ein Kennwort bereitstellen, Komplexitätsanforderungen für das Kennwort erzwingen und eine Mindestlänge für das Kennwort konfigurieren. Damit die Komplexitäts Anforderungs Einstellung effektiv ist, müssen Sie auch das Kennwort für die Gruppenrichtlinieneinstellung aktivieren, das die &quot; Komplexitätsanforderungen &quot; in der &gt; Windows-Einstellungen &gt; -Sicherheitseinstellungen &gt; -Kontorichtlinien für die &gt; Kennwortrichtlinien der Computer Konfiguration erfüllen muss.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Einstellungen werden erzwungen, wenn Sie BitLocker aktivieren, nicht, wenn Sie ein Volume entsperren. Mit BitLocker können Sie ein Laufwerk mit einem der auf dem Laufwerk verfügbaren Schutz aufheben.</p>
</div>
<div>

</div>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, können Benutzer ein Kennwort konfigurieren, das die von Ihnen definierten Anforderungen erfüllt. Um die Komplexitätsanforderungen für das Kennwort zu erzwingen, klicken Sie auf <strong> Kennwortkomplexität anfordern </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Konfigurieren des TPM-Platt Form Überprüfungsprofils für BIOS-basierte Firmware-Konfigurationen</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie konfigurieren, wie die TPM-Sicherheitshardware (Trusted Platform Module) des Computers&#39;den BitLocker-Verschlüsselungsschlüssel sichert. Diese Richtlinieneinstellung trifft nicht zu, wenn der Computer nicht über ein kompatibles TPM verfügt oder wenn BitLocker bereits mit TPM-Schutz aktiviert wurde.</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Diese Gruppenrichtlinieneinstellung gilt nur für Computer mit BIOS-Konfigurationen oder für Computer mit UEFI-Firmware, für die ein Compatibility Service Module (CSM) aktiviert ist. Computer, die eine systemeigene UEFI-Firmware-Konfiguration verwenden, speichern unterschiedliche Werte in den Platform Configuration Registers (PCRs). Verwenden Sie das &quot; TPM-Platt Form Überprüfungsprofil für systemeigene UEFI-Firmware-Konfigurationen konfigurieren &quot; , um das TPM-PCR-Profil für Computer zu konfigurieren, die die systemeigene UEFI-Firmware verwenden.</p>
</div>
<div>

</div>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, bevor Sie BitLocker aktivieren, können Sie die Startkomponenten konfigurieren, die das TPM überprüft, bevor Sie den Zugriff auf das BitLocker-verschlüsselte Betriebssystemlaufwerk entsperren. Wenn sich eine dieser Komponenten ändert, während der BitLocker-Schutz aktiviert ist, gibt das TPM den Verschlüsselungsschlüssel zum Entsperren des Laufwerks nicht frei, und der Computer zeigt stattdessen die BitLocker-Wiederherstellungskonsole an und erfordert, dass Sie entweder das Wiederherstellungskennwort oder den Wiederherstellungsschlüssel angeben, um das Laufwerk zu entsperren.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren oder nicht konfigurieren, verwendet BitLocker das Standardprofil für die plattformüberprüfung oder das Platt Form Überprüfungsprofil, das vom Setup Skript angegeben wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren des TPM-Platt Form Überprüfungsprofils</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie konfigurieren, wie die TPM-Sicherheitshardware (Trusted Platform Module) des Computers&#39;den BitLocker-Verschlüsselungsschlüssel sichert. Diese Richtlinieneinstellung trifft nicht zu, wenn der Computer nicht über ein kompatibles TPM verfügt oder wenn BitLocker bereits mit TPM-Schutz aktiviert wurde.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, bevor Sie BitLocker aktivieren, können Sie die Startkomponenten konfigurieren, die das TPM überprüft, bevor Sie den Zugriff auf das BitLocker-verschlüsselte Betriebssystemlaufwerk entsperren. Wenn sich eine dieser Komponenten ändert, während der BitLocker-Schutz aktiviert ist, gibt das TPM den Verschlüsselungsschlüssel zum Entsperren des Laufwerks nicht frei, und der Computer zeigt stattdessen die BitLocker-Wiederherstellungskonsole an und erfordert, dass Sie entweder das Wiederherstellungskennwort oder den Wiederherstellungsschlüssel angeben, um das Laufwerk zu entsperren.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren oder nicht konfigurieren, verwendet BitLocker das Standardprofil für die plattformüberprüfung oder das Platt Form Überprüfungsprofil, das vom Setupskript angegeben wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Konfigurieren des TPM-Platt Form Prüfungs Profils für systemeigene UEFI-Firmware-Konfigurationen</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie konfigurieren, wie die TPM-Sicherheitshardware (Trusted Platform Module) des Computers&#39;den BitLocker-Verschlüsselungsschlüssel sichert. Diese Richtlinieneinstellung trifft nicht zu, wenn der Computer nicht über ein kompatibles TPM verfügt oder wenn BitLocker bereits mit TPM-Schutz aktiviert wurde.</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Diese Gruppenrichtlinieneinstellung gilt nur für Computer mit einer systemeigenen UEFI-Firmware-Konfiguration.</p>
</div>
<div>

</div>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, bevor Sie BitLocker aktivieren, können Sie die Startkomponenten konfigurieren, die vom TPM überprüft werden, bevor der Zugriff auf das BitLocker-verschlüsselte Betriebssystemlaufwerk aufgehoben wird. Wenn sich eine dieser Komponenten ändert, während der BitLocker-Schutz aktiviert ist, gibt das TPM den Verschlüsselungsschlüssel zum Entsperren des Laufwerks nicht frei, und der Computer zeigt stattdessen die BitLocker-Wiederherstellungskonsole an und erfordert, dass Sie entweder das Wiederherstellungskennwort oder den Wiederherstellungsschlüssel angeben, um das Laufwerk zu entsperren.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren oder nicht konfigurieren, verwendet BitLocker das Standardprofil für die plattformüberprüfung oder das Platt Form Überprüfungsprofil, das vom Setupskript angegeben wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Zurücksetzen von Platt Form Überprüfungsdaten nach BitLocker-Wiederherstellung</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Verwenden Sie diese Richtlinieneinstellung, um zu steuern, ob Platt Form Überprüfungsdaten aktualisiert werden, wenn Windows nach der BitLocker-Wiederherstellung gestartet wird.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, werden Platt Form Überprüfungsdaten aktualisiert, wenn Windows nach der BitLocker-Wiederherstellung gestartet wird. Wenn Sie diese Richtlinieneinstellung deaktivieren, werden Platt Form Überprüfungsdaten nicht aktualisiert, wenn Windows nach der BitLocker-Wiederherstellung gestartet wird. Wenn Sie diese Richtlinieneinstellung nicht konfigurieren, werden Platt Form Überprüfungsdaten aktualisiert, wenn Windows nach der BitLocker-Wiederherstellung gestartet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwenden des erweiterten Startkonfigurationsdaten Überprüfungsprofils</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie bestimmte BCD-Einstellungen (Boot Configuration Data) auswählen, die während der plattformüberprüfung überprüft werden sollen.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, können Sie zusätzliche Einstellungen hinzufügen, die Standardeinstellungen entfernen oder beides. Wenn Sie diese Richtlinieneinstellung deaktivieren, wird der Computer auf ein BCD-Profil zurückgesetzt, das mit dem von Windows 7 verwendeten standardmäßigen BCD-Profil vergleichbar ist. Wenn Sie diese Richtlinieneinstellung nicht konfigurieren, überprüft der Computer die standardmäßigen Windows BCD-Einstellungen.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn BitLocker Secure Boot für Platform-und Start Configuration Data (BCD)-Integritätsüberprüfung verwendet, wie &quot; es in der Richtlinie für die Integritätsüberprüfung für die Integritätsprüfung zulassen definiert &quot; &quot; ist, wird die Richtlinie für die Verwendung verbesserter Startkonfigurations Datenüberprüfungen &quot; ignoriert.</p>
</div>
<div>

</div>
<p>Die Einstellung zum Steuern des Start Debuggens (0x16000010) wird immer überprüft und hat keine Auswirkungen, wenn Sie in den bereitgestellten Feldern enthalten ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Einstellungen für die Verschlüsselungsrichtlinien Erzwingung</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Verwenden Sie diese Richtlinieneinstellung, um die Anzahl der Tage zu konfigurieren, die Benutzer die Einhaltung der MBAM-Richtlinien für Ihr Betriebssystemlaufwerk verschieben können. Die Kulanzzeit beginnt, wenn das Betriebssystem zum ersten Mal als nicht kompatibel erkannt wird. Nach Ablauf dieser Frist können Benutzer die erforderliche Aktion nicht verschieben oder eine Ausnahme von ihr anfordern.</p>
<p>Wenn für den Verschlüsselungsprozess Benutzereingaben erforderlich sind, wird ein Dialogfeld angezeigt, das Benutzer nicht schließen können, bis Sie die erforderlichen Informationen bereitstellen.</p>
<p>Wenn Sie diese Einstellung deaktivieren oder nicht konfigurieren, sind die Benutzer nicht gezwungen, die MBAM-Richtlinien einzuhalten.</p>
<p>Wenn zum Hinzufügen eines Beschützers keine Benutzerinteraktion erforderlich ist, beginnt die Verschlüsselung im Hintergrund, nachdem die Kulanzzeit abgelaufen ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Konfigurieren der Nachricht und der URL für die Pre-Boot-Wiederherstellung</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinieneinstellung, um eine benutzerdefinierte Wiederherstellungs Nachricht zu konfigurieren oder eine URL anzugeben, die dann auf dem BitLocker-Wiederherstellungsbildschirm vor dem Start angezeigt wird, wenn das Betriebssystemlaufwerk gesperrt ist. Diese Einstellung steht nur auf Clientcomputern mit Windows 10 zur Verfügung.</p>
<p>Wenn diese Richtlinie aktiviert ist, können Sie eine der folgenden Optionen für die Wiederherstellungs Nachricht vor dem Start auswählen:</p>
<ul>
<li><p><strong>Benutzerdefinierte Wiederherstellungs Nachricht verwenden </strong> : Wählen Sie diese Option aus, um eine benutzerdefinierte Nachricht in den BitLocker-Wiederherstellungsbildschirm vor dem Start einzubeziehen. <strong>Geben Sie im Feld Benutzerdefinierte Wiederherstellungs Nachricht </strong> die Nachricht ein, die angezeigt werden soll. Wenn Sie auch eine Wiederherstellungs-URL angeben möchten, fügen Sie Sie als Teil Ihrer benutzerdefinierten Wiederherstellungs Nachricht ein.</p></li>
<li><p><strong>Benutzerdefinierte Wiederherstellungs-URL verwenden </strong> : Wählen Sie diese Option aus, um die Standard-URL zu ersetzen, die auf dem BitLocker-Wiederherstellungsbildschirm vor dem Start angezeigt wird. <strong>Geben Sie im Feld Benutzerdefinierte Wiederherstellungs </strong> -URL die URL ein, die angezeigt werden soll.</p></li>
<li><p><strong>Standard-Wiederherstellungs Nachricht und-URL verwenden </strong> : Wählen Sie diese Option aus, um die standardmäßige BitLocker-Wiederherstellungs Nachricht und-URL im Pre-Boot BitLocker-Wiederherstellungsbildschirm anzuzeigen Wenn Sie zuvor eine benutzerdefinierte Wiederherstellungs Nachricht oder-URL konfiguriert haben und die Standardnachricht wiederherstellen möchten, müssen Sie diese Richtlinie aktivieren und die <strong> Option Standard Wiederherstellungs Nachricht und-URL verwenden auswählen </strong> .</p></li>
</ul>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Im Pre-Boot-Vorgang werden nicht alle Zeichen und Sprachen unterstützt. Wir empfehlen, dass Sie testen, ob die Zeichen, die Sie für die benutzerdefinierte Nachricht oder URL verwenden, auf dem BitLocker-Wiederherstellungsbildschirm vor dem Start richtig angezeigt werden.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



### Gruppenrichtlinien Definitionen für Wechsellaufwerke

In diesem Abschnitt werden die Gruppenrichtlinien Definitionen für Wechseldatenträger für die Microsoft BitLocker-Verwaltung und-Überwachung auf dem folgenden GPO-Knoten beschrieben: **Computerkonfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker-Verwaltung)** &gt; **Wechsellaufwerk**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinienname</th>
<th align="left">Übersicht und vorgeschlagene Gruppenrichtlinieneinstellungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Steuern der Verwendung von BitLocker auf Wechseldatenträgern</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Diese Richtlinie steuert die Verwendung von BitLocker auf Wechseldaten Laufwerken.</p>
<p>Klicken Sie auf zulassen, dass <strong> Benutzer den BitLocker-Schutz auf Wechseldatenträgern anwenden </strong> , damit Benutzer den BitLocker-Setup-Assistenten auf einem Wechseldatenträger ausführen können.</p>
<p>Klicken Sie auf zulassen, dass <strong> Benutzer BitLocker auf Wechseldatenträgern Sperren und entschlüsseln </strong> , damit Benutzer die BitLocker-Laufwerkverschlüsselung vom Laufwerk entfernen oder die Verschlüsselung während der Wartung anhalten können.</p>
<p>Wenn diese Richtlinie aktiviert ist, und Sie auf zulassen, dass <strong> Benutzer den BitLocker-Schutz auf Wechseldatenträgern anwenden können </strong> , speichert der MBAM-Client die Wiederherstellungsinformationen zu Wechseldatenträgern auf dem MBAM-Schlüssel Wiederherstellungsserver und ermöglicht Benutzern das Wiederherstellen des Laufwerks, wenn das Kennwort verloren geht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Schreibzugriff auf Wechseldatenträger verweigern, die nicht durch BitLocker geschützt sind</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, damit nur die Schreibberechtigung für BitLocker-geschützte Laufwerke zulässig ist.</p>
<p>Wenn diese Richtlinie aktiviert ist, erfordern alle Wechseldatenträger auf dem Computer eine Verschlüsselung, bevor die Schreibberechtigung zulässig ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gewähren des Zugriffs auf von BitLocker geschützte Wechseldatenträger aus früheren Versionen von Windows</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, damit Festplatten mit dem FAT-Dateisystem gesperrt und auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, können Wechseldatenträger, die mit dem FAT-Dateisystem formatiert sind, auf Computern, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird, freigegeben werden, und deren Inhalt kann angezeigt werden. Diese Betriebssysteme verfügen über eine Leseberechtigung für BitLocker-geschützte Laufwerke.</p>
<p>Wenn die Richtlinie deaktiviert ist, können Wechseldatenträger, die mit dem FAT-Dateisystem formatiert sind, nicht entsperrt werden, und der Inhalt kann nicht auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren der Verwendung des Kennworts für Wechseldaten Laufwerke</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, um den Kennwortschutz auf Wechseldatenträgern zu konfigurieren.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, werden Kennwörter mit den Standardeinstellungen unterstützt, die keine Anforderungen an die Kennwortkomplexität enthalten und nur acht Zeichen erfordern.</p>
<p>Um die Sicherheit zu erhöhen, können Sie diese Richtlinie aktivieren und <strong> das Kennwort für Wechseldatenträger anfordern auswählen </strong> , auf <strong> Kennwortkomplexität anfordern </strong> und die gewünschte Mindestlänge für das Kennwort festlegen <strong> </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswählen, wie BitLocker-geschützte Wechsellaufwerke wiederhergestellt werden können</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie, um den BitLocker-Daten Wiederherstellungs-Agent zu aktivieren oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) zu speichern.</p>
<p>Wenn Sie auf <strong> nicht konfiguriert festgelegt </strong> ist, ist der Daten Wiederherstellungs-Agent zulässig, und Wiederherstellungsinformationen werden nicht in AD DS gesichert.</p>
<p>Für den MBAM-Vorgang müssen keine Wiederherstellungsinformationen in AD DS gesichert werden.</p></td>
</tr>
</tbody>
</table>




## Verwandte Themen


[Vorbereiten der Umgebung für MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Bereitstellungsvoraussetzungen für MBAM 2.5](mbam-25-deployment-prerequisites.md)


## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






