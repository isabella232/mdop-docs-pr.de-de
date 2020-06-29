---
title: Grundlegende Informationen zu eigenständigen MBAM 2.5-Berichten
description: Grundlegende Informationen zu eigenständigen MBAM 2.5-Berichten
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804481"
---
# Grundlegende Informationen zu eigenständigen MBAM 2.5-Berichten


In diesem Thema werden die Berichte beschrieben, die verfügbar sind, wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) in der eigenständigen Topologie ausführen.

**Hinweis:**  
Wenn Sie MBAM mit der Configuration Manager-Integrations Topologie ausführen, generieren Sie Berichte aus Configuration Manager anstatt aus MBAM. Weitere Informationen zu diesen Berichten finden Sie unter [Anzeigen von MBAM 2,5-Berichten für die Configuration Manager-Integrations Topologie](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) .



## Grundlegendes zu den MBAM-eigenständigen Topologie-Berichten


MBAM stellt drei Berichtstypen bereit, mit denen Sie Ihre Organisation auf die BitLocker-Konformität überwachen können:

-   [Enterprise-Konformitätsbericht](#bkmk-enterprisecompliance)

-   [Bericht zur Computer Konformität](#bkmk-compliance)

-   [Wiederherstellungs Überwachungsbericht](#bkmk-recovery)

Wenn Sie auf MBAM-Berichte zugreifen möchten, wenn Sie MBAM in der eigenständigen Topologie ausführen, öffnen Sie einen Webbrowser, und öffnen Sie dann die Website Verwaltung und Überwachung. Wählen Sie in der linken Menüleiste **Berichte** aus. Wählen Sie in der oberen Menüleiste die Art des zu generierenden Berichts aus. Weitere Informationen zum Generieren dieser Berichte finden Sie unter [Generieren von eigenständigen MBAM 2,5-Berichten](generating-mbam-25-stand-alone-reports.md).

### <a href="" id="bkmk-enterprisecompliance"></a>Enterprise-Konformitätsbericht

Mithilfe dieses Berichtstyps können Sie Informationen zur allgemeinen BitLocker-Konformität in Ihrer Organisation sammeln. Mithilfe von Filtern können Sie Ihre Suchergebnisse einschränken, um mehr über den Kompatibilitätsstatus und den Fehlerstatus von Computern in Ihrer Organisation zu erfahren.

**Übersicht über Unternehmenskonformität**

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
<td align="left"><p>Verwaltete Computer</p></td>
<td align="left"><p>Die Anzahl der Computer, die von MBAM verwaltet werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%-Kompatibel</p></td>
<td align="left"><p>Prozentsatz der kompatiblen Computer im Unternehmen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Nicht kompatibel</p></td>
<td align="left"><p>Prozentsatz der nicht kompatiblen Computer im Unternehmen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Ausgenommen</p></td>
<td align="left"><p>Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Nicht freigestellt</p></td>
<td align="left"><p>Prozentsatz der Computer, die nicht von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kompatibel</p></td>
<td align="left"><p>Prozentsatz der kompatiblen Computer im Unternehmen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nicht kompatibel</p></td>
<td align="left"><p>Prozentsatz der nicht kompatiblen Computer im Unternehmen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Befreit</p></td>
<td align="left"><p>Gesamtzahl der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nicht freigestellt</p></td>
<td align="left"><p>Gesamtzahl der Computer, die nicht von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
</tr>
</tbody>
</table>



**Informationen zum Unternehmens Kompatibilitäts Computer**

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
<td align="left"><p>Der Konformitätsstatus für den Computer gemäß der für den Computer angegebenen Richtlinie. Die Zustände sind nicht kompatibel und kompatibel. Weitere Informationen zum Interpretieren von Kompatibilitätszuständen finden Sie in der folgenden Tabelle des Compliance-Berichts für den Enterprise-Compliance-Bericht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Befreiung</p></td>
<td align="left"><p>Status, der angibt, ob dieser Computer von der BitLocker-Richtlinie ausgenommen ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Details zum Kompatibilitäts Status</p></td>
<td align="left"><p>Fehler-und Statusmeldungen bezüglich des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Letzter Kontakt</p></td>
<td align="left"><p>Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden. Die Kontaktfrequenz ist konfigurierbar. Weitere Informationen finden Sie in den MBAM-Gruppenrichtlinieneinstellungen.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a>Bericht zur Computer Konformität

Verwenden Sie diesen Berichtstyp, um Informationen zu sammeln, die für einen Computer oder benutzerspezifisch sind.

Zeigen Sie diesen Bericht an, indem Sie im Enterprise-Konformitätsbericht auf den Computernamen klicken oder den Computernamen im Bericht zur Computer Konformität eingeben. Dieser Bericht enthält detaillierte Verschlüsselungsinformationen zu jedem Laufwerk (Betriebssystem und feste Datenlaufwerke) auf einem Computer. Außerdem gibt Sie die Richtlinie an, die auf die einzelnen Laufwerktypen auf dem Computer angewendet wird. Um die Details der einzelnen Laufwerke anzuzeigen, erweitern Sie den Eintrag Computer Name.

**Hinweis:**  
Der Verschlüsselungsstatus für Wechseldatenträger wird in diesem Bericht nicht angezeigt.



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
<td align="left"><p>Der Typ des Betriebssystems auf dem Clientcomputer, der von MBAM verwaltet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kompatibilitäts Status</p></td>
<td align="left"><p>Gesamt Kompatibilitätsstatus des Computers, der von MBAM verwaltet wird. Gültige Zustände sind kompatibel und nicht kompatibel.</p>
<p>Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe die folgende Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet. Dieses Feld stellt jedoch den Konformitätsstatus gemäß der angegebenen Richtlinie dar.</p></td>
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
<td align="left"><p>Befreiung</p></td>
<td align="left"><p>Status, der angibt, ob dieser Computer von der BitLocker-Richtlinie ausgenommen ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Hersteller</p></td>
<td align="left"><p>Name des Computerherstellers, wie er im Computer-BIOS angezeigt wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modell</p></td>
<td align="left"><p>Name des Computerhersteller-Modells, wie er im Computer-BIOS angezeigt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Details zum Kompatibilitäts Status</p></td>
<td align="left"><p>Fehler-und Statusmeldungen bezüglich des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Letzter Kontakt</p></td>
<td align="left"><p>Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden. Die Kontaktfrequenz ist konfigurierbar. Weitere Informationen finden Sie in den MBAM-Gruppenrichtlinieneinstellungen.</p></td>
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
<td align="left"><p>Der Typ des Beschützers, der über die Gruppenrichtlinieneinstellung zum Verschlüsseln eines Betriebssystems oder eines festen Datenvolume ausgewählt wurde.</p></td>
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



### <a href="" id="bkmk-recovery"></a>Wiederherstellungs Überwachungsbericht

Verwenden Sie diesen Berichtstyp, um Benutzer zu überwachen, die Zugriff auf BitLocker-Wiederherstellungsschlüssel angefordert haben. Der Bericht bietet mehrere Filter basierend auf den gewünschten Filterkriterien. Sie können nach einer bestimmten Art von Benutzer (einem Helpdesk-Benutzer oder einem Endbenutzer) filtern, ob die Anforderung fehlgeschlagen ist oder erfolgreich war, welche Art von Schlüssel angefordert wurde, und ein Datumsbereich, in dem der Abruf erfolgte.

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
<td align="left"><p>Überwachungs Anforderungsquelle</p></td>
<td align="left"><p>Die Website, von der die Anforderung initiiert wurde. Dieser Eintrag hat einen von zwei Werten: <strong> Self-Service-Portal </strong> oder <strong> Helpdesk </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status anfordern</p></td>
<td align="left"><p>Der Status der Anforderung. Gültige Status sind erfolgreich (der Schlüssel wurde abgerufen) oder Fehler (der Schlüssel wurde nicht abgerufen).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Helpdesk-Nutzer</p></td>
<td align="left"><p>Helpdesk-Benutzer, der die Anforderung zum Abrufen von Schlüsseln initiiert hat.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn ein erweiterter Helpdesk-Benutzer den Schlüssel ohne Angabe des Endbenutzers wiederherstellen kann, ist das <strong> Feld Endbenutzer </strong> leer. Ein standardmäßiger Helpdesk-Benutzer muss den Endbenutzer angeben, und dieser Benutzer wird in diesem Feld angezeigt.</p>
<p>Bei einer Wiederherstellung über das Self-Service-Portal werden die anfordernden Endbenutzer sowohl in diesem Feld als auch im <strong> Feld Endbenutzer aufgelistet </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Endbenutzer</p></td>
<td align="left"><p>Endbenutzer, der die Anforderung zum Abrufen von Schlüsseln initiiert hat.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Computer</p></td>
<td align="left"><p>Der Computername des Computers, der wiederhergestellt wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Schlüsseltyp</p></td>
<td align="left"><p>Der Typ des Schlüssels, der vom Helpdesk-Benutzer oder vom Endbenutzer angefordert wurde. Die drei Schlüsseltypen, die MBAM sammelt, sind:</p>
<ul>
<li><p>Kennwort für Wiederherstellungsschlüssel (wird zum Wiederherstellen eines Computers im Wiederherstellungsmodus verwendet)</p></li>
<li><p>Wiederherstellungsschlüssel-ID (wird zum Wiederherstellen eines Computers im Wiederherstellungsmodus im Auftrag eines anderen Benutzers verwendet)</p></li>
<li><p>TPM-Kenn Wort Hash (wird zum Wiederherstellen eines Computers mit einem gesperrten TPM verwendet)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Beschreibung des Grunds</p></td>
<td align="left"><p>Der Grund dafür, dass der angegebene Schlüsseltyp vom Helpdesk-Benutzer oder vom Endbenutzer angefordert wurde. Die Gründe sind in den Features Drive Recovery und TPM Verwalten der Verwaltungs-und Überwachungs Website angegeben. Bei den gültigen Einträgen handelt es sich um vom Benutzer eingegebene Text oder einen der folgenden Ursachencodes:</p>
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



**Hinweis:**  
Berichtsergebnisse können in einer Datei gespeichert werden, indem Sie auf der Menüleiste **Berichte** auf die Schaltfläche **exportieren** klicken.




## Verwandte Themen


[BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[Generieren von eigenständigen MBAM 2.5-Berichten](generating-mbam-25-stand-alone-reports.md)



## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





