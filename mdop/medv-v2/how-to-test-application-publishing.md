---
title: So testen Sie die Anwendungsveröffentlichung
description: So testen Sie die Anwendungsveröffentlichung
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812040"
---
# So testen Sie die Anwendungsveröffentlichung


Nachdem Ihr Test der erstmaligen Einrichtung abgeschlossen wurde, können Sie überprüfen, ob die Veröffentlichungsfunktionalität der Anwendung wie erwartet funktioniert, indem Sie die folgenden Aufgaben ausführen.

<a href="" id="bkmk-apppub"></a>**So testen Sie die Anwendungsveröffentlichung**

1.  Überprüfen Sie, ob die für die Veröffentlichung angegebenen Anwendungen sichtbar sind.

    Klicken Sie auf **Start** und dann auf **Alle Programme** , und suchen Sie nach den angegebenen Anwendungen.

    In einigen Fällen ist es möglich, dass dieselbe Anwendung zwei Mal installiert wird, einmal auf dem Hostcomputer und einmal auf dem Gast. Wenn eine veröffentlichte Anwendung mit demselben Namen im **Start** Menü des Hosts an demselben Speicherort veröffentlicht wird, wird Sie von der Host Anwendungsverknüpfung unterschieden, indem der Name des virtuellen Computers dem Namen der Verknüpfung hinzugefügt wird. Bei einem virtuellen Computer mit dem Namen "MEDVHost1" kann eine Hostanwendung beispielsweise "Notepad" sein, und eine veröffentlichte Anwendung kann "Notepad (MEDVHost1)" sein.

2.  Überprüfen Sie, ob die Anwendungen wie beabsichtigt funktionieren.

    Starten Sie auf dem Hostcomputer die von Ihnen veröffentlichten Anwendungen, und überprüfen Sie, ob Sie in Windows XP SP3 auf dem Gast geöffnet sind. Die Anwendung muss in einem Windows XP-Fenster auf dem Desktop des Hostcomputers angezeigt werden.

3.  Überprüfen Sie ggf., ob die Dokumentumleitung wie beabsichtigt funktioniert.

    Wenn eine veröffentlichte Anwendung auf dem Gast einen Ordner auf dem Hostsystem Laufwerk öffnen muss, stellen Sie sicher, dass Sie den angegebenen Ordner öffnen kann.

    **Wichtig**  Da Windows Virtual PC das Erstellen einer Freigabe aus einem bereits freigegebenen Ordner nicht unterstützt, erfolgt die Umleitung nicht für Dokumente, die in einem freigegebenen Ordner geöffnet werden, beispielsweise im Ordner "eigene Dateien", der sich im Netzwerk befindet. Weitere Informationen finden Sie unter [Problembehandlung bei Vorgängen](operations-troubleshooting-medv2.md).

Nachdem Sie überprüft haben, ob veröffentlichte Anwendungen installiert sind und ordnungsgemäß funktionieren, können Sie testen, ob Anwendungen dem MED-V-Arbeitsbereich hinzugefügt oder daraus entfernt werden können.

**So testen Sie, ob eine Anwendung hinzugefügt oder entfernt werden kann**

1.  Hinzufügen oder Entfernen einer Anwendung aus dem MED-V-Arbeitsbereich

    Informationen zum Hinzufügen und Entfernen von Anwendungen aus einem Med-v-Arbeitsbereich finden Sie unter [Verwalten von Anwendungen, die in Med-v-Arbeitsbereichen bereitgestellt](managing-applications-deployed-to-med-v-workspaces.md)werden.

2.  Wenn Sie eine Anwendung hinzugefügt haben, wiederholen Sie die Schritte unter [So testen Sie die Anwendungsveröffentlichung](#bkmk-apppub) , um zu überprüfen, ob die neue Anwendung wie beabsichtigt funktioniert.

3.  Wenn Sie eine Anwendung entfernt haben, klicken Sie auf **Start** und dann auf **Alle Programme** , und stellen Sie sicher, dass alle von Ihnen entfernten Anwendungen nicht mehr aufgelistet sind.

**Hinweis**  Wenn bei der Überprüfung ihrer Publikationseinstellungen für die Anwendung Probleme auftreten, finden Sie Informationen unter [Behandeln von Vorgängen](operations-troubleshooting-medv2.md).

Nachdem Sie das Testen der Anwendungsveröffentlichung abgeschlossen haben, können Sie andere MED-V-Arbeitsbereichskonfigurationen testen, um zu überprüfen, ob Sie wie beabsichtigt funktionieren.

Nachdem Sie das Testen des Med-v-Arbeitsbereichs Pakets abgeschlossen haben und überprüft haben, dass es wie beabsichtigt funktioniert, können Sie den Med-v-Arbeitsbereich für Ihr Unternehmen bereitstellen.

## Verwandte Themen

[So testen Sie die URL-Umleitung](how-to-test-url-redirection.md)

[So überprüfen Sie erstmalige Einstellungen für das Setup](how-to-verify-first-time-setup-settings.md)

[Bereitstellen des MED-V-Arbeitsbereichspakets](deploying-the-med-v-workspace-package.md)

 

 





