---
title: Übersicht über Advanced Group Policy Management
description: Übersicht über Advanced Group Policy Management
author: dansimp
ms.assetid: 2c12f3b4-8472-4c5b-b7f8-1c98a80d6b47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94e47075ae865096f9fe7d327cc7b11cb54217d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809385"
---
# Übersicht über Advanced Group Policy Management


Mithilfe der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) können Sie die Funktionen der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) erweitern, um umfassende Änderungssteuerung und verbesserte Verwaltung für Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) bereitzustellen.

## Entwicklung von Gruppenrichtlinienobjekten mit Änderungssteuerung


Mit AGPM können Sie eine Kopie der einzelnen Gruppenrichtlinienobjekte in einem zentralen Archiv speichern, damit Gruppenrichtlinienadministratoren Sie offline anzeigen und ändern können, ohne die bereitgestellte Version des Gruppenrichtlinienobjekts unmittelbar zu beeinflussen. Darüber hinaus speichert AGPM eine Kopie jeder Version jedes gesteuerten Gruppenrichtlinienobjekts im Archiv, sodass Sie bei Bedarf auf eine frühere Version zurückgreifen können.

Die Begriffe "Einchecken" und "Auschecken" werden ebenso wie in einer Bibliothek (oder in Anwendungen, die Änderungssteuerung, Versionskontrolle oder Quellcodeverwaltung für die Programmierungs Entwicklung bereitstellen) verwendet. Wenn Sie ein Buch in einer Bibliothek verwenden möchten, können Sie es in der Bibliothek Auschecken. Niemand sonst kann es verwenden, wenn es ausgecheckt ist. Wenn Sie das Buch nicht mehr haben, können Sie es wieder in die Bibliothek einchecken, damit es von anderen verwendet werden kann.

Wenn Sie diese GPO-Steuerelementfeatures verwenden möchten, klicken Sie im Gruppenrichtlinien-Verwaltungs-Editor auf einen Knoten zum Ändern des Steuerelements. Der Knoten Change Control wird nur angezeigt, wenn Sie den AGPM-Client installiert haben.

Wenn Sie GPOs mithilfe von AGPM entwickeln:

1.  Erstellen eines neuen kontrollierten Gruppenrichtlinienobjekts oder Steuern eines zuvor unkontrollierten Gruppenrichtlinienobjekts

2.  Überprüfen Sie das Gruppenrichtlinienobjekt, damit Sie und nur Sie es ändern können.

3.  Bearbeiten Sie das Gruppenrichtlinienobjekt.

4.  Überprüfen Sie das bearbeitete GPO, damit es von anderen geändert oder bereitgestellt werden kann.

5.  Überprüfen Sie die Änderungen.

6.  Stellen Sie das Gruppenrichtlinienobjekt in der Produktionsumgebung bereit.

## Rollenbasierte Delegierung


AGPM bietet eine umfassende, einfach zu verwendende rollenbasierte Delegierung für die Verwaltung des Zugriffs auf GPOs im Archiv. Berechtigungen auf Domänenebene ermöglichen AGPM-Administratoren den Zugriff auf einzelne Domänen, ohne Zugriff auf andere Domänen zu gewähren. Die GPO-basierte Delegierung ermöglicht AGPM-Administratoren den Zugriff auf bestimmte GPOs, ohne domänenweiten Zugriff bereitzustellen.

In AGPM gibt es speziell definierte Rollen: AGPM-Administrator (Vollzugriff), genehmigende Person, Editor und Bearbeiter. Die Rolle AGPM-Administrator umfasst die Berechtigungen für alle anderen Rollen. Standardmäßig haben nur genehmigende Personen die Möglichkeit, GPOs in der Produktionsumgebung einer Domäne bereitzustellen, um die Umgebung vor Fehlern durch die wenig erfahrenen Editoren zu schützen. Standardmäßig umfassen alle Rollen auch die Rolle Prüfer und damit die Möglichkeit, die GPO-Einstellungen in Berichten anzuzeigen. AGPM bietet jedoch einem AGPM-Administrator die Flexibilität, den Zugriff auf Gruppenrichtlinienobjekte so anzupassen, dass Sie den Anforderungen Ihrer Organisation entsprechen.

## Delegierung in einer mehr Gruppenrichtlinien-Administratorumgebung


In einer Umgebung, in der mehrere Personen GPOs ändern, delegiert ein AGPM-Administrator die Berechtigung für Redakteure, Genehmiger und Prüfer, entweder als Gruppen oder als Einzelpersonen. Einen typischen Entwicklungsprozess für Gruppenrichtlinienobjekte für einen Editor und eine genehmigende Person finden Sie unter [Checkliste: erstellen, bearbeiten und Bereitstellen eines Gruppenrichtlinienobjekts](checklist-create-edit-and-deploy-a-gpo-agpm40.md).

### Weitere Verweise

-   [Advanced Group Policy Management 4.0](advanced-group-policy-management-40.md)

 

 





