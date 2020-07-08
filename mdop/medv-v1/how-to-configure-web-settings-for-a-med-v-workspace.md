---
title: So konfigurieren Sie Webeinstellungen für einen MED-V-Arbeitsbereich
description: So konfigurieren Sie Webeinstellungen für einen MED-V-Arbeitsbereich
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812133"
---
# So konfigurieren Sie Webeinstellungen für einen MED-V-Arbeitsbereich


Websites, die nur in älteren Versionen von Internet Explorer angezeigt werden können und die nicht im Hostbetriebssystem vorhanden sind, können in älteren Versionen von Internet Explorer innerhalb des MED-V-Arbeitsbereichs angezeigt werden. Der Benutzer muss im MED-V-Arbeitsbereich keinen Browser öffnen, um die angegebenen Websites anzuzeigen. Der Benutzer kann einen Browser auf dem Host öffnen und automatisch an den MED-V-Arbeitsbereich weitergeleitet werden und umgekehrt.

In den folgenden Verfahren wird beschrieben, wie Sie eine Liste von Webbrowsing-Regeln für einen MED-V-Arbeitsbereich einrichten können. Alle in den Regeln enthaltenen Websites können im MED-V-Arbeitsbereich oder auf dem Host durchsucht werden, wie vom Administrator definiert. Alle Websites, die nicht in den Regeln definiert sind, werden von der Umgebung aus durchsucht, in der Sie angefordert wurden. Sie können Sie jedoch auch als Gruppe konfigurieren, um im MED-V-Arbeitsbereich oder auf dem Host durchsucht zu werden.

**Hinweis:**  
Web-Einstellungen gelten nur für Internet Explorer und keine anderen Browser.



Alle Web-Einstellungen werden im **Richtlinien** Modul auf der Registerkarte **Web** konfiguriert.

## Konfigurieren von Webeinstellungen für den MED-V-Arbeitsbereich


**So konfigurieren Sie Webeinstellungen für den MED-V-Arbeitsbereich**

1.  Klicken Sie auf den zu konfigurierbaren MED-V-Arbeitsbereich.

2.  Aktivieren Sie das Kontrollkästchen **Durchsuchen der Liste der URLs, die in der folgenden Tabelle definiert** sind, um den Benutzer zu einem Browser im MED-V-Arbeitsbereich oder-Host umzuleiten, wenn der Benutzer zu einer URL sucht, die den angegebenen Web Rules entspricht.

3.  Klicken Sie auf eine der folgenden Optionen:

    -   **Im Arbeitsbereich**: Umleiten zu einem Browser im MED-V-Arbeitsbereich

    -   **Im Host**: Umleiten zu einem Browser auf dem Host.

4.  Aktivieren Sie das Kontrollkästchen **alle anderen URLs durchsuchen** , um alle URLs, die von den webregeln ausgeschlossen sind, an den Host-oder MED-V-Arbeitsbereich umzuleiten.

5.  Klicken Sie auf eine der folgenden Optionen:

    -   **Im Arbeitsbereich**: leiten Sie alle anderen URLs zu einem Browser im MED-V-Arbeitsbereich um.

    -   **Im Host**: Umleiten aller anderen URLs zu einem Browser auf dem Host.

6.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

## So fügen Sie eine Web-Regel hinzu


**So fügen Sie eine Web-Regel hinzu**

1.  Aktivieren Sie das Kontrollkästchen **Liste der in der folgenden Tabelle definierten URLs durchsuchen** , um die Webbrowser Regeln für das Internet zu aktivieren.

2.  Klicken Sie auf **Hinzufügen**.

    Eine neue webregel wird hinzugefügt.

3.  Konfigurieren Sie die webregel Eigenschaften wie in der folgenden Tabelle beschrieben.

4.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

**MED-V Workspace-Webeigenschaften**

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
<td align="left"><p>Typ</p></td>
<td align="left"><ul>
<li><p><strong>Domänensuffix </strong> – Zugriff auf eine beliebige Hostadresse, die mit dem in der <strong> Value </strong> -Eigenschaft angegebenen Suffix endet und entsprechend der im Web Browsing festgelegten Option festgelegt ist <strong> </strong> .</p></li>
<li><p><strong>IP-Präfix </strong> : Zugriff auf eine vollständige oder teilweise IP-Adresse im Bereich des in der <strong> Value-Eigenschaft angegebenen Präfixes </strong> und wird entsprechend der im Web Browsing festgelegten Option festgelegt <strong> </strong> .</p></li>
<li><p><strong>Alle lokalen Adressen </strong> – Zugriff auf alle Adressen ohne &#39;. &#39; und wird entsprechend der im Web-Browsing festgelegten Option festgesetzt <strong> </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Wert</p></td>
<td align="left"><ul>
<li><p>Wenn <strong> Domänensuffix </strong> in der <strong> Type </strong> -Eigenschaft ausgewählt ist, geben Sie ein Domänensuffix ein.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><ul>
<li><p>Geben Sie nicht &quot; * &quot; vor dem Suffix ein.</p></li>
<li><p>Domänensuffixe unterstützen Aliase ebenfalls.</p></li>
</ul>
</div>
<div>

</div></li>
<li><p>Wenn IP-Präfix in der <strong> Type </strong> -Eigenschaft ausgewählt ist, geben Sie eine vollständige oder teilweise IP-Adresse ein.</p></li>
</ul></td>
</tr>
</tbody>
</table>



## So löschen Sie eine Web-Regel


**So löschen Sie eine Web-Regel**

1.  Wählen Sie im Bereich **Web** die zu löschende Web-Regel aus.

2.  Klicken Sie auf **Entfernen**.

    Die Web-Regel wird gelöscht.

## Verwandte Themen


[Über die Benutzeroberfläche der MED-V-Management-Konsole](using-the-med-v-management-console-user-interface.md)

[Erstellen eines MED-V-Arbeitsbereichs](creating-a-med-v-workspacemedv-10-sp1.md)









