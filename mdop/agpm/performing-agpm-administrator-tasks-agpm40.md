---
title: Durchführen von AGPM-Administratoraufgaben
description: Durchführen von AGPM-Administratoraufgaben
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809343"
---
# Durchführen von AGPM-Administratoraufgaben


Mit der erweiterten Gruppenrichtlinienverwaltung (AGPM) kann ein AGPM-Administrator (Vollzugriff) domänenweite Optionen konfigurieren und Berechtigungen für genehmigende Personen, Bearbeiter, Bearbeiter und AGPM-Administratoren delegieren. Standardmäßig handelt es sich bei einem AGPM-Administrator um eine Person, die Vollzugriff hat – alle AGPM-Berechtigungen – und die daher Aufgaben ausführen kann, die mit einer Rolle verknüpft sind.

In einer Umgebung, in der mehrere Personengruppen Richtlinienobjekte (Group Policy Objects, GPOs) entwickeln, können Sie festlegen, dass alle Gruppenrichtlinienadministratoren dieselben Aufgaben ausführen und über die gleiche Zugriffsebene verfügen. Sie können aber auch festlegen, dass AGPM-Administratoren Berechtigungen für Editoren delegieren können, die Gruppenrichtlinienobjekte ändern und Genehmigern, die GPOs in der Produktionsumgebung bereitstellen. AGPM-Administratoren können Berechtigungen so konfigurieren, dass Sie den Anforderungen Ihrer Organisation entsprechen.

-   [Konfigurieren der erweiterten Gruppenrichtlinienverwaltung](configuring-advanced-group-policy-management-agpm40.md): Konfigurieren der AGPM-Server Verbindung und e-Mail-Benachrichtigung, Delegieren des Zugriffs auf GPOs in der Produktionsumgebung und Konfigurieren der Protokollierung und Ablaufverfolgung für die Problembehandlung.

-   [Verwalten des Archivs](managing-the-archive-agpm40.md): Delegieren des Zugriffs auf GPOs im Archiv, begrenzen der Anzahl der Versionen der einzelnen gespeicherten Gruppenrichtlinienobjekte, Importieren eines GPO aus einer anderen Domäne und sichern und Wiederherstellen des Archivs.

-   [Verwalten des AGPM-Diensts](managing-the-agpm-service-agpm40.md): beenden und starten Sie den AGPM-Dienst, oder ändern Sie den Archivierungspfad, das AGPM-Dienstkonto oder den Port, auf dem der AGPM-Dienst lauscht.

-   [Verschieben Sie den AGPM-Server und das Archiv](move-the-agpm-server-and-the-archive-agpm40.md): Verschieben Sie den AGPM-Dienst, das Archiv oder beides auf einen anderen Server.

**Hinweis**  Da die Rolle AGPM-Administrator die Berechtigungen für alle anderen Rollen umfasst, kann ein AGPM-Administrator die Aufgaben ausführen, die normalerweise mit einer anderen Rolle verknüpft sind.

[Durchführen von genehmigenden Aufgaben](performing-approver-tasks-agpm40.md)wie erstellen, bereitstellen oder Löschen von GPOs

[Durchführen von Editor Aufgaben](performing-editor-tasks-agpm40.md)wie bearbeiten, umbenennen, kennzeichnen oder Importieren von GPOs, Erstellen von Vorlagen oder Festlegen einer Standardvorlage

[Ausführen von Aufgaben mit Bearbeiter](performing-reviewer-tasks-agpm40.md), wie das Überprüfen von Einstellungen und Vergleichen von GPOs

 

### Weitere Überlegungen

Standardmäßig verfügt die AGPM-Administrator Rolle über Vollzugriff – alle AGPM-Berechtigungen:

-   Listeninhalt

-   Leseeinstellungen

-   Bearbeiten von Einstellungen

-   Erstellen eines GPO

-   Bereitstellen von Gruppenrichtlinienobjekten

-   Gruppenrichtlinienobjekt löschen

-   Exportieren von Gruppenrichtlinienobjekten

-   Importieren von Gruppenrichtlinienobjekten

-   Erstellen einer Vorlage

-   Optionen ändern

-   Ändern der Sicherheit

Die Berechtigungen zum **ändern** und **Ändern der Sicherheit** sind eindeutig für die Rolle des AGPM-Administrators.

 

 





