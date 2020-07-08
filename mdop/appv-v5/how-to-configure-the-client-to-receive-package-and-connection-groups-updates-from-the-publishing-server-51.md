---
title: So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver
description: So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver
author: dansimp
ms.assetid: 23b2d03a-20ce-4973-99ee-748f3b682207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 034cf5255d75bbaf6a5e65357bd5b3d472344f03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805693"
---
# So konfigurieren Sie den Client für den Empfang von Paket- und Verbindungsgruppenupdates vom Veröffentlichungsserver


Das Bereitstellen von Paketen und Verbindungsgruppen mit dem App-V 5,1-Veröffentlichungsserver ist hilfreich, da es eine Einzelpunkt Verwaltung und eine große Skalierbarkeit bietet.

Führen Sie die folgenden Schritte aus, um den App-V 5,1-Client so zu konfigurieren, dass Updates vom Veröffentlichungsserver empfangen werden.

**Hinweis**  Für die folgenden Verfahren wurde der Verwaltungsserver auf einem Computer mit dem Namen " **MyMgmtSrv**" installiert, und der Veröffentlichungsserver wurde auf einem Computer mit dem Namen " **MyPubSrv**" installiert.

 

**So konfigurieren Sie den App-V 5,1-Client für den Empfang von Updates vom Veröffentlichungsserver**

1.  Stellen Sie die App-V 5,1-Verwaltungs-und-Veröffentlichungsserver bereit, und fügen Sie die erforderlichen Pakete und Verbindungsgruppen hinzu. Weitere Informationen zum Hinzufügen von Paketen und Verbindungsgruppen finden Sie unter so wird es [gemacht: Hinzufügen oder Aktualisieren von Paketen mithilfe der Verwaltungskonsole](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) und [Erstellen einer Verbindungsgruppe](how-to-create-a-connection-group51.md).

2.  Um die Verwaltungskonsole zu öffnen, klicken Sie auf den folgenden Link, öffnen Sie einen Browser, und geben Sie Folgendes ein: http://MyMgmtSrv/AppvManagement/Console.html in einem Webbrowser, und importieren, veröffentlichen und berechtigen Sie alle Pakete und Verbindungsgruppen, die für eine bestimmte Gruppe von Benutzern erforderlich sind.

3.  Öffnen Sie auf dem Computer, auf dem der App-V 5,1-Client ausgeführt wird, eine erweiterte PowerShell-Eingabeaufforderung, und führen Sie den folgenden Befehl aus:

    **Add-AppvPublishingServer-Name ABC-URL http://MyPubSrv/AppvPublishing**

    Mit diesem Befehl wird der angegebene Veröffentlichungsserver konfiguriert. Es sollte eine Ausgabe ähnlich der folgenden angezeigt werden:

    ID: 1

    SetByGroupPolicy: falsch

    Name: ABC

    URL: http://MyPubSrv/AppvPublishing

    GlobalRefreshEnabled: falsch

    GlobalRefreshOnLogon: falsch

    GlobalRefreshInterval: 0

    GlobalRefreshIntervalUnit: Tag

    UserRefreshEnabled: true

    UserRefreshOnLogon: true

    UserRefreshInterval: 0

    UserRefreshIntervalUnit: Tag

    Die zurückgegebene ID – in diesem Fall 1

4.  Öffnen Sie auf dem Computer, auf dem der App-V 5,1-Client ausgeführt wird, eine PowerShell-Eingabeaufforderung, und geben Sie den folgenden Befehl ein:

    **Synchronisieren-AppvPublishingServer-Server-Nr. 1**

    Der Befehl fragt den Veröffentlichungsserver nach den Paketen und Verbindungsgruppen ab, die für diesen bestimmten Client basierend auf den Berechtigungen für die Pakete und Verbindungsgruppen, die auf dem Verwaltungsserver konfiguriert sind, hinzugefügt oder entfernt werden müssen.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

 

 





