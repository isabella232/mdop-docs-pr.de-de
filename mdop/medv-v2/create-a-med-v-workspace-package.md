---
title: Erstellen eines MED-V-Arbeitsbereichspakets
description: Erstellen eines MED-V-Arbeitsbereichspakets
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809850"
---
# Erstellen eines MED-V-Arbeitsbereichspakets


Ein Med-v-Arbeitsbereich ist die Windows XP-Desktopumgebung, in der Endbenutzer mit dem virtuellen Computer interagieren, der von Med-v bereitgestellt wird. Der Administrator erstellt und passt den MED-V-Arbeitsbereich an. Der Arbeitsbereich besteht aus einem Bild und der Gruppenrichtlinie, die die Regeln und Funktionen des MED-V-Arbeitsbereichs definiert.

Sie können mehrere MED-V-Arbeitsbereiche erstellen, die jeweils mit eigener Konfiguration, Einstellungen und Regeln angepasst werden. Jedem MED-V-Arbeitsbereich können Benutzer, Gruppen oder mehrere Benutzer oder Gruppen zugeordnet werden. Durch die Anpassung wird dieser MED-V-Arbeitsbereich nur für diesen Benutzer oder diese Gruppe zur Verfügung gestellt.

Verwenden Sie den **Med-v Workspace-Paketer** zum Erstellen von Med-v-Arbeitsbereichen. Der **MED-V Workspace-Paketer** ist in zwei Hauptabschnitte unterteilt:

-   Ein Hauptbereich mit drei Schaltflächen, die Sie zum Erstellen und Verwalten von MED-V-Arbeitsbereichen verwenden. Mit der Schaltfläche " **Med-v Workspace-Paket erstellen** " wird der Assistent zum Erstellen eines **Med-v-Arbeitsbereichs Pakets** geöffnet, mit dem Sie Ihre Med-v-Arbeitsbereiche erstellen.

-   Ein **Hilfe Center** auf der rechten Seite des Fensters, in dem Sie Informationen und Anleitungen zum Erstellen, testen und Verwalten Ihrer MED-V-Arbeitsbereiche finden.

**Wichtig**  
Bevor Sie den **MED-V-Arbeitsbereichs-Packager**verwenden können, müssen Sie zuerst sicherstellen, dass die Windows PowerShell-Ausführungsrichtlinie auf Unrestricted festgesetzt ist.

`Set-ExecutionPolicy Unrestricted`

Darüber hinaus muss die San-Richtlinie für den Computer, auf dem der **MED-V Workspace-Paketer** ausgeführt wird, auf "Online alle" eingestellt sein. Führen Sie die folgenden Befehle an einer Eingabeaufforderung mit Administratorrechten aus, um die Einstellung der San-Richtlinie zu überprüfen:

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

Wenn dies erforderlich ist, ändern Sie die San-Richtlinie in "Online alle", indem Sie an der Eingabeaufforderung die folgenden Befehle mit Administratoranmeldeinformationen eingeben:

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**Wichtig**  
Wenn die automatische datenträgerverschlüsselungssoftware auf dem Computer installiert ist, den Sie zum Bereitstellen der virtuellen Festplatte und zum Erstellen des MED-V-Arbeitsbereichs Pakets verwenden, müssen Sie die Software vor dem Start deaktivieren. Andernfalls können Sie den MED-V-Arbeitsbereich nicht auf einem anderen Computer verwenden.



Die hier bereitgestellten Informationen können Ihnen beim Erstellen Ihres MED-V Workspace-Bereitstellungspakets helfen.

## <a href="" id="bkmk-prereq"></a>Voraussetzungen


Bevor Sie mit dem Erstellen Ihres MED-V Workspace-Bereitstellungspakets beginnen, stellen Sie sicher, dass Sie Zugriff auf die folgenden Elemente haben:

-   **Ein vorbereitetes Windows XP-Abbild**

    Weitere Informationen zum Erstellen eines Windows XP-Images zur Verwendung mit Med-v finden Sie unter [Vorbereiten eines Med-v-Abbilds](prepare-a-med-v-image.md).

-   **Eine Textdatei oder Liste, die URL-Umleitungsinformationen enthält**

    Ihre URL-Umleitungs Textdatei oder-Liste enthält die URLs, die Sie vom Hostcomputer zu Internet Explorer im MED-V-Arbeitsbereich weiterleiten möchten. Wenn Sie den Verpackungs-Assistenten zum Erstellen Ihres MED-V-Arbeitsbereichs verwenden, können Sie diese Umleitungsinformationen importieren, eingeben oder kopieren und als einen der Schritte im Paketerstellungsprozess einfügen.

    **Hinweis:**  
    Die URL-Umleitung in MED-V unterstützt nur die Protokolle http und HTTPS. MED-V bietet keine Unterstützung für FTP oder andere Protokolle.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## Verpacken eines Med-v-Arbeitsbereichs für eine andere Sprache als die Sprache des Med-v-Arbeitsbereichs-Paket Computers


Standardmäßig unterstützt der MED-V-Arbeitsbereich Zeichen sowohl in der Sprache des Computers als auch in Englisch. Wenn Sie einen Med-v-Arbeitsbereich für eine Sprache erstellen möchten, die nicht auf dem Computer installiert ist, geben Sie **-Loc \ [Gebietsschema \]** im PowerShell-Skript (. ps1) nach dem Med-v-Arbeitsbereichsnamen ein.

Wenn Sie ein Med-v-Arbeitsbereichs Paket in einer anderen Sprache als der Standardsprache des Med-v Workspace-Paket Computers erstellen möchten, generieren Sie ein Skript in der Standardsprache, indem Sie den Med-v-Arbeitsbereichs-Paketdienst ausführen und dann das Ausgabeskript nach Bedarf für Ihr Gebietsschema ändern. Das Skript befindet sich im MED-V Workspace-Ausgabeverzeichnis, das während der Verpackung angegeben wurde. Die Namen der Gebietsschemaeinstellungen befinden sich auf der. BXL-Dateien im folgenden Verzeichnis:

C:\\Programme c:\\Programme\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.medv.Administration.Commands.WorkspacePackager\\locale

## Erstellen eines MED-V-Arbeitsbereichs Pakets


Führen Sie die folgenden Schritte aus, um ein MED-V-Arbeitsbereichs Paket zu erstellen:

****

1.  Klicken Sie zum Öffnen des **Med-v Workspace-Pakets**auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **Med-v Workspace Packager**.

2.  Klicken Sie im Hauptbereich des **Med-v Workspace-Pakets** auf **Med-v Workspace-Paket erstellen**.

    Der Med-v- **Assistent zum Erstellen eines Med-v-Arbeitsbereichs Pakets** wird angezeigt. Der Assistent besteht aus den folgenden Seiten:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Paketinformationen</strong></p></td>
    <td align="left"><p>Geben Sie einen Namen für den Med-v-Arbeitsbereich an, und wählen Sie einen Ordner aus, in dem die Med-v Workspace-Paketdateien gespeichert werden.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Windows XP-Abbild auswählen</strong></p></td>
    <td align="left"><p>Geben Sie Ihr vorbereitetes Windows XP Virtual PC-Abbild an.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Erstmaliges Einrichten</strong></p></td>
    <td align="left"><p>Geben Sie den Setupprozess an, dem MED-V bei der erstmaligen Einrichtung folgt.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>MED-V-Nachrichten</strong></p></td>
    <td align="left"><p>Geben Sie die Nachrichten und die optionale URL für Hilfeinformationen an, die der Endbenutzer während der erstmaligen Einrichtung sieht.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Benennen von Computern</strong></p></td>
    <td align="left"><p>Geben Sie an, wie der virtuelle MED-V-Computer benannt wird.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Kopieren von Einstellungen vom Host</strong></p></td>
    <td align="left"><p>Geben Sie an, wie die Einstellungen für den MED-V-Arbeitsbereich definiert werden.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Start und Netzwerk</strong></p></td>
    <td align="left"><p>Geben Sie die Einstellungen für den Start des MED-V Workspace, der Netzwerk-und der Benutzeranmeldeinformationen an.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Web-Umleitung</strong></p></td>
    <td align="left"><p>Geben Sie eine Textdatei oder eine Liste der URLs an, die Sie im MED-V-Arbeitsbereich an Internet Explorer weitergeleitet werden sollen.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Zusammenfassung</strong></p></td>
    <td align="left"><p>Überprüfen Sie Ihre Med-v Workspace-Einstellungen, und beginnen Sie mit dem Erstellen Ihres Med-v Workspace-Bereitstellungspakets.</p></td>
    </tr>
    </tbody>
    </table>



3.  Geben Sie auf der Seite **Paketinformationen** einen Namen für den Med-v-Arbeitsbereich ein, und wählen Sie einen Ordner aus, in dem die Med-v-Arbeitsbereichs Paketdateien gespeichert werden.

    **Warnung**  
    Sie müssen den MED-V-Arbeitsbereich benennen und einen Ordner angeben, um fortzufahren.



~~~
After you have finished, click **Next**.
~~~

4. Geben Sie auf der Seite **Windows XP-Abbild auswählen** den Speicherort Ihres vorbereiteten MED-V Windows XP Virtual PC-Bilds an (VHD-Datei).

   **Warnung**  
   Sie müssen ein Windows XP VHD-Abbild angeben, um fortfahren zu können.



~~~
After you have finished, click **Next**.
~~~

5. Wählen Sie auf der Seite für die **erstmalige Einrichtung** aus, ob die erstmalige Einrichtung ausgeführt werden soll, während Sie besucht oder unbeaufsichtigt sind, und ob Sie den MED-V-Arbeitsbereich separat verwenden oder von allen Endbenutzern auf einem freigegebenen Computer verwenden möchten.

   Wenn Sie die **unbeaufsichtigte Installation ohne Benachrichtigung**auswählen, wird der Endbenutzer nicht informiert, bevor das erstmalige Setup ausgeführt wird und der virtuelle Computer dem Endbenutzer während der erstmaligen Einrichtung nicht angezeigt wird. Darüber hinaus ist die Seite **MED-V-Nachrichten** des Assistenten ausgeblendet, da keine Nachrichten erforderlich sind, wenn die erstmalige Einrichtung in einem vollständig unbeaufsichtigten Modus ausgeführt wird.

   Wenn Sie die Option **unbeaufsichtigtes Setup auswählen, aber Endbenutzer Benachrichtigen, bevor das erstmalige Setup beginnt**, wird der Endbenutzer informiert, bevor die erstmalige Einrichtung ausgeführt wird. Bei der erstmaligen Einrichtung wird der virtuelle Computer dem Endbenutzer jedoch nicht angezeigt.

   Wählen Sie **beaufsichtigte Einrichtung** aus, wenn der Endbenutzer während der erstmaligen Einrichtung Informationen eingeben muss.

   Das Standardverhalten ist die **unbeaufsichtigte Installation, aber die Endbenutzer werden benachrichtigt, bevor das erstmalige Setup beginnt**.

   **Achtung**  
   Wenn Sie die Datei "Sysprep. inf" erstellt haben, damit für das Mini Setup eine Benutzereingabe erforderlich ist, müssen Sie " **beaufsichtigte Einrichtung** " auswählen oder während der erstmaligen Einrichtung Probleme auftreten.



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. Geben Sie auf der Seite **MED-V-Nachrichten** die folgenden Nachrichten an, die der Endbenutzer während der erstmaligen Einrichtung sieht:

   -   Die Meldung, die der Endbenutzer beim Starten der erstmaligen Einrichtung sieht.

   -   Die Meldung, die der Endbenutzer sieht, wenn die erstmalige Einrichtung fehlschlägt oder ein Fehler auftritt.

   **Hinweis:**  
   Die Seite **MED-V-Nachrichten** des Assistenten wird ausgeblendet, wenn Sie die **unbeaufsichtigte Installation ohne Benachrichtigung** auf der Seite zum **erstmaligen Einrichten** ausgewählt haben.



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. Auf der Seite **Naming Computers** können Sie angeben, ob die Computerbenennung von MED-V oder von einem Systemverwaltungstool wie Sysprep verwaltet wird. Standardmäßig wird die Computer Namensgebung von einem Systemverwaltungstool verwaltet.

   Wenn Sie angeben, dass die Computerbenennung von MED-V verwaltet wird, wählen Sie in der Dropdownliste eine vordefinierte computernaming Convention (Maske) aus. Eine Vorschau eines Beispiel Computernamens wird angezeigt, die auf dem Computer basiert, den Sie zum Erstellen des MED-V-Arbeitsbereichs Pakets verwenden.

   Wenn Sie eine der benutzerdefinierten Benennungskonventionen auswählen, sind die Felder, die Sie angeben können, auf die folgenden Zeichen limitiert:

   -   Die Felder "Präfix" und "Suffix" sind auf die Zeichen a-z, a-z, 0-9 und die Sonderzeichen limitiert! @ \ # $% ^ & ()-\ _ ' {}. und ~.

   -   Die Felder Hostname und username sind auf die Ziffern 0 bis 9 limitiert.

   **Wichtig**  
   Computer Namen müssen eindeutig sein und auf maximal 15 Zeichen limitiert sein. Wenn Sie sich für Ihre Computer Benennungsmethode entscheiden, sollten Sie die Endbenutzer in Frage stellen, die über mehrere Computer verfügen oder einen Computer freigeben, und vermeiden Sie die Verwendung von Computernamens Masken, die zu einer Kollision im Netzwerk führen können.



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. Auf der Seite **Einstellungen von Host kopieren** können Sie die folgenden Einstellungen auswählen, um anzugeben, wie der MED-V-Arbeitsbereich konfiguriert werden soll:

   **Achtung**  
   Die Einstellungen, die Sie auf dieser Seite angeben, die vom Hostcomputer in den MED-V-Arbeitsbereich kopiert werden, überschreiben die in der Antwortdatei "Sysprep. inf" angegebenen.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. Auf der Seite **Start und Netzwerk** können Sie das Standardverhalten für die folgenden Einstellungen ändern:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Starten des MED-V-Arbeitsbereichs</strong></p></td>
   <td align="left"><p>Wählen Sie aus, ob der Med-v-Arbeitsbereich bei der Benutzeranmeldung bei der ersten Verwendung gestartet oder der Endbenutzer entscheiden soll, wann der Med-v-Arbeitsbereich gestartet wird.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>Der Arbeitsbereich Med-v beginnt auf eine von zwei Arten: entweder beim Anmelden des Endbenutzers oder beim ersten Starten einer Aktion, für die Med-v erforderlich ist, beispielsweise das Öffnen einer veröffentlichten Anwendung oder das Eingeben einer URL, die eine Umleitung erfordert.</p>
   <p>Sie können diese Einstellung für den Endbenutzer definieren oder zulassen, dass der Endbenutzer steuert, wie MED-V gestartet wird.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Wenn Sie angeben, dass der Endbenutzer entscheidet, besteht das Standardverhalten darin, dass der MED-V-Arbeitsbereich bei der Anmeldung gestartet wird. Sie können die Standardeinstellung ändern, indem Sie mit der rechten Maustaste auf das Med-v-Symbol im Infobereich klicken und dann <strong> Med-v-Benutzereinstellungen auswählen </strong> . Wenn Sie diese Einstellung für den Endbenutzer definieren, können Sie nicht ändern, wie MED-V gestartet wird.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Networking</strong></p></td>
   <td align="left"><p>Wählen <strong> Sie </strong> <strong> </strong> für Ihre Netzwerkeinstellung freigegeben oder überbrückt aus. Der Standardwert ist <strong> Shared </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>Shared </strong> - der MED-V Workspace verwendet die Netzwerkadressübersetzung (Network Address Translation, NAT), um die IP-Adresse des Host-&#39;für ausgehenden Datenverkehr freizugeben.</p>
   <p><strong>Überbrückt </strong> - der MED-V-Arbeitsbereich verfügt über eine eigene Netzwerkadresse, die in der Regel über DHCP abgerufen wird.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Speichern von Anmeldeinformationen</strong></p></td>
   <td align="left"><p>Wählen Sie aus, ob die Endbenutzeranmeldeinformationen gespeichert werden sollen.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>Das Standardverhalten ist, dass die Speicherung von Anmeldeinformationen deaktiviert ist, damit der Endbenutzer bei jeder Anmeldung authentifiziert werden muss.</p>
   <div class="alert">
   <strong>Wichtig</strong><br/><p>Auch wenn die Zwischenspeicherung der Anmeldeinformationen des Endbenutzers die beste Benutzererfahrung bietet, sollten Sie sich mit den damit verbundenen Risiken vertraut machen.</p>
   <p>Die Domänenanmeldeinformationen des Endbenutzers werden in einem reversiblen Format im Windows-Anmelde Informations-Manager gespeichert. Daher kann ein Angreifer ein Programm schreiben, das das Kennwort abruft und Zugriff auf die Anmeldeinformationen des Benutzers erhält. Sie können dieses Risiko nur verringern, indem Sie die Speicherung von Anmeldeinformationen des Endbenutzers deaktivieren.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. Auf der Seite " **webumleitung** " können Sie eine Liste der URLs eingeben, einfügen oder importieren, die im MED-V-Arbeitsbereich an Internet Explorer umgeleitet werden. Weitere Informationen zum Konfigurieren der URL-Umleitungsinformationen finden Sie unter [Voraussetzungen](#bkmk-prereq).

   Sie können auch angeben, wie Internet Explorer im MED-V-Arbeitsbereich für Endbenutzer konfiguriert ist. Standardmäßig ist die Sicherheitsstufe Internet Zone auf hoch festgesetzt. Darüber hinaus werden bestimmte Standardbrowserfunktionen wie die Adressleiste entfernt. Diese Standardkonfiguration von Internet Explorer im MED-V-Arbeitsbereich bietet eine sicherere Browserumgebung für Endbenutzer.

   **Achtung**  
   Wenn Sie die Standardeinstellungen ändern, können Sie Internet Explorer im MED-V-Arbeitsbereich anpassen. Beachten Sie jedoch, dass Sie die Sicherheitsrisiken, die in älteren Versionen von Internet Explorer vorhanden sind, wenn Sie die Standardeinstellungen so ändern, dass Sie nicht so sicher sind, für Ihre Organisation verfügbar machen können. Weitere Informationen finden Sie unter [bewährte Methoden für die Sicherheit von MED-V-Vorgängen](security-best-practices-for-med-v-operations.md).



~~~
After you have finished, click **Next**.
~~~

11. Auf der **Zusammenfassungs** Seite können Sie die Verpackungs Einstellungen für diesen MED-V-Arbeitsbereich überprüfen. Wenn Sie Einstellungen ändern möchten, klicken Sie auf die Schaltfläche **zurück** , um zur entsprechenden Seite zurückzukehren. Nachdem Sie die Überprüfung der Einstellungen vorgenommen haben, klicken Sie auf **Erstellen**.

   Die Seite **Fertigstellung** des **Assistenten zum Erstellen von MED-V Workspace-Paketen** wird geöffnet, um den Fortschritt der Paketerstellung anzuzeigen.

   **Hinweis:**  
   Je nach Größe der festgelegten Festplatte kann es einige Minuten dauern, bis der Prozess des MED-V-Arbeitsbereichs Pakets abgeschlossen ist.



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. Klicken Sie auf **Schließen** , um den Verpackungs-Assistenten zu schließen und zum **MED-V Workspace-Paketer**zurückzukehren.

Ihr MED-V Workspace-Paket kann jetzt vor der Bereitstellung getestet werden.

## Verwandte Themen


[Konfigurieren von erweiterten Einstellungen mit Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md)

[Testen des MED-V-Arbeitsbereichspakets](testing-the-med-v-workspace-package.md)

[Vorbereiten eines MED-V-Images](prepare-a-med-v-image.md)









