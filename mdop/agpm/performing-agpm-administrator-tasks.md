---
title: Durchführen von AGPM-Administratoraufgaben
description: Durchführen von AGPM-Administratoraufgaben
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808323"
---
# Durchführen von AGPM-Administratoraufgaben


Ein AGPM-Administrator (Vollzugriff) konfiguriert domänenweite Optionen und delegiert Berechtigungen für genehmigende Personen, Bearbeiter, Prüfer und andere AGPM-Administratoren. Standardmäßig handelt es sich bei einem AGPM-Administrator um eine Person mit Vollzugriff (alle erweiterten Gruppenrichtlinienverwaltung \ [AGPM \]-Berechtigungen), und Sie können daher auch Aufgaben ausführen, die mit einer Rolle verknüpft sind.

In einer Umgebung, in der mehrere Personengruppen Richtlinienobjekte (Group Policy Objects, GPOs) entwickeln, können Sie auswählen, ob alle Benutzer der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) dieselben Aufgaben ausführen und über die gleiche Zugriffsebene verfügen oder ob AGPM-Administratoren Berechtigungen für Bearbeiter delegieren, die Änderungen an GPOs vornehmen, und Genehmigern, die GPOs in der Produktionsumgebung bereitstellen. AGPM-Administratoren können Berechtigungen so konfigurieren, dass Sie den Anforderungen Ihrer Organisation entsprechen.

-   [Konfigurieren der AGPM-Server-Verbindung](configure-the-agpm-server-connection.md)

-   [Konfigurieren von E-Mail-Benachrichtigungen](configure-e-mail-notification.md)

-   [Delegieren des Domänenebenenzugriffs](delegate-domain-level-access.md)

-   [Delegieren des Zugriffs auf eine einzelne Gruppenrichtlinienobjekte](delegate-access-to-an-individual-gpo.md)

-   [Konfigurieren von Protokollierung und Ablaufverfolgung](configure-logging-and-tracing.md)

-   [Verwalten des AGPM-Dienstes](managing-the-agpm-service.md)

    -   [Starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service.md)

    -   [Ändern des Archivpfads](modify-the-archive-path.md)

    -   [Ändern des AGPM-Dienstkontos](modify-the-agpm-service-account.md)

    -   [Ändern Sie den Port, den der AGPM-Dienst überwacht](modify-the-port-on-which-the-agpm-service-listens.md)

Da die Rolle des AGPM-Administrators auch die Berechtigungen für alle anderen Rollen umfasst, kann ein AGPM-Administrator die Aufgaben ausführen, die normalerweise mit einer anderen Rolle verknüpft sind.

-   [Durchführen von genehmigenden Aufgaben](performing-approver-tasks.md)wie erstellen, bereitstellen oder Löschen von GPOs

-   [Durchführen von Editor Aufgaben](performing-editor-tasks.md)wie bearbeiten, umbenennen, kennzeichnen oder Importieren von GPOs, Erstellen von Vorlagen oder Festlegen einer Standardvorlage

-   [Ausführen von Aufgaben mit Bearbeiter](performing-reviewer-tasks.md), wie das Überprüfen von Einstellungen und Vergleichen von GPOs

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

 

 





