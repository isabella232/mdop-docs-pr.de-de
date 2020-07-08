---
title: So erstellen Sie mithilfe der App-V 5.1-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei an
description: So erstellen Sie mithilfe der App-V 5.1-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei an
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805642"
---
# So erstellen Sie mithilfe der App-V 5.1-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei an


Sie können eine dynamische Konfiguration verwenden, um ein App-V 5,1-Paket für einen bestimmten Benutzer anzupassen. Sie müssen jedoch zuerst die Dynamic User Configuration-Datei (XML) oder die dynamische Bereitstellungs Konfigurationsdatei erstellen, bevor Sie die Dateien verwenden können. Die Erstellung der Datei ist eine erweiterte manuelle Operation. Allgemeine Informationen zu Dynamic User-Konfigurationsdateien finden Sie unter Informationen [zur dynamischen App-V 5,1-Konfiguration](about-app-v-51-dynamic-configuration.md).

Gehen Sie wie folgt vor, um mithilfe der App-V 5,1-Verwaltungskonsole eine Dynamic User-Konfigurationsdatei zu erstellen.

**So erstellen Sie eine Dynamic User-Konfigurationsdatei**

1.  Klicken Sie mit der rechten Maustaste auf den Namen des Pakets, das Sie anzeigen möchten, und wählen Sie **Active Directory-Zugriff bearbeiten** aus, um die Konfiguration anzuzeigen, die einer bestimmten Benutzergruppe zugewiesen ist. Alternativ können Sie das Paket auswählen und auf **Bearbeiten**klicken.

2.  Wählen Sie mithilfe der Liste der **anzeigen Entitäten mit Access**die Anzeigengruppe aus, die Sie anpassen möchten. Wählen Sie in der Dropdownliste **Benutzerdefiniert** aus, wenn Sie noch nicht ausgewählt ist. Der Link " **Bearbeiten** " wird angezeigt.

3.  Klicken Sie auf **Bearbeiten**. Die der Anzeigengruppe zugewiesene dynamische Benutzerkonfiguration wird angezeigt.

4.  Klicken Sie auf **erweitert**, und klicken Sie dann auf **Konfiguration exportieren**. Geben Sie einen Dateinamen ein, und klicken Sie auf **Speichern**. Nun können Sie die Datei bearbeiten, um ein Paket für einen Benutzer zu konfigurieren.

    **Hinweis:**  
    Wenn Sie eine Konfiguration exportieren möchten, während Sie unter Windows Server ausgeführt wird, müssen Sie "IE Enhanced Security Configuration" deaktivieren. Wenn diese Option aktiviert ist und auf Downloads blockieren eingestellt ist, können Sie nichts vom App-V-Server herunterladen.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)









