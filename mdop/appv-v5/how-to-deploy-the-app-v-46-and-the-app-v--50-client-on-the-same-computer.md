---
title: Bereitstellen der App-V 4.6 und des App-V 5.0-Clients auf demselben Computer
description: Bereitstellen der App-V 4.6 und des App-V 5.0-Clients auf demselben Computer
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.prod: w10
ms.openlocfilehash: f10f3d159c4724f3b486215b1169825bb029316d
ms.sourcegitcommit: 0132cd232b9c030820d95d91b71c4def0184400a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "11907228"
---
# <a name="how-to-deploy-the-app-v-46-and-the-app-v-50-client-on-the-same-computer"></a>Bereitstellen der App-V 4.6 und des App-V 5.0-Clients auf demselben Computer

**Hinweis:** App-V 4.6 hat den Mainstream-Support beendet. Im Folgenden wird davon ausgegangen, dass der App-V 4.6 SP3-Client bereits installiert ist.

Verwenden Sie die folgenden Informationen, um den App-V 5.0-Client (vorzugsweise mit den neuesten Service Packs und Hotfixes) und den App-V 4.6 SP3-Client auf demselben Computer zu installieren. Unterstützte Versionen, Anforderungen und andere Planungsinformationen finden Sie unter ["Planen der Migration von einer früheren Version von App-V".](planning-for-migrating-from-a-previous-version-of-app-v.md)

**So stellen Sie den App-V 5.0-Client und den App-V 4.6-Client auf demselben Computer bereit**

1.  Installieren Sie den App-V 5.0 SP3-Client auf dem Computer, auf dem die App-V 4.6-Version des Clients ausgeführt wird. Um optimale Ergebnisse zu erzielen, empfehlen wir, alle verfügbaren Updates auf dem App-V 5.0 SP3-Client zu installieren.

2.  Konvertieren oder sequenzieren Sie die Pakete schrittweise neu.

    -   Verwenden Sie zum Konvertieren der Pakete den App-V 5.0-Paketkonverter, und konvertieren Sie die erforderlichen Pakete in das App-V 5.0 **(APPV)-Dateiformat.**

    -   Um die Pakete neu zu sequenzieren, sollten Sie die neueste Version von Sequencer verwenden, um optimale Ergebnisse zu erzielen.

    Weitere Informationen zum Veröffentlichen von Paketen finden Sie unter ["Veröffentlichen eines Pakets mithilfe der Verwaltungskonsole".](how-to-publish-a-package-by-using-the-management-console-50.md)

3.  Stellen Sie Pakete auf den Clientcomputern bereit.

4.  Konvertieren Sie Erweiterungspunkte nach Bedarf. Weitere Informationen finden Sie in den folgenden Ressourcen:

    -   [So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.0-Paket für alle Benutzer eines bestimmten Computers](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  Testen Sie, ob Ihre App-V 5.0-Pakete erfolgreich sind, und entfernen Sie dann die 4.6-Pakete. Um den Benutzerstatus Ihrer Clientcomputer zu überprüfen, empfehlen wir die Verwendung von [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) oder eines anderen Verwaltungstools für die Benutzerumgebung.

    **Haben Sie einen Vorschlag für App-V?** Hier können Sie [Vorschläge](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)hinzufügen oder abstimmen. **Haben Sie ein App-V-Problem?** Verwenden Sie das [TechNet-Forum von App-V.](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)

## <a name="related-topics"></a>Verwandte Themen


[Planen der Migration von einer früheren Version von App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)

[Bereitstellen von App-V 5.0-Sequencer und -Client](deploying-the-app-v-50-sequencer-and-client.md)

 

 





