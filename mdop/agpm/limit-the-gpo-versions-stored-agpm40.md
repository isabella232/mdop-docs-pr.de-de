---
title: Beschränken der gespeicherten GPO-Versionen
description: Beschränken der gespeicherten GPO-Versionen
author: dansimp
ms.assetid: d802c7b6-f303-4b23-aefd-f19f1300b0ff
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: df6f6df2e2b1bae2cd972b67b76c27905622a723
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808379"
---
# Beschränken der gespeicherten GPO-Versionen


Standardmäßig werden alle Versionen der einzelnen gesteuerten Gruppenrichtlinienobjekte im Archiv auf dem AGPM-Server aufbewahrt. Allerdings können Sie die Anzahl der Versionen beschränken, die für jedes GPO aufbewahrt werden, und ältere Versionen löschen, wenn diese Grenze überschritten wird. Wenn GPO-Versionen gelöscht werden, verbleibt ein Datensatz der Version im Verlauf des Gruppenrichtlinienobjekts, aber die GPO-Version selbst wird aus dem Archiv gelöscht.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So begrenzen Sie die Anzahl der gespeicherten GPO-Versionen**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf die Registerkarte **AGPM-Server** .

3.  Aktivieren Sie das Kontrollkästchen **alte Versionen jedes GPO aus dem Archiv löschen** , und geben Sie die maximale Anzahl von Gruppenrichtlinienobjekten ein, die für die einzelnen Gruppenrichtlinienobjekte gespeichert werden sollen, und nicht die aktuelle Version. Wenn Sie nur die aktuelle Version beibehalten möchten, geben Sie 0 ein. Der Höchstwert darf nicht größer als 999 sein.

    **Wichtig**  Nur auf der Registerkarte " **eindeutige Versionen** " des **Verlaufs** Fensters werden nur die Gruppenrichtlinienobjekte angezeigt, die auf die Grenze begrenzt sind.

     

4.  Klicken Sie auf die Schaltfläche über **nehmen** .

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Änderungsoptionen** für die Domäne verfügen.

-   Sie können verhindern, dass eine GPO-Version gelöscht wird, indem Sie Sie im Verlauf als nicht löschbar kennzeichnen. Klicken Sie dazu mit der rechten Maustaste auf die Version im Verlauf des Gruppenrichtlinienobjekts, und klicken Sie auf **nicht löschen**.

### Weitere Verweise

-   [Verwalten des Archivs](managing-the-archive-agpm40.md)

 

 





