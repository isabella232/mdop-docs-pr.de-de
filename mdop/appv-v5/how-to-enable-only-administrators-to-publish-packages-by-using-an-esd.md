---
title: So schränken Sie die Veröffentlichung von Paketen mithilfe einer ESD auf Administratoren ein
description: So schränken Sie die Veröffentlichung von Paketen mithilfe einer ESD auf Administratoren ein
author: dansimp
ms.assetid: 03367b26-83d5-4299-ad52-b9177b9cf9a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 341e86ca806c5acc736c78cf8072aab6fb4286df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805480"
---
# So schränken Sie die Veröffentlichung von Paketen mithilfe einer ESD auf Administratoren ein


Ab App-v 5,0 SP3 können Sie den App-v-Client so konfigurieren, dass nur Administratoren (nicht Endbenutzer) Pakete veröffentlichen oder deren Veröffentlichung aufheben können. In früheren Versionen von App-V konnten Sie nicht verhindern, dass Endbenutzer diese Aufgaben ausführen.

**So aktivieren Sie nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen**

1.  Navigieren Sie zum folgenden Gruppenrichtlinien-Objektknoten:

    **Computer Konfiguration &gt; Richtlinien &gt; Administrative Vorlagen &gt; System &gt; App-V &gt; Publishing**.

2.  Aktivieren Sie die Gruppenrichtlinieneinstellung **Veröffentlichung als Administrator anfordern** .

    Informationen zum Verwenden von PowerShell zum Einrichten dieses Elements finden Sie unter [Verwalten von App-V 5,0-Paketen, die mit PowerShell auf einem eigenständigen Computer ausgeführt](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)werden.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





