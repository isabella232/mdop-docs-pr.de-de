---
title: So stellen Sie sicher, dass eine Verbindungsgruppe die Paketversion ignoriert
description: So stellen Sie sicher, dass eine Verbindungsgruppe die Paketversion ignoriert
author: dansimp
ms.assetid: 6ebc1bff-d190-4f4c-a6da-e09a4cca7874
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b64d1938419aef184c5df667bf71b8157de0450a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805369"
---
# So stellen Sie sicher, dass eine Verbindungsgruppe die Paketversion ignoriert


Microsoft Application Virtualization (App-V) 5,0 SP3 ermöglicht es Ihnen, eine Verbindungsgruppe so zu konfigurieren, dass Sie eine beliebige Version eines Pakets verwendet, wodurch Paketaktualisierungen vereinfacht und die Anzahl der zu erstellenden Verbindungsgruppen verringert wird.

Zum Upgrade eines Pakets in früheren Versionen von App-V mussten mehrere Schritte ausgeführt werden, einschließlich der Deaktivierung der Verbindungsgruppe und der Änderung der XML-Definitionsdatei der Verbindungsgruppe.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabenbeschreibung mit App-V 5,0 SP3</th>
<th align="left">Durchführen der Aufgabe mit App-V 5,0 SP3</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sie können eine Verbindungsgruppe so konfigurieren, dass Sie eine beliebige Version eines Pakets akzeptiert, mit der Sie das Paket aktualisieren können, ohne die Verbindungsgruppe deaktivieren zu müssen.</p>
<p><strong>Funktionsweise des Features:</strong></p>
<ul>
<li><p>Wenn die Verbindungsgruppe Zugriff auf mehrere Versionen eines Pakets hat, wird die neueste Version verwendet.</p></li>
<li><p>Wenn die Verbindungsgruppe ein optionales Paket enthält, das eine falsche Version aufweist, wird das Paket ignoriert und verhindert, dass die virtuelle Umgebung der Verbindungsgruppe nicht erstellt wird.</p></li>
<li><p>Wenn die Verbindungsgruppe ein nicht optionales Paket enthält, das eine falsche Version aufweist, kann die virtuelle Umgebung der Verbindungsgruppe nicht erstellt werden.</p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Schritte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Server – Verwaltungskonsole</p></td>
<td align="left"><ol>
<li><p>Wählen Sie in der Verwaltungskonsole <strong> Pakete für </strong> &gt; <strong> Verbindungsgruppen aus </strong> .</p></li>
<li><p>Wählen Sie in der Bibliothek Verbindungsgruppen die richtige Verbindungsgruppe aus.</p></li>
<li><p>Klicken <strong> Sie </strong> im Bereich verbundene Pakete auf Bearbeiten.</p></li>
<li><p>Aktivieren Sie <strong> </strong> das Kontrollkästchen beliebige Version verwenden neben dem Paketnamen, und klicken Sie auf über <strong> nehmen </strong> .</p></li>
</ol>
<p>Weitere Informationen zum Hinzufügen oder Aktualisieren von Paketen finden Sie unter so wird es <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)"> gemacht: Hinzufügen oder Aktualisieren von Paketen mithilfe der Verwaltungskonsole </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V-Client auf einem eigenständigen Computer</p></td>
<td align="left"><ol>
<li><p>Erstellen Sie das XML-Dokument der Verbindungsgruppe.</p></li>
<li><p>Um das Paket zu aktualisieren, setzen Sie das <strong> Package </strong> Tag-Attribut <strong> </strong> auf ein Sternchen ( <strong>*</strong> ).</p></li>
<li><p>Verwenden Sie das folgende Cmdlet, um die Verbindungsgruppe hinzuzufügen, und fügen Sie den Pfad zum XML-Dokument der Verbindungsgruppe hinzu:</p>
<p><strong>Add-AppvClientConnectionGroup</strong></p></li>
<li><p>Wenn Sie ein Paket aktualisieren, verwenden Sie die folgenden Cmdlets zum Entfernen des alten Pakets, Hinzufügen des aktualisierten Pakets und Veröffentlichen des aktualisierten Pakets:</p>
<ul>
<li><p>RemoveAppvClientPackage</p></li>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Publish-AppvClientPackage</p></li>
</ul></li>
</ol>
<p>Weitere Informationen finden Sie unter:</p>
<ul>
<li><p>Die XML-Beispieldatei, <strong> Verbindungsgruppen-XML-Datei mit optionalen Paketen </strong> , in diesem Abschnitt: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"> Verwenden optionaler Pakete in Verbindungsgruppen</a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell</a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## Verwandte Themen


[Verwalten von Verbindungsgruppen](managing-connection-groups.md)

 

 





