---
title: So ändern Sie die Client-Konfiguration mithilfe von PowerShell
description: So ändern Sie die Client-Konfiguration mithilfe von PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805270"
---
# So ändern Sie die Client-Konfiguration mithilfe von PowerShell


Gehen Sie wie folgt vor, um die App-V 5,0-Clientkonfiguration zu konfigurieren.

**So ändern Sie die App-V 5,0-Clientkonfiguration mithilfe von PowerShell**

1.  Verwenden Sie das Cmdlet " **festlegen-AppvClientConfiguration** ", um die Clienteinstellungen mithilfe von PowerShell zu konfigurieren.

2.  Wenn Sie die Clientkonfiguration ändern möchten, öffnen Sie eine PowerShell-Eingabeaufforderung, und führen Sie das folgende Cmdlet **-AppvClientConfiguration** mit allen erforderlichen Parametern aus. Beispiel:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)

 

 





