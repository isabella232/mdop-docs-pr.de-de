---
title: Planen der Gruppenrichtlinienanforderungen für MBAM 1.0
description: Planen der Gruppenrichtlinienanforderungen für MBAM 1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804226"
---
# Planen der Gruppenrichtlinienanforderungen für MBAM 1.0


Die Microsoft BitLocker-MBAM-Client Verwaltung erfordert die Anwendung benutzerdefinierter Gruppenrichtlinieneinstellungen. In diesem Thema werden die verfügbaren Richtlinienoptionen für Gruppenrichtlinienobjekte beschrieben, wenn Sie MBAM verwenden, um die BitLocker-Laufwerkverschlüsselung im Unternehmen zu verwalten.

**Wichtig**  
MBAM verwendet nicht die standardmäßigen GPO-Einstellungen für die Windows BitLocker Drive-Verschlüsselung. Wenn die Standardeinstellungen aktiviert sind, kann dies zu einem in Konflikt stehenden Verhalten führen. Wenn Sie MBAM zum Verwalten von BitLocker aktivieren möchten, müssen Sie nach der Installation der MBAM-Gruppenrichtlinienvorlage die Richtlinieneinstellungen für Gruppenrichtlinienobjekte definieren.



Nachdem Sie die MBAM-Gruppenrichtlinienvorlage installiert haben, können Sie die verfügbaren benutzerdefinierten MBAM-GPO-Richtlinieneinstellungen anzeigen und ändern, mit denen MBAM die BitLocker-Unternehmens-Verschlüsselung verwalten kann. Die MBAM-Gruppenrichtlinienvorlage muss auf einem Computer installiert sein, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (AGPM)-MDOP-Technologie ausgeführt werden kann. Zum Bearbeiten des anwendbaren Gruppenrichtlinienobjekts öffnen Sie dann die GPMC oder AGPM, und navigieren Sie dann zum folgenden GPO-Knoten: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltung)**.

Der MDOP MBAM (BitLocker Management)-GPO-Knoten enthält vier globale Richtlinieneinstellungen und vier untergeordnete GPO-Einstellungs Knoten. Die vier globalen Richtlinieneinstellungen für GPO sind: Client Verwaltung, festes Laufwerk, Betriebs System Laufwerk und Wechsellaufwerk. Die folgenden Abschnitte enthalten Richtlinien Definitionen und vorgeschlagene Richtlinieneinstellungen, die Ihnen bei der Planung der MBAM-Richtlinien Einstellungsanforderungen helfen.

**Hinweis:**  
Weitere Informationen zum Konfigurieren der Mindesteinstellungen für vorgeschlagene Gruppenrichtlinienobjekte, damit MBAM die BitLocker-Verschlüsselung verwalten kann, finden Sie unter [Bearbeiten von MBAM 1,0-GPO-Einstellungen](how-to-edit-mbam-10-gpo-settings.md).



## Definitionen globaler Richtlinien


In diesem Abschnitt werden die globalen MBAM-Definitionen beschrieben, die unter dem folgenden GPO-Knoten zu finden sind: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltung)**.

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


In diesem Abschnitt werden die Definitionen der clientverwaltungsrichtlinien für MBAM beschrieben, die unter dem folgenden GPO-Knoten gefunden werden: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltungs**  \\  **Clientverwaltung**).

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
<li><p><strong>MBAM-Wiederherstellungs-und Hardware </strong> Dienstendpunkt Dies ist die erste Richtlinieneinstellung, die Sie konfigurieren müssen, um die MBAM-Client-BitLocker-Verschlüsselungs Verwaltung zu aktivieren. Geben Sie für diese Einstellung den Endpunkt Speicherort ein, der dem folgenden Beispiel ähnelt: <strong> http:// </strong><em> &lt; MBAM Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port der Webdienst ist an &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc gebunden </strong> .</p></li>
<li><p><strong>Wählen Sie die zu speichernden BitLocker-Wiederherstellungsinformationen aus </strong> . Mit dieser Richtlinieneinstellung können Sie den Schlüssel Wiederherstellungs Dienst so konfigurieren, dass die BitLocker-Wiederherstellungsinformationen gesichert werden. Außerdem können Sie den Statusberichts Dienst für das Sammeln von Konformitäts-und Überwachungsberichten konfigurieren. Die Richtlinie stellt eine administrative Methode zur Verfügung, die von BitLocker verschlüsselte Daten zurückgibt, um Datenverluste aufgrund fehlender Schlüsselinformationen zu verhindern. Status Bericht und wichtige Wiederherstellungsaktivitäten werden automatisch an den konfigurierten Berichtsserver Speicherort gesendet.</p>
<p>Wenn Sie diese Richtlinieneinstellung nicht konfigurieren oder deaktivieren, werden die Schlüssel Wiederherstellungsinformationen nicht gespeichert, und der Statusbericht und die Schlüssel Wiederherstellungs Aktivität werden nicht an den Server gemeldet. Wenn diese Einstellung auf <strong> Wiederherstellungskennwort und Schlüsselpaket festgelegt ist </strong> , werden das Wiederherstellungskennwort und das Schlüsselpaket automatisch und lautlos auf dem konfigurierten Speicherort des Schlüssel Wiederherstellungs Servers gesichert.</p></li>
<li><p><strong>Geben Sie die Status Häufigkeit der Clientüberprüfung in Minuten ein </strong> . Diese Richtlinieneinstellung verwaltet, wie häufig der Client die BitLocker-Schutzrichtlinien und den Status auf dem Clientcomputer überprüft. Diese Richtlinie verwaltet auch die Häufigkeit, mit der der Client Kompatibilitätsstatus auf dem Server gespeichert wird. Der Client überprüft die BitLocker-Schutzrichtlinien und den Status auf dem Clientcomputer, und es wird auch der Client Wiederherstellungsschlüssel unter der konfigurierten Häufigkeit gesichert.</p>
<p>Legen Sie diese Häufigkeit basierend auf der von Ihrem Unternehmen festgelegten Anforderung fest, wie häufig der Kompatibilitätsstatus des Computers überprüft werden soll und wie häufig der Client Wiederherstellungsschlüssel gesichert werden soll.</p></li>
<li><p><strong>MBAM-Status Berichterstattungsdienst Endpunkt </strong> . Dies ist die zweite Richtlinieneinstellung, die Sie konfigurieren müssen, um die MBAM-Client-BitLocker-Verschlüsselungs Verwaltung zu aktivieren. Geben Sie für diese Einstellung den Endpunkt Speicherort ein, indem Sie das folgende Beispiel verwenden: <strong> http:// </strong><em> &lt; MBAM Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port der Webdienst ist an &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService. gebunden. SVC </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Hardware Kompatibilitätsüberprüfung zulassen</p></td>
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie die Überprüfung der Hardwarekompatibilität verwalten, bevor Sie den BitLocker-Schutz auf Laufwerken von MBAM-Clientcomputern aktivieren.</p>
<p>Sie sollten diese Richtlinienoption aktivieren, wenn Ihr Unternehmen über ältere Computer Hardware oder Computer verfügt, die kein Trusted Platform Module (TPM) unterstützen. Wenn eines der beiden Kriterien wahr ist, aktivieren Sie die Hardware Kompatibilitätsüberprüfung, um sicherzustellen, dass MBAM nur auf Computermodelle angewendet wird, die BitLocker unterstützen. Wenn alle Computer in Ihrer Organisation BitLocker unterstützen, müssen Sie die Hardware Kompatibilität nicht bereitstellen, und Sie können diese Richtlinie auf <strong> nicht konfiguriert festlegen </strong> .</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, wird das Modell des Computers alle 24 Stunden anhand der Hardwarekompatibilitätsliste überprüft, bevor die Richtlinie den BitLocker-Schutz auf einem Computerlaufwerk aktiviert.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Bevor Sie diese Richtlinieneinstellung aktivieren, stellen Sie sicher, dass Sie die <strong> Einstellung MBAM-Wiederherstellungs-und Hardware Dienstendpunkt </strong> in den <strong> Optionen für MBAM-Dienst Richtlinien konfigurieren </strong> konfiguriert haben.</p>
</div>
<div>

</div>
<p>Wenn Sie diese Richtlinieneinstellung entweder deaktivieren oder nicht konfigurieren, wird das Computermodell nicht anhand der Hardwarekompatibilitätsliste überprüft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Konfigurieren von Benutzer Freistellungs Richtlinien</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie eine Websiteadresse, e-Mail-Adresse oder Telefonnummer konfigurieren, mit der ein Benutzer angewiesen wird, eine Ausnahme von der BitLocker-Verschlüsselung anzufordern.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren und eine Websiteadresse, e-Mail-Adresse oder Telefonnummer angeben, wird ein Dialogfeld angezeigt, in dem Benutzer eine Anleitung zum beantragen einer Ausnahme vom BitLocker-Schutz sehen. Weitere Informationen zum Aktivieren von BitLocker-Verschlüsselungs Ausnahmen für Benutzer finden Sie unter <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> so wird es gemacht: Verwalten von Benutzer-BitLocker-Verschlüsselungs Ausnahmen </a> .</p>
<p>Wenn Sie diese Richtlinieneinstellung entweder deaktivieren oder nicht konfigurieren, werden die Anweisungen zum beantragen einer ausnahmeanforderung nicht für die Benutzer angezeigt.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Die Benutzer Befreiung wird pro Benutzer und nicht pro Computer verwaltet. Wenn sich mehrere Benutzer am gleichen Computer anmelden und ein Benutzer nicht freigestellt ist, wird der Computer verschlüsselt.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Definitionen fester Laufwerk Richtlinien


In diesem Abschnitt werden die Definitionen fester Laufwerk Richtlinien für MBAM beschrieben, die unter dem folgenden GPO-Knoten zu finden sind: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker-Verwaltung)**  \\  **festes Laufwerk**.

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
<td align="left"><p>Empfohlene Konfiguration: <strong> aktiviert </strong> , und aktivieren Sie das <strong> Kontrollkästchen Automatisches Entsperren eines festgelegten Datenlaufwerks, </strong> Wenn das Volume des Betriebssystems verschlüsselt werden muss.</p>
<p>Mit dieser Richtlinieneinstellung können Sie verwalten, ob die festen Laufwerke verschlüsselt werden sollen.</p>
<p>Wenn Sie diese Richtlinie aktivieren, deaktivieren Sie die <strong> Richtlinie für die Verwendung von Kennwort für feste Datenlaufwerke konfigurieren </strong> .</p>
<p>Wenn das <strong> Kontrollkästchen automatische Sperrung von festem Datenlaufwerk aktivieren </strong> aktiviert ist, muss das Betriebssystemvolume verschlüsselt sein.</p>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, müssen die Benutzer alle Festplatten unter BitLocker-Schutz setzen, wodurch die Laufwerke verschlüsselt werden.</p>
<p>Wenn Sie diese Richtlinie nicht konfigurieren oder wenn Sie diese Richtlinie deaktivieren, müssen Benutzer keine festen Laufwerke unter dem BitLocker-Schutz speichern.</p>
<p>Wenn Sie diese Richtlinie deaktivieren, entschlüsselt der MBAM-Agent alle verschlüsselten Festplatten.</p>
<p>Wenn die Verschlüsselung des Betriebssystemdatenträgers nicht erforderlich ist, deaktivieren <strong> Sie das Kontrollkästchen automatische Sperrung von festem Datenlaufwerk aktivieren </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verweigern der Schreibberechtigung für feste Laufwerke, die nicht durch BitLocker geschützt sind</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Diese Richtlinieneinstellung bestimmt, ob der BitLocker-Schutz für feste Laufwerke auf einem Computer erforderlich ist, damit Sie beschreibbar sind. Diese Richtlinieneinstellung wird angewendet, wenn Sie BitLocker aktivieren.</p>
<p>Wenn die Richtlinie nicht konfiguriert ist, werden alle festen Laufwerke auf dem Computer mit Lese-und Schreibberechtigungen bereitgestellt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gewähren des Zugriffs auf von BitLocker geschützte Festplatten aus früheren Versionen von Windows</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, um die festen Laufwerke, die mit dem Dateizuordnungstabelle (FAT)-Dateisystem auf Computern mit Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 formatiert sind, zu entsperren und anzuzeigen.</p>
<p>Diese Betriebssysteme verfügen über schreibgeschützte Berechtigungen für BitLocker-geschützte Laufwerke.</p>
<p>Wenn die Richtlinie deaktiviert ist, können Festplatten, die mit dem FAT-Dateisystem formatiert sind, nicht entsperrt werden, und der Inhalt kann nicht auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren der Verwendung des Kennworts für feste Laufwerke</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie zum Konfigurieren des Kennwortschutzes auf Festplatten.</p>
<p>Wenn die Richtlinie nicht konfiguriert ist, werden Kennwörter mit den Standardeinstellungen unterstützt, die keine Anforderungen an die Kennwortkomplexität enthalten und nur acht Zeichen erfordern.</p>
<p>Aktivieren Sie für höhere Sicherheit diese Richtlinie, und wählen Sie <strong> Kennwort für festes Datenlaufwerk anfordern aus </strong> , wählen Sie <strong> Kennwortkomplexität anfordern aus </strong> , und legen Sie die gewünschte <strong> minimale Kennwortlänge fest </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswählen, wie BitLocker-geschützte Festplatten wiederhergestellt werden können</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie, um den BitLocker-Daten Wiederherstellungs-Agent zu aktivieren oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) zu speichern.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, ist der BitLocker-Daten Wiederherstellungs-Agent zulässig, und Wiederherstellungsinformationen werden nicht in AD DS gesichert. Für MBAM müssen die Wiederherstellungsinformationen nicht in AD DS gesichert werden.</p></td>
</tr>
</tbody>
</table>



## Richtlinien Definitionen für das Betriebs System Laufwerk


In diesem Abschnitt werden die Richtlinien Definitionen für das Betriebssystemlaufwerk für MBAM beschrieben, die unter dem folgenden GPO-Knoten gefunden werden: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker Management)**-  \\  **Betriebs System Laufwerk**.

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
<p>Diese Richtlinieneinstellung bestimmt, ob das Betriebssystemlaufwerk verschlüsselt wird.</p>
<p>Konfigurieren Sie diese Richtlinie für die folgenden Aktionen:</p>
<ul>
<li><p>Erzwingen des BitLocker-Schutzes für das Betriebssystemlaufwerk</p></li>
<li><p>Konfigurieren Sie die PIN-Verwendung für die Verwendung einer TPM-PIN (Trusted Platform Module) für den Schutz des Betriebssystems.</p></li>
<li><p>Konfigurieren Sie erweiterte Start Pins, um Zeichen wie groß-und Kleinbuchstaben sowie Zahlen zu ermöglichen. MBAM unterstützt nicht die Verwendung von Symbolen und Leerzeichen für erweiterte Pins, obwohl BitLocker Symbole und Leerzeichen unterstützt.</p></li>
</ul>
<p>Wenn Sie diese Richtlinieneinstellung aktivieren, müssen Benutzer das Betriebssystemlaufwerk mithilfe von BitLocker sichern.</p>
<p>Wenn Sie die Einstellung nicht konfigurieren oder deaktivieren, müssen Benutzer das Betriebssystemlaufwerk nicht mithilfe von BitLocker sichern.</p>
<p>Wenn Sie diese Richtlinie deaktivieren, entschlüsselt der MBAM-Agent das Betriebssystemvolume, wenn es verschlüsselt ist.</p>
<p>Wenn diese Option aktiviert ist, müssen die Benutzer das Betriebssystem mithilfe des BitLocker-Schutzes sichern, und das Laufwerk ist verschlüsselt. Basierend auf Ihren Verschlüsselungsanforderungen können Sie die Schutzmethode für das Betriebssystemlaufwerk auswählen.</p>
<p>Verwenden Sie für höhere Sicherheitsanforderungen TPM + PIN, ermöglichen Sie erweiterte Pins, und setzen Sie die minimale PIN-Länge auf acht Zeichen.</p>
<p>Wenn diese Richtlinie mit der TPM +-PIN-Schutzfunktion aktiviert ist, können Sie die folgenden Richtlinien unter <strong> </strong>  /  <strong> Energie Verwaltungs </strong>  /  <strong> Einstellungen für Energieverwaltung deaktivieren </strong> :</p>
<ul>
<li><p>Standby-Status (S1-S3) beim schlafen zulassen (angeschlossen)</p></li>
<li><p>Standby-Status (S1-S3) beim schlafen zulassen (auf Akku)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren des TPM-Platt Form Überprüfungsprofils</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Mit dieser Richtlinieneinstellung können Sie konfigurieren, wie die TPM-Sicherheitshardware auf einem Computer den BitLocker-Verschlüsselungsschlüssel sichert. Diese Richtlinieneinstellung trifft nicht zu, wenn der Computer nicht über ein kompatibles TPM verfügt oder wenn BitLocker bereits den TPM-Schutz aktiviert hat.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, verwendet das TPM das standardmäßige Platt Form Überprüfungsprofil oder das Platt Form Überprüfungsprofil, das vom Setupskript angegeben wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswählen, wie BitLocker-geschützte Betriebssystemlaufwerke wiederhergestellt werden</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Konfigurieren Sie diese Richtlinie, um den BitLocker-Daten Wiederherstellungs-Agent zu aktivieren oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) zu speichern.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, ist der Daten Wiederherstellungs-Agent zulässig, und die Wiederherstellungsinformationen werden nicht in AD DS gesichert.</p>
<p>Für den MBAM-Vorgang müssen die Wiederherstellungsinformationen nicht in AD DS gesichert werden.</p></td>
</tr>
</tbody>
</table>



## Definitionen für Wechsellaufwerks Richtlinien


In diesem Abschnitt werden die Richtlinien Definitionen für Wechseldatenträger für MBAM beschrieben, die unter dem folgenden GPO-Knoten gefunden werden: **Computerkonfigurations**- \\ **Administrative Vorlagen** \\ **Windows Components** \\ **MDOP MBAM (BitLocker Management)**-  \\  **Wechsellaufwerk**.

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
<p>Aktivieren Sie das <strong> Kontrollkästchen Benutzer können BitLocker-Schutz auf Wechseldatenträgern anwenden </strong> , damit Benutzer den BitLocker-Setup-Assistenten auf einem Wechseldatenträger ausführen können.</p>
<p>Aktivieren Sie das <strong> Kontrollkästchen Benutzer können BitLocker auf Wechseldatenträgern Sperren und entschlüsseln </strong> , damit Benutzer die BitLocker-Laufwerkverschlüsselung vom Laufwerk entfernen oder die Verschlüsselung während der Wartung anhalten können.</p>
<p>Wenn diese Richtlinie aktiviert ist und die <strong> Option Benutzer können BitLocker-Schutz auf Wechseldatenträgern anwenden aktiviert </strong> ist, speichert der MBAM-Client die Wiederherstellungsinformationen zu Wechseldatenträgern auf dem MBAM-Schlüssel Wiederherstellungsserver und ermöglicht Benutzern das Wiederherstellen des Laufwerks, wenn das Kennwort verloren geht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verweigern der Schreibberechtigungen für Wechseldatenträger, die nicht durch BitLocker geschützt sind</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, damit nur-Leseberechtigungen für BitLocker-geschützte Laufwerke zulässig sind.</p>
<p>Wenn diese Richtlinie aktiviert ist, müssen alle auf dem Computer entfernbaren Datenlaufwerke verschlüsselt werden, bevor Schreibberechtigungen zulässig sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gewähren des Zugriffs auf von BitLocker geschützte Wechseldatenträger aus früheren Versionen von Windows</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, um die festen Laufwerke, die mit dem (FAT)-Dateisystem formatiert sind, auf Computern, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird, zu entsperren und anzuzeigen.</p>
<p>Diese Betriebssysteme verfügen über schreibgeschützte Berechtigungen für BitLocker-geschützte Laufwerke.</p>
<p>Wenn die Richtlinie deaktiviert ist, können Wechseldatenträger, die mit dem FAT-Dateisystem formatiert sind, nicht entsperrt werden, und der Inhalt kann nicht auf Computern angezeigt werden, auf denen Windows Server 2008, Windows Vista, Windows XP mit SP3 oder Windows XP mit SP2 ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren der Verwendung des Kennworts für Wechseldaten Laufwerke</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Aktivieren Sie diese Richtlinie, um den Kennwortschutz auf Wechseldatenträgern zu konfigurieren.</p>
<p>Wenn diese Richtlinie nicht konfiguriert ist, werden Kennwörter mit den Standardeinstellungen unterstützt, die keine Anforderungen an die Kennwortkomplexität enthalten und nur acht Zeichen erfordern.</p>
<p>Um die Sicherheit zu erhöhen, können Sie diese Richtlinie aktivieren und <strong> das Kennwort für Wechseldatenträger anfordern auswählen </strong> , <strong> die Option Kennwortkomplexität anfordern auswählen </strong> und dann die gewünschte <strong> Mindestlänge für das Kennwort festlegen </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswählen, wie BitLocker-geschützte Wechsellaufwerke wiederhergestellt werden können</p></td>
<td align="left"><p>Vorgeschlagene Konfiguration: <strong> nicht konfiguriert</strong></p>
<p>Sie können diese Richtlinie so konfigurieren, dass der BitLocker-Daten Wiederherstellungs-Agent aktiviert oder BitLocker-Wiederherstellungsinformationen in Active Directory-Domänendiensten (AD DS) gespeichert werden.</p>
<p>Wenn die Richtlinie auf "nicht konfiguriert" festgelegt ist <strong> </strong> , ist der Daten Wiederherstellungs-Agent zulässig, und die Wiederherstellungsinformationen werden nicht in AD DS gesichert.</p>
<p>Für den MBAM-Vorgang müssen die Wiederherstellungsinformationen nicht in AD DS gesichert werden.</p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[Vorbereiten der Umgebung für MBAM 1.0](preparing-your-environment-for-mbam-10.md)









