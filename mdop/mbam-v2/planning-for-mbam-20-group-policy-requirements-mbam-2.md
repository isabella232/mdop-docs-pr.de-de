---
title: Planen der Gruppenrichtlinienanforderungen für MBAM 2.0
description: Planen der Gruppenrichtlinienanforderungen für MBAM 2.0
author: dansimp
ms.assetid: f5e19dcb-eb15-4722-bb71-0734b3799eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6092507996fe6f0234178c8b1abae5cea7bf836
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804520"
---
# Planen der Gruppenrichtlinienanforderungen für MBAM 2.0


Zum Verwalten von Microsoft BitLocker-Verwaltungs-und-Überwachungs Clientcomputern (MBAM) müssen Sie die Typen von BitLocker-Beschützern, die Sie in Ihrer Organisation unterstützen möchten, in Frage stellen und dann die entsprechenden Gruppenrichtlinieneinstellungen konfigurieren, die Sie anwenden möchten. In diesem Thema werden die Gruppenrichtlinieneinstellungen beschrieben, die für die Verwendung von Microsoft BitLocker-Verwaltung und-Überwachung zum Verwalten der BitLocker-Laufwerkverschlüsselung in einem Unternehmen zur Verfügung stehen.

MBAM unterstützt die folgenden Arten von BitLocker-Beschützern für Betriebssystemlaufwerke: Trusted Platform Module (TPM), TPM + PIN, TPM + USB-Schlüssel und TPM + PIN + USB-Schlüssel, Kennwort, numerisches Kennwort und Daten Wiederherstellungs-Agent. Der Kennwortschutz wird nur für Windows to go-Geräte und für Windows 8-Geräte unterstützt, die kein TPM aufweisen. MBAM unterstützt die TPM + USB-Taste und die TPM + PIN + USB-Schlüssel-Schutzvorrichtungen nur, wenn das Betriebssystemvolume verschlüsselt ist, bevor MBAM installiert wird.

MBAM unterstützt die folgenden Typen von BitLocker-Beschützern für feste Datenlaufwerke: Kennwort, automatische Sperrung, numerisches Kennwort und Daten Wiederherstellungs-Agent.

Der numerische Kennwortschutz wird automatisch als Teil der Datenträgerverschlüsselung angewendet und muss nicht konfiguriert werden.

**Wichtig**  
Die standardmäßigen Windows BitLocker-Laufwerk Verschlüsselungseinstellungen für Gruppenrichtlinienobjekte (GPO) werden nicht von MBAM verwendet und können zu Konflikten führen, wenn Sie aktiviert sind. Wenn Sie MBAM zum Verwalten von BitLocker aktivieren möchten, müssen Sie die MBAM-Gruppenrichtlinieneinstellungen erst nach der Installation der MBAM-Gruppenrichtlinienvorlage definieren.



Erweiterte Start Pins können Zeichen wie groß-und Kleinbuchstaben und Zahlen enthalten. Im Gegensatz zu BitLocker unterstützt MBAM die Verwendung von Symbolen und Leerzeichen für erweiterte Pins nicht.

Installieren Sie die MBAM-Gruppenrichtlinienvorlage auf einem Computer, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (AGPM)-MDOP-Technologie ausgeführt werden kann. Zum Bearbeiten der GPO-Einstellungen, die die MBAM-Funktion aktivieren, müssen Sie zuerst die MBAM-Gruppenrichtlinienvorlage installieren, die GPMC oder AGPM öffnen, um das anwendbare GPO zu bearbeiten, und dann zum folgenden GPO-Knoten navigieren: **Computer Konfigurations** \\ **Richtlinien** \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltung).**

Der MDOP MBAM (BitLocker Management)-GPO-Knoten enthält vier globale Richtlinieneinstellungen und vier untergeordnete GPO-Einstellungen-Knoten: Client Verwaltung, festes Laufwerk, Betriebs System Laufwerk und Wechsellaufwerk. Die folgenden Abschnitte enthalten Richtlinien Definitionen und vorgeschlagene Richtlinieneinstellungen, die Sie bei der Planung der MBAM-Richtlinien Einstellungsanforderungen unterstützen.

**Hinweis:**  
Weitere Informationen zum Konfigurieren der mindestens empfohlenen GPO-Einstellungen, damit MBAM die BitLocker-Verschlüsselung verwalten kann, finden Sie unter [Bearbeiten von MBAM 2,0-GPO-Einstellungen](how-to-edit-mbam-20-gpo-settings-mbam-2.md).



## Definitionen globaler Richtlinien


In diesem Abschnitt werden die globalen Richtlinien Definitionen von MBAM beschrieben, die unter dem folgenden GPO-Knoten gefunden werden: **Computerkonfigurations** \\ **Richtlinien** \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltung)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinienname</th>
<th align="left">Übersicht und vorgeschlagene Richtlinieneinstellung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Wählen Sie Laufwerk Verschlüsselungsmethode und Verschlüsselungsstärke aus.</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie für die Verwendung einer bestimmten Verschlüsselungsmethode und Verschlüsselungsstärke.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, verwendet BitLocker die Standardverschlüsselungsmethode von AES 128-Bit mit Diffusor oder die vom Setupskript angegebene Verschlüsselungsmethode.</p></td>
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
<p>Wenn diese Richtlinie nicht konfiguriert ist, wird ein Standardobjekt-ID-1.3.6.1.4.1.311.67.1.1 verwendet, um ein Zertifikat anzugeben.</p></td>
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



## Definitionen für Client Verwaltungsrichtlinien


In diesem Abschnitt werden die Definitionen der clientverwaltungsrichtlinien für die Microsoft BitLocker-Verwaltung und-Überwachung auf dem folgenden GPO-Knoten beschrieben: **Computer Konfigurations** \\ **Richtlinien** \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltungs** \\ **Client Verwaltung**).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinienname</th>
<th align="left">Übersicht und vorgeschlagene Richtlinieneinstellungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Konfigurieren von MBAM-Diensten</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<ul>
<li><p><strong>MBAM-Wiederherstellungs-und Hardware </strong> Dienstendpunkt Verwenden Sie diese Einstellung, um die MBAM-Client-BitLocker-Verschlüsselungs Verwaltung zu aktivieren. Geben Sie einen Endpunkt Speicherort ein, der mit dem folgenden Beispiel vergleichbar ist: <strong> http:// </strong><em> &lt; MBAM Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port der Webdienst ist an &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc gebunden </strong> .</p></li>
<li><p><strong>Wählen Sie die zu speichernden BitLocker-Wiederherstellungsinformationen aus </strong> . Mit dieser Richtlinieneinstellung können Sie den Schlüssel Wiederherstellungs Dienst so konfigurieren, dass BitLocker-Wiederherstellungsinformationen gesichert werden. Darüber hinaus können Sie den Statusberichts Dienst für das Sammeln von Konformitäts-und Überwachungsberichten konfigurieren. Die Richtlinie stellt eine administrative Methode zur Verfügung, die von BitLocker verschlüsselte Daten zurückgibt, um Datenverluste aufgrund fehlender Schlüsselinformationen zu verhindern. Status Bericht und wichtige Wiederherstellungsaktivitäten werden automatisch an den konfigurierten Berichtsserver Speicherort gesendet.</p>
<p>Wenn Sie diese Richtlinieneinstellung nicht konfigurieren oder deaktivieren, werden die Schlüssel Wiederherstellungsinformationen nicht gespeichert, und der Statusbericht und die Schlüssel Wiederherstellungs Aktivität werden nicht an den Server gemeldet. Wenn diese Einstellung auf <strong> Wiederherstellungskennwort und Schlüsselpaket festgelegt ist </strong> , werden das Wiederherstellungskennwort und das Schlüsselpaket automatisch und lautlos auf dem konfigurierten Speicherort des Schlüssel Wiederherstellungs Servers gesichert.</p></li>
<li><p><strong>Geben Sie die Status Häufigkeit der Clientüberprüfung in Minuten ein </strong> . Diese Richtlinieneinstellung verwaltet, wie häufig der Client die BitLocker-Schutzrichtlinien und den Status auf dem Clientcomputer überprüft. Diese Richtlinie verwaltet auch die Häufigkeit, mit der der Client Kompatibilitätsstatus auf dem Server gespeichert wird. Der Client überprüft die BitLocker-Schutzrichtlinien und den Status auf dem Clientcomputer und stellt auch den Client Wiederherstellungsschlüssel unter der konfigurierten Häufigkeit sicher.</p>
<p>Legen Sie diese Häufigkeit basierend auf der Anforderung Ihres Unternehmens für die Häufigkeit der Überprüfung des Konformitätsstatus des Computers und die Häufigkeit des Sicherns des Client Wiederherstellungsschlüssels entsprechend ein.</p></li>
<li><p><strong>MBAM-Status Berichterstattungsdienst Endpunkt </strong> . Sie müssen diese Einstellung so konfigurieren, dass die MBAM-Client-BitLocker-Verschlüsselungs Verwaltung aktiviert wird. Geben Sie einen Endpunkt Speicherort ein, der mit dem folgenden Beispiel vergleichbar ist: <strong> http:// </strong><em> &lt; MBAM Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port der Webdienst ist an &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.svc gebunden </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren von Benutzer Freistellungs Richtlinien</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie eine Websiteadresse, e-Mail-Adresse oder Telefonnummer konfigurieren, mit der ein Benutzer angewiesen wird, eine Ausnahme von der BitLocker-Verschlüsselung anzufordern.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren und eine Websiteadresse, e-Mail-Adresse oder Telefonnummer angeben, wird Benutzern ein Dialogfeld angezeigt, in dem Sie Anweisungen zum beantragen einer Ausnahme vom BitLocker-Schutz erhalten. Weitere Informationen zum Aktivieren von BitLocker-Verschlüsselungs Ausnahmen für Benutzer finden Sie unter <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)"> so wird es gemacht: Verwalten von Benutzer-BitLocker-Verschlüsselungs Ausnahmen </a> .</p>
<p>Wenn Sie diese Richtlinieneinstellung entweder deaktivieren oder nicht konfigurieren, werden die Anweisungen für die ausnahmeanforderung nicht für die Benutzer angezeigt.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Die Benutzer Befreiung wird pro Benutzer und nicht pro Computer verwaltet. Wenn sich mehrere Benutzer am gleichen Computer anmelden und ein Benutzer nicht freigestellt ist, wird der Computer verschlüsselt.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Programm zur Verbesserung der Benutzerfreundlichkeit konfigurieren</p></td>
<td align="left"><p>Mit dieser Richtlinieneinstellung können Sie konfigurieren, wie MBAM-Benutzer an dem Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen können. Dieses Programm sammelt Informationen zur Computer Hardware und wie Benutzer MBAM verwenden, ohne Ihre Arbeit zu unterbrechen. Mithilfe dieser Informationen kann Microsoft ermitteln, welche MBAM-Features verbessert werden können. Microsoft wird diese Informationen nicht verwenden, um MBAM-Benutzer zu identifizieren oder zu kontaktieren.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, können Benutzer am Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren, können die Benutzer nicht am Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen.</p>
<p>Wenn Sie diese Richtlinieneinstellung nicht konfigurieren, können Benutzer am Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen.</p></td>
</tr>
</tbody>
</table>



## Definitionen fester Laufwerk Richtlinien


In diesem Abschnitt werden die Definitionen fester Laufwerk Richtlinien für die Microsoft BitLocker-Verwaltung und-Überwachung auf dem folgenden GPO-Knoten beschrieben: **Computerkonfigurations** \\ **Richtlinien** \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltung)** \\ **festes Laufwerk**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinienname</th>
<th align="left">Übersicht und vorgeschlagene Richtlinieneinstellung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Einstellungen für die Verschlüsselung fester Datenlaufwerke</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie verwalten, ob Festplatten verschlüsselt werden müssen.</p>
<p>Wenn das Volume des Betriebssystems verschlüsselt werden muss, wählen Sie die <strong> Option Auto-Unlock-festes Datenlaufwerk aktivieren aus </strong> .</p>
<p>Wenn Sie diese Richtlinie aktivieren, dürfen Sie die <strong> Richtlinie für die Verwendung von Kennwort für feste Datenlaufwerke konfigurieren nur dann deaktivieren, wenn </strong> die Verwendung der automatischen Sperrung für feste Datenlaufwerke zulässig oder erforderlich ist.</p>
<p>Wenn Sie die automatische Sperrung für fest Netzlaufwerke verwenden möchten, müssen Sie die Betriebssystem-Volumes so konfigurieren, dass Sie verschlüsselt werden.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, müssen die Benutzer alle Festplatten unter BitLocker-Schutz setzen, und die Laufwerke werden verschlüsselt.</p>
<p>Wenn Sie diese Richtlinieneinstellung nicht konfigurieren, müssen Benutzer keine festen Laufwerke unter BitLocker-Schutz setzen. Wenn Sie diese Richtlinie nach dem Verschlüsseln fester Datenlaufwerke anwenden, entschlüsselt der MBAM-Agent die verschlüsselten Festplatten.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren, können die Benutzer ihre festen Datenlaufwerke nicht unter BitLocker-Schutz stellen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Schreibzugriff auf Festplattenlaufwerke verweigern, die nicht durch BitLocker geschützt sind</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Diese Richtlinieneinstellung bestimmt, ob ein BitLocker-Schutz erforderlich ist, damit Festplatten auf einem Computer schreibbar sein können. Diese Richtlinieneinstellung wird angewendet, wenn Sie BitLocker aktivieren.</p>
<p>Wenn die Richtlinie nicht konfiguriert ist, werden alle festen Datenlaufwerke auf dem Computer mit Lese-und Schreibzugriff bereitgestellt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gewähren des Zugriffs auf von BitLocker geschützte Festplatten aus früheren Versionen von Windows</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, damit Festplatten mit dem FAT-Dateisystem gesperrt und auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</p>
<p>Wenn die Richtlinie aktiviert oder nicht konfiguriert ist, können Festplatten, die mit dem FAT-Dateisystem formatiert sind, freigegeben und deren Inhalt auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird. Diese Betriebssysteme verfügen über schreibgeschützten Zugriff auf von BitLocker geschützte Laufwerke.</p>
<p>Wenn die Richtlinie deaktiviert ist, können Festplatten, die mit dem FAT-Dateisystem formatiert sind, nicht entsperrt werden, und der Inhalt kann nicht auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren der Verwendung des Kennworts für feste Laufwerke</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Verwenden Sie diese Richtlinie, um anzugeben, ob ein Kennwort zum Entsperren von mit BitLocker geschützten festen Datenlaufwerken erforderlich ist.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, können Benutzer ein Kennwort konfigurieren, das die von Ihnen definierten Anforderungen erfüllt. BitLocker ermöglicht Benutzern das Entsperren eines Laufwerks mit einem der auf dem Laufwerk verfügbaren Schutzvorrichtungen.</p>
<p>Diese Einstellungen werden beim Aktivieren von BitLocker erzwungen, nicht beim Entsperren eines Volumes.</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren, ist es Benutzern nicht gestattet, ein Kennwort zu verwenden.</p>
<p>Wenn die Richtlinie nicht konfiguriert ist, werden Kennwörter mit den Standardeinstellungen unterstützt, die keine Anforderungen an die Kennwortkomplexität enthalten und nur acht Zeichen erfordern.</p>
<p>Aktivieren Sie für höhere Sicherheit diese Richtlinie, und wählen Sie <strong> Kennwort für festes Datenlaufwerk anfordern aus </strong> , wählen Sie <strong> Kennwortkomplexität anfordern aus </strong> , und legen Sie die gewünschte <strong> minimale Kennwortlänge fest </strong> .</p>
<p>Wenn Sie diese Richtlinieneinstellung deaktivieren, ist es Benutzern nicht gestattet, ein Kennwort zu verwenden.</p>
<p>Wenn Sie diese Richtlinieneinstellung nicht konfigurieren, werden Kennwörter mit den Standardeinstellungen unterstützt, die keine Anforderungen an die Kennwortkomplexität enthalten und nur acht Zeichen erfordern.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswählen, wie BitLocker-geschützte Festplatten wiederhergestellt werden können</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie, um den BitLocker-Daten Wiederherstellungs-Agent zu aktivieren oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) zu speichern.</p>
<p>Wenn die Richtlinie nicht konfiguriert ist, ist der BitLocker-Daten Wiederherstellungs-Agent zulässig, und Wiederherstellungsinformationen werden nicht in AD DS gesichert. Für MBAM müssen keine Wiederherstellungsinformationen in AD DS gesichert werden.</p></td>
</tr>
</tbody>
</table>



## Richtlinien Definitionen für das Betriebs System Laufwerk


In diesem Abschnitt werden die Richtlinien Definitionen für das Betriebssystemlaufwerk für die Microsoft BitLocker-Verwaltung und-Überwachung unter dem folgenden GPO-Knoten beschrieben: **Computerkonfigurations** \\ **Richtlinien** \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker Management)**- \\ **Betriebs System Laufwerk**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinienname</th>
<th align="left">Übersicht und vorgeschlagene Richtlinieneinstellung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verschlüsselungseinstellungen für das Betriebssystemlaufwerk</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie verwalten, ob das Betriebssystemlaufwerk verschlüsselt sein muss.</p>
<p>Für höhere Sicherheit sollten Sie die folgenden Richtlinieneinstellungen in <strong> System/Energieverwaltung/Sleep-Einstellungen deaktivieren, </strong> Wenn Sie Sie mit TPM + PIN Protector aktivieren:</p>
<ul>
<li><p>Standby-Status (S1-S3) beim schlafen zulassen (angeschlossen)</p></li>
<li><p>Standby-Status (S1-S3) beim schlafen zulassen (auf Akku)</p></li>
</ul>
<p>Wenn Sie Microsoft Windows 8 oder höher ausführen und BitLocker auf einem Computer ohne TPM verwenden möchten, aktivieren Sie das <strong> Kontrollkästchen BitLocker ohne kompatibles TPM zulassen </strong> . In diesem Modus ist für den Start ein Kennwort erforderlich. Wenn Sie das Kennwort vergessen haben, müssen Sie eine der BitLocker-Wiederherstellungsoptionen verwenden, um auf das Laufwerk zuzugreifen.</p>
<p>Auf einem Computer mit einem kompatiblen TPM können zwei Arten von Authentifizierungsmethoden beim Start verwendet werden, um zusätzlichen Schutz für verschlüsselte Daten bereitzustellen. Wenn der Computer gestartet wird, kann er nur das TPM zur Authentifizierung verwenden, oder es kann auch die Eingabe einer persönlichen Identifikationsnummer (PIN) erforderlich sein.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, müssen die Benutzer das Betriebssystemlaufwerk unter BitLocker-Schutz setzen, und das Laufwerk wird verschlüsselt.</p>
<p>Wenn Sie diese Richtlinie deaktivieren, können Benutzer das Betriebssystemlaufwerk nicht unter BitLocker-Schutz stellen. Wenn Sie diese Richtlinie anwenden, nachdem das Betriebssystemlaufwerk verschlüsselt wurde, wird das Laufwerk entschlüsselt.</p>
<p>Wenn Sie diese Richtlinie nicht konfigurieren, muss das Betriebssystemlaufwerk nicht unter BitLocker-Schutz gespeichert werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren des TPM-Platt Form Überprüfungsprofils</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie konfigurieren, wie die TPM-Sicherheitshardware auf einem Computer den BitLocker-Verschlüsselungsschlüssel sichert. Diese Richtlinieneinstellung trifft nicht zu, wenn der Computer nicht über ein kompatibles TPM verfügt oder wenn BitLocker bereits mit TPM-Schutz aktiviert wurde.</p>
<p>Wenn diese Richtlinieneinstellung nicht konfiguriert ist, verwendet das TPM das Standardprofil für die plattformüberprüfung oder das Platt Form Überprüfungsprofil, das vom Setupskript angegeben wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswählen, wie BitLocker-geschützte Betriebssystemlaufwerke wiederhergestellt werden können</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie, um den BitLocker-Daten Wiederherstellungs-Agent zu aktivieren oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) zu speichern.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, wird der Daten Wiederherstellungs-Agent zugelassen, und Wiederherstellungsinformationen werden nicht in AD DS gesichert.</p>
<p>Für den MBAM-Vorgang müssen keine Wiederherstellungsinformationen in AD DS gesichert werden.</p></td>
</tr>
</tbody>
</table>



## Definitionen für Wechsellaufwerks Richtlinien


In diesem Abschnitt werden die Richtlinien Definitionen für Wechseldatenträger für die Microsoft BitLocker-Verwaltung und-Überwachung auf dem folgenden GPO-Knoten beschrieben: **Computerkonfigurations** \\ **Richtlinien** \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Management)**-  \\  **Wechsellaufwerk**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinienname</th>
<th align="left">Übersicht und vorgeschlagene Richtlinieneinstellung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Steuern der Verwendung von BitLocker auf Wechseldatenträgern</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Diese Richtlinie steuert die Verwendung von BitLocker auf Wechseldaten Laufwerken.</p>
<p>Aktivieren Sie das <strong> Kontrollkästchen Benutzer können BitLocker-Schutz auf Wechseldatenträgern anwenden </strong> , damit Benutzer den BitLocker-Setup-Assistenten auf einem Wechseldaten Laufwerk ausführen können.</p>
<p>Aktivieren Sie das <strong> Kontrollkästchen Benutzer können BitLocker auf Wechseldatenträgern Sperren und entschlüsseln </strong> , damit Benutzer die BitLocker-Laufwerkverschlüsselung vom Laufwerk entfernen oder die Verschlüsselung während der Wartung anhalten können.</p>
<p>Wenn diese Richtlinie aktiviert ist und die <strong> Option Benutzer können BitLocker-Schutz auf Wechseldatenträgern anwenden aktiviert </strong> ist, speichert der MBAM-Client die Wiederherstellungsinformationen zu Wechseldatenträgern auf dem MBAM-Schlüssel Wiederherstellungsserver und ermöglicht Benutzern das Wiederherstellen des Laufwerks, wenn das Kennwort verloren geht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Schreibzugriff auf Wechseldatenträger verweigern, die nicht durch BitLocker geschützt sind</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, um nur Schreibzugriff auf BitLocker-geschützte Laufwerke zu ermöglichen.</p>
<p>Wenn diese Richtlinie aktiviert ist, müssen alle auf dem Computer entfernbaren Datenlaufwerke verschlüsselt werden, bevor Schreibzugriff zulässig ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gewähren des Zugriffs auf von BitLocker geschützte Wechseldatenträger aus früheren Versionen von Windows</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, damit Festplatten mit dem FAT-Dateisystem gesperrt und auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, können Wechseldatenträger, die mit dem FAT-Dateisystem formatiert sind, auf Computern, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird, freigegeben werden, und deren Inhalt kann angezeigt werden. Diese Betriebssysteme verfügen über schreibgeschützten Zugriff auf von BitLocker geschützte Laufwerke.</p>
<p>Wenn die Richtlinie deaktiviert ist, können Wechseldatenträger, die mit dem FAT-Dateisystem formatiert sind, nicht entsperrt werden, und der Inhalt kann nicht auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren der Verwendung des Kennworts für Wechseldaten Laufwerke</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, um den Kennwortschutz auf Wechseldatenträgern zu konfigurieren.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, werden Kennwörter mit den Standardeinstellungen unterstützt, die keine Anforderungen an die Kennwortkomplexität enthalten und nur acht Zeichen erfordern.</p>
<p>Um die Sicherheit zu erhöhen, können Sie diese Richtlinie aktivieren und das Kontrollkästchen <strong> Kennwort für Wechseldatenträger anfordern aktivieren </strong> , <strong> die Option Kennwortkomplexität anfordern </strong> und die gewünschte Mindestlänge für das Kennwort festlegen <strong> </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswählen, wie BitLocker-geschützte Wechsellaufwerke wiederhergestellt werden können</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie, um den BitLocker-Daten Wiederherstellungs-Agent zu aktivieren oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) zu speichern.</p>
<p>Wenn Sie auf <strong> nicht konfiguriert festgelegt </strong> ist, ist der Daten Wiederherstellungs-Agent zulässig, und die Wiederherstellungsinformationen werden nicht in AD DS gesichert.</p>
<p>Für den MBAM-Vorgang müssen keine Wiederherstellungsinformationen in AD DS gesichert werden.</p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[Bereitstellungsvoraussetzungen für MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)









