---
title: So generieren Sie Berichte
description: So generieren Sie Berichte
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812088"
---
# So generieren Sie Berichte


Die folgenden Berichtstypen können von Administratoren in MED-V erstellt werden:

-   [Status](#bkmk-generatingastatusreport)– verwenden Sie den Statusbericht, um den aktuellen Status aller aktiven Benutzer und aller MED-V-Arbeitsbereiche jedes Benutzers auf Grundlage eines definierten Zeitraums zu überprüfen. Dazu gehören das Anzeigen von Computern, die derzeit mit dem Server verbunden sind, oder, wenn Sie derzeit nicht verbunden sind, das Datum und die Uhrzeit der letzten Verbindung mit dem Server, den Status der einzelnen Computer und andere relevante Informationen.

-   [Aktivitätsprotokoll](#bkmk-generatinganactivitylogreport)– verwenden Sie diesen Bericht, um Ereignisse zu überprüfen, die von einem bestimmten Host oder Benutzer in einem definierten Datumsbereich stammen.

-   [Fehlerprotokoll](#bkmk-generatinganerrorlogreport)– verwenden Sie diesen Bericht, um Fehler anzuzeigen, die von einem bestimmten Host oder Benutzer in einem definierten Datumsbereich stammen.

Die Berichtsergebnisse können nach jeder beliebigen Spalte sortiert werden, indem Sie auf den entsprechenden Spaltennamen klicken.

Die Berichtsergebnisse können gruppiert werden, indem Sie eine Spaltenüberschrift an den Anfang des Berichts ziehen. Ziehen Sie mehrere Spaltenüberschriften, um eine Spalte nach der anderen zu gruppieren.

## <a href="" id="bkmk-generatingastatusreport"></a>Erstellen eines Status Berichts


**So erstellen Sie einen Statusbericht**

1.  Klicken Sie auf die Schaltfläche **Berichts** Verwaltung.

2.  Wählen Sie im Modul **Berichte** im Menü **Berichtstypen** den Eintrag **Status**aus, und klicken Sie auf **generieren**.

    Das Dialogfeld Berichtsparameter wird angezeigt.

3.  Geben Sie im Dialogfeld **Berichtsparameter** im Feld **Anzahl der Tage** eine Zahl ein, oder verwenden Sie die Pfeile, um die Anzahl der Tage auszuwählen, die in den Statusbericht aufgenommen werden sollen, und klicken Sie auf **OK**.

    Es wird ein Statusbericht generiert. Die Berichtsparameter sind in der folgenden Tabelle definiert.

**Client MED-V-Arbeitsbereichseigenschaften**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Eigenschaft</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Zeit</p></td>
<td align="left"><p>Das Datum und die Uhrzeit, zu der das Ereignis aufgetreten ist.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Standardmäßig werden die Ereignisse in absteigender Datumsreihenfolge angezeigt. Sie können jedoch durch Klicken auf die Spalte Zeit empfangen geändert werden.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Benutzername</p></td>
<td align="left"><p>Der Benutzer, der das Ereignis initiiert hat.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn das Ereignis vor einem angemeldeten Benutzer aufgetreten ist, lautet der Benutzername "System".</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Hostname</p></td>
<td align="left"><p>Der Name des Hostcomputers.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Name des Arbeitsbereichs</p></td>
<td align="left"><p>Der Name des MED-V-Arbeitsbereichs.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arbeitsbereichs Computer Name</p></td>
<td align="left"><p>Der Name des Computers, auf dem der MED-V-Arbeitsbereich ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Online</p></td>
<td align="left"><p>Der aktuelle Status des Clientcomputers:</p>
<ul>
<li><p><strong>Funktioniert nicht mehr</strong></p></li>
<li><p><strong>Begonnen zu &lt; Datum und Uhrzeit des Starts des Arbeitsbereichs&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Client Version</p></td>
<td align="left"><p>Die Versionsnummer des Clients.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Richtlinien Version</p></td>
<td align="left"><p>Die Richtlinienversion, die der MED-V Workspace zurzeit verwendet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Name des Bilds</p></td>
<td align="left"><p>Der Name des Bilds.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bild Version</p></td>
<td align="left"><p>Die Bildversion, die der MED-V Workspace zurzeit verwendet.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Die Version des MED-V-Arbeitsbereichs kann unbekannt sein, wenn Sie noch nicht auf einen Computer heruntergeladen wurde.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a>Erstellen eines Aktivitätsprotokoll Berichts


**So generieren Sie einen Aktivitätsprotokollbericht**

1.  Klicken Sie auf die Schaltfläche **Berichts** Verwaltung.

    Das Modul "Berichte" wird angezeigt.

2.  Wählen Sie im Modul **Berichte** im Menü **Berichtstypen** die Option **Aktivitätsprotokoll**aus, und klicken Sie auf **generieren**.

3.  Konfigurieren Sie im Dialogfeld **Berichtsparameter** einen oder mehrere der folgenden Parameter:

    -   **Anzahl der Tage**: die Anzahl der Tage, die im Bericht angezeigt werden sollen.

    -   **Benutzername enthält**– jedes Ereignis, bei dem der Benutzername den eingegebenen Text enthält, wird im Bericht berücksichtigt.

    -   **Hostname enthält**– jedes Ereignis, bei dem der Hostname den eingegebenen Text enthält, wird im Bericht berücksichtigt.

4.  Klicken Sie auf **OK**.

    Ein Bericht wird mit den ausgewählten Ereignissen und Datumsangaben erstellt. Die Berichtsparameter sind in der folgenden Tabelle definiert.

**Eigenschaften des Aktivitätsprotokoll Berichts**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Eigenschaft</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ereignis-ID</p></td>
<td align="left"><p>Die Ereignis-ID.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Schweregrad</p></td>
<td align="left"><p><strong>Informationen, Fehler, Warnung</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kategorie</p></td>
<td align="left"><p>Das Modul, auf das der Bericht verweist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Eine Beschreibung des Ereignisses.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Empfangene Zeit</p></td>
<td align="left"><p>Das Datum und die Uhrzeit, zu der das Ereignis auf dem Server empfangen wurde.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn der Client offline arbeitet, empfängt der Server die Berichte, wenn der Client online ist.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Standardmäßig werden die Ereignisse in absteigender Datumsreihenfolge angezeigt. Sie können jedoch durch Klicken auf die <strong> Spalte Zeit empfangen geändert werden </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Client Zeit</p></td>
<td align="left"><p>Das Datum und die Uhrzeit, zu der das Ereignis gemäß der Client Uhr aufgetreten ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Hostname</p></td>
<td align="left"><p>Der Name des Hostcomputers.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Benutzername</p></td>
<td align="left"><p>Der Benutzer, der das Ereignis initiiert hat.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Name des Arbeitsbereichs</p></td>
<td align="left"><p>Der Name des MED-V-Arbeitsbereichs.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Arbeitsbereichs Computer Name</p></td>
<td align="left"><p>Der Name des Computers, auf dem der MED-V-Arbeitsbereich ausgeführt wird.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a>Erstellen eines Fehlerprotokoll Berichts


**So generieren Sie einen Fehlerprotokoll Bericht**

1.  Klicken Sie auf die Schaltfläche **Berichts** Verwaltung.

2.  Wählen Sie im Modul **Berichte** im Menü **Berichtstypen** die Option **Fehlerprotokoll**aus, und klicken Sie auf **generieren**.

3.  Konfigurieren Sie im Dialogfeld **Berichtsparameter** einen oder mehrere der folgenden Parameter:

    -   **Anzahl der Tage**: die Anzahl der Tage, die im Bericht angezeigt werden sollen.

    -   **Benutzername enthält**– jedes Ereignis, bei dem der Benutzername den eingegebenen Text enthält, wird im Bericht berücksichtigt.

    -   **Hostname enthält**– jedes Ereignis, bei dem der Hostname den eingegebenen Text enthält, wird im Bericht berücksichtigt.

4.  Klicken Sie auf **OK**.

    Ein Bericht wird mit den ausgewählten Ereignissen und Datumsangaben erstellt. Die Berichtsparameter sind in der folgenden Tabelle definiert.

**Fehlerprotokoll-Berichtseigenschaften**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Eigenschaft</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ereignis-ID</p></td>
<td align="left"><p>Die Ereignis-ID.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kategorie</p></td>
<td align="left"><p>Das Modul, auf das der Bericht verweist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Eine Beschreibung des Ereignisses.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Empfangene Zeit</p></td>
<td align="left"><p>Das Datum und die Uhrzeit, zu der das Ereignis auf dem Server empfangen wurde.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn der Client offline arbeitet, empfängt der Server die Berichte, wenn der Client online ist.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Standardmäßig werden die Ereignisse in absteigender Datumsreihenfolge angezeigt. Sie können jedoch durch Klicken auf die <strong> Spalte Zeit empfangen geändert werden </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Client Zeit</p></td>
<td align="left"><p>Das Datum und die Uhrzeit, zu der das Ereignis gemäß der Client Uhr aufgetreten ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Hostname</p></td>
<td align="left"><p>Der Name des Hostcomputers.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Benutzername</p></td>
<td align="left"><p>Der Benutzer, der das Ereignis initiiert hat.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Name des Arbeitsbereichs</p></td>
<td align="left"><p>Der Name des MED-V-Arbeitsbereichs.</p></td>
</tr>
</tbody>
</table>











