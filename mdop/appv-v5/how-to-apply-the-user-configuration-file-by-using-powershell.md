---
title: So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an
description: So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an
author: dansimp
ms.assetid: f7d7c595-4fdd-4096-b53d-9eead111c339
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95ae5840f5eee04a29431716a956ddec7d0487aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805726"
---
# So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an


Die Dynamic User-Konfigurationsdatei wird angewendet, wenn ein Paket für einen bestimmten Benutzer veröffentlicht wird, und bestimmt, wie das Paket ausgeführt werden soll.

Gehen Sie wie folgt vor, um eine benutzerspezifische Konfigurationsdatei anzugeben. Das folgende Verfahren basiert auf dem Beispiel:

**c:\\Packages\\Contoso\\MyApp.appv**

**So wenden Sie eine Benutzerkonfigurationsdatei an**

1.  Geben Sie den folgenden Befehl ein, um das Paket auf dem Computer mithilfe der PowerShell-Konsole hinzuzufügen:

    **Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.AppV**.

2.  Verwenden Sie den folgenden Befehl, um das Paket für den Benutzer zu veröffentlichen und die aktualisierte Dynamic User-Konfigurationsdatei anzugeben:

    **Publish-AppVClientPackage $pkg – DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml**

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)

 

 





