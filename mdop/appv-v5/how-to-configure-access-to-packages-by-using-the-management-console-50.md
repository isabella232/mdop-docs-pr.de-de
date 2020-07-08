---
title: So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete
description: So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete
author: dansimp
ms.assetid: 8f4c91e4-f4e6-48cf-aa94-6085a054e8f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e1f5b51b118dc7b783a4a550e19fd39a61a0ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805714"
---
# So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete


Bevor Sie ein virtualisiertes App-V 5,0-Paket bereitstellen, müssen Sie die Active Directory-Domänendienste (AD DS)-Sicherheitsgruppen konfigurieren, die für den Zugriff auf und die Ausführung der Anwendungen zugelassen sind. Die Sicherheitsgruppen enthalten möglicherweise Computer oder Benutzer. Wenn Sie ein Paket zu einer Computergruppe berechtigen, wird das Paket Global auf allen Computern in der Gruppe veröffentlicht.

Gehen Sie wie folgt vor, um den Zugriff auf virtualisierte Pakete zu konfigurieren.

**So gewähren Sie Zugriff auf ein App-V 5,0-Paket**

1.  Suchen Sie das Paket, das Sie konfigurieren möchten:

    1.  Öffnen Sie die App-V 5,0-Verwaltungskonsole.

    2.  Klicken Sie zum Anzeigen der Seite **anzeigen Zugriff** mit der rechten Maustaste auf das zu konfigurierbare Paket, und wählen Sie **Active Directory-Zugriff bearbeiten**aus. Alternativ können Sie das Paket auswählen und im Bereich **anzeigen Zugriff** auf **Bearbeiten** klicken.

2.  Bereitstelleneiner Sicherheitsgruppe für das Paket:

    1.  Wechseln Sie zur Seite **gültige Active Directory-Namen und Grant-Zugriff suchen** .

    2.  **mydomain**  \\  **groupname**Geben Sie den Namen oder einen Teil des Namens eines Active Directory-Gruppenobjekts ein, und klicken Sie auf **überprüfen**.

        **Hinweis**  Stellen Sie sicher, dass Sie einen zugehörigen Domänennamen für die Gruppe angeben, nach der Sie suchen.

         

3.  Wenn Sie dem Paketzugriff gewähren möchten, wählen Sie die gewünschte Gruppe aus, und klicken Sie auf **Zugriff gewähren**. Die neu hinzugefügte Gruppe wird im Bereich " **anzeigen Entitäten mit Access** " angezeigt.

4.  

    Wenn Sie die Standardkonfigurationseinstellungen übernehmen und die Seite **anzeigen Zugriff** schließen möchten, klicken Sie auf **Schließen**.

    Wenn Sie Konfigurationen für eine bestimmte Gruppe anpassen möchten, klicken Sie auf die Dropdownliste **zugewiesene Konfigurationen** , und wählen Sie **Benutzerdefiniert**aus. Klicken Sie zum Konfigurieren der benutzerdefinierten Konfigurationen auf **Bearbeiten**. Nachdem Sie Access gewährt haben, klicken Sie auf **Schließen**.

**So entfernen Sie den Zugriff auf ein App-V 5,0-Paket**

1.  Suchen Sie das Paket, das Sie konfigurieren möchten:

    1.  Öffnen Sie die App-V 5,0-Verwaltungskonsole.

    2.  Klicken Sie zum Anzeigen der Seite **anzeigen Zugriff** mit der rechten Maustaste auf das zu konfigurierbare Paket, und wählen Sie **Active Directory-Zugriff bearbeiten**aus. Alternativ können Sie das Paket auswählen und im Bereich **anzeigen Zugriff** auf **Bearbeiten** klicken.

2.  Wählen Sie die Gruppe aus, die Sie entfernen möchten, und klicken Sie auf **Löschen**.

3.  Klicken Sie auf **Schließen**, um die Seite **anzeigen Zugriff** zu schließen.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)

 

 





