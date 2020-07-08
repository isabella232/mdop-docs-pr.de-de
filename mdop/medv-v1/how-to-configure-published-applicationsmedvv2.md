---
title: So konfigurieren Sie veröffentlichte Anwendungen
description: So konfigurieren Sie veröffentlichte Anwendungen
author: dansimp
ms.assetid: 43a59ff7-5d4e-49dc-84e5-1082bc4dd8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cb5736382f03e818ef10aa814a8e61044ca2b73a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810480"
---
# So konfigurieren Sie veröffentlichte Anwendungen


Anwendungen, die nicht mit dem Hostbetriebssystem kompatibel sind, können innerhalb des Med-v-Arbeitsbereichs ausgeführt und aus dem Med-v-Arbeitsbereich auf die gleiche Weise initiiert werden, wie Sie vom Desktop initiiert werden – über das Startmenü oder eine Verknüpfung mit einem lokalen Host. Ausgewählte und definierte Anwendungen werden als veröffentlichte Anwendungen bezeichnet. Die Verfahren in diesem Abschnitt beschreiben, wie Sie veröffentlichte Anwendungen hinzufügen und entfernen.

Eine Anwendung kann auf eine der folgenden Arten veröffentlicht werden:

-   Als Anwendung – wählen Sie eine bestimmte Anwendung aus, indem Sie in der Befehlszeile für die Anwendung eingeben. Nur die ausgewählte Anwendung wird veröffentlicht.

-   Als Menü: Wählen Sie einen Ordner aus, der mehrere Anwendungen enthält. Alle Anwendungen innerhalb des Ordners werden veröffentlicht und als Menü angezeigt.

## <a href="" id="bkmk-addingapublishedapplication"></a>So wird es gemacht: Hinzufügen einer veröffentlichten Anwendung zu einem MED-V-Arbeitsbereich


**So fügen Sie dem MED-V-Arbeitsbereich eine Anwendung hinzu**

1.  Klicken Sie auf den MED-V-Arbeitsbereich, den Sie konfigurieren möchten.

2.  Klicken Sie im Bereich **Anwendungen** im Abschnitt **veröffentlichte Anwendungen** auf **Hinzufügen** , um eine neue Anwendung hinzuzufügen.

3.  Konfigurieren Sie die Anwendungseigenschaften wie in der folgenden Tabelle beschrieben.

4.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

    **Hinweis:**  
    Wenn Sie Internet Explorer als veröffentlichte Anwendung festlegen, um sicherzustellen, dass die webumleitung ordnungsgemäß funktioniert, stellen Sie sicher, dass alle Parameter nicht in Klammern stehen.



**Veröffentlichte Anwendungseigenschaften**

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
<td align="left"><p>Aktiviert</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, um die veröffentlichte Anwendung zu aktivieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anzeigename</p></td>
<td align="left"><p>Der Name der Verknüpfung im Windows-Startmenü des Benutzers&#39;.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Bei dem Anzeigenamen wird die <strong> </strong> Groß-/Kleinschreibung nicht berücksichtigt.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Eine Beschreibung der veröffentlichten Anwendung, die als QuickInfo angezeigt wird, wenn der Mauszeiger des Benutzers&#39;auf die Verknüpfung zeigt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Befehlszeile</p></td>
<td align="left"><p>Der Befehl, mit dem die Anwendung innerhalb des MED-V-Arbeitsbereichs ausgeführt wird. Der vollständige Pfad ist erforderlich, und die Parameter können auf ähnliche Weise wie in jedem anderen Windows-Befehl an die Anwendung übergeben werden.</p>
<p>In einem revertible MED-V-Arbeitsbereich können Sie ein Netzlaufwerk mit MapNetworkDrive-Syntax zuordnen: &quot; <em> MapNetworkDrive-Laufwerk Pfad, Beispiels &lt; &gt; &lt; &gt; </em> &quot; Weise &quot; <em> MapNetworkDrive t: \tux\date </em> &quot; .</p>
<p>Verwenden Sie beispielsweise zum Veröffentlichen von Windows-Explorer die folgende Syntax: &quot; <em> c: &lt; /EM &gt; &quot; oder &quot; <em> c:\Windows </em> .&quot;</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Um eine Namensauflösung zu haben, müssen Sie eine der folgenden Aktionen ausführen:</p>
</div>
<div>

</div>
<ul>
<li><p>Konfigurieren Sie den DNS im Basis-Bild des MED-V-Arbeitsbereichs.</p></li>
<li><p>Überprüfen Sie, ob die DNS-Auflösung im Host definiert ist, und konfigurieren Sie Sie für die Verwendung des Host-DNS.</p></li>
<li><p>Verwenden Sie die IP-Adresse, um das Netzlaufwerk zu definieren.</p></li>
</ul>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn der Pfad Leerzeichen enthält, muss der gesamte Pfad in Anführungszeichen stehen.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Der Pfad sollte nicht mit einem umgekehrten Schrägstrich () enden.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Startmenü</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, um im Windows-Startmenü der Benutzer&#39;eine Verknüpfung für die Anwendung zu erstellen.</p></td>
</tr>
</tbody>
</table>



Alle veröffentlichten Anwendungen werden im Windows- **Startmenü** als Verknüpfungen angezeigt (**Starten Sie &gt; Alle Programme &gt; MED-V-Anwendungen**).

## Entfernen einer veröffentlichten Anwendung aus einem MED-V-Arbeitsbereich


**So entfernen Sie eine Anwendung aus dem MED-V-Arbeitsbereich**

1.  Klicken Sie auf einen MED-V-Arbeitsbereich.

2.  Wählen Sie im Bereich **Anwendungen** im Abschnitt **veröffentlichte Anwendungen** eine Anwendung aus, die entfernt werden soll.

3.  Klicken Sie auf **Entfernen**.

    Die Anwendung wird aus der Liste der veröffentlichten Anwendungen entfernt.

4.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

## So wird es gemacht: Hinzufügen eines veröffentlichten Menüs zu einem MED-V-Arbeitsbereich


**So fügen Sie dem MED-V-Arbeitsbereich ein veröffentlichtes Menü hinzu**

1.  Klicken Sie auf den MED-V-Arbeitsbereich, den Sie konfigurieren möchten.

2.  Klicken Sie im Bereich **Anwendungen** im Abschnitt **veröffentlichte Menüs** auf **Hinzufügen** , um ein neues Menü hinzuzufügen.

3.  Konfigurieren Sie die Menü Eigenschaften wie in der folgenden Tabelle beschrieben.

4.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

**Veröffentlichte Menü Eigenschaften**

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
<td align="left"><p>Aktiviert</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, um das Menü "veröffentlicht" zu aktivieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anzeigename</p></td>
<td align="left"><p>Der Name der Verknüpfung im Windows-Startmenü des Benutzers&#39;.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Die Beschreibung, die als QuickInfo angezeigt wird, wenn die Maus des Benutzers&#39;auf die Verknüpfung zeigt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ordner im Arbeitsbereich</p></td>
<td align="left"><p>Wählen Sie den Ordner aus, der als Menü veröffentlicht werden soll, in dem alle Anwendungen innerhalb des Ordners enthalten sind.</p>
<p>Der angezeigte Text ist ein relativer Pfad aus dem Ordner "Programme".</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn diese Option leer bleibt, werden alle Programme auf dem Host als Menü veröffentlicht.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Alle veröffentlichten Menüs werden im Windows- **Startmenü** als Verknüpfungen angezeigt (** &gt; Alle Programme starten &gt; MED-V-Anwendungen**). Sie können den Namen der Verknüpfung im Ordner Feld " **Start-Menüverknüpfungen"** ändern.

**Hinweis:**  
Bei der Konfiguration von zwei MED-V-Arbeitsbereichen empfiehlt es sich, einen anderen Namen für den Ordner "Start-Menüverknüpfungen" zu konfigurieren.



## So entfernen Sie ein veröffentlichtes Menü aus einem MED-V-Arbeitsbereich


**So entfernen Sie ein veröffentlichtes Menü aus einem MED-V-Arbeitsbereich**

1.  Klicken Sie auf einen MED-V-Arbeitsbereich.

2.  Wählen Sie im Bereich **Anwendungen** im Abschnitt **veröffentlichte Menüs** ein zu entfernendes Menü aus.

3.  Klicken Sie auf **Entfernen**.

    Das Menü wird aus der Liste der veröffentlichten Menüs entfernt.

4.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

## Ausführen einer veröffentlichten Anwendung über eine Befehlszeile auf dem Client


Mit dem folgenden Befehl kann der Administrator veröffentlichte Anwendungen von einem beliebigen Ort aus ausführen, beispielsweise eine Desktopverknüpfung:

``` syntax
"<Install path>\Manager\KidaroCommands.exe" /run "<published application name>" "<MED-V workspace name>"
```

**Hinweis:**  
Der MED-V-Arbeitsbereich, in dem die veröffentlichte Anwendung definiert ist, muss ausgeführt werden.



## Verwandte Themen


[So bearbeiten Sie eine veröffentlichte Anwendung mit erweiterten Einstellungen](how-to-edit-a-published-application-with-advanced-settings.md)

[Über die Benutzeroberfläche der MED-V-Management-Konsole](using-the-med-v-management-console-user-interface.md)

[Erstellen eines MED-V-Arbeitsbereichs](creating-a-med-v-workspacemedv-10-sp1.md)









