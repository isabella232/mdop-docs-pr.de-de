---
title: So erstellen Sie mithilfe der App-V 5.0-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei
description: So erstellen Sie mithilfe der App-V 5.0-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei
author: dansimp
ms.assetid: 0d1f6768-be30-4682-8eeb-aa95918b24c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d54e68caa380025b2ff6f3ea79d30f275b589b30
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805645"
---
# So erstellen Sie mithilfe der App-V 5.0-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei


Sie können eine dynamische Konfiguration verwenden, um ein App-V 5,0-Paket für einen bestimmten Benutzer anzupassen. Sie müssen jedoch zuerst die Dynamic User Configuration-Datei (XML) oder die dynamische Bereitstellungs Konfigurationsdatei erstellen, bevor Sie die Dateien verwenden können. Die Erstellung der Datei ist eine erweiterte manuelle Operation. Allgemeine Informationen zu Dynamic User-Konfigurationsdateien finden Sie unter Informationen [zur dynamischen App-V 5,0-Konfiguration](about-app-v-50-dynamic-configuration.md).

Gehen Sie wie folgt vor, um mithilfe der App-V 5,0-Verwaltungskonsole eine Dynamic User-Konfigurationsdatei zu erstellen.

**So erstellen Sie eine Dynamic User-Konfigurationsdatei**

1.  Klicken Sie mit der rechten Maustaste auf den Namen des Pakets, das Sie anzeigen möchten, und wählen Sie **Active Directory-Zugriff bearbeiten** aus, um die Konfiguration anzuzeigen, die einer bestimmten Benutzergruppe zugewiesen ist. Alternativ können Sie das Paket auswählen und auf **Bearbeiten**klicken.

2.  Wählen Sie mithilfe der Liste der **anzeigen Entitäten mit Access**die Anzeigengruppe aus, die Sie anpassen möchten. Wählen Sie in der Dropdownliste **Benutzerdefiniert** aus, wenn Sie noch nicht ausgewählt ist. Der Link " **Bearbeiten** " wird angezeigt.

3.  Klicken Sie auf **Bearbeiten**. Die der Anzeigengruppe zugewiesene dynamische Benutzerkonfiguration wird angezeigt.

4.  Klicken Sie auf **erweitert**, und klicken Sie dann auf **Konfiguration exportieren**. Geben Sie einen Dateinamen ein, und klicken Sie auf **Speichern**. Nun können Sie die Datei bearbeiten, um ein Paket für einen Benutzer zu konfigurieren.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)

 

 





