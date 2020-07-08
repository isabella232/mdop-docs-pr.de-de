---
title: So überprüfen Sie erstmalige Einstellungen für das Setup
description: So überprüfen Sie erstmalige Einstellungen für das Setup
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804667"
---
# So überprüfen Sie erstmalige Einstellungen für das Setup


Während der Test der erstmaligen Einrichtung ausgeführt wird oder nachdem er abgeschlossen wurde, können Sie die Einstellungen überprüfen, die Sie in Ihrem MED-V-Arbeitsbereich konfiguriert haben, indem Sie die folgenden Aufgaben ausführen.

**Hinweis**  Informationen dazu, wie Sie den erfolgreichen Abschluss der erstmaligen Einrichtung in Ihrem Unternehmen nach der Bereitstellung überwachen können, finden Sie unter über [Wachen von MED-V-Arbeitsbereichs Bereitstellungen](monitoring-med-v-workspace-deployments.md).

 

**So überprüfen Sie die Einstellungen während der erstmaligen Einrichtung**

1.  Überprüfen Sie Folgendes, während die erstmalige Einrichtung ausgeführt wird:

    Wenn Sie den **unbeaufsichtigten** Modus angegeben haben, stellen Sie sicher, dass der virtuelle Computer nicht angezeigt wird, wenn die erstmalige Einrichtung ausgeführt wird.

    Wenn Sie den beaufsichtigten Modus angegeben haben, überprüfen Sie, ob der virtuelle Computer angezeigt wird und alle Felder angezeigt werden, für die Benutzereingaben erforderlich sind.

2.  Sie können auch den vollständigen erstmaligen Setupprozess überwachen, indem Sie den virtuellen Computer anzeigen, wenn die erstmalige Einrichtung ausgeführt wird. Gehen Sie hierzu folgendermaßen vor:

    1.  Öffnen Sie die Windows Virtual PC-Konsole.

        Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Windows Virtual PC**, und klicken Sie dann auf **Windows Virtual PC**.

    2.  Starten Sie MED-V, wenn es noch nicht ausgeführt wird.

        Wenn Sie nicht bereits vorhanden sind, wird in kurzer Zeit ein virtueller Computer mit dem Namen des bereitgestellten MED-V-Arbeitsbereichs in der Liste der virtuellen Computer angezeigt.

    3.  Doppelklicken Sie auf den MED-V-virtuellen Computer, um ihn zu öffnen.

        Sie können den virtuellen MED-V-Computer beobachten, wenn er eingerichtet wird, und Sie können eine Problembehandlung für die Mini Einrichtung ausführen. Überprüfen Sie die Informationen in den verschiedenen Bildschirmen während ihrer Vorgehensweise, wie etwa die Konfiguration von Netzwerkeinstellungen, Informationen zu Computer Domänenbeitritt, Konfigurieren des Gast-Agents, Einrichten persönlicher Einstellungen und Herunterfahren.

    4.  Der virtuelle Computer wird automatisch geschlossen, wenn die erstmalige Einrichtung abgeschlossen ist.

        **Hinweis**  Sie können das Fenster des virtuellen Computers jederzeit schließen, und das erstmalige Setup wird fortgesetzt.

         

**So überprüfen Sie die Einstellungen nach Abschluss der erstmaligen Einrichtung**

1.  Stellen Sie sicher, dass die erstmalige Einrichtung erfolgreich abgeschlossen wurde.

2.  Überprüfen Sie, ob der MED-V-Arbeitsbereich ordnungsgemäß eingerichtet ist.

    1.  Öffnen Sie die Windows Virtual PC-Konsole.

        Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Windows Virtual PC**, und klicken Sie dann auf **Windows Virtual PC**.

    2.  Doppelklicken Sie auf Ihren installierten MED-V-Arbeitsbereich.

        Wenn der MED-V-Arbeitsbereich bereits eine virtuelle Anwendung ausführt, werden Sie möglicherweise aufgefordert, die Anwendung zu schließen, bevor Sie den virtuellen Computer öffnen können.

    3.  Klicken Sie im MED-V-Arbeitsbereich mit der rechten Maustaste auf Arbeits **Platz**, und klicken Sie dann auf **Eigenschaften**.

    4.  Überprüfen Sie, ob der MED-V-Arbeitsbereich der richtigen Domäne beigetreten ist. Wenn Sie auf Ihre Organisation zutreffen, testen Sie die Domänenmitgliedschaft, indem Sie zwei verschiedene Domänen angeben, um zu überprüfen, ob die Gast Domäne von der Hostdomäne überschrieben wird.

    5.  Überprüfen Sie, ob der MED-V-Arbeitsbereich der von Ihnen angegebenen Domänen Organisationseinheit beigetreten ist.

    6.  Wenn Sie die Computernamen Maske angegeben haben, überprüfen Sie, ob der Name des neuen Computers mit dem angegebenen übereinstimmt.

3.  Überprüfen Sie, ob die von Ihnen angegebenen Gebietsschemaeinstellungen richtig sind.

    1.  Klicken Sie im MED-V-Arbeitsbereich auf **Start** und dann auf **System**Steuerung.

    2.  Überprüfen Sie die angegebenen Konfigurationseinstellungen, beispielsweise **Datum und Uhrzeit** sowie **Region und Sprache**.

**Hinweis**  Wenn bei der Überprüfung der Einstellungen für die erstmalige Einrichtung Probleme auftreten, lesen Sie [Problembehandlung bei Vorgängen](operations-troubleshooting-medv2.md).

 

Nachdem Sie überprüft haben, dass die Einstellungen für die erstmalige Einrichtung korrekt sind, können Sie andere MED-V-Arbeitsbereichskonfigurationen testen, um zu überprüfen, ob Sie wie beabsichtigt funktionieren, beispielsweise die Veröffentlichung von Anwendungen und die URL-Umleitung.

Nachdem Sie alle Tests Ihres Med-v-Arbeitsbereichs Pakets abgeschlossen haben und überprüft haben, dass es wie beabsichtigt funktioniert, können Sie den Med-v-Arbeitsbereich für Ihr Unternehmen bereitstellen.

## Verwandte Themen


[So testen Sie die Anwendungsveröffentlichung](how-to-test-application-publishing.md)

[So testen Sie die URL-Umleitung](how-to-test-url-redirection.md)

[Bereitstellen des MED-V-Arbeitsbereichspakets](deploying-the-med-v-workspace-package.md)

[Verwalten von MED-V-Arbeitsbereichseinstellungen](manage-med-v-workspace-settings.md)

 

 





