---
title: Grundlegende Informationen zu MBAM Berichten im Konfigurations-Manager
description: Grundlegende Informationen zu MBAM Berichten im Konfigurations-Manager
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810186"
---
# Grundlegende Informationen zu MBAM Berichten im Konfigurations-Manager


Wenn die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der integrierten Configuration Manager-Topologie installiert wird, werden die Hardware Kompatibilitäts-und Berichterstattungsfeatures in die Configuration Manager-Infrastruktur und aus MBAM verschoben. Wenn Sie die Configuration Manager-Topologie verwenden, führen Sie Berichte von Configuration Manager anstatt von MBAM aus, mit Ausnahme des Wiederherstellungs Überwachungsberichts, auf den Sie weiterhin mithilfe der Website Verwaltung und Überwachung zugreifen.

Die Berichte für die integrierte Configuration Manager-Topologie zeigen die BitLocker-Kompatibilität für das Unternehmen und für einzelne Computer und Geräte an, die von MBAM verwaltet werden. In den Berichten werden sowohl tabellarische Informationen als auch Diagramme bereitgestellt, und Sie können Berichte filtern, um Daten aus unterschiedlichen Perspektiven anzuzeigen.

Die Informationen in diesem Thema beschreiben die MBAM-Berichte, die Sie über Configuration Manager ausführen. Informationen zu MBAM-Berichten für die eigenständige Topologie finden Sie unter [Grundlegendes zu MBAM-Berichten](understanding-mbam-reports-mbam-2.md).

## Zugreifen auf Berichte in Configuration Manager


Um in Configuration Manager auf das Feature Berichte zuzugreifen, öffnen Sie die **Configuration Manager-Konsole**. So zeigen Sie die Liste der verfügbaren Berichte an:

-   Erweitern Sie in Configuration Manager 2007 den Knoten **Computer Verwaltung** , und erweitern Sie dann den Knoten **Berichterstellung** .

-   Erweitern Sie in SystemCenter2012 ConfigurationManager im Bereich Überwachung unter **Übersicht**den Knoten **Berichterstattung** , und klicken Sie dann auf **Berichte**.

### BitLocker Enterprise Compliance-Dashboard

Das BitLocker Enterprise Compliance-Dashboard bietet die folgenden Diagramme, die den BitLocker-Kompatibilitätsstatus im gesamten Unternehmen anzeigen:

-   Verteilung des Kompatibilitäts Status

-   Verteilung nicht kompatibler Fehler

-   Kompatibilitäts Status Verteilung nach Laufwerktyp

**Verteilung des Kompatibilitäts Status**

Dieses Kreisdiagramm zeigt den Computer Kompatibilitätsstatus innerhalb des Unternehmens an und zeigt den Prozentsatz der Computer im Vergleich zur Gesamtzahl der Computer in der ausgewählten Sammlung an, die diesen Kompatibilitätsstatus aufweisen. Die tatsächliche Anzahl der Computer mit jedem Status wird ebenfalls angezeigt. Das Kreisdiagramm zeigt die folgenden Konformitätsstatus:

-   Kompatibel

-   Nicht kompatibel

-   Benutzer freigestellt

-   Temporärer Benutzer ausgenommen

-   Richtlinie nicht erzwungen

-   Unbekannt – Computer, deren Status als Fehler gemeldet wurde, oder Geräte, die Teil der Sammlung sind, aber ihren Kompatibilitätsstatus nie gemeldet haben, beispielsweise, wenn Sie von der Organisation getrennt wurden

**Verteilung nicht kompatibler Fehler**

Dieses Kreisdiagramm zeigt die Kategorien von Computern im Unternehmen, die nicht mit der BitLocker-Laufwerk Verschlüsselungsrichtlinie kompatibel sind, und zeigt die Anzahl der Computer in jeder Kategorie an. Jeder Kategorie-Prozentsatz wird anhand der Gesamtzahl der nicht kompatiblen Computer in der Sammlung berechnet.

-   Benutzer verzögerte Verschlüsselung

-   Kompatibles TPM konnte nicht gefunden werden

-   System Partition nicht verfügbar oder groß genug

-   Richtlinienkonflikt

-   Warten auf die automatische TPM-Bereitstellung

-   Ein unbekannter Fehler ist aufgetreten.

-   Keine Informationen – Computer, auf denen der MBAM-Client nicht installiert ist, oder die den MBAM-Client installiert, aber nicht aktiviert haben, beispielsweise funktioniert der Dienst nicht

**Kompatibilitäts Status Verteilung nach Laufwerktyp**

Dieses Balkendiagramm zeigt den aktuellen BitLocker-Konformitätsstatus nach Laufwerks. Die Status sind "kompatibel" und "nicht kompatibel". Für feste Datenlaufwerke und Betriebssystemlaufwerke werden Balken angezeigt. Computer, die nicht über ein festes Datenlaufwerk verfügen, sind enthalten und zeigen nur einen Wert in der Betriebs System-Laufwerkleiste an. Das Diagramm enthält keine Benutzer, denen eine Ausnahme von der BitLocker-Laufwerk Verschlüsselungsrichtlinie oder der Kategorie "keine Richtlinie" gewährt wurde.

### BitLocker Enterprise Compliance-Detailbericht

Dieser Bericht enthält Informationen zur allgemeinen BitLocker-Compliance im gesamten Unternehmen für die Sammlung von Computern, die für die BitLocker-Verwendung vorgesehen sind.

**BitLocker-Berichtsfelder für Unternehmens Konformitäts Details**

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
<td align="left"><p>Prozentsatz der Computer, deren Konformitätsstatus unbekannt ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Ausgenommen</p></td>
<td align="left"><p>Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Nicht freigestellt</p></td>
<td align="left"><p>Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
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
<td align="left"><p>Prozentsatz der Computer, deren Konformitätsstatus unbekannt ist.</p></td>
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

 

**BitLocker Enterprise Compliance Details-Bericht – Konformitätsstatus**

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

 

### BitLocker Enterprise Compliance-Zusammenfassungsbericht

Verwenden Sie diesen Berichtstyp, um Informationen zur allgemeinen BitLocker-Konformität im gesamten Unternehmen anzuzeigen und die Kompatibilität einzelner Computer anzuzeigen, die sich in der Sammlung von Computern befinden, die für die BitLocker-Verwendung vorgesehen sind.

**BitLocker Enterprise Compliance-Zusammenfassungsbericht (Felder)**

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
<td align="left"><p>Prozentsatz der Computer, deren Konformitätsstatus unbekannt ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Ausgenommen</p></td>
<td align="left"><p>Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Nicht freigestellt</p></td>
<td align="left"><p>Prozentsatz der Computer, die von der BitLocker-Verschlüsselungs Anforderung ausgenommen sind.</p></td>
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
<td align="left"><p>Prozentsatz der Computer, deren Konformitätsstatus unbekannt ist.</p></td>
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

 

**BitLocker Enterprise Compliance-Zusammenfassungsbericht – Computer Details**

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
<td align="left"><p>Gesamt Kompatibilitäts Status des Computers, der von MBAM verwaltet wird. Gültige Zustände sind kompatibel und nicht kompatibel. Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe nachfolgenden Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet. Dieses Feld stellt jedoch diesen Konformitätsstatus gemäß der angegebenen Richtlinie dar.</p></td>
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
<td align="left"><p>Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Letzter Kontakt</p></td>
<td align="left"><p>Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden. Die Kontakthäufigkeit ist konfigurierbar (siehe MBAM-Richtlinieneinstellungen).</p></td>
</tr>
</tbody>
</table>

 

### BitLocker-Computer Kompatibilitätsbericht

Verwenden Sie diesen Berichtstyp, um Informationen zu sammeln, die für einen Computer spezifisch sind. Der Computer Kompatibilitätsbericht enthält detaillierte Verschlüsselungsinformationen zu jedem Laufwerk (Betriebs System und feste Datenlaufwerke) auf einem Computer sowie einen Hinweis auf die Richtlinie, die auf die einzelnen Laufwerktypen auf dem Computer angewendet wird. Um die Details der einzelnen Laufwerke anzuzeigen, erweitern Sie den Eintrag Computer Name.

**Hinweis**  Der Verschlüsselungsstatus für Wechseldatenträger wird im Bericht nicht angezeigt.

 

**BitLocker-Computer Kompatibilitätsbericht – Felder für Computer Details**

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
<td align="left"><p>Gesamt Kompatibilitäts Status des Computers, der von MBAM verwaltet wird. Gültige Zustände sind kompatibel und nicht kompatibel. Beachten Sie, dass der Kompatibilitätsstatus pro Laufwerk (siehe nachfolgenden Tabelle) möglicherweise auf unterschiedliche Konformitäts Zustände hindeutet. Dieses Feld stellt jedoch diesen Konformitätsstatus gemäß der angegebenen Richtlinie dar.</p></td>
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
<td align="left"><p>Datum und Uhrzeit des letzten Kontakts des Computers mit dem Server, um den Kompatibilitätsstatus zu melden. Die Kontakthäufigkeit ist konfigurierbar (siehe MBAM-Richtlinieneinstellungen).</p></td>
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
<td align="left"><p>Fehler-und Statusmeldungen des Kompatibilitätszustands des Computers in Übereinstimmung mit der angegebenen Richtlinie.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Richtlinien Verschlüsselungsstärke</p></td>
<td align="left"><p>Die vom Administrator während der MBAM-Richtlinien Spezifikation ausgewählte Verschlüsselungsstärke. (Beispiel: 128-Bit mit Diffusor).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Richtlinie: Betriebs System Laufwerk</p></td>
<td align="left"><p>Gibt an, ob für den O/S und den entsprechenden Protector-Typ eine Verschlüsselung erforderlich ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Richtlinie: Festes Datenlaufwerk</p></td>
<td align="left"><p>Gibt an, ob für das festgelegte Laufwerk eine Verschlüsselung erforderlich ist.</p></td>
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

 

**BitLocker-Computer Kompatibilitätsbericht – Computer Volumen Felder**

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
<td align="left"><p>Der Typ des Beschützers, der über eine Richtlinie zum Verschlüsseln eines Betriebssystems oder eines festen Volumes ausgewählt wurde. Die gültigen Schutztypen für ein Betriebssystem sind TPM oder TPM + PIN, und bei einem festen Datenvolumen handelt es sich um ein Kennwort.</p></td>
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


[Verwenden von MBAM mit dem Konfigurations-Manager](using-mbam-with-configuration-manager.md)

 

 





