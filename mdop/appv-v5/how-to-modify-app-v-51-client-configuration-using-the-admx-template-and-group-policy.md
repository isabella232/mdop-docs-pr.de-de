---
title: Ändern der App-V 5.1-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie
description: Ändern der App-V 5.1-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie
author: dansimp
ms.assetid: 0d9cf13a-b29c-4c87-a776-15fea34027dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 18363b4fb904d995862ac30634be1350c972d918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805267"
---
# Ändern der App-V 5.1-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie


Verwenden Sie die Microsoft Application Virtualization (app-v) 5,1 ADMX-Vorlage, um App-v 5,1-Clienteinstellungen mithilfe der ADMX-Vorlage und der Gruppenrichtlinie zu konfigurieren.

**So ändern Sie die App-V 5,1-Clientkonfiguration mithilfe von Gruppenrichtlinien**

1.  Wenn Sie die APP-v 5,1-Clientkonfiguration ändern möchten, suchen Sie die **ADMXTemplate** -Dateien, die in App-v 5,1 zur Verfügung stehen.

    **Hinweis**  Verwenden Sie den folgenden Link zum Herunterladen der App-V 5,1 **ADMX-Vorlagen**: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .

     

2.  Kopieren Sie die Datei "template **. ADMX** " auf dem Computer, auf dem Sie Gruppenrichtlinien verwalten, in der Regel dem Domänencontroller, in das folgende Verzeichnis: ** &lt; Installationslaufwerk &gt; \ \ Windows \ \ PolicyDefinitions**.

    Kopieren Sie dann auf demselben Computer die **ADML** -Datei in das folgende Verzeichnis: ** &lt; InstallationDrive &gt; \ \ Windows \ \ PolicyDefinitions \ \ en-US**.

3.  Nachdem Sie die Dateien kopiert haben, öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole, um die Richtlinien zu ändern, die ihren App-v 5,1-Clients zugeordnet sind, navigieren Sie zu den **Computer Konfigurations**  /  **Richtlinien**  /  **Administrative Vorlagen**  /  **System**  /  **App-V**.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Bereitstellen von App-V 5.1](deploying-app-v-51.md)

[Informationen über Clientkonfigurationseinstellungen](about-client-configuration-settings51.md)

 

 





