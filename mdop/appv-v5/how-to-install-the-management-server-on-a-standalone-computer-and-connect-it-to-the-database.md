---
title: So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank
description: So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank
author: dansimp
ms.assetid: 95281287-cb56-4117-befd-854268ea147c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86f384e88b85101855287bb428e75376f7974219
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805420"
---
# So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank


Gehen Sie wie folgt vor, um den Verwaltungsserver auf einem eigenständigen Computer zu installieren und mit der Datenbank zu verbinden.

**So installieren Sie den Verwaltungsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank**

1.  Kopieren Sie die App-V 5,0 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten. Um die App-V 5,0 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus. Klicken Sie auf **Installieren**.

2.  Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.

3.  Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).** Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus. Klicken Sie auf **Weiter**.

4.  Aktivieren Sie auf der Seite **Featureauswahl** das Kontrollkästchen **Verwaltungs Server** , und klicken Sie auf **weiter**.

5.  Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.

6.  Wählen Sie auf der Seite **vorhandene Verwaltungsdatenbank konfigurieren** die Option **SQL-Remote Server verwenden**aus, und geben Sie den Computernamen des Computers ein, auf dem Microsoft SQL SQL ausgeführt wird, beispielsweise **Sie SQLSERVERMACHINE**.

    **Hinweis:**  
    Wenn Microsoft SQL Server auf demselben Server bereitgestellt wird, wählen Sie **lokalen SQL Server verwenden**aus.



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. Geben Sie auf der Seite **Konfigurieren der Verwaltungs Server Konfiguration** die Anzeigengruppe oder das Konto an, das für administrative Zwecke eine Verbindung mit der Verwaltungskonsole herstellen soll, beispielsweise **MyDomain\\MyUser** oder **MyDomain\\AdminGroup**. Das von Ihnen angegebene Konto oder die Anzeigengruppe wird aktiviert, um den Server über die Verwaltungskonsole zu verwalten. Sie können weitere Benutzer oder Gruppen mithilfe der Verwaltungskonsole nach der Installation hinzufügen.

   Geben Sie den **Website Namen** an, den Sie für den Verwaltungsdienst verwenden möchten. Übernehmen Sie die Standardeinstellung, wenn Sie keinen benutzerdefinierten Namen haben. Geben Sie für die **Portbindung**eine eindeutige Portnummer an, die verwendet werden soll, beispielsweise **12345**.

8. Klicken Sie auf **Installieren**.

9. Um zu bestätigen, dass das Setup erfolgreich abgeschlossen wurde, öffnen Sie einen Webbrowser, und geben Sie die folgende URL ein: http://managementserver:portnumber/Console.html Wenn die Installation erfolgreich war, sollte die **Silverlight-Verwaltungskonsole** angezeigt werden, ohne dass Fehlermeldungen oder Warnungen angezeigt werden.

   Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Bereitstellen von App-V 5.0](deploying-app-v-50.md)









