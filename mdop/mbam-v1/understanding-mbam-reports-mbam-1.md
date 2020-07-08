---
title: Grundlegende Informationen zu MBAM-Berichten
description: Grundlegende Informationen zu MBAM-Berichten
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809613"
---
# Grundlegende Informationen zu MBAM-Berichten


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) generiert verschiedene Berichte, um die BitLocker-Verwendung und-Kompatibilität zu überwachen. In diesem Thema werden die MBAM-Berichte für Unternehmenskonformität, einzelne Computer, Hardwarekompatibilität und wichtige Wiederherstellungsaktivitäten beschrieben.

## Grundlegendes zu berichten


Wenn Sie auf das Feature Berichte von MBAM zugreifen möchten, öffnen Sie die MBAM-Verwaltungswebsite. Wählen Sie im Navigationsbereich **Berichte** aus. Klicken Sie dann im Hauptinhaltsbereich auf die Registerkarte für Ihren Berichtstyp: **Enterprise-Konformitätsbericht**, **Computer Kompatibilitätsbericht**, **Hardware Überwachungsbericht**oder **Wiederherstellungs Überwachungsbericht**.

### Enterprise-Konformitätsbericht

Ein Enterprise-Konformitätsbericht enthält Informationen zur allgemeinen BitLocker-Konformität in Ihrer Organisation. Mit den verfügbaren Filtern für diesen Bericht können Sie Ihre Suchergebnisse nach dem Konformitätsstatus und dem Fehlerstatus einschränken. Dieser Bericht wird alle sechs Stunden ausgeführt.

**Enterprise-Konformitäts Berichtsfelder**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Spalten Name</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Computer Name</p></td>
<td align="left"><p>Der vom Benutzer angegebene DNS-Name, der von MBAM verwaltet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Domänen Name</p></td>
<td align="left"><p>Der vollqualifizierte Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kompatibilitäts Status</p></td>
<td align="left"><p>Der Konformitätsstatus für den Computer entsprechend der für den Computer angegebenen Richtlinie. Die möglichen Zustände sind nicht kompatibel und kompatibel. Weitere Informationen finden Sie unter Konformitätsberichte für den Unternehmens Konformitätsstatus in diesem Thema.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Befreiung</p></td>
<td align="left"><p>Der Status der Computer Hardware zum Ermitteln der Identifizierung des Hardwaretyps und ob der Computer von der Richtlinie ausgenommen ist. Es gibt drei mögliche Zustände: Hardware unbekannt (der Hardwaretyp wurde nicht von MBAM identifiziert), Hardware ausgenommen (der Hardwaretyp wurde identifiziert und als von der MBAM-Richtlinie ausgenommen gekennzeichnet) und nicht ausgenommen (die Hardware wurde identifiziert und ist nicht von der Richtlinie ausgenommen).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Geräte Benutzer</p></td>
<td align="left"><p>Bekannte Benutzer auf dem Computer, der von MBAM verwaltet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Details zum Kompatibilitäts Status</p></td>
<td align="left"><p>Fehler-und Statusmeldungen bezüglich des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Letzter Kontakt</p></td>
<td align="left"><p>Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden. Dieses Mal kann konfiguriert werden. Siehe MBAM-Richtlinieneinstellungen.</p></td>
</tr>
</tbody>
</table>

 

**Kompatibilitätsstatus für Unternehmens Konformitätsberichte**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Kompatibilitäts Status</th>
<th align="left">Befreiung</th>
<th align="left">Beschreibung</th>
<th align="left">Benutzeraktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nicht kompatibler</p></td>
<td align="left"><p>Nicht ausgenommen</p></td>
<td align="left"><p>Der Computer ist gemäß der angegebenen Richtlinie nicht kompatibel, und der Hardwaretyp wurde nicht als von der Richtlinie ausgenommen angegeben.</p></td>
<td align="left"><p>Klicken Sie auf <strong> Computer Name </strong> , um den Bericht zur Computer Konformität zu erweitern und festzustellen, ob der Status der einzelnen Laufwerke der angegebenen Richtlinie entspricht. Wenn der Verschlüsselungsstatus angibt, dass der Computer nicht verschlüsselt ist, ist möglicherweise die Verschlüsselung noch in Bearbeitung, oder es liegt ein Fehler auf dem Computer vor. Wenn kein Fehler vorliegt, besteht die wahrscheinlichste Ursache darin, dass der Computer noch eine Verbindung herstellt oder den Verschlüsselungsstatus herstellt. Überprüfen Sie später, ob sich der Status ändert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kompatibel</p></td>
<td align="left"><p>Nicht ausgenommen</p></td>
<td align="left"><p>Der Computer ist gemäß der angegebenen Richtlinie kompatibel.</p></td>
<td align="left"><p>Keine Aktion erforderlich. Optional können Sie den Bericht zur Computer Konformität anzeigen, um den Zustand des Computers zu bestätigen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kompatibel</p></td>
<td align="left"><p>Hardware ausgenommen</p></td>
<td align="left"><p>Wenn der Hardwaretyp ausgenommen ist. Unabhängig davon, wie die Richtlinie festgesetzt wird, oder der einzelne Status jeder Festplatte, wird der Gesamtzustand als kompatibel angesehen.</p></td>
<td align="left"><p>Keine Aktion erforderlich.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kompatibel</p></td>
<td align="left"><p>Hardware unbekannt</p></td>
<td align="left"><p>MBAM erkennt den Hardware-Typ, aber MBAM weiß nicht, ob es sich um eine Befreiung oder nicht um eine Befreiung handelt. Dies tritt auf, wenn der Administrator den kompatiblen Status für die Hardware nicht eingerichtet hat. Daher wird MBAM standardmäßig auf den kompatiblen Status zurückgesetzt.</p></td>
<td align="left"><p>Dies ist der Anfangszustand eines neu bereitgestellten MBAM-Clients. Sie ist in der Regel nur ein vorübergehender Zustand. Auch wenn der Administrator die Hardware als kompatibel gekennzeichnet hat, kann es zu einer erheblichen Verzögerung oder konfigurierbarer Wartezeit kommen, bevor der Clientcomputer wieder meldet. Notieren Sie sich die Uhrzeit des letzten Kontakts, und melden Sie sich nach dem angegebenen Intervall erneut an, um festzustellen, ob sich der Zustand geändert hat. Wenn sich der Status nicht geändert hat, liegt möglicherweise ein Fehler für diesen Computer oder Hardwaretyp vor.</p></td>
</tr>
</tbody>
</table>

 

### Bericht zur Computer Konformität

Der Bericht zur Computer Konformität zeigt Informationen an, die für einen Computer oder benutzerspezifisch sind.

Der Bericht zur Computer Konformität enthält detaillierte Verschlüsselungsinformationen und anwendbare Richtlinien für jedes Laufwerk auf einem Computer, einschließlich Betriebssystemlaufwerke und fest Netzlaufwerke. Wenn Sie diesen Berichtstyp anzeigen möchten, klicken Sie im Enterprise Compliance-Bericht auf den Computernamen, oder geben Sie den Computernamen in den Computer Kompatibilitätsbericht ein. Um die Details der einzelnen Laufwerke anzuzeigen, erweitern Sie den Eintrag Computer Name.

**Hinweis**  Dieser Bericht bietet keinen Verschlüsselungsstatus für Wechseldaten-Volumes.

 

**Bericht Felder für Computer Konformitätsberichte**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Spalten Name</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Computer Name</p></td>
<td align="left"><p>Der vom Benutzer angegebene DNS-Computername, der von MBAM verwaltet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Domänen Name</p></td>
<td align="left"><p>Der vollqualifizierte Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Computertyp</p></td>
<td align="left"><p>Der Portabilitäts des Computers. Gültige Typen sind nicht portabel und portabel.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Betriebssystem</p></td>
<td align="left"><p>Der Typ des Betriebssystems, der auf dem verwalteten MBAM-Clientcomputer installiert ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kompatibilitäts Status</p></td>
<td align="left"><p>Der allgemeine Kompatibilitäts Status des Computers, der von MBAM verwaltet wird. Gültige Zustände sind kompatibel und nicht kompatibel. Obwohl es möglich ist, kompatible und nicht konforme Laufwerke auf demselben Computer zu haben, gibt dieses Feld die gesamte Computer Konformität pro angegebene Richtlinie an.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Policy-Cypher-Stärke</p></td>
<td align="left"><p>Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke. Beispiel: 128-Bit mit Diffusor</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Richtlinien-Betriebs System Laufwerk</p></td>
<td align="left"><p>Gibt an, ob für den Typ O/S und Protector eine Verschlüsselung erforderlich ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Richtlinie mit festem Datenlaufwerk</p></td>
<td align="left"><p>Gibt an, ob für das festgelegte Laufwerk eine Verschlüsselung erforderlich ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Richtlinie Wechseldatenträger-Datenlaufwerk</p></td>
<td align="left"><p>Gibt an, ob für das Wechsellaufwerk eine Verschlüsselung erforderlich ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Geräte Benutzer</p></td>
<td align="left"><p>Stellt die Identität bekannter Benutzer auf dem Computer bereit.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Befreiung</p></td>
<td align="left"><p>Gibt an, ob der Computer-Hardwaretyp von MBAM erkannt wird und, falls bekannt, ob der Computer als von der Richtlinie ausgenommen angegeben wurde. Es gibt drei Zustände: Hardware unbekannt (der Hardwaretyp wurde nicht von MBAM identifiziert); Hardware ausgenommen (der Hardwaretyp wurde identifiziert und als von der MBAM-Richtlinie ausgenommen markiert); und nicht ausgenommen (die Hardware wurde identifiziert und ist nicht von der Richtlinie ausgenommen).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Hersteller</p></td>
<td align="left"><p>Der Name des Computerherstellers, wie er im Computer-BIOS angezeigt wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modell</p></td>
<td align="left"><p>Der Modellname des Computerherstellers, wie er im Computer-BIOS angezeigt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Details zum Kompatibilitäts Status</p></td>
<td align="left"><p>Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Letzter Kontakt</p></td>
<td align="left"><p>Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden. T</p></td>
</tr>
</tbody>
</table>

 

**Computer Konformitäts Berichts Laufwerk (Felder)**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Spalten Name</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Laufwerkbuchstabe</p></td>
<td align="left"><p>Computer Laufwerkbuchstabe, der diesem bestimmten Laufwerk vom Benutzer zugewiesen wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Laufwerktyp</p></td>
<td align="left"><p>Der Typ des Laufwerks. Gültige Werte sind Betriebs System Laufwerk und festes Datenlaufwerk. Hierbei handelt es sich um physikalische Laufwerke anstatt um logische Volumes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cypher-Stärke</p></td>
<td align="left"><p>Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Protector-Typ</p></td>
<td align="left"><p>Der Typ des Beschützers, der über eine Richtlinie zum Verschlüsseln eines Betriebssystems oder eines festen Volumes ausgewählt wurde. Die gültigen Schutztypen auf einem Betriebssystemlaufwerk sind TPM oder TPM + PIN. Der einzige gültige Protector-Typ für ein festes Datenvolumen ist ein Kennwort.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protector-Status</p></td>
<td align="left"><p>Dieses Feld gibt an, ob der Computer den in der Richtlinie angegebenen Protector-Typ aktiviert hat. Die gültigen Zustände sind ein-oder ausgeschaltet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verschlüsselungsstatus</p></td>
<td align="left"><p>Dies ist der aktuelle Verschlüsselungsstatus des Laufwerks. Gültige Zustände sind verschlüsselt, nicht verschlüsselt und verschlüsseln.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kompatibilitäts Status</p></td>
<td align="left"><p>Gibt an, ob das Laufwerk der Richtlinie entspricht. Status sind nicht kompatibel und kompatibel.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Details zum Kompatibilitäts Status</p></td>
<td align="left"><p>Enthält Fehler-und Statusmeldungen bezüglich des Kompatibilitätszustands des Computers.</p></td>
</tr>
</tbody>
</table>

 

### Hardware Überwachungsbericht

Dieser Bericht kann Ihnen dabei helfen, Änderungen am Hardware Kompatibilitätsstatus bestimmter Computermarken und-Modelle zu überwachen. Damit Sie die Suchergebnisse einschränken können, enthält dieser Berichtfilter für Kriterien wie Art der Änderung und Zeitpunkt des Auftretens. Jede Zustandsänderung wird nach Benutzer und Datum und Uhrzeit nachverfolgt. Der Hardwaretyp wird automatisch vom MBAM-Agent ausgefüllt, der auf dem Clientcomputer ausgeführt wird. Dieser Bericht verfolgt Benutzer Änderungen an den Informationen, die direkt vom verwalteten MBAM-Computer erfasst werden. Eine typische administrative Änderung ändert sich von kompatibel zu inkompatibel. Der Administrator kann jedoch auch ein beliebiges Feld überarbeiten.

**Hardware Überwachungsbericht (Felder)**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Spalten Name</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Datum und Uhrzeit</p></td>
<td align="left"><p>Datum und Uhrzeit, an dem eine Änderung am Hardwaretyp vorgenommen wurde. Beachten Sie, dass jedem eindeutigen Hardwaretyp mindestens ein Eintrag zugewiesen ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Benutzer</p></td>
<td align="left"><p>Administrator Benutzer, der die Änderung für den jeweiligen Eintrag vorgenommen hat.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Typ ändern</p></td>
<td align="left"><p>Der Typ der Änderung, die an den Hardwaretypen Informationen vorgenommen wurde. Gültige Werte sind Addition (neuer Eintrag), aktualisieren (vorhandener Eintrag ändern) oder löschen (vorhandenen Eintrag entfernen).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ursprünglicher Wert</p></td>
<td align="left"><p>Der Wert der Hardwaretypen Spezifikation, bevor die Änderung vorgenommen wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aktueller Wert</p></td>
<td align="left"><p>Der Wert der Hardwaretypen Spezifikation, nachdem die Änderung vorgenommen wurde.</p></td>
</tr>
</tbody>
</table>

 

### Wiederherstellungs Überwachungsbericht

Der Bericht zur Wiederherstellungsprüfung kann Ihnen dabei helfen, Benutzer zu überwachen, die Zugriff auf Wiederherstellungsschlüssel angefordert haben. Die Filterkriterien für diesen Bericht umfassen den Typ des Benutzers, der die Anforderung stellt, den Typ des angeforderten Schlüssels, den Zeitpunkt des Auftretens, den Erfolg oder den Fehler, den Zeitpunkt des Auftretens und den Typ des anfordernden Benutzers (Helpdesk, Endbenutzer). Dieser Bericht ermöglicht Administratoren, kontextbezogene Berichte zu erstellen, die auf dem Bedarf basieren.

**Wiederherstellungs Überwachungsbericht (Felder)**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Spalten Name</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Datum und Uhrzeit anfordern</p></td>
<td align="left"><p>Das Datum und die Uhrzeit, zu dem eine Schlüssel Abrufanforderung von einem Endbenutzer oder Helpdesk-Benutzer erstellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Status anfordern</p></td>
<td align="left"><p>Der Status der Anforderung. Gültige Status sind entweder erfolgreich (der Schlüssel wurde abgerufen) oder Fehler (der Schlüssel wurde nicht abgerufen).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Helpdesk-Nutzer</p></td>
<td align="left"><p>Der Helpdesk-Benutzer, der die Anforderung zum Abrufen von Schlüsseln initiiert hat. Wenn der Benutzer des Helpdesks den Schlüssel im Auftrag eines Endbenutzers abruft, ist das Feld Endbenutzer leer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Benutzer</p></td>
<td align="left"><p>Der Endbenutzer, der die Anforderung zum Abrufen von Schlüsseln initiiert hat.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Schlüsseltyp</p></td>
<td align="left"><p>Der Typ des Schlüssels, der angefordert wurde. MBAM sammelt drei Schlüsseltypen: Kennwort für Wiederherstellungsschlüssel (zum Wiederherstellen eines Computers im Wiederherstellungsmodus). Wiederherstellungsschlüssel-ID (zum Wiederherstellen eines Computers im Wiederherstellungsmodus im Auftrag eines anderen Benutzers) und TPM-Kennwort-Hash (Trusted Platform Module) (zum Wiederherstellen eines Computers mit einem gesperrten TPM).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Beschreibung des Grunds</p></td>
<td align="left"><p>Der Grund für die Anforderung des angegebenen Schlüsseltyps. Die Gründe sind in den Features Drive Recovery und TPM-Verwaltung der administrativen Website angegeben. Gültige Einträge sind der vom Benutzer eingegebene Text oder einer der folgenden Ursachencodes:</p>
<ul>
<li><p>Betriebs System-Startreihenfolge geändert</p></li>
<li><p>BIOS geändert</p></li>
<li><p>Geänderte Betriebs System Dateien</p></li>
<li><p>Startschlüssel verloren</p></li>
<li><p>PIN verloren</p></li>
<li><p>TPM-Reset</p></li>
<li><p>Passphrase verloren</p></li>
<li><p>Smartcard verloren</p></li>
<li><p>PIN-Sperrung zurücksetzen</p></li>
<li><p>Aktivieren von TPM</p></li>
<li><p>Deaktivieren von TPM</p></li>
<li><p>TPM-Kennwort ändern</p></li>
<li><p>TPM löschen</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Wenn Sie Berichtsergebnisse in einer Datei speichern möchten, klicken Sie auf der Menüleiste Berichte auf die Schaltfläche **exportieren** .

 

## Verwandte Themen


[BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 1.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





