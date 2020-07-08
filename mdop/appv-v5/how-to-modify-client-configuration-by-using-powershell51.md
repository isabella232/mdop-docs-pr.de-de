---
title: So ändern Sie die Client-Konfiguration mithilfe von PowerShell
description: So ändern Sie die Client-Konfiguration mithilfe von PowerShell
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805258"
---
# So ändern Sie die Client-Konfiguration mithilfe von PowerShell


Gehen Sie wie folgt vor, um die App-V 5,1-Clientkonfiguration zu konfigurieren.

**So ändern Sie die App-V 5,1-Clientkonfiguration mithilfe von PowerShell**

1.  Verwenden Sie das Cmdlet " **festlegen-AppvClientConfiguration** ", um die Clienteinstellungen mithilfe von PowerShell zu konfigurieren. Weitere Informationen zum Installieren von PowerShell und einer Liste mit Cmdlets finden Sie unter [Laden der PowerShell-Cmdlets und Abrufen der Cmdlet-Hilfe](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).

2.  Wenn Sie die Clientkonfiguration ändern möchten, öffnen Sie eine PowerShell-Eingabeaufforderung, und führen Sie das folgende Cmdlet **-AppvClientConfiguration** mit allen erforderlichen Parametern aus. Beispiel:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

 

 





