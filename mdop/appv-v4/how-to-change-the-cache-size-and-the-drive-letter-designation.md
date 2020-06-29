---
title: So ändern Sie die Cachegröße und Laufwerkbuchstabenangabe
description: So ändern Sie die Cachegröße und Laufwerkbuchstabenangabe
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807347"
---
# So ändern Sie die Cachegröße und Laufwerkbuchstabenangabe


Sie können die Größe des Caches und die Bezeichnung des Laufwerkbuchstabens direkt aus dem **Application Virtualization** -Knoten in der Application Virtualization Client Management Console ändern.

**Hinweis:**  
Nachdem die Cachegröße eingestellt wurde, kann Sie nicht verkleinert werden.



**So ändern Sie die Größe des Caches**

1.  Klicken Sie mit der rechten Maustaste auf den Knoten **Application Virtualization** , und wählen Sie im Popupmenü **Eigenschaften** aus.

2.  Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **Datei System** aus. Klicken Sie im Abschnitt **Client Cache-Konfigurationseinstellungen** auf eines der folgenden Optionsfelder, um auszuwählen, wie der Cachespeicher verwaltet werden soll:

    **Wichtig**  
    Wenn Sie die Einstellung Speicher **Platz für freien Speicherplatz verwenden** auswählen, wird mit dem eingegebenen Wert die Cachegröße auf die Gesamtgröße des Datenträgers abzüglich der von Ihnen eingegebenen Schwellenwert Nummer für freien Speicherplatz festgelegt. Wenn Sie dann zur Verwendung der Einstellung **Maximale Cachegröße verwenden** wiederherstellen möchten, müssen Sie eine größere Zahl als die vorhandene Cachegröße angeben. Andernfalls wird der Fehler "neue Größe muss größer sein als die vorhandene Cachegröße" angezeigt.



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. Klicken Sie auf **OK** oder auf über **nehmen** , um die Einstellung zu ändern.

**So ändern Sie die Bezeichnung des Laufwerkbuchstabens**

1.  Klicken Sie mit der rechten Maustaste auf den Knoten **Application Virtualization** , und wählen Sie im Popupmenü **Eigenschaften** aus.

2.  Wählen Sie auf der Registerkarte **Datei System** im Dialogfeld **Eigenschaften** im Feld **zu verwendender Antrieb** in der Dropdownliste der verfügbaren Laufwerkbuchstaben den gewünschten Laufwerkbuchstaben aus. Diese Einstellung wird wirksam, wenn der Computer neu gestartet wird.

3.  Klicken Sie auf **OK** oder auf über **nehmen** , um die Einstellung zu ändern.

## Verwandte Themen


[So konfigurieren Sie den Client in der Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









