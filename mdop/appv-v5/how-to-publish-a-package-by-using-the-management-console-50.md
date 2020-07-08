---
title: So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket
description: So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805237"
---
# So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket


Gehen Sie wie folgt vor, um ein App-V 5,0-Paket zu veröffentlichen. Nachdem Sie ein Paket veröffentlicht haben, können Computer, auf denen der App-V 5,0-Client ausgeführt wird, auf die Anwendungen in diesem Paket zugreifen und diese ausführen.

**Hinweis**  Die Möglichkeit, nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen (siehe unten) zu aktivieren, wird ab App-V 5,0 SP3 unterstützt.

 

**So veröffentlichen Sie ein App-V 5,0-Paket**

1.  In der App-V 5,0-Verwaltungskonsole. Klicken Sie mit der rechten Maustaste auf den Namen des zu veröffentlichenden Pakets, und wählen Sie **veröffentlichen**aus.

2.  Überprüfen Sie die Spalte **Status** , um zu überprüfen, ob das Paket veröffentlicht wurde und nun verfügbar ist. Wenn das Paket verfügbar ist, wird der **veröffentlichte** Status angezeigt.

    Wenn das Paket nicht erfolgreich veröffentlicht wird, wird der Status **unveröffentlicht** zusammen mit dem Fehlertext angezeigt, in dem erläutert wird, warum das Paket nicht verfügbar ist.

**So aktivieren Sie nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen**

1.  Navigieren Sie zum folgenden Gruppenrichtlinien-Objektknoten:

    **Computer Konfiguration &gt; Richtlinien &gt; Administrative Vorlagen &gt; System &gt; App-V &gt; Publishing**.

2.  Aktivieren Sie die Gruppenrichtlinieneinstellung **Veröffentlichung als Administrator anfordern** .

    Informationen zum Verwenden von PowerShell zum Einrichten dieses Elements finden Sie unter [Verwalten von App-V 5,0-Paketen, die mit PowerShell auf einem eigenständigen Computer ausgeführt](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)werden.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)

[So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





