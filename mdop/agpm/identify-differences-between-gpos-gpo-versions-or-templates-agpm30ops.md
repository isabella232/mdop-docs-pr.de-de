---
title: Ermitteln der Unterschiede zwischen Gruppenrichtlinienobjekten und Versionen oder Vorlagen von Gruppenrichtlinienobjekten
description: Ermitteln der Unterschiede zwischen Gruppenrichtlinienobjekten und Versionen oder Vorlagen von Gruppenrichtlinienobjekten
author: dansimp
ms.assetid: e391fa91-3956-4150-9d43-900cfc88d543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88c37a3723c31fb110e731084237a8d89350a4ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808440"
---
# Ermitteln der Unterschiede zwischen Gruppenrichtlinienobjekten und Versionen oder Vorlagen von Gruppenrichtlinienobjekten


Sie können HTML-basierte oder XML-basierte Differenz Berichte generieren, um die Unterschiede zwischen Gruppenrichtlinienobjekten (Group Policy Objects, GPOs), Vorlagen oder unterschiedlichen Versionen eines GPO zu analysieren.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Prüfer, Bearbeiter, genehmigende Person oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

## Erkennen von Unterschieden zwischen GPOs, GPO-Versionen oder Vorlagen


-   [Zwischen zwei GPOs oder Vorlagen](#bkmk-two-gpos)

-   [Zwischen einem Gruppenrichtlinienobjekt und einer Vorlage](#bkmk-gpo-and-template)

-   [Zwischen zwei Versionen eines GPO](#bkmk-two-versions)

-   [Zwischen einer GPO-Version und einer Vorlage](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**So ermitteln Sie Unterschiede zwischen zwei GPOs oder Vorlagen**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf eine Registerkarte, um GPOs anzuzeigen (oder Vorlagen, wenn Sie zwei Vorlagen vergleichen).

3.  Wählen Sie die beiden GPOs oder Vorlagen aus.

4.  Klicken Sie mit der rechten Maustaste auf eine der GPOs oder Vorlagen, klicken Sie auf **Unterschiede**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht** , um einen Unterschiedsbericht anzuzeigen, der die Einstellungen der GPOs oder Vorlagen zusammenfasst.

### <a href="" id="bkmk-gpo-and-template"></a>

**So ermitteln Sie Unterschiede zwischen einem Gruppenrichtlinienobjekt und einer Vorlage**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf eine Registerkarte, um GPOs anzuzeigen (oder Vorlagen, wenn Sie zwei Vorlagen vergleichen).

3.  Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, klicken Sie auf **Unterschiede**und dann auf **Vorlage**.

4.  Wählen Sie die Vorlage und den Typ des Berichts aus, und klicken Sie dann auf **OK** , um einen Unterschiedsbericht anzuzeigen, in dem die Einstellungen für das Gruppenrichtlinienobjekt und die Vorlage zusammengefasst sind.

### <a href="" id="bkmk-two-versions"></a>

**So ermitteln Sie Unterschiede zwischen zwei Versionen eines GPO**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf eine Registerkarte, um GPOs anzuzeigen (oder Vorlagen, wenn Sie zwei Vorlagen vergleichen).

3.  Doppelklicken Sie auf das Gruppenrichtlinienobjekt, um dessen Verlauf anzuzeigen, und markieren Sie dann die zu vergleichenden Versionen.

4.  Klicken Sie mit der rechten Maustaste auf eine der Versionen, klicken Sie auf **Unterschiede**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht** , um einen Unterschiedsbericht anzuzeigen, der die Einstellungen der GPOs zusammenfasst.

### <a href="" id="bkmk-gpo-version-and-template"></a>

**So ermitteln Sie Unterschiede zwischen einer GPO-Version und einer Vorlage**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf eine Registerkarte, um GPOs anzuzeigen (oder Vorlagen, wenn Sie zwei Vorlagen vergleichen).

3.  Doppelklicken Sie auf das Gruppenrichtlinienobjekt, um dessen Verlauf anzuzeigen.

4.  Klicken Sie mit der rechten Maustaste auf die zu interessierende GPO-Version, klicken Sie auf **Differenzen**, und klicken Sie dann auf **Vorlage**.

5.  Wählen Sie die Vorlage und den Typ des Berichts aus, und klicken Sie dann auf **OK** , um einen Unterschiedsbericht anzuzeigen, in dem die Einstellungen der GPO-Version und-Vorlage zusammengefasst sind.

## Schlüssel für Unterschiedsberichte


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Symbol</th>
<th align="left">Bedeutung</th>
<th align="left">Farbe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Keine</p></td>
<td align="left"><p>Element mit identischen Einstellungen in beiden GPOs vorhanden</p></td>
<td align="left"><p>Variiert je nach Ebene</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>Element ist in beiden GPOs vorhanden, jedoch mit geänderten Einstellungen</p></td>
<td align="left"><p>Blaue</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>Element ist nur im ersten GPO vorhanden</p></td>
<td align="left"><p>Rot</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>Element ist nur im zweiten GPO vorhanden</p></td>
<td align="left"><p>Grün</p></td>
</tr>
</tbody>
</table>

 

-   Bei Elementen mit geänderten Einstellungen werden die geänderten Einstellungen identifiziert, wenn das Element erweitert wird. Der Wert für das Attribut in den einzelnen Gruppenrichtlinienobjekten wird in der Reihenfolge angezeigt, in der die GPOs im Bericht angezeigt werden.

-   Einige Änderungen an Einstellungen können dazu führen, dass ein Element als zwei unterschiedliche Elemente gemeldet wird (eines ist nur im ersten GPO vorhanden, das nur in der zweiten vorhanden ist) und nicht als ein Element, das sich geändert hat.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Prüfer, ein Bearbeiter, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Leseeinstellungen** für das Gruppenrichtlinienobjekt verfügen. Außerdem müssen Sie zum Anzeigen der Liste der GPOs über die Berechtigung **Listeninhalt** für die Domäne verfügen.

### Weitere Verweise

-   [Durchführen von Prüferaufgaben](performing-reviewer-tasks-agpm30ops.md)

 

 





