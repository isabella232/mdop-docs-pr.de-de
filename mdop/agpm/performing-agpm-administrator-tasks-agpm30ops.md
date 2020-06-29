---
title: Durchführen von AGPM-Administratoraufgaben
description: Durchführen von AGPM-Administratoraufgaben
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809346"
---
# Durchführen von AGPM-Administratoraufgaben


In Advanced Group Policy Management (AGPM) konfiguriert ein AGPM-Administrator (Vollzugriff) domänenweite Optionen und delegiert Berechtigungen für genehmigende Personen, Bearbeiter, Prüfer und andere AGPM-Administratoren. Standardmäßig handelt es sich bei einem AGPM-Administrator um eine Person mit Vollzugriff (alle AGPM-Berechtigungen), die daher Aufgaben ausführen kann, die mit einer Rolle verknüpft sind.

In einer Umgebung, in der mehrere Personengruppen Richtlinienobjekte (Group Policy Objects, GPOs) entwickeln, können Sie auswählen, ob alle AGPM-Benutzer die gleichen Aufgaben ausführen und über die gleiche Zugriffsebene verfügen oder ob AGPM-Administratoren Berechtigungen für Editoren delegieren, die Änderungen an GPOs vornehmen, und Genehmigern, die GPOs in der Produktionsumgebung bereitstellen. AGPM-Administratoren können Berechtigungen so konfigurieren, dass Sie den Anforderungen Ihrer Organisation entsprechen.

-   [Konfigurieren der erweiterten Gruppenrichtlinienverwaltung](configuring-advanced-group-policy-management.md): Konfigurieren der AGPM-Server Verbindung und e-Mail-Benachrichtigung, Delegieren des Zugriffs auf GPOs in der Produktionsumgebung und Konfigurieren der Protokollierung und Ablaufverfolgung für die Problembehandlung.

-   [Verwalten des Archivs](managing-the-archive.md): Delegieren des Zugriffs auf GPOs im Archiv und begrenzen der Anzahl der Versionen jedes gespeicherten Gruppenrichtlinienobjekts.

-   [Verwalten des AGPM-Diensts](managing-the-agpm-service-agpm30ops.md): beenden und starten Sie den AGPM-Dienst, oder ändern Sie den Archivierungspfad, das AGPM-Dienstkonto oder den Port, auf dem der AGPM-Dienst lauscht.

-   [Verschieben Sie den AGPM-Server und das Archiv](move-the-agpm-server-and-the-archive.md): Verschieben Sie den AGPM-Dienst, das Archiv oder beides auf einen anderen Server.

Da die Rolle des AGPM-Administrators auch die Berechtigungen für alle anderen Rollen umfasst, kann ein AGPM-Administrator die Aufgaben ausführen, die normalerweise mit einer anderen Rolle verknüpft sind.

-   [Durchführen von genehmigenden Aufgaben](performing-approver-tasks-agpm30ops.md)wie erstellen, bereitstellen oder Löschen von GPOs

-   [Durchführen von Editor Aufgaben](performing-editor-tasks-agpm30ops.md)wie bearbeiten, umbenennen, kennzeichnen oder Importieren von GPOs, Erstellen von Vorlagen oder Festlegen einer Standardvorlage

-   [Ausführen von Aufgaben mit Bearbeiter](performing-reviewer-tasks-agpm30ops.md), wie das Überprüfen von Einstellungen und Vergleichen von GPOs

### Weitere Überlegungen

Standardmäßig verfügt die AGPM-Administrator Rolle über Vollzugriff – alle AGPM-Berechtigungen:

-   Listeninhalt

-   Leseeinstellungen

-   Bearbeiten von Einstellungen

-   Erstellen eines GPO

-   Bereitstellen von Gruppenrichtlinienobjekten

-   Gruppenrichtlinienobjekt löschen

-   Optionen ändern

-   Ändern der Sicherheit

-   Erstellen einer Vorlage

Die Berechtigungen zum **ändern** und **Ändern der Sicherheit** sind eindeutig für die Rolle des AGPM-Administrators.

 

 





