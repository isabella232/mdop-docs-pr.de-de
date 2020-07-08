---
title: Grundlegende Informationen zu MBAM-Berichten
description: Grundlegende Informationen zu MBAM-Berichten
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810180"
---
# Grundlegende Informationen zu MBAM-Berichten


Wenn Sie die eigenständige Topologie bei der Installation von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ausgewählt haben, können Sie in MBAM verschiedene Berichte ausführen, um die BitLocker-Verwendung und-Kompatibilität zu überwachen. MBAM meldet Compliance und weitere Informationen zu allen Computern und Geräten, die es verwaltet. Die Informationen in diesem Thema können verwendet werden, um Ihnen zu helfen, die Microsoft BitLocker-Verwaltungs-und-Überwachungsberichte für Enterprise-und einzelne Computer Konformität sowie für wichtige Wiederherstellungsaktivitäten zu verstehen.

**Hinweis**  Wenn Sie bei der Installation von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) die Configuration Manager-Topologie ausgewählt haben, werden Berichte vom Configuration Manager und nicht von MBAM generiert. Weitere Informationen zu berichten, die in Configuration Manager ausgeführt werden, finden Sie unter [Grundlegendes zu MBAM-Berichten in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).

 

## Grundlegendes zu berichten


Um auf das Feature Berichte der Microsoft BitLocker-Verwaltung und-Überwachung zuzugreifen, öffnen Sie einen Webbrowser, und öffnen Sie die Websiteverwaltung und Überwachung. Wählen Sie in der linken Menüleiste **Berichte** aus, und wählen Sie dann in der oberen Menüleiste die Art des zu generierenden Berichts aus.

### Enterprise-Konformitätsbericht

Mithilfe dieses Berichtstyps können Sie Informationen zur allgemeinen BitLocker-Konformität in Ihrer Organisation sammeln. Sie können verschiedene Filter verwenden, um Ihre Suchergebnisse auf den Konformitätsstatus und den Fehlerstatus zu begrenzen. Die Berichtsinformationen werden alle sechs Stunden aktualisiert.

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
<td align="left"><p>Vom Benutzer festgelegter DNS-Name, der von MBAM verwaltet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Domänen Name</p></td>
<td align="left"><p>Vollständig qualifizierter Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kompatibilitäts Status</p></td>
<td align="left"><p>Der Konformitätsstatus für den Computer gemäß der für den Computer angegebenen Richtlinie. Die Zustände sind nicht kompatibel und kompatibel. Weitere Informationen dazu, wie Kompatibilitätszustände interpretiert werden, finden Sie in der Tabelle Compliance-Status des Enterprise-Konformitäts Berichts.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Details zum Kompatibilitäts Status</p></td>
<td align="left"><p>Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Letzter Kontakt</p></td>
<td align="left"><p>Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden. Die Kontakthäufigkeit ist konfigurierbar (siehe MBAM-Richtlinieneinstellungen).</p></td>
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
<td align="left"><p>Der Computer ist gemäß der angegebenen Richtlinie nicht kompatibel.</p></td>
<td align="left"><p>Erweitern Sie die Details des Computer Compliance-Berichts, indem Sie auf <strong> Computer Name klicken </strong> und ermitteln, ob der Status der einzelnen Laufwerke der angegebenen Richtlinie entspricht. Wenn der Verschlüsselungsstatus angibt, dass der Computer nicht verschlüsselt ist, kann die Verschlüsselung in Bearbeitung sein, oder es liegt ein Fehler auf dem Computer vor. Wenn kein Fehler vorliegt, besteht die wahrscheinlichste Ursache darin, dass der Computer noch eine Verbindung herstellt oder den Verschlüsselungsstatus herstellt. Überprüfen Sie später, ob sich der Status ändert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kompatibel</p></td>
<td align="left"><p>Nicht ausgenommen</p></td>
<td align="left"><p>Der Computer ist gemäß der angegebenen Richtlinie kompatibel.</p></td>
<td align="left"><p>Keine Aktion erforderlich; Sie können den Status des Computers bestätigen, indem Sie den Computer Kompatibilitätsbericht anzeigen.</p></td>
</tr>
</tbody>
</table>

 

### Bericht zur Computer Konformität

Verwenden Sie diesen Berichtstyp, um Informationen zu sammeln, die für einen Computer oder benutzerspezifisch sind.

Dieser Bericht kann angezeigt werden, indem Sie im Enterprise-Konformitätsbericht auf den Computernamen klicken oder den Computernamen im Bericht zur Computer Konformität eingeben. Der Computer Kompatibilitätsbericht enthält detaillierte Verschlüsselungsinformationen zu jedem Laufwerk (Betriebssystem und feste Datenlaufwerke) auf einem Computer sowie einen Hinweis auf die Richtlinie, die auf die einzelnen Laufwerktypen auf dem Computer angewendet wird. Um die Details der einzelnen Laufwerke anzuzeigen, erweitern Sie den Eintrag Computer Name.

**Hinweis**  Der Verschlüsselungsstatus für Wechseldatenträger wird im Bericht nicht angezeigt.

 

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
<td align="left"><p>Vom Benutzer festgelegter DNS-Computername, der von MBAM verwaltet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Domänen Name</p></td>
<td align="left"><p>Vollständig qualifizierter Domänenname, in dem sich der Clientcomputer befindet und von MBAM verwaltet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Computertyp</p></td>
<td align="left"><p>Der Typ des Computers. Gültige Typen sind nicht portabel und portabel.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Betriebssystem</p></td>
<td align="left"><p>Der Typ des Betriebssystems, der auf dem von MBAM verwalteten Clientcomputer gefunden wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kompatibilitäts Status</p></td>
<td align="left"><p>Gesamt Kompatibilitätsstatus des Computers, der von MBAM verwaltet wird. Gültige Zustände sind kompatibel und nicht kompatibel. Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe die folgende Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet. Dieses Feld stellt jedoch den Konformitätsstatus gemäß der angegebenen Richtlinie dar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Richtlinien Verschlüsselungsstärke</p></td>
<td align="left"><p>Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke (beispielsweise 128-Bit mit Diffusor).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Richtlinien-Betriebs System Laufwerk</p></td>
<td align="left"><p>Gibt an, ob für das Betriebssystem eine Verschlüsselung erforderlich ist, und zeigt den entsprechenden Protector-Typ an.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Richtlinie – festes Datenlaufwerk</p></td>
<td align="left"><p>Gibt an, ob für das festgelegte Datenlaufwerk eine Verschlüsselung erforderlich ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Richtlinie Wechseldatenträger-Datenlaufwerk</p></td>
<td align="left"><p>Gibt an, ob für das Wechsellaufwerk eine Verschlüsselung erforderlich ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Geräte Benutzer</p></td>
<td align="left"><p>Bekannte Benutzer auf dem Computer, der von MBAM verwaltet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Hersteller</p></td>
<td align="left"><p>Name des Computerherstellers, wie er im Computer-BIOS angezeigt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modell</p></td>
<td align="left"><p>Name des Computerhersteller-Modells, wie er im Computer-BIOS angezeigt wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Details zum Kompatibilitäts Status</p></td>
<td align="left"><p>Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Letzter Kontakt</p></td>
<td align="left"><p>Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden. Die Kontakthäufigkeit ist konfigurierbar (siehe MBAM-Richtlinieneinstellungen).</p></td>
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
<td align="left"><p>Computer Laufwerkbuchstabe, der dem jeweiligen Laufwerk vom Benutzer zugewiesen wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Laufwerktyp</p></td>
<td align="left"><p>Der Typ des Laufwerks. Gültige Werte sind Betriebs System Laufwerk und festes Datenlaufwerk. Hierbei handelt es sich um physikalische Laufwerke anstatt um logische Volumes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verschlüsselungsstärke</p></td>
<td align="left"><p>Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Protector-Typ</p></td>
<td align="left"><p>Der Typ des Beschützers, der über die Richtlinie zum Verschlüsseln eines Betriebssystems oder eines festen Datenvolume ausgewählt wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protector-Status</p></td>
<td align="left"><p>Gibt an, dass der Computer, der von MBAM verwaltet wird, den in der Richtlinie angegebenen Protector-Typ aktiviert hat. Die gültigen Zustände sind ein-oder ausgeschaltet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verschlüsselungsstatus</p></td>
<td align="left"><p>Verschlüsselungsstatus des Laufwerks. Gültige Zustände sind verschlüsselt, nicht verschlüsselt und verschlüsseln.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kompatibilitäts Status</p></td>
<td align="left"><p>Status, der angibt, ob das Laufwerk der Richtlinie entspricht. Status sind nicht kompatibel und kompatibel.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Details zum Kompatibilitäts Status</p></td>
<td align="left"><p>Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers entsprechend der angegebenen Richtlinie.</p></td>
</tr>
</tbody>
</table>

 

### Wiederherstellungs Überwachungsbericht

Verwenden Sie diesen Berichtstyp, um Benutzer zu überwachen, die den Zugriff auf Wiederherstellungsschlüssel angefordert haben. Der Bericht bietet mehrere Filter basierend auf den gewünschten Filterkriterien. Benutzer können nach einer bestimmten Art von Benutzer filtern, entweder einem Helpdesk-Benutzer oder einem Endbenutzer, ob die Anforderung fehlgeschlagen ist oder erfolgreich war, der spezifische Typ des angeforderten Schlüssels und ein Datumsbereich, in dem der Abruf erfolgte. Der Administrator kann basierend auf dem Bedarf kontextbezogene Berichte erstellen.

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
<td align="left"><p>Datum und Uhrzeit, zu dem eine Schlüssel Abrufanforderung von einem Endbenutzer oder Helpdesk-Benutzer vorgenommen wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Status anfordern</p></td>
<td align="left"><p>Der Status der Anforderung. Gültige Status sind entweder erfolgreich (der Schlüssel wurde abgerufen) oder Fehler (der Schlüssel wurde nicht abgerufen).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Helpdesk-Nutzer</p></td>
<td align="left"><p>Helpdesk-Benutzer, der die Anforderung zum Abrufen von Schlüsseln initiiert hat. Hinweis: Wenn der Benutzer des Helpdesks den Schlüssel für einen Endbenutzer im Auftrag abruft, ist das Feld Endbenutzer leer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Benutzer</p></td>
<td align="left"><p>Endbenutzer, der die Anforderung zum Abrufen von Schlüsseln initiiert hat.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Schlüsseltyp</p></td>
<td align="left"><p>Der Typ des Schlüssels, der entweder vom Helpdesk-Benutzer oder vom Endbenutzer angefordert wurde. Die drei Arten von Schlüsseln, die MBAM sammelt, sind: Wiederherstellungsschlüssel Kennwort (zum Wiederherstellen eines Computers im Wiederherstellungsmodus), Wiederherstellungsschlüssel-ID (wird zum Wiederherstellen eines Computers im Wiederherstellungsmodus für einen anderen Benutzer verwendet) und TPM-Kenn Wort Hash (wird zum Wiederherstellen eines Computers mit einem gesperrten TPM verwendet).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Beschreibung des Grunds</p></td>
<td align="left"><p>Der Grund dafür, dass der angegebene Schlüsseltyp vom Helpdesk-Benutzer oder vom Endbenutzer angefordert wurde. Die Gründe sind in den Features Drive Recovery und TPM Verwalten der Verwaltungs-und Überwachungs Website angegeben. Bei den gültigen Einträgen handelt es sich um einen vom Benutzer eingegebenen Text oder einen der folgenden Ursachencodes:</p>
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
</ul></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Berichtsergebnisse können in einer Datei gespeichert werden, indem Sie auf der Menüleiste Berichte auf die Schaltfläche **exportieren** klicken. Weitere Informationen zum Ausführen von MBAM-Berichten finden Sie unter [so](how-to-generate-mbam-reports-mbam-2.md)wird es gemacht: Erstellen von MBAM-Berichten.

 

## Verwandte Themen


[BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





