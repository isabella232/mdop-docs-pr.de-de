---
title: So ändern Sie die Protokollberichtsebenen und setzen die Protokolldateien zurück
description: So ändern Sie die Protokollberichtsebenen und setzen die Protokolldateien zurück
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807351"
---
# So ändern Sie die Protokollberichtsebenen und setzen die Protokolldateien zurück


Mit dem folgenden Verfahren können Sie die Protokoll Berichterstattungs Ebene über den Knoten **Application Virtualization** in der Application Virtualization-Verwaltungskonsole ändern. Wenn die Protokolldatei die maximale Größe erreicht (Standard ist 256 MB), wird ein Reset erzwungen, wenn der nächste Schreibvorgang in das Protokoll erfolgt. Bei einem Reset wird eine neue Protokolldatei erstellt, und die alte Datei wird als Sicherung umbenannt.

**So ändern Sie die Protokoll Berichterstattungs Ebene**

1.  Klicken Sie mit der rechten Maustaste auf den Knoten **Application Virtualization** , und wählen Sie im Popupmenü **Eigenschaften** aus.

2.  Wählen Sie auf der Registerkarte **Allgemein** im Dialogfeld **Eigenschaften** in der Dropdownliste **Protokollebene** die gewünschte Protokollebene aus.

    **Hinweis**  Wenn Sie " **verbose** " als Protokollierungsstufe auswählen, werden die Protokolldateien sehr schnell vergrößert. Dies kann die Clientleistung hemmen, daher empfiehlt es sich, diese Protokollebene nur zum Diagnostizieren spezifischer Probleme zu verwenden.

     

3.  Wählen Sie auf der Registerkarte **Allgemein** im Dialogfeld **Eigenschaften** in der Dropdownliste **System Protokollebene** die gewünschte Protokollebene aus.

    **Hinweis**  Die Einstellung **Systemprotokollebene** steuert die Ebene der Nachrichten, die an das Systemereignisprotokoll gesendet werden. Die protokollierten Nachrichten sind identisch mit den Nachrichten, die im Clientereignisprotokoll protokolliert werden, aber an einem anderen Speicherort gespeichert sind.

     

4.  Klicken Sie auf **OK** oder auf über **nehmen** , um die Einstellung zu ändern.

**So setzen Sie die Protokolldatei zurück**

1.  Klicken Sie mit der rechten Maustaste auf den Knoten **Application Virtualization** , und wählen Sie im Popupmenü **Eigenschaften** aus.

2.  Klicken Sie im Dialogfeld **Eigenschaften** auf der Registerkarte **Allgemein** auf **Protokoll zurücksetzen** , um die aktuelle Protokolldatei zu sichern und sofort eine neue Protokolldatei zu starten. Die Sicherungsprotokolldateien werden im gleichen Ordner gespeichert.

3.  Klicken Sie auf **OK** oder auf über **nehmen** , um die Einstellung zu ändern.

## Verwandte Themen


[So konfigurieren Sie den Client in der Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[Benutzerzugriffsberechtigungen in Application Virtualization Client](user-access-permissions-in-application-virtualization-client.md)

 

 





