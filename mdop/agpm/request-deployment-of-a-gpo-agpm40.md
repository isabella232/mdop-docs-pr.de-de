---
title: Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts
description: Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 5783cfd0-bd93-46b4-8fa0-684bd39aa8fc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e9cc0fc12962dbdd7758c429a20fdd7c55b3cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808284"
---
# Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts


Nachdem Sie ein Gruppenrichtlinienobjekt (GPO) geändert und eingecheckt haben, stellen Sie das Gruppenrichtlinienobjekt bereit, damit es in der Produktionsumgebung wirksam wird.

Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle "Editor" oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So fordern Sie die Bereitstellungeines GPO in der Produktionsumgebung der Domäne an**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das zu implementierende GPO, und klicken Sie dann auf **Bereitstellen**.

4.  Sofern Sie kein genehmigender oder AGPM-Administrator sind oder über eine besondere Berechtigung zum Bereitstellen von GPOs verfügen, müssen Sie eine Anforderung für die Bereitstellung einreichen. Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein. Geben Sie einen Kommentar ein, der im **Protokoll** für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **Absenden**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt. Wenn eine genehmigende Person Ihre Anforderung genehmigt hat, wird das Gruppenrichtlinienobjekt von der Registerkarte **Ausstehend** auf die Registerkarte **gesteuert** verschoben und bereitgestellt.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bearbeiten von Einstellungen** für das Gruppenrichtlinienobjekt verfügen.

-   Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das GPO, und klicken Sie dann auf **zurück** Das Gruppenrichtlinienobjekt wird auf die Registerkarte **gesteuert** zurückgegeben.

### Weitere Verweise

-   [Durchführen von Editor-Aufgaben](performing-editor-tasks-agpm40.md)

 

 





