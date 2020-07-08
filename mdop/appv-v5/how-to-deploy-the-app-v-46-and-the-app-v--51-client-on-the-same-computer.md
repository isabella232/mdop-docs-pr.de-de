---
title: Bereitstellen der APP-v 4,6 und des App-v 5,1-Clients auf demselben Computer
description: Bereitstellen der APP-v 4,6 und des App-v 5,1-Clients auf demselben Computer
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805528"
---
# Bereitstellen der APP-v 4,6 und des App-v 5,1-Clients auf demselben Computer

**Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen.

Verwenden Sie die folgenden Informationen, um den Microsoft Application Virtualization (app-v) 5,1-Client (vorzugsweise mit den neuesten Service Packs und Hotfixes) und dem App-v 4.6 SP2-Client oder dem App-v 4.6 s3-Client auf demselben Computer zu installieren. Unterstützte Versionen, Anforderungen und andere Planungsinformationen finden Sie unter [Planen der Migration von einer früheren Version von App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).

**So stellen Sie den App-v 5,1-Client und den App-v 4,6-Client auf demselben Computer bereit**

1.  Installieren Sie die folgende Version des App-v-Clients auf dem Computer, auf dem App-v 4,6 ausgeführt wird.

    -   [Microsoft Application Virtualization 4,6 Service Pack 3](https://www.microsoft.com/download/details.aspx?id=41187)

2.  Installieren Sie den App-v 5,1-Client auf dem Computer, auf dem die APP-v 4,6 SP3-Version des Clients ausgeführt wird. Um optimale Ergebnisse zu erzielen, empfehlen wir, alle verfügbaren Updates für den App-V 5,1-Client zu installieren.

3.  Konvertieren Sie die Pakete allmählich, oder führen Sie eine Neusequenzierung durch.

    -   Verwenden Sie zum Konvertieren der Pakete den App-v 5,1-Paket Konverter, und konvertieren Sie die erforderlichen Pakete in das App-v 5,1-Dateiformat (**AppV**).

    -   Um die Pakete neu zu sequenzieren, sollten Sie die neueste Version des Sequencers verwenden, um optimale Ergebnisse zu erzielen.

    Weitere Informationen zum Veröffentlichen von Paketen finden Sie unter [Veröffentlichen eines Pakets mithilfe der Verwaltungskonsole](how-to-publish-a-package-by-using-the-management-console-51.md).

4.  Bereitstellen von Paketen auf den Clientcomputern

5.  Konvertieren Sie nach Bedarf Erweiterungspunkte. Weitere Informationen finden Sie in den folgenden Ressourcen:

    -   [So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.1-Paket für alle Benutzer eines bestimmten Computers](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.1 für einen bestimmten Benutzer](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  Testen Sie, ob Ihre App-V 5,1-Pakete erfolgreich sind, und entfernen Sie dann die 4,6-Pakete. Wenn Sie den Benutzerstatus Ihrer Clientcomputer überprüfen möchten, empfehlen wir, dass Sie die [Virtualisierung der Benutzeroberfläche](https://technet.microsoft.com/library/dn458947.aspx) oder ein anderes Tool für die Benutzer Umgebungsverwaltung verwenden.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Planen der Migration von einer früheren Version von App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[Bereitstellen von App-V 5.1-Sequencer und -Client](deploying-the-app-v-51-sequencer-and-client.md)

 

 





