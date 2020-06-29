---
title: Registerkarte „AGPM-Server“
description: Registerkarte „AGPM-Server“
author: dansimp
ms.assetid: a6689437-233e-4f33-a0d6-f7d432c96c00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7ffaa3f55d4ae1c2a59287d9dc302aec3dd00aed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807844"
---
# Registerkarte „AGPM-Server“


Auf der Registerkarte **AGPM Server** im Bereich **Änderungssteuerung** können Sie einen AGPM-Server auswählen, indem Sie einen vollqualifizierten Computernamen und-Port eingeben und ältere Versionen von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) aus dem Archiv löschen, um Speicherplatz auf dem AGPM-Server zu sparen.

## Angeben des AGPM-Servers


Der ausgewählte AGPM-Server bestimmt, welches Archiv auf der Registerkarte **Inhalt** angezeigt wird und an welchen Speicherort die Einstellungen für die **Domänendelegierung** angewendet werden. Der Standardport für Advanced Group Policy Management (AGPM) ist Port 4600.

Wenn die AGPM-Server Verbindung zentral mithilfe von Einstellungen für administrative Vorlagen konfiguriert ist, sind die Optionen auf dieser Registerkarte zum Konfigurieren der Verbindung nicht verfügbar. Weitere Informationen finden Sie unter [Konfigurieren von AGPM-Server Verbindungen](configure-agpm-server-connections-agpm40.md).

## Löschen alter GPO-Versionen


Standardmäßig werden alle Versionen jedes kontrollierten Gruppenrichtlinienobjekts im Archiv aufbewahrt. Sie können den AGPM-Dienst jedoch so konfigurieren, dass die Anzahl der für die einzelnen Gruppenrichtlinienobjekte aufbewahrten Versionen eingeschränkt wird, und die älteste Version wird automatisch gelöscht, wenn diese Grenze überschritten wird. Nur auf der Registerkarte " **eindeutige Versionen** " des **Verlaufs** Fensters werden nur die Gruppenrichtlinienobjekte angezeigt, die auf die Grenze begrenzt sind.

**Hinweis**  Die maximale Anzahl von eindeutigen Versionen, die für jedes GPO gespeichert werden, enthält nicht die aktuelle Version, sodass die Eingabe von 0 nur die aktuelle Version aufrecht erhält. Der Grenzwert darf nicht größer als 999-Versionen sein.

Wenn eine GPO-Version gelöscht wird, verbleibt ein Datensatz dieser Version im Verlauf des Gruppenrichtlinienobjekts, aber die GPO-Version selbst wird aus dem Archiv gelöscht. Sie können verhindern, dass eine GPO-Version gelöscht wird, indem Sie Sie im Protokoll als nicht löschbar kennzeichnen.

 

### Weitere Verweise

-   [Benutzeroberfläche: Advanced Group Policy Management](user-interface-advanced-group-policy-management-agpm40.md)

-   [Durchführen von AGPM-Administratoraufgaben](performing-agpm-administrator-tasks-agpm40.md)

-   [Durchführen von Prüferaufgaben](performing-reviewer-tasks-agpm40.md)

 

 





