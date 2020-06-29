---
title: So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste
description: So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805417"
---
# So installieren Sie die Verwaltungs- und Berichtsdatenbanken auf verschiedenen Computern über die Verwaltungs- und Berichtsdienste


Gehen Sie wie folgt vor, um den Datenbankserver und den Verwaltungsserver auf unterschiedlichen Computern zu installieren. Auf dem Computer, auf dem Sie den Datenbankserver installieren möchten, muss eine unterstützte Version von Microsoft SQL ausgeführt werden, oder die Installation schlägt fehl.

**Hinweis:**  
Nachdem Sie die Bereitstellung abgeschlossen haben, müssen der **Microsoft SQL Server-Name**, der **Instanzname** und der **Datenbankname** vom Administrator installiert werden, um eine Verbindung mit diesen Datenbanken herstellen zu können.



**So installieren Sie die Verwaltungsdatenbank und den Verwaltungsserver auf separaten Computern**

1.  Kopieren Sie die App-V 5,0 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten. Um die App-V 5,0 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus. Klicken Sie auf **Installieren**.

2.  Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.

3.  Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).** Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus. Klicken Sie auf **Weiter**.

4.  Wählen Sie auf der Seite **Featureauswahl** die Komponenten aus, die Sie installieren möchten, indem Sie das Kontrollkästchen **Verwaltungs Server-Datenbank** auswählen und auf **weiter**klicken.

5.  Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.

6.  Übernehmen Sie auf der **Seite erste neue Verwaltungs Server-Datenbank erstellen**die Standardauswahl, falls zutreffend, und klicken Sie auf **weiter**.

    Wenn Sie eine benutzerdefinierte SQL Server-Instanz verwenden, wählen Sie **benutzerdefinierte Instanz verwenden** aus, und geben Sie den Namen der Instanz ein.

    Wenn Sie einen benutzerdefinierten Datenbanknamen verwenden, wählen Sie **benutzerdefinierte Konfiguration** aus, und geben Sie den Datenbanknamen ein.

7.  Wählen Sie auf der nächsten Seite **neue Verwaltungs Server-Datenbank erstellen** die Option **Remotecomputer verwenden**aus, und geben Sie das Konto des Remotecomputers mit dem folgenden Format ein: **Domain\\MachineAccount**.

    **Hinweis:**  
    Wenn Sie den Verwaltungsserver auf demselben Computer bereitstellen möchten, müssen Sie **diesen lokalen Computer verwenden**auswählen.



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. Klicken Sie auf **Installieren**, um die Installation zu starten.

**So installieren Sie die Berichtsdatenbank und den Berichtsserver auf separaten Computern**

1.  Kopieren Sie die App-V 5,0 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten. Um die App-V 5,0 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus. Klicken Sie auf **Installieren**.

2.  Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.

3.  Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).** Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus. Klicken Sie auf **Weiter**.

4.  Wählen Sie auf der Seite **Featureauswahl** die Komponenten aus, die Sie installieren möchten, indem Sie das Kontrollkästchen **Berichts Server-Datenbank** auswählen und auf **weiter**klicken.

5.  Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.

6.  Übernehmen Sie auf der Seite erste **neue Berichts Server-Datenbank erstellen** die Standardauswahl, falls zutreffend, und klicken Sie auf **weiter**.

    Wenn Sie eine benutzerdefinierte SQL Server-Instanz verwenden, wählen Sie **benutzerdefinierte Instanz verwenden** aus, und geben Sie den Namen der Instanz ein.

    Wenn Sie einen benutzerdefinierten Datenbanknamen verwenden, wählen Sie **benutzerdefinierte Konfiguration** aus, und geben Sie den Datenbanknamen ein.

7.  Wählen Sie auf der nächsten Seite **neue Berichts Server-Datenbank erstellen** die Option **Remotecomputer verwenden**aus, und geben Sie das Konto des Remotecomputers mit dem folgenden Format ein: **Domain\\MachineAccount**.

    **Hinweis:**  
    Wenn Sie den Berichtsserver auf demselben Computer bereitstellen möchten, müssen Sie **diesen lokalen Computer verwenden**auswählen.



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. Klicken Sie auf **Installieren**, um die Installation zu starten.

**So installieren Sie die Verwaltungs-und Berichtsdatenbanken mithilfe von App-V 5,0-Datenbankskripts**

1.  Kopieren Sie die App-V 5,0 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten.

2.  Wenn Sie die App-V 5,0-Datenbankskripts extrahieren möchten, öffnen Sie eine Eingabeaufforderung, geben Sie den Speicherort der Installationsdateien an, und führen Sie den folgenden Befehl aus:

    **appv\_server\_setup.exe** **/Layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.

3.  Nachdem die Extrahierung abgeschlossen wurde, können Sie auf die App-V 5,0-Datenbankskripts und Anweisungen in der Readme-Datei zugreifen:

    -   Die Readme-Datei für die App-V 5,0-Verwaltungsdatenbank und die Anweisungen für die Anleitung finden Sie im folgenden Ordner: **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Management Database**.

    -   Die Readme-Datei für die App-V 5,0-Berichtsdatenbank und die Anweisungen für die Anleitung finden Sie im folgenden Ordner: **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Reporting Database**.

4.  Kopieren Sie für jede Datenbank die Skripts auf eine Freigabe, und ändern Sie Sie, und folgen Sie den Anweisungen in der Readme-Datei.

    **Hinweis:**  
    Weitere Informationen zum Ändern der in den Skripts enthaltenen erforderlichen SIDs finden Sie unter [Installieren der App-V-Datenbanken und Konvertieren der zugehörigen Sicherheitsbezeichner mithilfe von PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).



5.  Führen Sie die Skripts auf dem Computer aus, auf dem Microsoft SQL Server ausgeführt wird.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Bereitstellen von App-V 5.0](deploying-app-v-50.md)









