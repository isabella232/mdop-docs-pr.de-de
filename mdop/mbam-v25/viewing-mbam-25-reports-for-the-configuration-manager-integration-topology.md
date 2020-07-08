---
title: Anzeigen von MBAM 2.5-Berichten für die Configuration Manager-Integrationstopologie
description: Anzeigen von MBAM 2.5-Berichten für die Configuration Manager-Integrationstopologie
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810318"
---
# Anzeigen von MBAM 2.5-Berichten für die Configuration Manager-Integrationstopologie


In diesem Thema werden die Berichte beschrieben, die verfügbar sind, wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der Configuration Manager-Integrations Topologie konfigurieren. Die Berichte zeigen die BitLocker-Konformität für das Unternehmen und für einzelne Computer und Geräte an, die von MBAM verwaltet werden. Die Berichte liefern tabellarische Informationen und Diagramme und verfügen über Filter, mit denen Sie Daten aus unterschiedlichen Perspektiven anzeigen können.

In der Configuration Manager-Integrations Topologie können Sie Berichte aus Configuration Manager anstatt von der Websiteverwaltung und Überwachung anzeigen, mit Ausnahme des Berichts zur **Wiederherstellung**, den Sie auf der Websiteverwaltung und Überwachung weiterhin anzeigen.

Informationen zu MBAM-Berichten für die eigenständige Topologie finden Sie unter [Anzeigen von MBAM 2,5-Berichten für die eigenständige Topologie](viewing-mbam-25-reports-for-the-stand-alone-topology.md).

## Zugreifen auf Berichte in Configuration Manager


So greifen Sie in Configuration Manager auf das Feature Berichte zu:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version von Configuration Manager</th>
<th align="left">Anzeigen der Berichte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SystemCenter2012 ConfigurationManager</p></td>
<td align="left"><ol>
<li><p>Wählen Sie im linken Bereich den <strong> </strong> Arbeitsbereich Überwachung aus.</p></li>
<li><p>Erweitern Sie in der Struktur <strong> Übersicht </strong> &gt; <strong> Bericht Erstellungs </strong> &gt; <strong> Berichte </strong> &gt; <strong> MBAM </strong> .</p></li>
<li><p>Wählen Sie den Ordner aus, der die Sprache darstellt, in der Sie Berichte anzeigen möchten, und wählen Sie dann im rechten Bereich den Bericht aus.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 2007</p></td>
<td align="left"><ol>
<li><p>Erweitern Sie im linken Bereich <strong> Computer Management </strong> &gt; <strong> Reporting </strong> &gt; <strong> Reporting Services </strong> &gt; <strong> &lt; Servername &gt; </strong> &gt; <strong> Report Folders </strong> &gt; <strong> MBAM </strong> .</p></li>
<li><p>Wählen Sie den Ordner aus, der die Sprache darstellt, in der Sie Berichte anzeigen möchten, und wählen Sie dann im rechten Bereich den Bericht aus.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## Beschreibung von Berichten in Configuration Manager


Es gibt einige geringfügige Unterschiede in den Berichten für die Configuration Manager-Integrations Topologie und die eigenständige Topologie. In den folgenden Abschnitten werden die Daten in den MBAM-Berichten für die Configuration Manager-Integrations Topologie beschrieben:

-   [BitLocker Enterprise Compliance-Dashboard](#bkmk-dashboard)

-   [Details zur BitLocker-Unternehmenskonformität](#bkmk-compliancedetails)

-   [Zusammenfassung der BitLocker-Unternehmenskonformität](#bkmk-compliancesummary)

-   [BitLocker-Computer Kompatibilitätsbericht](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a>BitLocker Enterprise Compliance-Dashboard

Das BitLocker Enterprise Compliance-Dashboard bietet die folgenden Diagramme, die den BitLocker-Kompatibilitätsstatus im gesamten Unternehmen anzeigen:

-   Verteilung des Kompatibilitäts Status

-   Verteilung nicht kompatibler Fehler

-   Kompatibilitäts Status Verteilung nach Laufwerktyp

**Verteilung des Kompatibilitäts Status**

Dieses Kreisdiagramm zeigt den Kompatibilitätsstatus für Computer innerhalb des Unternehmens. Darüber hinaus wird der Prozentsatz der Computer im Vergleich zur Gesamtzahl der Computer in der ausgewählten Sammlung angezeigt, die diesen Kompatibilitätsstatus aufweisen. Die tatsächliche Anzahl der Computer mit jedem Status wird ebenfalls angezeigt. Das Kreisdiagramm zeigt die folgenden Konformitätsstatus:

-   Kompatibel

-   Nicht kompatibel

-   Benutzer freigestellt

-   Temporärer Benutzer ausgenommen

-   Richtlinie nicht erzwungen

-   Unbekannten. Diese Computer haben einen Status Fehler gemeldet, oder Sie sind Teil der Sammlung, haben aber ihren Kompatibilitätsstatus nie gemeldet. Das Fehlen eines Kompatibilitätsstatus kann auftreten, wenn der Computer von der Organisation getrennt ist.

**Verteilung nicht kompatibler Fehler**

Dieses Kreisdiagramm zeigt die Kategorien von Computern im Unternehmen, die nicht mit der BitLocker-Laufwerk Verschlüsselungsrichtlinie kompatibel sind, und zeigt die Anzahl der Computer in jeder Kategorie an. Jeder Kategorie-Prozentsatz wird anhand der Gesamtzahl der nicht kompatiblen Computer in der Sammlung berechnet.

-   Benutzer verzögerte Verschlüsselung

-   Kompatibles TPM konnte nicht gefunden werden

-   System Partition nicht verfügbar oder groß genug

-   Richtlinienkonflikt

-   Warten auf die automatische TPM-Bereitstellung

-   Ein unbekannter Fehler ist aufgetreten.

-   Keine Informationen. Auf diesen Computern ist der MBAM-Client nicht installiert, oder der MBAM-Client ist installiert, aber nicht aktiviert (beispielsweise funktioniert der Dienst nicht).

**Kompatibilitäts Status Verteilung nach Laufwerktyp**

Dieses Balkendiagramm zeigt den aktuellen BitLocker-Konformitätsstatus nach Laufwerks. Die Status sind **kompatibel** und **nicht kompatibel**. Für feste Datenlaufwerke und Betriebssystemlaufwerke werden Balken angezeigt. Computer, die nicht über ein festes Datenlaufwerk verfügen, sind enthalten und zeigen nur einen Wert in der **Betriebs System-Laufwerk** Leiste an. Das Diagramm enthält keine Benutzer, denen eine Ausnahme von der BitLocker-Laufwerk Verschlüsselungsrichtlinie oder der Kategorie "keine Richtlinie" gewährt wurde.

### <a href="" id="bkmk-compliancedetails"></a>Details zur BitLocker-Unternehmenskonformität

Dieser Bericht enthält Informationen zur allgemeinen BitLocker-Compliance im gesamten Unternehmen für die Sammlung von Computern, die für die BitLocker-Verwendung vorgesehen sind.

**BitLocker-Felder für Unternehmens Konformitäts Details**

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
<td align="left"><p>% Unknown Compliance</p></td>
<td align="left"><p>Prozentsatz der Computer mit einem Kompatibilitätsstatus, der unbekannt ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Ausgenommen</p></td>
<td align="left"><p>Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Nicht freigestellt</p></td>
<td align="left"><p>Prozentsatz der Computer, die nicht von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kompatibel</p></td>
<td align="left"><p>Prozentsatz der kompatiblen Computer im Unternehmen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nicht kompatibel</p></td>
<td align="left"><p>Prozentsatz der nicht kompatiblen Computer im Unternehmen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unbekannte Compliance</p></td>
<td align="left"><p>Prozentsatz der Computer mit einem Kompatibilitätsstatus, der unbekannt ist.</p></td>
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

 

**BitLocker Enterprise Compliance-Detailstatus**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Kompatibilitäts Status</th>
<th align="left">Befreiung</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nicht kompatibler</p></td>
<td align="left"><p>Nicht ausgenommen</p></td>
<td align="left"><p>Der Computer ist gemäß der angegebenen Richtlinie nicht kompatibel.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kompatibel</p></td>
<td align="left"><p>Nicht ausgenommen</p></td>
<td align="left"><p>Der Computer ist gemäß der angegebenen Richtlinie kompatibel.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a>Zusammenfassung der BitLocker-Unternehmenskonformität

Verwenden Sie diesen Berichtstyp, um Informationen zur allgemeinen BitLocker-Konformität im gesamten Unternehmen anzuzeigen und die Kompatibilität einzelner Computer anzuzeigen, die sich in der Sammlung von Computern befinden, die für die BitLocker-Verwendung vorgesehen sind.

**Zusammenfassungsfelder für BitLocker-Unternehmenskonformität**

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
<td align="left"><p>% Unknown Compliance</p></td>
<td align="left"><p>Prozentsatz der Computer mit einem Kompatibilitätsstatus, der unbekannt ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Ausgenommen</p></td>
<td align="left"><p>Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Nicht freigestellt</p></td>
<td align="left"><p>Prozentsatz der Computer, die nicht von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kompatibel</p></td>
<td align="left"><p>Prozentsatz der kompatiblen Computer im Unternehmen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nicht kompatibel</p></td>
<td align="left"><p>Prozentsatz der nicht kompatiblen Computer im Unternehmen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unbekannte Compliance</p></td>
<td align="left"><p>Prozentsatz der Computer mit einem Kompatibilitätsstatus, der unbekannt ist.</p></td>
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

 

**BitLocker-Zusammenfassungs Computer für Unternehmens Konformitäts Details**

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
<td align="left"><p>Kompatibilitäts Status</p></td>
<td align="left"><p>Gesamt Kompatibilitätsstatus des Computers, der von MBAM verwaltet wird. Gültige Zustände sind kompatibel und nicht kompatibel. Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe die folgende Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet. Dieses Feld stellt jedoch diesen Konformitätsstatus gemäß der angegebenen Richtlinie dar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Befreiung</p></td>
<td align="left"><p>Status, der angibt, ob der Benutzer von der BitLocker-Richtlinie ausgenommen oder nicht freigestellt ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Geräte Benutzer</p></td>
<td align="left"><p>Benutzer des Geräts.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Details zum Kompatibilitäts Status</p></td>
<td align="left"><p>Fehler-und Statusmeldungen bezüglich des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Letzter Kontakt</p></td>
<td align="left"><p>Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden. Die Kontakthäufigkeit kann über die Gruppenrichtlinieneinstellungen konfiguriert werden.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a>BitLocker-Computer Kompatibilitätsbericht

Verwenden Sie diesen Berichtstyp, um Informationen zu sammeln, die für einen Computer spezifisch sind. Der BitLocker-Computer Kompatibilitätsbericht enthält detaillierte Verschlüsselungsinformationen zu jedem Laufwerk auf einem Computer (Betriebssystem und fest Netzlaufwerke). Darüber hinaus gibt es einen Hinweis auf die Richtlinie, die auf die einzelnen Laufwerktypen auf dem Computer angewendet wird. Um die Details der einzelnen Laufwerke anzuzeigen, erweitern Sie den Eintrag Computer Name.

**Hinweis**  Der Verschlüsselungsstatus für Wechseldatenträger wird in diesem Bericht nicht angezeigt.

 

**BitLocker-Computer Kompatibilitätsbericht: Felder für Computer Details**

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
<td align="left"><p>Der Typ des Betriebssystems, der auf dem verwalteten MBAM-Clientcomputer gefunden wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Allgemeine Compliance</p></td>
<td align="left"><p>Gesamt Kompatibilitätsstatus des Computers, der von MBAM verwaltet wird. Gültige Zustände sind kompatibel und nicht kompatibel. Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe die folgende Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet. Dieses Feld steht jedoch für diesen Kompatibilitätszustand in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kompatibilität des Betriebssystems</p></td>
<td align="left"><p>Kompatibilitätsstatus des Betriebssystems, das von MBAM verwaltet wird. Gültige Zustände sind kompatibel und nicht kompatibel.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Festgelegte Datenlaufwerks Kompatibilität</p></td>
<td align="left"><p>Kompatibilitätsstatus des festen Datenlaufwerks, das von MBAM verwaltet wird. Gültige Zustände sind kompatibel und nicht kompatibel.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Datum der letzten Aktualisierung</p></td>
<td align="left"><p>Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden. Die Kontakthäufigkeit kann über die Gruppenrichtlinieneinstellungen konfiguriert werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Befreiung</p></td>
<td align="left"><p>Status, der angibt, ob der Benutzer von der BitLocker-Richtlinie ausgenommen oder nicht freigestellt ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Befreite Benutzer</p></td>
<td align="left"><p>Der Benutzer, der von der BitLocker-Richtlinie ausgenommen ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Befreiungs Datum</p></td>
<td align="left"><p>Das Datum, an dem die Befreiung gewährt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Details zum Kompatibilitäts Status</p></td>
<td align="left"><p>Fehler-und Statusmeldungen bezüglich des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Richtlinien Verschlüsselungsstärke</p></td>
<td align="left"><p>Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke (beispielsweise 128-Bit mit Diffusor).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Richtlinie: Betriebs System Laufwerk</p></td>
<td align="left"><p>Gibt an, ob für das Betriebssystem und den entsprechenden Protector-Typ eine Verschlüsselung erforderlich ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Richtlinie: Festes Datenlaufwerk</p></td>
<td align="left"><p>Gibt an, ob für das festgelegte Datenlaufwerk eine Verschlüsselung erforderlich ist.</p></td>
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
<td align="left"><p>Geräte Benutzer</p></td>
<td align="left"><p>Bekannte Benutzer auf dem Computer, der von MBAM verwaltet wird.</p></td>
</tr>
</tbody>
</table>

 

**BitLocker-Computer Kompatibilitätsbericht: Computer Volumen Felder**

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
<td align="left"><p>Schutztypen</p></td>
<td align="left"><p>Der Typ des Beschützers, der über die Richtlinie zum Verschlüsseln eines Betriebssystems oder eines festen Datenlaufwerks ausgewählt wurde. Die gültigen Schutztypen für ein Betriebssystem sind TPM oder TPM + PIN. Der gültige Protector-Typ für ein festes Datenlaufwerk ist ein Kennwort.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protector-Status</p></td>
<td align="left"><p>Gibt an, dass der Computer, der von MBAM verwaltet wird, den in der Richtlinie angegebenen Protector-Typ aktiviert hat. Die gültigen Zustände sind ein-oder ausgeschaltet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verschlüsselungsstatus</p></td>
<td align="left"><p>Verschlüsselungsstatus des Laufwerks. Gültige Zustände sind verschlüsselt, nicht verschlüsselt und verschlüsseln.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





