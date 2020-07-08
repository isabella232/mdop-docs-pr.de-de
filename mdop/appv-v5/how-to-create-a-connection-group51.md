---
title: So erstellen Sie eine Verbindungsgruppe
description: So erstellen Sie eine Verbindungsgruppe
author: dansimp
ms.assetid: 221e2eed-7ebb-42e3-b3d6-11c37c0578e6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f20b3e71c7c0b72d66700bbad945860112ffd03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805648"
---
# So erstellen Sie eine Verbindungsgruppe


Führen Sie die folgenden Schritte aus, um mithilfe der App-V-Verwaltungskonsole eine Verbindungsgruppe zu erstellen. Informationen zum Verwenden von PowerShell zum Erstellen von Verbindungsgruppen finden Sie unter [Verwalten von Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).

Wenn Sie Pakete in einer Verbindungsgruppe platzieren, werden deren Paketstamm Pfade zusammengeführt. Wenn Sie Pakete entfernen, behalten nur die restlichen Pakete den zusammengeführten Stamm bei.

**So erstellen Sie eine Verbindungsgruppe**

1.  Wählen Sie in der App-V 5,1-Verwaltungskonsole **Verbindungsgruppen** aus, um die Bibliothek Verbindungsgruppen anzuzeigen.

2.  Wählen Sie **Verbindungsgruppe hinzufügen** aus, um eine neue Verbindungsgruppe zu erstellen.

3.  Geben Sie im Bereich **Neue Verbindungsgruppe** eine Beschreibung für die Gruppe ein.

4.  Klicken Sie im Bereich **verbundene Pakete** auf **Bearbeiten** , um der Verbindungsgruppe eine neue Anwendung hinzuzufügen.

5.  Wählen Sie im Bereich **gesamte Bibliothek der Pakete** die Anwendung aus, die hinzugefügt werden soll, und klicken Sie auf den Pfeil, um die Anwendung hinzuzufügen.

    Um eine Anwendung zu entfernen, wählen Sie die Anwendung aus, die im Bereich **Pakete in** entfernt werden soll, und klicken Sie auf den Pfeil.

    Verwenden Sie die Pfeile im Bereich " **Pakete** ", um die Priorität für die Anwendungen in ihrer Verbindungsgruppe zu übernehmen.

    **Wichtig**  Standardmäßig werden die Access-Konfigurationen für Active Directory-Domänendienste, die einer bestimmten Anwendung zugeordnet sind, nicht zur Verbindungsgruppe hinzugefügt. Wenn Sie die Active Directory-Zugriffskonfiguration übertragen möchten, wählen Sie **Paketzugriff für Gruppen Zugriff hinzufügen**aus, der sich im Bereich **Pakete im** befindet.

     

6.  Nachdem Sie alle Anwendungen hinzugefügt und Active Directory-Zugriff konfiguriert haben, klicken Sie auf über **nehmen**.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

[Verwalten von Verbindungsgruppen](managing-connection-groups51.md)

 

 





