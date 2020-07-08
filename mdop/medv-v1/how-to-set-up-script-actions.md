---
title: So richten Sie Skriptaktionen ein
description: So richten Sie Skriptaktionen ein
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804190"
---
# So richten Sie Skriptaktionen ein


Der Skript Aktions-Editor ermöglicht es dem Administrator, Aktionen zu erstellen, die während der Einrichtung des MED-V-Arbeitsbereichs durchgeführt werden sollen, sowie die Reihenfolge zu definieren, in der Sie ausgeführt werden.

Im folgenden finden Sie eine Liste der Aktionen, die dem Domänen Setupskript hinzugefügt werden können:

-   **Windows neu starten**– starten Sie Windows neu.

-   **Beitreten**zu einer Domäne: Fügen Sie bei der Teilnahme an einer Domäne diese Aktion ein, und konfigurieren Sie den Benutzernamen, das Kennwort, den vollqualifizierten Domänennamen, den NetBIOS-Domänennamen und die Organisationseinheit (optional).

-   **Überprüfen der Konnektivität**– konfigurieren Sie einen Server für die Verbindung, und überprüfen Sie, ob der MED-V-Arbeitsbereich eine Verbindung mit einer Netzwerkressource (wie dem Domänenserver) herstellen kann.

-   **Befehlszeile**– konfigurieren Sie ein Skript im MED-V-Arbeitsbereich, und geben Sie eine Befehlszeile mit dem Pfad des Skripts und den Skript Argumenten ein.

-   **Computer umbenennen**– benennen Sie den virtuellen Computer basierend auf den definierten Einstellungen um.

-   **Deaktivieren der automatischen Anmeldung**: Deaktivieren Sie die automatische Windows-Anmeldung. Diese Aktion sollte am Ende der Skripts hinzugefügt werden, mit denen der Computer der Domäne hinzugefügt wird.

## <a href="" id="how-to-set-up-script-actions-"></a>So richten Sie Skriptaktionen ein


**So richten Sie Skriptaktionen ein**

1.  Klicken Sie auf der Registerkarte **VM-Setup** auf **Skript-Editor**.

2.  Klicken Sie im Dialogfeld **Skriptaktionen** auf **Hinzufügen**, und klicken Sie im Untermenü auf die gewünschten Aktionen.

3.  Konfigurieren Sie die Aktionen wie in den folgenden Tabellen beschrieben.

    **Hinweis** 
     **Computer umbenennen** ist auf der Registerkarte **VM-Einstellungen** konfiguriert. Weitere Informationen finden Sie unter [Konfigurieren von Eigenschaften des VM-Computer namens Musters](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. Legen Sie die Reihenfolge der Aktionen fest, indem Sie eine Aktion auswählen und auf nach **oben** oder **unten**klicken.

5. Klicken Sie auf **OK**.

**Hinweis**  
Wenn Sie das Skript für die Join-Domäne ausführen und das Skript funktionieren soll, muss der Benutzer, der sich beim virtuellen Computer des MED-V-Arbeitsbereichs angemeldet hat, über lokale Administratorrechte verfügen.



**Hinweis:**  
Beim Ausführen des Skripts zum Deaktivieren der automatischen Anmeldung wird empfohlen, das für die automatische Anmeldung verwendete lokale Gastkonto zu deaktivieren, sobald die anfängliche Einrichtung abgeschlossen ist.



### <a href="" id="bkmk-joindomainproperties"></a>

**Domäneneigenschaften beitreten**

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
<td align="left"><p>Zu verwendende Anmeldeinformationen, wenn Sie den virtuellen Computer zur Domäne hinzugefügt haben</p></td>
<td align="left"><p>Wählen Sie eine der folgenden Anmeldeinformationen aus, die Sie verwenden können, wenn Sie den virtuellen Computer zur Domäne hinzugefügt haben:</p>
<ul>
<li><p><strong>Verwenden Sie MED-V-Anmeldeinformationen </strong> – die Anmeldeinformationen für Endbenutzer.</p></li>
<li><p><strong>Verwenden Sie die folgenden Anmeldeinformationen </strong> – die angegebenen Anmeldeinformationen; geben Sie einen Benutzernamen und ein Kennwort in die entsprechenden Felder ein.</p></li>
</ul>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Die von Ihnen eingegebenen Anmeldeinformationen sind für alle MED-V Workspace-Benutzer sichtbar. Es wird nicht empfohlen, Domänenadministrator-Anmeldeinformationen bereitzustellen.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Domäne für den Beitritt</p></td>
<td align="left"><p>Wählen Sie eine der folgenden Optionen:</p>
<ul>
<li><p><strong>Verwenden Sie den beim Starten des Arbeitsbereichs verwendeten Domänennamen </strong> – nehmen Sie an der Domäne Teil, die vom Endbenutzer beim Anmelden beim MED-V-Client eingegeben wurde.</p>
<p>Klicken Sie auf <strong> globale Domänenzuordnungstabelle, um die Zuordnung von NetBIOS zu vollqualifizierten Domänennamen zu definieren </strong> . Klicken Sie in der Tabelle globale Domänenzuordnung auf <strong> Hinzufügen </strong> , geben Sie einen <strong> NetBIOS-Domänennamen </strong> und einen <strong> vollqualifizierten Domänennamen ein </strong> , und klicken Sie auf <strong> OK </strong> .</p></li>
<li><p><strong>Verwenden Sie den folgenden Domänennamen </strong> – nehmen Sie an der angegebenen Domäne Teil; geben Sie einen Domänennamen und einen NetBIOS-Domänennamen in die entsprechenden Felder ein.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Organisationseinheit</p></td>
<td align="left"><p>Eine Organisationseinheit (OU) kann angegeben werden, um den Computer mit einer bestimmten OU zu verbinden. Das Format muss einem definierten ou-Namen folgen: OU = &lt; Organisationseinheit &gt; , &lt; Domänen Controller (Beispiels &gt; Weise ou = QATest, DC = Il, DC = MED-V, DC = com).</p>
<div class="alert">
<strong>Warnung</strong><br/><p>Es wird nur eine OU für einzelne Ebenen unterstützt, wie im obigen Beispiel gezeigt.</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**Überprüfen der Verbindungseigenschaften**

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
<td align="left"><p>IP-Adresse</p></td>
<td align="left"><p>Die IP-Adresse des Servers, mit dem Sie die Verbindung überprüfen möchten.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Port</p></td>
<td align="left"><p>Der Port des Servers, mit dem Sie die Verbindung überprüfen möchten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Timeout</p></td>
<td align="left"><p>Die Anzahl der Sekunden, die auf eine Antwort gewartet werden muss, bevor ein Timeout eintritt.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**Befehlszeileneigenschaften**

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
<td align="left"><p>Pfad</p></td>
<td align="left"><p>Der Pfad der Befehlszeile.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Argumente</p></td>
<td align="left"><p>Befehlszeilenargumente</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auf beenden warten</p></td>
<td align="left"><p>Aktivieren Sie das Kontrollkästchen, um auf eine Rückgabe zu warten, bevor Sie mit den Skriptaktionen fortfahren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fehler bei Fehler</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, wenn die Rückgabe nichts anderes als der angegebene Wert ist.</p>
<p>Geben Sie den Wert ein, der den Befehl als Erfolg kennzeichnet.</p>
<p>Standard: <strong> 0</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nur einmal ausführen</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, wenn die Befehlszeile nur einmal ausgeführt werden soll. Wenn das Skript fehlschlägt oder abgebrochen wird, wird dieser Befehl nicht erneut ausgeführt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Diese Befehlszeile führt zu einem Neustart von Windows im Arbeitsbereich</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, wenn die Befehlszeile nach Abschluss einen Neustart bewirkt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Interaktionen zulassen</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, wenn für den Befehl Benutzerinteraktion erforderlich ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Statusmeldung</p></td>
<td align="left"><p>Die Meldung, die dem Benutzer angezeigt werden soll, während der Befehl ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fehlermeldung</p></td>
<td align="left"><p>Nachricht, die dem Benutzer angezeigt werden soll, wenn der Befehl fehlschlägt.</p></td>
</tr>
</tbody>
</table>

 

Beim Konfigurieren der Befehlszeilenaktion können verschiedene Variablen verwendet werden, wie in der folgenden Tabelle definiert.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parameter</th>
<th align="left">Wert</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>%MEDVUser%</p></td>
<td align="left"><p>Ein authentifizierter Benutzername.</p></td>
<td align="left"><p>MED-V authentifizierter Benutzername. Der Benutzername und das Kennwort können im Setupskript für die Teilnahme an einer Domänen-VM verwendet werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%MEDVPassword%</p></td>
<td align="left"><p>Ein authentifiziertes Kennwort.</p></td>
<td align="left"><p>MED-V-authentifiziertes Kennwort. Der Benutzername und das Kennwort können im Setupskript für die Teilnahme an einer Domänen-VM verwendet werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>%MEDVDomain%</p></td>
<td align="left"><p>Konfigurierte Domäne.</p></td>
<td align="left"><p>Die in der MED-V-Authentifizierung konfigurierte Domäne. Sie kann für das VM-Setupskript verwendet werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%DesiredMachineName%</p></td>
<td align="left"><p>Computer Name</p></td>
<td align="left"><p>Der in der Verwaltungsanwendung konfigurierte eindeutige Computername. Sie kann im VM-Setupskript verwendet werden.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[So konfigurieren Sie die Eigenschaften der Namensmuster virtueller Computer](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





