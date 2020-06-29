---
title: So stellen Sie den App-V 5.1-Server bereit
description: So stellen Sie den App-V 5.1-Server bereit
author: dansimp
ms.assetid: 4729beda-b98f-481b-ae74-ad71c59b1d69
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a367be7db4cea1835124657dbdfa3375474228e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805498"
---
# So stellen Sie den App-V 5.1-Server bereit


Gehen Sie wie folgt vor, um den Microsoft Application Virtualization (App-V) 5,1-Server zu installieren. Informationen zum Bereitstellen des App-v 5,1-Servers finden Sie unter [Informationen zu app-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).

**Bevor Sie beginnen:**

-   Stellen Sie sicher, dass Sie die erforderliche Software installiert haben. Weitere Informationen finden Sie unter [App-V 5,1-Voraussetzungen](app-v-51-prerequisites.md).

-   Lesen Sie den Abschnitt Server der [Sicherheitsüberlegungen zu App-V 5,1](app-v-51-security-considerations.md).

-   Geben Sie einen Port an, in dem die einzelnen Komponenten gehostet werden.

-   Fügen Sie Firewallregeln hinzu, damit eingehende Anforderungen auf die angegebenen Ports zugreifen können.

-   Wenn Sie anstelle des Windows Installers SQL-Skripts verwenden, um die Verwaltungsdatenbank oder die Berichtsdatenbank einzurichten, müssen Sie die SQL-Skripts ausführen, bevor Sie den Verwaltungsserver oder den Berichtsserver installieren. Weitere Informationen finden Sie unter [Bereitstellen der App-V-Datenbanken mithilfe von SQL-Skripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).

**So installieren Sie den App-V 5,1-Server**

1. Kopieren Sie die App-V 5,1 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.

2. Starten Sie die App-V 5,1 Server-Installation, indem Sie mit der rechten Maustaste klicken und **appv\_server\_setup.exe** als Administrator ausführen, und klicken Sie dann auf **Installieren**.

3. Überprüfen und akzeptieren Sie die Lizenzbestimmungen, und wählen Sie aus, ob Microsoft Updates aktiviert werden soll.

4. Wählen Sie auf der Seite **Featureauswahl** alle der folgenden Komponenten aus.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Komponente</th>
   <th align="left">Beschreibung</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Verwaltungsserver</p></td>
   <td align="left"><p>Bietet allgemeine Verwaltungsfunktionen für die App-V-Infrastruktur.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Verwaltungsdatenbank</p></td>
   <td align="left"><p>Vereinfacht die Bereitstellung von Datenbanken für die App-V-Verwaltung.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Veröffentlichungsserver</p></td>
   <td align="left"><p>Bietet Hosting-und Streamingfunktionen für virtuelle Anwendungen.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Berichtsserver</p></td>
   <td align="left"><p>Bietet App-V 5,1 Reporting Services.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Berichtsdatenbank</p></td>
   <td align="left"><p>Vereinfacht die Bereitstellung von Datenbanken für die App-V-Berichterstellung.</p></td>
   </tr>
   </tbody>
   </table>

     

5. Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, an dem die ausgewählten Komponenten installiert werden sollen, oder ändern Sie den Speicherort, indem Sie einen neuen Pfad in der **Installationsstandort** Zeile eingeben.

6. Konfigurieren Sie auf der Seite erste **neue Verwaltungsdatenbank erstellen** die **Microsoft SQL Server-Instanz** und die **Verwaltungs Server-Datenbank** , indem Sie die entsprechende Option unten auswählen.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Methode</th>
   <th align="left">Was Sie tun müssen</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Sie verwenden eine benutzerdefinierte Microsoft SQL Server-Instanz.</p></td>
   <td align="left"><p>Wählen Sie <strong> die benutzerdefinierte Instanz verwenden aus </strong> , und geben Sie den Namen der Instanz ein.</p>
   <p>Verwenden Sie das Format <strong> instanceName </strong> . Der angenommene Installationsspeicherort ist der lokale Computer.</p>
   <p>Nicht unterstützt: ein Servername unter Verwendung <strong> der </strong> &lt; starken &gt; Instanz von Format Servername </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Sie verwenden einen benutzerdefinierten Datenbanknamen.</p></td>
   <td align="left"><p>Wählen Sie <strong> benutzerdefinierte Konfiguration aus </strong> , und geben Sie den Datenbanknamen ein.</p>
   <p>Der Datenbankname muss eindeutig sein, oder die Installation schlägt fehl.</p></td>
   </tr>
   </tbody>
   </table>

     

7. Übernehmen Sie auf der Seite **Konfigurieren** den Standardwert **diesen lokalen Computer verwenden**.

   **Hinweis:**  
   Wenn Sie den Verwaltungsserver und die Verwaltungsdatenbank nebeneinander installieren, stehen einige Optionen auf dieser Seite nicht zur Verfügung. In diesem Fall sind die entsprechenden Optionen standardmäßig aktiviert und können nicht geändert werden.

     

8. Konfigurieren Sie auf der ersten Seite zum **Erstellen einer neuen Berichtsdatenbank** die **Microsoft SQL Server-Instanz** und die **Berichtsserver-Datenbank** , indem Sie die entsprechende Option unten auswählen.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Methode</th>
   <th align="left">Was Sie tun müssen</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Sie verwenden eine benutzerdefinierte Microsoft SQL Server-Instanz.</p></td>
   <td align="left"><p>Wählen Sie <strong> die benutzerdefinierte Instanz verwenden aus </strong> , und geben Sie den Namen der Instanz ein.</p>
   <p>Verwenden Sie das Format <strong> instanceName </strong> . Der angenommene Installationsspeicherort ist der lokale Computer.</p>
   <p>Nicht unterstützt: ein Servername unter Verwendung <strong> der </strong> &lt; starken &gt; Instanz von Format Servername </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Sie verwenden einen benutzerdefinierten Datenbanknamen.</p></td>
   <td align="left"><p>Wählen Sie <strong> benutzerdefinierte Konfiguration aus </strong> , und geben Sie den Datenbanknamen ein.</p>
   <p>Der Datenbankname muss eindeutig sein, oder die Installation schlägt fehl.</p></td>
   </tr>
   </tbody>
   </table>

     

9. Übernehmen Sie auf der Seite **configure** den Standardwert: **verwenden Sie diesen lokalen Computer**.

   **Hinweis:**  
   Wenn Sie den Verwaltungsserver und die Verwaltungsdatenbank nebeneinander installieren, stehen einige Optionen auf dieser Seite nicht zur Verfügung. In diesem Fall sind die entsprechenden Optionen standardmäßig aktiviert und können nicht geändert werden.

     

10. Geben Sie auf der Seite **configure** (Management Server Configuration) Folgendes an:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Zu konfigurierendes Element</th>
    <th align="left">Beschreibung und Beispiele</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Geben Sie die Anzeigengruppe mit den entsprechenden Berechtigungen zum Verwalten der App-V-Umgebung ein.</p></td>
    <td align="left"><p>Beispiel: MYDOMAIN\myuser</p>
    <p>Nach der Installation können Sie weitere Benutzer oder Gruppen mithilfe der Verwaltungskonsole hinzufügen. Globale Sicherheitsgruppen und Active Directory-Domänendienste (AD DS)-Verteilergruppen werden jedoch nicht unterstützt. <strong> </strong> <strong> Zum Ausführen dieser Aktion müssen Sie eine lokale Domäne oder universelle </strong> Gruppen verwenden.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Website Name </strong> : Geben Sie den benutzerdefinierten Namen an, der zum Ausführen des Veröffentlichungs Diensts verwendet wird.</p></td>
    <td align="left"><p>Wenn Sie keinen benutzerdefinierten Namen haben, nehmen Sie keine Änderungen vor.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Portbindung </strong> : Geben Sie eine eindeutige Portnummer an, die von App-V verwendet wird.</p></td>
    <td align="left"><p>Beispiel: <strong> 12345</strong></p>
    <p>Stellen Sie sicher, dass der angegebene Port nicht von einer anderen Website verwendet wird.</p></td>
    </tr>
    </tbody>
    </table>

     

11. Geben Sie auf der Seite **Konfigurieren** der **Veröffentlichungs Server Konfiguration** Folgendes an:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Zu konfigurierendes Element</th>
    <th align="left">Beschreibung und Beispiele</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Geben Sie die URL für den Verwaltungsdienst an.</p></td>
    <td align="left"><p>Beispiel<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Website Name </strong> : Geben Sie den benutzerdefinierten Namen an, der zum Ausführen des Veröffentlichungs Diensts verwendet wird.</p></td>
    <td align="left"><p>Wenn Sie keinen benutzerdefinierten Namen haben, nehmen Sie keine Änderungen vor.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Portbindung </strong> : Geben Sie eine eindeutige Portnummer an, die von App-V verwendet wird.</p></td>
    <td align="left"><p>Beispiel: 54321</p>
    <p>Stellen Sie sicher, dass der angegebene Port nicht von einer anderen Website verwendet wird.</p></td>
    </tr>
    </tbody>
    </table>

     

12. Geben Sie auf der Seite **Reporting Server** Folgendes an:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Zu konfigurierendes Element</th>
    <th align="left">Beschreibung und Beispiele</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Website Name </strong> : Geben Sie den benutzerdefinierten Namen an, der zum Ausführen des Berichts Diensts verwendet wird.</p></td>
    <td align="left"><p>Wenn Sie keinen benutzerdefinierten Namen haben, nehmen Sie keine Änderungen vor.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Portbindung </strong> : Geben Sie eine eindeutige Portnummer an, die von App-V verwendet wird.</p></td>
    <td align="left"><p>Beispiel: 55555</p>
    <p>Stellen Sie sicher, dass der angegebene Port nicht von einer anderen Website verwendet wird.</p></td>
    </tr>
    </tbody>
    </table>

     

13. Um die Installation zu starten, klicken Sie auf der Seite **Ready** auf **Installieren** , und klicken Sie dann auf der Seite **Fertig** auf **Schließen** .

14. Um zu überprüfen, ob das Setup erfolgreich abgeschlossen wurde, öffnen Sie einen Webbrowser, und geben Sie die folgende URL ein:

    **http:// &lt; Verwaltungsservercomputer Name &gt; : &lt; Verwaltungsdienst-Portnummer &gt; /Console.html**.

    Beispiel: **http://localhost:12345/console.html** . Wenn die Installation erfolgreich war, wird die App-V-Verwaltungskonsole ohne Fehler angezeigt.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Bereitstellen von App-V 5.1](deploying-app-v-51.md)

[So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[So installieren Sie den Veröffentlichungsserver auf einem Remotecomputer](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[So stellen Sie den App-V 5.1-Server mithilfe eines Skripts bereit](how-to-deploy-the-app-v-51-server-using-a-script.md)

 

 





