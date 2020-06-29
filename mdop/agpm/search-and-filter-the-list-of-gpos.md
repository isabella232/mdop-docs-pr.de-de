---
title: Suchen und Filtern der GPO-Liste
description: Suchen und Filtern der GPO-Liste
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808236"
---
# Suchen und Filtern der GPO-Liste


In Advanced Group Policy Management (AGPM) können Sie die Liste der Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) und deren Attribute durchsuchen, um die Liste der angezeigten GPOs zu filtern. So können Sie beispielsweise nach GPOs mit einem bestimmten Namen, Zustand oder Kommentar suchen. Sie können auch nach GPOs suchen, die zuletzt von einem bestimmten Gruppenrichtlinienadministrator oder an einem bestimmten Datum geändert wurden.

## Durchführen einer komplexen Suche


Sie können eine komplexe Suche mit dem Format GPO- *Attribut 1: Suchzeichenfolge 1 GPO-Attribut 2: Suchzeichenfolge 2 durchführen. Suchzeichenfolgen für alle Spalten*. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet.

-   **GPO-Attribut:** Eine Spaltenüberschrift in der Liste der Gruppenrichtlinienobjekte in AGPM, ausgenommen **Computer Version** oder **Benutzerversion**. Zu den GPO-Attributen gehören der Name des Gruppenrichtlinienobjekts, der Status, der Benutzer, der das Gruppenrichtlinienobjekt zuletzt geändert hat, Datum und Uhrzeit, zu dem das GPO zuletzt geändert wurde, Kommentar, GPO-Status und WMI-Filter, die auf das Gruppenrichtlinienobjekt angewendet wurden.

-   **Suchzeichenfolge:** Text, der in der angegebenen Spalte durchsucht werden soll. Wenn eine Zeichenfolge Leerzeichen enthält, müssen Sie die Zeichenfolge mit Anführungszeichen einschließen.

-   **Suchzeichenfolgen für alle Spalten:** Text, für den in allen Spalten in der Liste der Gruppenrichtlinienobjekte in AGPM außer der **Computer Version** und der **Benutzerversion**gesucht werden soll. Sie können mehrere Zeichenfolgen, die durch Leerzeichengetrennt sind, einbeziehen. Wenn eine Zeichenfolge Leerzeichen enthält, müssen Sie die Zeichenfolge mit Anführungszeichen einschließen.

Jedes GPO-Attribut und jedes Suchzeichenfolgen-paar sowie jede Suchzeichenfolge für alle Spalten werden mithilfe eines logischen und-Vorgangs kombiniert. Das Ergebnis ist eine Liste aller GPOs, für die jedes angegebene Attribut die angegebene Suchzeichenfolge enthält und für die alle Spalten-Suchzeichenfolgen in mindestens einer Spalte angezeigt werden. Die Suche gibt alle partiellen Übereinstimmungen für Zeichenfolgen zurück, sodass Sie einen Teil eines GPO-namens oder Benutzernamens eingeben und eine Liste aller GPOs anzeigen können, die diesen Text in seinem Namen enthalten.

Im folgenden finden Sie Beispiele für Suchvorgänge:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Beschreibung des Suchergebnisses</th>
<th align="left">Suchabfrage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Alle GPOs mit Namen, die die Text <strong> Sicherheit </strong> und <strong> Nordamerika enthalten </strong> .</p></td>
<td align="left"><p><strong>Name: </strong><strong> Sicherheits </strong><strong> Name: </strong> &quot; <strong> Nordamerika</strong>&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>Alle ausgecheckten GPOs.</p></td>
<td align="left"><p><strong>Status: </strong> &quot; <strong> ausgecheckt</strong>&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Alle GPOs, die zuletzt vom Benutzer mit dem Namen <strong> Administrator geändert </strong> und zuletzt innerhalb des vorherigen Monats geändert wurden.</p></td>
<td align="left"><p><strong>geändert von: </strong><strong> Administrator </strong><strong> Änderungsdatum: </strong><strong> lastmonth</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Alle GPOs, in denen die <strong> Word </strong> -Firewall im letzten Kommentar enthalten ist und in der die Word- <strong> Sicherheit </strong> in einer beliebigen Spalte angezeigt wird.</p></td>
<td align="left"><p><strong>Kommentar: </strong><strong> Firewall- </strong><strong> Sicherheit</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Alle GPOs, deren Status <strong> alle Einstellungen deaktiviert ist </strong> .</p></td>
<td align="left"><p><strong>GPO-Status: </strong><strong> alle</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Alle GPOs, auf die ein WMI-Filter mit dem Namen " <strong> mein WMI-Filter" </strong> angewendet wurde und die den Status der <strong> Benutzerkonfigurationseinstellungen deaktiviert haben </strong> .</p></td>
<td align="left"><p><strong>WMI-Filter: </strong> &quot; <strong> mein WMI-Filter- </strong> &quot; <strong> GPO-Status: </strong><strong> Benutzer</strong></p></td>
</tr>
</tbody>
</table>

 

## Angeben von Datumsangaben


Sie können nach GPOs suchen, die an einem bestimmten Datum, zu einem bestimmten Zeitpunkt oder während einer Zeitspanne geändert wurden, indem Sie dieselben speziellen Begriffe verwenden, die bei der Suche in Windows zur Verfügung stehen. Wenn Sie ein bestimmtes Datum oder eine bestimmte Uhrzeit eingeben, müssen Sie das Format verwenden, das in der Spalte **Änderungsdatum** verwendet wird. Im folgenden finden Sie Beispiele für Suchvorgänge in der Spalte **Änderungsdatum** :

-   **Änderungsdatum:****10/10/2009**

-   **Änderungsdatum:****10/10/2009 9:00:00 am**

-   **Änderungsdatum:****thisWeek**

Wenn Sie die Spalte **Änderungsdatum** durchsuchen, können Sie die folgenden speziellen Begriffe verwenden, bei denen die Groß-/Kleinschreibung nicht berücksichtigt wird:

-   **Today**

-   **Gestern**

-   **ThisWeek**

-   **LastWeek**

-   **ThisMonth**

-   **LastMonth**

-   **TwoMonths**

-   **ThreeMonths**

-   **ThisYear**

-   **Vorjahres**

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Prüfer, ein Bearbeiter, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigung **Listeninhalte** für die Domäne verfügen.

-   Weitere Informationen zu GPOs-Attributen finden Sie unter [Features für Inhalts Registerkarten](contents-tab-features-agpm40.md).

### Weitere Verweise

-   [Advanced Group Policy Management 4.0](advanced-group-policy-management-40.md)

 

 





