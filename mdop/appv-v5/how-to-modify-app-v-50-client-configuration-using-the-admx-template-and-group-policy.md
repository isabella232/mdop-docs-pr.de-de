---
title: So ändern Sie die App-V 5.0-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie
description: So ändern Sie die App-V 5.0-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie
author: dansimp
ms.assetid: 79d03a2b-2586-4ca7-bbaa-bdeb0a694279
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cd257691bf223baa5e2919d83fdbf53d34f271ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805279"
---
# So ändern Sie die App-V 5.0-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie


Verwenden Sie die APP-v 5,0 ADMX-Vorlage, um App-v 5,0-Clienteinstellungen mithilfe der ADMX-Vorlage und der Gruppenrichtlinie zu konfigurieren.

**So ändern Sie die App-V 5,0-Clientkonfiguration mithilfe von Gruppenrichtlinien**

1.  Wenn Sie die APP-v 5,0-Clientkonfiguration ändern möchten, suchen Sie die **ADMXTemplate** -Dateien, die in App-v 5,0 zur Verfügung stehen.

    **Hinweis**  Verwenden Sie den folgenden Link zum Herunterladen der App-V 5,0 **ADMX-Vorlagen**: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .

     

2.  Kopieren Sie die Datei "template **. ADMX** " auf dem Computer, auf dem Sie Gruppenrichtlinien verwalten, in der Regel dem Domänencontroller, in das folgende Verzeichnis: ** &lt; Installationslaufwerk &gt; \ \ Windows \ \ PolicyDefinitions**.

    Kopieren Sie dann auf demselben Computer die **ADML** -Datei in das folgende Verzeichnis: ** &lt; InstallationDrive &gt; \ \ Windows \ \ PolicyDefinitions \ \ en-US**.

3.  Nachdem Sie die Dateien kopiert haben, öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole, um die Richtlinien zu ändern, die ihren App-v 5,0-Clients zugeordnet sind, navigieren Sie zu den **Computer Konfigurations**  /  **Richtlinien**  /  **Administrative Vorlagen**  /  **System**  /  **App-V**.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Bereitstellen von App-V 5.0](deploying-app-v-50.md)

[Informationen über Clientkonfigurationseinstellungen](about-client-configuration-settings.md)

 

 





