---
title: So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank
description: So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank
author: dansimp
ms.assetid: d186bdb7-e522-4124-bc6d-7d5a41ba8266
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f20f1ce16c3f0168d1c797efd816d4125c0f1f53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805387"
---
# So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank


Gehen Sie wie folgt vor, um den Berichtsserver auf einem eigenständigen Computer zu installieren und mit der Datenbank zu verbinden.

**Wichtig**  
Bevor Sie die folgenden Schritte ausführen, sollten Sie die [App-V 5,0-Berichterstellung](about-app-v-50-reporting.md)lesen und verstehen.



**So installieren Sie den Berichtsserver auf einem eigenständigen Computer und verbinden ihn mit der Datenbank**

1.  Kopieren Sie die App-V 5,0 Server-Installationsdateien auf den Computer, auf dem Sie Sie installieren möchten. Um die App-V 5,0 Server-Installation zu starten, klicken Sie mit der rechten Maustaste, und führen Sie **appv\_server\_setup.exe** als Administrator aus. Klicken Sie auf **Installieren**.

2.  Überprüfen und akzeptieren Sie auf der Seite **Erste Schritte** die Lizenzbestimmungen, und klicken Sie auf **weiter**.

3.  Aktivieren Sie auf der Seite **Microsoft Update verwenden, um die Sicherheit Ihres Computers zu gewährleisten und auf dem neuesten Stand zu bleiben** , um Microsoft Updates zu aktivieren, die Option **Microsoft Update verwenden, wenn ich auf Updates Suche (empfohlen).** Wenn Sie Microsoft-Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus. Klicken Sie auf **Weiter**.

4.  Aktivieren Sie auf der Seite **Featureauswahl** das Kontrollkästchen **Berichts Server** , und klicken Sie auf **weiter**.

5.  Übernehmen Sie auf der Seite **Installationsspeicherort** den Standardspeicherort, und klicken Sie auf **weiter**.

6.  Wählen Sie auf der Seite **vorhandene Berichtsdatenbank konfigurieren** die Option **SQL-Remoteserver verwenden**aus, und geben Sie den Computernamen des Computers ein, auf dem Microsoft SQL Server ausgeführt wird, beispielsweise **Sie SQLSERVERMACHINE**.

    **Hinweis:**  
    Wenn Microsoft SQL Server auf demselben Server bereitgestellt wird, wählen Sie **lokalen SQL Server verwenden**aus.



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.
~~~

7. Klicken Sie auf der Seite **Konfigurieren der Berichts Server Konfiguration** .

   -   Geben Sie den Website Namen an, den Sie für den Berichterstellungsdienst verwenden möchten. Lassen Sie den Standardwert unverändert, wenn Sie keinen benutzerdefinierten Namen haben.

   -   Geben Sie für die **Portbindung**eine eindeutige Portnummer an, die von App-V 5,0, beispielsweise **55555**, verwendet wird. Sie sollten auch sicherstellen, dass der angegebene Port nicht von einer anderen Website verwendet wird.

8. Klicken Sie auf **Installieren**.

   Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Informationen zur App-V 5.0-Berichterstellung](about-app-v-50-reporting.md)

[Bereitstellen von App-V 5.0](deploying-app-v-50.md)

[So aktivieren Sie die Berichterstellung auf dem App-V 5.0-Client mithilfe von PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)









