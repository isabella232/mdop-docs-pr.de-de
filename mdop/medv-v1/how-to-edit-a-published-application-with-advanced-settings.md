---
title: So bearbeiten Sie eine veröffentlichte Anwendung mit erweiterten Einstellungen
description: So bearbeiten Sie eine veröffentlichte Anwendung mit erweiterten Einstellungen
author: dansimp
ms.assetid: 06a79049-9ce9-490f-aad7-fd4fdf185590
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 843aebb38f54959f209e742b398e3979acac3334
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812091"
---
# So bearbeiten Sie eine veröffentlichte Anwendung mit erweiterten Einstellungen


Nachdem eine veröffentlichte Anwendung hinzugefügt und konfiguriert wurde, kann die veröffentlichte Anwendung bearbeitet und weitere erweiterte Einstellungen konfiguriert werden.

**So bearbeiten Sie eine veröffentlichte Anwendung mit erweiterten Einstellungen**

1.  Fügen Sie im Bereich **Anwendungen** eine veröffentlichte Anwendung hinzu, und konfigurieren Sie Sie.

2.  Wählen Sie die veröffentlichte Anwendung aus, die Sie bearbeiten möchten.

3.  Klicken Sie auf **Bearbeiten**.

4.  Konfigurieren Sie im Dialogfeld **veröffentlichte Anwendung** die Parameter wie in der folgenden Tabelle beschrieben.

5.  Klicken Sie auf **OK**.

6.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

**Bearbeiten von veröffentlichten Anwendungseigenschaften**

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
<td align="left"><p>Anzeigename</p></td>
<td align="left"><p>Der Name der Verknüpfung im Windows-Startmenü des Benutzers&#39;.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Bei dem Anzeigenamen wird die <strong> </strong> Groß-/Kleinschreibung nicht berücksichtigt.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Eine Beschreibung des veröffentlichten Menüs.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Beginnen in</p></td>
<td align="left"><p>Das Verzeichnis, aus dem die Anwendung gestartet werden soll.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Der Pfad muss keine Anführungszeichen umfassen.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Befehlszeile</p></td>
<td align="left"><p>Der Befehl, mit dem die Anwendung innerhalb des MED-V-Arbeitsbereichs ausgeführt werden soll.</p>
<p>Der vollständige Pfad ist erforderlich, und die Parameter können auf ähnliche Weise wie in jedem anderen Windows-Befehl an die Anwendung übergeben werden.</p>
<p>In einer Domänenkonfiguration ist in der Regel ein freigegebenes Laufwerk auf dem Server vorhanden, dem alle Domänencomputer zugeordnet sind. Das Verzeichnis sollte hier zugeordnet werden, und wenn es sich um einen Ordner handelt, für den eine Benutzerauthentifizierung erforderlich ist, <strong> muss das Kontrollkästchen MED-V-Anmeldeinformationen zum Ausführen dieser Anwendung verwenden </strong> aktiviert sein.</p>
<p>In einem revertible MED-V-Arbeitsbereich können Sie ein Netzlaufwerk mit MapNetworkDrive-Syntax zuordnen: &quot; <em> MapNetworkDrive-Laufwerk Pfad, Beispiels &lt; &gt; &lt; &gt; </em> &quot; Weise &quot; <em> MapNetworkDrive t: \tux\data </em> &quot; .</p>
<p>Verwenden Sie beispielsweise zum Veröffentlichen von Windows-Explorer die folgende Syntax: &quot; <em> c: &amp; quot; oder &quot; c:\Windows </em> &quot; .</p>
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
<td align="left"><p>Hinzufügen einer Verknüpfung im Startmenü von Windows-Host</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, um im Windows-Startmenü der Benutzer&#39;eine Verknüpfung für die Anwendung zu erstellen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Starten dieser Anwendung beim Starten des Arbeitsbereichs</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, um die Anwendung automatisch auszuführen, wenn der MED-V-Arbeitsbereich gestartet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwenden von MED-V-Anmeldeinformationen zum Ausführen dieser Anwendung</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, um Anwendungen zu authentifizieren, die einen Benutzernamen und ein Kennwort unter Verwendung der MED-V-Anmeldeinformationen anfordern, anstatt die Anmeldeinformationen für die Anwendung festzulegen.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Bei Verwendung von SSO sollte die Befehlszeile <strong>C:\Windows\Explorer.exe &quot; Ordnerpfad sein &quot; </strong> . Wenn Sie SSO nicht verwenden, sollte die Befehlszeile &quot; <strong> Ordnerpfad sein </strong> &quot; .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[So konfigurieren Sie veröffentlichte Anwendungen](how-to-configure-published-applicationsmedvv2.md)









