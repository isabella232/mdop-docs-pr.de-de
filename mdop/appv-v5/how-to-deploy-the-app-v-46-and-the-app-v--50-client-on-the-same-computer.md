---
title: Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf demselben Computer
description: Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf demselben Computer
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805534"
---
# Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf demselben Computer

**Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen. Im folgenden wird davon ausgegangen, dass der App-V 4,6 SP3-Client bereits installiert ist.

Verwenden Sie die folgenden Informationen, um den App-v 5,0-Client (vorzugsweise mit den neuesten Service Packs und Hotfixes) und dem App-v 4.6 SP3-Client auf demselben Computer zu installieren. Unterstützte Versionen, Anforderungen und andere Planungsinformationen finden Sie unter [Planen der Migration von einer früheren Version von App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).

**So stellen Sie den App-v 5,0-Client und den App-v 4,6-Client auf demselben Computer bereit**

1.  Installieren Sie den App-v 5,0 SP3-Client auf dem Computer, auf dem die APP-v 4,6-Version des Clients ausgeführt wird. Um optimale Ergebnisse zu erzielen, empfehlen wir, alle verfügbaren Updates für den App-V 5,0 SP3-Client zu installieren.

2.  Konvertieren Sie die Pakete allmählich, oder führen Sie eine Neusequenzierung durch.

    -   Verwenden Sie zum Konvertieren der Pakete den App-v 5,0-Paket Konverter, und konvertieren Sie die erforderlichen Pakete in das App-v 5,0-Dateiformat (**AppV**).

    -   Um die Pakete neu zu sequenzieren, sollten Sie die neueste Version des Sequencers verwenden, um optimale Ergebnisse zu erzielen.

    Weitere Informationen zum Veröffentlichen von Paketen finden Sie unter [Veröffentlichen eines Pakets mithilfe der Verwaltungskonsole](how-to-publish-a-package-by-using-the-management-console-50.md).

3.  Bereitstellen von Paketen auf den Clientcomputern

4.  Konvertieren Sie nach Bedarf Erweiterungspunkte. Weitere Informationen finden Sie in den folgenden Ressourcen:

    -   [So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.0-Paket für alle Benutzer eines bestimmten Computers](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  Testen Sie, ob Ihre App-V 5,0-Pakete erfolgreich sind, und entfernen Sie dann die 4,6-Pakete. Wenn Sie den Benutzerstatus Ihrer Clientcomputer überprüfen möchten, empfehlen wir, dass Sie die [Virtualisierung der Benutzeroberfläche](https://technet.microsoft.com/library/dn458947.aspx) oder ein anderes Tool für die Benutzer Umgebungsverwaltung verwenden.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Planen der Migration von einer früheren Version von App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)

[Bereitstellen von App-V 5.0-Sequencer und -Client](deploying-the-app-v-50-sequencer-and-client.md)

 

 





